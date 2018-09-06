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
ms.openlocfilehash: ef4f9b416454471f8c9476f0bbccbcca20a22000
ms.sourcegitcommit: 971f19181b2cd68b7845bbebdb22858c06541c8c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/06/2018
ms.locfileid: "43384173"
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="07691-103">Azure PowerShell 的概觀</span><span class="sxs-lookup"><span data-stu-id="07691-103">Overview of Azure PowerShell</span></span>

<span data-ttu-id="07691-104">Azure PowerShell 提供了一組 Cmdlet，它們會使用 [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) 模型來管理 Azure 資源。</span><span class="sxs-lookup"><span data-stu-id="07691-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="07691-105">您可以在瀏覽器中將它與 [Azure Cloud Shell](/azure/cloud-shell/overview) 搭配使用，或可將它安裝在本機電腦上，並在任何 PowerShell 工作階段中使用它。</span><span class="sxs-lookup"><span data-stu-id="07691-105">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or you can install it on your local machine and use it in any PowerShell session.</span></span>

<span data-ttu-id="07691-106">使用 [Cloud Shell](/azure/cloud-shell/overview) 在您的瀏覽器中執行 Azure PowerShell，或在您自己的電腦上加以[安裝](install-azurerm-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="07691-106">Use the [Cloud Shell](/azure/cloud-shell/overview) to run the Azure PowerShell in your browser, or [install](install-azurerm-ps.md) it on own computer.</span></span> <span data-ttu-id="07691-107">接著請閱讀[開始](get-started-azureps.md)文件以開始使用它。</span><span class="sxs-lookup"><span data-stu-id="07691-107">Then read the [Get Started](get-started-azureps.md) article to begin using it.</span></span> <span data-ttu-id="07691-108">如需最新版本的相關資訊，請參閱[版本資訊](release-notes-azureps.md)。</span><span class="sxs-lookup"><span data-stu-id="07691-108">For information about the latest release, see the [release notes](release-notes-azureps.md).</span></span>

<span data-ttu-id="07691-109">下列範例可協助您了解如何使用 Azure PowerShell 來執行常見案例：</span><span class="sxs-lookup"><span data-stu-id="07691-109">The following samples can help you learn how to perform common scenarios with Azure PowerShell:</span></span>

* [<span data-ttu-id="07691-110">Linux 虛擬機器</span><span class="sxs-lookup"><span data-stu-id="07691-110">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="07691-111">Windows 虛擬機器</span><span class="sxs-lookup"><span data-stu-id="07691-111">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="07691-112">Web Apps</span><span class="sxs-lookup"><span data-stu-id="07691-112">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="07691-113">SQL Databases</span><span class="sxs-lookup"><span data-stu-id="07691-113">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

> [!NOTE]
> <span data-ttu-id="07691-114">如果您的部署使用無法轉換的傳統部署模型，您可以安裝 Azure PowerShell 的服務管理版本。</span><span class="sxs-lookup"><span data-stu-id="07691-114">If you have deployments that use the classic deployment model that cannot be converted, you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="07691-115">如需詳細資訊，請參閱[安裝 Azure PowerShell 服務管理模組](/powershell/azure/servicemanagement/install-azure-ps)。</span><span class="sxs-lookup"><span data-stu-id="07691-115">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>

## <a name="learn-powershell-basics"></a><span data-ttu-id="07691-116">了解 PowerShell 基本概念</span><span class="sxs-lookup"><span data-stu-id="07691-116">Learn PowerShell basics</span></span>

<span data-ttu-id="07691-117">如果您不熟悉 PowerShell，則 PowerShell 的簡介會很有幫助。</span><span class="sxs-lookup"><span data-stu-id="07691-117">If you are unfamiliar with PowerShell, you may find an introduction to PowerShell helpful.</span></span>

* [<span data-ttu-id="07691-118">安裝 PowerShell</span><span class="sxs-lookup"><span data-stu-id="07691-118">Installing PowerShell</span></span>](/powershell/scripting/installing-windows-powershell)
* [<span data-ttu-id="07691-119">使用 PowerShell 編寫指令碼</span><span class="sxs-lookup"><span data-stu-id="07691-119">Scripting with PowerShell</span></span>](/powershell/scripting/scripting-with-windows-powershell)

<span data-ttu-id="07691-120">您也可以觀賞這段影片︰[PowerShell 基本概念：(第 1 部分) 開始使用 PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1)。</span><span class="sxs-lookup"><span data-stu-id="07691-120">You can also watch this video: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span></span>

<span data-ttu-id="07691-121">或是參加 Microsoft Virtual Academy 的[開始使用 PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart)。</span><span class="sxs-lookup"><span data-stu-id="07691-121">Or attend the Microsoft Virtual Academy's [Getting Started with PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart).</span></span>

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="07691-122">其他 Azure Powershell 模組</span><span class="sxs-lookup"><span data-stu-id="07691-122">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="07691-123">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="07691-123">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="07691-124">Azure 資訊保護</span><span class="sxs-lookup"><span data-stu-id="07691-124">Azure Information Protection</span></span>](/powershell/azure/aip/)
* [<span data-ttu-id="07691-125">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="07691-125">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="07691-126">Azure ElasticDB</span><span class="sxs-lookup"><span data-stu-id="07691-126">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)