---
title: 依IP位址限制產品存取
description: 使用IP型存取來控制使用者對Adobe產品的存取，並將使用限制在核准的公用IP範圍。
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
exl-id: e4595040-3930-48af-9888-cf1349596c77
source-git-commit: d5f0473b100cda574b4980e6c871a9c275f9f95a
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 0%

---

# 依IP位址限制產品存取

適用於企業。

使用IP型存取控制使用者對Adobe產品的存取，並防止未列出的公開IP位址出現未經授權的使用。

移至[Admin Console](https://adminconsole.adobe.com/settings/identity)，將受信任的公用IP位址新增至&#x200B;**以IP為基礎的存取**&#x200B;允許清單，以安全地使用Adobe應用程式和服務。

## IP型存取的優點

IP型存取控制使用IP位址允許清單，來限制從隨機公用IP位址使用Adobe產品。 IP型存取適用於您Adobe Admin Console中的所有目錄和相關產品。

您可以將信任的公用IP新增至&#x200B;**允許的IP位址**&#x200B;清單，以停止使用者：

- 從允許的IP範圍以外的公用IP存取產品
- 從允許的IP範圍外的公用IP登入Adobe [使用者設定檔](https://helpx.adobe.com/tw/enterprise/using/manage-adobe-profiles.html)
- 在允許的IP範圍以外的網頁應用程式上切換使用者設定檔

  ![匯出組織結構](./assets/ip-based-access.avif)

## 啟用IP型存取

### 重要考量

>[!IMPORTANT]
>
>- 管理員必須先新增自己的公用IP位址，然後才可新增其他IP範圍。 否則，您可能會遇到錯誤。
>- IP型存取不適用於私人IP位址。

您只能以CIDR格式新增最多150個不同的公用IP範圍。

請依照下列步驟，在您的Adobe Admin Console中啟用IP型存取：

1. 移至&#x200B;**[Adobe Admin Console設定](https://adminconsole.adobe.com/settings/identity)**&#x200B;區段。
2. 選取並展開選取功能表中的&#x200B;**[!UICONTROL 隱私權與安全性]**，然後選取&#x200B;**[!UICONTROL 驗證設定]**。
3. 在&#x200B;**[!UICONTROL IP型存取]**&#x200B;區段中，選取&#x200B;**[!UICONTROL 新增IP位址]**&#x200B;按鈕。
4. 在&#x200B;**[!UICONTROL 新增IP位址]**&#x200B;視窗中：
   - 輸入公用IP位址或CIDR區塊，以新增至您的允許清單。
   - 請使用逗號來分隔多個IP位址。
   - 選取「**[!UICONTROL 儲存]**」。

   目前僅支援IPv4格式。 以下是一些範例：
   - IP v4位址： 1.3.4.6
   - IP v4子網路位址： 1.2.0.0/24

您的IP位址會在幾分鐘內新增。 關聯的使用者下次嘗試登入或在允許的公用IP位址之外切換設定檔時，將會看到限制。 我們建議您事先通知使用者這項變更。

您可以選取每個專案旁的編輯或刪除選項，編輯或移除任何列出的IP位址。

>[!NOTE]
>
>- 啟用IP型存取時，**不會發生強制登出**。 只有當使用者嘗試在登入或切換網頁上的設定檔時選取受限的設定檔時，才會受到影響。
>- 如果您使用安全的網頁閘道，請確定所有流量都透過該閘道進行路由。 檢視允許[網域清單](https://helpx.adobe.com/tw/enterprise/kb/network-endpoints.html)，讓Adobe應用程式和服務正常運作。
>- 如果您因輸入無效的IP位址而被鎖定在Admin Console之外，請連絡[Adobe客戶服務](https://helpx.adobe.com/tw/enterprise/using/support-for-enterprise.html)。

## 加入交談

若要共同作業、提出問題並與其他管理員交談，請造訪我們的[企業與Teams社群](https://www.adobe.com/go/entcom_tw)。
