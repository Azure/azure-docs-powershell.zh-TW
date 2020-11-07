---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 83E8DAD8-151A-408D-819F-274CB813ABDA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6f9a5753fdf4f87afc6baacbe9fc4c33c9be08ef
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93968005"
---
# <span data-ttu-id="0b1f8-101">Get-AzureSqlRecoverableDatabase</span><span class="sxs-lookup"><span data-stu-id="0b1f8-101">Get-AzureSqlRecoverableDatabase</span></span>

## <span data-ttu-id="0b1f8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0b1f8-102">SYNOPSIS</span></span>
<span data-ttu-id="0b1f8-103">從指定的伺服器取得可復原的資料庫。</span><span class="sxs-lookup"><span data-stu-id="0b1f8-103">Gets recoverable databases from a specified server.</span></span>

## <span data-ttu-id="0b1f8-104">句法</span><span class="sxs-lookup"><span data-stu-id="0b1f8-104">SYNTAX</span></span>

### <span data-ttu-id="0b1f8-105">AllDatabasesOnGivenServer (預設) </span><span class="sxs-lookup"><span data-stu-id="0b1f8-105">AllDatabasesOnGivenServer (Default)</span></span>
```
Get-AzureSqlRecoverableDatabase -ServerName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0b1f8-106">GivenDatabaseOnGivenServer</span><span class="sxs-lookup"><span data-stu-id="0b1f8-106">GivenDatabaseOnGivenServer</span></span>
```
Get-AzureSqlRecoverableDatabase -ServerName <String> -DatabaseName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="0b1f8-107">GivenDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="0b1f8-107">GivenDatabaseObject</span></span>
```
Get-AzureSqlRecoverableDatabase -Database <RecoverableDatabase> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="0b1f8-108">說明</span><span class="sxs-lookup"><span data-stu-id="0b1f8-108">DESCRIPTION</span></span>
<span data-ttu-id="0b1f8-109">**AzureSqlRecoverableDatabase** Cmdlet 會從指定的伺服器取得可復原的資料庫。</span><span class="sxs-lookup"><span data-stu-id="0b1f8-109">The **Get-AzureSqlRecoverableDatabase** cmdlet gets recoverable databases from a specified server.</span></span>
<span data-ttu-id="0b1f8-110">這個 Cmdlet 會在伺服器上取得特定的可復原資料庫或所有可復原的資料庫。</span><span class="sxs-lookup"><span data-stu-id="0b1f8-110">This cmdlet gets a specific recoverable database or all recoverable databases on a server.</span></span>

## <span data-ttu-id="0b1f8-111">示例</span><span class="sxs-lookup"><span data-stu-id="0b1f8-111">EXAMPLES</span></span>

### <span data-ttu-id="0b1f8-112">範例1：取得所有可復原的資料庫</span><span class="sxs-lookup"><span data-stu-id="0b1f8-112">Example 1: Get all recoverable databases</span></span>
```
PS C:\> Get-AzureSqlRecoverableDatabase -ServerName "Server01"
```

<span data-ttu-id="0b1f8-113">這個命令會取得伺服器上名為 Server01 的所有可復原資料庫。</span><span class="sxs-lookup"><span data-stu-id="0b1f8-113">This command gets all recoverable databases on the server named Server01.</span></span>

### <span data-ttu-id="0b1f8-114">範例2：取得特定的可復原資料庫</span><span class="sxs-lookup"><span data-stu-id="0b1f8-114">Example 2: Get a specific recoverable database</span></span>
```
PS C:\> Get-AzureSqlRecoverableDatabase -ServerName "Server01" -DatabaseName "Database17"
```

<span data-ttu-id="0b1f8-115">這個命令會在名為 Server01 的伺服器上檢索名為 Database17 的資料庫。</span><span class="sxs-lookup"><span data-stu-id="0b1f8-115">This command gets retrieves the database named Database17 on the server named Server01.</span></span>

## <span data-ttu-id="0b1f8-116">參數</span><span class="sxs-lookup"><span data-stu-id="0b1f8-116">PARAMETERS</span></span>

### <span data-ttu-id="0b1f8-117">-資料庫</span><span class="sxs-lookup"><span data-stu-id="0b1f8-117">-Database</span></span>
<span data-ttu-id="0b1f8-118">指定代表此 Cmdlet 所取得的可復原資料庫的物件。</span><span class="sxs-lookup"><span data-stu-id="0b1f8-118">Specifies an object that represents the recoverable database that this cmdlet gets.</span></span>

```yaml
Type: RecoverableDatabase
Parameter Sets: GivenDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b1f8-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0b1f8-119">-DatabaseName</span></span>
<span data-ttu-id="0b1f8-120">指定此 Cmdlet 取得的可復原資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="0b1f8-120">Specifies the name of the recoverable database that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GivenDatabaseOnGivenServer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b1f8-121">-設定檔</span><span class="sxs-lookup"><span data-stu-id="0b1f8-121">-Profile</span></span>
<span data-ttu-id="0b1f8-122">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="0b1f8-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0b1f8-123">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="0b1f8-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0b1f8-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0b1f8-124">-ServerName</span></span>
<span data-ttu-id="0b1f8-125">指定此 Cmdlet 取得可復原資料庫的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="0b1f8-125">Specifies the name of the server from which this cmdlet gets recoverable databases.</span></span>

```yaml
Type: String
Parameter Sets: AllDatabasesOnGivenServer, GivenDatabaseOnGivenServer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b1f8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b1f8-126">CommonParameters</span></span>
<span data-ttu-id="0b1f8-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0b1f8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b1f8-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0b1f8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b1f8-129">輸入</span><span class="sxs-lookup"><span data-stu-id="0b1f8-129">INPUTS</span></span>

### <span data-ttu-id="0b1f8-130">RecoverableDatabase （WindowsAzure）。</span><span class="sxs-lookup"><span data-stu-id="0b1f8-130">Microsoft.WindowsAzure.Management.Sql.Models.RecoverableDatabase</span></span>

## <span data-ttu-id="0b1f8-131">輸出</span><span class="sxs-lookup"><span data-stu-id="0b1f8-131">OUTPUTS</span></span>

### <span data-ttu-id="0b1f8-132">IEnumerable\<Microsoft.WindowsAzure.Management.Sql.Models.RecoverableDatabase\></span><span class="sxs-lookup"><span data-stu-id="0b1f8-132">IEnumerable\<Microsoft.WindowsAzure.Management.Sql.Models.RecoverableDatabase\></span></span>

## <span data-ttu-id="0b1f8-133">筆記</span><span class="sxs-lookup"><span data-stu-id="0b1f8-133">NOTES</span></span>
* <span data-ttu-id="0b1f8-134">您必須使用以憑證為基礎的驗證才能執行這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0b1f8-134">You must use certificate-based authentication to run this cmdlet.</span></span> <span data-ttu-id="0b1f8-135">在執行此 Cmdlet 的電腦上執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="0b1f8-135">Run the following commands on the computer where run this cmdlet:</span></span> 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## <span data-ttu-id="0b1f8-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="0b1f8-136">RELATED LINKS</span></span>

[<span data-ttu-id="0b1f8-137">Azure SQL 資料庫</span><span class="sxs-lookup"><span data-stu-id="0b1f8-137">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="0b1f8-138">取得可復原的資料庫</span><span class="sxs-lookup"><span data-stu-id="0b1f8-138">Get Recoverable Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn800985.aspx)

[<span data-ttu-id="0b1f8-139">Azure SQL 資料庫的作業</span><span class="sxs-lookup"><span data-stu-id="0b1f8-139">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="0b1f8-140">開始-AzureSqlDatabaseRecovery</span><span class="sxs-lookup"><span data-stu-id="0b1f8-140">Start-AzureSqlDatabaseRecovery</span></span>](./Start-AzureSqlDatabaseRecovery.md)


