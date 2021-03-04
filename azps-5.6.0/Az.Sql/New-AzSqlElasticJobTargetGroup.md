---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/new-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: 9a80504f1b3aff814d50b5b4aba98b488d1e55b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906477"
---
# <span data-ttu-id="96858-101">New-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="96858-101">New-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="96858-102">簡介</span><span class="sxs-lookup"><span data-stu-id="96858-102">SYNOPSIS</span></span>
<span data-ttu-id="96858-103">建立新目標群組</span><span class="sxs-lookup"><span data-stu-id="96858-103">Creates a new target group</span></span>

## <span data-ttu-id="96858-104">語法</span><span class="sxs-lookup"><span data-stu-id="96858-104">SYNTAX</span></span>

### <span data-ttu-id="96858-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="96858-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96858-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="96858-106">ObjectSet</span></span>
```
New-AzSqlElasticJobTargetGroup [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96858-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="96858-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobTargetGroup [-ParentResourceId] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96858-108">描述</span><span class="sxs-lookup"><span data-stu-id="96858-108">DESCRIPTION</span></span>
<span data-ttu-id="96858-109">Cmdlet New-AzSqlElasticJobTargetGroup建立新目標群組</span><span class="sxs-lookup"><span data-stu-id="96858-109">The New-AzSqlElasticJobTargetGroup cmdlet creates a new target group</span></span>

## <span data-ttu-id="96858-110">例子</span><span class="sxs-lookup"><span data-stu-id="96858-110">EXAMPLES</span></span>

### <span data-ttu-id="96858-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="96858-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1
```

<span data-ttu-id="96858-112">建立空白的目標群組</span><span class="sxs-lookup"><span data-stu-id="96858-112">Creates an empty target group</span></span>

## <span data-ttu-id="96858-113">參數</span><span class="sxs-lookup"><span data-stu-id="96858-113">PARAMETERS</span></span>

### <span data-ttu-id="96858-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="96858-114">-AgentName</span></span>
<span data-ttu-id="96858-115">代理人名稱</span><span class="sxs-lookup"><span data-stu-id="96858-115">The agent name</span></span>

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

### <span data-ttu-id="96858-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96858-116">-DefaultProfile</span></span>
<span data-ttu-id="96858-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="96858-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96858-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="96858-118">-Name</span></span>
<span data-ttu-id="96858-119">目標群組名</span><span class="sxs-lookup"><span data-stu-id="96858-119">The target group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96858-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="96858-120">-ParentObject</span></span>
<span data-ttu-id="96858-121">代理程式輸入物件</span><span class="sxs-lookup"><span data-stu-id="96858-121">The agent input object</span></span>

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

### <span data-ttu-id="96858-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="96858-122">-ParentResourceId</span></span>
<span data-ttu-id="96858-123">代理程式資源識別碼</span><span class="sxs-lookup"><span data-stu-id="96858-123">The agent resource id</span></span>

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

### <span data-ttu-id="96858-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96858-124">-ResourceGroupName</span></span>
<span data-ttu-id="96858-125">資源組名</span><span class="sxs-lookup"><span data-stu-id="96858-125">The resource group name</span></span>

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

### <span data-ttu-id="96858-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="96858-126">-ServerName</span></span>
<span data-ttu-id="96858-127">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="96858-127">The server name</span></span>

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

### <span data-ttu-id="96858-128">-確認</span><span class="sxs-lookup"><span data-stu-id="96858-128">-Confirm</span></span>
<span data-ttu-id="96858-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="96858-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96858-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96858-130">-WhatIf</span></span>
<span data-ttu-id="96858-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="96858-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96858-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="96858-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96858-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96858-133">CommonParameters</span></span>
<span data-ttu-id="96858-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="96858-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96858-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="96858-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96858-136">輸入</span><span class="sxs-lookup"><span data-stu-id="96858-136">INPUTS</span></span>

### <span data-ttu-id="96858-137">Microsoft.Azure.Commands.Sql.AzureJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="96858-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="96858-138">輸出</span><span class="sxs-lookup"><span data-stu-id="96858-138">OUTPUTS</span></span>

### <span data-ttu-id="96858-139">Microsoft.Azure.Commands.Sql.AzureJobs.Model.AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="96858-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="96858-140">筆記</span><span class="sxs-lookup"><span data-stu-id="96858-140">NOTES</span></span>

## <span data-ttu-id="96858-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="96858-141">RELATED LINKS</span></span>
