---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 1276a3c63ec4b9c4ec1c2c4c91ea792013cbacc9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140028"
---
# <span data-ttu-id="0dbe5-101">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0dbe5-101">Get-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="0dbe5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0dbe5-102">SYNOPSIS</span></span>
<span data-ttu-id="0dbe5-103">取得資料包捕獲資源的資訊和屬性和狀態。</span><span class="sxs-lookup"><span data-stu-id="0dbe5-103">Gets information and properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="0dbe5-104">句法</span><span class="sxs-lookup"><span data-stu-id="0dbe5-104">SYNTAX</span></span>

### <span data-ttu-id="0dbe5-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="0dbe5-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0dbe5-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="0dbe5-106">SetByName</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0dbe5-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="0dbe5-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherPacketCapture -Location <String> [-PacketCaptureName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0dbe5-108">說明</span><span class="sxs-lookup"><span data-stu-id="0dbe5-108">DESCRIPTION</span></span>
<span data-ttu-id="0dbe5-109">Get-AzNetworkWatcherPacketCapture 會取得資料包捕獲資源的屬性和狀態。</span><span class="sxs-lookup"><span data-stu-id="0dbe5-109">The Get-AzNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="0dbe5-110">示例</span><span class="sxs-lookup"><span data-stu-id="0dbe5-110">EXAMPLES</span></span>

### <span data-ttu-id="0dbe5-111">範例1：使用多個篩選器建立資料包捕獲並檢索其狀態</span><span class="sxs-lookup"><span data-stu-id="0dbe5-111">Example 1: Create a Packet Capture with multiple filters and retrieve its status</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="0dbe5-112">在這個範例中，我們會建立名為 "PacketCaptureTest" 的資料包捕獲，並提供多個篩選和時間限制。</span><span class="sxs-lookup"><span data-stu-id="0dbe5-112">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="0dbe5-113">會話完成後，就會將它儲存到指定的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="0dbe5-113">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="0dbe5-114">接著，我們會呼叫 Get-AzNetworkWatcherPacketCapture 來取得捕獲會話的狀態。</span><span class="sxs-lookup"><span data-stu-id="0dbe5-114">We then call Get-AzNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> <span data-ttu-id="0dbe5-115">注意：必須在目標虛擬機器上安裝 Azure 網路觀察程式延伸，才能建立資料包捕獲。</span><span class="sxs-lookup"><span data-stu-id="0dbe5-115">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

>[!NOTE]
><span data-ttu-id="0dbe5-116">如果您直接從 [New-AzNetworkWatcherPacketCapture] 命令建立 [資料包捕獲] 的參照，就不會有所有的屬性。</span><span class="sxs-lookup"><span data-stu-id="0dbe5-116">If you create a reference to the packet capture directly from the New-AzNetworkWatcherPacketCapture command, it won't have all the properties.</span></span> <span data-ttu-id="0dbe5-117">您可以呼叫 Get-AzNetworkWatcherPacketCapture 命令來取得資料包捕獲的所有屬性。</span><span class="sxs-lookup"><span data-stu-id="0dbe5-117">You can get all of the properties of the packet capture by making a call to the Get-AzNetworkWatcherPacketCapture command.</span></span>

### <span data-ttu-id="0dbe5-118">範例2：使用多個篩選器建立資料包捕獲並檢索其狀態</span><span class="sxs-lookup"><span data-stu-id="0dbe5-118">Example 2: Create a Packet Capture with multiple filters and retrieve its status</span></span>
```
Get-AzNetworkWatcherPacketCapture -ResourceGroupName rg1 -NetworkWatcherName nw1 -PacketCaptureName PacketCapture*
```

<span data-ttu-id="0dbe5-119">這個 Cmdlet 會傳回在 nw1 網路觀察程式中以「PacketCapture」為開頭的所有 PacketCaptures。</span><span class="sxs-lookup"><span data-stu-id="0dbe5-119">This cmdlet returns all PacketCaptures that start with "PacketCapture" in the nw1 Network Watcher.</span></span>

## <span data-ttu-id="0dbe5-120">參數</span><span class="sxs-lookup"><span data-stu-id="0dbe5-120">PARAMETERS</span></span>

### <span data-ttu-id="0dbe5-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0dbe5-121">-AsJob</span></span>
<span data-ttu-id="0dbe5-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0dbe5-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0dbe5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dbe5-123">-DefaultProfile</span></span>
<span data-ttu-id="0dbe5-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0dbe5-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0dbe5-125">-位置</span><span class="sxs-lookup"><span data-stu-id="0dbe5-125">-Location</span></span>
<span data-ttu-id="0dbe5-126">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="0dbe5-126">Location of the network watcher.</span></span>

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

### <span data-ttu-id="0dbe5-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0dbe5-127">-NetworkWatcher</span></span>
<span data-ttu-id="0dbe5-128">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="0dbe5-128">The network watcher resource.</span></span>

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

### <span data-ttu-id="0dbe5-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="0dbe5-129">-NetworkWatcherName</span></span>
<span data-ttu-id="0dbe5-130">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="0dbe5-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="0dbe5-131">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="0dbe5-131">-PacketCaptureName</span></span>
<span data-ttu-id="0dbe5-132">[資料包捕獲名稱]。</span><span class="sxs-lookup"><span data-stu-id="0dbe5-132">The packet capture name.</span></span>

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

### <span data-ttu-id="0dbe5-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0dbe5-133">-ResourceGroupName</span></span>
<span data-ttu-id="0dbe5-134">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0dbe5-134">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="0dbe5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dbe5-135">CommonParameters</span></span>
<span data-ttu-id="0dbe5-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0dbe5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dbe5-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0dbe5-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dbe5-138">輸入</span><span class="sxs-lookup"><span data-stu-id="0dbe5-138">INPUTS</span></span>

### <span data-ttu-id="0dbe5-139">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0dbe5-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="0dbe5-140">System.object</span><span class="sxs-lookup"><span data-stu-id="0dbe5-140">System.String</span></span>

## <span data-ttu-id="0dbe5-141">輸出</span><span class="sxs-lookup"><span data-stu-id="0dbe5-141">OUTPUTS</span></span>

### <span data-ttu-id="0dbe5-142">PSGetPacketCaptureResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0dbe5-142">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="0dbe5-143">筆記</span><span class="sxs-lookup"><span data-stu-id="0dbe5-143">NOTES</span></span>
<span data-ttu-id="0dbe5-144">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，資料包，捕獲，流量</span><span class="sxs-lookup"><span data-stu-id="0dbe5-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="0dbe5-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="0dbe5-145">RELATED LINKS</span></span>

[<span data-ttu-id="0dbe5-146">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0dbe5-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="0dbe5-147">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0dbe5-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="0dbe5-148">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0dbe5-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="0dbe5-149">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="0dbe5-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="0dbe5-150">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="0dbe5-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="0dbe5-151">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="0dbe5-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="0dbe5-152">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="0dbe5-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="0dbe5-153">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0dbe5-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0dbe5-154">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="0dbe5-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="0dbe5-155">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0dbe5-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0dbe5-156">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0dbe5-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0dbe5-157">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0dbe5-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0dbe5-158">新-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="0dbe5-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="0dbe5-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="0dbe5-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="0dbe5-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="0dbe5-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="0dbe5-161">停止 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0dbe5-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0dbe5-162">開始-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0dbe5-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0dbe5-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0dbe5-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0dbe5-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="0dbe5-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="0dbe5-165">移除-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0dbe5-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0dbe5-166">新-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0dbe5-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0dbe5-167">AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="0dbe5-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="0dbe5-168">AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="0dbe5-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="0dbe5-169">AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="0dbe5-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="0dbe5-170">AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="0dbe5-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="0dbe5-171">AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="0dbe5-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="0dbe5-172">AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0dbe5-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

