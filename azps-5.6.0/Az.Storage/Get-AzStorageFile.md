---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 38207027-FD76-45EE-8817-88599735C0B0
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
ms.openlocfilehash: e61171faba3661ad1d518641655ad87f06771ae6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913650"
---
# <span data-ttu-id="55e13-101">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="55e13-101">Get-AzStorageFile</span></span>

## <span data-ttu-id="55e13-102">簡介</span><span class="sxs-lookup"><span data-stu-id="55e13-102">SYNOPSIS</span></span>
<span data-ttu-id="55e13-103">列出路徑的目錄和檔案。</span><span class="sxs-lookup"><span data-stu-id="55e13-103">Lists directories and files for a path.</span></span>

## <span data-ttu-id="55e13-104">語法</span><span class="sxs-lookup"><span data-stu-id="55e13-104">SYNTAX</span></span>

### <span data-ttu-id="55e13-105">ShareName (預設) </span><span class="sxs-lookup"><span data-stu-id="55e13-105">ShareName (Default)</span></span>
```
Get-AzStorageFile [-ShareName] <String> [[-Path] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="55e13-106">共用</span><span class="sxs-lookup"><span data-stu-id="55e13-106">Share</span></span>
```
Get-AzStorageFile [-Share] <CloudFileShare> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="55e13-107">目錄</span><span class="sxs-lookup"><span data-stu-id="55e13-107">Directory</span></span>
```
Get-AzStorageFile [-Directory] <CloudFileDirectory> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="55e13-108">描述</span><span class="sxs-lookup"><span data-stu-id="55e13-108">DESCRIPTION</span></span>
<span data-ttu-id="55e13-109">**Get-AzStorageFile** Cmdlet 會列出您指定的共用或目錄目錄和檔案。</span><span class="sxs-lookup"><span data-stu-id="55e13-109">The **Get-AzStorageFile** cmdlet lists directories and files for the share or directory that you specify.</span></span>
<span data-ttu-id="55e13-110">指定 *Path* 參數，以取得指定路徑中的目錄或檔案實例。</span><span class="sxs-lookup"><span data-stu-id="55e13-110">Specify the *Path* parameter to get an instance of a directory or file in the specified path.</span></span>
<span data-ttu-id="55e13-111">此 Cmdlet 會 **返回 AzureStorageFile** 和 **AzureStorageDirectory** 物件。</span><span class="sxs-lookup"><span data-stu-id="55e13-111">This cmdlet returns **AzureStorageFile** and **AzureStorageDirectory** objects.</span></span>
<span data-ttu-id="55e13-112">您可以使用 **IsDirectory** 屬性來區分資料夾和檔案。</span><span class="sxs-lookup"><span data-stu-id="55e13-112">You can use the **IsDirectory** property to distinguish between folders and files.</span></span>

## <span data-ttu-id="55e13-113">例子</span><span class="sxs-lookup"><span data-stu-id="55e13-113">EXAMPLES</span></span>

### <span data-ttu-id="55e13-114">範例 1：列出共用中的目錄</span><span class="sxs-lookup"><span data-stu-id="55e13-114">Example 1: List directories in a share</span></span>
```
PS C:\>Get-AzStorageFile -ShareName "ContosoShare06" | where {$_.GetType().Name -eq "AzureStorageFileDirectory"}
```

<span data-ttu-id="55e13-115">此命令只會列出共用 ContosoShare06 中的目錄。</span><span class="sxs-lookup"><span data-stu-id="55e13-115">This command lists only the directories in the share ContosoShare06.</span></span>
<span data-ttu-id="55e13-116">它首先會同時取回檔案和目錄，然後使用管線運算子將它們傳遞給 **where** 運算子，然後捨棄類型不是 "AzureStorageFileDirectory" 的任何物件。</span><span class="sxs-lookup"><span data-stu-id="55e13-116">It first retrieves both files and directories, passes them to the **where** operator by using the pipeline operator, then discards any objects whose type is not "AzureStorageFileDirectory".</span></span>

### <span data-ttu-id="55e13-117">範例 2：列出檔案目錄</span><span class="sxs-lookup"><span data-stu-id="55e13-117">Example 2: List a File Directory</span></span>
```
PS C:\> Get-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoWorkingFolder" | Get-AzStorageFile
```

<span data-ttu-id="55e13-118">此命令會列出 Share ContosoShare06 下目錄 ContosoWorkingFolder 中的檔案和資料夾。</span><span class="sxs-lookup"><span data-stu-id="55e13-118">This command lists the files and folders in the directory ContosoWorkingFolder under the share ContosoShare06.</span></span>
<span data-ttu-id="55e13-119">它首先會取得目錄實例，然後將它管線到 **Get-AzStorageFile** Cmdlet 以列出目錄。</span><span class="sxs-lookup"><span data-stu-id="55e13-119">It first gets the directory instance, and then pipelines it to the **Get-AzStorageFile** cmdlet to list the directory.</span></span>

## <span data-ttu-id="55e13-120">參數</span><span class="sxs-lookup"><span data-stu-id="55e13-120">PARAMETERS</span></span>

### <span data-ttu-id="55e13-121">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="55e13-121">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="55e13-122">指定一個服務要求用戶端的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="55e13-122">Specifies the client side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="55e13-123">如果前一個通話在指定的時間間隔內失敗，此 Cmdlet 會重新重試要求。</span><span class="sxs-lookup"><span data-stu-id="55e13-123">If the previous call fails within the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="55e13-124">如果此 Cmdlet 在間隔經過之前未收到成功回應，此 Cmdlet 會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="55e13-124">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="55e13-125">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="55e13-125">-ConcurrentTaskCount</span></span>
<span data-ttu-id="55e13-126">指定同時進行的最大網路通話數。</span><span class="sxs-lookup"><span data-stu-id="55e13-126">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="55e13-127">您可以使用此參數來限制並行，以節流本地 CPU 和頻寬使用量，方法為指定並行網路通話的數量上限。</span><span class="sxs-lookup"><span data-stu-id="55e13-127">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="55e13-128">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="55e13-128">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="55e13-129">此參數可協助減輕低頻寬環境的網路連接問題，例如每秒 100 KB。</span><span class="sxs-lookup"><span data-stu-id="55e13-129">This parameter can help mitigate network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="55e13-130">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="55e13-130">The default value is 10.</span></span>

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

### <span data-ttu-id="55e13-131">-內容</span><span class="sxs-lookup"><span data-stu-id="55e13-131">-Context</span></span>
<span data-ttu-id="55e13-132">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="55e13-132">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="55e13-133">若要取得儲存內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="55e13-133">To obtain a Storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="55e13-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55e13-134">-DefaultProfile</span></span>
<span data-ttu-id="55e13-135">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="55e13-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55e13-136">-目錄</span><span class="sxs-lookup"><span data-stu-id="55e13-136">-Directory</span></span>
<span data-ttu-id="55e13-137">將資料夾指定為 **CloudFileDirectory** 物件。</span><span class="sxs-lookup"><span data-stu-id="55e13-137">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="55e13-138">此 Cmdlet 會獲得此參數指定的資料夾。</span><span class="sxs-lookup"><span data-stu-id="55e13-138">This cmdlet gets the folder that this parameter specifies.</span></span>
<span data-ttu-id="55e13-139">若要取得目錄，請使用 New-AzStorageDirectory Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="55e13-139">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="55e13-140">您也可以使用 **Get-AzStorageFile** Cmdlet 取得目錄。</span><span class="sxs-lookup"><span data-stu-id="55e13-140">You can also use the **Get-AzStorageFile** cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="55e13-141">-路徑</span><span class="sxs-lookup"><span data-stu-id="55e13-141">-Path</span></span>
<span data-ttu-id="55e13-142">指定資料夾的路徑。</span><span class="sxs-lookup"><span data-stu-id="55e13-142">Specifies the path of a folder.</span></span>
<span data-ttu-id="55e13-143">如果您省略 *Path* 參數 **，Get-AzStorageFile** 會列出指定檔案共用或目錄中的目錄和檔案。</span><span class="sxs-lookup"><span data-stu-id="55e13-143">If you omit the *Path* parameter, **Get-AzStorageFile** lists the directories and files in the specified file share or directory.</span></span>
<span data-ttu-id="55e13-144">如果您包含 *Path* 參數 **，Get-AzStorageFile** 會以指定的路徑，將目錄或檔案的例項。</span><span class="sxs-lookup"><span data-stu-id="55e13-144">If you include the *Path* parameter, **Get-AzStorageFile** returns an instance of a directory or file in the specified path.</span></span>

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

### <span data-ttu-id="55e13-145">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="55e13-145">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="55e13-146">指定要求的服務端逾時間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="55e13-146">Specifies the service-side timeout interval, in seconds, for a request.</span></span>
<span data-ttu-id="55e13-147">如果指定的時間間隔在服務處理要求之前已經過，儲存服務會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="55e13-147">If the specified interval elapses before the service processes the request, the Storage service returns an error.</span></span>

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

### <span data-ttu-id="55e13-148">-共用</span><span class="sxs-lookup"><span data-stu-id="55e13-148">-Share</span></span>
<span data-ttu-id="55e13-149">指定 **CloudFileShare** 物件。</span><span class="sxs-lookup"><span data-stu-id="55e13-149">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="55e13-150">此 Cmdlet 會從此參數指定的檔案共用中，獲得檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="55e13-150">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>
<span data-ttu-id="55e13-151">若要取得 **CloudFileShare** 物件，請使用 Get-AzStorageShare Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="55e13-151">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="55e13-152">此物件包含儲存內容。</span><span class="sxs-lookup"><span data-stu-id="55e13-152">This object contains the Storage context.</span></span>
<span data-ttu-id="55e13-153">如果您指定此參數，請勿指定 *CoNtext* 參數。</span><span class="sxs-lookup"><span data-stu-id="55e13-153">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="55e13-154">-ShareName</span><span class="sxs-lookup"><span data-stu-id="55e13-154">-ShareName</span></span>
<span data-ttu-id="55e13-155">指定檔案共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="55e13-155">Specifies the name of the file share.</span></span>
<span data-ttu-id="55e13-156">此 Cmdlet 會從此參數指定的檔案共用中，獲得檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="55e13-156">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="55e13-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55e13-157">CommonParameters</span></span>
<span data-ttu-id="55e13-158">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="55e13-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55e13-159">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="55e13-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55e13-160">輸入</span><span class="sxs-lookup"><span data-stu-id="55e13-160">INPUTS</span></span>

### <span data-ttu-id="55e13-161">Microsoft.Azure.storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="55e13-161">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="55e13-162">Microsoft.Azure.storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="55e13-162">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="55e13-163">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="55e13-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="55e13-164">輸出</span><span class="sxs-lookup"><span data-stu-id="55e13-164">OUTPUTS</span></span>

### <span data-ttu-id="55e13-165">Microsoft.WindowsAzure.Commands.Common.storage.ResourceModel.AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="55e13-165">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="55e13-166">筆記</span><span class="sxs-lookup"><span data-stu-id="55e13-166">NOTES</span></span>

## <span data-ttu-id="55e13-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="55e13-167">RELATED LINKS</span></span>

[<span data-ttu-id="55e13-168">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="55e13-168">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)

[<span data-ttu-id="55e13-169">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="55e13-169">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="55e13-170">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="55e13-170">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)

[<span data-ttu-id="55e13-171">Remove-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="55e13-171">Remove-AzStorageFile</span></span>](./Remove-AzStorageFile.md)

[<span data-ttu-id="55e13-172">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="55e13-172">Set-AzStorageFileContent</span></span>](./Set-AzStorageFileContent.md)


