---
title: 使用Global Admin Console將產品配置給子組織
description: 瞭解全域管理員如何分配資源給下階組織，以啟用每個組織內有效的資源管理和使用者指派。
Feature-set: Experience Cloud Services
Solution: Admin Console
Feature: Admin Console
exl-id: de6e785d-8965-40d5-ac78-7fbb2cd7afc7
source-git-commit: f14254a77ce3620208389b36222f89be8f9d15b6
workflow-type: tm+mt
source-wordcount: '1050'
ht-degree: 0%

---

# 使用Global Admin Console將產品配置給子組織

適用於企業。

瞭解全域管理員如何分配資源給下階組織，以啟用每個組織內有效的資源管理和使用者指派。

在[Global Admin Console](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/adopt-global-administration)中，移至&#x200B;**[!UICONTROL 產品配置]**&#x200B;標籤，然後選取要配置給子組織的產品。

登入[Global Admin Console](https://global-admin-console.adobe.com)。

>[!NOTE]
>
>**[!UICONTROL 產品配置]**&#x200B;僅適用於企業授權合約(ETLA)合約。

在跨組織分配和管理Adobe產品時，會將購買的資源分割為跨要管理的組織的資源配置。 您可以指定全部或部分資源，將產品資源的管理分給其他組織。 並非所有產品的所有資源都可配置；部分產品不可分配給其他組織。 這類產品會顯示在&#x200B;**[!UICONTROL 產品配置]**&#x200B;索引標籤中，但沒有可新增至其他組織的控制項。

>[!WARNING]
>
>您無法從具有&#x200B;**過期**&#x200B;的合約或組織處於&#x200B;**非作用中**&#x200B;狀態的子組織，配置產品給子組織。 深入瞭解[合約到期日](https://helpx.adobe.com/enterprise/using/contract-expiry.html)，或連絡您公司的管理員以取得協助，避免子組織中的使用者無法存取其Adobe應用程式和服務。

## 集區儲存空間

這適用於在其Admin Console中具有「儲存」索引標籤的客戶。 如果您沒有看到儲存體索引標籤，表示您的Admin Console尚未更新至企業儲存模式。 您的組織移轉後，您將會看到下列變更：

- 全域管理員可存取整個階層的儲存配額和使用量，並可使用&#x200B;**[!UICONTROL Global Admin Console]**&#x200B;中的[產品配置](https://adminconsole.adobe.com/)索引標籤，將儲存空間配置給組織。
- 系統管理員和儲存管理員可完整掌控並掌握整個組織的儲存作業。 他們可以使用&#x200B;**[!UICONTROL Adobe Admin Console]**&#x200B;中的[儲存體](https://adminconsole.adobe.com/)索引標籤來追蹤及管理儲存體。

隨著Adobe Creative Cloud儲存空間的更新，使用者的儲存配額變得靈活，最高可達組織購買的儲存空間。 [了解更多](https://helpx.adobe.com/enterprise/using/manage-adobe-storage.html)。

## 分配產品

Global Admin Console中的&#x200B;**[!UICONTROL 產品配置]**&#x200B;索引標籤會顯示跨組織階層購買之產品的配置單位。 作為[全域管理員](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators#admins)，您可以將這些產品資源配置給組織樹狀結構中的其他組織，並指定配置數量。 作為[全域檢視器](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators#admins)，您可以檢視及匯出資料，但無法進行任何更新。

若要將產品配置給組織，請遵循下列步驟：

1. 登入[Global Admin Console](https://global-admin-console.adobe.com)並移至&#x200B;**[!UICONTROL 產品配置]**。
1. 從下拉式清單中選取產品，以檢視如何將其配置給不同的組織。\
   如果組織目前沒有產品，則會顯示&#x200B;**[!UICONTROL 新增+]**&#x200B;圖示。

   >[ !Note]
   >
   >如果下階組織已有採購合約，則上階組織至該下階組織的產品配置可能會受到限制。 [了解更多](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html#limited-product-allocation)。

1. 若要配置產品，請選取相關組織的&#x200B;**[!UICONTROL 新增+]**&#x200B;圖示。\
   有些產品包含多個可配置的資源；在這種情況下，對話方塊中會列出多個資源，而且您必須為每個資源提供值。 例如，Adobe Stock可包含Adobe Stock影像積分和進階積分。
   ![Adobe Stock影像](/help/adobe-support-tools-guide/assets/adobe-stock-images.png)
1. 在出現的對話方塊中，指定產品數量。
1. 選取「**[!UICONTROL 儲存]**」。
1. 若要允許或不允許過度配置資源，請選取相關的切換。
   ![過度配置](/help/adobe-support-tools-guide/assets/overallocation.png)
1. 完成資源配置後，選取&#x200B;**[!UICONTROL 檢閱擱置的變更]**。 檢閱後，選取&#x200B;**[!UICONTROL 提交變更]**&#x200B;以[執行](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html)它們。

## 分配並分發Adobe Acrobat Sign使用者授權或交易

Global Admin Console可讓您在整個組織階層中配置與分配Acrobat Sign使用者授權或交易。 階層中擁有Acrobat Sign授權或配置給其交易的每個組織都會建立自己的個別Acrobat Sign帳戶。

- 所建立的每個Acrobat Sign帳戶都是獨立的，並在管理和內容方面各自獨立。
- 每個Acrobat Sign帳戶都不知道其他Acrobat Sign帳戶（例如，在上層或姐妹組織中）。

進一步瞭解[在Admin Console中管理Adobe Acrobat Sign](https://helpx.adobe.com/enterprise/using/adobe-sign-for-enterprise.html)。

若要管理知識型驗證(KBA)和電話驗證(PA)等驗證附加元件，請聯絡您的Adobe代表或客戶成功經理。


## 產品配置的限制

在下列情況下，從上階組織到下階組織的配置會受到限制：

- 如果兩個組織擁有不同的合約，且您嘗試配置的產品存在於兩個組織中，則不允許在合約之間混合相同的優惠方案。
- 如果兩個組織擁有相同的合約，您可以連絡您的Adobe代表或[提交支援](https://helpx.adobe.com/enterprise/using/support-for-enterprise.html)案例，指定Global Admin Console中的&#x200B;**[!UICONTROL 產品配置]**&#x200B;已封鎖，以要求配置產品的許可權。

## 過度配置

作為[全域系統管理員](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators#admins)，您可以允許資源過度配置。

與產品及組織關聯的配置[原則](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html#update-policies)指出是否允許過度配置。

過度配置允許將比父組織可用的更多產品資源授與子組織。 當配置近似時，它很有用，並且管理員不想負擔使資源分配相加的負擔。
如果針對組織中的產品資源停用過度配置，則子授權的總和不能超過父授權。 對於標示為已停用過度配置的資源，將不會執行過度配置請求。
當過度配置切換從啟用切換到停用時，如果資源的授權數量中存在過度配置情況，則必須調整授權值以排除過度配置，然後才能執行授權更新。

![過度配置](/help/adobe-support-tools-guide/assets/overallocation.png)

## 階層中過期的合約

您無法從已過期的ETLA合約將產品配置給子組織。 **[!UICONTROL 總覽]**&#x200B;和&#x200B;**[!UICONTROL 產品配置]**&#x200B;頁面上的應用程式內橫幅和通知（例如下列通知）會清楚指出一或多個子組織的合約即將到期、已到期或非作用中。

![產品配置](/help/adobe-support-tools-guide/assets/product-allocation.png)

>[ !I重要]
>
>當屬於階層一部分的ETLA合約停用後，產品就會從&#x200B;**[!UICONTROL 總覽]**&#x200B;和&#x200B;**[!UICONTROL 產品配置]**&#x200B;頁面中移除。

[進一步瞭解合約到期日](https://helpx.adobe.com/enterprise/using/contract-expiry.html)，或連絡您公司的管理員以取得協助，以防止子組織中的使用者無法存取其Adobe應用程式和服務。
