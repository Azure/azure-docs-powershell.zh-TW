---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/stop-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
ms.openlocfilehash: ff117dfee7f660845389bd62245be4ecfd53b2f7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93798134"
---
# <span data-ttu-id="04f24-101">Stop-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="04f24-101">Stop-AzSqlElasticJob</span></span>

## <span data-ttu-id="04f24-102">摘要</span><span class="sxs-lookup"><span data-stu-id="04f24-102">SYNOPSIS</span></span>
<span data-ttu-id="04f24-103">停止指定其工作執行 id 的工作</span><span class="sxs-lookup"><span data-stu-id="04f24-103">Stops a job given it's job execution id</span></span>

## <span data-ttu-id="04f24-104">句法</span><span class="sxs-lookup"><span data-stu-id="04f24-104">SYNTAX</span></span>

### <span data-ttu-id="04f24-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="04f24-105">DefaultSet (Default)</span></span>
```
Stop-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="04f24-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="04f24-106">ObjectSet</span></span>
```
Stop-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobExecutionModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04f24-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="04f24-107">ResourceIdSet</span></span>
```
Stop-AzSqlElasticJob [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04f24-108">說明</span><span class="sxs-lookup"><span data-stu-id="04f24-108">DESCRIPTION</span></span>
<span data-ttu-id="04f24-109">Stop-AzSqlElasticJob Cmdlet 會停止作業，並執行執行。</span><span class="sxs-lookup"><span data-stu-id="04f24-109">The Stop-AzSqlElasticJob cmdlet stops a job's with a running execution.</span></span>
<span data-ttu-id="04f24-110">傳回作業執行的目前狀態</span><span class="sxs-lookup"><span data-stu-id="04f24-110">Returns the current status of the job execution</span></span>

## <span data-ttu-id="04f24-111">示例</span><span class="sxs-lookup"><span data-stu-id="04f24-111">EXAMPLES</span></span>

### <span data-ttu-id="04f24-112">範例 1-停止執行工作執行的工作</span><span class="sxs-lookup"><span data-stu-id="04f24-112">Example 1 - Stops a job with a running job execution</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId dab0ebe8-fd52-42e9-bacf-e5f27577039b
$je | Stop-AzSqlElasticJob
JobName JobExecutionId                       Lifecycle                    StartTime            EndTime
------- --------------                       ---------                    ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b WaitingForChildJobExecutions 6/1/2018 10:13:56 PM
```

<span data-ttu-id="04f24-113">停止執行中的工作，並傳回目前的狀態</span><span class="sxs-lookup"><span data-stu-id="04f24-113">Stops a running job execution and returns it's current status</span></span>

## <span data-ttu-id="04f24-114">參數</span><span class="sxs-lookup"><span data-stu-id="04f24-114">PARAMETERS</span></span>

### <span data-ttu-id="04f24-115">-AgentName</span><span class="sxs-lookup"><span data-stu-id="04f24-115">-AgentName</span></span>
<span data-ttu-id="04f24-116">代理程式名稱</span><span class="sxs-lookup"><span data-stu-id="04f24-116">The agent name</span></span>

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

### <span data-ttu-id="04f24-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04f24-117">-DefaultProfile</span></span>
<span data-ttu-id="04f24-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="04f24-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04f24-119">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="04f24-119">-JobExecutionId</span></span>
<span data-ttu-id="04f24-120">作業執行 id。</span><span class="sxs-lookup"><span data-stu-id="04f24-120">The job execution id.</span></span>

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

### <span data-ttu-id="04f24-121">-JobName</span><span class="sxs-lookup"><span data-stu-id="04f24-121">-JobName</span></span>
<span data-ttu-id="04f24-122">作業名稱</span><span class="sxs-lookup"><span data-stu-id="04f24-122">The job name</span></span>

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

### <span data-ttu-id="04f24-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="04f24-123">-ParentObject</span></span>
<span data-ttu-id="04f24-124">Agent 控制資料庫物件</span><span class="sxs-lookup"><span data-stu-id="04f24-124">The Agent Control Database Object</span></span>

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

### <span data-ttu-id="04f24-125">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="04f24-125">-ParentResourceId</span></span>
<span data-ttu-id="04f24-126">作業執行資源識別碼</span><span class="sxs-lookup"><span data-stu-id="04f24-126">The job execution resource id</span></span>

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

### <span data-ttu-id="04f24-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04f24-127">-ResourceGroupName</span></span>
<span data-ttu-id="04f24-128">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="04f24-128">The resource group name</span></span>

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

### <span data-ttu-id="04f24-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="04f24-129">-ServerName</span></span>
<span data-ttu-id="04f24-130">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="04f24-130">The server name</span></span>

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

### <span data-ttu-id="04f24-131">-確認</span><span class="sxs-lookup"><span data-stu-id="04f24-131">-Confirm</span></span>
<span data-ttu-id="04f24-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="04f24-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04f24-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04f24-133">-WhatIf</span></span>
<span data-ttu-id="04f24-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="04f24-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04f24-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="04f24-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04f24-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04f24-136">CommonParameters</span></span>
<span data-ttu-id="04f24-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="04f24-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04f24-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="04f24-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04f24-139">輸入</span><span class="sxs-lookup"><span data-stu-id="04f24-139">INPUTS</span></span>

### <span data-ttu-id="04f24-140">AzureSqlElasticJobExecutionModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="04f24-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="04f24-141">輸出</span><span class="sxs-lookup"><span data-stu-id="04f24-141">OUTPUTS</span></span>

### <span data-ttu-id="04f24-142">AzureSqlElasticJobExecutionModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="04f24-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="04f24-143">筆記</span><span class="sxs-lookup"><span data-stu-id="04f24-143">NOTES</span></span>

## <span data-ttu-id="04f24-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="04f24-144">RELATED LINKS</span></span>
