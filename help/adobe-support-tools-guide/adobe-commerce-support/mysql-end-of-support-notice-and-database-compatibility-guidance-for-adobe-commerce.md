---
title: Adobe Commerce的MySQL支援終止通知和資料庫相容性指引
description: 本文提供MySQL支援終止時間表的相關資訊，以及支援Adobe Commerce版本的資料庫相容性指引。
solution: Commerce
source-git-commit: 2198e1882260ca17b8b99f7ed6d415791ec0d177
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 0%

---

# Adobe Commerce的MySQL支援終止通知和資料庫相容性指引

本文提供支援的Adobe Commerce版本的MySQL終止支援(EOS)和資料庫相容性的重要資訊。
Adobe強烈建議商戶檢閱此公告，並採取行動維護平台穩定性及符合支援要求。
進一步瞭解[MariaDB升級必要條件](https://experienceleague.adobe.com/en/docs/commerce-operations/implementation-playbook/best-practices/maintenance/mariadb-upgrade)和[系統需求](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/system-requirements)。

## MySQL 8.0終止支援(EOS)

MySQL 8.0於2026年4月30日終止支援(EOS)。
在此日期之後，下列Adobe Commerce版本將無法支援或維持與MySQL 8.0之後發行的MySQL版本的相容性：

* Adobe Commerce 2.4.7
* Adobe Commerce 2.4.6
* Adobe Commerce 2.4.5

Adobe將不會在這些Adobe Commerce發行版本上驗證或支援較新的MySQL主要版本。

## 內部部署客戶的必要動作

強烈建議執行以下版本的Adobe Commerce內部部署安裝，將其資料庫伺服器移轉至相容的MariaDB版本：

* 2.4.5
* 2.4.6
* 2.4.7

這些版本完全支援MariaDB，並且是日後建議的資料庫平台。

* 2.4.5
* 2.4.6
* 2.4.7

強烈建議將其資料庫伺服器移轉至相容的MariaDB版本。
這些Adobe Commerce版本完全支援MariaDB，因此是建議的資料庫平台。

## Adobe Commerce 2.4.8和2.4.9中的MySQL支援

Adobe Commerce 2.4.8和2.4.9是支援MySQL的最後兩個Adobe Commerce版本。

對於這些版本：
* MySQL 8.4是Adobe Commerce支援的最終MySQL版本。
* Adobe Commerce不會認證或支援8.4之後發行的MySQL版本。

## 未來方向：MariaDB做為預設的資料庫平台

日後，Adobe Commerce會繼續支援MariaDB作為預設和建議的資料庫平台。

Adobe強烈建議下列客戶開始規劃移轉至MariaDB的作業，以維持長期的相容性和支援一致性：
* 所有Adobe Commerce 2.4.8和2.4.9內部部署客戶
* 執行較舊支援Adobe Commerce版本的客戶
