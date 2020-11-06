---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 53988D79-1F8B-4138-9F92-2912D418C121
online version: ''
schema: 2.0.0
ms.openlocfilehash: bd885e79fb4daf1eec9dd8958283be28e52f920f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93442568"
---
# <span data-ttu-id="4cc1a-101">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="4cc1a-101">Remove-AzureStorageDirectory</span></span>

## <span data-ttu-id="4cc1a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4cc1a-102">SYNOPSIS</span></span>
<span data-ttu-id="4cc1a-103">刪除目錄。</span><span class="sxs-lookup"><span data-stu-id="4cc1a-103">Deletes a directory.</span></span>

## <span data-ttu-id="4cc1a-104">句法</span><span class="sxs-lookup"><span data-stu-id="4cc1a-104">SYNTAX</span></span>

### <span data-ttu-id="4cc1a-105">共用名稱 (預設) </span><span class="sxs-lookup"><span data-stu-id="4cc1a-105">ShareName (Default)</span></span>
```
Remove-AzureStorageDirectory [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cc1a-106">共用</span><span class="sxs-lookup"><span data-stu-id="4cc1a-106">Share</span></span>
```
Remove-AzureStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cc1a-107">空目錄</span><span class="sxs-lookup"><span data-stu-id="4cc1a-107">Directory</span></span>
```
Remove-AzureStorageDirectory [-Directory] <CloudFileDirectory> [[-Path] <String>] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cc1a-108">說明</span><span class="sxs-lookup"><span data-stu-id="4cc1a-108">DESCRIPTION</span></span>
<span data-ttu-id="4cc1a-109">**AzureStorageDirectory** Cmdlet 會刪除目錄。</span><span class="sxs-lookup"><span data-stu-id="4cc1a-109">The **Remove-AzureStorageDirectory** cmdlet deletes a directory.</span></span>

## <span data-ttu-id="4cc1a-110">示例</span><span class="sxs-lookup"><span data-stu-id="4cc1a-110">EXAMPLES</span></span>

### <span data-ttu-id="4cc1a-111">範例1：刪除資料夾</span><span class="sxs-lookup"><span data-stu-id="4cc1a-111">Example 1: Delete a folder</span></span>
```
PS C:\>Remove-AzureStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="4cc1a-112">這個命令會從名為 ContosoShare06 的檔案共用中刪除名為 ContosoWorkingFolder 的資料夾。</span><span class="sxs-lookup"><span data-stu-id="4cc1a-112">This command deletes the folder named ContosoWorkingFolder from the file share named ContosoShare06.</span></span>

## <span data-ttu-id="4cc1a-113">參數</span><span class="sxs-lookup"><span data-stu-id="4cc1a-113">PARAMETERS</span></span>

### <span data-ttu-id="4cc1a-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4cc1a-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="4cc1a-115">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="4cc1a-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="4cc1a-116">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="4cc1a-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="4cc1a-117">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="4cc1a-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="4cc1a-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="4cc1a-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="4cc1a-119">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="4cc1a-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="4cc1a-120">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="4cc1a-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="4cc1a-121">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="4cc1a-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="4cc1a-122">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="4cc1a-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="4cc1a-123">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="4cc1a-123">The default value is 10.</span></span>

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

### <span data-ttu-id="4cc1a-124">-內容</span><span class="sxs-lookup"><span data-stu-id="4cc1a-124">-Context</span></span>
<span data-ttu-id="4cc1a-125">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="4cc1a-125">Specifies an Azure storage context.</span></span>
<span data-ttu-id="4cc1a-126">若要取得儲存內容，請使用 [AzureStorageCoNtext](./New-AzureStorageContext.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4cc1a-126">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="4cc1a-127">-Directory</span><span class="sxs-lookup"><span data-stu-id="4cc1a-127">-Directory</span></span>
<span data-ttu-id="4cc1a-128">將資料夾指定為 **CloudFileDirectory** 物件。</span><span class="sxs-lookup"><span data-stu-id="4cc1a-128">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="4cc1a-129">這個 Cmdlet 會移除此參數指定的資料夾。</span><span class="sxs-lookup"><span data-stu-id="4cc1a-129">This cmdlet removes the folder that this parameter specifies.</span></span>
<span data-ttu-id="4cc1a-130">若要取得目錄，請使用 New-AzureStorageDirectory Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4cc1a-130">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="4cc1a-131">您也可以使用 **AzureStorageFile** Cmdlet 來取得目錄。</span><span class="sxs-lookup"><span data-stu-id="4cc1a-131">You can also use the **Get-AzureStorageFile** cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="4cc1a-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4cc1a-132">-PassThru</span></span>
<span data-ttu-id="4cc1a-133">表示如果此 Cmdlet 成功，則會傳回 $True 的值。</span><span class="sxs-lookup"><span data-stu-id="4cc1a-133">Indicates that, if this cmdlet succeeds, it returns a value of $True.</span></span>
<span data-ttu-id="4cc1a-134">如果您指定此參數，且由於 _Path_ 參數不適當的值而使 Cmdlet 不成功，則 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="4cc1a-134">If you specify this parameter, and if the cmdlet is unsuccessful because of an inappropriate value for the _Path_ parameter, the cmdlet returns an error.</span></span>
<span data-ttu-id="4cc1a-135">如果您沒有指定此參數，這個 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="4cc1a-135">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="4cc1a-136">-Path</span><span class="sxs-lookup"><span data-stu-id="4cc1a-136">-Path</span></span>
<span data-ttu-id="4cc1a-137">指定資料夾的路徑。</span><span class="sxs-lookup"><span data-stu-id="4cc1a-137">Specifies the path of a folder.</span></span>
<span data-ttu-id="4cc1a-138">如果此參數指定的資料夾為空白，這個 Cmdlet 會刪除該資料夾。</span><span class="sxs-lookup"><span data-stu-id="4cc1a-138">If the folder that this parameter specifies is empty, this cmdlet deletes that folder.</span></span>
<span data-ttu-id="4cc1a-139">如果資料夾不是空白，這個 Cmdlet 不會變更，而會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="4cc1a-139">If the folder is not empty, this cmdlet makes no change, and returns an error.</span></span>

```yaml
Type: String
Parameter Sets: ShareName, Share
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Directory
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cc1a-140">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4cc1a-140">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="4cc1a-141">指定要求中伺服器部分的超時時間長度。</span><span class="sxs-lookup"><span data-stu-id="4cc1a-141">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="4cc1a-142">-共用</span><span class="sxs-lookup"><span data-stu-id="4cc1a-142">-Share</span></span>
<span data-ttu-id="4cc1a-143">指定 **CloudFileShare** 物件。</span><span class="sxs-lookup"><span data-stu-id="4cc1a-143">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="4cc1a-144">這個 Cmdlet 會移除此參數指定之檔案共用底下的資料夾。</span><span class="sxs-lookup"><span data-stu-id="4cc1a-144">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>
<span data-ttu-id="4cc1a-145">若要取得 **CloudFileShare** 物件，請使用 Get-AzureStorageShare Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4cc1a-145">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="4cc1a-146">此物件包含儲存內容。</span><span class="sxs-lookup"><span data-stu-id="4cc1a-146">This object contains the storage context.</span></span>
<span data-ttu-id="4cc1a-147">如果您指定此參數，請勿指定 *CoNtext* 參數。</span><span class="sxs-lookup"><span data-stu-id="4cc1a-147">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="4cc1a-148">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="4cc1a-148">-ShareName</span></span>
<span data-ttu-id="4cc1a-149">指定檔案共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="4cc1a-149">Specifies the name of the file share.</span></span>
<span data-ttu-id="4cc1a-150">這個 Cmdlet 會移除此參數指定之檔案共用底下的資料夾。</span><span class="sxs-lookup"><span data-stu-id="4cc1a-150">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="4cc1a-151">-確認</span><span class="sxs-lookup"><span data-stu-id="4cc1a-151">-Confirm</span></span>
<span data-ttu-id="4cc1a-152">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4cc1a-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cc1a-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cc1a-153">-WhatIf</span></span>
<span data-ttu-id="4cc1a-154">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4cc1a-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cc1a-155">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4cc1a-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cc1a-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cc1a-156">CommonParameters</span></span>
<span data-ttu-id="4cc1a-157">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4cc1a-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cc1a-158">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4cc1a-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cc1a-159">輸入</span><span class="sxs-lookup"><span data-stu-id="4cc1a-159">INPUTS</span></span>

## <span data-ttu-id="4cc1a-160">輸出</span><span class="sxs-lookup"><span data-stu-id="4cc1a-160">OUTPUTS</span></span>

## <span data-ttu-id="4cc1a-161">筆記</span><span class="sxs-lookup"><span data-stu-id="4cc1a-161">NOTES</span></span>

## <span data-ttu-id="4cc1a-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="4cc1a-162">RELATED LINKS</span></span>

[<span data-ttu-id="4cc1a-163">AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="4cc1a-163">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="4cc1a-164">新-AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="4cc1a-164">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="4cc1a-165">新-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="4cc1a-165">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)
