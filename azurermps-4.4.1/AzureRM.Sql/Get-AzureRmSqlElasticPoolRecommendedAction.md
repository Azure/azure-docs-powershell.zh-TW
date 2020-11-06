---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 3FC9E586-3962-437E-B89F-BB4EA1FBF403
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolRecommendedAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolRecommendedAction.md
ms.openlocfilehash: b5ce9419606faf2775ab9a921e5998f40ab3c4fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448837"
---
# <span data-ttu-id="85ec9-101">Get-AzureRmSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="85ec9-101">Get-AzureRmSqlElasticPoolRecommendedAction</span></span>

## <span data-ttu-id="85ec9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="85ec9-102">SYNOPSIS</span></span>
<span data-ttu-id="85ec9-103">針對 Azure SQL 彈性 Pool Advisor 取得一或多個建議的動作。</span><span class="sxs-lookup"><span data-stu-id="85ec9-103">Gets one or more recommended actions for an Azure SQL Elastic Pool Advisor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85ec9-104">句法</span><span class="sxs-lookup"><span data-stu-id="85ec9-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolRecommendedAction [-RecommendedActionName <String>] -ServerName <String>
 -ElasticPoolName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85ec9-105">說明</span><span class="sxs-lookup"><span data-stu-id="85ec9-105">DESCRIPTION</span></span>
<span data-ttu-id="85ec9-106">**AzureRmSqlElasticPoolRecommendedAction** Cmdlet 會針對 Azure SQL 彈性 Pool Advisor 取得一或多個建議的動作。</span><span class="sxs-lookup"><span data-stu-id="85ec9-106">The **Get-AzureRmSqlElasticPoolRecommendedAction** cmdlet gets one or more recommended actions for an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="85ec9-107">示例</span><span class="sxs-lookup"><span data-stu-id="85ec9-107">EXAMPLES</span></span>

### <span data-ttu-id="85ec9-108">範例1：列出 Advisor 的所有建議動作</span><span class="sxs-lookup"><span data-stu-id="85ec9-108">Example 1: List all recommended actions for an Advisor</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolRecommendedAction -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex"
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

ElasticPoolName            : WIRunnerPool
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

ElasticPoolName            : WIRunnerPool
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

<span data-ttu-id="85ec9-109">這個命令會從名為 WIRunnerPool 的彈性池中取得名為「CreateIndex」的顧問所有建議動作清單。</span><span class="sxs-lookup"><span data-stu-id="85ec9-109">This command gets a list of all recommended actions of the Advisor named CreateIndex available for the elastic pool named WIRunnerPool.</span></span>

### <span data-ttu-id="85ec9-110">範例2：取得 Advisor 的單一建議動作</span><span class="sxs-lookup"><span data-stu-id="85ec9-110">Example 2: Get a single recommended action for an Advisor</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolRecommendedAction -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893"
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

<span data-ttu-id="85ec9-111">這個命令會 \[ \] \[ \] 從名為 CreateIndex 的 Advisor 中取得名為 IR_ test_schema _ test_table_0 .0361551 _6C7AE8CC9C87E7FD5893 的建議動作。</span><span class="sxs-lookup"><span data-stu-id="85ec9-111">This command gets the recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 from the Advisor named CreateIndex.</span></span>

## <span data-ttu-id="85ec9-112">參數</span><span class="sxs-lookup"><span data-stu-id="85ec9-112">PARAMETERS</span></span>

### <span data-ttu-id="85ec9-113">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="85ec9-113">-AdvisorName</span></span>
<span data-ttu-id="85ec9-114">指定此 Cmdlet 要求建議動作的顧問名稱。</span><span class="sxs-lookup"><span data-stu-id="85ec9-114">Specifies the name of the advisor for which this cmdlet requests recommended actions.</span></span>

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

### <span data-ttu-id="85ec9-115">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="85ec9-115">-ElasticPoolName</span></span>
<span data-ttu-id="85ec9-116">指定此 Cmdlet 要求建議動作的彈性池的名稱。</span><span class="sxs-lookup"><span data-stu-id="85ec9-116">Specifies the name of the elastic pool for which this cmdlet requests recommended actions.</span></span>

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

### <span data-ttu-id="85ec9-117">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="85ec9-117">-RecommendedActionName</span></span>
<span data-ttu-id="85ec9-118">指定此 Cmdlet 所取得之建議動作的名稱。</span><span class="sxs-lookup"><span data-stu-id="85ec9-118">Specifies the name of the recommended action that this cmdlet gets.</span></span>

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

### <span data-ttu-id="85ec9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85ec9-119">-ResourceGroupName</span></span>
<span data-ttu-id="85ec9-120">指定包含此彈性池之伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="85ec9-120">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="85ec9-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="85ec9-121">-ServerName</span></span>
<span data-ttu-id="85ec9-122">指定彈性池所在的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="85ec9-122">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="85ec9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85ec9-123">-DefaultProfile</span></span>
<span data-ttu-id="85ec9-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="85ec9-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85ec9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85ec9-125">CommonParameters</span></span>
<span data-ttu-id="85ec9-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="85ec9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85ec9-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="85ec9-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85ec9-128">輸入</span><span class="sxs-lookup"><span data-stu-id="85ec9-128">INPUTS</span></span>

## <span data-ttu-id="85ec9-129">輸出</span><span class="sxs-lookup"><span data-stu-id="85ec9-129">OUTPUTS</span></span>

### <span data-ttu-id="85ec9-130">AzureSqlElasticPoolRecommendedActionModel 中的 [RecommendedAction]</span><span class="sxs-lookup"><span data-stu-id="85ec9-130">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlElasticPoolRecommendedActionModel</span></span>

## <span data-ttu-id="85ec9-131">筆記</span><span class="sxs-lookup"><span data-stu-id="85ec9-131">NOTES</span></span>
* <span data-ttu-id="85ec9-132">關鍵字： azure、azurerm、arm、資源、管理、manager、sql、elasticpool、mssql、advisor、recommendedaction</span><span class="sxs-lookup"><span data-stu-id="85ec9-132">Keywords: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="85ec9-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="85ec9-133">RELATED LINKS</span></span>

[<span data-ttu-id="85ec9-134">AzureRmSqlDatabaseRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="85ec9-134">Get-AzureRmSqlDatabaseRecommendedAction</span></span>](./Get-AzureRmSqlDatabaseRecommendedAction.md)

[<span data-ttu-id="85ec9-135">AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="85ec9-135">Get-AzureRmSqlElasticPoolAdvisor</span></span>](./Get-AzureRmSqlElasticPoolAdvisor.md)

[<span data-ttu-id="85ec9-136">AzureRmSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="85ec9-136">Get-AzureRmSqlServerRecommendedAction</span></span>](./Get-AzureRmSqlServerRecommendedAction.md)

[<span data-ttu-id="85ec9-137">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="85ec9-137">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>](./Set-AzureRmSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="85ec9-138">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="85ec9-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)