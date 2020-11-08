---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchersecuritygroupview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: 37da72dd26df32dddee0ea28d2378418e9e4922e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141405"
---
# <span data-ttu-id="86f5a-101">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="86f5a-101">Get-AzNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="86f5a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="86f5a-102">SYNOPSIS</span></span>
<span data-ttu-id="86f5a-103">在 VM 上查看已設定且有效的網路安全性群組規則。</span><span class="sxs-lookup"><span data-stu-id="86f5a-103">View the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="86f5a-104">句法</span><span class="sxs-lookup"><span data-stu-id="86f5a-104">SYNTAX</span></span>

### <span data-ttu-id="86f5a-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="86f5a-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86f5a-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="86f5a-106">SetByName</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86f5a-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="86f5a-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -Location <String> -TargetVirtualMachineId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86f5a-108">說明</span><span class="sxs-lookup"><span data-stu-id="86f5a-108">DESCRIPTION</span></span>
<span data-ttu-id="86f5a-109">Get-AzNetworkWatcherSecurityGroupView 可讓您在 VM 上查看已設定且有效的網路安全性群組規則。</span><span class="sxs-lookup"><span data-stu-id="86f5a-109">The Get-AzNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="86f5a-110">示例</span><span class="sxs-lookup"><span data-stu-id="86f5a-110">EXAMPLES</span></span>

### <span data-ttu-id="86f5a-111">範例1：在 VM 上建立安全群組視圖呼叫</span><span class="sxs-lookup"><span data-stu-id="86f5a-111">Example 1: Make a Security Group View call on a VM</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="86f5a-112">在上述範例中，我們會先取得地區網路觀察程式，然後再取得區域中的 VM。</span><span class="sxs-lookup"><span data-stu-id="86f5a-112">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="86f5a-113">接著，我們會在指定的 VM 上進行安全性群組視圖通話。</span><span class="sxs-lookup"><span data-stu-id="86f5a-113">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="86f5a-114">參數</span><span class="sxs-lookup"><span data-stu-id="86f5a-114">PARAMETERS</span></span>

### <span data-ttu-id="86f5a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="86f5a-115">-AsJob</span></span>
<span data-ttu-id="86f5a-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="86f5a-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="86f5a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86f5a-117">-DefaultProfile</span></span>
<span data-ttu-id="86f5a-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="86f5a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86f5a-119">-位置</span><span class="sxs-lookup"><span data-stu-id="86f5a-119">-Location</span></span>
<span data-ttu-id="86f5a-120">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="86f5a-120">Location of the network watcher.</span></span>

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

### <span data-ttu-id="86f5a-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="86f5a-121">-NetworkWatcher</span></span>
<span data-ttu-id="86f5a-122">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="86f5a-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="86f5a-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="86f5a-123">-NetworkWatcherName</span></span>
<span data-ttu-id="86f5a-124">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="86f5a-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="86f5a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86f5a-125">-ResourceGroupName</span></span>
<span data-ttu-id="86f5a-126">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="86f5a-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="86f5a-127">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="86f5a-127">-TargetVirtualMachineId</span></span>
<span data-ttu-id="86f5a-128">目標 VM 識別碼</span><span class="sxs-lookup"><span data-stu-id="86f5a-128">The target VM Id</span></span>

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

### <span data-ttu-id="86f5a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86f5a-129">CommonParameters</span></span>
<span data-ttu-id="86f5a-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="86f5a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86f5a-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="86f5a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86f5a-132">輸入</span><span class="sxs-lookup"><span data-stu-id="86f5a-132">INPUTS</span></span>

### <span data-ttu-id="86f5a-133">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="86f5a-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="86f5a-134">System.object</span><span class="sxs-lookup"><span data-stu-id="86f5a-134">System.String</span></span>

## <span data-ttu-id="86f5a-135">輸出</span><span class="sxs-lookup"><span data-stu-id="86f5a-135">OUTPUTS</span></span>

### <span data-ttu-id="86f5a-136">PSSecurityGroupViewResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="86f5a-136">Microsoft.Azure.Commands.Network.Models.PSSecurityGroupViewResult</span></span>

## <span data-ttu-id="86f5a-137">筆記</span><span class="sxs-lookup"><span data-stu-id="86f5a-137">NOTES</span></span>
<span data-ttu-id="86f5a-138">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，流程，ip</span><span class="sxs-lookup"><span data-stu-id="86f5a-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="86f5a-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="86f5a-139">RELATED LINKS</span></span>

[<span data-ttu-id="86f5a-140">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="86f5a-140">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="86f5a-141">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="86f5a-141">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="86f5a-142">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="86f5a-142">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="86f5a-143">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="86f5a-143">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="86f5a-144">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="86f5a-144">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="86f5a-145">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="86f5a-145">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="86f5a-146">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="86f5a-146">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="86f5a-147">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="86f5a-147">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="86f5a-148">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="86f5a-148">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="86f5a-149">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="86f5a-149">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="86f5a-150">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="86f5a-150">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="86f5a-151">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="86f5a-151">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="86f5a-152">新-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="86f5a-152">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="86f5a-153">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="86f5a-153">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="86f5a-154">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="86f5a-154">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="86f5a-155">停止 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="86f5a-155">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="86f5a-156">開始-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="86f5a-156">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="86f5a-157">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="86f5a-157">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="86f5a-158">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="86f5a-158">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="86f5a-159">移除-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="86f5a-159">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="86f5a-160">新-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="86f5a-160">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="86f5a-161">AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="86f5a-161">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="86f5a-162">AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="86f5a-162">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="86f5a-163">AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="86f5a-163">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="86f5a-164">AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="86f5a-164">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="86f5a-165">AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="86f5a-165">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="86f5a-166">AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="86f5a-166">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
