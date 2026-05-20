---
title: 如何取得並套用[!UICONTROL 安全性修補程式]
description: 本文提供如何取得及套用已發行的[!UICONTROL 安全性修補程式]的指示，但無法取得指示。
exl-id: 6764d60e-5088-4a85-90fa-4372570b065b
source-git-commit: 9a4d96e06b949e4c229fdf0f084810b27bf8b346
workflow-type: tm+mt
source-wordcount: '660'
ht-degree: 0%

---

# 如何取得並套用[!UICONTROL 安全性修補程式]

>[!NOTE]
>如果您有內部部署安裝，而且未使用[!DNL CVS]或GitHub等版本控制系統來管理您的程式碼，您的Web主機或許可以協助套用修補程式。 歡迎聯絡他們以尋求支援。

本文提供如何取得及套用已發行的[!UICONTROL 安全性修補程式]的指示，但無法取得指示。

## 受影響的產品和版本

Adobe Commerce內部部署和雲端基礎結構 — 所有支援的版本


## 原因

針對Adobe Commerce安全性公告，Adobe只會在公告中明確發行成品時，提供個別的隔離修補程式檔案或Hotfix。 如果公告資料中未發佈或參考任何獨立的修補程式或Hotfix，Adobe之後就不會建立獨立的修補程式。

這是因為安全性修正是作為適用版本行的支援安全性版本的一部分一起設計、驗證和發行的。

因此，支援的修正路徑是為受影響的版本行套用官方安全更新，或升級至已包含該修正的版本。

## 解決方案


### 案例I：

* 如果[發行說明](https://experienceleague.adobe.com/zh-hant/docs/commerce-on-cloud/user-guide/release-notes/cloud-tools-suite)中提及隔離的修補程式檔案/Hotfix，請從[https://account.magento.com](https://account.magento.com/downloads/view/)的下載區段下載檔案。 共用存取許可權的使用者必須先獲得帳戶擁有者/授權持有者的下載許可權。

**警告：**

* Adobe Commerce 2.4.6在2027年8月30日前仍受延長支援支援。

* Adobe Commerce 2.4.5在2026年8月11日之前仍維持在延長支援下。 在此日期之後，Adobe僅提供到2027年5月31日的安全修正。

* Adobe Commerce 2.4.4不再提供延伸支援。 Adobe僅針對2027年5月31日之前提供安全性修正。

* 對於Adobe Commerce 2.4.4和2.4.5，Adobe僅提供安全性修補程式檔案。 這些更新不包括：

   * Adobe Commerce支援或工程協助
   * 品質修補程式
   * 平台或作業系統相依性更新

不支援的版本（2.3.x和2.4.0-2.4.3）不符合支援資格。 您可以升級至支援的版本，以接收最新的安全性修正。

### 案例II：

隔離的修補程式僅於例外情況下提供，並非實作安全性修正的推薦方法。

如果發行說明中未提及隔離的修補程式檔案或Hotfix，請遵循下列准則：

>[!IMPORTANT]
>
>如果隔離的修補程式檔案或Hotfix未明確針對安全性問題發行，請將完整的Adobe Commerce應用程式升級至受影響發行版本的最新適用修補程式版本。

**雲端：**

1. 在適用於Commerce的雲端修補程式底下，某些[!UICONTROL 安全性修補程式]可能包含在最新版的Cloud Tools Suite (ECE Tools)中/發行 — 請檢視[發行說明](https://experienceleague.adobe.com/zh-hant/docs/commerce-cloud-service/user-guide/release-notes/cloud-tools-suite)，如果發行版本中提到安全性修正，請將套件升級至該版本。
1. 如果發行說明未提及安全性修正，請繼續閱讀。

**雲端基礎結構或內部部署：**

* 如果無法使用隔離的修補程式檔案/Hotfix，[請將雲端基礎結構上的Adobe Commerce版本](https://experienceleague.adobe.com/zh-hant/docs/commerce-cloud-service/user-guide/develop/upgrade/commerce-version) 2.4.X升級至最新的修補程式版本2.4.X-pY。
* 如果無法使用隔離的修補程式檔案/Hotfix，[請將Adobe Commerce Version On-Premise](https://experienceleague.adobe.com/zh-hant/docs/commerce-operations/upgrade-guide/implementation/perform-upgrade) 2.4.X升級至最新的修補程式版本2.4.X-pY。

## 相關閱讀

* 請參閱&#x200B;*雲端基礎結構上的Commerce Cloud指南*&#x200B;中的[Adobe Commerce Tools Suite](https://experienceleague.adobe.com/zh-hant/docs/commerce-cloud-service/user-guide/release-notes/cloud-tools-suite)發行說明。
* 請參閱&#x200B;*雲端基礎結構指南上的Adobe Commerce*&#x200B;中的[升級Adobe Commerce版本](https://experienceleague.adobe.com/zh-hant/docs/commerce-cloud-service/user-guide/develop/upgrade/commerce-version)。
