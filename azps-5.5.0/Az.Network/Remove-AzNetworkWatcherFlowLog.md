---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 5c8532502e4e74b94a9d0c1e252c8d1cea9ddad8
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100411223"
---
# <span data-ttu-id="1ffb3-101">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="1ffb3-101">Remove-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="1ffb3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1ffb3-102">SYNOPSIS</span></span>
<span data-ttu-id="1ffb3-103">刪除指定的流程記錄資源。</span><span class="sxs-lookup"><span data-stu-id="1ffb3-103">Deletes the specified flow log resource.</span></span>

## <span data-ttu-id="1ffb3-104">語法</span><span class="sxs-lookup"><span data-stu-id="1ffb3-104">SYNTAX</span></span>

### <span data-ttu-id="1ffb3-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="1ffb3-105">SetByName (Default)</span></span>
```
Remove-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ffb3-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="1ffb3-106">SetByResource</span></span>
```
Remove-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ffb3-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="1ffb3-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcherFlowLog -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ffb3-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1ffb3-108">SetByResourceId</span></span>
```
Remove-AzNetworkWatcherFlowLog -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ffb3-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="1ffb3-109">SetByInputObject</span></span>
```
Remove-AzNetworkWatcherFlowLog -InputObject <PSFlowLogResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ffb3-110">描述</span><span class="sxs-lookup"><span data-stu-id="1ffb3-110">DESCRIPTION</span></span>
<span data-ttu-id="1ffb3-111">刪除指定的流程記錄資源。</span><span class="sxs-lookup"><span data-stu-id="1ffb3-111">Deletes the specified flow log resource.</span></span>

## <span data-ttu-id="1ffb3-112">例子</span><span class="sxs-lookup"><span data-stu-id="1ffb3-112">EXAMPLES</span></span>

### <span data-ttu-id="1ffb3-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="1ffb3-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetworkWatcherFlowLog -Location eastus -Name pstest
```

## <span data-ttu-id="1ffb3-114">參數</span><span class="sxs-lookup"><span data-stu-id="1ffb3-114">PARAMETERS</span></span>

### <span data-ttu-id="1ffb3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1ffb3-115">-AsJob</span></span>
<span data-ttu-id="1ffb3-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1ffb3-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1ffb3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ffb3-117">-DefaultProfile</span></span>
<span data-ttu-id="1ffb3-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1ffb3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ffb3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ffb3-119">-InputObject</span></span>
<span data-ttu-id="1ffb3-120">流程記錄物件。</span><span class="sxs-lookup"><span data-stu-id="1ffb3-120">Flow log object.</span></span>

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

### <span data-ttu-id="1ffb3-121">-位置</span><span class="sxs-lookup"><span data-stu-id="1ffb3-121">-Location</span></span>
<span data-ttu-id="1ffb3-122">網路監視者的位置。</span><span class="sxs-lookup"><span data-stu-id="1ffb3-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="1ffb3-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="1ffb3-123">-Name</span></span>
<span data-ttu-id="1ffb3-124">流程記錄名稱。</span><span class="sxs-lookup"><span data-stu-id="1ffb3-124">The flow log name.</span></span>

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

### <span data-ttu-id="1ffb3-125">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1ffb3-125">-NetworkWatcher</span></span>
<span data-ttu-id="1ffb3-126">網路監視程式資源。</span><span class="sxs-lookup"><span data-stu-id="1ffb3-126">The network watcher resource.</span></span>

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

### <span data-ttu-id="1ffb3-127">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="1ffb3-127">-NetworkWatcherName</span></span>
<span data-ttu-id="1ffb3-128">網路監視者的名稱。</span><span class="sxs-lookup"><span data-stu-id="1ffb3-128">The name of network watcher.</span></span>

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

### <span data-ttu-id="1ffb3-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1ffb3-129">-PassThru</span></span>
<span data-ttu-id="1ffb3-130">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="1ffb3-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="1ffb3-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ffb3-131">-ResourceGroupName</span></span>
<span data-ttu-id="1ffb3-132">網路監視者資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1ffb3-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="1ffb3-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ffb3-133">-ResourceId</span></span>
<span data-ttu-id="1ffb3-134">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1ffb3-134">Resource ID.</span></span>

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

### <span data-ttu-id="1ffb3-135">-確認</span><span class="sxs-lookup"><span data-stu-id="1ffb3-135">-Confirm</span></span>
<span data-ttu-id="1ffb3-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1ffb3-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ffb3-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ffb3-137">-WhatIf</span></span>
<span data-ttu-id="1ffb3-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1ffb3-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ffb3-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1ffb3-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ffb3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ffb3-140">CommonParameters</span></span>
<span data-ttu-id="1ffb3-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1ffb3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ffb3-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1ffb3-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ffb3-143">輸入</span><span class="sxs-lookup"><span data-stu-id="1ffb3-143">INPUTS</span></span>

### <span data-ttu-id="1ffb3-144">Microsoft.Azure.Commands.Network.models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1ffb3-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="1ffb3-145">System.String</span><span class="sxs-lookup"><span data-stu-id="1ffb3-145">System.String</span></span>

### <span data-ttu-id="1ffb3-146">Microsoft.Azure.Commands.Network.models.PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="1ffb3-146">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="1ffb3-147">輸出</span><span class="sxs-lookup"><span data-stu-id="1ffb3-147">OUTPUTS</span></span>

### <span data-ttu-id="1ffb3-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1ffb3-148">System.Boolean</span></span>

## <span data-ttu-id="1ffb3-149">筆記</span><span class="sxs-lookup"><span data-stu-id="1ffb3-149">NOTES</span></span>

## <span data-ttu-id="1ffb3-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="1ffb3-150">RELATED LINKS</span></span>

[<span data-ttu-id="1ffb3-151">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1ffb3-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="1ffb3-152">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1ffb3-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="1ffb3-153">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1ffb3-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="1ffb3-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="1ffb3-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="1ffb3-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="1ffb3-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="1ffb3-156">Get-AzNetworkWatcherTopwork</span><span class="sxs-lookup"><span data-stu-id="1ffb3-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="1ffb3-157">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="1ffb3-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="1ffb3-158">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1ffb3-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1ffb3-159">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="1ffb3-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="1ffb3-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1ffb3-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1ffb3-161">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1ffb3-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1ffb3-162">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1ffb3-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1ffb3-163">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="1ffb3-163">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="1ffb3-164">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="1ffb3-164">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="1ffb3-165">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="1ffb3-165">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="1ffb3-166">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1ffb3-166">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1ffb3-167">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1ffb3-167">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1ffb3-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1ffb3-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1ffb3-169">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="1ffb3-169">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="1ffb3-170">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1ffb3-170">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1ffb3-171">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1ffb3-171">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1ffb3-172">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="1ffb3-172">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="1ffb3-173">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="1ffb3-173">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="1ffb3-174">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="1ffb3-174">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="1ffb3-175">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="1ffb3-175">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="1ffb3-176">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="1ffb3-176">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="1ffb3-177">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1ffb3-177">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1ffb3-178">New-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="1ffb3-178">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="1ffb3-179">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="1ffb3-179">Set-AzNetworkWatcherFlowLog</span></span>](./Set-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="1ffb3-180">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="1ffb3-180">Get-AzNetworkWatcherFlowLog</span></span>](./Get-AzNetworkWatcherFlowLog.md)
