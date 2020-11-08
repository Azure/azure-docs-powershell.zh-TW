---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
ms.openlocfilehash: 4f6f0471224799e818f9db29e5be5a4c49f9c45e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129820"
---
# <span data-ttu-id="ec277-101">Set-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="ec277-101">Set-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="ec277-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ec277-102">SYNOPSIS</span></span>
<span data-ttu-id="ec277-103">更新作業步驟</span><span class="sxs-lookup"><span data-stu-id="ec277-103">Updates a job step</span></span>

## <span data-ttu-id="ec277-104">句法</span><span class="sxs-lookup"><span data-stu-id="ec277-104">SYNTAX</span></span>

### <span data-ttu-id="ec277-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ec277-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec277-106">WithRemoveOutput</span><span class="sxs-lookup"><span data-stu-id="ec277-106">WithRemoveOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-RemoveOutput] [-TargetGroupName <String>] [-CredentialName <String>]
 [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ec277-107">WithAddOutput</span><span class="sxs-lookup"><span data-stu-id="ec277-107">WithAddOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -OutputDatabaseResourceId <String> [-OutputCredentialName <String>]
 [-OutputTableName <String>] [-OutputSchemaName <String>] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ec277-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="ec277-108">ObjectSet</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-OutputDatabaseObject <AzureSqlDatabaseModel>] [-OutputCredentialName <String>] [-OutputTableName <String>]
 [-OutputSchemaName <String>] [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec277-109">WithRemoveOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="ec277-109">WithRemoveOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> [-RemoveOutput]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec277-110">WithAddOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="ec277-110">WithAddOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec277-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ec277-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec277-112">WithRemoveOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ec277-112">WithRemoveOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-RemoveOutput] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ec277-113">WithAddOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ec277-113">WithAddOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec277-114">說明</span><span class="sxs-lookup"><span data-stu-id="ec277-114">DESCRIPTION</span></span>
<span data-ttu-id="ec277-115">Set-AzSqlElasticJobStep Cmdlet 會更新作業步驟</span><span class="sxs-lookup"><span data-stu-id="ec277-115">The Set-AzSqlElasticJobStep cmdlet updates a job step</span></span>

## <span data-ttu-id="ec277-116">示例</span><span class="sxs-lookup"><span data-stu-id="ec277-116">EXAMPLES</span></span>

### <span data-ttu-id="ec277-117">範例1：更新作業的作業步驟目標群組</span><span class="sxs-lookup"><span data-stu-id="ec277-117">Example 1: Updates a job step's target group for a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -TargetGroupName tg2

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg2             cred1                 (43200,10,1,120,2) SELECT 1
```

### <span data-ttu-id="ec277-118">範例2：更新作業步驟的 T-sql 腳本以進行工作</span><span class="sxs-lookup"><span data-stu-id="ec277-118">Example 2: Updates a job step's T-SQL script for a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -CommandText "SELECT 2"

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 2
```

<span data-ttu-id="ec277-119">從工作更新作業步驟</span><span class="sxs-lookup"><span data-stu-id="ec277-119">Updates a job step from a job</span></span>

### <span data-ttu-id="ec277-120">範例3</span><span class="sxs-lookup"><span data-stu-id="ec277-120">Example 3</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticJobStep -AgentName agent -CommandText 'SELECT 2' -JobName job1 -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="ec277-121">參數</span><span class="sxs-lookup"><span data-stu-id="ec277-121">PARAMETERS</span></span>

### <span data-ttu-id="ec277-122">-AgentName</span><span class="sxs-lookup"><span data-stu-id="ec277-122">-AgentName</span></span>
<span data-ttu-id="ec277-123">代理程式名稱</span><span class="sxs-lookup"><span data-stu-id="ec277-123">The agent name</span></span>

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

### <span data-ttu-id="ec277-124">-CommandText</span><span class="sxs-lookup"><span data-stu-id="ec277-124">-CommandText</span></span>
<span data-ttu-id="ec277-125">命令文字</span><span class="sxs-lookup"><span data-stu-id="ec277-125">The command text</span></span>

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

### <span data-ttu-id="ec277-126">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="ec277-126">-CredentialName</span></span>
<span data-ttu-id="ec277-127">認證名稱</span><span class="sxs-lookup"><span data-stu-id="ec277-127">The credential name</span></span>

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

### <span data-ttu-id="ec277-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec277-128">-DefaultProfile</span></span>
<span data-ttu-id="ec277-129">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ec277-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec277-130">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="ec277-130">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="ec277-131">初始重試間隔秒數</span><span class="sxs-lookup"><span data-stu-id="ec277-131">The initial retry interval seconds</span></span>

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

### <span data-ttu-id="ec277-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec277-132">-InputObject</span></span>
<span data-ttu-id="ec277-133">作業步驟物件</span><span class="sxs-lookup"><span data-stu-id="ec277-133">The job step object</span></span>

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

### <span data-ttu-id="ec277-134">-JobName</span><span class="sxs-lookup"><span data-stu-id="ec277-134">-JobName</span></span>
<span data-ttu-id="ec277-135">作業名稱</span><span class="sxs-lookup"><span data-stu-id="ec277-135">The job name</span></span>

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

### <span data-ttu-id="ec277-136">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="ec277-136">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="ec277-137">[重試間隔秒數] 的最大值</span><span class="sxs-lookup"><span data-stu-id="ec277-137">The maximum retry interval seconds</span></span>

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

### <span data-ttu-id="ec277-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="ec277-138">-Name</span></span>
<span data-ttu-id="ec277-139">步驟名稱</span><span class="sxs-lookup"><span data-stu-id="ec277-139">The step name</span></span>

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

### <span data-ttu-id="ec277-140">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="ec277-140">-OutputCredentialName</span></span>
<span data-ttu-id="ec277-141">輸出認證名稱</span><span class="sxs-lookup"><span data-stu-id="ec277-141">The output credential name</span></span>

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

### <span data-ttu-id="ec277-142">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="ec277-142">-OutputDatabaseObject</span></span>
<span data-ttu-id="ec277-143">輸出資料庫物件</span><span class="sxs-lookup"><span data-stu-id="ec277-143">The output database object</span></span>

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

### <span data-ttu-id="ec277-144">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="ec277-144">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="ec277-145">輸出資料庫資源識別碼</span><span class="sxs-lookup"><span data-stu-id="ec277-145">The output database resource id</span></span>

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

### <span data-ttu-id="ec277-146">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="ec277-146">-OutputSchemaName</span></span>
<span data-ttu-id="ec277-147">輸出架構名稱</span><span class="sxs-lookup"><span data-stu-id="ec277-147">The output schema name</span></span>

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

### <span data-ttu-id="ec277-148">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="ec277-148">-OutputTableName</span></span>
<span data-ttu-id="ec277-149">輸出資料表名稱</span><span class="sxs-lookup"><span data-stu-id="ec277-149">The output table name</span></span>

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

### <span data-ttu-id="ec277-150">-RemoveOutput</span><span class="sxs-lookup"><span data-stu-id="ec277-150">-RemoveOutput</span></span>
<span data-ttu-id="ec277-151">指示是否要移除輸出的標誌</span><span class="sxs-lookup"><span data-stu-id="ec277-151">The flag to indicate whether to remove output</span></span>

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

### <span data-ttu-id="ec277-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec277-152">-ResourceGroupName</span></span>
<span data-ttu-id="ec277-153">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="ec277-153">The resource group name</span></span>

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

### <span data-ttu-id="ec277-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec277-154">-ResourceId</span></span>
<span data-ttu-id="ec277-155">作業步驟資源識別碼</span><span class="sxs-lookup"><span data-stu-id="ec277-155">The job step resource id</span></span>

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

### <span data-ttu-id="ec277-156">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="ec277-156">-RetryAttempts</span></span>
<span data-ttu-id="ec277-157">[重試 attemps]</span><span class="sxs-lookup"><span data-stu-id="ec277-157">The retry attemps</span></span>

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

### <span data-ttu-id="ec277-158">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="ec277-158">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="ec277-159">重試間隔回退乘數</span><span class="sxs-lookup"><span data-stu-id="ec277-159">The retry interval backoff multiplier</span></span>

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

### <span data-ttu-id="ec277-160">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ec277-160">-ServerName</span></span>
<span data-ttu-id="ec277-161">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="ec277-161">The server name</span></span>

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

### <span data-ttu-id="ec277-162">-StepId</span><span class="sxs-lookup"><span data-stu-id="ec277-162">-StepId</span></span>
<span data-ttu-id="ec277-163">步驟識別碼文字</span><span class="sxs-lookup"><span data-stu-id="ec277-163">The step id text</span></span>

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

### <span data-ttu-id="ec277-164">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="ec277-164">-TargetGroupName</span></span>
<span data-ttu-id="ec277-165">目標群組名稱</span><span class="sxs-lookup"><span data-stu-id="ec277-165">The target group name</span></span>

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

### <span data-ttu-id="ec277-166">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="ec277-166">-TimeoutSeconds</span></span>
<span data-ttu-id="ec277-167">超時秒數</span><span class="sxs-lookup"><span data-stu-id="ec277-167">The timeout seconds</span></span>

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

### <span data-ttu-id="ec277-168">-確認</span><span class="sxs-lookup"><span data-stu-id="ec277-168">-Confirm</span></span>
<span data-ttu-id="ec277-169">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ec277-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec277-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec277-170">-WhatIf</span></span>
<span data-ttu-id="ec277-171">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ec277-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec277-172">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ec277-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec277-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec277-173">CommonParameters</span></span>
<span data-ttu-id="ec277-174">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ec277-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec277-175">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ec277-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec277-176">輸入</span><span class="sxs-lookup"><span data-stu-id="ec277-176">INPUTS</span></span>

### <span data-ttu-id="ec277-177">AzureSqlElasticJobStepModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="ec277-177">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="ec277-178">輸出</span><span class="sxs-lookup"><span data-stu-id="ec277-178">OUTPUTS</span></span>

### <span data-ttu-id="ec277-179">AzureSqlElasticJobStepModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="ec277-179">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="ec277-180">筆記</span><span class="sxs-lookup"><span data-stu-id="ec277-180">NOTES</span></span>

## <span data-ttu-id="ec277-181">相關連結</span><span class="sxs-lookup"><span data-stu-id="ec277-181">RELATED LINKS</span></span>
