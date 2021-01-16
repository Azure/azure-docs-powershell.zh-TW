---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FA98E64B-D589-4653-9ACC-86573FAF4550
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageFileContent.md
ms.openlocfilehash: 3fed30a260532378274e2df815d6e4b252c018f6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98286052"
---
# <span data-ttu-id="9620d-101">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="9620d-101">Set-AzStorageFileContent</span></span>

## <span data-ttu-id="9620d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9620d-102">SYNOPSIS</span></span>
<span data-ttu-id="9620d-103">上傳檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="9620d-103">Uploads the contents of a file.</span></span>

## <span data-ttu-id="9620d-104">句法</span><span class="sxs-lookup"><span data-stu-id="9620d-104">SYNTAX</span></span>

### <span data-ttu-id="9620d-105">共用名稱 (預設) </span><span class="sxs-lookup"><span data-stu-id="9620d-105">ShareName (Default)</span></span>
```
Set-AzStorageFileContent [-ShareName] <String> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="9620d-106">共用</span><span class="sxs-lookup"><span data-stu-id="9620d-106">Share</span></span>
```
Set-AzStorageFileContent [-Share] <CloudFileShare> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="9620d-107">空目錄</span><span class="sxs-lookup"><span data-stu-id="9620d-107">Directory</span></span>
```
Set-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

## <span data-ttu-id="9620d-108">說明</span><span class="sxs-lookup"><span data-stu-id="9620d-108">DESCRIPTION</span></span>
<span data-ttu-id="9620d-109">**AzStorageFileContent** Cmdlet 會將檔案的內容上傳到指定共用上的檔案。</span><span class="sxs-lookup"><span data-stu-id="9620d-109">The **Set-AzStorageFileContent** cmdlet uploads the contents of a file to a file on a specified share.</span></span>

## <span data-ttu-id="9620d-110">示例</span><span class="sxs-lookup"><span data-stu-id="9620d-110">EXAMPLES</span></span>

### <span data-ttu-id="9620d-111">範例1：上傳目前資料夾中的檔案</span><span class="sxs-lookup"><span data-stu-id="9620d-111">Example 1: Upload a file in the current folder</span></span>
```
PS C:\>Set-AzStorageFileContent -ShareName "ContosoShare06" -Source "DataFile37" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="9620d-112">這個命令會將目前資料夾中的名為 DataFile37 的檔案，上傳為名為 CurrentDataFile 的檔案，該檔案名為 [ContosoWorkingFolder] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="9620d-112">This command uploads a file that is named DataFile37 in the current folder as a file that is named CurrentDataFile in the folder named ContosoWorkingFolder.</span></span>

### <span data-ttu-id="9620d-113">範例2：上傳目前資料夾中的所有檔案</span><span class="sxs-lookup"><span data-stu-id="9620d-113">Example 2: Upload all the files in the current folder</span></span>
```
PS C:\>$CurrentFolder = (Get-Item .).FullName
PS C:\> $Container = Get-AzStorageShare -Name "ContosoShare06"
PS C:\> Get-ChildItem -Recurse | Where-Object { $_.GetType().Name -eq "FileInfo"} | ForEach-Object {
    $path=$_.FullName.Substring($Currentfolder.Length+1).Replace("\","/")
    Set-AzStorageFileContent -Share $Container -Source $_.FullName -Path $path -Force
}
```

<span data-ttu-id="9620d-114">這個範例使用幾個常見的 Windows PowerShell Cmdlet 和目前的 Cmdlet，將目前資料夾中的所有檔案上傳到容器 ContosoShare06 的根資料夾。</span><span class="sxs-lookup"><span data-stu-id="9620d-114">This example uses several common Windows PowerShell cmdlets and the current cmdlet to upload all files from the current folder to the root folder of container ContosoShare06.</span></span>
<span data-ttu-id="9620d-115">第一個命令會取得目前資料夾的名稱，並將它儲存在 $CurrentFolder 變數中。</span><span class="sxs-lookup"><span data-stu-id="9620d-115">The first command gets the name of the current folder and stores it in the $CurrentFolder variable.</span></span>
<span data-ttu-id="9620d-116">第二個命令使用 **AzStorageShare** Cmdlet 來取得名為 ContosoShare06 的檔案共用，然後將它儲存在 $Container 變數中。</span><span class="sxs-lookup"><span data-stu-id="9620d-116">The second command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="9620d-117">最後一個命令會透過使用管線運算子來取得目前資料夾的內容，並將每個專案傳遞給 Where-Object Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9620d-117">The final command gets the contents of the current folder and passes each one to the Where-Object cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9620d-118">該 Cmdlet 會篩選掉不是檔案的物件，然後將檔案傳遞到 ForEach-Object Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9620d-118">That cmdlet filters out objects that are not files, and then passes the files to the ForEach-Object cmdlet.</span></span>
<span data-ttu-id="9620d-119">該 Cmdlet 會針對針對其建立適當路徑的每個檔案執行腳本區塊，然後使用目前的 Cmdlet 來上傳檔案。</span><span class="sxs-lookup"><span data-stu-id="9620d-119">That cmdlet runs a script block for each file that creates the appropriate path for it and then uses the current cmdlet to upload the file.</span></span>
<span data-ttu-id="9620d-120">結果的名稱與此範例上傳之其他檔案的相對位置相同。</span><span class="sxs-lookup"><span data-stu-id="9620d-120">The result has the same name and same relative position with regard to the other files that this example uploads.</span></span>
<span data-ttu-id="9620d-121">如需腳本區塊的詳細資訊，請輸入 `Get-Help about_Script_Blocks` 。</span><span class="sxs-lookup"><span data-stu-id="9620d-121">For more information about script blocks, type `Get-Help about_Script_Blocks`.</span></span>

### <span data-ttu-id="9620d-122">範例3：將本機檔案上傳到 Azure 檔案，並 perserve 本機檔案 SMB 屬性 (檔案 Attributtes、檔案建立時間、檔案上次寫入時間) 在 Azure 檔案中。</span><span class="sxs-lookup"><span data-stu-id="9620d-122">Example 3: Upload a local file to an Azure file, and perserve the local File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the Azure file.</span></span>
```
PS C:\>Get-AzStorageFileContent -source $localFilePath -ShareName sample -Path "dir1/file1" -PreserveSMBAttribute
```

<span data-ttu-id="9620d-123">這個範例會將本機檔案上傳到 Azure 檔案，並 perserves 本機檔案 SMB 屬性 (檔案 Attributtes、檔案建立時間、檔案上次寫入時間) 在 Azure 檔案中。</span><span class="sxs-lookup"><span data-stu-id="9620d-123">This example uploads a local file to an Azure file, and perserves the local File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the Azure file.</span></span>

## <span data-ttu-id="9620d-124">參數</span><span class="sxs-lookup"><span data-stu-id="9620d-124">PARAMETERS</span></span>

### <span data-ttu-id="9620d-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9620d-125">-AsJob</span></span>
<span data-ttu-id="9620d-126">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9620d-126">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="9620d-127">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9620d-127">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="9620d-128">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="9620d-128">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="9620d-129">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="9620d-129">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="9620d-130">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="9620d-130">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="9620d-131">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="9620d-131">-ConcurrentTaskCount</span></span>
<span data-ttu-id="9620d-132">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="9620d-132">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="9620d-133">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="9620d-133">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="9620d-134">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="9620d-134">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="9620d-135">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="9620d-135">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="9620d-136">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="9620d-136">The default value is 10.</span></span>

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

### <span data-ttu-id="9620d-137">-內容</span><span class="sxs-lookup"><span data-stu-id="9620d-137">-Context</span></span>
<span data-ttu-id="9620d-138">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="9620d-138">Specifies an Azure storage context.</span></span>
<span data-ttu-id="9620d-139">若要取得儲存內容，請使用 [AzStorageCoNtext](./New-AzStorageContext.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9620d-139">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="9620d-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9620d-140">-DefaultProfile</span></span>
<span data-ttu-id="9620d-141">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9620d-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9620d-142">-Directory</span><span class="sxs-lookup"><span data-stu-id="9620d-142">-Directory</span></span>
<span data-ttu-id="9620d-143">將資料夾指定為 **CloudFileDirectory** 物件。</span><span class="sxs-lookup"><span data-stu-id="9620d-143">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="9620d-144">這個 Cmdlet 會將檔案上傳到此參數指定的資料夾中。</span><span class="sxs-lookup"><span data-stu-id="9620d-144">This cmdlet uploads the file to the folder that this parameter specifies.</span></span>
<span data-ttu-id="9620d-145">若要取得目錄，請使用 New-AzStorageDirectory Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9620d-145">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="9620d-146">您也可以使用 Get-AzStorageFile Cmdlet 來取得目錄。</span><span class="sxs-lookup"><span data-stu-id="9620d-146">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="9620d-147">-Force</span><span class="sxs-lookup"><span data-stu-id="9620d-147">-Force</span></span>
<span data-ttu-id="9620d-148">表示此 Cmdlet 會覆寫現有的 Azure 儲存空間檔案。</span><span class="sxs-lookup"><span data-stu-id="9620d-148">Indicates that this cmdlet overwrites an existing Azure storage file.</span></span>

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

### <span data-ttu-id="9620d-149">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9620d-149">-PassThru</span></span>
<span data-ttu-id="9620d-150">表示此 Cmdlet 會傳回它所建立或上傳的 **AzureStorageFile** 物件。</span><span class="sxs-lookup"><span data-stu-id="9620d-150">Indicates that this cmdlet returns the **AzureStorageFile** object that it creates or uploads.</span></span>

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

### <span data-ttu-id="9620d-151">-Path</span><span class="sxs-lookup"><span data-stu-id="9620d-151">-Path</span></span>
<span data-ttu-id="9620d-152">指定檔案或資料夾的路徑。</span><span class="sxs-lookup"><span data-stu-id="9620d-152">Specifies the path of a file or folder.</span></span>
<span data-ttu-id="9620d-153">這個 Cmdlet 會將內容上傳到此參數指定的檔案，或傳給此參數指定之資料夾中的檔案。</span><span class="sxs-lookup"><span data-stu-id="9620d-153">This cmdlet uploads contents to the file that this parameter specifies, or to a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="9620d-154">如果您指定資料夾，這個 Cmdlet 會建立與來源檔案同名的檔案。</span><span class="sxs-lookup"><span data-stu-id="9620d-154">If you specify a folder, this cmdlet creates a file that has the same name as the source file.</span></span>
<span data-ttu-id="9620d-155">如果您指定不存在之檔案的路徑，這個 Cmdlet 會建立該檔案，並將內容儲存到該檔案。</span><span class="sxs-lookup"><span data-stu-id="9620d-155">If you specify a path of a file that does not exist, this cmdlet creates that file and saves the contents to that file.</span></span>
<span data-ttu-id="9620d-156">如果您指定的檔案已經存在，而且您指定了 _Force_ 參數，這個 Cmdlet 會覆寫檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="9620d-156">If you specify a file that already exists, and you specify the _Force_ parameter, this cmdlet overwrites the contents of the file.</span></span>
<span data-ttu-id="9620d-157">如果您指定的檔案已經存在，而您沒有指定 _Force_，這個 Cmdlet 不會變更，而且會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="9620d-157">If you specify a file that already exists and you do not specify _Force_, this cmdlet makes no change, and returns an error.</span></span>
<span data-ttu-id="9620d-158">如果您指定的資料夾路徑不存在，這個 Cmdlet 不會變更，而且會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="9620d-158">If you specify a path of a folder that does not exist, this cmdlet makes no change, and returns an error.</span></span>

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

### <span data-ttu-id="9620d-159">-PreserveSMBAttribute</span><span class="sxs-lookup"><span data-stu-id="9620d-159">-PreserveSMBAttribute</span></span>
<span data-ttu-id="9620d-160">保留來源檔案 SMB 屬性 (檔案 Attributtes、檔案建立時間、檔案上次寫入時間) 在目的地檔案中。</span><span class="sxs-lookup"><span data-stu-id="9620d-160">Keep the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in destination File.</span></span> <span data-ttu-id="9620d-161">這個參數只適用于 Windows。</span><span class="sxs-lookup"><span data-stu-id="9620d-161">This parameter is only available on Windows.</span></span>

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

### <span data-ttu-id="9620d-162">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9620d-162">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="9620d-163">指定要求中伺服器部分的超時時間長度。</span><span class="sxs-lookup"><span data-stu-id="9620d-163">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="9620d-164">-共用</span><span class="sxs-lookup"><span data-stu-id="9620d-164">-Share</span></span>
<span data-ttu-id="9620d-165">指定 **CloudFileShare** 物件。</span><span class="sxs-lookup"><span data-stu-id="9620d-165">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="9620d-166">這個 Cmdlet 會在檔案共用此參數指定的檔案上傳到檔案。</span><span class="sxs-lookup"><span data-stu-id="9620d-166">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>
<span data-ttu-id="9620d-167">若要取得 **CloudFileShare** 物件，請使用 Get-AzStorageShare Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9620d-167">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="9620d-168">此物件包含儲存內容。</span><span class="sxs-lookup"><span data-stu-id="9620d-168">This object contains the storage context.</span></span>
<span data-ttu-id="9620d-169">如果您指定此參數，請勿指定 *CoNtext* 參數。</span><span class="sxs-lookup"><span data-stu-id="9620d-169">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="9620d-170">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="9620d-170">-ShareName</span></span>
<span data-ttu-id="9620d-171">指定檔案共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="9620d-171">Specifies the name of the file share.</span></span>
<span data-ttu-id="9620d-172">這個 Cmdlet 會在檔案共用此參數指定的檔案上傳到檔案。</span><span class="sxs-lookup"><span data-stu-id="9620d-172">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>

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

### <span data-ttu-id="9620d-173">-來源</span><span class="sxs-lookup"><span data-stu-id="9620d-173">-Source</span></span>
<span data-ttu-id="9620d-174">指定此 Cmdlet 上傳的來源檔案。</span><span class="sxs-lookup"><span data-stu-id="9620d-174">Specifies the source file that this cmdlet uploads.</span></span>
<span data-ttu-id="9620d-175">如果您指定的檔案不存在，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="9620d-175">If you specify a file that does not exist, this cmdlet returns an error.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FullName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9620d-176">-確認</span><span class="sxs-lookup"><span data-stu-id="9620d-176">-Confirm</span></span>
<span data-ttu-id="9620d-177">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9620d-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9620d-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9620d-178">-WhatIf</span></span>
<span data-ttu-id="9620d-179">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9620d-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9620d-180">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9620d-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9620d-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9620d-181">CommonParameters</span></span>
<span data-ttu-id="9620d-182">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9620d-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9620d-183">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9620d-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9620d-184">輸入</span><span class="sxs-lookup"><span data-stu-id="9620d-184">INPUTS</span></span>

### <span data-ttu-id="9620d-185">CloudFileShare （即 Azure）</span><span class="sxs-lookup"><span data-stu-id="9620d-185">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="9620d-186">CloudFileDirectory （即 Azure）</span><span class="sxs-lookup"><span data-stu-id="9620d-186">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="9620d-187">System.object</span><span class="sxs-lookup"><span data-stu-id="9620d-187">System.String</span></span>

### <span data-ttu-id="9620d-188">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="9620d-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9620d-189">輸出</span><span class="sxs-lookup"><span data-stu-id="9620d-189">OUTPUTS</span></span>

### <span data-ttu-id="9620d-190">AzureStorageFile WindowsAzure. ResourceModel。</span><span class="sxs-lookup"><span data-stu-id="9620d-190">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="9620d-191">筆記</span><span class="sxs-lookup"><span data-stu-id="9620d-191">NOTES</span></span>

## <span data-ttu-id="9620d-192">相關連結</span><span class="sxs-lookup"><span data-stu-id="9620d-192">RELATED LINKS</span></span>

[<span data-ttu-id="9620d-193">移除-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="9620d-193">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)

[<span data-ttu-id="9620d-194">新-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="9620d-194">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="9620d-195">AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="9620d-195">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)
