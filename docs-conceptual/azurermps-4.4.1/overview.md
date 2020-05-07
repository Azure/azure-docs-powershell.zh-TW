---
title: Azure PowerShell 概觀 | Microsoft Docs
description: Azure PowerShell 的概觀以及有關安裝和設定的連結。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 08/31/2017
ms.openlocfilehash: 0541975e55620a8792c0d51213c4ed02ea29988f
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/05/2020
ms.locfileid: "67863416"
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="3cd1d-103">Azure PowerShell 的概觀</span><span class="sxs-lookup"><span data-stu-id="3cd1d-103">Overview of Azure PowerShell</span></span>

[!INCLUDE[az-replacing-azurerm.md](../includes/az-replacing-azurerm.md)]

<span data-ttu-id="3cd1d-104">Azure PowerShell 提供了一組 Cmdlet，它們會使用 [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) 模型來管理 Azure 資源。</span><span class="sxs-lookup"><span data-stu-id="3cd1d-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="3cd1d-105">您可以在瀏覽器中將它與 [Azure Cloud Shell](/azure/cloud-shell/overview) 搭配使用，或可將它安裝在本機電腦上，並在任何 PowerShell 工作階段中使用它。</span><span class="sxs-lookup"><span data-stu-id="3cd1d-105">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or you can install it on your local machine and use it in any PowerShell session.</span></span>

<span data-ttu-id="3cd1d-106">使用 [Cloud Shell](/azure/cloud-shell/overview) 在您的瀏覽器中執行 Azure PowerShell，或在您自己的電腦上加以[安裝](install-azurerm-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="3cd1d-106">Use the [Cloud Shell](/azure/cloud-shell/overview) to run the Azure PowerShell in your browser, or [install](install-azurerm-ps.md) it on own computer.</span></span> <span data-ttu-id="3cd1d-107">接著請閱讀[開始](get-started-azureps.md)文件以開始使用它。</span><span class="sxs-lookup"><span data-stu-id="3cd1d-107">Then read the [Get Started](get-started-azureps.md) article to begin using it.</span></span> <span data-ttu-id="3cd1d-108">如需最新版本的相關資訊，請參閱[版本資訊](release-notes-azureps.md)。</span><span class="sxs-lookup"><span data-stu-id="3cd1d-108">For information about the latest release, see the [release notes](release-notes-azureps.md).</span></span>

<span data-ttu-id="3cd1d-109">下列範例可協助您了解如何使用 Azure PowerShell 來執行常見案例：</span><span class="sxs-lookup"><span data-stu-id="3cd1d-109">The following samples can help you learn how to perform common scenarios with Azure PowerShell:</span></span>

* [<span data-ttu-id="3cd1d-110">Linux 虛擬機器</span><span class="sxs-lookup"><span data-stu-id="3cd1d-110">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="3cd1d-111">Windows 虛擬機器</span><span class="sxs-lookup"><span data-stu-id="3cd1d-111">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="3cd1d-112">Web Apps</span><span class="sxs-lookup"><span data-stu-id="3cd1d-112">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="3cd1d-113">SQL Databases</span><span class="sxs-lookup"><span data-stu-id="3cd1d-113">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="learn-powershell-basics"></a><span data-ttu-id="3cd1d-114">了解 PowerShell 基本概念</span><span class="sxs-lookup"><span data-stu-id="3cd1d-114">Learn PowerShell basics</span></span>

<span data-ttu-id="3cd1d-115">如果您不熟悉 PowerShell，則 PowerShell 的簡介會很有幫助。</span><span class="sxs-lookup"><span data-stu-id="3cd1d-115">If you are unfamiliar with PowerShell, you may find an introduction to PowerShell helpful.</span></span>

* [<span data-ttu-id="3cd1d-116">安裝 PowerShell</span><span class="sxs-lookup"><span data-stu-id="3cd1d-116">Installing PowerShell</span></span>](/powershell/scripting/installing-windows-powershell)
* [<span data-ttu-id="3cd1d-117">使用 PowerShell 編寫指令碼</span><span class="sxs-lookup"><span data-stu-id="3cd1d-117">Scripting with PowerShell</span></span>](/powershell/scripting/scripting-with-windows-powershell)

<span data-ttu-id="3cd1d-118">您也可以觀賞這段影片︰[PowerShell 基本概念：(第 1 部分) 開始使用 PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1)。</span><span class="sxs-lookup"><span data-stu-id="3cd1d-118">You can also watch this video: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span></span>

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="3cd1d-119">其他 Azure Powershell 模組</span><span class="sxs-lookup"><span data-stu-id="3cd1d-119">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="3cd1d-120">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="3cd1d-120">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="3cd1d-121">Azure 資訊保護</span><span class="sxs-lookup"><span data-stu-id="3cd1d-121">Azure Information Protection</span></span>](/powershell/azure/aip/)
* [<span data-ttu-id="3cd1d-122">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="3cd1d-122">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="3cd1d-123">Azure ElasticDB</span><span class="sxs-lookup"><span data-stu-id="3cd1d-123">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)
