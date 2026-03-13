---
title: 管理組織層次結構
description: 瞭解全域管理員如何在Global Admin Console中管理組織的階層。
Feature-set: Experience Cloud Services
Solution: Admin Console
Feature: Admin Console
source-git-commit: 3b3b2711887f0db086e4eb8281344cc7356accf7
workflow-type: tm+mt
source-wordcount: '1626'
ht-degree: 0%

---

# 管理組織階層

適用於企業。

瞭解全域管理員如何在Global Admin Console中管理組織的階層。

取得[對 [!DNL Global Admin Console]](https://helpx.adobe.com/enterprise/global-admin-console/adopt-global-administration.html#request-access)的存取權後，您可以建立新組織、將現有組織加入階層、刪除組織，以及變更父級組織。
[登入Global Admin Console](https://global-admin-console.adobe.com/)

組織是用於管理Adobe產品和用戶的結構。 [[!DNL Adobe Admin Console]](https://helpx.adobe.com/tw/enterprise/using/admin-console.html)允許管理員管理其組織中產品和用戶的部署和配置。 [[!DNL Global Admin Console]](https://helpx.adobe.com/enterprise/global-admin-console/overview.html)允許全局管理員建立、管理和刪除多個組織。

## 建立子組織

作為[全局管理員](https://helpx.adobe.com/enterprise/global-admin-console/manage-administrators.html)，您可以建立層次結構中任何組織的子組織，並設定名稱、國家/地區、用戶組、產品、產品配置檔案、管理員和策略。

建立新子組織時，系統會自動從直接父組織繼承以下內容：

- 組織的[策略](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html)設定（如果存在鎖定）。
- 系統管理員清單（由&#x200B;**[!UICONTROL 在建立]** [策略](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html)時繼承系統管理員控制）。
以下操作可防止系統管理員被繼承：
   - 缺少[網域信任](https://helpx.adobe.com/enterprise/using/directory-trust.html)。
   - 使用者型別限制（新增Adobe ID/ Enterprise ID/ Federated ID使用者原則）。 瞭解[原則詳細資料](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html)。
- 從父級組織有權存取的網域存取[[!DNL Federated ID]]或[[!DNL Enterprise ID]]位使用者。 這使父項中的網域使用者可在子組織中使用。 用戶訪問的繼承由&#x200B;**從父組織管理的目錄繼承用戶** [策略](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html)控制。
- 共用原則、密碼原則及安全性連絡人（由&#x200B;**在建立子組織時繼承資產共用設定** [原則](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html)）所控制。

1. 登入[Global Admin Console](https://global-admin-console.adobe.com/)。 在&#x200B;**[!UICONTROL 組織]**&#x200B;標籤中，選取您要新增子組織的組織。
2. 選取&#x200B;**[!UICONTROL 新增+]**&#x200B;圖示。
   ![新增組織](/help/adobe-support-tools-guide/assets/add-an-organization-1.png)
3. 指定組織的&#x200B;**名稱**&#x200B;和&#x200B;**國家**。\
   組織的簡單名稱必須介於4到100個字元之間；路徑名的最大長度為255個字元。
   ![添加子組織](/help/adobe-support-tools-guide/assets/add-an-child-organization.png)
4. 選取「**[!UICONTROL 儲存]**」。
5. 編輯完組織後，選擇&#x200B;**[!UICONTROL 審閱掛起的更改]**。 審閱後，選擇&#x200B;**[!UICONTROL 將更改]**&#x200B;提交到[執行](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html)。

## 刪除子組織

作為[全局管理員](https://helpx.adobe.com/enterprise/global-admin-console/manage-administrators.html)，您可以刪除子組織。 無法撤消刪除操作，並且無法刪除根組織。 分配給已刪除組織的資源將返回給其父組織。 在刪除組織之前，其父組織將自動成為其任何子組織的父組織。

只有滿足以下條件，才能刪除組織：

- 組織中沒有Sign帳戶、Adobe Stock購買或存放庫。
- 組織中沒有聲明的域。
- 組織中沒有實例化的產品。
- 組織中沒有可包含實例化的Experience Cloud產品。

>[!WARNING]
>
>刪除組織會影響用戶。 確保刪除組織時不會丟失任何訪問權限或資訊。

1. 登錄到[[!DNL Global Admin Console]](https://global-admin-console.adobe.com/)。 轉到&#x200B;**[!UICONTROL 組織]**&#x200B;頁籤並選擇要刪除的組織。
1. 選取&#x200B;**[!UICONTROL 刪除]**&#x200B;圖示。
   ![刪除組織](/help/adobe-support-tools-guide/assets/delete-organization.png)
1. 在&#x200B;**[!UICONTROL 刪除組織]**&#x200B;對話方塊中，選取&#x200B;**[!UICONTROL 確定]**。
1. 在您編輯完組織後，選取&#x200B;**[!UICONTROL 檢閱擱置中的變更]**。 檢閱後，選取&#x200B;**[!UICONTROL 提交變更]**&#x200B;以[執行](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html)它們。

## 重新命名組織

組織名稱是貴公司或機構的正式名稱，在購買時設定。 使用者在登入期間選取設定檔時，尤其是如果他們可以從多個組織存取Adobe產品，或需要選擇企業和個人設定檔時，會看到此名稱。

身為[全域系統管理員](https://helpx.adobe.com/enterprise/global-admin-console/manage-administrators.html)，您可以編輯任何父或子組織的名稱，以協助使用者在登入[[!DNL Creative Cloud]]產品和服務時識別正確的設定檔。

1. 登入[Global Admin Console](https://global-admin-console.adobe.com/)。 在&#x200B;**[!UICONTROL 組織]**&#x200B;標籤中，選取您要重新命名的組織。
1. 選取&#x200B;**[!UICONTROL 編輯]**&#x200B;圖示。
   ![更名組織](/help/adobe-support-tools-guide/assets/rename-organization.png)
1. 更新您的組織名稱並選擇&#x200B;**[!UICONTROL 保存]**。

>[!TIP]
>
>使用最多255個字元的清晰、可識別的組織名稱來幫助用戶選擇正確的配置檔案。 避免使用特殊字元，並考慮包括區域、部門或權利。 此外，避免在您的組織層次結構中出現不常見的縮寫詞和模糊或類似的名稱。
>使用最多255個字元的清晰、可識別的組織名稱來幫助用戶選擇正確的配置檔案。 避免使用特殊字元，並考慮包括區域、部門或權利。 此外，避免在您的組織層次結構中出現不常見的縮寫詞和模糊或類似的名稱。

更改記錄在審核日誌中，所有用戶都通過電子郵件獲得通知，並且24小時內無法再次更新名稱。 [瞭解如何查看和下載審核日誌](https://helpx.adobe.com/enterprise/global-admin-console/insights.html)。

## 更改組織的父級

作為[[!DNL Global Administrator]](https://helpx.adobe.com/enterprise/global-admin-console/manage-administrators.html)，您可以使用&#x200B;**[!UICONTROL 更改層次結構]**&#x200B;按鈕重新為組織層次結構中的組織父級。

更改組織的父級具有以下影響：

- 重新管理組織會用它移動整個子樹，該子樹根植於重新父代組織。 重新父代組織及其子代的路徑名將更新，以反映其新位置。
- 已移動組織的組織[策略](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html)已更新，以便新層次結構中的組織保留策略上的所有鎖。
- 變更階層中組織的職位可以變更該組織的全域管理員。 全域管理角色是向下繼承至階層，因此新父級組織的任何全域管理員都會自動成為已移動組織的全域管理員。 同樣地，如果全域管理員是舊父系的全域管理員，因此失去其在已移動組織中的角色。 繼承的全域管理角色不會列在組織的「管理員」窗格中。
- 重新設定父級也會影響已移動組織中可用的產品。 可能的話，[產品配置](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html)會更新，因此會透過新的父位置來進行。
- 如果無法更新產品分配以從新父代中獲得，則產品將與這些產品的產品配置檔案一起刪除。 由於此操作，用戶可能會失去訪問權限。 要使產品在新位置可用，新舊位置最近的共同祖先必須具有產品可用性。

>[!WARNING]
>
>如果由於重新養育而刪除產品，用戶將無法訪問這些產品。

1. 登錄到[Global Admin Console](https://global-admin-console.adobe.com/)。 在&#x200B;**[!UICONTROL 組織]**&#x200B;頁籤中，選擇&#x200B;**[!UICONTROL 更改層次結構]**&#x200B;以啟用組織的重新管理。
2. 在出現的彈出螢幕中選擇「**[!UICONTROL 確定]**」。
3. 要重新父項，請將子組織拖動到所需組織的頂部。
4. 完成組織重新管理後，選擇&#x200B;**[!UICONTROL 保存]**。
5. 編輯完組織後，選擇&#x200B;**[!UICONTROL 審閱掛起的更改]**。 審閱後，選擇&#x200B;**[!UICONTROL 將更改]**&#x200B;提交到[執行](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html)。

作業完成後，您可以導航到「產品分配」，[更改授權值](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html)以反映產品資源分配的更改。

## 使用組織映射器添加現有組織

作為[全域管理員](https://helpx.adobe.com/enterprise/global-admin-console/manage-administrators.html)，您可以將目前不是Global Admin Console階層一部分的現有組織新增至組織階層。

您也可以將小組組織新增至組織階層。 團隊組織不會參與產品配置或產品使用彙總，而Global Admin Console中的團隊組織管理是有限的。 您可以將受眾新增至組織階層，以追蹤受眾，並可檢視受眾購買的產品。 專案團隊組織下不能有子組織，也沒有企業組織的許多功能。

深入瞭解產品配置[的](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html#limitations)限制。

>[!WARNING]
>
> 您只能將子組織新增至以相同儲存模型為基礎的根組織。 因此，根據使用者儲存模型的子組織只能新增至根據使用者儲存模型的根組織。 而且，基於企業儲存模型的子組織只能根據企業儲存模型添加到根組織中。
>您只能將子組織添加到基於相同儲存模型的根組織。 因此，基於用戶儲存模型的子組織只能根據用戶儲存模型添加到根組織中。 而且，基於企業儲存模型的子組織只能根據企業儲存模型添加到根組織中。

**[!UICONTROL 組織映射器]**&#x200B;頁籤顯示以下內容：

1. 一個下拉清單，其中列出了可添加子組織的可能父組織。 這些組織是您為其全局管理員的組織。
1. 可在步驟1中選定的父項下添加的子組織清單。 這些組織是您是系統管理員且尚未是其他組織的子組織。

將組織添加到全局管理時，使用組織映射器添加的組織中的產品將保留為採購；[產品分配](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html)數字將停止在這些組織中累計。

1. 登錄到[Global Admin Console](https://global-admin-console.adobe.com/)，然後導航到&#x200B;**[!UICONTROL 組織映射器]**。
2. 從下拉清單中選擇父組織。\
   這些是直接為您新增為全域管理員的組織。 在下拉式清單中，如果您沒有看到要當作父項使用的組織，請在階層中選取一個較高的組織。 組織對應程式作業完成後，您可以使用[變更階層](https://helpx.adobe.com/enterprise/global-admin-console/set-up-organizations.html#change-the-parent-of-an-organization)，將樹狀結構中的新組織下移，以擁有您要使用的父系。
3. 選擇要作為上一步中選定組織的子項添加的組織。
4. 選擇&#x200B;**[!UICONTROL 審閱掛起的更改]**。 然後，選擇&#x200B;**[!UICONTROL 將更改]**&#x200B;提交到[執行](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html)。
5. 執行更改後，您可以重複上述步驟，將附加子組織添加到組織層次結構中。

組織在層次結構中後，您可以通過導航到&#x200B;**[!UICONTROL 組織]**&#x200B;頁籤來調整組織策略、管理員或其他設定。
