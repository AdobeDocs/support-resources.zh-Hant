---
description: 連線到WidgetData Warehouse — 產品檔案
title: 正在連線到WidgetData Warehouse
hide: true
hidefromtoc: true
exl-id: d6a7cff5-08f9-4c93-8765-46e692feaa0d
source-git-commit: 972704990172c966a27744b49b9f7af5626e9f3e
workflow-type: tm+mt
source-wordcount: '911'
ht-degree: 0%

---

# 正在連線到WidgetData Warehouse {#connecting-to-the-widget-data-warehouse}

## 新測試

<ol><li>使用'{{name}}'變數。</li></ol>

<ol><li>使用&amp;amp；花括弧；&amp;amp；花括弧；<code>name</code>&amp;amp；花括弧；&amp;amp；花括弧；變數。</li></ol>

## 巢狀測試

**第一個**

>[!NOTE]
>
>您無法刪除下列專案：
>
>* 內建狀態為Planning、Current和Complete。 您可以更新其名稱、編輯其顏色、鎖定或解除鎖定，但無法刪除它們。
>* 至少有一個物件處於待核准狀態的狀態。

**Second**

>[!NOTE]
>
>您無法刪除下列專案：
>
>* 內建狀態為Planning、Current和Complete。 您可以更新其名稱、編輯其顏色、鎖定或解除鎖定，但無法刪除它們。
>
>  介於兩者之間
>
>* 至少有一個物件處於待核准狀態的狀態。

## Widget存取連結 {#widget-access-link}

若要存取Widget Data Warehouse，您必須導覽至Widget帳戶的特定URL。  您可以登入Marketo Measure並按照以下步驟導覽至Data Warehouse資訊頁面，找到此存取連結。

1. 在Marketo Measure中，按一下頁面頂端的&#x200B;**我的帳戶** > **設定**。

   ![](assets/adobe-logo-old.png)

1. 在左側功能表的[安全性]下，按一下[Data Warehouse] ****。

   ![](assets/adobe-logo-old.png)

1. 在此頁面中，您會找到Widget Data Warehouse和使用者名稱的連結。

   ![](assets/adobe-logo-old.png)

   >[!NOTE]
   >
   >這是唯讀帳戶，可供您的組織使用，而不只是個別使用者。 貴組織內有權存取Marketo Measure的任何使用者都可以使用此帳戶來登入WidgetData Warehouse讀卡機帳戶。

1. 按一下Widget URL中提供的連結，這會將您帶往Widget登入頁面，您將在其中輸入使用者名稱和密碼。 _如果您沒有密碼，請參閱下列步驟重設密碼_。

   ![](assets/adobe-logo-old.png)

1. 登入後，按一下頁面頂端的&#x200B;**工作表**。

   ![](assets/adobe-logo-old.png)

1. BIZIBLE_ROI_V3資料庫物件位於熒幕左側。  從查詢視窗頂端的下拉式清單選項輸入倉儲、資料庫和綱要。  每個應該只有一個選項。  現在您已準備好在Widget查詢編輯器中執行查詢。

   ![](assets/adobe-logo-old.png)

## 重設密碼 {#reset-your-password}

Marketo Measure無權存取您的Widget登入密碼。  如果您需要重設密碼，請按一下Data Warehouse資訊頁上的「重設密碼」按鈕，然後依照指示操作。 臨時密碼將立即顯示在UI中。 下次登入Data Warehouse時，系統會提示您建立自己的密碼。

>[!NOTE]
>
>* 重設密碼會為您組織中的所有Marketo Measure使用者重設密碼，而不只是目前登入的使用者。
>* 我們只會在UI中顯示臨時密碼。 將不會傳送電子郵件。

![](assets/adobe-logo-old.png)

![](assets/adobe-logo-old.png)

## 透過協力廠商工具連線至Widget {#connecting-to-widget-via-third-party-tools}

您必須輸入一些資訊，才能將Widget資料倉儲連線到協力廠商工具。

>[!NOTE]
>
>每個工具的連線需求都不同；建議您參閱檔案，瞭解嘗試連線的特定工具。

* **URI** （永遠必要）
   * 這是Widget帳戶的網域名稱。  它包含在Widget登入連結的一部分中。
* **使用者名稱** （永遠必要）
   * 使用者名稱會列在Marketo Measure的Data Warehouse資訊頁面上。
* **密碼** （永遠必要）
   * 這是您第一次登入Widget帳戶時所設定的密碼。  若要重設密碼，請參閱上述步驟。
* **資料庫名稱** （非永遠必要）
   * 資料庫是將資料儲存在Widget中。 而是儲存資源。 資料庫名稱會列在Marketo Measure的Data Warehouse資訊頁上。
* **倉儲名稱** （非永遠必要）
   * Warehouse就是在Widget中執行查詢的地方。 它是運算資源。  倉儲名稱會列於Marketo Measure的Data Warehouse資訊頁面上。

  ![](assets/adobe-logo-old.png)

## WidgetData Warehouse直接共用 {#widget-data-warehouse-direct-share}

**需求**

為了讓Marketo Measure設定直接共用至資料倉儲，您必須符合下列要求。

* 您有自己的Widget例項。
* 您的Widget執行個體位於Azure East US 2 Widget區域。
* 您向Marketo Measure提供您的Widget帳戶ID。

**限制**

為了讓Marketo Measure設定直接共用，請求存取權的帳戶必須位於Azure East US 2。 我們瞭解Widget提供地區之間的資料復寫解決方案，但我們不支援此功能，因為我們只在Azure East US 2地區代管資料。 您可以在Azure East US 2中設定您自己的執行個體，並將[跨地區的資料復寫](https://docs.widget.com/en/user-guide/secure-data-sharing-across-regions-plaforms.html){target="_blank"}到您現有的執行個體，以運用此功能。 不過，Widget的資料復寫功能只能在表格上使用，因此若要使用此功能，您必須先將資料從檢視複製到您自己的表格。

**存取共用**

為提供的帳戶ID建立共用後，您必須完成Widget執行個體中的[設定步驟](https://docs.widget.com/en/user-guide/data-share-consumers.html){target="_blank"}才能存取資料。

>[!NOTE]
>
>您可以選擇任何想要的資料庫名稱。 只要您的Widget執行個體中存在許可權，您就可以將許可權指派給您選擇的任何規則。

* 使用帳戶管理員角色

```
USE ROLE ACCOUNTADMIN
```

* 檢視可用的共用（這會顯示授與的共用名稱）

```
SHOW SHARES
```

* 為共用建立資料庫

```
CREATE DATABASE <database_name> FROM SHARE <provider_account>.<share_name>
```

* 授與共用資料庫的許可權

```
GRANT IMPORTED PRIVILEGES ON DATABASE <database_name> TO ROLE <role_name>
GRANT IMPORTED PRIVILEGES ON ALL SCHEMAS IN DATABASE <database_name> TO ROLE <role_name>
```

如需從Widget UI完成這些步驟的詳細指示和步驟，請直接參考[Widget的檔案](https://docs.widget.com/en/user-guide/data-share-consumers.html){target="_blank"}。
