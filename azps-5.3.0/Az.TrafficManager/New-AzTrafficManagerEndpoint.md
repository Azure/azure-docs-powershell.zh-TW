---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: A7A908A1-7326-4725-A3F9-4D05E40C5F73
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/new-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 9a32176afba8f4182ee1300e9b38936e9f35746c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98287988"
---
# <span data-ttu-id="68805-101">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="68805-101">New-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="68805-102">摘要</span><span class="sxs-lookup"><span data-stu-id="68805-102">SYNOPSIS</span></span>
<span data-ttu-id="68805-103">在流量管理器設定檔中建立端點。</span><span class="sxs-lookup"><span data-stu-id="68805-103">Creates an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="68805-104">句法</span><span class="sxs-lookup"><span data-stu-id="68805-104">SYNTAX</span></span>

```
New-AzTrafficManagerEndpoint -Name <String> -ProfileName <String> -ResourceGroupName <String> -Type <String>
 [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68805-105">說明</span><span class="sxs-lookup"><span data-stu-id="68805-105">DESCRIPTION</span></span>
<span data-ttu-id="68805-106">**新的 AzTrafficManagerEndpoint** Cmdlet 會在 Azure 流量管理器設定檔中建立端點。</span><span class="sxs-lookup"><span data-stu-id="68805-106">The **New-AzTrafficManagerEndpoint** cmdlet creates an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="68805-107">這個 Cmdlet 會將每個新端點提交至流量管理器服務。</span><span class="sxs-lookup"><span data-stu-id="68805-107">This cmdlet commits each new endpoint to the Traffic Manager service.</span></span>
<span data-ttu-id="68805-108">若要在本機流量管理器設定檔物件中新增多個端點，並在單一作業中提交變更，請使用 Add-AzTrafficManagerEndpointConfig Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="68805-108">To add multiple endpoints to a local Traffic Manager profile object and commit changes in a single operation, use the Add-AzTrafficManagerEndpointConfig cmdlet.</span></span>

## <span data-ttu-id="68805-109">示例</span><span class="sxs-lookup"><span data-stu-id="68805-109">EXAMPLES</span></span>

### <span data-ttu-id="68805-110">範例1：建立設定檔的外部端點</span><span class="sxs-lookup"><span data-stu-id="68805-110">Example 1: Create an external endpoint for a profile</span></span>
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Target "www.contoso.com" -Weight 10
```

<span data-ttu-id="68805-111">這個命令會在名為 ResourceGroup11 的資源群組中，在名為 ContosoProfile 的設定檔中建立名為 contoso 的外部端點。</span><span class="sxs-lookup"><span data-stu-id="68805-111">This command creates an external endpoint named contoso in the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="68805-112">範例2：建立設定檔的 Azure 端點</span><span class="sxs-lookup"><span data-stu-id="68805-112">Example 2: Create an Azure endpoint for a profile</span></span>
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
```

<span data-ttu-id="68805-113">這個命令會在資源群組 ResourceGroup11 中，在名為 ContosoProfile 的設定檔中建立名為 contoso 的 Azure 端點。</span><span class="sxs-lookup"><span data-stu-id="68805-113">This command creates an Azure endpoint named contoso in the profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="68805-114">Azure 端點指向 azure Web 應用程式，其 Azure 資源管理器 ID 是由 *TargetResourceId* 中的 URI 路徑所提供。</span><span class="sxs-lookup"><span data-stu-id="68805-114">The Azure endpoint points to the Azure Web App whose Azure Resource Manager ID is given by the URI path in *TargetResourceId*.</span></span>
<span data-ttu-id="68805-115">因為 Web App 資源提供位置，所以命令不會指定 *EndpointLocation* 參數。</span><span class="sxs-lookup"><span data-stu-id="68805-115">The command does not specify the *EndpointLocation* parameter because the Web App resource supplies the location.</span></span>

## <span data-ttu-id="68805-116">參數</span><span class="sxs-lookup"><span data-stu-id="68805-116">PARAMETERS</span></span>

### <span data-ttu-id="68805-117">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="68805-117">-CustomHeader</span></span>
<span data-ttu-id="68805-118">針對探測要求的自訂標頭名稱和值對清單。</span><span class="sxs-lookup"><span data-stu-id="68805-118">List of custom header name and value pairs for probe requests.</span></span>

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

### <span data-ttu-id="68805-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68805-119">-DefaultProfile</span></span>
<span data-ttu-id="68805-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="68805-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68805-121">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="68805-121">-EndpointLocation</span></span>
<span data-ttu-id="68805-122">指定要在效能流量路由方法中使用的端點位置。</span><span class="sxs-lookup"><span data-stu-id="68805-122">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="68805-123">這個參數只適用于 ExternalEndpoints 或 NestedEndpoints 類型的端點。</span><span class="sxs-lookup"><span data-stu-id="68805-123">This parameter is only applicable to endpoints of the ExternalEndpoints or NestedEndpoints type.</span></span>
<span data-ttu-id="68805-124">使用效能流量路由方法時，您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="68805-124">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="68805-125">指定 Azure 地區名稱。</span><span class="sxs-lookup"><span data-stu-id="68805-125">Specify an Azure region name.</span></span>
<span data-ttu-id="68805-126">如需 Azure 區域的完整清單，請參閱 Azure 地區 http://azure.microsoft.com/regions/ (http://azure.microsoft.com/regions/) 。</span><span class="sxs-lookup"><span data-stu-id="68805-126">For a full list of Azure regions, see Azure Regionshttp://azure.microsoft.com/regions/ (http://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="68805-127">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="68805-127">-EndpointStatus</span></span>
<span data-ttu-id="68805-128">指定端點的狀態。</span><span class="sxs-lookup"><span data-stu-id="68805-128">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="68805-129">有效值為：</span><span class="sxs-lookup"><span data-stu-id="68805-129">Valid values are:</span></span> 

- <span data-ttu-id="68805-130">後</span><span class="sxs-lookup"><span data-stu-id="68805-130">Enabled</span></span> 
- <span data-ttu-id="68805-131">禁止</span><span class="sxs-lookup"><span data-stu-id="68805-131">Disabled</span></span> 

<span data-ttu-id="68805-132">如果狀態為 [已啟用]，則會針對端點健康情況探測端點，並包含在流量路由方法中。</span><span class="sxs-lookup"><span data-stu-id="68805-132">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

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

### <span data-ttu-id="68805-133">-GeoMapping</span><span class="sxs-lookup"><span data-stu-id="68805-133">-GeoMapping</span></span>
<span data-ttu-id="68805-134">使用 ' 地理 ' 流量路由方法時，對應到此端點的地區清單。</span><span class="sxs-lookup"><span data-stu-id="68805-134">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="68805-135">如需可接受值的完整清單，請參閱流量管理器檔。</span><span class="sxs-lookup"><span data-stu-id="68805-135">Please consult Traffic Manager documentation for a full list of accepted values.</span></span>

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

### <span data-ttu-id="68805-136">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="68805-136">-MinChildEndpoints</span></span>
<span data-ttu-id="68805-137">指定 Azure 地區名稱。</span><span class="sxs-lookup"><span data-stu-id="68805-137">Specify an Azure region name.</span></span>
<span data-ttu-id="68805-138">如需 Azure 區域的完整清單，請參閱 Azure 地區 http://azure.microsoft.com/regions/ (http://azure.microsoft.com/regions/) 。</span><span class="sxs-lookup"><span data-stu-id="68805-138">For a full list of Azure regions, see Azure Regionshttp://azure.microsoft.com/regions/ (http://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="68805-139">-名稱</span><span class="sxs-lookup"><span data-stu-id="68805-139">-Name</span></span>
<span data-ttu-id="68805-140">指定此 Cmdlet 建立之流量管理器端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="68805-140">Specifies the name of the Traffic Manager endpoint that this cmdlet creates.</span></span>

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

### <span data-ttu-id="68805-141">-優先順序</span><span class="sxs-lookup"><span data-stu-id="68805-141">-Priority</span></span>
<span data-ttu-id="68805-142">指定流量管理器指派給端點的優先順序。</span><span class="sxs-lookup"><span data-stu-id="68805-142">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="68805-143">只有在流量管理器設定檔是以優先順序流量路由方法設定的情況下，才能使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="68805-143">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="68805-144">有效的值是從1到1000的整數。</span><span class="sxs-lookup"><span data-stu-id="68805-144">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="68805-145">較低的值代表較高的優先順序。</span><span class="sxs-lookup"><span data-stu-id="68805-145">Lower values represent higher priority.</span></span>

<span data-ttu-id="68805-146">如果您指定優先順序，您必須在設定檔中的所有端點上指定優先順序，而且任何兩個端點都不能共用相同的優先順序值。</span><span class="sxs-lookup"><span data-stu-id="68805-146">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="68805-147">如果您沒有指定優先順序，流量主管會將預設的優先順序值指派給端點，並從一個 (1) 開始，並依照設定檔列出端點的順序進行。</span><span class="sxs-lookup"><span data-stu-id="68805-147">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

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

### <span data-ttu-id="68805-148">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="68805-148">-ProfileName</span></span>
<span data-ttu-id="68805-149">指定此 Cmdlet 新增端點的流量管理器設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="68805-149">Specifies the name of a Traffic Manager profile to which this cmdlet adds an endpoint.</span></span>
<span data-ttu-id="68805-150">若要取得設定檔，請使用 New-AzTrafficManagerProfile 或 Get-AzTrafficManagerProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="68805-150">To obtain a profile, use the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

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

### <span data-ttu-id="68805-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68805-151">-ResourceGroupName</span></span>
<span data-ttu-id="68805-152">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="68805-152">Specifies the name of a resource group.</span></span>
<span data-ttu-id="68805-153">這個 Cmdlet 會在此參數指定的群組中建立流量管理器端點。</span><span class="sxs-lookup"><span data-stu-id="68805-153">This cmdlet creates a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="68805-154">-SubnetMapping</span><span class="sxs-lookup"><span data-stu-id="68805-154">-SubnetMapping</span></span>
<span data-ttu-id="68805-155">使用 ' 子網上流量路由方法」時，對應至此端點的位址範圍或子網清單。</span><span class="sxs-lookup"><span data-stu-id="68805-155">The list of address ranges or subnets mapped to this endpoint when using the 'Subnet' traffic routing method.</span></span>

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

### <span data-ttu-id="68805-156">-目標</span><span class="sxs-lookup"><span data-stu-id="68805-156">-Target</span></span>
<span data-ttu-id="68805-157">指定端點的完整 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="68805-157">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="68805-158">當流量主管將流量導向到此端點時，會在 DNS 回應中傳回這個值。</span><span class="sxs-lookup"><span data-stu-id="68805-158">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="68805-159">請僅針對 ExternalEndpoints 端點類型指定此參數。</span><span class="sxs-lookup"><span data-stu-id="68805-159">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="68805-160">針對其他端點類型，請改為指定 *TargetResourceId* 參數。</span><span class="sxs-lookup"><span data-stu-id="68805-160">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

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

### <span data-ttu-id="68805-161">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="68805-161">-TargetResourceId</span></span>
<span data-ttu-id="68805-162">指定目標的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="68805-162">Specifies resource ID of the target.</span></span>
<span data-ttu-id="68805-163">僅針對 AzureEndpoints 和 NestedEndpoints 端點類型指定此參數。</span><span class="sxs-lookup"><span data-stu-id="68805-163">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="68805-164">針對 ExternalEndpoints 端點類型，請改為指定 *目標* 參數。</span><span class="sxs-lookup"><span data-stu-id="68805-164">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

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

### <span data-ttu-id="68805-165">-類型</span><span class="sxs-lookup"><span data-stu-id="68805-165">-Type</span></span>
<span data-ttu-id="68805-166">指定此 Cmdlet 新增至流量管理器設定檔的端點類型。</span><span class="sxs-lookup"><span data-stu-id="68805-166">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="68805-167">有效值為：</span><span class="sxs-lookup"><span data-stu-id="68805-167">Valid values are:</span></span> 

- <span data-ttu-id="68805-168">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="68805-168">AzureEndpoints</span></span>
- <span data-ttu-id="68805-169">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="68805-169">ExternalEndpoints</span></span>
- <span data-ttu-id="68805-170">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="68805-170">NestedEndpoints</span></span>

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

### <span data-ttu-id="68805-171">寬度</span><span class="sxs-lookup"><span data-stu-id="68805-171">-Weight</span></span>
<span data-ttu-id="68805-172">指定流量主管指派給端點的權重。</span><span class="sxs-lookup"><span data-stu-id="68805-172">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="68805-173">有效的值是從1到1000的整數。</span><span class="sxs-lookup"><span data-stu-id="68805-173">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="68805-174">預設值是一個 (1) 。</span><span class="sxs-lookup"><span data-stu-id="68805-174">The default value is one (1).</span></span>
<span data-ttu-id="68805-175">只有在流量管理器設定檔是使用加權流量路由方法設定的情況下，才能使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="68805-175">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

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

### <span data-ttu-id="68805-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68805-176">CommonParameters</span></span>
<span data-ttu-id="68805-177">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="68805-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68805-178">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="68805-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68805-179">輸入</span><span class="sxs-lookup"><span data-stu-id="68805-179">INPUTS</span></span>

### <span data-ttu-id="68805-180">所有</span><span class="sxs-lookup"><span data-stu-id="68805-180">None</span></span>

## <span data-ttu-id="68805-181">輸出</span><span class="sxs-lookup"><span data-stu-id="68805-181">OUTPUTS</span></span>

### <span data-ttu-id="68805-182">TrafficManagerEndpoint 中的 TrafficManager。</span><span class="sxs-lookup"><span data-stu-id="68805-182">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="68805-183">筆記</span><span class="sxs-lookup"><span data-stu-id="68805-183">NOTES</span></span>

## <span data-ttu-id="68805-184">相關連結</span><span class="sxs-lookup"><span data-stu-id="68805-184">RELATED LINKS</span></span>

[<span data-ttu-id="68805-185">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="68805-185">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="68805-186">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="68805-186">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="68805-187">AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="68805-187">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="68805-188">AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="68805-188">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="68805-189">新-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="68805-189">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="68805-190">移除-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="68805-190">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="68805-191">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="68805-191">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


