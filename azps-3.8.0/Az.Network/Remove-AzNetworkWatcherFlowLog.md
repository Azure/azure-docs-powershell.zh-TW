---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 8a5f911529a4fc6f1ceb4e242b0e751e5f1a528f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965508"
---
# <span data-ttu-id="fcd98-101">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="fcd98-101">Remove-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="fcd98-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fcd98-102">SYNOPSIS</span></span>
<span data-ttu-id="fcd98-103">刪除指定的 [資料流程記錄] 資源。</span><span class="sxs-lookup"><span data-stu-id="fcd98-103">Deletes the specified flow log resource.</span></span>

## <span data-ttu-id="fcd98-104">句法</span><span class="sxs-lookup"><span data-stu-id="fcd98-104">SYNTAX</span></span>

### <span data-ttu-id="fcd98-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="fcd98-105">SetByName (Default)</span></span>
```
Remove-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcd98-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="fcd98-106">SetByResource</span></span>
```
Remove-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcd98-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="fcd98-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcherFlowLog -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcd98-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="fcd98-108">SetByResourceId</span></span>
```
Remove-AzNetworkWatcherFlowLog -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcd98-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="fcd98-109">SetByInputObject</span></span>
```
Remove-AzNetworkWatcherFlowLog -InputObject <PSFlowLogResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcd98-110">說明</span><span class="sxs-lookup"><span data-stu-id="fcd98-110">DESCRIPTION</span></span>
<span data-ttu-id="fcd98-111">刪除指定的 [資料流程記錄] 資源。</span><span class="sxs-lookup"><span data-stu-id="fcd98-111">Deletes the specified flow log resource.</span></span>

## <span data-ttu-id="fcd98-112">示例</span><span class="sxs-lookup"><span data-stu-id="fcd98-112">EXAMPLES</span></span>

### <span data-ttu-id="fcd98-113">範例1</span><span class="sxs-lookup"><span data-stu-id="fcd98-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetworkWatcherFlowLog -Location eastus -Name pstest
```

## <span data-ttu-id="fcd98-114">參數</span><span class="sxs-lookup"><span data-stu-id="fcd98-114">PARAMETERS</span></span>

### <span data-ttu-id="fcd98-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fcd98-115">-AsJob</span></span>
<span data-ttu-id="fcd98-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="fcd98-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcd98-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcd98-117">-DefaultProfile</span></span>
<span data-ttu-id="fcd98-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fcd98-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcd98-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fcd98-119">-InputObject</span></span>
<span data-ttu-id="fcd98-120">資料流程記錄物件。</span><span class="sxs-lookup"><span data-stu-id="fcd98-120">Flow log object.</span></span>

```yaml
Type: PSFlowLogResource
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fcd98-121">-位置</span><span class="sxs-lookup"><span data-stu-id="fcd98-121">-Location</span></span>
<span data-ttu-id="fcd98-122">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="fcd98-122">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcd98-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="fcd98-123">-Name</span></span>
<span data-ttu-id="fcd98-124">流程記錄名稱。</span><span class="sxs-lookup"><span data-stu-id="fcd98-124">The flow log name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: FlowLogName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcd98-125">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fcd98-125">-NetworkWatcher</span></span>
<span data-ttu-id="fcd98-126">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="fcd98-126">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fcd98-127">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="fcd98-127">-NetworkWatcherName</span></span>
<span data-ttu-id="fcd98-128">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="fcd98-128">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcd98-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fcd98-129">-PassThru</span></span>
<span data-ttu-id="fcd98-130">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="fcd98-130">{{ Fill PassThru Description }}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcd98-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcd98-131">-ResourceGroupName</span></span>
<span data-ttu-id="fcd98-132">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fcd98-132">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcd98-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fcd98-133">-ResourceId</span></span>
<span data-ttu-id="fcd98-134">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="fcd98-134">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcd98-135">-確認</span><span class="sxs-lookup"><span data-stu-id="fcd98-135">-Confirm</span></span>
<span data-ttu-id="fcd98-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fcd98-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcd98-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcd98-137">-WhatIf</span></span>
<span data-ttu-id="fcd98-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fcd98-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcd98-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fcd98-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcd98-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcd98-140">CommonParameters</span></span>
<span data-ttu-id="fcd98-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fcd98-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcd98-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="fcd98-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcd98-143">輸入</span><span class="sxs-lookup"><span data-stu-id="fcd98-143">INPUTS</span></span>

### <span data-ttu-id="fcd98-144">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="fcd98-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="fcd98-145">System.object</span><span class="sxs-lookup"><span data-stu-id="fcd98-145">System.String</span></span>

### <span data-ttu-id="fcd98-146">PSFlowLogResource 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="fcd98-146">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="fcd98-147">輸出</span><span class="sxs-lookup"><span data-stu-id="fcd98-147">OUTPUTS</span></span>

### <span data-ttu-id="fcd98-148">System.object</span><span class="sxs-lookup"><span data-stu-id="fcd98-148">System.Boolean</span></span>

## <span data-ttu-id="fcd98-149">筆記</span><span class="sxs-lookup"><span data-stu-id="fcd98-149">NOTES</span></span>

## <span data-ttu-id="fcd98-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="fcd98-150">RELATED LINKS</span></span>

[<span data-ttu-id="fcd98-151">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fcd98-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="fcd98-152">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fcd98-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="fcd98-153">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fcd98-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="fcd98-154">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="fcd98-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="fcd98-155">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="fcd98-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="fcd98-156">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="fcd98-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="fcd98-157">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="fcd98-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="fcd98-158">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fcd98-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fcd98-159">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="fcd98-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="fcd98-160">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fcd98-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fcd98-161">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fcd98-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fcd98-162">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fcd98-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fcd98-163">新-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="fcd98-163">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="fcd98-164">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="fcd98-164">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="fcd98-165">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="fcd98-165">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="fcd98-166">停止 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fcd98-166">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="fcd98-167">開始-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fcd98-167">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="fcd98-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fcd98-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="fcd98-169">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="fcd98-169">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="fcd98-170">移除-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fcd98-170">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="fcd98-171">新-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fcd98-171">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="fcd98-172">AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="fcd98-172">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="fcd98-173">AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="fcd98-173">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="fcd98-174">AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="fcd98-174">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="fcd98-175">AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="fcd98-175">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="fcd98-176">AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="fcd98-176">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="fcd98-177">AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fcd98-177">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

[<span data-ttu-id="fcd98-178">新-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="fcd98-178">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog)

[<span data-ttu-id="fcd98-179">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="fcd98-179">Set-AzNetworkWatcherFlowLog</span></span>](./Set-AzNetworkWatcherFlowLog)

[<span data-ttu-id="fcd98-180">AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="fcd98-180">Get-AzNetworkWatcherFlowLog</span></span>](./Get-AzNetworkWatcherFlowLog)