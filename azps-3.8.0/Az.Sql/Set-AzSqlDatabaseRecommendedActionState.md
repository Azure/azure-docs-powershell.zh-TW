---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BDBA3AA3-DCC6-4C83-84C8-EE6D93BFE1D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaserecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseRecommendedActionState.md
ms.openlocfilehash: 6d634760080e3fb26153b747e733369b20bc8336
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93798265"
---
# <span data-ttu-id="93e89-101">Set-AzSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="93e89-101">Set-AzSqlDatabaseRecommendedActionState</span></span>

## <span data-ttu-id="93e89-102">摘要</span><span class="sxs-lookup"><span data-stu-id="93e89-102">SYNOPSIS</span></span>
<span data-ttu-id="93e89-103">更新 Azure SQL Database 建議動作的狀態。</span><span class="sxs-lookup"><span data-stu-id="93e89-103">Updates the state of an Azure SQL Database recommended action.</span></span>

## <span data-ttu-id="93e89-104">句法</span><span class="sxs-lookup"><span data-stu-id="93e89-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -DatabaseName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93e89-105">說明</span><span class="sxs-lookup"><span data-stu-id="93e89-105">DESCRIPTION</span></span>
<span data-ttu-id="93e89-106">**AzSqlDatabaseRecommendedActionState** Cmdlet 會更新 Azure SQL Database 建議動作的狀態。</span><span class="sxs-lookup"><span data-stu-id="93e89-106">The **Set-AzSqlDatabaseRecommendedActionState** cmdlet updates the state of an Azure SQL Database Recommended Action.</span></span>
<span data-ttu-id="93e89-107">這樣就能根據新的狀態來套用、還原或放棄建議的動作。</span><span class="sxs-lookup"><span data-stu-id="93e89-107">This allows a recommended action to be applied, reverted or discarded based on the new state.</span></span>

## <span data-ttu-id="93e89-108">示例</span><span class="sxs-lookup"><span data-stu-id="93e89-108">EXAMPLES</span></span>

### <span data-ttu-id="93e89-109">範例1：將建議動作狀態套用至擱置</span><span class="sxs-lookup"><span data-stu-id="93e89-109">Example 1: Apply a recommended action state to pending</span></span>
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

<span data-ttu-id="93e89-110">這個命令會將 \[ 屬於名為 WIRunner 之資料庫的 IR_ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893 的建議動作狀態更新為 [擱置中]。</span><span class="sxs-lookup"><span data-stu-id="93e89-110">This command updates the state of the recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 that belongs to the database named WIRunner to Pending.</span></span>

## <span data-ttu-id="93e89-111">參數</span><span class="sxs-lookup"><span data-stu-id="93e89-111">PARAMETERS</span></span>

### <span data-ttu-id="93e89-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="93e89-112">-AdvisorName</span></span>
<span data-ttu-id="93e89-113">指定此建議動作所屬之 advisor 的名稱。</span><span class="sxs-lookup"><span data-stu-id="93e89-113">Specifies the name of the advisor for which this recommended action belongs to.</span></span>

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

### <span data-ttu-id="93e89-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="93e89-114">-DatabaseName</span></span>
<span data-ttu-id="93e89-115">指定此 Cmdlet 設定建議動作狀態的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="93e89-115">Specifies the name of the database for which this cmdlet sets the recommended action state.</span></span>

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

### <span data-ttu-id="93e89-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93e89-116">-DefaultProfile</span></span>
<span data-ttu-id="93e89-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="93e89-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="93e89-118">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="93e89-118">-RecommendedActionName</span></span>
<span data-ttu-id="93e89-119">指定要更新其狀態的建議動作的名稱。</span><span class="sxs-lookup"><span data-stu-id="93e89-119">Specifies the name of the recommended action for which state is being updated.</span></span>

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

### <span data-ttu-id="93e89-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93e89-120">-ResourceGroupName</span></span>
<span data-ttu-id="93e89-121">指定包含此資料庫之伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="93e89-121">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="93e89-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="93e89-122">-ServerName</span></span>
<span data-ttu-id="93e89-123">指定資料庫所在的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="93e89-123">Specifies the name of the server the database is in.</span></span>

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

### <span data-ttu-id="93e89-124">-State</span><span class="sxs-lookup"><span data-stu-id="93e89-124">-State</span></span>
<span data-ttu-id="93e89-125">指定此 Cmdlet 更新建議動作狀態的新值。</span><span class="sxs-lookup"><span data-stu-id="93e89-125">Specifies the new value to which this cmdlet updates the recommended action state.</span></span>
<span data-ttu-id="93e89-126">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="93e89-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="93e89-127">有效</span><span class="sxs-lookup"><span data-stu-id="93e89-127">Active</span></span>
- <span data-ttu-id="93e89-128">擱置</span><span class="sxs-lookup"><span data-stu-id="93e89-128">Pending</span></span>
- <span data-ttu-id="93e89-129">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="93e89-129">PendingRevert</span></span>
- <span data-ttu-id="93e89-130">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="93e89-130">RevertCancelled</span></span>
- <span data-ttu-id="93e89-131">忽視</span><span class="sxs-lookup"><span data-stu-id="93e89-131">Ignored</span></span>
- <span data-ttu-id="93e89-132">已</span><span class="sxs-lookup"><span data-stu-id="93e89-132">Resolved</span></span>

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

### <span data-ttu-id="93e89-133">-確認</span><span class="sxs-lookup"><span data-stu-id="93e89-133">-Confirm</span></span>
<span data-ttu-id="93e89-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="93e89-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93e89-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93e89-135">-WhatIf</span></span>
<span data-ttu-id="93e89-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="93e89-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93e89-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="93e89-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93e89-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93e89-138">CommonParameters</span></span>
<span data-ttu-id="93e89-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="93e89-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93e89-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="93e89-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93e89-141">輸入</span><span class="sxs-lookup"><span data-stu-id="93e89-141">INPUTS</span></span>

### <span data-ttu-id="93e89-142">System.object</span><span class="sxs-lookup"><span data-stu-id="93e89-142">System.String</span></span>

### <span data-ttu-id="93e89-143">[RecommendedActionState]。 RecommendedAction。</span><span class="sxs-lookup"><span data-stu-id="93e89-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span></span>

## <span data-ttu-id="93e89-144">輸出</span><span class="sxs-lookup"><span data-stu-id="93e89-144">OUTPUTS</span></span>

### <span data-ttu-id="93e89-145">AzureSqlDatabaseRecommendedActionModel 中的 [RecommendedAction]</span><span class="sxs-lookup"><span data-stu-id="93e89-145">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlDatabaseRecommendedActionModel</span></span>

## <span data-ttu-id="93e89-146">筆記</span><span class="sxs-lookup"><span data-stu-id="93e89-146">NOTES</span></span>
* <span data-ttu-id="93e89-147">關鍵字： azure，azurerm，arm，資源，管理，管理員，sql，資料庫，mssql，advisor，recommendedaction</span><span class="sxs-lookup"><span data-stu-id="93e89-147">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="93e89-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="93e89-148">RELATED LINKS</span></span>

[<span data-ttu-id="93e89-149">AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="93e89-149">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="93e89-150">AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="93e89-150">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="93e89-151">AzSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="93e89-151">Get-AzSqlServerRecommendedAction</span></span>](./Get-AzSqlServerRecommendedAction.md)

[<span data-ttu-id="93e89-152">AzSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="93e89-152">Get-AzSqlElasticPoolRecommendedAction</span></span>](./Get-AzSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="93e89-153">Set-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="93e89-153">Set-AzSqlElasticPoolRecommendedActionState</span></span>](./Set-AzSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="93e89-154">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="93e89-154">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="93e89-155">Set-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="93e89-155">Set-AzSqlElasticPoolRecommendedActionState</span></span>](./Set-AzSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="93e89-156">Set-AzSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="93e89-156">Set-AzSqlServerRecommendedActionState</span></span>](./Set-AzSqlServerRecommendedActionState.md)

[<span data-ttu-id="93e89-157">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="93e89-157">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="93e89-158">Set-AzSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="93e89-158">Set-AzSqlServerAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlServerAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="93e89-159">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="93e89-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)