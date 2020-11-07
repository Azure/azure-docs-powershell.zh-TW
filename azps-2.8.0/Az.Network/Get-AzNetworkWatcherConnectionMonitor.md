---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 0c59de4b0c6dfd7da196b4ec67999406a14e0d1a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789557"
---
# <span data-ttu-id="a0f72-101">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a0f72-101">Get-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="a0f72-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a0f72-102">SYNOPSIS</span></span>
<span data-ttu-id="a0f72-103">以指定的名稱或連線監視器清單傳回連接監視器</span><span class="sxs-lookup"><span data-stu-id="a0f72-103">Returns connection monitor with specified name or the list of connection monitors</span></span>

## <span data-ttu-id="a0f72-104">句法</span><span class="sxs-lookup"><span data-stu-id="a0f72-104">SYNTAX</span></span>

### <span data-ttu-id="a0f72-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="a0f72-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0f72-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="a0f72-106">SetByResource</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0f72-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="a0f72-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0f72-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a0f72-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a0f72-109">說明</span><span class="sxs-lookup"><span data-stu-id="a0f72-109">DESCRIPTION</span></span>
<span data-ttu-id="a0f72-110">Get-AzNetworkWatcherConnectionMonitor Cmdlet 會以指定的名稱/resourceId 或與指定的網路監控程式/位置相對應的連線監視器清單傳回連接監視器。</span><span class="sxs-lookup"><span data-stu-id="a0f72-110">The Get-AzNetworkWatcherConnectionMonitor cmdlet returns the connection monitor with the specified name / resourceId or the list of connection monitors corresponding to the specified network watcher / location.</span></span>

## <span data-ttu-id="a0f72-111">示例</span><span class="sxs-lookup"><span data-stu-id="a0f72-111">EXAMPLES</span></span>

### <span data-ttu-id="a0f72-112">範例1：依名稱在指定位置取得連接監視器</span><span class="sxs-lookup"><span data-stu-id="a0f72-112">Example 1: Get connection monitor by name in the specified location</span></span>
```
PS C:\> Get-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm


Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/cm
Etag                        : W/"40961b58-e379-4204-a47b-0c477739b095"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/96e68903-0a56-4819-9987-8d08ad6
                              a1f99/resourceGroups/VarunRgCentralUSEUAP/providers/Microsoft.C
                              ompute/virtualMachines/irinavm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "google.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:19:28 PM
MonitoringStatus            : Stopped
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {
                                "key1": "value1"
                              }
```

<span data-ttu-id="a0f72-113">在這個範例中，我們會透過名稱在指定位置取得連接監視器。</span><span class="sxs-lookup"><span data-stu-id="a0f72-113">In this example we get connection monitor by name in the specified location.</span></span>

### <span data-ttu-id="a0f72-114">範例2：使用篩選取得連接監視器</span><span class="sxs-lookup"><span data-stu-id="a0f72-114">Example 2: Get connection monitors using filtering</span></span>
```
PS C:\> Get-AzNetworkWatcherConnectionMonitor -ResourceGroupName NetworkWatcherRG -NetworkWatcherName NetworkWatcher_centraluseuap -Name cm*


Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/cm
Etag                        : W/"40961b58-e379-4204-a47b-0c477739b095"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/96e68903-0a56-4819-9987-8d08ad6
                              a1f99/resourceGroups/VarunRgCentralUSEUAP/providers/Microsoft.C
                              ompute/virtualMachines/irinavm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "google.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:19:28 PM
MonitoringStatus            : Stopped
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {
                                "key1": "value1"
                              }
```

<span data-ttu-id="a0f72-115">在這個範例中，我們會在 NetworkWatcher_centraluseuap 中取得所有以 "cm" 開頭的連線監視器</span><span class="sxs-lookup"><span data-stu-id="a0f72-115">In this example we get all connection monitors in NetworkWatcher_centraluseuap that start with "cm"</span></span>

## <span data-ttu-id="a0f72-116">參數</span><span class="sxs-lookup"><span data-stu-id="a0f72-116">PARAMETERS</span></span>

### <span data-ttu-id="a0f72-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0f72-117">-DefaultProfile</span></span>
<span data-ttu-id="a0f72-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a0f72-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0f72-119">-位置</span><span class="sxs-lookup"><span data-stu-id="a0f72-119">-Location</span></span>
<span data-ttu-id="a0f72-120">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="a0f72-120">Location of the network watcher.</span></span>

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

### <span data-ttu-id="a0f72-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="a0f72-121">-Name</span></span>
<span data-ttu-id="a0f72-122">[連接監視器] 名稱。</span><span class="sxs-lookup"><span data-stu-id="a0f72-122">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="a0f72-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a0f72-123">-NetworkWatcher</span></span>
<span data-ttu-id="a0f72-124">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="a0f72-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="a0f72-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="a0f72-125">-NetworkWatcherName</span></span>
<span data-ttu-id="a0f72-126">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="a0f72-126">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f72-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0f72-127">-ResourceGroupName</span></span>
<span data-ttu-id="a0f72-128">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a0f72-128">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f72-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a0f72-129">-ResourceId</span></span>
<span data-ttu-id="a0f72-130">[連線監視器] 的 [資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="a0f72-130">Resource ID of the connection monitor.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0f72-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0f72-131">CommonParameters</span></span>
<span data-ttu-id="a0f72-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a0f72-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0f72-133">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a0f72-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0f72-134">輸入</span><span class="sxs-lookup"><span data-stu-id="a0f72-134">INPUTS</span></span>

### <span data-ttu-id="a0f72-135">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a0f72-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="a0f72-136">System.object</span><span class="sxs-lookup"><span data-stu-id="a0f72-136">System.String</span></span>

## <span data-ttu-id="a0f72-137">輸出</span><span class="sxs-lookup"><span data-stu-id="a0f72-137">OUTPUTS</span></span>

### <span data-ttu-id="a0f72-138">PSConnectionMonitorResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a0f72-138">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="a0f72-139">筆記</span><span class="sxs-lookup"><span data-stu-id="a0f72-139">NOTES</span></span>
<span data-ttu-id="a0f72-140">關鍵字： azure，azurerm，arm，資源，連線，管理，管理員，網路，網路，網路觀察程式，連線監視器</span><span class="sxs-lookup"><span data-stu-id="a0f72-140">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="a0f72-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="a0f72-141">RELATED LINKS</span></span>

[<span data-ttu-id="a0f72-142">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a0f72-142">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="a0f72-143">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a0f72-143">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="a0f72-144">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a0f72-144">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="a0f72-145">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="a0f72-145">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="a0f72-146">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="a0f72-146">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="a0f72-147">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="a0f72-147">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="a0f72-148">AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="a0f72-148">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="a0f72-149">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a0f72-149">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a0f72-150">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="a0f72-150">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="a0f72-151">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a0f72-151">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a0f72-152">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a0f72-152">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a0f72-153">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a0f72-153">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a0f72-154">AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a0f72-154">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a0f72-155">AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="a0f72-155">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="a0f72-156">移除-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a0f72-156">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a0f72-157">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a0f72-157">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a0f72-158">停止 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a0f72-158">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a0f72-159">新-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a0f72-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a0f72-160">新-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="a0f72-160">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="a0f72-161">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="a0f72-161">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="a0f72-162">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="a0f72-162">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="a0f72-163">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="a0f72-163">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="a0f72-164">開始-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a0f72-164">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a0f72-165">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="a0f72-165">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="a0f72-166">AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="a0f72-166">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="a0f72-167">AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="a0f72-167">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="a0f72-168">AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="a0f72-168">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)
