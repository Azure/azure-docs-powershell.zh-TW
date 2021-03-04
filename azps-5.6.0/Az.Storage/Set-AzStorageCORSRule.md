---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 288B7B56-B934-45AF-BF56-4EB0DD827522
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azstoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageCORSRule.md
ms.openlocfilehash: 6a04b038a452d979394ab57d8f3d905a57428051
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907958"
---
# <span data-ttu-id="a1906-101">Set-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="a1906-101">Set-AzStorageCORSRule</span></span>

## <span data-ttu-id="a1906-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a1906-102">SYNOPSIS</span></span>
<span data-ttu-id="a1906-103">設定儲存服務類型的 CORS 規則。</span><span class="sxs-lookup"><span data-stu-id="a1906-103">Sets the CORS rules for a type of Storage service.</span></span>

## <span data-ttu-id="a1906-104">語法</span><span class="sxs-lookup"><span data-stu-id="a1906-104">SYNTAX</span></span>

```
Set-AzStorageCORSRule [-ServiceType] <StorageServiceType> -CorsRules <PSCorsRule[]> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="a1906-105">描述</span><span class="sxs-lookup"><span data-stu-id="a1906-105">DESCRIPTION</span></span>
<span data-ttu-id="a1906-106">**Set-AzStorageCORSRule** Cmdlet 會針對一種 Azure 儲存服務類型 (CORS) 設定跨來源資源分享規則。</span><span class="sxs-lookup"><span data-stu-id="a1906-106">The **Set-AzStorageCORSRule** cmdlet sets the Cross-Origin Resource Sharing (CORS) rules for a type of Azure Storage service.</span></span>
<span data-ttu-id="a1906-107">此 Cmdlet 的儲存服務類型為 Blob、資料表、佇列和檔案。</span><span class="sxs-lookup"><span data-stu-id="a1906-107">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>
<span data-ttu-id="a1906-108">此 Cmdlet 會覆寫現有的規則。</span><span class="sxs-lookup"><span data-stu-id="a1906-108">This cmdlet overwrites the existing rules.</span></span>
<span data-ttu-id="a1906-109">若要查看目前規則，請使用 Get-AzStorageCORSRule Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a1906-109">To see the current rules, use the Get-AzStorageCORSRule cmdlet.</span></span>

## <span data-ttu-id="a1906-110">例子</span><span class="sxs-lookup"><span data-stu-id="a1906-110">EXAMPLES</span></span>

### <span data-ttu-id="a1906-111">範例 1：將 CORS 規則指派給 Blob 服務</span><span class="sxs-lookup"><span data-stu-id="a1906-111">Example 1: Assign CORS rules to the blob service</span></span>
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

<span data-ttu-id="a1906-112">第一個命令會指派規則陣列給$CorsRules變數。</span><span class="sxs-lookup"><span data-stu-id="a1906-112">The first command assigns an array of rules to the $CorsRules variable.</span></span>
<span data-ttu-id="a1906-113">此命令使用標準會延伸至此程式碼區塊中的多行。</span><span class="sxs-lookup"><span data-stu-id="a1906-113">This command uses standard extends over several lines in this code block.</span></span>
<span data-ttu-id="a1906-114">第二個命令會指派規則$CorsRules Blob 服務類型。</span><span class="sxs-lookup"><span data-stu-id="a1906-114">The second command assigns the rules in $CorsRules to the Blob service type.</span></span>

### <span data-ttu-id="a1906-115">範例 2：變更 Blob 服務 CORS 規則的屬性</span><span class="sxs-lookup"><span data-stu-id="a1906-115">Example 2: Change properties of a CORS rule for blob service</span></span>
```
PS C:\>$CorsRules = Get-AzStorageCORSRule -ServiceType Blob
PS C:\> $CorsRules[0].AllowedHeaders = @("x-ms-blob-content-type", "x-ms-blob-content-disposition")
PS C:\> $CorsRules[0].AllowedMethods = @("Get", "Connect", "Merge")
PS C:\> Set-AzStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

<span data-ttu-id="a1906-116">第一個命令會使用 **Get-AzStorageCORSRule Cmdlet** 取得 Blob 類型的目前 CORS 規則。</span><span class="sxs-lookup"><span data-stu-id="a1906-116">The first command gets the current CORS rules for the Blob type by using the **Get-AzStorageCORSRule** cmdlet.</span></span>
<span data-ttu-id="a1906-117">該命令將規則儲存在陣列$CorsRules中。</span><span class="sxs-lookup"><span data-stu-id="a1906-117">The command stores the rules in the $CorsRules array variable.</span></span>
<span data-ttu-id="a1906-118">第二個和第三個命令會修改 $CorsRules。</span><span class="sxs-lookup"><span data-stu-id="a1906-118">The second and third commands modify the first rule in $CorsRules.</span></span>
<span data-ttu-id="a1906-119">最後一個命令會指派規則$CorsRules Blob 服務類型。</span><span class="sxs-lookup"><span data-stu-id="a1906-119">The final command assigns the rules in $CorsRules to the Blob service type.</span></span>
<span data-ttu-id="a1906-120">修訂的規則會覆寫目前的 CORS 規則。</span><span class="sxs-lookup"><span data-stu-id="a1906-120">The revised rules overwrite the current CORS rules.</span></span>

## <span data-ttu-id="a1906-121">參數</span><span class="sxs-lookup"><span data-stu-id="a1906-121">PARAMETERS</span></span>

### <span data-ttu-id="a1906-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a1906-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a1906-123">指定一個服務要求用戶端的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="a1906-123">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="a1906-124">如果前一個通話在指定的時間間隔內失敗，此 Cmdlet 會重新重試要求。</span><span class="sxs-lookup"><span data-stu-id="a1906-124">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="a1906-125">如果此 Cmdlet 在間隔經過之前未收到成功回應，此 Cmdlet 會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="a1906-125">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="a1906-126">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a1906-126">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a1906-127">指定同時進行的最大網路通話數。</span><span class="sxs-lookup"><span data-stu-id="a1906-127">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="a1906-128">您可以使用此參數來限制並行，以節流本地 CPU 和頻寬使用量，方法為指定並行網路通話的數量上限。</span><span class="sxs-lookup"><span data-stu-id="a1906-128">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="a1906-129">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="a1906-129">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="a1906-130">此參數有助於減少低頻寬環境的網路連接問題，例如每秒 100 KB。</span><span class="sxs-lookup"><span data-stu-id="a1906-130">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="a1906-131">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="a1906-131">The default value is 10.</span></span>

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

### <span data-ttu-id="a1906-132">-內容</span><span class="sxs-lookup"><span data-stu-id="a1906-132">-Context</span></span>
<span data-ttu-id="a1906-133">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="a1906-133">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="a1906-134">若要取得內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a1906-134">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a1906-135">-CorsRules</span><span class="sxs-lookup"><span data-stu-id="a1906-135">-CorsRules</span></span>
<span data-ttu-id="a1906-136">指定 CORS 規則的陣列。</span><span class="sxs-lookup"><span data-stu-id="a1906-136">Specifies an array of CORS rules.</span></span>
<span data-ttu-id="a1906-137">您可以使用 Cmdlet 來Get-AzStorageCORSRule規則。</span><span class="sxs-lookup"><span data-stu-id="a1906-137">You can retrieve the existing rules using the Get-AzStorageCORSRule cmdlet.</span></span>

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

### <span data-ttu-id="a1906-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1906-138">-DefaultProfile</span></span>
<span data-ttu-id="a1906-139">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a1906-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1906-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a1906-140">-PassThru</span></span>
<span data-ttu-id="a1906-141">表示此 Cmdlet 會返回反映作業成功的布林值。</span><span class="sxs-lookup"><span data-stu-id="a1906-141">Indicates that this cmdlet returns a Boolean that reflects the success of the operation.</span></span>
<span data-ttu-id="a1906-142">根據預設，此 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="a1906-142">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="a1906-143">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a1906-143">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a1906-144">指定要求的伺服器部分之時間長度。</span><span class="sxs-lookup"><span data-stu-id="a1906-144">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="a1906-145">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="a1906-145">-ServiceType</span></span>
<span data-ttu-id="a1906-146">指定此 Cmdlet 指派規則的 Azure 儲存體服務類型。</span><span class="sxs-lookup"><span data-stu-id="a1906-146">Specifies the Azure Storage service type for which this cmdlet assigns rules.</span></span>
<span data-ttu-id="a1906-147">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a1906-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a1906-148">Blob</span><span class="sxs-lookup"><span data-stu-id="a1906-148">Blob</span></span> 
- <span data-ttu-id="a1906-149">表</span><span class="sxs-lookup"><span data-stu-id="a1906-149">Table</span></span> 
- <span data-ttu-id="a1906-150">佇列</span><span class="sxs-lookup"><span data-stu-id="a1906-150">Queue</span></span> 
- <span data-ttu-id="a1906-151">檔</span><span class="sxs-lookup"><span data-stu-id="a1906-151">File</span></span>

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

### <span data-ttu-id="a1906-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1906-152">CommonParameters</span></span>
<span data-ttu-id="a1906-153">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a1906-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1906-154">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a1906-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1906-155">輸入</span><span class="sxs-lookup"><span data-stu-id="a1906-155">INPUTS</span></span>

### <span data-ttu-id="a1906-156">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="a1906-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a1906-157">輸出</span><span class="sxs-lookup"><span data-stu-id="a1906-157">OUTPUTS</span></span>

### <span data-ttu-id="a1906-158">Microsoft.WindowsAzure.Commands.storage.Model.ResourceModel.PSCorsRule</span><span class="sxs-lookup"><span data-stu-id="a1906-158">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span></span>

## <span data-ttu-id="a1906-159">筆記</span><span class="sxs-lookup"><span data-stu-id="a1906-159">NOTES</span></span>

## <span data-ttu-id="a1906-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="a1906-160">RELATED LINKS</span></span>

[<span data-ttu-id="a1906-161">Get-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="a1906-161">Get-AzStorageCORSRule</span></span>](./Get-AzStorageCORSRule.md)

[<span data-ttu-id="a1906-162">New-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="a1906-162">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="a1906-163">Remove-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="a1906-163">Remove-AzStorageCORSRule</span></span>](./Remove-AzStorageCORSRule.md)


