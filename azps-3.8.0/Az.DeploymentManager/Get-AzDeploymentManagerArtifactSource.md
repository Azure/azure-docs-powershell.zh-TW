---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 5b330b2f20fb0611d4bfdea37756b4d62e3bbd69
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965852"
---
# <span data-ttu-id="339f3-101">Get-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="339f3-101">Get-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="339f3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="339f3-102">SYNOPSIS</span></span>

<span data-ttu-id="339f3-103">取得專案來源。</span><span class="sxs-lookup"><span data-stu-id="339f3-103">Gets the Artifact source.</span></span>

## <span data-ttu-id="339f3-104">句法</span><span class="sxs-lookup"><span data-stu-id="339f3-104">SYNTAX</span></span>

### <span data-ttu-id="339f3-105">互動式 (預設) </span><span class="sxs-lookup"><span data-stu-id="339f3-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="339f3-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="339f3-106">ResourceId</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="339f3-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="339f3-107">InputObject</span></span>
```
Get-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="339f3-108">說明</span><span class="sxs-lookup"><span data-stu-id="339f3-108">DESCRIPTION</span></span>
<span data-ttu-id="339f3-109">**AzDeploymentManagerArtifactSource** Cmdlet 會取得專案來源，並傳回代表該專案來源的物件。</span><span class="sxs-lookup"><span data-stu-id="339f3-109">The **Get-AzDeploymentManagerArtifactSource** cmdlet gets an artifact source, and returns an object that represents that artifact source.</span></span>
<span data-ttu-id="339f3-110">依名稱和資源組名稱指定專案來源。</span><span class="sxs-lookup"><span data-stu-id="339f3-110">Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="339f3-111">或者，您也可以提供 ArtifactSource 物件或 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="339f3-111">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="339f3-112">示例</span><span class="sxs-lookup"><span data-stu-id="339f3-112">EXAMPLES</span></span>

### <span data-ttu-id="339f3-113">範例1：取得專案來源</span><span class="sxs-lookup"><span data-stu-id="339f3-113">Example 1: Get an artifact source</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="339f3-114">這個命令會在 ContosoResourceGroup 中取得名為 ContosoArtifactSource 的專案來源。</span><span class="sxs-lookup"><span data-stu-id="339f3-114">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="339f3-115">範例2：使用資源識別碼取得專案來源</span><span class="sxs-lookup"><span data-stu-id="339f3-115">Example 2: Get an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="339f3-116">這個命令會在 ContosoResourceGroup 中取得名為 ContosoArtifactSource 的專案來源。</span><span class="sxs-lookup"><span data-stu-id="339f3-116">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="339f3-117">範例3：使用 New-AzDeploymentManagerArtifactSource 傳回的物件取得專案來源</span><span class="sxs-lookup"><span data-stu-id="339f3-117">Example 3: Get an artifact source using an object returned by New-AzDeploymentManagerArtifactSource</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="339f3-118">這個命令會分別取得 name 和 ResourceGroup 與 $artifactSourceObject 之 Name 和 ResourceGroupName 屬性相符的專案來源。</span><span class="sxs-lookup"><span data-stu-id="339f3-118">This command gets an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="339f3-119">參數</span><span class="sxs-lookup"><span data-stu-id="339f3-119">PARAMETERS</span></span>

### <span data-ttu-id="339f3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="339f3-120">-DefaultProfile</span></span>
<span data-ttu-id="339f3-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="339f3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="339f3-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="339f3-122">-InputObject</span></span>
<span data-ttu-id="339f3-123">專案來源物件。</span><span class="sxs-lookup"><span data-stu-id="339f3-123">Artifact Source object.</span></span>

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

### <span data-ttu-id="339f3-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="339f3-124">-Name</span></span>
<span data-ttu-id="339f3-125">專案來源的名稱。</span><span class="sxs-lookup"><span data-stu-id="339f3-125">The name of the artifact source.</span></span>

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

### <span data-ttu-id="339f3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="339f3-126">-ResourceGroupName</span></span>
<span data-ttu-id="339f3-127">[資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="339f3-127">The resource group.</span></span>

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

### <span data-ttu-id="339f3-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="339f3-128">-ResourceId</span></span>
<span data-ttu-id="339f3-129">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="339f3-129">The resource identifier.</span></span>

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

### <span data-ttu-id="339f3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="339f3-130">CommonParameters</span></span>
<span data-ttu-id="339f3-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="339f3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="339f3-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="339f3-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="339f3-133">輸入</span><span class="sxs-lookup"><span data-stu-id="339f3-133">INPUTS</span></span>

### <span data-ttu-id="339f3-134">System.object</span><span class="sxs-lookup"><span data-stu-id="339f3-134">System.String</span></span>

### <span data-ttu-id="339f3-135">PSArtifactSource 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="339f3-135">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="339f3-136">輸出</span><span class="sxs-lookup"><span data-stu-id="339f3-136">OUTPUTS</span></span>

### <span data-ttu-id="339f3-137">PSArtifactSource 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="339f3-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="339f3-138">筆記</span><span class="sxs-lookup"><span data-stu-id="339f3-138">NOTES</span></span>

## <span data-ttu-id="339f3-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="339f3-139">RELATED LINKS</span></span>