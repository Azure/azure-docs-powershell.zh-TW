---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcher
schema: 2.0.0
ms.openlocfilehash: 3e5853d99157fef87c2f02c2be9fab7bb983d1ae
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801226"
---
# <span data-ttu-id="b031f-101">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b031f-101">New-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="b031f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b031f-102">SYNOPSIS</span></span>
<span data-ttu-id="b031f-103">建立連接監視器。</span><span class="sxs-lookup"><span data-stu-id="b031f-103">Creates a connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b031f-104">句法</span><span class="sxs-lookup"><span data-stu-id="b031f-104">SYNTAX</span></span>

### <span data-ttu-id="b031f-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="b031f-105">SetByResource (Default)</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="b031f-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="b031f-106">SetByName</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="b031f-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="b031f-107">SetByLocation</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="b031f-108">說明</span><span class="sxs-lookup"><span data-stu-id="b031f-108">DESCRIPTION</span></span>
<span data-ttu-id="b031f-109">New-AzureRmNetworkWatcherConnectionMonitor Cmdlet 會針對指定的來源和目的地 rcreates 連線監視器。</span><span class="sxs-lookup"><span data-stu-id="b031f-109">The New-AzureRmNetworkWatcherConnectionMonitor cmdlet rcreates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="b031f-110">示例</span><span class="sxs-lookup"><span data-stu-id="b031f-110">EXAMPLES</span></span>

### <span data-ttu-id="b031f-111">---------------範例1：建立 vm 和網際網路目的地的連線監視器---------------</span><span class="sxs-lookup"><span data-stu-id="b031f-111">---------------  Example 1: Create a connection monitor for a vm and internet destination ---------------</span></span>
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

<span data-ttu-id="b031f-112">New-AzureRmNetworkWatcherConnectionMonitor Cmdlet 會為指定的來源和目的地建立連接監視器。</span><span class="sxs-lookup"><span data-stu-id="b031f-112">The New-AzureRmNetworkWatcherConnectionMonitor cmdlet creates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="b031f-113">參數</span><span class="sxs-lookup"><span data-stu-id="b031f-113">PARAMETERS</span></span>

### <span data-ttu-id="b031f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b031f-114">-AsJob</span></span>
<span data-ttu-id="b031f-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b031f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b031f-116">-AutoStart</span><span class="sxs-lookup"><span data-stu-id="b031f-116">-AutoStart</span></span>
<span data-ttu-id="b031f-117">自動啟動。</span><span class="sxs-lookup"><span data-stu-id="b031f-117">Auto start.</span></span>

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

### <span data-ttu-id="b031f-118">-確認</span><span class="sxs-lookup"><span data-stu-id="b031f-118">-Confirm</span></span>
<span data-ttu-id="b031f-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b031f-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b031f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b031f-120">-DefaultProfile</span></span>
<span data-ttu-id="b031f-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b031f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b031f-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="b031f-122">-DestinationAddress</span></span>
<span data-ttu-id="b031f-123">連線監視者目的地的 Ip 位址。</span><span class="sxs-lookup"><span data-stu-id="b031f-123">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="b031f-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="b031f-124">-DestinationPort</span></span>
<span data-ttu-id="b031f-125">[目的地埠]。</span><span class="sxs-lookup"><span data-stu-id="b031f-125">Destination port.</span></span>

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

### <span data-ttu-id="b031f-126">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="b031f-126">-DestinationResourceId</span></span>
<span data-ttu-id="b031f-127">連線監視者目的地的 ID。</span><span class="sxs-lookup"><span data-stu-id="b031f-127">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="b031f-128">-Force</span><span class="sxs-lookup"><span data-stu-id="b031f-128">-Force</span></span>
<span data-ttu-id="b031f-129">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="b031f-129">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="b031f-130">-位置</span><span class="sxs-lookup"><span data-stu-id="b031f-130">-Location</span></span>
<span data-ttu-id="b031f-131">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="b031f-131">Location of the network watcher.</span></span>

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

### <span data-ttu-id="b031f-132">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="b031f-132">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="b031f-133">監控間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="b031f-133">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="b031f-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="b031f-134">-Name</span></span>
<span data-ttu-id="b031f-135">[連接監視器] 名稱。</span><span class="sxs-lookup"><span data-stu-id="b031f-135">The connection monitor name.</span></span>

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

### <span data-ttu-id="b031f-136">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b031f-136">-NetworkWatcher</span></span>
<span data-ttu-id="b031f-137">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="b031f-137">The network watcher resource.</span></span>

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

### <span data-ttu-id="b031f-138">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="b031f-138">-NetworkWatcherName</span></span>
<span data-ttu-id="b031f-139">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="b031f-139">The name of network watcher.</span></span>

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

### <span data-ttu-id="b031f-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b031f-140">-ResourceGroupName</span></span>
<span data-ttu-id="b031f-141">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b031f-141">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="b031f-142">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="b031f-142">-SourcePort</span></span>
<span data-ttu-id="b031f-143">來源埠。</span><span class="sxs-lookup"><span data-stu-id="b031f-143">Source port.</span></span>

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

### <span data-ttu-id="b031f-144">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="b031f-144">-SourceResourceId</span></span>
<span data-ttu-id="b031f-145">連線監視來源的 ID。</span><span class="sxs-lookup"><span data-stu-id="b031f-145">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="b031f-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="b031f-146">-Tag</span></span>
<span data-ttu-id="b031f-147">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="b031f-147">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="b031f-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b031f-148">-WhatIf</span></span>
<span data-ttu-id="b031f-149">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b031f-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b031f-150">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b031f-150">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="b031f-151">輸入</span><span class="sxs-lookup"><span data-stu-id="b031f-151">INPUTS</span></span>

### <span data-ttu-id="b031f-152">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b031f-152">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="b031f-153">System.object</span><span class="sxs-lookup"><span data-stu-id="b031f-153">System.String</span></span>


## <span data-ttu-id="b031f-154">輸出</span><span class="sxs-lookup"><span data-stu-id="b031f-154">OUTPUTS</span></span>

### <span data-ttu-id="b031f-155">PSConnectionMonitorResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b031f-155">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="b031f-156">筆記</span><span class="sxs-lookup"><span data-stu-id="b031f-156">NOTES</span></span>
<span data-ttu-id="b031f-157">關鍵字： azure，azurerm，arm，資源，連線，管理，管理員，網路，網路，網路觀察程式，連線監視器</span><span class="sxs-lookup"><span data-stu-id="b031f-157">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="b031f-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="b031f-158">RELATED LINKS</span></span>
<span data-ttu-id="b031f-159">[新-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md) 
[AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md) 
[移除-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="b031f-159">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="b031f-160">[AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
[AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
[AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
[AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="b031f-160">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="b031f-161">[新-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
[新-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
[AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
[移除-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
[停止 AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="b031f-161">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="b031f-162">[AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md) 
[AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md) 
[移除-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="b031f-162">[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)
[Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)</span></span>
