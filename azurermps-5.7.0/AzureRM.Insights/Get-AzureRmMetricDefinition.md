---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7915A7AC-5A47-4868-B846-2896BCEBFAB2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermmetricdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetricDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetricDefinition.md
ms.openlocfilehash: de839f4b56f4aa1111e130bdf6396875f9aeb185
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449364"
---
# <span data-ttu-id="538c2-101">Get-AzureRmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="538c2-101">Get-AzureRmMetricDefinition</span></span>

## <span data-ttu-id="538c2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="538c2-102">SYNOPSIS</span></span>
<span data-ttu-id="538c2-103">取得公制定義。</span><span class="sxs-lookup"><span data-stu-id="538c2-103">Gets metric definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="538c2-104">句法</span><span class="sxs-lookup"><span data-stu-id="538c2-104">SYNTAX</span></span>

```
Get-AzureRmMetricDefinition [-ResourceId] <String> [-MetricName <String[]>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="538c2-105">說明</span><span class="sxs-lookup"><span data-stu-id="538c2-105">DESCRIPTION</span></span>
<span data-ttu-id="538c2-106">**AzureRmMetricDefinition** Cmdlet 會取得公制定義。</span><span class="sxs-lookup"><span data-stu-id="538c2-106">The **Get-AzureRmMetricDefinition** cmdlet gets metric definitions.</span></span>

## <span data-ttu-id="538c2-107">示例</span><span class="sxs-lookup"><span data-stu-id="538c2-107">EXAMPLES</span></span>

### <span data-ttu-id="538c2-108">範例1：取得資源的公制定義</span><span class="sxs-lookup"><span data-stu-id="538c2-108">Example 1: Get metric definitions for a resource</span></span>
```
PS C:\>Get-AzureRmMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2"
Name                   : CpuTime
Dimensions             : {}
MetricAvailabilities   : {Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability}
PrimaryAggregationType : Total
Properties             : {}
ResourceUri            : 
Unit                   : Seconds
Name                   : Requests
Dimensions             : {}
MetricAvailabilities   : {Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability}
PrimaryAggregationType : Total
Properties             : {}
ResourceUri            : 
Unit                   : Count
```

<span data-ttu-id="538c2-109">這個命令會取得指定資源的度量值定義。</span><span class="sxs-lookup"><span data-stu-id="538c2-109">This command gets the metrics definitions for the specified resource.</span></span>

### <span data-ttu-id="538c2-110">範例2：使用詳細的輸出取得公制定義</span><span class="sxs-lookup"><span data-stu-id="538c2-110">Example 2: Get metric definitions with detailed output</span></span>
```
PS C:\>Get-AzureRmMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2" -DetailedOutput
Dimensions             : 
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : CpuTime
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Seconds
Dimensions             : 
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : Requests
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Count
```

<span data-ttu-id="538c2-111">這個命令會取得 website2 的公制定義。</span><span class="sxs-lookup"><span data-stu-id="538c2-111">This command gets the metric definitions for website2.</span></span>
<span data-ttu-id="538c2-112">輸出是詳細的。</span><span class="sxs-lookup"><span data-stu-id="538c2-112">The output is detailed.</span></span>

### <span data-ttu-id="538c2-113">範例3：依名稱取得公制定義</span><span class="sxs-lookup"><span data-stu-id="538c2-113">Example 3: Get metric definitions by name</span></span>
```
PS C:\>Get-AzureRmMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2" -DetailedOutput -MetricNames "BytesSent,CpuTime"
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : CpuTime
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Seconds
Dimensions             : 
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : BytesSent
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Bytes
```

<span data-ttu-id="538c2-114">這個命令會取得 BytesSent 和 CpuTime 指標的定義。</span><span class="sxs-lookup"><span data-stu-id="538c2-114">This command gets definitions for the BytesSent and CpuTime metrics.</span></span>
<span data-ttu-id="538c2-115">輸出是詳細的。</span><span class="sxs-lookup"><span data-stu-id="538c2-115">The output is detailed.</span></span>

## <span data-ttu-id="538c2-116">參數</span><span class="sxs-lookup"><span data-stu-id="538c2-116">PARAMETERS</span></span>

### <span data-ttu-id="538c2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="538c2-117">-DefaultProfile</span></span>
<span data-ttu-id="538c2-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="538c2-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="538c2-119">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="538c2-119">-DetailedOutput</span></span>
<span data-ttu-id="538c2-120">表示此操作包含詳細的輸出。</span><span class="sxs-lookup"><span data-stu-id="538c2-120">Indicates that this operation included detailed output.</span></span>
<span data-ttu-id="538c2-121">如果您沒有指定此參數，則會匯總輸出。</span><span class="sxs-lookup"><span data-stu-id="538c2-121">If you do not specify this parameter, the output is summarized.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="538c2-122">-MetricName</span><span class="sxs-lookup"><span data-stu-id="538c2-122">-MetricName</span></span>
<span data-ttu-id="538c2-123">指定度量單位名稱的陣列。</span><span class="sxs-lookup"><span data-stu-id="538c2-123">Specifies an array of names of metrics.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: MetricNames

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="538c2-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="538c2-124">-ResourceId</span></span>
<span data-ttu-id="538c2-125">指定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="538c2-125">Specifies the resource ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="538c2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="538c2-126">CommonParameters</span></span>
<span data-ttu-id="538c2-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="538c2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="538c2-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="538c2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="538c2-129">輸入</span><span class="sxs-lookup"><span data-stu-id="538c2-129">INPUTS</span></span>

### <span data-ttu-id="538c2-130">所有</span><span class="sxs-lookup"><span data-stu-id="538c2-130">None</span></span>
<span data-ttu-id="538c2-131">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="538c2-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="538c2-132">輸出</span><span class="sxs-lookup"><span data-stu-id="538c2-132">OUTPUTS</span></span>

### <span data-ttu-id="538c2-133">PSMetricDefinition [] 的 OutputClasses []</span><span class="sxs-lookup"><span data-stu-id="538c2-133">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDefinition[]</span></span>

## <span data-ttu-id="538c2-134">筆記</span><span class="sxs-lookup"><span data-stu-id="538c2-134">NOTES</span></span>

## <span data-ttu-id="538c2-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="538c2-135">RELATED LINKS</span></span>

[<span data-ttu-id="538c2-136">AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="538c2-136">Get-AzureRmMetric</span></span>](./Get-AzureRmMetric.md)


