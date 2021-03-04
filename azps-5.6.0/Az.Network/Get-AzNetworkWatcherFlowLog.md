---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: c6138ebe91f682eec8ce3c837829d60dc25f7911
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902525"
---
# <span data-ttu-id="93153-101">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="93153-101">Get-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="93153-102">簡介</span><span class="sxs-lookup"><span data-stu-id="93153-102">SYNOPSIS</span></span>
<span data-ttu-id="93153-103">在指定的訂閱和地區中，獲得流程記錄資源或流程記錄資源清單。</span><span class="sxs-lookup"><span data-stu-id="93153-103">Gets a flow log resource or a list of flow log resources in the specified subscription and region.</span></span>

## <span data-ttu-id="93153-104">語法</span><span class="sxs-lookup"><span data-stu-id="93153-104">SYNTAX</span></span>

### <span data-ttu-id="93153-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="93153-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93153-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="93153-106">SetByResource</span></span>
```
Get-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93153-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="93153-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherFlowLog -Location <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="93153-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="93153-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherFlowLog -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="93153-109">描述</span><span class="sxs-lookup"><span data-stu-id="93153-109">DESCRIPTION</span></span>
<span data-ttu-id="93153-110">在指定的訂閱和地區中，獲得流程記錄資源或流程記錄資源清單。</span><span class="sxs-lookup"><span data-stu-id="93153-110">Gets a flow log resource or a list of flow log resources in the specified subscription and region.</span></span>

## <span data-ttu-id="93153-111">例子</span><span class="sxs-lookup"><span data-stu-id="93153-111">EXAMPLES</span></span>

### <span data-ttu-id="93153-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="93153-112">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkWatcherFlowLog -Location eastus -Name pstest
```

<span data-ttu-id="93153-113">Name : pstest Id : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState : Succeeded Location : eastus TargetResourceId : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled : True RetentionPolicy : { "Days": 5, "Enabled": true } Format : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": true, "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb", "workspaceRegion": "eastus", "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr oups/flowlogsv2demo/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace", "trafficAnalyticsInterval": 60 }</span><span class="sxs-lookup"><span data-stu-id="93153-113">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled                    : True RetentionPolicy            : { "Days": 5, "Enabled": true } Format                     : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": true, "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb", "workspaceRegion": "eastus", "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr oups/flowlogsv2demo/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace", "trafficAnalyticsInterval": 60 }</span></span>

## <span data-ttu-id="93153-114">參數</span><span class="sxs-lookup"><span data-stu-id="93153-114">PARAMETERS</span></span>

### <span data-ttu-id="93153-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93153-115">-DefaultProfile</span></span>
<span data-ttu-id="93153-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="93153-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93153-117">-位置</span><span class="sxs-lookup"><span data-stu-id="93153-117">-Location</span></span>
<span data-ttu-id="93153-118">網路監視者的位置。</span><span class="sxs-lookup"><span data-stu-id="93153-118">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93153-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="93153-119">-Name</span></span>
<span data-ttu-id="93153-120">流程記錄名稱。</span><span class="sxs-lookup"><span data-stu-id="93153-120">The flow log name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: FlowLogName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93153-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="93153-121">-NetworkWatcher</span></span>
<span data-ttu-id="93153-122">網路監視程式資源。</span><span class="sxs-lookup"><span data-stu-id="93153-122">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93153-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="93153-123">-NetworkWatcherName</span></span>
<span data-ttu-id="93153-124">網路監視者的名稱。</span><span class="sxs-lookup"><span data-stu-id="93153-124">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93153-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93153-125">-ResourceGroupName</span></span>
<span data-ttu-id="93153-126">網路監視者資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="93153-126">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93153-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="93153-127">-ResourceId</span></span>
<span data-ttu-id="93153-128">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="93153-128">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93153-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93153-129">CommonParameters</span></span>
<span data-ttu-id="93153-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="93153-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93153-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="93153-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93153-132">輸入</span><span class="sxs-lookup"><span data-stu-id="93153-132">INPUTS</span></span>

### <span data-ttu-id="93153-133">Microsoft.Azure.Commands.Network.models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="93153-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="93153-134">System.String</span><span class="sxs-lookup"><span data-stu-id="93153-134">System.String</span></span>

## <span data-ttu-id="93153-135">輸出</span><span class="sxs-lookup"><span data-stu-id="93153-135">OUTPUTS</span></span>

### <span data-ttu-id="93153-136">Microsoft.Azure.Commands.Network.models.PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="93153-136">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="93153-137">筆記</span><span class="sxs-lookup"><span data-stu-id="93153-137">NOTES</span></span>

## <span data-ttu-id="93153-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="93153-138">RELATED LINKS</span></span>

[<span data-ttu-id="93153-139">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="93153-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="93153-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="93153-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="93153-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="93153-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="93153-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="93153-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="93153-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="93153-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="93153-144">Get-AzNetworkWatcherTopwork</span><span class="sxs-lookup"><span data-stu-id="93153-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="93153-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="93153-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="93153-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="93153-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="93153-147">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="93153-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="93153-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="93153-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="93153-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="93153-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="93153-150">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="93153-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="93153-151">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="93153-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="93153-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="93153-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="93153-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="93153-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="93153-154">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="93153-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="93153-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="93153-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="93153-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="93153-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="93153-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="93153-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="93153-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="93153-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="93153-159">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="93153-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="93153-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="93153-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="93153-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="93153-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="93153-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="93153-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="93153-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="93153-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="93153-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="93153-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="93153-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="93153-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

[<span data-ttu-id="93153-166">New-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="93153-166">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="93153-167">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="93153-167">Set-AzNetworkWatcherFlowLog</span></span>](./Set-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="93153-168">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="93153-168">Remove-AzNetworkWatcherFlowLog</span></span>](./Remove-AzNetworkWatcherFlowLog.md)
