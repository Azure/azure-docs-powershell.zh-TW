---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDiagnosticSetting.md
ms.openlocfilehash: eeadf64c83f62a8d245a7ace8f750b34ddc230ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100134058"
---
# <span data-ttu-id="32770-101">Set-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="32770-101">Set-AzDiagnosticSetting</span></span>

## <span data-ttu-id="32770-102">摘要</span><span class="sxs-lookup"><span data-stu-id="32770-102">SYNOPSIS</span></span>
<span data-ttu-id="32770-103">設定資源的記錄和標準設定。</span><span class="sxs-lookup"><span data-stu-id="32770-103">Sets the logs and metrics settings for the resource.</span></span>

## <span data-ttu-id="32770-104">句法</span><span class="sxs-lookup"><span data-stu-id="32770-104">SYNTAX</span></span>

### <span data-ttu-id="32770-105">OldSetDiagnosticSetting (預設) </span><span class="sxs-lookup"><span data-stu-id="32770-105">OldSetDiagnosticSetting (Default)</span></span>
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

### <span data-ttu-id="32770-106">NewSetDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="32770-106">NewSetDiagnosticSetting</span></span>
```
Set-AzDiagnosticSetting -InputObject <PSServiceDiagnosticSettings> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32770-107">說明</span><span class="sxs-lookup"><span data-stu-id="32770-107">DESCRIPTION</span></span>
<span data-ttu-id="32770-108">**AzDiagnosticSetting** Cmdlet 可針對特定資源啟用或停用每個時間細微性與記錄類別。</span><span class="sxs-lookup"><span data-stu-id="32770-108">The **Set-AzDiagnosticSetting** cmdlet enables or disables each time grain and log category for the particular resource.</span></span>
<span data-ttu-id="32770-109">記錄和度量單位儲存在指定的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="32770-109">The logs and metrics are stored in the specified storage account.</span></span>
<span data-ttu-id="32770-110">這個 Cmdlet 會實現 ShouldProcess 模式，亦即，在實際建立、修改或移除資源之前，它可能會要求使用者進行確認。</span><span class="sxs-lookup"><span data-stu-id="32770-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="32770-111">示例</span><span class="sxs-lookup"><span data-stu-id="32770-111">EXAMPLES</span></span>

### <span data-ttu-id="32770-112">範例1：啟用資源的所有度量及記錄</span><span class="sxs-lookup"><span data-stu-id="32770-112">Example 1: Enable all metrics and logs for a resource</span></span>
```powershell
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True
```

<span data-ttu-id="32770-113">這個命令會啟用 Resource01 的所有可用度量值和記錄。</span><span class="sxs-lookup"><span data-stu-id="32770-113">This command enables all available metrics and logs for Resource01.</span></span>

### <span data-ttu-id="32770-114">範例2：停用所有的度量及記錄</span><span class="sxs-lookup"><span data-stu-id="32770-114">Example 2: Disable all metrics and logs</span></span>
```powershell
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $False
```

<span data-ttu-id="32770-115">這個命令會針對資源 Resource01 停用所有可用的度量和記錄。</span><span class="sxs-lookup"><span data-stu-id="32770-115">This command disables all available metrics and logs for the resource Resource01.</span></span>

### <span data-ttu-id="32770-116">範例3：啟用/停用多個公制類別</span><span class="sxs-lookup"><span data-stu-id="32770-116">Example 3: Enable/disable multiple metrics categories</span></span>
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

<span data-ttu-id="32770-117">這個命令會停用稱為 Category1 和 Category2 的度量值類別。</span><span class="sxs-lookup"><span data-stu-id="32770-117">This command disables the metrics categories called Category1 and Category2.</span></span>
<span data-ttu-id="32770-118">所有其他類別都將保持不變。</span><span class="sxs-lookup"><span data-stu-id="32770-118">All the other categories remain the same.</span></span>

### <span data-ttu-id="32770-119">範例4：啟用/停用多個記錄類別</span><span class="sxs-lookup"><span data-stu-id="32770-119">Example 4: Enable/disable multiple log categories</span></span>
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

<span data-ttu-id="32770-120">這個命令會啟用 Category1 和 Category2。</span><span class="sxs-lookup"><span data-stu-id="32770-120">This command enables Category1 and Category2.</span></span>
<span data-ttu-id="32770-121">所有其他的度量標準與記錄類別都保持不變。</span><span class="sxs-lookup"><span data-stu-id="32770-121">All the other metrics and logs categories remain the same.</span></span>

### <span data-ttu-id="32770-122">範例5：啟用時間細微性和多個類別</span><span class="sxs-lookup"><span data-stu-id="32770-122">Example 5: Enable a time grain and multiple categories</span></span>
```powershell
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Category Category1,Category2 -Timegrain PT1M
```

<span data-ttu-id="32770-123">這個命令只啟用 Category1、Category2 和時間細微性 PT1M。</span><span class="sxs-lookup"><span data-stu-id="32770-123">This command enables only Category1, Category2, and time grain PT1M.</span></span>
<span data-ttu-id="32770-124">所有其他時間 grains 和類別都不會改變。</span><span class="sxs-lookup"><span data-stu-id="32770-124">All other time grains and categories are unchanged.</span></span>

### <span data-ttu-id="32770-125">範例6：使用管線</span><span class="sxs-lookup"><span data-stu-id="32770-125">Example 6: Using pipeline</span></span>
```powershell
PS C:\>Get-AzDiagnosticSetting -ResourceId "Resource01" | Set-AzDiagnosticSetting -Enabled $True -Category Category1,Category2
```

<span data-ttu-id="32770-126">這個命令會使用 PowerShell 管線來設定 (不會變更診斷設定) 進行變更。</span><span class="sxs-lookup"><span data-stu-id="32770-126">This command uses the PowerShell pipeline to set (no change made) a diagnostic setting.</span></span>

## <span data-ttu-id="32770-127">參數</span><span class="sxs-lookup"><span data-stu-id="32770-127">PARAMETERS</span></span>

### <span data-ttu-id="32770-128">-類別</span><span class="sxs-lookup"><span data-stu-id="32770-128">-Category</span></span>
<span data-ttu-id="32770-129">根據 *Enabled* 的值，指定要啟用或停用的記錄類別清單。</span><span class="sxs-lookup"><span data-stu-id="32770-129">Specifies the list of log categories to enable or disable, according to the value of *Enabled*.</span></span>
<span data-ttu-id="32770-130">如果未指定任何類別，此命令會在所有支援的類別上執行。</span><span class="sxs-lookup"><span data-stu-id="32770-130">If no category is specified, this command operates on all supported categories.</span></span> 

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

### <span data-ttu-id="32770-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32770-131">-DefaultProfile</span></span>
<span data-ttu-id="32770-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="32770-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="32770-133">-啟用</span><span class="sxs-lookup"><span data-stu-id="32770-133">-Enabled</span></span>
<span data-ttu-id="32770-134">指出是否要啟用診斷。</span><span class="sxs-lookup"><span data-stu-id="32770-134">Indicates whether to enable diagnostics.</span></span>
<span data-ttu-id="32770-135">指定 $True 以啟用診斷，或 $False 以停用診斷程式。</span><span class="sxs-lookup"><span data-stu-id="32770-135">Specify $True to enable diagnostics, or $False to disable diagnostics.</span></span>

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

### <span data-ttu-id="32770-136">-EnableLog</span><span class="sxs-lookup"><span data-stu-id="32770-136">-EnableLog</span></span>
<span data-ttu-id="32770-137">指示是否應該啟用或停用診斷記錄的值</span><span class="sxs-lookup"><span data-stu-id="32770-137">The value indicating whether the diagnostic logs should be enabled or disabled</span></span>

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

### <span data-ttu-id="32770-138">-EnableMetrics</span><span class="sxs-lookup"><span data-stu-id="32770-138">-EnableMetrics</span></span>
<span data-ttu-id="32770-139">指示是否應該啟用或停用診斷指標的值</span><span class="sxs-lookup"><span data-stu-id="32770-139">The value indicating whether the diagnostic metrics should be enabled or disabled</span></span>

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

### <span data-ttu-id="32770-140">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="32770-140">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="32770-141">事件中心授權規則識別碼</span><span class="sxs-lookup"><span data-stu-id="32770-141">The event hub authorization rule id</span></span>

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

### <span data-ttu-id="32770-142">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="32770-142">-EventHubName</span></span>
<span data-ttu-id="32770-143">事件中樞名稱</span><span class="sxs-lookup"><span data-stu-id="32770-143">The event hub name</span></span>

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

### <span data-ttu-id="32770-144">-ExportToResourceSpecific</span><span class="sxs-lookup"><span data-stu-id="32770-144">-ExportToResourceSpecific</span></span>
<span data-ttu-id="32770-145">指示必須完成匯出至 LA 的旗標到資源特定資料表，請 a.k.a。</span><span class="sxs-lookup"><span data-stu-id="32770-145">Flag indicating that the export to LA must be done to a resource specific table, a.k.a.</span></span> <span data-ttu-id="32770-146">[專用] 或 [固定架構] 資料表，而不是稱為 **AzureDiagnostics** 的 **預設** 動態架構資料表。</span><span class="sxs-lookup"><span data-stu-id="32770-146">dedicated or fixed schema table, as opposed to the **default** dynamic schema table called **AzureDiagnostics**.</span></span>

<span data-ttu-id="32770-147">這個引數只會在指定了引數 **workspaceId** 時有效。</span><span class="sxs-lookup"><span data-stu-id="32770-147">This argument is effective only when the argument **-workspaceId** is also given.</span></span>

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

### <span data-ttu-id="32770-148">-InputObject</span><span class="sxs-lookup"><span data-stu-id="32770-148">-InputObject</span></span>
<span data-ttu-id="32770-149">輸入物件 (來自管線的可能。 ) 將會從這個物件中提取名稱和 resourceId。</span><span class="sxs-lookup"><span data-stu-id="32770-149">The input object (possible from the pipeline.) The name and resourceId will be extracted from this object.</span></span>

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

### <span data-ttu-id="32770-150">-MetricCategory</span><span class="sxs-lookup"><span data-stu-id="32770-150">-MetricCategory</span></span>
<span data-ttu-id="32770-151">[公制] 類別的清單。</span><span class="sxs-lookup"><span data-stu-id="32770-151">The list of metric categories.</span></span> <span data-ttu-id="32770-152">如果未指定任何類別，此命令會在所有支援的類別上執行。</span><span class="sxs-lookup"><span data-stu-id="32770-152">If no category is specified, this command operates on all supported categories.</span></span> 

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

### <span data-ttu-id="32770-153">-名稱</span><span class="sxs-lookup"><span data-stu-id="32770-153">-Name</span></span>
<span data-ttu-id="32770-154">診斷設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="32770-154">The name of the diagnostic setting.</span></span> <span data-ttu-id="32770-155">預設值為 [ **服務**]。</span><span class="sxs-lookup"><span data-stu-id="32770-155">The default value is **service**.</span></span>

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

### <span data-ttu-id="32770-156">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="32770-156">-ResourceId</span></span>
<span data-ttu-id="32770-157">指定資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="32770-157">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="32770-158">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="32770-158">-RetentionEnabled</span></span>
<span data-ttu-id="32770-159">指出是否已啟用診斷資訊的保留。</span><span class="sxs-lookup"><span data-stu-id="32770-159">Indicates whether retention of diagnostic information is enabled.</span></span>

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

### <span data-ttu-id="32770-160">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="32770-160">-RetentionInDays</span></span>
<span data-ttu-id="32770-161">指定保留原則（以天為單位）。</span><span class="sxs-lookup"><span data-stu-id="32770-161">Specifies the retention policy, in days.</span></span>

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

### <span data-ttu-id="32770-162">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="32770-162">-ServiceBusRuleId</span></span>
<span data-ttu-id="32770-163">服務匯流排規則 id。</span><span class="sxs-lookup"><span data-stu-id="32770-163">The Service Bus Rule id.</span></span>

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

### <span data-ttu-id="32770-164">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="32770-164">-StorageAccountId</span></span>
<span data-ttu-id="32770-165">指定要儲存資料的儲存空間帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="32770-165">Specifies the ID of the Storage account in which to save the data.</span></span>

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

### <span data-ttu-id="32770-166">-Timegrain</span><span class="sxs-lookup"><span data-stu-id="32770-166">-Timegrain</span></span>
<span data-ttu-id="32770-167">根據 [ *Enabled*] 的值，指定要啟用或停用度量單位的時間 grains。</span><span class="sxs-lookup"><span data-stu-id="32770-167">Specifies the time grains to enable or disable for metrics, according to the value of *Enabled*.</span></span>
<span data-ttu-id="32770-168">如果您沒有指定時間細微性，這個命令會在所有可用的時間 grains 上執行。</span><span class="sxs-lookup"><span data-stu-id="32770-168">If you do not specify a time grain, this command operates on all available time grains.</span></span>

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

### <span data-ttu-id="32770-169">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="32770-169">-WorkspaceId</span></span>
<span data-ttu-id="32770-170">要傳送記錄/度量單位之 Log Analytics 工作區的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="32770-170">The resource Id of the Log Analytics workspace to send logs/metrics to</span></span>

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

### <span data-ttu-id="32770-171">-確認</span><span class="sxs-lookup"><span data-stu-id="32770-171">-Confirm</span></span>
<span data-ttu-id="32770-172">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="32770-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32770-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32770-173">-WhatIf</span></span>
<span data-ttu-id="32770-174">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="32770-174">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="32770-175">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="32770-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32770-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32770-176">CommonParameters</span></span>
<span data-ttu-id="32770-177">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="32770-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32770-178">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="32770-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32770-179">輸入</span><span class="sxs-lookup"><span data-stu-id="32770-179">INPUTS</span></span>

### <span data-ttu-id="32770-180">PSServiceDiagnosticSettings 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="32770-180">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

### <span data-ttu-id="32770-181">System.object</span><span class="sxs-lookup"><span data-stu-id="32770-181">System.String</span></span>

### <span data-ttu-id="32770-182">System.object</span><span class="sxs-lookup"><span data-stu-id="32770-182">System.Boolean</span></span>

### <span data-ttu-id="32770-183">[System.object]。清單 ' 1 [CoreLib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="32770-183">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="32770-184">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="32770-184">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="32770-185">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="32770-185">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="32770-186">輸出</span><span class="sxs-lookup"><span data-stu-id="32770-186">OUTPUTS</span></span>

### <span data-ttu-id="32770-187">PSServiceDiagnosticSettings 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="32770-187">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="32770-188">筆記</span><span class="sxs-lookup"><span data-stu-id="32770-188">NOTES</span></span>

## <span data-ttu-id="32770-189">相關連結</span><span class="sxs-lookup"><span data-stu-id="32770-189">RELATED LINKS</span></span>

<span data-ttu-id="32770-190">[AzDiagnosticSetting](./Get-AzDiagnosticSetting.md) 
[移除-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="32770-190">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md)
[Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span></span>
