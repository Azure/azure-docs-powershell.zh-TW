---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
ms.openlocfilehash: f3a5b61561b0886af32aa13103f3234098c76357
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908202"
---
# <span data-ttu-id="a0a0c-101">New-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="a0a0c-101">New-AzFrontDoor</span></span>

## <span data-ttu-id="a0a0c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a0a0c-102">SYNOPSIS</span></span>
<span data-ttu-id="a0a0c-103">建立新的 Azure 前門負載平衡器</span><span class="sxs-lookup"><span data-stu-id="a0a0c-103">Create a new Azure Front Door load balancer</span></span>

## <span data-ttu-id="a0a0c-104">語法</span><span class="sxs-lookup"><span data-stu-id="a0a0c-104">SYNTAX</span></span>

### <span data-ttu-id="a0a0c-105">ByFieldsWithBackendPoolsSettingParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a0a0c-105">ByFieldsWithBackendPoolsSettingParameterSet (Default)</span></span>
```
New-AzFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-BackendPoolsSetting <PSBackendPoolsSetting>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0a0c-106">ByFieldsWithCertificateNameCheckParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0a0c-106">ByFieldsWithCertificateNameCheckParameterSet</span></span>
```
New-AzFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DisableCertificateNameCheck]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0a0c-107">描述</span><span class="sxs-lookup"><span data-stu-id="a0a0c-107">DESCRIPTION</span></span>
<span data-ttu-id="a0a0c-108">**New-AzFrontDoor** Cmdlet 在目前訂閱下的指定資源群組中，建立新的 Azure Front Door 負載平衡器</span><span class="sxs-lookup"><span data-stu-id="a0a0c-108">The **New-AzFrontDoor** cmdlet creates a new Azure Front Door load balancer in the specified resource group under current subscription</span></span>

## <span data-ttu-id="a0a0c-109">例子</span><span class="sxs-lookup"><span data-stu-id="a0a0c-109">EXAMPLES</span></span>

### <span data-ttu-id="a0a0c-110">範例 1：根據指定參數建立門道。</span><span class="sxs-lookup"><span data-stu-id="a0a0c-110">Example 1: Create a Front Door based on given parameters.</span></span>
```powershell
PS C:\> New-AzFrontDoor -Name "frontDoor1" -ResourceGroupName "rg1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1 -BackendPoolsSetting $backendPoolsSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
BackendPoolsSetting         : {backendPoolsSetting1}
EnforceCertificateNameCheck : {backendPoolsSetting1.EnforceCertificateNameCheck}
HealthProbeSettings         : {healthProbeSetting1}
LoadBalancingSettings       : {loadbalancingsetting1}
FrontendEndpoints           : {frontendendpoint1}
EnabledState                : Enabled
ResourceState               : Enabled
ProvisioningState           : Succeeded
Cname                       :
Tags                        : {tag1, tag2}
Id                          : /subscriptions/{guid}/resourcegroups/rg1/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoors
```

<span data-ttu-id="a0a0c-111">根據指定參數建立門道。</span><span class="sxs-lookup"><span data-stu-id="a0a0c-111">Create a Front Door based on given parameters.</span></span>

## <span data-ttu-id="a0a0c-112">參數</span><span class="sxs-lookup"><span data-stu-id="a0a0c-112">PARAMETERS</span></span>

### <span data-ttu-id="a0a0c-113">-後端多工緩衝處理程式</span><span class="sxs-lookup"><span data-stu-id="a0a0c-113">-BackendPool</span></span>
<span data-ttu-id="a0a0c-114">路由規則可用的後端多工緩衝處理程式。</span><span class="sxs-lookup"><span data-stu-id="a0a0c-114">Backendpools available to routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0a0c-115">-後端多工緩衝處理程式設定</span><span class="sxs-lookup"><span data-stu-id="a0a0c-115">-BackendPoolsSetting</span></span>
<span data-ttu-id="a0a0c-116">所有後端多工緩衝處理程式的設定</span><span class="sxs-lookup"><span data-stu-id="a0a0c-116">Settings for all backendPools</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting
Parameter Sets: ByFieldsWithBackendPoolsSettingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0a0c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0a0c-117">-DefaultProfile</span></span>
<span data-ttu-id="a0a0c-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a0a0c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0a0c-119">-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="a0a0c-119">-DisableCertificateNameCheck</span></span>
<span data-ttu-id="a0a0c-120">是否要停用所有後端資料庫之 HTTPS 要求上的憑證名稱檢查。</span><span class="sxs-lookup"><span data-stu-id="a0a0c-120">Whether to disable certificate name check on HTTPS requests to all backend pools.</span></span> <span data-ttu-id="a0a0c-121">對非 HTTPS 要求沒有影響。</span><span class="sxs-lookup"><span data-stu-id="a0a0c-121">No effect on non-HTTPS requests.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFieldsWithCertificateNameCheckParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0a0c-122">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="a0a0c-122">-EnabledState</span></span>
<span data-ttu-id="a0a0c-123">啟用前門負載平衡器狀態。</span><span class="sxs-lookup"><span data-stu-id="a0a0c-123">EnabledState of the Front Door load balancer.</span></span>
<span data-ttu-id="a0a0c-124">預設值為啟用</span><span class="sxs-lookup"><span data-stu-id="a0a0c-124">Default value is Enabled</span></span>

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

### <span data-ttu-id="a0a0c-125">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="a0a0c-125">-FrontendEndpoint</span></span>
<span data-ttu-id="a0a0c-126">路由規則可用的前端端點。</span><span class="sxs-lookup"><span data-stu-id="a0a0c-126">Frontend endpoints available to routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0a0c-127">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="a0a0c-127">-HealthProbeSetting</span></span>
<span data-ttu-id="a0a0c-128">與此前門實例相關聯的健康情況設定。</span><span class="sxs-lookup"><span data-stu-id="a0a0c-128">Health probe settings associated with this Front Door instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0a0c-129">-LoadBalsettingSetting</span><span class="sxs-lookup"><span data-stu-id="a0a0c-129">-LoadBalancingSetting</span></span>
<span data-ttu-id="a0a0c-130">與此前門實例相關聯的負載平衡設定。</span><span class="sxs-lookup"><span data-stu-id="a0a0c-130">Load balancing settings associated with this Front Door instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0a0c-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="a0a0c-131">-Name</span></span>
<span data-ttu-id="a0a0c-132">前門名稱。</span><span class="sxs-lookup"><span data-stu-id="a0a0c-132">Front Door name.</span></span>

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

### <span data-ttu-id="a0a0c-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0a0c-133">-ResourceGroupName</span></span>
<span data-ttu-id="a0a0c-134">要建立前門的資源組名。</span><span class="sxs-lookup"><span data-stu-id="a0a0c-134">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="a0a0c-135">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="a0a0c-135">-RoutingRule</span></span>
<span data-ttu-id="a0a0c-136">與此 FrontDoor 相關聯的路由規則</span><span class="sxs-lookup"><span data-stu-id="a0a0c-136">Routing rules associated with this FrontDoor</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0a0c-137">-標記</span><span class="sxs-lookup"><span data-stu-id="a0a0c-137">-Tag</span></span>
<span data-ttu-id="a0a0c-138">與 FrontDoor 相關聯的標記。</span><span class="sxs-lookup"><span data-stu-id="a0a0c-138">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="a0a0c-139">-確認</span><span class="sxs-lookup"><span data-stu-id="a0a0c-139">-Confirm</span></span>
<span data-ttu-id="a0a0c-140">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a0a0c-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0a0c-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0a0c-141">-WhatIf</span></span>
<span data-ttu-id="a0a0c-142">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a0a0c-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0a0c-143">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a0a0c-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0a0c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0a0c-144">CommonParameters</span></span>
<span data-ttu-id="a0a0c-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a0a0c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0a0c-146">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a0a0c-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0a0c-147">輸入</span><span class="sxs-lookup"><span data-stu-id="a0a0c-147">INPUTS</span></span>

### <span data-ttu-id="a0a0c-148">沒有</span><span class="sxs-lookup"><span data-stu-id="a0a0c-148">None</span></span>
## <span data-ttu-id="a0a0c-149">輸出</span><span class="sxs-lookup"><span data-stu-id="a0a0c-149">OUTPUTS</span></span>

### <span data-ttu-id="a0a0c-150">Microsoft.Azure.Commands.FrontDoor.models.PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="a0a0c-150">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>
## <span data-ttu-id="a0a0c-151">筆記</span><span class="sxs-lookup"><span data-stu-id="a0a0c-151">NOTES</span></span>

## <span data-ttu-id="a0a0c-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="a0a0c-152">RELATED LINKS</span></span>

<span data-ttu-id="a0a0c-153">[Get-AzFrontDoor](./Get-AzFrontDoor.md) 
[Set-AzFrontDoor](./Set-AzFrontDoor.md) 
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md) 
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md) 
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md) 
[New-AzFrontDoorLoadBalsettingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md) 
[New-AzFrontDoorFrontendPointObject](./New-AzFrontDoorFrontendEndpointObject.md) 
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="a0a0c-153">[Get-AzFrontDoor](./Get-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md)
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md)
[New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md)
[New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md)
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span></span>