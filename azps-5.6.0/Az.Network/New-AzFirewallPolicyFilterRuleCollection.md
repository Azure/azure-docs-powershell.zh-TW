---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicyfilterrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyFilterRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyFilterRuleCollection.md
ms.openlocfilehash: 3bdd96bfe85d6b78476e16a49b2700131ae5aca9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904598"
---
# <span data-ttu-id="9f8ed-101">New-AzFirewallPolicyFilterRuleCollection</span><span class="sxs-lookup"><span data-stu-id="9f8ed-101">New-AzFirewallPolicyFilterRuleCollection</span></span>

## <span data-ttu-id="9f8ed-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9f8ed-102">SYNOPSIS</span></span>
<span data-ttu-id="9f8ed-103">建立新 Azure 防火牆原則篩選規則集合</span><span class="sxs-lookup"><span data-stu-id="9f8ed-103">Create a new Azure Firewall Policy Filter Rule Collection</span></span>

## <span data-ttu-id="9f8ed-104">語法</span><span class="sxs-lookup"><span data-stu-id="9f8ed-104">SYNTAX</span></span>

```
New-AzFirewallPolicyFilterRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallPolicyRule[]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f8ed-105">描述</span><span class="sxs-lookup"><span data-stu-id="9f8ed-105">DESCRIPTION</span></span>
<span data-ttu-id="9f8ed-106">**New-AzFirewallPolicyFilterRuleCollection** Cmdlet 會建立 Azure 防火牆原則的篩選規則集合。</span><span class="sxs-lookup"><span data-stu-id="9f8ed-106">The **New-AzFirewallPolicyFilterRuleCollection** cmdlet creates a Filter rule collection for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="9f8ed-107">例子</span><span class="sxs-lookup"><span data-stu-id="9f8ed-107">EXAMPLES</span></span>

### <span data-ttu-id="9f8ed-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="9f8ed-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyFilterRuleCollection -Name FR1 -Priority 400 -Rule $appRule1 ,$appRule2 -ActionType "Allow"
```

<span data-ttu-id="9f8ed-109">此範例會建立具有 2 個規則條件的篩選規則</span><span class="sxs-lookup"><span data-stu-id="9f8ed-109">This example creates a Filter rule with 2 rule conditions</span></span>

## <span data-ttu-id="9f8ed-110">參數</span><span class="sxs-lookup"><span data-stu-id="9f8ed-110">PARAMETERS</span></span>

### <span data-ttu-id="9f8ed-111">-ActionType</span><span class="sxs-lookup"><span data-stu-id="9f8ed-111">-ActionType</span></span>
<span data-ttu-id="9f8ed-112">規則集合的動作</span><span class="sxs-lookup"><span data-stu-id="9f8ed-112">The action of the rule collection</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f8ed-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f8ed-113">-DefaultProfile</span></span>
<span data-ttu-id="9f8ed-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9f8ed-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f8ed-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="9f8ed-115">-Name</span></span>
<span data-ttu-id="9f8ed-116">應用程式規則集合的名稱</span><span class="sxs-lookup"><span data-stu-id="9f8ed-116">The name of the Application Rule Collection</span></span>

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

### <span data-ttu-id="9f8ed-117">-優先順序</span><span class="sxs-lookup"><span data-stu-id="9f8ed-117">-Priority</span></span>
<span data-ttu-id="9f8ed-118">規則集合的優先順序</span><span class="sxs-lookup"><span data-stu-id="9f8ed-118">The priority of the rule collection</span></span>

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

### <span data-ttu-id="9f8ed-119">-規則</span><span class="sxs-lookup"><span data-stu-id="9f8ed-119">-Rule</span></span>
<span data-ttu-id="9f8ed-120">應用程式規則清單</span><span class="sxs-lookup"><span data-stu-id="9f8ed-120">The list of application rules</span></span>

```yaml
Type: PSAzureFirewallPolicyRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f8ed-121">-確認</span><span class="sxs-lookup"><span data-stu-id="9f8ed-121">-Confirm</span></span>
<span data-ttu-id="9f8ed-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9f8ed-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f8ed-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f8ed-123">-WhatIf</span></span>
<span data-ttu-id="9f8ed-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9f8ed-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f8ed-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9f8ed-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f8ed-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f8ed-126">CommonParameters</span></span>
<span data-ttu-id="9f8ed-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9f8ed-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f8ed-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9f8ed-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f8ed-129">輸入</span><span class="sxs-lookup"><span data-stu-id="9f8ed-129">INPUTS</span></span>

### <span data-ttu-id="9f8ed-130">沒有</span><span class="sxs-lookup"><span data-stu-id="9f8ed-130">None</span></span>

## <span data-ttu-id="9f8ed-131">輸出</span><span class="sxs-lookup"><span data-stu-id="9f8ed-131">OUTPUTS</span></span>

### <span data-ttu-id="9f8ed-132">Microsoft.Azure.Commands.Network.models.PSAzureFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="9f8ed-132">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="9f8ed-133">筆記</span><span class="sxs-lookup"><span data-stu-id="9f8ed-133">NOTES</span></span>

## <span data-ttu-id="9f8ed-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="9f8ed-134">RELATED LINKS</span></span>
