---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/new-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobAgent.md
ms.openlocfilehash: ca23ba63e2f92fa14c97957a2b21b38d91e453ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909426"
---
# <span data-ttu-id="07254-101">New-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="07254-101">New-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="07254-102">簡介</span><span class="sxs-lookup"><span data-stu-id="07254-102">SYNOPSIS</span></span>
<span data-ttu-id="07254-103">建立新的彈性工作代理程式</span><span class="sxs-lookup"><span data-stu-id="07254-103">Creates a new elastic job agent</span></span>

## <span data-ttu-id="07254-104">語法</span><span class="sxs-lookup"><span data-stu-id="07254-104">SYNTAX</span></span>

### <span data-ttu-id="07254-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="07254-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-Name] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="07254-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="07254-106">ObjectSet</span></span>
```
New-AzSqlElasticJobAgent [-DatabaseObject] <AzureSqlDatabaseModel> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07254-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="07254-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobAgent [-DatabaseResourceId] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07254-108">描述</span><span class="sxs-lookup"><span data-stu-id="07254-108">DESCRIPTION</span></span>
<span data-ttu-id="07254-109">Cmdlet New-AzSqlElasticJobAgent Cmdlet 會建立一個新的 Job Job 代理程式</span><span class="sxs-lookup"><span data-stu-id="07254-109">The New-AzSqlElasticJobAgent cmdlet creates a new Elastic Job agent</span></span>

## <span data-ttu-id="07254-110">例子</span><span class="sxs-lookup"><span data-stu-id="07254-110">EXAMPLES</span></span>

### <span data-ttu-id="07254-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="07254-111">Example 1</span></span>
```
PS C:\> New-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -DatabaseName jobdb -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready
```

<span data-ttu-id="07254-112">建立新的彈性工作代理程式</span><span class="sxs-lookup"><span data-stu-id="07254-112">Creates a new Elastic Job agent</span></span>

## <span data-ttu-id="07254-113">參數</span><span class="sxs-lookup"><span data-stu-id="07254-113">PARAMETERS</span></span>

### <span data-ttu-id="07254-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="07254-114">-DatabaseName</span></span>
<span data-ttu-id="07254-115">資料庫名稱</span><span class="sxs-lookup"><span data-stu-id="07254-115">The database name</span></span>

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

### <span data-ttu-id="07254-116">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="07254-116">-DatabaseObject</span></span>
<span data-ttu-id="07254-117">代理程式控制項資料庫物件</span><span class="sxs-lookup"><span data-stu-id="07254-117">The Agent Control Database Object</span></span>

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

### <span data-ttu-id="07254-118">-DatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="07254-118">-DatabaseResourceId</span></span>
<span data-ttu-id="07254-119">代理程式控制資料庫資源識別碼</span><span class="sxs-lookup"><span data-stu-id="07254-119">The Agent Control Database Resource Id</span></span>

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

### <span data-ttu-id="07254-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07254-120">-DefaultProfile</span></span>
<span data-ttu-id="07254-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="07254-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07254-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="07254-122">-Name</span></span>
<span data-ttu-id="07254-123">代理人名稱</span><span class="sxs-lookup"><span data-stu-id="07254-123">The Agent Name</span></span>

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

### <span data-ttu-id="07254-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07254-124">-ResourceGroupName</span></span>
<span data-ttu-id="07254-125">資源組名</span><span class="sxs-lookup"><span data-stu-id="07254-125">The resource group name</span></span>

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

### <span data-ttu-id="07254-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="07254-126">-ServerName</span></span>
<span data-ttu-id="07254-127">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="07254-127">The server name</span></span>

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

### <span data-ttu-id="07254-128">-標記</span><span class="sxs-lookup"><span data-stu-id="07254-128">-Tag</span></span>
<span data-ttu-id="07254-129">代理程式標記</span><span class="sxs-lookup"><span data-stu-id="07254-129">The Agent Tags</span></span>

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

### <span data-ttu-id="07254-130">-確認</span><span class="sxs-lookup"><span data-stu-id="07254-130">-Confirm</span></span>
<span data-ttu-id="07254-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="07254-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07254-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07254-132">-WhatIf</span></span>
<span data-ttu-id="07254-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="07254-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07254-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="07254-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07254-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07254-135">CommonParameters</span></span>
<span data-ttu-id="07254-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="07254-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07254-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="07254-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07254-138">輸入</span><span class="sxs-lookup"><span data-stu-id="07254-138">INPUTS</span></span>

### <span data-ttu-id="07254-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="07254-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="07254-140">輸出</span><span class="sxs-lookup"><span data-stu-id="07254-140">OUTPUTS</span></span>

### <span data-ttu-id="07254-141">Microsoft.Azure.Commands.Sql.AzureJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="07254-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="07254-142">筆記</span><span class="sxs-lookup"><span data-stu-id="07254-142">NOTES</span></span>

## <span data-ttu-id="07254-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="07254-143">RELATED LINKS</span></span>
