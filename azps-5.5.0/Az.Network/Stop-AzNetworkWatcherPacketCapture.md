---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 42067c978c7791740d10af4df88c51dde3096c0e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100408996"
---
# <span data-ttu-id="82555-101">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="82555-101">Stop-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="82555-102">簡介</span><span class="sxs-lookup"><span data-stu-id="82555-102">SYNOPSIS</span></span>
<span data-ttu-id="82555-103">停止進行中的封包捕獲會話</span><span class="sxs-lookup"><span data-stu-id="82555-103">Stops a running packet capture session</span></span>

## <span data-ttu-id="82555-104">語法</span><span class="sxs-lookup"><span data-stu-id="82555-104">SYNTAX</span></span>

### <span data-ttu-id="82555-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="82555-105">SetByResource (Default)</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82555-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="82555-106">SetByName</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82555-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="82555-107">SetByLocation</span></span>
```
Stop-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82555-108">描述</span><span class="sxs-lookup"><span data-stu-id="82555-108">DESCRIPTION</span></span>
<span data-ttu-id="82555-109">此Stop-AzNetworkWatcherPacketCapture會停止進行中的封包捕獲會話。</span><span class="sxs-lookup"><span data-stu-id="82555-109">The Stop-AzNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="82555-110">會話停止之後，封包捕獲檔案會上傳至儲存空間和/或儲存于 VM 上，視其組配置而不同。</span><span class="sxs-lookup"><span data-stu-id="82555-110">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="82555-111">例子</span><span class="sxs-lookup"><span data-stu-id="82555-111">EXAMPLES</span></span>

### <span data-ttu-id="82555-112">範例 1：停止封包捕獲會話</span><span class="sxs-lookup"><span data-stu-id="82555-112">Example 1: Stop a packet capture session</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="82555-113">在此範例中，我們停止名為「PacketCaptureTest」的執行時間封包捕獲會話。</span><span class="sxs-lookup"><span data-stu-id="82555-113">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="82555-114">會話停止之後，封包捕獲檔案會上傳至儲存空間和/或儲存于 VM 上，視其組配置而不同。</span><span class="sxs-lookup"><span data-stu-id="82555-114">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="82555-115">參數</span><span class="sxs-lookup"><span data-stu-id="82555-115">PARAMETERS</span></span>

### <span data-ttu-id="82555-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="82555-116">-AsJob</span></span>
<span data-ttu-id="82555-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="82555-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="82555-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82555-118">-DefaultProfile</span></span>
<span data-ttu-id="82555-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="82555-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82555-120">-位置</span><span class="sxs-lookup"><span data-stu-id="82555-120">-Location</span></span>
<span data-ttu-id="82555-121">網路監視者的位置。</span><span class="sxs-lookup"><span data-stu-id="82555-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="82555-122">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="82555-122">-NetworkWatcher</span></span>
<span data-ttu-id="82555-123">網路監視程式資源。</span><span class="sxs-lookup"><span data-stu-id="82555-123">The network watcher resource.</span></span>

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

### <span data-ttu-id="82555-124">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="82555-124">-NetworkWatcherName</span></span>
<span data-ttu-id="82555-125">網路監視者的名稱。</span><span class="sxs-lookup"><span data-stu-id="82555-125">The name of network watcher.</span></span>

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

### <span data-ttu-id="82555-126">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="82555-126">-PacketCaptureName</span></span>
<span data-ttu-id="82555-127">封包捕獲名稱。</span><span class="sxs-lookup"><span data-stu-id="82555-127">The packet capture name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82555-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="82555-128">-PassThru</span></span>
<span data-ttu-id="82555-129">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="82555-129">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="82555-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82555-130">-ResourceGroupName</span></span>
<span data-ttu-id="82555-131">網路監視者資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="82555-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="82555-132">-確認</span><span class="sxs-lookup"><span data-stu-id="82555-132">-Confirm</span></span>
<span data-ttu-id="82555-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="82555-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82555-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82555-134">-WhatIf</span></span>
<span data-ttu-id="82555-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="82555-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82555-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="82555-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82555-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82555-137">CommonParameters</span></span>
<span data-ttu-id="82555-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="82555-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82555-139">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="82555-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82555-140">輸入</span><span class="sxs-lookup"><span data-stu-id="82555-140">INPUTS</span></span>

### <span data-ttu-id="82555-141">Microsoft.Azure.Commands.Network.models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="82555-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="82555-142">System.String</span><span class="sxs-lookup"><span data-stu-id="82555-142">System.String</span></span>

## <span data-ttu-id="82555-143">輸出</span><span class="sxs-lookup"><span data-stu-id="82555-143">OUTPUTS</span></span>

### <span data-ttu-id="82555-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="82555-144">System.Boolean</span></span>

## <span data-ttu-id="82555-145">筆記</span><span class="sxs-lookup"><span data-stu-id="82555-145">NOTES</span></span>
<span data-ttu-id="82555-146">關鍵字：azure、azurerm、arm、資源、管理、管理員、網路、網路、網路監視者、封包、捕獲、流量</span><span class="sxs-lookup"><span data-stu-id="82555-146">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="82555-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="82555-147">RELATED LINKS</span></span>

[<span data-ttu-id="82555-148">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="82555-148">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="82555-149">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="82555-149">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="82555-150">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="82555-150">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="82555-151">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="82555-151">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="82555-152">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="82555-152">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="82555-153">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="82555-153">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="82555-154">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="82555-154">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="82555-155">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="82555-155">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="82555-156">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="82555-156">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="82555-157">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="82555-157">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="82555-158">Get-AzNetworkWatcherTopwork</span><span class="sxs-lookup"><span data-stu-id="82555-158">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="82555-159">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="82555-159">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="82555-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="82555-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="82555-161">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="82555-161">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="82555-162">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="82555-162">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="82555-163">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="82555-163">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="82555-164">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="82555-164">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="82555-165">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="82555-165">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="82555-166">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="82555-166">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="82555-167">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="82555-167">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="82555-168">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="82555-168">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="82555-169">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="82555-169">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="82555-170">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="82555-170">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="82555-171">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="82555-171">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="82555-172">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="82555-172">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="82555-173">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="82555-173">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="82555-174">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="82555-174">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
