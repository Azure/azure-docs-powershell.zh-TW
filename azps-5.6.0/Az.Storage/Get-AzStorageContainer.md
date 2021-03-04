---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 90C3DF13-0010-49B6-A8CD-C6AC34BC3EFA
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainer.md
ms.openlocfilehash: 15aefebea30e829371c57c3c1cd575a604b81eaf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909305"
---
# <span data-ttu-id="3a01d-101">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3a01d-101">Get-AzStorageContainer</span></span>

## <span data-ttu-id="3a01d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3a01d-102">SYNOPSIS</span></span>
<span data-ttu-id="3a01d-103">列出儲存容器。</span><span class="sxs-lookup"><span data-stu-id="3a01d-103">Lists the storage containers.</span></span>

## <span data-ttu-id="3a01d-104">語法</span><span class="sxs-lookup"><span data-stu-id="3a01d-104">SYNTAX</span></span>

### <span data-ttu-id="3a01d-105">ContainerName (預設) </span><span class="sxs-lookup"><span data-stu-id="3a01d-105">ContainerName (Default)</span></span>
```
Get-AzStorageContainer [[-Name] <String>] [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="3a01d-106">ContainerPrefix</span><span class="sxs-lookup"><span data-stu-id="3a01d-106">ContainerPrefix</span></span>
```
Get-AzStorageContainer -Prefix <String> [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="3a01d-107">描述</span><span class="sxs-lookup"><span data-stu-id="3a01d-107">DESCRIPTION</span></span>
<span data-ttu-id="3a01d-108">**Get-AzStorageContainer Cmdlet** 會列出與 Azure 中儲存帳戶相關聯的儲存容器。</span><span class="sxs-lookup"><span data-stu-id="3a01d-108">The **Get-AzStorageContainer** cmdlet lists the storage containers associated with the storage account in Azure.</span></span>

## <span data-ttu-id="3a01d-109">例子</span><span class="sxs-lookup"><span data-stu-id="3a01d-109">EXAMPLES</span></span>

### <span data-ttu-id="3a01d-110">範例 1：按名稱取得 Azure 儲存體 Blob</span><span class="sxs-lookup"><span data-stu-id="3a01d-110">Example 1: Get Azure Storage blob by name</span></span>
```
PS C:\>Get-AzStorageContainer -Name container*
```

<span data-ttu-id="3a01d-111">此範例使用萬用字元來會以容器開頭的名稱，來返回所有容器的清單。</span><span class="sxs-lookup"><span data-stu-id="3a01d-111">This example uses a wildcard character to return a list of all containers with a name that starts with container.</span></span>

### <span data-ttu-id="3a01d-112">範例 2：使用容器名稱首碼取得 Azure 儲存容器</span><span class="sxs-lookup"><span data-stu-id="3a01d-112">Example 2: Get Azure Storage container by container name prefix</span></span>
```
PS C:\>Get-AzStorageContainer -Prefix "container"
```

<span data-ttu-id="3a01d-113">此範例使用 *首碼* 參數，會以容器開頭的名稱，來返回所有容器的清單。</span><span class="sxs-lookup"><span data-stu-id="3a01d-113">This example uses the *Prefix* parameter to return a list of all containers with a name that starts with container.</span></span>

## <span data-ttu-id="3a01d-114">參數</span><span class="sxs-lookup"><span data-stu-id="3a01d-114">PARAMETERS</span></span>

### <span data-ttu-id="3a01d-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3a01d-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="3a01d-116">指定一個服務要求用戶端的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="3a01d-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="3a01d-117">如果前一個通話在指定的時間間隔內失敗，此 Cmdlet 會重新重試要求。</span><span class="sxs-lookup"><span data-stu-id="3a01d-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="3a01d-118">如果此 Cmdlet 在間隔經過之前未收到成功回應，此 Cmdlet 會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="3a01d-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="3a01d-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="3a01d-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="3a01d-120">指定同時進行的最大網路通話數。</span><span class="sxs-lookup"><span data-stu-id="3a01d-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="3a01d-121">您可以使用此參數來限制並行，以節流本地 CPU 和頻寬使用量，方法為指定並行網路通話的數量上限。</span><span class="sxs-lookup"><span data-stu-id="3a01d-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="3a01d-122">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="3a01d-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="3a01d-123">此參數有助於減少低頻寬環境的網路連接問題，例如每秒 100 KB。</span><span class="sxs-lookup"><span data-stu-id="3a01d-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="3a01d-124">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="3a01d-124">The default value is 10.</span></span>

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

### <span data-ttu-id="3a01d-125">-內容</span><span class="sxs-lookup"><span data-stu-id="3a01d-125">-Context</span></span>
<span data-ttu-id="3a01d-126">指定儲存內容。</span><span class="sxs-lookup"><span data-stu-id="3a01d-126">Specifies the storage context.</span></span>
<span data-ttu-id="3a01d-127">若要建立，您可以使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3a01d-127">To create it, you can use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="3a01d-128">當您使用從 SAS Token 建立儲存內容時，不會取回容器許可權，因為查詢容器許可權需要儲存帳戶金鑰許可權。</span><span class="sxs-lookup"><span data-stu-id="3a01d-128">The container permissions won't be retrieved when you use a storage context created from SAS Token, because query container permissions requires Storage account key permission.</span></span>

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

### <span data-ttu-id="3a01d-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="3a01d-129">-ContinuationToken</span></span>
<span data-ttu-id="3a01d-130">指定 Blob 清單的延續權杖。</span><span class="sxs-lookup"><span data-stu-id="3a01d-130">Specifies a continuation token for the blob list.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.BlobContinuationToken
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a01d-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a01d-131">-DefaultProfile</span></span>
<span data-ttu-id="3a01d-132">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3a01d-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a01d-133">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="3a01d-133">-MaxCount</span></span>
<span data-ttu-id="3a01d-134">指定此 Cmdlet 會返回的物件數量上限。</span><span class="sxs-lookup"><span data-stu-id="3a01d-134">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="3a01d-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="3a01d-135">-Name</span></span>
<span data-ttu-id="3a01d-136">指定容器名稱。</span><span class="sxs-lookup"><span data-stu-id="3a01d-136">Specifies the container name.</span></span>
<span data-ttu-id="3a01d-137">如果容器名稱為空白，Cmdlet 會列出所有容器。</span><span class="sxs-lookup"><span data-stu-id="3a01d-137">If container name is empty, the cmdlet lists all the containers.</span></span>
<span data-ttu-id="3a01d-138">否則，它會列出符合指定名稱或一般名稱模式的所有容器。</span><span class="sxs-lookup"><span data-stu-id="3a01d-138">Otherwise, it lists all containers that match the specified name or the regular name pattern.</span></span>

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

### <span data-ttu-id="3a01d-139">-首碼</span><span class="sxs-lookup"><span data-stu-id="3a01d-139">-Prefix</span></span>
<span data-ttu-id="3a01d-140">指定您想要取得之容器名稱中使用的首碼。</span><span class="sxs-lookup"><span data-stu-id="3a01d-140">Specifies a prefix used in the name of the container or containers you want to get.</span></span>
<span data-ttu-id="3a01d-141">您可以使用這個來尋找以相同字串開頭的所有容器，例如 "my" 或 "test"。</span><span class="sxs-lookup"><span data-stu-id="3a01d-141">You can use this to find all containers that start with the same string, such as "my" or "test".</span></span>

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

### <span data-ttu-id="3a01d-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3a01d-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="3a01d-143">指定服務端要求的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="3a01d-143">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="3a01d-144">如果指定的時間間隔在服務處理要求之前已經過，儲存服務會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="3a01d-144">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="3a01d-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a01d-145">CommonParameters</span></span>
<span data-ttu-id="3a01d-146">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3a01d-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a01d-147">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="3a01d-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a01d-148">輸入</span><span class="sxs-lookup"><span data-stu-id="3a01d-148">INPUTS</span></span>

### <span data-ttu-id="3a01d-149">System.String</span><span class="sxs-lookup"><span data-stu-id="3a01d-149">System.String</span></span>

### <span data-ttu-id="3a01d-150">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="3a01d-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3a01d-151">輸出</span><span class="sxs-lookup"><span data-stu-id="3a01d-151">OUTPUTS</span></span>

### <span data-ttu-id="3a01d-152">Microsoft.WindowsAzure.Commands.Common.storage.ResourceModel.AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3a01d-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="3a01d-153">筆記</span><span class="sxs-lookup"><span data-stu-id="3a01d-153">NOTES</span></span>

## <span data-ttu-id="3a01d-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="3a01d-154">RELATED LINKS</span></span>

[<span data-ttu-id="3a01d-155">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3a01d-155">New-AzStorageContainer</span></span>](./New-AzStorageContainer.md)

[<span data-ttu-id="3a01d-156">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3a01d-156">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)

[<span data-ttu-id="3a01d-157">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="3a01d-157">Set-AzStorageContainerAcl</span></span>](./Set-AzStorageContainerAcl.md)


