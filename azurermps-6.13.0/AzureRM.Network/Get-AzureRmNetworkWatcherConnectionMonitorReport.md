---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherConnectionMonitorReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherConnectionMonitorReport.md
ms.openlocfilehash: 6e5f7370740e069bc3c8ce5f83ef2e784cc4012a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625272"
---
# <span data-ttu-id="9b2d6-101">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="9b2d6-101">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>

## <span data-ttu-id="9b2d6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9b2d6-102">SYNOPSIS</span></span>
<span data-ttu-id="9b2d6-103">查詢最近連接狀態的快照。</span><span class="sxs-lookup"><span data-stu-id="9b2d6-103">Query a snapshot of the most recent connection states.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b2d6-104">句法</span><span class="sxs-lookup"><span data-stu-id="9b2d6-104">SYNTAX</span></span>

### <span data-ttu-id="9b2d6-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="9b2d6-105">SetByName (Default)</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitorReport -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b2d6-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9b2d6-106">SetByResource</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitorReport -NetworkWatcher <PSNetworkWatcher> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b2d6-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="9b2d6-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitorReport -Location <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b2d6-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9b2d6-108">SetByResourceId</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitorReport -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b2d6-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="9b2d6-109">SetByInputObject</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitorReport -InputObject <PSConnectionMonitorResult> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b2d6-110">說明</span><span class="sxs-lookup"><span data-stu-id="9b2d6-110">DESCRIPTION</span></span>
<span data-ttu-id="9b2d6-111">Get-AzureRmNetworkWatcherConnectionMonitorReport Cmdlet 會傳回最近連接狀態的報告。</span><span class="sxs-lookup"><span data-stu-id="9b2d6-111">The Get-AzureRmNetworkWatcherConnectionMonitorReport cmdlet returns the report on the most recent connection states.</span></span>

## <span data-ttu-id="9b2d6-112">示例</span><span class="sxs-lookup"><span data-stu-id="9b2d6-112">EXAMPLES</span></span>

### <span data-ttu-id="9b2d6-113">範例1：在指定位置以名稱取得連接監視器的最新連線快照</span><span class="sxs-lookup"><span data-stu-id="9b2d6-113">Example 1: Get the most recent connection snapshot of the connection monitor by name in the specified location</span></span>
```
PS C:\> Get-AzureRmNetworkWatcherConnectionMonitorReport -Location centraluseuap -Name cm


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

<span data-ttu-id="9b2d6-114">在這個範例中，我們會查詢指定連線監視器的最近連接狀態。</span><span class="sxs-lookup"><span data-stu-id="9b2d6-114">In this example we query the most recent connection states of the specified connection monitor.</span></span>

## <span data-ttu-id="9b2d6-115">參數</span><span class="sxs-lookup"><span data-stu-id="9b2d6-115">PARAMETERS</span></span>

### <span data-ttu-id="9b2d6-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9b2d6-116">-AsJob</span></span>
<span data-ttu-id="9b2d6-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9b2d6-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9b2d6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b2d6-118">-DefaultProfile</span></span>
<span data-ttu-id="9b2d6-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9b2d6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b2d6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b2d6-120">-InputObject</span></span>
<span data-ttu-id="9b2d6-121">[連接監視器] 物件。</span><span class="sxs-lookup"><span data-stu-id="9b2d6-121">Connection monitor object.</span></span>

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

### <span data-ttu-id="9b2d6-122">-位置</span><span class="sxs-lookup"><span data-stu-id="9b2d6-122">-Location</span></span>
<span data-ttu-id="9b2d6-123">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="9b2d6-123">Location of the network watcher.</span></span>

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

### <span data-ttu-id="9b2d6-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="9b2d6-124">-Name</span></span>
<span data-ttu-id="9b2d6-125">[連接監視器] 名稱。</span><span class="sxs-lookup"><span data-stu-id="9b2d6-125">The connection monitor name.</span></span>

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

### <span data-ttu-id="9b2d6-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9b2d6-126">-NetworkWatcher</span></span>
<span data-ttu-id="9b2d6-127">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="9b2d6-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="9b2d6-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="9b2d6-128">-NetworkWatcherName</span></span>
<span data-ttu-id="9b2d6-129">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="9b2d6-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="9b2d6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b2d6-130">-ResourceGroupName</span></span>
<span data-ttu-id="9b2d6-131">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9b2d6-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="9b2d6-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b2d6-132">-ResourceId</span></span>
<span data-ttu-id="9b2d6-133">[連線監視器] 的 [資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="9b2d6-133">Resource ID of the connection monitor.</span></span>

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

### <span data-ttu-id="9b2d6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b2d6-134">CommonParameters</span></span>
<span data-ttu-id="9b2d6-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9b2d6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b2d6-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9b2d6-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b2d6-137">輸入</span><span class="sxs-lookup"><span data-stu-id="9b2d6-137">INPUTS</span></span>

### <span data-ttu-id="9b2d6-138">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9b2d6-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="9b2d6-139">參數： NetworkWatcher (ByValue) </span><span class="sxs-lookup"><span data-stu-id="9b2d6-139">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="9b2d6-140">System.object</span><span class="sxs-lookup"><span data-stu-id="9b2d6-140">System.String</span></span>

### <span data-ttu-id="9b2d6-141">PSConnectionMonitorResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9b2d6-141">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>
<span data-ttu-id="9b2d6-142">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="9b2d6-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="9b2d6-143">輸出</span><span class="sxs-lookup"><span data-stu-id="9b2d6-143">OUTPUTS</span></span>

### <span data-ttu-id="9b2d6-144">PSConnectionMonitorQueryResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9b2d6-144">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorQueryResult</span></span>

## <span data-ttu-id="9b2d6-145">筆記</span><span class="sxs-lookup"><span data-stu-id="9b2d6-145">NOTES</span></span>
<span data-ttu-id="9b2d6-146">關鍵字： azure，azurerm，arm，資源，連線，管理，管理員，網路，網路，網路觀察程式，連線監視器</span><span class="sxs-lookup"><span data-stu-id="9b2d6-146">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="9b2d6-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="9b2d6-147">RELATED LINKS</span></span>

[<span data-ttu-id="9b2d6-148">新-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9b2d6-148">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="9b2d6-149">AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9b2d6-149">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="9b2d6-150">移除-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9b2d6-150">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="9b2d6-151">AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="9b2d6-151">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="9b2d6-152">AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="9b2d6-152">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="9b2d6-153">AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="9b2d6-153">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="9b2d6-154">AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="9b2d6-154">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="9b2d6-155">新-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9b2d6-155">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="9b2d6-156">新-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="9b2d6-156">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="9b2d6-157">AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9b2d6-157">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="9b2d6-158">移除-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9b2d6-158">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="9b2d6-159">停止 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9b2d6-159">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="9b2d6-160">AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9b2d6-160">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="9b2d6-161">AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="9b2d6-161">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="9b2d6-162">移除-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9b2d6-162">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="9b2d6-163">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9b2d6-163">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="9b2d6-164">停止 AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9b2d6-164">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="9b2d6-165">新-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9b2d6-165">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="9b2d6-166">新-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="9b2d6-166">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>]()

[<span data-ttu-id="9b2d6-167">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="9b2d6-167">Test-AzureRmNetworkWatcherIPFlow</span></span>]()

[<span data-ttu-id="9b2d6-168">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="9b2d6-168">Test-AzureRmNetworkWatcherConnectivity</span></span>]()

[<span data-ttu-id="9b2d6-169">開始-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="9b2d6-169">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>]()

[<span data-ttu-id="9b2d6-170">開始-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9b2d6-170">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="9b2d6-171">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="9b2d6-171">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>]()

[<span data-ttu-id="9b2d6-172">AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="9b2d6-172">Get-AzureRMNetworkWatcherReachabilityReport</span></span>]()

[<span data-ttu-id="9b2d6-173">AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="9b2d6-173">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>]()

[<span data-ttu-id="9b2d6-174">AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="9b2d6-174">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>]()
