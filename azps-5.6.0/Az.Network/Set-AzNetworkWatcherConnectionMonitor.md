---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: e5f8e8f470570993433858a0aa1c165122c614e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916378"
---
# <span data-ttu-id="a3c7f-101">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a3c7f-101">Set-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="a3c7f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a3c7f-102">SYNOPSIS</span></span>
<span data-ttu-id="a3c7f-103">更新連接監視器資源。</span><span class="sxs-lookup"><span data-stu-id="a3c7f-103">Updates connection monitor resource.</span></span>

## <span data-ttu-id="a3c7f-104">語法</span><span class="sxs-lookup"><span data-stu-id="a3c7f-104">SYNTAX</span></span>

### <span data-ttu-id="a3c7f-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="a3c7f-105">SetByName (Default)</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a3c7f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="a3c7f-106">SetByResource</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a3c7f-107">SetByResourceV2</span><span class="sxs-lookup"><span data-stu-id="a3c7f-107">SetByResourceV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3c7f-108">SetByNameV2</span><span class="sxs-lookup"><span data-stu-id="a3c7f-108">SetByNameV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3c7f-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="a3c7f-109">SetByLocation</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3c7f-110">SetByLocationV2</span><span class="sxs-lookup"><span data-stu-id="a3c7f-110">SetByLocationV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3c7f-111">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a3c7f-111">SetByResourceId</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] -Tag <Hashtable> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3c7f-112">SetByResourceIdV2</span><span class="sxs-lookup"><span data-stu-id="a3c7f-112">SetByResourceIdV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String>
 -TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>
 -Output <PSNetworkWatcherConnectionMonitorOutputObject[]> -Note <String> -Tag <Hashtable> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3c7f-113">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="a3c7f-113">SetByInputObject</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3c7f-114">描述</span><span class="sxs-lookup"><span data-stu-id="a3c7f-114">DESCRIPTION</span></span>
<span data-ttu-id="a3c7f-115">Cmdlet Set-AzNetworkWatcherConnectionMonitor更新連接監視器資源。</span><span class="sxs-lookup"><span data-stu-id="a3c7f-115">The Set-AzNetworkWatcherConnectionMonitor cmdlet updates connection monitor resource.</span></span>

## <span data-ttu-id="a3c7f-116">例子</span><span class="sxs-lookup"><span data-stu-id="a3c7f-116">EXAMPLES</span></span>

### <span data-ttu-id="a3c7f-117">範例 1：更新連接監視器</span><span class="sxs-lookup"><span data-stu-id="a3c7f-117">Example 1: Update a connection monitor</span></span>
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

<span data-ttu-id="a3c7f-118">在此範例中，我們會變更 destinationAddress 並新增標記來更新現有的連接監視器。</span><span class="sxs-lookup"><span data-stu-id="a3c7f-118">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="a3c7f-119">參數</span><span class="sxs-lookup"><span data-stu-id="a3c7f-119">PARAMETERS</span></span>

### <span data-ttu-id="a3c7f-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3c7f-120">-AsJob</span></span>
<span data-ttu-id="a3c7f-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a3c7f-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a3c7f-122">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="a3c7f-122">-ConfigureOnly</span></span>
<span data-ttu-id="a3c7f-123">設定連接監視器，但不要啟動</span><span class="sxs-lookup"><span data-stu-id="a3c7f-123">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="a3c7f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3c7f-124">-DefaultProfile</span></span>
<span data-ttu-id="a3c7f-125">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a3c7f-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3c7f-126">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="a3c7f-126">-DestinationAddress</span></span>
<span data-ttu-id="a3c7f-127">連接監視器目的地位址 (IP 或功能變數名稱) 。</span><span class="sxs-lookup"><span data-stu-id="a3c7f-127">Address of the connection monitor destination (IP or domain name).</span></span>

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

### <span data-ttu-id="a3c7f-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="a3c7f-128">-DestinationPort</span></span>
<span data-ttu-id="a3c7f-129">連接監視器所使用的目的地埠。</span><span class="sxs-lookup"><span data-stu-id="a3c7f-129">The destination port used by connection monitor.</span></span>

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

### <span data-ttu-id="a3c7f-130">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="a3c7f-130">-DestinationResourceId</span></span>
<span data-ttu-id="a3c7f-131">使用連接監視器做為目的地的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a3c7f-131">The ID of the resource used as the destination by connection monitor.</span></span>

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

### <span data-ttu-id="a3c7f-132">-強制</span><span class="sxs-lookup"><span data-stu-id="a3c7f-132">-Force</span></span>
<span data-ttu-id="a3c7f-133">如果您想要覆寫資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="a3c7f-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="a3c7f-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3c7f-134">-InputObject</span></span>
<span data-ttu-id="a3c7f-135">連接監視器物件。</span><span class="sxs-lookup"><span data-stu-id="a3c7f-135">Connection monitor object.</span></span>

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

### <span data-ttu-id="a3c7f-136">-位置</span><span class="sxs-lookup"><span data-stu-id="a3c7f-136">-Location</span></span>
<span data-ttu-id="a3c7f-137">網路監視者的位置。</span><span class="sxs-lookup"><span data-stu-id="a3c7f-137">Location of the network watcher.</span></span>

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

### <span data-ttu-id="a3c7f-138">-MonitoringIntervalIn用秒</span><span class="sxs-lookup"><span data-stu-id="a3c7f-138">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="a3c7f-139">監控間隔以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="a3c7f-139">Monitoring interval in seconds.</span></span> <span data-ttu-id="a3c7f-140">預設值為 60 秒。</span><span class="sxs-lookup"><span data-stu-id="a3c7f-140">Default value is 60 seconds.</span></span>

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

### <span data-ttu-id="a3c7f-141">-名稱</span><span class="sxs-lookup"><span data-stu-id="a3c7f-141">-Name</span></span>
<span data-ttu-id="a3c7f-142">連接監視器名稱。</span><span class="sxs-lookup"><span data-stu-id="a3c7f-142">The connection monitor name.</span></span>

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

### <span data-ttu-id="a3c7f-143">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a3c7f-143">-NetworkWatcher</span></span>
<span data-ttu-id="a3c7f-144">網路監視程式資源。</span><span class="sxs-lookup"><span data-stu-id="a3c7f-144">The network watcher resource.</span></span>

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

### <span data-ttu-id="a3c7f-145">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="a3c7f-145">-NetworkWatcherName</span></span>
<span data-ttu-id="a3c7f-146">網路監視者的名稱。</span><span class="sxs-lookup"><span data-stu-id="a3c7f-146">The name of network watcher.</span></span>

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

### <span data-ttu-id="a3c7f-147">-注意</span><span class="sxs-lookup"><span data-stu-id="a3c7f-147">-Note</span></span>
<span data-ttu-id="a3c7f-148">與連接監視器相關聯的筆記。</span><span class="sxs-lookup"><span data-stu-id="a3c7f-148">Notes associated with connection monitor.</span></span>

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

### <span data-ttu-id="a3c7f-149">-輸出</span><span class="sxs-lookup"><span data-stu-id="a3c7f-149">-Output</span></span>
<span data-ttu-id="a3c7f-150">說明連接監視器的輸出目的地。</span><span class="sxs-lookup"><span data-stu-id="a3c7f-150">Describes a connection monitor output destinations.</span></span>

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

### <span data-ttu-id="a3c7f-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3c7f-151">-ResourceGroupName</span></span>
<span data-ttu-id="a3c7f-152">網路監視者資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a3c7f-152">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="a3c7f-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3c7f-153">-ResourceId</span></span>
<span data-ttu-id="a3c7f-154">ConnectionMonitor 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a3c7f-154">ConnectionMonitor resource ID.</span></span>

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

### <span data-ttu-id="a3c7f-155">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="a3c7f-155">-SourcePort</span></span>
<span data-ttu-id="a3c7f-156">連接監視器使用的來源埠。</span><span class="sxs-lookup"><span data-stu-id="a3c7f-156">The source port used by connection monitor.</span></span>

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

### <span data-ttu-id="a3c7f-157">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="a3c7f-157">-SourceResourceId</span></span>
<span data-ttu-id="a3c7f-158">使用連接監視器做為來源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a3c7f-158">The ID of the resource used as the source by connection monitor.</span></span>

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

### <span data-ttu-id="a3c7f-159">-標記</span><span class="sxs-lookup"><span data-stu-id="a3c7f-159">-Tag</span></span>
<span data-ttu-id="a3c7f-160">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="a3c7f-160">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="a3c7f-161">-TestGroup</span><span class="sxs-lookup"><span data-stu-id="a3c7f-161">-TestGroup</span></span>
<span data-ttu-id="a3c7f-162">測試群組清單。</span><span class="sxs-lookup"><span data-stu-id="a3c7f-162">The list of test groups.</span></span>

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

### <span data-ttu-id="a3c7f-163">-確認</span><span class="sxs-lookup"><span data-stu-id="a3c7f-163">-Confirm</span></span>
<span data-ttu-id="a3c7f-164">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a3c7f-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3c7f-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3c7f-165">-WhatIf</span></span>
<span data-ttu-id="a3c7f-166">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a3c7f-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3c7f-167">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a3c7f-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3c7f-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3c7f-168">CommonParameters</span></span>
<span data-ttu-id="a3c7f-169">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a3c7f-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3c7f-170">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a3c7f-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3c7f-171">輸入</span><span class="sxs-lookup"><span data-stu-id="a3c7f-171">INPUTS</span></span>

### <span data-ttu-id="a3c7f-172">Microsoft.Azure.Commands.Network.models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a3c7f-172">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="a3c7f-173">System.String</span><span class="sxs-lookup"><span data-stu-id="a3c7f-173">System.String</span></span>

### <span data-ttu-id="a3c7f-174">Microsoft.Azure.Commands.Network.models.PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="a3c7f-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="a3c7f-175">輸出</span><span class="sxs-lookup"><span data-stu-id="a3c7f-175">OUTPUTS</span></span>

### <span data-ttu-id="a3c7f-176">Microsoft.Azure.Commands.Network.models.PSConnectionMonitorResultV1</span><span class="sxs-lookup"><span data-stu-id="a3c7f-176">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="a3c7f-177">Microsoft.Azure.Commands.Network.models.PSConnectionMonitorResultV2</span><span class="sxs-lookup"><span data-stu-id="a3c7f-177">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="a3c7f-178">筆記</span><span class="sxs-lookup"><span data-stu-id="a3c7f-178">NOTES</span></span>

## <span data-ttu-id="a3c7f-179">相關連結</span><span class="sxs-lookup"><span data-stu-id="a3c7f-179">RELATED LINKS</span></span>
