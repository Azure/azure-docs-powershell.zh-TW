---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 730ECC60-72DE-46DA-A177-D5749F540710
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: f6c83084d52848e3dff25e2d3f0a22255845a56c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93611785"
---
# <span data-ttu-id="8c852-101">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8c852-101">Set-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="8c852-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8c852-102">SYNOPSIS</span></span>
<span data-ttu-id="8c852-103">針對 Azure 儲存體容器設定儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="8c852-103">Sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="8c852-104">句法</span><span class="sxs-lookup"><span data-stu-id="8c852-104">SYNTAX</span></span>

```
Set-AzStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8c852-105">說明</span><span class="sxs-lookup"><span data-stu-id="8c852-105">DESCRIPTION</span></span>
<span data-ttu-id="8c852-106">**AzStorageContainerStoredAccessPolicy** Cmdlet 會為 Azure 儲存空間容器設定儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="8c852-106">The **Set-AzStorageContainerStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="8c852-107">示例</span><span class="sxs-lookup"><span data-stu-id="8c852-107">EXAMPLES</span></span>

### <span data-ttu-id="8c852-108">範例1：在擁有完整許可權的儲存空間容器中設定儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="8c852-108">Example 1: Set a stored access policy in a storage container with full permission</span></span>
```
PS C:\>Set-AzStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy06" -Permission rwdl
```

<span data-ttu-id="8c852-109">這個命令會針對儲存容器（名為 MyContainer）設定一個名為 Policy06 的存取原則。</span><span class="sxs-lookup"><span data-stu-id="8c852-109">This command sets an access policy named Policy06 for storage container named MyContainer.</span></span>

## <span data-ttu-id="8c852-110">參數</span><span class="sxs-lookup"><span data-stu-id="8c852-110">PARAMETERS</span></span>

### <span data-ttu-id="8c852-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8c852-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="8c852-112">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="8c852-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="8c852-113">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="8c852-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="8c852-114">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="8c852-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="8c852-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="8c852-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="8c852-116">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="8c852-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="8c852-117">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="8c852-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="8c852-118">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="8c852-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="8c852-119">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="8c852-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="8c852-120">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="8c852-120">The default value is 10.</span></span>

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

### <span data-ttu-id="8c852-121">-容器</span><span class="sxs-lookup"><span data-stu-id="8c852-121">-Container</span></span>
<span data-ttu-id="8c852-122">指定 Azure 儲存空間容器名稱。</span><span class="sxs-lookup"><span data-stu-id="8c852-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="8c852-123">-內容</span><span class="sxs-lookup"><span data-stu-id="8c852-123">-Context</span></span>
<span data-ttu-id="8c852-124">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="8c852-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="8c852-125">若要取得儲存內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c852-125">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="8c852-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c852-126">-DefaultProfile</span></span>
<span data-ttu-id="8c852-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8c852-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c852-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="8c852-128">-ExpiryTime</span></span>
<span data-ttu-id="8c852-129">指定儲存的存取原則失效的時間。</span><span class="sxs-lookup"><span data-stu-id="8c852-129">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="8c852-130">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="8c852-130">-NoExpiryTime</span></span>
<span data-ttu-id="8c852-131">指示存取原則沒有到期日。</span><span class="sxs-lookup"><span data-stu-id="8c852-131">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="8c852-132">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="8c852-132">-NoStartTime</span></span>
<span data-ttu-id="8c852-133">將 [開始時間] 設定為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="8c852-133">Sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="8c852-134">-許可權</span><span class="sxs-lookup"><span data-stu-id="8c852-134">-Permission</span></span>
<span data-ttu-id="8c852-135">在儲存的存取原則中指定許可權，以存取儲存空間容器。</span><span class="sxs-lookup"><span data-stu-id="8c852-135">Specifies permissions in the stored access policy to access the storage container.</span></span>
<span data-ttu-id="8c852-136">請務必注意，這是字串，就像是 `rwd` 讀取、寫入及刪除) 的 (。</span><span class="sxs-lookup"><span data-stu-id="8c852-136">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="8c852-137">-原則</span><span class="sxs-lookup"><span data-stu-id="8c852-137">-Policy</span></span>
<span data-ttu-id="8c852-138">指定儲存的存取原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="8c852-138">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="8c852-139">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8c852-139">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="8c852-140">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="8c852-140">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="8c852-141">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="8c852-141">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="8c852-142">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="8c852-142">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="8c852-143">-StartTime</span><span class="sxs-lookup"><span data-stu-id="8c852-143">-StartTime</span></span>
<span data-ttu-id="8c852-144">指定儲存的存取原則生效的時間。</span><span class="sxs-lookup"><span data-stu-id="8c852-144">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="8c852-145">-確認</span><span class="sxs-lookup"><span data-stu-id="8c852-145">-Confirm</span></span>
<span data-ttu-id="8c852-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8c852-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c852-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c852-147">-WhatIf</span></span>
<span data-ttu-id="8c852-148">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8c852-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8c852-149">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c852-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c852-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c852-150">CommonParameters</span></span>
<span data-ttu-id="8c852-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8c852-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c852-152">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8c852-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c852-153">輸入</span><span class="sxs-lookup"><span data-stu-id="8c852-153">INPUTS</span></span>

### <span data-ttu-id="8c852-154">System.object</span><span class="sxs-lookup"><span data-stu-id="8c852-154">System.String</span></span>

### <span data-ttu-id="8c852-155">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="8c852-155">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8c852-156">輸出</span><span class="sxs-lookup"><span data-stu-id="8c852-156">OUTPUTS</span></span>

### <span data-ttu-id="8c852-157">System.object</span><span class="sxs-lookup"><span data-stu-id="8c852-157">System.String</span></span>

## <span data-ttu-id="8c852-158">筆記</span><span class="sxs-lookup"><span data-stu-id="8c852-158">NOTES</span></span>

## <span data-ttu-id="8c852-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="8c852-159">RELATED LINKS</span></span>

[<span data-ttu-id="8c852-160">AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8c852-160">Get-AzStorageContainerStoredAccessPolicy</span></span>](./Get-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="8c852-161">新-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="8c852-161">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="8c852-162">新-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8c852-162">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="8c852-163">移除-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8c852-163">Remove-AzStorageContainerStoredAccessPolicy</span></span>](./Remove-AzStorageContainerStoredAccessPolicy.md)