---
title: 管理管理員
description: Adobe客戶如何在Global Admin Console中設定和管理管理員，以控制使用者存取、產品授權和組織資源。
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
exl-id: 41c00379-98ee-4922-8eba-cc373c23a019
source-git-commit: 8860538190e99e171abc6273adda321443e41fed
workflow-type: tm+mt
source-wordcount: '1159'
ht-degree: 2%

---

# 管理管理員

*套用至企業。*

探索全域管理員權能，並瞭解如何將使用者、產品授權和群組的管理委派和分發給每個組織的管理員。

在Global Admin Console中，您可以選取組織並導覽至&#x200B;**[!UICONTROL 管理員]**&#x200B;索引標籤，以新增、編輯或移除管理員許可權。 若要瞭解更多資訊，請參閱[採用全域管理](https://helpx.adobe.com/enterprise/global-admin-console/adopt-global-administration.html)。 移至[Global Admin Console](https://global-admin-console.adobe.com/)登入。


Global Admin Console引進了稱為全域管理員的角色。 此角色與系統管理員不同，可讓您進行以下操作：

- 檢視新增至Adobe階層之所有Admin Console中Global Admin Console投資總額的全球格局。
- 監視多個Admin Console中的Adobe授權和資源指派及使用情況。
- 建立管理主控台或組織。
- 從根或父Admin Console配置產品授權給位於階層內下方的子Admin Console。
- 維持日常作業，同時系統管理員繼續管理自己的Admin Console。 例如，全域管理員可以將產品指派給子項Admin Console，但無法將產品指派給使用者。 系統管理員將會收到其Admin Console中的名額，並將產品指派給其使用者。
- 可選擇將組織原則套用至階層中的任何Admin Console。

## 基本管理任務

Global Admin Console的設計可在多個組織和Admin Console中運作。 下表概述各種功能及其完成位置，即Admin Console或Global Admin Console。

<table>
  <tr>
    <th colspan="2">任務</th>
    <th>Global Admin Console</th>
    <th>Admin Console</th>
  </tr>

<tr>
    <td colspan="2">建立、重新父系及刪除子組織</td>
    <td align="center">是</td>
    <td align="center">無</td>
  </tr>

<tr>
    <td colspan="2">使用多個組織</td>
    <td align="center">是</td>
    <td align="center">無</td>
  </tr>

<tr>
    <td rowspan="2" valign="middle">管理管理員</td>
    <td>針對一或多個組織</td>
    <td align="center">是</td>
    <td align="center">無</td>
  </tr>

<tr>
    <td>針對一個組織</td>
    <td align="center">是</td>
    <td align="center">是</td>
  </tr>

<tr>
    <td colspan="2">管理產品設定檔和使用者群組</td>
    <td align="center">是</td>
    <td align="center">是</td>
  </tr>

<tr>
    <td colspan="2">定義和管理原則</td>
    <td align="center">是</td>
    <td align="center">無</td>
  </tr>

<tr>
    <td colspan="2">跨組織分配產品</td>
    <td align="center">是</td>
    <td align="center">無</td>
  </tr>

<tr>
    <td colspan="2">配置產品給使用者</td>
    <td align="center">無</td>
    <td align="center">是</td>
  </tr>

<tr>
    <td colspan="2">管理使用者</td>
    <td align="center">無</td>
    <td align="center">是</td>
  </tr>

<tr>
    <td colspan="2">管理套件</td>
    <td align="center">無</td>
    <td align="center">是</td>
  </tr>

<tr>
    <td colspan="2">設定網域和目錄</td>
    <td align="center">無</td>
    <td align="center">是</td>
  </tr>

<tr>
    <td colspan="2">管理企業儲存和加密</td>
    <td align="center">無</td>
    <td align="center">是</td>
  </tr>
</table>

## 管理管理員

您可以建立彈性的管理階層，以對Adobe產品的存取和使用進行更精細的管理。 與Adobe Admin Console類似，Global Admin Console可讓您新增系統管理員、產品管理員、產品設定檔管理員、使用者群組管理員、部署管理員、支援管理員和儲存管理員。 這些管理員可以在他們身為管理員的組織中執行其個別的管理任務。 除了這些角色之外，全域管理還新增了兩個角色：全域管理員和全域檢視器。

全域管理員是一個可轉移的角色。 讓使用者成為組織的全域管理員可直接或間接讓該使用者成為該組織所有子系的全域管理員。 此外，如果在組織階層中建立新組織，則該組織任何父項的所有全域管理員將立即成為新建立組織的全域管理員。

下列是全域管理員角色的功能：

- 建立和刪除子組織
- 設定和編輯原則
- 設定及修改管理角色
- 新增和移除子組織中的產品
- 設定或變更子組織的資源配置
- 管理產品設定檔和使用者群組

以下是「全域檢視器」角色的功能：

- 檢視組織和子組織中的使用者群組、產品、產品設定檔、管理員、原則集和資源清單。

## 分散式管理

透過管理管理員，全域管理員可以將使用者、產品授權和群組的管理委派並分發給每個組織的管理員。 由全域管理員新增到組織的管理員，可以靈活地管理組織，而不會看到其他組織的管理。 因此，全域管理員可以委派資源的管理作業，並讓使用者隔離這些資源和使用者的資料。

全域管理員可以建立組織、將產品和儲存體等資源分配給這些組織、管理身分設定，以及建立和套用組織原則範本。 由全域管理員新增到組織的系統管理員可以將產品指派給使用者、將使用者上線、建立和管理產品設定檔，以及在該組織內執行其他管理任務。

## 新增管理員

1. 在[Global Admin Console](https://global-admin-console.adobe.com/)中，選取要編輯的組織，然後導覽至&#x200B;**[!UICONTROL 管理員]**&#x200B;索引標籤。

1. 選取&#x200B;**[!UICONTROL 新增管理員]**。

   ![Global Admin Console新增管理員](../assets/global-admin-console-add-admin.png)

1. 在&#x200B;**[!UICONTROL 新增管理員]**&#x200B;對話方塊中，輸入&#x200B;**[!UICONTROL 使用者詳細資料]**：電子郵件、名字、姓氏、帳戶型別和國家/地區代碼。

   如果您嘗試將現有使用者新增為管理員，請選擇與現有使用者相同的帳戶型別，否則新增作業將失敗。

   >[!NOTE]
   >
   > 組織對於可以新增的帳戶型別可以有限制。 這些可能以[原則](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html)或組織的其他組態引數為基礎。 組織不允許同時新增AdobeID使用者和BusinessID使用者。 一般而言，組織中不應有同時屬於這兩種型別的使用者，但根據規則設定的順序，可能會有特定「帳戶型別」的某些使用者預先設定原則或規則的應用日期。

1. 從&#x200B;**[!UICONTROL 管理員許可權]**&#x200B;區段中選取一或多個管理員角色。

   對於角色（例如產品管理員、產品設定檔管理員和使用者群組管理員），請分別選取特定的產品、設定檔和群組。

   ![Global Admin Console新增管理員](../assets/global-admin-console-add-admin-detail.png)

1. 選取「**[!UICONTROL 儲存]**」。

1. 編輯組織後，請選取&#x200B;**[!UICONTROL 檢閱擱置的變更]**，然後選取&#x200B;**[!UICONTROL 提交變更]**&#x200B;以[執行](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html)變更。

新增管理員角色時，使用者會收到電子郵件通知，告知他們角色已變更。

新增管理員後，他們會收到電子郵件訊息，邀請他們接受其角色，並給他們提供Admin Console的連結。 如果他們同時被新增為全域管理員和某些其他角色，他們將收到兩個邀請，一個邀請給Global Admin Console，一個邀請給Admin Console。

## 編輯管理員

1. 選取要編輯的組織，並導覽至「**[!UICONTROL 管理員]**」標籤。

1. 選取相關管理員的&#x200B;**[!UICONTROL 更多選項]** (⋮)圖示，然後選取&#x200B;**[!UICONTROL 編輯管理員]**。

   ![Global Admin Console編輯管理許可權](../assets/global-admin-console-edit-admin-right.png)

1. 更新管理員詳細資料，然後選取[儲存]。**&#x200B;**

1. 在您編輯完組織後，選取&#x200B;**[!UICONTROL 檢閱擱置中的變更]**。

每個新增或移除的管理員角色在暫止變更清單中都會顯示一個單獨的命令。 檢閱後，選取&#x200B;**[!UICONTROL 提交變更]**&#x200B;以[執行](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html)它們。

## 移除管理員許可權

1. 選取要編輯的組織，並導覽至「**[!UICONTROL 管理員]**」標籤。

1. 選取相關管理員的&#x200B;**[!UICONTROL 更多選項]** (⋮)圖示，然後選取&#x200B;**[!UICONTROL 移除管理員許可權]**。

   ![Global Admin Console移除管理員許可權](../assets/global-admin-console-remove-admin-right.png)

1. 在確認對話方塊中選取&#x200B;**[!UICONTROL 確定]**。

1. 在您編輯完組織後，選取&#x200B;**[!UICONTROL 檢閱擱置中的變更]**。 檢閱後，選取&#x200B;**[!UICONTROL 提交變更]**&#x200B;以[執行](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html)它們。

刪除管理員後，使用者會收到電子郵件通知，告知他們該組織的Admin Console存取權已喪失。
