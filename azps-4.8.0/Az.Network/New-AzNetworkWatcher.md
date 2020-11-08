---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcher.md
ms.openlocfilehash: 7c8f33d8339bb873b713acabd71ca57fe9107383
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970348"
---
# <span data-ttu-id="bc628-101">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bc628-101">New-AzNetworkWatcher</span></span>

## <span data-ttu-id="bc628-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bc628-102">SYNOPSIS</span></span>
<span data-ttu-id="bc628-103">建立新的網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="bc628-103">Creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="bc628-104">句法</span><span class="sxs-lookup"><span data-stu-id="bc628-104">SYNTAX</span></span>

```
New-AzNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc628-105">說明</span><span class="sxs-lookup"><span data-stu-id="bc628-105">DESCRIPTION</span></span>
<span data-ttu-id="bc628-106">New-AzNetworkWatcher Cmdlet 會建立新的網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="bc628-106">The New-AzNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="bc628-107">示例</span><span class="sxs-lookup"><span data-stu-id="bc628-107">EXAMPLES</span></span>

### <span data-ttu-id="bc628-108">範例1：建立網路觀察程式</span><span class="sxs-lookup"><span data-stu-id="bc628-108">Example 1: Create a Network Watcher</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"7cf1f2fe-8445-4aa7-9bf5-c15347282c39"
Location          : westcentralus
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="bc628-109">這個範例會在新建立的資源群組內建立新的網路觀察程式。</span><span class="sxs-lookup"><span data-stu-id="bc628-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="bc628-110">請注意，每個訂閱只能建立一個網路觀察程式。</span><span class="sxs-lookup"><span data-stu-id="bc628-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="bc628-111">參數</span><span class="sxs-lookup"><span data-stu-id="bc628-111">PARAMETERS</span></span>

### <span data-ttu-id="bc628-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc628-112">-DefaultProfile</span></span>
<span data-ttu-id="bc628-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bc628-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc628-114">-位置</span><span class="sxs-lookup"><span data-stu-id="bc628-114">-Location</span></span>
<span data-ttu-id="bc628-115">位於.</span><span class="sxs-lookup"><span data-stu-id="bc628-115">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc628-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="bc628-116">-Name</span></span>
<span data-ttu-id="bc628-117">網路觀察程式名稱。</span><span class="sxs-lookup"><span data-stu-id="bc628-117">The network watcher name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc628-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc628-118">-ResourceGroupName</span></span>
<span data-ttu-id="bc628-119">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bc628-119">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc628-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="bc628-120">-Tag</span></span>
<span data-ttu-id="bc628-121">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="bc628-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="bc628-122">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="bc628-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="bc628-123">-確認</span><span class="sxs-lookup"><span data-stu-id="bc628-123">-Confirm</span></span>
<span data-ttu-id="bc628-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bc628-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc628-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc628-125">-WhatIf</span></span>
<span data-ttu-id="bc628-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bc628-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc628-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bc628-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc628-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc628-128">CommonParameters</span></span>
<span data-ttu-id="bc628-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bc628-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc628-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bc628-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc628-131">輸入</span><span class="sxs-lookup"><span data-stu-id="bc628-131">INPUTS</span></span>

### <span data-ttu-id="bc628-132">System.object</span><span class="sxs-lookup"><span data-stu-id="bc628-132">System.String</span></span>

### <span data-ttu-id="bc628-133">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="bc628-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="bc628-134">輸出</span><span class="sxs-lookup"><span data-stu-id="bc628-134">OUTPUTS</span></span>

### <span data-ttu-id="bc628-135">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="bc628-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="bc628-136">筆記</span><span class="sxs-lookup"><span data-stu-id="bc628-136">NOTES</span></span>
<span data-ttu-id="bc628-137">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式</span><span class="sxs-lookup"><span data-stu-id="bc628-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="bc628-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="bc628-138">RELATED LINKS</span></span>

[<span data-ttu-id="bc628-139">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bc628-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="bc628-140">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bc628-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="bc628-141">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bc628-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="bc628-142">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="bc628-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="bc628-143">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="bc628-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="bc628-144">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="bc628-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="bc628-145">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="bc628-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="bc628-146">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bc628-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bc628-147">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="bc628-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="bc628-148">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bc628-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bc628-149">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bc628-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bc628-150">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bc628-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bc628-151">新-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="bc628-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="bc628-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="bc628-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="bc628-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="bc628-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="bc628-154">停止 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bc628-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="bc628-155">開始-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bc628-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="bc628-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bc628-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="bc628-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="bc628-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="bc628-158">移除-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bc628-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="bc628-159">新-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bc628-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="bc628-160">AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="bc628-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="bc628-161">AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="bc628-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="bc628-162">AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="bc628-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="bc628-163">AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="bc628-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="bc628-164">AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="bc628-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="bc628-165">AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bc628-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
