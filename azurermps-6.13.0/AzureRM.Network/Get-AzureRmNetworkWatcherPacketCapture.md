---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 00adf4abd887c56f4091761a4a2031bb6b033032
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455200"
---
# <span data-ttu-id="615bf-101">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="615bf-101">Get-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="615bf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="615bf-102">SYNOPSIS</span></span>
<span data-ttu-id="615bf-103">取得資料包捕獲資源的資訊和屬性和狀態。</span><span class="sxs-lookup"><span data-stu-id="615bf-103">Gets information and properties and status of a packet capture resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="615bf-104">句法</span><span class="sxs-lookup"><span data-stu-id="615bf-104">SYNTAX</span></span>

### <span data-ttu-id="615bf-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="615bf-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="615bf-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="615bf-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="615bf-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="615bf-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherPacketCapture -Location <String> [-PacketCaptureName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="615bf-108">說明</span><span class="sxs-lookup"><span data-stu-id="615bf-108">DESCRIPTION</span></span>
<span data-ttu-id="615bf-109">Get-AzureRmNetworkWatcherPacketCapture 會取得資料包捕獲資源的屬性和狀態。</span><span class="sxs-lookup"><span data-stu-id="615bf-109">The Get-AzureRmNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="615bf-110">示例</span><span class="sxs-lookup"><span data-stu-id="615bf-110">EXAMPLES</span></span>

### <span data-ttu-id="615bf-111">範例1：使用多個篩選器建立資料包捕獲並檢索其狀態</span><span class="sxs-lookup"><span data-stu-id="615bf-111">Example 1: Create a Packet Capture with multiple filters and retrieve its status</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="615bf-112">在這個範例中，我們會建立名為 "PacketCaptureTest" 的資料包捕獲，並提供多個篩選和時間限制。</span><span class="sxs-lookup"><span data-stu-id="615bf-112">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="615bf-113">會話完成後，就會將它儲存到指定的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="615bf-113">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="615bf-114">接著，我們會呼叫 Get-AzureRmNetworkWatcherPacketCapture 來取得捕獲會話的狀態。</span><span class="sxs-lookup"><span data-stu-id="615bf-114">We then call Get-AzureRmNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> <span data-ttu-id="615bf-115">注意：必須在目標虛擬機器上安裝 Azure 網路觀察程式延伸，才能建立資料包捕獲。</span><span class="sxs-lookup"><span data-stu-id="615bf-115">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="615bf-116">參數</span><span class="sxs-lookup"><span data-stu-id="615bf-116">PARAMETERS</span></span>

### <span data-ttu-id="615bf-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="615bf-117">-AsJob</span></span>
<span data-ttu-id="615bf-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="615bf-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="615bf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="615bf-119">-DefaultProfile</span></span>
<span data-ttu-id="615bf-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="615bf-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="615bf-121">-位置</span><span class="sxs-lookup"><span data-stu-id="615bf-121">-Location</span></span>
<span data-ttu-id="615bf-122">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="615bf-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="615bf-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="615bf-123">-NetworkWatcher</span></span>
<span data-ttu-id="615bf-124">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="615bf-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="615bf-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="615bf-125">-NetworkWatcherName</span></span>
<span data-ttu-id="615bf-126">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="615bf-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="615bf-127">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="615bf-127">-PacketCaptureName</span></span>
<span data-ttu-id="615bf-128">[資料包捕獲名稱]。</span><span class="sxs-lookup"><span data-stu-id="615bf-128">The packet capture name.</span></span>

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

### <span data-ttu-id="615bf-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="615bf-129">-ResourceGroupName</span></span>
<span data-ttu-id="615bf-130">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="615bf-130">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="615bf-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="615bf-131">CommonParameters</span></span>
<span data-ttu-id="615bf-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="615bf-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="615bf-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="615bf-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="615bf-134">輸入</span><span class="sxs-lookup"><span data-stu-id="615bf-134">INPUTS</span></span>

### <span data-ttu-id="615bf-135">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="615bf-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="615bf-136">參數： NetworkWatcher (ByValue) </span><span class="sxs-lookup"><span data-stu-id="615bf-136">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="615bf-137">System.object</span><span class="sxs-lookup"><span data-stu-id="615bf-137">System.String</span></span>
<span data-ttu-id="615bf-138">參數： NetworkWatcherName (ByValue) </span><span class="sxs-lookup"><span data-stu-id="615bf-138">Parameters: NetworkWatcherName (ByValue)</span></span>

## <span data-ttu-id="615bf-139">輸出</span><span class="sxs-lookup"><span data-stu-id="615bf-139">OUTPUTS</span></span>

### <span data-ttu-id="615bf-140">PSGetPacketCaptureResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="615bf-140">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="615bf-141">筆記</span><span class="sxs-lookup"><span data-stu-id="615bf-141">NOTES</span></span>
<span data-ttu-id="615bf-142">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，資料包，捕獲，流量</span><span class="sxs-lookup"><span data-stu-id="615bf-142">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="615bf-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="615bf-143">RELATED LINKS</span></span>

[<span data-ttu-id="615bf-144">新-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="615bf-144">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="615bf-145">AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="615bf-145">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="615bf-146">移除-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="615bf-146">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="615bf-147">AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="615bf-147">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="615bf-148">AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="615bf-148">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="615bf-149">AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="615bf-149">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="615bf-150">開始-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="615bf-150">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="615bf-151">新-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="615bf-151">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="615bf-152">新-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="615bf-152">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="615bf-153">AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="615bf-153">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="615bf-154">移除-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="615bf-154">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="615bf-155">停止 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="615bf-155">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="615bf-156">新-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="615bf-156">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="615bf-157">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="615bf-157">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="615bf-158">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="615bf-158">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="615bf-159">停止 AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="615bf-159">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="615bf-160">開始-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="615bf-160">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="615bf-161">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="615bf-161">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="615bf-162">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="615bf-162">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="615bf-163">移除-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="615bf-163">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="615bf-164">新-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="615bf-164">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="615bf-165">AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="615bf-165">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="615bf-166">AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="615bf-166">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="615bf-167">AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="615bf-167">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="615bf-168">AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="615bf-168">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="615bf-169">AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="615bf-169">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="615bf-170">AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="615bf-170">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)

