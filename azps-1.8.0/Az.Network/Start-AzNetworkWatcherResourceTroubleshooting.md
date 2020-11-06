---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-aznetworkwatcherresourcetroubleshooting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
ms.openlocfilehash: 5399c97f076f1402b20b91798d2db215d00af8b3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621388"
---
# <span data-ttu-id="d996a-101">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d996a-101">Start-AzNetworkWatcherResourceTroubleshooting</span></span>

## <span data-ttu-id="d996a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d996a-102">SYNOPSIS</span></span>
<span data-ttu-id="d996a-103">開始針對 Azure 中的網路資源進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="d996a-103">Starts troubleshooting on a Networking resource in Azure.</span></span>

## <span data-ttu-id="d996a-104">句法</span><span class="sxs-lookup"><span data-stu-id="d996a-104">SYNTAX</span></span>

### <span data-ttu-id="d996a-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="d996a-105">SetByResource (Default)</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -StorageId <String> -StoragePath <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d996a-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="d996a-106">SetByName</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d996a-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="d996a-107">SetByLocation</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -Location <String> -TargetResourceId <String> -StorageId <String>
 -StoragePath <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d996a-108">說明</span><span class="sxs-lookup"><span data-stu-id="d996a-108">DESCRIPTION</span></span>
<span data-ttu-id="d996a-109">Start-AzNetworkWatcherResourceTroubleshooting Cmdlet 會針對 Azure 中的網路資源開始疑難排解，並傳回潛在問題與緩解措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d996a-109">The Start-AzNetworkWatcherResourceTroubleshooting cmdlet starts troubleshooting for a Networking resource in Azure and returns information about potential issues and mitigations.</span></span> <span data-ttu-id="d996a-110">目前支援虛擬網路閘道和連線。</span><span class="sxs-lookup"><span data-stu-id="d996a-110">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="d996a-111">示例</span><span class="sxs-lookup"><span data-stu-id="d996a-111">EXAMPLES</span></span>

### <span data-ttu-id="d996a-112">範例1：啟動虛擬網路閘道的疑難排解</span><span class="sxs-lookup"><span data-stu-id="d996a-112">Example 1: Start Troubleshooting on a Virtual Network Gateway</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath
```

<span data-ttu-id="d996a-113">上述範例會在虛擬網路閘道開始進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="d996a-113">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="d996a-114">作業可能需要幾分鐘的時間才能完成。</span><span class="sxs-lookup"><span data-stu-id="d996a-114">The operation may take a few minutes to complete.</span></span>

## <span data-ttu-id="d996a-115">參數</span><span class="sxs-lookup"><span data-stu-id="d996a-115">PARAMETERS</span></span>

### <span data-ttu-id="d996a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d996a-116">-DefaultProfile</span></span>
<span data-ttu-id="d996a-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d996a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d996a-118">-位置</span><span class="sxs-lookup"><span data-stu-id="d996a-118">-Location</span></span>
<span data-ttu-id="d996a-119">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="d996a-119">Location of the network watcher.</span></span>

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

### <span data-ttu-id="d996a-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d996a-120">-NetworkWatcher</span></span>
<span data-ttu-id="d996a-121">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="d996a-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="d996a-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d996a-122">-NetworkWatcherName</span></span>
<span data-ttu-id="d996a-123">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="d996a-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="d996a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d996a-124">-ResourceGroupName</span></span>
<span data-ttu-id="d996a-125">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d996a-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="d996a-126">-StorageId</span><span class="sxs-lookup"><span data-stu-id="d996a-126">-StorageId</span></span>
<span data-ttu-id="d996a-127">[儲存空間識別碼]。</span><span class="sxs-lookup"><span data-stu-id="d996a-127">The storage ID.</span></span>

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

### <span data-ttu-id="d996a-128">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="d996a-128">-StoragePath</span></span>
<span data-ttu-id="d996a-129">儲存路徑。</span><span class="sxs-lookup"><span data-stu-id="d996a-129">The storage path.</span></span>

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

### <span data-ttu-id="d996a-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="d996a-130">-TargetResourceId</span></span>
<span data-ttu-id="d996a-131">指定要進行疑難排解之資源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d996a-131">Specifies the resource id of the resource to troubleshoot.</span></span> <span data-ttu-id="d996a-132">範例格式： "/subscriptions/$ {subscriptionId}/resourceGroups/$ {resourceGroupName}/providers/Microsoft.Network/connections/$ {connectionName}"</span><span class="sxs-lookup"><span data-stu-id="d996a-132">Example format: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span></span>

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

### <span data-ttu-id="d996a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d996a-133">CommonParameters</span></span>
<span data-ttu-id="d996a-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d996a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d996a-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d996a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d996a-136">輸入</span><span class="sxs-lookup"><span data-stu-id="d996a-136">INPUTS</span></span>

### <span data-ttu-id="d996a-137">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d996a-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="d996a-138">System.object</span><span class="sxs-lookup"><span data-stu-id="d996a-138">System.String</span></span>

## <span data-ttu-id="d996a-139">輸出</span><span class="sxs-lookup"><span data-stu-id="d996a-139">OUTPUTS</span></span>

### <span data-ttu-id="d996a-140">PSTroubleshootingResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d996a-140">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span></span>

## <span data-ttu-id="d996a-141">筆記</span><span class="sxs-lookup"><span data-stu-id="d996a-141">NOTES</span></span>
<span data-ttu-id="d996a-142">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，疑難排解，VPN，連線</span><span class="sxs-lookup"><span data-stu-id="d996a-142">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="d996a-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="d996a-143">RELATED LINKS</span></span>

[<span data-ttu-id="d996a-144">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d996a-144">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="d996a-145">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d996a-145">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="d996a-146">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d996a-146">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="d996a-147">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d996a-147">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="d996a-148">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d996a-148">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="d996a-149">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d996a-149">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="d996a-150">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d996a-150">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="d996a-151">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d996a-151">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d996a-152">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d996a-152">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="d996a-153">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d996a-153">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d996a-154">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d996a-154">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d996a-155">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d996a-155">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d996a-156">新-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="d996a-156">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="d996a-157">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d996a-157">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="d996a-158">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="d996a-158">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="d996a-159">停止 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d996a-159">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d996a-160">開始-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d996a-160">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d996a-161">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d996a-161">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d996a-162">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="d996a-162">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="d996a-163">移除-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d996a-163">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d996a-164">新-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d996a-164">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d996a-165">AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="d996a-165">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="d996a-166">AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="d996a-166">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="d996a-167">AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="d996a-167">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="d996a-168">AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="d996a-168">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="d996a-169">AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="d996a-169">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="d996a-170">AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d996a-170">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)