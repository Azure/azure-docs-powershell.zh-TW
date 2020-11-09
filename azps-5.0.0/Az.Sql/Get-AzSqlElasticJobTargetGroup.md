---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: f68baa997fd808a6e31bbb499f621f7ce303a25a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284632"
---
# <span data-ttu-id="42124-101">Get-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="42124-101">Get-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="42124-102">摘要</span><span class="sxs-lookup"><span data-stu-id="42124-102">SYNOPSIS</span></span>
<span data-ttu-id="42124-103">取得一個或多個作業目標群組</span><span class="sxs-lookup"><span data-stu-id="42124-103">Gets one or more job target groups</span></span>

## <span data-ttu-id="42124-104">句法</span><span class="sxs-lookup"><span data-stu-id="42124-104">SYNTAX</span></span>

### <span data-ttu-id="42124-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="42124-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42124-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="42124-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42124-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="42124-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42124-108">說明</span><span class="sxs-lookup"><span data-stu-id="42124-108">DESCRIPTION</span></span>
<span data-ttu-id="42124-109">Get-AzSqlElasticJobTargetGroup Cmdlet 會取得目標群組及其目標</span><span class="sxs-lookup"><span data-stu-id="42124-109">The Get-AzSqlElasticJobTargetGroup cmdlet gets a target group and it's targets</span></span>

## <span data-ttu-id="42124-110">示例</span><span class="sxs-lookup"><span data-stu-id="42124-110">EXAMPLES</span></span>

### <span data-ttu-id="42124-111">範例1</span><span class="sxs-lookup"><span data-stu-id="42124-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1             (s1,db1)
```

<span data-ttu-id="42124-112">取得目標群組及其目標</span><span class="sxs-lookup"><span data-stu-id="42124-112">Gets a target group and it's targets</span></span>

## <span data-ttu-id="42124-113">參數</span><span class="sxs-lookup"><span data-stu-id="42124-113">PARAMETERS</span></span>

### <span data-ttu-id="42124-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="42124-114">-AgentName</span></span>
<span data-ttu-id="42124-115">代理程式名稱</span><span class="sxs-lookup"><span data-stu-id="42124-115">The agent name</span></span>

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

### <span data-ttu-id="42124-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42124-116">-DefaultProfile</span></span>
<span data-ttu-id="42124-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="42124-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42124-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="42124-118">-Name</span></span>
<span data-ttu-id="42124-119">目標群組名稱</span><span class="sxs-lookup"><span data-stu-id="42124-119">The target group name</span></span>

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

### <span data-ttu-id="42124-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="42124-120">-ParentObject</span></span>
<span data-ttu-id="42124-121">Agent 物件</span><span class="sxs-lookup"><span data-stu-id="42124-121">The agent object</span></span>

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

### <span data-ttu-id="42124-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="42124-122">-ParentResourceId</span></span>
<span data-ttu-id="42124-123">Agent 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="42124-123">The agent resource id</span></span>

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

### <span data-ttu-id="42124-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42124-124">-ResourceGroupName</span></span>
<span data-ttu-id="42124-125">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="42124-125">The resource group name</span></span>

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

### <span data-ttu-id="42124-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="42124-126">-ServerName</span></span>
<span data-ttu-id="42124-127">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="42124-127">The server name</span></span>

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

### <span data-ttu-id="42124-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42124-128">CommonParameters</span></span>
<span data-ttu-id="42124-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="42124-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42124-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="42124-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42124-131">輸入</span><span class="sxs-lookup"><span data-stu-id="42124-131">INPUTS</span></span>

### <span data-ttu-id="42124-132">AzureSqlElasticJobAgentModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="42124-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="42124-133">輸出</span><span class="sxs-lookup"><span data-stu-id="42124-133">OUTPUTS</span></span>

### <span data-ttu-id="42124-134">AzureSqlElasticJobTargetGroupModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="42124-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="42124-135">筆記</span><span class="sxs-lookup"><span data-stu-id="42124-135">NOTES</span></span>

## <span data-ttu-id="42124-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="42124-136">RELATED LINKS</span></span>
