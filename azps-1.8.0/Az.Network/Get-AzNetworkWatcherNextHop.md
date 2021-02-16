---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchernexthop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
ms.openlocfilehash: 8da7165a9bb9e67076d9ba68f59ffd3208d1f391
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400411"
---
# <span data-ttu-id="b5a73-101">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="b5a73-101">Get-AzNetworkWatcherNextHop</span></span>

## <span data-ttu-id="b5a73-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b5a73-102">SYNOPSIS</span></span>
<span data-ttu-id="b5a73-103">從 VM 獲得下一個躍點。</span><span class="sxs-lookup"><span data-stu-id="b5a73-103">Gets the next hop from a VM.</span></span>

## <span data-ttu-id="b5a73-104">語法</span><span class="sxs-lookup"><span data-stu-id="b5a73-104">SYNTAX</span></span>

### <span data-ttu-id="b5a73-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="b5a73-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5a73-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="b5a73-106">SetByName</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5a73-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="b5a73-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherNextHop -Location <String> -TargetVirtualMachineId <String> -DestinationIPAddress <String>
 -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5a73-108">描述</span><span class="sxs-lookup"><span data-stu-id="b5a73-108">DESCRIPTION</span></span>
<span data-ttu-id="b5a73-109">Cmdlet Get-AzNetworkWatcherNextHop從 VM 獲得下一個躍點。</span><span class="sxs-lookup"><span data-stu-id="b5a73-109">The Get-AzNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span>
<span data-ttu-id="b5a73-110">下一個躍點可讓您查看 Azure 資源的類型、該資源的關聯 IP 位址，以及負責路由的路由資料表規則。</span><span class="sxs-lookup"><span data-stu-id="b5a73-110">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="b5a73-111">例子</span><span class="sxs-lookup"><span data-stu-id="b5a73-111">EXAMPLES</span></span>

### <span data-ttu-id="b5a73-112">範例 1：使用網際網路 IP 進行通訊時取得下一個躍點</span><span class="sxs-lookup"><span data-stu-id="b5a73-112">Example 1: Get the Next Hop when communicating with an Internet IP</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" }
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0
$Nics = Get-AzNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}
Get-AzNetworkWatcherNextHop -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -SourceIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress  -DestinationIPAddress 204.79.197.200


NextHopIpAddress NextHopType RouteTableId
---------------- ----------- ------------
                 Internet    System Route
```

<span data-ttu-id="b5a73-113">取得從指定虛擬 Vachine 上的主要網路介面到 204.79.197.200 (www.bing.com) </span><span class="sxs-lookup"><span data-stu-id="b5a73-113">Get's the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Vachine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="b5a73-114">參數</span><span class="sxs-lookup"><span data-stu-id="b5a73-114">PARAMETERS</span></span>

### <span data-ttu-id="b5a73-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b5a73-115">-AsJob</span></span>
<span data-ttu-id="b5a73-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b5a73-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b5a73-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5a73-117">-DefaultProfile</span></span>
<span data-ttu-id="b5a73-118">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b5a73-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5a73-119">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="b5a73-119">-DestinationIPAddress</span></span>
<span data-ttu-id="b5a73-120">目的地 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="b5a73-120">Destination IP address.</span></span>

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

### <span data-ttu-id="b5a73-121">-位置</span><span class="sxs-lookup"><span data-stu-id="b5a73-121">-Location</span></span>
<span data-ttu-id="b5a73-122">網路監視者的位置。</span><span class="sxs-lookup"><span data-stu-id="b5a73-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="b5a73-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b5a73-123">-NetworkWatcher</span></span>
<span data-ttu-id="b5a73-124">網路監視程式資源。</span><span class="sxs-lookup"><span data-stu-id="b5a73-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="b5a73-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="b5a73-125">-NetworkWatcherName</span></span>
<span data-ttu-id="b5a73-126">網路監視者的名稱。</span><span class="sxs-lookup"><span data-stu-id="b5a73-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="b5a73-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5a73-127">-ResourceGroupName</span></span>
<span data-ttu-id="b5a73-128">網路監視者資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b5a73-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="b5a73-129">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="b5a73-129">-SourceIPAddress</span></span>
<span data-ttu-id="b5a73-130">來源 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="b5a73-130">Source IP address.</span></span>

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

### <span data-ttu-id="b5a73-131">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="b5a73-131">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="b5a73-132">目標網路介面識別碼。</span><span class="sxs-lookup"><span data-stu-id="b5a73-132">Target network interface Id.</span></span>

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

### <span data-ttu-id="b5a73-133">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="b5a73-133">-TargetVirtualMachineId</span></span>
<span data-ttu-id="b5a73-134">目標虛擬機器識別碼。</span><span class="sxs-lookup"><span data-stu-id="b5a73-134">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="b5a73-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5a73-135">CommonParameters</span></span>
<span data-ttu-id="b5a73-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b5a73-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5a73-137">詳細資訊[請參閱about_CommonParameters。](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b5a73-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5a73-138">輸入</span><span class="sxs-lookup"><span data-stu-id="b5a73-138">INPUTS</span></span>

### <span data-ttu-id="b5a73-139">Microsoft.Azure.Commands.Network.models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b5a73-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="b5a73-140">System.String</span><span class="sxs-lookup"><span data-stu-id="b5a73-140">System.String</span></span>

## <span data-ttu-id="b5a73-141">輸出</span><span class="sxs-lookup"><span data-stu-id="b5a73-141">OUTPUTS</span></span>

### <span data-ttu-id="b5a73-142">Microsoft.Azure.Commands.Network.models.PSNextHopResult</span><span class="sxs-lookup"><span data-stu-id="b5a73-142">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="b5a73-143">筆記</span><span class="sxs-lookup"><span data-stu-id="b5a73-143">NOTES</span></span>
<span data-ttu-id="b5a73-144">關鍵字：azure、azurerm、arm、資源、管理、管理員、網路、網路、網路監視者、下一個、躍點</span><span class="sxs-lookup"><span data-stu-id="b5a73-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span>

## <span data-ttu-id="b5a73-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="b5a73-145">RELATED LINKS</span></span>

[<span data-ttu-id="b5a73-146">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b5a73-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="b5a73-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b5a73-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="b5a73-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b5a73-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="b5a73-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="b5a73-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="b5a73-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="b5a73-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="b5a73-151">Get-AzNetworkWatcherTopwork</span><span class="sxs-lookup"><span data-stu-id="b5a73-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="b5a73-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="b5a73-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="b5a73-153">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b5a73-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b5a73-154">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="b5a73-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="b5a73-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b5a73-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b5a73-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b5a73-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b5a73-157">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b5a73-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b5a73-158">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="b5a73-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="b5a73-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="b5a73-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="b5a73-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="b5a73-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="b5a73-161">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b5a73-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b5a73-162">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b5a73-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b5a73-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b5a73-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b5a73-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="b5a73-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="b5a73-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b5a73-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b5a73-166">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b5a73-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b5a73-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="b5a73-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="b5a73-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="b5a73-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="b5a73-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="b5a73-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="b5a73-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="b5a73-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="b5a73-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="b5a73-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="b5a73-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b5a73-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
