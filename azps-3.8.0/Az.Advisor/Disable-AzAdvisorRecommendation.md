---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/disable-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Disable-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Disable-AzAdvisorRecommendation.md
ms.openlocfilehash: c9ad0e4b6744c00e9b3f4e7894daa52d2575dd90
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957926"
---
# <span data-ttu-id="f4532-101">Disable-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="f4532-101">Disable-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="f4532-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f4532-102">SYNOPSIS</span></span>
<span data-ttu-id="f4532-103">停用 Azure Advisor 建議。</span><span class="sxs-lookup"><span data-stu-id="f4532-103">Disable an Azure Advisor recommendation.</span></span>

## <span data-ttu-id="f4532-104">句法</span><span class="sxs-lookup"><span data-stu-id="f4532-104">SYNTAX</span></span>

### <span data-ttu-id="f4532-105">IdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f4532-105">IdParameterSet (Default)</span></span>
```
Disable-AzAdvisorRecommendation [-ResourceId] <String> [[-Days] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4532-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4532-106">NameParameterSet</span></span>
```
Disable-AzAdvisorRecommendation [[-Days] <Int32>] [-RecommendationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4532-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4532-107">InputObjectParameterSet</span></span>
```
Disable-AzAdvisorRecommendation [[-Days] <Int32>] [-InputObject] <PsAzureAdvisorResourceRecommendationBase>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4532-108">說明</span><span class="sxs-lookup"><span data-stu-id="f4532-108">DESCRIPTION</span></span>
<span data-ttu-id="f4532-109">針對建議 (s) 建立抑制，這可讓特定的建議推遲特定的持續時間或無限期。</span><span class="sxs-lookup"><span data-stu-id="f4532-109">Creates a suppression for recommendation(s), this enables a particular recommendation to be postponed for a specific duration or infinitely.</span></span>

## <span data-ttu-id="f4532-110">示例</span><span class="sxs-lookup"><span data-stu-id="f4532-110">EXAMPLES</span></span>

### <span data-ttu-id="f4532-111">範例1</span><span class="sxs-lookup"><span data-stu-id="f4532-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzAdvisorRecommendation -Name "f380a3a8-9d18-cfad-78e0-55762c72a178"

SuppressionId : d1f70547-0e72-db29-443e-c1164d5d4377
Ttl           : -1
Id            : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations
                /{recommendation_id}/suppressions/HardCodedSupressionName
Name          : HardCodedSupressionName
Type          : Microsoft.Advisor/suppressions
```

<span data-ttu-id="f4532-112">針對指定的建議名稱，以預設的 SuppressionName 及預設日期為-1 來建立抑制。</span><span class="sxs-lookup"><span data-stu-id="f4532-112">Create a suppression for the given recommendation name with a default-SuppressionName and default days as -1.</span></span>

### <span data-ttu-id="f4532-113">範例2</span><span class="sxs-lookup"><span data-stu-id="f4532-113">Example 2</span></span>
```powershell
PS C:\> Disable-AzAdvisorRecommendation -ResourceId "/subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz" -Days 12

SuppressionId : 7d1f0547-0e72-db29-443e-c1164d5d4377
Ttl           : 12.00:00:00
Id            : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations
                /{recommendation_id}/suppressions/HardCodedSupressionName
Name          : HardCodedSupressionName
Type          : Microsoft.Advisor/suppressions
```

<span data-ttu-id="f4532-114">針對指定的建議識別碼建立禁止顯示。</span><span class="sxs-lookup"><span data-stu-id="f4532-114">A suppression is created for the given recommendation-Id.</span></span>

### <span data-ttu-id="f4532-115">範例3</span><span class="sxs-lookup"><span data-stu-id="f4532-115">Example 3</span></span>
```powershell
PS C:\>  Get-AzAdvisorRecommendation -ResourceId "/subscriptions/user_subscription/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz" | Disable-A
zAdvisorRecommendation

SuppressionId : daf24e78-af2d-e8d3-9c50-fa970edc2937
Ttl           : -1
Id            : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations
                /{recommendation_id}/suppressions/HardCodedSupressionName
Name          : HardCodedSupressionName
Type          : Microsoft.Advisor/suppressions
```

<span data-ttu-id="f4532-116">建立禁止顯示，從 Get-AzAdvisorRecommendation 移至 [停用] AzAdvisorRecommendation。</span><span class="sxs-lookup"><span data-stu-id="f4532-116">Creating a suppression, piping from Get-AzAdvisorRecommendation to Disable-AzAdvisorRecommendation.</span></span>

## <span data-ttu-id="f4532-117">參數</span><span class="sxs-lookup"><span data-stu-id="f4532-117">PARAMETERS</span></span>

### <span data-ttu-id="f4532-118">-確認</span><span class="sxs-lookup"><span data-stu-id="f4532-118">-Confirm</span></span>
<span data-ttu-id="f4532-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f4532-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4532-120">天</span><span class="sxs-lookup"><span data-stu-id="f4532-120">-Days</span></span>
<span data-ttu-id="f4532-121">停用的天數。</span><span class="sxs-lookup"><span data-stu-id="f4532-121">Days to disable.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4532-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4532-122">-DefaultProfile</span></span>
<span data-ttu-id="f4532-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f4532-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4532-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4532-124">-InputObject</span></span>
<span data-ttu-id="f4532-125">Get-AzAdvisorRecommendation call 傳回的 powershell 物件類型 PsAzureAdvisorResourceRecommendationBase。</span><span class="sxs-lookup"><span data-stu-id="f4532-125">The powershell object type PsAzureAdvisorResourceRecommendationBase returned by Get-AzAdvisorRecommendation call.</span></span>

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

### <span data-ttu-id="f4532-126">-RecommendationName</span><span class="sxs-lookup"><span data-stu-id="f4532-126">-RecommendationName</span></span>
<span data-ttu-id="f4532-127">建議的 CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="f4532-127">ResourceName of the recommendation</span></span>

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

### <span data-ttu-id="f4532-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4532-128">-ResourceId</span></span>
<span data-ttu-id="f4532-129">要取消的建議識別碼。</span><span class="sxs-lookup"><span data-stu-id="f4532-129">Id of the recommendation to be suppressed.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4532-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4532-130">-WhatIf</span></span>
<span data-ttu-id="f4532-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f4532-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4532-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f4532-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4532-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4532-133">CommonParameters</span></span>
<span data-ttu-id="f4532-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f4532-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f4532-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f4532-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4532-136">輸入</span><span class="sxs-lookup"><span data-stu-id="f4532-136">INPUTS</span></span>

### <span data-ttu-id="f4532-137">System.object</span><span class="sxs-lookup"><span data-stu-id="f4532-137">System.String</span></span>

### <span data-ttu-id="f4532-138">PsAzureAdvisorResourceRecommendationBase 中的 [...]</span><span class="sxs-lookup"><span data-stu-id="f4532-138">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="f4532-139">輸出</span><span class="sxs-lookup"><span data-stu-id="f4532-139">OUTPUTS</span></span>

### <span data-ttu-id="f4532-140">PsAzureAdvisorSuppressionContract 中的 [...]</span><span class="sxs-lookup"><span data-stu-id="f4532-140">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorSuppressionContract</span></span>

## <span data-ttu-id="f4532-141">筆記</span><span class="sxs-lookup"><span data-stu-id="f4532-141">NOTES</span></span>

## <span data-ttu-id="f4532-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="f4532-142">RELATED LINKS</span></span>
