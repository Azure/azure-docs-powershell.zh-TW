---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: 4652774b07ca3ae58baf29b614bd63519d537a0a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792690"
---
# <span data-ttu-id="624ce-101">Remove-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="624ce-101">Remove-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="624ce-102">摘要</span><span class="sxs-lookup"><span data-stu-id="624ce-102">SYNOPSIS</span></span>
<span data-ttu-id="624ce-103">移除目標群組</span><span class="sxs-lookup"><span data-stu-id="624ce-103">Removes the target group</span></span>

## <span data-ttu-id="624ce-104">句法</span><span class="sxs-lookup"><span data-stu-id="624ce-104">SYNTAX</span></span>

### <span data-ttu-id="624ce-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="624ce-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="624ce-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="624ce-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobTargetGroup [-InputObject] <AzureSqlElasticJobTargetGroupModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="624ce-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="624ce-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobTargetGroup [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="624ce-108">說明</span><span class="sxs-lookup"><span data-stu-id="624ce-108">DESCRIPTION</span></span>
<span data-ttu-id="624ce-109">Remove-AzSqlElasticJobTargetGroup Cmdlet 會移除目標群組及其目標</span><span class="sxs-lookup"><span data-stu-id="624ce-109">The Remove-AzSqlElasticJobTargetGroup cmdlet removes a target group and it's targets</span></span>

## <span data-ttu-id="624ce-110">示例</span><span class="sxs-lookup"><span data-stu-id="624ce-110">EXAMPLES</span></span>

### <span data-ttu-id="624ce-111">範例1</span><span class="sxs-lookup"><span data-stu-id="624ce-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent 
$agent | Remove-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1             (s1,db1)
```

<span data-ttu-id="624ce-112">移除目標群組及其目標</span><span class="sxs-lookup"><span data-stu-id="624ce-112">Removes a target group and it's targets</span></span>

## <span data-ttu-id="624ce-113">參數</span><span class="sxs-lookup"><span data-stu-id="624ce-113">PARAMETERS</span></span>

### <span data-ttu-id="624ce-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="624ce-114">-AgentName</span></span>
<span data-ttu-id="624ce-115">代理程式名稱</span><span class="sxs-lookup"><span data-stu-id="624ce-115">The agent name</span></span>

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

### <span data-ttu-id="624ce-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="624ce-116">-DefaultProfile</span></span>
<span data-ttu-id="624ce-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="624ce-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="624ce-118">-Force</span><span class="sxs-lookup"><span data-stu-id="624ce-118">-Force</span></span>
<span data-ttu-id="624ce-119">略過確認訊息以執行動作</span><span class="sxs-lookup"><span data-stu-id="624ce-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="624ce-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="624ce-120">-InputObject</span></span>
<span data-ttu-id="624ce-121">目標群組物件</span><span class="sxs-lookup"><span data-stu-id="624ce-121">The target group object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="624ce-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="624ce-122">-Name</span></span>
<span data-ttu-id="624ce-123">目標群組名稱</span><span class="sxs-lookup"><span data-stu-id="624ce-123">The target group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: TargetGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="624ce-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="624ce-124">-ResourceGroupName</span></span>
<span data-ttu-id="624ce-125">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="624ce-125">The resource group name</span></span>

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

### <span data-ttu-id="624ce-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="624ce-126">-ResourceId</span></span>
<span data-ttu-id="624ce-127">目標群組資源識別碼</span><span class="sxs-lookup"><span data-stu-id="624ce-127">The target group resource id</span></span>

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

### <span data-ttu-id="624ce-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="624ce-128">-ServerName</span></span>
<span data-ttu-id="624ce-129">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="624ce-129">The server name</span></span>

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

### <span data-ttu-id="624ce-130">-確認</span><span class="sxs-lookup"><span data-stu-id="624ce-130">-Confirm</span></span>
<span data-ttu-id="624ce-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="624ce-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="624ce-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="624ce-132">-WhatIf</span></span>
<span data-ttu-id="624ce-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="624ce-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="624ce-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="624ce-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="624ce-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="624ce-135">CommonParameters</span></span>
<span data-ttu-id="624ce-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="624ce-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="624ce-137">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="624ce-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="624ce-138">輸入</span><span class="sxs-lookup"><span data-stu-id="624ce-138">INPUTS</span></span>

### <span data-ttu-id="624ce-139">AzureSqlElasticJobTargetGroupModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="624ce-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="624ce-140">輸出</span><span class="sxs-lookup"><span data-stu-id="624ce-140">OUTPUTS</span></span>

### <span data-ttu-id="624ce-141">AzureSqlElasticJobTargetGroupModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="624ce-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="624ce-142">筆記</span><span class="sxs-lookup"><span data-stu-id="624ce-142">NOTES</span></span>

## <span data-ttu-id="624ce-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="624ce-143">RELATED LINKS</span></span>
