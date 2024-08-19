---
title: 程式碼區塊中的斜線UGP-11189
description: 程式碼區塊中的斜線UGP-11189測試
hide: true
hidefromtoc: true
source-git-commit: 4fc9b739d18941d276b88f8799163523c8bd5f85
workflow-type: tm+mt
source-wordcount: '45'
ht-degree: 4%

---

# 程式碼區塊中的斜線

1. 執行命令：

   ```bash
   vendor/bin/magento-patches -n status |grep "27015\|Status"
   ```

1. 下一步

不在程式碼區塊中

廠商/bin/magento-patches -n狀態 |grep &quot;27015\|Status&quot;

逸出的反斜線：

廠商/bin/magento-patches -n狀態 |grep &quot;27015&amp;amp；bsol；|Status&quot;
