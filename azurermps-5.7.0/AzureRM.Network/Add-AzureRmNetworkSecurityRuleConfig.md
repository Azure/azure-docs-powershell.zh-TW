---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9160A21D-0F83-415B-830B-F35C8B863E90
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermnetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmNetworkSecurityRuleConfig.md
ms.openlocfilehash: 0efe2c4492a9fb91ffd2083c9f23cfc314c2d3fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451448"
---
# <span data-ttu-id="43104-101">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="43104-101">Add-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="43104-102">摘要</span><span class="sxs-lookup"><span data-stu-id="43104-102">SYNOPSIS</span></span>
<span data-ttu-id="43104-103">新增網路安全規則設定至網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="43104-103">Adds a network security rule configuration to a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43104-104">句法</span><span class="sxs-lookup"><span data-stu-id="43104-104">SYNTAX</span></span>

### <span data-ttu-id="43104-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="43104-105">SetByResource (Default)</span></span>
```
Add-AzureRmNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DestinationApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="43104-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="43104-106">SetByResourceId</span></span>
```
Add-AzureRmNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DestinationApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-Access <String>]
 [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43104-107">說明</span><span class="sxs-lookup"><span data-stu-id="43104-107">DESCRIPTION</span></span>
<span data-ttu-id="43104-108">**AzureRmNetworkSecurityRuleConfig** Cmdlet 會將網路安全規則設定新增至 Azure 網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="43104-108">The **Add-AzureRmNetworkSecurityRuleConfig** cmdlet adds a network security rule configuration to an Azure network security group.</span></span>

## <span data-ttu-id="43104-109">示例</span><span class="sxs-lookup"><span data-stu-id="43104-109">EXAMPLES</span></span>

### <span data-ttu-id="43104-110">1：新增網路安全性群組</span><span class="sxs-lookup"><span data-stu-id="43104-110">1: Adding a network security group</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 | 
Add-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access 
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet 
    -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389 | 
    Set-AzureRmNetworkSecurityGroup
```

<span data-ttu-id="43104-111">第一個命令會從資源群組 "rg1" 檢索名為 "nsg1" 的 Azure 網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="43104-111">The first command retrieves an Azure network security group named "nsg1" from resource group "rg1".</span></span> <span data-ttu-id="43104-112">第二個命令會將一個名為「rdp-rule」的網路安全規則新增，允許從埠3389上的網際網路通訊到檢索到的網路安全群組物件。</span><span class="sxs-lookup"><span data-stu-id="43104-112">The second command adds a network security rule named "rdp-rule" that allows traffic from internet on port 3389 to the retrieved network security group object.</span></span> <span data-ttu-id="43104-113">保持已修改的 Azure 網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="43104-113">Persists the modified Azure network security group.</span></span>

### <span data-ttu-id="43104-114">1：使用應用程式安全性群組新增新的安全性規則</span><span class="sxs-lookup"><span data-stu-id="43104-114">1: Adding a new security rule with application security groups</span></span>
```
$srcAsg = New-AzureRmApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name srcAsg -Location "West US"
$destAsg = New-AzureRmApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name destAsg -Location "West US"

Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 |
Add-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceApplicationSecurityGroup
    $srcAsg -SourcePortRange * -DestinationApplicationSecurityGroup $destAsg -DestinationPortRange 3389 |
Set-AzureRmNetworkSecurityGroup
```

<span data-ttu-id="43104-115">首先，我們會建立兩個新的應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="43104-115">First, we create two new application security groups.</span></span> <span data-ttu-id="43104-116">接著，我們會從資源群組「rg1」檢索名為「nsg1」的 Azure 網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="43104-116">Then, we retrieve an Azure network security group named "nsg1" from resource group "rg1".</span></span> <span data-ttu-id="43104-117">然後將名為 "rdp-rule" 的網路安全性規則新增至它。</span><span class="sxs-lookup"><span data-stu-id="43104-117">and add a network security rule named "rdp-rule" to it.</span></span> <span data-ttu-id="43104-118">此規則允許從應用程式安全性群組 "srcAsg" 中的所有 IP 設定到埠3389上 "destAsg" 的所有 ip 設定的流量。</span><span class="sxs-lookup"><span data-stu-id="43104-118">The rule allows traffic from all the IP configurations in the application security group "srcAsg" to all the IP configurations in "destAsg" on port 3389.</span></span> <span data-ttu-id="43104-119">新增規則之後，我們會保留已修改的 Azure 網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="43104-119">After adding the rule, we persist the modified Azure network security group.</span></span>

## <span data-ttu-id="43104-120">參數</span><span class="sxs-lookup"><span data-stu-id="43104-120">PARAMETERS</span></span>

### <span data-ttu-id="43104-121">-Access</span><span class="sxs-lookup"><span data-stu-id="43104-121">-Access</span></span>
<span data-ttu-id="43104-122">指定是否允許或拒絕網路流量。</span><span class="sxs-lookup"><span data-stu-id="43104-122">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="43104-123">此參數可接受的值為： [允許] 和 [拒絕]。</span><span class="sxs-lookup"><span data-stu-id="43104-123">The acceptable values for this parameter are: Allow and Deny.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43104-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43104-124">-DefaultProfile</span></span>
<span data-ttu-id="43104-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="43104-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43104-126">-描述</span><span class="sxs-lookup"><span data-stu-id="43104-126">-Description</span></span>
<span data-ttu-id="43104-127">指定網路安全規則配置的描述。</span><span class="sxs-lookup"><span data-stu-id="43104-127">Specifies a description of a network security rule configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43104-128">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="43104-128">-DestinationAddressPrefix</span></span>
<span data-ttu-id="43104-129">指定目的地位址首碼。</span><span class="sxs-lookup"><span data-stu-id="43104-129">Specifies a destination address prefix.</span></span>
<span data-ttu-id="43104-130">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="43104-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="43104-131">未類別的域間路由 (CIDR) 位址</span><span class="sxs-lookup"><span data-stu-id="43104-131">A Classless Interdomain Routing (CIDR) address</span></span>
- <span data-ttu-id="43104-132">目的地 IP 位址範圍</span><span class="sxs-lookup"><span data-stu-id="43104-132">A destination IP address range</span></span>
- <span data-ttu-id="43104-133">萬用字元 ( \* ) ，以符合任何 IP 位址</span><span class="sxs-lookup"><span data-stu-id="43104-133">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="43104-134">您可以使用 [VirtualNetwork]、[AzureLoadBalancer] 和 [網際網路] 等標記。</span><span class="sxs-lookup"><span data-stu-id="43104-134">You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43104-135">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="43104-135">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="43104-136">針對規則設定為目的地的應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="43104-136">The application security group set as destination for the rule.</span></span> <span data-ttu-id="43104-137">它不能與 "DestinationAddressPrefix" 參數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="43104-137">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43104-138">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="43104-138">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="43104-139">針對規則設定為目的地的應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="43104-139">The application security group set as destination for the rule.</span></span> <span data-ttu-id="43104-140">它不能與 "DestinationAddressPrefix" 參數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="43104-140">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43104-141">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="43104-141">-DestinationPortRange</span></span>
<span data-ttu-id="43104-142">指定目的地埠或範圍。</span><span class="sxs-lookup"><span data-stu-id="43104-142">Specifies a destination port or range.</span></span>
<span data-ttu-id="43104-143">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="43104-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="43104-144">整數</span><span class="sxs-lookup"><span data-stu-id="43104-144">An integer</span></span>
- <span data-ttu-id="43104-145">0到65535之間的整數範圍</span><span class="sxs-lookup"><span data-stu-id="43104-145">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="43104-146">萬用字元 ( \* ) 與任何埠相符</span><span class="sxs-lookup"><span data-stu-id="43104-146">A wildcard character (\*) to match any port</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43104-147">方向</span><span class="sxs-lookup"><span data-stu-id="43104-147">-Direction</span></span>
<span data-ttu-id="43104-148">指定是否要針對傳入或傳出流量評估規則。</span><span class="sxs-lookup"><span data-stu-id="43104-148">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="43104-149">此參數可接受的值為：入站和出站。</span><span class="sxs-lookup"><span data-stu-id="43104-149">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Inbound, Outbound

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43104-150">-名稱</span><span class="sxs-lookup"><span data-stu-id="43104-150">-Name</span></span>
<span data-ttu-id="43104-151">指定網路安全規則配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="43104-151">Specifies the name of a network security rule configuration.</span></span>

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

### <span data-ttu-id="43104-152">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="43104-152">-NetworkSecurityGroup</span></span>
<span data-ttu-id="43104-153">指定 **NetworkSecurityGroup** 物件。</span><span class="sxs-lookup"><span data-stu-id="43104-153">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="43104-154">這個 Cmdlet 會將網路安全規則設定新增至此參數指定的物件。</span><span class="sxs-lookup"><span data-stu-id="43104-154">This cmdlet adds a network security rule configuration to the object that this parameter specifies.</span></span>

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43104-155">-優先順序</span><span class="sxs-lookup"><span data-stu-id="43104-155">-Priority</span></span>
<span data-ttu-id="43104-156">指定規則配置的優先順序。</span><span class="sxs-lookup"><span data-stu-id="43104-156">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="43104-157">此參數可接受的值為：100和4096之間的整數。</span><span class="sxs-lookup"><span data-stu-id="43104-157">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>

<span data-ttu-id="43104-158">對於集合中的每個規則，優先順序編號必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="43104-158">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="43104-159">優先順序編號越低，規則的優先順序就越高。</span><span class="sxs-lookup"><span data-stu-id="43104-159">The lower the priority number, the higher the priority of the rule.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43104-160">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="43104-160">-Protocol</span></span>
<span data-ttu-id="43104-161">指定規則配置適用的網路通訊協定。</span><span class="sxs-lookup"><span data-stu-id="43104-161">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="43104-162">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="43104-162">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="43104-163">Tcp-out</span><span class="sxs-lookup"><span data-stu-id="43104-163">Tcp</span></span>
- <span data-ttu-id="43104-164">Udp-in</span><span class="sxs-lookup"><span data-stu-id="43104-164">Udp</span></span>
- <span data-ttu-id="43104-165">萬用字元 ( \* ) 與以上兩個相符</span><span class="sxs-lookup"><span data-stu-id="43104-165">Wildcard character (\*) to match both</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp, *

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43104-166">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="43104-166">-SourceAddressPrefix</span></span>
<span data-ttu-id="43104-167">指定來源位址首碼。</span><span class="sxs-lookup"><span data-stu-id="43104-167">Specifies a source address prefix.</span></span>
<span data-ttu-id="43104-168">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="43104-168">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="43104-169">CIDR</span><span class="sxs-lookup"><span data-stu-id="43104-169">A CIDR</span></span>
- <span data-ttu-id="43104-170">來源 IP 範圍</span><span class="sxs-lookup"><span data-stu-id="43104-170">A source IP range</span></span>
- <span data-ttu-id="43104-171">通配字元 ( \* ) ，以符合任何 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="43104-171">A wildcard character (\*) to match any IP address.</span></span>

<span data-ttu-id="43104-172">您也可以使用 [VirtualNetwork]、[AzureLoadBalancer] 和 [網際網路] 等標記。</span><span class="sxs-lookup"><span data-stu-id="43104-172">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43104-173">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="43104-173">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="43104-174">針對規則設定為 [來源] 的應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="43104-174">The application security group set as source for the rule.</span></span> <span data-ttu-id="43104-175">它不能與 "SourceAddressPrefix" 參數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="43104-175">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43104-176">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="43104-176">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="43104-177">針對規則設定為 [來源] 的應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="43104-177">The application security group set as source for the rule.</span></span> <span data-ttu-id="43104-178">它不能與 "SourceAddressPrefix" 參數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="43104-178">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43104-179">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="43104-179">-SourcePortRange</span></span>
<span data-ttu-id="43104-180">指定來源埠或範圍。</span><span class="sxs-lookup"><span data-stu-id="43104-180">Specifies a source port or range.</span></span>
<span data-ttu-id="43104-181">這個值會以整數表示，以0到65535之間的範圍，或以萬用字元字元 ( \* ) 來與任何來源埠相符。</span><span class="sxs-lookup"><span data-stu-id="43104-181">This value is expressed as an integer, as a range between 0 and 65535, or as a wildcard character (\*) to match any source port.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43104-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43104-182">CommonParameters</span></span>
<span data-ttu-id="43104-183">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="43104-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43104-184">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="43104-184">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43104-185">輸入</span><span class="sxs-lookup"><span data-stu-id="43104-185">INPUTS</span></span>

### <span data-ttu-id="43104-186">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="43104-186">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="43104-187">形參 "NetworkSecurityGroup" 接受管線中 "PSNetworkSecurityGroup" 類型的值</span><span class="sxs-lookup"><span data-stu-id="43104-187">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="43104-188">輸出</span><span class="sxs-lookup"><span data-stu-id="43104-188">OUTPUTS</span></span>

### <span data-ttu-id="43104-189">PSNetworkSecurityGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="43104-189">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="43104-190">筆記</span><span class="sxs-lookup"><span data-stu-id="43104-190">NOTES</span></span>

## <span data-ttu-id="43104-191">相關連結</span><span class="sxs-lookup"><span data-stu-id="43104-191">RELATED LINKS</span></span>

[<span data-ttu-id="43104-192">AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="43104-192">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="43104-193">新-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="43104-193">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="43104-194">移除-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="43104-194">Remove-AzureRmNetworkSecurityRuleConfig</span></span>](./Remove-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="43104-195">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="43104-195">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)

