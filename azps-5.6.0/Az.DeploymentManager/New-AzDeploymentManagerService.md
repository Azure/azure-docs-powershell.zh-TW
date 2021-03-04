---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/new-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerService.md
ms.openlocfilehash: b9922d84edfbf90e16db1f050ae7abaeef7442a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909102"
---
# <span data-ttu-id="1aa8a-101">New-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="1aa8a-101">New-AzDeploymentManagerService</span></span>

## <span data-ttu-id="1aa8a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1aa8a-102">SYNOPSIS</span></span>
<span data-ttu-id="1aa8a-103">根據指定的服務拓撲建立服務。</span><span class="sxs-lookup"><span data-stu-id="1aa8a-103">Creates a service under the specified service topology.</span></span>

## <span data-ttu-id="1aa8a-104">語法</span><span class="sxs-lookup"><span data-stu-id="1aa8a-104">SYNTAX</span></span>

### <span data-ttu-id="1aa8a-105">互動式 (預設) </span><span class="sxs-lookup"><span data-stu-id="1aa8a-105">Interactive (Default)</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String> -Name <String>
 -Location <String> -TargetLocation <String> -TargetSubscriptionId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1aa8a-106">ByServiceTopserviceObject</span><span class="sxs-lookup"><span data-stu-id="1aa8a-106">ByServiceTopologyObject</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> -Name <String> -Location <String>
 -TargetLocation <String> -TargetSubscriptionId <String> [-ServiceTopologyObject] <PSServiceTopologyResource>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1aa8a-107">ByServiceTopsourceResourceId</span><span class="sxs-lookup"><span data-stu-id="1aa8a-107">ByServiceTopologyResourceId</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> -Name <String> -Location <String>
 -TargetLocation <String> -TargetSubscriptionId <String> [-ServiceTopologyId] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1aa8a-108">描述</span><span class="sxs-lookup"><span data-stu-id="1aa8a-108">DESCRIPTION</span></span>
<span data-ttu-id="1aa8a-109">**New-AzDeploymentManagerService** Cmdlet 會根據服務拓撲建立服務，並返回代表該服務的物件。</span><span class="sxs-lookup"><span data-stu-id="1aa8a-109">The **New-AzDeploymentManagerService** cmdlet creates a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="1aa8a-110">根據服務的名稱、服務拓撲和資源組名來指定服務。</span><span class="sxs-lookup"><span data-stu-id="1aa8a-110">Specify the service by its name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="1aa8a-111">Cmdlet 會返回 Service 物件。</span><span class="sxs-lookup"><span data-stu-id="1aa8a-111">The cmdlet returns a Service object.</span></span> <span data-ttu-id="1aa8a-112">您可以在本地修改此物件，然後使用 Cmdlet 將變更Set-AzDeploymentManagerService服務。</span><span class="sxs-lookup"><span data-stu-id="1aa8a-112">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="1aa8a-113">例子</span><span class="sxs-lookup"><span data-stu-id="1aa8a-113">EXAMPLES</span></span>

### <span data-ttu-id="1aa8a-114">範例 1</span><span class="sxs-lookup"><span data-stu-id="1aa8a-114">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1 -Location "Central US" -TargetLocation "East US" -TargetSubscriptionId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="1aa8a-115">在位於美國中央位置的 Resource Group ContosoResourceGroup 的服務拓撲 ContosoServiceTopsource 中，建立名稱為 ContosoService1 的新服務。</span><span class="sxs-lookup"><span data-stu-id="1aa8a-115">Creates a new service with name ContosoService1 under service topology ContosoServiceTopology in Resource Group ContosoResourceGroup, in the location Central US.</span></span> <span data-ttu-id="1aa8a-116">TargetLocation 屬性工作表示服務 ContosoService1 應部署至指定訂閱中的美國東部地區。</span><span class="sxs-lookup"><span data-stu-id="1aa8a-116">The TargetLocation property indicates that the service ContosoService1 should be deployed to the East US region in the subscription specified.</span></span>

## <span data-ttu-id="1aa8a-117">參數</span><span class="sxs-lookup"><span data-stu-id="1aa8a-117">PARAMETERS</span></span>

### <span data-ttu-id="1aa8a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1aa8a-118">-DefaultProfile</span></span>
<span data-ttu-id="1aa8a-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1aa8a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1aa8a-120">-位置</span><span class="sxs-lookup"><span data-stu-id="1aa8a-120">-Location</span></span>
<span data-ttu-id="1aa8a-121">服務資源的位置。</span><span class="sxs-lookup"><span data-stu-id="1aa8a-121">The location of the service resource.</span></span>

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

### <span data-ttu-id="1aa8a-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="1aa8a-122">-Name</span></span>
<span data-ttu-id="1aa8a-123">服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="1aa8a-123">The name of the service.</span></span>

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

### <span data-ttu-id="1aa8a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1aa8a-124">-ResourceGroupName</span></span>
<span data-ttu-id="1aa8a-125">資源群組。</span><span class="sxs-lookup"><span data-stu-id="1aa8a-125">The resource group.</span></span>

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

### <span data-ttu-id="1aa8a-126">-ServiceTopologyId</span><span class="sxs-lookup"><span data-stu-id="1aa8a-126">-ServiceTopologyId</span></span>
<span data-ttu-id="1aa8a-127">服務應建立的服務拓撲資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1aa8a-127">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="1aa8a-128">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="1aa8a-128">-ServiceTopologyName</span></span>
<span data-ttu-id="1aa8a-129">此服務所屬的服務拓撲名稱。</span><span class="sxs-lookup"><span data-stu-id="1aa8a-129">The name of the service topology this service belongs to.</span></span>

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

### <span data-ttu-id="1aa8a-130">-ServiceTopectObject</span><span class="sxs-lookup"><span data-stu-id="1aa8a-130">-ServiceTopologyObject</span></span>
<span data-ttu-id="1aa8a-131">服務應建立的服務拓撲物件。</span><span class="sxs-lookup"><span data-stu-id="1aa8a-131">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="1aa8a-132">-標記</span><span class="sxs-lookup"><span data-stu-id="1aa8a-132">-Tag</span></span>
<span data-ttu-id="1aa8a-133">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="1aa8a-133">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="1aa8a-134">-TargetLocation</span><span class="sxs-lookup"><span data-stu-id="1aa8a-134">-TargetLocation</span></span>
<span data-ttu-id="1aa8a-135">決定部署服務下資源的位置。</span><span class="sxs-lookup"><span data-stu-id="1aa8a-135">Determines the location where resources under the service would be deployed to.</span></span>

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

### <span data-ttu-id="1aa8a-136">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1aa8a-136">-TargetSubscriptionId</span></span>
<span data-ttu-id="1aa8a-137">決定服務下資源的部署訂閱。</span><span class="sxs-lookup"><span data-stu-id="1aa8a-137">Determines the subscription to which resources under the service would be deployed to.</span></span>

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

### <span data-ttu-id="1aa8a-138">-確認</span><span class="sxs-lookup"><span data-stu-id="1aa8a-138">-Confirm</span></span>
<span data-ttu-id="1aa8a-139">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1aa8a-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1aa8a-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1aa8a-140">-WhatIf</span></span>
<span data-ttu-id="1aa8a-141">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1aa8a-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1aa8a-142">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1aa8a-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1aa8a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1aa8a-143">CommonParameters</span></span>
<span data-ttu-id="1aa8a-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1aa8a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1aa8a-145">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1aa8a-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1aa8a-146">輸入</span><span class="sxs-lookup"><span data-stu-id="1aa8a-146">INPUTS</span></span>

### <span data-ttu-id="1aa8a-147">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="1aa8a-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1aa8a-148">輸出</span><span class="sxs-lookup"><span data-stu-id="1aa8a-148">OUTPUTS</span></span>

### <span data-ttu-id="1aa8a-149">Microsoft.Azure.Commands.DeploymentManager.models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="1aa8a-149">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="1aa8a-150">筆記</span><span class="sxs-lookup"><span data-stu-id="1aa8a-150">NOTES</span></span>

## <span data-ttu-id="1aa8a-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="1aa8a-151">RELATED LINKS</span></span>
