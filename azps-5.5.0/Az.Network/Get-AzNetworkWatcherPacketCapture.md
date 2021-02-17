---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: e836bb8738b594e09c65568cc0f454a476db9d34
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412821"
---
# <span data-ttu-id="d220f-101">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d220f-101">Get-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="d220f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d220f-102">SYNOPSIS</span></span>
<span data-ttu-id="d220f-103">獲得封包捕獲資源的資訊與屬性及狀態。</span><span class="sxs-lookup"><span data-stu-id="d220f-103">Gets information and properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="d220f-104">語法</span><span class="sxs-lookup"><span data-stu-id="d220f-104">SYNTAX</span></span>

### <span data-ttu-id="d220f-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="d220f-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d220f-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="d220f-106">SetByName</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d220f-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="d220f-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherPacketCapture -Location <String> [-PacketCaptureName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d220f-108">描述</span><span class="sxs-lookup"><span data-stu-id="d220f-108">DESCRIPTION</span></span>
<span data-ttu-id="d220f-109">此Get-AzNetworkWatcherPacketCapture會獲得封包捕獲資源的屬性和狀態。</span><span class="sxs-lookup"><span data-stu-id="d220f-109">The Get-AzNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="d220f-110">例子</span><span class="sxs-lookup"><span data-stu-id="d220f-110">EXAMPLES</span></span>

### <span data-ttu-id="d220f-111">範例 1：建立包含多個篩選的封包捕獲並取回其狀態</span><span class="sxs-lookup"><span data-stu-id="d220f-111">Example 1: Create a Packet Capture with multiple filters and retrieve its status</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="d220f-112">在此範例中，我們建立名為「PacketCaptureTest」的封包捕獲，具有多個篩選和時間限制。</span><span class="sxs-lookup"><span data-stu-id="d220f-112">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="d220f-113">會話完成之後，就會儲存到指定的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="d220f-113">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="d220f-114">接著，Get-AzNetworkWatcherPacketCapture以取回捕獲會話的狀態。</span><span class="sxs-lookup"><span data-stu-id="d220f-114">We then call Get-AzNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> <span data-ttu-id="d220f-115">注意：Azure 網路監視程式擴充功能必須安裝在目標虛擬機器上，以建立封包捕獲。</span><span class="sxs-lookup"><span data-stu-id="d220f-115">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

>[!NOTE]
><span data-ttu-id="d220f-116">如果您直接從命令建立封包捕獲的參照New-AzNetworkWatcherPacketCapture，就不會具有所有屬性。</span><span class="sxs-lookup"><span data-stu-id="d220f-116">If you create a reference to the packet capture directly from the New-AzNetworkWatcherPacketCapture command, it won't have all the properties.</span></span> <span data-ttu-id="d220f-117">您可以撥打至命令以取得封包捕獲Get-AzNetworkWatcherPacketCapture屬性。</span><span class="sxs-lookup"><span data-stu-id="d220f-117">You can get all of the properties of the packet capture by making a call to the Get-AzNetworkWatcherPacketCapture command.</span></span>

### <span data-ttu-id="d220f-118">範例 2：建立包含多個篩選的封包捕獲並取回其狀態</span><span class="sxs-lookup"><span data-stu-id="d220f-118">Example 2: Create a Packet Capture with multiple filters and retrieve its status</span></span>
```
Get-AzNetworkWatcherPacketCapture -ResourceGroupName rg1 -NetworkWatcherName nw1 -PacketCaptureName PacketCapture*
```

<span data-ttu-id="d220f-119">此 Cmdlet 會以 nw1 網路監視器中的 "PacketCapture" 做為開始的所有 PacketCapture。</span><span class="sxs-lookup"><span data-stu-id="d220f-119">This cmdlet returns all PacketCaptures that start with "PacketCapture" in the nw1 Network Watcher.</span></span>

## <span data-ttu-id="d220f-120">參數</span><span class="sxs-lookup"><span data-stu-id="d220f-120">PARAMETERS</span></span>

### <span data-ttu-id="d220f-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d220f-121">-AsJob</span></span>
<span data-ttu-id="d220f-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d220f-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d220f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d220f-123">-DefaultProfile</span></span>
<span data-ttu-id="d220f-124">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d220f-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d220f-125">-位置</span><span class="sxs-lookup"><span data-stu-id="d220f-125">-Location</span></span>
<span data-ttu-id="d220f-126">網路監視者的位置。</span><span class="sxs-lookup"><span data-stu-id="d220f-126">Location of the network watcher.</span></span>

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

### <span data-ttu-id="d220f-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d220f-127">-NetworkWatcher</span></span>
<span data-ttu-id="d220f-128">網路監視程式資源。</span><span class="sxs-lookup"><span data-stu-id="d220f-128">The network watcher resource.</span></span>

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

### <span data-ttu-id="d220f-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d220f-129">-NetworkWatcherName</span></span>
<span data-ttu-id="d220f-130">網路監視者的名稱。</span><span class="sxs-lookup"><span data-stu-id="d220f-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="d220f-131">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="d220f-131">-PacketCaptureName</span></span>
<span data-ttu-id="d220f-132">封包捕獲名稱。</span><span class="sxs-lookup"><span data-stu-id="d220f-132">The packet capture name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="d220f-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d220f-133">-ResourceGroupName</span></span>
<span data-ttu-id="d220f-134">網路監視者資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d220f-134">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="d220f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d220f-135">CommonParameters</span></span>
<span data-ttu-id="d220f-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d220f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d220f-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d220f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d220f-138">輸入</span><span class="sxs-lookup"><span data-stu-id="d220f-138">INPUTS</span></span>

### <span data-ttu-id="d220f-139">Microsoft.Azure.Commands.Network.models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d220f-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="d220f-140">System.String</span><span class="sxs-lookup"><span data-stu-id="d220f-140">System.String</span></span>

## <span data-ttu-id="d220f-141">輸出</span><span class="sxs-lookup"><span data-stu-id="d220f-141">OUTPUTS</span></span>

### <span data-ttu-id="d220f-142">Microsoft.Azure.Commands.Network.models.PSGetPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="d220f-142">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="d220f-143">筆記</span><span class="sxs-lookup"><span data-stu-id="d220f-143">NOTES</span></span>
<span data-ttu-id="d220f-144">關鍵字：azure、azurerm、arm、資源、管理、管理員、網路、網路、網路監視者、封包、捕獲、流量</span><span class="sxs-lookup"><span data-stu-id="d220f-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="d220f-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="d220f-145">RELATED LINKS</span></span>

[<span data-ttu-id="d220f-146">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d220f-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="d220f-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d220f-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="d220f-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d220f-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="d220f-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d220f-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="d220f-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d220f-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="d220f-151">Get-AzNetworkWatcherTopwork</span><span class="sxs-lookup"><span data-stu-id="d220f-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="d220f-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d220f-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="d220f-153">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d220f-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d220f-154">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d220f-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="d220f-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d220f-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d220f-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d220f-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d220f-157">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d220f-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d220f-158">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="d220f-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="d220f-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d220f-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="d220f-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="d220f-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="d220f-161">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d220f-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d220f-162">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d220f-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d220f-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d220f-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d220f-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="d220f-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="d220f-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d220f-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d220f-166">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d220f-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d220f-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="d220f-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="d220f-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="d220f-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="d220f-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="d220f-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="d220f-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="d220f-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="d220f-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="d220f-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="d220f-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d220f-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

