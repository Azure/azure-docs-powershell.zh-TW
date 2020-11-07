---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Remove-AzSqlDatabaseAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseAudit.md
ms.openlocfilehash: ad0103e2a4d529a4f306749a1d55ca0b6eadc013
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792702"
---
# <span data-ttu-id="df737-101">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="df737-101">Remove-AzSqlDatabaseAudit</span></span>

## <span data-ttu-id="df737-102">摘要</span><span class="sxs-lookup"><span data-stu-id="df737-102">SYNOPSIS</span></span>
<span data-ttu-id="df737-103">移除 Azure SQL 資料庫的審核設定。</span><span class="sxs-lookup"><span data-stu-id="df737-103">Removes the auditing settings of an Azure SQL database.</span></span>

## <span data-ttu-id="df737-104">句法</span><span class="sxs-lookup"><span data-stu-id="df737-104">SYNTAX</span></span>

### <span data-ttu-id="df737-105">DatabaseParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="df737-105">DatabaseParameterSet (Default)</span></span>
```
Remove-AzSqlDatabaseAudit [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df737-106">DatabaseObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="df737-106">DatabaseObjectParameterSet</span></span>
```
Remove-AzSqlDatabaseAudit -DatabaseObject <AzureSqlDatabaseModel> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df737-107">說明</span><span class="sxs-lookup"><span data-stu-id="df737-107">DESCRIPTION</span></span>
<span data-ttu-id="df737-108">**AzSqlDatabaseAudit** Cmdlet 會移除 Azure SQL 資料庫的審核設定。</span><span class="sxs-lookup"><span data-stu-id="df737-108">The **Remove-AzSqlDatabaseAudit** cmdlet removes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="df737-109">若要使用 Cmdlet，請使用 [ *ResourceGroupName* ]、[ *ServerName* ] 和 [ *DatabaseName* ] 參數來識別資料庫。</span><span class="sxs-lookup"><span data-stu-id="df737-109">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="df737-110">示例</span><span class="sxs-lookup"><span data-stu-id="df737-110">EXAMPLES</span></span>

### <span data-ttu-id="df737-111">範例1：移除 Azure SQL 資料庫的審核設定</span><span class="sxs-lookup"><span data-stu-id="df737-111">Example 1: Remove the auditing settings of an Azure SQL database</span></span>
```
PS C:\>Remove-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

### <span data-ttu-id="df737-112">範例2：在管道中移除 Azure SQL 資料庫的審核設定</span><span class="sxs-lookup"><span data-stu-id="df737-112">Example 2: Remove, through pipeline, the auditing settings of an Azure SQL database</span></span>
```
PS C:\> Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Remove-AzSqlDatabaseAudit
```

## <span data-ttu-id="df737-113">參數</span><span class="sxs-lookup"><span data-stu-id="df737-113">PARAMETERS</span></span>

### <span data-ttu-id="df737-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="df737-114">-DatabaseName</span></span>
<span data-ttu-id="df737-115">SQL 資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="df737-115">SQL Database name.</span></span>

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

### <span data-ttu-id="df737-116">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="df737-116">-DatabaseObject</span></span>
<span data-ttu-id="df737-117">要管理其審核原則的資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="df737-117">The database object to manage its audit policy.</span></span>

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

### <span data-ttu-id="df737-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df737-118">-DefaultProfile</span></span>
<span data-ttu-id="df737-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="df737-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df737-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df737-120">-ResourceGroupName</span></span>
<span data-ttu-id="df737-121">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="df737-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="df737-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="df737-122">-ServerName</span></span>
<span data-ttu-id="df737-123">SQL server 名稱。</span><span class="sxs-lookup"><span data-stu-id="df737-123">SQL server name.</span></span>

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

### <span data-ttu-id="df737-124">-確認</span><span class="sxs-lookup"><span data-stu-id="df737-124">-Confirm</span></span>
<span data-ttu-id="df737-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="df737-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df737-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df737-126">-WhatIf</span></span>
<span data-ttu-id="df737-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="df737-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="df737-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="df737-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df737-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df737-129">CommonParameters</span></span>
<span data-ttu-id="df737-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="df737-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df737-131">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="df737-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df737-132">輸入</span><span class="sxs-lookup"><span data-stu-id="df737-132">INPUTS</span></span>

### <span data-ttu-id="df737-133">System.object</span><span class="sxs-lookup"><span data-stu-id="df737-133">System.String</span></span>

### <span data-ttu-id="df737-134">AzureSqlDatabaseModel （.Sql）的。</span><span class="sxs-lookup"><span data-stu-id="df737-134">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="df737-135">輸出</span><span class="sxs-lookup"><span data-stu-id="df737-135">OUTPUTS</span></span>

### <span data-ttu-id="df737-136">System.object</span><span class="sxs-lookup"><span data-stu-id="df737-136">System.Boolean</span></span>

## <span data-ttu-id="df737-137">筆記</span><span class="sxs-lookup"><span data-stu-id="df737-137">NOTES</span></span>

## <span data-ttu-id="df737-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="df737-138">RELATED LINKS</span></span>
