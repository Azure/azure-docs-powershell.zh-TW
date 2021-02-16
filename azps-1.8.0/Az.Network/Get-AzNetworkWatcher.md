---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcher.md
ms.openlocfilehash: cf5d5cba1b824af3187b681c7c87f26e4970b197
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402757"
---
# <span data-ttu-id="aa0c3-101">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="aa0c3-101">Get-AzNetworkWatcher</span></span>

## <span data-ttu-id="aa0c3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="aa0c3-102">SYNOPSIS</span></span>
<span data-ttu-id="aa0c3-103">獲得網路監視程式的屬性</span><span class="sxs-lookup"><span data-stu-id="aa0c3-103">Gets the properties of a Network Watcher</span></span>

## <span data-ttu-id="aa0c3-104">語法</span><span class="sxs-lookup"><span data-stu-id="aa0c3-104">SYNTAX</span></span>

### <span data-ttu-id="aa0c3-105">清單</span><span class="sxs-lookup"><span data-stu-id="aa0c3-105">List</span></span>
```
Get-AzNetworkWatcher [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="aa0c3-106">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="aa0c3-106">SetByLocation</span></span>
```
Get-AzNetworkWatcher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa0c3-107">描述</span><span class="sxs-lookup"><span data-stu-id="aa0c3-107">DESCRIPTION</span></span>
<span data-ttu-id="aa0c3-108">Cmdlet Get-AzNetworkWatcher一或多個 Azure Network Watcher 資源。</span><span class="sxs-lookup"><span data-stu-id="aa0c3-108">The Get-AzNetworkWatcher cmdlet gets one or more Azure Network Watcher resources.</span></span>

## <span data-ttu-id="aa0c3-109">例子</span><span class="sxs-lookup"><span data-stu-id="aa0c3-109">EXAMPLES</span></span>

### <span data-ttu-id="aa0c3-110">範例 1：取得網路監視程式</span><span class="sxs-lookup"><span data-stu-id="aa0c3-110">Example 1: Get a Network Watcher</span></span>
```
Get-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="aa0c3-111">在資源群組 NetworkWatcherRG 中NetworkWatcher_westcentralus名為 Network Watcher。</span><span class="sxs-lookup"><span data-stu-id="aa0c3-111">Gets the Network Watcher named NetworkWatcher_westcentralus in the resource group NetworkWatcherRG.</span></span>

### <span data-ttu-id="aa0c3-112">範例 2：使用篩選列出網路監視程式</span><span class="sxs-lookup"><span data-stu-id="aa0c3-112">Example 2: List Network Watchers using filtering</span></span>
```
Get-AzNetworkWatcher -Name NetworkWatcher*

Name              : NetworkWatcher_westcentralus1
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus1
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              :
ProvisioningState : Succeeded

Name              : NetworkWatcher_westcentralus2
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus2
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="aa0c3-113">從 「NetworkWatcher」開始進行網路監看程式</span><span class="sxs-lookup"><span data-stu-id="aa0c3-113">Gets the Network Watchers that start with "NetworkWatcher"</span></span>

## <span data-ttu-id="aa0c3-114">參數</span><span class="sxs-lookup"><span data-stu-id="aa0c3-114">PARAMETERS</span></span>

### <span data-ttu-id="aa0c3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa0c3-115">-DefaultProfile</span></span>
<span data-ttu-id="aa0c3-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="aa0c3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa0c3-117">-位置</span><span class="sxs-lookup"><span data-stu-id="aa0c3-117">-Location</span></span>
<span data-ttu-id="aa0c3-118">網路監視者的位置。</span><span class="sxs-lookup"><span data-stu-id="aa0c3-118">Location of the network watcher.</span></span>

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

### <span data-ttu-id="aa0c3-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="aa0c3-119">-Name</span></span>
<span data-ttu-id="aa0c3-120">網路監視者名稱。</span><span class="sxs-lookup"><span data-stu-id="aa0c3-120">The network watcher name.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="aa0c3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa0c3-121">-ResourceGroupName</span></span>
<span data-ttu-id="aa0c3-122">資源組名。</span><span class="sxs-lookup"><span data-stu-id="aa0c3-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="aa0c3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa0c3-123">CommonParameters</span></span>
<span data-ttu-id="aa0c3-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="aa0c3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa0c3-125">詳細資訊[請參閱about_CommonParameters。](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aa0c3-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa0c3-126">輸入</span><span class="sxs-lookup"><span data-stu-id="aa0c3-126">INPUTS</span></span>

### <span data-ttu-id="aa0c3-127">沒有</span><span class="sxs-lookup"><span data-stu-id="aa0c3-127">None</span></span>

## <span data-ttu-id="aa0c3-128">輸出</span><span class="sxs-lookup"><span data-stu-id="aa0c3-128">OUTPUTS</span></span>

### <span data-ttu-id="aa0c3-129">Microsoft.Azure.Commands.Network.models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="aa0c3-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="aa0c3-130">筆記</span><span class="sxs-lookup"><span data-stu-id="aa0c3-130">NOTES</span></span>
<span data-ttu-id="aa0c3-131">關鍵字：azure、azurerm、arm、資源、管理、管理員、網路、網路、網路監視者</span><span class="sxs-lookup"><span data-stu-id="aa0c3-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="aa0c3-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="aa0c3-132">RELATED LINKS</span></span>

[<span data-ttu-id="aa0c3-133">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="aa0c3-133">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="aa0c3-134">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="aa0c3-134">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="aa0c3-135">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="aa0c3-135">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="aa0c3-136">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="aa0c3-136">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="aa0c3-137">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="aa0c3-137">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="aa0c3-138">Get-AzNetworkWatcherTopwork</span><span class="sxs-lookup"><span data-stu-id="aa0c3-138">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="aa0c3-139">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="aa0c3-139">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="aa0c3-140">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="aa0c3-140">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="aa0c3-141">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="aa0c3-141">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="aa0c3-142">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="aa0c3-142">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="aa0c3-143">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="aa0c3-143">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="aa0c3-144">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="aa0c3-144">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="aa0c3-145">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="aa0c3-145">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="aa0c3-146">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="aa0c3-146">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="aa0c3-147">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="aa0c3-147">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="aa0c3-148">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="aa0c3-148">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="aa0c3-149">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="aa0c3-149">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="aa0c3-150">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="aa0c3-150">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="aa0c3-151">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="aa0c3-151">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="aa0c3-152">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="aa0c3-152">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="aa0c3-153">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="aa0c3-153">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="aa0c3-154">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="aa0c3-154">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="aa0c3-155">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="aa0c3-155">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="aa0c3-156">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="aa0c3-156">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="aa0c3-157">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="aa0c3-157">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="aa0c3-158">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="aa0c3-158">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="aa0c3-159">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="aa0c3-159">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
