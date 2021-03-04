---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/remove-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
ms.openlocfilehash: 3c6a92a205aef19b1e4cef4842de4cf0414c2397
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903394"
---
# <span data-ttu-id="a3f70-101">Remove-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="a3f70-101">Remove-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="a3f70-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a3f70-102">SYNOPSIS</span></span>
<span data-ttu-id="a3f70-103">移除彈性工作代理程式</span><span class="sxs-lookup"><span data-stu-id="a3f70-103">Removes the elastic job agent</span></span>

## <span data-ttu-id="a3f70-104">語法</span><span class="sxs-lookup"><span data-stu-id="a3f70-104">SYNTAX</span></span>

### <span data-ttu-id="a3f70-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a3f70-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3f70-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="a3f70-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3f70-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a3f70-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3f70-108">描述</span><span class="sxs-lookup"><span data-stu-id="a3f70-108">DESCRIPTION</span></span>
<span data-ttu-id="a3f70-109">Cmdlet Remove-AzSqlElasticJobAgent移除了一個彈性工作代理程式</span><span class="sxs-lookup"><span data-stu-id="a3f70-109">The Remove-AzSqlElasticJobAgent cmdlet removes an Elastic Job agent</span></span>

## <span data-ttu-id="a3f70-110">例子</span><span class="sxs-lookup"><span data-stu-id="a3f70-110">EXAMPLES</span></span>

### <span data-ttu-id="a3f70-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="a3f70-111">Example 1</span></span>
```
PS C:\> Remove-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="a3f70-112">移除彈性工作代理程式</span><span class="sxs-lookup"><span data-stu-id="a3f70-112">Removes an Elastic Job agent</span></span>

## <span data-ttu-id="a3f70-113">參數</span><span class="sxs-lookup"><span data-stu-id="a3f70-113">PARAMETERS</span></span>

### <span data-ttu-id="a3f70-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3f70-114">-DefaultProfile</span></span>
<span data-ttu-id="a3f70-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a3f70-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3f70-116">-強制</span><span class="sxs-lookup"><span data-stu-id="a3f70-116">-Force</span></span>
<span data-ttu-id="a3f70-117">跳過執行動作的確認訊息</span><span class="sxs-lookup"><span data-stu-id="a3f70-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="a3f70-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3f70-118">-InputObject</span></span>
<span data-ttu-id="a3f70-119">代理程式物件</span><span class="sxs-lookup"><span data-stu-id="a3f70-119">The agent object</span></span>

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

### <span data-ttu-id="a3f70-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="a3f70-120">-Name</span></span>
<span data-ttu-id="a3f70-121">代理人名稱</span><span class="sxs-lookup"><span data-stu-id="a3f70-121">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: AgentName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3f70-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3f70-122">-ResourceGroupName</span></span>
<span data-ttu-id="a3f70-123">資源組名</span><span class="sxs-lookup"><span data-stu-id="a3f70-123">The resource group name</span></span>

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

### <span data-ttu-id="a3f70-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3f70-124">-ResourceId</span></span>
<span data-ttu-id="a3f70-125">代理程式資源識別碼</span><span class="sxs-lookup"><span data-stu-id="a3f70-125">The agent resource id</span></span>

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

### <span data-ttu-id="a3f70-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a3f70-126">-ServerName</span></span>
<span data-ttu-id="a3f70-127">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="a3f70-127">The server name</span></span>

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

### <span data-ttu-id="a3f70-128">-確認</span><span class="sxs-lookup"><span data-stu-id="a3f70-128">-Confirm</span></span>
<span data-ttu-id="a3f70-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a3f70-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3f70-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3f70-130">-WhatIf</span></span>
<span data-ttu-id="a3f70-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a3f70-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3f70-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a3f70-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3f70-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3f70-133">CommonParameters</span></span>
<span data-ttu-id="a3f70-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a3f70-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3f70-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a3f70-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3f70-136">輸入</span><span class="sxs-lookup"><span data-stu-id="a3f70-136">INPUTS</span></span>

### <span data-ttu-id="a3f70-137">Microsoft.Azure.Commands.Sql.AzureJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="a3f70-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="a3f70-138">輸出</span><span class="sxs-lookup"><span data-stu-id="a3f70-138">OUTPUTS</span></span>

### <span data-ttu-id="a3f70-139">Microsoft.Azure.Commands.Sql.AzureJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="a3f70-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="a3f70-140">筆記</span><span class="sxs-lookup"><span data-stu-id="a3f70-140">NOTES</span></span>

## <span data-ttu-id="a3f70-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="a3f70-141">RELATED LINKS</span></span>
