---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 26E06BA3-C550-40A5-B8E3-FEC8E9BF3867
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageCORSRule.md
ms.openlocfilehash: 873cee6ce1f724fb925ae743133ecfb9a1a5210a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447886"
---
# <span data-ttu-id="a8167-101">Remove-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="a8167-101">Remove-AzureStorageCORSRule</span></span>

## <span data-ttu-id="a8167-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a8167-102">SYNOPSIS</span></span>
<span data-ttu-id="a8167-103">移除存儲服務的 CORS。</span><span class="sxs-lookup"><span data-stu-id="a8167-103">Removes CORS for a Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8167-104">句法</span><span class="sxs-lookup"><span data-stu-id="a8167-104">SYNTAX</span></span>

```
Remove-AzureStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="a8167-105">說明</span><span class="sxs-lookup"><span data-stu-id="a8167-105">DESCRIPTION</span></span>
<span data-ttu-id="a8167-106">**AzureStorageCORSRule** Cmdlet 會移除 Azure 儲存空間服務 (CORS) 的跨來源資源分享。</span><span class="sxs-lookup"><span data-stu-id="a8167-106">The **Remove-AzureStorageCORSRule** cmdlet removes Cross-Origin Resource Sharing (CORS) for an Azure Storage service.</span></span>
<span data-ttu-id="a8167-107">這個 Cmdlet 會刪除儲存服務類型中的所有 CORS 規則。</span><span class="sxs-lookup"><span data-stu-id="a8167-107">This cmdlet deletes all CORS rules in a Storage service type.</span></span>
<span data-ttu-id="a8167-108">此 Cmdlet 的儲存服務類型為 Blob、資料表、佇列和檔案。</span><span class="sxs-lookup"><span data-stu-id="a8167-108">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>

## <span data-ttu-id="a8167-109">示例</span><span class="sxs-lookup"><span data-stu-id="a8167-109">EXAMPLES</span></span>

### <span data-ttu-id="a8167-110">範例1：移除 blob 服務的 CORS 規則</span><span class="sxs-lookup"><span data-stu-id="a8167-110">Example 1: Remove CORS rules for the blob service</span></span>
```
PS C:\>Remove-AzureStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="a8167-111">這個命令會移除 [Blob] 服務類型的 CORS 規則。</span><span class="sxs-lookup"><span data-stu-id="a8167-111">This command removes CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="a8167-112">參數</span><span class="sxs-lookup"><span data-stu-id="a8167-112">PARAMETERS</span></span>

### <span data-ttu-id="a8167-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a8167-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a8167-114">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="a8167-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="a8167-115">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="a8167-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="a8167-116">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="a8167-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="a8167-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a8167-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a8167-118">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="a8167-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="a8167-119">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="a8167-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="a8167-120">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="a8167-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="a8167-121">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="a8167-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="a8167-122">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="a8167-122">The default value is 10.</span></span>

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

### <span data-ttu-id="a8167-123">-內容</span><span class="sxs-lookup"><span data-stu-id="a8167-123">-Context</span></span>
<span data-ttu-id="a8167-124">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="a8167-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="a8167-125">若要取得儲存內容，請 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a8167-125">To obtain the storage context, the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a8167-126">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a8167-126">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a8167-127">指定要求中伺服器部分的超時時間長度。</span><span class="sxs-lookup"><span data-stu-id="a8167-127">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="a8167-128">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="a8167-128">-ServiceType</span></span>
<span data-ttu-id="a8167-129">指定此 Cmdlet 移除規則的 Azure 儲存空間服務類型。</span><span class="sxs-lookup"><span data-stu-id="a8167-129">Specifies the Azure Storage service type for which this cmdlet removes rules.</span></span>
<span data-ttu-id="a8167-130">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a8167-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a8167-131">Blob</span><span class="sxs-lookup"><span data-stu-id="a8167-131">Blob</span></span> 
- <span data-ttu-id="a8167-132">張</span><span class="sxs-lookup"><span data-stu-id="a8167-132">Table</span></span> 
- <span data-ttu-id="a8167-133">序列</span><span class="sxs-lookup"><span data-stu-id="a8167-133">Queue</span></span> 
- <span data-ttu-id="a8167-134">檔案</span><span class="sxs-lookup"><span data-stu-id="a8167-134">File</span></span>

```yaml
Type: StorageServiceType
Parameter Sets: (All)
Aliases: 
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8167-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8167-135">CommonParameters</span></span>
<span data-ttu-id="a8167-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a8167-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8167-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a8167-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8167-138">輸入</span><span class="sxs-lookup"><span data-stu-id="a8167-138">INPUTS</span></span>

### <span data-ttu-id="a8167-139">IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="a8167-139">IStorageContext</span></span>

<span data-ttu-id="a8167-140">參數「CoNtext」接受來自管線的 "IStorageCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="a8167-140">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="a8167-141">輸出</span><span class="sxs-lookup"><span data-stu-id="a8167-141">OUTPUTS</span></span>

## <span data-ttu-id="a8167-142">筆記</span><span class="sxs-lookup"><span data-stu-id="a8167-142">NOTES</span></span>

## <span data-ttu-id="a8167-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="a8167-143">RELATED LINKS</span></span>

[<span data-ttu-id="a8167-144">AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="a8167-144">Get-AzureStorageCORSRule</span></span>](./Get-AzureStorageCORSRule.md)

[<span data-ttu-id="a8167-145">Set-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="a8167-145">Set-AzureStorageCORSRule</span></span>](./Set-AzureStorageCORSRule.md)


