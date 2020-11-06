---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
ms.openlocfilehash: b06540e1f03058fd36302616d22375270b521b8d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621578"
---
# <span data-ttu-id="f0340-101">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f0340-101">Remove-AzNetworkWatcher</span></span>

## <span data-ttu-id="f0340-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f0340-102">SYNOPSIS</span></span>
<span data-ttu-id="f0340-103">移除網路觀察程式。</span><span class="sxs-lookup"><span data-stu-id="f0340-103">Removes a Network Watcher.</span></span>

## <span data-ttu-id="f0340-104">句法</span><span class="sxs-lookup"><span data-stu-id="f0340-104">SYNTAX</span></span>

### <span data-ttu-id="f0340-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f0340-105">SetByResource</span></span>
```
Remove-AzNetworkWatcher -NetworkWatcher <PSNetworkWatcher> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0340-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="f0340-106">SetByName</span></span>
```
Remove-AzNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0340-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="f0340-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcher -Location <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0340-108">說明</span><span class="sxs-lookup"><span data-stu-id="f0340-108">DESCRIPTION</span></span>
<span data-ttu-id="f0340-109">Remove-AzNetworkWatcher Cmdlet 會移除網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="f0340-109">The Remove-AzNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="f0340-110">示例</span><span class="sxs-lookup"><span data-stu-id="f0340-110">EXAMPLES</span></span>

### <span data-ttu-id="f0340-111">範例1：建立及刪除網路觀察程式</span><span class="sxs-lookup"><span data-stu-id="f0340-111">Example 1: Create and delete a Network Watcher</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="f0340-112">這個範例會在資源群組中建立網路觀察程式，然後立即將它刪除。</span><span class="sxs-lookup"><span data-stu-id="f0340-112">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="f0340-113">請注意，每個訂閱只能建立一個網路觀察程式。</span><span class="sxs-lookup"><span data-stu-id="f0340-113">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="f0340-114">若要在刪除虛擬網路時取消提示，請使用-Force 標誌。</span><span class="sxs-lookup"><span data-stu-id="f0340-114">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="f0340-115">參數</span><span class="sxs-lookup"><span data-stu-id="f0340-115">PARAMETERS</span></span>

### <span data-ttu-id="f0340-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f0340-116">-AsJob</span></span>
<span data-ttu-id="f0340-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f0340-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f0340-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0340-118">-DefaultProfile</span></span>
<span data-ttu-id="f0340-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f0340-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0340-120">-位置</span><span class="sxs-lookup"><span data-stu-id="f0340-120">-Location</span></span>
<span data-ttu-id="f0340-121">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="f0340-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="f0340-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="f0340-122">-Name</span></span>
<span data-ttu-id="f0340-123">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="f0340-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0340-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f0340-124">-NetworkWatcher</span></span>
<span data-ttu-id="f0340-125">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="f0340-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="f0340-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f0340-126">-PassThru</span></span>
<span data-ttu-id="f0340-127">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="f0340-127">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="f0340-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0340-128">-ResourceGroupName</span></span>
<span data-ttu-id="f0340-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f0340-129">The resource group name.</span></span>

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

### <span data-ttu-id="f0340-130">-確認</span><span class="sxs-lookup"><span data-stu-id="f0340-130">-Confirm</span></span>
<span data-ttu-id="f0340-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f0340-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0340-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0340-132">-WhatIf</span></span>
<span data-ttu-id="f0340-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f0340-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0340-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f0340-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0340-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0340-135">CommonParameters</span></span>
<span data-ttu-id="f0340-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f0340-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0340-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f0340-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0340-138">輸入</span><span class="sxs-lookup"><span data-stu-id="f0340-138">INPUTS</span></span>

### <span data-ttu-id="f0340-139">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f0340-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="f0340-140">System.object</span><span class="sxs-lookup"><span data-stu-id="f0340-140">System.String</span></span>

## <span data-ttu-id="f0340-141">輸出</span><span class="sxs-lookup"><span data-stu-id="f0340-141">OUTPUTS</span></span>

### <span data-ttu-id="f0340-142">System.object</span><span class="sxs-lookup"><span data-stu-id="f0340-142">System.Boolean</span></span>

## <span data-ttu-id="f0340-143">筆記</span><span class="sxs-lookup"><span data-stu-id="f0340-143">NOTES</span></span>
<span data-ttu-id="f0340-144">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式</span><span class="sxs-lookup"><span data-stu-id="f0340-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="f0340-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="f0340-145">RELATED LINKS</span></span>

[<span data-ttu-id="f0340-146">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f0340-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="f0340-147">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f0340-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="f0340-148">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f0340-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="f0340-149">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="f0340-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="f0340-150">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="f0340-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="f0340-151">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="f0340-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="f0340-152">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="f0340-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="f0340-153">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f0340-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f0340-154">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="f0340-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="f0340-155">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f0340-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f0340-156">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f0340-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f0340-157">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f0340-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f0340-158">新-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="f0340-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="f0340-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="f0340-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="f0340-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="f0340-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="f0340-161">停止 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f0340-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f0340-162">開始-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f0340-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f0340-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f0340-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f0340-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="f0340-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="f0340-165">移除-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f0340-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f0340-166">新-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f0340-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f0340-167">AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="f0340-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="f0340-168">AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="f0340-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="f0340-169">AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="f0340-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="f0340-170">AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="f0340-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="f0340-171">AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="f0340-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="f0340-172">AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f0340-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
