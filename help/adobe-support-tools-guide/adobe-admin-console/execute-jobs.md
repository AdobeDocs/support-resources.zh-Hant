---
title: 執行擱置中的工作
description: 瞭解如何在Adobe Admin Console中執行擱置中的工作，以確保所有變更都套用至您的組織。
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
exl-id: 18549d19-7985-4a45-8894-e69836ddb23c
source-git-commit: ad324036dbeb2a54855349321b2ba33405d2c075
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 0%

---

# 執行擱置中的工作

此功能適用於使用[[!DNL Global Admin Console]](https://global-admin-console.adobe.com/)的企業組織。

- [[!DNL Global Admin Console]](https://global-admin-console.adobe.com/)中的變更分兩個階段完成：

   1. **編輯階段**：變更組織或配置產品。
   2. **執行階段**：檢閱並執行暫止的變更，使其生效。

- 若要確保[[!DNL Global Admin Console]](https://helpx.adobe.com/tw/enterprise/global-admin-console/adopt-global-administration.html)中所做的所有變更已實作並生效，請選取&#x200B;**[!UICONTROL 工作執行]**&#x200B;索引標籤，然後繼續執行暫止的變更。

  登入[[!DNL Global Admin Console]](https://global-admin-console.adobe.com/)。

## 變更的持續性和可見性

### 變更持續性

- 您可以登出並在稍後返回，而不會遺失擱置的變更。
- 未執行的變更：
   - 會在30天後捨棄。
   - 作業階段結束時會被清除，例如瀏覽器標籤或視窗關閉時。

&#x200B;> [!NOTE]
>
> 請立即執行重要變更，以確保成功套用變更。

### 多個管理員和衝突

- 在同一個組織工作的兩名管理員：
   - 不要看到彼此的未執行變更。
   - 僅在下列時間後檢視變更：
      - 執行，以及
      - 正在重新整理顯示或重新登入。
- 未執行的變更可能會與已執行的變更發生衝突。

### 衝突處理

報告衝突：
- 在執行時，或
- 資料重新整理時（例如，登出再登入後）。

## 正在執行暫止的變更

身為全域管理員，您可以從&#x200B;**[!UICONTROL 工作執行]**&#x200B;索引標籤檢閱及執行暫止的變更。

### 執行變更的步驟

1. 登入[!DNL Global Admin Console]。
2. 從左側導覽面板中選取&#x200B;**[!UICONTROL 工作執行]**&#x200B;索引標籤。
3. 檢閱擱置的變更。
4. 選取&#x200B;**[!UICONTROL 送出變更]**&#x200B;以執行變更。

送出工作之後：

- 工作進入執行佇列。
- 工作執行時的狀態為&#x200B;**[!UICONTROL 擱置中]**。
- Adobe建議一次只執行一個工作，以實現可預測性及更輕鬆的疑難排解。

&#x200B;> [!IMPORTANT]
>
> 如果在執行期間發生錯誤，任何未成功套用的變更都必須重新輸入並重新提交。

### 長期執行的分配

如果產品配置需要超過12小時的時間：
- 工作已標示為&#x200B;**[!UICONTROL 失敗]**。
- 該工作中的任何後續擱置任務都不會執行。

![個擱置中的工作](assets/pending-jobs.png)

## 取消執行中的工作

您可以從&#x200B;**[!UICONTROL 工作執行]**&#x200B;索引標籤取消目前正在執行的工作。

### 取消執行中工作的步驟

1. 登入[!DNL Global Admin Console]。
2. 選取&#x200B;**[!UICONTROL 工作執行]**。
3. 選取&#x200B;**[!UICONTROL 取消執行中的工作]**。

### 取消行為

1. 工作會在目前步驟的結尾停止。
2. 工作不會在步驟中間停止。
3. 部分步驟可能需要幾分鐘或幾小時才能完成。
4. 在這段期間，工作可能會維持在&#x200B;**[!UICONTROL 正在取消]**&#x200B;狀態。

&#x200B;> [!NOTE]
>
> 計畫取消，並瞭解當工作停止時，目前步驟的完成可能會大幅延遲。

## 檢視工作歷史記錄

- 若要檢視過去30天內執行的工作：

   1. 登入[!DNL Global Admin Console]。
   2. 選取&#x200B;**[!UICONTROL 工作執行]**。
   3. 捲動至頁面底部。
   4. 選取&#x200B;**[!UICONTROL 最近的工作]**。

- 最近的工作顯示：
   - 已提交&#x200B;**工作命令**。
   - 與執行相關的&#x200B;**錯誤**&#x200B;和&#x200B;**警告**。

&#x200B;> [!NOTE]
>
> 後續重新命名或刪除相關物件&#x200B;**不會影響**&#x200B;命令在作業歷史記錄中的顯示方式。 歷史記錄會反映提交時的狀態。
