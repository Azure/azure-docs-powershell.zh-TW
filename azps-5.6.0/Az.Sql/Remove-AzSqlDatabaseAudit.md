---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/Remove-AzSqlDatabaseAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseAudit.md
ms.openlocfilehash: 9688475a1d8bae19b10bc5626dca643ac947156d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904274"
---
# <span data-ttu-id="daeff-101">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="daeff-101">Remove-AzSqlDatabaseAudit</span></span>

## <span data-ttu-id="daeff-102">簡介</span><span class="sxs-lookup"><span data-stu-id="daeff-102">SYNOPSIS</span></span>
<span data-ttu-id="daeff-103">移除 Azure SQL 資料庫的稽核設定。</span><span class="sxs-lookup"><span data-stu-id="daeff-103">Removes the auditing settings of an Azure SQL database.</span></span>

## <span data-ttu-id="daeff-104">語法</span><span class="sxs-lookup"><span data-stu-id="daeff-104">SYNTAX</span></span>

### <span data-ttu-id="daeff-105">DatabaseParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="daeff-105">DatabaseParameterSet (Default)</span></span>
```
Remove-AzSqlDatabaseAudit [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="daeff-106">DatabaseObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="daeff-106">DatabaseObjectParameterSet</span></span>
```
Remove-AzSqlDatabaseAudit -DatabaseObject <AzureSqlDatabaseModel> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="daeff-107">描述</span><span class="sxs-lookup"><span data-stu-id="daeff-107">DESCRIPTION</span></span>
<span data-ttu-id="daeff-108">**Remove-AzSqlDatabaseAudit** Cmdlet 會移除 Azure SQL 資料庫的稽核設定。</span><span class="sxs-lookup"><span data-stu-id="daeff-108">The **Remove-AzSqlDatabaseAudit** cmdlet removes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="daeff-109">若要使用 Cmdlet，請使用 *ResourceGroupName、ServerName* 和 *DatabaseName* 參數來識別資料庫。</span><span class="sxs-lookup"><span data-stu-id="daeff-109">To use the cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="daeff-110">例子</span><span class="sxs-lookup"><span data-stu-id="daeff-110">EXAMPLES</span></span>

### <span data-ttu-id="daeff-111">範例 1：移除 Azure SQL 資料庫的稽核設定</span><span class="sxs-lookup"><span data-stu-id="daeff-111">Example 1: Remove the auditing settings of an Azure SQL database</span></span>
```
PS C:\>Remove-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

### <span data-ttu-id="daeff-112">範例 2：透過管線移除 Azure SQL 資料庫的稽核設定</span><span class="sxs-lookup"><span data-stu-id="daeff-112">Example 2: Remove, through pipeline, the auditing settings of an Azure SQL database</span></span>
```
PS C:\> Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Remove-AzSqlDatabaseAudit
```

## <span data-ttu-id="daeff-113">參數</span><span class="sxs-lookup"><span data-stu-id="daeff-113">PARAMETERS</span></span>

### <span data-ttu-id="daeff-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="daeff-114">-DatabaseName</span></span>
<span data-ttu-id="daeff-115">SQL 資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="daeff-115">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daeff-116">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="daeff-116">-DatabaseObject</span></span>
<span data-ttu-id="daeff-117">要管理其稽核策略的資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="daeff-117">The database object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="daeff-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daeff-118">-DefaultProfile</span></span>
<span data-ttu-id="daeff-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="daeff-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="daeff-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="daeff-120">-ResourceGroupName</span></span>
<span data-ttu-id="daeff-121">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="daeff-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daeff-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="daeff-122">-ServerName</span></span>
<span data-ttu-id="daeff-123">SQL 伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="daeff-123">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daeff-124">-確認</span><span class="sxs-lookup"><span data-stu-id="daeff-124">-Confirm</span></span>
<span data-ttu-id="daeff-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="daeff-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="daeff-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="daeff-126">-WhatIf</span></span>
<span data-ttu-id="daeff-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="daeff-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="daeff-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="daeff-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="daeff-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daeff-129">CommonParameters</span></span>
<span data-ttu-id="daeff-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="daeff-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daeff-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="daeff-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daeff-132">輸入</span><span class="sxs-lookup"><span data-stu-id="daeff-132">INPUTS</span></span>

### <span data-ttu-id="daeff-133">System.String</span><span class="sxs-lookup"><span data-stu-id="daeff-133">System.String</span></span>

### <span data-ttu-id="daeff-134">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="daeff-134">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="daeff-135">輸出</span><span class="sxs-lookup"><span data-stu-id="daeff-135">OUTPUTS</span></span>

### <span data-ttu-id="daeff-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="daeff-136">System.Boolean</span></span>

## <span data-ttu-id="daeff-137">筆記</span><span class="sxs-lookup"><span data-stu-id="daeff-137">NOTES</span></span>

## <span data-ttu-id="daeff-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="daeff-138">RELATED LINKS</span></span>
