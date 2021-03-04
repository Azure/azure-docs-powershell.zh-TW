---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/set-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
ms.openlocfilehash: 9daa42e00d23af96d630795abcc88dbeaceacaff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915194"
---
# <span data-ttu-id="7ee32-101">Set-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="7ee32-101">Set-AzSqlElasticJob</span></span>

## <span data-ttu-id="7ee32-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7ee32-102">SYNOPSIS</span></span>
<span data-ttu-id="7ee32-103">更新工作</span><span class="sxs-lookup"><span data-stu-id="7ee32-103">Updates a job</span></span>

## <span data-ttu-id="7ee32-104">語法</span><span class="sxs-lookup"><span data-stu-id="7ee32-104">SYNTAX</span></span>

### <span data-ttu-id="7ee32-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7ee32-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ee32-106">RunOnce</span><span class="sxs-lookup"><span data-stu-id="7ee32-106">RunOnce</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ee32-107">經常性</span><span class="sxs-lookup"><span data-stu-id="7ee32-107">Recurring</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ee32-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="7ee32-108">ObjectSet</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7ee32-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="7ee32-109">RunOnceUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-RunOnce] [-StartTime <DateTime>]
 [-EndTime <DateTime>] [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ee32-110">週期性UsingParentObject</span><span class="sxs-lookup"><span data-stu-id="7ee32-110">RecurringUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ee32-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7ee32-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ee32-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="7ee32-112">RunOnceUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ee32-113">週期性UsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="7ee32-113">RecurringUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ee32-114">描述</span><span class="sxs-lookup"><span data-stu-id="7ee32-114">DESCRIPTION</span></span>
<span data-ttu-id="7ee32-115">Cmdlet Set-AzSqlElasticJob更新工作</span><span class="sxs-lookup"><span data-stu-id="7ee32-115">The Set-AzSqlElasticJob cmdlet updates a job</span></span>

## <span data-ttu-id="7ee32-116">例子</span><span class="sxs-lookup"><span data-stu-id="7ee32-116">EXAMPLES</span></span>

### <span data-ttu-id="7ee32-117">範例 1：更新工作以從現在開始開始一小時，並每隔 1 小時重複</span><span class="sxs-lookup"><span data-stu-id="7ee32-117">Example 1: Updates a job to start an hour from now and repeat every 1 hour</span></span>
```powershell
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Set-AzSqlElasticJob -IntervalType Hour -IntervalCount 1 -StartTime (Get-Date).AddHours(1) -Enable

JobName Version Description StartTime            EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------            -------                ------------ -------- -------
job1    0                   6/1/2018 10:50:15 PM 12/31/9999 11:59:59 AM Recurring    PT1H     True
```

<span data-ttu-id="7ee32-118">更新工作</span><span class="sxs-lookup"><span data-stu-id="7ee32-118">Updates a job</span></span>

### <span data-ttu-id="7ee32-119">範例 2</span><span class="sxs-lookup"><span data-stu-id="7ee32-119">Example 2</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticJob -AgentName agent -Enable -IntervalCount 1 -IntervalType Hour -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1 -StartTime '9/16/2016 11:31:12'
```

## <span data-ttu-id="7ee32-120">參數</span><span class="sxs-lookup"><span data-stu-id="7ee32-120">PARAMETERS</span></span>

### <span data-ttu-id="7ee32-121">-AgentName</span><span class="sxs-lookup"><span data-stu-id="7ee32-121">-AgentName</span></span>
<span data-ttu-id="7ee32-122">代理人名稱</span><span class="sxs-lookup"><span data-stu-id="7ee32-122">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, RunOnce, Recurring
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ee32-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ee32-123">-DefaultProfile</span></span>
<span data-ttu-id="7ee32-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7ee32-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ee32-125">-描述</span><span class="sxs-lookup"><span data-stu-id="7ee32-125">-Description</span></span>
<span data-ttu-id="7ee32-126">工作描述</span><span class="sxs-lookup"><span data-stu-id="7ee32-126">The job description</span></span>

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

### <span data-ttu-id="7ee32-127">-啟用</span><span class="sxs-lookup"><span data-stu-id="7ee32-127">-Enable</span></span>
<span data-ttu-id="7ee32-128">指出客戶想要啟用此工作的標標。</span><span class="sxs-lookup"><span data-stu-id="7ee32-128">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="7ee32-129">-EndTime</span><span class="sxs-lookup"><span data-stu-id="7ee32-129">-EndTime</span></span>
<span data-ttu-id="7ee32-130">工作排程結束時間</span><span class="sxs-lookup"><span data-stu-id="7ee32-130">The job schedule end time</span></span>

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

### <span data-ttu-id="7ee32-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7ee32-131">-InputObject</span></span>
<span data-ttu-id="7ee32-132">工作輸入物件</span><span class="sxs-lookup"><span data-stu-id="7ee32-132">The job input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet, RunOnceUsingParentObject, RecurringUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ee32-133">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="7ee32-133">-IntervalCount</span></span>
<span data-ttu-id="7ee32-134">週期性排程間隔計數</span><span class="sxs-lookup"><span data-stu-id="7ee32-134">The recurring schedule interval count</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: Recurring, RecurringUsingParentObject, RecurringUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ee32-135">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="7ee32-135">-IntervalType</span></span>
<span data-ttu-id="7ee32-136">週期性排程間隔類型 - 可以是分鐘、小時、日、周、月</span><span class="sxs-lookup"><span data-stu-id="7ee32-136">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

```yaml
Type: System.String
Parameter Sets: Recurring, RecurringUsingParentObject, RecurringUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ee32-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="7ee32-137">-Name</span></span>
<span data-ttu-id="7ee32-138">工作名稱</span><span class="sxs-lookup"><span data-stu-id="7ee32-138">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, RunOnce, Recurring
Aliases: JobName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ee32-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ee32-139">-ResourceGroupName</span></span>
<span data-ttu-id="7ee32-140">資源組名</span><span class="sxs-lookup"><span data-stu-id="7ee32-140">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, RunOnce, Recurring
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ee32-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7ee32-141">-ResourceId</span></span>
<span data-ttu-id="7ee32-142">工作資源識別碼</span><span class="sxs-lookup"><span data-stu-id="7ee32-142">The job resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, RunOnceUsingParentResourceId, RecurringUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ee32-143">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="7ee32-143">-RunOnce</span></span>
<span data-ttu-id="7ee32-144">指出工作的標號將會執行一次</span><span class="sxs-lookup"><span data-stu-id="7ee32-144">The flag to indicate job will be run once</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RunOnce, RunOnceUsingParentObject, RunOnceUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ee32-145">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7ee32-145">-ServerName</span></span>
<span data-ttu-id="7ee32-146">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="7ee32-146">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, RunOnce, Recurring
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ee32-147">-StartTime</span><span class="sxs-lookup"><span data-stu-id="7ee32-147">-StartTime</span></span>
<span data-ttu-id="7ee32-148">工作排程開始時間</span><span class="sxs-lookup"><span data-stu-id="7ee32-148">The job schedule start time</span></span>

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

### <span data-ttu-id="7ee32-149">-確認</span><span class="sxs-lookup"><span data-stu-id="7ee32-149">-Confirm</span></span>
<span data-ttu-id="7ee32-150">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7ee32-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ee32-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ee32-151">-WhatIf</span></span>
<span data-ttu-id="7ee32-152">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7ee32-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ee32-153">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7ee32-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ee32-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ee32-154">CommonParameters</span></span>
<span data-ttu-id="7ee32-155">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7ee32-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ee32-156">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7ee32-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ee32-157">輸入</span><span class="sxs-lookup"><span data-stu-id="7ee32-157">INPUTS</span></span>

### <span data-ttu-id="7ee32-158">Microsoft.Azure.Commands.Sql.AzureJobs.Model.AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="7ee32-158">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="7ee32-159">輸出</span><span class="sxs-lookup"><span data-stu-id="7ee32-159">OUTPUTS</span></span>

### <span data-ttu-id="7ee32-160">Microsoft.Azure.Commands.Sql.AzureJobs.Model.AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="7ee32-160">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="7ee32-161">筆記</span><span class="sxs-lookup"><span data-stu-id="7ee32-161">NOTES</span></span>

## <span data-ttu-id="7ee32-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="7ee32-162">RELATED LINKS</span></span>
