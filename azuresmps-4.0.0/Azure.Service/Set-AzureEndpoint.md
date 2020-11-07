---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1BA472FB-E684-486C-8066-42C9215DBDEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 83d1afcae66af7e4548b1dbd4031392969f4d267
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967503"
---
# <span data-ttu-id="545bf-101">Set-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="545bf-101">Set-AzureEndpoint</span></span>

## <span data-ttu-id="545bf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="545bf-102">SYNOPSIS</span></span>
<span data-ttu-id="545bf-103">修改指派給虛擬機器的端點。</span><span class="sxs-lookup"><span data-stu-id="545bf-103">Modifies an endpoint assigned to a virtual machine.</span></span>

## <span data-ttu-id="545bf-104">句法</span><span class="sxs-lookup"><span data-stu-id="545bf-104">SYNTAX</span></span>

```
Set-AzureEndpoint [-Name] <String> [[-Protocol] <String>] [[-LocalPort] <Int32>] [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-InternalLoadBalancerName <String>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>] [-VirtualIPName <String>]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="545bf-105">說明</span><span class="sxs-lookup"><span data-stu-id="545bf-105">DESCRIPTION</span></span>
<span data-ttu-id="545bf-106">**AzureEndpoint** Cmdlet 會修改指派給 Azure 虛擬機器的端點。</span><span class="sxs-lookup"><span data-stu-id="545bf-106">The **Set-AzureEndpoint** cmdlet modifies an endpoint assigned to an Azure virtual machine.</span></span>
<span data-ttu-id="545bf-107">您可以指定對未進行負載平衡的端點所做的變更。</span><span class="sxs-lookup"><span data-stu-id="545bf-107">You can specify changes to an endpoint that is not load balanced.</span></span>

## <span data-ttu-id="545bf-108">示例</span><span class="sxs-lookup"><span data-stu-id="545bf-108">EXAMPLES</span></span>

### <span data-ttu-id="545bf-109">範例1：修改端點以偵聽埠</span><span class="sxs-lookup"><span data-stu-id="545bf-109">Example 1: Modify an endpoint to listen on a port</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirutalMachine01" | Set-AzureEndpoint -Name "Web" -PublicPort 443 -LocalPort 443 -Protocol tcp | Update-AzureVM
```

<span data-ttu-id="545bf-110">這個命令會使用 **add-azurevm** Cmdlet 來檢索名為 VirtualMachine01 的虛擬機器的設定。</span><span class="sxs-lookup"><span data-stu-id="545bf-110">This command retrieves the configuration of a virtual machine named VirtualMachine01 by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="545bf-111">命令會使用管線運算子將它傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="545bf-111">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="545bf-112">這個 Cmdlet 會修改名為 [Web] 的端點，以在埠443上聆聽。</span><span class="sxs-lookup"><span data-stu-id="545bf-112">This cmdlet modifies the endpoint named Web to listen on port 443.</span></span>
<span data-ttu-id="545bf-113">該命令會將虛擬機器物件傳遞到會實現變更的 **add-azurevm** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="545bf-113">The command passes the virtual machine object to the **Update-AzureVM** cmdlet, which implements your changes.</span></span>

## <span data-ttu-id="545bf-114">參數</span><span class="sxs-lookup"><span data-stu-id="545bf-114">PARAMETERS</span></span>

### <span data-ttu-id="545bf-115">-ACL</span><span class="sxs-lookup"><span data-stu-id="545bf-115">-ACL</span></span>
<span data-ttu-id="545bf-116">指定 (ACL) 設定物件的存取控制清單，此 Cmdlet 會套用到端點。</span><span class="sxs-lookup"><span data-stu-id="545bf-116">Specifies an access control list (ACL) configuration object that this cmdlet applies to the endpoint.</span></span>

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

### <span data-ttu-id="545bf-117">-DirectServerReturn</span><span class="sxs-lookup"><span data-stu-id="545bf-117">-DirectServerReturn</span></span>
<span data-ttu-id="545bf-118">指定此 Cmdlet 是否允許直接返回伺服器。</span><span class="sxs-lookup"><span data-stu-id="545bf-118">Specifies whether this cmdlet enables direct server return.</span></span>
<span data-ttu-id="545bf-119">指定要啟用 $True，或 $False 以停用。</span><span class="sxs-lookup"><span data-stu-id="545bf-119">Specify $True to enable, or $False to disable.</span></span>

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

### <span data-ttu-id="545bf-120">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="545bf-120">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="545bf-121">指定端點的 TCP 空閒超時期間（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="545bf-121">Specifies the TCP idle time-out period, in minutes, for the endpoint.</span></span>

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

### <span data-ttu-id="545bf-122">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="545bf-122">-InformationAction</span></span>
<span data-ttu-id="545bf-123">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="545bf-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="545bf-124">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="545bf-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="545bf-125">持續</span><span class="sxs-lookup"><span data-stu-id="545bf-125">Continue</span></span>
- <span data-ttu-id="545bf-126">理會</span><span class="sxs-lookup"><span data-stu-id="545bf-126">Ignore</span></span>
- <span data-ttu-id="545bf-127">看</span><span class="sxs-lookup"><span data-stu-id="545bf-127">Inquire</span></span>
- <span data-ttu-id="545bf-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="545bf-128">SilentlyContinue</span></span>
- <span data-ttu-id="545bf-129">停止</span><span class="sxs-lookup"><span data-stu-id="545bf-129">Stop</span></span>
- <span data-ttu-id="545bf-130">封存</span><span class="sxs-lookup"><span data-stu-id="545bf-130">Suspend</span></span>

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

### <span data-ttu-id="545bf-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="545bf-131">-InformationVariable</span></span>
<span data-ttu-id="545bf-132">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="545bf-132">Specifies an information variable.</span></span>

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

### <span data-ttu-id="545bf-133">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="545bf-133">-InternalLoadBalancerName</span></span>
<span data-ttu-id="545bf-134">指定內部負載平衡器的名稱。</span><span class="sxs-lookup"><span data-stu-id="545bf-134">Specifies the name of the internal load balancer.</span></span>

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

### <span data-ttu-id="545bf-135">-LoadBalancerDistribution</span><span class="sxs-lookup"><span data-stu-id="545bf-135">-LoadBalancerDistribution</span></span>
<span data-ttu-id="545bf-136">指定負載平衡器分配演算法。</span><span class="sxs-lookup"><span data-stu-id="545bf-136">Specifies the load balancer distribution algorithm.</span></span>
<span data-ttu-id="545bf-137">有效值為：</span><span class="sxs-lookup"><span data-stu-id="545bf-137">Valid values are:</span></span> 

- <span data-ttu-id="545bf-138">sourceIP.</span><span class="sxs-lookup"><span data-stu-id="545bf-138">sourceIP.</span></span>
<span data-ttu-id="545bf-139">兩個元組關聯：來源 IP、目的地 IP</span><span class="sxs-lookup"><span data-stu-id="545bf-139">A two tuple affinity: Source IP, Destination IP</span></span> 
- <span data-ttu-id="545bf-140">sourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="545bf-140">sourceIPProtocol.</span></span>
<span data-ttu-id="545bf-141">三個元組關聯：來源 IP、目的地 IP、通訊協定</span><span class="sxs-lookup"><span data-stu-id="545bf-141">A three tuple affinity: Source IP, Destination IP, Protocol</span></span> 
- <span data-ttu-id="545bf-142">所有.</span><span class="sxs-lookup"><span data-stu-id="545bf-142">none.</span></span>
<span data-ttu-id="545bf-143">五個元組關聯：來源 IP、來源埠、目的地 IP、目的地埠、通訊協定</span><span class="sxs-lookup"><span data-stu-id="545bf-143">A five tuple affinity: Source IP, Source Port, Destination IP, Destination Port, Protocol</span></span> 

<span data-ttu-id="545bf-144">預設值為 [無]。</span><span class="sxs-lookup"><span data-stu-id="545bf-144">The default value is none.</span></span>

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

### <span data-ttu-id="545bf-145">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="545bf-145">-LocalPort</span></span>
<span data-ttu-id="545bf-146">指定此端點所使用的本機、私人埠。</span><span class="sxs-lookup"><span data-stu-id="545bf-146">Specifies the local, private, port that this endpoint uses.</span></span>
<span data-ttu-id="545bf-147">虛擬機器中的應用程式在此埠上偵聽此端點的服務輸入要求。</span><span class="sxs-lookup"><span data-stu-id="545bf-147">Applications within the virtual machine listen on this port for service input requests for this endpoint.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="545bf-148">-名稱</span><span class="sxs-lookup"><span data-stu-id="545bf-148">-Name</span></span>
<span data-ttu-id="545bf-149">指定端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="545bf-149">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="545bf-150">-設定檔</span><span class="sxs-lookup"><span data-stu-id="545bf-150">-Profile</span></span>
<span data-ttu-id="545bf-151">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="545bf-151">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="545bf-152">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="545bf-152">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="545bf-153">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="545bf-153">-Protocol</span></span>
<span data-ttu-id="545bf-154">指定端點的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="545bf-154">Specifies the protocol of the endpoint.</span></span>
<span data-ttu-id="545bf-155">有效值為：</span><span class="sxs-lookup"><span data-stu-id="545bf-155">Valid values are:</span></span> 

- <span data-ttu-id="545bf-156">tcp-out</span><span class="sxs-lookup"><span data-stu-id="545bf-156">tcp</span></span> 
- <span data-ttu-id="545bf-157">udp-in</span><span class="sxs-lookup"><span data-stu-id="545bf-157">udp</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="545bf-158">-PublicPort</span><span class="sxs-lookup"><span data-stu-id="545bf-158">-PublicPort</span></span>
<span data-ttu-id="545bf-159">指定端點使用的公用埠。</span><span class="sxs-lookup"><span data-stu-id="545bf-159">Specifies the public port that the endpoint uses.</span></span>

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

### <span data-ttu-id="545bf-160">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="545bf-160">-VirtualIPName</span></span>
<span data-ttu-id="545bf-161">指定 Azure 與端點相關聯之虛擬 IP 位址的名稱。</span><span class="sxs-lookup"><span data-stu-id="545bf-161">Specifies the name of a virtual IP address that Azure associates to the endpoint.</span></span>
<span data-ttu-id="545bf-162">您的服務可以有多個虛擬 Ip。</span><span class="sxs-lookup"><span data-stu-id="545bf-162">Your service can have multiple virtual IPs.</span></span>
<span data-ttu-id="545bf-163">若要建立虛擬 Ip，請使用 **AzureVirtualIP** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="545bf-163">To create virtual IPs, use the **Add-AzureVirtualIP** cmdlet.</span></span>

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

### <span data-ttu-id="545bf-164">-VM</span><span class="sxs-lookup"><span data-stu-id="545bf-164">-VM</span></span>
<span data-ttu-id="545bf-165">指定端點所屬的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="545bf-165">Specifies the virtual machine to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="545bf-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="545bf-166">CommonParameters</span></span>
<span data-ttu-id="545bf-167">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="545bf-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="545bf-168">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="545bf-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="545bf-169">輸入</span><span class="sxs-lookup"><span data-stu-id="545bf-169">INPUTS</span></span>

## <span data-ttu-id="545bf-170">輸出</span><span class="sxs-lookup"><span data-stu-id="545bf-170">OUTPUTS</span></span>

### <span data-ttu-id="545bf-171">System.object</span><span class="sxs-lookup"><span data-stu-id="545bf-171">System.Object</span></span>

## <span data-ttu-id="545bf-172">筆記</span><span class="sxs-lookup"><span data-stu-id="545bf-172">NOTES</span></span>

## <span data-ttu-id="545bf-173">相關連結</span><span class="sxs-lookup"><span data-stu-id="545bf-173">RELATED LINKS</span></span>

[<span data-ttu-id="545bf-174">附加 AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="545bf-174">Add-AzureEndpoint</span></span>](./Add-AzureEndpoint.md)

[<span data-ttu-id="545bf-175">附加 AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="545bf-175">Add-AzureVirtualIP</span></span>](./Add-AzureVirtualIP.md)

[<span data-ttu-id="545bf-176">AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="545bf-176">Get-AzureEndpoint</span></span>](./Get-AzureEndpoint.md)

[<span data-ttu-id="545bf-177">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="545bf-177">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="545bf-178">移除-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="545bf-178">Remove-AzureEndpoint</span></span>](./Remove-AzureEndpoint.md)

[<span data-ttu-id="545bf-179">更新-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="545bf-179">Update-AzureVM</span></span>](./Update-AzureVM.md)


