---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/powershell/module/az.databricks/remove-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksWorkspace.md
ms.openlocfilehash: c8e63bd0a6496b1c0ce0899f0e183fb10db32a7b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904481"
---
# <span data-ttu-id="f0eb1-101">Remove-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="f0eb1-101">Remove-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="f0eb1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f0eb1-102">SYNOPSIS</span></span>
<span data-ttu-id="f0eb1-103">刪除工作區。</span><span class="sxs-lookup"><span data-stu-id="f0eb1-103">Deletes the workspace.</span></span>

## <span data-ttu-id="f0eb1-104">語法</span><span class="sxs-lookup"><span data-stu-id="f0eb1-104">SYNTAX</span></span>

### <span data-ttu-id="f0eb1-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="f0eb1-105">Delete (Default)</span></span>
```
Remove-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f0eb1-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f0eb1-106">DeleteViaIdentity</span></span>
```
Remove-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f0eb1-107">描述</span><span class="sxs-lookup"><span data-stu-id="f0eb1-107">DESCRIPTION</span></span>
<span data-ttu-id="f0eb1-108">刪除工作區。</span><span class="sxs-lookup"><span data-stu-id="f0eb1-108">Deletes the workspace.</span></span>

## <span data-ttu-id="f0eb1-109">例子</span><span class="sxs-lookup"><span data-stu-id="f0eb1-109">EXAMPLES</span></span>

### <span data-ttu-id="f0eb1-110">範例 1：移除 Datab一s 工作區</span><span class="sxs-lookup"><span data-stu-id="f0eb1-110">Example 1: Remove a Databricks workspace</span></span>
```powershell
PS C:\> Remove-AzDatabricksWorkspace -ResourceGroupName testgroup -Name databricks-test
```

<span data-ttu-id="f0eb1-111">此命令會從資源群組移除 Datab一s 工作區。</span><span class="sxs-lookup"><span data-stu-id="f0eb1-111">This command removes a Databricks workspace from a resource group.</span></span>

### <span data-ttu-id="f0eb1-112">範例 2：根據物件移除 Datab本體工作區</span><span class="sxs-lookup"><span data-stu-id="f0eb1-112">Example 2: Remove a Databricks workspace by object</span></span>
```powershell
PS C:\> $dbr = Get-AzDatabricksWorkspace -ResourceGroupName testgroup -Name databricks-test02
PS C:\> Remove-AzDatabricksWorkspace -InputObject $dbr
```

<span data-ttu-id="f0eb1-113">此命令會從資源群組移除 Datab一s 工作區。</span><span class="sxs-lookup"><span data-stu-id="f0eb1-113">This command removes a Databricks workspace from a resource group.</span></span>

## <span data-ttu-id="f0eb1-114">參數</span><span class="sxs-lookup"><span data-stu-id="f0eb1-114">PARAMETERS</span></span>

### <span data-ttu-id="f0eb1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f0eb1-115">-AsJob</span></span>
<span data-ttu-id="f0eb1-116">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="f0eb1-116">Run the command as a job</span></span>

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

### <span data-ttu-id="f0eb1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0eb1-117">-DefaultProfile</span></span>
<span data-ttu-id="f0eb1-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f0eb1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0eb1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0eb1-119">-InputObject</span></span>
<span data-ttu-id="f0eb1-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="f0eb1-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f0eb1-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="f0eb1-121">-Name</span></span>
<span data-ttu-id="f0eb1-122">工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="f0eb1-122">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0eb1-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f0eb1-123">-NoWait</span></span>
<span data-ttu-id="f0eb1-124">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="f0eb1-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f0eb1-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f0eb1-125">-PassThru</span></span>
<span data-ttu-id="f0eb1-126">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="f0eb1-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f0eb1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0eb1-127">-ResourceGroupName</span></span>
<span data-ttu-id="f0eb1-128">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f0eb1-128">The name of the resource group.</span></span>
<span data-ttu-id="f0eb1-129">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="f0eb1-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f0eb1-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f0eb1-130">-SubscriptionId</span></span>
<span data-ttu-id="f0eb1-131">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f0eb1-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f0eb1-132">-確認</span><span class="sxs-lookup"><span data-stu-id="f0eb1-132">-Confirm</span></span>
<span data-ttu-id="f0eb1-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f0eb1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0eb1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0eb1-134">-WhatIf</span></span>
<span data-ttu-id="f0eb1-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f0eb1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0eb1-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f0eb1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0eb1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0eb1-137">CommonParameters</span></span>
<span data-ttu-id="f0eb1-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f0eb1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0eb1-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f0eb1-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0eb1-140">輸入</span><span class="sxs-lookup"><span data-stu-id="f0eb1-140">INPUTS</span></span>

### <span data-ttu-id="f0eb1-141">Microsoft.Azure.PowerShell.Cmdlets.Databuvs.models.IDatab一sIdentity</span><span class="sxs-lookup"><span data-stu-id="f0eb1-141">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="f0eb1-142">輸出</span><span class="sxs-lookup"><span data-stu-id="f0eb1-142">OUTPUTS</span></span>

### <span data-ttu-id="f0eb1-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f0eb1-143">System.Boolean</span></span>

## <span data-ttu-id="f0eb1-144">筆記</span><span class="sxs-lookup"><span data-stu-id="f0eb1-144">NOTES</span></span>

<span data-ttu-id="f0eb1-145">別名</span><span class="sxs-lookup"><span data-stu-id="f0eb1-145">ALIASES</span></span>

<span data-ttu-id="f0eb1-146">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="f0eb1-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f0eb1-147">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="f0eb1-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f0eb1-148">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="f0eb1-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f0eb1-149">INPUTOBJECT： <IDatabricksIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="f0eb1-149">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f0eb1-150">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="f0eb1-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f0eb1-151">`[PeeringName <String>]`：工作區 vNet 對等的名稱。</span><span class="sxs-lookup"><span data-stu-id="f0eb1-151">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="f0eb1-152">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f0eb1-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f0eb1-153">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="f0eb1-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="f0eb1-154">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f0eb1-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="f0eb1-155">`[WorkspaceName <String>]`：工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="f0eb1-155">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="f0eb1-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="f0eb1-156">RELATED LINKS</span></span>

