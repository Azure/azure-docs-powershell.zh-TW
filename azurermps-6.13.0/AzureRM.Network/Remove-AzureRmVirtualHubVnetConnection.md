---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualhubvnetConnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualHubVnetConnection.md
ms.openlocfilehash: 3a7c48803f18bf73f75e721296757e37ff89d44c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623553"
---
# <span data-ttu-id="81308-101">Remove-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="81308-101">Remove-AzureRmVirtualHubVnetConnection</span></span>

## <span data-ttu-id="81308-102">摘要</span><span class="sxs-lookup"><span data-stu-id="81308-102">SYNOPSIS</span></span>
<span data-ttu-id="81308-103">Remove-AzureRmVirtualHubVnetConnection Cmdlet 會將對遠端 VNET 的 Azure 虛擬網路連線與中樞 VNET 移除。</span><span class="sxs-lookup"><span data-stu-id="81308-103">The Remove-AzureRmVirtualHubVnetConnection cmdlet removes an Azure Virtual Network Connection which peers a remote VNET to the hub VNET.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81308-104">句法</span><span class="sxs-lookup"><span data-stu-id="81308-104">SYNTAX</span></span>

### <span data-ttu-id="81308-105">ByHubVirtualNetworkConnectionName (預設) </span><span class="sxs-lookup"><span data-stu-id="81308-105">ByHubVirtualNetworkConnectionName (Default)</span></span>
```
Remove-AzureRmVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="81308-106">ByHubVirtualNetworkConnectionObject</span><span class="sxs-lookup"><span data-stu-id="81308-106">ByHubVirtualNetworkConnectionObject</span></span>
```
Remove-AzureRmVirtualHubVnetConnection [-InputObject <PSHubVirtualNetworkConnection>] [-AsJob] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81308-107">ByHubVirtualNetworkConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="81308-107">ByHubVirtualNetworkConnectionResourceId</span></span>
```
Remove-AzureRmVirtualHubVnetConnection -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81308-108">說明</span><span class="sxs-lookup"><span data-stu-id="81308-108">DESCRIPTION</span></span>
<span data-ttu-id="81308-109">Remove-AzureRmVirtualHubVnetConnection Cmdlet 會將對遠端 VNET 的 Azure 虛擬網路連線與中樞 VNET 移除。</span><span class="sxs-lookup"><span data-stu-id="81308-109">The Remove-AzureRmVirtualHubVnetConnection cmdlet removes an Azure Virtual Network Connection which peers a remote VNET to the hub VNET.</span></span>

## <span data-ttu-id="81308-110">示例</span><span class="sxs-lookup"><span data-stu-id="81308-110">EXAMPLES</span></span>

### <span data-ttu-id="81308-111">範例1</span><span class="sxs-lookup"><span data-stu-id="81308-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzureRmVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzureRmVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Remove-AzureRmVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection
```

<span data-ttu-id="81308-112">上述將會在 Azure 中的該資源群組中建立資源群組、虛擬 WAN、虛擬網路、虛擬中心（在美國）。</span><span class="sxs-lookup"><span data-stu-id="81308-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="81308-113">隨後便會建立虛擬網路連線，以將虛擬網路連接到虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="81308-113">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="81308-114">建立中樞虛擬網路連線之後，就會使用其資源群組名稱、中樞名稱和連線名稱來移除中心虛擬網路連線。</span><span class="sxs-lookup"><span data-stu-id="81308-114">After the hub virtual network connection is created, it removes the hub virtual network connection using its resource group name, the hub name and the connection name.</span></span>

### <span data-ttu-id="81308-115">範例2</span><span class="sxs-lookup"><span data-stu-id="81308-115">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzureRmVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzureRmVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Get-AzureRmVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection | Remove-AzureRmHubVnetConnection
```

<span data-ttu-id="81308-116">上述將會在 Azure 中的該資源群組中建立資源群組、虛擬 WAN、虛擬網路、虛擬中心（在美國）。</span><span class="sxs-lookup"><span data-stu-id="81308-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="81308-117">隨後便會建立虛擬網路連線，以將虛擬網路連接到虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="81308-117">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="81308-118">建立中樞虛擬網路連線之後，就會從 AzureRmHubVirtualNetworkConnection 的輸出中使用 powershell 管道來移除中心虛擬網路連線。</span><span class="sxs-lookup"><span data-stu-id="81308-118">After the hub virtual network connection is created, it removes the hub virtual network connection using powershell piping on the output from Get-AzureRmHubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="81308-119">參數</span><span class="sxs-lookup"><span data-stu-id="81308-119">PARAMETERS</span></span>

### <span data-ttu-id="81308-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="81308-120">-AsJob</span></span>
<span data-ttu-id="81308-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="81308-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="81308-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81308-122">-DefaultProfile</span></span>
<span data-ttu-id="81308-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="81308-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81308-124">-Force</span><span class="sxs-lookup"><span data-stu-id="81308-124">-Force</span></span>
<span data-ttu-id="81308-125">若要覆寫資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="81308-125">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="81308-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81308-126">-InputObject</span></span>
<span data-ttu-id="81308-127">要修改的 hubvirtualnetworkconnection 資源。</span><span class="sxs-lookup"><span data-stu-id="81308-127">The hubvirtualnetworkconnection resource to modify.</span></span>

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

### <span data-ttu-id="81308-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="81308-128">-Name</span></span>
<span data-ttu-id="81308-129">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="81308-129">The resource name.</span></span>

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

### <span data-ttu-id="81308-130">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="81308-130">-ParentResourceName</span></span>
<span data-ttu-id="81308-131">父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="81308-131">The parent resource name.</span></span>

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

### <span data-ttu-id="81308-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="81308-132">-PassThru</span></span>
<span data-ttu-id="81308-133">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="81308-133">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="81308-134">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="81308-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="81308-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81308-135">-ResourceGroupName</span></span>
<span data-ttu-id="81308-136">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="81308-136">The resource group name.</span></span>

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

### <span data-ttu-id="81308-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="81308-137">-ResourceId</span></span>
<span data-ttu-id="81308-138">要修改之 hubvirtualnetworkconnection 資源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="81308-138">The resource id of the hubvirtualnetworkconnection resource to modify.</span></span>

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

### <span data-ttu-id="81308-139">-確認</span><span class="sxs-lookup"><span data-stu-id="81308-139">-Confirm</span></span>
<span data-ttu-id="81308-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="81308-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81308-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81308-141">-WhatIf</span></span>
<span data-ttu-id="81308-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="81308-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81308-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="81308-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81308-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81308-144">CommonParameters</span></span>
<span data-ttu-id="81308-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="81308-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81308-146">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="81308-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81308-147">輸入</span><span class="sxs-lookup"><span data-stu-id="81308-147">INPUTS</span></span>

### <span data-ttu-id="81308-148">PSHubVirtualNetworkConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="81308-148">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

### <span data-ttu-id="81308-149">System.object</span><span class="sxs-lookup"><span data-stu-id="81308-149">System.String</span></span>

## <span data-ttu-id="81308-150">輸出</span><span class="sxs-lookup"><span data-stu-id="81308-150">OUTPUTS</span></span>

### <span data-ttu-id="81308-151">System.object</span><span class="sxs-lookup"><span data-stu-id="81308-151">System.Boolean</span></span>

## <span data-ttu-id="81308-152">筆記</span><span class="sxs-lookup"><span data-stu-id="81308-152">NOTES</span></span>

## <span data-ttu-id="81308-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="81308-153">RELATED LINKS</span></span>
