---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33D
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/add-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: 79e3547a8065b20b693b05b7fe4582bbd775abdd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910877"
---
# <span data-ttu-id="e3a79-101">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="e3a79-101">Add-AzTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="e3a79-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e3a79-102">SYNOPSIS</span></span>
<span data-ttu-id="e3a79-103">新增端點至本地流量管理員設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="e3a79-103">Adds an endpoint to a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="e3a79-104">語法</span><span class="sxs-lookup"><span data-stu-id="e3a79-104">SYNTAX</span></span>

```
Add-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3a79-105">描述</span><span class="sxs-lookup"><span data-stu-id="e3a79-105">DESCRIPTION</span></span>
<span data-ttu-id="e3a79-106">**Add-AzTrafficManagerEndpointConfig** Cmdlet 會新增端點至本地 Azure 流量管理員設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="e3a79-106">The **Add-AzTrafficManagerEndpointConfig** cmdlet adds an endpoint to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="e3a79-107">您可以使用 Cmdlet 或 Cmdlet New-AzTrafficManagerProfile或Get-AzTrafficManagerProfile設定檔。</span><span class="sxs-lookup"><span data-stu-id="e3a79-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="e3a79-108">此 Cmdlet 可在本地設定檔物件上操作。</span><span class="sxs-lookup"><span data-stu-id="e3a79-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="e3a79-109">使用 Cmdlet 來針對流量管理員的設定檔Set-AzTrafficManagerProfile變更。</span><span class="sxs-lookup"><span data-stu-id="e3a79-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="e3a79-110">若要在單一作業中建立端點並提交變更，請使用 New-AzTrafficManagerEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e3a79-110">To create an endpoint and commit the change in a single operation, use the New-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="e3a79-111">例子</span><span class="sxs-lookup"><span data-stu-id="e3a79-111">EXAMPLES</span></span>

### <span data-ttu-id="e3a79-112">範例 1：新增端點至設定檔</span><span class="sxs-lookup"><span data-stu-id="e3a79-112">Example 1: Add an endpoint to a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerEndpointConfig -EndpointName "contoso" -EndpointStatus Enabled -Target "www.contoso.com" -TrafficManagerProfile $TrafficManagerProfile -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Weight 10
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="e3a79-113">第一個命令會使用 **Get-AzTrafficManagerProfile** Cmdlet 取得 Azure 流量管理員設定檔。</span><span class="sxs-lookup"><span data-stu-id="e3a79-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="e3a79-114">該命令將本地設定檔儲存在 $TrafficManagerProfile 變數中。</span><span class="sxs-lookup"><span data-stu-id="e3a79-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="e3a79-115">第二個命令會將名為 contoso 的端點新增到儲存在 $TrafficManagerProfile。</span><span class="sxs-lookup"><span data-stu-id="e3a79-115">The second command adds an endpoint named contoso to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="e3a79-116">該命令包含端點的群組原則資料。</span><span class="sxs-lookup"><span data-stu-id="e3a79-116">The command includes configuration data for the endpoint.</span></span>
<span data-ttu-id="e3a79-117">此命令只會變更本機物件。</span><span class="sxs-lookup"><span data-stu-id="e3a79-117">This command changes only the local object.</span></span>

<span data-ttu-id="e3a79-118">最後一個命令會更新 Azure 中的流量管理員設定檔，以與 $TrafficManagerProfile。</span><span class="sxs-lookup"><span data-stu-id="e3a79-118">The final command updates the Traffic Manager profile in Azure to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="e3a79-119">參數</span><span class="sxs-lookup"><span data-stu-id="e3a79-119">PARAMETERS</span></span>

### <span data-ttu-id="e3a79-120">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="e3a79-120">-CustomHeader</span></span>
<span data-ttu-id="e3a79-121">建議要求之自訂標題名稱和值組清單。</span><span class="sxs-lookup"><span data-stu-id="e3a79-121">List of custom header name and value pairs for probe requests.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3a79-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3a79-122">-DefaultProfile</span></span>
<span data-ttu-id="e3a79-123">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e3a79-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3a79-124">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="e3a79-124">-EndpointLocation</span></span>
<span data-ttu-id="e3a79-125">指定要用於 Performance 流量路由方法的端點位置。</span><span class="sxs-lookup"><span data-stu-id="e3a79-125">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="e3a79-126">此參數僅適用于 ExternalEndpoints 或 NestedEndpoints 類型的端點。</span><span class="sxs-lookup"><span data-stu-id="e3a79-126">This parameter is only applicable to endpoints of the ExternalEndpoints or the NestedEndpoints type.</span></span>
<span data-ttu-id="e3a79-127">使用 Performance 流量路由方法時，您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="e3a79-127">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="e3a79-128">指定 Azure 地區名稱。</span><span class="sxs-lookup"><span data-stu-id="e3a79-128">Specify an Azure region name.</span></span>
<span data-ttu-id="e3a79-129">有關 Azure 區域的完整清單，請參閱 Azure 區域 http://azure.microsoft.com/regions/ http://azure.microsoft.com/regions/) (。</span><span class="sxs-lookup"><span data-stu-id="e3a79-129">For a full list of Azure regions, see Azure Regionshttp://azure.microsoft.com/regions/ (http://azure.microsoft.com/regions/).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3a79-130">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e3a79-130">-EndpointName</span></span>
<span data-ttu-id="e3a79-131">指定此 Cmdlet 新增的流量管理員端點名稱。</span><span class="sxs-lookup"><span data-stu-id="e3a79-131">Specifies the name of the Traffic Manager endpoint that this cmdlet adds.</span></span>

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

### <span data-ttu-id="e3a79-132">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="e3a79-132">-EndpointStatus</span></span>
<span data-ttu-id="e3a79-133">指定端點的狀態。</span><span class="sxs-lookup"><span data-stu-id="e3a79-133">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="e3a79-134">有效的值為：</span><span class="sxs-lookup"><span data-stu-id="e3a79-134">Valid values are:</span></span> 

- <span data-ttu-id="e3a79-135">啟用</span><span class="sxs-lookup"><span data-stu-id="e3a79-135">Enabled</span></span> 
- <span data-ttu-id="e3a79-136">禁用</span><span class="sxs-lookup"><span data-stu-id="e3a79-136">Disabled</span></span> 

<span data-ttu-id="e3a79-137">如果狀態為 Enabled，端點會針對端點健康情況進行安排，並包含在流量路由方法中。</span><span class="sxs-lookup"><span data-stu-id="e3a79-137">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3a79-138">-GeoMapping</span><span class="sxs-lookup"><span data-stu-id="e3a79-138">-GeoMapping</span></span>
<span data-ttu-id="e3a79-139">使用'地理'流量路由方法時對應到此端點的區域清單。</span><span class="sxs-lookup"><span data-stu-id="e3a79-139">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="e3a79-140">如需接受值的完整清單，請參閱流量管理員 [檔](https://docs.microsoft.com/azure/traffic-manager/traffic-manager-geographic-regions)。</span><span class="sxs-lookup"><span data-stu-id="e3a79-140">Please consult Traffic Manager documentation for a [full list of accepted values](https://docs.microsoft.com/azure/traffic-manager/traffic-manager-geographic-regions).</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3a79-141">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="e3a79-141">-MinChildEndpoints</span></span>
<span data-ttu-id="e3a79-142">若要將父設定檔中的巢式端點視為可用，子設定檔中必須有的端點數目為最小值。</span><span class="sxs-lookup"><span data-stu-id="e3a79-142">The minimum number of endpoints that must be available in the child profile in order for the Nested Endpoint in the parent profile to be considered available.</span></span>
<span data-ttu-id="e3a79-143">僅適用于類型為 "NestedEndpoints" 的端點。</span><span class="sxs-lookup"><span data-stu-id="e3a79-143">Only applicable to endpoint of type 'NestedEndpoints'.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3a79-144">-優先順序</span><span class="sxs-lookup"><span data-stu-id="e3a79-144">-Priority</span></span>
<span data-ttu-id="e3a79-145">指定流量管理員指派給端點的優先順序。</span><span class="sxs-lookup"><span data-stu-id="e3a79-145">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="e3a79-146">只有在流量管理員設定檔設定為優先順序流量路由方法時，才能使用此參數。</span><span class="sxs-lookup"><span data-stu-id="e3a79-146">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="e3a79-147">有效值是 1 到 1000 的整數。</span><span class="sxs-lookup"><span data-stu-id="e3a79-147">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="e3a79-148">較低值代表較高的優先順序。</span><span class="sxs-lookup"><span data-stu-id="e3a79-148">Lower values represent higher priority.</span></span>

<span data-ttu-id="e3a79-149">如果您指定優先順序，則必須指定設定檔中所有端點的優先順序，而且沒有兩個端點可以共用相同的優先順序值。</span><span class="sxs-lookup"><span data-stu-id="e3a79-149">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="e3a79-150">如果您未指定優先順序，流量管理員會以設定檔列出端點的順序，為端點指派預設優先順序值，從 (1) 開始。</span><span class="sxs-lookup"><span data-stu-id="e3a79-150">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3a79-151">-子網映射</span><span class="sxs-lookup"><span data-stu-id="e3a79-151">-SubnetMapping</span></span>
<span data-ttu-id="e3a79-152">使用子網流量路由方法時，對應到此端點的位址範圍或子網清單。</span><span class="sxs-lookup"><span data-stu-id="e3a79-152">The list of address ranges or subnets mapped to this endpoint when using the 'Subnet' traffic routing method.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3a79-153">-目標</span><span class="sxs-lookup"><span data-stu-id="e3a79-153">-Target</span></span>
<span data-ttu-id="e3a79-154">指定端點的完全 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="e3a79-154">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="e3a79-155">流量管理員在將流量引導至此端點時，會于 DNS 回應中回回此值。</span><span class="sxs-lookup"><span data-stu-id="e3a79-155">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="e3a79-156">僅針對 ExternalEndpoints 端點類型指定此參數。</span><span class="sxs-lookup"><span data-stu-id="e3a79-156">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="e3a79-157">針對其他端點類型，請改為指定 *TargetResourceId* 參數。</span><span class="sxs-lookup"><span data-stu-id="e3a79-157">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3a79-158">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="e3a79-158">-TargetResourceId</span></span>
<span data-ttu-id="e3a79-159">指定目標的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e3a79-159">Specifies resource ID of the target.</span></span>
<span data-ttu-id="e3a79-160">僅針對 AzureEndpoints 和 NestedEndpoints 端點類型指定此參數。</span><span class="sxs-lookup"><span data-stu-id="e3a79-160">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="e3a79-161">針對 ExternalEndpoints 端點類型，請改為指定 *Target* 參數。</span><span class="sxs-lookup"><span data-stu-id="e3a79-161">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3a79-162">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e3a79-162">-TrafficManagerProfile</span></span>
<span data-ttu-id="e3a79-163">指定一個本地 **TrafficManagerProfile** 物件。</span><span class="sxs-lookup"><span data-stu-id="e3a79-163">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="e3a79-164">此 Cmdlet 會修改此本機物件。</span><span class="sxs-lookup"><span data-stu-id="e3a79-164">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="e3a79-165">若要取得 **TrafficManagerProfile** 物件，請使用 Get-AzTrafficManagerProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e3a79-165">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3a79-166">-類型</span><span class="sxs-lookup"><span data-stu-id="e3a79-166">-Type</span></span>
<span data-ttu-id="e3a79-167">指定此 Cmdlet 新增到 Azure 流量管理員設定檔的端點類型。</span><span class="sxs-lookup"><span data-stu-id="e3a79-167">Specifies the type of endpoint that this cmdlet adds to the Azure Traffic Manager profile.</span></span>
<span data-ttu-id="e3a79-168">有效的值為：</span><span class="sxs-lookup"><span data-stu-id="e3a79-168">Valid values are:</span></span> 

- <span data-ttu-id="e3a79-169">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="e3a79-169">AzureEndpoints</span></span>
- <span data-ttu-id="e3a79-170">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="e3a79-170">ExternalEndpoints</span></span>
- <span data-ttu-id="e3a79-171">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="e3a79-171">NestedEndpoints</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3a79-172">-重量</span><span class="sxs-lookup"><span data-stu-id="e3a79-172">-Weight</span></span>
<span data-ttu-id="e3a79-173">指定流量管理員指派給端點的粗細。</span><span class="sxs-lookup"><span data-stu-id="e3a79-173">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="e3a79-174">有效值是 1 到 1000 的整數。</span><span class="sxs-lookup"><span data-stu-id="e3a79-174">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="e3a79-175">預設值為 1 (1) 。</span><span class="sxs-lookup"><span data-stu-id="e3a79-175">The default value is one (1).</span></span>
<span data-ttu-id="e3a79-176">只有在使用加權流量路由方法設定流量管理員設定檔時，才能使用此參數。</span><span class="sxs-lookup"><span data-stu-id="e3a79-176">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3a79-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3a79-177">CommonParameters</span></span>
<span data-ttu-id="e3a79-178">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e3a79-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3a79-179">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="e3a79-179">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3a79-180">輸入</span><span class="sxs-lookup"><span data-stu-id="e3a79-180">INPUTS</span></span>

### <span data-ttu-id="e3a79-181">Microsoft.Azure.Commands.TrafficManager.models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e3a79-181">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="e3a79-182">輸出</span><span class="sxs-lookup"><span data-stu-id="e3a79-182">OUTPUTS</span></span>

### <span data-ttu-id="e3a79-183">Microsoft.Azure.Commands.TrafficManager.models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e3a79-183">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="e3a79-184">筆記</span><span class="sxs-lookup"><span data-stu-id="e3a79-184">NOTES</span></span>

## <span data-ttu-id="e3a79-185">相關連結</span><span class="sxs-lookup"><span data-stu-id="e3a79-185">RELATED LINKS</span></span>

[<span data-ttu-id="e3a79-186">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e3a79-186">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="e3a79-187">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e3a79-187">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="e3a79-188">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="e3a79-188">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="e3a79-189">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e3a79-189">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


