---
Module Name: Azure.AnalysisServices
Module Guid: c717b5a4-1f1b-4a2f-8aa1-bfd09934626e
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/azure.analysisservices
Help Version: 0.5.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Azure.AnalysisServices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Azure.AnalysisServices.md
ms.openlocfilehash: 1c4951c45a047fed26585f13e88f541281b04267
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/23/2019
ms.locfileid: "93441776"
---
# <span data-ttu-id="78596-101">AnalysisServices 模組</span><span class="sxs-lookup"><span data-stu-id="78596-101">Azure.AnalysisServices Module</span></span>
## <span data-ttu-id="78596-102">說明</span><span class="sxs-lookup"><span data-stu-id="78596-102">Description</span></span>
<span data-ttu-id="78596-103">此模組包含在指定的 Azure Analysis Services 環境中執行作業的命令</span><span class="sxs-lookup"><span data-stu-id="78596-103">This module contains commands for performing operations on a given Azure Analysis Services environment</span></span>

## <span data-ttu-id="78596-104">AnalysisServices Cmdlet</span><span class="sxs-lookup"><span data-stu-id="78596-104">Azure.AnalysisServices Cmdlets</span></span>
### [<span data-ttu-id="78596-105">附加 AzureAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="78596-105">Add-AzureAnalysisServicesAccount</span></span>](Add-AzureAnalysisServicesAccount.md)
<span data-ttu-id="78596-106">新增要用於 Azure Analysis Services server Cmdlet 要求的經過驗證的帳戶。</span><span class="sxs-lookup"><span data-stu-id="78596-106">Adds an authenticated account to use for Azure Analysis Services server cmdlet requests.</span></span>

### [<span data-ttu-id="78596-107">Export-AzureAnalysisServicesInstanceLog</span><span class="sxs-lookup"><span data-stu-id="78596-107">Export-AzureAnalysisServicesInstanceLog</span></span>](Export-AzureAnalysisServicesInstanceLog.md)
<span data-ttu-id="78596-108">根據 Add-AzureAnalysisServicesAccount 命令中指定的，從目前登入的環境中的 Analysis Services 伺服器實例匯出記錄</span><span class="sxs-lookup"><span data-stu-id="78596-108">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

### [<span data-ttu-id="78596-109">重新開機-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="78596-109">Restart-AzureAnalysisServicesInstance</span></span>](Restart-AzureAnalysisServicesInstance.md)
<span data-ttu-id="78596-110">在目前登入的環境中重新開機 Analysis Services 伺服器的實例，如 Add-AzureAnalysisServicesAccount 命令中所指定</span><span class="sxs-lookup"><span data-stu-id="78596-110">Restarts an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

### [<span data-ttu-id="78596-111">同步處理-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="78596-111">Sync-AzureAnalysisServicesInstance</span></span>](Sync-AzureAnalysisServicesInstance.md)
<span data-ttu-id="78596-112">將指定的 Analysis Services 伺服器實例上的指定資料庫同步處理到目前登入的 scaleout 中的所有查詢實例，如 Add-AzureAnalysisServicesAccount 命令中所指定</span><span class="sxs-lookup"><span data-stu-id="78596-112">Synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

