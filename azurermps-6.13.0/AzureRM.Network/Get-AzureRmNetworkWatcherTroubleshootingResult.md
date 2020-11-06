---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchertroubleshootingresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherTroubleshootingResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherTroubleshootingResult.md
ms.openlocfilehash: 527d0fd33629ed7e1fcecdd23ba7cf8c93822f16
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455196"
---
# <span data-ttu-id="e5822-101">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="e5822-101">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>

## <span data-ttu-id="e5822-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e5822-102">SYNOPSIS</span></span>
<span data-ttu-id="e5822-103">從先前執行或目前正在執行的疑難排解作業中取得疑難排解結果。</span><span class="sxs-lookup"><span data-stu-id="e5822-103">Gets the troubleshooting result from the previously run or currently running troubleshooting operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5822-104">句法</span><span class="sxs-lookup"><span data-stu-id="e5822-104">SYNTAX</span></span>

### <span data-ttu-id="e5822-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="e5822-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherTroubleshootingResult -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5822-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="e5822-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherTroubleshootingResult -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5822-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="e5822-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherTroubleshootingResult -Location <String> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5822-108">說明</span><span class="sxs-lookup"><span data-stu-id="e5822-108">DESCRIPTION</span></span>
<span data-ttu-id="e5822-109">Get-AzureRmNetworkWatcherTroubleshootingResult Cmdlet 會從先前執行或目前正在執行的 Start-AzureRmNetworkWatcherResourceTroubleshooting 操作中取得疑難排解結果。</span><span class="sxs-lookup"><span data-stu-id="e5822-109">The Get-AzureRmNetworkWatcherTroubleshootingResult cmdlet gets the troubleshooting result from the previously run or currently running Start-AzureRmNetworkWatcherResourceTroubleshooting operation.</span></span> <span data-ttu-id="e5822-110">如果正在進行疑難排解作業，則可能需要幾分鐘的時間才能完成。</span><span class="sxs-lookup"><span data-stu-id="e5822-110">If the troubleshooting operation is currently in progress, then this operation may take a few minutes to complete.</span></span> <span data-ttu-id="e5822-111">目前支援虛擬網路閘道和連線。</span><span class="sxs-lookup"><span data-stu-id="e5822-111">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="e5822-112">示例</span><span class="sxs-lookup"><span data-stu-id="e5822-112">EXAMPLES</span></span>

### <span data-ttu-id="e5822-113">範例1：啟動虛擬網路閘道及取得結果的疑難排解</span><span class="sxs-lookup"><span data-stu-id="e5822-113">Example 1: Start Troubleshooting on a Virtual Network Gateway and Retrieve Result</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath

Get-AzureRmNetworkWatcherTroubleshootingResult -NetworkWatcher $NW -TargetResourceId $target
```

<span data-ttu-id="e5822-114">上述範例會在虛擬網路閘道開始進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="e5822-114">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="e5822-115">作業可能需要幾分鐘的時間才能完成。</span><span class="sxs-lookup"><span data-stu-id="e5822-115">The operation may take a few minutes to complete.</span></span>
<span data-ttu-id="e5822-116">在疑難排解已開始之後，就會對資源進行 Get-AzureRmNetworkWatcherTroubleshootingResult 呼叫，以取得此通話的結果。</span><span class="sxs-lookup"><span data-stu-id="e5822-116">After troubleshooting has started, a Get-AzureRmNetworkWatcherTroubleshootingResult call is made to the resource to retrieve the result of this call.</span></span> 

## <span data-ttu-id="e5822-117">參數</span><span class="sxs-lookup"><span data-stu-id="e5822-117">PARAMETERS</span></span>

### <span data-ttu-id="e5822-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5822-118">-DefaultProfile</span></span>
<span data-ttu-id="e5822-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e5822-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5822-120">-位置</span><span class="sxs-lookup"><span data-stu-id="e5822-120">-Location</span></span>
<span data-ttu-id="e5822-121">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="e5822-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="e5822-122">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e5822-122">-NetworkWatcher</span></span>
<span data-ttu-id="e5822-123">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="e5822-123">The network watcher resource.</span></span>

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

### <span data-ttu-id="e5822-124">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="e5822-124">-NetworkWatcherName</span></span>
<span data-ttu-id="e5822-125">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5822-125">The name of network watcher.</span></span>

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

### <span data-ttu-id="e5822-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5822-126">-ResourceGroupName</span></span>
<span data-ttu-id="e5822-127">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5822-127">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="e5822-128">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="e5822-128">-TargetResourceId</span></span>
<span data-ttu-id="e5822-129">目標資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e5822-129">The target resource ID.</span></span>

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

### <span data-ttu-id="e5822-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5822-130">CommonParameters</span></span>
<span data-ttu-id="e5822-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e5822-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5822-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e5822-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5822-133">輸入</span><span class="sxs-lookup"><span data-stu-id="e5822-133">INPUTS</span></span>

### <span data-ttu-id="e5822-134">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e5822-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="e5822-135">參數： NetworkWatcher (ByValue) </span><span class="sxs-lookup"><span data-stu-id="e5822-135">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="e5822-136">System.object</span><span class="sxs-lookup"><span data-stu-id="e5822-136">System.String</span></span>
<span data-ttu-id="e5822-137">參數： NetworkWatcherName (ByValue) </span><span class="sxs-lookup"><span data-stu-id="e5822-137">Parameters: NetworkWatcherName (ByValue)</span></span>

## <span data-ttu-id="e5822-138">輸出</span><span class="sxs-lookup"><span data-stu-id="e5822-138">OUTPUTS</span></span>

### <span data-ttu-id="e5822-139">PSTroubleshootingResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e5822-139">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span></span>

## <span data-ttu-id="e5822-140">筆記</span><span class="sxs-lookup"><span data-stu-id="e5822-140">NOTES</span></span>
<span data-ttu-id="e5822-141">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，疑難排解，VPN，連線</span><span class="sxs-lookup"><span data-stu-id="e5822-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="e5822-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="e5822-142">RELATED LINKS</span></span>

[<span data-ttu-id="e5822-143">新-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e5822-143">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="e5822-144">AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e5822-144">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="e5822-145">移除-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e5822-145">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="e5822-146">AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="e5822-146">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="e5822-147">AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="e5822-147">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="e5822-148">AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="e5822-148">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="e5822-149">開始-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="e5822-149">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="e5822-150">新-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e5822-150">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e5822-151">新-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="e5822-151">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="e5822-152">AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e5822-152">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e5822-153">移除-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e5822-153">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e5822-154">停止 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e5822-154">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e5822-155">新-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5822-155">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="e5822-156">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="e5822-156">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="e5822-157">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="e5822-157">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="e5822-158">停止 AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e5822-158">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e5822-159">開始-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e5822-159">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e5822-160">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e5822-160">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e5822-161">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="e5822-161">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="e5822-162">移除-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e5822-162">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e5822-163">新-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e5822-163">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e5822-164">AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="e5822-164">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="e5822-165">AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="e5822-165">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="e5822-166">AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="e5822-166">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="e5822-167">AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="e5822-167">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="e5822-168">AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="e5822-168">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="e5822-169">AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e5822-169">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
