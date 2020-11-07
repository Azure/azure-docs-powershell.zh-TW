---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchertopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherTopology.md
ms.openlocfilehash: 72f5c803c7fa4f4693da3660c41f73eadb464ab7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794381"
---
# <span data-ttu-id="b7f3c-101">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="b7f3c-101">Get-AzNetworkWatcherTopology</span></span>

## <span data-ttu-id="b7f3c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b7f3c-102">SYNOPSIS</span></span>
<span data-ttu-id="b7f3c-103">在資源群組中取得資源及其關聯的網路層級視圖。</span><span class="sxs-lookup"><span data-stu-id="b7f3c-103">Gets a network level view of resources and their relationships in a resource group.</span></span>

## <span data-ttu-id="b7f3c-104">句法</span><span class="sxs-lookup"><span data-stu-id="b7f3c-104">SYNTAX</span></span>

### <span data-ttu-id="b7f3c-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="b7f3c-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherTopology -NetworkWatcher <PSNetworkWatcher> -TargetResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7f3c-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="b7f3c-106">SetByName</span></span>
```
Get-AzNetworkWatcherTopology -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7f3c-107">說明</span><span class="sxs-lookup"><span data-stu-id="b7f3c-107">DESCRIPTION</span></span>
<span data-ttu-id="b7f3c-108">Get-AzNetworkWatcherTopology Cmdlet 在資源群組中資源及其關聯的網路層級視圖。</span><span class="sxs-lookup"><span data-stu-id="b7f3c-108">The Get-AzNetworkWatcherTopology cmdlet a network level view of resources and their relationships in a resource group.</span></span> <span data-ttu-id="b7f3c-109">注意：如果來自多個區域的資源位於 [資源] 群組中，則只有與網路觀察程式相同區域中的資源，才會包含在 JSON 輸出中。</span><span class="sxs-lookup"><span data-stu-id="b7f3c-109">Note: If resources from multiple regions reside in the resource group, only the resources in the same region as the Network Watcher will be included in the JSON output.</span></span>

## <span data-ttu-id="b7f3c-110">示例</span><span class="sxs-lookup"><span data-stu-id="b7f3c-110">EXAMPLES</span></span>

### <span data-ttu-id="b7f3c-111">--------------------------範例1：取得 Azure 拓撲--------------------------</span><span class="sxs-lookup"><span data-stu-id="b7f3c-111">--------------------------  Example 1: Get an Azure Topology  --------------------------</span></span>
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

<span data-ttu-id="b7f3c-112">在這個範例中，我們會在包含 VM、Nic、NSG 和公用 IP 的資源群組上執行 Get-AzNetworkWatcherTopology Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b7f3c-112">In this example we run the Get-AzNetworkWatcherTopology cmdlet on a resource group that contains a VM, Nic, NSG, and public IP.</span></span>

## <span data-ttu-id="b7f3c-113">參數</span><span class="sxs-lookup"><span data-stu-id="b7f3c-113">PARAMETERS</span></span>

### <span data-ttu-id="b7f3c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7f3c-114">-DefaultProfile</span></span>
<span data-ttu-id="b7f3c-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b7f3c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7f3c-116">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b7f3c-116">-NetworkWatcher</span></span>
<span data-ttu-id="b7f3c-117">網路觀察程式資源。</span><span class="sxs-lookup"><span data-stu-id="b7f3c-117">The network watcher resource.</span></span>

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

### <span data-ttu-id="b7f3c-118">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="b7f3c-118">-NetworkWatcherName</span></span>
<span data-ttu-id="b7f3c-119">網路觀察程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="b7f3c-119">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7f3c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7f3c-120">-ResourceGroupName</span></span>
<span data-ttu-id="b7f3c-121">網路監視程式資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b7f3c-121">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7f3c-122">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7f3c-122">-TargetResourceGroupName</span></span>
<span data-ttu-id="b7f3c-123">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b7f3c-123">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7f3c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7f3c-124">CommonParameters</span></span>
<span data-ttu-id="b7f3c-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b7f3c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7f3c-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b7f3c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7f3c-127">輸入</span><span class="sxs-lookup"><span data-stu-id="b7f3c-127">INPUTS</span></span>

### <span data-ttu-id="b7f3c-128">PSNetworkWatcher 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b7f3c-128">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="b7f3c-129">System.object</span><span class="sxs-lookup"><span data-stu-id="b7f3c-129">System.String</span></span>

## <span data-ttu-id="b7f3c-130">輸出</span><span class="sxs-lookup"><span data-stu-id="b7f3c-130">OUTPUTS</span></span>

### <span data-ttu-id="b7f3c-131">PSTopology 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b7f3c-131">Microsoft.Azure.Commands.Network.Models.PSTopology</span></span>

## <span data-ttu-id="b7f3c-132">筆記</span><span class="sxs-lookup"><span data-stu-id="b7f3c-132">NOTES</span></span>
<span data-ttu-id="b7f3c-133">關鍵字： azure，azurerm，arm，資源，管理，管理員，網路，網路，網路觀察程式，拓撲，view</span><span class="sxs-lookup"><span data-stu-id="b7f3c-133">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, topology, view</span></span> 

## <span data-ttu-id="b7f3c-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="b7f3c-134">RELATED LINKS</span></span>

[<span data-ttu-id="b7f3c-135">新-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b7f3c-135">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="b7f3c-136">AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b7f3c-136">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="b7f3c-137">移除-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b7f3c-137">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="b7f3c-138">新-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b7f3c-138">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b7f3c-139">新-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="b7f3c-139">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="b7f3c-140">AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b7f3c-140">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b7f3c-141">移除-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b7f3c-141">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b7f3c-142">停止 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b7f3c-142">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b7f3c-143">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="b7f3c-143">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="b7f3c-144">AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="b7f3c-144">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="b7f3c-145">AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="b7f3c-145">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="b7f3c-146">開始-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="b7f3c-146">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

