---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 62B9754D-5EBF-4BEE-B07A-3E508C918F03
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldeleteddatabasebackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDeletedDatabaseBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDeletedDatabaseBackup.md
ms.openlocfilehash: 2358383cd7cfdbf547ae14476e788d6919baacd0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444300"
---
# <span data-ttu-id="a32f4-101">Get-AzureRmSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="a32f4-101">Get-AzureRmSqlDeletedDatabaseBackup</span></span>

## <span data-ttu-id="a32f4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a32f4-102">SYNOPSIS</span></span>
<span data-ttu-id="a32f4-103">取得您可以還原的已刪除資料庫。</span><span class="sxs-lookup"><span data-stu-id="a32f4-103">Gets a deleted database that you can restore.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a32f4-104">句法</span><span class="sxs-lookup"><span data-stu-id="a32f4-104">SYNTAX</span></span>

```
Get-AzureRmSqlDeletedDatabaseBackup [-ServerName] <String> [[-DatabaseName] <String>]
 [[-DeletionDate] <DateTime>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a32f4-105">說明</span><span class="sxs-lookup"><span data-stu-id="a32f4-105">DESCRIPTION</span></span>
<span data-ttu-id="a32f4-106">**AzureRMSqlDeletedDatabaseBackup** Cmdlet 會取得您可以還原的指定已刪除 SQL 資料庫備份，或是您可以還原的所有已刪除備份。</span><span class="sxs-lookup"><span data-stu-id="a32f4-106">The **Get-AzureRMSqlDeletedDatabaseBackup** cmdlet gets a specified deleted SQL database backup that you can restore, or all deleted backups that you can restore.</span></span>

<span data-ttu-id="a32f4-107">Azure 上的 SQL Server Stretch Database 服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a32f4-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="a32f4-108">示例</span><span class="sxs-lookup"><span data-stu-id="a32f4-108">EXAMPLES</span></span>

### <span data-ttu-id="a32f4-109">範例1：在伺服器上取得所有已刪除的資料庫備份</span><span class="sxs-lookup"><span data-stu-id="a32f4-109">Example 1: Get all deleted database backups on a server</span></span>
```
PS C:\>Get-AzureRMSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="a32f4-110">這個命令會在伺服器上取得所有已刪除的資料庫備份。</span><span class="sxs-lookup"><span data-stu-id="a32f4-110">This command gets all deleted database backups on a server.</span></span>

### <span data-ttu-id="a32f4-111">範例2：取得指定的已刪除資料庫備份</span><span class="sxs-lookup"><span data-stu-id="a32f4-111">Example 2: Get a specified deleted database backup</span></span>
```
PS C:\>Get-AzureRMSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="a32f4-112">這個命令會取得 ContosoDatabase 的已刪除資料庫備份。</span><span class="sxs-lookup"><span data-stu-id="a32f4-112">This command gets the deleted database backup for ContosoDatabase.</span></span>

## <span data-ttu-id="a32f4-113">參數</span><span class="sxs-lookup"><span data-stu-id="a32f4-113">PARAMETERS</span></span>

### <span data-ttu-id="a32f4-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a32f4-114">-DatabaseName</span></span>
<span data-ttu-id="a32f4-115">指定資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="a32f4-115">Specifies the name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a32f4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a32f4-116">-DefaultProfile</span></span>
<span data-ttu-id="a32f4-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a32f4-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a32f4-118">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="a32f4-118">-DeletionDate</span></span>
<span data-ttu-id="a32f4-119">指定資料庫已刪除的日期，做為 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="a32f4-119">Specifies the date, as a **DateTime** object, that the database was deleted.</span></span>
<span data-ttu-id="a32f4-120">若要取得 **DateTime** 物件，請使用 Get-Date Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a32f4-120">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a32f4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a32f4-121">-ResourceGroupName</span></span>
<span data-ttu-id="a32f4-122">指定指派給伺服器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a32f4-122">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a32f4-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a32f4-123">-ServerName</span></span>
<span data-ttu-id="a32f4-124">指定資料庫伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="a32f4-124">Specifies the name of the database server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a32f4-125">-確認</span><span class="sxs-lookup"><span data-stu-id="a32f4-125">-Confirm</span></span>
<span data-ttu-id="a32f4-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a32f4-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a32f4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a32f4-127">-WhatIf</span></span>
<span data-ttu-id="a32f4-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a32f4-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a32f4-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a32f4-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a32f4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a32f4-130">CommonParameters</span></span>
<span data-ttu-id="a32f4-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a32f4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a32f4-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a32f4-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a32f4-133">輸入</span><span class="sxs-lookup"><span data-stu-id="a32f4-133">INPUTS</span></span>

### <span data-ttu-id="a32f4-134">所有</span><span class="sxs-lookup"><span data-stu-id="a32f4-134">None</span></span>
<span data-ttu-id="a32f4-135">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="a32f4-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a32f4-136">輸出</span><span class="sxs-lookup"><span data-stu-id="a32f4-136">OUTPUTS</span></span>

## <span data-ttu-id="a32f4-137">筆記</span><span class="sxs-lookup"><span data-stu-id="a32f4-137">NOTES</span></span>

## <span data-ttu-id="a32f4-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="a32f4-138">RELATED LINKS</span></span>

[<span data-ttu-id="a32f4-139">AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a32f4-139">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="a32f4-140">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="a32f4-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
