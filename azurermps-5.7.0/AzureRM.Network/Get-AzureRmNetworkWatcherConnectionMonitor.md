---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: a78114bbf47113983453a0dd5c1e13db0fc73a6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447065"
---
# <span data-ttu-id="fd791-101">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fd791-101">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="fd791-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fd791-102">SYNOPSIS</span></span>
<span data-ttu-id="fd791-103">以指定的名稱或連線監視器清單傳回連接監視器</span><span class="sxs-lookup"><span data-stu-id="fd791-103">Returns connection monitor with specified name or the list of connection monitors</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd791-104">句法</span><span class="sxs-lookup"><span data-stu-id="fd791-104">SYNTAX</span></span>

### <span data-ttu-id="fd791-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="fd791-105">SetByName (Default)</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd791-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="fd791-106">SetByResource</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd791-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="fd791-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -Location <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd791-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="fd791-108">SetByResourceId</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fd791-109">說明</span><span class="sxs-lookup"><span data-stu-id="fd791-109">DESCRIPTION</span></span>
<span data-ttu-id="fd791-110">Get-AzureRmNetworkWatcherConnectionMonitor Cmdlet 會以指定的名稱/resourceId 或與指定的網路監控程式/位置相對應的連線監視器清單傳回連接監視器。</span><span class="sxs-lookup"><span data-stu-id="fd791-110">The Get-AzureRmNetworkWatcherConnectionMonitor cmdlet returns the connection monitor with the specified name / resourceId or the list of connection monitors corresponding to the specified network watcher / location.</span></span>

## <span data-ttu-id="fd791-111">示例</span><span class="sxs-lookup"><span data-stu-id="fd791-111">EXAMPLES</span></span>

### <span data-ttu-id="fd791-112">範例1：依名稱在指定位置取得連接監視器</span><span class="sxs-lookup"><span data-stu-id="fd791-112">Example 1: Get connection monitor by name in the specified location</span></span>
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

<span data-ttu-id="fd791-113">在這個範例中，我們會透過名稱在指定位置取得連接監視器。</span><span class="sxs-lookup"><span data-stu-id="fd791-113">In this example we get connection monitor by name in the specified location.</span></span>

## <span data-ttu-id="fd791-114">參數</span><span class="sxs-lookup"><span data-stu-id="fd791-114">PARAMETERS</span></span>

### <span data-ttu-id="fd791-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd791-115">-DefaultProfile</span></span>
<span data-ttu-id="fd791-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fd791-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd791-117">-位置</span><span class="sxs-lookup"><span data-stu-id="fd791-117">-Location</span></span>
<span data-ttu-id="fd791-118">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="fd791-118">Location of the network watcher.</span></span>

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

### <span data-ttu-id="fd791-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="fd791-119">-Name</span></span>
<span data-ttu-id="fd791-120">[連接監視器] 名稱。</span><span class="sxs-lookup"><span data-stu-id="fd791-120">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd791-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fd791-121">-NetworkWatcher</span></span>
<span data-ttu-id="fd791-122">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="fd791-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="fd791-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="fd791-123">-NetworkWatcherName</span></span>
<span data-ttu-id="fd791-124">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="fd791-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="fd791-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd791-125">-ResourceGroupName</span></span>
<span data-ttu-id="fd791-126">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fd791-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="fd791-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd791-127">-ResourceId</span></span>
<span data-ttu-id="fd791-128">[連線監視器] 的 [資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="fd791-128">Resource ID of the connection monitor.</span></span>

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

### <span data-ttu-id="fd791-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd791-129">CommonParameters</span></span>
<span data-ttu-id="fd791-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fd791-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="fd791-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fd791-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd791-132">輸入</span><span class="sxs-lookup"><span data-stu-id="fd791-132">INPUTS</span></span>

### <span data-ttu-id="fd791-133">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="fd791-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="fd791-134">System.object</span><span class="sxs-lookup"><span data-stu-id="fd791-134">System.String</span></span>

## <span data-ttu-id="fd791-135">輸出</span><span class="sxs-lookup"><span data-stu-id="fd791-135">OUTPUTS</span></span>

### <span data-ttu-id="fd791-136">PSConnectionMonitorResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="fd791-136">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="fd791-137">筆記</span><span class="sxs-lookup"><span data-stu-id="fd791-137">NOTES</span></span>
<span data-ttu-id="fd791-138">關鍵字： azure，azurerm，arm，資源，連線，管理，管理員，網路，網路，網路觀察程式，連線監視器</span><span class="sxs-lookup"><span data-stu-id="fd791-138">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="fd791-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="fd791-139">RELATED LINKS</span></span>

[<span data-ttu-id="fd791-140">新-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fd791-140">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="fd791-141">AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fd791-141">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="fd791-142">移除-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fd791-142">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="fd791-143">AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="fd791-143">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="fd791-144">AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="fd791-144">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="fd791-145">AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="fd791-145">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="fd791-146">AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="fd791-146">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="fd791-147">新-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fd791-147">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="fd791-148">新-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="fd791-148">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="fd791-149">AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fd791-149">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="fd791-150">移除-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fd791-150">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="fd791-151">停止 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fd791-151">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="fd791-152">新-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fd791-152">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="fd791-153">AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="fd791-153">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="fd791-154">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fd791-154">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="fd791-155">開始-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fd791-155">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="fd791-156">停止 AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fd791-156">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="fd791-157">移除-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fd791-157">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()
