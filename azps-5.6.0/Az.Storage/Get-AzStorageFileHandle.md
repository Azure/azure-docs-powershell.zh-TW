---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragefilehandle
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileHandle.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileHandle.md
ms.openlocfilehash: af5d807fcf7ad93536becd9c40df34b5e3b14220
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913649"
---
# <span data-ttu-id="38b24-101">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="38b24-101">Get-AzStorageFileHandle</span></span>

## <span data-ttu-id="38b24-102">簡介</span><span class="sxs-lookup"><span data-stu-id="38b24-102">SYNOPSIS</span></span>
<span data-ttu-id="38b24-103">列出檔案共用、檔案目錄或檔案的檔案控點。</span><span class="sxs-lookup"><span data-stu-id="38b24-103">Lists file handles of a file share, a file directory or a file.</span></span>

## <span data-ttu-id="38b24-104">語法</span><span class="sxs-lookup"><span data-stu-id="38b24-104">SYNTAX</span></span>

### <span data-ttu-id="38b24-105">ShareName (預設) </span><span class="sxs-lookup"><span data-stu-id="38b24-105">ShareName (Default)</span></span>
```
Get-AzStorageFileHandle [-ShareName] <String> [[-Path] <String>] [-Recursive] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="38b24-106">共用</span><span class="sxs-lookup"><span data-stu-id="38b24-106">Share</span></span>
```
Get-AzStorageFileHandle [-Share] <CloudFileShare> [[-Path] <String>] [-Recursive]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="38b24-107">目錄</span><span class="sxs-lookup"><span data-stu-id="38b24-107">Directory</span></span>
```
Get-AzStorageFileHandle [-Directory] <CloudFileDirectory> [[-Path] <String>] [-Recursive]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="38b24-108">檔</span><span class="sxs-lookup"><span data-stu-id="38b24-108">File</span></span>
```
Get-AzStorageFileHandle [-File] <CloudFile> [-Recursive] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="38b24-109">描述</span><span class="sxs-lookup"><span data-stu-id="38b24-109">DESCRIPTION</span></span>
<span data-ttu-id="38b24-110">**Get-AzStorageFileHandle** Cmdlet 會列出檔案共用、檔案目錄或檔案的檔案控點。</span><span class="sxs-lookup"><span data-stu-id="38b24-110">The **Get-AzStorageFileHandle** cmdlet lists file handles of a  file share, or file directory or a file.</span></span>

## <span data-ttu-id="38b24-111">例子</span><span class="sxs-lookup"><span data-stu-id="38b24-111">EXAMPLES</span></span>

### <span data-ttu-id="38b24-112">範例 1：以遞迴方式列出檔案共用上的所有檔案控點，並按 ClientIp 和 OpenTime 排序</span><span class="sxs-lookup"><span data-stu-id="38b24-112">Example 1: List all file handles on a file share recursively, and sort by ClientIp and OpenTime</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Recursive | Sort-Object ClientIP,OpenTime 

HandleId    Path                  ClientIp       ClientPort OpenTime             LastReconnectTime FileId               ParentId             SessionId          
--------    ----                  --------       ---------- --------             ----------------- ------               --------             ---------          
28506980357                       104.46.105.229 49805      2019-07-29 08:37:36Z                   0                    0                    9297571480349046273
28506980537 dir1                  104.46.105.229 49805      2019-07-30 09:28:48Z                   10376363910205800448 0                    9297571480349046273
28506980538 dir1                  104.46.105.229 49805      2019-07-30 09:28:48Z                   10376363910205800448 0                    9297571480349046273
28582543365                       104.46.119.170 51675      2019-07-30 09:29:32Z                   0                    0                    9477733061320772929
28582543375 dir1                  104.46.119.170 51675      2019-07-30 09:29:38Z                   10376363910205800448 0                    9477733061320772929
28582543376 dir1                  104.46.119.170 51675      2019-07-30 09:29:38Z                   10376363910205800448 0                    9477733061320772929
```

<span data-ttu-id="38b24-113">此命令會列出檔案共用上的檔案控點，並按 ClientIp 和 OpenTime 排序輸出。</span><span class="sxs-lookup"><span data-stu-id="38b24-113">This command lists file handles on a file share, and sort the output by ClientIp, then by OpenTime.</span></span>

### <span data-ttu-id="38b24-114">範例 2：以遞迴的方式列出檔案目錄上的前 2 個檔案控點</span><span class="sxs-lookup"><span data-stu-id="38b24-114">Example 2: List first 2 file handles on a file directory recursively</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2'  -Recursive -First 2

HandleId    Path      ClientIp       ClientPort OpenTime             LastReconnectTime FileId               ParentId             SessionId          
--------    ----      --------       ---------- --------             ----------------- ------               --------             ---------          
24057151779 dir1/dir2 104.46.105.229 50861      2019-06-18 07:39:23Z                   16140971433240035328 11529285414812647424 9549812641162070049
24057151780 dir1/dir2 104.46.105.229 50861      2019-06-18 07:39:23Z                   16140971433240035328 11529285414812647424 9549812641162070049
```

<span data-ttu-id="38b24-115">此命令會以遞迴的方式列出檔案目錄上的前 2 個檔案控點。</span><span class="sxs-lookup"><span data-stu-id="38b24-115">This command lists first 2 file handles on a file directory recursively .</span></span>

### <span data-ttu-id="38b24-116">範例 3：列出檔案的第 3 個到第 6 個檔案控點</span><span class="sxs-lookup"><span data-stu-id="38b24-116">Example 3: List the 3rd to the 6th file handles on a file</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2/test.txt' -skip 2 -First 4 

HandleId    Path               ClientIp       ClientPort OpenTime             LastReconnectTime FileId              ParentId             SessionId          
--------    ----               --------       ---------- --------             ----------------- ------              --------             ---------          
24055513248 dir1/dir2/test.txt 104.46.105.229 49817      2019-06-18 08:21:59Z                   9223407221226864640 16140971433240035328 9338416139169958321
24055513249 dir1/dir2/test.txt 104.46.105.229 49817      2019-06-18 08:21:59Z                   9223407221226864640 16140971433240035328 9338416139169958321
24055513252 dir1/dir2/test.txt 104.46.105.229 49964      2019-06-18 08:22:54Z                   9223407221226864640 16140971433240035328 9338416138431762125
24055513253 dir1/dir2/test.txt 104.46.105.229 49964      2019-06-18 08:22:54Z                   9223407221226864640 16140971433240035328 9338416138431762125
```

<span data-ttu-id="38b24-117">此命令會列出檔案的第 3 個到第 6 個檔案控點。</span><span class="sxs-lookup"><span data-stu-id="38b24-117">This command lists the 3rd to the 6th file handles on a file.</span></span>

## <span data-ttu-id="38b24-118">參數</span><span class="sxs-lookup"><span data-stu-id="38b24-118">PARAMETERS</span></span>

### <span data-ttu-id="38b24-119">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="38b24-119">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="38b24-120">用戶端會針對每個要求的最大執行時間 ，以碼錶示。</span><span class="sxs-lookup"><span data-stu-id="38b24-120">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="38b24-121">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="38b24-121">-ConcurrentTaskCount</span></span>
<span data-ttu-id="38b24-122">同時同步處理工作的總數量。</span><span class="sxs-lookup"><span data-stu-id="38b24-122">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="38b24-123">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="38b24-123">The default value is 10.</span></span>

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

### <span data-ttu-id="38b24-124">-內容</span><span class="sxs-lookup"><span data-stu-id="38b24-124">-Context</span></span>
<span data-ttu-id="38b24-125">Azure 儲存體內容物件</span><span class="sxs-lookup"><span data-stu-id="38b24-125">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="38b24-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38b24-126">-DefaultProfile</span></span>
<span data-ttu-id="38b24-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="38b24-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38b24-128">-目錄</span><span class="sxs-lookup"><span data-stu-id="38b24-128">-Directory</span></span>
<span data-ttu-id="38b24-129">CloudFileDirectory 物件指出列出檔案/目錄的基本資料夾。</span><span class="sxs-lookup"><span data-stu-id="38b24-129">CloudFileDirectory object indicated the base folder where the files/directories would be listed.</span></span>

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

### <span data-ttu-id="38b24-130">-檔案</span><span class="sxs-lookup"><span data-stu-id="38b24-130">-File</span></span>
<span data-ttu-id="38b24-131">CloudFile 物件將檔案表示為清單的檔案控點。</span><span class="sxs-lookup"><span data-stu-id="38b24-131">CloudFile object indicated the file to list File Handles.</span></span>

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

### <span data-ttu-id="38b24-132">-路徑</span><span class="sxs-lookup"><span data-stu-id="38b24-132">-Path</span></span>
<span data-ttu-id="38b24-133">現有檔案/目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="38b24-133">Path to an existing file/directory.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, Share, Directory
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38b24-134">-遞迴</span><span class="sxs-lookup"><span data-stu-id="38b24-134">-Recursive</span></span>
<span data-ttu-id="38b24-135">清單控點為遞迴。</span><span class="sxs-lookup"><span data-stu-id="38b24-135">List handles Recursively.</span></span>
<span data-ttu-id="38b24-136">僅適用于檔案目錄。</span><span class="sxs-lookup"><span data-stu-id="38b24-136">Only works on File Directory.</span></span>

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

### <span data-ttu-id="38b24-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="38b24-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="38b24-138">伺服器會在每個要求中以碼錶示時間。</span><span class="sxs-lookup"><span data-stu-id="38b24-138">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="38b24-139">-共用</span><span class="sxs-lookup"><span data-stu-id="38b24-139">-Share</span></span>
<span data-ttu-id="38b24-140">CloudFileShare 物件表示要列出檔案/目錄的共用。</span><span class="sxs-lookup"><span data-stu-id="38b24-140">CloudFileShare object indicated the share where the files/directories would be listed.</span></span>

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

### <span data-ttu-id="38b24-141">-ShareName</span><span class="sxs-lookup"><span data-stu-id="38b24-141">-ShareName</span></span>
<span data-ttu-id="38b24-142">列出檔案/目錄的檔案共用名稱稱。</span><span class="sxs-lookup"><span data-stu-id="38b24-142">Name of the file share where the files/directories would be listed.</span></span>

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

### <span data-ttu-id="38b24-143">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="38b24-143">-IncludeTotalCount</span></span>
<span data-ttu-id="38b24-144">以整數及 (來) 來報告資料集中的物件數目。</span><span class="sxs-lookup"><span data-stu-id="38b24-144">Reports the number of objects in the data set (an integer) followed by the objects.</span></span> <span data-ttu-id="38b24-145">如果 Cmdlet 無法判斷總計，會傳回'未知總計計數」。</span><span class="sxs-lookup"><span data-stu-id="38b24-145">If the cmdlet cannot determine the total count, it returns 'Unknown total count'.</span></span>
<span data-ttu-id="38b24-146">目前，此參數沒有任何影響。</span><span class="sxs-lookup"><span data-stu-id="38b24-146">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="38b24-147">-略過</span><span class="sxs-lookup"><span data-stu-id="38b24-147">-Skip</span></span>
<span data-ttu-id="38b24-148">忽略第一個 'n' 物件，然後獲得其餘的物件。</span><span class="sxs-lookup"><span data-stu-id="38b24-148">Ignores the first 'n' objects and then gets the remaining objects.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38b24-149">-第一個</span><span class="sxs-lookup"><span data-stu-id="38b24-149">-First</span></span>
<span data-ttu-id="38b24-150">只會獲得第一個 'n' 物件。</span><span class="sxs-lookup"><span data-stu-id="38b24-150">Gets only the first 'n' objects.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38b24-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38b24-151">CommonParameters</span></span>
<span data-ttu-id="38b24-152">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="38b24-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38b24-153">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="38b24-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38b24-154">輸入</span><span class="sxs-lookup"><span data-stu-id="38b24-154">INPUTS</span></span>

### <span data-ttu-id="38b24-155">Microsoft.Azure.storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="38b24-155">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="38b24-156">Microsoft.Azure.storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="38b24-156">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="38b24-157">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="38b24-157">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="38b24-158">輸出</span><span class="sxs-lookup"><span data-stu-id="38b24-158">OUTPUTS</span></span>

### <span data-ttu-id="38b24-159">Microsoft.Azure.storage.File.FileHandleResultSegment</span><span class="sxs-lookup"><span data-stu-id="38b24-159">Microsoft.Azure.Storage.File.FileHandleResultSegment</span></span>

## <span data-ttu-id="38b24-160">筆記</span><span class="sxs-lookup"><span data-stu-id="38b24-160">NOTES</span></span>

## <span data-ttu-id="38b24-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="38b24-161">RELATED LINKS</span></span>
