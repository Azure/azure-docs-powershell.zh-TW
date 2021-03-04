---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7915A7AC-5A47-4868-B846-2896BCEBFAB2
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azmetricdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricDefinition.md
ms.openlocfilehash: 3e1038fc44acc1e3834ee10a1fd08bb49c35cd82
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908906"
---
# <span data-ttu-id="90ae7-101">Get-AzMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="90ae7-101">Get-AzMetricDefinition</span></span>

## <span data-ttu-id="90ae7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="90ae7-102">SYNOPSIS</span></span>
<span data-ttu-id="90ae7-103">獲得公制定義。</span><span class="sxs-lookup"><span data-stu-id="90ae7-103">Gets metric definitions.</span></span>

## <span data-ttu-id="90ae7-104">語法</span><span class="sxs-lookup"><span data-stu-id="90ae7-104">SYNTAX</span></span>

```
Get-AzMetricDefinition [-ResourceId] <String> [-MetricName <String[]>] [-MetricNamespace <String>]
 [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90ae7-105">描述</span><span class="sxs-lookup"><span data-stu-id="90ae7-105">DESCRIPTION</span></span>
<span data-ttu-id="90ae7-106">**Get-AzMetricDefinition** Cmdlet 會取得公制定義。</span><span class="sxs-lookup"><span data-stu-id="90ae7-106">The **Get-AzMetricDefinition** cmdlet gets metric definitions.</span></span>

## <span data-ttu-id="90ae7-107">例子</span><span class="sxs-lookup"><span data-stu-id="90ae7-107">EXAMPLES</span></span>

### <span data-ttu-id="90ae7-108">範例 1：取得資源的公制定義</span><span class="sxs-lookup"><span data-stu-id="90ae7-108">Example 1: Get metric definitions for a resource</span></span>
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

<span data-ttu-id="90ae7-109">此命令會獲得指定資源的度量定義。</span><span class="sxs-lookup"><span data-stu-id="90ae7-109">This command gets the metrics definitions for the specified resource.</span></span>

### <span data-ttu-id="90ae7-110">範例 2：取得具有詳細輸出的公制定義</span><span class="sxs-lookup"><span data-stu-id="90ae7-110">Example 2: Get metric definitions with detailed output</span></span>
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

<span data-ttu-id="90ae7-111">此命令會獲得網站 2 的度量定義。</span><span class="sxs-lookup"><span data-stu-id="90ae7-111">This command gets the metric definitions for website2.</span></span>
<span data-ttu-id="90ae7-112">輸出為詳細資料。</span><span class="sxs-lookup"><span data-stu-id="90ae7-112">The output is detailed.</span></span>

### <span data-ttu-id="90ae7-113">範例 3：根據名稱取得公制定義</span><span class="sxs-lookup"><span data-stu-id="90ae7-113">Example 3: Get metric definitions by name</span></span>
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

<span data-ttu-id="90ae7-114">此命令會獲得 BytesSent 和 CpuTime 度量的定義。</span><span class="sxs-lookup"><span data-stu-id="90ae7-114">This command gets definitions for the BytesSent and CpuTime metrics.</span></span>
<span data-ttu-id="90ae7-115">輸出為詳細資料。</span><span class="sxs-lookup"><span data-stu-id="90ae7-115">The output is detailed.</span></span>

## <span data-ttu-id="90ae7-116">參數</span><span class="sxs-lookup"><span data-stu-id="90ae7-116">PARAMETERS</span></span>

### <span data-ttu-id="90ae7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90ae7-117">-DefaultProfile</span></span>
<span data-ttu-id="90ae7-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="90ae7-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="90ae7-119">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="90ae7-119">-DetailedOutput</span></span>
<span data-ttu-id="90ae7-120">表示此作業包含詳細輸出。</span><span class="sxs-lookup"><span data-stu-id="90ae7-120">Indicates that this operation included detailed output.</span></span>
<span data-ttu-id="90ae7-121">如果您未指定此參數，輸出會摘要顯示。</span><span class="sxs-lookup"><span data-stu-id="90ae7-121">If you do not specify this parameter, the output is summarized.</span></span>

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

### <span data-ttu-id="90ae7-122">-MetricName</span><span class="sxs-lookup"><span data-stu-id="90ae7-122">-MetricName</span></span>
<span data-ttu-id="90ae7-123">指定度量名稱的陣列。</span><span class="sxs-lookup"><span data-stu-id="90ae7-123">Specifies an array of names of metrics.</span></span>

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

### <span data-ttu-id="90ae7-124">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="90ae7-124">-MetricNamespace</span></span>
<span data-ttu-id="90ae7-125">指定查詢計量定義的公制命名空間。</span><span class="sxs-lookup"><span data-stu-id="90ae7-125">Specifies the metric namespace to query metric definitions for.</span></span>

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

### <span data-ttu-id="90ae7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="90ae7-126">-ResourceId</span></span>
<span data-ttu-id="90ae7-127">指定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="90ae7-127">Specifies the resource ID.</span></span>

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

### <span data-ttu-id="90ae7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90ae7-128">CommonParameters</span></span>
<span data-ttu-id="90ae7-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="90ae7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90ae7-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="90ae7-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90ae7-131">輸入</span><span class="sxs-lookup"><span data-stu-id="90ae7-131">INPUTS</span></span>

### <span data-ttu-id="90ae7-132">System.String</span><span class="sxs-lookup"><span data-stu-id="90ae7-132">System.String</span></span>

### <span data-ttu-id="90ae7-133">System.String[]</span><span class="sxs-lookup"><span data-stu-id="90ae7-133">System.String[]</span></span>

## <span data-ttu-id="90ae7-134">輸出</span><span class="sxs-lookup"><span data-stu-id="90ae7-134">OUTPUTS</span></span>

### <span data-ttu-id="90ae7-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="90ae7-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDefinition</span></span>

## <span data-ttu-id="90ae7-136">筆記</span><span class="sxs-lookup"><span data-stu-id="90ae7-136">NOTES</span></span>

<span data-ttu-id="90ae7-137">有關支援之計量的資訊，請參閱： https://docs.microsoft.com/azure/azure-monitor/platform/metrics-supported</span><span class="sxs-lookup"><span data-stu-id="90ae7-137">More information about the supported metrics may be found at: https://docs.microsoft.com/azure/azure-monitor/platform/metrics-supported</span></span>

## <span data-ttu-id="90ae7-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="90ae7-138">RELATED LINKS</span></span>

<span data-ttu-id="90ae7-139">[Get-AzMetric](./Get-AzMetric.md) 
[New-AzMetricFilter](./New-AzMetricFilter.md)</span><span class="sxs-lookup"><span data-stu-id="90ae7-139">[Get-AzMetric](./Get-AzMetric.md)
[New-AzMetricFilter](./New-AzMetricFilter.md)</span></span>


