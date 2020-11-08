---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-aznetworkwatcheripflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
ms.openlocfilehash: 75b8d976dc4c7be0544f2445ef991723c692edbf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127451"
---
# <span data-ttu-id="e020b-101">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="e020b-101">Test-AzNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="e020b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e020b-102">SYNOPSIS</span></span>
<span data-ttu-id="e020b-103">傳回是否允許或拒絕來自特定目的地的資料包。</span><span class="sxs-lookup"><span data-stu-id="e020b-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

## <span data-ttu-id="e020b-104">句法</span><span class="sxs-lookup"><span data-stu-id="e020b-104">SYNTAX</span></span>

### <span data-ttu-id="e020b-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="e020b-105">SetByResource (Default)</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e020b-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="e020b-106">SetByName</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e020b-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="e020b-107">SetByLocation</span></span>
```
Test-AzNetworkWatcherIPFlow -Location <String> -TargetVirtualMachineId <String> -Direction <String>
 -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e020b-108">說明</span><span class="sxs-lookup"><span data-stu-id="e020b-108">DESCRIPTION</span></span>
<span data-ttu-id="e020b-109">針對特定 VM 資源的 Test-AzNetworkWatcherIPFlow Cmdlet，以及使用本機和遠端、IP 位址和埠的指定方向的資料包，會傳回是否允許或拒絕該資料包。</span><span class="sxs-lookup"><span data-stu-id="e020b-109">The Test-AzNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="e020b-110">示例</span><span class="sxs-lookup"><span data-stu-id="e020b-110">EXAMPLES</span></span>

### <span data-ttu-id="e020b-111">範例1：執行 Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="e020b-111">Example 1: Run Test-AzNetworkWatcherIPFlow</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzNetworkInterface | Where-Object { $vm.NetworkProfile.NetworkInterfaces.Id -contains $_.Id }

Test-AzNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="e020b-112">取得此訂閱之西部中心的網路觀察程式，然後取得 VM 及其相關的網路介面。</span><span class="sxs-lookup"><span data-stu-id="e020b-112">Gets the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="e020b-113">接著，在第一個網路介面上執行 Test-AzNetworkWatcherIPFlow 使用第一個網路介面的第一個 IP，以取得網際網路上 IP 的輸出連線。</span><span class="sxs-lookup"><span data-stu-id="e020b-113">Then for the first Network Interface, runs Test-AzNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="e020b-114">參數</span><span class="sxs-lookup"><span data-stu-id="e020b-114">PARAMETERS</span></span>

### <span data-ttu-id="e020b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e020b-115">-AsJob</span></span>
<span data-ttu-id="e020b-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e020b-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e020b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e020b-117">-DefaultProfile</span></span>
<span data-ttu-id="e020b-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e020b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e020b-119">方向</span><span class="sxs-lookup"><span data-stu-id="e020b-119">-Direction</span></span>
<span data-ttu-id="e020b-120">發展.</span><span class="sxs-lookup"><span data-stu-id="e020b-120">Direction.</span></span>

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

### <span data-ttu-id="e020b-121">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="e020b-121">-LocalIPAddress</span></span>
<span data-ttu-id="e020b-122">[本機 IP 位址]。</span><span class="sxs-lookup"><span data-stu-id="e020b-122">Local IP Address.</span></span>

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

### <span data-ttu-id="e020b-123">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="e020b-123">-LocalPort</span></span>
<span data-ttu-id="e020b-124">本機埠。</span><span class="sxs-lookup"><span data-stu-id="e020b-124">Local Port.</span></span>

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

### <span data-ttu-id="e020b-125">-位置</span><span class="sxs-lookup"><span data-stu-id="e020b-125">-Location</span></span>
<span data-ttu-id="e020b-126">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="e020b-126">Location of the network watcher.</span></span>

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

### <span data-ttu-id="e020b-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e020b-127">-NetworkWatcher</span></span>
<span data-ttu-id="e020b-128">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="e020b-128">The network watcher resource.</span></span>

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

### <span data-ttu-id="e020b-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="e020b-129">-NetworkWatcherName</span></span>
<span data-ttu-id="e020b-130">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="e020b-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="e020b-131">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="e020b-131">-Protocol</span></span>
<span data-ttu-id="e020b-132">通訊協定.</span><span class="sxs-lookup"><span data-stu-id="e020b-132">Protocol.</span></span>

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

### <span data-ttu-id="e020b-133">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="e020b-133">-RemoteIPAddress</span></span>
<span data-ttu-id="e020b-134">[遠端 IP 位址]。</span><span class="sxs-lookup"><span data-stu-id="e020b-134">Remote IP Address.</span></span>

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

### <span data-ttu-id="e020b-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="e020b-135">-RemotePort</span></span>
<span data-ttu-id="e020b-136">遠端埠。</span><span class="sxs-lookup"><span data-stu-id="e020b-136">Remote port.</span></span>

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

### <span data-ttu-id="e020b-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e020b-137">-ResourceGroupName</span></span>
<span data-ttu-id="e020b-138">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e020b-138">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="e020b-139">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="e020b-139">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="e020b-140">目標網路介面 Id。</span><span class="sxs-lookup"><span data-stu-id="e020b-140">Target network interface Id.</span></span>

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

### <span data-ttu-id="e020b-141">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="e020b-141">-TargetVirtualMachineId</span></span>
<span data-ttu-id="e020b-142">目標虛擬機器 ID。</span><span class="sxs-lookup"><span data-stu-id="e020b-142">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="e020b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e020b-143">CommonParameters</span></span>
<span data-ttu-id="e020b-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e020b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e020b-145">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e020b-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e020b-146">輸入</span><span class="sxs-lookup"><span data-stu-id="e020b-146">INPUTS</span></span>

### <span data-ttu-id="e020b-147">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e020b-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="e020b-148">System.object</span><span class="sxs-lookup"><span data-stu-id="e020b-148">System.String</span></span>

## <span data-ttu-id="e020b-149">輸出</span><span class="sxs-lookup"><span data-stu-id="e020b-149">OUTPUTS</span></span>

### <span data-ttu-id="e020b-150">PSIPFlowVerifyResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e020b-150">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="e020b-151">筆記</span><span class="sxs-lookup"><span data-stu-id="e020b-151">NOTES</span></span>
<span data-ttu-id="e020b-152">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，流程，ip</span><span class="sxs-lookup"><span data-stu-id="e020b-152">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="e020b-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="e020b-153">RELATED LINKS</span></span>

[<span data-ttu-id="e020b-154">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e020b-154">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="e020b-155">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e020b-155">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="e020b-156">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e020b-156">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="e020b-157">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="e020b-157">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="e020b-158">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="e020b-158">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="e020b-159">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="e020b-159">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="e020b-160">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="e020b-160">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="e020b-161">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e020b-161">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e020b-162">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="e020b-162">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="e020b-163">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e020b-163">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e020b-164">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e020b-164">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e020b-165">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e020b-165">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e020b-166">新-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="e020b-166">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="e020b-167">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="e020b-167">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="e020b-168">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="e020b-168">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="e020b-169">停止 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e020b-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e020b-170">開始-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e020b-170">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e020b-171">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e020b-171">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e020b-172">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="e020b-172">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="e020b-173">移除-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e020b-173">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e020b-174">新-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e020b-174">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e020b-175">AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="e020b-175">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="e020b-176">AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="e020b-176">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="e020b-177">AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="e020b-177">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="e020b-178">AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="e020b-178">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="e020b-179">AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="e020b-179">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="e020b-180">AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e020b-180">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)