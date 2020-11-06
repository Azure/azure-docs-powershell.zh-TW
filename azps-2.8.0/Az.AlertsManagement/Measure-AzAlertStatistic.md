---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/measure-azalertstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Measure-AzAlertStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Measure-AzAlertStatistic.md
ms.openlocfilehash: 1cd4029d9e5bcdf67706784228a8104ed4eb221c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614125"
---
# <span data-ttu-id="a9f88-101">Measure-AzAlertStatistic</span><span class="sxs-lookup"><span data-stu-id="a9f88-101">Measure-AzAlertStatistic</span></span>

## <span data-ttu-id="a9f88-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a9f88-102">SYNOPSIS</span></span>
<span data-ttu-id="a9f88-103">取得警示摘要資訊</span><span class="sxs-lookup"><span data-stu-id="a9f88-103">Gets Alert Summary Information</span></span>

## <span data-ttu-id="a9f88-104">句法</span><span class="sxs-lookup"><span data-stu-id="a9f88-104">SYNTAX</span></span>

### <span data-ttu-id="a9f88-105">SummaryTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="a9f88-105">SummaryTargetResourceIdFilter</span></span>
```
Measure-AzAlertStatistic -GroupBy <String> [-TargetResourceId <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-TimeRange <String>] [-CustomTimeRange <String>] [-IncludeSmartGroupsCount <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9f88-106">SummaryFilter</span><span class="sxs-lookup"><span data-stu-id="a9f88-106">SummaryFilter</span></span>
```
Measure-AzAlertStatistic -GroupBy <String> [-TargetResourceType <String>] [-TargetResourceGroup <String>]
 [-MonitorService <String>] [-MonitorCondition <String>] [-Severity <String>] [-State <String>]
 [-AlertRuleId <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-IncludeSmartGroupsCount <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9f88-107">說明</span><span class="sxs-lookup"><span data-stu-id="a9f88-107">DESCRIPTION</span></span>
<span data-ttu-id="a9f88-108">**AzAlertStatistic** Cmdlet 會取得警報摘要詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a9f88-108">**Measure-AzAlertStatistic** cmdlet gets alert summary details.</span></span>

## <span data-ttu-id="a9f88-109">示例</span><span class="sxs-lookup"><span data-stu-id="a9f88-109">EXAMPLES</span></span>

### <span data-ttu-id="a9f88-110">範例1</span><span class="sxs-lookup"><span data-stu-id="a9f88-110">Example 1</span></span>
```powershell
PS C:\> Measure-AzAlertStatistic -GroupBy "severity,alertstate" -State "Active"
```

<span data-ttu-id="a9f88-111">摘要依嚴重性及狀態（依作用中狀態篩選）來分組的警示計數。</span><span class="sxs-lookup"><span data-stu-id="a9f88-111">Summarize alerts count grouped by severity and state filtered by Active state.</span></span>

## <span data-ttu-id="a9f88-112">參數</span><span class="sxs-lookup"><span data-stu-id="a9f88-112">PARAMETERS</span></span>

### <span data-ttu-id="a9f88-113">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="a9f88-113">-AlertRuleId</span></span>
<span data-ttu-id="a9f88-114">篩選警示規則識別碼</span><span class="sxs-lookup"><span data-stu-id="a9f88-114">Filter on Alert Rule Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9f88-115">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="a9f88-115">-CustomTimeRange</span></span>
<span data-ttu-id="a9f88-116">支援的格式- \< \> / \< \> 在時間為 ISO-8601 格式時的開始時間結束時間</span><span class="sxs-lookup"><span data-stu-id="a9f88-116">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9f88-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9f88-117">-DefaultProfile</span></span>
<span data-ttu-id="a9f88-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a9f88-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9f88-119">-GroupBy</span><span class="sxs-lookup"><span data-stu-id="a9f88-119">-GroupBy</span></span>
<span data-ttu-id="a9f88-120">[摘要方式] 屬性</span><span class="sxs-lookup"><span data-stu-id="a9f88-120">Summarize by property</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9f88-121">-IncludeSmartGroupsCount</span><span class="sxs-lookup"><span data-stu-id="a9f88-121">-IncludeSmartGroupsCount</span></span>
<span data-ttu-id="a9f88-122">包括 SmartGroups 計數</span><span class="sxs-lookup"><span data-stu-id="a9f88-122">Include SmartGroups Count</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9f88-123">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="a9f88-123">-MonitorCondition</span></span>
<span data-ttu-id="a9f88-124">篩選監視器條件</span><span class="sxs-lookup"><span data-stu-id="a9f88-124">Filter on Monitor Condition</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9f88-125">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="a9f88-125">-MonitorService</span></span>
<span data-ttu-id="a9f88-126">篩選 Moniter 服務</span><span class="sxs-lookup"><span data-stu-id="a9f88-126">Filter on Moniter Service</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9f88-127">-嚴重度</span><span class="sxs-lookup"><span data-stu-id="a9f88-127">-Severity</span></span>
<span data-ttu-id="a9f88-128">在警示嚴重度篩選</span><span class="sxs-lookup"><span data-stu-id="a9f88-128">Filter on Severity of alert</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9f88-129">-State</span><span class="sxs-lookup"><span data-stu-id="a9f88-129">-State</span></span>
<span data-ttu-id="a9f88-130">篩選警示狀態</span><span class="sxs-lookup"><span data-stu-id="a9f88-130">Filter on State of alert</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9f88-131">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a9f88-131">-TargetResourceGroup</span></span>
<span data-ttu-id="a9f88-132">篩選 [警示] 目標資源的 [資源] 群組名稱。</span><span class="sxs-lookup"><span data-stu-id="a9f88-132">Filter on Resource group name of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: SummaryFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9f88-133">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="a9f88-133">-TargetResourceId</span></span>
<span data-ttu-id="a9f88-134">篩選警報目標資源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a9f88-134">Filter on Resource Id of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: SummaryTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9f88-135">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="a9f88-135">-TargetResourceType</span></span>
<span data-ttu-id="a9f88-136">篩選警報目標資源的資源類型。</span><span class="sxs-lookup"><span data-stu-id="a9f88-136">Filter on Resource type of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: SummaryFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9f88-137">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="a9f88-137">-TimeRange</span></span>
<span data-ttu-id="a9f88-138">支援的時間範圍值-1h、1d、7d、30d (預設為 1d) </span><span class="sxs-lookup"><span data-stu-id="a9f88-138">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9f88-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9f88-139">CommonParameters</span></span>
<span data-ttu-id="a9f88-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a9f88-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9f88-141">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a9f88-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9f88-142">輸入</span><span class="sxs-lookup"><span data-stu-id="a9f88-142">INPUTS</span></span>

### <span data-ttu-id="a9f88-143">所有</span><span class="sxs-lookup"><span data-stu-id="a9f88-143">None</span></span>

## <span data-ttu-id="a9f88-144">輸出</span><span class="sxs-lookup"><span data-stu-id="a9f88-144">OUTPUTS</span></span>

### <span data-ttu-id="a9f88-145">AlertsManagement. OutputModels. PSAlertsSummary</span><span class="sxs-lookup"><span data-stu-id="a9f88-145">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertsSummary</span></span>

## <span data-ttu-id="a9f88-146">筆記</span><span class="sxs-lookup"><span data-stu-id="a9f88-146">NOTES</span></span>

## <span data-ttu-id="a9f88-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="a9f88-147">RELATED LINKS</span></span>
