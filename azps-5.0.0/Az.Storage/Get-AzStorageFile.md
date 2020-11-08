---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 38207027-FD76-45EE-8817-88599735C0B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
ms.openlocfilehash: 8251c18acad2da881c3215df6a2e743b6804af6e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137620"
---
# <span data-ttu-id="0b302-101">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="0b302-101">Get-AzStorageFile</span></span>

## <span data-ttu-id="0b302-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0b302-102">SYNOPSIS</span></span>
<span data-ttu-id="0b302-103">列出路徑的目錄和檔案。</span><span class="sxs-lookup"><span data-stu-id="0b302-103">Lists directories and files for a path.</span></span>

## <span data-ttu-id="0b302-104">句法</span><span class="sxs-lookup"><span data-stu-id="0b302-104">SYNTAX</span></span>

### <span data-ttu-id="0b302-105">共用名稱 (預設) </span><span class="sxs-lookup"><span data-stu-id="0b302-105">ShareName (Default)</span></span>
```
Get-AzStorageFile [-ShareName] <String> [[-Path] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="0b302-106">共用</span><span class="sxs-lookup"><span data-stu-id="0b302-106">Share</span></span>
```
Get-AzStorageFile [-Share] <CloudFileShare> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="0b302-107">空目錄</span><span class="sxs-lookup"><span data-stu-id="0b302-107">Directory</span></span>
```
Get-AzStorageFile [-Directory] <CloudFileDirectory> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="0b302-108">說明</span><span class="sxs-lookup"><span data-stu-id="0b302-108">DESCRIPTION</span></span>
<span data-ttu-id="0b302-109">**AzStorageFile** Cmdlet 會列出您指定的共用或目錄的目錄和檔案。</span><span class="sxs-lookup"><span data-stu-id="0b302-109">The **Get-AzStorageFile** cmdlet lists directories and files for the share or directory that you specify.</span></span>
<span data-ttu-id="0b302-110">指定 *path* 參數，以取得指定路徑中目錄或檔案的實例。</span><span class="sxs-lookup"><span data-stu-id="0b302-110">Specify the *Path* parameter to get an instance of a directory or file in the specified path.</span></span>
<span data-ttu-id="0b302-111">這個 Cmdlet 會傳回 **AzureStorageFile** 和 **AzureStorageDirectory** 物件。</span><span class="sxs-lookup"><span data-stu-id="0b302-111">This cmdlet returns **AzureStorageFile** and **AzureStorageDirectory** objects.</span></span>
<span data-ttu-id="0b302-112">您可以使用 **IsDirectory** 屬性來區分資料夾與檔案。</span><span class="sxs-lookup"><span data-stu-id="0b302-112">You can use the **IsDirectory** property to distinguish between folders and files.</span></span>

## <span data-ttu-id="0b302-113">示例</span><span class="sxs-lookup"><span data-stu-id="0b302-113">EXAMPLES</span></span>

### <span data-ttu-id="0b302-114">範例1：列出共用中的目錄</span><span class="sxs-lookup"><span data-stu-id="0b302-114">Example 1: List directories in a share</span></span>
```
PS C:\>Get-AzStorageFile -ShareName "ContosoShare06" | where {$_.GetType().Name -eq "AzureStorageFileDirectory"}
```

<span data-ttu-id="0b302-115">這個命令只會列出 [共用] ContosoShare06 中的目錄。</span><span class="sxs-lookup"><span data-stu-id="0b302-115">This command lists only the directories in the share ContosoShare06.</span></span>
<span data-ttu-id="0b302-116">它會先使用管線運算子來檢索檔案和目錄，並將它們傳到 **where** 運算子，然後捨棄類型不是 "AzureStorageFileDirectory" 的任何物件。</span><span class="sxs-lookup"><span data-stu-id="0b302-116">It first retrieves both files and directories, passes them to the **where** operator by using the pipeline operator, then discards any objects whose type is not "AzureStorageFileDirectory".</span></span>

### <span data-ttu-id="0b302-117">範例2：列出檔案目錄</span><span class="sxs-lookup"><span data-stu-id="0b302-117">Example 2: List a File Directory</span></span>
```
PS C:\> Get-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoWorkingFolder" | Get-AzStorageFile
```

<span data-ttu-id="0b302-118">這個命令會在 [共用 ContosoShare06] 底下的 [目錄 ContosoWorkingFolder] 中列出檔案和資料夾。</span><span class="sxs-lookup"><span data-stu-id="0b302-118">This command lists the files and folders in the directory ContosoWorkingFolder under the share ContosoShare06.</span></span>
<span data-ttu-id="0b302-119">它會先取得目錄實例，然後將它的管道加入 **AzStorageFile** Cmdlet，以列出該目錄。</span><span class="sxs-lookup"><span data-stu-id="0b302-119">It first gets the directory instance, and then pipelines it to the **Get-AzStorageFile** cmdlet to list the directory.</span></span>

## <span data-ttu-id="0b302-120">參數</span><span class="sxs-lookup"><span data-stu-id="0b302-120">PARAMETERS</span></span>

### <span data-ttu-id="0b302-121">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0b302-121">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="0b302-122">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="0b302-122">Specifies the client side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="0b302-123">如果上一個呼叫在指定的間隔時間內失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="0b302-123">If the previous call fails within the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="0b302-124">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="0b302-124">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="0b302-125">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="0b302-125">-ConcurrentTaskCount</span></span>
<span data-ttu-id="0b302-126">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="0b302-126">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="0b302-127">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="0b302-127">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="0b302-128">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="0b302-128">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="0b302-129">這個參數可協助減輕低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="0b302-129">This parameter can help mitigate network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="0b302-130">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="0b302-130">The default value is 10.</span></span>

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

### <span data-ttu-id="0b302-131">-內容</span><span class="sxs-lookup"><span data-stu-id="0b302-131">-Context</span></span>
<span data-ttu-id="0b302-132">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="0b302-132">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="0b302-133">若要取得儲存內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0b302-133">To obtain a Storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b302-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b302-134">-DefaultProfile</span></span>
<span data-ttu-id="0b302-135">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0b302-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b302-136">-Directory</span><span class="sxs-lookup"><span data-stu-id="0b302-136">-Directory</span></span>
<span data-ttu-id="0b302-137">將資料夾指定為 **CloudFileDirectory** 物件。</span><span class="sxs-lookup"><span data-stu-id="0b302-137">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="0b302-138">這個 Cmdlet 會取得此參數指定的資料夾。</span><span class="sxs-lookup"><span data-stu-id="0b302-138">This cmdlet gets the folder that this parameter specifies.</span></span>
<span data-ttu-id="0b302-139">若要取得目錄，請使用 New-AzStorageDirectory Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0b302-139">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="0b302-140">您也可以使用 **AzStorageFile** Cmdlet 來取得目錄。</span><span class="sxs-lookup"><span data-stu-id="0b302-140">You can also use the **Get-AzStorageFile** cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases: CloudFileDirectory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b302-141">-Path</span><span class="sxs-lookup"><span data-stu-id="0b302-141">-Path</span></span>
<span data-ttu-id="0b302-142">指定資料夾的路徑。</span><span class="sxs-lookup"><span data-stu-id="0b302-142">Specifies the path of a folder.</span></span>
<span data-ttu-id="0b302-143">如果您省略 *Path* 參數， **AzStorageFile** 會列出指定檔案共用或目錄中的目錄和檔案。</span><span class="sxs-lookup"><span data-stu-id="0b302-143">If you omit the *Path* parameter, **Get-AzStorageFile** lists the directories and files in the specified file share or directory.</span></span>
<span data-ttu-id="0b302-144">如果您包含 *Path* 參數，則 **AzStorageFile** 會傳回指定路徑中目錄或檔案的實例。</span><span class="sxs-lookup"><span data-stu-id="0b302-144">If you include the *Path* parameter, **Get-AzStorageFile** returns an instance of a directory or file in the specified path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b302-145">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0b302-145">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="0b302-146">指定要求的服務端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="0b302-146">Specifies the service-side timeout interval, in seconds, for a request.</span></span>
<span data-ttu-id="0b302-147">如果所指定的間隔在服務處理要求之前就已到期，儲存服務就會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="0b302-147">If the specified interval elapses before the service processes the request, the Storage service returns an error.</span></span>

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

### <span data-ttu-id="0b302-148">-共用</span><span class="sxs-lookup"><span data-stu-id="0b302-148">-Share</span></span>
<span data-ttu-id="0b302-149">指定 **CloudFileShare** 物件。</span><span class="sxs-lookup"><span data-stu-id="0b302-149">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="0b302-150">這個 Cmdlet 會從此參數指定的檔案共用取得檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="0b302-150">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>
<span data-ttu-id="0b302-151">若要取得 **CloudFileShare** 物件，請使用 Get-AzStorageShare Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0b302-151">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="0b302-152">此物件包含儲存內容。</span><span class="sxs-lookup"><span data-stu-id="0b302-152">This object contains the Storage context.</span></span>
<span data-ttu-id="0b302-153">如果您指定此參數，請勿指定 *CoNtext* 參數。</span><span class="sxs-lookup"><span data-stu-id="0b302-153">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b302-154">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="0b302-154">-ShareName</span></span>
<span data-ttu-id="0b302-155">指定檔案共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="0b302-155">Specifies the name of the file share.</span></span>
<span data-ttu-id="0b302-156">這個 Cmdlet 會從此參數指定的檔案共用取得檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="0b302-156">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b302-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b302-157">CommonParameters</span></span>
<span data-ttu-id="0b302-158">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0b302-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b302-159">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0b302-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b302-160">輸入</span><span class="sxs-lookup"><span data-stu-id="0b302-160">INPUTS</span></span>

### <span data-ttu-id="0b302-161">CloudFileShare （即 Azure）</span><span class="sxs-lookup"><span data-stu-id="0b302-161">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="0b302-162">CloudFileDirectory （即 Azure）</span><span class="sxs-lookup"><span data-stu-id="0b302-162">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="0b302-163">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="0b302-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0b302-164">輸出</span><span class="sxs-lookup"><span data-stu-id="0b302-164">OUTPUTS</span></span>

### <span data-ttu-id="0b302-165">AzureStorageFile WindowsAzure. ResourceModel。</span><span class="sxs-lookup"><span data-stu-id="0b302-165">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="0b302-166">筆記</span><span class="sxs-lookup"><span data-stu-id="0b302-166">NOTES</span></span>

## <span data-ttu-id="0b302-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="0b302-167">RELATED LINKS</span></span>

[<span data-ttu-id="0b302-168">AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="0b302-168">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)

[<span data-ttu-id="0b302-169">新-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="0b302-169">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="0b302-170">移除-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="0b302-170">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)

[<span data-ttu-id="0b302-171">移除-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="0b302-171">Remove-AzStorageFile</span></span>](./Remove-AzStorageFile.md)

[<span data-ttu-id="0b302-172">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="0b302-172">Set-AzStorageFileContent</span></span>](./Set-AzStorageFileContent.md)

