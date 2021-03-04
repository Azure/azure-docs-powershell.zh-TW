---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/start-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlElasticJob.md
ms.openlocfilehash: 6163c7be725d66c7e1f64fced3be0269ffedd32f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916860"
---
# <span data-ttu-id="bcf37-101">Start-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="bcf37-101">Start-AzSqlElasticJob</span></span>

## <span data-ttu-id="bcf37-102">簡介</span><span class="sxs-lookup"><span data-stu-id="bcf37-102">SYNOPSIS</span></span>
<span data-ttu-id="bcf37-103">開始工作，傳回可投票以查看其狀態的工作執行識別碼</span><span class="sxs-lookup"><span data-stu-id="bcf37-103">Starts a job, returning a job execution id that can be polled to view it's status</span></span>

## <span data-ttu-id="bcf37-104">語法</span><span class="sxs-lookup"><span data-stu-id="bcf37-104">SYNTAX</span></span>

### <span data-ttu-id="bcf37-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="bcf37-105">DefaultSet (Default)</span></span>
```
Start-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> [-Wait] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bcf37-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="bcf37-106">ObjectSet</span></span>
```
Start-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobModel> [-Wait] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bcf37-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="bcf37-107">ResourceIdSet</span></span>
```
Start-AzSqlElasticJob [-ParentResourceId] <String> [-Wait] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcf37-108">描述</span><span class="sxs-lookup"><span data-stu-id="bcf37-108">DESCRIPTION</span></span>
<span data-ttu-id="bcf37-109">Cmdlet Start-AzSqlElasticJob開始重新執行新工作的工作</span><span class="sxs-lookup"><span data-stu-id="bcf37-109">The Start-AzSqlElasticJob cmdlet starts a job returning a new job execution</span></span>

## <span data-ttu-id="bcf37-110">例子</span><span class="sxs-lookup"><span data-stu-id="bcf37-110">EXAMPLES</span></span>

### <span data-ttu-id="bcf37-111">範例 1 - 開始工作會返回新的工作執行</span><span class="sxs-lookup"><span data-stu-id="bcf37-111">Example 1 - Starts a job returning a new job execution</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Start-AzSqlElasticJob

JobName JobExecutionId                       Lifecycle StartTime EndTime
------- --------------                       --------- --------- -------
job1    b93b3a90-987b-4565-b3d3-5fa1751fa9bc Created
```

<span data-ttu-id="bcf37-112">開始重新執行新工作的工作</span><span class="sxs-lookup"><span data-stu-id="bcf37-112">Starts a job returning a new job execution</span></span>

## <span data-ttu-id="bcf37-113">參數</span><span class="sxs-lookup"><span data-stu-id="bcf37-113">PARAMETERS</span></span>

### <span data-ttu-id="bcf37-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="bcf37-114">-AgentName</span></span>
<span data-ttu-id="bcf37-115">代理人名稱</span><span class="sxs-lookup"><span data-stu-id="bcf37-115">The agent name</span></span>

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

### <span data-ttu-id="bcf37-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bcf37-116">-AsJob</span></span>
<span data-ttu-id="bcf37-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="bcf37-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bcf37-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcf37-118">-DefaultProfile</span></span>
<span data-ttu-id="bcf37-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="bcf37-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bcf37-120">-JobName</span><span class="sxs-lookup"><span data-stu-id="bcf37-120">-JobName</span></span>
<span data-ttu-id="bcf37-121">工作名稱</span><span class="sxs-lookup"><span data-stu-id="bcf37-121">The job name</span></span>

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

### <span data-ttu-id="bcf37-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="bcf37-122">-ParentObject</span></span>
<span data-ttu-id="bcf37-123">工作物件</span><span class="sxs-lookup"><span data-stu-id="bcf37-123">The job object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bcf37-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="bcf37-124">-ParentResourceId</span></span>
<span data-ttu-id="bcf37-125">工作資源識別碼</span><span class="sxs-lookup"><span data-stu-id="bcf37-125">The job resource id</span></span>

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

### <span data-ttu-id="bcf37-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcf37-126">-ResourceGroupName</span></span>
<span data-ttu-id="bcf37-127">資源組名</span><span class="sxs-lookup"><span data-stu-id="bcf37-127">The resource group name</span></span>

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

### <span data-ttu-id="bcf37-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bcf37-128">-ServerName</span></span>
<span data-ttu-id="bcf37-129">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="bcf37-129">The server name</span></span>

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

### <span data-ttu-id="bcf37-130">-等待</span><span class="sxs-lookup"><span data-stu-id="bcf37-130">-Wait</span></span>
<span data-ttu-id="bcf37-131">等待旗標，表示要等到工作執行完成</span><span class="sxs-lookup"><span data-stu-id="bcf37-131">The wait flag to indicate to wait until the job's execution is done</span></span>

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

### <span data-ttu-id="bcf37-132">-確認</span><span class="sxs-lookup"><span data-stu-id="bcf37-132">-Confirm</span></span>
<span data-ttu-id="bcf37-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="bcf37-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcf37-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcf37-134">-WhatIf</span></span>
<span data-ttu-id="bcf37-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bcf37-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcf37-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bcf37-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcf37-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcf37-137">CommonParameters</span></span>
<span data-ttu-id="bcf37-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="bcf37-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcf37-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bcf37-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcf37-140">輸入</span><span class="sxs-lookup"><span data-stu-id="bcf37-140">INPUTS</span></span>

### <span data-ttu-id="bcf37-141">Microsoft.Azure.Commands.Sql.AzureJobs.Model.AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="bcf37-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="bcf37-142">輸出</span><span class="sxs-lookup"><span data-stu-id="bcf37-142">OUTPUTS</span></span>

### <span data-ttu-id="bcf37-143">Microsoft.Azure.Commands.Sql.AzureJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="bcf37-143">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="bcf37-144">筆記</span><span class="sxs-lookup"><span data-stu-id="bcf37-144">NOTES</span></span>

## <span data-ttu-id="bcf37-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="bcf37-145">RELATED LINKS</span></span>
