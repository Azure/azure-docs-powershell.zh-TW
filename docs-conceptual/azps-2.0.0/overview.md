---
title: Azure PowerShell 的概觀
description: 概述 Azure PowerShell Az 模組，並有如何安裝和開始使用的相關資訊。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 01/10/2019
ms.openlocfilehash: 45ab083dd133c8c7b8dbe902484c92564bc216b9
ms.sourcegitcommit: accff0c2cd6035fcda2d917f6051a5b509eb6255
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/06/2019
ms.locfileid: "65048745"
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="27166-103">Azure PowerShell 的概觀</span><span class="sxs-lookup"><span data-stu-id="27166-103">Overview of Azure PowerShell</span></span>

<span data-ttu-id="27166-104">Azure PowerShell 提供了一組 Cmdlet，它們會使用 [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) 模型來管理 Azure 資源。</span><span class="sxs-lookup"><span data-stu-id="27166-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="27166-105">Azure PowerShell 會使用 .NET Standard，因此可供 Windows、macOS 和 Linux 使用。</span><span class="sxs-lookup"><span data-stu-id="27166-105">Azure PowerShell uses .NET Standard, making it available for Windows, macOS, and Linux.</span></span>
<span data-ttu-id="27166-106">Azure PowerShell 也可在 Azure Cloud Shell 取得。</span><span class="sxs-lookup"><span data-stu-id="27166-106">Azure PowerShell is also available on Azure Cloud Shell.</span></span>

## <a name="about-the-new-az-module"></a><span data-ttu-id="27166-107">關於新的 Az 模組</span><span class="sxs-lookup"><span data-stu-id="27166-107">About the new Az module</span></span>

<span data-ttu-id="27166-108">本文件說明適用於 Azure PowerShell 的新 Az 模組。</span><span class="sxs-lookup"><span data-stu-id="27166-108">This documentation describes the new Az module for Azure PowerShell.</span></span> <span data-ttu-id="27166-109">這個新模組是使用 .NET Standard 從頭開始撰寫的。</span><span class="sxs-lookup"><span data-stu-id="27166-109">This new module is written from the ground up in .NET Standard.</span></span> <span data-ttu-id="27166-110">使用 .NET Standard 可讓 Azure PowerShell 在 Windows 上的 PowerShell 5 或任何平台上的 PowerShell 6 底下執行。</span><span class="sxs-lookup"><span data-stu-id="27166-110">Using .NET Standard allows Azure PowerShell to run under PowerShell 5 on Windows or PowerShell 6 on any platform.</span></span> <span data-ttu-id="27166-111">現在在透過 PowerShell 與 Azure 互動時，預期會採用 Az 模組。</span><span class="sxs-lookup"><span data-stu-id="27166-111">The Az module is now the intended way to interact with Azure through PowerShell.</span></span>
<span data-ttu-id="27166-112">AzureRM 仍可取得 Bug 修正，但不會再獲得新的功能。</span><span class="sxs-lookup"><span data-stu-id="27166-112">AzureRM will continue to get bug fixes, but no longer receive new features.</span></span>

<span data-ttu-id="27166-113">請到 [Azure PowerShell Az 模組簡介](new-azureps-module-az.md)來了解新模組的完整詳細資料，包括命令重新命名的情形以及 AzureRM 的維護計劃。</span><span class="sxs-lookup"><span data-stu-id="27166-113">Learn the full details about the new module, including how commands have been renamed and the maintenance plans for AzureRM, in the [Introducing the Azure PowerShell Az module](new-azureps-module-az.md).</span></span> <span data-ttu-id="27166-114">如果您想要立即開始使用新的模組，請參閱[從 AzureRM 遷移至 Az](migrate-from-azurerm-to-az.md)。</span><span class="sxs-lookup"><span data-stu-id="27166-114">If you want to get started with using the new module right away, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

<span data-ttu-id="27166-115">您也可以取得 [AzureRM 文件](/powershell/azure/azurerm)。</span><span class="sxs-lookup"><span data-stu-id="27166-115">The [AzureRM documentation](/powershell/azure/azurerm) is also available.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="27166-116">雖然 Azure 文件將會進行更新以反映新的模組 Cmdlet 名稱，但相關文章可能仍會使用 AzureRM 命令。</span><span class="sxs-lookup"><span data-stu-id="27166-116">While the Azure documentation is being updated to reflect the new module cmdlet names, articles may still use the AzureRM commands.</span></span> <span data-ttu-id="27166-117">在安裝 Az 模組之後，建議您使用 `Enable-AzureRmAlias` 啟用 AzureRM Cmdlet 別名。</span><span class="sxs-lookup"><span data-stu-id="27166-117">After installing the Az module, it's recommended that you enable the AzureRM cmdlet aliases with `Enable-AzureRmAlias`.</span></span> <span data-ttu-id="27166-118">請參閱[從 AzureRM 遷移至 Az](migrate-from-azurerm-to-az.md) 文章以取得詳細資料。</span><span class="sxs-lookup"><span data-stu-id="27166-118">See the [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md) article for more details.</span></span>

## <a name="run-or-install"></a><span data-ttu-id="27166-119">執行或安裝</span><span class="sxs-lookup"><span data-stu-id="27166-119">Run or install</span></span>

<span data-ttu-id="27166-120">您可以在 Windows 的 PowerShell 5.1 或更高版本，或任何平台的 PowerShell 6 上安裝 Azure PowerShell，或是在 Azure Cloud Shell 中加以執行。</span><span class="sxs-lookup"><span data-stu-id="27166-120">You can install Azure PowerShell on PowerShell 5.1 or higher on Windows, PowerShell 6 on any platform, or run in Azure Cloud Shell.</span></span>

* <span data-ttu-id="27166-121">若要在您的瀏覽器中使用 Azure Cloud Shell 執行，請參閱 [Azure Cloud Shell 中的 PowerShell 快速入門](/azure/cloud-shell/quickstart-powershell)。</span><span class="sxs-lookup"><span data-stu-id="27166-121">To run in your browser with Azure Cloud Shell, see [Quickstart for PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span></span>
* <span data-ttu-id="27166-122">若要在您的系統上安裝 Azure PowerShell，請參閱[安裝 Azure PowerShell](install-az-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="27166-122">To install Azure PowerShell on your system, see [Install Azure PowerShell](install-az-ps.md).</span></span>

<span data-ttu-id="27166-123">如需最新 Azure PowerShell 版本的相關資訊，請參閱[版本資訊](release-notes-azureps.md)。</span><span class="sxs-lookup"><span data-stu-id="27166-123">For information about the latest Azure PowerShell release, see the [release notes](release-notes-azureps.md).</span></span>

## <a name="get-started"></a><span data-ttu-id="27166-124">開始使用</span><span class="sxs-lookup"><span data-stu-id="27166-124">Get Started</span></span>

<span data-ttu-id="27166-125">請參閱[開始使用 Azure PowerShell](get-started-azureps.md) 文章，以了解 Azure PowerShell 基本概念。</span><span class="sxs-lookup"><span data-stu-id="27166-125">Read the [Get Started with Azure PowerShell](get-started-azureps.md) article to learn the Azure PowerShell basics.</span></span> <span data-ttu-id="27166-126">如果您不熟悉 PowerShell，簡介可能會對您有所幫助：</span><span class="sxs-lookup"><span data-stu-id="27166-126">If you're not familiar with PowerShell, an introduction might be helpful:</span></span>

* [<span data-ttu-id="27166-127">安裝 PowerShell</span><span class="sxs-lookup"><span data-stu-id="27166-127">Install PowerShell</span></span>](/powershell/scripting/install/installing-powershell)
* [<span data-ttu-id="27166-128">使用 PowerShell 編寫指令碼</span><span class="sxs-lookup"><span data-stu-id="27166-128">Scripting with PowerShell</span></span>](/powershell/scripting/powershell-scripting)
* [<span data-ttu-id="27166-129">PowerShell 基本概念：(第 1 部份) 開始使用 PowerShell</span><span class="sxs-lookup"><span data-stu-id="27166-129">PowerShell Basics: (Part 1) Getting Started with PowerShell</span></span>](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1)
* <span data-ttu-id="27166-130">Microsoft Virtual Academy 的[開始使用 PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart)</span><span class="sxs-lookup"><span data-stu-id="27166-130">Microsoft Virtual Academy's [Getting Started with PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart)</span></span>

<span data-ttu-id="27166-131">下列範例說明 Azure 的一些常見用法：</span><span class="sxs-lookup"><span data-stu-id="27166-131">The following samples can help you with some common uses of Azure:</span></span>

* [<span data-ttu-id="27166-132">Linux 虛擬機器</span><span class="sxs-lookup"><span data-stu-id="27166-132">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="27166-133">Windows 虛擬機器</span><span class="sxs-lookup"><span data-stu-id="27166-133">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="27166-134">Web Apps</span><span class="sxs-lookup"><span data-stu-id="27166-134">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="27166-135">SQL Databases</span><span class="sxs-lookup"><span data-stu-id="27166-135">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="build-your-skills-with-microsoft-learn"></a><span data-ttu-id="27166-136">透過 Microsoft Learn 增進您的技巧</span><span class="sxs-lookup"><span data-stu-id="27166-136">Build your skills with Microsoft Learn</span></span>

- [<span data-ttu-id="27166-137">使用 PowerShell 指令碼將 Azure 工作自動化</span><span class="sxs-lookup"><span data-stu-id="27166-137">Automate Azure tasks using scripts with PowerShell</span></span>](/learn/modules/automate-azure-tasks-with-powershell/)
- [<span data-ttu-id="27166-138">更多互動式學習...</span><span class="sxs-lookup"><span data-stu-id="27166-138">More interactive learning...</span></span>](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="27166-139">其他 Azure Powershell 模組</span><span class="sxs-lookup"><span data-stu-id="27166-139">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="27166-140">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="27166-140">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="27166-141">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="27166-141">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="27166-142">Azure ElasticDB</span><span class="sxs-lookup"><span data-stu-id="27166-142">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)
