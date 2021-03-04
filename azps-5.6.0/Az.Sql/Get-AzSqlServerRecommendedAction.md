---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BB513A53-48A0-4F8F-93F0-D3DFA2C3D523
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserverrecommendedaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerRecommendedAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerRecommendedAction.md
ms.openlocfilehash: 604caf4d39808e56d5f924f07f67e1c93007d9a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910582"
---
# <span data-ttu-id="0a0c2-101">Get-AzSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="0a0c2-101">Get-AzSqlServerRecommendedAction</span></span>

## <span data-ttu-id="0a0c2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0a0c2-102">SYNOPSIS</span></span>
<span data-ttu-id="0a0c2-103">為 Azure SQL Server Advisor 獲得一或多個建議動作。</span><span class="sxs-lookup"><span data-stu-id="0a0c2-103">Gets one or more recommended actions for an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="0a0c2-104">語法</span><span class="sxs-lookup"><span data-stu-id="0a0c2-104">SYNTAX</span></span>

```
Get-AzSqlServerRecommendedAction [-RecommendedActionName <String>] -ServerName <String> -AdvisorName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a0c2-105">描述</span><span class="sxs-lookup"><span data-stu-id="0a0c2-105">DESCRIPTION</span></span>
<span data-ttu-id="0a0c2-106">**Get-AzSqlServerRecomactionAction** Cmdlet 會針對 Azure SQL Server Advisor 取得一或多個建議動作。</span><span class="sxs-lookup"><span data-stu-id="0a0c2-106">The **Get-AzSqlServerRecommendedAction** cmdlet gets one or more recommended actions for an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="0a0c2-107">例子</span><span class="sxs-lookup"><span data-stu-id="0a0c2-107">EXAMPLES</span></span>

### <span data-ttu-id="0a0c2-108">範例 1：取得特定顧問的所有建議動作清單</span><span class="sxs-lookup"><span data-stu-id="0a0c2-108">Example 1: Get a list of  all recommended actions for a specific Advisor</span></span>
```
PS C:\>Get-AzSqlServerRecommendedAction -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex"
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

<span data-ttu-id="0a0c2-109">此命令會針對名稱為 wi-runner-australia-east 的伺服器，提供名為 CreateIndex 的 SQL Server 建議動作清單。</span><span class="sxs-lookup"><span data-stu-id="0a0c2-109">This command gets a list of all recommended actions of for the SQL Server Advisor named CreateIndex available for the server named wi-runner-australia-east.</span></span>

### <span data-ttu-id="0a0c2-110">範例 2：取得顧問的單一建議動作</span><span class="sxs-lookup"><span data-stu-id="0a0c2-110">Example 2: Get a single recommended action for an Advisor</span></span>
```
PS C:\>Get-AzSqlServerRecommendedAction -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -RecommendedActionName 
IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893
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

<span data-ttu-id="0a0c2-111">此命令會從 \[ CreateIndex IR_test_schema _ \] \[ test_table_0.0361551 _6C7AE8CC9C87E7FD5893建議的動作 \] 。</span><span class="sxs-lookup"><span data-stu-id="0a0c2-111">This command gets a recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 from the Advisor named CreateIndex.</span></span>

## <span data-ttu-id="0a0c2-112">參數</span><span class="sxs-lookup"><span data-stu-id="0a0c2-112">PARAMETERS</span></span>

### <span data-ttu-id="0a0c2-113">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="0a0c2-113">-AdvisorName</span></span>
<span data-ttu-id="0a0c2-114">指定此 Cmdlet 要求動作的顧問名稱。</span><span class="sxs-lookup"><span data-stu-id="0a0c2-114">Specifies the name of the advisor for which this cmdlet requests actions.</span></span>

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

### <span data-ttu-id="0a0c2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a0c2-115">-DefaultProfile</span></span>
<span data-ttu-id="0a0c2-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="0a0c2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0a0c2-117">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="0a0c2-117">-RecommendedActionName</span></span>
<span data-ttu-id="0a0c2-118">指定此 Cmdlet 獲得的建議動作名稱。</span><span class="sxs-lookup"><span data-stu-id="0a0c2-118">Specifies the name of the recommended action that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0a0c2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a0c2-119">-ResourceGroupName</span></span>
<span data-ttu-id="0a0c2-120">指定包含此伺服器之伺服器的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="0a0c2-120">Specifies the name of the resource group of the server that contains this server.</span></span>

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

### <span data-ttu-id="0a0c2-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0a0c2-121">-ServerName</span></span>
<span data-ttu-id="0a0c2-122">指定建議程式所屬的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="0a0c2-122">Specifies the name of the server the Advisor belongs to.</span></span>

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

### <span data-ttu-id="0a0c2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a0c2-123">CommonParameters</span></span>
<span data-ttu-id="0a0c2-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0a0c2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a0c2-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0a0c2-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a0c2-126">輸入</span><span class="sxs-lookup"><span data-stu-id="0a0c2-126">INPUTS</span></span>

### <span data-ttu-id="0a0c2-127">System.String</span><span class="sxs-lookup"><span data-stu-id="0a0c2-127">System.String</span></span>

## <span data-ttu-id="0a0c2-128">輸出</span><span class="sxs-lookup"><span data-stu-id="0a0c2-128">OUTPUTS</span></span>

### <span data-ttu-id="0a0c2-129">Microsoft.Azure.Commands.sql.recommendedAction.Model.AzureSqlServerRecomactionModel</span><span class="sxs-lookup"><span data-stu-id="0a0c2-129">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlServerRecommendedActionModel</span></span>

## <span data-ttu-id="0a0c2-130">筆記</span><span class="sxs-lookup"><span data-stu-id="0a0c2-130">NOTES</span></span>
* <span data-ttu-id="0a0c2-131">關鍵字：azure、azurerm、arm、resource、management、manager、sql、server、mssql、advisor、recommendedaction</span><span class="sxs-lookup"><span data-stu-id="0a0c2-131">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="0a0c2-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="0a0c2-132">RELATED LINKS</span></span>

[<span data-ttu-id="0a0c2-133">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="0a0c2-133">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="0a0c2-134">Set-AzSqlServerRecomactionActionState</span><span class="sxs-lookup"><span data-stu-id="0a0c2-134">Set-AzSqlServerRecommendedActionState</span></span>](./Set-AzSqlServerRecommendedActionState.md)

[<span data-ttu-id="0a0c2-135">Get-AzSqlElasticPoolRecomactionAction</span><span class="sxs-lookup"><span data-stu-id="0a0c2-135">Get-AzSqlElasticPoolRecommendedAction</span></span>](./Get-AzSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="0a0c2-136">Get-AzSqlDatabaseRecomactionAction</span><span class="sxs-lookup"><span data-stu-id="0a0c2-136">Get-AzSqlDatabaseRecommendedAction</span></span>](./Get-AzSqlDatabaseRecommendedAction.md)

[<span data-ttu-id="0a0c2-137">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="0a0c2-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
