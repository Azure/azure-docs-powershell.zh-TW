---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 83d7da65ad8c525d4c37ab1b5f78eb72bf1d9f49
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126353"
---
# <span data-ttu-id="e5886-101">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e5886-101">Start-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="e5886-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e5886-102">SYNOPSIS</span></span>
<span data-ttu-id="e5886-103">啟動連線監視器</span><span class="sxs-lookup"><span data-stu-id="e5886-103">Start a connection monitor</span></span>

## <span data-ttu-id="e5886-104">句法</span><span class="sxs-lookup"><span data-stu-id="e5886-104">SYNTAX</span></span>

### <span data-ttu-id="e5886-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="e5886-105">SetByName (Default)</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5886-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e5886-106">SetByResource</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5886-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="e5886-107">SetByLocation</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5886-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e5886-108">SetByResourceId</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5886-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="e5886-109">SetByInputObject</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5886-110">說明</span><span class="sxs-lookup"><span data-stu-id="e5886-110">DESCRIPTION</span></span>
<span data-ttu-id="e5886-111">Start-AzNetworkWatcherConnectionMonitor Cmdlet 會啟動指定的連接監視器。</span><span class="sxs-lookup"><span data-stu-id="e5886-111">The Start-AzNetworkWatcherConnectionMonitor cmdlet starts the specified connection monitor.</span></span>

## <span data-ttu-id="e5886-112">示例</span><span class="sxs-lookup"><span data-stu-id="e5886-112">EXAMPLES</span></span>

### <span data-ttu-id="e5886-113">範例1：啟動連線監視器</span><span class="sxs-lookup"><span data-stu-id="e5886-113">Example 1: Start a connection monitor</span></span>
```
PS C:\> Start-AzNetworkWatcherConnectionMonitor -NetworkWatcherName NetworkWatcher_centraluseuap -ResourceGroupName NetworkWatcherRG -Name cm
```

<span data-ttu-id="e5886-114">在這個範例中，我們會啟動由名稱和網路監視程式指定的連線監視器</span><span class="sxs-lookup"><span data-stu-id="e5886-114">In this example we start connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="e5886-115">參數</span><span class="sxs-lookup"><span data-stu-id="e5886-115">PARAMETERS</span></span>

### <span data-ttu-id="e5886-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e5886-116">-AsJob</span></span>
<span data-ttu-id="e5886-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5886-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e5886-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5886-118">-DefaultProfile</span></span>
<span data-ttu-id="e5886-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e5886-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5886-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5886-120">-InputObject</span></span>
<span data-ttu-id="e5886-121">[連接監視器] 物件。</span><span class="sxs-lookup"><span data-stu-id="e5886-121">Connection monitor object.</span></span>

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

### <span data-ttu-id="e5886-122">-位置</span><span class="sxs-lookup"><span data-stu-id="e5886-122">-Location</span></span>
<span data-ttu-id="e5886-123">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="e5886-123">Location of the network watcher.</span></span>

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

### <span data-ttu-id="e5886-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="e5886-124">-Name</span></span>
<span data-ttu-id="e5886-125">[連接監視器] 名稱。</span><span class="sxs-lookup"><span data-stu-id="e5886-125">The connection monitor name.</span></span>

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

### <span data-ttu-id="e5886-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e5886-126">-NetworkWatcher</span></span>
<span data-ttu-id="e5886-127">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="e5886-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="e5886-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="e5886-128">-NetworkWatcherName</span></span>
<span data-ttu-id="e5886-129">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5886-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="e5886-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5886-130">-PassThru</span></span>
<span data-ttu-id="e5886-131">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="e5886-131">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="e5886-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5886-132">-ResourceGroupName</span></span>
<span data-ttu-id="e5886-133">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5886-133">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="e5886-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5886-134">-ResourceId</span></span>
<span data-ttu-id="e5886-135">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="e5886-135">Resource ID.</span></span>

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

### <span data-ttu-id="e5886-136">-確認</span><span class="sxs-lookup"><span data-stu-id="e5886-136">-Confirm</span></span>
<span data-ttu-id="e5886-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e5886-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5886-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5886-138">-WhatIf</span></span>
<span data-ttu-id="e5886-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e5886-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5886-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5886-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5886-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5886-141">CommonParameters</span></span>
<span data-ttu-id="e5886-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e5886-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5886-143">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e5886-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5886-144">輸入</span><span class="sxs-lookup"><span data-stu-id="e5886-144">INPUTS</span></span>

### <span data-ttu-id="e5886-145">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e5886-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="e5886-146">System.object</span><span class="sxs-lookup"><span data-stu-id="e5886-146">System.String</span></span>

### <span data-ttu-id="e5886-147">PSConnectionMonitorResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e5886-147">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="e5886-148">輸出</span><span class="sxs-lookup"><span data-stu-id="e5886-148">OUTPUTS</span></span>

### <span data-ttu-id="e5886-149">System.object</span><span class="sxs-lookup"><span data-stu-id="e5886-149">System.Boolean</span></span>

## <span data-ttu-id="e5886-150">筆記</span><span class="sxs-lookup"><span data-stu-id="e5886-150">NOTES</span></span>
<span data-ttu-id="e5886-151">關鍵字： azure，azurerm，arm，資源，連線，管理，管理員，網路，網路，網路觀察程式，連線監視器</span><span class="sxs-lookup"><span data-stu-id="e5886-151">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="e5886-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="e5886-152">RELATED LINKS</span></span>

[<span data-ttu-id="e5886-153">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e5886-153">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="e5886-154">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e5886-154">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="e5886-155">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e5886-155">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="e5886-156">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="e5886-156">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="e5886-157">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="e5886-157">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="e5886-158">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="e5886-158">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="e5886-159">AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="e5886-159">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="e5886-160">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e5886-160">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e5886-161">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="e5886-161">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="e5886-162">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e5886-162">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e5886-163">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e5886-163">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e5886-164">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e5886-164">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e5886-165">AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e5886-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e5886-166">AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="e5886-166">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="e5886-167">移除-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e5886-167">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e5886-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e5886-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e5886-169">停止 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e5886-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e5886-170">新-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e5886-170">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e5886-171">新-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5886-171">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="e5886-172">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="e5886-172">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="e5886-173">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="e5886-173">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="e5886-174">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="e5886-174">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="e5886-175">開始-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e5886-175">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e5886-176">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="e5886-176">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="e5886-177">AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="e5886-177">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="e5886-178">AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="e5886-178">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="e5886-179">AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="e5886-179">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)
