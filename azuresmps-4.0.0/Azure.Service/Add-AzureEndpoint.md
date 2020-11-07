---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D767F017-6545-4BC6-927E-E7A99A08D5D2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5b3122795f2af33a28206936b7b28322ad171b19
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967179"
---
# <span data-ttu-id="1684f-101">Add-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="1684f-101">Add-AzureEndpoint</span></span>

## <span data-ttu-id="1684f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1684f-102">SYNOPSIS</span></span>
<span data-ttu-id="1684f-103">將端點新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="1684f-103">Adds an endpoint to a virtual machine.</span></span>

## <span data-ttu-id="1684f-104">句法</span><span class="sxs-lookup"><span data-stu-id="1684f-104">SYNTAX</span></span>

### <span data-ttu-id="1684f-105">NoLB (預設) </span><span class="sxs-lookup"><span data-stu-id="1684f-105">NoLB (Default)</span></span>
```
Add-AzureEndpoint [-Name] <String> [-Protocol] <String> [-LocalPort] <Int32> [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-InternalLoadBalancerName <String>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>] [-VirtualIPName <String>]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="1684f-106">LBNoProbe</span><span class="sxs-lookup"><span data-stu-id="1684f-106">LBNoProbe</span></span>
```
Add-AzureEndpoint [-Name] <String> [-Protocol] <String> [-LocalPort] <Int32> [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] -LBSetName <String> [-NoProbe]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="1684f-107">LBDefaultProbe</span><span class="sxs-lookup"><span data-stu-id="1684f-107">LBDefaultProbe</span></span>
```
Add-AzureEndpoint [-Name] <String> [-Protocol] <String> [-LocalPort] <Int32> [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] -LBSetName <String> [-DefaultProbe]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="1684f-108">LBCustomProbe</span><span class="sxs-lookup"><span data-stu-id="1684f-108">LBCustomProbe</span></span>
```
Add-AzureEndpoint [-Name] <String> [-Protocol] <String> [-LocalPort] <Int32> [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] -LBSetName <String> -ProbePort <Int32>
 -ProbeProtocol <String> [-ProbePath <String>] [-ProbeIntervalInSeconds <Int32>]
 [-ProbeTimeoutInSeconds <Int32>] [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>]
 [-LoadBalancerDistribution <String>] [-VirtualIPName <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1684f-109">說明</span><span class="sxs-lookup"><span data-stu-id="1684f-109">DESCRIPTION</span></span>
<span data-ttu-id="1684f-110">**AzureEndpoint** Cmdlet 會將端點新增至 Azure 虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="1684f-110">The **Add-AzureEndpoint** cmdlet adds an endpoint to an Azure virtual machine object.</span></span>

## <span data-ttu-id="1684f-111">示例</span><span class="sxs-lookup"><span data-stu-id="1684f-111">EXAMPLES</span></span>

### <span data-ttu-id="1684f-112">範例1：新增端點</span><span class="sxs-lookup"><span data-stu-id="1684f-112">Example 1: Add an endpoint</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirutalMachine01" | Add-AzureEndpoint -Name "HttpIn" -Protocol "tcp" -PublicPort 80 -LocalPort 8080 | Update-AzureVM
```

<span data-ttu-id="1684f-113">這個命令會使用 **add-azurevm** Cmdlet 來檢索名為 VirtualMachine01 的虛擬機器的設定。</span><span class="sxs-lookup"><span data-stu-id="1684f-113">This command retrieves the configuration of a virtual machine named VirtualMachine01 by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="1684f-114">命令會使用管線運算子將它傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1684f-114">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1684f-115">這個 Cmdlet 會新增一個名為 HttpIn 的端點。</span><span class="sxs-lookup"><span data-stu-id="1684f-115">This cmdlet adds an endpoint named HttpIn.</span></span>
<span data-ttu-id="1684f-116">端點擁有公用埠80和本機埠8080。</span><span class="sxs-lookup"><span data-stu-id="1684f-116">The endpoint has a public port 80 and local port 8080.</span></span>
<span data-ttu-id="1684f-117">該命令會將虛擬機器物件傳遞到會實現變更的 **add-azurevm** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1684f-117">The command passes the virtual machine object to the **Update-AzureVM** cmdlet, which implements your changes.</span></span>

### <span data-ttu-id="1684f-118">範例2：新增屬於負載平衡群組的端點</span><span class="sxs-lookup"><span data-stu-id="1684f-118">Example 2: Add an endpoint that belongs to a load balanced group</span></span>
```
PS C:\> Get-AzureVM -ServiceName "LoadBalancedService" -Name "VirtualMachine12" | Add-AzureEndpoint -Name "HttpIn" -Protocol "tcp" -PublicPort 80 -LocalPort 8080 -LBSetName "WebFarm" -ProbePort 80 -ProbeProtocol "http" -ProbePath '/' | Update-AzureVM
```

<span data-ttu-id="1684f-119">這個命令會檢索名為 VirtualMachine07 的虛擬機器的設定。</span><span class="sxs-lookup"><span data-stu-id="1684f-119">This command retrieves the configuration of a virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="1684f-120">目前的 Cmdlet 會新增一個名為 HttpIn 的端點。</span><span class="sxs-lookup"><span data-stu-id="1684f-120">The current cmdlet adds an endpoint named HttpIn.</span></span>
<span data-ttu-id="1684f-121">端點擁有公用埠80和本機埠8080。</span><span class="sxs-lookup"><span data-stu-id="1684f-121">The endpoint has a public port 80 and local port 8080.</span></span>
<span data-ttu-id="1684f-122">端點屬於名為 WebFarm 的共用負載平衡組。</span><span class="sxs-lookup"><span data-stu-id="1684f-122">The endpoint belongs to the shared load balanced group named WebFarm.</span></span>
<span data-ttu-id="1684f-123">埠80上的 HTTP 探測，路徑為 "/" 會監視端點的可用性。</span><span class="sxs-lookup"><span data-stu-id="1684f-123">An HTTP probe on port 80 with a path of '/' monitors the availability of the endpoint.</span></span>
<span data-ttu-id="1684f-124">命令會實現您的變更。</span><span class="sxs-lookup"><span data-stu-id="1684f-124">The command implements your changes.</span></span>

### <span data-ttu-id="1684f-125">範例3：將虛擬 IP 與端點建立關聯</span><span class="sxs-lookup"><span data-stu-id="1684f-125">Example 3: Associate a virtual IP to an endpoint</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine25" | Add-AzureEndpoint -Name "HttpIn" -Protocol "tcp" -LocalPort 8080 -PublicPort 80 -VirtualIPName "ContosoVip11" | Update-AzureVM
```

<span data-ttu-id="1684f-126">這個命令會檢索名為 VirtualMachine25 的虛擬機器的設定。</span><span class="sxs-lookup"><span data-stu-id="1684f-126">This command retrieves the configuration of a virtual machine named VirtualMachine25.</span></span>
<span data-ttu-id="1684f-127">目前的 Cmdlet 會新增一個名為 HttpIn 的端點。</span><span class="sxs-lookup"><span data-stu-id="1684f-127">The current cmdlet adds an endpoint named HttpIn.</span></span>
<span data-ttu-id="1684f-128">端點擁有公用埠80和本機埠8080。</span><span class="sxs-lookup"><span data-stu-id="1684f-128">The endpoint has a public port 80 and local port 8080.</span></span>
<span data-ttu-id="1684f-129">這個命令會將虛擬 IP 與端點相關聯。</span><span class="sxs-lookup"><span data-stu-id="1684f-129">This command associates a virtual IP to the endpoint.</span></span>
<span data-ttu-id="1684f-130">命令會實現您的變更。</span><span class="sxs-lookup"><span data-stu-id="1684f-130">The command implements your changes.</span></span>

## <span data-ttu-id="1684f-131">參數</span><span class="sxs-lookup"><span data-stu-id="1684f-131">PARAMETERS</span></span>

### <span data-ttu-id="1684f-132">-ACL</span><span class="sxs-lookup"><span data-stu-id="1684f-132">-ACL</span></span>
<span data-ttu-id="1684f-133">指定端點 (ACL) 設定物件的存取控制清單。</span><span class="sxs-lookup"><span data-stu-id="1684f-133">Specifies an access control list (ACL) configuration object for the endpoint.</span></span>

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

### <span data-ttu-id="1684f-134">-DefaultProbe</span><span class="sxs-lookup"><span data-stu-id="1684f-134">-DefaultProbe</span></span>
<span data-ttu-id="1684f-135">表示此 Cmdlet 使用預設的探測設定。</span><span class="sxs-lookup"><span data-stu-id="1684f-135">Indicates that this cmdlet uses the default probe setting.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LBDefaultProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1684f-136">-DirectServerReturn</span><span class="sxs-lookup"><span data-stu-id="1684f-136">-DirectServerReturn</span></span>
<span data-ttu-id="1684f-137">指定此 Cmdlet 是否允許直接返回伺服器。</span><span class="sxs-lookup"><span data-stu-id="1684f-137">Specifies whether this cmdlet enables direct server return.</span></span>
<span data-ttu-id="1684f-138">指定要啟用 $True，或 $False 以停用。</span><span class="sxs-lookup"><span data-stu-id="1684f-138">Specify $True to enable, or $False to disable.</span></span>

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

### <span data-ttu-id="1684f-139">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="1684f-139">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="1684f-140">指定端點的 TCP 空閒超時期間（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="1684f-140">Specifies the TCP idle time-out period, in minutes, for the endpoint.</span></span>

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

### <span data-ttu-id="1684f-141">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="1684f-141">-InformationAction</span></span>
<span data-ttu-id="1684f-142">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="1684f-142">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1684f-143">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="1684f-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1684f-144">持續</span><span class="sxs-lookup"><span data-stu-id="1684f-144">Continue</span></span>
- <span data-ttu-id="1684f-145">理會</span><span class="sxs-lookup"><span data-stu-id="1684f-145">Ignore</span></span>
- <span data-ttu-id="1684f-146">看</span><span class="sxs-lookup"><span data-stu-id="1684f-146">Inquire</span></span>
- <span data-ttu-id="1684f-147">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1684f-147">SilentlyContinue</span></span>
- <span data-ttu-id="1684f-148">停止</span><span class="sxs-lookup"><span data-stu-id="1684f-148">Stop</span></span>
- <span data-ttu-id="1684f-149">封存</span><span class="sxs-lookup"><span data-stu-id="1684f-149">Suspend</span></span>

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

### <span data-ttu-id="1684f-150">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1684f-150">-InformationVariable</span></span>
<span data-ttu-id="1684f-151">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="1684f-151">Specifies an information variable.</span></span>

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

### <span data-ttu-id="1684f-152">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="1684f-152">-InternalLoadBalancerName</span></span>
<span data-ttu-id="1684f-153">指定內部負載平衡器的名稱。</span><span class="sxs-lookup"><span data-stu-id="1684f-153">Specifies the name of the internal load balancer.</span></span>

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

### <span data-ttu-id="1684f-154">-LBSetName</span><span class="sxs-lookup"><span data-stu-id="1684f-154">-LBSetName</span></span>
<span data-ttu-id="1684f-155">指定端點的負載平衡器集的名稱。</span><span class="sxs-lookup"><span data-stu-id="1684f-155">Specifies the name of the load balancer set for the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: LBNoProbe, LBDefaultProbe, LBCustomProbe
Aliases: LoadBalancedEndpointSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1684f-156">-LoadBalancerDistribution</span><span class="sxs-lookup"><span data-stu-id="1684f-156">-LoadBalancerDistribution</span></span>
<span data-ttu-id="1684f-157">指定負載平衡器分配演算法。</span><span class="sxs-lookup"><span data-stu-id="1684f-157">Specifies the load balancer distribution algorithm.</span></span>
<span data-ttu-id="1684f-158">有效值為：</span><span class="sxs-lookup"><span data-stu-id="1684f-158">Valid values are:</span></span> 

- <span data-ttu-id="1684f-159">sourceIP.</span><span class="sxs-lookup"><span data-stu-id="1684f-159">sourceIP.</span></span>
<span data-ttu-id="1684f-160">兩個元組關聯：來源 IP、目的地 IP</span><span class="sxs-lookup"><span data-stu-id="1684f-160">A two tuple affinity: Source IP, Destination IP</span></span> 
- <span data-ttu-id="1684f-161">sourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="1684f-161">sourceIPProtocol.</span></span>
<span data-ttu-id="1684f-162">三個元組關聯：來源 IP、目的地 IP、通訊協定</span><span class="sxs-lookup"><span data-stu-id="1684f-162">A three tuple affinity: Source IP, Destination IP, Protocol</span></span> 
- <span data-ttu-id="1684f-163">所有.</span><span class="sxs-lookup"><span data-stu-id="1684f-163">none.</span></span>
<span data-ttu-id="1684f-164">五個元組關聯：來源 IP、來源埠、目的地 IP、目的地埠、通訊協定</span><span class="sxs-lookup"><span data-stu-id="1684f-164">A five tuple affinity: Source IP, Source Port, Destination IP, Destination Port, Protocol</span></span> 

<span data-ttu-id="1684f-165">預設值為 [無]。</span><span class="sxs-lookup"><span data-stu-id="1684f-165">The default value is none.</span></span>

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

### <span data-ttu-id="1684f-166">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="1684f-166">-LocalPort</span></span>
<span data-ttu-id="1684f-167">指定此端點所使用的本機、私人埠。</span><span class="sxs-lookup"><span data-stu-id="1684f-167">Specifies the local, private, port that this endpoint uses.</span></span>
<span data-ttu-id="1684f-168">虛擬機器中的應用程式在此埠上偵聽此端點的服務輸入要求。</span><span class="sxs-lookup"><span data-stu-id="1684f-168">Applications within the virtual machine listen on this port for service input requests for this endpoint.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1684f-169">-名稱</span><span class="sxs-lookup"><span data-stu-id="1684f-169">-Name</span></span>
<span data-ttu-id="1684f-170">指定端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="1684f-170">Specifies a name for the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1684f-171">-NoProbe</span><span class="sxs-lookup"><span data-stu-id="1684f-171">-NoProbe</span></span>
<span data-ttu-id="1684f-172">表示此 Cmdlet 使用 [沒有探測] 設定。</span><span class="sxs-lookup"><span data-stu-id="1684f-172">Indicates that this cmdlet uses the no probe setting.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LBNoProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1684f-173">-ProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="1684f-173">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="1684f-174">指定端點的探測巡迴檢測間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="1684f-174">Specifies the probe polling interval, in seconds, for the endpoint.</span></span>

```yaml
Type: Int32
Parameter Sets: LBCustomProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1684f-175">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="1684f-175">-ProbePath</span></span>
<span data-ttu-id="1684f-176">指定 HTTP 探測的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="1684f-176">Specifies the relative path to the HTTP probe.</span></span>

```yaml
Type: String
Parameter Sets: LBCustomProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1684f-177">-ProbePort</span><span class="sxs-lookup"><span data-stu-id="1684f-177">-ProbePort</span></span>
<span data-ttu-id="1684f-178">指定端點使用的埠。</span><span class="sxs-lookup"><span data-stu-id="1684f-178">Specifies the port that the endpoint uses.</span></span>

```yaml
Type: Int32
Parameter Sets: LBCustomProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1684f-179">-ProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="1684f-179">-ProbeProtocol</span></span>
<span data-ttu-id="1684f-180">指定埠通訊協定。</span><span class="sxs-lookup"><span data-stu-id="1684f-180">Specifies the port protocol.</span></span>
<span data-ttu-id="1684f-181">有效值為：</span><span class="sxs-lookup"><span data-stu-id="1684f-181">Valid values are:</span></span> 

- <span data-ttu-id="1684f-182">tcp-out</span><span class="sxs-lookup"><span data-stu-id="1684f-182">tcp</span></span> 
- <span data-ttu-id="1684f-183">HTTP</span><span class="sxs-lookup"><span data-stu-id="1684f-183">http</span></span>

```yaml
Type: String
Parameter Sets: LBCustomProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1684f-184">-ProbeTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="1684f-184">-ProbeTimeoutInSeconds</span></span>
<span data-ttu-id="1684f-185">指定探測巡迴檢測超時期間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="1684f-185">Specifies the probe polling time-out period in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: LBCustomProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1684f-186">-設定檔</span><span class="sxs-lookup"><span data-stu-id="1684f-186">-Profile</span></span>
<span data-ttu-id="1684f-187">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="1684f-187">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1684f-188">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="1684f-188">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1684f-189">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="1684f-189">-Protocol</span></span>
<span data-ttu-id="1684f-190">指定端點的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="1684f-190">Specifies the protocol of the endpoint.</span></span>
<span data-ttu-id="1684f-191">有效值為：</span><span class="sxs-lookup"><span data-stu-id="1684f-191">Valid values are:</span></span> 

- <span data-ttu-id="1684f-192">tcp-out</span><span class="sxs-lookup"><span data-stu-id="1684f-192">tcp</span></span> 
- <span data-ttu-id="1684f-193">udp-in</span><span class="sxs-lookup"><span data-stu-id="1684f-193">udp</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1684f-194">-PublicPort</span><span class="sxs-lookup"><span data-stu-id="1684f-194">-PublicPort</span></span>
<span data-ttu-id="1684f-195">指定端點使用的公用埠。</span><span class="sxs-lookup"><span data-stu-id="1684f-195">Specifies the public port that the endpoint uses.</span></span>
<span data-ttu-id="1684f-196">如果您沒有指定值，Azure 會指派可用的埠。</span><span class="sxs-lookup"><span data-stu-id="1684f-196">If you do not specify a value, Azure assigns an available port.</span></span>

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

### <span data-ttu-id="1684f-197">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="1684f-197">-VirtualIPName</span></span>
<span data-ttu-id="1684f-198">指定 Azure 與端點相關聯之虛擬 IP 位址的名稱。</span><span class="sxs-lookup"><span data-stu-id="1684f-198">Specifies the name of a virtual IP address that Azure associates to the endpoint.</span></span>
<span data-ttu-id="1684f-199">您的服務可以有多個虛擬 Ip。</span><span class="sxs-lookup"><span data-stu-id="1684f-199">Your service can have multiple virtual IPs.</span></span>
<span data-ttu-id="1684f-200">若要建立虛擬 Ip，請使用 **AzureVirtualIP** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1684f-200">To create virtual IPs, use the **Add-AzureVirtualIP** cmdlet.</span></span>

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

### <span data-ttu-id="1684f-201">-VM</span><span class="sxs-lookup"><span data-stu-id="1684f-201">-VM</span></span>
<span data-ttu-id="1684f-202">指定端點所屬的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="1684f-202">Specifies the virtual machine to which the endpoint belongs.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1684f-203">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1684f-203">CommonParameters</span></span>
<span data-ttu-id="1684f-204">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1684f-204">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1684f-205">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1684f-205">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1684f-206">輸入</span><span class="sxs-lookup"><span data-stu-id="1684f-206">INPUTS</span></span>

## <span data-ttu-id="1684f-207">輸出</span><span class="sxs-lookup"><span data-stu-id="1684f-207">OUTPUTS</span></span>

### <span data-ttu-id="1684f-208">System.object</span><span class="sxs-lookup"><span data-stu-id="1684f-208">System.Object</span></span>

## <span data-ttu-id="1684f-209">筆記</span><span class="sxs-lookup"><span data-stu-id="1684f-209">NOTES</span></span>

## <span data-ttu-id="1684f-210">相關連結</span><span class="sxs-lookup"><span data-stu-id="1684f-210">RELATED LINKS</span></span>

[<span data-ttu-id="1684f-211">附加 AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="1684f-211">Add-AzureVirtualIP</span></span>](./Add-AzureVirtualIP.md)

[<span data-ttu-id="1684f-212">AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="1684f-212">Get-AzureEndpoint</span></span>](./Get-AzureEndpoint.md)

[<span data-ttu-id="1684f-213">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="1684f-213">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="1684f-214">移除-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="1684f-214">Remove-AzureEndpoint</span></span>](./Remove-AzureEndpoint.md)

[<span data-ttu-id="1684f-215">Set-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="1684f-215">Set-AzureEndpoint</span></span>](./Set-AzureEndpoint.md)

[<span data-ttu-id="1684f-216">更新-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="1684f-216">Update-AzureVM</span></span>](./Update-AzureVM.md)


