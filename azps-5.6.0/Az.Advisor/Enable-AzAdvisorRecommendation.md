---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/powershell/module/az.advisor/enable-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Enable-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Enable-AzAdvisorRecommendation.md
ms.openlocfilehash: 6bf98fad2b1604f88293b81c55d49e9de3f0c33c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905682"
---
# <span data-ttu-id="2ebaa-101">Enable-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="2ebaa-101">Enable-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="2ebaa-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2ebaa-102">SYNOPSIS</span></span>
<span data-ttu-id="2ebaa-103">啟用 Azure 建議 (建議) 。</span><span class="sxs-lookup"><span data-stu-id="2ebaa-103">Enables Azure Advisor recommendation(s).</span></span>

## <span data-ttu-id="2ebaa-104">語法</span><span class="sxs-lookup"><span data-stu-id="2ebaa-104">SYNTAX</span></span>

### <span data-ttu-id="2ebaa-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2ebaa-105">NameParameterSet (Default)</span></span>
```
Enable-AzAdvisorRecommendation [-RecommendationName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ebaa-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ebaa-106">IdParameterSet</span></span>
```
Enable-AzAdvisorRecommendation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ebaa-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ebaa-107">InputObjectParameterSet</span></span>
```
Enable-AzAdvisorRecommendation [-InputObject] <PsAzureAdvisorResourceRecommendationBase>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ebaa-108">描述</span><span class="sxs-lookup"><span data-stu-id="2ebaa-108">DESCRIPTION</span></span>
<span data-ttu-id="2ebaa-109">此 Cmdlet 啟用先前隱藏的建議。</span><span class="sxs-lookup"><span data-stu-id="2ebaa-109">This cmdlet enables a previously suppressed recommendation.</span></span> <span data-ttu-id="2ebaa-110">您也可以移除與建議相關的所有干擾。</span><span class="sxs-lookup"><span data-stu-id="2ebaa-110">You can remove all the suppressions associated with a recommendation as well.</span></span>

## <span data-ttu-id="2ebaa-111">例子</span><span class="sxs-lookup"><span data-stu-id="2ebaa-111">EXAMPLES</span></span>

### <span data-ttu-id="2ebaa-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="2ebaa-112">Example 1</span></span>
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

<span data-ttu-id="2ebaa-113">移除指定建議中名稱為 "recommendation_id" 的所有干擾。</span><span class="sxs-lookup"><span data-stu-id="2ebaa-113">Removes all the suppressions for the given recommendation with name "recommendation_id".</span></span>

### <span data-ttu-id="2ebaa-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="2ebaa-114">Example 2</span></span>
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

<span data-ttu-id="2ebaa-115">移除從管線傳遞之 (建議) 的所有干擾。</span><span class="sxs-lookup"><span data-stu-id="2ebaa-115">Removes all the suppressions for the given recommendation(s) passed from the pipeline.</span></span>

## <span data-ttu-id="2ebaa-116">參數</span><span class="sxs-lookup"><span data-stu-id="2ebaa-116">PARAMETERS</span></span>

### <span data-ttu-id="2ebaa-117">-確認</span><span class="sxs-lookup"><span data-stu-id="2ebaa-117">-Confirm</span></span>
<span data-ttu-id="2ebaa-118">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2ebaa-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ebaa-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ebaa-119">-DefaultProfile</span></span>
<span data-ttu-id="2ebaa-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2ebaa-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ebaa-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ebaa-121">-InputObject</span></span>
<span data-ttu-id="2ebaa-122">Powershell 物件類型 PsAzureAdvisorResourceRecommendationBase 由 Get-AzAdvisorRecommendation呼叫。</span><span class="sxs-lookup"><span data-stu-id="2ebaa-122">The powershell object type PsAzureAdvisorResourceRecommendationBase returned by Get-AzAdvisorRecommendation call.</span></span>

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

### <span data-ttu-id="2ebaa-123">-RecommendationName</span><span class="sxs-lookup"><span data-stu-id="2ebaa-123">-RecommendationName</span></span>
<span data-ttu-id="2ebaa-124">建議的資源名稱。</span><span class="sxs-lookup"><span data-stu-id="2ebaa-124">ResourceName of the recommendation.</span></span>

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

### <span data-ttu-id="2ebaa-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ebaa-125">-ResourceId</span></span>
<span data-ttu-id="2ebaa-126">要隱藏的建議識別碼。</span><span class="sxs-lookup"><span data-stu-id="2ebaa-126">Id of the recommendation to be suppressed.</span></span>

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

### <span data-ttu-id="2ebaa-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ebaa-127">-WhatIf</span></span>
<span data-ttu-id="2ebaa-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2ebaa-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ebaa-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2ebaa-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ebaa-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ebaa-130">CommonParameters</span></span>
<span data-ttu-id="2ebaa-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2ebaa-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2ebaa-132">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="2ebaa-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ebaa-133">輸入</span><span class="sxs-lookup"><span data-stu-id="2ebaa-133">INPUTS</span></span>

### <span data-ttu-id="2ebaa-134">System.String</span><span class="sxs-lookup"><span data-stu-id="2ebaa-134">System.String</span></span>

### <span data-ttu-id="2ebaa-135">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="2ebaa-135">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="2ebaa-136">輸出</span><span class="sxs-lookup"><span data-stu-id="2ebaa-136">OUTPUTS</span></span>

### <span data-ttu-id="2ebaa-137">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="2ebaa-137">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="2ebaa-138">筆記</span><span class="sxs-lookup"><span data-stu-id="2ebaa-138">NOTES</span></span>

## <span data-ttu-id="2ebaa-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="2ebaa-139">RELATED LINKS</span></span>
