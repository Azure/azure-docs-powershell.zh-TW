---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/enable-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Enable-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Enable-AzAdvisorRecommendation.md
ms.openlocfilehash: 7126a9c8ee11bcb5b32cc47ae31aaf821b171522
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969485"
---
# <span data-ttu-id="6eddc-101">Enable-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="6eddc-101">Enable-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="6eddc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6eddc-102">SYNOPSIS</span></span>
<span data-ttu-id="6eddc-103">啟用 Azure Advisor 建議 (s) 。</span><span class="sxs-lookup"><span data-stu-id="6eddc-103">Enables Azure Advisor recommendation(s).</span></span>

## <span data-ttu-id="6eddc-104">句法</span><span class="sxs-lookup"><span data-stu-id="6eddc-104">SYNTAX</span></span>

### <span data-ttu-id="6eddc-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6eddc-105">NameParameterSet (Default)</span></span>
```
Enable-AzAdvisorRecommendation [-RecommendationName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6eddc-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6eddc-106">IdParameterSet</span></span>
```
Enable-AzAdvisorRecommendation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6eddc-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6eddc-107">InputObjectParameterSet</span></span>
```
Enable-AzAdvisorRecommendation [-InputObject] <PsAzureAdvisorResourceRecommendationBase>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6eddc-108">說明</span><span class="sxs-lookup"><span data-stu-id="6eddc-108">DESCRIPTION</span></span>
<span data-ttu-id="6eddc-109">這個 Cmdlet 可啟用先前隱含的建議。</span><span class="sxs-lookup"><span data-stu-id="6eddc-109">This cmdlet enables a previously suppressed recommendation.</span></span> <span data-ttu-id="6eddc-110">您也可以移除所有與建議相關聯的禁止顯示。</span><span class="sxs-lookup"><span data-stu-id="6eddc-110">You can remove all the suppressions associated with a recommendation as well.</span></span>

## <span data-ttu-id="6eddc-111">示例</span><span class="sxs-lookup"><span data-stu-id="6eddc-111">EXAMPLES</span></span>

### <span data-ttu-id="6eddc-112">範例1</span><span class="sxs-lookup"><span data-stu-id="6eddc-112">Example 1</span></span>
```powershell
PS C:\> Enable-AzAdvisorRecommendation -ResourceId c3621337-f131-4bf4-92f2-3fb9c8cfa0d8 

ResourceId           : subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations/c3621337-f131-4bf4-92f2-3fb9c8cfa0d8
Category             : Performance
ExtendedProperties   : {}
Impact               : Medium
ImpactedField        : Microsoft.Cache/Redis
ImpactedValue        : xyz
LastUpdated          : 12/4/2018 12:06:47 AM
Metadata             : {}
RecommendationTypeId : 905a0026-8010-45b2-ab46-a92c3e4a5131
Risk                 : None
ShortDescription     : problem : Improve the performance and reliability of your Redis Cache instance
                       solution : Follow Redis cache Advisor recommendations

SuppressionIds       : {} 
Name                 : c3621337-f131-4bf4-92f2-3fb9c8cfa0d8
Type                 : Microsoft.Advisor/recommendations
```

<span data-ttu-id="6eddc-113">移除名稱為 "recommendation_id" 的指定建議的所有禁止顯示。</span><span class="sxs-lookup"><span data-stu-id="6eddc-113">Removes all the suppressions for the given recommendation with name "recommendation_id".</span></span>

### <span data-ttu-id="6eddc-114">範例2</span><span class="sxs-lookup"><span data-stu-id="6eddc-114">Example 2</span></span>
```powershell
PS C:\> Get-AzAdvisorRecommendation -ResourceId "/subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz" 
| Enable-AzAdvisorRecommendation

ResourceId           : subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations/{recommendation_id}
Category             : Performance
ExtendedProperties   : {}
Impact               : Medium
ImpactedField        : Microsoft.Cache/Redis
ImpactedValue        : xyz
LastUpdated          : 12/4/2018 12:06:47 AM
Metadata             : {}
RecommendationTypeId : 905a0026-8010-45b2-ab46-a92c3e4a5131
Risk                 : None
ShortDescription     : problem : Improve the performance and reliability of your Redis Cache instance
                       solution : Follow Redis cache Advisor recommendations

SuppressionIds       : {} 
Name                 : {recommendation_id}
Type                 : Microsoft.Advisor/recommendations
```

<span data-ttu-id="6eddc-115">移除指定建議的所有禁止顯示 (s) 從管線傳送。</span><span class="sxs-lookup"><span data-stu-id="6eddc-115">Removes all the suppressions for the given recommendation(s) passed from the pipeline.</span></span>

## <span data-ttu-id="6eddc-116">參數</span><span class="sxs-lookup"><span data-stu-id="6eddc-116">PARAMETERS</span></span>

### <span data-ttu-id="6eddc-117">-確認</span><span class="sxs-lookup"><span data-stu-id="6eddc-117">-Confirm</span></span>
<span data-ttu-id="6eddc-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6eddc-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6eddc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eddc-119">-DefaultProfile</span></span>
<span data-ttu-id="6eddc-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6eddc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6eddc-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6eddc-121">-InputObject</span></span>
<span data-ttu-id="6eddc-122">Get-AzAdvisorRecommendation call 傳回的 powershell 物件類型 PsAzureAdvisorResourceRecommendationBase。</span><span class="sxs-lookup"><span data-stu-id="6eddc-122">The powershell object type PsAzureAdvisorResourceRecommendationBase returned by Get-AzAdvisorRecommendation call.</span></span>

```yaml
Type: PsAzureAdvisorResourceRecommendationBase
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6eddc-123">-RecommendationName</span><span class="sxs-lookup"><span data-stu-id="6eddc-123">-RecommendationName</span></span>
<span data-ttu-id="6eddc-124">建議的數量。</span><span class="sxs-lookup"><span data-stu-id="6eddc-124">ResourceName of the recommendation.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6eddc-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6eddc-125">-ResourceId</span></span>
<span data-ttu-id="6eddc-126">要取消的建議識別碼。</span><span class="sxs-lookup"><span data-stu-id="6eddc-126">Id of the recommendation to be suppressed.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6eddc-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6eddc-127">-WhatIf</span></span>
<span data-ttu-id="6eddc-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6eddc-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6eddc-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6eddc-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6eddc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eddc-130">CommonParameters</span></span>
<span data-ttu-id="6eddc-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6eddc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="6eddc-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6eddc-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eddc-133">輸入</span><span class="sxs-lookup"><span data-stu-id="6eddc-133">INPUTS</span></span>

### <span data-ttu-id="6eddc-134">System.object</span><span class="sxs-lookup"><span data-stu-id="6eddc-134">System.String</span></span>

### <span data-ttu-id="6eddc-135">PsAzureAdvisorResourceRecommendationBase 中的 [...]</span><span class="sxs-lookup"><span data-stu-id="6eddc-135">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="6eddc-136">輸出</span><span class="sxs-lookup"><span data-stu-id="6eddc-136">OUTPUTS</span></span>

### <span data-ttu-id="6eddc-137">PsAzureAdvisorResourceRecommendationBase 中的 [...]</span><span class="sxs-lookup"><span data-stu-id="6eddc-137">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="6eddc-138">筆記</span><span class="sxs-lookup"><span data-stu-id="6eddc-138">NOTES</span></span>

## <span data-ttu-id="6eddc-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="6eddc-139">RELATED LINKS</span></span>
