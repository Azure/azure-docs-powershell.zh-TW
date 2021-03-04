---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/stop-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
ms.openlocfilehash: 2af89bac9e748fca0719abf34bd672d2b09c3af5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905830"
---
# <span data-ttu-id="a7ecc-101">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a7ecc-101">Stop-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="a7ecc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a7ecc-102">SYNOPSIS</span></span>
<span data-ttu-id="a7ecc-103">在管理群組中取消進行中部署</span><span class="sxs-lookup"><span data-stu-id="a7ecc-103">Cancel a running deployment at a management group</span></span>

## <span data-ttu-id="a7ecc-104">語法</span><span class="sxs-lookup"><span data-stu-id="a7ecc-104">SYNTAX</span></span>

### <span data-ttu-id="a7ecc-105">StopByDeploymentName (預設) </span><span class="sxs-lookup"><span data-stu-id="a7ecc-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7ecc-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="a7ecc-106">StopByDeploymentId</span></span>
```
Stop-AzManagementGroupDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7ecc-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="a7ecc-107">StopByInputObject</span></span>
```
Stop-AzManagementGroupDeployment -InputObject <PSDeployment> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7ecc-108">描述</span><span class="sxs-lookup"><span data-stu-id="a7ecc-108">DESCRIPTION</span></span>
<span data-ttu-id="a7ecc-109">**Stop-AzManagementGroupDeployment** Cmdlet 會取消已啟動但在管理群組中未完成的部署。</span><span class="sxs-lookup"><span data-stu-id="a7ecc-109">The **Stop-AzManagementGroupDeployment** cmdlet cancels a deployment that has started but not completed at a management group.</span></span>
<span data-ttu-id="a7ecc-110">若要停止部署，部署必須擁有不完整的部署狀態，例如部署，而不是已完成的狀態，例如已部署或失敗。</span><span class="sxs-lookup"><span data-stu-id="a7ecc-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="a7ecc-111">若要在管理群組中建立部署，請使用 New-AzManagementGroupDeployment Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a7ecc-111">To create a deployment at a management group, use the New-AzManagementGroupDeployment cmdlet.</span></span>

## <span data-ttu-id="a7ecc-112">例子</span><span class="sxs-lookup"><span data-stu-id="a7ecc-112">EXAMPLES</span></span>

### <span data-ttu-id="a7ecc-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="a7ecc-113">Example 1</span></span>
```
PS C:\>Stop-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01"
```

<span data-ttu-id="a7ecc-114">此命令會取消管理群組 「myMG」中執行中部署的「部署01」。</span><span class="sxs-lookup"><span data-stu-id="a7ecc-114">This command cancels a running deployment "deployment01" at the management group "myMG".</span></span>

### <span data-ttu-id="a7ecc-115">範例 2</span><span class="sxs-lookup"><span data-stu-id="a7ecc-115">Example 2</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01" | Stop-AzManagementGroupDeployment
```

<span data-ttu-id="a7ecc-116">此命令會向管理群組「myMG」收到部署「部署01」，並取消它。</span><span class="sxs-lookup"><span data-stu-id="a7ecc-116">This command gets the deployment "deployment01" at the management group "myMG" and cancels it.</span></span> 

## <span data-ttu-id="a7ecc-117">參數</span><span class="sxs-lookup"><span data-stu-id="a7ecc-117">PARAMETERS</span></span>

### <span data-ttu-id="a7ecc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7ecc-118">-DefaultProfile</span></span>
<span data-ttu-id="a7ecc-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a7ecc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7ecc-120">-Id</span><span class="sxs-lookup"><span data-stu-id="a7ecc-120">-Id</span></span>
<span data-ttu-id="a7ecc-121">部署之完整資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a7ecc-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="a7ecc-122">範例：/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="a7ecc-122">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7ecc-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7ecc-123">-InputObject</span></span>
<span data-ttu-id="a7ecc-124">部署物件。</span><span class="sxs-lookup"><span data-stu-id="a7ecc-124">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: StopByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7ecc-125">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="a7ecc-125">-ManagementGroupId</span></span>
<span data-ttu-id="a7ecc-126">管理群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="a7ecc-126">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7ecc-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="a7ecc-127">-Name</span></span>
<span data-ttu-id="a7ecc-128">部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="a7ecc-128">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7ecc-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a7ecc-129">-PassThru</span></span>
<span data-ttu-id="a7ecc-130">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="a7ecc-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="a7ecc-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="a7ecc-131">-Pre</span></span>
<span data-ttu-id="a7ecc-132">設定之後，表示當系統自動決定要使用哪個版本時，Cmdlet 應該使用測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="a7ecc-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="a7ecc-133">-確認</span><span class="sxs-lookup"><span data-stu-id="a7ecc-133">-Confirm</span></span>
<span data-ttu-id="a7ecc-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a7ecc-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7ecc-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7ecc-135">-WhatIf</span></span>
<span data-ttu-id="a7ecc-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a7ecc-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7ecc-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a7ecc-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7ecc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7ecc-138">CommonParameters</span></span>
<span data-ttu-id="a7ecc-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a7ecc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7ecc-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a7ecc-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7ecc-141">輸入</span><span class="sxs-lookup"><span data-stu-id="a7ecc-141">INPUTS</span></span>

### <span data-ttu-id="a7ecc-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="a7ecc-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="a7ecc-143">輸出</span><span class="sxs-lookup"><span data-stu-id="a7ecc-143">OUTPUTS</span></span>

### <span data-ttu-id="a7ecc-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a7ecc-144">System.Boolean</span></span>

## <span data-ttu-id="a7ecc-145">筆記</span><span class="sxs-lookup"><span data-stu-id="a7ecc-145">NOTES</span></span>

## <span data-ttu-id="a7ecc-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="a7ecc-146">RELATED LINKS</span></span>
