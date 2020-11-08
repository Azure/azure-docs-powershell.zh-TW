---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
ms.openlocfilehash: f6a989a206c6fabf8e64cc82fb07741983f144c5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970349"
---
# <span data-ttu-id="de8f2-101">New-AzFirewallPolicyNatRule</span><span class="sxs-lookup"><span data-stu-id="de8f2-101">New-AzFirewallPolicyNatRule</span></span>

## <span data-ttu-id="de8f2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="de8f2-102">SYNOPSIS</span></span>
<span data-ttu-id="de8f2-103">建立新的 Azure 防火牆原則 NAT 規則</span><span class="sxs-lookup"><span data-stu-id="de8f2-103">Create a new Azure Firewall Policy NAT Rule</span></span>

## <span data-ttu-id="de8f2-104">句法</span><span class="sxs-lookup"><span data-stu-id="de8f2-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> -DestinationPort <String[]>
 -Protocols <String[]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de8f2-105">說明</span><span class="sxs-lookup"><span data-stu-id="de8f2-105">DESCRIPTION</span></span>
<span data-ttu-id="de8f2-106">**新的-AzFirewallPolicyNatRule** Cmdlet 會建立 Azure 防火牆原則的 NAT 規則。</span><span class="sxs-lookup"><span data-stu-id="de8f2-106">The **New-AzFirewallPolicyNatRule** cmdlet creates a NAT rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="de8f2-107">示例</span><span class="sxs-lookup"><span data-stu-id="de8f2-107">EXAMPLES</span></span>

### <span data-ttu-id="de8f2-108">範例1</span><span class="sxs-lookup"><span data-stu-id="de8f2-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRule -Name NatRule1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress 10.20.30.40 -DestinationPort 1000 -TranslatedAddress "192.168.0.1" -TranslatedPort "100"
```

<span data-ttu-id="de8f2-109">這個範例會建立一個 NAT 規則，其中包含來源位址、通訊協定、目的地位址、目的地埠、翻譯位址，以及已翻譯的埠。</span><span class="sxs-lookup"><span data-stu-id="de8f2-109">This example creates a NAT rule with the source address, protocol, destination address, destination port, translated address, and translated port.</span></span>

## <span data-ttu-id="de8f2-110">參數</span><span class="sxs-lookup"><span data-stu-id="de8f2-110">PARAMETERS</span></span>

### <span data-ttu-id="de8f2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de8f2-111">-DefaultProfile</span></span>
<span data-ttu-id="de8f2-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="de8f2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de8f2-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="de8f2-113">-Name</span></span>
<span data-ttu-id="de8f2-114">NAT 規則集合的名稱</span><span class="sxs-lookup"><span data-stu-id="de8f2-114">The name of the NAT Rule Collection</span></span>

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

### <span data-ttu-id="de8f2-115">-描述</span><span class="sxs-lookup"><span data-stu-id="de8f2-115">-Description</span></span>
<span data-ttu-id="de8f2-116">規則的描述</span><span class="sxs-lookup"><span data-stu-id="de8f2-116">The description of the rule</span></span>

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

### <span data-ttu-id="de8f2-117">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="de8f2-117">-DestinationAddress</span></span>
<span data-ttu-id="de8f2-118">規則的目的地位址。</span><span class="sxs-lookup"><span data-stu-id="de8f2-118">The destination addresses of the rule.</span></span> <span data-ttu-id="de8f2-119">這必須是防火牆的公用 IP。</span><span class="sxs-lookup"><span data-stu-id="de8f2-119">This has to be Public IP of the Firewall.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de8f2-120">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="de8f2-120">-DestinationPort</span></span>
<span data-ttu-id="de8f2-121">規則的目的地埠</span><span class="sxs-lookup"><span data-stu-id="de8f2-121">The destination ports of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de8f2-122">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="de8f2-122">-Protocols</span></span>
<span data-ttu-id="de8f2-123">規則的通訊協定</span><span class="sxs-lookup"><span data-stu-id="de8f2-123">The protocols of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: Any, TCP, UDP, ICMP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de8f2-124">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="de8f2-124">-SourceAddress</span></span>
<span data-ttu-id="de8f2-125">規則的來源位址</span><span class="sxs-lookup"><span data-stu-id="de8f2-125">The source addresses of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de8f2-126">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="de8f2-126">-SourceIpGroup</span></span>
<span data-ttu-id="de8f2-127">規則的來源 ipgroups</span><span class="sxs-lookup"><span data-stu-id="de8f2-127">The source ipgroups of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de8f2-128">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="de8f2-128">-TranslatedAddress</span></span>
<span data-ttu-id="de8f2-129">此 NAT 規則的翻譯位址</span><span class="sxs-lookup"><span data-stu-id="de8f2-129">The translated address for this NAT rule</span></span>

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

### <span data-ttu-id="de8f2-130">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="de8f2-130">-TranslatedPort</span></span>
<span data-ttu-id="de8f2-131">此 NAT 規則的已翻譯埠</span><span class="sxs-lookup"><span data-stu-id="de8f2-131">The translated port for this NAT rule</span></span>

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

### <span data-ttu-id="de8f2-132">-確認</span><span class="sxs-lookup"><span data-stu-id="de8f2-132">-Confirm</span></span>
<span data-ttu-id="de8f2-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="de8f2-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de8f2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de8f2-134">-WhatIf</span></span>
<span data-ttu-id="de8f2-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="de8f2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de8f2-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="de8f2-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de8f2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de8f2-137">CommonParameters</span></span>
<span data-ttu-id="de8f2-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="de8f2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de8f2-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="de8f2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de8f2-140">輸入</span><span class="sxs-lookup"><span data-stu-id="de8f2-140">INPUTS</span></span>

### <span data-ttu-id="de8f2-141">所有</span><span class="sxs-lookup"><span data-stu-id="de8f2-141">None</span></span>

## <span data-ttu-id="de8f2-142">輸出</span><span class="sxs-lookup"><span data-stu-id="de8f2-142">OUTPUTS</span></span>

### <span data-ttu-id="de8f2-143">PSAzureFirewallNatRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="de8f2-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="de8f2-144">筆記</span><span class="sxs-lookup"><span data-stu-id="de8f2-144">NOTES</span></span>

## <span data-ttu-id="de8f2-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="de8f2-145">RELATED LINKS</span></span>
