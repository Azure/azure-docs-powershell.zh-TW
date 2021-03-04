---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 633FB5C9-BEB3-42A3-AF4F-A54CC3F9E0F7
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 45702774e44e4b3da0b90d37e86e478c52dcba17
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902402"
---
# <span data-ttu-id="a187b-101">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a187b-101">New-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="a187b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a187b-102">SYNOPSIS</span></span>
<span data-ttu-id="a187b-103">建立網路安全性規則組。</span><span class="sxs-lookup"><span data-stu-id="a187b-103">Creates a network security rule configuration.</span></span>

## <span data-ttu-id="a187b-104">語法</span><span class="sxs-lookup"><span data-stu-id="a187b-104">SYNTAX</span></span>

### <span data-ttu-id="a187b-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="a187b-105">SetByResource (Default)</span></span>
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>] [-SourceAddressPrefix <String[]>]
 [-DestinationAddressPrefix <String[]>] [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a187b-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a187b-106">SetByResourceId</span></span>
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>] [-SourceAddressPrefix <String[]>]
 [-DestinationAddressPrefix <String[]>] [-SourceApplicationSecurityGroupId <String[]>]
 [-DestinationApplicationSecurityGroupId <String[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a187b-107">描述</span><span class="sxs-lookup"><span data-stu-id="a187b-107">DESCRIPTION</span></span>
<span data-ttu-id="a187b-108">**New-AzNetworkSecurityRuleConfig** Cmdlet 會為網路安全性群組建立 Azure 網路安全性規則組。</span><span class="sxs-lookup"><span data-stu-id="a187b-108">The **New-AzNetworkSecurityRuleConfig** cmdlet creates an Azure network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="a187b-109">例子</span><span class="sxs-lookup"><span data-stu-id="a187b-109">EXAMPLES</span></span>

### <span data-ttu-id="a187b-110">範例 1：建立網路安全性規則以允許 RDP</span><span class="sxs-lookup"><span data-stu-id="a187b-110">Example 1: Create a network security rule to allow RDP</span></span>
```powershell
$rule1 = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
```

<span data-ttu-id="a187b-111">此命令會建立安全性規則，允許從網際網路存取埠 3389</span><span class="sxs-lookup"><span data-stu-id="a187b-111">This command creates a security rule allowing access from the Internet to port 3389</span></span>

### <span data-ttu-id="a187b-112">範例 2：建立允許 HTTP 的網路安全性規則</span><span class="sxs-lookup"><span data-stu-id="a187b-112">Example 2: Create a network security rule that allows HTTP</span></span>
```powershell
$rule2 = New-AzNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80
```

<span data-ttu-id="a187b-113">此命令會建立安全性規則，允許從網際網路存取埠 80</span><span class="sxs-lookup"><span data-stu-id="a187b-113">This command creates a security rule allowing access from the Internet to port 80</span></span>

## <span data-ttu-id="a187b-114">參數</span><span class="sxs-lookup"><span data-stu-id="a187b-114">PARAMETERS</span></span>

### <span data-ttu-id="a187b-115">-Access</span><span class="sxs-lookup"><span data-stu-id="a187b-115">-Access</span></span>
<span data-ttu-id="a187b-116">指定是否允許或拒絕網路流量。</span><span class="sxs-lookup"><span data-stu-id="a187b-116">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="a187b-117">此參數可接受的值為：允許和拒絕。</span><span class="sxs-lookup"><span data-stu-id="a187b-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="a187b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a187b-118">-DefaultProfile</span></span>
<span data-ttu-id="a187b-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a187b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a187b-120">-描述</span><span class="sxs-lookup"><span data-stu-id="a187b-120">-Description</span></span>
<span data-ttu-id="a187b-121">指定要建立之網路安全性規則組配置的描述。</span><span class="sxs-lookup"><span data-stu-id="a187b-121">Specifies a description of the network security rule configuration to create.</span></span>

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

### <span data-ttu-id="a187b-122">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a187b-122">-DestinationAddressPrefix</span></span>
<span data-ttu-id="a187b-123">指定目的地位址首碼。</span><span class="sxs-lookup"><span data-stu-id="a187b-123">Specifies a destination address prefix.</span></span>
<span data-ttu-id="a187b-124">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a187b-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a187b-125">CIDR 位址的無 (域) 路由</span><span class="sxs-lookup"><span data-stu-id="a187b-125">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="a187b-126">目的地 IP 位址範圍</span><span class="sxs-lookup"><span data-stu-id="a187b-126">A destination IP address range</span></span> 
- <span data-ttu-id="a187b-127">萬用字元 (\*) 比對任何 IP 位址。您可以使用 VirtualNetwork、AzureLoadBalancer 和 Internet 等標記。</span><span class="sxs-lookup"><span data-stu-id="a187b-127">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="a187b-128">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a187b-128">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="a187b-129">應用程式安全性群組設定為規則的目的地。</span><span class="sxs-lookup"><span data-stu-id="a187b-129">The application security group set as destination for the rule.</span></span> <span data-ttu-id="a187b-130">它無法與 "DestinationAddressPrefix" 參數一起使用。</span><span class="sxs-lookup"><span data-stu-id="a187b-130">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="a187b-131">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="a187b-131">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="a187b-132">應用程式安全性群組設定為規則的目的地。</span><span class="sxs-lookup"><span data-stu-id="a187b-132">The application security group set as destination for the rule.</span></span> <span data-ttu-id="a187b-133">它無法與 "DestinationAddressPrefix" 參數一起使用。</span><span class="sxs-lookup"><span data-stu-id="a187b-133">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="a187b-134">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="a187b-134">-DestinationPortRange</span></span>
<span data-ttu-id="a187b-135">指定目的地埠或範圍。</span><span class="sxs-lookup"><span data-stu-id="a187b-135">Specifies a destination port or range.</span></span>
<span data-ttu-id="a187b-136">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a187b-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a187b-137">整數</span><span class="sxs-lookup"><span data-stu-id="a187b-137">An integer</span></span>
- <span data-ttu-id="a187b-138">介於 0 到 65535 之間的整數範圍</span><span class="sxs-lookup"><span data-stu-id="a187b-138">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="a187b-139">\* (\*) 字元來比對任何埠</span><span class="sxs-lookup"><span data-stu-id="a187b-139">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="a187b-140">-方向</span><span class="sxs-lookup"><span data-stu-id="a187b-140">-Direction</span></span>
<span data-ttu-id="a187b-141">指定規則是評估內流量還是外發流量。</span><span class="sxs-lookup"><span data-stu-id="a187b-141">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="a187b-142">此參數可接受的值為：輸入和外發。</span><span class="sxs-lookup"><span data-stu-id="a187b-142">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="a187b-143">-名稱</span><span class="sxs-lookup"><span data-stu-id="a187b-143">-Name</span></span>
<span data-ttu-id="a187b-144">指定此 Cmdlet 所建立之網路安全性規則組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a187b-144">Specifies the name of the network security rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="a187b-145">-優先順序</span><span class="sxs-lookup"><span data-stu-id="a187b-145">-Priority</span></span>
<span data-ttu-id="a187b-146">指定規則配置的優先順序。</span><span class="sxs-lookup"><span data-stu-id="a187b-146">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="a187b-147">此參數可接受的值為：介於 100 和 4096 之間的整數。</span><span class="sxs-lookup"><span data-stu-id="a187b-147">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>
<span data-ttu-id="a187b-148">優先順序數位必須是唯一的，因為集合中每個規則都是唯一的。</span><span class="sxs-lookup"><span data-stu-id="a187b-148">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="a187b-149">優先順序數位越低，規則的優先順序越高。</span><span class="sxs-lookup"><span data-stu-id="a187b-149">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="a187b-150">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="a187b-150">-Protocol</span></span>
<span data-ttu-id="a187b-151">指定新規則組配置的適用網路通訊協定。</span><span class="sxs-lookup"><span data-stu-id="a187b-151">Specifies the network protocol that a new rule configuration applies to.</span></span>
<span data-ttu-id="a187b-152">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a187b-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a187b-153">Tcp</span><span class="sxs-lookup"><span data-stu-id="a187b-153">Tcp</span></span>
- <span data-ttu-id="a187b-154">Udp</span><span class="sxs-lookup"><span data-stu-id="a187b-154">Udp</span></span>
- <span data-ttu-id="a187b-155">萬用字元 (\*) 兩者相符。</span><span class="sxs-lookup"><span data-stu-id="a187b-155">wildcard character (\*) to match both.</span></span>

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

### <span data-ttu-id="a187b-156">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a187b-156">-SourceAddressPrefix</span></span>
<span data-ttu-id="a187b-157">指定來源位址首碼。</span><span class="sxs-lookup"><span data-stu-id="a187b-157">Specifies a source address prefix.</span></span>
<span data-ttu-id="a187b-158">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a187b-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a187b-159">A CIDR</span><span class="sxs-lookup"><span data-stu-id="a187b-159">A CIDR</span></span>
- <span data-ttu-id="a187b-160">來源 IP 範圍</span><span class="sxs-lookup"><span data-stu-id="a187b-160">A source IP range</span></span>
- <span data-ttu-id="a187b-161">\* (\*) 字元，以比對任何 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="a187b-161">A wildcard character (\*) to match any IP address.</span></span>
<span data-ttu-id="a187b-162">您也可以使用虛擬網路、AzureLoadBalancer 和網際網路等標記。</span><span class="sxs-lookup"><span data-stu-id="a187b-162">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="a187b-163">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a187b-163">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="a187b-164">應用程式安全性群組設定為規則的來源。</span><span class="sxs-lookup"><span data-stu-id="a187b-164">The application security group set as source for the rule.</span></span> <span data-ttu-id="a187b-165">它無法與 'SourceAddressPrefix' 參數一起使用。</span><span class="sxs-lookup"><span data-stu-id="a187b-165">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="a187b-166">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="a187b-166">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="a187b-167">應用程式安全性群組設定為規則的來源。</span><span class="sxs-lookup"><span data-stu-id="a187b-167">The application security group set as source for the rule.</span></span> <span data-ttu-id="a187b-168">它無法與 'SourceAddressPrefix' 參數一起使用。</span><span class="sxs-lookup"><span data-stu-id="a187b-168">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="a187b-169">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="a187b-169">-SourcePortRange</span></span>
<span data-ttu-id="a187b-170">指定來源埠或範圍。</span><span class="sxs-lookup"><span data-stu-id="a187b-170">Specifies the source port or range.</span></span>
<span data-ttu-id="a187b-171">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a187b-171">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a187b-172">整數</span><span class="sxs-lookup"><span data-stu-id="a187b-172">An integer</span></span>
- <span data-ttu-id="a187b-173">介於 0 到 65535 之間的整數範圍</span><span class="sxs-lookup"><span data-stu-id="a187b-173">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="a187b-174">\* (\*) 字元來比對任何埠</span><span class="sxs-lookup"><span data-stu-id="a187b-174">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="a187b-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a187b-175">CommonParameters</span></span>
<span data-ttu-id="a187b-176">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a187b-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a187b-177">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a187b-177">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a187b-178">輸入</span><span class="sxs-lookup"><span data-stu-id="a187b-178">INPUTS</span></span>

### <span data-ttu-id="a187b-179">沒有</span><span class="sxs-lookup"><span data-stu-id="a187b-179">None</span></span>

## <span data-ttu-id="a187b-180">輸出</span><span class="sxs-lookup"><span data-stu-id="a187b-180">OUTPUTS</span></span>

### <span data-ttu-id="a187b-181">Microsoft.Azure.Commands.Network.models.PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="a187b-181">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="a187b-182">筆記</span><span class="sxs-lookup"><span data-stu-id="a187b-182">NOTES</span></span>

## <span data-ttu-id="a187b-183">相關連結</span><span class="sxs-lookup"><span data-stu-id="a187b-183">RELATED LINKS</span></span>

[<span data-ttu-id="a187b-184">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a187b-184">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="a187b-185">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a187b-185">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="a187b-186">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a187b-186">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="a187b-187">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a187b-187">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


