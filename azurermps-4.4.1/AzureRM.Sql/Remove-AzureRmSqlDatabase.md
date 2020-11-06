---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B396388D-F91C-4BC9-A211-ABFF5DFC1693
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabase.md
ms.openlocfilehash: 1660c92ef4bef4cd832bc60506f7ef24d8927313
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457247"
---
# <span data-ttu-id="ff76d-101">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ff76d-101">Remove-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="ff76d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ff76d-102">SYNOPSIS</span></span>
<span data-ttu-id="ff76d-103">移除 Azure SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="ff76d-103">Removes an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff76d-104">句法</span><span class="sxs-lookup"><span data-stu-id="ff76d-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabase [-DatabaseName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ff76d-105">說明</span><span class="sxs-lookup"><span data-stu-id="ff76d-105">DESCRIPTION</span></span>
<span data-ttu-id="ff76d-106">**AzureRmSqlDatabase** Cmdlet 會移除 Azure SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="ff76d-106">The **Remove-AzureRmSqlDatabase** cmdlet removes an Azure SQL database.</span></span>

<span data-ttu-id="ff76d-107">Azure 上的 SQL Server Stretch Database 服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ff76d-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="ff76d-108">示例</span><span class="sxs-lookup"><span data-stu-id="ff76d-108">EXAMPLES</span></span>

### <span data-ttu-id="ff76d-109">範例1：從 Azure SQL server 移除資料庫</span><span class="sxs-lookup"><span data-stu-id="ff76d-109">Example 1: Remove a database from an Azure SQL server</span></span>
```
PS C:\>Remove-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="ff76d-110">這個命令會從伺服器 Server01 中移除名為 Database01 的資料庫。</span><span class="sxs-lookup"><span data-stu-id="ff76d-110">This command removes the database named Database01 from server Server01.</span></span>

## <span data-ttu-id="ff76d-111">參數</span><span class="sxs-lookup"><span data-stu-id="ff76d-111">PARAMETERS</span></span>

### <span data-ttu-id="ff76d-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ff76d-112">-DatabaseName</span></span>
<span data-ttu-id="ff76d-113">指定此 Cmdlet 移除之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="ff76d-113">Specifies the name of the database that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff76d-114">-Force</span><span class="sxs-lookup"><span data-stu-id="ff76d-114">-Force</span></span>
<span data-ttu-id="ff76d-115">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="ff76d-115">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff76d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff76d-116">-ResourceGroupName</span></span>
<span data-ttu-id="ff76d-117">指定指派給資料庫的 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ff76d-117">Specifies the name of the Azure resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="ff76d-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ff76d-118">-ServerName</span></span>
<span data-ttu-id="ff76d-119">指定託管資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="ff76d-119">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="ff76d-120">-確認</span><span class="sxs-lookup"><span data-stu-id="ff76d-120">-Confirm</span></span>
<span data-ttu-id="ff76d-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ff76d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff76d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff76d-122">-WhatIf</span></span>
<span data-ttu-id="ff76d-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ff76d-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff76d-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ff76d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff76d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff76d-125">-DefaultProfile</span></span>
<span data-ttu-id="ff76d-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ff76d-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff76d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff76d-127">CommonParameters</span></span>
<span data-ttu-id="ff76d-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ff76d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff76d-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ff76d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff76d-130">輸入</span><span class="sxs-lookup"><span data-stu-id="ff76d-130">INPUTS</span></span>

### <span data-ttu-id="ff76d-131">AzureSqlDatabaseModel （.Sql）的。</span><span class="sxs-lookup"><span data-stu-id="ff76d-131">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="ff76d-132">輸出</span><span class="sxs-lookup"><span data-stu-id="ff76d-132">OUTPUTS</span></span>

### <span data-ttu-id="ff76d-133">AzureSqlDatabaseModel （.Sql）的。</span><span class="sxs-lookup"><span data-stu-id="ff76d-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="ff76d-134">筆記</span><span class="sxs-lookup"><span data-stu-id="ff76d-134">NOTES</span></span>

## <span data-ttu-id="ff76d-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="ff76d-135">RELATED LINKS</span></span>

[<span data-ttu-id="ff76d-136">AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ff76d-136">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="ff76d-137">新-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ff76d-137">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="ff76d-138">Resume-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ff76d-138">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="ff76d-139">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ff76d-139">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="ff76d-140">暫停-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ff76d-140">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="ff76d-141">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="ff76d-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


