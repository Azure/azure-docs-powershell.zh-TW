---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcher.md
ms.openlocfilehash: c8417f8a1f1d16e00629d06a75be2802801afd2e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626536"
---
# <span data-ttu-id="3e0eb-101">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3e0eb-101">Get-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="3e0eb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3e0eb-102">SYNOPSIS</span></span>
<span data-ttu-id="3e0eb-103">取得網路觀察程式的屬性</span><span class="sxs-lookup"><span data-stu-id="3e0eb-103">Gets the properties of a Network Watcher</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e0eb-104">句法</span><span class="sxs-lookup"><span data-stu-id="3e0eb-104">SYNTAX</span></span>

### <span data-ttu-id="3e0eb-105">獲取</span><span class="sxs-lookup"><span data-stu-id="3e0eb-105">Get</span></span>
```
Get-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3e0eb-106">清單</span><span class="sxs-lookup"><span data-stu-id="3e0eb-106">List</span></span>
```
Get-AzureRmNetworkWatcher [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3e0eb-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="3e0eb-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e0eb-108">說明</span><span class="sxs-lookup"><span data-stu-id="3e0eb-108">DESCRIPTION</span></span>
<span data-ttu-id="3e0eb-109">Get-AzureRmNetworkWatcher Cmdlet 會取得一或多個 Azure 網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="3e0eb-109">The Get-AzureRmNetworkWatcher cmdlet gets one or more Azure Network Watcher resources.</span></span>

## <span data-ttu-id="3e0eb-110">示例</span><span class="sxs-lookup"><span data-stu-id="3e0eb-110">EXAMPLES</span></span>

### <span data-ttu-id="3e0eb-111">範例1：取得網路觀察程式</span><span class="sxs-lookup"><span data-stu-id="3e0eb-111">Example 1: Get a Network Watcher</span></span>
```
Get-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="3e0eb-112">在 [資源群組 NetworkWatcherRG] 中取得名為 NetworkWatcher_westcentralus 的網路觀察程式。</span><span class="sxs-lookup"><span data-stu-id="3e0eb-112">Gets the Network Watcher named NetworkWatcher_westcentralus in the resource group NetworkWatcherRG.</span></span>

## <span data-ttu-id="3e0eb-113">參數</span><span class="sxs-lookup"><span data-stu-id="3e0eb-113">PARAMETERS</span></span>

### <span data-ttu-id="3e0eb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e0eb-114">-DefaultProfile</span></span>
<span data-ttu-id="3e0eb-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3e0eb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e0eb-116">-位置</span><span class="sxs-lookup"><span data-stu-id="3e0eb-116">-Location</span></span>
<span data-ttu-id="3e0eb-117">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="3e0eb-117">Location of the network watcher.</span></span>

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

### <span data-ttu-id="3e0eb-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="3e0eb-118">-Name</span></span>
<span data-ttu-id="3e0eb-119">網路觀察程式名稱。</span><span class="sxs-lookup"><span data-stu-id="3e0eb-119">The network watcher name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e0eb-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e0eb-120">-ResourceGroupName</span></span>
<span data-ttu-id="3e0eb-121">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3e0eb-121">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e0eb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e0eb-122">CommonParameters</span></span>
<span data-ttu-id="3e0eb-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3e0eb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e0eb-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3e0eb-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e0eb-125">輸入</span><span class="sxs-lookup"><span data-stu-id="3e0eb-125">INPUTS</span></span>

### <span data-ttu-id="3e0eb-126">所有</span><span class="sxs-lookup"><span data-stu-id="3e0eb-126">None</span></span>

## <span data-ttu-id="3e0eb-127">輸出</span><span class="sxs-lookup"><span data-stu-id="3e0eb-127">OUTPUTS</span></span>

### <span data-ttu-id="3e0eb-128">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3e0eb-128">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="3e0eb-129">筆記</span><span class="sxs-lookup"><span data-stu-id="3e0eb-129">NOTES</span></span>
<span data-ttu-id="3e0eb-130">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式</span><span class="sxs-lookup"><span data-stu-id="3e0eb-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span> 

## <span data-ttu-id="3e0eb-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="3e0eb-131">RELATED LINKS</span></span>

[<span data-ttu-id="3e0eb-132">新-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3e0eb-132">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="3e0eb-133">AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3e0eb-133">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="3e0eb-134">移除-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3e0eb-134">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="3e0eb-135">AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="3e0eb-135">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="3e0eb-136">AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="3e0eb-136">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="3e0eb-137">AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="3e0eb-137">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="3e0eb-138">開始-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="3e0eb-138">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="3e0eb-139">新-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3e0eb-139">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3e0eb-140">新-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="3e0eb-140">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="3e0eb-141">AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3e0eb-141">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3e0eb-142">移除-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3e0eb-142">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3e0eb-143">停止 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3e0eb-143">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3e0eb-144">新-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="3e0eb-144">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="3e0eb-145">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="3e0eb-145">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="3e0eb-146">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="3e0eb-146">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="3e0eb-147">停止 AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3e0eb-147">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3e0eb-148">開始-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3e0eb-148">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3e0eb-149">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3e0eb-149">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3e0eb-150">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="3e0eb-150">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="3e0eb-151">移除-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3e0eb-151">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3e0eb-152">新-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3e0eb-152">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3e0eb-153">AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="3e0eb-153">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="3e0eb-154">AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="3e0eb-154">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="3e0eb-155">AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="3e0eb-155">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="3e0eb-156">AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="3e0eb-156">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="3e0eb-157">AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="3e0eb-157">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="3e0eb-158">AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3e0eb-158">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
