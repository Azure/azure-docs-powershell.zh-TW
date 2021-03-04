---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C21CC2FA-017E-492E-96E7-B37829917FAF
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: b48c56df294e12e9c8f84b45b3bb991406338b52
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904798"
---
# <span data-ttu-id="883a1-101">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="883a1-101">Set-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="883a1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="883a1-102">SYNOPSIS</span></span>
<span data-ttu-id="883a1-103">更新儲存空間共用上的儲存存取策略。</span><span class="sxs-lookup"><span data-stu-id="883a1-103">Updates a stored access policy on a Storage share.</span></span>

## <span data-ttu-id="883a1-104">語法</span><span class="sxs-lookup"><span data-stu-id="883a1-104">SYNTAX</span></span>

```
Set-AzStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="883a1-105">描述</span><span class="sxs-lookup"><span data-stu-id="883a1-105">DESCRIPTION</span></span>
<span data-ttu-id="883a1-106">**Set-AzStorageShareStoredAccessPolicy** Cmdlet 會更新 Azure 儲存空間共用上儲存的存取策略。</span><span class="sxs-lookup"><span data-stu-id="883a1-106">The **Set-AzStorageShareStoredAccessPolicy** cmdlet updates stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="883a1-107">例子</span><span class="sxs-lookup"><span data-stu-id="883a1-107">EXAMPLES</span></span>

### <span data-ttu-id="883a1-108">範例 1：更新儲存空間共用中的儲存存取策略</span><span class="sxs-lookup"><span data-stu-id="883a1-108">Example 1: Update a stored access policy in Storage share</span></span>
```
PS C:\>Set-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="883a1-109">此命令會更新具有共用完整許可權的已儲存存取策略。</span><span class="sxs-lookup"><span data-stu-id="883a1-109">This command updates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="883a1-110">參數</span><span class="sxs-lookup"><span data-stu-id="883a1-110">PARAMETERS</span></span>

### <span data-ttu-id="883a1-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="883a1-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="883a1-112">指定一個服務要求用戶端的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="883a1-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="883a1-113">如果前一個通話在指定的時間間隔內失敗，此 Cmdlet 會重新重試要求。</span><span class="sxs-lookup"><span data-stu-id="883a1-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="883a1-114">如果此 Cmdlet 在間隔經過之前未收到成功回應，此 Cmdlet 會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="883a1-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="883a1-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="883a1-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="883a1-116">指定同時進行的最大網路通話數。</span><span class="sxs-lookup"><span data-stu-id="883a1-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="883a1-117">您可以使用此參數來限制並行，以節流本地 CPU 和頻寬使用量，方法為指定並行網路通話的數量上限。</span><span class="sxs-lookup"><span data-stu-id="883a1-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="883a1-118">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="883a1-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="883a1-119">此參數有助於減少低頻寬環境的網路連接問題，例如每秒 100 KB。</span><span class="sxs-lookup"><span data-stu-id="883a1-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="883a1-120">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="883a1-120">The default value is 10.</span></span>

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

### <span data-ttu-id="883a1-121">-內容</span><span class="sxs-lookup"><span data-stu-id="883a1-121">-Context</span></span>
<span data-ttu-id="883a1-122">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="883a1-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="883a1-123">若要取得儲存內容，請使用 [New-AzStorageCoNtext](./New-AzStorageContext.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="883a1-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="883a1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="883a1-124">-DefaultProfile</span></span>
<span data-ttu-id="883a1-125">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="883a1-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="883a1-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="883a1-126">-ExpiryTime</span></span>
<span data-ttu-id="883a1-127">指定儲存的存取策略變成不正確時間。</span><span class="sxs-lookup"><span data-stu-id="883a1-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="883a1-128">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="883a1-128">-NoExpiryTime</span></span>
<span data-ttu-id="883a1-129">表示此 Cmdlet 會清除儲存存取策略中的 **ExpiryTime** 屬性。</span><span class="sxs-lookup"><span data-stu-id="883a1-129">Indicates that this cmdlet clears the **ExpiryTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="883a1-130">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="883a1-130">-NoStartTime</span></span>
<span data-ttu-id="883a1-131">表示此 Cmdlet 會清除儲存存取策略中的 **StartTime** 屬性。</span><span class="sxs-lookup"><span data-stu-id="883a1-131">Indicates that this cmdlet clears the **StartTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="883a1-132">-許可權</span><span class="sxs-lookup"><span data-stu-id="883a1-132">-Permission</span></span>
<span data-ttu-id="883a1-133">指定儲存存取策略中存取其下共用或檔案的許可權。</span><span class="sxs-lookup"><span data-stu-id="883a1-133">Specifies permissions in the stored access policy to access the share or files under it.</span></span>
<span data-ttu-id="883a1-134">請注意，這是一個字串，例如用於讀取 (寫入和 `rwd` 刪除) 。</span><span class="sxs-lookup"><span data-stu-id="883a1-134">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="883a1-135">-策略</span><span class="sxs-lookup"><span data-stu-id="883a1-135">-Policy</span></span>
<span data-ttu-id="883a1-136">指定儲存存取策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="883a1-136">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="883a1-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="883a1-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="883a1-138">指定要求的伺服器部分之時間長度。</span><span class="sxs-lookup"><span data-stu-id="883a1-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="883a1-139">-ShareName</span><span class="sxs-lookup"><span data-stu-id="883a1-139">-ShareName</span></span>
<span data-ttu-id="883a1-140">指定儲存空間共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="883a1-140">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="883a1-141">-StartTime</span><span class="sxs-lookup"><span data-stu-id="883a1-141">-StartTime</span></span>
<span data-ttu-id="883a1-142">指定儲存的存取策略生效的時間。</span><span class="sxs-lookup"><span data-stu-id="883a1-142">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="883a1-143">-確認</span><span class="sxs-lookup"><span data-stu-id="883a1-143">-Confirm</span></span>
<span data-ttu-id="883a1-144">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="883a1-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="883a1-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="883a1-145">-WhatIf</span></span>
<span data-ttu-id="883a1-146">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="883a1-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="883a1-147">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="883a1-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="883a1-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="883a1-148">CommonParameters</span></span>
<span data-ttu-id="883a1-149">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="883a1-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="883a1-150">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="883a1-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="883a1-151">輸入</span><span class="sxs-lookup"><span data-stu-id="883a1-151">INPUTS</span></span>

### <span data-ttu-id="883a1-152">System.String</span><span class="sxs-lookup"><span data-stu-id="883a1-152">System.String</span></span>

### <span data-ttu-id="883a1-153">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="883a1-153">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="883a1-154">輸出</span><span class="sxs-lookup"><span data-stu-id="883a1-154">OUTPUTS</span></span>

### <span data-ttu-id="883a1-155">System.String</span><span class="sxs-lookup"><span data-stu-id="883a1-155">System.String</span></span>

## <span data-ttu-id="883a1-156">筆記</span><span class="sxs-lookup"><span data-stu-id="883a1-156">NOTES</span></span>

## <span data-ttu-id="883a1-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="883a1-157">RELATED LINKS</span></span>

[<span data-ttu-id="883a1-158">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="883a1-158">Get-AzStorageShareStoredAccessPolicy</span></span>](./Get-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="883a1-159">New-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="883a1-159">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="883a1-160">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="883a1-160">New-AzStorageShareStoredAccessPolicy</span></span>](./New-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="883a1-161">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="883a1-161">Remove-AzStorageShareStoredAccessPolicy</span></span>](./Remove-AzStorageShareStoredAccessPolicy.md)
