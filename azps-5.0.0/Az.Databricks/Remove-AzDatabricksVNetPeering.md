---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/remove-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksVNetPeering.md
ms.openlocfilehash: 1c75bb4e8f94fadfb3b56c2fbb44889c5eaff458
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284841"
---
# <span data-ttu-id="ec29c-101">Remove-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="ec29c-101">Remove-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="ec29c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ec29c-102">SYNOPSIS</span></span>
<span data-ttu-id="ec29c-103">刪除工作區 vNetPeering。</span><span class="sxs-lookup"><span data-stu-id="ec29c-103">Deletes the workspace vNetPeering.</span></span>

## <span data-ttu-id="ec29c-104">句法</span><span class="sxs-lookup"><span data-stu-id="ec29c-104">SYNTAX</span></span>

### <span data-ttu-id="ec29c-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="ec29c-105">Delete (Default)</span></span>
```
Remove-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="ec29c-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ec29c-106">DeleteViaIdentity</span></span>
```
Remove-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ec29c-107">說明</span><span class="sxs-lookup"><span data-stu-id="ec29c-107">DESCRIPTION</span></span>
<span data-ttu-id="ec29c-108">刪除工作區 vNetPeering。</span><span class="sxs-lookup"><span data-stu-id="ec29c-108">Deletes the workspace vNetPeering.</span></span>

## <span data-ttu-id="ec29c-109">示例</span><span class="sxs-lookup"><span data-stu-id="ec29c-109">EXAMPLES</span></span>

### <span data-ttu-id="ec29c-110">範例1：按照名稱移除 databricks 的 vnet 對等操作</span><span class="sxs-lookup"><span data-stu-id="ec29c-110">Example 1: Remove a vnet peering of databricks by name</span></span>
```powershell
PS C:\> Remove-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01

```

<span data-ttu-id="ec29c-111">這個命令會依名稱移除 databricks 的 vnet 對等</span><span class="sxs-lookup"><span data-stu-id="ec29c-111">This command removes a vnet peering of databricks by name</span></span>

### <span data-ttu-id="ec29c-112">範例2：移除依物件 databricks 的 vnet 對等對等</span><span class="sxs-lookup"><span data-stu-id="ec29c-112">Example 2: Remove a vnet peering of databricks by object</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -ResourceGroupName lucas-manual-test -WorkspaceName databricks-test01 -PeeringName MyPeering-test01 | Remove-AzDatabricksVNetPeering

```

<span data-ttu-id="ec29c-113">這個命令會移除 databricks by 物件的 vnet 對等對等</span><span class="sxs-lookup"><span data-stu-id="ec29c-113">This command removes a vnet peering of databricks by object</span></span>

## <span data-ttu-id="ec29c-114">參數</span><span class="sxs-lookup"><span data-stu-id="ec29c-114">PARAMETERS</span></span>

### <span data-ttu-id="ec29c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ec29c-115">-AsJob</span></span>
<span data-ttu-id="ec29c-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="ec29c-116">Run the command as a job</span></span>

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

### <span data-ttu-id="ec29c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec29c-117">-DefaultProfile</span></span>
<span data-ttu-id="ec29c-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ec29c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec29c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec29c-119">-InputObject</span></span>
<span data-ttu-id="ec29c-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="ec29c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ec29c-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="ec29c-121">-Name</span></span>
<span data-ttu-id="ec29c-122">工作區 vNet 對等的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec29c-122">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="ec29c-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ec29c-123">-NoWait</span></span>
<span data-ttu-id="ec29c-124">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="ec29c-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ec29c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ec29c-125">-PassThru</span></span>
<span data-ttu-id="ec29c-126">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="ec29c-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ec29c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec29c-127">-ResourceGroupName</span></span>
<span data-ttu-id="ec29c-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec29c-128">The name of the resource group.</span></span>
<span data-ttu-id="ec29c-129">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="ec29c-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ec29c-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ec29c-130">-SubscriptionId</span></span>
<span data-ttu-id="ec29c-131">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="ec29c-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ec29c-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ec29c-132">-WorkspaceName</span></span>
<span data-ttu-id="ec29c-133">工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec29c-133">The name of the workspace.</span></span>

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

### <span data-ttu-id="ec29c-134">-確認</span><span class="sxs-lookup"><span data-stu-id="ec29c-134">-Confirm</span></span>
<span data-ttu-id="ec29c-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ec29c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec29c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec29c-136">-WhatIf</span></span>
<span data-ttu-id="ec29c-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ec29c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec29c-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ec29c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec29c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec29c-139">CommonParameters</span></span>
<span data-ttu-id="ec29c-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ec29c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec29c-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ec29c-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec29c-142">輸入</span><span class="sxs-lookup"><span data-stu-id="ec29c-142">INPUTS</span></span>

### <span data-ttu-id="ec29c-143">IDatabricksIdentity （Databricks）的</span><span class="sxs-lookup"><span data-stu-id="ec29c-143">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="ec29c-144">輸出</span><span class="sxs-lookup"><span data-stu-id="ec29c-144">OUTPUTS</span></span>

### <span data-ttu-id="ec29c-145">System.object</span><span class="sxs-lookup"><span data-stu-id="ec29c-145">System.Boolean</span></span>

## <span data-ttu-id="ec29c-146">筆記</span><span class="sxs-lookup"><span data-stu-id="ec29c-146">NOTES</span></span>

<span data-ttu-id="ec29c-147">別名</span><span class="sxs-lookup"><span data-stu-id="ec29c-147">ALIASES</span></span>

<span data-ttu-id="ec29c-148">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="ec29c-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ec29c-149">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="ec29c-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ec29c-150">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="ec29c-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ec29c-151">INPUTOBJECT <IDatabricksIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="ec29c-151">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ec29c-152">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="ec29c-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ec29c-153">`[PeeringName <String>]`： Workspace vNet 對等的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec29c-153">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="ec29c-154">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec29c-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ec29c-155">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="ec29c-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="ec29c-156">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ec29c-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="ec29c-157">`[WorkspaceName <String>]`：工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec29c-157">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="ec29c-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="ec29c-158">RELATED LINKS</span></span>

