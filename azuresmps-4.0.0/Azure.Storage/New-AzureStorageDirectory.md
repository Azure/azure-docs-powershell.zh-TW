---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 65962F9A-CC79-4B8B-9208-A993708FD36F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1bd97057cfafc48b3f1edd8539e7808056599117
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443099"
---
# <span data-ttu-id="535f4-101">New-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="535f4-101">New-AzureStorageDirectory</span></span>

## <span data-ttu-id="535f4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="535f4-102">SYNOPSIS</span></span>
<span data-ttu-id="535f4-103">建立目錄。</span><span class="sxs-lookup"><span data-stu-id="535f4-103">Creates a directory.</span></span>

## <span data-ttu-id="535f4-104">句法</span><span class="sxs-lookup"><span data-stu-id="535f4-104">SYNTAX</span></span>

### <span data-ttu-id="535f4-105">共用名稱 (預設) </span><span class="sxs-lookup"><span data-stu-id="535f4-105">ShareName (Default)</span></span>
```
New-AzureStorageDirectory [-ShareName] <String> [-Path] <String> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="535f4-106">共用</span><span class="sxs-lookup"><span data-stu-id="535f4-106">Share</span></span>
```
New-AzureStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="535f4-107">空目錄</span><span class="sxs-lookup"><span data-stu-id="535f4-107">Directory</span></span>
```
New-AzureStorageDirectory [-Directory] <CloudFileDirectory> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="535f4-108">說明</span><span class="sxs-lookup"><span data-stu-id="535f4-108">DESCRIPTION</span></span>
<span data-ttu-id="535f4-109">**新的-AzureStorageDirectory** Cmdlet 會建立目錄。</span><span class="sxs-lookup"><span data-stu-id="535f4-109">The **New-AzureStorageDirectory** cmdlet creates a directory.</span></span>
<span data-ttu-id="535f4-110">這個 Cmdlet 會傳回 **CloudFileDirectory** 物件。</span><span class="sxs-lookup"><span data-stu-id="535f4-110">This cmdlet returns a **CloudFileDirectory** object.</span></span>

## <span data-ttu-id="535f4-111">示例</span><span class="sxs-lookup"><span data-stu-id="535f4-111">EXAMPLES</span></span>

### <span data-ttu-id="535f4-112">範例1：在檔案共用中建立資料夾</span><span class="sxs-lookup"><span data-stu-id="535f4-112">Example 1: Create a folder in a file share</span></span>
```
PS C:\>New-AzureStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="535f4-113">這個命令會在檔案共用中建立名為 ContosoWorkingFolder 的資料夾（名為 ContosoShare06）。</span><span class="sxs-lookup"><span data-stu-id="535f4-113">This command creates a folder named ContosoWorkingFolder in the file share named ContosoShare06.</span></span>

### <span data-ttu-id="535f4-114">範例2：在檔案共用物件中指定的檔案共用中建立資料夾</span><span class="sxs-lookup"><span data-stu-id="535f4-114">Example 2: Create a folder in a file share specified in a file share object</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06" | New-AzureStorageDirectory -Path "ContosoWorkingFolder"
```

<span data-ttu-id="535f4-115">這個命令會使用 **AzureStorageShare** Cmdlet 來取得名為 ContosoShare06 的檔案共用，然後使用管線運算子將它傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="535f4-115">This command uses the **Get-AzureStorageShare** cmdlet to get the file share named ContosoShare06, and then passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="535f4-116">目前的 Cmdlet 會在 ContosoShare06 中建立名為 ContosoWorkingFolder 的資料夾。</span><span class="sxs-lookup"><span data-stu-id="535f4-116">The current cmdlet creates the folder named ContosoWorkingFolder in ContosoShare06.</span></span>

## <span data-ttu-id="535f4-117">參數</span><span class="sxs-lookup"><span data-stu-id="535f4-117">PARAMETERS</span></span>

### <span data-ttu-id="535f4-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="535f4-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="535f4-119">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="535f4-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="535f4-120">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="535f4-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="535f4-121">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="535f4-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="535f4-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="535f4-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="535f4-123">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="535f4-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="535f4-124">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="535f4-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="535f4-125">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="535f4-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="535f4-126">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="535f4-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="535f4-127">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="535f4-127">The default value is 10.</span></span>

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

### <span data-ttu-id="535f4-128">-內容</span><span class="sxs-lookup"><span data-stu-id="535f4-128">-Context</span></span>
<span data-ttu-id="535f4-129">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="535f4-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="535f4-130">若要取得儲存內容，請使用 [AzureStorageCoNtext](./New-AzureStorageContext.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="535f4-130">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="535f4-131">-Directory</span><span class="sxs-lookup"><span data-stu-id="535f4-131">-Directory</span></span>
<span data-ttu-id="535f4-132">將資料夾指定為 **CloudFileDirectory** 物件。</span><span class="sxs-lookup"><span data-stu-id="535f4-132">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="535f4-133">這個 Cmdlet 會在此參數指定的位置中建立資料夾。</span><span class="sxs-lookup"><span data-stu-id="535f4-133">This cmdlet creates the folder in the location that this parameter specifies.</span></span>
<span data-ttu-id="535f4-134">若要取得目錄，請使用 New-AzureStorageDirectory Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="535f4-134">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="535f4-135">您也可以使用 Get-AzureStorageFile Cmdlet 來取得目錄。</span><span class="sxs-lookup"><span data-stu-id="535f4-135">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="535f4-136">-Path</span><span class="sxs-lookup"><span data-stu-id="535f4-136">-Path</span></span>
<span data-ttu-id="535f4-137">指定資料夾的路徑。</span><span class="sxs-lookup"><span data-stu-id="535f4-137">Specifies the path of a folder.</span></span>
<span data-ttu-id="535f4-138">這個 Cmdlet 會為這個 Cmdlet 所指定的路徑建立一個資料夾。</span><span class="sxs-lookup"><span data-stu-id="535f4-138">This cmdlet creates a folder for the path that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="535f4-139">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="535f4-139">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="535f4-140">指定要求中伺服器部分的超時時間長度。</span><span class="sxs-lookup"><span data-stu-id="535f4-140">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="535f4-141">-共用</span><span class="sxs-lookup"><span data-stu-id="535f4-141">-Share</span></span>
<span data-ttu-id="535f4-142">指定 **CloudFileShare** 物件。</span><span class="sxs-lookup"><span data-stu-id="535f4-142">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="535f4-143">這個 Cmdlet 會在檔案共用中建立此參數指定的資料夾。</span><span class="sxs-lookup"><span data-stu-id="535f4-143">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>
<span data-ttu-id="535f4-144">若要取得 **CloudFileShare** 物件，請使用 Get-AzureStorageShare Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="535f4-144">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="535f4-145">此物件包含儲存內容。</span><span class="sxs-lookup"><span data-stu-id="535f4-145">This object contains the storage context.</span></span>
<span data-ttu-id="535f4-146">如果您指定此參數，請勿指定 *CoNtext* 參數。</span><span class="sxs-lookup"><span data-stu-id="535f4-146">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="535f4-147">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="535f4-147">-ShareName</span></span>
<span data-ttu-id="535f4-148">指定檔案共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="535f4-148">Specifies the name of the file share.</span></span>
<span data-ttu-id="535f4-149">這個 Cmdlet 會在檔案共用中建立此參數指定的資料夾。</span><span class="sxs-lookup"><span data-stu-id="535f4-149">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="535f4-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="535f4-150">CommonParameters</span></span>
<span data-ttu-id="535f4-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="535f4-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="535f4-152">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="535f4-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="535f4-153">輸入</span><span class="sxs-lookup"><span data-stu-id="535f4-153">INPUTS</span></span>

## <span data-ttu-id="535f4-154">輸出</span><span class="sxs-lookup"><span data-stu-id="535f4-154">OUTPUTS</span></span>

## <span data-ttu-id="535f4-155">筆記</span><span class="sxs-lookup"><span data-stu-id="535f4-155">NOTES</span></span>

## <span data-ttu-id="535f4-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="535f4-156">RELATED LINKS</span></span>

[<span data-ttu-id="535f4-157">AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="535f4-157">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="535f4-158">AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="535f4-158">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="535f4-159">新-AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="535f4-159">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="535f4-160">新-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="535f4-160">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)

[<span data-ttu-id="535f4-161">移除-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="535f4-161">Remove-AzureStorageDirectory</span></span>](./Remove-AzureStorageDirectory.md)
