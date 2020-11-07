---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: CB601E21-424D-4B09-85E5-A4B2A5068267
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2b7674cb5b7abc489dc6aa6d3746f499b9686312
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967849"
---
# <span data-ttu-id="cb548-101">Stop-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="cb548-101">Stop-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="cb548-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cb548-102">SYNOPSIS</span></span>
<span data-ttu-id="cb548-103">終止連續複製關聯。</span><span class="sxs-lookup"><span data-stu-id="cb548-103">Terminates a continuous copy relationship.</span></span>

## <span data-ttu-id="cb548-104">句法</span><span class="sxs-lookup"><span data-stu-id="cb548-104">SYNTAX</span></span>

### <span data-ttu-id="cb548-105">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="cb548-105">ByInputObject</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-ForcedTermination] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb548-106">ByDatabase</span><span class="sxs-lookup"><span data-stu-id="cb548-106">ByDatabase</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cb548-107">ByDatabaseName</span><span class="sxs-lookup"><span data-stu-id="cb548-107">ByDatabaseName</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cb548-108">說明</span><span class="sxs-lookup"><span data-stu-id="cb548-108">DESCRIPTION</span></span>
<span data-ttu-id="cb548-109">**AzureSqlDatabaseCopy** Cmdlet 會終止連續複製關聯。</span><span class="sxs-lookup"><span data-stu-id="cb548-109">The **Stop-AzureSqlDatabaseCopy** cmdlet terminates a continuous copy relationship.</span></span>
<span data-ttu-id="cb548-110">這個 Cmdlet 會停止源資料庫與次要或目標資料庫之間的資料移動，然後將次要資料庫的狀態變更為獨立的線上資料庫。</span><span class="sxs-lookup"><span data-stu-id="cb548-110">This cmdlet stops the data movement between the source database and secondary or target database, and then changes the state of the secondary database to be a stand-alone online database.</span></span>

<span data-ttu-id="cb548-111">您可以透過兩種方式來結束連續複製關聯、終止或計畫終止及強制終止（可能會造成資料遺失）。</span><span class="sxs-lookup"><span data-stu-id="cb548-111">There are two ways to end a continuous copy relationship, termination or planned termination and forced termination with possible data loss.</span></span>
<span data-ttu-id="cb548-112">在託管來源資料庫的伺服器上，您可以在終止或強制終止模式下執行此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cb548-112">On the server that hosts the source database, you can run this cmdlet in termination or forced termination mode.</span></span>
<span data-ttu-id="cb548-113">在裝載次要資料庫的伺服器上，您必須使用強制終止模式。</span><span class="sxs-lookup"><span data-stu-id="cb548-113">On the server that hosts the secondary database, you must use forced termination mode.</span></span>

<span data-ttu-id="cb548-114">已計畫的終止會等到源資料庫上的所有已提交事務（在您執行 Cmdlet 時）已複製到次要資料庫為止。</span><span class="sxs-lookup"><span data-stu-id="cb548-114">A planned termination waits until all committed transactions on the source database, at the time that you run the cmdlet, have been replicated to the secondary database.</span></span>
<span data-ttu-id="cb548-115">強制終止並不會等待複製任何未完成的已提交事務，而且可能會在次要資料庫中造成可能的資料遺失。</span><span class="sxs-lookup"><span data-stu-id="cb548-115">Forced termination does not wait for replication of any outstanding committed transactions, and can cause possible data loss in the secondary database.</span></span>

<span data-ttu-id="cb548-116">當複製狀態為 [擱置中] 時，只有強制終止才能成功結束連續複製關聯。</span><span class="sxs-lookup"><span data-stu-id="cb548-116">While replication status is PENDING, only forced termination can successfully end a continuous copy relationship.</span></span>
<span data-ttu-id="cb548-117">如果複製狀態為 [擱置中]，則不支援不強制的終止。</span><span class="sxs-lookup"><span data-stu-id="cb548-117">If the replication status is PENDING, termination that is not forced is not supported.</span></span>

## <span data-ttu-id="cb548-118">示例</span><span class="sxs-lookup"><span data-stu-id="cb548-118">EXAMPLES</span></span>

### <span data-ttu-id="cb548-119">範例1：終止連續複製關聯</span><span class="sxs-lookup"><span data-stu-id="cb548-119">Example 1: Terminate a continuous copy relationship</span></span>
```
PS C:\>Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

<span data-ttu-id="cb548-120">這個命令會在名為 lpqd0zbr8y 的伺服器上，終止名為 [訂單] 的資料庫連續複製關聯。</span><span class="sxs-lookup"><span data-stu-id="cb548-120">This command terminates the continuous copy relationship of database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="cb548-121">名為 bk0b8kf658 的伺服器會託管次要資料庫。</span><span class="sxs-lookup"><span data-stu-id="cb548-121">The server named bk0b8kf658 hosts the secondary database.</span></span>

### <span data-ttu-id="cb548-122">範例2：強行終止連續複製關聯</span><span class="sxs-lookup"><span data-stu-id="cb548-122">Example 2: Forcibly terminate a continuous copy relationship</span></span>
```
PS C:\>$DatabaseCopy = Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders"
PS C:\> $DatabaseCopy | Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -ForcedTermination
```

<span data-ttu-id="cb548-123">第一個命令會取得名為 lpqd0zbr8y 的伺服器上名為 [訂單] 的資料庫複製關係。</span><span class="sxs-lookup"><span data-stu-id="cb548-123">The first command gets the database copy relationship for the database named Orders on the server named lpqd0zbr8y.</span></span>

<span data-ttu-id="cb548-124">第二個命令會強制終止託管次要資料庫之伺服器的連續複製關聯。</span><span class="sxs-lookup"><span data-stu-id="cb548-124">The second command forcibly terminates a continuous copy relationship from the server that hosts the secondary database.</span></span>

## <span data-ttu-id="cb548-125">參數</span><span class="sxs-lookup"><span data-stu-id="cb548-125">PARAMETERS</span></span>

### <span data-ttu-id="cb548-126">-資料庫</span><span class="sxs-lookup"><span data-stu-id="cb548-126">-Database</span></span>
<span data-ttu-id="cb548-127">指定代表來源 Azure SQL 資料庫的物件。</span><span class="sxs-lookup"><span data-stu-id="cb548-127">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="cb548-128">這個 Cmdlet 會終止此參數指定之資料庫的連續複製關聯。</span><span class="sxs-lookup"><span data-stu-id="cb548-128">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>

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

### <span data-ttu-id="cb548-129">-DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="cb548-129">-DatabaseCopy</span></span>
<span data-ttu-id="cb548-130">指定代表資料庫的物件。</span><span class="sxs-lookup"><span data-stu-id="cb548-130">Specifies an object that represents a database.</span></span>
<span data-ttu-id="cb548-131">這個 Cmdlet 會終止此參數指定之資料庫的連續複製關聯。</span><span class="sxs-lookup"><span data-stu-id="cb548-131">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>
<span data-ttu-id="cb548-132">這個參數接受管線輸入。</span><span class="sxs-lookup"><span data-stu-id="cb548-132">This parameter accepts pipeline input.</span></span>

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

### <span data-ttu-id="cb548-133">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cb548-133">-DatabaseName</span></span>
<span data-ttu-id="cb548-134">指定資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb548-134">Specifies the name of a database.</span></span>
<span data-ttu-id="cb548-135">這個 Cmdlet 會終止此參數指定之資料庫的連續複製關聯。</span><span class="sxs-lookup"><span data-stu-id="cb548-135">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>

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

### <span data-ttu-id="cb548-136">-Force</span><span class="sxs-lookup"><span data-stu-id="cb548-136">-Force</span></span>
<span data-ttu-id="cb548-137">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="cb548-137">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cb548-138">-ForcedTermination</span><span class="sxs-lookup"><span data-stu-id="cb548-138">-ForcedTermination</span></span>
<span data-ttu-id="cb548-139">表示此 Cmdlet 會導致連續複製關聯的強制終止。</span><span class="sxs-lookup"><span data-stu-id="cb548-139">Indicates that this cmdlet causes forced termination of the continuous copy relationship.</span></span>
<span data-ttu-id="cb548-140">強制終止可能會造成資料遺失。</span><span class="sxs-lookup"><span data-stu-id="cb548-140">Forced termination may cause with data loss.</span></span>
<span data-ttu-id="cb548-141">若要在託管目標資料庫的伺服器上執行此 Cmdlet，您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="cb548-141">To run this cmdlet on a server that hosts the target database, you must specify this parameter.</span></span>
<span data-ttu-id="cb548-142">若要在託管來源資料庫的伺服器上執行這個 Cmdlet，如果次要資料庫無法使用，您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="cb548-142">To run this cmdlet on a server that hosts the source database, if the secondary database is unavailable, you must specify this parameter.</span></span>

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

### <span data-ttu-id="cb548-143">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="cb548-143">-PartnerDatabase</span></span>
<span data-ttu-id="cb548-144">指定次要資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb548-144">Specifies name of the secondary database.</span></span>
<span data-ttu-id="cb548-145">如果您指定名稱，則它必須符合源資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb548-145">If you specify a name, it must match the name of the source database.</span></span>

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

### <span data-ttu-id="cb548-146">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="cb548-146">-PartnerServer</span></span>
<span data-ttu-id="cb548-147">指定主持目標資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="cb548-147">Specifies the name of the server that hosts the target database.</span></span>

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

### <span data-ttu-id="cb548-148">-設定檔</span><span class="sxs-lookup"><span data-stu-id="cb548-148">-Profile</span></span>
<span data-ttu-id="cb548-149">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="cb548-149">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cb548-150">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="cb548-150">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cb548-151">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cb548-151">-ServerName</span></span>
<span data-ttu-id="cb548-152">指定源資料庫所在之伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb548-152">Specifies the name of the server on which the source database resides.</span></span>

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

### <span data-ttu-id="cb548-153">-確認</span><span class="sxs-lookup"><span data-stu-id="cb548-153">-Confirm</span></span>
<span data-ttu-id="cb548-154">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cb548-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb548-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb548-155">-WhatIf</span></span>
<span data-ttu-id="cb548-156">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cb548-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb548-157">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cb548-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb548-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb548-158">CommonParameters</span></span>
<span data-ttu-id="cb548-159">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cb548-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb548-160">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cb548-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb548-161">輸入</span><span class="sxs-lookup"><span data-stu-id="cb548-161">INPUTS</span></span>

### <span data-ttu-id="cb548-162">WindowsAzure. SqlDatabase. DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="cb548-162">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

### <span data-ttu-id="cb548-163">SqlDatabase.. Database （WindowsAzure）</span><span class="sxs-lookup"><span data-stu-id="cb548-163">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="cb548-164">輸出</span><span class="sxs-lookup"><span data-stu-id="cb548-164">OUTPUTS</span></span>

### <span data-ttu-id="cb548-165">所有</span><span class="sxs-lookup"><span data-stu-id="cb548-165">None</span></span>

## <span data-ttu-id="cb548-166">筆記</span><span class="sxs-lookup"><span data-stu-id="cb548-166">NOTES</span></span>
* <span data-ttu-id="cb548-167">驗證：此 Cmdlet 需要以憑證為基礎的驗證。</span><span class="sxs-lookup"><span data-stu-id="cb548-167">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="cb548-168">如需如何使用憑證式驗證來設定目前訂閱的範例，請參閱 **AzureSqlDatabaseServerCoNtext** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cb548-168">For an example of how to use certificate-based authentication to set the current subscription, see the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span>
* <span data-ttu-id="cb548-169">限制：在託管次要資料庫的伺服器上，只支援強制終止。</span><span class="sxs-lookup"><span data-stu-id="cb548-169">Restrictions: On the server that hosts the secondary database, only forced termination is supported.</span></span>
* <span data-ttu-id="cb548-170">在前一個次要資料庫上終止的影響：終止之後，次要資料庫成為獨立的資料庫。</span><span class="sxs-lookup"><span data-stu-id="cb548-170">Impact of termination on the former secondary database: After termination, the secondary database becomes an independent database.</span></span> <span data-ttu-id="cb548-171">如果在次要資料庫上已完成播種，則在終止之後，就會開啟此資料庫以供完全存取。</span><span class="sxs-lookup"><span data-stu-id="cb548-171">If seeding already completed on the secondary database, after termination this database is open for full access.</span></span> <span data-ttu-id="cb548-172">如果來源資料庫是讀寫資料庫，則前者的次要資料庫也會成為讀寫資料庫。</span><span class="sxs-lookup"><span data-stu-id="cb548-172">If the source database is a read-write database, the former secondary database becomes a read-write database, too.</span></span>

  <span data-ttu-id="cb548-173">如果正在進行衍生作業，則會中止播種，而前者在託管次要資料庫的伺服器上永遠不會顯示。</span><span class="sxs-lookup"><span data-stu-id="cb548-173">If seeding is currently in progress, seeding is aborted, and the former secondary database never becomes visible on the server that hosts the secondary database.</span></span>

* <span data-ttu-id="cb548-174">您可以將源資料庫設為唯讀模式。</span><span class="sxs-lookup"><span data-stu-id="cb548-174">You can set the source database to read-only mode.</span></span> <span data-ttu-id="cb548-175">這可保證在終止後，來源和次要資料庫已同步處理，並確保終止期間不會提交任何事務。</span><span class="sxs-lookup"><span data-stu-id="cb548-175">This guarantees that source and secondary databases are synchronized after termination, and makes sure that no transactions are committed during termination.</span></span> <span data-ttu-id="cb548-176">終止結束後，請將來源設回到讀寫模式。</span><span class="sxs-lookup"><span data-stu-id="cb548-176">Once the termination finishes, set the source back to read-write mode.</span></span> <span data-ttu-id="cb548-177">或者，您也可以將先前的次要資料庫設定為讀寫模式。</span><span class="sxs-lookup"><span data-stu-id="cb548-177">Optionally, you can also set the former secondary database to read-write mode.</span></span>
* <span data-ttu-id="cb548-178">監視：若要確認連續複製關聯之來源和目標上的作業狀態，請使用 **AzureSqlDatabaseOperation** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cb548-178">Monitoring: To verify the status of the operations at both the source and target of the continuous copy relationship, use the **Get-AzureSqlDatabaseOperation** cmdlet.</span></span>

## <span data-ttu-id="cb548-179">相關連結</span><span class="sxs-lookup"><span data-stu-id="cb548-179">RELATED LINKS</span></span>

[<span data-ttu-id="cb548-180">Azure SQL 資料庫</span><span class="sxs-lookup"><span data-stu-id="cb548-180">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="cb548-181">Azure SQL 資料庫的作業</span><span class="sxs-lookup"><span data-stu-id="cb548-181">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="cb548-182">停止資料庫複製</span><span class="sxs-lookup"><span data-stu-id="cb548-182">Stop Database Copy</span></span>](https://msdn.microsoft.com/en-us/library/dn509573.aspx)

[<span data-ttu-id="cb548-183">Azure SQL 資料庫 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb548-183">Azure SQL Database Cmdlets</span></span>](./Azure.SQLDatabase.md)

[<span data-ttu-id="cb548-184">AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="cb548-184">Get-AzureSqlDatabaseCopy</span></span>](./Get-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="cb548-185">開始-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="cb548-185">Start-AzureSqlDatabaseCopy</span></span>](./Start-AzureSqlDatabaseCopy.md)


