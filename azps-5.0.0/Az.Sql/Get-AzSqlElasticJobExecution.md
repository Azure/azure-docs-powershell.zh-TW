---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
ms.openlocfilehash: d5583e5d7c0984b36679517859cc5a109b808a1a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137285"
---
# <span data-ttu-id="06097-101">Get-AzSqlElasticJobExecution</span><span class="sxs-lookup"><span data-stu-id="06097-101">Get-AzSqlElasticJobExecution</span></span>

## <span data-ttu-id="06097-102">摘要</span><span class="sxs-lookup"><span data-stu-id="06097-102">SYNOPSIS</span></span>
<span data-ttu-id="06097-103">取得一或多個作業執行</span><span class="sxs-lookup"><span data-stu-id="06097-103">Gets one or more job executions</span></span>

## <span data-ttu-id="06097-104">句法</span><span class="sxs-lookup"><span data-stu-id="06097-104">SYNTAX</span></span>

### <span data-ttu-id="06097-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="06097-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName <String>] [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>]
 [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="06097-106">WithJobExecutionId</span><span class="sxs-lookup"><span data-stu-id="06097-106">WithJobExecutionId</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 -JobName <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06097-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="06097-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> [-JobName <String>]
 [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>]
 [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06097-108">WithJobExecutionIdUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="06097-108">WithJobExecutionIdUsingParentObject</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> -JobName <String>
 -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06097-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="06097-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> [-JobName <String>] [-Count] <Int32>
 [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>]
 [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06097-110">WithJobExecutionIdUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="06097-110">WithJobExecutionIdUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> -JobName <String> -JobExecutionId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06097-111">說明</span><span class="sxs-lookup"><span data-stu-id="06097-111">DESCRIPTION</span></span>
<span data-ttu-id="06097-112">Get-AzSqlElasticJobExecution Cmdlet 可取得一或多個作業執行</span><span class="sxs-lookup"><span data-stu-id="06097-112">The Get-AzSqlElasticJobExecution cmdlet gets one or more job executions</span></span>

## <span data-ttu-id="06097-113">示例</span><span class="sxs-lookup"><span data-stu-id="06097-113">EXAMPLES</span></span>

### <span data-ttu-id="06097-114">範例1：在所有工作中取得一或多個作業執行</span><span class="sxs-lookup"><span data-stu-id="06097-114">Example 1: Gets one or more job executions across all jobs</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b Canceled  6/1/2018 10:13:56 PM 6/1/2018 10:13:59 PM
job1    3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:43 PM 6/1/2018 10:11:47 PM
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

### <span data-ttu-id="06097-115">範例2：取得作業的一個或多個作業執行</span><span class="sxs-lookup"><span data-stu-id="06097-115">Example 2: Gets one or more job executions for a job</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3 -JobName job2

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

<span data-ttu-id="06097-116">取得一或多個作業執行</span><span class="sxs-lookup"><span data-stu-id="06097-116">Gets one or more job executions</span></span>

### <span data-ttu-id="06097-117">範例3</span><span class="sxs-lookup"><span data-stu-id="06097-117">Example 3</span></span>

<span data-ttu-id="06097-118">取得一或多個工作執行。</span><span class="sxs-lookup"><span data-stu-id="06097-118">Gets one or more job executions.</span></span> <span data-ttu-id="06097-119"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="06097-119">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Get-AzSqlElasticJobExecution -JobExecutionId 00000000-0000-0000-0000-000000000000 -JobName job1
```

## <span data-ttu-id="06097-120">參數</span><span class="sxs-lookup"><span data-stu-id="06097-120">PARAMETERS</span></span>

### <span data-ttu-id="06097-121">-使用中</span><span class="sxs-lookup"><span data-stu-id="06097-121">-Active</span></span>
<span data-ttu-id="06097-122">依建立時間最小值篩選</span><span class="sxs-lookup"><span data-stu-id="06097-122">Filter by create time min</span></span>

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

### <span data-ttu-id="06097-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="06097-123">-AgentName</span></span>
<span data-ttu-id="06097-124">[代理程式名稱]。</span><span class="sxs-lookup"><span data-stu-id="06097-124">The agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobExecutionId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06097-125">-Count</span><span class="sxs-lookup"><span data-stu-id="06097-125">-Count</span></span>
<span data-ttu-id="06097-126">Count 會傳回執行次數的上方。</span><span class="sxs-lookup"><span data-stu-id="06097-126">Count returns the top number of executions.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06097-127">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="06097-127">-CreateTimeMax</span></span>
<span data-ttu-id="06097-128">依建立時間最小值篩選</span><span class="sxs-lookup"><span data-stu-id="06097-128">Filter by create time min</span></span>

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

### <span data-ttu-id="06097-129">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="06097-129">-CreateTimeMin</span></span>
<span data-ttu-id="06097-130">依建立時間最小值篩選</span><span class="sxs-lookup"><span data-stu-id="06097-130">Filter by create time min</span></span>

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

### <span data-ttu-id="06097-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06097-131">-DefaultProfile</span></span>
<span data-ttu-id="06097-132">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="06097-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06097-133">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="06097-133">-EndTimeMax</span></span>
<span data-ttu-id="06097-134">依建立時間最小值篩選</span><span class="sxs-lookup"><span data-stu-id="06097-134">Filter by create time min</span></span>

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

### <span data-ttu-id="06097-135">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="06097-135">-EndTimeMin</span></span>
<span data-ttu-id="06097-136">依建立時間最小值篩選</span><span class="sxs-lookup"><span data-stu-id="06097-136">Filter by create time min</span></span>

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

### <span data-ttu-id="06097-137">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="06097-137">-JobExecutionId</span></span>
<span data-ttu-id="06097-138">作業執行 id。</span><span class="sxs-lookup"><span data-stu-id="06097-138">The job execution id.</span></span>

```yaml
Type: System.String
Parameter Sets: WithJobExecutionId, WithJobExecutionIdUsingParentObject, WithJobExecutionIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06097-139">-JobName</span><span class="sxs-lookup"><span data-stu-id="06097-139">-JobName</span></span>
<span data-ttu-id="06097-140">作業名稱。</span><span class="sxs-lookup"><span data-stu-id="06097-140">The job name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WithJobExecutionId, WithJobExecutionIdUsingParentObject, WithJobExecutionIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06097-141">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="06097-141">-ParentObject</span></span>
<span data-ttu-id="06097-142">作業執行 id。</span><span class="sxs-lookup"><span data-stu-id="06097-142">The job execution id.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel
Parameter Sets: ObjectSet, WithJobExecutionIdUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06097-143">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="06097-143">-ParentResourceId</span></span>
<span data-ttu-id="06097-144">[代理資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="06097-144">The agent resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, WithJobExecutionIdUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06097-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06097-145">-ResourceGroupName</span></span>
<span data-ttu-id="06097-146">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="06097-146">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobExecutionId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06097-147">-ServerName</span><span class="sxs-lookup"><span data-stu-id="06097-147">-ServerName</span></span>
<span data-ttu-id="06097-148">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="06097-148">The server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobExecutionId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06097-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06097-149">CommonParameters</span></span>
<span data-ttu-id="06097-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="06097-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06097-151">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="06097-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06097-152">輸入</span><span class="sxs-lookup"><span data-stu-id="06097-152">INPUTS</span></span>

### <span data-ttu-id="06097-153">AzureSqlElasticJobAgentModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="06097-153">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="06097-154">輸出</span><span class="sxs-lookup"><span data-stu-id="06097-154">OUTPUTS</span></span>

### <span data-ttu-id="06097-155">AzureSqlElasticJobExecutionModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="06097-155">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="06097-156">筆記</span><span class="sxs-lookup"><span data-stu-id="06097-156">NOTES</span></span>

## <span data-ttu-id="06097-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="06097-157">RELATED LINKS</span></span>