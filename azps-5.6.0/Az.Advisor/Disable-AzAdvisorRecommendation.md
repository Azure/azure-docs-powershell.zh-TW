---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/powershell/module/az.advisor/disable-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Disable-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Disable-AzAdvisorRecommendation.md
ms.openlocfilehash: 3695ee9d027733d3adea17797ffbcf669136e66b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905685"
---
# <span data-ttu-id="b8d1d-101">Disable-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="b8d1d-101">Disable-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="b8d1d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b8d1d-102">SYNOPSIS</span></span>
<span data-ttu-id="b8d1d-103">停用 Azure 建議程式。</span><span class="sxs-lookup"><span data-stu-id="b8d1d-103">Disable an Azure Advisor recommendation.</span></span>

## <span data-ttu-id="b8d1d-104">語法</span><span class="sxs-lookup"><span data-stu-id="b8d1d-104">SYNTAX</span></span>

### <span data-ttu-id="b8d1d-105">IdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b8d1d-105">IdParameterSet (Default)</span></span>
```
Disable-AzAdvisorRecommendation [-ResourceId] <String> [[-Days] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8d1d-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8d1d-106">NameParameterSet</span></span>
```
Disable-AzAdvisorRecommendation [[-Days] <Int32>] [-RecommendationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8d1d-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8d1d-107">InputObjectParameterSet</span></span>
```
Disable-AzAdvisorRecommendation [[-Days] <Int32>] [-InputObject] <PsAzureAdvisorResourceRecommendationBase>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8d1d-108">描述</span><span class="sxs-lookup"><span data-stu-id="b8d1d-108">DESCRIPTION</span></span>
<span data-ttu-id="b8d1d-109">建立建議建議 () ，這可讓特定建議延後特定期間或無限延遲。</span><span class="sxs-lookup"><span data-stu-id="b8d1d-109">Creates a suppression for recommendation(s), this enables a particular recommendation to be postponed for a specific duration or infinitely.</span></span>

## <span data-ttu-id="b8d1d-110">例子</span><span class="sxs-lookup"><span data-stu-id="b8d1d-110">EXAMPLES</span></span>

### <span data-ttu-id="b8d1d-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="b8d1d-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzAdvisorRecommendation -Name "f380a3a8-9d18-cfad-78e0-55762c72a178"

SuppressionId : d1f70547-0e72-db29-443e-c1164d5d4377
Ttl           : -1
Id            : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations
                /{recommendation_id}/suppressions/HardCodedSupressionName
Name          : HardCodedSupressionName
Type          : Microsoft.Advisor/suppressions
```

<span data-ttu-id="b8d1d-112">為指定的建議名稱建立預設 -Name 和預設天數為 -1 的預設建議名稱。</span><span class="sxs-lookup"><span data-stu-id="b8d1d-112">Create a suppression for the given recommendation name with a default-SuppressionName and default days as -1.</span></span>

### <span data-ttu-id="b8d1d-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="b8d1d-113">Example 2</span></span>
```powershell
PS C:\> Disable-AzAdvisorRecommendation -ResourceId "/subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz" -Days 12

SuppressionId : 7d1f0547-0e72-db29-443e-c1164d5d4377
Ttl           : 12.00:00:00
Id            : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommendations
                /{recommendation_id}/suppressions/HardCodedSupressionName
Name          : HardCodedSupressionName
Type          : Microsoft.Advisor/suppressions
```

<span data-ttu-id="b8d1d-114">系統會為所提供的建議識別碼建立一個建議。</span><span class="sxs-lookup"><span data-stu-id="b8d1d-114">A suppression is created for the given recommendation-Id.</span></span>

### <span data-ttu-id="b8d1d-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="b8d1d-115">Example 3</span></span>
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

<span data-ttu-id="b8d1d-116">建立裝飾，從Get-AzAdvisorRecommendation到 Disable-AzAdvisorRecommendation。</span><span class="sxs-lookup"><span data-stu-id="b8d1d-116">Creating a suppression, piping from Get-AzAdvisorRecommendation to Disable-AzAdvisorRecommendation.</span></span>

## <span data-ttu-id="b8d1d-117">參數</span><span class="sxs-lookup"><span data-stu-id="b8d1d-117">PARAMETERS</span></span>

### <span data-ttu-id="b8d1d-118">-確認</span><span class="sxs-lookup"><span data-stu-id="b8d1d-118">-Confirm</span></span>
<span data-ttu-id="b8d1d-119">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b8d1d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8d1d-120">-天數</span><span class="sxs-lookup"><span data-stu-id="b8d1d-120">-Days</span></span>
<span data-ttu-id="b8d1d-121">要停用的天數。</span><span class="sxs-lookup"><span data-stu-id="b8d1d-121">Days to disable.</span></span>

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

### <span data-ttu-id="b8d1d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8d1d-122">-DefaultProfile</span></span>
<span data-ttu-id="b8d1d-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b8d1d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8d1d-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8d1d-124">-InputObject</span></span>
<span data-ttu-id="b8d1d-125">Powershell 物件類型 PsAzureAdvisorResourceRecommendationBase 由 Get-AzAdvisorRecommendation呼叫。</span><span class="sxs-lookup"><span data-stu-id="b8d1d-125">The powershell object type PsAzureAdvisorResourceRecommendationBase returned by Get-AzAdvisorRecommendation call.</span></span>

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

### <span data-ttu-id="b8d1d-126">-RecommendationName</span><span class="sxs-lookup"><span data-stu-id="b8d1d-126">-RecommendationName</span></span>
<span data-ttu-id="b8d1d-127">建議的資源名稱</span><span class="sxs-lookup"><span data-stu-id="b8d1d-127">ResourceName of the recommendation</span></span>

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

### <span data-ttu-id="b8d1d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8d1d-128">-ResourceId</span></span>
<span data-ttu-id="b8d1d-129">要隱藏的建議識別碼。</span><span class="sxs-lookup"><span data-stu-id="b8d1d-129">Id of the recommendation to be suppressed.</span></span>

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

### <span data-ttu-id="b8d1d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8d1d-130">-WhatIf</span></span>
<span data-ttu-id="b8d1d-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b8d1d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8d1d-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b8d1d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8d1d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8d1d-133">CommonParameters</span></span>
<span data-ttu-id="b8d1d-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b8d1d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b8d1d-135">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="b8d1d-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8d1d-136">輸入</span><span class="sxs-lookup"><span data-stu-id="b8d1d-136">INPUTS</span></span>

### <span data-ttu-id="b8d1d-137">System.String</span><span class="sxs-lookup"><span data-stu-id="b8d1d-137">System.String</span></span>

### <span data-ttu-id="b8d1d-138">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="b8d1d-138">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="b8d1d-139">輸出</span><span class="sxs-lookup"><span data-stu-id="b8d1d-139">OUTPUTS</span></span>

### <span data-ttu-id="b8d1d-140">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorSuppressionContract</span><span class="sxs-lookup"><span data-stu-id="b8d1d-140">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorSuppressionContract</span></span>

## <span data-ttu-id="b8d1d-141">筆記</span><span class="sxs-lookup"><span data-stu-id="b8d1d-141">NOTES</span></span>

## <span data-ttu-id="b8d1d-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="b8d1d-142">RELATED LINKS</span></span>
