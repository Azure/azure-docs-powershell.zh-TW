---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherflowlogstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
ms.openlocfilehash: dd88c40876bf3ceb5f90a7088f5943fcf5f18ce8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127025"
---
# <span data-ttu-id="07bc3-101">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="07bc3-101">Get-AzNetworkWatcherFlowLogStatus</span></span>

## <span data-ttu-id="07bc3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="07bc3-102">SYNOPSIS</span></span>
<span data-ttu-id="07bc3-103">取得資源的流程記錄狀態。</span><span class="sxs-lookup"><span data-stu-id="07bc3-103">Gets the status of flow logging on a resource.</span></span>

## <span data-ttu-id="07bc3-104">句法</span><span class="sxs-lookup"><span data-stu-id="07bc3-104">SYNTAX</span></span>

### <span data-ttu-id="07bc3-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="07bc3-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07bc3-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="07bc3-106">SetByName</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07bc3-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="07bc3-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -Location <String> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07bc3-108">說明</span><span class="sxs-lookup"><span data-stu-id="07bc3-108">DESCRIPTION</span></span>
<span data-ttu-id="07bc3-109">Get-AzNetworkWatcherFlowLogStatus Cmdlet 會取得資源的流程記錄狀態。</span><span class="sxs-lookup"><span data-stu-id="07bc3-109">The Get-AzNetworkWatcherFlowLogStatus cmdlet Gets the status of flow logging on a resource.</span></span> <span data-ttu-id="07bc3-110">狀態包括是否針對提供的資源、已設定的儲存空間帳戶來傳送記錄，以及記錄的保留原則，都已啟用流程記錄。</span><span class="sxs-lookup"><span data-stu-id="07bc3-110">The status includes whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="07bc3-111">目前支援資料流程記錄的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="07bc3-111">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="07bc3-112">示例</span><span class="sxs-lookup"><span data-stu-id="07bc3-112">EXAMPLES</span></span>

### <span data-ttu-id="07bc3-113">範例1：取得指定 NSG 的流程記錄狀態</span><span class="sxs-lookup"><span data-stu-id="07bc3-113">Example 1: Get the Flow Logging Status for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG

PS C:\> Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher $NW -TargetResourceId $nsg.Id

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
Properties       : {
                     "Enabled": true,
                     "RetentionPolicy": {
                       "Days": 0,
                       "Enabled": false
                     },
                     "StorageId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"
                     "Format"         : {
                       "Type ": "Json",
                       "Version": 1
                     }
                   }
```

<span data-ttu-id="07bc3-114">在這個範例中，我們會取得網路安全性群組的流程記錄狀態。</span><span class="sxs-lookup"><span data-stu-id="07bc3-114">In this example we get the flow logging status for a Network Security Group.</span></span> <span data-ttu-id="07bc3-115">指定的 NSG 已啟用流程記錄、預設格式，且未設定保留原則。</span><span class="sxs-lookup"><span data-stu-id="07bc3-115">The specified NSG has flow logging enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="07bc3-116">範例2：取得指定 NSG 的流程記錄和流量分析狀態</span><span class="sxs-lookup"><span data-stu-id="07bc3-116">Example 2: Get the Flow Logging and Traffic Analytics Status for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG

PS C:\> Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher $NW -TargetResourceId $nsg.Id

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
Format           : {
                     "Type ": "Json",
                     "Version": 1
                   }
FlowAnalyticsConfiguration : {
            "networkWatcherFlowAnalyticsConfiguration": {
              "enabled": true,
              "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb",
              "workspaceRegion": "WorkspaceLocation",
              "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegroups/WorkspaceRg/providers/microsoft.operationalinsights/workspaces/WorkspaceName",
              "TrafficAnalyticsInterval": 60
            }
          }
```

<span data-ttu-id="07bc3-117">在這個範例中，我們會取得網路安全性群組的流程記錄和流量分析狀態。</span><span class="sxs-lookup"><span data-stu-id="07bc3-117">In this example we get the flow logging and Traffic Analytics status for a Network Security Group.</span></span> <span data-ttu-id="07bc3-118">指定的 NSG 已啟用流程記錄和流量分析、預設格式及沒有設定保留原則。</span><span class="sxs-lookup"><span data-stu-id="07bc3-118">The specified NSG has flow logging and Traffic Analytics enabled, default format and no retention policy set.</span></span>

## <span data-ttu-id="07bc3-119">參數</span><span class="sxs-lookup"><span data-stu-id="07bc3-119">PARAMETERS</span></span>

### <span data-ttu-id="07bc3-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="07bc3-120">-AsJob</span></span>
<span data-ttu-id="07bc3-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="07bc3-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="07bc3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07bc3-122">-DefaultProfile</span></span>
<span data-ttu-id="07bc3-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="07bc3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07bc3-124">-位置</span><span class="sxs-lookup"><span data-stu-id="07bc3-124">-Location</span></span>
<span data-ttu-id="07bc3-125">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="07bc3-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="07bc3-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="07bc3-126">-NetworkWatcher</span></span>
<span data-ttu-id="07bc3-127">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="07bc3-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="07bc3-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="07bc3-128">-NetworkWatcherName</span></span>
<span data-ttu-id="07bc3-129">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="07bc3-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="07bc3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07bc3-130">-ResourceGroupName</span></span>
<span data-ttu-id="07bc3-131">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="07bc3-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="07bc3-132">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="07bc3-132">-TargetResourceId</span></span>
<span data-ttu-id="07bc3-133">目標資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="07bc3-133">The target resource ID.</span></span>

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

### <span data-ttu-id="07bc3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07bc3-134">CommonParameters</span></span>
<span data-ttu-id="07bc3-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="07bc3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07bc3-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="07bc3-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07bc3-137">輸入</span><span class="sxs-lookup"><span data-stu-id="07bc3-137">INPUTS</span></span>

### <span data-ttu-id="07bc3-138">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="07bc3-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="07bc3-139">System.object</span><span class="sxs-lookup"><span data-stu-id="07bc3-139">System.String</span></span>

## <span data-ttu-id="07bc3-140">輸出</span><span class="sxs-lookup"><span data-stu-id="07bc3-140">OUTPUTS</span></span>

### <span data-ttu-id="07bc3-141">PSFlowLog 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="07bc3-141">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="07bc3-142">筆記</span><span class="sxs-lookup"><span data-stu-id="07bc3-142">NOTES</span></span>
<span data-ttu-id="07bc3-143">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，觀察程式，流程，記錄，flowlog，記錄</span><span class="sxs-lookup"><span data-stu-id="07bc3-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="07bc3-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="07bc3-144">RELATED LINKS</span></span>

[<span data-ttu-id="07bc3-145">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="07bc3-145">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="07bc3-146">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="07bc3-146">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="07bc3-147">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="07bc3-147">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="07bc3-148">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="07bc3-148">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="07bc3-149">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="07bc3-149">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="07bc3-150">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="07bc3-150">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="07bc3-151">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="07bc3-151">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="07bc3-152">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="07bc3-152">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="07bc3-153">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="07bc3-153">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="07bc3-154">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="07bc3-154">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="07bc3-155">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="07bc3-155">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="07bc3-156">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="07bc3-156">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="07bc3-157">新-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="07bc3-157">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="07bc3-158">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="07bc3-158">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="07bc3-159">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="07bc3-159">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="07bc3-160">停止 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="07bc3-160">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="07bc3-161">開始-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="07bc3-161">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="07bc3-162">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="07bc3-162">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="07bc3-163">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="07bc3-163">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="07bc3-164">移除-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="07bc3-164">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="07bc3-165">新-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="07bc3-165">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="07bc3-166">AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="07bc3-166">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="07bc3-167">AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="07bc3-167">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="07bc3-168">AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="07bc3-168">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="07bc3-169">AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="07bc3-169">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="07bc3-170">AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="07bc3-170">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="07bc3-171">AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="07bc3-171">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)