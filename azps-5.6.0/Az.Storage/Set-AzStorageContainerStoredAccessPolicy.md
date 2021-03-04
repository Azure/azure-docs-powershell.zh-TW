---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 730ECC60-72DE-46DA-A177-D5749F540710
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: e195b4844b35e5ab10d41ed505d619edf3f13515
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915017"
---
# <span data-ttu-id="25320-101">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="25320-101">Set-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="25320-102">簡介</span><span class="sxs-lookup"><span data-stu-id="25320-102">SYNOPSIS</span></span>
<span data-ttu-id="25320-103">設定 Azure 儲存容器的儲存存取策略。</span><span class="sxs-lookup"><span data-stu-id="25320-103">Sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="25320-104">語法</span><span class="sxs-lookup"><span data-stu-id="25320-104">SYNTAX</span></span>

```
Set-AzStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="25320-105">描述</span><span class="sxs-lookup"><span data-stu-id="25320-105">DESCRIPTION</span></span>
<span data-ttu-id="25320-106">**Set-AzStorageContainerStoredAccessPolicy** Cmdlet 會設定 Azure 儲存容器的儲存存取策略。</span><span class="sxs-lookup"><span data-stu-id="25320-106">The **Set-AzStorageContainerStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="25320-107">例子</span><span class="sxs-lookup"><span data-stu-id="25320-107">EXAMPLES</span></span>

### <span data-ttu-id="25320-108">範例 1：在具有完整許可權的儲存容器內設定儲存存取策略</span><span class="sxs-lookup"><span data-stu-id="25320-108">Example 1: Set a stored access policy in a storage container with full permission</span></span>
```
PS C:\>Set-AzStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy06" -Permission rwdl
```

<span data-ttu-id="25320-109">此命令會針對名為 MyContainer 的儲存容器設定名為 Policy06 的存取策略。</span><span class="sxs-lookup"><span data-stu-id="25320-109">This command sets an access policy named Policy06 for storage container named MyContainer.</span></span>

## <span data-ttu-id="25320-110">參數</span><span class="sxs-lookup"><span data-stu-id="25320-110">PARAMETERS</span></span>

### <span data-ttu-id="25320-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="25320-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="25320-112">指定一個服務要求用戶端的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="25320-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="25320-113">如果前一個通話在指定的時間間隔內失敗，此 Cmdlet 會重新重試要求。</span><span class="sxs-lookup"><span data-stu-id="25320-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="25320-114">如果此 Cmdlet 在間隔經過之前未收到成功回應，此 Cmdlet 會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="25320-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="25320-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="25320-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="25320-116">指定同時進行的最大網路通話數。</span><span class="sxs-lookup"><span data-stu-id="25320-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="25320-117">您可以使用此參數來限制並行，以節流本地 CPU 和頻寬使用量，方法為指定並行網路通話的數量上限。</span><span class="sxs-lookup"><span data-stu-id="25320-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="25320-118">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="25320-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="25320-119">此參數有助於減少低頻寬環境的網路連接問題，例如每秒 100 KB。</span><span class="sxs-lookup"><span data-stu-id="25320-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="25320-120">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="25320-120">The default value is 10.</span></span>

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

### <span data-ttu-id="25320-121">-Container</span><span class="sxs-lookup"><span data-stu-id="25320-121">-Container</span></span>
<span data-ttu-id="25320-122">指定 Azure 儲存容器名稱。</span><span class="sxs-lookup"><span data-stu-id="25320-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="25320-123">-內容</span><span class="sxs-lookup"><span data-stu-id="25320-123">-Context</span></span>
<span data-ttu-id="25320-124">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="25320-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="25320-125">若要取得儲存內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="25320-125">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="25320-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25320-126">-DefaultProfile</span></span>
<span data-ttu-id="25320-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="25320-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25320-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="25320-128">-ExpiryTime</span></span>
<span data-ttu-id="25320-129">指定儲存的存取策略變成不正確時間。</span><span class="sxs-lookup"><span data-stu-id="25320-129">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="25320-130">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="25320-130">-NoExpiryTime</span></span>
<span data-ttu-id="25320-131">表示存取策略沒有到期日。</span><span class="sxs-lookup"><span data-stu-id="25320-131">Indicates that the access policy has no expiration date.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25320-132">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="25320-132">-NoStartTime</span></span>
<span data-ttu-id="25320-133">將開始時間設定為$Null。</span><span class="sxs-lookup"><span data-stu-id="25320-133">Sets the start time to be $Null.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25320-134">-許可權</span><span class="sxs-lookup"><span data-stu-id="25320-134">-Permission</span></span>
<span data-ttu-id="25320-135">指定儲存存取策略中存取儲存容器的許可權。</span><span class="sxs-lookup"><span data-stu-id="25320-135">Specifies permissions in the stored access policy to access the storage container.</span></span>
<span data-ttu-id="25320-136">請注意，這是一個字串，例如用於讀取 (寫入和 `rwd` 刪除) 。</span><span class="sxs-lookup"><span data-stu-id="25320-136">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="25320-137">-策略</span><span class="sxs-lookup"><span data-stu-id="25320-137">-Policy</span></span>
<span data-ttu-id="25320-138">指定儲存存取策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="25320-138">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="25320-139">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="25320-139">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="25320-140">指定一個服務要求用戶端的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="25320-140">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="25320-141">如果前一個通話在指定的時間間隔內失敗，此 Cmdlet 會重新重試要求。</span><span class="sxs-lookup"><span data-stu-id="25320-141">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="25320-142">如果此 Cmdlet 在間隔經過之前未收到成功回應，此 Cmdlet 會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="25320-142">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="25320-143">-StartTime</span><span class="sxs-lookup"><span data-stu-id="25320-143">-StartTime</span></span>
<span data-ttu-id="25320-144">指定儲存的存取策略生效的時間。</span><span class="sxs-lookup"><span data-stu-id="25320-144">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="25320-145">-確認</span><span class="sxs-lookup"><span data-stu-id="25320-145">-Confirm</span></span>
<span data-ttu-id="25320-146">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="25320-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25320-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25320-147">-WhatIf</span></span>
<span data-ttu-id="25320-148">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="25320-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="25320-149">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="25320-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25320-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25320-150">CommonParameters</span></span>
<span data-ttu-id="25320-151">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="25320-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25320-152">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="25320-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25320-153">輸入</span><span class="sxs-lookup"><span data-stu-id="25320-153">INPUTS</span></span>

### <span data-ttu-id="25320-154">System.String</span><span class="sxs-lookup"><span data-stu-id="25320-154">System.String</span></span>

### <span data-ttu-id="25320-155">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="25320-155">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="25320-156">輸出</span><span class="sxs-lookup"><span data-stu-id="25320-156">OUTPUTS</span></span>

### <span data-ttu-id="25320-157">System.String</span><span class="sxs-lookup"><span data-stu-id="25320-157">System.String</span></span>

## <span data-ttu-id="25320-158">筆記</span><span class="sxs-lookup"><span data-stu-id="25320-158">NOTES</span></span>

## <span data-ttu-id="25320-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="25320-159">RELATED LINKS</span></span>

[<span data-ttu-id="25320-160">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="25320-160">Get-AzStorageContainerStoredAccessPolicy</span></span>](./Get-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="25320-161">New-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="25320-161">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="25320-162">New-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="25320-162">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="25320-163">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="25320-163">Remove-AzStorageContainerStoredAccessPolicy</span></span>](./Remove-AzStorageContainerStoredAccessPolicy.md)
