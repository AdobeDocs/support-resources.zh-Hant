---
title: 下載稽核記錄和匯出報告
description: 瞭解全域管理員如何在Global Admin Console中檢視、篩選和匯出稽核記錄和報告。
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
exl-id: 4b562a4d-14e5-4687-a1ae-6a435f087627
source-git-commit: 8db982f6a642a288453086c23d20b44b14d55354
workflow-type: tm+mt
source-wordcount: '880'
ht-degree: 3%

---

# 下載稽核記錄和匯出報告

適用於企業。

瞭解全域管理員如何使用Global Admin Console檢視、篩選及匯出稽核記錄和報告。

若要開始使用，請登入[Global Admin Console](https://global-admin-console.adobe.com/)。 然後移至&#x200B;**[!UICONTROL 分析]**&#x200B;標籤，並選取&#x200B;**[!UICONTROL 稽核記錄]**&#x200B;以追蹤跨組織所做的所有變更。

## 檢視和下載稽核記錄

身為全域管理員，您可以完整檢視Global Admin Console中的變更。 您可以搜尋所有組織中的稽核記錄，以找出過去90天內採取的動作，包括動作發生的時間及執行者。
- 稽核記錄可防止不適當的系統存取並稽核組織內的可疑行為，有助於確保持續合規性。
- Global Admin Console中可用的記錄檔僅包含全域管理員有權存取的事件。 不包含使用者指派或使用者事件。 [深入瞭解](https://helpx.adobe.com/tw/enterprise/using/admin-console.html)每個主控台提供的不同功能。
- 記錄會涵蓋階層中所有組織的事件，讓您一次搜尋所有組織的稽核記錄。

>[!NOTE]
>
> 作為[Adobe Admin Console](https://adminconsole.adobe.com)組織中的系統管理員，您可以使用[稽核記錄](https://helpx.adobe.com/tw/enterprise/using/audit-logs.html)來檢閱使用者指派和使用者事件。 稽核記錄中也會包含所選組織的子組織中系統管理員所執行的動作。 深入瞭解系統管理員如何[追蹤在Admin Console中所做的變更](https://helpx.adobe.com/tw/enterprise/using/audit-logs.html)。

若要檢視或下載組織的稽核記錄：

1. 以全域管理員身分登入[Global Admin Console](https://global-admin-console.adobe.com/insights)。
1. 選取&#x200B;**[!UICONTROL 分析]** > **[!UICONTROL 稽核記錄]**。
稽核記錄會顯示已篩選事件的下列資訊：

   | 欄位 | 說明 |
   |------ |-------------|
   | 日期 | 事件的日期和時間，以當地時區顯示。 |
   | 活動名稱 | 所執行動作的說明。 |
   | 事件詳細資料 | 其他事件詳細資訊（如有）。 |
   | 物件名稱 | 與事件有關的產品、產品設定檔或使用者群組名稱（如適用）。 |
   | 受影響的使用者 | 受影響使用者的電子郵件地址（如適用）。 |
   | 管理 | 執行動作之管理員的電子郵件地址。 如果動作是由Adobe後端系統執行，則會顯示&#x200B;*系統*。 |
   | IP位址 | 執行動作之電腦的IP位址。 通常可反映實體位置，但可能是Proxy伺服器或VPN位址。 |
   | 組織 | 受事件影響的組織名稱。 |


1. 您可以使用以下選項篩選稽核記錄：

   - 依受影響的使用者或管理員進行搜尋。
   - 選取一或多個組織。
   - 定義日期範圍。
   - 依事件名稱篩選。
   - 您可以合併篩選器來縮小結果範圍，例如檢視特定組織過去七天的事件。

   ![稽核記錄](assets/audit-logs.png)

   *根據事件名稱、受影響的組織或日期範圍篩選稽核記錄。*

   ![select-organization](assets/select-organizations.png)

   *選取要篩選稽核記錄的組織。*

1. 若要匯出稽核記錄，請選取&#x200B;**[!UICONTROL 匯出CSV]**&#x200B;以匯出篩選的結果。 結果會以CSV格式下載。

如需匯出中包含之欄位的詳細資訊，請參閱[記錄結構描述](#log-schema)。

>[!NOTE]
>
>匯出的稽核記錄報告會在產生後保留90天。


## 瞭解您的稽核記錄報告 {#log-schema}

匯出的稽核記錄報告包含每個組織的下列欄位：

| 欄位 | 說明 |
|------|------------|
| id | 事件 ID |
| eventTime | 事件的日期和時間（當地時區） |
| eventType | 事件的名稱 |
| eventSubtype | 其他事件詳細資訊（如有） |
| actorEmail | 執行事件之管理員的電子郵件地址。 如果事件是由Adobe後端系統執行，則會顯示&#x200B;*系統*。 |
| targetUserEmail | 受影響使用者的電子郵件（如適用） |
| targetGroupName | 受影響的使用者群組（如適用） |
| targetProductName | 受影響的產品（如適用） |
| targetProfileName | 受影響的產品設定檔（如適用） |
| ipAddress | 執行動作之電腦的IP位址。 通常可反映實體位置，但可能是Proxy伺服器或VPN位址。 |
| organizationName | 受影響組織的名稱 |

## 下載匯出報告

當任何全域管理員從[Global Admin Console](https://global-admin-console.adobe.com/insights)匯出組織資料時，報告會經過處理，並可在&#x200B;**[!UICONTROL 匯出報告]**&#x200B;的&#x200B;**[!UICONTROL Insights]**&#x200B;索引標籤下使用。

任何全域管理員產生的所有報表都可在單一位置使用。 匯出報表功能在下列情況下相當實用：

- 如果您的大型階層包含許多組織，則不必再等待匯出檔案進行處理。 您可以使用其他管理員產生的報表。
- 您不再需要保留或儲存這些報表以便日後比較。 報表會保留90天，且您可以隨時下載報表以比較報表。


若要下載匯出報表：

1. 登入[Global Admin Console](https://global-admin-console.adobe.com/insights)並導覽至&#x200B;**[!UICONTROL Insights]** > **[!UICONTROL 匯出報表]**。

   系統會顯示過去90天內產生的報表。 90天完成後，您可以再次產生報表。 瞭解如何產生[組織結構](https://helpx.adobe.com/tw/enterprise/global-admin-console/export-and-import-data.html#export-and-import-organization-structure)的報告。


   | 欄位 | 說明 |
   |------|------------|
   | 報表 | 產生報表的日期和時間（當地時區） |
   | 格式 | 檔案格式(CSV、JSON、XLSX) |
   | 大小 | 檔案大小 |
   | 建立者 | 產生報表之管理員的電子郵件地址 |
   | 動作 | 下載報表的連結 |

1. 若要下載報表，請選取&#x200B;**[!UICONTROL 下載]**。

   如果您剛產生的報告未出現在清單中，請選取&#x200B;**[!UICONTROL 重新整理]**。

   ![export-reports](assets/export-reports.png)

*下載過去90天內產生的任何報告。*
