---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 922026b14531cc1c65f60901914383b402d06889
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94288171"
---
# <span data-ttu-id="796e8-101">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="796e8-101">Stop-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="796e8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="796e8-102">SYNOPSIS</span></span>
<span data-ttu-id="796e8-103">停止執行中的 [資料包捕獲] 會話</span><span class="sxs-lookup"><span data-stu-id="796e8-103">Stops a running packet capture session</span></span>

## <span data-ttu-id="796e8-104">句法</span><span class="sxs-lookup"><span data-stu-id="796e8-104">SYNTAX</span></span>

### <span data-ttu-id="796e8-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="796e8-105">SetByResource (Default)</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="796e8-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="796e8-106">SetByName</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="796e8-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="796e8-107">SetByLocation</span></span>
```
Stop-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="796e8-108">說明</span><span class="sxs-lookup"><span data-stu-id="796e8-108">DESCRIPTION</span></span>
<span data-ttu-id="796e8-109">Stop-AzNetworkWatcherPacketCapture 會停止執行中的 [資料包捕獲] 會話。</span><span class="sxs-lookup"><span data-stu-id="796e8-109">The Stop-AzNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="796e8-110">會話停止之後，就會根據其設定，將資料包捕獲檔案上傳到儲存空間和/或儲存在 VM 的本機。</span><span class="sxs-lookup"><span data-stu-id="796e8-110">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="796e8-111">示例</span><span class="sxs-lookup"><span data-stu-id="796e8-111">EXAMPLES</span></span>

### <span data-ttu-id="796e8-112">範例1：停止資料包捕獲會話</span><span class="sxs-lookup"><span data-stu-id="796e8-112">Example 1: Stop a packet capture session</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="796e8-113">在這個範例中，我們會停止一個名為「PacketCaptureTest」的 [資料包捕獲] 會話。</span><span class="sxs-lookup"><span data-stu-id="796e8-113">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="796e8-114">會話停止之後，就會根據其設定，將資料包捕獲檔案上傳到儲存空間和/或儲存在 VM 的本機。</span><span class="sxs-lookup"><span data-stu-id="796e8-114">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="796e8-115">參數</span><span class="sxs-lookup"><span data-stu-id="796e8-115">PARAMETERS</span></span>

### <span data-ttu-id="796e8-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="796e8-116">-AsJob</span></span>
<span data-ttu-id="796e8-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="796e8-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="796e8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="796e8-118">-DefaultProfile</span></span>
<span data-ttu-id="796e8-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="796e8-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="796e8-120">-位置</span><span class="sxs-lookup"><span data-stu-id="796e8-120">-Location</span></span>
<span data-ttu-id="796e8-121">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="796e8-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="796e8-122">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="796e8-122">-NetworkWatcher</span></span>
<span data-ttu-id="796e8-123">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="796e8-123">The network watcher resource.</span></span>

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

### <span data-ttu-id="796e8-124">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="796e8-124">-NetworkWatcherName</span></span>
<span data-ttu-id="796e8-125">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="796e8-125">The name of network watcher.</span></span>

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

### <span data-ttu-id="796e8-126">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="796e8-126">-PacketCaptureName</span></span>
<span data-ttu-id="796e8-127">[資料包捕獲名稱]。</span><span class="sxs-lookup"><span data-stu-id="796e8-127">The packet capture name.</span></span>

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

### <span data-ttu-id="796e8-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="796e8-128">-PassThru</span></span>
<span data-ttu-id="796e8-129">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="796e8-129">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="796e8-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="796e8-130">-ResourceGroupName</span></span>
<span data-ttu-id="796e8-131">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="796e8-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="796e8-132">-確認</span><span class="sxs-lookup"><span data-stu-id="796e8-132">-Confirm</span></span>
<span data-ttu-id="796e8-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="796e8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="796e8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="796e8-134">-WhatIf</span></span>
<span data-ttu-id="796e8-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="796e8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="796e8-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="796e8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="796e8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="796e8-137">CommonParameters</span></span>
<span data-ttu-id="796e8-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="796e8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="796e8-139">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="796e8-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="796e8-140">輸入</span><span class="sxs-lookup"><span data-stu-id="796e8-140">INPUTS</span></span>

### <span data-ttu-id="796e8-141">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="796e8-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="796e8-142">System.object</span><span class="sxs-lookup"><span data-stu-id="796e8-142">System.String</span></span>

## <span data-ttu-id="796e8-143">輸出</span><span class="sxs-lookup"><span data-stu-id="796e8-143">OUTPUTS</span></span>

### <span data-ttu-id="796e8-144">System.object</span><span class="sxs-lookup"><span data-stu-id="796e8-144">System.Boolean</span></span>

## <span data-ttu-id="796e8-145">筆記</span><span class="sxs-lookup"><span data-stu-id="796e8-145">NOTES</span></span>
<span data-ttu-id="796e8-146">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，資料包，捕獲，流量</span><span class="sxs-lookup"><span data-stu-id="796e8-146">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="796e8-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="796e8-147">RELATED LINKS</span></span>

[<span data-ttu-id="796e8-148">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="796e8-148">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="796e8-149">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="796e8-149">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="796e8-150">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="796e8-150">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="796e8-151">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="796e8-151">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="796e8-152">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="796e8-152">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="796e8-153">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="796e8-153">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="796e8-154">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="796e8-154">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="796e8-155">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="796e8-155">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="796e8-156">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="796e8-156">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="796e8-157">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="796e8-157">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="796e8-158">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="796e8-158">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="796e8-159">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="796e8-159">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="796e8-160">AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="796e8-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="796e8-161">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="796e8-161">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="796e8-162">新-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="796e8-162">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="796e8-163">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="796e8-163">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="796e8-164">停止 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="796e8-164">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="796e8-165">開始-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="796e8-165">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="796e8-166">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="796e8-166">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="796e8-167">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="796e8-167">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="796e8-168">移除-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="796e8-168">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="796e8-169">新-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="796e8-169">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="796e8-170">AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="796e8-170">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="796e8-171">AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="796e8-171">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="796e8-172">AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="796e8-172">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="796e8-173">AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="796e8-173">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="796e8-174">AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="796e8-174">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
