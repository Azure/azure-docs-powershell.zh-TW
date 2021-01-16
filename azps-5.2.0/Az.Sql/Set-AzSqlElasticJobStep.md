---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
ms.openlocfilehash: 4f6f0471224799e818f9db29e5be5a4c49f9c45e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280975"
---
# <span data-ttu-id="bacad-101">Set-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="bacad-101">Set-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="bacad-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bacad-102">SYNOPSIS</span></span>
<span data-ttu-id="bacad-103">更新作業步驟</span><span class="sxs-lookup"><span data-stu-id="bacad-103">Updates a job step</span></span>

## <span data-ttu-id="bacad-104">句法</span><span class="sxs-lookup"><span data-stu-id="bacad-104">SYNTAX</span></span>

### <span data-ttu-id="bacad-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="bacad-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bacad-106">WithRemoveOutput</span><span class="sxs-lookup"><span data-stu-id="bacad-106">WithRemoveOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-RemoveOutput] [-TargetGroupName <String>] [-CredentialName <String>]
 [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bacad-107">WithAddOutput</span><span class="sxs-lookup"><span data-stu-id="bacad-107">WithAddOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -OutputDatabaseResourceId <String> [-OutputCredentialName <String>]
 [-OutputTableName <String>] [-OutputSchemaName <String>] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bacad-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="bacad-108">ObjectSet</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-OutputDatabaseObject <AzureSqlDatabaseModel>] [-OutputCredentialName <String>] [-OutputTableName <String>]
 [-OutputSchemaName <String>] [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bacad-109">WithRemoveOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="bacad-109">WithRemoveOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> [-RemoveOutput]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bacad-110">WithAddOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="bacad-110">WithAddOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bacad-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="bacad-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bacad-112">WithRemoveOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="bacad-112">WithRemoveOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-RemoveOutput] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bacad-113">WithAddOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="bacad-113">WithAddOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bacad-114">說明</span><span class="sxs-lookup"><span data-stu-id="bacad-114">DESCRIPTION</span></span>
<span data-ttu-id="bacad-115">Set-AzSqlElasticJobStep Cmdlet 會更新作業步驟</span><span class="sxs-lookup"><span data-stu-id="bacad-115">The Set-AzSqlElasticJobStep cmdlet updates a job step</span></span>

## <span data-ttu-id="bacad-116">示例</span><span class="sxs-lookup"><span data-stu-id="bacad-116">EXAMPLES</span></span>

### <span data-ttu-id="bacad-117">範例1：更新作業的作業步驟目標群組</span><span class="sxs-lookup"><span data-stu-id="bacad-117">Example 1: Updates a job step's target group for a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -TargetGroupName tg2

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg2             cred1                 (43200,10,1,120,2) SELECT 1
```

### <span data-ttu-id="bacad-118">範例2：更新作業步驟的 T-sql 腳本以進行工作</span><span class="sxs-lookup"><span data-stu-id="bacad-118">Example 2: Updates a job step's T-SQL script for a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -CommandText "SELECT 2"

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 2
```

<span data-ttu-id="bacad-119">從工作更新作業步驟</span><span class="sxs-lookup"><span data-stu-id="bacad-119">Updates a job step from a job</span></span>

### <span data-ttu-id="bacad-120">範例3</span><span class="sxs-lookup"><span data-stu-id="bacad-120">Example 3</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticJobStep -AgentName agent -CommandText 'SELECT 2' -JobName job1 -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="bacad-121">參數</span><span class="sxs-lookup"><span data-stu-id="bacad-121">PARAMETERS</span></span>

### <span data-ttu-id="bacad-122">-AgentName</span><span class="sxs-lookup"><span data-stu-id="bacad-122">-AgentName</span></span>
<span data-ttu-id="bacad-123">代理程式名稱</span><span class="sxs-lookup"><span data-stu-id="bacad-123">The agent name</span></span>

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

### <span data-ttu-id="bacad-124">-CommandText</span><span class="sxs-lookup"><span data-stu-id="bacad-124">-CommandText</span></span>
<span data-ttu-id="bacad-125">命令文字</span><span class="sxs-lookup"><span data-stu-id="bacad-125">The command text</span></span>

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

### <span data-ttu-id="bacad-126">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="bacad-126">-CredentialName</span></span>
<span data-ttu-id="bacad-127">認證名稱</span><span class="sxs-lookup"><span data-stu-id="bacad-127">The credential name</span></span>

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

### <span data-ttu-id="bacad-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bacad-128">-DefaultProfile</span></span>
<span data-ttu-id="bacad-129">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bacad-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bacad-130">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="bacad-130">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="bacad-131">初始重試間隔秒數</span><span class="sxs-lookup"><span data-stu-id="bacad-131">The initial retry interval seconds</span></span>

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

### <span data-ttu-id="bacad-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bacad-132">-InputObject</span></span>
<span data-ttu-id="bacad-133">作業步驟物件</span><span class="sxs-lookup"><span data-stu-id="bacad-133">The job step object</span></span>

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

### <span data-ttu-id="bacad-134">-JobName</span><span class="sxs-lookup"><span data-stu-id="bacad-134">-JobName</span></span>
<span data-ttu-id="bacad-135">作業名稱</span><span class="sxs-lookup"><span data-stu-id="bacad-135">The job name</span></span>

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

### <span data-ttu-id="bacad-136">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="bacad-136">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="bacad-137">[重試間隔秒數] 的最大值</span><span class="sxs-lookup"><span data-stu-id="bacad-137">The maximum retry interval seconds</span></span>

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

### <span data-ttu-id="bacad-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="bacad-138">-Name</span></span>
<span data-ttu-id="bacad-139">步驟名稱</span><span class="sxs-lookup"><span data-stu-id="bacad-139">The step name</span></span>

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

### <span data-ttu-id="bacad-140">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="bacad-140">-OutputCredentialName</span></span>
<span data-ttu-id="bacad-141">輸出認證名稱</span><span class="sxs-lookup"><span data-stu-id="bacad-141">The output credential name</span></span>

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

### <span data-ttu-id="bacad-142">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="bacad-142">-OutputDatabaseObject</span></span>
<span data-ttu-id="bacad-143">輸出資料庫物件</span><span class="sxs-lookup"><span data-stu-id="bacad-143">The output database object</span></span>

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

### <span data-ttu-id="bacad-144">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="bacad-144">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="bacad-145">輸出資料庫資源識別碼</span><span class="sxs-lookup"><span data-stu-id="bacad-145">The output database resource id</span></span>

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

### <span data-ttu-id="bacad-146">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="bacad-146">-OutputSchemaName</span></span>
<span data-ttu-id="bacad-147">輸出架構名稱</span><span class="sxs-lookup"><span data-stu-id="bacad-147">The output schema name</span></span>

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

### <span data-ttu-id="bacad-148">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="bacad-148">-OutputTableName</span></span>
<span data-ttu-id="bacad-149">輸出資料表名稱</span><span class="sxs-lookup"><span data-stu-id="bacad-149">The output table name</span></span>

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

### <span data-ttu-id="bacad-150">-RemoveOutput</span><span class="sxs-lookup"><span data-stu-id="bacad-150">-RemoveOutput</span></span>
<span data-ttu-id="bacad-151">指示是否要移除輸出的標誌</span><span class="sxs-lookup"><span data-stu-id="bacad-151">The flag to indicate whether to remove output</span></span>

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

### <span data-ttu-id="bacad-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bacad-152">-ResourceGroupName</span></span>
<span data-ttu-id="bacad-153">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="bacad-153">The resource group name</span></span>

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

### <span data-ttu-id="bacad-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bacad-154">-ResourceId</span></span>
<span data-ttu-id="bacad-155">作業步驟資源識別碼</span><span class="sxs-lookup"><span data-stu-id="bacad-155">The job step resource id</span></span>

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

### <span data-ttu-id="bacad-156">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="bacad-156">-RetryAttempts</span></span>
<span data-ttu-id="bacad-157">[重試 attemps]</span><span class="sxs-lookup"><span data-stu-id="bacad-157">The retry attemps</span></span>

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

### <span data-ttu-id="bacad-158">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="bacad-158">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="bacad-159">重試間隔回退乘數</span><span class="sxs-lookup"><span data-stu-id="bacad-159">The retry interval backoff multiplier</span></span>

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

### <span data-ttu-id="bacad-160">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bacad-160">-ServerName</span></span>
<span data-ttu-id="bacad-161">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="bacad-161">The server name</span></span>

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

### <span data-ttu-id="bacad-162">-StepId</span><span class="sxs-lookup"><span data-stu-id="bacad-162">-StepId</span></span>
<span data-ttu-id="bacad-163">步驟識別碼文字</span><span class="sxs-lookup"><span data-stu-id="bacad-163">The step id text</span></span>

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

### <span data-ttu-id="bacad-164">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="bacad-164">-TargetGroupName</span></span>
<span data-ttu-id="bacad-165">目標群組名稱</span><span class="sxs-lookup"><span data-stu-id="bacad-165">The target group name</span></span>

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

### <span data-ttu-id="bacad-166">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="bacad-166">-TimeoutSeconds</span></span>
<span data-ttu-id="bacad-167">超時秒數</span><span class="sxs-lookup"><span data-stu-id="bacad-167">The timeout seconds</span></span>

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

### <span data-ttu-id="bacad-168">-確認</span><span class="sxs-lookup"><span data-stu-id="bacad-168">-Confirm</span></span>
<span data-ttu-id="bacad-169">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bacad-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bacad-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bacad-170">-WhatIf</span></span>
<span data-ttu-id="bacad-171">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bacad-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bacad-172">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bacad-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bacad-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bacad-173">CommonParameters</span></span>
<span data-ttu-id="bacad-174">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bacad-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bacad-175">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="bacad-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bacad-176">輸入</span><span class="sxs-lookup"><span data-stu-id="bacad-176">INPUTS</span></span>

### <span data-ttu-id="bacad-177">AzureSqlElasticJobStepModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="bacad-177">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="bacad-178">輸出</span><span class="sxs-lookup"><span data-stu-id="bacad-178">OUTPUTS</span></span>

### <span data-ttu-id="bacad-179">AzureSqlElasticJobStepModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="bacad-179">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="bacad-180">筆記</span><span class="sxs-lookup"><span data-stu-id="bacad-180">NOTES</span></span>

## <span data-ttu-id="bacad-181">相關連結</span><span class="sxs-lookup"><span data-stu-id="bacad-181">RELATED LINKS</span></span>
