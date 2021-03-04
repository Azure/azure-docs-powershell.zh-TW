---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/powershell/module/az.batch/new-azbatchresourcefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
ms.openlocfilehash: f8df4d49f0181b7cf8abf2581a522f953f3f2df7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916289"
---
# <span data-ttu-id="3b49a-101">New-AzBatchResourceFile</span><span class="sxs-lookup"><span data-stu-id="3b49a-101">New-AzBatchResourceFile</span></span>

## <span data-ttu-id="3b49a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3b49a-102">SYNOPSIS</span></span>
<span data-ttu-id="3b49a-103">建立資源檔案供使用 `New-AzBatchTask` 。</span><span class="sxs-lookup"><span data-stu-id="3b49a-103">Creates a Resource File for usage by `New-AzBatchTask`.</span></span>

## <span data-ttu-id="3b49a-104">語法</span><span class="sxs-lookup"><span data-stu-id="3b49a-104">SYNTAX</span></span>

### <span data-ttu-id="3b49a-105">HTTPUrl (預設) </span><span class="sxs-lookup"><span data-stu-id="3b49a-105">HttpUrl (Default)</span></span>
```
New-AzBatchResourceFile -HttpUrl <String> -FilePath <String> [-FileMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b49a-106">StorageContainerUrl</span><span class="sxs-lookup"><span data-stu-id="3b49a-106">StorageContainerUrl</span></span>
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] [-BlobPrefix <String>]
 -StorageContainerUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b49a-107">AutoStorageContainerName</span><span class="sxs-lookup"><span data-stu-id="3b49a-107">AutoStorageContainerName</span></span>
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] -AutoStorageContainerName <String>
 [-BlobPrefix <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b49a-108">描述</span><span class="sxs-lookup"><span data-stu-id="3b49a-108">DESCRIPTION</span></span>
<span data-ttu-id="3b49a-109">建立資源檔案供使用 `New-AzBatchTask` 。</span><span class="sxs-lookup"><span data-stu-id="3b49a-109">Creates a Resource File for usage by `New-AzBatchTask`.</span></span>

## <span data-ttu-id="3b49a-110">例子</span><span class="sxs-lookup"><span data-stu-id="3b49a-110">EXAMPLES</span></span>

### <span data-ttu-id="3b49a-111">範例 1：從指向單一檔案的 HTTP URL 建立資源檔案</span><span class="sxs-lookup"><span data-stu-id="3b49a-111">Example 1: Create a resource file from an HTTP URL pointing at a single file</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -HttpUrl "https://testacct.blob.core.windows.net/" -FilePath "file1"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="3b49a-112">建立參照 `PSResourceFile` HTTP URL。</span><span class="sxs-lookup"><span data-stu-id="3b49a-112">Creates a `PSResourceFile` referencing an HTTP url.</span></span>

### <span data-ttu-id="3b49a-113">範例 2：從 Azure 儲存容器 URL 建立資源檔案</span><span class="sxs-lookup"><span data-stu-id="3b49a-113">Example 2: Create a resource file from an Azure Storage container URL</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -StorageContainerUrl "https://testacct.blob.core.windows.net/mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="3b49a-114">建立參照 `PSResourceFile` Azure 儲存容器 URL。</span><span class="sxs-lookup"><span data-stu-id="3b49a-114">Creates a `PSResourceFile` referencing an Azure Storage container URL.</span></span> <span data-ttu-id="3b49a-115">容器中的所有檔案都會下載到指定的資料夾。</span><span class="sxs-lookup"><span data-stu-id="3b49a-115">All files in the container will be downloaded to the specified folder.</span></span>

### <span data-ttu-id="3b49a-116">範例 3：從自動儲存容器名稱建立資源檔案</span><span class="sxs-lookup"><span data-stu-id="3b49a-116">Example 3: Create a resource file from an Auto Storage container name</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -AutoStorageContainerName "mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="3b49a-117">建立參照 `PSResourceFile` 自動儲存容器名稱。</span><span class="sxs-lookup"><span data-stu-id="3b49a-117">Creates a `PSResourceFile` referencing an Auto Storage container name.</span></span> <span data-ttu-id="3b49a-118">容器中的所有檔案都會下載到指定的資料夾。</span><span class="sxs-lookup"><span data-stu-id="3b49a-118">All files in the container will be downloaded to the specified folder.</span></span>

## <span data-ttu-id="3b49a-119">參數</span><span class="sxs-lookup"><span data-stu-id="3b49a-119">PARAMETERS</span></span>

### <span data-ttu-id="3b49a-120">-AutoStorageContainerName</span><span class="sxs-lookup"><span data-stu-id="3b49a-120">-AutoStorageContainerName</span></span>
<span data-ttu-id="3b49a-121">自動儲存帳戶中的儲存容器名稱。</span><span class="sxs-lookup"><span data-stu-id="3b49a-121">The storage container name in the auto storage account.</span></span>

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

### <span data-ttu-id="3b49a-122">-BlobPrefix</span><span class="sxs-lookup"><span data-stu-id="3b49a-122">-BlobPrefix</span></span>
<span data-ttu-id="3b49a-123">從 Azure 儲存容器下載 Blob 時，使用 Blob 首碼。</span><span class="sxs-lookup"><span data-stu-id="3b49a-123">Gets the blob prefix to use when downloading blobs from an Azure Storage container.</span></span>
<span data-ttu-id="3b49a-124">只有名稱以指定首碼開頭的 Blob 會下載。</span><span class="sxs-lookup"><span data-stu-id="3b49a-124">Only the blobs whose names begin with the specified prefix will be downloaded.</span></span>
<span data-ttu-id="3b49a-125">此首碼可以是部分檔案名或子目錄。</span><span class="sxs-lookup"><span data-stu-id="3b49a-125">This prefix can be a partial filename or a subdirectory.</span></span>
<span data-ttu-id="3b49a-126">如果未指定首碼，將會下載容器中的所有檔案。</span><span class="sxs-lookup"><span data-stu-id="3b49a-126">If a prefix is not specified, all the files in the container will be downloaded.</span></span>

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

### <span data-ttu-id="3b49a-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b49a-127">-DefaultProfile</span></span>
<span data-ttu-id="3b49a-128">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3b49a-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b49a-129">-FileMode</span><span class="sxs-lookup"><span data-stu-id="3b49a-129">-FileMode</span></span>
<span data-ttu-id="3b49a-130">以八進位格式獲得檔案許可權模式屬性。</span><span class="sxs-lookup"><span data-stu-id="3b49a-130">Gets the file permission mode attribute in octal format.</span></span>
<span data-ttu-id="3b49a-131">只有在資源檔案下載到 Linux 節點時，此屬性才適用。</span><span class="sxs-lookup"><span data-stu-id="3b49a-131">This property is applicable only if the resource file is downloaded to a Linux node.</span></span>
<span data-ttu-id="3b49a-132">如果未指定 Linux 節點的此屬性，預設值為 0770。</span><span class="sxs-lookup"><span data-stu-id="3b49a-132">If this property is not specified for a Linux node, then the default value is 0770.</span></span>

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

### <span data-ttu-id="3b49a-133">-FilePath</span><span class="sxs-lookup"><span data-stu-id="3b49a-133">-FilePath</span></span>
<span data-ttu-id="3b49a-134">計算節點上下載檔案的位置 (工作) 的工作目錄。</span><span class="sxs-lookup"><span data-stu-id="3b49a-134">The location on the compute node to which to download the file(s), relative to the task's working directory.</span></span> <span data-ttu-id="3b49a-135">如果已指定 HttpUrl 參數，則 FilePath 為必填專案，並說明要下載檔案的路徑，包括檔案名。</span><span class="sxs-lookup"><span data-stu-id="3b49a-135">If the HttpUrl parameter is specified, the FilePath is required and describes the path which the file will be downloaded to, including the filename.</span></span> <span data-ttu-id="3b49a-136">否則，如果已指定 AutoStorageContainerName 或 StorageContainerUrl 參數，則 FilePath 為選擇性專案，是下載檔案的目錄。</span><span class="sxs-lookup"><span data-stu-id="3b49a-136">Otherwise, if the AutoStorageContainerName or StorageContainerUrl parameters are specified, FilePath is optional and is the directory to download the files to.</span></span> <span data-ttu-id="3b49a-137">使用 FilePath 做為目錄時，任何已與輸入資料相關聯的目錄結構都會保留完整，並附加到指定的 FilePath 目錄。</span><span class="sxs-lookup"><span data-stu-id="3b49a-137">In the case where FilePath is used as a directory, any directory structure already associated with the input data will be retained in full and appended to the specified FilePath directory.</span></span> <span data-ttu-id="3b49a-138">指定的相對路徑無法中斷任務的工作目錄 (例如使用 '.」。) 。</span><span class="sxs-lookup"><span data-stu-id="3b49a-138">The specified relative path cannot break out of the task's working directory (for example by using '..').</span></span>

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

### <span data-ttu-id="3b49a-139">-HTTPUrl</span><span class="sxs-lookup"><span data-stu-id="3b49a-139">-HttpUrl</span></span>
<span data-ttu-id="3b49a-140">要下載之檔案的 URL。</span><span class="sxs-lookup"><span data-stu-id="3b49a-140">The URL of the file to download.</span></span>
<span data-ttu-id="3b49a-141">如果 URL 是 Azure Blob 儲存體，則必須使用匿名存取來讀取 URL;也就是說，批次處理服務不會在下載 Blob 時顯示任何認證。</span><span class="sxs-lookup"><span data-stu-id="3b49a-141">If the URL is Azure Blob Storage, it must be readable using anonymous access; that is, the Batch service does not present any credentials when downloading the blob.</span></span>
<span data-ttu-id="3b49a-142">有兩種方法可以取得 Azure 儲存空間中 Blob 的這類 URL：包含共用存取簽章 (SAS) 以在 Blob 上授予讀取權限，或設定 Blob 的 ACL 或容器以允許公用存取。</span><span class="sxs-lookup"><span data-stu-id="3b49a-142">There are two ways to get such a URL for a blob in Azure storage: include a Shared Access Signature (SAS) granting read permissions on the blob, or set the ACL for the blob or its container to allow public access.</span></span>

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

### <span data-ttu-id="3b49a-143">-StorageContainerUrl</span><span class="sxs-lookup"><span data-stu-id="3b49a-143">-StorageContainerUrl</span></span>
<span data-ttu-id="3b49a-144">Azure Blob 儲存體中 Blob 容器的 URL。</span><span class="sxs-lookup"><span data-stu-id="3b49a-144">The URL of the blob container within Azure Blob Storage.</span></span>
<span data-ttu-id="3b49a-145">此 URL 必須使用匿名存取來可讀取且可列出;也就是說，從容器下載 Blob 時，批次處理服務不會顯示任何認證。</span><span class="sxs-lookup"><span data-stu-id="3b49a-145">This URL must be readable and listable using anonymous access; that is, the Batch service does not present any credentials when downloading blobs from the container.</span></span>
<span data-ttu-id="3b49a-146">有兩種方法可以取得 Azure 儲存空間中容器的這類 URL：包含共用存取簽章 (SAS) 以在容器上授予讀取權限，或設定容器的 ACL 以允許公用存取。</span><span class="sxs-lookup"><span data-stu-id="3b49a-146">There are two ways to get such a URL for a container in Azure storage: include a Shared Access Signature (SAS) granting read permissions on the container, or set the ACL for the container to allow public access.</span></span>

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

### <span data-ttu-id="3b49a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b49a-147">CommonParameters</span></span>
<span data-ttu-id="3b49a-148">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3b49a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b49a-149">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3b49a-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b49a-150">輸入</span><span class="sxs-lookup"><span data-stu-id="3b49a-150">INPUTS</span></span>

### <span data-ttu-id="3b49a-151">沒有</span><span class="sxs-lookup"><span data-stu-id="3b49a-151">None</span></span>

## <span data-ttu-id="3b49a-152">輸出</span><span class="sxs-lookup"><span data-stu-id="3b49a-152">OUTPUTS</span></span>

### <span data-ttu-id="3b49a-153">Microsoft.Azure.Commands.Batch。Models.PSResourceFile</span><span class="sxs-lookup"><span data-stu-id="3b49a-153">Microsoft.Azure.Commands.Batch.Models.PSResourceFile</span></span>

## <span data-ttu-id="3b49a-154">筆記</span><span class="sxs-lookup"><span data-stu-id="3b49a-154">NOTES</span></span>

## <span data-ttu-id="3b49a-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="3b49a-155">RELATED LINKS</span></span>

[<span data-ttu-id="3b49a-156">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="3b49a-156">New-AzBatchTask</span></span>](./New-AzBatchTask.md)