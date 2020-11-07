---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
ms.openlocfilehash: 25c9845d0912374baa0e2219c234f63abe381cfc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957216"
---
# <span data-ttu-id="c2680-101">Add-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="c2680-101">Add-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="c2680-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c2680-102">SYNOPSIS</span></span>
<span data-ttu-id="c2680-103">新增作業步驟至作業</span><span class="sxs-lookup"><span data-stu-id="c2680-103">Adds a job step to a job</span></span>

## <span data-ttu-id="c2680-104">句法</span><span class="sxs-lookup"><span data-stu-id="c2680-104">SYNTAX</span></span>

### <span data-ttu-id="c2680-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c2680-105">DefaultSet (Default)</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String> -Name <String>
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2680-106">WithOutputDb</span><span class="sxs-lookup"><span data-stu-id="c2680-106">WithOutputDb</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String> -OutputTableName <String>
 -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c2680-107">WithOutputDbId</span><span class="sxs-lookup"><span data-stu-id="c2680-107">WithOutputDbId</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseResourceId <String> -OutputCredentialName <String> -OutputTableName <String> -Name <String>
 [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c2680-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="c2680-108">ObjectSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c2680-109">WithOutputDbUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="c2680-109">WithOutputDbUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2680-110">WithOutputDbIdUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="c2680-110">WithOutputDbIdUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseResourceId <String>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2680-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c2680-111">ResourceIdSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c2680-112">WithOutputDbUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="c2680-112">WithOutputDbUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2680-113">WithOutputDbIdUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="c2680-113">WithOutputDbIdUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseResourceId <String> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2680-114">說明</span><span class="sxs-lookup"><span data-stu-id="c2680-114">DESCRIPTION</span></span>
<span data-ttu-id="c2680-115">Add-AzSqlElasticJobStep Cmdlet 會將作業步驟新增至作業</span><span class="sxs-lookup"><span data-stu-id="c2680-115">The Add-AzSqlElasticJobStep cmdlet adds a job step to a job</span></span>

## <span data-ttu-id="c2680-116">示例</span><span class="sxs-lookup"><span data-stu-id="c2680-116">EXAMPLES</span></span>

### <span data-ttu-id="c2680-117">範例 1-在作業中加入步驟</span><span class="sxs-lookup"><span data-stu-id="c2680-117">Example 1 - Adds a step to a job</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -Name job1
$job | Add-AzSqlElasticJobStep -Name step1 -TargetGroupName tg1 -CredentialName cred1 -CommandText "SELECT 1"

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="c2680-118">新增作業步驟至作業</span><span class="sxs-lookup"><span data-stu-id="c2680-118">Adds a job step to a job</span></span>

## <span data-ttu-id="c2680-119">參數</span><span class="sxs-lookup"><span data-stu-id="c2680-119">PARAMETERS</span></span>

### <span data-ttu-id="c2680-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="c2680-120">-AgentName</span></span>
<span data-ttu-id="c2680-121">代理程式名稱</span><span class="sxs-lookup"><span data-stu-id="c2680-121">The agent name</span></span>

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

### <span data-ttu-id="c2680-122">-CommandText</span><span class="sxs-lookup"><span data-stu-id="c2680-122">-CommandText</span></span>
<span data-ttu-id="c2680-123">命令文字</span><span class="sxs-lookup"><span data-stu-id="c2680-123">The command text</span></span>

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

### <span data-ttu-id="c2680-124">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="c2680-124">-CredentialName</span></span>
<span data-ttu-id="c2680-125">認證名稱</span><span class="sxs-lookup"><span data-stu-id="c2680-125">The credential name</span></span>

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

### <span data-ttu-id="c2680-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2680-126">-DefaultProfile</span></span>
<span data-ttu-id="c2680-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c2680-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2680-128">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="c2680-128">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="c2680-129">初始重試間隔秒數</span><span class="sxs-lookup"><span data-stu-id="c2680-129">The initial retry interval seconds</span></span>

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

### <span data-ttu-id="c2680-130">-JobName</span><span class="sxs-lookup"><span data-stu-id="c2680-130">-JobName</span></span>
<span data-ttu-id="c2680-131">作業名稱</span><span class="sxs-lookup"><span data-stu-id="c2680-131">The job name</span></span>

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

### <span data-ttu-id="c2680-132">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="c2680-132">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="c2680-133">[重試間隔秒數] 的最大值</span><span class="sxs-lookup"><span data-stu-id="c2680-133">The maximum retry interval seconds</span></span>

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

### <span data-ttu-id="c2680-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="c2680-134">-Name</span></span>
<span data-ttu-id="c2680-135">作業步驟名稱</span><span class="sxs-lookup"><span data-stu-id="c2680-135">The job step name</span></span>

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

### <span data-ttu-id="c2680-136">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="c2680-136">-OutputCredentialName</span></span>
<span data-ttu-id="c2680-137">輸出認證名稱</span><span class="sxs-lookup"><span data-stu-id="c2680-137">The output credential name</span></span>

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

### <span data-ttu-id="c2680-138">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="c2680-138">-OutputDatabaseObject</span></span>
<span data-ttu-id="c2680-139">輸出資料庫物件</span><span class="sxs-lookup"><span data-stu-id="c2680-139">The output database object</span></span>

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

### <span data-ttu-id="c2680-140">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="c2680-140">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="c2680-141">輸出資料庫資源識別碼</span><span class="sxs-lookup"><span data-stu-id="c2680-141">The output database resource id</span></span>

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

### <span data-ttu-id="c2680-142">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="c2680-142">-OutputSchemaName</span></span>
<span data-ttu-id="c2680-143">輸出架構名稱</span><span class="sxs-lookup"><span data-stu-id="c2680-143">The output schema name</span></span>

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

### <span data-ttu-id="c2680-144">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="c2680-144">-OutputTableName</span></span>
<span data-ttu-id="c2680-145">輸出資料表名稱</span><span class="sxs-lookup"><span data-stu-id="c2680-145">The output table name</span></span>

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

### <span data-ttu-id="c2680-146">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c2680-146">-ParentObject</span></span>
<span data-ttu-id="c2680-147">工作物件</span><span class="sxs-lookup"><span data-stu-id="c2680-147">The job object</span></span>

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

### <span data-ttu-id="c2680-148">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="c2680-148">-ParentResourceId</span></span>
<span data-ttu-id="c2680-149">作業資源識別碼</span><span class="sxs-lookup"><span data-stu-id="c2680-149">The job resource id</span></span>

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

### <span data-ttu-id="c2680-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2680-150">-ResourceGroupName</span></span>
<span data-ttu-id="c2680-151">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="c2680-151">The resource group name</span></span>

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

### <span data-ttu-id="c2680-152">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="c2680-152">-RetryAttempts</span></span>
<span data-ttu-id="c2680-153">重試嘗試</span><span class="sxs-lookup"><span data-stu-id="c2680-153">The retry attempts</span></span>

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

### <span data-ttu-id="c2680-154">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="c2680-154">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="c2680-155">重試間隔傳回乘數</span><span class="sxs-lookup"><span data-stu-id="c2680-155">The retry interval back off multiplier</span></span>

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

### <span data-ttu-id="c2680-156">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c2680-156">-ServerName</span></span>
<span data-ttu-id="c2680-157">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="c2680-157">The server name</span></span>

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

### <span data-ttu-id="c2680-158">-StepId</span><span class="sxs-lookup"><span data-stu-id="c2680-158">-StepId</span></span>
<span data-ttu-id="c2680-159">步驟識別碼</span><span class="sxs-lookup"><span data-stu-id="c2680-159">The step id</span></span>

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

### <span data-ttu-id="c2680-160">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="c2680-160">-TargetGroupName</span></span>
<span data-ttu-id="c2680-161">目標群組名稱</span><span class="sxs-lookup"><span data-stu-id="c2680-161">The target group name</span></span>

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

### <span data-ttu-id="c2680-162">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="c2680-162">-TimeoutSeconds</span></span>
<span data-ttu-id="c2680-163">超時秒數</span><span class="sxs-lookup"><span data-stu-id="c2680-163">The time out seconds</span></span>

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

### <span data-ttu-id="c2680-164">-確認</span><span class="sxs-lookup"><span data-stu-id="c2680-164">-Confirm</span></span>
<span data-ttu-id="c2680-165">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c2680-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2680-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2680-166">-WhatIf</span></span>
<span data-ttu-id="c2680-167">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c2680-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2680-168">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c2680-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2680-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2680-169">CommonParameters</span></span>
<span data-ttu-id="c2680-170">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c2680-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2680-171">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c2680-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2680-172">輸入</span><span class="sxs-lookup"><span data-stu-id="c2680-172">INPUTS</span></span>

### <span data-ttu-id="c2680-173">AzureSqlElasticJobModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="c2680-173">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="c2680-174">輸出</span><span class="sxs-lookup"><span data-stu-id="c2680-174">OUTPUTS</span></span>

### <span data-ttu-id="c2680-175">AzureSqlElasticJobStepModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="c2680-175">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="c2680-176">筆記</span><span class="sxs-lookup"><span data-stu-id="c2680-176">NOTES</span></span>

## <span data-ttu-id="c2680-177">相關連結</span><span class="sxs-lookup"><span data-stu-id="c2680-177">RELATED LINKS</span></span>
