---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 5b5d7cff963a8f2a5322f67f31cfb31166f75aa9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100131107"
---
# <span data-ttu-id="5a949-101">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5a949-101">Set-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="5a949-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5a949-102">SYNOPSIS</span></span>
<span data-ttu-id="5a949-103">更新連接監視器資源。</span><span class="sxs-lookup"><span data-stu-id="5a949-103">Updates connection monitor resource.</span></span>

## <span data-ttu-id="5a949-104">句法</span><span class="sxs-lookup"><span data-stu-id="5a949-104">SYNTAX</span></span>

### <span data-ttu-id="5a949-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="5a949-105">SetByName (Default)</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5a949-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="5a949-106">SetByResource</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5a949-107">SetByResourceV2</span><span class="sxs-lookup"><span data-stu-id="5a949-107">SetByResourceV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a949-108">SetByNameV2</span><span class="sxs-lookup"><span data-stu-id="5a949-108">SetByNameV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a949-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="5a949-109">SetByLocation</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a949-110">SetByLocationV2</span><span class="sxs-lookup"><span data-stu-id="5a949-110">SetByLocationV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a949-111">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5a949-111">SetByResourceId</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] -Tag <Hashtable> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a949-112">SetByResourceIdV2</span><span class="sxs-lookup"><span data-stu-id="5a949-112">SetByResourceIdV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String>
 -TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>
 -Output <PSNetworkWatcherConnectionMonitorOutputObject[]> -Note <String> -Tag <Hashtable> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a949-113">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="5a949-113">SetByInputObject</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a949-114">說明</span><span class="sxs-lookup"><span data-stu-id="5a949-114">DESCRIPTION</span></span>
<span data-ttu-id="5a949-115">Set-AzNetworkWatcherConnectionMonitor Cmdlet 會更新連接監視器資源。</span><span class="sxs-lookup"><span data-stu-id="5a949-115">The Set-AzNetworkWatcherConnectionMonitor cmdlet updates connection monitor resource.</span></span>

## <span data-ttu-id="5a949-116">示例</span><span class="sxs-lookup"><span data-stu-id="5a949-116">EXAMPLES</span></span>

### <span data-ttu-id="5a949-117">範例1：更新連線監視者</span><span class="sxs-lookup"><span data-stu-id="5a949-117">Example 1: Update a connection monitor</span></span>
```
PS C:\> Set-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm
-DestinationAddress google.com -DestinationPort 80 -Tag @{"key1" = "value1"}

Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/cm
Etag                        : W/"5b2b20e8-0ce0-417e-9607-76208149bb67"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000
                                00000/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMach
                                ines/vm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "google.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:19:28 PM
MonitoringStatus            : Running
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {
                                "key1": "value1"
                              }
```

<span data-ttu-id="5a949-118">在這個範例中，我們會透過變更 destinationAddress 及新增標籤來更新現有的連線監視器。</span><span class="sxs-lookup"><span data-stu-id="5a949-118">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="5a949-119">參數</span><span class="sxs-lookup"><span data-stu-id="5a949-119">PARAMETERS</span></span>

### <span data-ttu-id="5a949-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5a949-120">-AsJob</span></span>
<span data-ttu-id="5a949-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5a949-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5a949-122">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="5a949-122">-ConfigureOnly</span></span>
<span data-ttu-id="5a949-123">設定連接監視器，但不啟動</span><span class="sxs-lookup"><span data-stu-id="5a949-123">Configure connection monitor, but do not start it</span></span>

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

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a949-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a949-124">-DefaultProfile</span></span>
<span data-ttu-id="5a949-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5a949-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a949-126">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="5a949-126">-DestinationAddress</span></span>
<span data-ttu-id="5a949-127">[連線監視器] 目的地 (IP 或功能變數名稱) 的位址。</span><span class="sxs-lookup"><span data-stu-id="5a949-127">Address of the connection monitor destination (IP or domain name).</span></span>

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

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a949-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="5a949-128">-DestinationPort</span></span>
<span data-ttu-id="5a949-129">[連線監視器] 使用的目的地埠。</span><span class="sxs-lookup"><span data-stu-id="5a949-129">The destination port used by connection monitor.</span></span>

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

```yaml
Type: System.Int32
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a949-130">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="5a949-130">-DestinationResourceId</span></span>
<span data-ttu-id="5a949-131">使用 [連線監視器] 作為目的地的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="5a949-131">The ID of the resource used as the destination by connection monitor.</span></span>

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

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a949-132">-Force</span><span class="sxs-lookup"><span data-stu-id="5a949-132">-Force</span></span>
<span data-ttu-id="5a949-133">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="5a949-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="5a949-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a949-134">-InputObject</span></span>
<span data-ttu-id="5a949-135">[連接監視器] 物件。</span><span class="sxs-lookup"><span data-stu-id="5a949-135">Connection monitor object.</span></span>

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

### <span data-ttu-id="5a949-136">-位置</span><span class="sxs-lookup"><span data-stu-id="5a949-136">-Location</span></span>
<span data-ttu-id="5a949-137">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="5a949-137">Location of the network watcher.</span></span>

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

### <span data-ttu-id="5a949-138">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="5a949-138">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="5a949-139">監控間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="5a949-139">Monitoring interval in seconds.</span></span> <span data-ttu-id="5a949-140">預設值為60秒。</span><span class="sxs-lookup"><span data-stu-id="5a949-140">Default value is 60 seconds.</span></span>

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

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a949-141">-名稱</span><span class="sxs-lookup"><span data-stu-id="5a949-141">-Name</span></span>
<span data-ttu-id="5a949-142">[連接監視器] 名稱。</span><span class="sxs-lookup"><span data-stu-id="5a949-142">The connection monitor name.</span></span>

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

### <span data-ttu-id="5a949-143">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5a949-143">-NetworkWatcher</span></span>
<span data-ttu-id="5a949-144">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="5a949-144">The network watcher resource.</span></span>

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

### <span data-ttu-id="5a949-145">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="5a949-145">-NetworkWatcherName</span></span>
<span data-ttu-id="5a949-146">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="5a949-146">The name of network watcher.</span></span>

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

### <span data-ttu-id="5a949-147">-記事</span><span class="sxs-lookup"><span data-stu-id="5a949-147">-Note</span></span>
<span data-ttu-id="5a949-148">與 [連線監視器] 相關聯的筆記。</span><span class="sxs-lookup"><span data-stu-id="5a949-148">Notes associated with connection monitor.</span></span>

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

```yaml
Type: System.String
Parameter Sets: SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a949-149">-輸出</span><span class="sxs-lookup"><span data-stu-id="5a949-149">-Output</span></span>
<span data-ttu-id="5a949-150">描述連線監視器的輸出目標。</span><span class="sxs-lookup"><span data-stu-id="5a949-150">Describes a connection monitor output destinations.</span></span>

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

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject[]
Parameter Sets: SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a949-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a949-151">-ResourceGroupName</span></span>
<span data-ttu-id="5a949-152">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5a949-152">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="5a949-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a949-153">-ResourceId</span></span>
<span data-ttu-id="5a949-154">ConnectionMonitor 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="5a949-154">ConnectionMonitor resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId, SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a949-155">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="5a949-155">-SourcePort</span></span>
<span data-ttu-id="5a949-156">[連線監視器] 使用的來源埠。</span><span class="sxs-lookup"><span data-stu-id="5a949-156">The source port used by connection monitor.</span></span>

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

```yaml
Type: System.Int32
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a949-157">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="5a949-157">-SourceResourceId</span></span>
<span data-ttu-id="5a949-158">使用 [連線] 監視器作為來源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="5a949-158">The ID of the resource used as the source by connection monitor.</span></span>

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

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a949-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="5a949-159">-Tag</span></span>
<span data-ttu-id="5a949-160">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="5a949-160">A hashtable which represents resource tags.</span></span>

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

```yaml
Type: System.Collections.Hashtable
Parameter Sets: SetByResourceId, SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a949-161">-TestGroup</span><span class="sxs-lookup"><span data-stu-id="5a949-161">-TestGroup</span></span>
<span data-ttu-id="5a949-162">測試群組清單。</span><span class="sxs-lookup"><span data-stu-id="5a949-162">The list of test groups.</span></span>

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

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject[]
Parameter Sets: SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a949-163">-確認</span><span class="sxs-lookup"><span data-stu-id="5a949-163">-Confirm</span></span>
<span data-ttu-id="5a949-164">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5a949-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a949-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a949-165">-WhatIf</span></span>
<span data-ttu-id="5a949-166">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5a949-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a949-167">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5a949-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a949-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a949-168">CommonParameters</span></span>
<span data-ttu-id="5a949-169">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5a949-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a949-170">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5a949-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a949-171">輸入</span><span class="sxs-lookup"><span data-stu-id="5a949-171">INPUTS</span></span>

### <span data-ttu-id="5a949-172">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5a949-172">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="5a949-173">System.object</span><span class="sxs-lookup"><span data-stu-id="5a949-173">System.String</span></span>

### <span data-ttu-id="5a949-174">PSConnectionMonitorResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5a949-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="5a949-175">輸出</span><span class="sxs-lookup"><span data-stu-id="5a949-175">OUTPUTS</span></span>

### <span data-ttu-id="5a949-176">PSConnectionMonitorResultV1 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5a949-176">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="5a949-177">PSConnectionMonitorResultV2 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5a949-177">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="5a949-178">筆記</span><span class="sxs-lookup"><span data-stu-id="5a949-178">NOTES</span></span>

## <span data-ttu-id="5a949-179">相關連結</span><span class="sxs-lookup"><span data-stu-id="5a949-179">RELATED LINKS</span></span>
