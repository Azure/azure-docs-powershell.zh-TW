---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-aznetworkwatcherresourcetroubleshooting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
ms.openlocfilehash: 0776b10a14236ac4806ccc166f24b1dd5a3ee3de
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98277416"
---
# <span data-ttu-id="f124f-101">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="f124f-101">Start-AzNetworkWatcherResourceTroubleshooting</span></span>

## <span data-ttu-id="f124f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f124f-102">SYNOPSIS</span></span>
<span data-ttu-id="f124f-103">開始針對 Azure 中的網路資源進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="f124f-103">Starts troubleshooting on a Networking resource in Azure.</span></span>

## <span data-ttu-id="f124f-104">句法</span><span class="sxs-lookup"><span data-stu-id="f124f-104">SYNTAX</span></span>

### <span data-ttu-id="f124f-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="f124f-105">SetByResource (Default)</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -StorageId <String> -StoragePath <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f124f-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="f124f-106">SetByName</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f124f-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="f124f-107">SetByLocation</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -Location <String> -TargetResourceId <String> -StorageId <String>
 -StoragePath <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f124f-108">說明</span><span class="sxs-lookup"><span data-stu-id="f124f-108">DESCRIPTION</span></span>
<span data-ttu-id="f124f-109">Start-AzNetworkWatcherResourceTroubleshooting Cmdlet 會針對 Azure 中的網路資源開始疑難排解，並傳回潛在問題與緩解措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f124f-109">The Start-AzNetworkWatcherResourceTroubleshooting cmdlet starts troubleshooting for a Networking resource in Azure and returns information about potential issues and mitigations.</span></span> <span data-ttu-id="f124f-110">目前支援虛擬網路閘道和連線。</span><span class="sxs-lookup"><span data-stu-id="f124f-110">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="f124f-111">示例</span><span class="sxs-lookup"><span data-stu-id="f124f-111">EXAMPLES</span></span>

### <span data-ttu-id="f124f-112">範例1：啟動虛擬網路閘道的疑難排解</span><span class="sxs-lookup"><span data-stu-id="f124f-112">Example 1: Start Troubleshooting on a Virtual Network Gateway</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath
```

<span data-ttu-id="f124f-113">上述範例會在虛擬網路閘道開始進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="f124f-113">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="f124f-114">作業可能需要幾分鐘的時間才能完成。</span><span class="sxs-lookup"><span data-stu-id="f124f-114">The operation may take a few minutes to complete.</span></span>

## <span data-ttu-id="f124f-115">參數</span><span class="sxs-lookup"><span data-stu-id="f124f-115">PARAMETERS</span></span>

### <span data-ttu-id="f124f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f124f-116">-DefaultProfile</span></span>
<span data-ttu-id="f124f-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f124f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f124f-118">-位置</span><span class="sxs-lookup"><span data-stu-id="f124f-118">-Location</span></span>
<span data-ttu-id="f124f-119">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="f124f-119">Location of the network watcher.</span></span>

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

### <span data-ttu-id="f124f-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f124f-120">-NetworkWatcher</span></span>
<span data-ttu-id="f124f-121">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="f124f-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="f124f-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="f124f-122">-NetworkWatcherName</span></span>
<span data-ttu-id="f124f-123">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="f124f-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="f124f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f124f-124">-ResourceGroupName</span></span>
<span data-ttu-id="f124f-125">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f124f-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="f124f-126">-StorageId</span><span class="sxs-lookup"><span data-stu-id="f124f-126">-StorageId</span></span>
<span data-ttu-id="f124f-127">[儲存空間識別碼]。</span><span class="sxs-lookup"><span data-stu-id="f124f-127">The storage ID.</span></span>

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

### <span data-ttu-id="f124f-128">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="f124f-128">-StoragePath</span></span>
<span data-ttu-id="f124f-129">儲存路徑。</span><span class="sxs-lookup"><span data-stu-id="f124f-129">The storage path.</span></span>

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

### <span data-ttu-id="f124f-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="f124f-130">-TargetResourceId</span></span>
<span data-ttu-id="f124f-131">指定要進行疑難排解之資源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f124f-131">Specifies the resource id of the resource to troubleshoot.</span></span> <span data-ttu-id="f124f-132">範例格式： "/subscriptions/$ {subscriptionId}/resourceGroups/$ {resourceGroupName}/providers/Microsoft.Network/connections/$ {connectionName}"</span><span class="sxs-lookup"><span data-stu-id="f124f-132">Example format: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span></span>

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

### <span data-ttu-id="f124f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f124f-133">CommonParameters</span></span>
<span data-ttu-id="f124f-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f124f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f124f-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f124f-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f124f-136">輸入</span><span class="sxs-lookup"><span data-stu-id="f124f-136">INPUTS</span></span>

### <span data-ttu-id="f124f-137">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f124f-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="f124f-138">System.object</span><span class="sxs-lookup"><span data-stu-id="f124f-138">System.String</span></span>

## <span data-ttu-id="f124f-139">輸出</span><span class="sxs-lookup"><span data-stu-id="f124f-139">OUTPUTS</span></span>

### <span data-ttu-id="f124f-140">PSTroubleshootingResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f124f-140">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span></span>

## <span data-ttu-id="f124f-141">筆記</span><span class="sxs-lookup"><span data-stu-id="f124f-141">NOTES</span></span>
<span data-ttu-id="f124f-142">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，疑難排解，VPN，連線</span><span class="sxs-lookup"><span data-stu-id="f124f-142">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="f124f-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="f124f-143">RELATED LINKS</span></span>

[<span data-ttu-id="f124f-144">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f124f-144">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="f124f-145">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f124f-145">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="f124f-146">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f124f-146">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="f124f-147">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="f124f-147">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="f124f-148">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="f124f-148">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="f124f-149">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="f124f-149">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="f124f-150">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="f124f-150">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="f124f-151">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f124f-151">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f124f-152">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="f124f-152">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="f124f-153">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f124f-153">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f124f-154">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f124f-154">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f124f-155">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f124f-155">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f124f-156">新-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="f124f-156">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="f124f-157">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="f124f-157">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="f124f-158">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="f124f-158">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="f124f-159">停止 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f124f-159">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f124f-160">開始-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f124f-160">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f124f-161">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f124f-161">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f124f-162">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="f124f-162">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="f124f-163">移除-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f124f-163">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f124f-164">新-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f124f-164">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f124f-165">AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="f124f-165">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="f124f-166">AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="f124f-166">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="f124f-167">AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="f124f-167">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="f124f-168">AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="f124f-168">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="f124f-169">AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="f124f-169">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="f124f-170">AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f124f-170">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
