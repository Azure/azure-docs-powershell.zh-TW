---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkwatcherflowlogstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
ms.openlocfilehash: dd135f20814f1d2bd5a5a785275659b19a4e628a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902529"
---
# <span data-ttu-id="49cf3-101">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="49cf3-101">Get-AzNetworkWatcherFlowLogStatus</span></span>

## <span data-ttu-id="49cf3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="49cf3-102">SYNOPSIS</span></span>
<span data-ttu-id="49cf3-103">在資源上獲得流程記錄的狀態。</span><span class="sxs-lookup"><span data-stu-id="49cf3-103">Gets the status of flow logging on a resource.</span></span>

## <span data-ttu-id="49cf3-104">語法</span><span class="sxs-lookup"><span data-stu-id="49cf3-104">SYNTAX</span></span>

### <span data-ttu-id="49cf3-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="49cf3-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49cf3-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="49cf3-106">SetByName</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49cf3-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="49cf3-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -Location <String> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49cf3-108">描述</span><span class="sxs-lookup"><span data-stu-id="49cf3-108">DESCRIPTION</span></span>
<span data-ttu-id="49cf3-109">此Get-AzNetworkWatcherFlowLogStatus Cmdlet 會獲得資源上流程記錄的狀態。</span><span class="sxs-lookup"><span data-stu-id="49cf3-109">The Get-AzNetworkWatcherFlowLogStatus cmdlet Gets the status of flow logging on a resource.</span></span> <span data-ttu-id="49cf3-110">狀態包括是否針對所提供的資源啟用流程記錄、已配置的儲存空間帳戶來傳送記錄，以及記錄保留原則。</span><span class="sxs-lookup"><span data-stu-id="49cf3-110">The status includes whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="49cf3-111">目前網路安全性群組支援流程記錄。</span><span class="sxs-lookup"><span data-stu-id="49cf3-111">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="49cf3-112">例子</span><span class="sxs-lookup"><span data-stu-id="49cf3-112">EXAMPLES</span></span>

### <span data-ttu-id="49cf3-113">範例 1：取得指定 NSG 的流量記錄狀態</span><span class="sxs-lookup"><span data-stu-id="49cf3-113">Example 1: Get the Flow Logging Status for a Specified NSG</span></span>
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

<span data-ttu-id="49cf3-114">在此範例中，我們取得網路安全性群組的流量記錄狀態。</span><span class="sxs-lookup"><span data-stu-id="49cf3-114">In this example we get the flow logging status for a Network Security Group.</span></span> <span data-ttu-id="49cf3-115">指定的 NSG 已啟用流程記錄、預設格式，而且未設定保留原則。</span><span class="sxs-lookup"><span data-stu-id="49cf3-115">The specified NSG has flow logging enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="49cf3-116">範例 2：取得指定 NSG 的流量記錄與流量分析狀態</span><span class="sxs-lookup"><span data-stu-id="49cf3-116">Example 2: Get the Flow Logging and Traffic Analytics Status for a Specified NSG</span></span>
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

<span data-ttu-id="49cf3-117">在此範例中，我們取得網路安全性群組的流量記錄和流量分析狀態。</span><span class="sxs-lookup"><span data-stu-id="49cf3-117">In this example we get the flow logging and Traffic Analytics status for a Network Security Group.</span></span> <span data-ttu-id="49cf3-118">指定的 NSG 已啟用流程記錄與流量分析，預設格式且未設定保留原則。</span><span class="sxs-lookup"><span data-stu-id="49cf3-118">The specified NSG has flow logging and Traffic Analytics enabled, default format and no retention policy set.</span></span>

## <span data-ttu-id="49cf3-119">參數</span><span class="sxs-lookup"><span data-stu-id="49cf3-119">PARAMETERS</span></span>

### <span data-ttu-id="49cf3-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="49cf3-120">-AsJob</span></span>
<span data-ttu-id="49cf3-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="49cf3-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="49cf3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49cf3-122">-DefaultProfile</span></span>
<span data-ttu-id="49cf3-123">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="49cf3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49cf3-124">-位置</span><span class="sxs-lookup"><span data-stu-id="49cf3-124">-Location</span></span>
<span data-ttu-id="49cf3-125">網路監視者的位置。</span><span class="sxs-lookup"><span data-stu-id="49cf3-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="49cf3-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="49cf3-126">-NetworkWatcher</span></span>
<span data-ttu-id="49cf3-127">網路監視程式資源。</span><span class="sxs-lookup"><span data-stu-id="49cf3-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="49cf3-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="49cf3-128">-NetworkWatcherName</span></span>
<span data-ttu-id="49cf3-129">網路監視者的名稱。</span><span class="sxs-lookup"><span data-stu-id="49cf3-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="49cf3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49cf3-130">-ResourceGroupName</span></span>
<span data-ttu-id="49cf3-131">網路監視者資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="49cf3-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="49cf3-132">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="49cf3-132">-TargetResourceId</span></span>
<span data-ttu-id="49cf3-133">目標資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="49cf3-133">The target resource ID.</span></span>

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

### <span data-ttu-id="49cf3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49cf3-134">CommonParameters</span></span>
<span data-ttu-id="49cf3-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="49cf3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49cf3-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49cf3-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49cf3-137">輸入</span><span class="sxs-lookup"><span data-stu-id="49cf3-137">INPUTS</span></span>

### <span data-ttu-id="49cf3-138">Microsoft.Azure.Commands.Network.models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="49cf3-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="49cf3-139">System.String</span><span class="sxs-lookup"><span data-stu-id="49cf3-139">System.String</span></span>

## <span data-ttu-id="49cf3-140">輸出</span><span class="sxs-lookup"><span data-stu-id="49cf3-140">OUTPUTS</span></span>

### <span data-ttu-id="49cf3-141">Microsoft.Azure.Commands.network.models.PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="49cf3-141">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="49cf3-142">筆記</span><span class="sxs-lookup"><span data-stu-id="49cf3-142">NOTES</span></span>
<span data-ttu-id="49cf3-143">關鍵字：azure、azurerm、arm、resource、management、manager、network、network、watcher、flow、logs、flowlog、logging</span><span class="sxs-lookup"><span data-stu-id="49cf3-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="49cf3-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="49cf3-144">RELATED LINKS</span></span>

[<span data-ttu-id="49cf3-145">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="49cf3-145">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="49cf3-146">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="49cf3-146">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="49cf3-147">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="49cf3-147">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="49cf3-148">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="49cf3-148">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="49cf3-149">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="49cf3-149">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="49cf3-150">Get-AzNetworkWatcherTopwork</span><span class="sxs-lookup"><span data-stu-id="49cf3-150">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="49cf3-151">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="49cf3-151">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="49cf3-152">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="49cf3-152">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="49cf3-153">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="49cf3-153">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="49cf3-154">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="49cf3-154">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="49cf3-155">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="49cf3-155">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="49cf3-156">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="49cf3-156">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="49cf3-157">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="49cf3-157">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="49cf3-158">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="49cf3-158">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="49cf3-159">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="49cf3-159">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="49cf3-160">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="49cf3-160">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="49cf3-161">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="49cf3-161">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="49cf3-162">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="49cf3-162">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="49cf3-163">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="49cf3-163">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="49cf3-164">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="49cf3-164">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="49cf3-165">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="49cf3-165">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="49cf3-166">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="49cf3-166">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="49cf3-167">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="49cf3-167">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="49cf3-168">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="49cf3-168">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="49cf3-169">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="49cf3-169">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="49cf3-170">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="49cf3-170">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="49cf3-171">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="49cf3-171">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
