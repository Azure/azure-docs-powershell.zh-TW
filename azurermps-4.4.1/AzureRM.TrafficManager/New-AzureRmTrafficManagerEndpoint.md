---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: A7A908A1-7326-4725-A3F9-4D05E40C5F73
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 7eaadd8c80fff6491983a3e1d9c750227eba43cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444891"
---
# <span data-ttu-id="2cc53-101">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2cc53-101">New-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="2cc53-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2cc53-102">SYNOPSIS</span></span>
<span data-ttu-id="2cc53-103">在流量管理器設定檔中建立端點。</span><span class="sxs-lookup"><span data-stu-id="2cc53-103">Creates an endpoint in a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2cc53-104">句法</span><span class="sxs-lookup"><span data-stu-id="2cc53-104">SYNTAX</span></span>

```
New-AzureRmTrafficManagerEndpoint -Name <String> -ProfileName <String> -ResourceGroupName <String>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2cc53-105">說明</span><span class="sxs-lookup"><span data-stu-id="2cc53-105">DESCRIPTION</span></span>
<span data-ttu-id="2cc53-106">**新的 AzureRmTrafficManagerEndpoint** Cmdlet 會在 Azure 流量管理器設定檔中建立端點。</span><span class="sxs-lookup"><span data-stu-id="2cc53-106">The **New-AzureRmTrafficManagerEndpoint** cmdlet creates an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="2cc53-107">這個 Cmdlet 會將每個新端點提交至流量管理器服務。</span><span class="sxs-lookup"><span data-stu-id="2cc53-107">This cmdlet commits each new endpoint to the Traffic Manager service.</span></span>
<span data-ttu-id="2cc53-108">若要在本機流量管理器設定檔物件中新增多個端點，並在單一作業中提交變更，請使用 Add-AzureRmTrafficManagerEndpointConfig Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2cc53-108">To add multiple endpoints to a local Traffic Manager profile object and commit changes in a single operation, use the Add-AzureRmTrafficManagerEndpointConfig cmdlet.</span></span>

## <span data-ttu-id="2cc53-109">示例</span><span class="sxs-lookup"><span data-stu-id="2cc53-109">EXAMPLES</span></span>

### <span data-ttu-id="2cc53-110">範例1：建立設定檔的外部端點</span><span class="sxs-lookup"><span data-stu-id="2cc53-110">Example 1: Create an external endpoint for a profile</span></span>
```
PS C:\>New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Target "www.contoso.com" -Weight 10
```

<span data-ttu-id="2cc53-111">這個命令會在名為 ResourceGroup11 的資源群組中，在名為 ContosoProfile 的設定檔中建立名為 contoso 的外部端點。</span><span class="sxs-lookup"><span data-stu-id="2cc53-111">This command creates an external endpoint named contoso in the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="2cc53-112">範例2：建立設定檔的 Azure 端點</span><span class="sxs-lookup"><span data-stu-id="2cc53-112">Example 2: Create an Azure endpoint for a profile</span></span>
```
PS C:\>New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
```

<span data-ttu-id="2cc53-113">這個命令會在資源群組 ResouceGroup11 中，在名為 ContosoProfile 的設定檔中建立名為 contoso 的 Azure 端點。</span><span class="sxs-lookup"><span data-stu-id="2cc53-113">This command creates an Azure endpoint named contoso in the profile named ContosoProfile in resource group ResouceGroup11.</span></span>
<span data-ttu-id="2cc53-114">Azure 端點指向 azure Web 應用程式，其 Azure 資源管理器 ID 是由 *TargetResourceId* 中的 URI 路徑所提供。</span><span class="sxs-lookup"><span data-stu-id="2cc53-114">The Azure endpoint points to the Azure Web App whose Azure Resource Manager ID is given by the URI path in *TargetResourceId*.</span></span>
<span data-ttu-id="2cc53-115">因為 Web App 資源提供位置，所以命令不會指定 *EndpointLocation* 參數。</span><span class="sxs-lookup"><span data-stu-id="2cc53-115">The command does not specify the *EndpointLocation* parameter because the Web App resource supplies the location.</span></span>

## <span data-ttu-id="2cc53-116">參數</span><span class="sxs-lookup"><span data-stu-id="2cc53-116">PARAMETERS</span></span>

### <span data-ttu-id="2cc53-117">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="2cc53-117">-EndpointLocation</span></span>
<span data-ttu-id="2cc53-118">指定要在效能流量路由方法中使用的端點位置。</span><span class="sxs-lookup"><span data-stu-id="2cc53-118">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="2cc53-119">這個參數只適用于 ExternalEndpoints 或 NestedEndpoints 類型的端點。</span><span class="sxs-lookup"><span data-stu-id="2cc53-119">This parameter is only applicable to endpoints of the ExternalEndpoints or NestedEndpoints type.</span></span>
<span data-ttu-id="2cc53-120">使用效能流量路由方法時，您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="2cc53-120">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="2cc53-121">指定 Azure 地區名稱。</span><span class="sxs-lookup"><span data-stu-id="2cc53-121">Specify an Azure region name.</span></span>
<span data-ttu-id="2cc53-122">如需 Azure 區域的完整清單，請參閱 Azure 地區 https://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/) 。</span><span class="sxs-lookup"><span data-stu-id="2cc53-122">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="2cc53-123">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="2cc53-123">-EndpointStatus</span></span>
<span data-ttu-id="2cc53-124">指定端點的狀態。</span><span class="sxs-lookup"><span data-stu-id="2cc53-124">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="2cc53-125">有效值為：</span><span class="sxs-lookup"><span data-stu-id="2cc53-125">Valid values are:</span></span> 

- <span data-ttu-id="2cc53-126">後</span><span class="sxs-lookup"><span data-stu-id="2cc53-126">Enabled</span></span> 
- <span data-ttu-id="2cc53-127">禁止</span><span class="sxs-lookup"><span data-stu-id="2cc53-127">Disabled</span></span> 

<span data-ttu-id="2cc53-128">如果狀態為 [已啟用]，則會針對端點健康情況探測端點，並包含在流量路由方法中。</span><span class="sxs-lookup"><span data-stu-id="2cc53-128">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

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

### <span data-ttu-id="2cc53-129">-GeoMapping</span><span class="sxs-lookup"><span data-stu-id="2cc53-129">-GeoMapping</span></span>
<span data-ttu-id="2cc53-130">使用 ' 地理 ' 流量路由方法時，對應到此端點的地區清單。</span><span class="sxs-lookup"><span data-stu-id="2cc53-130">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="2cc53-131">如需可接受值的完整清單，請參閱流量管理器檔。</span><span class="sxs-lookup"><span data-stu-id="2cc53-131">Please consult Traffic Manager documentation for a full list of accepted values.</span></span>
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

### <span data-ttu-id="2cc53-132">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="2cc53-132">-MinChildEndpoints</span></span>
<span data-ttu-id="2cc53-133">指定 Azure 地區名稱。</span><span class="sxs-lookup"><span data-stu-id="2cc53-133">Specify an Azure region name.</span></span>
<span data-ttu-id="2cc53-134">如需 Azure 區域的完整清單，請參閱 Azure 地區 https://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/) 。</span><span class="sxs-lookup"><span data-stu-id="2cc53-134">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="2cc53-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="2cc53-135">-Name</span></span>
<span data-ttu-id="2cc53-136">指定此 Cmdlet 建立之流量管理器端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="2cc53-136">Specifies the name of the Traffic Manager endpoint that this cmdlet creates.</span></span>

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

### <span data-ttu-id="2cc53-137">-優先順序</span><span class="sxs-lookup"><span data-stu-id="2cc53-137">-Priority</span></span>
<span data-ttu-id="2cc53-138">指定流量管理器指派給端點的優先順序。</span><span class="sxs-lookup"><span data-stu-id="2cc53-138">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="2cc53-139">只有在流量管理器設定檔是以優先順序流量路由方法設定的情況下，才能使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="2cc53-139">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="2cc53-140">有效的值是從1到1000的整數。</span><span class="sxs-lookup"><span data-stu-id="2cc53-140">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="2cc53-141">較低的值代表較高的優先順序。</span><span class="sxs-lookup"><span data-stu-id="2cc53-141">Lower values represent higher priority.</span></span>

<span data-ttu-id="2cc53-142">如果您指定優先順序，您必須在設定檔中的所有端點上指定優先順序，而且任何兩個端點都不能共用相同的優先順序值。</span><span class="sxs-lookup"><span data-stu-id="2cc53-142">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="2cc53-143">如果您沒有指定優先順序，流量主管會將預設的優先順序值指派給端點，並從一個 (1) 開始，並依照設定檔列出端點的順序進行。</span><span class="sxs-lookup"><span data-stu-id="2cc53-143">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

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

### <span data-ttu-id="2cc53-144">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="2cc53-144">-ProfileName</span></span>
<span data-ttu-id="2cc53-145">指定此 Cmdlet 新增端點的流量管理器設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="2cc53-145">Specifies the name of a Traffic Manager profile to which this cmdlet adds an endpoint.</span></span>
<span data-ttu-id="2cc53-146">若要取得設定檔，請使用 New-AzureRmTrafficManagerProfile 或 Get-AzureRmTrafficManagerProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2cc53-146">To obtain a profile, use the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

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

### <span data-ttu-id="2cc53-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cc53-147">-ResourceGroupName</span></span>
<span data-ttu-id="2cc53-148">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2cc53-148">Specifies the name of a resource group.</span></span>
<span data-ttu-id="2cc53-149">這個 Cmdlet 會在此參數指定的群組中建立流量管理器端點。</span><span class="sxs-lookup"><span data-stu-id="2cc53-149">This cmdlet creates a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="2cc53-150">-目標</span><span class="sxs-lookup"><span data-stu-id="2cc53-150">-Target</span></span>
<span data-ttu-id="2cc53-151">指定端點的完整 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="2cc53-151">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="2cc53-152">當流量主管將流量導向到此端點時，會在 DNS 回應中傳回這個值。</span><span class="sxs-lookup"><span data-stu-id="2cc53-152">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="2cc53-153">請僅針對 ExternalEndpoints 端點類型指定此參數。</span><span class="sxs-lookup"><span data-stu-id="2cc53-153">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="2cc53-154">針對其他端點類型，請改為指定 *TargetResourceId* 參數。</span><span class="sxs-lookup"><span data-stu-id="2cc53-154">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

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

### <span data-ttu-id="2cc53-155">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="2cc53-155">-TargetResourceId</span></span>
<span data-ttu-id="2cc53-156">指定目標的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="2cc53-156">Specifies resource ID of the target.</span></span>
<span data-ttu-id="2cc53-157">僅針對 AzureEndpoints 和 NestedEndpoints 端點類型指定此參數。</span><span class="sxs-lookup"><span data-stu-id="2cc53-157">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="2cc53-158">針對 ExternalEndpoints 端點類型，請改為指定 *目標* 參數。</span><span class="sxs-lookup"><span data-stu-id="2cc53-158">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

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

### <span data-ttu-id="2cc53-159">-類型</span><span class="sxs-lookup"><span data-stu-id="2cc53-159">-Type</span></span>
<span data-ttu-id="2cc53-160">指定此 Cmdlet 新增至流量管理器設定檔的端點類型。</span><span class="sxs-lookup"><span data-stu-id="2cc53-160">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="2cc53-161">有效值為：</span><span class="sxs-lookup"><span data-stu-id="2cc53-161">Valid values are:</span></span> 

- <span data-ttu-id="2cc53-162">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="2cc53-162">AzureEndpoints</span></span>
- <span data-ttu-id="2cc53-163">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="2cc53-163">ExternalEndpoints</span></span>
- <span data-ttu-id="2cc53-164">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="2cc53-164">NestedEndpoints</span></span>

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

### <span data-ttu-id="2cc53-165">寬度</span><span class="sxs-lookup"><span data-stu-id="2cc53-165">-Weight</span></span>
<span data-ttu-id="2cc53-166">指定流量主管指派給端點的權重。</span><span class="sxs-lookup"><span data-stu-id="2cc53-166">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="2cc53-167">有效的值是從1到1000的整數。</span><span class="sxs-lookup"><span data-stu-id="2cc53-167">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="2cc53-168">預設值是一個 (1) 。</span><span class="sxs-lookup"><span data-stu-id="2cc53-168">The default value is one (1).</span></span>
<span data-ttu-id="2cc53-169">只有在流量管理器設定檔是使用加權流量路由方法設定的情況下，才能使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="2cc53-169">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

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

### <span data-ttu-id="2cc53-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cc53-170">-DefaultProfile</span></span>
<span data-ttu-id="2cc53-171">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2cc53-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2cc53-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cc53-172">CommonParameters</span></span>
<span data-ttu-id="2cc53-173">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2cc53-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cc53-174">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2cc53-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cc53-175">輸入</span><span class="sxs-lookup"><span data-stu-id="2cc53-175">INPUTS</span></span>

## <span data-ttu-id="2cc53-176">輸出</span><span class="sxs-lookup"><span data-stu-id="2cc53-176">OUTPUTS</span></span>

### <span data-ttu-id="2cc53-177">TrafficManagerEndpoint 中的 TrafficManager。</span><span class="sxs-lookup"><span data-stu-id="2cc53-177">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="2cc53-178">筆記</span><span class="sxs-lookup"><span data-stu-id="2cc53-178">NOTES</span></span>

## <span data-ttu-id="2cc53-179">相關連結</span><span class="sxs-lookup"><span data-stu-id="2cc53-179">RELATED LINKS</span></span>

[<span data-ttu-id="2cc53-180">Disable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2cc53-180">Disable-AzureRmTrafficManagerEndpoint</span></span>](./Disable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="2cc53-181">Enable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2cc53-181">Enable-AzureRmTrafficManagerEndpoint</span></span>](./Enable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="2cc53-182">AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2cc53-182">Get-AzureRmTrafficManagerEndpoint</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="2cc53-183">AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2cc53-183">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="2cc53-184">新-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2cc53-184">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="2cc53-185">移除-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2cc53-185">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="2cc53-186">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2cc53-186">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


