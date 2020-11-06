---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/restart-azurermdeploymentmanagerrollout
schema: 2.0.0
ms.openlocfilehash: ee1ef6e5b8bcee4af1d3aef67767269042c552df
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443272"
---
# <span data-ttu-id="e51bd-101">Restart-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="e51bd-101">Restart-AzureRmDeploymentManagerRollout</span></span>

## <span data-ttu-id="e51bd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e51bd-102">SYNOPSIS</span></span>
<span data-ttu-id="e51bd-103">重新開機失敗的推出。</span><span class="sxs-lookup"><span data-stu-id="e51bd-103">Restart a failed rollout.</span></span>

## <span data-ttu-id="e51bd-104">句法</span><span class="sxs-lookup"><span data-stu-id="e51bd-104">SYNTAX</span></span>

### <span data-ttu-id="e51bd-105">互動式 (預設) </span><span class="sxs-lookup"><span data-stu-id="e51bd-105">Interactive (Default)</span></span>
```
Restart-AzureRmDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e51bd-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e51bd-106">ResourceId</span></span>
```
Restart-AzureRmDeploymentManagerRollout [-ResourceId] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e51bd-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="e51bd-107">InputObject</span></span>
```
Restart-AzureRmDeploymentManagerRollout [-Rollout] <PSRollout> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e51bd-108">說明</span><span class="sxs-lookup"><span data-stu-id="e51bd-108">DESCRIPTION</span></span>
<span data-ttu-id="e51bd-109">**Restart AzureRmDeploymentManagerRollout** Cmdlet 會重新開機失敗的推出，並傳回一個物件，該物件代表有關推出進度之所有詳細資訊的推出。</span><span class="sxs-lookup"><span data-stu-id="e51bd-109">The **Restart-AzureRmDeploymentManagerRollout** cmdlet restarts a failed rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="e51bd-110">依其名稱和資源群組名稱來指定推出。</span><span class="sxs-lookup"><span data-stu-id="e51bd-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="e51bd-111">或者，您也可以提供推出物件或 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="e51bd-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>
<span data-ttu-id="e51bd-112">[選用參數 SkipSucceeded] 可讓您略過首次執行中的所有成功步驟。</span><span class="sxs-lookup"><span data-stu-id="e51bd-112">Optional parameter SkipSucceeded allows you to skip all the succeeded steps in the previous run of the rollout.</span></span>

## <span data-ttu-id="e51bd-113">示例</span><span class="sxs-lookup"><span data-stu-id="e51bd-113">EXAMPLES</span></span>

### <span data-ttu-id="e51bd-114">範例1</span><span class="sxs-lookup"><span data-stu-id="e51bd-114">Example 1</span></span>
```powershell
PS C:\> Restart-AzureRmDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="e51bd-115">這個命令會在 ContosoResourceGroup 中重新開機一個名為 ContosoRollout 的推出。</span><span class="sxs-lookup"><span data-stu-id="e51bd-115">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="e51bd-116">SkipSucceeded 旗標指出已成功執行的所有步驟，都應該略過，且推出應該從上次失敗的位置繼續執行。</span><span class="sxs-lookup"><span data-stu-id="e51bd-116">The SkipSucceeded flag indicates that all the steps that already ran successfully should be skipped and the rollout should continue execution from where it last failed.</span></span>

### <span data-ttu-id="e51bd-117">範例2：使用資源識別碼重新開機推出</span><span class="sxs-lookup"><span data-stu-id="e51bd-117">Example 2: Restart a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzureRmDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="e51bd-118">這個命令會在 ContosoResourceGroup 中重新開機一個名為 ContosoRollout 的推出。</span><span class="sxs-lookup"><span data-stu-id="e51bd-118">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="e51bd-119">範例3：使用 [推出] 物件重新開機推出。</span><span class="sxs-lookup"><span data-stu-id="e51bd-119">Example 3: Restart a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -Rollout $rolloutObject
```

<span data-ttu-id="e51bd-120">這個命令會重新開機其名稱和 ResourceGroup 會分別與 $rolloutObject 的 Name 和 ResourceGroupName 屬性相符的推出。</span><span class="sxs-lookup"><span data-stu-id="e51bd-120">This command restarts a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="e51bd-121">參數</span><span class="sxs-lookup"><span data-stu-id="e51bd-121">PARAMETERS</span></span>

### <span data-ttu-id="e51bd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e51bd-122">-DefaultProfile</span></span>
<span data-ttu-id="e51bd-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e51bd-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e51bd-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="e51bd-124">-Name</span></span>
<span data-ttu-id="e51bd-125">推出的名稱。</span><span class="sxs-lookup"><span data-stu-id="e51bd-125">The name of the rollout.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e51bd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e51bd-126">-ResourceGroupName</span></span>
<span data-ttu-id="e51bd-127">[資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="e51bd-127">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e51bd-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e51bd-128">-ResourceId</span></span>
<span data-ttu-id="e51bd-129">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e51bd-129">The resource identifier.</span></span>

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

### <span data-ttu-id="e51bd-130">-推出</span><span class="sxs-lookup"><span data-stu-id="e51bd-130">-Rollout</span></span>
<span data-ttu-id="e51bd-131">要移除的資源。</span><span class="sxs-lookup"><span data-stu-id="e51bd-131">The resource to be removed.</span></span>

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

### <span data-ttu-id="e51bd-132">-SkipSucceeded</span><span class="sxs-lookup"><span data-stu-id="e51bd-132">-SkipSucceeded</span></span>
<span data-ttu-id="e51bd-133">跳過在前一次執行中運行成功的步驟。</span><span class="sxs-lookup"><span data-stu-id="e51bd-133">Skip steps that succeeded in the previous run of the rollout.</span></span>

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

### <span data-ttu-id="e51bd-134">-確認</span><span class="sxs-lookup"><span data-stu-id="e51bd-134">-Confirm</span></span>
<span data-ttu-id="e51bd-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e51bd-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e51bd-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e51bd-136">-WhatIf</span></span>
<span data-ttu-id="e51bd-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e51bd-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e51bd-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e51bd-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e51bd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e51bd-139">CommonParameters</span></span>
<span data-ttu-id="e51bd-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e51bd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e51bd-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e51bd-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e51bd-142">輸入</span><span class="sxs-lookup"><span data-stu-id="e51bd-142">INPUTS</span></span>

### <span data-ttu-id="e51bd-143">PSRollout 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="e51bd-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="e51bd-144">輸出</span><span class="sxs-lookup"><span data-stu-id="e51bd-144">OUTPUTS</span></span>

### <span data-ttu-id="e51bd-145">PSRollout 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="e51bd-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="e51bd-146">筆記</span><span class="sxs-lookup"><span data-stu-id="e51bd-146">NOTES</span></span>

## <span data-ttu-id="e51bd-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="e51bd-147">RELATED LINKS</span></span>

[<span data-ttu-id="e51bd-148">AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="e51bd-148">Get-AzureRmDeploymentManagerRollout</span></span>](./Get-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="e51bd-149">停止 AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="e51bd-149">Stop-AzureRmDeploymentManagerRollout</span></span>](./Stop-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="e51bd-150">移除-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="e51bd-150">Remove-AzureRmDeploymentManagerRollout</span></span>](./Remove-AzureRmDeploymentManagerRollout.md)