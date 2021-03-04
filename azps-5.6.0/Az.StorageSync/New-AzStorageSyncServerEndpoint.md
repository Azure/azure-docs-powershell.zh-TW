---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/new-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: c76fd37e0a95c6ea5c39897c617602106979f94a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916849"
---
# <span data-ttu-id="9a687-101">New-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9a687-101">New-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="9a687-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9a687-102">SYNOPSIS</span></span>
<span data-ttu-id="9a687-103">此命令在已登錄的伺服器上建立新伺服器端點。</span><span class="sxs-lookup"><span data-stu-id="9a687-103">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="9a687-104">這可讓伺服器上指定的路徑開始同步處理群組中與其他端點的檔案。</span><span class="sxs-lookup"><span data-stu-id="9a687-104">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span>

## <span data-ttu-id="9a687-105">語法</span><span class="sxs-lookup"><span data-stu-id="9a687-105">SYNTAX</span></span>

### <span data-ttu-id="9a687-106">StringParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9a687-106">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -ServerResourceId <String> -ServerLocalPath <String> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>]
 [-OfflineDataTransferShareName <String>] [InitialDownloadPolicy] [LocalCacheMode] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a687-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a687-107">ObjectParameterSet</span></span>
```
New-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [InitialDownloadPolicy] [LocalCacheMode] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a687-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a687-108">ParentStringParameterSet</span></span>
```
New-AzStorageSyncServerEndpoint [-ParentResourceId] <String> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [InitialDownloadPolicy] [LocalCacheMode] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a687-109">描述</span><span class="sxs-lookup"><span data-stu-id="9a687-109">DESCRIPTION</span></span>
<span data-ttu-id="9a687-110">此命令在已登錄的伺服器上建立新伺服器端點。</span><span class="sxs-lookup"><span data-stu-id="9a687-110">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="9a687-111">這可讓伺服器上指定的路徑開始同步處理群組中與其他端點的檔案。</span><span class="sxs-lookup"><span data-stu-id="9a687-111">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span> <span data-ttu-id="9a687-112">如果同步處理群組中其他端點已有檔案，且新新增的位置也包含檔案，對帳程式會嘗試判斷檔案實際上是否與其他端點位於相同的資料夾中。</span><span class="sxs-lookup"><span data-stu-id="9a687-112">If there are already files on other endpoints in the sync group and this newly added location also contains files, a reconciliation process will attempt to determine if files are in fact the same ones in the same folders as on other endpoints.</span></span> <span data-ttu-id="9a687-113">命名空間會合並及對帳，有助於防止衝突檔案。</span><span class="sxs-lookup"><span data-stu-id="9a687-113">The namespaces will merge and reconciliation helps to prevent conflict files.</span></span> <span data-ttu-id="9a687-114">如果其他伺服器端點有檔案，通常最好從這個伺服器上空白的位置開始，讓雲端的檔案以稱為快速災害復原的自動程式下拉至伺服器。</span><span class="sxs-lookup"><span data-stu-id="9a687-114">If there are files on other server endpoints it is often better to start with an empty location on this server, so that the files from the cloud come down to the server in an automatic process called fast disaster recovery.</span></span> <span data-ttu-id="9a687-115">命名空間中繼資料會先向下同步處理，然後下載每個檔案的資料流程。</span><span class="sxs-lookup"><span data-stu-id="9a687-115">Namespace metadata will be synced down first, then the data stream of each file is downloaded.</span></span> <span data-ttu-id="9a687-116">如果使用者或應用程式在下載順序外要求檔案，該檔案會優先回收，以滿足存取要求。</span><span class="sxs-lookup"><span data-stu-id="9a687-116">If a file is requested by a user or application out of download order, that file will be recalled with priority to satisfy the access request.</span></span> <span data-ttu-id="9a687-117">您可以選擇性地在此伺服器端點使用雲端分層，以判斷此端點是否應成為來自雲端之完整檔案集的緩存。</span><span class="sxs-lookup"><span data-stu-id="9a687-117">You can optionally use cloud tiering on this server endpoint to determine if this endpoint is supposed to become a cache of the complete set of files from the cloud.</span></span> <span data-ttu-id="9a687-118">如果使用雲端分層，檔案內容下載會從您可以設定之雲端分層策略定義的點停止。</span><span class="sxs-lookup"><span data-stu-id="9a687-118">If cloud tiering is used, then the file content download will stop at the point defined by the cloud tiering policies you can set.</span></span>

## <span data-ttu-id="9a687-119">例子</span><span class="sxs-lookup"><span data-stu-id="9a687-119">EXAMPLES</span></span>

### <span data-ttu-id="9a687-120">範例 1</span><span class="sxs-lookup"><span data-stu-id="9a687-120">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> New-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName" -ServerResourceId $RegisteredServer.ResourceId -ServerLocalPath "myServerLocalPath" -CloudTiering -OfflineDataTransfer -OfflineDataTransferShareName "myOfflineDataTransferShareName" -TierFilesOlderThanDays "myTierFilesOlderThanDays"
```

<span data-ttu-id="9a687-121">此命令在已登錄的伺服器上建立新伺服器端點，並將它插入同步處理群組。</span><span class="sxs-lookup"><span data-stu-id="9a687-121">This command creates a new server endpoint on a registered server and inserts it into a sync group.</span></span> <span data-ttu-id="9a687-122">THis 方式，它是其他端點之拓撲的一部分，而檔案中繼資料和內容會立即開始在同步處理群組中參照為端點的所有位置之間同步處理。</span><span class="sxs-lookup"><span data-stu-id="9a687-122">THis way it is part of a topology of other endpoints and file metadata and content will immediately start to sync between all locations referenced as endpoints in the sync group.</span></span>

## <span data-ttu-id="9a687-123">參數</span><span class="sxs-lookup"><span data-stu-id="9a687-123">PARAMETERS</span></span>

### <span data-ttu-id="9a687-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a687-124">-AsJob</span></span>
<span data-ttu-id="9a687-125">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9a687-125">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a687-126">-CloudTiering</span><span class="sxs-lookup"><span data-stu-id="9a687-126">-CloudTiering</span></span>
<span data-ttu-id="9a687-127">雲端分層參數</span><span class="sxs-lookup"><span data-stu-id="9a687-127">Cloud Tiering Parameter</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a687-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a687-128">-DefaultProfile</span></span>
<span data-ttu-id="9a687-129">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9a687-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a687-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="9a687-130">-Name</span></span>
<span data-ttu-id="9a687-131">ServerEndpoint 的名稱。</span><span class="sxs-lookup"><span data-stu-id="9a687-131">Name of the ServerEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerEndpointName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a687-132">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="9a687-132">-OfflineDataTransfer</span></span>
<span data-ttu-id="9a687-133">雲端來源資料參數</span><span class="sxs-lookup"><span data-stu-id="9a687-133">Cloud Seeded Data Parameter</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a687-134">-OfflineDataTransferShareName</span><span class="sxs-lookup"><span data-stu-id="9a687-134">-OfflineDataTransferShareName</span></span>
<span data-ttu-id="9a687-135">雲端樹種資料檔案共用 Uri 參數</span><span class="sxs-lookup"><span data-stu-id="9a687-135">Cloud Seeded Data File Share Uri Parameter</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a687-136">-initialDownloadPolicy</span><span class="sxs-lookup"><span data-stu-id="9a687-136">-initialDownloadPolicy</span></span>
<span data-ttu-id="9a687-137">本機快取模式參數</span><span class="sxs-lookup"><span data-stu-id="9a687-137">Local cache mode Parameter</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a687-138">-localCacheMode</span><span class="sxs-lookup"><span data-stu-id="9a687-138">-localCacheMode</span></span>
<span data-ttu-id="9a687-139">本機快取模式參數</span><span class="sxs-lookup"><span data-stu-id="9a687-139">Local cache mode Parameter</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a687-140">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9a687-140">-ParentObject</span></span>
<span data-ttu-id="9a687-141">SyncGroup 物件，通常會通過參數。</span><span class="sxs-lookup"><span data-stu-id="9a687-141">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup
Parameter Sets: ObjectParameterSet
Aliases: SyncGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a687-142">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="9a687-142">-ParentResourceId</span></span>
<span data-ttu-id="9a687-143">SyncGroup 父資源識別碼</span><span class="sxs-lookup"><span data-stu-id="9a687-143">SyncGroup Parent Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: SyncGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a687-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a687-144">-ResourceGroupName</span></span>
<span data-ttu-id="9a687-145">資源組名。</span><span class="sxs-lookup"><span data-stu-id="9a687-145">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a687-146">-ServerLocalPath</span><span class="sxs-lookup"><span data-stu-id="9a687-146">-ServerLocalPath</span></span>
<span data-ttu-id="9a687-147">伺服器本地路徑參數</span><span class="sxs-lookup"><span data-stu-id="9a687-147">Server Local Path Parameter</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a687-148">-ServerResourceId</span><span class="sxs-lookup"><span data-stu-id="9a687-148">-ServerResourceId</span></span>
<span data-ttu-id="9a687-149">RegisteredServer 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="9a687-149">RegisteredServer Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a687-150">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="9a687-150">-StorageSyncServiceName</span></span>
<span data-ttu-id="9a687-151">StorageSyncService 的名稱。</span><span class="sxs-lookup"><span data-stu-id="9a687-151">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a687-152">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="9a687-152">-SyncGroupName</span></span>
<span data-ttu-id="9a687-153">同步組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9a687-153">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a687-154">-TierFilesOlderDays</span><span class="sxs-lookup"><span data-stu-id="9a687-154">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="9a687-155">超過天數的第層檔案參數</span><span class="sxs-lookup"><span data-stu-id="9a687-155">Tier Files Older Than Days Parameter</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a687-156">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="9a687-156">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="9a687-157">大量可用空間百分比參數</span><span class="sxs-lookup"><span data-stu-id="9a687-157">Volume Free Space Percent Parameter</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a687-158">-確認</span><span class="sxs-lookup"><span data-stu-id="9a687-158">-Confirm</span></span>
<span data-ttu-id="9a687-159">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9a687-159">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a687-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a687-160">-WhatIf</span></span>
<span data-ttu-id="9a687-161">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9a687-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9a687-162">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9a687-162">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a687-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a687-163">CommonParameters</span></span>
<span data-ttu-id="9a687-164">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9a687-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a687-165">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="9a687-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a687-166">輸入</span><span class="sxs-lookup"><span data-stu-id="9a687-166">INPUTS</span></span>

### <span data-ttu-id="9a687-167">Microsoft.Azure.Commands.StorageSync.models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="9a687-167">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="9a687-168">System.String</span><span class="sxs-lookup"><span data-stu-id="9a687-168">System.String</span></span>

## <span data-ttu-id="9a687-169">輸出</span><span class="sxs-lookup"><span data-stu-id="9a687-169">OUTPUTS</span></span>

### <span data-ttu-id="9a687-170">Microsoft.Azure.Commands.StorageSync.models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9a687-170">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="9a687-171">筆記</span><span class="sxs-lookup"><span data-stu-id="9a687-171">NOTES</span></span>

## <span data-ttu-id="9a687-172">相關連結</span><span class="sxs-lookup"><span data-stu-id="9a687-172">RELATED LINKS</span></span>
