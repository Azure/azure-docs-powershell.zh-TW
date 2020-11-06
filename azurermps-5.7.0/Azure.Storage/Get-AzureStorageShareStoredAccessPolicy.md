---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 73BB521B-20F2-4F2B-AA88-2B128F36A9EF
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageShareStoredAccessPolicy.md
ms.openlocfilehash: e7ed025b7eec83145c4abe581974f21d7ed335fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449453"
---
# <span data-ttu-id="30992-101">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="30992-101">Get-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="30992-102">摘要</span><span class="sxs-lookup"><span data-stu-id="30992-102">SYNOPSIS</span></span>
<span data-ttu-id="30992-103">取得儲存空間共用的存取原則。</span><span class="sxs-lookup"><span data-stu-id="30992-103">Gets stored access policies for a Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30992-104">句法</span><span class="sxs-lookup"><span data-stu-id="30992-104">SYNTAX</span></span>

```
Get-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="30992-105">說明</span><span class="sxs-lookup"><span data-stu-id="30992-105">DESCRIPTION</span></span>
<span data-ttu-id="30992-106">**AzureStorageShareStoredAccessPolicy** Cmdlet 會針對 Azure 儲存空間共用取得儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="30992-106">The **Get-AzureStorageShareStoredAccessPolicy** cmdlet gets stored access policies for an Azure Storage share.</span></span>
<span data-ttu-id="30992-107">若要取得特定原則，請依名稱指定。</span><span class="sxs-lookup"><span data-stu-id="30992-107">To get a particular policy, specify it by name.</span></span>

## <span data-ttu-id="30992-108">示例</span><span class="sxs-lookup"><span data-stu-id="30992-108">EXAMPLES</span></span>

### <span data-ttu-id="30992-109">範例1：在共用中取得儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="30992-109">Example 1: Get a stored access policy in a share</span></span>
```
PS C:\>Get-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="30992-110">這個命令會在 ContosoShare 中取得名為 GeneralPolicy 的儲存訪問原則。</span><span class="sxs-lookup"><span data-stu-id="30992-110">This command gets a stored access policy named GeneralPolicy in ContosoShare.</span></span>

### <span data-ttu-id="30992-111">範例2：取得共用中所有已儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="30992-111">Example 2: Get all the stored access policies in share</span></span>
```
PS C:\>Get-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare"
```

<span data-ttu-id="30992-112">這個命令會取得 ContosoShare 中所有已儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="30992-112">This command gets all stored access policies in ContosoShare.</span></span>

## <span data-ttu-id="30992-113">參數</span><span class="sxs-lookup"><span data-stu-id="30992-113">PARAMETERS</span></span>

### <span data-ttu-id="30992-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="30992-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="30992-115">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="30992-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="30992-116">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="30992-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="30992-117">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="30992-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="30992-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="30992-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="30992-119">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="30992-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="30992-120">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="30992-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="30992-121">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="30992-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="30992-122">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="30992-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="30992-123">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="30992-123">The default value is 10.</span></span>

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

### <span data-ttu-id="30992-124">-內容</span><span class="sxs-lookup"><span data-stu-id="30992-124">-Context</span></span>
<span data-ttu-id="30992-125">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="30992-125">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="30992-126">若要取得內容，請使用 [AzureStorageCoNtext](./New-AzureStorageContext.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="30992-126">To obtain a context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="30992-127">-原則</span><span class="sxs-lookup"><span data-stu-id="30992-127">-Policy</span></span>
<span data-ttu-id="30992-128">指定此 Cmdlet 取得的儲存訪問原則名稱。</span><span class="sxs-lookup"><span data-stu-id="30992-128">Specifies the name of the stored access policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="30992-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="30992-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="30992-130">指定要求中伺服器部分的超時時間長度。</span><span class="sxs-lookup"><span data-stu-id="30992-130">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="30992-131">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="30992-131">-ShareName</span></span>
<span data-ttu-id="30992-132">指定此 Cmdlet 取得其原則的儲存空間份額名稱。</span><span class="sxs-lookup"><span data-stu-id="30992-132">Specifies the Storage share name for which this cmdlet gets policies.</span></span>

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

### <span data-ttu-id="30992-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30992-133">CommonParameters</span></span>
<span data-ttu-id="30992-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="30992-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30992-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="30992-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30992-136">輸入</span><span class="sxs-lookup"><span data-stu-id="30992-136">INPUTS</span></span>

### <span data-ttu-id="30992-137">IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="30992-137">IStorageContext</span></span>

<span data-ttu-id="30992-138">參數「CoNtext」接受來自管線的 "IStorageCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="30992-138">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="30992-139">字串</span><span class="sxs-lookup"><span data-stu-id="30992-139">String</span></span>

<span data-ttu-id="30992-140">參數「共用名稱」接受來自管線的 "String" 類型的值</span><span class="sxs-lookup"><span data-stu-id="30992-140">Parameter 'ShareName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="30992-141">輸出</span><span class="sxs-lookup"><span data-stu-id="30992-141">OUTPUTS</span></span>

### <span data-ttu-id="30992-142">[WindowsAzure] SharedAccessFilePolicy</span><span class="sxs-lookup"><span data-stu-id="30992-142">Microsoft.WindowsAzure.Storage.File.SharedAccessFilePolicy</span></span>

## <span data-ttu-id="30992-143">筆記</span><span class="sxs-lookup"><span data-stu-id="30992-143">NOTES</span></span>

## <span data-ttu-id="30992-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="30992-144">RELATED LINKS</span></span>

[<span data-ttu-id="30992-145">新-AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="30992-145">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="30992-146">新-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="30992-146">New-AzureStorageShareStoredAccessPolicy</span></span>](./New-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="30992-147">移除-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="30992-147">Remove-AzureStorageShareStoredAccessPolicy</span></span>](./Remove-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="30992-148">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="30992-148">Set-AzureStorageShareStoredAccessPolicy</span></span>](./Set-AzureStorageShareStoredAccessPolicy.md)
