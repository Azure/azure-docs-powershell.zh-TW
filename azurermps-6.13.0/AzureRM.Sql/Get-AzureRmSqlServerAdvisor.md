---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: DAEF11C1-281B-4BED-9283-2296E0B57018
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserveradvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAdvisor.md
ms.openlocfilehash: a77119e653f3d4e6155fbe98e85a583eca50c33f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625238"
---
# <span data-ttu-id="67603-101">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="67603-101">Get-AzureRmSqlServerAdvisor</span></span>

## <span data-ttu-id="67603-102">摘要</span><span class="sxs-lookup"><span data-stu-id="67603-102">SYNOPSIS</span></span>
<span data-ttu-id="67603-103">取得一或多個 Azure SQL Server 顧問。</span><span class="sxs-lookup"><span data-stu-id="67603-103">Gets one or more Advisors for an Azure SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67603-104">句法</span><span class="sxs-lookup"><span data-stu-id="67603-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67603-105">說明</span><span class="sxs-lookup"><span data-stu-id="67603-105">DESCRIPTION</span></span>
<span data-ttu-id="67603-106">**AzureRmSqlServerAdvisor** Cmdlet 會針對 Azure sql server 取得一或多個 Azure Sql server 顧問。</span><span class="sxs-lookup"><span data-stu-id="67603-106">The **Get-AzureRmSqlServerAdvisor** cmdlet gets one or more Azure SQL Server Advisors for an Azure SQL Server.</span></span>

## <span data-ttu-id="67603-107">示例</span><span class="sxs-lookup"><span data-stu-id="67603-107">EXAMPLES</span></span>

### <span data-ttu-id="67603-108">範例1：列出伺服器的所有顧問</span><span class="sxs-lookup"><span data-stu-id="67603-108">Example 1: List all the advisors for the server</span></span>
```
PS C:\> Get-AzureRmSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east"
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

<span data-ttu-id="67603-109">這個命令會取得名為 [wi-中]-東，且屬於名為 WIRunnersProd 之資源群組的所有伺服器顧問清單。</span><span class="sxs-lookup"><span data-stu-id="67603-109">This command gets a list of all the advisors for the server named wi-runner-australia-east that belongs to the resource group named WIRunnersProd.</span></span>

### <span data-ttu-id="67603-110">範例2：取得伺服器的單一顧問</span><span class="sxs-lookup"><span data-stu-id="67603-110">Example 2: Get a single advisor for the server</span></span>
```
PS C:\> Get-AzureRmSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex"
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

<span data-ttu-id="67603-111">這個命令會針對名為 [wi-東] 的伺服器，取得名為 CreateIndex 的顧問。</span><span class="sxs-lookup"><span data-stu-id="67603-111">This command gets the advisor named CreateIndex for the server named wi-runner-australia-east.</span></span>

### <span data-ttu-id="67603-112">範例3：使用回應中包含的建議動作來列出所有顧問</span><span class="sxs-lookup"><span data-stu-id="67603-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
```
PS C:\>Get-AzureRmSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ExpandRecommendedActions
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

<span data-ttu-id="67603-113">這個命令會取得伺服器中名為 [wi-東] 的所有顧問。</span><span class="sxs-lookup"><span data-stu-id="67603-113">This command gets all the advisors for the server named wi-runner-australia-east.</span></span>
<span data-ttu-id="67603-114">由於命令使用 *ExpandRecommendedActions* 參數，因此 Cmdlet 會取得回應中包含的建議動作。</span><span class="sxs-lookup"><span data-stu-id="67603-114">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the advisors recommended actions included in the response.</span></span>

### <span data-ttu-id="67603-115">範例4：透過回應中包含的建議動作來取得單一顧問</span><span class="sxs-lookup"><span data-stu-id="67603-115">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
```
PS C:\> Get-AzureRmSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -ExpandRecommendedActions
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

<span data-ttu-id="67603-116">這個命令會透過名為 [wi-fi-東] 的伺服器取得名為 CreateIndex 的 advisor，且回應中包含其建議的動作。</span><span class="sxs-lookup"><span data-stu-id="67603-116">This command gets advisor named CreateIndex from the server named wi-runner-australia-east with its recommended actions included in the response.</span></span>

## <span data-ttu-id="67603-117">參數</span><span class="sxs-lookup"><span data-stu-id="67603-117">PARAMETERS</span></span>

### <span data-ttu-id="67603-118">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="67603-118">-AdvisorName</span></span>
<span data-ttu-id="67603-119">指定此 Cmdlet 取得的顧問名稱。</span><span class="sxs-lookup"><span data-stu-id="67603-119">Specifies the name of the advisor that this cmdlet gets.</span></span>

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

### <span data-ttu-id="67603-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67603-120">-DefaultProfile</span></span>
<span data-ttu-id="67603-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="67603-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67603-122">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="67603-122">-ExpandRecommendedActions</span></span>
<span data-ttu-id="67603-123">表示 Cmdlet 包含回應中包含的顧問的建議動作。</span><span class="sxs-lookup"><span data-stu-id="67603-123">Indicates that the cmdlet includes the recommended actions of the advisors that are included in the response.</span></span>

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

### <span data-ttu-id="67603-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67603-124">-ResourceGroupName</span></span>
<span data-ttu-id="67603-125">指定伺服器資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="67603-125">Specifies name of the resource group of the server.</span></span>

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

### <span data-ttu-id="67603-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="67603-126">-ServerName</span></span>
<span data-ttu-id="67603-127">指定此 Cmdlet 要求的 advisor 伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="67603-127">Specifies the name of the server for the advisor that this cmdlet requests.</span></span>

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

### <span data-ttu-id="67603-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67603-128">CommonParameters</span></span>
<span data-ttu-id="67603-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="67603-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67603-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="67603-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67603-131">輸入</span><span class="sxs-lookup"><span data-stu-id="67603-131">INPUTS</span></span>

### <span data-ttu-id="67603-132">System.object</span><span class="sxs-lookup"><span data-stu-id="67603-132">System.String</span></span>

### <span data-ttu-id="67603-133">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="67603-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="67603-134">輸出</span><span class="sxs-lookup"><span data-stu-id="67603-134">OUTPUTS</span></span>

### <span data-ttu-id="67603-135">AzureSqlServerAdvisorModel 中的 [.Sql] 命令</span><span class="sxs-lookup"><span data-stu-id="67603-135">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span></span>

## <span data-ttu-id="67603-136">筆記</span><span class="sxs-lookup"><span data-stu-id="67603-136">NOTES</span></span>
* <span data-ttu-id="67603-137">關鍵字： azure，azurerm，arm，資源，管理，管理員，sql，server，mssql，advisor</span><span class="sxs-lookup"><span data-stu-id="67603-137">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span></span>

## <span data-ttu-id="67603-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="67603-138">RELATED LINKS</span></span>

[<span data-ttu-id="67603-139">AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="67603-139">Get-AzureRmSqlElasticPoolAdvisor</span></span>](./Get-AzureRmSqlElasticPoolAdvisor.md)

[<span data-ttu-id="67603-140">AzureRmSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="67603-140">Get-AzureRmSqlDatabaseAdvisor</span></span>](./Get-AzureRmSqlDatabaseAdvisor.md)

[<span data-ttu-id="67603-141">AzureRmSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="67603-141">Get-AzureRmSqlServerRecommendedAction</span></span>](./Get-AzureRmSqlServerRecommendedAction.md)

[<span data-ttu-id="67603-142">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="67603-142">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span></span>](./Set-AzureRmSqlServerAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="67603-143">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="67603-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

