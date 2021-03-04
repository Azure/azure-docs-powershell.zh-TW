---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/get-Azsqlelasticjobstepexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStepExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStepExecution.md
ms.openlocfilehash: 9918c314d239bf822fa789bcab6a9de923b8c2e2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914362"
---
# <span data-ttu-id="3a765-101">Get-AzSqlElasticJobStepExecution</span><span class="sxs-lookup"><span data-stu-id="3a765-101">Get-AzSqlElasticJobStepExecution</span></span>

## <span data-ttu-id="3a765-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3a765-102">SYNOPSIS</span></span>
<span data-ttu-id="3a765-103">執行一或多個工作步驟</span><span class="sxs-lookup"><span data-stu-id="3a765-103">Gets one or more job step executions</span></span>

## <span data-ttu-id="3a765-104">語法</span><span class="sxs-lookup"><span data-stu-id="3a765-104">SYNTAX</span></span>

### <span data-ttu-id="3a765-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3a765-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobStepExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>]
 [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3a765-106">WithJobStepName</span><span class="sxs-lookup"><span data-stu-id="3a765-106">WithJobStepName</span></span>
```
Get-AzSqlElasticJobStepExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> -StepName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3a765-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="3a765-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a765-108">WithJobStepNameUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="3a765-108">WithJobStepNameUsingParentObject</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> -StepName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a765-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3a765-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentResourceId] <String> [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a765-110">WithJobStepNameUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="3a765-110">WithJobStepNameUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentResourceId] <String> -StepName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a765-111">描述</span><span class="sxs-lookup"><span data-stu-id="3a765-111">DESCRIPTION</span></span>
<span data-ttu-id="3a765-112">Cmdlet Get-AzSqlElasticJobStepExecution從工作執行中執行一或多個工作步驟</span><span class="sxs-lookup"><span data-stu-id="3a765-112">The Get-AzSqlElasticJobStepExecution cmdlet gets one or more job step executions from a job execution</span></span>

## <span data-ttu-id="3a765-113">例子</span><span class="sxs-lookup"><span data-stu-id="3a765-113">EXAMPLES</span></span>

### <span data-ttu-id="3a765-114">範例 1 - 從工作執行中執行一或多個工作步驟執行</span><span class="sxs-lookup"><span data-stu-id="3a765-114">Example 1 - Gets one or more job step executions from a job executions</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobStepExecution

JobName JobVersion StepName StepId JobExecutionId                       Lifecycle StartTime            EndTime
------- ---------- -------- ------ --------------                       --------- ---------            -------
job1    1          step1    1      3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

### <span data-ttu-id="3a765-115">範例 2 - 從工作執行中執行一或多個工作步驟，篩選步驟名稱</span><span class="sxs-lookup"><span data-stu-id="3a765-115">Example 2 - Gets one or more job step executions from a job execution, filtering by step name</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobStepExecution -StepName step1

JobName JobVersion StepName StepId JobExecutionId                       Lifecycle StartTime            EndTime
------- ---------- -------- ------ --------------                       --------- ---------            -------
job1    1          step1    1      3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

<span data-ttu-id="3a765-116">執行一或多個工作步驟</span><span class="sxs-lookup"><span data-stu-id="3a765-116">Gets one or more job step executions</span></span>

## <span data-ttu-id="3a765-117">參數</span><span class="sxs-lookup"><span data-stu-id="3a765-117">PARAMETERS</span></span>

### <span data-ttu-id="3a765-118">-使用中</span><span class="sxs-lookup"><span data-stu-id="3a765-118">-Active</span></span>
<span data-ttu-id="3a765-119">標出要根據執行中執行來篩選。</span><span class="sxs-lookup"><span data-stu-id="3a765-119">Flag to filter by active executions.</span></span>

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

### <span data-ttu-id="3a765-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="3a765-120">-AgentName</span></span>
<span data-ttu-id="3a765-121">代理人名稱。</span><span class="sxs-lookup"><span data-stu-id="3a765-121">The agent name.</span></span>

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

### <span data-ttu-id="3a765-122">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="3a765-122">-CreateTimeMax</span></span>
<span data-ttu-id="3a765-123">根據建立時間最大值篩選</span><span class="sxs-lookup"><span data-stu-id="3a765-123">Filter by create time max</span></span>

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

### <span data-ttu-id="3a765-124">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="3a765-124">-CreateTimeMin</span></span>
<span data-ttu-id="3a765-125">根據建立時間分鐘篩選</span><span class="sxs-lookup"><span data-stu-id="3a765-125">Filter by create time min</span></span>

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

### <span data-ttu-id="3a765-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a765-126">-DefaultProfile</span></span>
<span data-ttu-id="3a765-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3a765-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a765-128">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="3a765-128">-EndTimeMax</span></span>
<span data-ttu-id="3a765-129">根據結束時間最大值篩選。</span><span class="sxs-lookup"><span data-stu-id="3a765-129">Filter by end time max.</span></span>

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

### <span data-ttu-id="3a765-130">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="3a765-130">-EndTimeMin</span></span>
<span data-ttu-id="3a765-131">根據結束時間分鐘篩選。</span><span class="sxs-lookup"><span data-stu-id="3a765-131">Filter by end time min.</span></span>

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

### <span data-ttu-id="3a765-132">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="3a765-132">-JobExecutionId</span></span>
<span data-ttu-id="3a765-133">工作執行識別碼。</span><span class="sxs-lookup"><span data-stu-id="3a765-133">The job execution id.</span></span>

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

### <span data-ttu-id="3a765-134">-JobName</span><span class="sxs-lookup"><span data-stu-id="3a765-134">-JobName</span></span>
<span data-ttu-id="3a765-135">工作名稱。</span><span class="sxs-lookup"><span data-stu-id="3a765-135">The job name.</span></span>

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

### <span data-ttu-id="3a765-136">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="3a765-136">-ParentObject</span></span>
<span data-ttu-id="3a765-137">代理程式物件。</span><span class="sxs-lookup"><span data-stu-id="3a765-137">The agent object.</span></span>

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

### <span data-ttu-id="3a765-138">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="3a765-138">-ParentResourceId</span></span>
<span data-ttu-id="3a765-139">工作執行資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="3a765-139">The job execution resource id.</span></span>

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

### <span data-ttu-id="3a765-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a765-140">-ResourceGroupName</span></span>
<span data-ttu-id="3a765-141">資源組名。</span><span class="sxs-lookup"><span data-stu-id="3a765-141">The resource group name.</span></span>

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

### <span data-ttu-id="3a765-142">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3a765-142">-ServerName</span></span>
<span data-ttu-id="3a765-143">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="3a765-143">The server name.</span></span>

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

### <span data-ttu-id="3a765-144">-StepName</span><span class="sxs-lookup"><span data-stu-id="3a765-144">-StepName</span></span>
<span data-ttu-id="3a765-145">工作步驟名稱。</span><span class="sxs-lookup"><span data-stu-id="3a765-145">The job step name.</span></span>

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

### <span data-ttu-id="3a765-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a765-146">CommonParameters</span></span>
<span data-ttu-id="3a765-147">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3a765-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a765-148">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3a765-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a765-149">輸入</span><span class="sxs-lookup"><span data-stu-id="3a765-149">INPUTS</span></span>

### <span data-ttu-id="3a765-150">Microsoft.Azure.Commands.Sql.AzureJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="3a765-150">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="3a765-151">輸出</span><span class="sxs-lookup"><span data-stu-id="3a765-151">OUTPUTS</span></span>

### <span data-ttu-id="3a765-152">Microsoft.Azure.Commands.Sql.AzureJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="3a765-152">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="3a765-153">筆記</span><span class="sxs-lookup"><span data-stu-id="3a765-153">NOTES</span></span>

## <span data-ttu-id="3a765-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="3a765-154">RELATED LINKS</span></span>
