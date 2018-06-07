---
title: Azure Stack PowerShell 概觀 | Microsoft Docs
description: Azure Stack PowerShell 安裝和設定概觀。
author: SnehaGunda
manager: Byronr
ms.product: azure-stack
ms.devlang: powershell
ms.topic: reference
ms.author: sngun
ms.manager: byronr
ms.openlocfilehash: 3f55ff613004f0726e20255126b29bf7f64662b8
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/06/2018
ms.locfileid: "34820188"
---
# <a name="azure-stack-powershell"></a><span data-ttu-id="cab5b-103">Azure Stack PowerShell</span><span class="sxs-lookup"><span data-stu-id="cab5b-103">Azure Stack PowerShell</span></span>

<span data-ttu-id="cab5b-104">Azure Stack 需要下列兩個 PowerShell 模組：</span><span class="sxs-lookup"><span data-stu-id="cab5b-104">Azure Stack requires the following two PowerShell modules:</span></span>  

1. <span data-ttu-id="cab5b-105">Azure Stack 相容的 **AzureRM** 模組，可藉由安裝 **2017-03-09-profile** API 版本設定檔來取得。</span><span class="sxs-lookup"><span data-stu-id="cab5b-105">The Azure Stack compatible **AzureRM** module which is available by installing the **2017-03-09-profile** API Version Profile.</span></span> <span data-ttu-id="cab5b-106">使用此設定檔安裝的 Cmdlet 只可供 Azure Stack 操作員和使用者使用。</span><span class="sxs-lookup"><span data-stu-id="cab5b-106">The cmdlets installed by using this profile can be used by Azure Stack operators and users.</span></span>

2. <span data-ttu-id="cab5b-107">最近的版本為 **1.2.11** 安裝 **AzureStack** 模組。</span><span class="sxs-lookup"><span data-stu-id="cab5b-107">The most current version is the **1.2.11** install of the **AzureStack** module.</span></span> <span data-ttu-id="cab5b-108">使用此模組安裝的 Cmdlet 只可供 Azure Stack 操作員使用。</span><span class="sxs-lookup"><span data-stu-id="cab5b-108">The cmdlets installed by using this module can be used by Azure Stack operators only.</span></span> <span data-ttu-id="cab5b-109">操作員可以使用此模組所提供的 PowerShell Cmdlet 來執行各項作業，例如管理供應項目、方案、服務、配額等。</span><span class="sxs-lookup"><span data-stu-id="cab5b-109">Operators can perform operations such as manage offers, plans, services, quotas, etc. by using the PowerShell cmdlets provided by this module.</span></span> <span data-ttu-id="cab5b-110">若要了解此模組中可用的 PowerShell Cmdlet，請參閱 [AzureStackAdmin](https://docs.microsoft.com/powershell/module/azurerm.azurestackadmin/?view=azurestackps-1.2.11#azurerm.azurestackadmin) 和 [AzureStackStorage](https://docs.microsoft.com/powershell/module/azurerm.azurestackstorage/?view=azurestackps-1.2.11#azurerm.azurestackstorage) 參考內容。</span><span class="sxs-lookup"><span data-stu-id="cab5b-110">To learn about the PowerShell cmdlets available in this module, see the [AzureStackAdmin](https://docs.microsoft.com/powershell/module/azurerm.azurestackadmin/?view=azurestackps-1.2.11#azurerm.azurestackadmin) and [AzureStackStorage](https://docs.microsoft.com/powershell/module/azurerm.azurestackstorage/?view=azurestackps-1.2.11#azurerm.azurestackstorage) Reference content.</span></span>

## <a name="next-steps"></a><span data-ttu-id="cab5b-111">後續步驟</span><span class="sxs-lookup"><span data-stu-id="cab5b-111">Next Steps</span></span>

* [<span data-ttu-id="cab5b-112">安裝 Azure Stack 適用的 PowerShell</span><span class="sxs-lookup"><span data-stu-id="cab5b-112">Install PowerShell for Azure Stack</span></span>](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9)
* [<span data-ttu-id="cab5b-113">設定 PowerShell 以便搭配 Azure Stack 使用</span><span class="sxs-lookup"><span data-stu-id="cab5b-113">Configure PowerShell for use with Azure Stack</span></span>](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-configure?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9)
