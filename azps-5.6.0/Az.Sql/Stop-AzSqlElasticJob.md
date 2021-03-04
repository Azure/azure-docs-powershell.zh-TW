---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/stop-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
ms.openlocfilehash: 1279366f07ce071e223aea1f7cc048403b9b4379
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912301"
---
# <span data-ttu-id="899f6-101">Stop-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="899f6-101">Stop-AzSqlElasticJob</span></span>

## <span data-ttu-id="899f6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="899f6-102">SYNOPSIS</span></span>
<span data-ttu-id="899f6-103">如果工作是工作執行識別碼，就停止工作</span><span class="sxs-lookup"><span data-stu-id="899f6-103">Stops a job given it's job execution id</span></span>

## <span data-ttu-id="899f6-104">語法</span><span class="sxs-lookup"><span data-stu-id="899f6-104">SYNTAX</span></span>

### <span data-ttu-id="899f6-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="899f6-105">DefaultSet (Default)</span></span>
```
Stop-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="899f6-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="899f6-106">ObjectSet</span></span>
```
Stop-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobExecutionModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="899f6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="899f6-107">ResourceIdSet</span></span>
```
Stop-AzSqlElasticJob [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="899f6-108">描述</span><span class="sxs-lookup"><span data-stu-id="899f6-108">DESCRIPTION</span></span>
<span data-ttu-id="899f6-109">此Stop-AzSqlElasticJob Cmdlet 會以執行中的執行來停止工作。</span><span class="sxs-lookup"><span data-stu-id="899f6-109">The Stop-AzSqlElasticJob cmdlet stops a job's with a running execution.</span></span>
<span data-ttu-id="899f6-110">會返回工作執行的目前狀態</span><span class="sxs-lookup"><span data-stu-id="899f6-110">Returns the current status of the job execution</span></span>

## <span data-ttu-id="899f6-111">例子</span><span class="sxs-lookup"><span data-stu-id="899f6-111">EXAMPLES</span></span>

### <span data-ttu-id="899f6-112">範例 1：以執行中的工作執行停止工作</span><span class="sxs-lookup"><span data-stu-id="899f6-112">Example 1: Stops a job with a running job execution</span></span>
```powershell
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId dab0ebe8-fd52-42e9-bacf-e5f27577039b
$je | Stop-AzSqlElasticJob
JobName JobExecutionId                       Lifecycle                    StartTime            EndTime
------- --------------                       ---------                    ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b WaitingForChildJobExecutions 6/1/2018 10:13:56 PM
```

<span data-ttu-id="899f6-113">停止執行中的工作，並返回目前的狀態</span><span class="sxs-lookup"><span data-stu-id="899f6-113">Stops a running job execution and returns it's current status</span></span>

### <span data-ttu-id="899f6-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="899f6-114">Example 2</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Stop-AzSqlElasticJob -AgentName agent -JobExecutionId 00000000-0000-0000-0000-000000000000 -JobName job1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="899f6-115">參數</span><span class="sxs-lookup"><span data-stu-id="899f6-115">PARAMETERS</span></span>

### <span data-ttu-id="899f6-116">-AgentName</span><span class="sxs-lookup"><span data-stu-id="899f6-116">-AgentName</span></span>
<span data-ttu-id="899f6-117">代理人名稱</span><span class="sxs-lookup"><span data-stu-id="899f6-117">The agent name</span></span>

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

### <span data-ttu-id="899f6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="899f6-118">-DefaultProfile</span></span>
<span data-ttu-id="899f6-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="899f6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="899f6-120">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="899f6-120">-JobExecutionId</span></span>
<span data-ttu-id="899f6-121">工作執行識別碼。</span><span class="sxs-lookup"><span data-stu-id="899f6-121">The job execution id.</span></span>

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

### <span data-ttu-id="899f6-122">-JobName</span><span class="sxs-lookup"><span data-stu-id="899f6-122">-JobName</span></span>
<span data-ttu-id="899f6-123">工作名稱</span><span class="sxs-lookup"><span data-stu-id="899f6-123">The job name</span></span>

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

### <span data-ttu-id="899f6-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="899f6-124">-ParentObject</span></span>
<span data-ttu-id="899f6-125">代理程式控制項資料庫物件</span><span class="sxs-lookup"><span data-stu-id="899f6-125">The Agent Control Database Object</span></span>

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

### <span data-ttu-id="899f6-126">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="899f6-126">-ParentResourceId</span></span>
<span data-ttu-id="899f6-127">工作執行資源識別碼</span><span class="sxs-lookup"><span data-stu-id="899f6-127">The job execution resource id</span></span>

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

### <span data-ttu-id="899f6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="899f6-128">-ResourceGroupName</span></span>
<span data-ttu-id="899f6-129">資源組名</span><span class="sxs-lookup"><span data-stu-id="899f6-129">The resource group name</span></span>

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

### <span data-ttu-id="899f6-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="899f6-130">-ServerName</span></span>
<span data-ttu-id="899f6-131">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="899f6-131">The server name</span></span>

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

### <span data-ttu-id="899f6-132">-確認</span><span class="sxs-lookup"><span data-stu-id="899f6-132">-Confirm</span></span>
<span data-ttu-id="899f6-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="899f6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="899f6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="899f6-134">-WhatIf</span></span>
<span data-ttu-id="899f6-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="899f6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="899f6-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="899f6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="899f6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="899f6-137">CommonParameters</span></span>
<span data-ttu-id="899f6-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="899f6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="899f6-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="899f6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="899f6-140">輸入</span><span class="sxs-lookup"><span data-stu-id="899f6-140">INPUTS</span></span>

### <span data-ttu-id="899f6-141">Microsoft.Azure.Commands.Sql.AzureJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="899f6-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="899f6-142">輸出</span><span class="sxs-lookup"><span data-stu-id="899f6-142">OUTPUTS</span></span>

### <span data-ttu-id="899f6-143">Microsoft.Azure.Commands.Sql.AzureJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="899f6-143">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="899f6-144">筆記</span><span class="sxs-lookup"><span data-stu-id="899f6-144">NOTES</span></span>

## <span data-ttu-id="899f6-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="899f6-145">RELATED LINKS</span></span>
