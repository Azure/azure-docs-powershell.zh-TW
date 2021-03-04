---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 73BB521B-20F2-4F2B-AA88-2B128F36A9EF
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 1e63be8e7db3b659b1f3d808477bdfef715e482b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916695"
---
# <span data-ttu-id="c6be1-101">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c6be1-101">Get-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="c6be1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c6be1-102">SYNOPSIS</span></span>
<span data-ttu-id="c6be1-103">取得儲存空間共用儲存的存取策略。</span><span class="sxs-lookup"><span data-stu-id="c6be1-103">Gets stored access policies for a Storage share.</span></span>

## <span data-ttu-id="c6be1-104">語法</span><span class="sxs-lookup"><span data-stu-id="c6be1-104">SYNTAX</span></span>

```
Get-AzStorageShareStoredAccessPolicy [-ShareName] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="c6be1-105">描述</span><span class="sxs-lookup"><span data-stu-id="c6be1-105">DESCRIPTION</span></span>
<span data-ttu-id="c6be1-106">**Get-AzStorageSharedAccessPolicy** Cmdlet 會取得 Azure 儲存空間共用的儲存存取策略。</span><span class="sxs-lookup"><span data-stu-id="c6be1-106">The **Get-AzStorageShareStoredAccessPolicy** cmdlet gets stored access policies for an Azure Storage share.</span></span>
<span data-ttu-id="c6be1-107">若要取得特定規則，請以名稱指定。</span><span class="sxs-lookup"><span data-stu-id="c6be1-107">To get a particular policy, specify it by name.</span></span>

## <span data-ttu-id="c6be1-108">例子</span><span class="sxs-lookup"><span data-stu-id="c6be1-108">EXAMPLES</span></span>

### <span data-ttu-id="c6be1-109">範例 1：在共用中取得儲存的存取策略</span><span class="sxs-lookup"><span data-stu-id="c6be1-109">Example 1: Get a stored access policy in a share</span></span>
```
PS C:\>Get-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="c6be1-110">此命令會取得 ContosoShare 中名為 GeneralPolicy 的已儲存存取策略。</span><span class="sxs-lookup"><span data-stu-id="c6be1-110">This command gets a stored access policy named GeneralPolicy in ContosoShare.</span></span>

### <span data-ttu-id="c6be1-111">範例 2：取得共用中所有儲存的存取策略</span><span class="sxs-lookup"><span data-stu-id="c6be1-111">Example 2: Get all the stored access policies in share</span></span>
```
PS C:\>Get-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare"
```

<span data-ttu-id="c6be1-112">此命令會取得 ContosoShare 中所有儲存的存取策略。</span><span class="sxs-lookup"><span data-stu-id="c6be1-112">This command gets all stored access policies in ContosoShare.</span></span>

## <span data-ttu-id="c6be1-113">參數</span><span class="sxs-lookup"><span data-stu-id="c6be1-113">PARAMETERS</span></span>

### <span data-ttu-id="c6be1-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c6be1-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c6be1-115">指定一個服務要求用戶端的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="c6be1-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c6be1-116">如果前一個通話在指定的時間間隔內失敗，此 Cmdlet 會重新重試要求。</span><span class="sxs-lookup"><span data-stu-id="c6be1-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c6be1-117">如果此 Cmdlet 在間隔經過之前未收到成功回應，此 Cmdlet 會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="c6be1-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c6be1-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c6be1-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c6be1-119">指定同時進行的最大網路通話數。</span><span class="sxs-lookup"><span data-stu-id="c6be1-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="c6be1-120">您可以使用此參數來限制並行，以節流本地 CPU 和頻寬使用量，方法為指定並行網路通話的數量上限。</span><span class="sxs-lookup"><span data-stu-id="c6be1-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="c6be1-121">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="c6be1-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="c6be1-122">此參數有助於減少低頻寬環境的網路連接問題，例如每秒 100 KB。</span><span class="sxs-lookup"><span data-stu-id="c6be1-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="c6be1-123">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="c6be1-123">The default value is 10.</span></span>

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

### <span data-ttu-id="c6be1-124">-內容</span><span class="sxs-lookup"><span data-stu-id="c6be1-124">-Context</span></span>
<span data-ttu-id="c6be1-125">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="c6be1-125">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="c6be1-126">若要取得內容，請使用 [New-AzStorageCoNtext](./New-AzStorageContext.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c6be1-126">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="c6be1-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6be1-127">-DefaultProfile</span></span>
<span data-ttu-id="c6be1-128">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c6be1-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6be1-129">-策略</span><span class="sxs-lookup"><span data-stu-id="c6be1-129">-Policy</span></span>
<span data-ttu-id="c6be1-130">指定此 Cmdlet 取得之已儲存存取策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="c6be1-130">Specifies the name of the stored access policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c6be1-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c6be1-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c6be1-132">指定要求的伺服器部分之時間長度。</span><span class="sxs-lookup"><span data-stu-id="c6be1-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="c6be1-133">-ShareName</span><span class="sxs-lookup"><span data-stu-id="c6be1-133">-ShareName</span></span>
<span data-ttu-id="c6be1-134">指定此 Cmdlet 會獲得該 Cmdlet 之策略的儲存空間共用名稱稱。</span><span class="sxs-lookup"><span data-stu-id="c6be1-134">Specifies the Storage share name for which this cmdlet gets policies.</span></span>

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

### <span data-ttu-id="c6be1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6be1-135">CommonParameters</span></span>
<span data-ttu-id="c6be1-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c6be1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6be1-137">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="c6be1-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6be1-138">輸入</span><span class="sxs-lookup"><span data-stu-id="c6be1-138">INPUTS</span></span>

### <span data-ttu-id="c6be1-139">System.String</span><span class="sxs-lookup"><span data-stu-id="c6be1-139">System.String</span></span>

### <span data-ttu-id="c6be1-140">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="c6be1-140">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c6be1-141">輸出</span><span class="sxs-lookup"><span data-stu-id="c6be1-141">OUTPUTS</span></span>

### <span data-ttu-id="c6be1-142">Microsoft.Azure.storage.File.SharedAccessFilePolicy</span><span class="sxs-lookup"><span data-stu-id="c6be1-142">Microsoft.Azure.Storage.File.SharedAccessFilePolicy</span></span>

## <span data-ttu-id="c6be1-143">筆記</span><span class="sxs-lookup"><span data-stu-id="c6be1-143">NOTES</span></span>

## <span data-ttu-id="c6be1-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="c6be1-144">RELATED LINKS</span></span>

[<span data-ttu-id="c6be1-145">New-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="c6be1-145">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="c6be1-146">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c6be1-146">New-AzStorageShareStoredAccessPolicy</span></span>](./New-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="c6be1-147">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c6be1-147">Remove-AzStorageShareStoredAccessPolicy</span></span>](./Remove-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="c6be1-148">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c6be1-148">Set-AzStorageShareStoredAccessPolicy</span></span>](./Set-AzStorageShareStoredAccessPolicy.md)
