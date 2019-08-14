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
# <a name="azure-stack-module-172"></a><span data-ttu-id="a28ed-103">Azure Stack 模組 1.7.2</span><span class="sxs-lookup"><span data-stu-id="a28ed-103">Azure Stack Module 1.7.2</span></span>

## <a name="requirements"></a><span data-ttu-id="a28ed-104">需求：</span><span class="sxs-lookup"><span data-stu-id="a28ed-104">Requirements:</span></span>

<span data-ttu-id="a28ed-105">最低支援的 Azure Stack 版本為 1904 版。</span><span class="sxs-lookup"><span data-stu-id="a28ed-105">Minimum supported Azure Stack version is 1904.</span></span>

<span data-ttu-id="a28ed-106">注意：如需較舊版的 Azure Stack 請查看[安裝 Azure Stack Powershell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span><span class="sxs-lookup"><span data-stu-id="a28ed-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="a28ed-107">Install</span><span class="sxs-lookup"><span data-stu-id="a28ed-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Install-Module -Name AzureRM -RequiredVersion 2.5.0

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.7.2
```

## <a name="release-notes"></a><span data-ttu-id="a28ed-108">版本資訊</span><span class="sxs-lookup"><span data-stu-id="a28ed-108">Release Notes</span></span>

* <span data-ttu-id="a28ed-109">由 1904 更新所支援</span><span class="sxs-lookup"><span data-stu-id="a28ed-109">Supported with 1904 update</span></span>
* <span data-ttu-id="a28ed-110">這是重大變更版本。</span><span class="sxs-lookup"><span data-stu-id="a28ed-110">This a breaking change release.</span></span> <span data-ttu-id="a28ed-111">如需重大變更的詳細資訊，請參閱 <https://aka.ms/azspshmigration170></span><span class="sxs-lookup"><span data-stu-id="a28ed-111">For details on the breaking changes, refer to <https://aka.ms/azspshmigration170></span></span>
* <span data-ttu-id="a28ed-112">重大變更：備份對憑證型加密模式所做的變更。</span><span class="sxs-lookup"><span data-stu-id="a28ed-112">Breaking change: Backup changes to cert-based encryption mode.</span></span> <span data-ttu-id="a28ed-113">對於對稱金鑰的支援已被取代。</span><span class="sxs-lookup"><span data-stu-id="a28ed-113">Support for symmetric keys is deprecated.</span></span>
* <span data-ttu-id="a28ed-114">如需重大變更的詳細資訊，請參閱 https://aka.ms/azspshmigration170</span><span class="sxs-lookup"><span data-stu-id="a28ed-114">For details on the breaking changes, refer to https://aka.ms/azspshmigration170</span></span>
* <span data-ttu-id="a28ed-115">Azs.Storage.Admin 模組</span><span class="sxs-lookup"><span data-stu-id="a28ed-115">Azs.Storage.Admin Module</span></span> 
* <span data-ttu-id="a28ed-116">錯誤修正 - 如果未提供，則新的儲存體配額會使用預設值。</span><span class="sxs-lookup"><span data-stu-id="a28ed-116">Bug fix - New Storage Quota uses defaults if none provided.</span></span>
