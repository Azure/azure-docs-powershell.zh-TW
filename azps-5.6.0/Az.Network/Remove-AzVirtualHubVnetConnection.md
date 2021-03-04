---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualhubvnetConnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubVnetConnection.md
ms.openlocfilehash: f5a48ec9ac28e13af7aaa763afe72437bed5fda4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915970"
---
# <span data-ttu-id="3c1d3-101">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="3c1d3-101">Remove-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="3c1d3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3c1d3-102">SYNOPSIS</span></span>
<span data-ttu-id="3c1d3-103">此Remove-AzVirtualHubVnetConnection Cmdlet 會移除 Azure 虛擬網路連接，將遠端 VNET 對等至中樞 VNET。</span><span class="sxs-lookup"><span data-stu-id="3c1d3-103">The Remove-AzVirtualHubVnetConnection cmdlet removes an Azure Virtual Network Connection which peers a remote VNET to the hub VNET.</span></span>

## <span data-ttu-id="3c1d3-104">語法</span><span class="sxs-lookup"><span data-stu-id="3c1d3-104">SYNTAX</span></span>

### <span data-ttu-id="3c1d3-105">ByHubVirtualNetworkConnectionName (預設) </span><span class="sxs-lookup"><span data-stu-id="3c1d3-105">ByHubVirtualNetworkConnectionName (Default)</span></span>
```
Remove-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3c1d3-106">ByHubVirtualNetworkConnectionObject</span><span class="sxs-lookup"><span data-stu-id="3c1d3-106">ByHubVirtualNetworkConnectionObject</span></span>
```
Remove-AzVirtualHubVnetConnection [-InputObject <PSHubVirtualNetworkConnection>] [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c1d3-107">ByHubVirtualNetworkConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="3c1d3-107">ByHubVirtualNetworkConnectionResourceId</span></span>
```
Remove-AzVirtualHubVnetConnection -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c1d3-108">描述</span><span class="sxs-lookup"><span data-stu-id="3c1d3-108">DESCRIPTION</span></span>
<span data-ttu-id="3c1d3-109">此Remove-AzVirtualHubVnetConnection Cmdlet 會移除 Azure 虛擬網路連接，將遠端 VNET 對等至中樞 VNET。</span><span class="sxs-lookup"><span data-stu-id="3c1d3-109">The Remove-AzVirtualHubVnetConnection cmdlet removes an Azure Virtual Network Connection which peers a remote VNET to the hub VNET.</span></span>

## <span data-ttu-id="3c1d3-110">例子</span><span class="sxs-lookup"><span data-stu-id="3c1d3-110">EXAMPLES</span></span>

### <span data-ttu-id="3c1d3-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="3c1d3-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Remove-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection
```

<span data-ttu-id="3c1d3-112">上述步驟將在 Azure 的資源群組中，建立資源群組、虛擬 WAN、虛擬網路、美國中心的虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="3c1d3-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="3c1d3-113">在此之後，將會建立一個虛擬網路連接，將虛擬網路對等至虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="3c1d3-113">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="3c1d3-114">中樞虛擬網路連接建立後，會使用其資源組名、中樞名稱和連接名稱，移除中樞虛擬網路連接。</span><span class="sxs-lookup"><span data-stu-id="3c1d3-114">After the hub virtual network connection is created, it removes the hub virtual network connection using its resource group name, the hub name and the connection name.</span></span>

### <span data-ttu-id="3c1d3-115">範例 2</span><span class="sxs-lookup"><span data-stu-id="3c1d3-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection | Remove-AzHubVnetConnection
```

<span data-ttu-id="3c1d3-116">上述步驟將在 Azure 的資源群組中，建立資源群組、虛擬 WAN、虛擬網路、美國中心的虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="3c1d3-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="3c1d3-117">在此之後，將會建立一個虛擬網路連接，將虛擬網路對等至虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="3c1d3-117">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="3c1d3-118">中樞虛擬網路連接建立之後，它會使用 Get-AzHubVirtualNetworkConnection 輸出上的 Powershell 管線移除中樞虛擬網路連接。</span><span class="sxs-lookup"><span data-stu-id="3c1d3-118">After the hub virtual network connection is created, it removes the hub virtual network connection using powershell piping on the output from Get-AzHubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="3c1d3-119">參數</span><span class="sxs-lookup"><span data-stu-id="3c1d3-119">PARAMETERS</span></span>

### <span data-ttu-id="3c1d3-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c1d3-120">-AsJob</span></span>
<span data-ttu-id="3c1d3-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3c1d3-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3c1d3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c1d3-122">-DefaultProfile</span></span>
<span data-ttu-id="3c1d3-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3c1d3-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c1d3-124">-強制</span><span class="sxs-lookup"><span data-stu-id="3c1d3-124">-Force</span></span>
<span data-ttu-id="3c1d3-125">如果您想要覆寫資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="3c1d3-125">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="3c1d3-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c1d3-126">-InputObject</span></span>
<span data-ttu-id="3c1d3-127">要修改的 hubvirtualnetworkconnection 資源。</span><span class="sxs-lookup"><span data-stu-id="3c1d3-127">The hubvirtualnetworkconnection resource to modify.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection
Parameter Sets: ByHubVirtualNetworkConnectionObject
Aliases: HubVirtualNetworkConnection

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c1d3-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="3c1d3-128">-Name</span></span>
<span data-ttu-id="3c1d3-129">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="3c1d3-129">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c1d3-130">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="3c1d3-130">-ParentResourceName</span></span>
<span data-ttu-id="3c1d3-131">父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="3c1d3-131">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c1d3-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3c1d3-132">-PassThru</span></span>
<span data-ttu-id="3c1d3-133">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="3c1d3-133">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3c1d3-134">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="3c1d3-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3c1d3-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c1d3-135">-ResourceGroupName</span></span>
<span data-ttu-id="3c1d3-136">資源組名。</span><span class="sxs-lookup"><span data-stu-id="3c1d3-136">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c1d3-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c1d3-137">-ResourceId</span></span>
<span data-ttu-id="3c1d3-138">hubvirtualnetworkconnection 資源要修改的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="3c1d3-138">The resource id of the hubvirtualnetworkconnection resource to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionResourceId
Aliases: HubVirtualNetworkConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c1d3-139">-確認</span><span class="sxs-lookup"><span data-stu-id="3c1d3-139">-Confirm</span></span>
<span data-ttu-id="3c1d3-140">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3c1d3-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c1d3-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c1d3-141">-WhatIf</span></span>
<span data-ttu-id="3c1d3-142">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3c1d3-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c1d3-143">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3c1d3-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c1d3-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c1d3-144">CommonParameters</span></span>
<span data-ttu-id="3c1d3-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3c1d3-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c1d3-146">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="3c1d3-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c1d3-147">輸入</span><span class="sxs-lookup"><span data-stu-id="3c1d3-147">INPUTS</span></span>

### <span data-ttu-id="3c1d3-148">Microsoft.Azure.Commands.Network.models.PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="3c1d3-148">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

### <span data-ttu-id="3c1d3-149">System.String</span><span class="sxs-lookup"><span data-stu-id="3c1d3-149">System.String</span></span>

## <span data-ttu-id="3c1d3-150">輸出</span><span class="sxs-lookup"><span data-stu-id="3c1d3-150">OUTPUTS</span></span>

### <span data-ttu-id="3c1d3-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3c1d3-151">System.Boolean</span></span>

## <span data-ttu-id="3c1d3-152">筆記</span><span class="sxs-lookup"><span data-stu-id="3c1d3-152">NOTES</span></span>

## <span data-ttu-id="3c1d3-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="3c1d3-153">RELATED LINKS</span></span>

[<span data-ttu-id="3c1d3-154">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="3c1d3-154">Get-AzVirtualHubVnetConnection</span></span>](./Get-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="3c1d3-155">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="3c1d3-155">New-AzVirtualHubVnetConnection</span></span>](./New-AzVirtualHubVnetConnection.md)
