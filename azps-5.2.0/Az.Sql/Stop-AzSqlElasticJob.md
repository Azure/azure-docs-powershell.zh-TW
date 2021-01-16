---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/stop-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
ms.openlocfilehash: ec5ab9706bd459a07c91e7060d3bf6da30f76ed5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98273927"
---
# <span data-ttu-id="83479-101">Stop-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="83479-101">Stop-AzSqlElasticJob</span></span>

## <span data-ttu-id="83479-102">摘要</span><span class="sxs-lookup"><span data-stu-id="83479-102">SYNOPSIS</span></span>
<span data-ttu-id="83479-103">停止指定其工作執行 id 的工作</span><span class="sxs-lookup"><span data-stu-id="83479-103">Stops a job given it's job execution id</span></span>

## <span data-ttu-id="83479-104">句法</span><span class="sxs-lookup"><span data-stu-id="83479-104">SYNTAX</span></span>

### <span data-ttu-id="83479-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="83479-105">DefaultSet (Default)</span></span>
```
Stop-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="83479-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="83479-106">ObjectSet</span></span>
```
Stop-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobExecutionModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83479-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="83479-107">ResourceIdSet</span></span>
```
Stop-AzSqlElasticJob [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83479-108">說明</span><span class="sxs-lookup"><span data-stu-id="83479-108">DESCRIPTION</span></span>
<span data-ttu-id="83479-109">Stop-AzSqlElasticJob Cmdlet 會停止作業，並執行執行。</span><span class="sxs-lookup"><span data-stu-id="83479-109">The Stop-AzSqlElasticJob cmdlet stops a job's with a running execution.</span></span>
<span data-ttu-id="83479-110">傳回作業執行的目前狀態</span><span class="sxs-lookup"><span data-stu-id="83479-110">Returns the current status of the job execution</span></span>

## <span data-ttu-id="83479-111">示例</span><span class="sxs-lookup"><span data-stu-id="83479-111">EXAMPLES</span></span>

### <span data-ttu-id="83479-112">範例1：停止執行作業執行的工作</span><span class="sxs-lookup"><span data-stu-id="83479-112">Example 1: Stops a job with a running job execution</span></span>
```powershell
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId dab0ebe8-fd52-42e9-bacf-e5f27577039b
$je | Stop-AzSqlElasticJob
JobName JobExecutionId                       Lifecycle                    StartTime            EndTime
------- --------------                       ---------                    ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b WaitingForChildJobExecutions 6/1/2018 10:13:56 PM
```

<span data-ttu-id="83479-113">停止執行中的工作，並傳回目前的狀態</span><span class="sxs-lookup"><span data-stu-id="83479-113">Stops a running job execution and returns it's current status</span></span>

### <span data-ttu-id="83479-114">範例2</span><span class="sxs-lookup"><span data-stu-id="83479-114">Example 2</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Stop-AzSqlElasticJob -AgentName agent -JobExecutionId 00000000-0000-0000-0000-000000000000 -JobName job1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="83479-115">參數</span><span class="sxs-lookup"><span data-stu-id="83479-115">PARAMETERS</span></span>

### <span data-ttu-id="83479-116">-AgentName</span><span class="sxs-lookup"><span data-stu-id="83479-116">-AgentName</span></span>
<span data-ttu-id="83479-117">代理程式名稱</span><span class="sxs-lookup"><span data-stu-id="83479-117">The agent name</span></span>

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

### <span data-ttu-id="83479-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83479-118">-DefaultProfile</span></span>
<span data-ttu-id="83479-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="83479-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83479-120">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="83479-120">-JobExecutionId</span></span>
<span data-ttu-id="83479-121">作業執行 id。</span><span class="sxs-lookup"><span data-stu-id="83479-121">The job execution id.</span></span>

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

### <span data-ttu-id="83479-122">-JobName</span><span class="sxs-lookup"><span data-stu-id="83479-122">-JobName</span></span>
<span data-ttu-id="83479-123">作業名稱</span><span class="sxs-lookup"><span data-stu-id="83479-123">The job name</span></span>

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

### <span data-ttu-id="83479-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="83479-124">-ParentObject</span></span>
<span data-ttu-id="83479-125">Agent 控制資料庫物件</span><span class="sxs-lookup"><span data-stu-id="83479-125">The Agent Control Database Object</span></span>

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

### <span data-ttu-id="83479-126">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="83479-126">-ParentResourceId</span></span>
<span data-ttu-id="83479-127">作業執行資源識別碼</span><span class="sxs-lookup"><span data-stu-id="83479-127">The job execution resource id</span></span>

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

### <span data-ttu-id="83479-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83479-128">-ResourceGroupName</span></span>
<span data-ttu-id="83479-129">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="83479-129">The resource group name</span></span>

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

### <span data-ttu-id="83479-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="83479-130">-ServerName</span></span>
<span data-ttu-id="83479-131">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="83479-131">The server name</span></span>

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

### <span data-ttu-id="83479-132">-確認</span><span class="sxs-lookup"><span data-stu-id="83479-132">-Confirm</span></span>
<span data-ttu-id="83479-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="83479-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83479-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83479-134">-WhatIf</span></span>
<span data-ttu-id="83479-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="83479-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83479-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="83479-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83479-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83479-137">CommonParameters</span></span>
<span data-ttu-id="83479-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="83479-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83479-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="83479-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83479-140">輸入</span><span class="sxs-lookup"><span data-stu-id="83479-140">INPUTS</span></span>

### <span data-ttu-id="83479-141">AzureSqlElasticJobExecutionModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="83479-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="83479-142">輸出</span><span class="sxs-lookup"><span data-stu-id="83479-142">OUTPUTS</span></span>

### <span data-ttu-id="83479-143">AzureSqlElasticJobExecutionModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="83479-143">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="83479-144">筆記</span><span class="sxs-lookup"><span data-stu-id="83479-144">NOTES</span></span>

## <span data-ttu-id="83479-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="83479-145">RELATED LINKS</span></span>
