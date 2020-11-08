---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRule.md
ms.openlocfilehash: c3cf6ce07ab746806181af917f656d27c6ffbbaa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136292"
---
# <span data-ttu-id="0620b-101">New-AzFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="0620b-101">New-AzFirewallNetworkRule</span></span>

## <span data-ttu-id="0620b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0620b-102">SYNOPSIS</span></span>
<span data-ttu-id="0620b-103">建立防火牆網路規則。</span><span class="sxs-lookup"><span data-stu-id="0620b-103">Creates a Firewall Network Rule.</span></span>

## <span data-ttu-id="0620b-104">句法</span><span class="sxs-lookup"><span data-stu-id="0620b-104">SYNTAX</span></span>

```
New-AzFirewallNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] [-DestinationAddress <String[]>] [-DestinationIpGroup <String[]>]
 [-DestinationFqdn <String[]>] -DestinationPort <String[]> -Protocol <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0620b-105">說明</span><span class="sxs-lookup"><span data-stu-id="0620b-105">DESCRIPTION</span></span>
<span data-ttu-id="0620b-106">**新的-AzFirewallNetworkRule** Cmdlet 會建立 Azure 防火牆的網路規則。</span><span class="sxs-lookup"><span data-stu-id="0620b-106">The **New-AzFirewallNetworkRule** cmdlet creates an network rule for Azure Firewall.</span></span>

## <span data-ttu-id="0620b-107">示例</span><span class="sxs-lookup"><span data-stu-id="0620b-107">EXAMPLES</span></span>

### <span data-ttu-id="0620b-108">範例1：建立所有 TCP 流量的規則</span><span class="sxs-lookup"><span data-stu-id="0620b-108">Example 1: Create a rule for all TCP traffic</span></span>
```powershell
$rule = New-AzFirewallNetworkRule -Name "all-tcp-traffic" -Description "Rule for all TCP traffic" -Protocol TCP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
```

<span data-ttu-id="0620b-109">這個範例會為所有 TCP 流量建立規則。</span><span class="sxs-lookup"><span data-stu-id="0620b-109">This example creates a rule for all TCP traffic.</span></span> <span data-ttu-id="0620b-110">使用者會根據與關聯的規則集合，針對規則允許或拒絕交通。</span><span class="sxs-lookup"><span data-stu-id="0620b-110">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="0620b-111">範例2：建立從10.0.0.0 至60.1.5.0：4040的所有 TCP 流量的規則</span><span class="sxs-lookup"><span data-stu-id="0620b-111">Example 2: Create a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040</span></span>
```powershell
$rule = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
```

<span data-ttu-id="0620b-112">這個範例會為從10.0.0.0 至60.1.5.0：4040的所有 TCP 流量建立規則。</span><span class="sxs-lookup"><span data-stu-id="0620b-112">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="0620b-113">使用者會根據與關聯的規則集合，針對規則允許或拒絕交通。</span><span class="sxs-lookup"><span data-stu-id="0620b-113">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="0620b-114">範例3：建立從任何來源到 10.0.0.0/16 的所有 TCP 與 ICMP 流量的規則</span><span class="sxs-lookup"><span data-stu-id="0620b-114">Example 3: Create a rule for all TCP and ICMP traffic from any source to 10.0.0.0/16</span></span>
```powershell
$rule = New-AzFirewallNetworkRule -Name "tcp-and-icmp-rule" -Description "Rule for all TCP and ICMP traffic from any source to 10.0.0.0/16" -Protocol TCP,ICMP -SourceAddress * -DestinationAddress "10.0.0.0/16" -DestinationPort *
```

<span data-ttu-id="0620b-115">這個範例會建立從任何來源到 10.0.0.0/16 的所有 TCP 流量的規則。</span><span class="sxs-lookup"><span data-stu-id="0620b-115">This example creates a rule for all TCP traffic from any source to 10.0.0.0/16.</span></span> <span data-ttu-id="0620b-116">使用者會根據與關聯的規則集合，針對規則允許或拒絕交通。</span><span class="sxs-lookup"><span data-stu-id="0620b-116">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

## <span data-ttu-id="0620b-117">參數</span><span class="sxs-lookup"><span data-stu-id="0620b-117">PARAMETERS</span></span>

### <span data-ttu-id="0620b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0620b-118">-DefaultProfile</span></span>
<span data-ttu-id="0620b-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0620b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0620b-120">-描述</span><span class="sxs-lookup"><span data-stu-id="0620b-120">-Description</span></span>
<span data-ttu-id="0620b-121">指定此規則的選擇性描述。</span><span class="sxs-lookup"><span data-stu-id="0620b-121">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="0620b-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="0620b-122">-DestinationAddress</span></span>
<span data-ttu-id="0620b-123">規則的目的地位址</span><span class="sxs-lookup"><span data-stu-id="0620b-123">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="0620b-124">-DestinationFqdn</span><span class="sxs-lookup"><span data-stu-id="0620b-124">-DestinationFqdn</span></span>
<span data-ttu-id="0620b-125">規則的目的地 FQDN</span><span class="sxs-lookup"><span data-stu-id="0620b-125">The destination FQDN of the rule</span></span>

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

### <span data-ttu-id="0620b-126">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="0620b-126">-DestinationIpGroup</span></span>
<span data-ttu-id="0620b-127">規則的目的地 ipgroup</span><span class="sxs-lookup"><span data-stu-id="0620b-127">The destination ipgroup of the rule</span></span>

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

### <span data-ttu-id="0620b-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="0620b-128">-DestinationPort</span></span>
<span data-ttu-id="0620b-129">規則的目的地埠</span><span class="sxs-lookup"><span data-stu-id="0620b-129">The destination ports of the rule</span></span>

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

### <span data-ttu-id="0620b-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="0620b-130">-Name</span></span>
<span data-ttu-id="0620b-131">指定此網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="0620b-131">Specifies the name of this network rule.</span></span> <span data-ttu-id="0620b-132">該名稱在規則集合內必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="0620b-132">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="0620b-133">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="0620b-133">-Protocol</span></span>
<span data-ttu-id="0620b-134">指定要依據此規則篩選的流量類型。</span><span class="sxs-lookup"><span data-stu-id="0620b-134">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="0620b-135">可能的值包括 TCP、UDP、ICMP 和 Any。</span><span class="sxs-lookup"><span data-stu-id="0620b-135">Possible values are TCP, UDP, ICMP and Any.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Any, TCP, UDP, ICMP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0620b-136">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="0620b-136">-SourceAddress</span></span>
<span data-ttu-id="0620b-137">規則的來源位址</span><span class="sxs-lookup"><span data-stu-id="0620b-137">The source addresses of the rule</span></span>

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

### <span data-ttu-id="0620b-138">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="0620b-138">-SourceIpGroup</span></span>
<span data-ttu-id="0620b-139">規則的來源 ipgroup</span><span class="sxs-lookup"><span data-stu-id="0620b-139">The source ipgroup of the rule</span></span>

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

### <span data-ttu-id="0620b-140">-確認</span><span class="sxs-lookup"><span data-stu-id="0620b-140">-Confirm</span></span>
<span data-ttu-id="0620b-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0620b-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0620b-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0620b-142">-WhatIf</span></span>
<span data-ttu-id="0620b-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0620b-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0620b-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0620b-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0620b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0620b-145">CommonParameters</span></span>
<span data-ttu-id="0620b-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0620b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0620b-147">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0620b-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0620b-148">輸入</span><span class="sxs-lookup"><span data-stu-id="0620b-148">INPUTS</span></span>

### <span data-ttu-id="0620b-149">所有</span><span class="sxs-lookup"><span data-stu-id="0620b-149">None</span></span>

## <span data-ttu-id="0620b-150">輸出</span><span class="sxs-lookup"><span data-stu-id="0620b-150">OUTPUTS</span></span>

### <span data-ttu-id="0620b-151">PSAzureFirewallNetworkRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0620b-151">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="0620b-152">筆記</span><span class="sxs-lookup"><span data-stu-id="0620b-152">NOTES</span></span>

## <span data-ttu-id="0620b-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="0620b-153">RELATED LINKS</span></span>

[<span data-ttu-id="0620b-154">新-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="0620b-154">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)

[<span data-ttu-id="0620b-155">新-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="0620b-155">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="0620b-156">AzFirewall</span><span class="sxs-lookup"><span data-stu-id="0620b-156">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
