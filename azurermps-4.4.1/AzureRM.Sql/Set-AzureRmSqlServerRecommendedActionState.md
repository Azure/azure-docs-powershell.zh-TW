---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 26EC220C-5123-4CEF-8CC6-5FFD08F33481
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerRecommendedActionState.md
ms.openlocfilehash: 4b000ef101b07bf882accb10b0256e0dbea513b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626479"
---
# <span data-ttu-id="ed526-101">Set-AzureRmSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="ed526-101">Set-AzureRmSqlServerRecommendedActionState</span></span>

## <span data-ttu-id="ed526-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ed526-102">SYNOPSIS</span></span>
<span data-ttu-id="ed526-103">更新 Azure SQL Server 建議動作的狀態。</span><span class="sxs-lookup"><span data-stu-id="ed526-103">Updates the state of an Azure SQL Server recommended action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed526-104">句法</span><span class="sxs-lookup"><span data-stu-id="ed526-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed526-105">說明</span><span class="sxs-lookup"><span data-stu-id="ed526-105">DESCRIPTION</span></span>
<span data-ttu-id="ed526-106">**AzureRmSqlServerRecommendedActionState** Cmdlet 會更新 Azure SQL Server 建議動作的狀態。</span><span class="sxs-lookup"><span data-stu-id="ed526-106">The **Set-AzureRmSqlServerRecommendedActionState** cmdlet updates state of an Azure SQL Server recommended action.</span></span>
<span data-ttu-id="ed526-107">這個 Cmdlet 會根據新的狀態來套用、還原或放棄建議的動作。</span><span class="sxs-lookup"><span data-stu-id="ed526-107">This cmdlet applies, reverts, or discards the recommended action based on the new state.</span></span>

## <span data-ttu-id="ed526-108">示例</span><span class="sxs-lookup"><span data-stu-id="ed526-108">EXAMPLES</span></span>

### <span data-ttu-id="ed526-109">Example1：將指定建議動作的狀態更新為 [擱置中]</span><span class="sxs-lookup"><span data-stu-id="ed526-109">Example1: Update the state of the specified recommended action to Pending</span></span>
```
PS C:\>Set-AzureRmSqlServerRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
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

<span data-ttu-id="ed526-110">更新名為 "IR_ \[ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893" 設為 "擱置" 的伺服器建議動作狀態</span><span class="sxs-lookup"><span data-stu-id="ed526-110">Updates state of server recommended action named "IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893" to "Pending"</span></span>

## <span data-ttu-id="ed526-111">參數</span><span class="sxs-lookup"><span data-stu-id="ed526-111">PARAMETERS</span></span>

### <span data-ttu-id="ed526-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="ed526-112">-AdvisorName</span></span>
<span data-ttu-id="ed526-113">指定包含建議動作的顧問名稱。</span><span class="sxs-lookup"><span data-stu-id="ed526-113">Specifies the name of the advisor that contains the recommended action.</span></span>

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

### <span data-ttu-id="ed526-114">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="ed526-114">-RecommendedActionName</span></span>
<span data-ttu-id="ed526-115">指定此 Cmdlet 更新狀態的建議動作名稱。</span><span class="sxs-lookup"><span data-stu-id="ed526-115">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

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

### <span data-ttu-id="ed526-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed526-116">-ResourceGroupName</span></span>
<span data-ttu-id="ed526-117">指定伺服器資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed526-117">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="ed526-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ed526-118">-ServerName</span></span>
<span data-ttu-id="ed526-119">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed526-119">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="ed526-120">-State</span><span class="sxs-lookup"><span data-stu-id="ed526-120">-State</span></span>
<span data-ttu-id="ed526-121">指定此 Cmdlet 更新建議動作狀態的新值。</span><span class="sxs-lookup"><span data-stu-id="ed526-121">Specifies the new value to which this cmdlet updates the recommended action state.</span></span>

<span data-ttu-id="ed526-122">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ed526-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ed526-123">有效</span><span class="sxs-lookup"><span data-stu-id="ed526-123">Active</span></span>
- <span data-ttu-id="ed526-124">擱置</span><span class="sxs-lookup"><span data-stu-id="ed526-124">Pending</span></span>
- <span data-ttu-id="ed526-125">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="ed526-125">PendingRevert</span></span>
- <span data-ttu-id="ed526-126">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="ed526-126">RevertCancelled</span></span>
- <span data-ttu-id="ed526-127">忽視</span><span class="sxs-lookup"><span data-stu-id="ed526-127">Ignored</span></span>
- <span data-ttu-id="ed526-128">已</span><span class="sxs-lookup"><span data-stu-id="ed526-128">Resolved</span></span>

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

### <span data-ttu-id="ed526-129">-確認</span><span class="sxs-lookup"><span data-stu-id="ed526-129">-Confirm</span></span>
<span data-ttu-id="ed526-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ed526-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed526-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed526-131">-WhatIf</span></span>
<span data-ttu-id="ed526-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ed526-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed526-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ed526-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed526-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed526-134">-DefaultProfile</span></span>
<span data-ttu-id="ed526-135">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ed526-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed526-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed526-136">CommonParameters</span></span>
<span data-ttu-id="ed526-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ed526-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed526-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ed526-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed526-139">輸入</span><span class="sxs-lookup"><span data-stu-id="ed526-139">INPUTS</span></span>

## <span data-ttu-id="ed526-140">輸出</span><span class="sxs-lookup"><span data-stu-id="ed526-140">OUTPUTS</span></span>

### <span data-ttu-id="ed526-141">AzureSqlServerRecommendedActionModel 中的 [RecommendedAction]</span><span class="sxs-lookup"><span data-stu-id="ed526-141">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlServerRecommendedActionModel</span></span>

## <span data-ttu-id="ed526-142">筆記</span><span class="sxs-lookup"><span data-stu-id="ed526-142">NOTES</span></span>
* <span data-ttu-id="ed526-143">關鍵字： azure，azurerm，arm，資源，管理，管理員，sql，server，mssql，advisor，recommendedaction</span><span class="sxs-lookup"><span data-stu-id="ed526-143">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="ed526-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="ed526-144">RELATED LINKS</span></span>

[<span data-ttu-id="ed526-145">AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="ed526-145">Get-AzureRmSqlServerAdvisor</span></span>](./Get-AzureRmSqlServerAdvisor.md)

[<span data-ttu-id="ed526-146">AzureRmSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="ed526-146">Get-AzureRmSqlServerRecommendedAction</span></span>](./Get-AzureRmSqlServerRecommendedAction.md)

[<span data-ttu-id="ed526-147">Set-AzureRmSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="ed526-147">Set-AzureRmSqlDatabaseRecommendedActionState</span></span>](./Set-AzureRmSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="ed526-148">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="ed526-148">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>](./Set-AzureRmSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="ed526-149">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="ed526-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
