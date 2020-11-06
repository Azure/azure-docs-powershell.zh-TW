---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubVnetConnection.md
ms.openlocfilehash: 79bf22b5da9426ccb895b42faaeb4b01036828aa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621935"
---
# <span data-ttu-id="24ace-101">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="24ace-101">Get-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="24ace-102">摘要</span><span class="sxs-lookup"><span data-stu-id="24ace-102">SYNOPSIS</span></span>
<span data-ttu-id="24ace-103">在虛擬中樞中取得虛擬網路連線，或列出虛擬中樞中的所有虛擬網路連線。</span><span class="sxs-lookup"><span data-stu-id="24ace-103">Gets a Virtual Network Connection in a virtual hub or lists all virtual network connections in a virtual hub.</span></span>

## <span data-ttu-id="24ace-104">句法</span><span class="sxs-lookup"><span data-stu-id="24ace-104">SYNTAX</span></span>

### <span data-ttu-id="24ace-105">ByVirtualHubName (預設) </span><span class="sxs-lookup"><span data-stu-id="24ace-105">ByVirtualHubName (Default)</span></span>
```
Get-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24ace-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="24ace-106">ByVirtualHubObject</span></span>
```
Get-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24ace-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="24ace-107">ByVirtualHubResourceId</span></span>
```
Get-AzVirtualHubVnetConnection -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24ace-108">說明</span><span class="sxs-lookup"><span data-stu-id="24ace-108">DESCRIPTION</span></span>
<span data-ttu-id="24ace-109">在虛擬中樞中取得虛擬網路連線，或列出虛擬中樞中的所有虛擬網路連線。</span><span class="sxs-lookup"><span data-stu-id="24ace-109">Gets a Virtual Network Connection in a virtual hub or lists all virtual network connections in a virtual hub.</span></span>

## <span data-ttu-id="24ace-110">示例</span><span class="sxs-lookup"><span data-stu-id="24ace-110">EXAMPLES</span></span>

### <span data-ttu-id="24ace-111">範例1</span><span class="sxs-lookup"><span data-stu-id="24ace-111">Example 1</span></span>
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
```

<span data-ttu-id="24ace-112">上述將會在 Azure 中的該資源群組中建立資源群組、虛擬 WAN、虛擬網路、虛擬中心（在美國）。</span><span class="sxs-lookup"><span data-stu-id="24ace-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="24ace-113">隨後便會建立虛擬網路連線，以將虛擬網路連接到虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="24ace-113">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="24ace-114">建立中樞虛擬網路連線之後，就會使用其資源組名、中樞名稱和連線名稱來取得中樞虛擬網路連線。</span><span class="sxs-lookup"><span data-stu-id="24ace-114">After the hub virtual network connection is created, it gets the hub virtual network connection using its resource group name, the hub name and the connection name.</span></span>

### <span data-ttu-id="24ace-115">範例2</span><span class="sxs-lookup"><span data-stu-id="24ace-115">Example 2</span></span>

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
```

<span data-ttu-id="24ace-116">上述將會在 Azure 中的該資源群組中建立資源群組、虛擬 WAN、虛擬網路、虛擬中心（在美國）。</span><span class="sxs-lookup"><span data-stu-id="24ace-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="24ace-117">隨後便會建立虛擬網路連線，以將虛擬網路連接到虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="24ace-117">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="24ace-118">建立中樞虛擬網路連線之後，它會使用其資源群組名稱和中樞名稱列出所有中樞虛擬網路連線。</span><span class="sxs-lookup"><span data-stu-id="24ace-118">After the hub virtual network connection is created, it lists all the hub virtual network connection using its resource group name and the hub name.</span></span>

### <span data-ttu-id="24ace-119">範例3</span><span class="sxs-lookup"><span data-stu-id="24ace-119">Example 3</span></span>

```powershell
PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name test*

Name                 : testvnetconnection1
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection1
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded

Name                 : testvnetconnection2
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection2
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
```

<span data-ttu-id="24ace-120">這個 Cmdlet 會列出所有以「test」開始、使用其資源群組名稱和中樞名稱的中心虛擬網路連線。</span><span class="sxs-lookup"><span data-stu-id="24ace-120">This cmdlet lists all the hub virtual network connections starting with "test" using its resource group name and the hub name.</span></span>

## <span data-ttu-id="24ace-121">參數</span><span class="sxs-lookup"><span data-stu-id="24ace-121">PARAMETERS</span></span>

### <span data-ttu-id="24ace-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24ace-122">-DefaultProfile</span></span>
<span data-ttu-id="24ace-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="24ace-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24ace-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="24ace-124">-Name</span></span>
<span data-ttu-id="24ace-125">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="24ace-125">The resource name.</span></span>

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

### <span data-ttu-id="24ace-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="24ace-126">-ParentObject</span></span>
<span data-ttu-id="24ace-127">[父資源]。</span><span class="sxs-lookup"><span data-stu-id="24ace-127">The parent resource.</span></span>

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

### <span data-ttu-id="24ace-128">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="24ace-128">-ParentResourceId</span></span>
<span data-ttu-id="24ace-129">[父資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="24ace-129">The parent resource id.</span></span>

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

### <span data-ttu-id="24ace-130">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="24ace-130">-ParentResourceName</span></span>
<span data-ttu-id="24ace-131">父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="24ace-131">The parent resource name.</span></span>

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

### <span data-ttu-id="24ace-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24ace-132">-ResourceGroupName</span></span>
<span data-ttu-id="24ace-133">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="24ace-133">The resource group name.</span></span>

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

### <span data-ttu-id="24ace-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24ace-134">CommonParameters</span></span>
<span data-ttu-id="24ace-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="24ace-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24ace-136">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="24ace-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24ace-137">輸入</span><span class="sxs-lookup"><span data-stu-id="24ace-137">INPUTS</span></span>

### <span data-ttu-id="24ace-138">PSVirtualHub 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="24ace-138">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="24ace-139">System.object</span><span class="sxs-lookup"><span data-stu-id="24ace-139">System.String</span></span>

## <span data-ttu-id="24ace-140">輸出</span><span class="sxs-lookup"><span data-stu-id="24ace-140">OUTPUTS</span></span>

### <span data-ttu-id="24ace-141">PSHubVirtualNetworkConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="24ace-141">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="24ace-142">筆記</span><span class="sxs-lookup"><span data-stu-id="24ace-142">NOTES</span></span>

## <span data-ttu-id="24ace-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="24ace-143">RELATED LINKS</span></span>

[<span data-ttu-id="24ace-144">新-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="24ace-144">New-AzVirtualHubVnetConnection</span></span>](./New-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="24ace-145">移除-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="24ace-145">Remove-AzVirtualHubVnetConnection</span></span>](./Remove-AzVirtualHubVnetConnection.md)
