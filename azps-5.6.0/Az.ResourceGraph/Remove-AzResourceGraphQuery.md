---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/powershell/module/az.resourcegraph/remove-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Remove-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Remove-AzResourceGraphQuery.md
ms.openlocfilehash: 0253a5fa7cf5ff13c678eb0a6d86c31335239fdb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914482"
---
# <span data-ttu-id="2b9e8-101">Remove-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="2b9e8-101">Remove-AzResourceGraphQuery</span></span>

## <span data-ttu-id="2b9e8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2b9e8-102">SYNOPSIS</span></span>
<span data-ttu-id="2b9e8-103">刪除圖形查詢。</span><span class="sxs-lookup"><span data-stu-id="2b9e8-103">Delete a graph query.</span></span>

## <span data-ttu-id="2b9e8-104">語法</span><span class="sxs-lookup"><span data-stu-id="2b9e8-104">SYNTAX</span></span>

### <span data-ttu-id="2b9e8-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="2b9e8-105">Delete (Default)</span></span>
```
Remove-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2b9e8-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2b9e8-106">DeleteViaIdentity</span></span>
```
Remove-AzResourceGraphQuery -InputObject <IResourceGraphIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2b9e8-107">描述</span><span class="sxs-lookup"><span data-stu-id="2b9e8-107">DESCRIPTION</span></span>
<span data-ttu-id="2b9e8-108">刪除圖形查詢。</span><span class="sxs-lookup"><span data-stu-id="2b9e8-108">Delete a graph query.</span></span>

## <span data-ttu-id="2b9e8-109">例子</span><span class="sxs-lookup"><span data-stu-id="2b9e8-109">EXAMPLES</span></span>

### <span data-ttu-id="2b9e8-110">範例 1：根據名稱移除資源圖形查詢</span><span class="sxs-lookup"><span data-stu-id="2b9e8-110">Example 1: Remove a resource graph query by name</span></span>
```powershell
PS C:\> Remove-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t03

```

<span data-ttu-id="2b9e8-111">此命令會按名稱移除資源圖形查詢。</span><span class="sxs-lookup"><span data-stu-id="2b9e8-111">This command removes a resource graph query by name.</span></span>

### <span data-ttu-id="2b9e8-112">範例 2：根據物件移除資源圖形查詢</span><span class="sxs-lookup"><span data-stu-id="2b9e8-112">Example 2: Remove a resource graph query by object</span></span>
```powershell
PS C:\> $query = Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t02
PS C:\> Remove-AzResourceGraphQuery -InputObject $query 

```

<span data-ttu-id="2b9e8-113">此命令會按物件移除資源圖形查詢。</span><span class="sxs-lookup"><span data-stu-id="2b9e8-113">This command removes a resource graph query by object.</span></span>

## <span data-ttu-id="2b9e8-114">參數</span><span class="sxs-lookup"><span data-stu-id="2b9e8-114">PARAMETERS</span></span>

### <span data-ttu-id="2b9e8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b9e8-115">-DefaultProfile</span></span>
<span data-ttu-id="2b9e8-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2b9e8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b9e8-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b9e8-117">-InputObject</span></span>
<span data-ttu-id="2b9e8-118">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="2b9e8-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b9e8-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="2b9e8-119">-Name</span></span>
<span data-ttu-id="2b9e8-120">Graph 查詢資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b9e8-120">The name of the Graph Query resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b9e8-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2b9e8-121">-PassThru</span></span>
<span data-ttu-id="2b9e8-122">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="2b9e8-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2b9e8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b9e8-123">-ResourceGroupName</span></span>
<span data-ttu-id="2b9e8-124">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b9e8-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b9e8-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2b9e8-125">-SubscriptionId</span></span>
<span data-ttu-id="2b9e8-126">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="2b9e8-126">The Azure subscription Id.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b9e8-127">-確認</span><span class="sxs-lookup"><span data-stu-id="2b9e8-127">-Confirm</span></span>
<span data-ttu-id="2b9e8-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2b9e8-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b9e8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b9e8-129">-WhatIf</span></span>
<span data-ttu-id="2b9e8-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2b9e8-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b9e8-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2b9e8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b9e8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b9e8-132">CommonParameters</span></span>
<span data-ttu-id="2b9e8-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2b9e8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b9e8-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2b9e8-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b9e8-135">輸入</span><span class="sxs-lookup"><span data-stu-id="2b9e8-135">INPUTS</span></span>

### <span data-ttu-id="2b9e8-136">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.models.IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="2b9e8-136">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="2b9e8-137">輸出</span><span class="sxs-lookup"><span data-stu-id="2b9e8-137">OUTPUTS</span></span>

### <span data-ttu-id="2b9e8-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2b9e8-138">System.Boolean</span></span>

## <span data-ttu-id="2b9e8-139">筆記</span><span class="sxs-lookup"><span data-stu-id="2b9e8-139">NOTES</span></span>

<span data-ttu-id="2b9e8-140">別名</span><span class="sxs-lookup"><span data-stu-id="2b9e8-140">ALIASES</span></span>

<span data-ttu-id="2b9e8-141">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="2b9e8-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2b9e8-142">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="2b9e8-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2b9e8-143">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="2b9e8-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2b9e8-144">INPUTOBJECT： <IResourceGraphIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="2b9e8-144">INPUTOBJECT <IResourceGraphIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2b9e8-145">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="2b9e8-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2b9e8-146">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b9e8-146">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="2b9e8-147">`[ResourceName <String>]`：Graph Query 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b9e8-147">`[ResourceName <String>]`: The name of the Graph Query resource.</span></span>
  - <span data-ttu-id="2b9e8-148">`[SubscriptionId <String>]`：Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="2b9e8-148">`[SubscriptionId <String>]`: The Azure subscription Id.</span></span>

## <span data-ttu-id="2b9e8-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="2b9e8-149">RELATED LINKS</span></span>

