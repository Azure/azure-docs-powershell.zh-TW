---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityRuleConfig.md
ms.openlocfilehash: c1febd5d39e99ef52e940c590fcd43c24b19affd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454699"
---
# <span data-ttu-id="d69cd-101">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d69cd-101">Set-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="d69cd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d69cd-102">SYNOPSIS</span></span>
<span data-ttu-id="d69cd-103">設定網路安全規則配置的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="d69cd-103">Sets the goal state for a network security rule configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d69cd-104">句法</span><span class="sxs-lookup"><span data-stu-id="d69cd-104">SYNTAX</span></span>

### <span data-ttu-id="d69cd-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="d69cd-105">SetByResource (Default)</span></span>
```
Set-AzureRmNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
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

### <span data-ttu-id="d69cd-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d69cd-106">SetByResourceId</span></span>
```
Set-AzureRmNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DestinationApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-Access <String>]
 [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d69cd-107">說明</span><span class="sxs-lookup"><span data-stu-id="d69cd-107">DESCRIPTION</span></span>
<span data-ttu-id="d69cd-108">**AzureRmNetworkSecurityRuleConfig** Cmdlet 會為 Azure 網路安全性規則設定設定目標狀態。</span><span class="sxs-lookup"><span data-stu-id="d69cd-108">The **Set-AzureRmNetworkSecurityRuleConfig** cmdlet sets the goal state for an Azure network security rule configuration.</span></span>

## <span data-ttu-id="d69cd-109">示例</span><span class="sxs-lookup"><span data-stu-id="d69cd-109">EXAMPLES</span></span>

### <span data-ttu-id="d69cd-110">範例1：變更網路安全性規則中的存取設定</span><span class="sxs-lookup"><span data-stu-id="d69cd-110">Example 1: Change the access configuration in a network security rule</span></span>
```
PS C:\>$nsg = Get-AzureRmNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="d69cd-111">第一個命令會取得名為 NSG-前端的網路安全性群組，然後將它儲存在 $nsg 的變數中。</span><span class="sxs-lookup"><span data-stu-id="d69cd-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>

<span data-ttu-id="d69cd-112">第二個命令會使用管線運算子，將 $nsg 的安全性群組傳遞給 AzureRmNetworkSecurityRuleConfig，以取得名為 rdp 規則的安全性規則設定。</span><span class="sxs-lookup"><span data-stu-id="d69cd-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzureRmNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>

<span data-ttu-id="d69cd-113">第三個命令會將 rdp 規則的存取設定變更為 [拒絕]。</span><span class="sxs-lookup"><span data-stu-id="d69cd-113">The third command changes the access configuration of rdp-rule to Deny.</span></span>

## <span data-ttu-id="d69cd-114">參數</span><span class="sxs-lookup"><span data-stu-id="d69cd-114">PARAMETERS</span></span>

### <span data-ttu-id="d69cd-115">-Access</span><span class="sxs-lookup"><span data-stu-id="d69cd-115">-Access</span></span>
<span data-ttu-id="d69cd-116">指定是否允許或拒絕網路流量。</span><span class="sxs-lookup"><span data-stu-id="d69cd-116">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="d69cd-117">此參數可接受的值為： [允許] 和 [拒絕]。</span><span class="sxs-lookup"><span data-stu-id="d69cd-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="d69cd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d69cd-118">-DefaultProfile</span></span>
<span data-ttu-id="d69cd-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d69cd-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d69cd-120">-描述</span><span class="sxs-lookup"><span data-stu-id="d69cd-120">-Description</span></span>
<span data-ttu-id="d69cd-121">指定規則配置的描述。</span><span class="sxs-lookup"><span data-stu-id="d69cd-121">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="d69cd-122">最大大小為140個字元。</span><span class="sxs-lookup"><span data-stu-id="d69cd-122">The maximum size is 140 characters.</span></span>

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

### <span data-ttu-id="d69cd-123">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="d69cd-123">-DestinationAddressPrefix</span></span>
<span data-ttu-id="d69cd-124">指定目的地位址首碼。</span><span class="sxs-lookup"><span data-stu-id="d69cd-124">Specifies a destination address prefix.</span></span>
<span data-ttu-id="d69cd-125">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="d69cd-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d69cd-126">未類別的域間路由 (CIDR) 位址</span><span class="sxs-lookup"><span data-stu-id="d69cd-126">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="d69cd-127">目的地 IP 位址範圍</span><span class="sxs-lookup"><span data-stu-id="d69cd-127">A destination IP address range</span></span> 
- <span data-ttu-id="d69cd-128">萬用字元 ( \* ) ，以符合任何 IP 位址</span><span class="sxs-lookup"><span data-stu-id="d69cd-128">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="d69cd-129">您可以使用 [VirtualNetwork]、[AzureLoadBalancer] 和 [網際網路] 等標記。</span><span class="sxs-lookup"><span data-stu-id="d69cd-129">You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="d69cd-130">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d69cd-130">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="d69cd-131">針對規則設定為目的地的應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="d69cd-131">The application security group set as destination for the rule.</span></span> <span data-ttu-id="d69cd-132">它不能與 "DestinationAddressPrefix" 參數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="d69cd-132">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="d69cd-133">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="d69cd-133">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="d69cd-134">針對規則設定為目的地的應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="d69cd-134">The application security group set as destination for the rule.</span></span> <span data-ttu-id="d69cd-135">它不能與 "DestinationAddressPrefix" 參數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="d69cd-135">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="d69cd-136">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="d69cd-136">-DestinationPortRange</span></span>
<span data-ttu-id="d69cd-137">指定目的地埠或範圍。</span><span class="sxs-lookup"><span data-stu-id="d69cd-137">Specifies a destination port or range.</span></span>
<span data-ttu-id="d69cd-138">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="d69cd-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d69cd-139">整數</span><span class="sxs-lookup"><span data-stu-id="d69cd-139">An integer</span></span> 
- <span data-ttu-id="d69cd-140">0到65535之間的整數範圍</span><span class="sxs-lookup"><span data-stu-id="d69cd-140">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="d69cd-141">萬用字元 ( \* ) 與任何埠相符</span><span class="sxs-lookup"><span data-stu-id="d69cd-141">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="d69cd-142">方向</span><span class="sxs-lookup"><span data-stu-id="d69cd-142">-Direction</span></span>
<span data-ttu-id="d69cd-143">指定是否針對內向或出局流量評估規則。</span><span class="sxs-lookup"><span data-stu-id="d69cd-143">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="d69cd-144">此參數可接受的值為：入站和出站。</span><span class="sxs-lookup"><span data-stu-id="d69cd-144">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="d69cd-145">-名稱</span><span class="sxs-lookup"><span data-stu-id="d69cd-145">-Name</span></span>
<span data-ttu-id="d69cd-146">指定此 Cmdlet 設定的網路安全規則配置名稱。</span><span class="sxs-lookup"><span data-stu-id="d69cd-146">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="d69cd-147">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d69cd-147">-NetworkSecurityGroup</span></span>
<span data-ttu-id="d69cd-148">指定包含要設定之網路安全性規則配置的 **NetworkSecurityGroup** 物件。</span><span class="sxs-lookup"><span data-stu-id="d69cd-148">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

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

### <span data-ttu-id="d69cd-149">-優先順序</span><span class="sxs-lookup"><span data-stu-id="d69cd-149">-Priority</span></span>
<span data-ttu-id="d69cd-150">指定規則配置的優先順序。</span><span class="sxs-lookup"><span data-stu-id="d69cd-150">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="d69cd-151">此參數可接受的值為：100和4096之間的整數。</span><span class="sxs-lookup"><span data-stu-id="d69cd-151">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>

<span data-ttu-id="d69cd-152">對於集合中的每個規則，優先順序編號必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="d69cd-152">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="d69cd-153">優先順序編號越低，規則的優先順序就越高。</span><span class="sxs-lookup"><span data-stu-id="d69cd-153">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="d69cd-154">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="d69cd-154">-Protocol</span></span>
<span data-ttu-id="d69cd-155">指定規則配置適用的網路通訊協定。</span><span class="sxs-lookup"><span data-stu-id="d69cd-155">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="d69cd-156">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="d69cd-156">The acceptable values for this parameter are:</span></span>

 <span data-ttu-id="d69cd-157">--Tcp</span><span class="sxs-lookup"><span data-stu-id="d69cd-157">--Tcp</span></span>
- <span data-ttu-id="d69cd-158">Udp-in</span><span class="sxs-lookup"><span data-stu-id="d69cd-158">Udp</span></span>
- <span data-ttu-id="d69cd-159">萬用字元 ( \* ) 與以上兩個字都相符</span><span class="sxs-lookup"><span data-stu-id="d69cd-159">A wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="d69cd-160">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="d69cd-160">-SourceAddressPrefix</span></span>
<span data-ttu-id="d69cd-161">指定來源位址首碼。</span><span class="sxs-lookup"><span data-stu-id="d69cd-161">Specifies a source address prefix.</span></span>
<span data-ttu-id="d69cd-162">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="d69cd-162">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d69cd-163">CIDR</span><span class="sxs-lookup"><span data-stu-id="d69cd-163">A CIDR</span></span>
- <span data-ttu-id="d69cd-164">來源 IP 範圍</span><span class="sxs-lookup"><span data-stu-id="d69cd-164">A source IP range</span></span>
- <span data-ttu-id="d69cd-165">萬用字元 ( \* ) ，以符合任何 IP 位址</span><span class="sxs-lookup"><span data-stu-id="d69cd-165">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="d69cd-166">您也可以使用 [VirtualNetwork]、[AzureLoadBalancer] 和 [網際網路] 等標記。</span><span class="sxs-lookup"><span data-stu-id="d69cd-166">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="d69cd-167">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d69cd-167">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="d69cd-168">針對規則設定為 [來源] 的應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="d69cd-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="d69cd-169">它不能與 "SourceAddressPrefix" 參數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="d69cd-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="d69cd-170">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="d69cd-170">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="d69cd-171">針對規則設定為 [來源] 的應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="d69cd-171">The application security group set as source for the rule.</span></span> <span data-ttu-id="d69cd-172">它不能與 "SourceAddressPrefix" 參數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="d69cd-172">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="d69cd-173">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="d69cd-173">-SourcePortRange</span></span>
<span data-ttu-id="d69cd-174">指定來源埠或範圍。</span><span class="sxs-lookup"><span data-stu-id="d69cd-174">Specifies the source port or range.</span></span>
<span data-ttu-id="d69cd-175">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="d69cd-175">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d69cd-176">整數</span><span class="sxs-lookup"><span data-stu-id="d69cd-176">An integer</span></span>
- <span data-ttu-id="d69cd-177">0到65535之間的整數範圍</span><span class="sxs-lookup"><span data-stu-id="d69cd-177">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="d69cd-178">萬用字元 ( \* ) 與任何埠相符</span><span class="sxs-lookup"><span data-stu-id="d69cd-178">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="d69cd-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d69cd-179">CommonParameters</span></span>
<span data-ttu-id="d69cd-180">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d69cd-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d69cd-181">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d69cd-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d69cd-182">輸入</span><span class="sxs-lookup"><span data-stu-id="d69cd-182">INPUTS</span></span>

### <span data-ttu-id="d69cd-183">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d69cd-183">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="d69cd-184">形參 "NetworkSecurityGroup" 接受管線中 "PSNetworkSecurityGroup" 類型的值</span><span class="sxs-lookup"><span data-stu-id="d69cd-184">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="d69cd-185">輸出</span><span class="sxs-lookup"><span data-stu-id="d69cd-185">OUTPUTS</span></span>

### <span data-ttu-id="d69cd-186">PSNetworkSecurityGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d69cd-186">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="d69cd-187">筆記</span><span class="sxs-lookup"><span data-stu-id="d69cd-187">NOTES</span></span>

## <span data-ttu-id="d69cd-188">相關連結</span><span class="sxs-lookup"><span data-stu-id="d69cd-188">RELATED LINKS</span></span>

[<span data-ttu-id="d69cd-189">附加 AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d69cd-189">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="d69cd-190">AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d69cd-190">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="d69cd-191">新-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d69cd-191">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="d69cd-192">移除-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d69cd-192">Remove-AzureRmNetworkSecurityRuleConfig</span></span>](./Remove-AzureRmNetworkSecurityRuleConfig.md)

