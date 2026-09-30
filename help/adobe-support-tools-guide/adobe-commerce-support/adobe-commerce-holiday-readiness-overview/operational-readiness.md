---
title: 營運整備
description: 營運整備建議，協助Adobe Commerce商家為高流量事件（例如節日季節）準備環境。
feature-set: Commerce
feature: Support
solution: Commerce
role: Developer, Admin, Leader
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: cdfd3bc1-dc23-5cf0-b965-d3c0c55cde67
    internal-label: Best Practices
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: bcd8874c-7b93-5596-bdaa-22660e84df14
    internal-label: Deploy
  - id: 5a951749-fac9-5bc7-9a98-ebe4ff066437
    internal-label: Cloud
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 938d2364-5176-55ec-80f1-9415253e5e51
    internal-label: Site Management
  - id: b48dbafb-4193-5648-b9d9-bf96e9c9a411
    internal-label: Backend Development
  - id: e7dae43f-215c-4cdf-90d3-c5a461a6e669
    internal-label: Admin tools and workspace
subfeature_v2:
  - id: bb2df8be-afdd-4818-b6b5-95ca1dd3bc3a
    internal-label: Admin workspace
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: c89c0345d0e483463ab44195c2d5c0cb18d1d4c5
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%
---

# 營運整備

本節提供相關技術建議，說明如何在雲端基礎結構和內部部署上準備Adobe Commerce環境，以因應假期之類的高流量事件。

## 套用所有安全性和效能修補程式 {#apply-all-security-and-performance-patches}

在凍結程式碼之前完成所有更新，以防止部署中斷。

## 執行假日前的健康情況檢查 {#run-pre-holiday-health-checks}

測試備份、cron健全狀況和快取熱身指令碼，以確保在負載下順利運作。

## 建立監控教戰手冊 {#establish-monitoring-playbooks}

記錄尖峰期間24x7回應的警示臨界值、向上呈報步驟及聯絡視窗。

## 檔案復原計畫 {#document-rollback-plans}

維護有版本的復原策略，以便從部署異常中快速復原。

