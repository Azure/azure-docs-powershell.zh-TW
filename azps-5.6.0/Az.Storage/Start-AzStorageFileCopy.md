---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A96A1A67-6C9C-499F-9935-B90F7ACEB50E
online version: https://docs.microsoft.com/powershell/module/az.storage/start-azstoragefilecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageFileCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageFileCopy.md
ms.openlocfilehash: 2b3bea343e5d4e2267c2bec14d60564392914a0d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903941"
---
# <span data-ttu-id="bedf0-101">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="bedf0-101">Start-AzStorageFileCopy</span></span>

## <span data-ttu-id="bedf0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="bedf0-102">SYNOPSIS</span></span>
<span data-ttu-id="bedf0-103">開始複製來源檔案。</span><span class="sxs-lookup"><span data-stu-id="bedf0-103">Starts to copy a source file.</span></span>

## <span data-ttu-id="bedf0-104">語法</span><span class="sxs-lookup"><span data-stu-id="bedf0-104">SYNTAX</span></span>

### <span data-ttu-id="bedf0-105">ContainerName</span><span class="sxs-lookup"><span data-stu-id="bedf0-105">ContainerName</span></span>
```
Start-AzStorageFileCopy -SrcBlobName <String> -SrcContainerName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bedf0-106">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="bedf0-106">ContainerInstance</span></span>
```
Start-AzStorageFileCopy -SrcBlobName <String> -SrcContainer <CloudBlobContainer> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bedf0-107">BlobInstanceFilePath</span><span class="sxs-lookup"><span data-stu-id="bedf0-107">BlobInstanceFilePath</span></span>
```
Start-AzStorageFileCopy -SrcBlob <CloudBlob> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bedf0-108">BlobInstanceFileInstance</span><span class="sxs-lookup"><span data-stu-id="bedf0-108">BlobInstanceFileInstance</span></span>
```
Start-AzStorageFileCopy -SrcBlob <CloudBlob> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bedf0-109">ShareName</span><span class="sxs-lookup"><span data-stu-id="bedf0-109">ShareName</span></span>
```
Start-AzStorageFileCopy -SrcFilePath <String> -SrcShareName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bedf0-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="bedf0-110">ShareInstance</span></span>
```
Start-AzStorageFileCopy -SrcFilePath <String> -SrcShare <CloudFileShare> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bedf0-111">FileInstanceToFilePath</span><span class="sxs-lookup"><span data-stu-id="bedf0-111">FileInstanceToFilePath</span></span>
```
Start-AzStorageFileCopy -SrcFile <CloudFile> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bedf0-112">FileInstanceToFileInstance</span><span class="sxs-lookup"><span data-stu-id="bedf0-112">FileInstanceToFileInstance</span></span>
```
Start-AzStorageFileCopy -SrcFile <CloudFile> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bedf0-113">UriToFilePath</span><span class="sxs-lookup"><span data-stu-id="bedf0-113">UriToFilePath</span></span>
```
Start-AzStorageFileCopy -AbsoluteUri <String> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bedf0-114">UriToFileInstance</span><span class="sxs-lookup"><span data-stu-id="bedf0-114">UriToFileInstance</span></span>
```
Start-AzStorageFileCopy -AbsoluteUri <String> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bedf0-115">描述</span><span class="sxs-lookup"><span data-stu-id="bedf0-115">DESCRIPTION</span></span>
<span data-ttu-id="bedf0-116">**Start-AzStorageFileCopy** Cmdlet 會開始將來源檔案複製到目的地檔案。</span><span class="sxs-lookup"><span data-stu-id="bedf0-116">The **Start-AzStorageFileCopy** cmdlet starts to copy a source file to a destination file.</span></span>

## <span data-ttu-id="bedf0-117">例子</span><span class="sxs-lookup"><span data-stu-id="bedf0-117">EXAMPLES</span></span>

### <span data-ttu-id="bedf0-118">範例 1：使用共用名稱稱和檔案名開始從檔案複製到檔案</span><span class="sxs-lookup"><span data-stu-id="bedf0-118">Example 1: Start copy operation from file to file by using share name and file name</span></span>
```
PS C:\>Start-AzStorageFileCopy -SrcShareName "ContosoShare01" -SrcFilePath "FilePath01" -DestShareName "ContosoShare02" -DestFilePath "FilePath02"
```

<span data-ttu-id="bedf0-119">此命令會啟動從檔案到檔案的複製作業。</span><span class="sxs-lookup"><span data-stu-id="bedf0-119">This command starts a copy operation from file to file.</span></span>
<span data-ttu-id="bedf0-120">命令會指定共用名稱稱和檔案名</span><span class="sxs-lookup"><span data-stu-id="bedf0-120">The command specifies share name and file name</span></span>

### <span data-ttu-id="bedf0-121">範例 2：使用容器名稱和 Blob 名稱，開始從 Blob 到檔案的複製作業</span><span class="sxs-lookup"><span data-stu-id="bedf0-121">Example 2: Start copy operation from blob to file by using container name and blob name</span></span>
```
PS C:\>Start-AzStorageFileCopy -SrcContainerName "ContosoContainer01" -SrcBlobName "ContosoBlob01" -DestShareName "ContosoShare" -DestFilePath "FilePath02"
```

<span data-ttu-id="bedf0-122">此命令會啟動從 Blob 到檔案的複製作業。</span><span class="sxs-lookup"><span data-stu-id="bedf0-122">This command starts a copy operation from blob to file.</span></span>
<span data-ttu-id="bedf0-123">命令會指定容器名稱和 Blob 名稱</span><span class="sxs-lookup"><span data-stu-id="bedf0-123">The command specifies container name and blob name</span></span>

## <span data-ttu-id="bedf0-124">參數</span><span class="sxs-lookup"><span data-stu-id="bedf0-124">PARAMETERS</span></span>

### <span data-ttu-id="bedf0-125">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="bedf0-125">-AbsoluteUri</span></span>
<span data-ttu-id="bedf0-126">指定來源檔案的 URI。</span><span class="sxs-lookup"><span data-stu-id="bedf0-126">Specifies the URI of the source file.</span></span>
<span data-ttu-id="bedf0-127">如果來源位置需要認證，您必須提供認證。</span><span class="sxs-lookup"><span data-stu-id="bedf0-127">If the source location requires a credential, you must provide one.</span></span>

```yaml
Type: System.String
Parameter Sets: UriToFilePath, UriToFileInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bedf0-128">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bedf0-128">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="bedf0-129">指定一個服務要求用戶端的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="bedf0-129">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="bedf0-130">如果前一個通話在指定的時間間隔內失敗，此 Cmdlet 會重新重試要求。</span><span class="sxs-lookup"><span data-stu-id="bedf0-130">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="bedf0-131">如果此 Cmdlet 在間隔經過之前未收到成功回應，此 Cmdlet 會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="bedf0-131">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bedf0-132">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="bedf0-132">-ConcurrentTaskCount</span></span>
<span data-ttu-id="bedf0-133">指定同時進行的最大網路通話數。</span><span class="sxs-lookup"><span data-stu-id="bedf0-133">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="bedf0-134">您可以使用此參數來限制並行，以節流本地 CPU 和頻寬使用量，方法為指定並行網路通話的數量上限。</span><span class="sxs-lookup"><span data-stu-id="bedf0-134">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="bedf0-135">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="bedf0-135">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="bedf0-136">此參數有助於減少低頻寬環境的網路連接問題，例如每秒 100 KB。</span><span class="sxs-lookup"><span data-stu-id="bedf0-136">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="bedf0-137">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="bedf0-137">The default value is 10.</span></span>

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

### <span data-ttu-id="bedf0-138">-內容</span><span class="sxs-lookup"><span data-stu-id="bedf0-138">-Context</span></span>
<span data-ttu-id="bedf0-139">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="bedf0-139">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="bedf0-140">若要取得內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bedf0-140">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerName, ShareName
Aliases: SrcContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bedf0-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bedf0-141">-DefaultProfile</span></span>
<span data-ttu-id="bedf0-142">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="bedf0-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bedf0-143">-DestCoNtext</span><span class="sxs-lookup"><span data-stu-id="bedf0-143">-DestContext</span></span>
<span data-ttu-id="bedf0-144">指定目的地的 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="bedf0-144">Specifies the Azure Storage context of the destination.</span></span>
<span data-ttu-id="bedf0-145">若要取得上下文，請使用 **New-AzStorageCoNtext。**</span><span class="sxs-lookup"><span data-stu-id="bedf0-145">To obtain a context, use **New-AzStorageContext**.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerName, ContainerInstance, BlobInstanceFilePath, ShareName, ShareInstance, FileInstanceToFilePath, UriToFilePath
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bedf0-146">-DestFile</span><span class="sxs-lookup"><span data-stu-id="bedf0-146">-DestFile</span></span>
<span data-ttu-id="bedf0-147">指定 **CloudFile** 物件。</span><span class="sxs-lookup"><span data-stu-id="bedf0-147">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="bedf0-148">您可以使用 Cmdlet 建立雲端檔案，或取得Get-AzStorageFile檔案。</span><span class="sxs-lookup"><span data-stu-id="bedf0-148">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: BlobInstanceFileInstance, FileInstanceToFileInstance, UriToFileInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bedf0-149">-DestFilePath</span><span class="sxs-lookup"><span data-stu-id="bedf0-149">-DestFilePath</span></span>
<span data-ttu-id="bedf0-150">指定目的地檔案相對於目的地共用的路徑。</span><span class="sxs-lookup"><span data-stu-id="bedf0-150">Specifies the path of the destination file relative to the destination share.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, ContainerInstance, BlobInstanceFilePath, ShareName, ShareInstance, FileInstanceToFilePath, UriToFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bedf0-151">-DestShareName</span><span class="sxs-lookup"><span data-stu-id="bedf0-151">-DestShareName</span></span>
<span data-ttu-id="bedf0-152">指定目的地共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="bedf0-152">Specifies the name of the destination share.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, ContainerInstance, BlobInstanceFilePath, ShareName, ShareInstance, FileInstanceToFilePath, UriToFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bedf0-153">-強制</span><span class="sxs-lookup"><span data-stu-id="bedf0-153">-Force</span></span>
<span data-ttu-id="bedf0-154">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="bedf0-154">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bedf0-155">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bedf0-155">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="bedf0-156">指定要求的伺服器部分之時間長度。</span><span class="sxs-lookup"><span data-stu-id="bedf0-156">Specifies the length of the time-out period for the server part of a request.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bedf0-157">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="bedf0-157">-SrcBlob</span></span>
<span data-ttu-id="bedf0-158">指定 **CloudBlob** 物件。</span><span class="sxs-lookup"><span data-stu-id="bedf0-158">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="bedf0-159">您可以使用 Cmdlet 建立雲端 blob 或取得Get-AzStorageBlob Blob。</span><span class="sxs-lookup"><span data-stu-id="bedf0-159">You can create a cloud blob or obtain one by using the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstanceFilePath, BlobInstanceFileInstance
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bedf0-160">-SrcBlobName</span><span class="sxs-lookup"><span data-stu-id="bedf0-160">-SrcBlobName</span></span>
<span data-ttu-id="bedf0-161">指定來源 Blob 的名稱。</span><span class="sxs-lookup"><span data-stu-id="bedf0-161">Specifies the name of the source blob.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, ContainerInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bedf0-162">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="bedf0-162">-SrcContainer</span></span>
<span data-ttu-id="bedf0-163">指定雲端 Blob 容器物件。</span><span class="sxs-lookup"><span data-stu-id="bedf0-163">Specifies a cloud blob container object.</span></span>
<span data-ttu-id="bedf0-164">您可以建立雲端 Blob 容器物件，或使用 Get-AzStorageContainer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bedf0-164">You can create cloud blob container object or use the Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bedf0-165">-SrcContainerName</span><span class="sxs-lookup"><span data-stu-id="bedf0-165">-SrcContainerName</span></span>
<span data-ttu-id="bedf0-166">指定來源容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="bedf0-166">Specifies the name of the source container.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bedf0-167">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="bedf0-167">-SrcFile</span></span>
<span data-ttu-id="bedf0-168">指定 **CloudFile** 物件。</span><span class="sxs-lookup"><span data-stu-id="bedf0-168">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="bedf0-169">您可以建立雲端檔案，或使用 **Get-AzStorageFile 取得一個**。</span><span class="sxs-lookup"><span data-stu-id="bedf0-169">You can create a cloud file or obtain one by using **Get-AzStorageFile**.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileInstanceToFilePath, FileInstanceToFileInstance
Aliases: CloudFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bedf0-170">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="bedf0-170">-SrcFilePath</span></span>
<span data-ttu-id="bedf0-171">指定來源檔案相對於來原始目錄或來源共用的路徑。</span><span class="sxs-lookup"><span data-stu-id="bedf0-171">Specifies the path of the source file relative to the source directory or source share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, ShareInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bedf0-172">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="bedf0-172">-SrcShare</span></span>
<span data-ttu-id="bedf0-173">指定雲端檔案共用物件。</span><span class="sxs-lookup"><span data-stu-id="bedf0-173">Specifies a cloud file share object.</span></span>
<span data-ttu-id="bedf0-174">您可以使用 Cmdlet 建立雲端檔案共用，或Get-AzStorageShare共用。</span><span class="sxs-lookup"><span data-stu-id="bedf0-174">You can create a cloud file share or obtain one by using the Get-AzStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: ShareInstance
Aliases: CloudFileShare

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bedf0-175">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="bedf0-175">-SrcShareName</span></span>
<span data-ttu-id="bedf0-176">指定來源共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="bedf0-176">Specifies the name of the source share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bedf0-177">-確認</span><span class="sxs-lookup"><span data-stu-id="bedf0-177">-Confirm</span></span>
<span data-ttu-id="bedf0-178">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="bedf0-178">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bedf0-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bedf0-179">-WhatIf</span></span>
<span data-ttu-id="bedf0-180">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bedf0-180">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bedf0-181">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bedf0-181">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bedf0-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bedf0-182">CommonParameters</span></span>
<span data-ttu-id="bedf0-183">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="bedf0-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bedf0-184">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="bedf0-184">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bedf0-185">輸入</span><span class="sxs-lookup"><span data-stu-id="bedf0-185">INPUTS</span></span>

### <span data-ttu-id="bedf0-186">Microsoft.Azure.storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="bedf0-186">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="bedf0-187">Microsoft.Azure.storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="bedf0-187">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="bedf0-188">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="bedf0-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="bedf0-189">輸出</span><span class="sxs-lookup"><span data-stu-id="bedf0-189">OUTPUTS</span></span>

### <span data-ttu-id="bedf0-190">Microsoft.WindowsAzure.Commands.Common.storage.ResourceModel.AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="bedf0-190">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="bedf0-191">筆記</span><span class="sxs-lookup"><span data-stu-id="bedf0-191">NOTES</span></span>

## <span data-ttu-id="bedf0-192">相關連結</span><span class="sxs-lookup"><span data-stu-id="bedf0-192">RELATED LINKS</span></span>

[<span data-ttu-id="bedf0-193">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="bedf0-193">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="bedf0-194">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="bedf0-194">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="bedf0-195">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="bedf0-195">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="bedf0-196">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="bedf0-196">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="bedf0-197">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="bedf0-197">Get-AzStorageFileCopyState</span></span>](./Get-AzStorageFileCopyState.md)

[<span data-ttu-id="bedf0-198">Stop-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="bedf0-198">Stop-AzStorageFileCopy</span></span>](./Stop-AzStorageFileCopy.md)
