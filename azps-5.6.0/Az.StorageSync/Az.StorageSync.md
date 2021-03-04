---
Module Name: Az.StorageSync
Module Guid: 001b4bbc-9d7d-43b2-9e95-7a70325e9509
Download Help Link: https://docs.microsoft.com/powershell/module/az.storagesync
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
ms.openlocfilehash: 9acaa8a562ffe88631a587703a3300ac13f73224
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907217"
---
# <span data-ttu-id="96f08-101">Az.StorageSync 模組</span><span class="sxs-lookup"><span data-stu-id="96f08-101">Az.StorageSync Module</span></span>
## <span data-ttu-id="96f08-102">描述</span><span class="sxs-lookup"><span data-stu-id="96f08-102">Description</span></span>
<span data-ttu-id="96f08-103">儲存同步處理模組中的 Cmdlet 可啟用 PowerShell 中與 Azure 檔案同步處理相關的作業。</span><span class="sxs-lookup"><span data-stu-id="96f08-103">The cmdlets in the Storage Sync module enable you to manage operations pertaining to Azure File Sync in PowerShell.</span></span>

## <span data-ttu-id="96f08-104">Az.StorageSync Cmdlet</span><span class="sxs-lookup"><span data-stu-id="96f08-104">Az.StorageSync Cmdlets</span></span>
### [<span data-ttu-id="96f08-105">Get-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="96f08-105">Get-AzStorageSyncCloudEndpoint</span></span>](Get-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="96f08-106">此命令會列出特定同步處理群組內的所有雲端端點。</span><span class="sxs-lookup"><span data-stu-id="96f08-106">This command lists all cloud endpoints within a given sync group.</span></span>

### [<span data-ttu-id="96f08-107">Get-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="96f08-107">Get-AzStorageSyncGroup</span></span>](Get-AzStorageSyncGroup.md)
<span data-ttu-id="96f08-108">此命令會列出給定儲存同步服務內的所有同步群組。</span><span class="sxs-lookup"><span data-stu-id="96f08-108">This command lists all sync groups within a given storage sync service.</span></span>

### [<span data-ttu-id="96f08-109">Get-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="96f08-109">Get-AzStorageSyncServer</span></span>](Get-AzStorageSyncServer.md)
<span data-ttu-id="96f08-110">此命令會列出所有註冊至給定儲存同步處理服務的伺服器。</span><span class="sxs-lookup"><span data-stu-id="96f08-110">This command lists all servers registered to a given storage sync service.</span></span>

### [<span data-ttu-id="96f08-111">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="96f08-111">Get-AzStorageSyncServerEndpoint</span></span>](Get-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="96f08-112">此命令會列出特定同步處理群組內的所有伺服器端點。</span><span class="sxs-lookup"><span data-stu-id="96f08-112">This command lists all server endpoints within a given sync group.</span></span>

### [<span data-ttu-id="96f08-113">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="96f08-113">Get-AzStorageSyncService</span></span>](Get-AzStorageSyncService.md)
<span data-ttu-id="96f08-114">此命令會列出訂閱/資源群組範圍內的所有儲存同步服務。</span><span class="sxs-lookup"><span data-stu-id="96f08-114">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

### [<span data-ttu-id="96f08-115">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="96f08-115">Invoke-AzStorageSyncChangeDetection</span></span>](Invoke-AzStorageSyncChangeDetection.md)
<span data-ttu-id="96f08-116">此命令可用來手動啟動命名空間變更的偵測。</span><span class="sxs-lookup"><span data-stu-id="96f08-116">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="96f08-117">它可以鎖定至整個共用、子資料夾或一組檔案。</span><span class="sxs-lookup"><span data-stu-id="96f08-117">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="96f08-118">最多可偵測到 10，000 個變更。</span><span class="sxs-lookup"><span data-stu-id="96f08-118">A maximum of 10,000 changes can be detected.</span></span> <span data-ttu-id="96f08-119">如果您知道變更的範圍，將此命令的執行限制為命名空間的一部分，以便快速完成變更偵測，且在 10，000 個變更限制內完成。</span><span class="sxs-lookup"><span data-stu-id="96f08-119">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within a 10,000 changes limit.</span></span>

### [<span data-ttu-id="96f08-120">Invoke-AzStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="96f08-120">Invoke-AzStorageSyncCompatibilityCheck</span></span>](Invoke-AzStorageSyncCompatibilityCheck.md)
<span data-ttu-id="96f08-121">檢查系統與 Azure 檔案同步處理之間潛在的相容性問題。</span><span class="sxs-lookup"><span data-stu-id="96f08-121">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

### [<span data-ttu-id="96f08-122">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="96f08-122">Invoke-AzStorageSyncFileRecall</span></span>](Invoke-AzStorageSyncFileRecall.md)
<span data-ttu-id="96f08-123">此命令會回收所有分層檔案回局磁片。</span><span class="sxs-lookup"><span data-stu-id="96f08-123">This command recalls all tiered files back to local disk.</span></span>

### [<span data-ttu-id="96f08-124">New-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="96f08-124">New-AzStorageSyncCloudEndpoint</span></span>](New-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="96f08-125">此命令在同步處理群組中建立 Azure 檔案同步處理雲端端點。</span><span class="sxs-lookup"><span data-stu-id="96f08-125">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

### [<span data-ttu-id="96f08-126">New-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="96f08-126">New-AzStorageSyncGroup</span></span>](New-AzStorageSyncGroup.md)
<span data-ttu-id="96f08-127">此命令會于指定的儲存同步服務中建立新同步組。</span><span class="sxs-lookup"><span data-stu-id="96f08-127">This command creates a new sync group within a specified storage sync service.</span></span>

### [<span data-ttu-id="96f08-128">New-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="96f08-128">New-AzStorageSyncServerEndpoint</span></span>](New-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="96f08-129">此命令在已登錄的伺服器上建立新伺服器端點。</span><span class="sxs-lookup"><span data-stu-id="96f08-129">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="96f08-130">這可讓伺服器上指定的路徑開始同步處理群組中與其他端點的檔案。</span><span class="sxs-lookup"><span data-stu-id="96f08-130">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span>

### [<span data-ttu-id="96f08-131">New-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="96f08-131">New-AzStorageSyncService</span></span>](New-AzStorageSyncService.md)
<span data-ttu-id="96f08-132">此命令在資源群組中建立新的儲存同步服務。</span><span class="sxs-lookup"><span data-stu-id="96f08-132">This command creates a new storage sync service in a resource group.</span></span>

### [<span data-ttu-id="96f08-133">Set-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="96f08-133">Set-AzStorageSyncService</span></span>](New-AzStorageSyncService.md)
<span data-ttu-id="96f08-134">此命令會設定資源群組中的儲存空間同步服務。</span><span class="sxs-lookup"><span data-stu-id="96f08-134">This command sets a storage sync service in a resource group.</span></span>

### [<span data-ttu-id="96f08-135">Register-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="96f08-135">Register-AzStorageSyncServer</span></span>](Register-AzStorageSyncServer.md)
<span data-ttu-id="96f08-136">此命令會註冊伺服器至儲存同步處理服務，服務會建立信任關係。</span><span class="sxs-lookup"><span data-stu-id="96f08-136">This command registers a server to a storage sync service which creates a trust relationship.</span></span> <span data-ttu-id="96f08-137">PowerShell 或 Azure 入口網站之後，就可以在此伺服器上設定同步處理。</span><span class="sxs-lookup"><span data-stu-id="96f08-137">PowerShell or the Azure portal can then be used to configure sync on this server.</span></span>

### [<span data-ttu-id="96f08-138">Remove-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="96f08-138">Remove-AzStorageSyncCloudEndpoint</span></span>](Remove-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="96f08-139">此命令會從同步處理群組中刪除指定的雲端端點。</span><span class="sxs-lookup"><span data-stu-id="96f08-139">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="96f08-140">沒有至少一個雲端端點，此同步處理群組中沒有任何其他伺服器端點可以同步處理。</span><span class="sxs-lookup"><span data-stu-id="96f08-140">Without at least one cloud endpoint, no other server endpoints in this sync group can sync.</span></span>

### [<span data-ttu-id="96f08-141">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="96f08-141">Remove-AzStorageSyncGroup</span></span>](Remove-AzStorageSyncGroup.md)
<span data-ttu-id="96f08-142">此命令將會刪除指定的同步組。</span><span class="sxs-lookup"><span data-stu-id="96f08-142">This command will delete the specified sync group.</span></span>

### [<span data-ttu-id="96f08-143">Remove-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="96f08-143">Remove-AzStorageSyncServerEndpoint</span></span>](Remove-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="96f08-144">此命令將會刪除指定的伺服器端點。</span><span class="sxs-lookup"><span data-stu-id="96f08-144">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="96f08-145">同步處理到這個位置將會立即停止。</span><span class="sxs-lookup"><span data-stu-id="96f08-145">Sync to this location will stop immediately.</span></span>

### [<span data-ttu-id="96f08-146">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="96f08-146">Remove-AzStorageSyncService</span></span>](Remove-AzStorageSyncService.md)
<span data-ttu-id="96f08-147">此命令將會刪除指定的儲存同步服務。</span><span class="sxs-lookup"><span data-stu-id="96f08-147">This command will delete the specified storage sync service.</span></span>

### [<span data-ttu-id="96f08-148">Reset-AzStorageSyncServerCertificate</span><span class="sxs-lookup"><span data-stu-id="96f08-148">Reset-AzStorageSyncServerCertificate</span></span>](Reset-AzStorageSyncServerCertificate.md)
<span data-ttu-id="96f08-149">僅適用于疑難排解。</span><span class="sxs-lookup"><span data-stu-id="96f08-149">Use for troubleshooting only.</span></span> <span data-ttu-id="96f08-150">此命令會匯總儲存同步處理伺服器憑證，用來描述儲存空間同步處理服務的伺服器身分識別。</span><span class="sxs-lookup"><span data-stu-id="96f08-150">This command will roll the storage sync server certificate used to describe the server identity to the storage sync service.</span></span>

### [<span data-ttu-id="96f08-151">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="96f08-151">Set-AzStorageSyncServerEndpoint</span></span>](Set-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="96f08-152">此命令允許變更伺服器端點的可調整參數。</span><span class="sxs-lookup"><span data-stu-id="96f08-152">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

### [<span data-ttu-id="96f08-153">取消註冊-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="96f08-153">Unregister-AzStorageSyncServer</span></span>](Unregister-AzStorageSyncServer.md)
<span data-ttu-id="96f08-154">警告：取消註冊伺服器會導致此伺服器上所有伺服器端點的串聯刪除。</span><span class="sxs-lookup"><span data-stu-id="96f08-154">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="96f08-155">此命令會從儲存同步處理服務取消註冊伺服器。</span><span class="sxs-lookup"><span data-stu-id="96f08-155">This command will unregister a server from it's storage sync service.</span></span>

