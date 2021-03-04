---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 2B12BC19-EF8F-43F5-AF04-C570FEEA1AE6
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
ms.openlocfilehash: d726ec3fe70ca329f6e5c07ea7aae46de4ad048a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915090"
---
# <span data-ttu-id="9a640-101">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9a640-101">New-AzStorageContainer</span></span>

## <span data-ttu-id="9a640-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9a640-102">SYNOPSIS</span></span>
<span data-ttu-id="9a640-103">建立 Azure 儲存容器。</span><span class="sxs-lookup"><span data-stu-id="9a640-103">Creates an Azure storage container.</span></span>

## <span data-ttu-id="9a640-104">語法</span><span class="sxs-lookup"><span data-stu-id="9a640-104">SYNTAX</span></span>

### <span data-ttu-id="9a640-105">ContainerName (預設) </span><span class="sxs-lookup"><span data-stu-id="9a640-105">ContainerName (Default)</span></span>
```
New-AzStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="9a640-106">EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="9a640-106">EncryptionScope</span></span>
```
New-AzStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 -DefaultEncryptionScope <String> -PreventEncryptionScopeOverride <Boolean> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="9a640-107">描述</span><span class="sxs-lookup"><span data-stu-id="9a640-107">DESCRIPTION</span></span>
<span data-ttu-id="9a640-108">**New-AzStorageContainer** Cmdlet 會建立 Azure 儲存容器。</span><span class="sxs-lookup"><span data-stu-id="9a640-108">The **New-AzStorageContainer** cmdlet creates an Azure storage container.</span></span>

## <span data-ttu-id="9a640-109">例子</span><span class="sxs-lookup"><span data-stu-id="9a640-109">EXAMPLES</span></span>

### <span data-ttu-id="9a640-110">範例 1：建立 Azure 儲存容器</span><span class="sxs-lookup"><span data-stu-id="9a640-110">Example 1: Create an Azure storage container</span></span>
```
PS C:\>New-AzStorageContainer -Name "ContainerName" -Permission Off
```

<span data-ttu-id="9a640-111">此命令會建立儲存容器。</span><span class="sxs-lookup"><span data-stu-id="9a640-111">This command creates a storage container.</span></span>

### <span data-ttu-id="9a640-112">範例 2：建立多個 Azure 儲存容器</span><span class="sxs-lookup"><span data-stu-id="9a640-112">Example 2: Create multiple Azure storage containers</span></span>
```
PS C:\>"container1 container2 container3".split() | New-AzStorageContainer -Permission Container
```

<span data-ttu-id="9a640-113">此範例會建立多個儲存容器。</span><span class="sxs-lookup"><span data-stu-id="9a640-113">This example creates multiple storage containers.</span></span>
<span data-ttu-id="9a640-114">它 **使用** .NET **String** 類的 Split 方法，然後傳遞管線上的名稱。</span><span class="sxs-lookup"><span data-stu-id="9a640-114">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

### <span data-ttu-id="9a640-115">範例 3：使用加密範圍建立 Azure 儲存容器</span><span class="sxs-lookup"><span data-stu-id="9a640-115">Example 3: Create an Azure storage container with Encryption Scope</span></span>
```
PS C:\> $container = New-AzStorageContainer  -Name "mycontainer" -DefaultEncryptionScope "myencryptscope" -PreventEncryptionScopeOverride $true 

PS C:\> $container.BlobContainerProperties.DefaultEncryptionScope
myencryptscope

PS C:\> $container.BlobContainerProperties.PreventEncryptionScopeOverride
True
```

<span data-ttu-id="9a640-116">此命令會建立儲存容器，使用預設加密範圍做為 myencryptscope，並使用不同的加密範圍預先轉換 Blob 上傳至此容器。</span><span class="sxs-lookup"><span data-stu-id="9a640-116">This command creates a storage container, with default Encryption Scope as myencryptscope, and prevert blob upload with different Encryption Scope to this container.</span></span>

## <span data-ttu-id="9a640-117">參數</span><span class="sxs-lookup"><span data-stu-id="9a640-117">PARAMETERS</span></span>

### <span data-ttu-id="9a640-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9a640-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="9a640-119">指定一個服務要求用戶端的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="9a640-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="9a640-120">如果前一個通話在指定的時間間隔內失敗，此 Cmdlet 會重新重試要求。</span><span class="sxs-lookup"><span data-stu-id="9a640-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="9a640-121">如果此 Cmdlet 在間隔經過之前未收到成功回應，此 Cmdlet 會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="9a640-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="9a640-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="9a640-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="9a640-123">指定同時進行的最大網路通話數。</span><span class="sxs-lookup"><span data-stu-id="9a640-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="9a640-124">您可以使用此參數來限制並行，以節流本地 CPU 和頻寬使用量，方法為指定並行網路通話的數量上限。</span><span class="sxs-lookup"><span data-stu-id="9a640-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="9a640-125">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="9a640-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="9a640-126">此參數有助於減少低頻寬環境的網路連接問題，例如每秒 100 KB。</span><span class="sxs-lookup"><span data-stu-id="9a640-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="9a640-127">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="9a640-127">The default value is 10.</span></span>

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

### <span data-ttu-id="9a640-128">-內容</span><span class="sxs-lookup"><span data-stu-id="9a640-128">-Context</span></span>
<span data-ttu-id="9a640-129">指定新容器的上下文。</span><span class="sxs-lookup"><span data-stu-id="9a640-129">Specifies a context for the new container.</span></span>

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

### <span data-ttu-id="9a640-130">-DefaultEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="9a640-130">-DefaultEncryptionScope</span></span>
<span data-ttu-id="9a640-131">將容器預設為針對所有寫入使用指定的加密範圍。</span><span class="sxs-lookup"><span data-stu-id="9a640-131">Default the container to use specified encryption scope for all writes.</span></span>

```yaml
Type: System.String
Parameter Sets: EncryptionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a640-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a640-132">-DefaultProfile</span></span>
<span data-ttu-id="9a640-133">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9a640-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a640-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="9a640-134">-Name</span></span>
<span data-ttu-id="9a640-135">指定新容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="9a640-135">Specifies a name for the new container.</span></span>

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

### <span data-ttu-id="9a640-136">-許可權</span><span class="sxs-lookup"><span data-stu-id="9a640-136">-Permission</span></span>
<span data-ttu-id="9a640-137">指定此容器的公用存取層級。</span><span class="sxs-lookup"><span data-stu-id="9a640-137">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="9a640-138">根據預設，容器及其中任何 Blob 只能由儲存帳戶的擁有者存取。</span><span class="sxs-lookup"><span data-stu-id="9a640-138">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="9a640-139">若要將匿名使用者的讀取權限授予容器及其 Blob，您可以設定容器許可權以啟用公用存取。</span><span class="sxs-lookup"><span data-stu-id="9a640-139">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="9a640-140">匿名使用者可以讀取公開容器中的 Blob，而不必驗證要求。</span><span class="sxs-lookup"><span data-stu-id="9a640-140">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="9a640-141">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="9a640-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9a640-142">容器。</span><span class="sxs-lookup"><span data-stu-id="9a640-142">Container.</span></span>
<span data-ttu-id="9a640-143">提供容器及其 Blob 的完整讀取存取權。</span><span class="sxs-lookup"><span data-stu-id="9a640-143">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="9a640-144">用戶端可以透過匿名要求列舉容器中的 Blob，但無法列舉儲存帳戶中的容器。</span><span class="sxs-lookup"><span data-stu-id="9a640-144">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> 
- <span data-ttu-id="9a640-145">Blob。</span><span class="sxs-lookup"><span data-stu-id="9a640-145">Blob.</span></span>
<span data-ttu-id="9a640-146">透過匿名要求，在整個容器內提供 Blob 資料的讀取存取，但不提供容器資料的存取權。</span><span class="sxs-lookup"><span data-stu-id="9a640-146">Provides read access to blob data throughout a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="9a640-147">用戶端無法使用匿名要求列舉容器中的 Blob。</span><span class="sxs-lookup"><span data-stu-id="9a640-147">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> 
- <span data-ttu-id="9a640-148">關閉。</span><span class="sxs-lookup"><span data-stu-id="9a640-148">Off.</span></span>
<span data-ttu-id="9a640-149">這只會限制存取儲存空間帳戶擁有者。</span><span class="sxs-lookup"><span data-stu-id="9a640-149">Which restricts access to only the storage account owner.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.Blob.BlobContainerPublicAccessType]
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob, Unknown

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a640-150">-PreventEncryptionScopeOverride</span><span class="sxs-lookup"><span data-stu-id="9a640-150">-PreventEncryptionScopeOverride</span></span>
<span data-ttu-id="9a640-151">從容器預設封鎖加密範圍的重寫。</span><span class="sxs-lookup"><span data-stu-id="9a640-151">Block override of encryption scope from the container default.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: EncryptionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a640-152">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9a640-152">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="9a640-153">指定服務端要求的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="9a640-153">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="9a640-154">如果指定的時間間隔在服務處理要求之前已經過，儲存服務會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="9a640-154">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="9a640-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a640-155">CommonParameters</span></span>
<span data-ttu-id="9a640-156">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9a640-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a640-157">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="9a640-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a640-158">輸入</span><span class="sxs-lookup"><span data-stu-id="9a640-158">INPUTS</span></span>

### <span data-ttu-id="9a640-159">System.String</span><span class="sxs-lookup"><span data-stu-id="9a640-159">System.String</span></span>

### <span data-ttu-id="9a640-160">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="9a640-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9a640-161">輸出</span><span class="sxs-lookup"><span data-stu-id="9a640-161">OUTPUTS</span></span>

### <span data-ttu-id="9a640-162">Microsoft.WindowsAzure.Commands.Common.storage.ResourceModel.AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9a640-162">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="9a640-163">筆記</span><span class="sxs-lookup"><span data-stu-id="9a640-163">NOTES</span></span>

## <span data-ttu-id="9a640-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="9a640-164">RELATED LINKS</span></span>

[<span data-ttu-id="9a640-165">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9a640-165">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="9a640-166">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9a640-166">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)

[<span data-ttu-id="9a640-167">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="9a640-167">Set-AzStorageContainerAcl</span></span>](./Set-AzStorageContainerAcl.md)


