---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: d6d11590699b52bb7245222ddaa01fbc42938d22
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398575"
---
# <span data-ttu-id="fa10c-101">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fa10c-101">Remove-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="fa10c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fa10c-102">SYNOPSIS</span></span>
<span data-ttu-id="fa10c-103">移除封包捕獲資源。</span><span class="sxs-lookup"><span data-stu-id="fa10c-103">Removes a packet capture resource.</span></span>

## <span data-ttu-id="fa10c-104">語法</span><span class="sxs-lookup"><span data-stu-id="fa10c-104">SYNTAX</span></span>

### <span data-ttu-id="fa10c-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="fa10c-105">SetByResource (Default)</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa10c-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="fa10c-106">SetByName</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa10c-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="fa10c-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa10c-108">描述</span><span class="sxs-lookup"><span data-stu-id="fa10c-108">DESCRIPTION</span></span>
<span data-ttu-id="fa10c-109">此Remove-AzNetworkWatcherPacketCapture移除封包捕獲資源。</span><span class="sxs-lookup"><span data-stu-id="fa10c-109">The Remove-AzNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="fa10c-110">建議您在呼叫 Remove-AzNetworkWatcherPacketCapture Stop-AzNetworkWatcherPacketCapture之前先撥打至您的電話。</span><span class="sxs-lookup"><span data-stu-id="fa10c-110">It is recommended to call Stop-AzNetworkWatcherPacketCapture before calling Remove-AzNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="fa10c-111">如果封包捕獲會話在封包Remove-AzNetworkWatcherPacketCapture稱為封包捕獲時，可能不會儲存。</span><span class="sxs-lookup"><span data-stu-id="fa10c-111">If the packet capture session is running when Remove-AzNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="fa10c-112">如果會話在移除包含捕獲資料的 .cap 檔案之前已經停止，則不會移除。</span><span class="sxs-lookup"><span data-stu-id="fa10c-112">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="fa10c-113">例子</span><span class="sxs-lookup"><span data-stu-id="fa10c-113">EXAMPLES</span></span>

### <span data-ttu-id="fa10c-114">範例 1：移除封包捕獲會話</span><span class="sxs-lookup"><span data-stu-id="fa10c-114">Example 1: Remove a packet capture session</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="fa10c-115">在此範例中，我們會移除名為「PacketCaptureTest」的現有封包捕獲會話。</span><span class="sxs-lookup"><span data-stu-id="fa10c-115">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="fa10c-116">參數</span><span class="sxs-lookup"><span data-stu-id="fa10c-116">PARAMETERS</span></span>

### <span data-ttu-id="fa10c-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fa10c-117">-AsJob</span></span>
<span data-ttu-id="fa10c-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="fa10c-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fa10c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa10c-119">-DefaultProfile</span></span>
<span data-ttu-id="fa10c-120">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="fa10c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa10c-121">-位置</span><span class="sxs-lookup"><span data-stu-id="fa10c-121">-Location</span></span>
<span data-ttu-id="fa10c-122">網路監視者的位置。</span><span class="sxs-lookup"><span data-stu-id="fa10c-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="fa10c-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fa10c-123">-NetworkWatcher</span></span>
<span data-ttu-id="fa10c-124">網路監視程式資源。</span><span class="sxs-lookup"><span data-stu-id="fa10c-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="fa10c-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="fa10c-125">-NetworkWatcherName</span></span>
<span data-ttu-id="fa10c-126">網路監視者的名稱。</span><span class="sxs-lookup"><span data-stu-id="fa10c-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="fa10c-127">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="fa10c-127">-PacketCaptureName</span></span>
<span data-ttu-id="fa10c-128">封包捕獲名稱。</span><span class="sxs-lookup"><span data-stu-id="fa10c-128">The packet capture name.</span></span>

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

### <span data-ttu-id="fa10c-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa10c-129">-PassThru</span></span>
<span data-ttu-id="fa10c-130">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="fa10c-130">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="fa10c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa10c-131">-ResourceGroupName</span></span>
<span data-ttu-id="fa10c-132">網路監視者資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fa10c-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="fa10c-133">-確認</span><span class="sxs-lookup"><span data-stu-id="fa10c-133">-Confirm</span></span>
<span data-ttu-id="fa10c-134">執行 Cmdlet 之前，系統會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="fa10c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa10c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa10c-135">-WhatIf</span></span>
<span data-ttu-id="fa10c-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fa10c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa10c-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fa10c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa10c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa10c-138">CommonParameters</span></span>
<span data-ttu-id="fa10c-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fa10c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa10c-140">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="fa10c-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa10c-141">輸入</span><span class="sxs-lookup"><span data-stu-id="fa10c-141">INPUTS</span></span>

### <span data-ttu-id="fa10c-142">Microsoft.Azure.Commands.Network.models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fa10c-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="fa10c-143">System.String</span><span class="sxs-lookup"><span data-stu-id="fa10c-143">System.String</span></span>

## <span data-ttu-id="fa10c-144">輸出</span><span class="sxs-lookup"><span data-stu-id="fa10c-144">OUTPUTS</span></span>

### <span data-ttu-id="fa10c-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fa10c-145">System.Boolean</span></span>

## <span data-ttu-id="fa10c-146">筆記</span><span class="sxs-lookup"><span data-stu-id="fa10c-146">NOTES</span></span>
<span data-ttu-id="fa10c-147">關鍵字：azure、azurerm、arm、資源、管理、管理員、網路、網路、網路監視程式、封包、捕獲、流量、移除</span><span class="sxs-lookup"><span data-stu-id="fa10c-147">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="fa10c-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="fa10c-148">RELATED LINKS</span></span>

[<span data-ttu-id="fa10c-149">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fa10c-149">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="fa10c-150">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fa10c-150">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="fa10c-151">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fa10c-151">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="fa10c-152">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="fa10c-152">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="fa10c-153">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="fa10c-153">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="fa10c-154">Get-AzNetworkWatcherTopwork</span><span class="sxs-lookup"><span data-stu-id="fa10c-154">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="fa10c-155">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="fa10c-155">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="fa10c-156">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fa10c-156">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fa10c-157">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="fa10c-157">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="fa10c-158">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fa10c-158">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fa10c-159">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fa10c-159">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fa10c-160">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fa10c-160">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fa10c-161">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="fa10c-161">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="fa10c-162">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="fa10c-162">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="fa10c-163">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="fa10c-163">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="fa10c-164">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fa10c-164">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="fa10c-165">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fa10c-165">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="fa10c-166">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fa10c-166">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="fa10c-167">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="fa10c-167">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="fa10c-168">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fa10c-168">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="fa10c-169">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fa10c-169">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="fa10c-170">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="fa10c-170">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="fa10c-171">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="fa10c-171">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="fa10c-172">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="fa10c-172">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="fa10c-173">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="fa10c-173">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="fa10c-174">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="fa10c-174">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="fa10c-175">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fa10c-175">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
