---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: ec7f6f910a50f479a923451fb9b893a5cabb5301
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789297"
---
# <span data-ttu-id="ef702-101">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ef702-101">New-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="ef702-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ef702-102">SYNOPSIS</span></span>
<span data-ttu-id="ef702-103">建立連接監視器。</span><span class="sxs-lookup"><span data-stu-id="ef702-103">Creates a connection monitor.</span></span>

## <span data-ttu-id="ef702-104">句法</span><span class="sxs-lookup"><span data-stu-id="ef702-104">SYNTAX</span></span>

### <span data-ttu-id="ef702-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="ef702-105">SetByName (Default)</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ef702-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="ef702-106">SetByResource</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ef702-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="ef702-107">SetByLocation</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef702-108">說明</span><span class="sxs-lookup"><span data-stu-id="ef702-108">DESCRIPTION</span></span>
<span data-ttu-id="ef702-109">New-AzNetworkWatcherConnectionMonitor Cmdlet 會為指定的來源和目的地建立連接監視器。</span><span class="sxs-lookup"><span data-stu-id="ef702-109">The New-AzNetworkWatcherConnectionMonitor cmdlet creates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="ef702-110">示例</span><span class="sxs-lookup"><span data-stu-id="ef702-110">EXAMPLES</span></span>

### <span data-ttu-id="ef702-111">範例1：建立 vm 和網際網路目的地的連線監視器</span><span class="sxs-lookup"><span data-stu-id="ef702-111">Example 1: Create a connection monitor for a vm and internet destination</span></span>
```
PS C:\> New-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm -DestinationAddress bing.com -DestinationPort 80

Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/t1
Etag                        : W/"e86b28cf-b907-4475-a8b7-34d310367694"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000
                                00000/resourceGroups/RgCentralUSEUAP/providers/Microsoft
                                .Compute/virtualMachines/vm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "bing.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:13:11 PM
MonitoringStatus            : Running
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {}
```

<span data-ttu-id="ef702-112">New-AzNetworkWatcherConnectionMonitor Cmdlet 會為指定的來源和目的地建立連接監視器。</span><span class="sxs-lookup"><span data-stu-id="ef702-112">The New-AzNetworkWatcherConnectionMonitor cmdlet creates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="ef702-113">參數</span><span class="sxs-lookup"><span data-stu-id="ef702-113">PARAMETERS</span></span>

### <span data-ttu-id="ef702-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ef702-114">-AsJob</span></span>
<span data-ttu-id="ef702-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ef702-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef702-116">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="ef702-116">-ConfigureOnly</span></span>
<span data-ttu-id="ef702-117">設定連接監視器，但不啟動</span><span class="sxs-lookup"><span data-stu-id="ef702-117">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="ef702-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef702-118">-DefaultProfile</span></span>
<span data-ttu-id="ef702-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ef702-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef702-120">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="ef702-120">-DestinationAddress</span></span>
<span data-ttu-id="ef702-121">連線監視者目的地的 Ip 位址。</span><span class="sxs-lookup"><span data-stu-id="ef702-121">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="ef702-122">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="ef702-122">-DestinationPort</span></span>
<span data-ttu-id="ef702-123">[目的地埠]。</span><span class="sxs-lookup"><span data-stu-id="ef702-123">Destination port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef702-124">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="ef702-124">-DestinationResourceId</span></span>
<span data-ttu-id="ef702-125">連線監視者目的地的 ID。</span><span class="sxs-lookup"><span data-stu-id="ef702-125">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="ef702-126">-Force</span><span class="sxs-lookup"><span data-stu-id="ef702-126">-Force</span></span>
<span data-ttu-id="ef702-127">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="ef702-127">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef702-128">-位置</span><span class="sxs-lookup"><span data-stu-id="ef702-128">-Location</span></span>
<span data-ttu-id="ef702-129">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="ef702-129">Location of the network watcher.</span></span>

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

### <span data-ttu-id="ef702-130">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="ef702-130">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="ef702-131">監控間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="ef702-131">Monitoring interval in seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef702-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="ef702-132">-Name</span></span>
<span data-ttu-id="ef702-133">[連接監視器] 名稱。</span><span class="sxs-lookup"><span data-stu-id="ef702-133">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef702-134">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ef702-134">-NetworkWatcher</span></span>
<span data-ttu-id="ef702-135">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="ef702-135">The network watcher resource.</span></span>

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

### <span data-ttu-id="ef702-136">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="ef702-136">-NetworkWatcherName</span></span>
<span data-ttu-id="ef702-137">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="ef702-137">The name of network watcher.</span></span>

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

### <span data-ttu-id="ef702-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef702-138">-ResourceGroupName</span></span>
<span data-ttu-id="ef702-139">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ef702-139">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="ef702-140">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="ef702-140">-SourcePort</span></span>
<span data-ttu-id="ef702-141">來源埠。</span><span class="sxs-lookup"><span data-stu-id="ef702-141">Source port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef702-142">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="ef702-142">-SourceResourceId</span></span>
<span data-ttu-id="ef702-143">連線監視來源的 ID。</span><span class="sxs-lookup"><span data-stu-id="ef702-143">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="ef702-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="ef702-144">-Tag</span></span>
<span data-ttu-id="ef702-145">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="ef702-145">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef702-146">-確認</span><span class="sxs-lookup"><span data-stu-id="ef702-146">-Confirm</span></span>
<span data-ttu-id="ef702-147">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ef702-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef702-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef702-148">-WhatIf</span></span>
<span data-ttu-id="ef702-149">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ef702-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef702-150">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ef702-150">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef702-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef702-151">CommonParameters</span></span>
<span data-ttu-id="ef702-152">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ef702-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef702-153">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ef702-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef702-154">輸入</span><span class="sxs-lookup"><span data-stu-id="ef702-154">INPUTS</span></span>

### <span data-ttu-id="ef702-155">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ef702-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="ef702-156">輸出</span><span class="sxs-lookup"><span data-stu-id="ef702-156">OUTPUTS</span></span>

### <span data-ttu-id="ef702-157">PSConnectionMonitorResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ef702-157">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="ef702-158">筆記</span><span class="sxs-lookup"><span data-stu-id="ef702-158">NOTES</span></span>
<span data-ttu-id="ef702-159">關鍵字： azure，azurerm，arm，資源，連線，管理，管理員，網路，網路，網路觀察程式，連線監視器</span><span class="sxs-lookup"><span data-stu-id="ef702-159">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="ef702-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="ef702-160">RELATED LINKS</span></span>

[<span data-ttu-id="ef702-161">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ef702-161">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="ef702-162">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ef702-162">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="ef702-163">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ef702-163">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="ef702-164">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="ef702-164">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="ef702-165">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="ef702-165">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="ef702-166">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="ef702-166">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="ef702-167">AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="ef702-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="ef702-168">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ef702-168">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ef702-169">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="ef702-169">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="ef702-170">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ef702-170">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ef702-171">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ef702-171">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ef702-172">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ef702-172">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ef702-173">AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ef702-173">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ef702-174">AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="ef702-174">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="ef702-175">移除-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ef702-175">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ef702-176">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ef702-176">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ef702-177">停止 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ef702-177">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ef702-178">新-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ef702-178">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ef702-179">新-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="ef702-179">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="ef702-180">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="ef702-180">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="ef702-181">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="ef702-181">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="ef702-182">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="ef702-182">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="ef702-183">開始-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ef702-183">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ef702-184">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="ef702-184">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="ef702-185">AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="ef702-185">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="ef702-186">AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="ef702-186">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="ef702-187">AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="ef702-187">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)
