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
ms.openlocfilehash: 1b3d707e862dd0c21e9e6b0a89f429ff21b1a99d
ms.sourcegitcommit: b02cbcd00748a4a9a4790a5fba229ce53c3bf973
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/09/2019
ms.locfileid: "68861336"
---
# <a name="azure-stack-module-172"></a>Azure Stack 模組 1.7.2

## <a name="requirements"></a>需求：

最低支援的 Azure Stack 版本為 1904 版。

注意：如需較舊版的 Azure Stack 請查看[安裝 Azure Stack Powershell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)

## <a name="install"></a>Install

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Install-Module -Name AzureRM -RequiredVersion 2.5.0

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.7.2
```

## <a name="release-notes"></a>版本資訊

* 由 1904 更新所支援
* 這是重大變更版本。 如需重大變更的詳細資訊，請參閱 <https://aka.ms/azspshmigration170>
* 重大變更：備份對憑證型加密模式所做的變更。 對於對稱金鑰的支援已被取代。
* 如需重大變更的詳細資訊，請參閱 https://aka.ms/azspshmigration170
* Azs.Storage.Admin 模組 
* 錯誤修正 - 如果未提供，則新的儲存體配額會使用預設值。
