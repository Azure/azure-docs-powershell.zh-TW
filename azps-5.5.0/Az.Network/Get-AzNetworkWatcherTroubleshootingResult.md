---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchertroubleshootingresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
ms.openlocfilehash: 871509fc03a7cb80735b6f011a7103350fd945ac
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100416119"
---
# <span data-ttu-id="7ea74-101">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="7ea74-101">Get-AzNetworkWatcherTroubleshootingResult</span></span>

## <span data-ttu-id="7ea74-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7ea74-102">SYNOPSIS</span></span>
<span data-ttu-id="7ea74-103">取得先前執行或目前執行疑難排解作業的疑難排解結果。</span><span class="sxs-lookup"><span data-stu-id="7ea74-103">Gets the troubleshooting result from the previously run or currently running troubleshooting operation.</span></span>

## <span data-ttu-id="7ea74-104">語法</span><span class="sxs-lookup"><span data-stu-id="7ea74-104">SYNTAX</span></span>

### <span data-ttu-id="7ea74-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="7ea74-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ea74-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="7ea74-106">SetByName</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ea74-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="7ea74-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -Location <String> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ea74-108">描述</span><span class="sxs-lookup"><span data-stu-id="7ea74-108">DESCRIPTION</span></span>
<span data-ttu-id="7ea74-109">此Get-AzNetworkWatcherTroubleshootingResult Cmdlet 會從先前執行或目前執行的任何作業取得疑Start-AzNetworkWatcherResourceTroubleshooting結果。</span><span class="sxs-lookup"><span data-stu-id="7ea74-109">The Get-AzNetworkWatcherTroubleshootingResult cmdlet gets the troubleshooting result from the previously run or currently running Start-AzNetworkWatcherResourceTroubleshooting operation.</span></span> <span data-ttu-id="7ea74-110">如果疑難排解作業正在進行中，則此作業可能需要幾分鐘才能完成。</span><span class="sxs-lookup"><span data-stu-id="7ea74-110">If the troubleshooting operation is currently in progress, then this operation may take a few minutes to complete.</span></span> <span data-ttu-id="7ea74-111">目前支援虛擬網路閘道和連接。</span><span class="sxs-lookup"><span data-stu-id="7ea74-111">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="7ea74-112">例子</span><span class="sxs-lookup"><span data-stu-id="7ea74-112">EXAMPLES</span></span>

### <span data-ttu-id="7ea74-113">範例 1：開始在虛擬網路閘道上進行疑難排解並取得結果</span><span class="sxs-lookup"><span data-stu-id="7ea74-113">Example 1: Start Troubleshooting on a Virtual Network Gateway and Retrieve Result</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath

Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher $NW -TargetResourceId $target
```

<span data-ttu-id="7ea74-114">上述範例會開始在虛擬網路閘道上進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="7ea74-114">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="7ea74-115">作業可能需要幾分鐘的時間才能完成。</span><span class="sxs-lookup"><span data-stu-id="7ea74-115">The operation may take a few minutes to complete.</span></span>
<span data-ttu-id="7ea74-116">疑難排解開始之後，Get-AzNetworkWatcherTroubleshootingResult資源撥打電話以取得此通話的結果。</span><span class="sxs-lookup"><span data-stu-id="7ea74-116">After troubleshooting has started, a Get-AzNetworkWatcherTroubleshootingResult call is made to the resource to retrieve the result of this call.</span></span> 

## <span data-ttu-id="7ea74-117">參數</span><span class="sxs-lookup"><span data-stu-id="7ea74-117">PARAMETERS</span></span>

### <span data-ttu-id="7ea74-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ea74-118">-DefaultProfile</span></span>
<span data-ttu-id="7ea74-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7ea74-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ea74-120">-位置</span><span class="sxs-lookup"><span data-stu-id="7ea74-120">-Location</span></span>
<span data-ttu-id="7ea74-121">網路監視者的位置。</span><span class="sxs-lookup"><span data-stu-id="7ea74-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="7ea74-122">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7ea74-122">-NetworkWatcher</span></span>
<span data-ttu-id="7ea74-123">網路監視程式資源。</span><span class="sxs-lookup"><span data-stu-id="7ea74-123">The network watcher resource.</span></span>

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

### <span data-ttu-id="7ea74-124">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="7ea74-124">-NetworkWatcherName</span></span>
<span data-ttu-id="7ea74-125">網路監視者的名稱。</span><span class="sxs-lookup"><span data-stu-id="7ea74-125">The name of network watcher.</span></span>

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

### <span data-ttu-id="7ea74-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ea74-126">-ResourceGroupName</span></span>
<span data-ttu-id="7ea74-127">網路監視者資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7ea74-127">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="7ea74-128">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="7ea74-128">-TargetResourceId</span></span>
<span data-ttu-id="7ea74-129">目標資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="7ea74-129">The target resource ID.</span></span>

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

### <span data-ttu-id="7ea74-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ea74-130">CommonParameters</span></span>
<span data-ttu-id="7ea74-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7ea74-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ea74-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7ea74-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ea74-133">輸入</span><span class="sxs-lookup"><span data-stu-id="7ea74-133">INPUTS</span></span>

### <span data-ttu-id="7ea74-134">Microsoft.Azure.Commands.Network.models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7ea74-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="7ea74-135">System.String</span><span class="sxs-lookup"><span data-stu-id="7ea74-135">System.String</span></span>

## <span data-ttu-id="7ea74-136">輸出</span><span class="sxs-lookup"><span data-stu-id="7ea74-136">OUTPUTS</span></span>

### <span data-ttu-id="7ea74-137">Microsoft.Azure.Commands.Network.models.PSTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="7ea74-137">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span></span>

## <span data-ttu-id="7ea74-138">筆記</span><span class="sxs-lookup"><span data-stu-id="7ea74-138">NOTES</span></span>
<span data-ttu-id="7ea74-139">關鍵字：azure、azurerm、arm、資源、管理、管理員、網路監視程式、疑難排解、VPN、連接</span><span class="sxs-lookup"><span data-stu-id="7ea74-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="7ea74-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="7ea74-140">RELATED LINKS</span></span>

[<span data-ttu-id="7ea74-141">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7ea74-141">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="7ea74-142">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7ea74-142">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="7ea74-143">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7ea74-143">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="7ea74-144">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="7ea74-144">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="7ea74-145">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="7ea74-145">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="7ea74-146">Get-AzNetworkWatcherTopwork</span><span class="sxs-lookup"><span data-stu-id="7ea74-146">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="7ea74-147">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="7ea74-147">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="7ea74-148">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7ea74-148">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7ea74-149">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="7ea74-149">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="7ea74-150">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7ea74-150">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7ea74-151">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7ea74-151">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7ea74-152">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7ea74-152">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7ea74-153">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ea74-153">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="7ea74-154">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="7ea74-154">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="7ea74-155">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="7ea74-155">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="7ea74-156">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7ea74-156">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7ea74-157">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7ea74-157">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7ea74-158">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7ea74-158">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7ea74-159">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="7ea74-159">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="7ea74-160">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7ea74-160">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7ea74-161">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7ea74-161">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7ea74-162">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="7ea74-162">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="7ea74-163">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="7ea74-163">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="7ea74-164">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="7ea74-164">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="7ea74-165">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="7ea74-165">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="7ea74-166">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="7ea74-166">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="7ea74-167">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7ea74-167">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
