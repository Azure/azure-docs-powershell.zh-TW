---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
ms.openlocfilehash: bda1d2e79e7ef67e69d7b425761750a95c2f3777
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435383"
---
# <span data-ttu-id="74a7b-101">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="74a7b-101">Stop-AzTenantDeployment</span></span>

## <span data-ttu-id="74a7b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="74a7b-102">SYNOPSIS</span></span>
<span data-ttu-id="74a7b-103">在租使用者範圍取消正在執行的部署</span><span class="sxs-lookup"><span data-stu-id="74a7b-103">Cancel a running deployment at tenant scope</span></span>

## <span data-ttu-id="74a7b-104">句法</span><span class="sxs-lookup"><span data-stu-id="74a7b-104">SYNTAX</span></span>

### <span data-ttu-id="74a7b-105">StopByDeploymentName (預設) </span><span class="sxs-lookup"><span data-stu-id="74a7b-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzTenantDeployment [-Name] <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74a7b-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="74a7b-106">StopByDeploymentId</span></span>
```
Stop-AzTenantDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74a7b-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="74a7b-107">StopByInputObject</span></span>
```
Stop-AzTenantDeployment -InputObject <PSDeployment> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74a7b-108">說明</span><span class="sxs-lookup"><span data-stu-id="74a7b-108">DESCRIPTION</span></span>
<span data-ttu-id="74a7b-109">**AzTenantDeployment** Cmdlet 會取消已啟動但未在目前租使用者範圍內完成的部署。</span><span class="sxs-lookup"><span data-stu-id="74a7b-109">The **Stop-AzTenantDeployment** cmdlet cancels a deployment that has started but not completed at the current tenant scope.</span></span>
<span data-ttu-id="74a7b-110">若要停止部署，部署必須具有不完整的提供狀態（例如 [提供]），而不是已完成的狀態（例如 [已預配] 或 [未成功]）。</span><span class="sxs-lookup"><span data-stu-id="74a7b-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="74a7b-111">若要在租使用者範圍中建立部署，請使用 New-AzTenantDeployment Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="74a7b-111">To create a deployment at tenant scope, use the New-AzTenantDeployment cmdlet.</span></span>

## <span data-ttu-id="74a7b-112">示例</span><span class="sxs-lookup"><span data-stu-id="74a7b-112">EXAMPLES</span></span>

### <span data-ttu-id="74a7b-113">範例1</span><span class="sxs-lookup"><span data-stu-id="74a7b-113">Example 1</span></span>
```
PS C:\>Stop-AzTenantDeployment -Name "deployment01"
```

<span data-ttu-id="74a7b-114">這個命令會在目前的租使用者範圍中取消正在執行的部署 "deployment01"。</span><span class="sxs-lookup"><span data-stu-id="74a7b-114">This command cancels a running deployment "deployment01" at the current tenant scope.</span></span>

### <span data-ttu-id="74a7b-115">範例2</span><span class="sxs-lookup"><span data-stu-id="74a7b-115">Example 2</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "deployment01" | Stop-AzTenantDeployment
```

<span data-ttu-id="74a7b-116">這個命令會在目前的租使用者範圍中取得部署 "deployment01"，並將它取消。</span><span class="sxs-lookup"><span data-stu-id="74a7b-116">This command gets the deployment "deployment01" at the current tenant scope and cancels it.</span></span> 

## <span data-ttu-id="74a7b-117">參數</span><span class="sxs-lookup"><span data-stu-id="74a7b-117">PARAMETERS</span></span>

### <span data-ttu-id="74a7b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74a7b-118">-DefaultProfile</span></span>
<span data-ttu-id="74a7b-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="74a7b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74a7b-120">-識別碼</span><span class="sxs-lookup"><span data-stu-id="74a7b-120">-Id</span></span>
<span data-ttu-id="74a7b-121">部署的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="74a7b-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="74a7b-122">範例：/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="74a7b-122">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="74a7b-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74a7b-123">-InputObject</span></span>
<span data-ttu-id="74a7b-124">部署物件。</span><span class="sxs-lookup"><span data-stu-id="74a7b-124">The deployment object.</span></span>

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

### <span data-ttu-id="74a7b-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="74a7b-125">-Name</span></span>
<span data-ttu-id="74a7b-126">部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="74a7b-126">The name of the deployment.</span></span>

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

### <span data-ttu-id="74a7b-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74a7b-127">-PassThru</span></span>
<span data-ttu-id="74a7b-128">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="74a7b-128">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="74a7b-129">-預先</span><span class="sxs-lookup"><span data-stu-id="74a7b-129">-Pre</span></span>
<span data-ttu-id="74a7b-130">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="74a7b-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="74a7b-131">-確認</span><span class="sxs-lookup"><span data-stu-id="74a7b-131">-Confirm</span></span>
<span data-ttu-id="74a7b-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="74a7b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74a7b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74a7b-133">-WhatIf</span></span>
<span data-ttu-id="74a7b-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="74a7b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74a7b-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="74a7b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74a7b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74a7b-136">CommonParameters</span></span>
<span data-ttu-id="74a7b-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="74a7b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74a7b-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="74a7b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74a7b-139">輸入</span><span class="sxs-lookup"><span data-stu-id="74a7b-139">INPUTS</span></span>

### <span data-ttu-id="74a7b-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="74a7b-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="74a7b-141">輸出</span><span class="sxs-lookup"><span data-stu-id="74a7b-141">OUTPUTS</span></span>

### <span data-ttu-id="74a7b-142">System.object</span><span class="sxs-lookup"><span data-stu-id="74a7b-142">System.Boolean</span></span>

## <span data-ttu-id="74a7b-143">筆記</span><span class="sxs-lookup"><span data-stu-id="74a7b-143">NOTES</span></span>

## <span data-ttu-id="74a7b-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="74a7b-144">RELATED LINKS</span></span>
