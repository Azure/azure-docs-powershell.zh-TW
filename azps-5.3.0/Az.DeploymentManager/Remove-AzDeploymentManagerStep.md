---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
ms.openlocfilehash: 5e4af2ef006e51cee135dd642bcae7282940e8be
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98436617"
---
# <span data-ttu-id="ebbbc-101">Remove-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="ebbbc-101">Remove-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="ebbbc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ebbbc-102">SYNOPSIS</span></span>
<span data-ttu-id="ebbbc-103">刪除步驟。</span><span class="sxs-lookup"><span data-stu-id="ebbbc-103">Deletes the step.</span></span>

## <span data-ttu-id="ebbbc-104">句法</span><span class="sxs-lookup"><span data-stu-id="ebbbc-104">SYNTAX</span></span>

### <span data-ttu-id="ebbbc-105">互動式 (預設) </span><span class="sxs-lookup"><span data-stu-id="ebbbc-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebbbc-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ebbbc-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebbbc-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="ebbbc-107">InputObject</span></span>
```
Remove-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebbbc-108">說明</span><span class="sxs-lookup"><span data-stu-id="ebbbc-108">DESCRIPTION</span></span>
<span data-ttu-id="ebbbc-109">**AzDeploymentManagerStep** Cmdlet 會刪除一個步驟。</span><span class="sxs-lookup"><span data-stu-id="ebbbc-109">The **Remove-AzDeploymentManagerStep** cmdlet deletes a step.</span></span>
<span data-ttu-id="ebbbc-110">依其名稱和資源群組名稱來指定步驟。</span><span class="sxs-lookup"><span data-stu-id="ebbbc-110">Specify the step by its name and the resource group name.</span></span> <span data-ttu-id="ebbbc-111">或者，您也可以提供 Step 物件或 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="ebbbc-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

## <span data-ttu-id="ebbbc-112">示例</span><span class="sxs-lookup"><span data-stu-id="ebbbc-112">EXAMPLES</span></span>

### <span data-ttu-id="ebbbc-113">範例1：移除步驟</span><span class="sxs-lookup"><span data-stu-id="ebbbc-113">Example 1: Remove a step</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="ebbbc-114">這個命令會在 ContosoResourceGroup 中刪除一個名為 ContosoService1WaitStep 的步驟。</span><span class="sxs-lookup"><span data-stu-id="ebbbc-114">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="ebbbc-115">範例2：使用資源識別碼移除步驟</span><span class="sxs-lookup"><span data-stu-id="ebbbc-115">Example 2: Remove a step using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="ebbbc-116">這個命令會在 ContosoResourceGroup 中刪除一個名為 ContosoService1WaitStep 的步驟。</span><span class="sxs-lookup"><span data-stu-id="ebbbc-116">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="ebbbc-117">範例3：使用 New-AzDeploymentManagerStep 傳回的物件移除步驟</span><span class="sxs-lookup"><span data-stu-id="ebbbc-117">Example 3: Remove a step using an object returned by New-AzDeploymentManagerStep</span></span>
### <span data-ttu-id="ebbbc-118">範例1</span><span class="sxs-lookup"><span data-stu-id="ebbbc-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -InputObject $stepObject
```

 <span data-ttu-id="ebbbc-119">這個命令會分別刪除名稱和 ResourceGroup 與 $stepObject 之 Name 和 ResourceGroupName 屬性相符的步驟。</span><span class="sxs-lookup"><span data-stu-id="ebbbc-119">This command deletes a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="ebbbc-120">參數</span><span class="sxs-lookup"><span data-stu-id="ebbbc-120">PARAMETERS</span></span>

### <span data-ttu-id="ebbbc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebbbc-121">-DefaultProfile</span></span>
<span data-ttu-id="ebbbc-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ebbbc-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebbbc-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ebbbc-123">-InputObject</span></span>
<span data-ttu-id="ebbbc-124">要移除的步驟。</span><span class="sxs-lookup"><span data-stu-id="ebbbc-124">The step to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebbbc-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="ebbbc-125">-Name</span></span>
<span data-ttu-id="ebbbc-126">步驟的名稱。</span><span class="sxs-lookup"><span data-stu-id="ebbbc-126">The name of the step.</span></span>

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

### <span data-ttu-id="ebbbc-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ebbbc-127">-PassThru</span></span>
<span data-ttu-id="ebbbc-128">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="ebbbc-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ebbbc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebbbc-129">-ResourceGroupName</span></span>
<span data-ttu-id="ebbbc-130">[資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="ebbbc-130">The resource group.</span></span>

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

### <span data-ttu-id="ebbbc-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ebbbc-131">-ResourceId</span></span>
<span data-ttu-id="ebbbc-132">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ebbbc-132">The resource identifier.</span></span>

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

### <span data-ttu-id="ebbbc-133">-確認</span><span class="sxs-lookup"><span data-stu-id="ebbbc-133">-Confirm</span></span>
<span data-ttu-id="ebbbc-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ebbbc-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebbbc-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebbbc-135">-WhatIf</span></span>
<span data-ttu-id="ebbbc-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ebbbc-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebbbc-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ebbbc-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebbbc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebbbc-138">CommonParameters</span></span>
<span data-ttu-id="ebbbc-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ebbbc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebbbc-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ebbbc-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebbbc-141">輸入</span><span class="sxs-lookup"><span data-stu-id="ebbbc-141">INPUTS</span></span>

### <span data-ttu-id="ebbbc-142">System.object</span><span class="sxs-lookup"><span data-stu-id="ebbbc-142">System.String</span></span>

### <span data-ttu-id="ebbbc-143">PSStepResource 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="ebbbc-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="ebbbc-144">輸出</span><span class="sxs-lookup"><span data-stu-id="ebbbc-144">OUTPUTS</span></span>

### <span data-ttu-id="ebbbc-145">System.object</span><span class="sxs-lookup"><span data-stu-id="ebbbc-145">System.Boolean</span></span>

## <span data-ttu-id="ebbbc-146">筆記</span><span class="sxs-lookup"><span data-stu-id="ebbbc-146">NOTES</span></span>

## <span data-ttu-id="ebbbc-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="ebbbc-147">RELATED LINKS</span></span>
