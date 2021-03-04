---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallnatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRule.md
ms.openlocfilehash: 2bbac9bebd79f1ca51a7defd4c57589764b2c34e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910422"
---
# <span data-ttu-id="a6b31-101">New-AzFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="a6b31-101">New-AzFirewallNatRule</span></span>

## <span data-ttu-id="a6b31-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a6b31-102">SYNOPSIS</span></span>
<span data-ttu-id="a6b31-103">建立防火牆 NAT 規則。</span><span class="sxs-lookup"><span data-stu-id="a6b31-103">Creates a Firewall NAT Rule.</span></span>

## <span data-ttu-id="a6b31-104">語法</span><span class="sxs-lookup"><span data-stu-id="a6b31-104">SYNTAX</span></span>

```
New-AzFirewallNatRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]>
 [-TranslatedAddress <String>] [-TranslatedFqdn <String>] -TranslatedPort <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6b31-105">描述</span><span class="sxs-lookup"><span data-stu-id="a6b31-105">DESCRIPTION</span></span>
<span data-ttu-id="a6b31-106">**New-AzFirewallNatRule** Cmdlet 會建立 Azure 防火牆的 NAT 規則。</span><span class="sxs-lookup"><span data-stu-id="a6b31-106">The **New-AzFirewallNatRule** cmdlet creates a NAT rule for Azure Firewall.</span></span>

## <span data-ttu-id="a6b31-107">例子</span><span class="sxs-lookup"><span data-stu-id="a6b31-107">EXAMPLES</span></span>

### <span data-ttu-id="a6b31-108">範例 1：建立規則給所有 TCP 流量從 10.0.0.0/24 到目的地 10.1.2.3：80 到目的地 10.4.5.6：8080</span><span class="sxs-lookup"><span data-stu-id="a6b31-108">Example 1: Create a rule to DNAT all TCP traffic from 10.0.0.0/24 with destination 10.1.2.3:80 to destination 10.4.5.6:8080</span></span>
```powershell
New-AzFirewallNatRule -Name "dnat-rule" -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.4.5.6" -TranslatedPort "8080"
```

<span data-ttu-id="a6b31-109">此範例會建立規則，讓所有來自 10.0.0.0/24 的流量，目的地為 10.1.2.3：80 到 10.4.5.6：8080</span><span class="sxs-lookup"><span data-stu-id="a6b31-109">This example creates a rule which will DNAT all traffic originating in 10.0.0.0/24 with destination 10.1.2.3:80 to 10.4.5.6:8080</span></span>

## <span data-ttu-id="a6b31-110">參數</span><span class="sxs-lookup"><span data-stu-id="a6b31-110">PARAMETERS</span></span>

### <span data-ttu-id="a6b31-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6b31-111">-DefaultProfile</span></span>
<span data-ttu-id="a6b31-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a6b31-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6b31-113">-描述</span><span class="sxs-lookup"><span data-stu-id="a6b31-113">-Description</span></span>
<span data-ttu-id="a6b31-114">指定此規則的選擇性描述。</span><span class="sxs-lookup"><span data-stu-id="a6b31-114">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="a6b31-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="a6b31-115">-DestinationAddress</span></span>
<span data-ttu-id="a6b31-116">規則的目的地位址</span><span class="sxs-lookup"><span data-stu-id="a6b31-116">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="a6b31-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="a6b31-117">-DestinationPort</span></span>
<span data-ttu-id="a6b31-118">規則的目標埠</span><span class="sxs-lookup"><span data-stu-id="a6b31-118">The destination ports of the rule</span></span>

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

### <span data-ttu-id="a6b31-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="a6b31-119">-Name</span></span>
<span data-ttu-id="a6b31-120">指定此 NAT 規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="a6b31-120">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="a6b31-121">名稱必須在規則集合中是唯一的。</span><span class="sxs-lookup"><span data-stu-id="a6b31-121">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="a6b31-122">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="a6b31-122">-Protocol</span></span>
<span data-ttu-id="a6b31-123">指定此規則要篩選的流量類型。</span><span class="sxs-lookup"><span data-stu-id="a6b31-123">Specifies the type of traffic to be filtered by this rule.</span></span>
<span data-ttu-id="a6b31-124">支援的通訊協定為 TCP 和 UDP。</span><span class="sxs-lookup"><span data-stu-id="a6b31-124">The supported protocols are TCP and UDP.</span></span>
<span data-ttu-id="a6b31-125">允許特殊值 「Any」，表示它會同時符合 TCP 和 UDP，但無法比對其他通訊協定。</span><span class="sxs-lookup"><span data-stu-id="a6b31-125">A special value "Any" is allowed, meaning it will match both TCP and UDP, but no other protocols.</span></span>

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

### <span data-ttu-id="a6b31-126">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="a6b31-126">-SourceAddress</span></span>
<span data-ttu-id="a6b31-127">規則的來源位址</span><span class="sxs-lookup"><span data-stu-id="a6b31-127">The source addresses of the rule</span></span>

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

### <span data-ttu-id="a6b31-128">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="a6b31-128">-SourceIpGroup</span></span>
<span data-ttu-id="a6b31-129">規則的來源 ipgroup</span><span class="sxs-lookup"><span data-stu-id="a6b31-129">The source ipgroup of the rule</span></span>

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

### <span data-ttu-id="a6b31-130">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="a6b31-130">-TranslatedAddress</span></span>
<span data-ttu-id="a6b31-131">指定位址翻譯所需的結果</span><span class="sxs-lookup"><span data-stu-id="a6b31-131">Specifies the desired result of the address translation</span></span>

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

### <span data-ttu-id="a6b31-132">-TranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="a6b31-132">-TranslatedFqdn</span></span>
<span data-ttu-id="a6b31-133">此 NAT 規則的翻譯 FQDN</span><span class="sxs-lookup"><span data-stu-id="a6b31-133">The translated FQDN for this NAT rule</span></span>

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

### <span data-ttu-id="a6b31-134">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="a6b31-134">-TranslatedPort</span></span>
<span data-ttu-id="a6b31-135">指定埠翻譯的所需結果</span><span class="sxs-lookup"><span data-stu-id="a6b31-135">Specifies the desired result of the port translation</span></span>

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

### <span data-ttu-id="a6b31-136">-確認</span><span class="sxs-lookup"><span data-stu-id="a6b31-136">-Confirm</span></span>
<span data-ttu-id="a6b31-137">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a6b31-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6b31-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6b31-138">-WhatIf</span></span>
<span data-ttu-id="a6b31-139">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a6b31-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6b31-140">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a6b31-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6b31-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6b31-141">CommonParameters</span></span>
<span data-ttu-id="a6b31-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a6b31-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6b31-143">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a6b31-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6b31-144">輸入</span><span class="sxs-lookup"><span data-stu-id="a6b31-144">INPUTS</span></span>

### <span data-ttu-id="a6b31-145">沒有</span><span class="sxs-lookup"><span data-stu-id="a6b31-145">None</span></span>

## <span data-ttu-id="a6b31-146">輸出</span><span class="sxs-lookup"><span data-stu-id="a6b31-146">OUTPUTS</span></span>

### <span data-ttu-id="a6b31-147">Microsoft.Azure.Commands.Network.models.PSAzureFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="a6b31-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="a6b31-148">筆記</span><span class="sxs-lookup"><span data-stu-id="a6b31-148">NOTES</span></span>

## <span data-ttu-id="a6b31-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="a6b31-149">RELATED LINKS</span></span>

[<span data-ttu-id="a6b31-150">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="a6b31-150">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="a6b31-151">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="a6b31-151">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="a6b31-152">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="a6b31-152">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
