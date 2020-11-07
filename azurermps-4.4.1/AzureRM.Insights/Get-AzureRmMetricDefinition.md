---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7915A7AC-5A47-4868-B846-2896BCEBFAB2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetricDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetricDefinition.md
ms.openlocfilehash: 4cb978b33b6bcb68d400f33fb2da06747ce9b763
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625175"
---
# <span data-ttu-id="fe4c6-101">Get-AzureRmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="fe4c6-101">Get-AzureRmMetricDefinition</span></span>

## <span data-ttu-id="fe4c6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fe4c6-102">SYNOPSIS</span></span>
<span data-ttu-id="fe4c6-103">取得公制定義。</span><span class="sxs-lookup"><span data-stu-id="fe4c6-103">Gets metric definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe4c6-104">句法</span><span class="sxs-lookup"><span data-stu-id="fe4c6-104">SYNTAX</span></span>

```
Get-AzureRmMetricDefinition [-ResourceId] <String> [-MetricNames <String[]>] [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe4c6-105">說明</span><span class="sxs-lookup"><span data-stu-id="fe4c6-105">DESCRIPTION</span></span>
<span data-ttu-id="fe4c6-106">**AzureRmMetricDefinition** Cmdlet 會取得公制定義。</span><span class="sxs-lookup"><span data-stu-id="fe4c6-106">The **Get-AzureRmMetricDefinition** cmdlet gets metric definitions.</span></span>

## <span data-ttu-id="fe4c6-107">示例</span><span class="sxs-lookup"><span data-stu-id="fe4c6-107">EXAMPLES</span></span>

### <span data-ttu-id="fe4c6-108">範例1：取得資源的公制定義</span><span class="sxs-lookup"><span data-stu-id="fe4c6-108">Example 1: Get metric definitions for a resource</span></span>
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

<span data-ttu-id="fe4c6-109">這個命令會取得指定資源的度量值定義。</span><span class="sxs-lookup"><span data-stu-id="fe4c6-109">This command gets the metrics definitions for the specified resource.</span></span>

### <span data-ttu-id="fe4c6-110">範例2：使用詳細的輸出取得公制定義</span><span class="sxs-lookup"><span data-stu-id="fe4c6-110">Example 2: Get metric definitions with detailed output</span></span>
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

<span data-ttu-id="fe4c6-111">這個命令會取得 website2 的公制定義。</span><span class="sxs-lookup"><span data-stu-id="fe4c6-111">This command gets the metric definitions for website2.</span></span>
<span data-ttu-id="fe4c6-112">輸出是詳細的。</span><span class="sxs-lookup"><span data-stu-id="fe4c6-112">The output is detailed.</span></span>

### <span data-ttu-id="fe4c6-113">範例3：依名稱取得公制定義</span><span class="sxs-lookup"><span data-stu-id="fe4c6-113">Example 3: Get metric definitions by name</span></span>
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

<span data-ttu-id="fe4c6-114">這個命令會取得 BytesSent 和 CpuTime 指標的定義。</span><span class="sxs-lookup"><span data-stu-id="fe4c6-114">This command gets definitions for the BytesSent and CpuTime metrics.</span></span>
<span data-ttu-id="fe4c6-115">輸出是詳細的。</span><span class="sxs-lookup"><span data-stu-id="fe4c6-115">The output is detailed.</span></span>

## <span data-ttu-id="fe4c6-116">參數</span><span class="sxs-lookup"><span data-stu-id="fe4c6-116">PARAMETERS</span></span>

### <span data-ttu-id="fe4c6-117">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="fe4c6-117">-DetailedOutput</span></span>
<span data-ttu-id="fe4c6-118">表示此操作包含詳細的輸出。</span><span class="sxs-lookup"><span data-stu-id="fe4c6-118">Indicates that this operation included detailed output.</span></span>
<span data-ttu-id="fe4c6-119">如果您沒有指定此參數，則會匯總輸出。</span><span class="sxs-lookup"><span data-stu-id="fe4c6-119">If you do not specify this parameter, the output is summarized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe4c6-120">-MetricNames</span><span class="sxs-lookup"><span data-stu-id="fe4c6-120">-MetricNames</span></span>
<span data-ttu-id="fe4c6-121">指定度量單位名稱的陣列。</span><span class="sxs-lookup"><span data-stu-id="fe4c6-121">Specifies an array of names of metrics.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe4c6-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe4c6-122">-ResourceId</span></span>
<span data-ttu-id="fe4c6-123">指定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="fe4c6-123">Specifies the resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe4c6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe4c6-124">-DefaultProfile</span></span>
<span data-ttu-id="fe4c6-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fe4c6-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe4c6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe4c6-126">CommonParameters</span></span>
<span data-ttu-id="fe4c6-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fe4c6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe4c6-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fe4c6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe4c6-129">輸入</span><span class="sxs-lookup"><span data-stu-id="fe4c6-129">INPUTS</span></span>

## <span data-ttu-id="fe4c6-130">輸出</span><span class="sxs-lookup"><span data-stu-id="fe4c6-130">OUTPUTS</span></span>

### <span data-ttu-id="fe4c6-131">PSMetricDefinition [] 的 OutputClasses []</span><span class="sxs-lookup"><span data-stu-id="fe4c6-131">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDefinition[]</span></span>

## <span data-ttu-id="fe4c6-132">筆記</span><span class="sxs-lookup"><span data-stu-id="fe4c6-132">NOTES</span></span>

## <span data-ttu-id="fe4c6-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="fe4c6-133">RELATED LINKS</span></span>

[<span data-ttu-id="fe4c6-134">AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="fe4c6-134">Get-AzureRmMetric</span></span>](./Get-AzureRmMetric.md)


