---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTenantDeployment.md
ms.openlocfilehash: 2417e152b2672d70425e5425a29c1901bfa29313
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141267"
---
# <span data-ttu-id="ca9e2-101">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="ca9e2-101">Remove-AzTenantDeployment</span></span>

## <span data-ttu-id="ca9e2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ca9e2-102">SYNOPSIS</span></span>
<span data-ttu-id="ca9e2-103">移除租使用者範圍及任何相關聯作業的部署</span><span class="sxs-lookup"><span data-stu-id="ca9e2-103">Removes a deployment at tenant scope and any associated operations</span></span>

## <span data-ttu-id="ca9e2-104">句法</span><span class="sxs-lookup"><span data-stu-id="ca9e2-104">SYNTAX</span></span>

### <span data-ttu-id="ca9e2-105">RemoveByDeploymentName (預設) </span><span class="sxs-lookup"><span data-stu-id="ca9e2-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzTenantDeployment [-Name] <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca9e2-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="ca9e2-106">RemoveByDeploymentId</span></span>
```
Remove-AzTenantDeployment -Id <String> [-AsJob] [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca9e2-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="ca9e2-107">RemoveByInputObject</span></span>
```
Remove-AzTenantDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca9e2-108">說明</span><span class="sxs-lookup"><span data-stu-id="ca9e2-108">DESCRIPTION</span></span>
<span data-ttu-id="ca9e2-109">**AzTenantDeployment** Cmdlet 會在目前的租使用者範圍及任何相關聯的作業中移除 Azure 部署。</span><span class="sxs-lookup"><span data-stu-id="ca9e2-109">The **Remove-AzTenantDeployment** cmdlet removes an Azure deployment at the current tenant scope and any associated operations.</span></span>

## <span data-ttu-id="ca9e2-110">示例</span><span class="sxs-lookup"><span data-stu-id="ca9e2-110">EXAMPLES</span></span>

### <span data-ttu-id="ca9e2-111">範例1：移除具有指定名稱的部署</span><span class="sxs-lookup"><span data-stu-id="ca9e2-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzTenantDeployment -Name "RolesDeployment"
```

<span data-ttu-id="ca9e2-112">這個命令會在目前的租使用者範圍中移除部署 "RolesDeployment"。</span><span class="sxs-lookup"><span data-stu-id="ca9e2-112">This command removes the deployment "RolesDeployment" at the current tenant scope.</span></span>

### <span data-ttu-id="ca9e2-113">範例2：取得並移除部署</span><span class="sxs-lookup"><span data-stu-id="ca9e2-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "RolesDeployment" | Remove-AzTenantDeployment
```

<span data-ttu-id="ca9e2-114">這個命令會在目前的租使用者範圍中取得部署 "RolesDeployment"，並將它移除。</span><span class="sxs-lookup"><span data-stu-id="ca9e2-114">This command gets the deployment "RolesDeployment" at the current tenant scope and removes it.</span></span>

## <span data-ttu-id="ca9e2-115">參數</span><span class="sxs-lookup"><span data-stu-id="ca9e2-115">PARAMETERS</span></span>

### <span data-ttu-id="ca9e2-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca9e2-116">-AsJob</span></span>
<span data-ttu-id="ca9e2-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca9e2-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ca9e2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca9e2-118">-DefaultProfile</span></span>
<span data-ttu-id="ca9e2-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ca9e2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca9e2-120">-識別碼</span><span class="sxs-lookup"><span data-stu-id="ca9e2-120">-Id</span></span>
<span data-ttu-id="ca9e2-121">部署的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ca9e2-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="ca9e2-122">範例：/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="ca9e2-122">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="ca9e2-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca9e2-123">-InputObject</span></span>
<span data-ttu-id="ca9e2-124">部署物件。</span><span class="sxs-lookup"><span data-stu-id="ca9e2-124">The deployment object.</span></span>

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

### <span data-ttu-id="ca9e2-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="ca9e2-125">-Name</span></span>
<span data-ttu-id="ca9e2-126">部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="ca9e2-126">The name of the deployment.</span></span>

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

### <span data-ttu-id="ca9e2-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca9e2-127">-PassThru</span></span>
<span data-ttu-id="ca9e2-128">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="ca9e2-128">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="ca9e2-129">-預先</span><span class="sxs-lookup"><span data-stu-id="ca9e2-129">-Pre</span></span>
<span data-ttu-id="ca9e2-130">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="ca9e2-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="ca9e2-131">-確認</span><span class="sxs-lookup"><span data-stu-id="ca9e2-131">-Confirm</span></span>
<span data-ttu-id="ca9e2-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ca9e2-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca9e2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca9e2-133">-WhatIf</span></span>
<span data-ttu-id="ca9e2-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ca9e2-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca9e2-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ca9e2-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca9e2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca9e2-136">CommonParameters</span></span>
<span data-ttu-id="ca9e2-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ca9e2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca9e2-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ca9e2-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca9e2-139">輸入</span><span class="sxs-lookup"><span data-stu-id="ca9e2-139">INPUTS</span></span>

### <span data-ttu-id="ca9e2-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="ca9e2-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="ca9e2-141">輸出</span><span class="sxs-lookup"><span data-stu-id="ca9e2-141">OUTPUTS</span></span>

### <span data-ttu-id="ca9e2-142">System.object</span><span class="sxs-lookup"><span data-stu-id="ca9e2-142">System.Boolean</span></span>

## <span data-ttu-id="ca9e2-143">筆記</span><span class="sxs-lookup"><span data-stu-id="ca9e2-143">NOTES</span></span>

## <span data-ttu-id="ca9e2-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="ca9e2-144">RELATED LINKS</span></span>
