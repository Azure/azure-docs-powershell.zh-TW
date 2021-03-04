---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/powershell/module/az.databricks/remove-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksVNetPeering.md
ms.openlocfilehash: 986bea9de45ea8a628cea8eda4d8a63ec74d46fc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909113"
---
# <span data-ttu-id="4262a-101">Remove-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="4262a-101">Remove-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="4262a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4262a-102">SYNOPSIS</span></span>
<span data-ttu-id="4262a-103">刪除工作區 vNetPeering。</span><span class="sxs-lookup"><span data-stu-id="4262a-103">Deletes the workspace vNetPeering.</span></span>

## <span data-ttu-id="4262a-104">語法</span><span class="sxs-lookup"><span data-stu-id="4262a-104">SYNTAX</span></span>

### <span data-ttu-id="4262a-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="4262a-105">Delete (Default)</span></span>
```
Remove-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="4262a-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4262a-106">DeleteViaIdentity</span></span>
```
Remove-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4262a-107">描述</span><span class="sxs-lookup"><span data-stu-id="4262a-107">DESCRIPTION</span></span>
<span data-ttu-id="4262a-108">刪除工作區 vNetPeering。</span><span class="sxs-lookup"><span data-stu-id="4262a-108">Deletes the workspace vNetPeering.</span></span>

## <span data-ttu-id="4262a-109">例子</span><span class="sxs-lookup"><span data-stu-id="4262a-109">EXAMPLES</span></span>

### <span data-ttu-id="4262a-110">範例 1：根據名稱移除 datab一s 的 vnet 對等</span><span class="sxs-lookup"><span data-stu-id="4262a-110">Example 1: Remove a vnet peering of databricks by name</span></span>
```powershell
PS C:\> Remove-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01

```

<span data-ttu-id="4262a-111">此命令會移除資料表名稱的 vnet 對等</span><span class="sxs-lookup"><span data-stu-id="4262a-111">This command removes a vnet peering of databricks by name</span></span>

### <span data-ttu-id="4262a-112">範例 2：移除資料b用物件進行 vnet 對等</span><span class="sxs-lookup"><span data-stu-id="4262a-112">Example 2: Remove a vnet peering of databricks by object</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -ResourceGroupName lucas-manual-test -WorkspaceName databricks-test01 -PeeringName MyPeering-test01 | Remove-AzDatabricksVNetPeering

```

<span data-ttu-id="4262a-113">此命令會移除資料表物件之 vnet 對等</span><span class="sxs-lookup"><span data-stu-id="4262a-113">This command removes a vnet peering of databricks by object</span></span>

## <span data-ttu-id="4262a-114">參數</span><span class="sxs-lookup"><span data-stu-id="4262a-114">PARAMETERS</span></span>

### <span data-ttu-id="4262a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4262a-115">-AsJob</span></span>
<span data-ttu-id="4262a-116">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="4262a-116">Run the command as a job</span></span>

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

### <span data-ttu-id="4262a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4262a-117">-DefaultProfile</span></span>
<span data-ttu-id="4262a-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4262a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4262a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4262a-119">-InputObject</span></span>
<span data-ttu-id="4262a-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="4262a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4262a-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="4262a-121">-Name</span></span>
<span data-ttu-id="4262a-122">工作區 vNet 對等的名稱。</span><span class="sxs-lookup"><span data-stu-id="4262a-122">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="4262a-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4262a-123">-NoWait</span></span>
<span data-ttu-id="4262a-124">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="4262a-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4262a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4262a-125">-PassThru</span></span>
<span data-ttu-id="4262a-126">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="4262a-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4262a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4262a-127">-ResourceGroupName</span></span>
<span data-ttu-id="4262a-128">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4262a-128">The name of the resource group.</span></span>
<span data-ttu-id="4262a-129">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="4262a-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4262a-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4262a-130">-SubscriptionId</span></span>
<span data-ttu-id="4262a-131">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="4262a-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="4262a-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4262a-132">-WorkspaceName</span></span>
<span data-ttu-id="4262a-133">工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="4262a-133">The name of the workspace.</span></span>

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

### <span data-ttu-id="4262a-134">-確認</span><span class="sxs-lookup"><span data-stu-id="4262a-134">-Confirm</span></span>
<span data-ttu-id="4262a-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4262a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4262a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4262a-136">-WhatIf</span></span>
<span data-ttu-id="4262a-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4262a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4262a-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4262a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4262a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4262a-139">CommonParameters</span></span>
<span data-ttu-id="4262a-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4262a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4262a-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4262a-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4262a-142">輸入</span><span class="sxs-lookup"><span data-stu-id="4262a-142">INPUTS</span></span>

### <span data-ttu-id="4262a-143">Microsoft.Azure.PowerShell.Cmdlets.Databuvs.models.IDatab一sIdentity</span><span class="sxs-lookup"><span data-stu-id="4262a-143">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="4262a-144">輸出</span><span class="sxs-lookup"><span data-stu-id="4262a-144">OUTPUTS</span></span>

### <span data-ttu-id="4262a-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4262a-145">System.Boolean</span></span>

## <span data-ttu-id="4262a-146">筆記</span><span class="sxs-lookup"><span data-stu-id="4262a-146">NOTES</span></span>

<span data-ttu-id="4262a-147">別名</span><span class="sxs-lookup"><span data-stu-id="4262a-147">ALIASES</span></span>

<span data-ttu-id="4262a-148">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="4262a-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4262a-149">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="4262a-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4262a-150">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="4262a-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4262a-151">INPUTOBJECT： <IDatabricksIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="4262a-151">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4262a-152">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="4262a-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4262a-153">`[PeeringName <String>]`：工作區 vNet 對等的名稱。</span><span class="sxs-lookup"><span data-stu-id="4262a-153">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="4262a-154">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4262a-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="4262a-155">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="4262a-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="4262a-156">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="4262a-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="4262a-157">`[WorkspaceName <String>]`：工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="4262a-157">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="4262a-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="4262a-158">RELATED LINKS</span></span>

