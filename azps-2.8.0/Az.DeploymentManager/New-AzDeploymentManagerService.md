---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerService.md
ms.openlocfilehash: 50708e5faebff03e63b0b6330bac66c2c409adda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612604"
---
# <span data-ttu-id="8847d-101">New-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="8847d-101">New-AzDeploymentManagerService</span></span>

## <span data-ttu-id="8847d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8847d-102">SYNOPSIS</span></span>
<span data-ttu-id="8847d-103">在指定的服務拓朴下建立服務。</span><span class="sxs-lookup"><span data-stu-id="8847d-103">Creates a service under the specified service topology.</span></span>

## <span data-ttu-id="8847d-104">句法</span><span class="sxs-lookup"><span data-stu-id="8847d-104">SYNTAX</span></span>

### <span data-ttu-id="8847d-105">互動式 (預設) </span><span class="sxs-lookup"><span data-stu-id="8847d-105">Interactive (Default)</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String> -Name <String>
 -Location <String> -TargetLocation <String> -TargetSubscriptionId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8847d-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="8847d-106">ByServiceTopologyObject</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> -Name <String> -Location <String>
 -TargetLocation <String> -TargetSubscriptionId <String> [-ServiceTopologyObject] <PSServiceTopologyResource>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8847d-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="8847d-107">ByServiceTopologyResourceId</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> -Name <String> -Location <String>
 -TargetLocation <String> -TargetSubscriptionId <String> [-ServiceTopologyId] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8847d-108">說明</span><span class="sxs-lookup"><span data-stu-id="8847d-108">DESCRIPTION</span></span>
<span data-ttu-id="8847d-109">**新的 AzDeploymentManagerService** Cmdlet 會在服務拓朴下建立服務，並傳回代表該服務的物件。</span><span class="sxs-lookup"><span data-stu-id="8847d-109">The **New-AzDeploymentManagerService** cmdlet creates a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="8847d-110">依其名稱指定服務、服務拓撲結構，以及資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="8847d-110">Specify the service by its name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="8847d-111">Cmdlet 會傳回服務物件。</span><span class="sxs-lookup"><span data-stu-id="8847d-111">The cmdlet returns a Service object.</span></span> <span data-ttu-id="8847d-112">您可以在本機修改這個物件，然後使用 Set-AzDeploymentManagerService Cmdlet 將變更套用至服務。</span><span class="sxs-lookup"><span data-stu-id="8847d-112">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="8847d-113">示例</span><span class="sxs-lookup"><span data-stu-id="8847d-113">EXAMPLES</span></span>

### <span data-ttu-id="8847d-114">範例1</span><span class="sxs-lookup"><span data-stu-id="8847d-114">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1 -Location "Central US" -TargetLocation "East US" -TargetSubscriptionId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="8847d-115">在 [資源群組 ContosoResourceGroup] 中的 [服務拓朴 ContosoServiceTopology] 底下，在 [位置] 中央，建立新的服務與 [名稱 ContosoService1]。</span><span class="sxs-lookup"><span data-stu-id="8847d-115">Creates a new service with name ContosoService1 under service topology ContosoServiceTopology in Resource Group ContosoResourceGroup, in the location Central US.</span></span> <span data-ttu-id="8847d-116">TargetLocation 屬性指明應該將服務 ContosoService1 部署到指定訂閱中的東美國地區。</span><span class="sxs-lookup"><span data-stu-id="8847d-116">The TargetLocation property indicates that the service ContosoService1 should be deployed to the East US region in the subscription specified.</span></span>

## <span data-ttu-id="8847d-117">參數</span><span class="sxs-lookup"><span data-stu-id="8847d-117">PARAMETERS</span></span>

### <span data-ttu-id="8847d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8847d-118">-DefaultProfile</span></span>
<span data-ttu-id="8847d-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8847d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8847d-120">-位置</span><span class="sxs-lookup"><span data-stu-id="8847d-120">-Location</span></span>
<span data-ttu-id="8847d-121">服務資源的位置。</span><span class="sxs-lookup"><span data-stu-id="8847d-121">The location of the service resource.</span></span>

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

### <span data-ttu-id="8847d-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="8847d-122">-Name</span></span>
<span data-ttu-id="8847d-123">服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="8847d-123">The name of the service.</span></span>

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

### <span data-ttu-id="8847d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8847d-124">-ResourceGroupName</span></span>
<span data-ttu-id="8847d-125">[資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="8847d-125">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8847d-126">-ServiceTopologyId</span><span class="sxs-lookup"><span data-stu-id="8847d-126">-ServiceTopologyId</span></span>
<span data-ttu-id="8847d-127">要在其中建立服務的服務拓撲資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8847d-127">The service topology resource identifier in which the service should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceTopologyResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8847d-128">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="8847d-128">-ServiceTopologyName</span></span>
<span data-ttu-id="8847d-129">此服務所屬的服務拓撲的名稱。</span><span class="sxs-lookup"><span data-stu-id="8847d-129">The name of the service topology this service belongs to.</span></span>

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

### <span data-ttu-id="8847d-130">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="8847d-130">-ServiceTopologyObject</span></span>
<span data-ttu-id="8847d-131">應該在其中建立服務的服務拓朴物件。</span><span class="sxs-lookup"><span data-stu-id="8847d-131">The service topology object in which the service should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByServiceTopologyObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8847d-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="8847d-132">-Tag</span></span>
<span data-ttu-id="8847d-133">代表資源標記的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="8847d-133">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8847d-134">-TargetLocation</span><span class="sxs-lookup"><span data-stu-id="8847d-134">-TargetLocation</span></span>
<span data-ttu-id="8847d-135">決定要將服務部署至其中的資源位置。</span><span class="sxs-lookup"><span data-stu-id="8847d-135">Determines the location where resources under the service would be deployed to.</span></span>

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

### <span data-ttu-id="8847d-136">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8847d-136">-TargetSubscriptionId</span></span>
<span data-ttu-id="8847d-137">決定要將服務部署到哪些資源的訂閱。</span><span class="sxs-lookup"><span data-stu-id="8847d-137">Determines the subscription to which resources under the service would be deployed to.</span></span>

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

### <span data-ttu-id="8847d-138">-確認</span><span class="sxs-lookup"><span data-stu-id="8847d-138">-Confirm</span></span>
<span data-ttu-id="8847d-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8847d-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8847d-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8847d-140">-WhatIf</span></span>
<span data-ttu-id="8847d-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8847d-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8847d-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8847d-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8847d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8847d-143">CommonParameters</span></span>
<span data-ttu-id="8847d-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8847d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8847d-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8847d-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8847d-146">輸入</span><span class="sxs-lookup"><span data-stu-id="8847d-146">INPUTS</span></span>

### <span data-ttu-id="8847d-147">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8847d-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8847d-148">輸出</span><span class="sxs-lookup"><span data-stu-id="8847d-148">OUTPUTS</span></span>

### <span data-ttu-id="8847d-149">PSServiceResource 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="8847d-149">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="8847d-150">筆記</span><span class="sxs-lookup"><span data-stu-id="8847d-150">NOTES</span></span>

## <span data-ttu-id="8847d-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="8847d-151">RELATED LINKS</span></span>