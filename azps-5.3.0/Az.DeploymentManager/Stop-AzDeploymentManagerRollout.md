---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/stop-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Stop-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Stop-AzDeploymentManagerRollout.md
ms.openlocfilehash: cd59cd39fb2834bed2162a257905fea643c0a767
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98289252"
---
# <span data-ttu-id="7273a-101">Stop-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="7273a-101">Stop-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="7273a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7273a-102">SYNOPSIS</span></span>
<span data-ttu-id="7273a-103">停止推出。</span><span class="sxs-lookup"><span data-stu-id="7273a-103">Stops the rollout.</span></span>

## <span data-ttu-id="7273a-104">句法</span><span class="sxs-lookup"><span data-stu-id="7273a-104">SYNTAX</span></span>

### <span data-ttu-id="7273a-105">互動式 (預設) </span><span class="sxs-lookup"><span data-stu-id="7273a-105">Interactive (Default)</span></span>
```
Stop-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7273a-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7273a-106">ResourceId</span></span>
```
Stop-AzDeploymentManagerRollout [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7273a-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="7273a-107">InputObject</span></span>
```
Stop-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7273a-108">說明</span><span class="sxs-lookup"><span data-stu-id="7273a-108">DESCRIPTION</span></span>
<span data-ttu-id="7273a-109">**Stop-AzDeploymentManagerRollout** Cmdlet 會停止進行中的推出，並傳回代表推出的目前狀態的物件。</span><span class="sxs-lookup"><span data-stu-id="7273a-109">The **Stop-AzDeploymentManagerRollout** cmdlet stops a rollout in progress and returns an object that represents the current state of the rollout.</span></span>
<span data-ttu-id="7273a-110">依其名稱和資源群組名稱來指定推出。</span><span class="sxs-lookup"><span data-stu-id="7273a-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="7273a-111">或者，您也可以提供推出物件或 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="7273a-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="7273a-112">請注意，一旦停止推出，就無法繼續或重新開機。</span><span class="sxs-lookup"><span data-stu-id="7273a-112">Note that once a rollout is stopped, it cannot be resumed or restarted.</span></span> <span data-ttu-id="7273a-113">您只能建立新的推出。</span><span class="sxs-lookup"><span data-stu-id="7273a-113">You can only create a new rollout.</span></span>

## <span data-ttu-id="7273a-114">示例</span><span class="sxs-lookup"><span data-stu-id="7273a-114">EXAMPLES</span></span>

### <span data-ttu-id="7273a-115">範例1</span><span class="sxs-lookup"><span data-stu-id="7273a-115">Example 1</span></span>
```powershell
PS C:\> Stop-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="7273a-116">這個命令會在 ContosoResourceGroup 中停止名為 ContosoRollout 的推出。</span><span class="sxs-lookup"><span data-stu-id="7273a-116">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="7273a-117">範例2：使用資源識別碼停止推出</span><span class="sxs-lookup"><span data-stu-id="7273a-117">Example 2: Stop a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="7273a-118">這個命令會在 ContosoResourceGroup 中停止名為 ContosoRollout 的推出。</span><span class="sxs-lookup"><span data-stu-id="7273a-118">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="7273a-119">範例3：使用 [推出] 物件停止推出。</span><span class="sxs-lookup"><span data-stu-id="7273a-119">Example 3: Stop a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="7273a-120">這個命令會停止其 name 和 ResourceGroup 會分別與 $rolloutObject 的 Name 和 ResourceGroupName 屬性相符的推出。</span><span class="sxs-lookup"><span data-stu-id="7273a-120">This command stops a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="7273a-121">參數</span><span class="sxs-lookup"><span data-stu-id="7273a-121">PARAMETERS</span></span>

### <span data-ttu-id="7273a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7273a-122">-DefaultProfile</span></span>
<span data-ttu-id="7273a-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7273a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7273a-124">-Force</span><span class="sxs-lookup"><span data-stu-id="7273a-124">-Force</span></span>
<span data-ttu-id="7273a-125">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="7273a-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7273a-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7273a-126">-InputObject</span></span>
<span data-ttu-id="7273a-127">要移除的推出。</span><span class="sxs-lookup"><span data-stu-id="7273a-127">The rollout to be removed.</span></span>

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

### <span data-ttu-id="7273a-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="7273a-128">-Name</span></span>
<span data-ttu-id="7273a-129">推出的名稱。</span><span class="sxs-lookup"><span data-stu-id="7273a-129">The name of the rollout.</span></span>

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

### <span data-ttu-id="7273a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7273a-130">-ResourceGroupName</span></span>
<span data-ttu-id="7273a-131">[資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="7273a-131">The resource group.</span></span>

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

### <span data-ttu-id="7273a-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7273a-132">-ResourceId</span></span>
<span data-ttu-id="7273a-133">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="7273a-133">The resource identifier.</span></span>

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

### <span data-ttu-id="7273a-134">-確認</span><span class="sxs-lookup"><span data-stu-id="7273a-134">-Confirm</span></span>
<span data-ttu-id="7273a-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7273a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7273a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7273a-136">-WhatIf</span></span>
<span data-ttu-id="7273a-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7273a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7273a-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7273a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7273a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7273a-139">CommonParameters</span></span>
<span data-ttu-id="7273a-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7273a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7273a-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7273a-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7273a-142">輸入</span><span class="sxs-lookup"><span data-stu-id="7273a-142">INPUTS</span></span>

### <span data-ttu-id="7273a-143">System.object</span><span class="sxs-lookup"><span data-stu-id="7273a-143">System.String</span></span>

### <span data-ttu-id="7273a-144">PSRollout 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="7273a-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="7273a-145">輸出</span><span class="sxs-lookup"><span data-stu-id="7273a-145">OUTPUTS</span></span>

### <span data-ttu-id="7273a-146">PSRollout 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="7273a-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="7273a-147">筆記</span><span class="sxs-lookup"><span data-stu-id="7273a-147">NOTES</span></span>

## <span data-ttu-id="7273a-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="7273a-148">RELATED LINKS</span></span>
