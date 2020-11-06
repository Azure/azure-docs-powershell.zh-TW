---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchernexthop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherNextHop.md
ms.openlocfilehash: 4c6a1e179cf0c6086035488d092232e85c570637
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448388"
---
# <span data-ttu-id="c461b-101">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c461b-101">Get-AzureRmNetworkWatcherNextHop</span></span>

## <span data-ttu-id="c461b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c461b-102">SYNOPSIS</span></span>
<span data-ttu-id="c461b-103">從 VM 取得下一個躍點。</span><span class="sxs-lookup"><span data-stu-id="c461b-103">Gets the next hop from a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c461b-104">句法</span><span class="sxs-lookup"><span data-stu-id="c461b-104">SYNTAX</span></span>

### <span data-ttu-id="c461b-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="c461b-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c461b-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="c461b-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c461b-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="c461b-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherNextHop -Location <String> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c461b-108">說明</span><span class="sxs-lookup"><span data-stu-id="c461b-108">DESCRIPTION</span></span>
<span data-ttu-id="c461b-109">Get-AzureRmNetworkWatcherNextHop Cmdlet 會從 VM 取得下一個躍點。</span><span class="sxs-lookup"><span data-stu-id="c461b-109">The Get-AzureRmNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="c461b-110">下一個躍點可讓您查看 Azure 資源類型、該資源的關聯 IP 位址，以及負責路由的路由表規則。</span><span class="sxs-lookup"><span data-stu-id="c461b-110">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="c461b-111">示例</span><span class="sxs-lookup"><span data-stu-id="c461b-111">EXAMPLES</span></span>

### <span data-ttu-id="c461b-112">範例1：在與網際網路 IP 通訊時取得下一個躍點</span><span class="sxs-lookup"><span data-stu-id="c461b-112">Example 1: Get the Next Hop when communicating with an Internet IP</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName ContosoResourceGroup -Name VM0
$Nics = Get-AzureRmNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}
Get-AzureRmNetworkWatcherNextHop -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -SourceIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress  -DestinationIPAddress 204.79.197.200


NextHopIpAddress NextHopType RouteTableId
---------------- ----------- ------------
                 Internet    System Route
```

<span data-ttu-id="c461b-113">取得從指定虛擬 Vachine 的主要網路介面到 204.79.197.200 (www.bing.com 的下一個從外寄通訊的躍點) </span><span class="sxs-lookup"><span data-stu-id="c461b-113">Get's the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Vachine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="c461b-114">參數</span><span class="sxs-lookup"><span data-stu-id="c461b-114">PARAMETERS</span></span>

### <span data-ttu-id="c461b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c461b-115">-AsJob</span></span>
<span data-ttu-id="c461b-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c461b-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c461b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c461b-117">-DefaultProfile</span></span>
<span data-ttu-id="c461b-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c461b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c461b-119">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="c461b-119">-DestinationIPAddress</span></span>
<span data-ttu-id="c461b-120">目的地 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="c461b-120">Destination IP address.</span></span>

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

### <span data-ttu-id="c461b-121">-位置</span><span class="sxs-lookup"><span data-stu-id="c461b-121">-Location</span></span>
<span data-ttu-id="c461b-122">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="c461b-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="c461b-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c461b-123">-NetworkWatcher</span></span>
<span data-ttu-id="c461b-124">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="c461b-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="c461b-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="c461b-125">-NetworkWatcherName</span></span>
<span data-ttu-id="c461b-126">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="c461b-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="c461b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c461b-127">-ResourceGroupName</span></span>
<span data-ttu-id="c461b-128">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c461b-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="c461b-129">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="c461b-129">-SourceIPAddress</span></span>
<span data-ttu-id="c461b-130">來源 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="c461b-130">Source IP address.</span></span>

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

### <span data-ttu-id="c461b-131">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="c461b-131">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="c461b-132">目標網路介面 Id。</span><span class="sxs-lookup"><span data-stu-id="c461b-132">Target network interface Id.</span></span>

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

### <span data-ttu-id="c461b-133">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="c461b-133">-TargetVirtualMachineId</span></span>
<span data-ttu-id="c461b-134">目標虛擬機器 ID。</span><span class="sxs-lookup"><span data-stu-id="c461b-134">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="c461b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c461b-135">CommonParameters</span></span>
<span data-ttu-id="c461b-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c461b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c461b-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c461b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c461b-138">輸入</span><span class="sxs-lookup"><span data-stu-id="c461b-138">INPUTS</span></span>

### <span data-ttu-id="c461b-139">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c461b-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="c461b-140">參數： NetworkWatcher (ByValue) </span><span class="sxs-lookup"><span data-stu-id="c461b-140">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="c461b-141">System.object</span><span class="sxs-lookup"><span data-stu-id="c461b-141">System.String</span></span>
<span data-ttu-id="c461b-142">參數： NetworkWatcherName (ByValue) </span><span class="sxs-lookup"><span data-stu-id="c461b-142">Parameters: NetworkWatcherName (ByValue)</span></span>

## <span data-ttu-id="c461b-143">輸出</span><span class="sxs-lookup"><span data-stu-id="c461b-143">OUTPUTS</span></span>

### <span data-ttu-id="c461b-144">PSNextHopResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c461b-144">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="c461b-145">筆記</span><span class="sxs-lookup"><span data-stu-id="c461b-145">NOTES</span></span>
<span data-ttu-id="c461b-146">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，下一步，hop</span><span class="sxs-lookup"><span data-stu-id="c461b-146">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="c461b-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="c461b-147">RELATED LINKS</span></span>

[<span data-ttu-id="c461b-148">新-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c461b-148">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="c461b-149">AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c461b-149">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="c461b-150">移除-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c461b-150">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="c461b-151">AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c461b-151">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="c461b-152">AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c461b-152">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="c461b-153">AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c461b-153">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="c461b-154">開始-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c461b-154">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="c461b-155">新-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c461b-155">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c461b-156">新-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c461b-156">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="c461b-157">AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c461b-157">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c461b-158">移除-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c461b-158">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c461b-159">停止 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c461b-159">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c461b-160">新-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="c461b-160">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="c461b-161">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="c461b-161">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="c461b-162">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="c461b-162">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="c461b-163">停止 AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c461b-163">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c461b-164">開始-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c461b-164">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c461b-165">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c461b-165">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c461b-166">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="c461b-166">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="c461b-167">移除-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c461b-167">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c461b-168">新-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c461b-168">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c461b-169">AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="c461b-169">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="c461b-170">AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="c461b-170">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="c461b-171">AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="c461b-171">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="c461b-172">AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="c461b-172">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="c461b-173">AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="c461b-173">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="c461b-174">AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c461b-174">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
