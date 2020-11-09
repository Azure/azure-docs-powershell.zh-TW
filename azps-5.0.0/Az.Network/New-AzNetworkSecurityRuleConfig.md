---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 633FB5C9-BEB3-42A3-AF4F-A54CC3F9E0F7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: adef9e3a2ba0d1e67ee8cb2ec9bdd14d9833f5d7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94286583"
---
# <span data-ttu-id="efa0c-101">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="efa0c-101">New-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="efa0c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="efa0c-102">SYNOPSIS</span></span>
<span data-ttu-id="efa0c-103">建立網路安全規則配置。</span><span class="sxs-lookup"><span data-stu-id="efa0c-103">Creates a network security rule configuration.</span></span>

## <span data-ttu-id="efa0c-104">句法</span><span class="sxs-lookup"><span data-stu-id="efa0c-104">SYNTAX</span></span>

### <span data-ttu-id="efa0c-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="efa0c-105">SetByResource (Default)</span></span>
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>] [-SourceAddressPrefix <String[]>]
 [-DestinationAddressPrefix <String[]>] [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="efa0c-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="efa0c-106">SetByResourceId</span></span>
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>] [-SourceAddressPrefix <String[]>]
 [-DestinationAddressPrefix <String[]>] [-SourceApplicationSecurityGroupId <String[]>]
 [-DestinationApplicationSecurityGroupId <String[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="efa0c-107">說明</span><span class="sxs-lookup"><span data-stu-id="efa0c-107">DESCRIPTION</span></span>
<span data-ttu-id="efa0c-108">**新的-AzNetworkSecurityRuleConfig** Cmdlet 會為網路安全性群組建立 Azure 網路安全規則配置。</span><span class="sxs-lookup"><span data-stu-id="efa0c-108">The **New-AzNetworkSecurityRuleConfig** cmdlet creates an Azure network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="efa0c-109">示例</span><span class="sxs-lookup"><span data-stu-id="efa0c-109">EXAMPLES</span></span>

### <span data-ttu-id="efa0c-110">範例1：建立網路安全規則以允許 RDP</span><span class="sxs-lookup"><span data-stu-id="efa0c-110">Example 1: Create a network security rule to allow RDP</span></span>
```powershell
$rule1 = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
```

<span data-ttu-id="efa0c-111">這個命令會建立一個允許從網際網路存取埠3389的安全性規則</span><span class="sxs-lookup"><span data-stu-id="efa0c-111">This command creates a security rule allowing access from the Internet to port 3389</span></span>

### <span data-ttu-id="efa0c-112">範例2：建立允許 HTTP 的網路安全規則</span><span class="sxs-lookup"><span data-stu-id="efa0c-112">Example 2: Create a network security rule that allows HTTP</span></span>
```powershell
$rule2 = New-AzNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80
```

<span data-ttu-id="efa0c-113">這個命令會建立一個允許從網際網路存取埠80的安全性規則</span><span class="sxs-lookup"><span data-stu-id="efa0c-113">This command creates a security rule allowing access from the Internet to port 80</span></span>

## <span data-ttu-id="efa0c-114">參數</span><span class="sxs-lookup"><span data-stu-id="efa0c-114">PARAMETERS</span></span>

### <span data-ttu-id="efa0c-115">-Access</span><span class="sxs-lookup"><span data-stu-id="efa0c-115">-Access</span></span>
<span data-ttu-id="efa0c-116">指定是否允許或拒絕網路流量。</span><span class="sxs-lookup"><span data-stu-id="efa0c-116">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="efa0c-117">此參數可接受的值為： [允許] 和 [拒絕]。</span><span class="sxs-lookup"><span data-stu-id="efa0c-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="efa0c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efa0c-118">-DefaultProfile</span></span>
<span data-ttu-id="efa0c-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="efa0c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="efa0c-120">-描述</span><span class="sxs-lookup"><span data-stu-id="efa0c-120">-Description</span></span>
<span data-ttu-id="efa0c-121">指定要建立的網路安全規則配置的描述。</span><span class="sxs-lookup"><span data-stu-id="efa0c-121">Specifies a description of the network security rule configuration to create.</span></span>

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

### <span data-ttu-id="efa0c-122">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="efa0c-122">-DestinationAddressPrefix</span></span>
<span data-ttu-id="efa0c-123">指定目的地位址首碼。</span><span class="sxs-lookup"><span data-stu-id="efa0c-123">Specifies a destination address prefix.</span></span>
<span data-ttu-id="efa0c-124">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="efa0c-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="efa0c-125">未類別的域間路由 (CIDR) 位址</span><span class="sxs-lookup"><span data-stu-id="efa0c-125">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="efa0c-126">目的地 IP 位址範圍</span><span class="sxs-lookup"><span data-stu-id="efa0c-126">A destination IP address range</span></span> 
- <span data-ttu-id="efa0c-127">萬用字元 ( \* ) 若要與任何 IP 位址相符，您可以使用 VirtualNetwork、AzureLoadBalancer 和 Internet 等標記。</span><span class="sxs-lookup"><span data-stu-id="efa0c-127">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="efa0c-128">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="efa0c-128">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="efa0c-129">針對規則設定為目的地的應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="efa0c-129">The application security group set as destination for the rule.</span></span> <span data-ttu-id="efa0c-130">它不能與 "DestinationAddressPrefix" 參數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="efa0c-130">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="efa0c-131">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="efa0c-131">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="efa0c-132">針對規則設定為目的地的應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="efa0c-132">The application security group set as destination for the rule.</span></span> <span data-ttu-id="efa0c-133">它不能與 "DestinationAddressPrefix" 參數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="efa0c-133">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="efa0c-134">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="efa0c-134">-DestinationPortRange</span></span>
<span data-ttu-id="efa0c-135">指定目的地埠或範圍。</span><span class="sxs-lookup"><span data-stu-id="efa0c-135">Specifies a destination port or range.</span></span>
<span data-ttu-id="efa0c-136">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="efa0c-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="efa0c-137">整數</span><span class="sxs-lookup"><span data-stu-id="efa0c-137">An integer</span></span>
- <span data-ttu-id="efa0c-138">0到65535之間的整數範圍</span><span class="sxs-lookup"><span data-stu-id="efa0c-138">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="efa0c-139">萬用字元 ( \* ) 與任何埠相符</span><span class="sxs-lookup"><span data-stu-id="efa0c-139">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="efa0c-140">方向</span><span class="sxs-lookup"><span data-stu-id="efa0c-140">-Direction</span></span>
<span data-ttu-id="efa0c-141">指定是否要針對傳入或傳出流量評估規則。</span><span class="sxs-lookup"><span data-stu-id="efa0c-141">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="efa0c-142">此參數可接受的值為：入站和出站。</span><span class="sxs-lookup"><span data-stu-id="efa0c-142">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="efa0c-143">-名稱</span><span class="sxs-lookup"><span data-stu-id="efa0c-143">-Name</span></span>
<span data-ttu-id="efa0c-144">指定此 Cmdlet 所建立的網路安全規則配置名稱。</span><span class="sxs-lookup"><span data-stu-id="efa0c-144">Specifies the name of the network security rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="efa0c-145">-優先順序</span><span class="sxs-lookup"><span data-stu-id="efa0c-145">-Priority</span></span>
<span data-ttu-id="efa0c-146">指定規則配置的優先順序。</span><span class="sxs-lookup"><span data-stu-id="efa0c-146">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="efa0c-147">此參數可接受的值為：100和4096之間的整數。</span><span class="sxs-lookup"><span data-stu-id="efa0c-147">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>
<span data-ttu-id="efa0c-148">對於集合中的每個規則，優先順序編號必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="efa0c-148">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="efa0c-149">優先順序編號越低，規則的優先順序就越高。</span><span class="sxs-lookup"><span data-stu-id="efa0c-149">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="efa0c-150">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="efa0c-150">-Protocol</span></span>
<span data-ttu-id="efa0c-151">指定新規則配置適用的網路通訊協定。</span><span class="sxs-lookup"><span data-stu-id="efa0c-151">Specifies the network protocol that a new rule configuration applies to.</span></span>
<span data-ttu-id="efa0c-152">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="efa0c-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="efa0c-153">Tcp-out</span><span class="sxs-lookup"><span data-stu-id="efa0c-153">Tcp</span></span>
- <span data-ttu-id="efa0c-154">Udp-in</span><span class="sxs-lookup"><span data-stu-id="efa0c-154">Udp</span></span>
- <span data-ttu-id="efa0c-155">萬用字元 ( \* ) ，以符合兩個字元。</span><span class="sxs-lookup"><span data-stu-id="efa0c-155">wildcard character (\*) to match both.</span></span>

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

### <span data-ttu-id="efa0c-156">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="efa0c-156">-SourceAddressPrefix</span></span>
<span data-ttu-id="efa0c-157">指定來源位址首碼。</span><span class="sxs-lookup"><span data-stu-id="efa0c-157">Specifies a source address prefix.</span></span>
<span data-ttu-id="efa0c-158">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="efa0c-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="efa0c-159">CIDR</span><span class="sxs-lookup"><span data-stu-id="efa0c-159">A CIDR</span></span>
- <span data-ttu-id="efa0c-160">來源 IP 範圍</span><span class="sxs-lookup"><span data-stu-id="efa0c-160">A source IP range</span></span>
- <span data-ttu-id="efa0c-161">通配字元 ( \* ) ，以符合任何 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="efa0c-161">A wildcard character (\*) to match any IP address.</span></span>
<span data-ttu-id="efa0c-162">您也可以使用 [VirtualNetwork]、[AzureLoadBalancer] 和 [網際網路] 等標記。</span><span class="sxs-lookup"><span data-stu-id="efa0c-162">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="efa0c-163">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="efa0c-163">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="efa0c-164">針對規則設定為 [來源] 的應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="efa0c-164">The application security group set as source for the rule.</span></span> <span data-ttu-id="efa0c-165">它不能與 "SourceAddressPrefix" 參數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="efa0c-165">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="efa0c-166">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="efa0c-166">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="efa0c-167">針對規則設定為 [來源] 的應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="efa0c-167">The application security group set as source for the rule.</span></span> <span data-ttu-id="efa0c-168">它不能與 "SourceAddressPrefix" 參數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="efa0c-168">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="efa0c-169">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="efa0c-169">-SourcePortRange</span></span>
<span data-ttu-id="efa0c-170">指定來源埠或範圍。</span><span class="sxs-lookup"><span data-stu-id="efa0c-170">Specifies the source port or range.</span></span>
<span data-ttu-id="efa0c-171">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="efa0c-171">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="efa0c-172">整數</span><span class="sxs-lookup"><span data-stu-id="efa0c-172">An integer</span></span>
- <span data-ttu-id="efa0c-173">0到65535之間的整數範圍</span><span class="sxs-lookup"><span data-stu-id="efa0c-173">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="efa0c-174">萬用字元 ( \* ) 與任何埠相符</span><span class="sxs-lookup"><span data-stu-id="efa0c-174">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="efa0c-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efa0c-175">CommonParameters</span></span>
<span data-ttu-id="efa0c-176">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="efa0c-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efa0c-177">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="efa0c-177">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efa0c-178">輸入</span><span class="sxs-lookup"><span data-stu-id="efa0c-178">INPUTS</span></span>

### <span data-ttu-id="efa0c-179">所有</span><span class="sxs-lookup"><span data-stu-id="efa0c-179">None</span></span>

## <span data-ttu-id="efa0c-180">輸出</span><span class="sxs-lookup"><span data-stu-id="efa0c-180">OUTPUTS</span></span>

### <span data-ttu-id="efa0c-181">PSSecurityRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="efa0c-181">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="efa0c-182">筆記</span><span class="sxs-lookup"><span data-stu-id="efa0c-182">NOTES</span></span>

## <span data-ttu-id="efa0c-183">相關連結</span><span class="sxs-lookup"><span data-stu-id="efa0c-183">RELATED LINKS</span></span>

[<span data-ttu-id="efa0c-184">附加 AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="efa0c-184">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="efa0c-185">AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="efa0c-185">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="efa0c-186">移除-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="efa0c-186">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="efa0c-187">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="efa0c-187">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


