---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerartifactsource
schema: 2.0.0
ms.openlocfilehash: 7473f125511995efb1f6273d3b8adb675a58d06d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93442500"
---
# <span data-ttu-id="e43dc-101">Remove-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="e43dc-101">Remove-AzureRmDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="e43dc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e43dc-102">SYNOPSIS</span></span>
<span data-ttu-id="e43dc-103">刪除專案來源。</span><span class="sxs-lookup"><span data-stu-id="e43dc-103">Deletes an artifact source.</span></span>

## <span data-ttu-id="e43dc-104">句法</span><span class="sxs-lookup"><span data-stu-id="e43dc-104">SYNTAX</span></span>

### <span data-ttu-id="e43dc-105">互動式 (預設) </span><span class="sxs-lookup"><span data-stu-id="e43dc-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerArtifactSource [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e43dc-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e43dc-106">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerArtifactSource [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e43dc-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="e43dc-107">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerArtifactSource [-ArtifactSource] <PSArtifactSource> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e43dc-108">說明</span><span class="sxs-lookup"><span data-stu-id="e43dc-108">DESCRIPTION</span></span>
<span data-ttu-id="e43dc-109">**AzureRmDeploymentManagerArtifactSource** Cmdlet 會刪除專案來源：依名稱和資源群組名稱指定專案來源。</span><span class="sxs-lookup"><span data-stu-id="e43dc-109">The **Remove-AzureRmDeploymentManagerArtifactSource** cmdlet deletes an artifact source Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="e43dc-110">或者，您也可以提供 ArtifactSource 物件或 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="e43dc-110">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="e43dc-111">示例</span><span class="sxs-lookup"><span data-stu-id="e43dc-111">EXAMPLES</span></span>

### <span data-ttu-id="e43dc-112">範例1：刪除專案來源</span><span class="sxs-lookup"><span data-stu-id="e43dc-112">Example 1: Delete an artifact source</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="e43dc-113">這個命令會在 ContosoResourceGroup 中刪除名為 ContosoArtifactSource 的專案來源。</span><span class="sxs-lookup"><span data-stu-id="e43dc-113">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="e43dc-114">範例2：使用資源識別碼刪除專案來源</span><span class="sxs-lookup"><span data-stu-id="e43dc-114">Example 2: Delete an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="e43dc-115">這個命令會在 ContosoResourceGroup 中刪除名為 ContosoArtifactSource 的專案來源。</span><span class="sxs-lookup"><span data-stu-id="e43dc-115">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="e43dc-116">範例3：使用物件刪除專案來源</span><span class="sxs-lookup"><span data-stu-id="e43dc-116">Example 3: Delete an artifact source using an object</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerArtifactSource -ArtifactSource $artifactSourceObject
```

<span data-ttu-id="e43dc-117">這個命令會分別刪除名稱和 ResourceGroup 與 $artifactSourceObject 的 Name 及 ResourceGroupName 屬性相符的專案來源。</span><span class="sxs-lookup"><span data-stu-id="e43dc-117">This command deletes an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="e43dc-118">參數</span><span class="sxs-lookup"><span data-stu-id="e43dc-118">PARAMETERS</span></span>

### <span data-ttu-id="e43dc-119">-ArtifactSource</span><span class="sxs-lookup"><span data-stu-id="e43dc-119">-ArtifactSource</span></span>
<span data-ttu-id="e43dc-120">要移除的專案存放區。</span><span class="sxs-lookup"><span data-stu-id="e43dc-120">The artifact store to be removed.</span></span>

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

### <span data-ttu-id="e43dc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e43dc-121">-DefaultProfile</span></span>
<span data-ttu-id="e43dc-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e43dc-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e43dc-123">-Force</span><span class="sxs-lookup"><span data-stu-id="e43dc-123">-Force</span></span>
<span data-ttu-id="e43dc-124">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="e43dc-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e43dc-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="e43dc-125">-Name</span></span>
<span data-ttu-id="e43dc-126">專案來源的名稱。</span><span class="sxs-lookup"><span data-stu-id="e43dc-126">The name of the artifact source.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e43dc-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e43dc-127">-PassThru</span></span>
<span data-ttu-id="e43dc-128">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="e43dc-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="e43dc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e43dc-129">-ResourceGroupName</span></span>
<span data-ttu-id="e43dc-130">[資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="e43dc-130">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e43dc-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e43dc-131">-ResourceId</span></span>
<span data-ttu-id="e43dc-132">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e43dc-132">The resource identifier.</span></span>

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

### <span data-ttu-id="e43dc-133">-確認</span><span class="sxs-lookup"><span data-stu-id="e43dc-133">-Confirm</span></span>
<span data-ttu-id="e43dc-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e43dc-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e43dc-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e43dc-135">-WhatIf</span></span>
<span data-ttu-id="e43dc-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e43dc-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e43dc-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e43dc-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e43dc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e43dc-138">CommonParameters</span></span>
<span data-ttu-id="e43dc-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e43dc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e43dc-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e43dc-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e43dc-141">輸入</span><span class="sxs-lookup"><span data-stu-id="e43dc-141">INPUTS</span></span>

### <span data-ttu-id="e43dc-142">PSArtifactSource 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="e43dc-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="e43dc-143">輸出</span><span class="sxs-lookup"><span data-stu-id="e43dc-143">OUTPUTS</span></span>

### <span data-ttu-id="e43dc-144">System.object</span><span class="sxs-lookup"><span data-stu-id="e43dc-144">System.Boolean</span></span>

## <span data-ttu-id="e43dc-145">筆記</span><span class="sxs-lookup"><span data-stu-id="e43dc-145">NOTES</span></span>

## <span data-ttu-id="e43dc-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="e43dc-146">RELATED LINKS</span></span>

[<span data-ttu-id="e43dc-147">新-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="e43dc-147">New-AzureRmDeploymentManagerArtifactSource</span></span>](./New-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="e43dc-148">AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="e43dc-148">Get-AzureRmDeploymentManagerArtifactSource</span></span>](./Get-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="e43dc-149">Set-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="e43dc-149">Set-AzureRmDeploymentManagerArtifactSource</span></span>](./Set-AzureRmDeploymentManagerArtifactSource.md)