---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5AECCBD7-1FDE-4217-9F59-36328062E669
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityGroup.md
ms.openlocfilehash: 46106379160ee593748a95489c2641d43114d863
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621983"
---
# <span data-ttu-id="25c8e-101">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="25c8e-101">Get-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="25c8e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="25c8e-102">SYNOPSIS</span></span>
<span data-ttu-id="25c8e-103">取得網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="25c8e-103">Gets a network security group.</span></span>

## <span data-ttu-id="25c8e-104">句法</span><span class="sxs-lookup"><span data-stu-id="25c8e-104">SYNTAX</span></span>

### <span data-ttu-id="25c8e-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="25c8e-105">NoExpand</span></span>
```
Get-AzNetworkSecurityGroup [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25c8e-106">擴充</span><span class="sxs-lookup"><span data-stu-id="25c8e-106">Expand</span></span>
```
Get-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25c8e-107">說明</span><span class="sxs-lookup"><span data-stu-id="25c8e-107">DESCRIPTION</span></span>
<span data-ttu-id="25c8e-108">**AzNetworkSecurityGroup** Cmdlet 會取得 Azure 網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="25c8e-108">The **Get-AzNetworkSecurityGroup** cmdlet gets an Azure network security group.</span></span>

## <span data-ttu-id="25c8e-109">示例</span><span class="sxs-lookup"><span data-stu-id="25c8e-109">EXAMPLES</span></span>

### <span data-ttu-id="25c8e-110">1：檢索現有的網路安全性群組</span><span class="sxs-lookup"><span data-stu-id="25c8e-110">1: Retrieve an existing network security group</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName "rg1"

Name                        : nsg1
ResourceGroupName           : rg1
Location                    : eastus
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provider
                              s/Microsoft.Network/networkInterfaces/nsg1
Etag                        : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid                : 00000000-0000-0000-0000-000000000000
ProvisioningState           : Succeeded
Tags                        :
VirtualMachine              : null
IpConfigurations            : [
                                {
                                  "Name": "ipconfig1",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                              /providers/Microsoft.Network/networkInterfaces/nsg1/ipConfigurations/ipcon
                              fig1",
                                  "PrivateIpAddress": "x.x.x.x",
                                  "PrivateIpAllocationMethod": "Dynamic",
                                  "Subnet": {
                                    "Delegations": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                              /providers/Microsoft.Network/virtualNetworks/vnetcrptestps2673/subnets/subnetcrptestp
                              s2673",
                                    "ServiceAssociationLinks": []
                                  },
                                  "PublicIpAddress": {
                                    "IpTags": [],
                                    "Zones": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                              /providers/Microsoft.Network/publicIPAddresses/pubipcrptestps2673"
                                  },
                                  "ProvisioningState": "Succeeded",
                                  "PrivateIpAddressVersion": "IPv4",
                                  "LoadBalancerBackendAddressPools": [],
                                  "LoadBalancerInboundNatRules": [],
                                  "Primary": true,
                                  "ApplicationGatewayBackendAddressPools": [],
                                  "ApplicationSecurityGroups": []
                                }
                              ]
DnsSettings                 : {
                                "DnsServers": [],
                                "AppliedDnsServers": [],
                                "InternalDomainNameSuffix": "xxxxxxxxxxxxxxx.xx.internal.cloudapp.net"
                              }
EnableIPForwarding          : False
EnableAcceleratedNetworking : False
NetworkSecurityGroup        : null
Primary                     :
MacAddress                  :
```

<span data-ttu-id="25c8e-111">這個命令會傳回資源群組 "rg1" 中的 Azure 網路安全性群組 "nsg1" 的內容</span><span class="sxs-lookup"><span data-stu-id="25c8e-111">This command returns contents of Azure network security group "nsg1" in resource group "rg1"</span></span>

### <span data-ttu-id="25c8e-112">2：使用篩選列出現有的網路安全性群組</span><span class="sxs-lookup"><span data-stu-id="25c8e-112">2: List existing network security groups using filtering</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg*

Name                        : nsg1
ResourceGroupName           : rg1
Location                    : eastus
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provider
                              s/Microsoft.Network/networkInterfaces/nsg1
Etag                        : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid                : 00000000-0000-0000-0000-000000000000
ProvisioningState           : Succeeded
Tags                        :
VirtualMachine              : null
IpConfigurations            : [
                                {
                                  "Name": "ipconfig1",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                              /providers/Microsoft.Network/networkInterfaces/nsg1/ipConfigurations/ipcon
                              fig1",
                                  "PrivateIpAddress": "x.x.x.x",
                                  "PrivateIpAllocationMethod": "Dynamic",
                                  "Subnet": {
                                    "Delegations": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                              /providers/Microsoft.Network/virtualNetworks/vnetcrptestps2673/subnets/subnetcrptestp
                              s2673",
                                    "ServiceAssociationLinks": []
                                  },
                                  "PublicIpAddress": {
                                    "IpTags": [],
                                    "Zones": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                              /providers/Microsoft.Network/publicIPAddresses/pubipcrptestps2673"
                                  },
                                  "ProvisioningState": "Succeeded",
                                  "PrivateIpAddressVersion": "IPv4",
                                  "LoadBalancerBackendAddressPools": [],
                                  "LoadBalancerInboundNatRules": [],
                                  "Primary": true,
                                  "ApplicationGatewayBackendAddressPools": [],
                                  "ApplicationSecurityGroups": []
                                }
                              ]
DnsSettings                 : {
                                "DnsServers": [],
                                "AppliedDnsServers": [],
                                "InternalDomainNameSuffix": "xxxxxxxxxxxxxxx.xx.internal.cloudapp.net"
                              }
EnableIPForwarding          : False
EnableAcceleratedNetworking : False
NetworkSecurityGroup        : null
Primary                     :
MacAddress                  :
```

<span data-ttu-id="25c8e-113">這個命令會傳回以 "nsg" 開頭的 Azure 網路安全性群組內容</span><span class="sxs-lookup"><span data-stu-id="25c8e-113">This command returns contents of Azure network security groups that start with "nsg"</span></span>

## <span data-ttu-id="25c8e-114">參數</span><span class="sxs-lookup"><span data-stu-id="25c8e-114">PARAMETERS</span></span>

### <span data-ttu-id="25c8e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25c8e-115">-DefaultProfile</span></span>
<span data-ttu-id="25c8e-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="25c8e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25c8e-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="25c8e-117">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25c8e-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="25c8e-118">-Name</span></span>
<span data-ttu-id="25c8e-119">指定此 Cmdlet 所取得之網路安全性群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="25c8e-119">Specifies the name of the network security group that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="25c8e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25c8e-120">-ResourceGroupName</span></span>
<span data-ttu-id="25c8e-121">指定網路安全性群組所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="25c8e-121">Specifies the name of the resource group that the network security group belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="25c8e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25c8e-122">CommonParameters</span></span>
<span data-ttu-id="25c8e-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="25c8e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25c8e-124">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="25c8e-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25c8e-125">輸入</span><span class="sxs-lookup"><span data-stu-id="25c8e-125">INPUTS</span></span>

### <span data-ttu-id="25c8e-126">System.object</span><span class="sxs-lookup"><span data-stu-id="25c8e-126">System.String</span></span>

## <span data-ttu-id="25c8e-127">輸出</span><span class="sxs-lookup"><span data-stu-id="25c8e-127">OUTPUTS</span></span>

### <span data-ttu-id="25c8e-128">PSNetworkSecurityGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="25c8e-128">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="25c8e-129">筆記</span><span class="sxs-lookup"><span data-stu-id="25c8e-129">NOTES</span></span>

## <span data-ttu-id="25c8e-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="25c8e-130">RELATED LINKS</span></span>

[<span data-ttu-id="25c8e-131">新-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="25c8e-131">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="25c8e-132">移除-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="25c8e-132">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)

[<span data-ttu-id="25c8e-133">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="25c8e-133">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)


