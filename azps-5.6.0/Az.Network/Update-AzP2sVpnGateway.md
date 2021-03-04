---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzP2sVpnGateway.md
ms.openlocfilehash: 33a22ce2089dd1111fcafce20208a1b948ce1253
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901829"
---
# <span data-ttu-id="06949-101">Update-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="06949-101">Update-AzP2sVpnGateway</span></span>

## <span data-ttu-id="06949-102">簡介</span><span class="sxs-lookup"><span data-stu-id="06949-102">SYNOPSIS</span></span>
<span data-ttu-id="06949-103">在 VirtualHub 下更新現有的 P2S VpnGateway，以指向網站連接。</span><span class="sxs-lookup"><span data-stu-id="06949-103">Update an existing P2SVpnGateway under VirtualHub for point to site connectivity.</span></span>

## <span data-ttu-id="06949-104">語法</span><span class="sxs-lookup"><span data-stu-id="06949-104">SYNTAX</span></span>

### <span data-ttu-id="06949-105">ByP2S VpnGatewayNameNo VpnServerConfigurationUpdate (預設) </span><span class="sxs-lookup"><span data-stu-id="06949-105">ByP2SVpnGatewayNameNoVpnServerConfigurationUpdate (Default)</span></span>
```
Update-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-VpnClientAddressPool <String[]>] [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>] [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06949-106">ByP2S VpnGatewayNameBy VpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="06949-106">ByP2SVpnGatewayNameByVpnServerConfigurationObject</span></span>
```
Update-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-VpnClientAddressPool <String[]>] [-VpnServerConfiguration <PSVpnServerConfiguration>] [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06949-107">ByP2S VpnGatewayNameBy VpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="06949-107">ByP2SVpnGatewayNameByVpnServerConfigurationResourceId</span></span>
```
Update-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-VpnClientAddressPool <String[]>]
 -VpnServerConfigurationId <String> [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="06949-108">ByP2S VpnGatewayObjectNo VpnServerConfigurationUpdate</span><span class="sxs-lookup"><span data-stu-id="06949-108">ByP2SVpnGatewayObjectNoVpnServerConfigurationUpdate</span></span>
```
Update-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-VpnClientAddressPool <String[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06949-109">ByP2S VpnGatewayObjectBy VpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="06949-109">ByP2SVpnGatewayObjectByVpnServerConfigurationObject</span></span>
```
Update-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-VpnClientAddressPool <String[]>]
 [-VpnServerConfiguration <PSVpnServerConfiguration>] [-VpnGatewayScaleUnit <UInt32>]
 [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06949-110">ByP2S VpnGatewayObjectBy VpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="06949-110">ByP2SVpnGatewayObjectByVpnServerConfigurationResourceId</span></span>
```
Update-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-VpnClientAddressPool <String[]>]
 -VpnServerConfigurationId <String> [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06949-111">ByP2S VpnGatewayResourceIdNo VpnServerConfigurationUpdate</span><span class="sxs-lookup"><span data-stu-id="06949-111">ByP2SVpnGatewayResourceIdNoVpnServerConfigurationUpdate</span></span>
```
Update-AzP2sVpnGateway -ResourceId <String> [-VpnClientAddressPool <String[]>] [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06949-112">ByP2S VpnGatewayResourceIdBy VpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="06949-112">ByP2SVpnGatewayResourceIdByVpnServerConfigurationObject</span></span>
```
Update-AzP2sVpnGateway -ResourceId <String> [-VpnClientAddressPool <String[]>] [-VpnServerConfiguration <PSVpnServerConfiguration>] [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06949-113">ByP2S VpnGatewayResourceIdBy VpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="06949-113">ByP2SVpnGatewayResourceIdByVpnServerConfigurationResourceId</span></span>
```
Update-AzP2sVpnGateway -ResourceId <String> [-VpnClientAddressPool <String[]>] -VpnServerConfigurationId <String> [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06949-114">描述</span><span class="sxs-lookup"><span data-stu-id="06949-114">DESCRIPTION</span></span>
<span data-ttu-id="06949-115">**Update-AzP2s VpnGateway** Cmdlet 可讓您使用新的 VpnClientAddressPool 或新的 VpnServerConfiguration 或 VpnGatewayScaleUnit 變更，在 VirtualHub 下更新現有的 P2S VpnGateway。</span><span class="sxs-lookup"><span data-stu-id="06949-115">The **Update-AzP2sVpnGateway** cmdlet enables you to update an existing P2SVpnGateway under VirtualHub with new VpnClientAddressPool or new VpnServerConfiguration or change of VpnGatewayScaleUnit.</span></span>

## <span data-ttu-id="06949-116">例子</span><span class="sxs-lookup"><span data-stu-id="06949-116">EXAMPLES</span></span>

### <span data-ttu-id="06949-117">範例 1</span><span class="sxs-lookup"><span data-stu-id="06949-117">Example 1</span></span>
```powershell
PS C:\> $vpnClientAddressSpaces = New-Object string[] 1 
PS C:\> $vpnClientAddressSpaces[0] = "101.10.0.0/16"
PS C:\> Update-AzP2sVpnGateway -ResourceGroupName P2SCortexGATesting -Name 683482ade8564515aed4b8448c9757ea-westus-gw -VpnClientAddressPool $vpnClientAddressSpaces -EnableInternetSecurityFlag                                

ResourceGroupName              : P2SCortexGATesting
Name                           : 683482ade8564515aed4b8448c9757ea-westus-gw
Id                             : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482ade8564515a
                                 ed4b8448c9757ea-westus-gw
Location                       : westus
VpnGatewayScaleUnit            : 1
VirtualHub                     : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/NilamdWestUsVirtualH
                                 ub
VpnServerConfiguration         : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/NilamdWe
                                 stUsConfig
VpnServerConfigurationLocation :
VpnClientConnectionHealth      : null
Type                           : Microsoft.Network/p2sVpnGateways
ProvisioningState              : Succeeded
P2SConnectionConfigurations    : [
                                   {
                                     "ProvisioningState": "Succeeded",
                                     "VpnClientAddressPool": {
                                       "AddressPrefixes": [
                                         "101.10.0.0/16"
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
                                     "Etag": "W/\"d7debc2f-ccbb-4f00-bddc-42c99b52fda3\"",
                                     "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482
                                 ade8564515aed4b8448c9757ea-westus-gw/p2sConnectionConfigurations/P2SConnectionConfigDefault"
                                   }
                                 ]
```

<span data-ttu-id="06949-118">**Update-AzP2s VpnGateway** Cmdlet 可讓您使用新的 VpnClientAddressPool 更新 VirtualHub 下現有的 P2S VpnGateway。</span><span class="sxs-lookup"><span data-stu-id="06949-118">The **Update-AzP2sVpnGateway** cmdlet enables you to update an existing P2SVpnGateway under VirtualHub with new VpnClientAddressPool.</span></span> <span data-ttu-id="06949-119">當指向網站用戶端與 P2S VpnGateway 連接時，此 VpnClientAddressPool 的其中一個 IP 位址會配置給該用戶端。</span><span class="sxs-lookup"><span data-stu-id="06949-119">When Point to site client connects with this P2SVpnGateway, one of the ip address from this VpnClientAddressPool gets allocated to that client.</span></span>

### <span data-ttu-id="06949-120">範例 2</span><span class="sxs-lookup"><span data-stu-id="06949-120">Example 2</span></span>

<span data-ttu-id="06949-121">在 VirtualHub 下更新現有的 P2S VpnGateway，以指向網站連接。</span><span class="sxs-lookup"><span data-stu-id="06949-121">Update an existing P2SVpnGateway under VirtualHub for point to site connectivity.</span></span> <span data-ttu-id="06949-122"> (自動) </span><span class="sxs-lookup"><span data-stu-id="06949-122">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Update-AzP2sVpnGateway -AsJob -Name 00000000-0000-0000-0000-00000000000000000-westus-gw -ResourceGroupName P2SCortexGATesting -VpnClientAddressPool <String[]> -VpnGatewayScaleUnit 1 -VpnServerConfiguration <PSVpnServerConfiguration>
```

## <span data-ttu-id="06949-123">參數</span><span class="sxs-lookup"><span data-stu-id="06949-123">PARAMETERS</span></span>

### <span data-ttu-id="06949-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06949-124">-AsJob</span></span>
<span data-ttu-id="06949-125">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="06949-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="06949-126">-CustomDnsServer</span><span class="sxs-lookup"><span data-stu-id="06949-126">-CustomDnsServer</span></span>
<span data-ttu-id="06949-127">自訂 Dns 伺服器的清單。</span><span class="sxs-lookup"><span data-stu-id="06949-127">The list of Custom Dns Servers.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06949-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06949-128">-DefaultProfile</span></span>
<span data-ttu-id="06949-129">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="06949-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06949-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06949-130">-InputObject</span></span>
<span data-ttu-id="06949-131">要修改的 p2s vpn 閘道物件</span><span class="sxs-lookup"><span data-stu-id="06949-131">The p2s vpn gateway object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObjectNoVpnServerConfigurationUpdate, ByP2SVpnGatewayObjectByVpnServerConfigurationObject, ByP2SVpnGatewayObjectByVpnServerConfigurationResourceId
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06949-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="06949-132">-Name</span></span>
<span data-ttu-id="06949-133">P2S vpn 閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="06949-133">The P2S vpn gateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByP2SVpnGatewayNameNoVpnServerConfigurationUpdate, ByP2SVpnGatewayNameByVpnServerConfigurationObject, ByP2SVpnGatewayNameByVpnServerConfigurationResourceId
Aliases: ResourceName, P2SVpnGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06949-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06949-134">-ResourceGroupName</span></span>
<span data-ttu-id="06949-135">資源組名。</span><span class="sxs-lookup"><span data-stu-id="06949-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByP2SVpnGatewayNameNoVpnServerConfigurationUpdate, ByP2SVpnGatewayNameByVpnServerConfigurationObject, ByP2SVpnGatewayNameByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06949-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="06949-136">-ResourceId</span></span>
<span data-ttu-id="06949-137">要修改之 P2S VpnGateway 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="06949-137">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByP2SVpnGatewayResourceIdNoVpnServerConfigurationUpdate, ByP2SVpnGatewayResourceIdByVpnServerConfigurationObject, ByP2SVpnGatewayResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06949-138">-EnableInternetSecurityFlag</span><span class="sxs-lookup"><span data-stu-id="06949-138">-EnableInternetSecurityFlag</span></span>
<span data-ttu-id="06949-139">為此 P2S VpnGateway 連接啟用網際網路安全性旗標</span><span class="sxs-lookup"><span data-stu-id="06949-139">Enable internet security flag for this P2SVpnGateway connections</span></span>

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

### <span data-ttu-id="06949-140">-DisableInternetSecurityFlag</span><span class="sxs-lookup"><span data-stu-id="06949-140">-DisableInternetSecurityFlag</span></span>
<span data-ttu-id="06949-141">停用此 P2S VpnGateway 連接的網際網路安全性旗標</span><span class="sxs-lookup"><span data-stu-id="06949-141">Disable internet security flag for this P2SVpnGateway connections</span></span>

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

### <span data-ttu-id="06949-142">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="06949-142">-RoutingConfiguration</span></span>
<span data-ttu-id="06949-143">此連接的路由群組原則</span><span class="sxs-lookup"><span data-stu-id="06949-143">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="06949-144">-標記</span><span class="sxs-lookup"><span data-stu-id="06949-144">-Tag</span></span>
<span data-ttu-id="06949-145">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="06949-145">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06949-146">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="06949-146">-VpnClientAddressPool</span></span>
<span data-ttu-id="06949-147">P2S VpnClient AddressPool for this P2S VpnGateway P2SConnectionConfiguration.</span><span class="sxs-lookup"><span data-stu-id="06949-147">P2S VpnClient AddressPool for this P2SVpnGateway P2SConnectionConfiguration.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06949-148">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="06949-148">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="06949-149">此 P2S VpnGateway 的縮放單位。</span><span class="sxs-lookup"><span data-stu-id="06949-149">The scale unit for this P2SVpnGateway.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06949-150">-VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="06949-150">-VpnServerConfiguration</span></span>
<span data-ttu-id="06949-151">要附加至此 P2S VpnGateway 的 VpnServerConfiguration。</span><span class="sxs-lookup"><span data-stu-id="06949-151">The VpnServerConfiguration to be attached to this P2SVpnGateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration
Parameter Sets: ByP2SVpnGatewayNameByVpnServerConfigurationObject, ByP2SVpnGatewayObjectByVpnServerConfigurationObject, ByP2SVpnGatewayResourceIdByVpnServerConfigurationObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06949-152">-VpnServerConfigurationId</span><span class="sxs-lookup"><span data-stu-id="06949-152">-VpnServerConfigurationId</span></span>
<span data-ttu-id="06949-153">將會附加此 P2S VpnGateway 的 Vpn 伺服器組組物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="06949-153">The id of Vpn server configuration object this P2SVpnGateway will be attached to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByP2SVpnGatewayNameByVpnServerConfigurationResourceId, ByP2SVpnGatewayObjectByVpnServerConfigurationResourceId, ByP2SVpnGatewayResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06949-154">-確認</span><span class="sxs-lookup"><span data-stu-id="06949-154">-Confirm</span></span>
<span data-ttu-id="06949-155">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="06949-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06949-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06949-156">-WhatIf</span></span>
<span data-ttu-id="06949-157">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="06949-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06949-158">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="06949-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06949-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06949-159">CommonParameters</span></span>
<span data-ttu-id="06949-160">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="06949-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06949-161">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="06949-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06949-162">輸入</span><span class="sxs-lookup"><span data-stu-id="06949-162">INPUTS</span></span>

### <span data-ttu-id="06949-163">Microsoft.Azure.Commands.Network.models.PSP2S VpnGateway</span><span class="sxs-lookup"><span data-stu-id="06949-163">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>
<span data-ttu-id="06949-164">System.String Microsoft.Azure.Commands.Network.models.PS VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="06949-164">System.String Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="06949-165">輸出</span><span class="sxs-lookup"><span data-stu-id="06949-165">OUTPUTS</span></span>

### <span data-ttu-id="06949-166">Microsoft.Azure.Commands.Network.models.PSP2S VpnGateway</span><span class="sxs-lookup"><span data-stu-id="06949-166">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="06949-167">筆記</span><span class="sxs-lookup"><span data-stu-id="06949-167">NOTES</span></span>

## <span data-ttu-id="06949-168">相關連結</span><span class="sxs-lookup"><span data-stu-id="06949-168">RELATED LINKS</span></span>

[<span data-ttu-id="06949-169">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="06949-169">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
