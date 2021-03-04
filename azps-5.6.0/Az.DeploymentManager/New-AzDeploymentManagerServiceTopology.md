---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/new-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: d9ce12176517109ab06f756956c886eae2be9685
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909098"
---
# <span data-ttu-id="766dc-101">New-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="766dc-101">New-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="766dc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="766dc-102">SYNOPSIS</span></span>
<span data-ttu-id="766dc-103">建立服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="766dc-103">Creates a service topology.</span></span>

## <span data-ttu-id="766dc-104">語法</span><span class="sxs-lookup"><span data-stu-id="766dc-104">SYNTAX</span></span>

```
New-AzDeploymentManagerServiceTopology -ResourceGroupName <String> -Name <String> -Location <String>
 [-ArtifactSourceId <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="766dc-105">描述</span><span class="sxs-lookup"><span data-stu-id="766dc-105">DESCRIPTION</span></span>
<span data-ttu-id="766dc-106">**New-AzDeploymentManagerServiceTop以 Cmdlet** 建立服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="766dc-106">The **New-AzDeploymentManagerServiceTopology** cmdlet creates a service topology.</span></span>

<span data-ttu-id="766dc-107">您可以在本地修改所返回的 ServiceTopology 物件，然後使用 Cmdlet 將變更Set-AzDeploymentManagerServiceTopology拓撲。</span><span class="sxs-lookup"><span data-stu-id="766dc-107">You can modify the returned ServiceTopology object locally, and then apply changes to the topology by using the Set-AzDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="766dc-108">所返回的物件</span><span class="sxs-lookup"><span data-stu-id="766dc-108">The returned object</span></span> 

<span data-ttu-id="766dc-109">所返回的物件有一個 ResourceId 欄位，可在部署資源中參照，指出在此服務拓撲中宣告的服務會部署在推出中。</span><span class="sxs-lookup"><span data-stu-id="766dc-109">The returned object has a ResourceId field which can be referenced in a rollout resource to indicate that the services declared in this service topology would be deployed in the rollout.</span></span>

## <span data-ttu-id="766dc-110">例子</span><span class="sxs-lookup"><span data-stu-id="766dc-110">EXAMPLES</span></span>

### <span data-ttu-id="766dc-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="766dc-111">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology -Location "Central US" -ArtifactSourceId "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="766dc-112">此 Cmdlet 在資源群組 ContosoResourceGroup 中建立一個新的服務拓撲，名稱為 ContosoServiceTop應，且位於美國中央位置。</span><span class="sxs-lookup"><span data-stu-id="766dc-112">This cmdlet creates a new service topology in the resource group ContosoResourceGroup with the name ContosoServiceTopology and in location Central US.</span></span> <span data-ttu-id="766dc-113">產品來源 ResourceId 指出，此拓撲中服務單位定義所需的專案需要從指定的產品來源讀取。</span><span class="sxs-lookup"><span data-stu-id="766dc-113">The artifact source ResourceId indicates that the artifacts required for the service unit definitions in this topology need to be read from the specified artifact source.</span></span>

### <span data-ttu-id="766dc-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="766dc-114">Example 2</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology -Location "Central US"
```

<span data-ttu-id="766dc-115">此 Cmdlet 在資源群組 ContosoResourceGroup 中建立一個新的服務拓撲，名稱為 ContosoServiceTop應，且位於美國中央位置。</span><span class="sxs-lookup"><span data-stu-id="766dc-115">This cmdlet creates a new service topology in the resource group ContosoResourceGroup with the name ContosoServiceTopology and in location Central US.</span></span> <span data-ttu-id="766dc-116">沒有產品來源參照表示此拓撲中服務單位定義所需的產品會以服務單位中的絕對 SAS URI 提供。</span><span class="sxs-lookup"><span data-stu-id="766dc-116">The absence of an artifact source reference indicates that the artifacts required for the service unit definitions in this topology would be provided as absolute SAS URIs in the service unit.</span></span>

## <span data-ttu-id="766dc-117">參數</span><span class="sxs-lookup"><span data-stu-id="766dc-117">PARAMETERS</span></span>

### <span data-ttu-id="766dc-118">-ArtifactSourceId</span><span class="sxs-lookup"><span data-stu-id="766dc-118">-ArtifactSourceId</span></span>
<span data-ttu-id="766dc-119">產品來源的識別碼，其中儲存了拓撲的瑕件。</span><span class="sxs-lookup"><span data-stu-id="766dc-119">The identifier of the artifact source, where the artifacts that make up the topology are stored.</span></span>

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

### <span data-ttu-id="766dc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="766dc-120">-DefaultProfile</span></span>
<span data-ttu-id="766dc-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="766dc-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="766dc-122">-位置</span><span class="sxs-lookup"><span data-stu-id="766dc-122">-Location</span></span>
<span data-ttu-id="766dc-123">拓撲的位置。</span><span class="sxs-lookup"><span data-stu-id="766dc-123">The location of the topology.</span></span>

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

### <span data-ttu-id="766dc-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="766dc-124">-Name</span></span>
<span data-ttu-id="766dc-125">拓撲的名稱。</span><span class="sxs-lookup"><span data-stu-id="766dc-125">The name of the topology.</span></span>

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

### <span data-ttu-id="766dc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="766dc-126">-ResourceGroupName</span></span>
<span data-ttu-id="766dc-127">資源群組。</span><span class="sxs-lookup"><span data-stu-id="766dc-127">The resource group.</span></span>

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

### <span data-ttu-id="766dc-128">-標記</span><span class="sxs-lookup"><span data-stu-id="766dc-128">-Tag</span></span>
<span data-ttu-id="766dc-129">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="766dc-129">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="766dc-130">-確認</span><span class="sxs-lookup"><span data-stu-id="766dc-130">-Confirm</span></span>
<span data-ttu-id="766dc-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="766dc-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="766dc-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="766dc-132">-WhatIf</span></span>
<span data-ttu-id="766dc-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="766dc-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="766dc-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="766dc-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="766dc-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="766dc-135">CommonParameters</span></span>
<span data-ttu-id="766dc-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="766dc-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="766dc-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="766dc-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="766dc-138">輸入</span><span class="sxs-lookup"><span data-stu-id="766dc-138">INPUTS</span></span>

### <span data-ttu-id="766dc-139">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="766dc-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="766dc-140">輸出</span><span class="sxs-lookup"><span data-stu-id="766dc-140">OUTPUTS</span></span>

### <span data-ttu-id="766dc-141">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopserviceserviceResource</span><span class="sxs-lookup"><span data-stu-id="766dc-141">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="766dc-142">筆記</span><span class="sxs-lookup"><span data-stu-id="766dc-142">NOTES</span></span>

## <span data-ttu-id="766dc-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="766dc-143">RELATED LINKS</span></span>
