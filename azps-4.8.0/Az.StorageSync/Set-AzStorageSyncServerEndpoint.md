---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/set-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: b8adfd7c069c4215ec8f26d259ed9d1bc39be2d9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971600"
---
# <span data-ttu-id="a9860-101">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a9860-101">Set-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="a9860-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a9860-102">SYNOPSIS</span></span>
<span data-ttu-id="a9860-103">這個命令可讓您變更伺服器端點的可調參數。</span><span class="sxs-lookup"><span data-stu-id="a9860-103">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

## <span data-ttu-id="a9860-104">句法</span><span class="sxs-lookup"><span data-stu-id="a9860-104">SYNTAX</span></span>

### <span data-ttu-id="a9860-105">StringParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a9860-105">StringParameterSet (Default)</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [LocalCacheMode] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9860-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9860-106">ResourceIdParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceId] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [LocalCacheMode] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9860-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9860-107">ObjectParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [LocalCacheMode] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9860-108">說明</span><span class="sxs-lookup"><span data-stu-id="a9860-108">DESCRIPTION</span></span>
<span data-ttu-id="a9860-109">這個命令可讓您變更伺服器端點的可調參數。</span><span class="sxs-lookup"><span data-stu-id="a9860-109">This command allows for changes on the adjustable parameters of a server endpoint.</span></span> <span data-ttu-id="a9860-110">舉例來說，您可以隨時變更雲端分層和雲端堆疊原則。</span><span class="sxs-lookup"><span data-stu-id="a9860-110">For instance cloud tiering and cloud tiering policies can be changed at any time.</span></span> <span data-ttu-id="a9860-111">在建立伺服器端點之後，就無法變更伺服器端點（例如本機路徑）的幾個方面。</span><span class="sxs-lookup"><span data-stu-id="a9860-111">Several aspects of a server endpoint, such as the local path, cannot be changed after the server endpoint had been created.</span></span>

## <span data-ttu-id="a9860-112">示例</span><span class="sxs-lookup"><span data-stu-id="a9860-112">EXAMPLES</span></span>

### <span data-ttu-id="a9860-113">範例1</span><span class="sxs-lookup"><span data-stu-id="a9860-113">Example 1</span></span>
```powershell
PS C:\> Set-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"  -TierFilesOlderThanDays 30 -OfflineDataTransfer -OfflineDataTransfer $false
```

<span data-ttu-id="a9860-114">這個範例會執行兩個動作，它會在指定的伺服器端點上設定新的雲端堆疊原則，這會指示伺服器將過去30天內未存取的所有檔案分級，而且也會停用離線資料傳輸模式，這是在建立期間在這個伺服器端點上啟用。</span><span class="sxs-lookup"><span data-stu-id="a9860-114">This example performs two actions, it sets a new cloud tiering policy on the specified server endpoint, which directs the server to tier all files that have not been accessed in the past 30 days and it also disables the offline data transfer mode, which was initially enabled on this server endpoint during it's creation.</span></span> <span data-ttu-id="a9860-115">離線資料傳輸是使用大量遷移服務（例如 Azure 資料盒）的互通性的一部分。</span><span class="sxs-lookup"><span data-stu-id="a9860-115">Offline data transfer is used as part of interoperability with bulk migration services, such as Azure Data Box.</span></span>

## <span data-ttu-id="a9860-116">參數</span><span class="sxs-lookup"><span data-stu-id="a9860-116">PARAMETERS</span></span>

### <span data-ttu-id="a9860-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a9860-117">-AsJob</span></span>
<span data-ttu-id="a9860-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a9860-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a9860-119">-CloudTiering</span><span class="sxs-lookup"><span data-stu-id="a9860-119">-CloudTiering</span></span>
<span data-ttu-id="a9860-120">雲端堆疊參數</span><span class="sxs-lookup"><span data-stu-id="a9860-120">Cloud Tiering Parameter</span></span>

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

### <span data-ttu-id="a9860-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9860-121">-DefaultProfile</span></span>
<span data-ttu-id="a9860-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a9860-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9860-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9860-123">-InputObject</span></span>
<span data-ttu-id="a9860-124">SyncGroup 物件，通常是透過參數傳遞。</span><span class="sxs-lookup"><span data-stu-id="a9860-124">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="a9860-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="a9860-125">-Name</span></span>
<span data-ttu-id="a9860-126">ServerEndpoint 的名稱。</span><span class="sxs-lookup"><span data-stu-id="a9860-126">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="a9860-127">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="a9860-127">-OfflineDataTransfer</span></span>
<span data-ttu-id="a9860-128">雲端種子資料參數</span><span class="sxs-lookup"><span data-stu-id="a9860-128">Cloud Seeded Data Parameter</span></span>

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

### <span data-ttu-id="a9860-129">-localCacheMode</span><span class="sxs-lookup"><span data-stu-id="a9860-129">-localCacheMode</span></span>
<span data-ttu-id="a9860-130">本機快取模式參數</span><span class="sxs-lookup"><span data-stu-id="a9860-130">Local cache mode Parameter</span></span>

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

### <span data-ttu-id="a9860-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9860-131">-ResourceGroupName</span></span>
<span data-ttu-id="a9860-132">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="a9860-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="a9860-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9860-133">-ResourceId</span></span>
<span data-ttu-id="a9860-134">ServerEndpoint 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="a9860-134">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="a9860-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="a9860-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="a9860-136">StorageSyncService 的名稱。</span><span class="sxs-lookup"><span data-stu-id="a9860-136">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="a9860-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="a9860-137">-SyncGroupName</span></span>
<span data-ttu-id="a9860-138">SyncGroup 的名稱。</span><span class="sxs-lookup"><span data-stu-id="a9860-138">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="a9860-139">-TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="a9860-139">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="a9860-140">[層檔案超過天數] 參數</span><span class="sxs-lookup"><span data-stu-id="a9860-140">Tier Files Older Than Days Parameter</span></span>

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

### <span data-ttu-id="a9860-141">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="a9860-141">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="a9860-142">Volume 可用空間百分比參數</span><span class="sxs-lookup"><span data-stu-id="a9860-142">Volume Free Space Percent Parameter</span></span>

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

### <span data-ttu-id="a9860-143">-確認</span><span class="sxs-lookup"><span data-stu-id="a9860-143">-Confirm</span></span>
<span data-ttu-id="a9860-144">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a9860-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9860-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9860-145">-WhatIf</span></span>
<span data-ttu-id="a9860-146">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a9860-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a9860-147">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a9860-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9860-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9860-148">CommonParameters</span></span>
<span data-ttu-id="a9860-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a9860-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9860-150">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a9860-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9860-151">輸入</span><span class="sxs-lookup"><span data-stu-id="a9860-151">INPUTS</span></span>

### <span data-ttu-id="a9860-152">System.object</span><span class="sxs-lookup"><span data-stu-id="a9860-152">System.String</span></span>

### <span data-ttu-id="a9860-153">PSServerEndpoint 中的 StorageSync。</span><span class="sxs-lookup"><span data-stu-id="a9860-153">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="a9860-154">輸出</span><span class="sxs-lookup"><span data-stu-id="a9860-154">OUTPUTS</span></span>

### <span data-ttu-id="a9860-155">PSServerEndpoint 中的 StorageSync。</span><span class="sxs-lookup"><span data-stu-id="a9860-155">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="a9860-156">筆記</span><span class="sxs-lookup"><span data-stu-id="a9860-156">NOTES</span></span>

## <span data-ttu-id="a9860-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="a9860-157">RELATED LINKS</span></span>