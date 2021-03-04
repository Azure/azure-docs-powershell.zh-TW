---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 292f1fa9c43def4649519b3285203056ef63c9b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913385"
---
# <span data-ttu-id="02741-101">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="02741-101">Remove-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="02741-102">簡介</span><span class="sxs-lookup"><span data-stu-id="02741-102">SYNOPSIS</span></span>
<span data-ttu-id="02741-103">移除封包捕獲資源。</span><span class="sxs-lookup"><span data-stu-id="02741-103">Removes a packet capture resource.</span></span>

## <span data-ttu-id="02741-104">語法</span><span class="sxs-lookup"><span data-stu-id="02741-104">SYNTAX</span></span>

### <span data-ttu-id="02741-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="02741-105">SetByResource (Default)</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02741-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="02741-106">SetByName</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02741-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="02741-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02741-108">描述</span><span class="sxs-lookup"><span data-stu-id="02741-108">DESCRIPTION</span></span>
<span data-ttu-id="02741-109">此Remove-AzNetworkWatcherPacketCapture移除封包捕獲資源。</span><span class="sxs-lookup"><span data-stu-id="02741-109">The Remove-AzNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="02741-110">建議您在呼叫 Remove-AzNetworkWatcherPacketCapture Stop-AzNetworkWatcherPacketCapture之前先撥打至您的電話。</span><span class="sxs-lookup"><span data-stu-id="02741-110">It is recommended to call Stop-AzNetworkWatcherPacketCapture before calling Remove-AzNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="02741-111">如果封包捕獲會話在封包Remove-AzNetworkWatcherPacketCapture稱為封包捕獲時，可能不會儲存。</span><span class="sxs-lookup"><span data-stu-id="02741-111">If the packet capture session is running when Remove-AzNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="02741-112">如果會話在移除包含捕獲資料的 .cap 檔案之前已經停止，系統不會移除。</span><span class="sxs-lookup"><span data-stu-id="02741-112">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="02741-113">例子</span><span class="sxs-lookup"><span data-stu-id="02741-113">EXAMPLES</span></span>

### <span data-ttu-id="02741-114">範例 1：移除封包捕獲會話</span><span class="sxs-lookup"><span data-stu-id="02741-114">Example 1: Remove a packet capture session</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="02741-115">在此範例中，我們會移除名為「PacketCaptureTest」的現有封包捕獲會話。</span><span class="sxs-lookup"><span data-stu-id="02741-115">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="02741-116">參數</span><span class="sxs-lookup"><span data-stu-id="02741-116">PARAMETERS</span></span>

### <span data-ttu-id="02741-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="02741-117">-AsJob</span></span>
<span data-ttu-id="02741-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="02741-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="02741-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02741-119">-DefaultProfile</span></span>
<span data-ttu-id="02741-120">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="02741-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02741-121">-位置</span><span class="sxs-lookup"><span data-stu-id="02741-121">-Location</span></span>
<span data-ttu-id="02741-122">網路監視者的位置。</span><span class="sxs-lookup"><span data-stu-id="02741-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="02741-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="02741-123">-NetworkWatcher</span></span>
<span data-ttu-id="02741-124">網路監視程式資源。</span><span class="sxs-lookup"><span data-stu-id="02741-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="02741-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="02741-125">-NetworkWatcherName</span></span>
<span data-ttu-id="02741-126">網路監視者的名稱。</span><span class="sxs-lookup"><span data-stu-id="02741-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="02741-127">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="02741-127">-PacketCaptureName</span></span>
<span data-ttu-id="02741-128">封包捕獲名稱。</span><span class="sxs-lookup"><span data-stu-id="02741-128">The packet capture name.</span></span>

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

### <span data-ttu-id="02741-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02741-129">-PassThru</span></span>
<span data-ttu-id="02741-130">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="02741-130">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="02741-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02741-131">-ResourceGroupName</span></span>
<span data-ttu-id="02741-132">網路監視者資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="02741-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="02741-133">-確認</span><span class="sxs-lookup"><span data-stu-id="02741-133">-Confirm</span></span>
<span data-ttu-id="02741-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="02741-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02741-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02741-135">-WhatIf</span></span>
<span data-ttu-id="02741-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="02741-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02741-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="02741-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02741-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02741-138">CommonParameters</span></span>
<span data-ttu-id="02741-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="02741-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02741-140">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="02741-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02741-141">輸入</span><span class="sxs-lookup"><span data-stu-id="02741-141">INPUTS</span></span>

### <span data-ttu-id="02741-142">Microsoft.Azure.Commands.Network.models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="02741-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="02741-143">System.String</span><span class="sxs-lookup"><span data-stu-id="02741-143">System.String</span></span>

## <span data-ttu-id="02741-144">輸出</span><span class="sxs-lookup"><span data-stu-id="02741-144">OUTPUTS</span></span>

### <span data-ttu-id="02741-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="02741-145">System.Boolean</span></span>

## <span data-ttu-id="02741-146">筆記</span><span class="sxs-lookup"><span data-stu-id="02741-146">NOTES</span></span>
<span data-ttu-id="02741-147">關鍵字：azure、azurerm、arm、資源、管理、管理員、網路、網路、網路監視程式、封包、捕獲、流量、移除</span><span class="sxs-lookup"><span data-stu-id="02741-147">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="02741-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="02741-148">RELATED LINKS</span></span>

[<span data-ttu-id="02741-149">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="02741-149">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="02741-150">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="02741-150">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="02741-151">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="02741-151">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="02741-152">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="02741-152">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="02741-153">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="02741-153">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="02741-154">Get-AzNetworkWatcherTopwork</span><span class="sxs-lookup"><span data-stu-id="02741-154">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="02741-155">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="02741-155">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="02741-156">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="02741-156">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="02741-157">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="02741-157">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="02741-158">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="02741-158">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="02741-159">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="02741-159">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="02741-160">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="02741-160">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="02741-161">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="02741-161">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="02741-162">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="02741-162">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="02741-163">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="02741-163">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="02741-164">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="02741-164">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="02741-165">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="02741-165">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="02741-166">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="02741-166">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="02741-167">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="02741-167">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="02741-168">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="02741-168">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="02741-169">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="02741-169">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="02741-170">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="02741-170">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="02741-171">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="02741-171">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="02741-172">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="02741-172">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="02741-173">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="02741-173">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="02741-174">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="02741-174">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="02741-175">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="02741-175">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
