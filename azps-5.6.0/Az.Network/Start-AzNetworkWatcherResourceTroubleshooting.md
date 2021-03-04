---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/start-aznetworkwatcherresourcetroubleshooting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
ms.openlocfilehash: 4886277bb994e0fe3a33645916660658a8367f1d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901921"
---
# <span data-ttu-id="7ce35-101">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="7ce35-101">Start-AzNetworkWatcherResourceTroubleshooting</span></span>

## <span data-ttu-id="7ce35-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7ce35-102">SYNOPSIS</span></span>
<span data-ttu-id="7ce35-103">開始在 Azure 中針對網路資源進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="7ce35-103">Starts troubleshooting on a Networking resource in Azure.</span></span>

## <span data-ttu-id="7ce35-104">語法</span><span class="sxs-lookup"><span data-stu-id="7ce35-104">SYNTAX</span></span>

### <span data-ttu-id="7ce35-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="7ce35-105">SetByResource (Default)</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -StorageId <String> -StoragePath <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ce35-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="7ce35-106">SetByName</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ce35-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="7ce35-107">SetByLocation</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -Location <String> -TargetResourceId <String> -StorageId <String>
 -StoragePath <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ce35-108">描述</span><span class="sxs-lookup"><span data-stu-id="7ce35-108">DESCRIPTION</span></span>
<span data-ttu-id="7ce35-109">Cmdlet Start-AzNetworkWatcherResourceTroubleshooting Azure 中的網路資源開始進行疑難排解，並返回潛在問題和減輕風險的資訊。</span><span class="sxs-lookup"><span data-stu-id="7ce35-109">The Start-AzNetworkWatcherResourceTroubleshooting cmdlet starts troubleshooting for a Networking resource in Azure and returns information about potential issues and mitigations.</span></span> <span data-ttu-id="7ce35-110">目前支援虛擬網路閘道和連接。</span><span class="sxs-lookup"><span data-stu-id="7ce35-110">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="7ce35-111">例子</span><span class="sxs-lookup"><span data-stu-id="7ce35-111">EXAMPLES</span></span>

### <span data-ttu-id="7ce35-112">範例 1：開始在虛擬網路閘道上進行疑難排解</span><span class="sxs-lookup"><span data-stu-id="7ce35-112">Example 1: Start Troubleshooting on a Virtual Network Gateway</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath
```

<span data-ttu-id="7ce35-113">上述範例會開始在虛擬網路閘道上進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="7ce35-113">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="7ce35-114">作業可能需要幾分鐘的時間才能完成。</span><span class="sxs-lookup"><span data-stu-id="7ce35-114">The operation may take a few minutes to complete.</span></span>

## <span data-ttu-id="7ce35-115">參數</span><span class="sxs-lookup"><span data-stu-id="7ce35-115">PARAMETERS</span></span>

### <span data-ttu-id="7ce35-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ce35-116">-DefaultProfile</span></span>
<span data-ttu-id="7ce35-117">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7ce35-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ce35-118">-位置</span><span class="sxs-lookup"><span data-stu-id="7ce35-118">-Location</span></span>
<span data-ttu-id="7ce35-119">網路監視者的位置。</span><span class="sxs-lookup"><span data-stu-id="7ce35-119">Location of the network watcher.</span></span>

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

### <span data-ttu-id="7ce35-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7ce35-120">-NetworkWatcher</span></span>
<span data-ttu-id="7ce35-121">網路監視程式資源。</span><span class="sxs-lookup"><span data-stu-id="7ce35-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="7ce35-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="7ce35-122">-NetworkWatcherName</span></span>
<span data-ttu-id="7ce35-123">網路監視者的名稱。</span><span class="sxs-lookup"><span data-stu-id="7ce35-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="7ce35-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ce35-124">-ResourceGroupName</span></span>
<span data-ttu-id="7ce35-125">網路監視者資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7ce35-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="7ce35-126">-StorageId</span><span class="sxs-lookup"><span data-stu-id="7ce35-126">-StorageId</span></span>
<span data-ttu-id="7ce35-127">儲存識別碼。</span><span class="sxs-lookup"><span data-stu-id="7ce35-127">The storage ID.</span></span>

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

### <span data-ttu-id="7ce35-128">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="7ce35-128">-StoragePath</span></span>
<span data-ttu-id="7ce35-129">儲存路徑。</span><span class="sxs-lookup"><span data-stu-id="7ce35-129">The storage path.</span></span>

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

### <span data-ttu-id="7ce35-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="7ce35-130">-TargetResourceId</span></span>
<span data-ttu-id="7ce35-131">指定要疑難排解之資源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="7ce35-131">Specifies the resource id of the resource to troubleshoot.</span></span> <span data-ttu-id="7ce35-132">範例格式：「/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span><span class="sxs-lookup"><span data-stu-id="7ce35-132">Example format: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span></span>

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

### <span data-ttu-id="7ce35-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ce35-133">CommonParameters</span></span>
<span data-ttu-id="7ce35-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7ce35-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ce35-135">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="7ce35-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ce35-136">輸入</span><span class="sxs-lookup"><span data-stu-id="7ce35-136">INPUTS</span></span>

### <span data-ttu-id="7ce35-137">Microsoft.Azure.Commands.Network.models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7ce35-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="7ce35-138">System.String</span><span class="sxs-lookup"><span data-stu-id="7ce35-138">System.String</span></span>

## <span data-ttu-id="7ce35-139">輸出</span><span class="sxs-lookup"><span data-stu-id="7ce35-139">OUTPUTS</span></span>

### <span data-ttu-id="7ce35-140">Microsoft.Azure.Commands.Network.models.PSTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="7ce35-140">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span></span>

## <span data-ttu-id="7ce35-141">筆記</span><span class="sxs-lookup"><span data-stu-id="7ce35-141">NOTES</span></span>
<span data-ttu-id="7ce35-142">關鍵字：azure、azurerm、arm、資源、管理、管理員、網路監視程式、疑難排解、VPN、連接</span><span class="sxs-lookup"><span data-stu-id="7ce35-142">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="7ce35-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="7ce35-143">RELATED LINKS</span></span>

[<span data-ttu-id="7ce35-144">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7ce35-144">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="7ce35-145">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7ce35-145">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="7ce35-146">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7ce35-146">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="7ce35-147">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="7ce35-147">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="7ce35-148">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="7ce35-148">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="7ce35-149">Get-AzNetworkWatcherTopwork</span><span class="sxs-lookup"><span data-stu-id="7ce35-149">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="7ce35-150">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="7ce35-150">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="7ce35-151">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7ce35-151">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7ce35-152">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="7ce35-152">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="7ce35-153">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7ce35-153">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7ce35-154">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7ce35-154">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7ce35-155">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7ce35-155">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7ce35-156">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ce35-156">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="7ce35-157">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="7ce35-157">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="7ce35-158">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="7ce35-158">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="7ce35-159">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7ce35-159">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7ce35-160">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7ce35-160">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7ce35-161">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7ce35-161">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7ce35-162">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="7ce35-162">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="7ce35-163">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7ce35-163">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7ce35-164">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7ce35-164">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7ce35-165">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="7ce35-165">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="7ce35-166">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="7ce35-166">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="7ce35-167">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="7ce35-167">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="7ce35-168">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="7ce35-168">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="7ce35-169">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="7ce35-169">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="7ce35-170">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7ce35-170">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
