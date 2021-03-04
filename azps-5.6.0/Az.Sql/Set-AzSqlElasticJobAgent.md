---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/set-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
ms.openlocfilehash: c65c7a74d4b2edfcddf8b4e08ee3e538c32d31df
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910581"
---
# <span data-ttu-id="d9592-101">Set-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="d9592-101">Set-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="d9592-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d9592-102">SYNOPSIS</span></span>
<span data-ttu-id="d9592-103">更新彈性工作代理程式</span><span class="sxs-lookup"><span data-stu-id="d9592-103">Updates an elastic job agent</span></span>

## <span data-ttu-id="d9592-104">語法</span><span class="sxs-lookup"><span data-stu-id="d9592-104">SYNTAX</span></span>

### <span data-ttu-id="d9592-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d9592-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9592-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="d9592-106">ObjectSet</span></span>
```
Set-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9592-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d9592-107">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9592-108">描述</span><span class="sxs-lookup"><span data-stu-id="d9592-108">DESCRIPTION</span></span>
<span data-ttu-id="d9592-109">Cmdlet Set-AzSqlElasticJobAgent更新了一個彈性工作代理程式</span><span class="sxs-lookup"><span data-stu-id="d9592-109">The Set-AzSqlElasticJobAgent cmdlet updates an Elastic Job agents</span></span>

## <span data-ttu-id="d9592-110">例子</span><span class="sxs-lookup"><span data-stu-id="d9592-110">EXAMPLES</span></span>

### <span data-ttu-id="d9592-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="d9592-111">Example 1</span></span>
```
PS C:\> Set-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent -Tag @{ Octopus = "Agent" }

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="d9592-112">更新彈性工作代理程式</span><span class="sxs-lookup"><span data-stu-id="d9592-112">Updates an Elastic Job agent</span></span>

## <span data-ttu-id="d9592-113">參數</span><span class="sxs-lookup"><span data-stu-id="d9592-113">PARAMETERS</span></span>

### <span data-ttu-id="d9592-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9592-114">-DefaultProfile</span></span>
<span data-ttu-id="d9592-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d9592-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9592-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9592-116">-InputObject</span></span>
<span data-ttu-id="d9592-117">代理程式輸入物件</span><span class="sxs-lookup"><span data-stu-id="d9592-117">The agent input object</span></span>

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

### <span data-ttu-id="d9592-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="d9592-118">-Name</span></span>
<span data-ttu-id="d9592-119">代理人名稱</span><span class="sxs-lookup"><span data-stu-id="d9592-119">The agent name</span></span>

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

### <span data-ttu-id="d9592-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9592-120">-ResourceGroupName</span></span>
<span data-ttu-id="d9592-121">資源組名</span><span class="sxs-lookup"><span data-stu-id="d9592-121">The resource group name</span></span>

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

### <span data-ttu-id="d9592-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9592-122">-ResourceId</span></span>
<span data-ttu-id="d9592-123">代理程式資源識別碼</span><span class="sxs-lookup"><span data-stu-id="d9592-123">The agent resource id</span></span>

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

### <span data-ttu-id="d9592-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d9592-124">-ServerName</span></span>
<span data-ttu-id="d9592-125">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="d9592-125">The server name</span></span>

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

### <span data-ttu-id="d9592-126">-標記</span><span class="sxs-lookup"><span data-stu-id="d9592-126">-Tag</span></span>
<span data-ttu-id="d9592-127">與 Azure SQL 資料庫代理程式建立關聯的標記</span><span class="sxs-lookup"><span data-stu-id="d9592-127">The tags to associate with the Azure SQL Database Agent</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9592-128">-確認</span><span class="sxs-lookup"><span data-stu-id="d9592-128">-Confirm</span></span>
<span data-ttu-id="d9592-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d9592-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9592-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9592-130">-WhatIf</span></span>
<span data-ttu-id="d9592-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d9592-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9592-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d9592-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9592-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9592-133">CommonParameters</span></span>
<span data-ttu-id="d9592-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d9592-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9592-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d9592-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9592-136">輸入</span><span class="sxs-lookup"><span data-stu-id="d9592-136">INPUTS</span></span>

### <span data-ttu-id="d9592-137">Microsoft.Azure.Commands.Sql.AzureJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="d9592-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="d9592-138">輸出</span><span class="sxs-lookup"><span data-stu-id="d9592-138">OUTPUTS</span></span>

### <span data-ttu-id="d9592-139">Microsoft.Azure.Commands.Sql.AzureJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="d9592-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="d9592-140">筆記</span><span class="sxs-lookup"><span data-stu-id="d9592-140">NOTES</span></span>

## <span data-ttu-id="d9592-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="d9592-141">RELATED LINKS</span></span>
