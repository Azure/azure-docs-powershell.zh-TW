---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/powershell/module/az.monitor/set-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDiagnosticSetting.md
ms.openlocfilehash: 148986d5ab16e4791a4c886f5ba4557b6dc90fba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904033"
---
# <span data-ttu-id="10fd6-101">Set-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="10fd6-101">Set-AzDiagnosticSetting</span></span>

## <span data-ttu-id="10fd6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="10fd6-102">SYNOPSIS</span></span>
<span data-ttu-id="10fd6-103">設定資源的記錄與計量設定。</span><span class="sxs-lookup"><span data-stu-id="10fd6-103">Sets the logs and metrics settings for the resource.</span></span>

## <span data-ttu-id="10fd6-104">語法</span><span class="sxs-lookup"><span data-stu-id="10fd6-104">SYNTAX</span></span>

### <span data-ttu-id="10fd6-105">OldSetDiagnosticSetting (預設) </span><span class="sxs-lookup"><span data-stu-id="10fd6-105">OldSetDiagnosticSetting (Default)</span></span>
```
Set-AzDiagnosticSetting -ResourceId <String> [-Name <String>] [-StorageAccountId <String>]
 [-ServiceBusRuleId <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleId <String>]
 [-Enabled <Boolean>] [-Category <System.Collections.Generic.List`1[System.String]>]
 [-MetricCategory <System.Collections.Generic.List`1[System.String]>]
 [-Timegrain <System.Collections.Generic.List`1[System.String]>] [-RetentionEnabled <Boolean>]
 [-WorkspaceId <String>] [-RetentionInDays <Int32>] [-ExportToResourceSpecific] [-EnableLog <Boolean>]
 [-EnableMetrics <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="10fd6-106">NewSetDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="10fd6-106">NewSetDiagnosticSetting</span></span>
```
Set-AzDiagnosticSetting -InputObject <PSServiceDiagnosticSettings> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10fd6-107">描述</span><span class="sxs-lookup"><span data-stu-id="10fd6-107">DESCRIPTION</span></span>
<span data-ttu-id="10fd6-108">**Set-AzDiagnosticSetting** Cmdlet 會啟用或停用特定資源的每一個紋理和記錄類別。</span><span class="sxs-lookup"><span data-stu-id="10fd6-108">The **Set-AzDiagnosticSetting** cmdlet enables or disables each time grain and log category for the particular resource.</span></span>
<span data-ttu-id="10fd6-109">記錄與計量會儲存在指定的儲存帳戶中。</span><span class="sxs-lookup"><span data-stu-id="10fd6-109">The logs and metrics are stored in the specified storage account.</span></span>
<span data-ttu-id="10fd6-110">此 Cmdlet 實做 ShouldProcess 模式，即實際建立、修改或移除資源之前，可能會向使用者要求確認。</span><span class="sxs-lookup"><span data-stu-id="10fd6-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="10fd6-111">例子</span><span class="sxs-lookup"><span data-stu-id="10fd6-111">EXAMPLES</span></span>

### <span data-ttu-id="10fd6-112">範例 1：啟用資源的所有計量和記錄</span><span class="sxs-lookup"><span data-stu-id="10fd6-112">Example 1: Enable all metrics and logs for a resource</span></span>
```powershell
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True
```

<span data-ttu-id="10fd6-113">此命令會啟用 Resource01 的所有可用計量和記錄。</span><span class="sxs-lookup"><span data-stu-id="10fd6-113">This command enables all available metrics and logs for Resource01.</span></span>

### <span data-ttu-id="10fd6-114">範例 2：停用所有計量和記錄</span><span class="sxs-lookup"><span data-stu-id="10fd6-114">Example 2: Disable all metrics and logs</span></span>
```powershell
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $False
```

<span data-ttu-id="10fd6-115">此命令會停用資源資源01 的所有可用計量和記錄。</span><span class="sxs-lookup"><span data-stu-id="10fd6-115">This command disables all available metrics and logs for the resource Resource01.</span></span>

### <span data-ttu-id="10fd6-116">範例 3：啟用/停用多個計量類別</span><span class="sxs-lookup"><span data-stu-id="10fd6-116">Example 3: Enable/disable multiple metrics categories</span></span>
```powershell
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $False -MetricCategory MetricCategory1,MetricCategory2
StorageAccountId   : <storageAccountId>
StorageAccountName : <storageAccountName>
Metrics
   Enabled   : False
   Category  : MetricCategory1
   Timegrain : PT1M
   Enabled   : False
   Category  : MetricCategory2
   Timegrain : PT1H
   Enabled   : True
   Category  : MetricCategory3
   Timegrain : PT1H
Logs
   Enabled  : True
   Category : Category1
   Enabled  : True
   Category : Category2
   Enabled  : True
   Category : Category3
   Enabled  : False
   Category : Category4
```

<span data-ttu-id="10fd6-117">此命令會停用名為 Category1 和 Category2 的度量類別。</span><span class="sxs-lookup"><span data-stu-id="10fd6-117">This command disables the metrics categories called Category1 and Category2.</span></span>
<span data-ttu-id="10fd6-118">所有其他類別都保持不變。</span><span class="sxs-lookup"><span data-stu-id="10fd6-118">All the other categories remain the same.</span></span>

### <span data-ttu-id="10fd6-119">範例 4：啟用/停用多個記錄類別</span><span class="sxs-lookup"><span data-stu-id="10fd6-119">Example 4: Enable/disable multiple log categories</span></span>
```powershell
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Category Category1,Category2
StorageAccountId   : <storageAccountId>
StorageAccountName : <storageAccountName>
Metrics
   Enabled   : False
   Category  : MetricCategory1
   Timegrain : PT1M
   Enabled   : False
   Category  : MetricCategory2
   Timegrain : PT1H
   Enabled   : True
   Category  : MetricCategory3
   Timegrain : PT1H
Logs
   Enabled  : True
   Category : Category1
   Enabled  : True
   Category : Category2
   Enabled  : True
   Category : Category3
   Enabled  : False
   Category : Category4
```

<span data-ttu-id="10fd6-120">此命令會啟用 Category1 和 Category2。</span><span class="sxs-lookup"><span data-stu-id="10fd6-120">This command enables Category1 and Category2.</span></span>
<span data-ttu-id="10fd6-121">所有其他計量和記錄類別都保持不變。</span><span class="sxs-lookup"><span data-stu-id="10fd6-121">All the other metrics and logs categories remain the same.</span></span>

### <span data-ttu-id="10fd6-122">範例 5：啟用時間紋理和多個類別</span><span class="sxs-lookup"><span data-stu-id="10fd6-122">Example 5: Enable a time grain and multiple categories</span></span>
```powershell
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Category Category1,Category2 -Timegrain PT1M
```

<span data-ttu-id="10fd6-123">此命令僅啟用 Category1、Category2 和 time grain PT1M。</span><span class="sxs-lookup"><span data-stu-id="10fd6-123">This command enables only Category1, Category2, and time grain PT1M.</span></span>
<span data-ttu-id="10fd6-124">所有其他時間量和類別均保持不變。</span><span class="sxs-lookup"><span data-stu-id="10fd6-124">All other time grains and categories are unchanged.</span></span>

### <span data-ttu-id="10fd6-125">範例 6：使用管線</span><span class="sxs-lookup"><span data-stu-id="10fd6-125">Example 6: Using pipeline</span></span>
```powershell
PS C:\>Get-AzDiagnosticSetting -ResourceId "Resource01" | Set-AzDiagnosticSetting -Enabled $True -Category Category1,Category2
```

<span data-ttu-id="10fd6-126">此命令使用 PowerShell 管線來 (診斷設定) 變更。</span><span class="sxs-lookup"><span data-stu-id="10fd6-126">This command uses the PowerShell pipeline to set (no change made) a diagnostic setting.</span></span>

## <span data-ttu-id="10fd6-127">參數</span><span class="sxs-lookup"><span data-stu-id="10fd6-127">PARAMETERS</span></span>

### <span data-ttu-id="10fd6-128">-類別</span><span class="sxs-lookup"><span data-stu-id="10fd6-128">-Category</span></span>
<span data-ttu-id="10fd6-129">根據 Enabled 的值指定要啟用或停用的記錄 *類別清單*。</span><span class="sxs-lookup"><span data-stu-id="10fd6-129">Specifies the list of log categories to enable or disable, according to the value of *Enabled*.</span></span>
<span data-ttu-id="10fd6-130">如果沒有指定類別，此命令會在所有支援的類別上執行。</span><span class="sxs-lookup"><span data-stu-id="10fd6-130">If no category is specified, this command operates on all supported categories.</span></span> 

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10fd6-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10fd6-131">-DefaultProfile</span></span>
<span data-ttu-id="10fd6-132">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="10fd6-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10fd6-133">-已啟用</span><span class="sxs-lookup"><span data-stu-id="10fd6-133">-Enabled</span></span>
<span data-ttu-id="10fd6-134">指出是否要啟用診斷。</span><span class="sxs-lookup"><span data-stu-id="10fd6-134">Indicates whether to enable diagnostics.</span></span>
<span data-ttu-id="10fd6-135">指定$True以啟用診斷，或$False停用診斷。</span><span class="sxs-lookup"><span data-stu-id="10fd6-135">Specify $True to enable diagnostics, or $False to disable diagnostics.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10fd6-136">-EnableLog</span><span class="sxs-lookup"><span data-stu-id="10fd6-136">-EnableLog</span></span>
<span data-ttu-id="10fd6-137">指出診斷記錄是否應該啟用或停用的值</span><span class="sxs-lookup"><span data-stu-id="10fd6-137">The value indicating whether the diagnostic logs should be enabled or disabled</span></span>

```yaml
Type: System.Boolean
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10fd6-138">-EnableMetrics</span><span class="sxs-lookup"><span data-stu-id="10fd6-138">-EnableMetrics</span></span>
<span data-ttu-id="10fd6-139">指出診斷計量是否應該啟用或停用的值</span><span class="sxs-lookup"><span data-stu-id="10fd6-139">The value indicating whether the diagnostic metrics should be enabled or disabled</span></span>

```yaml
Type: System.Boolean
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10fd6-140">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="10fd6-140">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="10fd6-141">事件中樞授權規則識別碼</span><span class="sxs-lookup"><span data-stu-id="10fd6-141">The event hub authorization rule id</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10fd6-142">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="10fd6-142">-EventHubName</span></span>
<span data-ttu-id="10fd6-143">事件中樞名稱</span><span class="sxs-lookup"><span data-stu-id="10fd6-143">The event hub name</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10fd6-144">-ExportToResourceS指定</span><span class="sxs-lookup"><span data-stu-id="10fd6-144">-ExportToResourceSpecific</span></span>
<span data-ttu-id="10fd6-145">指出匯出至 LA 的標號必須匯出至資源特定的資料表，即 a.k.a。</span><span class="sxs-lookup"><span data-stu-id="10fd6-145">Flag indicating that the export to LA must be done to a resource specific table, a.k.a.</span></span> <span data-ttu-id="10fd6-146">專用或固定架構資料表，與稱為 **AzureDiagnostics 的預設動態架構資料表相反**。 </span><span class="sxs-lookup"><span data-stu-id="10fd6-146">dedicated or fixed schema table, as opposed to the **default** dynamic schema table called **AzureDiagnostics**.</span></span>

<span data-ttu-id="10fd6-147">只有在同時提供引數 **-workspaceId** 時，此引數才有效。</span><span class="sxs-lookup"><span data-stu-id="10fd6-147">This argument is effective only when the argument **-workspaceId** is also given.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10fd6-148">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10fd6-148">-InputObject</span></span>
<span data-ttu-id="10fd6-149">從管線 (輸入物件。) 會從此物件解壓縮名稱與 resourceId。</span><span class="sxs-lookup"><span data-stu-id="10fd6-149">The input object (possible from the pipeline.) The name and resourceId will be extracted from this object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings
Parameter Sets: NewSetDiagnosticSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10fd6-150">-MetricCategory</span><span class="sxs-lookup"><span data-stu-id="10fd6-150">-MetricCategory</span></span>
<span data-ttu-id="10fd6-151">公制類別清單。</span><span class="sxs-lookup"><span data-stu-id="10fd6-151">The list of metric categories.</span></span> <span data-ttu-id="10fd6-152">如果沒有指定類別，此命令會在所有支援的類別上執行。</span><span class="sxs-lookup"><span data-stu-id="10fd6-152">If no category is specified, this command operates on all supported categories.</span></span> 

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10fd6-153">-名稱</span><span class="sxs-lookup"><span data-stu-id="10fd6-153">-Name</span></span>
<span data-ttu-id="10fd6-154">診斷設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="10fd6-154">The name of the diagnostic setting.</span></span> <span data-ttu-id="10fd6-155">預設值為 **服務**。</span><span class="sxs-lookup"><span data-stu-id="10fd6-155">The default value is **service**.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10fd6-156">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10fd6-156">-ResourceId</span></span>
<span data-ttu-id="10fd6-157">指定資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="10fd6-157">Specifies the ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10fd6-158">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="10fd6-158">-RetentionEnabled</span></span>
<span data-ttu-id="10fd6-159">指出是否已啟用診斷資訊的保留。</span><span class="sxs-lookup"><span data-stu-id="10fd6-159">Indicates whether retention of diagnostic information is enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10fd6-160">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="10fd6-160">-RetentionInDays</span></span>
<span data-ttu-id="10fd6-161">指定保留政策 ，以天數表示。</span><span class="sxs-lookup"><span data-stu-id="10fd6-161">Specifies the retention policy, in days.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10fd6-162">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="10fd6-162">-ServiceBusRuleId</span></span>
<span data-ttu-id="10fd6-163">服務母線規則識別碼。</span><span class="sxs-lookup"><span data-stu-id="10fd6-163">The Service Bus Rule id.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10fd6-164">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="10fd6-164">-StorageAccountId</span></span>
<span data-ttu-id="10fd6-165">指定儲存資料的儲存空間帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="10fd6-165">Specifies the ID of the Storage account in which to save the data.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10fd6-166">-Timegrain</span><span class="sxs-lookup"><span data-stu-id="10fd6-166">-Timegrain</span></span>
<span data-ttu-id="10fd6-167">根據 Enabled 的值指定要啟用或停用度量的時間 *量*。</span><span class="sxs-lookup"><span data-stu-id="10fd6-167">Specifies the time grains to enable or disable for metrics, according to the value of *Enabled*.</span></span>
<span data-ttu-id="10fd6-168">如果您未指定時間紋理，此命令會以所有可用的時間紋理操作。</span><span class="sxs-lookup"><span data-stu-id="10fd6-168">If you do not specify a time grain, this command operates on all available time grains.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10fd6-169">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="10fd6-169">-WorkspaceId</span></span>
<span data-ttu-id="10fd6-170">記錄分析工作區的資源識別碼，可傳送記錄/計量至</span><span class="sxs-lookup"><span data-stu-id="10fd6-170">The resource Id of the Log Analytics workspace to send logs/metrics to</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10fd6-171">-確認</span><span class="sxs-lookup"><span data-stu-id="10fd6-171">-Confirm</span></span>
<span data-ttu-id="10fd6-172">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="10fd6-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10fd6-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10fd6-173">-WhatIf</span></span>
<span data-ttu-id="10fd6-174">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="10fd6-174">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="10fd6-175">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="10fd6-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10fd6-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10fd6-176">CommonParameters</span></span>
<span data-ttu-id="10fd6-177">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="10fd6-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10fd6-178">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="10fd6-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10fd6-179">輸入</span><span class="sxs-lookup"><span data-stu-id="10fd6-179">INPUTS</span></span>

### <span data-ttu-id="10fd6-180">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="10fd6-180">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

### <span data-ttu-id="10fd6-181">System.String</span><span class="sxs-lookup"><span data-stu-id="10fd6-181">System.String</span></span>

### <span data-ttu-id="10fd6-182">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="10fd6-182">System.Boolean</span></span>

### <span data-ttu-id="10fd6-183">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="10fd6-183">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="10fd6-184">System.Nullable'1[[System.Boolean， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="10fd6-184">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="10fd6-185">System.Nullable'1[[System.Int32， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="10fd6-185">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="10fd6-186">輸出</span><span class="sxs-lookup"><span data-stu-id="10fd6-186">OUTPUTS</span></span>

### <span data-ttu-id="10fd6-187">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="10fd6-187">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="10fd6-188">筆記</span><span class="sxs-lookup"><span data-stu-id="10fd6-188">NOTES</span></span>

## <span data-ttu-id="10fd6-189">相關連結</span><span class="sxs-lookup"><span data-stu-id="10fd6-189">RELATED LINKS</span></span>

<span data-ttu-id="10fd6-190">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md) 
[Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="10fd6-190">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md)
[Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span></span>
