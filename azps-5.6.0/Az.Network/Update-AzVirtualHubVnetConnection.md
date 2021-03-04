---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHubVnetConnection.md
ms.openlocfilehash: 1454e3ba3fc3a7e229e064a32146ebddddc19392
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901818"
---
# <span data-ttu-id="46517-101">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="46517-101">Update-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="46517-102">簡介</span><span class="sxs-lookup"><span data-stu-id="46517-102">SYNOPSIS</span></span>
<span data-ttu-id="46517-103">更新現有的 HubVirtualNetworkConnection。</span><span class="sxs-lookup"><span data-stu-id="46517-103">Updates an existing HubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="46517-104">語法</span><span class="sxs-lookup"><span data-stu-id="46517-104">SYNTAX</span></span>

### <span data-ttu-id="46517-105">ByHubVirtualNetworkConnectionName (預設) </span><span class="sxs-lookup"><span data-stu-id="46517-105">ByHubVirtualNetworkConnectionName (Default)</span></span>
```
Update-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="46517-106">ByHubVirtualNetworkConnectionObject</span><span class="sxs-lookup"><span data-stu-id="46517-106">ByHubVirtualNetworkConnectionObject</span></span>
```
Update-AzVirtualHubVnetConnection -InputObject <PSHubVirtualNetworkConnection>
 [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="46517-107">ByHubVirtualNetworkConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="46517-107">ByHubVirtualNetworkConnectionResourceId</span></span>
```
Update-AzVirtualHubVnetConnection -ResourceId <String> [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46517-108">描述</span><span class="sxs-lookup"><span data-stu-id="46517-108">DESCRIPTION</span></span>
<span data-ttu-id="46517-109">更新現有的 HubVirtualNetworkConnection。</span><span class="sxs-lookup"><span data-stu-id="46517-109">Updates an existing HubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="46517-110">例子</span><span class="sxs-lookup"><span data-stu-id="46517-110">EXAMPLES</span></span>

### <span data-ttu-id="46517-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="46517-111">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Update-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -EnableInternetSecurity $true
Name                   : testvnetconnection
Id                     : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
EnableInternetSecurity : True
ProvisioningState      : Succeeded
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

<span data-ttu-id="46517-112">上述步驟將在 Azure 的資源群組中，建立資源群組、虛擬 WAN、虛擬網路、美國中心的虛擬中樞。</span><span class="sxs-lookup"><span data-stu-id="46517-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="46517-113">也會建立一個與虛擬中樞對等的虛擬網路連接。</span><span class="sxs-lookup"><span data-stu-id="46517-113">A Virtual Network Connection is also created which is peer the Virtual Network to the Virtual Hub.</span></span> <span data-ttu-id="46517-114">接著會更新此虛擬網路連接，以啟用網際網路安全性。</span><span class="sxs-lookup"><span data-stu-id="46517-114">This Virtual Network Connection is then updated to enable internet security.</span></span>

## <span data-ttu-id="46517-115">參數</span><span class="sxs-lookup"><span data-stu-id="46517-115">PARAMETERS</span></span>

### <span data-ttu-id="46517-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46517-116">-AsJob</span></span>
<span data-ttu-id="46517-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46517-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="46517-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46517-118">-DefaultProfile</span></span>
<span data-ttu-id="46517-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="46517-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46517-120">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="46517-120">-EnableInternetSecurity</span></span>
<span data-ttu-id="46517-121">啟用此連接的網際網路安全性。</span><span class="sxs-lookup"><span data-stu-id="46517-121">Enable internet security for this connection.</span></span>

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

### <span data-ttu-id="46517-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46517-122">-InputObject</span></span>
<span data-ttu-id="46517-123">要修改的 hubvirtualnetworkconnection 資源。</span><span class="sxs-lookup"><span data-stu-id="46517-123">The hubvirtualnetworkconnection resource to modify.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection
Parameter Sets: ByHubVirtualNetworkConnectionObject
Aliases: HubVirtualNetworkConnection
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46517-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="46517-124">-Name</span></span>
<span data-ttu-id="46517-125">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="46517-125">The resource name.</span></span>

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

### <span data-ttu-id="46517-126">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="46517-126">-ParentResourceName</span></span>
<span data-ttu-id="46517-127">父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="46517-127">The parent resource name.</span></span>

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

### <span data-ttu-id="46517-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46517-128">-ResourceGroupName</span></span>
<span data-ttu-id="46517-129">資源組名。</span><span class="sxs-lookup"><span data-stu-id="46517-129">The resource group name.</span></span>

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

### <span data-ttu-id="46517-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46517-130">-ResourceId</span></span>
<span data-ttu-id="46517-131">hubvirtualnetworkconnection 資源要修改的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="46517-131">The resource id of the hubvirtualnetworkconnection resource to modify.</span></span>

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

### <span data-ttu-id="46517-132">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="46517-132">-RoutingConfiguration</span></span>
<span data-ttu-id="46517-133">此連接的路由群組原則</span><span class="sxs-lookup"><span data-stu-id="46517-133">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="46517-134">-確認</span><span class="sxs-lookup"><span data-stu-id="46517-134">-Confirm</span></span>
<span data-ttu-id="46517-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="46517-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46517-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46517-136">-WhatIf</span></span>
<span data-ttu-id="46517-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="46517-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46517-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="46517-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46517-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46517-139">CommonParameters</span></span>
<span data-ttu-id="46517-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="46517-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46517-141">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="46517-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46517-142">輸入</span><span class="sxs-lookup"><span data-stu-id="46517-142">INPUTS</span></span>

### <span data-ttu-id="46517-143">System.String</span><span class="sxs-lookup"><span data-stu-id="46517-143">System.String</span></span>

### <span data-ttu-id="46517-144">Microsoft.Azure.Commands.Network.models.PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="46517-144">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="46517-145">輸出</span><span class="sxs-lookup"><span data-stu-id="46517-145">OUTPUTS</span></span>

### <span data-ttu-id="46517-146">Microsoft.Azure.Commands.Network.models.PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="46517-146">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="46517-147">筆記</span><span class="sxs-lookup"><span data-stu-id="46517-147">NOTES</span></span>

## <span data-ttu-id="46517-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="46517-148">RELATED LINKS</span></span>

[<span data-ttu-id="46517-149">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="46517-149">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
