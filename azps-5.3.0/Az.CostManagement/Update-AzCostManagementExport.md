---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/update-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Update-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Update-AzCostManagementExport.md
ms.openlocfilehash: 310600555f36fa0f6b129f2cf2a84581ffad044b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449499"
---
# <span data-ttu-id="624d9-101">Update-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="624d9-101">Update-AzCostManagementExport</span></span>

## <span data-ttu-id="624d9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="624d9-102">SYNOPSIS</span></span>
<span data-ttu-id="624d9-103">建立或更新匯出的操作。</span><span class="sxs-lookup"><span data-stu-id="624d9-103">The operation to create or update a export.</span></span>
<span data-ttu-id="624d9-104">更新操作需要在要求中設定最新的 eTag。</span><span class="sxs-lookup"><span data-stu-id="624d9-104">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="624d9-105">您可以執行 [取得] 作業，以取得最新的 eTag。</span><span class="sxs-lookup"><span data-stu-id="624d9-105">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="624d9-106">建立操作不需要 eTag。</span><span class="sxs-lookup"><span data-stu-id="624d9-106">Create operation does not require eTag.</span></span>

## <span data-ttu-id="624d9-107">句法</span><span class="sxs-lookup"><span data-stu-id="624d9-107">SYNTAX</span></span>

### <span data-ttu-id="624d9-108">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="624d9-108">UpdateExpanded (Default)</span></span>
```
Update-AzCostManagementExport -Name <String> -Scope <String> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-ETag <String>] [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="624d9-109">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="624d9-109">UpdateViaIdentityExpanded</span></span>
```
Update-AzCostManagementExport -InputObject <ICostManagementIdentity> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-ETag <String>] [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="624d9-110">說明</span><span class="sxs-lookup"><span data-stu-id="624d9-110">DESCRIPTION</span></span>
<span data-ttu-id="624d9-111">建立或更新匯出的操作。</span><span class="sxs-lookup"><span data-stu-id="624d9-111">The operation to create or update a export.</span></span>
<span data-ttu-id="624d9-112">更新操作需要在要求中設定最新的 eTag。</span><span class="sxs-lookup"><span data-stu-id="624d9-112">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="624d9-113">您可以執行 [取得] 作業，以取得最新的 eTag。</span><span class="sxs-lookup"><span data-stu-id="624d9-113">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="624d9-114">建立操作不需要 eTag。</span><span class="sxs-lookup"><span data-stu-id="624d9-114">Create operation does not require eTag.</span></span>

## <span data-ttu-id="624d9-115">示例</span><span class="sxs-lookup"><span data-stu-id="624d9-115">EXAMPLES</span></span>

### <span data-ttu-id="624d9-116">範例1：依範圍和名稱更新 AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="624d9-116">Example 1: Update AzCostManagementExport by scope and name</span></span>
```powershell
PS C:\> Update-AzCostManagementExport -Scope "subscriptions//*********" -Name "TestExport" -ScheduleRecurrence 'Weekly'

ETag              Name                                 Type
----              ----                                 ----
"********" TestExportDatasetAggregationInfo Microsoft.CostManagement/exports
```

<span data-ttu-id="624d9-117">依範圍和名稱更新 AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="624d9-117">Update AzCostManagementExport by Scope and name</span></span>

### <span data-ttu-id="624d9-118">範例2：由 InputObject 更新 AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="624d9-118">Example 2: Update AzCostManagementExport by InputObject</span></span>
```powershell
PS C:\> $oldExport = Get-AzCostManagementExport -Scope "subscriptions/*********" -Name "TestExport"
Update-AzCostManagementExport -InputObject $oldExport -ScheduleRecurrence 'Weekly'

ETag              Name                                 Type
----              ----                                 ----
"********" TestExportDatasetAggregationInfo Microsoft.CostManagement/exports
```

<span data-ttu-id="624d9-119">以 InputObject 更新 AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="624d9-119">Update AzCostManagementExport by InputObject</span></span>

## <span data-ttu-id="624d9-120">參數</span><span class="sxs-lookup"><span data-stu-id="624d9-120">PARAMETERS</span></span>

### <span data-ttu-id="624d9-121">-ConfigurationColumn</span><span class="sxs-lookup"><span data-stu-id="624d9-121">-ConfigurationColumn</span></span>
<span data-ttu-id="624d9-122">要包含在匯出中的欄名稱陣列。</span><span class="sxs-lookup"><span data-stu-id="624d9-122">Array of column names to be included in the export.</span></span>
<span data-ttu-id="624d9-123">如果未提供，匯出將會包含所有可用的欄。</span><span class="sxs-lookup"><span data-stu-id="624d9-123">If not provided then the export will include all available columns.</span></span>
<span data-ttu-id="624d9-124">可用的欄可能會依客戶通道而有所不同 (請參閱) 範例。</span><span class="sxs-lookup"><span data-stu-id="624d9-124">The available columns can vary by customer channel (see examples).</span></span>

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

### <span data-ttu-id="624d9-125">-DataSetGranularity</span><span class="sxs-lookup"><span data-stu-id="624d9-125">-DataSetGranularity</span></span>
<span data-ttu-id="624d9-126">匯出中列的細微性。</span><span class="sxs-lookup"><span data-stu-id="624d9-126">The granularity of rows in the export.</span></span>
<span data-ttu-id="624d9-127">目前只支援「每日」。</span><span class="sxs-lookup"><span data-stu-id="624d9-127">Currently only 'Daily' is supported.</span></span>

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

### <span data-ttu-id="624d9-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="624d9-128">-DefaultProfile</span></span>
<span data-ttu-id="624d9-129">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="624d9-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="624d9-130">-DefinitionTimeframe</span><span class="sxs-lookup"><span data-stu-id="624d9-130">-DefinitionTimeframe</span></span>
<span data-ttu-id="624d9-131">用於拉匯出資料的時間範圍。</span><span class="sxs-lookup"><span data-stu-id="624d9-131">The time frame for pulling data for the export.</span></span>
<span data-ttu-id="624d9-132">如果自訂，則必須提供特定的時間週期。</span><span class="sxs-lookup"><span data-stu-id="624d9-132">If custom, then a specific time period must be provided.</span></span>

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

### <span data-ttu-id="624d9-133">-DefinitionType</span><span class="sxs-lookup"><span data-stu-id="624d9-133">-DefinitionType</span></span>
<span data-ttu-id="624d9-134">匯出的類型。</span><span class="sxs-lookup"><span data-stu-id="624d9-134">The type of the export.</span></span>
<span data-ttu-id="624d9-135">請注意，"用法" 相當於 "ActualCost"，且適用于尚不提供費用或攤銷以進行服務預留的匯出。</span><span class="sxs-lookup"><span data-stu-id="624d9-135">Note that 'Usage' is equivalent to 'ActualCost' and is applicable to exports that do not yet provide data for charges or amortization for service reservations.</span></span>

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

### <span data-ttu-id="624d9-136">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="624d9-136">-DestinationContainer</span></span>
<span data-ttu-id="624d9-137">要上傳匯出的容器名稱。</span><span class="sxs-lookup"><span data-stu-id="624d9-137">The name of the container where exports will be uploaded.</span></span>

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

### <span data-ttu-id="624d9-138">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="624d9-138">-DestinationResourceId</span></span>
<span data-ttu-id="624d9-139">要傳送匯出的儲存空間帳戶的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="624d9-139">The resource id of the storage account where exports will be delivered.</span></span>

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

### <span data-ttu-id="624d9-140">-DestinationRootFolderPath</span><span class="sxs-lookup"><span data-stu-id="624d9-140">-DestinationRootFolderPath</span></span>
<span data-ttu-id="624d9-141">要上傳匯出的目錄名稱。</span><span class="sxs-lookup"><span data-stu-id="624d9-141">The name of the directory where exports will be uploaded.</span></span>

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

### <span data-ttu-id="624d9-142">-ETag</span><span class="sxs-lookup"><span data-stu-id="624d9-142">-ETag</span></span>
<span data-ttu-id="624d9-143">資源的 eTag。</span><span class="sxs-lookup"><span data-stu-id="624d9-143">eTag of the resource.</span></span>
<span data-ttu-id="624d9-144">若要處理併發更新案例，此欄位將用來判斷使用者是否要更新最新版本。</span><span class="sxs-lookup"><span data-stu-id="624d9-144">To handle concurrent update scenario, this field will be used to determine whether the user is updating the latest version or not.</span></span>

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

### <span data-ttu-id="624d9-145">-Format</span><span class="sxs-lookup"><span data-stu-id="624d9-145">-Format</span></span>
<span data-ttu-id="624d9-146">要傳送的匯出格式。</span><span class="sxs-lookup"><span data-stu-id="624d9-146">The format of the export being delivered.</span></span>
<span data-ttu-id="624d9-147">目前僅支援「Csv」。</span><span class="sxs-lookup"><span data-stu-id="624d9-147">Currently only 'Csv' is supported.</span></span>

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

### <span data-ttu-id="624d9-148">-InputObject</span><span class="sxs-lookup"><span data-stu-id="624d9-148">-InputObject</span></span>
<span data-ttu-id="624d9-149">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="624d9-149">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="624d9-150">-名稱</span><span class="sxs-lookup"><span data-stu-id="624d9-150">-Name</span></span>
<span data-ttu-id="624d9-151">匯出名稱。</span><span class="sxs-lookup"><span data-stu-id="624d9-151">Export Name.</span></span>

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

### <span data-ttu-id="624d9-152">-RecurrencePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="624d9-152">-RecurrencePeriodFrom</span></span>
<span data-ttu-id="624d9-153">週期性開始日期。</span><span class="sxs-lookup"><span data-stu-id="624d9-153">The start date of recurrence.</span></span>

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

### <span data-ttu-id="624d9-154">-RecurrencePeriodTo</span><span class="sxs-lookup"><span data-stu-id="624d9-154">-RecurrencePeriodTo</span></span>
<span data-ttu-id="624d9-155">週期性結束日期。</span><span class="sxs-lookup"><span data-stu-id="624d9-155">The end date of recurrence.</span></span>

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

### <span data-ttu-id="624d9-156">-ScheduleRecurrence</span><span class="sxs-lookup"><span data-stu-id="624d9-156">-ScheduleRecurrence</span></span>
<span data-ttu-id="624d9-157">排程週期。</span><span class="sxs-lookup"><span data-stu-id="624d9-157">The schedule recurrence.</span></span>

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

### <span data-ttu-id="624d9-158">-ScheduleStatus</span><span class="sxs-lookup"><span data-stu-id="624d9-158">-ScheduleStatus</span></span>
<span data-ttu-id="624d9-159">匯出排程的狀態。</span><span class="sxs-lookup"><span data-stu-id="624d9-159">The status of the export's schedule.</span></span>
<span data-ttu-id="624d9-160">如果是「不活躍」，則會暫停匯出的排程。</span><span class="sxs-lookup"><span data-stu-id="624d9-160">If 'Inactive', the export's schedule is paused.</span></span>

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

### <span data-ttu-id="624d9-161">-範圍</span><span class="sxs-lookup"><span data-stu-id="624d9-161">-Scope</span></span>
<span data-ttu-id="624d9-162">這個參數會從不同的觀點「訂閱」、「ResourceGroup」和「提供服務」定義 costmanagement 的範圍。</span><span class="sxs-lookup"><span data-stu-id="624d9-162">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="624d9-163">-TimePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="624d9-163">-TimePeriodFrom</span></span>
<span data-ttu-id="624d9-164">匯出資料的開始日期。</span><span class="sxs-lookup"><span data-stu-id="624d9-164">The start date for export data.</span></span>

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

### <span data-ttu-id="624d9-165">-TimePeriodTo</span><span class="sxs-lookup"><span data-stu-id="624d9-165">-TimePeriodTo</span></span>
<span data-ttu-id="624d9-166">匯出資料的結束日期。</span><span class="sxs-lookup"><span data-stu-id="624d9-166">The end date for export data.</span></span>

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

### <span data-ttu-id="624d9-167">-確認</span><span class="sxs-lookup"><span data-stu-id="624d9-167">-Confirm</span></span>
<span data-ttu-id="624d9-168">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="624d9-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="624d9-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="624d9-169">-WhatIf</span></span>
<span data-ttu-id="624d9-170">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="624d9-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="624d9-171">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="624d9-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="624d9-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="624d9-172">CommonParameters</span></span>
<span data-ttu-id="624d9-173">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="624d9-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="624d9-174">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="624d9-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="624d9-175">輸入</span><span class="sxs-lookup"><span data-stu-id="624d9-175">INPUTS</span></span>

### <span data-ttu-id="624d9-176">ICostManagementIdentity （CostManagement）的</span><span class="sxs-lookup"><span data-stu-id="624d9-176">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="624d9-177">輸出</span><span class="sxs-lookup"><span data-stu-id="624d9-177">OUTPUTS</span></span>

### <span data-ttu-id="624d9-178">IExport （CostManagement）。 Api20200601。</span><span class="sxs-lookup"><span data-stu-id="624d9-178">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="624d9-179">筆記</span><span class="sxs-lookup"><span data-stu-id="624d9-179">NOTES</span></span>

<span data-ttu-id="624d9-180">別名</span><span class="sxs-lookup"><span data-stu-id="624d9-180">ALIASES</span></span>

<span data-ttu-id="624d9-181">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="624d9-181">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="624d9-182">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="624d9-182">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="624d9-183">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="624d9-183">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="624d9-184">INPUTOBJECT <ICostManagementIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="624d9-184">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="624d9-185">`[AlertId <String>]`：警報 ID</span><span class="sxs-lookup"><span data-stu-id="624d9-185">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="624d9-186">`[ExportName <String>]`：匯出名稱。</span><span class="sxs-lookup"><span data-stu-id="624d9-186">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="624d9-187">`[ExternalCloudProviderId <String>]`：此專案可以是連結帳戶或 [{externalBillingAccountId}] 的 [{externalSubscriptionId} "，與維度/查詢作業搭配使用的合併帳戶。</span><span class="sxs-lookup"><span data-stu-id="624d9-187">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="624d9-188">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`：與維度/查詢作業相關聯的外部雲端提供者類型。</span><span class="sxs-lookup"><span data-stu-id="624d9-188">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="624d9-189">這包含合併帳戶的 [externalSubscriptions] 和 [externalBillingAccounts]。</span><span class="sxs-lookup"><span data-stu-id="624d9-189">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="624d9-190">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="624d9-190">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="624d9-191">`[Scope <String>]`：與 [查看] 作業相關聯的範圍。</span><span class="sxs-lookup"><span data-stu-id="624d9-191">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="624d9-192">這包括訂閱範圍的 [訂閱/{subscriptionId}]、[訂閱/{subscriptionId}/resourceGroups/{resourceGroupName} "（針對 resourceGroup 範圍）。提供者/Microsoft. 帳單/billingAccounts/{billingAccountId} ' for 帳單帳戶範圍，" 提供者/Microsoft. 帳單/billingAccounts/{billingAccountId}/部門/{departmentId} "的部門範圍，" 提供者/microsoft. 帳單/billingAccounts/{billingAccountId} "（適用于 EnrollmentAccounts 範圍，" 供應商/Microsoft]）。帳單/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId} ' for BillingProfile 範圍，' 提供者/Microsoft. 帳單/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId} ' 適用于 InvoiceSection 範圍，' 提供者/Microsoft. 管理/managementGroups/{managementGroupId} ' 管理群組範圍、' 提供者/Microsoft. CostManagement/externalBillingAccounts/{externalBillingAccountName}」（適用于外部帳單帳戶範圍和「提供者/CostManagement/externalSubscriptions/{externalSubscriptionName}」）。</span><span class="sxs-lookup"><span data-stu-id="624d9-192">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="624d9-193">`[ViewName <String>]`：視圖名稱</span><span class="sxs-lookup"><span data-stu-id="624d9-193">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="624d9-194">相關連結</span><span class="sxs-lookup"><span data-stu-id="624d9-194">RELATED LINKS</span></span>

