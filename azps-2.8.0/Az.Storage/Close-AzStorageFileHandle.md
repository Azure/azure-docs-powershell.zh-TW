---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/close-azstoragefilehandle
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Close-AzStorageFileHandle.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Close-AzStorageFileHandle.md
ms.openlocfilehash: cca517246f548deb64cba1b4bc737de88628e7f2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792904"
---
# <span data-ttu-id="e216e-101">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="e216e-101">Close-AzStorageFileHandle</span></span>

## <span data-ttu-id="e216e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e216e-102">SYNOPSIS</span></span>
<span data-ttu-id="e216e-103">關閉檔案共用、檔案目錄或檔案的檔案控制代碼。</span><span class="sxs-lookup"><span data-stu-id="e216e-103">Closes file handles of a file share, a file directory or a file.</span></span>

## <span data-ttu-id="e216e-104">句法</span><span class="sxs-lookup"><span data-stu-id="e216e-104">SYNTAX</span></span>

### <span data-ttu-id="e216e-105">ShareNameCloseAll (預設) </span><span class="sxs-lookup"><span data-stu-id="e216e-105">ShareNameCloseAll (Default)</span></span>
```
Close-AzStorageFileHandle [-ShareName] <String> [[-Path] <String>] [-Recursive] [-CloseAll]
 [-Context <IStorageContext>] [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e216e-106">ShareNameCloseSingle</span><span class="sxs-lookup"><span data-stu-id="e216e-106">ShareNameCloseSingle</span></span>
```
Close-AzStorageFileHandle [-ShareName] <String> -FileHandle <PSFileHandle> [-Context <IStorageContext>]
 [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e216e-107">ShareCloseAll</span><span class="sxs-lookup"><span data-stu-id="e216e-107">ShareCloseAll</span></span>
```
Close-AzStorageFileHandle [-Share] <CloudFileShare> [[-Path] <String>] [-Recursive] [-CloseAll] [-PassThru]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e216e-108">ShareCloseSingle</span><span class="sxs-lookup"><span data-stu-id="e216e-108">ShareCloseSingle</span></span>
```
Close-AzStorageFileHandle [-Share] <CloudFileShare> -FileHandle <PSFileHandle> [-PassThru] [-AsJob]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e216e-109">DirectoryCloseAll</span><span class="sxs-lookup"><span data-stu-id="e216e-109">DirectoryCloseAll</span></span>
```
Close-AzStorageFileHandle [-Directory] <CloudFileDirectory> [[-Path] <String>] [-Recursive] [-CloseAll]
 [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e216e-110">FileCloseAll</span><span class="sxs-lookup"><span data-stu-id="e216e-110">FileCloseAll</span></span>
```
Close-AzStorageFileHandle [-File] <CloudFile> [-CloseAll] [-PassThru] [-AsJob]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e216e-111">說明</span><span class="sxs-lookup"><span data-stu-id="e216e-111">DESCRIPTION</span></span>
<span data-ttu-id="e216e-112">**AzStorageFileHandle** Cmdlet 會關閉檔案共用或檔案目錄或檔案的檔案控制代碼。</span><span class="sxs-lookup"><span data-stu-id="e216e-112">The **Close-AzStorageFileHandle** cmdlet closes file handles of a  file share, or file directory or a file.</span></span>

## <span data-ttu-id="e216e-113">示例</span><span class="sxs-lookup"><span data-stu-id="e216e-113">EXAMPLES</span></span>

### <span data-ttu-id="e216e-114">範例1：列出目前儲存空間帳戶的所有檔案共用，並以遞迴方式關閉檔案共用的所有檔案控制碼。</span><span class="sxs-lookup"><span data-stu-id="e216e-114">Example 1: Lists all file shares of current Storage Account, and close all file handles of the file shares recursively.</span></span>
```
PS C:\>Get-AzStorageShare | Close-AzStorageFileHandle -CloseAll -Recursive
```

<span data-ttu-id="e216e-115">這個命令會列出目前儲存空間帳戶的所有檔案共用，並以遞迴方式關閉檔案共用的所有檔案控制代碼。</span><span class="sxs-lookup"><span data-stu-id="e216e-115">This command lists all file shares of current Storage Account, and close all file handles of the file shares recursively..</span></span>

### <span data-ttu-id="e216e-116">範例2：以遞迴方式關閉檔案目錄上的所有檔案控點，並顯示已關閉的檔案控制碼計數</span><span class="sxs-lookup"><span data-stu-id="e216e-116">Example 2: Close all file handles on a file directory recursively and show the closed file handle count</span></span>
```
PS C:\>Close-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2' -Recursive -CloseAll -PassThru
10
```

<span data-ttu-id="e216e-117">這個命令會關閉檔案目錄上的所有檔案控制碼，並顯示已關閉的檔案控制碼計數。</span><span class="sxs-lookup"><span data-stu-id="e216e-117">This command closes all file handles on a file directory and show the closed file handle count.</span></span>

### <span data-ttu-id="e216e-118">範例3：關閉檔案目錄1天前開啟的所有檔案控點</span><span class="sxs-lookup"><span data-stu-id="e216e-118">Example 3: Close all file handles which is opened 1 day ago on a file directory</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2' -Recursive | ? {$_.OpenTime.DateTime.AddDays(1) -lt (Get-Date)} | Close-AzStorageFileHandle -ShareName "mysharename"
```

<span data-ttu-id="e216e-119">這個命令會以遞迴方式列出檔案目錄中的所有檔案控制碼，篩選掉在1天前開啟的控制碼，然後關閉它們。</span><span class="sxs-lookup"><span data-stu-id="e216e-119">This command lists all file handles on a file directory recursively, filters out the handles which are opened 1 day ago, and then close them.</span></span>

### <span data-ttu-id="e216e-120">範例4：關閉檔案中的所有檔案控制代碼</span><span class="sxs-lookup"><span data-stu-id="e216e-120">Example 4: Close all file handles on a file</span></span> 
```
PS C:\>Close-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2/test.txt' -CloseAll
```

<span data-ttu-id="e216e-121">這個命令會關閉檔案上的所有檔案控制碼。</span><span class="sxs-lookup"><span data-stu-id="e216e-121">This command closes all file handles on a file.</span></span>

## <span data-ttu-id="e216e-122">參數</span><span class="sxs-lookup"><span data-stu-id="e216e-122">PARAMETERS</span></span>

### <span data-ttu-id="e216e-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e216e-123">-AsJob</span></span>
<span data-ttu-id="e216e-124">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e216e-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e216e-125">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e216e-125">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="e216e-126">用戶端每個要求的最大執行時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="e216e-126">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="e216e-127">-CloseAll</span><span class="sxs-lookup"><span data-stu-id="e216e-127">-CloseAll</span></span>
<span data-ttu-id="e216e-128">強制關閉所有檔案控制代碼。</span><span class="sxs-lookup"><span data-stu-id="e216e-128">Force close all File handles.</span></span>

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

### <span data-ttu-id="e216e-129">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="e216e-129">-ConcurrentTaskCount</span></span>
<span data-ttu-id="e216e-130">並行非同步工作的總數量。</span><span class="sxs-lookup"><span data-stu-id="e216e-130">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="e216e-131">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="e216e-131">The default value is 10.</span></span>

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

### <span data-ttu-id="e216e-132">-內容</span><span class="sxs-lookup"><span data-stu-id="e216e-132">-Context</span></span>
<span data-ttu-id="e216e-133">Azure 儲存區內容物件</span><span class="sxs-lookup"><span data-stu-id="e216e-133">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="e216e-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e216e-134">-DefaultProfile</span></span>
<span data-ttu-id="e216e-135">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e216e-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e216e-136">-Directory</span><span class="sxs-lookup"><span data-stu-id="e216e-136">-Directory</span></span>
<span data-ttu-id="e216e-137">CloudFileDirectory 物件表示會列出檔案/目錄的基底資料夾。</span><span class="sxs-lookup"><span data-stu-id="e216e-137">CloudFileDirectory object indicated the base folder where the files/directories would be listed.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: DirectoryCloseAll
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e216e-138">檔案</span><span class="sxs-lookup"><span data-stu-id="e216e-138">-File</span></span>
<span data-ttu-id="e216e-139">CloudFile 物件指出檔案要關閉控點。</span><span class="sxs-lookup"><span data-stu-id="e216e-139">CloudFile object indicated the file to close handle.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileCloseAll
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e216e-140">-FileHandle</span><span class="sxs-lookup"><span data-stu-id="e216e-140">-FileHandle</span></span>
<span data-ttu-id="e216e-141">關閉的檔案控制代碼。</span><span class="sxs-lookup"><span data-stu-id="e216e-141">The File Handle to close.</span></span>

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

### <span data-ttu-id="e216e-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e216e-142">-PassThru</span></span>
<span data-ttu-id="e216e-143">傳回封閉式檔案控制碼的計數。</span><span class="sxs-lookup"><span data-stu-id="e216e-143">Return the count of closed file handles.</span></span>

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

### <span data-ttu-id="e216e-144">-Path</span><span class="sxs-lookup"><span data-stu-id="e216e-144">-Path</span></span>
<span data-ttu-id="e216e-145">現有檔案/目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="e216e-145">Path to an existing file/directory.</span></span>

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

### <span data-ttu-id="e216e-146">-Recursive</span><span class="sxs-lookup"><span data-stu-id="e216e-146">-Recursive</span></span>
<span data-ttu-id="e216e-147">遞迴清單控點。</span><span class="sxs-lookup"><span data-stu-id="e216e-147">List handles Recursively.</span></span>
<span data-ttu-id="e216e-148">僅適用于檔案目錄。</span><span class="sxs-lookup"><span data-stu-id="e216e-148">Only works on File Directory.</span></span>

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

### <span data-ttu-id="e216e-149">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e216e-149">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="e216e-150">伺服器針對每個要求的超時時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="e216e-150">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="e216e-151">-共用</span><span class="sxs-lookup"><span data-stu-id="e216e-151">-Share</span></span>
<span data-ttu-id="e216e-152">CloudFileShare 物件表示會列出檔案/目錄的共用位置。</span><span class="sxs-lookup"><span data-stu-id="e216e-152">CloudFileShare object indicated the share where the files/directories would be listed.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: ShareCloseAll, ShareCloseSingle
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e216e-153">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="e216e-153">-ShareName</span></span>
<span data-ttu-id="e216e-154">列出檔案/目錄之檔案共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="e216e-154">Name of the file share where the files/directories would be listed.</span></span>

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

### <span data-ttu-id="e216e-155">-確認</span><span class="sxs-lookup"><span data-stu-id="e216e-155">-Confirm</span></span>
<span data-ttu-id="e216e-156">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e216e-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e216e-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e216e-157">-WhatIf</span></span>
<span data-ttu-id="e216e-158">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e216e-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e216e-159">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e216e-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e216e-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e216e-160">CommonParameters</span></span>
<span data-ttu-id="e216e-161">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e216e-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e216e-162">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e216e-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e216e-163">輸入</span><span class="sxs-lookup"><span data-stu-id="e216e-163">INPUTS</span></span>

### <span data-ttu-id="e216e-164">CloudFileShare （即 Azure）</span><span class="sxs-lookup"><span data-stu-id="e216e-164">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="e216e-165">CloudFileDirectory （即 Azure）</span><span class="sxs-lookup"><span data-stu-id="e216e-165">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="e216e-166">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="e216e-166">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e216e-167">輸出</span><span class="sxs-lookup"><span data-stu-id="e216e-167">OUTPUTS</span></span>

### <span data-ttu-id="e216e-168">CloseFileHandleResultSegment （即 Azure）</span><span class="sxs-lookup"><span data-stu-id="e216e-168">Microsoft.Azure.Storage.File.CloseFileHandleResultSegment</span></span>

## <span data-ttu-id="e216e-169">筆記</span><span class="sxs-lookup"><span data-stu-id="e216e-169">NOTES</span></span>

## <span data-ttu-id="e216e-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="e216e-170">RELATED LINKS</span></span>
