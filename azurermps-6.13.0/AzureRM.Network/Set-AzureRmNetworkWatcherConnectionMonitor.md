---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 5c7709c234ba762e5b87418cc0e9b3fc4637ac11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624369"
---
# <span data-ttu-id="f6550-101">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f6550-101">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="f6550-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f6550-102">SYNOPSIS</span></span>
<span data-ttu-id="f6550-103">更新連接監視器。</span><span class="sxs-lookup"><span data-stu-id="f6550-103">Update a connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6550-104">句法</span><span class="sxs-lookup"><span data-stu-id="f6550-104">SYNTAX</span></span>

### <span data-ttu-id="f6550-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="f6550-105">SetByName (Default)</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f6550-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f6550-106">SetByResource</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f6550-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="f6550-107">SetByLocation</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6550-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f6550-108">SetByResourceId</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6550-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="f6550-109">SetByInputObject</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6550-110">說明</span><span class="sxs-lookup"><span data-stu-id="f6550-110">DESCRIPTION</span></span>
<span data-ttu-id="f6550-111">Set-AzureRmNetworkWatcherConnectionMonitor Cmdlet 會更新指定的連接監視器。</span><span class="sxs-lookup"><span data-stu-id="f6550-111">The Set-AzureRmNetworkWatcherConnectionMonitor cmdlet updates the specified connection monitor.</span></span>

## <span data-ttu-id="f6550-112">示例</span><span class="sxs-lookup"><span data-stu-id="f6550-112">EXAMPLES</span></span>

### <span data-ttu-id="f6550-113">範例1：更新連線監視者</span><span class="sxs-lookup"><span data-stu-id="f6550-113">Example 1: Update a connection monitor</span></span>
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

<span data-ttu-id="f6550-114">在這個範例中，我們會透過變更 destinationAddress 及新增標籤來更新現有的連線監視器。</span><span class="sxs-lookup"><span data-stu-id="f6550-114">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="f6550-115">參數</span><span class="sxs-lookup"><span data-stu-id="f6550-115">PARAMETERS</span></span>

### <span data-ttu-id="f6550-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f6550-116">-AsJob</span></span>
<span data-ttu-id="f6550-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f6550-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f6550-118">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="f6550-118">-ConfigureOnly</span></span>
<span data-ttu-id="f6550-119">設定連接監視器，但不啟動</span><span class="sxs-lookup"><span data-stu-id="f6550-119">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="f6550-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6550-120">-DefaultProfile</span></span>
<span data-ttu-id="f6550-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f6550-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6550-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="f6550-122">-DestinationAddress</span></span>
<span data-ttu-id="f6550-123">連線監視者目的地的 Ip 位址。</span><span class="sxs-lookup"><span data-stu-id="f6550-123">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="f6550-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="f6550-124">-DestinationPort</span></span>
<span data-ttu-id="f6550-125">[目的地埠]。</span><span class="sxs-lookup"><span data-stu-id="f6550-125">Destination port.</span></span>

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

### <span data-ttu-id="f6550-126">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="f6550-126">-DestinationResourceId</span></span>
<span data-ttu-id="f6550-127">連線監視者目的地的 ID。</span><span class="sxs-lookup"><span data-stu-id="f6550-127">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="f6550-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f6550-128">-InputObject</span></span>
<span data-ttu-id="f6550-129">[連接監視器] 物件。</span><span class="sxs-lookup"><span data-stu-id="f6550-129">Connection monitor object.</span></span>

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

### <span data-ttu-id="f6550-130">-位置</span><span class="sxs-lookup"><span data-stu-id="f6550-130">-Location</span></span>
<span data-ttu-id="f6550-131">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="f6550-131">Location of the network watcher.</span></span>

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

### <span data-ttu-id="f6550-132">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="f6550-132">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="f6550-133">監控間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="f6550-133">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="f6550-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="f6550-134">-Name</span></span>
<span data-ttu-id="f6550-135">[連接監視器] 名稱。</span><span class="sxs-lookup"><span data-stu-id="f6550-135">The connection monitor name.</span></span>

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

### <span data-ttu-id="f6550-136">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f6550-136">-NetworkWatcher</span></span>
<span data-ttu-id="f6550-137">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="f6550-137">The network watcher resource.</span></span>

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

### <span data-ttu-id="f6550-138">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="f6550-138">-NetworkWatcherName</span></span>
<span data-ttu-id="f6550-139">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6550-139">The name of network watcher.</span></span>

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

### <span data-ttu-id="f6550-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6550-140">-ResourceGroupName</span></span>
<span data-ttu-id="f6550-141">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6550-141">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="f6550-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f6550-142">-ResourceId</span></span>
<span data-ttu-id="f6550-143">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="f6550-143">Resource ID.</span></span>

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

### <span data-ttu-id="f6550-144">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="f6550-144">-SourcePort</span></span>
<span data-ttu-id="f6550-145">來源埠。</span><span class="sxs-lookup"><span data-stu-id="f6550-145">Source port.</span></span>

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

### <span data-ttu-id="f6550-146">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="f6550-146">-SourceResourceId</span></span>
<span data-ttu-id="f6550-147">連線監視來源的 ID。</span><span class="sxs-lookup"><span data-stu-id="f6550-147">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="f6550-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="f6550-148">-Tag</span></span>
<span data-ttu-id="f6550-149">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="f6550-149">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="f6550-150">-確認</span><span class="sxs-lookup"><span data-stu-id="f6550-150">-Confirm</span></span>
<span data-ttu-id="f6550-151">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f6550-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6550-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6550-152">-WhatIf</span></span>
<span data-ttu-id="f6550-153">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f6550-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6550-154">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f6550-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6550-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6550-155">CommonParameters</span></span>
<span data-ttu-id="f6550-156">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f6550-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6550-157">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f6550-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6550-158">輸入</span><span class="sxs-lookup"><span data-stu-id="f6550-158">INPUTS</span></span>

### <span data-ttu-id="f6550-159">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f6550-159">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="f6550-160">參數： NetworkWatcher (ByValue) </span><span class="sxs-lookup"><span data-stu-id="f6550-160">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="f6550-161">System.object</span><span class="sxs-lookup"><span data-stu-id="f6550-161">System.String</span></span>

### <span data-ttu-id="f6550-162">PSConnectionMonitorResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f6550-162">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>
<span data-ttu-id="f6550-163">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="f6550-163">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="f6550-164">輸出</span><span class="sxs-lookup"><span data-stu-id="f6550-164">OUTPUTS</span></span>

### <span data-ttu-id="f6550-165">PSConnectionMonitorResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f6550-165">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="f6550-166">筆記</span><span class="sxs-lookup"><span data-stu-id="f6550-166">NOTES</span></span>
<span data-ttu-id="f6550-167">關鍵字： azure，azurerm，arm，資源，連線，管理，管理員，網路，網路，網路觀察程式，連線監視器</span><span class="sxs-lookup"><span data-stu-id="f6550-167">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="f6550-168">相關連結</span><span class="sxs-lookup"><span data-stu-id="f6550-168">RELATED LINKS</span></span>

[<span data-ttu-id="f6550-169">新-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f6550-169">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="f6550-170">AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f6550-170">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="f6550-171">移除-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f6550-171">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="f6550-172">AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="f6550-172">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="f6550-173">AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="f6550-173">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="f6550-174">AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="f6550-174">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="f6550-175">AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="f6550-175">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="f6550-176">新-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f6550-176">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="f6550-177">新-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="f6550-177">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="f6550-178">AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f6550-178">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="f6550-179">移除-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f6550-179">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="f6550-180">停止 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f6550-180">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="f6550-181">AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f6550-181">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="f6550-182">AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="f6550-182">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="f6550-183">移除-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f6550-183">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="f6550-184">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f6550-184">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="f6550-185">停止 AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f6550-185">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="f6550-186">新-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f6550-186">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="f6550-187">新-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="f6550-187">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>]()

[<span data-ttu-id="f6550-188">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="f6550-188">Test-AzureRmNetworkWatcherIPFlow</span></span>]()

[<span data-ttu-id="f6550-189">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="f6550-189">Test-AzureRmNetworkWatcherConnectivity</span></span>]()

[<span data-ttu-id="f6550-190">開始-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="f6550-190">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>]()

[<span data-ttu-id="f6550-191">開始-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f6550-191">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="f6550-192">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="f6550-192">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>]()

[<span data-ttu-id="f6550-193">AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="f6550-193">Get-AzureRMNetworkWatcherReachabilityReport</span></span>]()

[<span data-ttu-id="f6550-194">AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="f6550-194">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>]()

[<span data-ttu-id="f6550-195">AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="f6550-195">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>]()
