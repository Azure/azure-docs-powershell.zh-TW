---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobAgent.md
ms.openlocfilehash: 7d2985d2e5361f7594dbccac2e67c7c550c9b0a5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93799102"
---
# <span data-ttu-id="dbad8-101">Get-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="dbad8-101">Get-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="dbad8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dbad8-102">SYNOPSIS</span></span>
<span data-ttu-id="dbad8-103">取得 Azure SQL 彈性作業代理程式</span><span class="sxs-lookup"><span data-stu-id="dbad8-103">Gets a Azure SQL Elastic Job agent</span></span>

## <span data-ttu-id="dbad8-104">句法</span><span class="sxs-lookup"><span data-stu-id="dbad8-104">SYNTAX</span></span>

### <span data-ttu-id="dbad8-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="dbad8-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbad8-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="dbad8-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobAgent [-ParentObject] <AzureSqlServerModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbad8-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="dbad8-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobAgent [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbad8-108">說明</span><span class="sxs-lookup"><span data-stu-id="dbad8-108">DESCRIPTION</span></span>
<span data-ttu-id="dbad8-109">Get-AzSqlElasticJobAgent Cmdlet 會取得一或多個彈性作業代理程式</span><span class="sxs-lookup"><span data-stu-id="dbad8-109">The Get-AzSqlElasticJobAgent cmdlet gets one or more Elastic Job agents</span></span>

## <span data-ttu-id="dbad8-110">示例</span><span class="sxs-lookup"><span data-stu-id="dbad8-110">EXAMPLES</span></span>

### <span data-ttu-id="dbad8-111">範例1</span><span class="sxs-lookup"><span data-stu-id="dbad8-111">Example 1</span></span>
```
PS C:\> Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready
```

<span data-ttu-id="dbad8-112">取得彈性作業代理程式</span><span class="sxs-lookup"><span data-stu-id="dbad8-112">Gets an Elastic Job agent</span></span>

## <span data-ttu-id="dbad8-113">參數</span><span class="sxs-lookup"><span data-stu-id="dbad8-113">PARAMETERS</span></span>

### <span data-ttu-id="dbad8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbad8-114">-DefaultProfile</span></span>
<span data-ttu-id="dbad8-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dbad8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbad8-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="dbad8-116">-Name</span></span>
<span data-ttu-id="dbad8-117">代理程式名稱</span><span class="sxs-lookup"><span data-stu-id="dbad8-117">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AgentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbad8-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="dbad8-118">-ParentObject</span></span>
<span data-ttu-id="dbad8-119">伺服器輸入物件</span><span class="sxs-lookup"><span data-stu-id="dbad8-119">The server input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dbad8-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="dbad8-120">-ParentResourceId</span></span>
<span data-ttu-id="dbad8-121">伺服器資源識別碼</span><span class="sxs-lookup"><span data-stu-id="dbad8-121">The server resource id</span></span>

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

### <span data-ttu-id="dbad8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbad8-122">-ResourceGroupName</span></span>
<span data-ttu-id="dbad8-123">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="dbad8-123">The resource group name</span></span>

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

### <span data-ttu-id="dbad8-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="dbad8-124">-ServerName</span></span>
<span data-ttu-id="dbad8-125">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="dbad8-125">The server name</span></span>

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

### <span data-ttu-id="dbad8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbad8-126">CommonParameters</span></span>
<span data-ttu-id="dbad8-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dbad8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbad8-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="dbad8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbad8-129">輸入</span><span class="sxs-lookup"><span data-stu-id="dbad8-129">INPUTS</span></span>

### <span data-ttu-id="dbad8-130">AzureSqlServerModel 的 [.Sql] 命令</span><span class="sxs-lookup"><span data-stu-id="dbad8-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="dbad8-131">輸出</span><span class="sxs-lookup"><span data-stu-id="dbad8-131">OUTPUTS</span></span>

### <span data-ttu-id="dbad8-132">AzureSqlElasticJobAgentModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="dbad8-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="dbad8-133">筆記</span><span class="sxs-lookup"><span data-stu-id="dbad8-133">NOTES</span></span>

## <span data-ttu-id="dbad8-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="dbad8-134">RELATED LINKS</span></span>