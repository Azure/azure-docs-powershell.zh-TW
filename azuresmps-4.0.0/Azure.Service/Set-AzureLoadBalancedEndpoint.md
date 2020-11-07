---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7259C717-250C-454A-B0DF-738B70747FF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 298633bbc95bfb13ae340dea242c6c04267d479e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967399"
---
# <span data-ttu-id="67092-101">Set-AzureLoadBalancedEndpoint</span><span class="sxs-lookup"><span data-stu-id="67092-101">Set-AzureLoadBalancedEndpoint</span></span>

## <span data-ttu-id="67092-102">摘要</span><span class="sxs-lookup"><span data-stu-id="67092-102">SYNOPSIS</span></span>
<span data-ttu-id="67092-103">修改 Azure 服務內的負載等化器集中的所有端點。</span><span class="sxs-lookup"><span data-stu-id="67092-103">Modifies all of the endpoints in a load balancer set within an Azure service.</span></span>

## <span data-ttu-id="67092-104">句法</span><span class="sxs-lookup"><span data-stu-id="67092-104">SYNTAX</span></span>

### <span data-ttu-id="67092-105">DefaultProbe (預設) </span><span class="sxs-lookup"><span data-stu-id="67092-105">DefaultProbe (Default)</span></span>
```
Set-AzureLoadBalancedEndpoint -LBSetName <String> [-Protocol <String>] [-LocalPort <Int32>]
 [-PublicPort <Int32>] [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="67092-106">TCPProbe</span><span class="sxs-lookup"><span data-stu-id="67092-106">TCPProbe</span></span>
```
Set-AzureLoadBalancedEndpoint -LBSetName <String> [-Protocol <String>] [-LocalPort <Int32>]
 [-PublicPort <Int32>] [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-ProbeProtocolTCP]
 [-ProbePort <Int32>] [-ProbeIntervalInSeconds <Int32>] [-ProbeTimeoutInSeconds <Int32>]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="67092-107">HTTPProbe</span><span class="sxs-lookup"><span data-stu-id="67092-107">HTTPProbe</span></span>
```
Set-AzureLoadBalancedEndpoint -LBSetName <String> [-Protocol <String>] [-LocalPort <Int32>]
 [-PublicPort <Int32>] [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-ProbeProtocolHTTP]
 -ProbePath <String> [-ProbePort <Int32>] [-ProbeIntervalInSeconds <Int32>] [-ProbeTimeoutInSeconds <Int32>]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="67092-108">說明</span><span class="sxs-lookup"><span data-stu-id="67092-108">DESCRIPTION</span></span>
<span data-ttu-id="67092-109">**AzureLoadBalancedEndpoint** Cmdlet 會修改 Azure 服務集中的負載平衡器中的所有端點。</span><span class="sxs-lookup"><span data-stu-id="67092-109">The **Set-AzureLoadBalancedEndpoint** cmdlet modifies all of the endpoints in a load balancer set in an Azure service.</span></span>

## <span data-ttu-id="67092-110">示例</span><span class="sxs-lookup"><span data-stu-id="67092-110">EXAMPLES</span></span>

### <span data-ttu-id="67092-111">範例1：修改負載等化器集中的端點</span><span class="sxs-lookup"><span data-stu-id="67092-111">Example 1: Modify the endpoints in a load balancer set</span></span>
```
PS C:\> Set-AzureLoadBalancedEndpoint -ServiceName "ContosoService" -LBSetName "LBSet01" -Protocol "TCP" -LocalPort 80 -ProbeProtocolTCP -ProbePort 8080
```

<span data-ttu-id="67092-112">這個命令會修改名為 LBSet01 的負載等化器集中的所有端點，以使用 TCP 通訊協定和私人埠80。</span><span class="sxs-lookup"><span data-stu-id="67092-112">This command modifies all endpoints in the load balancer set named LBSet01 to use the TCP protocol and private port 80.</span></span>
<span data-ttu-id="67092-113">此命令會將負載平衡器探測器設定為使用埠8080上的 TCP 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="67092-113">The command sets the load balancer probe to use the TCP protocol on port 8080.</span></span>

### <span data-ttu-id="67092-114">範例2：指定不同的虛擬 IP</span><span class="sxs-lookup"><span data-stu-id="67092-114">Example 2: Specify a different virtual IP</span></span>
```
PS C:\> Set-AzureLoadBalancedEndpoint -ServiceName "ContosoService" -LBSetName "LBSet02" -VirtualIPName "Vip01"
```

<span data-ttu-id="67092-115">這個命令會修改具有負載等化器集名稱的負載平衡器，以使用名為 Vip01 的虛擬 IP。</span><span class="sxs-lookup"><span data-stu-id="67092-115">This command modifies the load balancer that has the load balancer set name to use a virtual IP named Vip01.</span></span>

## <span data-ttu-id="67092-116">參數</span><span class="sxs-lookup"><span data-stu-id="67092-116">PARAMETERS</span></span>

### <span data-ttu-id="67092-117">-ACL</span><span class="sxs-lookup"><span data-stu-id="67092-117">-ACL</span></span>
<span data-ttu-id="67092-118">指定 (ACL) 設定物件的存取控制清單，此 Cmdlet 適用于端點。</span><span class="sxs-lookup"><span data-stu-id="67092-118">Specifies an access control list (ACL) configuration object that this cmdlet applies to the endpoints.</span></span>

```yaml
Type: NetworkAclObject
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67092-119">-DirectServerReturn</span><span class="sxs-lookup"><span data-stu-id="67092-119">-DirectServerReturn</span></span>
<span data-ttu-id="67092-120">指定此 Cmdlet 是否允許直接返回伺服器。</span><span class="sxs-lookup"><span data-stu-id="67092-120">Specifies whether this cmdlet enables direct server return.</span></span>
<span data-ttu-id="67092-121">指定要啟用 $True，或 $False 以停用。</span><span class="sxs-lookup"><span data-stu-id="67092-121">Specify $True to enable, or $False to disable.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67092-122">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="67092-122">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="67092-123">指定端點的 TCP 空閒超時期間（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="67092-123">Specifies the TCP idle time-out period, in minutes, for the endpoints.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67092-124">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="67092-124">-InformationAction</span></span>
<span data-ttu-id="67092-125">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="67092-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="67092-126">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="67092-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="67092-127">持續</span><span class="sxs-lookup"><span data-stu-id="67092-127">Continue</span></span>
- <span data-ttu-id="67092-128">理會</span><span class="sxs-lookup"><span data-stu-id="67092-128">Ignore</span></span>
- <span data-ttu-id="67092-129">看</span><span class="sxs-lookup"><span data-stu-id="67092-129">Inquire</span></span>
- <span data-ttu-id="67092-130">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="67092-130">SilentlyContinue</span></span>
- <span data-ttu-id="67092-131">停止</span><span class="sxs-lookup"><span data-stu-id="67092-131">Stop</span></span>
- <span data-ttu-id="67092-132">封存</span><span class="sxs-lookup"><span data-stu-id="67092-132">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67092-133">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="67092-133">-InformationVariable</span></span>
<span data-ttu-id="67092-134">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="67092-134">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67092-135">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="67092-135">-InternalLoadBalancerName</span></span>
<span data-ttu-id="67092-136">指定此 Cmdlet 包含在配置中的內部負載等化器名稱。</span><span class="sxs-lookup"><span data-stu-id="67092-136">Specifies the name of the internal load balancer that this cmdlet includes in the configuration.</span></span>

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

### <span data-ttu-id="67092-137">-LBSetName</span><span class="sxs-lookup"><span data-stu-id="67092-137">-LBSetName</span></span>
<span data-ttu-id="67092-138">指定此 Cmdlet 更新之負載等化器集的名稱。</span><span class="sxs-lookup"><span data-stu-id="67092-138">Specifies the name of the load balancer set that this cmdlet updates.</span></span>

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

### <span data-ttu-id="67092-139">-LoadBalancerDistribution</span><span class="sxs-lookup"><span data-stu-id="67092-139">-LoadBalancerDistribution</span></span>
<span data-ttu-id="67092-140">指定負載平衡器分配演算法。</span><span class="sxs-lookup"><span data-stu-id="67092-140">Specifies the load balancer distribution algorithm.</span></span>
<span data-ttu-id="67092-141">有效值為：</span><span class="sxs-lookup"><span data-stu-id="67092-141">Valid values are:</span></span> 

- <span data-ttu-id="67092-142">sourceIP.</span><span class="sxs-lookup"><span data-stu-id="67092-142">sourceIP.</span></span>
<span data-ttu-id="67092-143">兩個元組關聯：來源 IP、目的地 IP</span><span class="sxs-lookup"><span data-stu-id="67092-143">A two tuple affinity: Source IP, Destination IP</span></span> 
- <span data-ttu-id="67092-144">sourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="67092-144">sourceIPProtocol.</span></span>
<span data-ttu-id="67092-145">三個元組關聯：來源 IP、目的地 IP、通訊協定</span><span class="sxs-lookup"><span data-stu-id="67092-145">A three tuple affinity: Source IP, Destination IP, Protocol</span></span> 
- <span data-ttu-id="67092-146">所有.</span><span class="sxs-lookup"><span data-stu-id="67092-146">none.</span></span>
<span data-ttu-id="67092-147">五個元組關聯：來源 IP、來源埠、目的地 IP、目的地埠、通訊協定</span><span class="sxs-lookup"><span data-stu-id="67092-147">A five tuple affinity: Source IP, Source Port, Destination IP, Destination Port, Protocol</span></span> 

<span data-ttu-id="67092-148">預設值為 [無]。</span><span class="sxs-lookup"><span data-stu-id="67092-148">The default value is none.</span></span>

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

### <span data-ttu-id="67092-149">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="67092-149">-LocalPort</span></span>
<span data-ttu-id="67092-150">指定這些端點所使用的本機、私人埠。</span><span class="sxs-lookup"><span data-stu-id="67092-150">Specifies the local, private, port that these endpoints use.</span></span>
<span data-ttu-id="67092-151">虛擬機器中的應用程式在此埠上偵聽此端點的服務輸入要求。</span><span class="sxs-lookup"><span data-stu-id="67092-151">Applications in the virtual machine listen on this port for service input requests for this endpoint.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67092-152">-ProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="67092-152">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="67092-153">指定端點的探針巡迴檢測間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="67092-153">Specifies the probe polling interval, in seconds, for the endpoints.</span></span>

```yaml
Type: Int32
Parameter Sets: TCPProbe, HTTPProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67092-154">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="67092-154">-ProbePath</span></span>
<span data-ttu-id="67092-155">指定 HTTP 探測的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="67092-155">Specifies the relative path of the HTTP Probe.</span></span>

```yaml
Type: String
Parameter Sets: HTTPProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67092-156">-ProbePort</span><span class="sxs-lookup"><span data-stu-id="67092-156">-ProbePort</span></span>
<span data-ttu-id="67092-157">指定負載平衡器探針所使用的埠。</span><span class="sxs-lookup"><span data-stu-id="67092-157">Specifies the port that the load balancer probe uses.</span></span>

```yaml
Type: Int32
Parameter Sets: TCPProbe, HTTPProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67092-158">-ProbeProtocolHTTP</span><span class="sxs-lookup"><span data-stu-id="67092-158">-ProbeProtocolHTTP</span></span>
<span data-ttu-id="67092-159">指定負載平衡器端點使用 HTTP 探測。</span><span class="sxs-lookup"><span data-stu-id="67092-159">Specifies that the load balancer endpoints use an HTTP Probe.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: HTTPProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67092-160">-ProbeProtocolTCP</span><span class="sxs-lookup"><span data-stu-id="67092-160">-ProbeProtocolTCP</span></span>
<span data-ttu-id="67092-161">指定負載平衡器端點使用 TCP 探測。</span><span class="sxs-lookup"><span data-stu-id="67092-161">Specifies that the load balancer endpoints use a TCP Probe.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: TCPProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67092-162">-ProbeTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="67092-162">-ProbeTimeoutInSeconds</span></span>
<span data-ttu-id="67092-163">指定探測巡迴檢測超時時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="67092-163">Specifies the probe polling time-out in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: TCPProbe, HTTPProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67092-164">-設定檔</span><span class="sxs-lookup"><span data-stu-id="67092-164">-Profile</span></span>
<span data-ttu-id="67092-165">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="67092-165">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="67092-166">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="67092-166">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67092-167">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="67092-167">-Protocol</span></span>
<span data-ttu-id="67092-168">指定端點的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="67092-168">Specifies the protocol of the endpoints.</span></span>
<span data-ttu-id="67092-169">有效值為：</span><span class="sxs-lookup"><span data-stu-id="67092-169">Valid values are:</span></span> 

- <span data-ttu-id="67092-170">TCP-OUT</span><span class="sxs-lookup"><span data-stu-id="67092-170">TCP</span></span> 
- <span data-ttu-id="67092-171">UDP-IN</span><span class="sxs-lookup"><span data-stu-id="67092-171">UDP</span></span>

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

### <span data-ttu-id="67092-172">-PublicPort</span><span class="sxs-lookup"><span data-stu-id="67092-172">-PublicPort</span></span>
<span data-ttu-id="67092-173">指定端點使用的公用埠。</span><span class="sxs-lookup"><span data-stu-id="67092-173">Specifies the public port that the endpoint uses.</span></span>
<span data-ttu-id="67092-174">如果您沒有指定值，Azure 會指派可用的埠。</span><span class="sxs-lookup"><span data-stu-id="67092-174">If you do not specify a value, Azure assigns an available port.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67092-175">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="67092-175">-ServiceName</span></span>
<span data-ttu-id="67092-176">指定包含此 Cmdlet 所修改之端點的 Azure 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="67092-176">Specifies the name of the Azure service that contains the endpoints that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67092-177">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="67092-177">-VirtualIPName</span></span>
<span data-ttu-id="67092-178">指定 Azure 與端點相關聯之虛擬 IP 位址的名稱。</span><span class="sxs-lookup"><span data-stu-id="67092-178">Specifies the name of a virtual IP address that Azure associates to the endpoints.</span></span>
<span data-ttu-id="67092-179">若要新增虛擬 Ip 至您的服務，請使用 **AzureVirtualIP** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="67092-179">To add virtual IPs to your service, use the **Add-AzureVirtualIP** cmdlet.</span></span>

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

### <span data-ttu-id="67092-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67092-180">CommonParameters</span></span>
<span data-ttu-id="67092-181">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="67092-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67092-182">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="67092-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67092-183">輸入</span><span class="sxs-lookup"><span data-stu-id="67092-183">INPUTS</span></span>

## <span data-ttu-id="67092-184">輸出</span><span class="sxs-lookup"><span data-stu-id="67092-184">OUTPUTS</span></span>

## <span data-ttu-id="67092-185">筆記</span><span class="sxs-lookup"><span data-stu-id="67092-185">NOTES</span></span>

## <span data-ttu-id="67092-186">相關連結</span><span class="sxs-lookup"><span data-stu-id="67092-186">RELATED LINKS</span></span>

[<span data-ttu-id="67092-187">附加 AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="67092-187">Add-AzureVirtualIP</span></span>](./Add-AzureVirtualIP.md)

[<span data-ttu-id="67092-188">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="67092-188">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)


