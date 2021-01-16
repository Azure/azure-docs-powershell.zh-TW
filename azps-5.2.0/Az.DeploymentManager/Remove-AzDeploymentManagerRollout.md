---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
ms.openlocfilehash: 8e5e2c25f69d6e61c21a0f616f49079710c2d5db
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281175"
---
# <span data-ttu-id="92ba6-101">Remove-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="92ba6-101">Remove-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="92ba6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="92ba6-102">SYNOPSIS</span></span>
<span data-ttu-id="92ba6-103">刪除推出。</span><span class="sxs-lookup"><span data-stu-id="92ba6-103">Deletes the rollout.</span></span>

## <span data-ttu-id="92ba6-104">句法</span><span class="sxs-lookup"><span data-stu-id="92ba6-104">SYNTAX</span></span>

### <span data-ttu-id="92ba6-105">互動式 (預設) </span><span class="sxs-lookup"><span data-stu-id="92ba6-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92ba6-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="92ba6-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92ba6-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="92ba6-107">InputObject</span></span>
```
Remove-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92ba6-108">說明</span><span class="sxs-lookup"><span data-stu-id="92ba6-108">DESCRIPTION</span></span>
<span data-ttu-id="92ba6-109">**AzDeploymentManagerRollout** Cmdlet 會在終端狀態中刪除推出。</span><span class="sxs-lookup"><span data-stu-id="92ba6-109">The **Remove-AzDeploymentManagerRollout** cmdlet deletes a rollout in a terminal state.</span></span>
<span data-ttu-id="92ba6-110">依其名稱和資源群組名稱來指定推出。</span><span class="sxs-lookup"><span data-stu-id="92ba6-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="92ba6-111">或者，您也可以提供推出物件或 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="92ba6-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

## <span data-ttu-id="92ba6-112">示例</span><span class="sxs-lookup"><span data-stu-id="92ba6-112">EXAMPLES</span></span>

### <span data-ttu-id="92ba6-113">範例1</span><span class="sxs-lookup"><span data-stu-id="92ba6-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="92ba6-114">這個命令會在 ContosoResourceGroup 中刪除一個名為 ContosoRollout 的推出。</span><span class="sxs-lookup"><span data-stu-id="92ba6-114">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="92ba6-115">範例2：使用資源識別碼刪除推出</span><span class="sxs-lookup"><span data-stu-id="92ba6-115">Example 2: Delete a rollout using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="92ba6-116">這個命令會在 ContosoResourceGroup 中刪除一個名為 ContosoRollout 的推出。</span><span class="sxs-lookup"><span data-stu-id="92ba6-116">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="92ba6-117">範例3：使用 [推出] 物件刪除推出。</span><span class="sxs-lookup"><span data-stu-id="92ba6-117">Example 3: Delete a rollout using the rollout object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="92ba6-118">這個命令會分別刪除名稱和 ResourceGroup 與 $rolloutObject 的 Name 及 ResourceGroupName 屬性相符的推出。</span><span class="sxs-lookup"><span data-stu-id="92ba6-118">This command deletes a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="92ba6-119">參數</span><span class="sxs-lookup"><span data-stu-id="92ba6-119">PARAMETERS</span></span>

### <span data-ttu-id="92ba6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92ba6-120">-DefaultProfile</span></span>
<span data-ttu-id="92ba6-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="92ba6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92ba6-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92ba6-122">-InputObject</span></span>
<span data-ttu-id="92ba6-123">要移除的資源。</span><span class="sxs-lookup"><span data-stu-id="92ba6-123">The resource to be removed.</span></span>

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

### <span data-ttu-id="92ba6-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="92ba6-124">-Name</span></span>
<span data-ttu-id="92ba6-125">推出的名稱。</span><span class="sxs-lookup"><span data-stu-id="92ba6-125">The name of the rollout.</span></span>

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

### <span data-ttu-id="92ba6-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92ba6-126">-PassThru</span></span>
<span data-ttu-id="92ba6-127">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="92ba6-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="92ba6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92ba6-128">-ResourceGroupName</span></span>
<span data-ttu-id="92ba6-129">[資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="92ba6-129">The resource group.</span></span>

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

### <span data-ttu-id="92ba6-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92ba6-130">-ResourceId</span></span>
<span data-ttu-id="92ba6-131">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="92ba6-131">The resource identifier.</span></span>

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

### <span data-ttu-id="92ba6-132">-確認</span><span class="sxs-lookup"><span data-stu-id="92ba6-132">-Confirm</span></span>
<span data-ttu-id="92ba6-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="92ba6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92ba6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92ba6-134">-WhatIf</span></span>
<span data-ttu-id="92ba6-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="92ba6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92ba6-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="92ba6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92ba6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92ba6-137">CommonParameters</span></span>
<span data-ttu-id="92ba6-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="92ba6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92ba6-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="92ba6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92ba6-140">輸入</span><span class="sxs-lookup"><span data-stu-id="92ba6-140">INPUTS</span></span>

### <span data-ttu-id="92ba6-141">System.object</span><span class="sxs-lookup"><span data-stu-id="92ba6-141">System.String</span></span>

### <span data-ttu-id="92ba6-142">PSRollout 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="92ba6-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="92ba6-143">輸出</span><span class="sxs-lookup"><span data-stu-id="92ba6-143">OUTPUTS</span></span>

### <span data-ttu-id="92ba6-144">System.object</span><span class="sxs-lookup"><span data-stu-id="92ba6-144">System.Boolean</span></span>

## <span data-ttu-id="92ba6-145">筆記</span><span class="sxs-lookup"><span data-stu-id="92ba6-145">NOTES</span></span>

## <span data-ttu-id="92ba6-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="92ba6-146">RELATED LINKS</span></span>
