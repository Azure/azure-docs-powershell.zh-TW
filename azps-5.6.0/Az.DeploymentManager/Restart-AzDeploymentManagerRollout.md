---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/restart-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Restart-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Restart-AzDeploymentManagerRollout.md
ms.openlocfilehash: d11a19ed5189220c8f6c327c9483e0e11e671ed8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909081"
---
# <span data-ttu-id="76c21-101">Restart-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="76c21-101">Restart-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="76c21-102">簡介</span><span class="sxs-lookup"><span data-stu-id="76c21-102">SYNOPSIS</span></span>
<span data-ttu-id="76c21-103">重新開機失敗推出。</span><span class="sxs-lookup"><span data-stu-id="76c21-103">Restarts a failed rollout.</span></span>

## <span data-ttu-id="76c21-104">語法</span><span class="sxs-lookup"><span data-stu-id="76c21-104">SYNTAX</span></span>

### <span data-ttu-id="76c21-105">互動式 (預設) </span><span class="sxs-lookup"><span data-stu-id="76c21-105">Interactive (Default)</span></span>
```
Restart-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76c21-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="76c21-106">ResourceId</span></span>
```
Restart-AzDeploymentManagerRollout [-ResourceId] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76c21-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="76c21-107">InputObject</span></span>
```
Restart-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76c21-108">描述</span><span class="sxs-lookup"><span data-stu-id="76c21-108">DESCRIPTION</span></span>
<span data-ttu-id="76c21-109">**Restart-AzDeploymentManagerRollout** Cmdlet 會重新開機失敗推出，並會返回代表該推出的物件，並包含推出進度的所有詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="76c21-109">The **Restart-AzDeploymentManagerRollout** cmdlet restarts a failed rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="76c21-110">根據部署名稱和資源組名來指定部署。</span><span class="sxs-lookup"><span data-stu-id="76c21-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="76c21-111">或者，您也可以提供部署物件或 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="76c21-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>
<span data-ttu-id="76c21-112">選擇性參數 SkipSucceed 可讓您略過前一次推出執行的所有成功步驟。</span><span class="sxs-lookup"><span data-stu-id="76c21-112">Optional parameter SkipSucceeded allows you to skip all the succeeded steps in the previous run of the rollout.</span></span>

## <span data-ttu-id="76c21-113">例子</span><span class="sxs-lookup"><span data-stu-id="76c21-113">EXAMPLES</span></span>

### <span data-ttu-id="76c21-114">範例 1</span><span class="sxs-lookup"><span data-stu-id="76c21-114">Example 1</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="76c21-115">此命令會重新開機 ContosoResourceGroup 中名為 ContosoRollout 的推出。</span><span class="sxs-lookup"><span data-stu-id="76c21-115">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="76c21-116">SkipSucceed 標號表示應略過所有已成功執行的步驟，並且應該從上次失敗的地方繼續執行這項推出。</span><span class="sxs-lookup"><span data-stu-id="76c21-116">The SkipSucceeded flag indicates that all the steps that already ran successfully should be skipped and the rollout should continue execution from where it last failed.</span></span>

### <span data-ttu-id="76c21-117">範例 2：使用資源識別碼重新開機推出</span><span class="sxs-lookup"><span data-stu-id="76c21-117">Example 2: Restart a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="76c21-118">此命令會重新開機 ContosoResourceGroup 中名為 ContosoRollout 的推出。</span><span class="sxs-lookup"><span data-stu-id="76c21-118">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="76c21-119">範例 3：使用推出物件重新開機推出。</span><span class="sxs-lookup"><span data-stu-id="76c21-119">Example 3: Restart a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="76c21-120">此命令會重新開機推出，其名稱和 ResourceGroup 分別符合 $rolloutObject 的名稱和資源組名屬性。</span><span class="sxs-lookup"><span data-stu-id="76c21-120">This command restarts a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="76c21-121">參數</span><span class="sxs-lookup"><span data-stu-id="76c21-121">PARAMETERS</span></span>

### <span data-ttu-id="76c21-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76c21-122">-DefaultProfile</span></span>
<span data-ttu-id="76c21-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="76c21-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76c21-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76c21-124">-InputObject</span></span>
<span data-ttu-id="76c21-125">要移除的資源。</span><span class="sxs-lookup"><span data-stu-id="76c21-125">The resource to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76c21-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="76c21-126">-Name</span></span>
<span data-ttu-id="76c21-127">推出名稱。</span><span class="sxs-lookup"><span data-stu-id="76c21-127">The name of the rollout.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76c21-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76c21-128">-ResourceGroupName</span></span>
<span data-ttu-id="76c21-129">資源群組。</span><span class="sxs-lookup"><span data-stu-id="76c21-129">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76c21-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76c21-130">-ResourceId</span></span>
<span data-ttu-id="76c21-131">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="76c21-131">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76c21-132">-SkipSucceed</span><span class="sxs-lookup"><span data-stu-id="76c21-132">-SkipSucceeded</span></span>
<span data-ttu-id="76c21-133">略過在前一次推出中成功執行的步驟。</span><span class="sxs-lookup"><span data-stu-id="76c21-133">Skip steps that succeeded in the previous run of the rollout.</span></span>

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

### <span data-ttu-id="76c21-134">-確認</span><span class="sxs-lookup"><span data-stu-id="76c21-134">-Confirm</span></span>
<span data-ttu-id="76c21-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="76c21-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76c21-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76c21-136">-WhatIf</span></span>
<span data-ttu-id="76c21-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="76c21-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76c21-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="76c21-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76c21-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76c21-139">CommonParameters</span></span>
<span data-ttu-id="76c21-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="76c21-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76c21-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76c21-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76c21-142">輸入</span><span class="sxs-lookup"><span data-stu-id="76c21-142">INPUTS</span></span>

### <span data-ttu-id="76c21-143">System.String</span><span class="sxs-lookup"><span data-stu-id="76c21-143">System.String</span></span>

### <span data-ttu-id="76c21-144">Microsoft.Azure.Commands.DeploymentManager.models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="76c21-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="76c21-145">輸出</span><span class="sxs-lookup"><span data-stu-id="76c21-145">OUTPUTS</span></span>

### <span data-ttu-id="76c21-146">Microsoft.Azure.Commands.DeploymentManager.models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="76c21-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="76c21-147">筆記</span><span class="sxs-lookup"><span data-stu-id="76c21-147">NOTES</span></span>

## <span data-ttu-id="76c21-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="76c21-148">RELATED LINKS</span></span>
