---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: FD3A0013-4365-4E65-891C-5C50A9D5658C
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageShare.md
ms.openlocfilehash: 31a8d6cbb205b451233bdc72793fb45443350fdd
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "93626659"
---
# <span data-ttu-id="7af26-101">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="7af26-101">Get-AzureStorageShare</span></span>

## <span data-ttu-id="7af26-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7af26-102">SYNOPSIS</span></span>
<span data-ttu-id="7af26-103">取得檔案共用的清單。</span><span class="sxs-lookup"><span data-stu-id="7af26-103">Gets a list of file shares.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7af26-104">句法</span><span class="sxs-lookup"><span data-stu-id="7af26-104">SYNTAX</span></span>

### <span data-ttu-id="7af26-105">MatchingPrefix (預設) </span><span class="sxs-lookup"><span data-stu-id="7af26-105">MatchingPrefix (Default)</span></span>
```
Get-AzureStorageShare [[-Prefix] <String>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="7af26-106">明確</span><span class="sxs-lookup"><span data-stu-id="7af26-106">Specific</span></span>
```
Get-AzureStorageShare [-Name] <String> [[-SnapshotTime] <DateTimeOffset>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="7af26-107">說明</span><span class="sxs-lookup"><span data-stu-id="7af26-107">DESCRIPTION</span></span>
<span data-ttu-id="7af26-108">**AzureStorageShare** Cmdlet 會取得儲存空間帳戶的檔案共用清單。</span><span class="sxs-lookup"><span data-stu-id="7af26-108">The **Get-AzureStorageShare** cmdlet gets a list of file shares for a storage account.</span></span>

## <span data-ttu-id="7af26-109">示例</span><span class="sxs-lookup"><span data-stu-id="7af26-109">EXAMPLES</span></span>

### <span data-ttu-id="7af26-110">範例1：取得檔案共用</span><span class="sxs-lookup"><span data-stu-id="7af26-110">Example 1: Get a file share</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="7af26-111">這個命令會取得名為 ContosoShare06 的檔案共用。</span><span class="sxs-lookup"><span data-stu-id="7af26-111">This command gets the file share named ContosoShare06.</span></span>

### <span data-ttu-id="7af26-112">範例2：取得以字串開頭的所有檔案共用</span><span class="sxs-lookup"><span data-stu-id="7af26-112">Example 2: Get all file shares that begin with a string</span></span>
```
PS C:\>Get-AzureStorageShare -Prefix "Contoso"
```

<span data-ttu-id="7af26-113">這個命令會取得名稱以 Contoso 為開頭的所有檔案共用。</span><span class="sxs-lookup"><span data-stu-id="7af26-113">This command gets all file shares that have names that begin with Contoso.</span></span>

### <span data-ttu-id="7af26-114">範例3：在指定的內容中取得所有檔案共用</span><span class="sxs-lookup"><span data-stu-id="7af26-114">Example 3: Get all file shares in a specified context</span></span>
```
PS C:\>$Context = New-AzureStorageContext -Local
PS C:\> Get-AzureStorageShare -Context $Context
```

<span data-ttu-id="7af26-115">第一個命令使用 **AzureStorageCoNtext** Cmdlet，以使用 *Local* 參數建立內容，然後將該內容物件儲存在 $CoNtext 變數中。</span><span class="sxs-lookup"><span data-stu-id="7af26-115">The first command uses the **New-AzureStorageContext** cmdlet to create a context by using the *Local* parameter, and then stores that context object in the $Context variable.</span></span>
<span data-ttu-id="7af26-116">第二個命令會針對儲存在 $CoNtext 中的內容物件，取得檔案共用。</span><span class="sxs-lookup"><span data-stu-id="7af26-116">The second command gets the file shares for the context object stored in $Context.</span></span>

### <span data-ttu-id="7af26-117">範例4：取得含特定共用名稱稱和 SnapshotTime 的檔案共用快照</span><span class="sxs-lookup"><span data-stu-id="7af26-117">Example 4: Get a file share snapshot with specific share name and SnapshotTime</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06" -SnapshotTime "6/16/2017 9:48:41 AM +00:00"
```

<span data-ttu-id="7af26-118">這個命令會取得含特定共用名稱稱和 SnapshotTime 的檔案共用快照。</span><span class="sxs-lookup"><span data-stu-id="7af26-118">This command gets a file share snapshot with specific share name and SnapshotTime.</span></span>

## <span data-ttu-id="7af26-119">參數</span><span class="sxs-lookup"><span data-stu-id="7af26-119">PARAMETERS</span></span>

### <span data-ttu-id="7af26-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7af26-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="7af26-121">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="7af26-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="7af26-122">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="7af26-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="7af26-123">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="7af26-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="7af26-124">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="7af26-124">-ConcurrentTaskCount</span></span>
<span data-ttu-id="7af26-125">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="7af26-125">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="7af26-126">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="7af26-126">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="7af26-127">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="7af26-127">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="7af26-128">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="7af26-128">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="7af26-129">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="7af26-129">The default value is 10.</span></span>

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

### <span data-ttu-id="7af26-130">-內容</span><span class="sxs-lookup"><span data-stu-id="7af26-130">-Context</span></span>
<span data-ttu-id="7af26-131">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="7af26-131">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="7af26-132">若要取得內容，請使用 [AzureStorageCoNtext](./New-AzureStorageContext.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7af26-132">To obtain a context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="7af26-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7af26-133">-DefaultProfile</span></span>
<span data-ttu-id="7af26-134">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7af26-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7af26-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="7af26-135">-Name</span></span>
<span data-ttu-id="7af26-136">指定檔案共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="7af26-136">Specifies the name of the file share.</span></span>
<span data-ttu-id="7af26-137">這個 Cmdlet 會取得此參數指定的檔案共用，或者，如果您指定的檔案共用名稱稱不存在，則無任何動作。</span><span class="sxs-lookup"><span data-stu-id="7af26-137">This cmdlet gets the file share that this parameter specifies, or nothing if you specify the name of a file share that does not exist.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7af26-138">-Prefix</span><span class="sxs-lookup"><span data-stu-id="7af26-138">-Prefix</span></span>
<span data-ttu-id="7af26-139">指定檔案共用的首碼。</span><span class="sxs-lookup"><span data-stu-id="7af26-139">Specifies the prefix for file shares.</span></span>
<span data-ttu-id="7af26-140">這個 Cmdlet 會取得與此參數指定的前置詞相符的檔案共用，如果沒有檔案共用與指定的首碼相符，就會取得檔案共用。</span><span class="sxs-lookup"><span data-stu-id="7af26-140">This cmdlet gets file shares that match the prefix that this parameter specifies, or no file shares if no file shares match the specified prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: MatchingPrefix
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7af26-141">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7af26-141">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="7af26-142">指定要求中伺服器部分的超時時間長度。</span><span class="sxs-lookup"><span data-stu-id="7af26-142">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="7af26-143">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="7af26-143">-SnapshotTime</span></span>
<span data-ttu-id="7af26-144">SnapshotTime 要接收的檔案共用快照。</span><span class="sxs-lookup"><span data-stu-id="7af26-144">SnapshotTime of the file share snapshot to be received.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: Specific
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7af26-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7af26-145">CommonParameters</span></span>
<span data-ttu-id="7af26-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7af26-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7af26-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7af26-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7af26-148">輸入</span><span class="sxs-lookup"><span data-stu-id="7af26-148">INPUTS</span></span>

### <span data-ttu-id="7af26-149">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="7af26-149">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7af26-150">輸出</span><span class="sxs-lookup"><span data-stu-id="7af26-150">OUTPUTS</span></span>

### <span data-ttu-id="7af26-151">[WindowsAzure] CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="7af26-151">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>

## <span data-ttu-id="7af26-152">筆記</span><span class="sxs-lookup"><span data-stu-id="7af26-152">NOTES</span></span>

## <span data-ttu-id="7af26-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="7af26-153">RELATED LINKS</span></span>

[<span data-ttu-id="7af26-154">新-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="7af26-154">New-AzureStorageShare</span></span>](./New-AzureStorageShare.md)

[<span data-ttu-id="7af26-155">移除-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="7af26-155">Remove-AzureStorageShare</span></span>](./Remove-AzureStorageShare.md)