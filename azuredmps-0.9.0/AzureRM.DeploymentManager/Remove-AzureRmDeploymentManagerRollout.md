---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerrollout
schema: 2.0.0
ms.openlocfilehash: f329468dce9c520eb647bb0d927ba91de64a5c33
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93442499"
---
# <span data-ttu-id="811b8-101">Remove-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="811b8-101">Remove-AzureRmDeploymentManagerRollout</span></span>

## <span data-ttu-id="811b8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="811b8-102">SYNOPSIS</span></span>
<span data-ttu-id="811b8-103">刪除推出。</span><span class="sxs-lookup"><span data-stu-id="811b8-103">Deletes a rollout.</span></span>

## <span data-ttu-id="811b8-104">句法</span><span class="sxs-lookup"><span data-stu-id="811b8-104">SYNTAX</span></span>

### <span data-ttu-id="811b8-105">互動式 (預設) </span><span class="sxs-lookup"><span data-stu-id="811b8-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="811b8-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="811b8-106">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerRollout [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="811b8-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="811b8-107">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerRollout [-Rollout] <PSRollout> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="811b8-108">說明</span><span class="sxs-lookup"><span data-stu-id="811b8-108">DESCRIPTION</span></span>
<span data-ttu-id="811b8-109">**AzureRmDeploymentManagerRollout** Cmdlet 會在終端狀態中刪除推出。</span><span class="sxs-lookup"><span data-stu-id="811b8-109">The **Remove-AzureRmDeploymentManagerRollout** cmdlet deletes a rollout in a terminal state.</span></span>
<span data-ttu-id="811b8-110">依其名稱和資源群組名稱來指定推出。</span><span class="sxs-lookup"><span data-stu-id="811b8-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="811b8-111">或者，您也可以提供推出物件或 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="811b8-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

## <span data-ttu-id="811b8-112">示例</span><span class="sxs-lookup"><span data-stu-id="811b8-112">EXAMPLES</span></span>

### <span data-ttu-id="811b8-113">範例1</span><span class="sxs-lookup"><span data-stu-id="811b8-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="811b8-114">這個命令會在 ContosoResourceGroup 中刪除一個名為 ContosoRollout 的推出。</span><span class="sxs-lookup"><span data-stu-id="811b8-114">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="811b8-115">範例2：使用資源識別碼刪除推出</span><span class="sxs-lookup"><span data-stu-id="811b8-115">Example 2: Delete a rollout using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="811b8-116">這個命令會在 ContosoResourceGroup 中刪除一個名為 ContosoRollout 的推出。</span><span class="sxs-lookup"><span data-stu-id="811b8-116">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="811b8-117">範例3：使用 [推出] 物件刪除推出。</span><span class="sxs-lookup"><span data-stu-id="811b8-117">Example 3: Delete a rollout using the rollout object.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerRollout -Rollout $rolloutObject
```

<span data-ttu-id="811b8-118">這個命令會分別刪除名稱和 ResourceGroup 與 $rolloutObject 的 Name 及 ResourceGroupName 屬性相符的推出。</span><span class="sxs-lookup"><span data-stu-id="811b8-118">This command deletes a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="811b8-119">參數</span><span class="sxs-lookup"><span data-stu-id="811b8-119">PARAMETERS</span></span>

### <span data-ttu-id="811b8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="811b8-120">-DefaultProfile</span></span>
<span data-ttu-id="811b8-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="811b8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="811b8-122">-Force</span><span class="sxs-lookup"><span data-stu-id="811b8-122">-Force</span></span>
<span data-ttu-id="811b8-123">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="811b8-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="811b8-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="811b8-124">-Name</span></span>
<span data-ttu-id="811b8-125">推出的名稱。</span><span class="sxs-lookup"><span data-stu-id="811b8-125">The name of the rollout.</span></span>

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

### <span data-ttu-id="811b8-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="811b8-126">-PassThru</span></span>
<span data-ttu-id="811b8-127">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="811b8-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="811b8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="811b8-128">-ResourceGroupName</span></span>
<span data-ttu-id="811b8-129">[資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="811b8-129">The resource group.</span></span>

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

### <span data-ttu-id="811b8-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="811b8-130">-ResourceId</span></span>
<span data-ttu-id="811b8-131">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="811b8-131">The resource identifier.</span></span>

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

### <span data-ttu-id="811b8-132">-推出</span><span class="sxs-lookup"><span data-stu-id="811b8-132">-Rollout</span></span>
<span data-ttu-id="811b8-133">要移除的資源。</span><span class="sxs-lookup"><span data-stu-id="811b8-133">The resource to be removed.</span></span>

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

### <span data-ttu-id="811b8-134">-確認</span><span class="sxs-lookup"><span data-stu-id="811b8-134">-Confirm</span></span>
<span data-ttu-id="811b8-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="811b8-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="811b8-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="811b8-136">-WhatIf</span></span>
<span data-ttu-id="811b8-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="811b8-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="811b8-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="811b8-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="811b8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="811b8-139">CommonParameters</span></span>
<span data-ttu-id="811b8-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="811b8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="811b8-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="811b8-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="811b8-142">輸入</span><span class="sxs-lookup"><span data-stu-id="811b8-142">INPUTS</span></span>

### <span data-ttu-id="811b8-143">PSRollout 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="811b8-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="811b8-144">輸出</span><span class="sxs-lookup"><span data-stu-id="811b8-144">OUTPUTS</span></span>

### <span data-ttu-id="811b8-145">System.object</span><span class="sxs-lookup"><span data-stu-id="811b8-145">System.Boolean</span></span>

## <span data-ttu-id="811b8-146">筆記</span><span class="sxs-lookup"><span data-stu-id="811b8-146">NOTES</span></span>

## <span data-ttu-id="811b8-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="811b8-147">RELATED LINKS</span></span>

[<span data-ttu-id="811b8-148">AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="811b8-148">Get-AzureRmDeploymentManagerRollout</span></span>](./Get-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="811b8-149">停止 AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="811b8-149">Stop-AzureRmDeploymentManagerRollout</span></span>](./Stop-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="811b8-150">重新開機-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="811b8-150">Restart-AzureRmDeploymentManagerRollout</span></span>](./Restart-AzureRmDeploymentManagerRollout.md)