---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33D
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: 77bb21030c24d9fed159160262c23e1e821e0fe1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957594"
---
# <span data-ttu-id="4d356-101">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="4d356-101">Add-AzTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="4d356-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4d356-102">SYNOPSIS</span></span>
<span data-ttu-id="4d356-103">將端點新增到本機流量管理器設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="4d356-103">Adds an endpoint to a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="4d356-104">句法</span><span class="sxs-lookup"><span data-stu-id="4d356-104">SYNTAX</span></span>

```
Add-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d356-105">說明</span><span class="sxs-lookup"><span data-stu-id="4d356-105">DESCRIPTION</span></span>
<span data-ttu-id="4d356-106">**AzTrafficManagerEndpointConfig** Cmdlet 會將端點新增到本機 Azure 流量管理器設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="4d356-106">The **Add-AzTrafficManagerEndpointConfig** cmdlet adds an endpoint to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="4d356-107">您可以使用 New-AzTrafficManagerProfile 或 Get-AzTrafficManagerProfile Cmdlet 來取得設定檔。</span><span class="sxs-lookup"><span data-stu-id="4d356-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="4d356-108">這個 Cmdlet 作用於本機設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="4d356-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="4d356-109">使用 Set-AzTrafficManagerProfile Cmdlet，將您的變更提交至流量管理器的設定檔。</span><span class="sxs-lookup"><span data-stu-id="4d356-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="4d356-110">若要建立端點並在單一作業中提交變更，請使用 New-AzTrafficManagerEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4d356-110">To create an endpoint and commit the change in a single operation, use the New-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="4d356-111">示例</span><span class="sxs-lookup"><span data-stu-id="4d356-111">EXAMPLES</span></span>

### <span data-ttu-id="4d356-112">範例1：在設定檔中新增端點</span><span class="sxs-lookup"><span data-stu-id="4d356-112">Example 1: Add an endpoint to a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerEndpointConfig -EndpointName "contoso" -EndpointStatus Enabled -Target "www.contoso.com" -TrafficManagerProfile $TrafficManagerProfile -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Weight 10
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="4d356-113">第一個命令會使用 **AzTrafficManagerProfile** Cmdlet 取得 Azure 流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="4d356-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="4d356-114">該命令會將本機設定檔儲存在 $TrafficManagerProfile 變數中。</span><span class="sxs-lookup"><span data-stu-id="4d356-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="4d356-115">第二個命令會將名為 contoso 的端點新增至儲存在 $TrafficManagerProfile 中的設定檔。</span><span class="sxs-lookup"><span data-stu-id="4d356-115">The second command adds an endpoint named contoso to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="4d356-116">此命令包含端點的配置資料。</span><span class="sxs-lookup"><span data-stu-id="4d356-116">The command includes configuration data for the endpoint.</span></span>
<span data-ttu-id="4d356-117">這個命令只會變更本機物件。</span><span class="sxs-lookup"><span data-stu-id="4d356-117">This command changes only the local object.</span></span>

<span data-ttu-id="4d356-118">Final 命令會更新 Azure 中的流量管理器設定檔，以符合 $TrafficManagerProfile 中的本機值。</span><span class="sxs-lookup"><span data-stu-id="4d356-118">The final command updates the Traffic Manager profile in Azure to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="4d356-119">參數</span><span class="sxs-lookup"><span data-stu-id="4d356-119">PARAMETERS</span></span>

### <span data-ttu-id="4d356-120">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="4d356-120">-CustomHeader</span></span>
<span data-ttu-id="4d356-121">針對探測要求的自訂標頭名稱和值對清單。</span><span class="sxs-lookup"><span data-stu-id="4d356-121">List of custom header name and value pairs for probe requests.</span></span>

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

### <span data-ttu-id="4d356-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d356-122">-DefaultProfile</span></span>
<span data-ttu-id="4d356-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4d356-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d356-124">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="4d356-124">-EndpointLocation</span></span>
<span data-ttu-id="4d356-125">指定要在效能流量路由方法中使用的端點位置。</span><span class="sxs-lookup"><span data-stu-id="4d356-125">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="4d356-126">這個參數只適用于 ExternalEndpoints 或 NestedEndpoints 類型的端點。</span><span class="sxs-lookup"><span data-stu-id="4d356-126">This parameter is only applicable to endpoints of the ExternalEndpoints or the NestedEndpoints type.</span></span>
<span data-ttu-id="4d356-127">使用效能流量路由方法時，您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="4d356-127">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="4d356-128">指定 Azure 地區名稱。</span><span class="sxs-lookup"><span data-stu-id="4d356-128">Specify an Azure region name.</span></span>
<span data-ttu-id="4d356-129">如需 Azure 區域的完整清單，請參閱 Azure 地區 http://azure.microsoft.com/regions/ (http://azure.microsoft.com/regions/) 。</span><span class="sxs-lookup"><span data-stu-id="4d356-129">For a full list of Azure regions, see Azure Regionshttp://azure.microsoft.com/regions/ (http://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="4d356-130">-終結點</span><span class="sxs-lookup"><span data-stu-id="4d356-130">-EndpointName</span></span>
<span data-ttu-id="4d356-131">指定此 Cmdlet 所新增之流量管理器端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="4d356-131">Specifies the name of the Traffic Manager endpoint that this cmdlet adds.</span></span>

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

### <span data-ttu-id="4d356-132">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="4d356-132">-EndpointStatus</span></span>
<span data-ttu-id="4d356-133">指定端點的狀態。</span><span class="sxs-lookup"><span data-stu-id="4d356-133">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="4d356-134">有效值為：</span><span class="sxs-lookup"><span data-stu-id="4d356-134">Valid values are:</span></span> 

- <span data-ttu-id="4d356-135">後</span><span class="sxs-lookup"><span data-stu-id="4d356-135">Enabled</span></span> 
- <span data-ttu-id="4d356-136">禁止</span><span class="sxs-lookup"><span data-stu-id="4d356-136">Disabled</span></span> 

<span data-ttu-id="4d356-137">如果狀態為 [已啟用]，則會針對端點健康情況探測端點，並包含在流量路由方法中。</span><span class="sxs-lookup"><span data-stu-id="4d356-137">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

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

### <span data-ttu-id="4d356-138">-GeoMapping</span><span class="sxs-lookup"><span data-stu-id="4d356-138">-GeoMapping</span></span>
<span data-ttu-id="4d356-139">使用 ' 地理 ' 流量路由方法時，對應到此端點的地區清單。</span><span class="sxs-lookup"><span data-stu-id="4d356-139">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="4d356-140">如需可 [接受值的完整清單](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions)，請參閱流量管理器檔。</span><span class="sxs-lookup"><span data-stu-id="4d356-140">Please consult Traffic Manager documentation for a [full list of accepted values](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions).</span></span>

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

### <span data-ttu-id="4d356-141">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="4d356-141">-MinChildEndpoints</span></span>
<span data-ttu-id="4d356-142">必須在子設定檔中提供的端點的最小數目，才能認為父設定檔中的嵌套端點可供使用。</span><span class="sxs-lookup"><span data-stu-id="4d356-142">The minimum number of endpoints that must be available in the child profile in order for the Nested Endpoint in the parent profile to be considered available.</span></span>
<span data-ttu-id="4d356-143">僅適用于類型 ' NestedEndpoints」的端點。</span><span class="sxs-lookup"><span data-stu-id="4d356-143">Only applicable to endpoint of type 'NestedEndpoints'.</span></span>

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

### <span data-ttu-id="4d356-144">-優先順序</span><span class="sxs-lookup"><span data-stu-id="4d356-144">-Priority</span></span>
<span data-ttu-id="4d356-145">指定流量管理器指派給端點的優先順序。</span><span class="sxs-lookup"><span data-stu-id="4d356-145">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="4d356-146">只有在流量管理器設定檔是以優先順序流量路由方法設定的情況下，才能使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="4d356-146">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="4d356-147">有效的值是從1到1000的整數。</span><span class="sxs-lookup"><span data-stu-id="4d356-147">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="4d356-148">較低的值代表較高的優先順序。</span><span class="sxs-lookup"><span data-stu-id="4d356-148">Lower values represent higher priority.</span></span>

<span data-ttu-id="4d356-149">如果您指定優先順序，您必須在設定檔中的所有端點上指定優先順序，而且任何兩個端點都不能共用相同的優先順序值。</span><span class="sxs-lookup"><span data-stu-id="4d356-149">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="4d356-150">如果您沒有指定優先順序，流量主管會將預設的優先順序值指派給端點，並從一個 (1) 開始，並依照設定檔列出端點的順序進行。</span><span class="sxs-lookup"><span data-stu-id="4d356-150">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

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

### <span data-ttu-id="4d356-151">-SubnetMapping</span><span class="sxs-lookup"><span data-stu-id="4d356-151">-SubnetMapping</span></span>
<span data-ttu-id="4d356-152">使用 ' 子網上流量路由方法」時，對應至此端點的位址範圍或子網清單。</span><span class="sxs-lookup"><span data-stu-id="4d356-152">The list of address ranges or subnets mapped to this endpoint when using the 'Subnet' traffic routing method.</span></span>

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

### <span data-ttu-id="4d356-153">-目標</span><span class="sxs-lookup"><span data-stu-id="4d356-153">-Target</span></span>
<span data-ttu-id="4d356-154">指定端點的完整 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="4d356-154">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="4d356-155">當流量主管將流量導向到此端點時，會在 DNS 回應中傳回這個值。</span><span class="sxs-lookup"><span data-stu-id="4d356-155">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="4d356-156">請僅針對 ExternalEndpoints 端點類型指定此參數。</span><span class="sxs-lookup"><span data-stu-id="4d356-156">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="4d356-157">針對其他端點類型，請改為指定 *TargetResourceId* 參數。</span><span class="sxs-lookup"><span data-stu-id="4d356-157">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

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

### <span data-ttu-id="4d356-158">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="4d356-158">-TargetResourceId</span></span>
<span data-ttu-id="4d356-159">指定目標的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="4d356-159">Specifies resource ID of the target.</span></span>
<span data-ttu-id="4d356-160">僅針對 AzureEndpoints 和 NestedEndpoints 端點類型指定此參數。</span><span class="sxs-lookup"><span data-stu-id="4d356-160">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="4d356-161">針對 ExternalEndpoints 端點類型，請改為指定 *目標* 參數。</span><span class="sxs-lookup"><span data-stu-id="4d356-161">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

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

### <span data-ttu-id="4d356-162">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4d356-162">-TrafficManagerProfile</span></span>
<span data-ttu-id="4d356-163">指定本機 **TrafficManagerProfile** 物件。</span><span class="sxs-lookup"><span data-stu-id="4d356-163">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="4d356-164">這個 Cmdlet 會修改這個本機物件。</span><span class="sxs-lookup"><span data-stu-id="4d356-164">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="4d356-165">若要取得 **TrafficManagerProfile** 物件，請使用 Get-AzTrafficManagerProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4d356-165">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="4d356-166">-類型</span><span class="sxs-lookup"><span data-stu-id="4d356-166">-Type</span></span>
<span data-ttu-id="4d356-167">指定此 Cmdlet 新增至 Azure 流量管理器設定檔的端點類型。</span><span class="sxs-lookup"><span data-stu-id="4d356-167">Specifies the type of endpoint that this cmdlet adds to the Azure Traffic Manager profile.</span></span>
<span data-ttu-id="4d356-168">有效值為：</span><span class="sxs-lookup"><span data-stu-id="4d356-168">Valid values are:</span></span> 

- <span data-ttu-id="4d356-169">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="4d356-169">AzureEndpoints</span></span>
- <span data-ttu-id="4d356-170">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="4d356-170">ExternalEndpoints</span></span>
- <span data-ttu-id="4d356-171">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="4d356-171">NestedEndpoints</span></span>

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

### <span data-ttu-id="4d356-172">寬度</span><span class="sxs-lookup"><span data-stu-id="4d356-172">-Weight</span></span>
<span data-ttu-id="4d356-173">指定流量主管指派給端點的權重。</span><span class="sxs-lookup"><span data-stu-id="4d356-173">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="4d356-174">有效的值是從1到1000的整數。</span><span class="sxs-lookup"><span data-stu-id="4d356-174">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="4d356-175">預設值是一個 (1) 。</span><span class="sxs-lookup"><span data-stu-id="4d356-175">The default value is one (1).</span></span>
<span data-ttu-id="4d356-176">只有在流量管理器設定檔是使用加權流量路由方法設定的情況下，才能使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="4d356-176">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

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

### <span data-ttu-id="4d356-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d356-177">CommonParameters</span></span>
<span data-ttu-id="4d356-178">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4d356-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d356-179">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4d356-179">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d356-180">輸入</span><span class="sxs-lookup"><span data-stu-id="4d356-180">INPUTS</span></span>

### <span data-ttu-id="4d356-181">TrafficManagerProfile 中的 TrafficManager。</span><span class="sxs-lookup"><span data-stu-id="4d356-181">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="4d356-182">輸出</span><span class="sxs-lookup"><span data-stu-id="4d356-182">OUTPUTS</span></span>

### <span data-ttu-id="4d356-183">TrafficManagerProfile 中的 TrafficManager。</span><span class="sxs-lookup"><span data-stu-id="4d356-183">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="4d356-184">筆記</span><span class="sxs-lookup"><span data-stu-id="4d356-184">NOTES</span></span>

## <span data-ttu-id="4d356-185">相關連結</span><span class="sxs-lookup"><span data-stu-id="4d356-185">RELATED LINKS</span></span>

[<span data-ttu-id="4d356-186">AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4d356-186">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="4d356-187">新-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4d356-187">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="4d356-188">移除-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="4d356-188">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="4d356-189">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4d356-189">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


