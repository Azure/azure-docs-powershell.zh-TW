---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 7427A101-9439-45B9-B72E-F8C2DA85E412
online version: ''
schema: 2.0.0
ms.openlocfilehash: c10ae808d105079b9739516bf9eaf316241b1b11
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967744"
---
# <span data-ttu-id="0d17d-101">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0d17d-101">Get-AzureSqlDatabase</span></span>

## <span data-ttu-id="0d17d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0d17d-102">SYNOPSIS</span></span>
<span data-ttu-id="0d17d-103">檢索一或多個資料庫。</span><span class="sxs-lookup"><span data-stu-id="0d17d-103">Retrieves one or more databases.</span></span>

## <span data-ttu-id="0d17d-104">句法</span><span class="sxs-lookup"><span data-stu-id="0d17d-104">SYNTAX</span></span>

### <span data-ttu-id="0d17d-105">ByConnectionCoNtext (預設) </span><span class="sxs-lookup"><span data-stu-id="0d17d-105">ByConnectionContext (Default)</span></span>
```
Get-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> [-Database <Database>]
 [-DatabaseName <String>] [-RestorableDropped] [-RestorableDroppedDatabase <RestorableDroppedDatabase>]
 [-DatabaseDeletionDate <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0d17d-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="0d17d-106">ByServerName</span></span>
```
Get-AzureSqlDatabase -ServerName <String> [-Database <Database>] [-DatabaseName <String>] [-RestorableDropped]
 [-RestorableDroppedDatabase <RestorableDroppedDatabase>] [-DatabaseDeletionDate <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0d17d-107">說明</span><span class="sxs-lookup"><span data-stu-id="0d17d-107">DESCRIPTION</span></span>
<span data-ttu-id="0d17d-108">**AzureSqlDatabase** Cmdlet 會從 Azure sql 資料庫伺服器中檢索 Azure sql database 的一個或多個實例。</span><span class="sxs-lookup"><span data-stu-id="0d17d-108">The **Get-AzureSqlDatabase** cmdlet retrieves one or more instances of an Azure SQL Database from an Azure SQL Database server.</span></span>
<span data-ttu-id="0d17d-109">您可以使用 **AzureSqlDatabaseServerCoNtext** Cmdlet 所建立的 Azure SQL Database server 連接內容來指定伺服器。</span><span class="sxs-lookup"><span data-stu-id="0d17d-109">You can specify the server with an Azure SQL Database server connection context that you create using the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span>
<span data-ttu-id="0d17d-110">或者，如果您指定 Azure SQL 資料庫伺服器名稱，此 Cmdlet 會使用目前的 Azure 訂閱資訊來驗證訪問伺服器的要求。</span><span class="sxs-lookup"><span data-stu-id="0d17d-110">Or, if you specify the Azure SQL Database server name, the cmdlet uses the current Azure subscription information to authenticate the request to access the server.</span></span>

<span data-ttu-id="0d17d-111">如果您沒有指定資料庫， **AzureSqlDatabase** Cmdlet 會傳回指定伺服器中的所有資料庫。</span><span class="sxs-lookup"><span data-stu-id="0d17d-111">If you do not specify a database, the **Get-AzureSqlDatabase** cmdlet returns all databases from the specified server.</span></span>

<span data-ttu-id="0d17d-112">檢索能還原的已丟棄資料庫：</span><span class="sxs-lookup"><span data-stu-id="0d17d-112">Retrieving restorable dropped databases:</span></span>

<span data-ttu-id="0d17d-113">使用 *RestorableDropped* 參數來檢索可還原的已刪除資料庫。</span><span class="sxs-lookup"><span data-stu-id="0d17d-113">Retrieve restorable dropped databases by using the *RestorableDropped* parameter.</span></span>
<span data-ttu-id="0d17d-114">若要傳回所有可還原的中斷資料庫，請使用不含 *DatabaseName* 和 *DatabaseDeletionDate* 的 *RestorableDropped* 參數。</span><span class="sxs-lookup"><span data-stu-id="0d17d-114">To return all restorable dropped databases use the *RestorableDropped* parameter without *DatabaseName* and *DatabaseDeletionDate*.</span></span>
<span data-ttu-id="0d17d-115">若要傳回特定的可還原已刪除的資料庫，請使用 *RestorableDropped* 參數及 *DatabaseName* 和 *DatabaseDeletionDate* 參數。</span><span class="sxs-lookup"><span data-stu-id="0d17d-115">To return a specific restorable dropped database use the *RestorableDropped* parameter with the *DatabaseName* and *DatabaseDeletionDate* parameters.</span></span>
<span data-ttu-id="0d17d-116">使用 *DatabaseName* 參數來檢索特定的可還原刪除的資料庫時，您也必須包含 *DatabaseDeletionDate* 參數，且指定的 *DatabaseDeletionDate* 值必須包含毫秒，才能符合所需的資料庫。</span><span class="sxs-lookup"><span data-stu-id="0d17d-116">When retrieving a specific restorable dropped database by using the *DatabaseName* parameter you must also include the *DatabaseDeletionDate* parameter and the specified *DatabaseDeletionDate* value must include milliseconds to match the desired database.</span></span>

<span data-ttu-id="0d17d-117">**AzureSqlDatabase** Cmdlet 會傳回伺服器上所有可還原的已丟棄資料庫，或傳回與 *DatabaseName* 和 *DatabaseDeletionDate* 相符的特定資料庫。</span><span class="sxs-lookup"><span data-stu-id="0d17d-117">The **Get-AzureSqlDatabase** cmdlet returns either all restorable dropped databases on a server, or one specific database that matches both *DatabaseName* and *DatabaseDeletionDate*.</span></span>
<span data-ttu-id="0d17d-118">若要傳回符合不同準則的可還原中斷資料庫（例如，所有可還原的特定名稱資料庫），您必須傳回所有可還原的已刪除資料庫，然後在用戶端上篩選結果。</span><span class="sxs-lookup"><span data-stu-id="0d17d-118">To return restorable dropped databases that satisfy different criteria, such as all restorable dropped databases of a specific name, you must return all restorable dropped databases, and then filter the results on the client.</span></span>

## <span data-ttu-id="0d17d-119">示例</span><span class="sxs-lookup"><span data-stu-id="0d17d-119">EXAMPLES</span></span>

### <span data-ttu-id="0d17d-120">範例1：在伺服器上檢索所有資料庫</span><span class="sxs-lookup"><span data-stu-id="0d17d-120">Example 1: Retrieve all databases on a server</span></span>
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="0d17d-121">這個命令會在伺服器上檢索名為 lpqd0zbr8y 的所有資料庫。</span><span class="sxs-lookup"><span data-stu-id="0d17d-121">This command retrieves all databases on the server named lpqd0zbr8y.</span></span>

### <span data-ttu-id="0d17d-122">範例2：在伺服器上檢索所有能還原的已丟棄資料庫</span><span class="sxs-lookup"><span data-stu-id="0d17d-122">Example 2: Retrieve all restorable dropped databases on a server</span></span>
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -RestorableDropped
```

<span data-ttu-id="0d17d-123">這個命令會在名為 lpqd0zbr8y 的伺服器上，檢索所有能還原的中斷資料庫。</span><span class="sxs-lookup"><span data-stu-id="0d17d-123">This command retrieves all restorable dropped databases on the server named lpqd0zbr8y.</span></span>

### <span data-ttu-id="0d17d-124">範例3：從連接內容所指定的伺服器中檢索資料庫</span><span class="sxs-lookup"><span data-stu-id="0d17d-124">Example 3: Retrieve a database from a server specified by a connection context</span></span>
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
```

<span data-ttu-id="0d17d-125">這個命令會從 $CoNtext 連接內容指定的伺服器中檢索名為 Database01 的資料庫。</span><span class="sxs-lookup"><span data-stu-id="0d17d-125">This command retrieves database named Database01 from the server specified by the connection context $Context.</span></span>

### <span data-ttu-id="0d17d-126">範例4：將資料庫物件儲存在變數中</span><span class="sxs-lookup"><span data-stu-id="0d17d-126">Example 4: Store a database object in a variable</span></span>
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
```

<span data-ttu-id="0d17d-127">這個命令會從伺服器（名為 lpqd0zbr8y）中檢索名為 Database01 的資料庫。</span><span class="sxs-lookup"><span data-stu-id="0d17d-127">This command retrieves database named Database01 from the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="0d17d-128">該命令會將資料庫物件儲存在 $Database 01 變數中。</span><span class="sxs-lookup"><span data-stu-id="0d17d-128">The command stores the database object in the $Database01 variable.</span></span>

### <span data-ttu-id="0d17d-129">範例5：取回還原的已刪除資料庫</span><span class="sxs-lookup"><span data-stu-id="0d17d-129">Example 5: Retrieve a restorable dropped database</span></span>
```
PS C:\> $DroppedDB = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01" -DatabaseDeletionDate "2012-11-09T22:59:43.000Z" -RestorableDropped
```

<span data-ttu-id="0d17d-130">這個命令會從伺服器（名為 lpqd0zbr8y）中檢索已從11/9/2012 刪除的可還原已刪除的 Database01 資料庫。</span><span class="sxs-lookup"><span data-stu-id="0d17d-130">This command retrieves the restorable dropped database named Database01 that was deleted on 11/9/2012 from the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="0d17d-131">這個命令會將結果儲存在 $DroppedDB 變數中。</span><span class="sxs-lookup"><span data-stu-id="0d17d-131">This command stores the results in the $DroppedDB variable.</span></span>

### <span data-ttu-id="0d17d-132">範例6：在伺服器上檢索所有能還原的中斷資料庫並篩選結果</span><span class="sxs-lookup"><span data-stu-id="0d17d-132">Example 6: Retrieve all restorable dropped databases on a server and filter the results</span></span>
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -RestorableDropped | Where-Object {$_.Name -eq "ContactDB"}
```

<span data-ttu-id="0d17d-133">這個命令會在名為 lpqd0zbr8y 的伺服器上檢索所有可還原的中斷資料庫，然後將結果篩選為僅限名為 ContactDB 的資料庫。</span><span class="sxs-lookup"><span data-stu-id="0d17d-133">This command retrieves all restorable dropped databases on the server named lpqd0zbr8y, and then filters the results to only the databases named ContactDB.</span></span>

## <span data-ttu-id="0d17d-134">參數</span><span class="sxs-lookup"><span data-stu-id="0d17d-134">PARAMETERS</span></span>

### <span data-ttu-id="0d17d-135">-ConnectionCoNtext</span><span class="sxs-lookup"><span data-stu-id="0d17d-135">-ConnectionContext</span></span>
<span data-ttu-id="0d17d-136">指定要從中檢索資料庫的伺服器連接內容。</span><span class="sxs-lookup"><span data-stu-id="0d17d-136">Specifies the connection context of a server from which to retrieve a database.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d17d-137">-資料庫</span><span class="sxs-lookup"><span data-stu-id="0d17d-137">-Database</span></span>
<span data-ttu-id="0d17d-138">指定代表此 Cmdlet 所檢索之資料庫的物件。</span><span class="sxs-lookup"><span data-stu-id="0d17d-138">Specifies an object that represents the database that this cmdlet retrieves.</span></span>

```yaml
Type: Database
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d17d-139">-DatabaseDeletionDate</span><span class="sxs-lookup"><span data-stu-id="0d17d-139">-DatabaseDeletionDate</span></span>
<span data-ttu-id="0d17d-140">指定刪除的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="0d17d-140">Specifies the date and time of a deletion.</span></span>
<span data-ttu-id="0d17d-141">如果您指定 *RestorableDropped* 參數，請指定此參數，以根據刪除日期和時間來檢索可還原的已刪除資料庫。</span><span class="sxs-lookup"><span data-stu-id="0d17d-141">If you specify the *RestorableDropped* parameter, specify this parameter to retrieve a restorable dropped database based on the deletion date and time.</span></span>

<span data-ttu-id="0d17d-142">*DatabaseDeletionDate* 參數必須包含毫秒，以符合所需資料庫的時間。</span><span class="sxs-lookup"><span data-stu-id="0d17d-142">The *DatabaseDeletionDate* parameter must include milliseconds to match the time of the desired database.</span></span>
<span data-ttu-id="0d17d-143">指定不含毫秒的值會產生資料庫找不到的結果。</span><span class="sxs-lookup"><span data-stu-id="0d17d-143">Specifying a value without milliseconds results in the database not being found.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d17d-144">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0d17d-144">-DatabaseName</span></span>
<span data-ttu-id="0d17d-145">指定此 Cmdlet 所檢索之資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d17d-145">Specifies the name of the database that this cmdlet retrieves.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d17d-146">-設定檔</span><span class="sxs-lookup"><span data-stu-id="0d17d-146">-Profile</span></span>
<span data-ttu-id="0d17d-147">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="0d17d-147">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0d17d-148">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="0d17d-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d17d-149">-RestorableDropped</span><span class="sxs-lookup"><span data-stu-id="0d17d-149">-RestorableDropped</span></span>
<span data-ttu-id="0d17d-150">表示此 Cmdlet 會傳回 *RestorableDroppedDatabase* 物件，而不是 *資料庫* 物件。</span><span class="sxs-lookup"><span data-stu-id="0d17d-150">Indicates that this cmdlet returns *RestorableDroppedDatabase* objects instead of *Database* objects.</span></span>
<span data-ttu-id="0d17d-151">您可以使用 *DatabaseDeletionDate* 參數來選取特定的可還原已刪除的資料庫。</span><span class="sxs-lookup"><span data-stu-id="0d17d-151">You can use the *DatabaseDeletionDate* parameter to select a specific restorable dropped database.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d17d-152">-RestorableDroppedDatabase</span><span class="sxs-lookup"><span data-stu-id="0d17d-152">-RestorableDroppedDatabase</span></span>
<span data-ttu-id="0d17d-153">指定代表此 Cmdlet 所檢索之可還原已刪除資料庫的物件。</span><span class="sxs-lookup"><span data-stu-id="0d17d-153">Specifies an object that represents the restorable dropped database that this cmdlet retrieves.</span></span>

```yaml
Type: RestorableDroppedDatabase
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d17d-154">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0d17d-154">-ServerName</span></span>
<span data-ttu-id="0d17d-155">指定包含此 Cmdlet 所檢索之資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="0d17d-155">Specifies the name of the server that contains the database that this cmdlet retrieves.</span></span>
<span data-ttu-id="0d17d-156">此 Cmdlet 會使用目前的 Azure 訂閱來存取伺服器。</span><span class="sxs-lookup"><span data-stu-id="0d17d-156">The cmdlet uses the current Azure subscription to access the server.</span></span>

```yaml
Type: String
Parameter Sets: ByServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d17d-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d17d-157">CommonParameters</span></span>
<span data-ttu-id="0d17d-158">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0d17d-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d17d-159">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0d17d-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d17d-160">輸入</span><span class="sxs-lookup"><span data-stu-id="0d17d-160">INPUTS</span></span>

### <span data-ttu-id="0d17d-161">SqlDatabase.. Database （WindowsAzure）</span><span class="sxs-lookup"><span data-stu-id="0d17d-161">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

### <span data-ttu-id="0d17d-162">SqlDatabase. RestorableDroppedDatabase （WindowsAzure）</span><span class="sxs-lookup"><span data-stu-id="0d17d-162">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase</span></span>

## <span data-ttu-id="0d17d-163">輸出</span><span class="sxs-lookup"><span data-stu-id="0d17d-163">OUTPUTS</span></span>

### <span data-ttu-id="0d17d-164">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database\></span><span class="sxs-lookup"><span data-stu-id="0d17d-164">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database\></span></span>
<span data-ttu-id="0d17d-165">如果您沒有指定 *RestorableDropped* 參數，此 Cmdlet 會傳回 *資料庫* 物件。</span><span class="sxs-lookup"><span data-stu-id="0d17d-165">This cmdlet returns a *Database* object if you do not specify the *RestorableDropped* parameter.</span></span>

### <span data-ttu-id="0d17d-166">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase\></span><span class="sxs-lookup"><span data-stu-id="0d17d-166">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase\></span></span>
<span data-ttu-id="0d17d-167">如果您指定 *RestorableDropped* 參數，這個 Cmdlet 會傳回 *RestorableDroppedDatabase* 物件。</span><span class="sxs-lookup"><span data-stu-id="0d17d-167">This cmdlet returns a *RestorableDroppedDatabase* object if you specify the *RestorableDropped* parameter.</span></span>

## <span data-ttu-id="0d17d-168">筆記</span><span class="sxs-lookup"><span data-stu-id="0d17d-168">NOTES</span></span>

## <span data-ttu-id="0d17d-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="0d17d-169">RELATED LINKS</span></span>

[<span data-ttu-id="0d17d-170">Azure SQL 資料庫</span><span class="sxs-lookup"><span data-stu-id="0d17d-170">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="0d17d-171">Azure SQL 資料庫的作業</span><span class="sxs-lookup"><span data-stu-id="0d17d-171">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="0d17d-172">新-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0d17d-172">New-AzureSqlDatabase</span></span>](./New-AzureSqlDatabase.md)

[<span data-ttu-id="0d17d-173">新-AzureSqlDatabaseServerCoNtext</span><span class="sxs-lookup"><span data-stu-id="0d17d-173">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)

[<span data-ttu-id="0d17d-174">移除-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0d17d-174">Remove-AzureSqlDatabase</span></span>](./Remove-AzureSqlDatabase.md)

[<span data-ttu-id="0d17d-175">Set-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0d17d-175">Set-AzureSqlDatabase</span></span>](./Set-AzureSqlDatabase.md)


