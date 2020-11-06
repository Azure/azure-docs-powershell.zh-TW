---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 38207027-FD76-45EE-8817-88599735C0B0
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFile.md
ms.openlocfilehash: a66b84586693052a2e6279c0cd56d8b091ae4230
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449469"
---
# <span data-ttu-id="644c5-101">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="644c5-101">Get-AzureStorageFile</span></span>

## <span data-ttu-id="644c5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="644c5-102">SYNOPSIS</span></span>
<span data-ttu-id="644c5-103">列出路徑的目錄和檔案。</span><span class="sxs-lookup"><span data-stu-id="644c5-103">Lists directories and files for a path.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="644c5-104">句法</span><span class="sxs-lookup"><span data-stu-id="644c5-104">SYNTAX</span></span>

### <span data-ttu-id="644c5-105">共用名稱 (預設) </span><span class="sxs-lookup"><span data-stu-id="644c5-105">ShareName (Default)</span></span>
```
Get-AzureStorageFile [-ShareName] <String> [[-Path] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="644c5-106">共用</span><span class="sxs-lookup"><span data-stu-id="644c5-106">Share</span></span>
```
Get-AzureStorageFile [-Share] <CloudFileShare> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="644c5-107">空目錄</span><span class="sxs-lookup"><span data-stu-id="644c5-107">Directory</span></span>
```
Get-AzureStorageFile [-Directory] <CloudFileDirectory> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="644c5-108">說明</span><span class="sxs-lookup"><span data-stu-id="644c5-108">DESCRIPTION</span></span>
<span data-ttu-id="644c5-109">**AzureStorageFile** Cmdlet 會列出您指定的共用或目錄的目錄和檔案。</span><span class="sxs-lookup"><span data-stu-id="644c5-109">The **Get-AzureStorageFile** cmdlet lists directories and files for the share or directory that you specify.</span></span>
<span data-ttu-id="644c5-110">指定 *path* 參數，以取得指定路徑中目錄或檔案的實例。</span><span class="sxs-lookup"><span data-stu-id="644c5-110">Specify the *Path* parameter to get an instance of a directory or file in the specified path.</span></span>

<span data-ttu-id="644c5-111">這個 Cmdlet 會傳回 **AzureStorageFile** 和 **AzureStorageDirectory** 物件。</span><span class="sxs-lookup"><span data-stu-id="644c5-111">This cmdlet returns **AzureStorageFile** and **AzureStorageDirectory** objects.</span></span>
<span data-ttu-id="644c5-112">您可以使用 **IsDirectory** 屬性來區分資料夾與檔案。</span><span class="sxs-lookup"><span data-stu-id="644c5-112">You can use the **IsDirectory** property to distinguish between folders and files.</span></span>

## <span data-ttu-id="644c5-113">示例</span><span class="sxs-lookup"><span data-stu-id="644c5-113">EXAMPLES</span></span>

### <span data-ttu-id="644c5-114">範例1：列出共用中的目錄</span><span class="sxs-lookup"><span data-stu-id="644c5-114">Example 1: List directories in a share</span></span>
```
PS C:\>Get-AzureStorageFile -ShareName "ContosoShare06" | where {$_.GetType().Name -eq "CloudFileDirectory"}
```

<span data-ttu-id="644c5-115">這個命令只會列出 [共用] ContosoShare06 中的目錄。</span><span class="sxs-lookup"><span data-stu-id="644c5-115">This command lists only the directories in the share ContosoShare06.</span></span>
<span data-ttu-id="644c5-116">它會先使用管線運算子來檢索檔案和目錄，並將它們傳到 **where** 運算子，然後捨棄類型不是 "CloudFileDirectory" 的任何物件。</span><span class="sxs-lookup"><span data-stu-id="644c5-116">It first retrieves both files and directories, passes them to the **where** operator by using the pipeline operator, then discards any objects whose type is not "CloudFileDirectory".</span></span>

### <span data-ttu-id="644c5-117">範例2：列出檔案目錄</span><span class="sxs-lookup"><span data-stu-id="644c5-117">Example 2: List a File Directory</span></span>
```
PS C:\> Get-AzureStorageFile -ShareName "ContosoShare06" -Path "ContosoWorkingFolder" | Get-AzureStorageFile
```

<span data-ttu-id="644c5-118">這個命令會在 [共用 ContosoShare06] 底下的 [目錄 ContosoWorkingFolder] 中列出檔案和資料夾。</span><span class="sxs-lookup"><span data-stu-id="644c5-118">This command lists the files and folders in the directory ContosoWorkingFolder under the share ContosoShare06.</span></span>
<span data-ttu-id="644c5-119">它會先取得目錄實例，然後將它的管道加入 **AzureStorageFile** Cmdlet，以列出該目錄。</span><span class="sxs-lookup"><span data-stu-id="644c5-119">It first gets the directory instance, and then pipelines it to the **Get-AzureStorageFile** cmdlet to list the directory.</span></span>

## <span data-ttu-id="644c5-120">參數</span><span class="sxs-lookup"><span data-stu-id="644c5-120">PARAMETERS</span></span>

### <span data-ttu-id="644c5-121">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="644c5-121">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="644c5-122">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="644c5-122">Specifies the client side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="644c5-123">如果上一個呼叫在指定的間隔時間內失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="644c5-123">If the previous call fails within the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="644c5-124">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="644c5-124">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="644c5-125">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="644c5-125">-ConcurrentTaskCount</span></span>
<span data-ttu-id="644c5-126">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="644c5-126">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="644c5-127">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="644c5-127">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="644c5-128">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="644c5-128">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="644c5-129">這個參數可協助減輕低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="644c5-129">This parameter can help mitigate network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="644c5-130">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="644c5-130">The default value is 10.</span></span>

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

### <span data-ttu-id="644c5-131">-內容</span><span class="sxs-lookup"><span data-stu-id="644c5-131">-Context</span></span>
<span data-ttu-id="644c5-132">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="644c5-132">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="644c5-133">若要取得儲存內容，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="644c5-133">To obtain a Storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ShareName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="644c5-134">-Directory</span><span class="sxs-lookup"><span data-stu-id="644c5-134">-Directory</span></span>
<span data-ttu-id="644c5-135">將資料夾指定為 **CloudFileDirectory** 物件。</span><span class="sxs-lookup"><span data-stu-id="644c5-135">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="644c5-136">這個 Cmdlet 會取得此參數指定的資料夾。</span><span class="sxs-lookup"><span data-stu-id="644c5-136">This cmdlet gets the folder that this parameter specifies.</span></span>
<span data-ttu-id="644c5-137">若要取得目錄，請使用 New-AzureStorageDirectory Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="644c5-137">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="644c5-138">您也可以使用 **AzureStorageFile** Cmdlet 來取得目錄。</span><span class="sxs-lookup"><span data-stu-id="644c5-138">You can also use the **Get-AzureStorageFile** cmdlet to obtain a directory.</span></span>

```yaml
Type: CloudFileDirectory
Parameter Sets: Directory
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="644c5-139">-Path</span><span class="sxs-lookup"><span data-stu-id="644c5-139">-Path</span></span>
<span data-ttu-id="644c5-140">指定資料夾的路徑。</span><span class="sxs-lookup"><span data-stu-id="644c5-140">Specifies the path of a folder.</span></span>

<span data-ttu-id="644c5-141">如果您省略 *Path* 參數， **AzureStorageFile** 會列出指定檔案共用或目錄中的目錄和檔案。</span><span class="sxs-lookup"><span data-stu-id="644c5-141">If you omit the *Path* parameter, **Get-AzureStorageFile** lists the directories and files in the specified file share or directory.</span></span>
<span data-ttu-id="644c5-142">如果您包含 *Path* 參數，則 **AzureStorageFile** 會傳回指定路徑中目錄或檔案的實例。</span><span class="sxs-lookup"><span data-stu-id="644c5-142">If you include the *Path* parameter, **Get-AzureStorageFile** returns an instance of a directory or file in the specified path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="644c5-143">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="644c5-143">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="644c5-144">指定要求的服務端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="644c5-144">Specifies the service-side timeout interval, in seconds, for a request.</span></span>
<span data-ttu-id="644c5-145">如果所指定的間隔在服務處理要求之前就已到期，儲存服務就會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="644c5-145">If the specified interval elapses before the service processes the request, the Storage service returns an error.</span></span>

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

### <span data-ttu-id="644c5-146">-共用</span><span class="sxs-lookup"><span data-stu-id="644c5-146">-Share</span></span>
<span data-ttu-id="644c5-147">指定 **CloudFileShare** 物件。</span><span class="sxs-lookup"><span data-stu-id="644c5-147">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="644c5-148">這個 Cmdlet 會從此參數指定的檔案共用取得檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="644c5-148">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>
<span data-ttu-id="644c5-149">若要取得 **CloudFileShare** 物件，請使用 Get-AzureStorageShare Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="644c5-149">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="644c5-150">此物件包含儲存內容。</span><span class="sxs-lookup"><span data-stu-id="644c5-150">This object contains the Storage context.</span></span>
<span data-ttu-id="644c5-151">如果您指定此參數，請勿指定 *CoNtext* 參數。</span><span class="sxs-lookup"><span data-stu-id="644c5-151">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: CloudFileShare
Parameter Sets: Share
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="644c5-152">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="644c5-152">-ShareName</span></span>
<span data-ttu-id="644c5-153">指定檔案共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="644c5-153">Specifies the name of the file share.</span></span>
<span data-ttu-id="644c5-154">這個 Cmdlet 會從此參數指定的檔案共用取得檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="644c5-154">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="644c5-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="644c5-155">CommonParameters</span></span>
<span data-ttu-id="644c5-156">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="644c5-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="644c5-157">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="644c5-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="644c5-158">輸入</span><span class="sxs-lookup"><span data-stu-id="644c5-158">INPUTS</span></span>

### <span data-ttu-id="644c5-159">IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="644c5-159">IStorageContext</span></span>

<span data-ttu-id="644c5-160">參數「CoNtext」接受來自管線的 "IStorageCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="644c5-160">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="644c5-161">CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="644c5-161">CloudFileDirectory</span></span>

<span data-ttu-id="644c5-162">形參 "Directory" 接受管線中 "CloudFileDirectory" 類型的值</span><span class="sxs-lookup"><span data-stu-id="644c5-162">Parameter 'Directory' accepts value of type 'CloudFileDirectory' from the pipeline</span></span>

### <span data-ttu-id="644c5-163">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="644c5-163">CloudFileShare</span></span>

<span data-ttu-id="644c5-164">形參 "Share" 接受管線中 "CloudFileShare" 類型的值</span><span class="sxs-lookup"><span data-stu-id="644c5-164">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

## <span data-ttu-id="644c5-165">輸出</span><span class="sxs-lookup"><span data-stu-id="644c5-165">OUTPUTS</span></span>

## <span data-ttu-id="644c5-166">筆記</span><span class="sxs-lookup"><span data-stu-id="644c5-166">NOTES</span></span>

## <span data-ttu-id="644c5-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="644c5-167">RELATED LINKS</span></span>

[<span data-ttu-id="644c5-168">AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="644c5-168">Get-AzureStorageFileContent</span></span>](./Get-AzureStorageFileContent.md)

[<span data-ttu-id="644c5-169">新-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="644c5-169">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)

[<span data-ttu-id="644c5-170">移除-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="644c5-170">Remove-AzureStorageDirectory</span></span>](./Remove-AzureStorageDirectory.md)

[<span data-ttu-id="644c5-171">移除-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="644c5-171">Remove-AzureStorageFile</span></span>](./Remove-AzureStorageFile.md)

[<span data-ttu-id="644c5-172">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="644c5-172">Set-AzureStorageFileContent</span></span>](./Set-AzureStorageFileContent.md)


