---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 811671E9-592E-4E58-8174-34D665206A65
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageFile.md
gitcommit: https://github.com/Azure/azure-powershell/blob/173e94aec59d7f539b72e43e90e5e7f8ba5f62bc
ms.openlocfilehash: 7d1b12f95d0e74f99d97f64a9d1f7d35c6704101
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447212"
---
# <span data-ttu-id="3fb94-101">Remove-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="3fb94-101">Remove-AzureStorageFile</span></span>

## <span data-ttu-id="3fb94-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3fb94-102">SYNOPSIS</span></span>
<span data-ttu-id="3fb94-103">刪除檔案。</span><span class="sxs-lookup"><span data-stu-id="3fb94-103">Deletes a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3fb94-104">句法</span><span class="sxs-lookup"><span data-stu-id="3fb94-104">SYNTAX</span></span>

### <span data-ttu-id="3fb94-105">共用名稱 (預設) </span><span class="sxs-lookup"><span data-stu-id="3fb94-105">ShareName (Default)</span></span>
```
Remove-AzureStorageFile [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fb94-106">共用</span><span class="sxs-lookup"><span data-stu-id="3fb94-106">Share</span></span>
```
Remove-AzureStorageFile [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fb94-107">空目錄</span><span class="sxs-lookup"><span data-stu-id="3fb94-107">Directory</span></span>
```
Remove-AzureStorageFile [-Directory] <CloudFileDirectory> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fb94-108">檔案</span><span class="sxs-lookup"><span data-stu-id="3fb94-108">File</span></span>
```
Remove-AzureStorageFile [-File] <CloudFile> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fb94-109">說明</span><span class="sxs-lookup"><span data-stu-id="3fb94-109">DESCRIPTION</span></span>
<span data-ttu-id="3fb94-110">**AzureStorageFile** Cmdlet 會刪除檔案。</span><span class="sxs-lookup"><span data-stu-id="3fb94-110">The **Remove-AzureStorageFile** cmdlet deletes a file.</span></span>

## <span data-ttu-id="3fb94-111">示例</span><span class="sxs-lookup"><span data-stu-id="3fb94-111">EXAMPLES</span></span>

### <span data-ttu-id="3fb94-112">範例1：從檔案共用中刪除檔案</span><span class="sxs-lookup"><span data-stu-id="3fb94-112">Example 1: Delete a file from a file share</span></span>
```
PS C:\>Remove-AzureStorageFile -ShareName "ContosoShare06" -Path "ContosoFile22"
```

<span data-ttu-id="3fb94-113">這個命令會從名為 ContosoShare06 的檔案共用中刪除名為 ContosoFile22 的檔案。</span><span class="sxs-lookup"><span data-stu-id="3fb94-113">This command deletes the file that is named ContosoFile22 from the file share named ContosoShare06.</span></span>

### <span data-ttu-id="3fb94-114">範例2：使用檔案共用物件從檔案共用取得檔案</span><span class="sxs-lookup"><span data-stu-id="3fb94-114">Example 2: Get a file from a file share by using a file share object</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06" | Remove-AzureStorageFile -Path "ContosoFile22"
```

<span data-ttu-id="3fb94-115">這個命令會使用 **AzureStorageShare** Cmdlet 來取得名為 ContosoShare06 的檔案共用，然後使用管線運算子將該物件傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3fb94-115">This command uses the **Get-AzureStorageShare** cmdlet to get the file share named ContosoShare06, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3fb94-116">目前的命令會從 ContosoShare06 中刪除名為 ContosoFile22 的檔案。</span><span class="sxs-lookup"><span data-stu-id="3fb94-116">The current command deletes the file that is named ContosoFile22 from ContosoShare06.</span></span>

## <span data-ttu-id="3fb94-117">參數</span><span class="sxs-lookup"><span data-stu-id="3fb94-117">PARAMETERS</span></span>

### <span data-ttu-id="3fb94-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3fb94-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="3fb94-119">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="3fb94-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="3fb94-120">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="3fb94-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="3fb94-121">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="3fb94-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="3fb94-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="3fb94-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="3fb94-123">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="3fb94-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="3fb94-124">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="3fb94-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="3fb94-125">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="3fb94-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="3fb94-126">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="3fb94-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="3fb94-127">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="3fb94-127">The default value is 10.</span></span>

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

### <span data-ttu-id="3fb94-128">-內容</span><span class="sxs-lookup"><span data-stu-id="3fb94-128">-Context</span></span>
<span data-ttu-id="3fb94-129">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="3fb94-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="3fb94-130">若要取得儲存內容，請使用 [AzureStorageCoNtext](./New-AzureStorageContext.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3fb94-130">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="3fb94-131">-Directory</span><span class="sxs-lookup"><span data-stu-id="3fb94-131">-Directory</span></span>
<span data-ttu-id="3fb94-132">將資料夾指定為 **CloudFileDirectory** 物件。</span><span class="sxs-lookup"><span data-stu-id="3fb94-132">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="3fb94-133">這個 Cmdlet 會移除此參數指定資料夾中的檔案。</span><span class="sxs-lookup"><span data-stu-id="3fb94-133">This cmdlet removes a file in the folder that this parameter specifies.</span></span>

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

### <span data-ttu-id="3fb94-134">檔案</span><span class="sxs-lookup"><span data-stu-id="3fb94-134">-File</span></span>
<span data-ttu-id="3fb94-135">將檔案指定為 **CloudFile** 物件。</span><span class="sxs-lookup"><span data-stu-id="3fb94-135">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="3fb94-136">這個 Cmdlet 會移除此參數指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="3fb94-136">This cmdlet removes the file that this parameter specifies.</span></span>
<span data-ttu-id="3fb94-137">若要取得 **CloudFile** 物件，請使用 Get-AzureStorageFile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3fb94-137">To obtain a **CloudFile** object, use the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: CloudFile
Parameter Sets: File
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3fb94-138">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3fb94-138">-PassThru</span></span>
<span data-ttu-id="3fb94-139">表示此 Cmdlet 會傳回反映操作成功的 **布林值** 。</span><span class="sxs-lookup"><span data-stu-id="3fb94-139">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="3fb94-140">根據預設，這個 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="3fb94-140">By default, this cmdlet does not return a value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fb94-141">-Path</span><span class="sxs-lookup"><span data-stu-id="3fb94-141">-Path</span></span>
<span data-ttu-id="3fb94-142">指定檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="3fb94-142">Specifies the path of a file.</span></span>
<span data-ttu-id="3fb94-143">這個 Cmdlet 會刪除此參數指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="3fb94-143">This cmdlet deletes the file that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ShareName, Share, Directory
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fb94-144">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3fb94-144">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="3fb94-145">指定要求中伺服器部分的超時時間長度。</span><span class="sxs-lookup"><span data-stu-id="3fb94-145">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="3fb94-146">-共用</span><span class="sxs-lookup"><span data-stu-id="3fb94-146">-Share</span></span>
<span data-ttu-id="3fb94-147">指定 **CloudFileShare** 物件。</span><span class="sxs-lookup"><span data-stu-id="3fb94-147">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="3fb94-148">這個 Cmdlet 會移除此參數指定的共用中的檔案。</span><span class="sxs-lookup"><span data-stu-id="3fb94-148">This cmdlet removes the file in the share this parameter specifies.</span></span>
<span data-ttu-id="3fb94-149">若要取得 **CloudFileShare** 物件，請使用 Get-AzureStorageShare Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3fb94-149">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="3fb94-150">此物件包含儲存內容。</span><span class="sxs-lookup"><span data-stu-id="3fb94-150">This object contains the storage context.</span></span>
<span data-ttu-id="3fb94-151">如果您指定此參數，請勿指定 *CoNtext* 參數。</span><span class="sxs-lookup"><span data-stu-id="3fb94-151">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="3fb94-152">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="3fb94-152">-ShareName</span></span>
<span data-ttu-id="3fb94-153">指定檔案共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="3fb94-153">Specifies the name of the file share.</span></span>
<span data-ttu-id="3fb94-154">這個 Cmdlet 會移除此參數指定的共用中的檔案。</span><span class="sxs-lookup"><span data-stu-id="3fb94-154">This cmdlet removes the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="3fb94-155">-確認</span><span class="sxs-lookup"><span data-stu-id="3fb94-155">-Confirm</span></span>
<span data-ttu-id="3fb94-156">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3fb94-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fb94-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fb94-157">-WhatIf</span></span>
<span data-ttu-id="3fb94-158">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3fb94-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fb94-159">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3fb94-159">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fb94-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fb94-160">CommonParameters</span></span>
<span data-ttu-id="3fb94-161">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3fb94-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fb94-162">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3fb94-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fb94-163">輸入</span><span class="sxs-lookup"><span data-stu-id="3fb94-163">INPUTS</span></span>

### <span data-ttu-id="3fb94-164">IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="3fb94-164">IStorageContext</span></span>

<span data-ttu-id="3fb94-165">參數「CoNtext」接受來自管線的 "IStorageCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="3fb94-165">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="3fb94-166">CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="3fb94-166">CloudFileDirectory</span></span>

<span data-ttu-id="3fb94-167">形參 "Directory" 接受管線中 "CloudFileDirectory" 類型的值</span><span class="sxs-lookup"><span data-stu-id="3fb94-167">Parameter 'Directory' accepts value of type 'CloudFileDirectory' from the pipeline</span></span>

### <span data-ttu-id="3fb94-168">CloudFile</span><span class="sxs-lookup"><span data-stu-id="3fb94-168">CloudFile</span></span>

<span data-ttu-id="3fb94-169">形參 "File" 接受管線中 "CloudFile" 類型的值</span><span class="sxs-lookup"><span data-stu-id="3fb94-169">Parameter 'File' accepts value of type 'CloudFile' from the pipeline</span></span>

### <span data-ttu-id="3fb94-170">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="3fb94-170">CloudFileShare</span></span>

<span data-ttu-id="3fb94-171">形參 "Share" 接受管線中 "CloudFileShare" 類型的值</span><span class="sxs-lookup"><span data-stu-id="3fb94-171">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

## <span data-ttu-id="3fb94-172">輸出</span><span class="sxs-lookup"><span data-stu-id="3fb94-172">OUTPUTS</span></span>

## <span data-ttu-id="3fb94-173">筆記</span><span class="sxs-lookup"><span data-stu-id="3fb94-173">NOTES</span></span>

## <span data-ttu-id="3fb94-174">相關連結</span><span class="sxs-lookup"><span data-stu-id="3fb94-174">RELATED LINKS</span></span>

[<span data-ttu-id="3fb94-175">AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="3fb94-175">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="3fb94-176">AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="3fb94-176">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="3fb94-177">新-AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="3fb94-177">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
