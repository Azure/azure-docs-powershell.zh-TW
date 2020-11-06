---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BDBA3AA3-DCC6-4C83-84C8-EE6D93BFE1D3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseRecommendedActionState.md
ms.openlocfilehash: d31af9321a474c1261b2ed75138696d9f1a45461
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447917"
---
# <span data-ttu-id="a9c58-101">Set-AzureRmSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="a9c58-101">Set-AzureRmSqlDatabaseRecommendedActionState</span></span>

## <span data-ttu-id="a9c58-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a9c58-102">SYNOPSIS</span></span>
<span data-ttu-id="a9c58-103">更新 Azure SQL Database 建議動作的狀態。</span><span class="sxs-lookup"><span data-stu-id="a9c58-103">Updates the state of an Azure SQL Database recommended action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9c58-104">句法</span><span class="sxs-lookup"><span data-stu-id="a9c58-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -DatabaseName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9c58-105">說明</span><span class="sxs-lookup"><span data-stu-id="a9c58-105">DESCRIPTION</span></span>
<span data-ttu-id="a9c58-106">**AzureRmSqlDatabaseRecommendedActionState** Cmdlet 會更新 Azure SQL Database 建議動作的狀態。</span><span class="sxs-lookup"><span data-stu-id="a9c58-106">The **Set-AzureRmSqlDatabaseRecommendedActionState** cmdlet updates the state of an Azure SQL Database Recommended Action.</span></span>
<span data-ttu-id="a9c58-107">這樣就能根據新的狀態來套用、還原或放棄建議的動作。</span><span class="sxs-lookup"><span data-stu-id="a9c58-107">This allows a recommended action to be applied, reverted or discarded based on the new state.</span></span>

## <span data-ttu-id="a9c58-108">示例</span><span class="sxs-lookup"><span data-stu-id="a9c58-108">EXAMPLES</span></span>

### <span data-ttu-id="a9c58-109">範例1：將建議動作狀態套用至擱置</span><span class="sxs-lookup"><span data-stu-id="a9c58-109">Example 1: Apply a recommended action state to pending</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
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

<span data-ttu-id="a9c58-110">這個命令會將 \[ 屬於名為 WIRunner 之資料庫的 IR_ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893 的建議動作狀態更新為 [擱置中]。</span><span class="sxs-lookup"><span data-stu-id="a9c58-110">This command updates the state of the recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 that belongs to the database named WIRunner to Pending.</span></span>

## <span data-ttu-id="a9c58-111">參數</span><span class="sxs-lookup"><span data-stu-id="a9c58-111">PARAMETERS</span></span>

### <span data-ttu-id="a9c58-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="a9c58-112">-AdvisorName</span></span>
<span data-ttu-id="a9c58-113">指定此建議動作所屬之 advisor 的名稱。</span><span class="sxs-lookup"><span data-stu-id="a9c58-113">Specifies the name of the advisor for which this recommended action belongs to.</span></span>

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

### <span data-ttu-id="a9c58-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a9c58-114">-DatabaseName</span></span>
<span data-ttu-id="a9c58-115">指定此 Cmdlet 設定建議動作狀態的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="a9c58-115">Specifies the name of the database for which this cmdlet sets the recommended action state.</span></span>

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

### <span data-ttu-id="a9c58-116">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="a9c58-116">-RecommendedActionName</span></span>
<span data-ttu-id="a9c58-117">指定要更新其狀態的建議動作的名稱。</span><span class="sxs-lookup"><span data-stu-id="a9c58-117">Specifies the name of the recommended action for which state is being updated.</span></span>

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

### <span data-ttu-id="a9c58-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9c58-118">-ResourceGroupName</span></span>
<span data-ttu-id="a9c58-119">指定包含此資料庫之伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a9c58-119">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="a9c58-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a9c58-120">-ServerName</span></span>
<span data-ttu-id="a9c58-121">指定資料庫所在的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="a9c58-121">Specifies the name of the server the database is in.</span></span>

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

### <span data-ttu-id="a9c58-122">-State</span><span class="sxs-lookup"><span data-stu-id="a9c58-122">-State</span></span>
<span data-ttu-id="a9c58-123">指定此 Cmdlet 更新建議動作狀態的新值。</span><span class="sxs-lookup"><span data-stu-id="a9c58-123">Specifies the new value to which this cmdlet updates the recommended action state.</span></span>

<span data-ttu-id="a9c58-124">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a9c58-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a9c58-125">有效</span><span class="sxs-lookup"><span data-stu-id="a9c58-125">Active</span></span>
- <span data-ttu-id="a9c58-126">擱置</span><span class="sxs-lookup"><span data-stu-id="a9c58-126">Pending</span></span>
- <span data-ttu-id="a9c58-127">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="a9c58-127">PendingRevert</span></span>
- <span data-ttu-id="a9c58-128">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="a9c58-128">RevertCancelled</span></span>
- <span data-ttu-id="a9c58-129">忽視</span><span class="sxs-lookup"><span data-stu-id="a9c58-129">Ignored</span></span>
- <span data-ttu-id="a9c58-130">已</span><span class="sxs-lookup"><span data-stu-id="a9c58-130">Resolved</span></span>

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

### <span data-ttu-id="a9c58-131">-確認</span><span class="sxs-lookup"><span data-stu-id="a9c58-131">-Confirm</span></span>
<span data-ttu-id="a9c58-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a9c58-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9c58-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9c58-133">-WhatIf</span></span>
<span data-ttu-id="a9c58-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a9c58-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9c58-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a9c58-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9c58-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9c58-136">-DefaultProfile</span></span>
<span data-ttu-id="a9c58-137">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a9c58-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9c58-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9c58-138">CommonParameters</span></span>
<span data-ttu-id="a9c58-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a9c58-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9c58-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a9c58-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9c58-141">輸入</span><span class="sxs-lookup"><span data-stu-id="a9c58-141">INPUTS</span></span>

## <span data-ttu-id="a9c58-142">輸出</span><span class="sxs-lookup"><span data-stu-id="a9c58-142">OUTPUTS</span></span>

### <span data-ttu-id="a9c58-143">AzureSqlDatabaseRecommendedActionModel 中的 [RecommendedAction]</span><span class="sxs-lookup"><span data-stu-id="a9c58-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlDatabaseRecommendedActionModel</span></span>

## <span data-ttu-id="a9c58-144">筆記</span><span class="sxs-lookup"><span data-stu-id="a9c58-144">NOTES</span></span>
* <span data-ttu-id="a9c58-145">關鍵字： azure，azurerm，arm，資源，管理，管理員，sql，資料庫，mssql，advisor，recommendedaction</span><span class="sxs-lookup"><span data-stu-id="a9c58-145">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="a9c58-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="a9c58-146">RELATED LINKS</span></span>

[<span data-ttu-id="a9c58-147">AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="a9c58-147">Get-AzureRmSqlServerAdvisor</span></span>](./Get-AzureRmSqlServerAdvisor.md)

[<span data-ttu-id="a9c58-148">AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="a9c58-148">Get-AzureRmSqlElasticPoolAdvisor</span></span>](./Get-AzureRmSqlElasticPoolAdvisor.md)

[<span data-ttu-id="a9c58-149">AzureRmSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="a9c58-149">Get-AzureRmSqlServerRecommendedAction</span></span>](./Get-AzureRmSqlServerRecommendedAction.md)

[<span data-ttu-id="a9c58-150">AzureRmSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="a9c58-150">Get-AzureRmSqlElasticPoolRecommendedAction</span></span>](./Get-AzureRmSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="a9c58-151">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="a9c58-151">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>](./Set-AzureRmSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="a9c58-152">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="a9c58-152">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="a9c58-153">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="a9c58-153">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>](./Set-AzureRmSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="a9c58-154">Set-AzureRmSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="a9c58-154">Set-AzureRmSqlServerRecommendedActionState</span></span>](./Set-AzureRmSqlServerRecommendedActionState.md)

[<span data-ttu-id="a9c58-155">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="a9c58-155">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="a9c58-156">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="a9c58-156">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span></span>](./Set-AzureRmSqlServerAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="a9c58-157">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="a9c58-157">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
