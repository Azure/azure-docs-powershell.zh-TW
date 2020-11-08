---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 50E09DF7-F5B5-4668-9520-73D562E91800
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaseadvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 1d6348c5ede63dee1f76059277c8f7d142a2c327
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127243"
---
# <span data-ttu-id="1f188-101">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="1f188-101">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="1f188-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1f188-102">SYNOPSIS</span></span>
<span data-ttu-id="1f188-103">修改 Azure SQL Database Advisor 的自動執行狀態。</span><span class="sxs-lookup"><span data-stu-id="1f188-103">Modifies auto execute status of an Azure SQL Database Advisor.</span></span>

## <span data-ttu-id="1f188-104">句法</span><span class="sxs-lookup"><span data-stu-id="1f188-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseAdvisorAutoExecuteStatus -AdvisorName <String> -AutoExecuteStatus <AdvisorAutoExecuteStatus>
 -ServerName <String> -DatabaseName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f188-105">說明</span><span class="sxs-lookup"><span data-stu-id="1f188-105">DESCRIPTION</span></span>
<span data-ttu-id="1f188-106">**AzSqlDatabaseAdvisorAutoExecuteStatus** Cmdlet 會修改 Azure SQL Database Advisor 的自動執行屬性。</span><span class="sxs-lookup"><span data-stu-id="1f188-106">The **Set-AzSqlDatabaseAdvisorAutoExecuteStatus** cmdlet modifies the auto execute property for an Azure SQL Database Advisor.</span></span>
<span data-ttu-id="1f188-107">這個 Cmdlet 目前支援啟用、停用和預設值。</span><span class="sxs-lookup"><span data-stu-id="1f188-107">Currently, this cmdlet supports the values Enabled, Disabled, and Default.</span></span>

## <span data-ttu-id="1f188-108">示例</span><span class="sxs-lookup"><span data-stu-id="1f188-108">EXAMPLES</span></span>

### <span data-ttu-id="1f188-109">範例1：啟用 advisor 的自動執行</span><span class="sxs-lookup"><span data-stu-id="1f188-109">Example 1: Enable auto execute for an advisor</span></span>
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

<span data-ttu-id="1f188-110">這個命令會將名為 CreateIndex 的 advisor 的自動執行狀態變更為 [啟用]。</span><span class="sxs-lookup"><span data-stu-id="1f188-110">This command changes the auto execute status of an advisor named CreateIndex to Enabled.</span></span>

## <span data-ttu-id="1f188-111">參數</span><span class="sxs-lookup"><span data-stu-id="1f188-111">PARAMETERS</span></span>

### <span data-ttu-id="1f188-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="1f188-112">-AdvisorName</span></span>
<span data-ttu-id="1f188-113">指定此 Cmdlet 修改狀態的顧問名稱。</span><span class="sxs-lookup"><span data-stu-id="1f188-113">Specifies the name of the advisor for which this cmdlet modifies the status.</span></span>

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

### <span data-ttu-id="1f188-114">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="1f188-114">-AutoExecuteStatus</span></span>
<span data-ttu-id="1f188-115">指定狀態的值。</span><span class="sxs-lookup"><span data-stu-id="1f188-115">Specifies the value for the status.</span></span>
<span data-ttu-id="1f188-116">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="1f188-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1f188-117">後</span><span class="sxs-lookup"><span data-stu-id="1f188-117">Enabled</span></span> 
- <span data-ttu-id="1f188-118">禁止</span><span class="sxs-lookup"><span data-stu-id="1f188-118">Disabled</span></span> 
- <span data-ttu-id="1f188-119">設置</span><span class="sxs-lookup"><span data-stu-id="1f188-119">Default</span></span>

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

### <span data-ttu-id="1f188-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1f188-120">-DatabaseName</span></span>
<span data-ttu-id="1f188-121">指定此 Cmdlet 修改狀態的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="1f188-121">Specifies the name of the database for which this cmdlet modifies status.</span></span>

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

### <span data-ttu-id="1f188-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f188-122">-DefaultProfile</span></span>
<span data-ttu-id="1f188-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="1f188-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f188-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f188-124">-ResourceGroupName</span></span>
<span data-ttu-id="1f188-125">指定包含此資料庫之伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1f188-125">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="1f188-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1f188-126">-ServerName</span></span>
<span data-ttu-id="1f188-127">指定資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="1f188-127">Specifies the name of the server for the database.</span></span>

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

### <span data-ttu-id="1f188-128">-確認</span><span class="sxs-lookup"><span data-stu-id="1f188-128">-Confirm</span></span>
<span data-ttu-id="1f188-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1f188-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f188-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f188-130">-WhatIf</span></span>
<span data-ttu-id="1f188-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1f188-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f188-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1f188-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f188-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f188-133">CommonParameters</span></span>
<span data-ttu-id="1f188-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1f188-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f188-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1f188-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f188-136">輸入</span><span class="sxs-lookup"><span data-stu-id="1f188-136">INPUTS</span></span>

### <span data-ttu-id="1f188-137">System.object</span><span class="sxs-lookup"><span data-stu-id="1f188-137">System.String</span></span>

### <span data-ttu-id="1f188-138">AdvisorAutoExecuteStatus 中的 [.Sql] 命令</span><span class="sxs-lookup"><span data-stu-id="1f188-138">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="1f188-139">輸出</span><span class="sxs-lookup"><span data-stu-id="1f188-139">OUTPUTS</span></span>

### <span data-ttu-id="1f188-140">AzureSqlDatabaseAdvisorModel 中的 [.Sql] 命令</span><span class="sxs-lookup"><span data-stu-id="1f188-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>

## <span data-ttu-id="1f188-141">筆記</span><span class="sxs-lookup"><span data-stu-id="1f188-141">NOTES</span></span>

## <span data-ttu-id="1f188-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="1f188-142">RELATED LINKS</span></span>

[<span data-ttu-id="1f188-143">AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="1f188-143">Get-AzSqlDatabaseAdvisor</span></span>](./Get-AzSqlDatabaseAdvisor.md)

[<span data-ttu-id="1f188-144">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="1f188-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

