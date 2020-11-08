---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/measure-azalertstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Measure-AzAlertStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Measure-AzAlertStatistic.md
ms.openlocfilehash: 96b83f6792babed9fed7c39cad44aec0ea0f26ed
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970724"
---
# <span data-ttu-id="dab3b-101">Measure-AzAlertStatistic</span><span class="sxs-lookup"><span data-stu-id="dab3b-101">Measure-AzAlertStatistic</span></span>

## <span data-ttu-id="dab3b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dab3b-102">SYNOPSIS</span></span>
<span data-ttu-id="dab3b-103">取得警示摘要資訊</span><span class="sxs-lookup"><span data-stu-id="dab3b-103">Gets Alert Summary Information</span></span>

## <span data-ttu-id="dab3b-104">句法</span><span class="sxs-lookup"><span data-stu-id="dab3b-104">SYNTAX</span></span>

### <span data-ttu-id="dab3b-105">SummaryTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="dab3b-105">SummaryTargetResourceIdFilter</span></span>
```
Measure-AzAlertStatistic -GroupBy <String> [-TargetResourceId <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-TimeRange <String>] [-CustomTimeRange <String>] [-IncludeSmartGroupsCount <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dab3b-106">SummaryFilter</span><span class="sxs-lookup"><span data-stu-id="dab3b-106">SummaryFilter</span></span>
```
Measure-AzAlertStatistic -GroupBy <String> [-TargetResourceType <String>] [-TargetResourceGroup <String>]
 [-MonitorService <String>] [-MonitorCondition <String>] [-Severity <String>] [-State <String>]
 [-AlertRuleId <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-IncludeSmartGroupsCount <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dab3b-107">說明</span><span class="sxs-lookup"><span data-stu-id="dab3b-107">DESCRIPTION</span></span>
<span data-ttu-id="dab3b-108">**AzAlertStatistic** Cmdlet 會取得警報摘要詳細資料。</span><span class="sxs-lookup"><span data-stu-id="dab3b-108">**Measure-AzAlertStatistic** cmdlet gets alert summary details.</span></span>

## <span data-ttu-id="dab3b-109">示例</span><span class="sxs-lookup"><span data-stu-id="dab3b-109">EXAMPLES</span></span>

### <span data-ttu-id="dab3b-110">範例1</span><span class="sxs-lookup"><span data-stu-id="dab3b-110">Example 1</span></span>
```powershell
PS C:\> Measure-AzAlertStatistic -GroupBy "severity,alertstate" -State "Active"
```

<span data-ttu-id="dab3b-111">摘要依嚴重性及狀態（依作用中狀態篩選）來分組的警示計數。</span><span class="sxs-lookup"><span data-stu-id="dab3b-111">Summarize alerts count grouped by severity and state filtered by Active state.</span></span>

## <span data-ttu-id="dab3b-112">參數</span><span class="sxs-lookup"><span data-stu-id="dab3b-112">PARAMETERS</span></span>

### <span data-ttu-id="dab3b-113">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="dab3b-113">-AlertRuleId</span></span>
<span data-ttu-id="dab3b-114">篩選警示規則識別碼</span><span class="sxs-lookup"><span data-stu-id="dab3b-114">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="dab3b-115">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="dab3b-115">-CustomTimeRange</span></span>
<span data-ttu-id="dab3b-116">支援的格式-在 \<start-time\> / \<end-time\> 時間為 ISO-8601 格式</span><span class="sxs-lookup"><span data-stu-id="dab3b-116">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

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

### <span data-ttu-id="dab3b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dab3b-117">-DefaultProfile</span></span>
<span data-ttu-id="dab3b-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dab3b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dab3b-119">-GroupBy</span><span class="sxs-lookup"><span data-stu-id="dab3b-119">-GroupBy</span></span>
<span data-ttu-id="dab3b-120">[摘要方式] 屬性</span><span class="sxs-lookup"><span data-stu-id="dab3b-120">Summarize by property</span></span>

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

### <span data-ttu-id="dab3b-121">-IncludeSmartGroupsCount</span><span class="sxs-lookup"><span data-stu-id="dab3b-121">-IncludeSmartGroupsCount</span></span>
<span data-ttu-id="dab3b-122">包括 SmartGroups 計數</span><span class="sxs-lookup"><span data-stu-id="dab3b-122">Include SmartGroups Count</span></span>

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

### <span data-ttu-id="dab3b-123">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="dab3b-123">-MonitorCondition</span></span>
<span data-ttu-id="dab3b-124">篩選監視器條件</span><span class="sxs-lookup"><span data-stu-id="dab3b-124">Filter on Monitor Condition</span></span>

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

### <span data-ttu-id="dab3b-125">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="dab3b-125">-MonitorService</span></span>
<span data-ttu-id="dab3b-126">篩選 Moniter 服務</span><span class="sxs-lookup"><span data-stu-id="dab3b-126">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="dab3b-127">-嚴重度</span><span class="sxs-lookup"><span data-stu-id="dab3b-127">-Severity</span></span>
<span data-ttu-id="dab3b-128">在警示嚴重度篩選</span><span class="sxs-lookup"><span data-stu-id="dab3b-128">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="dab3b-129">-State</span><span class="sxs-lookup"><span data-stu-id="dab3b-129">-State</span></span>
<span data-ttu-id="dab3b-130">篩選警示狀態</span><span class="sxs-lookup"><span data-stu-id="dab3b-130">Filter on State of alert</span></span>

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

### <span data-ttu-id="dab3b-131">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="dab3b-131">-TargetResourceGroup</span></span>
<span data-ttu-id="dab3b-132">篩選 [警示] 目標資源的 [資源] 群組名稱。</span><span class="sxs-lookup"><span data-stu-id="dab3b-132">Filter on Resource group name of the target resource of alert.</span></span>

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

### <span data-ttu-id="dab3b-133">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="dab3b-133">-TargetResourceId</span></span>
<span data-ttu-id="dab3b-134">篩選警報目標資源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="dab3b-134">Filter on Resource Id of the target resource of alert.</span></span>

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

### <span data-ttu-id="dab3b-135">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="dab3b-135">-TargetResourceType</span></span>
<span data-ttu-id="dab3b-136">篩選警報目標資源的資源類型。</span><span class="sxs-lookup"><span data-stu-id="dab3b-136">Filter on Resource type of the target resource of alert.</span></span>

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

### <span data-ttu-id="dab3b-137">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="dab3b-137">-TimeRange</span></span>
<span data-ttu-id="dab3b-138">支援的時間範圍值-1h、1d、7d、30d (預設為 1d) </span><span class="sxs-lookup"><span data-stu-id="dab3b-138">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="dab3b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dab3b-139">CommonParameters</span></span>
<span data-ttu-id="dab3b-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dab3b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dab3b-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="dab3b-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dab3b-142">輸入</span><span class="sxs-lookup"><span data-stu-id="dab3b-142">INPUTS</span></span>

### <span data-ttu-id="dab3b-143">所有</span><span class="sxs-lookup"><span data-stu-id="dab3b-143">None</span></span>

## <span data-ttu-id="dab3b-144">輸出</span><span class="sxs-lookup"><span data-stu-id="dab3b-144">OUTPUTS</span></span>

### <span data-ttu-id="dab3b-145">AlertsManagement. OutputModels. PSAlertsSummary</span><span class="sxs-lookup"><span data-stu-id="dab3b-145">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertsSummary</span></span>

## <span data-ttu-id="dab3b-146">筆記</span><span class="sxs-lookup"><span data-stu-id="dab3b-146">NOTES</span></span>

## <span data-ttu-id="dab3b-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="dab3b-147">RELATED LINKS</span></span>
