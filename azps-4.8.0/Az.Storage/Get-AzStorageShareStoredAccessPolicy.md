---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 73BB521B-20F2-4F2B-AA88-2B128F36A9EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 2e444fba12f0ffebfd3d6679293cac31fc574e93
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970044"
---
# <span data-ttu-id="0743a-101">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0743a-101">Get-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="0743a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0743a-102">SYNOPSIS</span></span>
<span data-ttu-id="0743a-103">取得儲存空間共用的存取原則。</span><span class="sxs-lookup"><span data-stu-id="0743a-103">Gets stored access policies for a Storage share.</span></span>

## <span data-ttu-id="0743a-104">句法</span><span class="sxs-lookup"><span data-stu-id="0743a-104">SYNTAX</span></span>

```
Get-AzStorageShareStoredAccessPolicy [-ShareName] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="0743a-105">說明</span><span class="sxs-lookup"><span data-stu-id="0743a-105">DESCRIPTION</span></span>
<span data-ttu-id="0743a-106">**AzStorageShareStoredAccessPolicy** Cmdlet 會針對 Azure 儲存空間共用取得儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="0743a-106">The **Get-AzStorageShareStoredAccessPolicy** cmdlet gets stored access policies for an Azure Storage share.</span></span>
<span data-ttu-id="0743a-107">若要取得特定原則，請依名稱指定。</span><span class="sxs-lookup"><span data-stu-id="0743a-107">To get a particular policy, specify it by name.</span></span>

## <span data-ttu-id="0743a-108">示例</span><span class="sxs-lookup"><span data-stu-id="0743a-108">EXAMPLES</span></span>

### <span data-ttu-id="0743a-109">範例1：在共用中取得儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="0743a-109">Example 1: Get a stored access policy in a share</span></span>
```
PS C:\>Get-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="0743a-110">這個命令會在 ContosoShare 中取得名為 GeneralPolicy 的儲存訪問原則。</span><span class="sxs-lookup"><span data-stu-id="0743a-110">This command gets a stored access policy named GeneralPolicy in ContosoShare.</span></span>

### <span data-ttu-id="0743a-111">範例2：取得共用中所有已儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="0743a-111">Example 2: Get all the stored access policies in share</span></span>
```
PS C:\>Get-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare"
```

<span data-ttu-id="0743a-112">這個命令會取得 ContosoShare 中所有已儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="0743a-112">This command gets all stored access policies in ContosoShare.</span></span>

## <span data-ttu-id="0743a-113">參數</span><span class="sxs-lookup"><span data-stu-id="0743a-113">PARAMETERS</span></span>

### <span data-ttu-id="0743a-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0743a-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="0743a-115">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="0743a-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="0743a-116">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="0743a-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="0743a-117">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="0743a-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="0743a-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="0743a-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="0743a-119">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="0743a-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="0743a-120">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="0743a-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="0743a-121">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="0743a-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="0743a-122">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="0743a-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="0743a-123">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="0743a-123">The default value is 10.</span></span>

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

### <span data-ttu-id="0743a-124">-內容</span><span class="sxs-lookup"><span data-stu-id="0743a-124">-Context</span></span>
<span data-ttu-id="0743a-125">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="0743a-125">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="0743a-126">若要取得內容，請使用 [AzStorageCoNtext](./New-AzStorageContext.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0743a-126">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="0743a-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0743a-127">-DefaultProfile</span></span>
<span data-ttu-id="0743a-128">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0743a-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0743a-129">-原則</span><span class="sxs-lookup"><span data-stu-id="0743a-129">-Policy</span></span>
<span data-ttu-id="0743a-130">指定此 Cmdlet 取得的儲存訪問原則名稱。</span><span class="sxs-lookup"><span data-stu-id="0743a-130">Specifies the name of the stored access policy that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0743a-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0743a-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="0743a-132">指定要求中伺服器部分的超時時間長度。</span><span class="sxs-lookup"><span data-stu-id="0743a-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="0743a-133">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="0743a-133">-ShareName</span></span>
<span data-ttu-id="0743a-134">指定此 Cmdlet 取得其原則的儲存空間份額名稱。</span><span class="sxs-lookup"><span data-stu-id="0743a-134">Specifies the Storage share name for which this cmdlet gets policies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0743a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0743a-135">CommonParameters</span></span>
<span data-ttu-id="0743a-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0743a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0743a-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0743a-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0743a-138">輸入</span><span class="sxs-lookup"><span data-stu-id="0743a-138">INPUTS</span></span>

### <span data-ttu-id="0743a-139">System.object</span><span class="sxs-lookup"><span data-stu-id="0743a-139">System.String</span></span>

### <span data-ttu-id="0743a-140">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="0743a-140">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0743a-141">輸出</span><span class="sxs-lookup"><span data-stu-id="0743a-141">OUTPUTS</span></span>

### <span data-ttu-id="0743a-142">SharedAccessFilePolicy （即 Azure）</span><span class="sxs-lookup"><span data-stu-id="0743a-142">Microsoft.Azure.Storage.File.SharedAccessFilePolicy</span></span>

## <span data-ttu-id="0743a-143">筆記</span><span class="sxs-lookup"><span data-stu-id="0743a-143">NOTES</span></span>

## <span data-ttu-id="0743a-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="0743a-144">RELATED LINKS</span></span>

[<span data-ttu-id="0743a-145">新-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="0743a-145">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="0743a-146">新-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0743a-146">New-AzStorageShareStoredAccessPolicy</span></span>](./New-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="0743a-147">移除-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0743a-147">Remove-AzStorageShareStoredAccessPolicy</span></span>](./Remove-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="0743a-148">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0743a-148">Set-AzStorageShareStoredAccessPolicy</span></span>](./Set-AzStorageShareStoredAccessPolicy.md)
