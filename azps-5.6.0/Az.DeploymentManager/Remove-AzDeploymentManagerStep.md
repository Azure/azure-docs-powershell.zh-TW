---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
ms.openlocfilehash: 96f5f9e3dd0390d714b0ee7a74b3f585b46dcc1b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905498"
---
# <span data-ttu-id="3b526-101">Remove-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="3b526-101">Remove-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="3b526-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3b526-102">SYNOPSIS</span></span>
<span data-ttu-id="3b526-103">刪除步驟。</span><span class="sxs-lookup"><span data-stu-id="3b526-103">Deletes the step.</span></span>

## <span data-ttu-id="3b526-104">語法</span><span class="sxs-lookup"><span data-stu-id="3b526-104">SYNTAX</span></span>

### <span data-ttu-id="3b526-105">互動式 (預設) </span><span class="sxs-lookup"><span data-stu-id="3b526-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b526-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b526-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b526-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="3b526-107">InputObject</span></span>
```
Remove-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b526-108">描述</span><span class="sxs-lookup"><span data-stu-id="3b526-108">DESCRIPTION</span></span>
<span data-ttu-id="3b526-109">**Remove-AzDeploymentManagerStep** Cmdlet 會刪除一個步驟。</span><span class="sxs-lookup"><span data-stu-id="3b526-109">The **Remove-AzDeploymentManagerStep** cmdlet deletes a step.</span></span>
<span data-ttu-id="3b526-110">請根據步驟的名稱和資源組名來指定步驟。</span><span class="sxs-lookup"><span data-stu-id="3b526-110">Specify the step by its name and the resource group name.</span></span> <span data-ttu-id="3b526-111">或者，您也可以提供 Step 物件或 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="3b526-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

## <span data-ttu-id="3b526-112">例子</span><span class="sxs-lookup"><span data-stu-id="3b526-112">EXAMPLES</span></span>

### <span data-ttu-id="3b526-113">範例 1：移除步驟</span><span class="sxs-lookup"><span data-stu-id="3b526-113">Example 1: Remove a step</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="3b526-114">此命令會刪除 ContosoResourceGroup 中名為 ContosoService1WaitStep 的步驟。</span><span class="sxs-lookup"><span data-stu-id="3b526-114">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="3b526-115">範例 2：使用資源識別碼移除步驟</span><span class="sxs-lookup"><span data-stu-id="3b526-115">Example 2: Remove a step using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="3b526-116">此命令會刪除 ContosoResourceGroup 中名為 ContosoService1WaitStep 的步驟。</span><span class="sxs-lookup"><span data-stu-id="3b526-116">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="3b526-117">範例 3：使用由 New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="3b526-117">Example 3: Remove a step using an object returned by New-AzDeploymentManagerStep</span></span>
### <span data-ttu-id="3b526-118">範例 1</span><span class="sxs-lookup"><span data-stu-id="3b526-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -InputObject $stepObject
```

 <span data-ttu-id="3b526-119">此命令會刪除名稱與 ResourceGroup 分別符合其名稱及資源組名稱$stepObject的步驟。</span><span class="sxs-lookup"><span data-stu-id="3b526-119">This command deletes a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="3b526-120">參數</span><span class="sxs-lookup"><span data-stu-id="3b526-120">PARAMETERS</span></span>

### <span data-ttu-id="3b526-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b526-121">-DefaultProfile</span></span>
<span data-ttu-id="3b526-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3b526-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b526-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b526-123">-InputObject</span></span>
<span data-ttu-id="3b526-124">要移除的步驟。</span><span class="sxs-lookup"><span data-stu-id="3b526-124">The step to be removed.</span></span>

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

### <span data-ttu-id="3b526-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="3b526-125">-Name</span></span>
<span data-ttu-id="3b526-126">步驟的名稱。</span><span class="sxs-lookup"><span data-stu-id="3b526-126">The name of the step.</span></span>

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

### <span data-ttu-id="3b526-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3b526-127">-PassThru</span></span>
<span data-ttu-id="3b526-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="3b526-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="3b526-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b526-129">-ResourceGroupName</span></span>
<span data-ttu-id="3b526-130">資源群組。</span><span class="sxs-lookup"><span data-stu-id="3b526-130">The resource group.</span></span>

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

### <span data-ttu-id="3b526-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b526-131">-ResourceId</span></span>
<span data-ttu-id="3b526-132">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="3b526-132">The resource identifier.</span></span>

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

### <span data-ttu-id="3b526-133">-確認</span><span class="sxs-lookup"><span data-stu-id="3b526-133">-Confirm</span></span>
<span data-ttu-id="3b526-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3b526-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b526-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b526-135">-WhatIf</span></span>
<span data-ttu-id="3b526-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3b526-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b526-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3b526-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b526-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b526-138">CommonParameters</span></span>
<span data-ttu-id="3b526-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3b526-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b526-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3b526-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b526-141">輸入</span><span class="sxs-lookup"><span data-stu-id="3b526-141">INPUTS</span></span>

### <span data-ttu-id="3b526-142">System.String</span><span class="sxs-lookup"><span data-stu-id="3b526-142">System.String</span></span>

### <span data-ttu-id="3b526-143">Microsoft.Azure.Commands.DeploymentManager.models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="3b526-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="3b526-144">輸出</span><span class="sxs-lookup"><span data-stu-id="3b526-144">OUTPUTS</span></span>

### <span data-ttu-id="3b526-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3b526-145">System.Boolean</span></span>

## <span data-ttu-id="3b526-146">筆記</span><span class="sxs-lookup"><span data-stu-id="3b526-146">NOTES</span></span>

## <span data-ttu-id="3b526-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="3b526-147">RELATED LINKS</span></span>
