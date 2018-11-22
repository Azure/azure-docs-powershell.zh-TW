---
title: Azure Stack Admin PowerShell 概觀 | Microsoft Docs
description: Azure Stack Admin PowerShell 的概觀以及有關安裝和設定的指示。
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: 72d147f5bc9c882083dda6b33b1c89663fd2eb34
ms.sourcegitcommit: 80a3da199954d0ab78765715fb49793e89a30f12
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/22/2018
ms.locfileid: "52257987"
---
# <a name="azure-stack-module-140"></a>Azure Stack 模組 1.4.0

## <a name="requirements"></a>需求：
支援的最低 Azure Stack 版本為 1804 版。

請注意：如果您使用的是舊版，請安裝版本 1.2.11

## <a name="known-issues"></a>已知問題：

- 需要 Azure Stack 1803 版本才能關閉警示
- New-AzsOffer 不允許建立具公用狀態的供應項目。 Set-AzsOffer Cmdlet 之後需要呼叫以變更狀態。
- 必須重新部署才能移除 IP 集區

## <a name="breaking-changes"></a>重大變更
自版本 1.3.0 以來均無重大變更。 從 1.2.11 移轉的所有中斷性變更記錄於此 https://aka.ms/azspowershellmigration

## <a name="install"></a>Install
```
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force
Uninstall-Module AzureRM.AzureStackStorage -Force
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2017-03-09-profile -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.4.0
```
## <a name="release-notes"></a>版本資訊
    * Azurestack 1.4.0 版本自先前版本 1.3.0 以來並無重大變更
    * Azs.AzureBridge.Admin
        - 修正在分頁結果中僅傳送單一頁面的 BUG
    * Azs.Backup.Admin
        - 已將 BackupFrequencyInHours、IsBackupSchedulerEnabled 及 BackupRetentionPeriodInDays 等新參數新增至 Cmdlet Set-AzsBackupShare
        - 已新增 Cmdlet New-EncyptionKeyBase64，以協助建立加密金鑰
        - 修正在分頁結果中僅傳送單一頁面的 BUG
    * Azs.Commerce.Admin
        - 修正在分頁結果中僅傳送單一頁面的 BUG
    * Azs.Fabric.Admin
        - 修正在分頁結果中僅傳送單一頁面的 BUG
        - 已新增 Cmdlet Add-AzsScaleUnitNode，讓管理員可將新的縮放單位節點新增至 azurestack 戳記
        - 已新增 Cmdlet 和 New-AzsScaleUnitNodeObject，以協助建立縮放單位參數物件
    * Azs.Gallery.Admin
        - 修正在分頁結果中僅傳送單一頁面的 BUG
    * Azs.InfrastructureInsights.Admin
        - 修正在分頁結果中僅傳送單一頁面的 BUG
    * Azs.Network.Admin
        - 修正在分頁結果中僅傳送單一頁面的 BUG
    * Azs.Update.Admin
        - 修正在分頁結果中僅傳送單一頁面的 BUG
    * Azs.Subscriptions
        - 修正在分頁結果中僅傳送單一頁面的 BUG
    * Azs.Subscriptions.Admin
        - 已新增 Cmdlet Move-AzsSubscription，以便在受委派的提供者供應項目之間移動訂用帳戶
        - 已新增 Cmdlet Test-AzsMoveSubscription，以便驗證該使用者訂用帳戶可以在受委派的提供者供應項目之間移動
        - 修正在分頁結果中僅傳送單一頁面的 BUG

## <a name="content"></a>內容：
### <a name="azure-bridge"></a>Azure Bridge
Azure Stack AzureBridge 管理員模組的預覽版本可讓您從 Azure 同步發佈映像。

### <a name="backup"></a>Backup 
備份管理員模組的預覽版本可允許管理員：
- 設定備份的儲存位置
- 執行備份
- 列出並還原已完成的備份

### <a name="commerce"></a>商業
Azure Stack 商務管理員模組的預覽版本可提供方法來檢視 Azure Stack 系統間的彙總資料使用量。

### <a name="compute"></a>計算
Azure Stack 計算管理員模組的預覽版本可提供功能來管理計算配額、平台映像和虛擬機器擴充功能。

### <a name="fabric"></a>網狀架構
Azure Stack 網狀架構管理員模組的預覽版本可讓系統管理員檢視和管理基礎結構元件：
- 縮放單位節點的停止、啟動和關閉
- 針對 FRU 相關活動清空和繼續縮放單位節點
- 縮放單位節點修復
- 基礎結構角色重新啟動
- 基礎結構角色執行個體的停止、啟動和關閉
- 建立新的 IP 集區

### <a name="gallery"></a>資源庫
Azure Stack 資源庫管理員模組的預覽版本可提供功能來管理 Azure Stack 市集中的資源庫項目。

### <a name="infrastructure-insights"></a>基礎結構深入解析
基礎結構深入解析管理員模組的預覽版本可讓系統管理員：
- 檢視其 Azure Stack 戳記資源的健康情況
- 檢視和管理警示

### <a name="keyvault"></a>KeyVault
Azure Stack KeyVault 管理員模組的預覽版本可讓系統管理員檢視 KeyVault 配額。

### <a name="network"></a>網路
網路管理員模組的預覽版本可以執行：
- 網路配額管理
- 檢視配置的網路資源，例如公用 IP 位址、虛擬網路、負載平衡器
- 提供 Cmdlet 以顯示系統管理員概觀

### <a name="storage"></a>儲存體
Azure Stack 儲存體管理員模組的預覽版本。  在此版本中，我們提供的功能有：
- 管理儲存體配額
- 記憶體回收刪除的儲存體資源
- 還原已刪除的儲存體帳戶
- 將容器從一個共用遷移到另一個
- 檢視個別儲存元件的相關資訊
- 檢視使用量和效能資訊

### <a name="subscription-admin"></a>訂用帳戶管理員
Azure Stack 訂用帳戶管理員模組的預覽版本。  此模組可提供功能讓系統管理員：
- 管理方案和供應項目
- 檢視使用量和效能資訊
- 管理 RBAC

### <a name="subscription"></a>訂用帳戶
Azure Stack 訂用帳戶模組的預覽版本。  此模組可提供功能讓使用者：
- 建立、刪除和更新訂用帳戶

### <a name="update"></a>更新
Azure Stack 更新管理員模組的預覽版本。  在此模組中系統管理員可以：
- 列出及安裝可用更新
- 繼續中斷的更新
- 檢視已安裝的更新
