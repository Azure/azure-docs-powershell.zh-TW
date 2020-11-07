---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherconnectionmonitorreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitorReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitorReport.md
ms.openlocfilehash: b524eb04ef9f6765fceb0f3ccb457e29bcc81093
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794388"
---
# <span data-ttu-id="4e872-101">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="4e872-101">Get-AzNetworkWatcherConnectionMonitorReport</span></span>

## <span data-ttu-id="4e872-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4e872-102">SYNOPSIS</span></span>
<span data-ttu-id="4e872-103">查詢最近連接狀態的快照。</span><span class="sxs-lookup"><span data-stu-id="4e872-103">Query a snapshot of the most recent connection states.</span></span>

## <span data-ttu-id="4e872-104">句法</span><span class="sxs-lookup"><span data-stu-id="4e872-104">SYNTAX</span></span>

### <span data-ttu-id="4e872-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="4e872-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherConnectionMonitorReport -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="4e872-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="4e872-106">SetByName</span></span>
```
Get-AzNetworkWatcherConnectionMonitorReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="4e872-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="4e872-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherConnectionMonitorReport -Location <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="4e872-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4e872-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherConnectionMonitorReport -ResourceId <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="4e872-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="4e872-109">SetByInputObject</span></span>
```
Get-AzNetworkWatcherConnectionMonitorReport -InputObject <PSConnectionMonitorResult> [-Name <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="4e872-110">說明</span><span class="sxs-lookup"><span data-stu-id="4e872-110">DESCRIPTION</span></span>
<span data-ttu-id="4e872-111">Get-AzNetworkWatcherConnectionMonitorReport Cmdlet 會傳回最近連接狀態的報告。</span><span class="sxs-lookup"><span data-stu-id="4e872-111">The Get-AzNetworkWatcherConnectionMonitorReport cmdlet returns the report on the most recent connection states.</span></span>

## <span data-ttu-id="4e872-112">示例</span><span class="sxs-lookup"><span data-stu-id="4e872-112">EXAMPLES</span></span>

### <span data-ttu-id="4e872-113">---------------範例1：在指定位置以名稱取得連接監視器的最新連線快照---------------</span><span class="sxs-lookup"><span data-stu-id="4e872-113">---------------  Example 1: Get the most recent connection snapshot of the connection monitor by name in the specified location ---------------</span></span>
```
PS C:\> Get-AzNetworkWatcherConnectionMonitorReport -Location centraluseuap -Name cm


States : [
           {
             "ConnectionState": "Reachable",
             "StartTime": "2018-01-12T01:18:20Z",
             "EvaluationState": "Completed",
             "Hops": [
               {
                 "Type": "Source",
                 "Id": "1530e0f2-c9b7-4bc0-a205-cf7332cd8983",
                 "Address": "10.1.1.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/appNic0/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "b19b74b1-423d-4f0b-99cd-bcaed4d0b8a2"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualAppliance",
                 "Id": "b19b74b1-423d-4f0b-99cd-bcaed4d0b8a2",
                 "Address": "10.1.2.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/fwNic/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "80e46c56-2cf9-4106-8602-608a74832d41"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualAppliance",
                 "Id": "80e46c56-2cf9-4106-8602-608a74832d41",
                 "Address": "10.1.3.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/auNic/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "e17cf884-69db-43b8-9cd5-f920770a0dbe"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualNetwork",
                 "Id": "e17cf884-69db-43b8-9cd5-f920770a0dbe",
                 "Address": "10.1.4.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/dbNic0/ipConfigurations/ipconfig1",
                 "NextHopIds": [],
                 "Issues": []
               }
             ]
           },
           {
             "ConnectionState": "Unreachable",
             "StartTime": "2018-01-12T01:14:11Z",
             "EvaluationState": "Completed",
             "Hops": [
               {
                 "Type": "Source",
                 "Id": "b6251ff8-3d07-4fdf-98f8-04b168e1cf90",
                 "Address": "10.1.1.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/appNic0/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "de6d463b-47fb-4beb-afc4-d77782755313"
                 ],
                 "Issues": [
                   {
                     "Origin": "Local",
                     "Severity": "Error",
                     "Type": "NetworkError",
                     "Context": []
                   }
                 ]
               },
               {
                 "Type": "VirtualAppliance",
                 "Id": "de6d463b-47fb-4beb-afc4-d77782755313",
                 "Address": "10.1.2.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/fwNic/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "0cbadb7e-cd99-4fa9-a832-eb4e0d112293"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualAppliance",
                 "Id": "0cbadb7e-cd99-4fa9-a832-eb4e0d112293",
                 "Address": "10.1.3.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/auNic/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "538005d1-994a-4350-9866-6985385beecf"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualNetwork",
                 "Id": "538005d1-994a-4350-9866-6985385beecf",
                 "Address": "10.1.4.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/dbNic0/ipConfigurations/ipconfig1",
                 "NextHopIds": [],
                 "Issues": []
               }
             ]
           },
           {
             "ConnectionState": "Reachable",
             "StartTime": "2018-01-11T23:54:05Z",
             "EvaluationState": "Completed",
             "Hops": [
               {
                 "Type": "Source",
                 "Id": "3dbec7e8-a37f-4acd-bc5f-86918fffba0e",
                 "Address": "10.1.1.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/appNic0/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "1a87cf61-1be6-4add-bba7-f84afbcf3726"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualAppliance",
                 "Id": "1a87cf61-1be6-4add-bba7-f84afbcf3726",
                 "Address": "10.1.2.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/fwNic/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "070c0740-308e-43ba-b72f-5d8d5a6537ec"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualAppliance",
                 "Id": "070c0740-308e-43ba-b72f-5d8d5a6537ec",
                 "Address": "10.1.3.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/auNic/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "760182e1-c88d-4cfc-a711-65e7e622a67a"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualNetwork",
                 "Id": "760182e1-c88d-4cfc-a711-65e7e622a67a",
                 "Address": "10.1.4.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/dbNic0/ipConfigurations/ipconfig1",
                 "NextHopIds": [],
                 "Issues": []
               }
             ]
           }
         ]

```

<span data-ttu-id="4e872-114">在這個範例中，我們會查詢指定連線監視器的最近連接狀態。</span><span class="sxs-lookup"><span data-stu-id="4e872-114">In this example we query the most recent connection states of the specified connection monitor.</span></span>

## <span data-ttu-id="4e872-115">參數</span><span class="sxs-lookup"><span data-stu-id="4e872-115">PARAMETERS</span></span>

### <span data-ttu-id="4e872-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4e872-116">-AsJob</span></span>
<span data-ttu-id="4e872-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="4e872-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4e872-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e872-118">-DefaultProfile</span></span>
<span data-ttu-id="4e872-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4e872-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e872-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e872-120">-InputObject</span></span>
<span data-ttu-id="4e872-121">[連接監視器] 物件。</span><span class="sxs-lookup"><span data-stu-id="4e872-121">Connection monitor object.</span></span>

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

### <span data-ttu-id="4e872-122">-位置</span><span class="sxs-lookup"><span data-stu-id="4e872-122">-Location</span></span>
<span data-ttu-id="4e872-123">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="4e872-123">Location of the network watcher.</span></span>

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

### <span data-ttu-id="4e872-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="4e872-124">-Name</span></span>
<span data-ttu-id="4e872-125">[連接監視器] 名稱。</span><span class="sxs-lookup"><span data-stu-id="4e872-125">The connection monitor name.</span></span>

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

### <span data-ttu-id="4e872-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4e872-126">-NetworkWatcher</span></span>
<span data-ttu-id="4e872-127">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="4e872-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="4e872-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="4e872-128">-NetworkWatcherName</span></span>
<span data-ttu-id="4e872-129">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="4e872-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="4e872-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e872-130">-ResourceGroupName</span></span>
<span data-ttu-id="4e872-131">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4e872-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="4e872-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e872-132">-ResourceId</span></span>
<span data-ttu-id="4e872-133">[連線監視器] 的 [資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="4e872-133">Resource ID of the connection monitor.</span></span>

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

## <span data-ttu-id="4e872-134">輸入</span><span class="sxs-lookup"><span data-stu-id="4e872-134">INPUTS</span></span>

### <span data-ttu-id="4e872-135">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4e872-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="4e872-136">PSConnectionMonitorResult 中的 [system.object] 命令。</span><span class="sxs-lookup"><span data-stu-id="4e872-136">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="4e872-137">輸出</span><span class="sxs-lookup"><span data-stu-id="4e872-137">OUTPUTS</span></span>

### <span data-ttu-id="4e872-138">PSConnectionMonitorQueryResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4e872-138">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorQueryResult</span></span>


## <span data-ttu-id="4e872-139">筆記</span><span class="sxs-lookup"><span data-stu-id="4e872-139">NOTES</span></span>
<span data-ttu-id="4e872-140">關鍵字： azure，azurerm，arm，資源，連線，管理，管理員，網路，網路，網路觀察程式，連線監視器</span><span class="sxs-lookup"><span data-stu-id="4e872-140">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="4e872-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="4e872-141">RELATED LINKS</span></span>
<span data-ttu-id="4e872-142">[新-AzNetworkWatcher](./New-AzNetworkWatcher.md) 
[AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
[移除-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="4e872-142">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="4e872-143">[AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
[AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
[AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
[AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="4e872-143">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="4e872-144">[新-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
[新-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
[AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
[移除-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
[停止 AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="4e872-144">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="4e872-145">[新-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md) 
[AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="4e872-145">[New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)</span></span>

