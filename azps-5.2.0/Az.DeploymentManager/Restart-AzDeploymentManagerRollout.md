---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/restart-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Restart-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Restart-AzDeploymentManagerRollout.md
ms.openlocfilehash: ba7b62d42764f5098868e6a15eb073cb6b898e82
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98276439"
---
# <span data-ttu-id="30135-101">Restart-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="30135-101">Restart-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="30135-102">摘要</span><span class="sxs-lookup"><span data-stu-id="30135-102">SYNOPSIS</span></span>
<span data-ttu-id="30135-103">重新開機失敗的推出。</span><span class="sxs-lookup"><span data-stu-id="30135-103">Restarts a failed rollout.</span></span>

## <span data-ttu-id="30135-104">句法</span><span class="sxs-lookup"><span data-stu-id="30135-104">SYNTAX</span></span>

### <span data-ttu-id="30135-105">互動式 (預設) </span><span class="sxs-lookup"><span data-stu-id="30135-105">Interactive (Default)</span></span>
```
Restart-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30135-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="30135-106">ResourceId</span></span>
```
Restart-AzDeploymentManagerRollout [-ResourceId] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30135-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="30135-107">InputObject</span></span>
```
Restart-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30135-108">說明</span><span class="sxs-lookup"><span data-stu-id="30135-108">DESCRIPTION</span></span>
<span data-ttu-id="30135-109">**Restart AzDeploymentManagerRollout** Cmdlet 會重新開機失敗的推出，並傳回一個物件，該物件代表有關推出進度之所有詳細資訊的推出。</span><span class="sxs-lookup"><span data-stu-id="30135-109">The **Restart-AzDeploymentManagerRollout** cmdlet restarts a failed rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="30135-110">依其名稱和資源群組名稱來指定推出。</span><span class="sxs-lookup"><span data-stu-id="30135-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="30135-111">或者，您也可以提供推出物件或 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="30135-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>
<span data-ttu-id="30135-112">[選用參數 SkipSucceeded] 可讓您略過首次執行中的所有成功步驟。</span><span class="sxs-lookup"><span data-stu-id="30135-112">Optional parameter SkipSucceeded allows you to skip all the succeeded steps in the previous run of the rollout.</span></span>

## <span data-ttu-id="30135-113">示例</span><span class="sxs-lookup"><span data-stu-id="30135-113">EXAMPLES</span></span>

### <span data-ttu-id="30135-114">範例1</span><span class="sxs-lookup"><span data-stu-id="30135-114">Example 1</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="30135-115">這個命令會在 ContosoResourceGroup 中重新開機一個名為 ContosoRollout 的推出。</span><span class="sxs-lookup"><span data-stu-id="30135-115">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="30135-116">SkipSucceeded 旗標指出已成功執行的所有步驟，都應該略過，且推出應該從上次失敗的位置繼續執行。</span><span class="sxs-lookup"><span data-stu-id="30135-116">The SkipSucceeded flag indicates that all the steps that already ran successfully should be skipped and the rollout should continue execution from where it last failed.</span></span>

### <span data-ttu-id="30135-117">範例2：使用資源識別碼重新開機推出</span><span class="sxs-lookup"><span data-stu-id="30135-117">Example 2: Restart a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="30135-118">這個命令會在 ContosoResourceGroup 中重新開機一個名為 ContosoRollout 的推出。</span><span class="sxs-lookup"><span data-stu-id="30135-118">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="30135-119">範例3：使用 [推出] 物件重新開機推出。</span><span class="sxs-lookup"><span data-stu-id="30135-119">Example 3: Restart a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="30135-120">這個命令會重新開機其名稱和 ResourceGroup 會分別與 $rolloutObject 的 Name 和 ResourceGroupName 屬性相符的推出。</span><span class="sxs-lookup"><span data-stu-id="30135-120">This command restarts a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="30135-121">參數</span><span class="sxs-lookup"><span data-stu-id="30135-121">PARAMETERS</span></span>

### <span data-ttu-id="30135-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30135-122">-DefaultProfile</span></span>
<span data-ttu-id="30135-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="30135-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30135-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="30135-124">-InputObject</span></span>
<span data-ttu-id="30135-125">要移除的資源。</span><span class="sxs-lookup"><span data-stu-id="30135-125">The resource to be removed.</span></span>

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

### <span data-ttu-id="30135-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="30135-126">-Name</span></span>
<span data-ttu-id="30135-127">推出的名稱。</span><span class="sxs-lookup"><span data-stu-id="30135-127">The name of the rollout.</span></span>

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

### <span data-ttu-id="30135-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30135-128">-ResourceGroupName</span></span>
<span data-ttu-id="30135-129">[資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="30135-129">The resource group.</span></span>

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

### <span data-ttu-id="30135-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="30135-130">-ResourceId</span></span>
<span data-ttu-id="30135-131">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="30135-131">The resource identifier.</span></span>

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

### <span data-ttu-id="30135-132">-SkipSucceeded</span><span class="sxs-lookup"><span data-stu-id="30135-132">-SkipSucceeded</span></span>
<span data-ttu-id="30135-133">跳過在前一次執行中運行成功的步驟。</span><span class="sxs-lookup"><span data-stu-id="30135-133">Skip steps that succeeded in the previous run of the rollout.</span></span>

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

### <span data-ttu-id="30135-134">-確認</span><span class="sxs-lookup"><span data-stu-id="30135-134">-Confirm</span></span>
<span data-ttu-id="30135-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="30135-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30135-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30135-136">-WhatIf</span></span>
<span data-ttu-id="30135-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="30135-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30135-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="30135-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30135-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30135-139">CommonParameters</span></span>
<span data-ttu-id="30135-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="30135-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30135-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="30135-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30135-142">輸入</span><span class="sxs-lookup"><span data-stu-id="30135-142">INPUTS</span></span>

### <span data-ttu-id="30135-143">System.object</span><span class="sxs-lookup"><span data-stu-id="30135-143">System.String</span></span>

### <span data-ttu-id="30135-144">PSRollout 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="30135-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="30135-145">輸出</span><span class="sxs-lookup"><span data-stu-id="30135-145">OUTPUTS</span></span>

### <span data-ttu-id="30135-146">PSRollout 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="30135-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="30135-147">筆記</span><span class="sxs-lookup"><span data-stu-id="30135-147">NOTES</span></span>

## <span data-ttu-id="30135-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="30135-148">RELATED LINKS</span></span>
