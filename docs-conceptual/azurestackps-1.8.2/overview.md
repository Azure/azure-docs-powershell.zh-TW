---
title: Azure Stack Admin PowerShell 概觀 | Microsoft Docs
description: Azure Stack Admin PowerShell 的概觀以及有關安裝和設定的指示。
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 08/06/2020
ms.openlocfilehash: e314374eff433d1869378bdaa9a0370c3fd3d8d1
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "88022927"
---
# <a name="azure-stack-module-182"></a>Azure Stack 模組 1.8.2

## <a name="requirements"></a>需求：

最低支援的 Azure Stack 版本為 1910 版。

注意:如需較舊版的 Azure Stack 請查看[安裝 Azure Stack Powershell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)

## <a name="install"></a>安裝

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.8.2
```

## <a name="release-notes"></a>版本資訊

* 由 1910 更新所支援
