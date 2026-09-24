---
title: 無法將使用者新增至Adobe Commerce雲端專案
description: 本文提供無法新增使用者至Adobe Commerce雲端專案時的解決方案。
feature: Cloud, Paas
solution: Commerce
feature-set: Commerce
role: Developer
exl-id: 2dc52d5e-0930-48c4-986e-ce3f9f6f8221
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: 5a951749-fac9-5bc7-9a98-ebe4ff066437
    internal-label: Cloud
  - id: 00451af3-7b97-5414-9992-3a6c269e413f
    internal-label: Paas
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: a4ba265c36bd4ba6c7c563879834f2c59fdc58a4
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 0%
---
# 無法將使用者新增至Adobe Commerce雲端專案

本文提供當您嘗試將使用者新增至雲端專案時的解決方案，但失敗並出現錯誤： *使用者XXX不存在*。

## 受影響的產品和版本

* 雲端基礎結構上的Adobe Commerce，[所有支援的版本](https://magento.com/sites/default/files/magento-software-lifecycle-policy.pdf)

## 問題

本文提供無法新增使用者至Adobe Commerce雲端專案時的解決方案。

## 原因

使用者的帳戶必須先在[https://accounts.magento.cloud](https://accounts.magento.cloud)建立並連結至其Adobe SSO，才能將其新增為專案的使用者。 如果使用者有Adobe帳戶，但沒有Commerce (magento.com)帳戶，則必須先建立帳戶。

## 解決方案

1. 要求使用者在[https://accounts.magento.cloud](https://accounts.magento.cloud)登入。 使用者必須使用相同的電子郵件地址向Adobe註冊。
   >[!NOTE]
   >在[https://account.adobe.com](https://account.adobe.com)建立或擁有帳戶，並不自動錶示使用者在[https://accounts.magento.cloud](https://accounts.magento.cloud)擁有帳戶。 使用者必須先建立[其Commerce帳戶](https://experienceleague.adobe.com/zh-hant/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account)。

1. 如果使用者已有Adobe帳戶但無法登入，請要求他們提交[支援要求](https://experienceleague.adobe.com/home?lang=zh-Hant#support)，並將[!UICONTROL 問題原因]設定為&#x200B;*使用者管理*。

1. 使用者成功登入[https://accounts.magento.cloud](https://accounts.magento.cloud)後，您可以將使用者新增至專案。 如需詳細步驟，請參閱Commerce on Cloud Infrastructure指南中的[新增使用者及管理存取權](https://experienceleague.adobe.com/zh-hant/docs/commerce-cloud-service/user-guide/project/user-access#add-users-and-manage-access)。

## 相關閱讀：

* 在雲端基礎結構的Commerce指南中[管理使用者存取](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html?lang=zh-Hant)。
* [無法登入Adobe Commerce支援或雲端帳戶](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/unable-to-log-in-to-support-or-cloud-project.html?lang=zh-Hant)
