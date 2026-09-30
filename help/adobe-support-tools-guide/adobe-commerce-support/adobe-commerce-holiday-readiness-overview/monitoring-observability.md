---
title: 監視和可觀察性
description: 監控和觀察性建議可幫助Adobe Commerce商家準備他們環境以進行高流量事件，例如假日季節。
feature-set: Commerce
feature: Support
solution: Commerce
role: Developer, Admin, Leader
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: 5a951749-fac9-5bc7-9a98-ebe4ff066437
    internal-label: Cloud
  - id: cdfd3bc1-dc23-5cf0-b965-d3c0c55cde67
    internal-label: Best Practices
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: 4239b8a6-e74f-567d-a7a5-b98b9ead0ea4
    internal-label: Observability
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
subfeature_v2:
  - id: 3c398179-d35a-51ba-b317-6c5b95feef5e
    internal-label: Logs
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 71589dd124714805fbf844540fb2d272433631ee
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 2%
---

# 監視和可觀察性

本節提供監控Adobe Commerce環境的技術建議，以便為節日季節之類的高流量事件做好準備。

>[!NOTE]
>
>標示為&#x200B;**（僅限雲端）**&#x200B;的步驟適用於雲端基礎結構上的Commerce。 大部分其他建議也適用於內部部署。

## 使用New Relic監控流量（僅限Cloud） {#monitor-traffic-with-new-relic}

雲端基礎結構上的Adobe Commerce包括[!DNL New Relic]可觀察性平台訂閱，該訂閱無縫地合併了[!DNL Fastly]個串流到[!DNL New Relic]中的記錄，而且幾乎是即時的。 此整合可讓您即時監控流量模式和趨勢，以便您採取修正動作。

使用這些記錄來：

* 識別您的網路請求來源國家/地區。
* 尋找抓取您網站的濫用IP位址或使用者代理。
* 識別以特定端點為目標的惡意流量，例如付款。
* 針對客戶使用的裝置和瀏覽器型別建立報表。

例如，監視流量的來源國家/地區，以確認其反映您的促銷活動和客戶的地理位置：

```sql
SELECT count(*) FROM Log
WHERE cache_status IS NOT NULL
AND project_id = '<YOUR_PROJECT_ID>'
AND (content_type LIKE 'text/html;%' or url LIKE '%graphql%' or url like '%rest%')
FACET geo_country_code
SINCE 7 days ago until today
```

修改此查詢以符合您的需求、進一步區隔查詢，或將其轉換為控制面板以集中追蹤。 如需詳細資訊，請參閱[New Relic記錄檔管理](https://experienceleague.adobe.com/zh-hant/docs/commerce-on-cloud/user-guide/monitor/new-relic/log-management)。

## 自訂New Relic警報（僅限雲端） {#customize-new-relic-alerts}

除了Adobe Commerce在雲端基礎結構上設定的「受管理警報」之外，您還可以在銷售旺季為您的平台設定範圍廣泛的警報和通知，例如，通知您機器人流量或GraphQL查詢的回應時間增加。 如需內建警示的完整清單，請參閱[Adobe Commerce的管理警示](https://experienceleague.adobe.com/zh-hant/docs/commerce-operations/tools/managed-alerts-for-adobe-commerce/managed-alerts-for-magento-commerce)。

[!DNL New Relic]警示和AI支援NRQL型查詢結構。 從&#x200B;**[!UICONTROL 警示與AI]**&#x200B;下的[!DNL New Relic]儀表板設定自訂警示。

## 檢閱Apdex分數（僅限Cloud） {#review-apdex-score}

Apdex分數會測量使用者對您網頁應用程式與服務之回應時間的滿意度。 您可以使用[!DNL New Relic]在雲端基礎結構上檢閱Adobe Commerce的Apdex分數。

Apdex分數介於0到1之間。 0分是最差的分數，表示100%的回應時間是&#x200B;**受挫感**。 1分是最佳分數，表示100%的回應時間是&#x200B;**滿意**。 [!DNL New Relic]會同時報告反映後端效能的應用程式伺服器分數和反映使用者端效能的一般使用者分數。

Apdex分數為0.5或更低的認股權證調查。 低於0.4的分數會被視為中斷。

[!DNL New Relic]與Apdex一起提供了一系列的統計資料，用於分析Adobe Commerce在雲端基礎結構上的效能問題。 如需相關步驟，請參閱[在Adobe Commerce上使用New Relic進行效能疑難排解](https://experienceleague.adobe.com/zh-hant/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/troubleshoot-performance-using-new-relic-on-magento-commerce)。

## 檢閱支援深入分析（SWAT報表） {#review-support-insights-swat-report}

如需環境的詳細報表，請產生全網站分析工具(SWAT)報表。 如需SWAT工具的詳細資訊，請參閱[全網站分析工具](https://experienceleague.adobe.com/zh-hant/docs/commerce-operations/tools/site-wide-analysis-tool/intro)。