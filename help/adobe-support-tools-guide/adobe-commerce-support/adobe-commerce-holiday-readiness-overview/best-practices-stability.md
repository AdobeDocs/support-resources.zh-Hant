---
title: 最佳實務和穩定性
description: 最佳實務和穩定性建議，可協助Adobe Commerce商家為高流量事件（例如節日季節）準備環境。
feature-set: Commerce
feature: Support
solution: Commerce
role: Developer, Admin, Leader
TQID: 'https://experienceleague.adobe.com/iA6ioGYYgQSotPrPqujDBdRcjBLUQXMGXfwlcSMGjkM'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: cdfd3bc1-dc23-5cf0-b965-d3c0c55cde67
    internal-label: Best Practices
  - id: 5a951749-fac9-5bc7-9a98-ebe4ff066437
    internal-label: Cloud
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
subfeature_v2:
  - id: 3c398179-d35a-51ba-b317-6c5b95feef5e
    internal-label: Logs
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 71589dd124714805fbf844540fb2d272433631ee
workflow-type: tm+mt
source-wordcount: '861'
ht-degree: 4%
---

# 最佳實務和穩定性

本節提供相關技術建議，說明如何在雲端基礎結構和內部部署上準備Adobe Commerce環境，以因應假期之類的高流量事件。

>[!NOTE]
>
>標示為&#x200B;**（僅限雲端）**&#x200B;的步驟適用於雲端基礎結構上的Commerce。 大部分其他建議也適用於內部部署。

## 升級至最新版Adobe Commerce {#upgrade-to-latest-version-of-adobe-commerce}

確認您的網站並非使用不受支援的Adobe Commerce版本，這可能會影響網站的效能，並增加安全性問題的弱點。 請升級至最新版Adobe Commerce，確保安全性並準備好因應節日季節。

Adobe Commerce的[最新版本](https://experienceleague.adobe.com/zh-hant/docs/commerce-operations/release/notes/overview)包含許多[重要安全性修正](https://experienceleague.adobe.com/zh-hant/docs/commerce-operations/release/notes/security-patches/overview)，包括增強功能和已緩解的問題，當您從舊版升級時，這些修正將有益於您的專案。

如需不支援之Adobe Commerce版本的詳細資訊，請檢閱[Adobe Commerce生命週期原則](https://experienceleague.adobe.com/zh-hant/docs/commerce-operations/release/planning/lifecycle-policy)。

## 安裝最新的ECE-Tools and Quality Patch Tool (QPT) {#install-latest-ece-tools-and-quality-patch-tool-qpt}

使用`--with-dependencies`引數確保已安裝最新的`ece-tools`模組及其相依模組，以便針對您的Adobe Commerce版本正確安裝所有必要的雲端修補程式。 如需步驟，請參閱[更新ECE-Tools套件](https://experienceleague.adobe.com/zh-hant/docs/commerce-on-cloud/user-guide/dev-tools/ece-tools/update-package)。

檢閱「品質修補程式工具」中可用的修補程式清單，並確定已套用與您的Adobe Commerce版本相容的效能修補程式。 請參閱[品質修補工具：搜尋修補程式](https://experienceleague.adobe.com/zh-hant/docs/commerce-operations/tools/quality-patches-tool/patches-available-in-qpt/patches-available-in-qpt-tool-overview)。

>[!NOTE]
>
>QPT適用於雲端基礎結構上的Adobe Commerce和內部部署安裝。 安裝和使用指令在這兩個指令之間有所差異 — 對於Cloud，QPT包含在ECE-Tools套件中。

## 檢閱和清除記錄檔 {#review-and-clean-log-files}

檢閱雲端環境中的記錄檔（例如，`~/var/log`下的應用程式記錄檔），並識別寫入預設或自訂記錄檔的任何經常記錄的記錄。 如需詳細資訊，請參閱[檢視及管理記錄檔](https://experienceleague.adobe.com/zh-hant/docs/commerce-on-cloud/user-guide/develop/test/log-locations)。

* 檢閱下列預設記錄檔並修正週期性錯誤： `~/var/log`、`~/var/log/exception.log`、`~/var/log/support_report.log`、`~/var/log/system.log`、`~/var/report`。
* 移除先前為疑難排解過去問題而新增的偵錯記錄。

[!DNL New Relic]中也提供這些記錄，請參閱[New Relic記錄管理](https://experienceleague.adobe.com/zh-hant/docs/commerce-on-cloud/user-guide/monitor/new-relic/log-management)。

## 監控磁碟大小成長 {#monitor-disk-size-growth}

您在雲端基礎結構上的Adobe Commerce有兩個主要磁碟區。 監視這些磁碟區，以確保在有大量流量時，它們有足夠的可用空間。 當任一磁碟區的使用量達到70%以上時，Adobe Commerce會發出警告。

* `/mnt/shared` （共用檔案，包括記錄檔和媒體檔案）
* `/data/mysql` （資料庫磁碟區）

如需詳細資訊，請參閱[管理磁碟空間](https://experienceleague.adobe.com/zh-hant/docs/commerce-on-cloud/user-guide/develop/storage/manage-disk-space)。

## 檢閱最慢的資料庫要求 {#review-slowest-database-requests}

請務必定期監視和檢閱[!DNL New Relic]中最耗時的資料庫交易。 調查明顯緩慢的查詢和元件。

* **檢查最耗時的交易：**&#x200B;移至&#x200B;**[!UICONTROL New Relic]** > **[!UICONTROL APM與服務]** >選取環境> **[!UICONTROL 資料庫]**，然後依最耗時的交易排序。

* **檢查MySQL緩慢查詢記錄：**&#x200B;檢閱`mysql-slow.log`系統記錄的緩慢查詢。 [!DNL New Relic]中也提供這些記錄檔：移至&#x200B;**[!UICONTROL New Relic]** > **[!UICONTROL 記錄檔]**，並依`filePath:"/var/log/mysql/mysql-slow.log"`篩選。

請定期檢閱[!DNL MySQL]慢速查詢記錄檔，以確認慢速查詢不是經常執行。 如需解決您識別為有問題的查詢的步驟，請參閱[解決資料庫效能問題](https://experienceleague.adobe.com/zh-hant/docs/commerce-operations/implementation-playbook/best-practices/maintenance/resolve-database-performance-issues)。

## 設定cron作業 {#configure-cron-jobs}

Commerce中的所有非同步作業都是使用Linux cron命令執行。

Commerce仰賴重要系統功能的正確cron工作設定，包括編制索引和佇列消費者作業。 若未正確設定，表示Commerce將無法如預期運作。

使用Unix crontab檔案中的適當Unix使用者，正確設定和設定Commerce cron至關重要。 每個Unix使用者都有自己的crontab檔案，這是用來為該使用者執行cron作業的設定。 如需相關步驟，請參閱[設定並執行cron工作](https://experienceleague.adobe.com/zh-hant/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs)。

無法再執行指令碼`dev/tools/cron.sh`，因為它已被移除。

## 最佳化使用者端設定 {#optimize-client-side-settings}

若要改善Commerce執行個體的店面回應能力，請在&#x200B;**[!UICONTROL 商店]** > **[!UICONTROL 設定]** > **[!UICONTROL 進階]** > **[!UICONTROL 開發人員]**&#x200B;下設定下列設定，這些設定僅在開發人員模式下可用：

* **[!UICONTROL 格線設定]** > **[!UICONTROL 非同步索引]**： *[!UICONTROL 啟用]*
* **[!UICONTROL CSS設定]** — **[!UICONTROL 縮小CSS檔案]**： *[!UICONTROL 是]*
* **[!UICONTROL JavaScript設定]** — **[!UICONTROL 最小化JavaScript檔案]**： *[!UICONTROL 是]*
* **[!UICONTROL JavaScript設定]** — **[!UICONTROL 啟用JavaScript組合]**： *[!UICONTROL 是]* （預設未啟用）
* **[!UICONTROL 範本設定]** — **[!UICONTROL 縮小HTML]**： *[!UICONTROL 是]*

由於Adobe Commerce on Cloud一律在生產模式中執行，請改為從命令列設定每個選項（例如`bin/magento config:set --lock-config dev/css/minify_files 1`），然後提交產生的`app/etc/config.php`變更並重新部署。 如需CLI路徑的完整清單，請參閱[最佳化資源檔](https://experienceleague.adobe.com/zh-hant/docs/commerce-operations/implementation-playbook/best-practices/development/optimize-css-js-files)。
