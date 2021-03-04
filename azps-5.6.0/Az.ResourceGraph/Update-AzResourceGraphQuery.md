---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/powershell/module/az.resourcegraph/update-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Update-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Update-AzResourceGraphQuery.md
ms.openlocfilehash: 60dcb163e480371fe211651cc929b6335877490b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914478"
---
# <span data-ttu-id="eabcc-101">Update-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="eabcc-101">Update-AzResourceGraphQuery</span></span>

## <span data-ttu-id="eabcc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="eabcc-102">SYNOPSIS</span></span>
<span data-ttu-id="eabcc-103">更新已新增的圖形查詢。</span><span class="sxs-lookup"><span data-stu-id="eabcc-103">Updates a graph query that has already been added.</span></span>

## <span data-ttu-id="eabcc-104">語法</span><span class="sxs-lookup"><span data-stu-id="eabcc-104">SYNTAX</span></span>

### <span data-ttu-id="eabcc-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="eabcc-105">UpdateExpanded (Default)</span></span>
```
Update-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-File <String>] [-Query <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="eabcc-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="eabcc-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzResourceGraphQuery -InputObject <IResourceGraphIdentity> [-Description <String>] [-File <String>]
 [-Query <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="eabcc-107">描述</span><span class="sxs-lookup"><span data-stu-id="eabcc-107">DESCRIPTION</span></span>
<span data-ttu-id="eabcc-108">更新已新增的圖形查詢。</span><span class="sxs-lookup"><span data-stu-id="eabcc-108">Updates a graph query that has already been added.</span></span>

## <span data-ttu-id="eabcc-109">例子</span><span class="sxs-lookup"><span data-stu-id="eabcc-109">EXAMPLES</span></span>

### <span data-ttu-id="eabcc-110">範例 1：更新參數查詢和按名稱標記</span><span class="sxs-lookup"><span data-stu-id="eabcc-110">Example 1: Update the parameter query and tag by name</span></span>
```powershell
PS C:\>  Update-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t05 -Query "project id, name, type, location, tags"  -Tag @{'key1'=1;'key2'=2}

Location Name      Type
-------- ----      ----
     global   query-t05 microsoft.resourcegraph/queries
```

<span data-ttu-id="eabcc-111">此命令會更新參數查詢，並按名稱標記。</span><span class="sxs-lookup"><span data-stu-id="eabcc-111">This command updates the parameter query and tag by name.</span></span>

### <span data-ttu-id="eabcc-112">範例 2：按物件更新參數檔案</span><span class="sxs-lookup"><span data-stu-id="eabcc-112">Example 2: Update the parameter file by object</span></span>
```powershell
PS C:\> $query =  Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t05 
PS C:\> Update-AzResourceGraphQuery -InputObject $query -File './Query.kql'

Location Name      Type
-------- ----      ----
     global   query-t05 microsoft.resourcegraph/queries
```

<span data-ttu-id="eabcc-113">此命令會更新參數查詢，並按物件標記。</span><span class="sxs-lookup"><span data-stu-id="eabcc-113">This command updates the parameter query and tag by object.</span></span>

## <span data-ttu-id="eabcc-114">參數</span><span class="sxs-lookup"><span data-stu-id="eabcc-114">PARAMETERS</span></span>

### <span data-ttu-id="eabcc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eabcc-115">-DefaultProfile</span></span>
<span data-ttu-id="eabcc-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="eabcc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eabcc-117">-描述</span><span class="sxs-lookup"><span data-stu-id="eabcc-117">-Description</span></span>
<span data-ttu-id="eabcc-118">圖形查詢的描述。</span><span class="sxs-lookup"><span data-stu-id="eabcc-118">The description of a graph query.</span></span>

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

### <span data-ttu-id="eabcc-119">-檔案</span><span class="sxs-lookup"><span data-stu-id="eabcc-119">-File</span></span>
<span data-ttu-id="eabcc-120">檔案的內容會傳遞至查詢參數。</span><span class="sxs-lookup"><span data-stu-id="eabcc-120">The content of the file will be passed to the query parameter.</span></span>

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

### <span data-ttu-id="eabcc-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eabcc-121">-InputObject</span></span>
<span data-ttu-id="eabcc-122">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="eabcc-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="eabcc-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="eabcc-123">-Name</span></span>
<span data-ttu-id="eabcc-124">Graph 查詢資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="eabcc-124">The name of the Graph Query resource.</span></span>

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

### <span data-ttu-id="eabcc-125">-查詢</span><span class="sxs-lookup"><span data-stu-id="eabcc-125">-Query</span></span>
<span data-ttu-id="eabcc-126">將會是圖形的 KQL 查詢。</span><span class="sxs-lookup"><span data-stu-id="eabcc-126">KQL query that will be graph.</span></span>

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

### <span data-ttu-id="eabcc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eabcc-127">-ResourceGroupName</span></span>
<span data-ttu-id="eabcc-128">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="eabcc-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="eabcc-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="eabcc-129">-SubscriptionId</span></span>
<span data-ttu-id="eabcc-130">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="eabcc-130">The Azure subscription Id.</span></span>

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

### <span data-ttu-id="eabcc-131">-標記</span><span class="sxs-lookup"><span data-stu-id="eabcc-131">-Tag</span></span>
<span data-ttu-id="eabcc-132">資源標記</span><span class="sxs-lookup"><span data-stu-id="eabcc-132">Resource tags</span></span>

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

### <span data-ttu-id="eabcc-133">-確認</span><span class="sxs-lookup"><span data-stu-id="eabcc-133">-Confirm</span></span>
<span data-ttu-id="eabcc-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="eabcc-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eabcc-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eabcc-135">-WhatIf</span></span>
<span data-ttu-id="eabcc-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="eabcc-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eabcc-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eabcc-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eabcc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eabcc-138">CommonParameters</span></span>
<span data-ttu-id="eabcc-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="eabcc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eabcc-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eabcc-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eabcc-141">輸入</span><span class="sxs-lookup"><span data-stu-id="eabcc-141">INPUTS</span></span>

### <span data-ttu-id="eabcc-142">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.models.IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="eabcc-142">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="eabcc-143">輸出</span><span class="sxs-lookup"><span data-stu-id="eabcc-143">OUTPUTS</span></span>

### <span data-ttu-id="eabcc-144">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.models.Api20180901Preview.IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="eabcc-144">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

## <span data-ttu-id="eabcc-145">筆記</span><span class="sxs-lookup"><span data-stu-id="eabcc-145">NOTES</span></span>

<span data-ttu-id="eabcc-146">別名</span><span class="sxs-lookup"><span data-stu-id="eabcc-146">ALIASES</span></span>

<span data-ttu-id="eabcc-147">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="eabcc-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="eabcc-148">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="eabcc-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="eabcc-149">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="eabcc-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="eabcc-150">INPUTOBJECT： <IResourceGraphIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="eabcc-150">INPUTOBJECT <IResourceGraphIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="eabcc-151">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="eabcc-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="eabcc-152">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="eabcc-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="eabcc-153">`[ResourceName <String>]`：Graph Query 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="eabcc-153">`[ResourceName <String>]`: The name of the Graph Query resource.</span></span>
  - <span data-ttu-id="eabcc-154">`[SubscriptionId <String>]`：Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="eabcc-154">`[SubscriptionId <String>]`: The Azure subscription Id.</span></span>

## <span data-ttu-id="eabcc-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="eabcc-155">RELATED LINKS</span></span>

