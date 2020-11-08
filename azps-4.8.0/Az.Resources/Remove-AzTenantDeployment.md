---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTenantDeployment.md
ms.openlocfilehash: ae9257860a54943dfe262d1574f834404ae0e3ff
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126877"
---
# <span data-ttu-id="01e8a-101">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="01e8a-101">Remove-AzTenantDeployment</span></span>

## <span data-ttu-id="01e8a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="01e8a-102">SYNOPSIS</span></span>
<span data-ttu-id="01e8a-103">移除租使用者範圍及任何相關聯作業的部署</span><span class="sxs-lookup"><span data-stu-id="01e8a-103">Removes a deployment at tenant scope and any associated operations</span></span>

## <span data-ttu-id="01e8a-104">句法</span><span class="sxs-lookup"><span data-stu-id="01e8a-104">SYNTAX</span></span>

### <span data-ttu-id="01e8a-105">RemoveByDeploymentName (預設) </span><span class="sxs-lookup"><span data-stu-id="01e8a-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzTenantDeployment [-Name] <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01e8a-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="01e8a-106">RemoveByDeploymentId</span></span>
```
Remove-AzTenantDeployment -Id <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01e8a-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="01e8a-107">RemoveByInputObject</span></span>
```
Remove-AzTenantDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01e8a-108">說明</span><span class="sxs-lookup"><span data-stu-id="01e8a-108">DESCRIPTION</span></span>
<span data-ttu-id="01e8a-109">**AzTenantDeployment** Cmdlet 會在目前的租使用者範圍及任何相關聯的作業中移除 Azure 部署。</span><span class="sxs-lookup"><span data-stu-id="01e8a-109">The **Remove-AzTenantDeployment** cmdlet removes an Azure deployment at the current tenant scope and any associated operations.</span></span>

## <span data-ttu-id="01e8a-110">示例</span><span class="sxs-lookup"><span data-stu-id="01e8a-110">EXAMPLES</span></span>

### <span data-ttu-id="01e8a-111">範例1：移除具有指定名稱的部署</span><span class="sxs-lookup"><span data-stu-id="01e8a-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzTenantDeployment -Name "RolesDeployment"
```

<span data-ttu-id="01e8a-112">這個命令會在目前的租使用者範圍中移除部署 "RolesDeployment"。</span><span class="sxs-lookup"><span data-stu-id="01e8a-112">This command removes the deployment "RolesDeployment" at the current tenant scope.</span></span>

### <span data-ttu-id="01e8a-113">範例2：取得並移除部署</span><span class="sxs-lookup"><span data-stu-id="01e8a-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "RolesDeployment" | Remove-AzTenantDeployment
```

<span data-ttu-id="01e8a-114">這個命令會在目前的租使用者範圍中取得部署 "RolesDeployment"，並將它移除。</span><span class="sxs-lookup"><span data-stu-id="01e8a-114">This command gets the deployment "RolesDeployment" at the current tenant scope and removes it.</span></span>

## <span data-ttu-id="01e8a-115">參數</span><span class="sxs-lookup"><span data-stu-id="01e8a-115">PARAMETERS</span></span>

### <span data-ttu-id="01e8a-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="01e8a-116">-ApiVersion</span></span>
<span data-ttu-id="01e8a-117">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="01e8a-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="01e8a-118">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="01e8a-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="01e8a-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="01e8a-119">-AsJob</span></span>
<span data-ttu-id="01e8a-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="01e8a-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="01e8a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01e8a-121">-DefaultProfile</span></span>
<span data-ttu-id="01e8a-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="01e8a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01e8a-123">-識別碼</span><span class="sxs-lookup"><span data-stu-id="01e8a-123">-Id</span></span>
<span data-ttu-id="01e8a-124">部署的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="01e8a-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="01e8a-125">範例：/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="01e8a-125">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01e8a-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01e8a-126">-InputObject</span></span>
<span data-ttu-id="01e8a-127">部署物件。</span><span class="sxs-lookup"><span data-stu-id="01e8a-127">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01e8a-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="01e8a-128">-Name</span></span>
<span data-ttu-id="01e8a-129">部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="01e8a-129">The name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDeploymentName
Aliases: DeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01e8a-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="01e8a-130">-PassThru</span></span>
<span data-ttu-id="01e8a-131">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="01e8a-131">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="01e8a-132">-預先</span><span class="sxs-lookup"><span data-stu-id="01e8a-132">-Pre</span></span>
<span data-ttu-id="01e8a-133">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="01e8a-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="01e8a-134">-確認</span><span class="sxs-lookup"><span data-stu-id="01e8a-134">-Confirm</span></span>
<span data-ttu-id="01e8a-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="01e8a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01e8a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01e8a-136">-WhatIf</span></span>
<span data-ttu-id="01e8a-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="01e8a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01e8a-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="01e8a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01e8a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01e8a-139">CommonParameters</span></span>
<span data-ttu-id="01e8a-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="01e8a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01e8a-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="01e8a-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01e8a-142">輸入</span><span class="sxs-lookup"><span data-stu-id="01e8a-142">INPUTS</span></span>

### <span data-ttu-id="01e8a-143">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="01e8a-143">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="01e8a-144">輸出</span><span class="sxs-lookup"><span data-stu-id="01e8a-144">OUTPUTS</span></span>

### <span data-ttu-id="01e8a-145">System.object</span><span class="sxs-lookup"><span data-stu-id="01e8a-145">System.Boolean</span></span>

## <span data-ttu-id="01e8a-146">筆記</span><span class="sxs-lookup"><span data-stu-id="01e8a-146">NOTES</span></span>

## <span data-ttu-id="01e8a-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="01e8a-147">RELATED LINKS</span></span>
