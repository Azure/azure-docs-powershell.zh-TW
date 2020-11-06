---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcher.md
ms.openlocfilehash: a242c1cbeda2a110f7bb58e8c320f2e9b4d60ac8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455176"
---
# <span data-ttu-id="dbff8-101">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dbff8-101">Remove-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="dbff8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dbff8-102">SYNOPSIS</span></span>
<span data-ttu-id="dbff8-103">移除網路觀察程式。</span><span class="sxs-lookup"><span data-stu-id="dbff8-103">Removes a Network Watcher.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dbff8-104">句法</span><span class="sxs-lookup"><span data-stu-id="dbff8-104">SYNTAX</span></span>

### <span data-ttu-id="dbff8-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="dbff8-105">SetByResource</span></span>
```
Remove-AzureRmNetworkWatcher -NetworkWatcher <PSNetworkWatcher> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbff8-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="dbff8-106">SetByName</span></span>
```
Remove-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbff8-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="dbff8-107">SetByLocation</span></span>
```
Remove-AzureRmNetworkWatcher -Location <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbff8-108">說明</span><span class="sxs-lookup"><span data-stu-id="dbff8-108">DESCRIPTION</span></span>
<span data-ttu-id="dbff8-109">Remove-AzureRmNetworkWatcher Cmdlet 會移除網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="dbff8-109">The Remove-AzureRmNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="dbff8-110">示例</span><span class="sxs-lookup"><span data-stu-id="dbff8-110">EXAMPLES</span></span>

### <span data-ttu-id="dbff8-111">範例1：建立及刪除網路觀察程式</span><span class="sxs-lookup"><span data-stu-id="dbff8-111">Example 1: Create and delete a Network Watcher</span></span>
```
New-AzureRmResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="dbff8-112">這個範例會在資源群組中建立網路觀察程式，然後立即將它刪除。</span><span class="sxs-lookup"><span data-stu-id="dbff8-112">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="dbff8-113">請注意，每個訂閱只能建立一個網路觀察程式。</span><span class="sxs-lookup"><span data-stu-id="dbff8-113">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="dbff8-114">若要在刪除虛擬網路時取消提示，請使用-Force 標誌。</span><span class="sxs-lookup"><span data-stu-id="dbff8-114">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="dbff8-115">參數</span><span class="sxs-lookup"><span data-stu-id="dbff8-115">PARAMETERS</span></span>

### <span data-ttu-id="dbff8-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dbff8-116">-AsJob</span></span>
<span data-ttu-id="dbff8-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="dbff8-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dbff8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbff8-118">-DefaultProfile</span></span>
<span data-ttu-id="dbff8-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dbff8-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbff8-120">-位置</span><span class="sxs-lookup"><span data-stu-id="dbff8-120">-Location</span></span>
<span data-ttu-id="dbff8-121">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="dbff8-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="dbff8-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="dbff8-122">-Name</span></span>
<span data-ttu-id="dbff8-123">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="dbff8-123">The resource name.</span></span>

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

### <span data-ttu-id="dbff8-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dbff8-124">-NetworkWatcher</span></span>
<span data-ttu-id="dbff8-125">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="dbff8-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="dbff8-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dbff8-126">-PassThru</span></span>
<span data-ttu-id="dbff8-127">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="dbff8-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="dbff8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbff8-128">-ResourceGroupName</span></span>
<span data-ttu-id="dbff8-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dbff8-129">The resource group name.</span></span>

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

### <span data-ttu-id="dbff8-130">-確認</span><span class="sxs-lookup"><span data-stu-id="dbff8-130">-Confirm</span></span>
<span data-ttu-id="dbff8-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dbff8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbff8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbff8-132">-WhatIf</span></span>
<span data-ttu-id="dbff8-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dbff8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbff8-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dbff8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbff8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbff8-135">CommonParameters</span></span>
<span data-ttu-id="dbff8-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dbff8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbff8-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dbff8-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbff8-138">輸入</span><span class="sxs-lookup"><span data-stu-id="dbff8-138">INPUTS</span></span>

### <span data-ttu-id="dbff8-139">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="dbff8-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="dbff8-140">參數： NetworkWatcher (ByValue) </span><span class="sxs-lookup"><span data-stu-id="dbff8-140">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="dbff8-141">System.object</span><span class="sxs-lookup"><span data-stu-id="dbff8-141">System.String</span></span>
<span data-ttu-id="dbff8-142">參數： Name (ByValue) </span><span class="sxs-lookup"><span data-stu-id="dbff8-142">Parameters: Name (ByValue)</span></span>

## <span data-ttu-id="dbff8-143">輸出</span><span class="sxs-lookup"><span data-stu-id="dbff8-143">OUTPUTS</span></span>

### <span data-ttu-id="dbff8-144">System.object</span><span class="sxs-lookup"><span data-stu-id="dbff8-144">System.Boolean</span></span>

## <span data-ttu-id="dbff8-145">筆記</span><span class="sxs-lookup"><span data-stu-id="dbff8-145">NOTES</span></span>
<span data-ttu-id="dbff8-146">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式</span><span class="sxs-lookup"><span data-stu-id="dbff8-146">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="dbff8-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="dbff8-147">RELATED LINKS</span></span>

[<span data-ttu-id="dbff8-148">新-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dbff8-148">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="dbff8-149">AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dbff8-149">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="dbff8-150">移除-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dbff8-150">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="dbff8-151">AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="dbff8-151">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="dbff8-152">AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="dbff8-152">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="dbff8-153">AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="dbff8-153">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="dbff8-154">開始-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="dbff8-154">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="dbff8-155">新-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dbff8-155">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dbff8-156">新-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="dbff8-156">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="dbff8-157">AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dbff8-157">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dbff8-158">移除-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dbff8-158">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dbff8-159">停止 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dbff8-159">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dbff8-160">新-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="dbff8-160">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="dbff8-161">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="dbff8-161">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="dbff8-162">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="dbff8-162">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="dbff8-163">停止 AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="dbff8-163">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="dbff8-164">開始-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="dbff8-164">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="dbff8-165">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="dbff8-165">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="dbff8-166">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="dbff8-166">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="dbff8-167">移除-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="dbff8-167">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="dbff8-168">新-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="dbff8-168">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="dbff8-169">AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="dbff8-169">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="dbff8-170">AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="dbff8-170">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="dbff8-171">AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="dbff8-171">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="dbff8-172">AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="dbff8-172">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="dbff8-173">AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="dbff8-173">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="dbff8-174">AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="dbff8-174">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
