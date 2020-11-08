---
Module Name: Az.StorageSync
Module Guid: 001b4bbc-9d7d-43b2-9e95-7a70325e9509
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.storagesync
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
ms.openlocfilehash: bc3704c3594826f19399c1967bbe86ed7f1e8773
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126696"
---
# <span data-ttu-id="aa327-101">Az StorageSync 模組</span><span class="sxs-lookup"><span data-stu-id="aa327-101">Az.StorageSync Module</span></span>
## <span data-ttu-id="aa327-102">說明</span><span class="sxs-lookup"><span data-stu-id="aa327-102">Description</span></span>
<span data-ttu-id="aa327-103">[儲存同步處理] 模組中的 Cmdlet 可讓您管理有關 PowerShell 中 Azure 檔案同步處理的作業。</span><span class="sxs-lookup"><span data-stu-id="aa327-103">The cmdlets in the Storage Sync module enable you to manage operations pertaining to Azure File Sync in PowerShell.</span></span>

## <span data-ttu-id="aa327-104">Az StorageSync Cmdlet</span><span class="sxs-lookup"><span data-stu-id="aa327-104">Az.StorageSync Cmdlets</span></span>
### [<span data-ttu-id="aa327-105">AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="aa327-105">Get-AzStorageSyncCloudEndpoint</span></span>](Get-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="aa327-106">這個命令會列出指定同步群組中的所有雲端端點。</span><span class="sxs-lookup"><span data-stu-id="aa327-106">This command lists all cloud endpoints within a given sync group.</span></span>

### [<span data-ttu-id="aa327-107">AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="aa327-107">Get-AzStorageSyncGroup</span></span>](Get-AzStorageSyncGroup.md)
<span data-ttu-id="aa327-108">這個命令會列出特定儲存同步處理服務中的所有同步處理群組。</span><span class="sxs-lookup"><span data-stu-id="aa327-108">This command lists all sync groups within a given storage sync service.</span></span>

### [<span data-ttu-id="aa327-109">AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="aa327-109">Get-AzStorageSyncServer</span></span>](Get-AzStorageSyncServer.md)
<span data-ttu-id="aa327-110">這個命令會列出已登錄至特定儲存同步處理服務的所有伺服器。</span><span class="sxs-lookup"><span data-stu-id="aa327-110">This command lists all servers registered to a given storage sync service.</span></span>

### [<span data-ttu-id="aa327-111">AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="aa327-111">Get-AzStorageSyncServerEndpoint</span></span>](Get-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="aa327-112">這個命令會列出指定同步群組中的所有伺服器端點。</span><span class="sxs-lookup"><span data-stu-id="aa327-112">This command lists all server endpoints within a given sync group.</span></span>

### [<span data-ttu-id="aa327-113">AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="aa327-113">Get-AzStorageSyncService</span></span>](Get-AzStorageSyncService.md)
<span data-ttu-id="aa327-114">這個命令會列出 [訂閱/資源群組] 的指定範圍內的所有儲存同步處理服務。</span><span class="sxs-lookup"><span data-stu-id="aa327-114">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

### [<span data-ttu-id="aa327-115">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="aa327-115">Invoke-AzStorageSyncChangeDetection</span></span>](Invoke-AzStorageSyncChangeDetection.md)
<span data-ttu-id="aa327-116">這個命令可以用來手動啟動命名空間變更的偵測。</span><span class="sxs-lookup"><span data-stu-id="aa327-116">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="aa327-117">您可以將它設定為整個共用、子資料夾或一組檔案的目標。</span><span class="sxs-lookup"><span data-stu-id="aa327-117">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="aa327-118">最多可以檢測到10000變更。</span><span class="sxs-lookup"><span data-stu-id="aa327-118">A maximum of 10,000 changes can be detected.</span></span> <span data-ttu-id="aa327-119">如果您知道變更範圍，請將此命令的執行限制為命名空間的一部分，因此變更偵測可以快速完成，且在10000變更限制內。</span><span class="sxs-lookup"><span data-stu-id="aa327-119">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within a 10,000 changes limit.</span></span>

### [<span data-ttu-id="aa327-120">Invoke-AzStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="aa327-120">Invoke-AzStorageSyncCompatibilityCheck</span></span>](Invoke-AzStorageSyncCompatibilityCheck.md)
<span data-ttu-id="aa327-121">檢查您的系統與 Azure 檔案同步處理之間可能的相容性問題。</span><span class="sxs-lookup"><span data-stu-id="aa327-121">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

### [<span data-ttu-id="aa327-122">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="aa327-122">Invoke-AzStorageSyncFileRecall</span></span>](Invoke-AzStorageSyncFileRecall.md)
<span data-ttu-id="aa327-123">這個命令會將所有的分層檔案撤回回本機磁片。</span><span class="sxs-lookup"><span data-stu-id="aa327-123">This command recalls all tiered files back to local disk.</span></span>

### [<span data-ttu-id="aa327-124">新-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="aa327-124">New-AzStorageSyncCloudEndpoint</span></span>](New-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="aa327-125">這個命令會在同步處理群組中建立 Azure 檔案同步處理雲端端點。</span><span class="sxs-lookup"><span data-stu-id="aa327-125">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

### [<span data-ttu-id="aa327-126">新-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="aa327-126">New-AzStorageSyncGroup</span></span>](New-AzStorageSyncGroup.md)
<span data-ttu-id="aa327-127">這個命令會在指定的儲存空間同步處理服務中建立新的同步處理群組。</span><span class="sxs-lookup"><span data-stu-id="aa327-127">This command creates a new sync group within a specified storage sync service.</span></span>

### [<span data-ttu-id="aa327-128">新-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="aa327-128">New-AzStorageSyncServerEndpoint</span></span>](New-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="aa327-129">這個命令會在已註冊的伺服器上建立新的伺服器端點。</span><span class="sxs-lookup"><span data-stu-id="aa327-129">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="aa327-130">這可讓伺服器上的指定路徑開始與同步群組中的其他端點同步處理檔案。</span><span class="sxs-lookup"><span data-stu-id="aa327-130">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span>

### [<span data-ttu-id="aa327-131">新-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="aa327-131">New-AzStorageSyncService</span></span>](New-AzStorageSyncService.md)
<span data-ttu-id="aa327-132">這個命令會在資源群組中建立新的儲存同步處理服務。</span><span class="sxs-lookup"><span data-stu-id="aa327-132">This command creates a new storage sync service in a resource group.</span></span>

### [<span data-ttu-id="aa327-133">Set-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="aa327-133">Set-AzStorageSyncService</span></span>](New-AzStorageSyncService.md)
<span data-ttu-id="aa327-134">這個命令會設定資源群組中的儲存同步處理服務。</span><span class="sxs-lookup"><span data-stu-id="aa327-134">This command sets a storage sync service in a resource group.</span></span>

### [<span data-ttu-id="aa327-135">Register-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="aa327-135">Register-AzStorageSyncServer</span></span>](Register-AzStorageSyncServer.md)
<span data-ttu-id="aa327-136">這個命令會將伺服器註冊至儲存同步處理服務，這會建立信任關係。</span><span class="sxs-lookup"><span data-stu-id="aa327-136">This command registers a server to a storage sync service which creates a trust relationship.</span></span> <span data-ttu-id="aa327-137">然後，您可以使用 PowerShell 或 Azure 入口網站來設定此伺服器上的同步處理。</span><span class="sxs-lookup"><span data-stu-id="aa327-137">PowerShell or the Azure portal can then be used to configure sync on this server.</span></span>

### [<span data-ttu-id="aa327-138">移除-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="aa327-138">Remove-AzStorageSyncCloudEndpoint</span></span>](Remove-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="aa327-139">這個命令會從同步處理群組中刪除指定的雲端端點。</span><span class="sxs-lookup"><span data-stu-id="aa327-139">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="aa327-140">若沒有至少一個雲端端點，此同步處理群組中則不能同步處理任何其他伺服器端點。</span><span class="sxs-lookup"><span data-stu-id="aa327-140">Without at least one cloud endpoint, no other server endpoints in this sync group can sync.</span></span>

### [<span data-ttu-id="aa327-141">移除-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="aa327-141">Remove-AzStorageSyncGroup</span></span>](Remove-AzStorageSyncGroup.md)
<span data-ttu-id="aa327-142">這個命令會刪除指定的同步處理群組。</span><span class="sxs-lookup"><span data-stu-id="aa327-142">This command will delete the specified sync group.</span></span>

### [<span data-ttu-id="aa327-143">移除-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="aa327-143">Remove-AzStorageSyncServerEndpoint</span></span>](Remove-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="aa327-144">這個命令會刪除指定的伺服器端點。</span><span class="sxs-lookup"><span data-stu-id="aa327-144">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="aa327-145">同步處理到這個位置將會立即停止。</span><span class="sxs-lookup"><span data-stu-id="aa327-145">Sync to this location will stop immediately.</span></span>

### [<span data-ttu-id="aa327-146">移除-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="aa327-146">Remove-AzStorageSyncService</span></span>](Remove-AzStorageSyncService.md)
<span data-ttu-id="aa327-147">這個命令會刪除指定的儲存同步處理服務。</span><span class="sxs-lookup"><span data-stu-id="aa327-147">This command will delete the specified storage sync service.</span></span>

### [<span data-ttu-id="aa327-148">Reset-AzStorageSyncServerCertificate</span><span class="sxs-lookup"><span data-stu-id="aa327-148">Reset-AzStorageSyncServerCertificate</span></span>](Reset-AzStorageSyncServerCertificate.md)
<span data-ttu-id="aa327-149">僅用於疑難排解。</span><span class="sxs-lookup"><span data-stu-id="aa327-149">Use for troubleshooting only.</span></span> <span data-ttu-id="aa327-150">這個命令會將用來描述伺服器身分識別的儲存同步處理伺服器憑證滾到儲存同步處理服務。</span><span class="sxs-lookup"><span data-stu-id="aa327-150">This command will roll the storage sync server certificate used to describe the server identity to the storage sync service.</span></span>

### [<span data-ttu-id="aa327-151">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="aa327-151">Set-AzStorageSyncServerEndpoint</span></span>](Set-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="aa327-152">這個命令可讓您變更伺服器端點的可調參數。</span><span class="sxs-lookup"><span data-stu-id="aa327-152">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

### [<span data-ttu-id="aa327-153">取消註冊-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="aa327-153">Unregister-AzStorageSyncServer</span></span>](Unregister-AzStorageSyncServer.md)
<span data-ttu-id="aa327-154">警告：取消註冊伺服器會導致層疊刪除此伺服器上的所有伺服器端點。</span><span class="sxs-lookup"><span data-stu-id="aa327-154">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="aa327-155">這個命令會從它的儲存同步處理服務登出伺服器。</span><span class="sxs-lookup"><span data-stu-id="aa327-155">This command will unregister a server from it's storage sync service.</span></span>

