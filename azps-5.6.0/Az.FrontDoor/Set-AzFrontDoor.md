---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/set-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoor.md
ms.openlocfilehash: 16501021189c815e7631062719781474a2e91a3e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906209"
---
# <span data-ttu-id="8b021-101">Set-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="8b021-101">Set-AzFrontDoor</span></span>

## <span data-ttu-id="8b021-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8b021-102">SYNOPSIS</span></span>
<span data-ttu-id="8b021-103">更新前門負載平衡器</span><span class="sxs-lookup"><span data-stu-id="8b021-103">Update a Front Door load balancer</span></span>

## <span data-ttu-id="8b021-104">語法</span><span class="sxs-lookup"><span data-stu-id="8b021-104">SYNTAX</span></span>

### <span data-ttu-id="8b021-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8b021-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b021-106">ByFieldsWithCertificateNameCheckParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b021-106">ByFieldsWithCertificateNameCheckParameterSet</span></span>
```
Set-AzFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DisableCertificateNameCheck]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b021-107">ByFieldsWithBackendPoolsSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b021-107">ByFieldsWithBackendPoolsSettingParameterSet</span></span>
```
Set-AzFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] -BackendPoolsSetting <PSBackendPoolsSetting>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b021-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b021-108">ByObjectParameterSet</span></span>
```
Set-AzFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b021-109">ByObjectWithCertificateNameCheckParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b021-109">ByObjectWithCertificateNameCheckParameterSet</span></span>
```
Set-AzFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DisableCertificateNameCheck] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8b021-110">ByObjectWithBackendPoolsSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b021-110">ByObjectWithBackendPoolsSettingParameterSet</span></span>
```
Set-AzFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 -BackendPoolsSetting <PSBackendPoolsSetting> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8b021-111">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b021-111">ByResourceIdParameterSet</span></span>
```
Set-AzFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b021-112">ByResourceIdWithCertificateNameCheckParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b021-112">ByResourceIdWithCertificateNameCheckParameterSet</span></span>
```
Set-AzFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DisableCertificateNameCheck] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8b021-113">ByResourceIdWithBackendPoolsSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b021-113">ByResourceIdWithBackendPoolsSettingParameterSet</span></span>
```
Set-AzFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 -BackendPoolsSetting <PSBackendPoolsSetting> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8b021-114">描述</span><span class="sxs-lookup"><span data-stu-id="8b021-114">DESCRIPTION</span></span>
<span data-ttu-id="8b021-115">**Set-AzFrontDoor** Cmdlet 會更新前門負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="8b021-115">The **Set-AzFrontDoor** cmdlet updates a Front Door load balancer.</span></span> <span data-ttu-id="8b021-116">如果沒有提供輸入參數，將會使用來自現有前門的舊參數。</span><span class="sxs-lookup"><span data-stu-id="8b021-116">If input parameters are not provided, old parameters from the existing Front Door will be used.</span></span>

## <span data-ttu-id="8b021-117">例子</span><span class="sxs-lookup"><span data-stu-id="8b021-117">EXAMPLES</span></span>

### <span data-ttu-id="8b021-118">範例 1：使用 FrontDoorName 和資源GroupName 更新現有的前門。</span><span class="sxs-lookup"><span data-stu-id="8b021-118">Example 1: update an existing Front Door with FrontDoorName and ResourceGroupName.</span></span>
```powershell
PS C:\> Set-AzFrontDoor -Name "frontDoor1" -ResourceGroupName "resourceGroup1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1 -BackendPoolsSetting $backendPoolsSetting1

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
Id                          : /subscriptions/{guid}/resourcegroups/{guid}/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoors
```

<span data-ttu-id="8b021-119">更新現有的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="8b021-119">update an existing FrontDoor.</span></span>

### <span data-ttu-id="8b021-120">範例 2：使用 PSFrontDoor 物件更新現有的前門。</span><span class="sxs-lookup"><span data-stu-id="8b021-120">Example 2: update an existing Front Door with PSFrontDoor object.</span></span>
```powershell
PS C:\>  Set-AzFrontDoor -InputObject $frontDoor1 -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1 -BackendPoolsSetting $backendPoolsSetting1

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
Id                          : /subscriptions/{guid}/resourcegroups/{guid}/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoor1
```

<span data-ttu-id="8b021-121">更新現有的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="8b021-121">update an existing FrontDoor.</span></span>

### <span data-ttu-id="8b021-122">範例 3：使用 ResourceId 更新現有的前門</span><span class="sxs-lookup"><span data-stu-id="8b021-122">Example 3: update an existing Front Door with ResourceId</span></span>
```powershell
PS C:\>  Set-AzFrontDoor -ResourceId {resourceId} -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1 -BackendPoolsSetting $backendPoolsSetting1

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
Id                          : /subscriptions/{guid}/resourcegroups/{guid}/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoor1
```

<span data-ttu-id="8b021-123">更新現有的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="8b021-123">update an existing FrontDoor.</span></span>

### <span data-ttu-id="8b021-124">範例 4：使用 -DisableCertificateNameCheck 參數更新現有前門的 BackendPoolSetting 屬性 EnforceCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="8b021-124">Example 4: update BackendPoolSetting property EnforceCertificateNameCheck of an existing Front Door with -DisableCertificateNameCheck switch parameter</span></span>
<span data-ttu-id="8b021-125">您可以使用 FrontoorName 和 ResourceGroupName、PSFrontDoor 物件或 ResourceId 來識別要更新的門。</span><span class="sxs-lookup"><span data-stu-id="8b021-125">Front Door to be updated can be identified using FrontoorName and ResourceGroupName, PSFrontDoor object, or ResourceId.</span></span> <span data-ttu-id="8b021-126"> (請參閱上述 3 個範例，例如) 範例使用 PSFrontDoor 物件。</span><span class="sxs-lookup"><span data-stu-id="8b021-126">(See above 3 examples for example) The below example uses PSFrontDoor object.</span></span>

```powershell
PS C:\>  Set-AzFrontDoor -InputObject $frontDoor1 -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1 -DisableCertificateNameCheck

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
BackendPoolsSetting         : {PSBackendPoolsSetting object with EnforceCertificateNameCheck is set to Disabled}
EnforceCertificateNameCheck : Disabled
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

<span data-ttu-id="8b021-127">更新現有的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="8b021-127">update an existing FrontDoor.</span></span>

## <span data-ttu-id="8b021-128">參數</span><span class="sxs-lookup"><span data-stu-id="8b021-128">PARAMETERS</span></span>

### <span data-ttu-id="8b021-129">-後端多工緩衝處理程式</span><span class="sxs-lookup"><span data-stu-id="8b021-129">-BackendPool</span></span>
<span data-ttu-id="8b021-130">路由規則可用的後端多工緩衝處理程式。</span><span class="sxs-lookup"><span data-stu-id="8b021-130">Backendpools available to routing rule.</span></span>

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

### <span data-ttu-id="8b021-131">-後端多工緩衝處理程式設定</span><span class="sxs-lookup"><span data-stu-id="8b021-131">-BackendPoolsSetting</span></span>
<span data-ttu-id="8b021-132">所有後端多工緩衝處理程式的設定。</span><span class="sxs-lookup"><span data-stu-id="8b021-132">Settings for all backendPools.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting
Parameter Sets: ByFieldsWithBackendPoolsSettingParameterSet, ByObjectWithBackendPoolsSettingParameterSet, ByResourceIdWithBackendPoolsSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b021-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b021-133">-DefaultProfile</span></span>
<span data-ttu-id="8b021-134">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8b021-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b021-135">-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="8b021-135">-DisableCertificateNameCheck</span></span>
<span data-ttu-id="8b021-136">是否要停用所有後端資料庫之 HTTPS 要求上的憑證名稱檢查。</span><span class="sxs-lookup"><span data-stu-id="8b021-136">Whether to disable certificate name check on HTTPS requests to all backend pools.</span></span> <span data-ttu-id="8b021-137">對非 HTTPS 要求沒有影響。</span><span class="sxs-lookup"><span data-stu-id="8b021-137">No effect on non-HTTPS requests.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFieldsWithCertificateNameCheckParameterSet, ByObjectWithCertificateNameCheckParameterSet, ByResourceIdWithCertificateNameCheckParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b021-138">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="8b021-138">-EnabledState</span></span>
<span data-ttu-id="8b021-139">前門負載平衡器的運作狀態。</span><span class="sxs-lookup"><span data-stu-id="8b021-139">Operational status of the Front Door load balancer.</span></span>

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

### <span data-ttu-id="8b021-140">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="8b021-140">-FrontendEndpoint</span></span>
<span data-ttu-id="8b021-141">路由規則可用的前端端點。</span><span class="sxs-lookup"><span data-stu-id="8b021-141">Frontend endpoints available to routing rule.</span></span>

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

### <span data-ttu-id="8b021-142">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="8b021-142">-HealthProbeSetting</span></span>
<span data-ttu-id="8b021-143">與此前門實例相關聯的健康情況設定。</span><span class="sxs-lookup"><span data-stu-id="8b021-143">Health probe settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="8b021-144">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b021-144">-InputObject</span></span>
<span data-ttu-id="8b021-145">要更新的門物件。</span><span class="sxs-lookup"><span data-stu-id="8b021-145">The Front Door object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor
Parameter Sets: ByObjectParameterSet, ByObjectWithCertificateNameCheckParameterSet, ByObjectWithBackendPoolsSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b021-146">-LoadBalsettingSetting</span><span class="sxs-lookup"><span data-stu-id="8b021-146">-LoadBalancingSetting</span></span>
<span data-ttu-id="8b021-147">與此前門實例相關聯的負載平衡設定。</span><span class="sxs-lookup"><span data-stu-id="8b021-147">Load balancing settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="8b021-148">-名稱</span><span class="sxs-lookup"><span data-stu-id="8b021-148">-Name</span></span>
<span data-ttu-id="8b021-149">要更新的門名稱。</span><span class="sxs-lookup"><span data-stu-id="8b021-149">The name of the Front Door to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsWithCertificateNameCheckParameterSet, ByFieldsWithBackendPoolsSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b021-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b021-150">-ResourceGroupName</span></span>
<span data-ttu-id="8b021-151">前門所屬的資源群組。</span><span class="sxs-lookup"><span data-stu-id="8b021-151">The resource group to which the Front Door belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsWithCertificateNameCheckParameterSet, ByFieldsWithBackendPoolsSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b021-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b021-152">-ResourceId</span></span>
<span data-ttu-id="8b021-153">要更新之前門的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="8b021-153">Resource Id of the Front Door to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet, ByResourceIdWithCertificateNameCheckParameterSet, ByResourceIdWithBackendPoolsSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b021-154">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="8b021-154">-RoutingRule</span></span>
<span data-ttu-id="8b021-155">與此 FrontDoor 相關聯的路由規則</span><span class="sxs-lookup"><span data-stu-id="8b021-155">Routing rules associated with this FrontDoor</span></span>

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

### <span data-ttu-id="8b021-156">-標記</span><span class="sxs-lookup"><span data-stu-id="8b021-156">-Tag</span></span>
<span data-ttu-id="8b021-157">與 FrontDoor 相關聯的標記。</span><span class="sxs-lookup"><span data-stu-id="8b021-157">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="8b021-158">-確認</span><span class="sxs-lookup"><span data-stu-id="8b021-158">-Confirm</span></span>
<span data-ttu-id="8b021-159">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8b021-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b021-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b021-160">-WhatIf</span></span>
<span data-ttu-id="8b021-161">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8b021-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b021-162">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8b021-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b021-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b021-163">CommonParameters</span></span>
<span data-ttu-id="8b021-164">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8b021-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b021-165">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8b021-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b021-166">輸入</span><span class="sxs-lookup"><span data-stu-id="8b021-166">INPUTS</span></span>

### <span data-ttu-id="8b021-167">Microsoft.Azure.Commands.FrontDoor.models.PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="8b021-167">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>
### <span data-ttu-id="8b021-168">System.String</span><span class="sxs-lookup"><span data-stu-id="8b021-168">System.String</span></span>
## <span data-ttu-id="8b021-169">輸出</span><span class="sxs-lookup"><span data-stu-id="8b021-169">OUTPUTS</span></span>

### <span data-ttu-id="8b021-170">Microsoft.Azure.Commands.FrontDoor.models.PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="8b021-170">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>
## <span data-ttu-id="8b021-171">筆記</span><span class="sxs-lookup"><span data-stu-id="8b021-171">NOTES</span></span>

## <span data-ttu-id="8b021-172">相關連結</span><span class="sxs-lookup"><span data-stu-id="8b021-172">RELATED LINKS</span></span>

<span data-ttu-id="8b021-173">[New-AzFrontDoor](./New-AzFrontDoor.md) 
[Get-AzFrontDoor](./Get-AzFrontDoor.md) 
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md) 
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md) 
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md) 
[New-AzFrontDoorLoadBalsettingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md) 
[New-AzFrontDoorFrontendPointObject](./New-AzFrontDoorFrontendEndpointObject.md) 
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="8b021-173">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Get-AzFrontDoor](./Get-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md)
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md)
[New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md)
[New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md)
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span></span>
