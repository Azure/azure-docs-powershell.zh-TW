---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 288B7B56-B934-45AF-BF56-4EB0DD827522
online version: ''
schema: 2.0.0
ms.openlocfilehash: 635b8e1524f6123aa6ddde4ed7a64768d6c3d791
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443556"
---
# <span data-ttu-id="cf11e-101">Set-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="cf11e-101">Set-AzureStorageCORSRule</span></span>

## <span data-ttu-id="cf11e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cf11e-102">SYNOPSIS</span></span>
<span data-ttu-id="cf11e-103">為一種類型的儲存服務設定 CORS 規則。</span><span class="sxs-lookup"><span data-stu-id="cf11e-103">Sets the CORS rules for a type of Storage service.</span></span>

## <span data-ttu-id="cf11e-104">句法</span><span class="sxs-lookup"><span data-stu-id="cf11e-104">SYNTAX</span></span>

```
Set-AzureStorageCORSRule [-ServiceType] <StorageServiceType> -CorsRules <PSCorsRule[]> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="cf11e-105">說明</span><span class="sxs-lookup"><span data-stu-id="cf11e-105">DESCRIPTION</span></span>
<span data-ttu-id="cf11e-106">**AzureStorageCORSRule** Cmdlet 會針對 Azure 儲存空間服務的類型，設定跨來源資源分享 (CORS) 規則。</span><span class="sxs-lookup"><span data-stu-id="cf11e-106">The **Set-AzureStorageCORSRule** cmdlet sets the Cross-Origin Resource Sharing (CORS) rules for a type of Azure Storage service.</span></span>
<span data-ttu-id="cf11e-107">此 Cmdlet 的儲存服務類型為 Blob、資料表、佇列和檔案。</span><span class="sxs-lookup"><span data-stu-id="cf11e-107">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>
<span data-ttu-id="cf11e-108">這個 Cmdlet 會覆寫現有的規則。</span><span class="sxs-lookup"><span data-stu-id="cf11e-108">This cmdlet overwrites the existing rules.</span></span>
<span data-ttu-id="cf11e-109">若要查看目前的規則，請使用 Get-AzureStorageCORSRule Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cf11e-109">To see the current rules, use the Get-AzureStorageCORSRule cmdlet.</span></span>

## <span data-ttu-id="cf11e-110">示例</span><span class="sxs-lookup"><span data-stu-id="cf11e-110">EXAMPLES</span></span>

### <span data-ttu-id="cf11e-111">範例1：將 CORS 規則指派給 blob 服務</span><span class="sxs-lookup"><span data-stu-id="cf11e-111">Example 1: Assign CORS rules to the blob service</span></span>
```
PS C:\>$CorsRules = (@{
    AllowedHeaders=@("x-ms-blob-content-type","x-ms-blob-content-disposition");
    AllowedOrigins=@("*");
    MaxAgeInSeconds=30;
    AllowedMethods=@("Get","Connect")},
    @{
    AllowedOrigins=@("http://www.fabrikam.com","http://www.contoso.com"); 
    ExposedHeaders=@("x-ms-meta-data*","x-ms-meta-customheader"); 
    AllowedHeaders=@("x-ms-meta-target*","x-ms-meta-customheader");
    MaxAgeInSeconds=30;
    AllowedMethods=@("Put")})
PS C:\> Set-AzureStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

<span data-ttu-id="cf11e-112">第一個命令會將一組規則指派給 $CorsRules 變數。</span><span class="sxs-lookup"><span data-stu-id="cf11e-112">The first command assigns an array of rules to the $CorsRules variable.</span></span>
<span data-ttu-id="cf11e-113">這個命令使用標準延伸到此程式碼塊中的數個行。</span><span class="sxs-lookup"><span data-stu-id="cf11e-113">This command uses standard extends over several lines in this code block.</span></span>

<span data-ttu-id="cf11e-114">第二個命令會將 $CorsRules 中的規則指派給 Blob 服務類型。</span><span class="sxs-lookup"><span data-stu-id="cf11e-114">The second command assigns the rules in $CorsRules to the Blob service type.</span></span>

### <span data-ttu-id="cf11e-115">範例2：變更 blob 服務的 CORS 規則屬性</span><span class="sxs-lookup"><span data-stu-id="cf11e-115">Example 2: Change properties of a CORS rule for blob service</span></span>
```
PS C:\>$CorsRules = Get-AzureStorageCORSRule -ServiceType Blob
PS C:\> $CorsRules[0].AllowedHeaders = @("x-ms-blob-content-type", "x-ms-blob-content-disposition")
PS C:\> $CorsRules[0].AllowedMethods = @("Get", "Connect", "Merge")
PS C:\> Set-AzureStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

<span data-ttu-id="cf11e-116">第一個命令會使用 **AzureStorageCORSRule** Cmdlet 取得 Blob 類型的目前 CORS 規則。</span><span class="sxs-lookup"><span data-stu-id="cf11e-116">The first command gets the current CORS rules for the Blob type by using the **Get-AzureStorageCORSRule** cmdlet.</span></span>
<span data-ttu-id="cf11e-117">該命令會將規則儲存在 $CorsRules 陣列變數中。</span><span class="sxs-lookup"><span data-stu-id="cf11e-117">The command stores the rules in the $CorsRules array variable.</span></span>

<span data-ttu-id="cf11e-118">第二個和第三個命令會修改 $CorsRules 中的第一個規則。</span><span class="sxs-lookup"><span data-stu-id="cf11e-118">The second and third commands modify the first rule in $CorsRules.</span></span>

<span data-ttu-id="cf11e-119">Final 命令會將 $CorsRules 中的規則指派給 Blob 服務類型。</span><span class="sxs-lookup"><span data-stu-id="cf11e-119">The final command assigns the rules in $CorsRules to the Blob service type.</span></span>
<span data-ttu-id="cf11e-120">修改後的規則會覆寫目前的 CORS 規則。</span><span class="sxs-lookup"><span data-stu-id="cf11e-120">The revised rules overwrite the current CORS rules.</span></span>

## <span data-ttu-id="cf11e-121">參數</span><span class="sxs-lookup"><span data-stu-id="cf11e-121">PARAMETERS</span></span>

### <span data-ttu-id="cf11e-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cf11e-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="cf11e-123">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="cf11e-123">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="cf11e-124">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="cf11e-124">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="cf11e-125">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="cf11e-125">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="cf11e-126">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="cf11e-126">-ConcurrentTaskCount</span></span>
<span data-ttu-id="cf11e-127">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="cf11e-127">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="cf11e-128">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="cf11e-128">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="cf11e-129">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="cf11e-129">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="cf11e-130">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="cf11e-130">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="cf11e-131">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="cf11e-131">The default value is 10.</span></span>

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

### <span data-ttu-id="cf11e-132">-內容</span><span class="sxs-lookup"><span data-stu-id="cf11e-132">-Context</span></span>
<span data-ttu-id="cf11e-133">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="cf11e-133">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="cf11e-134">若要取得內容，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cf11e-134">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="cf11e-135">-CorsRules</span><span class="sxs-lookup"><span data-stu-id="cf11e-135">-CorsRules</span></span>
<span data-ttu-id="cf11e-136">指定 CORS 規則的陣列。</span><span class="sxs-lookup"><span data-stu-id="cf11e-136">Specifies an array of CORS rules.</span></span>
<span data-ttu-id="cf11e-137">您可以使用 Get-AzureStorageCORSRule Cmdlet 來檢索現有規則。</span><span class="sxs-lookup"><span data-stu-id="cf11e-137">You can retrieve the existing rules using the Get-AzureStorageCORSRule cmdlet.</span></span>

```yaml
Type: PSCorsRule[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf11e-138">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cf11e-138">-PassThru</span></span>
<span data-ttu-id="cf11e-139">表示此 Cmdlet 會傳回反映操作成功的布林值。</span><span class="sxs-lookup"><span data-stu-id="cf11e-139">Indicates that this cmdlet returns a Boolean that reflects the success of the operation.</span></span>
<span data-ttu-id="cf11e-140">根據預設，這個 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="cf11e-140">By default, this cmdlet does not return a value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf11e-141">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cf11e-141">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="cf11e-142">指定要求中伺服器部分的超時時間長度。</span><span class="sxs-lookup"><span data-stu-id="cf11e-142">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="cf11e-143">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="cf11e-143">-ServiceType</span></span>
<span data-ttu-id="cf11e-144">指定此 Cmdlet 指派規則的 Azure 儲存空間服務類型。</span><span class="sxs-lookup"><span data-stu-id="cf11e-144">Specifies the Azure Storage service type for which this cmdlet assigns rules.</span></span>
<span data-ttu-id="cf11e-145">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="cf11e-145">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cf11e-146">Blob</span><span class="sxs-lookup"><span data-stu-id="cf11e-146">Blob</span></span> 
- <span data-ttu-id="cf11e-147">張</span><span class="sxs-lookup"><span data-stu-id="cf11e-147">Table</span></span> 
- <span data-ttu-id="cf11e-148">序列</span><span class="sxs-lookup"><span data-stu-id="cf11e-148">Queue</span></span> 
- <span data-ttu-id="cf11e-149">檔案</span><span class="sxs-lookup"><span data-stu-id="cf11e-149">File</span></span>

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

### <span data-ttu-id="cf11e-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf11e-150">CommonParameters</span></span>
<span data-ttu-id="cf11e-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cf11e-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf11e-152">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cf11e-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf11e-153">輸入</span><span class="sxs-lookup"><span data-stu-id="cf11e-153">INPUTS</span></span>

## <span data-ttu-id="cf11e-154">輸出</span><span class="sxs-lookup"><span data-stu-id="cf11e-154">OUTPUTS</span></span>

## <span data-ttu-id="cf11e-155">筆記</span><span class="sxs-lookup"><span data-stu-id="cf11e-155">NOTES</span></span>

## <span data-ttu-id="cf11e-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="cf11e-156">RELATED LINKS</span></span>

[<span data-ttu-id="cf11e-157">AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="cf11e-157">Get-AzureStorageCORSRule</span></span>](./Get-AzureStorageCORSRule.md)

[<span data-ttu-id="cf11e-158">新-AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="cf11e-158">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="cf11e-159">移除-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="cf11e-159">Remove-AzureStorageCORSRule</span></span>](./Remove-AzureStorageCORSRule.md)


