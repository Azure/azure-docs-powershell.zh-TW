---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E54BFD3A-CD54-4E6B-9574-92B8D3E88FF3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlob.md
ms.openlocfilehash: 44c14b1f5aa8426bfb78205fa66a53d7db7e3440
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126726"
---
# <span data-ttu-id="2fd02-101">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="2fd02-101">Get-AzStorageBlob</span></span>

## <span data-ttu-id="2fd02-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2fd02-102">SYNOPSIS</span></span>
<span data-ttu-id="2fd02-103">列出容器中的 blob。</span><span class="sxs-lookup"><span data-stu-id="2fd02-103">Lists blobs in a container.</span></span>

## <span data-ttu-id="2fd02-104">句法</span><span class="sxs-lookup"><span data-stu-id="2fd02-104">SYNTAX</span></span>

### <span data-ttu-id="2fd02-105">BlobName (預設) </span><span class="sxs-lookup"><span data-stu-id="2fd02-105">BlobName (Default)</span></span>
```
Get-AzStorageBlob [[-Blob] <String>] [-Container] <String> [-IncludeDeleted] [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="2fd02-106">SingleBlobSnapshotTime</span><span class="sxs-lookup"><span data-stu-id="2fd02-106">SingleBlobSnapshotTime</span></span>
```
Get-AzStorageBlob [-Blob] <String> [-Container] <String> [-IncludeDeleted] -SnapshotTime <DateTimeOffset>
 [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="2fd02-107">SingleBlobVersionID</span><span class="sxs-lookup"><span data-stu-id="2fd02-107">SingleBlobVersionID</span></span>
```
Get-AzStorageBlob [-Blob] <String> [-Container] <String> [-IncludeDeleted] -VersionId <String>
 [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="2fd02-108">BlobPrefix</span><span class="sxs-lookup"><span data-stu-id="2fd02-108">BlobPrefix</span></span>
```
Get-AzStorageBlob [-Prefix <String>] [-Container] <String> [-IncludeDeleted] [-IncludeVersion]
 [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="2fd02-109">說明</span><span class="sxs-lookup"><span data-stu-id="2fd02-109">DESCRIPTION</span></span>
<span data-ttu-id="2fd02-110">**AzStorageBlob** Cmdlet 會在 Azure 儲存空間帳戶的指定容器中列出 blob。</span><span class="sxs-lookup"><span data-stu-id="2fd02-110">The **Get-AzStorageBlob** cmdlet lists blobs in the specified container in an Azure storage account.</span></span>

## <span data-ttu-id="2fd02-111">示例</span><span class="sxs-lookup"><span data-stu-id="2fd02-111">EXAMPLES</span></span>

### <span data-ttu-id="2fd02-112">範例1：透過 blob 名稱取得 blob</span><span class="sxs-lookup"><span data-stu-id="2fd02-112">Example 1: Get a blob by blob name</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Blob blob*
```

<span data-ttu-id="2fd02-113">這個命令使用 blob 名稱和萬用字元來取得 blob。</span><span class="sxs-lookup"><span data-stu-id="2fd02-113">This command uses a blob name and wildcard to get a blob.</span></span>

### <span data-ttu-id="2fd02-114">範例2：使用管線在容器中取得 blob</span><span class="sxs-lookup"><span data-stu-id="2fd02-114">Example 2: Get blobs in a container by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Name container* | Get-AzStorageBlob -IncludeDeleted

   Container Uri: https://storageaccountname.blob.core.windows.net/container1

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime         IsDeleted 
----                 --------  ------          -----------                    ------------         ---------- ------------         --------- 
test1                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:19Z            2017-11-08 08:19:32Z True      
test1                BlockBlob 403116          application/octet-stream       2017-11-08 09:00:29Z                                 True      
test2                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:00Z                                 False
```

<span data-ttu-id="2fd02-115">這個命令會使用管線來取得所有 blob (在容器中的 [刪除狀態]) 中包含 blob。</span><span class="sxs-lookup"><span data-stu-id="2fd02-115">This command uses the pipeline to get all blobs (include blobs in Deleted status) in a container.</span></span>

### <span data-ttu-id="2fd02-116">範例3：透過名稱首碼取得 blob</span><span class="sxs-lookup"><span data-stu-id="2fd02-116">Example 3: Get blobs by name prefix</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Prefix "blob"
```

<span data-ttu-id="2fd02-117">這個命令會使用名稱首碼來取得 blob。</span><span class="sxs-lookup"><span data-stu-id="2fd02-117">This command uses a name prefix to get blobs.</span></span>

### <span data-ttu-id="2fd02-118">範例4：多個批次中的清單 blob</span><span class="sxs-lookup"><span data-stu-id="2fd02-118">Example 4: List blobs in multiple batches</span></span>
```
PS C:\>$MaxReturn = 10000
PS C:\> $ContainerName = "abc"
PS C:\> $Total = 0
PS C:\> $Token = $Null
PS C:\> do
 {
     $Blobs = Get-AzStorageBlob -Container $ContainerName -MaxCount $MaxReturn  -ContinuationToken $Token
     $Total += $Blobs.Count
     if($Blobs.Length -le 0) { Break;}
     $Token = $Blobs[$blobs.Count -1].ContinuationToken;
 }
 While ($Token -ne $Null)
PS C:\> Echo "Total $Total blobs in container $ContainerName"
```

<span data-ttu-id="2fd02-119">這個範例使用 *MaxCount* 和 *ContinuationToken* 參數，以多個批次列出 Azure 存儲區 blob。</span><span class="sxs-lookup"><span data-stu-id="2fd02-119">This example uses the *MaxCount* and *ContinuationToken* parameters to list Azure Storage blobs in multiple batches.</span></span>
<span data-ttu-id="2fd02-120">前四個命令會將值指派給要在範例中使用的變數。</span><span class="sxs-lookup"><span data-stu-id="2fd02-120">The first four commands assign values to variables to use in the example.</span></span>
<span data-ttu-id="2fd02-121">第五個命令指定一個 **Do** 語句，該語句使用 **AzStorageBlob** Cmdlet 來取得 blob。</span><span class="sxs-lookup"><span data-stu-id="2fd02-121">The fifth command specifies a **Do-While** statement that uses the **Get-AzStorageBlob** cmdlet to get blobs.</span></span>
<span data-ttu-id="2fd02-122">該語句包含儲存在 $Token 變數中的延續標記。</span><span class="sxs-lookup"><span data-stu-id="2fd02-122">The statement includes the continuation token stored in the $Token variable.</span></span>
<span data-ttu-id="2fd02-123">在迴圈執行時 $Token 變更值。</span><span class="sxs-lookup"><span data-stu-id="2fd02-123">$Token changes value as the loop runs.</span></span>
<span data-ttu-id="2fd02-124">如需詳細資訊，請輸入 `Get-Help About_Do` 。</span><span class="sxs-lookup"><span data-stu-id="2fd02-124">For more information, type `Get-Help About_Do`.</span></span>
<span data-ttu-id="2fd02-125">最後一個命令會使用 **Echo** 命令來顯示合計。</span><span class="sxs-lookup"><span data-stu-id="2fd02-125">The final command uses the **Echo** command to display the total.</span></span>

### <span data-ttu-id="2fd02-126">範例5：取得容器中的所有 blob （含 blob 版本）</span><span class="sxs-lookup"><span data-stu-id="2fd02-126">Example 5: Get all blobs in a container include blob version</span></span>
```
PS C:\>Get-AzStorageBlob -Container "containername"  -IncludeVersion 

   AccountName: storageaccountname, ContainerName: containername

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
blob1                BlockBlob 2097152         application/octet-stream       2020-07-06 06:56:06Z Hot                                     False      2020-07-06T06:56:06.2432658Z  
blob1                BlockBlob 2097152         application/octet-stream       2020-07-06 06:56:06Z Hot        2020-07-06T06:56:06.8588431Z False                                    
blob1                BlockBlob 2097152         application/octet-stream       2020-07-06 06:56:06Z Hot                                     False      2020-07-06T06:56:06.8598431Z *  
blob2                BlockBlob 2097152         application/octet-stream       2020-07-03 16:19:16Z Hot                                     False      2020-07-03T16:19:16.2883167Z  
blob2                BlockBlob 2097152         application/octet-stream       2020-07-03 16:19:35Z Hot                                     False      2020-07-03T16:19:35.2381110Z *
```

<span data-ttu-id="2fd02-127">這個命令會取得容器中的所有 blob，包括 blob 版本。</span><span class="sxs-lookup"><span data-stu-id="2fd02-127">This command gets all blobs in a container include blob version.</span></span>

### <span data-ttu-id="2fd02-128">範例6：取得單一 blob 版本</span><span class="sxs-lookup"><span data-stu-id="2fd02-128">Example 6: Get a single blob version</span></span>
```
PS C:\> Get-AzStorageBlob -Container "containername" -Blob blob2 -VersionId "2020-07-03T16:19:16.2883167Z" 

   AccountName: storageaccountname, ContainerName: containername

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
blob2                BlockBlob 2097152         application/octet-stream       2020-07-03 16:19:16Z Hot                                     False      2020-07-03T16:19:16.2883167Z
```

<span data-ttu-id="2fd02-129">這個命令會取得與 VersionId verion 的單一 blob。</span><span class="sxs-lookup"><span data-stu-id="2fd02-129">This command gets a single blobs verion with VersionId.</span></span>

### <span data-ttu-id="2fd02-130">範例7：取得單一 blob 快照</span><span class="sxs-lookup"><span data-stu-id="2fd02-130">Example 7: Get a single blob snapshot</span></span>
```
PS C:\> Get-AzStorageBlob -Container "containername" -Blob blob1 -SnapshotTime "2020-07-06T06:56:06.8588431Z"

   AccountName: storageaccountname, ContainerName: containername

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
blob1                BlockBlob 2097152         application/octet-stream       2020-07-06 06:56:06Z Hot        2020-07-06T06:56:06.8588431Z False
```

<span data-ttu-id="2fd02-131">這個命令會取得含有 SnapshotTime 的單一 blob 快照。</span><span class="sxs-lookup"><span data-stu-id="2fd02-131">This command gets a single blobs snapshot with SnapshotTime.</span></span>

## <span data-ttu-id="2fd02-132">參數</span><span class="sxs-lookup"><span data-stu-id="2fd02-132">PARAMETERS</span></span>

### <span data-ttu-id="2fd02-133">-Blob</span><span class="sxs-lookup"><span data-stu-id="2fd02-133">-Blob</span></span>
<span data-ttu-id="2fd02-134">指定可用於萬用字元搜尋的名稱或名稱模式。</span><span class="sxs-lookup"><span data-stu-id="2fd02-134">Specifies a name or name pattern, which can be used for a wildcard search.</span></span>
<span data-ttu-id="2fd02-135">如果未指定任何 blob 名稱，則 Cmdlet 會列出指定容器中的所有 blob。</span><span class="sxs-lookup"><span data-stu-id="2fd02-135">If no blob name is specified, the cmdlet lists all the blobs in the specified container.</span></span>
<span data-ttu-id="2fd02-136">如果為此參數指定一個值，則 Cmdlet 會列出名稱與此參數相符的所有 blob。</span><span class="sxs-lookup"><span data-stu-id="2fd02-136">If a value is specified for this parameter, the cmdlet lists all blobs with names that match this parameter.</span></span> <span data-ttu-id="2fd02-137">這個參數在字串中的任何位置都支援萬用字元。</span><span class="sxs-lookup"><span data-stu-id="2fd02-137">This parameter supports wildcards anywhere in the string.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SingleBlobSnapshotTime, SingleBlobVersionID
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fd02-138">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2fd02-138">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="2fd02-139">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="2fd02-139">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="2fd02-140">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="2fd02-140">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="2fd02-141">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="2fd02-141">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="2fd02-142">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="2fd02-142">-ConcurrentTaskCount</span></span>
<span data-ttu-id="2fd02-143">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="2fd02-143">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="2fd02-144">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="2fd02-144">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="2fd02-145">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="2fd02-145">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="2fd02-146">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="2fd02-146">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="2fd02-147">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="2fd02-147">The default value is 10.</span></span>

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

### <span data-ttu-id="2fd02-148">-容器</span><span class="sxs-lookup"><span data-stu-id="2fd02-148">-Container</span></span>
<span data-ttu-id="2fd02-149">指定容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="2fd02-149">Specifies the name of the container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fd02-150">-內容</span><span class="sxs-lookup"><span data-stu-id="2fd02-150">-Context</span></span>
<span data-ttu-id="2fd02-151">指定您想要取得其 blob 清單的 Azure 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="2fd02-151">Specifies the Azure storage account from which you want to get a list of blobs.</span></span>
<span data-ttu-id="2fd02-152">您可以使用 New-AzStorageContext Cmdlet 來建立儲存內容。</span><span class="sxs-lookup"><span data-stu-id="2fd02-152">You can use the New-AzStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="2fd02-153">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="2fd02-153">-ContinuationToken</span></span>
<span data-ttu-id="2fd02-154">指定 blob 清單的延續標記。</span><span class="sxs-lookup"><span data-stu-id="2fd02-154">Specifies a continuation token for the blob list.</span></span>
<span data-ttu-id="2fd02-155">使用此參數與 *MaxCount* 參數，在多個批次中列出 blob。</span><span class="sxs-lookup"><span data-stu-id="2fd02-155">Use this parameter and the *MaxCount* parameter to list blobs in multiple batches.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.BlobContinuationToken
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fd02-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fd02-156">-DefaultProfile</span></span>
<span data-ttu-id="2fd02-157">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2fd02-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fd02-158">-IncludeDeleted</span><span class="sxs-lookup"><span data-stu-id="2fd02-158">-IncludeDeleted</span></span>
<span data-ttu-id="2fd02-159">包含刪除的 Blob，預設的 [取得 blob] 不會包含已刪除的 blob。</span><span class="sxs-lookup"><span data-stu-id="2fd02-159">Include Deleted Blob, by default get blob won't include deleted blob.</span></span>

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

### <span data-ttu-id="2fd02-160">-IncludeVersion</span><span class="sxs-lookup"><span data-stu-id="2fd02-160">-IncludeVersion</span></span>
<span data-ttu-id="2fd02-161">只有在這個參數存在時，才會列出 Blob 版本，因此預設的 [取得 blob] 不會包含 blob 版本。</span><span class="sxs-lookup"><span data-stu-id="2fd02-161">Blob versions will be listed only if this parameter is present, by default get blob won't include blob versions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BlobPrefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fd02-162">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="2fd02-162">-MaxCount</span></span>
<span data-ttu-id="2fd02-163">指定此 Cmdlet 傳回的物件數目上限。</span><span class="sxs-lookup"><span data-stu-id="2fd02-163">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="2fd02-164">-Prefix</span><span class="sxs-lookup"><span data-stu-id="2fd02-164">-Prefix</span></span>
<span data-ttu-id="2fd02-165">針對您要取得的 blob 名稱指定一個前置詞。</span><span class="sxs-lookup"><span data-stu-id="2fd02-165">Specifies a prefix for the blob names that you want to get.</span></span>
<span data-ttu-id="2fd02-166">這個參數不支援使用正則運算式或萬用字元來進行搜尋。</span><span class="sxs-lookup"><span data-stu-id="2fd02-166">This parameter does not support using regular expressions or wildcard characters to search.</span></span>
<span data-ttu-id="2fd02-167">這表示如果容器只有一個名為 "My"、"MyBlob1" 和 "MyBlob2" 的 blob，且您指定了 "-Prefix My \*"，則 Cmdlet 不會傳回 blob。</span><span class="sxs-lookup"><span data-stu-id="2fd02-167">This means that if the container has only blobs named "My", "MyBlob1", and "MyBlob2" and you specify "-Prefix My\*", the cmdlet returns no blobs.</span></span>
<span data-ttu-id="2fd02-168">不過，如果您指定了 "-Prefix My"，此 Cmdlet 會傳回 "My"、"MyBlob1" 和 "MyBlob2"。</span><span class="sxs-lookup"><span data-stu-id="2fd02-168">However, if you specify "-Prefix My", the cmdlet returns "My", "MyBlob1", and "MyBlob2".</span></span>

```yaml
Type: System.String
Parameter Sets: BlobPrefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fd02-169">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2fd02-169">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="2fd02-170">指定要求的服務端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="2fd02-170">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="2fd02-171">如果所指定的間隔在服務處理要求之前就已到期，儲存服務就會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="2fd02-171">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="2fd02-172">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="2fd02-172">-SnapshotTime</span></span>
<span data-ttu-id="2fd02-173">Blob SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="2fd02-173">Blob SnapshotTime</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: SingleBlobSnapshotTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fd02-174">-VersionId</span><span class="sxs-lookup"><span data-stu-id="2fd02-174">-VersionId</span></span>
<span data-ttu-id="2fd02-175">Blob VersionId</span><span class="sxs-lookup"><span data-stu-id="2fd02-175">Blob VersionId</span></span>

```yaml
Type: System.String
Parameter Sets: SingleBlobVersionID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fd02-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fd02-176">CommonParameters</span></span>
<span data-ttu-id="2fd02-177">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2fd02-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fd02-178">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2fd02-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fd02-179">輸入</span><span class="sxs-lookup"><span data-stu-id="2fd02-179">INPUTS</span></span>

### <span data-ttu-id="2fd02-180">System.object</span><span class="sxs-lookup"><span data-stu-id="2fd02-180">System.String</span></span>

### <span data-ttu-id="2fd02-181">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="2fd02-181">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2fd02-182">輸出</span><span class="sxs-lookup"><span data-stu-id="2fd02-182">OUTPUTS</span></span>

### <span data-ttu-id="2fd02-183">AzureStorageBlob WindowsAzure. ResourceModel。</span><span class="sxs-lookup"><span data-stu-id="2fd02-183">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="2fd02-184">筆記</span><span class="sxs-lookup"><span data-stu-id="2fd02-184">NOTES</span></span>

## <span data-ttu-id="2fd02-185">相關連結</span><span class="sxs-lookup"><span data-stu-id="2fd02-185">RELATED LINKS</span></span>

[<span data-ttu-id="2fd02-186">AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2fd02-186">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="2fd02-187">移除-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="2fd02-187">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)

[<span data-ttu-id="2fd02-188">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2fd02-188">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)

