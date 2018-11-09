---
title: Azure PowerShell 概觀 | Microsoft Docs
description: Azure PowerShell 的概觀以及有關安裝和設定的連結。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 09/11/2018
ms.openlocfilehash: bdd8e69a2ea9df8b4fff100e1f3cc4c82d2d9d9d
ms.sourcegitcommit: ac4b53bb42a25aae013a9d8cd9ae98ada9397274
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/08/2018
ms.locfileid: "51274971"
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="878a1-103">Azure PowerShell 的概觀</span><span class="sxs-lookup"><span data-stu-id="878a1-103">Overview of Azure PowerShell</span></span>

<span data-ttu-id="878a1-104">Azure PowerShell 提供了一組 Cmdlet，它們會使用 [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) 模型來管理 Azure 資源。</span><span class="sxs-lookup"><span data-stu-id="878a1-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="878a1-105">您可以在瀏覽器中將它與 [Azure Cloud Shell](/azure/cloud-shell/overview) 搭配使用，或可將它安裝在本機電腦上，並在任何 PowerShell 工作階段中使用它。</span><span class="sxs-lookup"><span data-stu-id="878a1-105">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or you can install it on your local machine and use it in any PowerShell session.</span></span>

<span data-ttu-id="878a1-106">使用 [Cloud Shell](/azure/cloud-shell/overview) 在您的瀏覽器中執行 Azure PowerShell，或在您自己的電腦上加以[安裝](install-azurerm-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="878a1-106">Use the [Cloud Shell](/azure/cloud-shell/overview) to run the Azure PowerShell in your browser, or [install](install-azurerm-ps.md) it on own computer.</span></span> <span data-ttu-id="878a1-107">接著請閱讀[開始](get-started-azureps.md)文件以開始使用它。</span><span class="sxs-lookup"><span data-stu-id="878a1-107">Then read the [Get Started](get-started-azureps.md) article to begin using it.</span></span> <span data-ttu-id="878a1-108">如需最新版本的相關資訊，請參閱[版本資訊](release-notes-azureps.md)。</span><span class="sxs-lookup"><span data-stu-id="878a1-108">For information about the latest release, see the [release notes](release-notes-azureps.md).</span></span>

<span data-ttu-id="878a1-109">下列範例可協助您了解如何使用 Azure PowerShell 來執行常見案例：</span><span class="sxs-lookup"><span data-stu-id="878a1-109">The following samples can help you learn how to perform common scenarios with Azure PowerShell:</span></span>

* [<span data-ttu-id="878a1-110">Linux 虛擬機器</span><span class="sxs-lookup"><span data-stu-id="878a1-110">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="878a1-111">Windows 虛擬機器</span><span class="sxs-lookup"><span data-stu-id="878a1-111">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="878a1-112">Web Apps</span><span class="sxs-lookup"><span data-stu-id="878a1-112">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="878a1-113">SQL Databases</span><span class="sxs-lookup"><span data-stu-id="878a1-113">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

[!INCLUDE[az-replacing-azurerm](../includes/az-replacing-azurerm.md)]

## <a name="learn-powershell-basics"></a><span data-ttu-id="878a1-114">了解 PowerShell 基本概念</span><span class="sxs-lookup"><span data-stu-id="878a1-114">Learn PowerShell basics</span></span>

<span data-ttu-id="878a1-115">如果您不熟悉 PowerShell，PowerShell 的簡介可能會有所幫助。</span><span class="sxs-lookup"><span data-stu-id="878a1-115">If you're unfamiliar with PowerShell, an introduction to PowerShell may be helpful.</span></span>

* [<span data-ttu-id="878a1-116">安裝 PowerShell</span><span class="sxs-lookup"><span data-stu-id="878a1-116">Installing PowerShell</span></span>](/powershell/scripting/setup/installing-windows-powershell)
* [<span data-ttu-id="878a1-117">使用 PowerShell 編寫指令碼</span><span class="sxs-lookup"><span data-stu-id="878a1-117">Scripting with PowerShell</span></span>](/powershell/scripting/powershell-scripting)

<span data-ttu-id="878a1-118">您也可以觀賞這段影片︰[PowerShell 基本概念：(第 1 部分) 開始使用 PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1)。</span><span class="sxs-lookup"><span data-stu-id="878a1-118">You can also watch this video: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span></span>

<span data-ttu-id="878a1-119">或是參加 Microsoft Virtual Academy 的[開始使用 PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart)。</span><span class="sxs-lookup"><span data-stu-id="878a1-119">Or attend the Microsoft Virtual Academy's [Getting Started with PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart).</span></span>

## <a name="build-your-skills-with-microsoft-learn"></a><span data-ttu-id="878a1-120">透過 Microsoft Learn 增進您的技巧</span><span class="sxs-lookup"><span data-stu-id="878a1-120">Build your skills with Microsoft Learn</span></span>

- [<span data-ttu-id="878a1-121">使用 PowerShell 指令碼將 Azure 工作自動化</span><span class="sxs-lookup"><span data-stu-id="878a1-121">Automate Azure tasks using scripts with PowerShell</span></span>](/learn/modules/automate-azure-tasks-with-powershell/)
- [<span data-ttu-id="878a1-122">更多互動式學習...</span><span class="sxs-lookup"><span data-stu-id="878a1-122">More interactive learning...</span></span>](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="878a1-123">其他 Azure Powershell 模組</span><span class="sxs-lookup"><span data-stu-id="878a1-123">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="878a1-124">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="878a1-124">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="878a1-125">Azure 資訊保護</span><span class="sxs-lookup"><span data-stu-id="878a1-125">Azure Information Protection</span></span>](/powershell/azure/aip/)
* [<span data-ttu-id="878a1-126">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="878a1-126">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="878a1-127">Azure ElasticDB</span><span class="sxs-lookup"><span data-stu-id="878a1-127">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)