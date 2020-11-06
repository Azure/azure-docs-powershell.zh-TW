---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 5AAB22C6-8E3C-4BDC-8A54-DA5A9906B762
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseadvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAdvisor.md
ms.openlocfilehash: 853702ab34a6a9dab7e90f2335f99deb7155a837
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451039"
---
# <span data-ttu-id="cbcad-101">Get-AzureRmSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="cbcad-101">Get-AzureRmSqlDatabaseAdvisor</span></span>

## <span data-ttu-id="cbcad-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cbcad-102">SYNOPSIS</span></span>
<span data-ttu-id="cbcad-103">取得一或多個 Azure SQL 資料庫的顧問。</span><span class="sxs-lookup"><span data-stu-id="cbcad-103">Gets one or more Advisors for an Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cbcad-104">句法</span><span class="sxs-lookup"><span data-stu-id="cbcad-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 -DatabaseName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cbcad-105">說明</span><span class="sxs-lookup"><span data-stu-id="cbcad-105">DESCRIPTION</span></span>
<span data-ttu-id="cbcad-106">**AzureRmSqlDatabaseAdvisor** Cmdlet 會針對 Azure sql 資料庫取得一個或多個 Azure Sql database 顧問。</span><span class="sxs-lookup"><span data-stu-id="cbcad-106">The **Get-AzureRmSqlDatabaseAdvisor** cmdlet gets one or more Azure SQL Database Advisors for an Azure SQL Database.</span></span>

## <span data-ttu-id="cbcad-107">示例</span><span class="sxs-lookup"><span data-stu-id="cbcad-107">EXAMPLES</span></span>

### <span data-ttu-id="cbcad-108">範例1：列出指定資料庫的所有顧問</span><span class="sxs-lookup"><span data-stu-id="cbcad-108">Example 1: List all the advisors for the specified database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner"
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

<span data-ttu-id="cbcad-109">這個命令會針對屬於名為 [wi-東] 的伺服器的名稱為 WIRunner 的所有顧問列出該資料庫。</span><span class="sxs-lookup"><span data-stu-id="cbcad-109">This command gets lists all the advisors for the database named WIRunner that belongs to the server named wi-runner-australia-east.</span></span>

### <span data-ttu-id="cbcad-110">範例2：為指定的資料庫取得單一顧問</span><span class="sxs-lookup"><span data-stu-id="cbcad-110">Example 2: Get a single advisor for the specified database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex"
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

<span data-ttu-id="cbcad-111">這個命令會取得名為 WIRunner 之資料庫的名為 CreateIndex 的顧問。</span><span class="sxs-lookup"><span data-stu-id="cbcad-111">This command gets the Advisor named CreateIndex for the database named WIRunner.</span></span>

### <span data-ttu-id="cbcad-112">範例3：使用回應中包含的建議動作來列出所有顧問</span><span class="sxs-lookup"><span data-stu-id="cbcad-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -ExpandRecommendedActions
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

<span data-ttu-id="cbcad-113">這個命令會以回應中包含的建議動作來取得名為「WIRunner」的資料庫所有顧問。</span><span class="sxs-lookup"><span data-stu-id="cbcad-113">This command gets all the advisors for the database named 'WIRunner' with their recommended actions included in the response.</span></span>
<span data-ttu-id="cbcad-114">由於命令使用 *ExpandRecommendedActions* 參數，因此 Cmdlet 會取得回應的建議動作。</span><span class="sxs-lookup"><span data-stu-id="cbcad-114">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the recommended actions with the response.</span></span>

### <span data-ttu-id="cbcad-115">範例4：透過回應中包含的建議動作來取得單一顧問</span><span class="sxs-lookup"><span data-stu-id="cbcad-115">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex" -ExpandRecommendedActions
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

<span data-ttu-id="cbcad-116">這個命令會從名為 WIRunner 的資料庫中取得名為 CreateIndex 的顧問，且回應中包含其建議的動作。</span><span class="sxs-lookup"><span data-stu-id="cbcad-116">This command gets the Advisor named CreateIndex from the database named WIRunner with its recommended actions included in the response.</span></span>
<span data-ttu-id="cbcad-117">由於命令使用 *ExpandRecommendedActions* 參數，因此 Cmdlet 會取得回應的建議動作。</span><span class="sxs-lookup"><span data-stu-id="cbcad-117">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the recommended actions with the response.</span></span>

## <span data-ttu-id="cbcad-118">參數</span><span class="sxs-lookup"><span data-stu-id="cbcad-118">PARAMETERS</span></span>

### <span data-ttu-id="cbcad-119">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="cbcad-119">-AdvisorName</span></span>
<span data-ttu-id="cbcad-120">指定此 Cmdlet 取得的顧問名稱。</span><span class="sxs-lookup"><span data-stu-id="cbcad-120">Specifies the name of the advisor that this cmdlet gets.</span></span>

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

### <span data-ttu-id="cbcad-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cbcad-121">-DatabaseName</span></span>
<span data-ttu-id="cbcad-122">指定此 Cmdlet 要求 Advisor 之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="cbcad-122">Specifies the name of the database for which this cmdlet requests the Advisor.</span></span>

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

### <span data-ttu-id="cbcad-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbcad-123">-DefaultProfile</span></span>
<span data-ttu-id="cbcad-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="cbcad-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cbcad-125">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="cbcad-125">-ExpandRecommendedActions</span></span>
<span data-ttu-id="cbcad-126">表示此 Cmdlet 會取得回應的建議動作。</span><span class="sxs-lookup"><span data-stu-id="cbcad-126">Indicates that this cmdlet gets the recommended actions with the response.</span></span>

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

### <span data-ttu-id="cbcad-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbcad-127">-ResourceGroupName</span></span>
<span data-ttu-id="cbcad-128">指定包含此資料庫之伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cbcad-128">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="cbcad-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cbcad-129">-ServerName</span></span>
<span data-ttu-id="cbcad-130">指定包含資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="cbcad-130">Specifies the name of the server that contains the database.</span></span>

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

### <span data-ttu-id="cbcad-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbcad-131">CommonParameters</span></span>
<span data-ttu-id="cbcad-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cbcad-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbcad-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cbcad-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbcad-134">輸入</span><span class="sxs-lookup"><span data-stu-id="cbcad-134">INPUTS</span></span>

### <span data-ttu-id="cbcad-135">System.object</span><span class="sxs-lookup"><span data-stu-id="cbcad-135">System.String</span></span>

### <span data-ttu-id="cbcad-136">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="cbcad-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="cbcad-137">輸出</span><span class="sxs-lookup"><span data-stu-id="cbcad-137">OUTPUTS</span></span>

### <span data-ttu-id="cbcad-138">AzureSqlDatabaseAdvisorModel 中的 [.Sql] 命令</span><span class="sxs-lookup"><span data-stu-id="cbcad-138">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>

## <span data-ttu-id="cbcad-139">筆記</span><span class="sxs-lookup"><span data-stu-id="cbcad-139">NOTES</span></span>
* <span data-ttu-id="cbcad-140">關鍵字： azure，azurerm，arm，資源，管理，管理員，sql，資料庫，mssql，advisor</span><span class="sxs-lookup"><span data-stu-id="cbcad-140">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor</span></span>

## <span data-ttu-id="cbcad-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="cbcad-141">RELATED LINKS</span></span>

[<span data-ttu-id="cbcad-142">AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="cbcad-142">Get-AzureRmSqlServerAdvisor</span></span>](./Get-AzureRmSqlServerAdvisor.md)

[<span data-ttu-id="cbcad-143">AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="cbcad-143">Get-AzureRmSqlElasticPoolAdvisor</span></span>](./Get-AzureRmSqlElasticPoolAdvisor.md)

[<span data-ttu-id="cbcad-144">AzureRmSqlDatabaseRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="cbcad-144">Get-AzureRmSqlDatabaseRecommendedAction</span></span>](./Get-AzureRmSqlDatabaseRecommendedAction.md)

[<span data-ttu-id="cbcad-145">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="cbcad-145">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span></span>](./Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="cbcad-146">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="cbcad-146">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
