---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
ms.openlocfilehash: 58adbb3b160272007899dc8740e211b6e81a10a4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970066"
---
# <span data-ttu-id="8352f-101">Set-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="8352f-101">Set-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="8352f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8352f-102">SYNOPSIS</span></span>
<span data-ttu-id="8352f-103">更新彈性作業代理程式</span><span class="sxs-lookup"><span data-stu-id="8352f-103">Updates an elastic job agent</span></span>

## <span data-ttu-id="8352f-104">句法</span><span class="sxs-lookup"><span data-stu-id="8352f-104">SYNTAX</span></span>

### <span data-ttu-id="8352f-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8352f-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8352f-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="8352f-106">ObjectSet</span></span>
```
Set-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8352f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8352f-107">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8352f-108">說明</span><span class="sxs-lookup"><span data-stu-id="8352f-108">DESCRIPTION</span></span>
<span data-ttu-id="8352f-109">Set-AzSqlElasticJobAgent Cmdlet 會更新彈性作業代理程式</span><span class="sxs-lookup"><span data-stu-id="8352f-109">The Set-AzSqlElasticJobAgent cmdlet updates an Elastic Job agents</span></span>

## <span data-ttu-id="8352f-110">示例</span><span class="sxs-lookup"><span data-stu-id="8352f-110">EXAMPLES</span></span>

### <span data-ttu-id="8352f-111">範例1</span><span class="sxs-lookup"><span data-stu-id="8352f-111">Example 1</span></span>
```
PS C:\> Set-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent -Tag @{ Octopus = "Agent" }

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="8352f-112">更新彈性作業代理程式</span><span class="sxs-lookup"><span data-stu-id="8352f-112">Updates an Elastic Job agent</span></span>

## <span data-ttu-id="8352f-113">參數</span><span class="sxs-lookup"><span data-stu-id="8352f-113">PARAMETERS</span></span>

### <span data-ttu-id="8352f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8352f-114">-DefaultProfile</span></span>
<span data-ttu-id="8352f-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8352f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8352f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8352f-116">-InputObject</span></span>
<span data-ttu-id="8352f-117">Agent 輸入物件</span><span class="sxs-lookup"><span data-stu-id="8352f-117">The agent input object</span></span>

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

### <span data-ttu-id="8352f-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="8352f-118">-Name</span></span>
<span data-ttu-id="8352f-119">代理程式名稱</span><span class="sxs-lookup"><span data-stu-id="8352f-119">The agent name</span></span>

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

### <span data-ttu-id="8352f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8352f-120">-ResourceGroupName</span></span>
<span data-ttu-id="8352f-121">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="8352f-121">The resource group name</span></span>

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

### <span data-ttu-id="8352f-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8352f-122">-ResourceId</span></span>
<span data-ttu-id="8352f-123">Agent 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="8352f-123">The agent resource id</span></span>

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

### <span data-ttu-id="8352f-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8352f-124">-ServerName</span></span>
<span data-ttu-id="8352f-125">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="8352f-125">The server name</span></span>

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

### <span data-ttu-id="8352f-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="8352f-126">-Tag</span></span>
<span data-ttu-id="8352f-127">要與 Azure SQL 資料庫代理程式相關聯的標記</span><span class="sxs-lookup"><span data-stu-id="8352f-127">The tags to associate with the Azure SQL Database Agent</span></span>

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

### <span data-ttu-id="8352f-128">-確認</span><span class="sxs-lookup"><span data-stu-id="8352f-128">-Confirm</span></span>
<span data-ttu-id="8352f-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8352f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8352f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8352f-130">-WhatIf</span></span>
<span data-ttu-id="8352f-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8352f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8352f-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8352f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8352f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8352f-133">CommonParameters</span></span>
<span data-ttu-id="8352f-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8352f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8352f-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8352f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8352f-136">輸入</span><span class="sxs-lookup"><span data-stu-id="8352f-136">INPUTS</span></span>

### <span data-ttu-id="8352f-137">AzureSqlElasticJobAgentModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="8352f-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="8352f-138">輸出</span><span class="sxs-lookup"><span data-stu-id="8352f-138">OUTPUTS</span></span>

### <span data-ttu-id="8352f-139">AzureSqlElasticJobAgentModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="8352f-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="8352f-140">筆記</span><span class="sxs-lookup"><span data-stu-id="8352f-140">NOTES</span></span>

## <span data-ttu-id="8352f-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="8352f-141">RELATED LINKS</span></span>
