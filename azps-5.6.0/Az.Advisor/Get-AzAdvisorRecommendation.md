---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/powershell/module/az.advisor/get-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorRecommendation.md
ms.openlocfilehash: 9d45db213cf3569837c6b35284c95dc9a076a381
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905673"
---
# <span data-ttu-id="b1217-101">Get-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="b1217-101">Get-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="b1217-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b1217-102">SYNOPSIS</span></span>
<span data-ttu-id="b1217-103">獲得 Azure 建議程式建議清單。</span><span class="sxs-lookup"><span data-stu-id="b1217-103">Gets a list of Azure Advisor recommendations.</span></span>

## <span data-ttu-id="b1217-104">語法</span><span class="sxs-lookup"><span data-stu-id="b1217-104">SYNTAX</span></span>

### <span data-ttu-id="b1217-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b1217-105">NameParameterSet (Default)</span></span>
```
Get-AzAdvisorRecommendation [-Category <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1217-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1217-106">IdParameterSet</span></span>
```
Get-AzAdvisorRecommendation [-ResourceId] <String> [-Category <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1217-107">描述</span><span class="sxs-lookup"><span data-stu-id="b1217-107">DESCRIPTION</span></span>
<span data-ttu-id="b1217-108">取得 Azure 建議程式建議清單。</span><span class="sxs-lookup"><span data-stu-id="b1217-108">Obtains the list of Azure Advisor recommendations.</span></span> <span data-ttu-id="b1217-109">可以根據類別、資源識別碼、名稱等進行篩選。</span><span class="sxs-lookup"><span data-stu-id="b1217-109">Can be filtered by Category, resource-ID, name etc.</span></span>

## <span data-ttu-id="b1217-110">例子</span><span class="sxs-lookup"><span data-stu-id="b1217-110">EXAMPLES</span></span>

### <span data-ttu-id="b1217-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="b1217-111">Example 1</span></span>
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
<span data-ttu-id="b1217-112">獲得所有建議的清單。</span><span class="sxs-lookup"><span data-stu-id="b1217-112">Gets the list of all recommendations.</span></span>

### <span data-ttu-id="b1217-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="b1217-113">Example 2</span></span>
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
<span data-ttu-id="b1217-114">根據類別 Performance 篩選所有建議的清單。</span><span class="sxs-lookup"><span data-stu-id="b1217-114">Gets the list of all recommendations filtered by category Performance.</span></span>

## <span data-ttu-id="b1217-115">參數</span><span class="sxs-lookup"><span data-stu-id="b1217-115">PARAMETERS</span></span>

### <span data-ttu-id="b1217-116">-類別</span><span class="sxs-lookup"><span data-stu-id="b1217-116">-Category</span></span>
<span data-ttu-id="b1217-117">建議類別</span><span class="sxs-lookup"><span data-stu-id="b1217-117">Category of the recommendation</span></span>

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

### <span data-ttu-id="b1217-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1217-118">-DefaultProfile</span></span>
<span data-ttu-id="b1217-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b1217-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1217-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1217-120">-ResourceGroupName</span></span>
<span data-ttu-id="b1217-121">建議的資源組名稱</span><span class="sxs-lookup"><span data-stu-id="b1217-121">ResourceGroup name of the recommendation</span></span>

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

### <span data-ttu-id="b1217-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1217-122">-ResourceId</span></span>
<span data-ttu-id="b1217-123">建議中的 ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1217-123">ResourceId of the recommendation</span></span>

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

### <span data-ttu-id="b1217-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1217-124">CommonParameters</span></span>
<span data-ttu-id="b1217-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b1217-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b1217-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="b1217-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1217-127">輸入</span><span class="sxs-lookup"><span data-stu-id="b1217-127">INPUTS</span></span>

### <span data-ttu-id="b1217-128">System.String</span><span class="sxs-lookup"><span data-stu-id="b1217-128">System.String</span></span>

## <span data-ttu-id="b1217-129">輸出</span><span class="sxs-lookup"><span data-stu-id="b1217-129">OUTPUTS</span></span>

### <span data-ttu-id="b1217-130">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="b1217-130">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="b1217-131">筆記</span><span class="sxs-lookup"><span data-stu-id="b1217-131">NOTES</span></span>

## <span data-ttu-id="b1217-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="b1217-132">RELATED LINKS</span></span>
