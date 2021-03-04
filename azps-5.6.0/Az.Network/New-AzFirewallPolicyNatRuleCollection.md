---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicynatrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRuleCollection.md
ms.openlocfilehash: 4dd93dec5aad6fe0e77e92e44884c687d5841e49
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904025"
---
# <span data-ttu-id="15fcb-101">New-AzFirewallPolicyNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="15fcb-101">New-AzFirewallPolicyNatRuleCollection</span></span>

## <span data-ttu-id="15fcb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="15fcb-102">SYNOPSIS</span></span>
<span data-ttu-id="15fcb-103">建立新的 Azure 防火牆原則 Nat 規則集合</span><span class="sxs-lookup"><span data-stu-id="15fcb-103">Create a new Azure Firewall Policy Nat Rule Collection</span></span>

## <span data-ttu-id="15fcb-104">語法</span><span class="sxs-lookup"><span data-stu-id="15fcb-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNatRuleCollection -Name <String> -Priority <UInt32>
 -Rule <PSAzureFirewallPolicyNetworkRule> -ActionType <String> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15fcb-105">描述</span><span class="sxs-lookup"><span data-stu-id="15fcb-105">DESCRIPTION</span></span>
<span data-ttu-id="15fcb-106">**New-AzFirewallPolicyNatRuleCollection** Cmdlet 會為 Azure 防火牆原則建立 Nat 規則集合。</span><span class="sxs-lookup"><span data-stu-id="15fcb-106">The **New-AzFirewallPolicyNatRuleCollection** cmdlet creates a Nat rule collection for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="15fcb-107">例子</span><span class="sxs-lookup"><span data-stu-id="15fcb-107">EXAMPLES</span></span>

### <span data-ttu-id="15fcb-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="15fcb-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRuleCollection -Name NatRule1 -Priority 200 -Rule $netRule1 -ActionType "Dnat" -TranslatedAddress "192.168.0.1" -TranslatedPort "100"
```

<span data-ttu-id="15fcb-109">此範例會使用網路規則建立 nat 規則集合</span><span class="sxs-lookup"><span data-stu-id="15fcb-109">This example creates a nat rule collection with a network rule</span></span>

## <span data-ttu-id="15fcb-110">參數</span><span class="sxs-lookup"><span data-stu-id="15fcb-110">PARAMETERS</span></span>

### <span data-ttu-id="15fcb-111">-ActionType</span><span class="sxs-lookup"><span data-stu-id="15fcb-111">-ActionType</span></span>
<span data-ttu-id="15fcb-112">規則動作的類型</span><span class="sxs-lookup"><span data-stu-id="15fcb-112">The type of the rule action</span></span>

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

### <span data-ttu-id="15fcb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15fcb-113">-DefaultProfile</span></span>
<span data-ttu-id="15fcb-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="15fcb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15fcb-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="15fcb-115">-Name</span></span>
<span data-ttu-id="15fcb-116">網路規則集合的名稱</span><span class="sxs-lookup"><span data-stu-id="15fcb-116">The name of the Network Rule Collection</span></span>

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

### <span data-ttu-id="15fcb-117">-優先順序</span><span class="sxs-lookup"><span data-stu-id="15fcb-117">-Priority</span></span>
<span data-ttu-id="15fcb-118">規則集合的優先順序</span><span class="sxs-lookup"><span data-stu-id="15fcb-118">The priority of the rule collection</span></span>

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

### <span data-ttu-id="15fcb-119">-規則</span><span class="sxs-lookup"><span data-stu-id="15fcb-119">-Rule</span></span>
<span data-ttu-id="15fcb-120">網路規則清單</span><span class="sxs-lookup"><span data-stu-id="15fcb-120">The list of network rules</span></span>

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

### <span data-ttu-id="15fcb-121">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="15fcb-121">-TranslatedAddress</span></span>
<span data-ttu-id="15fcb-122">此 NAT 規則的翻譯位址</span><span class="sxs-lookup"><span data-stu-id="15fcb-122">The translated address for this NAT rule</span></span>

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

### <span data-ttu-id="15fcb-123">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="15fcb-123">-TranslatedPort</span></span>
<span data-ttu-id="15fcb-124">此 NAT 規則的翻譯埠</span><span class="sxs-lookup"><span data-stu-id="15fcb-124">The translated port for this NAT rule</span></span>

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

### <span data-ttu-id="15fcb-125">-確認</span><span class="sxs-lookup"><span data-stu-id="15fcb-125">-Confirm</span></span>
<span data-ttu-id="15fcb-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="15fcb-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15fcb-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15fcb-127">-WhatIf</span></span>
<span data-ttu-id="15fcb-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="15fcb-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15fcb-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="15fcb-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15fcb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15fcb-130">CommonParameters</span></span>
<span data-ttu-id="15fcb-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="15fcb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15fcb-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="15fcb-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15fcb-133">輸入</span><span class="sxs-lookup"><span data-stu-id="15fcb-133">INPUTS</span></span>

### <span data-ttu-id="15fcb-134">沒有</span><span class="sxs-lookup"><span data-stu-id="15fcb-134">None</span></span>

## <span data-ttu-id="15fcb-135">輸出</span><span class="sxs-lookup"><span data-stu-id="15fcb-135">OUTPUTS</span></span>

### <span data-ttu-id="15fcb-136">Microsoft.Azure.Commands.Network.models.PSAzureFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="15fcb-136">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="15fcb-137">筆記</span><span class="sxs-lookup"><span data-stu-id="15fcb-137">NOTES</span></span>

## <span data-ttu-id="15fcb-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="15fcb-138">RELATED LINKS</span></span>
