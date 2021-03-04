---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.costmanagement/update-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Update-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Update-AzCostManagementExport.md
ms.openlocfilehash: d4be10cf33952b026ceabe6cd407929acbe5c058
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902109"
---
# <span data-ttu-id="916fb-101">Update-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="916fb-101">Update-AzCostManagementExport</span></span>

## <span data-ttu-id="916fb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="916fb-102">SYNOPSIS</span></span>
<span data-ttu-id="916fb-103">建立或更新匯出的作業。</span><span class="sxs-lookup"><span data-stu-id="916fb-103">The operation to create or update a export.</span></span>
<span data-ttu-id="916fb-104">更新作業需要在要求中設定最新的 eTag。</span><span class="sxs-lookup"><span data-stu-id="916fb-104">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="916fb-105">您可以執行 get 運算來取得最新的 eTag。</span><span class="sxs-lookup"><span data-stu-id="916fb-105">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="916fb-106">建立作業不需要 eTag。</span><span class="sxs-lookup"><span data-stu-id="916fb-106">Create operation does not require eTag.</span></span>

## <span data-ttu-id="916fb-107">語法</span><span class="sxs-lookup"><span data-stu-id="916fb-107">SYNTAX</span></span>

### <span data-ttu-id="916fb-108">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="916fb-108">UpdateExpanded (Default)</span></span>
```
Update-AzCostManagementExport -Name <String> -Scope <String> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-ETag <String>] [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="916fb-109">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="916fb-109">UpdateViaIdentityExpanded</span></span>
```
Update-AzCostManagementExport -InputObject <ICostManagementIdentity> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-ETag <String>] [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="916fb-110">描述</span><span class="sxs-lookup"><span data-stu-id="916fb-110">DESCRIPTION</span></span>
<span data-ttu-id="916fb-111">建立或更新匯出的作業。</span><span class="sxs-lookup"><span data-stu-id="916fb-111">The operation to create or update a export.</span></span>
<span data-ttu-id="916fb-112">更新作業需要在要求中設定最新的 eTag。</span><span class="sxs-lookup"><span data-stu-id="916fb-112">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="916fb-113">您可以執行 get 運算來取得最新的 eTag。</span><span class="sxs-lookup"><span data-stu-id="916fb-113">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="916fb-114">建立作業不需要 eTag。</span><span class="sxs-lookup"><span data-stu-id="916fb-114">Create operation does not require eTag.</span></span>

## <span data-ttu-id="916fb-115">例子</span><span class="sxs-lookup"><span data-stu-id="916fb-115">EXAMPLES</span></span>

### <span data-ttu-id="916fb-116">範例 1：根據範圍和名稱更新 AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="916fb-116">Example 1: Update AzCostManagementExport by scope and name</span></span>
```powershell
PS C:\> Update-AzCostManagementExport -Scope "subscriptions//*********" -Name "TestExport" -ScheduleRecurrence 'Weekly'

ETag              Name                                 Type
----              ----                                 ----
"********" TestExportDatasetAggregationInfo Microsoft.CostManagement/exports
```

<span data-ttu-id="916fb-117">根據範圍和名稱更新 AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="916fb-117">Update AzCostManagementExport by Scope and name</span></span>

### <span data-ttu-id="916fb-118">範例 2：Update AzCostManagementExport by InputObject</span><span class="sxs-lookup"><span data-stu-id="916fb-118">Example 2: Update AzCostManagementExport by InputObject</span></span>
```powershell
PS C:\> $oldExport = Get-AzCostManagementExport -Scope "subscriptions/*********" -Name "TestExport"
Update-AzCostManagementExport -InputObject $oldExport -ScheduleRecurrence 'Weekly'

ETag              Name                                 Type
----              ----                                 ----
"********" TestExportDatasetAggregationInfo Microsoft.CostManagement/exports
```

<span data-ttu-id="916fb-119">更新 AzCostManagementExport by InputObject</span><span class="sxs-lookup"><span data-stu-id="916fb-119">Update AzCostManagementExport by InputObject</span></span>

## <span data-ttu-id="916fb-120">參數</span><span class="sxs-lookup"><span data-stu-id="916fb-120">PARAMETERS</span></span>

### <span data-ttu-id="916fb-121">-ConfigurationColumn</span><span class="sxs-lookup"><span data-stu-id="916fb-121">-ConfigurationColumn</span></span>
<span data-ttu-id="916fb-122">要包含在匯出中的欄名稱陣列。</span><span class="sxs-lookup"><span data-stu-id="916fb-122">Array of column names to be included in the export.</span></span>
<span data-ttu-id="916fb-123">如果沒有提供，則匯出會包含所有可用的欄。</span><span class="sxs-lookup"><span data-stu-id="916fb-123">If not provided then the export will include all available columns.</span></span>
<span data-ttu-id="916fb-124">可用欄可能會依客戶通道而異， (範例) 。</span><span class="sxs-lookup"><span data-stu-id="916fb-124">The available columns can vary by customer channel (see examples).</span></span>

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

### <span data-ttu-id="916fb-125">-DataSetGranularity</span><span class="sxs-lookup"><span data-stu-id="916fb-125">-DataSetGranularity</span></span>
<span data-ttu-id="916fb-126">匯出中列的細微程度。</span><span class="sxs-lookup"><span data-stu-id="916fb-126">The granularity of rows in the export.</span></span>
<span data-ttu-id="916fb-127">目前僅支援 '每日'。</span><span class="sxs-lookup"><span data-stu-id="916fb-127">Currently only 'Daily' is supported.</span></span>

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

### <span data-ttu-id="916fb-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="916fb-128">-DefaultProfile</span></span>
<span data-ttu-id="916fb-129">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="916fb-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="916fb-130">-DefinitionTimeframe</span><span class="sxs-lookup"><span data-stu-id="916fb-130">-DefinitionTimeframe</span></span>
<span data-ttu-id="916fb-131">提取匯出資料的時間範圍。</span><span class="sxs-lookup"><span data-stu-id="916fb-131">The time frame for pulling data for the export.</span></span>
<span data-ttu-id="916fb-132">如果為自訂，則必須提供特定的時段。</span><span class="sxs-lookup"><span data-stu-id="916fb-132">If custom, then a specific time period must be provided.</span></span>

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

### <span data-ttu-id="916fb-133">-DefinitionType</span><span class="sxs-lookup"><span data-stu-id="916fb-133">-DefinitionType</span></span>
<span data-ttu-id="916fb-134">匯出的類型。</span><span class="sxs-lookup"><span data-stu-id="916fb-134">The type of the export.</span></span>
<span data-ttu-id="916fb-135">請注意，使用狀況相當於"ActualCost"，適用于尚未提供服務預約費用或攤銷資料之匯出。</span><span class="sxs-lookup"><span data-stu-id="916fb-135">Note that 'Usage' is equivalent to 'ActualCost' and is applicable to exports that do not yet provide data for charges or amortization for service reservations.</span></span>

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

### <span data-ttu-id="916fb-136">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="916fb-136">-DestinationContainer</span></span>
<span data-ttu-id="916fb-137">要上傳匯出的容器名稱。</span><span class="sxs-lookup"><span data-stu-id="916fb-137">The name of the container where exports will be uploaded.</span></span>

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

### <span data-ttu-id="916fb-138">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="916fb-138">-DestinationResourceId</span></span>
<span data-ttu-id="916fb-139">要傳送匯出的儲存空間帳戶資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="916fb-139">The resource id of the storage account where exports will be delivered.</span></span>

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

### <span data-ttu-id="916fb-140">-DestinationRootFolderPath</span><span class="sxs-lookup"><span data-stu-id="916fb-140">-DestinationRootFolderPath</span></span>
<span data-ttu-id="916fb-141">要上傳匯出的目錄名稱。</span><span class="sxs-lookup"><span data-stu-id="916fb-141">The name of the directory where exports will be uploaded.</span></span>

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

### <span data-ttu-id="916fb-142">-ETag</span><span class="sxs-lookup"><span data-stu-id="916fb-142">-ETag</span></span>
<span data-ttu-id="916fb-143">資源的 eTag。</span><span class="sxs-lookup"><span data-stu-id="916fb-143">eTag of the resource.</span></span>
<span data-ttu-id="916fb-144">若要處理並行更新案例，此欄位將用來判斷使用者是否要更新最新版本。</span><span class="sxs-lookup"><span data-stu-id="916fb-144">To handle concurrent update scenario, this field will be used to determine whether the user is updating the latest version or not.</span></span>

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

### <span data-ttu-id="916fb-145">-格式</span><span class="sxs-lookup"><span data-stu-id="916fb-145">-Format</span></span>
<span data-ttu-id="916fb-146">要傳遞之匯出的格式。</span><span class="sxs-lookup"><span data-stu-id="916fb-146">The format of the export being delivered.</span></span>
<span data-ttu-id="916fb-147">目前僅支援 'Csv'。</span><span class="sxs-lookup"><span data-stu-id="916fb-147">Currently only 'Csv' is supported.</span></span>

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

### <span data-ttu-id="916fb-148">-InputObject</span><span class="sxs-lookup"><span data-stu-id="916fb-148">-InputObject</span></span>
<span data-ttu-id="916fb-149">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="916fb-149">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="916fb-150">-名稱</span><span class="sxs-lookup"><span data-stu-id="916fb-150">-Name</span></span>
<span data-ttu-id="916fb-151">匯出名稱。</span><span class="sxs-lookup"><span data-stu-id="916fb-151">Export Name.</span></span>

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

### <span data-ttu-id="916fb-152">-RecurrencePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="916fb-152">-RecurrencePeriodFrom</span></span>
<span data-ttu-id="916fb-153">週期的開始日期。</span><span class="sxs-lookup"><span data-stu-id="916fb-153">The start date of recurrence.</span></span>

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

### <span data-ttu-id="916fb-154">-RecurrencePeriodTo</span><span class="sxs-lookup"><span data-stu-id="916fb-154">-RecurrencePeriodTo</span></span>
<span data-ttu-id="916fb-155">週期的結束日期。</span><span class="sxs-lookup"><span data-stu-id="916fb-155">The end date of recurrence.</span></span>

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

### <span data-ttu-id="916fb-156">-ScheduleRecurrence</span><span class="sxs-lookup"><span data-stu-id="916fb-156">-ScheduleRecurrence</span></span>
<span data-ttu-id="916fb-157">排程週期。</span><span class="sxs-lookup"><span data-stu-id="916fb-157">The schedule recurrence.</span></span>

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

### <span data-ttu-id="916fb-158">-ScheduleStatus</span><span class="sxs-lookup"><span data-stu-id="916fb-158">-ScheduleStatus</span></span>
<span data-ttu-id="916fb-159">匯出排程的狀態。</span><span class="sxs-lookup"><span data-stu-id="916fb-159">The status of the export's schedule.</span></span>
<span data-ttu-id="916fb-160">如果為非使用中，匯出的排程會暫停。</span><span class="sxs-lookup"><span data-stu-id="916fb-160">If 'Inactive', the export's schedule is paused.</span></span>

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

### <span data-ttu-id="916fb-161">-範圍</span><span class="sxs-lookup"><span data-stu-id="916fb-161">-Scope</span></span>
<span data-ttu-id="916fb-162">此參數會從不同的觀點定義成本管理的範圍，從"訂閱」、"ResourceGroup"和"提供服務"。</span><span class="sxs-lookup"><span data-stu-id="916fb-162">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="916fb-163">-TimePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="916fb-163">-TimePeriodFrom</span></span>
<span data-ttu-id="916fb-164">匯出資料的開始日期。</span><span class="sxs-lookup"><span data-stu-id="916fb-164">The start date for export data.</span></span>

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

### <span data-ttu-id="916fb-165">-TimePeriodTo</span><span class="sxs-lookup"><span data-stu-id="916fb-165">-TimePeriodTo</span></span>
<span data-ttu-id="916fb-166">匯出資料的結束日期。</span><span class="sxs-lookup"><span data-stu-id="916fb-166">The end date for export data.</span></span>

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

### <span data-ttu-id="916fb-167">-確認</span><span class="sxs-lookup"><span data-stu-id="916fb-167">-Confirm</span></span>
<span data-ttu-id="916fb-168">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="916fb-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="916fb-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="916fb-169">-WhatIf</span></span>
<span data-ttu-id="916fb-170">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="916fb-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="916fb-171">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="916fb-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="916fb-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="916fb-172">CommonParameters</span></span>
<span data-ttu-id="916fb-173">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="916fb-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="916fb-174">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="916fb-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="916fb-175">輸入</span><span class="sxs-lookup"><span data-stu-id="916fb-175">INPUTS</span></span>

### <span data-ttu-id="916fb-176">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.models.ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="916fb-176">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="916fb-177">輸出</span><span class="sxs-lookup"><span data-stu-id="916fb-177">OUTPUTS</span></span>

### <span data-ttu-id="916fb-178">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.models.Api20200601.IExport</span><span class="sxs-lookup"><span data-stu-id="916fb-178">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="916fb-179">筆記</span><span class="sxs-lookup"><span data-stu-id="916fb-179">NOTES</span></span>

<span data-ttu-id="916fb-180">別名</span><span class="sxs-lookup"><span data-stu-id="916fb-180">ALIASES</span></span>

<span data-ttu-id="916fb-181">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="916fb-181">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="916fb-182">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="916fb-182">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="916fb-183">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="916fb-183">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="916fb-184">INPUTOBJECT： <ICostManagementIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="916fb-184">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="916fb-185">`[AlertId <String>]`：警示識別碼</span><span class="sxs-lookup"><span data-stu-id="916fb-185">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="916fb-186">`[ExportName <String>]`：匯出名稱。</span><span class="sxs-lookup"><span data-stu-id="916fb-186">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="916fb-187">`[ExternalCloudProviderId <String>]`：這可以是連結帳戶的 '{externalSubscriptionId}'，或用於維度/查詢作業之合併帳戶的 '{externalBillingAccountId}'。</span><span class="sxs-lookup"><span data-stu-id="916fb-187">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="916fb-188">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`：與維度/查詢作業相關聯的外部雲端提供者類型。</span><span class="sxs-lookup"><span data-stu-id="916fb-188">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="916fb-189">這包括連結帳戶的'externalSubscriptions'，以及合併帳戶的'externalBillingAccount'。</span><span class="sxs-lookup"><span data-stu-id="916fb-189">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="916fb-190">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="916fb-190">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="916fb-191">`[Scope <String>]`：與視圖作業相關聯的範圍。</span><span class="sxs-lookup"><span data-stu-id="916fb-191">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="916fb-192">這包括訂閱範圍中的 'subscriptions/{subscriptionId}'，resourceGroup 範圍中的 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope， 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/department/{departmentId}' for Department 範圍， 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount範圍， BillingProfile 範圍中的 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}'， 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}'' for InvoiceSection 範圍， 'providers/Microsoft.Management /managementGroups/{managementGroupId}' for Management Group scope， 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccount}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription 範圍.</span><span class="sxs-lookup"><span data-stu-id="916fb-192">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="916fb-193">`[ViewName <String>]`：查看名稱</span><span class="sxs-lookup"><span data-stu-id="916fb-193">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="916fb-194">相關連結</span><span class="sxs-lookup"><span data-stu-id="916fb-194">RELATED LINKS</span></span>

