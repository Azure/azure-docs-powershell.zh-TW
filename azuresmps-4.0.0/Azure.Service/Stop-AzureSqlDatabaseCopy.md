---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: CB601E21-424D-4B09-85E5-A4B2A5068267
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7716587787515221a6e016436a6e3d030c1ab0eb
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405613"
---
# <span data-ttu-id="f4a04-101">Stop-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="f4a04-101">Stop-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="f4a04-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f4a04-102">SYNOPSIS</span></span>
<span data-ttu-id="f4a04-103">終止連續的複製關係。</span><span class="sxs-lookup"><span data-stu-id="f4a04-103">Terminates a continuous copy relationship.</span></span>

## <span data-ttu-id="f4a04-104">語法</span><span class="sxs-lookup"><span data-stu-id="f4a04-104">SYNTAX</span></span>

### <span data-ttu-id="f4a04-105">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f4a04-105">ByInputObject</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-ForcedTermination] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4a04-106">ByDatabase</span><span class="sxs-lookup"><span data-stu-id="f4a04-106">ByDatabase</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f4a04-107">ByDatabaseName</span><span class="sxs-lookup"><span data-stu-id="f4a04-107">ByDatabaseName</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f4a04-108">描述</span><span class="sxs-lookup"><span data-stu-id="f4a04-108">DESCRIPTION</span></span>
<span data-ttu-id="f4a04-109">**Stop-AzureSqlDatabaseCopy** Cmdlet 會終止連續的複製關係。</span><span class="sxs-lookup"><span data-stu-id="f4a04-109">The **Stop-AzureSqlDatabaseCopy** cmdlet terminates a continuous copy relationship.</span></span>
<span data-ttu-id="f4a04-110">此 Cmdlet 會停止源資料庫與次要或目標資料庫之間的資料移動，然後將次要資料庫的狀態變更為獨立線上資料庫。</span><span class="sxs-lookup"><span data-stu-id="f4a04-110">This cmdlet stops the data movement between the source database and secondary or target database, and then changes the state of the secondary database to be a stand-alone online database.</span></span>

<span data-ttu-id="f4a04-111">有兩種方法可以結束連續的複製關係、終止或計畫終止，以及可能的資料遺失強制終止。</span><span class="sxs-lookup"><span data-stu-id="f4a04-111">There are two ways to end a continuous copy relationship, termination or planned termination and forced termination with possible data loss.</span></span>
<span data-ttu-id="f4a04-112">在主管源資料庫的伺服器上，您可以在終止或強制終止模式中執行此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f4a04-112">On the server that hosts the source database, you can run this cmdlet in termination or forced termination mode.</span></span>
<span data-ttu-id="f4a04-113">在主託管次要資料庫的伺服器上，您必須使用強制終止模式。</span><span class="sxs-lookup"><span data-stu-id="f4a04-113">On the server that hosts the secondary database, you must use forced termination mode.</span></span>

<span data-ttu-id="f4a04-114">計畫終止會等到您執行 Cmdlet 時源資料庫上的所有已提交交易複製到次要資料庫。</span><span class="sxs-lookup"><span data-stu-id="f4a04-114">A planned termination waits until all committed transactions on the source database, at the time that you run the cmdlet, have been replicated to the secondary database.</span></span>
<span data-ttu-id="f4a04-115">強制終止不會等待複製任何未解決的已提交交易，而且可能會導致次要資料庫中的資料遺失。</span><span class="sxs-lookup"><span data-stu-id="f4a04-115">Forced termination does not wait for replication of any outstanding committed transactions, and can cause possible data loss in the secondary database.</span></span>

<span data-ttu-id="f4a04-116">當複製狀態為擱置中時，只有強制終止可以成功結束連續的複製關係。</span><span class="sxs-lookup"><span data-stu-id="f4a04-116">While replication status is PENDING, only forced termination can successfully end a continuous copy relationship.</span></span>
<span data-ttu-id="f4a04-117">如果複製狀態為擱置中，則不支援未強制終止。</span><span class="sxs-lookup"><span data-stu-id="f4a04-117">If the replication status is PENDING, termination that is not forced is not supported.</span></span>

## <span data-ttu-id="f4a04-118">例子</span><span class="sxs-lookup"><span data-stu-id="f4a04-118">EXAMPLES</span></span>

### <span data-ttu-id="f4a04-119">範例 1：終止連續的複製關係</span><span class="sxs-lookup"><span data-stu-id="f4a04-119">Example 1: Terminate a continuous copy relationship</span></span>
```
PS C:\>Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

<span data-ttu-id="f4a04-120">此命令會終止名為 lpqd0zbr8y 伺服器上名為 Orders 的資料庫之連續複製關係。</span><span class="sxs-lookup"><span data-stu-id="f4a04-120">This command terminates the continuous copy relationship of database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="f4a04-121">名為 bk0b8kf658 的伺服器主託管次要資料庫。</span><span class="sxs-lookup"><span data-stu-id="f4a04-121">The server named bk0b8kf658 hosts the secondary database.</span></span>

### <span data-ttu-id="f4a04-122">範例 2：因應性終止連續的複製關係</span><span class="sxs-lookup"><span data-stu-id="f4a04-122">Example 2: Forcibly terminate a continuous copy relationship</span></span>
```
PS C:\>$DatabaseCopy = Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders"
PS C:\> $DatabaseCopy | Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -ForcedTermination
```

<span data-ttu-id="f4a04-123">第一個命令會針對名為 lpqd0zbr8y 的伺服器上名為 Orders 的資料庫，獲得資料庫的資料庫複製關係。</span><span class="sxs-lookup"><span data-stu-id="f4a04-123">The first command gets the database copy relationship for the database named Orders on the server named lpqd0zbr8y.</span></span>

<span data-ttu-id="f4a04-124">第二個命令會終止來自主託管次要資料庫之伺服器的連續複製關係。</span><span class="sxs-lookup"><span data-stu-id="f4a04-124">The second command forcibly terminates a continuous copy relationship from the server that hosts the secondary database.</span></span>

## <span data-ttu-id="f4a04-125">參數</span><span class="sxs-lookup"><span data-stu-id="f4a04-125">PARAMETERS</span></span>

### <span data-ttu-id="f4a04-126">-資料庫</span><span class="sxs-lookup"><span data-stu-id="f4a04-126">-Database</span></span>
<span data-ttu-id="f4a04-127">指定代表來源 Azure SQL Database 的物件。</span><span class="sxs-lookup"><span data-stu-id="f4a04-127">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="f4a04-128">此 Cmdlet 會終止此參數指定之資料庫的連續複製關係。</span><span class="sxs-lookup"><span data-stu-id="f4a04-128">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>

```yaml
Type: Database
Parameter Sets: ByDatabase
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4a04-129">-DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="f4a04-129">-DatabaseCopy</span></span>
<span data-ttu-id="f4a04-130">指定代表資料庫的物件。</span><span class="sxs-lookup"><span data-stu-id="f4a04-130">Specifies an object that represents a database.</span></span>
<span data-ttu-id="f4a04-131">此 Cmdlet 會終止此參數指定之資料庫的連續複製關係。</span><span class="sxs-lookup"><span data-stu-id="f4a04-131">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>
<span data-ttu-id="f4a04-132">此參數接受管線輸入。</span><span class="sxs-lookup"><span data-stu-id="f4a04-132">This parameter accepts pipeline input.</span></span>

```yaml
Type: DatabaseCopy
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4a04-133">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f4a04-133">-DatabaseName</span></span>
<span data-ttu-id="f4a04-134">指定資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="f4a04-134">Specifies the name of a database.</span></span>
<span data-ttu-id="f4a04-135">此 Cmdlet 會終止此參數指定之資料庫的連續複製關係。</span><span class="sxs-lookup"><span data-stu-id="f4a04-135">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4a04-136">-強制</span><span class="sxs-lookup"><span data-stu-id="f4a04-136">-Force</span></span>
<span data-ttu-id="f4a04-137">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="f4a04-137">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f4a04-138">-ForcedTermination</span><span class="sxs-lookup"><span data-stu-id="f4a04-138">-ForcedTermination</span></span>
<span data-ttu-id="f4a04-139">表示此 Cmdlet 會導致連續的複製關係強制終止。</span><span class="sxs-lookup"><span data-stu-id="f4a04-139">Indicates that this cmdlet causes forced termination of the continuous copy relationship.</span></span>
<span data-ttu-id="f4a04-140">強制終止可能會導致資料遺失。</span><span class="sxs-lookup"><span data-stu-id="f4a04-140">Forced termination may cause with data loss.</span></span>
<span data-ttu-id="f4a04-141">若要在主管目標資料庫的伺服器上執行此 Cmdlet，您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="f4a04-141">To run this cmdlet on a server that hosts the target database, you must specify this parameter.</span></span>
<span data-ttu-id="f4a04-142">若要在主管源資料庫的伺服器上執行此 Cmdlet，如果次要資料庫無法使用，您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="f4a04-142">To run this cmdlet on a server that hosts the source database, if the secondary database is unavailable, you must specify this parameter.</span></span>

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

### <span data-ttu-id="f4a04-143">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="f4a04-143">-PartnerDatabase</span></span>
<span data-ttu-id="f4a04-144">指定次要資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="f4a04-144">Specifies name of the secondary database.</span></span>
<span data-ttu-id="f4a04-145">如果您指定名稱，該名稱必須與源資料庫的名稱相符。</span><span class="sxs-lookup"><span data-stu-id="f4a04-145">If you specify a name, it must match the name of the source database.</span></span>

```yaml
Type: String
Parameter Sets: ByDatabase, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4a04-146">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="f4a04-146">-PartnerServer</span></span>
<span data-ttu-id="f4a04-147">指定主託管目標資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="f4a04-147">Specifies the name of the server that hosts the target database.</span></span>

```yaml
Type: String
Parameter Sets: ByDatabase, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4a04-148">-設定檔</span><span class="sxs-lookup"><span data-stu-id="f4a04-148">-Profile</span></span>
<span data-ttu-id="f4a04-149">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="f4a04-149">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f4a04-150">如果您未指定設定檔，此 Cmdlet 會從本地預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="f4a04-150">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f4a04-151">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f4a04-151">-ServerName</span></span>
<span data-ttu-id="f4a04-152">指定源資料庫所在的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="f4a04-152">Specifies the name of the server on which the source database resides.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4a04-153">-確認</span><span class="sxs-lookup"><span data-stu-id="f4a04-153">-Confirm</span></span>
<span data-ttu-id="f4a04-154">執行 Cmdlet 之前，系統會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f4a04-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4a04-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4a04-155">-WhatIf</span></span>
<span data-ttu-id="f4a04-156">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f4a04-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4a04-157">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f4a04-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4a04-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4a04-158">CommonParameters</span></span>
<span data-ttu-id="f4a04-159">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f4a04-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4a04-160">詳細資訊請參閱 https://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="f4a04-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4a04-161">輸入</span><span class="sxs-lookup"><span data-stu-id="f4a04-161">INPUTS</span></span>

### <span data-ttu-id="f4a04-162">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="f4a04-162">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

### <span data-ttu-id="f4a04-163">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span><span class="sxs-lookup"><span data-stu-id="f4a04-163">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="f4a04-164">輸出</span><span class="sxs-lookup"><span data-stu-id="f4a04-164">OUTPUTS</span></span>

### <span data-ttu-id="f4a04-165">沒有</span><span class="sxs-lookup"><span data-stu-id="f4a04-165">None</span></span>

## <span data-ttu-id="f4a04-166">筆記</span><span class="sxs-lookup"><span data-stu-id="f4a04-166">NOTES</span></span>
* <span data-ttu-id="f4a04-167">驗證：此 Cmdlet 需要憑證式驗證。</span><span class="sxs-lookup"><span data-stu-id="f4a04-167">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="f4a04-168">有關如何使用憑證式驗證來設定目前訂閱的範例，請參閱 **New-AzureSqlDatabaseServerCoNtext** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f4a04-168">For an example of how to use certificate-based authentication to set the current subscription, see the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span>
* <span data-ttu-id="f4a04-169">限制：在主託管次要資料庫的伺服器上，僅支援強制終止。</span><span class="sxs-lookup"><span data-stu-id="f4a04-169">Restrictions: On the server that hosts the secondary database, only forced termination is supported.</span></span>
* <span data-ttu-id="f4a04-170">終止對前次要資料庫的影響：終止後，次要資料庫會變成獨立資料庫。</span><span class="sxs-lookup"><span data-stu-id="f4a04-170">Impact of termination on the former secondary database: After termination, the secondary database becomes an independent database.</span></span> <span data-ttu-id="f4a04-171">如果次要資料庫的樹種已完成，則終止之後，此資料庫會開啟以完全存取。</span><span class="sxs-lookup"><span data-stu-id="f4a04-171">If seeding already completed on the secondary database, after termination this database is open for full access.</span></span> <span data-ttu-id="f4a04-172">如果源資料庫是讀寫資料庫，則前次要資料庫也會變成讀寫資料庫。</span><span class="sxs-lookup"><span data-stu-id="f4a04-172">If the source database is a read-write database, the former secondary database becomes a read-write database, too.</span></span>

  <span data-ttu-id="f4a04-173">如果目前進行中種樹，就會中止播下，而託管次要資料庫的伺服器上永遠不會顯示前次要資料庫。</span><span class="sxs-lookup"><span data-stu-id="f4a04-173">If seeding is currently in progress, seeding is aborted, and the former secondary database never becomes visible on the server that hosts the secondary database.</span></span>

* <span data-ttu-id="f4a04-174">您可以將源資料庫設定為唯讀模式。</span><span class="sxs-lookup"><span data-stu-id="f4a04-174">You can set the source database to read-only mode.</span></span> <span data-ttu-id="f4a04-175">這可確保來源資料庫和次要資料庫在終止後同步處理，並確保在終止期間不會提交任何交易。</span><span class="sxs-lookup"><span data-stu-id="f4a04-175">This guarantees that source and secondary databases are synchronized after termination, and makes sure that no transactions are committed during termination.</span></span> <span data-ttu-id="f4a04-176">終止完成後，將來源設定回讀寫模式。</span><span class="sxs-lookup"><span data-stu-id="f4a04-176">Once the termination finishes, set the source back to read-write mode.</span></span> <span data-ttu-id="f4a04-177">或者，您也可以將前次要資料庫設為讀寫模式。</span><span class="sxs-lookup"><span data-stu-id="f4a04-177">Optionally, you can also set the former secondary database to read-write mode.</span></span>
* <span data-ttu-id="f4a04-178">監控：若要驗證連續複製關係的來源和目標作業狀態，請使用 **Get-AzureSqlDatabaseOperation** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f4a04-178">Monitoring: To verify the status of the operations at both the source and target of the continuous copy relationship, use the **Get-AzureSqlDatabaseOperation** cmdlet.</span></span>

## <span data-ttu-id="f4a04-179">相關連結</span><span class="sxs-lookup"><span data-stu-id="f4a04-179">RELATED LINKS</span></span>

[<span data-ttu-id="f4a04-180">Azure SQL 資料庫</span><span class="sxs-lookup"><span data-stu-id="f4a04-180">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="f4a04-181">Azure SQL 資料庫的作業</span><span class="sxs-lookup"><span data-stu-id="f4a04-181">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="f4a04-182">停止資料庫複製</span><span class="sxs-lookup"><span data-stu-id="f4a04-182">Stop Database Copy</span></span>](https://msdn.microsoft.com/en-us/library/dn509573.aspx)



[<span data-ttu-id="f4a04-183">Get-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="f4a04-183">Get-AzureSqlDatabaseCopy</span></span>](./Get-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="f4a04-184">Start-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="f4a04-184">Start-AzureSqlDatabaseCopy</span></span>](./Start-AzureSqlDatabaseCopy.md)


