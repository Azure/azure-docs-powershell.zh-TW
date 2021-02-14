---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/get-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Get-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Get-AzResourceGraphQuery.md
ms.openlocfilehash: 6d7dbb9acbcc03f266d698d1f9d8ce89f320d04b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127226"
---
# <span data-ttu-id="43cf1-101">Get-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="43cf1-101">Get-AzResourceGraphQuery</span></span>

## <span data-ttu-id="43cf1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="43cf1-102">SYNOPSIS</span></span>
<span data-ttu-id="43cf1-103">透過其使用方式來取得單一圖形查詢。</span><span class="sxs-lookup"><span data-stu-id="43cf1-103">Get a single graph query by its resourceName.</span></span>

## <span data-ttu-id="43cf1-104">句法</span><span class="sxs-lookup"><span data-stu-id="43cf1-104">SYNTAX</span></span>

### <span data-ttu-id="43cf1-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="43cf1-105">List (Default)</span></span>
```
Get-AzResourceGraphQuery -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="43cf1-106">獲取</span><span class="sxs-lookup"><span data-stu-id="43cf1-106">Get</span></span>
```
Get-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="43cf1-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="43cf1-107">GetViaIdentity</span></span>
```
Get-AzResourceGraphQuery -InputObject <IResourceGraphIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="43cf1-108">說明</span><span class="sxs-lookup"><span data-stu-id="43cf1-108">DESCRIPTION</span></span>
<span data-ttu-id="43cf1-109">透過其使用方式來取得單一圖形查詢。</span><span class="sxs-lookup"><span data-stu-id="43cf1-109">Get a single graph query by its resourceName.</span></span>

## <span data-ttu-id="43cf1-110">示例</span><span class="sxs-lookup"><span data-stu-id="43cf1-110">EXAMPLES</span></span>

### <span data-ttu-id="43cf1-111">範例1：取得資源群組下的所有資源圖表查詢</span><span class="sxs-lookup"><span data-stu-id="43cf1-111">Example 1: Get all resource graph query under a resource group</span></span>
```powershell
PS C:\> Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="43cf1-112">這個命令會取得資源群組下的所有資源圖表查詢。</span><span class="sxs-lookup"><span data-stu-id="43cf1-112">This command gets all resource graph query under a resource group.</span></span>

### <span data-ttu-id="43cf1-113">範例2：依名稱取得資源圖表查詢</span><span class="sxs-lookup"><span data-stu-id="43cf1-113">Example 2: Get a resource graph query by name</span></span>
```powershell
PS C:\> Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name SharedQuery-t01

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="43cf1-114">這個命令會依名稱取得資源圖表查詢。</span><span class="sxs-lookup"><span data-stu-id="43cf1-114">This command gets a resource graph query by name.</span></span>

### <span data-ttu-id="43cf1-115">範例2：透過 objecy 取得資源圖表查詢</span><span class="sxs-lookup"><span data-stu-id="43cf1-115">Example 2: Get a resource graph query by objecy</span></span>
```powershell
PS C:\> $query = New-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t03 -Location 'global' -Query 'project id, name, type, location' -Description 'test'
PS C:\> Get-AzResourceGraphQuery -InputObject $query

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="43cf1-116">這個命令會透過物件取得資源圖表查詢。</span><span class="sxs-lookup"><span data-stu-id="43cf1-116">This command gets a resource graph query by object.</span></span>

## <span data-ttu-id="43cf1-117">參數</span><span class="sxs-lookup"><span data-stu-id="43cf1-117">PARAMETERS</span></span>

### <span data-ttu-id="43cf1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43cf1-118">-DefaultProfile</span></span>
<span data-ttu-id="43cf1-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="43cf1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43cf1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43cf1-120">-InputObject</span></span>
<span data-ttu-id="43cf1-121">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="43cf1-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="43cf1-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="43cf1-122">-Name</span></span>
<span data-ttu-id="43cf1-123">圖形查詢資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="43cf1-123">The name of the Graph Query resource.</span></span>

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

### <span data-ttu-id="43cf1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43cf1-124">-ResourceGroupName</span></span>
<span data-ttu-id="43cf1-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="43cf1-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="43cf1-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="43cf1-126">-SubscriptionId</span></span>
<span data-ttu-id="43cf1-127">Azure 訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="43cf1-127">The Azure subscription Id.</span></span>

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

### <span data-ttu-id="43cf1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43cf1-128">CommonParameters</span></span>
<span data-ttu-id="43cf1-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="43cf1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43cf1-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="43cf1-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43cf1-131">輸入</span><span class="sxs-lookup"><span data-stu-id="43cf1-131">INPUTS</span></span>

### <span data-ttu-id="43cf1-132">IResourceGraphIdentity （ResourceGraph）的</span><span class="sxs-lookup"><span data-stu-id="43cf1-132">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="43cf1-133">輸出</span><span class="sxs-lookup"><span data-stu-id="43cf1-133">OUTPUTS</span></span>

### <span data-ttu-id="43cf1-134">IGraphQueryResource （ResourceGraph）。 Api20180901Preview。</span><span class="sxs-lookup"><span data-stu-id="43cf1-134">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

## <span data-ttu-id="43cf1-135">筆記</span><span class="sxs-lookup"><span data-stu-id="43cf1-135">NOTES</span></span>

<span data-ttu-id="43cf1-136">別名</span><span class="sxs-lookup"><span data-stu-id="43cf1-136">ALIASES</span></span>

<span data-ttu-id="43cf1-137">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="43cf1-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="43cf1-138">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="43cf1-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="43cf1-139">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="43cf1-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="43cf1-140">INPUTOBJECT <IResourceGraphIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="43cf1-140">INPUTOBJECT <IResourceGraphIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="43cf1-141">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="43cf1-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="43cf1-142">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="43cf1-142">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="43cf1-143">`[ResourceName <String>]`：圖表查詢資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="43cf1-143">`[ResourceName <String>]`: The name of the Graph Query resource.</span></span>
  - <span data-ttu-id="43cf1-144">`[SubscriptionId <String>]`： Azure 訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="43cf1-144">`[SubscriptionId <String>]`: The Azure subscription Id.</span></span>

## <span data-ttu-id="43cf1-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="43cf1-145">RELATED LINKS</span></span>

