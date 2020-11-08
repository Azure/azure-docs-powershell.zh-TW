---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
ms.openlocfilehash: 53bd1b1cd1c2f7ba87df8cb5c27f1b2380db04af
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141037"
---
# <span data-ttu-id="47bd4-101">Set-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="47bd4-101">Set-AzSqlElasticJob</span></span>

## <span data-ttu-id="47bd4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="47bd4-102">SYNOPSIS</span></span>
<span data-ttu-id="47bd4-103">更新作業</span><span class="sxs-lookup"><span data-stu-id="47bd4-103">Updates a job</span></span>

## <span data-ttu-id="47bd4-104">句法</span><span class="sxs-lookup"><span data-stu-id="47bd4-104">SYNTAX</span></span>

### <span data-ttu-id="47bd4-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="47bd4-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47bd4-106">RunOnce</span><span class="sxs-lookup"><span data-stu-id="47bd4-106">RunOnce</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47bd4-107">週期性</span><span class="sxs-lookup"><span data-stu-id="47bd4-107">Recurring</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47bd4-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="47bd4-108">ObjectSet</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="47bd4-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="47bd4-109">RunOnceUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-RunOnce] [-StartTime <DateTime>]
 [-EndTime <DateTime>] [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47bd4-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="47bd4-110">RecurringUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47bd4-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="47bd4-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47bd4-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="47bd4-112">RunOnceUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47bd4-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="47bd4-113">RecurringUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47bd4-114">說明</span><span class="sxs-lookup"><span data-stu-id="47bd4-114">DESCRIPTION</span></span>
<span data-ttu-id="47bd4-115">Set-AzSqlElasticJob Cmdlet 會更新作業</span><span class="sxs-lookup"><span data-stu-id="47bd4-115">The Set-AzSqlElasticJob cmdlet updates a job</span></span>

## <span data-ttu-id="47bd4-116">示例</span><span class="sxs-lookup"><span data-stu-id="47bd4-116">EXAMPLES</span></span>

### <span data-ttu-id="47bd4-117">範例1：更新作業從現在開始一個小時，且每1小時重複一次</span><span class="sxs-lookup"><span data-stu-id="47bd4-117">Example 1: Updates a job to start an hour from now and repeat every 1 hour</span></span>
```powershell
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Set-AzSqlElasticJob -IntervalType Hour -IntervalCount 1 -StartTime (Get-Date).AddHours(1) -Enable

JobName Version Description StartTime            EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------            -------                ------------ -------- -------
job1    0                   6/1/2018 10:50:15 PM 12/31/9999 11:59:59 AM Recurring    PT1H     True
```

<span data-ttu-id="47bd4-118">更新作業</span><span class="sxs-lookup"><span data-stu-id="47bd4-118">Updates a job</span></span>

### <span data-ttu-id="47bd4-119">範例2</span><span class="sxs-lookup"><span data-stu-id="47bd4-119">Example 2</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticJob -AgentName agent -Enable -IntervalCount 1 -IntervalType Hour -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1 -StartTime '9/16/2016 11:31:12'
```

## <span data-ttu-id="47bd4-120">參數</span><span class="sxs-lookup"><span data-stu-id="47bd4-120">PARAMETERS</span></span>

### <span data-ttu-id="47bd4-121">-AgentName</span><span class="sxs-lookup"><span data-stu-id="47bd4-121">-AgentName</span></span>
<span data-ttu-id="47bd4-122">代理程式名稱</span><span class="sxs-lookup"><span data-stu-id="47bd4-122">The agent name</span></span>

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

### <span data-ttu-id="47bd4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47bd4-123">-DefaultProfile</span></span>
<span data-ttu-id="47bd4-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="47bd4-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47bd4-125">-描述</span><span class="sxs-lookup"><span data-stu-id="47bd4-125">-Description</span></span>
<span data-ttu-id="47bd4-126">作業描述</span><span class="sxs-lookup"><span data-stu-id="47bd4-126">The job description</span></span>

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

### <span data-ttu-id="47bd4-127">-啟用</span><span class="sxs-lookup"><span data-stu-id="47bd4-127">-Enable</span></span>
<span data-ttu-id="47bd4-128">指示客戶希望啟用此工作的標誌。</span><span class="sxs-lookup"><span data-stu-id="47bd4-128">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="47bd4-129">-EndTime</span><span class="sxs-lookup"><span data-stu-id="47bd4-129">-EndTime</span></span>
<span data-ttu-id="47bd4-130">作業排程結束時間</span><span class="sxs-lookup"><span data-stu-id="47bd4-130">The job schedule end time</span></span>

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

### <span data-ttu-id="47bd4-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47bd4-131">-InputObject</span></span>
<span data-ttu-id="47bd4-132">作業輸入物件</span><span class="sxs-lookup"><span data-stu-id="47bd4-132">The job input object</span></span>

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

### <span data-ttu-id="47bd4-133">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="47bd4-133">-IntervalCount</span></span>
<span data-ttu-id="47bd4-134">週期性排程間隔計數</span><span class="sxs-lookup"><span data-stu-id="47bd4-134">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="47bd4-135">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="47bd4-135">-IntervalType</span></span>
<span data-ttu-id="47bd4-136">週期性排程間隔類型-可以是分鐘、小時、日、周、月</span><span class="sxs-lookup"><span data-stu-id="47bd4-136">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="47bd4-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="47bd4-137">-Name</span></span>
<span data-ttu-id="47bd4-138">作業名稱</span><span class="sxs-lookup"><span data-stu-id="47bd4-138">The job name</span></span>

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

### <span data-ttu-id="47bd4-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47bd4-139">-ResourceGroupName</span></span>
<span data-ttu-id="47bd4-140">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="47bd4-140">The resource group name</span></span>

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

### <span data-ttu-id="47bd4-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47bd4-141">-ResourceId</span></span>
<span data-ttu-id="47bd4-142">作業資源識別碼</span><span class="sxs-lookup"><span data-stu-id="47bd4-142">The job resource id</span></span>

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

### <span data-ttu-id="47bd4-143">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="47bd4-143">-RunOnce</span></span>
<span data-ttu-id="47bd4-144">指示作業的標誌將會執行一次</span><span class="sxs-lookup"><span data-stu-id="47bd4-144">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="47bd4-145">-ServerName</span><span class="sxs-lookup"><span data-stu-id="47bd4-145">-ServerName</span></span>
<span data-ttu-id="47bd4-146">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="47bd4-146">The server name</span></span>

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

### <span data-ttu-id="47bd4-147">-StartTime</span><span class="sxs-lookup"><span data-stu-id="47bd4-147">-StartTime</span></span>
<span data-ttu-id="47bd4-148">作業排程開始時間</span><span class="sxs-lookup"><span data-stu-id="47bd4-148">The job schedule start time</span></span>

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

### <span data-ttu-id="47bd4-149">-確認</span><span class="sxs-lookup"><span data-stu-id="47bd4-149">-Confirm</span></span>
<span data-ttu-id="47bd4-150">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="47bd4-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47bd4-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47bd4-151">-WhatIf</span></span>
<span data-ttu-id="47bd4-152">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="47bd4-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47bd4-153">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="47bd4-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47bd4-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47bd4-154">CommonParameters</span></span>
<span data-ttu-id="47bd4-155">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="47bd4-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47bd4-156">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="47bd4-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47bd4-157">輸入</span><span class="sxs-lookup"><span data-stu-id="47bd4-157">INPUTS</span></span>

### <span data-ttu-id="47bd4-158">AzureSqlElasticJobModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="47bd4-158">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="47bd4-159">輸出</span><span class="sxs-lookup"><span data-stu-id="47bd4-159">OUTPUTS</span></span>

### <span data-ttu-id="47bd4-160">AzureSqlElasticJobModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="47bd4-160">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="47bd4-161">筆記</span><span class="sxs-lookup"><span data-stu-id="47bd4-161">NOTES</span></span>

## <span data-ttu-id="47bd4-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="47bd4-162">RELATED LINKS</span></span>