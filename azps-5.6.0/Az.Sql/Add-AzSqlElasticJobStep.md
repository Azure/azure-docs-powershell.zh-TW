---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/add-azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
ms.openlocfilehash: 41314cb2a65912e2973e91b27036fc099d2cbca6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904306"
---
# <span data-ttu-id="a58cf-101">Add-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="a58cf-101">Add-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="a58cf-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a58cf-102">SYNOPSIS</span></span>
<span data-ttu-id="a58cf-103">新增工作步驟至工作</span><span class="sxs-lookup"><span data-stu-id="a58cf-103">Adds a job step to a job</span></span>

## <span data-ttu-id="a58cf-104">語法</span><span class="sxs-lookup"><span data-stu-id="a58cf-104">SYNTAX</span></span>

### <span data-ttu-id="a58cf-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a58cf-105">DefaultSet (Default)</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String> -Name <String>
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a58cf-106">WithOutputDb</span><span class="sxs-lookup"><span data-stu-id="a58cf-106">WithOutputDb</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String> -OutputTableName <String>
 -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a58cf-107">WithOutputDbId</span><span class="sxs-lookup"><span data-stu-id="a58cf-107">WithOutputDbId</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseResourceId <String> -OutputCredentialName <String> -OutputTableName <String> -Name <String>
 [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a58cf-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="a58cf-108">ObjectSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a58cf-109">WithOutputDbUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="a58cf-109">WithOutputDbUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a58cf-110">WithOutputDbIdUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="a58cf-110">WithOutputDbIdUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseResourceId <String>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a58cf-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a58cf-111">ResourceIdSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a58cf-112">WithOutputDbUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a58cf-112">WithOutputDbUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a58cf-113">WithOutputDbIdUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a58cf-113">WithOutputDbIdUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseResourceId <String> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a58cf-114">描述</span><span class="sxs-lookup"><span data-stu-id="a58cf-114">DESCRIPTION</span></span>
<span data-ttu-id="a58cf-115">Cmdlet Add-AzSqlElasticJobStep新增工作步驟至工作</span><span class="sxs-lookup"><span data-stu-id="a58cf-115">The Add-AzSqlElasticJobStep cmdlet adds a job step to a job</span></span>

## <span data-ttu-id="a58cf-116">例子</span><span class="sxs-lookup"><span data-stu-id="a58cf-116">EXAMPLES</span></span>

### <span data-ttu-id="a58cf-117">範例 1：新增步驟至工作</span><span class="sxs-lookup"><span data-stu-id="a58cf-117">Example 1: Adds a step to a job</span></span>
```powershell
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -Name job1
$job | Add-AzSqlElasticJobStep -Name step1 -TargetGroupName tg1 -CredentialName cred1 -CommandText "SELECT 1"

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="a58cf-118">新增工作步驟至工作</span><span class="sxs-lookup"><span data-stu-id="a58cf-118">Adds a job step to a job</span></span>

## <span data-ttu-id="a58cf-119">參數</span><span class="sxs-lookup"><span data-stu-id="a58cf-119">PARAMETERS</span></span>

### <span data-ttu-id="a58cf-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="a58cf-120">-AgentName</span></span>
<span data-ttu-id="a58cf-121">代理人名稱</span><span class="sxs-lookup"><span data-stu-id="a58cf-121">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a58cf-122">-CommandText</span><span class="sxs-lookup"><span data-stu-id="a58cf-122">-CommandText</span></span>
<span data-ttu-id="a58cf-123">命令文字</span><span class="sxs-lookup"><span data-stu-id="a58cf-123">The command text</span></span>

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

### <span data-ttu-id="a58cf-124">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="a58cf-124">-CredentialName</span></span>
<span data-ttu-id="a58cf-125">認證名稱</span><span class="sxs-lookup"><span data-stu-id="a58cf-125">The credential name</span></span>

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

### <span data-ttu-id="a58cf-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a58cf-126">-DefaultProfile</span></span>
<span data-ttu-id="a58cf-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a58cf-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a58cf-128">-InitialRetryIntervalRets</span><span class="sxs-lookup"><span data-stu-id="a58cf-128">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="a58cf-129">初始重試間隔秒數</span><span class="sxs-lookup"><span data-stu-id="a58cf-129">The initial retry interval seconds</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a58cf-130">-JobName</span><span class="sxs-lookup"><span data-stu-id="a58cf-130">-JobName</span></span>
<span data-ttu-id="a58cf-131">工作名稱</span><span class="sxs-lookup"><span data-stu-id="a58cf-131">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a58cf-132">-MaximumRetryIntervalRets</span><span class="sxs-lookup"><span data-stu-id="a58cf-132">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="a58cf-133">重試間隔秒數上限</span><span class="sxs-lookup"><span data-stu-id="a58cf-133">The maximum retry interval seconds</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a58cf-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="a58cf-134">-Name</span></span>
<span data-ttu-id="a58cf-135">工作步驟名稱</span><span class="sxs-lookup"><span data-stu-id="a58cf-135">The job step name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a58cf-136">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="a58cf-136">-OutputCredentialName</span></span>
<span data-ttu-id="a58cf-137">輸出認證名稱</span><span class="sxs-lookup"><span data-stu-id="a58cf-137">The output credential name</span></span>

```yaml
Type: System.String
Parameter Sets: WithOutputDb, WithOutputDbId, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject, WithOutputDbUsingParentResourceId, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a58cf-138">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="a58cf-138">-OutputDatabaseObject</span></span>
<span data-ttu-id="a58cf-139">輸出資料庫物件</span><span class="sxs-lookup"><span data-stu-id="a58cf-139">The output database object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: WithOutputDb, WithOutputDbUsingParentObject, WithOutputDbUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a58cf-140">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="a58cf-140">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="a58cf-141">輸出資料庫資源識別碼</span><span class="sxs-lookup"><span data-stu-id="a58cf-141">The output database resource id</span></span>

```yaml
Type: System.String
Parameter Sets: WithOutputDbId, WithOutputDbIdUsingParentObject, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a58cf-142">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="a58cf-142">-OutputSchemaName</span></span>
<span data-ttu-id="a58cf-143">輸出架構名稱</span><span class="sxs-lookup"><span data-stu-id="a58cf-143">The output schema name</span></span>

```yaml
Type: System.String
Parameter Sets: WithOutputDb, WithOutputDbId, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject, WithOutputDbUsingParentResourceId, WithOutputDbIdUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a58cf-144">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="a58cf-144">-OutputTableName</span></span>
<span data-ttu-id="a58cf-145">輸出資料表名稱</span><span class="sxs-lookup"><span data-stu-id="a58cf-145">The output table name</span></span>

```yaml
Type: System.String
Parameter Sets: WithOutputDb, WithOutputDbId, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject, WithOutputDbUsingParentResourceId, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a58cf-146">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a58cf-146">-ParentObject</span></span>
<span data-ttu-id="a58cf-147">工作物件</span><span class="sxs-lookup"><span data-stu-id="a58cf-147">The job object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a58cf-148">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a58cf-148">-ParentResourceId</span></span>
<span data-ttu-id="a58cf-149">工作資源識別碼</span><span class="sxs-lookup"><span data-stu-id="a58cf-149">The job resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, WithOutputDbUsingParentResourceId, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a58cf-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a58cf-150">-ResourceGroupName</span></span>
<span data-ttu-id="a58cf-151">資源組名</span><span class="sxs-lookup"><span data-stu-id="a58cf-151">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a58cf-152">-重試Attempts</span><span class="sxs-lookup"><span data-stu-id="a58cf-152">-RetryAttempts</span></span>
<span data-ttu-id="a58cf-153">重試嘗試</span><span class="sxs-lookup"><span data-stu-id="a58cf-153">The retry attempts</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a58cf-154">-重試IntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="a58cf-154">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="a58cf-155">重試間隔回乘法</span><span class="sxs-lookup"><span data-stu-id="a58cf-155">The retry interval back off multiplier</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a58cf-156">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a58cf-156">-ServerName</span></span>
<span data-ttu-id="a58cf-157">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="a58cf-157">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a58cf-158">-StepId</span><span class="sxs-lookup"><span data-stu-id="a58cf-158">-StepId</span></span>
<span data-ttu-id="a58cf-159">步驟識別碼</span><span class="sxs-lookup"><span data-stu-id="a58cf-159">The step id</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a58cf-160">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="a58cf-160">-TargetGroupName</span></span>
<span data-ttu-id="a58cf-161">目標群組名</span><span class="sxs-lookup"><span data-stu-id="a58cf-161">The target group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId, ObjectSet, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject, ResourceIdSet, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WithOutputDbUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a58cf-162">-Timeout秒</span><span class="sxs-lookup"><span data-stu-id="a58cf-162">-TimeoutSeconds</span></span>
<span data-ttu-id="a58cf-163">秒數</span><span class="sxs-lookup"><span data-stu-id="a58cf-163">The time out seconds</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a58cf-164">-確認</span><span class="sxs-lookup"><span data-stu-id="a58cf-164">-Confirm</span></span>
<span data-ttu-id="a58cf-165">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a58cf-165">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a58cf-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a58cf-166">-WhatIf</span></span>
<span data-ttu-id="a58cf-167">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a58cf-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a58cf-168">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a58cf-168">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a58cf-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a58cf-169">CommonParameters</span></span>
<span data-ttu-id="a58cf-170">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a58cf-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a58cf-171">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a58cf-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a58cf-172">輸入</span><span class="sxs-lookup"><span data-stu-id="a58cf-172">INPUTS</span></span>

### <span data-ttu-id="a58cf-173">Microsoft.Azure.Commands.Sql.AzureJobs.Model.AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="a58cf-173">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="a58cf-174">輸出</span><span class="sxs-lookup"><span data-stu-id="a58cf-174">OUTPUTS</span></span>

### <span data-ttu-id="a58cf-175">Microsoft.Azure.Commands.Sql.AzureJobs.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="a58cf-175">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="a58cf-176">筆記</span><span class="sxs-lookup"><span data-stu-id="a58cf-176">NOTES</span></span>

## <span data-ttu-id="a58cf-177">相關連結</span><span class="sxs-lookup"><span data-stu-id="a58cf-177">RELATED LINKS</span></span>
