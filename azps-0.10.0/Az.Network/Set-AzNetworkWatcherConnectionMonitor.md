---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 93c54df5cb0976aa0bd8f73881208c1966bbe9d0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795401"
---
# <span data-ttu-id="be068-101">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="be068-101">Set-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="be068-102">摘要</span><span class="sxs-lookup"><span data-stu-id="be068-102">SYNOPSIS</span></span>
<span data-ttu-id="be068-103">更新連接監視器。</span><span class="sxs-lookup"><span data-stu-id="be068-103">Update a connection monitor.</span></span>

## <span data-ttu-id="be068-104">句法</span><span class="sxs-lookup"><span data-stu-id="be068-104">SYNTAX</span></span>

### <span data-ttu-id="be068-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="be068-105">SetByResource (Default)</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="be068-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="be068-106">SetByName</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="be068-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="be068-107">SetByLocation</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="be068-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="be068-108">SetByResourceId</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="be068-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="be068-109">SetByInputObject</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="be068-110">說明</span><span class="sxs-lookup"><span data-stu-id="be068-110">DESCRIPTION</span></span>
<span data-ttu-id="be068-111">Set-AzNetworkWatcherConnectionMonitor Cmdlet 會更新指定的連接監視器。</span><span class="sxs-lookup"><span data-stu-id="be068-111">The Set-AzNetworkWatcherConnectionMonitor cmdlet updates the specified connection monitor.</span></span>

## <span data-ttu-id="be068-112">示例</span><span class="sxs-lookup"><span data-stu-id="be068-112">EXAMPLES</span></span>

### <span data-ttu-id="be068-113">---------------範例1：更新連線監視---------------</span><span class="sxs-lookup"><span data-stu-id="be068-113">---------------  Example 1: Update a connection monitor ---------------</span></span>
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

<span data-ttu-id="be068-114">在這個範例中，我們會透過變更 destinationAddress 及新增標籤來更新現有的連線監視器。</span><span class="sxs-lookup"><span data-stu-id="be068-114">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="be068-115">參數</span><span class="sxs-lookup"><span data-stu-id="be068-115">PARAMETERS</span></span>

### <span data-ttu-id="be068-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="be068-116">-AsJob</span></span>
<span data-ttu-id="be068-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="be068-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="be068-118">-AutoStart</span><span class="sxs-lookup"><span data-stu-id="be068-118">-AutoStart</span></span>
<span data-ttu-id="be068-119">自動啟動。</span><span class="sxs-lookup"><span data-stu-id="be068-119">Auto start.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be068-120">-確認</span><span class="sxs-lookup"><span data-stu-id="be068-120">-Confirm</span></span>
<span data-ttu-id="be068-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="be068-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be068-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be068-122">-DefaultProfile</span></span>
<span data-ttu-id="be068-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="be068-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be068-124">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="be068-124">-DestinationAddress</span></span>
<span data-ttu-id="be068-125">連線監視者目的地的 Ip 位址。</span><span class="sxs-lookup"><span data-stu-id="be068-125">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="be068-126">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="be068-126">-DestinationPort</span></span>
<span data-ttu-id="be068-127">[目的地埠]。</span><span class="sxs-lookup"><span data-stu-id="be068-127">Destination port.</span></span>

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

### <span data-ttu-id="be068-128">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="be068-128">-DestinationResourceId</span></span>
<span data-ttu-id="be068-129">連線監視者目的地的 ID。</span><span class="sxs-lookup"><span data-stu-id="be068-129">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="be068-130">-Force</span><span class="sxs-lookup"><span data-stu-id="be068-130">-Force</span></span>
<span data-ttu-id="be068-131">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="be068-131">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="be068-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="be068-132">-InputObject</span></span>
<span data-ttu-id="be068-133">[連接監視器] 物件。</span><span class="sxs-lookup"><span data-stu-id="be068-133">Connection monitor object.</span></span>

```yaml
Type: PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be068-134">-位置</span><span class="sxs-lookup"><span data-stu-id="be068-134">-Location</span></span>
<span data-ttu-id="be068-135">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="be068-135">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be068-136">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="be068-136">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="be068-137">監控間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="be068-137">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="be068-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="be068-138">-Name</span></span>
<span data-ttu-id="be068-139">[連接監視器] 名稱。</span><span class="sxs-lookup"><span data-stu-id="be068-139">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be068-140">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="be068-140">-NetworkWatcher</span></span>
<span data-ttu-id="be068-141">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="be068-141">The network watcher resource.</span></span>

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

### <span data-ttu-id="be068-142">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="be068-142">-NetworkWatcherName</span></span>
<span data-ttu-id="be068-143">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="be068-143">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be068-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be068-144">-ResourceGroupName</span></span>
<span data-ttu-id="be068-145">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="be068-145">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be068-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="be068-146">-ResourceId</span></span>
<span data-ttu-id="be068-147">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="be068-147">Resource ID.</span></span>

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

### <span data-ttu-id="be068-148">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="be068-148">-SourcePort</span></span>
<span data-ttu-id="be068-149">來源埠。</span><span class="sxs-lookup"><span data-stu-id="be068-149">Source port.</span></span>

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

### <span data-ttu-id="be068-150">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="be068-150">-SourceResourceId</span></span>
<span data-ttu-id="be068-151">連線監視來源的 ID。</span><span class="sxs-lookup"><span data-stu-id="be068-151">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="be068-152">-Tag</span><span class="sxs-lookup"><span data-stu-id="be068-152">-Tag</span></span>
<span data-ttu-id="be068-153">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="be068-153">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="be068-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be068-154">-WhatIf</span></span>
<span data-ttu-id="be068-155">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="be068-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be068-156">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="be068-156">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="be068-157">輸入</span><span class="sxs-lookup"><span data-stu-id="be068-157">INPUTS</span></span>

### <span data-ttu-id="be068-158">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="be068-158">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="be068-159">PSConnectionMonitorResult 中的 [system.object] 命令。</span><span class="sxs-lookup"><span data-stu-id="be068-159">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="be068-160">輸出</span><span class="sxs-lookup"><span data-stu-id="be068-160">OUTPUTS</span></span>

### <span data-ttu-id="be068-161">PSConnectionMonitorResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="be068-161">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="be068-162">筆記</span><span class="sxs-lookup"><span data-stu-id="be068-162">NOTES</span></span>
<span data-ttu-id="be068-163">關鍵字： azure，azurerm，arm，資源，連線，管理，管理員，網路，網路，網路觀察程式，連線監視器</span><span class="sxs-lookup"><span data-stu-id="be068-163">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="be068-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="be068-164">RELATED LINKS</span></span>
<span data-ttu-id="be068-165">[新-AzNetworkWatcher](./New-AzNetworkWatcher.md) 
[AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
[移除-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="be068-165">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="be068-166">[AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
[AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
[AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
[AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="be068-166">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="be068-167">[新-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
[新-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
[AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
[移除-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
[停止 AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="be068-167">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="be068-168">[AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md) 
[AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md) 
[移除-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md) 
[開始-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="be068-168">[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)
[Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)
[Start-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md)</span></span>

