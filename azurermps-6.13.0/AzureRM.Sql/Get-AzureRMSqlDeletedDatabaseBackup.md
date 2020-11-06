---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 62B9754D-5EBF-4BEE-B07A-3E508C918F03
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldeleteddatabasebackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDeletedDatabaseBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDeletedDatabaseBackup.md
ms.openlocfilehash: 2373a076e6edd97314e08c9170f9584a904ad902
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448196"
---
# <span data-ttu-id="66970-101">Get-AzureRmSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="66970-101">Get-AzureRmSqlDeletedDatabaseBackup</span></span>

## <span data-ttu-id="66970-102">摘要</span><span class="sxs-lookup"><span data-stu-id="66970-102">SYNOPSIS</span></span>
<span data-ttu-id="66970-103">取得您可以還原的已刪除資料庫。</span><span class="sxs-lookup"><span data-stu-id="66970-103">Gets a deleted database that you can restore.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66970-104">句法</span><span class="sxs-lookup"><span data-stu-id="66970-104">SYNTAX</span></span>

```
Get-AzureRmSqlDeletedDatabaseBackup [-ServerName] <String> [[-DatabaseName] <String>]
 [[-DeletionDate] <DateTime>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66970-105">說明</span><span class="sxs-lookup"><span data-stu-id="66970-105">DESCRIPTION</span></span>
<span data-ttu-id="66970-106">**AzureRMSqlDeletedDatabaseBackup** Cmdlet 會取得您可以還原的指定已刪除 SQL 資料庫備份，或是您可以還原的所有已刪除備份。</span><span class="sxs-lookup"><span data-stu-id="66970-106">The **Get-AzureRMSqlDeletedDatabaseBackup** cmdlet gets a specified deleted SQL database backup that you can restore, or all deleted backups that you can restore.</span></span>
<span data-ttu-id="66970-107">Azure 上的 SQL Server Stretch Database 服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="66970-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="66970-108">示例</span><span class="sxs-lookup"><span data-stu-id="66970-108">EXAMPLES</span></span>

### <span data-ttu-id="66970-109">範例1：在伺服器上取得所有已刪除的資料庫備份</span><span class="sxs-lookup"><span data-stu-id="66970-109">Example 1: Get all deleted database backups on a server</span></span>
```
PS C:\>Get-AzureRMSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="66970-110">這個命令會在伺服器上取得所有已刪除的資料庫備份。</span><span class="sxs-lookup"><span data-stu-id="66970-110">This command gets all deleted database backups on a server.</span></span>

### <span data-ttu-id="66970-111">範例2：取得指定的已刪除資料庫備份</span><span class="sxs-lookup"><span data-stu-id="66970-111">Example 2: Get a specified deleted database backup</span></span>
```
PS C:\>Get-AzureRMSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="66970-112">這個命令會取得 ContosoDatabase 的已刪除資料庫備份。</span><span class="sxs-lookup"><span data-stu-id="66970-112">This command gets the deleted database backup for ContosoDatabase.</span></span>

## <span data-ttu-id="66970-113">參數</span><span class="sxs-lookup"><span data-stu-id="66970-113">PARAMETERS</span></span>

### <span data-ttu-id="66970-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="66970-114">-DatabaseName</span></span>
<span data-ttu-id="66970-115">指定資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="66970-115">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="66970-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66970-116">-DefaultProfile</span></span>
<span data-ttu-id="66970-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="66970-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="66970-118">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="66970-118">-DeletionDate</span></span>
<span data-ttu-id="66970-119">指定資料庫已刪除的日期，做為 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="66970-119">Specifies the date, as a **DateTime** object, that the database was deleted.</span></span>
<span data-ttu-id="66970-120">若要取得 **DateTime** 物件，請使用 Get-Date Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="66970-120">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66970-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66970-121">-ResourceGroupName</span></span>
<span data-ttu-id="66970-122">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="66970-122">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="66970-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="66970-123">-ServerName</span></span>
<span data-ttu-id="66970-124">指定資料庫伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="66970-124">Specifies the name of the database server.</span></span>

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

### <span data-ttu-id="66970-125">-確認</span><span class="sxs-lookup"><span data-stu-id="66970-125">-Confirm</span></span>
<span data-ttu-id="66970-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="66970-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66970-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66970-127">-WhatIf</span></span>
<span data-ttu-id="66970-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="66970-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66970-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="66970-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66970-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66970-130">CommonParameters</span></span>
<span data-ttu-id="66970-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="66970-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66970-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="66970-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66970-133">輸入</span><span class="sxs-lookup"><span data-stu-id="66970-133">INPUTS</span></span>

### <span data-ttu-id="66970-134">System.object</span><span class="sxs-lookup"><span data-stu-id="66970-134">System.String</span></span>

### <span data-ttu-id="66970-135">系統. Nullable "1 [[System. DateTime，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="66970-135">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="66970-136">輸出</span><span class="sxs-lookup"><span data-stu-id="66970-136">OUTPUTS</span></span>

### <span data-ttu-id="66970-137">AzureSqlDeletedDatabaseBackupModel 中的 [.Sql]。</span><span class="sxs-lookup"><span data-stu-id="66970-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDeletedDatabaseBackupModel</span></span>

## <span data-ttu-id="66970-138">筆記</span><span class="sxs-lookup"><span data-stu-id="66970-138">NOTES</span></span>

## <span data-ttu-id="66970-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="66970-139">RELATED LINKS</span></span>

[<span data-ttu-id="66970-140">AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="66970-140">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="66970-141">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="66970-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
