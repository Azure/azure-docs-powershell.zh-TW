---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 10D5B7E0-242B-4DC0-A527-8F6388E72E0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 5a0f976d561396bc93facfeedcbb1c89c768e5b2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98285460"
---
# <span data-ttu-id="c1c80-101">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c1c80-101">Get-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="c1c80-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c1c80-102">SYNOPSIS</span></span>
<span data-ttu-id="c1c80-103">取得 Azure 儲存體容器的儲存存取原則或原則。</span><span class="sxs-lookup"><span data-stu-id="c1c80-103">Gets the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="c1c80-104">句法</span><span class="sxs-lookup"><span data-stu-id="c1c80-104">SYNTAX</span></span>

```
Get-AzStorageContainerStoredAccessPolicy [-Container] <String> [[-Policy] <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="c1c80-105">說明</span><span class="sxs-lookup"><span data-stu-id="c1c80-105">DESCRIPTION</span></span>
<span data-ttu-id="c1c80-106">**AzStorageContainerStoredAccessPolicy** Cmdlet 會列出適用于 Azure 儲存體容器的已儲存存取原則或原則。</span><span class="sxs-lookup"><span data-stu-id="c1c80-106">The **Get-AzStorageContainerStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="c1c80-107">示例</span><span class="sxs-lookup"><span data-stu-id="c1c80-107">EXAMPLES</span></span>

### <span data-ttu-id="c1c80-108">範例1：在儲存空間容器中取得儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="c1c80-108">Example 1: Get a stored access policy in a storage container</span></span>
```
PS C:\>Get-AzStorageContainerStoredAccessPolicy -Container "Container07" -Policy "Policy22"
```

<span data-ttu-id="c1c80-109">這個命令會取得名為 Container07 的存儲容器中名為 Policy22 的訪問原則。</span><span class="sxs-lookup"><span data-stu-id="c1c80-109">This command gets the access policy named Policy22 in the storage container named Container07.</span></span>

### <span data-ttu-id="c1c80-110">範例2：取得儲存空間容器中所有已儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="c1c80-110">Example 2: Get all the stored access policies in a storage container</span></span>
```
PS C:\>Get-AzStorageContainerStoredAccessPolicy -Container "Container07"
```

<span data-ttu-id="c1c80-111">這個命令會取得名為 Container07 的存儲容器中的所有存取原則。</span><span class="sxs-lookup"><span data-stu-id="c1c80-111">This command gets all access policies in the storage container named Container07.</span></span>

## <span data-ttu-id="c1c80-112">參數</span><span class="sxs-lookup"><span data-stu-id="c1c80-112">PARAMETERS</span></span>

### <span data-ttu-id="c1c80-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c1c80-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c1c80-114">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="c1c80-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c1c80-115">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="c1c80-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c1c80-116">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="c1c80-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c1c80-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c1c80-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c1c80-118">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="c1c80-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="c1c80-119">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="c1c80-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="c1c80-120">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="c1c80-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="c1c80-121">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="c1c80-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="c1c80-122">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="c1c80-122">The default value is 10.</span></span>

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

### <span data-ttu-id="c1c80-123">-容器</span><span class="sxs-lookup"><span data-stu-id="c1c80-123">-Container</span></span>
<span data-ttu-id="c1c80-124">指定 Azure 儲存空間容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="c1c80-124">Specifies the name of your Azure storage container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1c80-125">-內容</span><span class="sxs-lookup"><span data-stu-id="c1c80-125">-Context</span></span>
<span data-ttu-id="c1c80-126">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="c1c80-126">Specifies the Azure storage context.</span></span>

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

### <span data-ttu-id="c1c80-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1c80-127">-DefaultProfile</span></span>
<span data-ttu-id="c1c80-128">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c1c80-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1c80-129">-原則</span><span class="sxs-lookup"><span data-stu-id="c1c80-129">-Policy</span></span>
<span data-ttu-id="c1c80-130">指定 Azure 儲存存取原則。</span><span class="sxs-lookup"><span data-stu-id="c1c80-130">Specifies the Azure stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1c80-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c1c80-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c1c80-132">指定要求的服務端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="c1c80-132">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="c1c80-133">如果所指定的間隔在服務處理要求之前就已到期，儲存服務就會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="c1c80-133">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="c1c80-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1c80-134">CommonParameters</span></span>
<span data-ttu-id="c1c80-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c1c80-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1c80-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c1c80-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1c80-137">輸入</span><span class="sxs-lookup"><span data-stu-id="c1c80-137">INPUTS</span></span>

### <span data-ttu-id="c1c80-138">System.object</span><span class="sxs-lookup"><span data-stu-id="c1c80-138">System.String</span></span>

### <span data-ttu-id="c1c80-139">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="c1c80-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c1c80-140">輸出</span><span class="sxs-lookup"><span data-stu-id="c1c80-140">OUTPUTS</span></span>

### <span data-ttu-id="c1c80-141">[SharedAccessBlobPolicy]。</span><span class="sxs-lookup"><span data-stu-id="c1c80-141">Microsoft.Azure.Storage.Blob.SharedAccessBlobPolicy</span></span>

## <span data-ttu-id="c1c80-142">筆記</span><span class="sxs-lookup"><span data-stu-id="c1c80-142">NOTES</span></span>

## <span data-ttu-id="c1c80-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="c1c80-143">RELATED LINKS</span></span>

[<span data-ttu-id="c1c80-144">新-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c1c80-144">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="c1c80-145">移除-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c1c80-145">Remove-AzStorageContainerStoredAccessPolicy</span></span>](./Remove-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="c1c80-146">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c1c80-146">Set-AzStorageContainerStoredAccessPolicy</span></span>](./Set-AzStorageContainerStoredAccessPolicy.md)


