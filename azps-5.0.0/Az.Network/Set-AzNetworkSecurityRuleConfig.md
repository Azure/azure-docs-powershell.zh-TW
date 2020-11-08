---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 42f92e7f90e5349c116f8a6ed948ed7a29a35ad2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138182"
---
# <span data-ttu-id="3960d-101">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3960d-101">Set-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="3960d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3960d-102">SYNOPSIS</span></span>
<span data-ttu-id="3960d-103">更新網路安全性群組的網路安全規則配置。</span><span class="sxs-lookup"><span data-stu-id="3960d-103">Updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="3960d-104">句法</span><span class="sxs-lookup"><span data-stu-id="3960d-104">SYNTAX</span></span>

### <span data-ttu-id="3960d-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="3960d-105">SetByResource (Default)</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3960d-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3960d-106">SetByResourceId</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3960d-107">說明</span><span class="sxs-lookup"><span data-stu-id="3960d-107">DESCRIPTION</span></span>
<span data-ttu-id="3960d-108">**AzNetworkSecurityRuleConfig** Cmdlet 會更新網路安全性群組的網路安全規則配置。</span><span class="sxs-lookup"><span data-stu-id="3960d-108">The **Set-AzNetworkSecurityRuleConfig** cmdlet updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="3960d-109">示例</span><span class="sxs-lookup"><span data-stu-id="3960d-109">EXAMPLES</span></span>

### <span data-ttu-id="3960d-110">範例1：變更網路安全性規則中的存取設定</span><span class="sxs-lookup"><span data-stu-id="3960d-110">Example 1: Change the access configuration in a network security rule</span></span>
```powershell
PS C:\>$nsg = Get-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="3960d-111">第一個命令會取得名為 NSG-前端的網路安全性群組，然後將它儲存在 $nsg 的變數中。</span><span class="sxs-lookup"><span data-stu-id="3960d-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>
<span data-ttu-id="3960d-112">第二個命令會使用管線運算子，將 $nsg 的安全性群組傳遞給 AzNetworkSecurityRuleConfig，以取得名為 rdp 規則的安全性規則設定。</span><span class="sxs-lookup"><span data-stu-id="3960d-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>
<span data-ttu-id="3960d-113">第三個命令會將 rdp 規則的存取設定變更為 [拒絕]。</span><span class="sxs-lookup"><span data-stu-id="3960d-113">The third command changes the access configuration of rdp-rule to Deny.</span></span>

### <span data-ttu-id="3960d-114">範例2</span><span class="sxs-lookup"><span data-stu-id="3960d-114">Example 2</span></span>

<span data-ttu-id="3960d-115">更新網路安全性群組的網路安全規則配置。</span><span class="sxs-lookup"><span data-stu-id="3960d-115">Updates a network security rule configuration for a network security group.</span></span> <span data-ttu-id="3960d-116"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="3960d-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzNetworkSecurityRuleConfig -Access Allow -DestinationAddressPrefix * -DestinationPortRange 3389 -Direction Inbound -Name 'rdp-rule' -NetworkSecurityGroup <PSNetworkSecurityGroup> -Priority 1 -Protocol Tcp -SourceAddressPrefix 'Internet' -SourcePortRange *
```

## <span data-ttu-id="3960d-117">參數</span><span class="sxs-lookup"><span data-stu-id="3960d-117">PARAMETERS</span></span>

### <span data-ttu-id="3960d-118">-Access</span><span class="sxs-lookup"><span data-stu-id="3960d-118">-Access</span></span>
<span data-ttu-id="3960d-119">指定是否允許或拒絕網路流量。</span><span class="sxs-lookup"><span data-stu-id="3960d-119">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="3960d-120">此參數可接受的值為： [允許] 和 [拒絕]。</span><span class="sxs-lookup"><span data-stu-id="3960d-120">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="3960d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3960d-121">-DefaultProfile</span></span>
<span data-ttu-id="3960d-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3960d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3960d-123">-描述</span><span class="sxs-lookup"><span data-stu-id="3960d-123">-Description</span></span>
<span data-ttu-id="3960d-124">指定規則配置的描述。</span><span class="sxs-lookup"><span data-stu-id="3960d-124">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="3960d-125">最大大小為140個字元。</span><span class="sxs-lookup"><span data-stu-id="3960d-125">The maximum size is 140 characters.</span></span>

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

### <span data-ttu-id="3960d-126">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="3960d-126">-DestinationAddressPrefix</span></span>
<span data-ttu-id="3960d-127">指定目的地位址首碼。</span><span class="sxs-lookup"><span data-stu-id="3960d-127">Specifies a destination address prefix.</span></span>
<span data-ttu-id="3960d-128">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="3960d-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3960d-129">未類別的域間路由 (CIDR) 位址</span><span class="sxs-lookup"><span data-stu-id="3960d-129">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="3960d-130">目的地 IP 位址範圍</span><span class="sxs-lookup"><span data-stu-id="3960d-130">A destination IP address range</span></span> 
- <span data-ttu-id="3960d-131">萬用字元 ( \* ) 若要與任何 IP 位址相符，您可以使用 VirtualNetwork、AzureLoadBalancer 和 Internet 等標記。</span><span class="sxs-lookup"><span data-stu-id="3960d-131">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="3960d-132">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3960d-132">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="3960d-133">針對規則設定為目的地的應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="3960d-133">The application security group set as destination for the rule.</span></span> <span data-ttu-id="3960d-134">它不能與 "DestinationAddressPrefix" 參數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="3960d-134">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="3960d-135">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="3960d-135">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="3960d-136">針對規則設定為目的地的應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="3960d-136">The application security group set as destination for the rule.</span></span> <span data-ttu-id="3960d-137">它不能與 "DestinationAddressPrefix" 參數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="3960d-137">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="3960d-138">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="3960d-138">-DestinationPortRange</span></span>
<span data-ttu-id="3960d-139">指定目的地埠或範圍。</span><span class="sxs-lookup"><span data-stu-id="3960d-139">Specifies a destination port or range.</span></span>
<span data-ttu-id="3960d-140">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="3960d-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3960d-141">整數</span><span class="sxs-lookup"><span data-stu-id="3960d-141">An integer</span></span> 
- <span data-ttu-id="3960d-142">0到65535之間的整數範圍</span><span class="sxs-lookup"><span data-stu-id="3960d-142">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="3960d-143">萬用字元 ( \* ) 與任何埠相符</span><span class="sxs-lookup"><span data-stu-id="3960d-143">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="3960d-144">方向</span><span class="sxs-lookup"><span data-stu-id="3960d-144">-Direction</span></span>
<span data-ttu-id="3960d-145">指定是否針對內向或出局流量評估規則。</span><span class="sxs-lookup"><span data-stu-id="3960d-145">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="3960d-146">此參數可接受的值為：入站和出站。</span><span class="sxs-lookup"><span data-stu-id="3960d-146">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="3960d-147">-名稱</span><span class="sxs-lookup"><span data-stu-id="3960d-147">-Name</span></span>
<span data-ttu-id="3960d-148">指定此 Cmdlet 設定的網路安全規則配置名稱。</span><span class="sxs-lookup"><span data-stu-id="3960d-148">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="3960d-149">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3960d-149">-NetworkSecurityGroup</span></span>
<span data-ttu-id="3960d-150">指定包含要設定之網路安全性規則配置的 **NetworkSecurityGroup** 物件。</span><span class="sxs-lookup"><span data-stu-id="3960d-150">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

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

### <span data-ttu-id="3960d-151">-優先順序</span><span class="sxs-lookup"><span data-stu-id="3960d-151">-Priority</span></span>
<span data-ttu-id="3960d-152">指定規則配置的優先順序。</span><span class="sxs-lookup"><span data-stu-id="3960d-152">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="3960d-153">此參數可接受的值為：100和4096之間的整數。</span><span class="sxs-lookup"><span data-stu-id="3960d-153">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>
<span data-ttu-id="3960d-154">對於集合中的每個規則，優先順序編號必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="3960d-154">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="3960d-155">優先順序編號越低，規則的優先順序就越高。</span><span class="sxs-lookup"><span data-stu-id="3960d-155">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="3960d-156">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="3960d-156">-Protocol</span></span>
<span data-ttu-id="3960d-157">指定規則配置適用的網路通訊協定。</span><span class="sxs-lookup"><span data-stu-id="3960d-157">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="3960d-158">此參數可接受的值為：--Tcp</span><span class="sxs-lookup"><span data-stu-id="3960d-158">The acceptable values for this parameter are: --Tcp</span></span>
- <span data-ttu-id="3960d-159">Udp-in</span><span class="sxs-lookup"><span data-stu-id="3960d-159">Udp</span></span>
- <span data-ttu-id="3960d-160">萬用字元 ( \* ) 與以上兩個字都相符</span><span class="sxs-lookup"><span data-stu-id="3960d-160">A wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="3960d-161">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="3960d-161">-SourceAddressPrefix</span></span>
<span data-ttu-id="3960d-162">指定來源位址首碼。</span><span class="sxs-lookup"><span data-stu-id="3960d-162">Specifies a source address prefix.</span></span>
<span data-ttu-id="3960d-163">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="3960d-163">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3960d-164">CIDR</span><span class="sxs-lookup"><span data-stu-id="3960d-164">A CIDR</span></span>
- <span data-ttu-id="3960d-165">來源 IP 範圍</span><span class="sxs-lookup"><span data-stu-id="3960d-165">A source IP range</span></span>
- <span data-ttu-id="3960d-166">萬用字元 ( \* ) 若要與任何 IP 位址相符，您也可以使用 VirtualNetwork、AzureLoadBalancer 和 Internet 等標記。</span><span class="sxs-lookup"><span data-stu-id="3960d-166">A wildcard character (\*) to match any IP address You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="3960d-167">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3960d-167">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="3960d-168">針對規則設定為 [來源] 的應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="3960d-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="3960d-169">它不能與 "SourceAddressPrefix" 參數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="3960d-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="3960d-170">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="3960d-170">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="3960d-171">針對規則設定為 [來源] 的應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="3960d-171">The application security group set as source for the rule.</span></span> <span data-ttu-id="3960d-172">它不能與 "SourceAddressPrefix" 參數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="3960d-172">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="3960d-173">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="3960d-173">-SourcePortRange</span></span>
<span data-ttu-id="3960d-174">指定來源埠或範圍。</span><span class="sxs-lookup"><span data-stu-id="3960d-174">Specifies the source port or range.</span></span>
<span data-ttu-id="3960d-175">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="3960d-175">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3960d-176">整數</span><span class="sxs-lookup"><span data-stu-id="3960d-176">An integer</span></span>
- <span data-ttu-id="3960d-177">0到65535之間的整數範圍</span><span class="sxs-lookup"><span data-stu-id="3960d-177">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="3960d-178">萬用字元 ( \* ) 與任何埠相符</span><span class="sxs-lookup"><span data-stu-id="3960d-178">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="3960d-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3960d-179">CommonParameters</span></span>
<span data-ttu-id="3960d-180">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3960d-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3960d-181">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3960d-181">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3960d-182">輸入</span><span class="sxs-lookup"><span data-stu-id="3960d-182">INPUTS</span></span>

### <span data-ttu-id="3960d-183">PSNetworkSecurityGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3960d-183">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="3960d-184">輸出</span><span class="sxs-lookup"><span data-stu-id="3960d-184">OUTPUTS</span></span>

### <span data-ttu-id="3960d-185">PSNetworkSecurityGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3960d-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="3960d-186">筆記</span><span class="sxs-lookup"><span data-stu-id="3960d-186">NOTES</span></span>

## <span data-ttu-id="3960d-187">相關連結</span><span class="sxs-lookup"><span data-stu-id="3960d-187">RELATED LINKS</span></span>

[<span data-ttu-id="3960d-188">附加 AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3960d-188">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="3960d-189">AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3960d-189">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="3960d-190">新-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3960d-190">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="3960d-191">移除-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3960d-191">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)


