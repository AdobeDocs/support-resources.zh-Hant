---
title: 表格分隔符號
description: 測試不同的表格分隔符號
hide: true
hidefromtoc: true
source-git-commit: 9ad23090cb13f36d6d015b23122736048fe2230c
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 28%

---

# 表格分隔符號

這裡沒什麼可看的。

## 標準Markdown表格包含 `<br>`

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

## Markdown表格（含兩次） `<br>`s

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

## Markdown表格包含 `<p>`

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
| 胡安亞 | 17 | 這是顏色 **綠色** 而且其用意是要當作事項換成不同的行，以及測試上述段落分隔符號的方式。 <p>這是顏色 **紅色** 而且其用意是要當作事項換成不同的行，以及測試上述段落分隔符號的方式。 <p>這是顏色 **藍色** 而且其用意是要當作事項換成不同的行，以及測試上述段落分隔符號的方式。 |
| 瑪麗亞 | 23 | 黃色<p>棕色 |

{style="table-layout:fixed"}

|  | 數字 | 顏色 |
|---|---|---|
| 胡安亞 | 17 | 這是顏色 **綠色** 而且其用意是要當作事項換成不同的行，以及測試上述段落分隔符號的方式。 <p>這是顏色 **紅色** 而且其用意是要當作事項換成不同的行，以及測試上述段落分隔符號的方式。 <p>這是顏色 **藍色** 而且其用意是要當作事項換成不同的行，以及測試上述段落分隔符號的方式。 |
| 瑪麗亞 | 23 | 黃色<p>棕色 |

{style="table-layout:auto"}
