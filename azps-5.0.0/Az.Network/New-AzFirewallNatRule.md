---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRule.md
ms.openlocfilehash: efe8821ee1ec0978c42aa59fc856b4d6e07fa7dc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139767"
---
# <span data-ttu-id="9d5a6-101">New-AzFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="9d5a6-101">New-AzFirewallNatRule</span></span>

## <span data-ttu-id="9d5a6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9d5a6-102">SYNOPSIS</span></span>
<span data-ttu-id="9d5a6-103">建立防火牆 NAT 規則。</span><span class="sxs-lookup"><span data-stu-id="9d5a6-103">Creates a Firewall NAT Rule.</span></span>

## <span data-ttu-id="9d5a6-104">句法</span><span class="sxs-lookup"><span data-stu-id="9d5a6-104">SYNTAX</span></span>

```
New-AzFirewallNatRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]>
 [-TranslatedAddress <String>] [-TranslatedFqdn <String>] -TranslatedPort <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d5a6-105">說明</span><span class="sxs-lookup"><span data-stu-id="9d5a6-105">DESCRIPTION</span></span>
<span data-ttu-id="9d5a6-106">**新的-AzFirewallNatRule** Cmdlet 會建立 Azure 防火牆的 NAT 規則。</span><span class="sxs-lookup"><span data-stu-id="9d5a6-106">The **New-AzFirewallNatRule** cmdlet creates a NAT rule for Azure Firewall.</span></span>

## <span data-ttu-id="9d5a6-107">示例</span><span class="sxs-lookup"><span data-stu-id="9d5a6-107">EXAMPLES</span></span>

### <span data-ttu-id="9d5a6-108">範例1：建立規則以 DNAT 從 10.0.0.0/24 到目的地10.1.2.3：80到 destination 10.4.5.6：8080的所有 TCP 流量</span><span class="sxs-lookup"><span data-stu-id="9d5a6-108">Example 1: Create a rule to DNAT all TCP traffic from 10.0.0.0/24 with destination 10.1.2.3:80 to destination 10.4.5.6:8080</span></span>
```powershell
New-AzFirewallNatRule -Name "dnat-rule" -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.4.5.6" -TranslatedPort "8080"
```

<span data-ttu-id="9d5a6-109">這個範例會建立一個規則，以 DNAT 所有以 10.0.0.0/24 產生的流量，以及目的地10.1.2.3：80至10.4.5.6：8080</span><span class="sxs-lookup"><span data-stu-id="9d5a6-109">This example creates a rule which will DNAT all traffic originating in 10.0.0.0/24 with destination 10.1.2.3:80 to 10.4.5.6:8080</span></span>

## <span data-ttu-id="9d5a6-110">參數</span><span class="sxs-lookup"><span data-stu-id="9d5a6-110">PARAMETERS</span></span>

### <span data-ttu-id="9d5a6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d5a6-111">-DefaultProfile</span></span>
<span data-ttu-id="9d5a6-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9d5a6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d5a6-113">-描述</span><span class="sxs-lookup"><span data-stu-id="9d5a6-113">-Description</span></span>
<span data-ttu-id="9d5a6-114">指定此規則的選擇性描述。</span><span class="sxs-lookup"><span data-stu-id="9d5a6-114">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="9d5a6-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="9d5a6-115">-DestinationAddress</span></span>
<span data-ttu-id="9d5a6-116">規則的目的地位址</span><span class="sxs-lookup"><span data-stu-id="9d5a6-116">The destination addresses of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d5a6-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="9d5a6-117">-DestinationPort</span></span>
<span data-ttu-id="9d5a6-118">規則的目的地埠</span><span class="sxs-lookup"><span data-stu-id="9d5a6-118">The destination ports of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d5a6-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="9d5a6-119">-Name</span></span>
<span data-ttu-id="9d5a6-120">指定此 NAT 規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="9d5a6-120">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="9d5a6-121">該名稱在規則集合內必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="9d5a6-121">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="9d5a6-122">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="9d5a6-122">-Protocol</span></span>
<span data-ttu-id="9d5a6-123">指定要依據此規則篩選的流量類型。</span><span class="sxs-lookup"><span data-stu-id="9d5a6-123">Specifies the type of traffic to be filtered by this rule.</span></span>
<span data-ttu-id="9d5a6-124">支援的通訊協定為 TCP 和 UDP。</span><span class="sxs-lookup"><span data-stu-id="9d5a6-124">The supported protocols are TCP and UDP.</span></span>
<span data-ttu-id="9d5a6-125">允許使用特殊值 "Any"，這表示它將與 TCP 和 UDP 都相符，但沒有其他通訊協定。</span><span class="sxs-lookup"><span data-stu-id="9d5a6-125">A special value "Any" is allowed, meaning it will match both TCP and UDP, but no other protocols.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Any, TCP, UDP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d5a6-126">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="9d5a6-126">-SourceAddress</span></span>
<span data-ttu-id="9d5a6-127">規則的來源位址</span><span class="sxs-lookup"><span data-stu-id="9d5a6-127">The source addresses of the rule</span></span>

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

### <span data-ttu-id="9d5a6-128">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="9d5a6-128">-SourceIpGroup</span></span>
<span data-ttu-id="9d5a6-129">規則的來源 ipgroup</span><span class="sxs-lookup"><span data-stu-id="9d5a6-129">The source ipgroup of the rule</span></span>

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

### <span data-ttu-id="9d5a6-130">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="9d5a6-130">-TranslatedAddress</span></span>
<span data-ttu-id="9d5a6-131">指定所需的位址轉換結果</span><span class="sxs-lookup"><span data-stu-id="9d5a6-131">Specifies the desired result of the address translation</span></span>

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

### <span data-ttu-id="9d5a6-132">-TranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="9d5a6-132">-TranslatedFqdn</span></span>
<span data-ttu-id="9d5a6-133">此 NAT 規則的已翻譯的 FQDN</span><span class="sxs-lookup"><span data-stu-id="9d5a6-133">The translated FQDN for this NAT rule</span></span>

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

### <span data-ttu-id="9d5a6-134">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="9d5a6-134">-TranslatedPort</span></span>
<span data-ttu-id="9d5a6-135">指定所需的埠轉譯結果</span><span class="sxs-lookup"><span data-stu-id="9d5a6-135">Specifies the desired result of the port translation</span></span>

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

### <span data-ttu-id="9d5a6-136">-確認</span><span class="sxs-lookup"><span data-stu-id="9d5a6-136">-Confirm</span></span>
<span data-ttu-id="9d5a6-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9d5a6-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d5a6-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d5a6-138">-WhatIf</span></span>
<span data-ttu-id="9d5a6-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9d5a6-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d5a6-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9d5a6-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d5a6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d5a6-141">CommonParameters</span></span>
<span data-ttu-id="9d5a6-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9d5a6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d5a6-143">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9d5a6-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d5a6-144">輸入</span><span class="sxs-lookup"><span data-stu-id="9d5a6-144">INPUTS</span></span>

### <span data-ttu-id="9d5a6-145">所有</span><span class="sxs-lookup"><span data-stu-id="9d5a6-145">None</span></span>

## <span data-ttu-id="9d5a6-146">輸出</span><span class="sxs-lookup"><span data-stu-id="9d5a6-146">OUTPUTS</span></span>

### <span data-ttu-id="9d5a6-147">PSAzureFirewallNatRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9d5a6-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="9d5a6-148">筆記</span><span class="sxs-lookup"><span data-stu-id="9d5a6-148">NOTES</span></span>

## <span data-ttu-id="9d5a6-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="9d5a6-149">RELATED LINKS</span></span>

[<span data-ttu-id="9d5a6-150">新-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="9d5a6-150">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="9d5a6-151">新-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="9d5a6-151">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="9d5a6-152">AzFirewall</span><span class="sxs-lookup"><span data-stu-id="9d5a6-152">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
