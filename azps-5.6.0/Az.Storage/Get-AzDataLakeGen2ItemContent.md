---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azdatalakegen2itemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ItemContent.md
ms.openlocfilehash: ca92972a02fb54f10e84dbb54add535da67596aa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902689"
---
# <span data-ttu-id="5ed73-101">Get-AzDataLakeGen2ItemContent</span><span class="sxs-lookup"><span data-stu-id="5ed73-101">Get-AzDataLakeGen2ItemContent</span></span>

## <span data-ttu-id="5ed73-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5ed73-102">SYNOPSIS</span></span>
<span data-ttu-id="5ed73-103">下載檔案。</span><span class="sxs-lookup"><span data-stu-id="5ed73-103">Download a file.</span></span>

## <span data-ttu-id="5ed73-104">語法</span><span class="sxs-lookup"><span data-stu-id="5ed73-104">SYNTAX</span></span>

### <span data-ttu-id="5ed73-105">ReceiveManual (預設) </span><span class="sxs-lookup"><span data-stu-id="5ed73-105">ReceiveManual (Default)</span></span>
```
Get-AzDataLakeGen2ItemContent [-FileSystem] <String> [-Path] <String> [-Destination <String>] [-CheckMd5]
 [-Force] [-AsJob] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ed73-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="5ed73-106">ItemPipeline</span></span>
```
Get-AzDataLakeGen2ItemContent -InputObject <AzureDataLakeGen2Item> [-Destination <String>] [-CheckMd5] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ed73-107">描述</span><span class="sxs-lookup"><span data-stu-id="5ed73-107">DESCRIPTION</span></span>
<span data-ttu-id="5ed73-108">**Get-AzDataLakeGen2ItemContent** Cmdlet 在 Azure 儲存帳戶中的 Filesystem 中下載檔案。</span><span class="sxs-lookup"><span data-stu-id="5ed73-108">The **Get-AzDataLakeGen2ItemContent** cmdlet download a file in a Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="5ed73-109">只有在儲存空間帳戶已啟用階層式命名空間時，此 Cmdlet 才能運作。</span><span class="sxs-lookup"><span data-stu-id="5ed73-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="5ed73-110">您可以使用"-EnableHierarchicalNamespace $true"執行 「New-AzStorageAccount」Cmdlet 來建立這類帳戶。</span><span class="sxs-lookup"><span data-stu-id="5ed73-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="5ed73-111">例子</span><span class="sxs-lookup"><span data-stu-id="5ed73-111">EXAMPLES</span></span>

### <span data-ttu-id="5ed73-112">範例 1：下載檔案而不提示</span><span class="sxs-lookup"><span data-stu-id="5ed73-112">Example 1: Download a file without prompt</span></span>
```
PS C:\> Get-AzDataLakeGen2ItemContent -FileSystem "filesystem1" -Path "dir1/file1" -Destination $localDestFile -Force

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:29:18Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="5ed73-113">此命令會下載檔案至本地檔案，而不需要提示。</span><span class="sxs-lookup"><span data-stu-id="5ed73-113">This command downloads a file to a local file without prompt.</span></span>

### <span data-ttu-id="5ed73-114">範例 2：取得檔案，然後管道將檔案下載至本地檔案</span><span class="sxs-lookup"><span data-stu-id="5ed73-114">Example 2: Get a file, then pipeline to download the file to a local file</span></span>
```
PS C:\> Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1" |  Get-AzDataLakeGen2ItemContent -Destination $localDestFile 

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:29:18Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="5ed73-115">此命令首先會獲得檔案，然後是管道以將檔案下載到本地檔案。</span><span class="sxs-lookup"><span data-stu-id="5ed73-115">This command first gets a file, then pipeline to download the file to a local file.</span></span>

## <span data-ttu-id="5ed73-116">參數</span><span class="sxs-lookup"><span data-stu-id="5ed73-116">PARAMETERS</span></span>

### <span data-ttu-id="5ed73-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5ed73-117">-AsJob</span></span>
<span data-ttu-id="5ed73-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5ed73-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5ed73-119">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="5ed73-119">-CheckMd5</span></span>
<span data-ttu-id="5ed73-120">檢查 md5sum</span><span class="sxs-lookup"><span data-stu-id="5ed73-120">check the md5sum</span></span>

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

### <span data-ttu-id="5ed73-121">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="5ed73-121">-ConcurrentTaskCount</span></span>
<span data-ttu-id="5ed73-122">同時同步處理工作的總數量。</span><span class="sxs-lookup"><span data-stu-id="5ed73-122">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="5ed73-123">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="5ed73-123">The default value is 10.</span></span>

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

### <span data-ttu-id="5ed73-124">-內容</span><span class="sxs-lookup"><span data-stu-id="5ed73-124">-Context</span></span>
<span data-ttu-id="5ed73-125">Azure 儲存體內容物件</span><span class="sxs-lookup"><span data-stu-id="5ed73-125">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="5ed73-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ed73-126">-DefaultProfile</span></span>
<span data-ttu-id="5ed73-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5ed73-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ed73-128">-目的地</span><span class="sxs-lookup"><span data-stu-id="5ed73-128">-Destination</span></span>
<span data-ttu-id="5ed73-129">目的地本地檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="5ed73-129">Destination local file path.</span></span>

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

### <span data-ttu-id="5ed73-130">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="5ed73-130">-FileSystem</span></span>
<span data-ttu-id="5ed73-131">FileSystem 名稱</span><span class="sxs-lookup"><span data-stu-id="5ed73-131">FileSystem name</span></span>

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

### <span data-ttu-id="5ed73-132">-強制</span><span class="sxs-lookup"><span data-stu-id="5ed73-132">-Force</span></span>
<span data-ttu-id="5ed73-133">強制覆寫現有的 Blob 或檔案</span><span class="sxs-lookup"><span data-stu-id="5ed73-133">Force to overwrite the existing blob or file</span></span>

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

### <span data-ttu-id="5ed73-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ed73-134">-InputObject</span></span>
<span data-ttu-id="5ed73-135">要下載的 Azure Datalake Gen2 專案物件。</span><span class="sxs-lookup"><span data-stu-id="5ed73-135">Azure Datalake Gen2 Item Object to download.</span></span>

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

### <span data-ttu-id="5ed73-136">-路徑</span><span class="sxs-lookup"><span data-stu-id="5ed73-136">-Path</span></span>
<span data-ttu-id="5ed73-137">指定檔案系統中應移除的路徑。</span><span class="sxs-lookup"><span data-stu-id="5ed73-137">The path in the specified Filesystem that should be removed.</span></span>
<span data-ttu-id="5ed73-138">可以是檔案或目錄，格式為 'directory/file.txt' 或 'directory1/directory2/'</span><span class="sxs-lookup"><span data-stu-id="5ed73-138">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

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

### <span data-ttu-id="5ed73-139">-確認</span><span class="sxs-lookup"><span data-stu-id="5ed73-139">-Confirm</span></span>
<span data-ttu-id="5ed73-140">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5ed73-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ed73-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ed73-141">-WhatIf</span></span>
<span data-ttu-id="5ed73-142">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5ed73-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ed73-143">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5ed73-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ed73-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ed73-144">CommonParameters</span></span>
<span data-ttu-id="5ed73-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5ed73-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ed73-146">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="5ed73-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ed73-147">輸入</span><span class="sxs-lookup"><span data-stu-id="5ed73-147">INPUTS</span></span>

### <span data-ttu-id="5ed73-148">System.String</span><span class="sxs-lookup"><span data-stu-id="5ed73-148">System.String</span></span>

### <span data-ttu-id="5ed73-149">Microsoft.WindowsAzure.Commands.Common.storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="5ed73-149">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="5ed73-150">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="5ed73-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="5ed73-151">輸出</span><span class="sxs-lookup"><span data-stu-id="5ed73-151">OUTPUTS</span></span>

### <span data-ttu-id="5ed73-152">Microsoft.WindowsAzure.Commands.Common.storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="5ed73-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="5ed73-153">筆記</span><span class="sxs-lookup"><span data-stu-id="5ed73-153">NOTES</span></span>

## <span data-ttu-id="5ed73-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="5ed73-154">RELATED LINKS</span></span>
