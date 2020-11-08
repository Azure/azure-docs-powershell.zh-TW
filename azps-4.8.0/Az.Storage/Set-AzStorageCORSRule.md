---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 288B7B56-B934-45AF-BF56-4EB0DD827522
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageCORSRule.md
ms.openlocfilehash: d7951e53c7cbd8c799c7158bb3cc5c3fabb5b039
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127998"
---
# <span data-ttu-id="38a03-101">Set-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="38a03-101">Set-AzStorageCORSRule</span></span>

## <span data-ttu-id="38a03-102">摘要</span><span class="sxs-lookup"><span data-stu-id="38a03-102">SYNOPSIS</span></span>
<span data-ttu-id="38a03-103">為一種類型的儲存服務設定 CORS 規則。</span><span class="sxs-lookup"><span data-stu-id="38a03-103">Sets the CORS rules for a type of Storage service.</span></span>

## <span data-ttu-id="38a03-104">句法</span><span class="sxs-lookup"><span data-stu-id="38a03-104">SYNTAX</span></span>

```
Set-AzStorageCORSRule [-ServiceType] <StorageServiceType> -CorsRules <PSCorsRule[]> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="38a03-105">說明</span><span class="sxs-lookup"><span data-stu-id="38a03-105">DESCRIPTION</span></span>
<span data-ttu-id="38a03-106">**AzStorageCORSRule** Cmdlet 會針對 Azure 儲存空間服務的類型，設定跨來源資源分享 (CORS) 規則。</span><span class="sxs-lookup"><span data-stu-id="38a03-106">The **Set-AzStorageCORSRule** cmdlet sets the Cross-Origin Resource Sharing (CORS) rules for a type of Azure Storage service.</span></span>
<span data-ttu-id="38a03-107">此 Cmdlet 的儲存服務類型為 Blob、資料表、佇列和檔案。</span><span class="sxs-lookup"><span data-stu-id="38a03-107">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>
<span data-ttu-id="38a03-108">這個 Cmdlet 會覆寫現有的規則。</span><span class="sxs-lookup"><span data-stu-id="38a03-108">This cmdlet overwrites the existing rules.</span></span>
<span data-ttu-id="38a03-109">若要查看目前的規則，請使用 Get-AzStorageCORSRule Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="38a03-109">To see the current rules, use the Get-AzStorageCORSRule cmdlet.</span></span>

## <span data-ttu-id="38a03-110">示例</span><span class="sxs-lookup"><span data-stu-id="38a03-110">EXAMPLES</span></span>

### <span data-ttu-id="38a03-111">範例1：將 CORS 規則指派給 blob 服務</span><span class="sxs-lookup"><span data-stu-id="38a03-111">Example 1: Assign CORS rules to the blob service</span></span>
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
PS C:\> Set-AzStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

<span data-ttu-id="38a03-112">第一個命令會將一組規則指派給 $CorsRules 變數。</span><span class="sxs-lookup"><span data-stu-id="38a03-112">The first command assigns an array of rules to the $CorsRules variable.</span></span>
<span data-ttu-id="38a03-113">這個命令使用標準延伸到此程式碼塊中的數個行。</span><span class="sxs-lookup"><span data-stu-id="38a03-113">This command uses standard extends over several lines in this code block.</span></span>
<span data-ttu-id="38a03-114">第二個命令會將 $CorsRules 中的規則指派給 Blob 服務類型。</span><span class="sxs-lookup"><span data-stu-id="38a03-114">The second command assigns the rules in $CorsRules to the Blob service type.</span></span>

### <span data-ttu-id="38a03-115">範例2：變更 blob 服務的 CORS 規則屬性</span><span class="sxs-lookup"><span data-stu-id="38a03-115">Example 2: Change properties of a CORS rule for blob service</span></span>
```
PS C:\>$CorsRules = Get-AzStorageCORSRule -ServiceType Blob
PS C:\> $CorsRules[0].AllowedHeaders = @("x-ms-blob-content-type", "x-ms-blob-content-disposition")
PS C:\> $CorsRules[0].AllowedMethods = @("Get", "Connect", "Merge")
PS C:\> Set-AzStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

<span data-ttu-id="38a03-116">第一個命令會使用 **AzStorageCORSRule** Cmdlet 取得 Blob 類型的目前 CORS 規則。</span><span class="sxs-lookup"><span data-stu-id="38a03-116">The first command gets the current CORS rules for the Blob type by using the **Get-AzStorageCORSRule** cmdlet.</span></span>
<span data-ttu-id="38a03-117">該命令會將規則儲存在 $CorsRules 陣列變數中。</span><span class="sxs-lookup"><span data-stu-id="38a03-117">The command stores the rules in the $CorsRules array variable.</span></span>
<span data-ttu-id="38a03-118">第二個和第三個命令會修改 $CorsRules 中的第一個規則。</span><span class="sxs-lookup"><span data-stu-id="38a03-118">The second and third commands modify the first rule in $CorsRules.</span></span>
<span data-ttu-id="38a03-119">Final 命令會將 $CorsRules 中的規則指派給 Blob 服務類型。</span><span class="sxs-lookup"><span data-stu-id="38a03-119">The final command assigns the rules in $CorsRules to the Blob service type.</span></span>
<span data-ttu-id="38a03-120">修改後的規則會覆寫目前的 CORS 規則。</span><span class="sxs-lookup"><span data-stu-id="38a03-120">The revised rules overwrite the current CORS rules.</span></span>

## <span data-ttu-id="38a03-121">參數</span><span class="sxs-lookup"><span data-stu-id="38a03-121">PARAMETERS</span></span>

### <span data-ttu-id="38a03-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="38a03-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="38a03-123">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="38a03-123">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="38a03-124">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="38a03-124">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="38a03-125">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="38a03-125">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="38a03-126">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="38a03-126">-ConcurrentTaskCount</span></span>
<span data-ttu-id="38a03-127">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="38a03-127">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="38a03-128">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="38a03-128">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="38a03-129">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="38a03-129">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="38a03-130">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="38a03-130">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="38a03-131">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="38a03-131">The default value is 10.</span></span>

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

### <span data-ttu-id="38a03-132">-內容</span><span class="sxs-lookup"><span data-stu-id="38a03-132">-Context</span></span>
<span data-ttu-id="38a03-133">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="38a03-133">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="38a03-134">若要取得內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="38a03-134">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="38a03-135">-CorsRules</span><span class="sxs-lookup"><span data-stu-id="38a03-135">-CorsRules</span></span>
<span data-ttu-id="38a03-136">指定 CORS 規則的陣列。</span><span class="sxs-lookup"><span data-stu-id="38a03-136">Specifies an array of CORS rules.</span></span>
<span data-ttu-id="38a03-137">您可以使用 Get-AzStorageCORSRule Cmdlet 來檢索現有規則。</span><span class="sxs-lookup"><span data-stu-id="38a03-137">You can retrieve the existing rules using the Get-AzStorageCORSRule cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38a03-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38a03-138">-DefaultProfile</span></span>
<span data-ttu-id="38a03-139">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="38a03-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38a03-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="38a03-140">-PassThru</span></span>
<span data-ttu-id="38a03-141">表示此 Cmdlet 會傳回反映操作成功的布林值。</span><span class="sxs-lookup"><span data-stu-id="38a03-141">Indicates that this cmdlet returns a Boolean that reflects the success of the operation.</span></span>
<span data-ttu-id="38a03-142">根據預設，這個 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="38a03-142">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="38a03-143">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="38a03-143">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="38a03-144">指定要求中伺服器部分的超時時間長度。</span><span class="sxs-lookup"><span data-stu-id="38a03-144">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="38a03-145">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="38a03-145">-ServiceType</span></span>
<span data-ttu-id="38a03-146">指定此 Cmdlet 指派規則的 Azure 儲存空間服務類型。</span><span class="sxs-lookup"><span data-stu-id="38a03-146">Specifies the Azure Storage service type for which this cmdlet assigns rules.</span></span>
<span data-ttu-id="38a03-147">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="38a03-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="38a03-148">Blob</span><span class="sxs-lookup"><span data-stu-id="38a03-148">Blob</span></span> 
- <span data-ttu-id="38a03-149">張</span><span class="sxs-lookup"><span data-stu-id="38a03-149">Table</span></span> 
- <span data-ttu-id="38a03-150">序列</span><span class="sxs-lookup"><span data-stu-id="38a03-150">Queue</span></span> 
- <span data-ttu-id="38a03-151">檔案</span><span class="sxs-lookup"><span data-stu-id="38a03-151">File</span></span>

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

### <span data-ttu-id="38a03-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38a03-152">CommonParameters</span></span>
<span data-ttu-id="38a03-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="38a03-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38a03-154">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="38a03-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38a03-155">輸入</span><span class="sxs-lookup"><span data-stu-id="38a03-155">INPUTS</span></span>

### <span data-ttu-id="38a03-156">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="38a03-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="38a03-157">輸出</span><span class="sxs-lookup"><span data-stu-id="38a03-157">OUTPUTS</span></span>

### <span data-ttu-id="38a03-158">WindowsAzure. ResourceModel.. PSCorsRule</span><span class="sxs-lookup"><span data-stu-id="38a03-158">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span></span>

## <span data-ttu-id="38a03-159">筆記</span><span class="sxs-lookup"><span data-stu-id="38a03-159">NOTES</span></span>

## <span data-ttu-id="38a03-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="38a03-160">RELATED LINKS</span></span>

[<span data-ttu-id="38a03-161">AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="38a03-161">Get-AzStorageCORSRule</span></span>](./Get-AzStorageCORSRule.md)

[<span data-ttu-id="38a03-162">新-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="38a03-162">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="38a03-163">移除-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="38a03-163">Remove-AzStorageCORSRule</span></span>](./Remove-AzStorageCORSRule.md)

