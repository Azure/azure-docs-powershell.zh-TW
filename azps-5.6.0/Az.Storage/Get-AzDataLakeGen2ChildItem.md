---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azdatalakegen2childitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ChildItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ChildItem.md
ms.openlocfilehash: 3505d9b07e1d56936a002b45bfeee7929823f4be
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910354"
---
# <span data-ttu-id="44101-101">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="44101-101">Get-AzDataLakeGen2ChildItem</span></span>

## <span data-ttu-id="44101-102">簡介</span><span class="sxs-lookup"><span data-stu-id="44101-102">SYNOPSIS</span></span>
<span data-ttu-id="44101-103">列出目錄或檔案系統根目錄中的子目錄和檔案。</span><span class="sxs-lookup"><span data-stu-id="44101-103">Lists sub directorys and files from a directory or filesystem root.</span></span>

## <span data-ttu-id="44101-104">語法</span><span class="sxs-lookup"><span data-stu-id="44101-104">SYNTAX</span></span>

```
Get-AzDataLakeGen2ChildItem [-FileSystem] <String> [[-Path] <String>] [-FetchProperty] [-Recurse]
 [-MaxCount <Int32>] [-ContinuationToken <String>] [-AsJob] [-OutputUserPrincipalName]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44101-105">描述</span><span class="sxs-lookup"><span data-stu-id="44101-105">DESCRIPTION</span></span>
<span data-ttu-id="44101-106">**Get-AzDataLakeGen2ChildItem** Cmdlet 會列出 Azure 儲存帳戶中目錄或 Filesystem 中的子目錄和檔案。</span><span class="sxs-lookup"><span data-stu-id="44101-106">The **Get-AzDataLakeGen2ChildItem** cmdlet lists sub directorys and files in a directory or Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="44101-107">只有在儲存空間帳戶已啟用階層式命名空間時，此 Cmdlet 才能運作。</span><span class="sxs-lookup"><span data-stu-id="44101-107">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="44101-108">您可以使用"-EnableHierarchicalNamespace $true"執行 「New-AzStorageAccount」Cmdlet 來建立這類帳戶。</span><span class="sxs-lookup"><span data-stu-id="44101-108">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="44101-109">例子</span><span class="sxs-lookup"><span data-stu-id="44101-109">EXAMPLES</span></span>

### <span data-ttu-id="44101-110">範例 1：列出檔案系統的直接子專案</span><span class="sxs-lookup"><span data-stu-id="44101-110">Example 1: List the direct sub items from a Filesystem</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" 

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1                 True                         2020-03-13 13:07:34Z rwxr-x---    $superuser           $superuser          
dir2                 True                         2020-03-23 09:28:36Z rwxr-x---    $superuser           $superuser
```

<span data-ttu-id="44101-111">此命令會列出檔案系統的直接子專案</span><span class="sxs-lookup"><span data-stu-id="44101-111">This command lists the direct sub items from a Filesystem</span></span>

### <span data-ttu-id="44101-112">範例 2：從目錄遞迴清單，然後抓取 Properties/ACL</span><span class="sxs-lookup"><span data-stu-id="44101-112">Example 2: List recursively from a directory, and fetch Properties/ACL</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" -Path "dir1/" -Recurse -FetchProperty

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir3            True                         2020-03-23 09:34:31Z rwx---rwx    $superuser           $superuser          
dir1/file1           False        1024            2020-03-23 09:29:18Z rwx---rwx    $superuser           $superuser           
dir1/testfile_1K_0   False        1024            2020-03-23 09:29:21Z rw-r-----    $superuser           $superuser
```

<span data-ttu-id="44101-113">此命令會列出檔案系統的直接子專案</span><span class="sxs-lookup"><span data-stu-id="44101-113">This command lists the direct sub items from a Filesystem</span></span>

### <span data-ttu-id="44101-114">範例 3：在多個批次中以遞迴的檔案格式列出專案</span><span class="sxs-lookup"><span data-stu-id="44101-114">Example 3: List items recursively from a Filesystem in multiple batches</span></span>
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

<span data-ttu-id="44101-115">此範例使用 *MaxCount* 和 *ContinuationToken* 參數，以遞迴的方法列出多個批次中來自檔案系統的專案。</span><span class="sxs-lookup"><span data-stu-id="44101-115">This example uses the *MaxCount* and *ContinuationToken* parameters to list items recursively from a Filesystem in multiple batches.</span></span>
<span data-ttu-id="44101-116">前四個命令會指派值給範例中要使用的變數。</span><span class="sxs-lookup"><span data-stu-id="44101-116">The first four commands assign values to variables to use in the example.</span></span>
<span data-ttu-id="44101-117">第五個命令會指定使用 **Get-AzDataLakeGen2ChildItem** Cmdlet 來列出專案的 **Do-While** 語句。</span><span class="sxs-lookup"><span data-stu-id="44101-117">The fifth command specifies a **Do-While** statement that uses the **Get-AzDataLakeGen2ChildItem** cmdlet to list items.</span></span>
<span data-ttu-id="44101-118">語句包含儲存在 $Token 變數中的延續權杖。</span><span class="sxs-lookup"><span data-stu-id="44101-118">The statement includes the continuation token stored in the $Token variable.</span></span>
<span data-ttu-id="44101-119">$Token迴圈執行時變更值。</span><span class="sxs-lookup"><span data-stu-id="44101-119">$Token changes value as the loop runs.</span></span>
<span data-ttu-id="44101-120">最後一個命令會使用 **Echo** 命令來顯示總計。</span><span class="sxs-lookup"><span data-stu-id="44101-120">The final command uses the **Echo** command to display the total.</span></span>

## <span data-ttu-id="44101-121">參數</span><span class="sxs-lookup"><span data-stu-id="44101-121">PARAMETERS</span></span>

### <span data-ttu-id="44101-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="44101-122">-AsJob</span></span>
<span data-ttu-id="44101-123">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="44101-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="44101-124">-內容</span><span class="sxs-lookup"><span data-stu-id="44101-124">-Context</span></span>
<span data-ttu-id="44101-125">Azure 儲存體內容物件</span><span class="sxs-lookup"><span data-stu-id="44101-125">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="44101-126">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="44101-126">-ContinuationToken</span></span>
<span data-ttu-id="44101-127">延續權杖。</span><span class="sxs-lookup"><span data-stu-id="44101-127">Continuation Token.</span></span>

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

### <span data-ttu-id="44101-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44101-128">-DefaultProfile</span></span>
<span data-ttu-id="44101-129">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="44101-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44101-130">-FetchProperty</span><span class="sxs-lookup"><span data-stu-id="44101-130">-FetchProperty</span></span>
<span data-ttu-id="44101-131">抓取資料餅專案屬性和 ACL。</span><span class="sxs-lookup"><span data-stu-id="44101-131">Fetch the datalake item properties and ACL.</span></span>

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

### <span data-ttu-id="44101-132">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="44101-132">-FileSystem</span></span>
<span data-ttu-id="44101-133">FileSystem 名稱</span><span class="sxs-lookup"><span data-stu-id="44101-133">FileSystem name</span></span>

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

### <span data-ttu-id="44101-134">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="44101-134">-MaxCount</span></span>
<span data-ttu-id="44101-135">可返回之 Blob 的最大值。</span><span class="sxs-lookup"><span data-stu-id="44101-135">The max count of the blobs that can return.</span></span>

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

### <span data-ttu-id="44101-136">-OutputUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="44101-136">-OutputUserPrincipalName</span></span>
<span data-ttu-id="44101-137">如果將這個參數化，則每個清單專案之擁有者和群組欄位中所返回的使用者身分識別值，將會從 Azure Active Directory 物件 ID 轉換為使用者主體名稱。</span><span class="sxs-lookup"><span data-stu-id="44101-137">If speicify this parameter, the user identity values returned in the owner and group fields of each list entry will be transformed from Azure Active Directory Object IDs to User Principal Names.</span></span> <span data-ttu-id="44101-138">如果未將參數化，值會以 Azure Active Directory 物件 IDS 退回。</span><span class="sxs-lookup"><span data-stu-id="44101-138">If not speicify this parameter, the values will be returned as Azure Active Directory Object IDs.</span></span> <span data-ttu-id="44101-139">請注意，群組和應用程式物件標識不會翻譯，因為它們沒有唯一的好記名稱。</span><span class="sxs-lookup"><span data-stu-id="44101-139">Note that group and application Object IDs are not translated because they do not have unique friendly names.</span></span>

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

### <span data-ttu-id="44101-140">-路徑</span><span class="sxs-lookup"><span data-stu-id="44101-140">-Path</span></span>
<span data-ttu-id="44101-141">指定檔案系統中應該要取取的路徑。</span><span class="sxs-lookup"><span data-stu-id="44101-141">The path in the specified Filesystem that should be retrieved.</span></span>
<span data-ttu-id="44101-142">應該是目錄，格式為 'directory1/directory2/'。</span><span class="sxs-lookup"><span data-stu-id="44101-142">Should be a directory, in the format 'directory1/directory2/'.</span></span>

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

### <span data-ttu-id="44101-143">-遞迴</span><span class="sxs-lookup"><span data-stu-id="44101-143">-Recurse</span></span>
<span data-ttu-id="44101-144">指出是否將遞迴取得子專案。</span><span class="sxs-lookup"><span data-stu-id="44101-144">Indicates if will recursively get the Child Item.</span></span>
<span data-ttu-id="44101-145">預設值為 False。</span><span class="sxs-lookup"><span data-stu-id="44101-145">The default is false.</span></span>

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

### <span data-ttu-id="44101-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44101-146">CommonParameters</span></span>
<span data-ttu-id="44101-147">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="44101-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44101-148">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="44101-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44101-149">輸入</span><span class="sxs-lookup"><span data-stu-id="44101-149">INPUTS</span></span>

### <span data-ttu-id="44101-150">System.String</span><span class="sxs-lookup"><span data-stu-id="44101-150">System.String</span></span>

### <span data-ttu-id="44101-151">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="44101-151">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="44101-152">輸出</span><span class="sxs-lookup"><span data-stu-id="44101-152">OUTPUTS</span></span>

### <span data-ttu-id="44101-153">Microsoft.WindowsAzure.Commands.Common.storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="44101-153">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="44101-154">筆記</span><span class="sxs-lookup"><span data-stu-id="44101-154">NOTES</span></span>

## <span data-ttu-id="44101-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="44101-155">RELATED LINKS</span></span>
