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
ms.openlocfilehash: b0e85bec82b9b7c876b2bbf337b603c8d68cf6a3
ms.sourcegitcommit: 4e1174236796e7da929ff276addb32e42c18b707
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/12/2019
ms.locfileid: "54240130"
---
# <a name="azure-stack-module-160"></a>Azure Stack 模組 1.6.0

## <a name="requirements"></a>需求：
支援的最低 Azure Stack 版本為 1811 版。

注意：如果您使用的是舊版，請安裝版本 1.6.0

## <a name="install"></a>Install
```
# Remove previous versions of AzureStack and AzureRM modules
Uninstall-Module -Name AzureRM -Force
Uninstall-Module -Name Azure.Storage -Force
Uninstall-Module -Name AzureStack -Force
Get-Module -Name "Azs*" -ListAvailable | Uninstall-Module  -Force 
Get-Module -Name "AzureRm*" -ListAvailable | Uninstall-Module  -Force

# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.6.0
```

## <a name="release-notes"></a>版本資訊
* 由 1811 更新所支援
* Azs.Compute.Admin 模組
    * 修正 New-DataDiskObject 遺漏 Azs 前置詞的問題，並新增別名及未來將有取代項目的警告。
* Azs.Update.Admin 模組
    * 新增警告，建議您在執行 Install-AzsUpdate 之前先執行 Test-AzureStack
* Azs.Fabric.Admin
    * 新 Cmdlet (Azure Stack 1811+ 支援的功能)
        * Get-AzsDrive
        * Get-AzsVolume
        * Get-AzsStorageSubSystem
    * 淘汰
        * Get-AzsInfrastructureVolume 現在是 Get-AzsVolume Cmdlet 的別名
* Azs.InfrastructureInsights.Admin
    *  新增 Repair-AzsAlert Cmdlet
* Azs.Storage.Admin
    * 修正未使用預設配額值的錯誤
* Azs.Subscriptions.Admin 模組
    * 修正 New-AddonPlanDefinitionObject 遺漏 Azs 前置詞的問題，並新增別名及未來將有取代項目的警告。
