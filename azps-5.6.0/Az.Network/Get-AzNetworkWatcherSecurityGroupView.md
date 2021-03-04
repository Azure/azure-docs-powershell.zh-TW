---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkwatchersecuritygroupview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: 3d2fa4a0d5c98ae468466780cffc2ea6439343f8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902514"
---
# <span data-ttu-id="254a4-101">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="254a4-101">Get-AzNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="254a4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="254a4-102">SYNOPSIS</span></span>
<span data-ttu-id="254a4-103">在 VM 上查看已配置且有效的網路安全性群組規則。</span><span class="sxs-lookup"><span data-stu-id="254a4-103">View the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="254a4-104">語法</span><span class="sxs-lookup"><span data-stu-id="254a4-104">SYNTAX</span></span>

### <span data-ttu-id="254a4-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="254a4-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="254a4-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="254a4-106">SetByName</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="254a4-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="254a4-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -Location <String> -TargetVirtualMachineId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="254a4-108">描述</span><span class="sxs-lookup"><span data-stu-id="254a4-108">DESCRIPTION</span></span>
<span data-ttu-id="254a4-109">此Get-AzNetworkWatcherSecurityGroupView可讓您查看已配置且有效的網路安全性群組規則，這些規則適用于 VM。</span><span class="sxs-lookup"><span data-stu-id="254a4-109">The Get-AzNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="254a4-110">例子</span><span class="sxs-lookup"><span data-stu-id="254a4-110">EXAMPLES</span></span>

### <span data-ttu-id="254a4-111">範例 1：在 VM 上撥打安全性群組視圖通話</span><span class="sxs-lookup"><span data-stu-id="254a4-111">Example 1: Make a Security Group View call on a VM</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="254a4-112">在上例中，我們先取得地區網路監視程式，再取得地區的 VM。</span><span class="sxs-lookup"><span data-stu-id="254a4-112">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="254a4-113">然後，我們在指定的 VM 上進行安全性群組視圖通話。</span><span class="sxs-lookup"><span data-stu-id="254a4-113">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="254a4-114">參數</span><span class="sxs-lookup"><span data-stu-id="254a4-114">PARAMETERS</span></span>

### <span data-ttu-id="254a4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="254a4-115">-AsJob</span></span>
<span data-ttu-id="254a4-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="254a4-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="254a4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="254a4-117">-DefaultProfile</span></span>
<span data-ttu-id="254a4-118">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="254a4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="254a4-119">-位置</span><span class="sxs-lookup"><span data-stu-id="254a4-119">-Location</span></span>
<span data-ttu-id="254a4-120">網路監視者的位置。</span><span class="sxs-lookup"><span data-stu-id="254a4-120">Location of the network watcher.</span></span>

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

### <span data-ttu-id="254a4-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="254a4-121">-NetworkWatcher</span></span>
<span data-ttu-id="254a4-122">網路監視程式資源。</span><span class="sxs-lookup"><span data-stu-id="254a4-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="254a4-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="254a4-123">-NetworkWatcherName</span></span>
<span data-ttu-id="254a4-124">網路監視者的名稱。</span><span class="sxs-lookup"><span data-stu-id="254a4-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="254a4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="254a4-125">-ResourceGroupName</span></span>
<span data-ttu-id="254a4-126">網路監視者資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="254a4-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="254a4-127">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="254a4-127">-TargetVirtualMachineId</span></span>
<span data-ttu-id="254a4-128">目標 VM 識別碼</span><span class="sxs-lookup"><span data-stu-id="254a4-128">The target VM Id</span></span>

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

### <span data-ttu-id="254a4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="254a4-129">CommonParameters</span></span>
<span data-ttu-id="254a4-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="254a4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="254a4-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="254a4-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="254a4-132">輸入</span><span class="sxs-lookup"><span data-stu-id="254a4-132">INPUTS</span></span>

### <span data-ttu-id="254a4-133">Microsoft.Azure.Commands.Network.models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="254a4-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="254a4-134">System.String</span><span class="sxs-lookup"><span data-stu-id="254a4-134">System.String</span></span>

## <span data-ttu-id="254a4-135">輸出</span><span class="sxs-lookup"><span data-stu-id="254a4-135">OUTPUTS</span></span>

### <span data-ttu-id="254a4-136">Microsoft.Azure.Commands.Network.models.PSSecurityGroupViewResult</span><span class="sxs-lookup"><span data-stu-id="254a4-136">Microsoft.Azure.Commands.Network.Models.PSSecurityGroupViewResult</span></span>

## <span data-ttu-id="254a4-137">筆記</span><span class="sxs-lookup"><span data-stu-id="254a4-137">NOTES</span></span>
<span data-ttu-id="254a4-138">關鍵字：azure、azurerm、arm、resource、management、manager、network、network、network watcher、flow、ip</span><span class="sxs-lookup"><span data-stu-id="254a4-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="254a4-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="254a4-139">RELATED LINKS</span></span>

[<span data-ttu-id="254a4-140">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="254a4-140">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="254a4-141">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="254a4-141">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="254a4-142">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="254a4-142">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="254a4-143">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="254a4-143">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="254a4-144">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="254a4-144">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="254a4-145">Get-AzNetworkWatcherTopwork</span><span class="sxs-lookup"><span data-stu-id="254a4-145">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="254a4-146">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="254a4-146">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="254a4-147">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="254a4-147">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="254a4-148">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="254a4-148">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="254a4-149">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="254a4-149">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="254a4-150">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="254a4-150">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="254a4-151">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="254a4-151">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="254a4-152">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="254a4-152">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="254a4-153">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="254a4-153">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="254a4-154">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="254a4-154">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="254a4-155">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="254a4-155">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="254a4-156">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="254a4-156">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="254a4-157">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="254a4-157">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="254a4-158">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="254a4-158">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="254a4-159">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="254a4-159">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="254a4-160">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="254a4-160">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="254a4-161">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="254a4-161">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="254a4-162">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="254a4-162">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="254a4-163">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="254a4-163">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="254a4-164">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="254a4-164">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="254a4-165">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="254a4-165">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="254a4-166">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="254a4-166">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
