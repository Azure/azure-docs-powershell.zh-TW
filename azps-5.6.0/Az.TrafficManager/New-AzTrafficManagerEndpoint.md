---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: A7A908A1-7326-4725-A3F9-4D05E40C5F73
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/new-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 6d9ec806c1456f572991f7c72189c47abbe9ffe8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910850"
---
# <span data-ttu-id="07e17-101">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="07e17-101">New-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="07e17-102">簡介</span><span class="sxs-lookup"><span data-stu-id="07e17-102">SYNOPSIS</span></span>
<span data-ttu-id="07e17-103">在流量管理員設定檔中建立端點。</span><span class="sxs-lookup"><span data-stu-id="07e17-103">Creates an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="07e17-104">語法</span><span class="sxs-lookup"><span data-stu-id="07e17-104">SYNTAX</span></span>

```
New-AzTrafficManagerEndpoint -Name <String> -ProfileName <String> -ResourceGroupName <String> -Type <String>
 [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07e17-105">描述</span><span class="sxs-lookup"><span data-stu-id="07e17-105">DESCRIPTION</span></span>
<span data-ttu-id="07e17-106">**New-AzTrafficManagerEndpoint** Cmdlet 在 Azure 流量管理員設定檔中建立端點。</span><span class="sxs-lookup"><span data-stu-id="07e17-106">The **New-AzTrafficManagerEndpoint** cmdlet creates an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="07e17-107">此 Cmdlet 會向流量管理員服務提交每個新端點。</span><span class="sxs-lookup"><span data-stu-id="07e17-107">This cmdlet commits each new endpoint to the Traffic Manager service.</span></span>
<span data-ttu-id="07e17-108">若要在單一作業中新增多個端點至本地流量管理員設定檔物件並提交變更，請使用 Add-AzTrafficManagerEndpointConfig Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="07e17-108">To add multiple endpoints to a local Traffic Manager profile object and commit changes in a single operation, use the Add-AzTrafficManagerEndpointConfig cmdlet.</span></span>

## <span data-ttu-id="07e17-109">例子</span><span class="sxs-lookup"><span data-stu-id="07e17-109">EXAMPLES</span></span>

### <span data-ttu-id="07e17-110">範例 1：建立設定檔的外部端點</span><span class="sxs-lookup"><span data-stu-id="07e17-110">Example 1: Create an external endpoint for a profile</span></span>
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Target "www.contoso.com" -Weight 10
```

<span data-ttu-id="07e17-111">此命令在資源群組中名為 ContosoProfile 的設定檔中，建立名為 contoso 的外部端點，名為 ResourceGroup11。</span><span class="sxs-lookup"><span data-stu-id="07e17-111">This command creates an external endpoint named contoso in the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="07e17-112">範例 2：建立設定檔的 Azure 端點</span><span class="sxs-lookup"><span data-stu-id="07e17-112">Example 2: Create an Azure endpoint for a profile</span></span>
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
```

<span data-ttu-id="07e17-113">此命令在資源群組 ResourceGroup11 中名為 ContosoProfile 的設定檔中，建立名為 contoso 的 Azure 端點。</span><span class="sxs-lookup"><span data-stu-id="07e17-113">This command creates an Azure endpoint named contoso in the profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="07e17-114">Azure 端點指向 Azure Web App，其 Azure Resource Manager 識別碼是由 *TargetResourceId* 中的 URI 路徑所提供。</span><span class="sxs-lookup"><span data-stu-id="07e17-114">The Azure endpoint points to the Azure Web App whose Azure Resource Manager ID is given by the URI path in *TargetResourceId*.</span></span>
<span data-ttu-id="07e17-115">此命令不會指定 *端點位置* 參數，因為 Web App 資源會提供位置。</span><span class="sxs-lookup"><span data-stu-id="07e17-115">The command does not specify the *EndpointLocation* parameter because the Web App resource supplies the location.</span></span>

## <span data-ttu-id="07e17-116">參數</span><span class="sxs-lookup"><span data-stu-id="07e17-116">PARAMETERS</span></span>

### <span data-ttu-id="07e17-117">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="07e17-117">-CustomHeader</span></span>
<span data-ttu-id="07e17-118">建議要求之自訂標題名稱和值組清單。</span><span class="sxs-lookup"><span data-stu-id="07e17-118">List of custom header name and value pairs for probe requests.</span></span>

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

### <span data-ttu-id="07e17-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07e17-119">-DefaultProfile</span></span>
<span data-ttu-id="07e17-120">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="07e17-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07e17-121">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="07e17-121">-EndpointLocation</span></span>
<span data-ttu-id="07e17-122">指定要用於 Performance 流量路由方法的端點位置。</span><span class="sxs-lookup"><span data-stu-id="07e17-122">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="07e17-123">此參數僅適用于 ExternalEndpoints 或 NestedEndpoints 類型的端點。</span><span class="sxs-lookup"><span data-stu-id="07e17-123">This parameter is only applicable to endpoints of the ExternalEndpoints or NestedEndpoints type.</span></span>
<span data-ttu-id="07e17-124">使用 Performance 流量路由方法時，您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="07e17-124">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="07e17-125">指定 Azure 地區名稱。</span><span class="sxs-lookup"><span data-stu-id="07e17-125">Specify an Azure region name.</span></span>
<span data-ttu-id="07e17-126">有關 Azure 區域的完整清單，請參閱 Azure 區域 http://azure.microsoft.com/regions/ http://azure.microsoft.com/regions/) (。</span><span class="sxs-lookup"><span data-stu-id="07e17-126">For a full list of Azure regions, see Azure Regionshttp://azure.microsoft.com/regions/ (http://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="07e17-127">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="07e17-127">-EndpointStatus</span></span>
<span data-ttu-id="07e17-128">指定端點的狀態。</span><span class="sxs-lookup"><span data-stu-id="07e17-128">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="07e17-129">有效的值為：</span><span class="sxs-lookup"><span data-stu-id="07e17-129">Valid values are:</span></span> 

- <span data-ttu-id="07e17-130">啟用</span><span class="sxs-lookup"><span data-stu-id="07e17-130">Enabled</span></span> 
- <span data-ttu-id="07e17-131">禁用</span><span class="sxs-lookup"><span data-stu-id="07e17-131">Disabled</span></span> 

<span data-ttu-id="07e17-132">如果狀態為 Enabled，端點會針對端點健康情況進行安排，並包含在流量路由方法中。</span><span class="sxs-lookup"><span data-stu-id="07e17-132">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

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

### <span data-ttu-id="07e17-133">-GeoMapping</span><span class="sxs-lookup"><span data-stu-id="07e17-133">-GeoMapping</span></span>
<span data-ttu-id="07e17-134">使用'地理'流量路由方法時對應到此端點的區域清單。</span><span class="sxs-lookup"><span data-stu-id="07e17-134">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="07e17-135">如需接受值的完整清單，請參閱流量管理員檔。</span><span class="sxs-lookup"><span data-stu-id="07e17-135">Please consult Traffic Manager documentation for a full list of accepted values.</span></span>

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

### <span data-ttu-id="07e17-136">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="07e17-136">-MinChildEndpoints</span></span>
<span data-ttu-id="07e17-137">指定 Azure 地區名稱。</span><span class="sxs-lookup"><span data-stu-id="07e17-137">Specify an Azure region name.</span></span>
<span data-ttu-id="07e17-138">有關 Azure 區域的完整清單，請參閱 Azure 區域 http://azure.microsoft.com/regions/ http://azure.microsoft.com/regions/) (。</span><span class="sxs-lookup"><span data-stu-id="07e17-138">For a full list of Azure regions, see Azure Regionshttp://azure.microsoft.com/regions/ (http://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="07e17-139">-名稱</span><span class="sxs-lookup"><span data-stu-id="07e17-139">-Name</span></span>
<span data-ttu-id="07e17-140">指定此 Cmdlet 所建立的流量管理員端點名稱。</span><span class="sxs-lookup"><span data-stu-id="07e17-140">Specifies the name of the Traffic Manager endpoint that this cmdlet creates.</span></span>

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

### <span data-ttu-id="07e17-141">-優先順序</span><span class="sxs-lookup"><span data-stu-id="07e17-141">-Priority</span></span>
<span data-ttu-id="07e17-142">指定流量管理員指派給端點的優先順序。</span><span class="sxs-lookup"><span data-stu-id="07e17-142">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="07e17-143">只有在流量管理員設定檔設定為優先順序流量路由方法時，才能使用此參數。</span><span class="sxs-lookup"><span data-stu-id="07e17-143">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="07e17-144">有效值是 1 到 1000 的整數。</span><span class="sxs-lookup"><span data-stu-id="07e17-144">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="07e17-145">較低值代表較高的優先順序。</span><span class="sxs-lookup"><span data-stu-id="07e17-145">Lower values represent higher priority.</span></span>

<span data-ttu-id="07e17-146">如果您指定優先順序，則必須指定設定檔中所有端點的優先順序，而且沒有兩個端點可以共用相同的優先順序值。</span><span class="sxs-lookup"><span data-stu-id="07e17-146">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="07e17-147">如果您未指定優先順序，流量管理員會以設定檔列出端點的順序，為端點指派預設優先順序值，從 (1) 開始。</span><span class="sxs-lookup"><span data-stu-id="07e17-147">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

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

### <span data-ttu-id="07e17-148">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="07e17-148">-ProfileName</span></span>
<span data-ttu-id="07e17-149">指定此 Cmdlet 新增端點的流量管理員設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="07e17-149">Specifies the name of a Traffic Manager profile to which this cmdlet adds an endpoint.</span></span>
<span data-ttu-id="07e17-150">若要取得設定檔，請使用New-AzTrafficManagerProfile或Get-AzTrafficManagerProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="07e17-150">To obtain a profile, use the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

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

### <span data-ttu-id="07e17-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07e17-151">-ResourceGroupName</span></span>
<span data-ttu-id="07e17-152">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="07e17-152">Specifies the name of a resource group.</span></span>
<span data-ttu-id="07e17-153">此 Cmdlet 會在此參數指定的群組中建立流量管理員端點。</span><span class="sxs-lookup"><span data-stu-id="07e17-153">This cmdlet creates a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="07e17-154">-子網映射</span><span class="sxs-lookup"><span data-stu-id="07e17-154">-SubnetMapping</span></span>
<span data-ttu-id="07e17-155">使用子網流量路由方法時，對應到此端點的位址範圍或子網清單。</span><span class="sxs-lookup"><span data-stu-id="07e17-155">The list of address ranges or subnets mapped to this endpoint when using the 'Subnet' traffic routing method.</span></span>

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

### <span data-ttu-id="07e17-156">-目標</span><span class="sxs-lookup"><span data-stu-id="07e17-156">-Target</span></span>
<span data-ttu-id="07e17-157">指定端點的完全 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="07e17-157">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="07e17-158">流量管理員在將流量引導至此端點時，會于 DNS 回應中回回此值。</span><span class="sxs-lookup"><span data-stu-id="07e17-158">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="07e17-159">僅針對 ExternalEndpoints 端點類型指定此參數。</span><span class="sxs-lookup"><span data-stu-id="07e17-159">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="07e17-160">針對其他端點類型，請改為指定 *TargetResourceId* 參數。</span><span class="sxs-lookup"><span data-stu-id="07e17-160">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

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

### <span data-ttu-id="07e17-161">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="07e17-161">-TargetResourceId</span></span>
<span data-ttu-id="07e17-162">指定目標的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="07e17-162">Specifies resource ID of the target.</span></span>
<span data-ttu-id="07e17-163">僅針對 AzureEndpoints 和 NestedEndpoints 端點類型指定此參數。</span><span class="sxs-lookup"><span data-stu-id="07e17-163">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="07e17-164">針對 ExternalEndpoints 端點類型，請改為指定 *Target* 參數。</span><span class="sxs-lookup"><span data-stu-id="07e17-164">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

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

### <span data-ttu-id="07e17-165">-類型</span><span class="sxs-lookup"><span data-stu-id="07e17-165">-Type</span></span>
<span data-ttu-id="07e17-166">指定此 Cmdlet 新增到流量管理員設定檔的端點類型。</span><span class="sxs-lookup"><span data-stu-id="07e17-166">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="07e17-167">有效的值為：</span><span class="sxs-lookup"><span data-stu-id="07e17-167">Valid values are:</span></span> 

- <span data-ttu-id="07e17-168">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="07e17-168">AzureEndpoints</span></span>
- <span data-ttu-id="07e17-169">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="07e17-169">ExternalEndpoints</span></span>
- <span data-ttu-id="07e17-170">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="07e17-170">NestedEndpoints</span></span>

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

### <span data-ttu-id="07e17-171">-重量</span><span class="sxs-lookup"><span data-stu-id="07e17-171">-Weight</span></span>
<span data-ttu-id="07e17-172">指定流量管理員指派給端點的粗細。</span><span class="sxs-lookup"><span data-stu-id="07e17-172">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="07e17-173">有效值是 1 到 1000 的整數。</span><span class="sxs-lookup"><span data-stu-id="07e17-173">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="07e17-174">預設值為 1 (1) 。</span><span class="sxs-lookup"><span data-stu-id="07e17-174">The default value is one (1).</span></span>
<span data-ttu-id="07e17-175">只有在使用加權流量路由方法設定流量管理員設定檔時，才能使用此參數。</span><span class="sxs-lookup"><span data-stu-id="07e17-175">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

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

### <span data-ttu-id="07e17-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07e17-176">CommonParameters</span></span>
<span data-ttu-id="07e17-177">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="07e17-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07e17-178">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="07e17-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07e17-179">輸入</span><span class="sxs-lookup"><span data-stu-id="07e17-179">INPUTS</span></span>

### <span data-ttu-id="07e17-180">沒有</span><span class="sxs-lookup"><span data-stu-id="07e17-180">None</span></span>

## <span data-ttu-id="07e17-181">輸出</span><span class="sxs-lookup"><span data-stu-id="07e17-181">OUTPUTS</span></span>

### <span data-ttu-id="07e17-182">Microsoft.Azure.Commands.TrafficManager.models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="07e17-182">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="07e17-183">筆記</span><span class="sxs-lookup"><span data-stu-id="07e17-183">NOTES</span></span>

## <span data-ttu-id="07e17-184">相關連結</span><span class="sxs-lookup"><span data-stu-id="07e17-184">RELATED LINKS</span></span>

[<span data-ttu-id="07e17-185">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="07e17-185">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="07e17-186">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="07e17-186">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="07e17-187">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="07e17-187">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="07e17-188">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="07e17-188">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="07e17-189">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="07e17-189">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="07e17-190">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="07e17-190">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="07e17-191">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="07e17-191">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


