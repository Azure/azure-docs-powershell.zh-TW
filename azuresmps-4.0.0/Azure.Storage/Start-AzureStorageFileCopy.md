---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: A96A1A67-6C9C-499F-9935-B90F7ACEB50E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 279e5f8e74ec46135e771f2b8446a5e0d2e959f2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443535"
---
# <span data-ttu-id="cbadc-101">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="cbadc-101">Start-AzureStorageFileCopy</span></span>

## <span data-ttu-id="cbadc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cbadc-102">SYNOPSIS</span></span>
<span data-ttu-id="cbadc-103">開始複製來源檔案。</span><span class="sxs-lookup"><span data-stu-id="cbadc-103">Starts to copy a source file.</span></span>

## <span data-ttu-id="cbadc-104">句法</span><span class="sxs-lookup"><span data-stu-id="cbadc-104">SYNTAX</span></span>

### <span data-ttu-id="cbadc-105">容器</span><span class="sxs-lookup"><span data-stu-id="cbadc-105">ContainerName</span></span>
```
Start-AzureStorageFileCopy -SrcBlobName <String> -SrcContainerName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbadc-106">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="cbadc-106">ContainerInstance</span></span>
```
Start-AzureStorageFileCopy -SrcBlobName <String> -SrcContainer <CloudBlobContainer> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbadc-107">BlobInstanceFilePath</span><span class="sxs-lookup"><span data-stu-id="cbadc-107">BlobInstanceFilePath</span></span>
```
Start-AzureStorageFileCopy -SrcBlob <CloudBlob> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbadc-108">BlobInstanceFileInstance</span><span class="sxs-lookup"><span data-stu-id="cbadc-108">BlobInstanceFileInstance</span></span>
```
Start-AzureStorageFileCopy -SrcBlob <CloudBlob> -DestFile <CloudFile> [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbadc-109">名</span><span class="sxs-lookup"><span data-stu-id="cbadc-109">ShareName</span></span>
```
Start-AzureStorageFileCopy -SrcFilePath <String> -SrcShareName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbadc-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="cbadc-110">ShareInstance</span></span>
```
Start-AzureStorageFileCopy -SrcFilePath <String> -SrcShare <CloudFileShare> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbadc-111">FileInstanceToFilePath</span><span class="sxs-lookup"><span data-stu-id="cbadc-111">FileInstanceToFilePath</span></span>
```
Start-AzureStorageFileCopy -SrcFile <CloudFile> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbadc-112">FileInstanceToFileInstance</span><span class="sxs-lookup"><span data-stu-id="cbadc-112">FileInstanceToFileInstance</span></span>
```
Start-AzureStorageFileCopy -SrcFile <CloudFile> -DestFile <CloudFile> [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbadc-113">UriToFilePath</span><span class="sxs-lookup"><span data-stu-id="cbadc-113">UriToFilePath</span></span>
```
Start-AzureStorageFileCopy -AbsoluteUri <String> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbadc-114">UriToFileInstance</span><span class="sxs-lookup"><span data-stu-id="cbadc-114">UriToFileInstance</span></span>
```
Start-AzureStorageFileCopy -AbsoluteUri <String> -DestFile <CloudFile> [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbadc-115">說明</span><span class="sxs-lookup"><span data-stu-id="cbadc-115">DESCRIPTION</span></span>
<span data-ttu-id="cbadc-116">**AzureStorageFileCopy** Cmdlet 會開始將來源檔案複製到目的地檔案。</span><span class="sxs-lookup"><span data-stu-id="cbadc-116">The **Start-AzureStorageFileCopy** cmdlet starts to copy a source file to a destination file.</span></span>

## <span data-ttu-id="cbadc-117">示例</span><span class="sxs-lookup"><span data-stu-id="cbadc-117">EXAMPLES</span></span>

### <span data-ttu-id="cbadc-118">範例1：使用共用名稱稱和檔案名從檔案開始複製操作</span><span class="sxs-lookup"><span data-stu-id="cbadc-118">Example 1: Start copy operation from file to file by using share name and file name</span></span>
```
PS C:\>Start-AzureStorageFileCopy -SrcShareName "ContosoShare01" -SrcFilePath "FilePath01" -DestShareName "ContosoShare02" -DestFilePath "FilePath02"
```

<span data-ttu-id="cbadc-119">這個命令會啟動從檔案到檔案的複製操作。</span><span class="sxs-lookup"><span data-stu-id="cbadc-119">This command starts a copy operation from file to file.</span></span>
<span data-ttu-id="cbadc-120">命令會指定共用名稱稱和檔案名</span><span class="sxs-lookup"><span data-stu-id="cbadc-120">The command specifies share name and file name</span></span>

### <span data-ttu-id="cbadc-121">範例2：使用容器名稱和 blob 名稱從 blob 開始複製作業至檔案</span><span class="sxs-lookup"><span data-stu-id="cbadc-121">Example 2: Start copy operation from blob to file by using container name and blob name</span></span>
```
PS C:\>Start-AzureStorageFileCopy -SrcContainerName "ContosoContainer01" -SrcBlobName "ContosoBlob01" -DestShareName "ContosoShare" -DestFilePath "FilePath02"
```

<span data-ttu-id="cbadc-122">這個命令會啟動從 blob 到檔案的複製作業。</span><span class="sxs-lookup"><span data-stu-id="cbadc-122">This command starts a copy operation from blob to file.</span></span>
<span data-ttu-id="cbadc-123">命令會指定容器名稱及 blob 名稱</span><span class="sxs-lookup"><span data-stu-id="cbadc-123">The command specifies container name and blob name</span></span>

## <span data-ttu-id="cbadc-124">參數</span><span class="sxs-lookup"><span data-stu-id="cbadc-124">PARAMETERS</span></span>

### <span data-ttu-id="cbadc-125">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="cbadc-125">-AbsoluteUri</span></span>
<span data-ttu-id="cbadc-126">指定來源檔案的 URI。</span><span class="sxs-lookup"><span data-stu-id="cbadc-126">Specifies the URI of the source file.</span></span>
<span data-ttu-id="cbadc-127">如果來源位置需要身分憑證，您必須提供認證。</span><span class="sxs-lookup"><span data-stu-id="cbadc-127">If the source location requires a credential, you must provide one.</span></span>

```yaml
Type: String
Parameter Sets: UriToFilePath, UriToFileInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbadc-128">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cbadc-128">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="cbadc-129">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="cbadc-129">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="cbadc-130">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="cbadc-130">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="cbadc-131">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="cbadc-131">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbadc-132">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="cbadc-132">-ConcurrentTaskCount</span></span>
<span data-ttu-id="cbadc-133">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="cbadc-133">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="cbadc-134">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="cbadc-134">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="cbadc-135">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="cbadc-135">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="cbadc-136">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="cbadc-136">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="cbadc-137">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="cbadc-137">The default value is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbadc-138">-內容</span><span class="sxs-lookup"><span data-stu-id="cbadc-138">-Context</span></span>
<span data-ttu-id="cbadc-139">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="cbadc-139">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="cbadc-140">若要取得內容，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cbadc-140">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ContainerName, ShareName
Aliases: SrcContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbadc-141">-DestCoNtext</span><span class="sxs-lookup"><span data-stu-id="cbadc-141">-DestContext</span></span>
<span data-ttu-id="cbadc-142">指定目的地的 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="cbadc-142">Specifies the Azure Storage context of the destination.</span></span>
<span data-ttu-id="cbadc-143">若要取得內容，請使用 **新的-AzureStorageCoNtext** 。</span><span class="sxs-lookup"><span data-stu-id="cbadc-143">To obtain a context, use **New-AzureStorageContext**.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ContainerName, ContainerInstance, BlobInstanceFilePath, ShareName, ShareInstance, FileInstanceToFilePath, UriToFilePath
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbadc-144">-DestFile</span><span class="sxs-lookup"><span data-stu-id="cbadc-144">-DestFile</span></span>
<span data-ttu-id="cbadc-145">指定 **CloudFile** 物件。</span><span class="sxs-lookup"><span data-stu-id="cbadc-145">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="cbadc-146">您可以使用 Get-AzureStorageFile Cmdlet 來建立雲端檔案或取得一個雲端檔案。</span><span class="sxs-lookup"><span data-stu-id="cbadc-146">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: CloudFile
Parameter Sets: BlobInstanceFileInstance, FileInstanceToFileInstance, UriToFileInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbadc-147">-DestFilePath</span><span class="sxs-lookup"><span data-stu-id="cbadc-147">-DestFilePath</span></span>
<span data-ttu-id="cbadc-148">指定目標檔案相對於目的地共用的路徑。</span><span class="sxs-lookup"><span data-stu-id="cbadc-148">Specifies the path of the destination file relative to the destination share.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName, ContainerInstance, BlobInstanceFilePath, ShareName, ShareInstance, FileInstanceToFilePath, UriToFilePath
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbadc-149">-DestShareName</span><span class="sxs-lookup"><span data-stu-id="cbadc-149">-DestShareName</span></span>
<span data-ttu-id="cbadc-150">指定目的地共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="cbadc-150">Specifies the name of the destination share.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName, ContainerInstance, BlobInstanceFilePath, ShareName, ShareInstance, FileInstanceToFilePath, UriToFilePath
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbadc-151">-Force</span><span class="sxs-lookup"><span data-stu-id="cbadc-151">-Force</span></span>
<span data-ttu-id="cbadc-152">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="cbadc-152">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbadc-153">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cbadc-153">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="cbadc-154">指定要求中伺服器部分的超時時間長度。</span><span class="sxs-lookup"><span data-stu-id="cbadc-154">Specifies the length of the time-out period for the server part of a request.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbadc-155">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="cbadc-155">-SrcBlob</span></span>
<span data-ttu-id="cbadc-156">指定 **CloudBlob** 物件。</span><span class="sxs-lookup"><span data-stu-id="cbadc-156">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="cbadc-157">您可以使用 Get-AzureStorageBlob Cmdlet 來建立雲端 blob 或取得一個。</span><span class="sxs-lookup"><span data-stu-id="cbadc-157">You can create a cloud blob or obtain one by using the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobInstanceFilePath, BlobInstanceFileInstance
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cbadc-158">-SrcBlobName</span><span class="sxs-lookup"><span data-stu-id="cbadc-158">-SrcBlobName</span></span>
<span data-ttu-id="cbadc-159">指定來源 blob 的名稱。</span><span class="sxs-lookup"><span data-stu-id="cbadc-159">Specifies the name of the source blob.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName, ContainerInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbadc-160">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="cbadc-160">-SrcContainer</span></span>
<span data-ttu-id="cbadc-161">指定雲端 blob 容器物件。</span><span class="sxs-lookup"><span data-stu-id="cbadc-161">Specifies a cloud blob container object.</span></span>
<span data-ttu-id="cbadc-162">您可以建立雲端 blob 容器物件或使用 Get-AzureStorageContainer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cbadc-162">You can create cloud blob container object or use the Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbadc-163">-SrcContainerName</span><span class="sxs-lookup"><span data-stu-id="cbadc-163">-SrcContainerName</span></span>
<span data-ttu-id="cbadc-164">指定來源容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="cbadc-164">Specifies the name of the source container.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbadc-165">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="cbadc-165">-SrcFile</span></span>
<span data-ttu-id="cbadc-166">指定 **CloudFile** 物件。</span><span class="sxs-lookup"><span data-stu-id="cbadc-166">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="cbadc-167">您可以使用 **AzureStorageFile** 建立雲端檔案或取得一個雲端檔案。</span><span class="sxs-lookup"><span data-stu-id="cbadc-167">You can create a cloud file or obtain one by using **Get-AzureStorageFile**.</span></span>

```yaml
Type: CloudFile
Parameter Sets: FileInstanceToFilePath, FileInstanceToFileInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cbadc-168">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="cbadc-168">-SrcFilePath</span></span>
<span data-ttu-id="cbadc-169">指定相對於來原始目錄或來源共用的來源檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="cbadc-169">Specifies the path of the source file relative to the source directory or source share.</span></span>

```yaml
Type: String
Parameter Sets: ShareName, ShareInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbadc-170">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="cbadc-170">-SrcShare</span></span>
<span data-ttu-id="cbadc-171">指定雲端檔案共用物件。</span><span class="sxs-lookup"><span data-stu-id="cbadc-171">Specifies a cloud file share object.</span></span>
<span data-ttu-id="cbadc-172">您可以使用 Get-AzureStorageShare Cmdlet 來建立雲端檔案共用或取得一個共用檔案。</span><span class="sxs-lookup"><span data-stu-id="cbadc-172">You can create a cloud file share or obtain one by using the Get-AzureStorageShare cmdlet.</span></span>

```yaml
Type: CloudFileShare
Parameter Sets: ShareInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbadc-173">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="cbadc-173">-SrcShareName</span></span>
<span data-ttu-id="cbadc-174">指定來源共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="cbadc-174">Specifies the name of the source share.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbadc-175">-確認</span><span class="sxs-lookup"><span data-stu-id="cbadc-175">-Confirm</span></span>
<span data-ttu-id="cbadc-176">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cbadc-176">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbadc-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbadc-177">-WhatIf</span></span>
<span data-ttu-id="cbadc-178">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cbadc-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbadc-179">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cbadc-179">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbadc-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbadc-180">CommonParameters</span></span>
<span data-ttu-id="cbadc-181">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cbadc-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbadc-182">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cbadc-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbadc-183">輸入</span><span class="sxs-lookup"><span data-stu-id="cbadc-183">INPUTS</span></span>

## <span data-ttu-id="cbadc-184">輸出</span><span class="sxs-lookup"><span data-stu-id="cbadc-184">OUTPUTS</span></span>

## <span data-ttu-id="cbadc-185">筆記</span><span class="sxs-lookup"><span data-stu-id="cbadc-185">NOTES</span></span>

## <span data-ttu-id="cbadc-186">相關連結</span><span class="sxs-lookup"><span data-stu-id="cbadc-186">RELATED LINKS</span></span>

[<span data-ttu-id="cbadc-187">AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="cbadc-187">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="cbadc-188">AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="cbadc-188">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="cbadc-189">AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="cbadc-189">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="cbadc-190">AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="cbadc-190">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="cbadc-191">AzureStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="cbadc-191">Get-AzureStorageFileCopyState</span></span>](./Get-AzureStorageFileCopyState.md)

[<span data-ttu-id="cbadc-192">停止 AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="cbadc-192">Stop-AzureStorageFileCopy</span></span>](./Stop-AzureStorageFileCopy.md)
