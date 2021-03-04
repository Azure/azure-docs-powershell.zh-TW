---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 5AAB22C6-8E3C-4BDC-8A54-DA5A9906B762
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabaseadvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvisor.md
ms.openlocfilehash: d946b6b324247a46760f762c4631419b6c6aac59
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905809"
---
# <span data-ttu-id="df580-101">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="df580-101">Get-AzSqlDatabaseAdvisor</span></span>

## <span data-ttu-id="df580-102">簡介</span><span class="sxs-lookup"><span data-stu-id="df580-102">SYNOPSIS</span></span>
<span data-ttu-id="df580-103">為 Azure SQL 資料庫獲得一或多個顧問。</span><span class="sxs-lookup"><span data-stu-id="df580-103">Gets one or more Advisors for an Azure SQL Database.</span></span>

## <span data-ttu-id="df580-104">語法</span><span class="sxs-lookup"><span data-stu-id="df580-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 -DatabaseName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="df580-105">描述</span><span class="sxs-lookup"><span data-stu-id="df580-105">DESCRIPTION</span></span>
<span data-ttu-id="df580-106">**Get-AzSqlDatabaseAdvisor** Cmdlet 會針對 Azure SQL 資料庫取得一或多個 Azure SQL 資料庫建議程式。</span><span class="sxs-lookup"><span data-stu-id="df580-106">The **Get-AzSqlDatabaseAdvisor** cmdlet gets one or more Azure SQL Database Advisors for an Azure SQL Database.</span></span>

## <span data-ttu-id="df580-107">例子</span><span class="sxs-lookup"><span data-stu-id="df580-107">EXAMPLES</span></span>

### <span data-ttu-id="df580-108">範例 1：列出指定資料庫的所有顧問</span><span class="sxs-lookup"><span data-stu-id="df580-108">Example 1: List all the advisors for the specified database</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner"
DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : SchemaIssue
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 8/1/2016 3:01:41 PM
RecommendationsStatus          : SchemaIsConsistent
RecommendedActions             : {}
```

<span data-ttu-id="df580-109">此命令會列出名為 WIRunner 之資料庫的所有建議程式，該伺服器名稱為 wi-run-australia-east。</span><span class="sxs-lookup"><span data-stu-id="df580-109">This command gets lists all the advisors for the database named WIRunner that belongs to the server named wi-runner-australia-east.</span></span>

### <span data-ttu-id="df580-110">範例 2：取得指定資料庫的單一建議程式</span><span class="sxs-lookup"><span data-stu-id="df580-110">Example 2: Get a single advisor for the specified database</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex"
DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="df580-111">此命令會針對名為 WIRunner 的資料庫，獲得名為 CreateIndex 的顧問。</span><span class="sxs-lookup"><span data-stu-id="df580-111">This command gets the Advisor named CreateIndex for the database named WIRunner.</span></span>

### <span data-ttu-id="df580-112">範例 3：列出所有顧問及其回應中包含的建議動作</span><span class="sxs-lookup"><span data-stu-id="df580-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -ExpandRecommendedActions
DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.236046]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.239359]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.437714]_6C7AE8CC9C87E7FD5893...} 

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {IR_[test_schema]_[test_table_0.0288891]_38724E1DCF2178318957, 
                                 IR_[test_schema]_[test_table_0.140264]_38724E1DCF2178318957, 
                                 IR_[test_schema]_[test_table_0.412191]_38724E1DCF2178318957, 
                                 IR_[test_schema]_[test_table_0.442075]_38724E1DCF2178318957...} 

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : SchemaIssue
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 8/1/2016 3:04:26 PM
RecommendationsStatus          : SchemaIsConsistent
RecommendedActions             : {}
```

<span data-ttu-id="df580-113">此命令會獲得名為 "WIRunner" 之資料庫的所有建議程式，並提供回應中的建議動作。</span><span class="sxs-lookup"><span data-stu-id="df580-113">This command gets all the advisors for the database named 'WIRunner' with their recommended actions included in the response.</span></span>
<span data-ttu-id="df580-114">由於命令使用 *ExpandRecomactionActions* 參數，因此 Cmdlet 會隨著回應獲得建議的動作。</span><span class="sxs-lookup"><span data-stu-id="df580-114">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the recommended actions with the response.</span></span>

### <span data-ttu-id="df580-115">範例 4：取得單一建議程式，其建議動作包含在回應中</span><span class="sxs-lookup"><span data-stu-id="df580-115">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex" -ExpandRecommendedActions
DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.236046]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.239359]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.437714]_6C7AE8CC9C87E7FD5893...}
```

<span data-ttu-id="df580-116">此命令會從名為 WIRunner 的資料庫獲得名為 CreateIndex 的建議程式，其建議動作會包含在回應中。</span><span class="sxs-lookup"><span data-stu-id="df580-116">This command gets the Advisor named CreateIndex from the database named WIRunner with its recommended actions included in the response.</span></span>
<span data-ttu-id="df580-117">由於命令使用 *ExpandRecomactionActions* 參數，因此 Cmdlet 會隨著回應獲得建議的動作。</span><span class="sxs-lookup"><span data-stu-id="df580-117">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the recommended actions with the response.</span></span>

### <span data-ttu-id="df580-118">範例 5：使用篩選列出指定資料庫的所有建議程式</span><span class="sxs-lookup"><span data-stu-id="df580-118">Example 5: List all the advisors for the specified database using filtering</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName d*
DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}
```

<span data-ttu-id="df580-119">此命令會列出名為 WIRunner 之資料庫的所有建議程式，該伺服器名稱為 wi-run-australia-east，開頭為 "d"。</span><span class="sxs-lookup"><span data-stu-id="df580-119">This command gets lists all the advisors for the database named WIRunner that belongs to the server named wi-runner-australia-east and start with the letter "d".</span></span>

## <span data-ttu-id="df580-120">參數</span><span class="sxs-lookup"><span data-stu-id="df580-120">PARAMETERS</span></span>

### <span data-ttu-id="df580-121">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="df580-121">-AdvisorName</span></span>
<span data-ttu-id="df580-122">指定此 Cmdlet 所獲得之建議程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="df580-122">Specifies the name of the advisor that this cmdlet gets.</span></span>

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

### <span data-ttu-id="df580-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="df580-123">-DatabaseName</span></span>
<span data-ttu-id="df580-124">指定此 Cmdlet 要求顧問使用的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="df580-124">Specifies the name of the database for which this cmdlet requests the Advisor.</span></span>

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

### <span data-ttu-id="df580-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df580-125">-DefaultProfile</span></span>
<span data-ttu-id="df580-126">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="df580-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="df580-127">-ExpandRecomactionActions</span><span class="sxs-lookup"><span data-stu-id="df580-127">-ExpandRecommendedActions</span></span>
<span data-ttu-id="df580-128">表示此 Cmdlet 會以回應獲得建議的動作。</span><span class="sxs-lookup"><span data-stu-id="df580-128">Indicates that this cmdlet gets the recommended actions with the response.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df580-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df580-129">-ResourceGroupName</span></span>
<span data-ttu-id="df580-130">指定包含此資料庫之伺服器的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="df580-130">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="df580-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="df580-131">-ServerName</span></span>
<span data-ttu-id="df580-132">指定包含資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="df580-132">Specifies the name of the server that contains the database.</span></span>

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

### <span data-ttu-id="df580-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df580-133">CommonParameters</span></span>
<span data-ttu-id="df580-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="df580-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df580-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="df580-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df580-136">輸入</span><span class="sxs-lookup"><span data-stu-id="df580-136">INPUTS</span></span>

### <span data-ttu-id="df580-137">System.String</span><span class="sxs-lookup"><span data-stu-id="df580-137">System.String</span></span>

### <span data-ttu-id="df580-138">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="df580-138">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="df580-139">輸出</span><span class="sxs-lookup"><span data-stu-id="df580-139">OUTPUTS</span></span>

### <span data-ttu-id="df580-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="df580-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>

## <span data-ttu-id="df580-141">筆記</span><span class="sxs-lookup"><span data-stu-id="df580-141">NOTES</span></span>
* <span data-ttu-id="df580-142">關鍵字：azure、azurerm、arm、resource、management、manager、sql、database、mssql、advisor</span><span class="sxs-lookup"><span data-stu-id="df580-142">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor</span></span>

## <span data-ttu-id="df580-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="df580-143">RELATED LINKS</span></span>

[<span data-ttu-id="df580-144">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="df580-144">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="df580-145">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="df580-145">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="df580-146">Get-AzSqlDatabaseRecomactionAction</span><span class="sxs-lookup"><span data-stu-id="df580-146">Get-AzSqlDatabaseRecommendedAction</span></span>](./Get-AzSqlDatabaseRecommendedAction.md)

[<span data-ttu-id="df580-147">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="df580-147">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlDatabaseAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="df580-148">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="df580-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
