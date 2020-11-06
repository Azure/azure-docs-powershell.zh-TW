---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchertroubleshootingresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
ms.openlocfilehash: 4f8fcbc0e5eee5aea92493b54acc631ffd144d3b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621952"
---
# <span data-ttu-id="603f1-101">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="603f1-101">Get-AzNetworkWatcherTroubleshootingResult</span></span>

## <span data-ttu-id="603f1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="603f1-102">SYNOPSIS</span></span>
<span data-ttu-id="603f1-103">從先前執行或目前正在執行的疑難排解作業中取得疑難排解結果。</span><span class="sxs-lookup"><span data-stu-id="603f1-103">Gets the troubleshooting result from the previously run or currently running troubleshooting operation.</span></span>

## <span data-ttu-id="603f1-104">句法</span><span class="sxs-lookup"><span data-stu-id="603f1-104">SYNTAX</span></span>

### <span data-ttu-id="603f1-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="603f1-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="603f1-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="603f1-106">SetByName</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="603f1-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="603f1-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -Location <String> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="603f1-108">說明</span><span class="sxs-lookup"><span data-stu-id="603f1-108">DESCRIPTION</span></span>
<span data-ttu-id="603f1-109">Get-AzNetworkWatcherTroubleshootingResult Cmdlet 會從先前執行或目前正在執行的 Start-AzNetworkWatcherResourceTroubleshooting 操作中取得疑難排解結果。</span><span class="sxs-lookup"><span data-stu-id="603f1-109">The Get-AzNetworkWatcherTroubleshootingResult cmdlet gets the troubleshooting result from the previously run or currently running Start-AzNetworkWatcherResourceTroubleshooting operation.</span></span> <span data-ttu-id="603f1-110">如果正在進行疑難排解作業，則可能需要幾分鐘的時間才能完成。</span><span class="sxs-lookup"><span data-stu-id="603f1-110">If the troubleshooting operation is currently in progress, then this operation may take a few minutes to complete.</span></span> <span data-ttu-id="603f1-111">目前支援虛擬網路閘道和連線。</span><span class="sxs-lookup"><span data-stu-id="603f1-111">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="603f1-112">示例</span><span class="sxs-lookup"><span data-stu-id="603f1-112">EXAMPLES</span></span>

### <span data-ttu-id="603f1-113">範例1：啟動虛擬網路閘道及取得結果的疑難排解</span><span class="sxs-lookup"><span data-stu-id="603f1-113">Example 1: Start Troubleshooting on a Virtual Network Gateway and Retrieve Result</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath

Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher $NW -TargetResourceId $target
```

<span data-ttu-id="603f1-114">上述範例會在虛擬網路閘道開始進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="603f1-114">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="603f1-115">作業可能需要幾分鐘的時間才能完成。</span><span class="sxs-lookup"><span data-stu-id="603f1-115">The operation may take a few minutes to complete.</span></span>
<span data-ttu-id="603f1-116">在疑難排解已開始之後，就會對資源進行 Get-AzNetworkWatcherTroubleshootingResult 呼叫，以取得此通話的結果。</span><span class="sxs-lookup"><span data-stu-id="603f1-116">After troubleshooting has started, a Get-AzNetworkWatcherTroubleshootingResult call is made to the resource to retrieve the result of this call.</span></span> 

## <span data-ttu-id="603f1-117">參數</span><span class="sxs-lookup"><span data-stu-id="603f1-117">PARAMETERS</span></span>

### <span data-ttu-id="603f1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="603f1-118">-DefaultProfile</span></span>
<span data-ttu-id="603f1-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="603f1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="603f1-120">-位置</span><span class="sxs-lookup"><span data-stu-id="603f1-120">-Location</span></span>
<span data-ttu-id="603f1-121">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="603f1-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="603f1-122">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="603f1-122">-NetworkWatcher</span></span>
<span data-ttu-id="603f1-123">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="603f1-123">The network watcher resource.</span></span>

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

### <span data-ttu-id="603f1-124">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="603f1-124">-NetworkWatcherName</span></span>
<span data-ttu-id="603f1-125">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="603f1-125">The name of network watcher.</span></span>

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

### <span data-ttu-id="603f1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="603f1-126">-ResourceGroupName</span></span>
<span data-ttu-id="603f1-127">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="603f1-127">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="603f1-128">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="603f1-128">-TargetResourceId</span></span>
<span data-ttu-id="603f1-129">目標資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="603f1-129">The target resource ID.</span></span>

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

### <span data-ttu-id="603f1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="603f1-130">CommonParameters</span></span>
<span data-ttu-id="603f1-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="603f1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="603f1-132">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="603f1-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="603f1-133">輸入</span><span class="sxs-lookup"><span data-stu-id="603f1-133">INPUTS</span></span>

### <span data-ttu-id="603f1-134">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="603f1-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="603f1-135">System.object</span><span class="sxs-lookup"><span data-stu-id="603f1-135">System.String</span></span>

## <span data-ttu-id="603f1-136">輸出</span><span class="sxs-lookup"><span data-stu-id="603f1-136">OUTPUTS</span></span>

### <span data-ttu-id="603f1-137">PSTroubleshootingResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="603f1-137">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span></span>

## <span data-ttu-id="603f1-138">筆記</span><span class="sxs-lookup"><span data-stu-id="603f1-138">NOTES</span></span>
<span data-ttu-id="603f1-139">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，疑難排解，VPN，連線</span><span class="sxs-lookup"><span data-stu-id="603f1-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="603f1-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="603f1-140">RELATED LINKS</span></span>

[<span data-ttu-id="603f1-141">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="603f1-141">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="603f1-142">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="603f1-142">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="603f1-143">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="603f1-143">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="603f1-144">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="603f1-144">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="603f1-145">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="603f1-145">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="603f1-146">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="603f1-146">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="603f1-147">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="603f1-147">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="603f1-148">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="603f1-148">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="603f1-149">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="603f1-149">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="603f1-150">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="603f1-150">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="603f1-151">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="603f1-151">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="603f1-152">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="603f1-152">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="603f1-153">新-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="603f1-153">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="603f1-154">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="603f1-154">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="603f1-155">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="603f1-155">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="603f1-156">停止 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="603f1-156">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="603f1-157">開始-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="603f1-157">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="603f1-158">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="603f1-158">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="603f1-159">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="603f1-159">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="603f1-160">移除-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="603f1-160">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="603f1-161">新-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="603f1-161">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="603f1-162">AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="603f1-162">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="603f1-163">AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="603f1-163">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="603f1-164">AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="603f1-164">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="603f1-165">AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="603f1-165">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="603f1-166">AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="603f1-166">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="603f1-167">AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="603f1-167">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
