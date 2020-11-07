---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 524e9334b3e706dc51a2dfd4efc5d6f3cce710c7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793192"
---
# <span data-ttu-id="864b5-101">New-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="864b5-101">New-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="864b5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="864b5-102">SYNOPSIS</span></span>
<span data-ttu-id="864b5-103">這個命令會在已註冊的伺服器上建立新的伺服器端點。</span><span class="sxs-lookup"><span data-stu-id="864b5-103">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="864b5-104">這可讓伺服器上的指定路徑開始與同步群組中的其他端點同步處理檔案。</span><span class="sxs-lookup"><span data-stu-id="864b5-104">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span>

## <span data-ttu-id="864b5-105">句法</span><span class="sxs-lookup"><span data-stu-id="864b5-105">SYNTAX</span></span>

### <span data-ttu-id="864b5-106">StringParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="864b5-106">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -ServerResourceId <String> -ServerLocalPath <String> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>]
 [-OfflineDataTransferShareName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="864b5-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="864b5-107">ObjectParameterSet</span></span>
```
New-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="864b5-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="864b5-108">ParentStringParameterSet</span></span>
```
New-AzStorageSyncServerEndpoint [-ParentResourceId] <String> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="864b5-109">說明</span><span class="sxs-lookup"><span data-stu-id="864b5-109">DESCRIPTION</span></span>
<span data-ttu-id="864b5-110">這個命令會在已註冊的伺服器上建立新的伺服器端點。</span><span class="sxs-lookup"><span data-stu-id="864b5-110">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="864b5-111">這可讓伺服器上的指定路徑開始與同步群組中的其他端點同步處理檔案。</span><span class="sxs-lookup"><span data-stu-id="864b5-111">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span> <span data-ttu-id="864b5-112">如果同步群組中的其他端點上已有檔案，而且這個新加入的位置也包含檔案，則調解程式將會嘗試判斷檔案與其他端點的相同資料夾中是否確實相同。</span><span class="sxs-lookup"><span data-stu-id="864b5-112">If there are already files on other endpoints in the sync group and this newly added location also contains files, a reconciliation process will attempt to determine if files are in fact the same ones in the same folders as on other endpoints.</span></span> <span data-ttu-id="864b5-113">命名空間將會合並，並可協助防止衝突檔案。</span><span class="sxs-lookup"><span data-stu-id="864b5-113">The namespaces will merge and reconciliation helps to prevent conflict files.</span></span> <span data-ttu-id="864b5-114">如果在其他伺服器端點上有檔案，通常最好從該伺服器上的空白位置開始，這樣來自雲端的檔案會在稱為快速災難復原的自動程式集中傳送給伺服器。</span><span class="sxs-lookup"><span data-stu-id="864b5-114">If there are files on other server endpoints it is often better to start with an empty location on this server, so that the files from the cloud come down to the server in an automatic process called fast disaster recovery.</span></span> <span data-ttu-id="864b5-115">命名空間中繼資料會先同步處理，然後下載每個檔案的資料流程。</span><span class="sxs-lookup"><span data-stu-id="864b5-115">Namespace metadata will be synced down first, then the data stream of each file is downloaded.</span></span> <span data-ttu-id="864b5-116">如果使用者或應用程式要求檔案不是下載順序，該檔案將會以優先順序來撤回，以符合存取要求。</span><span class="sxs-lookup"><span data-stu-id="864b5-116">If a file is requested by a user or application out of download order, that file will be recalled with priority to satisfy the access request.</span></span> <span data-ttu-id="864b5-117">您也可以選擇在此伺服器端點上使用雲端堆疊來判斷這個端點是否應該成為雲端檔案的完整檔案集的快取。</span><span class="sxs-lookup"><span data-stu-id="864b5-117">You can optionally use cloud tiering on this server endpoint to determine if this endpoint is supposed to become a cache of the complete set of files from the cloud.</span></span> <span data-ttu-id="864b5-118">如果使用雲端分層，則檔案內容下載將會停止于您可以設定的雲端堆疊原則所定義的點。</span><span class="sxs-lookup"><span data-stu-id="864b5-118">If cloud tiering is used, then the file content download will stop at the point defined by the cloud tiering policies you can set.</span></span>

## <span data-ttu-id="864b5-119">示例</span><span class="sxs-lookup"><span data-stu-id="864b5-119">EXAMPLES</span></span>

### <span data-ttu-id="864b5-120">範例1</span><span class="sxs-lookup"><span data-stu-id="864b5-120">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> New-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName" -ServerResourceId $RegisteredServer.ResourceId -ServerLocalPath "myServerLocalPath" -CloudTiering -OfflineDataTransfer -OfflineDataTransferShareName "myOfflineDataTransferShareName" -TierFilesOlderThanDays "myTierFilesOlderThanDays"
```

<span data-ttu-id="864b5-121">這個命令會在已註冊的伺服器上建立新的伺服器端點，並將它插入到同步處理群組中。</span><span class="sxs-lookup"><span data-stu-id="864b5-121">This command creates a new server endpoint on a registered server and inserts it into a sync group.</span></span> <span data-ttu-id="864b5-122">如此一來，它是其他端點拓撲的一部分，而檔案中繼資料和內容將會立即開始在同步處理群組中參照為端點的所有位置之間進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="864b5-122">THis way it is part of a topology of other endpoints and file metadata and content will immediately start to sync between all locations referenced as endpoints in the sync group.</span></span>

## <span data-ttu-id="864b5-123">參數</span><span class="sxs-lookup"><span data-stu-id="864b5-123">PARAMETERS</span></span>

### <span data-ttu-id="864b5-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="864b5-124">-AsJob</span></span>
<span data-ttu-id="864b5-125">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="864b5-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="864b5-126">-CloudTiering</span><span class="sxs-lookup"><span data-stu-id="864b5-126">-CloudTiering</span></span>
<span data-ttu-id="864b5-127">雲端堆疊參數</span><span class="sxs-lookup"><span data-stu-id="864b5-127">Cloud Tiering Parameter</span></span>

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

### <span data-ttu-id="864b5-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="864b5-128">-DefaultProfile</span></span>
<span data-ttu-id="864b5-129">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="864b5-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="864b5-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="864b5-130">-Name</span></span>
<span data-ttu-id="864b5-131">ServerEndpoint 的名稱。</span><span class="sxs-lookup"><span data-stu-id="864b5-131">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="864b5-132">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="864b5-132">-OfflineDataTransfer</span></span>
<span data-ttu-id="864b5-133">雲端種子資料參數</span><span class="sxs-lookup"><span data-stu-id="864b5-133">Cloud Seeded Data Parameter</span></span>

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

### <span data-ttu-id="864b5-134">-OfflineDataTransferShareName</span><span class="sxs-lookup"><span data-stu-id="864b5-134">-OfflineDataTransferShareName</span></span>
<span data-ttu-id="864b5-135">雲端種子資料檔案共用 Uri 參數</span><span class="sxs-lookup"><span data-stu-id="864b5-135">Cloud Seeded Data File Share Uri Parameter</span></span>

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

### <span data-ttu-id="864b5-136">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="864b5-136">-ParentObject</span></span>
<span data-ttu-id="864b5-137">SyncGroup 物件，通常是透過參數傳遞。</span><span class="sxs-lookup"><span data-stu-id="864b5-137">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="864b5-138">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="864b5-138">-ParentResourceId</span></span>
<span data-ttu-id="864b5-139">SyncGroup 父資源識別碼</span><span class="sxs-lookup"><span data-stu-id="864b5-139">SyncGroup Parent Resource Id</span></span>

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

### <span data-ttu-id="864b5-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="864b5-140">-ResourceGroupName</span></span>
<span data-ttu-id="864b5-141">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="864b5-141">Resource Group Name.</span></span>

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

### <span data-ttu-id="864b5-142">-ServerLocalPath</span><span class="sxs-lookup"><span data-stu-id="864b5-142">-ServerLocalPath</span></span>
<span data-ttu-id="864b5-143">伺服器本機路徑參數</span><span class="sxs-lookup"><span data-stu-id="864b5-143">Server Local Path Parameter</span></span>

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

### <span data-ttu-id="864b5-144">-ServerResourceId</span><span class="sxs-lookup"><span data-stu-id="864b5-144">-ServerResourceId</span></span>
<span data-ttu-id="864b5-145">RegisteredServer 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="864b5-145">RegisteredServer Resource Id</span></span>

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

### <span data-ttu-id="864b5-146">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="864b5-146">-StorageSyncServiceName</span></span>
<span data-ttu-id="864b5-147">StorageSyncService 的名稱。</span><span class="sxs-lookup"><span data-stu-id="864b5-147">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="864b5-148">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="864b5-148">-SyncGroupName</span></span>
<span data-ttu-id="864b5-149">SyncGroup 的名稱。</span><span class="sxs-lookup"><span data-stu-id="864b5-149">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="864b5-150">-TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="864b5-150">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="864b5-151">[層檔案超過天數] 參數</span><span class="sxs-lookup"><span data-stu-id="864b5-151">Tier Files Older Than Days Parameter</span></span>

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

### <span data-ttu-id="864b5-152">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="864b5-152">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="864b5-153">Volume 可用空間百分比參數</span><span class="sxs-lookup"><span data-stu-id="864b5-153">Volume Free Space Percent Parameter</span></span>

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

### <span data-ttu-id="864b5-154">-確認</span><span class="sxs-lookup"><span data-stu-id="864b5-154">-Confirm</span></span>
<span data-ttu-id="864b5-155">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="864b5-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="864b5-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="864b5-156">-WhatIf</span></span>
<span data-ttu-id="864b5-157">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="864b5-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="864b5-158">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="864b5-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="864b5-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="864b5-159">CommonParameters</span></span>
<span data-ttu-id="864b5-160">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="864b5-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="864b5-161">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="864b5-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="864b5-162">輸入</span><span class="sxs-lookup"><span data-stu-id="864b5-162">INPUTS</span></span>

### <span data-ttu-id="864b5-163">PSSyncGroup 中的 StorageSync。</span><span class="sxs-lookup"><span data-stu-id="864b5-163">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="864b5-164">System.object</span><span class="sxs-lookup"><span data-stu-id="864b5-164">System.String</span></span>

## <span data-ttu-id="864b5-165">輸出</span><span class="sxs-lookup"><span data-stu-id="864b5-165">OUTPUTS</span></span>

### <span data-ttu-id="864b5-166">PSServerEndpoint 中的 StorageSync。</span><span class="sxs-lookup"><span data-stu-id="864b5-166">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="864b5-167">筆記</span><span class="sxs-lookup"><span data-stu-id="864b5-167">NOTES</span></span>

## <span data-ttu-id="864b5-168">相關連結</span><span class="sxs-lookup"><span data-stu-id="864b5-168">RELATED LINKS</span></span>
