---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/get-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 819fb3427ae59291c6b6d78a9ce93ee4e519ee13
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905514"
---
# <span data-ttu-id="60fe0-101">Get-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="60fe0-101">Get-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="60fe0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="60fe0-102">SYNOPSIS</span></span>

<span data-ttu-id="60fe0-103">獲得產品來源。</span><span class="sxs-lookup"><span data-stu-id="60fe0-103">Gets the Artifact source.</span></span>

## <span data-ttu-id="60fe0-104">語法</span><span class="sxs-lookup"><span data-stu-id="60fe0-104">SYNTAX</span></span>

### <span data-ttu-id="60fe0-105">互動式 (預設) </span><span class="sxs-lookup"><span data-stu-id="60fe0-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60fe0-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="60fe0-106">ResourceId</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="60fe0-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="60fe0-107">InputObject</span></span>
```
Get-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60fe0-108">描述</span><span class="sxs-lookup"><span data-stu-id="60fe0-108">DESCRIPTION</span></span>
<span data-ttu-id="60fe0-109">**Get-AzDeploymentManagerArtifactSource** Cmdlet 會取得一個產品來源，並會返回一個代表該產品來源的物件。</span><span class="sxs-lookup"><span data-stu-id="60fe0-109">The **Get-AzDeploymentManagerArtifactSource** cmdlet gets an artifact source, and returns an object that represents that artifact source.</span></span>
<span data-ttu-id="60fe0-110">根據產品名稱和資源組名指定產品來源。</span><span class="sxs-lookup"><span data-stu-id="60fe0-110">Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="60fe0-111">或者，您也可以提供 ArtifactSource 物件或 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="60fe0-111">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="60fe0-112">例子</span><span class="sxs-lookup"><span data-stu-id="60fe0-112">EXAMPLES</span></span>

### <span data-ttu-id="60fe0-113">範例 1：取得產品來源</span><span class="sxs-lookup"><span data-stu-id="60fe0-113">Example 1: Get an artifact source</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="60fe0-114">此命令在 ContosoResourceGroup 中會獲得名為 ContosoArtifactSource 的假件來源。</span><span class="sxs-lookup"><span data-stu-id="60fe0-114">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="60fe0-115">範例 2：使用資源識別碼取得產品來源</span><span class="sxs-lookup"><span data-stu-id="60fe0-115">Example 2: Get an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="60fe0-116">此命令在 ContosoResourceGroup 中會獲得名為 ContosoArtifactSource 的假件來源。</span><span class="sxs-lookup"><span data-stu-id="60fe0-116">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="60fe0-117">範例 3：使用由 New-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="60fe0-117">Example 3: Get an artifact source using an object returned by New-AzDeploymentManagerArtifactSource</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="60fe0-118">此命令會獲得一個產品來源，其名稱和資源組會分別符合 $artifactSourceObject 名稱及 ResourceGroupName 屬性。</span><span class="sxs-lookup"><span data-stu-id="60fe0-118">This command gets an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="60fe0-119">參數</span><span class="sxs-lookup"><span data-stu-id="60fe0-119">PARAMETERS</span></span>

### <span data-ttu-id="60fe0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60fe0-120">-DefaultProfile</span></span>
<span data-ttu-id="60fe0-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="60fe0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60fe0-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60fe0-122">-InputObject</span></span>
<span data-ttu-id="60fe0-123">產品來源物件。</span><span class="sxs-lookup"><span data-stu-id="60fe0-123">Artifact Source object.</span></span>

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

### <span data-ttu-id="60fe0-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="60fe0-124">-Name</span></span>
<span data-ttu-id="60fe0-125">產品來源的名稱。</span><span class="sxs-lookup"><span data-stu-id="60fe0-125">The name of the artifact source.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60fe0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60fe0-126">-ResourceGroupName</span></span>
<span data-ttu-id="60fe0-127">資源群組。</span><span class="sxs-lookup"><span data-stu-id="60fe0-127">The resource group.</span></span>

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

### <span data-ttu-id="60fe0-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="60fe0-128">-ResourceId</span></span>
<span data-ttu-id="60fe0-129">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="60fe0-129">The resource identifier.</span></span>

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

### <span data-ttu-id="60fe0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60fe0-130">CommonParameters</span></span>
<span data-ttu-id="60fe0-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="60fe0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60fe0-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="60fe0-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60fe0-133">輸入</span><span class="sxs-lookup"><span data-stu-id="60fe0-133">INPUTS</span></span>

### <span data-ttu-id="60fe0-134">System.String</span><span class="sxs-lookup"><span data-stu-id="60fe0-134">System.String</span></span>

### <span data-ttu-id="60fe0-135">Microsoft.Azure.Commands.DeploymentManager.models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="60fe0-135">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="60fe0-136">輸出</span><span class="sxs-lookup"><span data-stu-id="60fe0-136">OUTPUTS</span></span>

### <span data-ttu-id="60fe0-137">Microsoft.Azure.Commands.DeploymentManager.models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="60fe0-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="60fe0-138">筆記</span><span class="sxs-lookup"><span data-stu-id="60fe0-138">NOTES</span></span>

## <span data-ttu-id="60fe0-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="60fe0-139">RELATED LINKS</span></span>
