---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
ms.openlocfilehash: dbc27ec87be3de4c320ad60b7dc204d704fe8f2f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98276040"
---
# <span data-ttu-id="7b843-101">Add-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="7b843-101">Add-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="7b843-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7b843-102">SYNOPSIS</span></span>
<span data-ttu-id="7b843-103">新增作業步驟至作業</span><span class="sxs-lookup"><span data-stu-id="7b843-103">Adds a job step to a job</span></span>

## <span data-ttu-id="7b843-104">句法</span><span class="sxs-lookup"><span data-stu-id="7b843-104">SYNTAX</span></span>

### <span data-ttu-id="7b843-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7b843-105">DefaultSet (Default)</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String> -Name <String>
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b843-106">WithOutputDb</span><span class="sxs-lookup"><span data-stu-id="7b843-106">WithOutputDb</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String> -OutputTableName <String>
 -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7b843-107">WithOutputDbId</span><span class="sxs-lookup"><span data-stu-id="7b843-107">WithOutputDbId</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseResourceId <String> -OutputCredentialName <String> -OutputTableName <String> -Name <String>
 [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7b843-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="7b843-108">ObjectSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7b843-109">WithOutputDbUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="7b843-109">WithOutputDbUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b843-110">WithOutputDbIdUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="7b843-110">WithOutputDbIdUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseResourceId <String>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b843-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7b843-111">ResourceIdSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7b843-112">WithOutputDbUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="7b843-112">WithOutputDbUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b843-113">WithOutputDbIdUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="7b843-113">WithOutputDbIdUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseResourceId <String> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b843-114">說明</span><span class="sxs-lookup"><span data-stu-id="7b843-114">DESCRIPTION</span></span>
<span data-ttu-id="7b843-115">Add-AzSqlElasticJobStep Cmdlet 會將作業步驟新增至作業</span><span class="sxs-lookup"><span data-stu-id="7b843-115">The Add-AzSqlElasticJobStep cmdlet adds a job step to a job</span></span>

## <span data-ttu-id="7b843-116">示例</span><span class="sxs-lookup"><span data-stu-id="7b843-116">EXAMPLES</span></span>

### <span data-ttu-id="7b843-117">範例1：在作業中加入步驟</span><span class="sxs-lookup"><span data-stu-id="7b843-117">Example 1: Adds a step to a job</span></span>
```powershell
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -Name job1
$job | Add-AzSqlElasticJobStep -Name step1 -TargetGroupName tg1 -CredentialName cred1 -CommandText "SELECT 1"

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="7b843-118">新增作業步驟至作業</span><span class="sxs-lookup"><span data-stu-id="7b843-118">Adds a job step to a job</span></span>

## <span data-ttu-id="7b843-119">參數</span><span class="sxs-lookup"><span data-stu-id="7b843-119">PARAMETERS</span></span>

### <span data-ttu-id="7b843-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="7b843-120">-AgentName</span></span>
<span data-ttu-id="7b843-121">代理程式名稱</span><span class="sxs-lookup"><span data-stu-id="7b843-121">The agent name</span></span>

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

### <span data-ttu-id="7b843-122">-CommandText</span><span class="sxs-lookup"><span data-stu-id="7b843-122">-CommandText</span></span>
<span data-ttu-id="7b843-123">命令文字</span><span class="sxs-lookup"><span data-stu-id="7b843-123">The command text</span></span>

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

### <span data-ttu-id="7b843-124">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="7b843-124">-CredentialName</span></span>
<span data-ttu-id="7b843-125">認證名稱</span><span class="sxs-lookup"><span data-stu-id="7b843-125">The credential name</span></span>

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

### <span data-ttu-id="7b843-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b843-126">-DefaultProfile</span></span>
<span data-ttu-id="7b843-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7b843-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b843-128">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="7b843-128">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="7b843-129">初始重試間隔秒數</span><span class="sxs-lookup"><span data-stu-id="7b843-129">The initial retry interval seconds</span></span>

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

### <span data-ttu-id="7b843-130">-JobName</span><span class="sxs-lookup"><span data-stu-id="7b843-130">-JobName</span></span>
<span data-ttu-id="7b843-131">作業名稱</span><span class="sxs-lookup"><span data-stu-id="7b843-131">The job name</span></span>

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

### <span data-ttu-id="7b843-132">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="7b843-132">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="7b843-133">[重試間隔秒數] 的最大值</span><span class="sxs-lookup"><span data-stu-id="7b843-133">The maximum retry interval seconds</span></span>

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

### <span data-ttu-id="7b843-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="7b843-134">-Name</span></span>
<span data-ttu-id="7b843-135">作業步驟名稱</span><span class="sxs-lookup"><span data-stu-id="7b843-135">The job step name</span></span>

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

### <span data-ttu-id="7b843-136">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="7b843-136">-OutputCredentialName</span></span>
<span data-ttu-id="7b843-137">輸出認證名稱</span><span class="sxs-lookup"><span data-stu-id="7b843-137">The output credential name</span></span>

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

### <span data-ttu-id="7b843-138">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="7b843-138">-OutputDatabaseObject</span></span>
<span data-ttu-id="7b843-139">輸出資料庫物件</span><span class="sxs-lookup"><span data-stu-id="7b843-139">The output database object</span></span>

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

### <span data-ttu-id="7b843-140">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="7b843-140">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="7b843-141">輸出資料庫資源識別碼</span><span class="sxs-lookup"><span data-stu-id="7b843-141">The output database resource id</span></span>

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

### <span data-ttu-id="7b843-142">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="7b843-142">-OutputSchemaName</span></span>
<span data-ttu-id="7b843-143">輸出架構名稱</span><span class="sxs-lookup"><span data-stu-id="7b843-143">The output schema name</span></span>

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

### <span data-ttu-id="7b843-144">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="7b843-144">-OutputTableName</span></span>
<span data-ttu-id="7b843-145">輸出資料表名稱</span><span class="sxs-lookup"><span data-stu-id="7b843-145">The output table name</span></span>

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

### <span data-ttu-id="7b843-146">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7b843-146">-ParentObject</span></span>
<span data-ttu-id="7b843-147">工作物件</span><span class="sxs-lookup"><span data-stu-id="7b843-147">The job object</span></span>

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

### <span data-ttu-id="7b843-148">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="7b843-148">-ParentResourceId</span></span>
<span data-ttu-id="7b843-149">作業資源識別碼</span><span class="sxs-lookup"><span data-stu-id="7b843-149">The job resource id</span></span>

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

### <span data-ttu-id="7b843-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b843-150">-ResourceGroupName</span></span>
<span data-ttu-id="7b843-151">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="7b843-151">The resource group name</span></span>

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

### <span data-ttu-id="7b843-152">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="7b843-152">-RetryAttempts</span></span>
<span data-ttu-id="7b843-153">重試嘗試</span><span class="sxs-lookup"><span data-stu-id="7b843-153">The retry attempts</span></span>

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

### <span data-ttu-id="7b843-154">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="7b843-154">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="7b843-155">重試間隔傳回乘數</span><span class="sxs-lookup"><span data-stu-id="7b843-155">The retry interval back off multiplier</span></span>

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

### <span data-ttu-id="7b843-156">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7b843-156">-ServerName</span></span>
<span data-ttu-id="7b843-157">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="7b843-157">The server name</span></span>

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

### <span data-ttu-id="7b843-158">-StepId</span><span class="sxs-lookup"><span data-stu-id="7b843-158">-StepId</span></span>
<span data-ttu-id="7b843-159">步驟識別碼</span><span class="sxs-lookup"><span data-stu-id="7b843-159">The step id</span></span>

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

### <span data-ttu-id="7b843-160">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="7b843-160">-TargetGroupName</span></span>
<span data-ttu-id="7b843-161">目標群組名稱</span><span class="sxs-lookup"><span data-stu-id="7b843-161">The target group name</span></span>

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

### <span data-ttu-id="7b843-162">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="7b843-162">-TimeoutSeconds</span></span>
<span data-ttu-id="7b843-163">超時秒數</span><span class="sxs-lookup"><span data-stu-id="7b843-163">The time out seconds</span></span>

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

### <span data-ttu-id="7b843-164">-確認</span><span class="sxs-lookup"><span data-stu-id="7b843-164">-Confirm</span></span>
<span data-ttu-id="7b843-165">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7b843-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b843-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b843-166">-WhatIf</span></span>
<span data-ttu-id="7b843-167">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7b843-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b843-168">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7b843-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b843-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b843-169">CommonParameters</span></span>
<span data-ttu-id="7b843-170">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7b843-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b843-171">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7b843-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b843-172">輸入</span><span class="sxs-lookup"><span data-stu-id="7b843-172">INPUTS</span></span>

### <span data-ttu-id="7b843-173">AzureSqlElasticJobModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="7b843-173">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="7b843-174">輸出</span><span class="sxs-lookup"><span data-stu-id="7b843-174">OUTPUTS</span></span>

### <span data-ttu-id="7b843-175">AzureSqlElasticJobStepModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="7b843-175">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="7b843-176">筆記</span><span class="sxs-lookup"><span data-stu-id="7b843-176">NOTES</span></span>

## <span data-ttu-id="7b843-177">相關連結</span><span class="sxs-lookup"><span data-stu-id="7b843-177">RELATED LINKS</span></span>
