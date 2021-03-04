---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 37E76360-B683-407C-9AEF-7138374562D8
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 3604d6e8d3c9394a53c59e220bdef31662a75f88
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915038"
---
# <span data-ttu-id="2d4a3-101">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2d4a3-101">New-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="2d4a3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2d4a3-102">SYNOPSIS</span></span>
<span data-ttu-id="2d4a3-103">在儲存空間共用上建立儲存的存取策略。</span><span class="sxs-lookup"><span data-stu-id="2d4a3-103">Creates a stored access policy on a Storage share.</span></span>

## <span data-ttu-id="2d4a3-104">語法</span><span class="sxs-lookup"><span data-stu-id="2d4a3-104">SYNTAX</span></span>

```
New-AzStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="2d4a3-105">描述</span><span class="sxs-lookup"><span data-stu-id="2d4a3-105">DESCRIPTION</span></span>
<span data-ttu-id="2d4a3-106">**New-AzStorageSharedAccessPolicy** Cmdlet 會建立 Azure 儲存空間共用上的儲存存取策略。</span><span class="sxs-lookup"><span data-stu-id="2d4a3-106">The **New-AzStorageShareStoredAccessPolicy** cmdlet creates a stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="2d4a3-107">例子</span><span class="sxs-lookup"><span data-stu-id="2d4a3-107">EXAMPLES</span></span>

### <span data-ttu-id="2d4a3-108">範例 1：在共用中建立儲存的存取策略</span><span class="sxs-lookup"><span data-stu-id="2d4a3-108">Example 1: Create a stored access policy in a share</span></span>
```
PS C:\>New-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="2d4a3-109">此命令會建立具有共用完整許可權的儲存存取策略。</span><span class="sxs-lookup"><span data-stu-id="2d4a3-109">This command creates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="2d4a3-110">參數</span><span class="sxs-lookup"><span data-stu-id="2d4a3-110">PARAMETERS</span></span>

### <span data-ttu-id="2d4a3-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2d4a3-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="2d4a3-112">指定一個服務要求用戶端的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="2d4a3-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="2d4a3-113">如果前一個通話在指定的時間間隔內失敗，此 Cmdlet 會重新重試要求。</span><span class="sxs-lookup"><span data-stu-id="2d4a3-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="2d4a3-114">如果此 Cmdlet 在間隔經過之前未收到成功回應，此 Cmdlet 會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="2d4a3-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="2d4a3-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="2d4a3-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="2d4a3-116">指定同時進行的最大網路通話數。</span><span class="sxs-lookup"><span data-stu-id="2d4a3-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="2d4a3-117">您可以使用此參數來限制並行，以節流本地 CPU 和頻寬使用量，方法為指定並行網路通話的數量上限。</span><span class="sxs-lookup"><span data-stu-id="2d4a3-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="2d4a3-118">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="2d4a3-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="2d4a3-119">此參數有助於減少低頻寬環境的網路連接問題，例如每秒 100 KB。</span><span class="sxs-lookup"><span data-stu-id="2d4a3-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="2d4a3-120">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="2d4a3-120">The default value is 10.</span></span>

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

### <span data-ttu-id="2d4a3-121">-內容</span><span class="sxs-lookup"><span data-stu-id="2d4a3-121">-Context</span></span>
<span data-ttu-id="2d4a3-122">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="2d4a3-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="2d4a3-123">若要取得儲存內容，請使用 [New-AzStorageCoNtext](./New-AzStorageContext.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2d4a3-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="2d4a3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d4a3-124">-DefaultProfile</span></span>
<span data-ttu-id="2d4a3-125">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2d4a3-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d4a3-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="2d4a3-126">-ExpiryTime</span></span>
<span data-ttu-id="2d4a3-127">指定儲存的存取策略變成不正確時間。</span><span class="sxs-lookup"><span data-stu-id="2d4a3-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d4a3-128">-許可權</span><span class="sxs-lookup"><span data-stu-id="2d4a3-128">-Permission</span></span>
<span data-ttu-id="2d4a3-129">指定儲存存取策略中存取儲存空間共用或其下檔案的許可權。</span><span class="sxs-lookup"><span data-stu-id="2d4a3-129">Specifies permissions in the stored access policy to access the Storage share or files under it.</span></span>
<span data-ttu-id="2d4a3-130">請注意，這是一個字串，例如用於讀取 (寫入和 `rwd` 刪除) 。</span><span class="sxs-lookup"><span data-stu-id="2d4a3-130">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d4a3-131">-策略</span><span class="sxs-lookup"><span data-stu-id="2d4a3-131">-Policy</span></span>
<span data-ttu-id="2d4a3-132">指定儲存存取策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="2d4a3-132">Specifies a name for the stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d4a3-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2d4a3-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="2d4a3-134">指定要求的伺服器部分之時間長度。</span><span class="sxs-lookup"><span data-stu-id="2d4a3-134">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="2d4a3-135">-ShareName</span><span class="sxs-lookup"><span data-stu-id="2d4a3-135">-ShareName</span></span>
<span data-ttu-id="2d4a3-136">指定儲存空間共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="2d4a3-136">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="2d4a3-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="2d4a3-137">-StartTime</span></span>
<span data-ttu-id="2d4a3-138">指定儲存的存取策略生效的時間。</span><span class="sxs-lookup"><span data-stu-id="2d4a3-138">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d4a3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d4a3-139">CommonParameters</span></span>
<span data-ttu-id="2d4a3-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2d4a3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d4a3-141">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="2d4a3-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d4a3-142">輸入</span><span class="sxs-lookup"><span data-stu-id="2d4a3-142">INPUTS</span></span>

### <span data-ttu-id="2d4a3-143">System.String</span><span class="sxs-lookup"><span data-stu-id="2d4a3-143">System.String</span></span>

### <span data-ttu-id="2d4a3-144">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="2d4a3-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2d4a3-145">輸出</span><span class="sxs-lookup"><span data-stu-id="2d4a3-145">OUTPUTS</span></span>

### <span data-ttu-id="2d4a3-146">System.String</span><span class="sxs-lookup"><span data-stu-id="2d4a3-146">System.String</span></span>

## <span data-ttu-id="2d4a3-147">筆記</span><span class="sxs-lookup"><span data-stu-id="2d4a3-147">NOTES</span></span>

## <span data-ttu-id="2d4a3-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="2d4a3-148">RELATED LINKS</span></span>

[<span data-ttu-id="2d4a3-149">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2d4a3-149">Get-AzStorageShareStoredAccessPolicy</span></span>](./Get-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="2d4a3-150">New-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="2d4a3-150">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="2d4a3-151">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2d4a3-151">Remove-AzStorageShareStoredAccessPolicy</span></span>](./Remove-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="2d4a3-152">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2d4a3-152">Set-AzStorageShareStoredAccessPolicy</span></span>](./Set-AzStorageShareStoredAccessPolicy.md)
