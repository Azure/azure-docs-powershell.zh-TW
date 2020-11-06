---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/test-azurermnetworkwatcheripflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherIPFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherIPFlow.md
ms.openlocfilehash: 6fc406d0af3ed451fbbf2f14c9ca8943256df744
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456940"
---
# <span data-ttu-id="42870-101">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="42870-101">Test-AzureRmNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="42870-102">摘要</span><span class="sxs-lookup"><span data-stu-id="42870-102">SYNOPSIS</span></span>
<span data-ttu-id="42870-103">傳回是否允許或拒絕來自特定目的地的資料包。</span><span class="sxs-lookup"><span data-stu-id="42870-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42870-104">句法</span><span class="sxs-lookup"><span data-stu-id="42870-104">SYNTAX</span></span>

### <span data-ttu-id="42870-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="42870-105">SetByResource (Default)</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42870-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="42870-106">SetByName</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42870-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="42870-107">SetByLocation</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -Location <String> -TargetVirtualMachineId <String> -Direction <String>
 -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42870-108">說明</span><span class="sxs-lookup"><span data-stu-id="42870-108">DESCRIPTION</span></span>
<span data-ttu-id="42870-109">針對特定 VM 資源的 Test-AzureRmNetworkWatcherIPFlow Cmdlet，以及使用本機和遠端、IP 位址和埠的指定方向的資料包，會傳回是否允許或拒絕該資料包。</span><span class="sxs-lookup"><span data-stu-id="42870-109">The Test-AzureRmNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="42870-110">示例</span><span class="sxs-lookup"><span data-stu-id="42870-110">EXAMPLES</span></span>

### <span data-ttu-id="42870-111">範例1：執行 Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="42870-111">Example 1: Run Test-AzureRmNetworkWatcherIPFlow</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzureRmNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}

Test-AzureRmNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="42870-112">取得此訂閱之西部中心的網路觀察程式，然後取得 VM 及其相關的網路介面。</span><span class="sxs-lookup"><span data-stu-id="42870-112">Get's the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="42870-113">接著，在第一個網路介面上執行 Test-AzureRmNetworkWatcherIPFlow 使用第一個網路介面的第一個 IP，以取得網際網路上 IP 的輸出連線。</span><span class="sxs-lookup"><span data-stu-id="42870-113">Then for the first Network Interface, runs Test-AzureRmNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="42870-114">參數</span><span class="sxs-lookup"><span data-stu-id="42870-114">PARAMETERS</span></span>

### <span data-ttu-id="42870-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="42870-115">-AsJob</span></span>
<span data-ttu-id="42870-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="42870-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="42870-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42870-117">-DefaultProfile</span></span>
<span data-ttu-id="42870-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="42870-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42870-119">方向</span><span class="sxs-lookup"><span data-stu-id="42870-119">-Direction</span></span>
<span data-ttu-id="42870-120">發展.</span><span class="sxs-lookup"><span data-stu-id="42870-120">Direction.</span></span>

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

### <span data-ttu-id="42870-121">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="42870-121">-LocalIPAddress</span></span>
<span data-ttu-id="42870-122">[本機 IP 位址]。</span><span class="sxs-lookup"><span data-stu-id="42870-122">Local IP Address.</span></span>

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

### <span data-ttu-id="42870-123">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="42870-123">-LocalPort</span></span>
<span data-ttu-id="42870-124">本機埠。</span><span class="sxs-lookup"><span data-stu-id="42870-124">Local Port.</span></span>

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

### <span data-ttu-id="42870-125">-位置</span><span class="sxs-lookup"><span data-stu-id="42870-125">-Location</span></span>
<span data-ttu-id="42870-126">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="42870-126">Location of the network watcher.</span></span>

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

### <span data-ttu-id="42870-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="42870-127">-NetworkWatcher</span></span>
<span data-ttu-id="42870-128">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="42870-128">The network watcher resource.</span></span>

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

### <span data-ttu-id="42870-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="42870-129">-NetworkWatcherName</span></span>
<span data-ttu-id="42870-130">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="42870-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="42870-131">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="42870-131">-Protocol</span></span>
<span data-ttu-id="42870-132">通訊協定.</span><span class="sxs-lookup"><span data-stu-id="42870-132">Protocol.</span></span>

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

### <span data-ttu-id="42870-133">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="42870-133">-RemoteIPAddress</span></span>
<span data-ttu-id="42870-134">[遠端 IP 位址]。</span><span class="sxs-lookup"><span data-stu-id="42870-134">Remote IP Address.</span></span>

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

### <span data-ttu-id="42870-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="42870-135">-RemotePort</span></span>
<span data-ttu-id="42870-136">遠端埠。</span><span class="sxs-lookup"><span data-stu-id="42870-136">Remote port.</span></span>

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

### <span data-ttu-id="42870-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42870-137">-ResourceGroupName</span></span>
<span data-ttu-id="42870-138">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="42870-138">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="42870-139">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="42870-139">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="42870-140">目標網路介面 Id。</span><span class="sxs-lookup"><span data-stu-id="42870-140">Target network interface Id.</span></span>

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

### <span data-ttu-id="42870-141">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="42870-141">-TargetVirtualMachineId</span></span>
<span data-ttu-id="42870-142">目標虛擬機器 ID。</span><span class="sxs-lookup"><span data-stu-id="42870-142">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="42870-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42870-143">CommonParameters</span></span>
<span data-ttu-id="42870-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="42870-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42870-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="42870-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42870-146">輸入</span><span class="sxs-lookup"><span data-stu-id="42870-146">INPUTS</span></span>

### <span data-ttu-id="42870-147">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="42870-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="42870-148">參數： NetworkWatcher (ByValue) </span><span class="sxs-lookup"><span data-stu-id="42870-148">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="42870-149">System.object</span><span class="sxs-lookup"><span data-stu-id="42870-149">System.String</span></span>
<span data-ttu-id="42870-150">參數： NetworkWatcherName (ByValue) </span><span class="sxs-lookup"><span data-stu-id="42870-150">Parameters: NetworkWatcherName (ByValue)</span></span>

## <span data-ttu-id="42870-151">輸出</span><span class="sxs-lookup"><span data-stu-id="42870-151">OUTPUTS</span></span>

### <span data-ttu-id="42870-152">PSIPFlowVerifyResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="42870-152">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="42870-153">筆記</span><span class="sxs-lookup"><span data-stu-id="42870-153">NOTES</span></span>
<span data-ttu-id="42870-154">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，流程，ip</span><span class="sxs-lookup"><span data-stu-id="42870-154">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="42870-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="42870-155">RELATED LINKS</span></span>

[<span data-ttu-id="42870-156">新-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="42870-156">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="42870-157">AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="42870-157">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="42870-158">移除-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="42870-158">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="42870-159">AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="42870-159">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="42870-160">AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="42870-160">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="42870-161">AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="42870-161">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="42870-162">開始-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="42870-162">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="42870-163">新-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="42870-163">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="42870-164">新-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="42870-164">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="42870-165">AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="42870-165">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="42870-166">移除-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="42870-166">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="42870-167">停止 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="42870-167">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="42870-168">新-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="42870-168">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="42870-169">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="42870-169">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="42870-170">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="42870-170">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="42870-171">停止 AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="42870-171">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="42870-172">開始-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="42870-172">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="42870-173">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="42870-173">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="42870-174">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="42870-174">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="42870-175">移除-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="42870-175">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="42870-176">新-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="42870-176">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="42870-177">AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="42870-177">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="42870-178">AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="42870-178">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="42870-179">AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="42870-179">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="42870-180">AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="42870-180">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="42870-181">AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="42870-181">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="42870-182">AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="42870-182">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
