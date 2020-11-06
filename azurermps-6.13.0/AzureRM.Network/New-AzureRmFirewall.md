---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewall.md
ms.openlocfilehash: 6486c7db87e8c71b0703b90a765fa30287b82769
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456008"
---
# <span data-ttu-id="bbce3-101">New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="bbce3-101">New-AzureRmFirewall</span></span>

## <span data-ttu-id="bbce3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bbce3-102">SYNOPSIS</span></span>
<span data-ttu-id="bbce3-103">在資源群組中建立新的防火牆。</span><span class="sxs-lookup"><span data-stu-id="bbce3-103">Creates a new Firewall in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bbce3-104">句法</span><span class="sxs-lookup"><span data-stu-id="bbce3-104">SYNTAX</span></span>

```
New-AzureRmFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-VirtualNetworkName <String>] [-PublicIpName <String>]
 [-ApplicationRuleCollection <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection]>]
 [-NatRuleCollection <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection]>]
 [-NetworkRuleCollection <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bbce3-105">說明</span><span class="sxs-lookup"><span data-stu-id="bbce3-105">DESCRIPTION</span></span>
<span data-ttu-id="bbce3-106">**新的-AzureRmFirewall** Cmdlet 會建立 Azure 防火牆。</span><span class="sxs-lookup"><span data-stu-id="bbce3-106">The **New-AzureRmFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="bbce3-107">示例</span><span class="sxs-lookup"><span data-stu-id="bbce3-107">EXAMPLES</span></span>

### <span data-ttu-id="bbce3-108">1：建立附加至虛擬網路的防火牆</span><span class="sxs-lookup"><span data-stu-id="bbce3-108">1:  Create a Firewall attached to a virtual network</span></span>
```
New-AzureRmFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name"
```

<span data-ttu-id="bbce3-109">這個範例會在與防火牆相同的資源群組中，建立附加至虛擬網路 "vnet" 的防火牆。</span><span class="sxs-lookup"><span data-stu-id="bbce3-109">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="bbce3-110">因為未指定任何規則，所以防火牆會封鎖所有流量 (預設行為) 。</span><span class="sxs-lookup"><span data-stu-id="bbce3-110">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>

### <span data-ttu-id="bbce3-111">2：建立可讓所有 HTTPS 流量使用的防火牆</span><span class="sxs-lookup"><span data-stu-id="bbce3-111">2:  Create a Firewall which allows all HTTPS traffic</span></span>
```
$rule = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzureRmFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzureRmFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name" -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="bbce3-112">這個範例會建立可讓埠443上所有 HTTPS 流量的防火牆。</span><span class="sxs-lookup"><span data-stu-id="bbce3-112">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>

### <span data-ttu-id="bbce3-113">3： DNAT-將流向10.1.2.3：80的流量重新導向至10.2.3.4：8080</span><span class="sxs-lookup"><span data-stu-id="bbce3-113">3:  DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```
$rule = New-AzureRmFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzureRmFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzureRmFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection
```

<span data-ttu-id="bbce3-114">這個範例建立了一個將10.1.2.3：80到10.2.3.4：8080的所有資料包的目的地 IP 和埠轉換成的防火牆。</span><span class="sxs-lookup"><span data-stu-id="bbce3-114">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>

## <span data-ttu-id="bbce3-115">參數</span><span class="sxs-lookup"><span data-stu-id="bbce3-115">PARAMETERS</span></span>

### <span data-ttu-id="bbce3-116">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="bbce3-116">-ApplicationRuleCollection</span></span>
<span data-ttu-id="bbce3-117">指定新防火牆的應用程式規則集合。</span><span class="sxs-lookup"><span data-stu-id="bbce3-117">Specifies the collections of application rules for the new Firewall.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbce3-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bbce3-118">-AsJob</span></span>
<span data-ttu-id="bbce3-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="bbce3-119">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbce3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbce3-120">-DefaultProfile</span></span>
<span data-ttu-id="bbce3-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bbce3-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bbce3-122">-Force</span><span class="sxs-lookup"><span data-stu-id="bbce3-122">-Force</span></span>
<span data-ttu-id="bbce3-123">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="bbce3-123">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbce3-124">-位置</span><span class="sxs-lookup"><span data-stu-id="bbce3-124">-Location</span></span>
<span data-ttu-id="bbce3-125">指定防火牆的區域。</span><span class="sxs-lookup"><span data-stu-id="bbce3-125">Specifies the region for the Firewall.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbce3-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="bbce3-126">-Name</span></span>
<span data-ttu-id="bbce3-127">指定此 Cmdlet 所建立之 Azure 防火牆的名稱。</span><span class="sxs-lookup"><span data-stu-id="bbce3-127">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbce3-128">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="bbce3-128">-NatRuleCollection</span></span>
<span data-ttu-id="bbce3-129">AzureFirewallNatRuleCollections 清單</span><span class="sxs-lookup"><span data-stu-id="bbce3-129">The list of AzureFirewallNatRuleCollections</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbce3-130">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="bbce3-130">-NetworkRuleCollection</span></span>
<span data-ttu-id="bbce3-131">AzureFirewallNetworkRuleCollections 清單</span><span class="sxs-lookup"><span data-stu-id="bbce3-131">The list of AzureFirewallNetworkRuleCollections</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbce3-132">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="bbce3-132">-PublicIpName</span></span>
<span data-ttu-id="bbce3-133">公用 Ip 名稱。</span><span class="sxs-lookup"><span data-stu-id="bbce3-133">Public Ip Name.</span></span> <span data-ttu-id="bbce3-134">公用 IP 必須使用標準 SKU，而且必須屬於與防火牆相同的資源群組。</span><span class="sxs-lookup"><span data-stu-id="bbce3-134">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbce3-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbce3-135">-ResourceGroupName</span></span>
<span data-ttu-id="bbce3-136">指定要包含防火牆之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bbce3-136">Specifies the name of a resource group to contain the Firewall.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbce3-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="bbce3-137">-Tag</span></span>
<span data-ttu-id="bbce3-138">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="bbce3-138">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="bbce3-139">例如：</span><span class="sxs-lookup"><span data-stu-id="bbce3-139">For example:</span></span>

<span data-ttu-id="bbce3-140">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="bbce3-140">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbce3-141">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="bbce3-141">-VirtualNetworkName</span></span>
<span data-ttu-id="bbce3-142">指定將部署防火牆的虛擬網路名稱。</span><span class="sxs-lookup"><span data-stu-id="bbce3-142">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="bbce3-143">虛擬網路和防火牆必須屬於相同的資源群組。</span><span class="sxs-lookup"><span data-stu-id="bbce3-143">Virtual network and Firewall must belong to the same resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbce3-144">-確認</span><span class="sxs-lookup"><span data-stu-id="bbce3-144">-Confirm</span></span>
<span data-ttu-id="bbce3-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bbce3-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbce3-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbce3-146">-WhatIf</span></span>
<span data-ttu-id="bbce3-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bbce3-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbce3-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bbce3-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbce3-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbce3-149">CommonParameters</span></span>
<span data-ttu-id="bbce3-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bbce3-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbce3-151">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bbce3-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbce3-152">輸入</span><span class="sxs-lookup"><span data-stu-id="bbce3-152">INPUTS</span></span>

### <span data-ttu-id="bbce3-153">所有</span><span class="sxs-lookup"><span data-stu-id="bbce3-153">None</span></span>
<span data-ttu-id="bbce3-154">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="bbce3-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bbce3-155">輸出</span><span class="sxs-lookup"><span data-stu-id="bbce3-155">OUTPUTS</span></span>

### <span data-ttu-id="bbce3-156">PSFirewall 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="bbce3-156">Microsoft.Azure.Commands.Network.Models.PSFirewall</span></span>

## <span data-ttu-id="bbce3-157">筆記</span><span class="sxs-lookup"><span data-stu-id="bbce3-157">NOTES</span></span>

## <span data-ttu-id="bbce3-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="bbce3-158">RELATED LINKS</span></span>

[<span data-ttu-id="bbce3-159">AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="bbce3-159">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)

[<span data-ttu-id="bbce3-160">移除-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="bbce3-160">Remove-AzureRmFirewall</span></span>](./Remove-AzureRmFirewall.md)

[<span data-ttu-id="bbce3-161">Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="bbce3-161">Set-AzureRmFirewall</span></span>](./Set-AzureRmFirewall.md)

[<span data-ttu-id="bbce3-162">新-AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="bbce3-162">New-AzureRmFirewallApplicationRuleCollection</span></span>](./New-AzureRmFirewallApplicationRuleCollection.md)

[<span data-ttu-id="bbce3-163">新-AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="bbce3-163">New-AzureRmFirewallNatRuleCollection</span></span>](./New-AzureRmFirewallNatRuleCollection.md)

[<span data-ttu-id="bbce3-164">新-AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="bbce3-164">New-AzureRmFirewallNetworkRuleCollection</span></span>](./New-AzureRmFirewallNetworkRuleCollection.md)
