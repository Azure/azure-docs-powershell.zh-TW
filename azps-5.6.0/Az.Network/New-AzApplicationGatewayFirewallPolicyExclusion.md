---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallpolicyexclusion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyExclusion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyExclusion.md
ms.openlocfilehash: 04cf39f9c0d8774ffb02688e4edf5804029df669
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907621"
---
# <span data-ttu-id="4d72c-101">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="4d72c-101">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>

## <span data-ttu-id="4d72c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4d72c-102">SYNOPSIS</span></span>
<span data-ttu-id="4d72c-103">在防火牆政策上建立排除專案</span><span class="sxs-lookup"><span data-stu-id="4d72c-103">Creates an exclusion on the Firewall Policy</span></span>

## <span data-ttu-id="4d72c-104">語法</span><span class="sxs-lookup"><span data-stu-id="4d72c-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyExclusion -MatchVariable <String> -SelectorMatchOperator <String>
 -Selector <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d72c-105">描述</span><span class="sxs-lookup"><span data-stu-id="4d72c-105">DESCRIPTION</span></span>
<span data-ttu-id="4d72c-106">**New-AzApplicationGatewayFirewallPolicyExclusion** Cmdlet 防火牆原則的新排除規則清單。</span><span class="sxs-lookup"><span data-stu-id="4d72c-106">The **New-AzApplicationGatewayFirewallPolicyExclusion** cmdlet a new exclusion rule list for firewall policy.</span></span>

## <span data-ttu-id="4d72c-107">例子</span><span class="sxs-lookup"><span data-stu-id="4d72c-107">EXAMPLES</span></span>

### <span data-ttu-id="4d72c-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="4d72c-108">Example 1</span></span>
```powershell
PS C:\> $exclusionEntry = New-AzApplicationGatewayFirewallPolicyExclusion -MatchVariable "RequestHeaderNames" -SelectorMatchOperator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="4d72c-109">此命令會為名為 RequestHeaderNames 的變數和名為 StartsWith 和選擇器名為 xyz 的運算子建立一個新的排除專案。</span><span class="sxs-lookup"><span data-stu-id="4d72c-109">This command creates a new exclusion-entry for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="4d72c-110">排除專案會儲存于$exclusionEntry。</span><span class="sxs-lookup"><span data-stu-id="4d72c-110">The exclusion entry is saved in $exclusionEntry.</span></span>

## <span data-ttu-id="4d72c-111">參數</span><span class="sxs-lookup"><span data-stu-id="4d72c-111">PARAMETERS</span></span>

### <span data-ttu-id="4d72c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d72c-112">-DefaultProfile</span></span>
<span data-ttu-id="4d72c-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4d72c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d72c-114">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="4d72c-114">-MatchVariable</span></span>
<span data-ttu-id="4d72c-115">要排除的變數。</span><span class="sxs-lookup"><span data-stu-id="4d72c-115">The variable to be excluded.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RequestHeaderNames, RequestCookieNames, RequestArgNames

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d72c-116">-選取器</span><span class="sxs-lookup"><span data-stu-id="4d72c-116">-Selector</span></span>
<span data-ttu-id="4d72c-117">當變數是集合時，運算子會用來指定此排除範圍適用于集合中的哪些元素。</span><span class="sxs-lookup"><span data-stu-id="4d72c-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="4d72c-118">-選擇器MatchOperator</span><span class="sxs-lookup"><span data-stu-id="4d72c-118">-SelectorMatchOperator</span></span>
<span data-ttu-id="4d72c-119">當變數是集合時，請于選取器上操作，以指定此排除專案適用于集合中的哪些元素。</span><span class="sxs-lookup"><span data-stu-id="4d72c-119">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Equals, Contains, StartsWith, EndsWith, EqualsAny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d72c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d72c-120">CommonParameters</span></span>
<span data-ttu-id="4d72c-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4d72c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d72c-122">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4d72c-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d72c-123">輸入</span><span class="sxs-lookup"><span data-stu-id="4d72c-123">INPUTS</span></span>

### <span data-ttu-id="4d72c-124">沒有</span><span class="sxs-lookup"><span data-stu-id="4d72c-124">None</span></span>

## <span data-ttu-id="4d72c-125">輸出</span><span class="sxs-lookup"><span data-stu-id="4d72c-125">OUTPUTS</span></span>

### <span data-ttu-id="4d72c-126">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="4d72c-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyExclusion</span></span>

## <span data-ttu-id="4d72c-127">筆記</span><span class="sxs-lookup"><span data-stu-id="4d72c-127">NOTES</span></span>

## <span data-ttu-id="4d72c-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="4d72c-128">RELATED LINKS</span></span>
