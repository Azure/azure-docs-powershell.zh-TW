---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNetworkRule.md
ms.openlocfilehash: 1100e42934c493bf8aea30e7372acc683b46b60b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447347"
---
# <span data-ttu-id="a893f-101">New-AzureRmFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a893f-101">New-AzureRmFirewallNetworkRule</span></span>

## <span data-ttu-id="a893f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a893f-102">SYNOPSIS</span></span>
<span data-ttu-id="a893f-103">建立防火牆網路規則。</span><span class="sxs-lookup"><span data-stu-id="a893f-103">Creates a Firewall Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a893f-104">句法</span><span class="sxs-lookup"><span data-stu-id="a893f-104">SYNTAX</span></span>

```
New-AzureRmFirewallNetworkRule -Name <String> [-Description <String>]
 -SourceAddress <System.Collections.Generic.List`1[System.String]>
 -DestinationAddress <System.Collections.Generic.List`1[System.String]>
 -DestinationPort <System.Collections.Generic.List`1[System.String]>
 -Protocol <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a893f-105">說明</span><span class="sxs-lookup"><span data-stu-id="a893f-105">DESCRIPTION</span></span>
<span data-ttu-id="a893f-106">**新的-AzureRmFirewallNetworkRule** Cmdlet 會建立 Azure 防火牆的網路規則。</span><span class="sxs-lookup"><span data-stu-id="a893f-106">The **New-AzureRmFirewallNetworkRule** cmdlet creates an network rule for Azure Firewall.</span></span>

## <span data-ttu-id="a893f-107">示例</span><span class="sxs-lookup"><span data-stu-id="a893f-107">EXAMPLES</span></span>

### <span data-ttu-id="a893f-108">1：建立所有 TCP 流量的規則</span><span class="sxs-lookup"><span data-stu-id="a893f-108">1:  Create a rule for all TCP traffic</span></span>
```
$rule = New-AzureRmFirewallNetworkRule -Name "all-tcp-traffic" -Description "Rule for all TCP traffic" -Protocol TCP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
```

<span data-ttu-id="a893f-109">這個範例會為所有 TCP 流量建立規則。</span><span class="sxs-lookup"><span data-stu-id="a893f-109">This example creates a rule for all TCP traffic.</span></span> <span data-ttu-id="a893f-110">使用者會根據與關聯的規則集合，針對規則允許或拒絕交通。</span><span class="sxs-lookup"><span data-stu-id="a893f-110">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="a893f-111">2：為從10.0.0.0 至60.1.5.0：4040的所有 TCP 流量建立規則。</span><span class="sxs-lookup"><span data-stu-id="a893f-111">2:  Create a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040</span></span>
```
$rule = New-AzureRmFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
```

<span data-ttu-id="a893f-112">這個範例會為從10.0.0.0 至60.1.5.0：4040的所有 TCP 流量建立規則。</span><span class="sxs-lookup"><span data-stu-id="a893f-112">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="a893f-113">使用者會根據與關聯的規則集合，針對規則允許或拒絕交通。</span><span class="sxs-lookup"><span data-stu-id="a893f-113">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="a893f-114">3：建立從任何來源到 10.0.0.0/16 的所有 TCP 與 ICMP 流量的規則</span><span class="sxs-lookup"><span data-stu-id="a893f-114">3: Create a rule for all TCP and ICMP traffic from any source to 10.0.0.0/16</span></span>
```
$rule = New-AzureRmFirewallNetworkRule -Name "tcp-and-icmp-rule" -Description "Rule for all TCP and ICMP traffic from any source to 10.0.0.0/16" -Protocol TCP,ICMP -SourceAddress * -DestinationAddress "10.0.0.0/16" -DestinationPort *
```

<span data-ttu-id="a893f-115">這個範例會為從10.0.0.0 至60.1.5.0：4040的所有 TCP 流量建立規則。</span><span class="sxs-lookup"><span data-stu-id="a893f-115">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="a893f-116">使用者會根據與關聯的規則集合，針對規則允許或拒絕交通。</span><span class="sxs-lookup"><span data-stu-id="a893f-116">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

## <span data-ttu-id="a893f-117">參數</span><span class="sxs-lookup"><span data-stu-id="a893f-117">PARAMETERS</span></span>

### <span data-ttu-id="a893f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a893f-118">-DefaultProfile</span></span>
<span data-ttu-id="a893f-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a893f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a893f-120">-描述</span><span class="sxs-lookup"><span data-stu-id="a893f-120">-Description</span></span>
<span data-ttu-id="a893f-121">指定此規則的選擇性描述。</span><span class="sxs-lookup"><span data-stu-id="a893f-121">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="a893f-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="a893f-122">-DestinationAddress</span></span>
<span data-ttu-id="a893f-123">規則的目的地位址</span><span class="sxs-lookup"><span data-stu-id="a893f-123">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="a893f-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="a893f-124">-DestinationPort</span></span>
<span data-ttu-id="a893f-125">規則的目的地埠</span><span class="sxs-lookup"><span data-stu-id="a893f-125">The destination ports of the rule</span></span>

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

### <span data-ttu-id="a893f-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="a893f-126">-Name</span></span>
<span data-ttu-id="a893f-127">指定此網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="a893f-127">Specifies the name of this network rule.</span></span> <span data-ttu-id="a893f-128">該名稱在規則集合內必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="a893f-128">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="a893f-129">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="a893f-129">-Protocol</span></span>
<span data-ttu-id="a893f-130">指定要依據此規則篩選的流量類型。</span><span class="sxs-lookup"><span data-stu-id="a893f-130">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="a893f-131">可能的值包括 TCP、UDP、ICMP 和 Any。</span><span class="sxs-lookup"><span data-stu-id="a893f-131">Possible values are TCP, UDP, ICMP and Any.</span></span>

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

### <span data-ttu-id="a893f-132">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="a893f-132">-SourceAddress</span></span>
<span data-ttu-id="a893f-133">規則的來源位址</span><span class="sxs-lookup"><span data-stu-id="a893f-133">The source addresses of the rule</span></span>

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

### <span data-ttu-id="a893f-134">-確認</span><span class="sxs-lookup"><span data-stu-id="a893f-134">-Confirm</span></span>
<span data-ttu-id="a893f-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a893f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a893f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a893f-136">-WhatIf</span></span>
<span data-ttu-id="a893f-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a893f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a893f-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a893f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a893f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a893f-139">CommonParameters</span></span>
<span data-ttu-id="a893f-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a893f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a893f-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a893f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a893f-142">輸入</span><span class="sxs-lookup"><span data-stu-id="a893f-142">INPUTS</span></span>

### <span data-ttu-id="a893f-143">所有</span><span class="sxs-lookup"><span data-stu-id="a893f-143">None</span></span>
<span data-ttu-id="a893f-144">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="a893f-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a893f-145">輸出</span><span class="sxs-lookup"><span data-stu-id="a893f-145">OUTPUTS</span></span>

### <span data-ttu-id="a893f-146">PSFirewallNetworkRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a893f-146">Microsoft.Azure.Commands.Network.Models.PSFirewallNetworkRule</span></span>

## <span data-ttu-id="a893f-147">筆記</span><span class="sxs-lookup"><span data-stu-id="a893f-147">NOTES</span></span>

## <span data-ttu-id="a893f-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="a893f-148">RELATED LINKS</span></span>

[<span data-ttu-id="a893f-149">新-AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="a893f-149">New-AzureRmFirewallNetworkRuleCollection</span></span>](./New-AzureRmFirewallNetworkRuleCollection.md)

[<span data-ttu-id="a893f-150">新-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="a893f-150">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="a893f-151">AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="a893f-151">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)
