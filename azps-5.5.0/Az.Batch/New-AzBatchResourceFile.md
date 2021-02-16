---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchresourcefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
ms.openlocfilehash: 43cbf86ca473b6984ee2190b1d10df61b6d32e64
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100141454"
---
# <span data-ttu-id="1c2ae-101">New-AzBatchResourceFile</span><span class="sxs-lookup"><span data-stu-id="1c2ae-101">New-AzBatchResourceFile</span></span>

## <span data-ttu-id="1c2ae-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1c2ae-102">SYNOPSIS</span></span>
<span data-ttu-id="1c2ae-103">建立供使用的資源檔 `New-AzBatchTask` 。</span><span class="sxs-lookup"><span data-stu-id="1c2ae-103">Creates a Resource File for usage by `New-AzBatchTask`.</span></span>

## <span data-ttu-id="1c2ae-104">句法</span><span class="sxs-lookup"><span data-stu-id="1c2ae-104">SYNTAX</span></span>

### <span data-ttu-id="1c2ae-105">HttpUrl (預設) </span><span class="sxs-lookup"><span data-stu-id="1c2ae-105">HttpUrl (Default)</span></span>
```
New-AzBatchResourceFile -HttpUrl <String> -FilePath <String> [-FileMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c2ae-106">StorageContainerUrl</span><span class="sxs-lookup"><span data-stu-id="1c2ae-106">StorageContainerUrl</span></span>
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] [-BlobPrefix <String>]
 -StorageContainerUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c2ae-107">AutoStorageContainerName</span><span class="sxs-lookup"><span data-stu-id="1c2ae-107">AutoStorageContainerName</span></span>
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] -AutoStorageContainerName <String>
 [-BlobPrefix <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c2ae-108">說明</span><span class="sxs-lookup"><span data-stu-id="1c2ae-108">DESCRIPTION</span></span>
<span data-ttu-id="1c2ae-109">建立供使用的資源檔 `New-AzBatchTask` 。</span><span class="sxs-lookup"><span data-stu-id="1c2ae-109">Creates a Resource File for usage by `New-AzBatchTask`.</span></span>

## <span data-ttu-id="1c2ae-110">示例</span><span class="sxs-lookup"><span data-stu-id="1c2ae-110">EXAMPLES</span></span>

### <span data-ttu-id="1c2ae-111">範例1：從指向單一檔案的 HTTP URL 建立資源檔</span><span class="sxs-lookup"><span data-stu-id="1c2ae-111">Example 1: Create a resource file from an HTTP URL pointing at a single file</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -HttpUrl "https://testacct.blob.core.windows.net/" -FilePath "file1"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="1c2ae-112">建立 `PSResourceFile` 參考 HTTP url。</span><span class="sxs-lookup"><span data-stu-id="1c2ae-112">Creates a `PSResourceFile` referencing an HTTP url.</span></span>

### <span data-ttu-id="1c2ae-113">範例2：從 Azure 儲存體容器 URL 建立資源檔</span><span class="sxs-lookup"><span data-stu-id="1c2ae-113">Example 2: Create a resource file from an Azure Storage container URL</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -StorageContainerUrl "https://testacct.blob.core.windows.net/mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="1c2ae-114">建立 `PSResourceFile` 參照 Azure 儲存體容器 URL。</span><span class="sxs-lookup"><span data-stu-id="1c2ae-114">Creates a `PSResourceFile` referencing an Azure Storage container URL.</span></span> <span data-ttu-id="1c2ae-115">容器中的所有檔案將會下載到指定的資料夾中。</span><span class="sxs-lookup"><span data-stu-id="1c2ae-115">All files in the container will be downloaded to the specified folder.</span></span>

### <span data-ttu-id="1c2ae-116">範例3：從自動儲存空間容器名稱建立資源檔</span><span class="sxs-lookup"><span data-stu-id="1c2ae-116">Example 3: Create a resource file from an Auto Storage container name</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -AutoStorageContainerName "mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="1c2ae-117">建立對 `PSResourceFile` 自動儲存空間容器名稱的參照。</span><span class="sxs-lookup"><span data-stu-id="1c2ae-117">Creates a `PSResourceFile` referencing an Auto Storage container name.</span></span> <span data-ttu-id="1c2ae-118">容器中的所有檔案將會下載到指定的資料夾中。</span><span class="sxs-lookup"><span data-stu-id="1c2ae-118">All files in the container will be downloaded to the specified folder.</span></span>

## <span data-ttu-id="1c2ae-119">參數</span><span class="sxs-lookup"><span data-stu-id="1c2ae-119">PARAMETERS</span></span>

### <span data-ttu-id="1c2ae-120">-AutoStorageContainerName</span><span class="sxs-lookup"><span data-stu-id="1c2ae-120">-AutoStorageContainerName</span></span>
<span data-ttu-id="1c2ae-121">[自動儲存空間] 帳戶中的儲存容器名稱。</span><span class="sxs-lookup"><span data-stu-id="1c2ae-121">The storage container name in the auto storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: AutoStorageContainerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c2ae-122">-BlobPrefix</span><span class="sxs-lookup"><span data-stu-id="1c2ae-122">-BlobPrefix</span></span>
<span data-ttu-id="1c2ae-123">取得從 Azure 儲存空間容器下載 blob 時所要使用的 blob 前置詞。</span><span class="sxs-lookup"><span data-stu-id="1c2ae-123">Gets the blob prefix to use when downloading blobs from an Azure Storage container.</span></span>
<span data-ttu-id="1c2ae-124">只有其名稱以指定的首碼開頭的 blob 才會下載。</span><span class="sxs-lookup"><span data-stu-id="1c2ae-124">Only the blobs whose names begin with the specified prefix will be downloaded.</span></span>
<span data-ttu-id="1c2ae-125">此前置詞可以是部分的檔案名或子目錄。</span><span class="sxs-lookup"><span data-stu-id="1c2ae-125">This prefix can be a partial filename or a subdirectory.</span></span>
<span data-ttu-id="1c2ae-126">如果未指定前置詞，將會下載容器中的所有檔案。</span><span class="sxs-lookup"><span data-stu-id="1c2ae-126">If a prefix is not specified, all the files in the container will be downloaded.</span></span>

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl, AutoStorageContainerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c2ae-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c2ae-127">-DefaultProfile</span></span>
<span data-ttu-id="1c2ae-128">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1c2ae-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c2ae-129">-低</span><span class="sxs-lookup"><span data-stu-id="1c2ae-129">-FileMode</span></span>
<span data-ttu-id="1c2ae-130">取得八進位格式的檔案許可權模式屬性。</span><span class="sxs-lookup"><span data-stu-id="1c2ae-130">Gets the file permission mode attribute in octal format.</span></span>
<span data-ttu-id="1c2ae-131">這個屬性只有在資源檔案下載到 Linux 節點時才適用。</span><span class="sxs-lookup"><span data-stu-id="1c2ae-131">This property is applicable only if the resource file is downloaded to a Linux node.</span></span>
<span data-ttu-id="1c2ae-132">如果沒有為 Linux 節點指定此屬性，則預設值為0770。</span><span class="sxs-lookup"><span data-stu-id="1c2ae-132">If this property is not specified for a Linux node, then the default value is 0770.</span></span>

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

### <span data-ttu-id="1c2ae-133">-FilePath</span><span class="sxs-lookup"><span data-stu-id="1c2ae-133">-FilePath</span></span>
<span data-ttu-id="1c2ae-134">要將檔案下載到哪個計算節點上 (s) 的位置，相對於任務的工作目錄。</span><span class="sxs-lookup"><span data-stu-id="1c2ae-134">The location on the compute node to which to download the file(s), relative to the task's working directory.</span></span> <span data-ttu-id="1c2ae-135">如果指定了 HttpUrl 參數，則需要 FilePath，並說明檔案將下載到哪個路徑，包括檔案名。</span><span class="sxs-lookup"><span data-stu-id="1c2ae-135">If the HttpUrl parameter is specified, the FilePath is required and describes the path which the file will be downloaded to, including the filename.</span></span> <span data-ttu-id="1c2ae-136">否則，如果指定 AutoStorageContainerName 或 StorageContainerUrl 參數，則 FilePath 是選擇性的，也就是下載檔案的目錄。</span><span class="sxs-lookup"><span data-stu-id="1c2ae-136">Otherwise, if the AutoStorageContainerName or StorageContainerUrl parameters are specified, FilePath is optional and is the directory to download the files to.</span></span> <span data-ttu-id="1c2ae-137">在使用 FilePath 做為目錄的情況下，任何已與輸入資料相關聯的目錄結構，都會保留完整並附加到指定的 FilePath 目錄中。</span><span class="sxs-lookup"><span data-stu-id="1c2ae-137">In the case where FilePath is used as a directory, any directory structure already associated with the input data will be retained in full and appended to the specified FilePath directory.</span></span> <span data-ttu-id="1c2ae-138">指定的相對路徑無法從工作的工作目錄中中斷 (例如使用 "...") ]。</span><span class="sxs-lookup"><span data-stu-id="1c2ae-138">The specified relative path cannot break out of the task's working directory (for example by using '..').</span></span>

```yaml
Type: System.String
Parameter Sets: HttpUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl, AutoStorageContainerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c2ae-139">-HttpUrl</span><span class="sxs-lookup"><span data-stu-id="1c2ae-139">-HttpUrl</span></span>
<span data-ttu-id="1c2ae-140">要下載之檔案的 URL。</span><span class="sxs-lookup"><span data-stu-id="1c2ae-140">The URL of the file to download.</span></span>
<span data-ttu-id="1c2ae-141">如果 URL 是 Azure Blob 儲存空間，就必須使用匿名存取才能閱讀;也就是說，在下載 blob 時，批次服務不會顯示任何認證。</span><span class="sxs-lookup"><span data-stu-id="1c2ae-141">If the URL is Azure Blob Storage, it must be readable using anonymous access; that is, the Batch service does not present any credentials when downloading the blob.</span></span>
<span data-ttu-id="1c2ae-142">您可以透過兩種方式取得 Azure 儲存區中的 blob URL：包含共用存取簽章 (SAS) 授予對 blob 的讀取權限，或將 blob 或其容器的 ACL 設定為允許公用存取。</span><span class="sxs-lookup"><span data-stu-id="1c2ae-142">There are two ways to get such a URL for a blob in Azure storage: include a Shared Access Signature (SAS) granting read permissions on the blob, or set the ACL for the blob or its container to allow public access.</span></span>

```yaml
Type: System.String
Parameter Sets: HttpUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c2ae-143">-StorageContainerUrl</span><span class="sxs-lookup"><span data-stu-id="1c2ae-143">-StorageContainerUrl</span></span>
<span data-ttu-id="1c2ae-144">Azure Blob 儲存空間中的 blob 容器 URL。</span><span class="sxs-lookup"><span data-stu-id="1c2ae-144">The URL of the blob container within Azure Blob Storage.</span></span>
<span data-ttu-id="1c2ae-145">這個 URL 必須是可讀取的，且可以使用匿名存取 listable。也就是說，當您從容器下載 blob 時，批服務不會顯示任何認證。</span><span class="sxs-lookup"><span data-stu-id="1c2ae-145">This URL must be readable and listable using anonymous access; that is, the Batch service does not present any credentials when downloading blobs from the container.</span></span>
<span data-ttu-id="1c2ae-146">在 Azure 儲存體中，有兩種方式可取得容器的 URL：包含共用存取簽章 (SAS) 授予容器的讀取權限，或設定容器的 ACL 以允許公用存取。</span><span class="sxs-lookup"><span data-stu-id="1c2ae-146">There are two ways to get such a URL for a container in Azure storage: include a Shared Access Signature (SAS) granting read permissions on the container, or set the ACL for the container to allow public access.</span></span>

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c2ae-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c2ae-147">CommonParameters</span></span>
<span data-ttu-id="1c2ae-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1c2ae-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c2ae-149">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1c2ae-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c2ae-150">輸入</span><span class="sxs-lookup"><span data-stu-id="1c2ae-150">INPUTS</span></span>

### <span data-ttu-id="1c2ae-151">所有</span><span class="sxs-lookup"><span data-stu-id="1c2ae-151">None</span></span>

## <span data-ttu-id="1c2ae-152">輸出</span><span class="sxs-lookup"><span data-stu-id="1c2ae-152">OUTPUTS</span></span>

### <span data-ttu-id="1c2ae-153">Microsoft.Azure.Commands.Batch。PSResourceFile</span><span class="sxs-lookup"><span data-stu-id="1c2ae-153">Microsoft.Azure.Commands.Batch.Models.PSResourceFile</span></span>

## <span data-ttu-id="1c2ae-154">筆記</span><span class="sxs-lookup"><span data-stu-id="1c2ae-154">NOTES</span></span>

## <span data-ttu-id="1c2ae-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="1c2ae-155">RELATED LINKS</span></span>

[<span data-ttu-id="1c2ae-156">新-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="1c2ae-156">New-AzBatchTask</span></span>](./New-AzBatchTask.md)