---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzDataLakeGen2Item.md
ms.openlocfilehash: 565267c6f35f52fd3a7a733477ed504d001cb70b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914258"
---
# <span data-ttu-id="0b947-101">New-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="0b947-101">New-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="0b947-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0b947-102">SYNOPSIS</span></span>
<span data-ttu-id="0b947-103">在檔案系統中建立檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="0b947-103">Create a file or directory in a filesystem.</span></span>

## <span data-ttu-id="0b947-104">語法</span><span class="sxs-lookup"><span data-stu-id="0b947-104">SYNTAX</span></span>

### <span data-ttu-id="0b947-105">檔案 (預設) </span><span class="sxs-lookup"><span data-stu-id="0b947-105">File (Default)</span></span>
```
New-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> -Source <String> [-Umask <String>]
 [-Permission <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b947-106">目錄</span><span class="sxs-lookup"><span data-stu-id="0b947-106">Directory</span></span>
```
New-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> [-Directory] [-Umask <String>]
 [-Permission <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b947-107">描述</span><span class="sxs-lookup"><span data-stu-id="0b947-107">DESCRIPTION</span></span>
<span data-ttu-id="0b947-108">**New-AzDataLakeGen2Item** Cmdlet 在 Azure 儲存帳戶中的檔案系統中建立檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="0b947-108">The **New-AzDataLakeGen2Item** cmdlet creates a file or directory in a Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="0b947-109">只有在儲存空間帳戶已啟用階層式命名空間時，此 Cmdlet 才能運作。</span><span class="sxs-lookup"><span data-stu-id="0b947-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="0b947-110">您可以使用"-EnableHierarchicalNamespace $true"執行 「New-AzStorageAccount」Cmdlet 來建立這類帳戶。</span><span class="sxs-lookup"><span data-stu-id="0b947-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="0b947-111">例子</span><span class="sxs-lookup"><span data-stu-id="0b947-111">EXAMPLES</span></span>

### <span data-ttu-id="0b947-112">範例 1：建立具有指定許可權的目錄、Umask、屬性和中繼資料</span><span class="sxs-lookup"><span data-stu-id="0b947-112">Example 1: Create a directory with specified permission, Umask, properties, and metadata</span></span>
```
PS C:\>New-AzDataLakeGen2Item -FileSystem "testfilesystem" -Path "dir1/dir2/" -Directory -Permission rwxrwxrwx -Umask ---rw---- -Property @{"CacheControl" = "READ"; "ContentDisposition" = "True"} -Metadata  @{"tag1" = "value1"; "tag2" = "value2" }

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir2            True                         2020-03-23 09:15:56Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="0b947-113">此命令會建立具有指定許可權、Umask、屬性和中繼資料的目錄</span><span class="sxs-lookup"><span data-stu-id="0b947-113">This command creates a directory with specified Permission, Umask, properties, and metadata</span></span>

### <span data-ttu-id="0b947-114">範例 2：建立 (上傳) 從本地來源檔案上傳資料湖檔案，而 Cmdlet 會以背景執行</span><span class="sxs-lookup"><span data-stu-id="0b947-114">Example 2: Create(upload) a data lake file from a local source file, and the cmdlet runs in background</span></span>
```
PS C:\> $task = New-AzDataLakeGen2Item  -FileSystem "testfilesystem" -Path "dir1/dir2/file1" -Source "c:\sourcefile.txt" -Force -asjob
PS C:\> $task | Wait-Job
PS C:\> $task.Output

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group                
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir2/file1      False        14400000        2020-03-23 09:19:13Z rw-r-----    $superuser           $superuser
```

<span data-ttu-id="0b947-115">此命令會建立 () 從本地來源檔案上傳資料湖檔案，而 Cmdlet 會以背景執行。</span><span class="sxs-lookup"><span data-stu-id="0b947-115">This command creates(upload) a data lake file from a local source file, and the cmdlet runs in background.</span></span>

## <span data-ttu-id="0b947-116">參數</span><span class="sxs-lookup"><span data-stu-id="0b947-116">PARAMETERS</span></span>

### <span data-ttu-id="0b947-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0b947-117">-AsJob</span></span>
<span data-ttu-id="0b947-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0b947-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0b947-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="0b947-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="0b947-120">同時同步處理工作的總數量。</span><span class="sxs-lookup"><span data-stu-id="0b947-120">The total amount of concurrent async tasks.</span></span> <span data-ttu-id="0b947-121">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="0b947-121">The default value is 10.</span></span>

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

### <span data-ttu-id="0b947-122">-內容</span><span class="sxs-lookup"><span data-stu-id="0b947-122">-Context</span></span>
<span data-ttu-id="0b947-123">Azure 儲存體內容物件</span><span class="sxs-lookup"><span data-stu-id="0b947-123">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b947-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b947-124">-DefaultProfile</span></span>
<span data-ttu-id="0b947-125">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0b947-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b947-126">-目錄</span><span class="sxs-lookup"><span data-stu-id="0b947-126">-Directory</span></span>
<span data-ttu-id="0b947-127">表示此新增專案是目錄，而非檔案。</span><span class="sxs-lookup"><span data-stu-id="0b947-127">Indicates that this new item is a directory and not a file.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Directory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b947-128">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="0b947-128">-FileSystem</span></span>
<span data-ttu-id="0b947-129">FileSystem 名稱</span><span class="sxs-lookup"><span data-stu-id="0b947-129">FileSystem name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b947-130">-強制</span><span class="sxs-lookup"><span data-stu-id="0b947-130">-Force</span></span>
<span data-ttu-id="0b947-131">如果傳遞，則建立新的專案時不需要任何提示</span><span class="sxs-lookup"><span data-stu-id="0b947-131">If passed then new item is created without any prompt</span></span>

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

### <span data-ttu-id="0b947-132">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="0b947-132">-Metadata</span></span>
<span data-ttu-id="0b947-133">指定所建立目錄或檔案的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="0b947-133">Specifies metadata for the created directory or file.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b947-134">-路徑</span><span class="sxs-lookup"><span data-stu-id="0b947-134">-Path</span></span>
<span data-ttu-id="0b947-135">指定檔案系統中應建立的路徑。</span><span class="sxs-lookup"><span data-stu-id="0b947-135">The path in the specified Filesystem that should be create.</span></span>
<span data-ttu-id="0b947-136">可以是檔案或目錄，格式為 'directory/file.txt' 或 'directory1/directory2/'</span><span class="sxs-lookup"><span data-stu-id="0b947-136">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b947-137">-許可權</span><span class="sxs-lookup"><span data-stu-id="0b947-137">-Permission</span></span>
<span data-ttu-id="0b947-138">設定檔案擁有者、檔案擁有者群組及其他的 POSIX 存取權限。</span><span class="sxs-lookup"><span data-stu-id="0b947-138">Sets POSIX access permissions for the file owner, the file owning group, and others.</span></span>
<span data-ttu-id="0b947-139">每個班級可能會獲得讀取、寫入或執行許可權。</span><span class="sxs-lookup"><span data-stu-id="0b947-139">Each class may be granted read, write, or execute permission.</span></span>
<span data-ttu-id="0b947-140">支援 (rwxrw-rw-) 符號。</span><span class="sxs-lookup"><span data-stu-id="0b947-140">Symbolic (rwxrw-rw-) is supported.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b947-141">-屬性</span><span class="sxs-lookup"><span data-stu-id="0b947-141">-Property</span></span>
<span data-ttu-id="0b947-142">指定所建立目錄或檔案的屬性。</span><span class="sxs-lookup"><span data-stu-id="0b947-142">Specifies properties for the created directory or file.</span></span> <span data-ttu-id="0b947-143">檔案支援的屬性為：CacheControl、ContentDisposition、ContentEncoding、ContentLanguage、ContentMD5、ContentType。</span><span class="sxs-lookup"><span data-stu-id="0b947-143">The supported properties for file are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>
<span data-ttu-id="0b947-144">目錄支援的屬性為：CacheControl、ContentDisposition、ContentEncoding、ContentLanguage。</span><span class="sxs-lookup"><span data-stu-id="0b947-144">The supported properties for directory are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b947-145">-來源</span><span class="sxs-lookup"><span data-stu-id="0b947-145">-Source</span></span>
<span data-ttu-id="0b947-146">指定要上傳到 Datalake Gen2 檔案的本地來源檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="0b947-146">Specify the local source file path which will be upload to a Datalake Gen2 file.</span></span>

```yaml
Type: System.String
Parameter Sets: File
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b947-147">-Umask</span><span class="sxs-lookup"><span data-stu-id="0b947-147">-Umask</span></span>
<span data-ttu-id="0b947-148">建立新專案且父目錄沒有預設 ACL 時，umask 會限制要建立之檔案或目錄的許可權。</span><span class="sxs-lookup"><span data-stu-id="0b947-148">When creating New Item and the parent directory does not have a default ACL, the umask restricts the permissions of the file or directory to be created.</span></span>
<span data-ttu-id="0b947-149">產生的許可權是由 p & ^u 提供，其中 p 是許可權，而您就是 umask。</span><span class="sxs-lookup"><span data-stu-id="0b947-149">The resulting permission is given by p & ^u, where p is the permission and u is the umask.</span></span>
<span data-ttu-id="0b947-150">支援 (rwxrw-rw-) 符號。</span><span class="sxs-lookup"><span data-stu-id="0b947-150">Symbolic (rwxrw-rw-) is supported.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b947-151">-確認</span><span class="sxs-lookup"><span data-stu-id="0b947-151">-Confirm</span></span>
<span data-ttu-id="0b947-152">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0b947-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b947-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b947-153">-WhatIf</span></span>
<span data-ttu-id="0b947-154">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0b947-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b947-155">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0b947-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b947-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b947-156">CommonParameters</span></span>
<span data-ttu-id="0b947-157">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0b947-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b947-158">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="0b947-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b947-159">輸入</span><span class="sxs-lookup"><span data-stu-id="0b947-159">INPUTS</span></span>

### <span data-ttu-id="0b947-160">System.String</span><span class="sxs-lookup"><span data-stu-id="0b947-160">System.String</span></span>

### <span data-ttu-id="0b947-161">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="0b947-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0b947-162">輸出</span><span class="sxs-lookup"><span data-stu-id="0b947-162">OUTPUTS</span></span>

### <span data-ttu-id="0b947-163">Microsoft.WindowsAzure.Commands.Common.storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="0b947-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="0b947-164">筆記</span><span class="sxs-lookup"><span data-stu-id="0b947-164">NOTES</span></span>

## <span data-ttu-id="0b947-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="0b947-165">RELATED LINKS</span></span>
