---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2Item.md
ms.openlocfilehash: 38e350f8dd4c6e8f37d75c8708387d5980e5cb84
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910357"
---
# <span data-ttu-id="fb589-101">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="fb589-101">Get-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="fb589-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fb589-102">SYNOPSIS</span></span>
<span data-ttu-id="fb589-103">在檔案系統中，獲得檔案或目錄的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="fb589-103">Gets the details of a file or directory in a filesystem.</span></span>

## <span data-ttu-id="fb589-104">語法</span><span class="sxs-lookup"><span data-stu-id="fb589-104">SYNTAX</span></span>

```
Get-AzDataLakeGen2Item [-FileSystem] <String> [-Path <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb589-105">描述</span><span class="sxs-lookup"><span data-stu-id="fb589-105">DESCRIPTION</span></span>
<span data-ttu-id="fb589-106">**Get-AzDataLakeGen2Item** Cmdlet 會取得 Azure 儲存帳戶中檔案系統中檔案或目錄的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="fb589-106">The **Get-AzDataLakeGen2Item** cmdlet gets the details of a file or directory in a Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="fb589-107">只有在儲存空間帳戶已啟用階層式命名空間時，此 Cmdlet 才能運作。</span><span class="sxs-lookup"><span data-stu-id="fb589-107">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="fb589-108">您可以使用"-EnableHierarchicalNamespace $true"執行 「New-AzStorageAccount」Cmdlet 來建立這類帳戶。</span><span class="sxs-lookup"><span data-stu-id="fb589-108">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="fb589-109">例子</span><span class="sxs-lookup"><span data-stu-id="fb589-109">EXAMPLES</span></span>

### <span data-ttu-id="fb589-110">範例 1：從 Filesystem 取得目錄，然後顯示詳細資料</span><span class="sxs-lookup"><span data-stu-id="fb589-110">Example 1: Get a directory from a Filesystem, and show the details</span></span>
```
PS C:\> $dir1 = Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/"
PS C:\> $dir1

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1                 True                         2020-03-23 09:15:56Z rwx---rwx    $superuser           $superuser     
 
PS C:\WINDOWS\system32> $dir1.ACL

DefaultScope AccessControlType EntityId Permissions
------------ ----------------- -------- -----------
False        User                       rwx        
False        Group                      ---        
False        Other                      rwx      

PS C:\WINDOWS\system32> $dir1.Permissions

Owner        : Execute, Write, Read
Group        : None
Other        : Execute, Write, Read
StickyBit    : False
ExtendedAcls : False

PS C:\WINDOWS\system32> $dir1.Properties.Metadata

Key          Value 
---          ----- 
hdi_isfolder true  
tag1         value1
tag2         value2

PS C:\WINDOWS\system32> $dir1.Properties

LastModified          : 3/23/2020 9:15:56 AM +00:00
CreatedOn             : 3/23/2020 9:15:56 AM +00:00
Metadata              : {[hdi_isfolder, true], [tag1, value1], [tag2, value2]}
CopyCompletedOn       : 1/1/0001 12:00:00 AM +00:00
CopyStatusDescription : 
CopyId                : 
CopyProgress          : 
CopySource            : 
CopyStatus            : Pending
IsIncrementalCopy     : False
LeaseDuration         : Infinite
LeaseState            : Available
LeaseStatus           : Unlocked
ContentLength         : 0
ContentType           : application/octet-stream
ETag                  : "0x8D7CF0ACBA35FA8"
ContentHash           : 
ContentEncoding       : UDF12
ContentDisposition    : 
ContentLanguage       : 
CacheControl          : READ
AcceptRanges          : bytes
IsServerEncrypted     : True
EncryptionKeySha256   : 
AccessTier            : Cool
ArchiveStatus         : 
AccessTierChangedOn   : 1/1/0001 12:00:00 AM +00:00
```

<span data-ttu-id="fb589-111">此命令會從檔案系統中獲得目錄，並顯示詳細資料。</span><span class="sxs-lookup"><span data-stu-id="fb589-111">This command gets a directory from a Filesystem, and show the details.</span></span>

### <span data-ttu-id="fb589-112">範例 2：從檔案系統取得檔案</span><span class="sxs-lookup"><span data-stu-id="fb589-112">Example 2: Get a file from a Filesystem</span></span>
```
PS C:\> Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1"

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:20:37Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="fb589-113">此命令會從檔案系統中獲得檔案詳細資料。</span><span class="sxs-lookup"><span data-stu-id="fb589-113">This command gets the details of a file from a Filesystem.</span></span> 

## <span data-ttu-id="fb589-114">參數</span><span class="sxs-lookup"><span data-stu-id="fb589-114">PARAMETERS</span></span>

### <span data-ttu-id="fb589-115">-內容</span><span class="sxs-lookup"><span data-stu-id="fb589-115">-Context</span></span>
<span data-ttu-id="fb589-116">Azure 儲存體內容物件</span><span class="sxs-lookup"><span data-stu-id="fb589-116">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="fb589-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb589-117">-DefaultProfile</span></span>
<span data-ttu-id="fb589-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="fb589-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb589-119">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="fb589-119">-FileSystem</span></span>
<span data-ttu-id="fb589-120">FileSystem 名稱</span><span class="sxs-lookup"><span data-stu-id="fb589-120">FileSystem name</span></span>

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

### <span data-ttu-id="fb589-121">-路徑</span><span class="sxs-lookup"><span data-stu-id="fb589-121">-Path</span></span>
<span data-ttu-id="fb589-122">指定檔案系統中應該要取取的路徑。</span><span class="sxs-lookup"><span data-stu-id="fb589-122">The path in the specified Filesystem that should be retrieved.</span></span>
<span data-ttu-id="fb589-123">可以是檔案或目錄，格式為 'directory/file.txt'或 'directory1/directory2/'。</span><span class="sxs-lookup"><span data-stu-id="fb589-123">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="fb589-124">不指定此參數以取得檔案系統的根目錄。</span><span class="sxs-lookup"><span data-stu-id="fb589-124">Not specify this parameter to get the root directory of the Filesystem.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb589-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb589-125">CommonParameters</span></span>
<span data-ttu-id="fb589-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fb589-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb589-127">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="fb589-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb589-128">輸入</span><span class="sxs-lookup"><span data-stu-id="fb589-128">INPUTS</span></span>

### <span data-ttu-id="fb589-129">System.String</span><span class="sxs-lookup"><span data-stu-id="fb589-129">System.String</span></span>

### <span data-ttu-id="fb589-130">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="fb589-130">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="fb589-131">輸出</span><span class="sxs-lookup"><span data-stu-id="fb589-131">OUTPUTS</span></span>

### <span data-ttu-id="fb589-132">Microsoft.WindowsAzure.Commands.Common.storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="fb589-132">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="fb589-133">筆記</span><span class="sxs-lookup"><span data-stu-id="fb589-133">NOTES</span></span>

## <span data-ttu-id="fb589-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="fb589-134">RELATED LINKS</span></span>
