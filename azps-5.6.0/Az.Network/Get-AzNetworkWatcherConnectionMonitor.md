---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 30ab203f50df9e712792e216a1b4ecf1c5378b2e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902530"
---
# <span data-ttu-id="22dee-101">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="22dee-101">Get-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="22dee-102">簡介</span><span class="sxs-lookup"><span data-stu-id="22dee-102">SYNOPSIS</span></span>
<span data-ttu-id="22dee-103">使用指定的名稱或連接監視器清單來返回連接監視器</span><span class="sxs-lookup"><span data-stu-id="22dee-103">Returns connection monitor with specified name or the list of connection monitors</span></span>

## <span data-ttu-id="22dee-104">語法</span><span class="sxs-lookup"><span data-stu-id="22dee-104">SYNTAX</span></span>

### <span data-ttu-id="22dee-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="22dee-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22dee-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="22dee-106">SetByResource</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22dee-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="22dee-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22dee-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="22dee-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="22dee-109">描述</span><span class="sxs-lookup"><span data-stu-id="22dee-109">DESCRIPTION</span></span>
<span data-ttu-id="22dee-110">Cmdlet Get-AzNetworkWatcherConnectionMonitor會以指定的名稱/resourceId 或對應到指定網路監視程式/位置的連接監視器清單，來返回連接監視器。</span><span class="sxs-lookup"><span data-stu-id="22dee-110">The Get-AzNetworkWatcherConnectionMonitor cmdlet returns the connection monitor with the specified name / resourceId or the list of connection monitors corresponding to the specified network watcher / location.</span></span>

## <span data-ttu-id="22dee-111">例子</span><span class="sxs-lookup"><span data-stu-id="22dee-111">EXAMPLES</span></span>

### <span data-ttu-id="22dee-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="22dee-112">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm
```

<span data-ttu-id="22dee-113">名稱：Cm Id ：/subscriptions/00000000-0000-0000-0000-000000000000/resourceGro ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/cm Etag ： W/"40961b58-e379-4204-a47b-0c477 739b095" ProvisioningState ： 成功來源 ： { "ResourceId"： "/subscriptions/96e68903-0a56-4819-9987-8d08ad 6 a1f99/resourceGroups/VarunRgCentralUSEUAP/providers/Microsoft.C ompute/virtualMachines/i本卡"， "Port"： 0 } Destination ： { "Address"： "google.com"， "Port"： 80 } MonitoringIntervalInWatchs ： 60 AutoStart ： True StartTime ： 1/12/2018 7：19：28 PM MonitoringStatus ： 已停止的位置 ： centraluseuap Type ： Microsoft.Network/networkWatchers/connectionMonitors Tags ： { "key1"： "value1" }</span><span class="sxs-lookup"><span data-stu-id="22dee-113">Name                        : cm Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/cm Etag                        : W/"40961b58-e379-4204-a47b-0c477739b095" ProvisioningState           : Succeeded Source                      : { "ResourceId": "/subscriptions/96e68903-0a56-4819-9987-8d08ad6 a1f99/resourceGroups/VarunRgCentralUSEUAP/providers/Microsoft.C ompute/virtualMachines/irinavm", "Port": 0 } Destination                 : { "Address": "google.com", "Port": 80 } MonitoringIntervalInSeconds : 60 AutoStart                   : True StartTime                   : 1/12/2018 7:19:28 PM MonitoringStatus            : Stopped Location                    : centraluseuap Type                        : Microsoft.Network/networkWatchers/connectionMonitors Tags                        : { "key1": "value1" }</span></span>

## <span data-ttu-id="22dee-114">參數</span><span class="sxs-lookup"><span data-stu-id="22dee-114">PARAMETERS</span></span>

### <span data-ttu-id="22dee-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22dee-115">-DefaultProfile</span></span>
<span data-ttu-id="22dee-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="22dee-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22dee-117">-位置</span><span class="sxs-lookup"><span data-stu-id="22dee-117">-Location</span></span>
<span data-ttu-id="22dee-118">網路監視者的位置。</span><span class="sxs-lookup"><span data-stu-id="22dee-118">Location of the network watcher.</span></span>

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

### <span data-ttu-id="22dee-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="22dee-119">-Name</span></span>
<span data-ttu-id="22dee-120">連接監視器名稱。</span><span class="sxs-lookup"><span data-stu-id="22dee-120">The connection monitor name.</span></span>

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

### <span data-ttu-id="22dee-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="22dee-121">-NetworkWatcher</span></span>
<span data-ttu-id="22dee-122">網路監視程式資源。</span><span class="sxs-lookup"><span data-stu-id="22dee-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="22dee-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="22dee-123">-NetworkWatcherName</span></span>
<span data-ttu-id="22dee-124">網路監視者的名稱。</span><span class="sxs-lookup"><span data-stu-id="22dee-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="22dee-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22dee-125">-ResourceGroupName</span></span>
<span data-ttu-id="22dee-126">網路監視者資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="22dee-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="22dee-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22dee-127">-ResourceId</span></span>
<span data-ttu-id="22dee-128">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="22dee-128">Resource ID.</span></span>

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

### <span data-ttu-id="22dee-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22dee-129">CommonParameters</span></span>
<span data-ttu-id="22dee-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="22dee-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22dee-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22dee-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22dee-132">輸入</span><span class="sxs-lookup"><span data-stu-id="22dee-132">INPUTS</span></span>

### <span data-ttu-id="22dee-133">Microsoft.Azure.Commands.Network.models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="22dee-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="22dee-134">System.String</span><span class="sxs-lookup"><span data-stu-id="22dee-134">System.String</span></span>

## <span data-ttu-id="22dee-135">輸出</span><span class="sxs-lookup"><span data-stu-id="22dee-135">OUTPUTS</span></span>

### <span data-ttu-id="22dee-136">Microsoft.Azure.Commands.Network.models.PSConnectionMonitorResultV1</span><span class="sxs-lookup"><span data-stu-id="22dee-136">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="22dee-137">Microsoft.Azure.Commands.Network.models.PSConnectionMonitorResultV2</span><span class="sxs-lookup"><span data-stu-id="22dee-137">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="22dee-138">筆記</span><span class="sxs-lookup"><span data-stu-id="22dee-138">NOTES</span></span>

## <span data-ttu-id="22dee-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="22dee-139">RELATED LINKS</span></span>
