---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azdatalakegen2itemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ItemContent.md
ms.openlocfilehash: 9721305494ffd9b1d6a6f260008f050c9600437a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140803"
---
# <span data-ttu-id="03f40-101">Get-AzDataLakeGen2ItemContent</span><span class="sxs-lookup"><span data-stu-id="03f40-101">Get-AzDataLakeGen2ItemContent</span></span>

## <span data-ttu-id="03f40-102">摘要</span><span class="sxs-lookup"><span data-stu-id="03f40-102">SYNOPSIS</span></span>
<span data-ttu-id="03f40-103">下載檔案。</span><span class="sxs-lookup"><span data-stu-id="03f40-103">Download a file.</span></span>

## <span data-ttu-id="03f40-104">句法</span><span class="sxs-lookup"><span data-stu-id="03f40-104">SYNTAX</span></span>

### <span data-ttu-id="03f40-105">ReceiveManual (預設) </span><span class="sxs-lookup"><span data-stu-id="03f40-105">ReceiveManual (Default)</span></span>
```
Get-AzDataLakeGen2ItemContent [-FileSystem] <String> [-Path] <String> [-Destination <String>] [-CheckMd5]
 [-Force] [-AsJob] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03f40-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="03f40-106">ItemPipeline</span></span>
```
Get-AzDataLakeGen2ItemContent -InputObject <AzureDataLakeGen2Item> [-Destination <String>] [-CheckMd5] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03f40-107">說明</span><span class="sxs-lookup"><span data-stu-id="03f40-107">DESCRIPTION</span></span>
<span data-ttu-id="03f40-108">**AzDataLakeGen2ItemContent** Cmdlet 會在 Azure 儲存空間帳戶的檔案系統中下載檔案。</span><span class="sxs-lookup"><span data-stu-id="03f40-108">The **Get-AzDataLakeGen2ItemContent** cmdlet download a file in a Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="03f40-109">這個 Cmdlet 只有在已針對儲存空間帳戶啟用階層命名空間時才適用。</span><span class="sxs-lookup"><span data-stu-id="03f40-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="03f40-110">此類型的帳戶可使用「-EnableHierarchicalNamespace $true」執行「新-AzStorageAccount」 Cmdlet 來建立。</span><span class="sxs-lookup"><span data-stu-id="03f40-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="03f40-111">示例</span><span class="sxs-lookup"><span data-stu-id="03f40-111">EXAMPLES</span></span>

### <span data-ttu-id="03f40-112">範例1：不提示就下載檔案</span><span class="sxs-lookup"><span data-stu-id="03f40-112">Example 1: Download a file without prompt</span></span>
```
PS C:\> Get-AzDataLakeGen2ItemContent -FileSystem "filesystem1" -Path "dir1/file1" -Destination $localDestFile -Force

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:29:18Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="03f40-113">這個命令不需提示就能將檔案下載到本機檔案。</span><span class="sxs-lookup"><span data-stu-id="03f40-113">This command downloads a file to a local file without prompt.</span></span>

### <span data-ttu-id="03f40-114">範例2：取得檔案，然後選取 [管線]，將檔案下載到本機檔案</span><span class="sxs-lookup"><span data-stu-id="03f40-114">Example 2: Get a file, then pipeline to download the file to a local file</span></span>
```
PS C:\> Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1" |  Get-AzDataLakeGen2ItemContent -Destination $localDestFile 

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:29:18Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="03f40-115">這個命令會先取得檔案，然後再取得 [管線]，將檔案下載到本機檔案。</span><span class="sxs-lookup"><span data-stu-id="03f40-115">This command first gets a file, then pipeline to download the file to a local file.</span></span>

## <span data-ttu-id="03f40-116">參數</span><span class="sxs-lookup"><span data-stu-id="03f40-116">PARAMETERS</span></span>

### <span data-ttu-id="03f40-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03f40-117">-AsJob</span></span>
<span data-ttu-id="03f40-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="03f40-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="03f40-119">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="03f40-119">-CheckMd5</span></span>
<span data-ttu-id="03f40-120">檢查 md5sum</span><span class="sxs-lookup"><span data-stu-id="03f40-120">check the md5sum</span></span>

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

### <span data-ttu-id="03f40-121">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="03f40-121">-ConcurrentTaskCount</span></span>
<span data-ttu-id="03f40-122">並行非同步工作的總數量。</span><span class="sxs-lookup"><span data-stu-id="03f40-122">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="03f40-123">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="03f40-123">The default value is 10.</span></span>

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

### <span data-ttu-id="03f40-124">-內容</span><span class="sxs-lookup"><span data-stu-id="03f40-124">-Context</span></span>
<span data-ttu-id="03f40-125">Azure 儲存區內容物件</span><span class="sxs-lookup"><span data-stu-id="03f40-125">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="03f40-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03f40-126">-DefaultProfile</span></span>
<span data-ttu-id="03f40-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="03f40-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03f40-128">-目的地</span><span class="sxs-lookup"><span data-stu-id="03f40-128">-Destination</span></span>
<span data-ttu-id="03f40-129">目的地本機檔路徑。</span><span class="sxs-lookup"><span data-stu-id="03f40-129">Destination local file path.</span></span>

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

### <span data-ttu-id="03f40-130">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="03f40-130">-FileSystem</span></span>
<span data-ttu-id="03f40-131">FileSystem 名稱</span><span class="sxs-lookup"><span data-stu-id="03f40-131">FileSystem name</span></span>

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

### <span data-ttu-id="03f40-132">-Force</span><span class="sxs-lookup"><span data-stu-id="03f40-132">-Force</span></span>
<span data-ttu-id="03f40-133">強制覆寫現有的 blob 或檔案</span><span class="sxs-lookup"><span data-stu-id="03f40-133">Force to overwrite the existing blob or file</span></span>

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

### <span data-ttu-id="03f40-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03f40-134">-InputObject</span></span>
<span data-ttu-id="03f40-135">要下載的 Azure Datalake Gen2 Item 物件。</span><span class="sxs-lookup"><span data-stu-id="03f40-135">Azure Datalake Gen2 Item Object to download.</span></span>

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

### <span data-ttu-id="03f40-136">-Path</span><span class="sxs-lookup"><span data-stu-id="03f40-136">-Path</span></span>
<span data-ttu-id="03f40-137">要移除的指定檔案系統中的路徑。</span><span class="sxs-lookup"><span data-stu-id="03f40-137">The path in the specified Filesystem that should be removed.</span></span>
<span data-ttu-id="03f40-138">可以是 "directory/file.txt" 格式或 "directory1/directory2/" 格式的檔案或目錄</span><span class="sxs-lookup"><span data-stu-id="03f40-138">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

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

### <span data-ttu-id="03f40-139">-確認</span><span class="sxs-lookup"><span data-stu-id="03f40-139">-Confirm</span></span>
<span data-ttu-id="03f40-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="03f40-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03f40-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03f40-141">-WhatIf</span></span>
<span data-ttu-id="03f40-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="03f40-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03f40-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="03f40-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03f40-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03f40-144">CommonParameters</span></span>
<span data-ttu-id="03f40-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="03f40-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03f40-146">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="03f40-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03f40-147">輸入</span><span class="sxs-lookup"><span data-stu-id="03f40-147">INPUTS</span></span>

### <span data-ttu-id="03f40-148">System.object</span><span class="sxs-lookup"><span data-stu-id="03f40-148">System.String</span></span>

### <span data-ttu-id="03f40-149">AzureDataLakeGen2Item WindowsAzure. ResourceModel。</span><span class="sxs-lookup"><span data-stu-id="03f40-149">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="03f40-150">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="03f40-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="03f40-151">輸出</span><span class="sxs-lookup"><span data-stu-id="03f40-151">OUTPUTS</span></span>

### <span data-ttu-id="03f40-152">AzureDataLakeGen2Item WindowsAzure. ResourceModel。</span><span class="sxs-lookup"><span data-stu-id="03f40-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="03f40-153">筆記</span><span class="sxs-lookup"><span data-stu-id="03f40-153">NOTES</span></span>

## <span data-ttu-id="03f40-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="03f40-154">RELATED LINKS</span></span>
