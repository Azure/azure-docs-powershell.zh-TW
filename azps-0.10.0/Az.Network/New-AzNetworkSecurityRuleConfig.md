---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 633FB5C9-BEB3-42A3-AF4F-A54CC3F9E0F7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 17e73f28595a0b99c8209634a6dee6838fa4599d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794257"
---
# <span data-ttu-id="a1376-101">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a1376-101">New-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="a1376-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a1376-102">SYNOPSIS</span></span>
<span data-ttu-id="a1376-103">建立網路安全規則配置。</span><span class="sxs-lookup"><span data-stu-id="a1376-103">Creates a network security rule configuration.</span></span>

## <span data-ttu-id="a1376-104">句法</span><span class="sxs-lookup"><span data-stu-id="a1376-104">SYNTAX</span></span>

### <span data-ttu-id="a1376-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="a1376-105">SetByResource (Default)</span></span>
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DestinationApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a1376-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a1376-106">SetByResourceId</span></span>
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DestinationApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-Access <String>]
 [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1376-107">說明</span><span class="sxs-lookup"><span data-stu-id="a1376-107">DESCRIPTION</span></span>
<span data-ttu-id="a1376-108">**新的-AzNetworkSecurityRuleConfig** Cmdlet 會為網路安全性群組建立 Azure 網路安全規則配置。</span><span class="sxs-lookup"><span data-stu-id="a1376-108">The **New-AzNetworkSecurityRuleConfig** cmdlet creates an Azure network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="a1376-109">示例</span><span class="sxs-lookup"><span data-stu-id="a1376-109">EXAMPLES</span></span>

### <span data-ttu-id="a1376-110">1：建立網路安全規則以允許 RDP</span><span class="sxs-lookup"><span data-stu-id="a1376-110">1: Create a network security rule to allow RDP</span></span>
```
$rule1 = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" 
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix 
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
```

<span data-ttu-id="a1376-111">這個命令會建立一個允許從網際網路存取埠3389的安全性規則</span><span class="sxs-lookup"><span data-stu-id="a1376-111">This command creates a security rule allowing access from the Internet to port 3389</span></span>

### <span data-ttu-id="a1376-112">2：建立允許 HTTP 的網路安全規則</span><span class="sxs-lookup"><span data-stu-id="a1376-112">2: Create a network security rule that allows HTTP</span></span>
```
$rule2 = New-AzNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" 
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix 
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80
```

<span data-ttu-id="a1376-113">這個命令會建立一個允許從網際網路存取埠80的安全性規則</span><span class="sxs-lookup"><span data-stu-id="a1376-113">This command creates a security rule allowing access from the Internet to port 80</span></span>

## <span data-ttu-id="a1376-114">參數</span><span class="sxs-lookup"><span data-stu-id="a1376-114">PARAMETERS</span></span>

### <span data-ttu-id="a1376-115">-Access</span><span class="sxs-lookup"><span data-stu-id="a1376-115">-Access</span></span>
<span data-ttu-id="a1376-116">指定是否允許或拒絕網路流量。</span><span class="sxs-lookup"><span data-stu-id="a1376-116">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="a1376-117">此參數可接受的值為： [允許] 和 [拒絕]。</span><span class="sxs-lookup"><span data-stu-id="a1376-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="a1376-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1376-118">-DefaultProfile</span></span>
<span data-ttu-id="a1376-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a1376-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1376-120">-描述</span><span class="sxs-lookup"><span data-stu-id="a1376-120">-Description</span></span>
<span data-ttu-id="a1376-121">指定要建立的網路安全規則配置的描述。</span><span class="sxs-lookup"><span data-stu-id="a1376-121">Specifies a description of the network security rule configuration to create.</span></span>

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

### <span data-ttu-id="a1376-122">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a1376-122">-DestinationAddressPrefix</span></span>
<span data-ttu-id="a1376-123">指定目的地位址首碼。</span><span class="sxs-lookup"><span data-stu-id="a1376-123">Specifies a destination address prefix.</span></span>
<span data-ttu-id="a1376-124">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a1376-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a1376-125">未類別的域間路由 (CIDR) 位址</span><span class="sxs-lookup"><span data-stu-id="a1376-125">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="a1376-126">目的地 IP 位址範圍</span><span class="sxs-lookup"><span data-stu-id="a1376-126">A destination IP address range</span></span> 
- <span data-ttu-id="a1376-127">萬用字元 ( \* ) ，以符合任何 IP 位址</span><span class="sxs-lookup"><span data-stu-id="a1376-127">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="a1376-128">您可以使用 [VirtualNetwork]、[AzureLoadBalancer] 和 [網際網路] 等標記。</span><span class="sxs-lookup"><span data-stu-id="a1376-128">You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="a1376-129">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a1376-129">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="a1376-130">針對規則設定為目的地的應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="a1376-130">The application security group set as destination for the rule.</span></span> <span data-ttu-id="a1376-131">它不能與 "DestinationAddressPrefix" 參數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="a1376-131">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="a1376-132">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="a1376-132">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="a1376-133">針對規則設定為目的地的應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="a1376-133">The application security group set as destination for the rule.</span></span> <span data-ttu-id="a1376-134">它不能與 "DestinationAddressPrefix" 參數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="a1376-134">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="a1376-135">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="a1376-135">-DestinationPortRange</span></span>
<span data-ttu-id="a1376-136">指定目的地埠或範圍。</span><span class="sxs-lookup"><span data-stu-id="a1376-136">Specifies a destination port or range.</span></span>
<span data-ttu-id="a1376-137">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a1376-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a1376-138">整數</span><span class="sxs-lookup"><span data-stu-id="a1376-138">An integer</span></span>
- <span data-ttu-id="a1376-139">0到65535之間的整數範圍</span><span class="sxs-lookup"><span data-stu-id="a1376-139">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="a1376-140">萬用字元 ( \* ) 與任何埠相符</span><span class="sxs-lookup"><span data-stu-id="a1376-140">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="a1376-141">方向</span><span class="sxs-lookup"><span data-stu-id="a1376-141">-Direction</span></span>
<span data-ttu-id="a1376-142">指定是否要針對傳入或傳出流量評估規則。</span><span class="sxs-lookup"><span data-stu-id="a1376-142">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="a1376-143">此參數可接受的值為：入站和出站。</span><span class="sxs-lookup"><span data-stu-id="a1376-143">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="a1376-144">-名稱</span><span class="sxs-lookup"><span data-stu-id="a1376-144">-Name</span></span>
<span data-ttu-id="a1376-145">指定此 Cmdlet 所建立的網路安全規則配置名稱。</span><span class="sxs-lookup"><span data-stu-id="a1376-145">Specifies the name of the network security rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="a1376-146">-優先順序</span><span class="sxs-lookup"><span data-stu-id="a1376-146">-Priority</span></span>
<span data-ttu-id="a1376-147">指定規則配置的優先順序。</span><span class="sxs-lookup"><span data-stu-id="a1376-147">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="a1376-148">此參數可接受的值為：100和4096之間的整數。</span><span class="sxs-lookup"><span data-stu-id="a1376-148">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>

<span data-ttu-id="a1376-149">對於集合中的每個規則，優先順序編號必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="a1376-149">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="a1376-150">優先順序編號越低，規則的優先順序就越高。</span><span class="sxs-lookup"><span data-stu-id="a1376-150">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="a1376-151">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="a1376-151">-Protocol</span></span>
<span data-ttu-id="a1376-152">指定新規則配置適用的網路通訊協定。</span><span class="sxs-lookup"><span data-stu-id="a1376-152">Specifies the network protocol that a new rule configuration applies to.</span></span>
<span data-ttu-id="a1376-153">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a1376-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a1376-154">Tcp-out</span><span class="sxs-lookup"><span data-stu-id="a1376-154">Tcp</span></span>
- <span data-ttu-id="a1376-155">Udp-in</span><span class="sxs-lookup"><span data-stu-id="a1376-155">Udp</span></span>
- <span data-ttu-id="a1376-156">萬用字元 ( \* ) ，以符合兩個字元。</span><span class="sxs-lookup"><span data-stu-id="a1376-156">wildcard character (\*) to match both.</span></span>

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

### <span data-ttu-id="a1376-157">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a1376-157">-SourceAddressPrefix</span></span>
<span data-ttu-id="a1376-158">指定來源位址首碼。</span><span class="sxs-lookup"><span data-stu-id="a1376-158">Specifies a source address prefix.</span></span>
<span data-ttu-id="a1376-159">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a1376-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a1376-160">CIDR</span><span class="sxs-lookup"><span data-stu-id="a1376-160">A CIDR</span></span>
- <span data-ttu-id="a1376-161">來源 IP 範圍</span><span class="sxs-lookup"><span data-stu-id="a1376-161">A source IP range</span></span>
- <span data-ttu-id="a1376-162">通配字元 ( \* ) ，以符合任何 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="a1376-162">A wildcard character (\*) to match any IP address.</span></span>

<span data-ttu-id="a1376-163">您也可以使用 [VirtualNetwork]、[AzureLoadBalancer] 和 [網際網路] 等標記。</span><span class="sxs-lookup"><span data-stu-id="a1376-163">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="a1376-164">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a1376-164">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="a1376-165">針對規則設定為 [來源] 的應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="a1376-165">The application security group set as source for the rule.</span></span> <span data-ttu-id="a1376-166">它不能與 "SourceAddressPrefix" 參數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="a1376-166">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="a1376-167">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="a1376-167">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="a1376-168">針對規則設定為 [來源] 的應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="a1376-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="a1376-169">它不能與 "SourceAddressPrefix" 參數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="a1376-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="a1376-170">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="a1376-170">-SourcePortRange</span></span>
<span data-ttu-id="a1376-171">指定來源埠或範圍。</span><span class="sxs-lookup"><span data-stu-id="a1376-171">Specifies the source port or range.</span></span>
<span data-ttu-id="a1376-172">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a1376-172">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a1376-173">整數</span><span class="sxs-lookup"><span data-stu-id="a1376-173">An integer</span></span>
- <span data-ttu-id="a1376-174">0到65535之間的整數範圍</span><span class="sxs-lookup"><span data-stu-id="a1376-174">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="a1376-175">萬用字元 ( \* ) 與任何埠相符</span><span class="sxs-lookup"><span data-stu-id="a1376-175">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="a1376-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1376-176">CommonParameters</span></span>
<span data-ttu-id="a1376-177">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a1376-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1376-178">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a1376-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1376-179">輸入</span><span class="sxs-lookup"><span data-stu-id="a1376-179">INPUTS</span></span>

## <span data-ttu-id="a1376-180">輸出</span><span class="sxs-lookup"><span data-stu-id="a1376-180">OUTPUTS</span></span>

### <span data-ttu-id="a1376-181">PSSecurityRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a1376-181">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="a1376-182">筆記</span><span class="sxs-lookup"><span data-stu-id="a1376-182">NOTES</span></span>

## <span data-ttu-id="a1376-183">相關連結</span><span class="sxs-lookup"><span data-stu-id="a1376-183">RELATED LINKS</span></span>

[<span data-ttu-id="a1376-184">附加 AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a1376-184">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="a1376-185">AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a1376-185">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="a1376-186">移除-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a1376-186">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="a1376-187">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a1376-187">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


