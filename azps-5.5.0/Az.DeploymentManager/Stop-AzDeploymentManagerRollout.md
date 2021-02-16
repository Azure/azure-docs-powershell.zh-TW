---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/stop-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Stop-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Stop-AzDeploymentManagerRollout.md
ms.openlocfilehash: cd59cd39fb2834bed2162a257905fea643c0a767
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100137258"
---
# <span data-ttu-id="389d3-101">Stop-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="389d3-101">Stop-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="389d3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="389d3-102">SYNOPSIS</span></span>
<span data-ttu-id="389d3-103">停止推出。</span><span class="sxs-lookup"><span data-stu-id="389d3-103">Stops the rollout.</span></span>

## <span data-ttu-id="389d3-104">句法</span><span class="sxs-lookup"><span data-stu-id="389d3-104">SYNTAX</span></span>

### <span data-ttu-id="389d3-105">互動式 (預設) </span><span class="sxs-lookup"><span data-stu-id="389d3-105">Interactive (Default)</span></span>
```
Stop-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="389d3-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="389d3-106">ResourceId</span></span>
```
Stop-AzDeploymentManagerRollout [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="389d3-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="389d3-107">InputObject</span></span>
```
Stop-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="389d3-108">說明</span><span class="sxs-lookup"><span data-stu-id="389d3-108">DESCRIPTION</span></span>
<span data-ttu-id="389d3-109">**Stop-AzDeploymentManagerRollout** Cmdlet 會停止進行中的推出，並傳回代表推出的目前狀態的物件。</span><span class="sxs-lookup"><span data-stu-id="389d3-109">The **Stop-AzDeploymentManagerRollout** cmdlet stops a rollout in progress and returns an object that represents the current state of the rollout.</span></span>
<span data-ttu-id="389d3-110">依其名稱和資源群組名稱來指定推出。</span><span class="sxs-lookup"><span data-stu-id="389d3-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="389d3-111">或者，您也可以提供推出物件或 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="389d3-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="389d3-112">請注意，一旦停止推出，就無法繼續或重新開機。</span><span class="sxs-lookup"><span data-stu-id="389d3-112">Note that once a rollout is stopped, it cannot be resumed or restarted.</span></span> <span data-ttu-id="389d3-113">您只能建立新的推出。</span><span class="sxs-lookup"><span data-stu-id="389d3-113">You can only create a new rollout.</span></span>

## <span data-ttu-id="389d3-114">示例</span><span class="sxs-lookup"><span data-stu-id="389d3-114">EXAMPLES</span></span>

### <span data-ttu-id="389d3-115">範例1</span><span class="sxs-lookup"><span data-stu-id="389d3-115">Example 1</span></span>
```powershell
PS C:\> Stop-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="389d3-116">這個命令會在 ContosoResourceGroup 中停止名為 ContosoRollout 的推出。</span><span class="sxs-lookup"><span data-stu-id="389d3-116">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="389d3-117">範例2：使用資源識別碼停止推出</span><span class="sxs-lookup"><span data-stu-id="389d3-117">Example 2: Stop a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="389d3-118">這個命令會在 ContosoResourceGroup 中停止名為 ContosoRollout 的推出。</span><span class="sxs-lookup"><span data-stu-id="389d3-118">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="389d3-119">範例3：使用 [推出] 物件停止推出。</span><span class="sxs-lookup"><span data-stu-id="389d3-119">Example 3: Stop a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="389d3-120">這個命令會停止其 name 和 ResourceGroup 會分別與 $rolloutObject 的 Name 和 ResourceGroupName 屬性相符的推出。</span><span class="sxs-lookup"><span data-stu-id="389d3-120">This command stops a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="389d3-121">參數</span><span class="sxs-lookup"><span data-stu-id="389d3-121">PARAMETERS</span></span>

### <span data-ttu-id="389d3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="389d3-122">-DefaultProfile</span></span>
<span data-ttu-id="389d3-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="389d3-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="389d3-124">-Force</span><span class="sxs-lookup"><span data-stu-id="389d3-124">-Force</span></span>
<span data-ttu-id="389d3-125">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="389d3-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="389d3-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="389d3-126">-InputObject</span></span>
<span data-ttu-id="389d3-127">要移除的推出。</span><span class="sxs-lookup"><span data-stu-id="389d3-127">The rollout to be removed.</span></span>

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

### <span data-ttu-id="389d3-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="389d3-128">-Name</span></span>
<span data-ttu-id="389d3-129">推出的名稱。</span><span class="sxs-lookup"><span data-stu-id="389d3-129">The name of the rollout.</span></span>

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

### <span data-ttu-id="389d3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="389d3-130">-ResourceGroupName</span></span>
<span data-ttu-id="389d3-131">[資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="389d3-131">The resource group.</span></span>

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

### <span data-ttu-id="389d3-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="389d3-132">-ResourceId</span></span>
<span data-ttu-id="389d3-133">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="389d3-133">The resource identifier.</span></span>

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

### <span data-ttu-id="389d3-134">-確認</span><span class="sxs-lookup"><span data-stu-id="389d3-134">-Confirm</span></span>
<span data-ttu-id="389d3-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="389d3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="389d3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="389d3-136">-WhatIf</span></span>
<span data-ttu-id="389d3-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="389d3-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="389d3-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="389d3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="389d3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="389d3-139">CommonParameters</span></span>
<span data-ttu-id="389d3-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="389d3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="389d3-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="389d3-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="389d3-142">輸入</span><span class="sxs-lookup"><span data-stu-id="389d3-142">INPUTS</span></span>

### <span data-ttu-id="389d3-143">System.object</span><span class="sxs-lookup"><span data-stu-id="389d3-143">System.String</span></span>

### <span data-ttu-id="389d3-144">PSRollout 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="389d3-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="389d3-145">輸出</span><span class="sxs-lookup"><span data-stu-id="389d3-145">OUTPUTS</span></span>

### <span data-ttu-id="389d3-146">PSRollout 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="389d3-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="389d3-147">筆記</span><span class="sxs-lookup"><span data-stu-id="389d3-147">NOTES</span></span>

## <span data-ttu-id="389d3-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="389d3-148">RELATED LINKS</span></span>
