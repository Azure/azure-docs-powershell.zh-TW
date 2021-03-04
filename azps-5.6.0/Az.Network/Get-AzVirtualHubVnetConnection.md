---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubVnetConnection.md
ms.openlocfilehash: c5de4de61a1a0d2aeb14d8a360500b928a28fdcf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916914"
---
# <span data-ttu-id="d70ea-101">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="d70ea-101">Get-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="d70ea-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d70ea-102">SYNOPSIS</span></span>
<span data-ttu-id="d70ea-103">在虛擬中樞中建立虛擬網路連接，或列出虛擬中樞中所有的虛擬網路連接。</span><span class="sxs-lookup"><span data-stu-id="d70ea-103">Gets a Virtual Network Connection in a virtual hub or lists all virtual network connections in a virtual hub.</span></span>

## <span data-ttu-id="d70ea-104">語法</span><span class="sxs-lookup"><span data-stu-id="d70ea-104">SYNTAX</span></span>

### <span data-ttu-id="d70ea-105">ByVirtualHubName (預設) </span><span class="sxs-lookup"><span data-stu-id="d70ea-105">ByVirtualHubName (Default)</span></span>
```
Get-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d70ea-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="d70ea-106">ByVirtualHubObject</span></span>
```
Get-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d70ea-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="d70ea-107">ByVirtualHubResourceId</span></span>
```
Get-AzVirtualHubVnetConnection -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d70ea-108">描述</span><span class="sxs-lookup"><span data-stu-id="d70ea-108">DESCRIPTION</span></span>
<span data-ttu-id="d70ea-109">在虛擬中樞中建立虛擬網路連接，或列出虛擬中樞中所有的虛擬網路連接。</span><span class="sxs-lookup"><span data-stu-id="d70ea-109">Gets a Virtual Network Connection in a virtual hub or lists all virtual network connections in a virtual hub.</span></span>

## <span data-ttu-id="d70ea-110">例子</span><span class="sxs-lookup"><span data-stu-id="d70ea-110">EXAMPLES</span></span>

### <span data-ttu-id="d70ea-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="d70ea-111">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet

PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork

PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
RoutingConfiguration : {
                            "AssociatedRouteTable": {
                                "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                            },
                            "PropagatedRouteTables": {
                                "Labels": [],
                                "Ids": [
                                    {
                                        "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                    }
                                ]
                            },
                            "VnetRoutes": {
                                "StaticRoutes": []
                            }
                        }
```

<span data-ttu-id="d70ea-112">上述步驟將在 Azure 的資源群組中，建立資源群組、虛擬 WAN、虛擬網路、美國中心的虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="d70ea-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="d70ea-113">在此之後，將會建立一個虛擬網路連接，將虛擬網路對等至虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="d70ea-113">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="d70ea-114">中樞虛擬網路連接建立後，會使用其資源組名、中樞名稱和連接名稱，獲得中樞虛擬網路連接。</span><span class="sxs-lookup"><span data-stu-id="d70ea-114">After the hub virtual network connection is created, it gets the hub virtual network connection using its resource group name, the hub name and the connection name.</span></span>

### <span data-ttu-id="d70ea-115">範例 2</span><span class="sxs-lookup"><span data-stu-id="d70ea-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
RoutingConfiguration : {
                            "AssociatedRouteTable": {
                                "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                            },
                            "PropagatedRouteTables": {
                                "Labels": [],
                                "Ids": [
                                    {
                                        "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                    }
                                ]
                            },
                            "VnetRoutes": {
                                "StaticRoutes": []
                            }
                        }
```

<span data-ttu-id="d70ea-116">上述步驟將在 Azure 的資源群組中，建立資源群組、虛擬 WAN、虛擬網路、美國中心的虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="d70ea-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="d70ea-117">在此之後，將會建立一個虛擬網路連接，將虛擬網路對等至虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="d70ea-117">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="d70ea-118">建立中樞虛擬網路連接之後，它會使用其資源組名和中樞名稱列出所有中樞虛擬網路連接。</span><span class="sxs-lookup"><span data-stu-id="d70ea-118">After the hub virtual network connection is created, it lists all the hub virtual network connection using its resource group name and the hub name.</span></span>

### <span data-ttu-id="d70ea-119">範例 3</span><span class="sxs-lookup"><span data-stu-id="d70ea-119">Example 3</span></span>

```powershell
PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name test*

Name                 : testvnetconnection1
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection1
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
RoutingConfiguration : {
                            "AssociatedRouteTable": {
                                "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                            },
                            "PropagatedRouteTables": {
                                "Labels": [],
                                "Ids": [
                                    {
                                        "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                    }
                                ]
                            },
                            "VnetRoutes": {
                                "StaticRoutes": []
                            }
                        }

Name                 : testvnetconnection2
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection2
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
RoutingConfiguration : {
                            "AssociatedRouteTable": {
                                "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                            },
                            "PropagatedRouteTables": {
                                "Labels": [],
                                "Ids": [
                                    {
                                        "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                    }
                                ]
                            },
                            "VnetRoutes": {
                                "StaticRoutes": []
                            }
                        }
```

<span data-ttu-id="d70ea-120">此 Cmdlet 會使用其資源組名和中樞名稱，列出所有中樞虛擬網路連接，從「測試」開始。</span><span class="sxs-lookup"><span data-stu-id="d70ea-120">This cmdlet lists all the hub virtual network connections starting with "test" using its resource group name and the hub name.</span></span>

## <span data-ttu-id="d70ea-121">參數</span><span class="sxs-lookup"><span data-stu-id="d70ea-121">PARAMETERS</span></span>

### <span data-ttu-id="d70ea-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d70ea-122">-DefaultProfile</span></span>
<span data-ttu-id="d70ea-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d70ea-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d70ea-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="d70ea-124">-Name</span></span>
<span data-ttu-id="d70ea-125">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="d70ea-125">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="d70ea-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d70ea-126">-ParentObject</span></span>
<span data-ttu-id="d70ea-127">父資源。</span><span class="sxs-lookup"><span data-stu-id="d70ea-127">The parent resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d70ea-128">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d70ea-128">-ParentResourceId</span></span>
<span data-ttu-id="d70ea-129">父資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d70ea-129">The parent resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d70ea-130">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="d70ea-130">-ParentResourceName</span></span>
<span data-ttu-id="d70ea-131">父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="d70ea-131">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d70ea-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d70ea-132">-ResourceGroupName</span></span>
<span data-ttu-id="d70ea-133">資源組名。</span><span class="sxs-lookup"><span data-stu-id="d70ea-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d70ea-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d70ea-134">CommonParameters</span></span>
<span data-ttu-id="d70ea-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d70ea-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d70ea-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d70ea-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d70ea-137">輸入</span><span class="sxs-lookup"><span data-stu-id="d70ea-137">INPUTS</span></span>

### <span data-ttu-id="d70ea-138">Microsoft.Azure.Commands.Network.models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="d70ea-138">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="d70ea-139">System.String</span><span class="sxs-lookup"><span data-stu-id="d70ea-139">System.String</span></span>

## <span data-ttu-id="d70ea-140">輸出</span><span class="sxs-lookup"><span data-stu-id="d70ea-140">OUTPUTS</span></span>

### <span data-ttu-id="d70ea-141">Microsoft.Azure.Commands.Network.models.PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="d70ea-141">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="d70ea-142">筆記</span><span class="sxs-lookup"><span data-stu-id="d70ea-142">NOTES</span></span>

## <span data-ttu-id="d70ea-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="d70ea-143">RELATED LINKS</span></span>

[<span data-ttu-id="d70ea-144">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="d70ea-144">New-AzVirtualHubVnetConnection</span></span>](./New-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="d70ea-145">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="d70ea-145">Remove-AzVirtualHubVnetConnection</span></span>](./Remove-AzVirtualHubVnetConnection.md)
