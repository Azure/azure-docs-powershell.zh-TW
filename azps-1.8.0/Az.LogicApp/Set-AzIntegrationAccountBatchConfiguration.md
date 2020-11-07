---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 40cd652a957d4e0a7565b573b288b333e4cebe33
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787034"
---
# <span data-ttu-id="6483d-101">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="6483d-101">Set-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="6483d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6483d-102">SYNOPSIS</span></span>
<span data-ttu-id="6483d-103">修改整合帳戶批次設定。</span><span class="sxs-lookup"><span data-stu-id="6483d-103">Modifies an integration account batch configuration.</span></span>

## <span data-ttu-id="6483d-104">句法</span><span class="sxs-lookup"><span data-stu-id="6483d-104">SYNTAX</span></span>

### <span data-ttu-id="6483d-105">ByIntegrationAccountAndParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="6483d-105">ByIntegrationAccountAndParameters (Default)</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6483d-106">ByIntegrationAccountAndJson</span><span class="sxs-lookup"><span data-stu-id="6483d-106">ByIntegrationAccountAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6483d-107">ByIntegrationAccountAndFilePath</span><span class="sxs-lookup"><span data-stu-id="6483d-107">ByIntegrationAccountAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6483d-108">ByInputObjectAndJson</span><span class="sxs-lookup"><span data-stu-id="6483d-108">ByInputObjectAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6483d-109">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="6483d-109">ByInputObjectAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6483d-110">ByInputObjectAndParameters</span><span class="sxs-lookup"><span data-stu-id="6483d-110">ByInputObjectAndParameters</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6483d-111">ByResourceIdAndJson</span><span class="sxs-lookup"><span data-stu-id="6483d-111">ByResourceIdAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> -BatchConfigurationDefinition <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6483d-112">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="6483d-112">ByResourceIdAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> -BatchConfigurationFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6483d-113">ByResourceIdAndParameters</span><span class="sxs-lookup"><span data-stu-id="6483d-113">ByResourceIdAndParameters</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> [-BatchGroupName <String>]
 [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>] [-ScheduleFrequency <String>]
 [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6483d-114">說明</span><span class="sxs-lookup"><span data-stu-id="6483d-114">DESCRIPTION</span></span>
<span data-ttu-id="6483d-115">**AzIntegrationAccountBatchConfiguration** Cmdlet 會修改整合帳戶批次配置。</span><span class="sxs-lookup"><span data-stu-id="6483d-115">The **Set-AzIntegrationAccountBatchConfiguration** cmdlet modifies an integration account batch configuration.</span></span>

## <span data-ttu-id="6483d-116">示例</span><span class="sxs-lookup"><span data-stu-id="6483d-116">EXAMPLES</span></span>

### <span data-ttu-id="6483d-117">範例1：使用本機檔案修改批次設定</span><span class="sxs-lookup"><span data-stu-id="6483d-117">Example 1: Modify a batch configuration using local file</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationFilePath $batchConfigurationFilePath

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="6483d-118">使用 [$batchConfigurationFilePath] 中所含檔案路徑上的本機檔案，修改名為 "sampleBatchConfig" 的批次配置。</span><span class="sxs-lookup"><span data-stu-id="6483d-118">Modify a batch configuration named "sampleBatchConfig" using the local file located at the file path contained in "$batchConfigurationFilePath".</span></span>

### <span data-ttu-id="6483d-119">範例2：使用 JSON 字串修改批次配置</span><span class="sxs-lookup"><span data-stu-id="6483d-119">Example 2: Modify a batch configuration using a JSON string</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationDefinition $batchConfigurationContent

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="6483d-120">使用 "$batchConfigurationContent" 中包含的 JSON 字串來修改名為 "sampleBatchConfig" 的批次配置。</span><span class="sxs-lookup"><span data-stu-id="6483d-120">Modify a batch configuration named "sampleBatchConfig" using the a JSON string contained in "$batchConfigurationContent".</span></span>

### <span data-ttu-id="6483d-121">範例3：使用參數修改批次設定</span><span class="sxs-lookup"><span data-stu-id="6483d-121">Example 3: Modify a batch configuration using parameters</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -MessageCount 199 -BatchSize 5 -ScheduleInterval 1 -ScheduleFrequency "Month"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="6483d-122">手動提供所有 nessecary 參數，即可修改名為 "sampleBatchConfig" 的批次配置。</span><span class="sxs-lookup"><span data-stu-id="6483d-122">Modify a batch configuration named "sampleBatchConfig" by manually providing all of the nessecary parameters.</span></span>

## <span data-ttu-id="6483d-123">參數</span><span class="sxs-lookup"><span data-stu-id="6483d-123">PARAMETERS</span></span>

### <span data-ttu-id="6483d-124">-BatchConfigurationDefinition</span><span class="sxs-lookup"><span data-stu-id="6483d-124">-BatchConfigurationDefinition</span></span>
<span data-ttu-id="6483d-125">整合帳戶批次配置定義。</span><span class="sxs-lookup"><span data-stu-id="6483d-125">The integration account batch configuration definition.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndJson, ByInputObjectAndJson, ByResourceIdAndJson
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6483d-126">-BatchConfigurationFilePath</span><span class="sxs-lookup"><span data-stu-id="6483d-126">-BatchConfigurationFilePath</span></span>
<span data-ttu-id="6483d-127">整合帳戶批次設定檔路徑。</span><span class="sxs-lookup"><span data-stu-id="6483d-127">The integration account batch configuration file path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByInputObjectAndFilePath, ByResourceIdAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6483d-128">-BatchGroupName</span><span class="sxs-lookup"><span data-stu-id="6483d-128">-BatchGroupName</span></span>
<span data-ttu-id="6483d-129">整合帳戶批次配置組名稱。</span><span class="sxs-lookup"><span data-stu-id="6483d-129">The integration account batch configuration group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6483d-130">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="6483d-130">-BatchSize</span></span>
<span data-ttu-id="6483d-131">整合帳戶批次配置的批次大小。</span><span class="sxs-lookup"><span data-stu-id="6483d-131">The integration account batch configuration batch size.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6483d-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6483d-132">-DefaultProfile</span></span>
<span data-ttu-id="6483d-133">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6483d-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6483d-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6483d-134">-InputObject</span></span>
<span data-ttu-id="6483d-135">整合帳戶批次配置。</span><span class="sxs-lookup"><span data-stu-id="6483d-135">An integration account batch configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration
Parameter Sets: ByInputObjectAndJson, ByInputObjectAndFilePath, ByInputObjectAndParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6483d-136">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="6483d-136">-MessageCount</span></span>
<span data-ttu-id="6483d-137">整合帳戶批次配置訊息計數。</span><span class="sxs-lookup"><span data-stu-id="6483d-137">The integration account batch configuration message count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6483d-138">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="6483d-138">-Metadata</span></span>
<span data-ttu-id="6483d-139">整合帳戶批次配置中繼資料。</span><span class="sxs-lookup"><span data-stu-id="6483d-139">The integration account batch configuration metadata.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6483d-140">-名稱</span><span class="sxs-lookup"><span data-stu-id="6483d-140">-Name</span></span>
<span data-ttu-id="6483d-141">整合帳戶批次配置名稱。</span><span class="sxs-lookup"><span data-stu-id="6483d-141">The integration account batch configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByIntegrationAccountAndJson, ByIntegrationAccountAndFilePath
Aliases: BatchConfigurationName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6483d-142">-ParentName</span><span class="sxs-lookup"><span data-stu-id="6483d-142">-ParentName</span></span>
<span data-ttu-id="6483d-143">整合帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="6483d-143">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByIntegrationAccountAndJson, ByIntegrationAccountAndFilePath
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6483d-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6483d-144">-ResourceGroupName</span></span>
<span data-ttu-id="6483d-145">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6483d-145">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByIntegrationAccountAndJson, ByIntegrationAccountAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6483d-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6483d-146">-ResourceId</span></span>
<span data-ttu-id="6483d-147">整合帳戶批次配置資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="6483d-147">The integration account batch configuration resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdAndJson, ByResourceIdAndFilePath, ByResourceIdAndParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6483d-148">-ScheduleFrequency</span><span class="sxs-lookup"><span data-stu-id="6483d-148">-ScheduleFrequency</span></span>
<span data-ttu-id="6483d-149">整合帳戶批次配置排程頻率。</span><span class="sxs-lookup"><span data-stu-id="6483d-149">The integration account batch configuration schedule frequency.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:
Accepted values: Month, Week, Day, Hour, Minute, Second

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6483d-150">-ScheduleInterval</span><span class="sxs-lookup"><span data-stu-id="6483d-150">-ScheduleInterval</span></span>
<span data-ttu-id="6483d-151">整合帳戶批次配置排程間隔。</span><span class="sxs-lookup"><span data-stu-id="6483d-151">The integration account batch configuration schedule interval.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6483d-152">-ScheduleStartTime</span><span class="sxs-lookup"><span data-stu-id="6483d-152">-ScheduleStartTime</span></span>
<span data-ttu-id="6483d-153">整合帳戶批次配置排程開始時間。</span><span class="sxs-lookup"><span data-stu-id="6483d-153">The integration account batch configuration schedule start time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6483d-154">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="6483d-154">-ScheduleTimeZone</span></span>
<span data-ttu-id="6483d-155">整合帳戶批次配置排程時區。</span><span class="sxs-lookup"><span data-stu-id="6483d-155">The integration account batch configuration schedule time zone.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6483d-156">-確認</span><span class="sxs-lookup"><span data-stu-id="6483d-156">-Confirm</span></span>
<span data-ttu-id="6483d-157">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6483d-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6483d-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6483d-158">-WhatIf</span></span>
<span data-ttu-id="6483d-159">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6483d-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6483d-160">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6483d-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6483d-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6483d-161">CommonParameters</span></span>
<span data-ttu-id="6483d-162">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6483d-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6483d-163">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6483d-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6483d-164">輸入</span><span class="sxs-lookup"><span data-stu-id="6483d-164">INPUTS</span></span>

### <span data-ttu-id="6483d-165">PSIntegrationAccountBatchConfiguration 中的 LogicApp。</span><span class="sxs-lookup"><span data-stu-id="6483d-165">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

### <span data-ttu-id="6483d-166">System.object</span><span class="sxs-lookup"><span data-stu-id="6483d-166">System.String</span></span>

## <span data-ttu-id="6483d-167">輸出</span><span class="sxs-lookup"><span data-stu-id="6483d-167">OUTPUTS</span></span>

### <span data-ttu-id="6483d-168">PSIntegrationAccountBatchConfiguration 中的 LogicApp。</span><span class="sxs-lookup"><span data-stu-id="6483d-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="6483d-169">筆記</span><span class="sxs-lookup"><span data-stu-id="6483d-169">NOTES</span></span>

## <span data-ttu-id="6483d-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="6483d-170">RELATED LINKS</span></span>
