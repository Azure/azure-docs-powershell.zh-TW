---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 90C3DF13-0010-49B6-A8CD-C6AC34BC3EFA
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageContainer.md
ms.openlocfilehash: 16365ea4f5c2826c173525b90e52fd2103d5d7dc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795149"
---
# <span data-ttu-id="97c6b-101">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="97c6b-101">Get-AzStorageContainer</span></span>

## <span data-ttu-id="97c6b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="97c6b-102">SYNOPSIS</span></span>
<span data-ttu-id="97c6b-103">列出儲存容器。</span><span class="sxs-lookup"><span data-stu-id="97c6b-103">Lists the storage containers.</span></span>

## <span data-ttu-id="97c6b-104">句法</span><span class="sxs-lookup"><span data-stu-id="97c6b-104">SYNTAX</span></span>

### <span data-ttu-id="97c6b-105">[容器] (預設) </span><span class="sxs-lookup"><span data-stu-id="97c6b-105">ContainerName (Default)</span></span>
```
Get-AzStorageContainer [[-Name] <String>] [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="97c6b-106">ContainerPrefix</span><span class="sxs-lookup"><span data-stu-id="97c6b-106">ContainerPrefix</span></span>
```
Get-AzStorageContainer -Prefix <String> [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="97c6b-107">說明</span><span class="sxs-lookup"><span data-stu-id="97c6b-107">DESCRIPTION</span></span>
<span data-ttu-id="97c6b-108">**AzStorageContainer** Cmdlet 會列出與 Azure 中的儲存空間帳戶相關聯的儲存空間容器。</span><span class="sxs-lookup"><span data-stu-id="97c6b-108">The **Get-AzStorageContainer** cmdlet lists the storage containers associated with the storage account in Azure.</span></span>

## <span data-ttu-id="97c6b-109">示例</span><span class="sxs-lookup"><span data-stu-id="97c6b-109">EXAMPLES</span></span>

### <span data-ttu-id="97c6b-110">範例1：依名稱取得 Azure 儲存區 blob</span><span class="sxs-lookup"><span data-stu-id="97c6b-110">Example 1: Get Azure Storage blob by name</span></span>
```
PS C:\>Get-AzStorageContainer -Name container*
```

<span data-ttu-id="97c6b-111">這個範例使用萬用字元傳回名稱以容器為開頭的所有容器清單。</span><span class="sxs-lookup"><span data-stu-id="97c6b-111">This example uses a wildcard character to return a list of all containers with a name that starts with container.</span></span>

### <span data-ttu-id="97c6b-112">範例2：透過容器名稱首碼取得 Azure 儲存空間容器</span><span class="sxs-lookup"><span data-stu-id="97c6b-112">Example 2: Get Azure Storage container by container name prefix</span></span>
```
PS C:\>Get-AzStorageContainer -Prefix "container"
```

<span data-ttu-id="97c6b-113">這個範例使用 *Prefix* 參數，傳回名稱以 container 開頭的所有容器清單。</span><span class="sxs-lookup"><span data-stu-id="97c6b-113">This example uses the *Prefix* parameter to return a list of all containers with a name that starts with container.</span></span>

## <span data-ttu-id="97c6b-114">參數</span><span class="sxs-lookup"><span data-stu-id="97c6b-114">PARAMETERS</span></span>

### <span data-ttu-id="97c6b-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="97c6b-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="97c6b-116">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="97c6b-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="97c6b-117">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="97c6b-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="97c6b-118">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="97c6b-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="97c6b-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="97c6b-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="97c6b-120">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="97c6b-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="97c6b-121">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="97c6b-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="97c6b-122">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="97c6b-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="97c6b-123">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="97c6b-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="97c6b-124">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="97c6b-124">The default value is 10.</span></span>

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

### <span data-ttu-id="97c6b-125">-內容</span><span class="sxs-lookup"><span data-stu-id="97c6b-125">-Context</span></span>
<span data-ttu-id="97c6b-126">指定儲存內容。</span><span class="sxs-lookup"><span data-stu-id="97c6b-126">Specifies the storage context.</span></span>
<span data-ttu-id="97c6b-127">若要建立它，您可以使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="97c6b-127">To create it, you can use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="97c6b-128">當您使用從 SAS 權杖建立的儲存內容時，此 Cmdlet 會失敗，因為 Cmdlet 會查詢需要儲存帳戶金鑰許可權的容器許可權。</span><span class="sxs-lookup"><span data-stu-id="97c6b-128">The cmdlet will fail when you use a storage context created from SAS Token because the cmdlet will query for container permissions which require Storage account key permission.</span></span>

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

### <span data-ttu-id="97c6b-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="97c6b-129">-ContinuationToken</span></span>
<span data-ttu-id="97c6b-130">指定 blob 清單的延續標記。</span><span class="sxs-lookup"><span data-stu-id="97c6b-130">Specifies a continuation token for the blob list.</span></span>

```yaml
Type: Microsoft.WindowsAz.Storage.Blob.BlobContinuationToken
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97c6b-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97c6b-131">-DefaultProfile</span></span>
<span data-ttu-id="97c6b-132">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="97c6b-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97c6b-133">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="97c6b-133">-MaxCount</span></span>
<span data-ttu-id="97c6b-134">指定此 Cmdlet 傳回的物件數目上限。</span><span class="sxs-lookup"><span data-stu-id="97c6b-134">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="97c6b-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="97c6b-135">-Name</span></span>
<span data-ttu-id="97c6b-136">指定容器名稱。</span><span class="sxs-lookup"><span data-stu-id="97c6b-136">Specifies the container name.</span></span>
<span data-ttu-id="97c6b-137">如果容器名稱是空的，Cmdlet 會列出所有的容器。</span><span class="sxs-lookup"><span data-stu-id="97c6b-137">If container name is empty, the cmdlet lists all the containers.</span></span>
<span data-ttu-id="97c6b-138">否則，它會列出符合指定名稱或一般名稱模式的所有容器。</span><span class="sxs-lookup"><span data-stu-id="97c6b-138">Otherwise, it lists all containers that match the specified name or the regular name pattern.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases: N, Container

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97c6b-139">-Prefix</span><span class="sxs-lookup"><span data-stu-id="97c6b-139">-Prefix</span></span>
<span data-ttu-id="97c6b-140">指定要取得之容器或容器名稱中所用的首碼。</span><span class="sxs-lookup"><span data-stu-id="97c6b-140">Specifies a prefix used in the name of the container or containers you want to get.</span></span>
<span data-ttu-id="97c6b-141">您可以使用此程式來找出所有以相同字串（例如「my」或「test」）開頭的容器。</span><span class="sxs-lookup"><span data-stu-id="97c6b-141">You can use this to find all containers that start with the same string, such as "my" or "test".</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerPrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97c6b-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="97c6b-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="97c6b-143">指定要求的服務端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="97c6b-143">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="97c6b-144">如果所指定的間隔在服務處理要求之前就已到期，儲存服務就會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="97c6b-144">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="97c6b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97c6b-145">CommonParameters</span></span>
<span data-ttu-id="97c6b-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="97c6b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97c6b-147">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="97c6b-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97c6b-148">輸入</span><span class="sxs-lookup"><span data-stu-id="97c6b-148">INPUTS</span></span>

### <span data-ttu-id="97c6b-149">System.object</span><span class="sxs-lookup"><span data-stu-id="97c6b-149">System.String</span></span>

### <span data-ttu-id="97c6b-150">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="97c6b-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="97c6b-151">輸出</span><span class="sxs-lookup"><span data-stu-id="97c6b-151">OUTPUTS</span></span>

### <span data-ttu-id="97c6b-152">AzureStorageContainer WindowsAzure. ResourceModel。</span><span class="sxs-lookup"><span data-stu-id="97c6b-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="97c6b-153">筆記</span><span class="sxs-lookup"><span data-stu-id="97c6b-153">NOTES</span></span>

## <span data-ttu-id="97c6b-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="97c6b-154">RELATED LINKS</span></span>

[<span data-ttu-id="97c6b-155">新-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="97c6b-155">New-AzStorageContainer</span></span>](./New-AzStorageContainer.md)

[<span data-ttu-id="97c6b-156">移除-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="97c6b-156">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)

[<span data-ttu-id="97c6b-157">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="97c6b-157">Set-AzStorageContainerAcl</span></span>](./Set-AzStorageContainerAcl.md)


