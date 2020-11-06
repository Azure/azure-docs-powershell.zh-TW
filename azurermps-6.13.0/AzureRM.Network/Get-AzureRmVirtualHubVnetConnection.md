---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualHubVnetConnection.md
ms.openlocfilehash: 8aeb992b08e2749168ef3da2db6c264158c6a9ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447355"
---
# <span data-ttu-id="416bb-101">Get-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="416bb-101">Get-AzureRmVirtualHubVnetConnection</span></span>

## <span data-ttu-id="416bb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="416bb-102">SYNOPSIS</span></span>
<span data-ttu-id="416bb-103">在虛擬中樞中取得虛擬網路連線，或列出虛擬中樞中的所有虛擬網路連線。</span><span class="sxs-lookup"><span data-stu-id="416bb-103">Gets a Virtual Network Connection in a virtual hub or lists all virtual network connections in a virtual hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="416bb-104">句法</span><span class="sxs-lookup"><span data-stu-id="416bb-104">SYNTAX</span></span>

### <span data-ttu-id="416bb-105">ByVirtualHubName (預設) </span><span class="sxs-lookup"><span data-stu-id="416bb-105">ByVirtualHubName (Default)</span></span>
```
Get-AzureRmVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="416bb-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="416bb-106">ByVirtualHubObject</span></span>
```
Get-AzureRmVirtualHubVnetConnection -ParentObject <PSVirtualHub> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="416bb-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="416bb-107">ByVirtualHubResourceId</span></span>
```
Get-AzureRmVirtualHubVnetConnection -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="416bb-108">說明</span><span class="sxs-lookup"><span data-stu-id="416bb-108">DESCRIPTION</span></span>
<span data-ttu-id="416bb-109">在虛擬中樞中取得虛擬網路連線，或列出虛擬中樞中的所有虛擬網路連線。</span><span class="sxs-lookup"><span data-stu-id="416bb-109">Gets a Virtual Network Connection in a virtual hub or lists all virtual network connections in a virtual hub.</span></span>

## <span data-ttu-id="416bb-110">示例</span><span class="sxs-lookup"><span data-stu-id="416bb-110">EXAMPLES</span></span>

### <span data-ttu-id="416bb-111">範例1</span><span class="sxs-lookup"><span data-stu-id="416bb-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzureRmVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet

PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzureRmVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork

PS C:\> Get-AzureRmVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
```

<span data-ttu-id="416bb-112">上述將會在 Azure 中的該資源群組中建立資源群組、虛擬 WAN、虛擬網路、虛擬中心（在美國）。</span><span class="sxs-lookup"><span data-stu-id="416bb-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="416bb-113">隨後便會建立虛擬網路連線，以將虛擬網路連接到虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="416bb-113">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="416bb-114">建立中樞虛擬網路連線之後，就會使用其資源組名、中樞名稱和連線名稱來取得中樞虛擬網路連線。</span><span class="sxs-lookup"><span data-stu-id="416bb-114">After the hub virtual network connection is created, it gets the hub virtual network connection using its resource group name, the hub name and the connection name.</span></span>

### <span data-ttu-id="416bb-115">範例2</span><span class="sxs-lookup"><span data-stu-id="416bb-115">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzureRmVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzureRmVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Get-AzureRmVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
```

<span data-ttu-id="416bb-116">上述將會在 Azure 中的該資源群組中建立資源群組、虛擬 WAN、虛擬網路、虛擬中心（在美國）。</span><span class="sxs-lookup"><span data-stu-id="416bb-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="416bb-117">隨後便會建立虛擬網路連線，以將虛擬網路連接到虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="416bb-117">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="416bb-118">建立中樞虛擬網路連線之後，它會使用其資源群組名稱和中樞名稱列出所有中樞虛擬網路連線。</span><span class="sxs-lookup"><span data-stu-id="416bb-118">After the hub virtual network connection is created, it lists all the hub virtual network connection using its resource group name and the hub name.</span></span>

## <span data-ttu-id="416bb-119">參數</span><span class="sxs-lookup"><span data-stu-id="416bb-119">PARAMETERS</span></span>

### <span data-ttu-id="416bb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="416bb-120">-DefaultProfile</span></span>
<span data-ttu-id="416bb-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="416bb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="416bb-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="416bb-122">-Name</span></span>
<span data-ttu-id="416bb-123">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="416bb-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="416bb-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="416bb-124">-ParentObject</span></span>
<span data-ttu-id="416bb-125">[父資源]。</span><span class="sxs-lookup"><span data-stu-id="416bb-125">The parent resource.</span></span>

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

### <span data-ttu-id="416bb-126">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="416bb-126">-ParentResourceId</span></span>
<span data-ttu-id="416bb-127">[父資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="416bb-127">The parent resource id.</span></span>

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

### <span data-ttu-id="416bb-128">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="416bb-128">-ParentResourceName</span></span>
<span data-ttu-id="416bb-129">父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="416bb-129">The parent resource name.</span></span>

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

### <span data-ttu-id="416bb-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="416bb-130">-ResourceGroupName</span></span>
<span data-ttu-id="416bb-131">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="416bb-131">The resource group name.</span></span>

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

### <span data-ttu-id="416bb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="416bb-132">CommonParameters</span></span>
<span data-ttu-id="416bb-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="416bb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="416bb-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="416bb-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="416bb-135">輸入</span><span class="sxs-lookup"><span data-stu-id="416bb-135">INPUTS</span></span>

### <span data-ttu-id="416bb-136">所有</span><span class="sxs-lookup"><span data-stu-id="416bb-136">None</span></span>

## <span data-ttu-id="416bb-137">輸出</span><span class="sxs-lookup"><span data-stu-id="416bb-137">OUTPUTS</span></span>

### <span data-ttu-id="416bb-138">PSHubVirtualNetworkConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="416bb-138">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="416bb-139">筆記</span><span class="sxs-lookup"><span data-stu-id="416bb-139">NOTES</span></span>

## <span data-ttu-id="416bb-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="416bb-140">RELATED LINKS</span></span>
