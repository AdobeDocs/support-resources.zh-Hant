---
title: 表格分隔符號
description: 測試不同的表格分隔符號
hide: true
hidefromtoc: true
exl-id: a769fcb7-f8d3-419b-bdd4-98b71bdf3b5d
source-git-commit: 972704990172c966a27744b49b9f7af5626e9f3e
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 25%

---

# 表格分隔符號

這裡沒什麼可看的。

## 含有`<br>`的標準Markdown表格

**固定`Green<br>Red<br>Blue`**

|  | 數字 | 顏色 |
|---|---|---|
| 胡安亞 | 17 | 綠色<br>紅色<br>藍色 |
| 瑪麗亞 | 23 | 黃色<br>棕色 |

{style="table-layout:fixed"}

**自動`Green<br>Red<br>Blue`**

|  | 數字 | 顏色 |
|---|---|---|
| 胡安亞 | 17 | 綠色<br>紅色<br>藍色 |
| 瑪麗亞 | 23 | 黃色<br>棕色 |

{style="table-layout:auto"}

## 含有雙`<br>`的Markdown表格

**固定`Green<br><br>Red<br><br>Blue`**

|  | 數字 | 顏色 |
|---|---|---|
| 胡安亞 | 17 | 綠色<br><br>紅色<br><br>藍色 |
| 瑪麗亞 | 23 | 黃色<br><br>棕色 |

{style="table-layout:fixed"}

**自動`Green<br><br>Red<br><br>Blue`**

|  | 數字 | 顏色 |
|---|---|---|
| 胡安亞 | 17 | 綠色<br><br>紅色<br><br>藍色 |
| 瑪麗亞 | 23 | 黃色<br><br>棕色 |

{style="table-layout:auto"}

## 具有`<p>`的Markdown表格

**固定`Green<p>Red<p>Blue`**

|  | 數字 | 顏色 |
|---|---|---|
| 胡安亞 | 17 | 綠色<p>紅色<p>藍色 |
| 瑪麗亞 | 23 | 黃色<p>棕色 |

{style="table-layout:fixed"}

**自動`Green<p>Red<p>Blue`**

|  | 數字 | 顏色 |
|---|---|---|
| 胡安亞 | 17 | 綠色<p>紅色<p>藍色 |
| 瑪麗亞 | 23 | 黃色<p>棕色 |

{style="table-layout:auto"}

|  | 數字 | 顏色 |
|---|---|---|
| 胡安亞 | 17 | 這是&#x200B;**綠色**&#x200B;的顏色，而且它要包裝成不同的行，並且是測試上述段落分隔符號的方式。 <p>這是&#x200B;**紅色**&#x200B;的顏色，並且是用來包裝成其他行，或是測試前述段落分隔的方式。 <p>這是&#x200B;**藍色**&#x200B;的顏色，而且是用來換成其他行，或是測試上述段落符號的方式。 |
| 瑪麗亞 | 23 | 黃色<p>棕色 |

{style="table-layout:fixed"}

|  | 數字 | 顏色 |
|---|---|---|
| 胡安亞 | 17 | 這是&#x200B;**綠色**&#x200B;的顏色，而且它要包裝成不同的行，並且是測試上述段落分隔符號的方式。 <p>這是&#x200B;**紅色**&#x200B;的顏色，並且是用來包裝成其他行，或是測試前述段落分隔的方式。 <p>這是&#x200B;**藍色**&#x200B;的顏色，而且是用來換成其他行，或是測試上述段落符號的方式。 |
| 瑪麗亞 | 23 | 黃色<p>棕色 |

{style="table-layout:auto"}
