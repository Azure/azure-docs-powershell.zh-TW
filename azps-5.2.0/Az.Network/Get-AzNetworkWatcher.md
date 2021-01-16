---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcher.md
ms.openlocfilehash: dc8d3a3db0eaa76974e02a62111b022ed81524b0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98284272"
---
# <span data-ttu-id="a3fd6-101">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a3fd6-101">Get-AzNetworkWatcher</span></span>

## <span data-ttu-id="a3fd6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a3fd6-102">SYNOPSIS</span></span>
<span data-ttu-id="a3fd6-103">取得網路觀察程式的屬性</span><span class="sxs-lookup"><span data-stu-id="a3fd6-103">Gets the properties of a Network Watcher</span></span>

## <span data-ttu-id="a3fd6-104">句法</span><span class="sxs-lookup"><span data-stu-id="a3fd6-104">SYNTAX</span></span>

### <span data-ttu-id="a3fd6-105">清單</span><span class="sxs-lookup"><span data-stu-id="a3fd6-105">List</span></span>
```
Get-AzNetworkWatcher [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a3fd6-106">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="a3fd6-106">SetByLocation</span></span>
```
Get-AzNetworkWatcher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3fd6-107">說明</span><span class="sxs-lookup"><span data-stu-id="a3fd6-107">DESCRIPTION</span></span>
<span data-ttu-id="a3fd6-108">Get-AzNetworkWatcher Cmdlet 會取得一或多個 Azure 網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="a3fd6-108">The Get-AzNetworkWatcher cmdlet gets one or more Azure Network Watcher resources.</span></span>

## <span data-ttu-id="a3fd6-109">示例</span><span class="sxs-lookup"><span data-stu-id="a3fd6-109">EXAMPLES</span></span>

### <span data-ttu-id="a3fd6-110">範例1：取得網路觀察程式</span><span class="sxs-lookup"><span data-stu-id="a3fd6-110">Example 1: Get a Network Watcher</span></span>
```
Get-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="a3fd6-111">在 [資源群組 NetworkWatcherRG] 中取得名為 NetworkWatcher_westcentralus 的網路觀察程式。</span><span class="sxs-lookup"><span data-stu-id="a3fd6-111">Gets the Network Watcher named NetworkWatcher_westcentralus in the resource group NetworkWatcherRG.</span></span>

### <span data-ttu-id="a3fd6-112">範例2：使用篩選列出網路觀察器</span><span class="sxs-lookup"><span data-stu-id="a3fd6-112">Example 2: List Network Watchers using filtering</span></span>
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

<span data-ttu-id="a3fd6-113">取得以 "NetworkWatcher" 開頭的網路觀察程式</span><span class="sxs-lookup"><span data-stu-id="a3fd6-113">Gets the Network Watchers that start with "NetworkWatcher"</span></span>

## <span data-ttu-id="a3fd6-114">參數</span><span class="sxs-lookup"><span data-stu-id="a3fd6-114">PARAMETERS</span></span>

### <span data-ttu-id="a3fd6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3fd6-115">-DefaultProfile</span></span>
<span data-ttu-id="a3fd6-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a3fd6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3fd6-117">-位置</span><span class="sxs-lookup"><span data-stu-id="a3fd6-117">-Location</span></span>
<span data-ttu-id="a3fd6-118">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="a3fd6-118">Location of the network watcher.</span></span>

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

### <span data-ttu-id="a3fd6-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="a3fd6-119">-Name</span></span>
<span data-ttu-id="a3fd6-120">網路觀察程式名稱。</span><span class="sxs-lookup"><span data-stu-id="a3fd6-120">The network watcher name.</span></span>

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

### <span data-ttu-id="a3fd6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3fd6-121">-ResourceGroupName</span></span>
<span data-ttu-id="a3fd6-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a3fd6-122">The resource group name.</span></span>

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

### <span data-ttu-id="a3fd6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3fd6-123">CommonParameters</span></span>
<span data-ttu-id="a3fd6-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a3fd6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3fd6-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a3fd6-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3fd6-126">輸入</span><span class="sxs-lookup"><span data-stu-id="a3fd6-126">INPUTS</span></span>

### <span data-ttu-id="a3fd6-127">所有</span><span class="sxs-lookup"><span data-stu-id="a3fd6-127">None</span></span>

## <span data-ttu-id="a3fd6-128">輸出</span><span class="sxs-lookup"><span data-stu-id="a3fd6-128">OUTPUTS</span></span>

### <span data-ttu-id="a3fd6-129">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a3fd6-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="a3fd6-130">筆記</span><span class="sxs-lookup"><span data-stu-id="a3fd6-130">NOTES</span></span>
<span data-ttu-id="a3fd6-131">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式</span><span class="sxs-lookup"><span data-stu-id="a3fd6-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span> 

## <span data-ttu-id="a3fd6-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="a3fd6-132">RELATED LINKS</span></span>

[<span data-ttu-id="a3fd6-133">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a3fd6-133">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="a3fd6-134">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a3fd6-134">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="a3fd6-135">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a3fd6-135">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="a3fd6-136">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="a3fd6-136">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="a3fd6-137">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="a3fd6-137">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="a3fd6-138">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="a3fd6-138">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="a3fd6-139">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="a3fd6-139">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="a3fd6-140">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a3fd6-140">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a3fd6-141">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="a3fd6-141">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="a3fd6-142">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a3fd6-142">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a3fd6-143">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a3fd6-143">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a3fd6-144">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a3fd6-144">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a3fd6-145">新-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="a3fd6-145">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="a3fd6-146">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="a3fd6-146">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="a3fd6-147">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="a3fd6-147">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="a3fd6-148">停止 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a3fd6-148">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a3fd6-149">開始-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a3fd6-149">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a3fd6-150">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a3fd6-150">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a3fd6-151">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="a3fd6-151">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="a3fd6-152">移除-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a3fd6-152">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a3fd6-153">新-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a3fd6-153">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a3fd6-154">AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="a3fd6-154">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="a3fd6-155">AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="a3fd6-155">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="a3fd6-156">AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="a3fd6-156">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="a3fd6-157">AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="a3fd6-157">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="a3fd6-158">AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="a3fd6-158">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="a3fd6-159">AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a3fd6-159">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
