---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
ms.openlocfilehash: 3c90e02194fa761bbb0fc00e11ea09d03ca00c1c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127343"
---
# <span data-ttu-id="be2ae-101">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="be2ae-101">Get-AzStorageFileContent</span></span>

## <span data-ttu-id="be2ae-102">摘要</span><span class="sxs-lookup"><span data-stu-id="be2ae-102">SYNOPSIS</span></span>
<span data-ttu-id="be2ae-103">下載檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="be2ae-103">Downloads the contents of a file.</span></span>

## <span data-ttu-id="be2ae-104">句法</span><span class="sxs-lookup"><span data-stu-id="be2ae-104">SYNTAX</span></span>

### <span data-ttu-id="be2ae-105">共用名稱 (預設) </span><span class="sxs-lookup"><span data-stu-id="be2ae-105">ShareName (Default)</span></span>
```
Get-AzStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="be2ae-106">共用</span><span class="sxs-lookup"><span data-stu-id="be2ae-106">Share</span></span>
```
Get-AzStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="be2ae-107">空目錄</span><span class="sxs-lookup"><span data-stu-id="be2ae-107">Directory</span></span>
```
Get-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="be2ae-108">檔案</span><span class="sxs-lookup"><span data-stu-id="be2ae-108">File</span></span>
```
Get-AzStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

## <span data-ttu-id="be2ae-109">說明</span><span class="sxs-lookup"><span data-stu-id="be2ae-109">DESCRIPTION</span></span>
<span data-ttu-id="be2ae-110">**AzStorageFileContent** Cmdlet 會下載檔案的內容，然後將檔案儲存到您指定的目的地。</span><span class="sxs-lookup"><span data-stu-id="be2ae-110">The **Get-AzStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="be2ae-111">這個 Cmdlet 不會傳回檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="be2ae-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="be2ae-112">示例</span><span class="sxs-lookup"><span data-stu-id="be2ae-112">EXAMPLES</span></span>

### <span data-ttu-id="be2ae-113">範例1：從資料夾下載檔案</span><span class="sxs-lookup"><span data-stu-id="be2ae-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="be2ae-114">這個命令會將資料夾 ContosoWorkingFolder 中名為 CurrentDataFile 的檔案從 [檔案共用] ContosoShare06 下載到 [目前] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="be2ae-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

### <span data-ttu-id="be2ae-115">範例2：下載 [範例檔案共用] 下的檔案</span><span class="sxs-lookup"><span data-stu-id="be2ae-115">Example 2: Downloads the files under sample file share</span></span>
```
PS C:\>Get-AzStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzStorageFileContent
```

<span data-ttu-id="be2ae-116">這個範例會下載 [範例檔案共用] 下的檔案</span><span class="sxs-lookup"><span data-stu-id="be2ae-116">This example downloads the files under sample file share</span></span>

### <span data-ttu-id="be2ae-117">範例3：下載 Azure 檔案至本機檔案，並 perserve Azure File SMB 屬性 (檔案 Attributtes、檔案建立時間、檔案上次寫入時間) 在本機檔案中。</span><span class="sxs-lookup"><span data-stu-id="be2ae-117">Example 3: Download an Azure file to a local file, and perserve the Azure File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the local file.</span></span>
```
PS C:\>Get-AzStorageFileContent -ShareName sample -Path "dir1/file1" -Destination $localFilePath -PreserveSMBAttribute
```

<span data-ttu-id="be2ae-118">這個範例會將 Azure 檔案下載到本機檔案，並 perserves Azure File SMB 屬性 (檔案 Attributtes、檔案建立時間、檔案上一次寫入時間) 在本機檔案中。</span><span class="sxs-lookup"><span data-stu-id="be2ae-118">This example downloads an Azure file to a local file, and perserves the Azure File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the local file.</span></span>

## <span data-ttu-id="be2ae-119">參數</span><span class="sxs-lookup"><span data-stu-id="be2ae-119">PARAMETERS</span></span>

### <span data-ttu-id="be2ae-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="be2ae-120">-AsJob</span></span>
<span data-ttu-id="be2ae-121">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="be2ae-121">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="be2ae-122">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="be2ae-122">-CheckMd5</span></span>
<span data-ttu-id="be2ae-123">指定是否要檢查已下載檔案的 Md5 加總。</span><span class="sxs-lookup"><span data-stu-id="be2ae-123">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="be2ae-124">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="be2ae-124">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="be2ae-125">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="be2ae-125">Specifies the client-side time-out interval, in seconds, for one service request.</span></span> <span data-ttu-id="be2ae-126">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="be2ae-126">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span> <span data-ttu-id="be2ae-127">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="be2ae-127">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="be2ae-128">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="be2ae-128">-ConcurrentTaskCount</span></span>
<span data-ttu-id="be2ae-129">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="be2ae-129">Specifies the maximum concurrent network calls.</span></span> <span data-ttu-id="be2ae-130">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="be2ae-130">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span> <span data-ttu-id="be2ae-131">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="be2ae-131">The specified value is an absolute count and is not multiplied by the core count.</span></span> <span data-ttu-id="be2ae-132">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="be2ae-132">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span> <span data-ttu-id="be2ae-133">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="be2ae-133">The default value is 10.</span></span>

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

### <span data-ttu-id="be2ae-134">-內容</span><span class="sxs-lookup"><span data-stu-id="be2ae-134">-Context</span></span>
<span data-ttu-id="be2ae-135">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="be2ae-135">Specifies an Azure Storage context.</span></span> <span data-ttu-id="be2ae-136">若要取得內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="be2ae-136">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="be2ae-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be2ae-137">-DefaultProfile</span></span>
<span data-ttu-id="be2ae-138">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="be2ae-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be2ae-139">-目的地</span><span class="sxs-lookup"><span data-stu-id="be2ae-139">-Destination</span></span>
<span data-ttu-id="be2ae-140">指定目的地路徑。</span><span class="sxs-lookup"><span data-stu-id="be2ae-140">Specifies the destination path.</span></span>
<span data-ttu-id="be2ae-141">這個 Cmdlet 會將檔案內容下載到此參數指定的位置。</span><span class="sxs-lookup"><span data-stu-id="be2ae-141">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>
<span data-ttu-id="be2ae-142">如果您指定不存在之檔案的路徑，此 Cmdlet 會建立該檔案，並將內容儲存到新檔案中。</span><span class="sxs-lookup"><span data-stu-id="be2ae-142">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="be2ae-143">如果您指定的檔案路徑已存在，而且您指定了 *Force* 參數，則 Cmdlet 會覆寫該檔案。</span><span class="sxs-lookup"><span data-stu-id="be2ae-143">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="be2ae-144">如果您指定現有檔案的路徑，而您沒有指定 *Force*，則 Cmdlet 會在繼續之前提示您。</span><span class="sxs-lookup"><span data-stu-id="be2ae-144">If you specify a path of an existing file and you do not specify *Force*, the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="be2ae-145">如果您指定資料夾的路徑，這個 Cmdlet 會嘗試建立具有 Azure 儲存空間檔案名稱的檔案。</span><span class="sxs-lookup"><span data-stu-id="be2ae-145">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be2ae-146">-Directory</span><span class="sxs-lookup"><span data-stu-id="be2ae-146">-Directory</span></span>
<span data-ttu-id="be2ae-147">將資料夾指定為 **CloudFileDirectory** 物件。</span><span class="sxs-lookup"><span data-stu-id="be2ae-147">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="be2ae-148">這個 Cmdlet 會取得此參數指定之資料夾中檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="be2ae-148">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="be2ae-149">若要取得目錄，請使用 New-AzStorageDirectory Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="be2ae-149">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="be2ae-150">您也可以使用 Get-AzStorageFile Cmdlet 來取得目錄。</span><span class="sxs-lookup"><span data-stu-id="be2ae-150">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="be2ae-151">檔案</span><span class="sxs-lookup"><span data-stu-id="be2ae-151">-File</span></span>
<span data-ttu-id="be2ae-152">將檔案指定為 **CloudFile** 物件。</span><span class="sxs-lookup"><span data-stu-id="be2ae-152">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="be2ae-153">這個 Cmdlet 會取得此參數指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="be2ae-153">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="be2ae-154">若要取得 **CloudFile** 物件，請使用 Get-AzStorageFile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="be2ae-154">To obtain a **CloudFile** object, use the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases: CloudFile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be2ae-155">-Force</span><span class="sxs-lookup"><span data-stu-id="be2ae-155">-Force</span></span>
<span data-ttu-id="be2ae-156">如果您指定不存在之檔案的路徑，此 Cmdlet 會建立該檔案，並將內容儲存到新檔案中。</span><span class="sxs-lookup"><span data-stu-id="be2ae-156">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="be2ae-157">如果您指定的檔案路徑已存在，而且您指定了 *Force* 參數，則 Cmdlet 會覆寫該檔案。</span><span class="sxs-lookup"><span data-stu-id="be2ae-157">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="be2ae-158">如果您指定現有檔案的路徑，而您沒有指定 *Force*，則 Cmdlet 會在繼續之前提示您。</span><span class="sxs-lookup"><span data-stu-id="be2ae-158">If you specify a path of an existing file and you do not specify *Force*, the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="be2ae-159">如果您指定資料夾的路徑，這個 Cmdlet 會嘗試建立具有 Azure 儲存空間檔案名稱的檔案。</span><span class="sxs-lookup"><span data-stu-id="be2ae-159">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="be2ae-160">-PassThru</span><span class="sxs-lookup"><span data-stu-id="be2ae-160">-PassThru</span></span>
<span data-ttu-id="be2ae-161">表示此 Cmdlet 會傳回它所下載的 **AzureStorageFile** 物件。</span><span class="sxs-lookup"><span data-stu-id="be2ae-161">Indicates that this cmdlet returns the **AzureStorageFile** object that it downloads.</span></span>

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

### <span data-ttu-id="be2ae-162">-Path</span><span class="sxs-lookup"><span data-stu-id="be2ae-162">-Path</span></span>
<span data-ttu-id="be2ae-163">指定檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="be2ae-163">Specifies the path of a file.</span></span>
<span data-ttu-id="be2ae-164">這個 Cmdlet 會取得此參數所指定之檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="be2ae-164">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="be2ae-165">如果檔案不存在，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="be2ae-165">If the file does not exist, this cmdlet returns an error.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, Share, Directory
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be2ae-166">-PreserveSMBAttribute</span><span class="sxs-lookup"><span data-stu-id="be2ae-166">-PreserveSMBAttribute</span></span>
<span data-ttu-id="be2ae-167">保留來源檔案 SMB 屬性 (檔案 Attributtes、檔案建立時間、檔案上次寫入時間) 在目的地檔案中。</span><span class="sxs-lookup"><span data-stu-id="be2ae-167">Keep the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in destination File.</span></span> <span data-ttu-id="be2ae-168">這個參數只適用于 Windows。</span><span class="sxs-lookup"><span data-stu-id="be2ae-168">This parameter is only available on Windows.</span></span>

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

### <span data-ttu-id="be2ae-169">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="be2ae-169">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="be2ae-170">指定要求的服務端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="be2ae-170">Specifies the service side time-out interval, in seconds, for a request.</span></span> <span data-ttu-id="be2ae-171">如果所指定的間隔在服務處理要求之前就已到期，儲存服務就會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="be2ae-171">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="be2ae-172">-共用</span><span class="sxs-lookup"><span data-stu-id="be2ae-172">-Share</span></span>
<span data-ttu-id="be2ae-173">指定 **CloudFileShare** 物件。</span><span class="sxs-lookup"><span data-stu-id="be2ae-173">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="be2ae-174">這個 Cmdlet 會下載此參數指定的共用中檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="be2ae-174">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="be2ae-175">若要取得 **CloudFileShare** 物件，請使用 Get-AzStorageShare Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="be2ae-175">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="be2ae-176">此物件包含儲存內容。</span><span class="sxs-lookup"><span data-stu-id="be2ae-176">This object contains the storage context.</span></span>
<span data-ttu-id="be2ae-177">如果您指定此參數，請勿指定 *CoNtext* 參數。</span><span class="sxs-lookup"><span data-stu-id="be2ae-177">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="be2ae-178">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="be2ae-178">-ShareName</span></span>
<span data-ttu-id="be2ae-179">指定檔案共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="be2ae-179">Specifies the name of the file share.</span></span>
<span data-ttu-id="be2ae-180">這個 Cmdlet 會下載此參數指定的共用中檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="be2ae-180">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="be2ae-181">-確認</span><span class="sxs-lookup"><span data-stu-id="be2ae-181">-Confirm</span></span>
<span data-ttu-id="be2ae-182">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="be2ae-182">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be2ae-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be2ae-183">-WhatIf</span></span>
<span data-ttu-id="be2ae-184">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="be2ae-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be2ae-185">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="be2ae-185">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be2ae-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be2ae-186">CommonParameters</span></span>
<span data-ttu-id="be2ae-187">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="be2ae-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be2ae-188">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="be2ae-188">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be2ae-189">輸入</span><span class="sxs-lookup"><span data-stu-id="be2ae-189">INPUTS</span></span>

### <span data-ttu-id="be2ae-190">CloudFileShare （即 Azure）</span><span class="sxs-lookup"><span data-stu-id="be2ae-190">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="be2ae-191">CloudFileDirectory （即 Azure）</span><span class="sxs-lookup"><span data-stu-id="be2ae-191">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="be2ae-192">CloudFile （即 Azure）</span><span class="sxs-lookup"><span data-stu-id="be2ae-192">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="be2ae-193">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="be2ae-193">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="be2ae-194">輸出</span><span class="sxs-lookup"><span data-stu-id="be2ae-194">OUTPUTS</span></span>

### <span data-ttu-id="be2ae-195">AzureStorageFile WindowsAzure. ResourceModel。</span><span class="sxs-lookup"><span data-stu-id="be2ae-195">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="be2ae-196">筆記</span><span class="sxs-lookup"><span data-stu-id="be2ae-196">NOTES</span></span>

## <span data-ttu-id="be2ae-197">相關連結</span><span class="sxs-lookup"><span data-stu-id="be2ae-197">RELATED LINKS</span></span>

[<span data-ttu-id="be2ae-198">AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="be2ae-198">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="be2ae-199">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="be2ae-199">Set-AzStorageFileContent</span></span>](./Set-AzStorageFileContent.md)


