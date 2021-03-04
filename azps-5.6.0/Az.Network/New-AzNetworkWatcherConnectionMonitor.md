---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 18db8d01bd9c6c54b1fdf3957f25e12848e309ae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903557"
---
# <span data-ttu-id="3141c-101">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3141c-101">New-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="3141c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3141c-102">SYNOPSIS</span></span>
<span data-ttu-id="3141c-103">建立連接監視器資源。</span><span class="sxs-lookup"><span data-stu-id="3141c-103">Creates a connection monitor resource.</span></span>

## <span data-ttu-id="3141c-104">語法</span><span class="sxs-lookup"><span data-stu-id="3141c-104">SYNTAX</span></span>

### <span data-ttu-id="3141c-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="3141c-105">SetByName (Default)</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3141c-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="3141c-106">SetByResource</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3141c-107">SetByResourceV2</span><span class="sxs-lookup"><span data-stu-id="3141c-107">SetByResourceV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3141c-108">SetByNameV2</span><span class="sxs-lookup"><span data-stu-id="3141c-108">SetByNameV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3141c-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="3141c-109">SetByLocation</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3141c-110">SetByLocationV2</span><span class="sxs-lookup"><span data-stu-id="3141c-110">SetByLocationV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3141c-111">SetByConnectionMonitorV2Object</span><span class="sxs-lookup"><span data-stu-id="3141c-111">SetByConnectionMonitorV2Object</span></span>
```
New-AzNetworkWatcherConnectionMonitor [-ConnectionMonitor <PSNetworkWatcherConnectionMonitorObject>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3141c-112">描述</span><span class="sxs-lookup"><span data-stu-id="3141c-112">DESCRIPTION</span></span>
<span data-ttu-id="3141c-113">New-AzNetworkWatcherConnectionMonitor Cmdlet 會為指定的來源和目的地 (SingleSourcedestination 連接監視器) 或一組測試群組 (MultiEndpointConnectionMonitor) 建立連接監視器資源。</span><span class="sxs-lookup"><span data-stu-id="3141c-113">The New-AzNetworkWatcherConnectionMonitor cmdlet creates a connection monitor resource for specified source and destination (SingleSourcedestination connection monitor) or set of test groups (MultiEndpointConnectionMonitor).</span></span>

## <span data-ttu-id="3141c-114">例子</span><span class="sxs-lookup"><span data-stu-id="3141c-114">EXAMPLES</span></span>

### <span data-ttu-id="3141c-115">範例 1</span><span class="sxs-lookup"><span data-stu-id="3141c-115">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm -DestinationAddress bing.com -DestinationPort 80
```

<span data-ttu-id="3141c-116">名稱：Cm Id ：/subscriptions/0000000-0000-0000-00000-000000000/resourceGro ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/t1 Etag ：W/"e86b28cf-b907-2007 4475-a8b7-34d310367694" ProvisioningState： succeedingState ： { "ResourceId"： "/subscriptions/0000000-0000-0000-0000-0000000 00000/resourceGroups/RgCentralUSEUAP/providers/Microsoft。Compute/virtualMachines/vm"， "Port"： 0 } Destination ： { "Address"： "bing.com"， "Port"： 80 } MonitoringIntervalInWatchs ： 60 AutoStart ： True StartTime ： 1/12/2018 7：13：11 PM MonitoringStatus ： 執行位置 ： centraluseuap Type ： Microsoft.Network/networkWatchers/connectionMonitors Tags： {}</span><span class="sxs-lookup"><span data-stu-id="3141c-116">Name                        : cm Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/t1 Etag                        : W/"e86b28cf-b907-4475-a8b7-34d310367694" ProvisioningState           : Succeeded Source                      : { "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000 00000/resourceGroups/RgCentralUSEUAP/providers/Microsoft .Compute/virtualMachines/vm", "Port": 0 } Destination                 : { "Address": "bing.com", "Port": 80 } MonitoringIntervalInSeconds : 60 AutoStart                   : True StartTime                   : 1/12/2018 7:13:11 PM MonitoringStatus            : Running Location                    : centraluseuap Type                        : Microsoft.Network/networkWatchers/connectionMonitors Tags                        : {}</span></span>

## <span data-ttu-id="3141c-117">參數</span><span class="sxs-lookup"><span data-stu-id="3141c-117">PARAMETERS</span></span>

### <span data-ttu-id="3141c-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3141c-118">-AsJob</span></span>
<span data-ttu-id="3141c-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3141c-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3141c-120">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="3141c-120">-ConfigureOnly</span></span>
<span data-ttu-id="3141c-121">設定連接監視器，但不要啟動</span><span class="sxs-lookup"><span data-stu-id="3141c-121">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="3141c-122">-ConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3141c-122">-ConnectionMonitor</span></span>
<span data-ttu-id="3141c-123">連接監視器物件。</span><span class="sxs-lookup"><span data-stu-id="3141c-123">Connection monitor object.</span></span>

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

### <span data-ttu-id="3141c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3141c-124">-DefaultProfile</span></span>
<span data-ttu-id="3141c-125">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3141c-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3141c-126">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="3141c-126">-DestinationAddress</span></span>
<span data-ttu-id="3141c-127">連接監視器目的地位址 (IP 或功能變數名稱) 。</span><span class="sxs-lookup"><span data-stu-id="3141c-127">Address of the connection monitor destination (IP or domain name).</span></span>

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

### <span data-ttu-id="3141c-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="3141c-128">-DestinationPort</span></span>
<span data-ttu-id="3141c-129">連接監視器所使用的目的地埠。</span><span class="sxs-lookup"><span data-stu-id="3141c-129">The destination port used by connection monitor.</span></span>

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

### <span data-ttu-id="3141c-130">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="3141c-130">-DestinationResourceId</span></span>
<span data-ttu-id="3141c-131">使用連接監視器做為目的地的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="3141c-131">The ID of the resource used as the destination by connection monitor.</span></span>

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

### <span data-ttu-id="3141c-132">-強制</span><span class="sxs-lookup"><span data-stu-id="3141c-132">-Force</span></span>
<span data-ttu-id="3141c-133">如果您想要覆寫資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="3141c-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="3141c-134">-位置</span><span class="sxs-lookup"><span data-stu-id="3141c-134">-Location</span></span>
<span data-ttu-id="3141c-135">網路監視者的位置。</span><span class="sxs-lookup"><span data-stu-id="3141c-135">Location of the network watcher.</span></span>

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

### <span data-ttu-id="3141c-136">-MonitoringIntervalIn用秒</span><span class="sxs-lookup"><span data-stu-id="3141c-136">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="3141c-137">監控間隔以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="3141c-137">Monitoring interval in seconds.</span></span> <span data-ttu-id="3141c-138">預設值為 60 秒。</span><span class="sxs-lookup"><span data-stu-id="3141c-138">Default value is 60 seconds.</span></span>

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

### <span data-ttu-id="3141c-139">-名稱</span><span class="sxs-lookup"><span data-stu-id="3141c-139">-Name</span></span>
<span data-ttu-id="3141c-140">連接監視器名稱。</span><span class="sxs-lookup"><span data-stu-id="3141c-140">The connection monitor name.</span></span>

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

### <span data-ttu-id="3141c-141">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3141c-141">-NetworkWatcher</span></span>
<span data-ttu-id="3141c-142">網路監視程式資源。</span><span class="sxs-lookup"><span data-stu-id="3141c-142">The network watcher resource.</span></span>

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

### <span data-ttu-id="3141c-143">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="3141c-143">-NetworkWatcherName</span></span>
<span data-ttu-id="3141c-144">網路監視者的名稱。</span><span class="sxs-lookup"><span data-stu-id="3141c-144">The name of network watcher.</span></span>

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

### <span data-ttu-id="3141c-145">-注意</span><span class="sxs-lookup"><span data-stu-id="3141c-145">-Note</span></span>
<span data-ttu-id="3141c-146">與連接監視器相關聯的筆記。</span><span class="sxs-lookup"><span data-stu-id="3141c-146">Notes associated with connection monitor.</span></span>

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

### <span data-ttu-id="3141c-147">-輸出</span><span class="sxs-lookup"><span data-stu-id="3141c-147">-Output</span></span>
<span data-ttu-id="3141c-148">說明連接監視器的輸出目的地。</span><span class="sxs-lookup"><span data-stu-id="3141c-148">Describes a connection monitor output destinations.</span></span>

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

### <span data-ttu-id="3141c-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3141c-149">-ResourceGroupName</span></span>
<span data-ttu-id="3141c-150">網路監視者資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3141c-150">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="3141c-151">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="3141c-151">-SourcePort</span></span>
<span data-ttu-id="3141c-152">連接監視器使用的來源埠。</span><span class="sxs-lookup"><span data-stu-id="3141c-152">The source port used by connection monitor.</span></span>

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

### <span data-ttu-id="3141c-153">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="3141c-153">-SourceResourceId</span></span>
<span data-ttu-id="3141c-154">使用連接監視器做為來源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="3141c-154">The ID of the resource used as the source by connection monitor.</span></span>

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

### <span data-ttu-id="3141c-155">-標記</span><span class="sxs-lookup"><span data-stu-id="3141c-155">-Tag</span></span>
<span data-ttu-id="3141c-156">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="3141c-156">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="3141c-157">-TestGroup</span><span class="sxs-lookup"><span data-stu-id="3141c-157">-TestGroup</span></span>
<span data-ttu-id="3141c-158">測試群組清單。</span><span class="sxs-lookup"><span data-stu-id="3141c-158">The list of test groups.</span></span>

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

### <span data-ttu-id="3141c-159">-確認</span><span class="sxs-lookup"><span data-stu-id="3141c-159">-Confirm</span></span>
<span data-ttu-id="3141c-160">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3141c-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3141c-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3141c-161">-WhatIf</span></span>
<span data-ttu-id="3141c-162">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3141c-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3141c-163">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3141c-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3141c-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3141c-164">CommonParameters</span></span>
<span data-ttu-id="3141c-165">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3141c-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3141c-166">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3141c-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3141c-167">輸入</span><span class="sxs-lookup"><span data-stu-id="3141c-167">INPUTS</span></span>

### <span data-ttu-id="3141c-168">Microsoft.Azure.Commands.Network.models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3141c-168">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="3141c-169">System.String</span><span class="sxs-lookup"><span data-stu-id="3141c-169">System.String</span></span>

### <span data-ttu-id="3141c-170">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="3141c-170">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="3141c-171">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="3141c-171">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="3141c-172">輸出</span><span class="sxs-lookup"><span data-stu-id="3141c-172">OUTPUTS</span></span>

### <span data-ttu-id="3141c-173">Microsoft.Azure.Commands.Network.models.PSConnectionMonitorResultV1</span><span class="sxs-lookup"><span data-stu-id="3141c-173">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="3141c-174">Microsoft.Azure.Commands.Network.models.PSConnectionMonitorResultV2</span><span class="sxs-lookup"><span data-stu-id="3141c-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="3141c-175">筆記</span><span class="sxs-lookup"><span data-stu-id="3141c-175">NOTES</span></span>

## <span data-ttu-id="3141c-176">相關連結</span><span class="sxs-lookup"><span data-stu-id="3141c-176">RELATED LINKS</span></span>
