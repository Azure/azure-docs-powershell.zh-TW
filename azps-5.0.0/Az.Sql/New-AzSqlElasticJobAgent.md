---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobAgent.md
ms.openlocfilehash: f00c2e9cb7b9d0d35efdf99a6f81f24488dd8387
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138122"
---
# <span data-ttu-id="867f3-101">New-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="867f3-101">New-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="867f3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="867f3-102">SYNOPSIS</span></span>
<span data-ttu-id="867f3-103">建立新的彈性作業代理程式</span><span class="sxs-lookup"><span data-stu-id="867f3-103">Creates a new elastic job agent</span></span>

## <span data-ttu-id="867f3-104">句法</span><span class="sxs-lookup"><span data-stu-id="867f3-104">SYNTAX</span></span>

### <span data-ttu-id="867f3-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="867f3-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-Name] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="867f3-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="867f3-106">ObjectSet</span></span>
```
New-AzSqlElasticJobAgent [-DatabaseObject] <AzureSqlDatabaseModel> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="867f3-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="867f3-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobAgent [-DatabaseResourceId] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="867f3-108">說明</span><span class="sxs-lookup"><span data-stu-id="867f3-108">DESCRIPTION</span></span>
<span data-ttu-id="867f3-109">New-AzSqlElasticJobAgent Cmdlet 會建立新的彈性作業代理程式</span><span class="sxs-lookup"><span data-stu-id="867f3-109">The New-AzSqlElasticJobAgent cmdlet creates a new Elastic Job agent</span></span>

## <span data-ttu-id="867f3-110">示例</span><span class="sxs-lookup"><span data-stu-id="867f3-110">EXAMPLES</span></span>

### <span data-ttu-id="867f3-111">範例1</span><span class="sxs-lookup"><span data-stu-id="867f3-111">Example 1</span></span>
```
PS C:\> New-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -DatabaseName jobdb -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready
```

<span data-ttu-id="867f3-112">建立新的彈性作業代理程式</span><span class="sxs-lookup"><span data-stu-id="867f3-112">Creates a new Elastic Job agent</span></span>

## <span data-ttu-id="867f3-113">參數</span><span class="sxs-lookup"><span data-stu-id="867f3-113">PARAMETERS</span></span>

### <span data-ttu-id="867f3-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="867f3-114">-DatabaseName</span></span>
<span data-ttu-id="867f3-115">資料庫名稱</span><span class="sxs-lookup"><span data-stu-id="867f3-115">The database name</span></span>

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

### <span data-ttu-id="867f3-116">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="867f3-116">-DatabaseObject</span></span>
<span data-ttu-id="867f3-117">Agent 控制資料庫物件</span><span class="sxs-lookup"><span data-stu-id="867f3-117">The Agent Control Database Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="867f3-118">-DatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="867f3-118">-DatabaseResourceId</span></span>
<span data-ttu-id="867f3-119">Agent 控制資料庫資源識別碼</span><span class="sxs-lookup"><span data-stu-id="867f3-119">The Agent Control Database Resource Id</span></span>

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

### <span data-ttu-id="867f3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="867f3-120">-DefaultProfile</span></span>
<span data-ttu-id="867f3-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="867f3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="867f3-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="867f3-122">-Name</span></span>
<span data-ttu-id="867f3-123">代理程式名稱</span><span class="sxs-lookup"><span data-stu-id="867f3-123">The Agent Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AgentName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="867f3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="867f3-124">-ResourceGroupName</span></span>
<span data-ttu-id="867f3-125">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="867f3-125">The resource group name</span></span>

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

### <span data-ttu-id="867f3-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="867f3-126">-ServerName</span></span>
<span data-ttu-id="867f3-127">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="867f3-127">The server name</span></span>

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

### <span data-ttu-id="867f3-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="867f3-128">-Tag</span></span>
<span data-ttu-id="867f3-129">Agent 標記</span><span class="sxs-lookup"><span data-stu-id="867f3-129">The Agent Tags</span></span>

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

### <span data-ttu-id="867f3-130">-確認</span><span class="sxs-lookup"><span data-stu-id="867f3-130">-Confirm</span></span>
<span data-ttu-id="867f3-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="867f3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="867f3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="867f3-132">-WhatIf</span></span>
<span data-ttu-id="867f3-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="867f3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="867f3-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="867f3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="867f3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="867f3-135">CommonParameters</span></span>
<span data-ttu-id="867f3-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="867f3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="867f3-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="867f3-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="867f3-138">輸入</span><span class="sxs-lookup"><span data-stu-id="867f3-138">INPUTS</span></span>

### <span data-ttu-id="867f3-139">AzureSqlDatabaseModel （.Sql）的。</span><span class="sxs-lookup"><span data-stu-id="867f3-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="867f3-140">輸出</span><span class="sxs-lookup"><span data-stu-id="867f3-140">OUTPUTS</span></span>

### <span data-ttu-id="867f3-141">AzureSqlElasticJobAgentModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="867f3-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="867f3-142">筆記</span><span class="sxs-lookup"><span data-stu-id="867f3-142">NOTES</span></span>

## <span data-ttu-id="867f3-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="867f3-143">RELATED LINKS</span></span>
