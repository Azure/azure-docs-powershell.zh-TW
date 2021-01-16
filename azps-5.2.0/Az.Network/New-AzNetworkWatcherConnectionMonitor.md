---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: b84d11f259ffbf606bf0538a2ff71f6e9999db0a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98276719"
---
# <span data-ttu-id="862f2-101">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="862f2-101">New-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="862f2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="862f2-102">SYNOPSIS</span></span>
<span data-ttu-id="862f2-103">建立連接監視器資源。</span><span class="sxs-lookup"><span data-stu-id="862f2-103">Creates a connection monitor resource.</span></span>

## <span data-ttu-id="862f2-104">句法</span><span class="sxs-lookup"><span data-stu-id="862f2-104">SYNTAX</span></span>

### <span data-ttu-id="862f2-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="862f2-105">SetByName (Default)</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="862f2-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="862f2-106">SetByResource</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="862f2-107">SetByResourceV2</span><span class="sxs-lookup"><span data-stu-id="862f2-107">SetByResourceV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="862f2-108">SetByNameV2</span><span class="sxs-lookup"><span data-stu-id="862f2-108">SetByNameV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="862f2-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="862f2-109">SetByLocation</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="862f2-110">SetByLocationV2</span><span class="sxs-lookup"><span data-stu-id="862f2-110">SetByLocationV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="862f2-111">SetByConnectionMonitorV2Object</span><span class="sxs-lookup"><span data-stu-id="862f2-111">SetByConnectionMonitorV2Object</span></span>
```
New-AzNetworkWatcherConnectionMonitor [-ConnectionMonitor <PSNetworkWatcherConnectionMonitorObject>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="862f2-112">說明</span><span class="sxs-lookup"><span data-stu-id="862f2-112">DESCRIPTION</span></span>
<span data-ttu-id="862f2-113">New-AzNetworkWatcherConnectionMonitor Cmdlet 會為指定的來源和目的地 (SingleSourcedestination 連接監視器) 或一組測試組 (MultiEndpointConnectionMonitor) 建立連線監視器資源。</span><span class="sxs-lookup"><span data-stu-id="862f2-113">The New-AzNetworkWatcherConnectionMonitor cmdlet creates a connection monitor resource for specified source and destination (SingleSourcedestination connection monitor) or set of test groups (MultiEndpointConnectionMonitor).</span></span>

## <span data-ttu-id="862f2-114">示例</span><span class="sxs-lookup"><span data-stu-id="862f2-114">EXAMPLES</span></span>

### <span data-ttu-id="862f2-115">範例1</span><span class="sxs-lookup"><span data-stu-id="862f2-115">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm -DestinationAddress bing.com -DestinationPort 80
```

<span data-ttu-id="862f2-116">名稱： cm Id：/subscriptions/00000000-0000-0000-0000-000000000000/resourceGro ups/NetworkWatcherRG/提供者/Microsoft. Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/t1 Etag： W/"e86b28cf-b907-4475-a8b7-34d310367694" ProvisioningState：成功來源： {"ResourceId"： "/subscriptions/00000000-0000-0000-0000-0000000 00000/resourceGroups/RgCentralUSEUAP/提供者/Microsoft。Compute/virtualMachines/vm "，" 埠 "： 0} 目的地： {" 位址 "：" bing.com "，" Port "： 80} MonitoringIntervalInSeconds：60自動啟動： True StartTime： 1/12/2018 7:13:11 PM MonitoringStatus：執行位置： centraluseuap 類型： Microsoft. Network/networkWatchers/connectionMonitors 標記： {}</span><span class="sxs-lookup"><span data-stu-id="862f2-116">Name                        : cm Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/t1 Etag                        : W/"e86b28cf-b907-4475-a8b7-34d310367694" ProvisioningState           : Succeeded Source                      : { "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000 00000/resourceGroups/RgCentralUSEUAP/providers/Microsoft .Compute/virtualMachines/vm", "Port": 0 } Destination                 : { "Address": "bing.com", "Port": 80 } MonitoringIntervalInSeconds : 60 AutoStart                   : True StartTime                   : 1/12/2018 7:13:11 PM MonitoringStatus            : Running Location                    : centraluseuap Type                        : Microsoft.Network/networkWatchers/connectionMonitors Tags                        : {}</span></span>

## <span data-ttu-id="862f2-117">參數</span><span class="sxs-lookup"><span data-stu-id="862f2-117">PARAMETERS</span></span>

### <span data-ttu-id="862f2-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="862f2-118">-AsJob</span></span>
<span data-ttu-id="862f2-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="862f2-119">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="862f2-120">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="862f2-120">-ConfigureOnly</span></span>
<span data-ttu-id="862f2-121">設定連接監視器，但不啟動</span><span class="sxs-lookup"><span data-stu-id="862f2-121">Configure connection monitor, but do not start it</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="862f2-122">-ConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="862f2-122">-ConnectionMonitor</span></span>
<span data-ttu-id="862f2-123">[連接監視器] 物件。</span><span class="sxs-lookup"><span data-stu-id="862f2-123">Connection monitor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorObject
Parameter Sets: SetByConnectionMonitorV2Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="862f2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="862f2-124">-DefaultProfile</span></span>
<span data-ttu-id="862f2-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="862f2-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="862f2-126">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="862f2-126">-DestinationAddress</span></span>
<span data-ttu-id="862f2-127">[連線監視器] 目的地 (IP 或功能變數名稱) 的位址。</span><span class="sxs-lookup"><span data-stu-id="862f2-127">Address of the connection monitor destination (IP or domain name).</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="862f2-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="862f2-128">-DestinationPort</span></span>
<span data-ttu-id="862f2-129">[連線監視器] 使用的目的地埠。</span><span class="sxs-lookup"><span data-stu-id="862f2-129">The destination port used by connection monitor.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="862f2-130">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="862f2-130">-DestinationResourceId</span></span>
<span data-ttu-id="862f2-131">使用 [連線監視器] 作為目的地的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="862f2-131">The ID of the resource used as the destination by connection monitor.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="862f2-132">-Force</span><span class="sxs-lookup"><span data-stu-id="862f2-132">-Force</span></span>
<span data-ttu-id="862f2-133">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="862f2-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="862f2-134">-位置</span><span class="sxs-lookup"><span data-stu-id="862f2-134">-Location</span></span>
<span data-ttu-id="862f2-135">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="862f2-135">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation, SetByLocationV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="862f2-136">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="862f2-136">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="862f2-137">監控間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="862f2-137">Monitoring interval in seconds.</span></span> <span data-ttu-id="862f2-138">預設值為60秒。</span><span class="sxs-lookup"><span data-stu-id="862f2-138">Default value is 60 seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="862f2-139">-名稱</span><span class="sxs-lookup"><span data-stu-id="862f2-139">-Name</span></span>
<span data-ttu-id="862f2-140">[連接監視器] 名稱。</span><span class="sxs-lookup"><span data-stu-id="862f2-140">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByResourceV2, SetByNameV2, SetByLocation, SetByLocationV2
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="862f2-141">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="862f2-141">-NetworkWatcher</span></span>
<span data-ttu-id="862f2-142">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="862f2-142">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource, SetByResourceV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="862f2-143">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="862f2-143">-NetworkWatcherName</span></span>
<span data-ttu-id="862f2-144">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="862f2-144">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByNameV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="862f2-145">-記事</span><span class="sxs-lookup"><span data-stu-id="862f2-145">-Note</span></span>
<span data-ttu-id="862f2-146">與 [連線監視器] 相關聯的筆記。</span><span class="sxs-lookup"><span data-stu-id="862f2-146">Notes associated with connection monitor.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceV2, SetByNameV2, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="862f2-147">-輸出</span><span class="sxs-lookup"><span data-stu-id="862f2-147">-Output</span></span>
<span data-ttu-id="862f2-148">描述連線監視器的輸出目標。</span><span class="sxs-lookup"><span data-stu-id="862f2-148">Describes a connection monitor output destinations.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject[]
Parameter Sets: SetByResourceV2, SetByNameV2, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="862f2-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="862f2-149">-ResourceGroupName</span></span>
<span data-ttu-id="862f2-150">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="862f2-150">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByNameV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="862f2-151">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="862f2-151">-SourcePort</span></span>
<span data-ttu-id="862f2-152">[連線監視器] 使用的來源埠。</span><span class="sxs-lookup"><span data-stu-id="862f2-152">The source port used by connection monitor.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="862f2-153">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="862f2-153">-SourceResourceId</span></span>
<span data-ttu-id="862f2-154">使用 [連線] 監視器作為來源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="862f2-154">The ID of the resource used as the source by connection monitor.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="862f2-155">-Tag</span><span class="sxs-lookup"><span data-stu-id="862f2-155">-Tag</span></span>
<span data-ttu-id="862f2-156">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="862f2-156">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: SetByName, SetByResource, SetByResourceV2, SetByNameV2, SetByLocation, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="862f2-157">-TestGroup</span><span class="sxs-lookup"><span data-stu-id="862f2-157">-TestGroup</span></span>
<span data-ttu-id="862f2-158">測試群組清單。</span><span class="sxs-lookup"><span data-stu-id="862f2-158">The list of test groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject[]
Parameter Sets: SetByResourceV2, SetByNameV2, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="862f2-159">-確認</span><span class="sxs-lookup"><span data-stu-id="862f2-159">-Confirm</span></span>
<span data-ttu-id="862f2-160">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="862f2-160">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="862f2-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="862f2-161">-WhatIf</span></span>
<span data-ttu-id="862f2-162">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="862f2-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="862f2-163">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="862f2-163">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="862f2-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="862f2-164">CommonParameters</span></span>
<span data-ttu-id="862f2-165">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="862f2-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="862f2-166">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="862f2-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="862f2-167">輸入</span><span class="sxs-lookup"><span data-stu-id="862f2-167">INPUTS</span></span>

### <span data-ttu-id="862f2-168">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="862f2-168">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="862f2-169">System.object</span><span class="sxs-lookup"><span data-stu-id="862f2-169">System.String</span></span>

### <span data-ttu-id="862f2-170">[System.object]. 清單 ' 1 [PSNetworkWatcherConnectionMonitorTestGroupObject，2.2.2.0，，版本 =，Culture = 中性，PublicKeyToken = null]]。）））））</span><span class="sxs-lookup"><span data-stu-id="862f2-170">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="862f2-171">[System.object]. 清單 ' 1 [PSNetworkWatcherConnectionMonitorOutputObject，2.2.2.0，，版本 =，Culture = 中性，PublicKeyToken = null]]。）））））</span><span class="sxs-lookup"><span data-stu-id="862f2-171">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="862f2-172">輸出</span><span class="sxs-lookup"><span data-stu-id="862f2-172">OUTPUTS</span></span>

### <span data-ttu-id="862f2-173">PSConnectionMonitorResultV1 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="862f2-173">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="862f2-174">PSConnectionMonitorResultV2 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="862f2-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="862f2-175">筆記</span><span class="sxs-lookup"><span data-stu-id="862f2-175">NOTES</span></span>

## <span data-ttu-id="862f2-176">相關連結</span><span class="sxs-lookup"><span data-stu-id="862f2-176">RELATED LINKS</span></span>
