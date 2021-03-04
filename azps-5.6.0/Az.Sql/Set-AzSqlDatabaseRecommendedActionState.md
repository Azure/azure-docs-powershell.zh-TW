---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BDBA3AA3-DCC6-4C83-84C8-EE6D93BFE1D3
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqldatabaserecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseRecommendedActionState.md
ms.openlocfilehash: f68aed09a0aef5e6edb83933bcef9827bd98420c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905750"
---
# <span data-ttu-id="f65ad-101">Set-AzSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="f65ad-101">Set-AzSqlDatabaseRecommendedActionState</span></span>

## <span data-ttu-id="f65ad-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f65ad-102">SYNOPSIS</span></span>
<span data-ttu-id="f65ad-103">更新 Azure SQL Database 建議的動作狀態。</span><span class="sxs-lookup"><span data-stu-id="f65ad-103">Updates the state of an Azure SQL Database recommended action.</span></span>

## <span data-ttu-id="f65ad-104">語法</span><span class="sxs-lookup"><span data-stu-id="f65ad-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -DatabaseName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f65ad-105">描述</span><span class="sxs-lookup"><span data-stu-id="f65ad-105">DESCRIPTION</span></span>
<span data-ttu-id="f65ad-106">**Set-AzSqlDatabaseRecomactionActionState** Cmdlet 會更新 Azure SQL 資料庫建議動作的狀態。</span><span class="sxs-lookup"><span data-stu-id="f65ad-106">The **Set-AzSqlDatabaseRecommendedActionState** cmdlet updates the state of an Azure SQL Database Recommended Action.</span></span>
<span data-ttu-id="f65ad-107">這可讓您根據新狀態來申請、還原或捨棄建議的動作。</span><span class="sxs-lookup"><span data-stu-id="f65ad-107">This allows a recommended action to be applied, reverted or discarded based on the new state.</span></span>

## <span data-ttu-id="f65ad-108">例子</span><span class="sxs-lookup"><span data-stu-id="f65ad-108">EXAMPLES</span></span>

### <span data-ttu-id="f65ad-109">範例 1：將建議的動作狀態適用于擱置中</span><span class="sxs-lookup"><span data-stu-id="f65ad-109">Example 1: Apply a recommended action state to pending</span></span>
```
PS C:\>Set-AzSqlDatabaseRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
DatabaseName               : WIRunner

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

<span data-ttu-id="f65ad-110">此命令會更新名為 \[ IR_test_schema \] _ \[ test_table_0.0361551 _6C7AE8CC9C87E7FD5893 之建議動作的狀態，該動作屬於名為 \] WIRunner 的資料庫，因此會更新為擱置中。</span><span class="sxs-lookup"><span data-stu-id="f65ad-110">This command updates the state of the recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 that belongs to the database named WIRunner to Pending.</span></span>

## <span data-ttu-id="f65ad-111">參數</span><span class="sxs-lookup"><span data-stu-id="f65ad-111">PARAMETERS</span></span>

### <span data-ttu-id="f65ad-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="f65ad-112">-AdvisorName</span></span>
<span data-ttu-id="f65ad-113">指定此建議動作所屬的建議程式名稱。</span><span class="sxs-lookup"><span data-stu-id="f65ad-113">Specifies the name of the advisor for which this recommended action belongs to.</span></span>

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

### <span data-ttu-id="f65ad-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f65ad-114">-DatabaseName</span></span>
<span data-ttu-id="f65ad-115">指定此 Cmdlet 會設定建議動作狀態的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="f65ad-115">Specifies the name of the database for which this cmdlet sets the recommended action state.</span></span>

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

### <span data-ttu-id="f65ad-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f65ad-116">-DefaultProfile</span></span>
<span data-ttu-id="f65ad-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="f65ad-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f65ad-118">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="f65ad-118">-RecommendedActionName</span></span>
<span data-ttu-id="f65ad-119">指定要更新之狀態的建議動作名稱。</span><span class="sxs-lookup"><span data-stu-id="f65ad-119">Specifies the name of the recommended action for which state is being updated.</span></span>

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

### <span data-ttu-id="f65ad-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f65ad-120">-ResourceGroupName</span></span>
<span data-ttu-id="f65ad-121">指定包含此資料庫之伺服器的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="f65ad-121">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="f65ad-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f65ad-122">-ServerName</span></span>
<span data-ttu-id="f65ad-123">指定資料庫位於的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="f65ad-123">Specifies the name of the server the database is in.</span></span>

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

### <span data-ttu-id="f65ad-124">-State</span><span class="sxs-lookup"><span data-stu-id="f65ad-124">-State</span></span>
<span data-ttu-id="f65ad-125">指定此 Cmdlet 更新建議動作狀態的新值。</span><span class="sxs-lookup"><span data-stu-id="f65ad-125">Specifies the new value to which this cmdlet updates the recommended action state.</span></span>
<span data-ttu-id="f65ad-126">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="f65ad-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f65ad-127">積極</span><span class="sxs-lookup"><span data-stu-id="f65ad-127">Active</span></span>
- <span data-ttu-id="f65ad-128">等待</span><span class="sxs-lookup"><span data-stu-id="f65ad-128">Pending</span></span>
- <span data-ttu-id="f65ad-129">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="f65ad-129">PendingRevert</span></span>
- <span data-ttu-id="f65ad-130">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="f65ad-130">RevertCancelled</span></span>
- <span data-ttu-id="f65ad-131">忽視</span><span class="sxs-lookup"><span data-stu-id="f65ad-131">Ignored</span></span>
- <span data-ttu-id="f65ad-132">解決</span><span class="sxs-lookup"><span data-stu-id="f65ad-132">Resolved</span></span>

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

### <span data-ttu-id="f65ad-133">-確認</span><span class="sxs-lookup"><span data-stu-id="f65ad-133">-Confirm</span></span>
<span data-ttu-id="f65ad-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f65ad-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f65ad-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f65ad-135">-WhatIf</span></span>
<span data-ttu-id="f65ad-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f65ad-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f65ad-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f65ad-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f65ad-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f65ad-138">CommonParameters</span></span>
<span data-ttu-id="f65ad-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f65ad-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f65ad-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f65ad-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f65ad-141">輸入</span><span class="sxs-lookup"><span data-stu-id="f65ad-141">INPUTS</span></span>

### <span data-ttu-id="f65ad-142">System.String</span><span class="sxs-lookup"><span data-stu-id="f65ad-142">System.String</span></span>

### <span data-ttu-id="f65ad-143">Microsoft.Azure.Commands.sql.recommendedAction.Cmdlet.RecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="f65ad-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span></span>

## <span data-ttu-id="f65ad-144">輸出</span><span class="sxs-lookup"><span data-stu-id="f65ad-144">OUTPUTS</span></span>

### <span data-ttu-id="f65ad-145">Microsoft.Azure.Commands.sql.RecommendedAction.Model.AzureSqlDatabaseRecomactionModel</span><span class="sxs-lookup"><span data-stu-id="f65ad-145">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlDatabaseRecommendedActionModel</span></span>

## <span data-ttu-id="f65ad-146">筆記</span><span class="sxs-lookup"><span data-stu-id="f65ad-146">NOTES</span></span>
* <span data-ttu-id="f65ad-147">關鍵字：azure、azurerm、arm、resource、management、manager、sql、database、mssql、advisor、recommendedaction</span><span class="sxs-lookup"><span data-stu-id="f65ad-147">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="f65ad-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="f65ad-148">RELATED LINKS</span></span>

[<span data-ttu-id="f65ad-149">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="f65ad-149">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="f65ad-150">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="f65ad-150">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="f65ad-151">Get-AzSqlServerRecomactionAction</span><span class="sxs-lookup"><span data-stu-id="f65ad-151">Get-AzSqlServerRecommendedAction</span></span>](./Get-AzSqlServerRecommendedAction.md)

[<span data-ttu-id="f65ad-152">Get-AzSqlElasticPoolRecomactionAction</span><span class="sxs-lookup"><span data-stu-id="f65ad-152">Get-AzSqlElasticPoolRecommendedAction</span></span>](./Get-AzSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="f65ad-153">Set-AzSqlElasticPoolRecomactionActionState</span><span class="sxs-lookup"><span data-stu-id="f65ad-153">Set-AzSqlElasticPoolRecommendedActionState</span></span>](./Set-AzSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="f65ad-154">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="f65ad-154">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="f65ad-155">Set-AzSqlElasticPoolRecomactionActionState</span><span class="sxs-lookup"><span data-stu-id="f65ad-155">Set-AzSqlElasticPoolRecommendedActionState</span></span>](./Set-AzSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="f65ad-156">Set-AzSqlServerRecomactionActionState</span><span class="sxs-lookup"><span data-stu-id="f65ad-156">Set-AzSqlServerRecommendedActionState</span></span>](./Set-AzSqlServerRecommendedActionState.md)

[<span data-ttu-id="f65ad-157">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="f65ad-157">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="f65ad-158">Set-AzSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="f65ad-158">Set-AzSqlServerAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlServerAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="f65ad-159">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="f65ad-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
