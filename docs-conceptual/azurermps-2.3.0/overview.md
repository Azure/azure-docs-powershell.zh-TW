---
title: Azure Stack PowerShell 概觀 | Microsoft Docs
description: Azure Stack PowerShell 的概觀以及有關安裝和設定的指示。
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: cd415e862bfaa2b767cce108689ebaf34ef74305
ms.sourcegitcommit: 087c588169786c005a3c177624fb3ac6c8870125
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/13/2018
ms.locfileid: "53218148"
---
# <a name="azurerm-module-230"></a>AzureRM 模組 2.3.0

## <a name="requirements"></a>需求：
支援的最低 Azure Stack 版本為 1808 版。

注意：如果您使用的是舊版，請安裝版本 1.2.11


## <a name="install"></a>Install
```powershell-interactive
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module -Name AzureRM -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force -ErrorAction Continue
Uninstall-Module AzureRM.AzureStackStorage -Force -ErrorAction Continue
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force
Get-Module Azure.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

```

## <a name="release-notes"></a>版本資訊
* 2.3.0 版中有一些重大變更。 若要從 1.2.11 版升級，我們已建立移轉指南： https://aka.ms/azspowershellmigration
* 此版本對應到 azurestack 特有的 api 設定檔 2018-03-01-hybrid
* 所有模組皆取用比 AzureRm.Profile 模組上更大或相等的相依性。
* 每個模組支援的 API 版本都會更新。 
    * 計算 - 2017-03-30
    * 網路 - 2017-10-01
    * 儲存體 2016-01-01
    * 資源 - 2018-02-01
    * KeyVault - 2016-10-01
    * DNS - 2016-04-01
* 您可以在 https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json 中找到每個資源類型的完整 API 版本對應

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
Azure Stack 計算管理員模組的預覽版本可提供功能來管理計算配額、平台映像、受控磁碟和虛擬機器擴充功能。

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
