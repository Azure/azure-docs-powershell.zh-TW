---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualhubvnetConnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubVnetConnection.md
ms.openlocfilehash: 16a17ed437194963f3cfd715a6e5364c8f4348c4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93790590"
---
# <span data-ttu-id="b120d-101">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="b120d-101">Remove-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="b120d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b120d-102">SYNOPSIS</span></span>
<span data-ttu-id="b120d-103">Remove-AzVirtualHubVnetConnection Cmdlet 會將對遠端 VNET 的 Azure 虛擬網路連線與中樞 VNET 移除。</span><span class="sxs-lookup"><span data-stu-id="b120d-103">The Remove-AzVirtualHubVnetConnection cmdlet removes an Azure Virtual Network Connection which peers a remote VNET to the hub VNET.</span></span>

## <span data-ttu-id="b120d-104">句法</span><span class="sxs-lookup"><span data-stu-id="b120d-104">SYNTAX</span></span>

### <span data-ttu-id="b120d-105">ByHubVirtualNetworkConnectionName (預設) </span><span class="sxs-lookup"><span data-stu-id="b120d-105">ByHubVirtualNetworkConnectionName (Default)</span></span>
```
Remove-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b120d-106">ByHubVirtualNetworkConnectionObject</span><span class="sxs-lookup"><span data-stu-id="b120d-106">ByHubVirtualNetworkConnectionObject</span></span>
```
Remove-AzVirtualHubVnetConnection [-InputObject <PSHubVirtualNetworkConnection>] [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b120d-107">ByHubVirtualNetworkConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="b120d-107">ByHubVirtualNetworkConnectionResourceId</span></span>
```
Remove-AzVirtualHubVnetConnection -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b120d-108">說明</span><span class="sxs-lookup"><span data-stu-id="b120d-108">DESCRIPTION</span></span>
<span data-ttu-id="b120d-109">Remove-AzVirtualHubVnetConnection Cmdlet 會將對遠端 VNET 的 Azure 虛擬網路連線與中樞 VNET 移除。</span><span class="sxs-lookup"><span data-stu-id="b120d-109">The Remove-AzVirtualHubVnetConnection cmdlet removes an Azure Virtual Network Connection which peers a remote VNET to the hub VNET.</span></span>

## <span data-ttu-id="b120d-110">示例</span><span class="sxs-lookup"><span data-stu-id="b120d-110">EXAMPLES</span></span>

### <span data-ttu-id="b120d-111">範例1</span><span class="sxs-lookup"><span data-stu-id="b120d-111">Example 1</span></span>

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

<span data-ttu-id="b120d-112">上述將會在 Azure 中的該資源群組中建立資源群組、虛擬 WAN、虛擬網路、虛擬中心（在美國）。</span><span class="sxs-lookup"><span data-stu-id="b120d-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="b120d-113">隨後便會建立虛擬網路連線，以將虛擬網路連接到虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="b120d-113">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="b120d-114">建立中樞虛擬網路連線之後，就會使用其資源群組名稱、中樞名稱和連線名稱來移除中心虛擬網路連線。</span><span class="sxs-lookup"><span data-stu-id="b120d-114">After the hub virtual network connection is created, it removes the hub virtual network connection using its resource group name, the hub name and the connection name.</span></span>

### <span data-ttu-id="b120d-115">範例2</span><span class="sxs-lookup"><span data-stu-id="b120d-115">Example 2</span></span>

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

<span data-ttu-id="b120d-116">上述將會在 Azure 中的該資源群組中建立資源群組、虛擬 WAN、虛擬網路、虛擬中心（在美國）。</span><span class="sxs-lookup"><span data-stu-id="b120d-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="b120d-117">隨後便會建立虛擬網路連線，以將虛擬網路連接到虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="b120d-117">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="b120d-118">建立中樞虛擬網路連線之後，就會從 AzHubVirtualNetworkConnection 的輸出中使用 powershell 管道來移除中心虛擬網路連線。</span><span class="sxs-lookup"><span data-stu-id="b120d-118">After the hub virtual network connection is created, it removes the hub virtual network connection using powershell piping on the output from Get-AzHubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="b120d-119">參數</span><span class="sxs-lookup"><span data-stu-id="b120d-119">PARAMETERS</span></span>

### <span data-ttu-id="b120d-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b120d-120">-AsJob</span></span>
<span data-ttu-id="b120d-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b120d-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b120d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b120d-122">-DefaultProfile</span></span>
<span data-ttu-id="b120d-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b120d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b120d-124">-Force</span><span class="sxs-lookup"><span data-stu-id="b120d-124">-Force</span></span>
<span data-ttu-id="b120d-125">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="b120d-125">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="b120d-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b120d-126">-InputObject</span></span>
<span data-ttu-id="b120d-127">要修改的 hubvirtualnetworkconnection 資源。</span><span class="sxs-lookup"><span data-stu-id="b120d-127">The hubvirtualnetworkconnection resource to modify.</span></span>

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

### <span data-ttu-id="b120d-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="b120d-128">-Name</span></span>
<span data-ttu-id="b120d-129">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="b120d-129">The resource name.</span></span>

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

### <span data-ttu-id="b120d-130">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="b120d-130">-ParentResourceName</span></span>
<span data-ttu-id="b120d-131">父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="b120d-131">The parent resource name.</span></span>

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

### <span data-ttu-id="b120d-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b120d-132">-PassThru</span></span>
<span data-ttu-id="b120d-133">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="b120d-133">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b120d-134">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="b120d-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b120d-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b120d-135">-ResourceGroupName</span></span>
<span data-ttu-id="b120d-136">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b120d-136">The resource group name.</span></span>

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

### <span data-ttu-id="b120d-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b120d-137">-ResourceId</span></span>
<span data-ttu-id="b120d-138">要修改之 hubvirtualnetworkconnection 資源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b120d-138">The resource id of the hubvirtualnetworkconnection resource to modify.</span></span>

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

### <span data-ttu-id="b120d-139">-確認</span><span class="sxs-lookup"><span data-stu-id="b120d-139">-Confirm</span></span>
<span data-ttu-id="b120d-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b120d-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b120d-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b120d-141">-WhatIf</span></span>
<span data-ttu-id="b120d-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b120d-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b120d-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b120d-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b120d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b120d-144">CommonParameters</span></span>
<span data-ttu-id="b120d-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b120d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b120d-146">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b120d-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b120d-147">輸入</span><span class="sxs-lookup"><span data-stu-id="b120d-147">INPUTS</span></span>

### <span data-ttu-id="b120d-148">PSHubVirtualNetworkConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b120d-148">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

### <span data-ttu-id="b120d-149">System.object</span><span class="sxs-lookup"><span data-stu-id="b120d-149">System.String</span></span>

## <span data-ttu-id="b120d-150">輸出</span><span class="sxs-lookup"><span data-stu-id="b120d-150">OUTPUTS</span></span>

### <span data-ttu-id="b120d-151">System.object</span><span class="sxs-lookup"><span data-stu-id="b120d-151">System.Boolean</span></span>

## <span data-ttu-id="b120d-152">筆記</span><span class="sxs-lookup"><span data-stu-id="b120d-152">NOTES</span></span>

## <span data-ttu-id="b120d-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="b120d-153">RELATED LINKS</span></span>

[<span data-ttu-id="b120d-154">AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="b120d-154">Get-AzVirtualHubVnetConnection</span></span>](./Get-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="b120d-155">新-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="b120d-155">New-AzVirtualHubVnetConnection</span></span>](./New-AzVirtualHubVnetConnection.md)
