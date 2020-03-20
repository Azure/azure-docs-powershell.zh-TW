---
title: Azure Stack Admin PowerShell 概觀 | Microsoft Docs
description: Azure Stack Admin PowerShell 的概觀以及有關安裝和設定的指示。
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 03/04/2020
ms.openlocfilehash: ef034424c72d88b3ceb28956da9ca56e4a7f3941
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2020
ms.locfileid: "79402709"
---
# <a name="azure-stack-module-181"></a><span data-ttu-id="422a7-103">Azure Stack 模組 1.8.1</span><span class="sxs-lookup"><span data-stu-id="422a7-103">Azure Stack Module 1.8.1</span></span>

## <a name="requirements"></a><span data-ttu-id="422a7-104">需求：</span><span class="sxs-lookup"><span data-stu-id="422a7-104">Requirements:</span></span>

<span data-ttu-id="422a7-105">最低支援的 Azure Stack 版本為 1910 版。</span><span class="sxs-lookup"><span data-stu-id="422a7-105">Minimum supported Azure Stack version is 1910.</span></span>

<span data-ttu-id="422a7-106">注意:如需較舊版的 Azure Stack 請查看[安裝 Azure Stack Powershell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span><span class="sxs-lookup"><span data-stu-id="422a7-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="422a7-107">安裝</span><span class="sxs-lookup"><span data-stu-id="422a7-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.8.1
```

## <a name="release-notes"></a><span data-ttu-id="422a7-108">版本資訊</span><span class="sxs-lookup"><span data-stu-id="422a7-108">Release Notes</span></span>

* <span data-ttu-id="422a7-109">由 1910 更新所支援</span><span class="sxs-lookup"><span data-stu-id="422a7-109">Supported with 1910 update</span></span>
