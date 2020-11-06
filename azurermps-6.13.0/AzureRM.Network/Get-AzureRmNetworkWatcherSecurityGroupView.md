---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchersecuritygroupview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: 9fe23ea5fa9bef544feae6112879cb1be6eeae7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446946"
---
# <span data-ttu-id="cfde3-101">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="cfde3-101">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="cfde3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cfde3-102">SYNOPSIS</span></span>
<span data-ttu-id="cfde3-103">在 VM 上查看已設定且有效的網路安全性群組規則。</span><span class="sxs-lookup"><span data-stu-id="cfde3-103">View the configured and effective network security group rules applied on a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cfde3-104">句法</span><span class="sxs-lookup"><span data-stu-id="cfde3-104">SYNTAX</span></span>

### <span data-ttu-id="cfde3-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="cfde3-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cfde3-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="cfde3-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cfde3-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="cfde3-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -Location <String> -TargetVirtualMachineId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cfde3-108">說明</span><span class="sxs-lookup"><span data-stu-id="cfde3-108">DESCRIPTION</span></span>
<span data-ttu-id="cfde3-109">Get-AzureRmNetworkWatcherSecurityGroupView 可讓您在 VM 上查看已設定且有效的網路安全性群組規則。</span><span class="sxs-lookup"><span data-stu-id="cfde3-109">The Get-AzureRmNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="cfde3-110">示例</span><span class="sxs-lookup"><span data-stu-id="cfde3-110">EXAMPLES</span></span>

### <span data-ttu-id="cfde3-111">範例1：在 VM 上建立安全群組視圖呼叫</span><span class="sxs-lookup"><span data-stu-id="cfde3-111">Example 1: Make a Security Group View call on a VM</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="cfde3-112">在上述範例中，我們會先取得地區網路觀察程式，然後再取得區域中的 VM。</span><span class="sxs-lookup"><span data-stu-id="cfde3-112">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="cfde3-113">接著，我們會在指定的 VM 上進行安全性群組視圖通話。</span><span class="sxs-lookup"><span data-stu-id="cfde3-113">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="cfde3-114">參數</span><span class="sxs-lookup"><span data-stu-id="cfde3-114">PARAMETERS</span></span>

### <span data-ttu-id="cfde3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cfde3-115">-AsJob</span></span>
<span data-ttu-id="cfde3-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cfde3-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cfde3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfde3-117">-DefaultProfile</span></span>
<span data-ttu-id="cfde3-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cfde3-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cfde3-119">-位置</span><span class="sxs-lookup"><span data-stu-id="cfde3-119">-Location</span></span>
<span data-ttu-id="cfde3-120">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="cfde3-120">Location of the network watcher.</span></span>

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

### <span data-ttu-id="cfde3-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cfde3-121">-NetworkWatcher</span></span>
<span data-ttu-id="cfde3-122">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="cfde3-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="cfde3-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="cfde3-123">-NetworkWatcherName</span></span>
<span data-ttu-id="cfde3-124">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="cfde3-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="cfde3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfde3-125">-ResourceGroupName</span></span>
<span data-ttu-id="cfde3-126">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cfde3-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="cfde3-127">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="cfde3-127">-TargetVirtualMachineId</span></span>
<span data-ttu-id="cfde3-128">目標 VM 識別碼</span><span class="sxs-lookup"><span data-stu-id="cfde3-128">The target VM Id</span></span>

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

### <span data-ttu-id="cfde3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfde3-129">CommonParameters</span></span>
<span data-ttu-id="cfde3-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cfde3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfde3-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cfde3-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfde3-132">輸入</span><span class="sxs-lookup"><span data-stu-id="cfde3-132">INPUTS</span></span>

### <span data-ttu-id="cfde3-133">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="cfde3-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="cfde3-134">參數： NetworkWatcher (ByValue) </span><span class="sxs-lookup"><span data-stu-id="cfde3-134">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="cfde3-135">System.object</span><span class="sxs-lookup"><span data-stu-id="cfde3-135">System.String</span></span>
<span data-ttu-id="cfde3-136">參數： NetworkWatcherName (ByValue) </span><span class="sxs-lookup"><span data-stu-id="cfde3-136">Parameters: NetworkWatcherName (ByValue)</span></span>

## <span data-ttu-id="cfde3-137">輸出</span><span class="sxs-lookup"><span data-stu-id="cfde3-137">OUTPUTS</span></span>

### <span data-ttu-id="cfde3-138">PSSecurityGroupViewResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="cfde3-138">Microsoft.Azure.Commands.Network.Models.PSSecurityGroupViewResult</span></span>

## <span data-ttu-id="cfde3-139">筆記</span><span class="sxs-lookup"><span data-stu-id="cfde3-139">NOTES</span></span>
<span data-ttu-id="cfde3-140">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，流程，ip</span><span class="sxs-lookup"><span data-stu-id="cfde3-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="cfde3-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="cfde3-141">RELATED LINKS</span></span>

[<span data-ttu-id="cfde3-142">新-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cfde3-142">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="cfde3-143">AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cfde3-143">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="cfde3-144">移除-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cfde3-144">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="cfde3-145">AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="cfde3-145">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="cfde3-146">AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="cfde3-146">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="cfde3-147">AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="cfde3-147">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="cfde3-148">開始-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="cfde3-148">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="cfde3-149">新-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cfde3-149">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cfde3-150">新-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="cfde3-150">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="cfde3-151">AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cfde3-151">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cfde3-152">移除-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cfde3-152">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cfde3-153">停止 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cfde3-153">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cfde3-154">新-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="cfde3-154">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="cfde3-155">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="cfde3-155">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="cfde3-156">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="cfde3-156">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="cfde3-157">停止 AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cfde3-157">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cfde3-158">開始-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cfde3-158">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cfde3-159">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cfde3-159">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cfde3-160">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="cfde3-160">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="cfde3-161">移除-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cfde3-161">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cfde3-162">新-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cfde3-162">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cfde3-163">AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="cfde3-163">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="cfde3-164">AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="cfde3-164">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="cfde3-165">AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="cfde3-165">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="cfde3-166">AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="cfde3-166">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="cfde3-167">AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="cfde3-167">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="cfde3-168">AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cfde3-168">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
