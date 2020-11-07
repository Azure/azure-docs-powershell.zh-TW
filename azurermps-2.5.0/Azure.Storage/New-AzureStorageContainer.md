---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 2B12BC19-EF8F-43F5-AF04-C570FEEA1AE6
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragecontainer
schema: 2.0.0
ms.openlocfilehash: 87967dbaaa57bb8050191ee1b20ebb5a760bc045
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801093"
---
# <span data-ttu-id="f6e7c-101">New-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f6e7c-101">New-AzureStorageContainer</span></span>

## <span data-ttu-id="f6e7c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f6e7c-102">SYNOPSIS</span></span>
<span data-ttu-id="f6e7c-103">建立 Azure 儲存空間容器。</span><span class="sxs-lookup"><span data-stu-id="f6e7c-103">Creates an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6e7c-104">句法</span><span class="sxs-lookup"><span data-stu-id="f6e7c-104">SYNTAX</span></span>

```
New-AzureStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="f6e7c-105">說明</span><span class="sxs-lookup"><span data-stu-id="f6e7c-105">DESCRIPTION</span></span>
<span data-ttu-id="f6e7c-106">**新的-AzureStorageContainer** Cmdlet 會建立 Azure 儲存空間容器。</span><span class="sxs-lookup"><span data-stu-id="f6e7c-106">The **New-AzureStorageContainer** cmdlet creates an Azure storage container.</span></span>

## <span data-ttu-id="f6e7c-107">示例</span><span class="sxs-lookup"><span data-stu-id="f6e7c-107">EXAMPLES</span></span>

### <span data-ttu-id="f6e7c-108">範例1：建立 Azure 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="f6e7c-108">Example 1: Create an Azure storage container</span></span>
```
PS C:\>New-AzureStorageContainer -Name "ContainerName" -Permission Off
```

<span data-ttu-id="f6e7c-109">這個命令會建立儲存容器。</span><span class="sxs-lookup"><span data-stu-id="f6e7c-109">This command creates a storage container.</span></span>

### <span data-ttu-id="f6e7c-110">範例2：建立多個 Azure 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="f6e7c-110">Example 2: Create multiple Azure storage containers</span></span>
```
PS C:\>"container1 container2 container3".split() | New-AzureStorageContainer -Permission Container
```

<span data-ttu-id="f6e7c-111">這個範例會建立多個儲存容器。</span><span class="sxs-lookup"><span data-stu-id="f6e7c-111">This example creates multiple storage containers.</span></span>
<span data-ttu-id="f6e7c-112">它會使用 .NET **字串** 類別的 **Split** 方法，然後傳送管線上的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6e7c-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="f6e7c-113">參數</span><span class="sxs-lookup"><span data-stu-id="f6e7c-113">PARAMETERS</span></span>

### <span data-ttu-id="f6e7c-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f6e7c-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="f6e7c-115">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="f6e7c-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="f6e7c-116">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="f6e7c-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="f6e7c-117">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="f6e7c-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="f6e7c-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="f6e7c-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="f6e7c-119">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="f6e7c-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="f6e7c-120">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="f6e7c-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="f6e7c-121">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="f6e7c-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="f6e7c-122">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="f6e7c-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="f6e7c-123">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="f6e7c-123">The default value is 10.</span></span>

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

### <span data-ttu-id="f6e7c-124">-內容</span><span class="sxs-lookup"><span data-stu-id="f6e7c-124">-Context</span></span>
<span data-ttu-id="f6e7c-125">指定新容器的內容。</span><span class="sxs-lookup"><span data-stu-id="f6e7c-125">Specifies a context for the new container.</span></span>

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

### <span data-ttu-id="f6e7c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6e7c-126">-DefaultProfile</span></span>
<span data-ttu-id="f6e7c-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f6e7c-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6e7c-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="f6e7c-128">-Name</span></span>
<span data-ttu-id="f6e7c-129">指定新容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6e7c-129">Specifies a name for the new container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6e7c-130">-許可權</span><span class="sxs-lookup"><span data-stu-id="f6e7c-130">-Permission</span></span>
<span data-ttu-id="f6e7c-131">指定此容器的公開存取層級。</span><span class="sxs-lookup"><span data-stu-id="f6e7c-131">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="f6e7c-132">根據預設，容器及其中的任何 blob 只能由儲存空間帳戶的擁有者存取。</span><span class="sxs-lookup"><span data-stu-id="f6e7c-132">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="f6e7c-133">若要授權匿名使用者讀取容器及其 blob 的許可權，您可以設定容器許可權來啟用公用存取。</span><span class="sxs-lookup"><span data-stu-id="f6e7c-133">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="f6e7c-134">匿名使用者可以在公開提供的容器中讀取 blob，而不需驗證要求。</span><span class="sxs-lookup"><span data-stu-id="f6e7c-134">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="f6e7c-135">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="f6e7c-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f6e7c-136">包裝箱.</span><span class="sxs-lookup"><span data-stu-id="f6e7c-136">Container.</span></span>
<span data-ttu-id="f6e7c-137">提供容器及其 blob 的完整讀取存取權。</span><span class="sxs-lookup"><span data-stu-id="f6e7c-137">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="f6e7c-138">用戶端可以透過匿名要求列舉容器中的 blob，但無法在儲存空間帳戶列舉容器。</span><span class="sxs-lookup"><span data-stu-id="f6e7c-138">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> 
- <span data-ttu-id="f6e7c-139">Blob.</span><span class="sxs-lookup"><span data-stu-id="f6e7c-139">Blob.</span></span>
<span data-ttu-id="f6e7c-140">透過匿名要求提供對容器中的 blob 資料的讀取存取權，但不提供對容器資料的存取權。</span><span class="sxs-lookup"><span data-stu-id="f6e7c-140">Provides read access to blob data throughout a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="f6e7c-141">用戶端無法使用匿名要求來列舉容器中的 blob。</span><span class="sxs-lookup"><span data-stu-id="f6e7c-141">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> 
- <span data-ttu-id="f6e7c-142">出.</span><span class="sxs-lookup"><span data-stu-id="f6e7c-142">Off.</span></span>
<span data-ttu-id="f6e7c-143">可限制存取權僅限儲存帳戶擁有者。</span><span class="sxs-lookup"><span data-stu-id="f6e7c-143">Which restricts access to only the storage account owner.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.WindowsAzure.Storage.Blob.BlobContainerPublicAccessType]
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob, Unknown

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6e7c-144">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f6e7c-144">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="f6e7c-145">指定要求的服務端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="f6e7c-145">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="f6e7c-146">如果所指定的間隔在服務處理要求之前就已到期，儲存服務就會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="f6e7c-146">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="f6e7c-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6e7c-147">CommonParameters</span></span>
<span data-ttu-id="f6e7c-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f6e7c-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6e7c-149">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f6e7c-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6e7c-150">輸入</span><span class="sxs-lookup"><span data-stu-id="f6e7c-150">INPUTS</span></span>

### <span data-ttu-id="f6e7c-151">System.object</span><span class="sxs-lookup"><span data-stu-id="f6e7c-151">System.String</span></span>

### <span data-ttu-id="f6e7c-152">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="f6e7c-152">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f6e7c-153">輸出</span><span class="sxs-lookup"><span data-stu-id="f6e7c-153">OUTPUTS</span></span>

### <span data-ttu-id="f6e7c-154">AzureStorageContainer WindowsAzure. ResourceModel。</span><span class="sxs-lookup"><span data-stu-id="f6e7c-154">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="f6e7c-155">筆記</span><span class="sxs-lookup"><span data-stu-id="f6e7c-155">NOTES</span></span>

## <span data-ttu-id="f6e7c-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="f6e7c-156">RELATED LINKS</span></span>

[<span data-ttu-id="f6e7c-157">AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f6e7c-157">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="f6e7c-158">移除-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f6e7c-158">Remove-AzureStorageContainer</span></span>](./Remove-AzureStorageContainer.md)

[<span data-ttu-id="f6e7c-159">Set-AzureStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="f6e7c-159">Set-AzureStorageContainerAcl</span></span>](./Set-AzureStorageContainerAcl.md)


