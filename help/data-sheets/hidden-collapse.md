---
title: 摺疊區段錯誤
description: UGP-13446可摺疊區段無法呈現，可能是因為嵌入了頁面索引標籤
hide: true
hidefromtoc: true
source-git-commit: f2d8eb9125df5f542c1ed075348586965f4adaad
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 7%

---

# 可摺疊區段

<http://jira.corp.adobe.com/browse/UGP-13446> UGP-13446可摺疊區段無法呈現，可能是因為嵌入了頁面索引標籤

## 範例

第一個具有頁面索引標籤；第二個沒有

### 選項2：搭配頁面索引標籤

+++ 手動安裝6.5.18.0 - 6.5.22.0的Hotfix

**步驟1：下載並解壓縮Hotfix套件**

- 從Adobe軟體發佈入口網站下載[ - 6.5.226.5.18.0的](https://www.adobe.com/tw/)Hotfix
- 在本機擷取

**步驟2：瀏覽至正確的版本資料夾**

- 根據環境中安裝的Service Pack版本，前往相符的資料夾。

  例如，Service Pack 20的資料夾為：

  ```
  <extracted-hotfix>/SP20/
  ```

**步驟3：找到部署目錄**

- 在JEE伺服器上的AEM Forms上，前往：

  ```
  [AEM installation directory]/deploy
  ```

  範例：`adobe/adobe-experience-manager-forms/deploy`



**步驟4：更新並取代EAR檔案**

>[!BEGINTABS]

>[!TAB JBoss]

1. 開啟`adobe-core-jboss.ear`並將`adminui.war`取代為

   ```
   adobe-xxe-configuration-hotfix/SP[version]/jboss/adminui.war
   ```

   例如, `adobe-xxe-configuration-hotfix/SP20/jboss/adminui.war`

1. 在`adobe-core-jboss.ear`內，移至`lib/`資料夾並將`adobe-uisupport.jar`取代為：

   ```
   adobe-xxe-configuration-hotfix/SP[version]/adobe-uisupport.jar
   ```

   例如, `adobe-xxe-configuration-hotfix/SP20/adobe-uisupport.jar`

1. 儲存EAR。 確保變更已正確儲存。


1. 將`adobe-edcserver-jboss.ear`取代為

   ```
   adobe-xxe-configuration-hotfix/SP[version]/jboss/adobe-edcserver-jboss.ear
   ```

   例如, `adobe-xxe-configuration-hotfix/SP20/jboss/adobe-edcserver-jboss.ear`

1. 將`adobe-forms-jboss.ear`取代為

   ```
   adobe-xxe-configuration-hotfix/SP[version]/jboss/adobe-forms-jboss.ear
   ```

   例如, `adobe-xxe-configuration-hotfix/SP20/jboss/adobe-forms-jboss.ear`



>[!TAB WebLogic]

1. 開啟`adobe-core-weblogic.ear`並將`adminui.war`取代為

   ```
   adobe-xxe-configuration-hotfix/SP[version]/weblogic/adminui.war
   ```

   例如, `adobe-xxe-configuration-hotfix/SP20/weblogic/adminui.war`

1. 在`adobe-core-weblogic.ear`內，將`adobe-uisupport.jar`取代為：

   ```
   adobe-xxe-configuration-hotfix/SP[version]/adobe-uisupport.jar
   ```

   例如, `adobe-xxe-configuration-hotfix/SP20/adobe-uisupport.jar`

1. 儲存EAR。 確保變更已正確儲存。


1. 將`adobe-edcserver-weblogic.ear`取代為

   ```
   adobe-xxe-configuration-hotfix/SP[version]/weblogic/adobe-edcserver-weblogic.ear
   ```

   例如, `adobe-xxe-configuration-hotfix/SP20/weblogic/adobe-edcserver-weblogic.ear`

1. 將`adobe-forms-weblogic.ear`取代為

   ```
   adobe-xxe-configuration-hotfix/SP[version]/weblogic/adobe-forms-weblogic.ear
   ```

   例如, `adobe-xxe-configuration-hotfix/SP20/weblogic/adobe-forms-weblogic.ear`

>[!TAB WebSphere]

1. 開啟`adobe-core-websphere.ear`並將`adminui.war`取代為

   ```
   adobe-xxe-configuration-hotfix/SP[version]/websphere/adminui.war
   ```

   例如, `adobe-xxe-configuration-hotfix/SP20/websphere/adminui.war`

1. 在`adobe-core-websphere.ear`內，將`adobe-uisupport.jar`取代為：

   ```
   adobe-xxe-configuration-hotfix/SP[version]/adobe-uisupport.jar
   ```

   例如, `adobe-xxe-configuration-hotfix/SP20/adobe-uisupport.jar`

1. 儲存EAR。 確保變更已正確儲存。


1. 將`adobe-edcserver-websphere.ear`取代為

   ```
   adobe-xxe-configuration-hotfix/SP[version]/websphere/adobe-edcserver-websphere.ear
   ```

   例如, `adobe-xxe-configuration-hotfix/SP20/websphere/adobe-edcserver-websphere.ear`

1. 將`adobe-forms-websphere.ear`取代為

   ```
   adobe-xxe-configuration-hotfix/SP[version]/websphere/adobe-forms-websphere.ear
   ```

   例如, `adobe-xxe-configuration-hotfix/SP20/websphere/adobe-forms-websphere.ear`

>[!ENDTABS]



**步驟5：使用`adobe-rightsmanagement-<appserver>-dsc.jar`更新**&#x200B;檔案

```
adobe-xxe-configuration-hotfix/SP[version]/<appserver>/adobe-rightsmanagement-<appserver>-dsc.jar
```

例如, `adobe-xxe-configuration-hotfix/SP20/jboss/adobe-rightsmanagement-jboss-dsc.jar`

**步驟6： WebSphere和WebLogic上Document Security的其他設定**：

如果您使用Document Security (前身為Rights Management)，請在啟動AEM Forms伺服器前設定下列Java系統屬性（JVM引數）：

```
-Dcom.adobe.forms.jee.services.allowDoctypeDeclaration=true
```


**步驟7：重新執行組態管理員**

- 啟動Configuration Manager以重新部署更新的EAR並套用Hotfix

+++

### 選項2：沒有頁面索引標籤

+++ 手動安裝6.5.18.0 - 6.5.22.0的Hotfix

**步驟1：下載並解壓縮Hotfix套件**

- 從Adobe軟體發佈入口網站下載[ - 6.5.226.5.18.0的](https://www.adobe.com/tw/)Hotfix
- 在本機擷取

**步驟2：瀏覽至正確的版本資料夾**

- 根據環境中安裝的Service Pack版本，前往相符的資料夾。

  例如，Service Pack 20的資料夾為：

  ```
  <extracted-hotfix>/SP20/
  ```

**步驟3：找到部署目錄**

- 在JEE伺服器上的AEM Forms上，前往：

  ```
  [AEM installation directory]/deploy
  ```

  範例：`adobe/adobe-experience-manager-forms/deploy`



**步驟4：更新並取代EAR檔案**

頁面索引標籤已刪除

**步驟5：使用`adobe-rightsmanagement-<appserver>-dsc.jar`更新**&#x200B;檔案

```
adobe-xxe-configuration-hotfix/SP[version]/<appserver>/adobe-rightsmanagement-<appserver>-dsc.jar
```

例如, `adobe-xxe-configuration-hotfix/SP20/jboss/adobe-rightsmanagement-jboss-dsc.jar`

**步驟6： WebSphere和WebLogic上Document Security的其他設定**：

如果您使用Document Security (前身為Rights Management)，請在啟動AEM Forms伺服器前設定下列Java系統屬性（JVM引數）：

```
-Dcom.adobe.forms.jee.services.allowDoctypeDeclaration=true
```


**步驟7：重新執行組態管理員**

- 啟動Configuration Manager以重新部署更新的EAR並套用Hotfix

+++

Fin
