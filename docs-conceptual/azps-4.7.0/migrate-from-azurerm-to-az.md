---
title: 將 Azure PowerShell 指令碼從 AzureRM 遷移至 Az
description: 了解將指令碼從 AzureRM 模組遷移至新 Az 模組所用的步驟和工具。
ms.devlang: powershell
ms.service: azure-powershell
ms.topic: conceptual
ms.date: 10/12/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 2f3b6a55b3c674a6030a1d3568e57cdb15c43b02
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "92001559"
---
# <a name="migrate-azure-powershell-from-azurerm-to-az"></a><span data-ttu-id="39112-103">將 Azure PowerShell 從 AzureRM 移轉至 Az</span><span class="sxs-lookup"><span data-stu-id="39112-103">Migrate Azure PowerShell from AzureRM to Az</span></span>

<span data-ttu-id="39112-104">所有 AzureRM PowerShell 模組的版本已過時，但依然可支援。</span><span class="sxs-lookup"><span data-stu-id="39112-104">All versions of the AzureRM PowerShell module are outdated, but not out of support.</span></span> <span data-ttu-id="39112-105">[Az PowerShell 模組](install-az-ps.md)現在是用來與 Azure 互動的建議 PowerShell 模組。</span><span class="sxs-lookup"><span data-stu-id="39112-105">The [Az PowerShell module](install-az-ps.md) is now the recommended PowerShell module for interacting with Azure.</span></span>

<span data-ttu-id="39112-106">針對 AzureRM Cmdlet 撰寫的指令碼不會自動使用新模組。</span><span class="sxs-lookup"><span data-stu-id="39112-106">Scripts written for the AzureRM cmdlets won't automatically work with the new module.</span></span> <span data-ttu-id="39112-107">為了更輕鬆地轉換，已開發 [AzureRM 至 Az 移轉工具組](https://github.com/Azure/azure-powershell-migration)。</span><span class="sxs-lookup"><span data-stu-id="39112-107">To make the transition easier, the [AzureRM to Az migration toolkit](https://github.com/Azure/azure-powershell-migration) was developed.</span></span> <span data-ttu-id="39112-108">不移轉移到新命令集當然很方便，但本文將會協助您開始轉換到 Az PowerShell 模組。</span><span class="sxs-lookup"><span data-stu-id="39112-108">No migration to a new command set is ever convenient, but this article will help you get started on transitioning to the Az PowerShell module.</span></span> <span data-ttu-id="39112-109">若要深入了解為何會建立 Az PowerShell 模組，請參閱[新的 Azure PowerShell Az 模組簡介](new-azureps-module-az.md)。</span><span class="sxs-lookup"><span data-stu-id="39112-109">To learn more about why the Az PowerShell module was created, see [Introducing the new Azure PowerShell Az module](new-azureps-module-az.md).</span></span>

<span data-ttu-id="39112-110">若要查看 AzureRM 和 Az 之間重大變更的完整清單，請參閱[從 AzureRM 到 Az 的完整變更](migrate-az-1.0.0.md)。</span><span class="sxs-lookup"><span data-stu-id="39112-110">To see the full list of breaking changes between AzureRM and Az, see the [full changes from AzureRM to Az](migrate-az-1.0.0.md).</span></span>

## <a name="ensure-existing-scripts-work-with-the-latest-azurerm-release"></a><span data-ttu-id="39112-111">確定現有指令碼可使用最新的 AzureRM 版本</span><span class="sxs-lookup"><span data-stu-id="39112-111">Ensure existing scripts work with the latest AzureRM release</span></span>

<span data-ttu-id="39112-112">在採取任何移轉步驟之前，請先檢查系統上安裝了哪些版本的 AzureRM。</span><span class="sxs-lookup"><span data-stu-id="39112-112">Before taking any migration steps, check which versions of AzureRM are installed on your system.</span></span>
<span data-ttu-id="39112-113">進行檢查可讓您確定指令碼是在最新的版本上執行，而且可讓您知道必須解除安裝哪些版本的 AzureRM。</span><span class="sxs-lookup"><span data-stu-id="39112-113">Doing so allows you to make sure scripts are already running on the latest release, and let you know which versions of AzureRM must be uninstalled.</span></span>

<span data-ttu-id="39112-114">若要檢查您所安裝的 AzureRM 版本，請執行下列範例：</span><span class="sxs-lookup"><span data-stu-id="39112-114">To check which version(s) of AzureRM you have installed, run the following example:</span></span>

```azurepowershell
Get-Module -Name AzureRM -ListAvailable -All
```

<span data-ttu-id="39112-115">AzureRM **最新的**可用版本為 **6.13.1**。</span><span class="sxs-lookup"><span data-stu-id="39112-115">The **latest** available release of AzureRM is **6.13.1**.</span></span> <span data-ttu-id="39112-116">如果您未安裝此版本，您現有的指令碼可能需要進行其他修改，才能使用本文和[重大變更清單](migrate-az-1.0.0.md)中未列出的 Az 模組。</span><span class="sxs-lookup"><span data-stu-id="39112-116">If you don't have this version installed, your existing scripts may need additional modifications to work with the Az module beyond what's described in this article and in the [breaking changes list](migrate-az-1.0.0.md).</span></span>

<span data-ttu-id="39112-117">如果您的指令碼無法使用 AzureRM 6.13.1，請根據[從 AzureRM 5.x 移轉至 6.x 的指南](/powershell/azure/azurerm/migration-guide.6.0.0)加以更新。</span><span class="sxs-lookup"><span data-stu-id="39112-117">If your scripts don't work with AzureRM 6.13.1, update them according to the [AzureRM 5.x to 6.x migration guide](/powershell/azure/azurerm/migration-guide.6.0.0).</span></span> <span data-ttu-id="39112-118">如果您使用舊版的 AzureRM 模組，請參考各個主要版本適用的移轉指南。</span><span class="sxs-lookup"><span data-stu-id="39112-118">If you use an earlier version of the AzureRM module, there are migration guides available for each major version.</span></span>

## <a name="install-the-azurerm-to-az-migration-toolkit"></a><span data-ttu-id="39112-119">安裝 AzureRM 至 Az 移轉工具組</span><span class="sxs-lookup"><span data-stu-id="39112-119">Install the AzureRM to Az migration toolkit</span></span>

```azurepowershell
Install-Module -Name Az.Tools.Migration
```

## <a name="automatically-migrate-your-powershell-scripts"></a><span data-ttu-id="39112-120">自動遷移您的 PowerShell 指令碼</span><span class="sxs-lookup"><span data-stu-id="39112-120">Automatically migrate your PowerShell scripts</span></span>

<span data-ttu-id="39112-121">透過 AzureRM 至 Az 移轉工具組，您可以產生一個計劃，以判斷在對指令碼進行任何修改之前，以及在安裝 Az PowerShell 模組之前，要對其執行哪些變更。</span><span class="sxs-lookup"><span data-stu-id="39112-121">With the AzureRM to Az migration toolkit, you can generate a plan to determine what changes will be performed on your scripts before making any modifications to them and before installing the Az PowerShell module.</span></span>

<span data-ttu-id="39112-122">[將 PowerShell 指令碼從 AzureRM 自動遷移至 Az PowerShell 模組](quickstart-migrate-azurerm-to-az-automatically.md)快速入門，會逐步引導您完成從 AzureRM 至 Az PowerShell 模組自動更新 PowerShell 指令碼的整個程序。</span><span class="sxs-lookup"><span data-stu-id="39112-122">The [Automatically migrate PowerShell scripts from AzureRM to the Az PowerShell module](quickstart-migrate-azurerm-to-az-automatically.md) quickstart walks you through the entire process of automatically updating your PowerShell scripts from AzureRM to the Az PowerShell module.</span></span>

## <a name="next-steps"></a><span data-ttu-id="39112-123">後續步驟</span><span class="sxs-lookup"><span data-stu-id="39112-123">Next steps</span></span>

<span data-ttu-id="39112-124">[安裝 Azure PowerShell](install-az-ps.md)
[解除安裝 AzureRM](uninstall-az-ps.md#uninstall-the-azurerm-module)</span><span class="sxs-lookup"><span data-stu-id="39112-124">[Install Azure PowerShell](install-az-ps.md)
[Uninstall AzureRM](uninstall-az-ps.md#uninstall-the-azurerm-module)</span></span>
