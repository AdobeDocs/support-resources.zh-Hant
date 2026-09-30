---
title: Adobe Commerce假日整備概覽
description: 針對高流量事件（例如節日假期）在雲端基礎結構環境中準備Adobe Commerce的執行層級指引。
feature-set: Commerce
feature: Support
solution: Commerce
role: Developer, Admin, Leader
TQID: 'https://experienceleague.adobe.com/63svzoaJbKTgiO3iJR3iCyr4-slOLmt4QaVT2Y--NYI'
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
source-git-commit: 7ffe3c23f94b67342f02ed655d0a1700dd8f5a02
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 0%
---

# Adobe Commerce假日整備概覽

本教戰手冊提供指導，協助您為Adobe Commerce環境做好因應假期等高流量事件的準備。 將技術建議整合為五個策略重點領域：

- 效能最佳化
- 最佳實務和穩定性
- 監視和可觀察性
- 擴充性與容量規劃
- 營運整備

這些重點區域可協助確保您的平台在尖峰負載下保持穩定、安全且效能。

## 效能最佳化

以下概略介紹確保最佳化效能的建議步驟。 如需詳細資訊，請參閱[Adobe Commerce假日整備>效能最佳化](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/performance-optimization.md)。

* 最佳化Fastly請求快取：標準化您的促銷追蹤引數，確認您的登入頁面可快取，並使用適用於PWA或Headless店面的GraphQL GET來提高您的Fastly快取命中率。
* 啟用Fastly IO：開啟Fastly影像最佳化和Deep IO，讓影像轉換在CDN邊緣而不是來源執行，以減少影像密集型店面的頁面轉譯時間。
* 啟用L2快取：將快取資料儲存在每個網頁節點本機，以縮短延遲並減少對Redis/Valkey的網路呼叫，具體取決於您的Adobe Commerce版本。 Adobe Commerce 2.4.9或更新於2.4.5-p16、2.4.6-p14、2.4.7-p9和2.4.8-p4的修補程式版本不支援Redis快取。
* 啟用從屬連線：將讀取繁重的查詢路由傳送到具有`MYSQL_USE_SLAVE_CONNECTION`和`REDIS_USE_SLAVE_CONNECTION`或`VALKEY_USE_SLAVE_CONNECTION`的復本節點，這樣主資料庫就不會成為載入瓶頸。
* 啟用非同步訂購和電子郵件處理：佇列訂購位置、訂購資料網格更新，以及結帳電子郵件可在三個不同設定中的背景執行，因此結帳速度在高訂購量下保持快速。
* 將索引器切換為「依排程更新」模式：將索引器從「儲存時更新」移至cron驅動的「依排程更新」模式，以避免在經常更新目錄時鎖定（customer_grid索引器除外）。
* 考慮縮放（分割）架構：如果調校和程式碼層級的修正仍使CPU在負載下處於最大限度，請改用可獨立縮放Web和資料庫節點的六節點分割層設定。

## 最佳實務和穩定性

以下為確保執行個體穩定性的最佳實務概觀。 如需每一個專案的詳細步驟，請參閱[Adobe Commerce假日整備>最佳實務與穩定性](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/best-practices-stability.md)。

* 升級至最新的Adobe Commerce版本：保持在支援的版本，以保留Adobe每個版本隨附的安全性修正和效能改善。
* 安裝最新的ECE-Tools and Quality Patch Tool (QPT)：更新ece-tools及其相依性，並確認適用的品質修補工具修正已套用，適用於雲端和內部部署安裝。
* 檢閱及清除記錄檔：移除偵錯記錄並監控週期性錯誤，以防止磁碟過度使用並改善記錄可見度。
* 監控磁碟大小成長：將共用檔案和資料庫磁碟區的使用率保持在70%以下，這樣儲存容量成長就不會觸發中斷。
* 檢閱慢速資料庫查詢：使用APM工具和MySQL慢速查詢記錄來尋找和修正高成本的查詢，然後才在尖峰流量下複合。
* 正確設定cron作業：確認cron在正確的使用者下每分鐘執行一次，因為Commerce中的每個非同步操作都取決於它。
* 最佳化使用者端設定：開啟CSS、JavaScript和HTML縮制及套件組合，以加速店面載入時間。

## 監視和可觀察性

以下是旺季期間監控Adobe Commerce執行個體的建議方法。 如需這些監控與可觀察性建議的詳細步驟，請參閱[Adobe Commerce假期整備>監控與可觀察性](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/monitoring-observability.md)。

* 透過New Relic監控流量：使用串流至New Relic的Fastly記錄檔來找出流量異常、濫用IP、以支付之類的端點為目標的惡意請求，以及裝置/瀏覽器趨勢。
* 自訂New Relic警報：在Adobe管理的警報基礎上，針對異常流量、GraphQL查詢速度緩慢或錯誤率上升，設定您自己的NRQL型警報。
* 追蹤Apdex分數：觀看Apdex分數（目標≥0.85），將後端和前端回應時間保持在使用者認為滿意的範圍內。
* 檢閱支援深入分析（SWAT報告）：在尖峰事件之前和之後執行SWAT報告，以識別系統層級的風險和改善領域。

## 擴充性與容量規劃

如需這些擴充性與容量規劃建議的詳細步驟，請參閱[Adobe Commerce假期整備>擴充性與容量規劃](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/scalability-capacity-planning.md)。

* 及早規劃叢集升級：在重大升級之前至少10個工作日，向Adobe支援請求臨時計算升級。
* 啟用Fastly來源遮蔽：透過您來源附近的遮蔽POP路由未快取的請求，以減少直接點選來源伺服器的請求。
* 執行載入和容錯移轉測試：在主要行銷活動之前測試載入和復原案例，以確認您的擴充和復原計畫實際有效。

## 營運整備

* 套用所有安全性和效能修補程式：在程式碼凍結前完成所有修補程式，以便稍後不會中斷部署。
* 執行假期前的健康情況檢查：測試備份、cron健康情況以及快取熱身指令碼，讓作業在負載下順利執行。
* 建立監控教戰手冊：記錄警報臨界值、向上呈報路徑和24x7連絡人，讓團隊可以在尖峰期間快速回應。
* 檔案復原計畫：讓已建立版本的復原策略準備就緒，以便您能夠從錯誤的部署快速復原。