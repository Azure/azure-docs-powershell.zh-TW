---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRule.md
ms.openlocfilehash: c7519b6cf5f95f80a20f94bbae5ec097964bd01a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789365"
---
# <span data-ttu-id="a5d51-101">New-AzFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="a5d51-101">New-AzFirewallNatRule</span></span>

## <span data-ttu-id="a5d51-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a5d51-102">SYNOPSIS</span></span>
<span data-ttu-id="a5d51-103">建立防火牆 NAT 規則。</span><span class="sxs-lookup"><span data-stu-id="a5d51-103">Creates a Firewall NAT Rule.</span></span>

## <span data-ttu-id="a5d51-104">句法</span><span class="sxs-lookup"><span data-stu-id="a5d51-104">SYNTAX</span></span>

```
New-AzFirewallNatRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5d51-105">說明</span><span class="sxs-lookup"><span data-stu-id="a5d51-105">DESCRIPTION</span></span>
<span data-ttu-id="a5d51-106">**新的-AzFirewallNatRule** Cmdlet 會建立 Azure 防火牆的 NAT 規則。</span><span class="sxs-lookup"><span data-stu-id="a5d51-106">The **New-AzFirewallNatRule** cmdlet creates a NAT rule for Azure Firewall.</span></span>

## <span data-ttu-id="a5d51-107">示例</span><span class="sxs-lookup"><span data-stu-id="a5d51-107">EXAMPLES</span></span>

### <span data-ttu-id="a5d51-108">1：建立規則以 DNAT 從 10.0.0.0/24 到目的地10.1.2.3：80到 destination 10.4.5.6：8080的所有 TCP 流量</span><span class="sxs-lookup"><span data-stu-id="a5d51-108">1:  Create a rule to DNAT all TCP traffic from 10.0.0.0/24 with destination 10.1.2.3:80 to destination 10.4.5.6:8080</span></span>
```
New-AzFirewallNatRule -Name "dnat-rule" -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.4.5.6" -TranslatedPort "8080"
```

<span data-ttu-id="a5d51-109">這個範例會建立一個規則，以 DNAT 所有以 10.0.0.0/24 產生的流量，以及目的地10.1.2.3：80至10.4.5.6：8080</span><span class="sxs-lookup"><span data-stu-id="a5d51-109">This example creates a rule which will DNAT all traffic originating in 10.0.0.0/24 with destination 10.1.2.3:80 to 10.4.5.6:8080</span></span>

## <span data-ttu-id="a5d51-110">參數</span><span class="sxs-lookup"><span data-stu-id="a5d51-110">PARAMETERS</span></span>

### <span data-ttu-id="a5d51-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5d51-111">-DefaultProfile</span></span>
<span data-ttu-id="a5d51-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a5d51-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5d51-113">-描述</span><span class="sxs-lookup"><span data-stu-id="a5d51-113">-Description</span></span>
<span data-ttu-id="a5d51-114">指定此規則的選擇性描述。</span><span class="sxs-lookup"><span data-stu-id="a5d51-114">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="a5d51-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="a5d51-115">-DestinationAddress</span></span>
<span data-ttu-id="a5d51-116">規則的目的地位址。</span><span class="sxs-lookup"><span data-stu-id="a5d51-116">The destination addresses of the rule.</span></span>

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

### <span data-ttu-id="a5d51-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="a5d51-117">-DestinationPort</span></span>
<span data-ttu-id="a5d51-118">規則的目的地埠</span><span class="sxs-lookup"><span data-stu-id="a5d51-118">The destination ports of the rule</span></span>

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

### <span data-ttu-id="a5d51-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="a5d51-119">-Name</span></span>
<span data-ttu-id="a5d51-120">指定此 NAT 規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="a5d51-120">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="a5d51-121">該名稱在規則集合內必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="a5d51-121">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="a5d51-122">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="a5d51-122">-Protocol</span></span>
<span data-ttu-id="a5d51-123">指定要依據此規則篩選的流量類型。</span><span class="sxs-lookup"><span data-stu-id="a5d51-123">Specifies the type of traffic to be filtered by this rule.</span></span>
<span data-ttu-id="a5d51-124">支援的通訊協定為 TCP 和 UDP。</span><span class="sxs-lookup"><span data-stu-id="a5d51-124">The supported protocols are TCP and UDP.</span></span>
<span data-ttu-id="a5d51-125">允許使用特殊值 "Any"，這表示它將與 TCP 和 UDP 都相符，但沒有其他通訊協定。</span><span class="sxs-lookup"><span data-stu-id="a5d51-125">A special value "Any" is allowed, meaning it will match both TCP and UDP, but no other protocols.</span></span>

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

### <span data-ttu-id="a5d51-126">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="a5d51-126">-SourceAddress</span></span>
<span data-ttu-id="a5d51-127">規則的來源位址</span><span class="sxs-lookup"><span data-stu-id="a5d51-127">The source addresses of the rule</span></span>

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

### <span data-ttu-id="a5d51-128">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="a5d51-128">-TranslatedAddress</span></span>
<span data-ttu-id="a5d51-129">指定所需的位址轉換結果</span><span class="sxs-lookup"><span data-stu-id="a5d51-129">Specifies the desired result of the address translation</span></span>

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

### <span data-ttu-id="a5d51-130">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="a5d51-130">-TranslatedPort</span></span>
<span data-ttu-id="a5d51-131">指定所需的埠轉譯結果</span><span class="sxs-lookup"><span data-stu-id="a5d51-131">Specifies the desired result of the port translation</span></span>

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

### <span data-ttu-id="a5d51-132">-確認</span><span class="sxs-lookup"><span data-stu-id="a5d51-132">-Confirm</span></span>
<span data-ttu-id="a5d51-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a5d51-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5d51-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5d51-134">-WhatIf</span></span>
<span data-ttu-id="a5d51-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a5d51-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5d51-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a5d51-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5d51-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5d51-137">CommonParameters</span></span>
<span data-ttu-id="a5d51-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a5d51-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5d51-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a5d51-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5d51-140">輸入</span><span class="sxs-lookup"><span data-stu-id="a5d51-140">INPUTS</span></span>

### <span data-ttu-id="a5d51-141">所有</span><span class="sxs-lookup"><span data-stu-id="a5d51-141">None</span></span>

## <span data-ttu-id="a5d51-142">輸出</span><span class="sxs-lookup"><span data-stu-id="a5d51-142">OUTPUTS</span></span>

### <span data-ttu-id="a5d51-143">PSAzureFirewallNatRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a5d51-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="a5d51-144">筆記</span><span class="sxs-lookup"><span data-stu-id="a5d51-144">NOTES</span></span>

## <span data-ttu-id="a5d51-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="a5d51-145">RELATED LINKS</span></span>

[<span data-ttu-id="a5d51-146">新-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="a5d51-146">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="a5d51-147">新-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="a5d51-147">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="a5d51-148">AzFirewall</span><span class="sxs-lookup"><span data-stu-id="a5d51-148">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
