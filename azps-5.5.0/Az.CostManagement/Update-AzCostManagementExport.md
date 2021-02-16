---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/update-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Update-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Update-AzCostManagementExport.md
ms.openlocfilehash: 310600555f36fa0f6b129f2cf2a84581ffad044b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100129594"
---
# <span data-ttu-id="1022f-101">Update-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="1022f-101">Update-AzCostManagementExport</span></span>

## <span data-ttu-id="1022f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1022f-102">SYNOPSIS</span></span>
<span data-ttu-id="1022f-103">建立或更新匯出的操作。</span><span class="sxs-lookup"><span data-stu-id="1022f-103">The operation to create or update a export.</span></span>
<span data-ttu-id="1022f-104">更新操作需要在要求中設定最新的 eTag。</span><span class="sxs-lookup"><span data-stu-id="1022f-104">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="1022f-105">您可以執行 [取得] 作業，以取得最新的 eTag。</span><span class="sxs-lookup"><span data-stu-id="1022f-105">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="1022f-106">建立操作不需要 eTag。</span><span class="sxs-lookup"><span data-stu-id="1022f-106">Create operation does not require eTag.</span></span>

## <span data-ttu-id="1022f-107">句法</span><span class="sxs-lookup"><span data-stu-id="1022f-107">SYNTAX</span></span>

### <span data-ttu-id="1022f-108">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="1022f-108">UpdateExpanded (Default)</span></span>
```
Update-AzCostManagementExport -Name <String> -Scope <String> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-ETag <String>] [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1022f-109">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="1022f-109">UpdateViaIdentityExpanded</span></span>
```
Update-AzCostManagementExport -InputObject <ICostManagementIdentity> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-ETag <String>] [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1022f-110">說明</span><span class="sxs-lookup"><span data-stu-id="1022f-110">DESCRIPTION</span></span>
<span data-ttu-id="1022f-111">建立或更新匯出的操作。</span><span class="sxs-lookup"><span data-stu-id="1022f-111">The operation to create or update a export.</span></span>
<span data-ttu-id="1022f-112">更新操作需要在要求中設定最新的 eTag。</span><span class="sxs-lookup"><span data-stu-id="1022f-112">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="1022f-113">您可以執行 [取得] 作業，以取得最新的 eTag。</span><span class="sxs-lookup"><span data-stu-id="1022f-113">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="1022f-114">建立操作不需要 eTag。</span><span class="sxs-lookup"><span data-stu-id="1022f-114">Create operation does not require eTag.</span></span>

## <span data-ttu-id="1022f-115">示例</span><span class="sxs-lookup"><span data-stu-id="1022f-115">EXAMPLES</span></span>

### <span data-ttu-id="1022f-116">範例1：依範圍和名稱更新 AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="1022f-116">Example 1: Update AzCostManagementExport by scope and name</span></span>
```powershell
PS C:\> Update-AzCostManagementExport -Scope "subscriptions//*********" -Name "TestExport" -ScheduleRecurrence 'Weekly'

ETag              Name                                 Type
----              ----                                 ----
"********" TestExportDatasetAggregationInfo Microsoft.CostManagement/exports
```

<span data-ttu-id="1022f-117">依範圍和名稱更新 AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="1022f-117">Update AzCostManagementExport by Scope and name</span></span>

### <span data-ttu-id="1022f-118">範例2：由 InputObject 更新 AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="1022f-118">Example 2: Update AzCostManagementExport by InputObject</span></span>
```powershell
PS C:\> $oldExport = Get-AzCostManagementExport -Scope "subscriptions/*********" -Name "TestExport"
Update-AzCostManagementExport -InputObject $oldExport -ScheduleRecurrence 'Weekly'

ETag              Name                                 Type
----              ----                                 ----
"********" TestExportDatasetAggregationInfo Microsoft.CostManagement/exports
```

<span data-ttu-id="1022f-119">以 InputObject 更新 AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="1022f-119">Update AzCostManagementExport by InputObject</span></span>

## <span data-ttu-id="1022f-120">參數</span><span class="sxs-lookup"><span data-stu-id="1022f-120">PARAMETERS</span></span>

### <span data-ttu-id="1022f-121">-ConfigurationColumn</span><span class="sxs-lookup"><span data-stu-id="1022f-121">-ConfigurationColumn</span></span>
<span data-ttu-id="1022f-122">要包含在匯出中的欄名稱陣列。</span><span class="sxs-lookup"><span data-stu-id="1022f-122">Array of column names to be included in the export.</span></span>
<span data-ttu-id="1022f-123">如果未提供，匯出將會包含所有可用的欄。</span><span class="sxs-lookup"><span data-stu-id="1022f-123">If not provided then the export will include all available columns.</span></span>
<span data-ttu-id="1022f-124">可用的欄可能會依客戶通道而有所不同 (請參閱) 範例。</span><span class="sxs-lookup"><span data-stu-id="1022f-124">The available columns can vary by customer channel (see examples).</span></span>

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

### <span data-ttu-id="1022f-125">-DataSetGranularity</span><span class="sxs-lookup"><span data-stu-id="1022f-125">-DataSetGranularity</span></span>
<span data-ttu-id="1022f-126">匯出中列的細微性。</span><span class="sxs-lookup"><span data-stu-id="1022f-126">The granularity of rows in the export.</span></span>
<span data-ttu-id="1022f-127">目前只支援「每日」。</span><span class="sxs-lookup"><span data-stu-id="1022f-127">Currently only 'Daily' is supported.</span></span>

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

### <span data-ttu-id="1022f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1022f-128">-DefaultProfile</span></span>
<span data-ttu-id="1022f-129">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1022f-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1022f-130">-DefinitionTimeframe</span><span class="sxs-lookup"><span data-stu-id="1022f-130">-DefinitionTimeframe</span></span>
<span data-ttu-id="1022f-131">用於拉匯出資料的時間範圍。</span><span class="sxs-lookup"><span data-stu-id="1022f-131">The time frame for pulling data for the export.</span></span>
<span data-ttu-id="1022f-132">如果自訂，則必須提供特定的時間週期。</span><span class="sxs-lookup"><span data-stu-id="1022f-132">If custom, then a specific time period must be provided.</span></span>

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

### <span data-ttu-id="1022f-133">-DefinitionType</span><span class="sxs-lookup"><span data-stu-id="1022f-133">-DefinitionType</span></span>
<span data-ttu-id="1022f-134">匯出的類型。</span><span class="sxs-lookup"><span data-stu-id="1022f-134">The type of the export.</span></span>
<span data-ttu-id="1022f-135">請注意，"用法" 相當於 "ActualCost"，且適用于尚不提供費用或攤銷以進行服務預留的匯出。</span><span class="sxs-lookup"><span data-stu-id="1022f-135">Note that 'Usage' is equivalent to 'ActualCost' and is applicable to exports that do not yet provide data for charges or amortization for service reservations.</span></span>

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

### <span data-ttu-id="1022f-136">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="1022f-136">-DestinationContainer</span></span>
<span data-ttu-id="1022f-137">要上傳匯出的容器名稱。</span><span class="sxs-lookup"><span data-stu-id="1022f-137">The name of the container where exports will be uploaded.</span></span>

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

### <span data-ttu-id="1022f-138">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="1022f-138">-DestinationResourceId</span></span>
<span data-ttu-id="1022f-139">要傳送匯出的儲存空間帳戶的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1022f-139">The resource id of the storage account where exports will be delivered.</span></span>

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

### <span data-ttu-id="1022f-140">-DestinationRootFolderPath</span><span class="sxs-lookup"><span data-stu-id="1022f-140">-DestinationRootFolderPath</span></span>
<span data-ttu-id="1022f-141">要上傳匯出的目錄名稱。</span><span class="sxs-lookup"><span data-stu-id="1022f-141">The name of the directory where exports will be uploaded.</span></span>

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

### <span data-ttu-id="1022f-142">-ETag</span><span class="sxs-lookup"><span data-stu-id="1022f-142">-ETag</span></span>
<span data-ttu-id="1022f-143">資源的 eTag。</span><span class="sxs-lookup"><span data-stu-id="1022f-143">eTag of the resource.</span></span>
<span data-ttu-id="1022f-144">若要處理併發更新案例，此欄位將用來判斷使用者是否要更新最新版本。</span><span class="sxs-lookup"><span data-stu-id="1022f-144">To handle concurrent update scenario, this field will be used to determine whether the user is updating the latest version or not.</span></span>

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

### <span data-ttu-id="1022f-145">-Format</span><span class="sxs-lookup"><span data-stu-id="1022f-145">-Format</span></span>
<span data-ttu-id="1022f-146">要傳送的匯出格式。</span><span class="sxs-lookup"><span data-stu-id="1022f-146">The format of the export being delivered.</span></span>
<span data-ttu-id="1022f-147">目前僅支援「Csv」。</span><span class="sxs-lookup"><span data-stu-id="1022f-147">Currently only 'Csv' is supported.</span></span>

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

### <span data-ttu-id="1022f-148">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1022f-148">-InputObject</span></span>
<span data-ttu-id="1022f-149">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="1022f-149">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1022f-150">-名稱</span><span class="sxs-lookup"><span data-stu-id="1022f-150">-Name</span></span>
<span data-ttu-id="1022f-151">匯出名稱。</span><span class="sxs-lookup"><span data-stu-id="1022f-151">Export Name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ExportName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1022f-152">-RecurrencePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="1022f-152">-RecurrencePeriodFrom</span></span>
<span data-ttu-id="1022f-153">週期性開始日期。</span><span class="sxs-lookup"><span data-stu-id="1022f-153">The start date of recurrence.</span></span>

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

### <span data-ttu-id="1022f-154">-RecurrencePeriodTo</span><span class="sxs-lookup"><span data-stu-id="1022f-154">-RecurrencePeriodTo</span></span>
<span data-ttu-id="1022f-155">週期性結束日期。</span><span class="sxs-lookup"><span data-stu-id="1022f-155">The end date of recurrence.</span></span>

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

### <span data-ttu-id="1022f-156">-ScheduleRecurrence</span><span class="sxs-lookup"><span data-stu-id="1022f-156">-ScheduleRecurrence</span></span>
<span data-ttu-id="1022f-157">排程週期。</span><span class="sxs-lookup"><span data-stu-id="1022f-157">The schedule recurrence.</span></span>

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

### <span data-ttu-id="1022f-158">-ScheduleStatus</span><span class="sxs-lookup"><span data-stu-id="1022f-158">-ScheduleStatus</span></span>
<span data-ttu-id="1022f-159">匯出排程的狀態。</span><span class="sxs-lookup"><span data-stu-id="1022f-159">The status of the export's schedule.</span></span>
<span data-ttu-id="1022f-160">如果是「不活躍」，則會暫停匯出的排程。</span><span class="sxs-lookup"><span data-stu-id="1022f-160">If 'Inactive', the export's schedule is paused.</span></span>

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

### <span data-ttu-id="1022f-161">-範圍</span><span class="sxs-lookup"><span data-stu-id="1022f-161">-Scope</span></span>
<span data-ttu-id="1022f-162">這個參數會從不同的觀點「訂閱」、「ResourceGroup」和「提供服務」定義 costmanagement 的範圍。</span><span class="sxs-lookup"><span data-stu-id="1022f-162">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1022f-163">-TimePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="1022f-163">-TimePeriodFrom</span></span>
<span data-ttu-id="1022f-164">匯出資料的開始日期。</span><span class="sxs-lookup"><span data-stu-id="1022f-164">The start date for export data.</span></span>

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

### <span data-ttu-id="1022f-165">-TimePeriodTo</span><span class="sxs-lookup"><span data-stu-id="1022f-165">-TimePeriodTo</span></span>
<span data-ttu-id="1022f-166">匯出資料的結束日期。</span><span class="sxs-lookup"><span data-stu-id="1022f-166">The end date for export data.</span></span>

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

### <span data-ttu-id="1022f-167">-確認</span><span class="sxs-lookup"><span data-stu-id="1022f-167">-Confirm</span></span>
<span data-ttu-id="1022f-168">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1022f-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1022f-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1022f-169">-WhatIf</span></span>
<span data-ttu-id="1022f-170">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1022f-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1022f-171">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1022f-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1022f-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1022f-172">CommonParameters</span></span>
<span data-ttu-id="1022f-173">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1022f-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1022f-174">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1022f-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1022f-175">輸入</span><span class="sxs-lookup"><span data-stu-id="1022f-175">INPUTS</span></span>

### <span data-ttu-id="1022f-176">ICostManagementIdentity （CostManagement）的</span><span class="sxs-lookup"><span data-stu-id="1022f-176">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="1022f-177">輸出</span><span class="sxs-lookup"><span data-stu-id="1022f-177">OUTPUTS</span></span>

### <span data-ttu-id="1022f-178">IExport （CostManagement）。 Api20200601。</span><span class="sxs-lookup"><span data-stu-id="1022f-178">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="1022f-179">筆記</span><span class="sxs-lookup"><span data-stu-id="1022f-179">NOTES</span></span>

<span data-ttu-id="1022f-180">別名</span><span class="sxs-lookup"><span data-stu-id="1022f-180">ALIASES</span></span>

<span data-ttu-id="1022f-181">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="1022f-181">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1022f-182">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="1022f-182">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1022f-183">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="1022f-183">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1022f-184">INPUTOBJECT <ICostManagementIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="1022f-184">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1022f-185">`[AlertId <String>]`：警報 ID</span><span class="sxs-lookup"><span data-stu-id="1022f-185">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="1022f-186">`[ExportName <String>]`：匯出名稱。</span><span class="sxs-lookup"><span data-stu-id="1022f-186">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="1022f-187">`[ExternalCloudProviderId <String>]`：此專案可以是連結帳戶或 [{externalBillingAccountId}] 的 [{externalSubscriptionId} "，與維度/查詢作業搭配使用的合併帳戶。</span><span class="sxs-lookup"><span data-stu-id="1022f-187">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="1022f-188">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`：與維度/查詢作業相關聯的外部雲端提供者類型。</span><span class="sxs-lookup"><span data-stu-id="1022f-188">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="1022f-189">這包含合併帳戶的 [externalSubscriptions] 和 [externalBillingAccounts]。</span><span class="sxs-lookup"><span data-stu-id="1022f-189">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="1022f-190">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="1022f-190">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1022f-191">`[Scope <String>]`：與 [查看] 作業相關聯的範圍。</span><span class="sxs-lookup"><span data-stu-id="1022f-191">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="1022f-192">這包括訂閱範圍的 [訂閱/{subscriptionId}]、[訂閱/{subscriptionId}/resourceGroups/{resourceGroupName} "（針對 resourceGroup 範圍）。提供者/Microsoft. 帳單/billingAccounts/{billingAccountId} ' for 帳單帳戶範圍，" 提供者/Microsoft. 帳單/billingAccounts/{billingAccountId}/部門/{departmentId} "的部門範圍，" 提供者/microsoft. 帳單/billingAccounts/{billingAccountId} "（適用于 EnrollmentAccounts 範圍，" 供應商/Microsoft]）。帳單/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId} ' for BillingProfile 範圍，' 提供者/Microsoft. 帳單/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId} ' 適用于 InvoiceSection 範圍，' 提供者/Microsoft. 管理/managementGroups/{managementGroupId} ' 管理群組範圍、' 提供者/Microsoft. CostManagement/externalBillingAccounts/{externalBillingAccountName}」（適用于外部帳單帳戶範圍和「提供者/CostManagement/externalSubscriptions/{externalSubscriptionName}」）。</span><span class="sxs-lookup"><span data-stu-id="1022f-192">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="1022f-193">`[ViewName <String>]`：視圖名稱</span><span class="sxs-lookup"><span data-stu-id="1022f-193">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="1022f-194">相關連結</span><span class="sxs-lookup"><span data-stu-id="1022f-194">RELATED LINKS</span></span>

