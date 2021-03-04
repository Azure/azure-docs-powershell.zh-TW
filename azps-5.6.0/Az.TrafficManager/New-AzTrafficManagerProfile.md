---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: DE31891A-0EF7-44D7-B955-A3279D27CC21
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/new-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerProfile.md
ms.openlocfilehash: a17f88a23399fda7f4775ca52fbe1d4aec35594d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901626"
---
# <span data-ttu-id="f36d3-101">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f36d3-101">New-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="f36d3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f36d3-102">SYNOPSIS</span></span>
<span data-ttu-id="f36d3-103">建立流量管理員設定檔。</span><span class="sxs-lookup"><span data-stu-id="f36d3-103">Creates a Traffic Manager profile.</span></span>

## <span data-ttu-id="f36d3-104">語法</span><span class="sxs-lookup"><span data-stu-id="f36d3-104">SYNTAX</span></span>

```
New-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-ProfileStatus <String>]
 -RelativeDnsName <String> -Ttl <UInt32> -TrafficRoutingMethod <String> -MonitorProtocol <String>
 -MonitorPort <UInt32> [-MonitorPath <String>] [-MonitorIntervalInSeconds <Int32>]
 [-MonitorTimeoutInSeconds <Int32>] [-MonitorToleratedNumberOfFailures <Int32>] [-MaxReturn <Int64>]
 [-Tag <Hashtable>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-ExpectedStatusCodeRange <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerExpectedStatusCodeRange]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f36d3-105">描述</span><span class="sxs-lookup"><span data-stu-id="f36d3-105">DESCRIPTION</span></span>
<span data-ttu-id="f36d3-106">**New-AzTrafficManagerProfile** Cmdlet 會建立 Azure 流量管理員設定檔。</span><span class="sxs-lookup"><span data-stu-id="f36d3-106">The **New-AzTrafficManagerProfile** cmdlet creates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="f36d3-107">指定 *名稱* 參數和必要的設定。</span><span class="sxs-lookup"><span data-stu-id="f36d3-107">Specify the *Name* parameter and required settings.</span></span>
<span data-ttu-id="f36d3-108">此 Cmdlet 會返回代表新設定檔的一個本機物件。</span><span class="sxs-lookup"><span data-stu-id="f36d3-108">This cmdlet returns a local object that represents the new profile.</span></span>

<span data-ttu-id="f36d3-109">此 Cmdlet 不會設定流量管理員端點。</span><span class="sxs-lookup"><span data-stu-id="f36d3-109">This cmdlet does not configure Traffic Manager endpoints.</span></span>
<span data-ttu-id="f36d3-110">您可以使用 Cmdlet 更新Add-AzTrafficManagerEndpointConfig物件。</span><span class="sxs-lookup"><span data-stu-id="f36d3-110">You can update the local profile object by using the Add-AzTrafficManagerEndpointConfig cmdlet.</span></span>
<span data-ttu-id="f36d3-111">然後使用 Cmdlet 將變更上傳到流量Set-AzTrafficManagerProfile管理員。</span><span class="sxs-lookup"><span data-stu-id="f36d3-111">Then upload changes to Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="f36d3-112">或者，您也可以使用 Cmdlet New-AzTrafficManagerEndpoint端點。</span><span class="sxs-lookup"><span data-stu-id="f36d3-112">Alternatively, you can add endpoints by using the New-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="f36d3-113">例子</span><span class="sxs-lookup"><span data-stu-id="f36d3-113">EXAMPLES</span></span>

### <span data-ttu-id="f36d3-114">範例 1：建立設定檔</span><span class="sxs-lookup"><span data-stu-id="f36d3-114">Example 1: Create a profile</span></span>
```
PS C:\>New-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" -ProfileStatus Enabled -TrafficRoutingMethod Performance -RelativeDnsName "contosoapp" -TTL 30 -MonitorProtocol HTTP -MonitorPort 80 -MonitorPath "/default.aspx"
```

<span data-ttu-id="f36d3-115">此命令在資源群組 ResourceGroup11 中建立名為 ContosoProfile 的 Azure 流量管理員設定檔。</span><span class="sxs-lookup"><span data-stu-id="f36d3-115">This command creates an Azure Traffic Manager profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="f36d3-116">DNS FQDN 已contosoapp.trafficmanager.net。</span><span class="sxs-lookup"><span data-stu-id="f36d3-116">The DNS FQDN is contosoapp.trafficmanager.net.</span></span>

## <span data-ttu-id="f36d3-117">參數</span><span class="sxs-lookup"><span data-stu-id="f36d3-117">PARAMETERS</span></span>

### <span data-ttu-id="f36d3-118">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="f36d3-118">-CustomHeader</span></span>
<span data-ttu-id="f36d3-119">建議要求之自訂標題名稱和值組清單。</span><span class="sxs-lookup"><span data-stu-id="f36d3-119">List of custom header name and value pairs for probe requests.</span></span>

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

### <span data-ttu-id="f36d3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f36d3-120">-DefaultProfile</span></span>
<span data-ttu-id="f36d3-121">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f36d3-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f36d3-122">-ExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="f36d3-122">-ExpectedStatusCodeRange</span></span>
<span data-ttu-id="f36d3-123">建議要求的預期 HTTP 狀態碼範圍清單。</span><span class="sxs-lookup"><span data-stu-id="f36d3-123">List of expected HTTP status code ranges for probe requests.</span></span>

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

### <span data-ttu-id="f36d3-124">-MaxReturn</span><span class="sxs-lookup"><span data-stu-id="f36d3-124">-MaxReturn</span></span>
<span data-ttu-id="f36d3-125">使用多重值路由方法之設定檔所返回的解答數目上限。</span><span class="sxs-lookup"><span data-stu-id="f36d3-125">The maximum number of answers returned for profiles with a MultiValue routing method.</span></span>

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

### <span data-ttu-id="f36d3-126">-MonitorIntervalIn以秒為單位</span><span class="sxs-lookup"><span data-stu-id="f36d3-126">-MonitorIntervalInSeconds</span></span>
<span data-ttu-id="f36d3-127">此時間間隔 (秒) 流量管理員會檢查此設定檔中每個端點的健康情況。</span><span class="sxs-lookup"><span data-stu-id="f36d3-127">The interval (in seconds) at which Traffic Manager will check the health of each endpoint in this profile.</span></span> <span data-ttu-id="f36d3-128">預設值為 30。</span><span class="sxs-lookup"><span data-stu-id="f36d3-128">The default is 30.</span></span>

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

### <span data-ttu-id="f36d3-129">-MonitorPath</span><span class="sxs-lookup"><span data-stu-id="f36d3-129">-MonitorPath</span></span>
<span data-ttu-id="f36d3-130">指定用來監控端點健康情況的路徑。</span><span class="sxs-lookup"><span data-stu-id="f36d3-130">Specifies the path that is used to monitor endpoint health.</span></span>
<span data-ttu-id="f36d3-131">指定相對於端點功能變數名稱的值。</span><span class="sxs-lookup"><span data-stu-id="f36d3-131">Specify a value relative to the endpoint domain name.</span></span>
<span data-ttu-id="f36d3-132">此值必須以斜線 (/) 。</span><span class="sxs-lookup"><span data-stu-id="f36d3-132">This value must begin with a slash (/).</span></span>

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

### <span data-ttu-id="f36d3-133">-MonitorPort</span><span class="sxs-lookup"><span data-stu-id="f36d3-133">-MonitorPort</span></span>
<span data-ttu-id="f36d3-134">指定用來監控端點健康情況之 TCP 埠。</span><span class="sxs-lookup"><span data-stu-id="f36d3-134">Specifies the TCP port that is used to monitor endpoint health.</span></span>
<span data-ttu-id="f36d3-135">有效值是 1 到 65535 的整數。</span><span class="sxs-lookup"><span data-stu-id="f36d3-135">Valid values are integers from 1 through 65535.</span></span>

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

### <span data-ttu-id="f36d3-136">-MonitorProtocol</span><span class="sxs-lookup"><span data-stu-id="f36d3-136">-MonitorProtocol</span></span>
<span data-ttu-id="f36d3-137">指定要用於監控端點健康情況之通訊協定。</span><span class="sxs-lookup"><span data-stu-id="f36d3-137">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="f36d3-138">有效的值為：</span><span class="sxs-lookup"><span data-stu-id="f36d3-138">Valid values are:</span></span>

- <span data-ttu-id="f36d3-139">HTTP</span><span class="sxs-lookup"><span data-stu-id="f36d3-139">HTTP</span></span>
- <span data-ttu-id="f36d3-140">HTTPS</span><span class="sxs-lookup"><span data-stu-id="f36d3-140">HTTPS</span></span>

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

### <span data-ttu-id="f36d3-141">-MonitorTimeoutIn用秒</span><span class="sxs-lookup"><span data-stu-id="f36d3-141">-MonitorTimeoutInSeconds</span></span>
<span data-ttu-id="f36d3-142">流量 (允許) 回應健康情況檢查的時間，以碼錶示。</span><span class="sxs-lookup"><span data-stu-id="f36d3-142">The time (in seconds) that Traffic Manager allows endpoints in this profile to respond to the health check.</span></span> <span data-ttu-id="f36d3-143">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="f36d3-143">The default is 10.</span></span>

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

### <span data-ttu-id="f36d3-144">-MonitorTo本NumberOfFailures</span><span class="sxs-lookup"><span data-stu-id="f36d3-144">-MonitorToleratedNumberOfFailures</span></span>
<span data-ttu-id="f36d3-145">流量管理員在宣告此設定檔中的端點在下次連續健康情況檢查失敗之後降級之前，會先檢查流量管理員的連續健康情況檢查次數。</span><span class="sxs-lookup"><span data-stu-id="f36d3-145">The number of consecutive failed health checks that Traffic Manager tolerates before declaring an endpoint in this profile Degraded after the next consecutive failed health check.</span></span> <span data-ttu-id="f36d3-146">預設值為 3。</span><span class="sxs-lookup"><span data-stu-id="f36d3-146">The default is 3.</span></span>

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

### <span data-ttu-id="f36d3-147">-名稱</span><span class="sxs-lookup"><span data-stu-id="f36d3-147">-Name</span></span>
<span data-ttu-id="f36d3-148">指定此 Cmdlet 所建立的流量管理員設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="f36d3-148">Specifies a name for the Traffic Manager profile that this cmdlet creates.</span></span>

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

### <span data-ttu-id="f36d3-149">-ProfileStatus</span><span class="sxs-lookup"><span data-stu-id="f36d3-149">-ProfileStatus</span></span>
<span data-ttu-id="f36d3-150">指定設定檔的狀態。</span><span class="sxs-lookup"><span data-stu-id="f36d3-150">Specifies the status of the profile.</span></span>
<span data-ttu-id="f36d3-151">有效的值為：啟用和停用。</span><span class="sxs-lookup"><span data-stu-id="f36d3-151">Valid values are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="f36d3-152">-RelativeDnsName</span><span class="sxs-lookup"><span data-stu-id="f36d3-152">-RelativeDnsName</span></span>
<span data-ttu-id="f36d3-153">指定此流量管理員設定檔提供的相對 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="f36d3-153">Specifies the relative DNS name that this Traffic Manager profile provides.</span></span>
<span data-ttu-id="f36d3-154">流量管理員會結合此值和 Azure 流量管理員用來構成設定檔 FQDN (FQDN) 的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="f36d3-154">Traffic Manager combines this value and the DNS domain name that Azure Traffic Manager uses to form the fully qualified domain name (FQDN) of the profile.</span></span>

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

### <span data-ttu-id="f36d3-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f36d3-155">-ResourceGroupName</span></span>
<span data-ttu-id="f36d3-156">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f36d3-156">Specifies the name of a resource group.</span></span>
<span data-ttu-id="f36d3-157">此 Cmdlet 會在此參數指定的群組中建立流量管理員設定檔。</span><span class="sxs-lookup"><span data-stu-id="f36d3-157">This cmdlet creates a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f36d3-158">-標記</span><span class="sxs-lookup"><span data-stu-id="f36d3-158">-Tag</span></span>
<span data-ttu-id="f36d3-159">以雜湊表格形式設定為伺服器上標記的索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="f36d3-159">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="f36d3-160">例如：</span><span class="sxs-lookup"><span data-stu-id="f36d3-160">For example:</span></span>

<span data-ttu-id="f36d3-161">@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="f36d3-161">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f36d3-162">-TrafficRoutingMethod</span><span class="sxs-lookup"><span data-stu-id="f36d3-162">-TrafficRoutingMethod</span></span>
<span data-ttu-id="f36d3-163">指定流量路由方法。</span><span class="sxs-lookup"><span data-stu-id="f36d3-163">Specifies the traffic routing method.</span></span>
<span data-ttu-id="f36d3-164">此方法會決定流量管理員會針對傳入 DNS 查詢所會返回的端點。</span><span class="sxs-lookup"><span data-stu-id="f36d3-164">This method determines which endpoint Traffic Manager returns in response to incoming DNS queries.</span></span>
<span data-ttu-id="f36d3-165">有效的值為：</span><span class="sxs-lookup"><span data-stu-id="f36d3-165">Valid values are:</span></span>

- <span data-ttu-id="f36d3-166">性能</span><span class="sxs-lookup"><span data-stu-id="f36d3-166">Performance</span></span>
- <span data-ttu-id="f36d3-167">加權</span><span class="sxs-lookup"><span data-stu-id="f36d3-167">Weighted</span></span>
- <span data-ttu-id="f36d3-168">優先</span><span class="sxs-lookup"><span data-stu-id="f36d3-168">Priority</span></span>
- <span data-ttu-id="f36d3-169">地理</span><span class="sxs-lookup"><span data-stu-id="f36d3-169">Geographic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Performance, Weighted, Priority, Geographic, Subnet, MultiValue

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f36d3-170">-Ttl</span><span class="sxs-lookup"><span data-stu-id="f36d3-170">-Ttl</span></span>
<span data-ttu-id="f36d3-171">指定 DNS 的活 (TTL) 值。</span><span class="sxs-lookup"><span data-stu-id="f36d3-171">Specifies the DNS Time to Live (TTL) value.</span></span>

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

### <span data-ttu-id="f36d3-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f36d3-172">CommonParameters</span></span>
<span data-ttu-id="f36d3-173">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f36d3-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f36d3-174">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="f36d3-174">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f36d3-175">輸入</span><span class="sxs-lookup"><span data-stu-id="f36d3-175">INPUTS</span></span>

### <span data-ttu-id="f36d3-176">沒有</span><span class="sxs-lookup"><span data-stu-id="f36d3-176">None</span></span>

## <span data-ttu-id="f36d3-177">輸出</span><span class="sxs-lookup"><span data-stu-id="f36d3-177">OUTPUTS</span></span>

### <span data-ttu-id="f36d3-178">Microsoft.Azure.Commands.TrafficManager.models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f36d3-178">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="f36d3-179">筆記</span><span class="sxs-lookup"><span data-stu-id="f36d3-179">NOTES</span></span>

## <span data-ttu-id="f36d3-180">相關連結</span><span class="sxs-lookup"><span data-stu-id="f36d3-180">RELATED LINKS</span></span>

[<span data-ttu-id="f36d3-181">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="f36d3-181">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="f36d3-182">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f36d3-182">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="f36d3-183">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f36d3-183">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="f36d3-184">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f36d3-184">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="f36d3-185">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f36d3-185">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="f36d3-186">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f36d3-186">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


