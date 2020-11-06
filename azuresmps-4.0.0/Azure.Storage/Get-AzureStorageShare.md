---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FD3A0013-4365-4E65-891C-5C50A9D5658C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7e816d29784ea8b2e69ba4b36162938f7a82007d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443420"
---
# <span data-ttu-id="6c880-101">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="6c880-101">Get-AzureStorageShare</span></span>

## <span data-ttu-id="6c880-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6c880-102">SYNOPSIS</span></span>
<span data-ttu-id="6c880-103">取得檔案共用的清單。</span><span class="sxs-lookup"><span data-stu-id="6c880-103">Gets a list of file shares.</span></span>

## <span data-ttu-id="6c880-104">句法</span><span class="sxs-lookup"><span data-stu-id="6c880-104">SYNTAX</span></span>

### <span data-ttu-id="6c880-105">MatchingPrefix (預設) </span><span class="sxs-lookup"><span data-stu-id="6c880-105">MatchingPrefix (Default)</span></span>
```
Get-AzureStorageShare [[-Prefix] <String>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="6c880-106">明確</span><span class="sxs-lookup"><span data-stu-id="6c880-106">Specific</span></span>
```
Get-AzureStorageShare [-Name] <String> [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="6c880-107">說明</span><span class="sxs-lookup"><span data-stu-id="6c880-107">DESCRIPTION</span></span>
<span data-ttu-id="6c880-108">**AzureStorageShare** Cmdlet 會取得儲存空間帳戶的檔案共用清單。</span><span class="sxs-lookup"><span data-stu-id="6c880-108">The **Get-AzureStorageShare** cmdlet gets a list of file shares for a storage account.</span></span>

## <span data-ttu-id="6c880-109">示例</span><span class="sxs-lookup"><span data-stu-id="6c880-109">EXAMPLES</span></span>

### <span data-ttu-id="6c880-110">範例1：取得檔案共用</span><span class="sxs-lookup"><span data-stu-id="6c880-110">Example 1: Get a file share</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="6c880-111">這個命令會取得名為 ContosoShare06 的檔案共用。</span><span class="sxs-lookup"><span data-stu-id="6c880-111">This command gets the file share named ContosoShare06.</span></span>

### <span data-ttu-id="6c880-112">範例2：取得以字串開頭的所有檔案共用</span><span class="sxs-lookup"><span data-stu-id="6c880-112">Example 2: Get all file shares that begin with a string</span></span>
```
PS C:\>Get-AzureStorageShare -Prefix "Contoso"
```

<span data-ttu-id="6c880-113">這個命令會取得名稱以 Contoso 為開頭的所有檔案共用。</span><span class="sxs-lookup"><span data-stu-id="6c880-113">This command gets all file shares that have names that begin with Contoso.</span></span>

### <span data-ttu-id="6c880-114">範例3：在指定的內容中取得所有檔案共用</span><span class="sxs-lookup"><span data-stu-id="6c880-114">Example 3: Get all file shares in a specified context</span></span>
```
PS C:\>$Context = New-AzureStorageContext -Local
PS C:\> Get-AzureStorageShare -Context $Context
```

<span data-ttu-id="6c880-115">第一個命令使用 **AzureStorageCoNtext** Cmdlet，以使用 *Local* 參數建立內容，然後將該內容物件儲存在 $CoNtext 變數中。</span><span class="sxs-lookup"><span data-stu-id="6c880-115">The first command uses the **New-AzureStorageContext** cmdlet to create a context by using the *Local* parameter, and then stores that context object in the $Context variable.</span></span>

<span data-ttu-id="6c880-116">第二個命令會針對儲存在 $CoNtext 中的內容物件，取得檔案共用。</span><span class="sxs-lookup"><span data-stu-id="6c880-116">The second command gets the file shares for the context object stored in $Context.</span></span>

## <span data-ttu-id="6c880-117">參數</span><span class="sxs-lookup"><span data-stu-id="6c880-117">PARAMETERS</span></span>

### <span data-ttu-id="6c880-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6c880-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="6c880-119">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="6c880-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="6c880-120">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="6c880-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="6c880-121">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="6c880-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="6c880-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="6c880-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="6c880-123">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="6c880-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="6c880-124">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="6c880-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="6c880-125">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="6c880-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="6c880-126">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="6c880-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="6c880-127">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="6c880-127">The default value is 10.</span></span>

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

### <span data-ttu-id="6c880-128">-內容</span><span class="sxs-lookup"><span data-stu-id="6c880-128">-Context</span></span>
<span data-ttu-id="6c880-129">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="6c880-129">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="6c880-130">若要取得內容，請使用 [AzureStorageCoNtext](./New-AzureStorageContext.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6c880-130">To obtain a context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="6c880-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="6c880-131">-Name</span></span>
<span data-ttu-id="6c880-132">指定檔案共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="6c880-132">Specifies the name of the file share.</span></span>
<span data-ttu-id="6c880-133">這個 Cmdlet 會取得此參數指定的檔案共用，或者，如果您指定的檔案共用名稱稱不存在，則無任何動作。</span><span class="sxs-lookup"><span data-stu-id="6c880-133">This cmdlet gets the file share that this parameter specifies, or nothing if you specify the name of a file share that does not exist.</span></span>

```yaml
Type: String
Parameter Sets: Specific
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c880-134">-Prefix</span><span class="sxs-lookup"><span data-stu-id="6c880-134">-Prefix</span></span>
<span data-ttu-id="6c880-135">指定檔案共用的首碼。</span><span class="sxs-lookup"><span data-stu-id="6c880-135">Specifies the prefix for file shares.</span></span>
<span data-ttu-id="6c880-136">這個 Cmdlet 會取得與此參數指定的前置詞相符的檔案共用，如果沒有檔案共用與指定的首碼相符，就會取得檔案共用。</span><span class="sxs-lookup"><span data-stu-id="6c880-136">This cmdlet gets file shares that match the prefix that this parameter specifies, or no file shares if no file shares match the specified prefix.</span></span>

```yaml
Type: String
Parameter Sets: MatchingPrefix
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c880-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6c880-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="6c880-138">指定要求中伺服器部分的超時時間長度。</span><span class="sxs-lookup"><span data-stu-id="6c880-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="6c880-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c880-139">CommonParameters</span></span>
<span data-ttu-id="6c880-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6c880-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c880-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6c880-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c880-142">輸入</span><span class="sxs-lookup"><span data-stu-id="6c880-142">INPUTS</span></span>

## <span data-ttu-id="6c880-143">輸出</span><span class="sxs-lookup"><span data-stu-id="6c880-143">OUTPUTS</span></span>

## <span data-ttu-id="6c880-144">筆記</span><span class="sxs-lookup"><span data-stu-id="6c880-144">NOTES</span></span>

## <span data-ttu-id="6c880-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="6c880-145">RELATED LINKS</span></span>

[<span data-ttu-id="6c880-146">新-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="6c880-146">New-AzureStorageShare</span></span>](./New-AzureStorageShare.md)

[<span data-ttu-id="6c880-147">移除-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="6c880-147">Remove-AzureStorageShare</span></span>](./Remove-AzureStorageShare.md)
