---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/new-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCacheStorageTarget.md
ms.openlocfilehash: eee07c01b0c9e0e2b072787d0d37a6a868fbf150
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139256"
---
# <span data-ttu-id="377e6-101">New-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="377e6-101">New-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="377e6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="377e6-102">SYNOPSIS</span></span>
<span data-ttu-id="377e6-103">建立一個儲存目標。</span><span class="sxs-lookup"><span data-stu-id="377e6-103">Creates a Storage Target.</span></span>

## <span data-ttu-id="377e6-104">句法</span><span class="sxs-lookup"><span data-stu-id="377e6-104">SYNTAX</span></span>

### <span data-ttu-id="377e6-105">ClfsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="377e6-105">ClfsParameterSet (Default)</span></span>
```
New-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-CLFS]
 [-StorageContainerID <String>] [-Junction <Hashtable[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="377e6-106">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="377e6-106">NfsParameterSet</span></span>
```
New-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-NFS]
 [-HostName <String>] [-UsageModel <String>] [-Junction <Hashtable[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="377e6-107">說明</span><span class="sxs-lookup"><span data-stu-id="377e6-107">DESCRIPTION</span></span>
<span data-ttu-id="377e6-108">**新的-AzHpcCacheStorageTarget** Cmdlet 會將一個儲存目標新增至 Azure HPC 快取。</span><span class="sxs-lookup"><span data-stu-id="377e6-108">The **New-AzHpcCacheStorageTarget** cmdlet adds a Storage Target to Azure HPC Cache.</span></span>

## <span data-ttu-id="377e6-109">示例</span><span class="sxs-lookup"><span data-stu-id="377e6-109">EXAMPLES</span></span>

### <span data-ttu-id="377e6-110">範例1</span><span class="sxs-lookup"><span data-stu-id="377e6-110">Example 1</span></span>
```powershell
PS C:\> New-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -CLFS -StorageContainerID "/subscriptions/testsub/resourceGroups/testRG/providers/Microsoft.Storage/storageAccounts/testdstorageaccount/blobServices/default/containers/testcontainer" -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

### <span data-ttu-id="377e6-111">範例2</span><span class="sxs-lookup"><span data-stu-id="377e6-111">Example 2</span></span>
```powershell
PS C:\> New-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -NFS -UsageModel "READ_HEAVY_INFREQ" -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

## <span data-ttu-id="377e6-112">參數</span><span class="sxs-lookup"><span data-stu-id="377e6-112">PARAMETERS</span></span>

### <span data-ttu-id="377e6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="377e6-113">-AsJob</span></span>
<span data-ttu-id="377e6-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="377e6-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="377e6-115">-CacheName</span><span class="sxs-lookup"><span data-stu-id="377e6-115">-CacheName</span></span>
<span data-ttu-id="377e6-116">快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="377e6-116">Name of cache.</span></span>

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

### <span data-ttu-id="377e6-117">-CLFS</span><span class="sxs-lookup"><span data-stu-id="377e6-117">-CLFS</span></span>
<span data-ttu-id="377e6-118">更新 CLFS 儲存目標型別。</span><span class="sxs-lookup"><span data-stu-id="377e6-118">Update CLFS Storage Target type.</span></span>

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

### <span data-ttu-id="377e6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="377e6-119">-DefaultProfile</span></span>
<span data-ttu-id="377e6-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="377e6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="377e6-121">-Force</span><span class="sxs-lookup"><span data-stu-id="377e6-121">-Force</span></span>
<span data-ttu-id="377e6-122">表示 Cmdlet 不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="377e6-122">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="377e6-123">根據預設，這個 Cmdlet 會提示您確認您要清除快取。</span><span class="sxs-lookup"><span data-stu-id="377e6-123">By default, this cmdlet prompts you to confirm that you want to flush the cache.</span></span>

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

### <span data-ttu-id="377e6-124">-HostName</span><span class="sxs-lookup"><span data-stu-id="377e6-124">-HostName</span></span>
<span data-ttu-id="377e6-125">NFS 主機名稱。</span><span class="sxs-lookup"><span data-stu-id="377e6-125">NFS host name.</span></span>

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

### <span data-ttu-id="377e6-126">-聯結</span><span class="sxs-lookup"><span data-stu-id="377e6-126">-Junction</span></span>
<span data-ttu-id="377e6-127">聯接.</span><span class="sxs-lookup"><span data-stu-id="377e6-127">Junction.</span></span>

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

### <span data-ttu-id="377e6-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="377e6-128">-Name</span></span>
<span data-ttu-id="377e6-129">儲存目標的名稱。</span><span class="sxs-lookup"><span data-stu-id="377e6-129">Name of storage target.</span></span>

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

### <span data-ttu-id="377e6-130">-NFS</span><span class="sxs-lookup"><span data-stu-id="377e6-130">-NFS</span></span>
<span data-ttu-id="377e6-131">更新 NFS 儲存目標型別。</span><span class="sxs-lookup"><span data-stu-id="377e6-131">Update NFS Storage Target type.</span></span>

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

### <span data-ttu-id="377e6-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="377e6-132">-ResourceGroupName</span></span>
<span data-ttu-id="377e6-133">您想要在哪個資源群組中為指定的快取建立儲存目標的名稱。</span><span class="sxs-lookup"><span data-stu-id="377e6-133">"Name of resource group under which you want to create storage target for given cache.</span></span>

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

### <span data-ttu-id="377e6-134">-StorageContainerID</span><span class="sxs-lookup"><span data-stu-id="377e6-134">-StorageContainerID</span></span>
<span data-ttu-id="377e6-135">StorageContainerID</span><span class="sxs-lookup"><span data-stu-id="377e6-135">StorageContainerID</span></span>

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

### <span data-ttu-id="377e6-136">-UsageModel</span><span class="sxs-lookup"><span data-stu-id="377e6-136">-UsageModel</span></span>
<span data-ttu-id="377e6-137">NFS 使用量模型。</span><span class="sxs-lookup"><span data-stu-id="377e6-137">NFS usage model.</span></span>

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

### <span data-ttu-id="377e6-138">-確認</span><span class="sxs-lookup"><span data-stu-id="377e6-138">-Confirm</span></span>
<span data-ttu-id="377e6-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="377e6-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="377e6-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="377e6-140">-WhatIf</span></span>
<span data-ttu-id="377e6-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="377e6-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="377e6-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="377e6-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="377e6-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="377e6-143">CommonParameters</span></span>
<span data-ttu-id="377e6-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="377e6-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="377e6-145">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="377e6-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="377e6-146">輸入</span><span class="sxs-lookup"><span data-stu-id="377e6-146">INPUTS</span></span>

### <span data-ttu-id="377e6-147">System.object</span><span class="sxs-lookup"><span data-stu-id="377e6-147">System.String</span></span>

## <span data-ttu-id="377e6-148">輸出</span><span class="sxs-lookup"><span data-stu-id="377e6-148">OUTPUTS</span></span>

### <span data-ttu-id="377e6-149">PsHpcStorageTarget （HPCCache）的</span><span class="sxs-lookup"><span data-stu-id="377e6-149">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span></span>

## <span data-ttu-id="377e6-150">筆記</span><span class="sxs-lookup"><span data-stu-id="377e6-150">NOTES</span></span>

## <span data-ttu-id="377e6-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="377e6-151">RELATED LINKS</span></span>
