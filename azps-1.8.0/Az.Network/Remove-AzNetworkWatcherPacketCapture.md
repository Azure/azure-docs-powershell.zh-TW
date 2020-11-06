---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: d99b085f5137c9f18d4dda50fce0654954266f37
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621576"
---
# <span data-ttu-id="a6b96-101">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a6b96-101">Remove-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="a6b96-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a6b96-102">SYNOPSIS</span></span>
<span data-ttu-id="a6b96-103">移除 [資料包捕獲資源]。</span><span class="sxs-lookup"><span data-stu-id="a6b96-103">Removes a packet capture resource.</span></span>

## <span data-ttu-id="a6b96-104">句法</span><span class="sxs-lookup"><span data-stu-id="a6b96-104">SYNTAX</span></span>

### <span data-ttu-id="a6b96-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="a6b96-105">SetByResource (Default)</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6b96-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="a6b96-106">SetByName</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6b96-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="a6b96-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6b96-108">說明</span><span class="sxs-lookup"><span data-stu-id="a6b96-108">DESCRIPTION</span></span>
<span data-ttu-id="a6b96-109">Remove-AzNetworkWatcherPacketCapture 會移除 [資料包捕獲資源]。</span><span class="sxs-lookup"><span data-stu-id="a6b96-109">The Remove-AzNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="a6b96-110">建議您先呼叫 Stop-AzNetworkWatcherPacketCapture，然後再呼叫 AzNetworkWatcherPacketCapture。</span><span class="sxs-lookup"><span data-stu-id="a6b96-110">It is recommended to call Stop-AzNetworkWatcherPacketCapture before calling Remove-AzNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="a6b96-111">如果 Remove-AzNetworkWatcherPacketCapture 稱為 [資料包捕獲會話]，則可能無法儲存 [資料包捕獲]。</span><span class="sxs-lookup"><span data-stu-id="a6b96-111">If the packet capture session is running when Remove-AzNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="a6b96-112">如果在移除前停止會話，則不會移除內含捕獲資料的 .cap 檔案。</span><span class="sxs-lookup"><span data-stu-id="a6b96-112">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="a6b96-113">示例</span><span class="sxs-lookup"><span data-stu-id="a6b96-113">EXAMPLES</span></span>

### <span data-ttu-id="a6b96-114">範例1：移除 [資料包捕獲] 會話</span><span class="sxs-lookup"><span data-stu-id="a6b96-114">Example 1: Remove a packet capture session</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="a6b96-115">在這個範例中，我們會移除名為 "PacketCaptureTest" 的現有資料包捕獲會話。</span><span class="sxs-lookup"><span data-stu-id="a6b96-115">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="a6b96-116">參數</span><span class="sxs-lookup"><span data-stu-id="a6b96-116">PARAMETERS</span></span>

### <span data-ttu-id="a6b96-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a6b96-117">-AsJob</span></span>
<span data-ttu-id="a6b96-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a6b96-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a6b96-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6b96-119">-DefaultProfile</span></span>
<span data-ttu-id="a6b96-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a6b96-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6b96-121">-位置</span><span class="sxs-lookup"><span data-stu-id="a6b96-121">-Location</span></span>
<span data-ttu-id="a6b96-122">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="a6b96-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="a6b96-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a6b96-123">-NetworkWatcher</span></span>
<span data-ttu-id="a6b96-124">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="a6b96-124">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6b96-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="a6b96-125">-NetworkWatcherName</span></span>
<span data-ttu-id="a6b96-126">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="a6b96-126">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6b96-127">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="a6b96-127">-PacketCaptureName</span></span>
<span data-ttu-id="a6b96-128">[資料包捕獲名稱]。</span><span class="sxs-lookup"><span data-stu-id="a6b96-128">The packet capture name.</span></span>

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

### <span data-ttu-id="a6b96-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a6b96-129">-PassThru</span></span>
<span data-ttu-id="a6b96-130">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="a6b96-130">Returns an object representing the item with which you are working.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6b96-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6b96-131">-ResourceGroupName</span></span>
<span data-ttu-id="a6b96-132">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a6b96-132">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6b96-133">-確認</span><span class="sxs-lookup"><span data-stu-id="a6b96-133">-Confirm</span></span>
<span data-ttu-id="a6b96-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a6b96-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6b96-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6b96-135">-WhatIf</span></span>
<span data-ttu-id="a6b96-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a6b96-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6b96-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a6b96-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6b96-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6b96-138">CommonParameters</span></span>
<span data-ttu-id="a6b96-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a6b96-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6b96-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a6b96-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6b96-141">輸入</span><span class="sxs-lookup"><span data-stu-id="a6b96-141">INPUTS</span></span>

### <span data-ttu-id="a6b96-142">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a6b96-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="a6b96-143">System.object</span><span class="sxs-lookup"><span data-stu-id="a6b96-143">System.String</span></span>

## <span data-ttu-id="a6b96-144">輸出</span><span class="sxs-lookup"><span data-stu-id="a6b96-144">OUTPUTS</span></span>

### <span data-ttu-id="a6b96-145">System.object</span><span class="sxs-lookup"><span data-stu-id="a6b96-145">System.Boolean</span></span>

## <span data-ttu-id="a6b96-146">筆記</span><span class="sxs-lookup"><span data-stu-id="a6b96-146">NOTES</span></span>
<span data-ttu-id="a6b96-147">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，資料包，捕獲，流量，移除</span><span class="sxs-lookup"><span data-stu-id="a6b96-147">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="a6b96-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="a6b96-148">RELATED LINKS</span></span>

[<span data-ttu-id="a6b96-149">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a6b96-149">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="a6b96-150">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a6b96-150">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="a6b96-151">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a6b96-151">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="a6b96-152">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="a6b96-152">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="a6b96-153">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="a6b96-153">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="a6b96-154">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="a6b96-154">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="a6b96-155">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="a6b96-155">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="a6b96-156">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a6b96-156">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a6b96-157">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="a6b96-157">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="a6b96-158">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a6b96-158">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a6b96-159">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a6b96-159">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a6b96-160">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a6b96-160">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a6b96-161">新-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="a6b96-161">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="a6b96-162">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="a6b96-162">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="a6b96-163">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="a6b96-163">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="a6b96-164">停止 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a6b96-164">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a6b96-165">開始-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a6b96-165">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a6b96-166">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a6b96-166">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a6b96-167">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="a6b96-167">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="a6b96-168">移除-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a6b96-168">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a6b96-169">新-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a6b96-169">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a6b96-170">AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="a6b96-170">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="a6b96-171">AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="a6b96-171">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="a6b96-172">AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="a6b96-172">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="a6b96-173">AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="a6b96-173">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="a6b96-174">AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="a6b96-174">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="a6b96-175">AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a6b96-175">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
