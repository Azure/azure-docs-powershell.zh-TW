---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 56026A74-A6DC-47A5-9643-5828C3D0E83B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 32219154f2036ee028b05a369c46be1d8e1def87
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967739"
---
# <span data-ttu-id="e0108-101">Get-AzureSqlDatabaseOperation</span><span class="sxs-lookup"><span data-stu-id="e0108-101">Get-AzureSqlDatabaseOperation</span></span>

## <span data-ttu-id="e0108-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e0108-102">SYNOPSIS</span></span>
<span data-ttu-id="e0108-103">取得 Azure 伺服器上資料庫作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="e0108-103">Gets the status of database operations on an Azure server.</span></span>

## <span data-ttu-id="e0108-104">句法</span><span class="sxs-lookup"><span data-stu-id="e0108-104">SYNTAX</span></span>

### <span data-ttu-id="e0108-105">ByConnectionCoNtext (預設) </span><span class="sxs-lookup"><span data-stu-id="e0108-105">ByConnectionContext (Default)</span></span>
```
Get-AzureSqlDatabaseOperation -ConnectionContext <IServerDataServiceContext> [-Database <Database>]
 [-DatabaseName <String>] [-OperationGuid <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e0108-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="e0108-106">ByServerName</span></span>
```
Get-AzureSqlDatabaseOperation -ServerName <String> [-Database <Database>] [-DatabaseName <String>]
 [-OperationGuid <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e0108-107">說明</span><span class="sxs-lookup"><span data-stu-id="e0108-107">DESCRIPTION</span></span>
<span data-ttu-id="e0108-108">**AzureSqlDatabaseOperation** Cmdlet 會取得指定 Azure 伺服器上資料庫作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="e0108-108">The **Get-AzureSqlDatabaseOperation** cmdlet gets the status of database operations on the specified Azure server.</span></span>
<span data-ttu-id="e0108-109">如果您只指定 *ServerName* 或 *ConnectionCoNtext* 參數，則 Cmdlet 會取得伺服器的所有資料庫作業。</span><span class="sxs-lookup"><span data-stu-id="e0108-109">If you specify only the *ServerName* or *ConnectionContext* parameter, the cmdlet gets all the database operations for the server.</span></span>
<span data-ttu-id="e0108-110">如果您同時使用 *database* 或 *DatabaseName* 參數指定資料庫，此 Cmdlet 會取得指定資料庫的所有操作。</span><span class="sxs-lookup"><span data-stu-id="e0108-110">If you also specify a database by using the *Database* or *DatabaseName* parameter, this cmdlet gets all the operations for the specified database.</span></span>
<span data-ttu-id="e0108-111">如果您指定的是操作 GUID 以及 *ServerName* 或 *ConnectionCoNtext* ，則此 Cmdlet 會取得單一資料庫操作。</span><span class="sxs-lookup"><span data-stu-id="e0108-111">If you specify an operation GUID, and *ServerName* or *ConnectionContext* , the cmdlet gets a single database operation.</span></span>

## <span data-ttu-id="e0108-112">示例</span><span class="sxs-lookup"><span data-stu-id="e0108-112">EXAMPLES</span></span>

### <span data-ttu-id="e0108-113">範例1：取得資料庫所有資料庫作業的狀態</span><span class="sxs-lookup"><span data-stu-id="e0108-113">Example 1: Get the status of all database operations for a database</span></span>
```
PS C:\> $Operations = Get-AzureSqlDatabaseOperation -ConnectionContext $Context -DatabaseName "Database17"
```

<span data-ttu-id="e0108-114">這個命令會取得伺服器上名為 Database17 的所有資料庫作業的狀態，而該伺服器已在連接內容 $CoNtext 指定的資料庫上。</span><span class="sxs-lookup"><span data-stu-id="e0108-114">This command gets the status of all database operations on the database named Database17 on the server that the connection context $Context specifies.</span></span>

### <span data-ttu-id="e0108-115">範例2：取得伺服器所有資料庫作業的狀態</span><span class="sxs-lookup"><span data-stu-id="e0108-115">Example 2: Get the status of all database operations for a server</span></span>
```
PS C:\> $Operations = Get-AzureSqlDatabaseOperation -ConnectionContext $Context
```

<span data-ttu-id="e0108-116">這個命令會在伺服器上取得連接內容 $CoNtext 指定的所有資料庫作業狀態。</span><span class="sxs-lookup"><span data-stu-id="e0108-116">This command gets the status of all database operations on the server that the connection context $Context specifies.</span></span>

## <span data-ttu-id="e0108-117">參數</span><span class="sxs-lookup"><span data-stu-id="e0108-117">PARAMETERS</span></span>

### <span data-ttu-id="e0108-118">-ConnectionCoNtext</span><span class="sxs-lookup"><span data-stu-id="e0108-118">-ConnectionContext</span></span>
<span data-ttu-id="e0108-119">指定伺服器的連接內容。</span><span class="sxs-lookup"><span data-stu-id="e0108-119">Specifies the connection context of a server.</span></span>

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

### <span data-ttu-id="e0108-120">-資料庫</span><span class="sxs-lookup"><span data-stu-id="e0108-120">-Database</span></span>
<span data-ttu-id="e0108-121">指定代表 Azure SQL 資料庫的物件。</span><span class="sxs-lookup"><span data-stu-id="e0108-121">Specifies an object that represents an Azure SQL Database.</span></span>
<span data-ttu-id="e0108-122">如果您指定此參數，您必須指定 *ServerName* 參數或 *ConnectionCoNtext* 參數。</span><span class="sxs-lookup"><span data-stu-id="e0108-122">If you specify this parameter, you must specify the *ServerName* parameter or *ConnectionContext* parameter.</span></span>

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

### <span data-ttu-id="e0108-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e0108-123">-DatabaseName</span></span>
<span data-ttu-id="e0108-124">指定資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="e0108-124">Specifies the name of a database.</span></span>
<span data-ttu-id="e0108-125">如果您指定此參數，您必須指定 *ServerName* 參數或 *ConnectionCoNtext* 參數。</span><span class="sxs-lookup"><span data-stu-id="e0108-125">If you specify this parameter, you must specify the *ServerName* parameter or the *ConnectionContext* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0108-126">-OperationGuid</span><span class="sxs-lookup"><span data-stu-id="e0108-126">-OperationGuid</span></span>
<span data-ttu-id="e0108-127">指定代表此 Cmdlet 取得狀態之特定資料庫作業的操作 ID。</span><span class="sxs-lookup"><span data-stu-id="e0108-127">Specifies the operation ID that represents a specific database operation for which this cmdlet gets status.</span></span>
<span data-ttu-id="e0108-128">您可以要求 Azure SQL 資料庫或伺服器的所有資料庫作業來取得作業 Id。</span><span class="sxs-lookup"><span data-stu-id="e0108-128">You can obtain operation IDs by requesting all the database operations for a Azure SQL Database or server.</span></span>
<span data-ttu-id="e0108-129">如果您指定此參數，您必須指定 *ServerName* 參數或 *ConnectionCoNtext* 參數。</span><span class="sxs-lookup"><span data-stu-id="e0108-129">If you specify this parameter, you must specify the *ServerName* parameter or the *ConnectionContext* parameter.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0108-130">-設定檔</span><span class="sxs-lookup"><span data-stu-id="e0108-130">-Profile</span></span>
<span data-ttu-id="e0108-131">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="e0108-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e0108-132">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="e0108-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e0108-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e0108-133">-ServerName</span></span>
<span data-ttu-id="e0108-134">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="e0108-134">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="e0108-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0108-135">CommonParameters</span></span>
<span data-ttu-id="e0108-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e0108-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0108-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e0108-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0108-138">輸入</span><span class="sxs-lookup"><span data-stu-id="e0108-138">INPUTS</span></span>

### <span data-ttu-id="e0108-139">SqlDatabase.. Database （WindowsAzure）</span><span class="sxs-lookup"><span data-stu-id="e0108-139">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

### <span data-ttu-id="e0108-140">WindowsAzure. SqlDatabase. SqlDatabaseServerCoNtext</span><span class="sxs-lookup"><span data-stu-id="e0108-140">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

### <span data-ttu-id="e0108-141">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="e0108-141">System.Guid</span></span>

## <span data-ttu-id="e0108-142">輸出</span><span class="sxs-lookup"><span data-stu-id="e0108-142">OUTPUTS</span></span>

### <span data-ttu-id="e0108-143">DatabaseOperationResponseList [] SqlDatabase. WindowsAzure. []</span><span class="sxs-lookup"><span data-stu-id="e0108-143">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database.DatabaseOperationResponseList[]</span></span>
<span data-ttu-id="e0108-144">如果您有多個作業，這個 Cmdlet 就會傳回 **DatabaseOperationResponseList** 物件的陣列。</span><span class="sxs-lookup"><span data-stu-id="e0108-144">This cmdlet returns an array of **DatabaseOperationResponseList** objects if you get multiple operations.</span></span>

### <span data-ttu-id="e0108-145">SqlDatabase. DatabaseOperationResponse （WindowsAzure）的</span><span class="sxs-lookup"><span data-stu-id="e0108-145">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database.DatabaseOperationResponse</span></span>

## <span data-ttu-id="e0108-146">筆記</span><span class="sxs-lookup"><span data-stu-id="e0108-146">NOTES</span></span>

## <span data-ttu-id="e0108-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="e0108-147">RELATED LINKS</span></span>

[<span data-ttu-id="e0108-148">Azure SQL 資料庫</span><span class="sxs-lookup"><span data-stu-id="e0108-148">Azure SQL Database</span></span>](https://msdn.microsoft.com/library/ee336279.aspx)

[<span data-ttu-id="e0108-149">資料庫操作狀態</span><span class="sxs-lookup"><span data-stu-id="e0108-149">Database Operation Status</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn720371.aspx)

[<span data-ttu-id="e0108-150">Azure SQL 資料庫的作業</span><span class="sxs-lookup"><span data-stu-id="e0108-150">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="e0108-151">AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e0108-151">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="e0108-152">新-AzureSqlDatabaseServerCoNtext</span><span class="sxs-lookup"><span data-stu-id="e0108-152">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)


