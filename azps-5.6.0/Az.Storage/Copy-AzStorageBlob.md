---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/copy-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Copy-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Copy-AzStorageBlob.md
ms.openlocfilehash: 76e89c90da10e8e232a564fb5fb7e5f8cc807327
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911269"
---
# <span data-ttu-id="162d6-101">Copy-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="162d6-101">Copy-AzStorageBlob</span></span>

## <span data-ttu-id="162d6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="162d6-102">SYNOPSIS</span></span>
<span data-ttu-id="162d6-103">同步複製 Blob。</span><span class="sxs-lookup"><span data-stu-id="162d6-103">Copy a blob synchronously.</span></span>

## <span data-ttu-id="162d6-104">語法</span><span class="sxs-lookup"><span data-stu-id="162d6-104">SYNTAX</span></span>

### <span data-ttu-id="162d6-105">ContainerName (預設) </span><span class="sxs-lookup"><span data-stu-id="162d6-105">ContainerName (Default)</span></span>
```
Copy-AzStorageBlob [-SrcBlob] <String> -SrcContainer <String> -DestContainer <String> [-DestBlob <String>]
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-EncryptionScope <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="162d6-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="162d6-106">BlobInstance</span></span>
```
Copy-AzStorageBlob [-BlobBaseClient <BlobBaseClient>] -DestContainer <String> [-DestBlob <String>]
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-EncryptionScope <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="162d6-107">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="162d6-107">UriPipeline</span></span>
```
Copy-AzStorageBlob -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-EncryptionScope <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="162d6-108">描述</span><span class="sxs-lookup"><span data-stu-id="162d6-108">DESCRIPTION</span></span>
<span data-ttu-id="162d6-109">**Copy-AzStorageBlob** Cmdlet 會同步複製 Blob，目前僅支援區塊 Blob。</span><span class="sxs-lookup"><span data-stu-id="162d6-109">The **Copy-AzStorageBlob** cmdlet copies a blob synchronously, currently only support block blob.</span></span>

## <span data-ttu-id="162d6-110">例子</span><span class="sxs-lookup"><span data-stu-id="162d6-110">EXAMPLES</span></span>

### <span data-ttu-id="162d6-111">範例 1：將命名 Blob 複製到另一個</span><span class="sxs-lookup"><span data-stu-id="162d6-111">Example 1: Copy a named blob to another</span></span>
```
C:\PS> $destBlob = Copy-AzStorageBlob -SrcContainer "sourcecontainername" -SrcBlob "srcblobname" -DestContainer "destcontainername" -DestBlob "destblobname"
```

<span data-ttu-id="162d6-112">此命令會使用新的 Blob 名稱，將 Blob 從來源容器複製到目的地容器。</span><span class="sxs-lookup"><span data-stu-id="162d6-112">This command copies a blob from source container to the destination container with a new blob name.</span></span> 

### <span data-ttu-id="162d6-113">範例 2：從 Blob 物件複製 Blob</span><span class="sxs-lookup"><span data-stu-id="162d6-113">Example 2: Copy blob from a blob object</span></span>
```
C:\PS> $srcBlob = Get-AzStorageBlob -Container $containerName -Blob $blobName  -Context $ctx 
C:\PS> $destBlob =  $srcBlob | Copy-AzStorageBlob  -DestContainer "destcontainername" -DestBlob "destblobname"
```

<span data-ttu-id="162d6-114">此命令會使用新的 Blob 名稱，將 Blob 從來源 Blob 物件複製到目的容器。</span><span class="sxs-lookup"><span data-stu-id="162d6-114">This command copies a blob from source blob object to the destination container with a new blob name.</span></span>

### <span data-ttu-id="162d6-115">範例 3：從 Blob Uri 複製 Blob</span><span class="sxs-lookup"><span data-stu-id="162d6-115">Example 3: Copy blob from a blob Uri</span></span>
```
C:\PS> $srcBlobUri = New-AzStorageBlobSASToken -Container $srcContainerName -Blob $srcBlobName -Permission rt -ExpiryTime (Get-Date).AddDays(7) -FullUri 
C:\PS> $destBlob = Copy-AzStorageBlob -AbsoluteUri $srcBlobUri -DestContainer "destcontainername" -DestBlob "destblobname"
```

<span data-ttu-id="162d6-116">第一個命令會建立來源 Blob 的 Blob Uri，具有 sas 許可權權杖 "rt"。</span><span class="sxs-lookup"><span data-stu-id="162d6-116">The first command creates a blob Uri of the source blob, with sas token of permission "rt".</span></span> <span data-ttu-id="162d6-117">第二個命令會從來源 Blob Uri 複製到目標 Blob。</span><span class="sxs-lookup"><span data-stu-id="162d6-117">The second command copies from source blob Uri to the destination blob.</span></span>

### <span data-ttu-id="162d6-118">範例 4：更新區塊 Blob 加密範圍</span><span class="sxs-lookup"><span data-stu-id="162d6-118">Example 4: Update a block blob encryption scope</span></span>
```
C:\PS> $blob = Copy-AzStorageBlob -SrcContainer $containerName -SrcBlob $blobname -DestContainer $containername -EncryptionScope $newScopeName -Force
```

<span data-ttu-id="162d6-119">此命令會更新區塊 Blob 加密範圍，以新的加密範圍將其複製到本身。</span><span class="sxs-lookup"><span data-stu-id="162d6-119">This command update a block blob encryption scope by copy it to itself with a new encryption scope.</span></span>

## <span data-ttu-id="162d6-120">參數</span><span class="sxs-lookup"><span data-stu-id="162d6-120">PARAMETERS</span></span>

### <span data-ttu-id="162d6-121">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="162d6-121">-AbsoluteUri</span></span>
<span data-ttu-id="162d6-122">來源 Blob uri</span><span class="sxs-lookup"><span data-stu-id="162d6-122">Source blob uri</span></span>

```yaml
Type: System.String
Parameter Sets: UriPipeline
Aliases: SrcUri, SourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="162d6-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="162d6-123">-AsJob</span></span>
<span data-ttu-id="162d6-124">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="162d6-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="162d6-125">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="162d6-125">-BlobBaseClient</span></span>
<span data-ttu-id="162d6-126">BlobBaseClient 物件</span><span class="sxs-lookup"><span data-stu-id="162d6-126">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobInstance
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="162d6-127">-內容</span><span class="sxs-lookup"><span data-stu-id="162d6-127">-Context</span></span>
<span data-ttu-id="162d6-128">來源 Azure 儲存體內容物件</span><span class="sxs-lookup"><span data-stu-id="162d6-128">Source Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerName, BlobInstance
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: UriPipeline
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="162d6-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="162d6-129">-DefaultProfile</span></span>
<span data-ttu-id="162d6-130">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="162d6-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="162d6-131">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="162d6-131">-DestBlob</span></span>
<span data-ttu-id="162d6-132">目的地 Blob 名稱</span><span class="sxs-lookup"><span data-stu-id="162d6-132">Destination blob name</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, BlobInstance
Aliases: DestinationBlob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UriPipeline
Aliases: DestinationBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="162d6-133">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="162d6-133">-DestContainer</span></span>
<span data-ttu-id="162d6-134">目的地容器名稱</span><span class="sxs-lookup"><span data-stu-id="162d6-134">Destination container name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="162d6-135">-DestCoNtext</span><span class="sxs-lookup"><span data-stu-id="162d6-135">-DestContext</span></span>
<span data-ttu-id="162d6-136">目的地儲存內容物件</span><span class="sxs-lookup"><span data-stu-id="162d6-136">Destination Storage context object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases: DestinationContext

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="162d6-137">-EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="162d6-137">-EncryptionScope</span></span>
<span data-ttu-id="162d6-138">要求 dest Blob 時所使用的加密範圍。</span><span class="sxs-lookup"><span data-stu-id="162d6-138">Encryption scope to be used when making requests to the dest blob.</span></span>

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

### <span data-ttu-id="162d6-139">-強制</span><span class="sxs-lookup"><span data-stu-id="162d6-139">-Force</span></span>
<span data-ttu-id="162d6-140">強制覆寫現有的 Blob 或檔案</span><span class="sxs-lookup"><span data-stu-id="162d6-140">Force to overwrite the existing blob or file</span></span>

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

### <span data-ttu-id="162d6-141">-RehydratePriority</span><span class="sxs-lookup"><span data-stu-id="162d6-141">-RehydratePriority</span></span>
<span data-ttu-id="162d6-142">封鎖 Blob RehydratePriority。</span><span class="sxs-lookup"><span data-stu-id="162d6-142">Block Blob RehydratePriority.</span></span>
<span data-ttu-id="162d6-143">表示要重新水合已存檔 Blob 的優先順序。</span><span class="sxs-lookup"><span data-stu-id="162d6-143">Indicates the priority with which to rehydrate an archived blob.</span></span>
<span data-ttu-id="162d6-144">有效值為高/標準。</span><span class="sxs-lookup"><span data-stu-id="162d6-144">Valid values are High/Standard.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.RehydratePriority
Parameter Sets: (All)
Aliases:
Accepted values: Standard, High

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="162d6-145">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="162d6-145">-SrcBlob</span></span>
<span data-ttu-id="162d6-146">Blob 名稱</span><span class="sxs-lookup"><span data-stu-id="162d6-146">Blob name</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases: SourceBlob

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="162d6-147">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="162d6-147">-SrcContainer</span></span>
<span data-ttu-id="162d6-148">來源容器名稱</span><span class="sxs-lookup"><span data-stu-id="162d6-148">Source Container name</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases: SourceContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="162d6-149">-StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="162d6-149">-StandardBlobTier</span></span>
<span data-ttu-id="162d6-150">封鎖 Blob 層，有效的值為 Hot/Cool/Archive。</span><span class="sxs-lookup"><span data-stu-id="162d6-150">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="162d6-151">請參閱 https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="162d6-151">See detail in https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hot, Cool, Archive

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="162d6-152">-確認</span><span class="sxs-lookup"><span data-stu-id="162d6-152">-Confirm</span></span>
<span data-ttu-id="162d6-153">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="162d6-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="162d6-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="162d6-154">-WhatIf</span></span>
<span data-ttu-id="162d6-155">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="162d6-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="162d6-156">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="162d6-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="162d6-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="162d6-157">CommonParameters</span></span>
<span data-ttu-id="162d6-158">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="162d6-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="162d6-159">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="162d6-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="162d6-160">輸入</span><span class="sxs-lookup"><span data-stu-id="162d6-160">INPUTS</span></span>

### <span data-ttu-id="162d6-161">Azure.storage.Blobs.Specialized.BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="162d6-161">Azure.Storage.Blobs.Specialized.BlobBaseClient</span></span>

### <span data-ttu-id="162d6-162">System.String</span><span class="sxs-lookup"><span data-stu-id="162d6-162">System.String</span></span>

### <span data-ttu-id="162d6-163">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="162d6-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="162d6-164">輸出</span><span class="sxs-lookup"><span data-stu-id="162d6-164">OUTPUTS</span></span>

### <span data-ttu-id="162d6-165">Microsoft.WindowsAzure.Commands.Common.storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="162d6-165">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="162d6-166">筆記</span><span class="sxs-lookup"><span data-stu-id="162d6-166">NOTES</span></span>

## <span data-ttu-id="162d6-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="162d6-167">RELATED LINKS</span></span>
