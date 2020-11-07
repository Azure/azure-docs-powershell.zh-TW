---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcher.md
ms.openlocfilehash: f098e0d776ab115211fb562ed4889502995ffdd7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626374"
---
# <span data-ttu-id="2dffe-101">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2dffe-101">New-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="2dffe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2dffe-102">SYNOPSIS</span></span>
<span data-ttu-id="2dffe-103">建立新的網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="2dffe-103">Creates a new Network Watcher resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2dffe-104">句法</span><span class="sxs-lookup"><span data-stu-id="2dffe-104">SYNTAX</span></span>

```
New-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2dffe-105">說明</span><span class="sxs-lookup"><span data-stu-id="2dffe-105">DESCRIPTION</span></span>
<span data-ttu-id="2dffe-106">New-AzureRmNetworkWatcher Cmdlet 會建立新的網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="2dffe-106">The New-AzureRmNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="2dffe-107">示例</span><span class="sxs-lookup"><span data-stu-id="2dffe-107">EXAMPLES</span></span>

### <span data-ttu-id="2dffe-108">範例1：建立網路觀察程式</span><span class="sxs-lookup"><span data-stu-id="2dffe-108">Example 1: Create a Network Watcher</span></span>
```
New-AzureRmResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"7cf1f2fe-8445-4aa7-9bf5-c15347282c39"
Location          : westcentralus
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="2dffe-109">這個範例會在新建立的資源群組內建立新的網路觀察程式。</span><span class="sxs-lookup"><span data-stu-id="2dffe-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="2dffe-110">請注意，每個訂閱只能建立一個網路觀察程式。</span><span class="sxs-lookup"><span data-stu-id="2dffe-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="2dffe-111">參數</span><span class="sxs-lookup"><span data-stu-id="2dffe-111">PARAMETERS</span></span>

### <span data-ttu-id="2dffe-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dffe-112">-DefaultProfile</span></span>
<span data-ttu-id="2dffe-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2dffe-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2dffe-114">-位置</span><span class="sxs-lookup"><span data-stu-id="2dffe-114">-Location</span></span>
<span data-ttu-id="2dffe-115">位於.</span><span class="sxs-lookup"><span data-stu-id="2dffe-115">Location.</span></span>

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

### <span data-ttu-id="2dffe-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="2dffe-116">-Name</span></span>
<span data-ttu-id="2dffe-117">網路觀察程式名稱。</span><span class="sxs-lookup"><span data-stu-id="2dffe-117">The network watcher name.</span></span>

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

### <span data-ttu-id="2dffe-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dffe-118">-ResourceGroupName</span></span>
<span data-ttu-id="2dffe-119">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2dffe-119">The resource group name.</span></span>

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

### <span data-ttu-id="2dffe-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="2dffe-120">-Tag</span></span>
<span data-ttu-id="2dffe-121">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="2dffe-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2dffe-122">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="2dffe-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2dffe-123">-確認</span><span class="sxs-lookup"><span data-stu-id="2dffe-123">-Confirm</span></span>
<span data-ttu-id="2dffe-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2dffe-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2dffe-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dffe-125">-WhatIf</span></span>
<span data-ttu-id="2dffe-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2dffe-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2dffe-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2dffe-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2dffe-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dffe-128">CommonParameters</span></span>
<span data-ttu-id="2dffe-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2dffe-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dffe-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2dffe-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dffe-131">輸入</span><span class="sxs-lookup"><span data-stu-id="2dffe-131">INPUTS</span></span>

### <span data-ttu-id="2dffe-132">System.object</span><span class="sxs-lookup"><span data-stu-id="2dffe-132">System.String</span></span>

### <span data-ttu-id="2dffe-133">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2dffe-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2dffe-134">輸出</span><span class="sxs-lookup"><span data-stu-id="2dffe-134">OUTPUTS</span></span>

### <span data-ttu-id="2dffe-135">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2dffe-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="2dffe-136">筆記</span><span class="sxs-lookup"><span data-stu-id="2dffe-136">NOTES</span></span>
<span data-ttu-id="2dffe-137">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式</span><span class="sxs-lookup"><span data-stu-id="2dffe-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="2dffe-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="2dffe-138">RELATED LINKS</span></span>

[<span data-ttu-id="2dffe-139">新-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2dffe-139">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="2dffe-140">AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2dffe-140">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="2dffe-141">移除-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2dffe-141">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="2dffe-142">AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="2dffe-142">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="2dffe-143">AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="2dffe-143">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="2dffe-144">AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="2dffe-144">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="2dffe-145">開始-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="2dffe-145">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="2dffe-146">新-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2dffe-146">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2dffe-147">新-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="2dffe-147">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="2dffe-148">AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2dffe-148">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2dffe-149">移除-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2dffe-149">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2dffe-150">停止 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2dffe-150">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2dffe-151">新-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="2dffe-151">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="2dffe-152">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="2dffe-152">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="2dffe-153">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="2dffe-153">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="2dffe-154">停止 AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2dffe-154">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2dffe-155">開始-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2dffe-155">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2dffe-156">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2dffe-156">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2dffe-157">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="2dffe-157">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="2dffe-158">移除-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2dffe-158">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2dffe-159">新-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2dffe-159">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2dffe-160">AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="2dffe-160">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="2dffe-161">AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="2dffe-161">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="2dffe-162">AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="2dffe-162">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="2dffe-163">AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="2dffe-163">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="2dffe-164">AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="2dffe-164">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="2dffe-165">AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2dffe-165">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
