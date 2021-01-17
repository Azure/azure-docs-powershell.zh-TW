---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobstepexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStepExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStepExecution.md
ms.openlocfilehash: 03c4a6dede1f60e782bbfecdec1fb18894b2ca15
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448116"
---
# <span data-ttu-id="646db-101">Get-AzSqlElasticJobStepExecution</span><span class="sxs-lookup"><span data-stu-id="646db-101">Get-AzSqlElasticJobStepExecution</span></span>

## <span data-ttu-id="646db-102">摘要</span><span class="sxs-lookup"><span data-stu-id="646db-102">SYNOPSIS</span></span>
<span data-ttu-id="646db-103">取得一或多個作業步驟執行</span><span class="sxs-lookup"><span data-stu-id="646db-103">Gets one or more job step executions</span></span>

## <span data-ttu-id="646db-104">句法</span><span class="sxs-lookup"><span data-stu-id="646db-104">SYNTAX</span></span>

### <span data-ttu-id="646db-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="646db-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobStepExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>]
 [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="646db-106">WithJobStepName</span><span class="sxs-lookup"><span data-stu-id="646db-106">WithJobStepName</span></span>
```
Get-AzSqlElasticJobStepExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> -StepName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="646db-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="646db-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="646db-108">WithJobStepNameUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="646db-108">WithJobStepNameUsingParentObject</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> -StepName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="646db-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="646db-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentResourceId] <String> [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="646db-110">WithJobStepNameUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="646db-110">WithJobStepNameUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentResourceId] <String> -StepName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="646db-111">說明</span><span class="sxs-lookup"><span data-stu-id="646db-111">DESCRIPTION</span></span>
<span data-ttu-id="646db-112">Get-AzSqlElasticJobStepExecution Cmdlet 會從作業執行中取得一或多個作業步驟執行</span><span class="sxs-lookup"><span data-stu-id="646db-112">The Get-AzSqlElasticJobStepExecution cmdlet gets one or more job step executions from a job execution</span></span>

## <span data-ttu-id="646db-113">示例</span><span class="sxs-lookup"><span data-stu-id="646db-113">EXAMPLES</span></span>

### <span data-ttu-id="646db-114">範例 1-從作業執行中取得一或多個作業步驟執行</span><span class="sxs-lookup"><span data-stu-id="646db-114">Example 1 - Gets one or more job step executions from a job executions</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobStepExecution

JobName JobVersion StepName StepId JobExecutionId                       Lifecycle StartTime            EndTime
------- ---------- -------- ------ --------------                       --------- ---------            -------
job1    1          step1    1      3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

### <span data-ttu-id="646db-115">範例 2-從作業執行中取得一或多個作業步驟執行，並依步驟名稱篩選</span><span class="sxs-lookup"><span data-stu-id="646db-115">Example 2 - Gets one or more job step executions from a job execution, filtering by step name</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobStepExecution -StepName step1

JobName JobVersion StepName StepId JobExecutionId                       Lifecycle StartTime            EndTime
------- ---------- -------- ------ --------------                       --------- ---------            -------
job1    1          step1    1      3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

<span data-ttu-id="646db-116">取得一或多個作業步驟執行</span><span class="sxs-lookup"><span data-stu-id="646db-116">Gets one or more job step executions</span></span>

## <span data-ttu-id="646db-117">參數</span><span class="sxs-lookup"><span data-stu-id="646db-117">PARAMETERS</span></span>

### <span data-ttu-id="646db-118">-使用中</span><span class="sxs-lookup"><span data-stu-id="646db-118">-Active</span></span>
<span data-ttu-id="646db-119">[旗標]：依作用中的執行進行篩選。</span><span class="sxs-lookup"><span data-stu-id="646db-119">Flag to filter by active executions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="646db-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="646db-120">-AgentName</span></span>
<span data-ttu-id="646db-121">[代理程式名稱]。</span><span class="sxs-lookup"><span data-stu-id="646db-121">The agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="646db-122">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="646db-122">-CreateTimeMax</span></span>
<span data-ttu-id="646db-123">依建立時間上限來篩選</span><span class="sxs-lookup"><span data-stu-id="646db-123">Filter by create time max</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="646db-124">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="646db-124">-CreateTimeMin</span></span>
<span data-ttu-id="646db-125">依建立時間最小值篩選</span><span class="sxs-lookup"><span data-stu-id="646db-125">Filter by create time min</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="646db-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="646db-126">-DefaultProfile</span></span>
<span data-ttu-id="646db-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="646db-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="646db-128">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="646db-128">-EndTimeMax</span></span>
<span data-ttu-id="646db-129">依 [結束時間上限] 篩選。</span><span class="sxs-lookup"><span data-stu-id="646db-129">Filter by end time max.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="646db-130">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="646db-130">-EndTimeMin</span></span>
<span data-ttu-id="646db-131">依 [最小結束時間] 篩選。</span><span class="sxs-lookup"><span data-stu-id="646db-131">Filter by end time min.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="646db-132">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="646db-132">-JobExecutionId</span></span>
<span data-ttu-id="646db-133">作業執行 id。</span><span class="sxs-lookup"><span data-stu-id="646db-133">The job execution id.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="646db-134">-JobName</span><span class="sxs-lookup"><span data-stu-id="646db-134">-JobName</span></span>
<span data-ttu-id="646db-135">作業名稱。</span><span class="sxs-lookup"><span data-stu-id="646db-135">The job name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="646db-136">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="646db-136">-ParentObject</span></span>
<span data-ttu-id="646db-137">Agent 物件。</span><span class="sxs-lookup"><span data-stu-id="646db-137">The agent object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel
Parameter Sets: ObjectSet, WithJobStepNameUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="646db-138">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="646db-138">-ParentResourceId</span></span>
<span data-ttu-id="646db-139">作業執行資源 id。</span><span class="sxs-lookup"><span data-stu-id="646db-139">The job execution resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, WithJobStepNameUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="646db-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="646db-140">-ResourceGroupName</span></span>
<span data-ttu-id="646db-141">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="646db-141">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="646db-142">-ServerName</span><span class="sxs-lookup"><span data-stu-id="646db-142">-ServerName</span></span>
<span data-ttu-id="646db-143">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="646db-143">The server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="646db-144">-StepName</span><span class="sxs-lookup"><span data-stu-id="646db-144">-StepName</span></span>
<span data-ttu-id="646db-145">作業步驟名稱。</span><span class="sxs-lookup"><span data-stu-id="646db-145">The job step name.</span></span>

```yaml
Type: System.String
Parameter Sets: WithJobStepName, WithJobStepNameUsingParentObject, WithJobStepNameUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="646db-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="646db-146">CommonParameters</span></span>
<span data-ttu-id="646db-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="646db-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="646db-148">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="646db-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="646db-149">輸入</span><span class="sxs-lookup"><span data-stu-id="646db-149">INPUTS</span></span>

### <span data-ttu-id="646db-150">AzureSqlElasticJobExecutionModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="646db-150">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="646db-151">輸出</span><span class="sxs-lookup"><span data-stu-id="646db-151">OUTPUTS</span></span>

### <span data-ttu-id="646db-152">AzureSqlElasticJobExecutionModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="646db-152">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="646db-153">筆記</span><span class="sxs-lookup"><span data-stu-id="646db-153">NOTES</span></span>

## <span data-ttu-id="646db-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="646db-154">RELATED LINKS</span></span>
