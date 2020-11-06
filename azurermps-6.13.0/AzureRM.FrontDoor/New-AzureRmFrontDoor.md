---
<span data-ttu-id="8c029-101">外部說明檔案： Microsoft.Azure.Commands.FrontDoor.dll-Help.xml 的模組名稱： AzureRM。 FrontDoor online 版本：對應的 URL 應如下所示： https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoor schema： 2.0.0 content_git_url： https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoor.md original_content_git_url： https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoor.md</span><span class="sxs-lookup"><span data-stu-id="8c029-101">external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml Module Name: AzureRM.FrontDoor online version: The corresponding URL should be the following: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoor schema: 2.0.0 content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoor.md original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoor.md</span></span>
---

# <a name="new-azurermfrontdoor"></a><span data-ttu-id="8c029-102">New-AzureRmFrontDoor</span><span class="sxs-lookup"><span data-stu-id="8c029-102">New-AzureRmFrontDoor</span></span>

## <a name="synopsis"></a><span data-ttu-id="8c029-103">摘要</span><span class="sxs-lookup"><span data-stu-id="8c029-103">SYNOPSIS</span></span>
<span data-ttu-id="8c029-104">建立新的 Azure 前門負載平衡器</span><span class="sxs-lookup"><span data-stu-id="8c029-104">Create a new Azure Front Door load balancer</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <a name="syntax"></a><span data-ttu-id="8c029-105">句法</span><span class="sxs-lookup"><span data-stu-id="8c029-105">SYNTAX</span></span>

```
New-AzureRmFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <a name="description"></a><span data-ttu-id="8c029-106">說明</span><span class="sxs-lookup"><span data-stu-id="8c029-106">DESCRIPTION</span></span>
<span data-ttu-id="8c029-107">**新的-AzureRmFrontDoor** Cmdlet 會在指定資源群組中的 [目前訂閱] 下建立新的 Azure 前門負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="8c029-107">The **New-AzureRmFrontDoor** cmdlet creates a new Azure Front Door load balancer in the specified resource group under current subscription</span></span>

## <a name="examples"></a><span data-ttu-id="8c029-108">示例</span><span class="sxs-lookup"><span data-stu-id="8c029-108">EXAMPLES</span></span>

### <a name="example-1-create-a-front-door-based-on-given-parameters"></a><span data-ttu-id="8c029-109">範例1：根據指定的參數建立前門。</span><span class="sxs-lookup"><span data-stu-id="8c029-109">Example 1: Create a Front Door based on given parameters.</span></span>
```powershell
PS C:\> New-AzureRmFrontDoor -Name "frontDoor1" -ResourceGroupName "rg1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

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
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="8c029-110">根據指定的參數建立一個前門。</span><span class="sxs-lookup"><span data-stu-id="8c029-110">Create a Front Door based on given parameters.</span></span>

## <a name="parameters"></a><span data-ttu-id="8c029-111">參數</span><span class="sxs-lookup"><span data-stu-id="8c029-111">PARAMETERS</span></span>

### <a name="-backendpool"></a><span data-ttu-id="8c029-112">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="8c029-112">-BackendPool</span></span>
<span data-ttu-id="8c029-113">Backendpools 可供路由規則使用。</span><span class="sxs-lookup"><span data-stu-id="8c029-113">Backendpools available to routing rule.</span></span>

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

### <a name="-defaultprofile"></a><span data-ttu-id="8c029-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c029-114">-DefaultProfile</span></span>
<span data-ttu-id="8c029-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8c029-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <a name="-enabledstate"></a><span data-ttu-id="8c029-116">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="8c029-116">-EnabledState</span></span>
<span data-ttu-id="8c029-117">前蓋負載平衡器的 EnabledState。</span><span class="sxs-lookup"><span data-stu-id="8c029-117">EnabledState of the Front Door load balancer.</span></span>
<span data-ttu-id="8c029-118">已啟用預設值</span><span class="sxs-lookup"><span data-stu-id="8c029-118">Default value is Enabled</span></span>

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

### <a name="-frontendendpoint"></a><span data-ttu-id="8c029-119">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="8c029-119">-FrontendEndpoint</span></span>
<span data-ttu-id="8c029-120">可供路由規則使用的前端端點。</span><span class="sxs-lookup"><span data-stu-id="8c029-120">Frontend endpoints available to routing rule.</span></span>

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

### <a name="-healthprobesetting"></a><span data-ttu-id="8c029-121">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="8c029-121">-HealthProbeSetting</span></span>
<span data-ttu-id="8c029-122">與此前門實例相關聯的健康情況探測器設定。</span><span class="sxs-lookup"><span data-stu-id="8c029-122">Health probe settings associated with this Front Door instance.</span></span>

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

### <a name="-loadbalancingsetting"></a><span data-ttu-id="8c029-123">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="8c029-123">-LoadBalancingSetting</span></span>
<span data-ttu-id="8c029-124">與此前門實例相關聯的負載平衡設定。</span><span class="sxs-lookup"><span data-stu-id="8c029-124">Load balancing settings associated with this Front Door instance.</span></span>

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

### <a name="-name"></a><span data-ttu-id="8c029-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="8c029-125">-Name</span></span>
<span data-ttu-id="8c029-126">前門名稱。</span><span class="sxs-lookup"><span data-stu-id="8c029-126">Front Door name.</span></span>

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

### <a name="-resourcegroupname"></a><span data-ttu-id="8c029-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c029-127">-ResourceGroupName</span></span>
<span data-ttu-id="8c029-128">在其中建立前蓋的資源群組名稱。</span><span class="sxs-lookup"><span data-stu-id="8c029-128">The resource group name that the Front Door will be created in.</span></span>

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

### <a name="-routingrule"></a><span data-ttu-id="8c029-129">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="8c029-129">-RoutingRule</span></span>
<span data-ttu-id="8c029-130">與此 FrontDoor 相關聯的路由規則</span><span class="sxs-lookup"><span data-stu-id="8c029-130">Routing rules associated with this FrontDoor</span></span>

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

### <a name="-tag"></a><span data-ttu-id="8c029-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="8c029-131">-Tag</span></span>
<span data-ttu-id="8c029-132">標記與 FrontDoor 相關聯。</span><span class="sxs-lookup"><span data-stu-id="8c029-132">The tags associate with the FrontDoor.</span></span>

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

### <a name="-confirm"></a><span data-ttu-id="8c029-133">-確認</span><span class="sxs-lookup"><span data-stu-id="8c029-133">-Confirm</span></span>
<span data-ttu-id="8c029-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8c029-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <a name="-whatif"></a><span data-ttu-id="8c029-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c029-135">-WhatIf</span></span>
<span data-ttu-id="8c029-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8c029-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c029-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c029-137">The cmdlet is not run.</span></span>

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

### <a name="commonparameters"></a><span data-ttu-id="8c029-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c029-138">CommonParameters</span></span>
<span data-ttu-id="8c029-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8c029-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c029-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8c029-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <a name="inputs"></a><span data-ttu-id="8c029-141">輸入</span><span class="sxs-lookup"><span data-stu-id="8c029-141">INPUTS</span></span>

### <a name="systemstring"></a><span data-ttu-id="8c029-142">System.object</span><span class="sxs-lookup"><span data-stu-id="8c029-142">System.String</span></span>

## <a name="outputs"></a><span data-ttu-id="8c029-143">輸出</span><span class="sxs-lookup"><span data-stu-id="8c029-143">OUTPUTS</span></span>

### <a name="microsoftazurecommandsfrontdoormodelspsfrontdoor"></a><span data-ttu-id="8c029-144">PSFrontDoor 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="8c029-144">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <a name="notes"></a><span data-ttu-id="8c029-145">筆記</span><span class="sxs-lookup"><span data-stu-id="8c029-145">NOTES</span></span>

## <a name="related-links"></a><span data-ttu-id="8c029-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="8c029-146">RELATED LINKS</span></span>

<span data-ttu-id="8c029-147">[AzureRmFrontDoor](./Get-AzureRmFrontDoor.md) 
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md) 
[移除-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md) 
[新-AzureRmFrontDoorRoutingRuleObject](./New-AzureRmFrontDoorRoutingRuleObject.md) 
[新-AzureRmFrontDoorHealthProbeSettingObject](./New-AzureRmFrontHealthProbeSettingObject.md) 
[新-AzureRmFrontDoorLoadBalancingSettingObject](./New-AzureRmFrontDoorLoadBalancingSettingObject.md) 
[新-AzureRmFrontDoorFrontendEndpointObject](./New-AzureRmFrontDoorFrontendEndpointObject.md) 
[新-AzureRmFrontDoorBackendPoolObject](./New-AzureRmFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="8c029-147">[Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)
[Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md)
[New-AzureRmFrontDoorRoutingRuleObject](./New-AzureRmFrontDoorRoutingRuleObject.md)
[New-AzureRmFrontDoorHealthProbeSettingObject](./New-AzureRmFrontHealthProbeSettingObject.md)
[New-AzureRmFrontDoorLoadBalancingSettingObject](./New-AzureRmFrontDoorLoadBalancingSettingObject.md)
[New-AzureRmFrontDoorFrontendEndpointObject](./New-AzureRmFrontDoorFrontendEndpointObject.md)
[New-AzureRmFrontDoorBackendPoolObject](./New-AzureRmFrontDoorBackendPoolObject.md)</span></span>
