---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 26E06BA3-C550-40A5-B8E3-FEC8E9BF3867
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageCORSRule.md
ms.openlocfilehash: aeae25ab3a8ff0b1fa3eb91db90497b44555631f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93966107"
---
# <span data-ttu-id="61ffc-101">Remove-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="61ffc-101">Remove-AzStorageCORSRule</span></span>

## <span data-ttu-id="61ffc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="61ffc-102">SYNOPSIS</span></span>
<span data-ttu-id="61ffc-103">移除存儲服務的 CORS。</span><span class="sxs-lookup"><span data-stu-id="61ffc-103">Removes CORS for a Storage service.</span></span>

## <span data-ttu-id="61ffc-104">句法</span><span class="sxs-lookup"><span data-stu-id="61ffc-104">SYNTAX</span></span>

```
Remove-AzStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="61ffc-105">說明</span><span class="sxs-lookup"><span data-stu-id="61ffc-105">DESCRIPTION</span></span>
<span data-ttu-id="61ffc-106">**AzStorageCORSRule** Cmdlet 會移除 Azure 儲存空間服務 (CORS) 的跨來源資源分享。</span><span class="sxs-lookup"><span data-stu-id="61ffc-106">The **Remove-AzStorageCORSRule** cmdlet removes Cross-Origin Resource Sharing (CORS) for an Azure Storage service.</span></span>
<span data-ttu-id="61ffc-107">這個 Cmdlet 會刪除儲存服務類型中的所有 CORS 規則。</span><span class="sxs-lookup"><span data-stu-id="61ffc-107">This cmdlet deletes all CORS rules in a Storage service type.</span></span>
<span data-ttu-id="61ffc-108">此 Cmdlet 的儲存服務類型為 Blob、資料表、佇列和檔案。</span><span class="sxs-lookup"><span data-stu-id="61ffc-108">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>

## <span data-ttu-id="61ffc-109">示例</span><span class="sxs-lookup"><span data-stu-id="61ffc-109">EXAMPLES</span></span>

### <span data-ttu-id="61ffc-110">範例1：移除 blob 服務的 CORS 規則</span><span class="sxs-lookup"><span data-stu-id="61ffc-110">Example 1: Remove CORS rules for the blob service</span></span>
```
PS C:\>Remove-AzStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="61ffc-111">這個命令會移除 [Blob] 服務類型的 CORS 規則。</span><span class="sxs-lookup"><span data-stu-id="61ffc-111">This command removes CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="61ffc-112">參數</span><span class="sxs-lookup"><span data-stu-id="61ffc-112">PARAMETERS</span></span>

### <span data-ttu-id="61ffc-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="61ffc-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="61ffc-114">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="61ffc-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="61ffc-115">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="61ffc-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="61ffc-116">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="61ffc-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="61ffc-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="61ffc-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="61ffc-118">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="61ffc-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="61ffc-119">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="61ffc-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="61ffc-120">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="61ffc-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="61ffc-121">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="61ffc-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="61ffc-122">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="61ffc-122">The default value is 10.</span></span>

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

### <span data-ttu-id="61ffc-123">-內容</span><span class="sxs-lookup"><span data-stu-id="61ffc-123">-Context</span></span>
<span data-ttu-id="61ffc-124">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="61ffc-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="61ffc-125">若要取得儲存內容，請 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="61ffc-125">To obtain the storage context, the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="61ffc-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61ffc-126">-DefaultProfile</span></span>
<span data-ttu-id="61ffc-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="61ffc-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61ffc-128">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="61ffc-128">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="61ffc-129">指定要求中伺服器部分的超時時間長度。</span><span class="sxs-lookup"><span data-stu-id="61ffc-129">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="61ffc-130">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="61ffc-130">-ServiceType</span></span>
<span data-ttu-id="61ffc-131">指定此 Cmdlet 移除規則的 Azure 儲存空間服務類型。</span><span class="sxs-lookup"><span data-stu-id="61ffc-131">Specifies the Azure Storage service type for which this cmdlet removes rules.</span></span>
<span data-ttu-id="61ffc-132">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="61ffc-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="61ffc-133">Blob</span><span class="sxs-lookup"><span data-stu-id="61ffc-133">Blob</span></span> 
- <span data-ttu-id="61ffc-134">張</span><span class="sxs-lookup"><span data-stu-id="61ffc-134">Table</span></span> 
- <span data-ttu-id="61ffc-135">序列</span><span class="sxs-lookup"><span data-stu-id="61ffc-135">Queue</span></span> 
- <span data-ttu-id="61ffc-136">檔案</span><span class="sxs-lookup"><span data-stu-id="61ffc-136">File</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.StorageServiceType
Parameter Sets: (All)
Aliases:
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61ffc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61ffc-137">CommonParameters</span></span>
<span data-ttu-id="61ffc-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="61ffc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61ffc-139">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="61ffc-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61ffc-140">輸入</span><span class="sxs-lookup"><span data-stu-id="61ffc-140">INPUTS</span></span>

### <span data-ttu-id="61ffc-141">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="61ffc-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="61ffc-142">輸出</span><span class="sxs-lookup"><span data-stu-id="61ffc-142">OUTPUTS</span></span>

### <span data-ttu-id="61ffc-143">System.void</span><span class="sxs-lookup"><span data-stu-id="61ffc-143">System.Void</span></span>

## <span data-ttu-id="61ffc-144">筆記</span><span class="sxs-lookup"><span data-stu-id="61ffc-144">NOTES</span></span>

## <span data-ttu-id="61ffc-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="61ffc-145">RELATED LINKS</span></span>

[<span data-ttu-id="61ffc-146">AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="61ffc-146">Get-AzStorageCORSRule</span></span>](./Get-AzStorageCORSRule.md)

[<span data-ttu-id="61ffc-147">Set-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="61ffc-147">Set-AzStorageCORSRule</span></span>](./Set-AzStorageCORSRule.md)


