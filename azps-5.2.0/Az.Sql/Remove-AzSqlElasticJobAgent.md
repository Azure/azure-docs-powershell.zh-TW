---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
ms.openlocfilehash: 1352ef72ffc6fd757b4019e217ecb439495ebb44
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280796"
---
# <span data-ttu-id="2a307-101">Remove-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="2a307-101">Remove-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="2a307-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2a307-102">SYNOPSIS</span></span>
<span data-ttu-id="2a307-103">移除彈性作業代理程式</span><span class="sxs-lookup"><span data-stu-id="2a307-103">Removes the elastic job agent</span></span>

## <span data-ttu-id="2a307-104">句法</span><span class="sxs-lookup"><span data-stu-id="2a307-104">SYNTAX</span></span>

### <span data-ttu-id="2a307-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2a307-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a307-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="2a307-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a307-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2a307-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a307-108">說明</span><span class="sxs-lookup"><span data-stu-id="2a307-108">DESCRIPTION</span></span>
<span data-ttu-id="2a307-109">Remove-AzSqlElasticJobAgent Cmdlet 會移除彈性作業代理程式</span><span class="sxs-lookup"><span data-stu-id="2a307-109">The Remove-AzSqlElasticJobAgent cmdlet removes an Elastic Job agent</span></span>

## <span data-ttu-id="2a307-110">示例</span><span class="sxs-lookup"><span data-stu-id="2a307-110">EXAMPLES</span></span>

### <span data-ttu-id="2a307-111">範例1</span><span class="sxs-lookup"><span data-stu-id="2a307-111">Example 1</span></span>
```
PS C:\> Remove-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="2a307-112">移除彈性作業代理程式</span><span class="sxs-lookup"><span data-stu-id="2a307-112">Removes an Elastic Job agent</span></span>

## <span data-ttu-id="2a307-113">參數</span><span class="sxs-lookup"><span data-stu-id="2a307-113">PARAMETERS</span></span>

### <span data-ttu-id="2a307-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a307-114">-DefaultProfile</span></span>
<span data-ttu-id="2a307-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2a307-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a307-116">-Force</span><span class="sxs-lookup"><span data-stu-id="2a307-116">-Force</span></span>
<span data-ttu-id="2a307-117">略過確認訊息以執行動作</span><span class="sxs-lookup"><span data-stu-id="2a307-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="2a307-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a307-118">-InputObject</span></span>
<span data-ttu-id="2a307-119">Agent 物件</span><span class="sxs-lookup"><span data-stu-id="2a307-119">The agent object</span></span>

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

### <span data-ttu-id="2a307-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="2a307-120">-Name</span></span>
<span data-ttu-id="2a307-121">代理程式名稱</span><span class="sxs-lookup"><span data-stu-id="2a307-121">The agent name</span></span>

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

### <span data-ttu-id="2a307-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a307-122">-ResourceGroupName</span></span>
<span data-ttu-id="2a307-123">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="2a307-123">The resource group name</span></span>

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

### <span data-ttu-id="2a307-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a307-124">-ResourceId</span></span>
<span data-ttu-id="2a307-125">Agent 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="2a307-125">The agent resource id</span></span>

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

### <span data-ttu-id="2a307-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2a307-126">-ServerName</span></span>
<span data-ttu-id="2a307-127">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="2a307-127">The server name</span></span>

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

### <span data-ttu-id="2a307-128">-確認</span><span class="sxs-lookup"><span data-stu-id="2a307-128">-Confirm</span></span>
<span data-ttu-id="2a307-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2a307-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a307-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a307-130">-WhatIf</span></span>
<span data-ttu-id="2a307-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2a307-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a307-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2a307-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a307-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a307-133">CommonParameters</span></span>
<span data-ttu-id="2a307-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2a307-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a307-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2a307-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a307-136">輸入</span><span class="sxs-lookup"><span data-stu-id="2a307-136">INPUTS</span></span>

### <span data-ttu-id="2a307-137">AzureSqlElasticJobAgentModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="2a307-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="2a307-138">輸出</span><span class="sxs-lookup"><span data-stu-id="2a307-138">OUTPUTS</span></span>

### <span data-ttu-id="2a307-139">AzureSqlElasticJobAgentModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="2a307-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="2a307-140">筆記</span><span class="sxs-lookup"><span data-stu-id="2a307-140">NOTES</span></span>

## <span data-ttu-id="2a307-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="2a307-141">RELATED LINKS</span></span>
