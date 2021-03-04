---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzP2sVpnGateway.md
ms.openlocfilehash: 08a641e2d944273d0ad6cd389e651901de1f5b4f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903502"
---
# <span data-ttu-id="b3a6f-101">New-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="b3a6f-101">New-AzP2sVpnGateway</span></span>

## <span data-ttu-id="b3a6f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b3a6f-102">SYNOPSIS</span></span>
<span data-ttu-id="b3a6f-103">在 VirtualHub 下建立新 P2S VpnGateway，以指向網站連接。</span><span class="sxs-lookup"><span data-stu-id="b3a6f-103">Create a new P2SVpnGateway under VirtualHub for point to site connectivity.</span></span>

## <span data-ttu-id="b3a6f-104">語法</span><span class="sxs-lookup"><span data-stu-id="b3a6f-104">SYNTAX</span></span>

### <span data-ttu-id="b3a6f-105">ByVirtualHubNameBy VpnServerConfigurationObject (預設) </span><span class="sxs-lookup"><span data-stu-id="b3a6f-105">ByVirtualHubNameByVpnServerConfigurationObject (Default)</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> [-VpnServerConfiguration <PSVpnServerConfiguration>] -VpnClientAddressPool <String[]>
 [-CustomDnsServer <String[]>] [-RoutingConfiguration <PSRoutingConfiguration>] [-EnableInternetSecurityFlag]
 [-EnableRoutingPreferenceInternetFlag] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3a6f-106">ByVirtualHubNameBy VpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="b3a6f-106">ByVirtualHubNameByVpnServerConfigurationResourceId</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> -VpnServerConfigurationId <String> -VpnClientAddressPool <String[]>
 [-CustomDnsServer <String[]>] [-RoutingConfiguration <PSRoutingConfiguration>] [-EnableInternetSecurityFlag]
 [-EnableRoutingPreferenceInternetFlag] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3a6f-107">ByVirtualHubObjectBy VpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="b3a6f-107">ByVirtualHubObjectByVpnServerConfigurationObject</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> [-VpnServerConfiguration <PSVpnServerConfiguration>]
 -VpnClientAddressPool <String[]> [-CustomDnsServer <String[]>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-EnableInternetSecurityFlag]
 [-EnableRoutingPreferenceInternetFlag] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3a6f-108">ByVirtualHubObjectBy VpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="b3a6f-108">ByVirtualHubObjectByVpnServerConfigurationResourceId</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> -VpnServerConfigurationId <String> -VpnClientAddressPool <String[]>
 [-CustomDnsServer <String[]>] [-RoutingConfiguration <PSRoutingConfiguration>] [-EnableInternetSecurityFlag]
 [-EnableRoutingPreferenceInternetFlag] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3a6f-109">ByVirtualHubResourceIdBy VpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="b3a6f-109">ByVirtualHubResourceIdByVpnServerConfigurationObject</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> [-VpnServerConfiguration <PSVpnServerConfiguration>] -VpnClientAddressPool <String[]>
 [-CustomDnsServer <String[]>] [-RoutingConfiguration <PSRoutingConfiguration>] [-EnableInternetSecurityFlag]
 [-EnableRoutingPreferenceInternetFlag] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3a6f-110">ByVirtualHubResourceIdBy VpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="b3a6f-110">ByVirtualHubResourceIdByVpnServerConfigurationResourceId</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> -VpnServerConfigurationId <String> -VpnClientAddressPool <String[]>
 [-CustomDnsServer <String[]>] [-RoutingConfiguration <PSRoutingConfiguration>] [-EnableInternetSecurityFlag]
 [-EnableRoutingPreferenceInternetFlag] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3a6f-111">描述</span><span class="sxs-lookup"><span data-stu-id="b3a6f-111">DESCRIPTION</span></span>
<span data-ttu-id="b3a6f-112">此New-AzP2sVpnGateway Cmdlet 可讓您在 VirtualHub 下建立新 P2S VpnGateway，從點到網站用戶端到 Azure VirtualWan 的指向網站連接。</span><span class="sxs-lookup"><span data-stu-id="b3a6f-112">The New-AzP2sVpnGateway cmdlet enables you to create a new P2SVpnGateway under VirtualHub for Point to site connectivity from Point to site clients to Azure VirtualWan.</span></span>

## <span data-ttu-id="b3a6f-113">例子</span><span class="sxs-lookup"><span data-stu-id="b3a6f-113">EXAMPLES</span></span>

### <span data-ttu-id="b3a6f-114">範例 1</span><span class="sxs-lookup"><span data-stu-id="b3a6f-114">Example 1</span></span>
```
PS C:\> $virtualHub = Get-AzVirtualHub -ResourceGroupName P2SCortexGATesting -Name WestUsVirtualHub
PS C:\> $vpnServerConfig1 = Get-AzVpnServerConfiguration -ResourceGroupName P2SCortexGATesting -Name WestUsConfig
PS C:\> $vpnClientAddressSpaces = New-Object string[] 1
PS C:\> $vpnClientAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $createdP2SVpnGateway = New-AzP2sVpnGateway -ResourceGroupName P2SCortexGATesting -Name 683482ade8564515aed4b8448c9757ea-westus-gw -VirtualHub $virtualHub -VpnGatewayScaleUnit 1 -VpnClientAddressPool $vpnClientAddressSpaces -VpnServerConfiguration $vpnServerConfig1 -EnableInternetSecurityFlag -EnableRoutingPreferenceInternetFlag

ResourceGroupName              : P2SCortexGATesting
Name                           : 683482ade8564515aed4b8448c9757ea-westus-gw
Id                             : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482ade8564515a
                                 ed4b8448c9757ea-westus-gw
Location                       : westus
VpnGatewayScaleUnit            : 1
VirtualHub                     : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub
VpnServerConfiguration         : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig
VpnServerConfigurationLocation :
VpnClientConnectionHealth      : null
Type                           : Microsoft.Network/p2sVpnGateways
ProvisioningState              : Succeeded
P2SConnectionConfigurations    : [
                                   {
                                     "ProvisioningState": "Succeeded",
                                     "VpnClientAddressPool": {
                                       "AddressPrefixes": [
                                         "192.168.2.0/24"
                                       ]
                                     },
                                     "EnableInternetSecurity": True,
                                     "RoutingConfiguration": {
                                       "AssociatedRouteTable": {
                                         "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub/hubRouteTables/defaultRouteTable"
                                       }
                                       "PropagatedRouteTables": {
                                         "Labels": [],
                                         "Ids": [
                                           {
                                            "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub/hubRouteTables/defaultRouteTable"
                                           }
                                        ]
                                       },
                                       "VnetRoutes": {
                                         "StaticRoutes": []
                                       }
                                     },
                                     "Name": "P2SConnectionConfigDefault",
                                     "Etag": "W/\"4b96e6a2-b4d8-46b3-9210-76d40f359bef\"",
                                     "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482
                                 ade8564515aed4b8448c9757ea-westus-gw/p2sConnectionConfigurations/P2SConnectionConfigDefault"
                                   }
                                 ]
```

<span data-ttu-id="b3a6f-115">此New-AzP2sVpnGateway Cmdlet 可讓您在 VirtualHub 下建立新 P2S VpnGateway，以建立指向網站的連結。</span><span class="sxs-lookup"><span data-stu-id="b3a6f-115">The New-AzP2sVpnGateway cmdlet enables you to create a new P2SVpnGateway under VirtualHub for Point to site connectivity.</span></span>

## <span data-ttu-id="b3a6f-116">參數</span><span class="sxs-lookup"><span data-stu-id="b3a6f-116">PARAMETERS</span></span>

### <span data-ttu-id="b3a6f-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b3a6f-117">-AsJob</span></span>
<span data-ttu-id="b3a6f-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b3a6f-118">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3a6f-119">-CustomDnsServer</span><span class="sxs-lookup"><span data-stu-id="b3a6f-119">-CustomDnsServer</span></span>
<span data-ttu-id="b3a6f-120">自訂 Dns 伺服器的清單。</span><span class="sxs-lookup"><span data-stu-id="b3a6f-120">The list of Custom Dns Servers.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3a6f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3a6f-121">-DefaultProfile</span></span>
<span data-ttu-id="b3a6f-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b3a6f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3a6f-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="b3a6f-123">-Name</span></span>
<span data-ttu-id="b3a6f-124">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="b3a6f-124">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, P2SVpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3a6f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3a6f-125">-ResourceGroupName</span></span>
<span data-ttu-id="b3a6f-126">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="b3a6f-126">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3a6f-127">-EnableInternetSecurityFlag</span><span class="sxs-lookup"><span data-stu-id="b3a6f-127">-EnableInternetSecurityFlag</span></span>
<span data-ttu-id="b3a6f-128">為此 P2S VpnGateway 連接啟用網際網路安全性旗標</span><span class="sxs-lookup"><span data-stu-id="b3a6f-128">Enable internet security flag for this P2SVpnGateway connections</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3a6f-129">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="b3a6f-129">-RoutingConfiguration</span></span>
<span data-ttu-id="b3a6f-130">此連接的路由群組原則</span><span class="sxs-lookup"><span data-stu-id="b3a6f-130">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="b3a6f-131">-標記</span><span class="sxs-lookup"><span data-stu-id="b3a6f-131">-Tag</span></span>
<span data-ttu-id="b3a6f-132">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b3a6f-132">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3a6f-133">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="b3a6f-133">-VirtualHub</span></span>
<span data-ttu-id="b3a6f-134">與此 P2S VpnGateway 相關聯的 VirtualHub。</span><span class="sxs-lookup"><span data-stu-id="b3a6f-134">The VirtualHub this P2SVpnGateway needs to be associated with.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObjectByVpnServerConfigurationObject, ByVirtualHubObjectByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3a6f-135">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="b3a6f-135">-VirtualHubId</span></span>
<span data-ttu-id="b3a6f-136">此 P2S VpnGateway 的 VirtualHub 識別碼必須相關聯。</span><span class="sxs-lookup"><span data-stu-id="b3a6f-136">The Id of the VirtualHub this P2SVpnGateway needs to be associated with.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceIdByVpnServerConfigurationObject, ByVirtualHubResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3a6f-137">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="b3a6f-137">-VirtualHubName</span></span>
<span data-ttu-id="b3a6f-138">此 P2S VpnGateway 的 VirtualHub 識別碼必須相關聯。</span><span class="sxs-lookup"><span data-stu-id="b3a6f-138">The Id of the VirtualHub this P2SVpnGateway needs to be associated with.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByVpnServerConfigurationObject, ByVirtualHubNameByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3a6f-139">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="b3a6f-139">-VpnClientAddressPool</span></span>
<span data-ttu-id="b3a6f-140">P2S VpnClient AddressPool for this P2S VpnGateway P2SConnectionConfiguration.</span><span class="sxs-lookup"><span data-stu-id="b3a6f-140">P2S VpnClient AddressPool for this P2SVpnGateway P2SConnectionConfiguration.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3a6f-141">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="b3a6f-141">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="b3a6f-142">此 P2S VpnGateway 的縮放單位。</span><span class="sxs-lookup"><span data-stu-id="b3a6f-142">The scale unit for this P2SVpnGateway.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3a6f-143">-VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="b3a6f-143">-VpnServerConfiguration</span></span>
<span data-ttu-id="b3a6f-144">要附加至此 P2S VpnGateway 的 VpnServerConfiguration。</span><span class="sxs-lookup"><span data-stu-id="b3a6f-144">The VpnServerConfiguration to be attached to this P2SVpnGateway.</span></span>

```yaml
Type: PSVpnServerConfiguration
Parameter Sets: ByVirtualHubNameByVpnServerConfigurationObject, ByVirtualHubObjectByVpnServerConfigurationObject, ByVirtualHubResourceIdByVpnServerConfigurationObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3a6f-145">-VpnServerConfigurationId</span><span class="sxs-lookup"><span data-stu-id="b3a6f-145">-VpnServerConfigurationId</span></span>
<span data-ttu-id="b3a6f-146">將會附加此 P2S VpnGateway 的 Vpn 伺服器組組物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b3a6f-146">The id of Vpn server configuration object this P2SVpnGateway will be attached to.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByVpnServerConfigurationResourceId, ByVirtualHubObjectByVpnServerConfigurationResourceId, ByVirtualHubResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3a6f-147">-EnableRoutingPreferenceInternetFlag</span><span class="sxs-lookup"><span data-stu-id="b3a6f-147">-EnableRoutingPreferenceInternetFlag</span></span>
<span data-ttu-id="b3a6f-148">在此 P2S VpnGateway 上啟用路由喜好設定網際網路的標標。</span><span class="sxs-lookup"><span data-stu-id="b3a6f-148">Flag to enable Routing Preference Internet on this P2SVpnGateway.</span></span>

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

### <span data-ttu-id="b3a6f-149">-確認</span><span class="sxs-lookup"><span data-stu-id="b3a6f-149">-Confirm</span></span>
<span data-ttu-id="b3a6f-150">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b3a6f-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3a6f-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3a6f-151">-WhatIf</span></span>
<span data-ttu-id="b3a6f-152">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b3a6f-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3a6f-153">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b3a6f-153">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3a6f-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3a6f-154">CommonParameters</span></span>
<span data-ttu-id="b3a6f-155">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b3a6f-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3a6f-156">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3a6f-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3a6f-157">輸入</span><span class="sxs-lookup"><span data-stu-id="b3a6f-157">INPUTS</span></span>

### <span data-ttu-id="b3a6f-158">Microsoft.Azure.Commands.Network.models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="b3a6f-158">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>
<span data-ttu-id="b3a6f-159">System.String Microsoft.Azure.Commands.network.models.PS VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="b3a6f-159">System.String Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="b3a6f-160">輸出</span><span class="sxs-lookup"><span data-stu-id="b3a6f-160">OUTPUTS</span></span>

### <span data-ttu-id="b3a6f-161">Microsoft.Azure.Commands.Network.models.PSP2S VpnGateway</span><span class="sxs-lookup"><span data-stu-id="b3a6f-161">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>
## <span data-ttu-id="b3a6f-162">筆記</span><span class="sxs-lookup"><span data-stu-id="b3a6f-162">NOTES</span></span>

## <span data-ttu-id="b3a6f-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="b3a6f-163">RELATED LINKS</span></span>

[<span data-ttu-id="b3a6f-164">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="b3a6f-164">New-AzRoutingConfiguration</span></span>]()

