---
title: Azure Stack Admin PowerShell 概觀 | Microsoft Docs
description: Azure Stack Admin PowerShell 的概觀以及有關安裝和設定的指示。
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 02/06/2019
ms.openlocfilehash: af0343e5ad92fa7f2b5c10e3e67cb7e10feb81c6
ms.sourcegitcommit: 0fdccb57a356b6e7c35a77b1f76e01fb96ef582b
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/17/2019
ms.locfileid: "65855783"
---
# <a name="azure-stack-module-172"></a>Azure Stack 模組 1.7.2

## <a name="requirements"></a>需求：

最低支援的 Azure Stack 版本為 1904 版。

注意：如需較舊版的 Azure Stack 請查看[安裝 Azure Stack Powershell](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)

## <a name="install-powershell-for-azure-stack"></a>安裝適用於 Azure Stack 的 PowerShell

安裝有三個步驟：

1. 安裝 Azure Stack PowerShell 取決於 Azure Stack 的版本而定
2. 啟用其他儲存體功能
3. 確認 PowerShell 的安裝

### <a name="install-azure-stack-powershell"></a>安裝 Azure Stack PowerShell

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install the AzureRM.BootStrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRM.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Get-AzureRmProfile -Update
Use-AzureRmProfile -Profile 2019-03-01-hybrid -Force
Install-Module -Name AzureStack -RequiredVersion 1.7.2
```

### <a name="enable-additional-storage-features"></a>啟用其他儲存體功能

```
# Install the Azure.Storage module version 4.5.0
Install-Module -Name Azure.Storage -RequiredVersion 4.5.0 -Force -AllowClobber

# Install the AzureRm.Storage module version 5.0.4
Install-Module -Name AzureRM.Storage -RequiredVersion 5.0.4 -Force -AllowClobber

# Remove incompatible storage module installed by AzureRM.Storage
Uninstall-Module Azure.Storage -RequiredVersion 4.6.1 -Force

# Load the modules explicitly specifying the versions
Import-Module -Name Azure.Storage -RequiredVersion 4.5.0
Import-Module -Name AzureRM.Storage -RequiredVersion 5.0.4
```

## <a name="release-notes"></a>版本資訊

* 由 1904 更新所支援
* 這是重大變更版本。 如需重大變更的詳細資訊，請參閱 <https://aka.ms/azspshmigration170>
* Azs.Backup.Admin 模組 * 重大變更：備份對憑證型加密模式所做的變更。 對於對稱金鑰的支援已被取代。
* Azs.Fabric.Admin Module       * 描述           * Get-AzsInfrastructureVolume 已淘汰，我們提供新的 Cmdlet Get-AzsVolume           * Get-AzsStorageSystem 已淘汰，我們提供新的 Cmdlet Get-AzsStorageSubSystem           * Get-AzsStoragePool 已淘汰，StorageSubSystem 物件具備容量屬性
* Azs.Compute.Admin 模組           * 錯誤修正：Add-AzsPlatformImage，Get-AzsPlatformImage：只在成功的路徑呼叫 ConvertTo-PlatformImageObject           * 錯誤修正：Add-AzsVmExtension，Get-AzsVmExtension：只在成功的路徑呼叫 ConvertTo-VmExtensionObject
* Azs.Storage.Admin 模組Module           * 錯誤修正 - 若未提供，新的儲存體配額會使用預設值。」
