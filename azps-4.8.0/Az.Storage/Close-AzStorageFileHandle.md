---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/close-azstoragefilehandle
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Close-AzStorageFileHandle.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Close-AzStorageFileHandle.md
ms.openlocfilehash: 0ac029d4fbe0ab632671f024ff90ebeca9717d50
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971653"
---
# <span data-ttu-id="35c81-101">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="35c81-101">Close-AzStorageFileHandle</span></span>

## <span data-ttu-id="35c81-102">摘要</span><span class="sxs-lookup"><span data-stu-id="35c81-102">SYNOPSIS</span></span>
<span data-ttu-id="35c81-103">關閉檔案共用、檔案目錄或檔案的檔案控制代碼。</span><span class="sxs-lookup"><span data-stu-id="35c81-103">Closes file handles of a file share, a file directory or a file.</span></span>

## <span data-ttu-id="35c81-104">句法</span><span class="sxs-lookup"><span data-stu-id="35c81-104">SYNTAX</span></span>

### <span data-ttu-id="35c81-105">ShareNameCloseAll (預設) </span><span class="sxs-lookup"><span data-stu-id="35c81-105">ShareNameCloseAll (Default)</span></span>
```
Close-AzStorageFileHandle [-ShareName] <String> [[-Path] <String>] [-Recursive] [-CloseAll]
 [-Context <IStorageContext>] [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35c81-106">ShareNameCloseSingle</span><span class="sxs-lookup"><span data-stu-id="35c81-106">ShareNameCloseSingle</span></span>
```
Close-AzStorageFileHandle [-ShareName] <String> -FileHandle <PSFileHandle> [-Context <IStorageContext>]
 [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="35c81-107">ShareCloseAll</span><span class="sxs-lookup"><span data-stu-id="35c81-107">ShareCloseAll</span></span>
```
Close-AzStorageFileHandle [-Share] <CloudFileShare> [[-Path] <String>] [-Recursive] [-CloseAll] [-PassThru]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="35c81-108">ShareCloseSingle</span><span class="sxs-lookup"><span data-stu-id="35c81-108">ShareCloseSingle</span></span>
```
Close-AzStorageFileHandle [-Share] <CloudFileShare> -FileHandle <PSFileHandle> [-PassThru] [-AsJob]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="35c81-109">DirectoryCloseAll</span><span class="sxs-lookup"><span data-stu-id="35c81-109">DirectoryCloseAll</span></span>
```
Close-AzStorageFileHandle [-Directory] <CloudFileDirectory> [[-Path] <String>] [-Recursive] [-CloseAll]
 [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="35c81-110">FileCloseAll</span><span class="sxs-lookup"><span data-stu-id="35c81-110">FileCloseAll</span></span>
```
Close-AzStorageFileHandle [-File] <CloudFile> [-CloseAll] [-PassThru] [-AsJob]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="35c81-111">說明</span><span class="sxs-lookup"><span data-stu-id="35c81-111">DESCRIPTION</span></span>
<span data-ttu-id="35c81-112">**AzStorageFileHandle** Cmdlet 會關閉檔案共用或檔案目錄或檔案的檔案控制代碼。</span><span class="sxs-lookup"><span data-stu-id="35c81-112">The **Close-AzStorageFileHandle** cmdlet closes file handles of a  file share, or file directory or a file.</span></span>

## <span data-ttu-id="35c81-113">示例</span><span class="sxs-lookup"><span data-stu-id="35c81-113">EXAMPLES</span></span>

### <span data-ttu-id="35c81-114">範例1：列出目前儲存空間帳戶的所有檔案共用，並以遞迴方式關閉檔案共用的所有檔案控制碼。</span><span class="sxs-lookup"><span data-stu-id="35c81-114">Example 1: Lists all file shares of current Storage Account, and close all file handles of the file shares recursively.</span></span>
```
PS C:\>Get-AzStorageShare | Close-AzStorageFileHandle -CloseAll -Recursive
```

<span data-ttu-id="35c81-115">這個命令會列出目前儲存空間帳戶的所有檔案共用，並以遞迴方式關閉檔案共用的所有檔案控制代碼。</span><span class="sxs-lookup"><span data-stu-id="35c81-115">This command lists all file shares of current Storage Account, and close all file handles of the file shares recursively..</span></span>

### <span data-ttu-id="35c81-116">範例2：以遞迴方式關閉檔案目錄上的所有檔案控點，並顯示已關閉的檔案控制碼計數</span><span class="sxs-lookup"><span data-stu-id="35c81-116">Example 2: Close all file handles on a file directory recursively and show the closed file handle count</span></span>
```
PS C:\>Close-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2' -Recursive -CloseAll -PassThru
10
```

<span data-ttu-id="35c81-117">這個命令會關閉檔案目錄上的所有檔案控制碼，並顯示已關閉的檔案控制碼計數。</span><span class="sxs-lookup"><span data-stu-id="35c81-117">This command closes all file handles on a file directory and show the closed file handle count.</span></span>

### <span data-ttu-id="35c81-118">範例3：關閉檔案目錄1天前開啟的所有檔案控點</span><span class="sxs-lookup"><span data-stu-id="35c81-118">Example 3: Close all file handles which is opened 1 day ago on a file directory</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2' -Recursive | ? {$_.OpenTime.DateTime.AddDays(1) -lt (Get-Date)} | Close-AzStorageFileHandle -ShareName "mysharename"
```

<span data-ttu-id="35c81-119">這個命令會以遞迴方式列出檔案目錄中的所有檔案控制碼，篩選掉在1天前開啟的控制碼，然後關閉它們。</span><span class="sxs-lookup"><span data-stu-id="35c81-119">This command lists all file handles on a file directory recursively, filters out the handles which are opened 1 day ago, and then close them.</span></span>

### <span data-ttu-id="35c81-120">範例4：關閉檔案中的所有檔案控制代碼</span><span class="sxs-lookup"><span data-stu-id="35c81-120">Example 4: Close all file handles on a file</span></span>
```
PS C:\>Close-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2/test.txt' -CloseAll
```

<span data-ttu-id="35c81-121">這個命令會關閉檔案上的所有檔案控制碼。</span><span class="sxs-lookup"><span data-stu-id="35c81-121">This command closes all file handles on a file.</span></span>

## <span data-ttu-id="35c81-122">參數</span><span class="sxs-lookup"><span data-stu-id="35c81-122">PARAMETERS</span></span>

### <span data-ttu-id="35c81-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35c81-123">-AsJob</span></span>
<span data-ttu-id="35c81-124">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="35c81-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="35c81-125">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="35c81-125">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="35c81-126">用戶端每個要求的最大執行時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="35c81-126">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="35c81-127">-CloseAll</span><span class="sxs-lookup"><span data-stu-id="35c81-127">-CloseAll</span></span>
<span data-ttu-id="35c81-128">強制關閉所有檔案控制代碼。</span><span class="sxs-lookup"><span data-stu-id="35c81-128">Force close all File handles.</span></span>

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

### <span data-ttu-id="35c81-129">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="35c81-129">-ConcurrentTaskCount</span></span>
<span data-ttu-id="35c81-130">並行非同步工作的總數量。</span><span class="sxs-lookup"><span data-stu-id="35c81-130">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="35c81-131">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="35c81-131">The default value is 10.</span></span>

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

### <span data-ttu-id="35c81-132">-內容</span><span class="sxs-lookup"><span data-stu-id="35c81-132">-Context</span></span>
<span data-ttu-id="35c81-133">Azure 儲存區內容物件</span><span class="sxs-lookup"><span data-stu-id="35c81-133">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="35c81-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35c81-134">-DefaultProfile</span></span>
<span data-ttu-id="35c81-135">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="35c81-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35c81-136">-Directory</span><span class="sxs-lookup"><span data-stu-id="35c81-136">-Directory</span></span>
<span data-ttu-id="35c81-137">CloudFileDirectory 物件表示會列出檔案/目錄的基底資料夾。</span><span class="sxs-lookup"><span data-stu-id="35c81-137">CloudFileDirectory object indicated the base folder where the files/directories would be listed.</span></span>

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

### <span data-ttu-id="35c81-138">檔案</span><span class="sxs-lookup"><span data-stu-id="35c81-138">-File</span></span>
<span data-ttu-id="35c81-139">CloudFile 物件指出檔案要關閉控點。</span><span class="sxs-lookup"><span data-stu-id="35c81-139">CloudFile object indicated the file to close handle.</span></span>

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

### <span data-ttu-id="35c81-140">-FileHandle</span><span class="sxs-lookup"><span data-stu-id="35c81-140">-FileHandle</span></span>
<span data-ttu-id="35c81-141">關閉的檔案控制代碼。</span><span class="sxs-lookup"><span data-stu-id="35c81-141">The File Handle to close.</span></span>

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

### <span data-ttu-id="35c81-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="35c81-142">-PassThru</span></span>
<span data-ttu-id="35c81-143">傳回封閉式檔案控制碼的計數。</span><span class="sxs-lookup"><span data-stu-id="35c81-143">Return the count of closed file handles.</span></span>

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

### <span data-ttu-id="35c81-144">-Path</span><span class="sxs-lookup"><span data-stu-id="35c81-144">-Path</span></span>
<span data-ttu-id="35c81-145">現有檔案/目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="35c81-145">Path to an existing file/directory.</span></span>

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

### <span data-ttu-id="35c81-146">-Recursive</span><span class="sxs-lookup"><span data-stu-id="35c81-146">-Recursive</span></span>
<span data-ttu-id="35c81-147">遞迴清單控點。</span><span class="sxs-lookup"><span data-stu-id="35c81-147">List handles Recursively.</span></span>
<span data-ttu-id="35c81-148">僅適用于檔案目錄。</span><span class="sxs-lookup"><span data-stu-id="35c81-148">Only works on File Directory.</span></span>

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

### <span data-ttu-id="35c81-149">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="35c81-149">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="35c81-150">伺服器針對每個要求的超時時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="35c81-150">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="35c81-151">-共用</span><span class="sxs-lookup"><span data-stu-id="35c81-151">-Share</span></span>
<span data-ttu-id="35c81-152">CloudFileShare 物件表示會列出檔案/目錄的共用位置。</span><span class="sxs-lookup"><span data-stu-id="35c81-152">CloudFileShare object indicated the share where the files/directories would be listed.</span></span>

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

### <span data-ttu-id="35c81-153">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="35c81-153">-ShareName</span></span>
<span data-ttu-id="35c81-154">列出檔案/目錄之檔案共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="35c81-154">Name of the file share where the files/directories would be listed.</span></span>

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

### <span data-ttu-id="35c81-155">-確認</span><span class="sxs-lookup"><span data-stu-id="35c81-155">-Confirm</span></span>
<span data-ttu-id="35c81-156">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="35c81-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35c81-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35c81-157">-WhatIf</span></span>
<span data-ttu-id="35c81-158">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="35c81-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35c81-159">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="35c81-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35c81-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35c81-160">CommonParameters</span></span>
<span data-ttu-id="35c81-161">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="35c81-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35c81-162">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="35c81-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35c81-163">輸入</span><span class="sxs-lookup"><span data-stu-id="35c81-163">INPUTS</span></span>

### <span data-ttu-id="35c81-164">CloudFileShare （即 Azure）</span><span class="sxs-lookup"><span data-stu-id="35c81-164">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="35c81-165">CloudFileDirectory （即 Azure）</span><span class="sxs-lookup"><span data-stu-id="35c81-165">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="35c81-166">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="35c81-166">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="35c81-167">輸出</span><span class="sxs-lookup"><span data-stu-id="35c81-167">OUTPUTS</span></span>

### <span data-ttu-id="35c81-168">CloseFileHandleResultSegment （即 Azure）</span><span class="sxs-lookup"><span data-stu-id="35c81-168">Microsoft.Azure.Storage.File.CloseFileHandleResultSegment</span></span>

## <span data-ttu-id="35c81-169">筆記</span><span class="sxs-lookup"><span data-stu-id="35c81-169">NOTES</span></span>

## <span data-ttu-id="35c81-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="35c81-170">RELATED LINKS</span></span>
