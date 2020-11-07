---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 4661C479-6E3B-425D-B9D2-B36D7A83130C
online version: ''
schema: 2.0.0
ms.openlocfilehash: c3c55ebd22337a8078f3ae495b3901317f4201e0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967740"
---
# <span data-ttu-id="e9bf7-101">Get-AzureSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="e9bf7-101">Get-AzureSqlDatabaseImportExportStatus</span></span>

## <span data-ttu-id="e9bf7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e9bf7-102">SYNOPSIS</span></span>
<span data-ttu-id="e9bf7-103">取得匯入或匯出要求的狀態。</span><span class="sxs-lookup"><span data-stu-id="e9bf7-103">Gets the status of an import or export request.</span></span>

## <span data-ttu-id="e9bf7-104">句法</span><span class="sxs-lookup"><span data-stu-id="e9bf7-104">SYNTAX</span></span>

### <span data-ttu-id="e9bf7-105">ByConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="e9bf7-105">ByConnectionInfo</span></span>
```
Get-AzureSqlDatabaseImportExportStatus -Username <String> -Password <String> -ServerName <String>
 -RequestId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e9bf7-106">ByRequestObject</span><span class="sxs-lookup"><span data-stu-id="e9bf7-106">ByRequestObject</span></span>
```
Get-AzureSqlDatabaseImportExportStatus -Request <ImportExportRequest> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="e9bf7-107">說明</span><span class="sxs-lookup"><span data-stu-id="e9bf7-107">DESCRIPTION</span></span>
<span data-ttu-id="e9bf7-108">**AzureSqlDatabaseImportExportStatus** Cmdlet 會取得匯入或匯出要求的狀態。</span><span class="sxs-lookup"><span data-stu-id="e9bf7-108">The **Get-AzureSqlDatabaseImportExportStatus** cmdlet gets the status of an import or export request.</span></span>
<span data-ttu-id="e9bf7-109">Start-AzureSqlDatabaseImport 或 Start-AzureSqlDatabaseExport Cmdlet 會啟動要求。</span><span class="sxs-lookup"><span data-stu-id="e9bf7-109">The Start-AzureSqlDatabaseImport or Start-AzureSqlDatabaseExport cmdlet initiates requests.</span></span>
<span data-ttu-id="e9bf7-110">您可以使用 *request* 參數指定 request 物件，或者您可以使用 *RequestId* 參數以及使用者名稱、 *密碼* 及 *ServerName* 參數來識別 *Username* 要求。</span><span class="sxs-lookup"><span data-stu-id="e9bf7-110">You can specify the request object by using the *Request* parameter, or you can identify the request by using the *RequestId* parameter and the *Username* , *Password* , and *ServerName* parameters.</span></span>

## <span data-ttu-id="e9bf7-111">示例</span><span class="sxs-lookup"><span data-stu-id="e9bf7-111">EXAMPLES</span></span>

### <span data-ttu-id="e9bf7-112">範例1：取得匯出要求的狀態</span><span class="sxs-lookup"><span data-stu-id="e9bf7-112">Example 1: Get the status of an export request</span></span>
```
PS C:\> $ExportRequest = Start-AzureSqlDatabaseExport -SqlConnectionContext $SqlContext -StorageContainer $Container -DatabaseName $DatabaseName -BlobName $BlobName
PS C:\> Get-AzureSqlDatabaseImportExportStatus -Request $ExportRequest
```

<span data-ttu-id="e9bf7-113">第一個命令會建立匯出要求，然後將它儲存在 $ExportRequest 變數中。</span><span class="sxs-lookup"><span data-stu-id="e9bf7-113">The first command creates an export request, and then stores it in the $ExportRequest variable.</span></span>

<span data-ttu-id="e9bf7-114">第二個命令會取得儲存在 $ExportRequest 中之匯出要求的狀態。</span><span class="sxs-lookup"><span data-stu-id="e9bf7-114">The second command gets the status of the export request stored in $ExportRequest.</span></span>

## <span data-ttu-id="e9bf7-115">參數</span><span class="sxs-lookup"><span data-stu-id="e9bf7-115">PARAMETERS</span></span>

### <span data-ttu-id="e9bf7-116">-Password</span><span class="sxs-lookup"><span data-stu-id="e9bf7-116">-Password</span></span>
<span data-ttu-id="e9bf7-117">指定連接至 Azure SQL Database server 所需的密碼。</span><span class="sxs-lookup"><span data-stu-id="e9bf7-117">Specifies the password that is required to connect to the Azure SQL Database server.</span></span>
<span data-ttu-id="e9bf7-118">如果您指定的是 *RequestId* 參數，您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="e9bf7-118">You must specify this parameter if you specified the *RequestId* parameter.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9bf7-119">-設定檔</span><span class="sxs-lookup"><span data-stu-id="e9bf7-119">-Profile</span></span>
<span data-ttu-id="e9bf7-120">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="e9bf7-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e9bf7-121">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="e9bf7-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e9bf7-122">-要求</span><span class="sxs-lookup"><span data-stu-id="e9bf7-122">-Request</span></span>
<span data-ttu-id="e9bf7-123">指定 **ImportExportRequest** 物件。</span><span class="sxs-lookup"><span data-stu-id="e9bf7-123">Specifies an **ImportExportRequest** object.</span></span>
<span data-ttu-id="e9bf7-124">若要取得匯入或匯出要求物件，請使用 Start-AzureSqlDatabaseImport 或 Start-AzureSqlDatabaseExport Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e9bf7-124">To obtain an import or export request object, use the Start-AzureSqlDatabaseImport or Start-AzureSqlDatabaseExport cmdlet.</span></span>

```yaml
Type: ImportExportRequest
Parameter Sets: ByRequestObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9bf7-125">-RequestId</span><span class="sxs-lookup"><span data-stu-id="e9bf7-125">-RequestId</span></span>
<span data-ttu-id="e9bf7-126">指定此 Cmdlet 取得狀態的匯入或匯出作業的 GUID。</span><span class="sxs-lookup"><span data-stu-id="e9bf7-126">Specifies the GUID of the import or export operation for which this cmdlet gets status.</span></span>
<span data-ttu-id="e9bf7-127">如果您指定此 *參數，您* 必須指定使用者名稱、 *密碼* 和 *ServerName* 參數。</span><span class="sxs-lookup"><span data-stu-id="e9bf7-127">If you specify this parameter, you must specify the *UserName* , *Password* , and *ServerName* parameters.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9bf7-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e9bf7-128">-ServerName</span></span>
<span data-ttu-id="e9bf7-129">指定 Azure SQL 資料庫伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="e9bf7-129">Specifies the name of the Azure SQL Database server.</span></span>
<span data-ttu-id="e9bf7-130">如果您指定的是 *RequestId* 參數，您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="e9bf7-130">You must specify this parameter if you specified the *RequestId* parameter.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9bf7-131">-Username</span><span class="sxs-lookup"><span data-stu-id="e9bf7-131">-Username</span></span>
<span data-ttu-id="e9bf7-132">指定連接至 Azure SQL Database server 所需的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="e9bf7-132">Specifies the user name required to connect to the Azure SQL Database server.</span></span>
<span data-ttu-id="e9bf7-133">如果您指定的是 *RequestId* 參數，您必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="e9bf7-133">You must specify this parameter if you specified the *RequestId* parameter.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9bf7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9bf7-134">CommonParameters</span></span>
<span data-ttu-id="e9bf7-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e9bf7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9bf7-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e9bf7-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9bf7-137">輸入</span><span class="sxs-lookup"><span data-stu-id="e9bf7-137">INPUTS</span></span>

## <span data-ttu-id="e9bf7-138">輸出</span><span class="sxs-lookup"><span data-stu-id="e9bf7-138">OUTPUTS</span></span>

### <span data-ttu-id="e9bf7-139">ImportExport. StatusInfo （WindowsAzure） SqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e9bf7-139">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.ImportExport.StatusInfo</span></span>

## <span data-ttu-id="e9bf7-140">筆記</span><span class="sxs-lookup"><span data-stu-id="e9bf7-140">NOTES</span></span>

## <span data-ttu-id="e9bf7-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="e9bf7-141">RELATED LINKS</span></span>

[<span data-ttu-id="e9bf7-142">Azure SQL 資料庫</span><span class="sxs-lookup"><span data-stu-id="e9bf7-142">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="e9bf7-143">取得匯入匯出資料庫狀態</span><span class="sxs-lookup"><span data-stu-id="e9bf7-143">Get Import Export Database Status</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn781289.aspx)

[<span data-ttu-id="e9bf7-144">Azure SQL 資料庫的作業</span><span class="sxs-lookup"><span data-stu-id="e9bf7-144">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="e9bf7-145">開始-AzureSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="e9bf7-145">Start-AzureSqlDatabaseExport</span></span>](./Start-AzureSqlDatabaseExport.md)

[<span data-ttu-id="e9bf7-146">開始-AzureSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="e9bf7-146">Start-AzureSqlDatabaseImport</span></span>](./Start-AzureSqlDatabaseImport.md)


