---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FD3A0013-4365-4E65-891C-5C50A9D5658C
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShare.md
ms.openlocfilehash: 88655ed408242794c6f23a7b170dc007a11ced50
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915714"
---
# <span data-ttu-id="58e48-101">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="58e48-101">Get-AzStorageShare</span></span>

## <span data-ttu-id="58e48-102">簡介</span><span class="sxs-lookup"><span data-stu-id="58e48-102">SYNOPSIS</span></span>
<span data-ttu-id="58e48-103">獲得檔案共用清單。</span><span class="sxs-lookup"><span data-stu-id="58e48-103">Gets a list of file shares.</span></span>

## <span data-ttu-id="58e48-104">語法</span><span class="sxs-lookup"><span data-stu-id="58e48-104">SYNTAX</span></span>

### <span data-ttu-id="58e48-105">比對Prefix (預設) </span><span class="sxs-lookup"><span data-stu-id="58e48-105">MatchingPrefix (Default)</span></span>
```
Get-AzStorageShare [[-Prefix] <String>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="58e48-106">特定</span><span class="sxs-lookup"><span data-stu-id="58e48-106">Specific</span></span>
```
Get-AzStorageShare [-Name] <String> [[-SnapshotTime] <DateTimeOffset>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="58e48-107">描述</span><span class="sxs-lookup"><span data-stu-id="58e48-107">DESCRIPTION</span></span>
<span data-ttu-id="58e48-108">**Get-AzStorageShare** Cmdlet 會取得儲存帳戶的檔案共用清單。</span><span class="sxs-lookup"><span data-stu-id="58e48-108">The **Get-AzStorageShare** cmdlet gets a list of file shares for a storage account.</span></span>

## <span data-ttu-id="58e48-109">例子</span><span class="sxs-lookup"><span data-stu-id="58e48-109">EXAMPLES</span></span>

### <span data-ttu-id="58e48-110">範例 1：取得檔案共用</span><span class="sxs-lookup"><span data-stu-id="58e48-110">Example 1: Get a file share</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="58e48-111">此命令會獲得名為 ContosoShare06 的檔案共用。</span><span class="sxs-lookup"><span data-stu-id="58e48-111">This command gets the file share named ContosoShare06.</span></span>

### <span data-ttu-id="58e48-112">範例 2：取得以字串開頭的所有檔案共用</span><span class="sxs-lookup"><span data-stu-id="58e48-112">Example 2: Get all file shares that begin with a string</span></span>
```
PS C:\>Get-AzStorageShare -Prefix "Contoso"
```

<span data-ttu-id="58e48-113">此命令會獲得名稱以 Contoso 開頭的所有檔案共用。</span><span class="sxs-lookup"><span data-stu-id="58e48-113">This command gets all file shares that have names that begin with Contoso.</span></span>

### <span data-ttu-id="58e48-114">範例 3：取得指定內容的所有檔案共用</span><span class="sxs-lookup"><span data-stu-id="58e48-114">Example 3: Get all file shares in a specified context</span></span>
```
PS C:\>$Context = New-AzStorageContext -Local
PS C:\> Get-AzStorageShare -Context $Context
```

<span data-ttu-id="58e48-115">第一個命令使用 **New-AzStorageCoNtext** Cmdlet 使用 *Local* 參數建立上下文，然後將該上下文物件儲存在 $CoNtext 變數中。</span><span class="sxs-lookup"><span data-stu-id="58e48-115">The first command uses the **New-AzStorageContext** cmdlet to create a context by using the *Local* parameter, and then stores that context object in the $Context variable.</span></span>
<span data-ttu-id="58e48-116">第二個命令會針對儲存在檔案中的上下文物件$CoNtext。</span><span class="sxs-lookup"><span data-stu-id="58e48-116">The second command gets the file shares for the context object stored in $Context.</span></span>

### <span data-ttu-id="58e48-117">範例 4：取得具有特定共用名稱稱和 SnapshotTime 的檔案共用快照</span><span class="sxs-lookup"><span data-stu-id="58e48-117">Example 4: Get a file share snapshot with specific share name and SnapshotTime</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" -SnapshotTime "6/16/2017 9:48:41 AM +00:00"
```

<span data-ttu-id="58e48-118">此命令會獲得具有特定共用名稱稱和 SnapshotTime 的檔案共用快照。</span><span class="sxs-lookup"><span data-stu-id="58e48-118">This command gets a file share snapshot with specific share name and SnapshotTime.</span></span>

## <span data-ttu-id="58e48-119">參數</span><span class="sxs-lookup"><span data-stu-id="58e48-119">PARAMETERS</span></span>

### <span data-ttu-id="58e48-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="58e48-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="58e48-121">指定一個服務要求用戶端的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="58e48-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="58e48-122">如果前一個通話在指定的時間間隔內失敗，此 Cmdlet 會重新重試要求。</span><span class="sxs-lookup"><span data-stu-id="58e48-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="58e48-123">如果此 Cmdlet 在間隔經過之前未收到成功回應，此 Cmdlet 會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="58e48-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="58e48-124">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="58e48-124">-ConcurrentTaskCount</span></span>
<span data-ttu-id="58e48-125">指定同時進行的最大網路通話數。</span><span class="sxs-lookup"><span data-stu-id="58e48-125">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="58e48-126">您可以使用此參數來限制並行，以節流本地 CPU 和頻寬使用量，方法為指定並行網路通話的數量上限。</span><span class="sxs-lookup"><span data-stu-id="58e48-126">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="58e48-127">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="58e48-127">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="58e48-128">此參數有助於減少低頻寬環境的網路連接問題，例如每秒 100 KB。</span><span class="sxs-lookup"><span data-stu-id="58e48-128">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="58e48-129">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="58e48-129">The default value is 10.</span></span>

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

### <span data-ttu-id="58e48-130">-內容</span><span class="sxs-lookup"><span data-stu-id="58e48-130">-Context</span></span>
<span data-ttu-id="58e48-131">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="58e48-131">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="58e48-132">若要取得內容，請使用 [New-AzStorageCoNtext](./New-AzStorageContext.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="58e48-132">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="58e48-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58e48-133">-DefaultProfile</span></span>
<span data-ttu-id="58e48-134">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="58e48-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58e48-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="58e48-135">-Name</span></span>
<span data-ttu-id="58e48-136">指定檔案共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="58e48-136">Specifies the name of the file share.</span></span>
<span data-ttu-id="58e48-137">此 Cmdlet 會獲得此參數指定的檔案共用，如果您指定不存在的檔案共用名稱稱，則沒有任何專案。</span><span class="sxs-lookup"><span data-stu-id="58e48-137">This cmdlet gets the file share that this parameter specifies, or nothing if you specify the name of a file share that does not exist.</span></span>

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

### <span data-ttu-id="58e48-138">-首碼</span><span class="sxs-lookup"><span data-stu-id="58e48-138">-Prefix</span></span>
<span data-ttu-id="58e48-139">指定檔案共用首碼。</span><span class="sxs-lookup"><span data-stu-id="58e48-139">Specifies the prefix for file shares.</span></span>
<span data-ttu-id="58e48-140">此 Cmdlet 會獲得符合此參數指定之首碼的檔案共用，如果沒有檔案共用符合指定的首碼，則不會共用任何檔案。</span><span class="sxs-lookup"><span data-stu-id="58e48-140">This cmdlet gets file shares that match the prefix that this parameter specifies, or no file shares if no file shares match the specified prefix.</span></span>

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

### <span data-ttu-id="58e48-141">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="58e48-141">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="58e48-142">指定要求的伺服器部分之時間長度。</span><span class="sxs-lookup"><span data-stu-id="58e48-142">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="58e48-143">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="58e48-143">-SnapshotTime</span></span>
<span data-ttu-id="58e48-144">要接收之檔案共用快照的快照時間。</span><span class="sxs-lookup"><span data-stu-id="58e48-144">SnapshotTime of the file share snapshot to be received.</span></span>

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

### <span data-ttu-id="58e48-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58e48-145">CommonParameters</span></span>
<span data-ttu-id="58e48-146">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="58e48-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58e48-147">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="58e48-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58e48-148">輸入</span><span class="sxs-lookup"><span data-stu-id="58e48-148">INPUTS</span></span>

### <span data-ttu-id="58e48-149">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="58e48-149">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="58e48-150">輸出</span><span class="sxs-lookup"><span data-stu-id="58e48-150">OUTPUTS</span></span>

### <span data-ttu-id="58e48-151">Microsoft.WindowsAzure.Commands.Common.storage.ResourceModel.AzureStorageFileShare</span><span class="sxs-lookup"><span data-stu-id="58e48-151">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span></span>

## <span data-ttu-id="58e48-152">筆記</span><span class="sxs-lookup"><span data-stu-id="58e48-152">NOTES</span></span>

## <span data-ttu-id="58e48-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="58e48-153">RELATED LINKS</span></span>

[<span data-ttu-id="58e48-154">New-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="58e48-154">New-AzStorageShare</span></span>](./New-AzStorageShare.md)

[<span data-ttu-id="58e48-155">Remove-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="58e48-155">Remove-AzStorageShare</span></span>](./Remove-AzStorageShare.md)
