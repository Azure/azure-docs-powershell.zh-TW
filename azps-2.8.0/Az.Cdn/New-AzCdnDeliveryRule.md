---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRule.md
ms.openlocfilehash: 981447b1988dd750534a69529989d5d3480bc006
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613533"
---
# <span data-ttu-id="222fc-101">New-AzCdnDeliveryRule</span><span class="sxs-lookup"><span data-stu-id="222fc-101">New-AzCdnDeliveryRule</span></span>

## <span data-ttu-id="222fc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="222fc-102">SYNOPSIS</span></span>
<span data-ttu-id="222fc-103">建立傳遞規則。</span><span class="sxs-lookup"><span data-stu-id="222fc-103">Creates a delivery rule.</span></span>

## <span data-ttu-id="222fc-104">句法</span><span class="sxs-lookup"><span data-stu-id="222fc-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRule [-Name <String>] -Order <Int32> [-Condition <PSDeliveryRuleCondition[]>]
 -Action <PSDeliveryRuleAction[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="222fc-105">說明</span><span class="sxs-lookup"><span data-stu-id="222fc-105">DESCRIPTION</span></span>
<span data-ttu-id="222fc-106">**新的-AzCdnDeliveryRule** Cmdlet 會建立 CDN 端點建立的傳遞規則。</span><span class="sxs-lookup"><span data-stu-id="222fc-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="222fc-107">示例</span><span class="sxs-lookup"><span data-stu-id="222fc-107">EXAMPLES</span></span>

### <span data-ttu-id="222fc-108">範例1</span><span class="sxs-lookup"><span data-stu-id="222fc-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRule -Name "rule1" -Order 1 -Condition $cond1 -Action $action1

Name  Order Actions           Conditions
----  ----- -------           ----------
rule1     1 {Accept-Encoding} {Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition}
```

<span data-ttu-id="222fc-109">建立簡單的規則。</span><span class="sxs-lookup"><span data-stu-id="222fc-109">Create a simple rule.</span></span>

## <span data-ttu-id="222fc-110">參數</span><span class="sxs-lookup"><span data-stu-id="222fc-110">PARAMETERS</span></span>

### <span data-ttu-id="222fc-111">-動作</span><span class="sxs-lookup"><span data-stu-id="222fc-111">-Action</span></span>
<span data-ttu-id="222fc-112">滿足規則的所有條件時所執行的動作清單。</span><span class="sxs-lookup"><span data-stu-id="222fc-112">A list of actions that are executed when all the conditions of a rule are satisfied.</span></span>

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

### <span data-ttu-id="222fc-113">-條件</span><span class="sxs-lookup"><span data-stu-id="222fc-113">-Condition</span></span>
<span data-ttu-id="222fc-114">要執行的動作必須符合的條件清單。</span><span class="sxs-lookup"><span data-stu-id="222fc-114">A list of conditions that must be matched for the actions to be executed.</span></span>

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

### <span data-ttu-id="222fc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="222fc-115">-DefaultProfile</span></span>
<span data-ttu-id="222fc-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="222fc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="222fc-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="222fc-117">-Name</span></span>
<span data-ttu-id="222fc-118">規則名稱</span><span class="sxs-lookup"><span data-stu-id="222fc-118">Name of the rule</span></span>

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

### <span data-ttu-id="222fc-119">-訂單</span><span class="sxs-lookup"><span data-stu-id="222fc-119">-Order</span></span>
<span data-ttu-id="222fc-120">規則順序</span><span class="sxs-lookup"><span data-stu-id="222fc-120">Order of the rule</span></span>

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

### <span data-ttu-id="222fc-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="222fc-121">CommonParameters</span></span>
<span data-ttu-id="222fc-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="222fc-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="222fc-123">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="222fc-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="222fc-124">輸入</span><span class="sxs-lookup"><span data-stu-id="222fc-124">INPUTS</span></span>

### <span data-ttu-id="222fc-125">所有</span><span class="sxs-lookup"><span data-stu-id="222fc-125">None</span></span>

## <span data-ttu-id="222fc-126">輸出</span><span class="sxs-lookup"><span data-stu-id="222fc-126">OUTPUTS</span></span>

### <span data-ttu-id="222fc-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRule</span><span class="sxs-lookup"><span data-stu-id="222fc-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRule</span></span>

## <span data-ttu-id="222fc-128">筆記</span><span class="sxs-lookup"><span data-stu-id="222fc-128">NOTES</span></span>

## <span data-ttu-id="222fc-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="222fc-129">RELATED LINKS</span></span>
