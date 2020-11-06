---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/set-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoor.md
ms.openlocfilehash: 57f1bf57495e75167a1936799c24aff5e6387722
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612343"
---
# <span data-ttu-id="33960-101">Set-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="33960-101">Set-AzFrontDoor</span></span>

## <span data-ttu-id="33960-102">摘要</span><span class="sxs-lookup"><span data-stu-id="33960-102">SYNOPSIS</span></span>
<span data-ttu-id="33960-103">更新前門負載平衡器</span><span class="sxs-lookup"><span data-stu-id="33960-103">Update a Front Door load balancer</span></span>

## <span data-ttu-id="33960-104">句法</span><span class="sxs-lookup"><span data-stu-id="33960-104">SYNTAX</span></span>

### <span data-ttu-id="33960-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="33960-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DisableCertificateNameCheck]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33960-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="33960-106">ByObjectParameterSet</span></span>
```
Set-AzFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DisableCertificateNameCheck] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="33960-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="33960-107">ByResourceIdParameterSet</span></span>
```
Set-AzFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DisableCertificateNameCheck] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="33960-108">說明</span><span class="sxs-lookup"><span data-stu-id="33960-108">DESCRIPTION</span></span>
<span data-ttu-id="33960-109">**AzFrontDoor** Cmdlet 會更新前門負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="33960-109">The **Set-AzFrontDoor** cmdlet updates a Front Door load balancer.</span></span> <span data-ttu-id="33960-110">如果未提供輸入參數，則會使用現有的前蓋的舊參數。</span><span class="sxs-lookup"><span data-stu-id="33960-110">If input parameters are not provided, old parameters from the existing Front Door will be used.</span></span>

## <span data-ttu-id="33960-111">示例</span><span class="sxs-lookup"><span data-stu-id="33960-111">EXAMPLES</span></span>

### <span data-ttu-id="33960-112">範例1：使用 FrontDoorName 和 ResourceGroupName 更新現有的前門。</span><span class="sxs-lookup"><span data-stu-id="33960-112">Example 1: update an existing Front Door with FrontDoorName and ResourceGroupName.</span></span>
```powershell
PS C:\> Set-AzFrontDoor -Name "frontDoor1" -ResourceGroupName "resourceGroup1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
EnforceCertificateNameCheck : Enabled
HealthProbeSettings         : {healthProbeSetting1}
LoadBalancingSettings       : {loadbalancingsetting1}
FrontendEndpoints           : {frontendendpoint1}
EnabledState                : Enabled
ResourceState               : Enabled
ProvisioningState           : Succeeded
Cname                       :
Tags                        : {tag1, tag2}
Id                          : /subscriptions/{guid}/resourcegroups/{guid}/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoors
```

<span data-ttu-id="33960-113">更新現有的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="33960-113">update an existing FrontDoor.</span></span>

### <span data-ttu-id="33960-114">範例2：使用 PSFrontDoor 物件更新現有的前門。</span><span class="sxs-lookup"><span data-stu-id="33960-114">Example 2: update an existing Front Door with PSFrontDoor object.</span></span>
```powershell
PS C:\>  Set-AzFrontDoor -InputObject $frontDoor1 -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
EnforceCertificateNameCheck : Enabled
HealthProbeSettings         : {healthProbeSetting1}
LoadBalancingSettings       : {loadbalancingsetting1}
FrontendEndpoints           : {frontendendpoint1}
EnabledState                : Enabled
ResourceState               : Enabled
ProvisioningState           : Succeeded
Cname                       :
Tags                        : {tag1, tag2}
Id                          : /subscriptions/{guid}/resourcegroups/{guid}/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoor1
```

<span data-ttu-id="33960-115">更新現有的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="33960-115">update an existing FrontDoor.</span></span>

### <span data-ttu-id="33960-116">範例3：使用 ResourceId 更新現有的前門</span><span class="sxs-lookup"><span data-stu-id="33960-116">Example 3: update an existing Front Door with ResourceId</span></span>
```powershell
PS C:\>  Set-AzFrontDoor -ResourceId {resourceId} -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
EnforceCertificateNameCheck : Enabled
HealthProbeSettings         : {healthProbeSetting1}
LoadBalancingSettings       : {loadbalancingsetting1}
FrontendEndpoints           : {frontendendpoint1}
EnabledState                : Enabled
ResourceState               : Enabled
ProvisioningState           : Succeeded
Cname                       :
Tags                        : {tag1, tag2}
Id                          : /subscriptions/{guid}/resourcegroups/{guid}/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoor1
```

<span data-ttu-id="33960-117">更新現有的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="33960-117">update an existing FrontDoor.</span></span>

## <span data-ttu-id="33960-118">參數</span><span class="sxs-lookup"><span data-stu-id="33960-118">PARAMETERS</span></span>

### <span data-ttu-id="33960-119">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="33960-119">-BackendPool</span></span>
<span data-ttu-id="33960-120">Backendpools 可供路由規則使用。</span><span class="sxs-lookup"><span data-stu-id="33960-120">Backendpools available to routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33960-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33960-121">-DefaultProfile</span></span>
<span data-ttu-id="33960-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="33960-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33960-123">-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="33960-123">-DisableCertificateNameCheck</span></span>
<span data-ttu-id="33960-124">是否要針對所有後端池停用 HTTPS 要求的憑證名稱檢查。</span><span class="sxs-lookup"><span data-stu-id="33960-124">Whether to disable certificate name check on HTTPS requests to all backend pools.</span></span> <span data-ttu-id="33960-125">對非 HTTPS 式要求沒有作用。</span><span class="sxs-lookup"><span data-stu-id="33960-125">No effect on non-HTTPS requests.</span></span>

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

### <span data-ttu-id="33960-126">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="33960-126">-EnabledState</span></span>
<span data-ttu-id="33960-127">前門負載平衡器的運作狀態。</span><span class="sxs-lookup"><span data-stu-id="33960-127">Operational status of the Front Door load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33960-128">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="33960-128">-FrontendEndpoint</span></span>
<span data-ttu-id="33960-129">可供路由規則使用的前端端點。</span><span class="sxs-lookup"><span data-stu-id="33960-129">Frontend endpoints available to routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33960-130">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="33960-130">-HealthProbeSetting</span></span>
<span data-ttu-id="33960-131">與此前門實例相關聯的健康情況探測器設定。</span><span class="sxs-lookup"><span data-stu-id="33960-131">Health probe settings associated with this Front Door instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33960-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33960-132">-InputObject</span></span>
<span data-ttu-id="33960-133">要更新的前蓋物件。</span><span class="sxs-lookup"><span data-stu-id="33960-133">The Front Door object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33960-134">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="33960-134">-LoadBalancingSetting</span></span>
<span data-ttu-id="33960-135">與此前門實例相關聯的負載平衡設定。</span><span class="sxs-lookup"><span data-stu-id="33960-135">Load balancing settings associated with this Front Door instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33960-136">-名稱</span><span class="sxs-lookup"><span data-stu-id="33960-136">-Name</span></span>
<span data-ttu-id="33960-137">要更新之前門的名稱。</span><span class="sxs-lookup"><span data-stu-id="33960-137">The name of the Front Door to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33960-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33960-138">-ResourceGroupName</span></span>
<span data-ttu-id="33960-139">前門所屬的資源群組。</span><span class="sxs-lookup"><span data-stu-id="33960-139">The resource group to which the Front Door belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33960-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="33960-140">-ResourceId</span></span>
<span data-ttu-id="33960-141">要更新之前門的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="33960-141">Resource Id of the Front Door to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33960-142">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="33960-142">-RoutingRule</span></span>
<span data-ttu-id="33960-143">與此 FrontDoor 相關聯的路由規則</span><span class="sxs-lookup"><span data-stu-id="33960-143">Routing rules associated with this FrontDoor</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33960-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="33960-144">-Tag</span></span>
<span data-ttu-id="33960-145">標記與 FrontDoor 相關聯。</span><span class="sxs-lookup"><span data-stu-id="33960-145">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="33960-146">-確認</span><span class="sxs-lookup"><span data-stu-id="33960-146">-Confirm</span></span>
<span data-ttu-id="33960-147">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="33960-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33960-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33960-148">-WhatIf</span></span>
<span data-ttu-id="33960-149">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="33960-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33960-150">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="33960-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33960-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33960-151">CommonParameters</span></span>
<span data-ttu-id="33960-152">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="33960-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33960-153">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="33960-153">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33960-154">輸入</span><span class="sxs-lookup"><span data-stu-id="33960-154">INPUTS</span></span>

### <span data-ttu-id="33960-155">PSFrontDoor 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="33960-155">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="33960-156">System.object</span><span class="sxs-lookup"><span data-stu-id="33960-156">System.String</span></span>

## <span data-ttu-id="33960-157">輸出</span><span class="sxs-lookup"><span data-stu-id="33960-157">OUTPUTS</span></span>

### <span data-ttu-id="33960-158">PSFrontDoor 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="33960-158">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="33960-159">筆記</span><span class="sxs-lookup"><span data-stu-id="33960-159">NOTES</span></span>

## <span data-ttu-id="33960-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="33960-160">RELATED LINKS</span></span>

<span data-ttu-id="33960-161">[新-AzFrontDoor](./New-AzFrontDoor.md) 
[AzFrontDoor](./Get-AzFrontDoor.md) 
[移除-AzFrontDoor](./Remove-AzFrontDoor.md) 
[新-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md) 
[新-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md) 
[新-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md) 
[新-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md) 
[新-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="33960-161">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Get-AzFrontDoor](./Get-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md)
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md)
[New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md)
[New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md)
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span></span>
