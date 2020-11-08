---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicyexclusion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyExclusion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyExclusion.md
ms.openlocfilehash: e5ad76625a171e1fd12fc583c6ad8acf593ed817
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94135841"
---
# <span data-ttu-id="4163c-101">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="4163c-101">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>

## <span data-ttu-id="4163c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4163c-102">SYNOPSIS</span></span>
<span data-ttu-id="4163c-103">在防火牆原則上建立排除</span><span class="sxs-lookup"><span data-stu-id="4163c-103">Creates an exclusion on the Firewall Policy</span></span>

## <span data-ttu-id="4163c-104">句法</span><span class="sxs-lookup"><span data-stu-id="4163c-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyExclusion -MatchVariable <String> -SelectorMatchOperator <String>
 -Selector <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4163c-105">說明</span><span class="sxs-lookup"><span data-stu-id="4163c-105">DESCRIPTION</span></span>
<span data-ttu-id="4163c-106">**新的-AzApplicationGatewayFirewallPolicyExclusion** Cmdlet 是防火牆原則的新排除規則清單。</span><span class="sxs-lookup"><span data-stu-id="4163c-106">The **New-AzApplicationGatewayFirewallPolicyExclusion** cmdlet a new exclusion rule list for firewall policy.</span></span>

## <span data-ttu-id="4163c-107">示例</span><span class="sxs-lookup"><span data-stu-id="4163c-107">EXAMPLES</span></span>

### <span data-ttu-id="4163c-108">範例1</span><span class="sxs-lookup"><span data-stu-id="4163c-108">Example 1</span></span>
```powershell
PS C:\> $exclusionEntry = New-AzApplicationGatewayFirewallPolicyExclusion -MatchVariable "RequestHeaderNames" -SelectorMatchOperator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="4163c-109">這個命令會為名為 RequestHeaderNames 的變數及名為 [xyz] 的運算子（名為 StartsWith 和選擇器）建立新的排除專案。</span><span class="sxs-lookup"><span data-stu-id="4163c-109">This command creates a new exclusion-entry for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="4163c-110">[排除] 專案會儲存在 $exclusionEntry 中。</span><span class="sxs-lookup"><span data-stu-id="4163c-110">The exclusion entry is saved in $exclusionEntry.</span></span>

## <span data-ttu-id="4163c-111">參數</span><span class="sxs-lookup"><span data-stu-id="4163c-111">PARAMETERS</span></span>

### <span data-ttu-id="4163c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4163c-112">-DefaultProfile</span></span>
<span data-ttu-id="4163c-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4163c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4163c-114">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="4163c-114">-MatchVariable</span></span>
<span data-ttu-id="4163c-115">要排除的變數。</span><span class="sxs-lookup"><span data-stu-id="4163c-115">The variable to be excluded.</span></span>

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

### <span data-ttu-id="4163c-116">-選取器</span><span class="sxs-lookup"><span data-stu-id="4163c-116">-Selector</span></span>
<span data-ttu-id="4163c-117">如果變數是集合，則是用來指定將此排除項適用于集合中哪些元素的運算子。</span><span class="sxs-lookup"><span data-stu-id="4163c-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="4163c-118">-SelectorMatchOperator</span><span class="sxs-lookup"><span data-stu-id="4163c-118">-SelectorMatchOperator</span></span>
<span data-ttu-id="4163c-119">當變數是集合時，請在選取器上操作，以指定將此排除項適用于集合中的哪些元素。</span><span class="sxs-lookup"><span data-stu-id="4163c-119">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="4163c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4163c-120">CommonParameters</span></span>
<span data-ttu-id="4163c-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4163c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4163c-122">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4163c-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4163c-123">輸入</span><span class="sxs-lookup"><span data-stu-id="4163c-123">INPUTS</span></span>

### <span data-ttu-id="4163c-124">所有</span><span class="sxs-lookup"><span data-stu-id="4163c-124">None</span></span>

## <span data-ttu-id="4163c-125">輸出</span><span class="sxs-lookup"><span data-stu-id="4163c-125">OUTPUTS</span></span>

### <span data-ttu-id="4163c-126">PSApplicationGatewayFirewallPolicyExclusion 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4163c-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyExclusion</span></span>

## <span data-ttu-id="4163c-127">筆記</span><span class="sxs-lookup"><span data-stu-id="4163c-127">NOTES</span></span>

## <span data-ttu-id="4163c-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="4163c-128">RELATED LINKS</span></span>
