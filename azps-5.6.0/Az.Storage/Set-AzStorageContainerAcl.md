---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BDEEF1EA-A785-4E17-9887-C2000BDFCF57
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azstoragecontaineracl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerAcl.md
ms.openlocfilehash: 23aa7e6df5aae820980551db445339ade34ac779
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915021"
---
# <span data-ttu-id="34540-101">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="34540-101">Set-AzStorageContainerAcl</span></span>

## <span data-ttu-id="34540-102">簡介</span><span class="sxs-lookup"><span data-stu-id="34540-102">SYNOPSIS</span></span>
<span data-ttu-id="34540-103">設定儲存容器的公用存取權限。</span><span class="sxs-lookup"><span data-stu-id="34540-103">Sets the public access permission to a storage container.</span></span>

## <span data-ttu-id="34540-104">語法</span><span class="sxs-lookup"><span data-stu-id="34540-104">SYNTAX</span></span>

```
Set-AzStorageContainerAcl [-Name] <String> [-Permission] <BlobContainerPublicAccessType> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="34540-105">描述</span><span class="sxs-lookup"><span data-stu-id="34540-105">DESCRIPTION</span></span>
<span data-ttu-id="34540-106">**Set-AzStorageContainerAcl** Cmdlet 會設定 Azure 中指定儲存容器的公用存取權限。</span><span class="sxs-lookup"><span data-stu-id="34540-106">The **Set-AzStorageContainerAcl** cmdlet sets the public access permission to the specified storage container in Azure.</span></span>

## <span data-ttu-id="34540-107">例子</span><span class="sxs-lookup"><span data-stu-id="34540-107">EXAMPLES</span></span>

### <span data-ttu-id="34540-108">範例 1：根據名稱設定 Azure 儲存容器 ACL</span><span class="sxs-lookup"><span data-stu-id="34540-108">Example 1: Set azure storage container ACL by name</span></span>
```
PS C:\>Set-AzStorageContainerAcl -Container "Container01" -Permission Off -PassThru
```

<span data-ttu-id="34540-109">此命令會建立沒有公用存取的容器。</span><span class="sxs-lookup"><span data-stu-id="34540-109">This command creates a container that has no public access.</span></span>

### <span data-ttu-id="34540-110">範例 2：使用管線設定 Azure 儲存容器 ACL</span><span class="sxs-lookup"><span data-stu-id="34540-110">Example 2: Set azure storage container ACL by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer container* | Set-AzStorageContainerAcl -Permission Blob -PassThru
```

<span data-ttu-id="34540-111">此命令會取得名稱以容器開頭的所有儲存容器，然後傳遞管線上的結果，以設定所有容器對 Blob 存取的許可權。</span><span class="sxs-lookup"><span data-stu-id="34540-111">This command gets all storage containers whose name starts with container and then passes the result on the pipeline to set the permission for them all to Blob access.</span></span>

## <span data-ttu-id="34540-112">參數</span><span class="sxs-lookup"><span data-stu-id="34540-112">PARAMETERS</span></span>

### <span data-ttu-id="34540-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="34540-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="34540-114">指定一個服務要求用戶端的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="34540-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="34540-115">如果前一個通話在指定的時間間隔內失敗，此 Cmdlet 會重新重試要求。</span><span class="sxs-lookup"><span data-stu-id="34540-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="34540-116">如果此 Cmdlet 在間隔經過之前未收到成功回應，此 Cmdlet 會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="34540-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="34540-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="34540-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="34540-118">指定同時進行的最大網路通話數。</span><span class="sxs-lookup"><span data-stu-id="34540-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="34540-119">您可以使用此參數來限制並行，以節流本地 CPU 和頻寬使用量，方法為指定並行網路通話的數量上限。</span><span class="sxs-lookup"><span data-stu-id="34540-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="34540-120">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="34540-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="34540-121">此參數有助於減少低頻寬環境的網路連接問題，例如每秒 100 KB。</span><span class="sxs-lookup"><span data-stu-id="34540-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="34540-122">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="34540-122">The default value is 10.</span></span>

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

### <span data-ttu-id="34540-123">-內容</span><span class="sxs-lookup"><span data-stu-id="34540-123">-Context</span></span>
<span data-ttu-id="34540-124">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="34540-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="34540-125">您可以使用 Cmdlet New-AzStorageContext建立。</span><span class="sxs-lookup"><span data-stu-id="34540-125">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="34540-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34540-126">-DefaultProfile</span></span>
<span data-ttu-id="34540-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="34540-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34540-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="34540-128">-Name</span></span>
<span data-ttu-id="34540-129">指定容器名稱。</span><span class="sxs-lookup"><span data-stu-id="34540-129">Specifies a container name.</span></span>

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

### <span data-ttu-id="34540-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="34540-130">-PassThru</span></span>
<span data-ttu-id="34540-131">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="34540-131">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="34540-132">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="34540-132">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="34540-133">-許可權</span><span class="sxs-lookup"><span data-stu-id="34540-133">-Permission</span></span>
<span data-ttu-id="34540-134">指定此容器的公用存取層級。</span><span class="sxs-lookup"><span data-stu-id="34540-134">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="34540-135">根據預設，容器及其中任何 Blob 只能由儲存帳戶的擁有者存取。</span><span class="sxs-lookup"><span data-stu-id="34540-135">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="34540-136">若要將匿名使用者的讀取權限授予容器及其 Blob，您可以設定容器許可權以啟用公用存取。</span><span class="sxs-lookup"><span data-stu-id="34540-136">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="34540-137">匿名使用者可以讀取公開容器中的 Blob，而不必驗證要求。</span><span class="sxs-lookup"><span data-stu-id="34540-137">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="34540-138">此參數可接受的值為：--Container。</span><span class="sxs-lookup"><span data-stu-id="34540-138">The acceptable values for this parameter are: --Container.</span></span>
<span data-ttu-id="34540-139">提供容器及其 Blob 的完整讀取存取權。</span><span class="sxs-lookup"><span data-stu-id="34540-139">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="34540-140">用戶端可以透過匿名要求列舉容器中的 Blob，但無法列舉儲存帳戶中的容器。</span><span class="sxs-lookup"><span data-stu-id="34540-140">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> <span data-ttu-id="34540-141">--Blob。</span><span class="sxs-lookup"><span data-stu-id="34540-141">--Blob.</span></span>
<span data-ttu-id="34540-142">透過匿名要求提供對容器中 Blob 資料的讀取存取，但不提供容器資料的存取權。</span><span class="sxs-lookup"><span data-stu-id="34540-142">Provides read access to blob data in a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="34540-143">用戶端無法使用匿名要求列舉容器中的 Blob。</span><span class="sxs-lookup"><span data-stu-id="34540-143">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> <span data-ttu-id="34540-144">--關閉。</span><span class="sxs-lookup"><span data-stu-id="34540-144">--Off.</span></span>
<span data-ttu-id="34540-145">僅限制存取儲存空間帳戶擁有者。</span><span class="sxs-lookup"><span data-stu-id="34540-145">Restricts access to only the storage account owner.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.BlobContainerPublicAccessType
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob, Unknown

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34540-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="34540-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="34540-147">指定服務端要求的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="34540-147">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="34540-148">如果指定的時間間隔在服務處理要求之前已經過，儲存服務會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="34540-148">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>
<span data-ttu-id="34540-149">伺服器端會針對每個要求排時。</span><span class="sxs-lookup"><span data-stu-id="34540-149">Server side time out for each request.</span></span>

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

### <span data-ttu-id="34540-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34540-150">CommonParameters</span></span>
<span data-ttu-id="34540-151">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="34540-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34540-152">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="34540-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34540-153">輸入</span><span class="sxs-lookup"><span data-stu-id="34540-153">INPUTS</span></span>

### <span data-ttu-id="34540-154">System.String</span><span class="sxs-lookup"><span data-stu-id="34540-154">System.String</span></span>

### <span data-ttu-id="34540-155">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="34540-155">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="34540-156">輸出</span><span class="sxs-lookup"><span data-stu-id="34540-156">OUTPUTS</span></span>

### <span data-ttu-id="34540-157">Microsoft.WindowsAzure.Commands.Common.storage.ResourceModel.AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="34540-157">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="34540-158">筆記</span><span class="sxs-lookup"><span data-stu-id="34540-158">NOTES</span></span>

## <span data-ttu-id="34540-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="34540-159">RELATED LINKS</span></span>

[<span data-ttu-id="34540-160">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="34540-160">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="34540-161">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="34540-161">New-AzStorageContainer</span></span>](./New-AzStorageContainer.md)

[<span data-ttu-id="34540-162">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="34540-162">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)


