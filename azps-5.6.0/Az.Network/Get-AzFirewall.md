---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 91D58F60-F22A-454A-B04C-E5AEF33E9D06
online version: https://docs.microsoft.com/powershell/module/az.network/get-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewall.md
ms.openlocfilehash: 56227c5c3df8f428e8d25329f8dbb9965ff502cc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903161"
---
# <span data-ttu-id="1719d-101">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="1719d-101">Get-AzFirewall</span></span>

## <span data-ttu-id="1719d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1719d-102">SYNOPSIS</span></span>
<span data-ttu-id="1719d-103">獲得 Azure 防火牆。</span><span class="sxs-lookup"><span data-stu-id="1719d-103">Gets a Azure Firewall.</span></span>

## <span data-ttu-id="1719d-104">語法</span><span class="sxs-lookup"><span data-stu-id="1719d-104">SYNTAX</span></span>

```
Get-AzFirewall [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1719d-105">描述</span><span class="sxs-lookup"><span data-stu-id="1719d-105">DESCRIPTION</span></span>
<span data-ttu-id="1719d-106">**Get-AzFirewall** Cmdlet 會取得資源群組中的一或多個防火牆。</span><span class="sxs-lookup"><span data-stu-id="1719d-106">The **Get-AzFirewall** cmdlet gets one or more Firewalls in a resource group.</span></span>

## <span data-ttu-id="1719d-107">例子</span><span class="sxs-lookup"><span data-stu-id="1719d-107">EXAMPLES</span></span>

### <span data-ttu-id="1719d-108">1：在資源群組中取回所有防火牆</span><span class="sxs-lookup"><span data-stu-id="1719d-108">1:  Retrieve all Firewalls in a resource group</span></span>
```
Get-AzFirewall -ResourceGroupName rgName

Name                       : azFw
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []
Zones                      : {}

Name                       : azFw1
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw1
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw1/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []
Zones                      : {}
```

<span data-ttu-id="1719d-109">此範例會取回資源群組 "rgName" 中所有的防火牆。</span><span class="sxs-lookup"><span data-stu-id="1719d-109">This example retrieves all Firewalls in resource group "rgName".</span></span>

### <span data-ttu-id="1719d-110">2：按名稱來取回防火牆</span><span class="sxs-lookup"><span data-stu-id="1719d-110">2:  Retrieve a Firewall by name</span></span>
```
Get-AzFirewall -ResourceGroupName rgName -Name azFw

Name                       : azFw
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []
Zones                      : {}
```

<span data-ttu-id="1719d-111">此範例會從資源群組 "rgName" 中，取回名為 "azFw" 的防火牆。</span><span class="sxs-lookup"><span data-stu-id="1719d-111">This example retrieves Firewall named "azFw" in resource group "rgName".</span></span>

### <span data-ttu-id="1719d-112">3：使用篩選來取回所有防火牆</span><span class="sxs-lookup"><span data-stu-id="1719d-112">3:  Retrieve all Firewalls with filtering</span></span>
```
Get-AzFirewall -Name azFw*

Name                       : azFw
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []
Zones                      : {}

Name                       : azFw1
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw1
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw1/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []
Zones                      : {}
```

<span data-ttu-id="1719d-113">此範例會從 "azFw" 開始的所有防火牆</span><span class="sxs-lookup"><span data-stu-id="1719d-113">This example retrieves all Firewalls that start with "azFw"</span></span>

### <span data-ttu-id="1719d-114">4：取回防火牆，然後將應用程式規則集合新增到防火牆</span><span class="sxs-lookup"><span data-stu-id="1719d-114">4:  Retrieve a firewall and then add a application rule collection to the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$appRule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$appRuleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $appRule -ActionType "Allow"
$azFw.AddApplicationRuleCollection($appRuleCollection)
```

<span data-ttu-id="1719d-115">此範例會取回防火牆，然後呼叫 AddApplicationRuleCollection 方法，將應用程式規則集合新增到防火牆。</span><span class="sxs-lookup"><span data-stu-id="1719d-115">This example retrieves a firewall, then adds a application rule collection to the firewall by calling method AddApplicationRuleCollection.</span></span>

### <span data-ttu-id="1719d-116">5：取回防火牆，然後將網路規則集合新增到防火牆</span><span class="sxs-lookup"><span data-stu-id="1719d-116">5:  Retrieve a firewall and then add a network rule collection to the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$netRule = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol "UDP" -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$netRuleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $netRule -ActionType "Allow"
$azFw.AddNetworkRuleCollection($netRuleCollection)
```

<span data-ttu-id="1719d-117">此範例會取回防火牆，然後呼叫方法 AddNetworkRuleCollection，將網路規則集合新增到防火牆。</span><span class="sxs-lookup"><span data-stu-id="1719d-117">This example retrieves a firewall, then adds a network rule collection to the firewall by calling method AddNetworkRuleCollection.</span></span>

### <span data-ttu-id="1719d-118">6：從防火牆中取用防火牆，然後依名稱來取用應用程式規則集合</span><span class="sxs-lookup"><span data-stu-id="1719d-118">6:  Retrieve a firewall and then retrieve a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$getAppRc=$azFw.GetApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="1719d-119">此範例會取得防火牆，然後依名稱取得規則集合，呼叫方法 GetApplicationRuleCollectionByName 位於防火牆物件上。</span><span class="sxs-lookup"><span data-stu-id="1719d-119">This example retrieves a firewall and then gets a rule collection by name, calling method GetApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="1719d-120">方法 GetApplicationRuleCollectionByName 的規則集合名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="1719d-120">The rule collection name for method GetApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="1719d-121">7：從防火牆中依名稱來取取防火牆，然後從網路規則集合中取回</span><span class="sxs-lookup"><span data-stu-id="1719d-121">7:  Retrieve a firewall and then retrieve a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$getNetRc=$azFw.GetNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="1719d-122">此範例會取得防火牆，然後依名稱取得規則集合，呼叫方法 GetNetworkRuleCollectionByName 位於防火牆物件上。</span><span class="sxs-lookup"><span data-stu-id="1719d-122">This example retrieves a firewall and then gets a rule collection by name, calling method GetNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="1719d-123">方法 GetNetworkRuleCollectionByName 的規則集合名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="1719d-123">The rule collection name for method GetNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="1719d-124">8：從防火牆中依名稱來取回防火牆，然後移除應用程式規則集合</span><span class="sxs-lookup"><span data-stu-id="1719d-124">8:  Retrieve a firewall and then remove a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="1719d-125">此範例會取回防火牆，然後依名稱移除規則集合，並呼叫防火牆物件上的 RemoveApplicationRuleCollectionByName。</span><span class="sxs-lookup"><span data-stu-id="1719d-125">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="1719d-126">方法 RemoveApplicationRuleCollectionByName 的規則集合名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="1719d-126">The rule collection name for method RemoveApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="1719d-127">9：從防火牆中依名稱來取回防火牆，然後移除網路規則集合</span><span class="sxs-lookup"><span data-stu-id="1719d-127">9:  Retrieve a firewall and then remove a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="1719d-128">此範例會取回防火牆，然後依名稱移除規則集合，呼叫方法為防火牆物件上的 RemoveNetworkRuleCollectionByName。</span><span class="sxs-lookup"><span data-stu-id="1719d-128">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="1719d-129">方法 RemoveNetworkRuleCollectionByName 的規則集合名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="1719d-129">The rule collection name for method RemoveNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="1719d-130">10：取回防火牆，然後配置防火牆</span><span class="sxs-lookup"><span data-stu-id="1719d-130">10:  Retrieve a firewall and then allocate the firewall</span></span>
```
$vnet=Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName "rgName"
$publicIp=Get-AzPublicIpAddress -Name "firewallpip" -ResourceGroupName "rgName"
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.Allocate($vnet, $publicIp)
```

<span data-ttu-id="1719d-131">此範例會取回防火牆，並呼叫防火牆上的配置，以使用與防火牆關聯的 (應用程式與) 集合來啟動防火牆服務。</span><span class="sxs-lookup"><span data-stu-id="1719d-131">This example retrieves a firewall and calls Allocate on the firewall to start the firewall service using the configuration (application and network rule collections) associated with the firewall.</span></span>

## <span data-ttu-id="1719d-132">參數</span><span class="sxs-lookup"><span data-stu-id="1719d-132">PARAMETERS</span></span>

### <span data-ttu-id="1719d-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1719d-133">-DefaultProfile</span></span>
<span data-ttu-id="1719d-134">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1719d-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1719d-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="1719d-135">-Name</span></span>
<span data-ttu-id="1719d-136">指定此 Cmdlet 所獲取的防火牆名稱。</span><span class="sxs-lookup"><span data-stu-id="1719d-136">Specifies the name of the Firewall that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1719d-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1719d-137">-ResourceGroupName</span></span>
<span data-ttu-id="1719d-138">指定防火牆所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="1719d-138">Specifies the name of the resource group that Firewall belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1719d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1719d-139">CommonParameters</span></span>
<span data-ttu-id="1719d-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1719d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1719d-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1719d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1719d-142">輸入</span><span class="sxs-lookup"><span data-stu-id="1719d-142">INPUTS</span></span>

### <span data-ttu-id="1719d-143">System.String</span><span class="sxs-lookup"><span data-stu-id="1719d-143">System.String</span></span>

## <span data-ttu-id="1719d-144">輸出</span><span class="sxs-lookup"><span data-stu-id="1719d-144">OUTPUTS</span></span>

### <span data-ttu-id="1719d-145">Microsoft.Azure.Commands.Network.models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="1719d-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

### <span data-ttu-id="1719d-146">System.Collections.Generic.IEnumerable'1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="1719d-146">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="1719d-147">筆記</span><span class="sxs-lookup"><span data-stu-id="1719d-147">NOTES</span></span>

## <span data-ttu-id="1719d-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="1719d-148">RELATED LINKS</span></span>

[<span data-ttu-id="1719d-149">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="1719d-149">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="1719d-150">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="1719d-150">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="1719d-151">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="1719d-151">Set-AzFirewall</span></span>](./Set-AzFirewall.md)
