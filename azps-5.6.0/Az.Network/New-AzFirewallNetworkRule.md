---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRule.md
ms.openlocfilehash: 7b2c78793f5a5e5ae6de8c67ffc214ed5c9b9076
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910033"
---
# <span data-ttu-id="b61a3-101">New-AzFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b61a3-101">New-AzFirewallNetworkRule</span></span>

## <span data-ttu-id="b61a3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b61a3-102">SYNOPSIS</span></span>
<span data-ttu-id="b61a3-103">建立防火牆網路規則。</span><span class="sxs-lookup"><span data-stu-id="b61a3-103">Creates a Firewall Network Rule.</span></span>

## <span data-ttu-id="b61a3-104">語法</span><span class="sxs-lookup"><span data-stu-id="b61a3-104">SYNTAX</span></span>

```
New-AzFirewallNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] [-DestinationAddress <String[]>] [-DestinationIpGroup <String[]>]
 [-DestinationFqdn <String[]>] -DestinationPort <String[]> -Protocol <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b61a3-105">描述</span><span class="sxs-lookup"><span data-stu-id="b61a3-105">DESCRIPTION</span></span>
<span data-ttu-id="b61a3-106">**New-AzFirewallNetworkRule** Cmdlet 會建立 Azure 防火牆的網路規則。</span><span class="sxs-lookup"><span data-stu-id="b61a3-106">The **New-AzFirewallNetworkRule** cmdlet creates an network rule for Azure Firewall.</span></span>

## <span data-ttu-id="b61a3-107">例子</span><span class="sxs-lookup"><span data-stu-id="b61a3-107">EXAMPLES</span></span>

### <span data-ttu-id="b61a3-108">範例 1：建立所有 TCP 流量的規則</span><span class="sxs-lookup"><span data-stu-id="b61a3-108">Example 1: Create a rule for all TCP traffic</span></span>
```powershell
$rule = New-AzFirewallNetworkRule -Name "all-tcp-traffic" -Description "Rule for all TCP traffic" -Protocol TCP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
```

<span data-ttu-id="b61a3-109">此範例會建立所有 TCP 流量的規則。</span><span class="sxs-lookup"><span data-stu-id="b61a3-109">This example creates a rule for all TCP traffic.</span></span> <span data-ttu-id="b61a3-110">使用者根據與規則關聯的規則集合，強制執行規則是否允許或拒絕流量。</span><span class="sxs-lookup"><span data-stu-id="b61a3-110">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="b61a3-111">範例 2：針對從 10.0.0.0 到 60.1.5.0：4040 的所有 TCP 流量建立規則</span><span class="sxs-lookup"><span data-stu-id="b61a3-111">Example 2: Create a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040</span></span>
```powershell
$rule = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
```

<span data-ttu-id="b61a3-112">此範例會針對從 10.0.0.0 到 60.1.5.0：4040 的所有 TCP 流量建立規則。</span><span class="sxs-lookup"><span data-stu-id="b61a3-112">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="b61a3-113">使用者根據與規則關聯的規則集合，強制執行規則是否允許或拒絕流量。</span><span class="sxs-lookup"><span data-stu-id="b61a3-113">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="b61a3-114">範例 3：針對從任何來源到 10.0.0.0/16 的所有 TCP 和 ICMP 流量建立規則</span><span class="sxs-lookup"><span data-stu-id="b61a3-114">Example 3: Create a rule for all TCP and ICMP traffic from any source to 10.0.0.0/16</span></span>
```powershell
$rule = New-AzFirewallNetworkRule -Name "tcp-and-icmp-rule" -Description "Rule for all TCP and ICMP traffic from any source to 10.0.0.0/16" -Protocol TCP,ICMP -SourceAddress * -DestinationAddress "10.0.0.0/16" -DestinationPort *
```

<span data-ttu-id="b61a3-115">此範例會針對從任何來源到 10.0.0.0/16 的所有 TCP 流量建立規則。</span><span class="sxs-lookup"><span data-stu-id="b61a3-115">This example creates a rule for all TCP traffic from any source to 10.0.0.0/16.</span></span> <span data-ttu-id="b61a3-116">使用者根據與規則關聯的規則集合，強制執行規則是否允許或拒絕流量。</span><span class="sxs-lookup"><span data-stu-id="b61a3-116">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

## <span data-ttu-id="b61a3-117">參數</span><span class="sxs-lookup"><span data-stu-id="b61a3-117">PARAMETERS</span></span>

### <span data-ttu-id="b61a3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b61a3-118">-DefaultProfile</span></span>
<span data-ttu-id="b61a3-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b61a3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b61a3-120">-描述</span><span class="sxs-lookup"><span data-stu-id="b61a3-120">-Description</span></span>
<span data-ttu-id="b61a3-121">指定此規則的選擇性描述。</span><span class="sxs-lookup"><span data-stu-id="b61a3-121">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="b61a3-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="b61a3-122">-DestinationAddress</span></span>
<span data-ttu-id="b61a3-123">規則的目的地位址</span><span class="sxs-lookup"><span data-stu-id="b61a3-123">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="b61a3-124">-DestinationFqdn</span><span class="sxs-lookup"><span data-stu-id="b61a3-124">-DestinationFqdn</span></span>
<span data-ttu-id="b61a3-125">規則的目標 FQDN</span><span class="sxs-lookup"><span data-stu-id="b61a3-125">The destination FQDN of the rule</span></span>

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

### <span data-ttu-id="b61a3-126">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="b61a3-126">-DestinationIpGroup</span></span>
<span data-ttu-id="b61a3-127">規則的目標 ipgroup</span><span class="sxs-lookup"><span data-stu-id="b61a3-127">The destination ipgroup of the rule</span></span>

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

### <span data-ttu-id="b61a3-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="b61a3-128">-DestinationPort</span></span>
<span data-ttu-id="b61a3-129">規則的目標埠</span><span class="sxs-lookup"><span data-stu-id="b61a3-129">The destination ports of the rule</span></span>

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

### <span data-ttu-id="b61a3-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="b61a3-130">-Name</span></span>
<span data-ttu-id="b61a3-131">指定此網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="b61a3-131">Specifies the name of this network rule.</span></span> <span data-ttu-id="b61a3-132">名稱必須在規則集合中是唯一的。</span><span class="sxs-lookup"><span data-stu-id="b61a3-132">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="b61a3-133">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="b61a3-133">-Protocol</span></span>
<span data-ttu-id="b61a3-134">指定此規則要篩選的流量類型。</span><span class="sxs-lookup"><span data-stu-id="b61a3-134">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="b61a3-135">可能的值為 TCP、UDP、ICMP 和 Any。</span><span class="sxs-lookup"><span data-stu-id="b61a3-135">Possible values are TCP, UDP, ICMP and Any.</span></span>

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

### <span data-ttu-id="b61a3-136">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="b61a3-136">-SourceAddress</span></span>
<span data-ttu-id="b61a3-137">規則的來源位址</span><span class="sxs-lookup"><span data-stu-id="b61a3-137">The source addresses of the rule</span></span>

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

### <span data-ttu-id="b61a3-138">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="b61a3-138">-SourceIpGroup</span></span>
<span data-ttu-id="b61a3-139">規則的來源 ipgroup</span><span class="sxs-lookup"><span data-stu-id="b61a3-139">The source ipgroup of the rule</span></span>

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

### <span data-ttu-id="b61a3-140">-確認</span><span class="sxs-lookup"><span data-stu-id="b61a3-140">-Confirm</span></span>
<span data-ttu-id="b61a3-141">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b61a3-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b61a3-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b61a3-142">-WhatIf</span></span>
<span data-ttu-id="b61a3-143">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b61a3-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b61a3-144">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b61a3-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b61a3-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b61a3-145">CommonParameters</span></span>
<span data-ttu-id="b61a3-146">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b61a3-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b61a3-147">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="b61a3-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b61a3-148">輸入</span><span class="sxs-lookup"><span data-stu-id="b61a3-148">INPUTS</span></span>

### <span data-ttu-id="b61a3-149">沒有</span><span class="sxs-lookup"><span data-stu-id="b61a3-149">None</span></span>

## <span data-ttu-id="b61a3-150">輸出</span><span class="sxs-lookup"><span data-stu-id="b61a3-150">OUTPUTS</span></span>

### <span data-ttu-id="b61a3-151">Microsoft.Azure.Commands.Network.models.PSAzureFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b61a3-151">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="b61a3-152">筆記</span><span class="sxs-lookup"><span data-stu-id="b61a3-152">NOTES</span></span>

## <span data-ttu-id="b61a3-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="b61a3-153">RELATED LINKS</span></span>

[<span data-ttu-id="b61a3-154">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="b61a3-154">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)

[<span data-ttu-id="b61a3-155">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b61a3-155">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="b61a3-156">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b61a3-156">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
