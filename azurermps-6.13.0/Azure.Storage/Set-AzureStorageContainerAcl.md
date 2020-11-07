---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: BDEEF1EA-A785-4E17-9887-C2000BDFCF57
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragecontaineracl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageContainerAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageContainerAcl.md
ms.openlocfilehash: c3451552d919b33b7dd2dcf72b8b9982f50e8b88
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624264"
---
# <span data-ttu-id="41c34-101">Set-AzureStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="41c34-101">Set-AzureStorageContainerAcl</span></span>

## <span data-ttu-id="41c34-102">摘要</span><span class="sxs-lookup"><span data-stu-id="41c34-102">SYNOPSIS</span></span>
<span data-ttu-id="41c34-103">將公用存取許可權設定為儲存容器。</span><span class="sxs-lookup"><span data-stu-id="41c34-103">Sets the public access permission to a storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41c34-104">句法</span><span class="sxs-lookup"><span data-stu-id="41c34-104">SYNTAX</span></span>

```
Set-AzureStorageContainerAcl [-Name] <String> [-Permission] <BlobContainerPublicAccessType> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="41c34-105">說明</span><span class="sxs-lookup"><span data-stu-id="41c34-105">DESCRIPTION</span></span>
<span data-ttu-id="41c34-106">**AzureStorageContainerAcl** Cmdlet 會將公用存取許可權設定為 Azure 中指定的儲存空間容器。</span><span class="sxs-lookup"><span data-stu-id="41c34-106">The **Set-AzureStorageContainerAcl** cmdlet sets the public access permission to the specified storage container in Azure.</span></span>

## <span data-ttu-id="41c34-107">示例</span><span class="sxs-lookup"><span data-stu-id="41c34-107">EXAMPLES</span></span>

### <span data-ttu-id="41c34-108">範例1：依名稱設定 azure 儲存空間容器 ACL</span><span class="sxs-lookup"><span data-stu-id="41c34-108">Example 1: Set azure storage container ACL by name</span></span>
```
PS C:\>Set-AzureStorageContainerAcl -Container "Container01" -Permission Off -PassThru
```

<span data-ttu-id="41c34-109">這個命令會建立沒有公開存取權的容器。</span><span class="sxs-lookup"><span data-stu-id="41c34-109">This command creates a container that has no public access.</span></span>

### <span data-ttu-id="41c34-110">範例2：使用管線設定 azure 儲存體容器 ACL</span><span class="sxs-lookup"><span data-stu-id="41c34-110">Example 2: Set azure storage container ACL by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer container* | Set-AzureStorageContainerAcl -Permission Blob -PassThru
```

<span data-ttu-id="41c34-111">這個命令會取得名稱以容器為開頭的所有儲存容器，然後在管線上傳遞結果，將它們的許可權設定為 Blob 存取。</span><span class="sxs-lookup"><span data-stu-id="41c34-111">This command gets all storage containers whose name starts with container and then passes the result on the pipeline to set the permission for them all to Blob access.</span></span>

## <span data-ttu-id="41c34-112">參數</span><span class="sxs-lookup"><span data-stu-id="41c34-112">PARAMETERS</span></span>

### <span data-ttu-id="41c34-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="41c34-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="41c34-114">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="41c34-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="41c34-115">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="41c34-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="41c34-116">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="41c34-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="41c34-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="41c34-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="41c34-118">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="41c34-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="41c34-119">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="41c34-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="41c34-120">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="41c34-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="41c34-121">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="41c34-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="41c34-122">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="41c34-122">The default value is 10.</span></span>

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

### <span data-ttu-id="41c34-123">-內容</span><span class="sxs-lookup"><span data-stu-id="41c34-123">-Context</span></span>
<span data-ttu-id="41c34-124">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="41c34-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="41c34-125">您可以使用 New-AzureStorageContext Cmdlet 來建立它。</span><span class="sxs-lookup"><span data-stu-id="41c34-125">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="41c34-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41c34-126">-DefaultProfile</span></span>
<span data-ttu-id="41c34-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="41c34-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41c34-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="41c34-128">-Name</span></span>
<span data-ttu-id="41c34-129">指定容器名稱。</span><span class="sxs-lookup"><span data-stu-id="41c34-129">Specifies a container name.</span></span>

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

### <span data-ttu-id="41c34-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41c34-130">-PassThru</span></span>
<span data-ttu-id="41c34-131">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="41c34-131">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="41c34-132">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="41c34-132">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="41c34-133">-許可權</span><span class="sxs-lookup"><span data-stu-id="41c34-133">-Permission</span></span>
<span data-ttu-id="41c34-134">指定此容器的公開存取層級。</span><span class="sxs-lookup"><span data-stu-id="41c34-134">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="41c34-135">根據預設，容器及其中的任何 blob 只能由儲存空間帳戶的擁有者存取。</span><span class="sxs-lookup"><span data-stu-id="41c34-135">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="41c34-136">若要授權匿名使用者讀取容器及其 blob 的許可權，您可以設定容器許可權來啟用公用存取。</span><span class="sxs-lookup"><span data-stu-id="41c34-136">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="41c34-137">匿名使用者可以在公開提供的容器中讀取 blob，而不需驗證要求。</span><span class="sxs-lookup"><span data-stu-id="41c34-137">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="41c34-138">此參數可接受的值為：--Container。</span><span class="sxs-lookup"><span data-stu-id="41c34-138">The acceptable values for this parameter are: --Container.</span></span>
<span data-ttu-id="41c34-139">提供容器及其 blob 的完整讀取存取權。</span><span class="sxs-lookup"><span data-stu-id="41c34-139">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="41c34-140">用戶端可以透過匿名要求列舉容器中的 blob，但無法在儲存空間帳戶列舉容器。</span><span class="sxs-lookup"><span data-stu-id="41c34-140">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> <span data-ttu-id="41c34-141">--Blob。</span><span class="sxs-lookup"><span data-stu-id="41c34-141">--Blob.</span></span>
<span data-ttu-id="41c34-142">透過匿名要求提供對容器中 blob 資料的讀取存取權，但不提供容器資料的存取權。</span><span class="sxs-lookup"><span data-stu-id="41c34-142">Provides read access to blob data in a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="41c34-143">用戶端無法使用匿名要求來列舉容器中的 blob。</span><span class="sxs-lookup"><span data-stu-id="41c34-143">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> <span data-ttu-id="41c34-144">-關閉。</span><span class="sxs-lookup"><span data-stu-id="41c34-144">--Off.</span></span>
<span data-ttu-id="41c34-145">限制僅限儲存帳戶擁有者的存取權。</span><span class="sxs-lookup"><span data-stu-id="41c34-145">Restricts access to only the storage account owner.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.BlobContainerPublicAccessType
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob, Unknown

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41c34-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="41c34-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="41c34-147">指定要求的服務端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="41c34-147">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="41c34-148">如果所指定的間隔在服務處理要求之前就已到期，儲存服務就會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="41c34-148">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>
<span data-ttu-id="41c34-149">針對每個要求的伺服器端超時。</span><span class="sxs-lookup"><span data-stu-id="41c34-149">Server side time out for each request.</span></span>

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

### <span data-ttu-id="41c34-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41c34-150">CommonParameters</span></span>
<span data-ttu-id="41c34-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="41c34-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41c34-152">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="41c34-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41c34-153">輸入</span><span class="sxs-lookup"><span data-stu-id="41c34-153">INPUTS</span></span>

### <span data-ttu-id="41c34-154">System.object</span><span class="sxs-lookup"><span data-stu-id="41c34-154">System.String</span></span>

### <span data-ttu-id="41c34-155">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="41c34-155">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="41c34-156">輸出</span><span class="sxs-lookup"><span data-stu-id="41c34-156">OUTPUTS</span></span>

### <span data-ttu-id="41c34-157">AzureStorageContainer WindowsAzure. ResourceModel。</span><span class="sxs-lookup"><span data-stu-id="41c34-157">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="41c34-158">筆記</span><span class="sxs-lookup"><span data-stu-id="41c34-158">NOTES</span></span>

## <span data-ttu-id="41c34-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="41c34-159">RELATED LINKS</span></span>

[<span data-ttu-id="41c34-160">AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="41c34-160">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="41c34-161">新-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="41c34-161">New-AzureStorageContainer</span></span>](./New-AzureStorageContainer.md)

[<span data-ttu-id="41c34-162">移除-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="41c34-162">Remove-AzureStorageContainer</span></span>](./Remove-AzureStorageContainer.md)


