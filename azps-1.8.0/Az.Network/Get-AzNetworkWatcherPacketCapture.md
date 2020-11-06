---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 94d59f66563e3d4fd5f236613676e0cbe6b466c8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621968"
---
# <span data-ttu-id="a8532-101">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a8532-101">Get-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="a8532-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a8532-102">SYNOPSIS</span></span>
<span data-ttu-id="a8532-103">取得資料包捕獲資源的資訊和屬性和狀態。</span><span class="sxs-lookup"><span data-stu-id="a8532-103">Gets information and properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="a8532-104">句法</span><span class="sxs-lookup"><span data-stu-id="a8532-104">SYNTAX</span></span>

### <span data-ttu-id="a8532-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="a8532-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8532-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="a8532-106">SetByName</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8532-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="a8532-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherPacketCapture -Location <String> [-PacketCaptureName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8532-108">說明</span><span class="sxs-lookup"><span data-stu-id="a8532-108">DESCRIPTION</span></span>
<span data-ttu-id="a8532-109">Get-AzNetworkWatcherPacketCapture 會取得資料包捕獲資源的屬性和狀態。</span><span class="sxs-lookup"><span data-stu-id="a8532-109">The Get-AzNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="a8532-110">示例</span><span class="sxs-lookup"><span data-stu-id="a8532-110">EXAMPLES</span></span>

### <span data-ttu-id="a8532-111">範例1：使用多個篩選器建立資料包捕獲並檢索其狀態</span><span class="sxs-lookup"><span data-stu-id="a8532-111">Example 1: Create a Packet Capture with multiple filters and retrieve its status</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="a8532-112">在這個範例中，我們會建立名為 "PacketCaptureTest" 的資料包捕獲，並提供多個篩選和時間限制。</span><span class="sxs-lookup"><span data-stu-id="a8532-112">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="a8532-113">會話完成後，就會將它儲存到指定的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="a8532-113">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="a8532-114">接著，我們會呼叫 Get-AzNetworkWatcherPacketCapture 來取得捕獲會話的狀態。</span><span class="sxs-lookup"><span data-stu-id="a8532-114">We then call Get-AzNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> <span data-ttu-id="a8532-115">注意：必須在目標虛擬機器上安裝 Azure 網路觀察程式延伸，才能建立資料包捕獲。</span><span class="sxs-lookup"><span data-stu-id="a8532-115">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

### <span data-ttu-id="a8532-116">範例2：使用多個篩選器建立資料包捕獲並檢索其狀態</span><span class="sxs-lookup"><span data-stu-id="a8532-116">Example 2: Create a Packet Capture with multiple filters and retrieve its status</span></span>
```
Get-AzNetworkWatcherPacketCapture -ResourceGroupName rg1 -NetworkWatcherName nw1 -PacketCaptureName PacketCapture*
```

<span data-ttu-id="a8532-117">這個 Cmdlet 會傳回在 nw1 網路觀察程式中以「PacketCapture」為開頭的所有 PacketCaptures。</span><span class="sxs-lookup"><span data-stu-id="a8532-117">This cmdlet returns all PacketCaptures that start with "PacketCapture" in the nw1 Network Watcher.</span></span>

## <span data-ttu-id="a8532-118">參數</span><span class="sxs-lookup"><span data-stu-id="a8532-118">PARAMETERS</span></span>

### <span data-ttu-id="a8532-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a8532-119">-AsJob</span></span>
<span data-ttu-id="a8532-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a8532-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a8532-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8532-121">-DefaultProfile</span></span>
<span data-ttu-id="a8532-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a8532-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8532-123">-位置</span><span class="sxs-lookup"><span data-stu-id="a8532-123">-Location</span></span>
<span data-ttu-id="a8532-124">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="a8532-124">Location of the network watcher.</span></span>

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

### <span data-ttu-id="a8532-125">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a8532-125">-NetworkWatcher</span></span>
<span data-ttu-id="a8532-126">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="a8532-126">The network watcher resource.</span></span>

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

### <span data-ttu-id="a8532-127">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="a8532-127">-NetworkWatcherName</span></span>
<span data-ttu-id="a8532-128">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="a8532-128">The name of network watcher.</span></span>

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

### <span data-ttu-id="a8532-129">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="a8532-129">-PacketCaptureName</span></span>
<span data-ttu-id="a8532-130">[資料包捕獲名稱]。</span><span class="sxs-lookup"><span data-stu-id="a8532-130">The packet capture name.</span></span>

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

### <span data-ttu-id="a8532-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8532-131">-ResourceGroupName</span></span>
<span data-ttu-id="a8532-132">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a8532-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="a8532-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8532-133">CommonParameters</span></span>
<span data-ttu-id="a8532-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a8532-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8532-135">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a8532-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8532-136">輸入</span><span class="sxs-lookup"><span data-stu-id="a8532-136">INPUTS</span></span>

### <span data-ttu-id="a8532-137">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a8532-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="a8532-138">System.object</span><span class="sxs-lookup"><span data-stu-id="a8532-138">System.String</span></span>

## <span data-ttu-id="a8532-139">輸出</span><span class="sxs-lookup"><span data-stu-id="a8532-139">OUTPUTS</span></span>

### <span data-ttu-id="a8532-140">PSGetPacketCaptureResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a8532-140">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="a8532-141">筆記</span><span class="sxs-lookup"><span data-stu-id="a8532-141">NOTES</span></span>
<span data-ttu-id="a8532-142">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，資料包，捕獲，流量</span><span class="sxs-lookup"><span data-stu-id="a8532-142">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="a8532-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="a8532-143">RELATED LINKS</span></span>

[<span data-ttu-id="a8532-144">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a8532-144">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="a8532-145">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a8532-145">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="a8532-146">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a8532-146">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="a8532-147">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="a8532-147">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="a8532-148">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="a8532-148">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="a8532-149">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="a8532-149">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="a8532-150">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="a8532-150">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="a8532-151">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a8532-151">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a8532-152">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="a8532-152">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="a8532-153">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a8532-153">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a8532-154">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a8532-154">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a8532-155">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a8532-155">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a8532-156">新-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="a8532-156">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="a8532-157">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="a8532-157">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="a8532-158">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="a8532-158">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="a8532-159">停止 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a8532-159">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a8532-160">開始-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a8532-160">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a8532-161">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a8532-161">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a8532-162">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="a8532-162">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="a8532-163">移除-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a8532-163">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a8532-164">新-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a8532-164">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a8532-165">AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="a8532-165">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="a8532-166">AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="a8532-166">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="a8532-167">AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="a8532-167">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="a8532-168">AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="a8532-168">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="a8532-169">AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="a8532-169">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="a8532-170">AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a8532-170">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

