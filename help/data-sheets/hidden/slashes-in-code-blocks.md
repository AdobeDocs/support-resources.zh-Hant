---
title: 程式碼區塊中的斜線UGP-11189
description: 程式碼區塊中的斜線UGP-11189測試
hide: true
hidefromtoc: true
source-git-commit: 2255dad674f1b4d456ffb50ebec9313bc4b3d7f5
workflow-type: tm+mt
source-wordcount: '46'
ht-degree: 0%

---

# 程式碼區塊中的斜線

1. 執行命令：

   ```bash
   vendor/bin/magento-patches -n status |grep "27015\|Status"
   ```

1. 執行命令（逸出）：

   ```bash
   vendor/bin/magento-patches -n status |grep "27015&bsol;|Status"
   ```

不在程式碼區塊中

廠商/bin/magento-patches -n狀態 |grep &quot;27015\|Status&quot;

逸出：

廠商/bin/magento-patches -n狀態 |grep &quot;27015&amp;amp；bsol；|Status&quot;

