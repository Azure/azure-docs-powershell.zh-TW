---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: c2da2b9173b3977a606699fd8e1def3dae2a68d9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127026"
---
# <span data-ttu-id="051d7-101">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="051d7-101">Get-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="051d7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="051d7-102">SYNOPSIS</span></span>
<span data-ttu-id="051d7-103">以指定的名稱或連線監視器清單傳回連接監視器</span><span class="sxs-lookup"><span data-stu-id="051d7-103">Returns connection monitor with specified name or the list of connection monitors</span></span>

## <span data-ttu-id="051d7-104">句法</span><span class="sxs-lookup"><span data-stu-id="051d7-104">SYNTAX</span></span>

### <span data-ttu-id="051d7-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="051d7-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="051d7-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="051d7-106">SetByResource</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="051d7-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="051d7-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="051d7-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="051d7-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="051d7-109">說明</span><span class="sxs-lookup"><span data-stu-id="051d7-109">DESCRIPTION</span></span>
<span data-ttu-id="051d7-110">Get-AzNetworkWatcherConnectionMonitor Cmdlet 會以指定的名稱/resourceId 或與指定的網路監控程式/位置相對應的連線監視器清單傳回連接監視器。</span><span class="sxs-lookup"><span data-stu-id="051d7-110">The Get-AzNetworkWatcherConnectionMonitor cmdlet returns the connection monitor with the specified name / resourceId or the list of connection monitors corresponding to the specified network watcher / location.</span></span>

## <span data-ttu-id="051d7-111">示例</span><span class="sxs-lookup"><span data-stu-id="051d7-111">EXAMPLES</span></span>

### <span data-ttu-id="051d7-112">範例1</span><span class="sxs-lookup"><span data-stu-id="051d7-112">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm
```

<span data-ttu-id="051d7-113">名稱： cm Id：/subscriptions/00000000-0000-0000-0000-000000000000/resourceGro ups/NetworkWatcherRG/提供者/Microsoft. Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/cm Etag： W/"40961b58-e379-4204-a47b-0c477739b095" ProvisioningState：成功來源： {"ResourceId"： "/subscriptions/96e68903-0a56-4819-9987-8d08ad6 a1f99/resourceGroups/VarunRgCentralUSEUAP/提供者/Microsoft。 C ompute/virtualMachines/irinavm"，"Port"： 0} 目的地： {"位址"： "google.com"，"Port"： 80} MonitoringIntervalInSeconds：60自動啟動： True StartTime： 1/12/2018 7:19:28 PM MonitoringStatus：已停止的位置： centraluseuap 類型： Microsoft. Network/networkWatchers/connectionMonitors 標記： {"key1"： "value1"}</span><span class="sxs-lookup"><span data-stu-id="051d7-113">Name                        : cm Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/cm Etag                        : W/"40961b58-e379-4204-a47b-0c477739b095" ProvisioningState           : Succeeded Source                      : { "ResourceId": "/subscriptions/96e68903-0a56-4819-9987-8d08ad6 a1f99/resourceGroups/VarunRgCentralUSEUAP/providers/Microsoft.C ompute/virtualMachines/irinavm", "Port": 0 } Destination                 : { "Address": "google.com", "Port": 80 } MonitoringIntervalInSeconds : 60 AutoStart                   : True StartTime                   : 1/12/2018 7:19:28 PM MonitoringStatus            : Stopped Location                    : centraluseuap Type                        : Microsoft.Network/networkWatchers/connectionMonitors Tags                        : { "key1": "value1" }</span></span>

## <span data-ttu-id="051d7-114">參數</span><span class="sxs-lookup"><span data-stu-id="051d7-114">PARAMETERS</span></span>

### <span data-ttu-id="051d7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="051d7-115">-DefaultProfile</span></span>
<span data-ttu-id="051d7-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="051d7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="051d7-117">-位置</span><span class="sxs-lookup"><span data-stu-id="051d7-117">-Location</span></span>
<span data-ttu-id="051d7-118">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="051d7-118">Location of the network watcher.</span></span>

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

### <span data-ttu-id="051d7-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="051d7-119">-Name</span></span>
<span data-ttu-id="051d7-120">[連接監視器] 名稱。</span><span class="sxs-lookup"><span data-stu-id="051d7-120">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="051d7-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="051d7-121">-NetworkWatcher</span></span>
<span data-ttu-id="051d7-122">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="051d7-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="051d7-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="051d7-123">-NetworkWatcherName</span></span>
<span data-ttu-id="051d7-124">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="051d7-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="051d7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="051d7-125">-ResourceGroupName</span></span>
<span data-ttu-id="051d7-126">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="051d7-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="051d7-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="051d7-127">-ResourceId</span></span>
<span data-ttu-id="051d7-128">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="051d7-128">Resource ID.</span></span>

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

### <span data-ttu-id="051d7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="051d7-129">CommonParameters</span></span>
<span data-ttu-id="051d7-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="051d7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="051d7-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="051d7-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="051d7-132">輸入</span><span class="sxs-lookup"><span data-stu-id="051d7-132">INPUTS</span></span>

### <span data-ttu-id="051d7-133">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="051d7-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="051d7-134">System.object</span><span class="sxs-lookup"><span data-stu-id="051d7-134">System.String</span></span>

## <span data-ttu-id="051d7-135">輸出</span><span class="sxs-lookup"><span data-stu-id="051d7-135">OUTPUTS</span></span>

### <span data-ttu-id="051d7-136">PSConnectionMonitorResultV1 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="051d7-136">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="051d7-137">PSConnectionMonitorResultV2 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="051d7-137">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="051d7-138">筆記</span><span class="sxs-lookup"><span data-stu-id="051d7-138">NOTES</span></span>

## <span data-ttu-id="051d7-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="051d7-139">RELATED LINKS</span></span>
