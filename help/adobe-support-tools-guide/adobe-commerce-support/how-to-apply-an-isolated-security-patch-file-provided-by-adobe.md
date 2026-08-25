---
title: 如何套用Adobe提供的獨立修補程式
description: 本文會說明如何針對Adobe Commerce內部部署、Adobe Commerce on Cloud基礎架構和Magento Open Source套用隔離修補程式。
feature: Best Practices, Compliance, Console
solution: Commerce
feature-set: Commerce
autotag-review: '2026-08-19T13:22:21.768Z'
TQID: 'https://experienceleague.adobe.com/tmaNqB6uOX2ukmfxQvcqFvYwm2UyO6USzb7t8hFQM1A'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: b5f00040-57a0-4a6d-a39e-383b1936c2c9
source-git-commit: 45b00b9b0d2ceb422747c0a4a34f060f33ab127b
workflow-type: tm+mt
source-wordcount: 219
ht-degree: 0%

---

# 如何套用Adobe提供的獨立修補程式

本文會說明如何針對Adobe Commerce內部部署、Adobe Commerce on Cloud基礎架構和Magento Open Source套用隔離修補程式。

>[!WARNING]
>
>我們強烈建議先在中繼/整合環境中套用及測試修補程式，然後再將其套用至生產環境。 我們也建議您在進行任何操作之前先使用最近的備份。

## 如何在雲端基礎結構上套用Adobe Commerce的隔離修補程式 {#cloud}

1. 如果您的專案根目錄中沒有`m2-hotfixes`目錄，請建立目錄。
1. 將`%patch_name%.patch`檔案複製到`m2-hotfixes`目錄。
1. 新增、認可及推送您的程式碼變更：

   ```git
   git add -A
   ```

   ```git
   git commit -m "Apply %patch_name%.patch patch"
   ```

   ```git
   git push origin
   ```

如需將修補程式套用至雲端專案的其他資訊，請參閱[套用修補程式](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/develop/upgrade/apply-patches)。

## 如何為Adobe Commerce內部部署和Magento Open Source套用隔離修補程式 {#commerce}

1. 將修補程式上傳至您的Adobe Commerce內部部署或Magento Open Source根目錄。
1. 執行下列SSH命令：

   ```bash
   patch -p1 < %patch_name%.patch
   ```

   （如果上述命令無法運作，請嘗試使用`-p2`而非`-p1`）

1. 若要反映變更，請在&#x200B;**[!UICONTROL 系統]** > **[!UICONTROL 快取管理]**&#x200B;下的[!UICONTROL 管理員]中重新整理快取。
