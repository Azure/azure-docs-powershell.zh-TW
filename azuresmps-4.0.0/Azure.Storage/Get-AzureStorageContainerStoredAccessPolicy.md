---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 10D5B7E0-242B-4DC0-A527-8F6388E72E0A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4e9ea56c53d73b9c71d2eade4fec7025466ed82d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443455"
---
# <span data-ttu-id="004c1-101">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="004c1-101">Get-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="004c1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="004c1-102">SYNOPSIS</span></span>
<span data-ttu-id="004c1-103">取得 Azure 儲存體容器的儲存存取原則或原則。</span><span class="sxs-lookup"><span data-stu-id="004c1-103">Gets the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="004c1-104">句法</span><span class="sxs-lookup"><span data-stu-id="004c1-104">SYNTAX</span></span>

```
Get-AzureStorageContainerStoredAccessPolicy [-Container] <String> [[-Policy] <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="004c1-105">說明</span><span class="sxs-lookup"><span data-stu-id="004c1-105">DESCRIPTION</span></span>
<span data-ttu-id="004c1-106">**AzureStorageContainerStoredAccessPolicy** Cmdlet 會列出適用于 Azure 儲存體容器的已儲存存取原則或原則。</span><span class="sxs-lookup"><span data-stu-id="004c1-106">The **Get-AzureStorageContainerStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="004c1-107">示例</span><span class="sxs-lookup"><span data-stu-id="004c1-107">EXAMPLES</span></span>

### <span data-ttu-id="004c1-108">範例1：在儲存空間容器中取得儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="004c1-108">Example 1: Get a stored access policy in a storage container</span></span>
```
PS C:\>Get-AzureStorageContainerStoredAccessPolicy -Container "Container07" -Policy "Policy22"
```

<span data-ttu-id="004c1-109">這個命令會取得名為 Container07 的存儲容器中名為 Policy22 的訪問原則。</span><span class="sxs-lookup"><span data-stu-id="004c1-109">This command gets the access policy named Policy22 in the storage container named Container07.</span></span>

### <span data-ttu-id="004c1-110">範例2：取得儲存空間容器中所有已儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="004c1-110">Example 2: Get all the stored access policies in a storage container</span></span>
```
PS C:\>Get-AzureStorageContainerStoredAccessPolicy -Container "Container07"
```

<span data-ttu-id="004c1-111">這個命令會取得名為 Container07 的存儲容器中的所有存取原則。</span><span class="sxs-lookup"><span data-stu-id="004c1-111">This command gets all access policies in the storage container named Container07.</span></span>

## <span data-ttu-id="004c1-112">參數</span><span class="sxs-lookup"><span data-stu-id="004c1-112">PARAMETERS</span></span>

### <span data-ttu-id="004c1-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="004c1-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="004c1-114">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="004c1-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="004c1-115">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="004c1-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="004c1-116">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="004c1-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="004c1-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="004c1-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="004c1-118">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="004c1-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="004c1-119">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="004c1-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="004c1-120">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="004c1-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="004c1-121">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="004c1-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="004c1-122">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="004c1-122">The default value is 10.</span></span>

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

### <span data-ttu-id="004c1-123">-容器</span><span class="sxs-lookup"><span data-stu-id="004c1-123">-Container</span></span>
<span data-ttu-id="004c1-124">指定 Azure 儲存空間容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="004c1-124">Specifies the name of your Azure storage container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="004c1-125">-內容</span><span class="sxs-lookup"><span data-stu-id="004c1-125">-Context</span></span>
<span data-ttu-id="004c1-126">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="004c1-126">Specifies the Azure storage context.</span></span>

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

### <span data-ttu-id="004c1-127">-原則</span><span class="sxs-lookup"><span data-stu-id="004c1-127">-Policy</span></span>
<span data-ttu-id="004c1-128">指定 Azure 儲存存取原則。</span><span class="sxs-lookup"><span data-stu-id="004c1-128">Specifies the Azure stored access policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="004c1-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="004c1-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="004c1-130">指定要求的服務端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="004c1-130">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="004c1-131">如果所指定的間隔在服務處理要求之前就已到期，儲存服務就會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="004c1-131">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="004c1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="004c1-132">CommonParameters</span></span>
<span data-ttu-id="004c1-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="004c1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="004c1-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="004c1-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="004c1-135">輸入</span><span class="sxs-lookup"><span data-stu-id="004c1-135">INPUTS</span></span>

## <span data-ttu-id="004c1-136">輸出</span><span class="sxs-lookup"><span data-stu-id="004c1-136">OUTPUTS</span></span>

## <span data-ttu-id="004c1-137">筆記</span><span class="sxs-lookup"><span data-stu-id="004c1-137">NOTES</span></span>

## <span data-ttu-id="004c1-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="004c1-138">RELATED LINKS</span></span>

[<span data-ttu-id="004c1-139">新-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="004c1-139">New-AzureStorageContainerStoredAccessPolicy</span></span>](./New-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="004c1-140">移除-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="004c1-140">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="004c1-141">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="004c1-141">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)


