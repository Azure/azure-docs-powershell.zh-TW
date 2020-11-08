---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStep.md
ms.openlocfilehash: 3a749f02854a915792a12271b2cf59b1091fef70
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137284"
---
# <span data-ttu-id="01ba3-101">Get-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="01ba3-101">Get-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="01ba3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="01ba3-102">SYNOPSIS</span></span>
<span data-ttu-id="01ba3-103">取得一或多個作業步驟</span><span class="sxs-lookup"><span data-stu-id="01ba3-103">Gets one or more job steps</span></span>

## <span data-ttu-id="01ba3-104">句法</span><span class="sxs-lookup"><span data-stu-id="01ba3-104">SYNTAX</span></span>

### <span data-ttu-id="01ba3-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="01ba3-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01ba3-106">GetVersion</span><span class="sxs-lookup"><span data-stu-id="01ba3-106">GetVersion</span></span>
```
Get-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -Version <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="01ba3-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="01ba3-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01ba3-108">GetVersionUsingJobObject</span><span class="sxs-lookup"><span data-stu-id="01ba3-108">GetVersionUsingJobObject</span></span>
```
Get-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -Name <String> -Version <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01ba3-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="01ba3-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobStep [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01ba3-110">GetVersionUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="01ba3-110">GetVersionUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobStep [-ParentResourceId] <String> -Name <String> -Version <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01ba3-111">說明</span><span class="sxs-lookup"><span data-stu-id="01ba3-111">DESCRIPTION</span></span>
<span data-ttu-id="01ba3-112">Get-AzSqlElasticJobStep Cmdlet 會從工作取得一或多個作業步驟</span><span class="sxs-lookup"><span data-stu-id="01ba3-112">The Get-AzSqlElasticJobStep cmdlet gets one or more job steps from a job</span></span>

## <span data-ttu-id="01ba3-113">示例</span><span class="sxs-lookup"><span data-stu-id="01ba3-113">EXAMPLES</span></span>

### <span data-ttu-id="01ba3-114">範例1：從工作取得作業步驟</span><span class="sxs-lookup"><span data-stu-id="01ba3-114">Example 1: Gets a job step from a job</span></span>
```powershell
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Get-AzSqlElasticJobStep -Name step1

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 1
```

<span data-ttu-id="01ba3-115">從工作取得作業步驟</span><span class="sxs-lookup"><span data-stu-id="01ba3-115">Gets a job step from a job</span></span>

## <span data-ttu-id="01ba3-116">參數</span><span class="sxs-lookup"><span data-stu-id="01ba3-116">PARAMETERS</span></span>

### <span data-ttu-id="01ba3-117">-AgentName</span><span class="sxs-lookup"><span data-stu-id="01ba3-117">-AgentName</span></span>
<span data-ttu-id="01ba3-118">代理程式名稱</span><span class="sxs-lookup"><span data-stu-id="01ba3-118">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01ba3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01ba3-119">-DefaultProfile</span></span>
<span data-ttu-id="01ba3-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="01ba3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01ba3-121">-JobName</span><span class="sxs-lookup"><span data-stu-id="01ba3-121">-JobName</span></span>
<span data-ttu-id="01ba3-122">作業名稱</span><span class="sxs-lookup"><span data-stu-id="01ba3-122">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01ba3-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="01ba3-123">-Name</span></span>
<span data-ttu-id="01ba3-124">作業步驟名稱</span><span class="sxs-lookup"><span data-stu-id="01ba3-124">The job step name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases: StepName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetVersion, GetVersionUsingJobObject, GetVersionUsingParentResourceId
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01ba3-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="01ba3-125">-ParentObject</span></span>
<span data-ttu-id="01ba3-126">作業輸入物件</span><span class="sxs-lookup"><span data-stu-id="01ba3-126">The job input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet, GetVersionUsingJobObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01ba3-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="01ba3-127">-ParentResourceId</span></span>
<span data-ttu-id="01ba3-128">作業資源識別碼</span><span class="sxs-lookup"><span data-stu-id="01ba3-128">The job resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, GetVersionUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01ba3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01ba3-129">-ResourceGroupName</span></span>
<span data-ttu-id="01ba3-130">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="01ba3-130">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01ba3-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="01ba3-131">-ServerName</span></span>
<span data-ttu-id="01ba3-132">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="01ba3-132">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01ba3-133">-版本</span><span class="sxs-lookup"><span data-stu-id="01ba3-133">-Version</span></span>
<span data-ttu-id="01ba3-134">作業步驟名稱</span><span class="sxs-lookup"><span data-stu-id="01ba3-134">The job step name</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetVersionUsingJobObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetVersionUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01ba3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01ba3-135">CommonParameters</span></span>
<span data-ttu-id="01ba3-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="01ba3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01ba3-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="01ba3-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01ba3-138">輸入</span><span class="sxs-lookup"><span data-stu-id="01ba3-138">INPUTS</span></span>

### <span data-ttu-id="01ba3-139">AzureSqlElasticJobModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="01ba3-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="01ba3-140">輸出</span><span class="sxs-lookup"><span data-stu-id="01ba3-140">OUTPUTS</span></span>

### <span data-ttu-id="01ba3-141">AzureSqlElasticJobStepModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="01ba3-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="01ba3-142">筆記</span><span class="sxs-lookup"><span data-stu-id="01ba3-142">NOTES</span></span>

## <span data-ttu-id="01ba3-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="01ba3-143">RELATED LINKS</span></span>