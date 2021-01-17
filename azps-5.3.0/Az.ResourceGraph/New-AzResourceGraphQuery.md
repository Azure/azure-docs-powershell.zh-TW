---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/new-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/New-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/New-AzResourceGraphQuery.md
ms.openlocfilehash: 853c06c6179f25065efba71b2d148c36e2d74ef4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98436206"
---
# <span data-ttu-id="58381-101">New-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="58381-101">New-AzResourceGraphQuery</span></span>

## <span data-ttu-id="58381-102">摘要</span><span class="sxs-lookup"><span data-stu-id="58381-102">SYNOPSIS</span></span>
<span data-ttu-id="58381-103">建立新的圖表查詢。</span><span class="sxs-lookup"><span data-stu-id="58381-103">Create a new graph query.</span></span>

## <span data-ttu-id="58381-104">句法</span><span class="sxs-lookup"><span data-stu-id="58381-104">SYNTAX</span></span>

```
New-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-File <String>] [-Location <String>] [-Query <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="58381-105">說明</span><span class="sxs-lookup"><span data-stu-id="58381-105">DESCRIPTION</span></span>
<span data-ttu-id="58381-106">建立新的圖表查詢。</span><span class="sxs-lookup"><span data-stu-id="58381-106">Create a new graph query.</span></span>

## <span data-ttu-id="58381-107">示例</span><span class="sxs-lookup"><span data-stu-id="58381-107">EXAMPLES</span></span>

### <span data-ttu-id="58381-108">範例1：由 query 參數建立資源圖表查詢</span><span class="sxs-lookup"><span data-stu-id="58381-108">Example 1: Create a resource graph query by the query parameter</span></span>
```powershell
PS C:\> New-AzResourceGraphQuery -Name query-t03 -ResourceGroupName azure-rg-test -Location "global" -Description "requesting a subset of resource fields." -Query "project id, name, type, location, tags" 


Location Name      Type
-------- ----      ----
     global   query-t03 microsoft.resourcegraph/queries
```

<span data-ttu-id="58381-109">這個命令會依據查詢參數建立資源圖表查詢。</span><span class="sxs-lookup"><span data-stu-id="58381-109">This command creates a resource graph query by the query parameter.</span></span>

### <span data-ttu-id="58381-110">範例2：由 file 參數建立資源圖表查詢</span><span class="sxs-lookup"><span data-stu-id="58381-110">Example 2: Create a resource graph query by the file parameter</span></span>
```powershell
PS C:\> New-AzResourceGraphQuery -Name query-t04 -ResourceGroupName azure-rg-test -Location "global" -Description "requesting a subset of resource fields." -File 'D:\azure-service\ResourceGraph.Autorest\azure-powershell\src\ResourceGraph\ResourceGraph.Autorest\test\Query.kql'

Location Name      Type
-------- ----      ----
     global   query-t04 microsoft.resourcegraph/queries
```

<span data-ttu-id="58381-111">這個命令會透過 file 參數建立資源圖表查詢。</span><span class="sxs-lookup"><span data-stu-id="58381-111">This command creates a resource graph query by the file parameter.</span></span>

## <span data-ttu-id="58381-112">參數</span><span class="sxs-lookup"><span data-stu-id="58381-112">PARAMETERS</span></span>

### <span data-ttu-id="58381-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58381-113">-DefaultProfile</span></span>
<span data-ttu-id="58381-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="58381-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58381-115">-描述</span><span class="sxs-lookup"><span data-stu-id="58381-115">-Description</span></span>
<span data-ttu-id="58381-116">圖表查詢的描述。</span><span class="sxs-lookup"><span data-stu-id="58381-116">The description of a graph query.</span></span>

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

### <span data-ttu-id="58381-117">檔案</span><span class="sxs-lookup"><span data-stu-id="58381-117">-File</span></span>
<span data-ttu-id="58381-118">檔案的內容會傳遞到查詢參數。</span><span class="sxs-lookup"><span data-stu-id="58381-118">The content of the file will be passed to the query parameter.</span></span>

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

### <span data-ttu-id="58381-119">-位置</span><span class="sxs-lookup"><span data-stu-id="58381-119">-Location</span></span>
<span data-ttu-id="58381-120">資源的位置</span><span class="sxs-lookup"><span data-stu-id="58381-120">The location of the resource</span></span>

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

### <span data-ttu-id="58381-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="58381-121">-Name</span></span>
<span data-ttu-id="58381-122">圖形查詢資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="58381-122">The name of the Graph Query resource.</span></span>

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

### <span data-ttu-id="58381-123">-Query</span><span class="sxs-lookup"><span data-stu-id="58381-123">-Query</span></span>
<span data-ttu-id="58381-124">將會成為圖形的 KQL 查詢。</span><span class="sxs-lookup"><span data-stu-id="58381-124">KQL query that will be graph.</span></span>

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

### <span data-ttu-id="58381-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58381-125">-ResourceGroupName</span></span>
<span data-ttu-id="58381-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="58381-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="58381-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="58381-127">-SubscriptionId</span></span>
<span data-ttu-id="58381-128">Azure 訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="58381-128">The Azure subscription Id.</span></span>

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

### <span data-ttu-id="58381-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="58381-129">-Tag</span></span>
<span data-ttu-id="58381-130">資源標記</span><span class="sxs-lookup"><span data-stu-id="58381-130">Resource tags</span></span>

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

### <span data-ttu-id="58381-131">-確認</span><span class="sxs-lookup"><span data-stu-id="58381-131">-Confirm</span></span>
<span data-ttu-id="58381-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="58381-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58381-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58381-133">-WhatIf</span></span>
<span data-ttu-id="58381-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="58381-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58381-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="58381-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58381-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58381-136">CommonParameters</span></span>
<span data-ttu-id="58381-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="58381-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58381-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="58381-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58381-139">輸入</span><span class="sxs-lookup"><span data-stu-id="58381-139">INPUTS</span></span>

### <span data-ttu-id="58381-140">IGraphQueryResource （ResourceGraph）。 Api20180901Preview。</span><span class="sxs-lookup"><span data-stu-id="58381-140">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

### <span data-ttu-id="58381-141">IResourceGraphIdentity （ResourceGraph）的</span><span class="sxs-lookup"><span data-stu-id="58381-141">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="58381-142">輸出</span><span class="sxs-lookup"><span data-stu-id="58381-142">OUTPUTS</span></span>

### <span data-ttu-id="58381-143">IGraphQueryResource （ResourceGraph）。 Api20180901Preview。</span><span class="sxs-lookup"><span data-stu-id="58381-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

## <span data-ttu-id="58381-144">筆記</span><span class="sxs-lookup"><span data-stu-id="58381-144">NOTES</span></span>

<span data-ttu-id="58381-145">別名</span><span class="sxs-lookup"><span data-stu-id="58381-145">ALIASES</span></span>

## <span data-ttu-id="58381-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="58381-146">RELATED LINKS</span></span>

