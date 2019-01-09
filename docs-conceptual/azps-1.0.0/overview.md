---
title: Azure PowerShell 的概觀
description: 概述 Azure PowerShell Az 模組，並有如何安裝和開始使用的相關資訊。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 10/29/2018
ms.openlocfilehash: 7982e122d49db4d558648231d1ab8bfeed80be2d
ms.sourcegitcommit: 4acddc7026522c4fe39de2c4424917d88ee01b7e
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/21/2018
ms.locfileid: "53736455"
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="9db6e-103">Azure PowerShell 的概觀</span><span class="sxs-lookup"><span data-stu-id="9db6e-103">Overview of Azure PowerShell</span></span>

<span data-ttu-id="9db6e-104">Azure PowerShell 提供了一組 Cmdlet，它們會使用 [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) 模型來管理 Azure 資源。</span><span class="sxs-lookup"><span data-stu-id="9db6e-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="9db6e-105">Azure PowerShell 會使用 .NET Standard，因此可供 Windows、macOS 和 Linux 使用。</span><span class="sxs-lookup"><span data-stu-id="9db6e-105">Azure PowerShell uses .NET Standard, making it available for Windows, macOS, and Linux.</span></span>
<span data-ttu-id="9db6e-106">Azure PowerShell 也可從 Azure Cloud Shell 取得。</span><span class="sxs-lookup"><span data-stu-id="9db6e-106">Azure PowerShell is also available from Azure Cloud Shell.</span></span>

<span data-ttu-id="9db6e-107">使用 [Azure Cloud Shell](/azure/cloud-shell/overview) 在瀏覽器中執行 Azure PowerShell，或將其[安裝到本機](install-az-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="9db6e-107">Use [Azure Cloud Shell](/azure/cloud-shell/overview) to run Azure PowerShell in your browser, or [install locally](install-az-ps.md).</span></span> <span data-ttu-id="9db6e-108">請參閱[開始使用](get-started-azureps.md)文章，以了解 Azure PowerShell 基本概念，並開始使用 Azure。</span><span class="sxs-lookup"><span data-stu-id="9db6e-108">Check out the [Get Started](get-started-azureps.md) article to learn the Azure PowerShell basics and get started with Azure.</span></span>

<span data-ttu-id="9db6e-109">如需最新 Azure PowerShell 版本的相關資訊，請參閱[版本資訊](release-notes-azureps.md)。</span><span class="sxs-lookup"><span data-stu-id="9db6e-109">For information about the latest Azure PowerShell release, see the [release notes](release-notes-azureps.md).</span></span>

## <a name="about-the-new-az-module"></a><span data-ttu-id="9db6e-110">關於新的 Az 模組</span><span class="sxs-lookup"><span data-stu-id="9db6e-110">About the new Az module</span></span>

<span data-ttu-id="9db6e-111">本文件說明適用於 Azure PowerShell 的新 Az 模組。</span><span class="sxs-lookup"><span data-stu-id="9db6e-111">This documentation describes the new Az module for Azure PowerShell.</span></span> <span data-ttu-id="9db6e-112">這個新模組是使用 .NET Standard 從頭開始撰寫的。</span><span class="sxs-lookup"><span data-stu-id="9db6e-112">This new module is written from the ground up in .NET Standard.</span></span> <span data-ttu-id="9db6e-113">使用 .NET Standard 可讓 Azure PowerShell 在 Windows 上的 PowerShell 5.x 或任何平台上的 PowerShell 6 底下執行。</span><span class="sxs-lookup"><span data-stu-id="9db6e-113">Using .NET Standard allows Azure PowerShell to run under PowerShell 5.x on Windows or PowerShell 6 on any platform.</span></span> <span data-ttu-id="9db6e-114">現在在透過 PowerShell 與 Azure 互動時，預期會採用 Az 模組。</span><span class="sxs-lookup"><span data-stu-id="9db6e-114">The Az module is now the intended way to interact with Azure through PowerShell.</span></span>
<span data-ttu-id="9db6e-115">AzureRM 仍可取得 Bug 修正，但不會再獲得新的功能。</span><span class="sxs-lookup"><span data-stu-id="9db6e-115">AzureRM will continue to get bug fixes, but no longer receive new features.</span></span>

<span data-ttu-id="9db6e-116">請到 [Azure PowerShell Az 模組簡介](new-azureps-module-az.md)來了解新模組的完整詳細資料，包括命令重新命名的情形以及 AzureRM 的維護計劃。</span><span class="sxs-lookup"><span data-stu-id="9db6e-116">Learn the full details about the new module, including how commands have been renamed and the maintenance plans for AzureRM, in the [Introducing the Azure PowerShell Az module](new-azureps-module-az.md).</span></span> <span data-ttu-id="9db6e-117">如果您想要立即開始使用新的模組，請參閱[從 AzureRM 遷移至 Az](migrate-from-azurerm-to-az.md)。</span><span class="sxs-lookup"><span data-stu-id="9db6e-117">If you want to get started with using the new module right away, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

<span data-ttu-id="9db6e-118">您也可以取得 [AzureRM 文件](/powershell/azure/azurerm)。</span><span class="sxs-lookup"><span data-stu-id="9db6e-118">The [AzureRM documentation](/powershell/azure/azurerm) is also available.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="9db6e-119">雖然 Azure 文件將會進行更新以反映新的模組 Cmdlet 名稱，但相關文章可能仍會使用 AzureRM 命令。</span><span class="sxs-lookup"><span data-stu-id="9db6e-119">While the Azure documentation is being updated to reflect the new module cmdlet names, articles may still use the AzureRM commands.</span></span> <span data-ttu-id="9db6e-120">在安裝 Az 模組之後，建議您使用 `Enable-AzureRmAlias` 啟用 AzureRM Cmdlet 別名。</span><span class="sxs-lookup"><span data-stu-id="9db6e-120">After installing the Az module, it's recommended that you enable the AzureRM cmdlet aliases with `Enable-AzureRmAlias`.</span></span> <span data-ttu-id="9db6e-121">請參閱[從 AzureRM 遷移至 Az](migrate-from-azurerm-to-az.md) 文章以取得詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9db6e-121">See the [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md) article for more details.</span></span>

## <a name="common-scenarios"></a><span data-ttu-id="9db6e-122">常見案例</span><span class="sxs-lookup"><span data-stu-id="9db6e-122">Common scenarios</span></span>

<span data-ttu-id="9db6e-123">下列範例可協助您了解如何使用 Azure PowerShell 來執行常見案例：</span><span class="sxs-lookup"><span data-stu-id="9db6e-123">The following samples can help you learn how to perform common scenarios with Azure PowerShell:</span></span>

* [<span data-ttu-id="9db6e-124">Linux 虛擬機器</span><span class="sxs-lookup"><span data-stu-id="9db6e-124">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="9db6e-125">Windows 虛擬機器</span><span class="sxs-lookup"><span data-stu-id="9db6e-125">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="9db6e-126">Web Apps</span><span class="sxs-lookup"><span data-stu-id="9db6e-126">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="9db6e-127">SQL Databases</span><span class="sxs-lookup"><span data-stu-id="9db6e-127">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="learn-powershell-basics"></a><span data-ttu-id="9db6e-128">了解 PowerShell 基本概念</span><span class="sxs-lookup"><span data-stu-id="9db6e-128">Learn PowerShell basics</span></span>

<span data-ttu-id="9db6e-129">如果您不熟悉 PowerShell，簡介可能會對您有所幫助。</span><span class="sxs-lookup"><span data-stu-id="9db6e-129">If you're unfamiliar with PowerShell, an introduction may be helpful.</span></span>

* [<span data-ttu-id="9db6e-130">安裝 PowerShell</span><span class="sxs-lookup"><span data-stu-id="9db6e-130">Installing PowerShell</span></span>](/powershell/scripting/setup/installing-windows-powershell)
* [<span data-ttu-id="9db6e-131">使用 PowerShell 編寫指令碼</span><span class="sxs-lookup"><span data-stu-id="9db6e-131">Scripting with PowerShell</span></span>](/powershell/scripting/powershell-scripting)

<span data-ttu-id="9db6e-132">您也可以觀看這段影片：[PowerShell 基本概念：(第 1 部份) 開始使用 PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1)。</span><span class="sxs-lookup"><span data-stu-id="9db6e-132">You can also watch this video: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span></span>

<span data-ttu-id="9db6e-133">或是參加 Microsoft Virtual Academy 的[開始使用 PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart)。</span><span class="sxs-lookup"><span data-stu-id="9db6e-133">Or attend the Microsoft Virtual Academy's [Getting Started with PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart).</span></span>

## <a name="build-your-skills-with-microsoft-learn"></a><span data-ttu-id="9db6e-134">透過 Microsoft Learn 增進您的技巧</span><span class="sxs-lookup"><span data-stu-id="9db6e-134">Build your skills with Microsoft Learn</span></span>

- [<span data-ttu-id="9db6e-135">使用 PowerShell 指令碼將 Azure 工作自動化</span><span class="sxs-lookup"><span data-stu-id="9db6e-135">Automate Azure tasks using scripts with PowerShell</span></span>](/learn/modules/automate-azure-tasks-with-powershell/)
- [<span data-ttu-id="9db6e-136">更多互動式學習...</span><span class="sxs-lookup"><span data-stu-id="9db6e-136">More interactive learning...</span></span>](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="9db6e-137">其他 Azure Powershell 模組</span><span class="sxs-lookup"><span data-stu-id="9db6e-137">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="9db6e-138">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="9db6e-138">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="9db6e-139">Azure 資訊保護</span><span class="sxs-lookup"><span data-stu-id="9db6e-139">Azure Information Protection</span></span>](/powershell/azure/aip/)
* [<span data-ttu-id="9db6e-140">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="9db6e-140">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="9db6e-141">Azure ElasticDB</span><span class="sxs-lookup"><span data-stu-id="9db6e-141">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)
