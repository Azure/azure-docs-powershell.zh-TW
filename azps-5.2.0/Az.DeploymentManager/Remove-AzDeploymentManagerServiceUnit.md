---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: d4248a13282824c60e698b2257b3e38a78ce3a6f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98278530"
---
# <span data-ttu-id="0aaa8-101">Remove-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="0aaa8-101">Remove-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="0aaa8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0aaa8-102">SYNOPSIS</span></span>
<span data-ttu-id="0aaa8-103">刪除服務單元。</span><span class="sxs-lookup"><span data-stu-id="0aaa8-103">Deletes the service unit.</span></span>

## <span data-ttu-id="0aaa8-104">句法</span><span class="sxs-lookup"><span data-stu-id="0aaa8-104">SYNTAX</span></span>

### <span data-ttu-id="0aaa8-105">互動式 (預設) </span><span class="sxs-lookup"><span data-stu-id="0aaa8-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0aaa8-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="0aaa8-106">ByTopologyObjectAndServiceName</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0aaa8-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="0aaa8-107">ByTopologyResourceAndServiceName</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0aaa8-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="0aaa8-108">ByServiceObject</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-Name] <String> [-ServiceObject] <PSServiceResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0aaa8-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="0aaa8-109">ByServiceResourceId</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-Name] <String> [-ServiceResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0aaa8-110">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0aaa8-110">ResourceId</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0aaa8-111">InputObject</span><span class="sxs-lookup"><span data-stu-id="0aaa8-111">InputObject</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0aaa8-112">說明</span><span class="sxs-lookup"><span data-stu-id="0aaa8-112">DESCRIPTION</span></span>
<span data-ttu-id="0aaa8-113">**AzDeploymentManagerServiceUnit** Cmdlet 會刪除服務中的服務單元。</span><span class="sxs-lookup"><span data-stu-id="0aaa8-113">The **Remove-AzDeploymentManagerServiceUnit** cmdlet deletes a service unit in a service.</span></span>

<span data-ttu-id="0aaa8-114">依名稱指定服務單位、定義所用的服務、服務拓朴名稱和資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="0aaa8-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="0aaa8-115">或者，您也可以提供 ServiceUnit 物件或 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="0aaa8-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

## <span data-ttu-id="0aaa8-116">示例</span><span class="sxs-lookup"><span data-stu-id="0aaa8-116">EXAMPLES</span></span>

### <span data-ttu-id="0aaa8-117">範例1</span><span class="sxs-lookup"><span data-stu-id="0aaa8-117">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="0aaa8-118">這個命令會在 ContosoResourceGroup 中名為 [ContosoServiceTopology] 的服務拓撲中，刪除一個名為 ContosoService1Storage 的服務單元。</span><span class="sxs-lookup"><span data-stu-id="0aaa8-118">This command deletes a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="0aaa8-119">範例2：使用資源識別碼刪除服務單元。</span><span class="sxs-lookup"><span data-stu-id="0aaa8-119">Example 2: Delete a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="0aaa8-120">這個命令會在 ContosoResourceGroup 中名為 [ContosoServiceTopology] 的服務拓朴中，取得服務 ContosoService1 下的服務單元（名為 ContosoService1Storage）。</span><span class="sxs-lookup"><span data-stu-id="0aaa8-120">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="0aaa8-121">範例3：使用服務單元物件刪除服務單元。</span><span class="sxs-lookup"><span data-stu-id="0aaa8-121">Example 3: Delete a service unit using the service unit object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="0aaa8-122">這個命令會分別刪除其名稱、服務名稱、服務拓朴名稱和 ResourceGroup 與 $serviceUnitObject 的名稱、ServiceName、ServiceTopologyName 和 ResourceGroupName 屬性相符的服務單元。</span><span class="sxs-lookup"><span data-stu-id="0aaa8-122">This command deletes a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="0aaa8-123">參數</span><span class="sxs-lookup"><span data-stu-id="0aaa8-123">PARAMETERS</span></span>

### <span data-ttu-id="0aaa8-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0aaa8-124">-DefaultProfile</span></span>
<span data-ttu-id="0aaa8-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0aaa8-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0aaa8-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0aaa8-126">-InputObject</span></span>
<span data-ttu-id="0aaa8-127">[服務單元] 資源物件。</span><span class="sxs-lookup"><span data-stu-id="0aaa8-127">Service unit resource object.</span></span>

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

### <span data-ttu-id="0aaa8-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="0aaa8-128">-Name</span></span>
<span data-ttu-id="0aaa8-129">服務單元的名稱。</span><span class="sxs-lookup"><span data-stu-id="0aaa8-129">The name of the service unit.</span></span>

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

### <span data-ttu-id="0aaa8-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0aaa8-130">-PassThru</span></span>
<span data-ttu-id="0aaa8-131">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="0aaa8-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="0aaa8-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0aaa8-132">-ResourceGroupName</span></span>
<span data-ttu-id="0aaa8-133">[資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="0aaa8-133">The resource group.</span></span>

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

### <span data-ttu-id="0aaa8-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0aaa8-134">-ResourceId</span></span>
<span data-ttu-id="0aaa8-135">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0aaa8-135">The resource identifier.</span></span>

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

### <span data-ttu-id="0aaa8-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="0aaa8-136">-ServiceName</span></span>
<span data-ttu-id="0aaa8-137">服務單元所屬的服務名稱。</span><span class="sxs-lookup"><span data-stu-id="0aaa8-137">The name of the service the service unit is part of.</span></span>

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

### <span data-ttu-id="0aaa8-138">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="0aaa8-138">-ServiceObject</span></span>
<span data-ttu-id="0aaa8-139">應該在其中建立服務單元的服務物件。</span><span class="sxs-lookup"><span data-stu-id="0aaa8-139">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="0aaa8-140">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="0aaa8-140">-ServiceResourceId</span></span>
<span data-ttu-id="0aaa8-141">在其中建立服務單元的服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0aaa8-141">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="0aaa8-142">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="0aaa8-142">-ServiceTopologyName</span></span>
<span data-ttu-id="0aaa8-143">服務單元所屬的服務拓撲的名稱。</span><span class="sxs-lookup"><span data-stu-id="0aaa8-143">The name of the service topology the service unit is part of.</span></span>

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

### <span data-ttu-id="0aaa8-144">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="0aaa8-144">-ServiceTopologyObject</span></span>
<span data-ttu-id="0aaa8-145">應該在其中建立服務單元的服務拓撲物件。</span><span class="sxs-lookup"><span data-stu-id="0aaa8-145">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="0aaa8-146">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="0aaa8-146">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="0aaa8-147">在其中建立服務單元的服務拓撲資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0aaa8-147">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="0aaa8-148">-確認</span><span class="sxs-lookup"><span data-stu-id="0aaa8-148">-Confirm</span></span>
<span data-ttu-id="0aaa8-149">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0aaa8-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0aaa8-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0aaa8-150">-WhatIf</span></span>
<span data-ttu-id="0aaa8-151">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0aaa8-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0aaa8-152">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0aaa8-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0aaa8-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0aaa8-153">CommonParameters</span></span>
<span data-ttu-id="0aaa8-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0aaa8-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0aaa8-155">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0aaa8-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0aaa8-156">輸入</span><span class="sxs-lookup"><span data-stu-id="0aaa8-156">INPUTS</span></span>

### <span data-ttu-id="0aaa8-157">System.object</span><span class="sxs-lookup"><span data-stu-id="0aaa8-157">System.String</span></span>

### <span data-ttu-id="0aaa8-158">PSServiceUnitResource 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="0aaa8-158">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="0aaa8-159">輸出</span><span class="sxs-lookup"><span data-stu-id="0aaa8-159">OUTPUTS</span></span>

### <span data-ttu-id="0aaa8-160">System.object</span><span class="sxs-lookup"><span data-stu-id="0aaa8-160">System.Boolean</span></span>

## <span data-ttu-id="0aaa8-161">筆記</span><span class="sxs-lookup"><span data-stu-id="0aaa8-161">NOTES</span></span>

## <span data-ttu-id="0aaa8-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="0aaa8-162">RELATED LINKS</span></span>
