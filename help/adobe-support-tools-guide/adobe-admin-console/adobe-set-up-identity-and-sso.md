---
title: 設定身分和單一登入
description: 瞭解組織系統管理員如何使用Adobe ID、Enterprise ID或Federated ID在Adobe Admin Console中設定使用者身分和單一登入(SSO)。
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
source-git-commit: 0c2992946f1cdbbcfb44a2baf37888bd05b2253b
workflow-type: tm+mt
source-wordcount: '870'
ht-degree: 1%

---

# 設定身分和單一登入

**套用至：**&#x200B;企業

瞭解如何在Adobe Admin Console中設定身分識別。 比較Adobe ID、Enterprise ID和Federated ID，並設定單一登入(SSO)以安全地存取Adobe應用程式。

設定身分並設定單一登入(SSO)，讓員工可以使用現有的組織認證[登入](https://adminconsole.adobe.com/settings/)。

以下是有關如何[設定身分和SSO (YouTube)](https://youtu.be/V57lU4zaSBs)的影片教學課程。

## 重要辭彙和概念

### 目錄

Admin Console中的目錄是儲存諸如驗證之類的使用者和原則等資源的實體。 這些目錄類似於LDAP或Active Directories。

### 身分提供者(IdP)

身分提供者(IdP)是您組織的身分提供者，例如：

- 主動式目錄
- Microsoft Azure
- Ping
- Okta
- 共用
- Shibboleth

### 相關角色

| 角色 | 責任 |
|------|----------------|
| 系統管理員 | 與IdP目錄管理員和DNS管理員合作，在Admin Console中設定身分識別。 |
| DNS管理員 | 更新DNS權杖以驗證網域所有權。 |
| 識別提供者(IdP)目錄管理員 | 處理IdP入口網站和相關聯的聯結器。 |

### Adobe ID

由一般使用者建立、擁有和管理。 Adobe會執行驗證，而一般使用者會管理身分。 根據[儲存模式](https://helpx.adobe.com/enterprise/using/storage-for-business.html)，使用者或企業仍可控制檔案和資料。

對於已更新為企業儲存模式的組織，資產和資料由組織控制。 對於尚未更新的組織，此個人擁有並控制Adobe ID資產。

### Enterprise ID

由組織建立、擁有和管理。 Adobe會託管Enterprise ID並執行驗證，但組織會維護Enterprise ID。 管理員會建立Enterprise ID並核發給使用者。 管理員可以接管帳戶或刪除Enterprise ID以永久封鎖相關資料的存取權，藉此撤銷對產品和服務的存取權。 若要深入瞭解，請按一下[這裡](https://helpx.adobe.com/enterprise/using/setup-enterprise-id.html)。

### Federated ID

由組織建立和擁有，並透過同盟連結至企業目錄。 組織會透過SAML2身分提供者(IdP)管理憑證並處理單一登入。

以下是一些建議使用Federated ID的要求和情況：

- 如果您要根據您組織的企業目錄提供使用者。
- 如果您想要管理使用者的驗證。
- 如果您需要維持嚴格控制使用者可用的應用程式和服務。

## 設定身分而不使用單一登入

如果您的組織目前未在其他應用程式上使用SSO，您可使用Adobe ID或Enterprise ID。

## 使用Adobe ID

Adobe正在將所有組織更新至[企業儲存模型](https://helpx.adobe.com/enterprise/using/storage-for-business.html)。 這可讓貴組織更好地控制使用者的資產和資料。

開始使用[新增使用者](https://helpx.adobe.com/tw/enterprise/using/users.html)至Admin Console。

## 使用Enterprise ID設定身分

如果您想要在不使用SSO的情況下對使用者的資料進行更多控制，您可以設定Enterprise ID目錄。 只有管理員可建立Enterprise ID並核發給使用者。

請參閱[使用Enterprise ID設定組織](https://helpx.adobe.com/enterprise/using/setup-enterprise-id.html)，以取得建立Enterprise ID目錄的要求和步驟。

## 以單一登入設定身分

您必須使用Federated ID帳戶設定使用者身分才能使用SSO。

建議在下列情況下使用Federated ID：

- 您必須嚴格控制使用者可用的應用程式和服務。
- 您想要管理使用者的驗證。
- 您想要根據您組織的企業目錄提供使用者。

## 設定新的SSO整合

您可以使用熱門的身分識別服務提供者（例如Microsoft Azure AD、Google），或使用其他以SAML為基礎的IdP，為您的組織與Adobe產品設定SSO。

**Azure AD** （建議使用） - [設定SSO並與Azure AD Connector進行使用者同步](https://helpx.adobe.com/enterprise/using/sso-setup-azure.html)

**其他SAML IdP** - [與其他SAML提供者設定SSO](https://helpx.adobe.com/enterprise/using/create-directory.html)

**Google** （建議） - [使用Google Connector設定SSO和使用者同步](https://helpx.adobe.com/enterprise/using/setup-sso-google.html)

## 管理現有SSO設定

在您的組織和Adobe之間設定SSO後，使用下列專案管理和變更您的設定。

瞭解如何管理您的網域和目錄：

- [管理使用者](https://helpx.adobe.com/tw/enterprise/using/users.html)和[群組](https://helpx.adobe.com/enterprise/using/user-groups..html)
- [將網域連結至目錄](https://helpx.adobe.com/enterprise/using/add-domains-directories.html#link-domains-to-directoies)以控制使用者對應用程式、服務和設定的存取
- [管理目錄信任](https://helpx.adobe.com/enterprise/using/directory-trust.html)以使用其他組織宣告的網域

瞭解如何變更您的身分提供者：

- [變更IdP](https://helpx.adobe.com/enterprise/using/migrate-authentication-provider.html)而不中斷使用者的工作
- [跨目錄移動網域](https://helpx.adobe.com/enterprise/using/manage-domains-directories.html#move-domains-across-directories)
- [移除舊版目錄使用者](https://helpx.adobe.com/enterprise/using/manage-directory-users.html)
- [刪除舊/無人認領的網域和空白目錄](https://helpx.adobe.com/enterprise/using/manage-domains-directories.html#delete)

## 錯誤和常見問題

設定和管理SSO時常見問題和錯誤的解決方案：

### Azure AD — 常見問題集和疑難排解

#### 常見問題集

- [Azure AD聯結器常見問題集](https://helpx.adobe.com/enterprise/using/azure-ad-connector-faq.html)
- [如何刪除目錄和網域](https://helpx.adobe.com/enterprise/using/sso-setup-azure.html#Deletedirectoriesandremovedomains)

#### 疑難排解

- [拒絕存取的使用者](https://helpx.adobe.com/enterprise/using/sso-setup-azure.html#sync-issues)
- [同步處理問題](https://helpx.adobe.com/enterprise/using/sso-setup-azure.html#sync-issues)

### 其他SAML IdP — 常見問題集和疑難排解

#### 常見問題集

[SAML整合常見問題集](https://helpx.adobe.com/enterprise/using/sso-faq.html)

#### 疑難排解

- [一般SSO疑難排解](https://helpx.adobe.com/enterprise/kb/tshoot-fed-id.html)
- [「拒絕存取」錯誤](https://helpx.adobe.com/enterprise/kb/tshoot-fed-id.html#Error_Access_Denied_logging_in)
- [「另一個使用者目前登入」錯誤](https://helpx.adobe.com/enterprise/kb/tshoot-fed-id.html#ErrorAnotheruseriscurrentlyloggedin)
- [執行SAML追蹤](https://helpx.adobe.com/enterprise/kb/perform-a-saml-trace.html)

### Google — 常見問題集

- [Google聯結器常見問題集](https://helpx.adobe.com/enterprise/using/google-federation-faq.html)
- [如何刪除目錄和網域](https://helpx.adobe.com/enterprise/using/setup-sso-google.html#Deletedirectoriesandremovedomains)

## 加入交談

若要共同作業、提出問題並與其他管理員交談，請使用[企業和Teams社群](https://www.adobe.com/go/entcom)。

## 法律與隱私權

- [法律注意事項](https://helpx.adobe.com/legal/legal-notices.html)
- [線上隱私權原則](https://www.adobe.com/tw/privacy.html)
