---
title: 隱藏的疑難排解
description: 隱患
type: Troubleshooting
hide: true
hidefromtoc: true
exl-id: dfb54d2d-e4f4-420f-8e91-f1aba704cb31
source-git-commit: d163b3a086aaabf98d75625ffab653a7cfd5bd67
workflow-type: tm+mt
source-wordcount: '32'
ht-degree: 12%

---

# 隱藏的疑難排解

有`type: Troubleshooting`套用至此頁面。 它有左側導覽嗎？

## 程式碼表格

直`<code>`

<table>
    <tr>
      <th>已排序的身分清單</th>
      <th>選取的身分</th>
    </tr>
    <tr>
      <td><code>PrimaryIdentities [<br/>&nbsp;&nbsp;{"id": "ccid-2", "namespace": "CCID"},<br/>&nbsp;&nbsp;{"id": "ecid-1", "namespace": "ECID"},<br/>&nbsp;&nbsp;{"id": "ecid-2", "namespace": "ECID"}<br/>&nbsp;]<br/>&nbsp;NonPrimaryIdentities [<br/>&nbsp;&nbsp;{"id": "ccid-1", "namespace": "CCID"},<br/>&nbsp;&nbsp;{"id": "ecid-3", "namespace": "ECID"}<br/>]</code> </td>
      <td><code>"id": "ccid-1",<br/>&nbsp;"namespace": "CCID"</code> </td>
    </tr>
  </table>

與`<pre lang="json"><code>`


<table>
    <tr>
      <th>已排序的身分清單</th>
      <th>選取的身分</th>
    </tr>
    <tr>
      <td><pre lang="json"><code>PrimaryIdentities [<br/>&nbsp;&nbsp;{"id": "ccid-2", "namespace": "CCID"},<br/>&nbsp;&nbsp;{"id": "ecid-1", "namespace": "ECID"},<br/>&nbsp;&nbsp;{"id": "ecid-2", "namespace": "ECID"}<br/>&nbsp;]<br/>&nbsp;NonPrimaryIdentities [<br/>&nbsp;&nbsp;{"id": "ccid-1", "namespace": "CCID"},<br/>&nbsp;&nbsp;{"id": "ecid-3", "namespace": "ECID"}<br/>]</pre></code> </td>
      <td><pre lang="json"><code>"id": "ccid-1",<br/>&nbsp;"namespace": "CCID"</pre></code> </td>
    </tr>
  </table>

