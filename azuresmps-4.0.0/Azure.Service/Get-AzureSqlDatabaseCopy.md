---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5AEF7D44-624D-4794-86FF-156E6729BB56
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8752766572975ef97094a3915446086c903a7fd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967741"
---
# <span data-ttu-id="cacab-101">Get-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="cacab-101">Get-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="cacab-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cacab-102">SYNOPSIS</span></span>
<span data-ttu-id="cacab-103">檢查複製關聯的狀態。</span><span class="sxs-lookup"><span data-stu-id="cacab-103">Checks the status of copy relationships.</span></span>

## <span data-ttu-id="cacab-104">句法</span><span class="sxs-lookup"><span data-stu-id="cacab-104">SYNTAX</span></span>

### <span data-ttu-id="cacab-105">ByServerNameOnly (預設) </span><span class="sxs-lookup"><span data-stu-id="cacab-105">ByServerNameOnly (Default)</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> [-DatabaseName <String>] [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="cacab-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="cacab-106">ByInputObject</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="cacab-107">ByDatabase</span><span class="sxs-lookup"><span data-stu-id="cacab-107">ByDatabase</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="cacab-108">說明</span><span class="sxs-lookup"><span data-stu-id="cacab-108">DESCRIPTION</span></span>
<span data-ttu-id="cacab-109">**AzureSqlDatabaseCopy** Cmdlet 會檢查一或多個活動複本關聯的狀態。</span><span class="sxs-lookup"><span data-stu-id="cacab-109">The **Get-AzureSqlDatabaseCopy** cmdlet checks the status of one or more active copy relationships.</span></span>
<span data-ttu-id="cacab-110">在執行 Start-AzureSqlDatabaseCopy 或 Stop-AzureSqlDatabaseCopy Cmdlet 之後，請執行這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cacab-110">Run this cmdlet after you run the Start-AzureSqlDatabaseCopy or Stop-AzureSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="cacab-111">您可以檢查特定的複本關聯性、所有複製關聯，或是複製關聯的篩選清單，例如特定目標伺服器上的所有複本。</span><span class="sxs-lookup"><span data-stu-id="cacab-111">You can check a specific copy relationship, all copy relationships, or a filtered list of copy relationships, such as all copies on a specific target server.</span></span>
<span data-ttu-id="cacab-112">您可以在裝載來源或目標資料庫的伺服器上執行這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cacab-112">You can run this cmdlet on the server that hosts the source or target database.</span></span>

<span data-ttu-id="cacab-113">這個 Cmdlet 是同步的。</span><span class="sxs-lookup"><span data-stu-id="cacab-113">This cmdlet is synchronous.</span></span>
<span data-ttu-id="cacab-114">這個 Cmdlet 會封鎖 Azure PowerShell 主控台，直到它傳回 status 物件為止。</span><span class="sxs-lookup"><span data-stu-id="cacab-114">The cmdlet blocks the Azure PowerShell console until it returns a status object.</span></span>

<span data-ttu-id="cacab-115">*PartnerServer* 和 *PartnerDatabase* 參數是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="cacab-115">The *PartnerServer* and *PartnerDatabase* parameters are optional.</span></span>
<span data-ttu-id="cacab-116">如果您沒有指定任何一個參數，這個 Cmdlet 會傳回結果表格。</span><span class="sxs-lookup"><span data-stu-id="cacab-116">If you do not specify either parameter, this cmdlet returns a table of results.</span></span>
<span data-ttu-id="cacab-117">若只要查看特定資料庫的狀態，請同時指定這兩個參數。</span><span class="sxs-lookup"><span data-stu-id="cacab-117">To see the status for only a particular database, specify both parameters.</span></span>

## <span data-ttu-id="cacab-118">示例</span><span class="sxs-lookup"><span data-stu-id="cacab-118">EXAMPLES</span></span>

### <span data-ttu-id="cacab-119">範例1：取得資料庫的複製狀態</span><span class="sxs-lookup"><span data-stu-id="cacab-119">Example 1: Get the copy status of a database</span></span>
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

<span data-ttu-id="cacab-120">這個命令會在名為 lpqd0zbr8y 的伺服器上，取得名為 [訂單] 的資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="cacab-120">This command gets the status of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="cacab-121">*PartnerServer* 參數會將這個命令限制在 bk0b8kf658 伺服器。</span><span class="sxs-lookup"><span data-stu-id="cacab-121">The *PartnerServer* parameter restricts this command to the bk0b8kf658 server.</span></span>

### <span data-ttu-id="cacab-122">範例2：取得伺服器上所有複本的狀態 serverGet 伺服器上所有複本的狀態</span><span class="sxs-lookup"><span data-stu-id="cacab-122">Example 2: Get the status of all copies on a serverGet the status of all copies on a server</span></span>
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="cacab-123">這個命令會取得伺服器上名為 lpqd0zbr8y 的所有活動複本狀態。</span><span class="sxs-lookup"><span data-stu-id="cacab-123">This command gets the status of all active copies on the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="cacab-124">參數</span><span class="sxs-lookup"><span data-stu-id="cacab-124">PARAMETERS</span></span>

### <span data-ttu-id="cacab-125">-資料庫</span><span class="sxs-lookup"><span data-stu-id="cacab-125">-Database</span></span>
<span data-ttu-id="cacab-126">指定代表來源 Azure SQL 資料庫的物件。</span><span class="sxs-lookup"><span data-stu-id="cacab-126">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="cacab-127">這個 Cmdlet 會取得此參數指定之資料庫的複製狀態。</span><span class="sxs-lookup"><span data-stu-id="cacab-127">This cmdlet gets the copy status of the database that this parameter specifies.</span></span>

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

### <span data-ttu-id="cacab-128">-DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="cacab-128">-DatabaseCopy</span></span>
<span data-ttu-id="cacab-129">指定代表資料庫的物件。</span><span class="sxs-lookup"><span data-stu-id="cacab-129">Specifies an object that represents a database.</span></span>
<span data-ttu-id="cacab-130">這個 Cmdlet 會取得此參數指定之資料庫的複製狀態。</span><span class="sxs-lookup"><span data-stu-id="cacab-130">This cmdlet gets the copy status of the database that this parameter specifies.</span></span>
<span data-ttu-id="cacab-131">這個參數接受管線輸入。</span><span class="sxs-lookup"><span data-stu-id="cacab-131">This parameter accepts pipeline input.</span></span>

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

### <span data-ttu-id="cacab-132">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cacab-132">-DatabaseName</span></span>
<span data-ttu-id="cacab-133">指定源資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="cacab-133">Specifies the name of the source database.</span></span>
<span data-ttu-id="cacab-134">這個 Cmdlet 會取得此參數指定之資料庫的複製狀態。</span><span class="sxs-lookup"><span data-stu-id="cacab-134">This cmdlet gets that copy status of the database that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameOnly
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cacab-135">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="cacab-135">-PartnerDatabase</span></span>
<span data-ttu-id="cacab-136">指定次要資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="cacab-136">Specifies name of the secondary database.</span></span>
<span data-ttu-id="cacab-137">如果在 sys.dm_database_copies 動態管理檢視中找不到這個資料庫，這個 Cmdlet 會傳回一個空的狀態物件。</span><span class="sxs-lookup"><span data-stu-id="cacab-137">If this database is not found in the sys.dm_database_copies dynamic management view, this cmdlet returns an empty status object.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameOnly, ByDatabase
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cacab-138">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="cacab-138">-PartnerServer</span></span>
<span data-ttu-id="cacab-139">指定主持目標資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="cacab-139">Specifies the name of the server that hosts the target database.</span></span>
<span data-ttu-id="cacab-140">如果在 sys.dm_database_copies 動態管理檢視中找不到這個伺服器，這個 Cmdlet 會傳回一個空的狀態物件。</span><span class="sxs-lookup"><span data-stu-id="cacab-140">If this server is not found in the sys.dm_database_copies dynamic management view, this cmdlet returns an empty status object.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameOnly, ByDatabase
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cacab-141">-設定檔</span><span class="sxs-lookup"><span data-stu-id="cacab-141">-Profile</span></span>
<span data-ttu-id="cacab-142">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="cacab-142">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cacab-143">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="cacab-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cacab-144">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cacab-144">-ServerName</span></span>
<span data-ttu-id="cacab-145">指定資料庫複本所在之伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="cacab-145">Specifies the name of the server on which the database copy resides.</span></span>

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

### <span data-ttu-id="cacab-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cacab-146">CommonParameters</span></span>
<span data-ttu-id="cacab-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cacab-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cacab-148">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cacab-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cacab-149">輸入</span><span class="sxs-lookup"><span data-stu-id="cacab-149">INPUTS</span></span>

### <span data-ttu-id="cacab-150">WindowsAzure. SqlDatabase. DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="cacab-150">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

### <span data-ttu-id="cacab-151">SqlDatabase.. Database （WindowsAzure）</span><span class="sxs-lookup"><span data-stu-id="cacab-151">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="cacab-152">輸出</span><span class="sxs-lookup"><span data-stu-id="cacab-152">OUTPUTS</span></span>

### <span data-ttu-id="cacab-153">WindowsAzure. SqlDatabase. DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="cacab-153">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

## <span data-ttu-id="cacab-154">筆記</span><span class="sxs-lookup"><span data-stu-id="cacab-154">NOTES</span></span>
* <span data-ttu-id="cacab-155">驗證：此 Cmdlet 需要以憑證為基礎的驗證。</span><span class="sxs-lookup"><span data-stu-id="cacab-155">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="cacab-156">如需如何使用以憑證為基礎的驗證來設定目前訂閱的範例，請參閱 New-AzureSqlDatabaseServerContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cacab-156">For an example of how to use certificate-based authentication to set the current subscription, see the New-AzureSqlDatabaseServerContext cmdlet.</span></span>

## <span data-ttu-id="cacab-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="cacab-157">RELATED LINKS</span></span>

[<span data-ttu-id="cacab-158">Azure SQL 資料庫</span><span class="sxs-lookup"><span data-stu-id="cacab-158">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="cacab-159">Azure SQL 資料庫的作業</span><span class="sxs-lookup"><span data-stu-id="cacab-159">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="cacab-160">Azure SQL 資料庫 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cacab-160">Azure SQL Database Cmdlets</span></span>](./Azure.SQLDatabase.md)

[<span data-ttu-id="cacab-161">開始-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="cacab-161">Start-AzureSqlDatabaseCopy</span></span>](./Start-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="cacab-162">停止 AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="cacab-162">Stop-AzureSqlDatabaseCopy</span></span>](./Stop-AzureSqlDatabaseCopy.md)


