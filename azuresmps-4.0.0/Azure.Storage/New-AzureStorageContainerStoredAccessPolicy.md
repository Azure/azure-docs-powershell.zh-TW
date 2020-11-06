---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C324F28A-7215-4F10-A012-92B4F6544BC0
online version: ''
schema: 2.0.0
ms.openlocfilehash: a95d5afafbed6ab6e3ba81cbfd509fd7b531217e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93623254"
---
# <span data-ttu-id="e5228-101">New-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e5228-101">New-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="e5228-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e5228-102">SYNOPSIS</span></span>
<span data-ttu-id="e5228-103">建立 Azure 儲存空間容器的儲存存取原則。</span><span class="sxs-lookup"><span data-stu-id="e5228-103">Creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="e5228-104">句法</span><span class="sxs-lookup"><span data-stu-id="e5228-104">SYNTAX</span></span>

```
New-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="e5228-105">說明</span><span class="sxs-lookup"><span data-stu-id="e5228-105">DESCRIPTION</span></span>
<span data-ttu-id="e5228-106">**新的-AzureStorageContainerStoredAccessPolicy** Cmdlet 會為 Azure 儲存空間容器建立儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="e5228-106">The **New-AzureStorageContainerStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="e5228-107">示例</span><span class="sxs-lookup"><span data-stu-id="e5228-107">EXAMPLES</span></span>

### <span data-ttu-id="e5228-108">範例1：在儲存空間容器中建立儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="e5228-108">Example 1: Create a stored access policy in a storage container</span></span>
```
PS C:\>New-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy01"
```

<span data-ttu-id="e5228-109">這個命令會在名為 MyContainer 的存儲容器中建立名為 Policy01 的訪問原則。</span><span class="sxs-lookup"><span data-stu-id="e5228-109">This command creates an access policy named Policy01 in the storage container named MyContainer.</span></span>

## <span data-ttu-id="e5228-110">參數</span><span class="sxs-lookup"><span data-stu-id="e5228-110">PARAMETERS</span></span>

### <span data-ttu-id="e5228-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e5228-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="e5228-112">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="e5228-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="e5228-113">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="e5228-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="e5228-114">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="e5228-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="e5228-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="e5228-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="e5228-116">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="e5228-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="e5228-117">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="e5228-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="e5228-118">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="e5228-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="e5228-119">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="e5228-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="e5228-120">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="e5228-120">The default value is 10.</span></span>

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

### <span data-ttu-id="e5228-121">-容器</span><span class="sxs-lookup"><span data-stu-id="e5228-121">-Container</span></span>
<span data-ttu-id="e5228-122">指定 Azure 儲存空間容器名稱。</span><span class="sxs-lookup"><span data-stu-id="e5228-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="e5228-123">-內容</span><span class="sxs-lookup"><span data-stu-id="e5228-123">-Context</span></span>
<span data-ttu-id="e5228-124">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="e5228-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="e5228-125">若要取得儲存內容，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5228-125">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="e5228-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="e5228-126">-ExpiryTime</span></span>
<span data-ttu-id="e5228-127">指定儲存的存取原則失效的時間。</span><span class="sxs-lookup"><span data-stu-id="e5228-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="e5228-128">-許可權</span><span class="sxs-lookup"><span data-stu-id="e5228-128">-Permission</span></span>
<span data-ttu-id="e5228-129">指定此容器的公開存取層級。</span><span class="sxs-lookup"><span data-stu-id="e5228-129">Specifies the level of public access to this container.</span></span>

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

### <span data-ttu-id="e5228-130">-原則</span><span class="sxs-lookup"><span data-stu-id="e5228-130">-Policy</span></span>
<span data-ttu-id="e5228-131">指定儲存的存取原則，包括此 SAS 權杖的許可權。</span><span class="sxs-lookup"><span data-stu-id="e5228-131">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="e5228-132">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e5228-132">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="e5228-133">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="e5228-133">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="e5228-134">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="e5228-134">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="e5228-135">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="e5228-135">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="e5228-136">-StartTime</span><span class="sxs-lookup"><span data-stu-id="e5228-136">-StartTime</span></span>
<span data-ttu-id="e5228-137">指定儲存的存取原則生效的時間。</span><span class="sxs-lookup"><span data-stu-id="e5228-137">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="e5228-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5228-138">CommonParameters</span></span>
<span data-ttu-id="e5228-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e5228-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5228-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e5228-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5228-141">輸入</span><span class="sxs-lookup"><span data-stu-id="e5228-141">INPUTS</span></span>

## <span data-ttu-id="e5228-142">輸出</span><span class="sxs-lookup"><span data-stu-id="e5228-142">OUTPUTS</span></span>

## <span data-ttu-id="e5228-143">筆記</span><span class="sxs-lookup"><span data-stu-id="e5228-143">NOTES</span></span>

## <span data-ttu-id="e5228-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="e5228-144">RELATED LINKS</span></span>

[<span data-ttu-id="e5228-145">AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e5228-145">Get-AzureStorageContainerStoredAccessPolicy</span></span>](./Get-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="e5228-146">新-AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="e5228-146">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="e5228-147">移除-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e5228-147">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="e5228-148">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e5228-148">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)


