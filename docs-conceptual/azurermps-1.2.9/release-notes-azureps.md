---
title: Azure PowerShell 變更記錄 | Microsoft Docs
description: 這是在最新版中對 Azure powershell 所做的變更歷程記錄。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: 91d97260568a36e1135196899503fb0c8e1c6731
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/08/2018
ms.locfileid: "34853010"
---
# <a name="release-notes"></a><span data-ttu-id="fa4d2-103">版本資訊</span><span class="sxs-lookup"><span data-stu-id="fa4d2-103">Release notes</span></span>

<span data-ttu-id="fa4d2-104">這是此版本中對 Azure PowerShell 所做的變更清單。</span><span class="sxs-lookup"><span data-stu-id="fa4d2-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <a name="version-129"></a><span data-ttu-id="fa4d2-105">1.2.9 版</span><span class="sxs-lookup"><span data-stu-id="fa4d2-105">Version 1.2.9</span></span>

<span data-ttu-id="fa4d2-106">此版本變更</span><span class="sxs-lookup"><span data-stu-id="fa4d2-106">Changes This Release</span></span>

* <span data-ttu-id="fa4d2-107">AzureRm.AzureStackAdmin 模組</span><span class="sxs-lookup"><span data-stu-id="fa4d2-107">AzureRm.AzureStackAdmin Module</span></span>
    + <span data-ttu-id="fa4d2-108">變更 Add-AzureRmResourceProviderRegistration Cmdlet 以支援系統管理員 Azure Resource Manager 和租用戶 Azure Resource Manager 分割</span><span class="sxs-lookup"><span data-stu-id="fa4d2-108">Changes in the Add-AzureRmResourceProviderRegistration cmdlet for the support of Admin Azure resource manager and tenant azure resource manager split.</span></span> <span data-ttu-id="fa4d2-109">已新增 -ResourceManagerType 參數。</span><span class="sxs-lookup"><span data-stu-id="fa4d2-109">A new parameter -ResourceManagerType has been added.</span></span>
    + <span data-ttu-id="fa4d2-110">移除每個 Cmdlet 中的 -AdminUri、-ApiVersion, -SubscriptionId 和 -Token 參數。</span><span class="sxs-lookup"><span data-stu-id="fa4d2-110">Removal of the parameters -AdminUri, -ApiVersion, -SubscriptionId and -Token from each cmdlets.</span></span> <span data-ttu-id="fa4d2-111">我們一直列印這些參數將會被淘汰且現在已移除的警告。</span><span class="sxs-lookup"><span data-stu-id="fa4d2-111">We have been printing warnings that these parameters will be deprecated and now they got removed.</span></span>
* <span data-ttu-id="fa4d2-112">AzureStackStorage 模組</span><span class="sxs-lookup"><span data-stu-id="fa4d2-112">AzureStackStorage module</span></span>
    + <span data-ttu-id="fa4d2-113">已新增 Cmdlet 來支援容器移轉案例。</span><span class="sxs-lookup"><span data-stu-id="fa4d2-113">Added new cmdlets to support container migration scenarios.</span></span>
    + <span data-ttu-id="fa4d2-114">已移除參考內部元件和基礎功能的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fa4d2-114">Removed cmdlets referring to internal components and underlying features.</span></span>
* <span data-ttu-id="fa4d2-115">AzureRM.BootStrapper</span><span class="sxs-lookup"><span data-stu-id="fa4d2-115">AzureRM.BootStrapper</span></span>
    + <span data-ttu-id="fa4d2-116">建立新的模組，以利用版本設定檔來管理 Azure PowerShell Cmdlet 的版本</span><span class="sxs-lookup"><span data-stu-id="fa4d2-116">Created new module to manage versions of Azure PowerShell cmdlets through the use of version profiles</span></span>