---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FA98E64B-D589-4653-9ACC-86573FAF4550
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageFileContent.md
ms.openlocfilehash: 5f2aed68aea9f97b3dd66a5322d332d4666c081e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626465"
---
# <span data-ttu-id="04299-101">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="04299-101">Set-AzureStorageFileContent</span></span>

## <span data-ttu-id="04299-102">摘要</span><span class="sxs-lookup"><span data-stu-id="04299-102">SYNOPSIS</span></span>
<span data-ttu-id="04299-103">上傳檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="04299-103">Uploads the contents of a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04299-104">句法</span><span class="sxs-lookup"><span data-stu-id="04299-104">SYNTAX</span></span>

### <span data-ttu-id="04299-105">共用名稱 (預設) </span><span class="sxs-lookup"><span data-stu-id="04299-105">ShareName (Default)</span></span>
```
Set-AzureStorageFileContent [-ShareName] <String> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04299-106">共用</span><span class="sxs-lookup"><span data-stu-id="04299-106">Share</span></span>
```
Set-AzureStorageFileContent [-Share] <CloudFileShare> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04299-107">空目錄</span><span class="sxs-lookup"><span data-stu-id="04299-107">Directory</span></span>
```
Set-AzureStorageFileContent [-Directory] <CloudFileDirectory> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04299-108">說明</span><span class="sxs-lookup"><span data-stu-id="04299-108">DESCRIPTION</span></span>
<span data-ttu-id="04299-109">**AzureStorageFileContent** Cmdlet 會將檔案的內容上傳到指定共用上的檔案。</span><span class="sxs-lookup"><span data-stu-id="04299-109">The **Set-AzureStorageFileContent** cmdlet uploads the contents of a file to a file on a specified share.</span></span>

## <span data-ttu-id="04299-110">示例</span><span class="sxs-lookup"><span data-stu-id="04299-110">EXAMPLES</span></span>

### <span data-ttu-id="04299-111">範例1：上傳目前資料夾中的檔案</span><span class="sxs-lookup"><span data-stu-id="04299-111">Example 1: Upload a file in the current folder</span></span>
```
PS C:\>Set-AzureStorageFileContent -ShareName "ContosoShare06" -Source "DataFile37" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="04299-112">這個命令會將目前資料夾中的名為 DataFile37 的檔案，上傳為名為 CurrentDataFile 的檔案，該檔案名為 [ContosoWorkingFolder] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="04299-112">This command uploads a file that is named DataFile37 in the current folder as a file that is named CurrentDataFile in the folder named ContosoWorkingFolder.</span></span>

### <span data-ttu-id="04299-113">範例2：上傳目前資料夾中的所有檔案</span><span class="sxs-lookup"><span data-stu-id="04299-113">Example 2: Upload all the files in the current folder</span></span>
```
PS C:\>$CurrentFolder = (Get-Item .).FullName
PS C:\> $Container = Get-AzureStorageShare -Name "ContosoShare06"
PS C:\> Get-ChildItem -Recurse | Where-Object { $_.GetType().Name -eq "FileInfo"} | ForEach-Object {
    $path=$_.FullName.Substring($Currentfolder.Length+1).Replace("\","/")
    Set-AzureStorageFileContent -Share $Container -Source $_.FullName -Path $path -Force
}
```

<span data-ttu-id="04299-114">這個範例使用幾個常見的 Windows PowerShell Cmdlet 和目前的 Cmdlet，將目前資料夾中的所有檔案上傳到容器 ContosoShare06 的根資料夾。</span><span class="sxs-lookup"><span data-stu-id="04299-114">This example uses several common Windows PowerShell cmdlets and the current cmdlet to upload all files from the current folder to the root folder of container ContosoShare06.</span></span>

<span data-ttu-id="04299-115">第一個命令會取得目前資料夾的名稱，並將它儲存在 $CurrentFolder 變數中。</span><span class="sxs-lookup"><span data-stu-id="04299-115">The first command gets the name of the current folder and stores it in the $CurrentFolder variable.</span></span>

<span data-ttu-id="04299-116">第二個命令使用 **AzureStorageShare** Cmdlet 來取得名為 ContosoShare06 的檔案共用，然後將它儲存在 $Container 變數中。</span><span class="sxs-lookup"><span data-stu-id="04299-116">The second command uses the **Get-AzureStorageShare** cmdlet to get the file share named ContosoShare06, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="04299-117">最後一個命令會透過使用管線運算子來取得目前資料夾的內容，並將每個專案傳遞給 Where-Object Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="04299-117">The final command gets the contents of the current folder and passes each one to the Where-Object cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="04299-118">該 Cmdlet 會篩選掉不是檔案的物件，然後將檔案傳遞到 ForEach-Object Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="04299-118">That cmdlet filters out objects that are not files, and then passes the files to the ForEach-Object cmdlet.</span></span>
<span data-ttu-id="04299-119">該 Cmdlet 會針對針對其建立適當路徑的每個檔案執行腳本區塊，然後使用目前的 Cmdlet 來上傳檔案。</span><span class="sxs-lookup"><span data-stu-id="04299-119">That cmdlet runs a script block for each file that creates the appropriate path for it and then uses the current cmdlet to upload the file.</span></span>
<span data-ttu-id="04299-120">結果的名稱與此範例上傳之其他檔案的相對位置相同。</span><span class="sxs-lookup"><span data-stu-id="04299-120">The result has the same name and same relative position with regard to the other files that this example uploads.</span></span>
<span data-ttu-id="04299-121">如需腳本區塊的詳細資訊，請輸入 `Get-Help about_Script_Blocks` 。</span><span class="sxs-lookup"><span data-stu-id="04299-121">For more information about script blocks, type `Get-Help about_Script_Blocks`.</span></span>

## <span data-ttu-id="04299-122">參數</span><span class="sxs-lookup"><span data-stu-id="04299-122">PARAMETERS</span></span>

### <span data-ttu-id="04299-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="04299-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="04299-124">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="04299-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="04299-125">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="04299-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="04299-126">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="04299-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="04299-127">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="04299-127">-ConcurrentTaskCount</span></span>
<span data-ttu-id="04299-128">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="04299-128">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="04299-129">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="04299-129">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="04299-130">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="04299-130">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="04299-131">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="04299-131">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="04299-132">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="04299-132">The default value is 10.</span></span>

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

### <span data-ttu-id="04299-133">-內容</span><span class="sxs-lookup"><span data-stu-id="04299-133">-Context</span></span>
<span data-ttu-id="04299-134">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="04299-134">Specifies an Azure storage context.</span></span>
<span data-ttu-id="04299-135">若要取得儲存內容，請使用 [AzureStorageCoNtext](./New-AzureStorageContext.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="04299-135">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="04299-136">-Directory</span><span class="sxs-lookup"><span data-stu-id="04299-136">-Directory</span></span>
<span data-ttu-id="04299-137">將資料夾指定為 **CloudFileDirectory** 物件。</span><span class="sxs-lookup"><span data-stu-id="04299-137">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="04299-138">這個 Cmdlet 會將檔案上傳到此參數指定的資料夾中。</span><span class="sxs-lookup"><span data-stu-id="04299-138">This cmdlet uploads the file to the folder that this parameter specifies.</span></span>
<span data-ttu-id="04299-139">若要取得目錄，請使用 New-AzureStorageDirectory Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="04299-139">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="04299-140">您也可以使用 Get-AzureStorageFile Cmdlet 來取得目錄。</span><span class="sxs-lookup"><span data-stu-id="04299-140">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="04299-141">-Force</span><span class="sxs-lookup"><span data-stu-id="04299-141">-Force</span></span>
<span data-ttu-id="04299-142">表示此 Cmdlet 會覆寫現有的 Azure 儲存空間檔案。</span><span class="sxs-lookup"><span data-stu-id="04299-142">Indicates that this cmdlet overwrites an existing Azure storage file.</span></span>

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

### <span data-ttu-id="04299-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="04299-143">-PassThru</span></span>
<span data-ttu-id="04299-144">表示此 Cmdlet 會傳回它所建立或上傳的 **AzureStorageFile** 物件。</span><span class="sxs-lookup"><span data-stu-id="04299-144">Indicates that this cmdlet returns the **AzureStorageFile** object that it creates or uploads.</span></span>

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

### <span data-ttu-id="04299-145">-Path</span><span class="sxs-lookup"><span data-stu-id="04299-145">-Path</span></span>
<span data-ttu-id="04299-146">指定檔案或資料夾的路徑。</span><span class="sxs-lookup"><span data-stu-id="04299-146">Specifies the path of a file or folder.</span></span>
<span data-ttu-id="04299-147">這個 Cmdlet 會將內容上傳到此參數指定的檔案，或傳給此參數指定之資料夾中的檔案。</span><span class="sxs-lookup"><span data-stu-id="04299-147">This cmdlet uploads contents to the file that this parameter specifies, or to a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="04299-148">如果您指定資料夾，這個 Cmdlet 會建立與來源檔案同名的檔案。</span><span class="sxs-lookup"><span data-stu-id="04299-148">If you specify a folder, this cmdlet creates a file that has the same name as the source file.</span></span>

<span data-ttu-id="04299-149">如果您指定不存在之檔案的路徑，這個 Cmdlet 會建立該檔案，並將內容儲存到該檔案。</span><span class="sxs-lookup"><span data-stu-id="04299-149">If you specify a path of a file that does not exist, this cmdlet creates that file and saves the contents to that file.</span></span>
<span data-ttu-id="04299-150">如果您指定的檔案已經存在，而且您指定了 _Force_ 參數，這個 Cmdlet 會覆寫檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="04299-150">If you specify a file that already exists, and you specify the _Force_ parameter, this cmdlet overwrites the contents of the file.</span></span>
<span data-ttu-id="04299-151">如果您指定的檔案已經存在，而您沒有指定 _Force_ ，這個 Cmdlet 不會變更，而且會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="04299-151">If you specify a file that already exists and you do not specify _Force_ , this cmdlet makes no change, and returns an error.</span></span>

<span data-ttu-id="04299-152">如果您指定的資料夾路徑不存在，這個 Cmdlet 不會變更，而且會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="04299-152">If you specify a path of a folder that does not exist, this cmdlet makes no change, and returns an error.</span></span>


```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04299-153">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="04299-153">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="04299-154">指定要求中伺服器部分的超時時間長度。</span><span class="sxs-lookup"><span data-stu-id="04299-154">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="04299-155">-共用</span><span class="sxs-lookup"><span data-stu-id="04299-155">-Share</span></span>
<span data-ttu-id="04299-156">指定 **CloudFileShare** 物件。</span><span class="sxs-lookup"><span data-stu-id="04299-156">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="04299-157">這個 Cmdlet 會在檔案共用此參數指定的檔案上傳到檔案。</span><span class="sxs-lookup"><span data-stu-id="04299-157">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>
<span data-ttu-id="04299-158">若要取得 **CloudFileShare** 物件，請使用 Get-AzureStorageShare Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="04299-158">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="04299-159">此物件包含儲存內容。</span><span class="sxs-lookup"><span data-stu-id="04299-159">This object contains the storage context.</span></span>
<span data-ttu-id="04299-160">如果您指定此參數，請勿指定 *CoNtext* 參數。</span><span class="sxs-lookup"><span data-stu-id="04299-160">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="04299-161">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="04299-161">-ShareName</span></span>
<span data-ttu-id="04299-162">指定檔案共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="04299-162">Specifies the name of the file share.</span></span>
<span data-ttu-id="04299-163">這個 Cmdlet 會在檔案共用此參數指定的檔案上傳到檔案。</span><span class="sxs-lookup"><span data-stu-id="04299-163">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>

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

### <span data-ttu-id="04299-164">-來源</span><span class="sxs-lookup"><span data-stu-id="04299-164">-Source</span></span>
<span data-ttu-id="04299-165">指定此 Cmdlet 上傳的來源檔案。</span><span class="sxs-lookup"><span data-stu-id="04299-165">Specifies the source file that this cmdlet uploads.</span></span>
<span data-ttu-id="04299-166">如果您指定的檔案不存在，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="04299-166">If you specify a file that does not exist, this cmdlet returns an error.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: FullName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04299-167">-確認</span><span class="sxs-lookup"><span data-stu-id="04299-167">-Confirm</span></span>
<span data-ttu-id="04299-168">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="04299-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04299-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04299-169">-WhatIf</span></span>
<span data-ttu-id="04299-170">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="04299-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04299-171">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="04299-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04299-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04299-172">CommonParameters</span></span>
<span data-ttu-id="04299-173">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="04299-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04299-174">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="04299-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04299-175">輸入</span><span class="sxs-lookup"><span data-stu-id="04299-175">INPUTS</span></span>

### <span data-ttu-id="04299-176">IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="04299-176">IStorageContext</span></span>

<span data-ttu-id="04299-177">參數「CoNtext」接受來自管線的 "IStorageCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="04299-177">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="04299-178">CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="04299-178">CloudFileDirectory</span></span>

<span data-ttu-id="04299-179">形參 "Directory" 接受管線中 "CloudFileDirectory" 類型的值</span><span class="sxs-lookup"><span data-stu-id="04299-179">Parameter 'Directory' accepts value of type 'CloudFileDirectory' from the pipeline</span></span>

### <span data-ttu-id="04299-180">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="04299-180">CloudFileShare</span></span>

<span data-ttu-id="04299-181">形參 "Share" 接受管線中 "CloudFileShare" 類型的值</span><span class="sxs-lookup"><span data-stu-id="04299-181">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

## <span data-ttu-id="04299-182">輸出</span><span class="sxs-lookup"><span data-stu-id="04299-182">OUTPUTS</span></span>

## <span data-ttu-id="04299-183">筆記</span><span class="sxs-lookup"><span data-stu-id="04299-183">NOTES</span></span>

## <span data-ttu-id="04299-184">相關連結</span><span class="sxs-lookup"><span data-stu-id="04299-184">RELATED LINKS</span></span>

[<span data-ttu-id="04299-185">移除-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="04299-185">Remove-AzureStorageDirectory</span></span>](./Remove-AzureStorageDirectory.md)

[<span data-ttu-id="04299-186">新-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="04299-186">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)

[<span data-ttu-id="04299-187">AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="04299-187">Get-AzureStorageFileContent</span></span>](./Get-AzureStorageFileContent.md)
