---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5EE936CA-DD9A-4BC6-B835-E22AE633B46D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4bc7c8f39f1bdbd35cfffeb59b3b4f184f30845e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966873"
---
# <span data-ttu-id="2b694-101">Start-AzureSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="2b694-101">Start-AzureSqlDatabaseImport</span></span>

## <span data-ttu-id="2b694-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2b694-102">SYNOPSIS</span></span>
<span data-ttu-id="2b694-103">從 blob 儲存體開始匯入作業至 Azure SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="2b694-103">Starts an import operation from blob storage to an Azure SQL Database.</span></span>

## <span data-ttu-id="2b694-104">句法</span><span class="sxs-lookup"><span data-stu-id="2b694-104">SYNTAX</span></span>

### <span data-ttu-id="2b694-105">ByContainerObject</span><span class="sxs-lookup"><span data-stu-id="2b694-105">ByContainerObject</span></span>
```
Start-AzureSqlDatabaseImport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContainer <AzureStorageContainer> -DatabaseName <String> -BlobName <String>
 [-Edition <DatabaseEdition>] [-DatabaseMaxSize <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="2b694-106">ByContainerName</span><span class="sxs-lookup"><span data-stu-id="2b694-106">ByContainerName</span></span>
```
Start-AzureSqlDatabaseImport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContext <IStorageContext> -StorageContainerName <String> -DatabaseName <String> -BlobName <String>
 [-Edition <DatabaseEdition>] [-DatabaseMaxSize <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2b694-107">說明</span><span class="sxs-lookup"><span data-stu-id="2b694-107">DESCRIPTION</span></span>
<span data-ttu-id="2b694-108">**AzureSqlDatabaseImport** Cmdlet 會從 azure Blob 儲存體開始匯入作業至 Azure SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="2b694-108">The **Start-AzureSqlDatabaseImport** cmdlet starts an import operation from Azure Blob storage to an Azure SQL Database.</span></span>
<span data-ttu-id="2b694-109">如果資料庫不存在，此 Cmdlet 會使用您所指定的大小與版本值來建立它。</span><span class="sxs-lookup"><span data-stu-id="2b694-109">If the database does not exist, this cmdlet creates it by using the size and edition values that you specify.</span></span>
<span data-ttu-id="2b694-110">操作需要資料庫伺服器線上內容。</span><span class="sxs-lookup"><span data-stu-id="2b694-110">The operation requires a database server connection context.</span></span>
<span data-ttu-id="2b694-111">使用 Get-AzureSqlDatabaseImportExportStatus Cmdlet 來取得匯入操作的狀態。</span><span class="sxs-lookup"><span data-stu-id="2b694-111">Use the Get-AzureSqlDatabaseImportExportStatus cmdlet to get the status of the import operation.</span></span>

## <span data-ttu-id="2b694-112">示例</span><span class="sxs-lookup"><span data-stu-id="2b694-112">EXAMPLES</span></span>

### <span data-ttu-id="2b694-113">範例1：匯入資料庫</span><span class="sxs-lookup"><span data-stu-id="2b694-113">Example 1: Import a database</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> $SqlContext = New-AzureSqlDatabaseServerContext -ServerName $ServerName -Credentials $Credential
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName $StorageName -StorageAccountKey $StorageKey
PS C:\> $Container = Get-AzureStorageContainer -Name $ContainerName -Context $StorageContext
PS C:\> $ImportRequest = Start-AzureSqlDatabaseImport -SqlConnectionContext $SqlContext -StorageContainer $Container -DatabaseName $DatabaseName -BlobName $BlobName
```

<span data-ttu-id="2b694-114">這個範例會啟動從 $BlobName 變數中的 Blob 儲存體到名為 DatabaseName 的 Azure SQL 資料庫的匯入處理常式。</span><span class="sxs-lookup"><span data-stu-id="2b694-114">This example initiates an import process from the Blob storage in the $BlobName variable into the Azure SQL Database named DatabaseName.</span></span>

## <span data-ttu-id="2b694-115">參數</span><span class="sxs-lookup"><span data-stu-id="2b694-115">PARAMETERS</span></span>

### <span data-ttu-id="2b694-116">-BlobName</span><span class="sxs-lookup"><span data-stu-id="2b694-116">-BlobName</span></span>
<span data-ttu-id="2b694-117">指定此 Cmdlet 從中匯入資料庫的 Azure Blob 儲存空間名稱。</span><span class="sxs-lookup"><span data-stu-id="2b694-117">Specifies the name of the Azure Blob storage from which this cmdlet imports the database.</span></span>

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

### <span data-ttu-id="2b694-118">-DatabaseMaxSize</span><span class="sxs-lookup"><span data-stu-id="2b694-118">-DatabaseMaxSize</span></span>
<span data-ttu-id="2b694-119">指定資料庫的最大大小（以 gb 為限制）。</span><span class="sxs-lookup"><span data-stu-id="2b694-119">Specifies the maximum size, in gigabytes, for the database.</span></span>
<span data-ttu-id="2b694-120">如果資料庫不存在，此 Cmdlet 會根據此最大大小建立。</span><span class="sxs-lookup"><span data-stu-id="2b694-120">If the database does not exist, this cmdlet creates it based on this maximum size.</span></span>
<span data-ttu-id="2b694-121">根據版本，可接受的值會有所不同。</span><span class="sxs-lookup"><span data-stu-id="2b694-121">The acceptable values differ based on edition.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b694-122">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2b694-122">-DatabaseName</span></span>
<span data-ttu-id="2b694-123">指定資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b694-123">Specifies a name for the database.</span></span>
<span data-ttu-id="2b694-124">如果資料庫不存在，此 Cmdlet 會建立它，並指派此參數指定的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b694-124">If the database does not exist, this cmdlet creates it, and assigns the name that this parameter specifies.</span></span>

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

### <span data-ttu-id="2b694-125">-Edition</span><span class="sxs-lookup"><span data-stu-id="2b694-125">-Edition</span></span>
<span data-ttu-id="2b694-126">指定資料庫的版本。</span><span class="sxs-lookup"><span data-stu-id="2b694-126">Specifies the edition of the database.</span></span>
<span data-ttu-id="2b694-127">如果資料庫不存在，此 Cmdlet 會將它建立為此版本。</span><span class="sxs-lookup"><span data-stu-id="2b694-127">If the database does not exist, this cmdlet creates it as this edition.</span></span>
<span data-ttu-id="2b694-128">有效值為：</span><span class="sxs-lookup"><span data-stu-id="2b694-128">Valid values are:</span></span> 

- <span data-ttu-id="2b694-129">所有</span><span class="sxs-lookup"><span data-stu-id="2b694-129">None</span></span>
- <span data-ttu-id="2b694-130">網站</span><span class="sxs-lookup"><span data-stu-id="2b694-130">Web</span></span> 
- <span data-ttu-id="2b694-131">部門</span><span class="sxs-lookup"><span data-stu-id="2b694-131">Business</span></span> 
- <span data-ttu-id="2b694-132">空白</span><span class="sxs-lookup"><span data-stu-id="2b694-132">Basic</span></span>
- <span data-ttu-id="2b694-133">標準</span><span class="sxs-lookup"><span data-stu-id="2b694-133">Standard</span></span>
- <span data-ttu-id="2b694-134">佳</span><span class="sxs-lookup"><span data-stu-id="2b694-134">Premium</span></span>

<span data-ttu-id="2b694-135">預設值為 Web。</span><span class="sxs-lookup"><span data-stu-id="2b694-135">The default is Web.</span></span>

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b694-136">-設定檔</span><span class="sxs-lookup"><span data-stu-id="2b694-136">-Profile</span></span>
<span data-ttu-id="2b694-137">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="2b694-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2b694-138">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="2b694-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2b694-139">-SqlConnectionCoNtext</span><span class="sxs-lookup"><span data-stu-id="2b694-139">-SqlConnectionContext</span></span>
<span data-ttu-id="2b694-140">指定包含資料庫之伺服器的連接內容。</span><span class="sxs-lookup"><span data-stu-id="2b694-140">Specifies the connection context of a server that contains the database.</span></span>

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

### <span data-ttu-id="2b694-141">-StorageContainer</span><span class="sxs-lookup"><span data-stu-id="2b694-141">-StorageContainer</span></span>
<span data-ttu-id="2b694-142">指定包含此 Cmdlet 從中匯入資料庫之 Blob 的儲存容器。</span><span class="sxs-lookup"><span data-stu-id="2b694-142">Specifies the storage container that contains the Blob from which this cmdlet imports a database.</span></span>

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

### <span data-ttu-id="2b694-143">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="2b694-143">-StorageContainerName</span></span>
<span data-ttu-id="2b694-144">指定 [Blob 儲存區] 容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b694-144">Specifies the name of the Blob storage container.</span></span>

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

### <span data-ttu-id="2b694-145">-StorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="2b694-145">-StorageContext</span></span>
<span data-ttu-id="2b694-146">指定 [Blob 儲存區] 容器的內容。</span><span class="sxs-lookup"><span data-stu-id="2b694-146">Specifies the context of the Blob storage container.</span></span>

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

### <span data-ttu-id="2b694-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b694-147">CommonParameters</span></span>
<span data-ttu-id="2b694-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2b694-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b694-149">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2b694-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b694-150">輸入</span><span class="sxs-lookup"><span data-stu-id="2b694-150">INPUTS</span></span>

## <span data-ttu-id="2b694-151">輸出</span><span class="sxs-lookup"><span data-stu-id="2b694-151">OUTPUTS</span></span>

### <span data-ttu-id="2b694-152">SqlDatabase. ImportExportRequest （WindowsAzure）</span><span class="sxs-lookup"><span data-stu-id="2b694-152">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.ImportExportRequest</span></span>

## <span data-ttu-id="2b694-153">筆記</span><span class="sxs-lookup"><span data-stu-id="2b694-153">NOTES</span></span>

## <span data-ttu-id="2b694-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="2b694-154">RELATED LINKS</span></span>

[<span data-ttu-id="2b694-155">Azure SQL 資料庫</span><span class="sxs-lookup"><span data-stu-id="2b694-155">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="2b694-156">匯入資料庫</span><span class="sxs-lookup"><span data-stu-id="2b694-156">Import Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn781284.aspx)

[<span data-ttu-id="2b694-157">Azure SQL 資料庫的作業</span><span class="sxs-lookup"><span data-stu-id="2b694-157">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="2b694-158">AzureSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="2b694-158">Get-AzureSqlDatabaseImportExportStatus</span></span>](./Get-AzureSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="2b694-159">開始-AzureSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="2b694-159">Start-AzureSqlDatabaseExport</span></span>](./Start-AzureSqlDatabaseExport.md)


