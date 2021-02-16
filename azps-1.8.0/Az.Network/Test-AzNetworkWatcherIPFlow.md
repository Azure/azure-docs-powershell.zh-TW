---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-aznetworkwatcheripflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
ms.openlocfilehash: b3a58652a619552187ac8e52760393589e937e78
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402689"
---
# <span data-ttu-id="47218-101">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="47218-101">Test-AzNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="47218-102">簡介</span><span class="sxs-lookup"><span data-stu-id="47218-102">SYNOPSIS</span></span>
<span data-ttu-id="47218-103">會返回封包是否允許或拒絕來自特定目的地。</span><span class="sxs-lookup"><span data-stu-id="47218-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

## <span data-ttu-id="47218-104">語法</span><span class="sxs-lookup"><span data-stu-id="47218-104">SYNTAX</span></span>

### <span data-ttu-id="47218-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="47218-105">SetByResource (Default)</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47218-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="47218-106">SetByName</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47218-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="47218-107">SetByLocation</span></span>
```
Test-AzNetworkWatcherIPFlow -Location <String> -TargetVirtualMachineId <String> -Direction <String>
 -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47218-108">描述</span><span class="sxs-lookup"><span data-stu-id="47218-108">DESCRIPTION</span></span>
<span data-ttu-id="47218-109">Cmdlet Test-AzNetworkWatcherIPFlow的 Cmdlet，針對指定的 VM 資源，以及使用本地和遠端 IP 位址和埠指定方向的封包，會針對封包是允許還是拒絕，會返回。</span><span class="sxs-lookup"><span data-stu-id="47218-109">The Test-AzNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="47218-110">例子</span><span class="sxs-lookup"><span data-stu-id="47218-110">EXAMPLES</span></span>

### <span data-ttu-id="47218-111">範例 1：執行Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="47218-111">Example 1: Run Test-AzNetworkWatcherIPFlow</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}

Test-AzNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="47218-112">取得此訂閱美國中西部的網路監視程式，然後取得 VM 及其相關聯的網路介面。</span><span class="sxs-lookup"><span data-stu-id="47218-112">Get's the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="47218-113">然後針對第一個網路介面，Test-AzNetworkWatcherIPFlow使用第一個網路介面的第一個 IP 執行，以在網際網路上連出 IP。</span><span class="sxs-lookup"><span data-stu-id="47218-113">Then for the first Network Interface, runs Test-AzNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="47218-114">參數</span><span class="sxs-lookup"><span data-stu-id="47218-114">PARAMETERS</span></span>

### <span data-ttu-id="47218-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47218-115">-AsJob</span></span>
<span data-ttu-id="47218-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="47218-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47218-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47218-117">-DefaultProfile</span></span>
<span data-ttu-id="47218-118">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="47218-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47218-119">-方向</span><span class="sxs-lookup"><span data-stu-id="47218-119">-Direction</span></span>
<span data-ttu-id="47218-120">方向。</span><span class="sxs-lookup"><span data-stu-id="47218-120">Direction.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Inbound, Outbound

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47218-121">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="47218-121">-LocalIPAddress</span></span>
<span data-ttu-id="47218-122">本地 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="47218-122">Local IP Address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47218-123">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="47218-123">-LocalPort</span></span>
<span data-ttu-id="47218-124">本地埠。</span><span class="sxs-lookup"><span data-stu-id="47218-124">Local Port.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47218-125">-位置</span><span class="sxs-lookup"><span data-stu-id="47218-125">-Location</span></span>
<span data-ttu-id="47218-126">網路監視者的位置。</span><span class="sxs-lookup"><span data-stu-id="47218-126">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47218-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="47218-127">-NetworkWatcher</span></span>
<span data-ttu-id="47218-128">網路監視程式資源。</span><span class="sxs-lookup"><span data-stu-id="47218-128">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47218-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="47218-129">-NetworkWatcherName</span></span>
<span data-ttu-id="47218-130">網路監視者的名稱。</span><span class="sxs-lookup"><span data-stu-id="47218-130">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47218-131">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="47218-131">-Protocol</span></span>
<span data-ttu-id="47218-132">協定。</span><span class="sxs-lookup"><span data-stu-id="47218-132">Protocol.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: TCP, UDP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47218-133">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="47218-133">-RemoteIPAddress</span></span>
<span data-ttu-id="47218-134">遠端 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="47218-134">Remote IP Address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47218-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="47218-135">-RemotePort</span></span>
<span data-ttu-id="47218-136">遠端埠。</span><span class="sxs-lookup"><span data-stu-id="47218-136">Remote port.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47218-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47218-137">-ResourceGroupName</span></span>
<span data-ttu-id="47218-138">網路監視者資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="47218-138">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47218-139">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="47218-139">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="47218-140">目標網路介面識別碼。</span><span class="sxs-lookup"><span data-stu-id="47218-140">Target network interface Id.</span></span>

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

### <span data-ttu-id="47218-141">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="47218-141">-TargetVirtualMachineId</span></span>
<span data-ttu-id="47218-142">目標虛擬機器識別碼。</span><span class="sxs-lookup"><span data-stu-id="47218-142">The target virtual machine ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47218-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47218-143">CommonParameters</span></span>
<span data-ttu-id="47218-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="47218-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47218-145">詳細資訊請參閱 https://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="47218-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47218-146">輸入</span><span class="sxs-lookup"><span data-stu-id="47218-146">INPUTS</span></span>

### <span data-ttu-id="47218-147">Microsoft.Azure.Commands.Network.models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="47218-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="47218-148">System.String</span><span class="sxs-lookup"><span data-stu-id="47218-148">System.String</span></span>

## <span data-ttu-id="47218-149">輸出</span><span class="sxs-lookup"><span data-stu-id="47218-149">OUTPUTS</span></span>

### <span data-ttu-id="47218-150">Microsoft.Azure.Commands.Network.models.PSIPFlowVerifyResult</span><span class="sxs-lookup"><span data-stu-id="47218-150">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="47218-151">筆記</span><span class="sxs-lookup"><span data-stu-id="47218-151">NOTES</span></span>
<span data-ttu-id="47218-152">關鍵字：azure、azurerm、arm、resource、management、manager、network、network、network watcher、flow、ip</span><span class="sxs-lookup"><span data-stu-id="47218-152">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="47218-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="47218-153">RELATED LINKS</span></span>

[<span data-ttu-id="47218-154">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="47218-154">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="47218-155">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="47218-155">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="47218-156">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="47218-156">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="47218-157">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="47218-157">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="47218-158">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="47218-158">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="47218-159">Get-AzNetworkWatcherTopwork</span><span class="sxs-lookup"><span data-stu-id="47218-159">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="47218-160">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="47218-160">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="47218-161">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="47218-161">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="47218-162">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="47218-162">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="47218-163">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="47218-163">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="47218-164">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="47218-164">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="47218-165">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="47218-165">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="47218-166">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="47218-166">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="47218-167">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="47218-167">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="47218-168">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="47218-168">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="47218-169">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="47218-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="47218-170">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="47218-170">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="47218-171">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="47218-171">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="47218-172">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="47218-172">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="47218-173">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="47218-173">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="47218-174">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="47218-174">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="47218-175">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="47218-175">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="47218-176">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="47218-176">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="47218-177">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="47218-177">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="47218-178">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="47218-178">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="47218-179">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="47218-179">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="47218-180">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="47218-180">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
