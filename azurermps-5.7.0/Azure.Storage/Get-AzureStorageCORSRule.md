---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5FA8A3F3-F52C-40BC-94C2-4CDA00C6F32F
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageCORSRule.md
ms.openlocfilehash: 38ad6f5631f816070e9d59ba7b78c2a39cff2b2c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624118"
---
# <span data-ttu-id="527fa-101">Get-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="527fa-101">Get-AzureStorageCORSRule</span></span>

## <span data-ttu-id="527fa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="527fa-102">SYNOPSIS</span></span>
<span data-ttu-id="527fa-103">取得儲存服務類型的 CORS 規則。</span><span class="sxs-lookup"><span data-stu-id="527fa-103">Gets CORS rules for a Storage service type.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="527fa-104">句法</span><span class="sxs-lookup"><span data-stu-id="527fa-104">SYNTAX</span></span>

```
Get-AzureStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="527fa-105">說明</span><span class="sxs-lookup"><span data-stu-id="527fa-105">DESCRIPTION</span></span>
<span data-ttu-id="527fa-106">AzureStorageCORSRule Cmdlet 會針對 Azure 儲存服務類型， **取得** 交叉來源資源分享 (CORS) 規則。</span><span class="sxs-lookup"><span data-stu-id="527fa-106">The **Get-AzureStorageCORSRule** cmdlet gets Cross-Origin Resource Sharing (CORS) rules for an Azure Storage service type.</span></span>

## <span data-ttu-id="527fa-107">示例</span><span class="sxs-lookup"><span data-stu-id="527fa-107">EXAMPLES</span></span>

### <span data-ttu-id="527fa-108">範例1：取得 blob 服務的 CORS 規則</span><span class="sxs-lookup"><span data-stu-id="527fa-108">Example 1: Get CORS rules of blob service</span></span>
```
PS C:\>Get-AzureStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="527fa-109">這個命令會取得 Blob 服務類型的 CORS 規則。</span><span class="sxs-lookup"><span data-stu-id="527fa-109">This command gets the CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="527fa-110">參數</span><span class="sxs-lookup"><span data-stu-id="527fa-110">PARAMETERS</span></span>

### <span data-ttu-id="527fa-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="527fa-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="527fa-112">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="527fa-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="527fa-113">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="527fa-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="527fa-114">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="527fa-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="527fa-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="527fa-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="527fa-116">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="527fa-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="527fa-117">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="527fa-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="527fa-118">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="527fa-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="527fa-119">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="527fa-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="527fa-120">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="527fa-120">The default value is 10.</span></span>

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

### <span data-ttu-id="527fa-121">-內容</span><span class="sxs-lookup"><span data-stu-id="527fa-121">-Context</span></span>
<span data-ttu-id="527fa-122">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="527fa-122">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="527fa-123">若要取得內容，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="527fa-123">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="527fa-124">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="527fa-124">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="527fa-125">指定要求中伺服器部分的超時時間長度。</span><span class="sxs-lookup"><span data-stu-id="527fa-125">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="527fa-126">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="527fa-126">-ServiceType</span></span>
<span data-ttu-id="527fa-127">指定此 Cmdlet 取得 CORS 規則的 Azure 儲存服務類型。</span><span class="sxs-lookup"><span data-stu-id="527fa-127">Specifies the Azure Storage service type for which this cmdlet gets CORS rules.</span></span>
<span data-ttu-id="527fa-128">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="527fa-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="527fa-129">Blob</span><span class="sxs-lookup"><span data-stu-id="527fa-129">Blob</span></span> 
- <span data-ttu-id="527fa-130">張</span><span class="sxs-lookup"><span data-stu-id="527fa-130">Table</span></span> 
- <span data-ttu-id="527fa-131">序列</span><span class="sxs-lookup"><span data-stu-id="527fa-131">Queue</span></span> 
- <span data-ttu-id="527fa-132">檔案</span><span class="sxs-lookup"><span data-stu-id="527fa-132">File</span></span>

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

### <span data-ttu-id="527fa-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="527fa-133">CommonParameters</span></span>
<span data-ttu-id="527fa-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="527fa-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="527fa-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="527fa-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="527fa-136">輸入</span><span class="sxs-lookup"><span data-stu-id="527fa-136">INPUTS</span></span>

### <span data-ttu-id="527fa-137">IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="527fa-137">IStorageContext</span></span>

<span data-ttu-id="527fa-138">參數「CoNtext」接受來自管線的 "IStorageCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="527fa-138">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="527fa-139">輸出</span><span class="sxs-lookup"><span data-stu-id="527fa-139">OUTPUTS</span></span>

###  
<span data-ttu-id="527fa-140">這個 Cmdlet 會傳回 **PSCORSRule** 物件的陣列，這些物件代表目前在服務上的 CORS 規則。</span><span class="sxs-lookup"><span data-stu-id="527fa-140">This cmdlet returns an array of **PSCORSRule** objects which represent the CORS rules currently on a service.</span></span>

## <span data-ttu-id="527fa-141">筆記</span><span class="sxs-lookup"><span data-stu-id="527fa-141">NOTES</span></span>

## <span data-ttu-id="527fa-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="527fa-142">RELATED LINKS</span></span>

[<span data-ttu-id="527fa-143">移除-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="527fa-143">Remove-AzureStorageCORSRule</span></span>](./Remove-AzureStorageCORSRule.md)

[<span data-ttu-id="527fa-144">Set-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="527fa-144">Set-AzureStorageCORSRule</span></span>](./Set-AzureStorageCORSRule.md)


