---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkwatchertopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherTopology.md
ms.openlocfilehash: 525dff96126c91d2d434d681bd49659513e7ec7e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902497"
---
# <span data-ttu-id="5feb6-101">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="5feb6-101">Get-AzNetworkWatcherTopology</span></span>

## <span data-ttu-id="5feb6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5feb6-102">SYNOPSIS</span></span>
<span data-ttu-id="5feb6-103">在資源群組中，以網路層級查看資源及其關係。</span><span class="sxs-lookup"><span data-stu-id="5feb6-103">Gets a network level view of resources and their relationships in a resource group.</span></span>

## <span data-ttu-id="5feb6-104">語法</span><span class="sxs-lookup"><span data-stu-id="5feb6-104">SYNTAX</span></span>

### <span data-ttu-id="5feb6-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="5feb6-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherTopology -NetworkWatcher <PSNetworkWatcher> -TargetResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5feb6-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="5feb6-106">SetByName</span></span>
```
Get-AzNetworkWatcherTopology -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5feb6-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="5feb6-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherTopology -Location <String> -TargetResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5feb6-108">描述</span><span class="sxs-lookup"><span data-stu-id="5feb6-108">DESCRIPTION</span></span>
<span data-ttu-id="5feb6-109">此Get-AzNetworkWatcherTopology Cmdlet 資源的網路層級視圖及其在資源群組中的關係。</span><span class="sxs-lookup"><span data-stu-id="5feb6-109">The Get-AzNetworkWatcherTopology cmdlet a network level view of resources and their relationships in a resource group.</span></span> <span data-ttu-id="5feb6-110">注意：如果來自多個區域的資源位於資源群組中，則 JSON 輸出中只會包含與網路監視者同一區域的資源。</span><span class="sxs-lookup"><span data-stu-id="5feb6-110">Note: If resources from multiple regions reside in the resource group, only the resources in the same region as the Network Watcher will be included in the JSON output.</span></span>

## <span data-ttu-id="5feb6-111">例子</span><span class="sxs-lookup"><span data-stu-id="5feb6-111">EXAMPLES</span></span>

### <span data-ttu-id="5feb6-112">範例 1：取得 Azure 拓撲</span><span class="sxs-lookup"><span data-stu-id="5feb6-112">Example 1: Get an Azure Topology</span></span>
```
$networkWatcher = Get-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG 
Get-AzNetworkWatcherTopology -NetworkWatcher $networkWatcher -ResourceGroupName testresourcegroup

Id                : e33d80cf-4f76-4b8f-b51c-5bb8eba80103
CreatedDateTime   : 0/00/0000 9:21:51 PM
LastModified      : 0/00/0000 4:53:29 AM
TopologyResources : [
                      {
                        "Name": "testresourcegroup-vnet",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/virtualNetworks/testresourcegroup-vnet",
                        "Location": "westcentralus",
                        "TopologyAssociations": [
                          {
                            "Name": "default",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/virtualNetworks/testresourcegroup-vnet/subnets/default",
                            "AssociationType": "Contains"
                          }
                        ]
                      },
                      {
                        "Name": "default",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/virtualNetworks/testresourcegroup-vnet/subnets/default",
                        "Location": "westcentralus",
                        "TopologyAssociations": []
                      },
                      {
                        "Name": "VM0",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Compute/virtualMachines/VM0",
                        "TopologyAssociations": [
                          {
                            "Name": "vm0131",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkInterfaces/vm0131",
                            "AssociationType": "Contains"
                          }
                        ]
                      },
                      {
                        "Name": "vm0131",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkInterfaces/vm0131",
                        "Location": "westcentralus",
                        "TopologyAssociations": [
                          {
                            "Name": "VM0",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Compute/virtualMachines/VM0",
                            "AssociationType": "Associated"
                          },
                          {
                            "Name": "VM0-nsg",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkSecurityGroups/VM0-nsg",
                            "AssociationType": "Associated"
                          },
                          {
                            "Name": "default",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/virtualNetworks/testresourcegroup-vnet/subnets/default",
                            "AssociationType": "Associated"
                          },
                          {
                            "Name": "VM0-ip",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/publicIPAddresses/VM0-ip",
                            "AssociationType": "Associated"
                          }
                        ]
                      },
                      {
                        "Name": "VM0-nsg",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkSecurityGroups/VM0-nsg",
                        "Location": "westcentralus",
                        "TopologyAssociations": [
                          {
                            "Name": "default-allow-rdp",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkSecurityGroups/VM0-nsg/securityRules/default-allow-rdp",
                            "AssociationType": "Contains"
                          }
                        ]
                      },
                      {
                        "Name": "default-allow-rdp",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkSecurityGroups/VM0-nsg/securityRules/default-allow-rdp",
                        "Location": "westcentralus",
                        "TopologyAssociations": []
                      },
                      {
                        "Name": "VM0-ip",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/publicIPAddresses/VM0-ip",
                        "Location": "westcentralus",
                        "TopologyAssociations": [
                          {
                            "Name": "vm0131",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkInterfaces/vm0131",
                            "AssociationType": "Associated"
                          }
                        ]
                      }
                    ]
```

<span data-ttu-id="5feb6-113">在此範例中，我們在Get-AzNetworkWatcherTopology VM、Nic、NSG 和公用 IP 的資源群組上執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5feb6-113">In this example we run the Get-AzNetworkWatcherTopology cmdlet on a resource group that contains a VM, Nic, NSG, and public IP.</span></span>

## <span data-ttu-id="5feb6-114">參數</span><span class="sxs-lookup"><span data-stu-id="5feb6-114">PARAMETERS</span></span>

### <span data-ttu-id="5feb6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5feb6-115">-DefaultProfile</span></span>
<span data-ttu-id="5feb6-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5feb6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5feb6-117">-位置</span><span class="sxs-lookup"><span data-stu-id="5feb6-117">-Location</span></span>
<span data-ttu-id="5feb6-118">網路監視者的位置。</span><span class="sxs-lookup"><span data-stu-id="5feb6-118">Location of the network watcher.</span></span>

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

### <span data-ttu-id="5feb6-119">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5feb6-119">-NetworkWatcher</span></span>
<span data-ttu-id="5feb6-120">網路監視程式資源。</span><span class="sxs-lookup"><span data-stu-id="5feb6-120">The network watcher resource.</span></span>

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

### <span data-ttu-id="5feb6-121">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="5feb6-121">-NetworkWatcherName</span></span>
<span data-ttu-id="5feb6-122">網路監視者的名稱。</span><span class="sxs-lookup"><span data-stu-id="5feb6-122">The name of network watcher.</span></span>

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

### <span data-ttu-id="5feb6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5feb6-123">-ResourceGroupName</span></span>
<span data-ttu-id="5feb6-124">網路監視者資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5feb6-124">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="5feb6-125">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5feb6-125">-TargetResourceGroupName</span></span>
<span data-ttu-id="5feb6-126">資源組名。</span><span class="sxs-lookup"><span data-stu-id="5feb6-126">The resource group name.</span></span>

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

### <span data-ttu-id="5feb6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5feb6-127">CommonParameters</span></span>
<span data-ttu-id="5feb6-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5feb6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5feb6-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5feb6-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5feb6-130">輸入</span><span class="sxs-lookup"><span data-stu-id="5feb6-130">INPUTS</span></span>

### <span data-ttu-id="5feb6-131">Microsoft.Azure.Commands.Network.models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5feb6-131">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="5feb6-132">System.String</span><span class="sxs-lookup"><span data-stu-id="5feb6-132">System.String</span></span>

## <span data-ttu-id="5feb6-133">輸出</span><span class="sxs-lookup"><span data-stu-id="5feb6-133">OUTPUTS</span></span>

### <span data-ttu-id="5feb6-134">Microsoft.Azure.Commands.Network.models.PSTop用</span><span class="sxs-lookup"><span data-stu-id="5feb6-134">Microsoft.Azure.Commands.Network.Models.PSTopology</span></span>

## <span data-ttu-id="5feb6-135">筆記</span><span class="sxs-lookup"><span data-stu-id="5feb6-135">NOTES</span></span>
<span data-ttu-id="5feb6-136">關鍵字：azure、azurerm、arm、資源、管理、管理員、網路監視器、拓撲、視圖</span><span class="sxs-lookup"><span data-stu-id="5feb6-136">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, topology, view</span></span> 

## <span data-ttu-id="5feb6-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="5feb6-137">RELATED LINKS</span></span>

[<span data-ttu-id="5feb6-138">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5feb6-138">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="5feb6-139">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5feb6-139">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="5feb6-140">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5feb6-140">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="5feb6-141">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="5feb6-141">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="5feb6-142">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="5feb6-142">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="5feb6-143">Get-AzNetworkWatcherTopwork</span><span class="sxs-lookup"><span data-stu-id="5feb6-143">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="5feb6-144">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="5feb6-144">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="5feb6-145">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5feb6-145">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5feb6-146">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="5feb6-146">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="5feb6-147">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5feb6-147">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5feb6-148">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5feb6-148">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5feb6-149">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5feb6-149">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5feb6-150">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="5feb6-150">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="5feb6-151">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="5feb6-151">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="5feb6-152">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="5feb6-152">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="5feb6-153">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5feb6-153">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5feb6-154">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5feb6-154">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5feb6-155">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5feb6-155">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5feb6-156">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="5feb6-156">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="5feb6-157">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5feb6-157">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5feb6-158">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5feb6-158">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5feb6-159">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="5feb6-159">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="5feb6-160">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="5feb6-160">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="5feb6-161">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="5feb6-161">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="5feb6-162">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="5feb6-162">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="5feb6-163">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="5feb6-163">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="5feb6-164">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5feb6-164">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

