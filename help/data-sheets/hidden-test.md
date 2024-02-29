---
title: 隱藏測試頁面
description: 此頁面已從搜尋和目錄中隱藏
hide: true
hidefromtoc: true
badgePremium: label="Premium" type="Positive" url="https://www.premium-product.com" tooltip="下載 Premium"
badgeExam: label="測驗 ADO-E903" type="neutral"
source-git-commit: 0e4881c62b518866bd39d5c3f8eef0dc6063441b
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 94%

---

# 隱藏測試頁面

啟用?下午 3:10 左右重新檢查提交。 下午 3:30 會上線嗎?

## 按鈕

[按鈕預設](https://www.adobe.com/)

**[主要按鈕](https://www.adobe.com/)**

_[次要按鈕](https://www.adobe.com/)_

**_[第三按鈕](https://www.adobe.com/)_**

## 預覽問題

以下段落無法在 VSC 預覽中正確顯示。 我不知道為什麼。

如果您的密碼是由 [!DNL Adobe] 管理，您可以[變更 Adobe 帳戶中的密碼](https://helpx.adobe.com/tw/manage-account/using/change-or-reset-password.html){target="_blank"}。

## 備註類型

所有支援的備註類型。

>[!NOTE]
>
>這是一個標準的備註區塊。

>[!TIP]
>
>這是一個標準技巧。

>[!IMPORTANT]
>
>這是一個重要的備註。

>[!WARNING]
>
>這是一個警告。

>[!CAUTION]
>
>這是一個注意事項。

>[!ADMIN]
>
>這是一個管理備註，顯示為「管理」。 僅 EXL。

>[!AVAILABILITY]
>
>這是可用性備註。 僅 EXL。

>[!PREREQUISITES]
>
>這是先決條件備註。 僅 EXL。

>[!INFO]
>
>這是一則資訊備註。 僅 EXL。

>[!ERROR]
>
>這是一個錯誤備註。 僅 EXL。

>[!SUCCESS]
>
>這是一個成功備註。 僅 EXL。

>[!MORELIKETHIS]
>
>* 第 1 頁
>* 第 2 頁

## 徽章

徽章是用作內容指示器的彩色標籤。 例如，您可以新增徽章將文章標記為 _Beta_ 或將某個部分標記為 _Premium_。 您可以變更徽章的顏色並與 URL 和工具提示關聯。

[!BADGE 徽章範例]

有兩種類型 of 徽章，各自有不同的語法：

* **中繼資料** - 在頁面頂部附近顯示徽章
* **內嵌** - 顯示語法所在的徽章

### 中繼資料徽章

在中繼資料中新增徽章語法會將徽章放置在文章中的頁面標題 (H1) 上方。

您可以為徽章命名，例如使用 _badge1_ 或 _badge2_。 或者，您可以更有創意 (只要名稱以 _badge_&#x200B;開頭即可)。

中繼資料範例：

```
badgePremium: label="Premium" type="Positive" url="https://www.premium-product.com" tooltip="Download Premium"
badgeExam: label="Exam ADO-E903" type="neutral"
```

* **badgePremium：**&#x200B;此範例顯示含 URL 和工具提示的 Premium 徽章。

* **badgeExam：**&#x200B;此範例顯示含測驗 ID 號碼的深色徽章。

#### 內嵌徽章

在自身的行或標題、表格或其他頁面元素中指定徽章資訊。

以下是含 beta 標籤、藍色、URL 和工具提示的內嵌徽章的語法：

`[!BADGE Beta]{type=Informative url="https://www.example.com" tooltip="Go to example.com"}`

### 可用的徽章顏色

徽章使用 Adobe Spectrum 中定義的顏色：

| 類型 | 徽章 |
|---|---|
| 資訊性 (預設) | [!BADGE Beta]{type=Informative url="https://www.example.com"} |
| 正面 | [!BADGE 新功能]{type=Positive url="https://www.example.com" tooltip="前往example.com"} |
| 負面 | [!BADGE 已終止]{type=negative tooltip="此功能現已終止"} |
| 中立 | [!BADGE 可能]{type=Neutral tooltip="騎手從馬背上掉了下來……"} |
| 警告 | [!BADGE 注意]{type=Caution tooltip="Yellow status"} |

語法範例

```
|Type|Badge|
|---|---|
|Informative (default)|[!BADGE Beta]{type=Informative url="https://www.example.com"}|
|Positive|[!BADGE New Feature]{type=Positive url="https://www.example.com" tooltip="Go to example.com"}|
|Negative|[!BADGE Discontinued]{type=negative tooltip="This feature is now end of life"}|
|Neutral|[!BADGE Maybe]{type=Neutral tooltip="A rider fell off the horse..."}|
|Caution|[!BADGE Attention]{type=Caution tooltip="Yellow status"}|
```

### 徽章要求

* 中繼資料中只允許使用兩個徽章。 此規則是可設定的，因此如果您需要例外狀況，請告訴我們。
* 只需要徽章標籤。 `type`、 `url` 和 `tooltip` 參數是選擇性的。 `type` 參數決定顏色。 `url` 參數允許使用者點擊徽章來開啟文章或頁面。 `tooltip` 參數在滑鼠停留時顯示工具提示文字。
* 為 `TOC.md` 檔案新增徽章會在指南中的每篇文章上顯示徽章。 如果您為徽章指定跳到文章的 URL，請確保使用根連結 (例如，`/help/guide/article.md`) 而不是相對連結 (例如，`article.md`) 來說明不同資料夾中的文章。
* 新增徽章至 `metadata-new.md` 會在存放庫中的每篇文章上顯示該徽章。
* 對於中繼資料徽章，請確保所有值都用引號括住。 對於內嵌徽章，請確保將 `url` 和 `tooltip` 用引號括住。
* 有效類型值包括&#x200B;*資訊性* (預設，藍色)、*正面* (綠色)、*負面* (紅色)、*中立* (深灰色) 和&#x200B;*警告* (黃色)。
* 徽章標籤已當地語系化。
* 如果指定了多個中繼資料徽章，徽章將根據徽章名稱的字母順序顯示，例如 `badge1:` 或 `badgeWeb`。
* 如果您希望在新標籤中開啟 URL，請使用下列語法：

  ```
  [!BADGE Open in new tab]{type=Negative url="https://www.adobe.com newtab=true" tooltip="Open adobe.com in new tab"}
  ```

  轉譯：

  [!BADGE 在新標籤中開啟]{type=Negative url="https://www.adobe.com newtab=true" tooltip="在新標籤中開啟 adobe.com"}

## 文字醒目提示

Workfront 團隊希望能夠使用黃色醒目提示來指示即將推出的功能預覽。這是它的運作原理。

範例 1：

```
This entire paragraph should NOT be highlighted. <span class="preview"> This word is **bold** inside a highlighted sentence.</span> And this is just the last sentence.
```

轉譯：

整個段落不應醒目提示。<span class="preview"> 該單字在醒目提示的句子中為&#x200B;**粗體**。</span> 而這只是最後一句。

範例 2：

```
Highlighting should start after this paragraph.

<div class="preview">

Start of DIV.

This is a new paragraph, then an image

![image](/help/data-sheets/assets/BusinessSupportThumbnail.png)

Last highlighted item.

</div>

Not highlighted
```

轉譯：

醒目提示應在本段落之後開始。

<div class="preview">

DIV 的開頭。

這是一個新段落，然後是一張影像

![影像](/help/data-sheets/assets/BusinessSupportThumbnail.png)

最後醒目提示的項目。

</div>

未醒目提示

## 程式碼區塊的語法醒目提示

Experience League 支援程式碼區塊的語法醒目提示。 確保在一組開頭的反引號後指定一種語言，例如 `java`，以確保正確醒目提示語法。 有關有效語言的清單，請參閱 [https://prismjs.com](https://prismjs.com/#supported-languages)。 如果缺少任何語言，請記錄 jira 票證。

### 程式碼區塊中的行號

在語言後面加上 `{line-numbers="true"}` 以啟用行號。

有行號的範例 (&grave;&grave;&grave;`html {line-numbers="true"}`)：

```html {line-numbers="true"}
<!DOCTYPE html>
<html>
<body>

<h1>My First Heading</h1>
<p>My first paragraph.</p>

</body>
</html>
```

**開始在行 _ 上編號**

在行號語法後面加上 `start-number="n"` 以從 1 以外的數字開始編號。

有新起始行的範例 (&grave;&grave;&grave;`html {line-numbers="true" start-line="7"}`)：

```html {line-numbers="true" start-line="7"}
<!DOCTYPE html>
<html>
<body>

<h1>My First Heading</h1>
<p>My first paragraph.</p>
<p>My second paragraph.</p>

</body>
</html>
```

### 程式碼區塊中的行醒目提示

在行號語法後新增 `highlight="n"` 以醒目提示程式碼區塊中的行。 指定 `11-13, 16` 將醒目提示第 11 行到第 13 行和第 16 行。

有醒目提示行的範例 (&grave;&grave;&grave;`html {line-numbers="true" start-line="7" highlight="11-13, 16"}`)：

```html {line-numbers="true" start-line="7" highlight="11-13, 16"}
<!DOCTYPE html>
<html>
<body>

<h1>My First Heading</h1>
<p>My first paragraph.</p>
<p>My second paragraph.</p>

</body>
</html>
```
