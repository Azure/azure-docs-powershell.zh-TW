---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
ms.openlocfilehash: f39554dacdaabfc42fe44d55a7f3034c1c8b54df
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93798398"
---
# <span data-ttu-id="43d8c-101">Set-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="43d8c-101">Set-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="43d8c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="43d8c-102">SYNOPSIS</span></span>
<span data-ttu-id="43d8c-103">更新作業步驟</span><span class="sxs-lookup"><span data-stu-id="43d8c-103">Updates a job step</span></span>

## <span data-ttu-id="43d8c-104">句法</span><span class="sxs-lookup"><span data-stu-id="43d8c-104">SYNTAX</span></span>

### <span data-ttu-id="43d8c-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="43d8c-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43d8c-106">WithRemoveOutput</span><span class="sxs-lookup"><span data-stu-id="43d8c-106">WithRemoveOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-RemoveOutput] [-TargetGroupName <String>] [-CredentialName <String>]
 [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="43d8c-107">WithAddOutput</span><span class="sxs-lookup"><span data-stu-id="43d8c-107">WithAddOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -OutputDatabaseResourceId <String> [-OutputCredentialName <String>]
 [-OutputTableName <String>] [-OutputSchemaName <String>] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="43d8c-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="43d8c-108">ObjectSet</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-OutputDatabaseObject <AzureSqlDatabaseModel>] [-OutputCredentialName <String>] [-OutputTableName <String>]
 [-OutputSchemaName <String>] [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43d8c-109">WithRemoveOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="43d8c-109">WithRemoveOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> [-RemoveOutput]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43d8c-110">WithAddOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="43d8c-110">WithAddOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43d8c-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="43d8c-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43d8c-112">WithRemoveOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="43d8c-112">WithRemoveOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-RemoveOutput] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="43d8c-113">WithAddOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="43d8c-113">WithAddOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43d8c-114">說明</span><span class="sxs-lookup"><span data-stu-id="43d8c-114">DESCRIPTION</span></span>
<span data-ttu-id="43d8c-115">Set-AzSqlElasticJobStep Cmdlet 會更新作業步驟</span><span class="sxs-lookup"><span data-stu-id="43d8c-115">The Set-AzSqlElasticJobStep cmdlet updates a job step</span></span>

## <span data-ttu-id="43d8c-116">示例</span><span class="sxs-lookup"><span data-stu-id="43d8c-116">EXAMPLES</span></span>

### <span data-ttu-id="43d8c-117">範例 1-更新作業的作業步驟目標群組</span><span class="sxs-lookup"><span data-stu-id="43d8c-117">Example 1 - Updates a job step's target group for a job</span></span>
```
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -TargetGroupName tg2

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg2             cred1                 (43200,10,1,120,2) SELECT 1
```

### <span data-ttu-id="43d8c-118">範例 2-更新作業步驟的 T-sql 腳本以進行工作</span><span class="sxs-lookup"><span data-stu-id="43d8c-118">Example 2 - Updates a job step's T-SQL script for a job</span></span>
```
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -CommandText "SELECT 2"

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 2
```

<span data-ttu-id="43d8c-119">從工作更新作業步驟</span><span class="sxs-lookup"><span data-stu-id="43d8c-119">Updates a job step from a job</span></span>

## <span data-ttu-id="43d8c-120">參數</span><span class="sxs-lookup"><span data-stu-id="43d8c-120">PARAMETERS</span></span>

### <span data-ttu-id="43d8c-121">-AgentName</span><span class="sxs-lookup"><span data-stu-id="43d8c-121">-AgentName</span></span>
<span data-ttu-id="43d8c-122">代理程式名稱</span><span class="sxs-lookup"><span data-stu-id="43d8c-122">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43d8c-123">-CommandText</span><span class="sxs-lookup"><span data-stu-id="43d8c-123">-CommandText</span></span>
<span data-ttu-id="43d8c-124">命令文字</span><span class="sxs-lookup"><span data-stu-id="43d8c-124">The command text</span></span>

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

### <span data-ttu-id="43d8c-125">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="43d8c-125">-CredentialName</span></span>
<span data-ttu-id="43d8c-126">認證名稱</span><span class="sxs-lookup"><span data-stu-id="43d8c-126">The credential name</span></span>

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

### <span data-ttu-id="43d8c-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43d8c-127">-DefaultProfile</span></span>
<span data-ttu-id="43d8c-128">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="43d8c-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43d8c-129">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="43d8c-129">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="43d8c-130">初始重試間隔秒數</span><span class="sxs-lookup"><span data-stu-id="43d8c-130">The initial retry interval seconds</span></span>

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

### <span data-ttu-id="43d8c-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43d8c-131">-InputObject</span></span>
<span data-ttu-id="43d8c-132">作業步驟物件</span><span class="sxs-lookup"><span data-stu-id="43d8c-132">The job step object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel
Parameter Sets: ObjectSet, WithRemoveOutputUsingParentObject, WithAddOutputUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43d8c-133">-JobName</span><span class="sxs-lookup"><span data-stu-id="43d8c-133">-JobName</span></span>
<span data-ttu-id="43d8c-134">作業名稱</span><span class="sxs-lookup"><span data-stu-id="43d8c-134">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43d8c-135">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="43d8c-135">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="43d8c-136">[重試間隔秒數] 的最大值</span><span class="sxs-lookup"><span data-stu-id="43d8c-136">The maximum retry interval seconds</span></span>

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

### <span data-ttu-id="43d8c-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="43d8c-137">-Name</span></span>
<span data-ttu-id="43d8c-138">步驟名稱</span><span class="sxs-lookup"><span data-stu-id="43d8c-138">The step name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43d8c-139">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="43d8c-139">-OutputCredentialName</span></span>
<span data-ttu-id="43d8c-140">輸出認證名稱</span><span class="sxs-lookup"><span data-stu-id="43d8c-140">The output credential name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithAddOutput, ObjectSet, WithAddOutputUsingParentObject, ResourceIdSet, WithAddOutputUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43d8c-141">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="43d8c-141">-OutputDatabaseObject</span></span>
<span data-ttu-id="43d8c-142">輸出資料庫物件</span><span class="sxs-lookup"><span data-stu-id="43d8c-142">The output database object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43d8c-143">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="43d8c-143">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="43d8c-144">輸出資料庫資源識別碼</span><span class="sxs-lookup"><span data-stu-id="43d8c-144">The output database resource id</span></span>

```yaml
Type: System.String
Parameter Sets: WithAddOutput, WithAddOutputUsingParentObject, WithAddOutputUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43d8c-145">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="43d8c-145">-OutputSchemaName</span></span>
<span data-ttu-id="43d8c-146">輸出架構名稱</span><span class="sxs-lookup"><span data-stu-id="43d8c-146">The output schema name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithAddOutput, ObjectSet, WithAddOutputUsingParentObject, ResourceIdSet, WithAddOutputUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43d8c-147">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="43d8c-147">-OutputTableName</span></span>
<span data-ttu-id="43d8c-148">輸出資料表名稱</span><span class="sxs-lookup"><span data-stu-id="43d8c-148">The output table name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithAddOutput, ObjectSet, WithAddOutputUsingParentObject, ResourceIdSet, WithAddOutputUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43d8c-149">-RemoveOutput</span><span class="sxs-lookup"><span data-stu-id="43d8c-149">-RemoveOutput</span></span>
<span data-ttu-id="43d8c-150">指示是否要移除輸出的標誌</span><span class="sxs-lookup"><span data-stu-id="43d8c-150">The flag to indicate whether to remove output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WithRemoveOutput, WithRemoveOutputUsingParentObject, WithRemoveOutputUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43d8c-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43d8c-151">-ResourceGroupName</span></span>
<span data-ttu-id="43d8c-152">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="43d8c-152">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43d8c-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43d8c-153">-ResourceId</span></span>
<span data-ttu-id="43d8c-154">作業步驟資源識別碼</span><span class="sxs-lookup"><span data-stu-id="43d8c-154">The job step resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, WithRemoveOutputUsingParentResourceId, WithAddOutputUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43d8c-155">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="43d8c-155">-RetryAttempts</span></span>
<span data-ttu-id="43d8c-156">[重試 attemps]</span><span class="sxs-lookup"><span data-stu-id="43d8c-156">The retry attemps</span></span>

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

### <span data-ttu-id="43d8c-157">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="43d8c-157">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="43d8c-158">重試間隔回退乘數</span><span class="sxs-lookup"><span data-stu-id="43d8c-158">The retry interval backoff multiplier</span></span>

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

### <span data-ttu-id="43d8c-159">-ServerName</span><span class="sxs-lookup"><span data-stu-id="43d8c-159">-ServerName</span></span>
<span data-ttu-id="43d8c-160">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="43d8c-160">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43d8c-161">-StepId</span><span class="sxs-lookup"><span data-stu-id="43d8c-161">-StepId</span></span>
<span data-ttu-id="43d8c-162">步驟識別碼文字</span><span class="sxs-lookup"><span data-stu-id="43d8c-162">The step id text</span></span>

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

### <span data-ttu-id="43d8c-163">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="43d8c-163">-TargetGroupName</span></span>
<span data-ttu-id="43d8c-164">目標群組名稱</span><span class="sxs-lookup"><span data-stu-id="43d8c-164">The target group name</span></span>

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

### <span data-ttu-id="43d8c-165">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="43d8c-165">-TimeoutSeconds</span></span>
<span data-ttu-id="43d8c-166">超時秒數</span><span class="sxs-lookup"><span data-stu-id="43d8c-166">The timeout seconds</span></span>

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

### <span data-ttu-id="43d8c-167">-確認</span><span class="sxs-lookup"><span data-stu-id="43d8c-167">-Confirm</span></span>
<span data-ttu-id="43d8c-168">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="43d8c-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43d8c-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43d8c-169">-WhatIf</span></span>
<span data-ttu-id="43d8c-170">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="43d8c-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43d8c-171">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="43d8c-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43d8c-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43d8c-172">CommonParameters</span></span>
<span data-ttu-id="43d8c-173">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="43d8c-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43d8c-174">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="43d8c-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43d8c-175">輸入</span><span class="sxs-lookup"><span data-stu-id="43d8c-175">INPUTS</span></span>

### <span data-ttu-id="43d8c-176">AzureSqlElasticJobStepModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="43d8c-176">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="43d8c-177">輸出</span><span class="sxs-lookup"><span data-stu-id="43d8c-177">OUTPUTS</span></span>

### <span data-ttu-id="43d8c-178">AzureSqlElasticJobStepModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="43d8c-178">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="43d8c-179">筆記</span><span class="sxs-lookup"><span data-stu-id="43d8c-179">NOTES</span></span>

## <span data-ttu-id="43d8c-180">相關連結</span><span class="sxs-lookup"><span data-stu-id="43d8c-180">RELATED LINKS</span></span>