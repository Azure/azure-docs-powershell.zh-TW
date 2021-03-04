---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/get-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: 022ef6979ddac4fa31c0a1dae42ae04c044498dc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914358"
---
# <span data-ttu-id="5d2cc-101">Get-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="5d2cc-101">Get-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="5d2cc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5d2cc-102">SYNOPSIS</span></span>
<span data-ttu-id="5d2cc-103">獲得一或多個工作目標群組</span><span class="sxs-lookup"><span data-stu-id="5d2cc-103">Gets one or more job target groups</span></span>

## <span data-ttu-id="5d2cc-104">語法</span><span class="sxs-lookup"><span data-stu-id="5d2cc-104">SYNTAX</span></span>

### <span data-ttu-id="5d2cc-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5d2cc-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d2cc-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="5d2cc-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d2cc-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5d2cc-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d2cc-108">描述</span><span class="sxs-lookup"><span data-stu-id="5d2cc-108">DESCRIPTION</span></span>
<span data-ttu-id="5d2cc-109">Cmdlet Get-AzSqlElasticJobTargetGroup會獲得目標群組，且其為目標</span><span class="sxs-lookup"><span data-stu-id="5d2cc-109">The Get-AzSqlElasticJobTargetGroup cmdlet gets a target group and it's targets</span></span>

## <span data-ttu-id="5d2cc-110">例子</span><span class="sxs-lookup"><span data-stu-id="5d2cc-110">EXAMPLES</span></span>

### <span data-ttu-id="5d2cc-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="5d2cc-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1             (s1,db1)
```

<span data-ttu-id="5d2cc-112">獲得目標群組及其目標</span><span class="sxs-lookup"><span data-stu-id="5d2cc-112">Gets a target group and it's targets</span></span>

## <span data-ttu-id="5d2cc-113">參數</span><span class="sxs-lookup"><span data-stu-id="5d2cc-113">PARAMETERS</span></span>

### <span data-ttu-id="5d2cc-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="5d2cc-114">-AgentName</span></span>
<span data-ttu-id="5d2cc-115">代理人名稱</span><span class="sxs-lookup"><span data-stu-id="5d2cc-115">The agent name</span></span>

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

### <span data-ttu-id="5d2cc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d2cc-116">-DefaultProfile</span></span>
<span data-ttu-id="5d2cc-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5d2cc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d2cc-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="5d2cc-118">-Name</span></span>
<span data-ttu-id="5d2cc-119">目標群組名</span><span class="sxs-lookup"><span data-stu-id="5d2cc-119">The target group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d2cc-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5d2cc-120">-ParentObject</span></span>
<span data-ttu-id="5d2cc-121">代理程式物件</span><span class="sxs-lookup"><span data-stu-id="5d2cc-121">The agent object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d2cc-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="5d2cc-122">-ParentResourceId</span></span>
<span data-ttu-id="5d2cc-123">代理程式資源識別碼</span><span class="sxs-lookup"><span data-stu-id="5d2cc-123">The agent resource id</span></span>

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

### <span data-ttu-id="5d2cc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d2cc-124">-ResourceGroupName</span></span>
<span data-ttu-id="5d2cc-125">資源組名</span><span class="sxs-lookup"><span data-stu-id="5d2cc-125">The resource group name</span></span>

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

### <span data-ttu-id="5d2cc-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5d2cc-126">-ServerName</span></span>
<span data-ttu-id="5d2cc-127">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="5d2cc-127">The server name</span></span>

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

### <span data-ttu-id="5d2cc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d2cc-128">CommonParameters</span></span>
<span data-ttu-id="5d2cc-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5d2cc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d2cc-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5d2cc-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d2cc-131">輸入</span><span class="sxs-lookup"><span data-stu-id="5d2cc-131">INPUTS</span></span>

### <span data-ttu-id="5d2cc-132">Microsoft.Azure.Commands.Sql.AzureJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="5d2cc-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="5d2cc-133">輸出</span><span class="sxs-lookup"><span data-stu-id="5d2cc-133">OUTPUTS</span></span>

### <span data-ttu-id="5d2cc-134">Microsoft.Azure.Commands.Sql.AzureJobs.Model.AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="5d2cc-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="5d2cc-135">筆記</span><span class="sxs-lookup"><span data-stu-id="5d2cc-135">NOTES</span></span>

## <span data-ttu-id="5d2cc-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="5d2cc-136">RELATED LINKS</span></span>
