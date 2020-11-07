---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 730ECC60-72DE-46DA-A177-D5749F540710
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageContainerStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 63fd207c9d3348e17718f6d4ad8dbd53a09752af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625736"
---
# <span data-ttu-id="5a8b9-101">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5a8b9-101">Set-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="5a8b9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5a8b9-102">SYNOPSIS</span></span>
<span data-ttu-id="5a8b9-103">針對 Azure 儲存體容器設定儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-103">Sets a stored access policy for an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a8b9-104">句法</span><span class="sxs-lookup"><span data-stu-id="5a8b9-104">SYNTAX</span></span>

```
Set-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a8b9-105">說明</span><span class="sxs-lookup"><span data-stu-id="5a8b9-105">DESCRIPTION</span></span>
<span data-ttu-id="5a8b9-106">**AzureStorageContainerStoredAccessPolicy** Cmdlet 會為 Azure 儲存空間容器設定儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-106">The **Set-AzureStorageContainerStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="5a8b9-107">示例</span><span class="sxs-lookup"><span data-stu-id="5a8b9-107">EXAMPLES</span></span>

### <span data-ttu-id="5a8b9-108">範例1：在擁有完整許可權的儲存空間容器中設定儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="5a8b9-108">Example 1: Set a stored access policy in a storage container with full permission</span></span>
```
PS C:\>Set-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy06" -Permission rwdl
```

<span data-ttu-id="5a8b9-109">這個命令會針對儲存容器（名為 MyContainer）設定一個名為 Policy06 的存取原則。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-109">This command sets an access policy named Policy06 for storage container named MyContainer.</span></span>

## <span data-ttu-id="5a8b9-110">參數</span><span class="sxs-lookup"><span data-stu-id="5a8b9-110">PARAMETERS</span></span>

### <span data-ttu-id="5a8b9-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5a8b9-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="5a8b9-112">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="5a8b9-113">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="5a8b9-114">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a8b9-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="5a8b9-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="5a8b9-116">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="5a8b9-117">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="5a8b9-118">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="5a8b9-119">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="5a8b9-120">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-120">The default value is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a8b9-121">-容器</span><span class="sxs-lookup"><span data-stu-id="5a8b9-121">-Container</span></span>
<span data-ttu-id="5a8b9-122">指定 Azure 儲存空間容器名稱。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-122">Specifies the Azure storage container name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a8b9-123">-內容</span><span class="sxs-lookup"><span data-stu-id="5a8b9-123">-Context</span></span>
<span data-ttu-id="5a8b9-124">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="5a8b9-125">若要取得儲存內容，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-125">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a8b9-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="5a8b9-126">-ExpiryTime</span></span>
<span data-ttu-id="5a8b9-127">指定儲存的存取原則失效的時間。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a8b9-128">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="5a8b9-128">-NoExpiryTime</span></span>
<span data-ttu-id="5a8b9-129">指示存取原則沒有到期日。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-129">Indicates that the access policy has no expiration date.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a8b9-130">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="5a8b9-130">-NoStartTime</span></span>
<span data-ttu-id="5a8b9-131">將 [開始時間] 設定為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-131">Sets the start time to be $Null.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a8b9-132">-許可權</span><span class="sxs-lookup"><span data-stu-id="5a8b9-132">-Permission</span></span>
<span data-ttu-id="5a8b9-133">在儲存的存取原則中指定許可權，以存取儲存空間容器。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-133">Specifies permissions in the stored access policy to access the storage container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a8b9-134">-原則</span><span class="sxs-lookup"><span data-stu-id="5a8b9-134">-Policy</span></span>
<span data-ttu-id="5a8b9-135">指定儲存的存取原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-135">Specifies the name for the stored access policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a8b9-136">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5a8b9-136">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="5a8b9-137">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-137">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="5a8b9-138">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-138">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="5a8b9-139">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-139">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a8b9-140">-StartTime</span><span class="sxs-lookup"><span data-stu-id="5a8b9-140">-StartTime</span></span>
<span data-ttu-id="5a8b9-141">指定儲存的存取原則生效的時間。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-141">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a8b9-142">-確認</span><span class="sxs-lookup"><span data-stu-id="5a8b9-142">-Confirm</span></span>
<span data-ttu-id="5a8b9-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a8b9-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a8b9-144">-WhatIf</span></span>
<span data-ttu-id="5a8b9-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5a8b9-146">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-146">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a8b9-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a8b9-147">CommonParameters</span></span>
<span data-ttu-id="5a8b9-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a8b9-149">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5a8b9-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a8b9-150">輸入</span><span class="sxs-lookup"><span data-stu-id="5a8b9-150">INPUTS</span></span>

### <span data-ttu-id="5a8b9-151">字串</span><span class="sxs-lookup"><span data-stu-id="5a8b9-151">String</span></span>

<span data-ttu-id="5a8b9-152">"Container" 是從管線接受類型 "String" 的值</span><span class="sxs-lookup"><span data-stu-id="5a8b9-152">Parameter 'Container' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="5a8b9-153">IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="5a8b9-153">IStorageContext</span></span>

<span data-ttu-id="5a8b9-154">參數「CoNtext」接受來自管線的 "IStorageCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="5a8b9-154">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="5a8b9-155">輸出</span><span class="sxs-lookup"><span data-stu-id="5a8b9-155">OUTPUTS</span></span>

### <span data-ttu-id="5a8b9-156">System.object</span><span class="sxs-lookup"><span data-stu-id="5a8b9-156">System.String</span></span>

## <span data-ttu-id="5a8b9-157">筆記</span><span class="sxs-lookup"><span data-stu-id="5a8b9-157">NOTES</span></span>

## <span data-ttu-id="5a8b9-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="5a8b9-158">RELATED LINKS</span></span>

[<span data-ttu-id="5a8b9-159">AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5a8b9-159">Get-AzureStorageContainerStoredAccessPolicy</span></span>](./Get-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="5a8b9-160">新-AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="5a8b9-160">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="5a8b9-161">新-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5a8b9-161">New-AzureStorageContainerStoredAccessPolicy</span></span>](./New-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="5a8b9-162">移除-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5a8b9-162">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)
