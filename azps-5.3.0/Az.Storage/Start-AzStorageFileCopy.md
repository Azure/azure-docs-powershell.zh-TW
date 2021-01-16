---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A96A1A67-6C9C-499F-9935-B90F7ACEB50E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstoragefilecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageFileCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageFileCopy.md
ms.openlocfilehash: 578c32a27f53f586ec8a8013533e42928df48d30
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98286031"
---
# <span data-ttu-id="72453-101">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="72453-101">Start-AzStorageFileCopy</span></span>

## <span data-ttu-id="72453-102">摘要</span><span class="sxs-lookup"><span data-stu-id="72453-102">SYNOPSIS</span></span>
<span data-ttu-id="72453-103">開始複製來源檔案。</span><span class="sxs-lookup"><span data-stu-id="72453-103">Starts to copy a source file.</span></span>

## <span data-ttu-id="72453-104">句法</span><span class="sxs-lookup"><span data-stu-id="72453-104">SYNTAX</span></span>

### <span data-ttu-id="72453-105">容器</span><span class="sxs-lookup"><span data-stu-id="72453-105">ContainerName</span></span>
```
Start-AzStorageFileCopy -SrcBlobName <String> -SrcContainerName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="72453-106">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="72453-106">ContainerInstance</span></span>
```
Start-AzStorageFileCopy -SrcBlobName <String> -SrcContainer <CloudBlobContainer> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72453-107">BlobInstanceFilePath</span><span class="sxs-lookup"><span data-stu-id="72453-107">BlobInstanceFilePath</span></span>
```
Start-AzStorageFileCopy -SrcBlob <CloudBlob> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72453-108">BlobInstanceFileInstance</span><span class="sxs-lookup"><span data-stu-id="72453-108">BlobInstanceFileInstance</span></span>
```
Start-AzStorageFileCopy -SrcBlob <CloudBlob> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72453-109">名</span><span class="sxs-lookup"><span data-stu-id="72453-109">ShareName</span></span>
```
Start-AzStorageFileCopy -SrcFilePath <String> -SrcShareName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="72453-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="72453-110">ShareInstance</span></span>
```
Start-AzStorageFileCopy -SrcFilePath <String> -SrcShare <CloudFileShare> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72453-111">FileInstanceToFilePath</span><span class="sxs-lookup"><span data-stu-id="72453-111">FileInstanceToFilePath</span></span>
```
Start-AzStorageFileCopy -SrcFile <CloudFile> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72453-112">FileInstanceToFileInstance</span><span class="sxs-lookup"><span data-stu-id="72453-112">FileInstanceToFileInstance</span></span>
```
Start-AzStorageFileCopy -SrcFile <CloudFile> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72453-113">UriToFilePath</span><span class="sxs-lookup"><span data-stu-id="72453-113">UriToFilePath</span></span>
```
Start-AzStorageFileCopy -AbsoluteUri <String> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72453-114">UriToFileInstance</span><span class="sxs-lookup"><span data-stu-id="72453-114">UriToFileInstance</span></span>
```
Start-AzStorageFileCopy -AbsoluteUri <String> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72453-115">說明</span><span class="sxs-lookup"><span data-stu-id="72453-115">DESCRIPTION</span></span>
<span data-ttu-id="72453-116">**AzStorageFileCopy** Cmdlet 會開始將來源檔案複製到目的地檔案。</span><span class="sxs-lookup"><span data-stu-id="72453-116">The **Start-AzStorageFileCopy** cmdlet starts to copy a source file to a destination file.</span></span>

## <span data-ttu-id="72453-117">示例</span><span class="sxs-lookup"><span data-stu-id="72453-117">EXAMPLES</span></span>

### <span data-ttu-id="72453-118">範例1：使用共用名稱稱和檔案名從檔案開始複製操作</span><span class="sxs-lookup"><span data-stu-id="72453-118">Example 1: Start copy operation from file to file by using share name and file name</span></span>
```
PS C:\>Start-AzStorageFileCopy -SrcShareName "ContosoShare01" -SrcFilePath "FilePath01" -DestShareName "ContosoShare02" -DestFilePath "FilePath02"
```

<span data-ttu-id="72453-119">這個命令會啟動從檔案到檔案的複製操作。</span><span class="sxs-lookup"><span data-stu-id="72453-119">This command starts a copy operation from file to file.</span></span>
<span data-ttu-id="72453-120">命令會指定共用名稱稱和檔案名</span><span class="sxs-lookup"><span data-stu-id="72453-120">The command specifies share name and file name</span></span>

### <span data-ttu-id="72453-121">範例2：使用容器名稱和 blob 名稱從 blob 開始複製作業至檔案</span><span class="sxs-lookup"><span data-stu-id="72453-121">Example 2: Start copy operation from blob to file by using container name and blob name</span></span>
```
PS C:\>Start-AzStorageFileCopy -SrcContainerName "ContosoContainer01" -SrcBlobName "ContosoBlob01" -DestShareName "ContosoShare" -DestFilePath "FilePath02"
```

<span data-ttu-id="72453-122">這個命令會啟動從 blob 到檔案的複製作業。</span><span class="sxs-lookup"><span data-stu-id="72453-122">This command starts a copy operation from blob to file.</span></span>
<span data-ttu-id="72453-123">命令會指定容器名稱及 blob 名稱</span><span class="sxs-lookup"><span data-stu-id="72453-123">The command specifies container name and blob name</span></span>

## <span data-ttu-id="72453-124">參數</span><span class="sxs-lookup"><span data-stu-id="72453-124">PARAMETERS</span></span>

### <span data-ttu-id="72453-125">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="72453-125">-AbsoluteUri</span></span>
<span data-ttu-id="72453-126">指定來源檔案的 URI。</span><span class="sxs-lookup"><span data-stu-id="72453-126">Specifies the URI of the source file.</span></span>
<span data-ttu-id="72453-127">如果來源位置需要身分憑證，您必須提供認證。</span><span class="sxs-lookup"><span data-stu-id="72453-127">If the source location requires a credential, you must provide one.</span></span>

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

### <span data-ttu-id="72453-128">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="72453-128">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="72453-129">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="72453-129">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="72453-130">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="72453-130">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="72453-131">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="72453-131">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="72453-132">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="72453-132">-ConcurrentTaskCount</span></span>
<span data-ttu-id="72453-133">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="72453-133">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="72453-134">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="72453-134">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="72453-135">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="72453-135">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="72453-136">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="72453-136">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="72453-137">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="72453-137">The default value is 10.</span></span>

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

### <span data-ttu-id="72453-138">-內容</span><span class="sxs-lookup"><span data-stu-id="72453-138">-Context</span></span>
<span data-ttu-id="72453-139">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="72453-139">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="72453-140">若要取得內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="72453-140">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="72453-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72453-141">-DefaultProfile</span></span>
<span data-ttu-id="72453-142">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="72453-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72453-143">-DestCoNtext</span><span class="sxs-lookup"><span data-stu-id="72453-143">-DestContext</span></span>
<span data-ttu-id="72453-144">指定目的地的 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="72453-144">Specifies the Azure Storage context of the destination.</span></span>
<span data-ttu-id="72453-145">若要取得內容，請使用 **新的-AzStorageCoNtext**。</span><span class="sxs-lookup"><span data-stu-id="72453-145">To obtain a context, use **New-AzStorageContext**.</span></span>

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

### <span data-ttu-id="72453-146">-DestFile</span><span class="sxs-lookup"><span data-stu-id="72453-146">-DestFile</span></span>
<span data-ttu-id="72453-147">指定 **CloudFile** 物件。</span><span class="sxs-lookup"><span data-stu-id="72453-147">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="72453-148">您可以使用 Get-AzStorageFile Cmdlet 來建立雲端檔案或取得一個雲端檔案。</span><span class="sxs-lookup"><span data-stu-id="72453-148">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="72453-149">-DestFilePath</span><span class="sxs-lookup"><span data-stu-id="72453-149">-DestFilePath</span></span>
<span data-ttu-id="72453-150">指定目標檔案相對於目的地共用的路徑。</span><span class="sxs-lookup"><span data-stu-id="72453-150">Specifies the path of the destination file relative to the destination share.</span></span>

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

### <span data-ttu-id="72453-151">-DestShareName</span><span class="sxs-lookup"><span data-stu-id="72453-151">-DestShareName</span></span>
<span data-ttu-id="72453-152">指定目的地共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="72453-152">Specifies the name of the destination share.</span></span>

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

### <span data-ttu-id="72453-153">-Force</span><span class="sxs-lookup"><span data-stu-id="72453-153">-Force</span></span>
<span data-ttu-id="72453-154">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="72453-154">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="72453-155">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="72453-155">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="72453-156">指定要求中伺服器部分的超時時間長度。</span><span class="sxs-lookup"><span data-stu-id="72453-156">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="72453-157">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="72453-157">-SrcBlob</span></span>
<span data-ttu-id="72453-158">指定 **CloudBlob** 物件。</span><span class="sxs-lookup"><span data-stu-id="72453-158">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="72453-159">您可以使用 Get-AzStorageBlob Cmdlet 來建立雲端 blob 或取得一個。</span><span class="sxs-lookup"><span data-stu-id="72453-159">You can create a cloud blob or obtain one by using the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="72453-160">-SrcBlobName</span><span class="sxs-lookup"><span data-stu-id="72453-160">-SrcBlobName</span></span>
<span data-ttu-id="72453-161">指定來源 blob 的名稱。</span><span class="sxs-lookup"><span data-stu-id="72453-161">Specifies the name of the source blob.</span></span>

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

### <span data-ttu-id="72453-162">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="72453-162">-SrcContainer</span></span>
<span data-ttu-id="72453-163">指定雲端 blob 容器物件。</span><span class="sxs-lookup"><span data-stu-id="72453-163">Specifies a cloud blob container object.</span></span>
<span data-ttu-id="72453-164">您可以建立雲端 blob 容器物件或使用 Get-AzStorageContainer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="72453-164">You can create cloud blob container object or use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="72453-165">-SrcContainerName</span><span class="sxs-lookup"><span data-stu-id="72453-165">-SrcContainerName</span></span>
<span data-ttu-id="72453-166">指定來源容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="72453-166">Specifies the name of the source container.</span></span>

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

### <span data-ttu-id="72453-167">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="72453-167">-SrcFile</span></span>
<span data-ttu-id="72453-168">指定 **CloudFile** 物件。</span><span class="sxs-lookup"><span data-stu-id="72453-168">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="72453-169">您可以使用 **AzStorageFile** 建立雲端檔案或取得一個雲端檔案。</span><span class="sxs-lookup"><span data-stu-id="72453-169">You can create a cloud file or obtain one by using **Get-AzStorageFile**.</span></span>

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

### <span data-ttu-id="72453-170">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="72453-170">-SrcFilePath</span></span>
<span data-ttu-id="72453-171">指定相對於來原始目錄或來源共用的來源檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="72453-171">Specifies the path of the source file relative to the source directory or source share.</span></span>

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

### <span data-ttu-id="72453-172">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="72453-172">-SrcShare</span></span>
<span data-ttu-id="72453-173">指定雲端檔案共用物件。</span><span class="sxs-lookup"><span data-stu-id="72453-173">Specifies a cloud file share object.</span></span>
<span data-ttu-id="72453-174">您可以使用 Get-AzStorageShare Cmdlet 來建立雲端檔案共用或取得一個共用檔案。</span><span class="sxs-lookup"><span data-stu-id="72453-174">You can create a cloud file share or obtain one by using the Get-AzStorageShare cmdlet.</span></span>

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

### <span data-ttu-id="72453-175">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="72453-175">-SrcShareName</span></span>
<span data-ttu-id="72453-176">指定來源共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="72453-176">Specifies the name of the source share.</span></span>

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

### <span data-ttu-id="72453-177">-確認</span><span class="sxs-lookup"><span data-stu-id="72453-177">-Confirm</span></span>
<span data-ttu-id="72453-178">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="72453-178">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72453-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72453-179">-WhatIf</span></span>
<span data-ttu-id="72453-180">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="72453-180">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72453-181">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="72453-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72453-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72453-182">CommonParameters</span></span>
<span data-ttu-id="72453-183">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="72453-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72453-184">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="72453-184">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72453-185">輸入</span><span class="sxs-lookup"><span data-stu-id="72453-185">INPUTS</span></span>

### <span data-ttu-id="72453-186">[CloudBlob]。</span><span class="sxs-lookup"><span data-stu-id="72453-186">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="72453-187">CloudFile （即 Azure）</span><span class="sxs-lookup"><span data-stu-id="72453-187">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="72453-188">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="72453-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="72453-189">輸出</span><span class="sxs-lookup"><span data-stu-id="72453-189">OUTPUTS</span></span>

### <span data-ttu-id="72453-190">AzureStorageFile WindowsAzure. ResourceModel。</span><span class="sxs-lookup"><span data-stu-id="72453-190">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="72453-191">筆記</span><span class="sxs-lookup"><span data-stu-id="72453-191">NOTES</span></span>

## <span data-ttu-id="72453-192">相關連結</span><span class="sxs-lookup"><span data-stu-id="72453-192">RELATED LINKS</span></span>

[<span data-ttu-id="72453-193">AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="72453-193">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="72453-194">AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="72453-194">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="72453-195">AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="72453-195">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="72453-196">AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="72453-196">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="72453-197">AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="72453-197">Get-AzStorageFileCopyState</span></span>](./Get-AzStorageFileCopyState.md)

[<span data-ttu-id="72453-198">停止 AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="72453-198">Stop-AzStorageFileCopy</span></span>](./Stop-AzStorageFileCopy.md)
