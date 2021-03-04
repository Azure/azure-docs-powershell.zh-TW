---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/move-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Move-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Move-AzDataLakeGen2Item.md
ms.openlocfilehash: 203e7a246c16345631da290645b356392c165bad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908718"
---
# <span data-ttu-id="b3984-101">Move-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="b3984-101">Move-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="b3984-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b3984-102">SYNOPSIS</span></span>
<span data-ttu-id="b3984-103">在同一個儲存空間帳戶中，將檔案或目錄移至另一個檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="b3984-103">Move a file or directory to another a file or directory in same Storage account.</span></span>

## <span data-ttu-id="b3984-104">語法</span><span class="sxs-lookup"><span data-stu-id="b3984-104">SYNTAX</span></span>

### <span data-ttu-id="b3984-105">ReceiveManual (預設) </span><span class="sxs-lookup"><span data-stu-id="b3984-105">ReceiveManual (Default)</span></span>
```
Move-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> -DestFileSystem <String> -DestPath <String>
 [-Force] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b3984-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="b3984-106">ItemPipeline</span></span>
```
Move-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> -DestFileSystem <String> -DestPath <String>
 [-Force] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b3984-107">描述</span><span class="sxs-lookup"><span data-stu-id="b3984-107">DESCRIPTION</span></span>
<span data-ttu-id="b3984-108">**Move-AzDataLakeGen2Item** Cmdlet 會將檔案或目錄移至同一個儲存帳戶中的另一個檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="b3984-108">The **Move-AzDataLakeGen2Item** cmdlet moves a a file or directory to another a file or directory in same Storage account.</span></span>
<span data-ttu-id="b3984-109">只有在儲存空間帳戶已啟用階層式命名空間時，此 Cmdlet 才能運作。</span><span class="sxs-lookup"><span data-stu-id="b3984-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="b3984-110">您可以使用"-EnableHierarchicalNamespace $true"執行 「New-AzStorageAccount」Cmdlet 來建立這類帳戶。</span><span class="sxs-lookup"><span data-stu-id="b3984-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="b3984-111">例子</span><span class="sxs-lookup"><span data-stu-id="b3984-111">EXAMPLES</span></span>

### <span data-ttu-id="b3984-112">範例 1：在同一個檔案系統中移動折頁</span><span class="sxs-lookup"><span data-stu-id="b3984-112">Example 1: Move a fold in same Filesystem</span></span>
```
PS C:\> Move-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/" -DestFileSystem "filesystem1" -DestPath "dir3/"

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir3                 True                         2020-03-13 13:07:34Z rwxrw-rw-    $superuser           $superuser
```

<span data-ttu-id="b3984-113">此命令會在同一個檔案系統中將目錄 "dir1" 移至目錄 "dir3"。</span><span class="sxs-lookup"><span data-stu-id="b3984-113">This command move directory 'dir1' to directory 'dir3' in the same Filesystem.</span></span>

### <span data-ttu-id="b3984-114">範例 2：根據管線將檔案移至同一個儲存帳戶中的另一個檔案系統，而不提示</span><span class="sxs-lookup"><span data-stu-id="b3984-114">Example 2: Move a file by pipeline, to another Filesystem in the same Storage account without prompt</span></span>
```
PS C:\> Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1" | Move-AzDataLakeGen2Item -DestFileSystem "filesystem2" -DestPath "dir2/file2" -Force

   FileSystem Name: filesystem2

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir2/file2           False        1024            2020-03-23 09:57:33Z rwxrw-rw-    $superuser           $superuser
```

<span data-ttu-id="b3984-115">此命令將 'filesystem1' 中的檔案 'dir1/file1' 移至同一個儲存帳戶中的 'filesystem2' 中的 'dir2/file2'，而不會提示。</span><span class="sxs-lookup"><span data-stu-id="b3984-115">This command move file 'dir1/file1' in 'filesystem1' to file 'dir2/file2' in 'filesystem2' in the same Storage account without prompt.</span></span>

## <span data-ttu-id="b3984-116">參數</span><span class="sxs-lookup"><span data-stu-id="b3984-116">PARAMETERS</span></span>

### <span data-ttu-id="b3984-117">-內容</span><span class="sxs-lookup"><span data-stu-id="b3984-117">-Context</span></span>
<span data-ttu-id="b3984-118">Azure 儲存體內容物件</span><span class="sxs-lookup"><span data-stu-id="b3984-118">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="b3984-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3984-119">-DefaultProfile</span></span>
<span data-ttu-id="b3984-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b3984-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3984-121">-DestFileSystem</span><span class="sxs-lookup"><span data-stu-id="b3984-121">-DestFileSystem</span></span>
<span data-ttu-id="b3984-122">Dest FileSystem 名稱</span><span class="sxs-lookup"><span data-stu-id="b3984-122">Dest FileSystem name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3984-123">-DestPath</span><span class="sxs-lookup"><span data-stu-id="b3984-123">-DestPath</span></span>
<span data-ttu-id="b3984-124">Dest Blob 路徑</span><span class="sxs-lookup"><span data-stu-id="b3984-124">Dest Blob path</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3984-125">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="b3984-125">-FileSystem</span></span>
<span data-ttu-id="b3984-126">FileSystem 名稱</span><span class="sxs-lookup"><span data-stu-id="b3984-126">FileSystem name</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3984-127">-強制</span><span class="sxs-lookup"><span data-stu-id="b3984-127">-Force</span></span>
<span data-ttu-id="b3984-128">強制超寫目的地。</span><span class="sxs-lookup"><span data-stu-id="b3984-128">Force to over write the destination.</span></span>

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

### <span data-ttu-id="b3984-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3984-129">-InputObject</span></span>
<span data-ttu-id="b3984-130">要移動的 Azure Datalake 第 2 代專案物件。</span><span class="sxs-lookup"><span data-stu-id="b3984-130">Azure Datalake Gen2 Item Object to move from.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item
Parameter Sets: ItemPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3984-131">-路徑</span><span class="sxs-lookup"><span data-stu-id="b3984-131">-Path</span></span>
<span data-ttu-id="b3984-132">指定檔案系統中應移動的路徑。</span><span class="sxs-lookup"><span data-stu-id="b3984-132">The path in the specified Filesystem that should be move from.</span></span>
<span data-ttu-id="b3984-133">可以是檔案或目錄，格式為 'directory/file.txt' 或 'directory1/directory2/'</span><span class="sxs-lookup"><span data-stu-id="b3984-133">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3984-134">-確認</span><span class="sxs-lookup"><span data-stu-id="b3984-134">-Confirm</span></span>
<span data-ttu-id="b3984-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b3984-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3984-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3984-136">-WhatIf</span></span>
<span data-ttu-id="b3984-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b3984-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3984-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b3984-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3984-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3984-139">CommonParameters</span></span>
<span data-ttu-id="b3984-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b3984-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3984-141">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="b3984-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3984-142">輸入</span><span class="sxs-lookup"><span data-stu-id="b3984-142">INPUTS</span></span>

### <span data-ttu-id="b3984-143">System.String</span><span class="sxs-lookup"><span data-stu-id="b3984-143">System.String</span></span>

### <span data-ttu-id="b3984-144">Microsoft.WindowsAzure.Commands.Common.storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="b3984-144">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="b3984-145">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="b3984-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b3984-146">輸出</span><span class="sxs-lookup"><span data-stu-id="b3984-146">OUTPUTS</span></span>

### <span data-ttu-id="b3984-147">Microsoft.WindowsAzure.Commands.Common.storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="b3984-147">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="b3984-148">筆記</span><span class="sxs-lookup"><span data-stu-id="b3984-148">NOTES</span></span>

## <span data-ttu-id="b3984-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="b3984-149">RELATED LINKS</span></span>
