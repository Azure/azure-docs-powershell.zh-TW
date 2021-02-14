---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/update-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Update-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Update-AzResourceGraphQuery.md
ms.openlocfilehash: 6ae44183a368babb43a93063518dfbf4f3d15e18
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127199"
---
# <span data-ttu-id="9b7fb-101">Update-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="9b7fb-101">Update-AzResourceGraphQuery</span></span>

## <span data-ttu-id="9b7fb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9b7fb-102">SYNOPSIS</span></span>
<span data-ttu-id="9b7fb-103">更新已新增的圖形查詢。</span><span class="sxs-lookup"><span data-stu-id="9b7fb-103">Updates a graph query that has already been added.</span></span>

## <span data-ttu-id="9b7fb-104">句法</span><span class="sxs-lookup"><span data-stu-id="9b7fb-104">SYNTAX</span></span>

### <span data-ttu-id="9b7fb-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="9b7fb-105">UpdateExpanded (Default)</span></span>
```
Update-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-File <String>] [-Query <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9b7fb-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="9b7fb-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzResourceGraphQuery -InputObject <IResourceGraphIdentity> [-Description <String>] [-File <String>]
 [-Query <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9b7fb-107">說明</span><span class="sxs-lookup"><span data-stu-id="9b7fb-107">DESCRIPTION</span></span>
<span data-ttu-id="9b7fb-108">更新已新增的圖形查詢。</span><span class="sxs-lookup"><span data-stu-id="9b7fb-108">Updates a graph query that has already been added.</span></span>

## <span data-ttu-id="9b7fb-109">示例</span><span class="sxs-lookup"><span data-stu-id="9b7fb-109">EXAMPLES</span></span>

### <span data-ttu-id="9b7fb-110">範例1：依名稱更新參數查詢和標記</span><span class="sxs-lookup"><span data-stu-id="9b7fb-110">Example 1: Update the parameter query and tag by name</span></span>
```powershell
PS C:\>  Update-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t05 -Query "project id, name, type, location, tags"  -Tag @{'key1'=1;'key2'=2}

Location Name      Type
-------- ----      ----
     global   query-t05 microsoft.resourcegraph/queries
```

<span data-ttu-id="9b7fb-111">這個命令會依名稱更新參數查詢和標記。</span><span class="sxs-lookup"><span data-stu-id="9b7fb-111">This command updates the parameter query and tag by name.</span></span>

### <span data-ttu-id="9b7fb-112">範例2：依物件更新參數檔</span><span class="sxs-lookup"><span data-stu-id="9b7fb-112">Example 2: Update the parameter file by object</span></span>
```powershell
PS C:\> $query =  Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t05 
PS C:\> Update-AzResourceGraphQuery -InputObject $query -File './Query.kql'

Location Name      Type
-------- ----      ----
     global   query-t05 microsoft.resourcegraph/queries
```

<span data-ttu-id="9b7fb-113">這個命令會根據物件更新參數查詢及標記。</span><span class="sxs-lookup"><span data-stu-id="9b7fb-113">This command updates the parameter query and tag by object.</span></span>

## <span data-ttu-id="9b7fb-114">參數</span><span class="sxs-lookup"><span data-stu-id="9b7fb-114">PARAMETERS</span></span>

### <span data-ttu-id="9b7fb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b7fb-115">-DefaultProfile</span></span>
<span data-ttu-id="9b7fb-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9b7fb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b7fb-117">-描述</span><span class="sxs-lookup"><span data-stu-id="9b7fb-117">-Description</span></span>
<span data-ttu-id="9b7fb-118">圖表查詢的描述。</span><span class="sxs-lookup"><span data-stu-id="9b7fb-118">The description of a graph query.</span></span>

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

### <span data-ttu-id="9b7fb-119">檔案</span><span class="sxs-lookup"><span data-stu-id="9b7fb-119">-File</span></span>
<span data-ttu-id="9b7fb-120">檔案的內容會傳遞到查詢參數。</span><span class="sxs-lookup"><span data-stu-id="9b7fb-120">The content of the file will be passed to the query parameter.</span></span>

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

### <span data-ttu-id="9b7fb-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b7fb-121">-InputObject</span></span>
<span data-ttu-id="9b7fb-122">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="9b7fb-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b7fb-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="9b7fb-123">-Name</span></span>
<span data-ttu-id="9b7fb-124">圖形查詢資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="9b7fb-124">The name of the Graph Query resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b7fb-125">-Query</span><span class="sxs-lookup"><span data-stu-id="9b7fb-125">-Query</span></span>
<span data-ttu-id="9b7fb-126">將會成為圖形的 KQL 查詢。</span><span class="sxs-lookup"><span data-stu-id="9b7fb-126">KQL query that will be graph.</span></span>

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

### <span data-ttu-id="9b7fb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b7fb-127">-ResourceGroupName</span></span>
<span data-ttu-id="9b7fb-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9b7fb-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b7fb-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9b7fb-129">-SubscriptionId</span></span>
<span data-ttu-id="9b7fb-130">Azure 訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="9b7fb-130">The Azure subscription Id.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b7fb-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="9b7fb-131">-Tag</span></span>
<span data-ttu-id="9b7fb-132">資源標記</span><span class="sxs-lookup"><span data-stu-id="9b7fb-132">Resource tags</span></span>

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

### <span data-ttu-id="9b7fb-133">-確認</span><span class="sxs-lookup"><span data-stu-id="9b7fb-133">-Confirm</span></span>
<span data-ttu-id="9b7fb-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9b7fb-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b7fb-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b7fb-135">-WhatIf</span></span>
<span data-ttu-id="9b7fb-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9b7fb-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b7fb-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9b7fb-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b7fb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b7fb-138">CommonParameters</span></span>
<span data-ttu-id="9b7fb-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9b7fb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b7fb-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9b7fb-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b7fb-141">輸入</span><span class="sxs-lookup"><span data-stu-id="9b7fb-141">INPUTS</span></span>

### <span data-ttu-id="9b7fb-142">IResourceGraphIdentity （ResourceGraph）的</span><span class="sxs-lookup"><span data-stu-id="9b7fb-142">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="9b7fb-143">輸出</span><span class="sxs-lookup"><span data-stu-id="9b7fb-143">OUTPUTS</span></span>

### <span data-ttu-id="9b7fb-144">IGraphQueryResource （ResourceGraph）。 Api20180901Preview。</span><span class="sxs-lookup"><span data-stu-id="9b7fb-144">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

## <span data-ttu-id="9b7fb-145">筆記</span><span class="sxs-lookup"><span data-stu-id="9b7fb-145">NOTES</span></span>

<span data-ttu-id="9b7fb-146">別名</span><span class="sxs-lookup"><span data-stu-id="9b7fb-146">ALIASES</span></span>

<span data-ttu-id="9b7fb-147">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="9b7fb-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9b7fb-148">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="9b7fb-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9b7fb-149">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="9b7fb-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9b7fb-150">INPUTOBJECT <IResourceGraphIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="9b7fb-150">INPUTOBJECT <IResourceGraphIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9b7fb-151">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="9b7fb-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9b7fb-152">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9b7fb-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="9b7fb-153">`[ResourceName <String>]`：圖表查詢資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="9b7fb-153">`[ResourceName <String>]`: The name of the Graph Query resource.</span></span>
  - <span data-ttu-id="9b7fb-154">`[SubscriptionId <String>]`： Azure 訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="9b7fb-154">`[SubscriptionId <String>]`: The Azure subscription Id.</span></span>

## <span data-ttu-id="9b7fb-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="9b7fb-155">RELATED LINKS</span></span>

