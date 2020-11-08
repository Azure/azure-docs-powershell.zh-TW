---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E066BBFA-2E03-431D-85D1-99F230B6AC59
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterface.md
ms.openlocfilehash: 1f49c2de253b41db97719933111a5ec2f9b861d5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137660"
---
# <span data-ttu-id="d1a41-101">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d1a41-101">Get-AzNetworkInterface</span></span>

## <span data-ttu-id="d1a41-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d1a41-102">SYNOPSIS</span></span>
<span data-ttu-id="d1a41-103">取得網路介面。</span><span class="sxs-lookup"><span data-stu-id="d1a41-103">Gets a network interface.</span></span>

## <span data-ttu-id="d1a41-104">句法</span><span class="sxs-lookup"><span data-stu-id="d1a41-104">SYNTAX</span></span>

### <span data-ttu-id="d1a41-105">NoExpandStandAloneNic (預設) </span><span class="sxs-lookup"><span data-stu-id="d1a41-105">NoExpandStandAloneNic (Default)</span></span>
```
Get-AzNetworkInterface [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1a41-106">ExpandStandAloneNic</span><span class="sxs-lookup"><span data-stu-id="d1a41-106">ExpandStandAloneNic</span></span>
```
Get-AzNetworkInterface -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1a41-107">NoExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="d1a41-107">NoExpandScaleSetNic</span></span>
```
Get-AzNetworkInterface [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1a41-108">ExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="d1a41-108">ExpandScaleSetNic</span></span>
```
Get-AzNetworkInterface -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d1a41-109">GetByResourceIdExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1a41-109">GetByResourceIdExpandParameterSet</span></span>
```
Get-AzNetworkInterface -ResourceId <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d1a41-110">GetByResourceIdNoExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1a41-110">GetByResourceIdNoExpandParameterSet</span></span>
```
Get-AzNetworkInterface -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1a41-111">說明</span><span class="sxs-lookup"><span data-stu-id="d1a41-111">DESCRIPTION</span></span>
<span data-ttu-id="d1a41-112">**AzNetworkInterface** Cmdlet 會取得 azure 網路介面或資源群組中的 azure 網路介面清單。</span><span class="sxs-lookup"><span data-stu-id="d1a41-112">The **Get-AzNetworkInterface** cmdlet gets an Azure network interface or a list of Azure network interfaces in a resource group.</span></span>

## <span data-ttu-id="d1a41-113">示例</span><span class="sxs-lookup"><span data-stu-id="d1a41-113">EXAMPLES</span></span>

### <span data-ttu-id="d1a41-114">範例1：取得所有網路介面</span><span class="sxs-lookup"><span data-stu-id="d1a41-114">Example 1: Get all network interfaces</span></span>
```
PS C:\> Get-AzNetworkInterface

Name                        : test1
ResourceGroupName           : ResourceGroup1
Location                    : eastus
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/providers/Micros
                              oft.Network/networkInterfaces/test1
Etag                        : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid                : 00000000-0000-0000-0000-000000000000
ProvisioningState           : Succeeded
Tags                        :
VirtualMachine              : {
                                "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/provide
                              rs/Microsoft.Compute/virtualMachines/test1"
                              }
IpConfigurations            : [
                                {
                                  "Name": "test1",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/provi
                              ders/Microsoft.Network/networkInterfaces/test1/ipConfigurations/test1",
                                  "PrivateIpAddress": "x.x.x.x",
                                  "PrivateIpAllocationMethod": "Dynamic",
                                  "Subnet": {
                                    "Delegations": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/pro
                              viders/Microsoft.Network/virtualNetworks/test1/subnets/test1",
                                    "ServiceAssociationLinks": []
                                  },
                                  "PublicIpAddress": {
                                    "IpTags": [],
                                    "Zones": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/pro
                              viders/Microsoft.Network/publicIPAddresses/test1"
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
                                "AppliedDnsServers": []
                              }
EnableIPForwarding          : False
EnableAcceleratedNetworking : False
NetworkSecurityGroup        : {
                                "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/provide
                              rs/Microsoft.Network/networkSecurityGroups/test1"
                              }
Primary                     : True
MacAddress                  :
```

<span data-ttu-id="d1a41-115">這個命令會取得目前訂閱的所有網路介面。</span><span class="sxs-lookup"><span data-stu-id="d1a41-115">This command gets all network interfaces for the current subscription.</span></span>

### <span data-ttu-id="d1a41-116">範例2：取得所有具有特定配定狀態的網路介面</span><span class="sxs-lookup"><span data-stu-id="d1a41-116">Example 2: Get all network interfaces with a specific provisioning state</span></span>
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" | Where-Object {$_.ProvisioningState -eq 'Succeeded'}

Name                        : test1
ResourceGroupName           : ResourceGroup1
Location                    : eastus
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/providers/Micros
                              oft.Network/networkInterfaces/test1
Etag                        : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid                : 00000000-0000-0000-0000-000000000000
ProvisioningState           : Succeeded
Tags                        :
VirtualMachine              : {
                                "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/provide
                              rs/Microsoft.Compute/virtualMachines/test1"
                              }
IpConfigurations            : [
                                {
                                  "Name": "test1",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/provi
                              ders/Microsoft.Network/networkInterfaces/test1/ipConfigurations/test1",
                                  "PrivateIpAddress": "x.x.x.x",
                                  "PrivateIpAllocationMethod": "Dynamic",
                                  "Subnet": {
                                    "Delegations": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/pro
                              viders/Microsoft.Network/virtualNetworks/test1/subnets/test1",
                                    "ServiceAssociationLinks": []
                                  },
                                  "PublicIpAddress": {
                                    "IpTags": [],
                                    "Zones": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/pro
                              viders/Microsoft.Network/publicIPAddresses/test1"
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
                                "AppliedDnsServers": []
                              }
EnableIPForwarding          : False
EnableAcceleratedNetworking : False
NetworkSecurityGroup        : {
                                "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/provide
                              rs/Microsoft.Network/networkSecurityGroups/test1"
                              }
Primary                     : True
MacAddress                  :
```

<span data-ttu-id="d1a41-117">這個命令會取得名為 ResourceGroup1 的資源群組中的所有網路介面，且該資源群組的 [已成功] 提供狀態。</span><span class="sxs-lookup"><span data-stu-id="d1a41-117">This command gets all network interfaces in the resource group named ResourceGroup1 that has a provisioning state of succeeded.</span></span>

### <span data-ttu-id="d1a41-118">範例3：使用篩選取得網路介面</span><span class="sxs-lookup"><span data-stu-id="d1a41-118">Example 3: Get network interfaces using filtering</span></span>
```
PS C:\> Get-AzNetworkInterface -Name test*

Name                        : test1
ResourceGroupName           : ResourceGroup1
Location                    : eastus
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/providers/Micros
                              oft.Network/networkInterfaces/test1
Etag                        : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid                : 00000000-0000-0000-0000-000000000000
ProvisioningState           : Succeeded
Tags                        :
VirtualMachine              : {
                                "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/provide
                              rs/Microsoft.Compute/virtualMachines/test1"
                              }
IpConfigurations            : [
                                {
                                  "Name": "test1",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/provi
                              ders/Microsoft.Network/networkInterfaces/test1/ipConfigurations/test1",
                                  "PrivateIpAddress": "x.x.x.x",
                                  "PrivateIpAllocationMethod": "Dynamic",
                                  "Subnet": {
                                    "Delegations": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/pro
                              viders/Microsoft.Network/virtualNetworks/test1/subnets/test1",
                                    "ServiceAssociationLinks": []
                                  },
                                  "PublicIpAddress": {
                                    "IpTags": [],
                                    "Zones": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/pro
                              viders/Microsoft.Network/publicIPAddresses/test1"
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
                                "AppliedDnsServers": []
                              }
EnableIPForwarding          : False
EnableAcceleratedNetworking : False
NetworkSecurityGroup        : {
                                "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/provide
                              rs/Microsoft.Network/networkSecurityGroups/test1"
                              }
Primary                     : True
MacAddress                  :
```

<span data-ttu-id="d1a41-119">這個命令會取得以「test」開頭的目前訂閱的所有網路介面。</span><span class="sxs-lookup"><span data-stu-id="d1a41-119">This command gets all network interfaces for the current subscription that start with "test".</span></span>

## <span data-ttu-id="d1a41-120">參數</span><span class="sxs-lookup"><span data-stu-id="d1a41-120">PARAMETERS</span></span>

### <span data-ttu-id="d1a41-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1a41-121">-DefaultProfile</span></span>
<span data-ttu-id="d1a41-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d1a41-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1a41-123">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="d1a41-123">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: ExpandStandAloneNic, ExpandScaleSetNic, GetByResourceIdExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1a41-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="d1a41-124">-Name</span></span>
<span data-ttu-id="d1a41-125">指定此 Cmdlet 所取得之網路介面的名稱。</span><span class="sxs-lookup"><span data-stu-id="d1a41-125">Specifies the name of the network interface that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneNic, NoExpandScaleSetNic
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneNic, ExpandScaleSetNic
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="d1a41-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1a41-126">-ResourceGroupName</span></span>
<span data-ttu-id="d1a41-127">指定此 Cmdlet 取得網路介面之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d1a41-127">Specifies the name of the resource group from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneNic
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneNic, NoExpandScaleSetNic, ExpandScaleSetNic
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="d1a41-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1a41-128">-ResourceId</span></span>
<span data-ttu-id="d1a41-129">網路介面的 Azure 資源管理器識別碼。</span><span class="sxs-lookup"><span data-stu-id="d1a41-129">The Azure resource manager id of the network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdExpandParameterSet, GetByResourceIdNoExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1a41-130">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="d1a41-130">-VirtualMachineIndex</span></span>
<span data-ttu-id="d1a41-131">指定此 Cmdlet 取得網路介面之虛擬機器規模集的虛擬機器索引。</span><span class="sxs-lookup"><span data-stu-id="d1a41-131">Specifies the virtual machine index of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetNic
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetNic
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1a41-132">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="d1a41-132">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="d1a41-133">指定此 Cmdlet 取得網路介面的虛擬機器規模集的名稱。</span><span class="sxs-lookup"><span data-stu-id="d1a41-133">Specifies the name of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetNic
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetNic
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1a41-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1a41-134">CommonParameters</span></span>
<span data-ttu-id="d1a41-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d1a41-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1a41-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d1a41-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1a41-137">輸入</span><span class="sxs-lookup"><span data-stu-id="d1a41-137">INPUTS</span></span>

### <span data-ttu-id="d1a41-138">System.object</span><span class="sxs-lookup"><span data-stu-id="d1a41-138">System.String</span></span>

## <span data-ttu-id="d1a41-139">輸出</span><span class="sxs-lookup"><span data-stu-id="d1a41-139">OUTPUTS</span></span>

### <span data-ttu-id="d1a41-140">PSNetworkInterface 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d1a41-140">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="d1a41-141">筆記</span><span class="sxs-lookup"><span data-stu-id="d1a41-141">NOTES</span></span>

## <span data-ttu-id="d1a41-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="d1a41-142">RELATED LINKS</span></span>

[<span data-ttu-id="d1a41-143">新-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d1a41-143">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="d1a41-144">移除-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d1a41-144">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)

[<span data-ttu-id="d1a41-145">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d1a41-145">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)


