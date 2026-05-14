---
title: 如何請求雲端基礎結構上的臨時Adobe Commerce升級
description: 如果您的組織正在規劃您預期會有高流量的線上活動，或您突然發現您的網站正在進行高流量活動，您可以提出[支援票證](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html?lang=en#submit-ticket)以請求雲端基礎結構存放區中Adobe Commerce的臨時額外雲端容量。
solution: Commerce
exl-id: 203882c0-929a-4bb3-afff-738bc518b46b
TQID: https://experienceleague.adobe.com/9--JwGLuX01kXR569r1OjVrkiTd2BQa-j-gOTs9oKGY
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: dac87252-6066-4d6e-a9d2-f6d84c323de7id: e8818fe6-9c8b-4bc0-9ef8-377a10b7bc75
subfeature_v2: id: f8ddfd3b-6194-46e8-a176-0e918039be56
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: d1c3158bb425e7966ccc5e5d79457c6b33e00063
workflow-type: tm+mt
source-wordcount: 1136
ht-degree: 1%

---

# 如何請求雲端基礎結構上的臨時Adobe Commerce升級

如果您的組織正在計畫發生您預期的高流量線上活動，或您突然發現您的網站正在發生高流量活動，您可以提出[支援票證](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html?lang=en#submit-ticket)，為雲端基礎結構存放區上的Adobe Commerce請求暫時的額外雲端容量。

>[!NOTE]
>
>非緊急擴充請求需要48個營業時間通知。 除非網站完全無法運作，或接收的流量比預期的要高很多，且效能已嚴重降低，否則促銷活動的向上擴展不會被視為緊急情況。

## 受影響的產品和版本

* 雲端基礎結構上的Adobe Commerce，所有[支援的版本](https://www.adobe.com/content/dam/cc/en/legal/terms/enterprise/pdfs/Adobe-Commerce-Software-Lifecycle-Policy.pdf)。

## 如何識別高流量事件

在New Relic警報中，您可以使用基準警報條件來定義臨界值，以調整資料的行為。

基準線警示對於建立下列警示條件非常有用：

* 只在資料行為異常時通知您。
* 動態調整以因應不斷變化的資料和趨勢，包括每日或每週趨勢。

此外，當您還沒有已知行為時，基準線警報在新應用程式中可正常運作。

請依照此連結深入瞭解New Relic [套用智慧的異常偵測](https://docs.newrelic.com/docs/alerts-applied-intelligence/applied-intelligence/anomaly-detection/anomaly-detection-applied-intelligence/)。

如果您收到建議高流量事件的警示通知，您可能需要考慮[提交支援票證](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html?lang=en#submit-ticket)以要求額外的容量。 請遵循下列步驟。

## 如何監控網站效能

Adobe為雲端基礎結構上的Adobe Commerce提供一組New Relic警報政策專業計畫架構和雲端基礎結構上的Adobe Commerce入門計畫架構生產環境可追蹤以下關鍵績效指標：

* [Apdex分數](https://docs.newrelic.com/docs/apm/new-relic-apm/apdex/apdex-measure-user-satisfaction)
* 錯誤率
* 磁碟空間（僅適用於Pro架構生產環境）

這些原則會根據業界最佳實務，設定影響效能的警告和嚴重狀況的臨界值。 當您的網站遇到觸發警報臨界值的基礎結構或應用程式問題時，New Relic會傳送警報通知，以便您主動解決問題。 若要使用這些原則，您必須設定接收警示訊息的通知通道。

請依照此連結瞭解如何[設定效能型警示](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/monitor/new-relic/new-relic-service#monitor-performance-with-managed-alerts)。

## 請求臨時擴充的步驟

若要要求暫時性的額外雲端容量，請在Adobe Commerce支援中心提交[支援票證](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html?lang=en#submit-ticket)，並提供下列資訊：

>[!NOTE]
>
>*假期突波要求*&#x200B;選項只能選擇在10月到12月之間。

1. 選取您需要支援的[!DNL Adobe Commerce]產品：
   * [!DNL Commerce Cloud]
   * [!DNL Commerce on Managed Service]

1. 填入下列欄位：
   * **[!UICONTROL 案例標題]**
   * **[!UICONTROL 案例描述]** *（請確定這些描述清楚說明問題和內容。）*

1. 從&#x200B;**[!UICONTROL 問題原因]**&#x200B;下拉式功能表中選取&#x200B;*基礎結構變更要求*。

1. 從下拉式功能表中選擇&#x200B;**[!UICONTROL 環境]**。

1. 從下拉式功能表中選取適當的&#x200B;**[!UICONTROL 產品版本]**。

1. 從&#x200B;**[!UICONTROL 您今天想要進行的基礎變更]**&#x200B;下拉式選單中選擇&#x200B;*雲端專案調整大小(vCPU)*。

1. **選取[!UICONTROL 架構]**：
   * *預設架構：*&#x200B;從&#x200B;**選取大小**&#x200B;下拉式功能表中選取&#x200B;*下一個可用大小*。
   * *縮放架構：*&#x200B;選取時，畫面會變更為顯示兩個額外的欄位：
      * *網頁節點的大小*
      * *服務節點的大小* *（請輸入每個節點的所需大小。）*

1. 以UTC格式（日期和時間）輸入&#x200B;**[!UICONTROL 開始日期]**。

1. 輸入UTC格式的&#x200B;**[!UICONTROL 截止日期]** （日期和時間）。

1. 提供&#x200B;**[!UICONTROL 專案URL]** *（可在https://accounts.magento.cloud/下找到，通常採用`https://[REGION].magento.cloud/projects/PROJECT_ID`格式）*

1. 輸入&#x200B;**[!UICONTROL 專案識別碼]**。

1. 提供&#x200B;**[!UICONTROL 受影響的URL]** *（必須以`http://`或`https://`開頭。）*

1. 選取&#x200B;**[!UICONTROL 優先順序]**。

1. 選取&#x200B;**[!UICONTROL 業務影響]**。

1. 確認&#x200B;**[!UICONTROL 時區]** *（例如，`(UTC-5:00) Indiana (East)`）*

1. 輸入&#x200B;**[!UICONTROL 電話號碼]** *（例如，`+12015550123`）*

1. 按一下&#x200B;**[!UICONTROL 提交]**，完成您的支援案例。

>[!NOTE]
>
>排定擴充功能後，自動化系統會調整雲端例項的大小。 程式完成時，您可能無法收到任何票證通知。 您可以使用Adobe Commerce觀察工具，檢視您的AWS或Azure執行個體型別，以[驗證變更](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/how-to/check-vcpu-using-observation-for-adobe-commerce)。

## 檢視您的升級記錄

您可以向&#x200B;**CSM （客戶成功經理）**要求資訊，以檢視要求調整大小的歷程記錄。
下列資訊適用於每個調整大小請求：

* **大小開始日期**： upsize要求的日期。
* **大小結束日期**：叢集回復到先前大小的日期。
* **vCPU大小**：叢集在放大後的大小。
* **天使用量**：叢集維持擴大多長時間。
* **週期vCPU**：已依據使用天數變更vCPU大小。 （例如，vCPU大小192 x 25天等於4,800）。


## 相關閱讀

* 如需如何衡量及改善網站績效的深入分析、方法和範例，請參閱我們的支援知識庫中的下列深入文章：
   * [雲端上Adobe Commerce的CPU配置計算](https://experienceleague.adobe.com/zh-hant/docs/commerce-knowledge-base/kb/how-to/magento-commerce-cloud-cpu-allocation-calculation)
   * [檢查雲端上的Adobe Commerce是否需要主機執行個體的大小調整](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/how-to/magento-commerce-cloud-check-if-upsize-for-hosts-instances-is-needed)
   * [檢查雲端上Adobe Commerce的主機CPU設定](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/how-to/magento-commerce-cloud-check-hosts-cpu-configuration)
* 如需如何識別中斷的詳細資訊，請參閱我們的支援知識庫中的[識別並測量雲端上Adobe Commerce的中斷](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/how-to/how-to-identify-outages)。
* 如需改善網站效能以避免使用容量增加之需要的資訊，請參閱我們的開發人員檔案中的下列文章：
   * [影像大小](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/products/digital-assets/product-image-config#product-image-resizing)
   * [全頁快取](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/tools/cache-management#full-page-caching)
   * [ECE-Tools](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/dev-tools/ece-tools/package-overview)
