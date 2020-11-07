---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 6723557D-8052-4BFA-872C-384B1423B3AE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 185ad06375fe9bbd11cb25c26b25704baeaa1dfe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967016"
---
# <span data-ttu-id="315c5-101">Get-AzureSqlDatabaseServerQuota</span><span class="sxs-lookup"><span data-stu-id="315c5-101">Get-AzureSqlDatabaseServerQuota</span></span>

## <span data-ttu-id="315c5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="315c5-102">SYNOPSIS</span></span>
<span data-ttu-id="315c5-103">取得 Azure SQL 資料庫伺服器的配額資訊。</span><span class="sxs-lookup"><span data-stu-id="315c5-103">Gets quota information for an Azure SQL Database server.</span></span>

## <span data-ttu-id="315c5-104">句法</span><span class="sxs-lookup"><span data-stu-id="315c5-104">SYNTAX</span></span>

### <span data-ttu-id="315c5-105">ByConnectionCoNtext</span><span class="sxs-lookup"><span data-stu-id="315c5-105">ByConnectionContext</span></span>
```
Get-AzureSqlDatabaseServerQuota -ConnectionContext <IServerDataServiceContext> [-QuotaName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="315c5-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="315c5-106">ByServerName</span></span>
```
Get-AzureSqlDatabaseServerQuota -ServerName <String> [-QuotaName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="315c5-107">說明</span><span class="sxs-lookup"><span data-stu-id="315c5-107">DESCRIPTION</span></span>
<span data-ttu-id="315c5-108">**AzureSqlDatabaseServerQuota** Cmdlet 會取得 Azure SQL Database Server 指定實例的配額資訊。</span><span class="sxs-lookup"><span data-stu-id="315c5-108">The **Get-AzureSqlDatabaseServerQuota** cmdlet gets the quota information for a specified instance of Azure SQL Database Server.</span></span>
<span data-ttu-id="315c5-109">指定連接內容或伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="315c5-109">Specify a connection context or the server name.</span></span>
<span data-ttu-id="315c5-110">如果您沒有指定配額名稱，此 Cmdlet 會取得伺服器的所有配額資訊。</span><span class="sxs-lookup"><span data-stu-id="315c5-110">If you do not specify a quota name, this cmdlet gets all the quota information for the server.</span></span>

## <span data-ttu-id="315c5-111">示例</span><span class="sxs-lookup"><span data-stu-id="315c5-111">EXAMPLES</span></span>

### <span data-ttu-id="315c5-112">範例1：取得特定配額的資訊</span><span class="sxs-lookup"><span data-stu-id="315c5-112">Example 1: Get information for a specific quota</span></span>
```
PS C:\> $QuotaPremium = GetAzureSqlDatabaseServerQuota $Context -QuotaName "Premium_Databases"
```

<span data-ttu-id="315c5-113">這個命令會從已儲存在 $CoNtext 變數中之連接所指定的 Azure SQL 資料庫伺服器取得名為 Premium_Databases 的配額。</span><span class="sxs-lookup"><span data-stu-id="315c5-113">This command gets the quota named Premium_Databases from the Azure SQL Database server specified by the connection stored in the $Context variable.</span></span>

### <span data-ttu-id="315c5-114">範例2：取得所有配額的資訊</span><span class="sxs-lookup"><span data-stu-id="315c5-114">Example 2: Get information for all quotas</span></span>
```
PS C:\> $QuotaList = GetAzureSqlDatabaseServerQuota $Context
```

<span data-ttu-id="315c5-115">這個命令會從連接指定的伺服器取得所有配額值 $CoNtext。</span><span class="sxs-lookup"><span data-stu-id="315c5-115">This command gets all quota values from the server specified by the connection $Context.</span></span>

## <span data-ttu-id="315c5-116">參數</span><span class="sxs-lookup"><span data-stu-id="315c5-116">PARAMETERS</span></span>

### <span data-ttu-id="315c5-117">-ConnectionCoNtext</span><span class="sxs-lookup"><span data-stu-id="315c5-117">-ConnectionContext</span></span>
<span data-ttu-id="315c5-118">指定伺服器的連接內容。</span><span class="sxs-lookup"><span data-stu-id="315c5-118">Specifies the connection context of a server.</span></span>

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

### <span data-ttu-id="315c5-119">-設定檔</span><span class="sxs-lookup"><span data-stu-id="315c5-119">-Profile</span></span>
<span data-ttu-id="315c5-120">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="315c5-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="315c5-121">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="315c5-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="315c5-122">-QuotaName</span><span class="sxs-lookup"><span data-stu-id="315c5-122">-QuotaName</span></span>
<span data-ttu-id="315c5-123">指定此 Cmdlet 取得的配額值的名稱。</span><span class="sxs-lookup"><span data-stu-id="315c5-123">Specifies the name of the quota value that this cmdlet gets.</span></span>

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

### <span data-ttu-id="315c5-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="315c5-124">-ServerName</span></span>
<span data-ttu-id="315c5-125">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="315c5-125">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="315c5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="315c5-126">CommonParameters</span></span>
<span data-ttu-id="315c5-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="315c5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="315c5-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="315c5-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="315c5-129">輸入</span><span class="sxs-lookup"><span data-stu-id="315c5-129">INPUTS</span></span>

## <span data-ttu-id="315c5-130">輸出</span><span class="sxs-lookup"><span data-stu-id="315c5-130">OUTPUTS</span></span>

### <span data-ttu-id="315c5-131">ServerQuota [] SqlDatabase. []</span><span class="sxs-lookup"><span data-stu-id="315c5-131">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServerQuota[]</span></span>

## <span data-ttu-id="315c5-132">筆記</span><span class="sxs-lookup"><span data-stu-id="315c5-132">NOTES</span></span>
* <span data-ttu-id="315c5-133">驗證：此 Cmdlet 可以使用 SQL Server 驗證或以證書為基礎的驗證。</span><span class="sxs-lookup"><span data-stu-id="315c5-133">Authentication: This cmdlet can use either SQL Server authentication or certificate-based authentication.</span></span> <span data-ttu-id="315c5-134">如需設定驗證的範例，請參閱 New-AzureSqlDatabaseServerContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="315c5-134">For examples of setting up authentication, see the New-AzureSqlDatabaseServerContext cmdlet.</span></span>

## <span data-ttu-id="315c5-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="315c5-135">RELATED LINKS</span></span>

[<span data-ttu-id="315c5-136">Azure SQL 資料庫</span><span class="sxs-lookup"><span data-stu-id="315c5-136">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="315c5-137">Azure SQL 資料庫的作業</span><span class="sxs-lookup"><span data-stu-id="315c5-137">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="315c5-138">新-AzureSqlDatabaseServerCoNtext</span><span class="sxs-lookup"><span data-stu-id="315c5-138">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)


