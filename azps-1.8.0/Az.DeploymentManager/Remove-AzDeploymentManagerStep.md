---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
ms.openlocfilehash: 6b95c1110368024c267bb56c3cdaa6eb3c9c68af
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622427"
---
# <span data-ttu-id="d369d-101">Remove-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="d369d-101">Remove-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="d369d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d369d-102">SYNOPSIS</span></span>
<span data-ttu-id="d369d-103">刪除步驟。</span><span class="sxs-lookup"><span data-stu-id="d369d-103">Deletes the step.</span></span>

## <span data-ttu-id="d369d-104">句法</span><span class="sxs-lookup"><span data-stu-id="d369d-104">SYNTAX</span></span>

### <span data-ttu-id="d369d-105">互動式 (預設) </span><span class="sxs-lookup"><span data-stu-id="d369d-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d369d-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d369d-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d369d-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="d369d-107">InputObject</span></span>
```
Remove-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d369d-108">說明</span><span class="sxs-lookup"><span data-stu-id="d369d-108">DESCRIPTION</span></span>
<span data-ttu-id="d369d-109">**AzDeploymentManagerStep** Cmdlet 會刪除一個步驟。</span><span class="sxs-lookup"><span data-stu-id="d369d-109">The **Remove-AzDeploymentManagerStep** cmdlet deletes a step.</span></span>
<span data-ttu-id="d369d-110">依其名稱和資源群組名稱來指定步驟。</span><span class="sxs-lookup"><span data-stu-id="d369d-110">Specify the step by its name and the resource group name.</span></span> <span data-ttu-id="d369d-111">或者，您也可以提供 Step 物件或 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="d369d-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

## <span data-ttu-id="d369d-112">示例</span><span class="sxs-lookup"><span data-stu-id="d369d-112">EXAMPLES</span></span>

### <span data-ttu-id="d369d-113">範例1：移除步驟</span><span class="sxs-lookup"><span data-stu-id="d369d-113">Example 1: Remove a step</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="d369d-114">這個命令會在 ContosoResourceGroup 中刪除一個名為 ContosoService1WaitStep 的步驟。</span><span class="sxs-lookup"><span data-stu-id="d369d-114">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="d369d-115">範例2：使用資源識別碼移除步驟</span><span class="sxs-lookup"><span data-stu-id="d369d-115">Example 2: Remove a step using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="d369d-116">這個命令會在 ContosoResourceGroup 中刪除一個名為 ContosoService1WaitStep 的步驟。</span><span class="sxs-lookup"><span data-stu-id="d369d-116">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="d369d-117">範例3：使用 New-AzDeploymentManagerStep 傳回的物件移除步驟</span><span class="sxs-lookup"><span data-stu-id="d369d-117">Example 3: Remove a step using an object returned by New-AzDeploymentManagerStep</span></span>
### <span data-ttu-id="d369d-118">範例1</span><span class="sxs-lookup"><span data-stu-id="d369d-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -InputObject $stepObject
```

 <span data-ttu-id="d369d-119">這個命令會分別刪除名稱和 ResourceGroup 與 $stepObject 之 Name 和 ResourceGroupName 屬性相符的步驟。</span><span class="sxs-lookup"><span data-stu-id="d369d-119">This command deletes a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="d369d-120">參數</span><span class="sxs-lookup"><span data-stu-id="d369d-120">PARAMETERS</span></span>

### <span data-ttu-id="d369d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d369d-121">-DefaultProfile</span></span>
<span data-ttu-id="d369d-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d369d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d369d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d369d-123">-InputObject</span></span>
<span data-ttu-id="d369d-124">要移除的步驟。</span><span class="sxs-lookup"><span data-stu-id="d369d-124">The step to be removed.</span></span>

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

### <span data-ttu-id="d369d-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="d369d-125">-Name</span></span>
<span data-ttu-id="d369d-126">步驟的名稱。</span><span class="sxs-lookup"><span data-stu-id="d369d-126">The name of the step.</span></span>

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

### <span data-ttu-id="d369d-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d369d-127">-PassThru</span></span>
<span data-ttu-id="d369d-128">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="d369d-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d369d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d369d-129">-ResourceGroupName</span></span>
<span data-ttu-id="d369d-130">[資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="d369d-130">The resource group.</span></span>

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

### <span data-ttu-id="d369d-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d369d-131">-ResourceId</span></span>
<span data-ttu-id="d369d-132">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d369d-132">The resource identifier.</span></span>

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

### <span data-ttu-id="d369d-133">-確認</span><span class="sxs-lookup"><span data-stu-id="d369d-133">-Confirm</span></span>
<span data-ttu-id="d369d-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d369d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d369d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d369d-135">-WhatIf</span></span>
<span data-ttu-id="d369d-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d369d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d369d-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d369d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d369d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d369d-138">CommonParameters</span></span>
<span data-ttu-id="d369d-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d369d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d369d-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d369d-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d369d-141">輸入</span><span class="sxs-lookup"><span data-stu-id="d369d-141">INPUTS</span></span>

### <span data-ttu-id="d369d-142">System.object</span><span class="sxs-lookup"><span data-stu-id="d369d-142">System.String</span></span>

### <span data-ttu-id="d369d-143">PSStepResource 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="d369d-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="d369d-144">輸出</span><span class="sxs-lookup"><span data-stu-id="d369d-144">OUTPUTS</span></span>

### <span data-ttu-id="d369d-145">System.object</span><span class="sxs-lookup"><span data-stu-id="d369d-145">System.Boolean</span></span>

## <span data-ttu-id="d369d-146">筆記</span><span class="sxs-lookup"><span data-stu-id="d369d-146">NOTES</span></span>

## <span data-ttu-id="d369d-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="d369d-147">RELATED LINKS</span></span>
