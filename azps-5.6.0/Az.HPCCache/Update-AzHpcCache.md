---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/update-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Update-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Update-AzHpcCache.md
ms.openlocfilehash: a4676884c791a6716672a411d374630e617a872c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917273"
---
# <span data-ttu-id="bd905-101">Update-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="bd905-101">Update-AzHpcCache</span></span>

## <span data-ttu-id="bd905-102">簡介</span><span class="sxs-lookup"><span data-stu-id="bd905-102">SYNOPSIS</span></span>
<span data-ttu-id="bd905-103">更新 HPC Cache。</span><span class="sxs-lookup"><span data-stu-id="bd905-103">Updates a HPC Cache.</span></span>

## <span data-ttu-id="bd905-104">語法</span><span class="sxs-lookup"><span data-stu-id="bd905-104">SYNTAX</span></span>

### <span data-ttu-id="bd905-105">FlushParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="bd905-105">FlushParameterSet (Default)</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> [-Flush] [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd905-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd905-106">ByResourceIdParameterSet</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd905-107">UpgradeParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd905-107">UpgradeParameterSet</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> [-Upgrade] [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd905-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd905-108">ByObjectParameterSet</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> -InputObject <PSHPCCache> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd905-109">描述</span><span class="sxs-lookup"><span data-stu-id="bd905-109">DESCRIPTION</span></span>
<span data-ttu-id="bd905-110">**Update-AzHpcCache** Cmdlet 會更新 Azure HPC Cache。</span><span class="sxs-lookup"><span data-stu-id="bd905-110">The **Update-AzHpcCache** cmdlet updates a Azure HPC Cache.</span></span>

## <span data-ttu-id="bd905-111">例子</span><span class="sxs-lookup"><span data-stu-id="bd905-111">EXAMPLES</span></span>

### <span data-ttu-id="bd905-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="bd905-112">Example 1</span></span>
```powershell
PS C:\> Update-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="bd905-113">參數</span><span class="sxs-lookup"><span data-stu-id="bd905-113">PARAMETERS</span></span>

### <span data-ttu-id="bd905-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bd905-114">-AsJob</span></span>
<span data-ttu-id="bd905-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="bd905-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bd905-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd905-116">-DefaultProfile</span></span>
<span data-ttu-id="bd905-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="bd905-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd905-118">-Flush</span><span class="sxs-lookup"><span data-stu-id="bd905-118">-Flush</span></span>
<span data-ttu-id="bd905-119">清除 HPC Cache。</span><span class="sxs-lookup"><span data-stu-id="bd905-119">Flushes HPC Cache.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FlushParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd905-120">-強制</span><span class="sxs-lookup"><span data-stu-id="bd905-120">-Force</span></span>
<span data-ttu-id="bd905-121">表示 Cmdlet 不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="bd905-121">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="bd905-122">根據預設，此 Cmdlet 會提示您確認要更新快點。</span><span class="sxs-lookup"><span data-stu-id="bd905-122">By default, this cmdlet prompts you to confirm that you want to update the cache.</span></span>

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

### <span data-ttu-id="bd905-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd905-123">-InputObject</span></span>
<span data-ttu-id="bd905-124">要更新的快用物件。</span><span class="sxs-lookup"><span data-stu-id="bd905-124">The cache object to update.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd905-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="bd905-125">-Name</span></span>
<span data-ttu-id="bd905-126">緩存名稱。</span><span class="sxs-lookup"><span data-stu-id="bd905-126">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CacheName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd905-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bd905-127">-PassThru</span></span>
<span data-ttu-id="bd905-128">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="bd905-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="bd905-129">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="bd905-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bd905-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd905-130">-ResourceGroupName</span></span>
<span data-ttu-id="bd905-131">這是要更新快點的資源組名。</span><span class="sxs-lookup"><span data-stu-id="bd905-131">Name of resource group under which you want to update cache.</span></span>

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

### <span data-ttu-id="bd905-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd905-132">-ResourceId</span></span>
<span data-ttu-id="bd905-133">Cache 的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="bd905-133">The resource id of the Cache</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd905-134">-升級</span><span class="sxs-lookup"><span data-stu-id="bd905-134">-Upgrade</span></span>
<span data-ttu-id="bd905-135">升級 HpcCache。</span><span class="sxs-lookup"><span data-stu-id="bd905-135">Upgrade HpcCache.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpgradeParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd905-136">-確認</span><span class="sxs-lookup"><span data-stu-id="bd905-136">-Confirm</span></span>
<span data-ttu-id="bd905-137">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="bd905-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd905-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd905-138">-WhatIf</span></span>
<span data-ttu-id="bd905-139">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bd905-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bd905-140">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bd905-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd905-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd905-141">CommonParameters</span></span>
<span data-ttu-id="bd905-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="bd905-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd905-143">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd905-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd905-144">輸入</span><span class="sxs-lookup"><span data-stu-id="bd905-144">INPUTS</span></span>

### <span data-ttu-id="bd905-145">System.String</span><span class="sxs-lookup"><span data-stu-id="bd905-145">System.String</span></span>

## <span data-ttu-id="bd905-146">輸出</span><span class="sxs-lookup"><span data-stu-id="bd905-146">OUTPUTS</span></span>

## <span data-ttu-id="bd905-147">筆記</span><span class="sxs-lookup"><span data-stu-id="bd905-147">NOTES</span></span>

## <span data-ttu-id="bd905-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="bd905-148">RELATED LINKS</span></span>
