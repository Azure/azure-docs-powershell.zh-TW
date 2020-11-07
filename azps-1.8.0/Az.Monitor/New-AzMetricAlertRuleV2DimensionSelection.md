---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2dimensionselection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
ms.openlocfilehash: 349677b4686b2df5a72f233b729a5028dc322057
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93786678"
---
# <span data-ttu-id="8c283-101">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="8c283-101">New-AzMetricAlertRuleV2DimensionSelection</span></span>

## <span data-ttu-id="8c283-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8c283-102">SYNOPSIS</span></span>
<span data-ttu-id="8c283-103">建立可用於構造標準警示準則的局部維度選擇物件。</span><span class="sxs-lookup"><span data-stu-id="8c283-103">Creates a local dimension selection object that can be used to construct a metric alert criteria.</span></span>

## <span data-ttu-id="8c283-104">句法</span><span class="sxs-lookup"><span data-stu-id="8c283-104">SYNTAX</span></span>

```
New-AzMetricAlertRuleV2DimensionSelection -DimensionName <String> -ValuesToInclude <String[]>
 [-ValuesToExclude <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c283-105">說明</span><span class="sxs-lookup"><span data-stu-id="8c283-105">DESCRIPTION</span></span>
<span data-ttu-id="8c283-106">**AzMetricAlertRuleV2DimensionSelection** Cmdlet 會建立局部維度選取物件，以協助使用 **新的-AzMetricAlertRuleV2Criteria** Cmdlet 來構造公制警報準則。</span><span class="sxs-lookup"><span data-stu-id="8c283-106">The **New-AzMetricAlertRuleV2DimensionSelection** cmdlet creates a local dimension selection object to help with the construction of metric alert criteria using **New-AzMetricAlertRuleV2Criteria** cmdlet.</span></span>

## <span data-ttu-id="8c283-107">示例</span><span class="sxs-lookup"><span data-stu-id="8c283-107">EXAMPLES</span></span>

### <span data-ttu-id="8c283-108">範例1：建立維度選取物件</span><span class="sxs-lookup"><span data-stu-id="8c283-108">Example 1 : Create a dimension selection object</span></span>

```powershell
PS C:\> New-AzMetricAlertRuleV2DimensionSelection -DimensionName LUN -ValuesToInclude 1,3,4

Dimension IncludeValues ExcludeValues
--------- ------------- -------------
LUN       {1, 3, 4}     
```

<span data-ttu-id="8c283-109">這個命令會建立一個維度選取物件，指定 {1,3,4} 需要選取維度 "LUN" 的值</span><span class="sxs-lookup"><span data-stu-id="8c283-109">This command creates a dimension selection object that specifies that values {1,3,4} need to be selected for Dimension "LUN"</span></span>

## <span data-ttu-id="8c283-110">參數</span><span class="sxs-lookup"><span data-stu-id="8c283-110">PARAMETERS</span></span>

### <span data-ttu-id="8c283-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c283-111">-DefaultProfile</span></span>
<span data-ttu-id="8c283-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8c283-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c283-113">-DimensionName</span><span class="sxs-lookup"><span data-stu-id="8c283-113">-DimensionName</span></span>
<span data-ttu-id="8c283-114">維度名稱</span><span class="sxs-lookup"><span data-stu-id="8c283-114">The Dimension name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c283-115">-ValuesToExclude</span><span class="sxs-lookup"><span data-stu-id="8c283-115">-ValuesToExclude</span></span>
<span data-ttu-id="8c283-116">ExcludeValues</span><span class="sxs-lookup"><span data-stu-id="8c283-116">The ExcludeValues</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c283-117">-ValuesToInclude</span><span class="sxs-lookup"><span data-stu-id="8c283-117">-ValuesToInclude</span></span>
<span data-ttu-id="8c283-118">IncludeValues</span><span class="sxs-lookup"><span data-stu-id="8c283-118">The IncludeValues</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c283-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c283-119">CommonParameters</span></span>
<span data-ttu-id="8c283-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8c283-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="8c283-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8c283-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c283-122">輸入</span><span class="sxs-lookup"><span data-stu-id="8c283-122">INPUTS</span></span>

### <span data-ttu-id="8c283-123">System.object</span><span class="sxs-lookup"><span data-stu-id="8c283-123">System.String</span></span>

### <span data-ttu-id="8c283-124">System.object []</span><span class="sxs-lookup"><span data-stu-id="8c283-124">System.String[]</span></span>

## <span data-ttu-id="8c283-125">輸出</span><span class="sxs-lookup"><span data-stu-id="8c283-125">OUTPUTS</span></span>

### <span data-ttu-id="8c283-126">PSMetricDimension 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="8c283-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension</span></span>

## <span data-ttu-id="8c283-127">筆記</span><span class="sxs-lookup"><span data-stu-id="8c283-127">NOTES</span></span>

## <span data-ttu-id="8c283-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="8c283-128">RELATED LINKS</span></span>