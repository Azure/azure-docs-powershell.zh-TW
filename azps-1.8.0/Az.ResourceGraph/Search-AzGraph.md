---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.dll-Help.xml
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/search-azgraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
ms.openlocfilehash: 5a9a47ff6f4a329d3e48ec54df85ade3be5ae84d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620912"
---
# <span data-ttu-id="d69af-101">Search-AzGraph</span><span class="sxs-lookup"><span data-stu-id="d69af-101">Search-AzGraph</span></span>

## <span data-ttu-id="d69af-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d69af-102">SYNOPSIS</span></span>
<span data-ttu-id="d69af-103">查詢由 Azure 資源管理器管理的資源。</span><span class="sxs-lookup"><span data-stu-id="d69af-103">Queries the resources managed by Azure Resource Manager.</span></span>

## <span data-ttu-id="d69af-104">句法</span><span class="sxs-lookup"><span data-stu-id="d69af-104">SYNTAX</span></span>

```
Search-AzGraph [-Query] <String> [-Subscription <String[]>] [-First <Int32>] [-Skip <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d69af-105">說明</span><span class="sxs-lookup"><span data-stu-id="d69af-105">DESCRIPTION</span></span>
<span data-ttu-id="d69af-106">若要深入瞭解查詢語法，請參閱： https://aka.ms/resource-graph/learntoquery</span><span class="sxs-lookup"><span data-stu-id="d69af-106">Learn more about the query syntax here: https://aka.ms/resource-graph/learntoquery</span></span>

## <span data-ttu-id="d69af-107">示例</span><span class="sxs-lookup"><span data-stu-id="d69af-107">EXAMPLES</span></span>

### <span data-ttu-id="d69af-108">範例1</span><span class="sxs-lookup"><span data-stu-id="d69af-108">Example 1</span></span>
```powershell
PS C:\> Search-AzGraph "project id, name, type, location, tags" -First 3


id         : /subscriptions/1ef51df4-f8a9-4b69-9919-1ef51df4eff6/resourceGroups/Service-INT-a/providers/Microsoft.Compute/virtualMachineScaleSets/nt
name       : nt
type       : microsoft.compute/virtualmachinescalesets
location   : eastus
tags       : @{resourceType=Service Fabric; clusterName=gov-art-int-nt-a}

id         : /subscriptions/1ef51df4-f8a9-4b69-9919-1ef51df4eff6/resourceGroups/Service-INT-a/providers/Microsoft.EventGrid/topics/egtopic-1
name       : egtopic-1
type       : microsoft.eventgrid/topics
location   : westus2
tags       :
```

<span data-ttu-id="d69af-109">簡單的資源查詢，要求資源欄位的子集。</span><span class="sxs-lookup"><span data-stu-id="d69af-109">Simple resources query requesting a subset of resource fields.</span></span>

### <span data-ttu-id="d69af-110">範例2</span><span class="sxs-lookup"><span data-stu-id="d69af-110">Example 2</span></span>
```powershell
PS C:\> Search-AzGraph "project id, name, type, location | where type =~ 'Microsoft.Compute/virtualMachines' | summarize count() by location | top 3 by count_"

location      count_
--------      ------
eastus            66
westcentralus     32
westus            26
```

<span data-ttu-id="d69af-111">資源的複雜查詢，具有選取欄位、篩選及摘要。</span><span class="sxs-lookup"><span data-stu-id="d69af-111">A complex query on resources featuring field selection, filtering and summarizing.</span></span>

## <span data-ttu-id="d69af-112">參數</span><span class="sxs-lookup"><span data-stu-id="d69af-112">PARAMETERS</span></span>

### <span data-ttu-id="d69af-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d69af-113">-DefaultProfile</span></span>
<span data-ttu-id="d69af-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d69af-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d69af-115">-Query</span><span class="sxs-lookup"><span data-stu-id="d69af-115">-Query</span></span>
<span data-ttu-id="d69af-116">[資源圖表] 查詢。</span><span class="sxs-lookup"><span data-stu-id="d69af-116">Resource Graph query.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d69af-117">-訂閱</span><span class="sxs-lookup"><span data-stu-id="d69af-117">-Subscription</span></span>
<span data-ttu-id="d69af-118">[訂閱] (s) 來執行查詢。</span><span class="sxs-lookup"><span data-stu-id="d69af-118">Subscription(s) to run query against.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d69af-119">-略過</span><span class="sxs-lookup"><span data-stu-id="d69af-119">-Skip</span></span>
<span data-ttu-id="d69af-120">忽略前 N 個物件，然後取得剩餘的物件。</span><span class="sxs-lookup"><span data-stu-id="d69af-120">Ignores the first N objects and then gets the remaining objects.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d69af-121">-優先</span><span class="sxs-lookup"><span data-stu-id="d69af-121">-First</span></span>
<span data-ttu-id="d69af-122">要傳回的物件數目上限。</span><span class="sxs-lookup"><span data-stu-id="d69af-122">The maximum number of objects to return.</span></span> <span data-ttu-id="d69af-123">允許的值：1-5000。</span><span class="sxs-lookup"><span data-stu-id="d69af-123">Allowed values: 1-5000.</span></span>
<span data-ttu-id="d69af-124">預設值為100。</span><span class="sxs-lookup"><span data-stu-id="d69af-124">Default value is 100.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d69af-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d69af-125">CommonParameters</span></span>
<span data-ttu-id="d69af-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d69af-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d69af-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d69af-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d69af-128">輸入</span><span class="sxs-lookup"><span data-stu-id="d69af-128">INPUTS</span></span>

### <span data-ttu-id="d69af-129">所有</span><span class="sxs-lookup"><span data-stu-id="d69af-129">None</span></span>

## <span data-ttu-id="d69af-130">輸出</span><span class="sxs-lookup"><span data-stu-id="d69af-130">OUTPUTS</span></span>

### <span data-ttu-id="d69af-131">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="d69af-131">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="d69af-132">筆記</span><span class="sxs-lookup"><span data-stu-id="d69af-132">NOTES</span></span>

## <span data-ttu-id="d69af-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="d69af-133">RELATED LINKS</span></span>
