---
title: 身分總覽
description: 瞭解並選擇您組織的身分型別（Federated ID、Enterprise ID、Adobe ID和個人Adobe ID），並在Admin Console中管理使用者存取權。
Feature-set: Experience Cloud Services
Solution: Admin Console
Feature: Admin Console
source-git-commit: c066e95c05f8e8a0953daecda9a220268d325f98
workflow-type: tm+mt
source-wordcount: '723'
ht-degree: 5%

---


# 身分總覽

適用於企業和團隊。

Adobe的identity management system可協助管理員建立和管理使用者對應用程式和服務的存取權。 Adobe提供這些身分型別或帳戶，用於驗證和授權使用者。

## Adobe Admin Console上的身分型別

身分型別可讓組織以不同層級控制使用者的帳戶和資料。 您選擇的身分模型對於貴組織儲存和共用資產的方式有相當大影響。 雖然Federated ID和Enterprise ID模型是由組織建立和管理的，但Adobe ID是由個人建立和管理的。

下表會引導您選擇最適合貴組織的身分識別模式。

>[!NOTE]
>如果您的組織尚未更新為Adobe的企業儲存模式，而且您仍在使用適用於個人的Adobe ID，請參閱下方[身分型別表格](https://helpx.adobe.com/tw/enterprise/using/identity.html#using-personal-adobe-id)中的說明。

<table>
<thead>
<tr>
<th scope="col">身分型別</th>

<th scope="col" style="text-align: center;">
  <img src="./assets/federated-id.png" alt="Federated ID圖示"><br>
  Federated ID
</th>
<th scope="col" style="text-align: center;">
  <img src="./assets/enterprise-id.png" alt="Enterprise ID"><br>
  Enterprise ID
</th>
<th scope="col" style="text-align: center;">
  <img src="./assets/adobe-id.png" alt="Adobe ID"><br>
  Adobe ID
</th>
</tr>
</thead>
<tbody>
<tr>
<th scope="row"><strong>重要方案</strong></th>
<td>由組織建立、擁有和管理。 組織管理使用者認證，並透過SAML2身分提供者(IdP)使用單一登入(SSO)。</td>
<td>由組織建立、擁有和管理。 組織保留在已驗證網域上建立使用者帳戶的專屬權利。</td>
<td>由一般使用者建立、擁有和管理。 Adobe會執行驗證，而一般使用者會管理身分。 根據<a href="https://helpx.adobe.com/tw/enterprise/using/storage-for-business.html">儲存模式</a>，使用者或企業仍可控制檔案和資料。 在未驗證、公開或信任的網域上建立Adobe ID帳戶。 請參閱下面附註一節的要點2。</td>
</tr>
<tr>
<th scope="row"><strong>帳戶與資料所有權</strong></th>
<td colspan="2">組織擁有與控制</td>
<td>企業儲存空間由組織擁有，使用者儲存空間由使用者擁有</td>
</tr>
<tr>
<th scope="row"><strong>安全性與監控</strong></th>
<td colspan="2">
  <ul>
    <li>稽核記錄</li>
    <li>內容記錄</li>
    <li>共用限制</li>
    <li>組織的驗證設定</li>
  </ul>
</td>

<td>
  <ul>
    <li>內容記錄</li>
    <li>共用限制</li>
    <li>密碼原則</li>
  </ul>
</td>

</tr>
<tr>
<th scope="row"><strong>重設密碼</strong></th>
<td colspan="2">不支援</td>
<td><a href="https://helpx.adobe.com/tw/manage-account/using/change-or-reset-password.html">重設您的帳戶密碼</a></td>
</tr>
<tr>
<th scope="row"><strong>適用於企業的Creative Cloud和適用於企業的Document Cloud</strong></th>
<td colspan="3">支援</td>
</tr>
<tr>
<th scope="row"><strong>適用於團隊的Creative Cloud和適用於團隊的Document Cloud</strong></th>
<td colspan="2">不支援</td>
<td>支援</td>
</tr>
<tr>
<th scope="row"><strong>Experience Cloud</strong></th>
<td colspan="3">支援</td>
</tr>
<tr>
<th scope="row"><strong>建議用於</strong></th>
<td>
  <ul>
    <li>已使用SSO或SAML的組織</li>
    <li>現有的目錄服務（例如Google和Azure AD）</li>
    <li>需要與非Adobe服務輕鬆整合</li>
    <li>可以展示網域的所有權</li>
  </ul>
</td>
<td>
  <ul>
    <li>可以展示網域的所有權</li>
    <li>不需要SSO</li>
  </ul>
</td>
<td>
  <ul>
    <li>適用於團隊的Creative Cloud</li>
    <li>組織偏好使用他們未擁有的網域</li>
    <li>公用網域（例如Hotmail、Gmail）</li>
    <li>存取Adobe Experience Manager Mobile等應用程式</li>
  </ul>
</td>
</tr>
<tr>
<th scope="row"><strong>開始使用</strong></th>
<td><a href="https://helpx.adobe.com/tw/enterprise/using/set-up-identity.html">設定身分</a></td>
<td><a href="https://helpx.adobe.com/tw/enterprise/using/add-domains-directories.html#claim-domains">宣告網域</a></td>
<td><a href="https://helpx.adobe.com/tw/enterprise/using/users.html#add-users">新增使用者</a></td>
</tr>
</tbody>
</table>

>[!NOTE]
>
>1. 適用於團隊的Creative Cloud的密碼原則與適用於個人的Creative Cloud的密碼原則相同。
>1. Adobe ID使用者使用其Adobe ID憑證或透過其所屬組織的驗證模型（SSO、2FA等）進行驗證。 在這種情況下，會將使用者重新導向至所屬組織的SSO頁面。 驗證之後，使用者可能需要[選擇企業設定檔](https://helpx.adobe.com/tw/enterprise/kb/enterprise-id-faq.html#choose-profile)。

## 使用個人Adobe ID

Adobe正在更新所有團隊和企業客戶，以使用Adobe的企業儲存模式。 如果您的組織有使用個人Adobe ID存取其公司或學校Adobe應用程式和服務的使用者，請參閱下表。

### 個人Adobe ID

<table>
<thead>
<tr>
<th scope="col">身分識別類型</th>
</th>
<th scope="col" style="text-align: center;">
  <img src="./assets/personal-adobe-id.png" alt="Adobe ID"><br>
  個人Adobe ID
</th>
</tr>
</thead>
<tbody>
<tr>
<th scope="row"><strong>重要方案</strong></th>
<td>由一般使用者建立、擁有和管理。 Adobe會執行驗證，而一般使用者會管理身分。</td>
</tr>
<tr>
<th scope="row"><strong>帳戶與資料所有權</strong></th>
<td>使用者控制</td>
</tr>
<tr>
<th scope="row"><strong>安全性與監控</strong></th>
<td>密碼原則。 請參閱下面附註一節中的要點1。</td>
</tr>
<tr>
<th scope="row"><strong>重設密碼</strong></th>
<td><a href="https://helpx.adobe.com/tw/manage-account/using/change-or-reset-password.html">重設您的帳戶密碼。</a>請參考以下附註一節中的要點2。</td>
</tr>
<tr>
<th scope="row"><strong>適用於企業的Creative Cloud和適用於企業的Document Cloud</strong></th>
<td>支援</td>
</tr>
<tr>
<th scope="row"><strong>Experience Cloud</strong></th>
<td>支援</td>
</tr>
<tr>
<th scope="row"><strong>僅適用於/建議用於</strong></th>
<td>
  <ul>
    <li>企業與團隊客戶在移轉前上線</li>
    <li>適用於團隊的Creative Cloud</li>
    <li>想要控制使用者的手</li>
    <li>存取Digital Publishing Suite等應用程式</li>
    <li>使用者從組織分離後擁有資產</li>
  </ul>
</td>
</tr>
<tr>
<th scope="row"><strong>開始使用</strong></th>
<td><a href="https://helpx.adobe.com/tw/enterprise/using/users.html#add-users">新增使用者</a></td>
</tr>
</tbody>
</table>

>[!NOTE]
>
>1. 適用於團隊的Creative Cloud的密碼原則與適用於個人的Creative Cloud的密碼原則相同。
>1. 針對使用[企業儲存空間](https://helpx.adobe.com/tw/enterprise/using/manage-adobe-storage.html)的企業客戶Creative Cloud，管理員可以將Adobe ID使用者新增至Admin Console，但無法將其新增至產品設定檔。 管理員必須將Adobe ID使用者移轉至另一個身分型別。
>1. 有些產品和服務（例如&#x200B;**Adobe授權網站）僅支援** Adobe ID。

## 更多相關資訊

- [設定身分](https://helpx.adobe.com/tw/enterprise/using/set-up-identity.html)
- [切換使用者身分](https://helpx.adobe.com/tw/enterprise/using/switch-user-identity.html)
- [Admin Console概觀](https://helpx.adobe.com/enterprise/using/admin-console-overview.html)
- [教育常見問題集](https://helpx.adobe.com/enterprise/using/education-faq.html)
- [新增和管理使用者](https://helpx.adobe.com/tw/enterprise/using/users.html)