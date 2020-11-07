---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoormatchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorMatchConditionObject.md
ms.openlocfilehash: 70ab8b592c550280f424f9c0a4bfced877942edc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624375"
---
# <span data-ttu-id="5edc1-101">New-AzureRmFrontDoorMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="5edc1-101">New-AzureRmFrontDoorMatchConditionObject</span></span>

## <span data-ttu-id="5edc1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5edc1-102">SYNOPSIS</span></span>
<span data-ttu-id="5edc1-103">建立 WAF 原則建立的 MatchCondition 物件</span><span class="sxs-lookup"><span data-stu-id="5edc1-103">Create MatchCondition Object for WAF policy creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5edc1-104">句法</span><span class="sxs-lookup"><span data-stu-id="5edc1-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorMatchConditionObject -MatchVariable <PSMatchVariable>
 -OperatorProperty <PSOperatorProperty> -MatchValue <String[]> [-Selector <String>]
 [-NegateCondition <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5edc1-105">說明</span><span class="sxs-lookup"><span data-stu-id="5edc1-105">DESCRIPTION</span></span>
<span data-ttu-id="5edc1-106">建立 WAF 原則建立的 MatchCondition 物件</span><span class="sxs-lookup"><span data-stu-id="5edc1-106">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="5edc1-107">示例</span><span class="sxs-lookup"><span data-stu-id="5edc1-107">EXAMPLES</span></span>

### <span data-ttu-id="5edc1-108">範例1</span><span class="sxs-lookup"><span data-stu-id="5edc1-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "UserAgent" -MatchValue "Windows"


MatchVariable    : RequestHeader
OperatorProperty : Contains
MatchValue       : {Windows}
Selector         : UserAgent
NegateCondition  : False
```

<span data-ttu-id="5edc1-109">建立 MatchCondition 物件</span><span class="sxs-lookup"><span data-stu-id="5edc1-109">Create a MatchCondition object</span></span>

## <span data-ttu-id="5edc1-110">參數</span><span class="sxs-lookup"><span data-stu-id="5edc1-110">PARAMETERS</span></span>

### <span data-ttu-id="5edc1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5edc1-111">-DefaultProfile</span></span>
<span data-ttu-id="5edc1-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5edc1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5edc1-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="5edc1-113">-MatchValue</span></span>
<span data-ttu-id="5edc1-114">[相符] 值。</span><span class="sxs-lookup"><span data-stu-id="5edc1-114">Match value.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5edc1-115">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="5edc1-115">-MatchVariable</span></span>
<span data-ttu-id="5edc1-116">[相符] 變數。</span><span class="sxs-lookup"><span data-stu-id="5edc1-116">Match Variable.</span></span>
<span data-ttu-id="5edc1-117">可能的值包括： "RemoteAddr"、"RequestMethod"、"QueryString"、"PostArgs"、"RequestUri"、"RequestHeader"、"RequestBody"</span><span class="sxs-lookup"><span data-stu-id="5edc1-117">Possible values include: 'RemoteAddr', 'RequestMethod', 'QueryString', 'PostArgs','RequestUri', 'RequestHeader', 'RequestBody'</span></span>

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

### <span data-ttu-id="5edc1-118">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="5edc1-118">-NegateCondition</span></span>
<span data-ttu-id="5edc1-119">描述此情況是否為 [否定] 條件，或 [非預設值] 為 false</span><span class="sxs-lookup"><span data-stu-id="5edc1-119">Describes if this is negate condition or not Default value is false</span></span>

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

### <span data-ttu-id="5edc1-120">-OperatorProperty</span><span class="sxs-lookup"><span data-stu-id="5edc1-120">-OperatorProperty</span></span>
<span data-ttu-id="5edc1-121">描述要相符的運算子。</span><span class="sxs-lookup"><span data-stu-id="5edc1-121">Describes operator to be matched.</span></span>
<span data-ttu-id="5edc1-122">可能的值包括： [Any]、"IPMatch"、"GeoMatch"、"等於"、"Contains"、"小於"、"GreaterThan"、"LessThanOrEqual"、"GreaterThanOrEqual"、"BeginsWith"、"EndsWith"、""、"" "</span><span class="sxs-lookup"><span data-stu-id="5edc1-122">Possible values include: 'Any', 'IPMatch', 'GeoMatch', 'Equal', 'Contains', 'LessThan', 'GreaterThan', 'LessThanOrEqual', 'GreaterThanOrEqual', 'BeginsWith', 'EndsWith''</span></span>

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

### <span data-ttu-id="5edc1-123">-選取器</span><span class="sxs-lookup"><span data-stu-id="5edc1-123">-Selector</span></span>
<span data-ttu-id="5edc1-124">要相符的 RequestHeader 或 RequestBody 中的選擇器名稱</span><span class="sxs-lookup"><span data-stu-id="5edc1-124">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="5edc1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5edc1-125">CommonParameters</span></span>
<span data-ttu-id="5edc1-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5edc1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5edc1-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5edc1-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5edc1-128">輸入</span><span class="sxs-lookup"><span data-stu-id="5edc1-128">INPUTS</span></span>

### <span data-ttu-id="5edc1-129">所有</span><span class="sxs-lookup"><span data-stu-id="5edc1-129">None</span></span>

## <span data-ttu-id="5edc1-130">輸出</span><span class="sxs-lookup"><span data-stu-id="5edc1-130">OUTPUTS</span></span>

### <span data-ttu-id="5edc1-131">PSMatchCondition 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="5edc1-131">Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition</span></span>

## <span data-ttu-id="5edc1-132">筆記</span><span class="sxs-lookup"><span data-stu-id="5edc1-132">NOTES</span></span>

## <span data-ttu-id="5edc1-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="5edc1-133">RELATED LINKS</span></span>

[<span data-ttu-id="5edc1-134">新-AzureRmFrontDoorCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="5edc1-134">New-AzureRmFrontDoorCustomRuleObject</span></span>](./New-AzureRmFrontDoorCustomRuleObject.md)
