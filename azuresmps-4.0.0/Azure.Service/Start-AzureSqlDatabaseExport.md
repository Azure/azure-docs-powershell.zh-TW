---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 3005E411-9466-4602-8E07-F4EF8804AB2A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22bff485bf49e0ec5f482e1325af661862583605
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967198"
---
# <span data-ttu-id="f3aa4-101">Start-AzureSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="f3aa4-101">Start-AzureSqlDatabaseExport</span></span>

## <span data-ttu-id="f3aa4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f3aa4-102">SYNOPSIS</span></span>
<span data-ttu-id="f3aa4-103">從 Azure SQL 資料庫開始匯出作業至 Blob 儲存空間。</span><span class="sxs-lookup"><span data-stu-id="f3aa4-103">Starts an export operation from an Azure SQL Database to Blob storage.</span></span>

## <span data-ttu-id="f3aa4-104">句法</span><span class="sxs-lookup"><span data-stu-id="f3aa4-104">SYNTAX</span></span>

### <span data-ttu-id="f3aa4-105">ByContainerObject</span><span class="sxs-lookup"><span data-stu-id="f3aa4-105">ByContainerObject</span></span>
```
Start-AzureSqlDatabaseExport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContainer <AzureStorageContainer> -DatabaseName <String> -BlobName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f3aa4-106">ByContainerName</span><span class="sxs-lookup"><span data-stu-id="f3aa4-106">ByContainerName</span></span>
```
Start-AzureSqlDatabaseExport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContext <IStorageContext> -StorageContainerName <String> -DatabaseName <String> -BlobName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f3aa4-107">說明</span><span class="sxs-lookup"><span data-stu-id="f3aa4-107">DESCRIPTION</span></span>
<span data-ttu-id="f3aa4-108">**AzureSqlDatabaseExport** Cmdlet 會從 Azure SQL 資料庫開始匯出作業至 Blob 儲存空間。</span><span class="sxs-lookup"><span data-stu-id="f3aa4-108">The **Start-AzureSqlDatabaseExport** cmdlet starts an export operation from an Azure SQL Database to Blob storage.</span></span>
<span data-ttu-id="f3aa4-109">操作需要資料庫伺服器線上內容。</span><span class="sxs-lookup"><span data-stu-id="f3aa4-109">The operation requires a database server connection context.</span></span>
<span data-ttu-id="f3aa4-110">使用 Get-AzureSqlDatabaseImportExportStatus Cmdlet 取得匯出操作的狀態。</span><span class="sxs-lookup"><span data-stu-id="f3aa4-110">Use the Get-AzureSqlDatabaseImportExportStatus cmdlet to get the status of the export operation.</span></span>

## <span data-ttu-id="f3aa4-111">示例</span><span class="sxs-lookup"><span data-stu-id="f3aa4-111">EXAMPLES</span></span>

### <span data-ttu-id="f3aa4-112">範例1：匯出資料庫</span><span class="sxs-lookup"><span data-stu-id="f3aa4-112">Example 1: Export a database</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> $SqlContext = New-AzureSqlDatabaseServerContext -ServerName $ServerName -Credential $Credential
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName $StorageName -StorageAccountKey $StorageKey
PS C:\> $Container = Get-AzureStorageContainer -Name $ContainerName -Context $StorageContext
PS C:\> $exportRequest = Start-AzureSqlDatabaseExport -SqlConnectionContext $SqlContext -StorageContainer $Container -DatabaseName $DatabaseName -BlobName $BlobName
```

<span data-ttu-id="f3aa4-113">這個範例會啟動 Azure SQL Database 的匯出程式，並將名稱儲存在 $DatabaseName 變數中，並儲存在 $BlobName 變數中的 Blob 儲存空間。</span><span class="sxs-lookup"><span data-stu-id="f3aa4-113">This example initiates an export process from the Azure SQL Database that has the name stored in the $DatabaseName variable to the Blob storage stored in the $BlobName variable.</span></span>

## <span data-ttu-id="f3aa4-114">參數</span><span class="sxs-lookup"><span data-stu-id="f3aa4-114">PARAMETERS</span></span>

### <span data-ttu-id="f3aa4-115">-BlobName</span><span class="sxs-lookup"><span data-stu-id="f3aa4-115">-BlobName</span></span>
<span data-ttu-id="f3aa4-116">指定此 Cmdlet 匯出資料庫的 Azure Blob 儲存空間名稱。</span><span class="sxs-lookup"><span data-stu-id="f3aa4-116">Specifies the name of the Azure Blob storage into which this cmdlet exports the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3aa4-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f3aa4-117">-DatabaseName</span></span>
<span data-ttu-id="f3aa4-118">指定此 Cmdlet 匯出資料的資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3aa4-118">Specifies the name of the database from which this cmdlet exports data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3aa4-119">-設定檔</span><span class="sxs-lookup"><span data-stu-id="f3aa4-119">-Profile</span></span>
<span data-ttu-id="f3aa4-120">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="f3aa4-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f3aa4-121">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="f3aa4-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f3aa4-122">-SqlConnectionCoNtext</span><span class="sxs-lookup"><span data-stu-id="f3aa4-122">-SqlConnectionContext</span></span>
<span data-ttu-id="f3aa4-123">指定包含資料庫之伺服器的連接內容。</span><span class="sxs-lookup"><span data-stu-id="f3aa4-123">Specifies the connection context of a server that contains the database.</span></span>

```yaml
Type: ISqlServerConnectionInformation
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3aa4-124">-StorageContainer</span><span class="sxs-lookup"><span data-stu-id="f3aa4-124">-StorageContainer</span></span>
<span data-ttu-id="f3aa4-125">指定包含此 Cmdlet 匯出資料庫之 Blob 的儲存容器。</span><span class="sxs-lookup"><span data-stu-id="f3aa4-125">Specifies the storage container that contains the Blob into which this cmdlet export a database.</span></span>

```yaml
Type: AzureStorageContainer
Parameter Sets: ByContainerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3aa4-126">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="f3aa4-126">-StorageContainerName</span></span>
<span data-ttu-id="f3aa4-127">指定包含此 Cmdlet 匯出資料庫之 Blob 之儲存容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3aa4-127">Specifies the name of the storage container that contains the Blob into which this cmdlet exports a database.</span></span>

```yaml
Type: String
Parameter Sets: ByContainerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3aa4-128">-StorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="f3aa4-128">-StorageContext</span></span>
<span data-ttu-id="f3aa4-129">指定 [Blob 儲存區] 容器的內容。</span><span class="sxs-lookup"><span data-stu-id="f3aa4-129">Specifies the context of the Blob storage container.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ByContainerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3aa4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3aa4-130">CommonParameters</span></span>
<span data-ttu-id="f3aa4-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f3aa4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3aa4-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f3aa4-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3aa4-133">輸入</span><span class="sxs-lookup"><span data-stu-id="f3aa4-133">INPUTS</span></span>

## <span data-ttu-id="f3aa4-134">輸出</span><span class="sxs-lookup"><span data-stu-id="f3aa4-134">OUTPUTS</span></span>

### <span data-ttu-id="f3aa4-135">SqlDatabase. ImportExportRequest （WindowsAzure）</span><span class="sxs-lookup"><span data-stu-id="f3aa4-135">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.ImportExportRequest</span></span>

## <span data-ttu-id="f3aa4-136">筆記</span><span class="sxs-lookup"><span data-stu-id="f3aa4-136">NOTES</span></span>

## <span data-ttu-id="f3aa4-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="f3aa4-137">RELATED LINKS</span></span>

[<span data-ttu-id="f3aa4-138">Azure SQL 資料庫</span><span class="sxs-lookup"><span data-stu-id="f3aa4-138">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="f3aa4-139">匯出資料庫</span><span class="sxs-lookup"><span data-stu-id="f3aa4-139">Export Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn781282.aspx)

[<span data-ttu-id="f3aa4-140">Azure SQL 資料庫的作業</span><span class="sxs-lookup"><span data-stu-id="f3aa4-140">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="f3aa4-141">AzureSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="f3aa4-141">Get-AzureSqlDatabaseImportExportStatus</span></span>](./Get-AzureSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="f3aa4-142">開始-AzureSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="f3aa4-142">Start-AzureSqlDatabaseImport</span></span>](./Start-AzureSqlDatabaseImport.md)


