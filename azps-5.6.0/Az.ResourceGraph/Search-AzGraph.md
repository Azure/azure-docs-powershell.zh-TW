---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.dll-Help.xml
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/powershell/module/az.resourcegraph/search-azgraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
ms.openlocfilehash: e96d4fa13dc1b479c37b56cb3887b6d519df24f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914481"
---
# <span data-ttu-id="0d588-101">Search-AzGraph</span><span class="sxs-lookup"><span data-stu-id="0d588-101">Search-AzGraph</span></span>

## <span data-ttu-id="0d588-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0d588-102">SYNOPSIS</span></span>
<span data-ttu-id="0d588-103">查詢 Azure Resource Manager 所管理的資源。</span><span class="sxs-lookup"><span data-stu-id="0d588-103">Queries the resources managed by Azure Resource Manager.</span></span>

## <span data-ttu-id="0d588-104">語法</span><span class="sxs-lookup"><span data-stu-id="0d588-104">SYNTAX</span></span>

```
Search-AzGraph [-Query] <String> [-Subscription <String[]>] [-First <Int32>] [-Skip <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d588-105">描述</span><span class="sxs-lookup"><span data-stu-id="0d588-105">DESCRIPTION</span></span>
<span data-ttu-id="0d588-106">若要深入瞭解查詢語法，請在這裡： https://aka.ms/resource-graph/learntoquery</span><span class="sxs-lookup"><span data-stu-id="0d588-106">Learn more about the query syntax here: https://aka.ms/resource-graph/learntoquery</span></span>

## <span data-ttu-id="0d588-107">例子</span><span class="sxs-lookup"><span data-stu-id="0d588-107">EXAMPLES</span></span>

### <span data-ttu-id="0d588-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="0d588-108">Example 1</span></span>
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

<span data-ttu-id="0d588-109">要求資源欄位子集的簡單資源查詢。</span><span class="sxs-lookup"><span data-stu-id="0d588-109">Simple resources query requesting a subset of resource fields.</span></span>

### <span data-ttu-id="0d588-110">範例 2</span><span class="sxs-lookup"><span data-stu-id="0d588-110">Example 2</span></span>
```powershell
PS C:\> Search-AzGraph "project id, name, type, location | where type =~ 'Microsoft.Compute/virtualMachines' | summarize count() by location | top 3 by count_"

location      count_
--------      ------
eastus            66
westcentralus     32
westus            26
```

<span data-ttu-id="0d588-111">以欄位選取、篩選和摘要為特色之資源的複雜查詢。</span><span class="sxs-lookup"><span data-stu-id="0d588-111">A complex query on resources featuring field selection, filtering and summarizing.</span></span>

### <span data-ttu-id="0d588-112">範例 3</span><span class="sxs-lookup"><span data-stu-id="0d588-112">Example 3</span></span>
```powershell
PS C:\> Search-AzGraph -Include DisplayName -Query 'where type =~ "Microsoft.Compute/virtualMachines"| where properties.storageProfile.osDisk.managedDisk == "" | project name, resourceGroup, subscriptionDisplayName'

name         resourceGroup      subscriptionDisplayName
----         -------------      -----------------------
ContosoVM    RG-Contoso         Contoso Production Subscription                                               

```
<span data-ttu-id="0d588-113">具有所有虛擬機器的查詢，這些虛擬機器不是使用受管理的磁片，而且包含訂閱顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="0d588-113">A query featuring all virtual machines which are not using Managed Disks and includes subscription display names.</span></span>

### <span data-ttu-id="0d588-114">範例 4</span><span class="sxs-lookup"><span data-stu-id="0d588-114">Example 4</span></span>
```powershell
PS C:\> Search-AzGraph -Include DisplayName -Query 'summarize count() by tenantDisplayName, subscriptionDisplayName'

tenantDisplayName   subscriptionDisplayName              count_
-----------------   -----------------------              ------
ContosoTenant       Contoso Production Subscription      118                                           
```
<span data-ttu-id="0d588-115">顯示按租使用者和訂閱顯示名稱之資源計數的查詢。</span><span class="sxs-lookup"><span data-stu-id="0d588-115">A query displaying the count of resources by tenant and subscription display names.</span></span>

## <span data-ttu-id="0d588-116">參數</span><span class="sxs-lookup"><span data-stu-id="0d588-116">PARAMETERS</span></span>

### <span data-ttu-id="0d588-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d588-117">-DefaultProfile</span></span>
<span data-ttu-id="0d588-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0d588-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d588-119">-查詢</span><span class="sxs-lookup"><span data-stu-id="0d588-119">-Query</span></span>
<span data-ttu-id="0d588-120">資源圖形查詢。</span><span class="sxs-lookup"><span data-stu-id="0d588-120">Resource Graph query.</span></span>

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

### <span data-ttu-id="0d588-121">-訂閱</span><span class="sxs-lookup"><span data-stu-id="0d588-121">-Subscription</span></span>
<span data-ttu-id="0d588-122">訂閱 () 執行查詢。</span><span class="sxs-lookup"><span data-stu-id="0d588-122">Subscription(s) to run query against.</span></span>

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

### <span data-ttu-id="0d588-123">-略過</span><span class="sxs-lookup"><span data-stu-id="0d588-123">-Skip</span></span>
<span data-ttu-id="0d588-124">忽略前 N 個物件，然後獲得其餘的物件。</span><span class="sxs-lookup"><span data-stu-id="0d588-124">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="0d588-125">-第一個</span><span class="sxs-lookup"><span data-stu-id="0d588-125">-First</span></span>
<span data-ttu-id="0d588-126">要返回的物件數量上限。</span><span class="sxs-lookup"><span data-stu-id="0d588-126">The maximum number of objects to return.</span></span> <span data-ttu-id="0d588-127">允許的值：1-5000。</span><span class="sxs-lookup"><span data-stu-id="0d588-127">Allowed values: 1-5000.</span></span>
<span data-ttu-id="0d588-128">預設值為 100。</span><span class="sxs-lookup"><span data-stu-id="0d588-128">Default value is 100.</span></span>

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

### <span data-ttu-id="0d588-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d588-129">CommonParameters</span></span>
<span data-ttu-id="0d588-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0d588-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d588-131">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="0d588-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d588-132">輸入</span><span class="sxs-lookup"><span data-stu-id="0d588-132">INPUTS</span></span>

### <span data-ttu-id="0d588-133">沒有</span><span class="sxs-lookup"><span data-stu-id="0d588-133">None</span></span>

## <span data-ttu-id="0d588-134">輸出</span><span class="sxs-lookup"><span data-stu-id="0d588-134">OUTPUTS</span></span>

### <span data-ttu-id="0d588-135">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="0d588-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="0d588-136">筆記</span><span class="sxs-lookup"><span data-stu-id="0d588-136">NOTES</span></span>

## <span data-ttu-id="0d588-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="0d588-137">RELATED LINKS</span></span>
