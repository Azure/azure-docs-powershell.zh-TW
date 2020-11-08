---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/set-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCacheStorageTarget.md
ms.openlocfilehash: fa799a05b76f9f6941b19bf171beb77318b77d39
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138838"
---
# <span data-ttu-id="fe8f3-101">Set-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="fe8f3-101">Set-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="fe8f3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fe8f3-102">SYNOPSIS</span></span>
<span data-ttu-id="fe8f3-103">更新存儲目標。</span><span class="sxs-lookup"><span data-stu-id="fe8f3-103">Updates a Storage Target.</span></span>

## <span data-ttu-id="fe8f3-104">句法</span><span class="sxs-lookup"><span data-stu-id="fe8f3-104">SYNTAX</span></span>

### <span data-ttu-id="fe8f3-105">ClfsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="fe8f3-105">ClfsParameterSet (Default)</span></span>
```
Set-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-CLFS]
 [-Junction <Hashtable[]>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fe8f3-106">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe8f3-106">NfsParameterSet</span></span>
```
Set-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-NFS]
 [-Junction <Hashtable[]>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fe8f3-107">說明</span><span class="sxs-lookup"><span data-stu-id="fe8f3-107">DESCRIPTION</span></span>
<span data-ttu-id="fe8f3-108">**AzHpcCacheStorageTarget** Cmdlet 會更新附加至 Azure HPC 緩存的儲存目標。</span><span class="sxs-lookup"><span data-stu-id="fe8f3-108">The **Set-AzHpcCacheStorageTarget** cmdlet updates a Storage Target attached to Azure HPC cache.</span></span>

## <span data-ttu-id="fe8f3-109">示例</span><span class="sxs-lookup"><span data-stu-id="fe8f3-109">EXAMPLES</span></span>

### <span data-ttu-id="fe8f3-110">範例1</span><span class="sxs-lookup"><span data-stu-id="fe8f3-110">Example 1</span></span>
```powershell
PS C:\> Set-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -CLFS -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

### <span data-ttu-id="fe8f3-111">範例2</span><span class="sxs-lookup"><span data-stu-id="fe8f3-111">Example 2</span></span>
```powershell
PS C:\> Set-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -NFS -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/export"})
```

## <span data-ttu-id="fe8f3-112">參數</span><span class="sxs-lookup"><span data-stu-id="fe8f3-112">PARAMETERS</span></span>

### <span data-ttu-id="fe8f3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fe8f3-113">-AsJob</span></span>
<span data-ttu-id="fe8f3-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="fe8f3-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fe8f3-115">-CacheName</span><span class="sxs-lookup"><span data-stu-id="fe8f3-115">-CacheName</span></span>
<span data-ttu-id="fe8f3-116">快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="fe8f3-116">Name of cache.</span></span>

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

### <span data-ttu-id="fe8f3-117">-CLFS</span><span class="sxs-lookup"><span data-stu-id="fe8f3-117">-CLFS</span></span>
<span data-ttu-id="fe8f3-118">更新 CLFS 儲存目標型別。</span><span class="sxs-lookup"><span data-stu-id="fe8f3-118">Update CLFS Storage Target type.</span></span>

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

### <span data-ttu-id="fe8f3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe8f3-119">-DefaultProfile</span></span>
<span data-ttu-id="fe8f3-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fe8f3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe8f3-121">-Force</span><span class="sxs-lookup"><span data-stu-id="fe8f3-121">-Force</span></span>
<span data-ttu-id="fe8f3-122">表示 Cmdlet 不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fe8f3-122">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="fe8f3-123">根據預設，這個 Cmdlet 會提示您確認您要清除快取。</span><span class="sxs-lookup"><span data-stu-id="fe8f3-123">By default, this cmdlet prompts you to confirm that you want to flush the cache.</span></span>

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

### <span data-ttu-id="fe8f3-124">-聯結</span><span class="sxs-lookup"><span data-stu-id="fe8f3-124">-Junction</span></span>
<span data-ttu-id="fe8f3-125">聯接.</span><span class="sxs-lookup"><span data-stu-id="fe8f3-125">Junction.</span></span>

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

### <span data-ttu-id="fe8f3-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="fe8f3-126">-Name</span></span>
<span data-ttu-id="fe8f3-127">儲存目標的名稱。</span><span class="sxs-lookup"><span data-stu-id="fe8f3-127">Name of storage target.</span></span>

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

### <span data-ttu-id="fe8f3-128">-NFS</span><span class="sxs-lookup"><span data-stu-id="fe8f3-128">-NFS</span></span>
<span data-ttu-id="fe8f3-129">更新 NFS 儲存目標型別。</span><span class="sxs-lookup"><span data-stu-id="fe8f3-129">Update NFS Storage Target type.</span></span>

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

### <span data-ttu-id="fe8f3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe8f3-130">-ResourceGroupName</span></span>
<span data-ttu-id="fe8f3-131">您要在其中更新儲存空間目標的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fe8f3-131">Name of resource group under which you want to update storage target.</span></span>

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

### <span data-ttu-id="fe8f3-132">-確認</span><span class="sxs-lookup"><span data-stu-id="fe8f3-132">-Confirm</span></span>
<span data-ttu-id="fe8f3-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fe8f3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe8f3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe8f3-134">-WhatIf</span></span>
<span data-ttu-id="fe8f3-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fe8f3-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fe8f3-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fe8f3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe8f3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe8f3-137">CommonParameters</span></span>
<span data-ttu-id="fe8f3-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fe8f3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe8f3-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="fe8f3-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe8f3-140">輸入</span><span class="sxs-lookup"><span data-stu-id="fe8f3-140">INPUTS</span></span>

### <span data-ttu-id="fe8f3-141">System.object</span><span class="sxs-lookup"><span data-stu-id="fe8f3-141">System.String</span></span>

## <span data-ttu-id="fe8f3-142">輸出</span><span class="sxs-lookup"><span data-stu-id="fe8f3-142">OUTPUTS</span></span>

### <span data-ttu-id="fe8f3-143">PsHpcStorageTarget （HPCCache）的</span><span class="sxs-lookup"><span data-stu-id="fe8f3-143">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span></span>

## <span data-ttu-id="fe8f3-144">筆記</span><span class="sxs-lookup"><span data-stu-id="fe8f3-144">NOTES</span></span>

## <span data-ttu-id="fe8f3-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="fe8f3-145">RELATED LINKS</span></span>