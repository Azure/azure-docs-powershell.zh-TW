---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/powershell/module/az.resourcegraph/get-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Get-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Get-AzResourceGraphQuery.md
ms.openlocfilehash: 46f59df272a62ca9cd6b517d3672436a01a75ffb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914493"
---
# <span data-ttu-id="e6f18-101">Get-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="e6f18-101">Get-AzResourceGraphQuery</span></span>

## <span data-ttu-id="e6f18-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e6f18-102">SYNOPSIS</span></span>
<span data-ttu-id="e6f18-103">根據其 resourceName 取得單一圖形查詢。</span><span class="sxs-lookup"><span data-stu-id="e6f18-103">Get a single graph query by its resourceName.</span></span>

## <span data-ttu-id="e6f18-104">語法</span><span class="sxs-lookup"><span data-stu-id="e6f18-104">SYNTAX</span></span>

### <span data-ttu-id="e6f18-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="e6f18-105">List (Default)</span></span>
```
Get-AzResourceGraphQuery -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="e6f18-106">獲取</span><span class="sxs-lookup"><span data-stu-id="e6f18-106">Get</span></span>
```
Get-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e6f18-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e6f18-107">GetViaIdentity</span></span>
```
Get-AzResourceGraphQuery -InputObject <IResourceGraphIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="e6f18-108">描述</span><span class="sxs-lookup"><span data-stu-id="e6f18-108">DESCRIPTION</span></span>
<span data-ttu-id="e6f18-109">根據其 resourceName 取得單一圖形查詢。</span><span class="sxs-lookup"><span data-stu-id="e6f18-109">Get a single graph query by its resourceName.</span></span>

## <span data-ttu-id="e6f18-110">例子</span><span class="sxs-lookup"><span data-stu-id="e6f18-110">EXAMPLES</span></span>

### <span data-ttu-id="e6f18-111">範例 1：在資源群組下取得所有資源圖形查詢</span><span class="sxs-lookup"><span data-stu-id="e6f18-111">Example 1: Get all resource graph queries under a resource group</span></span>
```powershell
PS C:\> Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="e6f18-112">此命令會獲得資源群組下的所有資源圖形查詢。</span><span class="sxs-lookup"><span data-stu-id="e6f18-112">This command gets all resource graph query under a resource group.</span></span>

### <span data-ttu-id="e6f18-113">範例 2：根據名稱取得資源圖形查詢</span><span class="sxs-lookup"><span data-stu-id="e6f18-113">Example 2: Get a resource graph query by name</span></span>
```powershell
PS C:\> Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name SharedQuery-t01

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="e6f18-114">此命令會按名稱獲得資源圖形查詢。</span><span class="sxs-lookup"><span data-stu-id="e6f18-114">This command gets a resource graph query by name.</span></span>

### <span data-ttu-id="e6f18-115">範例 2：根據物件取得資源圖形查詢</span><span class="sxs-lookup"><span data-stu-id="e6f18-115">Example 2: Get a resource graph query by object</span></span>
```powershell
PS C:\> $query = New-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t03 -Location 'global' -Query 'project id, name, type, location' -Description 'test'
PS C:\> Get-AzResourceGraphQuery -InputObject $query

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="e6f18-116">此命令會按物件獲得資源圖形查詢。</span><span class="sxs-lookup"><span data-stu-id="e6f18-116">This command gets a resource graph query by object.</span></span>

## <span data-ttu-id="e6f18-117">參數</span><span class="sxs-lookup"><span data-stu-id="e6f18-117">PARAMETERS</span></span>

### <span data-ttu-id="e6f18-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6f18-118">-DefaultProfile</span></span>
<span data-ttu-id="e6f18-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e6f18-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6f18-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6f18-120">-InputObject</span></span>
<span data-ttu-id="e6f18-121">身分識別參數</span><span class="sxs-lookup"><span data-stu-id="e6f18-121">Identity Parameter</span></span>

<span data-ttu-id="e6f18-122">若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="e6f18-122">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6f18-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="e6f18-123">-Name</span></span>
<span data-ttu-id="e6f18-124">Graph 查詢資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="e6f18-124">The name of the Graph Query resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6f18-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6f18-125">-ResourceGroupName</span></span>
<span data-ttu-id="e6f18-126">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e6f18-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6f18-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e6f18-127">-SubscriptionId</span></span>
<span data-ttu-id="e6f18-128">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="e6f18-128">The Azure subscription Id.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6f18-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6f18-129">CommonParameters</span></span>
<span data-ttu-id="e6f18-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e6f18-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6f18-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e6f18-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6f18-132">輸入</span><span class="sxs-lookup"><span data-stu-id="e6f18-132">INPUTS</span></span>

### <span data-ttu-id="e6f18-133">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.models.IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="e6f18-133">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="e6f18-134">輸出</span><span class="sxs-lookup"><span data-stu-id="e6f18-134">OUTPUTS</span></span>

### <span data-ttu-id="e6f18-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.models.Api20180901Preview.IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="e6f18-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

## <span data-ttu-id="e6f18-136">筆記</span><span class="sxs-lookup"><span data-stu-id="e6f18-136">NOTES</span></span>

<span data-ttu-id="e6f18-137">別名</span><span class="sxs-lookup"><span data-stu-id="e6f18-137">ALIASES</span></span>

<span data-ttu-id="e6f18-138">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="e6f18-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e6f18-139">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="e6f18-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e6f18-140">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="e6f18-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e6f18-141">INPUTOBJECT： <IResourceGraphIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="e6f18-141">INPUTOBJECT <IResourceGraphIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e6f18-142">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="e6f18-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e6f18-143">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e6f18-143">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="e6f18-144">`[ResourceName <String>]`：Graph Query 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="e6f18-144">`[ResourceName <String>]`: The name of the Graph Query resource.</span></span>
  - <span data-ttu-id="e6f18-145">`[SubscriptionId <String>]`：Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="e6f18-145">`[SubscriptionId <String>]`: The Azure subscription Id.</span></span>

## <span data-ttu-id="e6f18-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="e6f18-146">RELATED LINKS</span></span>

