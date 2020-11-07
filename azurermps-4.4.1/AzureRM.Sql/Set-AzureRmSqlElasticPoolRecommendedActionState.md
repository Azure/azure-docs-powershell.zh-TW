---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: EFDFCE12-F39C-4F52-9962-4601F0C4FD47
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPoolRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPoolRecommendedActionState.md
ms.openlocfilehash: 1bc5d89a381027bd72697d873308eb85807a6e63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625048"
---
# <span data-ttu-id="71b2b-101">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="71b2b-101">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>

## <span data-ttu-id="71b2b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="71b2b-102">SYNOPSIS</span></span>
<span data-ttu-id="71b2b-103">更新 Azure SQL 彈性池建議動作的狀態。</span><span class="sxs-lookup"><span data-stu-id="71b2b-103">Updates the state of an Azure SQL Elastic Pool recommended action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71b2b-104">句法</span><span class="sxs-lookup"><span data-stu-id="71b2b-104">SYNTAX</span></span>

```
Set-AzureRmSqlElasticPoolRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -ElasticPoolName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71b2b-105">說明</span><span class="sxs-lookup"><span data-stu-id="71b2b-105">DESCRIPTION</span></span>
<span data-ttu-id="71b2b-106">**AzureRmSqlElasticPoolRecommendedActionState** Cmdlet 會更新 Azure SQL 彈性池建議動作的狀態。</span><span class="sxs-lookup"><span data-stu-id="71b2b-106">The **Set-AzureRmSqlElasticPoolRecommendedActionState** cmdlet updates state of an Azure SQL Elastic Pool recommended action.</span></span>
<span data-ttu-id="71b2b-107">這個 Cmdlet 會根據新的狀態，套用建議的動作、還原或放棄。</span><span class="sxs-lookup"><span data-stu-id="71b2b-107">This cmdlet applies an recommended action, reverted, or discarded based on the new state.</span></span>

## <span data-ttu-id="71b2b-108">示例</span><span class="sxs-lookup"><span data-stu-id="71b2b-108">EXAMPLES</span></span>

### <span data-ttu-id="71b2b-109">範例1：將建議動作的狀態更新為擱置</span><span class="sxs-lookup"><span data-stu-id="71b2b-109">Example 1: Update the state of a recommended action to Pending</span></span>
```
PS C:\>Set-AzureRmSqlElasticPoolRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
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

<span data-ttu-id="71b2b-110">這個命令會將彈性池建議動作的狀態（IR_ test_schema _）更新為 [ \[ \] 擱置] \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893]。</span><span class="sxs-lookup"><span data-stu-id="71b2b-110">This command updates the state of elastic pool recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 to Pending.</span></span>

## <span data-ttu-id="71b2b-111">參數</span><span class="sxs-lookup"><span data-stu-id="71b2b-111">PARAMETERS</span></span>

### <span data-ttu-id="71b2b-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="71b2b-112">-AdvisorName</span></span>
<span data-ttu-id="71b2b-113">指定此建議動作所屬之 advisor 的名稱。</span><span class="sxs-lookup"><span data-stu-id="71b2b-113">Specifies the name of the advisor for which this recommended action belongs to.</span></span>

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

### <span data-ttu-id="71b2b-114">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="71b2b-114">-ElasticPoolName</span></span>
<span data-ttu-id="71b2b-115">指定彈性池的名稱。</span><span class="sxs-lookup"><span data-stu-id="71b2b-115">Specifies name of the elastic pool.</span></span>

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

### <span data-ttu-id="71b2b-116">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="71b2b-116">-RecommendedActionName</span></span>
<span data-ttu-id="71b2b-117">指定此 Cmdlet 更新狀態的建議動作名稱。</span><span class="sxs-lookup"><span data-stu-id="71b2b-117">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

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

### <span data-ttu-id="71b2b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71b2b-118">-ResourceGroupName</span></span>
<span data-ttu-id="71b2b-119">指定包含此彈性池之伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="71b2b-119">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="71b2b-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="71b2b-120">-ServerName</span></span>
<span data-ttu-id="71b2b-121">指定彈性池所在的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="71b2b-121">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="71b2b-122">-State</span><span class="sxs-lookup"><span data-stu-id="71b2b-122">-State</span></span>
<span data-ttu-id="71b2b-123">指定此 Cmdlet 更新建議動作狀態的值。</span><span class="sxs-lookup"><span data-stu-id="71b2b-123">Specifies the value to which this cmdlet updates the recommended action state.</span></span>

<span data-ttu-id="71b2b-124">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="71b2b-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="71b2b-125">有效</span><span class="sxs-lookup"><span data-stu-id="71b2b-125">Active</span></span>
- <span data-ttu-id="71b2b-126">擱置</span><span class="sxs-lookup"><span data-stu-id="71b2b-126">Pending</span></span>
- <span data-ttu-id="71b2b-127">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="71b2b-127">PendingRevert</span></span>
- <span data-ttu-id="71b2b-128">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="71b2b-128">RevertCancelled</span></span>
- <span data-ttu-id="71b2b-129">忽視</span><span class="sxs-lookup"><span data-stu-id="71b2b-129">Ignored</span></span>
- <span data-ttu-id="71b2b-130">已</span><span class="sxs-lookup"><span data-stu-id="71b2b-130">Resolved</span></span>

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

### <span data-ttu-id="71b2b-131">-確認</span><span class="sxs-lookup"><span data-stu-id="71b2b-131">-Confirm</span></span>
<span data-ttu-id="71b2b-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="71b2b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71b2b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71b2b-133">-WhatIf</span></span>
<span data-ttu-id="71b2b-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="71b2b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71b2b-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="71b2b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71b2b-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71b2b-136">-DefaultProfile</span></span>
<span data-ttu-id="71b2b-137">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="71b2b-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71b2b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71b2b-138">CommonParameters</span></span>
<span data-ttu-id="71b2b-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="71b2b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71b2b-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="71b2b-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71b2b-141">輸入</span><span class="sxs-lookup"><span data-stu-id="71b2b-141">INPUTS</span></span>

## <span data-ttu-id="71b2b-142">輸出</span><span class="sxs-lookup"><span data-stu-id="71b2b-142">OUTPUTS</span></span>

## <span data-ttu-id="71b2b-143">筆記</span><span class="sxs-lookup"><span data-stu-id="71b2b-143">NOTES</span></span>
* <span data-ttu-id="71b2b-144">關鍵字： azure、azurerm、arm、資源、管理、manager、sql、elasticpool、mssql、advisor、recommendedaction</span><span class="sxs-lookup"><span data-stu-id="71b2b-144">Keywords: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="71b2b-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="71b2b-145">RELATED LINKS</span></span>

[<span data-ttu-id="71b2b-146">AzureRmSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="71b2b-146">Get-AzureRmSqlElasticPoolRecommendedAction</span></span>](./Get-AzureRmSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="71b2b-147">Set-AzureRmSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="71b2b-147">Set-AzureRmSqlDatabaseRecommendedActionState</span></span>](./Set-AzureRmSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="71b2b-148">Set-AzureRmSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="71b2b-148">Set-AzureRmSqlServerRecommendedActionState</span></span>](./Set-AzureRmSqlServerRecommendedActionState.md)

[<span data-ttu-id="71b2b-149">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="71b2b-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
