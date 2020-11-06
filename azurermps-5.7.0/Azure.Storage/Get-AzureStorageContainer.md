---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 90C3DF13-0010-49B6-A8CD-C6AC34BC3EFA
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainer.md
ms.openlocfilehash: 45368a3abe428c65604d4ba103cf793972e50ea1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449473"
---
# <span data-ttu-id="a6c88-101">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a6c88-101">Get-AzureStorageContainer</span></span>

## <span data-ttu-id="a6c88-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a6c88-102">SYNOPSIS</span></span>
<span data-ttu-id="a6c88-103">列出儲存容器。</span><span class="sxs-lookup"><span data-stu-id="a6c88-103">Lists the storage containers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6c88-104">句法</span><span class="sxs-lookup"><span data-stu-id="a6c88-104">SYNTAX</span></span>

### <span data-ttu-id="a6c88-105">[容器] (預設) </span><span class="sxs-lookup"><span data-stu-id="a6c88-105">ContainerName (Default)</span></span>
```
Get-AzureStorageContainer [[-Name] <String>] [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="a6c88-106">ContainerPrefix</span><span class="sxs-lookup"><span data-stu-id="a6c88-106">ContainerPrefix</span></span>
```
Get-AzureStorageContainer -Prefix <String> [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="a6c88-107">說明</span><span class="sxs-lookup"><span data-stu-id="a6c88-107">DESCRIPTION</span></span>
<span data-ttu-id="a6c88-108">**AzureStorageContainer** Cmdlet 會列出與 Azure 中的儲存空間帳戶相關聯的儲存空間容器。</span><span class="sxs-lookup"><span data-stu-id="a6c88-108">The **Get-AzureStorageContainer** cmdlet lists the storage containers associated with the storage account in Azure.</span></span>

## <span data-ttu-id="a6c88-109">示例</span><span class="sxs-lookup"><span data-stu-id="a6c88-109">EXAMPLES</span></span>

### <span data-ttu-id="a6c88-110">範例1：依名稱取得 Azure 儲存區 blob</span><span class="sxs-lookup"><span data-stu-id="a6c88-110">Example 1: Get Azure Storage blob by name</span></span>
```
PS C:\>Get-AzureStorageContainer -Name container*
```

<span data-ttu-id="a6c88-111">這個範例使用萬用字元傳回名稱以容器為開頭的所有容器清單。</span><span class="sxs-lookup"><span data-stu-id="a6c88-111">This example uses a wildcard character to return a list of all containers with a name that starts with container.</span></span>

### <span data-ttu-id="a6c88-112">範例2：透過容器名稱首碼取得 Azure 儲存空間容器</span><span class="sxs-lookup"><span data-stu-id="a6c88-112">Example 2: Get Azure Storage container by container name prefix</span></span>
```
PS C:\>Get-AzureStorageContainer -Prefix "container"
```

<span data-ttu-id="a6c88-113">這個範例使用 *Prefix* 參數，傳回名稱以 container 開頭的所有容器清單。</span><span class="sxs-lookup"><span data-stu-id="a6c88-113">This example uses the *Prefix* parameter to return a list of all containers with a name that starts with container.</span></span>

## <span data-ttu-id="a6c88-114">參數</span><span class="sxs-lookup"><span data-stu-id="a6c88-114">PARAMETERS</span></span>

### <span data-ttu-id="a6c88-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a6c88-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a6c88-116">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="a6c88-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="a6c88-117">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="a6c88-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="a6c88-118">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="a6c88-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="a6c88-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a6c88-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a6c88-120">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="a6c88-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="a6c88-121">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="a6c88-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="a6c88-122">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="a6c88-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="a6c88-123">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="a6c88-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="a6c88-124">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="a6c88-124">The default value is 10.</span></span>

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

### <span data-ttu-id="a6c88-125">-內容</span><span class="sxs-lookup"><span data-stu-id="a6c88-125">-Context</span></span>
<span data-ttu-id="a6c88-126">指定儲存內容。</span><span class="sxs-lookup"><span data-stu-id="a6c88-126">Specifies the storage context.</span></span>
<span data-ttu-id="a6c88-127">若要建立它，您可以使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a6c88-127">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>
<span data-ttu-id="a6c88-128">當您使用從 SAS 權杖建立的儲存內容時，此 Cmdlet 會失敗，因為 Cmdlet 會查詢需要儲存帳戶金鑰許可權的容器許可權。</span><span class="sxs-lookup"><span data-stu-id="a6c88-128">The cmdlet will fail when you use a storage context created from SAS Token because the cmdlet will query for container permissions which require Storage account key permission.</span></span>

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

### <span data-ttu-id="a6c88-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="a6c88-129">-ContinuationToken</span></span>
<span data-ttu-id="a6c88-130">指定 blob 清單的延續標記。</span><span class="sxs-lookup"><span data-stu-id="a6c88-130">Specifies a continuation token for the blob list.</span></span>

```yaml
Type: BlobContinuationToken
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6c88-131">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="a6c88-131">-MaxCount</span></span>
<span data-ttu-id="a6c88-132">指定此 Cmdlet 傳回的物件數目上限。</span><span class="sxs-lookup"><span data-stu-id="a6c88-132">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="a6c88-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="a6c88-133">-Name</span></span>
<span data-ttu-id="a6c88-134">指定容器名稱。</span><span class="sxs-lookup"><span data-stu-id="a6c88-134">Specifies the container name.</span></span>
<span data-ttu-id="a6c88-135">如果容器名稱是空的，Cmdlet 會列出所有的容器。</span><span class="sxs-lookup"><span data-stu-id="a6c88-135">If container name is empty, the cmdlet lists all the containers.</span></span>
<span data-ttu-id="a6c88-136">否則，它會列出符合指定名稱或一般名稱模式的所有容器。</span><span class="sxs-lookup"><span data-stu-id="a6c88-136">Otherwise, it lists all containers that match the specified name or the regular name pattern.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName
Aliases: N, Container

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="a6c88-137">-Prefix</span><span class="sxs-lookup"><span data-stu-id="a6c88-137">-Prefix</span></span>
<span data-ttu-id="a6c88-138">指定要取得之容器或容器名稱中所用的首碼。</span><span class="sxs-lookup"><span data-stu-id="a6c88-138">Specifies a prefix used in the name of the container or containers you want to get.</span></span>
<span data-ttu-id="a6c88-139">您可以使用此程式來找出所有以相同字串（例如「my」或「test」）開頭的容器。</span><span class="sxs-lookup"><span data-stu-id="a6c88-139">You can use this to find all containers that start with the same string, such as "my" or "test".</span></span>

```yaml
Type: String
Parameter Sets: ContainerPrefix
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6c88-140">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a6c88-140">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a6c88-141">指定要求的服務端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="a6c88-141">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="a6c88-142">如果所指定的間隔在服務處理要求之前就已到期，儲存服務就會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="a6c88-142">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="a6c88-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6c88-143">CommonParameters</span></span>
<span data-ttu-id="a6c88-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a6c88-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6c88-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a6c88-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6c88-146">輸入</span><span class="sxs-lookup"><span data-stu-id="a6c88-146">INPUTS</span></span>

### <span data-ttu-id="a6c88-147">IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="a6c88-147">IStorageContext</span></span>

<span data-ttu-id="a6c88-148">參數「CoNtext」接受來自管線的 "IStorageCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="a6c88-148">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="a6c88-149">字串</span><span class="sxs-lookup"><span data-stu-id="a6c88-149">String</span></span>

<span data-ttu-id="a6c88-150">形參 "Name" 接受管線中類型 "String" 的值</span><span class="sxs-lookup"><span data-stu-id="a6c88-150">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="a6c88-151">輸出</span><span class="sxs-lookup"><span data-stu-id="a6c88-151">OUTPUTS</span></span>

### <span data-ttu-id="a6c88-152">AzureStorageContainer WindowsAzure. ResourceModel。</span><span class="sxs-lookup"><span data-stu-id="a6c88-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="a6c88-153">筆記</span><span class="sxs-lookup"><span data-stu-id="a6c88-153">NOTES</span></span>

## <span data-ttu-id="a6c88-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="a6c88-154">RELATED LINKS</span></span>

[<span data-ttu-id="a6c88-155">新-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a6c88-155">New-AzureStorageContainer</span></span>](./New-AzureStorageContainer.md)

[<span data-ttu-id="a6c88-156">移除-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a6c88-156">Remove-AzureStorageContainer</span></span>](./Remove-AzureStorageContainer.md)

[<span data-ttu-id="a6c88-157">Set-AzureStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="a6c88-157">Set-AzureStorageContainerAcl</span></span>](./Set-AzureStorageContainerAcl.md)


