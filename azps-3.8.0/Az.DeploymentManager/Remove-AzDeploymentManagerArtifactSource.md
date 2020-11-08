---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: fa9dc4f8234e9c6e709d59f3945b05eeceef4316
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965850"
---
# <span data-ttu-id="14391-101">Remove-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="14391-101">Remove-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="14391-102">摘要</span><span class="sxs-lookup"><span data-stu-id="14391-102">SYNOPSIS</span></span>
<span data-ttu-id="14391-103">刪除指定的專案來源。</span><span class="sxs-lookup"><span data-stu-id="14391-103">Deletes the specified artifact source.</span></span>

## <span data-ttu-id="14391-104">句法</span><span class="sxs-lookup"><span data-stu-id="14391-104">SYNTAX</span></span>

### <span data-ttu-id="14391-105">互動式 (預設) </span><span class="sxs-lookup"><span data-stu-id="14391-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14391-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="14391-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14391-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="14391-107">InputObject</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14391-108">說明</span><span class="sxs-lookup"><span data-stu-id="14391-108">DESCRIPTION</span></span>
<span data-ttu-id="14391-109">**AzDeploymentManagerArtifactSource** Cmdlet 會刪除專案來源：依名稱和資源群組名稱指定專案來源。</span><span class="sxs-lookup"><span data-stu-id="14391-109">The **Remove-AzDeploymentManagerArtifactSource** cmdlet deletes an artifact source Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="14391-110">或者，您也可以提供 ArtifactSource 物件或 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="14391-110">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="14391-111">示例</span><span class="sxs-lookup"><span data-stu-id="14391-111">EXAMPLES</span></span>

### <span data-ttu-id="14391-112">範例1：刪除專案來源</span><span class="sxs-lookup"><span data-stu-id="14391-112">Example 1: Delete an artifact source</span></span>
### <span data-ttu-id="14391-113">範例1</span><span class="sxs-lookup"><span data-stu-id="14391-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="14391-114">這個命令會在 ContosoResourceGroup 中刪除名為 ContosoArtifactSource 的專案來源。</span><span class="sxs-lookup"><span data-stu-id="14391-114">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="14391-115">範例2：使用資源識別碼刪除專案來源</span><span class="sxs-lookup"><span data-stu-id="14391-115">Example 2: Delete an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="14391-116">這個命令會在 ContosoResourceGroup 中刪除名為 ContosoArtifactSource 的專案來源。</span><span class="sxs-lookup"><span data-stu-id="14391-116">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="14391-117">範例3：使用物件刪除專案來源</span><span class="sxs-lookup"><span data-stu-id="14391-117">Example 3: Delete an artifact source using an object</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="14391-118">這個命令會分別刪除名稱和 ResourceGroup 與 $artifactSourceObject 的 Name 及 ResourceGroupName 屬性相符的專案來源。</span><span class="sxs-lookup"><span data-stu-id="14391-118">This command deletes an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="14391-119">參數</span><span class="sxs-lookup"><span data-stu-id="14391-119">PARAMETERS</span></span>

### <span data-ttu-id="14391-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14391-120">-DefaultProfile</span></span>
<span data-ttu-id="14391-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="14391-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14391-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14391-122">-InputObject</span></span>
<span data-ttu-id="14391-123">要移除的專案來源。</span><span class="sxs-lookup"><span data-stu-id="14391-123">The artifact source to be removed.</span></span>

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

### <span data-ttu-id="14391-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="14391-124">-Name</span></span>
<span data-ttu-id="14391-125">專案來源的名稱。</span><span class="sxs-lookup"><span data-stu-id="14391-125">The name of the artifact source.</span></span>

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

### <span data-ttu-id="14391-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="14391-126">-PassThru</span></span>
<span data-ttu-id="14391-127">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="14391-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="14391-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14391-128">-ResourceGroupName</span></span>
<span data-ttu-id="14391-129">[資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="14391-129">The resource group.</span></span>

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

### <span data-ttu-id="14391-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14391-130">-ResourceId</span></span>
<span data-ttu-id="14391-131">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="14391-131">The resource identifier.</span></span>

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

### <span data-ttu-id="14391-132">-確認</span><span class="sxs-lookup"><span data-stu-id="14391-132">-Confirm</span></span>
<span data-ttu-id="14391-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="14391-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14391-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14391-134">-WhatIf</span></span>
<span data-ttu-id="14391-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="14391-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14391-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="14391-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14391-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14391-137">CommonParameters</span></span>
<span data-ttu-id="14391-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="14391-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14391-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="14391-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14391-140">輸入</span><span class="sxs-lookup"><span data-stu-id="14391-140">INPUTS</span></span>

### <span data-ttu-id="14391-141">System.object</span><span class="sxs-lookup"><span data-stu-id="14391-141">System.String</span></span>

### <span data-ttu-id="14391-142">PSArtifactSource 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="14391-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="14391-143">輸出</span><span class="sxs-lookup"><span data-stu-id="14391-143">OUTPUTS</span></span>

### <span data-ttu-id="14391-144">System.object</span><span class="sxs-lookup"><span data-stu-id="14391-144">System.Boolean</span></span>

## <span data-ttu-id="14391-145">筆記</span><span class="sxs-lookup"><span data-stu-id="14391-145">NOTES</span></span>

## <span data-ttu-id="14391-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="14391-146">RELATED LINKS</span></span>