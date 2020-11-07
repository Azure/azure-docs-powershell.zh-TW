---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 44f81008b0693a4ff14a80a818e9d2514dfe0ebf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625612"
---
# <span data-ttu-id="e369d-101">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e369d-101">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="e369d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e369d-102">SYNOPSIS</span></span>
<span data-ttu-id="e369d-103">更新連接監視器。</span><span class="sxs-lookup"><span data-stu-id="e369d-103">Update a connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e369d-104">句法</span><span class="sxs-lookup"><span data-stu-id="e369d-104">SYNTAX</span></span>

### <span data-ttu-id="e369d-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="e369d-105">SetByName (Default)</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e369d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e369d-106">SetByResource</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e369d-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="e369d-107">SetByLocation</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e369d-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e369d-108">SetByResourceId</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e369d-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="e369d-109">SetByInputObject</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e369d-110">說明</span><span class="sxs-lookup"><span data-stu-id="e369d-110">DESCRIPTION</span></span>
<span data-ttu-id="e369d-111">Set-AzureRmNetworkWatcherConnectionMonitor Cmdlet 會更新指定的連接監視器。</span><span class="sxs-lookup"><span data-stu-id="e369d-111">The Set-AzureRmNetworkWatcherConnectionMonitor cmdlet updates the specified connection monitor.</span></span>

## <span data-ttu-id="e369d-112">示例</span><span class="sxs-lookup"><span data-stu-id="e369d-112">EXAMPLES</span></span>

### <span data-ttu-id="e369d-113">範例1：更新連線監視者</span><span class="sxs-lookup"><span data-stu-id="e369d-113">Example 1: Update a connection monitor</span></span>
```
PS C:\> Set-AzureRmNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm 
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

<span data-ttu-id="e369d-114">在這個範例中，我們會透過變更 destinationAddress 及新增標籤來更新現有的連線監視器。</span><span class="sxs-lookup"><span data-stu-id="e369d-114">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="e369d-115">參數</span><span class="sxs-lookup"><span data-stu-id="e369d-115">PARAMETERS</span></span>

### <span data-ttu-id="e369d-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e369d-116">-AsJob</span></span>
<span data-ttu-id="e369d-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e369d-117">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e369d-118">-確認</span><span class="sxs-lookup"><span data-stu-id="e369d-118">-Confirm</span></span>
<span data-ttu-id="e369d-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e369d-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e369d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e369d-120">-DefaultProfile</span></span>
<span data-ttu-id="e369d-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e369d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e369d-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="e369d-122">-DestinationAddress</span></span>
<span data-ttu-id="e369d-123">連線監視者目的地的 Ip 位址。</span><span class="sxs-lookup"><span data-stu-id="e369d-123">The Ip address of the connection monitor destination.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e369d-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="e369d-124">-DestinationPort</span></span>
<span data-ttu-id="e369d-125">[目的地埠]。</span><span class="sxs-lookup"><span data-stu-id="e369d-125">Destination port.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e369d-126">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="e369d-126">-DestinationResourceId</span></span>
<span data-ttu-id="e369d-127">連線監視者目的地的 ID。</span><span class="sxs-lookup"><span data-stu-id="e369d-127">The ID of the connection monitor destination.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e369d-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e369d-128">-InputObject</span></span>
<span data-ttu-id="e369d-129">[連接監視器] 物件。</span><span class="sxs-lookup"><span data-stu-id="e369d-129">Connection monitor object.</span></span>

```yaml
Type: PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e369d-130">-位置</span><span class="sxs-lookup"><span data-stu-id="e369d-130">-Location</span></span>
<span data-ttu-id="e369d-131">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="e369d-131">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e369d-132">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="e369d-132">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="e369d-133">監控間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="e369d-133">Monitoring interval in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e369d-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="e369d-134">-Name</span></span>
<span data-ttu-id="e369d-135">[連接監視器] 名稱。</span><span class="sxs-lookup"><span data-stu-id="e369d-135">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e369d-136">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e369d-136">-NetworkWatcher</span></span>
<span data-ttu-id="e369d-137">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="e369d-137">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e369d-138">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="e369d-138">-NetworkWatcherName</span></span>
<span data-ttu-id="e369d-139">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="e369d-139">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e369d-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e369d-140">-ResourceGroupName</span></span>
<span data-ttu-id="e369d-141">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e369d-141">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e369d-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e369d-142">-ResourceId</span></span>
<span data-ttu-id="e369d-143">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="e369d-143">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e369d-144">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="e369d-144">-SourcePort</span></span>
<span data-ttu-id="e369d-145">來源埠。</span><span class="sxs-lookup"><span data-stu-id="e369d-145">Source port.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e369d-146">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="e369d-146">-SourceResourceId</span></span>
<span data-ttu-id="e369d-147">連線監視來源的 ID。</span><span class="sxs-lookup"><span data-stu-id="e369d-147">The ID of the connection monitor source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e369d-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="e369d-148">-Tag</span></span>
<span data-ttu-id="e369d-149">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="e369d-149">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e369d-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e369d-150">-WhatIf</span></span>
<span data-ttu-id="e369d-151">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e369d-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e369d-152">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e369d-152">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e369d-153">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="e369d-153">-ConfigureOnly</span></span>
<span data-ttu-id="e369d-154">設定連接監視器，但不啟動</span><span class="sxs-lookup"><span data-stu-id="e369d-154">Configure connection monitor, but do not start it</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e369d-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e369d-155">CommonParameters</span></span>
<span data-ttu-id="e369d-156">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e369d-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e369d-157">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e369d-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e369d-158">輸入</span><span class="sxs-lookup"><span data-stu-id="e369d-158">INPUTS</span></span>

### <span data-ttu-id="e369d-159">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e369d-159">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="e369d-160">PSConnectionMonitorResult 中的 [system.object] 命令。</span><span class="sxs-lookup"><span data-stu-id="e369d-160">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="e369d-161">輸出</span><span class="sxs-lookup"><span data-stu-id="e369d-161">OUTPUTS</span></span>

### <span data-ttu-id="e369d-162">PSConnectionMonitorResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e369d-162">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="e369d-163">筆記</span><span class="sxs-lookup"><span data-stu-id="e369d-163">NOTES</span></span>
<span data-ttu-id="e369d-164">關鍵字： azure，azurerm，arm，資源，連線，管理，管理員，網路，網路，網路觀察程式，連線監視器</span><span class="sxs-lookup"><span data-stu-id="e369d-164">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="e369d-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="e369d-165">RELATED LINKS</span></span>

[<span data-ttu-id="e369d-166">新-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e369d-166">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="e369d-167">AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e369d-167">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="e369d-168">移除-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e369d-168">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="e369d-169">AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="e369d-169">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="e369d-170">AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="e369d-170">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="e369d-171">AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="e369d-171">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="e369d-172">AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="e369d-172">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="e369d-173">新-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e369d-173">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="e369d-174">新-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="e369d-174">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="e369d-175">AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e369d-175">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="e369d-176">移除-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e369d-176">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="e369d-177">停止 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e369d-177">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="e369d-178">AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e369d-178">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="e369d-179">AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="e369d-179">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="e369d-180">移除-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e369d-180">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="e369d-181">開始-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e369d-181">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="e369d-182">停止 AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e369d-182">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="e369d-183">新-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e369d-183">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()
