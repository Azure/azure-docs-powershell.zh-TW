---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
ms.openlocfilehash: 04f182cb410e77a9ca61aa6f80da14c08e517406
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792590"
---
# <span data-ttu-id="92b08-101">Set-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="92b08-101">Set-AzSqlElasticJob</span></span>

## <span data-ttu-id="92b08-102">摘要</span><span class="sxs-lookup"><span data-stu-id="92b08-102">SYNOPSIS</span></span>
<span data-ttu-id="92b08-103">更新作業</span><span class="sxs-lookup"><span data-stu-id="92b08-103">Updates a job</span></span>

## <span data-ttu-id="92b08-104">句法</span><span class="sxs-lookup"><span data-stu-id="92b08-104">SYNTAX</span></span>

### <span data-ttu-id="92b08-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="92b08-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92b08-106">RunOnce</span><span class="sxs-lookup"><span data-stu-id="92b08-106">RunOnce</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92b08-107">週期性</span><span class="sxs-lookup"><span data-stu-id="92b08-107">Recurring</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92b08-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="92b08-108">ObjectSet</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="92b08-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="92b08-109">RunOnceUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-RunOnce] [-StartTime <DateTime>]
 [-EndTime <DateTime>] [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92b08-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="92b08-110">RecurringUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92b08-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="92b08-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92b08-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="92b08-112">RunOnceUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92b08-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="92b08-113">RecurringUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92b08-114">說明</span><span class="sxs-lookup"><span data-stu-id="92b08-114">DESCRIPTION</span></span>
<span data-ttu-id="92b08-115">Set-AzSqlElasticJob Cmdlet 會更新作業</span><span class="sxs-lookup"><span data-stu-id="92b08-115">The Set-AzSqlElasticJob cmdlet updates a job</span></span>

## <span data-ttu-id="92b08-116">示例</span><span class="sxs-lookup"><span data-stu-id="92b08-116">EXAMPLES</span></span>

### <span data-ttu-id="92b08-117">範例 1-更新作業以從現在開始一個小時，並每1小時重複一次</span><span class="sxs-lookup"><span data-stu-id="92b08-117">Example 1 - Updates a job to start an hour from now and repeat every 1 hour</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Set-AzSqlElasticJob -IntervalType Hour -IntervalCount 1 -StartTime (Get-Date).AddHours(1) -Enable

JobName Version Description StartTime            EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------            -------                ------------ -------- -------
job1    0                   6/1/2018 10:50:15 PM 12/31/9999 11:59:59 AM Recurring    PT1H     True
```

<span data-ttu-id="92b08-118">更新作業</span><span class="sxs-lookup"><span data-stu-id="92b08-118">Updates a job</span></span>

## <span data-ttu-id="92b08-119">參數</span><span class="sxs-lookup"><span data-stu-id="92b08-119">PARAMETERS</span></span>

### <span data-ttu-id="92b08-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="92b08-120">-AgentName</span></span>
<span data-ttu-id="92b08-121">代理程式名稱</span><span class="sxs-lookup"><span data-stu-id="92b08-121">The agent name</span></span>

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

### <span data-ttu-id="92b08-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92b08-122">-DefaultProfile</span></span>
<span data-ttu-id="92b08-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="92b08-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92b08-124">-描述</span><span class="sxs-lookup"><span data-stu-id="92b08-124">-Description</span></span>
<span data-ttu-id="92b08-125">作業描述</span><span class="sxs-lookup"><span data-stu-id="92b08-125">The job description</span></span>

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

### <span data-ttu-id="92b08-126">-啟用</span><span class="sxs-lookup"><span data-stu-id="92b08-126">-Enable</span></span>
<span data-ttu-id="92b08-127">指示客戶希望啟用此工作的標誌。</span><span class="sxs-lookup"><span data-stu-id="92b08-127">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="92b08-128">-EndTime</span><span class="sxs-lookup"><span data-stu-id="92b08-128">-EndTime</span></span>
<span data-ttu-id="92b08-129">作業排程結束時間</span><span class="sxs-lookup"><span data-stu-id="92b08-129">The job schedule end time</span></span>

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

### <span data-ttu-id="92b08-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92b08-130">-InputObject</span></span>
<span data-ttu-id="92b08-131">作業輸入物件</span><span class="sxs-lookup"><span data-stu-id="92b08-131">The job input object</span></span>

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

### <span data-ttu-id="92b08-132">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="92b08-132">-IntervalCount</span></span>
<span data-ttu-id="92b08-133">週期性排程間隔計數</span><span class="sxs-lookup"><span data-stu-id="92b08-133">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="92b08-134">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="92b08-134">-IntervalType</span></span>
<span data-ttu-id="92b08-135">週期性排程間隔類型-可以是分鐘、小時、日、周、月</span><span class="sxs-lookup"><span data-stu-id="92b08-135">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="92b08-136">-名稱</span><span class="sxs-lookup"><span data-stu-id="92b08-136">-Name</span></span>
<span data-ttu-id="92b08-137">作業名稱</span><span class="sxs-lookup"><span data-stu-id="92b08-137">The job name</span></span>

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

### <span data-ttu-id="92b08-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92b08-138">-ResourceGroupName</span></span>
<span data-ttu-id="92b08-139">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="92b08-139">The resource group name</span></span>

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

### <span data-ttu-id="92b08-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92b08-140">-ResourceId</span></span>
<span data-ttu-id="92b08-141">作業資源識別碼</span><span class="sxs-lookup"><span data-stu-id="92b08-141">The job resource id</span></span>

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

### <span data-ttu-id="92b08-142">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="92b08-142">-RunOnce</span></span>
<span data-ttu-id="92b08-143">指示作業的標誌將會執行一次</span><span class="sxs-lookup"><span data-stu-id="92b08-143">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="92b08-144">-ServerName</span><span class="sxs-lookup"><span data-stu-id="92b08-144">-ServerName</span></span>
<span data-ttu-id="92b08-145">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="92b08-145">The server name</span></span>

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

### <span data-ttu-id="92b08-146">-StartTime</span><span class="sxs-lookup"><span data-stu-id="92b08-146">-StartTime</span></span>
<span data-ttu-id="92b08-147">作業排程開始時間</span><span class="sxs-lookup"><span data-stu-id="92b08-147">The job schedule start time</span></span>

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

### <span data-ttu-id="92b08-148">-確認</span><span class="sxs-lookup"><span data-stu-id="92b08-148">-Confirm</span></span>
<span data-ttu-id="92b08-149">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="92b08-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92b08-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92b08-150">-WhatIf</span></span>
<span data-ttu-id="92b08-151">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="92b08-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92b08-152">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="92b08-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92b08-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92b08-153">CommonParameters</span></span>
<span data-ttu-id="92b08-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="92b08-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92b08-155">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="92b08-155">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92b08-156">輸入</span><span class="sxs-lookup"><span data-stu-id="92b08-156">INPUTS</span></span>

### <span data-ttu-id="92b08-157">AzureSqlElasticJobModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="92b08-157">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="92b08-158">輸出</span><span class="sxs-lookup"><span data-stu-id="92b08-158">OUTPUTS</span></span>

### <span data-ttu-id="92b08-159">AzureSqlElasticJobModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="92b08-159">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="92b08-160">筆記</span><span class="sxs-lookup"><span data-stu-id="92b08-160">NOTES</span></span>

## <span data-ttu-id="92b08-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="92b08-161">RELATED LINKS</span></span>
