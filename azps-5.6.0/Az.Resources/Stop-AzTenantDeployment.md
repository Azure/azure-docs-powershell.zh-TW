---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/stop-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
ms.openlocfilehash: e6948bf1868865bb53bd3e1bfabc68aded44cd4c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905822"
---
# <span data-ttu-id="0f93e-101">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="0f93e-101">Stop-AzTenantDeployment</span></span>

## <span data-ttu-id="0f93e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0f93e-102">SYNOPSIS</span></span>
<span data-ttu-id="0f93e-103">在租使用者範圍中取消進行中部署</span><span class="sxs-lookup"><span data-stu-id="0f93e-103">Cancel a running deployment at tenant scope</span></span>

## <span data-ttu-id="0f93e-104">語法</span><span class="sxs-lookup"><span data-stu-id="0f93e-104">SYNTAX</span></span>

### <span data-ttu-id="0f93e-105">StopByDeploymentName (預設) </span><span class="sxs-lookup"><span data-stu-id="0f93e-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzTenantDeployment [-Name] <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f93e-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="0f93e-106">StopByDeploymentId</span></span>
```
Stop-AzTenantDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f93e-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="0f93e-107">StopByInputObject</span></span>
```
Stop-AzTenantDeployment -InputObject <PSDeployment> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f93e-108">描述</span><span class="sxs-lookup"><span data-stu-id="0f93e-108">DESCRIPTION</span></span>
<span data-ttu-id="0f93e-109">**Stop-AzTenantDeployment** Cmdlet 會取消目前租使用者範圍中已開始但尚未完成的部署。</span><span class="sxs-lookup"><span data-stu-id="0f93e-109">The **Stop-AzTenantDeployment** cmdlet cancels a deployment that has started but not completed at the current tenant scope.</span></span>
<span data-ttu-id="0f93e-110">若要停止部署，部署必須擁有不完整的部署狀態，例如部署，而不是已完成的狀態，例如已部署或失敗。</span><span class="sxs-lookup"><span data-stu-id="0f93e-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="0f93e-111">若要在租使用者範圍中建立部署，請使用 New-AzTenantDeployment Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0f93e-111">To create a deployment at tenant scope, use the New-AzTenantDeployment cmdlet.</span></span>

## <span data-ttu-id="0f93e-112">例子</span><span class="sxs-lookup"><span data-stu-id="0f93e-112">EXAMPLES</span></span>

### <span data-ttu-id="0f93e-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="0f93e-113">Example 1</span></span>
```
PS C:\>Stop-AzTenantDeployment -Name "deployment01"
```

<span data-ttu-id="0f93e-114">此命令會取消目前租使用者範圍中執行中的部署「部署01」。</span><span class="sxs-lookup"><span data-stu-id="0f93e-114">This command cancels a running deployment "deployment01" at the current tenant scope.</span></span>

### <span data-ttu-id="0f93e-115">範例 2</span><span class="sxs-lookup"><span data-stu-id="0f93e-115">Example 2</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "deployment01" | Stop-AzTenantDeployment
```

<span data-ttu-id="0f93e-116">此命令會獲得目前租使用者範圍中的部署「部署01」，並取消它。</span><span class="sxs-lookup"><span data-stu-id="0f93e-116">This command gets the deployment "deployment01" at the current tenant scope and cancels it.</span></span> 

## <span data-ttu-id="0f93e-117">參數</span><span class="sxs-lookup"><span data-stu-id="0f93e-117">PARAMETERS</span></span>

### <span data-ttu-id="0f93e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f93e-118">-DefaultProfile</span></span>
<span data-ttu-id="0f93e-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0f93e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f93e-120">-Id</span><span class="sxs-lookup"><span data-stu-id="0f93e-120">-Id</span></span>
<span data-ttu-id="0f93e-121">部署之完整資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0f93e-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="0f93e-122">範例：/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="0f93e-122">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="0f93e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f93e-123">-InputObject</span></span>
<span data-ttu-id="0f93e-124">部署物件。</span><span class="sxs-lookup"><span data-stu-id="0f93e-124">The deployment object.</span></span>

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

### <span data-ttu-id="0f93e-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="0f93e-125">-Name</span></span>
<span data-ttu-id="0f93e-126">部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="0f93e-126">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentName
Aliases: DeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f93e-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0f93e-127">-PassThru</span></span>
<span data-ttu-id="0f93e-128">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="0f93e-128">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="0f93e-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="0f93e-129">-Pre</span></span>
<span data-ttu-id="0f93e-130">設定之後，表示當系統自動決定要使用哪個版本時，Cmdlet 應該使用測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="0f93e-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="0f93e-131">-確認</span><span class="sxs-lookup"><span data-stu-id="0f93e-131">-Confirm</span></span>
<span data-ttu-id="0f93e-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0f93e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f93e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f93e-133">-WhatIf</span></span>
<span data-ttu-id="0f93e-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0f93e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f93e-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0f93e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f93e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f93e-136">CommonParameters</span></span>
<span data-ttu-id="0f93e-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0f93e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f93e-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0f93e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f93e-139">輸入</span><span class="sxs-lookup"><span data-stu-id="0f93e-139">INPUTS</span></span>

### <span data-ttu-id="0f93e-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="0f93e-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="0f93e-141">輸出</span><span class="sxs-lookup"><span data-stu-id="0f93e-141">OUTPUTS</span></span>

### <span data-ttu-id="0f93e-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0f93e-142">System.Boolean</span></span>

## <span data-ttu-id="0f93e-143">筆記</span><span class="sxs-lookup"><span data-stu-id="0f93e-143">NOTES</span></span>

## <span data-ttu-id="0f93e-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="0f93e-144">RELATED LINKS</span></span>
