---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/move-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Move-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Move-AzDataLakeGen2Item.md
ms.openlocfilehash: b8d46d85d00f00afdfa326b22a759f60af7b5bbe
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98273755"
---
# <span data-ttu-id="c4625-101">Move-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="c4625-101">Move-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="c4625-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c4625-102">SYNOPSIS</span></span>
<span data-ttu-id="c4625-103">將檔案或目錄移至相同儲存空間帳戶中的另一個檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="c4625-103">Move a file or directory to another a file or directory in same Storage account.</span></span>

## <span data-ttu-id="c4625-104">句法</span><span class="sxs-lookup"><span data-stu-id="c4625-104">SYNTAX</span></span>

### <span data-ttu-id="c4625-105">ReceiveManual (預設) </span><span class="sxs-lookup"><span data-stu-id="c4625-105">ReceiveManual (Default)</span></span>
```
Move-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> -DestFileSystem <String> -DestPath <String>
 [-Force] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c4625-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="c4625-106">ItemPipeline</span></span>
```
Move-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> -DestFileSystem <String> -DestPath <String>
 [-Force] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c4625-107">說明</span><span class="sxs-lookup"><span data-stu-id="c4625-107">DESCRIPTION</span></span>
<span data-ttu-id="c4625-108">**AzDataLakeGen2Item** Cmdlet 會將檔案或目錄移至同一個儲存空間帳戶中的另一個檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="c4625-108">The **Move-AzDataLakeGen2Item** cmdlet moves a a file or directory to another a file or directory in same Storage account.</span></span>
<span data-ttu-id="c4625-109">這個 Cmdlet 只有在已針對儲存空間帳戶啟用階層命名空間時才適用。</span><span class="sxs-lookup"><span data-stu-id="c4625-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="c4625-110">此類型的帳戶可使用「-EnableHierarchicalNamespace $true」執行「新-AzStorageAccount」 Cmdlet 來建立。</span><span class="sxs-lookup"><span data-stu-id="c4625-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="c4625-111">示例</span><span class="sxs-lookup"><span data-stu-id="c4625-111">EXAMPLES</span></span>

### <span data-ttu-id="c4625-112">範例1：在相同的 Filesystem 中移動折頁</span><span class="sxs-lookup"><span data-stu-id="c4625-112">Example 1: Move a fold in same Filesystem</span></span>
```
PS C:\> Move-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/" -DestFileSystem "filesystem1" -DestPath "dir3/"

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir3                 True                         2020-03-13 13:07:34Z rwxrw-rw-    $superuser           $superuser
```

<span data-ttu-id="c4625-113">這個命令會將目錄 ' dir1」移至同一個 Filesystem 中的目錄 ' dir3」。</span><span class="sxs-lookup"><span data-stu-id="c4625-113">This command move directory 'dir1' to directory 'dir3' in the same Filesystem.</span></span>

### <span data-ttu-id="c4625-114">範例2：依流水線將檔案移動到另一個儲存空間帳戶中的另一個檔案系統，而不會出現提示</span><span class="sxs-lookup"><span data-stu-id="c4625-114">Example 2: Move a file by pipeline, to another Filesystem in the same Storage account without prompt</span></span>
```
PS C:\> Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1" | Move-AzDataLakeGen2Item -DestFileSystem "filesystem2" -DestPath "dir2/file2" -Force

   FileSystem Name: filesystem2

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir2/file2           False        1024            2020-03-23 09:57:33Z rwxrw-rw-    $superuser           $superuser
```

<span data-ttu-id="c4625-115">這個命令會將 [filesystem1] 中的檔案 "dir1/file1" 移至相同儲存空間帳戶中的 [dir2/file2]，而不會出現提示。</span><span class="sxs-lookup"><span data-stu-id="c4625-115">This command move file 'dir1/file1' in 'filesystem1' to file 'dir2/file2' in 'filesystem2' in the same Storage account without prompt.</span></span>

## <span data-ttu-id="c4625-116">參數</span><span class="sxs-lookup"><span data-stu-id="c4625-116">PARAMETERS</span></span>

### <span data-ttu-id="c4625-117">-內容</span><span class="sxs-lookup"><span data-stu-id="c4625-117">-Context</span></span>
<span data-ttu-id="c4625-118">Azure 儲存區內容物件</span><span class="sxs-lookup"><span data-stu-id="c4625-118">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="c4625-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4625-119">-DefaultProfile</span></span>
<span data-ttu-id="c4625-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c4625-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4625-121">-DestFileSystem</span><span class="sxs-lookup"><span data-stu-id="c4625-121">-DestFileSystem</span></span>
<span data-ttu-id="c4625-122">目標 FileSystem 名稱</span><span class="sxs-lookup"><span data-stu-id="c4625-122">Dest FileSystem name</span></span>

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

### <span data-ttu-id="c4625-123">-DestPath</span><span class="sxs-lookup"><span data-stu-id="c4625-123">-DestPath</span></span>
<span data-ttu-id="c4625-124">Dest Blob 路徑</span><span class="sxs-lookup"><span data-stu-id="c4625-124">Dest Blob path</span></span>

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

### <span data-ttu-id="c4625-125">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="c4625-125">-FileSystem</span></span>
<span data-ttu-id="c4625-126">FileSystem 名稱</span><span class="sxs-lookup"><span data-stu-id="c4625-126">FileSystem name</span></span>

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

### <span data-ttu-id="c4625-127">-Force</span><span class="sxs-lookup"><span data-stu-id="c4625-127">-Force</span></span>
<span data-ttu-id="c4625-128">強制轉移目的地。</span><span class="sxs-lookup"><span data-stu-id="c4625-128">Force to over write the destination.</span></span>

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

### <span data-ttu-id="c4625-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4625-129">-InputObject</span></span>
<span data-ttu-id="c4625-130">要從中移出的 Azure Datalake Gen2 Item 物件。</span><span class="sxs-lookup"><span data-stu-id="c4625-130">Azure Datalake Gen2 Item Object to move from.</span></span>

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

### <span data-ttu-id="c4625-131">-Path</span><span class="sxs-lookup"><span data-stu-id="c4625-131">-Path</span></span>
<span data-ttu-id="c4625-132">要從指定的 Filesystem 中移動的路徑。</span><span class="sxs-lookup"><span data-stu-id="c4625-132">The path in the specified Filesystem that should be move from.</span></span>
<span data-ttu-id="c4625-133">可以是 "directory/file.txt" 格式或 "directory1/directory2/" 格式的檔案或目錄</span><span class="sxs-lookup"><span data-stu-id="c4625-133">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

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

### <span data-ttu-id="c4625-134">-確認</span><span class="sxs-lookup"><span data-stu-id="c4625-134">-Confirm</span></span>
<span data-ttu-id="c4625-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c4625-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4625-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4625-136">-WhatIf</span></span>
<span data-ttu-id="c4625-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c4625-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4625-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c4625-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4625-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4625-139">CommonParameters</span></span>
<span data-ttu-id="c4625-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c4625-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4625-141">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c4625-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4625-142">輸入</span><span class="sxs-lookup"><span data-stu-id="c4625-142">INPUTS</span></span>

### <span data-ttu-id="c4625-143">System.object</span><span class="sxs-lookup"><span data-stu-id="c4625-143">System.String</span></span>

### <span data-ttu-id="c4625-144">AzureDataLakeGen2Item WindowsAzure. ResourceModel。</span><span class="sxs-lookup"><span data-stu-id="c4625-144">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="c4625-145">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="c4625-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c4625-146">輸出</span><span class="sxs-lookup"><span data-stu-id="c4625-146">OUTPUTS</span></span>

### <span data-ttu-id="c4625-147">AzureDataLakeGen2Item WindowsAzure. ResourceModel。</span><span class="sxs-lookup"><span data-stu-id="c4625-147">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="c4625-148">筆記</span><span class="sxs-lookup"><span data-stu-id="c4625-148">NOTES</span></span>

## <span data-ttu-id="c4625-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="c4625-149">RELATED LINKS</span></span>
