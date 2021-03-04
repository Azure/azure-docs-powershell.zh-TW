---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5FA8A3F3-F52C-40BC-94C2-4CDA00C6F32F
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageCORSRule.md
ms.openlocfilehash: e4313dda57632fbc2a5381b1f92067da85c1a905
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915117"
---
# <span data-ttu-id="4c8ac-101">Get-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="4c8ac-101">Get-AzStorageCORSRule</span></span>

## <span data-ttu-id="4c8ac-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4c8ac-102">SYNOPSIS</span></span>
<span data-ttu-id="4c8ac-103">為儲存服務類型獲得 CORS 規則。</span><span class="sxs-lookup"><span data-stu-id="4c8ac-103">Gets CORS rules for a Storage service type.</span></span>

## <span data-ttu-id="4c8ac-104">語法</span><span class="sxs-lookup"><span data-stu-id="4c8ac-104">SYNTAX</span></span>

```
Get-AzStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="4c8ac-105">描述</span><span class="sxs-lookup"><span data-stu-id="4c8ac-105">DESCRIPTION</span></span>
<span data-ttu-id="4c8ac-106">**Get-AzStorageCORSRule** Cmdlet 會取得 Azure 儲存服務類型的 (CORS) 規則。</span><span class="sxs-lookup"><span data-stu-id="4c8ac-106">The **Get-AzStorageCORSRule** cmdlet gets Cross-Origin Resource Sharing (CORS) rules for an Azure Storage service type.</span></span>

## <span data-ttu-id="4c8ac-107">例子</span><span class="sxs-lookup"><span data-stu-id="4c8ac-107">EXAMPLES</span></span>

### <span data-ttu-id="4c8ac-108">範例 1：取得 Blob 服務的 CORS 規則</span><span class="sxs-lookup"><span data-stu-id="4c8ac-108">Example 1: Get CORS rules of blob service</span></span>
```
PS C:\>Get-AzStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="4c8ac-109">此命令會獲得 Blob 服務類型的 CORS 規則。</span><span class="sxs-lookup"><span data-stu-id="4c8ac-109">This command gets the CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="4c8ac-110">參數</span><span class="sxs-lookup"><span data-stu-id="4c8ac-110">PARAMETERS</span></span>

### <span data-ttu-id="4c8ac-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4c8ac-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="4c8ac-112">指定一個服務要求用戶端的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="4c8ac-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="4c8ac-113">如果前一個通話在指定的時間間隔內失敗，此 Cmdlet 會重新重試要求。</span><span class="sxs-lookup"><span data-stu-id="4c8ac-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="4c8ac-114">如果此 Cmdlet 在間隔經過之前未收到成功回應，此 Cmdlet 會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="4c8ac-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="4c8ac-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="4c8ac-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="4c8ac-116">指定同時進行的最大網路通話數。</span><span class="sxs-lookup"><span data-stu-id="4c8ac-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="4c8ac-117">您可以使用此參數來限制並行，以節流本地 CPU 和頻寬使用量，方法為指定並行網路通話的數量上限。</span><span class="sxs-lookup"><span data-stu-id="4c8ac-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="4c8ac-118">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="4c8ac-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="4c8ac-119">此參數有助於減少低頻寬環境的網路連接問題，例如每秒 100 KB。</span><span class="sxs-lookup"><span data-stu-id="4c8ac-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="4c8ac-120">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="4c8ac-120">The default value is 10.</span></span>

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

### <span data-ttu-id="4c8ac-121">-內容</span><span class="sxs-lookup"><span data-stu-id="4c8ac-121">-Context</span></span>
<span data-ttu-id="4c8ac-122">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="4c8ac-122">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="4c8ac-123">若要取得內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4c8ac-123">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="4c8ac-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c8ac-124">-DefaultProfile</span></span>
<span data-ttu-id="4c8ac-125">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4c8ac-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c8ac-126">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4c8ac-126">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="4c8ac-127">指定要求的伺服器部分之時間長度。</span><span class="sxs-lookup"><span data-stu-id="4c8ac-127">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="4c8ac-128">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="4c8ac-128">-ServiceType</span></span>
<span data-ttu-id="4c8ac-129">指定此 Cmdlet 會獲得 CORS 規則的 Azure 儲存體服務類型。</span><span class="sxs-lookup"><span data-stu-id="4c8ac-129">Specifies the Azure Storage service type for which this cmdlet gets CORS rules.</span></span>
<span data-ttu-id="4c8ac-130">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="4c8ac-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4c8ac-131">Blob</span><span class="sxs-lookup"><span data-stu-id="4c8ac-131">Blob</span></span> 
- <span data-ttu-id="4c8ac-132">表</span><span class="sxs-lookup"><span data-stu-id="4c8ac-132">Table</span></span> 
- <span data-ttu-id="4c8ac-133">佇列</span><span class="sxs-lookup"><span data-stu-id="4c8ac-133">Queue</span></span> 
- <span data-ttu-id="4c8ac-134">檔</span><span class="sxs-lookup"><span data-stu-id="4c8ac-134">File</span></span>

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

### <span data-ttu-id="4c8ac-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c8ac-135">CommonParameters</span></span>
<span data-ttu-id="4c8ac-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4c8ac-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c8ac-137">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="4c8ac-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c8ac-138">輸入</span><span class="sxs-lookup"><span data-stu-id="4c8ac-138">INPUTS</span></span>

### <span data-ttu-id="4c8ac-139">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="4c8ac-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4c8ac-140">輸出</span><span class="sxs-lookup"><span data-stu-id="4c8ac-140">OUTPUTS</span></span>

### <span data-ttu-id="4c8ac-141">Microsoft.WindowsAzure.Commands.storage.Model.ResourceModel.PSCorsRule</span><span class="sxs-lookup"><span data-stu-id="4c8ac-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span></span>

## <span data-ttu-id="4c8ac-142">筆記</span><span class="sxs-lookup"><span data-stu-id="4c8ac-142">NOTES</span></span>

## <span data-ttu-id="4c8ac-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="4c8ac-143">RELATED LINKS</span></span>

[<span data-ttu-id="4c8ac-144">Remove-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="4c8ac-144">Remove-AzStorageCORSRule</span></span>](./Remove-AzStorageCORSRule.md)

[<span data-ttu-id="4c8ac-145">Set-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="4c8ac-145">Set-AzStorageCORSRule</span></span>](./Set-AzStorageCORSRule.md)


