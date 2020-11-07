---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
ms.openlocfilehash: 2c4d0865ba1fb904e367857702d1344f5fb210cc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93799090"
---
# <span data-ttu-id="f88aa-101">Get-AzSqlElasticJobExecution</span><span class="sxs-lookup"><span data-stu-id="f88aa-101">Get-AzSqlElasticJobExecution</span></span>

## <span data-ttu-id="f88aa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f88aa-102">SYNOPSIS</span></span>
<span data-ttu-id="f88aa-103">取得一或多個作業執行</span><span class="sxs-lookup"><span data-stu-id="f88aa-103">Gets one or more job executions</span></span>

## <span data-ttu-id="f88aa-104">句法</span><span class="sxs-lookup"><span data-stu-id="f88aa-104">SYNTAX</span></span>

### <span data-ttu-id="f88aa-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f88aa-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName <String>] [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>]
 [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f88aa-106">WithJobExecutionId</span><span class="sxs-lookup"><span data-stu-id="f88aa-106">WithJobExecutionId</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 -JobName <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f88aa-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="f88aa-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> [-JobName <String>]
 [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>]
 [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f88aa-108">WithJobExecutionIdUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="f88aa-108">WithJobExecutionIdUsingParentObject</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> -JobName <String>
 -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f88aa-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f88aa-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> [-JobName <String>] [-Count] <Int32>
 [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>]
 [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f88aa-110">WithJobExecutionIdUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f88aa-110">WithJobExecutionIdUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> -JobName <String> -JobExecutionId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f88aa-111">說明</span><span class="sxs-lookup"><span data-stu-id="f88aa-111">DESCRIPTION</span></span>
<span data-ttu-id="f88aa-112">Get-AzSqlElasticJobExecution Cmdlet 可取得一或多個作業執行</span><span class="sxs-lookup"><span data-stu-id="f88aa-112">The Get-AzSqlElasticJobExecution cmdlet gets one or more job executions</span></span>

## <span data-ttu-id="f88aa-113">示例</span><span class="sxs-lookup"><span data-stu-id="f88aa-113">EXAMPLES</span></span>

### <span data-ttu-id="f88aa-114">範例 1-在所有工作中取得一或多個作業執行</span><span class="sxs-lookup"><span data-stu-id="f88aa-114">Example 1 - Gets one or more job executions across all jobs</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b Canceled  6/1/2018 10:13:56 PM 6/1/2018 10:13:59 PM
job1    3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:43 PM 6/1/2018 10:11:47 PM
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

### <span data-ttu-id="f88aa-115">範例 2-取得作業的一個或多個作業執行</span><span class="sxs-lookup"><span data-stu-id="f88aa-115">Example 2 - Gets one or more job executions for a job</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3 -JobName job2

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

<span data-ttu-id="f88aa-116">取得一或多個作業執行</span><span class="sxs-lookup"><span data-stu-id="f88aa-116">Gets one or more job executions</span></span>

## <span data-ttu-id="f88aa-117">參數</span><span class="sxs-lookup"><span data-stu-id="f88aa-117">PARAMETERS</span></span>

### <span data-ttu-id="f88aa-118">-使用中</span><span class="sxs-lookup"><span data-stu-id="f88aa-118">-Active</span></span>
<span data-ttu-id="f88aa-119">依建立時間最小值篩選</span><span class="sxs-lookup"><span data-stu-id="f88aa-119">Filter by create time min</span></span>

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

### <span data-ttu-id="f88aa-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="f88aa-120">-AgentName</span></span>
<span data-ttu-id="f88aa-121">[代理程式名稱]。</span><span class="sxs-lookup"><span data-stu-id="f88aa-121">The agent name.</span></span>

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

### <span data-ttu-id="f88aa-122">-Count</span><span class="sxs-lookup"><span data-stu-id="f88aa-122">-Count</span></span>
<span data-ttu-id="f88aa-123">Count 會傳回執行次數的上方。</span><span class="sxs-lookup"><span data-stu-id="f88aa-123">Count returns the top number of executions.</span></span>

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

### <span data-ttu-id="f88aa-124">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="f88aa-124">-CreateTimeMax</span></span>
<span data-ttu-id="f88aa-125">依建立時間最小值篩選</span><span class="sxs-lookup"><span data-stu-id="f88aa-125">Filter by create time min</span></span>

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

### <span data-ttu-id="f88aa-126">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="f88aa-126">-CreateTimeMin</span></span>
<span data-ttu-id="f88aa-127">依建立時間最小值篩選</span><span class="sxs-lookup"><span data-stu-id="f88aa-127">Filter by create time min</span></span>

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

### <span data-ttu-id="f88aa-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f88aa-128">-DefaultProfile</span></span>
<span data-ttu-id="f88aa-129">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f88aa-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f88aa-130">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="f88aa-130">-EndTimeMax</span></span>
<span data-ttu-id="f88aa-131">依建立時間最小值篩選</span><span class="sxs-lookup"><span data-stu-id="f88aa-131">Filter by create time min</span></span>

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

### <span data-ttu-id="f88aa-132">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="f88aa-132">-EndTimeMin</span></span>
<span data-ttu-id="f88aa-133">依建立時間最小值篩選</span><span class="sxs-lookup"><span data-stu-id="f88aa-133">Filter by create time min</span></span>

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

### <span data-ttu-id="f88aa-134">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="f88aa-134">-JobExecutionId</span></span>
<span data-ttu-id="f88aa-135">作業執行 id。</span><span class="sxs-lookup"><span data-stu-id="f88aa-135">The job execution id.</span></span>

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

### <span data-ttu-id="f88aa-136">-JobName</span><span class="sxs-lookup"><span data-stu-id="f88aa-136">-JobName</span></span>
<span data-ttu-id="f88aa-137">作業名稱。</span><span class="sxs-lookup"><span data-stu-id="f88aa-137">The job name.</span></span>

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

### <span data-ttu-id="f88aa-138">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f88aa-138">-ParentObject</span></span>
<span data-ttu-id="f88aa-139">作業執行 id。</span><span class="sxs-lookup"><span data-stu-id="f88aa-139">The job execution id.</span></span>

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

### <span data-ttu-id="f88aa-140">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f88aa-140">-ParentResourceId</span></span>
<span data-ttu-id="f88aa-141">[代理資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="f88aa-141">The agent resource id.</span></span>

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

### <span data-ttu-id="f88aa-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f88aa-142">-ResourceGroupName</span></span>
<span data-ttu-id="f88aa-143">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f88aa-143">The resource group name.</span></span>

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

### <span data-ttu-id="f88aa-144">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f88aa-144">-ServerName</span></span>
<span data-ttu-id="f88aa-145">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="f88aa-145">The server name.</span></span>

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

### <span data-ttu-id="f88aa-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f88aa-146">CommonParameters</span></span>
<span data-ttu-id="f88aa-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f88aa-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f88aa-148">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f88aa-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f88aa-149">輸入</span><span class="sxs-lookup"><span data-stu-id="f88aa-149">INPUTS</span></span>

### <span data-ttu-id="f88aa-150">AzureSqlElasticJobAgentModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="f88aa-150">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="f88aa-151">輸出</span><span class="sxs-lookup"><span data-stu-id="f88aa-151">OUTPUTS</span></span>

### <span data-ttu-id="f88aa-152">AzureSqlElasticJobExecutionModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="f88aa-152">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="f88aa-153">筆記</span><span class="sxs-lookup"><span data-stu-id="f88aa-153">NOTES</span></span>

## <span data-ttu-id="f88aa-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="f88aa-154">RELATED LINKS</span></span>
