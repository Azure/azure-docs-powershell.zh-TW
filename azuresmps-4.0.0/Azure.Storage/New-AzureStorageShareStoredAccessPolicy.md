---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 37E76360-B683-407C-9AEF-7138374562D8
online version: ''
schema: 2.0.0
ms.openlocfilehash: f76cd56055e800dc5d7d5ac15e66be23621ffbe2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93442744"
---
# <span data-ttu-id="c0e3f-101">New-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c0e3f-101">New-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="c0e3f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c0e3f-102">SYNOPSIS</span></span>
<span data-ttu-id="c0e3f-103">在儲存空間共用上建立儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="c0e3f-103">Creates a stored access policy on a Storage share.</span></span>

## <span data-ttu-id="c0e3f-104">句法</span><span class="sxs-lookup"><span data-stu-id="c0e3f-104">SYNTAX</span></span>

```
New-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="c0e3f-105">說明</span><span class="sxs-lookup"><span data-stu-id="c0e3f-105">DESCRIPTION</span></span>
<span data-ttu-id="c0e3f-106">**新的-AzureStorageShareStoredAccessPolicy** Cmdlet 會在 Azure 儲存空間共用上建立儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="c0e3f-106">The **New-AzureStorageShareStoredAccessPolicy** cmdlet creates a stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="c0e3f-107">示例</span><span class="sxs-lookup"><span data-stu-id="c0e3f-107">EXAMPLES</span></span>

### <span data-ttu-id="c0e3f-108">範例1：在共用中建立儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="c0e3f-108">Example 1: Create a stored access policy in a share</span></span>
```
PS C:\>New-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="c0e3f-109">這個命令會建立一個在共用中擁有完整許可權的儲存存取原則。</span><span class="sxs-lookup"><span data-stu-id="c0e3f-109">This command creates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="c0e3f-110">參數</span><span class="sxs-lookup"><span data-stu-id="c0e3f-110">PARAMETERS</span></span>

### <span data-ttu-id="c0e3f-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c0e3f-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c0e3f-112">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="c0e3f-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c0e3f-113">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="c0e3f-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c0e3f-114">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="c0e3f-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c0e3f-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c0e3f-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c0e3f-116">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="c0e3f-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="c0e3f-117">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="c0e3f-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="c0e3f-118">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="c0e3f-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="c0e3f-119">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="c0e3f-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="c0e3f-120">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="c0e3f-120">The default value is 10.</span></span>

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

### <span data-ttu-id="c0e3f-121">-內容</span><span class="sxs-lookup"><span data-stu-id="c0e3f-121">-Context</span></span>
<span data-ttu-id="c0e3f-122">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="c0e3f-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="c0e3f-123">若要取得儲存內容，請使用 [AzureStorageCoNtext](./New-AzureStorageContext.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c0e3f-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="c0e3f-124">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="c0e3f-124">-ExpiryTime</span></span>
<span data-ttu-id="c0e3f-125">指定儲存的存取原則失效的時間。</span><span class="sxs-lookup"><span data-stu-id="c0e3f-125">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0e3f-126">-許可權</span><span class="sxs-lookup"><span data-stu-id="c0e3f-126">-Permission</span></span>
<span data-ttu-id="c0e3f-127">指定儲存的存取原則中的許可權，以存取儲存空間共用或其下的檔案。</span><span class="sxs-lookup"><span data-stu-id="c0e3f-127">Specifies permissions in the stored access policy to access the Storage share or files under it.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0e3f-128">-原則</span><span class="sxs-lookup"><span data-stu-id="c0e3f-128">-Policy</span></span>
<span data-ttu-id="c0e3f-129">指定儲存的存取原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="c0e3f-129">Specifies a name for the stored access policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0e3f-130">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c0e3f-130">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c0e3f-131">指定要求中伺服器部分的超時時間長度。</span><span class="sxs-lookup"><span data-stu-id="c0e3f-131">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="c0e3f-132">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="c0e3f-132">-ShareName</span></span>
<span data-ttu-id="c0e3f-133">指定儲存空間共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="c0e3f-133">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="c0e3f-134">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c0e3f-134">-StartTime</span></span>
<span data-ttu-id="c0e3f-135">指定儲存的存取原則生效的時間。</span><span class="sxs-lookup"><span data-stu-id="c0e3f-135">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0e3f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0e3f-136">CommonParameters</span></span>
<span data-ttu-id="c0e3f-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c0e3f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0e3f-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c0e3f-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0e3f-139">輸入</span><span class="sxs-lookup"><span data-stu-id="c0e3f-139">INPUTS</span></span>

## <span data-ttu-id="c0e3f-140">輸出</span><span class="sxs-lookup"><span data-stu-id="c0e3f-140">OUTPUTS</span></span>

## <span data-ttu-id="c0e3f-141">筆記</span><span class="sxs-lookup"><span data-stu-id="c0e3f-141">NOTES</span></span>

## <span data-ttu-id="c0e3f-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="c0e3f-142">RELATED LINKS</span></span>

[<span data-ttu-id="c0e3f-143">AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c0e3f-143">Get-AzureStorageShareStoredAccessPolicy</span></span>](./Get-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="c0e3f-144">新-AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="c0e3f-144">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="c0e3f-145">移除-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c0e3f-145">Remove-AzureStorageShareStoredAccessPolicy</span></span>](./Remove-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="c0e3f-146">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c0e3f-146">Set-AzureStorageShareStoredAccessPolicy</span></span>](./Set-AzureStorageShareStoredAccessPolicy.md)
