---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 26EC220C-5123-4CEF-8CC6-5FFD08F33481
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverrecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerRecommendedActionState.md
ms.openlocfilehash: 78366f70db7bd586e1e35566f167c7cae2c2dbf0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98279183"
---
# <span data-ttu-id="1012e-101">Set-AzSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="1012e-101">Set-AzSqlServerRecommendedActionState</span></span>

## <span data-ttu-id="1012e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1012e-102">SYNOPSIS</span></span>
<span data-ttu-id="1012e-103">更新 Azure SQL Server 建議動作的狀態。</span><span class="sxs-lookup"><span data-stu-id="1012e-103">Updates the state of an Azure SQL Server recommended action.</span></span>

## <span data-ttu-id="1012e-104">句法</span><span class="sxs-lookup"><span data-stu-id="1012e-104">SYNTAX</span></span>

```
Set-AzSqlServerRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1012e-105">說明</span><span class="sxs-lookup"><span data-stu-id="1012e-105">DESCRIPTION</span></span>
<span data-ttu-id="1012e-106">**AzSqlServerRecommendedActionState** Cmdlet 會更新 Azure SQL Server 建議動作的狀態。</span><span class="sxs-lookup"><span data-stu-id="1012e-106">The **Set-AzSqlServerRecommendedActionState** cmdlet updates state of an Azure SQL Server recommended action.</span></span>
<span data-ttu-id="1012e-107">這個 Cmdlet 會根據新的狀態來套用、還原或放棄建議的動作。</span><span class="sxs-lookup"><span data-stu-id="1012e-107">This cmdlet applies, reverts, or discards the recommended action based on the new state.</span></span>

## <span data-ttu-id="1012e-108">示例</span><span class="sxs-lookup"><span data-stu-id="1012e-108">EXAMPLES</span></span>

### <span data-ttu-id="1012e-109">Example1：將指定建議動作的狀態更新為 [擱置中]</span><span class="sxs-lookup"><span data-stu-id="1012e-109">Example1: Update the state of the specified recommended action to Pending</span></span>
```
PS C:\>Set-AzSqlServerRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
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

<span data-ttu-id="1012e-110">更新名為 "IR_ \[ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893" 設為 "擱置" 的伺服器建議動作狀態</span><span class="sxs-lookup"><span data-stu-id="1012e-110">Updates state of server recommended action named "IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893" to "Pending"</span></span>

## <span data-ttu-id="1012e-111">參數</span><span class="sxs-lookup"><span data-stu-id="1012e-111">PARAMETERS</span></span>

### <span data-ttu-id="1012e-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="1012e-112">-AdvisorName</span></span>
<span data-ttu-id="1012e-113">指定包含建議動作的顧問名稱。</span><span class="sxs-lookup"><span data-stu-id="1012e-113">Specifies the name of the advisor that contains the recommended action.</span></span>

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

### <span data-ttu-id="1012e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1012e-114">-DefaultProfile</span></span>
<span data-ttu-id="1012e-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="1012e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1012e-116">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="1012e-116">-RecommendedActionName</span></span>
<span data-ttu-id="1012e-117">指定此 Cmdlet 更新狀態的建議動作名稱。</span><span class="sxs-lookup"><span data-stu-id="1012e-117">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

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

### <span data-ttu-id="1012e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1012e-118">-ResourceGroupName</span></span>
<span data-ttu-id="1012e-119">指定伺服器資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1012e-119">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="1012e-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1012e-120">-ServerName</span></span>
<span data-ttu-id="1012e-121">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="1012e-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="1012e-122">-State</span><span class="sxs-lookup"><span data-stu-id="1012e-122">-State</span></span>
<span data-ttu-id="1012e-123">指定此 Cmdlet 更新建議動作狀態的新值。</span><span class="sxs-lookup"><span data-stu-id="1012e-123">Specifies the new value to which this cmdlet updates the recommended action state.</span></span>
<span data-ttu-id="1012e-124">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="1012e-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1012e-125">有效</span><span class="sxs-lookup"><span data-stu-id="1012e-125">Active</span></span>
- <span data-ttu-id="1012e-126">擱置</span><span class="sxs-lookup"><span data-stu-id="1012e-126">Pending</span></span>
- <span data-ttu-id="1012e-127">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="1012e-127">PendingRevert</span></span>
- <span data-ttu-id="1012e-128">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="1012e-128">RevertCancelled</span></span>
- <span data-ttu-id="1012e-129">忽視</span><span class="sxs-lookup"><span data-stu-id="1012e-129">Ignored</span></span>
- <span data-ttu-id="1012e-130">已</span><span class="sxs-lookup"><span data-stu-id="1012e-130">Resolved</span></span>

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

### <span data-ttu-id="1012e-131">-確認</span><span class="sxs-lookup"><span data-stu-id="1012e-131">-Confirm</span></span>
<span data-ttu-id="1012e-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1012e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1012e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1012e-133">-WhatIf</span></span>
<span data-ttu-id="1012e-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1012e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1012e-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1012e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1012e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1012e-136">CommonParameters</span></span>
<span data-ttu-id="1012e-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1012e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1012e-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1012e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1012e-139">輸入</span><span class="sxs-lookup"><span data-stu-id="1012e-139">INPUTS</span></span>

### <span data-ttu-id="1012e-140">System.object</span><span class="sxs-lookup"><span data-stu-id="1012e-140">System.String</span></span>

### <span data-ttu-id="1012e-141">[RecommendedActionState]。 RecommendedAction。</span><span class="sxs-lookup"><span data-stu-id="1012e-141">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span></span>

## <span data-ttu-id="1012e-142">輸出</span><span class="sxs-lookup"><span data-stu-id="1012e-142">OUTPUTS</span></span>

### <span data-ttu-id="1012e-143">AzureSqlServerRecommendedActionModel 中的 [RecommendedAction]</span><span class="sxs-lookup"><span data-stu-id="1012e-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlServerRecommendedActionModel</span></span>

## <span data-ttu-id="1012e-144">筆記</span><span class="sxs-lookup"><span data-stu-id="1012e-144">NOTES</span></span>
* <span data-ttu-id="1012e-145">關鍵字： azure，azurerm，arm，資源，管理，管理員，sql，server，mssql，advisor，recommendedaction</span><span class="sxs-lookup"><span data-stu-id="1012e-145">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="1012e-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="1012e-146">RELATED LINKS</span></span>

[<span data-ttu-id="1012e-147">AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="1012e-147">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="1012e-148">AzSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="1012e-148">Get-AzSqlServerRecommendedAction</span></span>](./Get-AzSqlServerRecommendedAction.md)

[<span data-ttu-id="1012e-149">Set-AzSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="1012e-149">Set-AzSqlDatabaseRecommendedActionState</span></span>](./Set-AzSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="1012e-150">Set-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="1012e-150">Set-AzSqlElasticPoolRecommendedActionState</span></span>](./Set-AzSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="1012e-151">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="1012e-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
