---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 65962F9A-CC79-4B8B-9208-A993708FD36F
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageDirectory.md
ms.openlocfilehash: bc83da1cd177585b76d68eb0b55cdd15120ff22e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449450"
---
# <span data-ttu-id="0eeb3-101">New-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="0eeb3-101">New-AzureStorageDirectory</span></span>

## <span data-ttu-id="0eeb3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0eeb3-102">SYNOPSIS</span></span>
<span data-ttu-id="0eeb3-103">建立目錄。</span><span class="sxs-lookup"><span data-stu-id="0eeb3-103">Creates a directory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0eeb3-104">句法</span><span class="sxs-lookup"><span data-stu-id="0eeb3-104">SYNTAX</span></span>

### <span data-ttu-id="0eeb3-105">共用名稱 (預設) </span><span class="sxs-lookup"><span data-stu-id="0eeb3-105">ShareName (Default)</span></span>
```
New-AzureStorageDirectory [-ShareName] <String> [-Path] <String> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="0eeb3-106">共用</span><span class="sxs-lookup"><span data-stu-id="0eeb3-106">Share</span></span>
```
New-AzureStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="0eeb3-107">空目錄</span><span class="sxs-lookup"><span data-stu-id="0eeb3-107">Directory</span></span>
```
New-AzureStorageDirectory [-Directory] <CloudFileDirectory> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="0eeb3-108">說明</span><span class="sxs-lookup"><span data-stu-id="0eeb3-108">DESCRIPTION</span></span>
<span data-ttu-id="0eeb3-109">**新的-AzureStorageDirectory** Cmdlet 會建立目錄。</span><span class="sxs-lookup"><span data-stu-id="0eeb3-109">The **New-AzureStorageDirectory** cmdlet creates a directory.</span></span>
<span data-ttu-id="0eeb3-110">這個 Cmdlet 會傳回 **CloudFileDirectory** 物件。</span><span class="sxs-lookup"><span data-stu-id="0eeb3-110">This cmdlet returns a **CloudFileDirectory** object.</span></span>

## <span data-ttu-id="0eeb3-111">示例</span><span class="sxs-lookup"><span data-stu-id="0eeb3-111">EXAMPLES</span></span>

### <span data-ttu-id="0eeb3-112">範例1：在檔案共用中建立資料夾</span><span class="sxs-lookup"><span data-stu-id="0eeb3-112">Example 1: Create a folder in a file share</span></span>
```
PS C:\>New-AzureStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="0eeb3-113">這個命令會在檔案共用中建立名為 ContosoWorkingFolder 的資料夾（名為 ContosoShare06）。</span><span class="sxs-lookup"><span data-stu-id="0eeb3-113">This command creates a folder named ContosoWorkingFolder in the file share named ContosoShare06.</span></span>

### <span data-ttu-id="0eeb3-114">範例2：在檔案共用物件中指定的檔案共用中建立資料夾</span><span class="sxs-lookup"><span data-stu-id="0eeb3-114">Example 2: Create a folder in a file share specified in a file share object</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06" | New-AzureStorageDirectory -Path "ContosoWorkingFolder"
```

<span data-ttu-id="0eeb3-115">這個命令會使用 **AzureStorageShare** Cmdlet 來取得名為 ContosoShare06 的檔案共用，然後使用管線運算子將它傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0eeb3-115">This command uses the **Get-AzureStorageShare** cmdlet to get the file share named ContosoShare06, and then passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0eeb3-116">目前的 Cmdlet 會在 ContosoShare06 中建立名為 ContosoWorkingFolder 的資料夾。</span><span class="sxs-lookup"><span data-stu-id="0eeb3-116">The current cmdlet creates the folder named ContosoWorkingFolder in ContosoShare06.</span></span>

## <span data-ttu-id="0eeb3-117">參數</span><span class="sxs-lookup"><span data-stu-id="0eeb3-117">PARAMETERS</span></span>

### <span data-ttu-id="0eeb3-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0eeb3-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="0eeb3-119">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="0eeb3-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="0eeb3-120">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="0eeb3-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="0eeb3-121">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="0eeb3-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="0eeb3-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="0eeb3-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="0eeb3-123">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="0eeb3-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="0eeb3-124">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="0eeb3-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="0eeb3-125">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="0eeb3-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="0eeb3-126">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="0eeb3-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="0eeb3-127">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="0eeb3-127">The default value is 10.</span></span>

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

### <span data-ttu-id="0eeb3-128">-內容</span><span class="sxs-lookup"><span data-stu-id="0eeb3-128">-Context</span></span>
<span data-ttu-id="0eeb3-129">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="0eeb3-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="0eeb3-130">若要取得儲存內容，請使用 [AzureStorageCoNtext](./New-AzureStorageContext.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0eeb3-130">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="0eeb3-131">-Directory</span><span class="sxs-lookup"><span data-stu-id="0eeb3-131">-Directory</span></span>
<span data-ttu-id="0eeb3-132">將資料夾指定為 **CloudFileDirectory** 物件。</span><span class="sxs-lookup"><span data-stu-id="0eeb3-132">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="0eeb3-133">這個 Cmdlet 會在此參數指定的位置中建立資料夾。</span><span class="sxs-lookup"><span data-stu-id="0eeb3-133">This cmdlet creates the folder in the location that this parameter specifies.</span></span>
<span data-ttu-id="0eeb3-134">若要取得目錄，請使用 New-AzureStorageDirectory Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0eeb3-134">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="0eeb3-135">您也可以使用 Get-AzureStorageFile Cmdlet 來取得目錄。</span><span class="sxs-lookup"><span data-stu-id="0eeb3-135">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="0eeb3-136">-Path</span><span class="sxs-lookup"><span data-stu-id="0eeb3-136">-Path</span></span>
<span data-ttu-id="0eeb3-137">指定資料夾的路徑。</span><span class="sxs-lookup"><span data-stu-id="0eeb3-137">Specifies the path of a folder.</span></span>
<span data-ttu-id="0eeb3-138">這個 Cmdlet 會為這個 Cmdlet 所指定的路徑建立一個資料夾。</span><span class="sxs-lookup"><span data-stu-id="0eeb3-138">This cmdlet creates a folder for the path that this cmdlet specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0eeb3-139">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0eeb3-139">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="0eeb3-140">指定要求中伺服器部分的超時時間長度。</span><span class="sxs-lookup"><span data-stu-id="0eeb3-140">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="0eeb3-141">-共用</span><span class="sxs-lookup"><span data-stu-id="0eeb3-141">-Share</span></span>
<span data-ttu-id="0eeb3-142">指定 **CloudFileShare** 物件。</span><span class="sxs-lookup"><span data-stu-id="0eeb3-142">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="0eeb3-143">這個 Cmdlet 會在檔案共用中建立此參數指定的資料夾。</span><span class="sxs-lookup"><span data-stu-id="0eeb3-143">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>
<span data-ttu-id="0eeb3-144">若要取得 **CloudFileShare** 物件，請使用 Get-AzureStorageShare Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0eeb3-144">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="0eeb3-145">此物件包含儲存內容。</span><span class="sxs-lookup"><span data-stu-id="0eeb3-145">This object contains the storage context.</span></span>
<span data-ttu-id="0eeb3-146">如果您指定此參數，請勿指定 *CoNtext* 參數。</span><span class="sxs-lookup"><span data-stu-id="0eeb3-146">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="0eeb3-147">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="0eeb3-147">-ShareName</span></span>
<span data-ttu-id="0eeb3-148">指定檔案共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="0eeb3-148">Specifies the name of the file share.</span></span>
<span data-ttu-id="0eeb3-149">這個 Cmdlet 會在檔案共用中建立此參數指定的資料夾。</span><span class="sxs-lookup"><span data-stu-id="0eeb3-149">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="0eeb3-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eeb3-150">CommonParameters</span></span>
<span data-ttu-id="0eeb3-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0eeb3-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eeb3-152">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0eeb3-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eeb3-153">輸入</span><span class="sxs-lookup"><span data-stu-id="0eeb3-153">INPUTS</span></span>

### <span data-ttu-id="0eeb3-154">IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="0eeb3-154">IStorageContext</span></span>

<span data-ttu-id="0eeb3-155">參數「CoNtext」接受來自管線的 "IStorageCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="0eeb3-155">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="0eeb3-156">CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="0eeb3-156">CloudFileDirectory</span></span>

<span data-ttu-id="0eeb3-157">形參 "Directory" 接受管線中 "CloudFileDirectory" 類型的值</span><span class="sxs-lookup"><span data-stu-id="0eeb3-157">Parameter 'Directory' accepts value of type 'CloudFileDirectory' from the pipeline</span></span>

### <span data-ttu-id="0eeb3-158">字串</span><span class="sxs-lookup"><span data-stu-id="0eeb3-158">String</span></span>

<span data-ttu-id="0eeb3-159">形參 "Path" 接受來自管線的 "String" 類型的值</span><span class="sxs-lookup"><span data-stu-id="0eeb3-159">Parameter 'Path' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="0eeb3-160">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="0eeb3-160">CloudFileShare</span></span>

<span data-ttu-id="0eeb3-161">形參 "Share" 接受管線中 "CloudFileShare" 類型的值</span><span class="sxs-lookup"><span data-stu-id="0eeb3-161">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

## <span data-ttu-id="0eeb3-162">輸出</span><span class="sxs-lookup"><span data-stu-id="0eeb3-162">OUTPUTS</span></span>

## <span data-ttu-id="0eeb3-163">筆記</span><span class="sxs-lookup"><span data-stu-id="0eeb3-163">NOTES</span></span>

## <span data-ttu-id="0eeb3-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="0eeb3-164">RELATED LINKS</span></span>

[<span data-ttu-id="0eeb3-165">AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="0eeb3-165">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="0eeb3-166">AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="0eeb3-166">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="0eeb3-167">新-AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="0eeb3-167">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="0eeb3-168">新-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="0eeb3-168">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)

[<span data-ttu-id="0eeb3-169">移除-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="0eeb3-169">Remove-AzureStorageDirectory</span></span>](./Remove-AzureStorageDirectory.md)
