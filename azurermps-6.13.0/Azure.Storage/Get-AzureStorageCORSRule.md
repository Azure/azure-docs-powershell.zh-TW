---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 5FA8A3F3-F52C-40BC-94C2-4CDA00C6F32F
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageCORSRule.md
ms.openlocfilehash: 6b5d7fa889810563964aa66a34b567f482781ac6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448516"
---
# <span data-ttu-id="65dde-101">Get-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="65dde-101">Get-AzureStorageCORSRule</span></span>

## <span data-ttu-id="65dde-102">摘要</span><span class="sxs-lookup"><span data-stu-id="65dde-102">SYNOPSIS</span></span>
<span data-ttu-id="65dde-103">取得儲存服務類型的 CORS 規則。</span><span class="sxs-lookup"><span data-stu-id="65dde-103">Gets CORS rules for a Storage service type.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65dde-104">句法</span><span class="sxs-lookup"><span data-stu-id="65dde-104">SYNTAX</span></span>

```
Get-AzureStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="65dde-105">說明</span><span class="sxs-lookup"><span data-stu-id="65dde-105">DESCRIPTION</span></span>
<span data-ttu-id="65dde-106">AzureStorageCORSRule Cmdlet 會針對 Azure 儲存服務類型， **取得** 交叉來源資源分享 (CORS) 規則。</span><span class="sxs-lookup"><span data-stu-id="65dde-106">The **Get-AzureStorageCORSRule** cmdlet gets Cross-Origin Resource Sharing (CORS) rules for an Azure Storage service type.</span></span>

## <span data-ttu-id="65dde-107">示例</span><span class="sxs-lookup"><span data-stu-id="65dde-107">EXAMPLES</span></span>

### <span data-ttu-id="65dde-108">範例1：取得 blob 服務的 CORS 規則</span><span class="sxs-lookup"><span data-stu-id="65dde-108">Example 1: Get CORS rules of blob service</span></span>
```
PS C:\>Get-AzureStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="65dde-109">這個命令會取得 Blob 服務類型的 CORS 規則。</span><span class="sxs-lookup"><span data-stu-id="65dde-109">This command gets the CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="65dde-110">參數</span><span class="sxs-lookup"><span data-stu-id="65dde-110">PARAMETERS</span></span>

### <span data-ttu-id="65dde-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="65dde-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="65dde-112">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="65dde-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="65dde-113">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="65dde-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="65dde-114">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="65dde-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="65dde-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="65dde-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="65dde-116">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="65dde-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="65dde-117">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="65dde-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="65dde-118">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="65dde-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="65dde-119">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="65dde-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="65dde-120">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="65dde-120">The default value is 10.</span></span>

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

### <span data-ttu-id="65dde-121">-內容</span><span class="sxs-lookup"><span data-stu-id="65dde-121">-Context</span></span>
<span data-ttu-id="65dde-122">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="65dde-122">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="65dde-123">若要取得內容，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="65dde-123">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="65dde-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65dde-124">-DefaultProfile</span></span>
<span data-ttu-id="65dde-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="65dde-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65dde-126">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="65dde-126">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="65dde-127">指定要求中伺服器部分的超時時間長度。</span><span class="sxs-lookup"><span data-stu-id="65dde-127">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="65dde-128">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="65dde-128">-ServiceType</span></span>
<span data-ttu-id="65dde-129">指定此 Cmdlet 取得 CORS 規則的 Azure 儲存服務類型。</span><span class="sxs-lookup"><span data-stu-id="65dde-129">Specifies the Azure Storage service type for which this cmdlet gets CORS rules.</span></span>
<span data-ttu-id="65dde-130">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="65dde-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="65dde-131">Blob</span><span class="sxs-lookup"><span data-stu-id="65dde-131">Blob</span></span> 
- <span data-ttu-id="65dde-132">張</span><span class="sxs-lookup"><span data-stu-id="65dde-132">Table</span></span> 
- <span data-ttu-id="65dde-133">序列</span><span class="sxs-lookup"><span data-stu-id="65dde-133">Queue</span></span> 
- <span data-ttu-id="65dde-134">檔案</span><span class="sxs-lookup"><span data-stu-id="65dde-134">File</span></span>

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

### <span data-ttu-id="65dde-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65dde-135">CommonParameters</span></span>
<span data-ttu-id="65dde-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="65dde-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65dde-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="65dde-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65dde-138">輸入</span><span class="sxs-lookup"><span data-stu-id="65dde-138">INPUTS</span></span>

### <span data-ttu-id="65dde-139">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="65dde-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="65dde-140">輸出</span><span class="sxs-lookup"><span data-stu-id="65dde-140">OUTPUTS</span></span>

### <span data-ttu-id="65dde-141">WindowsAzure. ResourceModel.. PSCorsRule</span><span class="sxs-lookup"><span data-stu-id="65dde-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span></span>

## <span data-ttu-id="65dde-142">筆記</span><span class="sxs-lookup"><span data-stu-id="65dde-142">NOTES</span></span>

## <span data-ttu-id="65dde-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="65dde-143">RELATED LINKS</span></span>

[<span data-ttu-id="65dde-144">移除-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="65dde-144">Remove-AzureStorageCORSRule</span></span>](./Remove-AzureStorageCORSRule.md)

[<span data-ttu-id="65dde-145">Set-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="65dde-145">Set-AzureStorageCORSRule</span></span>](./Set-AzureStorageCORSRule.md)


