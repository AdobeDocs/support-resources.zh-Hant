---
title: Adobe Admin Console使用者
description: 規劃在Adobe Admin Console上管理使用者的策略 — 新增管理員和一般使用者、選擇使用者管理方法並指派授權。
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
source-git-commit: d92f4190b68a480409f4126a877de3469ed836f0
workflow-type: tm+mt
source-wordcount: '842'
ht-degree: 3%

---

# Adobe Admin Console使用者

適用於企業和團隊。

面對這些問題之一？ 選取問題以檢視解決方案。

- [管理系統管理員角色](https://helpx.adobe.com/enterprise/using/admin-roles.html)
- [下載安裝問題](https://helpx.adobe.com/download-install.html)
- [重設Enterprise ID使用者密碼](https://helpx.adobe.com/enterprise/kb/enterprise-id-faq.html#faq)
- [解決Federated ID錯誤](https://helpx.adobe.com/enterprise/kb/tshoot-fed-id.html)
- [刪除使用者或還原已刪除的使用者](https://helpx.adobe.com/enterprise/using/manage-directory-users.html)

**Adobe Admin Console — 使用者** — [在YouTube上觀看](https://youtu.be/w8b36YX2TEM)

## 為何要將使用者新增至Adobe Admin Console

>[!NOTE]
>
>身為Adobe Admin Console的管理員，在您選擇您的[身分型別](https://helpx.adobe.com/tw/enterprise/using/identity.html)和[設定身分](https://helpx.adobe.com/tw/enterprise/using/set-up-identity.html)後，您的下一個任務是將使用者新增到Admin Console。

Adobe enterprise和teams廣泛定義了兩種使用者：

### 管理員（管理員）

企業或團隊管理員會在Admin Console上執行管理任務。 您可以新增管理員來定義靈活的管理階層，以便更精細地管理Adobe產品存取、使用及其他管理任務。

所有管理員都必須新增至Admin Console。 新增管理員時，管理員許可權是以其[管理員角色](https://helpx.adobe.com/enterprise/using/admin-roles.html)為基礎。

### 一般使用者

一般使用者是指貴組織或機構中使用您組織或機構在Adobe合約中取得的Adobe產品和服務的使用者。

## 決定您的使用者管理策略

視您的需求而定，您需個別新增、移除或更新使用者&#x200B;**，或使用其中一個可用的&#x200B;*大量上傳方法*。 使用下列矩陣作為規劃使用者管理的指南。

>[!NOTE]
>
>如果您是新的Adobe企業或團隊客戶，建議您先詳閱此表格，然後再開始在Admin Console上管理使用者。 現有客戶可以使用此功能，尤其是如果他們計畫從一種身分型別移轉至另一種身分型別（請參閱[編輯身分型別](https://helpx.adobe.com/enterprise/using/switch-user-identity.html)）。

<table>
<thead>
<tr>
<th scope="col"></th>
<th scope="col"><strong>個別(Admin Console)</strong></th>
<th scope="col"><strong>CSV大量上傳(Admin Console)</strong></th>
<th scope="col"><strong>Azure / Google聯結器</strong></th>
<th scope="col"><strong>使用者同步工具</strong></th>
<th scope="col"><strong>使用者管理REST API</strong></th>
</tr>
</thead>
<tbody>
<tr>
<th scope="row"><strong>套用至</strong></th>
<td colspan="2">Adobe團隊和企業客戶</td>
<td colspan="3">Adobe企業客戶</td>
</tr>
<tr>
<th scope="row"><strong>說明</strong></th>
<td>在Admin Console中個別管理使用者。</td>
<td>在Admin Console中透過CSV檔案上傳管理使用者。</td>
<td>根據您現有的Azure AD入口網站或Google同盟來管理使用者（和群組）。</td>
<td colspan="2">根據您組織的LDAP管理使用者（和群組）。</td>
</tr>
<tr>
<th scope="row"><strong>新增使用者</strong></th>
<td><strong>Admin Console</strong>中的<strong>使用者</strong>索引標籤。 <a href="https://helpx.adobe.com/enterprise/using/manage-users-individually.html#add-users">閱讀全文</a>。</td>
<td>在<strong>Admin Console</strong>中使用<strong>透過CSV</strong>新增使用者。 <a href="https://helpx.adobe.com/enterprise/using/bulk-upload-users.html">閱讀更多</a>。<em> （使用預設的CSV範本。）</em></td>
<td>在<a href="https://helpx.adobe.com/enterprise/using/sso-setup-azure.html">Azure</a>或<a href="https://helpx.adobe.com/enterprise/using/setup-sso-google.html">Google</a>中新增使用者。 或透過<strong>Admin Console</strong>進行。</td>
<td colspan="2">您應將使用者新增至組織的LDAP中。</td>
</tr>
<tr>
<th scope="row"><strong>移除使用者</strong></th>
<td>在<strong>Admin Console</strong>中選取並移除使用者。 <a href="https://helpx.adobe.com/enterprise/using/manage-users-individually.html#remove-users">閱讀全文</a>。</td>
<td>在<strong>Admin Console</strong>的<strong>使用者</strong>索引標籤中選擇<strong>透過CSV移除使用者</strong>。 <a href="https://helpx.adobe.com/enterprise/using/bulk-upload-users.html#remove-users">閱讀更多</a>。<em> （使用預設的CSV範本。）</em></td>
<td>必須在<a href="https://helpx.adobe.com/enterprise/using/sso-setup-azure.html">Azure</a>或<a href="https://helpx.adobe.com/enterprise/using/setup-sso-google.html">Google</a>中移除使用者。</td>
<td colspan="2">確定使用者資訊已同步。 <strong>警告：</strong>不在您組織LDAP中的使用者會從Admin Console中移除。</td>
</tr>
<tr>
<th scope="row"><strong>編輯使用者詳細資訊</strong></th>
<td>選取使用者，然後在Admin Console中<strong>編輯使用者詳細資訊</strong>。 <a href="https://helpx.adobe.com/enterprise/using/manage-users-individually.html#edit-user-details">閱讀全文</a>。</td>
<td>在<strong>Admin Console</strong>的<strong>使用者</strong>索引標籤中選擇<strong>依CSV編輯使用者詳細資訊</strong>。 <a href="https://helpx.adobe.com/enterprise/using/bulk-upload-users.html#edit-user-details">閱讀更多</a>。<em> （使用預設的CSV範本。）</em></td>
<td>必須在<a href="https://helpx.adobe.com/enterprise/using/sso-setup-azure.html">Azure</a>或<a href="https://helpx.adobe.com/enterprise/using/setup-sso-google.html">Google</a>中變更所有使用者資訊。</td>
<td colspan="2">確定使用者資訊已同步。</td>
</tr>
<tr>
<th scope="row"><strong>支援的身分型別</strong></th>
<td colspan="2">全部</td>
<td>Federated ID</td>
<td colspan="2">Federated ID和Enterprise ID</td>
</tr>
<tr>
<th scope="row"><strong>最大 每個操作的更新</strong></th>
<td>10</td>
<td>25,000 （<em>5,000為最佳效能</em>）</td>
<td colspan="3">無限制（對應至您組織的LDAP）</td>
</tr>
<tr>
<th scope="row"><strong>需要</strong></th>
<td>Adobe Admin Console</td>
<td>建立和更新.csv檔案格式，最好使用Microsoft Excel</td>
<td>您必須設定Azure AD或Google同盟</td>

<td>
  <ul>
    <li>macOS終端機或Windows命令提示</li>
    <li>瞭解LDAP</li>
  </ul>
</td>

<td>有關程式設計語言（例如Python）的工作知識，能使用REST API</td>
</tr>
<tr>
<th scope="row"><strong>閱讀全文</strong></th>
<td><a href="https://helpx.adobe.com/tw/enterprise/using/manage-users-individually.html">管理個別使用者</a></td>

<td>
  <ul>
    <li>
      <a href="https://helpx.adobe.com/enterprise/using/bulk-upload-users.html">
        管理使用者|大量上傳CSV
      </a>
    </li>
    <li>
      <a href="https://helpx.adobe.com/enterprise/kb/troubleshoot-bulk-user-csv-upload.html">
        疑難排解大量使用者CSV上傳
      </a>
    </li>
  </ul>
</td>

<td>
  <ul>
    <li>
      <a href="https://helpx.adobe.com/enterprise/using/sso-setup-azure.html">
        Azure AD聯結器
      </a>
    </li>
    <li>
      <a href="https://helpx.adobe.com/enterprise/using/setup-sso-google.html">
        Google同盟聯結器
      </a>
    </li>
  </ul>
</td>

<td>
  <ul>
    <li>
      <a href="https://adobe-apiplatform.github.io/user-sync.py/en/">
        關於使用者同步
      </a>
    </li>
    <li>
      <a href="https://github.com/adobe-apiplatform/user-sync.py">
        Git存放庫
      </a>
    </li>
    <li>
      <a href="https://helpx.adobe.com/enterprise/using/user-sync.html">
        逐步指南
      </a>
    </li>
  </ul>
</td>
<td><a href="https://developer.adobe.com/umapi/">關於UMAPI</a></td>
</tr>
</tbody>
</table>

## 後續步驟

### 建立封裝

新增後，您的使用者已準備好指派他們指定的應用程式和服務。

根據您的授權方式指派授權給一般使用者：

- **具名使用者授權：**&#x200B;將這些使用者新增至&#x200B;**產品** （[適用於團隊](https://helpx.adobe.com/enterprise/using/assign-licenses-to-teams-users.html)）或&#x200B;**產品設定檔** （[適用於企業](https://helpx.adobe.com/tw/enterprise/using/manage-product-profiles.html)），以授予Adobe產品和服務權益。 如需詳細資訊，請參閱如何[建立具名使用者授權套件](https://helpx.adobe.com/enterprise/using/create-nul-packages.html)和[產品設定檔](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html#create-product-profile)。
- **共用裝置授權：** [新增的使用者](https://helpx.adobe.com/enterprise/using/sdl-deployment-guide.html#add-users-admin-console)可以使用已設定的共用裝置，只有&#x200B;**組織使用者才能存取**。 如需詳細資訊，請參閱[建立SDL封裝](https://helpx.adobe.com/enterprise/using/create-sdl-packages.html)。

### 部署套件

建立封裝後，請使用下列其中一種方法將其部署到使用者端電腦：

- 移至使用者端電腦，然後按兩下套件檔案（Windows或macOS）。
- 使用Windows命令提示字元或macOS終端機。
- 使用協力廠商工具：
   - [Microsoft Intune](https://helpx.adobe.com/enterprise/kb/deploy-packages-using-ms-intune.html)
   - [Microsoft System Center Configuration Manager (SCCM)](https://helpx.adobe.com/enterprise/kb/deploy-packages-using-sccm.html)
   - [Apple遠端案頭(ARD)](https://helpx.adobe.com/enterprise/kb/deploy-packages-using-ard.html)
   - [JAMF Pro](https://helpx.adobe.com/enterprise/kb/deploy-packages-using-jamf-pro.html)
   - [Munki](https://helpx.adobe.com/enterprise/kb/deploy-packages-using-munki.html)

## 相關閱讀

- [管理使用者|個別](https://helpx.adobe.com/tw/enterprise/using/manage-users-individually.html)
- [管理使用者|大量CSV上傳](https://helpx.adobe.com/enterprise/using/bulk-upload-users.html)
- [管理目錄使用者](https://helpx.adobe.com/enterprise/using/manage-directory-users.html)
- [Admin Console](https://helpx.adobe.com/tw/enterprise/using/admin-console.html)
- [將使用者指派給產品設定檔（適用於企業和機構）](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html#assign-users)
- [指派授權給團隊使用者](https://helpx.adobe.com/enterprise/using/assign-licenses-to-teams-users.html)
- [商務儲存模型](https://helpx.adobe.com/enterprise/kb/business-storage-model-introduction.html)