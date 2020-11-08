---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
ms.openlocfilehash: 8604aa58efff7b6fe7ef6dc931fdcb54b313d634
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957655"
---
# <span data-ttu-id="7671d-101">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="7671d-101">Stop-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="7671d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7671d-102">SYNOPSIS</span></span>
<span data-ttu-id="7671d-103">在管理群組取消執行中的部署</span><span class="sxs-lookup"><span data-stu-id="7671d-103">Cancel a running deployment at a management group</span></span>

## <span data-ttu-id="7671d-104">句法</span><span class="sxs-lookup"><span data-stu-id="7671d-104">SYNTAX</span></span>

### <span data-ttu-id="7671d-105">StopByDeploymentName (預設) </span><span class="sxs-lookup"><span data-stu-id="7671d-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-PassThru]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7671d-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="7671d-106">StopByDeploymentId</span></span>
```
Stop-AzManagementGroupDeployment -Id <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7671d-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="7671d-107">StopByInputObject</span></span>
```
Stop-AzManagementGroupDeployment -InputObject <PSDeployment> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7671d-108">說明</span><span class="sxs-lookup"><span data-stu-id="7671d-108">DESCRIPTION</span></span>
<span data-ttu-id="7671d-109">**AzManagementGroupDeployment** Cmdlet 會取消已啟動但未在管理群組完成的部署。</span><span class="sxs-lookup"><span data-stu-id="7671d-109">The **Stop-AzManagementGroupDeployment** cmdlet cancels a deployment that has started but not completed at a management group.</span></span>
<span data-ttu-id="7671d-110">若要停止部署，部署必須具有不完整的提供狀態（例如 [提供]），而不是已完成的狀態（例如 [已預配] 或 [未成功]）。</span><span class="sxs-lookup"><span data-stu-id="7671d-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="7671d-111">若要在管理群組建立部署，請使用 New-AzManagementGroupDeployment Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7671d-111">To create a deployment at a management group, use the New-AzManagementGroupDeployment cmdlet.</span></span>

## <span data-ttu-id="7671d-112">示例</span><span class="sxs-lookup"><span data-stu-id="7671d-112">EXAMPLES</span></span>

### <span data-ttu-id="7671d-113">範例1</span><span class="sxs-lookup"><span data-stu-id="7671d-113">Example 1</span></span>
```
PS C:\>Stop-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01"
```

<span data-ttu-id="7671d-114">這個命令會在管理群組「myMG」取消執行部署「deployment01」。</span><span class="sxs-lookup"><span data-stu-id="7671d-114">This command cancels a running deployment "deployment01" at the management group "myMG".</span></span>

### <span data-ttu-id="7671d-115">範例2</span><span class="sxs-lookup"><span data-stu-id="7671d-115">Example 2</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01" | Stop-AzManagementGroupDeployment
```

<span data-ttu-id="7671d-116">這個命令會取得管理群組「myMG」的部署「deployment01」，並予以取消。</span><span class="sxs-lookup"><span data-stu-id="7671d-116">This command gets the deployment "deployment01" at the management group "myMG" and cancels it.</span></span> 

## <span data-ttu-id="7671d-117">參數</span><span class="sxs-lookup"><span data-stu-id="7671d-117">PARAMETERS</span></span>

### <span data-ttu-id="7671d-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7671d-118">-ApiVersion</span></span>
<span data-ttu-id="7671d-119">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="7671d-119">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="7671d-120">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="7671d-120">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7671d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7671d-121">-DefaultProfile</span></span>
<span data-ttu-id="7671d-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7671d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7671d-123">-識別碼</span><span class="sxs-lookup"><span data-stu-id="7671d-123">-Id</span></span>
<span data-ttu-id="7671d-124">部署的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="7671d-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="7671d-125">範例：/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="7671d-125">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: StopByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7671d-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7671d-126">-InputObject</span></span>
<span data-ttu-id="7671d-127">部署物件。</span><span class="sxs-lookup"><span data-stu-id="7671d-127">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: StopByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7671d-128">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="7671d-128">-ManagementGroupId</span></span>
<span data-ttu-id="7671d-129">管理群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="7671d-129">The management group id.</span></span>

```yaml
Type: String
Parameter Sets: StopByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7671d-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="7671d-130">-Name</span></span>
<span data-ttu-id="7671d-131">部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="7671d-131">The name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: StopByDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7671d-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7671d-132">-PassThru</span></span>
<span data-ttu-id="7671d-133">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="7671d-133">{{ Fill PassThru Description }}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7671d-134">-預先</span><span class="sxs-lookup"><span data-stu-id="7671d-134">-Pre</span></span>
<span data-ttu-id="7671d-135">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="7671d-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7671d-136">-確認</span><span class="sxs-lookup"><span data-stu-id="7671d-136">-Confirm</span></span>
<span data-ttu-id="7671d-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7671d-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7671d-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7671d-138">-WhatIf</span></span>
<span data-ttu-id="7671d-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7671d-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7671d-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7671d-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7671d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7671d-141">CommonParameters</span></span>
<span data-ttu-id="7671d-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7671d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7671d-143">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7671d-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7671d-144">輸入</span><span class="sxs-lookup"><span data-stu-id="7671d-144">INPUTS</span></span>

### <span data-ttu-id="7671d-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="7671d-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="7671d-146">輸出</span><span class="sxs-lookup"><span data-stu-id="7671d-146">OUTPUTS</span></span>

### <span data-ttu-id="7671d-147">System.object</span><span class="sxs-lookup"><span data-stu-id="7671d-147">System.Boolean</span></span>

## <span data-ttu-id="7671d-148">筆記</span><span class="sxs-lookup"><span data-stu-id="7671d-148">NOTES</span></span>

## <span data-ttu-id="7671d-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="7671d-149">RELATED LINKS</span></span>