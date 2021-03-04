---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/powershell/module/az.resourcegraph/new-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/New-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/New-AzResourceGraphQuery.md
ms.openlocfilehash: c20e7c63fac01459d3df9d417b0fcec6aed83d36
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914489"
---
# <span data-ttu-id="92971-101">New-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="92971-101">New-AzResourceGraphQuery</span></span>

## <span data-ttu-id="92971-102">簡介</span><span class="sxs-lookup"><span data-stu-id="92971-102">SYNOPSIS</span></span>
<span data-ttu-id="92971-103">建立新圖形查詢。</span><span class="sxs-lookup"><span data-stu-id="92971-103">Create a new graph query.</span></span>

## <span data-ttu-id="92971-104">語法</span><span class="sxs-lookup"><span data-stu-id="92971-104">SYNTAX</span></span>

```
New-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-File <String>] [-Location <String>] [-Query <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="92971-105">描述</span><span class="sxs-lookup"><span data-stu-id="92971-105">DESCRIPTION</span></span>
<span data-ttu-id="92971-106">建立新圖形查詢。</span><span class="sxs-lookup"><span data-stu-id="92971-106">Create a new graph query.</span></span>

## <span data-ttu-id="92971-107">例子</span><span class="sxs-lookup"><span data-stu-id="92971-107">EXAMPLES</span></span>

### <span data-ttu-id="92971-108">範例 1：根據查詢參數建立資源圖形查詢</span><span class="sxs-lookup"><span data-stu-id="92971-108">Example 1: Create a resource graph query by the query parameter</span></span>
```powershell
PS C:\> New-AzResourceGraphQuery -Name query-t03 -ResourceGroupName azure-rg-test -Location "global" -Description "requesting a subset of resource fields." -Query "project id, name, type, location, tags" 


Location Name      Type
-------- ----      ----
     global   query-t03 microsoft.resourcegraph/queries
```

<span data-ttu-id="92971-109">此命令會以查詢參數建立資源圖形查詢。</span><span class="sxs-lookup"><span data-stu-id="92971-109">This command creates a resource graph query by the query parameter.</span></span>

### <span data-ttu-id="92971-110">範例 2：根據檔案參數建立資源圖形查詢</span><span class="sxs-lookup"><span data-stu-id="92971-110">Example 2: Create a resource graph query by the file parameter</span></span>
```powershell
PS C:\> New-AzResourceGraphQuery -Name query-t04 -ResourceGroupName azure-rg-test -Location "global" -Description "requesting a subset of resource fields." -File 'D:\azure-service\ResourceGraph.Autorest\azure-powershell\src\ResourceGraph\ResourceGraph.Autorest\test\Query.kql'

Location Name      Type
-------- ----      ----
     global   query-t04 microsoft.resourcegraph/queries
```

<span data-ttu-id="92971-111">此命令會以檔案參數建立資源圖形查詢。</span><span class="sxs-lookup"><span data-stu-id="92971-111">This command creates a resource graph query by the file parameter.</span></span>

## <span data-ttu-id="92971-112">參數</span><span class="sxs-lookup"><span data-stu-id="92971-112">PARAMETERS</span></span>

### <span data-ttu-id="92971-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92971-113">-DefaultProfile</span></span>
<span data-ttu-id="92971-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="92971-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92971-115">-描述</span><span class="sxs-lookup"><span data-stu-id="92971-115">-Description</span></span>
<span data-ttu-id="92971-116">圖形查詢的描述。</span><span class="sxs-lookup"><span data-stu-id="92971-116">The description of a graph query.</span></span>

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

### <span data-ttu-id="92971-117">-檔案</span><span class="sxs-lookup"><span data-stu-id="92971-117">-File</span></span>
<span data-ttu-id="92971-118">檔案的內容會傳遞至查詢參數。</span><span class="sxs-lookup"><span data-stu-id="92971-118">The content of the file will be passed to the query parameter.</span></span>

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

### <span data-ttu-id="92971-119">-位置</span><span class="sxs-lookup"><span data-stu-id="92971-119">-Location</span></span>
<span data-ttu-id="92971-120">資源的位置</span><span class="sxs-lookup"><span data-stu-id="92971-120">The location of the resource</span></span>

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

### <span data-ttu-id="92971-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="92971-121">-Name</span></span>
<span data-ttu-id="92971-122">Graph 查詢資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="92971-122">The name of the Graph Query resource.</span></span>

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

### <span data-ttu-id="92971-123">-查詢</span><span class="sxs-lookup"><span data-stu-id="92971-123">-Query</span></span>
<span data-ttu-id="92971-124">將會是圖形的 KQL 查詢。</span><span class="sxs-lookup"><span data-stu-id="92971-124">KQL query that will be graph.</span></span>

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

### <span data-ttu-id="92971-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92971-125">-ResourceGroupName</span></span>
<span data-ttu-id="92971-126">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="92971-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="92971-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="92971-127">-SubscriptionId</span></span>
<span data-ttu-id="92971-128">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="92971-128">The Azure subscription Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92971-129">-標記</span><span class="sxs-lookup"><span data-stu-id="92971-129">-Tag</span></span>
<span data-ttu-id="92971-130">資源標記</span><span class="sxs-lookup"><span data-stu-id="92971-130">Resource tags</span></span>

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

### <span data-ttu-id="92971-131">-確認</span><span class="sxs-lookup"><span data-stu-id="92971-131">-Confirm</span></span>
<span data-ttu-id="92971-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="92971-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92971-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92971-133">-WhatIf</span></span>
<span data-ttu-id="92971-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="92971-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92971-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="92971-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92971-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92971-136">CommonParameters</span></span>
<span data-ttu-id="92971-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="92971-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92971-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="92971-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92971-139">輸入</span><span class="sxs-lookup"><span data-stu-id="92971-139">INPUTS</span></span>

### <span data-ttu-id="92971-140">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.models.Api20180901Preview.IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="92971-140">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

### <span data-ttu-id="92971-141">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.models.IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="92971-141">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="92971-142">輸出</span><span class="sxs-lookup"><span data-stu-id="92971-142">OUTPUTS</span></span>

### <span data-ttu-id="92971-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.models.Api20180901Preview.IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="92971-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

## <span data-ttu-id="92971-144">筆記</span><span class="sxs-lookup"><span data-stu-id="92971-144">NOTES</span></span>

<span data-ttu-id="92971-145">別名</span><span class="sxs-lookup"><span data-stu-id="92971-145">ALIASES</span></span>

## <span data-ttu-id="92971-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="92971-146">RELATED LINKS</span></span>

