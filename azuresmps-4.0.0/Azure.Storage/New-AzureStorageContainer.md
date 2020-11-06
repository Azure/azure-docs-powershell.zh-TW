---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 2B12BC19-EF8F-43F5-AF04-C570FEEA1AE6
online version: ''
schema: 2.0.0
ms.openlocfilehash: d80a8a75082503cf8cde9df7a779ca7f0d7d4b92
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443407"
---
# <span data-ttu-id="6db19-101">New-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6db19-101">New-AzureStorageContainer</span></span>

## <span data-ttu-id="6db19-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6db19-102">SYNOPSIS</span></span>
<span data-ttu-id="6db19-103">建立 Azure 儲存空間容器。</span><span class="sxs-lookup"><span data-stu-id="6db19-103">Creates an Azure storage container.</span></span>

## <span data-ttu-id="6db19-104">句法</span><span class="sxs-lookup"><span data-stu-id="6db19-104">SYNTAX</span></span>

```
New-AzureStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="6db19-105">說明</span><span class="sxs-lookup"><span data-stu-id="6db19-105">DESCRIPTION</span></span>
<span data-ttu-id="6db19-106">**新的-AzureStorageContainer** Cmdlet 會建立 Azure 儲存空間容器。</span><span class="sxs-lookup"><span data-stu-id="6db19-106">The **New-AzureStorageContainer** cmdlet creates an Azure storage container.</span></span>

## <span data-ttu-id="6db19-107">示例</span><span class="sxs-lookup"><span data-stu-id="6db19-107">EXAMPLES</span></span>

### <span data-ttu-id="6db19-108">範例1：建立 Azure 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="6db19-108">Example 1: Create an Azure storage container</span></span>
```
PS C:\>New-AzureStorageContainer -Name "ContainerName" -Permission Off
```

<span data-ttu-id="6db19-109">這個命令會建立儲存容器。</span><span class="sxs-lookup"><span data-stu-id="6db19-109">This command creates a storage container.</span></span>

### <span data-ttu-id="6db19-110">範例2：建立多個 Azure 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="6db19-110">Example 2: Create multiple Azure storage containers</span></span>
```
PS C:\>"container1 container2 container3".split() | New-AzureStorageContainer -Permission Container
```

<span data-ttu-id="6db19-111">這個範例會建立多個儲存容器。</span><span class="sxs-lookup"><span data-stu-id="6db19-111">This example creates multiple storage containers.</span></span>
<span data-ttu-id="6db19-112">它會使用 .NET **字串** 類別的 **Split** 方法，然後傳送管線上的名稱。</span><span class="sxs-lookup"><span data-stu-id="6db19-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="6db19-113">參數</span><span class="sxs-lookup"><span data-stu-id="6db19-113">PARAMETERS</span></span>

### <span data-ttu-id="6db19-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6db19-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="6db19-115">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="6db19-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="6db19-116">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="6db19-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="6db19-117">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="6db19-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="6db19-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="6db19-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="6db19-119">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="6db19-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="6db19-120">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="6db19-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="6db19-121">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="6db19-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="6db19-122">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="6db19-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="6db19-123">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="6db19-123">The default value is 10.</span></span>

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

### <span data-ttu-id="6db19-124">-內容</span><span class="sxs-lookup"><span data-stu-id="6db19-124">-Context</span></span>
<span data-ttu-id="6db19-125">指定新容器的內容。</span><span class="sxs-lookup"><span data-stu-id="6db19-125">Specifies a context for the new container.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6db19-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="6db19-126">-Name</span></span>
<span data-ttu-id="6db19-127">指定新容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="6db19-127">Specifies a name for the new container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6db19-128">-許可權</span><span class="sxs-lookup"><span data-stu-id="6db19-128">-Permission</span></span>
<span data-ttu-id="6db19-129">指定此容器的公開存取層級。</span><span class="sxs-lookup"><span data-stu-id="6db19-129">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="6db19-130">根據預設，容器及其中的任何 blob 只能由儲存空間帳戶的擁有者存取。</span><span class="sxs-lookup"><span data-stu-id="6db19-130">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="6db19-131">若要授權匿名使用者讀取容器及其 blob 的許可權，您可以設定容器許可權來啟用公用存取。</span><span class="sxs-lookup"><span data-stu-id="6db19-131">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="6db19-132">匿名使用者可以在公開提供的容器中讀取 blob，而不需驗證要求。</span><span class="sxs-lookup"><span data-stu-id="6db19-132">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="6db19-133">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="6db19-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6db19-134">包裝箱.</span><span class="sxs-lookup"><span data-stu-id="6db19-134">Container.</span></span>
<span data-ttu-id="6db19-135">提供容器及其 blob 的完整讀取存取權。</span><span class="sxs-lookup"><span data-stu-id="6db19-135">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="6db19-136">用戶端可以透過匿名要求列舉容器中的 blob，但無法在儲存空間帳戶列舉容器。</span><span class="sxs-lookup"><span data-stu-id="6db19-136">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> 
- <span data-ttu-id="6db19-137">Blob.</span><span class="sxs-lookup"><span data-stu-id="6db19-137">Blob.</span></span>
<span data-ttu-id="6db19-138">透過匿名要求提供對容器中的 blob 資料的讀取存取權，但不提供對容器資料的存取權。</span><span class="sxs-lookup"><span data-stu-id="6db19-138">Provides read access to blob data throughout a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="6db19-139">用戶端無法使用匿名要求來列舉容器中的 blob。</span><span class="sxs-lookup"><span data-stu-id="6db19-139">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> 
- <span data-ttu-id="6db19-140">出.</span><span class="sxs-lookup"><span data-stu-id="6db19-140">Off.</span></span>
<span data-ttu-id="6db19-141">可限制存取權僅限儲存帳戶擁有者。</span><span class="sxs-lookup"><span data-stu-id="6db19-141">Which restricts access to only the storage account owner.</span></span>

```yaml
Type: BlobContainerPublicAccessType
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6db19-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6db19-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="6db19-143">指定要求的服務端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="6db19-143">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="6db19-144">如果所指定的間隔在服務處理要求之前就已到期，儲存服務就會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="6db19-144">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="6db19-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6db19-145">CommonParameters</span></span>
<span data-ttu-id="6db19-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6db19-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6db19-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6db19-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6db19-148">輸入</span><span class="sxs-lookup"><span data-stu-id="6db19-148">INPUTS</span></span>

## <span data-ttu-id="6db19-149">輸出</span><span class="sxs-lookup"><span data-stu-id="6db19-149">OUTPUTS</span></span>

## <span data-ttu-id="6db19-150">筆記</span><span class="sxs-lookup"><span data-stu-id="6db19-150">NOTES</span></span>

## <span data-ttu-id="6db19-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="6db19-151">RELATED LINKS</span></span>

[<span data-ttu-id="6db19-152">AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6db19-152">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="6db19-153">移除-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6db19-153">Remove-AzureStorageContainer</span></span>](./Remove-AzureStorageContainer.md)

[<span data-ttu-id="6db19-154">Set-AzureStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="6db19-154">Set-AzureStorageContainerAcl</span></span>](./Set-AzureStorageContainerAcl.md)


