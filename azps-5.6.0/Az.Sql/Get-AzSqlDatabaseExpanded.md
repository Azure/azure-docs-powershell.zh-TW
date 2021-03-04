---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 952967EB-AEAD-4597-B837-6669CE73739E
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabaseexpanded
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseExpanded.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseExpanded.md
ms.openlocfilehash: d7eb52a9da5866b4aed280f1ac35651800c67a25
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913302"
---
# <span data-ttu-id="87df0-101">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="87df0-101">Get-AzSqlDatabaseExpanded</span></span>

## <span data-ttu-id="87df0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="87df0-102">SYNOPSIS</span></span>
<span data-ttu-id="87df0-103">獲得資料庫及其展開的屬性值。</span><span class="sxs-lookup"><span data-stu-id="87df0-103">Gets a database and its expanded property values.</span></span>

## <span data-ttu-id="87df0-104">語法</span><span class="sxs-lookup"><span data-stu-id="87df0-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseExpanded [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87df0-105">描述</span><span class="sxs-lookup"><span data-stu-id="87df0-105">DESCRIPTION</span></span>
<span data-ttu-id="87df0-106">**Get-AzSqlDatabaseExpanded** Cmdlet 會取得資料庫及其展開的屬性值。</span><span class="sxs-lookup"><span data-stu-id="87df0-106">The **Get-AzSqlDatabaseExpanded** cmdlet gets a database and its expanded property values.</span></span>
<span data-ttu-id="87df0-107">Azure 上的 SQL Server 延伸資料庫服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="87df0-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="87df0-108">例子</span><span class="sxs-lookup"><span data-stu-id="87df0-108">EXAMPLES</span></span>

### <span data-ttu-id="87df0-109">範例 1：取得具有服務層級建議程式資訊的資料庫物件</span><span class="sxs-lookup"><span data-stu-id="87df0-109">Example 1: Get database object that has service tier advisor information</span></span>
```
PS C:\> Get-AzSqlDatabaseExpanded -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="87df0-110">此命令會返回包含服務層級建議程式資訊的已展開屬性的資料庫。</span><span class="sxs-lookup"><span data-stu-id="87df0-110">This command returns the database that has expanded properties that contain the service tier advisor information.</span></span>

### <span data-ttu-id="87df0-111">範例 2：使用篩選列出資料庫物件</span><span class="sxs-lookup"><span data-stu-id="87df0-111">Example 2: List database objects using filtering</span></span>
```
PS C:\> Get-AzSqlDatabaseExpanded -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database*"
```

<span data-ttu-id="87df0-112">此命令會針對 Server01 中以「資料庫」為起始的所有資料庫，會返回展開的資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="87df0-112">This command returns expanded database object for all databases in Server01 that start with "Database".</span></span>

## <span data-ttu-id="87df0-113">參數</span><span class="sxs-lookup"><span data-stu-id="87df0-113">PARAMETERS</span></span>

### <span data-ttu-id="87df0-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="87df0-114">-DatabaseName</span></span>
<span data-ttu-id="87df0-115">指定要取得的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="87df0-115">Specifies the name of the database to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87df0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87df0-116">-DefaultProfile</span></span>
<span data-ttu-id="87df0-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="87df0-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="87df0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87df0-118">-ResourceGroupName</span></span>
<span data-ttu-id="87df0-119">指定伺服器指派給的資源組名。</span><span class="sxs-lookup"><span data-stu-id="87df0-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="87df0-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="87df0-120">-ServerName</span></span>
<span data-ttu-id="87df0-121">指定主資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="87df0-121">Specifies the name of the server that hosts the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87df0-122">-確認</span><span class="sxs-lookup"><span data-stu-id="87df0-122">-Confirm</span></span>
<span data-ttu-id="87df0-123">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="87df0-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87df0-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87df0-124">-WhatIf</span></span>
<span data-ttu-id="87df0-125">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="87df0-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87df0-126">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="87df0-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87df0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87df0-127">CommonParameters</span></span>
<span data-ttu-id="87df0-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="87df0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87df0-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="87df0-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87df0-130">輸入</span><span class="sxs-lookup"><span data-stu-id="87df0-130">INPUTS</span></span>

### <span data-ttu-id="87df0-131">System.String</span><span class="sxs-lookup"><span data-stu-id="87df0-131">System.String</span></span>

## <span data-ttu-id="87df0-132">輸出</span><span class="sxs-lookup"><span data-stu-id="87df0-132">OUTPUTS</span></span>

### <span data-ttu-id="87df0-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModelExpanded</span><span class="sxs-lookup"><span data-stu-id="87df0-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModelExpanded</span></span>

## <span data-ttu-id="87df0-134">筆記</span><span class="sxs-lookup"><span data-stu-id="87df0-134">NOTES</span></span>

## <span data-ttu-id="87df0-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="87df0-135">RELATED LINKS</span></span>

[<span data-ttu-id="87df0-136">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="87df0-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
