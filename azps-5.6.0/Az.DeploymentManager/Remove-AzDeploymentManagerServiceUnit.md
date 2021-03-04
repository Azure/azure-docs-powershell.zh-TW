---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: db7291f143abc5305f79f6b41310a5526c9fbb3e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905501"
---
# <span data-ttu-id="d8f3c-101">Remove-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="d8f3c-101">Remove-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="d8f3c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d8f3c-102">SYNOPSIS</span></span>
<span data-ttu-id="d8f3c-103">刪除服務單位。</span><span class="sxs-lookup"><span data-stu-id="d8f3c-103">Deletes the service unit.</span></span>

## <span data-ttu-id="d8f3c-104">語法</span><span class="sxs-lookup"><span data-stu-id="d8f3c-104">SYNTAX</span></span>

### <span data-ttu-id="d8f3c-105">互動式 (預設) </span><span class="sxs-lookup"><span data-stu-id="d8f3c-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8f3c-106">ByTopserviceObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="d8f3c-106">ByTopologyObjectAndServiceName</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8f3c-107">ByTopserviceResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="d8f3c-107">ByTopologyResourceAndServiceName</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8f3c-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="d8f3c-108">ByServiceObject</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-Name] <String> [-ServiceObject] <PSServiceResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8f3c-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="d8f3c-109">ByServiceResourceId</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-Name] <String> [-ServiceResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8f3c-110">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d8f3c-110">ResourceId</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8f3c-111">InputObject</span><span class="sxs-lookup"><span data-stu-id="d8f3c-111">InputObject</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8f3c-112">描述</span><span class="sxs-lookup"><span data-stu-id="d8f3c-112">DESCRIPTION</span></span>
<span data-ttu-id="d8f3c-113">**Remove-AzDeploymentManagerServiceUnit** Cmdlet 會刪除服務中的服務單位。</span><span class="sxs-lookup"><span data-stu-id="d8f3c-113">The **Remove-AzDeploymentManagerServiceUnit** cmdlet deletes a service unit in a service.</span></span>

<span data-ttu-id="d8f3c-114">根據服務單位的名稱、定義的服務、服務拓撲名稱和資源組名來指定服務單位。</span><span class="sxs-lookup"><span data-stu-id="d8f3c-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="d8f3c-115">或者，您也可以提供 ServiceUnit 物件或 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="d8f3c-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

## <span data-ttu-id="d8f3c-116">例子</span><span class="sxs-lookup"><span data-stu-id="d8f3c-116">EXAMPLES</span></span>

### <span data-ttu-id="d8f3c-117">範例 1</span><span class="sxs-lookup"><span data-stu-id="d8f3c-117">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="d8f3c-118">此命令會刪除位於 ContosoResourceGroup 中，服務拓撲 ContosoService1 下名為 ContosoService1Storage 的服務單位。</span><span class="sxs-lookup"><span data-stu-id="d8f3c-118">This command deletes a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="d8f3c-119">範例 2：使用資源識別碼刪除服務單位。</span><span class="sxs-lookup"><span data-stu-id="d8f3c-119">Example 2: Delete a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="d8f3c-120">此命令在 ContosoResourceGroup 的服務拓撲 ContosoService1 的服務拓撲下，會獲得名為 ContosoService1Storage 的服務單位。</span><span class="sxs-lookup"><span data-stu-id="d8f3c-120">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="d8f3c-121">範例 3：使用服務單位物件刪除服務單位。</span><span class="sxs-lookup"><span data-stu-id="d8f3c-121">Example 3: Delete a service unit using the service unit object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="d8f3c-122">此命令會刪除服務單位，其名稱、服務名稱、服務拓撲名稱及 ResourceGroup 分別符合服務名稱、ServiceName、ServiceTopologyName 和 ResourceGroupName 屬性$serviceUnitObject。</span><span class="sxs-lookup"><span data-stu-id="d8f3c-122">This command deletes a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="d8f3c-123">參數</span><span class="sxs-lookup"><span data-stu-id="d8f3c-123">PARAMETERS</span></span>

### <span data-ttu-id="d8f3c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8f3c-124">-DefaultProfile</span></span>
<span data-ttu-id="d8f3c-125">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d8f3c-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8f3c-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8f3c-126">-InputObject</span></span>
<span data-ttu-id="d8f3c-127">服務單位資源物件。</span><span class="sxs-lookup"><span data-stu-id="d8f3c-127">Service unit resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8f3c-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="d8f3c-128">-Name</span></span>
<span data-ttu-id="d8f3c-129">服務單位的名稱。</span><span class="sxs-lookup"><span data-stu-id="d8f3c-129">The name of the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName, ByServiceObject, ByServiceResourceId
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8f3c-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d8f3c-130">-PassThru</span></span>
<span data-ttu-id="d8f3c-131">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="d8f3c-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d8f3c-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8f3c-132">-ResourceGroupName</span></span>
<span data-ttu-id="d8f3c-133">資源群組。</span><span class="sxs-lookup"><span data-stu-id="d8f3c-133">The resource group.</span></span>

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

### <span data-ttu-id="d8f3c-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d8f3c-134">-ResourceId</span></span>
<span data-ttu-id="d8f3c-135">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d8f3c-135">The resource identifier.</span></span>

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

### <span data-ttu-id="d8f3c-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d8f3c-136">-ServiceName</span></span>
<span data-ttu-id="d8f3c-137">服務單位的服務名稱是其中一部分。</span><span class="sxs-lookup"><span data-stu-id="d8f3c-137">The name of the service the service unit is part of.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8f3c-138">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="d8f3c-138">-ServiceObject</span></span>
<span data-ttu-id="d8f3c-139">應建立服務單位的服務物件。</span><span class="sxs-lookup"><span data-stu-id="d8f3c-139">The service object in which the service unit should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: ByServiceObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8f3c-140">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="d8f3c-140">-ServiceResourceId</span></span>
<span data-ttu-id="d8f3c-141">應建立服務單位的服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d8f3c-141">The service resource identifier in which the service unit should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8f3c-142">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="d8f3c-142">-ServiceTopologyName</span></span>
<span data-ttu-id="d8f3c-143">服務單元的服務拓撲名稱是其中一部分。</span><span class="sxs-lookup"><span data-stu-id="d8f3c-143">The name of the service topology the service unit is part of.</span></span>

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

### <span data-ttu-id="d8f3c-144">-ServiceTopectObject</span><span class="sxs-lookup"><span data-stu-id="d8f3c-144">-ServiceTopologyObject</span></span>
<span data-ttu-id="d8f3c-145">應建立服務單位的服務拓撲物件。</span><span class="sxs-lookup"><span data-stu-id="d8f3c-145">The service topology object in which the service unit should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByTopologyObjectAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8f3c-146">-ServiceTopsourceResourceId</span><span class="sxs-lookup"><span data-stu-id="d8f3c-146">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="d8f3c-147">應建立服務單位的服務拓撲資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d8f3c-147">The service topology resource identifier in which the service unit should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8f3c-148">-確認</span><span class="sxs-lookup"><span data-stu-id="d8f3c-148">-Confirm</span></span>
<span data-ttu-id="d8f3c-149">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d8f3c-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8f3c-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8f3c-150">-WhatIf</span></span>
<span data-ttu-id="d8f3c-151">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d8f3c-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8f3c-152">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d8f3c-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8f3c-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8f3c-153">CommonParameters</span></span>
<span data-ttu-id="d8f3c-154">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d8f3c-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8f3c-155">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8f3c-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8f3c-156">輸入</span><span class="sxs-lookup"><span data-stu-id="d8f3c-156">INPUTS</span></span>

### <span data-ttu-id="d8f3c-157">System.String</span><span class="sxs-lookup"><span data-stu-id="d8f3c-157">System.String</span></span>

### <span data-ttu-id="d8f3c-158">Microsoft.Azure.Commands.DeploymentManager.models.PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="d8f3c-158">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="d8f3c-159">輸出</span><span class="sxs-lookup"><span data-stu-id="d8f3c-159">OUTPUTS</span></span>

### <span data-ttu-id="d8f3c-160">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d8f3c-160">System.Boolean</span></span>

## <span data-ttu-id="d8f3c-161">筆記</span><span class="sxs-lookup"><span data-stu-id="d8f3c-161">NOTES</span></span>

## <span data-ttu-id="d8f3c-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="d8f3c-162">RELATED LINKS</span></span>
