---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherflowlogstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
ms.openlocfilehash: a45a6ad4ee85dfabb28bef07400a0b6ebe115d7c
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100414946"
---
# <span data-ttu-id="7fd7f-101">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="7fd7f-101">Get-AzNetworkWatcherFlowLogStatus</span></span>

## <span data-ttu-id="7fd7f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7fd7f-102">SYNOPSIS</span></span>
<span data-ttu-id="7fd7f-103">在資源上獲得流程記錄的狀態。</span><span class="sxs-lookup"><span data-stu-id="7fd7f-103">Gets the status of flow logging on a resource.</span></span>

## <span data-ttu-id="7fd7f-104">語法</span><span class="sxs-lookup"><span data-stu-id="7fd7f-104">SYNTAX</span></span>

### <span data-ttu-id="7fd7f-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="7fd7f-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7fd7f-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="7fd7f-106">SetByName</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7fd7f-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="7fd7f-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -Location <String> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7fd7f-108">描述</span><span class="sxs-lookup"><span data-stu-id="7fd7f-108">DESCRIPTION</span></span>
<span data-ttu-id="7fd7f-109">此Get-AzNetworkWatcherFlowLogStatus Cmdlet 會獲得資源上流程記錄的狀態。</span><span class="sxs-lookup"><span data-stu-id="7fd7f-109">The Get-AzNetworkWatcherFlowLogStatus cmdlet Gets the status of flow logging on a resource.</span></span> <span data-ttu-id="7fd7f-110">狀態包括是否針對所提供的資源啟用流程記錄、已配置的儲存空間帳戶來傳送記錄，以及記錄保留原則。</span><span class="sxs-lookup"><span data-stu-id="7fd7f-110">The status includes whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="7fd7f-111">目前網路安全性群組支援流程記錄。</span><span class="sxs-lookup"><span data-stu-id="7fd7f-111">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="7fd7f-112">例子</span><span class="sxs-lookup"><span data-stu-id="7fd7f-112">EXAMPLES</span></span>

### <span data-ttu-id="7fd7f-113">範例 1：取得指定 NSG 的流量記錄狀態</span><span class="sxs-lookup"><span data-stu-id="7fd7f-113">Example 1: Get the Flow Logging Status for a Specified NSG</span></span>
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

<span data-ttu-id="7fd7f-114">在此範例中，我們取得網路安全性群組的流量記錄狀態。</span><span class="sxs-lookup"><span data-stu-id="7fd7f-114">In this example we get the flow logging status for a Network Security Group.</span></span> <span data-ttu-id="7fd7f-115">指定的 NSG 已啟用流程記錄、預設格式，而且未設定保留原則。</span><span class="sxs-lookup"><span data-stu-id="7fd7f-115">The specified NSG has flow logging enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="7fd7f-116">範例 2：取得指定 NSG 的流量記錄與流量分析狀態</span><span class="sxs-lookup"><span data-stu-id="7fd7f-116">Example 2: Get the Flow Logging and Traffic Analytics Status for a Specified NSG</span></span>
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

<span data-ttu-id="7fd7f-117">在此範例中，我們取得網路安全性群組的流量記錄和流量分析狀態。</span><span class="sxs-lookup"><span data-stu-id="7fd7f-117">In this example we get the flow logging and Traffic Analytics status for a Network Security Group.</span></span> <span data-ttu-id="7fd7f-118">指定的 NSG 已啟用流程記錄與流量分析，預設格式且未設定保留原則。</span><span class="sxs-lookup"><span data-stu-id="7fd7f-118">The specified NSG has flow logging and Traffic Analytics enabled, default format and no retention policy set.</span></span>

## <span data-ttu-id="7fd7f-119">參數</span><span class="sxs-lookup"><span data-stu-id="7fd7f-119">PARAMETERS</span></span>

### <span data-ttu-id="7fd7f-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7fd7f-120">-AsJob</span></span>
<span data-ttu-id="7fd7f-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7fd7f-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7fd7f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fd7f-122">-DefaultProfile</span></span>
<span data-ttu-id="7fd7f-123">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7fd7f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7fd7f-124">-位置</span><span class="sxs-lookup"><span data-stu-id="7fd7f-124">-Location</span></span>
<span data-ttu-id="7fd7f-125">網路監視者的位置。</span><span class="sxs-lookup"><span data-stu-id="7fd7f-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="7fd7f-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7fd7f-126">-NetworkWatcher</span></span>
<span data-ttu-id="7fd7f-127">網路監視程式資源。</span><span class="sxs-lookup"><span data-stu-id="7fd7f-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="7fd7f-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="7fd7f-128">-NetworkWatcherName</span></span>
<span data-ttu-id="7fd7f-129">網路監視者的名稱。</span><span class="sxs-lookup"><span data-stu-id="7fd7f-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="7fd7f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fd7f-130">-ResourceGroupName</span></span>
<span data-ttu-id="7fd7f-131">網路監視者資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7fd7f-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="7fd7f-132">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="7fd7f-132">-TargetResourceId</span></span>
<span data-ttu-id="7fd7f-133">目標資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="7fd7f-133">The target resource ID.</span></span>

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

### <span data-ttu-id="7fd7f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fd7f-134">CommonParameters</span></span>
<span data-ttu-id="7fd7f-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7fd7f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fd7f-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7fd7f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fd7f-137">輸入</span><span class="sxs-lookup"><span data-stu-id="7fd7f-137">INPUTS</span></span>

### <span data-ttu-id="7fd7f-138">Microsoft.Azure.Commands.Network.models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7fd7f-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="7fd7f-139">System.String</span><span class="sxs-lookup"><span data-stu-id="7fd7f-139">System.String</span></span>

## <span data-ttu-id="7fd7f-140">輸出</span><span class="sxs-lookup"><span data-stu-id="7fd7f-140">OUTPUTS</span></span>

### <span data-ttu-id="7fd7f-141">Microsoft.Azure.Commands.network.models.PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="7fd7f-141">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="7fd7f-142">筆記</span><span class="sxs-lookup"><span data-stu-id="7fd7f-142">NOTES</span></span>
<span data-ttu-id="7fd7f-143">關鍵字：azure、azurerm、arm、resource、management、manager、network、network、watcher、flow、logs、flowlog、logging</span><span class="sxs-lookup"><span data-stu-id="7fd7f-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="7fd7f-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="7fd7f-144">RELATED LINKS</span></span>

[<span data-ttu-id="7fd7f-145">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7fd7f-145">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="7fd7f-146">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7fd7f-146">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="7fd7f-147">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7fd7f-147">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="7fd7f-148">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="7fd7f-148">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="7fd7f-149">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="7fd7f-149">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="7fd7f-150">Get-AzNetworkWatcherTopwork</span><span class="sxs-lookup"><span data-stu-id="7fd7f-150">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="7fd7f-151">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="7fd7f-151">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="7fd7f-152">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7fd7f-152">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7fd7f-153">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="7fd7f-153">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="7fd7f-154">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7fd7f-154">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7fd7f-155">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7fd7f-155">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7fd7f-156">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7fd7f-156">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7fd7f-157">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="7fd7f-157">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="7fd7f-158">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="7fd7f-158">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="7fd7f-159">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="7fd7f-159">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="7fd7f-160">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7fd7f-160">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7fd7f-161">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7fd7f-161">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7fd7f-162">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7fd7f-162">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7fd7f-163">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="7fd7f-163">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="7fd7f-164">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7fd7f-164">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7fd7f-165">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7fd7f-165">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7fd7f-166">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="7fd7f-166">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="7fd7f-167">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="7fd7f-167">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="7fd7f-168">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="7fd7f-168">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="7fd7f-169">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="7fd7f-169">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="7fd7f-170">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="7fd7f-170">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="7fd7f-171">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7fd7f-171">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
