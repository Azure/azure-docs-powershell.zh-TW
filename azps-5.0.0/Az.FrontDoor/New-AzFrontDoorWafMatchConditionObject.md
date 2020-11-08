---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmatchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafMatchConditionObject.md
ms.openlocfilehash: 0340cbf8c71b0ab117f1ff967ec7c3bb3e32b8f9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94136897"
---
# <span data-ttu-id="bb0fc-101">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="bb0fc-101">New-AzFrontDoorWafMatchConditionObject</span></span>

## <span data-ttu-id="bb0fc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bb0fc-102">SYNOPSIS</span></span>
<span data-ttu-id="bb0fc-103">建立 WAF 原則建立的 MatchCondition 物件</span><span class="sxs-lookup"><span data-stu-id="bb0fc-103">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="bb0fc-104">句法</span><span class="sxs-lookup"><span data-stu-id="bb0fc-104">SYNTAX</span></span>

```
New-AzFrontDoorWafMatchConditionObject -MatchVariable <String> -OperatorProperty <String>
 [-MatchValue <String[]>] [-Selector <String>] [-NegateCondition <Boolean>] [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb0fc-105">說明</span><span class="sxs-lookup"><span data-stu-id="bb0fc-105">DESCRIPTION</span></span>
<span data-ttu-id="bb0fc-106">建立 WAF 原則建立的 MatchCondition 物件</span><span class="sxs-lookup"><span data-stu-id="bb0fc-106">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="bb0fc-107">示例</span><span class="sxs-lookup"><span data-stu-id="bb0fc-107">EXAMPLES</span></span>

### <span data-ttu-id="bb0fc-108">範例1</span><span class="sxs-lookup"><span data-stu-id="bb0fc-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "User-Agent" -MatchValue "Windows"


MatchVariable OperatorProperty MatchValue Selector   NegateCondition Transform
------------- ---------------- ---------- --------   --------------- ---------
RequestHeader Contains         {Windows}  User-Agent           False
```

### <span data-ttu-id="bb0fc-109">範例2</span><span class="sxs-lookup"><span data-stu-id="bb0fc-109">Example 2</span></span>
```powershell
PS C:\> New-AzFrontDoorWafMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "User-Agent" -MatchValue "WINDOWS" -Transform Uppercase


MatchVariable OperatorProperty MatchValue Selector   NegateCondition Transform
------------- ---------------- ---------- --------   --------------- ---------
RequestHeader Contains         {WINDOWS}  User-Agent           False {Uppercase}
```

<span data-ttu-id="bb0fc-110">建立 MatchCondition 物件</span><span class="sxs-lookup"><span data-stu-id="bb0fc-110">Create a MatchCondition object</span></span>

## <span data-ttu-id="bb0fc-111">參數</span><span class="sxs-lookup"><span data-stu-id="bb0fc-111">PARAMETERS</span></span>

### <span data-ttu-id="bb0fc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb0fc-112">-DefaultProfile</span></span>
<span data-ttu-id="bb0fc-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bb0fc-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb0fc-114">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="bb0fc-114">-MatchValue</span></span>
<span data-ttu-id="bb0fc-115">[相符] 值。</span><span class="sxs-lookup"><span data-stu-id="bb0fc-115">Match value.</span></span>

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

### <span data-ttu-id="bb0fc-116">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="bb0fc-116">-MatchVariable</span></span>
<span data-ttu-id="bb0fc-117">[相符] 變數。</span><span class="sxs-lookup"><span data-stu-id="bb0fc-117">Match Variable.</span></span>
<span data-ttu-id="bb0fc-118">可能的值包括： "RemoteAddr"、"RequestMethod"、"QueryString"、"PostArgs"、"RequestUri"、"RequestHeader"、"RequestBody"、"SocketAddr"</span><span class="sxs-lookup"><span data-stu-id="bb0fc-118">Possible values include: 'RemoteAddr', 'RequestMethod', 'QueryString', 'PostArgs','RequestUri', 'RequestHeader', 'RequestBody', 'SocketAddr'</span></span>

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

### <span data-ttu-id="bb0fc-119">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="bb0fc-119">-NegateCondition</span></span>
<span data-ttu-id="bb0fc-120">描述此情況是否為 [否定] 條件，或 [非預設值] 為 false</span><span class="sxs-lookup"><span data-stu-id="bb0fc-120">Describes if this is negate condition or not Default value is false</span></span>

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

### <span data-ttu-id="bb0fc-121">-OperatorProperty</span><span class="sxs-lookup"><span data-stu-id="bb0fc-121">-OperatorProperty</span></span>
<span data-ttu-id="bb0fc-122">描述要相符的運算子。</span><span class="sxs-lookup"><span data-stu-id="bb0fc-122">Describes operator to be matched.</span></span>
<span data-ttu-id="bb0fc-123">可能的值包括： "Any"、"IPMatch"、"GeoMatch"、"等於"、"Contains"、"小於"、"GreaterThan"、"LessThanOrEqual"、"GreaterThanOrEqual"、"BeginsWith"、"EndsWith"、""、""、"RegEx"</span><span class="sxs-lookup"><span data-stu-id="bb0fc-123">Possible values include: 'Any', 'IPMatch', 'GeoMatch', 'Equal', 'Contains', 'LessThan', 'GreaterThan', 'LessThanOrEqual', 'GreaterThanOrEqual', 'BeginsWith', 'EndsWith', 'RegEx'</span></span>

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

### <span data-ttu-id="bb0fc-124">-選取器</span><span class="sxs-lookup"><span data-stu-id="bb0fc-124">-Selector</span></span>
<span data-ttu-id="bb0fc-125">要相符的 RequestHeader 或 RequestBody 中的選擇器名稱</span><span class="sxs-lookup"><span data-stu-id="bb0fc-125">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="bb0fc-126">-轉換</span><span class="sxs-lookup"><span data-stu-id="bb0fc-126">-Transform</span></span>
<span data-ttu-id="bb0fc-127">要套用的轉換。</span><span class="sxs-lookup"><span data-stu-id="bb0fc-127">Transforms to apply.</span></span> <span data-ttu-id="bb0fc-128">可能的值包括： "小寫"、"大寫"、"Trim"、"UrlDecode"、"UrlEncode"、"RemoveNulls"。</span><span class="sxs-lookup"><span data-stu-id="bb0fc-128">Possible values include: 'Lowercase', 'Uppercase', 'Trim', 'UrlDecode', 'UrlEncode', 'RemoveNulls'.</span></span>

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

### <span data-ttu-id="bb0fc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb0fc-129">CommonParameters</span></span>
<span data-ttu-id="bb0fc-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bb0fc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb0fc-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="bb0fc-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb0fc-132">輸入</span><span class="sxs-lookup"><span data-stu-id="bb0fc-132">INPUTS</span></span>

### <span data-ttu-id="bb0fc-133">所有</span><span class="sxs-lookup"><span data-stu-id="bb0fc-133">None</span></span>

## <span data-ttu-id="bb0fc-134">輸出</span><span class="sxs-lookup"><span data-stu-id="bb0fc-134">OUTPUTS</span></span>

### <span data-ttu-id="bb0fc-135">PSMatchCondition 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="bb0fc-135">Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition</span></span>

## <span data-ttu-id="bb0fc-136">筆記</span><span class="sxs-lookup"><span data-stu-id="bb0fc-136">NOTES</span></span>

## <span data-ttu-id="bb0fc-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="bb0fc-137">RELATED LINKS</span></span>

[<span data-ttu-id="bb0fc-138">新-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="bb0fc-138">New-AzFrontDoorWafCustomRuleObject</span></span>](./New-AzFrontDoorWafCustomRuleObject.md)