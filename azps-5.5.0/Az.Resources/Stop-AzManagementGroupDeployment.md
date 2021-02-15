---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
ms.openlocfilehash: 96c4f9147875198716d530ee065177472233e465
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142576"
---
# <span data-ttu-id="1bbef-101">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1bbef-101">Stop-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="1bbef-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1bbef-102">SYNOPSIS</span></span>
<span data-ttu-id="1bbef-103">在管理群組取消執行中的部署</span><span class="sxs-lookup"><span data-stu-id="1bbef-103">Cancel a running deployment at a management group</span></span>

## <span data-ttu-id="1bbef-104">句法</span><span class="sxs-lookup"><span data-stu-id="1bbef-104">SYNTAX</span></span>

### <span data-ttu-id="1bbef-105">StopByDeploymentName (預設) </span><span class="sxs-lookup"><span data-stu-id="1bbef-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bbef-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="1bbef-106">StopByDeploymentId</span></span>
```
Stop-AzManagementGroupDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bbef-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="1bbef-107">StopByInputObject</span></span>
```
Stop-AzManagementGroupDeployment -InputObject <PSDeployment> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bbef-108">說明</span><span class="sxs-lookup"><span data-stu-id="1bbef-108">DESCRIPTION</span></span>
<span data-ttu-id="1bbef-109">**AzManagementGroupDeployment** Cmdlet 會取消已啟動但未在管理群組完成的部署。</span><span class="sxs-lookup"><span data-stu-id="1bbef-109">The **Stop-AzManagementGroupDeployment** cmdlet cancels a deployment that has started but not completed at a management group.</span></span>
<span data-ttu-id="1bbef-110">若要停止部署，部署必須具有不完整的提供狀態（例如 [提供]），而不是已完成的狀態（例如 [已預配] 或 [未成功]）。</span><span class="sxs-lookup"><span data-stu-id="1bbef-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="1bbef-111">若要在管理群組建立部署，請使用 New-AzManagementGroupDeployment Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1bbef-111">To create a deployment at a management group, use the New-AzManagementGroupDeployment cmdlet.</span></span>

## <span data-ttu-id="1bbef-112">示例</span><span class="sxs-lookup"><span data-stu-id="1bbef-112">EXAMPLES</span></span>

### <span data-ttu-id="1bbef-113">範例1</span><span class="sxs-lookup"><span data-stu-id="1bbef-113">Example 1</span></span>
```
PS C:\>Stop-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01"
```

<span data-ttu-id="1bbef-114">這個命令會在管理群組「myMG」取消執行部署「deployment01」。</span><span class="sxs-lookup"><span data-stu-id="1bbef-114">This command cancels a running deployment "deployment01" at the management group "myMG".</span></span>

### <span data-ttu-id="1bbef-115">範例2</span><span class="sxs-lookup"><span data-stu-id="1bbef-115">Example 2</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01" | Stop-AzManagementGroupDeployment
```

<span data-ttu-id="1bbef-116">這個命令會取得管理群組「myMG」的部署「deployment01」，並予以取消。</span><span class="sxs-lookup"><span data-stu-id="1bbef-116">This command gets the deployment "deployment01" at the management group "myMG" and cancels it.</span></span> 

## <span data-ttu-id="1bbef-117">參數</span><span class="sxs-lookup"><span data-stu-id="1bbef-117">PARAMETERS</span></span>

### <span data-ttu-id="1bbef-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bbef-118">-DefaultProfile</span></span>
<span data-ttu-id="1bbef-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1bbef-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1bbef-120">-識別碼</span><span class="sxs-lookup"><span data-stu-id="1bbef-120">-Id</span></span>
<span data-ttu-id="1bbef-121">部署的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1bbef-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="1bbef-122">範例：/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="1bbef-122">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="1bbef-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1bbef-123">-InputObject</span></span>
<span data-ttu-id="1bbef-124">部署物件。</span><span class="sxs-lookup"><span data-stu-id="1bbef-124">The deployment object.</span></span>

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

### <span data-ttu-id="1bbef-125">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="1bbef-125">-ManagementGroupId</span></span>
<span data-ttu-id="1bbef-126">管理群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="1bbef-126">The management group id.</span></span>

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

### <span data-ttu-id="1bbef-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="1bbef-127">-Name</span></span>
<span data-ttu-id="1bbef-128">部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="1bbef-128">The name of the deployment.</span></span>

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

### <span data-ttu-id="1bbef-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1bbef-129">-PassThru</span></span>
<span data-ttu-id="1bbef-130">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="1bbef-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="1bbef-131">-預先</span><span class="sxs-lookup"><span data-stu-id="1bbef-131">-Pre</span></span>
<span data-ttu-id="1bbef-132">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="1bbef-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="1bbef-133">-確認</span><span class="sxs-lookup"><span data-stu-id="1bbef-133">-Confirm</span></span>
<span data-ttu-id="1bbef-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1bbef-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bbef-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bbef-135">-WhatIf</span></span>
<span data-ttu-id="1bbef-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1bbef-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bbef-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1bbef-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bbef-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bbef-138">CommonParameters</span></span>
<span data-ttu-id="1bbef-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1bbef-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bbef-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1bbef-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bbef-141">輸入</span><span class="sxs-lookup"><span data-stu-id="1bbef-141">INPUTS</span></span>

### <span data-ttu-id="1bbef-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="1bbef-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="1bbef-143">輸出</span><span class="sxs-lookup"><span data-stu-id="1bbef-143">OUTPUTS</span></span>

### <span data-ttu-id="1bbef-144">System.object</span><span class="sxs-lookup"><span data-stu-id="1bbef-144">System.Boolean</span></span>

## <span data-ttu-id="1bbef-145">筆記</span><span class="sxs-lookup"><span data-stu-id="1bbef-145">NOTES</span></span>

## <span data-ttu-id="1bbef-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="1bbef-146">RELATED LINKS</span></span>
