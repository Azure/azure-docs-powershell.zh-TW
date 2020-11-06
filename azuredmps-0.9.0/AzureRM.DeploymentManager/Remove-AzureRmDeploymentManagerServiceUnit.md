---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerserviceunit
schema: 2.0.0
ms.openlocfilehash: 993b250b0c49efc448c0198c4e9a3aea29f77714
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443275"
---
# <span data-ttu-id="69b2d-101">Remove-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="69b2d-101">Remove-AzureRmDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="69b2d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="69b2d-102">SYNOPSIS</span></span>
<span data-ttu-id="69b2d-103">刪除服務拓朴中服務的服務單元。</span><span class="sxs-lookup"><span data-stu-id="69b2d-103">Deletes the service unit of a service in a service topology.</span></span>

## <span data-ttu-id="69b2d-104">句法</span><span class="sxs-lookup"><span data-stu-id="69b2d-104">SYNTAX</span></span>

### <span data-ttu-id="69b2d-105">互動式 (預設) </span><span class="sxs-lookup"><span data-stu-id="69b2d-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69b2d-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="69b2d-106">ByTopologyObjectAndServiceName</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopology] <PSServiceTopologyResource> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69b2d-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="69b2d-107">ByTopologyResourceAndServiceName</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69b2d-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="69b2d-108">ByServiceObject</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-Name] <String> [-Service] <PSServiceResource> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69b2d-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="69b2d-109">ByServiceResourceId</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-Name] <String> [-ServiceResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69b2d-110">ResourceId</span><span class="sxs-lookup"><span data-stu-id="69b2d-110">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69b2d-111">InputObject</span><span class="sxs-lookup"><span data-stu-id="69b2d-111">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-ServiceUnit] <PSServiceUnitResource> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69b2d-112">說明</span><span class="sxs-lookup"><span data-stu-id="69b2d-112">DESCRIPTION</span></span>
<span data-ttu-id="69b2d-113">**AzureRmDeploymentManagerServiceUnit** Cmdlet 會刪除服務中的服務單元。</span><span class="sxs-lookup"><span data-stu-id="69b2d-113">The **Remove-AzureRmDeploymentManagerServiceUnit** cmdlet deletes a service unit in a service.</span></span>

<span data-ttu-id="69b2d-114">依名稱指定服務單位、定義所用的服務、服務拓朴名稱和資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="69b2d-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="69b2d-115">或者，您也可以提供 ServiceUnit 物件或 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="69b2d-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

## <span data-ttu-id="69b2d-116">示例</span><span class="sxs-lookup"><span data-stu-id="69b2d-116">EXAMPLES</span></span>

### <span data-ttu-id="69b2d-117">範例1</span><span class="sxs-lookup"><span data-stu-id="69b2d-117">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="69b2d-118">這個命令會在 ContosoResourceGroup 中名為 [ContosoServiceTopology] 的服務拓撲中，刪除一個名為 ContosoService1Storage 的服務單元。</span><span class="sxs-lookup"><span data-stu-id="69b2d-118">This command deletes a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="69b2d-119">範例2：使用資源識別碼刪除服務單元。</span><span class="sxs-lookup"><span data-stu-id="69b2d-119">Example 2: Delete a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="69b2d-120">這個命令會在 ContosoResourceGroup 中名為 [ContosoServiceTopology] 的服務拓朴中，取得服務 ContosoService1 下的服務單元（名為 ContosoService1Storage）。</span><span class="sxs-lookup"><span data-stu-id="69b2d-120">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="69b2d-121">範例3：使用服務單元物件刪除服務單元。</span><span class="sxs-lookup"><span data-stu-id="69b2d-121">Example 3: Delete a service unit using the service unit object.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerServiceUnit -ServiceUnit $serviceUnitObject
```

<span data-ttu-id="69b2d-122">這個命令會分別刪除其名稱、服務名稱、服務拓朴名稱和 ResourceGroup 與 $serviceUnitObject 的名稱、ServiceName、ServiceTopologyName 和 ResourceGroupName 屬性相符的服務單元。</span><span class="sxs-lookup"><span data-stu-id="69b2d-122">This command deletes a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="69b2d-123">參數</span><span class="sxs-lookup"><span data-stu-id="69b2d-123">PARAMETERS</span></span>

### <span data-ttu-id="69b2d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69b2d-124">-DefaultProfile</span></span>
<span data-ttu-id="69b2d-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="69b2d-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69b2d-126">-Force</span><span class="sxs-lookup"><span data-stu-id="69b2d-126">-Force</span></span>
<span data-ttu-id="69b2d-127">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="69b2d-127">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="69b2d-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="69b2d-128">-Name</span></span>
<span data-ttu-id="69b2d-129">要刪除的服務單元的名稱。</span><span class="sxs-lookup"><span data-stu-id="69b2d-129">The name of the service unit to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName, ByServiceObject, ByServiceResourceId
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69b2d-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69b2d-130">-PassThru</span></span>
<span data-ttu-id="69b2d-131">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="69b2d-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="69b2d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69b2d-132">-ResourceGroupName</span></span>
<span data-ttu-id="69b2d-133">[資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="69b2d-133">The resource group.</span></span>

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

### <span data-ttu-id="69b2d-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69b2d-134">-ResourceId</span></span>
<span data-ttu-id="69b2d-135">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="69b2d-135">The resource identifier.</span></span>

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

### <span data-ttu-id="69b2d-136">-服務</span><span class="sxs-lookup"><span data-stu-id="69b2d-136">-Service</span></span>
<span data-ttu-id="69b2d-137">應該在其中建立服務單元的服務物件。</span><span class="sxs-lookup"><span data-stu-id="69b2d-137">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="69b2d-138">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="69b2d-138">-ServiceName</span></span>
<span data-ttu-id="69b2d-139">服務單元所屬之服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="69b2d-139">The name of the service the service unit belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69b2d-140">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="69b2d-140">-ServiceResourceId</span></span>
<span data-ttu-id="69b2d-141">在其中建立服務單元的服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="69b2d-141">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="69b2d-142">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="69b2d-142">-ServiceTopology</span></span>
<span data-ttu-id="69b2d-143">應該在其中建立服務單元的服務拓撲物件。</span><span class="sxs-lookup"><span data-stu-id="69b2d-143">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="69b2d-144">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="69b2d-144">-ServiceTopologyName</span></span>
<span data-ttu-id="69b2d-145">服務單元所屬之服務拓撲的名稱。</span><span class="sxs-lookup"><span data-stu-id="69b2d-145">The name of the service topology the service unit belongs to.</span></span>

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

### <span data-ttu-id="69b2d-146">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="69b2d-146">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="69b2d-147">在其中建立服務單元的服務拓撲資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="69b2d-147">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="69b2d-148">-ServiceUnit</span><span class="sxs-lookup"><span data-stu-id="69b2d-148">-ServiceUnit</span></span>
<span data-ttu-id="69b2d-149">要移除的資源。</span><span class="sxs-lookup"><span data-stu-id="69b2d-149">The resource to be removed.</span></span>

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

### <span data-ttu-id="69b2d-150">-確認</span><span class="sxs-lookup"><span data-stu-id="69b2d-150">-Confirm</span></span>
<span data-ttu-id="69b2d-151">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="69b2d-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69b2d-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69b2d-152">-WhatIf</span></span>
<span data-ttu-id="69b2d-153">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="69b2d-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69b2d-154">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="69b2d-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69b2d-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69b2d-155">CommonParameters</span></span>
<span data-ttu-id="69b2d-156">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="69b2d-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69b2d-157">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="69b2d-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69b2d-158">輸入</span><span class="sxs-lookup"><span data-stu-id="69b2d-158">INPUTS</span></span>

### <span data-ttu-id="69b2d-159">PSServiceUnitResource 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="69b2d-159">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="69b2d-160">輸出</span><span class="sxs-lookup"><span data-stu-id="69b2d-160">OUTPUTS</span></span>

### <span data-ttu-id="69b2d-161">System.object</span><span class="sxs-lookup"><span data-stu-id="69b2d-161">System.Boolean</span></span>

## <span data-ttu-id="69b2d-162">筆記</span><span class="sxs-lookup"><span data-stu-id="69b2d-162">NOTES</span></span>

## <span data-ttu-id="69b2d-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="69b2d-163">RELATED LINKS</span></span>

[<span data-ttu-id="69b2d-164">新-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="69b2d-164">New-AzureRmDeploymentManagerServiceUnit</span></span>](./New-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="69b2d-165">AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="69b2d-165">Get-AzureRmDeploymentManagerServiceUnit</span></span>](./Get-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="69b2d-166">Set-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="69b2d-166">Set-AzureRmDeploymentManagerServiceUnit</span></span>](./Set-AzureRmDeploymentManagerServiceUnit.md)