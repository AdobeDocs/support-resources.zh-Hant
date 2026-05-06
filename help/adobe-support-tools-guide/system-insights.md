---
title: 系統分析
description: 系統深入分析會主動識別Adobe Commerce環境中的潛在問題。 在案例建立期間檢閱深入分析可減少解決時間，有助於防止中斷，並支援穩定而安全的部署。
hide: true
source-git-commit: f9a38443243d230c76d968ca7a67c4ba29d07a26
workflow-type: tm+mt
source-wordcount: '738'
ht-degree: 0%

---

# 系統分析

系統深入分析提供主動式發現，協助識別Adobe產品設定中的效能、安全性和功能方面潛在問題。 這些見解會根據從可觀察性工具（包括API、New Relic和[!DNL Splunk]）收集的遙測資料，顯示效能降低、安全性弱點或設定錯誤等風險。

「系統深入分析」會在案例建立過程中出現，有助於加快診斷和解決問題的速度。

## 系統深入分析的建立方式

Adobe團隊會持續分析常見的支援問題和新興趨勢。 Adobe會根據這些發現，將自動化檢查新增至系統。

這些檢查會掃描產品設定，以偵測設定錯誤、工作停滯或可能導致功能問題或系統中斷的情況。

當檢查識別的值或狀態超出Adobe產品和支援團隊定義的安全範圍時，系統將其顯示為系統Insight。

## 為什麼系統分析很重要

定期檢視系統深入分析有助於及早發現問題，以免影響系統穩定性或客戶體驗。 這種主動式方法：

- 提升平台可靠性
- 減少停機時間
- 協助維護Adobe建議的最佳實務

## 可用性和範圍

「系統深入分析」目前僅適用於Adobe Commerce。 這些見解會在Experience League支援上的案例建立過程中出現，也可透過[全網站分析工具(SWAT)](https://experienceleague.adobe.com/en/docs/commerce-operations/tools/site-wide-analysis-tool/intro)取得。

>[!Note]
>
>系統分析只會顯示生產環境的資料。

## 存取系統分析

系統深入分析會出現在整個案例建立工作流程中。 輸入問題詳細資訊後，**[!UICONTROL 系統深入分析]**&#x200B;面板會出現在畫面右側，AI支援的建議區段下方。 若要深入瞭解AI支援的建議，請參閱Adobe客戶支援體驗文章中的[填寫支援票證](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-customer-support-experience#fill-out-the-support-ticket)。

面板會顯示範圍設定為特定專案執行個體的可捲動見解清單。 範圍設定是以在&#x200B;**[!UICONTROL 專案URL]**&#x200B;欄位中輸入的資訊為基礎。 請正確輸入&#x200B;**[!UICONTROL 專案URL]**，以確保深入分析反映正確的環境。

面板載入後，會顯示為環境標幟的insight卡的可捲動清單。 每個insight卡片都包含：

- 摘要問題的標題
- insight的簡短說明

![存取支援資源](/help/adobe-support-tools-guide/assets/access-support-resources.png)

若要檢視完整的insight詳細資訊，請從清單中選取insight卡片。 詳細檢視提供下列資訊：

- insight名稱
- 標籤insight的Adobe產品
- insight型別，分類為：
   - [!UICONTROL 功能]
   - [!UICONTROL 效能]
   - [!UICONTROL 安全性]
- [!UICONTROL 風險等級]表示嚴重程度
- [!UICONTROL 上次檢查執行]指出偵測到結果的時間。
- [!UICONTROL Insight Source]，由全網站分析工具(SWAT)提供
- 對問題及其潛在影響的詳細說明，以及調查和解決問題的可操作步驟。 詳細檢視也會說明這類問題的典型原因，並提供相關Adobe檔案的連結以供額外參考。

![按一下案例卡](/help/adobe-support-tools-guide/assets/click-case-card.png)

在繼續之前，請先檢閱面板中的所有深入分析，因為insight可以直接解決所遇到的問題。

## 在insight上執行動作

檢閱insight後，請選擇下列動作之一。

### 繼續建立案例

如果問題持續存在或需要其他協助，請選取&#x200B;**[!UICONTROL 繼續建立案例]**。 系統會保留所有先前輸入的案例資訊。

### 將問題標籤為已解決

如果insight已解決問題且不再需要支援案例，請選取「**[!UICONTROL 問題已解決]**」。

選取此選項時：

- 確認對話方塊隨即顯示。
- 此對話方塊會指出所有輸入的案例資料將會永久清除。

insight上的![動作](/help/adobe-support-tools-guide/assets/issue-resolved.png)

選取&#x200B;**[!UICONTROL 完成]**&#x200B;以確認並返回&#x200B;**[!UICONTROL 我的案例]**&#x200B;頁面。 選取&#x200B;**[!UICONTROL 取消]**&#x200B;以返回insight詳細資料檢視。

![清除大小寫表單](/help/adobe-support-tools-guide/assets/clear-case-form.png)

## 在insight上提供意見回饋

在每個insight詳細資料檢視的底部，都可以提供insight是否實用的意見回饋。 此意見反應可協助Adobe持續改善System Insights的相關性和準確性。

![提供意見回饋](/help/adobe-support-tools-guide/assets/submit-feedback.png)

若要提供意見回饋：

1. 開啟insight詳細資料檢視。
2. 捲動至面板底部。
3. 找到提示&#x200B;**[!UICONTROL 這是否有幫助？ 傳送意見反應。]**
4. 選取下列其中一個選項：
   - 如果insight有所幫助，請&#x200B;**豎起拇指**&#x200B;圖示
   - 如果insight沒有幫助，請&#x200B;**按下縮圖**&#x200B;圖示
5. （選擇性）輸入其他註解。
6. 選取&#x200B;**[!UICONTROL 提交]**&#x200B;以傳送意見反應，或選取&#x200B;**[!UICONTROL 解除]**&#x200B;以關閉意見反應區段而不提交。
