---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BC8C0D59-662F-47D2-8619-9F69D78B171D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpooladvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolAdvisor.md
ms.openlocfilehash: 3032824d51e7892c21830decbdb1c92d03d7a2e1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142975"
---
# <span data-ttu-id="169eb-101">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="169eb-101">Get-AzSqlElasticPoolAdvisor</span></span>

## <span data-ttu-id="169eb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="169eb-102">SYNOPSIS</span></span>
<span data-ttu-id="169eb-103">取得 Azure SQL 彈性池的一個或多個顧問。</span><span class="sxs-lookup"><span data-stu-id="169eb-103">Gets one or more Advisors for an Azure SQL Elastic Pool.</span></span>

## <span data-ttu-id="169eb-104">句法</span><span class="sxs-lookup"><span data-stu-id="169eb-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 -ElasticPoolName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="169eb-105">說明</span><span class="sxs-lookup"><span data-stu-id="169eb-105">DESCRIPTION</span></span>
<span data-ttu-id="169eb-106">**AzSqlElasticPoolAdvisor** Cmdlet 可取得 Azure Sql 彈性池的一個或多個 Azure Sql 彈性池顧問。</span><span class="sxs-lookup"><span data-stu-id="169eb-106">The **Get-AzSqlElasticPoolAdvisor** cmdlet gets one or more Azure SQL Elastic Pool Advisors for an Azure SQL Elastic Pool.</span></span>

## <span data-ttu-id="169eb-107">示例</span><span class="sxs-lookup"><span data-stu-id="169eb-107">EXAMPLES</span></span>

### <span data-ttu-id="169eb-108">範例1：列出指定彈性池的所有顧問</span><span class="sxs-lookup"><span data-stu-id="169eb-108">Example 1: List all the advisors for the specified elastic pool</span></span>
```
PS C:\>Get-AzSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool"
ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}

ElasticPoolName                : WIRunnerPool
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

<span data-ttu-id="169eb-109">此命令會列出一個名為 WIRunnerPool 的彈性池的所有顧問。</span><span class="sxs-lookup"><span data-stu-id="169eb-109">The command gets lists all the advisors for the elastic pool named WIRunnerPool.</span></span>

### <span data-ttu-id="169eb-110">範例2：取得指定彈性池的單一顧問</span><span class="sxs-lookup"><span data-stu-id="169eb-110">Example 2: Get a single advisor for the specified elastic pool</span></span>
```
PS C:\>Get-AzSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex"
ElasticPoolName                : WIRunnerPool
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

<span data-ttu-id="169eb-111">這個命令會取得名為 WIRunnerPool 的彈性池名為 CreateIndex 的顧問。</span><span class="sxs-lookup"><span data-stu-id="169eb-111">This command gets the Advisor named CreateIndex for the elastic pool named WIRunnerPool.</span></span>

### <span data-ttu-id="169eb-112">範例3：使用回應中包含的建議動作來列出所有顧問</span><span class="sxs-lookup"><span data-stu-id="169eb-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
```
PS C:\>Get-AzSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -ExpandRecommendedActions
ElasticPoolName                : WIRunnerPool
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

ElasticPoolName                : WIRunnerPool
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

ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}

ElasticPoolName                : WIRunnerPool
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

<span data-ttu-id="169eb-113">這個命令會以回應中包含的建議動作來取得彈性池的所有顧問。</span><span class="sxs-lookup"><span data-stu-id="169eb-113">This command gets all the advisors for the elastic pool with their recommended actions included in the response.</span></span>

### <span data-ttu-id="169eb-114">範例4：透過回應中包含的建議動作來取得單一顧問</span><span class="sxs-lookup"><span data-stu-id="169eb-114">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
```
PS C:\>Get-AzSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -ExpandRecommendedActions
ElasticPoolName                : WIRunnerPool
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

<span data-ttu-id="169eb-115">這個命令會透過名為 [wi-fi-東] 的伺服器取得名為 CreateIndex 的 advisor，且回應中包含其建議的動作。</span><span class="sxs-lookup"><span data-stu-id="169eb-115">This command gets advisor named CreateIndex from the server named wi-runner-australia-east with its recommended actions included in the response.</span></span>

### <span data-ttu-id="169eb-116">範例5：使用篩選來列出指定彈性池的所有顧問</span><span class="sxs-lookup"><span data-stu-id="169eb-116">Example 5: List all the advisors for the specified elastic pool using filtering</span></span>
```
PS C:\>Get-AzSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName d*
ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

ElasticPoolName                : WIRunnerPool
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

<span data-ttu-id="169eb-117">此命令會列出一個名為 WIRunnerPool 的彈性池（以字母 "d" 開頭）的所有顧問。</span><span class="sxs-lookup"><span data-stu-id="169eb-117">The command gets lists all the advisors for the elastic pool named WIRunnerPool that start with the letter "d".</span></span>

## <span data-ttu-id="169eb-118">參數</span><span class="sxs-lookup"><span data-stu-id="169eb-118">PARAMETERS</span></span>

### <span data-ttu-id="169eb-119">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="169eb-119">-AdvisorName</span></span>
<span data-ttu-id="169eb-120">指定此 Cmdlet 取得的顧問名稱。</span><span class="sxs-lookup"><span data-stu-id="169eb-120">Specifies the name of the Advisor that this cmdlet gets.</span></span>

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

### <span data-ttu-id="169eb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="169eb-121">-DefaultProfile</span></span>
<span data-ttu-id="169eb-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="169eb-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="169eb-123">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="169eb-123">-ElasticPoolName</span></span>
<span data-ttu-id="169eb-124">指定此 Cmdlet 要求 Advisor 的彈性池的名稱。</span><span class="sxs-lookup"><span data-stu-id="169eb-124">Specifies the name of the elastic pool for which this cmdlet requests the Advisor.</span></span>

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

### <span data-ttu-id="169eb-125">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="169eb-125">-ExpandRecommendedActions</span></span>
<span data-ttu-id="169eb-126">表示 Cmdlet 在回應中包括 Advisor 的建議動作。</span><span class="sxs-lookup"><span data-stu-id="169eb-126">Indicates that the cmdlet includes the recommended actions of the Advisor in the response.</span></span>

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

### <span data-ttu-id="169eb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="169eb-127">-ResourceGroupName</span></span>
<span data-ttu-id="169eb-128">指定包含此彈性池之伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="169eb-128">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="169eb-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="169eb-129">-ServerName</span></span>
<span data-ttu-id="169eb-130">指定彈性池所在的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="169eb-130">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="169eb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="169eb-131">CommonParameters</span></span>
<span data-ttu-id="169eb-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="169eb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="169eb-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="169eb-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="169eb-134">輸入</span><span class="sxs-lookup"><span data-stu-id="169eb-134">INPUTS</span></span>

### <span data-ttu-id="169eb-135">System.object</span><span class="sxs-lookup"><span data-stu-id="169eb-135">System.String</span></span>

### <span data-ttu-id="169eb-136">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="169eb-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="169eb-137">輸出</span><span class="sxs-lookup"><span data-stu-id="169eb-137">OUTPUTS</span></span>

### <span data-ttu-id="169eb-138">AzureSqlElasticPoolAdvisorModel 中的 [.Sql] 命令</span><span class="sxs-lookup"><span data-stu-id="169eb-138">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span></span>

## <span data-ttu-id="169eb-139">筆記</span><span class="sxs-lookup"><span data-stu-id="169eb-139">NOTES</span></span>
* <span data-ttu-id="169eb-140">關鍵字： azure，azurerm，arm，資源，管理，管理員，sql，elasticpool，mssql，advisor</span><span class="sxs-lookup"><span data-stu-id="169eb-140">Keywords: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor</span></span>

## <span data-ttu-id="169eb-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="169eb-141">RELATED LINKS</span></span>

[<span data-ttu-id="169eb-142">AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="169eb-142">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="169eb-143">AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="169eb-143">Get-AzSqlDatabaseAdvisor</span></span>](./Get-AzSqlDatabaseAdvisor.md)

[<span data-ttu-id="169eb-144">AzSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="169eb-144">Get-AzSqlElasticPoolRecommendedAction</span></span>](./Get-AzSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="169eb-145">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="169eb-145">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="169eb-146">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="169eb-146">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
