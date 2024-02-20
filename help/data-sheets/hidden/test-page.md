---
title: 測試頁面（隱藏）
description: 用於內部測試的測試頁面
hide: true
hidefromtoc: true
source-git-commit: 8956f958d373f1c67f4ffddf48388f7611ce00ea
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 1%

---

# 測試頁面（隱藏）

隱藏測試頁面

## 影像(EXLM-412)

### 影像包含暫留文字

![替代文字 — package.png](assets/package.png "游標停留文字 — 這是package.png")

### 文字置中

<p align="center">我置中</p>

<center>我置中</center>

### 可縮放影像

`![Dive image](assets/maui-dive.jpg "Diving in Maui"){width=100 zoomable}`

**平坦**

![下潛影像](assets/maui-dive.jpg "在茂宜島跳水"){width=100 zoomable}

**注意**

>[!NOTE]
>
>按一下下列影像檢視潛水員：
>
>![下潛影像](assets/maui-dive.jpg "在茂宜島跳水"){width=100 zoomable}

**表格**

|  | 數字 | 顏色 |
|---|---|---|
| 胡安雅 | 17 | 綠色<br>紅色<br>藍色 |
| Maria | 23 | 黃色<br>棕色 |
| Bob | 60 | 檢視影像<br>![下潛影像](assets/maui-dive.jpg "在茂宜島跳水"){width=100 zoomable} |

{style="table-layout:fixed"}

### 基本影像測試

寬度=200 （與下表比較）

![替代文字](assets/maui-dive.jpg "寬度= 200"){width=200}

寬度=50% （與下表比較）

![替代文字](assets/maui-flip.jpg "寬度= 50%"){width=50%}

### 包裝測試 ![替代文字](assets/package.png "靠右對齊"){align="right"}

**無對齊**

![替代文字](assets/maui-dive.jpg "寬度= 100"){width=100} 在茂宜島跳崖並不像人們想象的那麼困難。 潛水確實有四個步驟，而安全潛水則有五個步驟。 首先，從懸崖上猛跳下去，立即伸出雙臂並指向腳趾。 這是相機的姿勢。 第二，將您的身體機動到一個合理的著陸位置。 這看起來可能像是恐慌，但這僅僅是一種基於情緒的調整。 第三，以不會傷害身體的方式濺射。 第四，突然出現，就好像您已完成此百萬次了，而且有點無聊。

**靠右對齊**

在茂宜島跳崖並不像人們想象的那麼困難。 潛水確實有四個步驟，而安全潛水則有五個步驟。 首先，從懸崖上猛跳下去，立即伸出雙臂並指向腳趾。 這是相機的姿勢。 第二，將您的身體機動到一個合理的著陸位置。 這看起來可能像是恐慌，但這僅僅是一種基於情緒的調整。 第三，以不會傷害身體的方式濺射。 第四，突然出現，就好像您已完成此百萬次了，而且有點無聊。 ![替代文字](assets/maui-dive.jpg "100寬度靠右對齊"){width="100" align="right"}

**靠左對齊**

![替代文字](assets/maui-dive.jpg "100寬度靠左對齊"){width="100" align="left"} 在茂宜島跳崖並不像人們想象的那麼困難。 潛水確實有四個步驟，而安全潛水則有五個步驟。 首先，從懸崖上猛跳下去，立即伸出雙臂並指向腳趾。 這是相機的姿勢。 第二，將您的身體機動到一個合理的著陸位置。 這看起來可能像是恐慌，但這僅僅是一種基於情緒的調整。 第三，以不會傷害身體的方式濺射。 第四，突然出現，就好像您已完成此百萬次了，而且有點無聊。

**假的右對齊**

在茂宜島跳崖並不困難。 ![替代文字](assets/maui-dive.jpg "100寬度靠右對齊"){width="100" align="right"}

潛水確實有四個步驟，而安全潛水則有五個步驟。 首先，從懸崖上猛跳下去，立即伸出雙臂並指向腳趾。 這是相機的姿勢。 第二，將您的身體機動到一個合理的著陸位置。 這看起來可能像是恐慌，但這僅僅是一種基於情緒的調整。 第三，以不會傷害身體的方式濺射。 第四，突然出現，就好像您已完成此百萬次了，而且有點無聊。


### 影像對齊方式

一般

![替代文字](assets/package.png "將圖示文字暫留")

下方靠右對齊

![替代文字](assets/package.png "align=right"){align="right"}

靠右內嵌 ![替代文字](assets/package.png "align=right"){align="right"}

中央寬度= 250

![替代文字](assets/maui-dive.jpg "align=center"){align=&quot;center&quot; width=250}

### 標題對齊方式

**粗體標題** ![替代文字](assets/package.png "align=right"){align="right"}

請參閱上方的粗體標題。

### 表格中的影像

圖示靠右對齊，俯檢視片置中200畫素，翻轉影像靠右對齊50%。

| <center>左側 | 中間 | 右</center> |
|---|---|---|
| ![替代文字](assets/package.png "align=right"){align=right} | ![替代文字](assets/maui-dive.jpg "align=center width=200"){align="center" width="200"} | ![替代文字](assets/maui-flip.jpg "align=right width=50%"){align="right" width="50%"} |

## 檔案附件(EXLM-1124)

下載 [PDF](/help/data-sheets/assets/BusinessSupportDatasheet.pdf)

下載 [JS](assets/main.js)

下載 [CSS](assets/main.css)

下載 [TXT檔案](assets/dots.txt)

下載 [XLSX檔案](assets/4-module_version.xlsx)

下載 [ZIP檔案](assets/2-Factor-Authentication-DataSource-and-FDM.zip)
