---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/add-azurermtrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerEndpointConfig.md
ms.openlocfilehash: e9e6817d9a290acf1e91067edfd90cdf8081f1f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452003"
---
# <span data-ttu-id="ebe9a-101">Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="ebe9a-101">Add-AzureRmTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="ebe9a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ebe9a-102">SYNOPSIS</span></span>
<span data-ttu-id="ebe9a-103">將端點新增到本機流量管理器設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-103">Adds an endpoint to a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ebe9a-104">句法</span><span class="sxs-lookup"><span data-stu-id="ebe9a-104">SYNTAX</span></span>

```
Add-AzureRmTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ebe9a-105">說明</span><span class="sxs-lookup"><span data-stu-id="ebe9a-105">DESCRIPTION</span></span>
<span data-ttu-id="ebe9a-106">**AzureRmTrafficManagerEndpointConfig** Cmdlet 會將端點新增到本機 Azure 流量管理器設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-106">The **Add-AzureRmTrafficManagerEndpointConfig** cmdlet adds an endpoint to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="ebe9a-107">您可以使用 New-AzureRmTrafficManagerProfile 或 Get-AzureRmTrafficManagerProfile Cmdlet 來取得設定檔。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-107">You can get a profile by using the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="ebe9a-108">這個 Cmdlet 作用於本機設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="ebe9a-109">使用 Set-AzureRmTrafficManagerProfile Cmdlet，將您的變更提交至流量管理器的設定檔。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="ebe9a-110">若要建立端點並在單一作業中提交變更，請使用 New-AzureRmTrafficManagerEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-110">To create an endpoint and commit the change in a single operation, use the New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="ebe9a-111">示例</span><span class="sxs-lookup"><span data-stu-id="ebe9a-111">EXAMPLES</span></span>

### <span data-ttu-id="ebe9a-112">範例1：在設定檔中新增端點</span><span class="sxs-lookup"><span data-stu-id="ebe9a-112">Example 1: Add an endpoint to a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzureRmTrafficManagerEndpointConfig -EndpointName "contoso" -EndpointStatus Enabled -Target "www.contoso.com" -TrafficManagerProfile $TrafficManagerProfile -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Weight 10
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="ebe9a-113">第一個命令會使用 **AzureRmTrafficManagerProfile** Cmdlet 取得 Azure 流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="ebe9a-114">該命令會將本機設定檔儲存在 $TrafficManagerProfile 變數中。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="ebe9a-115">第二個命令會將名為 contoso 的端點新增至儲存在 $TrafficManagerProfile 中的設定檔。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-115">The second command adds an endpoint named contoso to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="ebe9a-116">此命令包含端點的配置資料。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-116">The command includes configuration data for the endpoint.</span></span>
<span data-ttu-id="ebe9a-117">這個命令只會變更本機物件。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-117">This command changes only the local object.</span></span>

<span data-ttu-id="ebe9a-118">Final 命令會更新 Azure 中的流量管理器設定檔，以符合 $TrafficManagerProfile 中的本機值。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-118">The final command updates the Traffic Manager profile in Azure to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="ebe9a-119">參數</span><span class="sxs-lookup"><span data-stu-id="ebe9a-119">PARAMETERS</span></span>

### <span data-ttu-id="ebe9a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebe9a-120">-DefaultProfile</span></span>
<span data-ttu-id="ebe9a-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebe9a-122">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="ebe9a-122">-EndpointLocation</span></span>
<span data-ttu-id="ebe9a-123">指定要在效能流量路由方法中使用的端點位置。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-123">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="ebe9a-124">這個參數只適用于 ExternalEndpoints 或 NestedEndpoints 類型的端點。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-124">This parameter is only applicable to endpoints of the ExternalEndpoints or the NestedEndpoints type.</span></span>
<span data-ttu-id="ebe9a-125">使用效能流量路由方法時，您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-125">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="ebe9a-126">指定 Azure 地區名稱。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-126">Specify an Azure region name.</span></span>
<span data-ttu-id="ebe9a-127">如需 Azure 區域的完整清單，請參閱 Azure 地區 https://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/) 。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-127">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebe9a-128">-終結點</span><span class="sxs-lookup"><span data-stu-id="ebe9a-128">-EndpointName</span></span>
<span data-ttu-id="ebe9a-129">指定此 Cmdlet 所新增之流量管理器端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-129">Specifies the name of the Traffic Manager endpoint that this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebe9a-130">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="ebe9a-130">-EndpointStatus</span></span>
<span data-ttu-id="ebe9a-131">指定端點的狀態。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-131">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="ebe9a-132">有效值為：</span><span class="sxs-lookup"><span data-stu-id="ebe9a-132">Valid values are:</span></span> 

- <span data-ttu-id="ebe9a-133">後</span><span class="sxs-lookup"><span data-stu-id="ebe9a-133">Enabled</span></span> 
- <span data-ttu-id="ebe9a-134">禁止</span><span class="sxs-lookup"><span data-stu-id="ebe9a-134">Disabled</span></span> 

<span data-ttu-id="ebe9a-135">如果狀態為 [已啟用]，則會針對端點健康情況探測端點，並包含在流量路由方法中。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-135">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebe9a-136">-GeoMapping</span><span class="sxs-lookup"><span data-stu-id="ebe9a-136">-GeoMapping</span></span>
<span data-ttu-id="ebe9a-137">使用 ' 地理 ' 流量路由方法時，對應到此端點的地區清單。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-137">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="ebe9a-138">如需可 [接受值的完整清單](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions)，請參閱流量管理器檔。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-138">Please consult Traffic Manager documentation for a [full list of accepted values](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions).</span></span>
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

### <span data-ttu-id="ebe9a-139">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="ebe9a-139">-MinChildEndpoints</span></span>
<span data-ttu-id="ebe9a-140">指定 Azure 地區名稱。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-140">Specify an Azure region name.</span></span>
<span data-ttu-id="ebe9a-141">如需 Azure 區域的完整清單，請參閱 Azure 地區 https://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/) 。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-141">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebe9a-142">-優先順序</span><span class="sxs-lookup"><span data-stu-id="ebe9a-142">-Priority</span></span>
<span data-ttu-id="ebe9a-143">指定流量管理器指派給端點的優先順序。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-143">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="ebe9a-144">只有在流量管理器設定檔是以優先順序流量路由方法設定的情況下，才能使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-144">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="ebe9a-145">有效的值是從1到1000的整數。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-145">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="ebe9a-146">較低的值代表較高的優先順序。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-146">Lower values represent higher priority.</span></span>

<span data-ttu-id="ebe9a-147">如果您指定優先順序，您必須在設定檔中的所有端點上指定優先順序，而且任何兩個端點都不能共用相同的優先順序值。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-147">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="ebe9a-148">如果您沒有指定優先順序，流量主管會將預設的優先順序值指派給端點，並從一個 (1) 開始，並依照設定檔列出端點的順序進行。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-148">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebe9a-149">-目標</span><span class="sxs-lookup"><span data-stu-id="ebe9a-149">-Target</span></span>
<span data-ttu-id="ebe9a-150">指定端點的完整 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-150">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="ebe9a-151">當流量主管將流量導向到此端點時，會在 DNS 回應中傳回這個值。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-151">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="ebe9a-152">請僅針對 ExternalEndpoints 端點類型指定此參數。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-152">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="ebe9a-153">針對其他端點類型，請改為指定 *TargetResourceId* 參數。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-153">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebe9a-154">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="ebe9a-154">-TargetResourceId</span></span>
<span data-ttu-id="ebe9a-155">指定目標的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-155">Specifies resource ID of the target.</span></span>
<span data-ttu-id="ebe9a-156">僅針對 AzureEndpoints 和 NestedEndpoints 端點類型指定此參數。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-156">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="ebe9a-157">針對 ExternalEndpoints 端點類型，請改為指定 *目標* 參數。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-157">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebe9a-158">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ebe9a-158">-TrafficManagerProfile</span></span>
<span data-ttu-id="ebe9a-159">指定本機 **TrafficManagerProfile** 物件。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-159">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="ebe9a-160">這個 Cmdlet 會修改這個本機物件。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-160">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="ebe9a-161">若要取得 **TrafficManagerProfile** 物件，請使用 Get-AzureRmTrafficManagerProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-161">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: TrafficManagerProfile
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebe9a-162">-類型</span><span class="sxs-lookup"><span data-stu-id="ebe9a-162">-Type</span></span>
<span data-ttu-id="ebe9a-163">指定此 Cmdlet 新增至 Azure 流量管理器設定檔的端點類型。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-163">Specifies the type of endpoint that this cmdlet adds to the Azure Traffic Manager profile.</span></span>
<span data-ttu-id="ebe9a-164">有效值為：</span><span class="sxs-lookup"><span data-stu-id="ebe9a-164">Valid values are:</span></span> 

- <span data-ttu-id="ebe9a-165">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="ebe9a-165">AzureEndpoints</span></span>
- <span data-ttu-id="ebe9a-166">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="ebe9a-166">ExternalEndpoints</span></span>
- <span data-ttu-id="ebe9a-167">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="ebe9a-167">NestedEndpoints</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebe9a-168">寬度</span><span class="sxs-lookup"><span data-stu-id="ebe9a-168">-Weight</span></span>
<span data-ttu-id="ebe9a-169">指定流量主管指派給端點的權重。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-169">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="ebe9a-170">有效的值是從1到1000的整數。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-170">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="ebe9a-171">預設值是一個 (1) 。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-171">The default value is one (1).</span></span>
<span data-ttu-id="ebe9a-172">只有在流量管理器設定檔是使用加權流量路由方法設定的情況下，才能使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-172">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebe9a-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebe9a-173">CommonParameters</span></span>
<span data-ttu-id="ebe9a-174">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebe9a-175">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebe9a-176">輸入</span><span class="sxs-lookup"><span data-stu-id="ebe9a-176">INPUTS</span></span>

### <span data-ttu-id="ebe9a-177">TrafficManagerProfile （）</span><span class="sxs-lookup"><span data-stu-id="ebe9a-177">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="ebe9a-178">這個 Cmdlet 接受 **TrafficManagerProfile** 物件到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-178">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="ebe9a-179">輸出</span><span class="sxs-lookup"><span data-stu-id="ebe9a-179">OUTPUTS</span></span>

### <span data-ttu-id="ebe9a-180">TrafficManagerProfile （）</span><span class="sxs-lookup"><span data-stu-id="ebe9a-180">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="ebe9a-181">這個 Cmdlet 會傳回修改過的 **TrafficManagerProfile** 物件。</span><span class="sxs-lookup"><span data-stu-id="ebe9a-181">This cmdlet returns a modified **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="ebe9a-182">筆記</span><span class="sxs-lookup"><span data-stu-id="ebe9a-182">NOTES</span></span>

## <span data-ttu-id="ebe9a-183">相關連結</span><span class="sxs-lookup"><span data-stu-id="ebe9a-183">RELATED LINKS</span></span>

[<span data-ttu-id="ebe9a-184">AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ebe9a-184">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="ebe9a-185">新-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ebe9a-185">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="ebe9a-186">移除-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="ebe9a-186">Remove-AzureRmTrafficManagerEndpointConfig</span></span>](./Remove-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="ebe9a-187">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ebe9a-187">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


