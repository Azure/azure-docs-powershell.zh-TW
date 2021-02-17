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
ms.locfileid: "100404593"
---
# <span data-ttu-id="709b9-101">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="709b9-101">Get-AzNetworkWatcherTroubleshootingResult</span></span>

## <span data-ttu-id="709b9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="709b9-102">SYNOPSIS</span></span>
<span data-ttu-id="709b9-103">取得先前執行或目前執行疑難排解作業的疑難排解結果。</span><span class="sxs-lookup"><span data-stu-id="709b9-103">Gets the troubleshooting result from the previously run or currently running troubleshooting operation.</span></span>

## <span data-ttu-id="709b9-104">語法</span><span class="sxs-lookup"><span data-stu-id="709b9-104">SYNTAX</span></span>

### <span data-ttu-id="709b9-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="709b9-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="709b9-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="709b9-106">SetByName</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="709b9-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="709b9-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -Location <String> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="709b9-108">描述</span><span class="sxs-lookup"><span data-stu-id="709b9-108">DESCRIPTION</span></span>
<span data-ttu-id="709b9-109">此Get-AzNetworkWatcherTroubleshootingResult Cmdlet 會從先前執行或目前執行的任何作業取得疑Start-AzNetworkWatcherResourceTroubleshooting結果。</span><span class="sxs-lookup"><span data-stu-id="709b9-109">The Get-AzNetworkWatcherTroubleshootingResult cmdlet gets the troubleshooting result from the previously run or currently running Start-AzNetworkWatcherResourceTroubleshooting operation.</span></span> <span data-ttu-id="709b9-110">如果疑難排解作業正在進行中，則此作業可能需要幾分鐘才能完成。</span><span class="sxs-lookup"><span data-stu-id="709b9-110">If the troubleshooting operation is currently in progress, then this operation may take a few minutes to complete.</span></span> <span data-ttu-id="709b9-111">目前支援虛擬網路閘道和連接。</span><span class="sxs-lookup"><span data-stu-id="709b9-111">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="709b9-112">例子</span><span class="sxs-lookup"><span data-stu-id="709b9-112">EXAMPLES</span></span>

### <span data-ttu-id="709b9-113">範例 1：開始在虛擬網路閘道上進行疑難排解並取得結果</span><span class="sxs-lookup"><span data-stu-id="709b9-113">Example 1: Start Troubleshooting on a Virtual Network Gateway and Retrieve Result</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath

Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher $NW -TargetResourceId $target
```

<span data-ttu-id="709b9-114">上述範例會開始在虛擬網路閘道上進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="709b9-114">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="709b9-115">作業可能需要幾分鐘的時間才能完成。</span><span class="sxs-lookup"><span data-stu-id="709b9-115">The operation may take a few minutes to complete.</span></span>
<span data-ttu-id="709b9-116">疑難排解開始之後，Get-AzNetworkWatcherTroubleshootingResult資源撥打電話以取得此通話的結果。</span><span class="sxs-lookup"><span data-stu-id="709b9-116">After troubleshooting has started, a Get-AzNetworkWatcherTroubleshootingResult call is made to the resource to retrieve the result of this call.</span></span> 

## <span data-ttu-id="709b9-117">參數</span><span class="sxs-lookup"><span data-stu-id="709b9-117">PARAMETERS</span></span>

### <span data-ttu-id="709b9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="709b9-118">-DefaultProfile</span></span>
<span data-ttu-id="709b9-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="709b9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="709b9-120">-位置</span><span class="sxs-lookup"><span data-stu-id="709b9-120">-Location</span></span>
<span data-ttu-id="709b9-121">網路監視者的位置。</span><span class="sxs-lookup"><span data-stu-id="709b9-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="709b9-122">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="709b9-122">-NetworkWatcher</span></span>
<span data-ttu-id="709b9-123">網路監視程式資源。</span><span class="sxs-lookup"><span data-stu-id="709b9-123">The network watcher resource.</span></span>

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

### <span data-ttu-id="709b9-124">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="709b9-124">-NetworkWatcherName</span></span>
<span data-ttu-id="709b9-125">網路監視者的名稱。</span><span class="sxs-lookup"><span data-stu-id="709b9-125">The name of network watcher.</span></span>

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

### <span data-ttu-id="709b9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="709b9-126">-ResourceGroupName</span></span>
<span data-ttu-id="709b9-127">網路監視者資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="709b9-127">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="709b9-128">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="709b9-128">-TargetResourceId</span></span>
<span data-ttu-id="709b9-129">目標資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="709b9-129">The target resource ID.</span></span>

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

### <span data-ttu-id="709b9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="709b9-130">CommonParameters</span></span>
<span data-ttu-id="709b9-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="709b9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="709b9-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="709b9-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="709b9-133">輸入</span><span class="sxs-lookup"><span data-stu-id="709b9-133">INPUTS</span></span>

### <span data-ttu-id="709b9-134">Microsoft.Azure.Commands.Network.models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="709b9-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="709b9-135">System.String</span><span class="sxs-lookup"><span data-stu-id="709b9-135">System.String</span></span>

## <span data-ttu-id="709b9-136">輸出</span><span class="sxs-lookup"><span data-stu-id="709b9-136">OUTPUTS</span></span>

### <span data-ttu-id="709b9-137">Microsoft.Azure.Commands.Network.models.PSTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="709b9-137">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span></span>

## <span data-ttu-id="709b9-138">筆記</span><span class="sxs-lookup"><span data-stu-id="709b9-138">NOTES</span></span>
<span data-ttu-id="709b9-139">關鍵字：azure、azurerm、arm、資源、管理、管理員、網路監視程式、疑難排解、VPN、連接</span><span class="sxs-lookup"><span data-stu-id="709b9-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="709b9-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="709b9-140">RELATED LINKS</span></span>

[<span data-ttu-id="709b9-141">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="709b9-141">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="709b9-142">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="709b9-142">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="709b9-143">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="709b9-143">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="709b9-144">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="709b9-144">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="709b9-145">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="709b9-145">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="709b9-146">Get-AzNetworkWatcherTopwork</span><span class="sxs-lookup"><span data-stu-id="709b9-146">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="709b9-147">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="709b9-147">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="709b9-148">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="709b9-148">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="709b9-149">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="709b9-149">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="709b9-150">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="709b9-150">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="709b9-151">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="709b9-151">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="709b9-152">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="709b9-152">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="709b9-153">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="709b9-153">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="709b9-154">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="709b9-154">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="709b9-155">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="709b9-155">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="709b9-156">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="709b9-156">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="709b9-157">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="709b9-157">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="709b9-158">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="709b9-158">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="709b9-159">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="709b9-159">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="709b9-160">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="709b9-160">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="709b9-161">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="709b9-161">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="709b9-162">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="709b9-162">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="709b9-163">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="709b9-163">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="709b9-164">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="709b9-164">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="709b9-165">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="709b9-165">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="709b9-166">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="709b9-166">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="709b9-167">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="709b9-167">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
