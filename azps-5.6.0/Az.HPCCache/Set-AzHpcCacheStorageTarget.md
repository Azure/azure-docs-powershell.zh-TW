---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/set-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCacheStorageTarget.md
ms.openlocfilehash: d60997647ed4f6bb1317148daadcbe4c0e00a5c8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917294"
---
# <span data-ttu-id="b1dbc-101">Set-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="b1dbc-101">Set-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="b1dbc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b1dbc-102">SYNOPSIS</span></span>
<span data-ttu-id="b1dbc-103">更新儲存目標。</span><span class="sxs-lookup"><span data-stu-id="b1dbc-103">Updates a Storage Target.</span></span>

## <span data-ttu-id="b1dbc-104">語法</span><span class="sxs-lookup"><span data-stu-id="b1dbc-104">SYNTAX</span></span>

### <span data-ttu-id="b1dbc-105">ClfsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b1dbc-105">ClfsParameterSet (Default)</span></span>
```
Set-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-CLFS]
 [-Junction <Hashtable[]>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b1dbc-106">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1dbc-106">NfsParameterSet</span></span>
```
Set-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-NFS]
 [-Junction <Hashtable[]>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b1dbc-107">描述</span><span class="sxs-lookup"><span data-stu-id="b1dbc-107">DESCRIPTION</span></span>
<span data-ttu-id="b1dbc-108">**Set-AzHpcCacheStorageTarget** Cmdlet 會更新附加至 Azure HPC 緩存的儲存目標。</span><span class="sxs-lookup"><span data-stu-id="b1dbc-108">The **Set-AzHpcCacheStorageTarget** cmdlet updates a Storage Target attached to Azure HPC cache.</span></span>

## <span data-ttu-id="b1dbc-109">例子</span><span class="sxs-lookup"><span data-stu-id="b1dbc-109">EXAMPLES</span></span>

### <span data-ttu-id="b1dbc-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="b1dbc-110">Example 1</span></span>
```powershell
PS C:\> Set-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -CLFS -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

### <span data-ttu-id="b1dbc-111">範例 2</span><span class="sxs-lookup"><span data-stu-id="b1dbc-111">Example 2</span></span>
```powershell
PS C:\> Set-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -NFS -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/export"})
```

## <span data-ttu-id="b1dbc-112">參數</span><span class="sxs-lookup"><span data-stu-id="b1dbc-112">PARAMETERS</span></span>

### <span data-ttu-id="b1dbc-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b1dbc-113">-AsJob</span></span>
<span data-ttu-id="b1dbc-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b1dbc-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b1dbc-115">-CacheName</span><span class="sxs-lookup"><span data-stu-id="b1dbc-115">-CacheName</span></span>
<span data-ttu-id="b1dbc-116">緩存名稱。</span><span class="sxs-lookup"><span data-stu-id="b1dbc-116">Name of cache.</span></span>

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

### <span data-ttu-id="b1dbc-117">-CLFS</span><span class="sxs-lookup"><span data-stu-id="b1dbc-117">-CLFS</span></span>
<span data-ttu-id="b1dbc-118">更新 CLFS 儲存目標型別。</span><span class="sxs-lookup"><span data-stu-id="b1dbc-118">Update CLFS Storage Target type.</span></span>

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

### <span data-ttu-id="b1dbc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1dbc-119">-DefaultProfile</span></span>
<span data-ttu-id="b1dbc-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b1dbc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1dbc-121">-強制</span><span class="sxs-lookup"><span data-stu-id="b1dbc-121">-Force</span></span>
<span data-ttu-id="b1dbc-122">表示 Cmdlet 不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b1dbc-122">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="b1dbc-123">根據預設，此 Cmdlet 會提示您確認要清除該緩存。</span><span class="sxs-lookup"><span data-stu-id="b1dbc-123">By default, this cmdlet prompts you to confirm that you want to flush the cache.</span></span>

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

### <span data-ttu-id="b1dbc-124">-聯接</span><span class="sxs-lookup"><span data-stu-id="b1dbc-124">-Junction</span></span>
<span data-ttu-id="b1dbc-125">結。</span><span class="sxs-lookup"><span data-stu-id="b1dbc-125">Junction.</span></span>

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

### <span data-ttu-id="b1dbc-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="b1dbc-126">-Name</span></span>
<span data-ttu-id="b1dbc-127">儲存目標的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1dbc-127">Name of storage target.</span></span>

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

### <span data-ttu-id="b1dbc-128">-NFS</span><span class="sxs-lookup"><span data-stu-id="b1dbc-128">-NFS</span></span>
<span data-ttu-id="b1dbc-129">更新 NFS 儲存目標型別。</span><span class="sxs-lookup"><span data-stu-id="b1dbc-129">Update NFS Storage Target type.</span></span>

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

### <span data-ttu-id="b1dbc-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1dbc-130">-ResourceGroupName</span></span>
<span data-ttu-id="b1dbc-131">要更新儲存目標的資源組名。</span><span class="sxs-lookup"><span data-stu-id="b1dbc-131">Name of resource group under which you want to update storage target.</span></span>

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

### <span data-ttu-id="b1dbc-132">-確認</span><span class="sxs-lookup"><span data-stu-id="b1dbc-132">-Confirm</span></span>
<span data-ttu-id="b1dbc-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b1dbc-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1dbc-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1dbc-134">-WhatIf</span></span>
<span data-ttu-id="b1dbc-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b1dbc-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b1dbc-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b1dbc-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1dbc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1dbc-137">CommonParameters</span></span>
<span data-ttu-id="b1dbc-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b1dbc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1dbc-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b1dbc-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1dbc-140">輸入</span><span class="sxs-lookup"><span data-stu-id="b1dbc-140">INPUTS</span></span>

### <span data-ttu-id="b1dbc-141">System.String</span><span class="sxs-lookup"><span data-stu-id="b1dbc-141">System.String</span></span>

## <span data-ttu-id="b1dbc-142">輸出</span><span class="sxs-lookup"><span data-stu-id="b1dbc-142">OUTPUTS</span></span>

### <span data-ttu-id="b1dbc-143">Microsoft.Azure.PowerShell.Cmdlets.HPCache.models.PsHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="b1dbc-143">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span></span>

## <span data-ttu-id="b1dbc-144">筆記</span><span class="sxs-lookup"><span data-stu-id="b1dbc-144">NOTES</span></span>

## <span data-ttu-id="b1dbc-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="b1dbc-145">RELATED LINKS</span></span>
