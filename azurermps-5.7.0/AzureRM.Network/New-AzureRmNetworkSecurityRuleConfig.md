---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 633FB5C9-BEB3-42A3-AF4F-A54CC3F9E0F7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkSecurityRuleConfig.md
ms.openlocfilehash: 14af257cf6c5d5e547f81b76fd82a910580b3790
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449847"
---
# <span data-ttu-id="fe2d1-101">New-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fe2d1-101">New-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="fe2d1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fe2d1-102">SYNOPSIS</span></span>
<span data-ttu-id="fe2d1-103">建立網路安全規則配置。</span><span class="sxs-lookup"><span data-stu-id="fe2d1-103">Creates a network security rule configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe2d1-104">句法</span><span class="sxs-lookup"><span data-stu-id="fe2d1-104">SYNTAX</span></span>

### <span data-ttu-id="fe2d1-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="fe2d1-105">SetByResource (Default)</span></span>
```
New-AzureRmNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DestinationApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fe2d1-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="fe2d1-106">SetByResourceId</span></span>
```
New-AzureRmNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DestinationApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-Access <String>]
 [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe2d1-107">說明</span><span class="sxs-lookup"><span data-stu-id="fe2d1-107">DESCRIPTION</span></span>
<span data-ttu-id="fe2d1-108">**新的-AzureRmNetworkSecurityRuleConfig** Cmdlet 會為網路安全性群組建立 Azure 網路安全規則配置。</span><span class="sxs-lookup"><span data-stu-id="fe2d1-108">The **New-AzureRmNetworkSecurityRuleConfig** cmdlet creates an Azure network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="fe2d1-109">示例</span><span class="sxs-lookup"><span data-stu-id="fe2d1-109">EXAMPLES</span></span>

### <span data-ttu-id="fe2d1-110">1：建立網路安全規則以允許 RDP</span><span class="sxs-lookup"><span data-stu-id="fe2d1-110">1: Create a network security rule to allow RDP</span></span>
```
$rule1 = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" 
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix 
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
```

<span data-ttu-id="fe2d1-111">這個命令會建立一個允許從網際網路存取埠3389的安全性規則</span><span class="sxs-lookup"><span data-stu-id="fe2d1-111">This command creates a security rule allowing access from the Internet to port 3389</span></span>

### <span data-ttu-id="fe2d1-112">2：建立允許 HTTP 的網路安全規則</span><span class="sxs-lookup"><span data-stu-id="fe2d1-112">2: Create a network security rule that allows HTTP</span></span>
```
$rule2 = New-AzureRmNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" 
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix 
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80
```

<span data-ttu-id="fe2d1-113">這個命令會建立一個允許從網際網路存取埠80的安全性規則</span><span class="sxs-lookup"><span data-stu-id="fe2d1-113">This command creates a security rule allowing access from the Internet to port 80</span></span>

## <span data-ttu-id="fe2d1-114">參數</span><span class="sxs-lookup"><span data-stu-id="fe2d1-114">PARAMETERS</span></span>

### <span data-ttu-id="fe2d1-115">-Access</span><span class="sxs-lookup"><span data-stu-id="fe2d1-115">-Access</span></span>
<span data-ttu-id="fe2d1-116">指定是否允許或拒絕網路流量。</span><span class="sxs-lookup"><span data-stu-id="fe2d1-116">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="fe2d1-117">此參數可接受的值為： [允許] 和 [拒絕]。</span><span class="sxs-lookup"><span data-stu-id="fe2d1-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="fe2d1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe2d1-118">-DefaultProfile</span></span>
<span data-ttu-id="fe2d1-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fe2d1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe2d1-120">-描述</span><span class="sxs-lookup"><span data-stu-id="fe2d1-120">-Description</span></span>
<span data-ttu-id="fe2d1-121">指定要建立的網路安全規則配置的描述。</span><span class="sxs-lookup"><span data-stu-id="fe2d1-121">Specifies a description of the network security rule configuration to create.</span></span>

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

### <span data-ttu-id="fe2d1-122">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="fe2d1-122">-DestinationAddressPrefix</span></span>
<span data-ttu-id="fe2d1-123">指定目的地位址首碼。</span><span class="sxs-lookup"><span data-stu-id="fe2d1-123">Specifies a destination address prefix.</span></span>
<span data-ttu-id="fe2d1-124">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="fe2d1-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fe2d1-125">未類別的域間路由 (CIDR) 位址</span><span class="sxs-lookup"><span data-stu-id="fe2d1-125">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="fe2d1-126">目的地 IP 位址範圍</span><span class="sxs-lookup"><span data-stu-id="fe2d1-126">A destination IP address range</span></span> 
- <span data-ttu-id="fe2d1-127">萬用字元 ( \* ) ，以符合任何 IP 位址</span><span class="sxs-lookup"><span data-stu-id="fe2d1-127">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="fe2d1-128">您可以使用 [VirtualNetwork]、[AzureLoadBalancer] 和 [網際網路] 等標記。</span><span class="sxs-lookup"><span data-stu-id="fe2d1-128">You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="fe2d1-129">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fe2d1-129">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="fe2d1-130">針對規則設定為目的地的應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="fe2d1-130">The application security group set as destination for the rule.</span></span> <span data-ttu-id="fe2d1-131">它不能與 "DestinationAddressPrefix" 參數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="fe2d1-131">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="fe2d1-132">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="fe2d1-132">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="fe2d1-133">針對規則設定為目的地的應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="fe2d1-133">The application security group set as destination for the rule.</span></span> <span data-ttu-id="fe2d1-134">它不能與 "DestinationAddressPrefix" 參數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="fe2d1-134">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="fe2d1-135">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="fe2d1-135">-DestinationPortRange</span></span>
<span data-ttu-id="fe2d1-136">指定目的地埠或範圍。</span><span class="sxs-lookup"><span data-stu-id="fe2d1-136">Specifies a destination port or range.</span></span>
<span data-ttu-id="fe2d1-137">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="fe2d1-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fe2d1-138">整數</span><span class="sxs-lookup"><span data-stu-id="fe2d1-138">An integer</span></span>
- <span data-ttu-id="fe2d1-139">0到65535之間的整數範圍</span><span class="sxs-lookup"><span data-stu-id="fe2d1-139">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="fe2d1-140">萬用字元 ( \* ) 與任何埠相符</span><span class="sxs-lookup"><span data-stu-id="fe2d1-140">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="fe2d1-141">方向</span><span class="sxs-lookup"><span data-stu-id="fe2d1-141">-Direction</span></span>
<span data-ttu-id="fe2d1-142">指定是否要針對傳入或傳出流量評估規則。</span><span class="sxs-lookup"><span data-stu-id="fe2d1-142">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="fe2d1-143">此參數可接受的值為：入站和出站。</span><span class="sxs-lookup"><span data-stu-id="fe2d1-143">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="fe2d1-144">-名稱</span><span class="sxs-lookup"><span data-stu-id="fe2d1-144">-Name</span></span>
<span data-ttu-id="fe2d1-145">指定此 Cmdlet 所建立的網路安全規則配置名稱。</span><span class="sxs-lookup"><span data-stu-id="fe2d1-145">Specifies the name of the network security rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="fe2d1-146">-優先順序</span><span class="sxs-lookup"><span data-stu-id="fe2d1-146">-Priority</span></span>
<span data-ttu-id="fe2d1-147">指定規則配置的優先順序。</span><span class="sxs-lookup"><span data-stu-id="fe2d1-147">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="fe2d1-148">此參數可接受的值為：100和4096之間的整數。</span><span class="sxs-lookup"><span data-stu-id="fe2d1-148">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>

<span data-ttu-id="fe2d1-149">對於集合中的每個規則，優先順序編號必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="fe2d1-149">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="fe2d1-150">優先順序編號越低，規則的優先順序就越高。</span><span class="sxs-lookup"><span data-stu-id="fe2d1-150">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="fe2d1-151">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="fe2d1-151">-Protocol</span></span>
<span data-ttu-id="fe2d1-152">指定新規則配置適用的網路通訊協定。</span><span class="sxs-lookup"><span data-stu-id="fe2d1-152">Specifies the network protocol that a new rule configuration applies to.</span></span>
<span data-ttu-id="fe2d1-153">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="fe2d1-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fe2d1-154">Tcp-out</span><span class="sxs-lookup"><span data-stu-id="fe2d1-154">Tcp</span></span>
- <span data-ttu-id="fe2d1-155">Udp-in</span><span class="sxs-lookup"><span data-stu-id="fe2d1-155">Udp</span></span>
- <span data-ttu-id="fe2d1-156">萬用字元 ( \* ) ，以符合兩個字元。</span><span class="sxs-lookup"><span data-stu-id="fe2d1-156">wildcard character (\*) to match both.</span></span>

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

### <span data-ttu-id="fe2d1-157">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="fe2d1-157">-SourceAddressPrefix</span></span>
<span data-ttu-id="fe2d1-158">指定來源位址首碼。</span><span class="sxs-lookup"><span data-stu-id="fe2d1-158">Specifies a source address prefix.</span></span>
<span data-ttu-id="fe2d1-159">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="fe2d1-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fe2d1-160">CIDR</span><span class="sxs-lookup"><span data-stu-id="fe2d1-160">A CIDR</span></span>
- <span data-ttu-id="fe2d1-161">來源 IP 範圍</span><span class="sxs-lookup"><span data-stu-id="fe2d1-161">A source IP range</span></span>
- <span data-ttu-id="fe2d1-162">通配字元 ( \* ) ，以符合任何 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="fe2d1-162">A wildcard character (\*) to match any IP address.</span></span>

<span data-ttu-id="fe2d1-163">您也可以使用 [VirtualNetwork]、[AzureLoadBalancer] 和 [網際網路] 等標記。</span><span class="sxs-lookup"><span data-stu-id="fe2d1-163">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="fe2d1-164">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fe2d1-164">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="fe2d1-165">針對規則設定為 [來源] 的應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="fe2d1-165">The application security group set as source for the rule.</span></span> <span data-ttu-id="fe2d1-166">它不能與 "SourceAddressPrefix" 參數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="fe2d1-166">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="fe2d1-167">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="fe2d1-167">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="fe2d1-168">針對規則設定為 [來源] 的應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="fe2d1-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="fe2d1-169">它不能與 "SourceAddressPrefix" 參數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="fe2d1-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="fe2d1-170">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="fe2d1-170">-SourcePortRange</span></span>
<span data-ttu-id="fe2d1-171">指定來源埠或範圍。</span><span class="sxs-lookup"><span data-stu-id="fe2d1-171">Specifies the source port or range.</span></span>
<span data-ttu-id="fe2d1-172">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="fe2d1-172">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fe2d1-173">整數</span><span class="sxs-lookup"><span data-stu-id="fe2d1-173">An integer</span></span>
- <span data-ttu-id="fe2d1-174">0到65535之間的整數範圍</span><span class="sxs-lookup"><span data-stu-id="fe2d1-174">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="fe2d1-175">萬用字元 ( \* ) 與任何埠相符</span><span class="sxs-lookup"><span data-stu-id="fe2d1-175">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="fe2d1-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe2d1-176">CommonParameters</span></span>
<span data-ttu-id="fe2d1-177">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fe2d1-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe2d1-178">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fe2d1-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe2d1-179">輸入</span><span class="sxs-lookup"><span data-stu-id="fe2d1-179">INPUTS</span></span>

### <span data-ttu-id="fe2d1-180">所有</span><span class="sxs-lookup"><span data-stu-id="fe2d1-180">None</span></span>
<span data-ttu-id="fe2d1-181">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="fe2d1-181">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fe2d1-182">輸出</span><span class="sxs-lookup"><span data-stu-id="fe2d1-182">OUTPUTS</span></span>

### <span data-ttu-id="fe2d1-183">PSSecurityRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="fe2d1-183">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="fe2d1-184">筆記</span><span class="sxs-lookup"><span data-stu-id="fe2d1-184">NOTES</span></span>

## <span data-ttu-id="fe2d1-185">相關連結</span><span class="sxs-lookup"><span data-stu-id="fe2d1-185">RELATED LINKS</span></span>

[<span data-ttu-id="fe2d1-186">附加 AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fe2d1-186">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="fe2d1-187">AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fe2d1-187">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="fe2d1-188">移除-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fe2d1-188">Remove-AzureRmNetworkSecurityRuleConfig</span></span>](./Remove-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="fe2d1-189">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fe2d1-189">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)


