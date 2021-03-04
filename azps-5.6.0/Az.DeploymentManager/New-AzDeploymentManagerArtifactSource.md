---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/new-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 8aab061d7f61605273bd7147dc5a85ca45bf8ad0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905502"
---
# <span data-ttu-id="4fa2c-101">New-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="4fa2c-101">New-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="4fa2c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4fa2c-102">SYNOPSIS</span></span>
<span data-ttu-id="4fa2c-103">建立產品來源。</span><span class="sxs-lookup"><span data-stu-id="4fa2c-103">Creates an artifact source.</span></span>

## <span data-ttu-id="4fa2c-104">語法</span><span class="sxs-lookup"><span data-stu-id="4fa2c-104">SYNTAX</span></span>

```
New-AzDeploymentManagerArtifactSource -ResourceGroupName <String> -Name <String> -Location <String>
 -SasUri <String> [-Tag <Hashtable>] [-ArtifactRoot <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fa2c-105">描述</span><span class="sxs-lookup"><span data-stu-id="4fa2c-105">DESCRIPTION</span></span>
<span data-ttu-id="4fa2c-106">**New-AzDeploymentManagerArtifactSource** Cmdlet 會建立一個製作來源。</span><span class="sxs-lookup"><span data-stu-id="4fa2c-106">The **New-AzDeploymentManagerArtifactSource** cmdlet creates an artifact source.</span></span>
<span data-ttu-id="4fa2c-107">指定 *名稱\*\*、ResourceGroupName* 和必要的屬性。</span><span class="sxs-lookup"><span data-stu-id="4fa2c-107">Specify the *Name*, *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="4fa2c-108">您可以在本地修改所返回的物件，然後使用 Cmdlet 將變更Set-AzDeploymentManagerArtifactSource來源。</span><span class="sxs-lookup"><span data-stu-id="4fa2c-108">You can modify the returned object locally and then apply the changes to the artifact source by using the Set-AzDeploymentManagerArtifactSource cmdlet.</span></span>

<span data-ttu-id="4fa2c-109">Cmdlet 會返回一個包含 ResourceId 的 ArtifactSource 物件，可在 New-AzDeploymentManagerServiceTopology Cmdlet 中參照，以便從此位置參照 ServiceUnit 資源 、範本和參數檔案所需的專案。</span><span class="sxs-lookup"><span data-stu-id="4fa2c-109">The cmdlet returns an ArtifactSource object that has a ResourceId which can be referenced in the New-AzDeploymentManagerServiceTopology cmdlet so that artifacts required for a ServiceUnit resource, the Template and Parameters files, can be referenced from this location.</span></span>

## <span data-ttu-id="4fa2c-110">例子</span><span class="sxs-lookup"><span data-stu-id="4fa2c-110">EXAMPLES</span></span>

### <span data-ttu-id="4fa2c-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="4fa2c-111">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerArtifactSource -ResourceGroupName ContosoResourceGroup -Name ContosoArtifactSource -Location "Central US" -SasUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts?sasParameters"
```

<span data-ttu-id="4fa2c-112">在 ContosoResourceGroup 中建立一個產品來源，名稱為 ContosoArtifactSource，而美中地區是資源的位置。</span><span class="sxs-lookup"><span data-stu-id="4fa2c-112">Creates an artifact source in the ContosoResourceGroup with the name ContosoArtifactSource with Central US as the location of the resource.</span></span> <span data-ttu-id="4fa2c-113">SasUri 屬性會提供 Azure 儲存體 SAS Uri 至儲存產品之儲存容器。</span><span class="sxs-lookup"><span data-stu-id="4fa2c-113">The SasUri property provides an Azure Storage SAS Uri to the storage container where the artifacts are stored.</span></span>

## <span data-ttu-id="4fa2c-114">參數</span><span class="sxs-lookup"><span data-stu-id="4fa2c-114">PARAMETERS</span></span>

### <span data-ttu-id="4fa2c-115">-ArtifactRoot</span><span class="sxs-lookup"><span data-stu-id="4fa2c-115">-ArtifactRoot</span></span>
<span data-ttu-id="4fa2c-116">產品儲存容器下的選擇性目錄位移。</span><span class="sxs-lookup"><span data-stu-id="4fa2c-116">The optional directory offset under the storage container for the artifacts.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fa2c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fa2c-117">-DefaultProfile</span></span>
<span data-ttu-id="4fa2c-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4fa2c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fa2c-119">-位置</span><span class="sxs-lookup"><span data-stu-id="4fa2c-119">-Location</span></span>
<span data-ttu-id="4fa2c-120">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="4fa2c-120">The location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fa2c-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="4fa2c-121">-Name</span></span>
<span data-ttu-id="4fa2c-122">產品來源的名稱。</span><span class="sxs-lookup"><span data-stu-id="4fa2c-122">The name of the artifact source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fa2c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fa2c-123">-ResourceGroupName</span></span>
<span data-ttu-id="4fa2c-124">資源群組。</span><span class="sxs-lookup"><span data-stu-id="4fa2c-124">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fa2c-125">-SasUri</span><span class="sxs-lookup"><span data-stu-id="4fa2c-125">-SasUri</span></span>
<span data-ttu-id="4fa2c-126">儲存產品之 Azure 儲存容器的 SAS Uri。</span><span class="sxs-lookup"><span data-stu-id="4fa2c-126">The SAS Uri to the Azure storage container where the artifacts are stored.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fa2c-127">-標記</span><span class="sxs-lookup"><span data-stu-id="4fa2c-127">-Tag</span></span>
<span data-ttu-id="4fa2c-128">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="4fa2c-128">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fa2c-129">-確認</span><span class="sxs-lookup"><span data-stu-id="4fa2c-129">-Confirm</span></span>
<span data-ttu-id="4fa2c-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4fa2c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fa2c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fa2c-131">-WhatIf</span></span>
<span data-ttu-id="4fa2c-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4fa2c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fa2c-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4fa2c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fa2c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fa2c-134">CommonParameters</span></span>
<span data-ttu-id="4fa2c-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4fa2c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fa2c-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4fa2c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fa2c-137">輸入</span><span class="sxs-lookup"><span data-stu-id="4fa2c-137">INPUTS</span></span>

### <span data-ttu-id="4fa2c-138">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="4fa2c-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4fa2c-139">輸出</span><span class="sxs-lookup"><span data-stu-id="4fa2c-139">OUTPUTS</span></span>

### <span data-ttu-id="4fa2c-140">Microsoft.Azure.Commands.DeploymentManager.models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="4fa2c-140">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="4fa2c-141">筆記</span><span class="sxs-lookup"><span data-stu-id="4fa2c-141">NOTES</span></span>

## <span data-ttu-id="4fa2c-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="4fa2c-142">RELATED LINKS</span></span>
