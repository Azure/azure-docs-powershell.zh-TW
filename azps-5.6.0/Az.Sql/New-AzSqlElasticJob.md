---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
ms.openlocfilehash: 961f37db94cff87952b2811a528a94cc71ffabff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916696"
---
# <span data-ttu-id="08f2d-101">New-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="08f2d-101">New-AzSqlElasticJob</span></span>

## <span data-ttu-id="08f2d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="08f2d-102">SYNOPSIS</span></span>
<span data-ttu-id="08f2d-103">建立新工作</span><span class="sxs-lookup"><span data-stu-id="08f2d-103">Creates a new job</span></span>

## <span data-ttu-id="08f2d-104">語法</span><span class="sxs-lookup"><span data-stu-id="08f2d-104">SYNTAX</span></span>

### <span data-ttu-id="08f2d-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="08f2d-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="08f2d-106">RunOnce</span><span class="sxs-lookup"><span data-stu-id="08f2d-106">RunOnce</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08f2d-107">經常性</span><span class="sxs-lookup"><span data-stu-id="08f2d-107">Recurring</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="08f2d-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="08f2d-108">ObjectSet</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-Description <String>]
 [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08f2d-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="08f2d-109">RunOnceUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-RunOnce]
 [-StartTime <DateTime>] [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08f2d-110">週期性UsingParentObject</span><span class="sxs-lookup"><span data-stu-id="08f2d-110">RecurringUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08f2d-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="08f2d-111">ResourceIdSet</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08f2d-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="08f2d-112">RunOnceUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-RunOnce] [-StartTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="08f2d-113">週期性UsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="08f2d-113">RecurringUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08f2d-114">描述</span><span class="sxs-lookup"><span data-stu-id="08f2d-114">DESCRIPTION</span></span>
<span data-ttu-id="08f2d-115">Cmdlet New-AzSqlElasticJob建立新工作</span><span class="sxs-lookup"><span data-stu-id="08f2d-115">The New-AzSqlElasticJob cmdlet creates a new job</span></span>

## <span data-ttu-id="08f2d-116">例子</span><span class="sxs-lookup"><span data-stu-id="08f2d-116">EXAMPLES</span></span>

### <span data-ttu-id="08f2d-117">範例 1：建立新工作</span><span class="sxs-lookup"><span data-stu-id="08f2d-117">Example 1: Creates a new job</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="08f2d-118">建立新工作</span><span class="sxs-lookup"><span data-stu-id="08f2d-118">Creates a new job</span></span>

### <span data-ttu-id="08f2d-119">範例 2</span><span class="sxs-lookup"><span data-stu-id="08f2d-119">Example 2</span></span>

<span data-ttu-id="08f2d-120">建立新工作。</span><span class="sxs-lookup"><span data-stu-id="08f2d-120">Creates a new job.</span></span> <span data-ttu-id="08f2d-121"> (自動) </span><span class="sxs-lookup"><span data-stu-id="08f2d-121">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlElasticJob -Name job1 -RunOnce
```

## <span data-ttu-id="08f2d-122">參數</span><span class="sxs-lookup"><span data-stu-id="08f2d-122">PARAMETERS</span></span>

### <span data-ttu-id="08f2d-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="08f2d-123">-AgentName</span></span>
<span data-ttu-id="08f2d-124">代理人名稱</span><span class="sxs-lookup"><span data-stu-id="08f2d-124">The agent name</span></span>

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

### <span data-ttu-id="08f2d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08f2d-125">-DefaultProfile</span></span>
<span data-ttu-id="08f2d-126">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="08f2d-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08f2d-127">-描述</span><span class="sxs-lookup"><span data-stu-id="08f2d-127">-Description</span></span>
<span data-ttu-id="08f2d-128">工作描述</span><span class="sxs-lookup"><span data-stu-id="08f2d-128">The job description</span></span>

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

### <span data-ttu-id="08f2d-129">-啟用</span><span class="sxs-lookup"><span data-stu-id="08f2d-129">-Enable</span></span>
<span data-ttu-id="08f2d-130">指出客戶想要啟用此工作的標標。</span><span class="sxs-lookup"><span data-stu-id="08f2d-130">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="08f2d-131">-EndTime</span><span class="sxs-lookup"><span data-stu-id="08f2d-131">-EndTime</span></span>
<span data-ttu-id="08f2d-132">工作排程結束時間</span><span class="sxs-lookup"><span data-stu-id="08f2d-132">The job schedule end time</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: Recurring, RecurringUsingParentObject, RecurringUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08f2d-133">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="08f2d-133">-IntervalCount</span></span>
<span data-ttu-id="08f2d-134">週期性排程間隔計數</span><span class="sxs-lookup"><span data-stu-id="08f2d-134">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="08f2d-135">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="08f2d-135">-IntervalType</span></span>
<span data-ttu-id="08f2d-136">週期性排程間隔類型 - 可以是分鐘、小時、日、周、月</span><span class="sxs-lookup"><span data-stu-id="08f2d-136">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="08f2d-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="08f2d-137">-Name</span></span>
<span data-ttu-id="08f2d-138">工作名稱</span><span class="sxs-lookup"><span data-stu-id="08f2d-138">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: JobName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08f2d-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="08f2d-139">-ParentObject</span></span>
<span data-ttu-id="08f2d-140">代理程式輸入物件</span><span class="sxs-lookup"><span data-stu-id="08f2d-140">The agent input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel
Parameter Sets: ObjectSet, RunOnceUsingParentObject, RecurringUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08f2d-141">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="08f2d-141">-ParentResourceId</span></span>
<span data-ttu-id="08f2d-142">代理程式資源識別碼</span><span class="sxs-lookup"><span data-stu-id="08f2d-142">The agent resource id</span></span>

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

### <span data-ttu-id="08f2d-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08f2d-143">-ResourceGroupName</span></span>
<span data-ttu-id="08f2d-144">資源組名</span><span class="sxs-lookup"><span data-stu-id="08f2d-144">The resource group name</span></span>

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

### <span data-ttu-id="08f2d-145">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="08f2d-145">-RunOnce</span></span>
<span data-ttu-id="08f2d-146">指出工作的標號將會執行一次</span><span class="sxs-lookup"><span data-stu-id="08f2d-146">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="08f2d-147">-ServerName</span><span class="sxs-lookup"><span data-stu-id="08f2d-147">-ServerName</span></span>
<span data-ttu-id="08f2d-148">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="08f2d-148">The server name</span></span>

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

### <span data-ttu-id="08f2d-149">-StartTime</span><span class="sxs-lookup"><span data-stu-id="08f2d-149">-StartTime</span></span>
<span data-ttu-id="08f2d-150">工作排程開始時間</span><span class="sxs-lookup"><span data-stu-id="08f2d-150">The job schedule start time</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: RunOnce, Recurring, RunOnceUsingParentObject, RecurringUsingParentObject, RunOnceUsingParentResourceId, RecurringUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08f2d-151">-確認</span><span class="sxs-lookup"><span data-stu-id="08f2d-151">-Confirm</span></span>
<span data-ttu-id="08f2d-152">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="08f2d-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08f2d-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08f2d-153">-WhatIf</span></span>
<span data-ttu-id="08f2d-154">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="08f2d-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08f2d-155">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="08f2d-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08f2d-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08f2d-156">CommonParameters</span></span>
<span data-ttu-id="08f2d-157">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="08f2d-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08f2d-158">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="08f2d-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08f2d-159">輸入</span><span class="sxs-lookup"><span data-stu-id="08f2d-159">INPUTS</span></span>

### <span data-ttu-id="08f2d-160">Microsoft.Azure.Commands.Sql.AzureJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="08f2d-160">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="08f2d-161">輸出</span><span class="sxs-lookup"><span data-stu-id="08f2d-161">OUTPUTS</span></span>

### <span data-ttu-id="08f2d-162">Microsoft.Azure.Commands.Sql.AzureJobs.Model.AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="08f2d-162">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="08f2d-163">筆記</span><span class="sxs-lookup"><span data-stu-id="08f2d-163">NOTES</span></span>

## <span data-ttu-id="08f2d-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="08f2d-164">RELATED LINKS</span></span>
