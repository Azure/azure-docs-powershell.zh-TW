---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/close-azstoragefilehandle
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Close-AzStorageFileHandle.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Close-AzStorageFileHandle.md
ms.openlocfilehash: 71985cc978425c343e535e6455172f61e5397934
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911270"
---
# <span data-ttu-id="a324e-101">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="a324e-101">Close-AzStorageFileHandle</span></span>

## <span data-ttu-id="a324e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a324e-102">SYNOPSIS</span></span>
<span data-ttu-id="a324e-103">關閉檔案共用、檔案目錄或檔案的檔案控點。</span><span class="sxs-lookup"><span data-stu-id="a324e-103">Closes file handles of a file share, a file directory or a file.</span></span>

## <span data-ttu-id="a324e-104">語法</span><span class="sxs-lookup"><span data-stu-id="a324e-104">SYNTAX</span></span>

### <span data-ttu-id="a324e-105">ShareNameCloseAll (預設) </span><span class="sxs-lookup"><span data-stu-id="a324e-105">ShareNameCloseAll (Default)</span></span>
```
Close-AzStorageFileHandle [-ShareName] <String> [[-Path] <String>] [-Recursive] [-CloseAll]
 [-Context <IStorageContext>] [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a324e-106">ShareNameCloseSingle</span><span class="sxs-lookup"><span data-stu-id="a324e-106">ShareNameCloseSingle</span></span>
```
Close-AzStorageFileHandle [-ShareName] <String> -FileHandle <PSFileHandle> [-Context <IStorageContext>]
 [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a324e-107">ShareCloseAll</span><span class="sxs-lookup"><span data-stu-id="a324e-107">ShareCloseAll</span></span>
```
Close-AzStorageFileHandle [-Share] <CloudFileShare> [[-Path] <String>] [-Recursive] [-CloseAll] [-PassThru]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a324e-108">ShareCloseSingle</span><span class="sxs-lookup"><span data-stu-id="a324e-108">ShareCloseSingle</span></span>
```
Close-AzStorageFileHandle [-Share] <CloudFileShare> -FileHandle <PSFileHandle> [-PassThru] [-AsJob]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a324e-109">DirectoryCloseAll</span><span class="sxs-lookup"><span data-stu-id="a324e-109">DirectoryCloseAll</span></span>
```
Close-AzStorageFileHandle [-Directory] <CloudFileDirectory> [[-Path] <String>] [-Recursive] [-CloseAll]
 [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a324e-110">FileCloseAll</span><span class="sxs-lookup"><span data-stu-id="a324e-110">FileCloseAll</span></span>
```
Close-AzStorageFileHandle [-File] <CloudFile> [-CloseAll] [-PassThru] [-AsJob]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a324e-111">描述</span><span class="sxs-lookup"><span data-stu-id="a324e-111">DESCRIPTION</span></span>
<span data-ttu-id="a324e-112">**Close-AzStorageFileHandle** Cmdlet 會關閉檔案共用、檔案目錄或檔案的檔案控點。</span><span class="sxs-lookup"><span data-stu-id="a324e-112">The **Close-AzStorageFileHandle** cmdlet closes file handles of a  file share, or file directory or a file.</span></span>

## <span data-ttu-id="a324e-113">例子</span><span class="sxs-lookup"><span data-stu-id="a324e-113">EXAMPLES</span></span>

### <span data-ttu-id="a324e-114">範例 1：列出目前儲存空間帳戶的所有檔案共用，然後以遞迴的方式關閉檔案共用的所有檔案控點。</span><span class="sxs-lookup"><span data-stu-id="a324e-114">Example 1: Lists all file shares of current Storage Account, and close all file handles of the file shares recursively.</span></span>
```
PS C:\>Get-AzStorageShare | Close-AzStorageFileHandle -CloseAll -Recursive
```

<span data-ttu-id="a324e-115">此命令會列出目前儲存空間帳戶的所有檔案共用，並以遞迴的方式關閉檔案共用的所有檔案控點。</span><span class="sxs-lookup"><span data-stu-id="a324e-115">This command lists all file shares of current Storage Account, and close all file handles of the file shares recursively..</span></span>

### <span data-ttu-id="a324e-116">範例 2：以遞迴的方式關閉檔案目錄上的所有檔案控點，並顯示已關閉的檔案控點計數</span><span class="sxs-lookup"><span data-stu-id="a324e-116">Example 2: Close all file handles on a file directory recursively and show the closed file handle count</span></span>
```
PS C:\>Close-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2' -Recursive -CloseAll -PassThru
10
```

<span data-ttu-id="a324e-117">此命令會關閉檔案目錄上的所有檔案控點，並顯示已關閉的檔案控點計數。</span><span class="sxs-lookup"><span data-stu-id="a324e-117">This command closes all file handles on a file directory and show the closed file handle count.</span></span>

### <span data-ttu-id="a324e-118">範例 3：關閉檔案目錄上 1 天前開啟的所有檔案控點</span><span class="sxs-lookup"><span data-stu-id="a324e-118">Example 3: Close all file handles which is opened 1 day ago on a file directory</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2' -Recursive | ? {$_.OpenTime.DateTime.AddDays(1) -lt (Get-Date)} | Close-AzStorageFileHandle -ShareName "mysharename"
```

<span data-ttu-id="a324e-119">此命令會以遞迴的方式列出檔案目錄上的所有檔案控點、篩選掉 1 天前開啟的控點，然後關閉這些控點。</span><span class="sxs-lookup"><span data-stu-id="a324e-119">This command lists all file handles on a file directory recursively, filters out the handles which are opened 1 day ago, and then close them.</span></span>

### <span data-ttu-id="a324e-120">範例 4：關閉檔案上的所有檔案控點</span><span class="sxs-lookup"><span data-stu-id="a324e-120">Example 4: Close all file handles on a file</span></span>
```
PS C:\>Close-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2/test.txt' -CloseAll
```

<span data-ttu-id="a324e-121">此命令會關閉檔案上的所有檔案控點。</span><span class="sxs-lookup"><span data-stu-id="a324e-121">This command closes all file handles on a file.</span></span>

## <span data-ttu-id="a324e-122">參數</span><span class="sxs-lookup"><span data-stu-id="a324e-122">PARAMETERS</span></span>

### <span data-ttu-id="a324e-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a324e-123">-AsJob</span></span>
<span data-ttu-id="a324e-124">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a324e-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a324e-125">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a324e-125">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a324e-126">用戶端會針對每個要求的最大執行時間 ，以碼錶示。</span><span class="sxs-lookup"><span data-stu-id="a324e-126">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="a324e-127">-CloseAll</span><span class="sxs-lookup"><span data-stu-id="a324e-127">-CloseAll</span></span>
<span data-ttu-id="a324e-128">強制關閉所有檔案控點。</span><span class="sxs-lookup"><span data-stu-id="a324e-128">Force close all File handles.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ShareNameCloseAll, ShareCloseAll, DirectoryCloseAll, FileCloseAll
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a324e-129">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a324e-129">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a324e-130">同時同步處理工作的總數量。</span><span class="sxs-lookup"><span data-stu-id="a324e-130">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="a324e-131">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="a324e-131">The default value is 10.</span></span>

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

### <span data-ttu-id="a324e-132">-內容</span><span class="sxs-lookup"><span data-stu-id="a324e-132">-Context</span></span>
<span data-ttu-id="a324e-133">Azure 儲存體內容物件</span><span class="sxs-lookup"><span data-stu-id="a324e-133">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareNameCloseAll, ShareNameCloseSingle
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a324e-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a324e-134">-DefaultProfile</span></span>
<span data-ttu-id="a324e-135">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a324e-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a324e-136">-目錄</span><span class="sxs-lookup"><span data-stu-id="a324e-136">-Directory</span></span>
<span data-ttu-id="a324e-137">CloudFileDirectory 物件指出列出檔案/目錄的基本資料夾。</span><span class="sxs-lookup"><span data-stu-id="a324e-137">CloudFileDirectory object indicated the base folder where the files/directories would be listed.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: DirectoryCloseAll
Aliases: CloudFileDirectory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a324e-138">-檔案</span><span class="sxs-lookup"><span data-stu-id="a324e-138">-File</span></span>
<span data-ttu-id="a324e-139">CloudFile 物件表示檔案要關閉控點。</span><span class="sxs-lookup"><span data-stu-id="a324e-139">CloudFile object indicated the file to close handle.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileCloseAll
Aliases: CloudFile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a324e-140">-FileHandle</span><span class="sxs-lookup"><span data-stu-id="a324e-140">-FileHandle</span></span>
<span data-ttu-id="a324e-141">要關閉的檔案控點。</span><span class="sxs-lookup"><span data-stu-id="a324e-141">The File Handle to close.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSFileHandle
Parameter Sets: ShareNameCloseSingle, ShareCloseSingle
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a324e-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a324e-142">-PassThru</span></span>
<span data-ttu-id="a324e-143">會返回已關閉的檔案控點計數。</span><span class="sxs-lookup"><span data-stu-id="a324e-143">Return the count of closed file handles.</span></span>

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

### <span data-ttu-id="a324e-144">-路徑</span><span class="sxs-lookup"><span data-stu-id="a324e-144">-Path</span></span>
<span data-ttu-id="a324e-145">現有檔案/目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="a324e-145">Path to an existing file/directory.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareNameCloseAll, ShareCloseAll, DirectoryCloseAll
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a324e-146">-遞迴</span><span class="sxs-lookup"><span data-stu-id="a324e-146">-Recursive</span></span>
<span data-ttu-id="a324e-147">清單控點為遞迴。</span><span class="sxs-lookup"><span data-stu-id="a324e-147">List handles Recursively.</span></span>
<span data-ttu-id="a324e-148">僅適用于檔案目錄。</span><span class="sxs-lookup"><span data-stu-id="a324e-148">Only works on File Directory.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ShareNameCloseAll, ShareCloseAll, DirectoryCloseAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a324e-149">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a324e-149">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a324e-150">伺服器會在每個要求中以碼錶示時間。</span><span class="sxs-lookup"><span data-stu-id="a324e-150">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="a324e-151">-共用</span><span class="sxs-lookup"><span data-stu-id="a324e-151">-Share</span></span>
<span data-ttu-id="a324e-152">CloudFileShare 物件表示要列出檔案/目錄的共用。</span><span class="sxs-lookup"><span data-stu-id="a324e-152">CloudFileShare object indicated the share where the files/directories would be listed.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: ShareCloseAll, ShareCloseSingle
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a324e-153">-ShareName</span><span class="sxs-lookup"><span data-stu-id="a324e-153">-ShareName</span></span>
<span data-ttu-id="a324e-154">列出檔案/目錄的檔案共用名稱稱。</span><span class="sxs-lookup"><span data-stu-id="a324e-154">Name of the file share where the files/directories would be listed.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareNameCloseAll, ShareNameCloseSingle
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a324e-155">-確認</span><span class="sxs-lookup"><span data-stu-id="a324e-155">-Confirm</span></span>
<span data-ttu-id="a324e-156">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a324e-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a324e-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a324e-157">-WhatIf</span></span>
<span data-ttu-id="a324e-158">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a324e-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a324e-159">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a324e-159">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a324e-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a324e-160">CommonParameters</span></span>
<span data-ttu-id="a324e-161">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a324e-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a324e-162">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a324e-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a324e-163">輸入</span><span class="sxs-lookup"><span data-stu-id="a324e-163">INPUTS</span></span>

### <span data-ttu-id="a324e-164">Microsoft.Azure.storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="a324e-164">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="a324e-165">Microsoft.Azure.storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="a324e-165">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="a324e-166">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="a324e-166">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a324e-167">輸出</span><span class="sxs-lookup"><span data-stu-id="a324e-167">OUTPUTS</span></span>

### <span data-ttu-id="a324e-168">Microsoft.Azure.storage.File.CloseFileHandleResultSegment</span><span class="sxs-lookup"><span data-stu-id="a324e-168">Microsoft.Azure.Storage.File.CloseFileHandleResultSegment</span></span>

## <span data-ttu-id="a324e-169">筆記</span><span class="sxs-lookup"><span data-stu-id="a324e-169">NOTES</span></span>

## <span data-ttu-id="a324e-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="a324e-170">RELATED LINKS</span></span>
