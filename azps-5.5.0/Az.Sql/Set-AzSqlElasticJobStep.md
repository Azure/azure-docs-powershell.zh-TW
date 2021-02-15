---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
ms.openlocfilehash: 4f6f0471224799e818f9db29e5be5a4c49f9c45e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127395"
---
# <span data-ttu-id="b117b-101">Set-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="b117b-101">Set-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="b117b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b117b-102">SYNOPSIS</span></span>
<span data-ttu-id="b117b-103">更新作業步驟</span><span class="sxs-lookup"><span data-stu-id="b117b-103">Updates a job step</span></span>

## <span data-ttu-id="b117b-104">句法</span><span class="sxs-lookup"><span data-stu-id="b117b-104">SYNTAX</span></span>

### <span data-ttu-id="b117b-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b117b-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b117b-106">WithRemoveOutput</span><span class="sxs-lookup"><span data-stu-id="b117b-106">WithRemoveOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-RemoveOutput] [-TargetGroupName <String>] [-CredentialName <String>]
 [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b117b-107">WithAddOutput</span><span class="sxs-lookup"><span data-stu-id="b117b-107">WithAddOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -OutputDatabaseResourceId <String> [-OutputCredentialName <String>]
 [-OutputTableName <String>] [-OutputSchemaName <String>] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b117b-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="b117b-108">ObjectSet</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-OutputDatabaseObject <AzureSqlDatabaseModel>] [-OutputCredentialName <String>] [-OutputTableName <String>]
 [-OutputSchemaName <String>] [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b117b-109">WithRemoveOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="b117b-109">WithRemoveOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> [-RemoveOutput]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b117b-110">WithAddOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="b117b-110">WithAddOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b117b-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b117b-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b117b-112">WithRemoveOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b117b-112">WithRemoveOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-RemoveOutput] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b117b-113">WithAddOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b117b-113">WithAddOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b117b-114">說明</span><span class="sxs-lookup"><span data-stu-id="b117b-114">DESCRIPTION</span></span>
<span data-ttu-id="b117b-115">Set-AzSqlElasticJobStep Cmdlet 會更新作業步驟</span><span class="sxs-lookup"><span data-stu-id="b117b-115">The Set-AzSqlElasticJobStep cmdlet updates a job step</span></span>

## <span data-ttu-id="b117b-116">示例</span><span class="sxs-lookup"><span data-stu-id="b117b-116">EXAMPLES</span></span>

### <span data-ttu-id="b117b-117">範例1：更新作業的作業步驟目標群組</span><span class="sxs-lookup"><span data-stu-id="b117b-117">Example 1: Updates a job step's target group for a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -TargetGroupName tg2

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg2             cred1                 (43200,10,1,120,2) SELECT 1
```

### <span data-ttu-id="b117b-118">範例2：更新作業步驟的 T-sql 腳本以進行工作</span><span class="sxs-lookup"><span data-stu-id="b117b-118">Example 2: Updates a job step's T-SQL script for a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -CommandText "SELECT 2"

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 2
```

<span data-ttu-id="b117b-119">從工作更新作業步驟</span><span class="sxs-lookup"><span data-stu-id="b117b-119">Updates a job step from a job</span></span>

### <span data-ttu-id="b117b-120">範例3</span><span class="sxs-lookup"><span data-stu-id="b117b-120">Example 3</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticJobStep -AgentName agent -CommandText 'SELECT 2' -JobName job1 -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="b117b-121">參數</span><span class="sxs-lookup"><span data-stu-id="b117b-121">PARAMETERS</span></span>

### <span data-ttu-id="b117b-122">-AgentName</span><span class="sxs-lookup"><span data-stu-id="b117b-122">-AgentName</span></span>
<span data-ttu-id="b117b-123">代理程式名稱</span><span class="sxs-lookup"><span data-stu-id="b117b-123">The agent name</span></span>

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

### <span data-ttu-id="b117b-124">-CommandText</span><span class="sxs-lookup"><span data-stu-id="b117b-124">-CommandText</span></span>
<span data-ttu-id="b117b-125">命令文字</span><span class="sxs-lookup"><span data-stu-id="b117b-125">The command text</span></span>

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

### <span data-ttu-id="b117b-126">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="b117b-126">-CredentialName</span></span>
<span data-ttu-id="b117b-127">認證名稱</span><span class="sxs-lookup"><span data-stu-id="b117b-127">The credential name</span></span>

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

### <span data-ttu-id="b117b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b117b-128">-DefaultProfile</span></span>
<span data-ttu-id="b117b-129">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b117b-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b117b-130">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="b117b-130">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="b117b-131">初始重試間隔秒數</span><span class="sxs-lookup"><span data-stu-id="b117b-131">The initial retry interval seconds</span></span>

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

### <span data-ttu-id="b117b-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b117b-132">-InputObject</span></span>
<span data-ttu-id="b117b-133">作業步驟物件</span><span class="sxs-lookup"><span data-stu-id="b117b-133">The job step object</span></span>

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

### <span data-ttu-id="b117b-134">-JobName</span><span class="sxs-lookup"><span data-stu-id="b117b-134">-JobName</span></span>
<span data-ttu-id="b117b-135">作業名稱</span><span class="sxs-lookup"><span data-stu-id="b117b-135">The job name</span></span>

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

### <span data-ttu-id="b117b-136">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="b117b-136">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="b117b-137">[重試間隔秒數] 的最大值</span><span class="sxs-lookup"><span data-stu-id="b117b-137">The maximum retry interval seconds</span></span>

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

### <span data-ttu-id="b117b-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="b117b-138">-Name</span></span>
<span data-ttu-id="b117b-139">步驟名稱</span><span class="sxs-lookup"><span data-stu-id="b117b-139">The step name</span></span>

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

### <span data-ttu-id="b117b-140">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="b117b-140">-OutputCredentialName</span></span>
<span data-ttu-id="b117b-141">輸出認證名稱</span><span class="sxs-lookup"><span data-stu-id="b117b-141">The output credential name</span></span>

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

### <span data-ttu-id="b117b-142">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="b117b-142">-OutputDatabaseObject</span></span>
<span data-ttu-id="b117b-143">輸出資料庫物件</span><span class="sxs-lookup"><span data-stu-id="b117b-143">The output database object</span></span>

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

### <span data-ttu-id="b117b-144">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="b117b-144">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="b117b-145">輸出資料庫資源識別碼</span><span class="sxs-lookup"><span data-stu-id="b117b-145">The output database resource id</span></span>

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

### <span data-ttu-id="b117b-146">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="b117b-146">-OutputSchemaName</span></span>
<span data-ttu-id="b117b-147">輸出架構名稱</span><span class="sxs-lookup"><span data-stu-id="b117b-147">The output schema name</span></span>

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

### <span data-ttu-id="b117b-148">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="b117b-148">-OutputTableName</span></span>
<span data-ttu-id="b117b-149">輸出資料表名稱</span><span class="sxs-lookup"><span data-stu-id="b117b-149">The output table name</span></span>

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

### <span data-ttu-id="b117b-150">-RemoveOutput</span><span class="sxs-lookup"><span data-stu-id="b117b-150">-RemoveOutput</span></span>
<span data-ttu-id="b117b-151">指示是否要移除輸出的標誌</span><span class="sxs-lookup"><span data-stu-id="b117b-151">The flag to indicate whether to remove output</span></span>

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

### <span data-ttu-id="b117b-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b117b-152">-ResourceGroupName</span></span>
<span data-ttu-id="b117b-153">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="b117b-153">The resource group name</span></span>

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

### <span data-ttu-id="b117b-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b117b-154">-ResourceId</span></span>
<span data-ttu-id="b117b-155">作業步驟資源識別碼</span><span class="sxs-lookup"><span data-stu-id="b117b-155">The job step resource id</span></span>

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

### <span data-ttu-id="b117b-156">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="b117b-156">-RetryAttempts</span></span>
<span data-ttu-id="b117b-157">[重試 attemps]</span><span class="sxs-lookup"><span data-stu-id="b117b-157">The retry attemps</span></span>

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

### <span data-ttu-id="b117b-158">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="b117b-158">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="b117b-159">重試間隔回退乘數</span><span class="sxs-lookup"><span data-stu-id="b117b-159">The retry interval backoff multiplier</span></span>

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

### <span data-ttu-id="b117b-160">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b117b-160">-ServerName</span></span>
<span data-ttu-id="b117b-161">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="b117b-161">The server name</span></span>

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

### <span data-ttu-id="b117b-162">-StepId</span><span class="sxs-lookup"><span data-stu-id="b117b-162">-StepId</span></span>
<span data-ttu-id="b117b-163">步驟識別碼文字</span><span class="sxs-lookup"><span data-stu-id="b117b-163">The step id text</span></span>

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

### <span data-ttu-id="b117b-164">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="b117b-164">-TargetGroupName</span></span>
<span data-ttu-id="b117b-165">目標群組名稱</span><span class="sxs-lookup"><span data-stu-id="b117b-165">The target group name</span></span>

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

### <span data-ttu-id="b117b-166">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="b117b-166">-TimeoutSeconds</span></span>
<span data-ttu-id="b117b-167">超時秒數</span><span class="sxs-lookup"><span data-stu-id="b117b-167">The timeout seconds</span></span>

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

### <span data-ttu-id="b117b-168">-確認</span><span class="sxs-lookup"><span data-stu-id="b117b-168">-Confirm</span></span>
<span data-ttu-id="b117b-169">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b117b-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b117b-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b117b-170">-WhatIf</span></span>
<span data-ttu-id="b117b-171">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b117b-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b117b-172">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b117b-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b117b-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b117b-173">CommonParameters</span></span>
<span data-ttu-id="b117b-174">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b117b-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b117b-175">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b117b-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b117b-176">輸入</span><span class="sxs-lookup"><span data-stu-id="b117b-176">INPUTS</span></span>

### <span data-ttu-id="b117b-177">AzureSqlElasticJobStepModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="b117b-177">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="b117b-178">輸出</span><span class="sxs-lookup"><span data-stu-id="b117b-178">OUTPUTS</span></span>

### <span data-ttu-id="b117b-179">AzureSqlElasticJobStepModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="b117b-179">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="b117b-180">筆記</span><span class="sxs-lookup"><span data-stu-id="b117b-180">NOTES</span></span>

## <span data-ttu-id="b117b-181">相關連結</span><span class="sxs-lookup"><span data-stu-id="b117b-181">RELATED LINKS</span></span>
