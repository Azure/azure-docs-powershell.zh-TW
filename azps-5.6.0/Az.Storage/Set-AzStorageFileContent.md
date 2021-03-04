---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FA98E64B-D589-4653-9ACC-86573FAF4550
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageFileContent.md
ms.openlocfilehash: 597728b1b327da28495574ca865a2e75a1a774a3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907462"
---
# <span data-ttu-id="c6592-101">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="c6592-101">Set-AzStorageFileContent</span></span>

## <span data-ttu-id="c6592-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c6592-102">SYNOPSIS</span></span>
<span data-ttu-id="c6592-103">上傳檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="c6592-103">Uploads the contents of a file.</span></span>

## <span data-ttu-id="c6592-104">語法</span><span class="sxs-lookup"><span data-stu-id="c6592-104">SYNTAX</span></span>

### <span data-ttu-id="c6592-105">ShareName (預設) </span><span class="sxs-lookup"><span data-stu-id="c6592-105">ShareName (Default)</span></span>
```
Set-AzStorageFileContent [-ShareName] <String> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="c6592-106">共用</span><span class="sxs-lookup"><span data-stu-id="c6592-106">Share</span></span>
```
Set-AzStorageFileContent [-Share] <CloudFileShare> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="c6592-107">目錄</span><span class="sxs-lookup"><span data-stu-id="c6592-107">Directory</span></span>
```
Set-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

## <span data-ttu-id="c6592-108">描述</span><span class="sxs-lookup"><span data-stu-id="c6592-108">DESCRIPTION</span></span>
<span data-ttu-id="c6592-109">**Set-AzStorageFileContent** Cmdlet 會上傳檔案的內容至指定共用上的檔案。</span><span class="sxs-lookup"><span data-stu-id="c6592-109">The **Set-AzStorageFileContent** cmdlet uploads the contents of a file to a file on a specified share.</span></span>

## <span data-ttu-id="c6592-110">例子</span><span class="sxs-lookup"><span data-stu-id="c6592-110">EXAMPLES</span></span>

### <span data-ttu-id="c6592-111">範例 1：上傳目前資料夾中的檔案</span><span class="sxs-lookup"><span data-stu-id="c6592-111">Example 1: Upload a file in the current folder</span></span>
```
PS C:\>Set-AzStorageFileContent -ShareName "ContosoShare06" -Source "DataFile37" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="c6592-112">此命令會上傳目前資料夾中名為 DataFile37 的檔案，作為名為 ContosoWorkingFolder 資料夾中 CurrentDataFile 的檔案。</span><span class="sxs-lookup"><span data-stu-id="c6592-112">This command uploads a file that is named DataFile37 in the current folder as a file that is named CurrentDataFile in the folder named ContosoWorkingFolder.</span></span>

### <span data-ttu-id="c6592-113">範例 2：上傳目前資料夾中的所有檔案</span><span class="sxs-lookup"><span data-stu-id="c6592-113">Example 2: Upload all the files in the current folder</span></span>
```
PS C:\>$CurrentFolder = (Get-Item .).FullName
PS C:\> $Container = Get-AzStorageShare -Name "ContosoShare06"
PS C:\> Get-ChildItem -Recurse | Where-Object { $_.GetType().Name -eq "FileInfo"} | ForEach-Object {
    $path=$_.FullName.Substring($Currentfolder.Length+1).Replace("\","/")
    Set-AzStorageFileContent -Share $Container -Source $_.FullName -Path $path -Force
}
```

<span data-ttu-id="c6592-114">此範例使用數種常見的 Windows PowerShell Cmdlet 和目前的 Cmdlet，將目前資料夾中的所有檔案上傳到容器 ContosoShare06 的根資料夾。</span><span class="sxs-lookup"><span data-stu-id="c6592-114">This example uses several common Windows PowerShell cmdlets and the current cmdlet to upload all files from the current folder to the root folder of container ContosoShare06.</span></span>
<span data-ttu-id="c6592-115">第一個命令會獲得目前資料夾的名稱，並儲存在$CurrentFolder變數。</span><span class="sxs-lookup"><span data-stu-id="c6592-115">The first command gets the name of the current folder and stores it in the $CurrentFolder variable.</span></span>
<span data-ttu-id="c6592-116">第二個命令使用 **Get-AzStorageShare** Cmdlet 取得名為 ContosoShare06 的檔案共用，然後將它儲存在$Container變數中。</span><span class="sxs-lookup"><span data-stu-id="c6592-116">The second command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="c6592-117">最後一個命令會獲得目前資料夾的內容，然後使用管線運算子將每個資料夾Where-Object Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c6592-117">The final command gets the contents of the current folder and passes each one to the Where-Object cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c6592-118">該 Cmdlet 會篩選出非檔案的物件，然後將檔案傳遞至 ForEach-Object Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c6592-118">That cmdlet filters out objects that are not files, and then passes the files to the ForEach-Object cmdlet.</span></span>
<span data-ttu-id="c6592-119">該 Cmdlet 會針對每個建立適當路徑的檔案執行腳本區塊，然後使用目前的 Cmdlet 上傳檔案。</span><span class="sxs-lookup"><span data-stu-id="c6592-119">That cmdlet runs a script block for each file that creates the appropriate path for it and then uses the current cmdlet to upload the file.</span></span>
<span data-ttu-id="c6592-120">針對此範例上傳的其他檔案，結果的名稱和相對位置相同。</span><span class="sxs-lookup"><span data-stu-id="c6592-120">The result has the same name and same relative position with regard to the other files that this example uploads.</span></span>
<span data-ttu-id="c6592-121">有關腳本區塊的資訊，請鍵入 `Get-Help about_Script_Blocks` 。</span><span class="sxs-lookup"><span data-stu-id="c6592-121">For more information about script blocks, type `Get-Help about_Script_Blocks`.</span></span>

### <span data-ttu-id="c6592-122">範例 3：將本地檔案上傳至 Azure 檔案，並保留 Azure 檔案中的本地檔案 SMB 屬性 (File 一文、檔案建立時間、檔案上次寫入時間) 。</span><span class="sxs-lookup"><span data-stu-id="c6592-122">Example 3: Upload a local file to an Azure file, and perserve the local File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the Azure file.</span></span>
```
PS C:\>Get-AzStorageFileContent -source $localFilePath -ShareName sample -Path "dir1/file1" -PreserveSMBAttribute
```

<span data-ttu-id="c6592-123">此範例會上傳本地檔案至 Azure 檔案，並保留 Azure 檔案中的本地檔案 SMB 屬性 (檔案問題、檔案建立時間、檔案上次寫入時間) 。</span><span class="sxs-lookup"><span data-stu-id="c6592-123">This example uploads a local file to an Azure file, and perserves the local File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the Azure file.</span></span>

## <span data-ttu-id="c6592-124">參數</span><span class="sxs-lookup"><span data-stu-id="c6592-124">PARAMETERS</span></span>

### <span data-ttu-id="c6592-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c6592-125">-AsJob</span></span>
<span data-ttu-id="c6592-126">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c6592-126">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="c6592-127">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c6592-127">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c6592-128">指定一個服務要求用戶端的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="c6592-128">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c6592-129">如果前一個通話在指定的時間間隔內失敗，此 Cmdlet 會重新重試要求。</span><span class="sxs-lookup"><span data-stu-id="c6592-129">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c6592-130">如果此 Cmdlet 在間隔經過之前未收到成功回應，此 Cmdlet 會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="c6592-130">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c6592-131">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c6592-131">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c6592-132">指定同時進行的最大網路通話數。</span><span class="sxs-lookup"><span data-stu-id="c6592-132">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="c6592-133">您可以使用此參數來限制並行，以節流本地 CPU 和頻寬使用量，方法為指定並行網路通話的數量上限。</span><span class="sxs-lookup"><span data-stu-id="c6592-133">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="c6592-134">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="c6592-134">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="c6592-135">此參數有助於減少低頻寬環境的網路連接問題，例如每秒 100 KB。</span><span class="sxs-lookup"><span data-stu-id="c6592-135">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="c6592-136">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="c6592-136">The default value is 10.</span></span>

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

### <span data-ttu-id="c6592-137">-內容</span><span class="sxs-lookup"><span data-stu-id="c6592-137">-Context</span></span>
<span data-ttu-id="c6592-138">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="c6592-138">Specifies an Azure storage context.</span></span>
<span data-ttu-id="c6592-139">若要取得儲存內容，請使用 [New-AzStorageCoNtext](./New-AzStorageContext.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c6592-139">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="c6592-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6592-140">-DefaultProfile</span></span>
<span data-ttu-id="c6592-141">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c6592-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6592-142">-目錄</span><span class="sxs-lookup"><span data-stu-id="c6592-142">-Directory</span></span>
<span data-ttu-id="c6592-143">將資料夾指定為 **CloudFileDirectory** 物件。</span><span class="sxs-lookup"><span data-stu-id="c6592-143">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="c6592-144">此 Cmdlet 會上傳檔案至此參數指定的資料夾。</span><span class="sxs-lookup"><span data-stu-id="c6592-144">This cmdlet uploads the file to the folder that this parameter specifies.</span></span>
<span data-ttu-id="c6592-145">若要取得目錄，請使用 New-AzStorageDirectory Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c6592-145">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="c6592-146">您也可以使用 Get-AzStorageFile取得目錄。</span><span class="sxs-lookup"><span data-stu-id="c6592-146">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="c6592-147">-強制</span><span class="sxs-lookup"><span data-stu-id="c6592-147">-Force</span></span>
<span data-ttu-id="c6592-148">表示此 Cmdlet 覆寫現有的 Azure 儲存檔案。</span><span class="sxs-lookup"><span data-stu-id="c6592-148">Indicates that this cmdlet overwrites an existing Azure storage file.</span></span>

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

### <span data-ttu-id="c6592-149">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c6592-149">-PassThru</span></span>
<span data-ttu-id="c6592-150">表示此 Cmdlet 會返回它建立或上傳的 **AzureStorageFile** 物件。</span><span class="sxs-lookup"><span data-stu-id="c6592-150">Indicates that this cmdlet returns the **AzureStorageFile** object that it creates or uploads.</span></span>

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

### <span data-ttu-id="c6592-151">-路徑</span><span class="sxs-lookup"><span data-stu-id="c6592-151">-Path</span></span>
<span data-ttu-id="c6592-152">指定檔案或資料夾的路徑。</span><span class="sxs-lookup"><span data-stu-id="c6592-152">Specifies the path of a file or folder.</span></span>
<span data-ttu-id="c6592-153">此 Cmdlet 會上傳內容至此參數指定的檔案，或此參數指定之資料夾中的檔案。</span><span class="sxs-lookup"><span data-stu-id="c6592-153">This cmdlet uploads contents to the file that this parameter specifies, or to a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="c6592-154">如果您指定資料夾，此 Cmdlet 會建立與來源檔案名稱相同的檔案。</span><span class="sxs-lookup"><span data-stu-id="c6592-154">If you specify a folder, this cmdlet creates a file that has the same name as the source file.</span></span>
<span data-ttu-id="c6592-155">如果您指定不存在之檔案的路徑，此 Cmdlet 會建立該檔案，並會將內容存到該檔案。</span><span class="sxs-lookup"><span data-stu-id="c6592-155">If you specify a path of a file that does not exist, this cmdlet creates that file and saves the contents to that file.</span></span>
<span data-ttu-id="c6592-156">如果您指定已存在的檔案，而且您指定 _Force_ 參數，此 Cmdlet 會覆寫檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="c6592-156">If you specify a file that already exists, and you specify the _Force_ parameter, this cmdlet overwrites the contents of the file.</span></span>
<span data-ttu-id="c6592-157">如果您指定已存在的檔案，但未指定 _Force，_ 此 Cmdlet 不會變更，並會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="c6592-157">If you specify a file that already exists and you do not specify _Force_, this cmdlet makes no change, and returns an error.</span></span>
<span data-ttu-id="c6592-158">如果您指定不存在的資料夾路徑，此 Cmdlet 不會變更，並會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="c6592-158">If you specify a path of a folder that does not exist, this cmdlet makes no change, and returns an error.</span></span>

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

### <span data-ttu-id="c6592-159">-PreserveSMBAttribute</span><span class="sxs-lookup"><span data-stu-id="c6592-159">-PreserveSMBAttribute</span></span>
<span data-ttu-id="c6592-160">將來源檔案 SMB 屬性 (檔指定、檔案建立時間、檔案上次寫入時間) 目標檔案中。</span><span class="sxs-lookup"><span data-stu-id="c6592-160">Keep the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in destination File.</span></span> <span data-ttu-id="c6592-161">此參數僅適用于 Windows。</span><span class="sxs-lookup"><span data-stu-id="c6592-161">This parameter is only available on Windows.</span></span>

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

### <span data-ttu-id="c6592-162">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c6592-162">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c6592-163">指定要求的伺服器部分之時間長度。</span><span class="sxs-lookup"><span data-stu-id="c6592-163">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="c6592-164">-共用</span><span class="sxs-lookup"><span data-stu-id="c6592-164">-Share</span></span>
<span data-ttu-id="c6592-165">指定 **CloudFileShare** 物件。</span><span class="sxs-lookup"><span data-stu-id="c6592-165">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="c6592-166">此 Cmdlet 會上傳到此參數指定之檔案共用中的檔案。</span><span class="sxs-lookup"><span data-stu-id="c6592-166">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>
<span data-ttu-id="c6592-167">若要取得 **CloudFileShare** 物件，請使用 Get-AzStorageShare Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c6592-167">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="c6592-168">此物件包含儲存內容。</span><span class="sxs-lookup"><span data-stu-id="c6592-168">This object contains the storage context.</span></span>
<span data-ttu-id="c6592-169">如果您指定此參數，請勿指定 *CoNtext* 參數。</span><span class="sxs-lookup"><span data-stu-id="c6592-169">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="c6592-170">-ShareName</span><span class="sxs-lookup"><span data-stu-id="c6592-170">-ShareName</span></span>
<span data-ttu-id="c6592-171">指定檔案共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="c6592-171">Specifies the name of the file share.</span></span>
<span data-ttu-id="c6592-172">此 Cmdlet 會上傳到此參數指定之檔案共用中的檔案。</span><span class="sxs-lookup"><span data-stu-id="c6592-172">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>

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

### <span data-ttu-id="c6592-173">-來源</span><span class="sxs-lookup"><span data-stu-id="c6592-173">-Source</span></span>
<span data-ttu-id="c6592-174">指定此 Cmdlet 上傳的來源檔案。</span><span class="sxs-lookup"><span data-stu-id="c6592-174">Specifies the source file that this cmdlet uploads.</span></span>
<span data-ttu-id="c6592-175">如果您指定不存在的檔案，此 Cmdlet 會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="c6592-175">If you specify a file that does not exist, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c6592-176">-確認</span><span class="sxs-lookup"><span data-stu-id="c6592-176">-Confirm</span></span>
<span data-ttu-id="c6592-177">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c6592-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6592-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6592-178">-WhatIf</span></span>
<span data-ttu-id="c6592-179">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c6592-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6592-180">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c6592-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6592-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6592-181">CommonParameters</span></span>
<span data-ttu-id="c6592-182">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c6592-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6592-183">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="c6592-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6592-184">輸入</span><span class="sxs-lookup"><span data-stu-id="c6592-184">INPUTS</span></span>

### <span data-ttu-id="c6592-185">Microsoft.Azure.storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="c6592-185">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="c6592-186">Microsoft.Azure.storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="c6592-186">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="c6592-187">System.String</span><span class="sxs-lookup"><span data-stu-id="c6592-187">System.String</span></span>

### <span data-ttu-id="c6592-188">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="c6592-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c6592-189">輸出</span><span class="sxs-lookup"><span data-stu-id="c6592-189">OUTPUTS</span></span>

### <span data-ttu-id="c6592-190">Microsoft.WindowsAzure.Commands.Common.storage.ResourceModel.AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="c6592-190">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="c6592-191">筆記</span><span class="sxs-lookup"><span data-stu-id="c6592-191">NOTES</span></span>

## <span data-ttu-id="c6592-192">相關連結</span><span class="sxs-lookup"><span data-stu-id="c6592-192">RELATED LINKS</span></span>

[<span data-ttu-id="c6592-193">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="c6592-193">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)

[<span data-ttu-id="c6592-194">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="c6592-194">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="c6592-195">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="c6592-195">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)
