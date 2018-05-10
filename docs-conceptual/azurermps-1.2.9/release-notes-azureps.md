---
title: Azure PowerShell 變更記錄 | Microsoft Docs
description: 這是在最新版中對 Azure powershell 所做的變更歷程記錄。
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: 5fe7591855577e083aad5923aed37b18d0b2a40c
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/08/2018
---
# <a name="release-notes"></a><span data-ttu-id="ed154-103">版本資訊</span><span class="sxs-lookup"><span data-stu-id="ed154-103">Release notes</span></span>

<span data-ttu-id="ed154-104">這是此版本中對 Azure PowerShell 所做的變更清單。</span><span class="sxs-lookup"><span data-stu-id="ed154-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <a name="version-129"></a><span data-ttu-id="ed154-105">1.2.9 版</span><span class="sxs-lookup"><span data-stu-id="ed154-105">Version 1.2.9</span></span>

<span data-ttu-id="ed154-106">此版本變更</span><span class="sxs-lookup"><span data-stu-id="ed154-106">Changes This Release</span></span>

* <span data-ttu-id="ed154-107">AzureRm.AzureStackAdmin 模組</span><span class="sxs-lookup"><span data-stu-id="ed154-107">AzureRm.AzureStackAdmin Module</span></span>
    + <span data-ttu-id="ed154-108">變更 Add-AzureRmResourceProviderRegistration Cmdlet 以支援系統管理員 Azure Resource Manager 和租用戶 Azure Resource Manager 分割</span><span class="sxs-lookup"><span data-stu-id="ed154-108">Changes in the Add-AzureRmResourceProviderRegistration cmdlet for the support of Admin Azure resource manager and tenant azure resource manager split.</span></span> <span data-ttu-id="ed154-109">已新增 -ResourceManagerType 參數。</span><span class="sxs-lookup"><span data-stu-id="ed154-109">A new parameter -ResourceManagerType has been added.</span></span>
    + <span data-ttu-id="ed154-110">移除每個 Cmdlet 中的 -AdminUri、-ApiVersion, -SubscriptionId 和 -Token 參數。</span><span class="sxs-lookup"><span data-stu-id="ed154-110">Removal of the parameters -AdminUri, -ApiVersion, -SubscriptionId and -Token from each cmdlets.</span></span> <span data-ttu-id="ed154-111">我們一直列印這些參數將會被淘汰且現在已移除的警告。</span><span class="sxs-lookup"><span data-stu-id="ed154-111">We have been printing warnings that these parameters will be deprecated and now they got removed.</span></span>
* <span data-ttu-id="ed154-112">AzureStackStorage 模組</span><span class="sxs-lookup"><span data-stu-id="ed154-112">AzureStackStorage module</span></span>
    + <span data-ttu-id="ed154-113">已新增 Cmdlet 來支援容器移轉案例。</span><span class="sxs-lookup"><span data-stu-id="ed154-113">Added new cmdlets to support container migration scenarios.</span></span>
    + <span data-ttu-id="ed154-114">已移除參考內部元件和基礎功能的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ed154-114">Removed cmdlets referring to internal components and underlying features.</span></span>
* <span data-ttu-id="ed154-115">AzureRM.BootStrapper</span><span class="sxs-lookup"><span data-stu-id="ed154-115">AzureRM.BootStrapper</span></span>
    + <span data-ttu-id="ed154-116">建立新的模組，以利用版本設定檔來管理 Azure PowerShell Cmdlet 的版本</span><span class="sxs-lookup"><span data-stu-id="ed154-116">Created new module to manage versions of Azure PowerShell cmdlets through the use of version profiles</span></span>