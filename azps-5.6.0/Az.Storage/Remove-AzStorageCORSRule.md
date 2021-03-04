---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 26E06BA3-C550-40A5-B8E3-FEC8E9BF3867
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageCORSRule.md
ms.openlocfilehash: 9c6213fb619297ca5e2c49883f42a5d875d940e5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910349"
---
# <span data-ttu-id="6a315-101">Remove-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="6a315-101">Remove-AzStorageCORSRule</span></span>

## <span data-ttu-id="6a315-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6a315-102">SYNOPSIS</span></span>
<span data-ttu-id="6a315-103">移除儲存服務的 CORS。</span><span class="sxs-lookup"><span data-stu-id="6a315-103">Removes CORS for a Storage service.</span></span>

## <span data-ttu-id="6a315-104">語法</span><span class="sxs-lookup"><span data-stu-id="6a315-104">SYNTAX</span></span>

```
Remove-AzStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="6a315-105">描述</span><span class="sxs-lookup"><span data-stu-id="6a315-105">DESCRIPTION</span></span>
<span data-ttu-id="6a315-106">**Remove-AzStorageCORSRule** Cmdlet 會移除 Azure 儲存 (CORS) 的跨來源資源分享。</span><span class="sxs-lookup"><span data-stu-id="6a315-106">The **Remove-AzStorageCORSRule** cmdlet removes Cross-Origin Resource Sharing (CORS) for an Azure Storage service.</span></span>
<span data-ttu-id="6a315-107">此 Cmdlet 會刪除儲存服務類型中所有的 CORS 規則。</span><span class="sxs-lookup"><span data-stu-id="6a315-107">This cmdlet deletes all CORS rules in a Storage service type.</span></span>
<span data-ttu-id="6a315-108">此 Cmdlet 的儲存服務類型為 Blob、資料表、佇列和檔案。</span><span class="sxs-lookup"><span data-stu-id="6a315-108">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>

## <span data-ttu-id="6a315-109">例子</span><span class="sxs-lookup"><span data-stu-id="6a315-109">EXAMPLES</span></span>

### <span data-ttu-id="6a315-110">範例 1：移除 Blob 服務的 CORS 規則</span><span class="sxs-lookup"><span data-stu-id="6a315-110">Example 1: Remove CORS rules for the blob service</span></span>
```
PS C:\>Remove-AzStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="6a315-111">此命令會移除 Blob 服務類型的 CORS 規則。</span><span class="sxs-lookup"><span data-stu-id="6a315-111">This command removes CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="6a315-112">參數</span><span class="sxs-lookup"><span data-stu-id="6a315-112">PARAMETERS</span></span>

### <span data-ttu-id="6a315-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6a315-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="6a315-114">指定一個服務要求用戶端的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="6a315-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="6a315-115">如果前一個通話在指定的時間間隔內失敗，此 Cmdlet 會重新重試要求。</span><span class="sxs-lookup"><span data-stu-id="6a315-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="6a315-116">如果此 Cmdlet 在間隔經過之前未收到成功回應，此 Cmdlet 會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="6a315-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="6a315-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="6a315-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="6a315-118">指定同時進行的最大網路通話數。</span><span class="sxs-lookup"><span data-stu-id="6a315-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="6a315-119">您可以使用此參數來限制並行，以節流本地 CPU 和頻寬使用量，方法為指定並行網路通話的數量上限。</span><span class="sxs-lookup"><span data-stu-id="6a315-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="6a315-120">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="6a315-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="6a315-121">此參數有助於減少低頻寬環境的網路連接問題，例如每秒 100 KB。</span><span class="sxs-lookup"><span data-stu-id="6a315-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="6a315-122">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="6a315-122">The default value is 10.</span></span>

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

### <span data-ttu-id="6a315-123">-內容</span><span class="sxs-lookup"><span data-stu-id="6a315-123">-Context</span></span>
<span data-ttu-id="6a315-124">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="6a315-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="6a315-125">若要取得儲存內容，New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6a315-125">To obtain the storage context, the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="6a315-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a315-126">-DefaultProfile</span></span>
<span data-ttu-id="6a315-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6a315-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a315-128">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6a315-128">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="6a315-129">指定要求的伺服器部分之時間長度。</span><span class="sxs-lookup"><span data-stu-id="6a315-129">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="6a315-130">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="6a315-130">-ServiceType</span></span>
<span data-ttu-id="6a315-131">指定此 Cmdlet 會移除規則的 Azure 儲存體服務類型。</span><span class="sxs-lookup"><span data-stu-id="6a315-131">Specifies the Azure Storage service type for which this cmdlet removes rules.</span></span>
<span data-ttu-id="6a315-132">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="6a315-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6a315-133">Blob</span><span class="sxs-lookup"><span data-stu-id="6a315-133">Blob</span></span> 
- <span data-ttu-id="6a315-134">表</span><span class="sxs-lookup"><span data-stu-id="6a315-134">Table</span></span> 
- <span data-ttu-id="6a315-135">佇列</span><span class="sxs-lookup"><span data-stu-id="6a315-135">Queue</span></span> 
- <span data-ttu-id="6a315-136">檔</span><span class="sxs-lookup"><span data-stu-id="6a315-136">File</span></span>

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

### <span data-ttu-id="6a315-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a315-137">CommonParameters</span></span>
<span data-ttu-id="6a315-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6a315-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a315-139">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="6a315-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a315-140">輸入</span><span class="sxs-lookup"><span data-stu-id="6a315-140">INPUTS</span></span>

### <span data-ttu-id="6a315-141">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="6a315-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6a315-142">輸出</span><span class="sxs-lookup"><span data-stu-id="6a315-142">OUTPUTS</span></span>

### <span data-ttu-id="6a315-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="6a315-143">System.Void</span></span>

## <span data-ttu-id="6a315-144">筆記</span><span class="sxs-lookup"><span data-stu-id="6a315-144">NOTES</span></span>

## <span data-ttu-id="6a315-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="6a315-145">RELATED LINKS</span></span>

[<span data-ttu-id="6a315-146">Get-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="6a315-146">Get-AzStorageCORSRule</span></span>](./Get-AzStorageCORSRule.md)

[<span data-ttu-id="6a315-147">Set-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="6a315-147">Set-AzStorageCORSRule</span></span>](./Set-AzStorageCORSRule.md)


