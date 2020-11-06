---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallnatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNatRule.md
ms.openlocfilehash: 0bad5133dd57ec0bee88949fbc9536a6389d6112
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450234"
---
# <span data-ttu-id="24872-101">New-AzureRmFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="24872-101">New-AzureRmFirewallNatRule</span></span>

## <span data-ttu-id="24872-102">摘要</span><span class="sxs-lookup"><span data-stu-id="24872-102">SYNOPSIS</span></span>
<span data-ttu-id="24872-103">建立防火牆 NAT 規則。</span><span class="sxs-lookup"><span data-stu-id="24872-103">Creates a Firewall NAT Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24872-104">句法</span><span class="sxs-lookup"><span data-stu-id="24872-104">SYNTAX</span></span>

```
New-AzureRmFirewallNatRule -Name <String> [-Description <String>]
 -SourceAddress <System.Collections.Generic.List`1[System.String]>
 -DestinationAddress <System.Collections.Generic.List`1[System.String]>
 -DestinationPort <System.Collections.Generic.List`1[System.String]>
 -Protocol <System.Collections.Generic.List`1[System.String]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24872-105">說明</span><span class="sxs-lookup"><span data-stu-id="24872-105">DESCRIPTION</span></span>
<span data-ttu-id="24872-106">**新的-AzureRmFirewallNatRule** Cmdlet 會建立 Azure 防火牆的 NAT 規則。</span><span class="sxs-lookup"><span data-stu-id="24872-106">The **New-AzureRmFirewallNatRule** cmdlet creates a NAT rule for Azure Firewall.</span></span>

## <span data-ttu-id="24872-107">示例</span><span class="sxs-lookup"><span data-stu-id="24872-107">EXAMPLES</span></span>

### <span data-ttu-id="24872-108">1：建立規則以 DNAT 從 10.0.0.0/24 到目的地10.1.2.3：80到 destination 10.4.5.6：8080的所有 TCP 流量</span><span class="sxs-lookup"><span data-stu-id="24872-108">1:  Create a rule to DNAT all TCP traffic from 10.0.0.0/24 with destination 10.1.2.3:80 to destination 10.4.5.6:8080</span></span>
```
New-AzureRmFirewallNatRule -Name "dnat-rule" -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.4.5.6" -TranslatedPort "8080"
```

<span data-ttu-id="24872-109">這個範例會建立一個規則，以 DNAT 所有以 10.0.0.0/24 產生的流量，以及目的地10.1.2.3：80至10.4.5.6：8080</span><span class="sxs-lookup"><span data-stu-id="24872-109">This example creates a rule which will DNAT all traffic originating in 10.0.0.0/24 with destination 10.1.2.3:80 to 10.4.5.6:8080</span></span>

## <span data-ttu-id="24872-110">參數</span><span class="sxs-lookup"><span data-stu-id="24872-110">PARAMETERS</span></span>

### <span data-ttu-id="24872-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24872-111">-DefaultProfile</span></span>
<span data-ttu-id="24872-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="24872-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24872-113">-描述</span><span class="sxs-lookup"><span data-stu-id="24872-113">-Description</span></span>
<span data-ttu-id="24872-114">指定此規則的選擇性描述。</span><span class="sxs-lookup"><span data-stu-id="24872-114">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="24872-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="24872-115">-DestinationAddress</span></span>
<span data-ttu-id="24872-116">規則的目的地位址。</span><span class="sxs-lookup"><span data-stu-id="24872-116">The destination addresses of the rule.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24872-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="24872-117">-DestinationPort</span></span>
<span data-ttu-id="24872-118">規則的目的地埠</span><span class="sxs-lookup"><span data-stu-id="24872-118">The destination ports of the rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24872-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="24872-119">-Name</span></span>
<span data-ttu-id="24872-120">指定此 NAT 規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="24872-120">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="24872-121">該名稱在規則集合內必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="24872-121">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="24872-122">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="24872-122">-Protocol</span></span>
<span data-ttu-id="24872-123">指定要依據此規則篩選的流量類型。</span><span class="sxs-lookup"><span data-stu-id="24872-123">Specifies the type of traffic to be filtered by this rule.</span></span>
<span data-ttu-id="24872-124">支援的通訊協定為 TCP 和 UDP。</span><span class="sxs-lookup"><span data-stu-id="24872-124">The supported protocols are TCP and UDP.</span></span>
<span data-ttu-id="24872-125">允許使用特殊值 "Any"，這表示它將與 TCP 和 UDP 都相符，但沒有其他通訊協定。</span><span class="sxs-lookup"><span data-stu-id="24872-125">A special value "Any" is allowed, meaning it will match both TCP and UDP, but no other protocols.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:
Accepted values: Any, TCP, UDP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24872-126">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="24872-126">-SourceAddress</span></span>
<span data-ttu-id="24872-127">規則的來源位址</span><span class="sxs-lookup"><span data-stu-id="24872-127">The source addresses of the rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24872-128">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="24872-128">-TranslatedAddress</span></span>
<span data-ttu-id="24872-129">指定所需的位址轉換結果</span><span class="sxs-lookup"><span data-stu-id="24872-129">Specifies the desired result of the address translation</span></span>

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

### <span data-ttu-id="24872-130">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="24872-130">-TranslatedPort</span></span>
<span data-ttu-id="24872-131">指定所需的埠轉譯結果</span><span class="sxs-lookup"><span data-stu-id="24872-131">Specifies the desired result of the port translation</span></span>

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

### <span data-ttu-id="24872-132">-確認</span><span class="sxs-lookup"><span data-stu-id="24872-132">-Confirm</span></span>
<span data-ttu-id="24872-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="24872-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24872-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24872-134">-WhatIf</span></span>
<span data-ttu-id="24872-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="24872-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24872-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24872-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24872-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24872-137">CommonParameters</span></span>
<span data-ttu-id="24872-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="24872-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24872-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="24872-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24872-140">輸入</span><span class="sxs-lookup"><span data-stu-id="24872-140">INPUTS</span></span>

### <span data-ttu-id="24872-141">所有</span><span class="sxs-lookup"><span data-stu-id="24872-141">None</span></span>
<span data-ttu-id="24872-142">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="24872-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="24872-143">輸出</span><span class="sxs-lookup"><span data-stu-id="24872-143">OUTPUTS</span></span>

### <span data-ttu-id="24872-144">PSFirewallNatRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="24872-144">Microsoft.Azure.Commands.Network.Models.PSFirewallNatRule</span></span>

## <span data-ttu-id="24872-145">筆記</span><span class="sxs-lookup"><span data-stu-id="24872-145">NOTES</span></span>

## <span data-ttu-id="24872-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="24872-146">RELATED LINKS</span></span>

[<span data-ttu-id="24872-147">新-AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="24872-147">New-AzureRmFirewallNatRuleCollection</span></span>](./New-AzureRmFirewallNatRuleCollection.md)

[<span data-ttu-id="24872-148">新-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="24872-148">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="24872-149">AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="24872-149">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)
