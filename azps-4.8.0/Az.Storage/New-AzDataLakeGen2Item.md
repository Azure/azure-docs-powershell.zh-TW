---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzDataLakeGen2Item.md
ms.openlocfilehash: 26f3dbc3462688458647e2e9676916063ffa3586
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126721"
---
# <span data-ttu-id="42ee8-101">New-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="42ee8-101">New-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="42ee8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="42ee8-102">SYNOPSIS</span></span>
<span data-ttu-id="42ee8-103">在檔案系統中建立檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="42ee8-103">Create a file or directory in a filesystem.</span></span>

## <span data-ttu-id="42ee8-104">句法</span><span class="sxs-lookup"><span data-stu-id="42ee8-104">SYNTAX</span></span>

### <span data-ttu-id="42ee8-105">檔案 (預設) </span><span class="sxs-lookup"><span data-stu-id="42ee8-105">File (Default)</span></span>
```
New-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> -Source <String> [-Umask <String>]
 [-Permission <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42ee8-106">空目錄</span><span class="sxs-lookup"><span data-stu-id="42ee8-106">Directory</span></span>
```
New-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> [-Directory] [-Umask <String>]
 [-Permission <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42ee8-107">說明</span><span class="sxs-lookup"><span data-stu-id="42ee8-107">DESCRIPTION</span></span>
<span data-ttu-id="42ee8-108">**新的-AzDataLakeGen2Item** Cmdlet 會在 Azure 儲存空間帳戶的 Filesystem 中建立檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="42ee8-108">The **New-AzDataLakeGen2Item** cmdlet creates a file or directory in a Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="42ee8-109">這個 Cmdlet 只有在已針對儲存空間帳戶啟用階層命名空間時才適用。</span><span class="sxs-lookup"><span data-stu-id="42ee8-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="42ee8-110">此類型的帳戶可使用「-EnableHierarchicalNamespace $true」執行「新-AzStorageAccount」 Cmdlet 來建立。</span><span class="sxs-lookup"><span data-stu-id="42ee8-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="42ee8-111">示例</span><span class="sxs-lookup"><span data-stu-id="42ee8-111">EXAMPLES</span></span>

### <span data-ttu-id="42ee8-112">範例1：使用指定的許可權、Umask、屬性及中繼資料建立目錄</span><span class="sxs-lookup"><span data-stu-id="42ee8-112">Example 1: Create a directory with specified permission, Umask, properties, and metadata</span></span>
```
PS C:\>New-AzDataLakeGen2Item -FileSystem "testfilesystem" -Path "dir1/dir2/" -Directory -Permission rwxrwxrwx -Umask ---rw---- -Property @{"CacheControl" = "READ"; "ContentDisposition" = "True"} -Metadata  @{"tag1" = "value1"; "tag2" = "value2" }

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir2            True                         2020-03-23 09:15:56Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="42ee8-113">這個命令會建立具有指定許可權、Umask、屬性及中繼資料的目錄</span><span class="sxs-lookup"><span data-stu-id="42ee8-113">This command creates a directory with specified Permission, Umask, properties, and metadata</span></span>

### <span data-ttu-id="42ee8-114">範例2：建立 (從本機來源檔案) 資料 lake 檔案，而 Cmdlet 在背景執行</span><span class="sxs-lookup"><span data-stu-id="42ee8-114">Example 2: Create(upload) a data lake file from a local source file, and the cmdlet runs in background</span></span>
```
PS C:\> $task = New-AzDataLakeGen2Item  -FileSystem "testfilesystem" -Path "dir1/dir2/file1" -Source "c:\sourcefile.txt" -Force -asjob
PS C:\> $task | Wait-Job
PS C:\> $task.Output

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group                
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir2/file1      False        14400000        2020-03-23 09:19:13Z rw-r-----    $superuser           $superuser
```

<span data-ttu-id="42ee8-115">這個命令會建立 (從本機來源檔案) 資料 lake 檔案的上傳，而 Cmdlet 則會在背景執行。</span><span class="sxs-lookup"><span data-stu-id="42ee8-115">This command creates(upload) a data lake file from a local source file, and the cmdlet runs in background.</span></span>

## <span data-ttu-id="42ee8-116">參數</span><span class="sxs-lookup"><span data-stu-id="42ee8-116">PARAMETERS</span></span>

### <span data-ttu-id="42ee8-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="42ee8-117">-AsJob</span></span>
<span data-ttu-id="42ee8-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="42ee8-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="42ee8-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="42ee8-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="42ee8-120">並行非同步工作的總數量。</span><span class="sxs-lookup"><span data-stu-id="42ee8-120">The total amount of concurrent async tasks.</span></span> <span data-ttu-id="42ee8-121">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="42ee8-121">The default value is 10.</span></span>

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

### <span data-ttu-id="42ee8-122">-內容</span><span class="sxs-lookup"><span data-stu-id="42ee8-122">-Context</span></span>
<span data-ttu-id="42ee8-123">Azure 儲存區內容物件</span><span class="sxs-lookup"><span data-stu-id="42ee8-123">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="42ee8-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42ee8-124">-DefaultProfile</span></span>
<span data-ttu-id="42ee8-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="42ee8-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42ee8-126">-Directory</span><span class="sxs-lookup"><span data-stu-id="42ee8-126">-Directory</span></span>
<span data-ttu-id="42ee8-127">表示此新專案是目錄，而不是檔案。</span><span class="sxs-lookup"><span data-stu-id="42ee8-127">Indicates that this new item is a directory and not a file.</span></span>

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

### <span data-ttu-id="42ee8-128">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="42ee8-128">-FileSystem</span></span>
<span data-ttu-id="42ee8-129">FileSystem 名稱</span><span class="sxs-lookup"><span data-stu-id="42ee8-129">FileSystem name</span></span>

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

### <span data-ttu-id="42ee8-130">-Force</span><span class="sxs-lookup"><span data-stu-id="42ee8-130">-Force</span></span>
<span data-ttu-id="42ee8-131">如果傳遞之後，就會建立新專案而不會出現任何提示</span><span class="sxs-lookup"><span data-stu-id="42ee8-131">If passed then new item is created without any prompt</span></span>

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

### <span data-ttu-id="42ee8-132">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="42ee8-132">-Metadata</span></span>
<span data-ttu-id="42ee8-133">指定已建立的目錄或檔案的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="42ee8-133">Specifies metadata for the created directory or file.</span></span>

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

### <span data-ttu-id="42ee8-134">-Path</span><span class="sxs-lookup"><span data-stu-id="42ee8-134">-Path</span></span>
<span data-ttu-id="42ee8-135">要建立的指定 Filesystem 中的路徑。</span><span class="sxs-lookup"><span data-stu-id="42ee8-135">The path in the specified Filesystem that should be create.</span></span>
<span data-ttu-id="42ee8-136">可以是 "directory/file.txt" 格式或 "directory1/directory2/" 格式的檔案或目錄</span><span class="sxs-lookup"><span data-stu-id="42ee8-136">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

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

### <span data-ttu-id="42ee8-137">-許可權</span><span class="sxs-lookup"><span data-stu-id="42ee8-137">-Permission</span></span>
<span data-ttu-id="42ee8-138">為檔案擁有者、擁有的群組及其他人設定 POSIX 存取許可權。</span><span class="sxs-lookup"><span data-stu-id="42ee8-138">Sets POSIX access permissions for the file owner, the file owning group, and others.</span></span>
<span data-ttu-id="42ee8-139">每個類別都可能被授與 [讀取]、[寫入] 或 [執行] 許可權。</span><span class="sxs-lookup"><span data-stu-id="42ee8-139">Each class may be granted read, write, or execute permission.</span></span>
<span data-ttu-id="42ee8-140">支援符號 (rwxrw-cd-rw-) 。</span><span class="sxs-lookup"><span data-stu-id="42ee8-140">Symbolic (rwxrw-rw-) is supported.</span></span>

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

### <span data-ttu-id="42ee8-141">-屬性</span><span class="sxs-lookup"><span data-stu-id="42ee8-141">-Property</span></span>
<span data-ttu-id="42ee8-142">指定已建立的目錄或檔案的屬性。</span><span class="sxs-lookup"><span data-stu-id="42ee8-142">Specifies properties for the created directory or file.</span></span> <span data-ttu-id="42ee8-143">支援的檔案屬性有： CacheControl、ContentDisposition、ContentEncoding、ContentLanguage、ContentMD5、ContentType。</span><span class="sxs-lookup"><span data-stu-id="42ee8-143">The supported properties for file are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>
<span data-ttu-id="42ee8-144">目錄支援的屬性為： CacheControl、ContentDisposition、ContentEncoding、ContentLanguage。</span><span class="sxs-lookup"><span data-stu-id="42ee8-144">The supported properties for directory are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span></span>

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

### <span data-ttu-id="42ee8-145">-來源</span><span class="sxs-lookup"><span data-stu-id="42ee8-145">-Source</span></span>
<span data-ttu-id="42ee8-146">指定將上傳到 Datalake Gen2 檔案的本機來源檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="42ee8-146">Specify the local source file path which will be upload to a Datalake Gen2 file.</span></span>

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

### <span data-ttu-id="42ee8-147">-Umask</span><span class="sxs-lookup"><span data-stu-id="42ee8-147">-Umask</span></span>
<span data-ttu-id="42ee8-148">當您建立新專案，而上層目錄沒有預設的 ACL 時，umask 會限制要建立的檔案或目錄的許可權。</span><span class="sxs-lookup"><span data-stu-id="42ee8-148">When creating New Item and the parent directory does not have a default ACL, the umask restricts the permissions of the file or directory to be created.</span></span>
<span data-ttu-id="42ee8-149">產生的許可權是由 p & ^ u 提供，其中 p 是許可權，而您是 umask。</span><span class="sxs-lookup"><span data-stu-id="42ee8-149">The resulting permission is given by p & ^u, where p is the permission and u is the umask.</span></span>
<span data-ttu-id="42ee8-150">支援符號 (rwxrw-cd-rw-) 。</span><span class="sxs-lookup"><span data-stu-id="42ee8-150">Symbolic (rwxrw-rw-) is supported.</span></span>

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

### <span data-ttu-id="42ee8-151">-確認</span><span class="sxs-lookup"><span data-stu-id="42ee8-151">-Confirm</span></span>
<span data-ttu-id="42ee8-152">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="42ee8-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42ee8-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42ee8-153">-WhatIf</span></span>
<span data-ttu-id="42ee8-154">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="42ee8-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42ee8-155">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="42ee8-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42ee8-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42ee8-156">CommonParameters</span></span>
<span data-ttu-id="42ee8-157">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="42ee8-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42ee8-158">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="42ee8-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42ee8-159">輸入</span><span class="sxs-lookup"><span data-stu-id="42ee8-159">INPUTS</span></span>

### <span data-ttu-id="42ee8-160">System.object</span><span class="sxs-lookup"><span data-stu-id="42ee8-160">System.String</span></span>

### <span data-ttu-id="42ee8-161">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="42ee8-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="42ee8-162">輸出</span><span class="sxs-lookup"><span data-stu-id="42ee8-162">OUTPUTS</span></span>

### <span data-ttu-id="42ee8-163">AzureDataLakeGen2Item WindowsAzure. ResourceModel。</span><span class="sxs-lookup"><span data-stu-id="42ee8-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="42ee8-164">筆記</span><span class="sxs-lookup"><span data-stu-id="42ee8-164">NOTES</span></span>

## <span data-ttu-id="42ee8-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="42ee8-165">RELATED LINKS</span></span>