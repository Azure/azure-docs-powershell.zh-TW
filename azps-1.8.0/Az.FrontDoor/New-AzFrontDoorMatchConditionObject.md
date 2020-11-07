---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoormatchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorMatchConditionObject.md
ms.openlocfilehash: ed711160bf761fe7b28f02a94d1ab4ffa6fdb59f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787789"
---
# <span data-ttu-id="1f8c5-101">New-AzFrontDoorMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="1f8c5-101">New-AzFrontDoorMatchConditionObject</span></span>

## <span data-ttu-id="1f8c5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1f8c5-102">SYNOPSIS</span></span>
<span data-ttu-id="1f8c5-103">建立 WAF 原則建立的 MatchCondition 物件</span><span class="sxs-lookup"><span data-stu-id="1f8c5-103">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="1f8c5-104">句法</span><span class="sxs-lookup"><span data-stu-id="1f8c5-104">SYNTAX</span></span>

```
New-AzFrontDoorMatchConditionObject -MatchVariable <PSMatchVariable> -OperatorProperty <PSOperatorProperty>
 [-MatchValue <String[]>] [-Selector <String>] [-NegateCondition <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f8c5-105">說明</span><span class="sxs-lookup"><span data-stu-id="1f8c5-105">DESCRIPTION</span></span>
<span data-ttu-id="1f8c5-106">建立 WAF 原則建立的 MatchCondition 物件</span><span class="sxs-lookup"><span data-stu-id="1f8c5-106">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="1f8c5-107">示例</span><span class="sxs-lookup"><span data-stu-id="1f8c5-107">EXAMPLES</span></span>

### <span data-ttu-id="1f8c5-108">範例1</span><span class="sxs-lookup"><span data-stu-id="1f8c5-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "User-Agent" -MatchValue "Windows"


MatchVariable OperatorProperty MatchValue Selector   NegateCondition
------------- ---------------- ---------- --------   ---------------
RequestHeader         Contains {Windows}  User-Agent           False
```

<span data-ttu-id="1f8c5-109">建立 MatchCondition 物件</span><span class="sxs-lookup"><span data-stu-id="1f8c5-109">Create a MatchCondition object</span></span>

## <span data-ttu-id="1f8c5-110">參數</span><span class="sxs-lookup"><span data-stu-id="1f8c5-110">PARAMETERS</span></span>

### <span data-ttu-id="1f8c5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f8c5-111">-DefaultProfile</span></span>
<span data-ttu-id="1f8c5-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1f8c5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f8c5-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="1f8c5-113">-MatchValue</span></span>
<span data-ttu-id="1f8c5-114">[相符] 值。</span><span class="sxs-lookup"><span data-stu-id="1f8c5-114">Match value.</span></span>

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

### <span data-ttu-id="1f8c5-115">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="1f8c5-115">-MatchVariable</span></span>
<span data-ttu-id="1f8c5-116">[相符] 變數。</span><span class="sxs-lookup"><span data-stu-id="1f8c5-116">Match Variable.</span></span>
<span data-ttu-id="1f8c5-117">可能的值包括： "RemoteAddr"、"RequestMethod"、"QueryString"、"PostArgs"、"RequestUri"、"RequestHeader"、"RequestBody"</span><span class="sxs-lookup"><span data-stu-id="1f8c5-117">Possible values include: 'RemoteAddr', 'RequestMethod', 'QueryString', 'PostArgs','RequestUri', 'RequestHeader', 'RequestBody'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSMatchVariable
Parameter Sets: (All)
Aliases:
Accepted values: RemoteAddr, RequestMethod, QueryString, PostArgs, RequestUri, RequestHeader, RequestBody

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f8c5-118">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="1f8c5-118">-NegateCondition</span></span>
<span data-ttu-id="1f8c5-119">描述此情況是否為 [否定] 條件，或 [非預設值] 為 false</span><span class="sxs-lookup"><span data-stu-id="1f8c5-119">Describes if this is negate condition or not Default value is false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f8c5-120">-OperatorProperty</span><span class="sxs-lookup"><span data-stu-id="1f8c5-120">-OperatorProperty</span></span>
<span data-ttu-id="1f8c5-121">描述要相符的運算子。</span><span class="sxs-lookup"><span data-stu-id="1f8c5-121">Describes operator to be matched.</span></span>
<span data-ttu-id="1f8c5-122">可能的值包括： [Any]、"IPMatch"、"GeoMatch"、"等於"、"Contains"、"小於"、"GreaterThan"、"LessThanOrEqual"、"GreaterThanOrEqual"、"BeginsWith"、"EndsWith"、""、"" "</span><span class="sxs-lookup"><span data-stu-id="1f8c5-122">Possible values include: 'Any', 'IPMatch', 'GeoMatch', 'Equal', 'Contains', 'LessThan', 'GreaterThan', 'LessThanOrEqual', 'GreaterThanOrEqual', 'BeginsWith', 'EndsWith''</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSOperatorProperty
Parameter Sets: (All)
Aliases:
Accepted values: Any, IPMatch, GeoMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f8c5-123">-選取器</span><span class="sxs-lookup"><span data-stu-id="1f8c5-123">-Selector</span></span>
<span data-ttu-id="1f8c5-124">要相符的 RequestHeader 或 RequestBody 中的選擇器名稱</span><span class="sxs-lookup"><span data-stu-id="1f8c5-124">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="1f8c5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f8c5-125">CommonParameters</span></span>
<span data-ttu-id="1f8c5-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1f8c5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f8c5-127">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1f8c5-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f8c5-128">輸入</span><span class="sxs-lookup"><span data-stu-id="1f8c5-128">INPUTS</span></span>

### <span data-ttu-id="1f8c5-129">所有</span><span class="sxs-lookup"><span data-stu-id="1f8c5-129">None</span></span>

## <span data-ttu-id="1f8c5-130">輸出</span><span class="sxs-lookup"><span data-stu-id="1f8c5-130">OUTPUTS</span></span>

### <span data-ttu-id="1f8c5-131">PSMatchCondition 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="1f8c5-131">Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition</span></span>

## <span data-ttu-id="1f8c5-132">筆記</span><span class="sxs-lookup"><span data-stu-id="1f8c5-132">NOTES</span></span>

## <span data-ttu-id="1f8c5-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="1f8c5-133">RELATED LINKS</span></span>

[<span data-ttu-id="1f8c5-134">新-AzFrontDoorCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="1f8c5-134">New-AzFrontDoorCustomRuleObject</span></span>](./New-AzFrontDoorCustomRuleObject.md)
