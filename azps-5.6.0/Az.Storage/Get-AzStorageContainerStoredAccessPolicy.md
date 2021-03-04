---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 10D5B7E0-242B-4DC0-A527-8F6388E72E0A
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 7d3d16632e2afb503bf659058643244fd8578d44
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903942"
---
# <span data-ttu-id="768ba-101">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="768ba-101">Get-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="768ba-102">簡介</span><span class="sxs-lookup"><span data-stu-id="768ba-102">SYNOPSIS</span></span>
<span data-ttu-id="768ba-103">取得 Azure 儲存容器的儲存存取策略或策略。</span><span class="sxs-lookup"><span data-stu-id="768ba-103">Gets the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="768ba-104">語法</span><span class="sxs-lookup"><span data-stu-id="768ba-104">SYNTAX</span></span>

```
Get-AzStorageContainerStoredAccessPolicy [-Container] <String> [[-Policy] <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="768ba-105">描述</span><span class="sxs-lookup"><span data-stu-id="768ba-105">DESCRIPTION</span></span>
<span data-ttu-id="768ba-106">**Get-AzStorageContainerStoredAccessPolicy** Cmdlet 會列出 Azure 儲存容器的儲存存取策略或策略。</span><span class="sxs-lookup"><span data-stu-id="768ba-106">The **Get-AzStorageContainerStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="768ba-107">例子</span><span class="sxs-lookup"><span data-stu-id="768ba-107">EXAMPLES</span></span>

### <span data-ttu-id="768ba-108">範例 1：在儲存容器內取得儲存的存取策略</span><span class="sxs-lookup"><span data-stu-id="768ba-108">Example 1: Get a stored access policy in a storage container</span></span>
```
PS C:\>Get-AzStorageContainerStoredAccessPolicy -Container "Container07" -Policy "Policy22"
```

<span data-ttu-id="768ba-109">此命令在名為 Container07 的儲存容器內取得名為 Policy22 的存取策略。</span><span class="sxs-lookup"><span data-stu-id="768ba-109">This command gets the access policy named Policy22 in the storage container named Container07.</span></span>

### <span data-ttu-id="768ba-110">範例 2：取得儲存容器內的所有儲存存取策略</span><span class="sxs-lookup"><span data-stu-id="768ba-110">Example 2: Get all the stored access policies in a storage container</span></span>
```
PS C:\>Get-AzStorageContainerStoredAccessPolicy -Container "Container07"
```

<span data-ttu-id="768ba-111">此命令會取得名為 Container07 的儲存容器內的所有存取策略。</span><span class="sxs-lookup"><span data-stu-id="768ba-111">This command gets all access policies in the storage container named Container07.</span></span>

## <span data-ttu-id="768ba-112">參數</span><span class="sxs-lookup"><span data-stu-id="768ba-112">PARAMETERS</span></span>

### <span data-ttu-id="768ba-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="768ba-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="768ba-114">指定一個服務要求用戶端的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="768ba-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="768ba-115">如果前一個通話在指定的時間間隔內失敗，此 Cmdlet 會重新重試要求。</span><span class="sxs-lookup"><span data-stu-id="768ba-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="768ba-116">如果此 Cmdlet 在間隔經過之前未收到成功回應，此 Cmdlet 會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="768ba-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="768ba-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="768ba-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="768ba-118">指定同時進行的最大網路通話數。</span><span class="sxs-lookup"><span data-stu-id="768ba-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="768ba-119">您可以使用此參數來限制並行，以節流本地 CPU 和頻寬使用量，方法為指定並行網路通話的數量上限。</span><span class="sxs-lookup"><span data-stu-id="768ba-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="768ba-120">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="768ba-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="768ba-121">此參數有助於減少低頻寬環境的網路連接問題，例如每秒 100 KB。</span><span class="sxs-lookup"><span data-stu-id="768ba-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="768ba-122">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="768ba-122">The default value is 10.</span></span>

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

### <span data-ttu-id="768ba-123">-Container</span><span class="sxs-lookup"><span data-stu-id="768ba-123">-Container</span></span>
<span data-ttu-id="768ba-124">指定 Azure 儲存容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="768ba-124">Specifies the name of your Azure storage container.</span></span>

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

### <span data-ttu-id="768ba-125">-內容</span><span class="sxs-lookup"><span data-stu-id="768ba-125">-Context</span></span>
<span data-ttu-id="768ba-126">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="768ba-126">Specifies the Azure storage context.</span></span>

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

### <span data-ttu-id="768ba-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="768ba-127">-DefaultProfile</span></span>
<span data-ttu-id="768ba-128">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="768ba-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="768ba-129">-策略</span><span class="sxs-lookup"><span data-stu-id="768ba-129">-Policy</span></span>
<span data-ttu-id="768ba-130">指定 Azure 儲存的存取策略。</span><span class="sxs-lookup"><span data-stu-id="768ba-130">Specifies the Azure stored access policy.</span></span>

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

### <span data-ttu-id="768ba-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="768ba-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="768ba-132">指定服務端要求的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="768ba-132">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="768ba-133">如果指定的時間間隔在服務處理要求之前已經過，儲存服務會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="768ba-133">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="768ba-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="768ba-134">CommonParameters</span></span>
<span data-ttu-id="768ba-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="768ba-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="768ba-136">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="768ba-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="768ba-137">輸入</span><span class="sxs-lookup"><span data-stu-id="768ba-137">INPUTS</span></span>

### <span data-ttu-id="768ba-138">System.String</span><span class="sxs-lookup"><span data-stu-id="768ba-138">System.String</span></span>

### <span data-ttu-id="768ba-139">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="768ba-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="768ba-140">輸出</span><span class="sxs-lookup"><span data-stu-id="768ba-140">OUTPUTS</span></span>

### <span data-ttu-id="768ba-141">Microsoft.Azure.storage.Blob.SharedAccessBlobPolicy</span><span class="sxs-lookup"><span data-stu-id="768ba-141">Microsoft.Azure.Storage.Blob.SharedAccessBlobPolicy</span></span>

## <span data-ttu-id="768ba-142">筆記</span><span class="sxs-lookup"><span data-stu-id="768ba-142">NOTES</span></span>

## <span data-ttu-id="768ba-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="768ba-143">RELATED LINKS</span></span>

[<span data-ttu-id="768ba-144">New-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="768ba-144">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="768ba-145">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="768ba-145">Remove-AzStorageContainerStoredAccessPolicy</span></span>](./Remove-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="768ba-146">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="768ba-146">Set-AzStorageContainerStoredAccessPolicy</span></span>](./Set-AzStorageContainerStoredAccessPolicy.md)


