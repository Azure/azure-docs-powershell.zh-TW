---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: EFDFCE12-F39C-4F52-9962-4601F0C4FD47
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlelasticpoolrecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolRecommendedActionState.md
ms.openlocfilehash: 5ef58938342845b437d714e44a55256892632546
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915193"
---
# <span data-ttu-id="1cd85-101">Set-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="1cd85-101">Set-AzSqlElasticPoolRecommendedActionState</span></span>

## <span data-ttu-id="1cd85-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1cd85-102">SYNOPSIS</span></span>
<span data-ttu-id="1cd85-103">更新 Azure SQL Pool Pool 建議的動作狀態。</span><span class="sxs-lookup"><span data-stu-id="1cd85-103">Updates the state of an Azure SQL Elastic Pool recommended action.</span></span>

## <span data-ttu-id="1cd85-104">語法</span><span class="sxs-lookup"><span data-stu-id="1cd85-104">SYNTAX</span></span>

```
Set-AzSqlElasticPoolRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -ElasticPoolName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cd85-105">描述</span><span class="sxs-lookup"><span data-stu-id="1cd85-105">DESCRIPTION</span></span>
<span data-ttu-id="1cd85-106">**Set-AzSqlElasticPoolRecomactionActionState** Cmdlet 會更新 Azure SQL 集區建議動作的狀態。</span><span class="sxs-lookup"><span data-stu-id="1cd85-106">The **Set-AzSqlElasticPoolRecommendedActionState** cmdlet updates state of an Azure SQL Elastic Pool recommended action.</span></span>
<span data-ttu-id="1cd85-107">此 Cmdlet 會根據新狀態，適用建議的動作、還原或捨棄。</span><span class="sxs-lookup"><span data-stu-id="1cd85-107">This cmdlet applies an recommended action, reverted, or discarded based on the new state.</span></span>

## <span data-ttu-id="1cd85-108">例子</span><span class="sxs-lookup"><span data-stu-id="1cd85-108">EXAMPLES</span></span>

### <span data-ttu-id="1cd85-109">範例 1：將建議動作的狀態更新為擱置</span><span class="sxs-lookup"><span data-stu-id="1cd85-109">Example 1: Update the state of a recommended action to Pending</span></span>
```
PS C:\>Set-AzSqlElasticPoolRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
ElasticPoolName            : WIRunnerPool
ResourceGroupName          : WIRunnersProd
ServerName                 : wi-runner-australia-east
AdvisorName                : CreateIndex
RecommendedActionName      : IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893
Details                    : {[indexName, nci_wi_test_table_0.0361551_6C7AE8CC9C87E7FD5893], [indexType, 
                             NONCLUSTERED], [schema, [test_schema]], [table, [test_table_0.0361551]]...} 
ErrorDetails               : Microsoft.Azure.Management.Sql.Models.RecommendedActionErrorInfo
EstimatedImpact            : {ActionDuration, SpaceChange}
ExecuteActionDuration      : PT1M
ExecuteActionInitiatedBy   : User
ExecuteActionInitiatedTime : 4/21/2016 3:24:47 PM
ExecuteActionStartTime     : 4/21/2016 3:24:47 PM
ImplementationDetails      : Microsoft.Azure.Management.Sql.Models.RecommendedActionImplementationInfo
IsArchivedAction           : False
IsExecutableAction         : True
IsRevertableAction         : True
LastRefresh                : 4/21/2016 3:24:47 PM
LinkedObjects              : {}
ObservedImpact             : {CpuUtilization, LogicalReads, LogicalWrites, QueriesWithImprovedPerformance...} 
RecommendationReason       : 
RevertActionDuration       : 
RevertActionInitiatedBy    : 
RevertActionInitiatedTime  : 
RevertActionStartTime      : 
Score                      : 2
State                      : Microsoft.Azure.Management.Sql.Models.RecommendedActionStateInfo
TimeSeries                 : {}
ValidSince                 : 4/21/2016 3:24:47 PM
```

<span data-ttu-id="1cd85-110">此命令會更新稱為 IR_test_schema \[ \] _ \[ test_table_0.0361551 的_6C7AE8CC9C87E7FD5893狀態 \] 。</span><span class="sxs-lookup"><span data-stu-id="1cd85-110">This command updates the state of elastic pool recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 to Pending.</span></span>

## <span data-ttu-id="1cd85-111">參數</span><span class="sxs-lookup"><span data-stu-id="1cd85-111">PARAMETERS</span></span>

### <span data-ttu-id="1cd85-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="1cd85-112">-AdvisorName</span></span>
<span data-ttu-id="1cd85-113">指定此建議動作所屬的建議程式名稱。</span><span class="sxs-lookup"><span data-stu-id="1cd85-113">Specifies the name of the advisor for which this recommended action belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cd85-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cd85-114">-DefaultProfile</span></span>
<span data-ttu-id="1cd85-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="1cd85-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1cd85-116">-PoolPoolName</span><span class="sxs-lookup"><span data-stu-id="1cd85-116">-ElasticPoolName</span></span>
<span data-ttu-id="1cd85-117">指定泳層資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="1cd85-117">Specifies name of the elastic pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cd85-118">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="1cd85-118">-RecommendedActionName</span></span>
<span data-ttu-id="1cd85-119">指定此 Cmdlet 更新狀態的建議動作名稱。</span><span class="sxs-lookup"><span data-stu-id="1cd85-119">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cd85-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cd85-120">-ResourceGroupName</span></span>
<span data-ttu-id="1cd85-121">指定包含此集區之伺服器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="1cd85-121">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cd85-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1cd85-122">-ServerName</span></span>
<span data-ttu-id="1cd85-123">指定集中資料庫位於的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="1cd85-123">Specifies the name of the server the elastic pool is in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cd85-124">-State</span><span class="sxs-lookup"><span data-stu-id="1cd85-124">-State</span></span>
<span data-ttu-id="1cd85-125">指定此 Cmdlet 更新建議動作狀態的值。</span><span class="sxs-lookup"><span data-stu-id="1cd85-125">Specifies the value to which this cmdlet updates the recommended action state.</span></span>
<span data-ttu-id="1cd85-126">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="1cd85-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1cd85-127">積極</span><span class="sxs-lookup"><span data-stu-id="1cd85-127">Active</span></span>
- <span data-ttu-id="1cd85-128">等待</span><span class="sxs-lookup"><span data-stu-id="1cd85-128">Pending</span></span>
- <span data-ttu-id="1cd85-129">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="1cd85-129">PendingRevert</span></span>
- <span data-ttu-id="1cd85-130">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="1cd85-130">RevertCancelled</span></span>
- <span data-ttu-id="1cd85-131">忽視</span><span class="sxs-lookup"><span data-stu-id="1cd85-131">Ignored</span></span>
- <span data-ttu-id="1cd85-132">解決</span><span class="sxs-lookup"><span data-stu-id="1cd85-132">Resolved</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState
Parameter Sets: (All)
Aliases:
Accepted values: Active, Pending, PendingRevert, RevertCancelled, Ignored, Resolved

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cd85-133">-確認</span><span class="sxs-lookup"><span data-stu-id="1cd85-133">-Confirm</span></span>
<span data-ttu-id="1cd85-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1cd85-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cd85-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cd85-135">-WhatIf</span></span>
<span data-ttu-id="1cd85-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1cd85-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cd85-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1cd85-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cd85-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cd85-138">CommonParameters</span></span>
<span data-ttu-id="1cd85-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1cd85-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cd85-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1cd85-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cd85-141">輸入</span><span class="sxs-lookup"><span data-stu-id="1cd85-141">INPUTS</span></span>

### <span data-ttu-id="1cd85-142">System.String</span><span class="sxs-lookup"><span data-stu-id="1cd85-142">System.String</span></span>

### <span data-ttu-id="1cd85-143">Microsoft.Azure.Commands.sql.recommendedAction.Cmdlet.RecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="1cd85-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span></span>

## <span data-ttu-id="1cd85-144">輸出</span><span class="sxs-lookup"><span data-stu-id="1cd85-144">OUTPUTS</span></span>

### <span data-ttu-id="1cd85-145">Microsoft.Azure.Commands.sql.recommendedAction.Model.AzureSqlElasticPoolRecomactionModel</span><span class="sxs-lookup"><span data-stu-id="1cd85-145">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlElasticPoolRecommendedActionModel</span></span>

## <span data-ttu-id="1cd85-146">筆記</span><span class="sxs-lookup"><span data-stu-id="1cd85-146">NOTES</span></span>
* <span data-ttu-id="1cd85-147">關鍵字：azure、azurerm、arm、resource、management、manager、sql、pool、mssql、advisor、recommendedaction</span><span class="sxs-lookup"><span data-stu-id="1cd85-147">Keywords: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="1cd85-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="1cd85-148">RELATED LINKS</span></span>

[<span data-ttu-id="1cd85-149">Get-AzSqlElasticPoolRecomactionAction</span><span class="sxs-lookup"><span data-stu-id="1cd85-149">Get-AzSqlElasticPoolRecommendedAction</span></span>](./Get-AzSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="1cd85-150">Set-AzSqlDatabaseRecomactionActionState</span><span class="sxs-lookup"><span data-stu-id="1cd85-150">Set-AzSqlDatabaseRecommendedActionState</span></span>](./Set-AzSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="1cd85-151">Set-AzSqlServerRecomactionActionState</span><span class="sxs-lookup"><span data-stu-id="1cd85-151">Set-AzSqlServerRecommendedActionState</span></span>](./Set-AzSqlServerRecommendedActionState.md)

[<span data-ttu-id="1cd85-152">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="1cd85-152">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
