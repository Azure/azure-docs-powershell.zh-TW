---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
ms.openlocfilehash: 06f3dec483c2c8b5e1730cb1046f927d6d38a7f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905845"
---
# <span data-ttu-id="2432a-101">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2432a-101">Remove-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="2432a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2432a-102">SYNOPSIS</span></span>
<span data-ttu-id="2432a-103">移除管理群組的部署以及任何相關聯的作業</span><span class="sxs-lookup"><span data-stu-id="2432a-103">Removes a deployment at a management group and any associated operations</span></span>

## <span data-ttu-id="2432a-104">語法</span><span class="sxs-lookup"><span data-stu-id="2432a-104">SYNTAX</span></span>

### <span data-ttu-id="2432a-105">RemoveByDeploymentName (預設) </span><span class="sxs-lookup"><span data-stu-id="2432a-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2432a-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="2432a-106">RemoveByDeploymentId</span></span>
```
Remove-AzManagementGroupDeployment -Id <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2432a-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="2432a-107">RemoveByInputObject</span></span>
```
Remove-AzManagementGroupDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2432a-108">描述</span><span class="sxs-lookup"><span data-stu-id="2432a-108">DESCRIPTION</span></span>
<span data-ttu-id="2432a-109">**Remove-AzManagementGroupDeployment** Cmdlet 會移除管理群組的 Azure 部署以及任何相關聯的作業。</span><span class="sxs-lookup"><span data-stu-id="2432a-109">The **Remove-AzManagementGroupDeployment** cmdlet removes an Azure deployment at a management group and any associated operations.</span></span>

## <span data-ttu-id="2432a-110">例子</span><span class="sxs-lookup"><span data-stu-id="2432a-110">EXAMPLES</span></span>

### <span data-ttu-id="2432a-111">範例 1：移除具有指定名稱的部署</span><span class="sxs-lookup"><span data-stu-id="2432a-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment"
```

<span data-ttu-id="2432a-112">此命令會移除管理群組 「myMG」的部署「RolesDeployment」。</span><span class="sxs-lookup"><span data-stu-id="2432a-112">This command removes the deployment "RolesDeployment" at the management group "myMG".</span></span>

### <span data-ttu-id="2432a-113">範例 2：取得並移除部署</span><span class="sxs-lookup"><span data-stu-id="2432a-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment" | Remove-AzManagementGroupDeployment
```

<span data-ttu-id="2432a-114">此命令會獲得管理群組 「myMG」的部署「RolesDeployment」，並移除它。</span><span class="sxs-lookup"><span data-stu-id="2432a-114">This command gets the deployment "RolesDeployment" at the management group "myMG" and removes it.</span></span>

## <span data-ttu-id="2432a-115">參數</span><span class="sxs-lookup"><span data-stu-id="2432a-115">PARAMETERS</span></span>

### <span data-ttu-id="2432a-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2432a-116">-AsJob</span></span>
<span data-ttu-id="2432a-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2432a-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2432a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2432a-118">-DefaultProfile</span></span>
<span data-ttu-id="2432a-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2432a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2432a-120">-Id</span><span class="sxs-lookup"><span data-stu-id="2432a-120">-Id</span></span>
<span data-ttu-id="2432a-121">部署之完整資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="2432a-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="2432a-122">範例：/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="2432a-122">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2432a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2432a-123">-InputObject</span></span>
<span data-ttu-id="2432a-124">部署物件。</span><span class="sxs-lookup"><span data-stu-id="2432a-124">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2432a-125">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="2432a-125">-ManagementGroupId</span></span>
<span data-ttu-id="2432a-126">管理群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="2432a-126">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2432a-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="2432a-127">-Name</span></span>
<span data-ttu-id="2432a-128">部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="2432a-128">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2432a-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2432a-129">-PassThru</span></span>
<span data-ttu-id="2432a-130">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="2432a-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="2432a-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="2432a-131">-Pre</span></span>
<span data-ttu-id="2432a-132">設定之後，表示當系統自動決定要使用哪個版本時，Cmdlet 應該使用測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="2432a-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="2432a-133">-確認</span><span class="sxs-lookup"><span data-stu-id="2432a-133">-Confirm</span></span>
<span data-ttu-id="2432a-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2432a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2432a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2432a-135">-WhatIf</span></span>
<span data-ttu-id="2432a-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2432a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2432a-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2432a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2432a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2432a-138">CommonParameters</span></span>
<span data-ttu-id="2432a-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2432a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2432a-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2432a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2432a-141">輸入</span><span class="sxs-lookup"><span data-stu-id="2432a-141">INPUTS</span></span>

### <span data-ttu-id="2432a-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="2432a-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="2432a-143">輸出</span><span class="sxs-lookup"><span data-stu-id="2432a-143">OUTPUTS</span></span>

### <span data-ttu-id="2432a-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2432a-144">System.Boolean</span></span>

## <span data-ttu-id="2432a-145">筆記</span><span class="sxs-lookup"><span data-stu-id="2432a-145">NOTES</span></span>

## <span data-ttu-id="2432a-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="2432a-146">RELATED LINKS</span></span>
