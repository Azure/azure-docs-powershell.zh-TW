---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynatrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRuleCollection.md
ms.openlocfilehash: 010fd83d8b8e26e67e35afcc54b03ca0c1a5bd5a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138721"
---
# <span data-ttu-id="008e7-101">New-AzFirewallPolicyNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="008e7-101">New-AzFirewallPolicyNatRuleCollection</span></span>

## <span data-ttu-id="008e7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="008e7-102">SYNOPSIS</span></span>
<span data-ttu-id="008e7-103">建立新的 Azure 防火牆原則 Nat 規則集合</span><span class="sxs-lookup"><span data-stu-id="008e7-103">Create a new Azure Firewall Policy Nat Rule Collection</span></span>

## <span data-ttu-id="008e7-104">句法</span><span class="sxs-lookup"><span data-stu-id="008e7-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNatRuleCollection -Name <String> -Priority <UInt32>
 -Rule <PSAzureFirewallPolicyNetworkRule> -ActionType <String> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="008e7-105">說明</span><span class="sxs-lookup"><span data-stu-id="008e7-105">DESCRIPTION</span></span>
<span data-ttu-id="008e7-106">**新的-AzFirewallPolicyNatRuleCollection** Cmdlet 會針對 Azure 防火牆原則建立 Nat 規則集合。</span><span class="sxs-lookup"><span data-stu-id="008e7-106">The **New-AzFirewallPolicyNatRuleCollection** cmdlet creates a Nat rule collection for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="008e7-107">示例</span><span class="sxs-lookup"><span data-stu-id="008e7-107">EXAMPLES</span></span>

### <span data-ttu-id="008e7-108">範例1</span><span class="sxs-lookup"><span data-stu-id="008e7-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRuleCollection -Name NatRule1 -Priority 200 -Rule $netRule1 -ActionType "Dnat" -TranslatedAddress "192.168.0.1" -TranslatedPort "100"
```

<span data-ttu-id="008e7-109">這個範例會建立含網路規則的 nat 規則集合</span><span class="sxs-lookup"><span data-stu-id="008e7-109">This example creates a nat rule collection with a network rule</span></span>

## <span data-ttu-id="008e7-110">參數</span><span class="sxs-lookup"><span data-stu-id="008e7-110">PARAMETERS</span></span>

### <span data-ttu-id="008e7-111">-ActionType</span><span class="sxs-lookup"><span data-stu-id="008e7-111">-ActionType</span></span>
<span data-ttu-id="008e7-112">規則動作的類型</span><span class="sxs-lookup"><span data-stu-id="008e7-112">The type of the rule action</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Dnat

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="008e7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="008e7-113">-DefaultProfile</span></span>
<span data-ttu-id="008e7-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="008e7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="008e7-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="008e7-115">-Name</span></span>
<span data-ttu-id="008e7-116">網路規則集合的名稱</span><span class="sxs-lookup"><span data-stu-id="008e7-116">The name of the Network Rule Collection</span></span>

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

### <span data-ttu-id="008e7-117">-優先順序</span><span class="sxs-lookup"><span data-stu-id="008e7-117">-Priority</span></span>
<span data-ttu-id="008e7-118">規則集合的優先順序</span><span class="sxs-lookup"><span data-stu-id="008e7-118">The priority of the rule collection</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="008e7-119">-規則</span><span class="sxs-lookup"><span data-stu-id="008e7-119">-Rule</span></span>
<span data-ttu-id="008e7-120">網路規則清單</span><span class="sxs-lookup"><span data-stu-id="008e7-120">The list of network rules</span></span>

```yaml
Type: PSAzureFirewallPolicyNetworkRule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="008e7-121">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="008e7-121">-TranslatedAddress</span></span>
<span data-ttu-id="008e7-122">此 NAT 規則的翻譯位址</span><span class="sxs-lookup"><span data-stu-id="008e7-122">The translated address for this NAT rule</span></span>

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

### <span data-ttu-id="008e7-123">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="008e7-123">-TranslatedPort</span></span>
<span data-ttu-id="008e7-124">此 NAT 規則的已翻譯埠</span><span class="sxs-lookup"><span data-stu-id="008e7-124">The translated port for this NAT rule</span></span>

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

### <span data-ttu-id="008e7-125">-確認</span><span class="sxs-lookup"><span data-stu-id="008e7-125">-Confirm</span></span>
<span data-ttu-id="008e7-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="008e7-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="008e7-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="008e7-127">-WhatIf</span></span>
<span data-ttu-id="008e7-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="008e7-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="008e7-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="008e7-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="008e7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="008e7-130">CommonParameters</span></span>
<span data-ttu-id="008e7-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="008e7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="008e7-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="008e7-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="008e7-133">輸入</span><span class="sxs-lookup"><span data-stu-id="008e7-133">INPUTS</span></span>

### <span data-ttu-id="008e7-134">所有</span><span class="sxs-lookup"><span data-stu-id="008e7-134">None</span></span>

## <span data-ttu-id="008e7-135">輸出</span><span class="sxs-lookup"><span data-stu-id="008e7-135">OUTPUTS</span></span>

### <span data-ttu-id="008e7-136">PSAzureFirewallNetworkRuleCollection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="008e7-136">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="008e7-137">筆記</span><span class="sxs-lookup"><span data-stu-id="008e7-137">NOTES</span></span>

## <span data-ttu-id="008e7-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="008e7-138">RELATED LINKS</span></span>