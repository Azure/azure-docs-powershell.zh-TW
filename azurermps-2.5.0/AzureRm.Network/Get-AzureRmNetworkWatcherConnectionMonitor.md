---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcher
schema: 2.0.0
ms.openlocfilehash: 014942f38abf0caae01463d07343b5ad473a24d7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800434"
---
# <span data-ttu-id="dd226-101">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="dd226-101">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="dd226-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dd226-102">SYNOPSIS</span></span>
<span data-ttu-id="dd226-103">以指定的名稱或連線監視器清單傳回連接監視器</span><span class="sxs-lookup"><span data-stu-id="dd226-103">Returns connection monitor with specified name or the list of connection monitors</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd226-104">句法</span><span class="sxs-lookup"><span data-stu-id="dd226-104">SYNTAX</span></span>

### <span data-ttu-id="dd226-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="dd226-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="dd226-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="dd226-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="dd226-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="dd226-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="dd226-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="dd226-108">SetByResourceId</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="dd226-109">說明</span><span class="sxs-lookup"><span data-stu-id="dd226-109">DESCRIPTION</span></span>
<span data-ttu-id="dd226-110">Get-AzureRmNetworkWatcherConnectionMonitor Cmdlet 會以指定的名稱/resourceId 或與指定的網路監控程式/位置相對應的連線監視器清單傳回連接監視器。</span><span class="sxs-lookup"><span data-stu-id="dd226-110">The Get-AzureRmNetworkWatcherConnectionMonitor cmdlet returns the connection monitor with the specified name / resourceId or the list of connection monitors corresponding to the specified network watcher / location.</span></span>

## <span data-ttu-id="dd226-111">示例</span><span class="sxs-lookup"><span data-stu-id="dd226-111">EXAMPLES</span></span>

### <span data-ttu-id="dd226-112">---------------範例1：依名稱在指定位置取得連接監視器---------------</span><span class="sxs-lookup"><span data-stu-id="dd226-112">---------------  Example 1: Get connection monitor by name in the specified location ---------------</span></span>
```
PS C:\> Get-AzureRmNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm


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

<span data-ttu-id="dd226-113">在這個範例中，我們會透過名稱在指定位置取得連接監視器。</span><span class="sxs-lookup"><span data-stu-id="dd226-113">In this example we get connection monitor by name in the specified location.</span></span>

## <span data-ttu-id="dd226-114">參數</span><span class="sxs-lookup"><span data-stu-id="dd226-114">PARAMETERS</span></span>

### <span data-ttu-id="dd226-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd226-115">-AsJob</span></span>
<span data-ttu-id="dd226-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="dd226-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dd226-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd226-117">-DefaultProfile</span></span>
<span data-ttu-id="dd226-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dd226-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd226-119">-位置</span><span class="sxs-lookup"><span data-stu-id="dd226-119">-Location</span></span>
<span data-ttu-id="dd226-120">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="dd226-120">Location of the network watcher.</span></span>

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

### <span data-ttu-id="dd226-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="dd226-121">-Name</span></span>
<span data-ttu-id="dd226-122">[連接監視器] 名稱。</span><span class="sxs-lookup"><span data-stu-id="dd226-122">The connection monitor name.</span></span>

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

### <span data-ttu-id="dd226-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dd226-123">-NetworkWatcher</span></span>
<span data-ttu-id="dd226-124">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="dd226-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="dd226-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="dd226-125">-NetworkWatcherName</span></span>
<span data-ttu-id="dd226-126">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="dd226-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="dd226-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd226-127">-ResourceGroupName</span></span>
<span data-ttu-id="dd226-128">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dd226-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="dd226-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd226-129">-ResourceId</span></span>
<span data-ttu-id="dd226-130">[連線監視器] 的 [資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="dd226-130">Resource ID of the connection monitor.</span></span>

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

### <span data-ttu-id="dd226-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd226-131">CommonParameters</span></span>
<span data-ttu-id="dd226-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dd226-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd226-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dd226-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd226-134">輸入</span><span class="sxs-lookup"><span data-stu-id="dd226-134">INPUTS</span></span>

### <span data-ttu-id="dd226-135">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="dd226-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="dd226-136">System.object</span><span class="sxs-lookup"><span data-stu-id="dd226-136">System.String</span></span>


## <span data-ttu-id="dd226-137">輸出</span><span class="sxs-lookup"><span data-stu-id="dd226-137">OUTPUTS</span></span>

### <span data-ttu-id="dd226-138">PSConnectionMonitorResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="dd226-138">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="dd226-139">筆記</span><span class="sxs-lookup"><span data-stu-id="dd226-139">NOTES</span></span>
<span data-ttu-id="dd226-140">關鍵字： azure，azurerm，arm，資源，連線，管理，管理員，網路，網路，網路觀察程式，連線監視器</span><span class="sxs-lookup"><span data-stu-id="dd226-140">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="dd226-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="dd226-141">RELATED LINKS</span></span>
<span data-ttu-id="dd226-142">[新-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md) 
[AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md) 
[移除-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="dd226-142">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="dd226-143">[AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
[AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
[AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
[AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="dd226-143">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="dd226-144">[新-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
[新-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
[AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
[移除-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
[停止 AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="dd226-144">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="dd226-145">[新-AzureRmNetworkWatcherConnectionMonitor](./New-AzureRmNetworkWatcherConnectionMonitor.md) 
[AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)</span><span class="sxs-lookup"><span data-stu-id="dd226-145">[New-AzureRmNetworkWatcherConnectionMonitor](./New-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)</span></span>
