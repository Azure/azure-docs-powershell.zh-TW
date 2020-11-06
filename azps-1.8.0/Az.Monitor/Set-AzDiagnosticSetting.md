---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDiagnosticSetting.md
ms.openlocfilehash: 7c33c351b7daea7b39fd614a8d842a4ed8be7f2b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622232"
---
# <span data-ttu-id="38256-101">Set-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="38256-101">Set-AzDiagnosticSetting</span></span>

## <span data-ttu-id="38256-102">摘要</span><span class="sxs-lookup"><span data-stu-id="38256-102">SYNOPSIS</span></span>
<span data-ttu-id="38256-103">設定資源的記錄和標準設定。</span><span class="sxs-lookup"><span data-stu-id="38256-103">Sets the logs and metrics settings for the resource.</span></span>

## <span data-ttu-id="38256-104">句法</span><span class="sxs-lookup"><span data-stu-id="38256-104">SYNTAX</span></span>

### <span data-ttu-id="38256-105">OldSetDiagnosticSetting (預設) </span><span class="sxs-lookup"><span data-stu-id="38256-105">OldSetDiagnosticSetting (Default)</span></span>
```
Set-AzDiagnosticSetting -ResourceId <String> [-Name <String>] [-StorageAccountId <String>]
 [-ServiceBusRuleId <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleId <String>]
 [-Enabled <Boolean>] [-Category <System.Collections.Generic.List`1[System.String]>]
 [-MetricCategory <System.Collections.Generic.List`1[System.String]>]
 [-Timegrain <System.Collections.Generic.List`1[System.String]>] [-RetentionEnabled <Boolean>]
 [-WorkspaceId <String>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38256-106">NewSetDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="38256-106">NewSetDiagnosticSetting</span></span>
```
Set-AzDiagnosticSetting -InputObject <PSServiceDiagnosticSettings> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38256-107">說明</span><span class="sxs-lookup"><span data-stu-id="38256-107">DESCRIPTION</span></span>
<span data-ttu-id="38256-108">**AzDiagnosticSetting** Cmdlet 可針對特定資源啟用或停用每個時間細微性與記錄類別。</span><span class="sxs-lookup"><span data-stu-id="38256-108">The **Set-AzDiagnosticSetting** cmdlet enables or disables each time grain and log category for the particular resource.</span></span>
<span data-ttu-id="38256-109">記錄和度量單位儲存在指定的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="38256-109">The logs and metrics are stored in the specified storage account.</span></span>
<span data-ttu-id="38256-110">這個 Cmdlet 會實現 ShouldProcess 模式，亦即，在實際建立、修改或移除資源之前，它可能會要求使用者進行確認。</span><span class="sxs-lookup"><span data-stu-id="38256-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="38256-111">示例</span><span class="sxs-lookup"><span data-stu-id="38256-111">EXAMPLES</span></span>

### <span data-ttu-id="38256-112">範例1：啟用資源的所有度量及記錄</span><span class="sxs-lookup"><span data-stu-id="38256-112">Example 1: Enable all metrics and logs for a resource</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True
```

<span data-ttu-id="38256-113">這個命令會啟用 Resource01 的所有可用度量值和記錄。</span><span class="sxs-lookup"><span data-stu-id="38256-113">This command enables all available metrics and logs for Resource01.</span></span>

### <span data-ttu-id="38256-114">範例2：停用所有的度量及記錄</span><span class="sxs-lookup"><span data-stu-id="38256-114">Example 2: Disable all metrics and logs</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $False
```

<span data-ttu-id="38256-115">這個命令會針對資源 Resource01 停用所有可用的度量和記錄。</span><span class="sxs-lookup"><span data-stu-id="38256-115">This command disables all available metrics and logs for the resource Resource01.</span></span>

### <span data-ttu-id="38256-116">範例3：啟用/停用多個公制類別</span><span class="sxs-lookup"><span data-stu-id="38256-116">Example 3: Enable/disable multiple metrics categories</span></span>
```
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

<span data-ttu-id="38256-117">這個命令會停用名為 Category1 和 Category2 的度量單位 cateories。</span><span class="sxs-lookup"><span data-stu-id="38256-117">This command disables the metrics cateories called Category1 and Category2.</span></span>
<span data-ttu-id="38256-118">所有其他類別都將保持不變。</span><span class="sxs-lookup"><span data-stu-id="38256-118">All the other categories remain the same.</span></span>

### <span data-ttu-id="38256-119">範例4：啟用/停用多個記錄類別</span><span class="sxs-lookup"><span data-stu-id="38256-119">Example 4: Enable/disable multiple log categories</span></span>
```
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

<span data-ttu-id="38256-120">這個命令會啟用 Category1 和 Category2。</span><span class="sxs-lookup"><span data-stu-id="38256-120">This command enables Category1 and Category2.</span></span>
<span data-ttu-id="38256-121">所有其他的度量標準與記錄類別都保持不變。</span><span class="sxs-lookup"><span data-stu-id="38256-121">All the other metrics and logs categories remain the same.</span></span>

### <span data-ttu-id="38256-122">範例4：啟用時間細微性和多個類別</span><span class="sxs-lookup"><span data-stu-id="38256-122">Example 4: Enable a time grain and multiple categories</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Category Category1,Category2 -Timegrain PT1M
```

<span data-ttu-id="38256-123">這個命令只啟用 Category1、Category2 和時間細微性 PT1M。</span><span class="sxs-lookup"><span data-stu-id="38256-123">This command enables only Category1, Category2, and time grain PT1M.</span></span>
<span data-ttu-id="38256-124">所有其他時間 grains 和類別都不會改變。</span><span class="sxs-lookup"><span data-stu-id="38256-124">All other time grains and categories are unchanged.</span></span>

### <span data-ttu-id="38256-125">範例5：使用管線</span><span class="sxs-lookup"><span data-stu-id="38256-125">Example 5: Using pipeline</span></span>
```
PS C:\>Get-AzDiagnosticSetting -ResourceId "Resource01" | Set-AzDiagnosticSetting
```

<span data-ttu-id="38256-126">這個命令使用 PowerShell 管線來設定 (不會) 診斷設定中進行變更。</span><span class="sxs-lookup"><span data-stu-id="38256-126">This command uses the PowerShell pipeline to set (not change made) a diagnostic setting.</span></span>

## <span data-ttu-id="38256-127">參數</span><span class="sxs-lookup"><span data-stu-id="38256-127">PARAMETERS</span></span>

### <span data-ttu-id="38256-128">-類別</span><span class="sxs-lookup"><span data-stu-id="38256-128">-Category</span></span>
<span data-ttu-id="38256-129">根據 *Enabled* 的值，指定要啟用或停用的記錄類別清單。</span><span class="sxs-lookup"><span data-stu-id="38256-129">Specifies the list of log categories to enable or disable, according to the value of *Enabled*.</span></span>
<span data-ttu-id="38256-130">如果未指定任何類別，此命令會在所有支援的類別上執行。</span><span class="sxs-lookup"><span data-stu-id="38256-130">If no category is specified, this command operates on all supported categories.</span></span> 

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

### <span data-ttu-id="38256-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38256-131">-DefaultProfile</span></span>
<span data-ttu-id="38256-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="38256-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="38256-133">-啟用</span><span class="sxs-lookup"><span data-stu-id="38256-133">-Enabled</span></span>
<span data-ttu-id="38256-134">指出是否要啟用診斷。</span><span class="sxs-lookup"><span data-stu-id="38256-134">Indicates whether to enable diagnostics.</span></span>
<span data-ttu-id="38256-135">指定 $True 以啟用診斷，或 $False 以停用診斷程式。</span><span class="sxs-lookup"><span data-stu-id="38256-135">Specify $True to enable diagnostics, or $False to disable diagnostics.</span></span>

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

### <span data-ttu-id="38256-136">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="38256-136">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="38256-137">事件中心授權規則識別碼</span><span class="sxs-lookup"><span data-stu-id="38256-137">The event hub authorization rule id</span></span>

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

### <span data-ttu-id="38256-138">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="38256-138">-EventHubName</span></span>
<span data-ttu-id="38256-139">事件中樞名稱</span><span class="sxs-lookup"><span data-stu-id="38256-139">The event hub name</span></span>

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

### <span data-ttu-id="38256-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38256-140">-InputObject</span></span>
<span data-ttu-id="38256-141">輸入物件 (來自管線的可能。 ) 將會從這個物件中提取名稱和 resourceId。</span><span class="sxs-lookup"><span data-stu-id="38256-141">The input object (possible from the pipeline.) The name and resourceId will be extracted from this object.</span></span>

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

### <span data-ttu-id="38256-142">-MetricCategory</span><span class="sxs-lookup"><span data-stu-id="38256-142">-MetricCategory</span></span>
<span data-ttu-id="38256-143">[公制] 類別的清單。</span><span class="sxs-lookup"><span data-stu-id="38256-143">The list of metric categories.</span></span> <span data-ttu-id="38256-144">如果未指定任何類別，此命令會在所有支援的類別上執行。</span><span class="sxs-lookup"><span data-stu-id="38256-144">If no category is specified, this command operates on all supported categories.</span></span> 

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

### <span data-ttu-id="38256-145">-名稱</span><span class="sxs-lookup"><span data-stu-id="38256-145">-Name</span></span>
<span data-ttu-id="38256-146">診斷設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="38256-146">The name of the diagnostic setting.</span></span> <span data-ttu-id="38256-147">預設值為 [ **服務** ]。</span><span class="sxs-lookup"><span data-stu-id="38256-147">The default value is **service**.</span></span>

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

### <span data-ttu-id="38256-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38256-148">-ResourceId</span></span>
<span data-ttu-id="38256-149">指定資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="38256-149">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="38256-150">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="38256-150">-RetentionEnabled</span></span>
<span data-ttu-id="38256-151">指出是否已啟用診斷資訊的保留。</span><span class="sxs-lookup"><span data-stu-id="38256-151">Indicates whether retention of diagnostic information is enabled.</span></span>

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

### <span data-ttu-id="38256-152">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="38256-152">-RetentionInDays</span></span>
<span data-ttu-id="38256-153">指定保留原則（以天為單位）。</span><span class="sxs-lookup"><span data-stu-id="38256-153">Specifies the retention policy, in days.</span></span>

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

### <span data-ttu-id="38256-154">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="38256-154">-ServiceBusRuleId</span></span>
<span data-ttu-id="38256-155">服務匯流排規則 id。</span><span class="sxs-lookup"><span data-stu-id="38256-155">The Service Bus Rule id.</span></span>

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

### <span data-ttu-id="38256-156">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="38256-156">-StorageAccountId</span></span>
<span data-ttu-id="38256-157">指定要儲存資料的儲存空間帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="38256-157">Specifies the ID of the Storage account in which to save the data.</span></span>

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

### <span data-ttu-id="38256-158">-Timegrain</span><span class="sxs-lookup"><span data-stu-id="38256-158">-Timegrain</span></span>
<span data-ttu-id="38256-159">根據 [ *Enabled* ] 的值，指定要啟用或停用度量單位的時間 grains。</span><span class="sxs-lookup"><span data-stu-id="38256-159">Specifies the time grains to enable or disable for metrics, according to the value of *Enabled*.</span></span>
<span data-ttu-id="38256-160">如果您沒有指定時間細微性，這個命令會在所有可用的時間 grains 上執行。</span><span class="sxs-lookup"><span data-stu-id="38256-160">If you do not specify a time grain, this command operates on all available time grains.</span></span>

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

### <span data-ttu-id="38256-161">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="38256-161">-WorkspaceId</span></span>
<span data-ttu-id="38256-162">工作區的識別碼</span><span class="sxs-lookup"><span data-stu-id="38256-162">The Id of the workspace</span></span>

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

### <span data-ttu-id="38256-163">-確認</span><span class="sxs-lookup"><span data-stu-id="38256-163">-Confirm</span></span>
<span data-ttu-id="38256-164">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="38256-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38256-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38256-165">-WhatIf</span></span>
<span data-ttu-id="38256-166">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="38256-166">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="38256-167">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="38256-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38256-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38256-168">CommonParameters</span></span>
<span data-ttu-id="38256-169">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="38256-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38256-170">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="38256-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38256-171">輸入</span><span class="sxs-lookup"><span data-stu-id="38256-171">INPUTS</span></span>

### <span data-ttu-id="38256-172">PSServiceDiagnosticSettings 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="38256-172">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

### <span data-ttu-id="38256-173">System.object</span><span class="sxs-lookup"><span data-stu-id="38256-173">System.String</span></span>

### <span data-ttu-id="38256-174">System.object</span><span class="sxs-lookup"><span data-stu-id="38256-174">System.Boolean</span></span>

### <span data-ttu-id="38256-175">[System.object]。清單 ' 1 [CoreLib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="38256-175">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="38256-176">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="38256-176">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="38256-177">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="38256-177">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="38256-178">輸出</span><span class="sxs-lookup"><span data-stu-id="38256-178">OUTPUTS</span></span>

### <span data-ttu-id="38256-179">PSServiceDiagnosticSettings 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="38256-179">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="38256-180">筆記</span><span class="sxs-lookup"><span data-stu-id="38256-180">NOTES</span></span>

## <span data-ttu-id="38256-181">相關連結</span><span class="sxs-lookup"><span data-stu-id="38256-181">RELATED LINKS</span></span>

<span data-ttu-id="38256-182">[AzDiagnosticSetting](./Get-AzDiagnosticSetting.md) 
[移除-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="38256-182">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md)
[Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span></span>
