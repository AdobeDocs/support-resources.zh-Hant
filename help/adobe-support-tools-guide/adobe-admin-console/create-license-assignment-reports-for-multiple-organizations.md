---
title: 為多個組織和產品建立授權指派報告
description: 從Global Admin Console產生、檢視及下載多個組織和產品的授權指派報告。
Feature-set: Experience Cloud Services
Solution: Admin Console
Feature: Admin Console
exl-id: e3380a89-8529-473f-bd17-efb05466eab9
source-git-commit: 74d2dd4eb999f91172eec4c3b5690e1e8b8bd293
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 1%

---

# 為多個組織和產品建立授權指派報告

瞭解全域管理員如何針對特定日期範圍產生並下載多個組織和產品的詳細授權報告，以便精確追蹤授權布建。

>[!NOTE]
>
>若要建立、檢視及匯出授權指派報告，請登入[Global Admin Console](https://global-admin-console.adobe.com/)，然後前往&#x200B;**[!UICONTROL 深入分析]** > **[!UICONTROL 報告]** > **[!UICONTROL 授權指派]**。

## 建立報告

授權指派報告可協助您主動監控授權布建並減少手動追蹤。 全域管理員可以為任意數量的子組織建立所選產品的授權指派報告，以監視所有部門的軟體授權布建資料。

1. 前往Global Admin Console中的&#x200B;**[[!UICONTROL Insights]](https://global-admin-console.adobe.com/insights)**&#x200B;標籤。
1. 在&#x200B;**[!UICONTROL 授權指派]**&#x200B;頁面上，選取&#x200B;**[!UICONTROL 建立報告]**。
1. 選取組織並選取&#x200B;**[!UICONTROL 下一步]**。 您可以使用&#x200B;**[!UICONTROL 全選]**&#x200B;按鈕，個別挑選每個組織或選取父項內的所有子組織。

   >[!NOTE]
   >
   >**瞭解無法選取特定組織的原因**：
   >如果下階組織沒有合約，或擁有與上階組織相同產品的個別企業合約，則無法建立授權指定報表。 例如，如果父組織的合約具有Adobe Acrobat，而子組織與其他合約的一部分具有相同，則產品配置會受限。 因此，在Global Admin Console中建立報表的能力也受到限制。 [瞭解如何使用這類組織的個別Admin Console](https://helpx.adobe.com/tw/enterprise/using/assignment-reports.html)追蹤布建。

   >[!NOTE]
   >
   >您只能為具有有效合約的組織建立指定報表。

1. 選取要包含在報告中的產品，然後選取&#x200B;**[!UICONTROL 下一步]**。

   >[!NOTE]
   >
   >**瞭解無法選取特定產品的原因**：
   >在Global Admin Console中無法配置的產品不會納入報告建立作業。 這目前包括某些數位體驗產品，例如[!DNL Workfront]、[!DNL Adobe Experience Manager]和[!DNL Adobe Experience Platform]，以及產品，例如[!DNL Adobe Firefly Services]、[!DNL Acrobat Sign]和[!DNL Adobe Stock]。 [您使用Adobe Admin Console來尋找這些產品的授權布建資料](https://helpx.adobe.com/tw/enterprise/using/assignment-reports.html)。

1. 選取要按月或年彙總報表。
1. 選取自訂日期範圍或從預設集選項中選擇。 您可以挑選從2020年6月18日開始直到前一天的任何開始日期，只要該日期不在合約開始日期之前。
1. 選取「下載&#x200B;**&#x200B;**」將報表匯出為CSV檔案。

報告開始處理並出現在&#x200B;**[!UICONTROL 授權指派]**&#x200B;頁面上，其中包含名稱、建立者、建立時間、日期範圍和狀態等詳細資訊。 準備就緒後，您會收到電子郵件通知，並自動下載報告。

任何全域管理員都可以在報表準備就緒後隨時使用報表名稱旁的&#x200B;**[!UICONTROL 下載]**&#x200B;圖示下載報表。

>[!NOTE]
>
>- 為確保反映最新資料，請在任何配置後48小時產生報表。
>- 報表在產生後會保留90天。

## 檢視和下載先前產生的報表

全域管理員可以檢視及下載貴組織中任何其他全域管理員所產生的授權指派報告。 但是，全域檢視器只能檢視授權指派報告的清單。

1. 前往Global Admin Console中的&#x200B;**[[!UICONTROL Insights]](https://global-admin-console.adobe.com/insights)**&#x200B;標籤。
1. 在&#x200B;**[!UICONTROL 授權指派]**&#x200B;頁面上，列出所有報告以及下列詳細資料：

   | 欄位 | 說明 |
   | ------------- | ------------------------------------------------------------------------------------------------- |
   | 名稱 | 已自動產生且無法編輯。 |
   | 建立者 | 產生報表的全域管理員。 |
   | 建立時間 | 建立報表的系統時間。 |
   | 日期範圍 | 為報表選取的日期範圍。 |
   | 狀態 | 如果報告已可供下載，**成功**；如果仍在產生報告，則&#x200B;**正在處理**。 |

1. 若要將報表匯出為CSV檔案，請選取報表旁的&#x200B;**[!UICONTROL 下載]**&#x200B;圖示。

## 知道您的授權指派報告

您下載的報表包含每個事件的下列資訊：

| 欄位 | 說明 |
| -------------------------------- | -------------------------------------------------------- |
| 組織 ID | 繫結至上層組織的唯一ID |
| 組織名稱 | 父級組織的名稱 |
| 子組織ID | 所選子組織的唯一識別碼 |
| 子組織名稱 | 子組織的名稱 |
| 授權ID | 產品授權的唯一識別碼 |
| 產品名稱 | 所選產品的名稱 |
| 日期 | 日期選擇 |
| 授權數量總計 | 父級組織層級的授權總數 |
| 子授權 | 配置給子組織的授權計數 |
| 每月/每年尖峰指派數量 | 授權布建的彙總值（每月/每年） |
