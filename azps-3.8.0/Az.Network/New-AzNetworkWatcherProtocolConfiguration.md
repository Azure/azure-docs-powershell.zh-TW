---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherprotocolconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherProtocolConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherProtocolConfiguration.md
ms.openlocfilehash: 5358fa9898bca17f75c0111ef15b69e8cff4f75d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957777"
---
# <span data-ttu-id="e4175-101">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4175-101">New-AzNetworkWatcherProtocolConfiguration</span></span>

## <span data-ttu-id="e4175-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e4175-102">SYNOPSIS</span></span>
<span data-ttu-id="e4175-103">建立新的通訊協定設定物件。</span><span class="sxs-lookup"><span data-stu-id="e4175-103">Creates a new protocol configuration object.</span></span>

## <span data-ttu-id="e4175-104">句法</span><span class="sxs-lookup"><span data-stu-id="e4175-104">SYNTAX</span></span>

```
New-AzNetworkWatcherProtocolConfiguration -Protocol <String> [-Method <String>] [-Header <IDictionary>]
 [-ValidStatusCode <Int32[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4175-105">說明</span><span class="sxs-lookup"><span data-stu-id="e4175-105">DESCRIPTION</span></span>
<span data-ttu-id="e4175-106">New-AzNetworkWatcherProtocolConfiguration Cmdlet 會建立新的通訊協定設定物件。</span><span class="sxs-lookup"><span data-stu-id="e4175-106">The New-AzNetworkWatcherProtocolConfiguration cmdlet creates a new protocol configuration object.</span></span> <span data-ttu-id="e4175-107">這個物件是用來在連線檢查會話期間使用指定準則來限制通訊協定設定。</span><span class="sxs-lookup"><span data-stu-id="e4175-107">This object is used to restrict the protocol configuration during a connectivity check session using the specified criteria.</span></span> 

## <span data-ttu-id="e4175-108">示例</span><span class="sxs-lookup"><span data-stu-id="e4175-108">EXAMPLES</span></span>

### <span data-ttu-id="e4175-109">範例1：使用通訊協定設定，測試從 VM 到網站的網路觀察程式連線能力</span><span class="sxs-lookup"><span data-stu-id="e4175-109">Example 1: Test Network Watcher Connectivity from a VM to a website with protocol configuration</span></span>
```
$config = New-AzNetworkWatcherProtocolConfiguration -Protocol Http -Method Get -Headers @{"accept"="application/json"} -ValidStatusCodes @(200,202,204)

Test-AzNetworkWatcherConnectivity -NetworkWatcherName NetworkWatcher -ResourceGroupName NetworkWatcherRG -SourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" -DestinationAddress "bing.com" -DestinationPort 80 -ProtocolConfiguration $config


ConnectionStatus : Reachable
AvgLatencyInMs   : 4
MinLatencyInMs   : 2
MaxLatencyInMs   : 15
ProbesSent       : 15
ProbesFailed     : 0
Hops             : [
                     {
                       "Type": "Source",
                       "Id": "f8cff464-e13f-457f-a09e-4dcd53d38a85",
                       "Address": "10.1.1.4",
                       "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/provi                   iders/Microsoft.Network/networkInterfaces/appNic0/ipConfigurations/ipconfig1",
                       "NextHopIds": [
                         "1034b1bf-0b1b-4f0a-93b2-900477f45485"
                       ],
                       "Issues": []
                     },
                     {
                       "Type": "Internet",
                       "Id": "1034b1bf-0b1b-4f0a-93b2-900477f45485",
                       "Address": "13.107.21.200",
                       "ResourceId": "Internet",
                       "NextHopIds": [],
                       "Issues": []
                     }
                   ]
```

<span data-ttu-id="e4175-110">在這個範例中，我們會測試 Azure 中 VM 的連線性與 www.bing.com。</span><span class="sxs-lookup"><span data-stu-id="e4175-110">In this example we test connectivity from a VM in Azure to www.bing.com.</span></span>

## <span data-ttu-id="e4175-111">參數</span><span class="sxs-lookup"><span data-stu-id="e4175-111">PARAMETERS</span></span>

### <span data-ttu-id="e4175-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4175-112">-DefaultProfile</span></span>
<span data-ttu-id="e4175-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e4175-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4175-114">-頁首</span><span class="sxs-lookup"><span data-stu-id="e4175-114">-Header</span></span>
<span data-ttu-id="e4175-115">HTTP 標頭清單</span><span class="sxs-lookup"><span data-stu-id="e4175-115">list of HTTP headers</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4175-116">-方法</span><span class="sxs-lookup"><span data-stu-id="e4175-116">-Method</span></span>
<span data-ttu-id="e4175-117">HTTP 方法</span><span class="sxs-lookup"><span data-stu-id="e4175-117">HTTP method</span></span>

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

### <span data-ttu-id="e4175-118">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="e4175-118">-Protocol</span></span>
<span data-ttu-id="e4175-119">通訊協定類型</span><span class="sxs-lookup"><span data-stu-id="e4175-119">Protocol type</span></span>

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

### <span data-ttu-id="e4175-120">-ValidStatusCode</span><span class="sxs-lookup"><span data-stu-id="e4175-120">-ValidStatusCode</span></span>
<span data-ttu-id="e4175-121">有效的狀態碼</span><span class="sxs-lookup"><span data-stu-id="e4175-121">valid status codes</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4175-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4175-122">CommonParameters</span></span>
<span data-ttu-id="e4175-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e4175-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4175-124">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e4175-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4175-125">輸入</span><span class="sxs-lookup"><span data-stu-id="e4175-125">INPUTS</span></span>

### <span data-ttu-id="e4175-126">所有</span><span class="sxs-lookup"><span data-stu-id="e4175-126">None</span></span>

## <span data-ttu-id="e4175-127">輸出</span><span class="sxs-lookup"><span data-stu-id="e4175-127">OUTPUTS</span></span>

### <span data-ttu-id="e4175-128">PSNetworkWatcherProtocolConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e4175-128">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherProtocolConfiguration</span></span>

## <span data-ttu-id="e4175-129">筆記</span><span class="sxs-lookup"><span data-stu-id="e4175-129">NOTES</span></span>
<span data-ttu-id="e4175-130">關鍵字： azure、azurerm、arm、資源、管理、管理員、網路、網路、觀察者、資料包、捕獲、流量、篩選器</span><span class="sxs-lookup"><span data-stu-id="e4175-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span>

## <span data-ttu-id="e4175-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="e4175-131">RELATED LINKS</span></span>

[<span data-ttu-id="e4175-132">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e4175-132">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="e4175-133">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e4175-133">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="e4175-134">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e4175-134">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="e4175-135">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="e4175-135">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="e4175-136">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="e4175-136">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="e4175-137">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="e4175-137">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="e4175-138">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="e4175-138">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="e4175-139">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e4175-139">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e4175-140">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="e4175-140">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="e4175-141">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e4175-141">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e4175-142">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e4175-142">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e4175-143">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e4175-143">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e4175-144">新-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4175-144">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="e4175-145">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="e4175-145">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="e4175-146">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="e4175-146">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="e4175-147">停止 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e4175-147">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e4175-148">開始-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e4175-148">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e4175-149">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e4175-149">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e4175-150">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="e4175-150">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="e4175-151">移除-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e4175-151">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e4175-152">新-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e4175-152">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e4175-153">AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="e4175-153">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="e4175-154">AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="e4175-154">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="e4175-155">AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="e4175-155">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="e4175-156">AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="e4175-156">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="e4175-157">AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="e4175-157">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="e4175-158">AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e4175-158">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
