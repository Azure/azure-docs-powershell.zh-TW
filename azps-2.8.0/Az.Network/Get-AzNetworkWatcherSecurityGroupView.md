---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchersecuritygroupview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: e1b6b0339b093a048d6d74998ac6b0eb276e81cd
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100411002"
---
# <span data-ttu-id="e43a9-101">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="e43a9-101">Get-AzNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="e43a9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e43a9-102">SYNOPSIS</span></span>
<span data-ttu-id="e43a9-103">在 VM 上查看已配置且有效的網路安全性群組規則。</span><span class="sxs-lookup"><span data-stu-id="e43a9-103">View the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="e43a9-104">語法</span><span class="sxs-lookup"><span data-stu-id="e43a9-104">SYNTAX</span></span>

### <span data-ttu-id="e43a9-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="e43a9-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e43a9-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="e43a9-106">SetByName</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e43a9-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="e43a9-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -Location <String> -TargetVirtualMachineId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e43a9-108">描述</span><span class="sxs-lookup"><span data-stu-id="e43a9-108">DESCRIPTION</span></span>
<span data-ttu-id="e43a9-109">此Get-AzNetworkWatcherSecurityGroupView可讓您查看已配置且有效的網路安全性群組規則，這些規則適用于 VM。</span><span class="sxs-lookup"><span data-stu-id="e43a9-109">The Get-AzNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="e43a9-110">例子</span><span class="sxs-lookup"><span data-stu-id="e43a9-110">EXAMPLES</span></span>

### <span data-ttu-id="e43a9-111">範例 1：在 VM 上撥打安全性群組視圖通話</span><span class="sxs-lookup"><span data-stu-id="e43a9-111">Example 1: Make a Security Group View call on a VM</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="e43a9-112">在上例中，我們先取得地區網路監視程式，再取得地區的 VM。</span><span class="sxs-lookup"><span data-stu-id="e43a9-112">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="e43a9-113">然後，我們在指定的 VM 上進行安全性群組視圖通話。</span><span class="sxs-lookup"><span data-stu-id="e43a9-113">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="e43a9-114">參數</span><span class="sxs-lookup"><span data-stu-id="e43a9-114">PARAMETERS</span></span>

### <span data-ttu-id="e43a9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e43a9-115">-AsJob</span></span>
<span data-ttu-id="e43a9-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e43a9-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e43a9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e43a9-117">-DefaultProfile</span></span>
<span data-ttu-id="e43a9-118">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e43a9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e43a9-119">-位置</span><span class="sxs-lookup"><span data-stu-id="e43a9-119">-Location</span></span>
<span data-ttu-id="e43a9-120">網路監視者的位置。</span><span class="sxs-lookup"><span data-stu-id="e43a9-120">Location of the network watcher.</span></span>

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

### <span data-ttu-id="e43a9-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e43a9-121">-NetworkWatcher</span></span>
<span data-ttu-id="e43a9-122">網路監視程式資源。</span><span class="sxs-lookup"><span data-stu-id="e43a9-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="e43a9-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="e43a9-123">-NetworkWatcherName</span></span>
<span data-ttu-id="e43a9-124">網路監視者的名稱。</span><span class="sxs-lookup"><span data-stu-id="e43a9-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="e43a9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e43a9-125">-ResourceGroupName</span></span>
<span data-ttu-id="e43a9-126">網路監視者資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e43a9-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="e43a9-127">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="e43a9-127">-TargetVirtualMachineId</span></span>
<span data-ttu-id="e43a9-128">目標 VM 識別碼</span><span class="sxs-lookup"><span data-stu-id="e43a9-128">The target VM Id</span></span>

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

### <span data-ttu-id="e43a9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e43a9-129">CommonParameters</span></span>
<span data-ttu-id="e43a9-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e43a9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e43a9-131">詳細資訊[請參閱about_CommonParameters。](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e43a9-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e43a9-132">輸入</span><span class="sxs-lookup"><span data-stu-id="e43a9-132">INPUTS</span></span>

### <span data-ttu-id="e43a9-133">Microsoft.Azure.Commands.Network.models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e43a9-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="e43a9-134">System.String</span><span class="sxs-lookup"><span data-stu-id="e43a9-134">System.String</span></span>

## <span data-ttu-id="e43a9-135">輸出</span><span class="sxs-lookup"><span data-stu-id="e43a9-135">OUTPUTS</span></span>

### <span data-ttu-id="e43a9-136">Microsoft.Azure.Commands.Network.models.PSSecurityGroupViewResult</span><span class="sxs-lookup"><span data-stu-id="e43a9-136">Microsoft.Azure.Commands.Network.Models.PSSecurityGroupViewResult</span></span>

## <span data-ttu-id="e43a9-137">筆記</span><span class="sxs-lookup"><span data-stu-id="e43a9-137">NOTES</span></span>
<span data-ttu-id="e43a9-138">關鍵字：azure、azurerm、arm、resource、management、manager、network、network、network watcher、flow、ip</span><span class="sxs-lookup"><span data-stu-id="e43a9-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="e43a9-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="e43a9-139">RELATED LINKS</span></span>

[<span data-ttu-id="e43a9-140">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e43a9-140">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="e43a9-141">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e43a9-141">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="e43a9-142">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e43a9-142">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="e43a9-143">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="e43a9-143">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="e43a9-144">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="e43a9-144">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="e43a9-145">Get-AzNetworkWatcherTopwork</span><span class="sxs-lookup"><span data-stu-id="e43a9-145">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="e43a9-146">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="e43a9-146">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="e43a9-147">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e43a9-147">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e43a9-148">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="e43a9-148">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="e43a9-149">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e43a9-149">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e43a9-150">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e43a9-150">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e43a9-151">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e43a9-151">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e43a9-152">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="e43a9-152">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="e43a9-153">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="e43a9-153">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="e43a9-154">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="e43a9-154">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="e43a9-155">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e43a9-155">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e43a9-156">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e43a9-156">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e43a9-157">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e43a9-157">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e43a9-158">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="e43a9-158">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="e43a9-159">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e43a9-159">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e43a9-160">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e43a9-160">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e43a9-161">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="e43a9-161">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="e43a9-162">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="e43a9-162">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="e43a9-163">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="e43a9-163">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="e43a9-164">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="e43a9-164">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="e43a9-165">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="e43a9-165">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="e43a9-166">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e43a9-166">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
