---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/stop-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
ms.openlocfilehash: 794cc94ece2452f1fd5518d64d4071d7fa6ec326
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904861"
---
# <span data-ttu-id="0d91d-101">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="0d91d-101">Stop-AzDeployment</span></span>

## <span data-ttu-id="0d91d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0d91d-102">SYNOPSIS</span></span>
<span data-ttu-id="0d91d-103">取消進行中部署</span><span class="sxs-lookup"><span data-stu-id="0d91d-103">Cancel a running deployment</span></span>

## <span data-ttu-id="0d91d-104">語法</span><span class="sxs-lookup"><span data-stu-id="0d91d-104">SYNTAX</span></span>

### <span data-ttu-id="0d91d-105">StopByDeploymentName (預設) </span><span class="sxs-lookup"><span data-stu-id="0d91d-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzDeployment [-Name] <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d91d-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="0d91d-106">StopByDeploymentId</span></span>
```
Stop-AzDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d91d-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="0d91d-107">StopByInputObject</span></span>
```
Stop-AzDeployment -InputObject <PSDeployment> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d91d-108">描述</span><span class="sxs-lookup"><span data-stu-id="0d91d-108">DESCRIPTION</span></span>
<span data-ttu-id="0d91d-109">**Stop-AzDeployment** Cmdlet 會取消訂閱範圍中已啟動但尚未完成的部署。</span><span class="sxs-lookup"><span data-stu-id="0d91d-109">The **Stop-AzDeployment** cmdlet cancels a deployment at subscription scope that has started but not completed.</span></span>
<span data-ttu-id="0d91d-110">若要停止部署，部署必須擁有不完整的部署狀態，例如部署，而不是已完成的狀態，例如已部署或失敗。</span><span class="sxs-lookup"><span data-stu-id="0d91d-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="0d91d-111">若要在訂閱範圍中建立部署，請使用 New-AzDeployment Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0d91d-111">To create a deployment at subscription scope, use the New-AzDeployment cmdlet.</span></span>

<span data-ttu-id="0d91d-112">此 Cmdlet 只會停止一個進行中的部署。</span><span class="sxs-lookup"><span data-stu-id="0d91d-112">This cmdlet stops only one running deployment.</span></span> <span data-ttu-id="0d91d-113">使用 *Name* 參數來停止特定部署。</span><span class="sxs-lookup"><span data-stu-id="0d91d-113">Use the *Name* parameter to stop a specific deployment.</span></span>

## <span data-ttu-id="0d91d-114">例子</span><span class="sxs-lookup"><span data-stu-id="0d91d-114">EXAMPLES</span></span>

### <span data-ttu-id="0d91d-115">範例 1</span><span class="sxs-lookup"><span data-stu-id="0d91d-115">Example 1</span></span>
```
PS C:\>Stop-AzDeployment -Name "deployment01"
```

<span data-ttu-id="0d91d-116">此命令會取消目前訂閱範圍中執行中的部署「部署01」。</span><span class="sxs-lookup"><span data-stu-id="0d91d-116">This command cancels a running deployment "deployment01" at the current subscription scope.</span></span>

### <span data-ttu-id="0d91d-117">範例 2</span><span class="sxs-lookup"><span data-stu-id="0d91d-117">Example 2</span></span>
```
PS C:\>Get-AzDeployment -Name "deployment01" | Stop-AzDeployment
```

<span data-ttu-id="0d91d-118">此命令會獲得目前訂閱範圍中的部署「部署01」，並取消它。</span><span class="sxs-lookup"><span data-stu-id="0d91d-118">This command gets the deployment "deployment01" at the current subscription scope and cancels it.</span></span> 

## <span data-ttu-id="0d91d-119">參數</span><span class="sxs-lookup"><span data-stu-id="0d91d-119">PARAMETERS</span></span>

### <span data-ttu-id="0d91d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d91d-120">-DefaultProfile</span></span>
<span data-ttu-id="0d91d-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0d91d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d91d-122">-Id</span><span class="sxs-lookup"><span data-stu-id="0d91d-122">-Id</span></span>
<span data-ttu-id="0d91d-123">部署之完整資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0d91d-123">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="0d91d-124">範例：/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="0d91d-124">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="0d91d-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d91d-125">-InputObject</span></span>
<span data-ttu-id="0d91d-126">部署物件。</span><span class="sxs-lookup"><span data-stu-id="0d91d-126">The deployment object.</span></span>

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

### <span data-ttu-id="0d91d-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="0d91d-127">-Name</span></span>
<span data-ttu-id="0d91d-128">部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d91d-128">The name of the deployment.</span></span>

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

### <span data-ttu-id="0d91d-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0d91d-129">-PassThru</span></span>
<span data-ttu-id="0d91d-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="0d91d-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="0d91d-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="0d91d-131">-Pre</span></span>
<span data-ttu-id="0d91d-132">設定之後，表示當系統自動決定要使用哪個版本時，Cmdlet 應該使用測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="0d91d-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="0d91d-133">-確認</span><span class="sxs-lookup"><span data-stu-id="0d91d-133">-Confirm</span></span>
<span data-ttu-id="0d91d-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0d91d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d91d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d91d-135">-WhatIf</span></span>
<span data-ttu-id="0d91d-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0d91d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d91d-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0d91d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d91d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d91d-138">CommonParameters</span></span>
<span data-ttu-id="0d91d-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0d91d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d91d-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0d91d-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d91d-141">輸入</span><span class="sxs-lookup"><span data-stu-id="0d91d-141">INPUTS</span></span>

### <span data-ttu-id="0d91d-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="0d91d-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="0d91d-143">輸出</span><span class="sxs-lookup"><span data-stu-id="0d91d-143">OUTPUTS</span></span>

### <span data-ttu-id="0d91d-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0d91d-144">System.Boolean</span></span>

## <span data-ttu-id="0d91d-145">筆記</span><span class="sxs-lookup"><span data-stu-id="0d91d-145">NOTES</span></span>

## <span data-ttu-id="0d91d-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="0d91d-146">RELATED LINKS</span></span>
