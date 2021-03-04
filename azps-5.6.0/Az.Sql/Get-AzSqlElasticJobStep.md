---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/get-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStep.md
ms.openlocfilehash: d70a0b6abd31d4104301e877fb21bf1d0589a24f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914369"
---
# <span data-ttu-id="ca5ef-101">Get-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="ca5ef-101">Get-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="ca5ef-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ca5ef-102">SYNOPSIS</span></span>
<span data-ttu-id="ca5ef-103">獲得一或多個工作步驟</span><span class="sxs-lookup"><span data-stu-id="ca5ef-103">Gets one or more job steps</span></span>

## <span data-ttu-id="ca5ef-104">語法</span><span class="sxs-lookup"><span data-stu-id="ca5ef-104">SYNTAX</span></span>

### <span data-ttu-id="ca5ef-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ca5ef-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca5ef-106">GetVersion</span><span class="sxs-lookup"><span data-stu-id="ca5ef-106">GetVersion</span></span>
```
Get-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -Version <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ca5ef-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="ca5ef-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca5ef-108">GetVersionUsingJobObject</span><span class="sxs-lookup"><span data-stu-id="ca5ef-108">GetVersionUsingJobObject</span></span>
```
Get-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -Name <String> -Version <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca5ef-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ca5ef-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobStep [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca5ef-110">GetVersionUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ca5ef-110">GetVersionUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobStep [-ParentResourceId] <String> -Name <String> -Version <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca5ef-111">描述</span><span class="sxs-lookup"><span data-stu-id="ca5ef-111">DESCRIPTION</span></span>
<span data-ttu-id="ca5ef-112">Cmdlet Get-AzSqlElasticJobStep從工作獲得一或多個工作步驟</span><span class="sxs-lookup"><span data-stu-id="ca5ef-112">The Get-AzSqlElasticJobStep cmdlet gets one or more job steps from a job</span></span>

## <span data-ttu-id="ca5ef-113">例子</span><span class="sxs-lookup"><span data-stu-id="ca5ef-113">EXAMPLES</span></span>

### <span data-ttu-id="ca5ef-114">範例 1：從工作獲得工作步驟</span><span class="sxs-lookup"><span data-stu-id="ca5ef-114">Example 1: Gets a job step from a job</span></span>
```powershell
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Get-AzSqlElasticJobStep -Name step1

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 1
```

<span data-ttu-id="ca5ef-115">從工作獲得工作步驟</span><span class="sxs-lookup"><span data-stu-id="ca5ef-115">Gets a job step from a job</span></span>

## <span data-ttu-id="ca5ef-116">參數</span><span class="sxs-lookup"><span data-stu-id="ca5ef-116">PARAMETERS</span></span>

### <span data-ttu-id="ca5ef-117">-AgentName</span><span class="sxs-lookup"><span data-stu-id="ca5ef-117">-AgentName</span></span>
<span data-ttu-id="ca5ef-118">代理人名稱</span><span class="sxs-lookup"><span data-stu-id="ca5ef-118">The agent name</span></span>

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

### <span data-ttu-id="ca5ef-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca5ef-119">-DefaultProfile</span></span>
<span data-ttu-id="ca5ef-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ca5ef-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca5ef-121">-JobName</span><span class="sxs-lookup"><span data-stu-id="ca5ef-121">-JobName</span></span>
<span data-ttu-id="ca5ef-122">工作名稱</span><span class="sxs-lookup"><span data-stu-id="ca5ef-122">The job name</span></span>

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

### <span data-ttu-id="ca5ef-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="ca5ef-123">-Name</span></span>
<span data-ttu-id="ca5ef-124">工作步驟名稱</span><span class="sxs-lookup"><span data-stu-id="ca5ef-124">The job step name</span></span>

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

### <span data-ttu-id="ca5ef-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ca5ef-125">-ParentObject</span></span>
<span data-ttu-id="ca5ef-126">工作輸入物件</span><span class="sxs-lookup"><span data-stu-id="ca5ef-126">The job input object</span></span>

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

### <span data-ttu-id="ca5ef-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ca5ef-127">-ParentResourceId</span></span>
<span data-ttu-id="ca5ef-128">工作資源識別碼</span><span class="sxs-lookup"><span data-stu-id="ca5ef-128">The job resource id</span></span>

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

### <span data-ttu-id="ca5ef-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca5ef-129">-ResourceGroupName</span></span>
<span data-ttu-id="ca5ef-130">資源組名</span><span class="sxs-lookup"><span data-stu-id="ca5ef-130">The resource group name</span></span>

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

### <span data-ttu-id="ca5ef-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ca5ef-131">-ServerName</span></span>
<span data-ttu-id="ca5ef-132">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="ca5ef-132">The server name</span></span>

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

### <span data-ttu-id="ca5ef-133">-版本</span><span class="sxs-lookup"><span data-stu-id="ca5ef-133">-Version</span></span>
<span data-ttu-id="ca5ef-134">工作步驟名稱</span><span class="sxs-lookup"><span data-stu-id="ca5ef-134">The job step name</span></span>

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

### <span data-ttu-id="ca5ef-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca5ef-135">CommonParameters</span></span>
<span data-ttu-id="ca5ef-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ca5ef-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca5ef-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ca5ef-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca5ef-138">輸入</span><span class="sxs-lookup"><span data-stu-id="ca5ef-138">INPUTS</span></span>

### <span data-ttu-id="ca5ef-139">Microsoft.Azure.Commands.Sql.AzureJobs.Model.AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="ca5ef-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="ca5ef-140">輸出</span><span class="sxs-lookup"><span data-stu-id="ca5ef-140">OUTPUTS</span></span>

### <span data-ttu-id="ca5ef-141">Microsoft.Azure.Commands.Sql.AzureJobs.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="ca5ef-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="ca5ef-142">筆記</span><span class="sxs-lookup"><span data-stu-id="ca5ef-142">NOTES</span></span>

## <span data-ttu-id="ca5ef-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="ca5ef-143">RELATED LINKS</span></span>
