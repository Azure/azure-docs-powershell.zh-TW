---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/stop-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
ms.openlocfilehash: 0b7fc702ad331a2ad51e1adfaf4aefd6ae440259
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792818"
---
# <span data-ttu-id="505f2-101">Stop-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="505f2-101">Stop-AzSqlElasticJob</span></span>

## <span data-ttu-id="505f2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="505f2-102">SYNOPSIS</span></span>
<span data-ttu-id="505f2-103">停止指定其工作執行 id 的工作</span><span class="sxs-lookup"><span data-stu-id="505f2-103">Stops a job given it's job execution id</span></span>

## <span data-ttu-id="505f2-104">句法</span><span class="sxs-lookup"><span data-stu-id="505f2-104">SYNTAX</span></span>

### <span data-ttu-id="505f2-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="505f2-105">DefaultSet (Default)</span></span>
```
Stop-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="505f2-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="505f2-106">ObjectSet</span></span>
```
Stop-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobExecutionModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="505f2-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="505f2-107">ResourceIdSet</span></span>
```
Stop-AzSqlElasticJob [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="505f2-108">說明</span><span class="sxs-lookup"><span data-stu-id="505f2-108">DESCRIPTION</span></span>
<span data-ttu-id="505f2-109">Stop-AzSqlElasticJob Cmdlet 會停止作業，並執行執行。</span><span class="sxs-lookup"><span data-stu-id="505f2-109">The Stop-AzSqlElasticJob cmdlet stops a job's with a running execution.</span></span>
<span data-ttu-id="505f2-110">傳回作業執行的目前狀態</span><span class="sxs-lookup"><span data-stu-id="505f2-110">Returns the current status of the job execution</span></span>

## <span data-ttu-id="505f2-111">示例</span><span class="sxs-lookup"><span data-stu-id="505f2-111">EXAMPLES</span></span>

### <span data-ttu-id="505f2-112">範例 1-停止執行工作執行的工作</span><span class="sxs-lookup"><span data-stu-id="505f2-112">Example 1 - Stops a job with a running job execution</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId dab0ebe8-fd52-42e9-bacf-e5f27577039b
$je | Stop-AzSqlElasticJob
JobName JobExecutionId                       Lifecycle                    StartTime            EndTime
------- --------------                       ---------                    ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b WaitingForChildJobExecutions 6/1/2018 10:13:56 PM
```

<span data-ttu-id="505f2-113">停止執行中的工作，並傳回目前的狀態</span><span class="sxs-lookup"><span data-stu-id="505f2-113">Stops a running job execution and returns it's current status</span></span>

## <span data-ttu-id="505f2-114">參數</span><span class="sxs-lookup"><span data-stu-id="505f2-114">PARAMETERS</span></span>

### <span data-ttu-id="505f2-115">-AgentName</span><span class="sxs-lookup"><span data-stu-id="505f2-115">-AgentName</span></span>
<span data-ttu-id="505f2-116">代理程式名稱</span><span class="sxs-lookup"><span data-stu-id="505f2-116">The agent name</span></span>

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

### <span data-ttu-id="505f2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="505f2-117">-DefaultProfile</span></span>
<span data-ttu-id="505f2-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="505f2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="505f2-119">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="505f2-119">-JobExecutionId</span></span>
<span data-ttu-id="505f2-120">作業執行 id。</span><span class="sxs-lookup"><span data-stu-id="505f2-120">The job execution id.</span></span>

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

### <span data-ttu-id="505f2-121">-JobName</span><span class="sxs-lookup"><span data-stu-id="505f2-121">-JobName</span></span>
<span data-ttu-id="505f2-122">作業名稱</span><span class="sxs-lookup"><span data-stu-id="505f2-122">The job name</span></span>

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

### <span data-ttu-id="505f2-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="505f2-123">-ParentObject</span></span>
<span data-ttu-id="505f2-124">Agent 控制資料庫物件</span><span class="sxs-lookup"><span data-stu-id="505f2-124">The Agent Control Database Object</span></span>

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

### <span data-ttu-id="505f2-125">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="505f2-125">-ParentResourceId</span></span>
<span data-ttu-id="505f2-126">作業執行資源識別碼</span><span class="sxs-lookup"><span data-stu-id="505f2-126">The job execution resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="505f2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="505f2-127">-ResourceGroupName</span></span>
<span data-ttu-id="505f2-128">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="505f2-128">The resource group name</span></span>

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

### <span data-ttu-id="505f2-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="505f2-129">-ServerName</span></span>
<span data-ttu-id="505f2-130">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="505f2-130">The server name</span></span>

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

### <span data-ttu-id="505f2-131">-確認</span><span class="sxs-lookup"><span data-stu-id="505f2-131">-Confirm</span></span>
<span data-ttu-id="505f2-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="505f2-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="505f2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="505f2-133">-WhatIf</span></span>
<span data-ttu-id="505f2-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="505f2-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="505f2-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="505f2-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="505f2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="505f2-136">CommonParameters</span></span>
<span data-ttu-id="505f2-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="505f2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="505f2-138">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="505f2-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="505f2-139">輸入</span><span class="sxs-lookup"><span data-stu-id="505f2-139">INPUTS</span></span>

### <span data-ttu-id="505f2-140">AzureSqlElasticJobExecutionModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="505f2-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="505f2-141">輸出</span><span class="sxs-lookup"><span data-stu-id="505f2-141">OUTPUTS</span></span>

### <span data-ttu-id="505f2-142">AzureSqlElasticJobExecutionModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="505f2-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="505f2-143">筆記</span><span class="sxs-lookup"><span data-stu-id="505f2-143">NOTES</span></span>

## <span data-ttu-id="505f2-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="505f2-144">RELATED LINKS</span></span>

## <span data-ttu-id="505f2-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="505f2-145">RELATED LINKS</span></span>
