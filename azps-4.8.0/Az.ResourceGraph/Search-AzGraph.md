---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.dll-Help.xml
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/search-azgraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
ms.openlocfilehash: e1d9aa5c9bf2538f20d37a23b35dec4d7a850cbc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969116"
---
# <span data-ttu-id="3d24b-101">Search-AzGraph</span><span class="sxs-lookup"><span data-stu-id="3d24b-101">Search-AzGraph</span></span>

## <span data-ttu-id="3d24b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3d24b-102">SYNOPSIS</span></span>
<span data-ttu-id="3d24b-103">查詢由 Azure 資源管理器管理的資源。</span><span class="sxs-lookup"><span data-stu-id="3d24b-103">Queries the resources managed by Azure Resource Manager.</span></span>

## <span data-ttu-id="3d24b-104">句法</span><span class="sxs-lookup"><span data-stu-id="3d24b-104">SYNTAX</span></span>

```
Search-AzGraph [-Query] <String> [-Subscription <String[]>] [-First <Int32>] [-Skip <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d24b-105">說明</span><span class="sxs-lookup"><span data-stu-id="3d24b-105">DESCRIPTION</span></span>
<span data-ttu-id="3d24b-106">若要深入瞭解查詢語法，請參閱： https://aka.ms/resource-graph/learntoquery</span><span class="sxs-lookup"><span data-stu-id="3d24b-106">Learn more about the query syntax here: https://aka.ms/resource-graph/learntoquery</span></span>

## <span data-ttu-id="3d24b-107">示例</span><span class="sxs-lookup"><span data-stu-id="3d24b-107">EXAMPLES</span></span>

### <span data-ttu-id="3d24b-108">範例1</span><span class="sxs-lookup"><span data-stu-id="3d24b-108">Example 1</span></span>
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

<span data-ttu-id="3d24b-109">簡單的資源查詢，要求資源欄位的子集。</span><span class="sxs-lookup"><span data-stu-id="3d24b-109">Simple resources query requesting a subset of resource fields.</span></span>

### <span data-ttu-id="3d24b-110">範例2</span><span class="sxs-lookup"><span data-stu-id="3d24b-110">Example 2</span></span>
```powershell
PS C:\> Search-AzGraph "project id, name, type, location | where type =~ 'Microsoft.Compute/virtualMachines' | summarize count() by location | top 3 by count_"

location      count_
--------      ------
eastus            66
westcentralus     32
westus            26
```

<span data-ttu-id="3d24b-111">資源的複雜查詢，具有選取欄位、篩選及摘要。</span><span class="sxs-lookup"><span data-stu-id="3d24b-111">A complex query on resources featuring field selection, filtering and summarizing.</span></span>

### <span data-ttu-id="3d24b-112">範例3</span><span class="sxs-lookup"><span data-stu-id="3d24b-112">Example 3</span></span>
```powershell
PS C:\> Search-AzGraph -Include DisplayName -Query 'where type =~ "Microsoft.Compute/virtualMachines"| where properties.storageProfile.osDisk.managedDisk == "" | project name, resourceGroup, subscriptionDisplayName'

name         resourceGroup      subscriptionDisplayName
----         -------------      -----------------------
ContosoVM    RG-Contoso         Contoso Production Subscription                                               

```
<span data-ttu-id="3d24b-113">含所有未使用受管理磁片並包含訂閱顯示名稱的虛擬機器的查詢。</span><span class="sxs-lookup"><span data-stu-id="3d24b-113">A query featuring all virtual machines which are not using Managed Disks and includes subscription display names.</span></span>

### <span data-ttu-id="3d24b-114">範例4</span><span class="sxs-lookup"><span data-stu-id="3d24b-114">Example 4</span></span>
```powershell
PS C:\> Search-AzGraph -Include DisplayName -Query 'summarize count() by tenantDisplayName, subscriptionDisplayName'

tenantDisplayName   subscriptionDisplayName              count_
-----------------   -----------------------              ------
ContosoTenant       Contoso Production Subscription      118                                           
```
<span data-ttu-id="3d24b-115">依租使用者及訂閱顯示名稱顯示資源計數的查詢。</span><span class="sxs-lookup"><span data-stu-id="3d24b-115">A query displaying the count of resources by tenant and subscription display names.</span></span>

## <span data-ttu-id="3d24b-116">參數</span><span class="sxs-lookup"><span data-stu-id="3d24b-116">PARAMETERS</span></span>

### <span data-ttu-id="3d24b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d24b-117">-DefaultProfile</span></span>
<span data-ttu-id="3d24b-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3d24b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d24b-119">-Query</span><span class="sxs-lookup"><span data-stu-id="3d24b-119">-Query</span></span>
<span data-ttu-id="3d24b-120">[資源圖表] 查詢。</span><span class="sxs-lookup"><span data-stu-id="3d24b-120">Resource Graph query.</span></span>

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

### <span data-ttu-id="3d24b-121">-訂閱</span><span class="sxs-lookup"><span data-stu-id="3d24b-121">-Subscription</span></span>
<span data-ttu-id="3d24b-122">[訂閱] (s) 來執行查詢。</span><span class="sxs-lookup"><span data-stu-id="3d24b-122">Subscription(s) to run query against.</span></span>

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

### <span data-ttu-id="3d24b-123">-略過</span><span class="sxs-lookup"><span data-stu-id="3d24b-123">-Skip</span></span>
<span data-ttu-id="3d24b-124">忽略前 N 個物件，然後取得剩餘的物件。</span><span class="sxs-lookup"><span data-stu-id="3d24b-124">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="3d24b-125">-優先</span><span class="sxs-lookup"><span data-stu-id="3d24b-125">-First</span></span>
<span data-ttu-id="3d24b-126">要傳回的物件數目上限。</span><span class="sxs-lookup"><span data-stu-id="3d24b-126">The maximum number of objects to return.</span></span> <span data-ttu-id="3d24b-127">允許的值：1-5000。</span><span class="sxs-lookup"><span data-stu-id="3d24b-127">Allowed values: 1-5000.</span></span>
<span data-ttu-id="3d24b-128">預設值為100。</span><span class="sxs-lookup"><span data-stu-id="3d24b-128">Default value is 100.</span></span>

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

### <span data-ttu-id="3d24b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d24b-129">CommonParameters</span></span>
<span data-ttu-id="3d24b-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3d24b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d24b-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3d24b-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d24b-132">輸入</span><span class="sxs-lookup"><span data-stu-id="3d24b-132">INPUTS</span></span>

### <span data-ttu-id="3d24b-133">所有</span><span class="sxs-lookup"><span data-stu-id="3d24b-133">None</span></span>

## <span data-ttu-id="3d24b-134">輸出</span><span class="sxs-lookup"><span data-stu-id="3d24b-134">OUTPUTS</span></span>

### <span data-ttu-id="3d24b-135">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="3d24b-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="3d24b-136">筆記</span><span class="sxs-lookup"><span data-stu-id="3d24b-136">NOTES</span></span>

## <span data-ttu-id="3d24b-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="3d24b-137">RELATED LINKS</span></span>
