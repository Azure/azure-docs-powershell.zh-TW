---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchertopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherTopology.md
ms.openlocfilehash: 83b0ce893529638818e85844fcb9bd087941f155
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98288767"
---
# <span data-ttu-id="1c7bb-101">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="1c7bb-101">Get-AzNetworkWatcherTopology</span></span>

## <span data-ttu-id="1c7bb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1c7bb-102">SYNOPSIS</span></span>
<span data-ttu-id="1c7bb-103">在資源群組中取得資源及其關聯的網路層級視圖。</span><span class="sxs-lookup"><span data-stu-id="1c7bb-103">Gets a network level view of resources and their relationships in a resource group.</span></span>

## <span data-ttu-id="1c7bb-104">句法</span><span class="sxs-lookup"><span data-stu-id="1c7bb-104">SYNTAX</span></span>

### <span data-ttu-id="1c7bb-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="1c7bb-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherTopology -NetworkWatcher <PSNetworkWatcher> -TargetResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c7bb-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="1c7bb-106">SetByName</span></span>
```
Get-AzNetworkWatcherTopology -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c7bb-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="1c7bb-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherTopology -Location <String> -TargetResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c7bb-108">說明</span><span class="sxs-lookup"><span data-stu-id="1c7bb-108">DESCRIPTION</span></span>
<span data-ttu-id="1c7bb-109">Get-AzNetworkWatcherTopology Cmdlet 在資源群組中資源及其關聯的網路層級視圖。</span><span class="sxs-lookup"><span data-stu-id="1c7bb-109">The Get-AzNetworkWatcherTopology cmdlet a network level view of resources and their relationships in a resource group.</span></span> <span data-ttu-id="1c7bb-110">注意：如果來自多個區域的資源位於 [資源] 群組中，則只有與網路觀察程式相同區域中的資源，才會包含在 JSON 輸出中。</span><span class="sxs-lookup"><span data-stu-id="1c7bb-110">Note: If resources from multiple regions reside in the resource group, only the resources in the same region as the Network Watcher will be included in the JSON output.</span></span>

## <span data-ttu-id="1c7bb-111">示例</span><span class="sxs-lookup"><span data-stu-id="1c7bb-111">EXAMPLES</span></span>

### <span data-ttu-id="1c7bb-112">範例1：取得 Azure 拓撲</span><span class="sxs-lookup"><span data-stu-id="1c7bb-112">Example 1: Get an Azure Topology</span></span>
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

<span data-ttu-id="1c7bb-113">在這個範例中，我們會在包含 VM、Nic、NSG 和公用 IP 的資源群組上執行 Get-AzNetworkWatcherTopology Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1c7bb-113">In this example we run the Get-AzNetworkWatcherTopology cmdlet on a resource group that contains a VM, Nic, NSG, and public IP.</span></span>

## <span data-ttu-id="1c7bb-114">參數</span><span class="sxs-lookup"><span data-stu-id="1c7bb-114">PARAMETERS</span></span>

### <span data-ttu-id="1c7bb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c7bb-115">-DefaultProfile</span></span>
<span data-ttu-id="1c7bb-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1c7bb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c7bb-117">-位置</span><span class="sxs-lookup"><span data-stu-id="1c7bb-117">-Location</span></span>
<span data-ttu-id="1c7bb-118">網路觀察程式的位置。</span><span class="sxs-lookup"><span data-stu-id="1c7bb-118">Location of the network watcher.</span></span>

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

### <span data-ttu-id="1c7bb-119">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1c7bb-119">-NetworkWatcher</span></span>
<span data-ttu-id="1c7bb-120">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="1c7bb-120">The network watcher resource.</span></span>

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

### <span data-ttu-id="1c7bb-121">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="1c7bb-121">-NetworkWatcherName</span></span>
<span data-ttu-id="1c7bb-122">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="1c7bb-122">The name of network watcher.</span></span>

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

### <span data-ttu-id="1c7bb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c7bb-123">-ResourceGroupName</span></span>
<span data-ttu-id="1c7bb-124">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1c7bb-124">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="1c7bb-125">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c7bb-125">-TargetResourceGroupName</span></span>
<span data-ttu-id="1c7bb-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1c7bb-126">The resource group name.</span></span>

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

### <span data-ttu-id="1c7bb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c7bb-127">CommonParameters</span></span>
<span data-ttu-id="1c7bb-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1c7bb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c7bb-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1c7bb-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c7bb-130">輸入</span><span class="sxs-lookup"><span data-stu-id="1c7bb-130">INPUTS</span></span>

### <span data-ttu-id="1c7bb-131">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1c7bb-131">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="1c7bb-132">System.object</span><span class="sxs-lookup"><span data-stu-id="1c7bb-132">System.String</span></span>

## <span data-ttu-id="1c7bb-133">輸出</span><span class="sxs-lookup"><span data-stu-id="1c7bb-133">OUTPUTS</span></span>

### <span data-ttu-id="1c7bb-134">PSTopology 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1c7bb-134">Microsoft.Azure.Commands.Network.Models.PSTopology</span></span>

## <span data-ttu-id="1c7bb-135">筆記</span><span class="sxs-lookup"><span data-stu-id="1c7bb-135">NOTES</span></span>
<span data-ttu-id="1c7bb-136">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，拓撲，view</span><span class="sxs-lookup"><span data-stu-id="1c7bb-136">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, topology, view</span></span> 

## <span data-ttu-id="1c7bb-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="1c7bb-137">RELATED LINKS</span></span>

[<span data-ttu-id="1c7bb-138">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1c7bb-138">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="1c7bb-139">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1c7bb-139">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="1c7bb-140">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1c7bb-140">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="1c7bb-141">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="1c7bb-141">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="1c7bb-142">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="1c7bb-142">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="1c7bb-143">AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="1c7bb-143">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="1c7bb-144">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="1c7bb-144">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="1c7bb-145">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1c7bb-145">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1c7bb-146">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="1c7bb-146">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="1c7bb-147">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1c7bb-147">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1c7bb-148">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1c7bb-148">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1c7bb-149">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1c7bb-149">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1c7bb-150">新-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="1c7bb-150">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="1c7bb-151">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="1c7bb-151">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="1c7bb-152">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="1c7bb-152">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="1c7bb-153">停止 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1c7bb-153">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1c7bb-154">開始-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1c7bb-154">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1c7bb-155">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1c7bb-155">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1c7bb-156">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="1c7bb-156">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="1c7bb-157">移除-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1c7bb-157">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1c7bb-158">新-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1c7bb-158">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1c7bb-159">AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="1c7bb-159">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="1c7bb-160">AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="1c7bb-160">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="1c7bb-161">AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="1c7bb-161">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="1c7bb-162">AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="1c7bb-162">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="1c7bb-163">AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="1c7bb-163">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="1c7bb-164">AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1c7bb-164">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

