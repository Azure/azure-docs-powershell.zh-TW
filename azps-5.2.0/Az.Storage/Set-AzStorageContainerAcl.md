---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BDEEF1EA-A785-4E17-9887-C2000BDFCF57
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragecontaineracl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerAcl.md
ms.openlocfilehash: a23df1d7f6af188557c8e949f116e3dd12351c49
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98279906"
---
# <span data-ttu-id="3c68c-101">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="3c68c-101">Set-AzStorageContainerAcl</span></span>

## <span data-ttu-id="3c68c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3c68c-102">SYNOPSIS</span></span>
<span data-ttu-id="3c68c-103">將公用存取許可權設定為儲存容器。</span><span class="sxs-lookup"><span data-stu-id="3c68c-103">Sets the public access permission to a storage container.</span></span>

## <span data-ttu-id="3c68c-104">句法</span><span class="sxs-lookup"><span data-stu-id="3c68c-104">SYNTAX</span></span>

```
Set-AzStorageContainerAcl [-Name] <String> [-Permission] <BlobContainerPublicAccessType> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="3c68c-105">說明</span><span class="sxs-lookup"><span data-stu-id="3c68c-105">DESCRIPTION</span></span>
<span data-ttu-id="3c68c-106">**AzStorageContainerAcl** Cmdlet 會將公用存取許可權設定為 Azure 中指定的儲存空間容器。</span><span class="sxs-lookup"><span data-stu-id="3c68c-106">The **Set-AzStorageContainerAcl** cmdlet sets the public access permission to the specified storage container in Azure.</span></span>

## <span data-ttu-id="3c68c-107">示例</span><span class="sxs-lookup"><span data-stu-id="3c68c-107">EXAMPLES</span></span>

### <span data-ttu-id="3c68c-108">範例1：依名稱設定 azure 儲存空間容器 ACL</span><span class="sxs-lookup"><span data-stu-id="3c68c-108">Example 1: Set azure storage container ACL by name</span></span>
```
PS C:\>Set-AzStorageContainerAcl -Container "Container01" -Permission Off -PassThru
```

<span data-ttu-id="3c68c-109">這個命令會建立沒有公開存取權的容器。</span><span class="sxs-lookup"><span data-stu-id="3c68c-109">This command creates a container that has no public access.</span></span>

### <span data-ttu-id="3c68c-110">範例2：使用管線設定 azure 儲存體容器 ACL</span><span class="sxs-lookup"><span data-stu-id="3c68c-110">Example 2: Set azure storage container ACL by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer container* | Set-AzStorageContainerAcl -Permission Blob -PassThru
```

<span data-ttu-id="3c68c-111">這個命令會取得名稱以容器為開頭的所有儲存容器，然後在管線上傳遞結果，將它們的許可權設定為 Blob 存取。</span><span class="sxs-lookup"><span data-stu-id="3c68c-111">This command gets all storage containers whose name starts with container and then passes the result on the pipeline to set the permission for them all to Blob access.</span></span>

## <span data-ttu-id="3c68c-112">參數</span><span class="sxs-lookup"><span data-stu-id="3c68c-112">PARAMETERS</span></span>

### <span data-ttu-id="3c68c-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3c68c-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="3c68c-114">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="3c68c-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="3c68c-115">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="3c68c-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="3c68c-116">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="3c68c-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="3c68c-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="3c68c-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="3c68c-118">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="3c68c-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="3c68c-119">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="3c68c-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="3c68c-120">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="3c68c-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="3c68c-121">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="3c68c-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="3c68c-122">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="3c68c-122">The default value is 10.</span></span>

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

### <span data-ttu-id="3c68c-123">-內容</span><span class="sxs-lookup"><span data-stu-id="3c68c-123">-Context</span></span>
<span data-ttu-id="3c68c-124">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="3c68c-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="3c68c-125">您可以使用 New-AzStorageContext Cmdlet 來建立它。</span><span class="sxs-lookup"><span data-stu-id="3c68c-125">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="3c68c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c68c-126">-DefaultProfile</span></span>
<span data-ttu-id="3c68c-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3c68c-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c68c-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="3c68c-128">-Name</span></span>
<span data-ttu-id="3c68c-129">指定容器名稱。</span><span class="sxs-lookup"><span data-stu-id="3c68c-129">Specifies a container name.</span></span>

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

### <span data-ttu-id="3c68c-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3c68c-130">-PassThru</span></span>
<span data-ttu-id="3c68c-131">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="3c68c-131">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3c68c-132">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="3c68c-132">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3c68c-133">-許可權</span><span class="sxs-lookup"><span data-stu-id="3c68c-133">-Permission</span></span>
<span data-ttu-id="3c68c-134">指定此容器的公開存取層級。</span><span class="sxs-lookup"><span data-stu-id="3c68c-134">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="3c68c-135">根據預設，容器及其中的任何 blob 只能由儲存空間帳戶的擁有者存取。</span><span class="sxs-lookup"><span data-stu-id="3c68c-135">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="3c68c-136">若要授權匿名使用者讀取容器及其 blob 的許可權，您可以設定容器許可權來啟用公用存取。</span><span class="sxs-lookup"><span data-stu-id="3c68c-136">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="3c68c-137">匿名使用者可以在公開提供的容器中讀取 blob，而不需驗證要求。</span><span class="sxs-lookup"><span data-stu-id="3c68c-137">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="3c68c-138">此參數可接受的值為：--Container。</span><span class="sxs-lookup"><span data-stu-id="3c68c-138">The acceptable values for this parameter are: --Container.</span></span>
<span data-ttu-id="3c68c-139">提供容器及其 blob 的完整讀取存取權。</span><span class="sxs-lookup"><span data-stu-id="3c68c-139">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="3c68c-140">用戶端可以透過匿名要求列舉容器中的 blob，但無法在儲存空間帳戶列舉容器。</span><span class="sxs-lookup"><span data-stu-id="3c68c-140">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> <span data-ttu-id="3c68c-141">--Blob。</span><span class="sxs-lookup"><span data-stu-id="3c68c-141">--Blob.</span></span>
<span data-ttu-id="3c68c-142">透過匿名要求提供對容器中 blob 資料的讀取存取權，但不提供容器資料的存取權。</span><span class="sxs-lookup"><span data-stu-id="3c68c-142">Provides read access to blob data in a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="3c68c-143">用戶端無法使用匿名要求來列舉容器中的 blob。</span><span class="sxs-lookup"><span data-stu-id="3c68c-143">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> <span data-ttu-id="3c68c-144">-關閉。</span><span class="sxs-lookup"><span data-stu-id="3c68c-144">--Off.</span></span>
<span data-ttu-id="3c68c-145">限制僅限儲存帳戶擁有者的存取權。</span><span class="sxs-lookup"><span data-stu-id="3c68c-145">Restricts access to only the storage account owner.</span></span>

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

### <span data-ttu-id="3c68c-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3c68c-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="3c68c-147">指定要求的服務端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="3c68c-147">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="3c68c-148">如果所指定的間隔在服務處理要求之前就已到期，儲存服務就會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="3c68c-148">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>
<span data-ttu-id="3c68c-149">針對每個要求的伺服器端超時。</span><span class="sxs-lookup"><span data-stu-id="3c68c-149">Server side time out for each request.</span></span>

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

### <span data-ttu-id="3c68c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c68c-150">CommonParameters</span></span>
<span data-ttu-id="3c68c-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3c68c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c68c-152">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3c68c-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c68c-153">輸入</span><span class="sxs-lookup"><span data-stu-id="3c68c-153">INPUTS</span></span>

### <span data-ttu-id="3c68c-154">System.object</span><span class="sxs-lookup"><span data-stu-id="3c68c-154">System.String</span></span>

### <span data-ttu-id="3c68c-155">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="3c68c-155">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3c68c-156">輸出</span><span class="sxs-lookup"><span data-stu-id="3c68c-156">OUTPUTS</span></span>

### <span data-ttu-id="3c68c-157">AzureStorageContainer WindowsAzure. ResourceModel。</span><span class="sxs-lookup"><span data-stu-id="3c68c-157">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="3c68c-158">筆記</span><span class="sxs-lookup"><span data-stu-id="3c68c-158">NOTES</span></span>

## <span data-ttu-id="3c68c-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="3c68c-159">RELATED LINKS</span></span>

[<span data-ttu-id="3c68c-160">AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3c68c-160">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="3c68c-161">新-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3c68c-161">New-AzStorageContainer</span></span>](./New-AzStorageContainer.md)

[<span data-ttu-id="3c68c-162">移除-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3c68c-162">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)


