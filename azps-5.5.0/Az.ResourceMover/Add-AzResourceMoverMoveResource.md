---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/add-azresourcemovermoveresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Add-AzResourceMoverMoveResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Add-AzResourceMoverMoveResource.md
ms.openlocfilehash: bafba030de13cdee2c4b7026f498c07cf4231fdd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142643"
---
# <span data-ttu-id="ac524-101">Add-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="ac524-101">Add-AzResourceMoverMoveResource</span></span>

## <span data-ttu-id="ac524-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ac524-102">SYNOPSIS</span></span>
<span data-ttu-id="ac524-103">在移動集合中建立或更新移動資源。</span><span class="sxs-lookup"><span data-stu-id="ac524-103">Creates or updates a Move Resource in the move collection.</span></span>

## <span data-ttu-id="ac524-104">句法</span><span class="sxs-lookup"><span data-stu-id="ac524-104">SYNTAX</span></span>

```
Add-AzResourceMoverMoveResource -MoveCollectionName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DependsOnOverride <IMoveResourceDependencyOverride[]>]
 [-ExistingTargetId <String>] [-ResourceSettingResourceType <String>]
 [-ResourceSettingTargetResourceName <String>] [-SourceId <String>]
 [-SourceResourceSettingResourceType <String>] [-SourceResourceSettingTargetResourceName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ac524-105">說明</span><span class="sxs-lookup"><span data-stu-id="ac524-105">DESCRIPTION</span></span>
<span data-ttu-id="ac524-106">在移動集合中建立或更新移動資源。</span><span class="sxs-lookup"><span data-stu-id="ac524-106">Creates or updates a Move Resource in the move collection.</span></span>

## <span data-ttu-id="ac524-107">示例</span><span class="sxs-lookup"><span data-stu-id="ac524-107">EXAMPLES</span></span>

### <span data-ttu-id="ac524-108">範例1：將資源新增至移動收藏。</span><span class="sxs-lookup"><span data-stu-id="ac524-108">Example 1: Adding a resource to the move collection.</span></span>
```powershell
PS C:\> Add-AzResourceMoverMoveResource -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName "PS-centralus-westcentralus-demoRM" -SourceId "/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Compute/virtualMachines/PSDemoVM" -Name PSDemoVM -ResourceSettingResourceType "Microsoft.Compute/virtualMachines" -ResourceSettingTargetResourceName PSDemoVM

Output:

Code                                    :
DependsOn                               : {}
DependsOnOverride                       : {}
Detail                                  :
ExistingTargetId                        :
Id                                      : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migr
                                          ate/MoveCollections/PS-centralus-westcentralus-demoRM/MoveResources/PSDemoVM
Message                                 :
MoveStatusCode                          : DependencyComputationPending
MoveStatusDetail                        : {}
MoveStatusJobName                       :
MoveStatusJobProgress                   :
MoveStatusMessage                       : The dependency computation is not completed for resource - /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resou
                                          rceGroups/PSDemoRM/providers/Microsoft.Compute/virtualMachines/PSDemoVM.
                                              Possible Causes: Dependency computation is pending for resource.
                                              Recommended Action: Validate dependencies to compute the dependencies.

MoveStatusMoveState                     : PreparePending
MoveStatusTarget                        :
MoveStatusTargetId                      :
Name                                    : PSDemoVM
ProvisioningState                       : Succeeded
ResourceSettingResourceType             : Microsoft.Compute/virtualMachines
ResourceSettingTargetResourceName       : PSDemoVM
SourceId                                : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Compute/virtualMachi
                                          nes/PSDemoVM
SourceResourceSettingResourceType       : Microsoft.Compute/virtualMachines
SourceResourceSettingTargetResourceName : PSDemoVM
Target                                  :
TargetId                                :
Type          

```

<span data-ttu-id="ac524-109">在指定的訂閱內將資源新增至移動集合。</span><span class="sxs-lookup"><span data-stu-id="ac524-109">Adding a resource to the move collection within the specified subscription.</span></span>

## <span data-ttu-id="ac524-110">參數</span><span class="sxs-lookup"><span data-stu-id="ac524-110">PARAMETERS</span></span>

### <span data-ttu-id="ac524-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ac524-111">-AsJob</span></span>
<span data-ttu-id="ac524-112">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="ac524-112">Run the command as a job</span></span>

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

### <span data-ttu-id="ac524-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac524-113">-DefaultProfile</span></span>
<span data-ttu-id="ac524-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ac524-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac524-115">-DependsOnOverride</span><span class="sxs-lookup"><span data-stu-id="ac524-115">-DependsOnOverride</span></span>
<span data-ttu-id="ac524-116">取得或設定 [移動資源相依性覆寫]。</span><span class="sxs-lookup"><span data-stu-id="ac524-116">Gets or sets the move resource dependencies overrides.</span></span>
<span data-ttu-id="ac524-117">若要建立，請參閱 DEPENDSONOVERRIDE 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="ac524-117">To construct, see NOTES section for DEPENDSONOVERRIDE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveResourceDependencyOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac524-118">-ExistingTargetId</span><span class="sxs-lookup"><span data-stu-id="ac524-118">-ExistingTargetId</span></span>
<span data-ttu-id="ac524-119">取得或設定資源的現有目標扶手 Id。</span><span class="sxs-lookup"><span data-stu-id="ac524-119">Gets or sets the existing target ARM Id of the resource.</span></span>

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

### <span data-ttu-id="ac524-120">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="ac524-120">-MoveCollectionName</span></span>
<span data-ttu-id="ac524-121">[移動集合名稱]。</span><span class="sxs-lookup"><span data-stu-id="ac524-121">The Move Collection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac524-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="ac524-122">-Name</span></span>
<span data-ttu-id="ac524-123">移動資源名稱。</span><span class="sxs-lookup"><span data-stu-id="ac524-123">The Move Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MoveResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac524-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ac524-124">-NoWait</span></span>
<span data-ttu-id="ac524-125">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="ac524-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ac524-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac524-126">-ResourceGroupName</span></span>
<span data-ttu-id="ac524-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ac524-127">The Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac524-128">-ResourceSettingResourceType</span><span class="sxs-lookup"><span data-stu-id="ac524-128">-ResourceSettingResourceType</span></span>
<span data-ttu-id="ac524-129">資源類型。</span><span class="sxs-lookup"><span data-stu-id="ac524-129">The resource type.</span></span>
<span data-ttu-id="ac524-130">例如，此值可以是 Microsoft. Compute/virtualMachines。</span><span class="sxs-lookup"><span data-stu-id="ac524-130">For example, the value can be Microsoft.Compute/virtualMachines.</span></span>

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

### <span data-ttu-id="ac524-131">-ResourceSettingTargetResourceName</span><span class="sxs-lookup"><span data-stu-id="ac524-131">-ResourceSettingTargetResourceName</span></span>
<span data-ttu-id="ac524-132">取得或設定目標資源名稱。</span><span class="sxs-lookup"><span data-stu-id="ac524-132">Gets or sets the target Resource name.</span></span>

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

### <span data-ttu-id="ac524-133">-SourceId</span><span class="sxs-lookup"><span data-stu-id="ac524-133">-SourceId</span></span>
<span data-ttu-id="ac524-134">取得或設定資源的來源扶手 Id。</span><span class="sxs-lookup"><span data-stu-id="ac524-134">Gets or sets the Source ARM Id of the resource.</span></span>

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

### <span data-ttu-id="ac524-135">-SourceResourceSettingResourceType</span><span class="sxs-lookup"><span data-stu-id="ac524-135">-SourceResourceSettingResourceType</span></span>
<span data-ttu-id="ac524-136">資源類型。</span><span class="sxs-lookup"><span data-stu-id="ac524-136">The resource type.</span></span>
<span data-ttu-id="ac524-137">例如，此值可以是 Microsoft. Compute/virtualMachines。</span><span class="sxs-lookup"><span data-stu-id="ac524-137">For example, the value can be Microsoft.Compute/virtualMachines.</span></span>

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

### <span data-ttu-id="ac524-138">-SourceResourceSettingTargetResourceName</span><span class="sxs-lookup"><span data-stu-id="ac524-138">-SourceResourceSettingTargetResourceName</span></span>
<span data-ttu-id="ac524-139">取得或設定目標資源名稱。</span><span class="sxs-lookup"><span data-stu-id="ac524-139">Gets or sets the target Resource name.</span></span>

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

### <span data-ttu-id="ac524-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ac524-140">-SubscriptionId</span></span>
<span data-ttu-id="ac524-141">訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="ac524-141">The Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac524-142">-確認</span><span class="sxs-lookup"><span data-stu-id="ac524-142">-Confirm</span></span>
<span data-ttu-id="ac524-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ac524-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac524-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac524-144">-WhatIf</span></span>
<span data-ttu-id="ac524-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ac524-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac524-146">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ac524-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac524-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac524-147">CommonParameters</span></span>
<span data-ttu-id="ac524-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ac524-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac524-149">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ac524-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac524-150">輸入</span><span class="sxs-lookup"><span data-stu-id="ac524-150">INPUTS</span></span>

## <span data-ttu-id="ac524-151">輸出</span><span class="sxs-lookup"><span data-stu-id="ac524-151">OUTPUTS</span></span>

### <span data-ttu-id="ac524-152">IMoveResource （ResourceMover）。 Api20191001Preview。</span><span class="sxs-lookup"><span data-stu-id="ac524-152">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveResource</span></span>

## <span data-ttu-id="ac524-153">筆記</span><span class="sxs-lookup"><span data-stu-id="ac524-153">NOTES</span></span>

<span data-ttu-id="ac524-154">別名</span><span class="sxs-lookup"><span data-stu-id="ac524-154">ALIASES</span></span>

<span data-ttu-id="ac524-155">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="ac524-155">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ac524-156">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="ac524-156">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ac524-157">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="ac524-157">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ac524-158">DEPENDSONOVERRIDE <IMoveResourceDependencyOverride [] >：取得或設定移動資源相依性覆寫。</span><span class="sxs-lookup"><span data-stu-id="ac524-158">DEPENDSONOVERRIDE <IMoveResourceDependencyOverride[]>: Gets or sets the move resource dependencies overrides.</span></span>
  - <span data-ttu-id="ac524-159">`[Id <String>]`：取得或設定相依資源的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="ac524-159">`[Id <String>]`: Gets or sets the ARM ID of the dependent resource.</span></span>
  - <span data-ttu-id="ac524-160">`[TargetId <String>]`：取得或設定相依資源之 MoveResource 或資源臂 ID 的資源扶手 id。</span><span class="sxs-lookup"><span data-stu-id="ac524-160">`[TargetId <String>]`: Gets or sets the resource ARM id of either the MoveResource or the resource ARM ID of         the dependent resource.</span></span>

## <span data-ttu-id="ac524-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="ac524-161">RELATED LINKS</span></span>

