---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F63769D6-9A31-4A67-972A-1E0428853C86
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88f61718e363a630b70519590025a6da80364aeb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966869"
---
# <span data-ttu-id="13bdd-101">Start-AzureSqlDatabaseRecovery</span><span class="sxs-lookup"><span data-stu-id="13bdd-101">Start-AzureSqlDatabaseRecovery</span></span>

## <span data-ttu-id="13bdd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="13bdd-102">SYNOPSIS</span></span>
<span data-ttu-id="13bdd-103">啟動資料庫的還原要求。</span><span class="sxs-lookup"><span data-stu-id="13bdd-103">Initiates a restore request for a database.</span></span>

## <span data-ttu-id="13bdd-104">句法</span><span class="sxs-lookup"><span data-stu-id="13bdd-104">SYNTAX</span></span>

### <span data-ttu-id="13bdd-105">BySourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="13bdd-105">BySourceDatabaseName</span></span>
```
Start-AzureSqlDatabaseRecovery -SourceServerName <String> -SourceDatabaseName <String>
 [-TargetServerName <String>] [-TargetDatabaseName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="13bdd-106">BySourceDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="13bdd-106">BySourceDatabaseObject</span></span>
```
Start-AzureSqlDatabaseRecovery -SourceDatabase <RecoverableDatabase> [-TargetServerName <String>]
 [-TargetDatabaseName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="13bdd-107">說明</span><span class="sxs-lookup"><span data-stu-id="13bdd-107">DESCRIPTION</span></span>
<span data-ttu-id="13bdd-108">**Start-AzureSqlDatabaseRecovery** Cmdlet 會針對即時或刪除的資料庫啟動還原要求。</span><span class="sxs-lookup"><span data-stu-id="13bdd-108">The **Start-AzureSqlDatabaseRecovery** cmdlet initiates a restore request for a live or dropped database.</span></span>
<span data-ttu-id="13bdd-109">這個 Cmdlet 支援基本的復原，該恢復會使用資料庫最近已知可用的備份。</span><span class="sxs-lookup"><span data-stu-id="13bdd-109">This cmdlet supports basic recovery that uses the last known available backup for the database.</span></span>
<span data-ttu-id="13bdd-110">[恢復] 作業會建立新的資料庫。</span><span class="sxs-lookup"><span data-stu-id="13bdd-110">The recovery operation creates a new database.</span></span>
<span data-ttu-id="13bdd-111">如果您在同一個伺服器上復原即時資料庫，您必須為新資料庫指定不同的名稱。</span><span class="sxs-lookup"><span data-stu-id="13bdd-111">If you recover a live database on the same server, you must specify a different name for the new database.</span></span>

<span data-ttu-id="13bdd-112">若要為資料庫執行時間點還原，請改用 **Start AzureSqlDatabaseRestore** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="13bdd-112">To do a point in time restore for a database, use the **Start-AzureSqlDatabaseRestore** cmdlet instead.</span></span>

## <span data-ttu-id="13bdd-113">示例</span><span class="sxs-lookup"><span data-stu-id="13bdd-113">EXAMPLES</span></span>

### <span data-ttu-id="13bdd-114">範例1：復原指定為物件的資料庫</span><span class="sxs-lookup"><span data-stu-id="13bdd-114">Example 1: Recover a database specified as an object</span></span>
```
PS C:\> $Database = Get-AzureSqlRecoverableDatabase -ServerName "Server01" -DatabaseName "Database17" 
PS C:\> $Operation = Start-AzureSqlDatabaseRecovery -SourceDatabase $Database -TargetDatabaseName "DatabaseRestored"
```

<span data-ttu-id="13bdd-115">第一個命令會使用 **AzureSqlRecoverableDatabase** Cmdlet 取得資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="13bdd-115">The first command gets a database object by using the **Get-AzureSqlRecoverableDatabase** cmdlet.</span></span>
<span data-ttu-id="13bdd-116">該命令會將該物件儲存在 $Database 變數中。</span><span class="sxs-lookup"><span data-stu-id="13bdd-116">The command stores that object in the $Database variable.</span></span>

<span data-ttu-id="13bdd-117">第二個命令會恢復儲存在 $Database 中的資料庫。</span><span class="sxs-lookup"><span data-stu-id="13bdd-117">The second command recovers the database stored in $Database.</span></span>

### <span data-ttu-id="13bdd-118">範例2：復原名稱指定的資料庫</span><span class="sxs-lookup"><span data-stu-id="13bdd-118">Example 2: Recover a database specified by name</span></span>
```
PS C:\> $Operation = Start-AzureSqlDatabaseRecovery -SourceServerName "Server01" -SourceDatabaseName "Database17" -TargetDatabaseName "DatabaseRestored"
```

<span data-ttu-id="13bdd-119">這個命令會使用資料庫名稱來恢復資料庫。</span><span class="sxs-lookup"><span data-stu-id="13bdd-119">This command recovers a database using the database name.</span></span>

## <span data-ttu-id="13bdd-120">參數</span><span class="sxs-lookup"><span data-stu-id="13bdd-120">PARAMETERS</span></span>

### <span data-ttu-id="13bdd-121">-設定檔</span><span class="sxs-lookup"><span data-stu-id="13bdd-121">-Profile</span></span>
<span data-ttu-id="13bdd-122">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="13bdd-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="13bdd-123">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="13bdd-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="13bdd-124">-SourceDatabase</span><span class="sxs-lookup"><span data-stu-id="13bdd-124">-SourceDatabase</span></span>
<span data-ttu-id="13bdd-125">指定代表此 Cmdlet 所恢復之資料庫的資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="13bdd-125">Specifies the database object that represents the database that this cmdlet recovers.</span></span>

```yaml
Type: RecoverableDatabase
Parameter Sets: BySourceDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13bdd-126">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="13bdd-126">-SourceDatabaseName</span></span>
<span data-ttu-id="13bdd-127">指定此 Cmdlet 要恢復的資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="13bdd-127">Specifies the name of the database that this cmdlet recovers.</span></span>

```yaml
Type: String
Parameter Sets: BySourceDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13bdd-128">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="13bdd-128">-SourceServerName</span></span>
<span data-ttu-id="13bdd-129">指定源資料庫處於即時及正在執行的伺服器名稱，或在刪除之前執行源資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="13bdd-129">Specifies the name of the server on which the source database is live and running, or on which the source database ran before it was deleted.</span></span>

```yaml
Type: String
Parameter Sets: BySourceDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13bdd-130">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="13bdd-130">-TargetDatabaseName</span></span>
<span data-ttu-id="13bdd-131">指定復原資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="13bdd-131">Specifies the name of the recovered database.</span></span>
<span data-ttu-id="13bdd-132">如果來源資料庫仍在使用中，若要將其復原至同一個伺服器，您必須指定與源資料庫名稱不同的名稱。</span><span class="sxs-lookup"><span data-stu-id="13bdd-132">If the source database is still live, in order to recover it to the same server, you must specify a name that differs from the source database name.</span></span>

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

### <span data-ttu-id="13bdd-133">-TargetServerName</span><span class="sxs-lookup"><span data-stu-id="13bdd-133">-TargetServerName</span></span>
<span data-ttu-id="13bdd-134">指定要還原資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="13bdd-134">Specifies the name of the server to which to restore a database.</span></span>
<span data-ttu-id="13bdd-135">您可以將資料庫還原至同一個伺服器或另一個伺服器。</span><span class="sxs-lookup"><span data-stu-id="13bdd-135">You can restore a database to the same server or to a different server.</span></span>

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

### <span data-ttu-id="13bdd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13bdd-136">CommonParameters</span></span>
<span data-ttu-id="13bdd-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="13bdd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13bdd-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="13bdd-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13bdd-139">輸入</span><span class="sxs-lookup"><span data-stu-id="13bdd-139">INPUTS</span></span>

### <span data-ttu-id="13bdd-140">RecoverableDatabase （WindowsAzure）。</span><span class="sxs-lookup"><span data-stu-id="13bdd-140">Microsoft.WindowsAzure.Management.Sql.Models.RecoverableDatabase</span></span>

## <span data-ttu-id="13bdd-141">輸出</span><span class="sxs-lookup"><span data-stu-id="13bdd-141">OUTPUTS</span></span>

### <span data-ttu-id="13bdd-142">RecoverDatabaseOperation （WindowsAzure）。</span><span class="sxs-lookup"><span data-stu-id="13bdd-142">Microsoft.WindowsAzure.Management.Sql.Models.RecoverDatabaseOperation</span></span>

## <span data-ttu-id="13bdd-143">筆記</span><span class="sxs-lookup"><span data-stu-id="13bdd-143">NOTES</span></span>
* <span data-ttu-id="13bdd-144">您必須使用以憑證為基礎的驗證才能執行這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="13bdd-144">You must use certificate-based authentication to run this cmdlet.</span></span> <span data-ttu-id="13bdd-145">在執行此 Cmdlet 的電腦上執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="13bdd-145">Run the following commands on the computer where you run this cmdlet:</span></span> 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## <span data-ttu-id="13bdd-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="13bdd-146">RELATED LINKS</span></span>

[<span data-ttu-id="13bdd-147">Azure SQL 資料庫</span><span class="sxs-lookup"><span data-stu-id="13bdd-147">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="13bdd-148">建立資料庫恢復要求</span><span class="sxs-lookup"><span data-stu-id="13bdd-148">Create Database Recovery Request</span></span>](https://msdn.microsoft.com/en-us/library/dn800986.aspx)

[<span data-ttu-id="13bdd-149">Azure SQL Database 中的異地複製</span><span class="sxs-lookup"><span data-stu-id="13bdd-149">Geo-Replication in Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/)

[<span data-ttu-id="13bdd-150">Azure SQL 資料庫的作業</span><span class="sxs-lookup"><span data-stu-id="13bdd-150">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="13bdd-151">AzureSqlRecoverableDatabase</span><span class="sxs-lookup"><span data-stu-id="13bdd-151">Get-AzureSqlRecoverableDatabase</span></span>](./Get-AzureSqlRecoverableDatabase.md)

[<span data-ttu-id="13bdd-152">開始-AzureSqlDatabaseRestore</span><span class="sxs-lookup"><span data-stu-id="13bdd-152">Start-AzureSqlDatabaseRestore</span></span>](./Start-AzureSqlDatabaseRestore.md)


