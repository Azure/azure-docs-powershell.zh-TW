---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C324F28A-7215-4F10-A012-92B4F6544BC0
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 6e7230ad6cb2bd3f58ebd3328aa20fe3c1bf2bbc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915078"
---
# <span data-ttu-id="9f0f6-101">New-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9f0f6-101">New-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="9f0f6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9f0f6-102">SYNOPSIS</span></span>
<span data-ttu-id="9f0f6-103">建立 Azure 儲存容器的儲存存取策略。</span><span class="sxs-lookup"><span data-stu-id="9f0f6-103">Creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="9f0f6-104">語法</span><span class="sxs-lookup"><span data-stu-id="9f0f6-104">SYNTAX</span></span>

```
New-AzStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="9f0f6-105">描述</span><span class="sxs-lookup"><span data-stu-id="9f0f6-105">DESCRIPTION</span></span>
<span data-ttu-id="9f0f6-106">**New-AzStorageContainerStoredAccessPolicy** Cmdlet 會建立 Azure 儲存容器的儲存存取策略。</span><span class="sxs-lookup"><span data-stu-id="9f0f6-106">The **New-AzStorageContainerStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="9f0f6-107">例子</span><span class="sxs-lookup"><span data-stu-id="9f0f6-107">EXAMPLES</span></span>

### <span data-ttu-id="9f0f6-108">範例 1：在儲存容器內建立儲存的存取策略</span><span class="sxs-lookup"><span data-stu-id="9f0f6-108">Example 1: Create a stored access policy in a storage container</span></span>
```
PS C:\>New-AzStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy01"
```

<span data-ttu-id="9f0f6-109">此命令在名為 MyContainer 的儲存容器內建立一個名為 Policy01 的存取策略。</span><span class="sxs-lookup"><span data-stu-id="9f0f6-109">This command creates an access policy named Policy01 in the storage container named MyContainer.</span></span>

## <span data-ttu-id="9f0f6-110">參數</span><span class="sxs-lookup"><span data-stu-id="9f0f6-110">PARAMETERS</span></span>

### <span data-ttu-id="9f0f6-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9f0f6-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="9f0f6-112">指定一個服務要求用戶端的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="9f0f6-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="9f0f6-113">如果前一個通話在指定的時間間隔內失敗，此 Cmdlet 會重新重試要求。</span><span class="sxs-lookup"><span data-stu-id="9f0f6-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="9f0f6-114">如果此 Cmdlet 在間隔經過之前未收到成功回應，此 Cmdlet 會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="9f0f6-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="9f0f6-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="9f0f6-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="9f0f6-116">指定同時進行的最大網路通話數。</span><span class="sxs-lookup"><span data-stu-id="9f0f6-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="9f0f6-117">您可以使用此參數來限制並行，以節流本地 CPU 和頻寬使用量，方法為指定並行網路通話的數量上限。</span><span class="sxs-lookup"><span data-stu-id="9f0f6-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="9f0f6-118">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="9f0f6-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="9f0f6-119">此參數有助於減少低頻寬環境的網路連接問題，例如每秒 100 KB。</span><span class="sxs-lookup"><span data-stu-id="9f0f6-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="9f0f6-120">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="9f0f6-120">The default value is 10.</span></span>

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

### <span data-ttu-id="9f0f6-121">-Container</span><span class="sxs-lookup"><span data-stu-id="9f0f6-121">-Container</span></span>
<span data-ttu-id="9f0f6-122">指定 Azure 儲存容器名稱。</span><span class="sxs-lookup"><span data-stu-id="9f0f6-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="9f0f6-123">-內容</span><span class="sxs-lookup"><span data-stu-id="9f0f6-123">-Context</span></span>
<span data-ttu-id="9f0f6-124">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="9f0f6-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="9f0f6-125">若要取得儲存內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9f0f6-125">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="9f0f6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f0f6-126">-DefaultProfile</span></span>
<span data-ttu-id="9f0f6-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9f0f6-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f0f6-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="9f0f6-128">-ExpiryTime</span></span>
<span data-ttu-id="9f0f6-129">指定儲存的存取策略變成不正確時間。</span><span class="sxs-lookup"><span data-stu-id="9f0f6-129">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="9f0f6-130">-許可權</span><span class="sxs-lookup"><span data-stu-id="9f0f6-130">-Permission</span></span>
<span data-ttu-id="9f0f6-131">指定儲存存取策略中存取容器的許可權。</span><span class="sxs-lookup"><span data-stu-id="9f0f6-131">Specifies permissions in the stored access policy to access the container.</span></span>
<span data-ttu-id="9f0f6-132">請注意，這是一個字串，例如用於讀取 (寫入和 `rwd` 刪除) 。</span><span class="sxs-lookup"><span data-stu-id="9f0f6-132">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="9f0f6-133">-策略</span><span class="sxs-lookup"><span data-stu-id="9f0f6-133">-Policy</span></span>
<span data-ttu-id="9f0f6-134">指定儲存的存取策略，包括此 SAS 權杖的許可權。</span><span class="sxs-lookup"><span data-stu-id="9f0f6-134">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="9f0f6-135">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9f0f6-135">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="9f0f6-136">指定一個服務要求用戶端的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="9f0f6-136">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="9f0f6-137">如果前一個通話在指定的時間間隔內失敗，此 Cmdlet 會重新重試要求。</span><span class="sxs-lookup"><span data-stu-id="9f0f6-137">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="9f0f6-138">如果此 Cmdlet 在間隔經過之前未收到成功回應，此 Cmdlet 會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="9f0f6-138">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="9f0f6-139">-StartTime</span><span class="sxs-lookup"><span data-stu-id="9f0f6-139">-StartTime</span></span>
<span data-ttu-id="9f0f6-140">指定儲存的存取策略生效的時間。</span><span class="sxs-lookup"><span data-stu-id="9f0f6-140">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="9f0f6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f0f6-141">CommonParameters</span></span>
<span data-ttu-id="9f0f6-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9f0f6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f0f6-143">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="9f0f6-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f0f6-144">輸入</span><span class="sxs-lookup"><span data-stu-id="9f0f6-144">INPUTS</span></span>

### <span data-ttu-id="9f0f6-145">System.String</span><span class="sxs-lookup"><span data-stu-id="9f0f6-145">System.String</span></span>

### <span data-ttu-id="9f0f6-146">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="9f0f6-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9f0f6-147">輸出</span><span class="sxs-lookup"><span data-stu-id="9f0f6-147">OUTPUTS</span></span>

### <span data-ttu-id="9f0f6-148">System.String</span><span class="sxs-lookup"><span data-stu-id="9f0f6-148">System.String</span></span>

## <span data-ttu-id="9f0f6-149">筆記</span><span class="sxs-lookup"><span data-stu-id="9f0f6-149">NOTES</span></span>

## <span data-ttu-id="9f0f6-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="9f0f6-150">RELATED LINKS</span></span>

[<span data-ttu-id="9f0f6-151">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9f0f6-151">Get-AzStorageContainerStoredAccessPolicy</span></span>](./Get-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="9f0f6-152">New-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="9f0f6-152">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="9f0f6-153">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9f0f6-153">Remove-AzStorageContainerStoredAccessPolicy</span></span>](./Remove-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="9f0f6-154">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9f0f6-154">Set-AzStorageContainerStoredAccessPolicy</span></span>](./Set-AzStorageContainerStoredAccessPolicy.md)


