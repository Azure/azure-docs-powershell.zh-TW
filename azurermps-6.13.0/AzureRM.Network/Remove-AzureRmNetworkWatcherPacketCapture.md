---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 0c0568dc11411e27af1db9d9e3d59c0026b0a39a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455172"
---
# <span data-ttu-id="9045c-101">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9045c-101">Remove-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="9045c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9045c-102">SYNOPSIS</span></span>
<span data-ttu-id="9045c-103">移除 [資料包捕獲資源]。</span><span class="sxs-lookup"><span data-stu-id="9045c-103">Removes a packet capture resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9045c-104">句法</span><span class="sxs-lookup"><span data-stu-id="9045c-104">SYNTAX</span></span>

### <span data-ttu-id="9045c-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="9045c-105">SetByResource (Default)</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9045c-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="9045c-106">SetByName</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9045c-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="9045c-107">SetByLocation</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9045c-108">說明</span><span class="sxs-lookup"><span data-stu-id="9045c-108">DESCRIPTION</span></span>
<span data-ttu-id="9045c-109">Remove-AzureRmNetworkWatcherPacketCapture 會移除 [資料包捕獲資源]。</span><span class="sxs-lookup"><span data-stu-id="9045c-109">The Remove-AzureRmNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="9045c-110">建議您先呼叫 Stop-AzureRmNetworkWatcherPacketCapture，然後再呼叫 AzureRmNetworkWatcherPacketCapture。</span><span class="sxs-lookup"><span data-stu-id="9045c-110">It is recommended to call Stop-AzureRmNetworkWatcherPacketCapture before calling Remove-AzureRmNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="9045c-111">如果 Remove-AzureRmNetworkWatcherPacketCapture 稱為 [資料包捕獲會話]，則可能無法儲存 [資料包捕獲]。</span><span class="sxs-lookup"><span data-stu-id="9045c-111">If the packet capture session is running when Remove-AzureRmNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="9045c-112">如果在移除前停止會話，則不會移除內含捕獲資料的 .cap 檔案。</span><span class="sxs-lookup"><span data-stu-id="9045c-112">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="9045c-113">示例</span><span class="sxs-lookup"><span data-stu-id="9045c-113">EXAMPLES</span></span>

### <span data-ttu-id="9045c-114">範例1：移除 [資料包捕獲] 會話</span><span class="sxs-lookup"><span data-stu-id="9045c-114">Example 1: Remove a packet capture session</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="9045c-115">在這個範例中，我們會移除名為 "PacketCaptureTest" 的現有資料包捕獲會話。</span><span class="sxs-lookup"><span data-stu-id="9045c-115">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="9045c-116">參數</span><span class="sxs-lookup"><span data-stu-id="9045c-116">PARAMETERS</span></span>

### <span data-ttu-id="9045c-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9045c-117">-AsJob</span></span>
<span data-ttu-id="9045c-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9045c-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9045c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9045c-119">-DefaultProfile</span></span>
<span data-ttu-id="9045c-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9045c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9045c-121">-位置</span><span class="sxs-lookup"><span data-stu-id="9045c-121">-Location</span></span>
<span data-ttu-id="9045c-122">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="9045c-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="9045c-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9045c-123">-NetworkWatcher</span></span>
<span data-ttu-id="9045c-124">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="9045c-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="9045c-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="9045c-125">-NetworkWatcherName</span></span>
<span data-ttu-id="9045c-126">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="9045c-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="9045c-127">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="9045c-127">-PacketCaptureName</span></span>
<span data-ttu-id="9045c-128">[資料包捕獲名稱]。</span><span class="sxs-lookup"><span data-stu-id="9045c-128">The packet capture name.</span></span>

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

### <span data-ttu-id="9045c-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9045c-129">-PassThru</span></span>
<span data-ttu-id="9045c-130">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="9045c-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="9045c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9045c-131">-ResourceGroupName</span></span>
<span data-ttu-id="9045c-132">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9045c-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="9045c-133">-確認</span><span class="sxs-lookup"><span data-stu-id="9045c-133">-Confirm</span></span>
<span data-ttu-id="9045c-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9045c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9045c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9045c-135">-WhatIf</span></span>
<span data-ttu-id="9045c-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9045c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9045c-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9045c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9045c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9045c-138">CommonParameters</span></span>
<span data-ttu-id="9045c-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9045c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9045c-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9045c-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9045c-141">輸入</span><span class="sxs-lookup"><span data-stu-id="9045c-141">INPUTS</span></span>

### <span data-ttu-id="9045c-142">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9045c-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="9045c-143">參數： NetworkWatcher (ByValue) </span><span class="sxs-lookup"><span data-stu-id="9045c-143">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="9045c-144">System.object</span><span class="sxs-lookup"><span data-stu-id="9045c-144">System.String</span></span>
<span data-ttu-id="9045c-145">參數： NetworkWatcherName (ByValue) </span><span class="sxs-lookup"><span data-stu-id="9045c-145">Parameters: NetworkWatcherName (ByValue)</span></span>

## <span data-ttu-id="9045c-146">輸出</span><span class="sxs-lookup"><span data-stu-id="9045c-146">OUTPUTS</span></span>

### <span data-ttu-id="9045c-147">System.object</span><span class="sxs-lookup"><span data-stu-id="9045c-147">System.Boolean</span></span>

## <span data-ttu-id="9045c-148">筆記</span><span class="sxs-lookup"><span data-stu-id="9045c-148">NOTES</span></span>
<span data-ttu-id="9045c-149">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，資料包，捕獲，流量，移除</span><span class="sxs-lookup"><span data-stu-id="9045c-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="9045c-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="9045c-150">RELATED LINKS</span></span>

[<span data-ttu-id="9045c-151">新-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9045c-151">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="9045c-152">AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9045c-152">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="9045c-153">移除-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9045c-153">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="9045c-154">AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="9045c-154">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="9045c-155">AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="9045c-155">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="9045c-156">AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="9045c-156">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="9045c-157">開始-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="9045c-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="9045c-158">新-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9045c-158">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9045c-159">新-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="9045c-159">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="9045c-160">AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9045c-160">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9045c-161">移除-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9045c-161">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9045c-162">停止 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9045c-162">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9045c-163">新-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="9045c-163">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="9045c-164">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="9045c-164">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="9045c-165">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="9045c-165">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="9045c-166">停止 AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9045c-166">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9045c-167">開始-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9045c-167">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9045c-168">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9045c-168">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9045c-169">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="9045c-169">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="9045c-170">移除-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9045c-170">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9045c-171">新-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9045c-171">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9045c-172">AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="9045c-172">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="9045c-173">AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="9045c-173">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="9045c-174">AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="9045c-174">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="9045c-175">AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="9045c-175">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="9045c-176">AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="9045c-176">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="9045c-177">AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9045c-177">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
