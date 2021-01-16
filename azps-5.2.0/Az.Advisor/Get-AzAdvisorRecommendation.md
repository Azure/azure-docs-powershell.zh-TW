---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/get-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorRecommendation.md
ms.openlocfilehash: 631e471af79ab5ac567afeafa8103e22ae885ed7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98278951"
---
# <span data-ttu-id="e43e8-101">Get-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="e43e8-101">Get-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="e43e8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e43e8-102">SYNOPSIS</span></span>
<span data-ttu-id="e43e8-103">取得 Azure Advisor 建議的清單。</span><span class="sxs-lookup"><span data-stu-id="e43e8-103">Gets a list of Azure Advisor recommendations.</span></span>

## <span data-ttu-id="e43e8-104">句法</span><span class="sxs-lookup"><span data-stu-id="e43e8-104">SYNTAX</span></span>

### <span data-ttu-id="e43e8-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e43e8-105">NameParameterSet (Default)</span></span>
```
Get-AzAdvisorRecommendation [-Category <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e43e8-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e43e8-106">IdParameterSet</span></span>
```
Get-AzAdvisorRecommendation [-ResourceId] <String> [-Category <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e43e8-107">說明</span><span class="sxs-lookup"><span data-stu-id="e43e8-107">DESCRIPTION</span></span>
<span data-ttu-id="e43e8-108">獲取 Azure Advisor 建議清單。</span><span class="sxs-lookup"><span data-stu-id="e43e8-108">Obtains the list of Azure Advisor recommendations.</span></span> <span data-ttu-id="e43e8-109">可以依據類別、資源識別碼、名稱等進行篩選。</span><span class="sxs-lookup"><span data-stu-id="e43e8-109">Can be filtered by Category, resource-ID, name etc.</span></span>

## <span data-ttu-id="e43e8-110">示例</span><span class="sxs-lookup"><span data-stu-id="e43e8-110">EXAMPLES</span></span>

### <span data-ttu-id="e43e8-111">範例1</span><span class="sxs-lookup"><span data-stu-id="e43e8-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAdvisorRecommendation
ResourceId                   : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommen
                       dations/{recommendation-Id}
Category             : Performance
ExtendedProperties   : {}
Impact               : Medium
ImpactedField        : Microsoft.Cache/Redis
ImpactedValue        : azacache
LastUpdated          : 12/5/2018 4:45:55 PM
Metadata             : {}
RecommendationTypeId : 905a0026-8010-45b2-ab46-a92c3e4a5131
Risk                 : None
ShortDescription     : Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsRecommendationBaseShortDescription
SuppressionIds       : {}
Name                 : {recommendation-Id}
Type                 : Microsoft.Advisor/recommendations
```
<span data-ttu-id="e43e8-112">取得所有建議的清單。</span><span class="sxs-lookup"><span data-stu-id="e43e8-112">Gets the list of all recommendations.</span></span>

### <span data-ttu-id="e43e8-113">範例2</span><span class="sxs-lookup"><span data-stu-id="e43e8-113">Example 2</span></span>
```powershell
PS C:\> Get-AzAdvisorRecommendation -Category Performance
ResourceId                   : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommen
                       dations/{recommendation-Id}
Category             : Performance
ExtendedProperties   : {}
Impact               : Medium
ImpactedField        : Microsoft.Cache/Redis
ImpactedValue        : azacache
LastUpdated          : 12/5/2018 4:45:55 PM
Metadata             : {}
RecommendationTypeId : 905a0026-8010-45b2-ab46-a92c3e4a5131
Risk                 : None
ShortDescription     : Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsRecommendationBaseShortDescription
SuppressionIds       : {}
Name                 : {recommendation-Id}
Type                 : Microsoft.Advisor/recommendations
```
<span data-ttu-id="e43e8-114">取得依類別效能篩選的所有建議的清單。</span><span class="sxs-lookup"><span data-stu-id="e43e8-114">Gets the list of all recommendations filtered by category Performance.</span></span>

## <span data-ttu-id="e43e8-115">參數</span><span class="sxs-lookup"><span data-stu-id="e43e8-115">PARAMETERS</span></span>

### <span data-ttu-id="e43e8-116">-類別</span><span class="sxs-lookup"><span data-stu-id="e43e8-116">-Category</span></span>
<span data-ttu-id="e43e8-117">建議類別</span><span class="sxs-lookup"><span data-stu-id="e43e8-117">Category of the recommendation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Cost, HighAvailability, Performance, Security, OperationalExcellence

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e43e8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e43e8-118">-DefaultProfile</span></span>
<span data-ttu-id="e43e8-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e43e8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e43e8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e43e8-120">-ResourceGroupName</span></span>
<span data-ttu-id="e43e8-121">建議的 ResourceGroup 名稱</span><span class="sxs-lookup"><span data-stu-id="e43e8-121">ResourceGroup name of the recommendation</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e43e8-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e43e8-122">-ResourceId</span></span>
<span data-ttu-id="e43e8-123">建議的 ResourceId</span><span class="sxs-lookup"><span data-stu-id="e43e8-123">ResourceId of the recommendation</span></span>

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

### <span data-ttu-id="e43e8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e43e8-124">CommonParameters</span></span>
<span data-ttu-id="e43e8-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e43e8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e43e8-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e43e8-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e43e8-127">輸入</span><span class="sxs-lookup"><span data-stu-id="e43e8-127">INPUTS</span></span>

### <span data-ttu-id="e43e8-128">System.object</span><span class="sxs-lookup"><span data-stu-id="e43e8-128">System.String</span></span>

## <span data-ttu-id="e43e8-129">輸出</span><span class="sxs-lookup"><span data-stu-id="e43e8-129">OUTPUTS</span></span>

### <span data-ttu-id="e43e8-130">PsAzureAdvisorResourceRecommendationBase 中的 [...]</span><span class="sxs-lookup"><span data-stu-id="e43e8-130">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="e43e8-131">筆記</span><span class="sxs-lookup"><span data-stu-id="e43e8-131">NOTES</span></span>

## <span data-ttu-id="e43e8-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="e43e8-132">RELATED LINKS</span></span>
