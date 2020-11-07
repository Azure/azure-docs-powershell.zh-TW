---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 71b717ec1777dfd55e29925e82923d8d9f8d7a37
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789118"
---
# <span data-ttu-id="e2f71-101">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e2f71-101">Remove-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="e2f71-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e2f71-102">SYNOPSIS</span></span>
<span data-ttu-id="e2f71-103">移除 [連接監視器]。</span><span class="sxs-lookup"><span data-stu-id="e2f71-103">Remove connection monitor.</span></span>

## <span data-ttu-id="e2f71-104">句法</span><span class="sxs-lookup"><span data-stu-id="e2f71-104">SYNTAX</span></span>

### <span data-ttu-id="e2f71-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="e2f71-105">SetByName (Default)</span></span>
```
Remove-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2f71-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e2f71-106">SetByResource</span></span>
```
Remove-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2f71-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="e2f71-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2f71-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e2f71-108">SetByResourceId</span></span>
```
Remove-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2f71-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="e2f71-109">SetByInputObject</span></span>
```
Remove-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2f71-110">說明</span><span class="sxs-lookup"><span data-stu-id="e2f71-110">DESCRIPTION</span></span>
<span data-ttu-id="e2f71-111">AzNetworkWatcherConnectionMonitor Cmdlet 會移除指定的連接監視器。</span><span class="sxs-lookup"><span data-stu-id="e2f71-111">The remove-AzNetworkWatcherConnectionMonitor cmdlet removes the specified connection monitor.</span></span>

## <span data-ttu-id="e2f71-112">示例</span><span class="sxs-lookup"><span data-stu-id="e2f71-112">EXAMPLES</span></span>

### <span data-ttu-id="e2f71-113">範例1：移除指定的連接監視器</span><span class="sxs-lookup"><span data-stu-id="e2f71-113">Example 1: Remove the specified connection monitor</span></span>
```
PS C:\> Remove-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm
```

<span data-ttu-id="e2f71-114">在這個範例中，我們會刪除由位置和名稱指定的連線監視器。</span><span class="sxs-lookup"><span data-stu-id="e2f71-114">In this example we delete the connection monitor specified by location and name.</span></span>

## <span data-ttu-id="e2f71-115">參數</span><span class="sxs-lookup"><span data-stu-id="e2f71-115">PARAMETERS</span></span>

### <span data-ttu-id="e2f71-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2f71-116">-AsJob</span></span>
<span data-ttu-id="e2f71-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e2f71-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e2f71-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2f71-118">-DefaultProfile</span></span>
<span data-ttu-id="e2f71-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e2f71-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2f71-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2f71-120">-InputObject</span></span>
<span data-ttu-id="e2f71-121">[連接監視器] 物件。</span><span class="sxs-lookup"><span data-stu-id="e2f71-121">Connection monitor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2f71-122">-位置</span><span class="sxs-lookup"><span data-stu-id="e2f71-122">-Location</span></span>
<span data-ttu-id="e2f71-123">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="e2f71-123">Location of the network watcher.</span></span>

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

### <span data-ttu-id="e2f71-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="e2f71-124">-Name</span></span>
<span data-ttu-id="e2f71-125">[連接監視器] 名稱。</span><span class="sxs-lookup"><span data-stu-id="e2f71-125">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2f71-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e2f71-126">-NetworkWatcher</span></span>
<span data-ttu-id="e2f71-127">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="e2f71-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="e2f71-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="e2f71-128">-NetworkWatcherName</span></span>
<span data-ttu-id="e2f71-129">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="e2f71-129">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2f71-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2f71-130">-PassThru</span></span>
<span data-ttu-id="e2f71-131">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="e2f71-131">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="e2f71-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2f71-132">-ResourceGroupName</span></span>
<span data-ttu-id="e2f71-133">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e2f71-133">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2f71-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2f71-134">-ResourceId</span></span>
<span data-ttu-id="e2f71-135">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="e2f71-135">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2f71-136">-確認</span><span class="sxs-lookup"><span data-stu-id="e2f71-136">-Confirm</span></span>
<span data-ttu-id="e2f71-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e2f71-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2f71-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2f71-138">-WhatIf</span></span>
<span data-ttu-id="e2f71-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e2f71-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2f71-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e2f71-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2f71-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2f71-141">CommonParameters</span></span>
<span data-ttu-id="e2f71-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e2f71-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2f71-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e2f71-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2f71-144">輸入</span><span class="sxs-lookup"><span data-stu-id="e2f71-144">INPUTS</span></span>

### <span data-ttu-id="e2f71-145">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e2f71-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="e2f71-146">System.object</span><span class="sxs-lookup"><span data-stu-id="e2f71-146">System.String</span></span>

### <span data-ttu-id="e2f71-147">PSConnectionMonitorResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e2f71-147">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="e2f71-148">輸出</span><span class="sxs-lookup"><span data-stu-id="e2f71-148">OUTPUTS</span></span>

### <span data-ttu-id="e2f71-149">System.object</span><span class="sxs-lookup"><span data-stu-id="e2f71-149">System.Boolean</span></span>

## <span data-ttu-id="e2f71-150">筆記</span><span class="sxs-lookup"><span data-stu-id="e2f71-150">NOTES</span></span>
<span data-ttu-id="e2f71-151">關鍵字： azure，azurerm，arm，資源，連線，管理，管理員，網路，網路，網路觀察程式，連線監視器</span><span class="sxs-lookup"><span data-stu-id="e2f71-151">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="e2f71-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="e2f71-152">RELATED LINKS</span></span>

[<span data-ttu-id="e2f71-153">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e2f71-153">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="e2f71-154">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e2f71-154">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="e2f71-155">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e2f71-155">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="e2f71-156">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="e2f71-156">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="e2f71-157">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="e2f71-157">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="e2f71-158">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="e2f71-158">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="e2f71-159">AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="e2f71-159">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="e2f71-160">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e2f71-160">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e2f71-161">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="e2f71-161">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="e2f71-162">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e2f71-162">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e2f71-163">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e2f71-163">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e2f71-164">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e2f71-164">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e2f71-165">AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e2f71-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e2f71-166">AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="e2f71-166">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="e2f71-167">移除-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e2f71-167">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e2f71-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e2f71-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e2f71-169">停止 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e2f71-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e2f71-170">新-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e2f71-170">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e2f71-171">新-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2f71-171">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="e2f71-172">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="e2f71-172">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="e2f71-173">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="e2f71-173">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="e2f71-174">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="e2f71-174">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="e2f71-175">開始-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e2f71-175">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e2f71-176">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="e2f71-176">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="e2f71-177">AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="e2f71-177">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="e2f71-178">AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="e2f71-178">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="e2f71-179">AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="e2f71-179">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)
