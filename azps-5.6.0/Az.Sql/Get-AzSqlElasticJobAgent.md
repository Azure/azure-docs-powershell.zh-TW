---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/get-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobAgent.md
ms.openlocfilehash: 6ff5bdb6a3de7b1704ee41de0b6ff0b0f736ec5e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917570"
---
# <span data-ttu-id="b2d6e-101">Get-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="b2d6e-101">Get-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="b2d6e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b2d6e-102">SYNOPSIS</span></span>
<span data-ttu-id="b2d6e-103">獲得 Azure SQL 進位工作代理程式</span><span class="sxs-lookup"><span data-stu-id="b2d6e-103">Gets a Azure SQL Elastic Job agent</span></span>

## <span data-ttu-id="b2d6e-104">語法</span><span class="sxs-lookup"><span data-stu-id="b2d6e-104">SYNTAX</span></span>

### <span data-ttu-id="b2d6e-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b2d6e-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2d6e-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="b2d6e-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobAgent [-ParentObject] <AzureSqlServerModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2d6e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b2d6e-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobAgent [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2d6e-108">描述</span><span class="sxs-lookup"><span data-stu-id="b2d6e-108">DESCRIPTION</span></span>
<span data-ttu-id="b2d6e-109">Cmdlet Get-AzSqlElasticJobAgent一或多個彈性工作代理程式</span><span class="sxs-lookup"><span data-stu-id="b2d6e-109">The Get-AzSqlElasticJobAgent cmdlet gets one or more Elastic Job agents</span></span>

## <span data-ttu-id="b2d6e-110">例子</span><span class="sxs-lookup"><span data-stu-id="b2d6e-110">EXAMPLES</span></span>

### <span data-ttu-id="b2d6e-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="b2d6e-111">Example 1</span></span>
```
PS C:\> Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready
```

<span data-ttu-id="b2d6e-112">獲得彈性工作代理程式</span><span class="sxs-lookup"><span data-stu-id="b2d6e-112">Gets an Elastic Job agent</span></span>

## <span data-ttu-id="b2d6e-113">參數</span><span class="sxs-lookup"><span data-stu-id="b2d6e-113">PARAMETERS</span></span>

### <span data-ttu-id="b2d6e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2d6e-114">-DefaultProfile</span></span>
<span data-ttu-id="b2d6e-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b2d6e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2d6e-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="b2d6e-116">-Name</span></span>
<span data-ttu-id="b2d6e-117">代理人名稱</span><span class="sxs-lookup"><span data-stu-id="b2d6e-117">The agent name</span></span>

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

### <span data-ttu-id="b2d6e-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b2d6e-118">-ParentObject</span></span>
<span data-ttu-id="b2d6e-119">伺服器輸入物件</span><span class="sxs-lookup"><span data-stu-id="b2d6e-119">The server input object</span></span>

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

### <span data-ttu-id="b2d6e-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b2d6e-120">-ParentResourceId</span></span>
<span data-ttu-id="b2d6e-121">伺服器資源識別碼</span><span class="sxs-lookup"><span data-stu-id="b2d6e-121">The server resource id</span></span>

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

### <span data-ttu-id="b2d6e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2d6e-122">-ResourceGroupName</span></span>
<span data-ttu-id="b2d6e-123">資源組名</span><span class="sxs-lookup"><span data-stu-id="b2d6e-123">The resource group name</span></span>

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

### <span data-ttu-id="b2d6e-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b2d6e-124">-ServerName</span></span>
<span data-ttu-id="b2d6e-125">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="b2d6e-125">The server name</span></span>

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

### <span data-ttu-id="b2d6e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2d6e-126">CommonParameters</span></span>
<span data-ttu-id="b2d6e-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b2d6e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2d6e-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b2d6e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2d6e-129">輸入</span><span class="sxs-lookup"><span data-stu-id="b2d6e-129">INPUTS</span></span>

### <span data-ttu-id="b2d6e-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="b2d6e-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="b2d6e-131">輸出</span><span class="sxs-lookup"><span data-stu-id="b2d6e-131">OUTPUTS</span></span>

### <span data-ttu-id="b2d6e-132">Microsoft.Azure.Commands.Sql.AzureJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="b2d6e-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="b2d6e-133">筆記</span><span class="sxs-lookup"><span data-stu-id="b2d6e-133">NOTES</span></span>

## <span data-ttu-id="b2d6e-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="b2d6e-134">RELATED LINKS</span></span>
