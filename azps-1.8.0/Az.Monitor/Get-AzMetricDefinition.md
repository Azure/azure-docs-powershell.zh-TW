---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7915A7AC-5A47-4868-B846-2896BCEBFAB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azmetricdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricDefinition.md
ms.openlocfilehash: e30ae2389d7f597cd667b9d29ab76087a55315cd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93786718"
---
# <span data-ttu-id="bdb7e-101">Get-AzMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="bdb7e-101">Get-AzMetricDefinition</span></span>

## <span data-ttu-id="bdb7e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bdb7e-102">SYNOPSIS</span></span>
<span data-ttu-id="bdb7e-103">取得公制定義。</span><span class="sxs-lookup"><span data-stu-id="bdb7e-103">Gets metric definitions.</span></span>

## <span data-ttu-id="bdb7e-104">句法</span><span class="sxs-lookup"><span data-stu-id="bdb7e-104">SYNTAX</span></span>

```
Get-AzMetricDefinition [-ResourceId] <String> [-MetricName <String[]>] [-MetricNamespace <String>]
 [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bdb7e-105">說明</span><span class="sxs-lookup"><span data-stu-id="bdb7e-105">DESCRIPTION</span></span>
<span data-ttu-id="bdb7e-106">**AzMetricDefinition** Cmdlet 會取得公制定義。</span><span class="sxs-lookup"><span data-stu-id="bdb7e-106">The **Get-AzMetricDefinition** cmdlet gets metric definitions.</span></span>

## <span data-ttu-id="bdb7e-107">示例</span><span class="sxs-lookup"><span data-stu-id="bdb7e-107">EXAMPLES</span></span>

### <span data-ttu-id="bdb7e-108">範例1：取得資源的公制定義</span><span class="sxs-lookup"><span data-stu-id="bdb7e-108">Example 1: Get metric definitions for a resource</span></span>
```
PS C:\>Get-AzMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2"
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

<span data-ttu-id="bdb7e-109">這個命令會取得指定資源的度量值定義。</span><span class="sxs-lookup"><span data-stu-id="bdb7e-109">This command gets the metrics definitions for the specified resource.</span></span>

### <span data-ttu-id="bdb7e-110">範例2：使用詳細的輸出取得公制定義</span><span class="sxs-lookup"><span data-stu-id="bdb7e-110">Example 2: Get metric definitions with detailed output</span></span>
```
PS C:\>Get-AzMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2" -DetailedOutput
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

<span data-ttu-id="bdb7e-111">這個命令會取得 website2 的公制定義。</span><span class="sxs-lookup"><span data-stu-id="bdb7e-111">This command gets the metric definitions for website2.</span></span>
<span data-ttu-id="bdb7e-112">輸出是詳細的。</span><span class="sxs-lookup"><span data-stu-id="bdb7e-112">The output is detailed.</span></span>

### <span data-ttu-id="bdb7e-113">範例3：依名稱取得公制定義</span><span class="sxs-lookup"><span data-stu-id="bdb7e-113">Example 3: Get metric definitions by name</span></span>
```
PS C:\>Get-AzMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2" -DetailedOutput -MetricNames "BytesSent,CpuTime"
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

<span data-ttu-id="bdb7e-114">這個命令會取得 BytesSent 和 CpuTime 指標的定義。</span><span class="sxs-lookup"><span data-stu-id="bdb7e-114">This command gets definitions for the BytesSent and CpuTime metrics.</span></span>
<span data-ttu-id="bdb7e-115">輸出是詳細的。</span><span class="sxs-lookup"><span data-stu-id="bdb7e-115">The output is detailed.</span></span>

## <span data-ttu-id="bdb7e-116">參數</span><span class="sxs-lookup"><span data-stu-id="bdb7e-116">PARAMETERS</span></span>

### <span data-ttu-id="bdb7e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdb7e-117">-DefaultProfile</span></span>
<span data-ttu-id="bdb7e-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="bdb7e-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdb7e-119">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="bdb7e-119">-DetailedOutput</span></span>
<span data-ttu-id="bdb7e-120">表示此操作包含詳細的輸出。</span><span class="sxs-lookup"><span data-stu-id="bdb7e-120">Indicates that this operation included detailed output.</span></span>
<span data-ttu-id="bdb7e-121">如果您沒有指定此參數，則會匯總輸出。</span><span class="sxs-lookup"><span data-stu-id="bdb7e-121">If you do not specify this parameter, the output is summarized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdb7e-122">-MetricName</span><span class="sxs-lookup"><span data-stu-id="bdb7e-122">-MetricName</span></span>
<span data-ttu-id="bdb7e-123">指定度量單位名稱的陣列。</span><span class="sxs-lookup"><span data-stu-id="bdb7e-123">Specifies an array of names of metrics.</span></span>

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

### <span data-ttu-id="bdb7e-124">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="bdb7e-124">-MetricNamespace</span></span>
<span data-ttu-id="bdb7e-125">指定要為其查詢規格定義的度量命名空間。</span><span class="sxs-lookup"><span data-stu-id="bdb7e-125">Specifies the metric namespace to query metric definitions for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdb7e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bdb7e-126">-ResourceId</span></span>
<span data-ttu-id="bdb7e-127">指定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="bdb7e-127">Specifies the resource ID.</span></span>

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

### <span data-ttu-id="bdb7e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdb7e-128">CommonParameters</span></span>
<span data-ttu-id="bdb7e-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bdb7e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdb7e-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bdb7e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdb7e-131">輸入</span><span class="sxs-lookup"><span data-stu-id="bdb7e-131">INPUTS</span></span>

### <span data-ttu-id="bdb7e-132">System.object</span><span class="sxs-lookup"><span data-stu-id="bdb7e-132">System.String</span></span>

### <span data-ttu-id="bdb7e-133">System.object []</span><span class="sxs-lookup"><span data-stu-id="bdb7e-133">System.String[]</span></span>

## <span data-ttu-id="bdb7e-134">輸出</span><span class="sxs-lookup"><span data-stu-id="bdb7e-134">OUTPUTS</span></span>

### <span data-ttu-id="bdb7e-135">PSMetricDefinition 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="bdb7e-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDefinition</span></span>

## <span data-ttu-id="bdb7e-136">筆記</span><span class="sxs-lookup"><span data-stu-id="bdb7e-136">NOTES</span></span>

## <span data-ttu-id="bdb7e-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="bdb7e-137">RELATED LINKS</span></span>

<span data-ttu-id="bdb7e-138">[AzMetric](./Get-AzMetric.md) 
[新-AzMetricFilter](./New-AzMetricFilter.md)</span><span class="sxs-lookup"><span data-stu-id="bdb7e-138">[Get-AzMetric](./Get-AzMetric.md)
[New-AzMetricFilter](./New-AzMetricFilter.md)</span></span>


