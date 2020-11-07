---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7915A7AC-5A47-4868-B846-2896BCEBFAB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azmetricdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricDefinition.md
ms.openlocfilehash: 9ca873736ad86eaac17dd2795ad61716197ceaba
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93799165"
---
# <span data-ttu-id="e3ca9-101">Get-AzMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="e3ca9-101">Get-AzMetricDefinition</span></span>

## <span data-ttu-id="e3ca9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e3ca9-102">SYNOPSIS</span></span>
<span data-ttu-id="e3ca9-103">取得公制定義。</span><span class="sxs-lookup"><span data-stu-id="e3ca9-103">Gets metric definitions.</span></span>

## <span data-ttu-id="e3ca9-104">句法</span><span class="sxs-lookup"><span data-stu-id="e3ca9-104">SYNTAX</span></span>

```
Get-AzMetricDefinition [-ResourceId] <String> [-MetricName <String[]>] [-MetricNamespace <String>]
 [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3ca9-105">說明</span><span class="sxs-lookup"><span data-stu-id="e3ca9-105">DESCRIPTION</span></span>
<span data-ttu-id="e3ca9-106">**AzMetricDefinition** Cmdlet 會取得公制定義。</span><span class="sxs-lookup"><span data-stu-id="e3ca9-106">The **Get-AzMetricDefinition** cmdlet gets metric definitions.</span></span>

## <span data-ttu-id="e3ca9-107">示例</span><span class="sxs-lookup"><span data-stu-id="e3ca9-107">EXAMPLES</span></span>

### <span data-ttu-id="e3ca9-108">範例1：取得資源的公制定義</span><span class="sxs-lookup"><span data-stu-id="e3ca9-108">Example 1: Get metric definitions for a resource</span></span>
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

<span data-ttu-id="e3ca9-109">這個命令會取得指定資源的度量值定義。</span><span class="sxs-lookup"><span data-stu-id="e3ca9-109">This command gets the metrics definitions for the specified resource.</span></span>

### <span data-ttu-id="e3ca9-110">範例2：使用詳細的輸出取得公制定義</span><span class="sxs-lookup"><span data-stu-id="e3ca9-110">Example 2: Get metric definitions with detailed output</span></span>
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

<span data-ttu-id="e3ca9-111">這個命令會取得 website2 的公制定義。</span><span class="sxs-lookup"><span data-stu-id="e3ca9-111">This command gets the metric definitions for website2.</span></span>
<span data-ttu-id="e3ca9-112">輸出是詳細的。</span><span class="sxs-lookup"><span data-stu-id="e3ca9-112">The output is detailed.</span></span>

### <span data-ttu-id="e3ca9-113">範例3：依名稱取得公制定義</span><span class="sxs-lookup"><span data-stu-id="e3ca9-113">Example 3: Get metric definitions by name</span></span>
```
PS C:\>Get-AzMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2" -DetailedOutput -MetricName "BytesSent,CpuTime"
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

<span data-ttu-id="e3ca9-114">這個命令會取得 BytesSent 和 CpuTime 指標的定義。</span><span class="sxs-lookup"><span data-stu-id="e3ca9-114">This command gets definitions for the BytesSent and CpuTime metrics.</span></span>
<span data-ttu-id="e3ca9-115">輸出是詳細的。</span><span class="sxs-lookup"><span data-stu-id="e3ca9-115">The output is detailed.</span></span>

## <span data-ttu-id="e3ca9-116">參數</span><span class="sxs-lookup"><span data-stu-id="e3ca9-116">PARAMETERS</span></span>

### <span data-ttu-id="e3ca9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3ca9-117">-DefaultProfile</span></span>
<span data-ttu-id="e3ca9-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e3ca9-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e3ca9-119">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="e3ca9-119">-DetailedOutput</span></span>
<span data-ttu-id="e3ca9-120">表示此操作包含詳細的輸出。</span><span class="sxs-lookup"><span data-stu-id="e3ca9-120">Indicates that this operation included detailed output.</span></span>
<span data-ttu-id="e3ca9-121">如果您沒有指定此參數，則會匯總輸出。</span><span class="sxs-lookup"><span data-stu-id="e3ca9-121">If you do not specify this parameter, the output is summarized.</span></span>

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

### <span data-ttu-id="e3ca9-122">-MetricName</span><span class="sxs-lookup"><span data-stu-id="e3ca9-122">-MetricName</span></span>
<span data-ttu-id="e3ca9-123">指定度量單位名稱的陣列。</span><span class="sxs-lookup"><span data-stu-id="e3ca9-123">Specifies an array of names of metrics.</span></span>

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

### <span data-ttu-id="e3ca9-124">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="e3ca9-124">-MetricNamespace</span></span>
<span data-ttu-id="e3ca9-125">指定要為其查詢規格定義的度量命名空間。</span><span class="sxs-lookup"><span data-stu-id="e3ca9-125">Specifies the metric namespace to query metric definitions for.</span></span>

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

### <span data-ttu-id="e3ca9-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3ca9-126">-ResourceId</span></span>
<span data-ttu-id="e3ca9-127">指定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e3ca9-127">Specifies the resource ID.</span></span>

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

### <span data-ttu-id="e3ca9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3ca9-128">CommonParameters</span></span>
<span data-ttu-id="e3ca9-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e3ca9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3ca9-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e3ca9-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3ca9-131">輸入</span><span class="sxs-lookup"><span data-stu-id="e3ca9-131">INPUTS</span></span>

### <span data-ttu-id="e3ca9-132">System.object</span><span class="sxs-lookup"><span data-stu-id="e3ca9-132">System.String</span></span>

### <span data-ttu-id="e3ca9-133">System.object []</span><span class="sxs-lookup"><span data-stu-id="e3ca9-133">System.String[]</span></span>

## <span data-ttu-id="e3ca9-134">輸出</span><span class="sxs-lookup"><span data-stu-id="e3ca9-134">OUTPUTS</span></span>

### <span data-ttu-id="e3ca9-135">PSMetricDefinition 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="e3ca9-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDefinition</span></span>

## <span data-ttu-id="e3ca9-136">筆記</span><span class="sxs-lookup"><span data-stu-id="e3ca9-136">NOTES</span></span>

<span data-ttu-id="e3ca9-137">您可以在以下網址找到有關支援之指標的詳細資訊： https://docs.microsoft.com/en-us/azure/azure-monitor/platform/metrics-supported</span><span class="sxs-lookup"><span data-stu-id="e3ca9-137">More information about the supported metrics may be found at: https://docs.microsoft.com/en-us/azure/azure-monitor/platform/metrics-supported</span></span>

## <span data-ttu-id="e3ca9-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="e3ca9-138">RELATED LINKS</span></span>

<span data-ttu-id="e3ca9-139">[AzMetric](./Get-AzMetric.md) 
[新-AzMetricFilter](./New-AzMetricFilter.md)</span><span class="sxs-lookup"><span data-stu-id="e3ca9-139">[Get-AzMetric](./Get-AzMetric.md)
[New-AzMetricFilter](./New-AzMetricFilter.md)</span></span>


