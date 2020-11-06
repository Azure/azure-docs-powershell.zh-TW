---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/stop-azurermnetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: fc78481ceeec796fe4a498bf76092955adb1639a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450215"
---
# <span data-ttu-id="432ca-101">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="432ca-101">Stop-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="432ca-102">摘要</span><span class="sxs-lookup"><span data-stu-id="432ca-102">SYNOPSIS</span></span>
<span data-ttu-id="432ca-103">停止執行中的 [資料包捕獲] 會話</span><span class="sxs-lookup"><span data-stu-id="432ca-103">Stops a running packet capture session</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="432ca-104">句法</span><span class="sxs-lookup"><span data-stu-id="432ca-104">SYNTAX</span></span>

### <span data-ttu-id="432ca-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="432ca-105">SetByResource (Default)</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="432ca-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="432ca-106">SetByName</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="432ca-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="432ca-107">SetByLocation</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="432ca-108">說明</span><span class="sxs-lookup"><span data-stu-id="432ca-108">DESCRIPTION</span></span>
<span data-ttu-id="432ca-109">Stop-AzureRmNetworkWatcherPacketCapture 會停止執行中的 [資料包捕獲] 會話。</span><span class="sxs-lookup"><span data-stu-id="432ca-109">The Stop-AzureRmNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="432ca-110">會話停止之後，就會根據其設定，將資料包捕獲檔案上傳到儲存空間和/或儲存在 VM 的本機。</span><span class="sxs-lookup"><span data-stu-id="432ca-110">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="432ca-111">示例</span><span class="sxs-lookup"><span data-stu-id="432ca-111">EXAMPLES</span></span>

### <span data-ttu-id="432ca-112">範例1：停止資料包捕獲會話</span><span class="sxs-lookup"><span data-stu-id="432ca-112">Example 1: Stop a packet capture session</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="432ca-113">在這個範例中，我們會停止一個名為「PacketCaptureTest」的 [資料包捕獲] 會話。</span><span class="sxs-lookup"><span data-stu-id="432ca-113">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="432ca-114">會話停止之後，就會根據其設定，將資料包捕獲檔案上傳到儲存空間和/或儲存在 VM 的本機。</span><span class="sxs-lookup"><span data-stu-id="432ca-114">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="432ca-115">參數</span><span class="sxs-lookup"><span data-stu-id="432ca-115">PARAMETERS</span></span>

### <span data-ttu-id="432ca-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="432ca-116">-AsJob</span></span>
<span data-ttu-id="432ca-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="432ca-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="432ca-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="432ca-118">-DefaultProfile</span></span>
<span data-ttu-id="432ca-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="432ca-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="432ca-120">-位置</span><span class="sxs-lookup"><span data-stu-id="432ca-120">-Location</span></span>
<span data-ttu-id="432ca-121">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="432ca-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="432ca-122">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="432ca-122">-NetworkWatcher</span></span>
<span data-ttu-id="432ca-123">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="432ca-123">The network watcher resource.</span></span>

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

### <span data-ttu-id="432ca-124">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="432ca-124">-NetworkWatcherName</span></span>
<span data-ttu-id="432ca-125">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="432ca-125">The name of network watcher.</span></span>

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

### <span data-ttu-id="432ca-126">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="432ca-126">-PacketCaptureName</span></span>
<span data-ttu-id="432ca-127">[資料包捕獲名稱]。</span><span class="sxs-lookup"><span data-stu-id="432ca-127">The packet capture name.</span></span>

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

### <span data-ttu-id="432ca-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="432ca-128">-PassThru</span></span>
<span data-ttu-id="432ca-129">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="432ca-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="432ca-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="432ca-130">-ResourceGroupName</span></span>
<span data-ttu-id="432ca-131">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="432ca-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="432ca-132">-確認</span><span class="sxs-lookup"><span data-stu-id="432ca-132">-Confirm</span></span>
<span data-ttu-id="432ca-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="432ca-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="432ca-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="432ca-134">-WhatIf</span></span>
<span data-ttu-id="432ca-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="432ca-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="432ca-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="432ca-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="432ca-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="432ca-137">CommonParameters</span></span>
<span data-ttu-id="432ca-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="432ca-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="432ca-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="432ca-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="432ca-140">輸入</span><span class="sxs-lookup"><span data-stu-id="432ca-140">INPUTS</span></span>

### <span data-ttu-id="432ca-141">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="432ca-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="432ca-142">參數： NetworkWatcher (ByValue) </span><span class="sxs-lookup"><span data-stu-id="432ca-142">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="432ca-143">System.object</span><span class="sxs-lookup"><span data-stu-id="432ca-143">System.String</span></span>
<span data-ttu-id="432ca-144">參數： NetworkWatcherName (ByValue) </span><span class="sxs-lookup"><span data-stu-id="432ca-144">Parameters: NetworkWatcherName (ByValue)</span></span>

## <span data-ttu-id="432ca-145">輸出</span><span class="sxs-lookup"><span data-stu-id="432ca-145">OUTPUTS</span></span>

### <span data-ttu-id="432ca-146">System.object</span><span class="sxs-lookup"><span data-stu-id="432ca-146">System.Boolean</span></span>

## <span data-ttu-id="432ca-147">筆記</span><span class="sxs-lookup"><span data-stu-id="432ca-147">NOTES</span></span>
<span data-ttu-id="432ca-148">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，資料包，捕獲，流量</span><span class="sxs-lookup"><span data-stu-id="432ca-148">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="432ca-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="432ca-149">RELATED LINKS</span></span>

[<span data-ttu-id="432ca-150">新-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="432ca-150">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="432ca-151">新-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="432ca-151">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="432ca-152">AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="432ca-152">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="432ca-153">移除-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="432ca-153">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="432ca-154">新-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="432ca-154">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="432ca-155">AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="432ca-155">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="432ca-156">移除-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="432ca-156">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="432ca-157">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="432ca-157">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="432ca-158">AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="432ca-158">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="432ca-159">AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="432ca-159">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="432ca-160">AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="432ca-160">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="432ca-161">開始-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="432ca-161">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="432ca-162">AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="432ca-162">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="432ca-163">停止 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="432ca-163">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="432ca-164">新-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="432ca-164">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="432ca-165">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="432ca-165">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="432ca-166">停止 AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="432ca-166">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="432ca-167">開始-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="432ca-167">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="432ca-168">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="432ca-168">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="432ca-169">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="432ca-169">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="432ca-170">移除-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="432ca-170">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="432ca-171">新-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="432ca-171">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="432ca-172">AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="432ca-172">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="432ca-173">AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="432ca-173">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="432ca-174">AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="432ca-174">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="432ca-175">AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="432ca-175">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="432ca-176">AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="432ca-176">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
