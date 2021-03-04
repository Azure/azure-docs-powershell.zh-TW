---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/new-azcdndeliveryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRule.md
ms.openlocfilehash: a2143e0363d08a06ac72ee7c5207ef93f5c3a509
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914913"
---
# <span data-ttu-id="5e105-101">New-AzCdnDeliveryRule</span><span class="sxs-lookup"><span data-stu-id="5e105-101">New-AzCdnDeliveryRule</span></span>

## <span data-ttu-id="5e105-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5e105-102">SYNOPSIS</span></span>
<span data-ttu-id="5e105-103">建立傳遞規則。</span><span class="sxs-lookup"><span data-stu-id="5e105-103">Creates a delivery rule.</span></span>

## <span data-ttu-id="5e105-104">語法</span><span class="sxs-lookup"><span data-stu-id="5e105-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRule [-Name <String>] -Order <Int32> [-Condition <PSDeliveryRuleCondition[]>]
 -Action <PSDeliveryRuleAction[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e105-105">描述</span><span class="sxs-lookup"><span data-stu-id="5e105-105">DESCRIPTION</span></span>
<span data-ttu-id="5e105-106">**New-AzCdnDeliveryRule** Cmdlet 會建立 CDN 端點的建立傳遞規則。</span><span class="sxs-lookup"><span data-stu-id="5e105-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="5e105-107">例子</span><span class="sxs-lookup"><span data-stu-id="5e105-107">EXAMPLES</span></span>

### <span data-ttu-id="5e105-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="5e105-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRule -Name "rule1" -Order 1 -Condition $cond1 -Action $action1

Name  Order Actions           Conditions
----  ----- -------           ----------
rule1     1 {Accept-Encoding} {Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition}
```

<span data-ttu-id="5e105-109">建立簡單的規則。</span><span class="sxs-lookup"><span data-stu-id="5e105-109">Create a simple rule.</span></span>

## <span data-ttu-id="5e105-110">參數</span><span class="sxs-lookup"><span data-stu-id="5e105-110">PARAMETERS</span></span>

### <span data-ttu-id="5e105-111">-動作</span><span class="sxs-lookup"><span data-stu-id="5e105-111">-Action</span></span>
<span data-ttu-id="5e105-112">滿足規則的所有條件時所執行的動作清單。</span><span class="sxs-lookup"><span data-stu-id="5e105-112">A list of actions that are executed when all the conditions of a rule are satisfied.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e105-113">-條件</span><span class="sxs-lookup"><span data-stu-id="5e105-113">-Condition</span></span>
<span data-ttu-id="5e105-114">必須相符的條件清單，以執行要執行的動作。</span><span class="sxs-lookup"><span data-stu-id="5e105-114">A list of conditions that must be matched for the actions to be executed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e105-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e105-115">-DefaultProfile</span></span>
<span data-ttu-id="5e105-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5e105-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e105-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="5e105-117">-Name</span></span>
<span data-ttu-id="5e105-118">規則名稱</span><span class="sxs-lookup"><span data-stu-id="5e105-118">Name of the rule</span></span>

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

### <span data-ttu-id="5e105-119">-訂單</span><span class="sxs-lookup"><span data-stu-id="5e105-119">-Order</span></span>
<span data-ttu-id="5e105-120">規則的順序</span><span class="sxs-lookup"><span data-stu-id="5e105-120">Order of the rule</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e105-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e105-121">CommonParameters</span></span>
<span data-ttu-id="5e105-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5e105-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e105-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5e105-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e105-124">輸入</span><span class="sxs-lookup"><span data-stu-id="5e105-124">INPUTS</span></span>

### <span data-ttu-id="5e105-125">沒有</span><span class="sxs-lookup"><span data-stu-id="5e105-125">None</span></span>

## <span data-ttu-id="5e105-126">輸出</span><span class="sxs-lookup"><span data-stu-id="5e105-126">OUTPUTS</span></span>

### <span data-ttu-id="5e105-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSD力規則</span><span class="sxs-lookup"><span data-stu-id="5e105-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRule</span></span>

## <span data-ttu-id="5e105-128">筆記</span><span class="sxs-lookup"><span data-stu-id="5e105-128">NOTES</span></span>

## <span data-ttu-id="5e105-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="5e105-129">RELATED LINKS</span></span>
