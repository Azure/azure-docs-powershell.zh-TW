---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/get-azstorageblobqueryresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobQueryResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobQueryResult.md
ms.openlocfilehash: fbb1c8e4e2a5421ea7714a0d7a82b1f1cc2567f1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93968976"
---
# <span data-ttu-id="189df-101">Get-AzStorageBlobQueryResult</span><span class="sxs-lookup"><span data-stu-id="189df-101">Get-AzStorageBlobQueryResult</span></span>

## <span data-ttu-id="189df-102">摘要</span><span class="sxs-lookup"><span data-stu-id="189df-102">SYNOPSIS</span></span>
<span data-ttu-id="189df-103">在 blob 內容 (SQL) 語句中套用簡單的結構化查詢語言，只將資料的已查詢子集儲存至本機檔案。</span><span class="sxs-lookup"><span data-stu-id="189df-103">Applies a simple Structured Query Language (SQL) statement on a blob's contents and save only the queried subset of the data to a local file.</span></span>

## <span data-ttu-id="189df-104">句法</span><span class="sxs-lookup"><span data-stu-id="189df-104">SYNTAX</span></span>

### <span data-ttu-id="189df-105">NamePipeline (預設) </span><span class="sxs-lookup"><span data-stu-id="189df-105">NamePipeline (Default)</span></span>
```
Get-AzStorageBlobQueryResult [-Blob] <String> [-Container] <String> [-SnapshotTime <DateTimeOffset>]
 [-VersionId <String>] -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="189df-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="189df-106">BlobPipeline</span></span>
```
Get-AzStorageBlobQueryResult -BlobBaseClient <BlobBaseClient> -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="189df-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="189df-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobQueryResult -BlobContainerClient <BlobContainerClient> [-Blob] <String>
 [-SnapshotTime <DateTimeOffset>] [-VersionId <String>] -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="189df-108">說明</span><span class="sxs-lookup"><span data-stu-id="189df-108">DESCRIPTION</span></span>
<span data-ttu-id="189df-109">**AzStorageBlobQueryResult** Cmdlet 會在 blob 內容的 SQL) 語句中套用簡單的結構化查詢語言 (，並將所查詢的資料子集儲存至本機檔案。</span><span class="sxs-lookup"><span data-stu-id="189df-109">The **Get-AzStorageBlobQueryResult** cmdlet applies a simple Structured Query Language (SQL) statement on a blob's contents and save the queried subset of the data to a local file.</span></span>

## <span data-ttu-id="189df-110">示例</span><span class="sxs-lookup"><span data-stu-id="189df-110">EXAMPLES</span></span>

### <span data-ttu-id="189df-111">範例1：查詢 blob</span><span class="sxs-lookup"><span data-stu-id="189df-111">Example 1: Query a blob</span></span>
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

<span data-ttu-id="189df-112">這個命令 querys 將輸入配置為 csv 的 blob succsssfully，並將輸出配置為 json，並將輸出儲存至本機檔案 "c:\resultfile.json"。</span><span class="sxs-lookup"><span data-stu-id="189df-112">This command querys a blob succsssfully with input config as csv, and output config as json, and save the output to local file "c:\resultfile.json".</span></span>

### <span data-ttu-id="189df-113">範例2：查詢 blob 快照</span><span class="sxs-lookup"><span data-stu-id="189df-113">Example 2: Query a blob snapshot</span></span>
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

<span data-ttu-id="189df-114">這個命令會先取得 blob 快照的 blob 物件，然後查詢 blob 快照，並顯示結果包含查詢錯誤。</span><span class="sxs-lookup"><span data-stu-id="189df-114">This command first gets a blob object for blob snapshot, then queries the blob snapshot and show the result include query error.</span></span>

## <span data-ttu-id="189df-115">參數</span><span class="sxs-lookup"><span data-stu-id="189df-115">PARAMETERS</span></span>

### <span data-ttu-id="189df-116">-Blob</span><span class="sxs-lookup"><span data-stu-id="189df-116">-Blob</span></span>
<span data-ttu-id="189df-117">Blob 名稱</span><span class="sxs-lookup"><span data-stu-id="189df-117">Blob name</span></span>

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

### <span data-ttu-id="189df-118">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="189df-118">-BlobBaseClient</span></span>
<span data-ttu-id="189df-119">BlobBaseClient 物件</span><span class="sxs-lookup"><span data-stu-id="189df-119">BlobBaseClient Object</span></span>

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

### <span data-ttu-id="189df-120">-BlobContainerClient</span><span class="sxs-lookup"><span data-stu-id="189df-120">-BlobContainerClient</span></span>
<span data-ttu-id="189df-121">BlobContainerClient 物件</span><span class="sxs-lookup"><span data-stu-id="189df-121">BlobContainerClient Object</span></span>

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

### <span data-ttu-id="189df-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="189df-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="189df-123">用戶端每個要求的最大執行時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="189df-123">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="189df-124">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="189df-124">-ConcurrentTaskCount</span></span>
<span data-ttu-id="189df-125">並行非同步工作的總數量。</span><span class="sxs-lookup"><span data-stu-id="189df-125">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="189df-126">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="189df-126">The default value is 10.</span></span>

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

### <span data-ttu-id="189df-127">-容器</span><span class="sxs-lookup"><span data-stu-id="189df-127">-Container</span></span>
<span data-ttu-id="189df-128">容器名稱</span><span class="sxs-lookup"><span data-stu-id="189df-128">Container name</span></span>

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

### <span data-ttu-id="189df-129">-內容</span><span class="sxs-lookup"><span data-stu-id="189df-129">-Context</span></span>
<span data-ttu-id="189df-130">Azure 儲存區內容物件</span><span class="sxs-lookup"><span data-stu-id="189df-130">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="189df-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="189df-131">-DefaultProfile</span></span>
<span data-ttu-id="189df-132">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="189df-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="189df-133">-Force</span><span class="sxs-lookup"><span data-stu-id="189df-133">-Force</span></span>
<span data-ttu-id="189df-134">強制覆寫現有的檔案。</span><span class="sxs-lookup"><span data-stu-id="189df-134">Force to overwrite the existing file.</span></span>

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

### <span data-ttu-id="189df-135">-InputTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="189df-135">-InputTextConfiguration</span></span>
<span data-ttu-id="189df-136">用來處理查詢輸入文字的配置。</span><span class="sxs-lookup"><span data-stu-id="189df-136">The configuration used to handled the query input text.</span></span> <span data-ttu-id="189df-137">使用新的-AzStorageBlobQueryConfig 建立 configuration 物件。</span><span class="sxs-lookup"><span data-stu-id="189df-137">Create configuration object the with New-AzStorageBlobQueryConfig.</span></span>

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

### <span data-ttu-id="189df-138">-OutputTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="189df-138">-OutputTextConfiguration</span></span>
<span data-ttu-id="189df-139">用來處理查詢輸出文字的配置。</span><span class="sxs-lookup"><span data-stu-id="189df-139">The configuration used to handled the query output text.</span></span> <span data-ttu-id="189df-140">使用新的-AzStorageBlobQueryConfig 建立 configuration 物件。</span><span class="sxs-lookup"><span data-stu-id="189df-140">Create configuration object the with New-AzStorageBlobQueryConfig.</span></span>

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

### <span data-ttu-id="189df-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="189df-141">-PassThru</span></span>
<span data-ttu-id="189df-142">返回是否已成功查詢指定的 blob。</span><span class="sxs-lookup"><span data-stu-id="189df-142">Return whether the specified blob is successfully queried.</span></span>

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

### <span data-ttu-id="189df-143">-QueryString</span><span class="sxs-lookup"><span data-stu-id="189df-143">-QueryString</span></span>
<span data-ttu-id="189df-144">查詢字串，請參閱以下內容中的詳細資料： https://docs.microsoft.com/en-us/azure/storage/blobs/query-acceleration-sql-reference</span><span class="sxs-lookup"><span data-stu-id="189df-144">Query string, see more details in: https://docs.microsoft.com/en-us/azure/storage/blobs/query-acceleration-sql-reference</span></span>

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

### <span data-ttu-id="189df-145">-ResultFile</span><span class="sxs-lookup"><span data-stu-id="189df-145">-ResultFile</span></span>
<span data-ttu-id="189df-146">儲存查詢結果的本機檔路徑。</span><span class="sxs-lookup"><span data-stu-id="189df-146">Local file path to save the query result.</span></span>

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

### <span data-ttu-id="189df-147">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="189df-147">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="189df-148">伺服器針對每個要求的超時時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="189df-148">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="189df-149">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="189df-149">-SnapshotTime</span></span>
<span data-ttu-id="189df-150">Blob SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="189df-150">Blob SnapshotTime</span></span>

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

### <span data-ttu-id="189df-151">-VersionId</span><span class="sxs-lookup"><span data-stu-id="189df-151">-VersionId</span></span>
<span data-ttu-id="189df-152">Blob VersionId</span><span class="sxs-lookup"><span data-stu-id="189df-152">Blob VersionId</span></span>

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

### <span data-ttu-id="189df-153">-確認</span><span class="sxs-lookup"><span data-stu-id="189df-153">-Confirm</span></span>
<span data-ttu-id="189df-154">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="189df-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="189df-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="189df-155">-WhatIf</span></span>
<span data-ttu-id="189df-156">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="189df-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="189df-157">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="189df-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="189df-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="189df-158">CommonParameters</span></span>
<span data-ttu-id="189df-159">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="189df-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="189df-160">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="189df-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="189df-161">輸入</span><span class="sxs-lookup"><span data-stu-id="189df-161">INPUTS</span></span>

### <span data-ttu-id="189df-162">BlobBaseClient 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="189df-162">Azure.Storage.Blobs.Specialized.BlobBaseClient</span></span>

### <span data-ttu-id="189df-163">BlobContainerClient 的存儲 Blob</span><span class="sxs-lookup"><span data-stu-id="189df-163">Azure.Storage.Blobs.BlobContainerClient</span></span>

### <span data-ttu-id="189df-164">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="189df-164">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="189df-165">輸出</span><span class="sxs-lookup"><span data-stu-id="189df-165">OUTPUTS</span></span>

### <span data-ttu-id="189df-166">System.object</span><span class="sxs-lookup"><span data-stu-id="189df-166">System.Boolean</span></span>

## <span data-ttu-id="189df-167">筆記</span><span class="sxs-lookup"><span data-stu-id="189df-167">NOTES</span></span>

## <span data-ttu-id="189df-168">相關連結</span><span class="sxs-lookup"><span data-stu-id="189df-168">RELATED LINKS</span></span>
