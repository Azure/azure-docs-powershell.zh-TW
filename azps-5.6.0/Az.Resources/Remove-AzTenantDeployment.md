---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTenantDeployment.md
ms.openlocfilehash: f995050e86189c1b84652895ad0434403c4e86d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908773"
---
# <span data-ttu-id="ea884-101">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="ea884-101">Remove-AzTenantDeployment</span></span>

## <span data-ttu-id="ea884-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ea884-102">SYNOPSIS</span></span>
<span data-ttu-id="ea884-103">移除租使用者範圍和任何相關作業的部署</span><span class="sxs-lookup"><span data-stu-id="ea884-103">Removes a deployment at tenant scope and any associated operations</span></span>

## <span data-ttu-id="ea884-104">語法</span><span class="sxs-lookup"><span data-stu-id="ea884-104">SYNTAX</span></span>

### <span data-ttu-id="ea884-105">RemoveByDeploymentName (預設) </span><span class="sxs-lookup"><span data-stu-id="ea884-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzTenantDeployment [-Name] <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea884-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="ea884-106">RemoveByDeploymentId</span></span>
```
Remove-AzTenantDeployment -Id <String> [-AsJob] [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea884-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="ea884-107">RemoveByInputObject</span></span>
```
Remove-AzTenantDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea884-108">描述</span><span class="sxs-lookup"><span data-stu-id="ea884-108">DESCRIPTION</span></span>
<span data-ttu-id="ea884-109">**Remove-AzTenantDeployment** Cmdlet 會移除目前租使用者範圍和任何相關聯的作業中的 Azure 部署。</span><span class="sxs-lookup"><span data-stu-id="ea884-109">The **Remove-AzTenantDeployment** cmdlet removes an Azure deployment at the current tenant scope and any associated operations.</span></span>

## <span data-ttu-id="ea884-110">例子</span><span class="sxs-lookup"><span data-stu-id="ea884-110">EXAMPLES</span></span>

### <span data-ttu-id="ea884-111">範例 1：移除具有指定名稱的部署</span><span class="sxs-lookup"><span data-stu-id="ea884-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzTenantDeployment -Name "RolesDeployment"
```

<span data-ttu-id="ea884-112">此命令會移除目前租使用者範圍中的部署「RolesDeployment」。</span><span class="sxs-lookup"><span data-stu-id="ea884-112">This command removes the deployment "RolesDeployment" at the current tenant scope.</span></span>

### <span data-ttu-id="ea884-113">範例 2：取得並移除部署</span><span class="sxs-lookup"><span data-stu-id="ea884-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "RolesDeployment" | Remove-AzTenantDeployment
```

<span data-ttu-id="ea884-114">此命令會獲得目前租使用者範圍中的部署「RolesDeployment」，並移除它。</span><span class="sxs-lookup"><span data-stu-id="ea884-114">This command gets the deployment "RolesDeployment" at the current tenant scope and removes it.</span></span>

## <span data-ttu-id="ea884-115">參數</span><span class="sxs-lookup"><span data-stu-id="ea884-115">PARAMETERS</span></span>

### <span data-ttu-id="ea884-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ea884-116">-AsJob</span></span>
<span data-ttu-id="ea884-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ea884-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ea884-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea884-118">-DefaultProfile</span></span>
<span data-ttu-id="ea884-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ea884-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea884-120">-Id</span><span class="sxs-lookup"><span data-stu-id="ea884-120">-Id</span></span>
<span data-ttu-id="ea884-121">部署之完整資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ea884-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="ea884-122">範例：/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="ea884-122">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="ea884-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea884-123">-InputObject</span></span>
<span data-ttu-id="ea884-124">部署物件。</span><span class="sxs-lookup"><span data-stu-id="ea884-124">The deployment object.</span></span>

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

### <span data-ttu-id="ea884-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="ea884-125">-Name</span></span>
<span data-ttu-id="ea884-126">部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="ea884-126">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentName
Aliases: DeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea884-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ea884-127">-PassThru</span></span>
<span data-ttu-id="ea884-128">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="ea884-128">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="ea884-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="ea884-129">-Pre</span></span>
<span data-ttu-id="ea884-130">設定之後，表示當系統自動決定要使用哪個版本時，Cmdlet 應該使用測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="ea884-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="ea884-131">-確認</span><span class="sxs-lookup"><span data-stu-id="ea884-131">-Confirm</span></span>
<span data-ttu-id="ea884-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ea884-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea884-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea884-133">-WhatIf</span></span>
<span data-ttu-id="ea884-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ea884-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea884-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ea884-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea884-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea884-136">CommonParameters</span></span>
<span data-ttu-id="ea884-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ea884-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea884-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ea884-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea884-139">輸入</span><span class="sxs-lookup"><span data-stu-id="ea884-139">INPUTS</span></span>

### <span data-ttu-id="ea884-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="ea884-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="ea884-141">輸出</span><span class="sxs-lookup"><span data-stu-id="ea884-141">OUTPUTS</span></span>

### <span data-ttu-id="ea884-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ea884-142">System.Boolean</span></span>

## <span data-ttu-id="ea884-143">筆記</span><span class="sxs-lookup"><span data-stu-id="ea884-143">NOTES</span></span>

## <span data-ttu-id="ea884-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="ea884-144">RELATED LINKS</span></span>
