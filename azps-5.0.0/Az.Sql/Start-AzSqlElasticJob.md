---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/start-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlElasticJob.md
ms.openlocfilehash: 5ab6b7e6e77fcfcf470c67bfdd8e300ddc4343ea
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285767"
---
# <span data-ttu-id="36f36-101">Start-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="36f36-101">Start-AzSqlElasticJob</span></span>

## <span data-ttu-id="36f36-102">摘要</span><span class="sxs-lookup"><span data-stu-id="36f36-102">SYNOPSIS</span></span>
<span data-ttu-id="36f36-103">啟動作業，然後返回可輪詢以查看其狀態的作業執行 id。</span><span class="sxs-lookup"><span data-stu-id="36f36-103">Starts a job, returning a job execution id that can be polled to view it's status</span></span>

## <span data-ttu-id="36f36-104">句法</span><span class="sxs-lookup"><span data-stu-id="36f36-104">SYNTAX</span></span>

### <span data-ttu-id="36f36-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="36f36-105">DefaultSet (Default)</span></span>
```
Start-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> [-Wait] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="36f36-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="36f36-106">ObjectSet</span></span>
```
Start-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobModel> [-Wait] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36f36-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="36f36-107">ResourceIdSet</span></span>
```
Start-AzSqlElasticJob [-ParentResourceId] <String> [-Wait] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36f36-108">說明</span><span class="sxs-lookup"><span data-stu-id="36f36-108">DESCRIPTION</span></span>
<span data-ttu-id="36f36-109">Start-AzSqlElasticJob Cmdlet 會啟動作業，返回新的作業執行</span><span class="sxs-lookup"><span data-stu-id="36f36-109">The Start-AzSqlElasticJob cmdlet starts a job returning a new job execution</span></span>

## <span data-ttu-id="36f36-110">示例</span><span class="sxs-lookup"><span data-stu-id="36f36-110">EXAMPLES</span></span>

### <span data-ttu-id="36f36-111">範例 1-開始傳回新工作執行作業</span><span class="sxs-lookup"><span data-stu-id="36f36-111">Example 1 - Starts a job returning a new job execution</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Start-AzSqlElasticJob

JobName JobExecutionId                       Lifecycle StartTime EndTime
------- --------------                       --------- --------- -------
job1    b93b3a90-987b-4565-b3d3-5fa1751fa9bc Created
```

<span data-ttu-id="36f36-112">開始作業，返回新工作執行</span><span class="sxs-lookup"><span data-stu-id="36f36-112">Starts a job returning a new job execution</span></span>

## <span data-ttu-id="36f36-113">參數</span><span class="sxs-lookup"><span data-stu-id="36f36-113">PARAMETERS</span></span>

### <span data-ttu-id="36f36-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="36f36-114">-AgentName</span></span>
<span data-ttu-id="36f36-115">代理程式名稱</span><span class="sxs-lookup"><span data-stu-id="36f36-115">The agent name</span></span>

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

### <span data-ttu-id="36f36-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="36f36-116">-AsJob</span></span>
<span data-ttu-id="36f36-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36f36-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="36f36-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36f36-118">-DefaultProfile</span></span>
<span data-ttu-id="36f36-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="36f36-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36f36-120">-JobName</span><span class="sxs-lookup"><span data-stu-id="36f36-120">-JobName</span></span>
<span data-ttu-id="36f36-121">作業名稱</span><span class="sxs-lookup"><span data-stu-id="36f36-121">The job name</span></span>

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

### <span data-ttu-id="36f36-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="36f36-122">-ParentObject</span></span>
<span data-ttu-id="36f36-123">工作物件</span><span class="sxs-lookup"><span data-stu-id="36f36-123">The job object</span></span>

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

### <span data-ttu-id="36f36-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="36f36-124">-ParentResourceId</span></span>
<span data-ttu-id="36f36-125">作業資源識別碼</span><span class="sxs-lookup"><span data-stu-id="36f36-125">The job resource id</span></span>

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

### <span data-ttu-id="36f36-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36f36-126">-ResourceGroupName</span></span>
<span data-ttu-id="36f36-127">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="36f36-127">The resource group name</span></span>

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

### <span data-ttu-id="36f36-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="36f36-128">-ServerName</span></span>
<span data-ttu-id="36f36-129">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="36f36-129">The server name</span></span>

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

### <span data-ttu-id="36f36-130">-稍候</span><span class="sxs-lookup"><span data-stu-id="36f36-130">-Wait</span></span>
<span data-ttu-id="36f36-131">在作業執行完成前要等待的等待標誌</span><span class="sxs-lookup"><span data-stu-id="36f36-131">The wait flag to indicate to wait until the job's execution is done</span></span>

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

### <span data-ttu-id="36f36-132">-確認</span><span class="sxs-lookup"><span data-stu-id="36f36-132">-Confirm</span></span>
<span data-ttu-id="36f36-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="36f36-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36f36-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36f36-134">-WhatIf</span></span>
<span data-ttu-id="36f36-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="36f36-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36f36-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="36f36-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36f36-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36f36-137">CommonParameters</span></span>
<span data-ttu-id="36f36-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="36f36-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36f36-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="36f36-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36f36-140">輸入</span><span class="sxs-lookup"><span data-stu-id="36f36-140">INPUTS</span></span>

### <span data-ttu-id="36f36-141">AzureSqlElasticJobModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="36f36-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="36f36-142">輸出</span><span class="sxs-lookup"><span data-stu-id="36f36-142">OUTPUTS</span></span>

### <span data-ttu-id="36f36-143">AzureSqlElasticJobExecutionModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="36f36-143">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="36f36-144">筆記</span><span class="sxs-lookup"><span data-stu-id="36f36-144">NOTES</span></span>

## <span data-ttu-id="36f36-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="36f36-145">RELATED LINKS</span></span>
