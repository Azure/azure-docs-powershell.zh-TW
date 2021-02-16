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
ms.locfileid: "100398590"
---
# <span data-ttu-id="2ad62-101">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="2ad62-101">Remove-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="2ad62-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2ad62-102">SYNOPSIS</span></span>
<span data-ttu-id="2ad62-103">刪除指定的流程記錄資源。</span><span class="sxs-lookup"><span data-stu-id="2ad62-103">Deletes the specified flow log resource.</span></span>

## <span data-ttu-id="2ad62-104">語法</span><span class="sxs-lookup"><span data-stu-id="2ad62-104">SYNTAX</span></span>

### <span data-ttu-id="2ad62-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="2ad62-105">SetByName (Default)</span></span>
```
Remove-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ad62-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="2ad62-106">SetByResource</span></span>
```
Remove-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ad62-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="2ad62-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcherFlowLog -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ad62-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2ad62-108">SetByResourceId</span></span>
```
Remove-AzNetworkWatcherFlowLog -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ad62-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="2ad62-109">SetByInputObject</span></span>
```
Remove-AzNetworkWatcherFlowLog -InputObject <PSFlowLogResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ad62-110">描述</span><span class="sxs-lookup"><span data-stu-id="2ad62-110">DESCRIPTION</span></span>
<span data-ttu-id="2ad62-111">刪除指定的流程記錄資源。</span><span class="sxs-lookup"><span data-stu-id="2ad62-111">Deletes the specified flow log resource.</span></span>

## <span data-ttu-id="2ad62-112">例子</span><span class="sxs-lookup"><span data-stu-id="2ad62-112">EXAMPLES</span></span>

### <span data-ttu-id="2ad62-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="2ad62-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetworkWatcherFlowLog -Location eastus -Name pstest
```

## <span data-ttu-id="2ad62-114">參數</span><span class="sxs-lookup"><span data-stu-id="2ad62-114">PARAMETERS</span></span>

### <span data-ttu-id="2ad62-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2ad62-115">-AsJob</span></span>
<span data-ttu-id="2ad62-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2ad62-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2ad62-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ad62-117">-DefaultProfile</span></span>
<span data-ttu-id="2ad62-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2ad62-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ad62-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ad62-119">-InputObject</span></span>
<span data-ttu-id="2ad62-120">流程記錄物件。</span><span class="sxs-lookup"><span data-stu-id="2ad62-120">Flow log object.</span></span>

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

### <span data-ttu-id="2ad62-121">-位置</span><span class="sxs-lookup"><span data-stu-id="2ad62-121">-Location</span></span>
<span data-ttu-id="2ad62-122">網路監視者的位置。</span><span class="sxs-lookup"><span data-stu-id="2ad62-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="2ad62-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="2ad62-123">-Name</span></span>
<span data-ttu-id="2ad62-124">流程記錄名稱。</span><span class="sxs-lookup"><span data-stu-id="2ad62-124">The flow log name.</span></span>

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

### <span data-ttu-id="2ad62-125">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2ad62-125">-NetworkWatcher</span></span>
<span data-ttu-id="2ad62-126">網路監視程式資源。</span><span class="sxs-lookup"><span data-stu-id="2ad62-126">The network watcher resource.</span></span>

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

### <span data-ttu-id="2ad62-127">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="2ad62-127">-NetworkWatcherName</span></span>
<span data-ttu-id="2ad62-128">網路監視者的名稱。</span><span class="sxs-lookup"><span data-stu-id="2ad62-128">The name of network watcher.</span></span>

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

### <span data-ttu-id="2ad62-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2ad62-129">-PassThru</span></span>
<span data-ttu-id="2ad62-130">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="2ad62-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="2ad62-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ad62-131">-ResourceGroupName</span></span>
<span data-ttu-id="2ad62-132">網路監視者資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2ad62-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="2ad62-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ad62-133">-ResourceId</span></span>
<span data-ttu-id="2ad62-134">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="2ad62-134">Resource ID.</span></span>

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

### <span data-ttu-id="2ad62-135">-確認</span><span class="sxs-lookup"><span data-stu-id="2ad62-135">-Confirm</span></span>
<span data-ttu-id="2ad62-136">執行 Cmdlet 之前，系統會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2ad62-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ad62-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ad62-137">-WhatIf</span></span>
<span data-ttu-id="2ad62-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2ad62-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ad62-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2ad62-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ad62-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ad62-140">CommonParameters</span></span>
<span data-ttu-id="2ad62-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2ad62-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ad62-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2ad62-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ad62-143">輸入</span><span class="sxs-lookup"><span data-stu-id="2ad62-143">INPUTS</span></span>

### <span data-ttu-id="2ad62-144">Microsoft.Azure.Commands.Network.models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2ad62-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="2ad62-145">System.String</span><span class="sxs-lookup"><span data-stu-id="2ad62-145">System.String</span></span>

### <span data-ttu-id="2ad62-146">Microsoft.Azure.Commands.Network.models.PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="2ad62-146">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="2ad62-147">輸出</span><span class="sxs-lookup"><span data-stu-id="2ad62-147">OUTPUTS</span></span>

### <span data-ttu-id="2ad62-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2ad62-148">System.Boolean</span></span>

## <span data-ttu-id="2ad62-149">筆記</span><span class="sxs-lookup"><span data-stu-id="2ad62-149">NOTES</span></span>

## <span data-ttu-id="2ad62-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="2ad62-150">RELATED LINKS</span></span>

[<span data-ttu-id="2ad62-151">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2ad62-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="2ad62-152">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2ad62-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="2ad62-153">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2ad62-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="2ad62-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="2ad62-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="2ad62-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="2ad62-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="2ad62-156">Get-AzNetworkWatcherTopwork</span><span class="sxs-lookup"><span data-stu-id="2ad62-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="2ad62-157">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="2ad62-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="2ad62-158">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2ad62-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2ad62-159">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="2ad62-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="2ad62-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2ad62-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2ad62-161">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2ad62-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2ad62-162">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2ad62-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2ad62-163">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="2ad62-163">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="2ad62-164">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="2ad62-164">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="2ad62-165">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="2ad62-165">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="2ad62-166">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2ad62-166">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2ad62-167">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2ad62-167">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2ad62-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2ad62-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2ad62-169">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="2ad62-169">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="2ad62-170">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2ad62-170">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2ad62-171">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2ad62-171">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2ad62-172">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="2ad62-172">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="2ad62-173">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="2ad62-173">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="2ad62-174">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="2ad62-174">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="2ad62-175">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="2ad62-175">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="2ad62-176">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="2ad62-176">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="2ad62-177">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2ad62-177">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2ad62-178">New-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="2ad62-178">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="2ad62-179">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="2ad62-179">Set-AzNetworkWatcherFlowLog</span></span>](./Set-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="2ad62-180">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="2ad62-180">Get-AzNetworkWatcherFlowLog</span></span>](./Get-AzNetworkWatcherFlowLog.md)
