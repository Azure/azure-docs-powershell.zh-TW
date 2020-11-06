---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/new-azurermdeploymentmanagerservicetopology
schema: 2.0.0
ms.openlocfilehash: d7e3055c6443faa2c85d63e6cfdb611cb7d2eb41
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443232"
---
# <span data-ttu-id="52c68-101">New-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="52c68-101">New-AzureRmDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="52c68-102">摘要</span><span class="sxs-lookup"><span data-stu-id="52c68-102">SYNOPSIS</span></span>
<span data-ttu-id="52c68-103">建立新的服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="52c68-103">Creates a new service topology.</span></span>

## <span data-ttu-id="52c68-104">句法</span><span class="sxs-lookup"><span data-stu-id="52c68-104">SYNTAX</span></span>

```
New-AzureRmDeploymentManagerServiceTopology -ResourceGroupName <String> -Name <String> -Location <String>
 [-ArtifactSourceId <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52c68-105">說明</span><span class="sxs-lookup"><span data-stu-id="52c68-105">DESCRIPTION</span></span>
<span data-ttu-id="52c68-106">**新的-AzureRmDeploymentManagerServiceTopology** Cmdlet 會建立服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="52c68-106">The **New-AzureRmDeploymentManagerServiceTopology** cmdlet creates a service topology.</span></span>

<span data-ttu-id="52c68-107">您可以在本機修改傳回的 ServiceTopology 物件，然後使用 Set-AzureRmDeploymentManagerServiceTopology Cmdlet 將變更套用到拓撲。</span><span class="sxs-lookup"><span data-stu-id="52c68-107">You can modify the returned ServiceTopology object locally, and then apply changes to the topology by using the Set-AzureRmDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="52c68-108">傳回的物件</span><span class="sxs-lookup"><span data-stu-id="52c68-108">The returned object</span></span> 

<span data-ttu-id="52c68-109">傳回的物件有一個 ResourceId 欄位，可以在推出資源中參考，以指出此服務拓撲中宣告的服務會部署在推出中。</span><span class="sxs-lookup"><span data-stu-id="52c68-109">The returned object has a ResourceId field which can be referenced in a rollout resource to indicate that the services declared in this service topology would be deployed in the rollout.</span></span>

## <span data-ttu-id="52c68-110">示例</span><span class="sxs-lookup"><span data-stu-id="52c68-110">EXAMPLES</span></span>

### <span data-ttu-id="52c68-111">範例1</span><span class="sxs-lookup"><span data-stu-id="52c68-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology -Location "Central US" -ArtifactSourceId "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="52c68-112">這個 Cmdlet 會在 [資源] 群組 ContosoResourceGroup 中使用名稱 ContosoServiceTopology，並在 [地區] 的中央位置建立新的服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="52c68-112">This cmdlet creates a new service topology in the resource group ContosoResourceGroup with the name ContosoServiceTopology and in location Central US.</span></span> <span data-ttu-id="52c68-113">專案來源 ResourceId 指出必須從指定的專案來源讀取此拓撲中的服務單元定義所需的專案。</span><span class="sxs-lookup"><span data-stu-id="52c68-113">The artifact source ResourceId indicates that the artifacts required for the service unit definitions in this topology need to be read from the specified artifact source.</span></span>

### <span data-ttu-id="52c68-114">範例2</span><span class="sxs-lookup"><span data-stu-id="52c68-114">Example 2</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology -Location "Central US"
```

<span data-ttu-id="52c68-115">這個 Cmdlet 會在 [資源] 群組 ContosoResourceGroup 中使用名稱 ContosoServiceTopology，並在 [地區] 的中央位置建立新的服務拓撲。</span><span class="sxs-lookup"><span data-stu-id="52c68-115">This cmdlet creates a new service topology in the resource group ContosoResourceGroup with the name ContosoServiceTopology and in location Central US.</span></span> <span data-ttu-id="52c68-116">缺少專案來源參照表示此拓朴中的服務單元定義所需的專案將會以服務單元中的絕對 SAS Uri 提供。</span><span class="sxs-lookup"><span data-stu-id="52c68-116">The absence of an artifact source reference indicates that the artifacts required for the service unit definitions in this topology would be provided as absolute SAS URIs in the service unit.</span></span>

## <span data-ttu-id="52c68-117">參數</span><span class="sxs-lookup"><span data-stu-id="52c68-117">PARAMETERS</span></span>

### <span data-ttu-id="52c68-118">-ArtifactSourceId</span><span class="sxs-lookup"><span data-stu-id="52c68-118">-ArtifactSourceId</span></span>
<span data-ttu-id="52c68-119">專案來源的識別碼，會儲存組成拓撲的專案。</span><span class="sxs-lookup"><span data-stu-id="52c68-119">The identifier of the artifact source, where the artifacts that make up the topology are stored.</span></span>

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

### <span data-ttu-id="52c68-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52c68-120">-DefaultProfile</span></span>
<span data-ttu-id="52c68-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="52c68-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52c68-122">-位置</span><span class="sxs-lookup"><span data-stu-id="52c68-122">-Location</span></span>
<span data-ttu-id="52c68-123">拓朴的位置。</span><span class="sxs-lookup"><span data-stu-id="52c68-123">The location of the topology.</span></span>

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

### <span data-ttu-id="52c68-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="52c68-124">-Name</span></span>
<span data-ttu-id="52c68-125">拓朴的名稱。</span><span class="sxs-lookup"><span data-stu-id="52c68-125">The name of the topology.</span></span>

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

### <span data-ttu-id="52c68-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52c68-126">-ResourceGroupName</span></span>
<span data-ttu-id="52c68-127">[資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="52c68-127">The resource group.</span></span>

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

### <span data-ttu-id="52c68-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="52c68-128">-Tag</span></span>
<span data-ttu-id="52c68-129">代表資源標記的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="52c68-129">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="52c68-130">-確認</span><span class="sxs-lookup"><span data-stu-id="52c68-130">-Confirm</span></span>
<span data-ttu-id="52c68-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="52c68-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52c68-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52c68-132">-WhatIf</span></span>
<span data-ttu-id="52c68-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="52c68-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="52c68-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="52c68-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52c68-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52c68-135">CommonParameters</span></span>
<span data-ttu-id="52c68-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="52c68-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52c68-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="52c68-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52c68-138">輸入</span><span class="sxs-lookup"><span data-stu-id="52c68-138">INPUTS</span></span>

### <span data-ttu-id="52c68-139">所有</span><span class="sxs-lookup"><span data-stu-id="52c68-139">None</span></span>

## <span data-ttu-id="52c68-140">輸出</span><span class="sxs-lookup"><span data-stu-id="52c68-140">OUTPUTS</span></span>

### <span data-ttu-id="52c68-141">PSServiceTopologyResource 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="52c68-141">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="52c68-142">筆記</span><span class="sxs-lookup"><span data-stu-id="52c68-142">NOTES</span></span>

## <span data-ttu-id="52c68-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="52c68-143">RELATED LINKS</span></span>

[<span data-ttu-id="52c68-144">AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="52c68-144">Get-AzureRmDeploymentManagerServiceTopology</span></span>](./Get-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="52c68-145">移除-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="52c68-145">Remove-AzureRmDeploymentManagerServiceTopology</span></span>](./Remove-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="52c68-146">Set-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="52c68-146">Set-AzureRmDeploymentManagerServiceTopology</span></span>](./Set-AzureRmDeploymentManagerServiceTopology.md)