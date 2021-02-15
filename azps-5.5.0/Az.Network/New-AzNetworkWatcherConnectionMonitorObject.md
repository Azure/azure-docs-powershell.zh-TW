---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorObject.md
ms.openlocfilehash: 06c20432821336b57764d70b5747759b7517801f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142151"
---
# <span data-ttu-id="d553c-101">New-AzNetworkWatcherConnectionMonitorObject</span><span class="sxs-lookup"><span data-stu-id="d553c-101">New-AzNetworkWatcherConnectionMonitorObject</span></span>

## <span data-ttu-id="d553c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d553c-102">SYNOPSIS</span></span>
<span data-ttu-id="d553c-103">建立連線監視 V2 物件。</span><span class="sxs-lookup"><span data-stu-id="d553c-103">Create a connection monitor V2 object.</span></span>

## <span data-ttu-id="d553c-104">句法</span><span class="sxs-lookup"><span data-stu-id="d553c-104">SYNTAX</span></span>

### <span data-ttu-id="d553c-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d553c-105">SetByResource</span></span>
```
New-AzNetworkWatcherConnectionMonitorObject -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d553c-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="d553c-106">SetByName</span></span>
```
New-AzNetworkWatcherConnectionMonitorObject -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d553c-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="d553c-107">SetByLocation</span></span>
```
New-AzNetworkWatcherConnectionMonitorObject -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d553c-108">說明</span><span class="sxs-lookup"><span data-stu-id="d553c-108">DESCRIPTION</span></span>
<span data-ttu-id="d553c-109">New-AzNetworkWatcherConnectionMonitorObject Cmdlet 會建立連接監視器 V2 物件。</span><span class="sxs-lookup"><span data-stu-id="d553c-109">The New-AzNetworkWatcherConnectionMonitorObject cmdlet creates a connection monitor V2 object.</span></span>

## <span data-ttu-id="d553c-110">示例</span><span class="sxs-lookup"><span data-stu-id="d553c-110">EXAMPLES</span></span>

### <span data-ttu-id="d553c-111">範例1</span><span class="sxs-lookup"><span data-stu-id="d553c-111">Example 1</span></span>
```powershell
PS> $cmtest = New-AzNetworkWatcherConnectionMonitorObject -Location westcentralus -Name cmV2test -TestGroup $testGroup1, $testGroup2 -Tag @{"name" = "value"}
PS> $cmtest
```

<span data-ttu-id="d553c-112">NetworkWatcherName : NetworkWatcher_westcentralus ResourceGroupName : NetworkWatcherRG Name : cmV2test TestGroups : [ { "Name": "testGroup1", "Disable": false, "TestConfigurations": [ { "Name": "tcpTC", "TestFrequencySec": 60, "ProtocolConfiguration": { "Port": 80, "DisableTraceRoute": false }, "SuccessThreshold": { "ChecksFailedPercent": 20, "RoundTripTimeMs": 5 } }, { "Name": "icmpTC", "TestFrequencySec": 30, "PreferredIPVersion": "IPv4", "ProtocolConfiguration": { "DisableTraceRoute": true } } ], "Sources": [ { "Name": "MultiTierApp0 (IrinaRGWestcentralus) ", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/RGW estcentralus/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" }, { "Name": "NPM-CommonEUS (er-lab) ", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/er-lab/p roviders/Microsoft.OperationalInsights/workspaces/NPM-CommonEUS", "Filter": { "Type": "Include", "Items": [ { "Type": "AgentAddress", "Address": "SEA-Cust50-VM01" }, { "Type": "AgentAddress", "Address": "WIN-P0HGNDO2S1B" } ] } } ], "Destinations": [ { "Name": "bingEndpoint", "Address": "bing.com" }, { "Name": "googleEndpoint", "Address": "google.com" } ] }, { "Name": "testGroup2", "Disable": false, "TestConfigurations": [ { "Name": "HTTPTC", "TestFrequencySec": 120, "ProtocolConfiguration": { "Port": 443, "Method": "GET", "RequestHeaders": [ { "Name": "Allow", "Value": "GET" } ], "ValidStatusCodeRanges": [ "2xx", "300-308" ], "PreferHTTPS": true }, "SuccessThreshold": { "ChecksFailedPercent": 20, "RoundTripTimeMs": 30 } } ], "Sources": [ { "Name": "MultiTierApp0 (IrinaRGWestcentralus) "，"ResourceId"： "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/IrinaRGW estcentralus/提供者/Microsoft. 計算/virtualMachines/MultiTierApp0"}]，"目的地"： [{"Name"： "googleEndpoint"，"Address"： "google.com"}]}] 輸出： null 記事： [值 "}</span><span class="sxs-lookup"><span data-stu-id="d553c-112">NetworkWatcherName : NetworkWatcher_westcentralus ResourceGroupName  : NetworkWatcherRG Name               : cmV2test TestGroups         : [ { "Name": "testGroup1", "Disable": false, "TestConfigurations": [ { "Name": "tcpTC", "TestFrequencySec": 60, "ProtocolConfiguration": { "Port": 80, "DisableTraceRoute": false }, "SuccessThreshold": { "ChecksFailedPercent": 20, "RoundTripTimeMs": 5 } }, { "Name": "icmpTC", "TestFrequencySec": 30, "PreferredIPVersion": "IPv4", "ProtocolConfiguration": { "DisableTraceRoute": true } } ], "Sources": [ { "Name": "MultiTierApp0(IrinaRGWestcentralus)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/RGW estcentralus/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" }, { "Name": "NPM-CommonEUS(er-lab)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/er-lab/p roviders/Microsoft.OperationalInsights/workspaces/NPM-CommonEUS", "Filter": { "Type": "Include", "Items": [ { "Type": "AgentAddress", "Address": "SEA-Cust50-VM01" }, { "Type": "AgentAddress", "Address": "WIN-P0HGNDO2S1B" } ] } } ], "Destinations": [ { "Name": "bingEndpoint", "Address": "bing.com" }, { "Name": "googleEndpoint", "Address": "google.com" } ] }, { "Name": "testGroup2", "Disable": false, "TestConfigurations": [ { "Name": "httpTC", "TestFrequencySec": 120, "ProtocolConfiguration": { "Port": 443, "Method": "GET", "RequestHeaders": [ { "Name": "Allow", "Value": "GET" } ], "ValidStatusCodeRanges": [ "2xx", "300-308" ], "PreferHTTPS": true }, "SuccessThreshold": { "ChecksFailedPercent": 20, "RoundTripTimeMs": 30 } } ], "Sources": [ { "Name": "MultiTierApp0(IrinaRGWestcentralus)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/IrinaRGW estcentralus/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" } ], "Destinations": [ { "Name": "googleEndpoint", "Address": "google.com" } ] } ] Outputs            : null Notes              : Tags               : { "name": "value" }</span></span>
        
   

## <span data-ttu-id="d553c-113">參數</span><span class="sxs-lookup"><span data-stu-id="d553c-113">PARAMETERS</span></span>

### <span data-ttu-id="d553c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d553c-114">-DefaultProfile</span></span>
<span data-ttu-id="d553c-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d553c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d553c-116">-位置</span><span class="sxs-lookup"><span data-stu-id="d553c-116">-Location</span></span>
<span data-ttu-id="d553c-117">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="d553c-117">Location of the network watcher.</span></span>

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

### <span data-ttu-id="d553c-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="d553c-118">-Name</span></span>
<span data-ttu-id="d553c-119">[連接監視器] 名稱。</span><span class="sxs-lookup"><span data-stu-id="d553c-119">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d553c-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d553c-120">-NetworkWatcher</span></span>
<span data-ttu-id="d553c-121">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="d553c-121">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d553c-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d553c-122">-NetworkWatcherName</span></span>
<span data-ttu-id="d553c-123">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="d553c-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="d553c-124">-記事</span><span class="sxs-lookup"><span data-stu-id="d553c-124">-Note</span></span>
<span data-ttu-id="d553c-125">與 [連線監視器] 相關聯的筆記。</span><span class="sxs-lookup"><span data-stu-id="d553c-125">Notes associated with connection monitor.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d553c-126">-輸出</span><span class="sxs-lookup"><span data-stu-id="d553c-126">-Output</span></span>
<span data-ttu-id="d553c-127">描述連線監視器的輸出目標。</span><span class="sxs-lookup"><span data-stu-id="d553c-127">Describes a connection monitor output destinations.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d553c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d553c-128">-ResourceGroupName</span></span>
<span data-ttu-id="d553c-129">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d553c-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="d553c-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="d553c-130">-Tag</span></span>
<span data-ttu-id="d553c-131">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="d553c-131">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d553c-132">-TestGroup</span><span class="sxs-lookup"><span data-stu-id="d553c-132">-TestGroup</span></span>
<span data-ttu-id="d553c-133">測試群組清單。</span><span class="sxs-lookup"><span data-stu-id="d553c-133">The list of test groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d553c-134">-確認</span><span class="sxs-lookup"><span data-stu-id="d553c-134">-Confirm</span></span>
<span data-ttu-id="d553c-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d553c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d553c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d553c-136">-WhatIf</span></span>
<span data-ttu-id="d553c-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d553c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d553c-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d553c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d553c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d553c-139">CommonParameters</span></span>
<span data-ttu-id="d553c-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d553c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d553c-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d553c-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d553c-142">輸入</span><span class="sxs-lookup"><span data-stu-id="d553c-142">INPUTS</span></span>

### <span data-ttu-id="d553c-143">所有</span><span class="sxs-lookup"><span data-stu-id="d553c-143">None</span></span>

## <span data-ttu-id="d553c-144">輸出</span><span class="sxs-lookup"><span data-stu-id="d553c-144">OUTPUTS</span></span>

### <span data-ttu-id="d553c-145">PSNetworkWatcherConnectionMonitorObject 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d553c-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorObject</span></span>

## <span data-ttu-id="d553c-146">筆記</span><span class="sxs-lookup"><span data-stu-id="d553c-146">NOTES</span></span>

## <span data-ttu-id="d553c-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="d553c-147">RELATED LINKS</span></span>
