---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/remove-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksVNetPeering.md
ms.openlocfilehash: 1c75bb4e8f94fadfb3b56c2fbb44889c5eaff458
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100129426"
---
# <span data-ttu-id="bedc5-101">Remove-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="bedc5-101">Remove-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="bedc5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bedc5-102">SYNOPSIS</span></span>
<span data-ttu-id="bedc5-103">刪除工作區 vNetPeering。</span><span class="sxs-lookup"><span data-stu-id="bedc5-103">Deletes the workspace vNetPeering.</span></span>

## <span data-ttu-id="bedc5-104">句法</span><span class="sxs-lookup"><span data-stu-id="bedc5-104">SYNTAX</span></span>

### <span data-ttu-id="bedc5-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="bedc5-105">Delete (Default)</span></span>
```
Remove-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="bedc5-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bedc5-106">DeleteViaIdentity</span></span>
```
Remove-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bedc5-107">說明</span><span class="sxs-lookup"><span data-stu-id="bedc5-107">DESCRIPTION</span></span>
<span data-ttu-id="bedc5-108">刪除工作區 vNetPeering。</span><span class="sxs-lookup"><span data-stu-id="bedc5-108">Deletes the workspace vNetPeering.</span></span>

## <span data-ttu-id="bedc5-109">示例</span><span class="sxs-lookup"><span data-stu-id="bedc5-109">EXAMPLES</span></span>

### <span data-ttu-id="bedc5-110">範例1：按照名稱移除 databricks 的 vnet 對等操作</span><span class="sxs-lookup"><span data-stu-id="bedc5-110">Example 1: Remove a vnet peering of databricks by name</span></span>
```powershell
PS C:\> Remove-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01

```

<span data-ttu-id="bedc5-111">這個命令會依名稱移除 databricks 的 vnet 對等</span><span class="sxs-lookup"><span data-stu-id="bedc5-111">This command removes a vnet peering of databricks by name</span></span>

### <span data-ttu-id="bedc5-112">範例2：移除依物件 databricks 的 vnet 對等對等</span><span class="sxs-lookup"><span data-stu-id="bedc5-112">Example 2: Remove a vnet peering of databricks by object</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -ResourceGroupName lucas-manual-test -WorkspaceName databricks-test01 -PeeringName MyPeering-test01 | Remove-AzDatabricksVNetPeering

```

<span data-ttu-id="bedc5-113">這個命令會移除 databricks by 物件的 vnet 對等對等</span><span class="sxs-lookup"><span data-stu-id="bedc5-113">This command removes a vnet peering of databricks by object</span></span>

## <span data-ttu-id="bedc5-114">參數</span><span class="sxs-lookup"><span data-stu-id="bedc5-114">PARAMETERS</span></span>

### <span data-ttu-id="bedc5-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bedc5-115">-AsJob</span></span>
<span data-ttu-id="bedc5-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="bedc5-116">Run the command as a job</span></span>

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

### <span data-ttu-id="bedc5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bedc5-117">-DefaultProfile</span></span>
<span data-ttu-id="bedc5-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bedc5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bedc5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bedc5-119">-InputObject</span></span>
<span data-ttu-id="bedc5-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="bedc5-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bedc5-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="bedc5-121">-Name</span></span>
<span data-ttu-id="bedc5-122">工作區 vNet 對等的名稱。</span><span class="sxs-lookup"><span data-stu-id="bedc5-122">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="bedc5-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="bedc5-123">-NoWait</span></span>
<span data-ttu-id="bedc5-124">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="bedc5-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="bedc5-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bedc5-125">-PassThru</span></span>
<span data-ttu-id="bedc5-126">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="bedc5-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="bedc5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bedc5-127">-ResourceGroupName</span></span>
<span data-ttu-id="bedc5-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bedc5-128">The name of the resource group.</span></span>
<span data-ttu-id="bedc5-129">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="bedc5-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="bedc5-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bedc5-130">-SubscriptionId</span></span>
<span data-ttu-id="bedc5-131">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="bedc5-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="bedc5-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bedc5-132">-WorkspaceName</span></span>
<span data-ttu-id="bedc5-133">工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="bedc5-133">The name of the workspace.</span></span>

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

### <span data-ttu-id="bedc5-134">-確認</span><span class="sxs-lookup"><span data-stu-id="bedc5-134">-Confirm</span></span>
<span data-ttu-id="bedc5-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bedc5-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bedc5-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bedc5-136">-WhatIf</span></span>
<span data-ttu-id="bedc5-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bedc5-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bedc5-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bedc5-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bedc5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bedc5-139">CommonParameters</span></span>
<span data-ttu-id="bedc5-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bedc5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bedc5-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="bedc5-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bedc5-142">輸入</span><span class="sxs-lookup"><span data-stu-id="bedc5-142">INPUTS</span></span>

### <span data-ttu-id="bedc5-143">IDatabricksIdentity （Databricks）的</span><span class="sxs-lookup"><span data-stu-id="bedc5-143">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="bedc5-144">輸出</span><span class="sxs-lookup"><span data-stu-id="bedc5-144">OUTPUTS</span></span>

### <span data-ttu-id="bedc5-145">System.object</span><span class="sxs-lookup"><span data-stu-id="bedc5-145">System.Boolean</span></span>

## <span data-ttu-id="bedc5-146">筆記</span><span class="sxs-lookup"><span data-stu-id="bedc5-146">NOTES</span></span>

<span data-ttu-id="bedc5-147">別名</span><span class="sxs-lookup"><span data-stu-id="bedc5-147">ALIASES</span></span>

<span data-ttu-id="bedc5-148">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="bedc5-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bedc5-149">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="bedc5-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bedc5-150">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="bedc5-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bedc5-151">INPUTOBJECT <IDatabricksIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="bedc5-151">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bedc5-152">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="bedc5-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bedc5-153">`[PeeringName <String>]`： Workspace vNet 對等的名稱。</span><span class="sxs-lookup"><span data-stu-id="bedc5-153">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="bedc5-154">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bedc5-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="bedc5-155">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="bedc5-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="bedc5-156">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="bedc5-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="bedc5-157">`[WorkspaceName <String>]`：工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="bedc5-157">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="bedc5-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="bedc5-158">RELATED LINKS</span></span>

