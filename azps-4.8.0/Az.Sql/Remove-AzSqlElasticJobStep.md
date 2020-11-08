---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
ms.openlocfilehash: b097c95f45700afabd3317a1014641da061d410d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127259"
---
# <span data-ttu-id="8dbb7-101">Remove-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="8dbb7-101">Remove-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="8dbb7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8dbb7-102">SYNOPSIS</span></span>
<span data-ttu-id="8dbb7-103">移除作業步驟</span><span class="sxs-lookup"><span data-stu-id="8dbb7-103">Removes the job step</span></span>

## <span data-ttu-id="8dbb7-104">句法</span><span class="sxs-lookup"><span data-stu-id="8dbb7-104">SYNTAX</span></span>

### <span data-ttu-id="8dbb7-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8dbb7-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8dbb7-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="8dbb7-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dbb7-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8dbb7-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8dbb7-108">說明</span><span class="sxs-lookup"><span data-stu-id="8dbb7-108">DESCRIPTION</span></span>
<span data-ttu-id="8dbb7-109">Remove-AzSqlElasticJobStep Cmdlet 會從工作中移除作業步驟</span><span class="sxs-lookup"><span data-stu-id="8dbb7-109">The Remove-AzSqlElasticJobStep cmdlet removes a job step from a job</span></span>

## <span data-ttu-id="8dbb7-110">示例</span><span class="sxs-lookup"><span data-stu-id="8dbb7-110">EXAMPLES</span></span>

### <span data-ttu-id="8dbb7-111">範例1：從工作中移除作業步驟</span><span class="sxs-lookup"><span data-stu-id="8dbb7-111">Example 1: Removes a job step from a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -Name step1
$jobStep | Remove-AzSqlElasticJobStep

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="8dbb7-112">從工作中移除作業步驟</span><span class="sxs-lookup"><span data-stu-id="8dbb7-112">Removes a job step from a job</span></span>

### <span data-ttu-id="8dbb7-113">範例2</span><span class="sxs-lookup"><span data-stu-id="8dbb7-113">Example 2</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Remove-AzSqlElasticJobStep -AgentName agent -JobName job1 -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="8dbb7-114">參數</span><span class="sxs-lookup"><span data-stu-id="8dbb7-114">PARAMETERS</span></span>

### <span data-ttu-id="8dbb7-115">-AgentName</span><span class="sxs-lookup"><span data-stu-id="8dbb7-115">-AgentName</span></span>
<span data-ttu-id="8dbb7-116">代理程式名稱</span><span class="sxs-lookup"><span data-stu-id="8dbb7-116">The agent name</span></span>

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

### <span data-ttu-id="8dbb7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dbb7-117">-DefaultProfile</span></span>
<span data-ttu-id="8dbb7-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8dbb7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8dbb7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8dbb7-119">-InputObject</span></span>
<span data-ttu-id="8dbb7-120">作業步驟輸入物件</span><span class="sxs-lookup"><span data-stu-id="8dbb7-120">The job step input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8dbb7-121">-JobName</span><span class="sxs-lookup"><span data-stu-id="8dbb7-121">-JobName</span></span>
<span data-ttu-id="8dbb7-122">作業名稱</span><span class="sxs-lookup"><span data-stu-id="8dbb7-122">The job name</span></span>

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

### <span data-ttu-id="8dbb7-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="8dbb7-123">-Name</span></span>
<span data-ttu-id="8dbb7-124">作業步驟名稱</span><span class="sxs-lookup"><span data-stu-id="8dbb7-124">The job step name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dbb7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dbb7-125">-ResourceGroupName</span></span>
<span data-ttu-id="8dbb7-126">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="8dbb7-126">The resource group name</span></span>

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

### <span data-ttu-id="8dbb7-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8dbb7-127">-ResourceId</span></span>
<span data-ttu-id="8dbb7-128">作業步驟資源識別碼</span><span class="sxs-lookup"><span data-stu-id="8dbb7-128">The job step resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dbb7-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8dbb7-129">-ServerName</span></span>
<span data-ttu-id="8dbb7-130">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="8dbb7-130">The server name</span></span>

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

### <span data-ttu-id="8dbb7-131">-確認</span><span class="sxs-lookup"><span data-stu-id="8dbb7-131">-Confirm</span></span>
<span data-ttu-id="8dbb7-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8dbb7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dbb7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dbb7-133">-WhatIf</span></span>
<span data-ttu-id="8dbb7-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8dbb7-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8dbb7-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8dbb7-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dbb7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dbb7-136">CommonParameters</span></span>
<span data-ttu-id="8dbb7-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8dbb7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dbb7-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8dbb7-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dbb7-139">輸入</span><span class="sxs-lookup"><span data-stu-id="8dbb7-139">INPUTS</span></span>

### <span data-ttu-id="8dbb7-140">AzureSqlElasticJobStepModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="8dbb7-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="8dbb7-141">輸出</span><span class="sxs-lookup"><span data-stu-id="8dbb7-141">OUTPUTS</span></span>

### <span data-ttu-id="8dbb7-142">AzureSqlElasticJobStepModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="8dbb7-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="8dbb7-143">筆記</span><span class="sxs-lookup"><span data-stu-id="8dbb7-143">NOTES</span></span>

## <span data-ttu-id="8dbb7-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="8dbb7-144">RELATED LINKS</span></span>