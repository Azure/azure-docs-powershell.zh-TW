---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerstep
schema: 2.0.0
ms.openlocfilehash: 3abceb6c3c270378c911036967698f459cbe063a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93442584"
---
# <span data-ttu-id="2a955-101">Remove-AzureRmDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="2a955-101">Remove-AzureRmDeploymentManagerStep</span></span>

## <span data-ttu-id="2a955-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2a955-102">SYNOPSIS</span></span>
<span data-ttu-id="2a955-103">刪除步驟。</span><span class="sxs-lookup"><span data-stu-id="2a955-103">Deletes a step.</span></span>

## <span data-ttu-id="2a955-104">句法</span><span class="sxs-lookup"><span data-stu-id="2a955-104">SYNTAX</span></span>

### <span data-ttu-id="2a955-105">互動式 (預設) </span><span class="sxs-lookup"><span data-stu-id="2a955-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a955-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a955-106">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerStep [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a955-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="2a955-107">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerStep [-Step] <PSStepResource> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a955-108">說明</span><span class="sxs-lookup"><span data-stu-id="2a955-108">DESCRIPTION</span></span>
<span data-ttu-id="2a955-109">**AzureRmDeploymentManagerStep** Cmdlet 會刪除一個步驟。</span><span class="sxs-lookup"><span data-stu-id="2a955-109">The **Remove-AzureRmDeploymentManagerStep** cmdlet deletes a step.</span></span>
<span data-ttu-id="2a955-110">依其名稱和資源群組名稱來指定步驟。</span><span class="sxs-lookup"><span data-stu-id="2a955-110">Specify the step by its name and the resource group name.</span></span> <span data-ttu-id="2a955-111">或者，您也可以提供 Step 物件或 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="2a955-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

## <span data-ttu-id="2a955-112">示例</span><span class="sxs-lookup"><span data-stu-id="2a955-112">EXAMPLES</span></span>
### <span data-ttu-id="2a955-113">範例1：移除步驟</span><span class="sxs-lookup"><span data-stu-id="2a955-113">Example 1: Remove a step</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="2a955-114">這個命令會在 ContosoResourceGroup 中刪除一個名為 ContosoService1WaitStep 的步驟。</span><span class="sxs-lookup"><span data-stu-id="2a955-114">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="2a955-115">範例2：使用資源識別碼移除步驟</span><span class="sxs-lookup"><span data-stu-id="2a955-115">Example 2: Remove a step using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="2a955-116">這個命令會在 ContosoResourceGroup 中刪除一個名為 ContosoService1WaitStep 的步驟。</span><span class="sxs-lookup"><span data-stu-id="2a955-116">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="2a955-117">範例3：使用 New-AzureRmDeploymentManagerStep 傳回的物件移除步驟</span><span class="sxs-lookup"><span data-stu-id="2a955-117">Example 3: Remove a step using an object returned by New-AzureRmDeploymentManagerStep</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerStep -Step $stepObject
```

 <span data-ttu-id="2a955-118">這個命令會分別刪除名稱和 ResourceGroup 與 $stepObject 之 Name 和 ResourceGroupName 屬性相符的步驟。</span><span class="sxs-lookup"><span data-stu-id="2a955-118">This command deletes a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="2a955-119">參數</span><span class="sxs-lookup"><span data-stu-id="2a955-119">PARAMETERS</span></span>

### <span data-ttu-id="2a955-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a955-120">-DefaultProfile</span></span>
<span data-ttu-id="2a955-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2a955-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a955-122">-Force</span><span class="sxs-lookup"><span data-stu-id="2a955-122">-Force</span></span>
<span data-ttu-id="2a955-123">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="2a955-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2a955-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="2a955-124">-Name</span></span>
<span data-ttu-id="2a955-125">步驟的名稱。</span><span class="sxs-lookup"><span data-stu-id="2a955-125">The name of the step.</span></span>

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

### <span data-ttu-id="2a955-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a955-126">-PassThru</span></span>
<span data-ttu-id="2a955-127">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="2a955-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="2a955-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a955-128">-ResourceGroupName</span></span>
<span data-ttu-id="2a955-129">[資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="2a955-129">The resource group.</span></span>

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

### <span data-ttu-id="2a955-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a955-130">-ResourceId</span></span>
<span data-ttu-id="2a955-131">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="2a955-131">The resource identifier.</span></span>

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

### <span data-ttu-id="2a955-132">-步驟</span><span class="sxs-lookup"><span data-stu-id="2a955-132">-Step</span></span>
<span data-ttu-id="2a955-133">要移除的步驟。</span><span class="sxs-lookup"><span data-stu-id="2a955-133">The step to be removed.</span></span>

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

### <span data-ttu-id="2a955-134">-確認</span><span class="sxs-lookup"><span data-stu-id="2a955-134">-Confirm</span></span>
<span data-ttu-id="2a955-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2a955-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a955-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a955-136">-WhatIf</span></span>
<span data-ttu-id="2a955-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2a955-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a955-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2a955-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a955-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a955-139">CommonParameters</span></span>
<span data-ttu-id="2a955-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2a955-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2a955-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2a955-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a955-142">輸入</span><span class="sxs-lookup"><span data-stu-id="2a955-142">INPUTS</span></span>

### <span data-ttu-id="2a955-143">System.object</span><span class="sxs-lookup"><span data-stu-id="2a955-143">System.String</span></span>

### <span data-ttu-id="2a955-144">PSStepResource 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="2a955-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="2a955-145">輸出</span><span class="sxs-lookup"><span data-stu-id="2a955-145">OUTPUTS</span></span>

### <span data-ttu-id="2a955-146">System.object</span><span class="sxs-lookup"><span data-stu-id="2a955-146">System.Boolean</span></span>

## <span data-ttu-id="2a955-147">筆記</span><span class="sxs-lookup"><span data-stu-id="2a955-147">NOTES</span></span>

## <span data-ttu-id="2a955-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="2a955-148">RELATED LINKS</span></span>
