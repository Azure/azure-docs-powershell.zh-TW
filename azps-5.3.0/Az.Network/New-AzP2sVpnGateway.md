---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzP2sVpnGateway.md
ms.openlocfilehash: 516cd38257a8742f1bc23b3207b7e3c982d9eb36
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98438819"
---
# <span data-ttu-id="6ce9d-101">New-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6ce9d-101">New-AzP2sVpnGateway</span></span>

## <span data-ttu-id="6ce9d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6ce9d-102">SYNOPSIS</span></span>
<span data-ttu-id="6ce9d-103">在 [VirtualHub] 下建立新的 P2SVpnGateway，以指向 [網站連線]。</span><span class="sxs-lookup"><span data-stu-id="6ce9d-103">Create a new P2SVpnGateway under VirtualHub for point to site connectivity.</span></span>

## <span data-ttu-id="6ce9d-104">句法</span><span class="sxs-lookup"><span data-stu-id="6ce9d-104">SYNTAX</span></span>

### <span data-ttu-id="6ce9d-105">ByVirtualHubNameByVpnServerConfigurationObject (預設) </span><span class="sxs-lookup"><span data-stu-id="6ce9d-105">ByVirtualHubNameByVpnServerConfigurationObject (Default)</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> [-VpnServerConfiguration <PSVpnServerConfiguration>] -VpnClientAddressPool <String[]> [-CustomDnsServer <String[]>] [-EnableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ce9d-106">ByVirtualHubNameByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="6ce9d-106">ByVirtualHubNameByVpnServerConfigurationResourceId</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> -VpnServerConfigurationId <String> -VpnClientAddressPool <String[]>
 [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ce9d-107">ByVirtualHubObjectByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="6ce9d-107">ByVirtualHubObjectByVpnServerConfigurationObject</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> [-VpnServerConfiguration <PSVpnServerConfiguration>]
 -VpnClientAddressPool <String[]> [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ce9d-108">ByVirtualHubObjectByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="6ce9d-108">ByVirtualHubObjectByVpnServerConfigurationResourceId</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> -VpnServerConfigurationId <String> -VpnClientAddressPool <String[]>
 [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ce9d-109">ByVirtualHubResourceIdByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="6ce9d-109">ByVirtualHubResourceIdByVpnServerConfigurationObject</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> [-VpnServerConfiguration <PSVpnServerConfiguration>] -VpnClientAddressPool <String[]>
 [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ce9d-110">ByVirtualHubResourceIdByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="6ce9d-110">ByVirtualHubResourceIdByVpnServerConfigurationResourceId</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> -VpnServerConfigurationId <String> -VpnClientAddressPool <String[]>
 [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ce9d-111">說明</span><span class="sxs-lookup"><span data-stu-id="6ce9d-111">DESCRIPTION</span></span>
<span data-ttu-id="6ce9d-112">**新的-AzP2sVpnGateway** Cmdlet 可讓您在 VirtualHub 下建立新的 P2SVpnGateway，以從指向網站用戶端到 Azure VirtualWan。</span><span class="sxs-lookup"><span data-stu-id="6ce9d-112">The **New-AzP2sVpnGateway** cmdlet enables you to create a new P2SVpnGateway under VirtualHub for Point to site connectivity from Point to site clients to Azure VirtualWan.</span></span>

## <span data-ttu-id="6ce9d-113">示例</span><span class="sxs-lookup"><span data-stu-id="6ce9d-113">EXAMPLES</span></span>

### <span data-ttu-id="6ce9d-114">範例1</span><span class="sxs-lookup"><span data-stu-id="6ce9d-114">Example 1</span></span>
```powershell
PS C:\> $virtualHub = Get-AzVirtualHub -ResourceGroupName P2SCortexGATesting -Name WestUsVirtualHub
PS C:\> $vpnServerConfig1 = Get-AzVpnServerConfiguration -ResourceGroupName P2SCortexGATesting -Name WestUsConfig
PS C:\> $vpnClientAddressSpaces = New-Object string[] 1
PS C:\> $vpnClientAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $createdP2SVpnGateway = New-AzP2sVpnGateway -ResourceGroupName P2SCortexGATesting -Name 683482ade8564515aed4b8448c9757ea-westus-gw -VirtualHub $virtualHub -VpnGatewayScaleUnit 1 -VpnClientAddressPool $vpnClientAddressSpaces -VpnServerConfiguration $vpnServerConfig1 -EnableInternetSecurityFlag

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

<span data-ttu-id="6ce9d-115">**新的-AzP2sVpnGateway** Cmdlet 可讓您在 VirtualHub 中建立新的 P2SVpnGateway，以指向 [網站連線]。</span><span class="sxs-lookup"><span data-stu-id="6ce9d-115">The **New-AzP2sVpnGateway** cmdlet enables you to create a new P2SVpnGateway under VirtualHub for Point to site connectivity.</span></span>

## <span data-ttu-id="6ce9d-116">參數</span><span class="sxs-lookup"><span data-stu-id="6ce9d-116">PARAMETERS</span></span>

### <span data-ttu-id="6ce9d-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6ce9d-117">-AsJob</span></span>
<span data-ttu-id="6ce9d-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6ce9d-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6ce9d-119">-CustomDnsServer</span><span class="sxs-lookup"><span data-stu-id="6ce9d-119">-CustomDnsServer</span></span>
<span data-ttu-id="6ce9d-120">自訂 Dns 伺服器的清單。</span><span class="sxs-lookup"><span data-stu-id="6ce9d-120">The list of Custom Dns Servers.</span></span>

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

### <span data-ttu-id="6ce9d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ce9d-121">-DefaultProfile</span></span>
<span data-ttu-id="6ce9d-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6ce9d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ce9d-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="6ce9d-123">-Name</span></span>
<span data-ttu-id="6ce9d-124">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="6ce9d-124">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, P2SVpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ce9d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ce9d-125">-ResourceGroupName</span></span>
<span data-ttu-id="6ce9d-126">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="6ce9d-126">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ce9d-127">-EnableInternetSecurityFlag</span><span class="sxs-lookup"><span data-stu-id="6ce9d-127">-EnableInternetSecurityFlag</span></span>
<span data-ttu-id="6ce9d-128">針對此 P2SVpnGateway 連線啟用網際網路安全標誌</span><span class="sxs-lookup"><span data-stu-id="6ce9d-128">Enable internet security flag for this P2SVpnGateway connections</span></span>

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

### <span data-ttu-id="6ce9d-129">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ce9d-129">-RoutingConfiguration</span></span>
<span data-ttu-id="6ce9d-130">此連線的路由設定</span><span class="sxs-lookup"><span data-stu-id="6ce9d-130">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="6ce9d-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="6ce9d-131">-Tag</span></span>
<span data-ttu-id="6ce9d-132">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="6ce9d-132">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="6ce9d-133">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="6ce9d-133">-VirtualHub</span></span>
<span data-ttu-id="6ce9d-134">此 P2SVpnGateway 需要關聯的 VirtualHub。</span><span class="sxs-lookup"><span data-stu-id="6ce9d-134">The VirtualHub this P2SVpnGateway needs to be associated with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObjectByVpnServerConfigurationObject, ByVirtualHubObjectByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ce9d-135">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="6ce9d-135">-VirtualHubId</span></span>
<span data-ttu-id="6ce9d-136">此 P2SVpnGateway 需要關聯之 VirtualHub 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6ce9d-136">The Id of the VirtualHub this P2SVpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceIdByVpnServerConfigurationObject, ByVirtualHubResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ce9d-137">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="6ce9d-137">-VirtualHubName</span></span>
<span data-ttu-id="6ce9d-138">此 P2SVpnGateway 需要關聯之 VirtualHub 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6ce9d-138">The Id of the VirtualHub this P2SVpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubNameByVpnServerConfigurationObject, ByVirtualHubNameByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ce9d-139">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="6ce9d-139">-VpnClientAddressPool</span></span>
<span data-ttu-id="6ce9d-140">P2S VpnClient AddressPool P2SVpnGateway P2SConnectionConfiguration。</span><span class="sxs-lookup"><span data-stu-id="6ce9d-140">P2S VpnClient AddressPool for this P2SVpnGateway P2SConnectionConfiguration.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ce9d-141">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="6ce9d-141">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="6ce9d-142">此 P2SVpnGateway 的縮放單位。</span><span class="sxs-lookup"><span data-stu-id="6ce9d-142">The scale unit for this P2SVpnGateway.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ce9d-143">-VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ce9d-143">-VpnServerConfiguration</span></span>
<span data-ttu-id="6ce9d-144">要附加到此 P2SVpnGateway 的 VpnServerConfiguration。</span><span class="sxs-lookup"><span data-stu-id="6ce9d-144">The VpnServerConfiguration to be attached to this P2SVpnGateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration
Parameter Sets: ByVirtualHubNameByVpnServerConfigurationObject, ByVirtualHubObjectByVpnServerConfigurationObject, ByVirtualHubResourceIdByVpnServerConfigurationObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ce9d-145">-VpnServerConfigurationId</span><span class="sxs-lookup"><span data-stu-id="6ce9d-145">-VpnServerConfigurationId</span></span>
<span data-ttu-id="6ce9d-146">此 P2SVpnGateway 將附加到的 Vpn 伺服器設定物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6ce9d-146">The id of Vpn server configuration object this P2SVpnGateway will be attached to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubNameByVpnServerConfigurationResourceId, ByVirtualHubObjectByVpnServerConfigurationResourceId, ByVirtualHubResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ce9d-147">-確認</span><span class="sxs-lookup"><span data-stu-id="6ce9d-147">-Confirm</span></span>
<span data-ttu-id="6ce9d-148">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6ce9d-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ce9d-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ce9d-149">-WhatIf</span></span>
<span data-ttu-id="6ce9d-150">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6ce9d-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ce9d-151">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6ce9d-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ce9d-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ce9d-152">CommonParameters</span></span>
<span data-ttu-id="6ce9d-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6ce9d-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ce9d-154">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6ce9d-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ce9d-155">輸入</span><span class="sxs-lookup"><span data-stu-id="6ce9d-155">INPUTS</span></span>

### <span data-ttu-id="6ce9d-156">PSVirtualHub 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6ce9d-156">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>
<span data-ttu-id="6ce9d-157">PSVpnServerConfiguration 中的 [system.object] 命令。</span><span class="sxs-lookup"><span data-stu-id="6ce9d-157">System.String Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="6ce9d-158">輸出</span><span class="sxs-lookup"><span data-stu-id="6ce9d-158">OUTPUTS</span></span>

### <span data-ttu-id="6ce9d-159">PSP2SVpnGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6ce9d-159">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="6ce9d-160">筆記</span><span class="sxs-lookup"><span data-stu-id="6ce9d-160">NOTES</span></span>

## <span data-ttu-id="6ce9d-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="6ce9d-161">RELATED LINKS</span></span>

[<span data-ttu-id="6ce9d-162">新-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ce9d-162">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
