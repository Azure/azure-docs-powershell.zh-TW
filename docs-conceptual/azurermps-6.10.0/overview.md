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
ms.openlocfilehash: f03243f6f560407b63aff154494cf164d670d810
ms.sourcegitcommit: f6f5e256143aa6c097de3e57e930d8badea49f30
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/18/2018
ms.locfileid: "49398884"
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="8485b-103">Azure PowerShell 的概觀</span><span class="sxs-lookup"><span data-stu-id="8485b-103">Overview of Azure PowerShell</span></span>

<span data-ttu-id="8485b-104">Azure PowerShell 提供了一組 Cmdlet，它們會使用 [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) 模型來管理 Azure 資源。</span><span class="sxs-lookup"><span data-stu-id="8485b-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="8485b-105">您可以在瀏覽器中將它與 [Azure Cloud Shell](/azure/cloud-shell/overview) 搭配使用，或可將它安裝在本機電腦上，並在任何 PowerShell 工作階段中使用它。</span><span class="sxs-lookup"><span data-stu-id="8485b-105">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or you can install it on your local machine and use it in any PowerShell session.</span></span>

<span data-ttu-id="8485b-106">使用 [Cloud Shell](/azure/cloud-shell/overview) 在您的瀏覽器中執行 Azure PowerShell，或在您自己的電腦上加以[安裝](install-azurerm-ps.md)。</span><span class="sxs-lookup"><span data-stu-id="8485b-106">Use the [Cloud Shell](/azure/cloud-shell/overview) to run the Azure PowerShell in your browser, or [install](install-azurerm-ps.md) it on own computer.</span></span> <span data-ttu-id="8485b-107">接著請閱讀[開始](get-started-azureps.md)文件以開始使用它。</span><span class="sxs-lookup"><span data-stu-id="8485b-107">Then read the [Get Started](get-started-azureps.md) article to begin using it.</span></span> <span data-ttu-id="8485b-108">如需最新版本的相關資訊，請參閱[版本資訊](release-notes-azureps.md)。</span><span class="sxs-lookup"><span data-stu-id="8485b-108">For information about the latest release, see the [release notes](release-notes-azureps.md).</span></span>

<span data-ttu-id="8485b-109">下列範例可協助您了解如何使用 Azure PowerShell 來執行常見案例：</span><span class="sxs-lookup"><span data-stu-id="8485b-109">The following samples can help you learn how to perform common scenarios with Azure PowerShell:</span></span>

* [<span data-ttu-id="8485b-110">Linux 虛擬機器</span><span class="sxs-lookup"><span data-stu-id="8485b-110">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="8485b-111">Windows 虛擬機器</span><span class="sxs-lookup"><span data-stu-id="8485b-111">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="8485b-112">Web Apps</span><span class="sxs-lookup"><span data-stu-id="8485b-112">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="8485b-113">SQL Databases</span><span class="sxs-lookup"><span data-stu-id="8485b-113">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

> [!NOTE]
> <span data-ttu-id="8485b-114">如果您的部署使用無法轉換的傳統部署模型，您可以安裝 Azure PowerShell 的服務管理版本。</span><span class="sxs-lookup"><span data-stu-id="8485b-114">If you have deployments that use the classic deployment model that cannot be converted, you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="8485b-115">如需詳細資訊，請參閱[安裝 Azure PowerShell 服務管理模組](/powershell/azure/servicemanagement/install-azure-ps)。</span><span class="sxs-lookup"><span data-stu-id="8485b-115">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>

## <a name="learn-powershell-basics"></a><span data-ttu-id="8485b-116">了解 PowerShell 基本概念</span><span class="sxs-lookup"><span data-stu-id="8485b-116">Learn PowerShell basics</span></span>

<span data-ttu-id="8485b-117">如果您不熟悉 PowerShell，PowerShell 的簡介可能會有所幫助。</span><span class="sxs-lookup"><span data-stu-id="8485b-117">If you're unfamiliar with PowerShell, an introduction to PowerShell may be helpful.</span></span>

* [<span data-ttu-id="8485b-118">安裝 PowerShell</span><span class="sxs-lookup"><span data-stu-id="8485b-118">Installing PowerShell</span></span>](/powershell/scripting/setup/installing-windows-powershell)
* [<span data-ttu-id="8485b-119">使用 PowerShell 編寫指令碼</span><span class="sxs-lookup"><span data-stu-id="8485b-119">Scripting with PowerShell</span></span>](/powershell/scripting/powershell-scripting)

<span data-ttu-id="8485b-120">您也可以觀賞這段影片︰[PowerShell 基本概念：(第 1 部分) 開始使用 PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1)。</span><span class="sxs-lookup"><span data-stu-id="8485b-120">You can also watch this video: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span></span>

<span data-ttu-id="8485b-121">或是參加 Microsoft Virtual Academy 的[開始使用 PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart)。</span><span class="sxs-lookup"><span data-stu-id="8485b-121">Or attend the Microsoft Virtual Academy's [Getting Started with PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart).</span></span>

## <a name="build-your-skills-with-microsoft-learn"></a><span data-ttu-id="8485b-122">透過 Microsoft Learn 增進您的技巧</span><span class="sxs-lookup"><span data-stu-id="8485b-122">Build your skills with Microsoft Learn</span></span>

- [<span data-ttu-id="8485b-123">使用 PowerShell 指令碼將 Azure 工作自動化</span><span class="sxs-lookup"><span data-stu-id="8485b-123">Automate Azure tasks using scripts with PowerShell</span></span>](/learn/modules/automate-azure-tasks-with-powershell/)
- [<span data-ttu-id="8485b-124">更多互動式學習...</span><span class="sxs-lookup"><span data-stu-id="8485b-124">More interactive learning...</span></span>](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="8485b-125">其他 Azure Powershell 模組</span><span class="sxs-lookup"><span data-stu-id="8485b-125">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="8485b-126">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="8485b-126">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="8485b-127">Azure 資訊保護</span><span class="sxs-lookup"><span data-stu-id="8485b-127">Azure Information Protection</span></span>](/powershell/azure/aip/)
* [<span data-ttu-id="8485b-128">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="8485b-128">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="8485b-129">Azure ElasticDB</span><span class="sxs-lookup"><span data-stu-id="8485b-129">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)
