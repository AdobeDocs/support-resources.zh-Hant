---
title: Adobe DX解決方案統一假日整備指南
description: 本文提供DX解決方案的假期整備指南。
solution: Experience Platform, Journey Optimizer, Customer Journey Analytics, Commerce, Experience Manager, Workfront, Campaign, Analytics, Target, Marketo Engage
role: Developer, Admin, Leader, User
source-git-commit: a5fe17df6ee6e9d23f82776d7200fba9f7d5f267
workflow-type: tm+mt
source-wordcount: '3813'
ht-degree: 1%

---

# Adobe DX解決方案統一假日整備指南


Adobe DX解決方案統一假日整備指南將重點放在主動式規劃而非被動式問題解決上，協助您為假日季節做好準備。 它提供實用的步驟，確保您的執行個體已準備就緒，以在潛在問題出現之前將其減至最少。 Adobe團隊擁有技術專業知識、廣泛的功能，以及經過驗證的方法，可提供適當層級的支援和指導（包括技術和策略層面），讓您的企業做好準備。

請遵循下列最佳實務，確保您的Adobe Digital Experience解決方案具復原力、安全無虞，並可因應尖峰假期流量：

* 規劃增加的流量。
* 避免在尖峰時段期間發生重大變更；在假期之前或之後排程更新。
* 使用儀表板和警報來監控效能並及早偵測瓶頸。
* 請確定您的授權支援聯絡人是最新的。
* 儘可能提前[連絡Adobe支援](https://experienceleague.adobe.com/zh-hant/docs/learning-manager/using/faq/how-to-submit-support-ticket)。

如需Adobe針對特定解決方案的假期整備建議，請參閱下列章節。

* [Adobe Experience Platform](#aep)
* [Adobe Journey Optimizer](#ajo)
* [Adobe Customer Journey Analytics](#cja)
* [Adobe Commerce](#commerce)
* [Adobe Experience Manager](#aem)
* [Adobe Marketo](#marketo)
* [Adobe Workfront](#workfront)
* [Adobe Campaign](#campaign)
* [Adobe Analytics](#analytics)
* [Adobe Target](#target)

>[!NOTE]
>
>按一下每個區段以展開它。


## Adobe Experience Platform (AEP)假日整備指南 {#aep}

+++**按一下以檢視Adobe Experience Platform (AEP)假期整備建議。**

Adobe Experience Platform (AEP)在提供即時客戶體驗方面扮演了重要的角色。 隨著假期臨近，請務必確保您的AEP實作已最佳化以增加流量、安全資料處理和可擴充的擷取。

### 預測季節性需求

為了準備好因應季節性流量尖峰，Adobe建議規劃容量並監控串流設定檔擷取。 這包括預測資料量，並確保您的系統能夠處理增加的輸送量。 請參閱[容量和季節性流量的計畫](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/dataflows/ui/monitor-streaming-profile)以取得參考。

### 準備進行擴展

Adobe提供數種策略，確保您的環境已準備好因應假期流量：

* 增加沙箱的已分配容量。
* 識別[監視儀表板](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/dataflows/ui/monitor-streaming-profile)中的高輸送量資料流，並視需要套用節流或篩選。
* 使用低延遲使用案例的批次擷取來最佳化效能，如[授權使用與容量：串流輸送量最佳實務](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/landing/license/capacity#suggestions)中所述。

這些做法有助於維持擷取可靠性，並減少尖峰期間的延遲。

### 最佳作法和護欄

為了保持在運作限制內並避免服務中斷，Adobe建議遵循下列內嵌和設定檔護欄：

* [串流輸送量最佳實務](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/landing/license/capacity#suggestions)
* [資料擷取的護欄](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/ingestion/guardrails)
* [即時客戶個人檔案資料和細分的預設護欄](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/profile/guardrails)
* [AEP藍圖：護欄](https://experienceleague.adobe.com/zh-hant/docs/blueprints-learn/architecture/architecture-overview/guardrails)

### 安全性與治理

Adobe強調強大的安全性和治理實務，尤其是在高流量季節中，因為此時資料敏感性已提高。

如需有關如何保護客戶資料、強制執行隱私權控制以及維護Adobe Experience Platform實作合規性的建議，請參閱[AEP：安全性](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/landing/governance-privacy-security/overview#security)中的治理、隱私權與安全性。

遵循這些指引，並運用Adobe的公開檔案，組織即可確保其Adobe Experience Platform彈性、安全，並準備好在整個假期中提供卓越的客戶體驗。

+++

## Adobe Journey Optimizer (AJO)假日整備指南 {#ajo}

+++**按一下以檢視Adobe Journey Optimizer (AJO)假期整備建議。**


為了準備Adobe Journey Optimizer的假日季節，組織應預期事件尖峰和跨管道複雜性、設定歷程和頻率規則，並確保資料衛生和決策邏輯。 他們還必須大規模驗證效能、強制執行安全性和API護欄，並套用高峰期後的深入分析以調整未來的行銷活動。

### 預測需求

* 根據假日季節壓縮和較大量的行銷活動，預計：
   * 即時事件和觸發的歷程（放棄購買、最後一分鐘優惠）流量激增
   * 訊息飽和度風險（較高的選擇退出、疲勞）
   * 增加跨管道複雜性（電子郵件+推播+簡訊+應用程式內）
* 使用去年的量度（開啟/點按/選擇退出率、歷程進入量）來模擬預期載入，並設定訊息系統的臨界值。
* 識別可能的「靜音視窗」或低效能期間（例如：週末、假日），並據此規劃傳送量。

### 準備進行擴展

* 確保AJO中的所有管道設定皆已正確設定：電子郵件、推播、簡訊、網頁、應用程式內。 請參閱[設定頻道設定](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/configuration/channel-surfaces)。
* 設定頻率上限和上限規則，以控制訊息數量。 請參閱[頻率限定](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/tutorials/configuration/business-rules/configure-frequency-capping-rules)文章。
* 設定頻道/歷程規則集：請參閱[使用規則集](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/conflict-prioritization/capping-rules/rule-sets)。
* 準備您的資料衛生/即時事件串流和細分架構。
* 請確定您已定義假日行銷活動的目標對象，例如：
   * 高價值客戶
   * 忠誠區段
   * 購物車放棄者
   * 首次購買者
* 預先載入或準備假日歷程的範本，運用決策邏輯（優惠方案/限制），讓您能夠根據詳細目錄、時效性優惠方案和管道偏好設定進行動態調整。 請參閱[將限制新增至優惠方案](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/decisioning/offer-decisioning/managing-offers-in-the-offer-library/configure-offers/add-constraints)文章中的範例。
* 技術整備：確認API/端點負載容量、自訂動作和外部整合的節流/上限規則。 請參閱[護欄和限制](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/get-started/guardrails)。

### 測試及驗證

* 使用您的實驗架構來測試關鍵變數變更：
   * 傳送時間
   * 優惠型別
   * 頻道組合
請參閱[AJO Experimentation Accelerator最佳實務](https://experienceleague.adobe.com/en/docs/experimentation-accelerator/using/get-started/experiment-accelerator-best-practices)。
* 進行端對端歷程驗證：
   * 事件觸發程式
   * 分段專案
   * 歷程路徑流程
   * 個人化邏輯
   * 優惠方案限制
   * 退出條件
* 驗證上限和衝突規則。 請參閱[歷程上限與仲裁](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/conflict-prioritization/journey-capping)文章。
* 針對尖峰傳送或尖峰的壓力測試縮放磁碟區：模擬高觸發磁碟區以驗證系統在負載下的行為。
* 驗證傳遞能力：預熱電子郵件網域/傳送者、確認行動推播設定，以及檢查簡訊/應用程式內遞補頻道。

### 最佳做法

* 使用全通路協調。 請參閱部落格[Essential全通路客戶歷程，以取得參與度和成長率](https://business.adobe.com/blog/essential-customer-journeys-for-omnichannel-engagement)文章，其中顯示AJO的假日季節範例。
* 視需要排定即時觸發器的優先順序。 例如：購物車放棄、瀏覽放棄和股票提醒，因為節日購物者比較被動反應。
* 利用細分和個人化：鎖定高意圖區段、根據過去的購買行為和偏好設定量身打造選件。
* 最少的訊息疲勞：強制上限與無訊息工作時間，以避免過度索取。 請參閱AJO中的[每日頻率上限提升客戶體驗](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/elevate-customer-experience-with-daily-frequency-capping-in-ajo/ba-p/761510)部落格。
* 時機很重要：計畫會在假期中更早傳送（指定壓縮季節），並將頻道與時區和本機對象行為調整一致。
* 提供動態/限時優惠方案以建立急迫性，但可跨通道協調，以避免重複和衝突。
* 使用隱藏邏輯：隱藏剛購買的受眾，或套用購買後歷程以避免備援傳訊。

### 安全性與治理

* 確保已設定存取控制和許可權，以便只有必要的使用者才能部署歷程或修改商業規則。
* 監視並強制執行API呼叫/連線上限：例如，請參閱[上限API | Adobe Journey Optimizer](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/connect-systems/external-systems/capping)文章。
* 使用簡潔的第一方資料並確保適當的身分拼接，讓傳訊以客戶為中心，不會重複/錯位。
* 確保傳遞能力網域溫度升高，並具備反垃圾郵件措施，特別是針對高流量假日傳送。
* 在高峰季節經常檢閱稽核記錄和歷程變更，以及早偵測誤執行或錯誤的歷程。

### 尖峰後學習

* 在高峰載入後，審查歷程專案計數、隱藏計數、選擇退出率、傳遞能力量度和管道效能。
* 清理抑制的區段，並暫停或淘汰為假期時段建立的歷程，以避免結轉疲勞。
* 利用即時績效的深入分析來調整下一年的計畫（例如：傳送時間調整、頻道組合和訊息量）。

透過主動預測季節性需求、設定管道和規則、驗證歷程效能，以及強制實行安全性與控管，組織可確保Adobe Journey Optimizer在本假日季節及其他時間內，提供順暢、個人化和可復原的客戶體驗。

+++

## Customer Journey Analytics (CJA)假日整備指南 {#cja}

+++**按一下以檢視Customer Journey Analytics (CJA)假期整備建議。**

Customer Journey Analytics使用5 P來達成假日/旺季整備。

### 準備進行擴展

* 檢閱CJA連線和資料檢視；建立哪些連線和資料檢視需要增強的監控和布建。
* 確認布建足以因應假日規模；視需要擴充重要連線和資料檢視。 如需詳細資訊，請參閱[管理連線](https://experienceleague.adobe.com/zh-hant/docs/analytics-platform/using/cja-connections/manage-connections)。

### 監視效能

* 利用RAM （[[!UICONTROL 報告活動管理員]總覽](https://experienceleague.adobe.com/zh-hant/docs/analytics-platform/using/reporting-activity-manager/reporting-activity-overview)）即時監視使用中及佇列的報告要求、識別無容量連線，並找出瓶頸。
* 使用[錯誤和疑難排解指南](https://experienceleague.adobe.com/zh-hant/docs/analytics-platform/using/cja-workspace/workspace-faq/error-messages)和[已知限制](https://experienceleague.adobe.com/zh-hant/docs/analytics-platform/using/cja-workspace/workspace-faq/aw-limitations)文章，在尖峰負載期間留意延遲增加的情況。
* 讓管理員透過RAM搶先暫停或取消長時間執行/封鎖的請求。 請參閱CJA[文章中的](https://experienceleague.adobe.com/zh-hant/docs/analytics-platform/using/reporting-activity-manager/reporting-activity-cancel-requests)取消報告要求。

### 最佳做法

* 在低流量期間排程匯出/報告，以平滑載入並將延遲降至最低。 請參閱[排程報告](https://experienceleague.adobe.com/zh-hant/docs/analytics-platform/using/cja-components/scheduled-projects-manager)文章。
* 展開請求：以一天中的不同間隔排程報表。
* 減少面板、簡化區段、縮短日期範圍，以及避免過多的並行工作。 請參閱[最佳化CJA Workspace效能](https://experienceleague.adobe.com/zh-hant/docs/analytics-platform/using/cja-workspace/workspace-faq/optimizing-performance)文章以取得詳細資料。

### 疑難排解

* 疑難排解工作區錯誤時，請參閱錯誤訊息以取得原因和建議的動作；使用RAM （[!UICONTROL 報告活動管理員]）來清除瓶頸並有效管理並行。 如需詳細資訊，請參閱[CJA Workspace錯誤處理](https://experienceleague.adobe.com/zh-hant/docs/analytics-platform/using/cja-workspace/workspace-faq/error-messages)。
* CJA使用RAM （[[!UICONTROL 中的]報告活動管理員](https://experienceleague.adobe.com/zh-hant/docs/analytics-platform/using/reporting-activity-manager/reporting-activity-overview)）來找出有問題的使用者、查詢或專案；視需要排定優先順序並終止/取消。

### 尖峰後學習

* 假日/尖峰期過後，請檢閱效能和事件記錄檔，以評估所提供最佳實務的影響。
* 檢閱緩慢的查詢和使用者任務，以識別可以為下一季最佳化的模式/趨勢。
* 從使用者和利害關係人收集意見回饋 — 使用新獲得的見解更新您自己的Runbook和整備計畫。
* 透過您的帳戶團隊向Adobe團隊提供意見回饋。

+++

## Adobe Commerce假日整備指南 {#commerce}

+++**按一下以檢視Adobe Commerce假日整備建議。**

為了確保您的組織能夠順利度過旺季，請務必為您的Adobe Commerce數位店面做好準備以應付高流量。

### 預測需求

* 在旺季假期銷售期間（11月中旬至1月中旬），Adobe建議雲端基礎結構上代管的所有Adobe Commerce商戶透過提交假期高載容量要求，主動規劃訪客增加。 如需詳細資訊，請參閱雲端基礎結構上的[Adobe Commerce的假期突增容量要求](https://experienceleague.adobe.com/zh-hant/docs/commerce-knowledge-base/kb/announcements/commerce-announcements/holiday-surge-capacity-requests-for-magento-commerce-cloud)。

### 準備進行擴展

遵循[規劃與樞紐分析：2025年旺季的戰略方針](https://experienceleague.adobe.com/zh-hant/perspectives/planning-and-pivoting-a-strategic-approach-to-peak-season-2025)指南中的建議，該指南使用Adobe Commerce (和選用的Adobe Experience Cloud工具)提供可操作的策略，以協助您規劃、樞紐分析並在一年中最繁忙的時段提供傑出的客戶體驗。

### 最佳做法

* 遵循Adobe的指南[如何針對高流量準備您的基礎結構 — 旺季效能的5 Ps](https://business.adobe.com/blog/how-to/the-5-ps-of-peak-season-performance-a-guide-to-preparing-your-infrastructure-for-high-traffic)。
* 檢視[Commerce假期整備的技術秘訣](https://experienceleague.adobe.com/zh-hant/docs/commerce-knowledge-base/kb/how-to/tech-tips-for-commerce-holiday-readiness)，瞭解如何在假期中讓您的基礎建設準備好應付高流量、防止停機時間，以及最佳化效能的相關秘訣。

+++

## Adobe Experience Manager (AEM)假日整備指南 {#aem}

+++**按一下以檢視Adobe Experience Manager (AEM)假期整備建議。**

假期即將來臨，對許多Adobe客戶而言，這表示銷售高峰期已開始。 我們致力於您的成功，希望確保您為即將到來的流量激增做好充分準備。

### Adobe Experience Manager (AEM)雲端服務

如果您的組織在假期遇到最忙碌的時刻，您可能會考慮如何最佳化Adobe Experience Manager網站以因應尖峰流量。 幸運的是有了Adobe Experience Manager雲端服務，您的網站已具備自動擴展的功能，無論流量是否突然變更，都能確保訪客獲得順暢的體驗。

#### 準備進行擴展

* 如需使用Adobe Experience Manager雲端服務為高流量做好準備的詳細深入分析和指引，請參閱下列連結：

   * AEM as a Cloud Service中的[CDN](https://experienceleague.adobe.com/zh-hant/docs/experience-manager-cloud-service/content/implementing/content-delivery/cdn)
   * [AEM as a Cloud Service快取](https://experienceleague.adobe.com/zh-hant/docs/experience-manager-learn/cloud-service/caching/overview)

* 如果您是Ultimate Success客戶，且最近與Adobe客戶團隊共用大量預測資訊，請放心再次將資訊傳送給我們，我們已經有一個檢視。

我們在此支援您歷程的每個步驟。 如果您有任何問題或顧慮，請隨時[提交支援票證](https://experienceleague.adobe.com/zh-hant/docs/learning-manager/using/faq/how-to-submit-support-ticket)。

若要在節日季節準備行銷活動，請檢視[AEMaaCS使用手冊：簡介 — 行銷活動引數](https://experienceleague.adobe.com/zh-hant/docs/experience-manager-cloud-service/content/implementing/content-delivery/caching#marketing-parameters)檔案。

#### 安全性與治理

如需AEM網站流量安全/保護的詳細資訊，請參閱AEM as a Cloud Service教學課程中的[概觀 — 保護AEM網站](https://experienceleague.adobe.com/zh-hant/docs/experience-manager-learn/cloud-service/security/traffic-filter-and-waf-rules/overview)文章。

#### 假日維護規劃

Adobe已排程維護排除期，以確保在關鍵假期期間服務不會中斷：

* **不會發生自動更新**，介於：
   * 2025年11月24日至2025年12月2日
   * 2025年12月15日至2026年1月2日

這可確保高流量期間的穩定性。 如需完整的發行排程和維護期間，請參閱[AEM發行藍圖](https://experienceleague.adobe.com/zh-hant/docs/experience-manager-release-information/aem-release-updates/update-releases-roadmap)。


### Adobe Experience Manager (AEM)搭配Adobe Managed Services (AMS)

AEM客戶運用Adobe Managed Services時，可以主動與其CSE合作，針對假日的保障需求進行規劃。

++++

## Adobe Marketo假日整備指南 {#marketo}

+++**按一下以檢視Adobe Marketo假日整備建議。**

為確保透過Adobe Marketo成功進行節日行銷活動，團隊應驗證電子郵件驗證設定、清理並保護其資料庫、最佳化行銷活動邏輯和排程、徹底測試電子郵件轉譯和可遞送性，並簡化支援對尖峰績效和參與度的整備。

### 準備進行擴展

* 檢查您的SPF/DKIM設定，確認所有專案皆已設定且正常運作。 請參閱[設定SPF和DKIM以取得您的電子郵件傳遞能力](https://experienceleague.adobe.com/zh-hant/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-spf-and-dkim-for-your-email-deliverability)文章以取得詳細資料。
* 清除非作用中/無效的記錄，以稽核並清除Marketo資料庫。 這會增加您傳送登陸到最暢銷潛在客戶收件匣中的機會。 請參閱[Marketo資料庫健康情況檢查及如何保持乾淨](https://nation.marketo.com/t5/champion-program-blogs/marketo-database-health-check-up-amp-how-to-keep-it-clean/ba-p/323563)文章以取得詳細資料。
* 確認您的團隊成員擁有執行任務的正確許可權，並防止對電子郵件的意外存取或變更。 無論您是透過&#x200B;**[!UICONTROL 管理員]**&#x200B;或透過&#x200B;**[!UICONTROL Admin Console]**&#x200B;進行變更，我們都能協助您完成變更。 請參閱[管理使用者角色和許可權](https://experienceleague.adobe.com/zh-hant/docs/marketo/using/product-docs/administration/users-and-roles/managing-user-roles-and-permissions)文章。
* 請檢閱您的Launchpad整合，以確保正確驗證並在使用之前解決任何潛在錯誤。 請參閱[Marketo Developer Guide： Authentication](https://experienceleague.adobe.com/zh-hant/docs/marketo-developer/marketo/rest/authentication)文章。

### 最佳做法

效率始於瞭解Marketo如何排定行銷活動的優先順序及處理行銷活動。 透過這些最佳化秘訣，讓您的行銷活動擁有極快的速度。

* 瞭解Marketo如何排定行銷活動流程步驟處理的優先順序，對於避免不慎延遲任何緊急或高優先順序的電子郵件至關重要。 請參閱[Campaign處理的運作方式](https://nation.marketo.com/t5/knowledgebase/how-campaign-processing-works/ta-p/248264)文章。
* 留意智慧清單邏輯有助於確保您的行銷活動快速並以最高績效執行。 請參閱[智慧列示最佳實務](https://experienceleague.adobe.com/zh-hant/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/creating-a-smart-list/best-practices-for-smart-lists)文章。
* **[!UICONTROL 開始時間]**&#x200B;或&#x200B;**[!UICONTROL 收件者時區]**&#x200B;可以在您傳送之前開始建立電子郵件、減少延遲，並為具有高資源邏輯的合格潛在客戶提供額外的準備時間。 如需詳細資訊，請參閱[電子郵件程式](https://experienceleague.adobe.com/zh-hant/docs/marketo/using/product-docs/email-marketing/email-programs/email-program-actions/head-start-for-email-programs)的「開門即用」，以及[使用收件者時區排程電子郵件程式](https://experienceleague.adobe.com/zh-hant/docs/marketo/using/product-docs/email-marketing/email-programs/email-program-actions/scheduling-with-recipient-time-zone/schedule-email-programs-with-recipient-time-zone)文章。
* 您的行銷活動處於作用中狀態，潛在客戶正在流過，然後您注意到流程步驟出現錯誤。 快速調整是很容易修正的問題，但若您變更即時等待步驟或重新排序流程時，能知道會發生什麼情況，可協助您避免許多問題，並於稍後清除。 請參閱[在等待步驟](https://nation.marketo.com/t5/knowledgebase/editing-campaign-flow-with-members-in-wait-steps/ta-p/254294)中與成員編輯行銷活動流程。

### 測試及驗證

在您點選&#x200B;**[!UICONTROL 傳送]**&#x200B;之前，請確定您的電子郵件外觀與執行方式與預期完全相同。

* Marketo提供多種方法來測試電子郵件的外觀，以確保其外觀與您的構想完全相同。
   * 使用&#x200B;**[!UICONTROL 預覽]**&#x200B;函式，透過分段預覽或個別潛在客戶來確保您的動態內容和Token正確呈現。 請參閱[預覽包含動態內容的電子郵件](https://experienceleague.adobe.com/zh-hant/docs/marketo/using/product-docs/email-marketing/general/functions-in-the-editor/preview-an-email-with-dynamic-content)文章。
   * 快速輕鬆地將直接電子郵件傳送至您的測試記錄，以瞭解您的電子郵件在不同使用者端/裝置上的顯示方式。 請參閱[從智慧列示](https://experienceleague.adobe.com/zh-hant/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/using-smart-lists/run-a-single-flow-step-from-a-smart-list)文章執行單一流程步驟。
   * 對於[!DNL Litmus]位使用者，現在比以往更容易整合您的帳戶，並直接從電子郵件編輯器開始轉譯測試。 檢視[使用 [!DNL Litmus]](https://experienceleague.adobe.com/zh-hant/docs/marketo/using/product-docs/email-marketing/email-designer/test-email-rendering)測試電子郵件轉譯文章。
* 檢視電子郵件垃圾郵件報告功能，此功能與[!DNL SpamAssassin]整合，以檢閱您的電子郵件內容，並指派分數，說明其點選收件匣或標示為&#x200B;*垃圾郵件*&#x200B;的可能性。 請參閱[電子郵件垃圾郵件報告](https://experienceleague.adobe.com/zh-hant/docs/marketo/using/product-docs/email-marketing/email-designer/spam-report)文章。
* 密切注視[!UICONTROL 行銷活動佇列]，確認您的行銷活動正在處理中，並正確排定高度緊急專案的優先順序。 檢視[我的行銷活動是否正在執行？](https://nation.marketo.com/t5/knowledgebase/is-my-campaign-running/ta-p/248662)篇文章。

### 簡化您的支援體驗

發生錯誤時，速度很重要，Marketo支援可提供協助！ 請在您的支援案例中加入這些細節，避免來回切換，協助我們的團隊加速解決問題。 請參閱[使用Marketo支援的最佳實務](https://nation.marketo.com/t5/knowledgebase/best-practices-for-working-with-marketo-support/ta-p/253491)文章。

有了本指南，您可以更輕鬆地瞭解自己正從有利的位置開始，以在此關鍵期間促進參與和轉換。 利害關係重大，但您的壓力並不一定非要如此。 立即開始準備，讓這個假日季節成為您最成功的季節。

+++

## Adobe Workfront假日整備指南 {#workfront}

+++**按一下以檢視Adobe Workfront假日整備建議。**

為了準備Adobe Workfront迎接假日季節，團隊應更新支援聯絡人、根據Adobe調整內部時程表、避免在尖峰時段期間發生重大變更，並主動監控自動化和整合，以確保順暢的運作。

### 準備進行擴展

為了確保假期能提供順暢的支援體驗：

* 事先檢閱並更新您的授權支援連絡人。
* 驗證在關鍵問題發生時，主要利害關係人是否可與支援部門合作。
* 如果計畫產品或工作流程在假日視窗中變更，請考慮在11月中旬或1月初之前排程，以獲得最佳的週轉時間。
* 向您的Adobe聯絡人傳達內部假日排程，以確保一致性。

### 測試及驗證

掌握Workfront發行版本的最新資訊，並在沙箱環境中測試新功能：

* [準備Adobe Workfront發行](https://experienceleague.adobe.com/zh-hant/docs/workfront/using/product-announcements/product-releases/release-readiness)
* [Workfront發行說明封存](https://experienceleague.adobe.com/zh-hant/docs/workfront/using/product-announcements/product-releases/product-releases)
* [2025年第1季版本總覽](https://experienceleague.adobe.com/zh-hant/docs/workfront/using/product-announcements/product-releases/release-25-q1/25-q1-release-overview)
* [Workfront發行網路研討會影片](https://experienceleague.adobe.com/zh-hant/docs/events/workfront-recordings/releases/25-1-release-webinar)

### 最佳做法

* 主動式計畫：識別任何可能受內部休假排程影響的系統相依性或排程的自動化。
* 持續溝通：讓您的內部團隊和Adobe支援得知規劃的維護或關鍵事件。
* 使用儀表板：監視重要的整合和自動化，以掌握效能問題的早期跡象。
* 提早上報：如果您預期或發現服務降級狀況，請立即開啟支援票證 — 不要等待它變得嚴重。

透過提前規劃、保持清晰的溝通及及早上報問題，組織可以最大限度地減少中斷，並確保Workfront在整個假日期間持續支援關鍵工作流程。

+++

## Adobe Campaign假日整備指南 {#campaign}

+++**按一下以檢視Adobe Campaign假日整備建議。**


為了讓Adobe Campaign做好假日整備的準備，團隊應主動驗證傳遞能力設定、最佳化對象細分和訊息頻率、確保基礎架構可擴充性，並測試跨頻道行銷活動協調以有效處理季節性流量和參與尖峰。

### 讓您的假日行銷活動脫穎而出的專家秘訣

就像開始您的節日購物永遠都不嫌早一樣，開始規劃大獲成功的節日行銷活動也永遠都不嫌早。 有了Adobe Campaign，您可以設計、規劃及執行行銷活動，好讓貴組織的所有節日願望都成真。 但是您知道在年底之前讓執行的行銷活動大獲成功的所有秘訣嗎？ 觀看此影片，[專家秘訣，讓您的假日行銷活動脫穎而出](https://experienceleague.adobe.com/zh-hant/docs/events/experience-league-live-recordings/episodes/exl-live-episode-03)，其中會討論傳遞能力和執行最佳實務，並示範如何在Adobe Campaign中完成所有工作。

### 假日期間的考量事項和準備事項

此影片[Adobe Campaign：假日整備 — 假日期間的考量事項和準備事項](https://helpx.adobe.com/tw/customer-care-office-hours/campaign/campaign-holiday-readiness.html)，內容包括：

* 參與Campaign社群
* 可遞送性 — 節日及以外時間的考量事項！
* Adobe Campaign Classic (ACC)與Adobe Campaign Standard (ACS)的技術建議

為了讓Adobe Campaign準備好因應假期旺季的需求，組織應完成傳遞能力檢查、驗證行銷活動設定，並確保可擴充的基礎結構和跨管道協調到位，以在整個假期中自信地執行大量對時間敏感的行銷活動。

+++

## Adobe Analytics假日整備指南 {#analytics}

+++**按一下以檢視Adobe Analytics假日整備建議。**

隨著假期臨近，使用Adobe Analytics的組織應主動採取措施，以確保尖峰流量期間的資料準確性、平台效能和報表可靠性。 Adobe提供多種資源和最佳實務，以協助團隊有效準備。

### 預測流量

為確保足夠的硬體配置與系統回應能力，Adobe建議提前&#x200B;**提交每小時尖峰與每日伺服器點選/呼叫磁碟區**。

* 檢查[流量尖峰排程和硬體配置前置時間](https://experienceleague.adobe.com/zh-hant/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/traffic-management/t-traffic-schedule-spike#hardware-allocation-lead-times)，因為瞭解資料可用速度對於高流量期間的即時決策至關重要。

* 在[Adobe Analytics資料延遲概觀](https://experienceleague.adobe.com/zh-hant/docs/analytics/technotes/latency)中瞭解Adobe Analytics中的資料可用性和延遲有何影響，包括未預期的流量尖峰和硬體問題，並探索減少資料延遲的建議策略。

### 最佳做法

對於使用資料摘要匯出原始分析資料的團隊，Adobe提供了有關最佳化摘要設定和避免常見陷阱的指引。

* [Adobe Analytics資料摘要的最佳作法](https://experienceleague.adobe.com/zh-hant/docs/analytics/export/analytics-data-feed/data-feeds-best-practices)

為了在假期維持快速可靠的報表，Adobe建議：

* [最佳化Analysis Workspace效能](https://experienceleague.adobe.com/zh-hant/docs/analytics/analyze/analysis-workspace/workspace-faq/optimizing-performance)
* [Report Builder的疑難排解和最佳做法：最佳化要求的建議](https://experienceleague.adobe.com/zh-hant/docs/analytics/analyze/legacy-report-builder/troubleshoot#section_33EF919255BF46CD97105D8ACB43573F)
* [Analytics元件指南：排程報表佇列](https://experienceleague.adobe.com/zh-hant/docs/analytics/components/scheduled-reports-admin)

### 假日維護規劃

Adobe通常會在假期尖峰期間強制執行&#x200B;**維護排除期間**，以確保服務不會中斷。 客戶應透過Experience League監控Adobe的發行和維護排程，並與其Adobe客戶團隊協調支援規劃。

依照這些指引，並運用Adobe的公開檔案，組織可確保其Adobe Analytics實作穩健、回應迅速，並因應假日季節的需求。

+++

## Adobe Target假日整備指南 {#target}

+++**按一下以檢視Adobe Target假日整備建議。**

假日季節提供令人振奮的參與機會，但同時也伴隨著流量激增等挑戰，以及對個人化系統的需求增加。 為協助您在此關鍵期間提供順暢的體驗，我們已編譯重要建議，以確保您的Adobe Target實作準備就緒。

### 預測需求

首先，您可以預期20-50%或以上的流量尖峰，並驗證您的基礎架構能否處理負載。 預測Adobe Target、Analytics和AEP的活動和資料量，避免出現意外情況。

此外，識別關鍵任務歷程（例如結帳、產品推薦和促銷優惠）也很重要，因此個人化工作會聚焦於最重要的地方。

請參閱[使用Adobe Target最佳化的最佳實務](https://experienceleague.adobe.com/zh-hant/docs/target-learn/tutorials/administration/strategy/target-best-practices-for-optimization)。

### 準備進行擴展

* 規劃網站和行動裝置上的流量增加，並通知Target支援團隊增加伺服器容量，以避免任何封鎖的呼叫。
* 對於任何載入/畫筆測試，應事先通知Target支援團隊。
* 升級至最新的`at.js`/傳送API版本。
* 凍結非關鍵變更；準備遞補體驗。
* 協調支援和向上呈報流程，並啟用主動警示。

### 測試及驗證

使用[QA連結](https://experienceleague.adobe.com/zh-hant/docs/target/using/activities/activity-qa/activity-qa)驗證內容傳遞，以確認一切如預期般運作。 使用&#x200B;**[!UICONTROL 符合對象規則來檢視體驗]**&#x200B;切換，以確保適當的對象符合您正在測試的活動。 仔細檢查您的&#x200B;**[!UICONTROL 目標量度]**&#x200B;設定是否已對齊活動的&#x200B;**[!UICONTROL 目標]**。 隨時備妥備份計畫，以防萬一。

### 最佳做法

讓您的實作保持在[Adobe Target限制](https://experienceleague.adobe.com/zh-hant/docs/target/using/troubleshoot/target-limits)以內，並在啟動前預先驗證[GDPR和CCPA合規性](https://experienceleague.adobe.com/zh-hant/docs/target-dev/developer/implementation/privacy/cmp-privacy-and-general-data-protection-regulation)。 維護少於100個使用中的活動，並封存舊的活動，以簡化流程。 利用&#x200B;**[!UICONTROL 自動分配]**/**[!UICONTROL 自動鎖定目標]**&#x200B;進行AI驅動的最佳化。 建立復原計畫和即時監控儀表板。

### 安全性與治理

在個人化體驗之前，請先確認GDPR和CCPA下的同意合規性。 請避免將個人識別資訊(PII)儲存在設定檔引數中，並驗證API安全性以保護客戶資料。

+++
