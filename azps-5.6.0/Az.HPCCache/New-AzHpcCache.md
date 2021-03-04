---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/new-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCache.md
ms.openlocfilehash: e0df378cb50d7d308d5d6a9f0acf8a15466b8a11
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917306"
---
# <span data-ttu-id="f94cc-101">New-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="f94cc-101">New-AzHpcCache</span></span>

## <span data-ttu-id="f94cc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f94cc-102">SYNOPSIS</span></span>
<span data-ttu-id="f94cc-103">建立 HPC Cache。</span><span class="sxs-lookup"><span data-stu-id="f94cc-103">Creates a HPC Cache.</span></span>

## <span data-ttu-id="f94cc-104">語法</span><span class="sxs-lookup"><span data-stu-id="f94cc-104">SYNTAX</span></span>

```
New-AzHpcCache -ResourceGroupName <String> -Name <String> -Sku <String> -SubnetUri <String> -CacheSize <Int32>
 -Location <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f94cc-105">描述</span><span class="sxs-lookup"><span data-stu-id="f94cc-105">DESCRIPTION</span></span>
<span data-ttu-id="f94cc-106">**New-AzHpcCache** Cmdlet 會建立 Azure HPC Cache。</span><span class="sxs-lookup"><span data-stu-id="f94cc-106">The **New-AzHpcCache** cmdlet creates a Azure HPC Cache.</span></span>

## <span data-ttu-id="f94cc-107">例子</span><span class="sxs-lookup"><span data-stu-id="f94cc-107">EXAMPLES</span></span>

### <span data-ttu-id="f94cc-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="f94cc-108">Example 1</span></span>
```powershell
PS C:\> New-AzHpcCache -ResourceGroupName testRG -CacheName testCache -Sku Standard_2G -SubnetUri /subscriptions/<subid>/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/testvnet/subnets/defauly-tip1-test2 -cacheSize 3072 -Location eastus -Tag @{"tag1" = "value1"; "tag2" = "value2"}
```

## <span data-ttu-id="f94cc-109">參數</span><span class="sxs-lookup"><span data-stu-id="f94cc-109">PARAMETERS</span></span>

### <span data-ttu-id="f94cc-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f94cc-110">-AsJob</span></span>
<span data-ttu-id="f94cc-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f94cc-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f94cc-112">-CacheSize</span><span class="sxs-lookup"><span data-stu-id="f94cc-112">-CacheSize</span></span>
<span data-ttu-id="f94cc-113">CacheSize。</span><span class="sxs-lookup"><span data-stu-id="f94cc-113">CacheSize.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f94cc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f94cc-114">-DefaultProfile</span></span>
<span data-ttu-id="f94cc-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f94cc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f94cc-116">-位置</span><span class="sxs-lookup"><span data-stu-id="f94cc-116">-Location</span></span>
<span data-ttu-id="f94cc-117">位置。</span><span class="sxs-lookup"><span data-stu-id="f94cc-117">Location.</span></span>

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

### <span data-ttu-id="f94cc-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="f94cc-118">-Name</span></span>
<span data-ttu-id="f94cc-119">緩存名稱。</span><span class="sxs-lookup"><span data-stu-id="f94cc-119">Name of cache.</span></span>

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

### <span data-ttu-id="f94cc-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f94cc-120">-ResourceGroupName</span></span>
<span data-ttu-id="f94cc-121">要建立緩存的資源組名。</span><span class="sxs-lookup"><span data-stu-id="f94cc-121">Name of resource group under which you want to create cache.</span></span>

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

### <span data-ttu-id="f94cc-122">-SKU</span><span class="sxs-lookup"><span data-stu-id="f94cc-122">-Sku</span></span>
<span data-ttu-id="f94cc-123">Sku。</span><span class="sxs-lookup"><span data-stu-id="f94cc-123">Sku.</span></span>

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

### <span data-ttu-id="f94cc-124">-子網Uri</span><span class="sxs-lookup"><span data-stu-id="f94cc-124">-SubnetUri</span></span>
<span data-ttu-id="f94cc-125">子網URI。</span><span class="sxs-lookup"><span data-stu-id="f94cc-125">SubnetURI.</span></span>

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

### <span data-ttu-id="f94cc-126">-標記</span><span class="sxs-lookup"><span data-stu-id="f94cc-126">-Tag</span></span>
<span data-ttu-id="f94cc-127">要與 HPC Cache 關聯的標記。</span><span class="sxs-lookup"><span data-stu-id="f94cc-127">The tags to associate with HPC Cache.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f94cc-128">-確認</span><span class="sxs-lookup"><span data-stu-id="f94cc-128">-Confirm</span></span>
<span data-ttu-id="f94cc-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f94cc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f94cc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f94cc-130">-WhatIf</span></span>
<span data-ttu-id="f94cc-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f94cc-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f94cc-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f94cc-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f94cc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f94cc-133">CommonParameters</span></span>
<span data-ttu-id="f94cc-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f94cc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f94cc-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f94cc-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f94cc-136">輸入</span><span class="sxs-lookup"><span data-stu-id="f94cc-136">INPUTS</span></span>

### <span data-ttu-id="f94cc-137">System.String</span><span class="sxs-lookup"><span data-stu-id="f94cc-137">System.String</span></span>

### <span data-ttu-id="f94cc-138">System.Int32</span><span class="sxs-lookup"><span data-stu-id="f94cc-138">System.Int32</span></span>

## <span data-ttu-id="f94cc-139">輸出</span><span class="sxs-lookup"><span data-stu-id="f94cc-139">OUTPUTS</span></span>

### <span data-ttu-id="f94cc-140">Microsoft.Azure.PowerShell.Cmdlets.HPCache.models.PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="f94cc-140">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="f94cc-141">筆記</span><span class="sxs-lookup"><span data-stu-id="f94cc-141">NOTES</span></span>

## <span data-ttu-id="f94cc-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="f94cc-142">RELATED LINKS</span></span>
