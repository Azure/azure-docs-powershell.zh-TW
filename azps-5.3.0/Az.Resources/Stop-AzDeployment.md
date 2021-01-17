---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
ms.openlocfilehash: fd3fc9b254fab2044ad955d7b4aeb43783d5a907
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435386"
---
# <span data-ttu-id="5d4d7-101">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="5d4d7-101">Stop-AzDeployment</span></span>

## <span data-ttu-id="5d4d7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5d4d7-102">SYNOPSIS</span></span>
<span data-ttu-id="5d4d7-103">取消執行中的部署</span><span class="sxs-lookup"><span data-stu-id="5d4d7-103">Cancel a running deployment</span></span>

## <span data-ttu-id="5d4d7-104">句法</span><span class="sxs-lookup"><span data-stu-id="5d4d7-104">SYNTAX</span></span>

### <span data-ttu-id="5d4d7-105">StopByDeploymentName (預設) </span><span class="sxs-lookup"><span data-stu-id="5d4d7-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzDeployment [-Name] <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d4d7-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="5d4d7-106">StopByDeploymentId</span></span>
```
Stop-AzDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d4d7-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="5d4d7-107">StopByInputObject</span></span>
```
Stop-AzDeployment -InputObject <PSDeployment> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d4d7-108">說明</span><span class="sxs-lookup"><span data-stu-id="5d4d7-108">DESCRIPTION</span></span>
<span data-ttu-id="5d4d7-109">**AzDeployment** Cmdlet 會在已開始但尚未完成的訂閱範圍中取消部署。</span><span class="sxs-lookup"><span data-stu-id="5d4d7-109">The **Stop-AzDeployment** cmdlet cancels a deployment at subscription scope that has started but not completed.</span></span>
<span data-ttu-id="5d4d7-110">若要停止部署，部署必須具有不完整的提供狀態（例如 [提供]），而不是已完成的狀態（例如 [已預配] 或 [未成功]）。</span><span class="sxs-lookup"><span data-stu-id="5d4d7-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="5d4d7-111">若要在訂閱範圍建立部署，請使用 New-AzDeployment Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5d4d7-111">To create a deployment at subscription scope, use the New-AzDeployment cmdlet.</span></span>

<span data-ttu-id="5d4d7-112">這個 Cmdlet 只會停止一個正在執行的部署。</span><span class="sxs-lookup"><span data-stu-id="5d4d7-112">This cmdlet stops only one running deployment.</span></span> <span data-ttu-id="5d4d7-113">使用 *Name* 參數停止特定的部署。</span><span class="sxs-lookup"><span data-stu-id="5d4d7-113">Use the *Name* parameter to stop a specific deployment.</span></span>

## <span data-ttu-id="5d4d7-114">示例</span><span class="sxs-lookup"><span data-stu-id="5d4d7-114">EXAMPLES</span></span>

### <span data-ttu-id="5d4d7-115">範例1</span><span class="sxs-lookup"><span data-stu-id="5d4d7-115">Example 1</span></span>
```
PS C:\>Stop-AzDeployment -Name "deployment01"
```

<span data-ttu-id="5d4d7-116">這個命令會在目前的訂閱範圍中取消正在執行的部署 "deployment01"。</span><span class="sxs-lookup"><span data-stu-id="5d4d7-116">This command cancels a running deployment "deployment01" at the current subscription scope.</span></span>

### <span data-ttu-id="5d4d7-117">範例2</span><span class="sxs-lookup"><span data-stu-id="5d4d7-117">Example 2</span></span>
```
PS C:\>Get-AzDeployment -Name "deployment01" | Stop-AzDeployment
```

<span data-ttu-id="5d4d7-118">這個命令會在目前的訂閱範圍中取得部署 "deployment01"，並加以取消。</span><span class="sxs-lookup"><span data-stu-id="5d4d7-118">This command gets the deployment "deployment01" at the current subscription scope and cancels it.</span></span> 

## <span data-ttu-id="5d4d7-119">參數</span><span class="sxs-lookup"><span data-stu-id="5d4d7-119">PARAMETERS</span></span>

### <span data-ttu-id="5d4d7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d4d7-120">-DefaultProfile</span></span>
<span data-ttu-id="5d4d7-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5d4d7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d4d7-122">-識別碼</span><span class="sxs-lookup"><span data-stu-id="5d4d7-122">-Id</span></span>
<span data-ttu-id="5d4d7-123">部署的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="5d4d7-123">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="5d4d7-124">範例：/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="5d4d7-124">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="5d4d7-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d4d7-125">-InputObject</span></span>
<span data-ttu-id="5d4d7-126">部署物件。</span><span class="sxs-lookup"><span data-stu-id="5d4d7-126">The deployment object.</span></span>

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

### <span data-ttu-id="5d4d7-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="5d4d7-127">-Name</span></span>
<span data-ttu-id="5d4d7-128">部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="5d4d7-128">The name of the deployment.</span></span>

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

### <span data-ttu-id="5d4d7-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5d4d7-129">-PassThru</span></span>
<span data-ttu-id="5d4d7-130">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="5d4d7-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="5d4d7-131">-預先</span><span class="sxs-lookup"><span data-stu-id="5d4d7-131">-Pre</span></span>
<span data-ttu-id="5d4d7-132">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="5d4d7-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="5d4d7-133">-確認</span><span class="sxs-lookup"><span data-stu-id="5d4d7-133">-Confirm</span></span>
<span data-ttu-id="5d4d7-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5d4d7-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d4d7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d4d7-135">-WhatIf</span></span>
<span data-ttu-id="5d4d7-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5d4d7-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d4d7-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5d4d7-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d4d7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d4d7-138">CommonParameters</span></span>
<span data-ttu-id="5d4d7-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5d4d7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d4d7-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5d4d7-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d4d7-141">輸入</span><span class="sxs-lookup"><span data-stu-id="5d4d7-141">INPUTS</span></span>

### <span data-ttu-id="5d4d7-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="5d4d7-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="5d4d7-143">輸出</span><span class="sxs-lookup"><span data-stu-id="5d4d7-143">OUTPUTS</span></span>

### <span data-ttu-id="5d4d7-144">System.object</span><span class="sxs-lookup"><span data-stu-id="5d4d7-144">System.Boolean</span></span>

## <span data-ttu-id="5d4d7-145">筆記</span><span class="sxs-lookup"><span data-stu-id="5d4d7-145">NOTES</span></span>

## <span data-ttu-id="5d4d7-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="5d4d7-146">RELATED LINKS</span></span>
