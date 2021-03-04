---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
ms.openlocfilehash: 33fcfabb50b0b4af73fe7111c587ac88e746598e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909301"
---
# <span data-ttu-id="0c97b-101">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="0c97b-101">Get-AzStorageFileContent</span></span>

## <span data-ttu-id="0c97b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0c97b-102">SYNOPSIS</span></span>
<span data-ttu-id="0c97b-103">下載檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="0c97b-103">Downloads the contents of a file.</span></span>

## <span data-ttu-id="0c97b-104">語法</span><span class="sxs-lookup"><span data-stu-id="0c97b-104">SYNTAX</span></span>

### <span data-ttu-id="0c97b-105">ShareName (預設) </span><span class="sxs-lookup"><span data-stu-id="0c97b-105">ShareName (Default)</span></span>
```
Get-AzStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="0c97b-106">共用</span><span class="sxs-lookup"><span data-stu-id="0c97b-106">Share</span></span>
```
Get-AzStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="0c97b-107">目錄</span><span class="sxs-lookup"><span data-stu-id="0c97b-107">Directory</span></span>
```
Get-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="0c97b-108">檔</span><span class="sxs-lookup"><span data-stu-id="0c97b-108">File</span></span>
```
Get-AzStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

## <span data-ttu-id="0c97b-109">描述</span><span class="sxs-lookup"><span data-stu-id="0c97b-109">DESCRIPTION</span></span>
<span data-ttu-id="0c97b-110">**Get-AzStorageFileContent** Cmdlet 會下載檔案的內容，然後將它存到您指定的目的地。</span><span class="sxs-lookup"><span data-stu-id="0c97b-110">The **Get-AzStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="0c97b-111">此 Cmdlet 不會返回檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="0c97b-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="0c97b-112">例子</span><span class="sxs-lookup"><span data-stu-id="0c97b-112">EXAMPLES</span></span>

### <span data-ttu-id="0c97b-113">範例 1：從資料夾下載檔案</span><span class="sxs-lookup"><span data-stu-id="0c97b-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="0c97b-114">此命令會從檔案共用 ContosoShare06 的資料夾 ContosoWorkingFolder 下載名為 CurrentDataFile 的檔案至目前的資料夾。</span><span class="sxs-lookup"><span data-stu-id="0c97b-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

### <span data-ttu-id="0c97b-115">範例 2：下載範例檔案共用下的檔案</span><span class="sxs-lookup"><span data-stu-id="0c97b-115">Example 2: Downloads the files under sample file share</span></span>
```
PS C:\>Get-AzStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzStorageFileContent
```

<span data-ttu-id="0c97b-116">此範例會下載範例檔案共用下的檔案</span><span class="sxs-lookup"><span data-stu-id="0c97b-116">This example downloads the files under sample file share</span></span>

### <span data-ttu-id="0c97b-117">範例 3：將 Azure 檔案下載到本地檔案，並保留本地檔案中的 Azure 檔案 SMB 屬性 (File 一文、檔案建立時間、檔案上次寫入時間) 。</span><span class="sxs-lookup"><span data-stu-id="0c97b-117">Example 3: Download an Azure file to a local file, and perserve the Azure File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the local file.</span></span>
```
PS C:\>Get-AzStorageFileContent -ShareName sample -Path "dir1/file1" -Destination $localFilePath -PreserveSMBAttribute
```

<span data-ttu-id="0c97b-118">此範例會下載 Azure 檔案至本地檔案，並保留本地檔案中的 Azure 檔案 SMB 屬性 (檔案問題、檔案建立時間、檔案上次寫入時間) 。</span><span class="sxs-lookup"><span data-stu-id="0c97b-118">This example downloads an Azure file to a local file, and perserves the Azure File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the local file.</span></span>

## <span data-ttu-id="0c97b-119">參數</span><span class="sxs-lookup"><span data-stu-id="0c97b-119">PARAMETERS</span></span>

### <span data-ttu-id="0c97b-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0c97b-120">-AsJob</span></span>
<span data-ttu-id="0c97b-121">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0c97b-121">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="0c97b-122">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="0c97b-122">-CheckMd5</span></span>
<span data-ttu-id="0c97b-123">指定是否要針對下載的檔案檢查 Md5 加總。</span><span class="sxs-lookup"><span data-stu-id="0c97b-123">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="0c97b-124">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0c97b-124">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="0c97b-125">指定一個服務要求用戶端的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="0c97b-125">Specifies the client-side time-out interval, in seconds, for one service request.</span></span> <span data-ttu-id="0c97b-126">如果前一個通話在指定的時間間隔內失敗，此 Cmdlet 會重新重試要求。</span><span class="sxs-lookup"><span data-stu-id="0c97b-126">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span> <span data-ttu-id="0c97b-127">如果此 Cmdlet 在間隔經過之前未收到成功回應，此 Cmdlet 會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="0c97b-127">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="0c97b-128">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="0c97b-128">-ConcurrentTaskCount</span></span>
<span data-ttu-id="0c97b-129">指定同時進行的最大網路通話數。</span><span class="sxs-lookup"><span data-stu-id="0c97b-129">Specifies the maximum concurrent network calls.</span></span> <span data-ttu-id="0c97b-130">您可以使用此參數來限制並行，以節流本地 CPU 和頻寬使用量，方法為指定並行網路通話的數量上限。</span><span class="sxs-lookup"><span data-stu-id="0c97b-130">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span> <span data-ttu-id="0c97b-131">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="0c97b-131">The specified value is an absolute count and is not multiplied by the core count.</span></span> <span data-ttu-id="0c97b-132">此參數有助於減少低頻寬環境的網路連接問題，例如每秒 100 KB。</span><span class="sxs-lookup"><span data-stu-id="0c97b-132">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span> <span data-ttu-id="0c97b-133">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="0c97b-133">The default value is 10.</span></span>

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

### <span data-ttu-id="0c97b-134">-內容</span><span class="sxs-lookup"><span data-stu-id="0c97b-134">-Context</span></span>
<span data-ttu-id="0c97b-135">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="0c97b-135">Specifies an Azure Storage context.</span></span> <span data-ttu-id="0c97b-136">若要取得內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0c97b-136">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="0c97b-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c97b-137">-DefaultProfile</span></span>
<span data-ttu-id="0c97b-138">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0c97b-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c97b-139">-目的地</span><span class="sxs-lookup"><span data-stu-id="0c97b-139">-Destination</span></span>
<span data-ttu-id="0c97b-140">指定目的地路徑。</span><span class="sxs-lookup"><span data-stu-id="0c97b-140">Specifies the destination path.</span></span>
<span data-ttu-id="0c97b-141">此 Cmdlet 會下載檔案內容至此參數指定的位置。</span><span class="sxs-lookup"><span data-stu-id="0c97b-141">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>
<span data-ttu-id="0c97b-142">如果您指定不存在之檔案的路徑，此 Cmdlet 會建立該檔案，並會將內容存到新檔案中。</span><span class="sxs-lookup"><span data-stu-id="0c97b-142">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="0c97b-143">如果您指定已存在之檔案的路徑，並指定 *Force* 參數，Cmdlet 會覆寫檔案。</span><span class="sxs-lookup"><span data-stu-id="0c97b-143">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="0c97b-144">如果您指定現有檔案的路徑，但未指定 Force，Cmdlet會先提示您再繼續。</span><span class="sxs-lookup"><span data-stu-id="0c97b-144">If you specify a path of an existing file and you do not specify *Force*, the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="0c97b-145">如果您指定資料夾的路徑，此 Cmdlet 會嘗試建立具有 Azure 儲存檔案名的檔案。</span><span class="sxs-lookup"><span data-stu-id="0c97b-145">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="0c97b-146">-目錄</span><span class="sxs-lookup"><span data-stu-id="0c97b-146">-Directory</span></span>
<span data-ttu-id="0c97b-147">將資料夾指定為 **CloudFileDirectory** 物件。</span><span class="sxs-lookup"><span data-stu-id="0c97b-147">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="0c97b-148">此 Cmdlet 會在此參數指定的資料夾中，獲得檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="0c97b-148">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="0c97b-149">若要取得目錄，請使用 New-AzStorageDirectory Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0c97b-149">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="0c97b-150">您也可以使用 Get-AzStorageFile取得目錄。</span><span class="sxs-lookup"><span data-stu-id="0c97b-150">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="0c97b-151">-檔案</span><span class="sxs-lookup"><span data-stu-id="0c97b-151">-File</span></span>
<span data-ttu-id="0c97b-152">將檔案指定為 **CloudFile** 物件。</span><span class="sxs-lookup"><span data-stu-id="0c97b-152">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="0c97b-153">此 Cmdlet 會獲得此參數指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="0c97b-153">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="0c97b-154">若要取得 **CloudFile** 物件，請使用 Get-AzStorageFile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0c97b-154">To obtain a **CloudFile** object, use the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="0c97b-155">-強制</span><span class="sxs-lookup"><span data-stu-id="0c97b-155">-Force</span></span>
<span data-ttu-id="0c97b-156">如果您指定不存在之檔案的路徑，此 Cmdlet 會建立該檔案，並會將內容存到新檔案中。</span><span class="sxs-lookup"><span data-stu-id="0c97b-156">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="0c97b-157">如果您指定已存在之檔案的路徑，並指定 *Force* 參數，Cmdlet 會覆寫檔案。</span><span class="sxs-lookup"><span data-stu-id="0c97b-157">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="0c97b-158">如果您指定現有檔案的路徑，但未指定 Force，Cmdlet會先提示您再繼續。</span><span class="sxs-lookup"><span data-stu-id="0c97b-158">If you specify a path of an existing file and you do not specify *Force*, the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="0c97b-159">如果您指定資料夾的路徑，此 Cmdlet 會嘗試建立具有 Azure 儲存檔案名的檔案。</span><span class="sxs-lookup"><span data-stu-id="0c97b-159">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="0c97b-160">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0c97b-160">-PassThru</span></span>
<span data-ttu-id="0c97b-161">表示此 Cmdlet 會返回 **它下載的 AzureStorageFile** 物件。</span><span class="sxs-lookup"><span data-stu-id="0c97b-161">Indicates that this cmdlet returns the **AzureStorageFile** object that it downloads.</span></span>

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

### <span data-ttu-id="0c97b-162">-路徑</span><span class="sxs-lookup"><span data-stu-id="0c97b-162">-Path</span></span>
<span data-ttu-id="0c97b-163">指定檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="0c97b-163">Specifies the path of a file.</span></span>
<span data-ttu-id="0c97b-164">此 Cmdlet 會獲得此參數指定的檔案內容。</span><span class="sxs-lookup"><span data-stu-id="0c97b-164">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="0c97b-165">如果檔案不存在，此 Cmdlet 會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="0c97b-165">If the file does not exist, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="0c97b-166">-PreserveSMBAttribute</span><span class="sxs-lookup"><span data-stu-id="0c97b-166">-PreserveSMBAttribute</span></span>
<span data-ttu-id="0c97b-167">將來源檔案 SMB 屬性 (檔指定、檔案建立時間、檔案上次寫入時間) 目標檔案中。</span><span class="sxs-lookup"><span data-stu-id="0c97b-167">Keep the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in destination File.</span></span> <span data-ttu-id="0c97b-168">此參數僅適用于 Windows。</span><span class="sxs-lookup"><span data-stu-id="0c97b-168">This parameter is only available on Windows.</span></span>

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

### <span data-ttu-id="0c97b-169">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0c97b-169">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="0c97b-170">指定服務端要求的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="0c97b-170">Specifies the service side time-out interval, in seconds, for a request.</span></span> <span data-ttu-id="0c97b-171">如果指定的時間間隔在服務處理要求之前已經過，儲存服務會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="0c97b-171">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="0c97b-172">-共用</span><span class="sxs-lookup"><span data-stu-id="0c97b-172">-Share</span></span>
<span data-ttu-id="0c97b-173">指定 **CloudFileShare** 物件。</span><span class="sxs-lookup"><span data-stu-id="0c97b-173">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="0c97b-174">此 Cmdlet 會在此參數指定的共用中下載檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="0c97b-174">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="0c97b-175">若要取得 **CloudFileShare** 物件，請使用 Get-AzStorageShare Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0c97b-175">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="0c97b-176">此物件包含儲存內容。</span><span class="sxs-lookup"><span data-stu-id="0c97b-176">This object contains the storage context.</span></span>
<span data-ttu-id="0c97b-177">如果您指定此參數，請勿指定 *CoNtext* 參數。</span><span class="sxs-lookup"><span data-stu-id="0c97b-177">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="0c97b-178">-ShareName</span><span class="sxs-lookup"><span data-stu-id="0c97b-178">-ShareName</span></span>
<span data-ttu-id="0c97b-179">指定檔案共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="0c97b-179">Specifies the name of the file share.</span></span>
<span data-ttu-id="0c97b-180">此 Cmdlet 會在此參數指定的共用中下載檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="0c97b-180">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="0c97b-181">-確認</span><span class="sxs-lookup"><span data-stu-id="0c97b-181">-Confirm</span></span>
<span data-ttu-id="0c97b-182">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0c97b-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c97b-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c97b-183">-WhatIf</span></span>
<span data-ttu-id="0c97b-184">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0c97b-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c97b-185">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0c97b-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c97b-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c97b-186">CommonParameters</span></span>
<span data-ttu-id="0c97b-187">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0c97b-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c97b-188">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="0c97b-188">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c97b-189">輸入</span><span class="sxs-lookup"><span data-stu-id="0c97b-189">INPUTS</span></span>

### <span data-ttu-id="0c97b-190">Microsoft.Azure.storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="0c97b-190">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="0c97b-191">Microsoft.Azure.storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="0c97b-191">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="0c97b-192">Microsoft.Azure.storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="0c97b-192">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="0c97b-193">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="0c97b-193">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0c97b-194">輸出</span><span class="sxs-lookup"><span data-stu-id="0c97b-194">OUTPUTS</span></span>

### <span data-ttu-id="0c97b-195">Microsoft.WindowsAzure.Commands.Common.storage.ResourceModel.AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="0c97b-195">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="0c97b-196">筆記</span><span class="sxs-lookup"><span data-stu-id="0c97b-196">NOTES</span></span>

## <span data-ttu-id="0c97b-197">相關連結</span><span class="sxs-lookup"><span data-stu-id="0c97b-197">RELATED LINKS</span></span>

[<span data-ttu-id="0c97b-198">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="0c97b-198">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="0c97b-199">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="0c97b-199">Set-AzStorageFileContent</span></span>](./Set-AzStorageFileContent.md)


