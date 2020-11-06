---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerservice
schema: 2.0.0
ms.openlocfilehash: 4b2cd4ef2dde674b10d51dc378578acbd13c4a7b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93442496"
---
# <span data-ttu-id="8399d-101">Remove-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="8399d-101">Remove-AzureRmDeploymentManagerService</span></span>

## <span data-ttu-id="8399d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8399d-102">SYNOPSIS</span></span>
<span data-ttu-id="8399d-103">刪除服務拓朴中的服務。</span><span class="sxs-lookup"><span data-stu-id="8399d-103">Deletes a service in a service topology.</span></span>

## <span data-ttu-id="8399d-104">句法</span><span class="sxs-lookup"><span data-stu-id="8399d-104">SYNTAX</span></span>

### <span data-ttu-id="8399d-105">互動式 (預設) </span><span class="sxs-lookup"><span data-stu-id="8399d-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8399d-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="8399d-106">ByServiceTopologyObject</span></span>
```
Remove-AzureRmDeploymentManagerService [-Name] <String> [-ServiceTopology] <PSServiceTopologyResource> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8399d-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="8399d-107">ByServiceTopologyResourceId</span></span>
```
Remove-AzureRmDeploymentManagerService [-Name] <String> [-ServiceTopologyResourceId] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8399d-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8399d-108">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerService [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8399d-109">InputObject</span><span class="sxs-lookup"><span data-stu-id="8399d-109">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerService [-Service] <PSServiceResource> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8399d-110">說明</span><span class="sxs-lookup"><span data-stu-id="8399d-110">DESCRIPTION</span></span>
<span data-ttu-id="8399d-111">**AzureRmDeploymentManagerService** Cmdlet 會刪除服務拓朴下的服務。</span><span class="sxs-lookup"><span data-stu-id="8399d-111">The **Remove-AzureRmDeploymentManagerService** cmdlet deletes a service under a service topology.</span></span>
<span data-ttu-id="8399d-112">依其名稱指定服務、服務拓撲結構，以及資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="8399d-112">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="8399d-113">或者，您也可以提供服務物件或 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="8399d-113">Alternately, you can provide the Service object or the ResourceId.</span></span>

## <span data-ttu-id="8399d-114">示例</span><span class="sxs-lookup"><span data-stu-id="8399d-114">EXAMPLES</span></span>

### <span data-ttu-id="8399d-115">範例1</span><span class="sxs-lookup"><span data-stu-id="8399d-115">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="8399d-116">這個命令會在 ContosoResourceGroup 中名為 ContosoServiceTopology 的服務拓撲中，刪除名為 ContosoService1 的服務。</span><span class="sxs-lookup"><span data-stu-id="8399d-116">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="8399d-117">範例2：使用資源識別碼刪除服務。</span><span class="sxs-lookup"><span data-stu-id="8399d-117">Example 2: Delete a service using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="8399d-118">這個命令會在 ContosoResourceGroup 中名為 ContosoServiceTopology 的服務拓撲中，刪除名為 ContosoService1 的服務。</span><span class="sxs-lookup"><span data-stu-id="8399d-118">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="8399d-119">範例3：使用服務物件刪除服務。</span><span class="sxs-lookup"><span data-stu-id="8399d-119">Example 3: Delete a service using the service object.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerService -Service $serviceObject
```

<span data-ttu-id="8399d-120">這個命令會分別刪除名稱、服務拓朴名稱和 ResourceGroup 與 $serviceObject 的名稱、ServiceTopologyName 及 ResourceGroupName 屬性相符的服務。</span><span class="sxs-lookup"><span data-stu-id="8399d-120">This command deletes a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>

## <span data-ttu-id="8399d-121">參數</span><span class="sxs-lookup"><span data-stu-id="8399d-121">PARAMETERS</span></span>

### <span data-ttu-id="8399d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8399d-122">-DefaultProfile</span></span>
<span data-ttu-id="8399d-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8399d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8399d-124">-Force</span><span class="sxs-lookup"><span data-stu-id="8399d-124">-Force</span></span>
<span data-ttu-id="8399d-125">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="8399d-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8399d-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="8399d-126">-Name</span></span>
<span data-ttu-id="8399d-127">服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="8399d-127">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8399d-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8399d-128">-PassThru</span></span>
<span data-ttu-id="8399d-129">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="8399d-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="8399d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8399d-130">-ResourceGroupName</span></span>
<span data-ttu-id="8399d-131">[資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="8399d-131">The resource group.</span></span>

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

### <span data-ttu-id="8399d-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8399d-132">-ResourceId</span></span>
<span data-ttu-id="8399d-133">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8399d-133">The resource identifier.</span></span>

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

### <span data-ttu-id="8399d-134">-服務</span><span class="sxs-lookup"><span data-stu-id="8399d-134">-Service</span></span>
<span data-ttu-id="8399d-135">要移除的資源。</span><span class="sxs-lookup"><span data-stu-id="8399d-135">The resource to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8399d-136">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="8399d-136">-ServiceTopology</span></span>
<span data-ttu-id="8399d-137">應該在其中建立服務的服務拓朴物件。</span><span class="sxs-lookup"><span data-stu-id="8399d-137">The service topology object in which the service should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByServiceTopologyObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8399d-138">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="8399d-138">-ServiceTopologyName</span></span>
<span data-ttu-id="8399d-139">服務所屬之服務拓撲的名稱。</span><span class="sxs-lookup"><span data-stu-id="8399d-139">The name of the service topology the service belongs to.</span></span>

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

### <span data-ttu-id="8399d-140">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="8399d-140">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="8399d-141">要在其中建立服務的服務拓撲資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8399d-141">The service topology resource identifier in which the service should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceTopologyResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8399d-142">-確認</span><span class="sxs-lookup"><span data-stu-id="8399d-142">-Confirm</span></span>
<span data-ttu-id="8399d-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8399d-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8399d-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8399d-144">-WhatIf</span></span>
<span data-ttu-id="8399d-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8399d-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8399d-146">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8399d-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8399d-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8399d-147">CommonParameters</span></span>
<span data-ttu-id="8399d-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8399d-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8399d-149">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8399d-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8399d-150">輸入</span><span class="sxs-lookup"><span data-stu-id="8399d-150">INPUTS</span></span>

### <span data-ttu-id="8399d-151">PSServiceResource 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="8399d-151">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="8399d-152">輸出</span><span class="sxs-lookup"><span data-stu-id="8399d-152">OUTPUTS</span></span>

### <span data-ttu-id="8399d-153">System.object</span><span class="sxs-lookup"><span data-stu-id="8399d-153">System.Boolean</span></span>

## <span data-ttu-id="8399d-154">筆記</span><span class="sxs-lookup"><span data-stu-id="8399d-154">NOTES</span></span>

## <span data-ttu-id="8399d-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="8399d-155">RELATED LINKS</span></span>

[<span data-ttu-id="8399d-156">新-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="8399d-156">New-AzureRmDeploymentManagerService</span></span>](./New-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="8399d-157">AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="8399d-157">Get-AzureRmDeploymentManagerService</span></span>](./Get-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="8399d-158">Set-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="8399d-158">Set-AzureRmDeploymentManagerService</span></span>](./Set-AzureRmDeploymentManagerService.md)