---
title: 擴充性與容量規劃
description: 擴充性和容量規劃建議，可協助Adobe Commerce商家為高流量事件（例如節日季節）準備環境。
feature-set: Commerce
feature: Support
solution: Commerce
role: Developer, Admin, Leader
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 5a951749-fac9-5bc7-9a98-ebe4ff066437
    internal-label: Cloud
  - id: e8818fe6-9c8b-4bc0-9ef8-377a10b7bc75
    internal-label: Architecture
subfeature_v2:
  - id: f8ddfd3b-6194-46e8-a176-0e918039be56
    internal-label: Cloud architecture
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: b2220ea4cb5a301cbee6cea5fb90d6dc8a05eeff
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%
---

# 擴充性與容量規劃

本節提供縮放Adobe Commerce環境的技術建議，以便為節日季節之類的高流量事件做好準備。

>[!NOTE]
>
>標示為&#x200B;**（僅限雲端）**&#x200B;的步驟適用於雲端基礎結構上的Commerce。 大部分其他建議也適用於內部部署。

## 儘早規劃叢集擴充規模（僅限雲端） {#plan-cluster-upsize-early}

對於雲端基礎結構客戶的Commerce，臨時叢集擴充可分配更多運算資源以處理旺季的流量激增。 提出日期範圍和所需叢集大小的支援票證，並與您的專屬客戶經理協調目前資源消耗和需求。 請在需要容量之前至少提前48個營業時間提交請求，尤其是對於假日季節，請儘早提交，因為黑色星期五和網路星期一的容量有限。 請參閱[如何要求暫時的擴充大小](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-commerce-support/how-to-request-temporary-adobe-commerce-on-cloud-infrastructure-upsize)。

例如，如果專業架構的客戶每日基準為24個核心（24個vCPU、96GB RAM），每日7天可擴充至96個核心，則其耗用的資源約為4倍（96個vCPU、384GB RAM），以增量方式消耗約504個vCPU天數(96×7−24×7)。

## Fastly來源遮蔽 {#fastly-origin-shielding}

Adobe Commerce [!DNL Fastly]來源遮蔽的目的是減少直接傳往Adobe Commerce來源的流量。 收到要求時，[!DNL Fastly]邊緣位置(Point of Presence)會檢查快取的內容並傳送它。 如果未快取，則會繼續到Shield POP檢查它是否已在其中快取，如果先前甚至從其他全域POP請求過內容，則會將其快取。 最後，如果未在Shield POP上快取，則只會繼續前往原始伺服器。

可在Adobe Commerce管理員的[!DNL Fastly]組態後端設定中啟用[!DNL Fastly]來源遮蔽。 選擇最接近Adobe Commerce原始資料中心的遮蔽位置，以獲得最佳效能。 如需詳細資訊，請參閱[設定後端與來源遮蔽](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/cdn/setup-fastly/fastly-custom-cache-configuration#configure-back-ends-and-origin-shielding)。 依預設，[!DNL Fastly]來源遮蔽未啟用。

## 執行載入和容錯移轉測試 {#conduct-load-and-failover-tests}

在主要行銷活動之前執行載入和復原測試，以驗證擴充設定和復原計畫。