---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/new-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCacheStorageTarget.md
ms.openlocfilehash: deb359905086d68edb4129e023ce6dd8d2ceaf10
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917305"
---
# <span data-ttu-id="5ffa1-101">New-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="5ffa1-101">New-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="5ffa1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5ffa1-102">SYNOPSIS</span></span>
<span data-ttu-id="5ffa1-103">建立儲存目標。</span><span class="sxs-lookup"><span data-stu-id="5ffa1-103">Creates a Storage Target.</span></span>

## <span data-ttu-id="5ffa1-104">語法</span><span class="sxs-lookup"><span data-stu-id="5ffa1-104">SYNTAX</span></span>

### <span data-ttu-id="5ffa1-105">ClfsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5ffa1-105">ClfsParameterSet (Default)</span></span>
```
New-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-CLFS]
 [-StorageContainerID <String>] [-Junction <Hashtable[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ffa1-106">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ffa1-106">NfsParameterSet</span></span>
```
New-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-NFS]
 [-HostName <String>] [-UsageModel <String>] [-Junction <Hashtable[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ffa1-107">描述</span><span class="sxs-lookup"><span data-stu-id="5ffa1-107">DESCRIPTION</span></span>
<span data-ttu-id="5ffa1-108">**New-AzHpcCacheStorageTarget** Cmdlet 會將儲存目標新增到 Azure HPC Cache。</span><span class="sxs-lookup"><span data-stu-id="5ffa1-108">The **New-AzHpcCacheStorageTarget** cmdlet adds a Storage Target to Azure HPC Cache.</span></span>

## <span data-ttu-id="5ffa1-109">例子</span><span class="sxs-lookup"><span data-stu-id="5ffa1-109">EXAMPLES</span></span>

### <span data-ttu-id="5ffa1-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="5ffa1-110">Example 1</span></span>
```powershell
PS C:\> New-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -CLFS -StorageContainerID "/subscriptions/testsub/resourceGroups/testRG/providers/Microsoft.Storage/storageAccounts/testdstorageaccount/blobServices/default/containers/testcontainer" -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

### <span data-ttu-id="5ffa1-111">範例 2</span><span class="sxs-lookup"><span data-stu-id="5ffa1-111">Example 2</span></span>
```powershell
PS C:\> New-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -NFS -UsageModel "READ_HEAVY_INFREQ" -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

## <span data-ttu-id="5ffa1-112">參數</span><span class="sxs-lookup"><span data-stu-id="5ffa1-112">PARAMETERS</span></span>

### <span data-ttu-id="5ffa1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5ffa1-113">-AsJob</span></span>
<span data-ttu-id="5ffa1-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5ffa1-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5ffa1-115">-CacheName</span><span class="sxs-lookup"><span data-stu-id="5ffa1-115">-CacheName</span></span>
<span data-ttu-id="5ffa1-116">緩存名稱。</span><span class="sxs-lookup"><span data-stu-id="5ffa1-116">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ffa1-117">-CLFS</span><span class="sxs-lookup"><span data-stu-id="5ffa1-117">-CLFS</span></span>
<span data-ttu-id="5ffa1-118">更新 CLFS 儲存目標型別。</span><span class="sxs-lookup"><span data-stu-id="5ffa1-118">Update CLFS Storage Target type.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ClfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ffa1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ffa1-119">-DefaultProfile</span></span>
<span data-ttu-id="5ffa1-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5ffa1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ffa1-121">-強制</span><span class="sxs-lookup"><span data-stu-id="5ffa1-121">-Force</span></span>
<span data-ttu-id="5ffa1-122">表示 Cmdlet 不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5ffa1-122">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="5ffa1-123">根據預設，此 Cmdlet 會提示您確認要清除該緩存。</span><span class="sxs-lookup"><span data-stu-id="5ffa1-123">By default, this cmdlet prompts you to confirm that you want to flush the cache.</span></span>

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

### <span data-ttu-id="5ffa1-124">-HostName</span><span class="sxs-lookup"><span data-stu-id="5ffa1-124">-HostName</span></span>
<span data-ttu-id="5ffa1-125">NFS 主機名稱。</span><span class="sxs-lookup"><span data-stu-id="5ffa1-125">NFS host name.</span></span>

```yaml
Type: System.String
Parameter Sets: NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ffa1-126">-聯接</span><span class="sxs-lookup"><span data-stu-id="5ffa1-126">-Junction</span></span>
<span data-ttu-id="5ffa1-127">結。</span><span class="sxs-lookup"><span data-stu-id="5ffa1-127">Junction.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ffa1-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="5ffa1-128">-Name</span></span>
<span data-ttu-id="5ffa1-129">儲存目標的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ffa1-129">Name of storage target.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageTargetName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ffa1-130">-NFS</span><span class="sxs-lookup"><span data-stu-id="5ffa1-130">-NFS</span></span>
<span data-ttu-id="5ffa1-131">更新 NFS 儲存目標型別。</span><span class="sxs-lookup"><span data-stu-id="5ffa1-131">Update NFS Storage Target type.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ffa1-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ffa1-132">-ResourceGroupName</span></span>
<span data-ttu-id="5ffa1-133">「您想要為指定緩存建立儲存目標的資源組名。</span><span class="sxs-lookup"><span data-stu-id="5ffa1-133">"Name of resource group under which you want to create storage target for given cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ffa1-134">-StorageContainerID</span><span class="sxs-lookup"><span data-stu-id="5ffa1-134">-StorageContainerID</span></span>
<span data-ttu-id="5ffa1-135">StorageContainerID</span><span class="sxs-lookup"><span data-stu-id="5ffa1-135">StorageContainerID</span></span>

```yaml
Type: System.String
Parameter Sets: ClfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ffa1-136">-UsageModel</span><span class="sxs-lookup"><span data-stu-id="5ffa1-136">-UsageModel</span></span>
<span data-ttu-id="5ffa1-137">NFS 使用方式模型。</span><span class="sxs-lookup"><span data-stu-id="5ffa1-137">NFS usage model.</span></span>

```yaml
Type: System.String
Parameter Sets: NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ffa1-138">-確認</span><span class="sxs-lookup"><span data-stu-id="5ffa1-138">-Confirm</span></span>
<span data-ttu-id="5ffa1-139">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5ffa1-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ffa1-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ffa1-140">-WhatIf</span></span>
<span data-ttu-id="5ffa1-141">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5ffa1-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5ffa1-142">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5ffa1-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ffa1-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ffa1-143">CommonParameters</span></span>
<span data-ttu-id="5ffa1-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5ffa1-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ffa1-145">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5ffa1-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ffa1-146">輸入</span><span class="sxs-lookup"><span data-stu-id="5ffa1-146">INPUTS</span></span>

### <span data-ttu-id="5ffa1-147">System.String</span><span class="sxs-lookup"><span data-stu-id="5ffa1-147">System.String</span></span>

## <span data-ttu-id="5ffa1-148">輸出</span><span class="sxs-lookup"><span data-stu-id="5ffa1-148">OUTPUTS</span></span>

### <span data-ttu-id="5ffa1-149">Microsoft.Azure.PowerShell.Cmdlets.HPCache.models.PsHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="5ffa1-149">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span></span>

## <span data-ttu-id="5ffa1-150">筆記</span><span class="sxs-lookup"><span data-stu-id="5ffa1-150">NOTES</span></span>

## <span data-ttu-id="5ffa1-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="5ffa1-151">RELATED LINKS</span></span>
