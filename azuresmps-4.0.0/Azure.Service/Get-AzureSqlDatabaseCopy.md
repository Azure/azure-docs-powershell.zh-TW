---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5AEF7D44-624D-4794-86FF-156E6729BB56
online version: ''
schema: 2.0.0
ms.openlocfilehash: 95e276bf6af11698a4b3b82077175ec2ede2d7dc
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402417"
---
# <span data-ttu-id="cccd2-101">Get-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="cccd2-101">Get-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="cccd2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cccd2-102">SYNOPSIS</span></span>
<span data-ttu-id="cccd2-103">檢查複製關係的狀態。</span><span class="sxs-lookup"><span data-stu-id="cccd2-103">Checks the status of copy relationships.</span></span>

## <span data-ttu-id="cccd2-104">語法</span><span class="sxs-lookup"><span data-stu-id="cccd2-104">SYNTAX</span></span>

### <span data-ttu-id="cccd2-105">ByServerNameOnly (預設) </span><span class="sxs-lookup"><span data-stu-id="cccd2-105">ByServerNameOnly (Default)</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> [-DatabaseName <String>] [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="cccd2-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="cccd2-106">ByInputObject</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="cccd2-107">ByDatabase</span><span class="sxs-lookup"><span data-stu-id="cccd2-107">ByDatabase</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="cccd2-108">描述</span><span class="sxs-lookup"><span data-stu-id="cccd2-108">DESCRIPTION</span></span>
<span data-ttu-id="cccd2-109">**Get-AzureSqlDatabaseCopy** Cmdlet 會檢查一或多個使用中複製關係的狀態。</span><span class="sxs-lookup"><span data-stu-id="cccd2-109">The **Get-AzureSqlDatabaseCopy** cmdlet checks the status of one or more active copy relationships.</span></span>
<span data-ttu-id="cccd2-110">執行此 Cmdlet 之後，Start-AzureSqlDatabaseCopy或Stop-AzureSqlDatabaseCopy Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cccd2-110">Run this cmdlet after you run the Start-AzureSqlDatabaseCopy or Stop-AzureSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="cccd2-111">您可以檢查特定的複本關係、所有複製關係或篩選的複製關係清單，例如特定目標伺服器上的所有複本。</span><span class="sxs-lookup"><span data-stu-id="cccd2-111">You can check a specific copy relationship, all copy relationships, or a filtered list of copy relationships, such as all copies on a specific target server.</span></span>
<span data-ttu-id="cccd2-112">您可以在主管來源或目標資料庫的伺服器上執行此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cccd2-112">You can run this cmdlet on the server that hosts the source or target database.</span></span>

<span data-ttu-id="cccd2-113">此 Cmdlet 是同步的。</span><span class="sxs-lookup"><span data-stu-id="cccd2-113">This cmdlet is synchronous.</span></span>
<span data-ttu-id="cccd2-114">Cmdlet 會區塊 Azure PowerShell 主控台，直到它返回狀態物件。</span><span class="sxs-lookup"><span data-stu-id="cccd2-114">The cmdlet blocks the Azure PowerShell console until it returns a status object.</span></span>

<span data-ttu-id="cccd2-115">*PartnerServer 和* *PartnerDatabase* 參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="cccd2-115">The *PartnerServer* and *PartnerDatabase* parameters are optional.</span></span>
<span data-ttu-id="cccd2-116">如果您未指定任一參數，此 Cmdlet 會返回結果表。</span><span class="sxs-lookup"><span data-stu-id="cccd2-116">If you do not specify either parameter, this cmdlet returns a table of results.</span></span>
<span data-ttu-id="cccd2-117">若要只查看特定資料庫的狀態，請指定這兩個參數。</span><span class="sxs-lookup"><span data-stu-id="cccd2-117">To see the status for only a particular database, specify both parameters.</span></span>

## <span data-ttu-id="cccd2-118">例子</span><span class="sxs-lookup"><span data-stu-id="cccd2-118">EXAMPLES</span></span>

### <span data-ttu-id="cccd2-119">範例 1：取得資料庫的複製狀態</span><span class="sxs-lookup"><span data-stu-id="cccd2-119">Example 1: Get the copy status of a database</span></span>
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

<span data-ttu-id="cccd2-120">此命令會在伺服器上獲得名為 lpqd0zbr8y 的 Orders 資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="cccd2-120">This command gets the status of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="cccd2-121">*PartnerServer* 參數將此命令限制為 bk0b8kf658 伺服器。</span><span class="sxs-lookup"><span data-stu-id="cccd2-121">The *PartnerServer* parameter restricts this command to the bk0b8kf658 server.</span></span>

### <span data-ttu-id="cccd2-122">範例 2：取得伺服器上所有複本的狀態取得伺服器上所有複本的狀態</span><span class="sxs-lookup"><span data-stu-id="cccd2-122">Example 2: Get the status of all copies on a serverGet the status of all copies on a server</span></span>
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="cccd2-123">此命令會在伺服器上獲得所有使用中複本的狀態，名稱為 lpqd0zbr8y。</span><span class="sxs-lookup"><span data-stu-id="cccd2-123">This command gets the status of all active copies on the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="cccd2-124">參數</span><span class="sxs-lookup"><span data-stu-id="cccd2-124">PARAMETERS</span></span>

### <span data-ttu-id="cccd2-125">-資料庫</span><span class="sxs-lookup"><span data-stu-id="cccd2-125">-Database</span></span>
<span data-ttu-id="cccd2-126">指定代表來源 Azure SQL Database 的物件。</span><span class="sxs-lookup"><span data-stu-id="cccd2-126">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="cccd2-127">此 Cmdlet 會獲得此參數指定之資料庫的複製狀態。</span><span class="sxs-lookup"><span data-stu-id="cccd2-127">This cmdlet gets the copy status of the database that this parameter specifies.</span></span>

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

### <span data-ttu-id="cccd2-128">-DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="cccd2-128">-DatabaseCopy</span></span>
<span data-ttu-id="cccd2-129">指定代表資料庫的物件。</span><span class="sxs-lookup"><span data-stu-id="cccd2-129">Specifies an object that represents a database.</span></span>
<span data-ttu-id="cccd2-130">此 Cmdlet 會獲得此參數指定之資料庫的複製狀態。</span><span class="sxs-lookup"><span data-stu-id="cccd2-130">This cmdlet gets the copy status of the database that this parameter specifies.</span></span>
<span data-ttu-id="cccd2-131">此參數接受管線輸入。</span><span class="sxs-lookup"><span data-stu-id="cccd2-131">This parameter accepts pipeline input.</span></span>

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

### <span data-ttu-id="cccd2-132">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cccd2-132">-DatabaseName</span></span>
<span data-ttu-id="cccd2-133">指定源資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="cccd2-133">Specifies the name of the source database.</span></span>
<span data-ttu-id="cccd2-134">此 Cmdlet 會獲得此參數指定之資料庫的複製狀態。</span><span class="sxs-lookup"><span data-stu-id="cccd2-134">This cmdlet gets that copy status of the database that this parameter specifies.</span></span>

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

### <span data-ttu-id="cccd2-135">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="cccd2-135">-PartnerDatabase</span></span>
<span data-ttu-id="cccd2-136">指定次要資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="cccd2-136">Specifies name of the secondary database.</span></span>
<span data-ttu-id="cccd2-137">如果在動態管理sys.dm_database_copies找不到此資料庫，此 Cmdlet 會返回空白的狀態物件。</span><span class="sxs-lookup"><span data-stu-id="cccd2-137">If this database is not found in the sys.dm_database_copies dynamic management view, this cmdlet returns an empty status object.</span></span>

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

### <span data-ttu-id="cccd2-138">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="cccd2-138">-PartnerServer</span></span>
<span data-ttu-id="cccd2-139">指定主託管目標資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="cccd2-139">Specifies the name of the server that hosts the target database.</span></span>
<span data-ttu-id="cccd2-140">如果在動態管理sys.dm_database_copies找不到此伺服器，此 Cmdlet 會返回空白的狀態物件。</span><span class="sxs-lookup"><span data-stu-id="cccd2-140">If this server is not found in the sys.dm_database_copies dynamic management view, this cmdlet returns an empty status object.</span></span>

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

### <span data-ttu-id="cccd2-141">-設定檔</span><span class="sxs-lookup"><span data-stu-id="cccd2-141">-Profile</span></span>
<span data-ttu-id="cccd2-142">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="cccd2-142">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cccd2-143">如果您未指定設定檔，此 Cmdlet 會從本地預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="cccd2-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cccd2-144">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cccd2-144">-ServerName</span></span>
<span data-ttu-id="cccd2-145">指定資料庫副本所在的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="cccd2-145">Specifies the name of the server on which the database copy resides.</span></span>

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

### <span data-ttu-id="cccd2-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cccd2-146">CommonParameters</span></span>
<span data-ttu-id="cccd2-147">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cccd2-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cccd2-148">詳細資訊請參閱 https://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="cccd2-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cccd2-149">輸入</span><span class="sxs-lookup"><span data-stu-id="cccd2-149">INPUTS</span></span>

### <span data-ttu-id="cccd2-150">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="cccd2-150">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

### <span data-ttu-id="cccd2-151">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span><span class="sxs-lookup"><span data-stu-id="cccd2-151">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="cccd2-152">輸出</span><span class="sxs-lookup"><span data-stu-id="cccd2-152">OUTPUTS</span></span>

### <span data-ttu-id="cccd2-153">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="cccd2-153">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

## <span data-ttu-id="cccd2-154">筆記</span><span class="sxs-lookup"><span data-stu-id="cccd2-154">NOTES</span></span>
* <span data-ttu-id="cccd2-155">驗證：此 Cmdlet 需要憑證式驗證。</span><span class="sxs-lookup"><span data-stu-id="cccd2-155">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="cccd2-156">有關如何使用憑證式驗證來設定目前訂閱的範例，請參閱 New-AzureSqlDatabaseServerContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cccd2-156">For an example of how to use certificate-based authentication to set the current subscription, see the New-AzureSqlDatabaseServerContext cmdlet.</span></span>

## <span data-ttu-id="cccd2-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="cccd2-157">RELATED LINKS</span></span>

[<span data-ttu-id="cccd2-158">Azure SQL 資料庫</span><span class="sxs-lookup"><span data-stu-id="cccd2-158">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="cccd2-159">Azure SQL 資料庫的作業</span><span class="sxs-lookup"><span data-stu-id="cccd2-159">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)



[<span data-ttu-id="cccd2-160">Start-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="cccd2-160">Start-AzureSqlDatabaseCopy</span></span>](./Start-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="cccd2-161">Stop-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="cccd2-161">Stop-AzureSqlDatabaseCopy</span></span>](./Stop-AzureSqlDatabaseCopy.md)


