---
title: 效能最佳化
description: 效能最佳化建議，可協助Adobe Commerce商戶針對佳節假期等高流量活動準備環境。
feature-set: Commerce
feature: Support
solution: Commerce
role: Developer, Admin, Leader
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: cdfd3bc1-dc23-5cf0-b965-d3c0c55cde67
    internal-label: Best Practices
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: e8818fe6-9c8b-4bc0-9ef8-377a10b7bc75
    internal-label: Architecture
subfeature_v2:
  - id: f8ddfd3b-6194-46e8-a176-0e918039be56
    internal-label: Cloud architecture
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: b2220ea4cb5a301cbee6cea5fb90d6dc8a05eeff
workflow-type: tm+mt
source-wordcount: '1698'
ht-degree: 0%
---

# 效能最佳化

本節提供相關技術建議，說明如何在雲端基礎結構和內部部署上準備Adobe Commerce環境，以因應假期之類的高流量事件。

>[!NOTE]
>
>標示為&#x200B;**（僅限雲端）**&#x200B;的步驟適用於雲端基礎結構上的Commerce。 大部分其他建議也適用於內部部署。

## 最佳化Fastly請求快取（僅限雲端） {#optimize-fastly-request-caching}

[!DNL Fastly]會在邊緣快取回應，以減少原始伺服器的負載。 在高峰季節，一些設定檢查可協助您善加利用快取，尤其是當您使用追蹤引數或Headless店面執行促銷活動時。 如需完整的組態參考，請參閱[自訂快取組態](https://experienceleague.adobe.com/zh-hant/docs/commerce-on-cloud/user-guide/cdn/setup-fastly/fastly-custom-cache-configuration)。

* 標準化追蹤引數：在節日期間，您可能會執行社交和付費行銷活動（例如Google Ads、Facebook和X），這些會將唯一的追蹤字串附加至每個URL。 每個唯一字串會為原本屬於相同頁面的內容建立個別的快取專案，以降低快取命中率。 將這些引數新增至Adobe Commerce管理員中[!DNL Fastly]設定的&#x200B;**[!UICONTROL 已忽略的URL引數]**&#x200B;清單，讓[!DNL Fastly]可將其視為同等專案。
* 確認您的登入頁面可快取：檢查每個促銷活動登入頁面上的`x-cache`回應標題。 可快取頁面在後續載入時傳回`HIT`或`HIT`/`MISS`配對。 如果標頭傳回`MISS, MISS`，表示頁面未快取，需要調查。
* 針對GraphQL查詢使用GET請求：如果您執行PWA或Headless店面，請將GraphQL查詢以`GET`請求的形式傳送，並將查詢包含在URL中，而非以`POST`請求的形式傳送。 [!DNL Fastly]只快取`GET`個請求，其中查詢是URL的一部分。 不快取內文中有傳送查詢的`GET`要求。

>[!NOTE]
>
>[!DNL Fastly]來源遮蔽也會影響快取效能。 如需組態詳細資訊，請參閱[Fastly來源遮蔽](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/scalability-capacity-planning.md#fastly-origin-shielding)。

## 啟用Fastly IO （僅限雲端） {#enable-fastly-io}

[!DNL Fastly] IO將影像調整大小和格式轉換解除安裝到[!DNL Fastly]邊緣網路，而非Adobe Commerce來源。 這可以降低伺服器負載，並提升影像密集型店面的頁面轉譯速度，這是高流量銷售期間常見的瓶頸。 如需設定選項，請參閱[Fastly影像最佳化](https://experienceleague.adobe.com/zh-hant/docs/commerce-on-cloud/user-guide/cdn/fastly-image-optimization)。

開始之前，請確認已設定來源遮蔽。[!DNL Fastly] IO需要來源遮蔽作為先決條件。 如需組態詳細資訊，請參閱[Fastly來源遮蔽](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/scalability-capacity-planning.md#fastly-origin-shielding)。

若要啟用[!DNL Fastly] IO：

1. 在Admin中，移至&#x200B;**[!UICONTROL Fastly設定]**&#x200B;頁面，並選取&#x200B;**[!UICONTROL 預設IO設定選項]**&#x200B;旁的&#x200B;**[!UICONTROL 設定]**。
1. 確認[!DNL Fastly] IO程式碼片段已啟用。
1. 在&#x200B;**[!UICONTROL 影像最佳化]**&#x200B;設定中，將&#x200B;**[!UICONTROL 啟用深層影像最佳化]**&#x200B;設定為&#x200B;*[!UICONTROL 是]*。 此設定會停用Adobe Commerce的內建影像調整大小功能，並將工作轉移到[!DNL Fastly]。
1. 確認遮蔽位置已正確設定。 如需組態詳細資訊，請參閱[Fastly來源遮蔽](#fastly-origin-shielding)。

>[!NOTE]
>
>深度影像最佳化只會調整產品影像的大小。 CMS影像（例如橫幅和內容區塊）不受影響，並繼續使用Adobe Commerce的內建調整大小。

若要確認[!DNL Fastly] IO正常運作，請檢查產品影像要求上的回應標頭：

* `x-cache`標頭傳回`HIT`。
* 已填入`fastly-io-info`和`fastly-stats`標頭。
* 影像URL在路徑中未包含`/cache/`目錄。

## 實作Redis L2快取 {#implement-redis-l2-cache}

實作有效的快取做法，讓您的存放區在流量尖峰季節可靠執行。[!DNL Redis] L2快取會將快取資料儲存在每個網頁節點本機，將網路頻寬減少到[!DNL Redis]。 如需L2快取運作方式的背景資訊，請參閱[第二級快取](https://experienceleague.adobe.com/zh-hant/docs/commerce-operations/configuration-guide/cache/level-two-cache)。

在雲端基礎結構上的Commerce上，設定`REDIS_BACKEND`部署變數來啟用此功能。 如需設定步驟，請參閱《雲端基礎結構上的Commerce指南》中的[REDIS_BACKEND](https://experienceleague.adobe.com/zh-hant/docs/commerce-on-cloud/user-guide/configure/env/stage/variables-deploy#redis_backend)。 內部部署，直接在`app/etc/env.php`中進行設定。

>[!NOTE]
>
>不支援[!DNL Redis]作為Adobe Commerce 2.4.9或更新版本上的L2快取後端，或是2.4.5-p16、2.4.6-p14、2.4.7-p9或2.4.8-p4之前的修補程式發行版本。 在這些版本中，請改用`VALKEY_BACKEND`。

## 啟用MySQL和Redis從屬連線（僅限雲端） {#enable-mysql-and-redis-slave-connections}

[!DNL Redis]和[!DNL MySQL]從屬連線會將讀取流量解除安裝到復本節點，減少高流量期間主連線的負載。 如需設定步驟，請參閱[MYSQL_USE_SLAVE_CONNECTION](https://experienceleague.adobe.com/zh-hant/docs/commerce-on-cloud/user-guide/configure/env/stage/variables-deploy#mysql_use_slave_connection)和[REDIS_USE_SLAVE_CONNECTION](https://experienceleague.adobe.com/zh-hant/docs/commerce-on-cloud/user-guide/configure/env/stage/variables-deploy#redis_use_slave_connection)或[VALKEY_USE_SLAVE_CONNECTION](https://experienceleague.adobe.com/zh-hant/docs/commerce-on-cloud/user-guide/configure/env/stage/variables-deploy#valkey_use_slave_connection) （視您的Adobe Commerce版本而定）。

### Redis從屬連線

[!DNL Redis]從屬連線是至[!DNL Redis]執行個體的唯讀連線，允許從非主節點提供讀取流量。 若未啟用，[!DNL MySQL]可能會遭遇高負載瓶頸。 檢查[!DNL New Relic]的APM概觀圖表，以取得上升的回應時間做為早期符號，然後依最耗時的交易排序，在&#x200B;**[!UICONTROL 資料庫]**&#x200B;索引標籤中確認，以識別緩慢的[!DNL MySQL] `SELECT`查詢。 透過將部署變數`REDIS_USE_SLAVE_CONNECTION`設定為`true`來啟用此功能。

>[!NOTE]
>
>`REDIS_USE_SLAVE_CONNECTION`僅在Staging和Production Pro叢集環境中受支援。 起始或縮放（分割）架構專案不支援此功能。 在Scaled架構上啟用它會造成[!DNL Redis]個連線錯誤 — 請改在該架構上使用[!DNL Redis] L2快取。 請參閱上述[實作Redis L2快取](#implement-redis-l2-cache-implement-redis-l2-cache)。

### MySQL從屬連線

啟用Pro叢集環境上的`MYSQL_USE_SLAVE_CONNECTION`旗標，以將特定的唯讀資料庫查詢導向從屬連線，從主連線解除安裝查詢執行。

>[!CAUTION]
>
>在生產環境中啟用任一設定之前進行負載測試。 在負載正常的環境中，從屬連線可能會使效能降低10%到15%。 在負載較重且持續較重的環境中，它們可以大幅提升效能。 在啟用之前評估預期旺季流量下。

## 啟用非同步訂單和電子郵件處理 {#enable-asynchronous-order-and-email-processing}

使用非同步處理在背景將大量訂單相關作業排入佇列並執行，減少尖峰流量期間的前端延遲。 這涵蓋三個相關但不同的設定 — 請參閱[組態最佳實務](https://experienceleague.adobe.com/zh-hant/docs/commerce-operations/performance-best-practices/configuration)以取得概覽。

* 非同步訂購位置： 「非同步訂購」模組會將訂單標示為已接收、將其置於佇列中，並處理先進先出的訂單。 預設為停用。 從命令列啟用它：

  ```
  bin/magento setup:config:set --checkout-async 1
  ```

  啟用後，無法立即取得訂單詳細資料 — 訂單會維持佇列狀態，直到`placeOrderProcess`消費者根據存貨（預設為啟用）驗證並更新為止。 在停用此模組之前，請確認所有執行中的非同步訂單皆已完成處理。 如需詳細資訊，請參閱[結帳效能最佳實務](https://experienceleague.adobe.com/zh-hant/docs/commerce-operations/performance-best-practices/high-throughput-order-processing)。

* 非同步處理訂單資料：密集的店面銷售和密集的訂單處理可能在資料庫層級發生衝突。 啟用此設定會區分這兩種流量模式，因此訂單會暫時儲存並大量移至Order Management格線，而不會發生衝突。 此排程會依cron更新「訂單」、「商業發票」、「出貨」及「銷退折讓單」等網格，避免鎖定並減少處理時間。 為了獲得最佳結果，請設定cron每分鐘執行一次。

  >[!NOTE]
  > 
  >啟用方式取決於您的部署模式。 雲端基礎結構暫存和生產環境上的Adobe Commerce預設以生產模式執行，其中無法透過管理員使用此設定。 在生產模式中，請改為執行`bin/magento config:set dev/grid/async_indexing 1`。 在預設模式下，移至&#x200B;**[!UICONTROL 商店]** > **[!UICONTROL 設定]** > **[!UICONTROL 進階]** > **[!UICONTROL 開發人員]** > **[!UICONTROL 格線設定]**，並將&#x200B;**[!UICONTROL 非同步索引]**&#x200B;設定為&#x200B;*[!UICONTROL 啟用]*。

  如需詳細資訊，請參閱[已排程的訂單作業](https://experienceleague.adobe.com/zh-hant/docs/commerce-admin/stores-sales/order-management/orders/order-scheduled-operations)。

* 非同步電子郵件通知：此設定會將結帳與訂單處理電子郵件通知移至背景。 在&#x200B;**[!UICONTROL 商店]** > **[!UICONTROL 設定]** > **[!UICONTROL 銷售]** > **[!UICONTROL 銷售電子郵件]** > **[!UICONTROL 一般設定]** > **[!UICONTROL 非同步傳送]**&#x200B;啟用它。

## 設定索引器以依排程更新 {#configure-indexers-for-update-on-schedule}

將索引器設定為以排程模式執行，以避免資料庫鎖定，並改善頻繁更新目錄時的回應能力。 如需詳細資訊，請參閱[索引器組態的最佳實務](https://experienceleague.adobe.com/zh-hant/docs/commerce-operations/implementation-playbook/best-practices/maintenance/indexer-configuration)。

索引子可以在儲存&#x200B;**時以**&#x200B;[!UICONTROL &#x200B; Update或排程&#x200B;]&#x200B;**模式下以** Update執行。

* 每當目錄或其他資料變更時，就立即&#x200B;**[!UICONTROL 儲存時更新]**&#x200B;索引。 假設更新和瀏覽強度低，在高負載下可能會導致嚴重延遲和資料無法使用。
* 建議將&#x200B;**[!UICONTROL 排程更新]**&#x200B;用於生產。 它會透過專用的cron工作，在背景中儲存資料更新和重新索引的相關資訊。

在&#x200B;**[!UICONTROL 系統]** > **[!UICONTROL 工具]** > **[!UICONTROL 索引管理]**&#x200B;分別設定每個索引器的更新模式。

>[!IMPORTANT]
>
>`customer_grid`索引子支援的模式取決於您的Adobe Commerce版本。 在2.4.8之前的版本上，「客戶網格」僅支援&#x200B;**[!UICONTROL 儲存時更新]**，請勿將其設定為&#x200B;**[!UICONTROL 排程更新]**。 在Adobe Commerce 2.4.8和更新版本上，Customer Grid支援這兩種模式，現在預設為&#x200B;**[!UICONTROL 依排程更新]**。

## 停用並評估型錄平面表格 {#disable-and-evaluate-catalog-flat-table}

不建議將平面表格用於產品和類別。 這項已棄用的功能可能會導致效能降低和索引問題。 如需詳細資訊，請參閱[一般目錄](https://experienceleague.adobe.com/zh-hant/docs/commerce-admin/catalog/catalog/catalog-flat)。

若要停用一般目錄，請移至&#x200B;**[!UICONTROL 商店]** > **[!UICONTROL 設定]** > **[!UICONTROL 目錄]** > **[!UICONTROL 目錄]** > **[!UICONTROL 店面]**，將&#x200B;**[!UICONTROL 使用一般目錄類別]**&#x200B;設定為&#x200B;*[!UICONTROL 否]*，將&#x200B;**[!UICONTROL 使用一般目錄產品]**&#x200B;設定為&#x200B;*[!UICONTROL 否]*，然後按一下&#x200B;**[!UICONTROL 儲存設定]**。

某些協力廠商模組和自訂專案確實需要平面表格才能正常運作。 在停用平面表格之前，評估繼續使用這些擴充功能的影響和風險。

## 考慮縮放（分割）架構（僅限雲端） {#consider-scaled-split-architecture}

如果在套用之前的設定和程式碼層級最佳化後，負載測試或即時基礎架構效能仍顯示CPU和其他資源已達上限，請考慮移至縮放（分割）架構。 如需詳細資訊，請參閱[縮放架構](https://experienceleague.adobe.com/zh-hant/docs/commerce-on-cloud/user-guide/architecture/scaled-architecture)。

>[!NOTE]
>
>擴充的架構僅適用於具有Pro 48或以上叢集的客戶。

分割層架構使用最少六個節點：三個執行[!DNL OpenSearch]或[!DNL Elasticsearch]、[!DNL MariaDB]和[!DNL Redis]或[!DNL Valkey]的服務節點，以及三個執行`php-fpm`和`NGINX`的Web節點。

* 服務節點只能透過增加伺服器大小（CPU和記憶體）垂直縮放。 因為資料庫叢集是專為高可用性而建置，所以服務節點無法以可靠的方式水準擴展。
* Web節點可以垂直和水平擴展，新增Web伺服器來處理增加的請求量。

這可讓您在高負載期間依需求擴充基礎架構，並獨立擴充每個階層。 若要在預期的高負載期間之前切換至分割層架構，請聯絡您的Adobe客戶團隊。
