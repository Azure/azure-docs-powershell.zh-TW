---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/powershell/module/az.network/set-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 12967d69e1886b6446db906e5822fd10bbad0037
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915273"
---
# <span data-ttu-id="1743d-101">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1743d-101">Set-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="1743d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1743d-102">SYNOPSIS</span></span>
<span data-ttu-id="1743d-103">更新網路安全性群組的網路安全性規則組。</span><span class="sxs-lookup"><span data-stu-id="1743d-103">Updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="1743d-104">語法</span><span class="sxs-lookup"><span data-stu-id="1743d-104">SYNTAX</span></span>

### <span data-ttu-id="1743d-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="1743d-105">SetByResource (Default)</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1743d-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1743d-106">SetByResourceId</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1743d-107">描述</span><span class="sxs-lookup"><span data-stu-id="1743d-107">DESCRIPTION</span></span>
<span data-ttu-id="1743d-108">**Set-AzNetworkSecurityRuleConfig** Cmdlet 會更新網路安全性群組的網路安全性規則設定。</span><span class="sxs-lookup"><span data-stu-id="1743d-108">The **Set-AzNetworkSecurityRuleConfig** cmdlet updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="1743d-109">例子</span><span class="sxs-lookup"><span data-stu-id="1743d-109">EXAMPLES</span></span>

### <span data-ttu-id="1743d-110">範例 1：變更網路安全性規則的存取組</span><span class="sxs-lookup"><span data-stu-id="1743d-110">Example 1: Change the access configuration in a network security rule</span></span>
```powershell
PS C:\>$nsg = Get-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="1743d-111">第一個命令會獲得名為 NSG-FrontEnd 的網路安全性群組，然後將它儲存在變數 $nsg。</span><span class="sxs-lookup"><span data-stu-id="1743d-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>
<span data-ttu-id="1743d-112">第二個命令使用管線運算子，將 $nsg 中的安全性組傳遞到 Get-AzNetworkSecurityRuleConfig，此命令會取得名為 rdp-rule 的安全性規則組。</span><span class="sxs-lookup"><span data-stu-id="1743d-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>
<span data-ttu-id="1743d-113">第三個命令將 rdp-rule 的存取組式變更為拒絕。</span><span class="sxs-lookup"><span data-stu-id="1743d-113">The third command changes the access configuration of rdp-rule to Deny.</span></span> <span data-ttu-id="1743d-114">不過，這會覆寫規則，並且只設定傳遞至 Set-AzNetworkSecurityRuleConfig 函數的參數。</span><span class="sxs-lookup"><span data-stu-id="1743d-114">However, this overwrites the rule and only sets the parameters that are passed to the Set-AzNetworkSecurityRuleConfig function.</span></span>   <span data-ttu-id="1743d-115">注意：無法變更單一屬性</span><span class="sxs-lookup"><span data-stu-id="1743d-115">NOTE: There is no way to change a single attribute</span></span>

### <span data-ttu-id="1743d-116">範例 2</span><span class="sxs-lookup"><span data-stu-id="1743d-116">Example 2</span></span>

<span data-ttu-id="1743d-117">更新網路安全性群組的網路安全性規則組。</span><span class="sxs-lookup"><span data-stu-id="1743d-117">Updates a network security rule configuration for a network security group.</span></span> <span data-ttu-id="1743d-118"> (自動) </span><span class="sxs-lookup"><span data-stu-id="1743d-118">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzNetworkSecurityRuleConfig -Access Allow -DestinationAddressPrefix * -DestinationPortRange 3389 -Direction Inbound -Name 'rdp-rule' -NetworkSecurityGroup <PSNetworkSecurityGroup> -Priority 1 -Protocol Tcp -SourceAddressPrefix 'Internet' -SourcePortRange *
```

## <span data-ttu-id="1743d-119">參數</span><span class="sxs-lookup"><span data-stu-id="1743d-119">PARAMETERS</span></span>

### <span data-ttu-id="1743d-120">-Access</span><span class="sxs-lookup"><span data-stu-id="1743d-120">-Access</span></span>
<span data-ttu-id="1743d-121">指定是否允許或拒絕網路流量。</span><span class="sxs-lookup"><span data-stu-id="1743d-121">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="1743d-122">此參數可接受的值為：允許和拒絕。</span><span class="sxs-lookup"><span data-stu-id="1743d-122">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="1743d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1743d-123">-DefaultProfile</span></span>
<span data-ttu-id="1743d-124">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1743d-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1743d-125">-描述</span><span class="sxs-lookup"><span data-stu-id="1743d-125">-Description</span></span>
<span data-ttu-id="1743d-126">指定規則組配置的描述。</span><span class="sxs-lookup"><span data-stu-id="1743d-126">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="1743d-127">大小上限為 140 個字元。</span><span class="sxs-lookup"><span data-stu-id="1743d-127">The maximum size is 140 characters.</span></span>

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

### <span data-ttu-id="1743d-128">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="1743d-128">-DestinationAddressPrefix</span></span>
<span data-ttu-id="1743d-129">指定目的地位址首碼。</span><span class="sxs-lookup"><span data-stu-id="1743d-129">Specifies a destination address prefix.</span></span>
<span data-ttu-id="1743d-130">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="1743d-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1743d-131">CIDR 位址的無 (域) 路由</span><span class="sxs-lookup"><span data-stu-id="1743d-131">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="1743d-132">目的地 IP 位址範圍</span><span class="sxs-lookup"><span data-stu-id="1743d-132">A destination IP address range</span></span> 
- <span data-ttu-id="1743d-133">萬用字元 (\*) 比對任何 IP 位址。您可以使用 VirtualNetwork、AzureLoadBalancer 和 Internet 等標記。</span><span class="sxs-lookup"><span data-stu-id="1743d-133">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="1743d-134">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1743d-134">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="1743d-135">應用程式安全性群組設定為規則的目的地。</span><span class="sxs-lookup"><span data-stu-id="1743d-135">The application security group set as destination for the rule.</span></span> <span data-ttu-id="1743d-136">它無法與 "DestinationAddressPrefix" 參數一起使用。</span><span class="sxs-lookup"><span data-stu-id="1743d-136">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="1743d-137">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="1743d-137">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="1743d-138">應用程式安全性群組設定為規則的目的地。</span><span class="sxs-lookup"><span data-stu-id="1743d-138">The application security group set as destination for the rule.</span></span> <span data-ttu-id="1743d-139">它無法與 "DestinationAddressPrefix" 參數一起使用。</span><span class="sxs-lookup"><span data-stu-id="1743d-139">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="1743d-140">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="1743d-140">-DestinationPortRange</span></span>
<span data-ttu-id="1743d-141">指定目的地埠或範圍。</span><span class="sxs-lookup"><span data-stu-id="1743d-141">Specifies a destination port or range.</span></span>
<span data-ttu-id="1743d-142">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="1743d-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1743d-143">整數</span><span class="sxs-lookup"><span data-stu-id="1743d-143">An integer</span></span> 
- <span data-ttu-id="1743d-144">介於 0 到 65535 之間的整數範圍</span><span class="sxs-lookup"><span data-stu-id="1743d-144">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="1743d-145">\* (\*) 字元來比對任何埠</span><span class="sxs-lookup"><span data-stu-id="1743d-145">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="1743d-146">-方向</span><span class="sxs-lookup"><span data-stu-id="1743d-146">-Direction</span></span>
<span data-ttu-id="1743d-147">指定規則是評估內流量還是外發流量。</span><span class="sxs-lookup"><span data-stu-id="1743d-147">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="1743d-148">此參數可接受的值為：輸入和外發。</span><span class="sxs-lookup"><span data-stu-id="1743d-148">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="1743d-149">-名稱</span><span class="sxs-lookup"><span data-stu-id="1743d-149">-Name</span></span>
<span data-ttu-id="1743d-150">指定此 Cmdlet 所設定之網路安全性規則組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1743d-150">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="1743d-151">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1743d-151">-NetworkSecurityGroup</span></span>
<span data-ttu-id="1743d-152">指定包含要設定之網路安全性規則設定之 **NetworkSecurityGroup** 物件。</span><span class="sxs-lookup"><span data-stu-id="1743d-152">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

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

### <span data-ttu-id="1743d-153">-優先順序</span><span class="sxs-lookup"><span data-stu-id="1743d-153">-Priority</span></span>
<span data-ttu-id="1743d-154">指定規則配置的優先順序。</span><span class="sxs-lookup"><span data-stu-id="1743d-154">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="1743d-155">此參數可接受的值為：介於 100 和 4096 之間的整數。</span><span class="sxs-lookup"><span data-stu-id="1743d-155">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>
<span data-ttu-id="1743d-156">優先順序數位必須是唯一的，因為集合中每個規則都是唯一的。</span><span class="sxs-lookup"><span data-stu-id="1743d-156">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="1743d-157">優先順序數位越低，規則的優先順序越高。</span><span class="sxs-lookup"><span data-stu-id="1743d-157">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="1743d-158">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="1743d-158">-Protocol</span></span>
<span data-ttu-id="1743d-159">指定規則組配置所適用的網路通訊協定。</span><span class="sxs-lookup"><span data-stu-id="1743d-159">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="1743d-160">此參數可接受的值為：--Tcp</span><span class="sxs-lookup"><span data-stu-id="1743d-160">The acceptable values for this parameter are: --Tcp</span></span>
- <span data-ttu-id="1743d-161">Udp</span><span class="sxs-lookup"><span data-stu-id="1743d-161">Udp</span></span>
- <span data-ttu-id="1743d-162">\**的萬用字元 (*) 兩者相符</span><span class="sxs-lookup"><span data-stu-id="1743d-162">A wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="1743d-163">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="1743d-163">-SourceAddressPrefix</span></span>
<span data-ttu-id="1743d-164">指定來源位址首碼。</span><span class="sxs-lookup"><span data-stu-id="1743d-164">Specifies a source address prefix.</span></span>
<span data-ttu-id="1743d-165">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="1743d-165">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1743d-166">A CIDR</span><span class="sxs-lookup"><span data-stu-id="1743d-166">A CIDR</span></span>
- <span data-ttu-id="1743d-167">來源 IP 範圍</span><span class="sxs-lookup"><span data-stu-id="1743d-167">A source IP range</span></span>
- <span data-ttu-id="1743d-168">萬用字元 (\*) 比對任何 IP 位址。您也可以使用 VirtualNetwork、AzureLoadBalancer 和 Internet 等標記。</span><span class="sxs-lookup"><span data-stu-id="1743d-168">A wildcard character (\*) to match any IP address You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="1743d-169">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1743d-169">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="1743d-170">應用程式安全性群組設定為規則的來源。</span><span class="sxs-lookup"><span data-stu-id="1743d-170">The application security group set as source for the rule.</span></span> <span data-ttu-id="1743d-171">它無法與 'SourceAddressPrefix' 參數一起使用。</span><span class="sxs-lookup"><span data-stu-id="1743d-171">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="1743d-172">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="1743d-172">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="1743d-173">應用程式安全性群組設定為規則的來源。</span><span class="sxs-lookup"><span data-stu-id="1743d-173">The application security group set as source for the rule.</span></span> <span data-ttu-id="1743d-174">它無法與 'SourceAddressPrefix' 參數一起使用。</span><span class="sxs-lookup"><span data-stu-id="1743d-174">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="1743d-175">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="1743d-175">-SourcePortRange</span></span>
<span data-ttu-id="1743d-176">指定來源埠或範圍。</span><span class="sxs-lookup"><span data-stu-id="1743d-176">Specifies the source port or range.</span></span>
<span data-ttu-id="1743d-177">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="1743d-177">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1743d-178">整數</span><span class="sxs-lookup"><span data-stu-id="1743d-178">An integer</span></span>
- <span data-ttu-id="1743d-179">介於 0 到 65535 之間的整數範圍</span><span class="sxs-lookup"><span data-stu-id="1743d-179">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="1743d-180">\* (\*) 字元來比對任何埠</span><span class="sxs-lookup"><span data-stu-id="1743d-180">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="1743d-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1743d-181">CommonParameters</span></span>
<span data-ttu-id="1743d-182">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1743d-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1743d-183">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="1743d-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1743d-184">輸入</span><span class="sxs-lookup"><span data-stu-id="1743d-184">INPUTS</span></span>

### <span data-ttu-id="1743d-185">Microsoft.Azure.Commands.Network.models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1743d-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="1743d-186">輸出</span><span class="sxs-lookup"><span data-stu-id="1743d-186">OUTPUTS</span></span>

### <span data-ttu-id="1743d-187">Microsoft.Azure.Commands.Network.models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1743d-187">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="1743d-188">筆記</span><span class="sxs-lookup"><span data-stu-id="1743d-188">NOTES</span></span>

## <span data-ttu-id="1743d-189">相關連結</span><span class="sxs-lookup"><span data-stu-id="1743d-189">RELATED LINKS</span></span>

[<span data-ttu-id="1743d-190">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1743d-190">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="1743d-191">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1743d-191">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="1743d-192">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1743d-192">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="1743d-193">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1743d-193">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)


