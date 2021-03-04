---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E54BFD3A-CD54-4E6B-9574-92B8D3E88FF3
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlob.md
ms.openlocfilehash: 317d25ecfa48203c411f368aa5b00ac3380773ef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915145"
---
# <span data-ttu-id="8f143-101">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="8f143-101">Get-AzStorageBlob</span></span>

## <span data-ttu-id="8f143-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8f143-102">SYNOPSIS</span></span>
<span data-ttu-id="8f143-103">列出容器中的 Blob。</span><span class="sxs-lookup"><span data-stu-id="8f143-103">Lists blobs in a container.</span></span>

## <span data-ttu-id="8f143-104">語法</span><span class="sxs-lookup"><span data-stu-id="8f143-104">SYNTAX</span></span>

### <span data-ttu-id="8f143-105">BlobName (預設) </span><span class="sxs-lookup"><span data-stu-id="8f143-105">BlobName (Default)</span></span>
```
Get-AzStorageBlob [[-Blob] <String>] [-Container] <String> [-IncludeDeleted] [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="8f143-106">SingleBlobSnapshotTime</span><span class="sxs-lookup"><span data-stu-id="8f143-106">SingleBlobSnapshotTime</span></span>
```
Get-AzStorageBlob [-Blob] <String> [-Container] <String> [-IncludeDeleted] -SnapshotTime <DateTimeOffset>
 [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="8f143-107">SingleBlobVersionID</span><span class="sxs-lookup"><span data-stu-id="8f143-107">SingleBlobVersionID</span></span>
```
Get-AzStorageBlob [-Blob] <String> [-Container] <String> [-IncludeDeleted] -VersionId <String>
 [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="8f143-108">BlobPrefix</span><span class="sxs-lookup"><span data-stu-id="8f143-108">BlobPrefix</span></span>
```
Get-AzStorageBlob [-Prefix <String>] [-Container] <String> [-IncludeDeleted] [-IncludeVersion]
 [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="8f143-109">描述</span><span class="sxs-lookup"><span data-stu-id="8f143-109">DESCRIPTION</span></span>
<span data-ttu-id="8f143-110">**Get-AzStorageBlob** Cmdlet 會列出 Azure 儲存帳戶中指定容器中的 Blob。</span><span class="sxs-lookup"><span data-stu-id="8f143-110">The **Get-AzStorageBlob** cmdlet lists blobs in the specified container in an Azure storage account.</span></span>

## <span data-ttu-id="8f143-111">例子</span><span class="sxs-lookup"><span data-stu-id="8f143-111">EXAMPLES</span></span>

### <span data-ttu-id="8f143-112">範例 1：使用 Blob 名稱取得 Blob</span><span class="sxs-lookup"><span data-stu-id="8f143-112">Example 1: Get a blob by blob name</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Blob blob*
```

<span data-ttu-id="8f143-113">此命令使用 Blob 名稱和萬用字元來取得 Blob。</span><span class="sxs-lookup"><span data-stu-id="8f143-113">This command uses a blob name and wildcard to get a blob.</span></span>

### <span data-ttu-id="8f143-114">範例 2：使用管線在容器中取得 Blob</span><span class="sxs-lookup"><span data-stu-id="8f143-114">Example 2: Get blobs in a container by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Name container* | Get-AzStorageBlob -IncludeDeleted

   Container Uri: https://storageaccountname.blob.core.windows.net/container1

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime         IsDeleted 
----                 --------  ------          -----------                    ------------         ---------- ------------         --------- 
test1                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:19Z            2017-11-08 08:19:32Z True      
test1                BlockBlob 403116          application/octet-stream       2017-11-08 09:00:29Z                                 True      
test2                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:00Z                                 False
```

<span data-ttu-id="8f143-115">此命令會使用管線取得所有 blob， (容器中的已刪除狀態) Blob。</span><span class="sxs-lookup"><span data-stu-id="8f143-115">This command uses the pipeline to get all blobs (include blobs in Deleted status) in a container.</span></span>

### <span data-ttu-id="8f143-116">範例 3：根據名稱首碼取得 Blob</span><span class="sxs-lookup"><span data-stu-id="8f143-116">Example 3: Get blobs by name prefix</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Prefix "blob"
```

<span data-ttu-id="8f143-117">此命令使用名稱首碼來取得 Blob。</span><span class="sxs-lookup"><span data-stu-id="8f143-117">This command uses a name prefix to get blobs.</span></span>

### <span data-ttu-id="8f143-118">範例 4：列出多個批次中的 Blob</span><span class="sxs-lookup"><span data-stu-id="8f143-118">Example 4: List blobs in multiple batches</span></span>
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

<span data-ttu-id="8f143-119">此範例使用 *MaxCount* 和 *ContinuationToken* 參數來列出多個批次中的 Azure 儲存體 Blob。</span><span class="sxs-lookup"><span data-stu-id="8f143-119">This example uses the *MaxCount* and *ContinuationToken* parameters to list Azure Storage blobs in multiple batches.</span></span>
<span data-ttu-id="8f143-120">前四個命令會指派值給範例中要使用的變數。</span><span class="sxs-lookup"><span data-stu-id="8f143-120">The first four commands assign values to variables to use in the example.</span></span>
<span data-ttu-id="8f143-121">第五個命令會指定使用 **Get-AzStorageBlob** Cmdlet 取得 Blob 的 **Do-While** 語句。</span><span class="sxs-lookup"><span data-stu-id="8f143-121">The fifth command specifies a **Do-While** statement that uses the **Get-AzStorageBlob** cmdlet to get blobs.</span></span>
<span data-ttu-id="8f143-122">語句包含儲存在 $Token 變數中的延續權杖。</span><span class="sxs-lookup"><span data-stu-id="8f143-122">The statement includes the continuation token stored in the $Token variable.</span></span>
<span data-ttu-id="8f143-123">$Token迴圈執行時變更值。</span><span class="sxs-lookup"><span data-stu-id="8f143-123">$Token changes value as the loop runs.</span></span>
<span data-ttu-id="8f143-124">如需要詳細資訊，請鍵入 `Get-Help About_Do` 。</span><span class="sxs-lookup"><span data-stu-id="8f143-124">For more information, type `Get-Help About_Do`.</span></span>
<span data-ttu-id="8f143-125">最後一個命令會使用 **Echo** 命令來顯示總計。</span><span class="sxs-lookup"><span data-stu-id="8f143-125">The final command uses the **Echo** command to display the total.</span></span>

### <span data-ttu-id="8f143-126">範例 5：取得容器中的所有 Blob 包含 Blob 版本</span><span class="sxs-lookup"><span data-stu-id="8f143-126">Example 5: Get all blobs in a container include blob version</span></span>
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

<span data-ttu-id="8f143-127">此命令會獲得容器內的所有 Blob 包含 Blob 版本。</span><span class="sxs-lookup"><span data-stu-id="8f143-127">This command gets all blobs in a container include blob version.</span></span>

### <span data-ttu-id="8f143-128">範例 6：取得單一 Blob 版本</span><span class="sxs-lookup"><span data-stu-id="8f143-128">Example 6: Get a single blob version</span></span>
```
PS C:\> Get-AzStorageBlob -Container "containername" -Blob blob2 -VersionId "2020-07-03T16:19:16.2883167Z" 

   AccountName: storageaccountname, ContainerName: containername

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
blob2                BlockBlob 2097152         application/octet-stream       2020-07-03 16:19:16Z Hot                                     False      2020-07-03T16:19:16.2883167Z
```

<span data-ttu-id="8f143-129">此命令會使用 VersionId 獲得單一 Blob 版本。</span><span class="sxs-lookup"><span data-stu-id="8f143-129">This command gets a single blobs verion with VersionId.</span></span>

### <span data-ttu-id="8f143-130">範例 7：取得單一 Blob 快照</span><span class="sxs-lookup"><span data-stu-id="8f143-130">Example 7: Get a single blob snapshot</span></span>
```
PS C:\> Get-AzStorageBlob -Container "containername" -Blob blob1 -SnapshotTime "2020-07-06T06:56:06.8588431Z"

   AccountName: storageaccountname, ContainerName: containername

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
blob1                BlockBlob 2097152         application/octet-stream       2020-07-06 06:56:06Z Hot        2020-07-06T06:56:06.8588431Z False
```

<span data-ttu-id="8f143-131">此命令會使用 SnapshotTime 獲得單一 Blob 快照。</span><span class="sxs-lookup"><span data-stu-id="8f143-131">This command gets a single blobs snapshot with SnapshotTime.</span></span>

## <span data-ttu-id="8f143-132">參數</span><span class="sxs-lookup"><span data-stu-id="8f143-132">PARAMETERS</span></span>

### <span data-ttu-id="8f143-133">-Blob</span><span class="sxs-lookup"><span data-stu-id="8f143-133">-Blob</span></span>
<span data-ttu-id="8f143-134">指定名稱或名稱模式，可用於萬用字元搜尋。</span><span class="sxs-lookup"><span data-stu-id="8f143-134">Specifies a name or name pattern, which can be used for a wildcard search.</span></span>
<span data-ttu-id="8f143-135">如果沒有指定 Blob 名稱，Cmdlet 會列出指定容器中的所有 Blob。</span><span class="sxs-lookup"><span data-stu-id="8f143-135">If no blob name is specified, the cmdlet lists all the blobs in the specified container.</span></span>
<span data-ttu-id="8f143-136">如果為此參數指定值，Cmdlet 會列出所有名稱符合此參數的 Blob。</span><span class="sxs-lookup"><span data-stu-id="8f143-136">If a value is specified for this parameter, the cmdlet lists all blobs with names that match this parameter.</span></span> <span data-ttu-id="8f143-137">此參數支援字串中任何位置的萬用字元。</span><span class="sxs-lookup"><span data-stu-id="8f143-137">This parameter supports wildcards anywhere in the string.</span></span>

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

### <span data-ttu-id="8f143-138">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8f143-138">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="8f143-139">指定一個服務要求用戶端的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="8f143-139">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="8f143-140">如果前一個通話在指定的時間間隔內失敗，此 Cmdlet 會重新重試要求。</span><span class="sxs-lookup"><span data-stu-id="8f143-140">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="8f143-141">如果此 Cmdlet 在間隔經過之前未收到成功回應，此 Cmdlet 會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="8f143-141">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="8f143-142">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="8f143-142">-ConcurrentTaskCount</span></span>
<span data-ttu-id="8f143-143">指定同時進行的最大網路通話數。</span><span class="sxs-lookup"><span data-stu-id="8f143-143">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="8f143-144">您可以使用此參數來限制並行，以節流本地 CPU 和頻寬使用量，方法為指定並行網路通話的數量上限。</span><span class="sxs-lookup"><span data-stu-id="8f143-144">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="8f143-145">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="8f143-145">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="8f143-146">此參數有助於減少低頻寬環境的網路連接問題，例如每秒 100 KB。</span><span class="sxs-lookup"><span data-stu-id="8f143-146">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="8f143-147">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="8f143-147">The default value is 10.</span></span>

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

### <span data-ttu-id="8f143-148">-Container</span><span class="sxs-lookup"><span data-stu-id="8f143-148">-Container</span></span>
<span data-ttu-id="8f143-149">指定容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="8f143-149">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="8f143-150">-內容</span><span class="sxs-lookup"><span data-stu-id="8f143-150">-Context</span></span>
<span data-ttu-id="8f143-151">指定您想要取得 Blob 清單的 Azure 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="8f143-151">Specifies the Azure storage account from which you want to get a list of blobs.</span></span>
<span data-ttu-id="8f143-152">您可以使用 New-AzStorageContext Cmdlet 來建立儲存內容。</span><span class="sxs-lookup"><span data-stu-id="8f143-152">You can use the New-AzStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="8f143-153">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="8f143-153">-ContinuationToken</span></span>
<span data-ttu-id="8f143-154">指定 Blob 清單的延續權杖。</span><span class="sxs-lookup"><span data-stu-id="8f143-154">Specifies a continuation token for the blob list.</span></span>
<span data-ttu-id="8f143-155">使用此參數和 *MaxCount* 參數列出多個批次中的 Blob。</span><span class="sxs-lookup"><span data-stu-id="8f143-155">Use this parameter and the *MaxCount* parameter to list blobs in multiple batches.</span></span>

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

### <span data-ttu-id="8f143-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f143-156">-DefaultProfile</span></span>
<span data-ttu-id="8f143-157">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8f143-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f143-158">-IncludeDeleted</span><span class="sxs-lookup"><span data-stu-id="8f143-158">-IncludeDeleted</span></span>
<span data-ttu-id="8f143-159">包含已刪除的 Blob，根據預設，get blob 不會包含已刪除的 Blob。</span><span class="sxs-lookup"><span data-stu-id="8f143-159">Include Deleted Blob, by default get blob won't include deleted blob.</span></span>

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

### <span data-ttu-id="8f143-160">-IncludeVersion</span><span class="sxs-lookup"><span data-stu-id="8f143-160">-IncludeVersion</span></span>
<span data-ttu-id="8f143-161">只有在此參數存在時，Blob 版本會列出，根據預設，取得 Blob 不會包含 Blob 版本。</span><span class="sxs-lookup"><span data-stu-id="8f143-161">Blob versions will be listed only if this parameter is present, by default get blob won't include blob versions.</span></span>

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

### <span data-ttu-id="8f143-162">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="8f143-162">-MaxCount</span></span>
<span data-ttu-id="8f143-163">指定此 Cmdlet 會返回的物件數量上限。</span><span class="sxs-lookup"><span data-stu-id="8f143-163">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="8f143-164">-首碼</span><span class="sxs-lookup"><span data-stu-id="8f143-164">-Prefix</span></span>
<span data-ttu-id="8f143-165">指定要取得之 Blob 名稱的首碼。</span><span class="sxs-lookup"><span data-stu-id="8f143-165">Specifies a prefix for the blob names that you want to get.</span></span>
<span data-ttu-id="8f143-166">此參數不支援使用正則運算式或萬用字元進行搜尋。</span><span class="sxs-lookup"><span data-stu-id="8f143-166">This parameter does not support using regular expressions or wildcard characters to search.</span></span>
<span data-ttu-id="8f143-167">這表示，如果容器只有名稱為「我的」、「MyBlob1」和「MyBlob2」的 Blob，而且您指定「-首碼 My\*」，Cmdlet 會不會返回任何 Blob。</span><span class="sxs-lookup"><span data-stu-id="8f143-167">This means that if the container has only blobs named "My", "MyBlob1", and "MyBlob2" and you specify "-Prefix My\*", the cmdlet returns no blobs.</span></span>
<span data-ttu-id="8f143-168">不過，如果您指定"-首碼 My"，Cmdlet 會返回 "My"、"MyBlob1" 和 "MyBlob2"。</span><span class="sxs-lookup"><span data-stu-id="8f143-168">However, if you specify "-Prefix My", the cmdlet returns "My", "MyBlob1", and "MyBlob2".</span></span>

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

### <span data-ttu-id="8f143-169">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8f143-169">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="8f143-170">指定服務端要求的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="8f143-170">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="8f143-171">如果指定的時間間隔在服務處理要求之前已經過，儲存服務會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="8f143-171">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="8f143-172">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="8f143-172">-SnapshotTime</span></span>
<span data-ttu-id="8f143-173">Blob 快照時間</span><span class="sxs-lookup"><span data-stu-id="8f143-173">Blob SnapshotTime</span></span>

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

### <span data-ttu-id="8f143-174">-VersionId</span><span class="sxs-lookup"><span data-stu-id="8f143-174">-VersionId</span></span>
<span data-ttu-id="8f143-175">Blob VersionId</span><span class="sxs-lookup"><span data-stu-id="8f143-175">Blob VersionId</span></span>

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

### <span data-ttu-id="8f143-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f143-176">CommonParameters</span></span>
<span data-ttu-id="8f143-177">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8f143-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f143-178">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="8f143-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f143-179">輸入</span><span class="sxs-lookup"><span data-stu-id="8f143-179">INPUTS</span></span>

### <span data-ttu-id="8f143-180">System.String</span><span class="sxs-lookup"><span data-stu-id="8f143-180">System.String</span></span>

### <span data-ttu-id="8f143-181">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="8f143-181">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8f143-182">輸出</span><span class="sxs-lookup"><span data-stu-id="8f143-182">OUTPUTS</span></span>

### <span data-ttu-id="8f143-183">Microsoft.WindowsAzure.Commands.Common.storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="8f143-183">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="8f143-184">筆記</span><span class="sxs-lookup"><span data-stu-id="8f143-184">NOTES</span></span>

## <span data-ttu-id="8f143-185">相關連結</span><span class="sxs-lookup"><span data-stu-id="8f143-185">RELATED LINKS</span></span>

[<span data-ttu-id="8f143-186">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8f143-186">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="8f143-187">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="8f143-187">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)

[<span data-ttu-id="8f143-188">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8f143-188">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)


