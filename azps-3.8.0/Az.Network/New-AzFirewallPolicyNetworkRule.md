---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
ms.openlocfilehash: b4cbc404139cd56e75f03c5cb19cb9b761576e39
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957759"
---
# <span data-ttu-id="687e4-101">New-AzFirewallPolicyNetworkRule</span><span class="sxs-lookup"><span data-stu-id="687e4-101">New-AzFirewallPolicyNetworkRule</span></span>

## <span data-ttu-id="687e4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="687e4-102">SYNOPSIS</span></span>
<span data-ttu-id="687e4-103">建立新的 Azure 防火牆原則網路規則</span><span class="sxs-lookup"><span data-stu-id="687e4-103">Create a new Azure Firewall Policy Network Rule</span></span>

## <span data-ttu-id="687e4-104">句法</span><span class="sxs-lookup"><span data-stu-id="687e4-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocols <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="687e4-105">說明</span><span class="sxs-lookup"><span data-stu-id="687e4-105">DESCRIPTION</span></span>
<span data-ttu-id="687e4-106">**新的-AzFirewallPolicyNetworkRule** Cmdlet 會建立 Azure 防火牆原則的網路規則。</span><span class="sxs-lookup"><span data-stu-id="687e4-106">The **New-AzFirewallPolicyNetworkRule** cmdlet creates a Network rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="687e4-107">示例</span><span class="sxs-lookup"><span data-stu-id="687e4-107">EXAMPLES</span></span>

### <span data-ttu-id="687e4-108">範例1</span><span class="sxs-lookup"><span data-stu-id="687e4-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNetworkRule -Name NRC1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress * -DestinationPort *
```

<span data-ttu-id="687e4-109">這個範例會建立一個含有來源位址、通訊協定、目的地位址及目的地埠的網路規則</span><span class="sxs-lookup"><span data-stu-id="687e4-109">This example creates an network rule with the source address, protocol , destination address and destination port</span></span>

## <span data-ttu-id="687e4-110">參數</span><span class="sxs-lookup"><span data-stu-id="687e4-110">PARAMETERS</span></span>

### <span data-ttu-id="687e4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="687e4-111">-DefaultProfile</span></span>
<span data-ttu-id="687e4-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="687e4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="687e4-113">-描述</span><span class="sxs-lookup"><span data-stu-id="687e4-113">-Description</span></span>
<span data-ttu-id="687e4-114">規則的描述</span><span class="sxs-lookup"><span data-stu-id="687e4-114">The description of the rule</span></span>

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

### <span data-ttu-id="687e4-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="687e4-115">-DestinationAddress</span></span>
<span data-ttu-id="687e4-116">規則的目的地位址</span><span class="sxs-lookup"><span data-stu-id="687e4-116">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="687e4-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="687e4-117">-DestinationPort</span></span>
<span data-ttu-id="687e4-118">規則的目的地埠</span><span class="sxs-lookup"><span data-stu-id="687e4-118">The destination ports of the rule</span></span>

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

### <span data-ttu-id="687e4-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="687e4-119">-Name</span></span>
<span data-ttu-id="687e4-120">網路規則的名稱</span><span class="sxs-lookup"><span data-stu-id="687e4-120">The name of the Network Rule</span></span>

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

### <span data-ttu-id="687e4-121">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="687e4-121">-Protocols</span></span>
<span data-ttu-id="687e4-122">規則的通訊協定</span><span class="sxs-lookup"><span data-stu-id="687e4-122">The protocols of the rule</span></span>

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

### <span data-ttu-id="687e4-123">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="687e4-123">-SourceAddress</span></span>
<span data-ttu-id="687e4-124">規則的來源位址</span><span class="sxs-lookup"><span data-stu-id="687e4-124">The source addresses of the rule</span></span>

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

### <span data-ttu-id="687e4-125">-確認</span><span class="sxs-lookup"><span data-stu-id="687e4-125">-Confirm</span></span>
<span data-ttu-id="687e4-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="687e4-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="687e4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="687e4-127">-WhatIf</span></span>
<span data-ttu-id="687e4-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="687e4-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="687e4-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="687e4-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="687e4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="687e4-130">CommonParameters</span></span>
<span data-ttu-id="687e4-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="687e4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="687e4-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="687e4-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="687e4-133">輸入</span><span class="sxs-lookup"><span data-stu-id="687e4-133">INPUTS</span></span>

### <span data-ttu-id="687e4-134">所有</span><span class="sxs-lookup"><span data-stu-id="687e4-134">None</span></span>

## <span data-ttu-id="687e4-135">輸出</span><span class="sxs-lookup"><span data-stu-id="687e4-135">OUTPUTS</span></span>

### <span data-ttu-id="687e4-136">PSAzureFirewallNetworkRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="687e4-136">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="687e4-137">筆記</span><span class="sxs-lookup"><span data-stu-id="687e4-137">NOTES</span></span>

## <span data-ttu-id="687e4-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="687e4-138">RELATED LINKS</span></span>