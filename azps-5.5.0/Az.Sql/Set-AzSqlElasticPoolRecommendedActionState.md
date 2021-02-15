---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: EFDFCE12-F39C-4F52-9962-4601F0C4FD47
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpoolrecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolRecommendedActionState.md
ms.openlocfilehash: 64a8884075bcc849deffd4083c95ec1849859a68
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127390"
---
# <span data-ttu-id="e88ce-101">Set-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="e88ce-101">Set-AzSqlElasticPoolRecommendedActionState</span></span>

## <span data-ttu-id="e88ce-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e88ce-102">SYNOPSIS</span></span>
<span data-ttu-id="e88ce-103">更新 Azure SQL 彈性池建議動作的狀態。</span><span class="sxs-lookup"><span data-stu-id="e88ce-103">Updates the state of an Azure SQL Elastic Pool recommended action.</span></span>

## <span data-ttu-id="e88ce-104">句法</span><span class="sxs-lookup"><span data-stu-id="e88ce-104">SYNTAX</span></span>

```
Set-AzSqlElasticPoolRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -ElasticPoolName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e88ce-105">說明</span><span class="sxs-lookup"><span data-stu-id="e88ce-105">DESCRIPTION</span></span>
<span data-ttu-id="e88ce-106">**AzSqlElasticPoolRecommendedActionState** Cmdlet 會更新 Azure SQL 彈性池建議動作的狀態。</span><span class="sxs-lookup"><span data-stu-id="e88ce-106">The **Set-AzSqlElasticPoolRecommendedActionState** cmdlet updates state of an Azure SQL Elastic Pool recommended action.</span></span>
<span data-ttu-id="e88ce-107">這個 Cmdlet 會根據新的狀態，套用建議的動作、還原或放棄。</span><span class="sxs-lookup"><span data-stu-id="e88ce-107">This cmdlet applies an recommended action, reverted, or discarded based on the new state.</span></span>

## <span data-ttu-id="e88ce-108">示例</span><span class="sxs-lookup"><span data-stu-id="e88ce-108">EXAMPLES</span></span>

### <span data-ttu-id="e88ce-109">範例1：將建議動作的狀態更新為擱置</span><span class="sxs-lookup"><span data-stu-id="e88ce-109">Example 1: Update the state of a recommended action to Pending</span></span>
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

<span data-ttu-id="e88ce-110">這個命令會將彈性池建議動作的狀態（IR_ test_schema _）更新為 [ \[ \] 擱置] \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893]。</span><span class="sxs-lookup"><span data-stu-id="e88ce-110">This command updates the state of elastic pool recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 to Pending.</span></span>

## <span data-ttu-id="e88ce-111">參數</span><span class="sxs-lookup"><span data-stu-id="e88ce-111">PARAMETERS</span></span>

### <span data-ttu-id="e88ce-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="e88ce-112">-AdvisorName</span></span>
<span data-ttu-id="e88ce-113">指定此建議動作所屬之 advisor 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e88ce-113">Specifies the name of the advisor for which this recommended action belongs to.</span></span>

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

### <span data-ttu-id="e88ce-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e88ce-114">-DefaultProfile</span></span>
<span data-ttu-id="e88ce-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e88ce-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e88ce-116">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="e88ce-116">-ElasticPoolName</span></span>
<span data-ttu-id="e88ce-117">指定彈性池的名稱。</span><span class="sxs-lookup"><span data-stu-id="e88ce-117">Specifies name of the elastic pool.</span></span>

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

### <span data-ttu-id="e88ce-118">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="e88ce-118">-RecommendedActionName</span></span>
<span data-ttu-id="e88ce-119">指定此 Cmdlet 更新狀態的建議動作名稱。</span><span class="sxs-lookup"><span data-stu-id="e88ce-119">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

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

### <span data-ttu-id="e88ce-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e88ce-120">-ResourceGroupName</span></span>
<span data-ttu-id="e88ce-121">指定包含此彈性池之伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e88ce-121">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="e88ce-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e88ce-122">-ServerName</span></span>
<span data-ttu-id="e88ce-123">指定彈性池所在的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="e88ce-123">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="e88ce-124">-State</span><span class="sxs-lookup"><span data-stu-id="e88ce-124">-State</span></span>
<span data-ttu-id="e88ce-125">指定此 Cmdlet 更新建議動作狀態的值。</span><span class="sxs-lookup"><span data-stu-id="e88ce-125">Specifies the value to which this cmdlet updates the recommended action state.</span></span>
<span data-ttu-id="e88ce-126">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="e88ce-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e88ce-127">有效</span><span class="sxs-lookup"><span data-stu-id="e88ce-127">Active</span></span>
- <span data-ttu-id="e88ce-128">擱置</span><span class="sxs-lookup"><span data-stu-id="e88ce-128">Pending</span></span>
- <span data-ttu-id="e88ce-129">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="e88ce-129">PendingRevert</span></span>
- <span data-ttu-id="e88ce-130">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="e88ce-130">RevertCancelled</span></span>
- <span data-ttu-id="e88ce-131">忽視</span><span class="sxs-lookup"><span data-stu-id="e88ce-131">Ignored</span></span>
- <span data-ttu-id="e88ce-132">已</span><span class="sxs-lookup"><span data-stu-id="e88ce-132">Resolved</span></span>

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

### <span data-ttu-id="e88ce-133">-確認</span><span class="sxs-lookup"><span data-stu-id="e88ce-133">-Confirm</span></span>
<span data-ttu-id="e88ce-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e88ce-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e88ce-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e88ce-135">-WhatIf</span></span>
<span data-ttu-id="e88ce-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e88ce-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e88ce-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e88ce-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e88ce-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e88ce-138">CommonParameters</span></span>
<span data-ttu-id="e88ce-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e88ce-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e88ce-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e88ce-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e88ce-141">輸入</span><span class="sxs-lookup"><span data-stu-id="e88ce-141">INPUTS</span></span>

### <span data-ttu-id="e88ce-142">System.object</span><span class="sxs-lookup"><span data-stu-id="e88ce-142">System.String</span></span>

### <span data-ttu-id="e88ce-143">[RecommendedActionState]。 RecommendedAction。</span><span class="sxs-lookup"><span data-stu-id="e88ce-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span></span>

## <span data-ttu-id="e88ce-144">輸出</span><span class="sxs-lookup"><span data-stu-id="e88ce-144">OUTPUTS</span></span>

### <span data-ttu-id="e88ce-145">AzureSqlElasticPoolRecommendedActionModel 中的 [RecommendedAction]</span><span class="sxs-lookup"><span data-stu-id="e88ce-145">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlElasticPoolRecommendedActionModel</span></span>

## <span data-ttu-id="e88ce-146">筆記</span><span class="sxs-lookup"><span data-stu-id="e88ce-146">NOTES</span></span>
* <span data-ttu-id="e88ce-147">關鍵字： azure、azurerm、arm、資源、管理、manager、sql、elasticpool、mssql、advisor、recommendedaction</span><span class="sxs-lookup"><span data-stu-id="e88ce-147">Keywords: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="e88ce-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="e88ce-148">RELATED LINKS</span></span>

[<span data-ttu-id="e88ce-149">AzSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="e88ce-149">Get-AzSqlElasticPoolRecommendedAction</span></span>](./Get-AzSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="e88ce-150">Set-AzSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="e88ce-150">Set-AzSqlDatabaseRecommendedActionState</span></span>](./Set-AzSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="e88ce-151">Set-AzSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="e88ce-151">Set-AzSqlServerRecommendedActionState</span></span>](./Set-AzSqlServerRecommendedActionState.md)

[<span data-ttu-id="e88ce-152">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="e88ce-152">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
