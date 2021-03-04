---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/remove-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
ms.openlocfilehash: 788817dd9ca344501dc25bad48b71b7e24b653d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902718"
---
# <span data-ttu-id="45c60-101">Remove-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="45c60-101">Remove-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="45c60-102">簡介</span><span class="sxs-lookup"><span data-stu-id="45c60-102">SYNOPSIS</span></span>
<span data-ttu-id="45c60-103">移除工作步驟</span><span class="sxs-lookup"><span data-stu-id="45c60-103">Removes the job step</span></span>

## <span data-ttu-id="45c60-104">語法</span><span class="sxs-lookup"><span data-stu-id="45c60-104">SYNTAX</span></span>

### <span data-ttu-id="45c60-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="45c60-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="45c60-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="45c60-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45c60-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="45c60-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45c60-108">描述</span><span class="sxs-lookup"><span data-stu-id="45c60-108">DESCRIPTION</span></span>
<span data-ttu-id="45c60-109">Cmdlet Remove-AzSqlElasticJobStep移除工作步驟</span><span class="sxs-lookup"><span data-stu-id="45c60-109">The Remove-AzSqlElasticJobStep cmdlet removes a job step from a job</span></span>

## <span data-ttu-id="45c60-110">例子</span><span class="sxs-lookup"><span data-stu-id="45c60-110">EXAMPLES</span></span>

### <span data-ttu-id="45c60-111">範例 1：從工作移除工作步驟</span><span class="sxs-lookup"><span data-stu-id="45c60-111">Example 1: Removes a job step from a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -Name step1
$jobStep | Remove-AzSqlElasticJobStep

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="45c60-112">從工作移除工作步驟</span><span class="sxs-lookup"><span data-stu-id="45c60-112">Removes a job step from a job</span></span>

### <span data-ttu-id="45c60-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="45c60-113">Example 2</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Remove-AzSqlElasticJobStep -AgentName agent -JobName job1 -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="45c60-114">參數</span><span class="sxs-lookup"><span data-stu-id="45c60-114">PARAMETERS</span></span>

### <span data-ttu-id="45c60-115">-AgentName</span><span class="sxs-lookup"><span data-stu-id="45c60-115">-AgentName</span></span>
<span data-ttu-id="45c60-116">代理人名稱</span><span class="sxs-lookup"><span data-stu-id="45c60-116">The agent name</span></span>

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

### <span data-ttu-id="45c60-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45c60-117">-DefaultProfile</span></span>
<span data-ttu-id="45c60-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="45c60-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45c60-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45c60-119">-InputObject</span></span>
<span data-ttu-id="45c60-120">工作步驟輸入物件</span><span class="sxs-lookup"><span data-stu-id="45c60-120">The job step input object</span></span>

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

### <span data-ttu-id="45c60-121">-JobName</span><span class="sxs-lookup"><span data-stu-id="45c60-121">-JobName</span></span>
<span data-ttu-id="45c60-122">工作名稱</span><span class="sxs-lookup"><span data-stu-id="45c60-122">The job name</span></span>

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

### <span data-ttu-id="45c60-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="45c60-123">-Name</span></span>
<span data-ttu-id="45c60-124">工作步驟名稱</span><span class="sxs-lookup"><span data-stu-id="45c60-124">The job step name</span></span>

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

### <span data-ttu-id="45c60-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45c60-125">-ResourceGroupName</span></span>
<span data-ttu-id="45c60-126">資源組名</span><span class="sxs-lookup"><span data-stu-id="45c60-126">The resource group name</span></span>

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

### <span data-ttu-id="45c60-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45c60-127">-ResourceId</span></span>
<span data-ttu-id="45c60-128">工作步驟資源識別碼</span><span class="sxs-lookup"><span data-stu-id="45c60-128">The job step resource id</span></span>

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

### <span data-ttu-id="45c60-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="45c60-129">-ServerName</span></span>
<span data-ttu-id="45c60-130">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="45c60-130">The server name</span></span>

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

### <span data-ttu-id="45c60-131">-確認</span><span class="sxs-lookup"><span data-stu-id="45c60-131">-Confirm</span></span>
<span data-ttu-id="45c60-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="45c60-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45c60-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45c60-133">-WhatIf</span></span>
<span data-ttu-id="45c60-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="45c60-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45c60-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="45c60-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45c60-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45c60-136">CommonParameters</span></span>
<span data-ttu-id="45c60-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="45c60-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45c60-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="45c60-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45c60-139">輸入</span><span class="sxs-lookup"><span data-stu-id="45c60-139">INPUTS</span></span>

### <span data-ttu-id="45c60-140">Microsoft.Azure.Commands.Sql.AzureJobs.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="45c60-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="45c60-141">輸出</span><span class="sxs-lookup"><span data-stu-id="45c60-141">OUTPUTS</span></span>

### <span data-ttu-id="45c60-142">Microsoft.Azure.Commands.Sql.AzureJobs.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="45c60-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="45c60-143">筆記</span><span class="sxs-lookup"><span data-stu-id="45c60-143">NOTES</span></span>

## <span data-ttu-id="45c60-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="45c60-144">RELATED LINKS</span></span>
