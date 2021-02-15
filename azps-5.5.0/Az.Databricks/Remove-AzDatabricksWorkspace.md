---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/remove-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksWorkspace.md
ms.openlocfilehash: 629b12a7db506b0a96633396b97e0df3d66e1760
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100129422"
---
# <span data-ttu-id="b32bc-101">Remove-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="b32bc-101">Remove-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="b32bc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b32bc-102">SYNOPSIS</span></span>
<span data-ttu-id="b32bc-103">刪除工作區。</span><span class="sxs-lookup"><span data-stu-id="b32bc-103">Deletes the workspace.</span></span>

## <span data-ttu-id="b32bc-104">句法</span><span class="sxs-lookup"><span data-stu-id="b32bc-104">SYNTAX</span></span>

### <span data-ttu-id="b32bc-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="b32bc-105">Delete (Default)</span></span>
```
Remove-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b32bc-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b32bc-106">DeleteViaIdentity</span></span>
```
Remove-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b32bc-107">說明</span><span class="sxs-lookup"><span data-stu-id="b32bc-107">DESCRIPTION</span></span>
<span data-ttu-id="b32bc-108">刪除工作區。</span><span class="sxs-lookup"><span data-stu-id="b32bc-108">Deletes the workspace.</span></span>

## <span data-ttu-id="b32bc-109">示例</span><span class="sxs-lookup"><span data-stu-id="b32bc-109">EXAMPLES</span></span>

### <span data-ttu-id="b32bc-110">範例1：移除 Databricks 工作區</span><span class="sxs-lookup"><span data-stu-id="b32bc-110">Example 1: Remove a Databricks workspace</span></span>
```powershell
PS C:\> Remove-AzDatabricksWorkspace -ResourceGroupName testgroup -Name databricks-test
```

<span data-ttu-id="b32bc-111">這個命令會從資源群組中移除 Databricks 工作區。</span><span class="sxs-lookup"><span data-stu-id="b32bc-111">This command removes a Databricks workspace from a resource group.</span></span>

### <span data-ttu-id="b32bc-112">範例2：依物件移除 Databricks 工作區</span><span class="sxs-lookup"><span data-stu-id="b32bc-112">Example 2: Remove a Databricks workspace by object</span></span>
```powershell
PS C:\> $dbr = Get-AzDatabricksWorkspace -ResourceGroupName testgroup -Name databricks-test02
PS C:\> Remove-AzDatabricksWorkspace -InputObject $dbr
```

<span data-ttu-id="b32bc-113">這個命令會從資源群組中移除 Databricks 工作區。</span><span class="sxs-lookup"><span data-stu-id="b32bc-113">This command removes a Databricks workspace from a resource group.</span></span>

## <span data-ttu-id="b32bc-114">參數</span><span class="sxs-lookup"><span data-stu-id="b32bc-114">PARAMETERS</span></span>

### <span data-ttu-id="b32bc-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b32bc-115">-AsJob</span></span>
<span data-ttu-id="b32bc-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="b32bc-116">Run the command as a job</span></span>

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

### <span data-ttu-id="b32bc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b32bc-117">-DefaultProfile</span></span>
<span data-ttu-id="b32bc-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b32bc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b32bc-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b32bc-119">-InputObject</span></span>
<span data-ttu-id="b32bc-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b32bc-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b32bc-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="b32bc-121">-Name</span></span>
<span data-ttu-id="b32bc-122">工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="b32bc-122">The name of the workspace.</span></span>

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

### <span data-ttu-id="b32bc-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b32bc-123">-NoWait</span></span>
<span data-ttu-id="b32bc-124">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="b32bc-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b32bc-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b32bc-125">-PassThru</span></span>
<span data-ttu-id="b32bc-126">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="b32bc-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b32bc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b32bc-127">-ResourceGroupName</span></span>
<span data-ttu-id="b32bc-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b32bc-128">The name of the resource group.</span></span>
<span data-ttu-id="b32bc-129">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="b32bc-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b32bc-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b32bc-130">-SubscriptionId</span></span>
<span data-ttu-id="b32bc-131">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="b32bc-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b32bc-132">-確認</span><span class="sxs-lookup"><span data-stu-id="b32bc-132">-Confirm</span></span>
<span data-ttu-id="b32bc-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b32bc-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b32bc-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b32bc-134">-WhatIf</span></span>
<span data-ttu-id="b32bc-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b32bc-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b32bc-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b32bc-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b32bc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b32bc-137">CommonParameters</span></span>
<span data-ttu-id="b32bc-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b32bc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b32bc-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b32bc-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b32bc-140">輸入</span><span class="sxs-lookup"><span data-stu-id="b32bc-140">INPUTS</span></span>

### <span data-ttu-id="b32bc-141">IDatabricksIdentity （Databricks）的</span><span class="sxs-lookup"><span data-stu-id="b32bc-141">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="b32bc-142">輸出</span><span class="sxs-lookup"><span data-stu-id="b32bc-142">OUTPUTS</span></span>

### <span data-ttu-id="b32bc-143">System.object</span><span class="sxs-lookup"><span data-stu-id="b32bc-143">System.Boolean</span></span>

## <span data-ttu-id="b32bc-144">筆記</span><span class="sxs-lookup"><span data-stu-id="b32bc-144">NOTES</span></span>

<span data-ttu-id="b32bc-145">別名</span><span class="sxs-lookup"><span data-stu-id="b32bc-145">ALIASES</span></span>

<span data-ttu-id="b32bc-146">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="b32bc-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b32bc-147">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="b32bc-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b32bc-148">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="b32bc-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b32bc-149">INPUTOBJECT <IDatabricksIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="b32bc-149">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b32bc-150">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="b32bc-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b32bc-151">`[PeeringName <String>]`： Workspace vNet 對等的名稱。</span><span class="sxs-lookup"><span data-stu-id="b32bc-151">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="b32bc-152">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b32bc-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b32bc-153">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="b32bc-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="b32bc-154">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b32bc-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b32bc-155">`[WorkspaceName <String>]`：工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="b32bc-155">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="b32bc-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="b32bc-156">RELATED LINKS</span></span>

