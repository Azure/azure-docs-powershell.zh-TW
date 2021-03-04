---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/powershell/module/az.alertsmanagement/measure-azalertstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Measure-AzAlertStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Measure-AzAlertStatistic.md
ms.openlocfilehash: 27fb22a5cded5e196a4bef0aa8b504771abef864
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913985"
---
# <span data-ttu-id="df5fa-101">Measure-AzAlertStatistic</span><span class="sxs-lookup"><span data-stu-id="df5fa-101">Measure-AzAlertStatistic</span></span>

## <span data-ttu-id="df5fa-102">簡介</span><span class="sxs-lookup"><span data-stu-id="df5fa-102">SYNOPSIS</span></span>
<span data-ttu-id="df5fa-103">獲得警示摘要資訊</span><span class="sxs-lookup"><span data-stu-id="df5fa-103">Gets Alert Summary Information</span></span>

## <span data-ttu-id="df5fa-104">語法</span><span class="sxs-lookup"><span data-stu-id="df5fa-104">SYNTAX</span></span>

### <span data-ttu-id="df5fa-105">SummaryTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="df5fa-105">SummaryTargetResourceIdFilter</span></span>
```
Measure-AzAlertStatistic -GroupBy <String> [-TargetResourceId <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-TimeRange <String>] [-CustomTimeRange <String>] [-IncludeSmartGroupsCount <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df5fa-106">SummaryFilter</span><span class="sxs-lookup"><span data-stu-id="df5fa-106">SummaryFilter</span></span>
```
Measure-AzAlertStatistic -GroupBy <String> [-TargetResourceType <String>] [-TargetResourceGroup <String>]
 [-MonitorService <String>] [-MonitorCondition <String>] [-Severity <String>] [-State <String>]
 [-AlertRuleId <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-IncludeSmartGroupsCount <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df5fa-107">描述</span><span class="sxs-lookup"><span data-stu-id="df5fa-107">DESCRIPTION</span></span>
<span data-ttu-id="df5fa-108">**Measure-AzAlertStatistic** Cmdlet 會獲得警示摘要詳細資料。</span><span class="sxs-lookup"><span data-stu-id="df5fa-108">**Measure-AzAlertStatistic** cmdlet gets alert summary details.</span></span>

## <span data-ttu-id="df5fa-109">例子</span><span class="sxs-lookup"><span data-stu-id="df5fa-109">EXAMPLES</span></span>

### <span data-ttu-id="df5fa-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="df5fa-110">Example 1</span></span>
```powershell
PS C:\> Measure-AzAlertStatistic -GroupBy "severity,alertstate" -State "Active"
```

<span data-ttu-id="df5fa-111">摘要警示計數，以嚴重性和狀態根據活動狀態篩選。</span><span class="sxs-lookup"><span data-stu-id="df5fa-111">Summarize alerts count grouped by severity and state filtered by Active state.</span></span>

## <span data-ttu-id="df5fa-112">參數</span><span class="sxs-lookup"><span data-stu-id="df5fa-112">PARAMETERS</span></span>

### <span data-ttu-id="df5fa-113">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="df5fa-113">-AlertRuleId</span></span>
<span data-ttu-id="df5fa-114">篩選警示規則識別碼</span><span class="sxs-lookup"><span data-stu-id="df5fa-114">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="df5fa-115">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="df5fa-115">-CustomTimeRange</span></span>
<span data-ttu-id="df5fa-116">支援的格式 - \<start-time\> / \<end-time\> 時間為 ISO-8601 格式</span><span class="sxs-lookup"><span data-stu-id="df5fa-116">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

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

### <span data-ttu-id="df5fa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df5fa-117">-DefaultProfile</span></span>
<span data-ttu-id="df5fa-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="df5fa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df5fa-119">-GroupBy</span><span class="sxs-lookup"><span data-stu-id="df5fa-119">-GroupBy</span></span>
<span data-ttu-id="df5fa-120">根據屬性摘要</span><span class="sxs-lookup"><span data-stu-id="df5fa-120">Summarize by property</span></span>

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

### <span data-ttu-id="df5fa-121">-IncludeSmartGroupsCount</span><span class="sxs-lookup"><span data-stu-id="df5fa-121">-IncludeSmartGroupsCount</span></span>
<span data-ttu-id="df5fa-122">包含 SmartGroups Count</span><span class="sxs-lookup"><span data-stu-id="df5fa-122">Include SmartGroups Count</span></span>

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

### <span data-ttu-id="df5fa-123">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="df5fa-123">-MonitorCondition</span></span>
<span data-ttu-id="df5fa-124">在監視器條件上篩選</span><span class="sxs-lookup"><span data-stu-id="df5fa-124">Filter on Monitor Condition</span></span>

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

### <span data-ttu-id="df5fa-125">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="df5fa-125">-MonitorService</span></span>
<span data-ttu-id="df5fa-126">在 Moniter Service 上篩選</span><span class="sxs-lookup"><span data-stu-id="df5fa-126">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="df5fa-127">-嚴重性</span><span class="sxs-lookup"><span data-stu-id="df5fa-127">-Severity</span></span>
<span data-ttu-id="df5fa-128">篩選警示嚴重性</span><span class="sxs-lookup"><span data-stu-id="df5fa-128">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="df5fa-129">-State</span><span class="sxs-lookup"><span data-stu-id="df5fa-129">-State</span></span>
<span data-ttu-id="df5fa-130">篩選通知狀態</span><span class="sxs-lookup"><span data-stu-id="df5fa-130">Filter on State of alert</span></span>

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

### <span data-ttu-id="df5fa-131">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="df5fa-131">-TargetResourceGroup</span></span>
<span data-ttu-id="df5fa-132">篩選警示目標資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="df5fa-132">Filter on Resource group name of the target resource of alert.</span></span>

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

### <span data-ttu-id="df5fa-133">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="df5fa-133">-TargetResourceId</span></span>
<span data-ttu-id="df5fa-134">篩選警示目標資源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="df5fa-134">Filter on Resource Id of the target resource of alert.</span></span>

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

### <span data-ttu-id="df5fa-135">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="df5fa-135">-TargetResourceType</span></span>
<span data-ttu-id="df5fa-136">篩選警示目標資源的資源類型。</span><span class="sxs-lookup"><span data-stu-id="df5fa-136">Filter on Resource type of the target resource of alert.</span></span>

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

### <span data-ttu-id="df5fa-137">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="df5fa-137">-TimeRange</span></span>
<span data-ttu-id="df5fa-138">支援的時間範圍值 - 1h、1d、7d、30d (預設值為 1d) </span><span class="sxs-lookup"><span data-stu-id="df5fa-138">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="df5fa-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df5fa-139">CommonParameters</span></span>
<span data-ttu-id="df5fa-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="df5fa-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df5fa-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="df5fa-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df5fa-142">輸入</span><span class="sxs-lookup"><span data-stu-id="df5fa-142">INPUTS</span></span>

### <span data-ttu-id="df5fa-143">沒有</span><span class="sxs-lookup"><span data-stu-id="df5fa-143">None</span></span>

## <span data-ttu-id="df5fa-144">輸出</span><span class="sxs-lookup"><span data-stu-id="df5fa-144">OUTPUTS</span></span>

### <span data-ttu-id="df5fa-145">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertsSummary</span><span class="sxs-lookup"><span data-stu-id="df5fa-145">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertsSummary</span></span>

## <span data-ttu-id="df5fa-146">筆記</span><span class="sxs-lookup"><span data-stu-id="df5fa-146">NOTES</span></span>

## <span data-ttu-id="df5fa-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="df5fa-147">RELATED LINKS</span></span>
