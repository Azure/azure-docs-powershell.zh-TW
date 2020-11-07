---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 952967EB-AEAD-4597-B837-6669CE73739E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseexpanded
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseExpanded.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseExpanded.md
ms.openlocfilehash: 9ff2284e602fe0bb9a7afea886385a02f89298a7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792561"
---
# <span data-ttu-id="835f7-101">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="835f7-101">Get-AzSqlDatabaseExpanded</span></span>

## <span data-ttu-id="835f7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="835f7-102">SYNOPSIS</span></span>
<span data-ttu-id="835f7-103">取得資料庫及其展開的屬性值。</span><span class="sxs-lookup"><span data-stu-id="835f7-103">Gets a database and its expanded property values.</span></span>

## <span data-ttu-id="835f7-104">句法</span><span class="sxs-lookup"><span data-stu-id="835f7-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseExpanded [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="835f7-105">說明</span><span class="sxs-lookup"><span data-stu-id="835f7-105">DESCRIPTION</span></span>
<span data-ttu-id="835f7-106">**AzSqlDatabaseExpanded** Cmdlet 會取得資料庫及其展開的屬性值。</span><span class="sxs-lookup"><span data-stu-id="835f7-106">The **Get-AzSqlDatabaseExpanded** cmdlet gets a database and its expanded property values.</span></span>
<span data-ttu-id="835f7-107">Azure 上的 SQL Server Stretch Database 服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="835f7-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="835f7-108">示例</span><span class="sxs-lookup"><span data-stu-id="835f7-108">EXAMPLES</span></span>

### <span data-ttu-id="835f7-109">範例1：取得擁有 service 層 advisor 資訊的資料庫物件</span><span class="sxs-lookup"><span data-stu-id="835f7-109">Example 1: Get database object that has service tier advisor information</span></span>
```
PS C:\> Get-AzSqlDatabaseExpanded -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="835f7-110">這個命令會傳回展開屬性的資料庫，其中包含服務層顧問資訊。</span><span class="sxs-lookup"><span data-stu-id="835f7-110">This command returns the database that has expanded properties that contain the service tier advisor information.</span></span>

### <span data-ttu-id="835f7-111">範例2：使用篩選來列出資料庫物件</span><span class="sxs-lookup"><span data-stu-id="835f7-111">Example 2: List database objects using filtering</span></span>
```
PS C:\> Get-AzSqlDatabaseExpanded -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database*"
```

<span data-ttu-id="835f7-112">這個命令會針對以 "Database" 開頭的 Server01 中的所有資料庫，傳回擴充的資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="835f7-112">This command returns expanded database object for all databases in Server01 that start with "Database".</span></span>

## <span data-ttu-id="835f7-113">參數</span><span class="sxs-lookup"><span data-stu-id="835f7-113">PARAMETERS</span></span>

### <span data-ttu-id="835f7-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="835f7-114">-DatabaseName</span></span>
<span data-ttu-id="835f7-115">指定要取得之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="835f7-115">Specifies the name of the database to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="835f7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="835f7-116">-DefaultProfile</span></span>
<span data-ttu-id="835f7-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="835f7-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="835f7-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="835f7-118">-ResourceGroupName</span></span>
<span data-ttu-id="835f7-119">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="835f7-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="835f7-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="835f7-120">-ServerName</span></span>
<span data-ttu-id="835f7-121">指定託管資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="835f7-121">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="835f7-122">-確認</span><span class="sxs-lookup"><span data-stu-id="835f7-122">-Confirm</span></span>
<span data-ttu-id="835f7-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="835f7-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="835f7-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="835f7-124">-WhatIf</span></span>
<span data-ttu-id="835f7-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="835f7-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="835f7-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="835f7-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="835f7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="835f7-127">CommonParameters</span></span>
<span data-ttu-id="835f7-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="835f7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="835f7-129">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="835f7-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="835f7-130">輸入</span><span class="sxs-lookup"><span data-stu-id="835f7-130">INPUTS</span></span>

### <span data-ttu-id="835f7-131">System.object</span><span class="sxs-lookup"><span data-stu-id="835f7-131">System.String</span></span>

## <span data-ttu-id="835f7-132">輸出</span><span class="sxs-lookup"><span data-stu-id="835f7-132">OUTPUTS</span></span>

### <span data-ttu-id="835f7-133">AzureSqlDatabaseModelExpanded （.Sql）的。</span><span class="sxs-lookup"><span data-stu-id="835f7-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModelExpanded</span></span>

## <span data-ttu-id="835f7-134">筆記</span><span class="sxs-lookup"><span data-stu-id="835f7-134">NOTES</span></span>

## <span data-ttu-id="835f7-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="835f7-135">RELATED LINKS</span></span>

[<span data-ttu-id="835f7-136">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="835f7-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
