---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/new-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 8e5b34d82639ac91afd07f4c2cdc8729e6d213b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916529"
---
# <span data-ttu-id="fb4e1-101">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="fb4e1-101">New-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="fb4e1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fb4e1-102">SYNOPSIS</span></span>
<span data-ttu-id="fb4e1-103">建立整合帳戶批次組組。</span><span class="sxs-lookup"><span data-stu-id="fb4e1-103">Creates an integration account batch configuration.</span></span>

## <span data-ttu-id="fb4e1-104">語法</span><span class="sxs-lookup"><span data-stu-id="fb4e1-104">SYNTAX</span></span>

### <span data-ttu-id="fb4e1-105">By方AccountAndParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="fb4e1-105">ByIntegrationAccountAndParameters (Default)</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb4e1-106">By方AccountAndJson</span><span class="sxs-lookup"><span data-stu-id="fb4e1-106">ByIntegrationAccountAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb4e1-107">By方AccountAndFilePath</span><span class="sxs-lookup"><span data-stu-id="fb4e1-107">ByIntegrationAccountAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb4e1-108">ByInputObjectAndJson</span><span class="sxs-lookup"><span data-stu-id="fb4e1-108">ByInputObjectAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb4e1-109">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="fb4e1-109">ByInputObjectAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb4e1-110">ByInputObjectAndParameters</span><span class="sxs-lookup"><span data-stu-id="fb4e1-110">ByInputObjectAndParameters</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb4e1-111">ByResourceIdAndJson</span><span class="sxs-lookup"><span data-stu-id="fb4e1-111">ByResourceIdAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb4e1-112">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="fb4e1-112">ByResourceIdAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb4e1-113">ByResourceIdAndParameters</span><span class="sxs-lookup"><span data-stu-id="fb4e1-113">ByResourceIdAndParameters</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String> [-BatchGroupName <String>]
 [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>] [-ScheduleFrequency <String>]
 [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb4e1-114">描述</span><span class="sxs-lookup"><span data-stu-id="fb4e1-114">DESCRIPTION</span></span>
<span data-ttu-id="fb4e1-115">**Get-Az有AccountBatchConfiguration** Cmdlet 會建立整合帳戶中的新批次組組。</span><span class="sxs-lookup"><span data-stu-id="fb4e1-115">The **Get-AzIntegrationAccountBatchConfiguration** cmdlet creates a new batch configuration in an integration account.</span></span>

## <span data-ttu-id="fb4e1-116">例子</span><span class="sxs-lookup"><span data-stu-id="fb4e1-116">EXAMPLES</span></span>

### <span data-ttu-id="fb4e1-117">範例 1：使用本地檔案建立新批次組</span><span class="sxs-lookup"><span data-stu-id="fb4e1-117">Example 1: Create new batch configuration using local file</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationFilePath $batchConfigurationFilePath

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="fb4e1-118">使用位於「$batchConfigurationFilePath」中包含的檔案路徑的本地檔案，來建立新的批次組$batchConfigurationFilePath。</span><span class="sxs-lookup"><span data-stu-id="fb4e1-118">Creates a new batch configuration using the local file located at the file path contained in "$batchConfigurationFilePath".</span></span>

### <span data-ttu-id="fb4e1-119">範例 2：使用 JSON 字串建立新批次組組</span><span class="sxs-lookup"><span data-stu-id="fb4e1-119">Example 2: Create new batch configuration using a JSON string</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationDefinition $batchConfigurationContent

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="fb4e1-120">使用 "$batchConfigurationContent" 中包含的 JSON 字串來建立新的批次組$batchConfigurationContent。</span><span class="sxs-lookup"><span data-stu-id="fb4e1-120">Creates a new batch configuration using the a JSON string contained in "$batchConfigurationContent".</span></span>

### <span data-ttu-id="fb4e1-121">範例 3：使用參數建立新批次設定</span><span class="sxs-lookup"><span data-stu-id="fb4e1-121">Example 3: Create new batch configuration using parameters</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -MessageCount 199 -BatchSize 5 -ScheduleInterval 1 -ScheduleFrequency "Month"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="fb4e1-122">手動提供所有必要的參數，以建立新的批次設定。</span><span class="sxs-lookup"><span data-stu-id="fb4e1-122">Creates a new batch configuration by manually providing all of the necessary parameters.</span></span>

## <span data-ttu-id="fb4e1-123">參數</span><span class="sxs-lookup"><span data-stu-id="fb4e1-123">PARAMETERS</span></span>

### <span data-ttu-id="fb4e1-124">-BatchConfigurationDefinition</span><span class="sxs-lookup"><span data-stu-id="fb4e1-124">-BatchConfigurationDefinition</span></span>
<span data-ttu-id="fb4e1-125">整合帳戶批次組組定義。</span><span class="sxs-lookup"><span data-stu-id="fb4e1-125">The integration account batch configuration definition.</span></span>

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

### <span data-ttu-id="fb4e1-126">-BatchConfigurationFilePath</span><span class="sxs-lookup"><span data-stu-id="fb4e1-126">-BatchConfigurationFilePath</span></span>
<span data-ttu-id="fb4e1-127">整合帳戶批次組設定檔路徑。</span><span class="sxs-lookup"><span data-stu-id="fb4e1-127">The integration account batch configuration file path.</span></span>

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

### <span data-ttu-id="fb4e1-128">-BatchGroupName</span><span class="sxs-lookup"><span data-stu-id="fb4e1-128">-BatchGroupName</span></span>
<span data-ttu-id="fb4e1-129">整合帳戶批次組組名。</span><span class="sxs-lookup"><span data-stu-id="fb4e1-129">The integration account batch configuration group name.</span></span>

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

### <span data-ttu-id="fb4e1-130">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="fb4e1-130">-BatchSize</span></span>
<span data-ttu-id="fb4e1-131">整合帳戶批次組組批次大小。</span><span class="sxs-lookup"><span data-stu-id="fb4e1-131">The integration account batch configuration batch size.</span></span>

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

### <span data-ttu-id="fb4e1-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb4e1-132">-DefaultProfile</span></span>
<span data-ttu-id="fb4e1-133">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="fb4e1-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb4e1-134">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="fb4e1-134">-MessageCount</span></span>
<span data-ttu-id="fb4e1-135">整合帳戶批次組組訊息計數。</span><span class="sxs-lookup"><span data-stu-id="fb4e1-135">The integration account batch configuration message count.</span></span>

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

### <span data-ttu-id="fb4e1-136">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="fb4e1-136">-Metadata</span></span>
<span data-ttu-id="fb4e1-137">整合帳戶批次組組中繼資料。</span><span class="sxs-lookup"><span data-stu-id="fb4e1-137">The integration account batch configuration metadata.</span></span>

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

### <span data-ttu-id="fb4e1-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="fb4e1-138">-Name</span></span>
<span data-ttu-id="fb4e1-139">整合帳戶批次組組名稱。</span><span class="sxs-lookup"><span data-stu-id="fb4e1-139">The integration account batch configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BatchConfigurationName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb4e1-140">-ParentName</span><span class="sxs-lookup"><span data-stu-id="fb4e1-140">-ParentName</span></span>
<span data-ttu-id="fb4e1-141">整合帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="fb4e1-141">The integration account name.</span></span>

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

### <span data-ttu-id="fb4e1-142">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="fb4e1-142">-ParentObject</span></span>
<span data-ttu-id="fb4e1-143">整合帳戶物件。</span><span class="sxs-lookup"><span data-stu-id="fb4e1-143">An integration account object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Logic.Models.IntegrationAccount
Parameter Sets: ByInputObjectAndJson, ByInputObjectAndFilePath, ByInputObjectAndParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb4e1-144">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="fb4e1-144">-ParentResourceId</span></span>
<span data-ttu-id="fb4e1-145">整合帳戶批次組組資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="fb4e1-145">The integration account batch configuration resource id.</span></span>

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

### <span data-ttu-id="fb4e1-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb4e1-146">-ResourceGroupName</span></span>
<span data-ttu-id="fb4e1-147">資源組名。</span><span class="sxs-lookup"><span data-stu-id="fb4e1-147">The resource group name.</span></span>

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

### <span data-ttu-id="fb4e1-148">-ScheduleFrequency</span><span class="sxs-lookup"><span data-stu-id="fb4e1-148">-ScheduleFrequency</span></span>
<span data-ttu-id="fb4e1-149">整合帳戶批次組程排程頻率。</span><span class="sxs-lookup"><span data-stu-id="fb4e1-149">The integration account batch configuration schedule frequency.</span></span>

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

### <span data-ttu-id="fb4e1-150">-ScheduleInterval</span><span class="sxs-lookup"><span data-stu-id="fb4e1-150">-ScheduleInterval</span></span>
<span data-ttu-id="fb4e1-151">整合帳戶批次組程排程間隔。</span><span class="sxs-lookup"><span data-stu-id="fb4e1-151">The integration account batch configuration schedule interval.</span></span>

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

### <span data-ttu-id="fb4e1-152">-排程StartTime</span><span class="sxs-lookup"><span data-stu-id="fb4e1-152">-ScheduleStartTime</span></span>
<span data-ttu-id="fb4e1-153">整合帳戶批次組組排程開始時間。</span><span class="sxs-lookup"><span data-stu-id="fb4e1-153">The integration account batch configuration schedule start time.</span></span>

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

### <span data-ttu-id="fb4e1-154">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="fb4e1-154">-ScheduleTimeZone</span></span>
<span data-ttu-id="fb4e1-155">整合帳戶批次組程時區。</span><span class="sxs-lookup"><span data-stu-id="fb4e1-155">The integration account batch configuration schedule time zone.</span></span>

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

### <span data-ttu-id="fb4e1-156">-確認</span><span class="sxs-lookup"><span data-stu-id="fb4e1-156">-Confirm</span></span>
<span data-ttu-id="fb4e1-157">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="fb4e1-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb4e1-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb4e1-158">-WhatIf</span></span>
<span data-ttu-id="fb4e1-159">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fb4e1-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fb4e1-160">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fb4e1-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb4e1-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb4e1-161">CommonParameters</span></span>
<span data-ttu-id="fb4e1-162">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fb4e1-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb4e1-163">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="fb4e1-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb4e1-164">輸入</span><span class="sxs-lookup"><span data-stu-id="fb4e1-164">INPUTS</span></span>

### <span data-ttu-id="fb4e1-165">Microsoft.Azure.management.Logic.models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="fb4e1-165">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="fb4e1-166">System.String</span><span class="sxs-lookup"><span data-stu-id="fb4e1-166">System.String</span></span>

## <span data-ttu-id="fb4e1-167">輸出</span><span class="sxs-lookup"><span data-stu-id="fb4e1-167">OUTPUTS</span></span>

### <span data-ttu-id="fb4e1-168">Microsoft.Azure.Commands.LogicApp.models.PS方AccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="fb4e1-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="fb4e1-169">筆記</span><span class="sxs-lookup"><span data-stu-id="fb4e1-169">NOTES</span></span>

## <span data-ttu-id="fb4e1-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="fb4e1-170">RELATED LINKS</span></span>
