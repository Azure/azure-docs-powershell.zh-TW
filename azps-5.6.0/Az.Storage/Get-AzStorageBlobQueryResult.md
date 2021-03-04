---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/Az.storage/get-azstorageblobqueryresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobQueryResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobQueryResult.md
ms.openlocfilehash: 7a790610d9ff3334494276eee7bb85af5b9ba3fc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915130"
---
# <span data-ttu-id="93118-101">Get-AzStorageBlobQueryResult</span><span class="sxs-lookup"><span data-stu-id="93118-101">Get-AzStorageBlobQueryResult</span></span>

## <span data-ttu-id="93118-102">簡介</span><span class="sxs-lookup"><span data-stu-id="93118-102">SYNOPSIS</span></span>
<span data-ttu-id="93118-103">在 blob 的內容上 (SQL) SQL 查詢語言，並僅將資料查詢子集儲存至本地檔案。</span><span class="sxs-lookup"><span data-stu-id="93118-103">Applies a simple Structured Query Language (SQL) statement on a blob's contents and save only the queried subset of the data to a local file.</span></span>

## <span data-ttu-id="93118-104">語法</span><span class="sxs-lookup"><span data-stu-id="93118-104">SYNTAX</span></span>

### <span data-ttu-id="93118-105">NamePipeline (預設) </span><span class="sxs-lookup"><span data-stu-id="93118-105">NamePipeline (Default)</span></span>
```
Get-AzStorageBlobQueryResult [-Blob] <String> [-Container] <String> [-SnapshotTime <DateTimeOffset>]
 [-VersionId <String>] -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="93118-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="93118-106">BlobPipeline</span></span>
```
Get-AzStorageBlobQueryResult -BlobBaseClient <BlobBaseClient> -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="93118-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="93118-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobQueryResult -BlobContainerClient <BlobContainerClient> [-Blob] <String>
 [-SnapshotTime <DateTimeOffset>] [-VersionId <String>] -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="93118-108">描述</span><span class="sxs-lookup"><span data-stu-id="93118-108">DESCRIPTION</span></span>
<span data-ttu-id="93118-109">**Get-AzStorageBlobQueryResult** Cmdlet 會針對 Blob 的內容，將簡單的結構化查詢語言 (SQL) 語句，並儲存查詢的資料子集至本地檔案。</span><span class="sxs-lookup"><span data-stu-id="93118-109">The **Get-AzStorageBlobQueryResult** cmdlet applies a simple Structured Query Language (SQL) statement on a blob's contents and save the queried subset of the data to a local file.</span></span>

## <span data-ttu-id="93118-110">例子</span><span class="sxs-lookup"><span data-stu-id="93118-110">EXAMPLES</span></span>

### <span data-ttu-id="93118-111">範例 1：查詢 Blob</span><span class="sxs-lookup"><span data-stu-id="93118-111">Example 1: Query a blob</span></span>
```powershell
PS C:\> $inputconfig = New-AzStorageBlobQueryConfig -AsCsv -HasHeader

PS C:\> $outputconfig = New-AzStorageBlobQueryConfig -AsJson

PS C:\> $queryString = "SELECT * FROM BlobStorage WHERE Name = 'a'"

PS C:\> $result = Get-AzStorageBlobQueryResult -Container $containerName -Blob $blobName -QueryString $queryString -ResultFile "c:\resultfile.json" -InputTextConfiguration $inputconfig -OutputTextConfiguration $outputconfig -Context $ctx

PS C:\> $result

BytesScanned FailureCount BlobQueryError
------------ ------------ --------------
         449            0
```

<span data-ttu-id="93118-112">此命令會以 csv 的輸入方式查詢 blob 處理，並輸出 config 為 json，並儲存輸出到「c:\resultfile.js」。</span><span class="sxs-lookup"><span data-stu-id="93118-112">This command querys a blob succsssfully with input config as csv, and output config as json, and save the output to local file "c:\resultfile.json".</span></span>

### <span data-ttu-id="93118-113">範例 2：查詢 Blob 快照</span><span class="sxs-lookup"><span data-stu-id="93118-113">Example 2: Query a blob snapshot</span></span>
```powershell
PS C:\> $blob = Get-AzStorageBlob -Container $containerName -Blob $blobName -SnapshotTime "2020-07-29T11:08:21.1097874Z" -Context $ctx

PS C:\> $inputconfig = New-AzStorageBlobQueryConfig -AsCsv -ColumnSeparator "," -QuotationCharacter """" -EscapeCharacter "\" -RecordSeparator "`n" -HasHeader

PS C:\> $outputconfig = New-AzStorageBlobQueryConfig -AsJson -RecordSeparator "`n" 

PS C:\> $queryString = "SELECT * FROM BlobStorage WHERE _1 LIKE '1%%'"

PS C:\> $result = $blob | Get-AzStorageBlobQueryResult -QueryString $queryString -ResultFile $localFilePath -InputTextConfiguration $inputconfig -OutputTextConfiguration $outputconfig

PS C:\> $result

BytesScanned FailureCount BlobQueryError
------------ ------------ --------------
   187064971            1 {ParseError}  



PS C:\> $result.BlobQueryError

Name       Description                                                   IsFatal Position
----       -----------                                                   ------- --------
ParseError Unexpected token '1' at [byte: 3077737]. Expecting token ','.    True  7270632
```

<span data-ttu-id="93118-114">此命令會先取得 Blob 快照的 Blob 物件，然後查詢 Blob 快照，然後顯示結果包含查詢錯誤。</span><span class="sxs-lookup"><span data-stu-id="93118-114">This command first gets a blob object for blob snapshot, then queries the blob snapshot and show the result include query error.</span></span>

## <span data-ttu-id="93118-115">參數</span><span class="sxs-lookup"><span data-stu-id="93118-115">PARAMETERS</span></span>

### <span data-ttu-id="93118-116">-Blob</span><span class="sxs-lookup"><span data-stu-id="93118-116">-Blob</span></span>
<span data-ttu-id="93118-117">Blob 名稱</span><span class="sxs-lookup"><span data-stu-id="93118-117">Blob name</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93118-118">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="93118-118">-BlobBaseClient</span></span>
<span data-ttu-id="93118-119">BlobBaseClient 物件</span><span class="sxs-lookup"><span data-stu-id="93118-119">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93118-120">-BlobContainerClient</span><span class="sxs-lookup"><span data-stu-id="93118-120">-BlobContainerClient</span></span>
<span data-ttu-id="93118-121">BlobContainerClient 物件</span><span class="sxs-lookup"><span data-stu-id="93118-121">BlobContainerClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.BlobContainerClient
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93118-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="93118-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="93118-123">用戶端會針對每個要求的最大執行時間 ，以碼錶示。</span><span class="sxs-lookup"><span data-stu-id="93118-123">The client side maximum execution time for each request in seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93118-124">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="93118-124">-ConcurrentTaskCount</span></span>
<span data-ttu-id="93118-125">同時同步處理工作的總數量。</span><span class="sxs-lookup"><span data-stu-id="93118-125">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="93118-126">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="93118-126">The default value is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93118-127">-Container</span><span class="sxs-lookup"><span data-stu-id="93118-127">-Container</span></span>
<span data-ttu-id="93118-128">容器名稱</span><span class="sxs-lookup"><span data-stu-id="93118-128">Container name</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93118-129">-內容</span><span class="sxs-lookup"><span data-stu-id="93118-129">-Context</span></span>
<span data-ttu-id="93118-130">Azure 儲存體內容物件</span><span class="sxs-lookup"><span data-stu-id="93118-130">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93118-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93118-131">-DefaultProfile</span></span>
<span data-ttu-id="93118-132">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="93118-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93118-133">-強制</span><span class="sxs-lookup"><span data-stu-id="93118-133">-Force</span></span>
<span data-ttu-id="93118-134">強制覆寫現有的檔案。</span><span class="sxs-lookup"><span data-stu-id="93118-134">Force to overwrite the existing file.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93118-135">-InputTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="93118-135">-InputTextConfiguration</span></span>
<span data-ttu-id="93118-136">用來處理查詢輸入文字的組配置。</span><span class="sxs-lookup"><span data-stu-id="93118-136">The configuration used to handled the query input text.</span></span> <span data-ttu-id="93118-137">使用 New-AzStorageBlobQueryConfig 建立組組物件。</span><span class="sxs-lookup"><span data-stu-id="93118-137">Create configuration object the with New-AzStorageBlobQueryConfig.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93118-138">-OutputTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="93118-138">-OutputTextConfiguration</span></span>
<span data-ttu-id="93118-139">用來處理查詢輸出文字的組配置。</span><span class="sxs-lookup"><span data-stu-id="93118-139">The configuration used to handled the query output text.</span></span> <span data-ttu-id="93118-140">使用 New-AzStorageBlobQueryConfig 建立組組物件。</span><span class="sxs-lookup"><span data-stu-id="93118-140">Create configuration object the with New-AzStorageBlobQueryConfig.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93118-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="93118-141">-PassThru</span></span>
<span data-ttu-id="93118-142">返回指定的 Blob 是否已成功查詢。</span><span class="sxs-lookup"><span data-stu-id="93118-142">Return whether the specified blob is successfully queried.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93118-143">-QueryString</span><span class="sxs-lookup"><span data-stu-id="93118-143">-QueryString</span></span>
<span data-ttu-id="93118-144">查詢字串，請參閱以下位置的更多詳細資料： https://docs.microsoft.com/azure/storage/blobs/query-acceleration-sql-reference</span><span class="sxs-lookup"><span data-stu-id="93118-144">Query string, see more details in: https://docs.microsoft.com/azure/storage/blobs/query-acceleration-sql-reference</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93118-145">-ResultFile</span><span class="sxs-lookup"><span data-stu-id="93118-145">-ResultFile</span></span>
<span data-ttu-id="93118-146">儲存查詢結果的本地檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="93118-146">Local file path to save the query result.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93118-147">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="93118-147">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="93118-148">伺服器會在每個要求中以碼錶示時間。</span><span class="sxs-lookup"><span data-stu-id="93118-148">The server time out for each request in seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93118-149">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="93118-149">-SnapshotTime</span></span>
<span data-ttu-id="93118-150">Blob 快照時間</span><span class="sxs-lookup"><span data-stu-id="93118-150">Blob SnapshotTime</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93118-151">-VersionId</span><span class="sxs-lookup"><span data-stu-id="93118-151">-VersionId</span></span>
<span data-ttu-id="93118-152">Blob VersionId</span><span class="sxs-lookup"><span data-stu-id="93118-152">Blob VersionId</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93118-153">-確認</span><span class="sxs-lookup"><span data-stu-id="93118-153">-Confirm</span></span>
<span data-ttu-id="93118-154">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="93118-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93118-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93118-155">-WhatIf</span></span>
<span data-ttu-id="93118-156">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="93118-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93118-157">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="93118-157">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93118-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93118-158">CommonParameters</span></span>
<span data-ttu-id="93118-159">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="93118-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93118-160">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="93118-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93118-161">輸入</span><span class="sxs-lookup"><span data-stu-id="93118-161">INPUTS</span></span>

### <span data-ttu-id="93118-162">Azure.storage.Blobs.Specialized.BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="93118-162">Azure.Storage.Blobs.Specialized.BlobBaseClient</span></span>

### <span data-ttu-id="93118-163">Azure.storage.Blobs.BlobContainerClient</span><span class="sxs-lookup"><span data-stu-id="93118-163">Azure.Storage.Blobs.BlobContainerClient</span></span>

### <span data-ttu-id="93118-164">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="93118-164">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="93118-165">輸出</span><span class="sxs-lookup"><span data-stu-id="93118-165">OUTPUTS</span></span>

### <span data-ttu-id="93118-166">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="93118-166">System.Boolean</span></span>

## <span data-ttu-id="93118-167">筆記</span><span class="sxs-lookup"><span data-stu-id="93118-167">NOTES</span></span>

## <span data-ttu-id="93118-168">相關連結</span><span class="sxs-lookup"><span data-stu-id="93118-168">RELATED LINKS</span></span>
