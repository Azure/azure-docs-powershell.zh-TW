---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerartifactsource
schema: 2.0.0
ms.openlocfilehash: baf5059d3a952e90422f3e16d83634291aa87614
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93623228"
---
# <span data-ttu-id="d2375-101">Get-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="d2375-101">Get-AzureRmDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="d2375-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d2375-102">SYNOPSIS</span></span>
<span data-ttu-id="d2375-103">取得專案來源。</span><span class="sxs-lookup"><span data-stu-id="d2375-103">Gets an artifact source.</span></span>

## <span data-ttu-id="d2375-104">句法</span><span class="sxs-lookup"><span data-stu-id="d2375-104">SYNTAX</span></span>

### <span data-ttu-id="d2375-105">互動式 (預設) </span><span class="sxs-lookup"><span data-stu-id="d2375-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerArtifactSource [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2375-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2375-106">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerArtifactSource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d2375-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="d2375-107">InputObject</span></span>
```
Get-AzureRmDeploymentManagerArtifactSource [-ArtifactSource] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2375-108">說明</span><span class="sxs-lookup"><span data-stu-id="d2375-108">DESCRIPTION</span></span>
<span data-ttu-id="d2375-109">**AzureRmDeploymentManagerArtifactSource** Cmdlet 會取得專案來源，並傳回代表該專案來源的物件。</span><span class="sxs-lookup"><span data-stu-id="d2375-109">The **Get-AzureRmDeploymentManagerArtifactSource** cmdlet gets an artifact source, and returns an object that represents that artifact source.</span></span>
<span data-ttu-id="d2375-110">依名稱和資源組名稱指定專案來源。</span><span class="sxs-lookup"><span data-stu-id="d2375-110">Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="d2375-111">或者，您也可以提供 ArtifactSource 物件或 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="d2375-111">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

<span data-ttu-id="d2375-112">您可以在本機修改這個物件，然後使用 Set-AzureRmDeploymentManagerArtifactSource Cmdlet 將變更套用至專案來源。</span><span class="sxs-lookup"><span data-stu-id="d2375-112">You can modify this object locally, and then apply changes to the artifact source by using the Set-AzureRmDeploymentManagerArtifactSource cmdlet.</span></span>

## <span data-ttu-id="d2375-113">示例</span><span class="sxs-lookup"><span data-stu-id="d2375-113">EXAMPLES</span></span>

### <span data-ttu-id="d2375-114">範例1：取得專案來源</span><span class="sxs-lookup"><span data-stu-id="d2375-114">Example 1: Get an artifact source</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="d2375-115">這個命令會在 ContosoResourceGroup 中取得名為 ContosoArtifactSource 的專案來源。</span><span class="sxs-lookup"><span data-stu-id="d2375-115">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="d2375-116">範例2：使用資源識別碼取得專案來源</span><span class="sxs-lookup"><span data-stu-id="d2375-116">Example 2: Get an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="d2375-117">這個命令會在 ContosoResourceGroup 中取得名為 ContosoArtifactSource 的專案來源。</span><span class="sxs-lookup"><span data-stu-id="d2375-117">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="d2375-118">範例3：使用 New-AzureRmDeploymentManagerArtifactSource 傳回的物件取得專案來源</span><span class="sxs-lookup"><span data-stu-id="d2375-118">Example 3: Get an artifact source using an object returned by New-AzureRmDeploymentManagerArtifactSource</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerArtifactSource -ArtifactSource $artifactSourceObject
```

<span data-ttu-id="d2375-119">這個命令會分別取得 name 和 ResourceGroup 與 $artifactSourceObject 之 Name 和 ResourceGroupName 屬性相符的專案來源。</span><span class="sxs-lookup"><span data-stu-id="d2375-119">This command gets an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="d2375-120">參數</span><span class="sxs-lookup"><span data-stu-id="d2375-120">PARAMETERS</span></span>

### <span data-ttu-id="d2375-121">-ArtifactSource</span><span class="sxs-lookup"><span data-stu-id="d2375-121">-ArtifactSource</span></span>
<span data-ttu-id="d2375-122">專案來源物件。</span><span class="sxs-lookup"><span data-stu-id="d2375-122">Artifact Source object.</span></span>

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

### <span data-ttu-id="d2375-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2375-123">-DefaultProfile</span></span>
<span data-ttu-id="d2375-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d2375-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2375-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="d2375-125">-Name</span></span>
<span data-ttu-id="d2375-126">專案來源的名稱。</span><span class="sxs-lookup"><span data-stu-id="d2375-126">The name of the artifact source.</span></span>

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

### <span data-ttu-id="d2375-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2375-127">-ResourceGroupName</span></span>
<span data-ttu-id="d2375-128">[資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="d2375-128">The resource group.</span></span>

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

### <span data-ttu-id="d2375-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2375-129">-ResourceId</span></span>
<span data-ttu-id="d2375-130">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d2375-130">The resource identifier.</span></span>

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

### <span data-ttu-id="d2375-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2375-131">CommonParameters</span></span>
<span data-ttu-id="d2375-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d2375-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2375-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d2375-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2375-134">輸入</span><span class="sxs-lookup"><span data-stu-id="d2375-134">INPUTS</span></span>

### <span data-ttu-id="d2375-135">所有</span><span class="sxs-lookup"><span data-stu-id="d2375-135">None</span></span>

## <span data-ttu-id="d2375-136">輸出</span><span class="sxs-lookup"><span data-stu-id="d2375-136">OUTPUTS</span></span>

### <span data-ttu-id="d2375-137">PSArtifactSource 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="d2375-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="d2375-138">筆記</span><span class="sxs-lookup"><span data-stu-id="d2375-138">NOTES</span></span>

## <span data-ttu-id="d2375-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="d2375-139">RELATED LINKS</span></span>

[<span data-ttu-id="d2375-140">新-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="d2375-140">New-AzureRmDeploymentManagerArtifactSource</span></span>](./New-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="d2375-141">移除-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="d2375-141">Remove-AzureRmDeploymentManagerArtifactSource</span></span>](./Remove-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="d2375-142">Set-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="d2375-142">Set-AzureRmDeploymentManagerArtifactSource</span></span>](./Set-AzureRmDeploymentManagerArtifactSource.md)