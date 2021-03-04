---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 50E09DF7-F5B5-4668-9520-73D562E91800
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqldatabaseadvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 214fe4c32ed49433aa57752508604d0179334401
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913057"
---
# <span data-ttu-id="1315b-101">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="1315b-101">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="1315b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1315b-102">SYNOPSIS</span></span>
<span data-ttu-id="1315b-103">修改 Azure SQL 資料庫建議程式自動執行狀態。</span><span class="sxs-lookup"><span data-stu-id="1315b-103">Modifies auto execute status of an Azure SQL Database Advisor.</span></span>

## <span data-ttu-id="1315b-104">語法</span><span class="sxs-lookup"><span data-stu-id="1315b-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseAdvisorAutoExecuteStatus -AdvisorName <String> -AutoExecuteStatus <AdvisorAutoExecuteStatus>
 -ServerName <String> -DatabaseName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1315b-105">描述</span><span class="sxs-lookup"><span data-stu-id="1315b-105">DESCRIPTION</span></span>
<span data-ttu-id="1315b-106">**Set-AzSqlDatabaseAdvisorAutoExecuteStatus Cmdlet** 會修改 Azure SQL Database Advisor 的自動執行屬性。</span><span class="sxs-lookup"><span data-stu-id="1315b-106">The **Set-AzSqlDatabaseAdvisorAutoExecuteStatus** cmdlet modifies the auto execute property for an Azure SQL Database Advisor.</span></span>
<span data-ttu-id="1315b-107">目前，此 Cmdlet 支援啟用、停用和預設值的值。</span><span class="sxs-lookup"><span data-stu-id="1315b-107">Currently, this cmdlet supports the values Enabled, Disabled, and Default.</span></span>

## <span data-ttu-id="1315b-108">例子</span><span class="sxs-lookup"><span data-stu-id="1315b-108">EXAMPLES</span></span>

### <span data-ttu-id="1315b-109">範例 1：為顧問啟用自動執行</span><span class="sxs-lookup"><span data-stu-id="1315b-109">Example 1: Enable auto execute for an advisor</span></span>
```
PS C:\>Set-AzSqlDatabaseAdvisorAutoExecuteStatus -ResourceGroupName "ContosoRunnersProd" -ServerName "runner-australia-east" -DatabaseName "ContosoRunner" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
DatabaseName                   : ContosoRunner
ResourceGroupName              : ContosoRunnersProd
ServerName                     : runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Enabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="1315b-110">此命令會變更名為 CreateIndex 的顧問的自動執行狀態為啟用。</span><span class="sxs-lookup"><span data-stu-id="1315b-110">This command changes the auto execute status of an advisor named CreateIndex to Enabled.</span></span>

## <span data-ttu-id="1315b-111">參數</span><span class="sxs-lookup"><span data-stu-id="1315b-111">PARAMETERS</span></span>

### <span data-ttu-id="1315b-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="1315b-112">-AdvisorName</span></span>
<span data-ttu-id="1315b-113">指定此 Cmdlet 修改其狀態的顧問名稱。</span><span class="sxs-lookup"><span data-stu-id="1315b-113">Specifies the name of the advisor for which this cmdlet modifies the status.</span></span>

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

### <span data-ttu-id="1315b-114">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="1315b-114">-AutoExecuteStatus</span></span>
<span data-ttu-id="1315b-115">指定狀態的值。</span><span class="sxs-lookup"><span data-stu-id="1315b-115">Specifies the value for the status.</span></span>
<span data-ttu-id="1315b-116">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="1315b-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1315b-117">啟用</span><span class="sxs-lookup"><span data-stu-id="1315b-117">Enabled</span></span> 
- <span data-ttu-id="1315b-118">禁用</span><span class="sxs-lookup"><span data-stu-id="1315b-118">Disabled</span></span> 
- <span data-ttu-id="1315b-119">預設</span><span class="sxs-lookup"><span data-stu-id="1315b-119">Default</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled, Default

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1315b-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1315b-120">-DatabaseName</span></span>
<span data-ttu-id="1315b-121">指定此 Cmdlet 修改狀態的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="1315b-121">Specifies the name of the database for which this cmdlet modifies status.</span></span>

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

### <span data-ttu-id="1315b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1315b-122">-DefaultProfile</span></span>
<span data-ttu-id="1315b-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="1315b-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1315b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1315b-124">-ResourceGroupName</span></span>
<span data-ttu-id="1315b-125">指定包含此資料庫之伺服器的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="1315b-125">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="1315b-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1315b-126">-ServerName</span></span>
<span data-ttu-id="1315b-127">指定資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="1315b-127">Specifies the name of the server for the database.</span></span>

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

### <span data-ttu-id="1315b-128">-確認</span><span class="sxs-lookup"><span data-stu-id="1315b-128">-Confirm</span></span>
<span data-ttu-id="1315b-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1315b-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1315b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1315b-130">-WhatIf</span></span>
<span data-ttu-id="1315b-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1315b-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1315b-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1315b-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1315b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1315b-133">CommonParameters</span></span>
<span data-ttu-id="1315b-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1315b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1315b-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1315b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1315b-136">輸入</span><span class="sxs-lookup"><span data-stu-id="1315b-136">INPUTS</span></span>

### <span data-ttu-id="1315b-137">System.String</span><span class="sxs-lookup"><span data-stu-id="1315b-137">System.String</span></span>

### <span data-ttu-id="1315b-138">Microsoft.Azure.Commands.sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="1315b-138">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="1315b-139">輸出</span><span class="sxs-lookup"><span data-stu-id="1315b-139">OUTPUTS</span></span>

### <span data-ttu-id="1315b-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="1315b-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>

## <span data-ttu-id="1315b-141">筆記</span><span class="sxs-lookup"><span data-stu-id="1315b-141">NOTES</span></span>

## <span data-ttu-id="1315b-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="1315b-142">RELATED LINKS</span></span>

[<span data-ttu-id="1315b-143">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="1315b-143">Get-AzSqlDatabaseAdvisor</span></span>](./Get-AzSqlDatabaseAdvisor.md)

[<span data-ttu-id="1315b-144">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="1315b-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

