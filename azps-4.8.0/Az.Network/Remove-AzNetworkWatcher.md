---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
ms.openlocfilehash: fb2dfd74e4807aab76fb48a4593a8a46c4fe6f3f
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412872"
---
# <span data-ttu-id="42251-101">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="42251-101">Remove-AzNetworkWatcher</span></span>

## <span data-ttu-id="42251-102">簡介</span><span class="sxs-lookup"><span data-stu-id="42251-102">SYNOPSIS</span></span>
<span data-ttu-id="42251-103">移除網路監視程式。</span><span class="sxs-lookup"><span data-stu-id="42251-103">Removes a Network Watcher.</span></span>

## <span data-ttu-id="42251-104">語法</span><span class="sxs-lookup"><span data-stu-id="42251-104">SYNTAX</span></span>

### <span data-ttu-id="42251-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="42251-105">SetByResource</span></span>
```
Remove-AzNetworkWatcher -NetworkWatcher <PSNetworkWatcher> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42251-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="42251-106">SetByName</span></span>
```
Remove-AzNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42251-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="42251-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcher -Location <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42251-108">描述</span><span class="sxs-lookup"><span data-stu-id="42251-108">DESCRIPTION</span></span>
<span data-ttu-id="42251-109">Cmdlet Remove-AzNetworkWatcher移除網路監視程式資源。</span><span class="sxs-lookup"><span data-stu-id="42251-109">The Remove-AzNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="42251-110">例子</span><span class="sxs-lookup"><span data-stu-id="42251-110">EXAMPLES</span></span>

### <span data-ttu-id="42251-111">範例 1：建立及刪除網路監視程式</span><span class="sxs-lookup"><span data-stu-id="42251-111">Example 1: Create and delete a Network Watcher</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="42251-112">此範例在資源群組中建立網路監視程式，然後立即刪除。</span><span class="sxs-lookup"><span data-stu-id="42251-112">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="42251-113">請注意，每個訂閱每個地區只能建立一個網路監視程式。</span><span class="sxs-lookup"><span data-stu-id="42251-113">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="42251-114">若要隱藏刪除虛擬網路時提示，請使用 -Force 旗標。</span><span class="sxs-lookup"><span data-stu-id="42251-114">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="42251-115">參數</span><span class="sxs-lookup"><span data-stu-id="42251-115">PARAMETERS</span></span>

### <span data-ttu-id="42251-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="42251-116">-AsJob</span></span>
<span data-ttu-id="42251-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="42251-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="42251-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42251-118">-DefaultProfile</span></span>
<span data-ttu-id="42251-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="42251-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42251-120">-位置</span><span class="sxs-lookup"><span data-stu-id="42251-120">-Location</span></span>
<span data-ttu-id="42251-121">網路監視者的位置。</span><span class="sxs-lookup"><span data-stu-id="42251-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="42251-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="42251-122">-Name</span></span>
<span data-ttu-id="42251-123">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="42251-123">The resource name.</span></span>

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

### <span data-ttu-id="42251-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="42251-124">-NetworkWatcher</span></span>
<span data-ttu-id="42251-125">網路監視程式資源。</span><span class="sxs-lookup"><span data-stu-id="42251-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="42251-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="42251-126">-PassThru</span></span>
<span data-ttu-id="42251-127">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="42251-127">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="42251-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42251-128">-ResourceGroupName</span></span>
<span data-ttu-id="42251-129">資源組名。</span><span class="sxs-lookup"><span data-stu-id="42251-129">The resource group name.</span></span>

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

### <span data-ttu-id="42251-130">-確認</span><span class="sxs-lookup"><span data-stu-id="42251-130">-Confirm</span></span>
<span data-ttu-id="42251-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="42251-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42251-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42251-132">-WhatIf</span></span>
<span data-ttu-id="42251-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="42251-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42251-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="42251-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42251-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42251-135">CommonParameters</span></span>
<span data-ttu-id="42251-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="42251-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42251-137">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="42251-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42251-138">輸入</span><span class="sxs-lookup"><span data-stu-id="42251-138">INPUTS</span></span>

### <span data-ttu-id="42251-139">Microsoft.Azure.Commands.Network.models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="42251-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="42251-140">System.String</span><span class="sxs-lookup"><span data-stu-id="42251-140">System.String</span></span>

## <span data-ttu-id="42251-141">輸出</span><span class="sxs-lookup"><span data-stu-id="42251-141">OUTPUTS</span></span>

### <span data-ttu-id="42251-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="42251-142">System.Boolean</span></span>

## <span data-ttu-id="42251-143">筆記</span><span class="sxs-lookup"><span data-stu-id="42251-143">NOTES</span></span>
<span data-ttu-id="42251-144">關鍵字：azure、azurerm、arm、resource、management、manager、network、network、network watcher</span><span class="sxs-lookup"><span data-stu-id="42251-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="42251-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="42251-145">RELATED LINKS</span></span>

[<span data-ttu-id="42251-146">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="42251-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="42251-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="42251-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="42251-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="42251-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="42251-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="42251-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="42251-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="42251-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="42251-151">Get-AzNetworkWatcherTopwork</span><span class="sxs-lookup"><span data-stu-id="42251-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="42251-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="42251-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="42251-153">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="42251-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="42251-154">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="42251-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="42251-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="42251-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="42251-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="42251-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="42251-157">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="42251-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="42251-158">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="42251-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="42251-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="42251-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="42251-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="42251-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="42251-161">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="42251-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="42251-162">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="42251-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="42251-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="42251-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="42251-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="42251-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="42251-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="42251-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="42251-166">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="42251-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="42251-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="42251-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="42251-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="42251-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="42251-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="42251-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="42251-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="42251-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="42251-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="42251-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="42251-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="42251-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
