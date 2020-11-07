---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 3f380135cc6edde875c927dd9d640a10cdf14957
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625273"
---
# <span data-ttu-id="b3c2b-101">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b3c2b-101">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="b3c2b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b3c2b-102">SYNOPSIS</span></span>
<span data-ttu-id="b3c2b-103">以指定的名稱或連線監視器清單傳回連接監視器</span><span class="sxs-lookup"><span data-stu-id="b3c2b-103">Returns connection monitor with specified name or the list of connection monitors</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3c2b-104">句法</span><span class="sxs-lookup"><span data-stu-id="b3c2b-104">SYNTAX</span></span>

### <span data-ttu-id="b3c2b-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="b3c2b-105">SetByName (Default)</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3c2b-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b3c2b-106">SetByResource</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3c2b-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="b3c2b-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -Location <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3c2b-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b3c2b-108">SetByResourceId</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b3c2b-109">說明</span><span class="sxs-lookup"><span data-stu-id="b3c2b-109">DESCRIPTION</span></span>
<span data-ttu-id="b3c2b-110">Get-AzureRmNetworkWatcherConnectionMonitor Cmdlet 會以指定的名稱/resourceId 或與指定的網路監控程式/位置相對應的連線監視器清單傳回連接監視器。</span><span class="sxs-lookup"><span data-stu-id="b3c2b-110">The Get-AzureRmNetworkWatcherConnectionMonitor cmdlet returns the connection monitor with the specified name / resourceId or the list of connection monitors corresponding to the specified network watcher / location.</span></span>

## <span data-ttu-id="b3c2b-111">示例</span><span class="sxs-lookup"><span data-stu-id="b3c2b-111">EXAMPLES</span></span>

### <span data-ttu-id="b3c2b-112">範例1：依名稱在指定位置取得連接監視器</span><span class="sxs-lookup"><span data-stu-id="b3c2b-112">Example 1: Get connection monitor by name in the specified location</span></span>
```
PS C:\> Get-AzureRmNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm


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

<span data-ttu-id="b3c2b-113">在這個範例中，我們會透過名稱在指定位置取得連接監視器。</span><span class="sxs-lookup"><span data-stu-id="b3c2b-113">In this example we get connection monitor by name in the specified location.</span></span>

## <span data-ttu-id="b3c2b-114">參數</span><span class="sxs-lookup"><span data-stu-id="b3c2b-114">PARAMETERS</span></span>

### <span data-ttu-id="b3c2b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3c2b-115">-DefaultProfile</span></span>
<span data-ttu-id="b3c2b-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b3c2b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3c2b-117">-位置</span><span class="sxs-lookup"><span data-stu-id="b3c2b-117">-Location</span></span>
<span data-ttu-id="b3c2b-118">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="b3c2b-118">Location of the network watcher.</span></span>

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

### <span data-ttu-id="b3c2b-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="b3c2b-119">-Name</span></span>
<span data-ttu-id="b3c2b-120">[連接監視器] 名稱。</span><span class="sxs-lookup"><span data-stu-id="b3c2b-120">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3c2b-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b3c2b-121">-NetworkWatcher</span></span>
<span data-ttu-id="b3c2b-122">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="b3c2b-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="b3c2b-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="b3c2b-123">-NetworkWatcherName</span></span>
<span data-ttu-id="b3c2b-124">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3c2b-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="b3c2b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3c2b-125">-ResourceGroupName</span></span>
<span data-ttu-id="b3c2b-126">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3c2b-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="b3c2b-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3c2b-127">-ResourceId</span></span>
<span data-ttu-id="b3c2b-128">[連線監視器] 的 [資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="b3c2b-128">Resource ID of the connection monitor.</span></span>

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

### <span data-ttu-id="b3c2b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3c2b-129">CommonParameters</span></span>
<span data-ttu-id="b3c2b-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b3c2b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3c2b-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b3c2b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3c2b-132">輸入</span><span class="sxs-lookup"><span data-stu-id="b3c2b-132">INPUTS</span></span>

### <span data-ttu-id="b3c2b-133">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b3c2b-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="b3c2b-134">參數： NetworkWatcher (ByValue) </span><span class="sxs-lookup"><span data-stu-id="b3c2b-134">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="b3c2b-135">System.object</span><span class="sxs-lookup"><span data-stu-id="b3c2b-135">System.String</span></span>

## <span data-ttu-id="b3c2b-136">輸出</span><span class="sxs-lookup"><span data-stu-id="b3c2b-136">OUTPUTS</span></span>

### <span data-ttu-id="b3c2b-137">PSConnectionMonitorResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b3c2b-137">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="b3c2b-138">筆記</span><span class="sxs-lookup"><span data-stu-id="b3c2b-138">NOTES</span></span>
<span data-ttu-id="b3c2b-139">關鍵字： azure，azurerm，arm，資源，連線，管理，管理員，網路，網路，網路觀察程式，連線監視器</span><span class="sxs-lookup"><span data-stu-id="b3c2b-139">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="b3c2b-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="b3c2b-140">RELATED LINKS</span></span>

[<span data-ttu-id="b3c2b-141">新-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b3c2b-141">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="b3c2b-142">AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b3c2b-142">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="b3c2b-143">移除-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b3c2b-143">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="b3c2b-144">AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="b3c2b-144">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="b3c2b-145">AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="b3c2b-145">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="b3c2b-146">AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="b3c2b-146">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="b3c2b-147">AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="b3c2b-147">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="b3c2b-148">新-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b3c2b-148">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="b3c2b-149">新-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="b3c2b-149">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="b3c2b-150">AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b3c2b-150">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="b3c2b-151">移除-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b3c2b-151">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="b3c2b-152">停止 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b3c2b-152">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="b3c2b-153">AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b3c2b-153">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="b3c2b-154">AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="b3c2b-154">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="b3c2b-155">移除-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b3c2b-155">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="b3c2b-156">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b3c2b-156">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="b3c2b-157">停止 AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b3c2b-157">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="b3c2b-158">新-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b3c2b-158">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="b3c2b-159">新-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="b3c2b-159">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>]()

[<span data-ttu-id="b3c2b-160">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="b3c2b-160">Test-AzureRmNetworkWatcherIPFlow</span></span>]()

[<span data-ttu-id="b3c2b-161">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="b3c2b-161">Test-AzureRmNetworkWatcherConnectivity</span></span>]()

[<span data-ttu-id="b3c2b-162">開始-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="b3c2b-162">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>]()

[<span data-ttu-id="b3c2b-163">開始-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b3c2b-163">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="b3c2b-164">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="b3c2b-164">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>]()

[<span data-ttu-id="b3c2b-165">AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="b3c2b-165">Get-AzureRMNetworkWatcherReachabilityReport</span></span>]()

[<span data-ttu-id="b3c2b-166">AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="b3c2b-166">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>]()

[<span data-ttu-id="b3c2b-167">AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="b3c2b-167">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>]()
