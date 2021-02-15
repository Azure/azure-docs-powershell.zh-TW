---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRule.md
ms.openlocfilehash: c3cf6ce07ab746806181af917f656d27c6ffbbaa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100131270"
---
# <span data-ttu-id="3d03c-101">New-AzFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3d03c-101">New-AzFirewallNetworkRule</span></span>

## <span data-ttu-id="3d03c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3d03c-102">SYNOPSIS</span></span>
<span data-ttu-id="3d03c-103">建立防火牆網路規則。</span><span class="sxs-lookup"><span data-stu-id="3d03c-103">Creates a Firewall Network Rule.</span></span>

## <span data-ttu-id="3d03c-104">句法</span><span class="sxs-lookup"><span data-stu-id="3d03c-104">SYNTAX</span></span>

```
New-AzFirewallNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] [-DestinationAddress <String[]>] [-DestinationIpGroup <String[]>]
 [-DestinationFqdn <String[]>] -DestinationPort <String[]> -Protocol <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d03c-105">說明</span><span class="sxs-lookup"><span data-stu-id="3d03c-105">DESCRIPTION</span></span>
<span data-ttu-id="3d03c-106">**新的-AzFirewallNetworkRule** Cmdlet 會建立 Azure 防火牆的網路規則。</span><span class="sxs-lookup"><span data-stu-id="3d03c-106">The **New-AzFirewallNetworkRule** cmdlet creates an network rule for Azure Firewall.</span></span>

## <span data-ttu-id="3d03c-107">示例</span><span class="sxs-lookup"><span data-stu-id="3d03c-107">EXAMPLES</span></span>

### <span data-ttu-id="3d03c-108">範例1：建立所有 TCP 流量的規則</span><span class="sxs-lookup"><span data-stu-id="3d03c-108">Example 1: Create a rule for all TCP traffic</span></span>
```powershell
$rule = New-AzFirewallNetworkRule -Name "all-tcp-traffic" -Description "Rule for all TCP traffic" -Protocol TCP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
```

<span data-ttu-id="3d03c-109">這個範例會為所有 TCP 流量建立規則。</span><span class="sxs-lookup"><span data-stu-id="3d03c-109">This example creates a rule for all TCP traffic.</span></span> <span data-ttu-id="3d03c-110">使用者會根據與關聯的規則集合，針對規則允許或拒絕交通。</span><span class="sxs-lookup"><span data-stu-id="3d03c-110">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="3d03c-111">範例2：建立從10.0.0.0 至60.1.5.0：4040的所有 TCP 流量的規則</span><span class="sxs-lookup"><span data-stu-id="3d03c-111">Example 2: Create a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040</span></span>
```powershell
$rule = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
```

<span data-ttu-id="3d03c-112">這個範例會為從10.0.0.0 至60.1.5.0：4040的所有 TCP 流量建立規則。</span><span class="sxs-lookup"><span data-stu-id="3d03c-112">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="3d03c-113">使用者會根據與關聯的規則集合，針對規則允許或拒絕交通。</span><span class="sxs-lookup"><span data-stu-id="3d03c-113">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="3d03c-114">範例3：建立從任何來源到 10.0.0.0/16 的所有 TCP 與 ICMP 流量的規則</span><span class="sxs-lookup"><span data-stu-id="3d03c-114">Example 3: Create a rule for all TCP and ICMP traffic from any source to 10.0.0.0/16</span></span>
```powershell
$rule = New-AzFirewallNetworkRule -Name "tcp-and-icmp-rule" -Description "Rule for all TCP and ICMP traffic from any source to 10.0.0.0/16" -Protocol TCP,ICMP -SourceAddress * -DestinationAddress "10.0.0.0/16" -DestinationPort *
```

<span data-ttu-id="3d03c-115">這個範例會建立從任何來源到 10.0.0.0/16 的所有 TCP 流量的規則。</span><span class="sxs-lookup"><span data-stu-id="3d03c-115">This example creates a rule for all TCP traffic from any source to 10.0.0.0/16.</span></span> <span data-ttu-id="3d03c-116">使用者會根據與關聯的規則集合，針對規則允許或拒絕交通。</span><span class="sxs-lookup"><span data-stu-id="3d03c-116">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

## <span data-ttu-id="3d03c-117">參數</span><span class="sxs-lookup"><span data-stu-id="3d03c-117">PARAMETERS</span></span>

### <span data-ttu-id="3d03c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d03c-118">-DefaultProfile</span></span>
<span data-ttu-id="3d03c-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3d03c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d03c-120">-描述</span><span class="sxs-lookup"><span data-stu-id="3d03c-120">-Description</span></span>
<span data-ttu-id="3d03c-121">指定此規則的選擇性描述。</span><span class="sxs-lookup"><span data-stu-id="3d03c-121">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="3d03c-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="3d03c-122">-DestinationAddress</span></span>
<span data-ttu-id="3d03c-123">規則的目的地位址</span><span class="sxs-lookup"><span data-stu-id="3d03c-123">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="3d03c-124">-DestinationFqdn</span><span class="sxs-lookup"><span data-stu-id="3d03c-124">-DestinationFqdn</span></span>
<span data-ttu-id="3d03c-125">規則的目的地 FQDN</span><span class="sxs-lookup"><span data-stu-id="3d03c-125">The destination FQDN of the rule</span></span>

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

### <span data-ttu-id="3d03c-126">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="3d03c-126">-DestinationIpGroup</span></span>
<span data-ttu-id="3d03c-127">規則的目的地 ipgroup</span><span class="sxs-lookup"><span data-stu-id="3d03c-127">The destination ipgroup of the rule</span></span>

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

### <span data-ttu-id="3d03c-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="3d03c-128">-DestinationPort</span></span>
<span data-ttu-id="3d03c-129">規則的目的地埠</span><span class="sxs-lookup"><span data-stu-id="3d03c-129">The destination ports of the rule</span></span>

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

### <span data-ttu-id="3d03c-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="3d03c-130">-Name</span></span>
<span data-ttu-id="3d03c-131">指定此網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d03c-131">Specifies the name of this network rule.</span></span> <span data-ttu-id="3d03c-132">該名稱在規則集合內必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="3d03c-132">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="3d03c-133">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="3d03c-133">-Protocol</span></span>
<span data-ttu-id="3d03c-134">指定要依據此規則篩選的流量類型。</span><span class="sxs-lookup"><span data-stu-id="3d03c-134">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="3d03c-135">可能的值包括 TCP、UDP、ICMP 和 Any。</span><span class="sxs-lookup"><span data-stu-id="3d03c-135">Possible values are TCP, UDP, ICMP and Any.</span></span>

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

### <span data-ttu-id="3d03c-136">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="3d03c-136">-SourceAddress</span></span>
<span data-ttu-id="3d03c-137">規則的來源位址</span><span class="sxs-lookup"><span data-stu-id="3d03c-137">The source addresses of the rule</span></span>

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

### <span data-ttu-id="3d03c-138">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="3d03c-138">-SourceIpGroup</span></span>
<span data-ttu-id="3d03c-139">規則的來源 ipgroup</span><span class="sxs-lookup"><span data-stu-id="3d03c-139">The source ipgroup of the rule</span></span>

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

### <span data-ttu-id="3d03c-140">-確認</span><span class="sxs-lookup"><span data-stu-id="3d03c-140">-Confirm</span></span>
<span data-ttu-id="3d03c-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3d03c-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d03c-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d03c-142">-WhatIf</span></span>
<span data-ttu-id="3d03c-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3d03c-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d03c-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3d03c-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d03c-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d03c-145">CommonParameters</span></span>
<span data-ttu-id="3d03c-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3d03c-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d03c-147">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3d03c-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d03c-148">輸入</span><span class="sxs-lookup"><span data-stu-id="3d03c-148">INPUTS</span></span>

### <span data-ttu-id="3d03c-149">所有</span><span class="sxs-lookup"><span data-stu-id="3d03c-149">None</span></span>

## <span data-ttu-id="3d03c-150">輸出</span><span class="sxs-lookup"><span data-stu-id="3d03c-150">OUTPUTS</span></span>

### <span data-ttu-id="3d03c-151">PSAzureFirewallNetworkRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3d03c-151">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="3d03c-152">筆記</span><span class="sxs-lookup"><span data-stu-id="3d03c-152">NOTES</span></span>

## <span data-ttu-id="3d03c-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="3d03c-153">RELATED LINKS</span></span>

[<span data-ttu-id="3d03c-154">新-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="3d03c-154">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)

[<span data-ttu-id="3d03c-155">新-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="3d03c-155">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="3d03c-156">AzFirewall</span><span class="sxs-lookup"><span data-stu-id="3d03c-156">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
