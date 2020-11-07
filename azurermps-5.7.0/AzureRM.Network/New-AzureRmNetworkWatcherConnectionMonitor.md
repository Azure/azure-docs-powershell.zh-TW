---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: b8dd04fa4727465ee9b3be3eaf5e5e06a2243338
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625881"
---
# <span data-ttu-id="9e9d0-101">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9e9d0-101">New-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="9e9d0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9e9d0-102">SYNOPSIS</span></span>
<span data-ttu-id="9e9d0-103">建立連接監視器。</span><span class="sxs-lookup"><span data-stu-id="9e9d0-103">Creates a connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e9d0-104">句法</span><span class="sxs-lookup"><span data-stu-id="9e9d0-104">SYNTAX</span></span>

### <span data-ttu-id="9e9d0-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="9e9d0-105">SetByName (Default)</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9e9d0-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9e9d0-106">SetByResource</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9e9d0-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="9e9d0-107">SetByLocation</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e9d0-108">說明</span><span class="sxs-lookup"><span data-stu-id="9e9d0-108">DESCRIPTION</span></span>
<span data-ttu-id="9e9d0-109">New-AzureRmNetworkWatcherConnectionMonitor Cmdlet 會針對指定的來源和目的地 rcreates 連線監視器。</span><span class="sxs-lookup"><span data-stu-id="9e9d0-109">The New-AzureRmNetworkWatcherConnectionMonitor cmdlet rcreates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="9e9d0-110">示例</span><span class="sxs-lookup"><span data-stu-id="9e9d0-110">EXAMPLES</span></span>

### <span data-ttu-id="9e9d0-111">範例1：建立 vm 和網際網路目的地的連線監視器</span><span class="sxs-lookup"><span data-stu-id="9e9d0-111">Example 1: Create a connection monitor for a vm and internet destination</span></span>
```
PS C:\> New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm -DestinationAddress bing.com -DestinationPort 80

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

<span data-ttu-id="9e9d0-112">New-AzureRmNetworkWatcherConnectionMonitor Cmdlet 會為指定的來源和目的地建立連接監視器。</span><span class="sxs-lookup"><span data-stu-id="9e9d0-112">The New-AzureRmNetworkWatcherConnectionMonitor cmdlet creates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="9e9d0-113">參數</span><span class="sxs-lookup"><span data-stu-id="9e9d0-113">PARAMETERS</span></span>

### <span data-ttu-id="9e9d0-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9e9d0-114">-AsJob</span></span>
<span data-ttu-id="9e9d0-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9e9d0-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9e9d0-116">-確認</span><span class="sxs-lookup"><span data-stu-id="9e9d0-116">-Confirm</span></span>
<span data-ttu-id="9e9d0-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9e9d0-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e9d0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e9d0-118">-DefaultProfile</span></span>
<span data-ttu-id="9e9d0-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9e9d0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e9d0-120">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="9e9d0-120">-DestinationAddress</span></span>
<span data-ttu-id="9e9d0-121">連線監視者目的地的 Ip 位址。</span><span class="sxs-lookup"><span data-stu-id="9e9d0-121">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="9e9d0-122">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="9e9d0-122">-DestinationPort</span></span>
<span data-ttu-id="9e9d0-123">[目的地埠]。</span><span class="sxs-lookup"><span data-stu-id="9e9d0-123">Destination port.</span></span>

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

### <span data-ttu-id="9e9d0-124">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="9e9d0-124">-DestinationResourceId</span></span>
<span data-ttu-id="9e9d0-125">連線監視者目的地的 ID。</span><span class="sxs-lookup"><span data-stu-id="9e9d0-125">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="9e9d0-126">-Force</span><span class="sxs-lookup"><span data-stu-id="9e9d0-126">-Force</span></span>
<span data-ttu-id="9e9d0-127">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="9e9d0-127">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="9e9d0-128">-位置</span><span class="sxs-lookup"><span data-stu-id="9e9d0-128">-Location</span></span>
<span data-ttu-id="9e9d0-129">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="9e9d0-129">Location of the network watcher.</span></span>

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

### <span data-ttu-id="9e9d0-130">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="9e9d0-130">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="9e9d0-131">監控間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="9e9d0-131">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="9e9d0-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="9e9d0-132">-Name</span></span>
<span data-ttu-id="9e9d0-133">[連接監視器] 名稱。</span><span class="sxs-lookup"><span data-stu-id="9e9d0-133">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e9d0-134">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9e9d0-134">-NetworkWatcher</span></span>
<span data-ttu-id="9e9d0-135">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="9e9d0-135">The network watcher resource.</span></span>

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

### <span data-ttu-id="9e9d0-136">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="9e9d0-136">-NetworkWatcherName</span></span>
<span data-ttu-id="9e9d0-137">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="9e9d0-137">The name of network watcher.</span></span>

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

### <span data-ttu-id="9e9d0-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e9d0-138">-ResourceGroupName</span></span>
<span data-ttu-id="9e9d0-139">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9e9d0-139">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="9e9d0-140">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="9e9d0-140">-SourcePort</span></span>
<span data-ttu-id="9e9d0-141">來源埠。</span><span class="sxs-lookup"><span data-stu-id="9e9d0-141">Source port.</span></span>

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

### <span data-ttu-id="9e9d0-142">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="9e9d0-142">-SourceResourceId</span></span>
<span data-ttu-id="9e9d0-143">連線監視來源的 ID。</span><span class="sxs-lookup"><span data-stu-id="9e9d0-143">The ID of the connection monitor source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e9d0-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="9e9d0-144">-Tag</span></span>
<span data-ttu-id="9e9d0-145">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="9e9d0-145">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="9e9d0-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e9d0-146">-WhatIf</span></span>
<span data-ttu-id="9e9d0-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9e9d0-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e9d0-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9e9d0-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e9d0-149">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="9e9d0-149">-ConfigureOnly</span></span>
<span data-ttu-id="9e9d0-150">設定連接監視器，但不啟動</span><span class="sxs-lookup"><span data-stu-id="9e9d0-150">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="9e9d0-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e9d0-151">CommonParameters</span></span>
<span data-ttu-id="9e9d0-152">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9e9d0-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="9e9d0-153">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9e9d0-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e9d0-154">輸入</span><span class="sxs-lookup"><span data-stu-id="9e9d0-154">INPUTS</span></span>

### <span data-ttu-id="9e9d0-155">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9e9d0-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="9e9d0-156">System.object</span><span class="sxs-lookup"><span data-stu-id="9e9d0-156">System.String</span></span>

## <span data-ttu-id="9e9d0-157">輸出</span><span class="sxs-lookup"><span data-stu-id="9e9d0-157">OUTPUTS</span></span>

### <span data-ttu-id="9e9d0-158">PSConnectionMonitorResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9e9d0-158">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="9e9d0-159">筆記</span><span class="sxs-lookup"><span data-stu-id="9e9d0-159">NOTES</span></span>
<span data-ttu-id="9e9d0-160">關鍵字： azure，azurerm，arm，資源，連線，管理，管理員，網路，網路，網路觀察程式，連線監視器</span><span class="sxs-lookup"><span data-stu-id="9e9d0-160">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="9e9d0-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="9e9d0-161">RELATED LINKS</span></span>

[<span data-ttu-id="9e9d0-162">新-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9e9d0-162">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="9e9d0-163">AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9e9d0-163">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="9e9d0-164">移除-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9e9d0-164">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="9e9d0-165">AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="9e9d0-165">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="9e9d0-166">AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="9e9d0-166">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="9e9d0-167">AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="9e9d0-167">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="9e9d0-168">AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="9e9d0-168">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="9e9d0-169">新-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9e9d0-169">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="9e9d0-170">新-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="9e9d0-170">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="9e9d0-171">AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9e9d0-171">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="9e9d0-172">移除-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9e9d0-172">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="9e9d0-173">停止 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9e9d0-173">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="9e9d0-174">AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9e9d0-174">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="9e9d0-175">AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="9e9d0-175">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="9e9d0-176">移除-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9e9d0-176">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="9e9d0-177">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9e9d0-177">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="9e9d0-178">開始-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9e9d0-178">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="9e9d0-179">停止 AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9e9d0-179">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()
