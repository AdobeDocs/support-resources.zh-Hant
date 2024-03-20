---
title: 錯誤修正（隱藏）
description: 目的在進行內部測試的測試頁面
hide: true
hidefromtoc: true
source-git-commit: 57c0a39d3b2dcb50259ee285b1a61f8ad4db12ea
workflow-type: tm+mt
source-wordcount: '1817'
ht-degree: 27%

---

# 錯誤修正

## UGP-10584內嵌徽章無法運作

這些徽章應與專案符號專案位於同一行。

* [[!DNL Mixpanel]](note-test.md) [!BADGE 附註]{type=Informative}
* [[!DNL Pendo]](tables.md) [!BADGE 表格]{type=Positive}
* [[!DNL RainFocus]](syntax-style-guide.md) [!BADGE 語法樣式指南]{type=Positive}

## UGP-10560 — 可摺疊區段中的徽章

+++ 舊版

### V1.16版本

_2023 年 2 月 13 日_

[!BADGE 支援]{type=Informative tooltip="支援"}

![新增](assets/package.png) 目錄服務API現在支援產品影片。
![修正](assets/package.png) 現在支援固定價格的套件組合產品。
![修正](assets/package.png) 無庫存選項現在顯示在PDP Widget中。

#### 已知限制

尚未支援這些功能：

* 動態屬性承載的大小上限為9 MB。
* 群組產品價格。 可使用簡單產品價格計算。
* 在影像陣列中，只有第一個影像包含角色。

使用API Mesh和核心GraphQL API可以解決下列限制：

* 最低廣告價格
* [層級定價](https://www.adobe.com/tw/)

### V1.13版本

_2023年10月12日_

[!BADGE 支援]{type=Informative tooltip="支援"}

![新增](assets/package.png) 目錄服務支援 `inStock` 產品變體的標幟。
![新增](assets/package.png) `urlKey` 和 `externalId` 已新增至GraphQL結構描述。
![新增](assets/package.png) 現已支援可下載的產品和禮品卡。

### V1.12版本

_2023年9月19日_

[!BADGE 支援]{type=Informative tooltip="支援"}

![新增](https://www.adobe.com/tw/).
![修正](assets/package.png) 此版本包含服務端的錯誤修正和改善。

### V1.11版本

_2023年7月18日_

[!BADGE 支援]{type=Informative tooltip="支援"}

![新增](assets/package.png) 目錄服務現在支援 [`recommendations`](https://developer.adobe.com/commerce/services/graphql/recommendations/recommendations/) 產品Recommendations的GraphQL查詢。

### V1.10版本

_2023年6月27日_

[!BADGE 支援]{type=Informative tooltip="支援"}

![新增](assets/package.png) 目錄服務API現在支援「相關產品」。

### V1.7版本

_2023年4月12日_

[!BADGE 支援]{type=Informative tooltip="支援"}

![新增](assets/package.png) 目錄服務現在會清理已刪除的產品變體。
![修正](assets/package.png) 基礎建設擴充能力與效能提升。

### V1.6版本

_2023年3月28日_

[!BADGE 支援]{type=Informative tooltip="支援"}

![新增](assets/package.png) 將色票新增至 [`products`](https://developer.adobe.com/commerce/services/graphql/catalog-service/products/) 查詢。
![新增](https://www.adobe.com/tw/).

### V1.5版本

_2023年3月6日_

[!BADGE 支援]{type=Informative tooltip="支援"}

![新增](assets/package.png) 已新增 [`categories`](https://developer.adobe.com/commerce/services/graphql/schema/catalog-service/categories/) GraphQL功能。
![修正](assets/package.png) 改善效能和API擴充性。

### V1.4版本

_2023年2月7_

[!BADGE 支援]{type=Informative tooltip="支援"}

![新增](assets/package.png) 已發佈目錄服務中繼資料以簡化安裝步驟。
![修正](assets/package.png) API擴充性和效能的改善。

### V1.3版本

_2023年1月17日_

[!BADGE 支援]{type=Informative tooltip="支援"}

![新增](assets/package.png) 簡化並改善入門體驗。
![新增](assets/package.png) 新的客戶沙箱端點可用於生產前測試。
![新增](assets/package.png) 新增對虛擬產品的支援。
![修正](assets/package.png) API擴充性和效能的改善。

### V1.1版本

_2022年11月18日_

[!BADGE 支援]{type=Informative tooltip="支援"}

![新增](assets/package.png) 目錄服務現在支援Adobe的 [API網格](https://developer.adobe.com/graphql-mesh-gateway/).
![修正](assets/package.png) 改善API擴充性和整體效能。

### V1.0版本

_2022年10月4日_

[!BADGE 支援]{type=Informative tooltip="支援"}

![新增](assets/package.png) 現在支援套件和分組的產品。
![新增](assets/package.png) 新增B2B可見性覆寫。 產品現在可供搜尋，並可新增至特定客戶群組的購物車。
![修正](assets/package.png) 服務現在更穩定，效能也有所改善。

### 0.3版 — Beta+

_2022年9月12日_

[!BADGE 支援]{type=Informative tooltip="支援"}

![新增](assets/package.png) 變體支援的影像：根據選取的選項傳回產品影像
![新增](assets/package.png) 價格支援的角色：僅允許特定客戶群組的成員檢視產品價格
![修正](assets/package.png) 改善服務的穩定性與效能
![新增](assets/package.png) 從目錄中刪除產品時，會收到更新

### 測試版本

_2022 年 8 月 9 日_

[!BADGE 支援]{type=Informative tooltip="支援"}

![新增](assets/package.png) 此 `products` 和 `refineProduct` 查詢會傳回以下資料：

* 預先定義的（系統）產品屬性。
* 動態產品屬性，並依角色（產品顯示頁面/產品清單頁面）篩選。
* 產品選項。
* 產品影像並依角色(PDP/PLP)篩選。
* 簡單產品的特定價格，以及可設定產品的價格範圍。
* 客戶群組價格和價格範圍。 這類優惠會針對沒有客戶群組的購物者傳回遞補預設價格。
* 使用B2B客戶特定定價的產品型別。

+++

## UGP-10565 — 文字醒目提示

在此之前的文字 `<div class="preview">`

<div class="preview">

### 新增Workfront原生欄位

您可以將Workfront原生欄位新增至自訂表單。 當自訂表單附加到物件時，會從物件資料填入欄位。 例如，附加到專案的自訂表單上的說明欄位將提取專案說明。 （如果沒有可用資料，欄位可能會顯示「N/A」。）

1. 在畫面左側，尋找 **原生欄位** 並將其拖曳至畫布上的區段。
1. 在畫面右側，設定自訂欄位的選項：

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">標籤</td> 
      <td> <p>（必要）輸入描述性標籤以顯示於欄位上方。 您可以隨時變更標籤。</p> <p><b>重要</b>：請避免在此標籤中使用特殊字元。 它們在報表中無法正確顯示。</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">名稱</td> 
      <td> <p>（必要）此名稱是系統識別欄位的方式。</p><p> 當您第一次設定欄位並輸入標籤時，「名稱」欄位會自動填入以和欄位相符。 但是「標籤」和「名稱」欄位不同步，這可讓您自由地變更使用者看到的標籤，而不必變更系統看到的名稱。</p>
      <p><b>重要</b>：
      <ul> 
      <li>雖然可以這樣做，但建議您不要在您或其他使用者開始使用Workfront中的自訂表單後變更此名稱。 如果這樣做，系統將不再識別現在可能在Workfront其他區域參考它的欄位。</p> </li>
      <li> <p>每個欄位名稱在貴組織的Workfront例項中必須是唯一的。 如此一來，您便可重複使用已針對其他自訂表單建立的表單。</p> </li>
      <li><p>建議您不要在自訂欄位名稱中使用句號/點字元，以防止在Workfront的不同區域使用欄位時發生錯誤。</p></td> 
     </tr> 
     <tr> 
      <td role="rowheader">說明</td> 
      <td> <p>輸入有關欄位的任何其他資訊。 當使用者填寫自訂表單時，可以將滑鼠指標暫留在問號圖示上，以檢視包含您在此處輸入資訊的工具提示。</td> 
     </tr> 
     <tr> 
      <td role="rowheader">參考欄位</td> 
      <td><p>（必要）選取Workfront原生欄位。<p><p>僅表單物件的原生欄位可用。 例如，如果表單設計器頂端的「物件型別」清單顯示「專案」，您將能夠選取專案的原生欄位，但不能選取任務特定的欄位。</p></td>
     </tr>
     <tr> 
      <td role="rowheader">大小</td> 
      <td>（可選）視需要變更欄位的顯示大小。</td> 
     </tr> 
    </tbody> 
   </table>

1. 若要儲存變更，請按一下 **套用** 並移至另一個區段，以繼續建立您的表單。

   或

   按一下&#x200B;**儲存並關閉**。

</div>

醒目提示後的文字

## UGP-10566 — 連結文字小於HTML表格中的一般文字

另請參閱UGP-9780

<table style="table-layout:auto"> 
<tbody> 
<tr>
<td>輸入至</td>
<td>說明</td>
<td>可用於 </td>
</tr>
<tr> 
    <td role="rowheader">標籤</td> 
    <td> <p>（必要）輸入描述性標籤，以在自訂欄位上方顯示。 您可以隨時變更標籤。 如需詳細資訊，請參閱 <a href="https://www.adobe.com/tw/" class="MCXref xref">新增自訂欄位至自訂表單</a> 本文章內容。</p> <p><b>重要</b>：請避免在此標籤中使用特殊字元。 它們在報表中無法正確顯示。</p> </td> 
    <td>
    <ul>
    <li>選項按鈕。 如需詳細資訊，請參閱 <a href="https://www.adobe.com/tw/">新增自訂欄位至自訂表單</a> 本文章內容。 （無類別）</li>
    <li>核取方塊群組</li>
    <li>下拉式清單</li>
    </ul></td>
</tr> 
</tbody> 
</table>

## UGP-9176 — 舊錯誤

「span」標籤在NOTE （和清單）中無法正常運作

如需有關新註解體驗中哪些功能可用以及哪些物件的資訊，請參閱 [新的評論體驗](note-test.md).

1. 移至您要新增回覆的物件。
1. 按一下 **更新**，然後按一下 **註解** 定位物件，並尋找您要回覆的註解或回覆

   或

   <span class="preview">按一下 **全部** 標籤，然後按一下 **在評論中回覆** 以在「註解」標籤中開啟註解並回覆。 您無法在「全部」索引標籤中回覆。</span>

1. （可選）若要在回覆中包含先前更新的文字，請按一下 **更多** 選單，然後按一下 **引用回覆**. 先前更新的文字會出現在輸入區域中，以垂直灰色線標示。
1. 按一下 **回覆**.

   ![](assets/package.png)

   您可以在頁面底部看到目前參與交談的使用者 **新增回覆……** 方塊中，您可以新增更多或移除不再相關的專案。 這些使用者以及訂閱物件的任何使用者會在物件進行更新或回覆時收到通知。 您也可以標籤更多使用者，讓他們加入您的回覆中。  若要標籤更多使用者，請參閱 [標籤其他人的更新](note-test.md).

   >[!TIP]
   >
   >   若要新增其他回覆至現有的回覆，您可以開始輸入 **新增回覆……** 方塊，或按一下 **回覆** 在原始註解上。 您的回覆會新增至對話串的結尾。

1. 開始輸入您的回覆，並使用RTF工具列的任何其他選項。 如需有關使用RTF或其他更新功能的資訊，請參閱 [更新工作](note-test.md).

1. 按一下 **提交** 以儲存回覆。

1. （可選）按一下 **更多** 選單（位於您要回覆的評論右上角），以取得管理回覆的更多選項。 如需詳細資訊，請參閱 [更新工作](note-test.md).


## UGP-10614 — 有影像的問題表格

我認為 `{width="20"}` 引數造成表格中出現問題。

## Expert 和 Ultimate 成功計劃的比較

|  | Expert 成功計劃 | Ultimate 成功計劃 |
|--- |--- |--- |
|  | 借助 Expert 成功計劃，您可以獲得&#x200B;**24X7 全年無休的專家服務**，在發生重要業務問題時進行技術疑難排解和指導。或者，您可以利用我們的自助資源、獨家最佳作法以及 Adobe 專家和同行的線上社群，找到快速解決方案。 <p> *隨附在所有 Adobe Experience Cloud 授權中。* | 藉助 Ultimate 成功計劃，您將體驗到&#x200B;**策略指導和主動的技術健康狀況，以提供高效能的數位體驗**。您的 Adobe 環境將由一組專家團隊提供支援，這些專家熟悉您的業務並專注於執行符合您業務影響目標和優先順序的藍圖。 |
| **成功團隊** | 匯集的支援工程師團隊 | 包括： <ul><li> 指定的技術客戶經理 </li><li> 指定的客戶成功經理 </li><li> 指定的支援服務經理</li><li> 匯集的技術工程師和策略專家團隊提供成功加速器 </li><li> 匯集的支援工程師團隊 </li></ul> |
| **主動式技術 + 營運支援** | ![不包含圖示](../assets/Cross_red_circle.svg){width="20"} 不包含 | 包括： <ul><li>升級和移轉審查、發行準備 </li><li>產品藍圖審查</li><li> 一致的技術和策略藍圖</li><li>重要事件準備與規劃</li><li>規劃相關且及時的啟用</li><li>技術最佳實務和產業指南</li><li>支持/與產品團隊保持一致</li><li>實現重要業務目標的統一計劃 - 共同行動計劃 (MAP)</li></ul> |
| **技術支援** | 包括： <ul><li>**P1**：24x7 問題支援</li><li>**P2、P3、P4**：營業時間支援</li><li>標準中斷管理</li><li>匯集的向上呈報管理</li></ul> | 包括： <ul><li>**P1**：24x7 問題支援</li><li>**P2/P3**：24x5 問題支援</li><li>**P4**：營業時間支援</li><li>有優先權的中斷管理</li><li>指定專家向上呈報管理</li></ul> |
| **成功加速器** | ![不包含圖示](../assets/Cross_red_circle.svg){width="20"} 不包含 | TAM 和 CSM 定期排程的成功加速器<p>*(有關更多資訊，請參閱成功加速器目錄)* |
| **支援管道** | 線上、電話、Experience League、論壇 | 個人化線上入口網站、有優先權的電話、Experience League、論壇 |

{style="table-layout:fixed"}

## 支援附加元件

| 附加元件 | Expert 成功計劃 | Ultimate 成功計劃 |
|--- |--- |--- |
| **事件管理附加元件**<br>&#x200B;提供管理關鍵事件的整個生命週期所需的端對端領導力和支援 | ![可用圖示](../assets/Plus_blue.svg){width="20"} 可用 | ![可用圖示](../assets/Plus_blue.svg){width="20"} 可用 |
| **技術客戶總監附加元件**<br>&#x200B;您的首席技術資源，負責提供領導階層監督、擁有高階主管參與能力，並確保治理，讓您獲取最大的業務成果 | ![不適用圖示](../assets/Cross_red_circle.svg){width="20"} 不適用 | ![可用圖示](../assets/Plus_blue.svg){width="20"} 可用 |
| **進階雲端支援附加元件**<br>&#x200B;對 Adobe Experience Manager as a Cloud Service 客戶的頂級服務和價值保證 | ![可用圖示](../assets/Plus_blue.svg){width="20"} 可用 | ![可用圖示](../assets/Plus_blue.svg){width="20"} 可用 |
| **導師輔導附加元件**<br>&#x200B;以即時訓練方法提供基於技能的學習 | ![可用圖示](../assets/Plus_blue.svg){width="20"} 可用 | ![可用圖示](../assets/green_checkmark.svg){width="20"} 已包含 |
| **開發人員強化附加元件**<br>&#x200B;可聯絡現場工程專家來協助進行故障修復工作 | ![可用圖示](../assets/Plus_blue.svg){width="20"} 可用 | ![已包含圖示](../assets/green_checkmark.svg){width="20"} 已包含 |
| **優先級佇列套件組合附加元件**<br>&#x200B;免排隊優先處理您的票證，並獲得導師輔導和開發人員強化的額外存取權限 | ![可用圖示](../assets/Plus_blue.svg){width="20"} 可用 | ![已包含圖示](../assets/green_checkmark.svg){width="20"} 已包含 |

{style="table-layout:fixed"}
