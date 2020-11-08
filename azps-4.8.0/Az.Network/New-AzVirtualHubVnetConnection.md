---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
ms.openlocfilehash: e9156887f328242f8c4896dc707a1814f58f2869
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94135807"
---
# <span data-ttu-id="dbfde-101">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="dbfde-101">New-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="dbfde-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dbfde-102">SYNOPSIS</span></span>
<span data-ttu-id="dbfde-103">New-AzVirtualHubVnetConnection Cmdlet 會建立對 Azure 虛擬中樞擁有虛擬網路的 HubVirtualNetworkConnection 資源。</span><span class="sxs-lookup"><span data-stu-id="dbfde-103">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="dbfde-104">句法</span><span class="sxs-lookup"><span data-stu-id="dbfde-104">SYNTAX</span></span>

### <span data-ttu-id="dbfde-105">ByVirtualHubNameByRemoteVirtualNetworkObject (預設) </span><span class="sxs-lookup"><span data-stu-id="dbfde-105">ByVirtualHubNameByRemoteVirtualNetworkObject (Default)</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbfde-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="dbfde-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbfde-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="dbfde-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbfde-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="dbfde-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dbfde-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="dbfde-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbfde-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="dbfde-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dbfde-111">說明</span><span class="sxs-lookup"><span data-stu-id="dbfde-111">DESCRIPTION</span></span>
<span data-ttu-id="dbfde-112">New-AzVirtualHubVnetConnection Cmdlet 會建立對 Azure 虛擬中樞擁有虛擬網路的 HubVirtualNetworkConnection 資源。</span><span class="sxs-lookup"><span data-stu-id="dbfde-112">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="dbfde-113">示例</span><span class="sxs-lookup"><span data-stu-id="dbfde-113">EXAMPLES</span></span>

### <span data-ttu-id="dbfde-114">範例1</span><span class="sxs-lookup"><span data-stu-id="dbfde-114">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
EnableInternetSecurity : False
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

<span data-ttu-id="dbfde-115">上述將會在 Azure 中的該資源群組中建立資源群組、虛擬 WAN、虛擬網路、虛擬中心（在美國）。</span><span class="sxs-lookup"><span data-stu-id="dbfde-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="dbfde-116">隨後便會建立虛擬網路連線，以將虛擬網路連接到虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="dbfde-116">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

### <span data-ttu-id="dbfde-117">範例2</span><span class="sxs-lookup"><span data-stu-id="dbfde-117">Example 2</span></span>

<span data-ttu-id="dbfde-118">New-AzVirtualHubVnetConnection Cmdlet 會建立對 Azure 虛擬中樞擁有虛擬網路的 HubVirtualNetworkConnection 資源。</span><span class="sxs-lookup"><span data-stu-id="dbfde-118">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span> <span data-ttu-id="dbfde-119"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="dbfde-119">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVirtualHubVnetConnection -EnableInternetSecurity -Name 'testvnetconnection' -ParentResourceName 'westushub' -RemoteVirtualNetwork <PSVirtualNetwork> -ResourceGroupName 'testRG'
```

## <span data-ttu-id="dbfde-120">參數</span><span class="sxs-lookup"><span data-stu-id="dbfde-120">PARAMETERS</span></span>

### <span data-ttu-id="dbfde-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dbfde-121">-AsJob</span></span>
<span data-ttu-id="dbfde-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="dbfde-122">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbfde-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbfde-123">-DefaultProfile</span></span>
<span data-ttu-id="dbfde-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dbfde-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbfde-125">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="dbfde-125">-EnableInternetSecurity</span></span>
<span data-ttu-id="dbfde-126">針對此連線啟用網際網路安全性</span><span class="sxs-lookup"><span data-stu-id="dbfde-126">Enable internet security for this connection</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbfde-127">-EnableInternetSecurityFlag</span><span class="sxs-lookup"><span data-stu-id="dbfde-127">-EnableInternetSecurityFlag</span></span>
<span data-ttu-id="dbfde-128">針對此連線啟用網際網路安全性</span><span class="sxs-lookup"><span data-stu-id="dbfde-128">Enable internet security for this connection</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbfde-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="dbfde-129">-Name</span></span>
<span data-ttu-id="dbfde-130">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="dbfde-130">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbfde-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="dbfde-131">-ParentObject</span></span>
<span data-ttu-id="dbfde-132">[父資源]。</span><span class="sxs-lookup"><span data-stu-id="dbfde-132">The parent resource.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkResourceId
Aliases: VirtualHub, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dbfde-133">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="dbfde-133">-ParentResourceId</span></span>
<span data-ttu-id="dbfde-134">[父資源]。</span><span class="sxs-lookup"><span data-stu-id="dbfde-134">The parent resource.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceIdByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbfde-135">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="dbfde-135">-ParentResourceName</span></span>
<span data-ttu-id="dbfde-136">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dbfde-136">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbfde-137">-RemoteVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="dbfde-137">-RemoteVirtualNetwork</span></span>
<span data-ttu-id="dbfde-138">此中樞虛擬網路連線所連結的遠端虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="dbfde-138">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbfde-139">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="dbfde-139">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="dbfde-140">此中樞虛擬網路連線所連結的遠端虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="dbfde-140">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkResourceId, ByVirtualHubObjectByRemoteVirtualNetworkResourceId, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbfde-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbfde-141">-ResourceGroupName</span></span>
<span data-ttu-id="dbfde-142">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dbfde-142">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbfde-143">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="dbfde-143">-RoutingConfiguration</span></span>
<span data-ttu-id="dbfde-144">此連線的路由設定</span><span class="sxs-lookup"><span data-stu-id="dbfde-144">Routing configuration for this connection</span></span>

```yaml
Type: PSRoutingConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbfde-145">-確認</span><span class="sxs-lookup"><span data-stu-id="dbfde-145">-Confirm</span></span>
<span data-ttu-id="dbfde-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dbfde-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbfde-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbfde-147">-WhatIf</span></span>
<span data-ttu-id="dbfde-148">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dbfde-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbfde-149">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dbfde-149">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbfde-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbfde-150">CommonParameters</span></span>
<span data-ttu-id="dbfde-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dbfde-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbfde-152">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="dbfde-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbfde-153">輸入</span><span class="sxs-lookup"><span data-stu-id="dbfde-153">INPUTS</span></span>

### <span data-ttu-id="dbfde-154">PSVirtualHub 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="dbfde-154">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="dbfde-155">System.object</span><span class="sxs-lookup"><span data-stu-id="dbfde-155">System.String</span></span>

## <span data-ttu-id="dbfde-156">輸出</span><span class="sxs-lookup"><span data-stu-id="dbfde-156">OUTPUTS</span></span>

### <span data-ttu-id="dbfde-157">PSHubVirtualNetworkConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="dbfde-157">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="dbfde-158">筆記</span><span class="sxs-lookup"><span data-stu-id="dbfde-158">NOTES</span></span>

## <span data-ttu-id="dbfde-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="dbfde-159">RELATED LINKS</span></span>

[<span data-ttu-id="dbfde-160">AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="dbfde-160">Get-AzVirtualHubVnetConnection</span></span>](./Get-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="dbfde-161">移除-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="dbfde-161">Remove-AzVirtualHubVnetConnection</span></span>](./Remove-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="dbfde-162">新-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="dbfde-162">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)