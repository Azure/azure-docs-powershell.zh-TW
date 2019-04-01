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
ms.openlocfilehash: 3daf7746dfc0e06c62209be0ffa164d657d91935
ms.sourcegitcommit: 4153218b2b51e42d6c3315bb7f0fcbcfac7d1f86
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/29/2019
ms.locfileid: "58616981"
---
# <a name="azure-stack-module-170"></a>Azure Stack Module 1.7.0

## <a name="requirements"></a>需求：

最低支援的 Azure Stack 版本為 1901 版。

注意：如需較舊版的 Azure Stack 請查看[安裝 Azure Stack Powershell](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)

## <a name="install"></a>Install

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Install-Module -Name AzureRM -RequiredVersion 2.4.0

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.7.0
```

## <a name="release-notes"></a>版本資訊

* 由 1901 更新所支援
* 這是重大變更版本。 如需重大變更的詳細資訊，請參閱 <https://aka.ms/azspshmigration170>
* Azs.Backup.Admin 模組 * 重大變更：備份對憑證型加密模式所做的變更。 對於對稱金鑰的支援已被取代。
* Azs.Fabric.Admin Module       * 描述           * Get-AzsInfrastructureVolume 已淘汰，我們提供新的 Cmdlet Get-AzsVolume           * Get-AzsStorageSystem 已淘汰，我們提供新的 Cmdlet Get-AzsStorageSubSystem           * Get-AzsStoragePool 已淘汰，StorageSubSystem 物件具備容量屬性
* Azs.Compute.Admin 模組           * 錯誤修正：Add-AzsPlatformImage，Get-AzsPlatformImage：只在成功的路徑呼叫 ConvertTo-PlatformImageObject           * 錯誤修正：Add-AzsVmExtension，Get-AzsVmExtension：只在成功的路徑呼叫 ConvertTo-VmExtensionObject
* Azs.Storage.Admin 模組Module           * 錯誤修正 - 若未提供，新的儲存體配額會使用預設值。」
