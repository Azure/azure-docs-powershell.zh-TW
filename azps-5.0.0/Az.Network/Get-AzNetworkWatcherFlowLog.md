---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 5f4322ba81cdae5bdb0b33c2658a6d7934ed638d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137656"
---
# <span data-ttu-id="d443a-101">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="d443a-101">Get-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="d443a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d443a-102">SYNOPSIS</span></span>
<span data-ttu-id="d443a-103">取得指定訂閱和區域中的資料流程記錄資源或資料流程記錄資源清單。</span><span class="sxs-lookup"><span data-stu-id="d443a-103">Gets a flow log resource or a list of flow log resources in the specified subscription and region.</span></span>

## <span data-ttu-id="d443a-104">句法</span><span class="sxs-lookup"><span data-stu-id="d443a-104">SYNTAX</span></span>

### <span data-ttu-id="d443a-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="d443a-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d443a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d443a-106">SetByResource</span></span>
```
Get-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d443a-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="d443a-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherFlowLog -Location <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d443a-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d443a-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherFlowLog -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d443a-109">說明</span><span class="sxs-lookup"><span data-stu-id="d443a-109">DESCRIPTION</span></span>
<span data-ttu-id="d443a-110">取得指定訂閱和區域中的資料流程記錄資源或資料流程記錄資源清單。</span><span class="sxs-lookup"><span data-stu-id="d443a-110">Gets a flow log resource or a list of flow log resources in the specified subscription and region.</span></span>

## <span data-ttu-id="d443a-111">示例</span><span class="sxs-lookup"><span data-stu-id="d443a-111">EXAMPLES</span></span>

### <span data-ttu-id="d443a-112">範例1</span><span class="sxs-lookup"><span data-stu-id="d443a-112">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkWatcherFlowLog -Location eastus -Name pstest
```

<span data-ttu-id="d443a-113">Name （名稱）： pstest Id：/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/networkWatchers/NetworkWatcher_eastus//FlowLogs/pstest Etag： W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState：成功的位置： eastus TargetResourceId：/subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/microsoft. Network/networkSecurityGroups/MyNSG StorageId：/subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/： [Enabled "（天數）：5，" 已啟用]： True} 格式： {"Type"： "JSON"，"版本"： 2} FlowAnalyticsConfiguration： {"networkWatcherFlowAnalyticsConfiguration"： {[Enabled "： True，" workspaceId "：" bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb "，" workspaceRegion "：" eastus "，" workspaceResourceId "："/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr "，" oups "：" FlowLogsV2Demo OperationalInsights/MyWorkspace/提供者/"，" trafficAnalyticsInterval "： 60}</span><span class="sxs-lookup"><span data-stu-id="d443a-113">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled                    : True RetentionPolicy            : { "Days": 5, "Enabled": true } Format                     : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": true, "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb", "workspaceRegion": "eastus", "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr oups/flowlogsv2demo/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace", "trafficAnalyticsInterval": 60 }</span></span>

## <span data-ttu-id="d443a-114">參數</span><span class="sxs-lookup"><span data-stu-id="d443a-114">PARAMETERS</span></span>

### <span data-ttu-id="d443a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d443a-115">-DefaultProfile</span></span>
<span data-ttu-id="d443a-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d443a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d443a-117">-位置</span><span class="sxs-lookup"><span data-stu-id="d443a-117">-Location</span></span>
<span data-ttu-id="d443a-118">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="d443a-118">Location of the network watcher.</span></span>

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

### <span data-ttu-id="d443a-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="d443a-119">-Name</span></span>
<span data-ttu-id="d443a-120">流程記錄名稱。</span><span class="sxs-lookup"><span data-stu-id="d443a-120">The flow log name.</span></span>

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

### <span data-ttu-id="d443a-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d443a-121">-NetworkWatcher</span></span>
<span data-ttu-id="d443a-122">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="d443a-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="d443a-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d443a-123">-NetworkWatcherName</span></span>
<span data-ttu-id="d443a-124">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="d443a-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="d443a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d443a-125">-ResourceGroupName</span></span>
<span data-ttu-id="d443a-126">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d443a-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="d443a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d443a-127">-ResourceId</span></span>
<span data-ttu-id="d443a-128">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="d443a-128">Resource ID.</span></span>

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

### <span data-ttu-id="d443a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d443a-129">CommonParameters</span></span>
<span data-ttu-id="d443a-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d443a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d443a-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d443a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d443a-132">輸入</span><span class="sxs-lookup"><span data-stu-id="d443a-132">INPUTS</span></span>

### <span data-ttu-id="d443a-133">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d443a-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="d443a-134">System.object</span><span class="sxs-lookup"><span data-stu-id="d443a-134">System.String</span></span>

## <span data-ttu-id="d443a-135">輸出</span><span class="sxs-lookup"><span data-stu-id="d443a-135">OUTPUTS</span></span>

### <span data-ttu-id="d443a-136">PSFlowLogResource 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d443a-136">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="d443a-137">筆記</span><span class="sxs-lookup"><span data-stu-id="d443a-137">NOTES</span></span>

## <span data-ttu-id="d443a-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="d443a-138">RELATED LINKS</span></span>

[<span data-ttu-id="d443a-139">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d443a-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="d443a-140">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d443a-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="d443a-141">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d443a-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="d443a-142">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d443a-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="d443a-143">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d443a-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="d443a-144">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d443a-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="d443a-145">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d443a-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="d443a-146">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d443a-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d443a-147">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d443a-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="d443a-148">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d443a-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d443a-149">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d443a-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d443a-150">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d443a-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d443a-151">新-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="d443a-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="d443a-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d443a-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="d443a-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="d443a-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="d443a-154">停止 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d443a-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d443a-155">開始-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d443a-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d443a-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d443a-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d443a-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="d443a-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="d443a-158">移除-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d443a-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d443a-159">新-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d443a-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d443a-160">AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="d443a-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="d443a-161">AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="d443a-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="d443a-162">AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="d443a-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="d443a-163">AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="d443a-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="d443a-164">AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="d443a-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="d443a-165">AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d443a-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

[<span data-ttu-id="d443a-166">新-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="d443a-166">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="d443a-167">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="d443a-167">Set-AzNetworkWatcherFlowLog</span></span>](./Set-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="d443a-168">移除-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="d443a-168">Remove-AzNetworkWatcherFlowLog</span></span>](./Remove-AzNetworkWatcherFlowLog.md)
