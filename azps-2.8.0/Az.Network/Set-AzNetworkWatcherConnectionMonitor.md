---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 7e3836f2c546c5ba3ad2ee4a2845e7c813601dda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791610"
---
# <span data-ttu-id="2f749-101">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2f749-101">Set-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="2f749-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2f749-102">SYNOPSIS</span></span>
<span data-ttu-id="2f749-103">更新連接監視器。</span><span class="sxs-lookup"><span data-stu-id="2f749-103">Update a connection monitor.</span></span>

## <span data-ttu-id="2f749-104">句法</span><span class="sxs-lookup"><span data-stu-id="2f749-104">SYNTAX</span></span>

### <span data-ttu-id="2f749-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="2f749-105">SetByName (Default)</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2f749-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="2f749-106">SetByResource</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2f749-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="2f749-107">SetByLocation</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f749-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2f749-108">SetByResourceId</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f749-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="2f749-109">SetByInputObject</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f749-110">說明</span><span class="sxs-lookup"><span data-stu-id="2f749-110">DESCRIPTION</span></span>
<span data-ttu-id="2f749-111">Set-AzNetworkWatcherConnectionMonitor Cmdlet 會更新指定的連接監視器。</span><span class="sxs-lookup"><span data-stu-id="2f749-111">The Set-AzNetworkWatcherConnectionMonitor cmdlet updates the specified connection monitor.</span></span>

## <span data-ttu-id="2f749-112">示例</span><span class="sxs-lookup"><span data-stu-id="2f749-112">EXAMPLES</span></span>

### <span data-ttu-id="2f749-113">範例1：更新連線監視者</span><span class="sxs-lookup"><span data-stu-id="2f749-113">Example 1: Update a connection monitor</span></span>
```
PS C:\> Set-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm
-DestinationAddress google.com -DestinationPort 80 -Tag @{"key1" = "value1"}

Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/cm
Etag                        : W/"5b2b20e8-0ce0-417e-9607-76208149bb67"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000
                                00000/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMach
                                ines/vm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "google.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:19:28 PM
MonitoringStatus            : Running
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {
                                "key1": "value1"
                              }
```

<span data-ttu-id="2f749-114">在這個範例中，我們會透過變更 destinationAddress 及新增標籤來更新現有的連線監視器。</span><span class="sxs-lookup"><span data-stu-id="2f749-114">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="2f749-115">參數</span><span class="sxs-lookup"><span data-stu-id="2f749-115">PARAMETERS</span></span>

### <span data-ttu-id="2f749-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2f749-116">-AsJob</span></span>
<span data-ttu-id="2f749-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2f749-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2f749-118">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="2f749-118">-ConfigureOnly</span></span>
<span data-ttu-id="2f749-119">設定連接監視器，但不啟動</span><span class="sxs-lookup"><span data-stu-id="2f749-119">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="2f749-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f749-120">-DefaultProfile</span></span>
<span data-ttu-id="2f749-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2f749-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f749-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="2f749-122">-DestinationAddress</span></span>
<span data-ttu-id="2f749-123">連線監視者目的地的 Ip 位址。</span><span class="sxs-lookup"><span data-stu-id="2f749-123">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="2f749-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="2f749-124">-DestinationPort</span></span>
<span data-ttu-id="2f749-125">[目的地埠]。</span><span class="sxs-lookup"><span data-stu-id="2f749-125">Destination port.</span></span>

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

### <span data-ttu-id="2f749-126">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="2f749-126">-DestinationResourceId</span></span>
<span data-ttu-id="2f749-127">連線監視者目的地的 ID。</span><span class="sxs-lookup"><span data-stu-id="2f749-127">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="2f749-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f749-128">-InputObject</span></span>
<span data-ttu-id="2f749-129">[連接監視器] 物件。</span><span class="sxs-lookup"><span data-stu-id="2f749-129">Connection monitor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f749-130">-位置</span><span class="sxs-lookup"><span data-stu-id="2f749-130">-Location</span></span>
<span data-ttu-id="2f749-131">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="2f749-131">Location of the network watcher.</span></span>

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

### <span data-ttu-id="2f749-132">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="2f749-132">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="2f749-133">監控間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="2f749-133">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="2f749-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="2f749-134">-Name</span></span>
<span data-ttu-id="2f749-135">[連接監視器] 名稱。</span><span class="sxs-lookup"><span data-stu-id="2f749-135">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f749-136">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2f749-136">-NetworkWatcher</span></span>
<span data-ttu-id="2f749-137">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="2f749-137">The network watcher resource.</span></span>

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

### <span data-ttu-id="2f749-138">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="2f749-138">-NetworkWatcherName</span></span>
<span data-ttu-id="2f749-139">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f749-139">The name of network watcher.</span></span>

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

### <span data-ttu-id="2f749-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f749-140">-ResourceGroupName</span></span>
<span data-ttu-id="2f749-141">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f749-141">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="2f749-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f749-142">-ResourceId</span></span>
<span data-ttu-id="2f749-143">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="2f749-143">Resource ID.</span></span>

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

### <span data-ttu-id="2f749-144">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="2f749-144">-SourcePort</span></span>
<span data-ttu-id="2f749-145">來源埠。</span><span class="sxs-lookup"><span data-stu-id="2f749-145">Source port.</span></span>

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

### <span data-ttu-id="2f749-146">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="2f749-146">-SourceResourceId</span></span>
<span data-ttu-id="2f749-147">連線監視來源的 ID。</span><span class="sxs-lookup"><span data-stu-id="2f749-147">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="2f749-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="2f749-148">-Tag</span></span>
<span data-ttu-id="2f749-149">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="2f749-149">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="2f749-150">-確認</span><span class="sxs-lookup"><span data-stu-id="2f749-150">-Confirm</span></span>
<span data-ttu-id="2f749-151">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2f749-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f749-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f749-152">-WhatIf</span></span>
<span data-ttu-id="2f749-153">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2f749-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f749-154">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2f749-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f749-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f749-155">CommonParameters</span></span>
<span data-ttu-id="2f749-156">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2f749-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f749-157">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2f749-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f749-158">輸入</span><span class="sxs-lookup"><span data-stu-id="2f749-158">INPUTS</span></span>

### <span data-ttu-id="2f749-159">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2f749-159">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="2f749-160">System.object</span><span class="sxs-lookup"><span data-stu-id="2f749-160">System.String</span></span>

### <span data-ttu-id="2f749-161">PSConnectionMonitorResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2f749-161">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="2f749-162">輸出</span><span class="sxs-lookup"><span data-stu-id="2f749-162">OUTPUTS</span></span>

### <span data-ttu-id="2f749-163">PSConnectionMonitorResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2f749-163">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="2f749-164">筆記</span><span class="sxs-lookup"><span data-stu-id="2f749-164">NOTES</span></span>
<span data-ttu-id="2f749-165">關鍵字： azure，azurerm，arm，資源，連線，管理，管理員，網路，網路，網路觀察程式，連線監視器</span><span class="sxs-lookup"><span data-stu-id="2f749-165">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="2f749-166">相關連結</span><span class="sxs-lookup"><span data-stu-id="2f749-166">RELATED LINKS</span></span>

[<span data-ttu-id="2f749-167">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2f749-167">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="2f749-168">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2f749-168">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="2f749-169">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2f749-169">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="2f749-170">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="2f749-170">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="2f749-171">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="2f749-171">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="2f749-172">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="2f749-172">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="2f749-173">AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="2f749-173">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="2f749-174">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2f749-174">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2f749-175">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="2f749-175">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="2f749-176">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2f749-176">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2f749-177">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2f749-177">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2f749-178">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2f749-178">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2f749-179">AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2f749-179">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2f749-180">AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="2f749-180">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="2f749-181">移除-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2f749-181">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2f749-182">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2f749-182">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2f749-183">停止 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2f749-183">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2f749-184">新-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2f749-184">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2f749-185">新-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="2f749-185">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="2f749-186">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="2f749-186">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="2f749-187">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="2f749-187">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="2f749-188">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="2f749-188">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="2f749-189">開始-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2f749-189">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2f749-190">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="2f749-190">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="2f749-191">AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="2f749-191">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="2f749-192">AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="2f749-192">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="2f749-193">AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="2f749-193">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)
