---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: d8ab2ce24db9c6ab07989dc5a4a45b8bfca8fc78
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794389"
---
# <span data-ttu-id="f5734-101">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f5734-101">Get-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="f5734-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f5734-102">SYNOPSIS</span></span>
<span data-ttu-id="f5734-103">以指定的名稱或連線監視器清單傳回連接監視器</span><span class="sxs-lookup"><span data-stu-id="f5734-103">Returns connection monitor with specified name or the list of connection monitors</span></span>

## <span data-ttu-id="f5734-104">句法</span><span class="sxs-lookup"><span data-stu-id="f5734-104">SYNTAX</span></span>

### <span data-ttu-id="f5734-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="f5734-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="f5734-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="f5734-106">SetByName</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="f5734-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="f5734-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="f5734-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f5734-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="f5734-109">說明</span><span class="sxs-lookup"><span data-stu-id="f5734-109">DESCRIPTION</span></span>
<span data-ttu-id="f5734-110">Get-AzNetworkWatcherConnectionMonitor Cmdlet 會以指定的名稱/resourceId 或與指定的網路監控程式/位置相對應的連線監視器清單傳回連接監視器。</span><span class="sxs-lookup"><span data-stu-id="f5734-110">The Get-AzNetworkWatcherConnectionMonitor cmdlet returns the connection monitor with the specified name / resourceId or the list of connection monitors corresponding to the specified network watcher / location.</span></span>

## <span data-ttu-id="f5734-111">示例</span><span class="sxs-lookup"><span data-stu-id="f5734-111">EXAMPLES</span></span>

### <span data-ttu-id="f5734-112">---------------範例1：依名稱在指定位置取得連接監視器---------------</span><span class="sxs-lookup"><span data-stu-id="f5734-112">---------------  Example 1: Get connection monitor by name in the specified location ---------------</span></span>
```
PS C:\> Get-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm


Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/cm
Etag                        : W/"40961b58-e379-4204-a47b-0c477739b095"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/96e68903-0a56-4819-9987-8d08ad6
                              a1f99/resourceGroups/VarunRgCentralUSEUAP/providers/Microsoft.C
                              ompute/virtualMachines/irinavm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "google.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:19:28 PM
MonitoringStatus            : Stopped
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {
                                "key1": "value1"
                              }
```

<span data-ttu-id="f5734-113">在這個範例中，我們會透過名稱在指定位置取得連接監視器。</span><span class="sxs-lookup"><span data-stu-id="f5734-113">In this example we get connection monitor by name in the specified location.</span></span>

## <span data-ttu-id="f5734-114">參數</span><span class="sxs-lookup"><span data-stu-id="f5734-114">PARAMETERS</span></span>

### <span data-ttu-id="f5734-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f5734-115">-AsJob</span></span>
<span data-ttu-id="f5734-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f5734-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f5734-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5734-117">-DefaultProfile</span></span>
<span data-ttu-id="f5734-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f5734-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5734-119">-位置</span><span class="sxs-lookup"><span data-stu-id="f5734-119">-Location</span></span>
<span data-ttu-id="f5734-120">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="f5734-120">Location of the network watcher.</span></span>

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

### <span data-ttu-id="f5734-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="f5734-121">-Name</span></span>
<span data-ttu-id="f5734-122">[連接監視器] 名稱。</span><span class="sxs-lookup"><span data-stu-id="f5734-122">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5734-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f5734-123">-NetworkWatcher</span></span>
<span data-ttu-id="f5734-124">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="f5734-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="f5734-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="f5734-125">-NetworkWatcherName</span></span>
<span data-ttu-id="f5734-126">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="f5734-126">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5734-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5734-127">-ResourceGroupName</span></span>
<span data-ttu-id="f5734-128">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f5734-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="f5734-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5734-129">-ResourceId</span></span>
<span data-ttu-id="f5734-130">[連線監視器] 的 [資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="f5734-130">Resource ID of the connection monitor.</span></span>

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

### <span data-ttu-id="f5734-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5734-131">CommonParameters</span></span>
<span data-ttu-id="f5734-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f5734-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5734-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f5734-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5734-134">輸入</span><span class="sxs-lookup"><span data-stu-id="f5734-134">INPUTS</span></span>

### <span data-ttu-id="f5734-135">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f5734-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="f5734-136">System.object</span><span class="sxs-lookup"><span data-stu-id="f5734-136">System.String</span></span>


## <span data-ttu-id="f5734-137">輸出</span><span class="sxs-lookup"><span data-stu-id="f5734-137">OUTPUTS</span></span>

### <span data-ttu-id="f5734-138">PSConnectionMonitorResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f5734-138">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="f5734-139">筆記</span><span class="sxs-lookup"><span data-stu-id="f5734-139">NOTES</span></span>
<span data-ttu-id="f5734-140">關鍵字： azure，azurerm，arm，資源，連線，管理，管理員，網路，網路，網路觀察程式，連線監視器</span><span class="sxs-lookup"><span data-stu-id="f5734-140">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="f5734-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="f5734-141">RELATED LINKS</span></span>
<span data-ttu-id="f5734-142">[新-AzNetworkWatcher](./New-AzNetworkWatcher.md) 
[AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
[移除-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="f5734-142">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="f5734-143">[AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
[AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
[AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
[AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="f5734-143">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="f5734-144">[新-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
[新-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
[AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
[移除-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
[停止 AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="f5734-144">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="f5734-145">[新-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md) 
[AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)</span><span class="sxs-lookup"><span data-stu-id="f5734-145">[New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)</span></span>