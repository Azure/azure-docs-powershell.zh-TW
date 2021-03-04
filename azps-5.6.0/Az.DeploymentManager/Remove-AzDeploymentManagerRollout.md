---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
ms.openlocfilehash: 3ade9bfd724a84e162c0cedd937f2255ebb5b6a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909097"
---
# <span data-ttu-id="68691-101">Remove-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="68691-101">Remove-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="68691-102">簡介</span><span class="sxs-lookup"><span data-stu-id="68691-102">SYNOPSIS</span></span>
<span data-ttu-id="68691-103">刪除推出。</span><span class="sxs-lookup"><span data-stu-id="68691-103">Deletes the rollout.</span></span>

## <span data-ttu-id="68691-104">語法</span><span class="sxs-lookup"><span data-stu-id="68691-104">SYNTAX</span></span>

### <span data-ttu-id="68691-105">互動式 (預設) </span><span class="sxs-lookup"><span data-stu-id="68691-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68691-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="68691-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68691-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="68691-107">InputObject</span></span>
```
Remove-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68691-108">描述</span><span class="sxs-lookup"><span data-stu-id="68691-108">DESCRIPTION</span></span>
<span data-ttu-id="68691-109">**Remove-AzDeploymentManagerRollout** Cmdlet 會刪除終端機狀態中的推出。</span><span class="sxs-lookup"><span data-stu-id="68691-109">The **Remove-AzDeploymentManagerRollout** cmdlet deletes a rollout in a terminal state.</span></span>
<span data-ttu-id="68691-110">根據部署名稱和資源組名來指定部署。</span><span class="sxs-lookup"><span data-stu-id="68691-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="68691-111">或者，您也可以提供部署物件或 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="68691-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

## <span data-ttu-id="68691-112">例子</span><span class="sxs-lookup"><span data-stu-id="68691-112">EXAMPLES</span></span>

### <span data-ttu-id="68691-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="68691-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="68691-114">此命令會刪除 ContosoResourceGroup 中名為 ContosoRollout 的推出。</span><span class="sxs-lookup"><span data-stu-id="68691-114">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="68691-115">範例 2：使用資源識別碼刪除部署</span><span class="sxs-lookup"><span data-stu-id="68691-115">Example 2: Delete a rollout using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="68691-116">此命令會刪除 ContosoResourceGroup 中名為 ContosoRollout 的推出。</span><span class="sxs-lookup"><span data-stu-id="68691-116">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="68691-117">範例 3：使用部署物件刪除部署。</span><span class="sxs-lookup"><span data-stu-id="68691-117">Example 3: Delete a rollout using the rollout object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="68691-118">此命令會刪除其名稱和 ResourceGroup 分別符合其名稱及資源組名稱屬性的部署$rolloutObject。</span><span class="sxs-lookup"><span data-stu-id="68691-118">This command deletes a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="68691-119">參數</span><span class="sxs-lookup"><span data-stu-id="68691-119">PARAMETERS</span></span>

### <span data-ttu-id="68691-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68691-120">-DefaultProfile</span></span>
<span data-ttu-id="68691-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="68691-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68691-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68691-122">-InputObject</span></span>
<span data-ttu-id="68691-123">要移除的資源。</span><span class="sxs-lookup"><span data-stu-id="68691-123">The resource to be removed.</span></span>

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

### <span data-ttu-id="68691-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="68691-124">-Name</span></span>
<span data-ttu-id="68691-125">推出名稱。</span><span class="sxs-lookup"><span data-stu-id="68691-125">The name of the rollout.</span></span>

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

### <span data-ttu-id="68691-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="68691-126">-PassThru</span></span>
<span data-ttu-id="68691-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="68691-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="68691-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68691-128">-ResourceGroupName</span></span>
<span data-ttu-id="68691-129">資源群組。</span><span class="sxs-lookup"><span data-stu-id="68691-129">The resource group.</span></span>

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

### <span data-ttu-id="68691-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="68691-130">-ResourceId</span></span>
<span data-ttu-id="68691-131">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="68691-131">The resource identifier.</span></span>

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

### <span data-ttu-id="68691-132">-確認</span><span class="sxs-lookup"><span data-stu-id="68691-132">-Confirm</span></span>
<span data-ttu-id="68691-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="68691-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68691-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68691-134">-WhatIf</span></span>
<span data-ttu-id="68691-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="68691-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68691-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="68691-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68691-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68691-137">CommonParameters</span></span>
<span data-ttu-id="68691-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="68691-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68691-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="68691-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68691-140">輸入</span><span class="sxs-lookup"><span data-stu-id="68691-140">INPUTS</span></span>

### <span data-ttu-id="68691-141">System.String</span><span class="sxs-lookup"><span data-stu-id="68691-141">System.String</span></span>

### <span data-ttu-id="68691-142">Microsoft.Azure.Commands.DeploymentManager.models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="68691-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="68691-143">輸出</span><span class="sxs-lookup"><span data-stu-id="68691-143">OUTPUTS</span></span>

### <span data-ttu-id="68691-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="68691-144">System.Boolean</span></span>

## <span data-ttu-id="68691-145">筆記</span><span class="sxs-lookup"><span data-stu-id="68691-145">NOTES</span></span>

## <span data-ttu-id="68691-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="68691-146">RELATED LINKS</span></span>
