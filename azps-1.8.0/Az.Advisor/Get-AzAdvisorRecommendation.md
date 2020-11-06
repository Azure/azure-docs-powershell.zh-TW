---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/get-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorRecommendation.md
ms.openlocfilehash: 894fc2b3f3e722c7924e05e6c700ae03f741562f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93611701"
---
# <span data-ttu-id="13759-101">Get-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="13759-101">Get-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="13759-102">摘要</span><span class="sxs-lookup"><span data-stu-id="13759-102">SYNOPSIS</span></span>
<span data-ttu-id="13759-103">取得 Azure Advisor 建議的清單。</span><span class="sxs-lookup"><span data-stu-id="13759-103">Gets a list of Azure Advisor recommendations.</span></span>

## <span data-ttu-id="13759-104">句法</span><span class="sxs-lookup"><span data-stu-id="13759-104">SYNTAX</span></span>

### <span data-ttu-id="13759-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="13759-105">NameParameterSet (Default)</span></span>
```
Get-AzAdvisorRecommendation [-Category <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13759-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="13759-106">IdParameterSet</span></span>
```
Get-AzAdvisorRecommendation [-ResourceId] <String> [-Category <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13759-107">說明</span><span class="sxs-lookup"><span data-stu-id="13759-107">DESCRIPTION</span></span>
<span data-ttu-id="13759-108">獲取 Azure Advisor 建議清單。</span><span class="sxs-lookup"><span data-stu-id="13759-108">Obtains the list of Azure Advisor recommendations.</span></span> <span data-ttu-id="13759-109">可以依據類別、資源識別碼、名稱等進行篩選。</span><span class="sxs-lookup"><span data-stu-id="13759-109">Can be filtered by Category, resource-ID, name etc.</span></span>

## <span data-ttu-id="13759-110">示例</span><span class="sxs-lookup"><span data-stu-id="13759-110">EXAMPLES</span></span>

### <span data-ttu-id="13759-111">範例1</span><span class="sxs-lookup"><span data-stu-id="13759-111">Example 1</span></span>
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
<span data-ttu-id="13759-112">取得所有建議的清單。</span><span class="sxs-lookup"><span data-stu-id="13759-112">Gets the list of all recommendations.</span></span>

### <span data-ttu-id="13759-113">範例2</span><span class="sxs-lookup"><span data-stu-id="13759-113">Example 2</span></span>
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
<span data-ttu-id="13759-114">取得依類別效能篩選的所有建議的清單。</span><span class="sxs-lookup"><span data-stu-id="13759-114">Gets the list of all recommendations filtered by category Performance.</span></span>

## <span data-ttu-id="13759-115">參數</span><span class="sxs-lookup"><span data-stu-id="13759-115">PARAMETERS</span></span>

### <span data-ttu-id="13759-116">-類別</span><span class="sxs-lookup"><span data-stu-id="13759-116">-Category</span></span>
<span data-ttu-id="13759-117">建議類別</span><span class="sxs-lookup"><span data-stu-id="13759-117">Category of the recommendation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Cost, HighAvailability, Performance, Security

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13759-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13759-118">-DefaultProfile</span></span>
<span data-ttu-id="13759-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="13759-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13759-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13759-120">-ResourceGroupName</span></span>
<span data-ttu-id="13759-121">建議的 ResourceGroup 名稱</span><span class="sxs-lookup"><span data-stu-id="13759-121">ResourceGroup name of the recommendation</span></span>

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

### <span data-ttu-id="13759-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13759-122">-ResourceId</span></span>
<span data-ttu-id="13759-123">建議的 ResourceId</span><span class="sxs-lookup"><span data-stu-id="13759-123">ResourceId of the recommendation</span></span>

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

### <span data-ttu-id="13759-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13759-124">CommonParameters</span></span>
<span data-ttu-id="13759-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="13759-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="13759-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="13759-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13759-127">輸入</span><span class="sxs-lookup"><span data-stu-id="13759-127">INPUTS</span></span>

### <span data-ttu-id="13759-128">System.object</span><span class="sxs-lookup"><span data-stu-id="13759-128">System.String</span></span>

## <span data-ttu-id="13759-129">輸出</span><span class="sxs-lookup"><span data-stu-id="13759-129">OUTPUTS</span></span>

### <span data-ttu-id="13759-130">PsAzureAdvisorResourceRecommendationBase 中的 [...]</span><span class="sxs-lookup"><span data-stu-id="13759-130">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="13759-131">筆記</span><span class="sxs-lookup"><span data-stu-id="13759-131">NOTES</span></span>

## <span data-ttu-id="13759-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="13759-132">RELATED LINKS</span></span>
