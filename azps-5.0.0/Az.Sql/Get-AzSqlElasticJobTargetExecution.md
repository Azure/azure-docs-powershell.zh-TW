---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobtargetexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetExecution.md
ms.openlocfilehash: 6e61a83d843e0ceaa7d7926060da848d80d16eae
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285775"
---
# <span data-ttu-id="53f62-101">Get-AzSqlElasticJobTargetExecution</span><span class="sxs-lookup"><span data-stu-id="53f62-101">Get-AzSqlElasticJobTargetExecution</span></span>

## <span data-ttu-id="53f62-102">摘要</span><span class="sxs-lookup"><span data-stu-id="53f62-102">SYNOPSIS</span></span>
<span data-ttu-id="53f62-103">取得一或多個作業目標執行</span><span class="sxs-lookup"><span data-stu-id="53f62-103">Gets one or more job target executions</span></span>

## <span data-ttu-id="53f62-104">句法</span><span class="sxs-lookup"><span data-stu-id="53f62-104">SYNTAX</span></span>

### <span data-ttu-id="53f62-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="53f62-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobTargetExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> -Count <Int32> [-StepName <String>] [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53f62-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="53f62-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobTargetExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> -Count <Int32>
 [-StepName <String>] [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>]
 [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53f62-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="53f62-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobTargetExecution [-ParentResourceId] <String> -Count <Int32> [-StepName <String>]
 [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>]
 [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53f62-108">說明</span><span class="sxs-lookup"><span data-stu-id="53f62-108">DESCRIPTION</span></span>
<span data-ttu-id="53f62-109">Get-AzSqlElasticJobTargetExecution Cmdlet 會從作業執行中取得一或多個作業目標執行</span><span class="sxs-lookup"><span data-stu-id="53f62-109">The Get-AzSqlElasticJobTargetExecution cmdlet gets one or more job target executions from a job execution</span></span>

## <span data-ttu-id="53f62-110">示例</span><span class="sxs-lookup"><span data-stu-id="53f62-110">EXAMPLES</span></span>

### <span data-ttu-id="53f62-111">範例1：從作業執行中取得一或多個作業目標執行</span><span class="sxs-lookup"><span data-stu-id="53f62-111">Example 1: Gets one or more job target executions from a job executions</span></span>
```powershell
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobTargetExecution -Count 2
JobName JobVersion StepName StepId JobExecutionId                       Lifecycle       TargetServerName TargetDatabaseName StartTime            EndTime
------- ---------- -------- ------ --------------                       ---------       ---------------- ------------------ ---------            -------
job1    1          step2    1      ea0a870b-dfe3-427e-9f95-d229d7815b65 Succeeded       s1               db2                6/1/2018 10:11:47 PM 6/1/2018 10:11:50 PM
job1    1          step1    1      ea0a870b-dfe3-427e-9f95-d229d7815b65 Succeeded       s1               db1                6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

### <span data-ttu-id="53f62-112">範例2：從作業執行中取得一或多個作業目標執行-依步驟名稱篩選</span><span class="sxs-lookup"><span data-stu-id="53f62-112">Example 2: Gets one or more job target executions from a job executions - filtering by step name</span></span>
```powershell
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobTargetExecution -Count 2 -StepName step2
JobName JobVersion StepName StepId JobExecutionId                       Lifecycle       TargetServerName TargetDatabaseName StartTime            EndTime
------- ---------- -------- ------ --------------                       ---------       ---------------- ------------------ ---------            -------
job1    1          step2    1      ea0a870b-dfe3-427e-9f95-d229d7815b65 Succeeded       s1               db2                6/1/2018 10:11:47 PM 6/1/2018 10:11:50 PM
```

<span data-ttu-id="53f62-113">取得一或多個作業目標執行</span><span class="sxs-lookup"><span data-stu-id="53f62-113">Gets one or more job target executions</span></span>

## <span data-ttu-id="53f62-114">參數</span><span class="sxs-lookup"><span data-stu-id="53f62-114">PARAMETERS</span></span>

### <span data-ttu-id="53f62-115">-使用中</span><span class="sxs-lookup"><span data-stu-id="53f62-115">-Active</span></span>
<span data-ttu-id="53f62-116">[旗標]：依作用中的執行進行篩選。</span><span class="sxs-lookup"><span data-stu-id="53f62-116">Flag to filter by active executions.</span></span>

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

### <span data-ttu-id="53f62-117">-AgentName</span><span class="sxs-lookup"><span data-stu-id="53f62-117">-AgentName</span></span>
<span data-ttu-id="53f62-118">[代理程式名稱]。</span><span class="sxs-lookup"><span data-stu-id="53f62-118">The agent name.</span></span>

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

### <span data-ttu-id="53f62-119">-Count</span><span class="sxs-lookup"><span data-stu-id="53f62-119">-Count</span></span>
<span data-ttu-id="53f62-120">Count 會傳回執行次數的上方。</span><span class="sxs-lookup"><span data-stu-id="53f62-120">Count returns the top number of executions.</span></span>

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

### <span data-ttu-id="53f62-121">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="53f62-121">-CreateTimeMax</span></span>
<span data-ttu-id="53f62-122">依建立時間上限來篩選</span><span class="sxs-lookup"><span data-stu-id="53f62-122">Filter by create time max</span></span>

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

### <span data-ttu-id="53f62-123">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="53f62-123">-CreateTimeMin</span></span>
<span data-ttu-id="53f62-124">依建立時間最小值篩選</span><span class="sxs-lookup"><span data-stu-id="53f62-124">Filter by create time min</span></span>

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

### <span data-ttu-id="53f62-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53f62-125">-DefaultProfile</span></span>
<span data-ttu-id="53f62-126">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="53f62-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53f62-127">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="53f62-127">-EndTimeMax</span></span>
<span data-ttu-id="53f62-128">依 [結束時間上限] 篩選。</span><span class="sxs-lookup"><span data-stu-id="53f62-128">Filter by end time max.</span></span>

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

### <span data-ttu-id="53f62-129">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="53f62-129">-EndTimeMin</span></span>
<span data-ttu-id="53f62-130">依 [最小結束時間] 篩選。</span><span class="sxs-lookup"><span data-stu-id="53f62-130">Filter by end time min.</span></span>

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

### <span data-ttu-id="53f62-131">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="53f62-131">-JobExecutionId</span></span>
<span data-ttu-id="53f62-132">作業執行 id。</span><span class="sxs-lookup"><span data-stu-id="53f62-132">The job execution id.</span></span>

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

### <span data-ttu-id="53f62-133">-JobName</span><span class="sxs-lookup"><span data-stu-id="53f62-133">-JobName</span></span>
<span data-ttu-id="53f62-134">作業名稱。</span><span class="sxs-lookup"><span data-stu-id="53f62-134">The job name.</span></span>

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

### <span data-ttu-id="53f62-135">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="53f62-135">-ParentObject</span></span>
<span data-ttu-id="53f62-136">作業執行物件。</span><span class="sxs-lookup"><span data-stu-id="53f62-136">The job execution object.</span></span>

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

### <span data-ttu-id="53f62-137">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="53f62-137">-ParentResourceId</span></span>
<span data-ttu-id="53f62-138">作業執行資源 id。</span><span class="sxs-lookup"><span data-stu-id="53f62-138">The job execution resource id.</span></span>

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

### <span data-ttu-id="53f62-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53f62-139">-ResourceGroupName</span></span>
<span data-ttu-id="53f62-140">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="53f62-140">The resource group name.</span></span>

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

### <span data-ttu-id="53f62-141">-ServerName</span><span class="sxs-lookup"><span data-stu-id="53f62-141">-ServerName</span></span>
<span data-ttu-id="53f62-142">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="53f62-142">The server name.</span></span>

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

### <span data-ttu-id="53f62-143">-StepName</span><span class="sxs-lookup"><span data-stu-id="53f62-143">-StepName</span></span>
<span data-ttu-id="53f62-144">作業步驟名稱。</span><span class="sxs-lookup"><span data-stu-id="53f62-144">The job step name.</span></span>

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

### <span data-ttu-id="53f62-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53f62-145">CommonParameters</span></span>
<span data-ttu-id="53f62-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="53f62-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53f62-147">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="53f62-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53f62-148">輸入</span><span class="sxs-lookup"><span data-stu-id="53f62-148">INPUTS</span></span>

### <span data-ttu-id="53f62-149">AzureSqlElasticJobExecutionModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="53f62-149">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="53f62-150">輸出</span><span class="sxs-lookup"><span data-stu-id="53f62-150">OUTPUTS</span></span>

### <span data-ttu-id="53f62-151">AzureSqlElasticJobExecutionModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="53f62-151">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="53f62-152">筆記</span><span class="sxs-lookup"><span data-stu-id="53f62-152">NOTES</span></span>

## <span data-ttu-id="53f62-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="53f62-153">RELATED LINKS</span></span>
