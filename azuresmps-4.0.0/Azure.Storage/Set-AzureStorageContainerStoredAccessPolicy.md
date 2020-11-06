---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 730ECC60-72DE-46DA-A177-D5749F540710
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1bdded3834806e33f4605f626b78fe06bc370bf6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443555"
---
# <span data-ttu-id="3a190-101">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3a190-101">Set-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="3a190-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3a190-102">SYNOPSIS</span></span>
<span data-ttu-id="3a190-103">針對 Azure 儲存體容器設定儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="3a190-103">Sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="3a190-104">句法</span><span class="sxs-lookup"><span data-stu-id="3a190-104">SYNTAX</span></span>

```
Set-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a190-105">說明</span><span class="sxs-lookup"><span data-stu-id="3a190-105">DESCRIPTION</span></span>
<span data-ttu-id="3a190-106">**AzureStorageContainerStoredAccessPolicy** Cmdlet 會為 Azure 儲存空間容器設定儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="3a190-106">The **Set-AzureStorageContainerStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="3a190-107">示例</span><span class="sxs-lookup"><span data-stu-id="3a190-107">EXAMPLES</span></span>

### <span data-ttu-id="3a190-108">範例1：在儲存空間容器中設定儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="3a190-108">Example 1: Set a stored access policy in a storage container</span></span>
```
PS C:\>Set-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy06"
```

<span data-ttu-id="3a190-109">這個命令會針對儲存容器（名為 MyContainer）設定一個名為 Policy06 的存取原則。</span><span class="sxs-lookup"><span data-stu-id="3a190-109">This command sets an access policy named Policy06 for storage container named MyContainer.</span></span>

## <span data-ttu-id="3a190-110">參數</span><span class="sxs-lookup"><span data-stu-id="3a190-110">PARAMETERS</span></span>

### <span data-ttu-id="3a190-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3a190-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="3a190-112">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="3a190-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="3a190-113">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="3a190-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="3a190-114">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="3a190-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="3a190-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="3a190-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="3a190-116">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="3a190-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="3a190-117">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="3a190-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="3a190-118">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="3a190-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="3a190-119">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="3a190-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="3a190-120">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="3a190-120">The default value is 10.</span></span>

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

### <span data-ttu-id="3a190-121">-容器</span><span class="sxs-lookup"><span data-stu-id="3a190-121">-Container</span></span>
<span data-ttu-id="3a190-122">指定 Azure 儲存空間容器名稱。</span><span class="sxs-lookup"><span data-stu-id="3a190-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="3a190-123">-內容</span><span class="sxs-lookup"><span data-stu-id="3a190-123">-Context</span></span>
<span data-ttu-id="3a190-124">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="3a190-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="3a190-125">若要取得儲存內容，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3a190-125">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="3a190-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="3a190-126">-ExpiryTime</span></span>
<span data-ttu-id="3a190-127">指定儲存的存取原則失效的時間。</span><span class="sxs-lookup"><span data-stu-id="3a190-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="3a190-128">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="3a190-128">-NoExpiryTime</span></span>
<span data-ttu-id="3a190-129">指示存取原則沒有到期日。</span><span class="sxs-lookup"><span data-stu-id="3a190-129">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="3a190-130">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="3a190-130">-NoStartTime</span></span>
<span data-ttu-id="3a190-131">將 [開始時間] 設定為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="3a190-131">Sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="3a190-132">-許可權</span><span class="sxs-lookup"><span data-stu-id="3a190-132">-Permission</span></span>
<span data-ttu-id="3a190-133">指定此容器的公開存取層級。</span><span class="sxs-lookup"><span data-stu-id="3a190-133">Specifies the level of public access to this container.</span></span>

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

### <span data-ttu-id="3a190-134">-原則</span><span class="sxs-lookup"><span data-stu-id="3a190-134">-Policy</span></span>
<span data-ttu-id="3a190-135">指定儲存的存取原則，包括此共用存取簽名 (SAS) 權杖的許可權。</span><span class="sxs-lookup"><span data-stu-id="3a190-135">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="3a190-136">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3a190-136">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="3a190-137">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="3a190-137">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="3a190-138">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="3a190-138">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="3a190-139">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="3a190-139">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="3a190-140">-StartTime</span><span class="sxs-lookup"><span data-stu-id="3a190-140">-StartTime</span></span>
<span data-ttu-id="3a190-141">指定儲存的存取原則生效的時間。</span><span class="sxs-lookup"><span data-stu-id="3a190-141">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="3a190-142">-確認</span><span class="sxs-lookup"><span data-stu-id="3a190-142">-Confirm</span></span>
<span data-ttu-id="3a190-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3a190-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a190-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a190-144">-WhatIf</span></span>
<span data-ttu-id="3a190-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3a190-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3a190-146">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3a190-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a190-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a190-147">CommonParameters</span></span>
<span data-ttu-id="3a190-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3a190-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a190-149">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3a190-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a190-150">輸入</span><span class="sxs-lookup"><span data-stu-id="3a190-150">INPUTS</span></span>

## <span data-ttu-id="3a190-151">輸出</span><span class="sxs-lookup"><span data-stu-id="3a190-151">OUTPUTS</span></span>

## <span data-ttu-id="3a190-152">筆記</span><span class="sxs-lookup"><span data-stu-id="3a190-152">NOTES</span></span>

## <span data-ttu-id="3a190-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="3a190-153">RELATED LINKS</span></span>

[<span data-ttu-id="3a190-154">AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3a190-154">Get-AzureStorageContainerStoredAccessPolicy</span></span>](./Get-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="3a190-155">新-AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="3a190-155">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="3a190-156">新-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3a190-156">New-AzureStorageContainerStoredAccessPolicy</span></span>](./New-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="3a190-157">移除-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3a190-157">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)
