---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: DAEF11C1-281B-4BED-9283-2296E0B57018
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveradvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvisor.md
ms.openlocfilehash: 1d487c4397d1a7c29f0b415ee973d01e4dc6f1a1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98439036"
---
# <span data-ttu-id="4cdf9-101">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="4cdf9-101">Get-AzSqlServerAdvisor</span></span>

## <span data-ttu-id="4cdf9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4cdf9-102">SYNOPSIS</span></span>
<span data-ttu-id="4cdf9-103">取得一或多個 Azure SQL Server 顧問。</span><span class="sxs-lookup"><span data-stu-id="4cdf9-103">Gets one or more Advisors for an Azure SQL Server.</span></span>

## <span data-ttu-id="4cdf9-104">句法</span><span class="sxs-lookup"><span data-stu-id="4cdf9-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4cdf9-105">說明</span><span class="sxs-lookup"><span data-stu-id="4cdf9-105">DESCRIPTION</span></span>
<span data-ttu-id="4cdf9-106">**AzSqlServerAdvisor** Cmdlet 會針對 Azure sql server 取得一或多個 Azure Sql server 顧問。</span><span class="sxs-lookup"><span data-stu-id="4cdf9-106">The **Get-AzSqlServerAdvisor** cmdlet gets one or more Azure SQL Server Advisors for an Azure SQL Server.</span></span>

## <span data-ttu-id="4cdf9-107">示例</span><span class="sxs-lookup"><span data-stu-id="4cdf9-107">EXAMPLES</span></span>

### <span data-ttu-id="4cdf9-108">範例1：列出伺服器的所有顧問</span><span class="sxs-lookup"><span data-stu-id="4cdf9-108">Example 1: List all the advisors for the server</span></span>
```
PS C:\> Get-AzSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east"
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}

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

<span data-ttu-id="4cdf9-109">這個命令會取得名為 [wi-中]-東，且屬於名為 WIRunnersProd 之資源群組的所有伺服器顧問清單。</span><span class="sxs-lookup"><span data-stu-id="4cdf9-109">This command gets a list of all the advisors for the server named wi-runner-australia-east that belongs to the resource group named WIRunnersProd.</span></span>

### <span data-ttu-id="4cdf9-110">範例2：取得伺服器的單一顧問</span><span class="sxs-lookup"><span data-stu-id="4cdf9-110">Example 2: Get a single advisor for the server</span></span>
```
PS C:\> Get-AzSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex"
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

<span data-ttu-id="4cdf9-111">這個命令會針對名為 [wi-東] 的伺服器，取得名為 CreateIndex 的顧問。</span><span class="sxs-lookup"><span data-stu-id="4cdf9-111">This command gets the advisor named CreateIndex for the server named wi-runner-australia-east.</span></span>

### <span data-ttu-id="4cdf9-112">範例3：使用回應中包含的建議動作來列出所有顧問</span><span class="sxs-lookup"><span data-stu-id="4cdf9-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
```
PS C:\>Get-AzSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ExpandRecommendedActions
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

ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}
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

<span data-ttu-id="4cdf9-113">這個命令會取得伺服器中名為 [wi-東] 的所有顧問。</span><span class="sxs-lookup"><span data-stu-id="4cdf9-113">This command gets all the advisors for the server named wi-runner-australia-east.</span></span>
<span data-ttu-id="4cdf9-114">由於命令使用 *ExpandRecommendedActions* 參數，因此 Cmdlet 會取得回應中包含的建議動作。</span><span class="sxs-lookup"><span data-stu-id="4cdf9-114">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the advisors recommended actions included in the response.</span></span>

### <span data-ttu-id="4cdf9-115">範例4：透過回應中包含的建議動作來取得單一顧問</span><span class="sxs-lookup"><span data-stu-id="4cdf9-115">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
```
PS C:\> Get-AzSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -ExpandRecommendedActions
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

<span data-ttu-id="4cdf9-116">這個命令會透過名為 [wi-fi-東] 的伺服器取得名為 CreateIndex 的 advisor，且回應中包含其建議的動作。</span><span class="sxs-lookup"><span data-stu-id="4cdf9-116">This command gets advisor named CreateIndex from the server named wi-runner-australia-east with its recommended actions included in the response.</span></span>

### <span data-ttu-id="4cdf9-117">範例5：使用篩選來列出伺服器的所有顧問</span><span class="sxs-lookup"><span data-stu-id="4cdf9-117">Example 5: List all the advisors for the server using filtering</span></span>
```
PS C:\> Get-AzSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName d*
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

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

<span data-ttu-id="4cdf9-118">這個命令會取得名為 [wi-東南部-澳大利亞-東] 的所有顧問的清單，該伺服器屬於以字母 "d" 開頭的名稱為 WIRunnersProd 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="4cdf9-118">This command gets a list of all the advisors for the server named wi-runner-australia-east that belongs to the resource group named WIRunnersProd that start with the letter "d".</span></span>

## <span data-ttu-id="4cdf9-119">參數</span><span class="sxs-lookup"><span data-stu-id="4cdf9-119">PARAMETERS</span></span>

### <span data-ttu-id="4cdf9-120">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="4cdf9-120">-AdvisorName</span></span>
<span data-ttu-id="4cdf9-121">指定此 Cmdlet 取得的顧問名稱。</span><span class="sxs-lookup"><span data-stu-id="4cdf9-121">Specifies the name of the advisor that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4cdf9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cdf9-122">-DefaultProfile</span></span>
<span data-ttu-id="4cdf9-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="4cdf9-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4cdf9-124">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="4cdf9-124">-ExpandRecommendedActions</span></span>
<span data-ttu-id="4cdf9-125">表示 Cmdlet 包含回應中包含的顧問的建議動作。</span><span class="sxs-lookup"><span data-stu-id="4cdf9-125">Indicates that the cmdlet includes the recommended actions of the advisors that are included in the response.</span></span>

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

### <span data-ttu-id="4cdf9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cdf9-126">-ResourceGroupName</span></span>
<span data-ttu-id="4cdf9-127">指定伺服器資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4cdf9-127">Specifies name of the resource group of the server.</span></span>

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

### <span data-ttu-id="4cdf9-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4cdf9-128">-ServerName</span></span>
<span data-ttu-id="4cdf9-129">指定此 Cmdlet 要求的 advisor 伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="4cdf9-129">Specifies the name of the server for the advisor that this cmdlet requests.</span></span>

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

### <span data-ttu-id="4cdf9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cdf9-130">CommonParameters</span></span>
<span data-ttu-id="4cdf9-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4cdf9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cdf9-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4cdf9-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cdf9-133">輸入</span><span class="sxs-lookup"><span data-stu-id="4cdf9-133">INPUTS</span></span>

### <span data-ttu-id="4cdf9-134">System.object</span><span class="sxs-lookup"><span data-stu-id="4cdf9-134">System.String</span></span>

### <span data-ttu-id="4cdf9-135">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="4cdf9-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4cdf9-136">輸出</span><span class="sxs-lookup"><span data-stu-id="4cdf9-136">OUTPUTS</span></span>

### <span data-ttu-id="4cdf9-137">AzureSqlServerAdvisorModel 中的 [.Sql] 命令</span><span class="sxs-lookup"><span data-stu-id="4cdf9-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span></span>

## <span data-ttu-id="4cdf9-138">筆記</span><span class="sxs-lookup"><span data-stu-id="4cdf9-138">NOTES</span></span>
* <span data-ttu-id="4cdf9-139">關鍵字： azure，azurerm，arm，資源，管理，管理員，sql，server，mssql，advisor</span><span class="sxs-lookup"><span data-stu-id="4cdf9-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span></span>

## <span data-ttu-id="4cdf9-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="4cdf9-140">RELATED LINKS</span></span>

[<span data-ttu-id="4cdf9-141">AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="4cdf9-141">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="4cdf9-142">AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="4cdf9-142">Get-AzSqlDatabaseAdvisor</span></span>](./Get-AzSqlDatabaseAdvisor.md)

[<span data-ttu-id="4cdf9-143">AzSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="4cdf9-143">Get-AzSqlServerRecommendedAction</span></span>](./Get-AzSqlServerRecommendedAction.md)

[<span data-ttu-id="4cdf9-144">Set-AzSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="4cdf9-144">Set-AzSqlServerAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlServerAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="4cdf9-145">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="4cdf9-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

