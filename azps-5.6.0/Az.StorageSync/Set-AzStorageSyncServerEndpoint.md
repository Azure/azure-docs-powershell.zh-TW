---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/set-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 65df82b189442a32738e445a1b48093c18816bbc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907422"
---
# <span data-ttu-id="b5f2c-101">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b5f2c-101">Set-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="b5f2c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b5f2c-102">SYNOPSIS</span></span>
<span data-ttu-id="b5f2c-103">此命令允許變更伺服器端點的可調整參數。</span><span class="sxs-lookup"><span data-stu-id="b5f2c-103">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

## <span data-ttu-id="b5f2c-104">語法</span><span class="sxs-lookup"><span data-stu-id="b5f2c-104">SYNTAX</span></span>

### <span data-ttu-id="b5f2c-105">StringParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b5f2c-105">StringParameterSet (Default)</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [LocalCacheMode] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5f2c-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5f2c-106">ResourceIdParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceId] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [LocalCacheMode] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5f2c-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5f2c-107">ObjectParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [LocalCacheMode] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5f2c-108">描述</span><span class="sxs-lookup"><span data-stu-id="b5f2c-108">DESCRIPTION</span></span>
<span data-ttu-id="b5f2c-109">此命令允許變更伺服器端點的可調整參數。</span><span class="sxs-lookup"><span data-stu-id="b5f2c-109">This command allows for changes on the adjustable parameters of a server endpoint.</span></span> <span data-ttu-id="b5f2c-110">例如，您隨時都可以變更雲端分層和雲端分層策略。</span><span class="sxs-lookup"><span data-stu-id="b5f2c-110">For instance cloud tiering and cloud tiering policies can be changed at any time.</span></span> <span data-ttu-id="b5f2c-111">伺服器端點的數個層面 ，例如本地路徑，在建立伺服器端點之後無法變更。</span><span class="sxs-lookup"><span data-stu-id="b5f2c-111">Several aspects of a server endpoint, such as the local path, cannot be changed after the server endpoint had been created.</span></span>

## <span data-ttu-id="b5f2c-112">例子</span><span class="sxs-lookup"><span data-stu-id="b5f2c-112">EXAMPLES</span></span>

### <span data-ttu-id="b5f2c-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="b5f2c-113">Example 1</span></span>
```powershell
PS C:\> Set-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"  -TierFilesOlderThanDays 30 -OfflineDataTransfer -OfflineDataTransfer $false
```

<span data-ttu-id="b5f2c-114">此範例會執行兩個動作，它會在指定的伺服器端點上設定新的雲端分層策略，引導伺服器對過去 30 天內未存取的所有檔案進行分層，同時也會停用離線資料傳輸模式，此模式最初是在建立時在此伺服器端點上啟用。</span><span class="sxs-lookup"><span data-stu-id="b5f2c-114">This example performs two actions, it sets a new cloud tiering policy on the specified server endpoint, which directs the server to tier all files that have not been accessed in the past 30 days and it also disables the offline data transfer mode, which was initially enabled on this server endpoint during it's creation.</span></span> <span data-ttu-id="b5f2c-115">離線資料傳輸會做為大量移轉服務的互通性的一部分，例如 Azure Data Box。</span><span class="sxs-lookup"><span data-stu-id="b5f2c-115">Offline data transfer is used as part of interoperability with bulk migration services, such as Azure Data Box.</span></span>

## <span data-ttu-id="b5f2c-116">參數</span><span class="sxs-lookup"><span data-stu-id="b5f2c-116">PARAMETERS</span></span>

### <span data-ttu-id="b5f2c-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b5f2c-117">-AsJob</span></span>
<span data-ttu-id="b5f2c-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b5f2c-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b5f2c-119">-CloudTiering</span><span class="sxs-lookup"><span data-stu-id="b5f2c-119">-CloudTiering</span></span>
<span data-ttu-id="b5f2c-120">雲端分層參數</span><span class="sxs-lookup"><span data-stu-id="b5f2c-120">Cloud Tiering Parameter</span></span>

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

### <span data-ttu-id="b5f2c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5f2c-121">-DefaultProfile</span></span>
<span data-ttu-id="b5f2c-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b5f2c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5f2c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5f2c-123">-InputObject</span></span>
<span data-ttu-id="b5f2c-124">SyncGroup 物件，通常會通過參數。</span><span class="sxs-lookup"><span data-stu-id="b5f2c-124">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint
Parameter Sets: ObjectParameterSet
Aliases: RegisteredServer

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5f2c-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="b5f2c-125">-Name</span></span>
<span data-ttu-id="b5f2c-126">ServerEndpoint 的名稱。</span><span class="sxs-lookup"><span data-stu-id="b5f2c-126">Name of the ServerEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ServerEndpointName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5f2c-127">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="b5f2c-127">-OfflineDataTransfer</span></span>
<span data-ttu-id="b5f2c-128">雲端來源資料參數</span><span class="sxs-lookup"><span data-stu-id="b5f2c-128">Cloud Seeded Data Parameter</span></span>

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

### <span data-ttu-id="b5f2c-129">-localCacheMode</span><span class="sxs-lookup"><span data-stu-id="b5f2c-129">-localCacheMode</span></span>
<span data-ttu-id="b5f2c-130">本機快取模式參數</span><span class="sxs-lookup"><span data-stu-id="b5f2c-130">Local cache mode Parameter</span></span>

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

### <span data-ttu-id="b5f2c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5f2c-131">-ResourceGroupName</span></span>
<span data-ttu-id="b5f2c-132">資源組名。</span><span class="sxs-lookup"><span data-stu-id="b5f2c-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="b5f2c-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5f2c-133">-ResourceId</span></span>
<span data-ttu-id="b5f2c-134">ServerEndpoint 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="b5f2c-134">ServerEndpoint Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5f2c-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="b5f2c-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="b5f2c-136">StorageSyncService 的名稱。</span><span class="sxs-lookup"><span data-stu-id="b5f2c-136">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="b5f2c-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="b5f2c-137">-SyncGroupName</span></span>
<span data-ttu-id="b5f2c-138">同步組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b5f2c-138">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="b5f2c-139">-TierFilesOlderDays</span><span class="sxs-lookup"><span data-stu-id="b5f2c-139">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="b5f2c-140">超過天數的第層檔案參數</span><span class="sxs-lookup"><span data-stu-id="b5f2c-140">Tier Files Older Than Days Parameter</span></span>

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

### <span data-ttu-id="b5f2c-141">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="b5f2c-141">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="b5f2c-142">大量可用空間百分比參數</span><span class="sxs-lookup"><span data-stu-id="b5f2c-142">Volume Free Space Percent Parameter</span></span>

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

### <span data-ttu-id="b5f2c-143">-確認</span><span class="sxs-lookup"><span data-stu-id="b5f2c-143">-Confirm</span></span>
<span data-ttu-id="b5f2c-144">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b5f2c-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5f2c-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5f2c-145">-WhatIf</span></span>
<span data-ttu-id="b5f2c-146">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b5f2c-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b5f2c-147">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b5f2c-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5f2c-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5f2c-148">CommonParameters</span></span>
<span data-ttu-id="b5f2c-149">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b5f2c-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5f2c-150">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="b5f2c-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5f2c-151">輸入</span><span class="sxs-lookup"><span data-stu-id="b5f2c-151">INPUTS</span></span>

### <span data-ttu-id="b5f2c-152">System.String</span><span class="sxs-lookup"><span data-stu-id="b5f2c-152">System.String</span></span>

### <span data-ttu-id="b5f2c-153">Microsoft.Azure.Commands.StorageSync.models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b5f2c-153">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="b5f2c-154">輸出</span><span class="sxs-lookup"><span data-stu-id="b5f2c-154">OUTPUTS</span></span>

### <span data-ttu-id="b5f2c-155">Microsoft.Azure.Commands.StorageSync.models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b5f2c-155">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="b5f2c-156">筆記</span><span class="sxs-lookup"><span data-stu-id="b5f2c-156">NOTES</span></span>

## <span data-ttu-id="b5f2c-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="b5f2c-157">RELATED LINKS</span></span>
