---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobtargetexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetExecution.md
ms.openlocfilehash: 566bfb8caae85c6f4e6ef75a38bdd5363ddb1eaa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93799077"
---
# <span data-ttu-id="13ff6-101">Get-AzSqlElasticJobTargetExecution</span><span class="sxs-lookup"><span data-stu-id="13ff6-101">Get-AzSqlElasticJobTargetExecution</span></span>

## <span data-ttu-id="13ff6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="13ff6-102">SYNOPSIS</span></span>
<span data-ttu-id="13ff6-103">取得一或多個作業目標執行</span><span class="sxs-lookup"><span data-stu-id="13ff6-103">Gets one or more job target executions</span></span>

## <span data-ttu-id="13ff6-104">句法</span><span class="sxs-lookup"><span data-stu-id="13ff6-104">SYNTAX</span></span>

### <span data-ttu-id="13ff6-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="13ff6-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobTargetExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> -Count <Int32> [-StepName <String>] [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13ff6-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="13ff6-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobTargetExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> -Count <Int32>
 [-StepName <String>] [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>]
 [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13ff6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="13ff6-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobTargetExecution [-ParentResourceId] <String> -Count <Int32> [-StepName <String>]
 [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>]
 [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13ff6-108">說明</span><span class="sxs-lookup"><span data-stu-id="13ff6-108">DESCRIPTION</span></span>
<span data-ttu-id="13ff6-109">Get-AzSqlElasticJobTargetExecution Cmdlet 會從作業執行中取得一或多個作業目標執行</span><span class="sxs-lookup"><span data-stu-id="13ff6-109">The Get-AzSqlElasticJobTargetExecution cmdlet gets one or more job target executions from a job execution</span></span>

## <span data-ttu-id="13ff6-110">示例</span><span class="sxs-lookup"><span data-stu-id="13ff6-110">EXAMPLES</span></span>

### <span data-ttu-id="13ff6-111">範例 1-從作業執行中取得一或多個作業目標執行</span><span class="sxs-lookup"><span data-stu-id="13ff6-111">Example 1 - Gets one or more job target executions from a job executions</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobTargetExecution -Count 2
JobName JobVersion StepName StepId JobExecutionId                       Lifecycle       TargetServerName TargetDatabaseName StartTime            EndTime
------- ---------- -------- ------ --------------                       ---------       ---------------- ------------------ ---------            -------
job1    1          step2    1      ea0a870b-dfe3-427e-9f95-d229d7815b65 Succeeded       s1               db2                6/1/2018 10:11:47 PM 6/1/2018 10:11:50 PM
job1    1          step1    1      ea0a870b-dfe3-427e-9f95-d229d7815b65 Succeeded       s1               db1                6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

### <span data-ttu-id="13ff6-112">範例 2-從作業執行中取得一或多個作業目標執行-依步驟名稱篩選</span><span class="sxs-lookup"><span data-stu-id="13ff6-112">Example 2 - Gets one or more job target executions from a job executions - filtering by step name</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobTargetExecution -Count 2 -StepName step2
JobName JobVersion StepName StepId JobExecutionId                       Lifecycle       TargetServerName TargetDatabaseName StartTime            EndTime
------- ---------- -------- ------ --------------                       ---------       ---------------- ------------------ ---------            -------
job1    1          step2    1      ea0a870b-dfe3-427e-9f95-d229d7815b65 Succeeded       s1               db2                6/1/2018 10:11:47 PM 6/1/2018 10:11:50 PM
```

<span data-ttu-id="13ff6-113">取得一或多個作業目標執行</span><span class="sxs-lookup"><span data-stu-id="13ff6-113">Gets one or more job target executions</span></span>

## <span data-ttu-id="13ff6-114">參數</span><span class="sxs-lookup"><span data-stu-id="13ff6-114">PARAMETERS</span></span>

### <span data-ttu-id="13ff6-115">-使用中</span><span class="sxs-lookup"><span data-stu-id="13ff6-115">-Active</span></span>
<span data-ttu-id="13ff6-116">[旗標]：依作用中的執行進行篩選。</span><span class="sxs-lookup"><span data-stu-id="13ff6-116">Flag to filter by active executions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13ff6-117">-AgentName</span><span class="sxs-lookup"><span data-stu-id="13ff6-117">-AgentName</span></span>
<span data-ttu-id="13ff6-118">[代理程式名稱]。</span><span class="sxs-lookup"><span data-stu-id="13ff6-118">The agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13ff6-119">-Count</span><span class="sxs-lookup"><span data-stu-id="13ff6-119">-Count</span></span>
<span data-ttu-id="13ff6-120">Count 會傳回執行次數的上方。</span><span class="sxs-lookup"><span data-stu-id="13ff6-120">Count returns the top number of executions.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13ff6-121">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="13ff6-121">-CreateTimeMax</span></span>
<span data-ttu-id="13ff6-122">依建立時間上限來篩選</span><span class="sxs-lookup"><span data-stu-id="13ff6-122">Filter by create time max</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13ff6-123">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="13ff6-123">-CreateTimeMin</span></span>
<span data-ttu-id="13ff6-124">依建立時間最小值篩選</span><span class="sxs-lookup"><span data-stu-id="13ff6-124">Filter by create time min</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13ff6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13ff6-125">-DefaultProfile</span></span>
<span data-ttu-id="13ff6-126">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="13ff6-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13ff6-127">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="13ff6-127">-EndTimeMax</span></span>
<span data-ttu-id="13ff6-128">依 [結束時間上限] 篩選。</span><span class="sxs-lookup"><span data-stu-id="13ff6-128">Filter by end time max.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13ff6-129">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="13ff6-129">-EndTimeMin</span></span>
<span data-ttu-id="13ff6-130">依 [最小結束時間] 篩選。</span><span class="sxs-lookup"><span data-stu-id="13ff6-130">Filter by end time min.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13ff6-131">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="13ff6-131">-JobExecutionId</span></span>
<span data-ttu-id="13ff6-132">作業執行 id。</span><span class="sxs-lookup"><span data-stu-id="13ff6-132">The job execution id.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13ff6-133">-JobName</span><span class="sxs-lookup"><span data-stu-id="13ff6-133">-JobName</span></span>
<span data-ttu-id="13ff6-134">作業名稱。</span><span class="sxs-lookup"><span data-stu-id="13ff6-134">The job name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13ff6-135">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="13ff6-135">-ParentObject</span></span>
<span data-ttu-id="13ff6-136">作業執行物件。</span><span class="sxs-lookup"><span data-stu-id="13ff6-136">The job execution object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13ff6-137">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="13ff6-137">-ParentResourceId</span></span>
<span data-ttu-id="13ff6-138">作業執行資源 id。</span><span class="sxs-lookup"><span data-stu-id="13ff6-138">The job execution resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13ff6-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13ff6-139">-ResourceGroupName</span></span>
<span data-ttu-id="13ff6-140">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="13ff6-140">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13ff6-141">-ServerName</span><span class="sxs-lookup"><span data-stu-id="13ff6-141">-ServerName</span></span>
<span data-ttu-id="13ff6-142">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="13ff6-142">The server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13ff6-143">-StepName</span><span class="sxs-lookup"><span data-stu-id="13ff6-143">-StepName</span></span>
<span data-ttu-id="13ff6-144">作業步驟名稱。</span><span class="sxs-lookup"><span data-stu-id="13ff6-144">The job step name.</span></span>

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

### <span data-ttu-id="13ff6-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13ff6-145">CommonParameters</span></span>
<span data-ttu-id="13ff6-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="13ff6-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13ff6-147">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="13ff6-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13ff6-148">輸入</span><span class="sxs-lookup"><span data-stu-id="13ff6-148">INPUTS</span></span>

### <span data-ttu-id="13ff6-149">AzureSqlElasticJobExecutionModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="13ff6-149">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="13ff6-150">輸出</span><span class="sxs-lookup"><span data-stu-id="13ff6-150">OUTPUTS</span></span>

### <span data-ttu-id="13ff6-151">AzureSqlElasticJobExecutionModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="13ff6-151">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="13ff6-152">筆記</span><span class="sxs-lookup"><span data-stu-id="13ff6-152">NOTES</span></span>

## <span data-ttu-id="13ff6-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="13ff6-153">RELATED LINKS</span></span>
