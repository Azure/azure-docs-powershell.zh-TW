---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/new-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementExport.md
ms.openlocfilehash: edc0475a9d4299e1bd7346ab441a78b09905d59c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100137355"
---
# <span data-ttu-id="0964a-101">New-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="0964a-101">New-AzCostManagementExport</span></span>

## <span data-ttu-id="0964a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0964a-102">SYNOPSIS</span></span>
<span data-ttu-id="0964a-103">建立或更新匯出的操作。</span><span class="sxs-lookup"><span data-stu-id="0964a-103">The operation to create or update a export.</span></span>
<span data-ttu-id="0964a-104">更新操作需要在要求中設定最新的 eTag。</span><span class="sxs-lookup"><span data-stu-id="0964a-104">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="0964a-105">您可以執行 [取得] 作業，以取得最新的 eTag。</span><span class="sxs-lookup"><span data-stu-id="0964a-105">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="0964a-106">建立操作不需要 eTag。</span><span class="sxs-lookup"><span data-stu-id="0964a-106">Create operation does not require eTag.</span></span>

## <span data-ttu-id="0964a-107">句法</span><span class="sxs-lookup"><span data-stu-id="0964a-107">SYNTAX</span></span>

```
New-AzCostManagementExport -Name <String> -Scope <String> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0964a-108">說明</span><span class="sxs-lookup"><span data-stu-id="0964a-108">DESCRIPTION</span></span>
<span data-ttu-id="0964a-109">建立或更新匯出的操作。</span><span class="sxs-lookup"><span data-stu-id="0964a-109">The operation to create or update a export.</span></span>
<span data-ttu-id="0964a-110">更新操作需要在要求中設定最新的 eTag。</span><span class="sxs-lookup"><span data-stu-id="0964a-110">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="0964a-111">您可以執行 [取得] 作業，以取得最新的 eTag。</span><span class="sxs-lookup"><span data-stu-id="0964a-111">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="0964a-112">建立操作不需要 eTag。</span><span class="sxs-lookup"><span data-stu-id="0964a-112">Create operation does not require eTag.</span></span>

## <span data-ttu-id="0964a-113">示例</span><span class="sxs-lookup"><span data-stu-id="0964a-113">EXAMPLES</span></span>

### <span data-ttu-id="0964a-114">範例1：建立 AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="0964a-114">Example 1: Create an AzCostManagementExport</span></span>
```powershell
PS C:\> New-AzCostManagementExport -Scope "subscriptions/***********" -Name "CostManagementExportTest" -ScheduleStatus "Active" -ScheduleRecurrence "Daily" -RecurrencePeriodFrom "2020-10-31T20:00:00Z" -RecurrencePeriodTo "2020-11-30T00:00:00Z" -Format "Csv" -DestinationResourceId "/subscriptions/*************/resourceGroups/ResourceGroupTest/providers/Microsoft.Storage/storageAccounts/storageAccountTest" `  -DestinationContainer "exports" -DestinationRootFolderPath "ad-hoc" -DefinitionType "Usage" -DefinitionTimeframe "MonthToDate" -DatasetGranularity "Daily"

ETag              Name                                      Type
----              ----                                      ----
"********" TestExportDatasetAggregationInfosagdhaghj Microsoft.CostManagement/exports
```

<span data-ttu-id="0964a-115">建立 AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="0964a-115">Create an AzCostManagementExport</span></span>

## <span data-ttu-id="0964a-116">參數</span><span class="sxs-lookup"><span data-stu-id="0964a-116">PARAMETERS</span></span>

### <span data-ttu-id="0964a-117">-ConfigurationColumn</span><span class="sxs-lookup"><span data-stu-id="0964a-117">-ConfigurationColumn</span></span>
<span data-ttu-id="0964a-118">要包含在匯出中的欄名稱陣列。</span><span class="sxs-lookup"><span data-stu-id="0964a-118">Array of column names to be included in the export.</span></span>
<span data-ttu-id="0964a-119">如果未提供，匯出將會包含所有可用的欄。</span><span class="sxs-lookup"><span data-stu-id="0964a-119">If not provided then the export will include all available columns.</span></span>
<span data-ttu-id="0964a-120">可用的欄可能會依客戶通道而有所不同 (請參閱) 範例。</span><span class="sxs-lookup"><span data-stu-id="0964a-120">The available columns can vary by customer channel (see examples).</span></span>

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

### <span data-ttu-id="0964a-121">-DataSetGranularity</span><span class="sxs-lookup"><span data-stu-id="0964a-121">-DataSetGranularity</span></span>
<span data-ttu-id="0964a-122">匯出中列的細微性。</span><span class="sxs-lookup"><span data-stu-id="0964a-122">The granularity of rows in the export.</span></span>
<span data-ttu-id="0964a-123">目前只支援「每日」。</span><span class="sxs-lookup"><span data-stu-id="0964a-123">Currently only 'Daily' is supported.</span></span>

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

### <span data-ttu-id="0964a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0964a-124">-DefaultProfile</span></span>
<span data-ttu-id="0964a-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0964a-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0964a-126">-DefinitionTimeframe</span><span class="sxs-lookup"><span data-stu-id="0964a-126">-DefinitionTimeframe</span></span>
<span data-ttu-id="0964a-127">用於拉匯出資料的時間範圍。</span><span class="sxs-lookup"><span data-stu-id="0964a-127">The time frame for pulling data for the export.</span></span>
<span data-ttu-id="0964a-128">如果自訂，則必須提供特定的時間週期。</span><span class="sxs-lookup"><span data-stu-id="0964a-128">If custom, then a specific time period must be provided.</span></span>

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

### <span data-ttu-id="0964a-129">-DefinitionType</span><span class="sxs-lookup"><span data-stu-id="0964a-129">-DefinitionType</span></span>
<span data-ttu-id="0964a-130">匯出的類型。</span><span class="sxs-lookup"><span data-stu-id="0964a-130">The type of the export.</span></span>
<span data-ttu-id="0964a-131">請注意，"用法" 相當於 "ActualCost"，且適用于尚不提供費用或攤銷以進行服務預留的匯出。</span><span class="sxs-lookup"><span data-stu-id="0964a-131">Note that 'Usage' is equivalent to 'ActualCost' and is applicable to exports that do not yet provide data for charges or amortization for service reservations.</span></span>

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

### <span data-ttu-id="0964a-132">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="0964a-132">-DestinationContainer</span></span>
<span data-ttu-id="0964a-133">要上傳匯出的容器名稱。</span><span class="sxs-lookup"><span data-stu-id="0964a-133">The name of the container where exports will be uploaded.</span></span>

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

### <span data-ttu-id="0964a-134">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="0964a-134">-DestinationResourceId</span></span>
<span data-ttu-id="0964a-135">要傳送匯出的儲存空間帳戶的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0964a-135">The resource id of the storage account where exports will be delivered.</span></span>

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

### <span data-ttu-id="0964a-136">-DestinationRootFolderPath</span><span class="sxs-lookup"><span data-stu-id="0964a-136">-DestinationRootFolderPath</span></span>
<span data-ttu-id="0964a-137">要上傳匯出的目錄名稱。</span><span class="sxs-lookup"><span data-stu-id="0964a-137">The name of the directory where exports will be uploaded.</span></span>

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

### <span data-ttu-id="0964a-138">-Format</span><span class="sxs-lookup"><span data-stu-id="0964a-138">-Format</span></span>
<span data-ttu-id="0964a-139">要傳送的匯出格式。</span><span class="sxs-lookup"><span data-stu-id="0964a-139">The format of the export being delivered.</span></span>
<span data-ttu-id="0964a-140">目前僅支援「Csv」。</span><span class="sxs-lookup"><span data-stu-id="0964a-140">Currently only 'Csv' is supported.</span></span>

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

### <span data-ttu-id="0964a-141">-名稱</span><span class="sxs-lookup"><span data-stu-id="0964a-141">-Name</span></span>
<span data-ttu-id="0964a-142">匯出名稱。</span><span class="sxs-lookup"><span data-stu-id="0964a-142">Export Name.</span></span>

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

### <span data-ttu-id="0964a-143">-RecurrencePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="0964a-143">-RecurrencePeriodFrom</span></span>
<span data-ttu-id="0964a-144">週期性開始日期。</span><span class="sxs-lookup"><span data-stu-id="0964a-144">The start date of recurrence.</span></span>

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

### <span data-ttu-id="0964a-145">-RecurrencePeriodTo</span><span class="sxs-lookup"><span data-stu-id="0964a-145">-RecurrencePeriodTo</span></span>
<span data-ttu-id="0964a-146">週期性結束日期。</span><span class="sxs-lookup"><span data-stu-id="0964a-146">The end date of recurrence.</span></span>

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

### <span data-ttu-id="0964a-147">-ScheduleRecurrence</span><span class="sxs-lookup"><span data-stu-id="0964a-147">-ScheduleRecurrence</span></span>
<span data-ttu-id="0964a-148">排程週期。</span><span class="sxs-lookup"><span data-stu-id="0964a-148">The schedule recurrence.</span></span>

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

### <span data-ttu-id="0964a-149">-ScheduleStatus</span><span class="sxs-lookup"><span data-stu-id="0964a-149">-ScheduleStatus</span></span>
<span data-ttu-id="0964a-150">匯出排程的狀態。</span><span class="sxs-lookup"><span data-stu-id="0964a-150">The status of the export's schedule.</span></span>
<span data-ttu-id="0964a-151">如果是「不活躍」，則會暫停匯出的排程。</span><span class="sxs-lookup"><span data-stu-id="0964a-151">If 'Inactive', the export's schedule is paused.</span></span>

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

### <span data-ttu-id="0964a-152">-範圍</span><span class="sxs-lookup"><span data-stu-id="0964a-152">-Scope</span></span>
<span data-ttu-id="0964a-153">這個參數會從不同的觀點「訂閱」、「ResourceGroup」和「提供服務」定義 costmanagement 的範圍。</span><span class="sxs-lookup"><span data-stu-id="0964a-153">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="0964a-154">-TimePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="0964a-154">-TimePeriodFrom</span></span>
<span data-ttu-id="0964a-155">匯出資料的開始日期。</span><span class="sxs-lookup"><span data-stu-id="0964a-155">The start date for export data.</span></span>

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

### <span data-ttu-id="0964a-156">-TimePeriodTo</span><span class="sxs-lookup"><span data-stu-id="0964a-156">-TimePeriodTo</span></span>
<span data-ttu-id="0964a-157">匯出資料的結束日期。</span><span class="sxs-lookup"><span data-stu-id="0964a-157">The end date for export data.</span></span>

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

### <span data-ttu-id="0964a-158">-確認</span><span class="sxs-lookup"><span data-stu-id="0964a-158">-Confirm</span></span>
<span data-ttu-id="0964a-159">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0964a-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0964a-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0964a-160">-WhatIf</span></span>
<span data-ttu-id="0964a-161">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0964a-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0964a-162">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0964a-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0964a-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0964a-163">CommonParameters</span></span>
<span data-ttu-id="0964a-164">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0964a-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0964a-165">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0964a-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0964a-166">輸入</span><span class="sxs-lookup"><span data-stu-id="0964a-166">INPUTS</span></span>

## <span data-ttu-id="0964a-167">輸出</span><span class="sxs-lookup"><span data-stu-id="0964a-167">OUTPUTS</span></span>

### <span data-ttu-id="0964a-168">IExport （CostManagement）。 Api20200601。</span><span class="sxs-lookup"><span data-stu-id="0964a-168">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="0964a-169">筆記</span><span class="sxs-lookup"><span data-stu-id="0964a-169">NOTES</span></span>

<span data-ttu-id="0964a-170">別名</span><span class="sxs-lookup"><span data-stu-id="0964a-170">ALIASES</span></span>

## <span data-ttu-id="0964a-171">相關連結</span><span class="sxs-lookup"><span data-stu-id="0964a-171">RELATED LINKS</span></span>

