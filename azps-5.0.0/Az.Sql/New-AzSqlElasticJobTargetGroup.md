---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: 5818bd11b3131ff340857e033053eb492a9178e6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138120"
---
# <span data-ttu-id="32fa8-101">New-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="32fa8-101">New-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="32fa8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="32fa8-102">SYNOPSIS</span></span>
<span data-ttu-id="32fa8-103">建立新的目標群組</span><span class="sxs-lookup"><span data-stu-id="32fa8-103">Creates a new target group</span></span>

## <span data-ttu-id="32fa8-104">句法</span><span class="sxs-lookup"><span data-stu-id="32fa8-104">SYNTAX</span></span>

### <span data-ttu-id="32fa8-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="32fa8-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32fa8-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="32fa8-106">ObjectSet</span></span>
```
New-AzSqlElasticJobTargetGroup [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32fa8-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="32fa8-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobTargetGroup [-ParentResourceId] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32fa8-108">說明</span><span class="sxs-lookup"><span data-stu-id="32fa8-108">DESCRIPTION</span></span>
<span data-ttu-id="32fa8-109">New-AzSqlElasticJobTargetGroup Cmdlet 會建立新的目標群組</span><span class="sxs-lookup"><span data-stu-id="32fa8-109">The New-AzSqlElasticJobTargetGroup cmdlet creates a new target group</span></span>

## <span data-ttu-id="32fa8-110">示例</span><span class="sxs-lookup"><span data-stu-id="32fa8-110">EXAMPLES</span></span>

### <span data-ttu-id="32fa8-111">範例1</span><span class="sxs-lookup"><span data-stu-id="32fa8-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1
```

<span data-ttu-id="32fa8-112">建立空白的目標群組</span><span class="sxs-lookup"><span data-stu-id="32fa8-112">Creates an empty target group</span></span>

## <span data-ttu-id="32fa8-113">參數</span><span class="sxs-lookup"><span data-stu-id="32fa8-113">PARAMETERS</span></span>

### <span data-ttu-id="32fa8-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="32fa8-114">-AgentName</span></span>
<span data-ttu-id="32fa8-115">代理程式名稱</span><span class="sxs-lookup"><span data-stu-id="32fa8-115">The agent name</span></span>

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

### <span data-ttu-id="32fa8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32fa8-116">-DefaultProfile</span></span>
<span data-ttu-id="32fa8-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="32fa8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32fa8-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="32fa8-118">-Name</span></span>
<span data-ttu-id="32fa8-119">目標群組名稱</span><span class="sxs-lookup"><span data-stu-id="32fa8-119">The target group name</span></span>

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

### <span data-ttu-id="32fa8-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="32fa8-120">-ParentObject</span></span>
<span data-ttu-id="32fa8-121">Agent 輸入物件</span><span class="sxs-lookup"><span data-stu-id="32fa8-121">The agent input object</span></span>

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

### <span data-ttu-id="32fa8-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="32fa8-122">-ParentResourceId</span></span>
<span data-ttu-id="32fa8-123">Agent 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="32fa8-123">The agent resource id</span></span>

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

### <span data-ttu-id="32fa8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32fa8-124">-ResourceGroupName</span></span>
<span data-ttu-id="32fa8-125">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="32fa8-125">The resource group name</span></span>

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

### <span data-ttu-id="32fa8-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="32fa8-126">-ServerName</span></span>
<span data-ttu-id="32fa8-127">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="32fa8-127">The server name</span></span>

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

### <span data-ttu-id="32fa8-128">-確認</span><span class="sxs-lookup"><span data-stu-id="32fa8-128">-Confirm</span></span>
<span data-ttu-id="32fa8-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="32fa8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32fa8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32fa8-130">-WhatIf</span></span>
<span data-ttu-id="32fa8-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="32fa8-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32fa8-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="32fa8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32fa8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32fa8-133">CommonParameters</span></span>
<span data-ttu-id="32fa8-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="32fa8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32fa8-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="32fa8-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32fa8-136">輸入</span><span class="sxs-lookup"><span data-stu-id="32fa8-136">INPUTS</span></span>

### <span data-ttu-id="32fa8-137">AzureSqlElasticJobAgentModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="32fa8-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="32fa8-138">輸出</span><span class="sxs-lookup"><span data-stu-id="32fa8-138">OUTPUTS</span></span>

### <span data-ttu-id="32fa8-139">AzureSqlElasticJobTargetGroupModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="32fa8-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="32fa8-140">筆記</span><span class="sxs-lookup"><span data-stu-id="32fa8-140">NOTES</span></span>

## <span data-ttu-id="32fa8-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="32fa8-141">RELATED LINKS</span></span>