---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.costmanagement/new-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementExport.md
ms.openlocfilehash: bc3ff9c6d27cba92cf29090dda988a27f9e8a50b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916760"
---
# <span data-ttu-id="18b04-101">New-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="18b04-101">New-AzCostManagementExport</span></span>

## <span data-ttu-id="18b04-102">簡介</span><span class="sxs-lookup"><span data-stu-id="18b04-102">SYNOPSIS</span></span>
<span data-ttu-id="18b04-103">建立或更新匯出的作業。</span><span class="sxs-lookup"><span data-stu-id="18b04-103">The operation to create or update a export.</span></span>
<span data-ttu-id="18b04-104">更新作業需要在要求中設定最新的 eTag。</span><span class="sxs-lookup"><span data-stu-id="18b04-104">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="18b04-105">您可以執行 get 運算來取得最新的 eTag。</span><span class="sxs-lookup"><span data-stu-id="18b04-105">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="18b04-106">建立作業不需要 eTag。</span><span class="sxs-lookup"><span data-stu-id="18b04-106">Create operation does not require eTag.</span></span>

## <span data-ttu-id="18b04-107">語法</span><span class="sxs-lookup"><span data-stu-id="18b04-107">SYNTAX</span></span>

```
New-AzCostManagementExport -Name <String> -Scope <String> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="18b04-108">描述</span><span class="sxs-lookup"><span data-stu-id="18b04-108">DESCRIPTION</span></span>
<span data-ttu-id="18b04-109">建立或更新匯出的作業。</span><span class="sxs-lookup"><span data-stu-id="18b04-109">The operation to create or update a export.</span></span>
<span data-ttu-id="18b04-110">更新作業需要在要求中設定最新的 eTag。</span><span class="sxs-lookup"><span data-stu-id="18b04-110">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="18b04-111">您可以執行 get 運算來取得最新的 eTag。</span><span class="sxs-lookup"><span data-stu-id="18b04-111">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="18b04-112">建立作業不需要 eTag。</span><span class="sxs-lookup"><span data-stu-id="18b04-112">Create operation does not require eTag.</span></span>

## <span data-ttu-id="18b04-113">例子</span><span class="sxs-lookup"><span data-stu-id="18b04-113">EXAMPLES</span></span>

### <span data-ttu-id="18b04-114">範例 1：建立 AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="18b04-114">Example 1: Create an AzCostManagementExport</span></span>
```powershell
PS C:\> New-AzCostManagementExport -Scope "subscriptions/***********" -Name "CostManagementExportTest" -ScheduleStatus "Active" -ScheduleRecurrence "Daily" -RecurrencePeriodFrom "2020-10-31T20:00:00Z" -RecurrencePeriodTo "2020-11-30T00:00:00Z" -Format "Csv" -DestinationResourceId "/subscriptions/*************/resourceGroups/ResourceGroupTest/providers/Microsoft.Storage/storageAccounts/storageAccountTest" `  -DestinationContainer "exports" -DestinationRootFolderPath "ad-hoc" -DefinitionType "Usage" -DefinitionTimeframe "MonthToDate" -DatasetGranularity "Daily"

ETag              Name                                      Type
----              ----                                      ----
"********" TestExportDatasetAggregationInfosagdhaghj Microsoft.CostManagement/exports
```

<span data-ttu-id="18b04-115">建立 AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="18b04-115">Create an AzCostManagementExport</span></span>

## <span data-ttu-id="18b04-116">參數</span><span class="sxs-lookup"><span data-stu-id="18b04-116">PARAMETERS</span></span>

### <span data-ttu-id="18b04-117">-ConfigurationColumn</span><span class="sxs-lookup"><span data-stu-id="18b04-117">-ConfigurationColumn</span></span>
<span data-ttu-id="18b04-118">要包含在匯出中的欄名稱陣列。</span><span class="sxs-lookup"><span data-stu-id="18b04-118">Array of column names to be included in the export.</span></span>
<span data-ttu-id="18b04-119">如果沒有提供，則匯出會包含所有可用的欄。</span><span class="sxs-lookup"><span data-stu-id="18b04-119">If not provided then the export will include all available columns.</span></span>
<span data-ttu-id="18b04-120">可用欄可能會依客戶通道而異， (範例) 。</span><span class="sxs-lookup"><span data-stu-id="18b04-120">The available columns can vary by customer channel (see examples).</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18b04-121">-DataSetGranularity</span><span class="sxs-lookup"><span data-stu-id="18b04-121">-DataSetGranularity</span></span>
<span data-ttu-id="18b04-122">匯出中列的細微程度。</span><span class="sxs-lookup"><span data-stu-id="18b04-122">The granularity of rows in the export.</span></span>
<span data-ttu-id="18b04-123">目前僅支援 '每日'。</span><span class="sxs-lookup"><span data-stu-id="18b04-123">Currently only 'Daily' is supported.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.GranularityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18b04-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18b04-124">-DefaultProfile</span></span>
<span data-ttu-id="18b04-125">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="18b04-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18b04-126">-DefinitionTimeframe</span><span class="sxs-lookup"><span data-stu-id="18b04-126">-DefinitionTimeframe</span></span>
<span data-ttu-id="18b04-127">提取匯出資料的時間範圍。</span><span class="sxs-lookup"><span data-stu-id="18b04-127">The time frame for pulling data for the export.</span></span>
<span data-ttu-id="18b04-128">如果為自訂，則必須提供特定的時段。</span><span class="sxs-lookup"><span data-stu-id="18b04-128">If custom, then a specific time period must be provided.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.TimeframeType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18b04-129">-DefinitionType</span><span class="sxs-lookup"><span data-stu-id="18b04-129">-DefinitionType</span></span>
<span data-ttu-id="18b04-130">匯出的類型。</span><span class="sxs-lookup"><span data-stu-id="18b04-130">The type of the export.</span></span>
<span data-ttu-id="18b04-131">請注意，使用狀況相當於"ActualCost"，適用于尚未提供服務預約費用或攤銷資料之匯出。</span><span class="sxs-lookup"><span data-stu-id="18b04-131">Note that 'Usage' is equivalent to 'ActualCost' and is applicable to exports that do not yet provide data for charges or amortization for service reservations.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.ExportType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18b04-132">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="18b04-132">-DestinationContainer</span></span>
<span data-ttu-id="18b04-133">要上傳匯出的容器名稱。</span><span class="sxs-lookup"><span data-stu-id="18b04-133">The name of the container where exports will be uploaded.</span></span>

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

### <span data-ttu-id="18b04-134">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="18b04-134">-DestinationResourceId</span></span>
<span data-ttu-id="18b04-135">要傳送匯出的儲存空間帳戶資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="18b04-135">The resource id of the storage account where exports will be delivered.</span></span>

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

### <span data-ttu-id="18b04-136">-DestinationRootFolderPath</span><span class="sxs-lookup"><span data-stu-id="18b04-136">-DestinationRootFolderPath</span></span>
<span data-ttu-id="18b04-137">要上傳匯出的目錄名稱。</span><span class="sxs-lookup"><span data-stu-id="18b04-137">The name of the directory where exports will be uploaded.</span></span>

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

### <span data-ttu-id="18b04-138">-格式</span><span class="sxs-lookup"><span data-stu-id="18b04-138">-Format</span></span>
<span data-ttu-id="18b04-139">要傳遞之匯出的格式。</span><span class="sxs-lookup"><span data-stu-id="18b04-139">The format of the export being delivered.</span></span>
<span data-ttu-id="18b04-140">目前僅支援 'Csv'。</span><span class="sxs-lookup"><span data-stu-id="18b04-140">Currently only 'Csv' is supported.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.FormatType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18b04-141">-名稱</span><span class="sxs-lookup"><span data-stu-id="18b04-141">-Name</span></span>
<span data-ttu-id="18b04-142">匯出名稱。</span><span class="sxs-lookup"><span data-stu-id="18b04-142">Export Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExportName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18b04-143">-RecurrencePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="18b04-143">-RecurrencePeriodFrom</span></span>
<span data-ttu-id="18b04-144">週期的開始日期。</span><span class="sxs-lookup"><span data-stu-id="18b04-144">The start date of recurrence.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18b04-145">-RecurrencePeriodTo</span><span class="sxs-lookup"><span data-stu-id="18b04-145">-RecurrencePeriodTo</span></span>
<span data-ttu-id="18b04-146">週期的結束日期。</span><span class="sxs-lookup"><span data-stu-id="18b04-146">The end date of recurrence.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18b04-147">-ScheduleRecurrence</span><span class="sxs-lookup"><span data-stu-id="18b04-147">-ScheduleRecurrence</span></span>
<span data-ttu-id="18b04-148">排程週期。</span><span class="sxs-lookup"><span data-stu-id="18b04-148">The schedule recurrence.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.RecurrenceType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18b04-149">-ScheduleStatus</span><span class="sxs-lookup"><span data-stu-id="18b04-149">-ScheduleStatus</span></span>
<span data-ttu-id="18b04-150">匯出排程的狀態。</span><span class="sxs-lookup"><span data-stu-id="18b04-150">The status of the export's schedule.</span></span>
<span data-ttu-id="18b04-151">如果為非使用中，匯出的排程會暫停。</span><span class="sxs-lookup"><span data-stu-id="18b04-151">If 'Inactive', the export's schedule is paused.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.StatusType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18b04-152">-範圍</span><span class="sxs-lookup"><span data-stu-id="18b04-152">-Scope</span></span>
<span data-ttu-id="18b04-153">此參數會從不同的觀點定義成本管理的範圍，從"訂閱」、"ResourceGroup"和"提供服務"。</span><span class="sxs-lookup"><span data-stu-id="18b04-153">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="18b04-154">-TimePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="18b04-154">-TimePeriodFrom</span></span>
<span data-ttu-id="18b04-155">匯出資料的開始日期。</span><span class="sxs-lookup"><span data-stu-id="18b04-155">The start date for export data.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18b04-156">-TimePeriodTo</span><span class="sxs-lookup"><span data-stu-id="18b04-156">-TimePeriodTo</span></span>
<span data-ttu-id="18b04-157">匯出資料的結束日期。</span><span class="sxs-lookup"><span data-stu-id="18b04-157">The end date for export data.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18b04-158">-確認</span><span class="sxs-lookup"><span data-stu-id="18b04-158">-Confirm</span></span>
<span data-ttu-id="18b04-159">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="18b04-159">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18b04-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18b04-160">-WhatIf</span></span>
<span data-ttu-id="18b04-161">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="18b04-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18b04-162">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="18b04-162">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18b04-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18b04-163">CommonParameters</span></span>
<span data-ttu-id="18b04-164">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="18b04-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18b04-165">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="18b04-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18b04-166">輸入</span><span class="sxs-lookup"><span data-stu-id="18b04-166">INPUTS</span></span>

## <span data-ttu-id="18b04-167">輸出</span><span class="sxs-lookup"><span data-stu-id="18b04-167">OUTPUTS</span></span>

### <span data-ttu-id="18b04-168">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.models.Api20200601.IExport</span><span class="sxs-lookup"><span data-stu-id="18b04-168">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="18b04-169">筆記</span><span class="sxs-lookup"><span data-stu-id="18b04-169">NOTES</span></span>

<span data-ttu-id="18b04-170">別名</span><span class="sxs-lookup"><span data-stu-id="18b04-170">ALIASES</span></span>

## <span data-ttu-id="18b04-171">相關連結</span><span class="sxs-lookup"><span data-stu-id="18b04-171">RELATED LINKS</span></span>

