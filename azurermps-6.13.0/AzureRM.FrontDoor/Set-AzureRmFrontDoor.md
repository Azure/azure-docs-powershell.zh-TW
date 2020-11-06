---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/set-azurermfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Set-AzureRmFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Set-AzureRmFrontDoor.md
ms.openlocfilehash: 250fa8a5638e1aa9d67d212fd45352c7756d2aef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93443819"
---
# <span data-ttu-id="93cc2-101">Set-AzureRmFrontDoor</span><span class="sxs-lookup"><span data-stu-id="93cc2-101">Set-AzureRmFrontDoor</span></span>

## <span data-ttu-id="93cc2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="93cc2-102">SYNOPSIS</span></span>
<span data-ttu-id="93cc2-103">更新前門負載平衡器</span><span class="sxs-lookup"><span data-stu-id="93cc2-103">Update a Front Door load balancer</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93cc2-104">句法</span><span class="sxs-lookup"><span data-stu-id="93cc2-104">SYNTAX</span></span>

### <span data-ttu-id="93cc2-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="93cc2-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzureRmFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93cc2-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="93cc2-106">ByObjectParameterSet</span></span>
```
Set-AzureRmFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93cc2-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="93cc2-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93cc2-108">說明</span><span class="sxs-lookup"><span data-stu-id="93cc2-108">DESCRIPTION</span></span>
<span data-ttu-id="93cc2-109">**AzureRmFrontDoor** Cmdlet 會更新前門負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="93cc2-109">The **Set-AzureRmFrontDoor** cmdlet updates a Front Door load balancer.</span></span> <span data-ttu-id="93cc2-110">如果未提供輸入參數，則會使用現有的前蓋的舊參數。</span><span class="sxs-lookup"><span data-stu-id="93cc2-110">If input parameters are not provided, old parameters from the existing Front Door will be used.</span></span>

## <span data-ttu-id="93cc2-111">示例</span><span class="sxs-lookup"><span data-stu-id="93cc2-111">EXAMPLES</span></span>

### <span data-ttu-id="93cc2-112">範例1：使用 FrontDoorName 和 ResourceGroupName 更新現有的前門。</span><span class="sxs-lookup"><span data-stu-id="93cc2-112">Example 1: update an existing Front Door with FrontDoorName and ResourceGroupName.</span></span>
```powershell
PS C:\> Set-AzureRmFrontDoor -Name "frontDoor1" -ResourceGroupName "resourceGroup1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="93cc2-113">更新現有的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="93cc2-113">update an existing FrontDoor.</span></span>

### <span data-ttu-id="93cc2-114">範例2：使用 PSFrontDoor 物件更新現有的前門。</span><span class="sxs-lookup"><span data-stu-id="93cc2-114">Example 2: update an existing Front Door with PSFrontDoor object.</span></span>
```powershell
PS C:\>  Set-AzureRmFrontDoor -InputObject $frontDoor1 -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="93cc2-115">更新現有的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="93cc2-115">update an existing FrontDoor.</span></span>

### <span data-ttu-id="93cc2-116">範例3：使用 ResourceId 更新現有的前門</span><span class="sxs-lookup"><span data-stu-id="93cc2-116">Example 3: update an existing Front Door with ResourceId</span></span>
```powershell
PS C:\>  Set-AzureRmFrontDoor -ResourceId {resourceId} -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="93cc2-117">更新現有的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="93cc2-117">update an existing FrontDoor.</span></span>

## <span data-ttu-id="93cc2-118">參數</span><span class="sxs-lookup"><span data-stu-id="93cc2-118">PARAMETERS</span></span>

### <span data-ttu-id="93cc2-119">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="93cc2-119">-BackendPool</span></span>
<span data-ttu-id="93cc2-120">Backendpools 可供路由規則使用。</span><span class="sxs-lookup"><span data-stu-id="93cc2-120">Backendpools available to routing rule.</span></span>

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

### <span data-ttu-id="93cc2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93cc2-121">-DefaultProfile</span></span>
<span data-ttu-id="93cc2-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="93cc2-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93cc2-123">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="93cc2-123">-EnabledState</span></span>
<span data-ttu-id="93cc2-124">前門負載平衡器的運作狀態。</span><span class="sxs-lookup"><span data-stu-id="93cc2-124">Operational status of the Front Door load balancer.</span></span>

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

### <span data-ttu-id="93cc2-125">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="93cc2-125">-FrontendEndpoint</span></span>
<span data-ttu-id="93cc2-126">可供路由規則使用的前端端點。</span><span class="sxs-lookup"><span data-stu-id="93cc2-126">Frontend endpoints available to routing rule.</span></span>

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

### <span data-ttu-id="93cc2-127">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="93cc2-127">-HealthProbeSetting</span></span>
<span data-ttu-id="93cc2-128">與此前門實例相關聯的健康情況探測器設定。</span><span class="sxs-lookup"><span data-stu-id="93cc2-128">Health probe settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="93cc2-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93cc2-129">-InputObject</span></span>
<span data-ttu-id="93cc2-130">要更新的前蓋物件。</span><span class="sxs-lookup"><span data-stu-id="93cc2-130">The Front Door object to update.</span></span>

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

### <span data-ttu-id="93cc2-131">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="93cc2-131">-LoadBalancingSetting</span></span>
<span data-ttu-id="93cc2-132">與此前門實例相關聯的負載平衡設定。</span><span class="sxs-lookup"><span data-stu-id="93cc2-132">Load balancing settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="93cc2-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="93cc2-133">-Name</span></span>
<span data-ttu-id="93cc2-134">要更新之前門的名稱。</span><span class="sxs-lookup"><span data-stu-id="93cc2-134">The name of the Front Door to update.</span></span>

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

### <span data-ttu-id="93cc2-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93cc2-135">-ResourceGroupName</span></span>
<span data-ttu-id="93cc2-136">前門所屬的資源群組。</span><span class="sxs-lookup"><span data-stu-id="93cc2-136">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="93cc2-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="93cc2-137">-ResourceId</span></span>
<span data-ttu-id="93cc2-138">要更新之前門的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="93cc2-138">Resource Id of the Front Door to update</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93cc2-139">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="93cc2-139">-RoutingRule</span></span>
<span data-ttu-id="93cc2-140">與此 FrontDoor 相關聯的路由規則</span><span class="sxs-lookup"><span data-stu-id="93cc2-140">Routing rules associated with this FrontDoor</span></span>

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

### <span data-ttu-id="93cc2-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="93cc2-141">-Tag</span></span>
<span data-ttu-id="93cc2-142">標記與 FrontDoor 相關聯。</span><span class="sxs-lookup"><span data-stu-id="93cc2-142">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="93cc2-143">-確認</span><span class="sxs-lookup"><span data-stu-id="93cc2-143">-Confirm</span></span>
<span data-ttu-id="93cc2-144">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="93cc2-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93cc2-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93cc2-145">-WhatIf</span></span>
<span data-ttu-id="93cc2-146">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="93cc2-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93cc2-147">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="93cc2-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93cc2-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93cc2-148">CommonParameters</span></span>
<span data-ttu-id="93cc2-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="93cc2-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93cc2-150">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="93cc2-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93cc2-151">輸入</span><span class="sxs-lookup"><span data-stu-id="93cc2-151">INPUTS</span></span>

### <span data-ttu-id="93cc2-152">PSFrontDoor 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="93cc2-152">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="93cc2-153">System.object</span><span class="sxs-lookup"><span data-stu-id="93cc2-153">System.String</span></span>

## <span data-ttu-id="93cc2-154">輸出</span><span class="sxs-lookup"><span data-stu-id="93cc2-154">OUTPUTS</span></span>

### <span data-ttu-id="93cc2-155">PSFrontDoor 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="93cc2-155">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="93cc2-156">筆記</span><span class="sxs-lookup"><span data-stu-id="93cc2-156">NOTES</span></span>

## <span data-ttu-id="93cc2-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="93cc2-157">RELATED LINKS</span></span>

<span data-ttu-id="93cc2-158">[新-AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
[AzureRmFrontDoor](./Get-AzureRmFrontDoor.md) 
[移除-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md) 
[新-AzureRmFrontDoorRoutingRuleObject](./New-AzureRmFrontDoorRoutingRuleObject.md) 
[新-AzureRmFrontDoorHealthProbeSettingObject](./New-AzureRmFrontHealthProbeSettingObject.md) 
[新-AzureRmFrontDoorLoadBalancingSettingObject](./New-AzureRmFrontDoorLoadBalancingSettingObject.md) 
[新-AzureRmFrontDoorFrontendEndpointObject](./New-AzureRmFrontDoorFrontendEndpointObject.md) 
[新-AzureRmFrontDoorBackendPoolObject](./New-AzureRmFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="93cc2-158">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md)
[Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md)
[New-AzureRmFrontDoorRoutingRuleObject](./New-AzureRmFrontDoorRoutingRuleObject.md)
[New-AzureRmFrontDoorHealthProbeSettingObject](./New-AzureRmFrontHealthProbeSettingObject.md)
[New-AzureRmFrontDoorLoadBalancingSettingObject](./New-AzureRmFrontDoorLoadBalancingSettingObject.md)
[New-AzureRmFrontDoorFrontendEndpointObject](./New-AzureRmFrontDoorFrontendEndpointObject.md)
[New-AzureRmFrontDoorBackendPoolObject](./New-AzureRmFrontDoorBackendPoolObject.md)</span></span>
