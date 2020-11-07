---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: DE31891A-0EF7-44D7-B955-A3279D27CC21
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/new-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: bc59e5b317588317ae9dc428db76c924847895da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625542"
---
# <span data-ttu-id="cb08c-101">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cb08c-101">New-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="cb08c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cb08c-102">SYNOPSIS</span></span>
<span data-ttu-id="cb08c-103">建立流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="cb08c-103">Creates a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb08c-104">句法</span><span class="sxs-lookup"><span data-stu-id="cb08c-104">SYNTAX</span></span>

```
New-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-ProfileStatus <String>]
 -RelativeDnsName <String> -Ttl <UInt32> -TrafficRoutingMethod <String> -MonitorProtocol <String>
 -MonitorPort <UInt32> [-MonitorPath <String>] [-MonitorIntervalInSeconds <Int32>]
 [-MonitorTimeoutInSeconds <Int32>] [-MonitorToleratedNumberOfFailures <Int32>] [-MaxReturn <Int64>]
 [-Tag <Hashtable>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-ExpectedStatusCodeRange <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerExpectedStatusCodeRange]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb08c-105">說明</span><span class="sxs-lookup"><span data-stu-id="cb08c-105">DESCRIPTION</span></span>
<span data-ttu-id="cb08c-106">**新的-AzureRmTrafficManagerProfile** Cmdlet 會建立 Azure 流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="cb08c-106">The **New-AzureRmTrafficManagerProfile** cmdlet creates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="cb08c-107">指定 *Name* 參數及必要的設定。</span><span class="sxs-lookup"><span data-stu-id="cb08c-107">Specify the *Name* parameter and required settings.</span></span>
<span data-ttu-id="cb08c-108">這個 Cmdlet 會傳回代表新設定檔的本機物件。</span><span class="sxs-lookup"><span data-stu-id="cb08c-108">This cmdlet returns a local object that represents the new profile.</span></span>

<span data-ttu-id="cb08c-109">這個 Cmdlet 不會設定流量管理器端點。</span><span class="sxs-lookup"><span data-stu-id="cb08c-109">This cmdlet does not configure Traffic Manager endpoints.</span></span>
<span data-ttu-id="cb08c-110">您可以使用 Add-AzureRmTrafficManagerEndpointConfig Cmdlet 來更新本機設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="cb08c-110">You can update the local profile object by using the Add-AzureRmTrafficManagerEndpointConfig cmdlet.</span></span>
<span data-ttu-id="cb08c-111">然後使用 Set-AzureRmTrafficManagerProfile Cmdlet 將變更上傳到流量管理器。</span><span class="sxs-lookup"><span data-stu-id="cb08c-111">Then upload changes to Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="cb08c-112">或者，您也可以使用 New-AzureRmTrafficManagerEndpoint Cmdlet 來新增端點。</span><span class="sxs-lookup"><span data-stu-id="cb08c-112">Alternatively, you can add endpoints by using the New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="cb08c-113">示例</span><span class="sxs-lookup"><span data-stu-id="cb08c-113">EXAMPLES</span></span>

### <span data-ttu-id="cb08c-114">範例1：建立設定檔</span><span class="sxs-lookup"><span data-stu-id="cb08c-114">Example 1: Create a profile</span></span>
```
PS C:\>New-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" -ProfileStatus Enabled -TrafficRoutingMethod Performance -RelativeDnsName "contosoapp" -TTL 30 -MonitorProtocol HTTP -MonitorPort 80 -MonitorPath "/default.aspx"
```

<span data-ttu-id="cb08c-115">這個命令會在資源群組 ResourceGroup11 中建立名為 ContosoProfile 的 Azure 流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="cb08c-115">This command creates an Azure Traffic Manager profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="cb08c-116">DNS FQDN 是 contosoapp.trafficmanager.net。</span><span class="sxs-lookup"><span data-stu-id="cb08c-116">The DNS FQDN is contosoapp.trafficmanager.net.</span></span>

## <span data-ttu-id="cb08c-117">參數</span><span class="sxs-lookup"><span data-stu-id="cb08c-117">PARAMETERS</span></span>

### <span data-ttu-id="cb08c-118">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="cb08c-118">-CustomHeader</span></span>
<span data-ttu-id="cb08c-119">針對探測要求的自訂標頭名稱和值對清單。</span><span class="sxs-lookup"><span data-stu-id="cb08c-119">List of custom header name and value pairs for probe requests.</span></span>

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

### <span data-ttu-id="cb08c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb08c-120">-DefaultProfile</span></span>
<span data-ttu-id="cb08c-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cb08c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb08c-122">-ExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="cb08c-122">-ExpectedStatusCodeRange</span></span>
<span data-ttu-id="cb08c-123">探測要求的預期 HTTP 狀態碼範圍清單。</span><span class="sxs-lookup"><span data-stu-id="cb08c-123">List of expected HTTP status code ranges for probe requests.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerExpectedStatusCodeRange]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb08c-124">-MaxReturn</span><span class="sxs-lookup"><span data-stu-id="cb08c-124">-MaxReturn</span></span>
<span data-ttu-id="cb08c-125">針對具有多值路由方法之設定檔所傳回的最大答卷數。</span><span class="sxs-lookup"><span data-stu-id="cb08c-125">The maximum number of answers returned for profiles with a MultiValue routing method.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb08c-126">-MonitorIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="cb08c-126">-MonitorIntervalInSeconds</span></span>
<span data-ttu-id="cb08c-127">間隔 (以秒為單位) 流量管理員將在此設定檔中檢查每個端點的健康情況。</span><span class="sxs-lookup"><span data-stu-id="cb08c-127">The interval (in seconds) at which Traffic Manager will check the health of each endpoint in this profile.</span></span> <span data-ttu-id="cb08c-128">預設值為30。</span><span class="sxs-lookup"><span data-stu-id="cb08c-128">The default is 30.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: IntervalInSecondsForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb08c-129">-MonitorPath</span><span class="sxs-lookup"><span data-stu-id="cb08c-129">-MonitorPath</span></span>
<span data-ttu-id="cb08c-130">指定用來監視端點健康情況的路徑。</span><span class="sxs-lookup"><span data-stu-id="cb08c-130">Specifies the path that is used to monitor endpoint health.</span></span>
<span data-ttu-id="cb08c-131">指定相對於端點網功能變數名稱稱的值。</span><span class="sxs-lookup"><span data-stu-id="cb08c-131">Specify a value relative to the endpoint domain name.</span></span>
<span data-ttu-id="cb08c-132">此值必須以斜線 (/) 開頭。</span><span class="sxs-lookup"><span data-stu-id="cb08c-132">This value must begin with a slash (/).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PathForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb08c-133">-MonitorPort</span><span class="sxs-lookup"><span data-stu-id="cb08c-133">-MonitorPort</span></span>
<span data-ttu-id="cb08c-134">指定用來監視端點健康情況的 TCP 埠。</span><span class="sxs-lookup"><span data-stu-id="cb08c-134">Specifies the TCP port that is used to monitor endpoint health.</span></span>
<span data-ttu-id="cb08c-135">有效的值是從1到65535的整數。</span><span class="sxs-lookup"><span data-stu-id="cb08c-135">Valid values are integers from 1 through 65535.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases: PortForMonitor

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb08c-136">-MonitorProtocol</span><span class="sxs-lookup"><span data-stu-id="cb08c-136">-MonitorProtocol</span></span>
<span data-ttu-id="cb08c-137">指定用來監視端點健康情況的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="cb08c-137">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="cb08c-138">有效值為：</span><span class="sxs-lookup"><span data-stu-id="cb08c-138">Valid values are:</span></span>

- <span data-ttu-id="cb08c-139">HTTP</span><span class="sxs-lookup"><span data-stu-id="cb08c-139">HTTP</span></span>
- <span data-ttu-id="cb08c-140">IP-HTTPS</span><span class="sxs-lookup"><span data-stu-id="cb08c-140">HTTPS</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProtocolForMonitor
Accepted values: HTTP, HTTPS, TCP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb08c-141">-MonitorTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="cb08c-141">-MonitorTimeoutInSeconds</span></span>
<span data-ttu-id="cb08c-142">流量管理器允許此設定檔中的端點回應健康情況檢查的時間 (以秒為單位）) 。</span><span class="sxs-lookup"><span data-stu-id="cb08c-142">The time (in seconds) that Traffic Manager allows endpoints in this profile to respond to the health check.</span></span> <span data-ttu-id="cb08c-143">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="cb08c-143">The default is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: TimeoutInSecondsForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb08c-144">-MonitorToleratedNumberOfFailures</span><span class="sxs-lookup"><span data-stu-id="cb08c-144">-MonitorToleratedNumberOfFailures</span></span>
<span data-ttu-id="cb08c-145">在此設定檔中宣告端點前，在下一個連續失敗狀況檢查已降級之後，通信量 Manager tolerates 的連續失敗狀況檢查次數。</span><span class="sxs-lookup"><span data-stu-id="cb08c-145">The number of consecutive failed health checks that Traffic Manager tolerates before declaring an endpoint in this profile Degraded after the next consecutive failed health check.</span></span> <span data-ttu-id="cb08c-146">預設值為3。</span><span class="sxs-lookup"><span data-stu-id="cb08c-146">The default is 3.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ToleratedNumberOfFailuresForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb08c-147">-名稱</span><span class="sxs-lookup"><span data-stu-id="cb08c-147">-Name</span></span>
<span data-ttu-id="cb08c-148">指定此 Cmdlet 所建立之流量管理器設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb08c-148">Specifies a name for the Traffic Manager profile that this cmdlet creates.</span></span>

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

### <span data-ttu-id="cb08c-149">-ProfileStatus</span><span class="sxs-lookup"><span data-stu-id="cb08c-149">-ProfileStatus</span></span>
<span data-ttu-id="cb08c-150">指定設定檔的狀態。</span><span class="sxs-lookup"><span data-stu-id="cb08c-150">Specifies the status of the profile.</span></span>
<span data-ttu-id="cb08c-151">有效值為： Enabled 和 Disabled。</span><span class="sxs-lookup"><span data-stu-id="cb08c-151">Valid values are: Enabled and Disabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb08c-152">-RelativeDnsName</span><span class="sxs-lookup"><span data-stu-id="cb08c-152">-RelativeDnsName</span></span>
<span data-ttu-id="cb08c-153">指定此流量管理器設定檔所提供的相對 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="cb08c-153">Specifies the relative DNS name that this Traffic Manager profile provides.</span></span>
<span data-ttu-id="cb08c-154">流量管理器結合此值與 DNS 功能變數名稱，而 Azure 流量 Manager 會使用該名稱來構成設定檔的完整功能變數名稱 (FQDN) 。</span><span class="sxs-lookup"><span data-stu-id="cb08c-154">Traffic Manager combines this value and the DNS domain name that Azure Traffic Manager uses to form the fully qualified domain name (FQDN) of the profile.</span></span>

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

### <span data-ttu-id="cb08c-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb08c-155">-ResourceGroupName</span></span>
<span data-ttu-id="cb08c-156">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb08c-156">Specifies the name of a resource group.</span></span>
<span data-ttu-id="cb08c-157">這個 Cmdlet 會在此參數指定的群組中建立流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="cb08c-157">This cmdlet creates a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="cb08c-158">-Tag</span><span class="sxs-lookup"><span data-stu-id="cb08c-158">-Tag</span></span>
<span data-ttu-id="cb08c-159">在伺服器上將雜湊表的格式設定為標記的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="cb08c-159">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="cb08c-160">例如：</span><span class="sxs-lookup"><span data-stu-id="cb08c-160">For example:</span></span>

<span data-ttu-id="cb08c-161">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="cb08c-161">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb08c-162">-TrafficRoutingMethod</span><span class="sxs-lookup"><span data-stu-id="cb08c-162">-TrafficRoutingMethod</span></span>
<span data-ttu-id="cb08c-163">指定流量路由方法。</span><span class="sxs-lookup"><span data-stu-id="cb08c-163">Specifies the traffic routing method.</span></span>
<span data-ttu-id="cb08c-164">這個方法會判斷哪個端點流量主管會傳回，以回應傳入的 DNS 查詢。</span><span class="sxs-lookup"><span data-stu-id="cb08c-164">This method determines which endpoint Traffic Manager returns in response to incoming DNS queries.</span></span>
<span data-ttu-id="cb08c-165">有效值為：</span><span class="sxs-lookup"><span data-stu-id="cb08c-165">Valid values are:</span></span>

- <span data-ttu-id="cb08c-166">提高</span><span class="sxs-lookup"><span data-stu-id="cb08c-166">Performance</span></span>
- <span data-ttu-id="cb08c-167">加</span><span class="sxs-lookup"><span data-stu-id="cb08c-167">Weighted</span></span>
- <span data-ttu-id="cb08c-168">優先順序</span><span class="sxs-lookup"><span data-stu-id="cb08c-168">Priority</span></span>
- <span data-ttu-id="cb08c-169">位置</span><span class="sxs-lookup"><span data-stu-id="cb08c-169">Geographic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Performance, Weighted, Priority, Geographic

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb08c-170">-Ttl</span><span class="sxs-lookup"><span data-stu-id="cb08c-170">-Ttl</span></span>
<span data-ttu-id="cb08c-171">指定 (TTL) 值的 DNS 時間。</span><span class="sxs-lookup"><span data-stu-id="cb08c-171">Specifies the DNS Time to Live (TTL) value.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb08c-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb08c-172">CommonParameters</span></span>
<span data-ttu-id="cb08c-173">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cb08c-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb08c-174">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cb08c-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb08c-175">輸入</span><span class="sxs-lookup"><span data-stu-id="cb08c-175">INPUTS</span></span>

### <span data-ttu-id="cb08c-176">所有</span><span class="sxs-lookup"><span data-stu-id="cb08c-176">None</span></span>
<span data-ttu-id="cb08c-177">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="cb08c-177">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cb08c-178">輸出</span><span class="sxs-lookup"><span data-stu-id="cb08c-178">OUTPUTS</span></span>

### <span data-ttu-id="cb08c-179">TrafficManagerProfile （）</span><span class="sxs-lookup"><span data-stu-id="cb08c-179">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="cb08c-180">這個 Cmdlet 會傳回新的 TrafficManagerProfile 物件。</span><span class="sxs-lookup"><span data-stu-id="cb08c-180">This cmdlet returns a new TrafficManagerProfile object.</span></span>

## <span data-ttu-id="cb08c-181">筆記</span><span class="sxs-lookup"><span data-stu-id="cb08c-181">NOTES</span></span>

## <span data-ttu-id="cb08c-182">相關連結</span><span class="sxs-lookup"><span data-stu-id="cb08c-182">RELATED LINKS</span></span>

[<span data-ttu-id="cb08c-183">附加 AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="cb08c-183">Add-AzureRmTrafficManagerEndpointConfig</span></span>](./Add-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="cb08c-184">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cb08c-184">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="cb08c-185">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cb08c-185">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="cb08c-186">AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cb08c-186">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="cb08c-187">移除-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cb08c-187">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="cb08c-188">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cb08c-188">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


