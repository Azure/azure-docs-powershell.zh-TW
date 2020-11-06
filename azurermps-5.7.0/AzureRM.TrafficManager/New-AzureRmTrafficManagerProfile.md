---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: DE31891A-0EF7-44D7-B955-A3279D27CC21
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/new-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 896324e8d08cae69f24c195de9b44b325985c2c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448524"
---
# <span data-ttu-id="ea508-101">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ea508-101">New-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="ea508-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ea508-102">SYNOPSIS</span></span>
<span data-ttu-id="ea508-103">建立流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="ea508-103">Creates a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea508-104">句法</span><span class="sxs-lookup"><span data-stu-id="ea508-104">SYNTAX</span></span>

```
New-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-ProfileStatus <String>]
 -RelativeDnsName <String> -Ttl <UInt32> -TrafficRoutingMethod <String> -MonitorProtocol <String>
 -MonitorPort <UInt32> [-MonitorPath <String>] [-MonitorIntervalInSeconds <Int32>]
 [-MonitorTimeoutInSeconds <Int32>] [-MonitorToleratedNumberOfFailures <Int32>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea508-105">說明</span><span class="sxs-lookup"><span data-stu-id="ea508-105">DESCRIPTION</span></span>
<span data-ttu-id="ea508-106">**新的-AzureRmTrafficManagerProfile** Cmdlet 會建立 Azure 流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="ea508-106">The **New-AzureRmTrafficManagerProfile** cmdlet creates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="ea508-107">指定 *Name* 參數及必要的設定。</span><span class="sxs-lookup"><span data-stu-id="ea508-107">Specify the *Name* parameter and required settings.</span></span>
<span data-ttu-id="ea508-108">這個 Cmdlet 會傳回代表新設定檔的本機物件。</span><span class="sxs-lookup"><span data-stu-id="ea508-108">This cmdlet returns a local object that represents the new profile.</span></span>

<span data-ttu-id="ea508-109">這個 Cmdlet 不會設定流量管理器端點。</span><span class="sxs-lookup"><span data-stu-id="ea508-109">This cmdlet does not configure Traffic Manager endpoints.</span></span>
<span data-ttu-id="ea508-110">您可以使用 Add-AzureRmTrafficManagerEndpointConfig Cmdlet 來更新本機設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="ea508-110">You can update the local profile object by using the Add-AzureRmTrafficManagerEndpointConfig cmdlet.</span></span>
<span data-ttu-id="ea508-111">然後使用 Set-AzureRmTrafficManagerProfile Cmdlet 將變更上傳到流量管理器。</span><span class="sxs-lookup"><span data-stu-id="ea508-111">Then upload changes to Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="ea508-112">或者，您也可以使用 New-AzureRmTrafficManagerEndpoint Cmdlet 來新增端點。</span><span class="sxs-lookup"><span data-stu-id="ea508-112">Alternatively, you can add endpoints by using the New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="ea508-113">示例</span><span class="sxs-lookup"><span data-stu-id="ea508-113">EXAMPLES</span></span>

### <span data-ttu-id="ea508-114">範例1：建立設定檔</span><span class="sxs-lookup"><span data-stu-id="ea508-114">Example 1: Create a profile</span></span>
```
PS C:\>New-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" -ProfileStatus Enabled -TrafficRoutingMethod Performance -RelativeDnsName "contosoapp" -TTL 30 -MonitorProtocol HTTP -MonitorPort 80 -MonitorPath "/default.aspx"
```

<span data-ttu-id="ea508-115">這個命令會在資源群組 ResourceGroup11 中建立名為 ContosoProfile 的 Azure 流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="ea508-115">This command creates an Azure Traffic Manager profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="ea508-116">DNS FQDN 是 contosoapp.trafficmanager.net。</span><span class="sxs-lookup"><span data-stu-id="ea508-116">The DNS FQDN is contosoapp.trafficmanager.net.</span></span>

## <span data-ttu-id="ea508-117">參數</span><span class="sxs-lookup"><span data-stu-id="ea508-117">PARAMETERS</span></span>

### <span data-ttu-id="ea508-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea508-118">-DefaultProfile</span></span>
<span data-ttu-id="ea508-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ea508-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea508-120">-MonitorIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="ea508-120">-MonitorIntervalInSeconds</span></span>
<span data-ttu-id="ea508-121">間隔 (以秒為單位) 流量管理員將在此設定檔中檢查每個端點的健康情況。</span><span class="sxs-lookup"><span data-stu-id="ea508-121">The interval (in seconds) at which Traffic Manager will check the health of each endpoint in this profile.</span></span> <span data-ttu-id="ea508-122">預設值為30。</span><span class="sxs-lookup"><span data-stu-id="ea508-122">The default is 30.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: IntervalInSecondsForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea508-123">-MonitorPath</span><span class="sxs-lookup"><span data-stu-id="ea508-123">-MonitorPath</span></span>
<span data-ttu-id="ea508-124">指定用來監視端點健康情況的路徑。</span><span class="sxs-lookup"><span data-stu-id="ea508-124">Specifies the path that is used to monitor endpoint health.</span></span>
<span data-ttu-id="ea508-125">指定相對於端點網功能變數名稱稱的值。</span><span class="sxs-lookup"><span data-stu-id="ea508-125">Specify a value relative to the endpoint domain name.</span></span>
<span data-ttu-id="ea508-126">此值必須以斜線 (/) 開頭。</span><span class="sxs-lookup"><span data-stu-id="ea508-126">This value must begin with a slash (/).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: PathForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea508-127">-MonitorPort</span><span class="sxs-lookup"><span data-stu-id="ea508-127">-MonitorPort</span></span>
<span data-ttu-id="ea508-128">指定用來監視端點健康情況的 TCP 埠。</span><span class="sxs-lookup"><span data-stu-id="ea508-128">Specifies the TCP port that is used to monitor endpoint health.</span></span>
<span data-ttu-id="ea508-129">有效的值是從1到65535的整數。</span><span class="sxs-lookup"><span data-stu-id="ea508-129">Valid values are integers from 1 through 65535.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: PortForMonitor

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea508-130">-MonitorProtocol</span><span class="sxs-lookup"><span data-stu-id="ea508-130">-MonitorProtocol</span></span>
<span data-ttu-id="ea508-131">指定用來監視端點健康情況的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="ea508-131">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="ea508-132">有效值為：</span><span class="sxs-lookup"><span data-stu-id="ea508-132">Valid values are:</span></span>

- <span data-ttu-id="ea508-133">HTTP</span><span class="sxs-lookup"><span data-stu-id="ea508-133">HTTP</span></span>
- <span data-ttu-id="ea508-134">IP-HTTPS</span><span class="sxs-lookup"><span data-stu-id="ea508-134">HTTPS</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ProtocolForMonitor
Accepted values: HTTP, HTTPS, TCP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea508-135">-MonitorTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="ea508-135">-MonitorTimeoutInSeconds</span></span>
<span data-ttu-id="ea508-136">流量管理器允許此設定檔中的端點回應健康情況檢查的時間 (以秒為單位）) 。</span><span class="sxs-lookup"><span data-stu-id="ea508-136">The time (in seconds) that Traffic Manager allows endpoints in this profile to respond to the health check.</span></span> <span data-ttu-id="ea508-137">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="ea508-137">The default is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: TimeoutInSecondsForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea508-138">-MonitorToleratedNumberOfFailures</span><span class="sxs-lookup"><span data-stu-id="ea508-138">-MonitorToleratedNumberOfFailures</span></span>
<span data-ttu-id="ea508-139">在此設定檔中宣告端點前，在下一個連續失敗狀況檢查已降級之後，通信量 Manager tolerates 的連續失敗狀況檢查次數。</span><span class="sxs-lookup"><span data-stu-id="ea508-139">The number of consecutive failed health checks that Traffic Manager tolerates before declaring an endpoint in this profile Degraded after the next consecutive failed health check.</span></span> <span data-ttu-id="ea508-140">預設值為3。</span><span class="sxs-lookup"><span data-stu-id="ea508-140">The default is 3.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: ToleratedNumberOfFailuresForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea508-141">-名稱</span><span class="sxs-lookup"><span data-stu-id="ea508-141">-Name</span></span>
<span data-ttu-id="ea508-142">指定此 Cmdlet 所建立之流量管理器設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="ea508-142">Specifies a name for the Traffic Manager profile that this cmdlet creates.</span></span>

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

### <span data-ttu-id="ea508-143">-ProfileStatus</span><span class="sxs-lookup"><span data-stu-id="ea508-143">-ProfileStatus</span></span>
<span data-ttu-id="ea508-144">指定設定檔的狀態。</span><span class="sxs-lookup"><span data-stu-id="ea508-144">Specifies the status of the profile.</span></span>
<span data-ttu-id="ea508-145">有效值為： Enabled 和 Disabled。</span><span class="sxs-lookup"><span data-stu-id="ea508-145">Valid values are: Enabled and Disabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea508-146">-RelativeDnsName</span><span class="sxs-lookup"><span data-stu-id="ea508-146">-RelativeDnsName</span></span>
<span data-ttu-id="ea508-147">指定此流量管理器設定檔所提供的相對 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="ea508-147">Specifies the relative DNS name that this Traffic Manager profile provides.</span></span>
<span data-ttu-id="ea508-148">流量管理器結合此值與 DNS 功能變數名稱，而 Azure 流量 Manager 會使用該名稱來構成設定檔的完整功能變數名稱 (FQDN) 。</span><span class="sxs-lookup"><span data-stu-id="ea508-148">Traffic Manager combines this value and the DNS domain name that Azure Traffic Manager uses to form the fully qualified domain name (FQDN) of the profile.</span></span>

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

### <span data-ttu-id="ea508-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea508-149">-ResourceGroupName</span></span>
<span data-ttu-id="ea508-150">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ea508-150">Specifies the name of a resource group.</span></span>
<span data-ttu-id="ea508-151">這個 Cmdlet 會在此參數指定的群組中建立流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="ea508-151">This cmdlet creates a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ea508-152">-Tag</span><span class="sxs-lookup"><span data-stu-id="ea508-152">-Tag</span></span>
<span data-ttu-id="ea508-153">在伺服器上將雜湊表的格式設定為標記的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="ea508-153">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="ea508-154">例如：</span><span class="sxs-lookup"><span data-stu-id="ea508-154">For example:</span></span>

<span data-ttu-id="ea508-155">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="ea508-155">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea508-156">-TrafficRoutingMethod</span><span class="sxs-lookup"><span data-stu-id="ea508-156">-TrafficRoutingMethod</span></span>
<span data-ttu-id="ea508-157">指定流量路由方法。</span><span class="sxs-lookup"><span data-stu-id="ea508-157">Specifies the traffic routing method.</span></span>
<span data-ttu-id="ea508-158">這個方法會判斷哪個端點流量主管會傳回，以回應傳入的 DNS 查詢。</span><span class="sxs-lookup"><span data-stu-id="ea508-158">This method determines which endpoint Traffic Manager returns in response to incoming DNS queries.</span></span>
<span data-ttu-id="ea508-159">有效值為：</span><span class="sxs-lookup"><span data-stu-id="ea508-159">Valid values are:</span></span>

- <span data-ttu-id="ea508-160">提高</span><span class="sxs-lookup"><span data-stu-id="ea508-160">Performance</span></span>
- <span data-ttu-id="ea508-161">加</span><span class="sxs-lookup"><span data-stu-id="ea508-161">Weighted</span></span>
- <span data-ttu-id="ea508-162">優先順序</span><span class="sxs-lookup"><span data-stu-id="ea508-162">Priority</span></span>
- <span data-ttu-id="ea508-163">位置</span><span class="sxs-lookup"><span data-stu-id="ea508-163">Geographic</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Performance, Weighted, Priority, Geographic

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea508-164">-Ttl</span><span class="sxs-lookup"><span data-stu-id="ea508-164">-Ttl</span></span>
<span data-ttu-id="ea508-165">指定 (TTL) 值的 DNS 時間。</span><span class="sxs-lookup"><span data-stu-id="ea508-165">Specifies the DNS Time to Live (TTL) value.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea508-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea508-166">CommonParameters</span></span>
<span data-ttu-id="ea508-167">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ea508-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea508-168">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ea508-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea508-169">輸入</span><span class="sxs-lookup"><span data-stu-id="ea508-169">INPUTS</span></span>

### <span data-ttu-id="ea508-170">所有</span><span class="sxs-lookup"><span data-stu-id="ea508-170">None</span></span>
<span data-ttu-id="ea508-171">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="ea508-171">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ea508-172">輸出</span><span class="sxs-lookup"><span data-stu-id="ea508-172">OUTPUTS</span></span>

### <span data-ttu-id="ea508-173">TrafficManagerProfile （）</span><span class="sxs-lookup"><span data-stu-id="ea508-173">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="ea508-174">這個 Cmdlet 會傳回新的 TrafficManagerProfile 物件。</span><span class="sxs-lookup"><span data-stu-id="ea508-174">This cmdlet returns a new TrafficManagerProfile object.</span></span>

## <span data-ttu-id="ea508-175">筆記</span><span class="sxs-lookup"><span data-stu-id="ea508-175">NOTES</span></span>

## <span data-ttu-id="ea508-176">相關連結</span><span class="sxs-lookup"><span data-stu-id="ea508-176">RELATED LINKS</span></span>

[<span data-ttu-id="ea508-177">附加 AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="ea508-177">Add-AzureRmTrafficManagerEndpointConfig</span></span>](./Add-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="ea508-178">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ea508-178">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="ea508-179">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ea508-179">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="ea508-180">AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ea508-180">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="ea508-181">移除-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ea508-181">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="ea508-182">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ea508-182">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


