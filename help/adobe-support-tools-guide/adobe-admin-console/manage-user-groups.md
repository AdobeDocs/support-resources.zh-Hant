---
title: 在Global Admin Console中管理使用者群組
description: 瞭解如何在Global Admin Console中建立、共用、編輯和刪除使用者群組，以簡化跨組織的使用者管理。
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
exl-id: 1e20362a-0974-4b83-a083-9edaab04c255
source-git-commit: 265c341935b3257e5731a129c42411151645ae89
workflow-type: tm+mt
source-wordcount: '1330'
ht-degree: 0%

---

# 在Global Admin Console中管理使用者群組

在Global Admin Console中建立、管理和共用使用者群組，透過將具有相同許可權的使用者分組、節省時間並確保一致性，來簡化使用者管理。

在[Global Admin Console](https://helpx.adobe.com/tw/enterprise/global-admin-console/adopt-global-administration.html)中，選取組織並導覽至&#x200B;**[!UICONTROL 使用者群組]**。 使用單一使用者管理來源在多個組織間共用群組，以同步使用者和群組。

[登入Global Admin Console](https://global-admin-console.adobe.com)



## 建立使用者群組

您可以[大量個別建立使用者群組](https://helpx.adobe.com/tw/enterprise/using/user-groups.html)，或[直接從已建立的Azure AD](https://helpx.adobe.com/tw/enterprise/using/add-azure-sync.html)同步處理至Adobe Admin Console中的同盟目錄。 在Global Admin Console中，您可以使用指派的相關產品設定檔來定義使用者群組，使用者群組管理員稍後可以使用Admin Console新增使用者。

1. 登入[Global Admin Console](https://global-admin-console.adobe.com/)，選取要編輯的組織，然後導覽至&#x200B;**[!UICONTROL 使用者群組]**&#x200B;索引標籤。

2. 選取&#x200B;**[!UICONTROL 新增使用者群組]**。

   ![Global Admin Console中的「組織」索引標籤，且已選取使用者「群組」索引標籤。](assets/add-user-group.png "新增使用者群組")

   _新增使用者群組至組織以簡化使用者管理。_

3. 在出現的&#x200B;**[!UICONTROL 新增使用者群組]**&#x200B;對話方塊中輸入下列內容：
   - **[!UICONTROL 名稱]**：指定使用者群組的名稱。
   - **[!UICONTROL 產品設定檔]**：如果您想要授與使用者群組中目前或未來成員的產品存取權，請按一下下拉式箭頭，從清單中選取產品設定檔，或輸入產品設定檔名稱，然後從顯示的下拉式清單中選取。 若要新增尚未建立的產品設定檔，您必須先使用[產品設定檔](https://helpx.adobe.com/tw/enterprise/using/global-admin-edit-organizations.html#profiles)索引標籤執行此操作。
   - **[!UICONTROL 管理員]**：按一下下拉箭頭，從清單中選取管理員，或輸入管理員的電子郵件地址，然後從顯示的下拉式清單中選取管理員。 如果您要新增尚未建立的管理員，必須先使用[管理員](#share-user-groups)索引標籤建立該管理員。

   您指定的產品設定檔會指派給使用者群組，而您指定的管理員會成為該群組的使用者群組管理員。 使用者群組管理員可使用相關組織的Adobe Admin Console來管理群組。

4. 選取「**[!UICONTROL 儲存]**」。

5. 選取&#x200B;**[!UICONTROL 檢閱擱置的變更]**&#x200B;以檢閱更新。 然後，選取&#x200B;**[!UICONTROL 提交變更]**&#x200B;以[執行](https://helpx.adobe.com/tw/enterprise/global-admin-console/set-up-organizations.html#execute-jobs)它們。

   >[!NOTE]
   >
   >全域管理員可以使用Global Admin Console [將產品設定檔和使用者群組管理員](#review-user-groups)指派給使用者群組。 使用Adobe Admin Console，系統管理員和使用者群組管理員可以[新增使用者，並將管理員和產品設定檔](https://helpx.adobe.com/tw/enterprise/using/user-groups.html)指派給使用者群組。



## 共用使用者群組

群組投影可讓您將使用者群組及其關聯的使用者從單一管理來源同步到多個Admin Console。 全域管理員可與來源組織的階層子系共用使用者群組，向下工作，而不是向上或並排工作。

1. 登入[Global Admin Console](https://global-admin-console.adobe.com/)，選取組織，並導覽至&#x200B;**[!UICONTROL 使用者群組]**&#x200B;索引標籤。

2. 選取您要共用之使用者群組的核取方塊。

   在下列情況下，群組可能會停用共用：
   - 使用者群組是從另一個組織共用。 若要共用或編輯群組，請從組織階層中選取擁有該群組的組織。
   - 組織未針對企業使用[Adobe儲存空間](https://helpx.adobe.com/in/enterprise/using/storage-for-business.html)，此儲存空間正分階段在全域推出。
   - 組織原則已停用。 移至&#x200B;**[!UICONTROL 原則]**&#x200B;標籤以開啟&#x200B;**[!UICONTROL 管理共用使用者群組]**&#x200B;原則。
   - 組織沒有任何可與其共用使用者群組的子組織。

3. 選取&#x200B;**[!UICONTROL 共用使用者群組]**。

4. <a id="review-user-groups"></a>檢閱要與其他組織共用的使用者群組。 如果您也是所選組織的系統管理員，請選取&#x200B;**[!UICONTROL 在Admin Console中開啟]** <img src="assets/icon-open-in-admin-console.png" alt="在Admin Console中開啟圖示" width="14" height="14">圖示可檢閱Adobe Admin Console中的使用者群組成員清單。

   >[!NOTE]
   >
   >若要避免衝突，請確定您計畫與其共用使用者群組的組織尚未擁有相同名稱的群組。

5. 選取&#x200B;**[!UICONTROL 下一步]**。

6. 選取要與其共用使用者群組的組織，並選取&#x200B;**[!UICONTROL 下一步]**。

7. 如果沒有衝突，請選取&#x200B;**[!UICONTROL 共用使用者群組]**。

   如果發生衝突（目標組織中存在具有相同名稱的使用者群組），請選擇下列其中一個選項，然後選取&#x200B;**[!UICONTROL 共用使用者群組]**：
   - **[!UICONTROL 忽略（預設）]**：略過目標組織中相同名稱的群組。
   - **[!UICONTROL 僅新增]**：將新使用者新增至現有的使用者群組，合併使用者群組，而不移除任何使用者。
   - **[!UICONTROL 映象群組]**：新增或移除使用者，調整目標組織的群組以符合共用群組。

8. 選取&#x200B;**[!UICONTROL 檢閱擱置的變更]**&#x200B;以檢閱更新。 然後，選取&#x200B;**[!UICONTROL 提交變更]**&#x200B;以[執行](https://helpx.adobe.com/tw/enterprise/global-admin-console/set-up-organizations.html#execute-jobs)它們。

   記錄群組預測事件以供您參考。 瞭解[檢視和下載稽核記錄](https://helpx.adobe.com/tw/enterprise/global-admin-console/insights.html)。


當您共用使用者群組時，該群組及其使用者會新增至目標組織。 但是，*來源使用者群組控制*&#x200B;共用的使用者群組及其使用者。 管理員和產品設定檔指派在組織之間&#x200B;*未*&#x200B;同步。

目標組織中會自動更新預計使用者群組名稱或來源使用者群組中關聯使用者的變更。 雖然無法直接管理共用使用者群組，但目標組織內的管理員可以將產品設定檔指派給共用群組，授予群組使用者授權存取權。



## 撤銷共用群組的存取權

1. 登入[Global Admin Console](https://global-admin-console.adobe.com/)，選取組織，並導覽至&#x200B;**[!UICONTROL 使用者群組]**&#x200B;索引標籤。

2. 選取&#x200B;**[!UICONTROL 管理相關使用者群組的共用存取權]**。

3. 選取您要撤銷存取權的組織。

4. 選取&#x200B;**[!UICONTROL 撤銷存取權]**。

5. 撤銷存取權時，您可以選擇刪除使用者群組和使用者，或在目標組織中保留復本：
   - 刪除時，使用者群組會從目標組織中移除。 不屬於其他共用群組成員的使用者會從目標組織移除，並失去對所有產品、服務和資產的存取權。
   - 在保留副本時，使用者群組和使用者會保留在目標組織中，保持所有指派不變。 不過，使用者群組將不再同步，並可由目標組織的管理員管理。

6. 選取&#x200B;**[!UICONTROL 撤銷存取權]**。

7. 選取&#x200B;**[!UICONTROL 檢閱擱置的變更]**&#x200B;以檢閱更新。 然後，選取&#x200B;**[!UICONTROL 提交變更]**&#x200B;以[執行](https://helpx.adobe.com/tw/enterprise/global-admin-console/set-up-organizations.html#execute-jobs)它們。



## 編輯使用者群組

1. 登入[Global Admin Console](https://global-admin-console.adobe.com/)，選取組織，並導覽至&#x200B;**[!UICONTROL 使用者群組]**&#x200B;索引標籤。

2. 選取&#x200B;**[!UICONTROL 其他選項]** 相關使用者群組的<img src="assets/icon-more-options.png" alt="「更多選項」圖示" width="14" height="14" style="vertical-align:middle">圖示，並選取&#x200B;**[!UICONTROL 編輯使用者群組]**。

   >[!NOTE]
   >
   >您無法編輯所選組織未擁有的使用者群組。

   ![選取的組織，其使用者群組索引標籤下的編輯使用者群組選項反白顯示。](assets/edit-user-group.png "編輯使用者群組")

   _編輯使用者群組以更新使用者群組名稱、產品設定檔或管理員。_

3. 更新使用者群組名稱、產品設定檔或管理員。 然後，選取&#x200B;**[!UICONTROL 儲存]**。

   >[!NOTE]
   >
   >在&#x200B;**[!UICONTROL 編輯使用者群組]**&#x200B;精靈中，您只能將管理員角色指派給已在此組織中指派了管理員角色的使用者。 瞭解如何[新增管理員](https://experienceleague.adobe.com/zh-hant/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators)。

4. 選取&#x200B;**[!UICONTROL 檢閱擱置的變更]**&#x200B;以檢閱更新。 然後，選取&#x200B;**[!UICONTROL 提交變更]**&#x200B;以[執行](https://helpx.adobe.com/tw/enterprise/using/global-admin-set-up-organizations.html#execute-jobs)它們。

   >[!NOTE]
   >
   >如果您變更共用使用者群組的名稱，則會在目標組織中自動更新變更。



## 刪除使用者群組

1. 登入[Global Admin Console](https://global-admin-console.adobe.com/)，選取組織，並導覽至&#x200B;**[!UICONTROL 使用者群組]**&#x200B;索引標籤。

2. 選取&#x200B;**[!UICONTROL 其他選項]** 相關使用者群組的<img src="assets/icon-more-options.png" alt="「更多選項」圖示" width="14" height="14" style="vertical-align:middle">圖示，並選取&#x200B;**[!UICONTROL 刪除使用者群組]**。

   >[!NOTE]
   >
   >您無法刪除所選組織未擁有的使用者群組。

3. 在出現的對話方塊中選取&#x200B;**[!UICONTROL 確定]**。

   >[!CAUTION]
   >
   >刪除使用者群組可能會影響您的使用者。 確保刪除使用者群組時，沒有存取權或資訊會遺失。

4. 在您編輯組織後，請選取&#x200B;**[!UICONTROL 檢閱擱置的變更]**&#x200B;以檢閱這些變更。 然後，選取&#x200B;**[!UICONTROL 提交變更]**&#x200B;以[執行](https://helpx.adobe.com/tw/enterprise/using/global-admin-set-up-organizations.html#execute-jobs)它們。
