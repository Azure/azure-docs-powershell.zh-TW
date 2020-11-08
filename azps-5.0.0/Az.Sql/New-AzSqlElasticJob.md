---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
ms.openlocfilehash: e6853c3b4fa32a10e93ee281aab0b97755403671
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138131"
---
# <span data-ttu-id="50a45-101">New-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="50a45-101">New-AzSqlElasticJob</span></span>

## <span data-ttu-id="50a45-102">摘要</span><span class="sxs-lookup"><span data-stu-id="50a45-102">SYNOPSIS</span></span>
<span data-ttu-id="50a45-103">建立新工作</span><span class="sxs-lookup"><span data-stu-id="50a45-103">Creates a new job</span></span>

## <span data-ttu-id="50a45-104">句法</span><span class="sxs-lookup"><span data-stu-id="50a45-104">SYNTAX</span></span>

### <span data-ttu-id="50a45-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="50a45-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="50a45-106">RunOnce</span><span class="sxs-lookup"><span data-stu-id="50a45-106">RunOnce</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50a45-107">週期性</span><span class="sxs-lookup"><span data-stu-id="50a45-107">Recurring</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="50a45-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="50a45-108">ObjectSet</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-Description <String>]
 [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50a45-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="50a45-109">RunOnceUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-RunOnce]
 [-StartTime <DateTime>] [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50a45-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="50a45-110">RecurringUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50a45-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="50a45-111">ResourceIdSet</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50a45-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="50a45-112">RunOnceUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-RunOnce] [-StartTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="50a45-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="50a45-113">RecurringUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50a45-114">說明</span><span class="sxs-lookup"><span data-stu-id="50a45-114">DESCRIPTION</span></span>
<span data-ttu-id="50a45-115">New-AzSqlElasticJob Cmdlet 會建立新工作</span><span class="sxs-lookup"><span data-stu-id="50a45-115">The New-AzSqlElasticJob cmdlet creates a new job</span></span>

## <span data-ttu-id="50a45-116">示例</span><span class="sxs-lookup"><span data-stu-id="50a45-116">EXAMPLES</span></span>

### <span data-ttu-id="50a45-117">範例1：建立新工作</span><span class="sxs-lookup"><span data-stu-id="50a45-117">Example 1: Creates a new job</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="50a45-118">建立新工作</span><span class="sxs-lookup"><span data-stu-id="50a45-118">Creates a new job</span></span>

### <span data-ttu-id="50a45-119">範例2</span><span class="sxs-lookup"><span data-stu-id="50a45-119">Example 2</span></span>

<span data-ttu-id="50a45-120">建立新工作。</span><span class="sxs-lookup"><span data-stu-id="50a45-120">Creates a new job.</span></span> <span data-ttu-id="50a45-121"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="50a45-121">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlElasticJob -Name job1 -RunOnce
```

## <span data-ttu-id="50a45-122">參數</span><span class="sxs-lookup"><span data-stu-id="50a45-122">PARAMETERS</span></span>

### <span data-ttu-id="50a45-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="50a45-123">-AgentName</span></span>
<span data-ttu-id="50a45-124">代理程式名稱</span><span class="sxs-lookup"><span data-stu-id="50a45-124">The agent name</span></span>

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

### <span data-ttu-id="50a45-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50a45-125">-DefaultProfile</span></span>
<span data-ttu-id="50a45-126">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="50a45-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50a45-127">-描述</span><span class="sxs-lookup"><span data-stu-id="50a45-127">-Description</span></span>
<span data-ttu-id="50a45-128">作業描述</span><span class="sxs-lookup"><span data-stu-id="50a45-128">The job description</span></span>

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

### <span data-ttu-id="50a45-129">-啟用</span><span class="sxs-lookup"><span data-stu-id="50a45-129">-Enable</span></span>
<span data-ttu-id="50a45-130">指示客戶希望啟用此工作的標誌。</span><span class="sxs-lookup"><span data-stu-id="50a45-130">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="50a45-131">-EndTime</span><span class="sxs-lookup"><span data-stu-id="50a45-131">-EndTime</span></span>
<span data-ttu-id="50a45-132">作業排程結束時間</span><span class="sxs-lookup"><span data-stu-id="50a45-132">The job schedule end time</span></span>

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

### <span data-ttu-id="50a45-133">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="50a45-133">-IntervalCount</span></span>
<span data-ttu-id="50a45-134">週期性排程間隔計數</span><span class="sxs-lookup"><span data-stu-id="50a45-134">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="50a45-135">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="50a45-135">-IntervalType</span></span>
<span data-ttu-id="50a45-136">週期性排程間隔類型-可以是分鐘、小時、日、周、月</span><span class="sxs-lookup"><span data-stu-id="50a45-136">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="50a45-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="50a45-137">-Name</span></span>
<span data-ttu-id="50a45-138">作業名稱</span><span class="sxs-lookup"><span data-stu-id="50a45-138">The job name</span></span>

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

### <span data-ttu-id="50a45-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="50a45-139">-ParentObject</span></span>
<span data-ttu-id="50a45-140">Agent 輸入物件</span><span class="sxs-lookup"><span data-stu-id="50a45-140">The agent input object</span></span>

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

### <span data-ttu-id="50a45-141">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="50a45-141">-ParentResourceId</span></span>
<span data-ttu-id="50a45-142">Agent 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="50a45-142">The agent resource id</span></span>

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

### <span data-ttu-id="50a45-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50a45-143">-ResourceGroupName</span></span>
<span data-ttu-id="50a45-144">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="50a45-144">The resource group name</span></span>

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

### <span data-ttu-id="50a45-145">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="50a45-145">-RunOnce</span></span>
<span data-ttu-id="50a45-146">指示作業的標誌將會執行一次</span><span class="sxs-lookup"><span data-stu-id="50a45-146">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="50a45-147">-ServerName</span><span class="sxs-lookup"><span data-stu-id="50a45-147">-ServerName</span></span>
<span data-ttu-id="50a45-148">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="50a45-148">The server name</span></span>

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

### <span data-ttu-id="50a45-149">-StartTime</span><span class="sxs-lookup"><span data-stu-id="50a45-149">-StartTime</span></span>
<span data-ttu-id="50a45-150">作業排程開始時間</span><span class="sxs-lookup"><span data-stu-id="50a45-150">The job schedule start time</span></span>

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

### <span data-ttu-id="50a45-151">-確認</span><span class="sxs-lookup"><span data-stu-id="50a45-151">-Confirm</span></span>
<span data-ttu-id="50a45-152">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="50a45-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50a45-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50a45-153">-WhatIf</span></span>
<span data-ttu-id="50a45-154">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="50a45-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50a45-155">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="50a45-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50a45-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50a45-156">CommonParameters</span></span>
<span data-ttu-id="50a45-157">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="50a45-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50a45-158">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="50a45-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50a45-159">輸入</span><span class="sxs-lookup"><span data-stu-id="50a45-159">INPUTS</span></span>

### <span data-ttu-id="50a45-160">AzureSqlElasticJobAgentModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="50a45-160">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="50a45-161">輸出</span><span class="sxs-lookup"><span data-stu-id="50a45-161">OUTPUTS</span></span>

### <span data-ttu-id="50a45-162">AzureSqlElasticJobModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="50a45-162">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="50a45-163">筆記</span><span class="sxs-lookup"><span data-stu-id="50a45-163">NOTES</span></span>

## <span data-ttu-id="50a45-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="50a45-164">RELATED LINKS</span></span>