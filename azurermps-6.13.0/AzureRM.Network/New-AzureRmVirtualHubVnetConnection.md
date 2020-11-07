---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualHubVnetConnection.md
ms.openlocfilehash: 6805d6671d0335599dc95f206ddb8482867734fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624594"
---
# <span data-ttu-id="71a1a-101">New-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="71a1a-101">New-AzureRmVirtualHubVnetConnection</span></span>

## <span data-ttu-id="71a1a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="71a1a-102">SYNOPSIS</span></span>
<span data-ttu-id="71a1a-103">New-AzureRmVirtualHubVnetConnection Cmdlet 會建立對 Azure 虛擬中樞擁有虛擬網路的 HubVirtualNetworkConnection 資源。</span><span class="sxs-lookup"><span data-stu-id="71a1a-103">The New-AzureRmVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71a1a-104">句法</span><span class="sxs-lookup"><span data-stu-id="71a1a-104">SYNTAX</span></span>

### <span data-ttu-id="71a1a-105">ByVirtualHubNameByRemoteVirtualNetworkObject (預設) </span><span class="sxs-lookup"><span data-stu-id="71a1a-105">ByVirtualHubNameByRemoteVirtualNetworkObject (Default)</span></span>
```
New-AzureRmVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71a1a-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="71a1a-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span></span>
```
New-AzureRmVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="71a1a-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="71a1a-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span></span>
```
New-AzureRmVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71a1a-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="71a1a-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span></span>
```
New-AzureRmVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String>
 -RemoteVirtualNetworkId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="71a1a-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="71a1a-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span></span>
```
New-AzureRmVirtualHubVnetConnection -ParentResourceId <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71a1a-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="71a1a-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span></span>
```
New-AzureRmVirtualHubVnetConnection -ParentResourceId <String> -Name <String> -RemoteVirtualNetworkId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71a1a-111">說明</span><span class="sxs-lookup"><span data-stu-id="71a1a-111">DESCRIPTION</span></span>
<span data-ttu-id="71a1a-112">New-AzureRmVirtualHubVnetConnection Cmdlet 會建立對 Azure 虛擬中樞擁有虛擬網路的 HubVirtualNetworkConnection 資源。</span><span class="sxs-lookup"><span data-stu-id="71a1a-112">The New-AzureRmVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="71a1a-113">示例</span><span class="sxs-lookup"><span data-stu-id="71a1a-113">EXAMPLES</span></span>

### <span data-ttu-id="71a1a-114">範例1</span><span class="sxs-lookup"><span data-stu-id="71a1a-114">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzureRmVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzureRmVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
```

<span data-ttu-id="71a1a-115">上述將會在 Azure 中的該資源群組中建立資源群組、虛擬 WAN、虛擬網路、虛擬中心（在美國）。</span><span class="sxs-lookup"><span data-stu-id="71a1a-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="71a1a-116">隨後便會建立虛擬網路連線，以將虛擬網路連接到虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="71a1a-116">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

## <span data-ttu-id="71a1a-117">參數</span><span class="sxs-lookup"><span data-stu-id="71a1a-117">PARAMETERS</span></span>

### <span data-ttu-id="71a1a-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71a1a-118">-AsJob</span></span>
<span data-ttu-id="71a1a-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="71a1a-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="71a1a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71a1a-120">-DefaultProfile</span></span>
<span data-ttu-id="71a1a-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="71a1a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71a1a-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="71a1a-122">-Name</span></span>
<span data-ttu-id="71a1a-123">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="71a1a-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71a1a-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="71a1a-124">-ParentObject</span></span>
<span data-ttu-id="71a1a-125">[父資源]。</span><span class="sxs-lookup"><span data-stu-id="71a1a-125">The parent resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkResourceId
Aliases: VirtualHub, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71a1a-126">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="71a1a-126">-ParentResourceId</span></span>
<span data-ttu-id="71a1a-127">[父資源]。</span><span class="sxs-lookup"><span data-stu-id="71a1a-127">The parent resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceIdByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71a1a-128">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="71a1a-128">-ParentResourceName</span></span>
<span data-ttu-id="71a1a-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="71a1a-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71a1a-130">-RemoteVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="71a1a-130">-RemoteVirtualNetwork</span></span>
<span data-ttu-id="71a1a-131">此中樞虛擬網路連線所連結的遠端虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="71a1a-131">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71a1a-132">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="71a1a-132">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="71a1a-133">此中樞虛擬網路連線所連結的遠端虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="71a1a-133">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkResourceId, ByVirtualHubObjectByRemoteVirtualNetworkResourceId, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71a1a-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71a1a-134">-ResourceGroupName</span></span>
<span data-ttu-id="71a1a-135">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="71a1a-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71a1a-136">-確認</span><span class="sxs-lookup"><span data-stu-id="71a1a-136">-Confirm</span></span>
<span data-ttu-id="71a1a-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="71a1a-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71a1a-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71a1a-138">-WhatIf</span></span>
<span data-ttu-id="71a1a-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="71a1a-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71a1a-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="71a1a-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71a1a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71a1a-141">CommonParameters</span></span>
<span data-ttu-id="71a1a-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="71a1a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71a1a-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="71a1a-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71a1a-144">輸入</span><span class="sxs-lookup"><span data-stu-id="71a1a-144">INPUTS</span></span>

### <span data-ttu-id="71a1a-145">PSVirtualHub 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="71a1a-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="71a1a-146">System.object</span><span class="sxs-lookup"><span data-stu-id="71a1a-146">System.String</span></span>

## <span data-ttu-id="71a1a-147">輸出</span><span class="sxs-lookup"><span data-stu-id="71a1a-147">OUTPUTS</span></span>

### <span data-ttu-id="71a1a-148">PSHubVirtualNetworkConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="71a1a-148">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="71a1a-149">筆記</span><span class="sxs-lookup"><span data-stu-id="71a1a-149">NOTES</span></span>

## <span data-ttu-id="71a1a-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="71a1a-150">RELATED LINKS</span></span>
