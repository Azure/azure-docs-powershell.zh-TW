---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: bfdcfbf57f44479ad35a2b9075590a0d40351ec9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794250"
---
# <span data-ttu-id="667b3-101">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="667b3-101">New-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="667b3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="667b3-102">SYNOPSIS</span></span>
<span data-ttu-id="667b3-103">建立連接監視器。</span><span class="sxs-lookup"><span data-stu-id="667b3-103">Creates a connection monitor.</span></span>

## <span data-ttu-id="667b3-104">句法</span><span class="sxs-lookup"><span data-stu-id="667b3-104">SYNTAX</span></span>

### <span data-ttu-id="667b3-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="667b3-105">SetByResource (Default)</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="667b3-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="667b3-106">SetByName</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="667b3-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="667b3-107">SetByLocation</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="667b3-108">說明</span><span class="sxs-lookup"><span data-stu-id="667b3-108">DESCRIPTION</span></span>
<span data-ttu-id="667b3-109">New-AzNetworkWatcherConnectionMonitor Cmdlet 會針對指定的來源和目的地 rcreates 連線監視器。</span><span class="sxs-lookup"><span data-stu-id="667b3-109">The New-AzNetworkWatcherConnectionMonitor cmdlet rcreates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="667b3-110">示例</span><span class="sxs-lookup"><span data-stu-id="667b3-110">EXAMPLES</span></span>

### <span data-ttu-id="667b3-111">---------------範例1：建立 vm 和網際網路目的地的連線監視器---------------</span><span class="sxs-lookup"><span data-stu-id="667b3-111">---------------  Example 1: Create a connection monitor for a vm and internet destination ---------------</span></span>
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

<span data-ttu-id="667b3-112">New-AzNetworkWatcherConnectionMonitor Cmdlet 會為指定的來源和目的地建立連接監視器。</span><span class="sxs-lookup"><span data-stu-id="667b3-112">The New-AzNetworkWatcherConnectionMonitor cmdlet creates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="667b3-113">參數</span><span class="sxs-lookup"><span data-stu-id="667b3-113">PARAMETERS</span></span>

### <span data-ttu-id="667b3-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="667b3-114">-AsJob</span></span>
<span data-ttu-id="667b3-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="667b3-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="667b3-116">-AutoStart</span><span class="sxs-lookup"><span data-stu-id="667b3-116">-AutoStart</span></span>
<span data-ttu-id="667b3-117">自動啟動。</span><span class="sxs-lookup"><span data-stu-id="667b3-117">Auto start.</span></span>

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

### <span data-ttu-id="667b3-118">-確認</span><span class="sxs-lookup"><span data-stu-id="667b3-118">-Confirm</span></span>
<span data-ttu-id="667b3-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="667b3-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="667b3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="667b3-120">-DefaultProfile</span></span>
<span data-ttu-id="667b3-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="667b3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="667b3-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="667b3-122">-DestinationAddress</span></span>
<span data-ttu-id="667b3-123">連線監視者目的地的 Ip 位址。</span><span class="sxs-lookup"><span data-stu-id="667b3-123">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="667b3-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="667b3-124">-DestinationPort</span></span>
<span data-ttu-id="667b3-125">[目的地埠]。</span><span class="sxs-lookup"><span data-stu-id="667b3-125">Destination port.</span></span>

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

### <span data-ttu-id="667b3-126">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="667b3-126">-DestinationResourceId</span></span>
<span data-ttu-id="667b3-127">連線監視者目的地的 ID。</span><span class="sxs-lookup"><span data-stu-id="667b3-127">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="667b3-128">-Force</span><span class="sxs-lookup"><span data-stu-id="667b3-128">-Force</span></span>
<span data-ttu-id="667b3-129">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="667b3-129">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="667b3-130">-位置</span><span class="sxs-lookup"><span data-stu-id="667b3-130">-Location</span></span>
<span data-ttu-id="667b3-131">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="667b3-131">Location of the network watcher.</span></span>

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

### <span data-ttu-id="667b3-132">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="667b3-132">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="667b3-133">監控間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="667b3-133">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="667b3-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="667b3-134">-Name</span></span>
<span data-ttu-id="667b3-135">[連接監視器] 名稱。</span><span class="sxs-lookup"><span data-stu-id="667b3-135">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="667b3-136">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="667b3-136">-NetworkWatcher</span></span>
<span data-ttu-id="667b3-137">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="667b3-137">The network watcher resource.</span></span>

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

### <span data-ttu-id="667b3-138">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="667b3-138">-NetworkWatcherName</span></span>
<span data-ttu-id="667b3-139">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="667b3-139">The name of network watcher.</span></span>

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

### <span data-ttu-id="667b3-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="667b3-140">-ResourceGroupName</span></span>
<span data-ttu-id="667b3-141">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="667b3-141">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="667b3-142">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="667b3-142">-SourcePort</span></span>
<span data-ttu-id="667b3-143">來源埠。</span><span class="sxs-lookup"><span data-stu-id="667b3-143">Source port.</span></span>

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

### <span data-ttu-id="667b3-144">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="667b3-144">-SourceResourceId</span></span>
<span data-ttu-id="667b3-145">連線監視來源的 ID。</span><span class="sxs-lookup"><span data-stu-id="667b3-145">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="667b3-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="667b3-146">-Tag</span></span>
<span data-ttu-id="667b3-147">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="667b3-147">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="667b3-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="667b3-148">-WhatIf</span></span>
<span data-ttu-id="667b3-149">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="667b3-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="667b3-150">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="667b3-150">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="667b3-151">輸入</span><span class="sxs-lookup"><span data-stu-id="667b3-151">INPUTS</span></span>

### <span data-ttu-id="667b3-152">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="667b3-152">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="667b3-153">System.object</span><span class="sxs-lookup"><span data-stu-id="667b3-153">System.String</span></span>


## <span data-ttu-id="667b3-154">輸出</span><span class="sxs-lookup"><span data-stu-id="667b3-154">OUTPUTS</span></span>

### <span data-ttu-id="667b3-155">PSConnectionMonitorResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="667b3-155">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="667b3-156">筆記</span><span class="sxs-lookup"><span data-stu-id="667b3-156">NOTES</span></span>
<span data-ttu-id="667b3-157">關鍵字： azure，azurerm，arm，資源，連線，管理，管理員，網路，網路，網路觀察程式，連線監視器</span><span class="sxs-lookup"><span data-stu-id="667b3-157">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="667b3-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="667b3-158">RELATED LINKS</span></span>
<span data-ttu-id="667b3-159">[新-AzNetworkWatcher](./New-AzNetworkWatcher.md) 
[AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
[移除-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="667b3-159">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="667b3-160">[AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
[AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
[AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
[AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="667b3-160">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="667b3-161">[新-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
[新-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
[AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
[移除-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
[停止 AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="667b3-161">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="667b3-162">[AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md) 
[AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md) 
[移除-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="667b3-162">[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)
[Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)</span></span>
