---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: EF6C862B-A89C-48AB-A590-92CFA387305F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaserecommendedaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseRecommendedAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseRecommendedAction.md
ms.openlocfilehash: fc54e470ed79593b40d25fdfc4cf655a0a8f44d4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98282399"
---
# <span data-ttu-id="a5ad1-101">Get-AzSqlDatabaseRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="a5ad1-101">Get-AzSqlDatabaseRecommendedAction</span></span>

## <span data-ttu-id="a5ad1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a5ad1-102">SYNOPSIS</span></span>
<span data-ttu-id="a5ad1-103">針對 Azure SQL Database Advisor 取得一或多個建議的動作。</span><span class="sxs-lookup"><span data-stu-id="a5ad1-103">Gets one or more recommended actions for an Azure SQL Database Advisor.</span></span>

## <span data-ttu-id="a5ad1-104">句法</span><span class="sxs-lookup"><span data-stu-id="a5ad1-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseRecommendedAction [-RecommendedActionName <String>] -ServerName <String>
 -DatabaseName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5ad1-105">說明</span><span class="sxs-lookup"><span data-stu-id="a5ad1-105">DESCRIPTION</span></span>
<span data-ttu-id="a5ad1-106">**AzSqlDatabaseRecommendedAction** Cmdlet 會針對 Azure SQL Database Advisor 取得一或多個建議的動作。</span><span class="sxs-lookup"><span data-stu-id="a5ad1-106">The **Get-AzSqlDatabaseRecommendedAction** cmdlet gets one or more recommended actions for an Azure SQL Database Advisor.</span></span>

## <span data-ttu-id="a5ad1-107">示例</span><span class="sxs-lookup"><span data-stu-id="a5ad1-107">EXAMPLES</span></span>

### <span data-ttu-id="a5ad1-108">範例1：列出 Advisor 的所有建議動作</span><span class="sxs-lookup"><span data-stu-id="a5ad1-108">Example 1: List all the recommended actions for an Advisor</span></span>
```
PS C:\>Get-AzSqlDatabaseRecommendedAction -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex"
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

DatabaseName               : WIRunner
ResourceGroupName          : WIRunnersProd
ServerName                 : wi-runner-australia-east
AdvisorName                : CreateIndex
RecommendedActionName      : IR_[test_schema]_[test_table_0.236046]_6C7AE8CC9C87E7FD5893
Details                    : {[indexName, nci_wi_test_table_0.236046_6C7AE8CC9C87E7FD5893], [indexType, NONCLUSTERED], 
                             [schema, [test_schema]], [table, [test_table_0.236046]]...} 
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
ObservedImpact             : {SpaceChange}
RecommendationReason       : 
RevertActionDuration       : 
RevertActionInitiatedBy    : 
RevertActionInitiatedTime  : 
RevertActionStartTime      : 
Score                      : 3
State                      : Microsoft.Azure.Management.Sql.Models.RecommendedActionStateInfo
TimeSeries                 : {}
ValidSince                 : 4/21/2016 3:24:47 PM
DatabaseName               : WIRunner
ResourceGroupName          : WIRunnersProd
ServerName                 : wi-runner-australia-east
AdvisorName                : CreateIndex
RecommendedActionName      : IR_[test_schema]_[test_table_0.239359]_6C7AE8CC9C87E7FD5893
Details                    : {[indexName, nci_wi_test_table_0.239359_6C7AE8CC9C87E7FD5893], [indexType, NONCLUSTERED], 
                             [schema, [test_schema]], [table, [test_table_0.239359]]...} 
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
RevertActionDuration       : PT10S
RevertActionInitiatedBy    : System
RevertActionInitiatedTime  : 4/21/2016 3:24:47 PM
RevertActionStartTime      : 4/21/2016 3:24:47 PM
Score                      : 3
State                      : Microsoft.Azure.Management.Sql.Models.RecommendedActionStateInfo
TimeSeries                 : {}
ValidSince                 : 4/21/2016 3:24:47 PM
```

<span data-ttu-id="a5ad1-109">這個命令會從名為 [wi-東] 的資料庫中取得名為「CreateIndex」的顧問所有建議動作清單。</span><span class="sxs-lookup"><span data-stu-id="a5ad1-109">This command gets a list of all recommended actions of the Advisor named CreateIndex available for the database named wi-runner-australia-east.</span></span>

### <span data-ttu-id="a5ad1-110">範例2：取得 Advisor 的單一建議動作</span><span class="sxs-lookup"><span data-stu-id="a5ad1-110">Example 2: Get a single recommended action for an Advisor</span></span>
```
PS C:\>Get-AzSqlDatabaseRecommendedAction -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893"
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

<span data-ttu-id="a5ad1-111">這個命令會取得名為 CreateIndex 之 \[ Advisor IR_ test_schema \] _ \[ test_table_0 .0361551 _6C7AE8CC9C87E7FD5893 的建議動作 \] 。</span><span class="sxs-lookup"><span data-stu-id="a5ad1-111">This command gets the recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 for the Advisor named CreateIndex.</span></span>

## <span data-ttu-id="a5ad1-112">參數</span><span class="sxs-lookup"><span data-stu-id="a5ad1-112">PARAMETERS</span></span>

### <span data-ttu-id="a5ad1-113">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="a5ad1-113">-AdvisorName</span></span>
<span data-ttu-id="a5ad1-114">指定此 Cmdlet 要求建議動作的顧問名稱。</span><span class="sxs-lookup"><span data-stu-id="a5ad1-114">Specifies the name of the Advisor for which this cmdlet requests recommended actions.</span></span>

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

### <span data-ttu-id="a5ad1-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a5ad1-115">-DatabaseName</span></span>
<span data-ttu-id="a5ad1-116">指定此 Cmdlet 要求建議動作的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="a5ad1-116">Specifies the name of the database for which this cmdlet requests recommended actions.</span></span>

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

### <span data-ttu-id="a5ad1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5ad1-117">-DefaultProfile</span></span>
<span data-ttu-id="a5ad1-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a5ad1-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a5ad1-119">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="a5ad1-119">-RecommendedActionName</span></span>
<span data-ttu-id="a5ad1-120">指定此 Cmdlet 所取得之建議動作的名稱。</span><span class="sxs-lookup"><span data-stu-id="a5ad1-120">Specifies the name of the recommended action that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5ad1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5ad1-121">-ResourceGroupName</span></span>
<span data-ttu-id="a5ad1-122">指定包含此資料庫之伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a5ad1-122">Specifies name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="a5ad1-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a5ad1-123">-ServerName</span></span>
<span data-ttu-id="a5ad1-124">指定資料庫所在的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="a5ad1-124">Specifies the name of the server the database is in.</span></span>

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

### <span data-ttu-id="a5ad1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5ad1-125">CommonParameters</span></span>
<span data-ttu-id="a5ad1-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a5ad1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5ad1-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a5ad1-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5ad1-128">輸入</span><span class="sxs-lookup"><span data-stu-id="a5ad1-128">INPUTS</span></span>

### <span data-ttu-id="a5ad1-129">System.object</span><span class="sxs-lookup"><span data-stu-id="a5ad1-129">System.String</span></span>

## <span data-ttu-id="a5ad1-130">輸出</span><span class="sxs-lookup"><span data-stu-id="a5ad1-130">OUTPUTS</span></span>

### <span data-ttu-id="a5ad1-131">AzureSqlDatabaseRecommendedActionModel 中的 [RecommendedAction]</span><span class="sxs-lookup"><span data-stu-id="a5ad1-131">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlDatabaseRecommendedActionModel</span></span>

## <span data-ttu-id="a5ad1-132">筆記</span><span class="sxs-lookup"><span data-stu-id="a5ad1-132">NOTES</span></span>
* <span data-ttu-id="a5ad1-133">關鍵字： azure，azurerm，arm，資源，管理，管理員，sql，資料庫，mssql，advisor，recommendedaction</span><span class="sxs-lookup"><span data-stu-id="a5ad1-133">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="a5ad1-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="a5ad1-134">RELATED LINKS</span></span>

[<span data-ttu-id="a5ad1-135">AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="a5ad1-135">Get-AzSqlDatabaseAdvisor</span></span>](./Get-AzSqlDatabaseAdvisor.md)

[<span data-ttu-id="a5ad1-136">AzSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="a5ad1-136">Get-AzSqlServerRecommendedAction</span></span>](./Get-AzSqlServerRecommendedAction.md)

[<span data-ttu-id="a5ad1-137">Set-AzSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="a5ad1-137">Set-AzSqlDatabaseRecommendedActionState</span></span>](./Set-AzSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="a5ad1-138">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="a5ad1-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
