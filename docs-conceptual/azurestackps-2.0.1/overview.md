---
title: Azure Stack Hub Admin PowerShell 概觀 | Microsoft Docs
description: Azure Stack Hub Admin PowerShell 的概觀以及有關安裝和設定的指示。
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 06/22/2020
ms.openlocfilehash: f9bb71e19ecfe34f2c8646973f7a10526d2e8673
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/01/2020
ms.locfileid: "96427916"
---
# <a name="azure-stack-hub-module-201"></a><span data-ttu-id="2c95b-103">Azure Stack Hub 模組 2.0.1</span><span class="sxs-lookup"><span data-stu-id="2c95b-103">Azure Stack Hub Module 2.0.1</span></span>

## <a name="requirements"></a><span data-ttu-id="2c95b-104">需求：</span><span class="sxs-lookup"><span data-stu-id="2c95b-104">Requirements:</span></span>

<span data-ttu-id="2c95b-105">最低支援的 Azure Stack Hub 版本為 2002 版。</span><span class="sxs-lookup"><span data-stu-id="2c95b-105">Minimum supported Azure Stack Hub version is 2002.</span></span>

<span data-ttu-id="2c95b-106">注意:如需較舊版的 Azure Stack 請查看[安裝 Azure Stack Powershell](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span><span class="sxs-lookup"><span data-stu-id="2c95b-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="2c95b-107">安裝</span><span class="sxs-lookup"><span data-stu-id="2c95b-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue
Get-Module -Name Az.* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue

Install-Module -Name Az.BootStrapper -Force -AllowPrerelease

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 2.0.1-preview -AllowPrerelease
```


## <a name="release-notes"></a><span data-ttu-id="2c95b-108">版本資訊</span><span class="sxs-lookup"><span data-stu-id="2c95b-108">Release Notes</span></span>

* <span data-ttu-id="2c95b-109">由 2002 更新所支援。</span><span class="sxs-lookup"><span data-stu-id="2c95b-109">Supported with 2002 update.</span></span>  

  <span data-ttu-id="2c95b-110">Azure Stack Hub 2.0.0 是一個重大變更。</span><span class="sxs-lookup"><span data-stu-id="2c95b-110">The Azure Stack Hub 2.0.0 is a breaking change.</span></span> <span data-ttu-id="2c95b-111">此模組會使用 Az 模組，而不是 AzureRM 模組。</span><span class="sxs-lookup"><span data-stu-id="2c95b-111">The module uses the Az module rather than the AzureRM module.</span></span> <span data-ttu-id="2c95b-112">＜[在 Azure Stack Hub 中從 AzureRM 移轉至 Azure PowerShell Az](/azure-stack/operator/azure-stack-powershell-install)＞中有移轉指南和重大變更清單。</span><span class="sxs-lookup"><span data-stu-id="2c95b-112">You can find a migration guide and a list of breaking changes in [Migrate from AzureRM to Azure PowerShell Az in Azure Stack Hub](/azure-stack/operator/azure-stack-powershell-install).</span></span>