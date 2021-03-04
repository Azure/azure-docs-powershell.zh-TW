---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9160A21D-0F83-415B-830B-F35C8B863E90
online version: https://docs.microsoft.com/powershell/module/az.network/add-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 11481d2063b6acb2938361726de45f72dba539c0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904029"
---
# <span data-ttu-id="a36e3-101">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a36e3-101">Add-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="a36e3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a36e3-102">SYNOPSIS</span></span>
<span data-ttu-id="a36e3-103">新增網路安全性規則組至網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="a36e3-103">Adds a network security rule configuration to a network security group.</span></span>

## <span data-ttu-id="a36e3-104">語法</span><span class="sxs-lookup"><span data-stu-id="a36e3-104">SYNTAX</span></span>

### <span data-ttu-id="a36e3-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="a36e3-105">SetByResource (Default)</span></span>
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a36e3-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a36e3-106">SetByResourceId</span></span>
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a36e3-107">描述</span><span class="sxs-lookup"><span data-stu-id="a36e3-107">DESCRIPTION</span></span>
<span data-ttu-id="a36e3-108">**Add-AzNetworkSecurityRuleConfig** Cmdlet 會新增網路安全性規則組至 Azure 網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="a36e3-108">The **Add-AzNetworkSecurityRuleConfig** cmdlet adds a network security rule configuration to an Azure network security group.</span></span>

## <span data-ttu-id="a36e3-109">例子</span><span class="sxs-lookup"><span data-stu-id="a36e3-109">EXAMPLES</span></span>

### <span data-ttu-id="a36e3-110">1：新增網路安全性群組</span><span class="sxs-lookup"><span data-stu-id="a36e3-110">1: Adding a network security group</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 | 
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access 
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet 
    -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389 | 
    Set-AzNetworkSecurityGroup
```

<span data-ttu-id="a36e3-111">第一個命令會從資源群組 "rg1" 中，從名稱為 "nsg1" 的 Azure 網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="a36e3-111">The first command retrieves an Azure network security group named "nsg1" from resource group "rg1".</span></span> <span data-ttu-id="a36e3-112">第二個命令會新增名為「rdp-rule」的網路安全性規則，允許流量從埠 3389 上的網際網路流量到已取回的網路安全性群組物件。</span><span class="sxs-lookup"><span data-stu-id="a36e3-112">The second command adds a network security rule named "rdp-rule" that allows traffic from internet on port 3389 to the retrieved network security group object.</span></span> <span data-ttu-id="a36e3-113">保留已修改的 Azure 網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="a36e3-113">Persists the modified Azure network security group.</span></span>

### <span data-ttu-id="a36e3-114">2：使用應用程式安全性群組新增安全性規則</span><span class="sxs-lookup"><span data-stu-id="a36e3-114">2: Adding a new security rule with application security groups</span></span>
```
$srcAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name srcAsg -Location "West US"
$destAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name destAsg -Location "West US"

Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 |
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceApplicationSecurityGroup
    $srcAsg -SourcePortRange * -DestinationApplicationSecurityGroup $destAsg -DestinationPortRange 3389 |
Set-AzNetworkSecurityGroup
```

<span data-ttu-id="a36e3-115">首先，我們建立兩個新的應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="a36e3-115">First, we create two new application security groups.</span></span> <span data-ttu-id="a36e3-116">接著，從資源群組 "rg1" 中，將 Azure 網路安全性群組命名為 "nsg1"。</span><span class="sxs-lookup"><span data-stu-id="a36e3-116">Then, we retrieve an Azure network security group named "nsg1" from resource group "rg1".</span></span> <span data-ttu-id="a36e3-117">並新增名為「rdp-rule」的網路安全性規則。</span><span class="sxs-lookup"><span data-stu-id="a36e3-117">and add a network security rule named "rdp-rule" to it.</span></span> <span data-ttu-id="a36e3-118">規則允許流量從應用程式安全性群組 "srcAsg" 的所有 IP 組流量，到埠 3389 上 "destAsg" 的所有 IP 組。</span><span class="sxs-lookup"><span data-stu-id="a36e3-118">The rule allows traffic from all the IP configurations in the application security group "srcAsg" to all the IP configurations in "destAsg" on port 3389.</span></span> <span data-ttu-id="a36e3-119">新增規則之後，我們會保留已修改的 Azure 網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="a36e3-119">After adding the rule, we persist the modified Azure network security group.</span></span>

## <span data-ttu-id="a36e3-120">參數</span><span class="sxs-lookup"><span data-stu-id="a36e3-120">PARAMETERS</span></span>

### <span data-ttu-id="a36e3-121">-Access</span><span class="sxs-lookup"><span data-stu-id="a36e3-121">-Access</span></span>
<span data-ttu-id="a36e3-122">指定是否允許或拒絕網路流量。</span><span class="sxs-lookup"><span data-stu-id="a36e3-122">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="a36e3-123">此參數可接受的值為：允許和拒絕。</span><span class="sxs-lookup"><span data-stu-id="a36e3-123">The acceptable values for this parameter are: Allow and Deny.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a36e3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a36e3-124">-DefaultProfile</span></span>
<span data-ttu-id="a36e3-125">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a36e3-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a36e3-126">-描述</span><span class="sxs-lookup"><span data-stu-id="a36e3-126">-Description</span></span>
<span data-ttu-id="a36e3-127">指定網路安全性規則組配置的描述。</span><span class="sxs-lookup"><span data-stu-id="a36e3-127">Specifies a description of a network security rule configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a36e3-128">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a36e3-128">-DestinationAddressPrefix</span></span>
<span data-ttu-id="a36e3-129">指定目的地位址首碼。</span><span class="sxs-lookup"><span data-stu-id="a36e3-129">Specifies a destination address prefix.</span></span>
<span data-ttu-id="a36e3-130">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a36e3-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a36e3-131">CIDR 位址的無 (域) 路由</span><span class="sxs-lookup"><span data-stu-id="a36e3-131">A Classless Interdomain Routing (CIDR) address</span></span>
- <span data-ttu-id="a36e3-132">目的地 IP 位址範圍</span><span class="sxs-lookup"><span data-stu-id="a36e3-132">A destination IP address range</span></span>
- <span data-ttu-id="a36e3-133">萬用字元 (\*) 比對任何 IP 位址。您可以使用 VirtualNetwork、AzureLoadBalancer 和 Internet 等標記。</span><span class="sxs-lookup"><span data-stu-id="a36e3-133">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="a36e3-134">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a36e3-134">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="a36e3-135">應用程式安全性群組設定為規則的目的地。</span><span class="sxs-lookup"><span data-stu-id="a36e3-135">The application security group set as destination for the rule.</span></span> <span data-ttu-id="a36e3-136">它無法與 "DestinationAddressPrefix" 參數一起使用。</span><span class="sxs-lookup"><span data-stu-id="a36e3-136">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a36e3-137">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="a36e3-137">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="a36e3-138">應用程式安全性群組設定為規則的目的地。</span><span class="sxs-lookup"><span data-stu-id="a36e3-138">The application security group set as destination for the rule.</span></span> <span data-ttu-id="a36e3-139">它無法與 "DestinationAddressPrefix" 參數一起使用。</span><span class="sxs-lookup"><span data-stu-id="a36e3-139">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a36e3-140">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="a36e3-140">-DestinationPortRange</span></span>
<span data-ttu-id="a36e3-141">指定目的地埠或範圍。</span><span class="sxs-lookup"><span data-stu-id="a36e3-141">Specifies a destination port or range.</span></span>
<span data-ttu-id="a36e3-142">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a36e3-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a36e3-143">整數</span><span class="sxs-lookup"><span data-stu-id="a36e3-143">An integer</span></span>
- <span data-ttu-id="a36e3-144">介於 0 到 65535 之間的整數範圍</span><span class="sxs-lookup"><span data-stu-id="a36e3-144">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="a36e3-145">\* (\*) 字元來比對任何埠</span><span class="sxs-lookup"><span data-stu-id="a36e3-145">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="a36e3-146">-方向</span><span class="sxs-lookup"><span data-stu-id="a36e3-146">-Direction</span></span>
<span data-ttu-id="a36e3-147">指定規則是評估內流量還是外發流量。</span><span class="sxs-lookup"><span data-stu-id="a36e3-147">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="a36e3-148">此參數可接受的值為：輸入和外發。</span><span class="sxs-lookup"><span data-stu-id="a36e3-148">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Inbound, Outbound

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a36e3-149">-名稱</span><span class="sxs-lookup"><span data-stu-id="a36e3-149">-Name</span></span>
<span data-ttu-id="a36e3-150">指定網路安全性規則組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a36e3-150">Specifies the name of a network security rule configuration.</span></span>

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

### <span data-ttu-id="a36e3-151">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a36e3-151">-NetworkSecurityGroup</span></span>
<span data-ttu-id="a36e3-152">指定 **NetworkSecurityGroup** 物件。</span><span class="sxs-lookup"><span data-stu-id="a36e3-152">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="a36e3-153">此 Cmdlet 會新增網路安全性規則設定至此參數指定的物件。</span><span class="sxs-lookup"><span data-stu-id="a36e3-153">This cmdlet adds a network security rule configuration to the object that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a36e3-154">-優先順序</span><span class="sxs-lookup"><span data-stu-id="a36e3-154">-Priority</span></span>
<span data-ttu-id="a36e3-155">指定規則配置的優先順序。</span><span class="sxs-lookup"><span data-stu-id="a36e3-155">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="a36e3-156">此參數可接受的值為：介於 100 和 4096 之間的整數。</span><span class="sxs-lookup"><span data-stu-id="a36e3-156">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>
<span data-ttu-id="a36e3-157">優先順序數位必須是唯一的，因為集合中每個規則都是唯一的。</span><span class="sxs-lookup"><span data-stu-id="a36e3-157">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="a36e3-158">優先順序數位越低，規則的優先順序越高。</span><span class="sxs-lookup"><span data-stu-id="a36e3-158">The lower the priority number, the higher the priority of the rule.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a36e3-159">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="a36e3-159">-Protocol</span></span>
<span data-ttu-id="a36e3-160">指定規則組配置所適用的網路通訊協定。</span><span class="sxs-lookup"><span data-stu-id="a36e3-160">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="a36e3-161">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a36e3-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a36e3-162">Tcp</span><span class="sxs-lookup"><span data-stu-id="a36e3-162">Tcp</span></span>
- <span data-ttu-id="a36e3-163">Udp</span><span class="sxs-lookup"><span data-stu-id="a36e3-163">Udp</span></span>
- <span data-ttu-id="a36e3-164">\*\* (\*) 兩者相符</span><span class="sxs-lookup"><span data-stu-id="a36e3-164">Wildcard character (\*) to match both</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Tcp, Udp, *

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a36e3-165">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a36e3-165">-SourceAddressPrefix</span></span>
<span data-ttu-id="a36e3-166">指定來源位址首碼。</span><span class="sxs-lookup"><span data-stu-id="a36e3-166">Specifies a source address prefix.</span></span>
<span data-ttu-id="a36e3-167">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a36e3-167">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a36e3-168">A CIDR</span><span class="sxs-lookup"><span data-stu-id="a36e3-168">A CIDR</span></span>
- <span data-ttu-id="a36e3-169">來源 IP 範圍</span><span class="sxs-lookup"><span data-stu-id="a36e3-169">A source IP range</span></span>
- <span data-ttu-id="a36e3-170">\* (\*) 字元，以比對任何 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="a36e3-170">A wildcard character (\*) to match any IP address.</span></span>
<span data-ttu-id="a36e3-171">您也可以使用虛擬網路、AzureLoadBalancer 和網際網路等標記。</span><span class="sxs-lookup"><span data-stu-id="a36e3-171">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="a36e3-172">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a36e3-172">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="a36e3-173">應用程式安全性群組設定為規則的來源。</span><span class="sxs-lookup"><span data-stu-id="a36e3-173">The application security group set as source for the rule.</span></span> <span data-ttu-id="a36e3-174">它無法與 'SourceAddressPrefix' 參數一起使用。</span><span class="sxs-lookup"><span data-stu-id="a36e3-174">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a36e3-175">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="a36e3-175">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="a36e3-176">應用程式安全性群組設定為規則的來源。</span><span class="sxs-lookup"><span data-stu-id="a36e3-176">The application security group set as source for the rule.</span></span> <span data-ttu-id="a36e3-177">它無法與 'SourceAddressPrefix' 參數一起使用。</span><span class="sxs-lookup"><span data-stu-id="a36e3-177">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a36e3-178">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="a36e3-178">-SourcePortRange</span></span>
<span data-ttu-id="a36e3-179">指定來源埠或範圍。</span><span class="sxs-lookup"><span data-stu-id="a36e3-179">Specifies a source port or range.</span></span>
<span data-ttu-id="a36e3-180">此值會以整數表示、範圍介於 0 到 65535 之間，或以萬用字元 (\*) 來比對任何來源埠。</span><span class="sxs-lookup"><span data-stu-id="a36e3-180">This value is expressed as an integer, as a range between 0 and 65535, or as a wildcard character (\*) to match any source port.</span></span>

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

### <span data-ttu-id="a36e3-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a36e3-181">CommonParameters</span></span>
<span data-ttu-id="a36e3-182">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a36e3-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a36e3-183">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a36e3-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a36e3-184">輸入</span><span class="sxs-lookup"><span data-stu-id="a36e3-184">INPUTS</span></span>

### <span data-ttu-id="a36e3-185">Microsoft.Azure.Commands.Network.models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a36e3-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="a36e3-186">輸出</span><span class="sxs-lookup"><span data-stu-id="a36e3-186">OUTPUTS</span></span>

### <span data-ttu-id="a36e3-187">Microsoft.Azure.Commands.Network.models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a36e3-187">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="a36e3-188">筆記</span><span class="sxs-lookup"><span data-stu-id="a36e3-188">NOTES</span></span>

## <span data-ttu-id="a36e3-189">相關連結</span><span class="sxs-lookup"><span data-stu-id="a36e3-189">RELATED LINKS</span></span>

[<span data-ttu-id="a36e3-190">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a36e3-190">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="a36e3-191">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a36e3-191">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="a36e3-192">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a36e3-192">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="a36e3-193">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a36e3-193">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


