---
title: 在Global Admin Console中管理產品設定檔
description: 瞭解全域管理員如何在Global Admin Console中新增、編輯和刪除產品設定檔。
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
product_v2: id: f7bdf6be-dd3b-4d2d-ac52-0e62ed0d3102
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 011223f71c06bcc17f669751ee8b12c81c52436f
workflow-type: tm+mt
source-wordcount: 580
ht-degree: 1%

---

# 在Global Admin Console中管理產品設定檔

> **套用至：**&#x200B;企業


## 概觀

全域管理員可以在[Global Admin Console](https://global-admin-console.adobe.com/)中新增、編輯和刪除產品設定檔。

>[!NOTE]
>
>在[Global Admin Console](https://helpx.adobe.com/enterprise/global-admin-console/adopt-global-administration.html#request-access)中，選取組織並導覽至&#x200B;**[!UICONTROL 產品]**。 您可以使用產品設定檔來啟用產品的所有或選取的服務。

如同在標準Admin Console中，產品設定檔可讓您微調組織內產品的使用方式。 您也可以將管理員（稱為&#x200B;**[!UICONTROL 產品設定檔管理員]**）指派給產品設定檔。 這些管理員可以將一般使用者新增到他們管理的產品設定檔。

若要管理產品設定檔，請選取產品。 將會顯示新增、編輯和刪除產品設定檔的控制項。

>[!NOTE]
>
>對於某些產品，您無法在Global Admin Console中建立或編輯產品設定檔。 在這種情況下，請改用[Admin Console](https://helpx.adobe.com/tw/enterprise/using/admin-console.html)。

## 新增產品設定檔

1. 在[Global Admin Console](https://global-admin-console.adobe.com/)中，選取要編輯的組織，然後導覽至&#x200B;**[!UICONTROL 產品]**&#x200B;索引標籤。
1. 選取要新增產品設定檔的產品。
1. 選取&#x200B;**[!UICONTROL 新增設定檔]**。
1. 在&#x200B;**[!UICONTROL 新增設定檔]**&#x200B;對話方塊中，輸入下列詳細資料：

   | 欄位 | 說明 |
   |---|---|
   | **[!UICONTROL 名稱]** | 組織內產品設定檔的唯一名稱，與其他產品設定檔和使用者群組不同。 |
   | **[!UICONTROL 配額]** | 為此設定檔分配的目標授權數量。 |
   | **[!UICONTROL 使用者群組]** | 從下拉式清單中選取，或輸入使用者群組名稱。 如果使用者群組尚未存在，請先透過[**[!UICONTROL 使用者群組&#x200B;]**](https://helpx.adobe.com/enterprise/global-admin-console/manage-user-groups.html)索引標籤建立它。 |
   | **[!UICONTROL 管理員]** | 從下拉式清單中選取，或輸入管理員的電子郵件地址。 如果管理員尚未存在，請先透過[**[!UICONTROL 管理員&#x200B;]**](https://helpx.adobe.com/enterprise/global-admin-console/manage-administrators.html)索引標籤建立他們。 |

   指定的[!UICONTROL 使用者群組]已指派產品設定檔。 指定的管理員會成為&#x200B;**[!UICONTROL 產品設定檔管理員]**，可以透過Adobe Admin Console管理相關組織的設定檔。

   ![新增設定檔](./assets/manage-product-profiles_add-profile.png)

1. 使用&#x200B;**[!UICONTROL 通知]**&#x200B;切換來啟用或停用電子郵件通知。 啟用後，當使用者新增到設定檔或從中移除時，會收到電子郵件通知。
1. 使用個別&#x200B;**[!UICONTROL 服務]**&#x200B;切換來啟用或停用產品設定檔的特定服務。 如需詳細資訊，請參閱[啟用/停用產品設定檔的服務](https://helpx.adobe.com/enterprise/using/enable-disable-services.html)。
1. 選取「**[!UICONTROL 儲存]**」。
1. 完成編輯組織後，請選取&#x200B;**[!UICONTROL 檢閱擱置的變更]**。 檢閱後，選取&#x200B;**[!UICONTROL 提交變更]**&#x200B;以[執行](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html)它們。

## 編輯產品設定檔

1. 選取要編輯的組織，導覽至「**[!UICONTROL 產品]**」標籤，然後選取產品。
1. 選取相關產品設定檔的&#x200B;**[!UICONTROL 更多選項]** ![更多選項](./assets/manage-product-profiles_more-options.png)圖示，然後選取&#x200B;**[!UICONTROL 編輯設定檔]**。
1. 視需要更新產品設定檔詳細資料，並選取&#x200B;**[!UICONTROL 儲存]**。
1. 完成編輯組織後，請選取&#x200B;**[!UICONTROL 檢閱擱置的變更]**。 檢閱後，選取&#x200B;**[!UICONTROL 提交變更]**&#x200B;以[執行](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html)它們。

## 刪除產品設定檔

>[!WARNING]
>
> 刪除產品設定檔會移除身為該設定檔成員，或屬於附加至該設定檔之使用者群組的所有使用者的產品存取權。

1. 選取要編輯的組織，導覽至「**[!UICONTROL 產品]**」標籤，然後選取產品。
1. 選取相關產品設定檔的&#x200B;**[!UICONTROL 更多選項]** ![更多選項](./assets/manage-product-profiles_more-options.png)圖示，然後選取&#x200B;**[!UICONTROL 刪除設定檔]**。
1. 在確認對話方塊中選取&#x200B;**[!UICONTROL 確定]**。
1. 完成編輯組織後，請選取&#x200B;**[!UICONTROL 檢閱擱置的變更]**。 檢閱後，選取&#x200B;**[!UICONTROL 提交變更]**&#x200B;以[執行](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html)它們。


## 相關閱讀

- [採用全域管理](https://helpx.adobe.com/enterprise/global-admin-console/adopt-global-administration.html)
- [管理管理員](https://helpx.adobe.com/enterprise/global-admin-console/manage-administrators.html)
- [管理使用者群組](https://helpx.adobe.com/enterprise/global-admin-console/manage-user-groups.html)
- [配置產品給子組織](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html)
- [執行擱置中的工作](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html)
- [啟用/停用服務](https://helpx.adobe.com/enterprise/using/enable-disable-services.html)
- [Admin Console概觀](https://helpx.adobe.com/tw/enterprise/using/admin-console.html)
