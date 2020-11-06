---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C21CC2FA-017E-492E-96E7-B37829917FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: b7d10ba1418ee7dd47a5dfa5256d0fecbc2e46ad
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93611777"
---
# <span data-ttu-id="ce350-101">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ce350-101">Set-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="ce350-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ce350-102">SYNOPSIS</span></span>
<span data-ttu-id="ce350-103">更新儲存空間共用上的儲存存取原則。</span><span class="sxs-lookup"><span data-stu-id="ce350-103">Updates a stored access policy on a Storage share.</span></span>

## <span data-ttu-id="ce350-104">句法</span><span class="sxs-lookup"><span data-stu-id="ce350-104">SYNTAX</span></span>

```
Set-AzStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ce350-105">說明</span><span class="sxs-lookup"><span data-stu-id="ce350-105">DESCRIPTION</span></span>
<span data-ttu-id="ce350-106">**AzStorageShareStoredAccessPolicy** Cmdlet 會更新 Azure 儲存空間共用上儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="ce350-106">The **Set-AzStorageShareStoredAccessPolicy** cmdlet updates stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="ce350-107">示例</span><span class="sxs-lookup"><span data-stu-id="ce350-107">EXAMPLES</span></span>

### <span data-ttu-id="ce350-108">範例1：在儲存空間共用中更新已儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="ce350-108">Example 1: Update a stored access policy in Storage share</span></span>
```
PS C:\>Set-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="ce350-109">這個命令會更新在共用中擁有完整許可權的儲存存取原則。</span><span class="sxs-lookup"><span data-stu-id="ce350-109">This command updates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="ce350-110">參數</span><span class="sxs-lookup"><span data-stu-id="ce350-110">PARAMETERS</span></span>

### <span data-ttu-id="ce350-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ce350-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ce350-112">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="ce350-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ce350-113">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="ce350-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ce350-114">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="ce350-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ce350-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ce350-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ce350-116">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="ce350-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ce350-117">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="ce350-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ce350-118">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="ce350-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ce350-119">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="ce350-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ce350-120">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="ce350-120">The default value is 10.</span></span>

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

### <span data-ttu-id="ce350-121">-內容</span><span class="sxs-lookup"><span data-stu-id="ce350-121">-Context</span></span>
<span data-ttu-id="ce350-122">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="ce350-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ce350-123">若要取得儲存內容，請使用 [AzStorageCoNtext](./New-AzStorageContext.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ce350-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="ce350-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce350-124">-DefaultProfile</span></span>
<span data-ttu-id="ce350-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ce350-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce350-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="ce350-126">-ExpiryTime</span></span>
<span data-ttu-id="ce350-127">指定儲存的存取原則失效的時間。</span><span class="sxs-lookup"><span data-stu-id="ce350-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="ce350-128">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="ce350-128">-NoExpiryTime</span></span>
<span data-ttu-id="ce350-129">表示此 Cmdlet 清除已儲存的存取原則中的 **ExpiryTime** 屬性。</span><span class="sxs-lookup"><span data-stu-id="ce350-129">Indicates that this cmdlet clears the **ExpiryTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="ce350-130">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="ce350-130">-NoStartTime</span></span>
<span data-ttu-id="ce350-131">表示此 Cmdlet 清除已儲存的 access 原則中的 **StartTime** 屬性。</span><span class="sxs-lookup"><span data-stu-id="ce350-131">Indicates that this cmdlet clears the **StartTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="ce350-132">-許可權</span><span class="sxs-lookup"><span data-stu-id="ce350-132">-Permission</span></span>
<span data-ttu-id="ce350-133">在儲存的存取原則中指定許可權，以存取共用或其底下的檔案。</span><span class="sxs-lookup"><span data-stu-id="ce350-133">Specifies permissions in the stored access policy to access the share or files under it.</span></span>
<span data-ttu-id="ce350-134">請務必注意，這是字串，就像是 `rwd` 讀取、寫入及刪除) 的 (。</span><span class="sxs-lookup"><span data-stu-id="ce350-134">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="ce350-135">-原則</span><span class="sxs-lookup"><span data-stu-id="ce350-135">-Policy</span></span>
<span data-ttu-id="ce350-136">指定儲存的存取原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="ce350-136">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="ce350-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ce350-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ce350-138">指定要求中伺服器部分的超時時間長度。</span><span class="sxs-lookup"><span data-stu-id="ce350-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="ce350-139">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="ce350-139">-ShareName</span></span>
<span data-ttu-id="ce350-140">指定儲存空間共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="ce350-140">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="ce350-141">-StartTime</span><span class="sxs-lookup"><span data-stu-id="ce350-141">-StartTime</span></span>
<span data-ttu-id="ce350-142">指定儲存的存取原則生效的時間。</span><span class="sxs-lookup"><span data-stu-id="ce350-142">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="ce350-143">-確認</span><span class="sxs-lookup"><span data-stu-id="ce350-143">-Confirm</span></span>
<span data-ttu-id="ce350-144">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ce350-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce350-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce350-145">-WhatIf</span></span>
<span data-ttu-id="ce350-146">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ce350-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ce350-147">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ce350-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce350-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce350-148">CommonParameters</span></span>
<span data-ttu-id="ce350-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ce350-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce350-150">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ce350-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce350-151">輸入</span><span class="sxs-lookup"><span data-stu-id="ce350-151">INPUTS</span></span>

### <span data-ttu-id="ce350-152">System.object</span><span class="sxs-lookup"><span data-stu-id="ce350-152">System.String</span></span>

### <span data-ttu-id="ce350-153">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="ce350-153">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ce350-154">輸出</span><span class="sxs-lookup"><span data-stu-id="ce350-154">OUTPUTS</span></span>

### <span data-ttu-id="ce350-155">System.object</span><span class="sxs-lookup"><span data-stu-id="ce350-155">System.String</span></span>

## <span data-ttu-id="ce350-156">筆記</span><span class="sxs-lookup"><span data-stu-id="ce350-156">NOTES</span></span>

## <span data-ttu-id="ce350-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="ce350-157">RELATED LINKS</span></span>

[<span data-ttu-id="ce350-158">AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ce350-158">Get-AzStorageShareStoredAccessPolicy</span></span>](./Get-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="ce350-159">新-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="ce350-159">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="ce350-160">新-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ce350-160">New-AzStorageShareStoredAccessPolicy</span></span>](./New-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="ce350-161">移除-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ce350-161">Remove-AzStorageShareStoredAccessPolicy</span></span>](./Remove-AzStorageShareStoredAccessPolicy.md)
