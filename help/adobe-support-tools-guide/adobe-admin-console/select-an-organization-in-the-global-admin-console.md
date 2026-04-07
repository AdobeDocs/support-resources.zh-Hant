---
title: 在Global Admin Console中選取組織
description: 瞭解如何選擇要在Global Admin Console中編輯的組織。
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
exl-id: 6a94922a-3343-433d-96e7-0af0f26581a1
source-git-commit: d5f0473b100cda574b4980e6c871a9c275f9f95a
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 1%

---

# 在Global Admin Console中選取組織

瞭解如何選擇要在Global Admin Console中編輯的組織。

>[!NOTE]
>
>存取[Global Admin Console](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/adopt-global-administration#request-access-to-the-global-admin-console)後，您可以先選取組織來檢視及管理組織的名稱、使用者群組、產品設定檔、管理員和組織原則。 若要登入，請前往[Global Admin Console](https://global-admin-console.adobe.com/)。

Global Admin Console是組織的中心，管理Adobe資源。 全域管理員可以：

- 在其組織下建立子組織
- 指派系統管理員來管理他們
- 將資源分配給子組織，以便管理並指定給這些組織中的使用者

>[!NOTE]
>
> 組織中的使用者和管理員無法檢視其組織外的使用者、儲存空間或其他資源。

## 選取您的組織

在&#x200B;**[!UICONTROL 組織選擇器]**&#x200B;下拉式清單中列出的組織是您明確為其全域管理員的組織，亦即，您被新增至具有全域管理員或全域檢視器角色之該組織的管理員清單。 您隱含地是階層中該點之下所有組織的全域管理員（或全域檢視器），但這些組織未列在[!UICONTROL 組織選擇器]中。

![組織選取器](/help/adobe-support-tools-guide/assets/org-picker.png)

如果您希望列出這些組織，請將您自己新增為要列出的組織的全域管理員。 當您在[!UICONTROL 組織選擇器]中選取組織時，您的管理許可權是以所選組織的全域管理員為基礎。 您可能也會在樹狀結構中以較高之父級組織的全域管理員身分列出，這會提供您更多許可權。 您必須選取較高層級組織才能取得其他許可權。

在Global Admin Console中，從[!UICONTROL 階層樹狀結構]選取組織後，您就可以開始編輯特定組織的資訊。

**編輯可能影響：**

- 組織名稱
- 使用者群組
- 產品設定檔
- 管理員
- 組織原則

**編輯無法影響：**

- 使用者（刪除群組或產品設定檔除外）
- 新增使用者（管理員除外）

從階層樹狀結構選取組織時，會顯示下列資訊：

- 組織名稱
- 區域
- 使用者人數
- 產品清單
- 產品設定檔
- 使用者群組
- 管理員
- 申請的網域
- 組織的原則值

若要檢視或編輯產品、使用者群組、管理員、網域、原則或原則範本，請選取適當的索引標籤。 在大多數情況下，您可以使用[!UICONTROL 搜尋]欄位來找出索引標籤中的特定專案。

![編輯組織](/help/adobe-support-tools-guide/assets/edit-an-organization.png)

任何新增至組織或從組織移除的管理員都會收到電子郵件通知。 某組織的某些原則變更會在該組織的Admin Console中產生通知。

## 瞭解限制和必要條件

- 巢狀組織的最大深度為5。 因此，允許a/b/c/d/e ，但a/b/c/d/e/f為錯誤。 例如，允許Acme Corp/ International Region/ Acme Europe/ Acme UK/ Acme London，但Acme Corp/ International Region/ Acme Europe/ Acme UK/ Acme London/ Acme Mayfair為錯誤。

- 路徑名稱長度上限（包括所有組織）為255個字元（包括&quot;/&quot;）。 單一組織名稱的最大長度介於4到100個字元之間。

- 組織路徑名稱是唯一的，但簡易名稱在其同層級中是唯一的。 組織階層中的其他位置可能有相同簡單名稱的組織。

- 您只能使用Global Admin Console檢視連結至所選組織的網域清單。 如果您是所選組織的系統管理員，請選取&#x200B;**[!UICONTROL 在Admin Console中開啟]**&#x200B;以[管理網域](https://helpx.adobe.com/enterprise/using/manage-domains-directories.html)。 若要瞭解[網域]索引標籤中顯示的資訊，請參閱[匯出和匯入結構描述](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/export-or-import-organization-structure-and-product-allocations#export-and-import-schemas)。

- IE 11不支援全域管理存取。 使用其他瀏覽器或更新版本的IE瀏覽器。
