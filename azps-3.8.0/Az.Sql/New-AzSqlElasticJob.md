---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
ms.openlocfilehash: 98c019c8dedf767fc2b75bb2133f7c545ffd03ce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93797038"
---
# <span data-ttu-id="a56a6-101">New-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="a56a6-101">New-AzSqlElasticJob</span></span>

## <span data-ttu-id="a56a6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a56a6-102">SYNOPSIS</span></span>
<span data-ttu-id="a56a6-103">建立新工作</span><span class="sxs-lookup"><span data-stu-id="a56a6-103">Creates a new job</span></span>

## <span data-ttu-id="a56a6-104">句法</span><span class="sxs-lookup"><span data-stu-id="a56a6-104">SYNTAX</span></span>

### <span data-ttu-id="a56a6-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a56a6-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a56a6-106">RunOnce</span><span class="sxs-lookup"><span data-stu-id="a56a6-106">RunOnce</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a56a6-107">週期性</span><span class="sxs-lookup"><span data-stu-id="a56a6-107">Recurring</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a56a6-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="a56a6-108">ObjectSet</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-Description <String>]
 [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a56a6-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="a56a6-109">RunOnceUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-RunOnce]
 [-StartTime <DateTime>] [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a56a6-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="a56a6-110">RecurringUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a56a6-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a56a6-111">ResourceIdSet</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a56a6-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a56a6-112">RunOnceUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-RunOnce] [-StartTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a56a6-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a56a6-113">RecurringUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a56a6-114">說明</span><span class="sxs-lookup"><span data-stu-id="a56a6-114">DESCRIPTION</span></span>
<span data-ttu-id="a56a6-115">New-AzSqlElasticJob Cmdlet 會建立新工作</span><span class="sxs-lookup"><span data-stu-id="a56a6-115">The New-AzSqlElasticJob cmdlet creates a new job</span></span>

## <span data-ttu-id="a56a6-116">示例</span><span class="sxs-lookup"><span data-stu-id="a56a6-116">EXAMPLES</span></span>

### <span data-ttu-id="a56a6-117">範例 1-建立新工作</span><span class="sxs-lookup"><span data-stu-id="a56a6-117">Example 1 - Creates a new job</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="a56a6-118">建立新工作</span><span class="sxs-lookup"><span data-stu-id="a56a6-118">Creates a new job</span></span>

## <span data-ttu-id="a56a6-119">參數</span><span class="sxs-lookup"><span data-stu-id="a56a6-119">PARAMETERS</span></span>

### <span data-ttu-id="a56a6-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="a56a6-120">-AgentName</span></span>
<span data-ttu-id="a56a6-121">代理程式名稱</span><span class="sxs-lookup"><span data-stu-id="a56a6-121">The agent name</span></span>

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

### <span data-ttu-id="a56a6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a56a6-122">-DefaultProfile</span></span>
<span data-ttu-id="a56a6-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a56a6-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a56a6-124">-描述</span><span class="sxs-lookup"><span data-stu-id="a56a6-124">-Description</span></span>
<span data-ttu-id="a56a6-125">作業描述</span><span class="sxs-lookup"><span data-stu-id="a56a6-125">The job description</span></span>

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

### <span data-ttu-id="a56a6-126">-啟用</span><span class="sxs-lookup"><span data-stu-id="a56a6-126">-Enable</span></span>
<span data-ttu-id="a56a6-127">指示客戶希望啟用此工作的標誌。</span><span class="sxs-lookup"><span data-stu-id="a56a6-127">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="a56a6-128">-EndTime</span><span class="sxs-lookup"><span data-stu-id="a56a6-128">-EndTime</span></span>
<span data-ttu-id="a56a6-129">作業排程結束時間</span><span class="sxs-lookup"><span data-stu-id="a56a6-129">The job schedule end time</span></span>

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

### <span data-ttu-id="a56a6-130">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="a56a6-130">-IntervalCount</span></span>
<span data-ttu-id="a56a6-131">週期性排程間隔計數</span><span class="sxs-lookup"><span data-stu-id="a56a6-131">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="a56a6-132">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="a56a6-132">-IntervalType</span></span>
<span data-ttu-id="a56a6-133">週期性排程間隔類型-可以是分鐘、小時、日、周、月</span><span class="sxs-lookup"><span data-stu-id="a56a6-133">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="a56a6-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="a56a6-134">-Name</span></span>
<span data-ttu-id="a56a6-135">作業名稱</span><span class="sxs-lookup"><span data-stu-id="a56a6-135">The job name</span></span>

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

### <span data-ttu-id="a56a6-136">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a56a6-136">-ParentObject</span></span>
<span data-ttu-id="a56a6-137">Agent 輸入物件</span><span class="sxs-lookup"><span data-stu-id="a56a6-137">The agent input object</span></span>

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

### <span data-ttu-id="a56a6-138">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a56a6-138">-ParentResourceId</span></span>
<span data-ttu-id="a56a6-139">Agent 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="a56a6-139">The agent resource id</span></span>

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

### <span data-ttu-id="a56a6-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a56a6-140">-ResourceGroupName</span></span>
<span data-ttu-id="a56a6-141">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="a56a6-141">The resource group name</span></span>

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

### <span data-ttu-id="a56a6-142">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="a56a6-142">-RunOnce</span></span>
<span data-ttu-id="a56a6-143">指示作業的標誌將會執行一次</span><span class="sxs-lookup"><span data-stu-id="a56a6-143">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="a56a6-144">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a56a6-144">-ServerName</span></span>
<span data-ttu-id="a56a6-145">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="a56a6-145">The server name</span></span>

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

### <span data-ttu-id="a56a6-146">-StartTime</span><span class="sxs-lookup"><span data-stu-id="a56a6-146">-StartTime</span></span>
<span data-ttu-id="a56a6-147">作業排程開始時間</span><span class="sxs-lookup"><span data-stu-id="a56a6-147">The job schedule start time</span></span>

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

### <span data-ttu-id="a56a6-148">-確認</span><span class="sxs-lookup"><span data-stu-id="a56a6-148">-Confirm</span></span>
<span data-ttu-id="a56a6-149">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a56a6-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a56a6-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a56a6-150">-WhatIf</span></span>
<span data-ttu-id="a56a6-151">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a56a6-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a56a6-152">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a56a6-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a56a6-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a56a6-153">CommonParameters</span></span>
<span data-ttu-id="a56a6-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a56a6-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a56a6-155">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a56a6-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a56a6-156">輸入</span><span class="sxs-lookup"><span data-stu-id="a56a6-156">INPUTS</span></span>

### <span data-ttu-id="a56a6-157">AzureSqlElasticJobAgentModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="a56a6-157">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="a56a6-158">輸出</span><span class="sxs-lookup"><span data-stu-id="a56a6-158">OUTPUTS</span></span>

### <span data-ttu-id="a56a6-159">AzureSqlElasticJobModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="a56a6-159">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="a56a6-160">筆記</span><span class="sxs-lookup"><span data-stu-id="a56a6-160">NOTES</span></span>

## <span data-ttu-id="a56a6-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="a56a6-161">RELATED LINKS</span></span>
