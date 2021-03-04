---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: b10d73e118b590a06c2af5a1755a59d219f9f180
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904450"
---
# <span data-ttu-id="48370-101">Remove-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="48370-101">Remove-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="48370-102">簡介</span><span class="sxs-lookup"><span data-stu-id="48370-102">SYNOPSIS</span></span>
<span data-ttu-id="48370-103">刪除指定的產品來源。</span><span class="sxs-lookup"><span data-stu-id="48370-103">Deletes the specified artifact source.</span></span>

## <span data-ttu-id="48370-104">語法</span><span class="sxs-lookup"><span data-stu-id="48370-104">SYNTAX</span></span>

### <span data-ttu-id="48370-105">互動式 (預設) </span><span class="sxs-lookup"><span data-stu-id="48370-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48370-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="48370-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48370-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="48370-107">InputObject</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48370-108">描述</span><span class="sxs-lookup"><span data-stu-id="48370-108">DESCRIPTION</span></span>
<span data-ttu-id="48370-109">**Remove-AzDeploymentManagerArtifactSource** Cmdlet 會刪除產品來源，請根據其名稱和資源組名來指定產品來源。</span><span class="sxs-lookup"><span data-stu-id="48370-109">The **Remove-AzDeploymentManagerArtifactSource** cmdlet deletes an artifact source Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="48370-110">或者，您也可以提供 ArtifactSource 物件或 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="48370-110">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="48370-111">例子</span><span class="sxs-lookup"><span data-stu-id="48370-111">EXAMPLES</span></span>

### <span data-ttu-id="48370-112">範例 1：刪除產品來源</span><span class="sxs-lookup"><span data-stu-id="48370-112">Example 1: Delete an artifact source</span></span>
### <span data-ttu-id="48370-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="48370-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="48370-114">此命令會刪除 ContosoResourceGroup 中名為 ContosoArtifactSource 的假件來源。</span><span class="sxs-lookup"><span data-stu-id="48370-114">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="48370-115">範例 2：使用資源識別碼刪除產品來源</span><span class="sxs-lookup"><span data-stu-id="48370-115">Example 2: Delete an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="48370-116">此命令會刪除 ContosoResourceGroup 中名為 ContosoArtifactSource 的假件來源。</span><span class="sxs-lookup"><span data-stu-id="48370-116">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="48370-117">範例 3：使用物件刪除產品來源</span><span class="sxs-lookup"><span data-stu-id="48370-117">Example 3: Delete an artifact source using an object</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="48370-118">此命令會刪除其名稱與 ResourceGroup 分別符合其名稱及資源組名稱屬性的$artifactSourceObject來源。</span><span class="sxs-lookup"><span data-stu-id="48370-118">This command deletes an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="48370-119">參數</span><span class="sxs-lookup"><span data-stu-id="48370-119">PARAMETERS</span></span>

### <span data-ttu-id="48370-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48370-120">-DefaultProfile</span></span>
<span data-ttu-id="48370-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="48370-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48370-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48370-122">-InputObject</span></span>
<span data-ttu-id="48370-123">要移除的瑕件來源。</span><span class="sxs-lookup"><span data-stu-id="48370-123">The artifact source to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48370-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="48370-124">-Name</span></span>
<span data-ttu-id="48370-125">產品來源的名稱。</span><span class="sxs-lookup"><span data-stu-id="48370-125">The name of the artifact source.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48370-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="48370-126">-PassThru</span></span>
<span data-ttu-id="48370-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="48370-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="48370-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48370-128">-ResourceGroupName</span></span>
<span data-ttu-id="48370-129">資源群組。</span><span class="sxs-lookup"><span data-stu-id="48370-129">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48370-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="48370-130">-ResourceId</span></span>
<span data-ttu-id="48370-131">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="48370-131">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48370-132">-確認</span><span class="sxs-lookup"><span data-stu-id="48370-132">-Confirm</span></span>
<span data-ttu-id="48370-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="48370-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48370-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48370-134">-WhatIf</span></span>
<span data-ttu-id="48370-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="48370-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48370-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="48370-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48370-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48370-137">CommonParameters</span></span>
<span data-ttu-id="48370-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="48370-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48370-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="48370-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48370-140">輸入</span><span class="sxs-lookup"><span data-stu-id="48370-140">INPUTS</span></span>

### <span data-ttu-id="48370-141">System.String</span><span class="sxs-lookup"><span data-stu-id="48370-141">System.String</span></span>

### <span data-ttu-id="48370-142">Microsoft.Azure.Commands.DeploymentManager.models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="48370-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="48370-143">輸出</span><span class="sxs-lookup"><span data-stu-id="48370-143">OUTPUTS</span></span>

### <span data-ttu-id="48370-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="48370-144">System.Boolean</span></span>

## <span data-ttu-id="48370-145">筆記</span><span class="sxs-lookup"><span data-stu-id="48370-145">NOTES</span></span>

## <span data-ttu-id="48370-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="48370-146">RELATED LINKS</span></span>
