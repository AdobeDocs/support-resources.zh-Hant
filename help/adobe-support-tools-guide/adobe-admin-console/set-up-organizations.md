---
title: 管理組織階層
description: 瞭解全域管理員如何在Global Admin Console中管理組織的階層。
Feature-set: Experience Cloud Services
Solution: Admin Console
Feature: Admin Console
exl-id: 6fcf16e3-0408-4961-9981-14d526e1ea28
source-git-commit: 976bfc44cdae61376e2da89019f7758518c6fadc
workflow-type: tm+mt
source-wordcount: '1527'
ht-degree: 0%

---

# 管理組織階層

適用於企業。

瞭解全域管理員如何在Global Admin Console中管理組織的階層。

取得[對 [!DNL Global Admin Console]](https://experienceleague.adobe.com/zh-hant/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/adopt-global-administration#request-access-to-the-global-admin-console)的存取權後，您可以建立新組織、將現有組織加入階層、刪除組織，以及變更父級組織。 前往這裡[登入Global Admin Console](https://global-admin-console.adobe.com/)

組織是一種用來管理Adobe產品和使用者的結構。 [[!DNL Adobe Admin Console]](https://experienceleague.adobe.com/zh-hant/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/admin-console-overview)可讓系統管理員管理其組織中產品與使用者的部署與設定。 [[!DNL Global Admin Console]](https://experienceleague.adobe.com/zh-hant/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/adopt-global-administration)可讓全域管理員建立、管理及刪除多個組織。

## 建立子組織

作為[全域管理員](https://experienceleague.adobe.com/zh-hant/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators)，您可以在階層中建立任何組織的子組織，並設定名稱、國家/地區、使用者群組、產品、產品設定檔、管理員和原則。

建立新的下階組織時，系統會自動從直接父項繼承下列專案：

- 組織的[原則](https://helpx.adobe.com/tw/enterprise/global-admin-console/update-policies.html)設定（如果有的話，包括鎖定）。
- 系統管理員清單（由&#x200B;**[!UICONTROL 建立]** [原則](https://helpx.adobe.com/tw/enterprise/global-admin-console/update-policies.html)時繼承系統管理員控制）。
下列專案可防止系統管理員被繼承：
   - 缺少[網域信任](https://helpx.adobe.com/tw/enterprise/using/directory-trust.html)。
   - 使用者型別限制（新增Adobe ID / Enterprise ID / Federated ID使用者原則）。 瞭解[原則詳細資料](https://helpx.adobe.com/tw/enterprise/global-admin-console/update-policies.html)。
- 從父級組織有權存取的網域存取[[!DNL Federated ID]]或[[!DNL Enterprise ID]]位使用者。 這使父項中的網域使用者可在子組織中使用。 使用者存取權的繼承由&#x200B;**從父系組織管理的目錄繼承使用者** [原則](https://helpx.adobe.com/tw/enterprise/global-admin-console/update-policies.html)。
- 共用原則、密碼原則及安全性連絡人（由&#x200B;**在建立子組織時繼承資產共用設定** [原則](https://helpx.adobe.com/tw/enterprise/global-admin-console/update-policies.html)）所控制。

1. 登入[Global Admin Console](https://global-admin-console.adobe.com/)。 在&#x200B;**[!UICONTROL 組織]**&#x200B;標籤中，選取您要新增子組織的組織。
2. 選取&#x200B;**[!UICONTROL 新增+]**&#x200B;圖示。
   ![新增組織](/help/adobe-support-tools-guide/assets/add-an-organization-1.png)
3. 指定組織的&#x200B;**名稱**&#x200B;和&#x200B;**國家/地區**。\
   組織的簡單名稱必須介於4到100個字元之間；路徑名稱的最大長度為255個字元。
   ![新增子組織](/help/adobe-support-tools-guide/assets/add-a-child-organization.png)
4. 選取「**[!UICONTROL 儲存]**」。
5. 在您編輯完組織後，選取&#x200B;**[!UICONTROL 檢閱擱置中的變更]**。 檢閱後，選取&#x200B;**[!UICONTROL 提交變更]**&#x200B;以[執行](https://helpx.adobe.com/tw/enterprise/global-admin-console/execute-jobs.html)它們。

## 刪除子組織

作為[全域系統管理員](https://experienceleague.adobe.com/zh-hant/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators)，您可以刪除子組織。 刪除操作無法復原，且無法刪除根組織。 分配給已刪除組織的資源會傳回至其父級組織。 刪除組織之前，其父項會自動成為其任何子組織的父項。

只有在符合下列條件時，才能刪除組織：

- 組織中沒有Sign帳戶、Adobe Stock購買或存放庫。
- 組織中沒有已宣告的網域。
- 組織中沒有具現化的產品。
- 沒有任何Experience Cloud產品可以包含組織中的具現化。

>[!WARNING]
>
>刪除組織會影響您的使用者。 確保刪除組織時沒有存取權或資訊會遺失。

1. 登入[[!DNL Global Admin Console]](https://global-admin-console.adobe.com/)。 移至&#x200B;**[!UICONTROL 組織]**&#x200B;標籤，並選取您要刪除的組織。
1. 選取&#x200B;**[!UICONTROL 刪除]**&#x200B;圖示。
   ![刪除組織](/help/adobe-support-tools-guide/assets/delete-organization.png)
1. 在&#x200B;**[!UICONTROL 刪除組織]**&#x200B;對話方塊中，選取&#x200B;**[!UICONTROL 確定]**。
1. 在您編輯完組織後，選取&#x200B;**[!UICONTROL 檢閱擱置中的變更]**。 檢閱後，選取&#x200B;**[!UICONTROL 提交變更]**&#x200B;以[執行](https://helpx.adobe.com/tw/enterprise/global-admin-console/execute-jobs.html)它們。

## 重新命名組織

組織名稱是貴公司或機構的正式名稱，在購買時設定。 使用者在登入期間選取設定檔時，尤其是如果他們可以從多個組織存取Adobe產品，或需要選擇企業和個人設定檔時，會看到此名稱。

身為[全域系統管理員](https://experienceleague.adobe.com/zh-hant/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators)，您可以編輯任何父或子組織的名稱，以協助使用者在登入[[!DNL Creative Cloud]]產品和服務時識別正確的設定檔。

1. 登入[Global Admin Console](https://global-admin-console.adobe.com/)。 在&#x200B;**[!UICONTROL 組織]**&#x200B;標籤中，選取您要重新命名的組織。
1. 選取&#x200B;**[!UICONTROL 編輯]**&#x200B;圖示。
   ![重新命名組織](/help/adobe-support-tools-guide/assets/rename-organization.png)
1. 更新您的組織名稱並選取&#x200B;**[!UICONTROL 儲存]**。

>[!TIP]
>
>使用清晰、可辨識的組織名稱（最多255個字元），協助使用者選取正確的設定檔。 避免使用特殊字元，並考慮包括地區、部門或軟體權利檔案。 此外，請避免貴組織階層中出現不常見的首字母縮略詞，以及名稱模糊或類似。

變更會記錄到稽核記錄中，所有使用者都會收到電子郵件通知，而且名稱無法在24小時內再次更新。 [瞭解如何檢視及下載稽核記錄](https://experienceleague.adobe.com/zh-hant/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/download-audit-logs-and-export-reports)。

## 變更組織的父系

作為[[!DNL Global Administrator]](https://experienceleague.adobe.com/zh-hant/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators)，您可以使用&#x200B;**[!UICONTROL 變更階層]**&#x200B;按鈕，重新父級組織階層中的組織。

變更組織的父項會產生下列影響：

- 重設父系組織會以其移動根在重設父系組織的整個子樹狀結構。 已重新父系的組織及其子系的路徑名稱會更新，以反映它們的新位置。
- 已移動組織的組織[原則](https://helpx.adobe.com/tw/enterprise/global-admin-console/update-policies.html)已更新，因此原則上的任何鎖定都由新階層中的組織保留。
- 變更階層中組織的職位可以變更該組織的全域管理員。 全域管理角色是向下繼承至階層，因此新父級組織的任何全域管理員都會自動成為已移動組織的全域管理員。 同樣地，如果全域管理員是舊父系的全域管理員，因此失去其在已移動組織中的角色。 繼承的全域管理角色不會列在組織的「管理員」窗格中。
- 重新設定父級也會影響已移動組織中可用的產品。 可能的話，[產品配置](https://helpx.adobe.com/tw/enterprise/global-admin-console/allocate-products.html)會更新，因此會透過新的父位置來進行。
- 如果產品配置無法更新為來自新的父項，則會移除產品以及這些產品的產品設定檔。 使用者可能會因此作業而失去存取權。 若要在新位置提供產品，舊位置和新位置最接近的共同祖先必須提供產品。

>[!WARNING]
>
>如果因重新設定家長而移除產品，使用者將無法存取這些產品。

1. 登入[Global Admin Console](https://global-admin-console.adobe.com/)。 在&#x200B;**[!UICONTROL 組織]**&#x200B;索引標籤中，選取&#x200B;**[!UICONTROL 變更階層]**&#x200B;以啟用重新設定組織的父系。
2. 在出現的快顯畫面中選取&#x200B;**[!UICONTROL 確定]**。
3. 若要重新父系，請將子組織拖曳到所需組織上。
4. 當您完成組織重設父系時，選取&#x200B;**[!UICONTROL 儲存]**。
5. 在您編輯完組織後，選取&#x200B;**[!UICONTROL 檢閱擱置中的變更]**。 檢閱後，選取&#x200B;**[!UICONTROL 提交變更]**&#x200B;以[執行](https://helpx.adobe.com/tw/enterprise/global-admin-console/execute-jobs.html)它們。

工作完成後，您可以導覽至「產品配置」並[變更授權值](https://helpx.adobe.com/tw/enterprise/global-admin-console/allocate-products.html)以反映產品資源配置的變更。

## 使用組織對應程式新增現有組織

作為[全域管理員](https://experienceleague.adobe.com/zh-hant/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators)，您可以將目前不是Global Admin Console階層一部分的現有組織新增至組織階層。

您也可以將小組組織新增至組織階層。 團隊組織不會參與產品配置或產品使用彙總，而Global Admin Console中的團隊組織管理是有限的。 您可以將受眾新增至組織階層，以追蹤受眾，並可檢視受眾購買的產品。 專案團隊組織下不能有子組織，也沒有企業組織的許多功能。

深入瞭解產品配置[的](https://helpx.adobe.com/tw/enterprise/global-admin-console/allocate-products.html#limitations)限制。

>[!WARNING]
>
> 您只能將子組織新增至以相同儲存模型為基礎的根組織。 因此，根據使用者儲存模型的子組織只能新增至根據使用者儲存模型的根組織。 而且，根據企業儲存模型的子組織只能新增至根據企業儲存模型的根組織。

**[!UICONTROL 組織對應程式]**&#x200B;索引標籤會顯示下列專案：

1. 包含可新增子項組織的可能父項組織清單的下拉式清單。 這些是您身為全域管理員的組織。
1. 可在步驟1中所選父項下新增的子組織清單。 這些組織是您身為系統管理員且尚未成為其他組織子項的組織。

將組織新增至全域管理時，使用組織對應程式新增的組織中的產品仍會維持為購買；[產品配置](https://helpx.adobe.com/tw/enterprise/global-admin-console/allocate-products.html)數字會停止在這些組織中的累計。

1. 登入[Global Admin Console](https://global-admin-console.adobe.com/)，並導覽至&#x200B;**[!UICONTROL 組織對應程式]**。
2. 從下拉式清單中選取父級組織。\
   這些是直接為您新增為全域管理員的組織。 在下拉式清單中，如果您沒有看到要當作父項使用的組織，請在階層中選取一個較高的組織。 組織對應程式作業完成後，您可以使用[變更階層](https://experienceleague.adobe.com/zh-hant/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/set-up-organizations#change-the-parent-of-an-organization)，將樹狀結構中的新組織下移，以擁有您要使用的父系。
3. 選取要新增為上一步驟中所選組織的子項的組織。
4. 選取&#x200B;**[!UICONTROL 檢閱擱置中的變更]**。 然後，選取&#x200B;**[!UICONTROL 提交變更]**&#x200B;以[執行](https://helpx.adobe.com/tw/enterprise/global-admin-console/execute-jobs.html)它們。
5. 執行變更後，您可以重複上述步驟，將其他子組織新增至您的組織階層。

當組織進入階層後，您可以導覽至&#x200B;**[!UICONTROL 組織]**&#x200B;標籤，以調整組織原則、管理員或其他設定。
