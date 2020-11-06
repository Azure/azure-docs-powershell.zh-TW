---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerEndpointConfig.md
ms.openlocfilehash: f2abe6acd0406f78ba2bb691b562cd0bcbffeb35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444896"
---
# <span data-ttu-id="68869-101">Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="68869-101">Add-AzureRmTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="68869-102">摘要</span><span class="sxs-lookup"><span data-stu-id="68869-102">SYNOPSIS</span></span>
<span data-ttu-id="68869-103">將端點新增到本機流量管理器設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="68869-103">Adds an endpoint to a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68869-104">句法</span><span class="sxs-lookup"><span data-stu-id="68869-104">SYNTAX</span></span>

```
Add-AzureRmTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="68869-105">說明</span><span class="sxs-lookup"><span data-stu-id="68869-105">DESCRIPTION</span></span>
<span data-ttu-id="68869-106">**AzureRmTrafficManagerEndpointConfig** Cmdlet 會將端點新增到本機 Azure 流量管理器設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="68869-106">The **Add-AzureRmTrafficManagerEndpointConfig** cmdlet adds an endpoint to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="68869-107">您可以使用 New-AzureRmTrafficManagerProfile 或 Get-AzureRmTrafficManagerProfile Cmdlet 來取得設定檔。</span><span class="sxs-lookup"><span data-stu-id="68869-107">You can get a profile by using the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="68869-108">這個 Cmdlet 作用於本機設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="68869-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="68869-109">使用 Set-AzureRmTrafficManagerProfile Cmdlet，將您的變更提交至流量管理器的設定檔。</span><span class="sxs-lookup"><span data-stu-id="68869-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="68869-110">若要建立端點並在單一作業中提交變更，請使用 New-AzureRmTrafficManagerEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="68869-110">To create an endpoint and commit the change in a single operation, use the New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="68869-111">示例</span><span class="sxs-lookup"><span data-stu-id="68869-111">EXAMPLES</span></span>

### <span data-ttu-id="68869-112">範例1：在設定檔中新增端點</span><span class="sxs-lookup"><span data-stu-id="68869-112">Example 1: Add an endpoint to a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzureRmTrafficManagerEndpointConfig -EndpointName "contoso" -EndpointStatus Enabled -Target "www.contoso.com" -TrafficManagerProfile $TrafficManagerProfile -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Weight 10
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="68869-113">第一個命令會使用 **AzureRmTrafficManagerProfile** Cmdlet 取得 Azure 流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="68869-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="68869-114">該命令會將本機設定檔儲存在 $TrafficManagerProfile 變數中。</span><span class="sxs-lookup"><span data-stu-id="68869-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="68869-115">第二個命令會將名為 contoso 的端點新增至儲存在 $TrafficManagerProfile 中的設定檔。</span><span class="sxs-lookup"><span data-stu-id="68869-115">The second command adds an endpoint named contoso to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="68869-116">此命令包含端點的配置資料。</span><span class="sxs-lookup"><span data-stu-id="68869-116">The command includes configuration data for the endpoint.</span></span>
<span data-ttu-id="68869-117">這個命令只會變更本機物件。</span><span class="sxs-lookup"><span data-stu-id="68869-117">This command changes only the local object.</span></span>

<span data-ttu-id="68869-118">Final 命令會更新 Azure 中的流量管理器設定檔，以符合 $TrafficManagerProfile 中的本機值。</span><span class="sxs-lookup"><span data-stu-id="68869-118">The final command updates the Traffic Manager profile in Azure to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="68869-119">參數</span><span class="sxs-lookup"><span data-stu-id="68869-119">PARAMETERS</span></span>

### <span data-ttu-id="68869-120">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="68869-120">-EndpointLocation</span></span>
<span data-ttu-id="68869-121">指定要在效能流量路由方法中使用的端點位置。</span><span class="sxs-lookup"><span data-stu-id="68869-121">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="68869-122">這個參數只適用于 ExternalEndpoints 或 NestedEndpoints 類型的端點。</span><span class="sxs-lookup"><span data-stu-id="68869-122">This parameter is only applicable to endpoints of the ExternalEndpoints or the NestedEndpoints type.</span></span>
<span data-ttu-id="68869-123">使用效能流量路由方法時，您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="68869-123">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="68869-124">指定 Azure 地區名稱。</span><span class="sxs-lookup"><span data-stu-id="68869-124">Specify an Azure region name.</span></span>
<span data-ttu-id="68869-125">如需 Azure 區域的完整清單，請參閱 Azure 地區 https://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/) 。</span><span class="sxs-lookup"><span data-stu-id="68869-125">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="68869-126">-終結點</span><span class="sxs-lookup"><span data-stu-id="68869-126">-EndpointName</span></span>
<span data-ttu-id="68869-127">指定此 Cmdlet 所新增之流量管理器端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="68869-127">Specifies the name of the Traffic Manager endpoint that this cmdlet adds.</span></span>

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

### <span data-ttu-id="68869-128">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="68869-128">-EndpointStatus</span></span>
<span data-ttu-id="68869-129">指定端點的狀態。</span><span class="sxs-lookup"><span data-stu-id="68869-129">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="68869-130">有效值為：</span><span class="sxs-lookup"><span data-stu-id="68869-130">Valid values are:</span></span> 

- <span data-ttu-id="68869-131">後</span><span class="sxs-lookup"><span data-stu-id="68869-131">Enabled</span></span> 
- <span data-ttu-id="68869-132">禁止</span><span class="sxs-lookup"><span data-stu-id="68869-132">Disabled</span></span> 

<span data-ttu-id="68869-133">如果狀態為 [已啟用]，則會針對端點健康情況探測端點，並包含在流量路由方法中。</span><span class="sxs-lookup"><span data-stu-id="68869-133">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

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

### <span data-ttu-id="68869-134">-GeoMapping</span><span class="sxs-lookup"><span data-stu-id="68869-134">-GeoMapping</span></span>
<span data-ttu-id="68869-135">使用 ' 地理 ' 流量路由方法時，對應到此端點的地區清單。</span><span class="sxs-lookup"><span data-stu-id="68869-135">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="68869-136">如需可 [接受值的完整清單](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions)，請參閱流量管理器檔。</span><span class="sxs-lookup"><span data-stu-id="68869-136">Please consult Traffic Manager documentation for a [full list of accepted values](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions).</span></span>
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

### <span data-ttu-id="68869-137">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="68869-137">-MinChildEndpoints</span></span>
<span data-ttu-id="68869-138">指定 Azure 地區名稱。</span><span class="sxs-lookup"><span data-stu-id="68869-138">Specify an Azure region name.</span></span>
<span data-ttu-id="68869-139">如需 Azure 區域的完整清單，請參閱 Azure 地區 https://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/) 。</span><span class="sxs-lookup"><span data-stu-id="68869-139">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="68869-140">-優先順序</span><span class="sxs-lookup"><span data-stu-id="68869-140">-Priority</span></span>
<span data-ttu-id="68869-141">指定流量管理器指派給端點的優先順序。</span><span class="sxs-lookup"><span data-stu-id="68869-141">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="68869-142">只有在流量管理器設定檔是以優先順序流量路由方法設定的情況下，才能使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="68869-142">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="68869-143">有效的值是從1到1000的整數。</span><span class="sxs-lookup"><span data-stu-id="68869-143">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="68869-144">較低的值代表較高的優先順序。</span><span class="sxs-lookup"><span data-stu-id="68869-144">Lower values represent higher priority.</span></span>

<span data-ttu-id="68869-145">如果您指定優先順序，您必須在設定檔中的所有端點上指定優先順序，而且任何兩個端點都不能共用相同的優先順序值。</span><span class="sxs-lookup"><span data-stu-id="68869-145">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="68869-146">如果您沒有指定優先順序，流量主管會將預設的優先順序值指派給端點，並從一個 (1) 開始，並依照設定檔列出端點的順序進行。</span><span class="sxs-lookup"><span data-stu-id="68869-146">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

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

### <span data-ttu-id="68869-147">-目標</span><span class="sxs-lookup"><span data-stu-id="68869-147">-Target</span></span>
<span data-ttu-id="68869-148">指定端點的完整 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="68869-148">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="68869-149">當流量主管將流量導向到此端點時，會在 DNS 回應中傳回這個值。</span><span class="sxs-lookup"><span data-stu-id="68869-149">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="68869-150">請僅針對 ExternalEndpoints 端點類型指定此參數。</span><span class="sxs-lookup"><span data-stu-id="68869-150">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="68869-151">針對其他端點類型，請改為指定 *TargetResourceId* 參數。</span><span class="sxs-lookup"><span data-stu-id="68869-151">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

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

### <span data-ttu-id="68869-152">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="68869-152">-TargetResourceId</span></span>
<span data-ttu-id="68869-153">指定目標的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="68869-153">Specifies resource ID of the target.</span></span>
<span data-ttu-id="68869-154">僅針對 AzureEndpoints 和 NestedEndpoints 端點類型指定此參數。</span><span class="sxs-lookup"><span data-stu-id="68869-154">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="68869-155">針對 ExternalEndpoints 端點類型，請改為指定 *目標* 參數。</span><span class="sxs-lookup"><span data-stu-id="68869-155">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

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

### <span data-ttu-id="68869-156">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="68869-156">-TrafficManagerProfile</span></span>
<span data-ttu-id="68869-157">指定本機 **TrafficManagerProfile** 物件。</span><span class="sxs-lookup"><span data-stu-id="68869-157">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="68869-158">這個 Cmdlet 會修改這個本機物件。</span><span class="sxs-lookup"><span data-stu-id="68869-158">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="68869-159">若要取得 **TrafficManagerProfile** 物件，請使用 Get-AzureRmTrafficManagerProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="68869-159">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="68869-160">-類型</span><span class="sxs-lookup"><span data-stu-id="68869-160">-Type</span></span>
<span data-ttu-id="68869-161">指定此 Cmdlet 新增至 Azure 流量管理器設定檔的端點類型。</span><span class="sxs-lookup"><span data-stu-id="68869-161">Specifies the type of endpoint that this cmdlet adds to the Azure Traffic Manager profile.</span></span>
<span data-ttu-id="68869-162">有效值為：</span><span class="sxs-lookup"><span data-stu-id="68869-162">Valid values are:</span></span> 

- <span data-ttu-id="68869-163">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="68869-163">AzureEndpoints</span></span>
- <span data-ttu-id="68869-164">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="68869-164">ExternalEndpoints</span></span>
- <span data-ttu-id="68869-165">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="68869-165">NestedEndpoints</span></span>

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

### <span data-ttu-id="68869-166">寬度</span><span class="sxs-lookup"><span data-stu-id="68869-166">-Weight</span></span>
<span data-ttu-id="68869-167">指定流量主管指派給端點的權重。</span><span class="sxs-lookup"><span data-stu-id="68869-167">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="68869-168">有效的值是從1到1000的整數。</span><span class="sxs-lookup"><span data-stu-id="68869-168">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="68869-169">預設值是一個 (1) 。</span><span class="sxs-lookup"><span data-stu-id="68869-169">The default value is one (1).</span></span>
<span data-ttu-id="68869-170">只有在流量管理器設定檔是使用加權流量路由方法設定的情況下，才能使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="68869-170">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

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

### <span data-ttu-id="68869-171">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68869-171">-DefaultProfile</span></span>
<span data-ttu-id="68869-172">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="68869-172">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68869-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68869-173">CommonParameters</span></span>
<span data-ttu-id="68869-174">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="68869-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68869-175">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="68869-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68869-176">輸入</span><span class="sxs-lookup"><span data-stu-id="68869-176">INPUTS</span></span>

### <span data-ttu-id="68869-177">TrafficManagerProfile （）</span><span class="sxs-lookup"><span data-stu-id="68869-177">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="68869-178">這個 Cmdlet 接受 **TrafficManagerProfile** 物件到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="68869-178">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="68869-179">輸出</span><span class="sxs-lookup"><span data-stu-id="68869-179">OUTPUTS</span></span>

### <span data-ttu-id="68869-180">TrafficManagerProfile （）</span><span class="sxs-lookup"><span data-stu-id="68869-180">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="68869-181">這個 Cmdlet 會傳回修改過的 **TrafficManagerProfile** 物件。</span><span class="sxs-lookup"><span data-stu-id="68869-181">This cmdlet returns a modified **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="68869-182">筆記</span><span class="sxs-lookup"><span data-stu-id="68869-182">NOTES</span></span>

## <span data-ttu-id="68869-183">相關連結</span><span class="sxs-lookup"><span data-stu-id="68869-183">RELATED LINKS</span></span>

[<span data-ttu-id="68869-184">AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="68869-184">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="68869-185">新-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="68869-185">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="68869-186">移除-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="68869-186">Remove-AzureRmTrafficManagerEndpointConfig</span></span>](./Remove-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="68869-187">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="68869-187">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


