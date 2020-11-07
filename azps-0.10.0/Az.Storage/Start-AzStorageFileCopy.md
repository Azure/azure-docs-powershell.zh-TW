---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A96A1A67-6C9C-499F-9935-B90F7ACEB50E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstoragefilecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Start-AzStorageFileCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Start-AzStorageFileCopy.md
ms.openlocfilehash: 3336820514bbf4a949be2657d5955079efa87fac
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795021"
---
# <span data-ttu-id="9c8d3-101">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="9c8d3-101">Start-AzStorageFileCopy</span></span>

## <span data-ttu-id="9c8d3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9c8d3-102">SYNOPSIS</span></span>
<span data-ttu-id="9c8d3-103">開始複製來源檔案。</span><span class="sxs-lookup"><span data-stu-id="9c8d3-103">Starts to copy a source file.</span></span>

## <span data-ttu-id="9c8d3-104">句法</span><span class="sxs-lookup"><span data-stu-id="9c8d3-104">SYNTAX</span></span>

### <span data-ttu-id="9c8d3-105">容器</span><span class="sxs-lookup"><span data-stu-id="9c8d3-105">ContainerName</span></span>
```
Start-AzStorageFileCopy -SrcBlobName <String> -SrcContainerName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9c8d3-106">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="9c8d3-106">ContainerInstance</span></span>
```
Start-AzStorageFileCopy -SrcBlobName <String> -SrcContainer <CloudBlobContainer> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c8d3-107">BlobInstanceFilePath</span><span class="sxs-lookup"><span data-stu-id="9c8d3-107">BlobInstanceFilePath</span></span>
```
Start-AzStorageFileCopy -SrcBlob <CloudBlob> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c8d3-108">BlobInstanceFileInstance</span><span class="sxs-lookup"><span data-stu-id="9c8d3-108">BlobInstanceFileInstance</span></span>
```
Start-AzStorageFileCopy -SrcBlob <CloudBlob> -DestFile <CloudFile> [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9c8d3-109">名</span><span class="sxs-lookup"><span data-stu-id="9c8d3-109">ShareName</span></span>
```
Start-AzStorageFileCopy -SrcFilePath <String> -SrcShareName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9c8d3-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="9c8d3-110">ShareInstance</span></span>
```
Start-AzStorageFileCopy -SrcFilePath <String> -SrcShare <CloudFileShare> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c8d3-111">FileInstanceToFilePath</span><span class="sxs-lookup"><span data-stu-id="9c8d3-111">FileInstanceToFilePath</span></span>
```
Start-AzStorageFileCopy -SrcFile <CloudFile> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c8d3-112">FileInstanceToFileInstance</span><span class="sxs-lookup"><span data-stu-id="9c8d3-112">FileInstanceToFileInstance</span></span>
```
Start-AzStorageFileCopy -SrcFile <CloudFile> -DestFile <CloudFile> [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9c8d3-113">UriToFilePath</span><span class="sxs-lookup"><span data-stu-id="9c8d3-113">UriToFilePath</span></span>
```
Start-AzStorageFileCopy -AbsoluteUri <String> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c8d3-114">UriToFileInstance</span><span class="sxs-lookup"><span data-stu-id="9c8d3-114">UriToFileInstance</span></span>
```
Start-AzStorageFileCopy -AbsoluteUri <String> -DestFile <CloudFile> [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9c8d3-115">說明</span><span class="sxs-lookup"><span data-stu-id="9c8d3-115">DESCRIPTION</span></span>
<span data-ttu-id="9c8d3-116">**AzStorageFileCopy** Cmdlet 會開始將來源檔案複製到目的地檔案。</span><span class="sxs-lookup"><span data-stu-id="9c8d3-116">The **Start-AzStorageFileCopy** cmdlet starts to copy a source file to a destination file.</span></span>

## <span data-ttu-id="9c8d3-117">示例</span><span class="sxs-lookup"><span data-stu-id="9c8d3-117">EXAMPLES</span></span>

### <span data-ttu-id="9c8d3-118">範例1：使用共用名稱稱和檔案名從檔案開始複製操作</span><span class="sxs-lookup"><span data-stu-id="9c8d3-118">Example 1: Start copy operation from file to file by using share name and file name</span></span>
```
PS C:\>Start-AzStorageFileCopy -SrcShareName "ContosoShare01" -SrcFilePath "FilePath01" -DestShareName "ContosoShare02" -DestFilePath "FilePath02"
```

<span data-ttu-id="9c8d3-119">這個命令會啟動從檔案到檔案的複製操作。</span><span class="sxs-lookup"><span data-stu-id="9c8d3-119">This command starts a copy operation from file to file.</span></span>
<span data-ttu-id="9c8d3-120">命令會指定共用名稱稱和檔案名</span><span class="sxs-lookup"><span data-stu-id="9c8d3-120">The command specifies share name and file name</span></span>

### <span data-ttu-id="9c8d3-121">範例2：使用容器名稱和 blob 名稱從 blob 開始複製作業至檔案</span><span class="sxs-lookup"><span data-stu-id="9c8d3-121">Example 2: Start copy operation from blob to file by using container name and blob name</span></span>
```
PS C:\>Start-AzStorageFileCopy -SrcContainerName "ContosoContainer01" -SrcBlobName "ContosoBlob01" -DestShareName "ContosoShare" -DestFilePath "FilePath02"
```

<span data-ttu-id="9c8d3-122">這個命令會啟動從 blob 到檔案的複製作業。</span><span class="sxs-lookup"><span data-stu-id="9c8d3-122">This command starts a copy operation from blob to file.</span></span>
<span data-ttu-id="9c8d3-123">命令會指定容器名稱及 blob 名稱</span><span class="sxs-lookup"><span data-stu-id="9c8d3-123">The command specifies container name and blob name</span></span>

## <span data-ttu-id="9c8d3-124">參數</span><span class="sxs-lookup"><span data-stu-id="9c8d3-124">PARAMETERS</span></span>

### <span data-ttu-id="9c8d3-125">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="9c8d3-125">-AbsoluteUri</span></span>
<span data-ttu-id="9c8d3-126">指定來源檔案的 URI。</span><span class="sxs-lookup"><span data-stu-id="9c8d3-126">Specifies the URI of the source file.</span></span>
<span data-ttu-id="9c8d3-127">如果來源位置需要身分憑證，您必須提供認證。</span><span class="sxs-lookup"><span data-stu-id="9c8d3-127">If the source location requires a credential, you must provide one.</span></span>

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

### <span data-ttu-id="9c8d3-128">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9c8d3-128">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="9c8d3-129">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="9c8d3-129">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="9c8d3-130">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="9c8d3-130">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="9c8d3-131">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="9c8d3-131">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="9c8d3-132">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="9c8d3-132">-ConcurrentTaskCount</span></span>
<span data-ttu-id="9c8d3-133">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="9c8d3-133">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="9c8d3-134">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="9c8d3-134">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="9c8d3-135">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="9c8d3-135">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="9c8d3-136">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="9c8d3-136">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="9c8d3-137">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="9c8d3-137">The default value is 10.</span></span>

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

### <span data-ttu-id="9c8d3-138">-內容</span><span class="sxs-lookup"><span data-stu-id="9c8d3-138">-Context</span></span>
<span data-ttu-id="9c8d3-139">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="9c8d3-139">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="9c8d3-140">若要取得內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9c8d3-140">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="9c8d3-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c8d3-141">-DefaultProfile</span></span>
<span data-ttu-id="9c8d3-142">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9c8d3-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c8d3-143">-DestCoNtext</span><span class="sxs-lookup"><span data-stu-id="9c8d3-143">-DestContext</span></span>
<span data-ttu-id="9c8d3-144">指定目的地的 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="9c8d3-144">Specifies the Azure Storage context of the destination.</span></span>
<span data-ttu-id="9c8d3-145">若要取得內容，請使用 **新的-AzStorageCoNtext** 。</span><span class="sxs-lookup"><span data-stu-id="9c8d3-145">To obtain a context, use **New-AzStorageContext**.</span></span>

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

### <span data-ttu-id="9c8d3-146">-DestFile</span><span class="sxs-lookup"><span data-stu-id="9c8d3-146">-DestFile</span></span>
<span data-ttu-id="9c8d3-147">指定 **CloudFile** 物件。</span><span class="sxs-lookup"><span data-stu-id="9c8d3-147">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="9c8d3-148">您可以使用 Get-AzStorageFile Cmdlet 來建立雲端檔案或取得一個雲端檔案。</span><span class="sxs-lookup"><span data-stu-id="9c8d3-148">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: BlobInstanceFileInstance, FileInstanceToFileInstance, UriToFileInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c8d3-149">-DestFilePath</span><span class="sxs-lookup"><span data-stu-id="9c8d3-149">-DestFilePath</span></span>
<span data-ttu-id="9c8d3-150">指定目標檔案相對於目的地共用的路徑。</span><span class="sxs-lookup"><span data-stu-id="9c8d3-150">Specifies the path of the destination file relative to the destination share.</span></span>

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

### <span data-ttu-id="9c8d3-151">-DestShareName</span><span class="sxs-lookup"><span data-stu-id="9c8d3-151">-DestShareName</span></span>
<span data-ttu-id="9c8d3-152">指定目的地共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="9c8d3-152">Specifies the name of the destination share.</span></span>

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

### <span data-ttu-id="9c8d3-153">-Force</span><span class="sxs-lookup"><span data-stu-id="9c8d3-153">-Force</span></span>
<span data-ttu-id="9c8d3-154">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="9c8d3-154">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9c8d3-155">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9c8d3-155">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="9c8d3-156">指定要求中伺服器部分的超時時間長度。</span><span class="sxs-lookup"><span data-stu-id="9c8d3-156">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="9c8d3-157">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="9c8d3-157">-SrcBlob</span></span>
<span data-ttu-id="9c8d3-158">指定 **CloudBlob** 物件。</span><span class="sxs-lookup"><span data-stu-id="9c8d3-158">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="9c8d3-159">您可以使用 Get-AzStorageBlob Cmdlet 來建立雲端 blob 或取得一個。</span><span class="sxs-lookup"><span data-stu-id="9c8d3-159">You can create a cloud blob or obtain one by using the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstanceFilePath, BlobInstanceFileInstance
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c8d3-160">-SrcBlobName</span><span class="sxs-lookup"><span data-stu-id="9c8d3-160">-SrcBlobName</span></span>
<span data-ttu-id="9c8d3-161">指定來源 blob 的名稱。</span><span class="sxs-lookup"><span data-stu-id="9c8d3-161">Specifies the name of the source blob.</span></span>

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

### <span data-ttu-id="9c8d3-162">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="9c8d3-162">-SrcContainer</span></span>
<span data-ttu-id="9c8d3-163">指定雲端 blob 容器物件。</span><span class="sxs-lookup"><span data-stu-id="9c8d3-163">Specifies a cloud blob container object.</span></span>
<span data-ttu-id="9c8d3-164">您可以建立雲端 blob 容器物件或使用 Get-AzStorageContainer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9c8d3-164">You can create cloud blob container object or use the Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c8d3-165">-SrcContainerName</span><span class="sxs-lookup"><span data-stu-id="9c8d3-165">-SrcContainerName</span></span>
<span data-ttu-id="9c8d3-166">指定來源容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="9c8d3-166">Specifies the name of the source container.</span></span>

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

### <span data-ttu-id="9c8d3-167">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="9c8d3-167">-SrcFile</span></span>
<span data-ttu-id="9c8d3-168">指定 **CloudFile** 物件。</span><span class="sxs-lookup"><span data-stu-id="9c8d3-168">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="9c8d3-169">您可以使用 **AzStorageFile** 建立雲端檔案或取得一個雲端檔案。</span><span class="sxs-lookup"><span data-stu-id="9c8d3-169">You can create a cloud file or obtain one by using **Get-AzStorageFile**.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: FileInstanceToFilePath, FileInstanceToFileInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c8d3-170">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="9c8d3-170">-SrcFilePath</span></span>
<span data-ttu-id="9c8d3-171">指定相對於來原始目錄或來源共用的來源檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="9c8d3-171">Specifies the path of the source file relative to the source directory or source share.</span></span>

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

### <span data-ttu-id="9c8d3-172">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="9c8d3-172">-SrcShare</span></span>
<span data-ttu-id="9c8d3-173">指定雲端檔案共用物件。</span><span class="sxs-lookup"><span data-stu-id="9c8d3-173">Specifies a cloud file share object.</span></span>
<span data-ttu-id="9c8d3-174">您可以使用 Get-AzStorageShare Cmdlet 來建立雲端檔案共用或取得一個共用檔案。</span><span class="sxs-lookup"><span data-stu-id="9c8d3-174">You can create a cloud file share or obtain one by using the Get-AzStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: ShareInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c8d3-175">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="9c8d3-175">-SrcShareName</span></span>
<span data-ttu-id="9c8d3-176">指定來源共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="9c8d3-176">Specifies the name of the source share.</span></span>

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

### <span data-ttu-id="9c8d3-177">-確認</span><span class="sxs-lookup"><span data-stu-id="9c8d3-177">-Confirm</span></span>
<span data-ttu-id="9c8d3-178">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9c8d3-178">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c8d3-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c8d3-179">-WhatIf</span></span>
<span data-ttu-id="9c8d3-180">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9c8d3-180">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c8d3-181">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9c8d3-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c8d3-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c8d3-182">CommonParameters</span></span>
<span data-ttu-id="9c8d3-183">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9c8d3-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c8d3-184">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9c8d3-184">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c8d3-185">輸入</span><span class="sxs-lookup"><span data-stu-id="9c8d3-185">INPUTS</span></span>

### <span data-ttu-id="9c8d3-186">[WindowsAz] CloudBlob</span><span class="sxs-lookup"><span data-stu-id="9c8d3-186">Microsoft.WindowsAz.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="9c8d3-187">[WindowsAz] CloudFile</span><span class="sxs-lookup"><span data-stu-id="9c8d3-187">Microsoft.WindowsAz.Storage.File.CloudFile</span></span>
<span data-ttu-id="9c8d3-188">參數： SrcFile (ByValue) </span><span class="sxs-lookup"><span data-stu-id="9c8d3-188">Parameters: SrcFile (ByValue)</span></span>

### <span data-ttu-id="9c8d3-189">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="9c8d3-189">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9c8d3-190">輸出</span><span class="sxs-lookup"><span data-stu-id="9c8d3-190">OUTPUTS</span></span>

### <span data-ttu-id="9c8d3-191">System.void</span><span class="sxs-lookup"><span data-stu-id="9c8d3-191">System.Void</span></span>

## <span data-ttu-id="9c8d3-192">筆記</span><span class="sxs-lookup"><span data-stu-id="9c8d3-192">NOTES</span></span>

## <span data-ttu-id="9c8d3-193">相關連結</span><span class="sxs-lookup"><span data-stu-id="9c8d3-193">RELATED LINKS</span></span>

[<span data-ttu-id="9c8d3-194">AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="9c8d3-194">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="9c8d3-195">AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9c8d3-195">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="9c8d3-196">AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="9c8d3-196">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="9c8d3-197">AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="9c8d3-197">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="9c8d3-198">AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="9c8d3-198">Get-AzStorageFileCopyState</span></span>](./Get-AzStorageFileCopyState.md)

[<span data-ttu-id="9c8d3-199">停止 AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="9c8d3-199">Stop-AzStorageFileCopy</span></span>](./Stop-AzStorageFileCopy.md)