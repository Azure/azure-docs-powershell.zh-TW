---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azdatalakegen2childitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ChildItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ChildItem.md
ms.openlocfilehash: 9160eabf2492969ad7fa3916791854abd4ef6c44
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958245"
---
# <span data-ttu-id="1c955-101">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="1c955-101">Get-AzDataLakeGen2ChildItem</span></span>

## <span data-ttu-id="1c955-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1c955-102">SYNOPSIS</span></span>
<span data-ttu-id="1c955-103">列出目錄或 filesystem 根目錄中的子 directorys 和檔案。</span><span class="sxs-lookup"><span data-stu-id="1c955-103">Lists sub directorys and files from a directory or filesystem root.</span></span>

## <span data-ttu-id="1c955-104">句法</span><span class="sxs-lookup"><span data-stu-id="1c955-104">SYNTAX</span></span>

```
Get-AzDataLakeGen2ChildItem [-FileSystem] <String> [[-Path] <String>] [-FetchProperty] [-Recurse]
 [-MaxCount <Int32>] [-ContinuationToken <String>] [-AsJob] [-OutputUserPrincipalName]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c955-105">說明</span><span class="sxs-lookup"><span data-stu-id="1c955-105">DESCRIPTION</span></span>
<span data-ttu-id="1c955-106">**AzDataLakeGen2ChildItem** Cmdlet 會在 Azure 儲存空間帳戶中列出目錄或檔案系統中的子 directorys 和檔案。</span><span class="sxs-lookup"><span data-stu-id="1c955-106">The **Get-AzDataLakeGen2ChildItem** cmdlet lists sub directorys and files in a directory or Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="1c955-107">這個 Cmdlet 只有在已針對儲存空間帳戶啟用階層命名空間時才適用。</span><span class="sxs-lookup"><span data-stu-id="1c955-107">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="1c955-108">此類型的帳戶可使用「-EnableHierarchicalNamespace $true」執行「新-AzStorageAccount」 Cmdlet 來建立。</span><span class="sxs-lookup"><span data-stu-id="1c955-108">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="1c955-109">示例</span><span class="sxs-lookup"><span data-stu-id="1c955-109">EXAMPLES</span></span>

### <span data-ttu-id="1c955-110">範例1：從 Filesystem 列出直接子專案</span><span class="sxs-lookup"><span data-stu-id="1c955-110">Example 1: List the direct sub items from a Filesystem</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" 

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1                 True                         2020-03-13 13:07:34Z rwxr-x---    $superuser           $superuser          
dir2                 True                         2020-03-23 09:28:36Z rwxr-x---    $superuser           $superuser
```

<span data-ttu-id="1c955-111">這個命令會從 Filesystem 中列出直接子專案</span><span class="sxs-lookup"><span data-stu-id="1c955-111">This command lists the direct sub items from a Filesystem</span></span>

### <span data-ttu-id="1c955-112">範例2：以遞迴方式從目錄中清單，並提取屬性/ACL</span><span class="sxs-lookup"><span data-stu-id="1c955-112">Example 2: List recursively from a directory, and fetch Properties/ACL</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" -Path "dir1/" -Recurse -FetchProperty

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir3            True                         2020-03-23 09:34:31Z rwx---rwx    $superuser           $superuser          
dir1/file1           False        1024            2020-03-23 09:29:18Z rwx---rwx    $superuser           $superuser           
dir1/testfile_1K_0   False        1024            2020-03-23 09:29:21Z rw-r-----    $superuser           $superuser
```

<span data-ttu-id="1c955-113">這個命令會從 Filesystem 中列出直接子專案</span><span class="sxs-lookup"><span data-stu-id="1c955-113">This command lists the direct sub items from a Filesystem</span></span>

### <span data-ttu-id="1c955-114">範例3：以多個批次以遞迴方式列出 Filesystem 中的專案</span><span class="sxs-lookup"><span data-stu-id="1c955-114">Example 3: List items recursively from a Filesystem in multiple batches</span></span>
```
PS C:\> $MaxReturn = 10000
PS C:\> $FileSystemName = "filesystem1"
PS C:\> $Total = 0
PS C:\> $Token = $Null
PS C:\> do
 {
     $items = Get-AzDataLakeGen2ChildItem -FileSystem $FileSystemName -Recurse -MaxCount $MaxReturn  -ContinuationToken $Token
     $Total += $items.Count
     if($items.Length -le 0) { Break;}
     $Token = $items[$items.Count -1].ContinuationToken;
 }
 While ($Token -ne $Null)
PS C:\> Echo "Total $Total items in Filesystem $FileSystemName"
```

<span data-ttu-id="1c955-115">這個範例使用 *MaxCount* 和 *ContinuationToken* 參數，以多個批次從 Filesystem 中以遞迴方式列出專案。</span><span class="sxs-lookup"><span data-stu-id="1c955-115">This example uses the *MaxCount* and *ContinuationToken* parameters to list items recursively from a Filesystem in multiple batches.</span></span>
<span data-ttu-id="1c955-116">前四個命令會將值指派給要在範例中使用的變數。</span><span class="sxs-lookup"><span data-stu-id="1c955-116">The first four commands assign values to variables to use in the example.</span></span>
<span data-ttu-id="1c955-117">第五個命令指定一個 **Do** 語句，該語句使用 **AzDataLakeGen2ChildItem** Cmdlet 來列出專案。</span><span class="sxs-lookup"><span data-stu-id="1c955-117">The fifth command specifies a **Do-While** statement that uses the **Get-AzDataLakeGen2ChildItem** cmdlet to list items.</span></span>
<span data-ttu-id="1c955-118">該語句包含儲存在 $Token 變數中的延續標記。</span><span class="sxs-lookup"><span data-stu-id="1c955-118">The statement includes the continuation token stored in the $Token variable.</span></span>
<span data-ttu-id="1c955-119">在迴圈執行時 $Token 變更值。</span><span class="sxs-lookup"><span data-stu-id="1c955-119">$Token changes value as the loop runs.</span></span>
<span data-ttu-id="1c955-120">最後一個命令會使用 **Echo** 命令來顯示合計。</span><span class="sxs-lookup"><span data-stu-id="1c955-120">The final command uses the **Echo** command to display the total.</span></span>

## <span data-ttu-id="1c955-121">參數</span><span class="sxs-lookup"><span data-stu-id="1c955-121">PARAMETERS</span></span>

### <span data-ttu-id="1c955-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1c955-122">-AsJob</span></span>
<span data-ttu-id="1c955-123">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1c955-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1c955-124">-內容</span><span class="sxs-lookup"><span data-stu-id="1c955-124">-Context</span></span>
<span data-ttu-id="1c955-125">Azure 儲存區內容物件</span><span class="sxs-lookup"><span data-stu-id="1c955-125">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="1c955-126">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="1c955-126">-ContinuationToken</span></span>
<span data-ttu-id="1c955-127">延續標記。</span><span class="sxs-lookup"><span data-stu-id="1c955-127">Continuation Token.</span></span>

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

### <span data-ttu-id="1c955-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c955-128">-DefaultProfile</span></span>
<span data-ttu-id="1c955-129">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1c955-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c955-130">-FetchProperty</span><span class="sxs-lookup"><span data-stu-id="1c955-130">-FetchProperty</span></span>
<span data-ttu-id="1c955-131">提取 datalake 專案屬性和 ACL。</span><span class="sxs-lookup"><span data-stu-id="1c955-131">Fetch the datalake item properties and ACL.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: FetchPermission

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c955-132">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="1c955-132">-FileSystem</span></span>
<span data-ttu-id="1c955-133">FileSystem 名稱</span><span class="sxs-lookup"><span data-stu-id="1c955-133">FileSystem name</span></span>

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

### <span data-ttu-id="1c955-134">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="1c955-134">-MaxCount</span></span>
<span data-ttu-id="1c955-135">可傳回的 blob 數上限。</span><span class="sxs-lookup"><span data-stu-id="1c955-135">The max count of the blobs that can return.</span></span>

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

### <span data-ttu-id="1c955-136">-OutputUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="1c955-136">-OutputUserPrincipalName</span></span>
<span data-ttu-id="1c955-137">如果 speicify 此參數，在每個清單專案的擁有者和群組欄位中傳回的使用者身分識別值，就會從 Azure Active Directory 物件識別碼轉換為使用者主要名稱。</span><span class="sxs-lookup"><span data-stu-id="1c955-137">If speicify this parameter, the user identity values returned in the owner and group fields of each list entry will be transformed from Azure Active Directory Object IDs to User Principal Names.</span></span> <span data-ttu-id="1c955-138">如果未 speicify 此參數，值將會以 Azure Active Directory 物件識別碼的形式傳回。</span><span class="sxs-lookup"><span data-stu-id="1c955-138">If not speicify this parameter, the values will be returned as Azure Active Directory Object IDs.</span></span> <span data-ttu-id="1c955-139">請注意，群組和應用程式物件識別碼不會翻譯，因為它們沒有唯一的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="1c955-139">Note that group and application Object IDs are not translated because they do not have unique friendly names.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: UserPrincipalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c955-140">-Path</span><span class="sxs-lookup"><span data-stu-id="1c955-140">-Path</span></span>
<span data-ttu-id="1c955-141">要在指定的 Filesystem 中檢索的路徑。</span><span class="sxs-lookup"><span data-stu-id="1c955-141">The path in the specified Filesystem that should be retrieved.</span></span>
<span data-ttu-id="1c955-142">必須是 [directory1/directory2/"格式的目錄。</span><span class="sxs-lookup"><span data-stu-id="1c955-142">Should be a directory, in the format 'directory1/directory2/'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c955-143">-遞迴</span><span class="sxs-lookup"><span data-stu-id="1c955-143">-Recurse</span></span>
<span data-ttu-id="1c955-144">指示是否會以遞迴方式取得子專案。</span><span class="sxs-lookup"><span data-stu-id="1c955-144">Indicates if will recursively get the Child Item.</span></span>
<span data-ttu-id="1c955-145">預設值為 false。</span><span class="sxs-lookup"><span data-stu-id="1c955-145">The default is false.</span></span>

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

### <span data-ttu-id="1c955-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c955-146">CommonParameters</span></span>
<span data-ttu-id="1c955-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1c955-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c955-148">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1c955-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c955-149">輸入</span><span class="sxs-lookup"><span data-stu-id="1c955-149">INPUTS</span></span>

### <span data-ttu-id="1c955-150">System.object</span><span class="sxs-lookup"><span data-stu-id="1c955-150">System.String</span></span>

### <span data-ttu-id="1c955-151">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="1c955-151">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="1c955-152">輸出</span><span class="sxs-lookup"><span data-stu-id="1c955-152">OUTPUTS</span></span>

### <span data-ttu-id="1c955-153">AzureDataLakeGen2Item WindowsAzure. ResourceModel。</span><span class="sxs-lookup"><span data-stu-id="1c955-153">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="1c955-154">筆記</span><span class="sxs-lookup"><span data-stu-id="1c955-154">NOTES</span></span>

## <span data-ttu-id="1c955-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="1c955-155">RELATED LINKS</span></span>
