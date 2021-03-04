---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcher.md
ms.openlocfilehash: 331665aae56715db41e4789e9d0c74fc253e7440
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906897"
---
# <span data-ttu-id="679f5-101">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="679f5-101">New-AzNetworkWatcher</span></span>

## <span data-ttu-id="679f5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="679f5-102">SYNOPSIS</span></span>
<span data-ttu-id="679f5-103">建立新網路監視程式資源。</span><span class="sxs-lookup"><span data-stu-id="679f5-103">Creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="679f5-104">語法</span><span class="sxs-lookup"><span data-stu-id="679f5-104">SYNTAX</span></span>

```
New-AzNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="679f5-105">描述</span><span class="sxs-lookup"><span data-stu-id="679f5-105">DESCRIPTION</span></span>
<span data-ttu-id="679f5-106">此New-AzNetworkWatcher Cmdlet 會建立一個新的網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="679f5-106">The New-AzNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="679f5-107">例子</span><span class="sxs-lookup"><span data-stu-id="679f5-107">EXAMPLES</span></span>

### <span data-ttu-id="679f5-108">範例 1：建立網路監視程式</span><span class="sxs-lookup"><span data-stu-id="679f5-108">Example 1: Create a Network Watcher</span></span>
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

<span data-ttu-id="679f5-109">此範例會于新建立的資源群組中建立新網路觀察程式。</span><span class="sxs-lookup"><span data-stu-id="679f5-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="679f5-110">請注意，每個訂閱每個地區只能建立一個網路監視程式。</span><span class="sxs-lookup"><span data-stu-id="679f5-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="679f5-111">參數</span><span class="sxs-lookup"><span data-stu-id="679f5-111">PARAMETERS</span></span>

### <span data-ttu-id="679f5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="679f5-112">-DefaultProfile</span></span>
<span data-ttu-id="679f5-113">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="679f5-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="679f5-114">-位置</span><span class="sxs-lookup"><span data-stu-id="679f5-114">-Location</span></span>
<span data-ttu-id="679f5-115">位置。</span><span class="sxs-lookup"><span data-stu-id="679f5-115">Location.</span></span>

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

### <span data-ttu-id="679f5-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="679f5-116">-Name</span></span>
<span data-ttu-id="679f5-117">網路監視者名稱。</span><span class="sxs-lookup"><span data-stu-id="679f5-117">The network watcher name.</span></span>

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

### <span data-ttu-id="679f5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="679f5-118">-ResourceGroupName</span></span>
<span data-ttu-id="679f5-119">資源組名。</span><span class="sxs-lookup"><span data-stu-id="679f5-119">The resource group name.</span></span>

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

### <span data-ttu-id="679f5-120">-標記</span><span class="sxs-lookup"><span data-stu-id="679f5-120">-Tag</span></span>
<span data-ttu-id="679f5-121">以雜湊表格形式建立索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="679f5-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="679f5-122">例如：@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="679f5-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="679f5-123">-確認</span><span class="sxs-lookup"><span data-stu-id="679f5-123">-Confirm</span></span>
<span data-ttu-id="679f5-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="679f5-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="679f5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="679f5-125">-WhatIf</span></span>
<span data-ttu-id="679f5-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="679f5-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="679f5-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="679f5-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="679f5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="679f5-128">CommonParameters</span></span>
<span data-ttu-id="679f5-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="679f5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="679f5-130">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="679f5-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="679f5-131">輸入</span><span class="sxs-lookup"><span data-stu-id="679f5-131">INPUTS</span></span>

### <span data-ttu-id="679f5-132">System.String</span><span class="sxs-lookup"><span data-stu-id="679f5-132">System.String</span></span>

### <span data-ttu-id="679f5-133">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="679f5-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="679f5-134">輸出</span><span class="sxs-lookup"><span data-stu-id="679f5-134">OUTPUTS</span></span>

### <span data-ttu-id="679f5-135">Microsoft.Azure.Commands.Network.models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="679f5-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="679f5-136">筆記</span><span class="sxs-lookup"><span data-stu-id="679f5-136">NOTES</span></span>
<span data-ttu-id="679f5-137">關鍵字：azure、azurerm、arm、resource、management、manager、network、network、network watcher</span><span class="sxs-lookup"><span data-stu-id="679f5-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="679f5-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="679f5-138">RELATED LINKS</span></span>

[<span data-ttu-id="679f5-139">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="679f5-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="679f5-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="679f5-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="679f5-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="679f5-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="679f5-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="679f5-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="679f5-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="679f5-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="679f5-144">Get-AzNetworkWatcherTopwork</span><span class="sxs-lookup"><span data-stu-id="679f5-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="679f5-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="679f5-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="679f5-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="679f5-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="679f5-147">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="679f5-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="679f5-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="679f5-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="679f5-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="679f5-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="679f5-150">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="679f5-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="679f5-151">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="679f5-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="679f5-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="679f5-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="679f5-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="679f5-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="679f5-154">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="679f5-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="679f5-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="679f5-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="679f5-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="679f5-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="679f5-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="679f5-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="679f5-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="679f5-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="679f5-159">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="679f5-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="679f5-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="679f5-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="679f5-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="679f5-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="679f5-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="679f5-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="679f5-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="679f5-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="679f5-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="679f5-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="679f5-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="679f5-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
