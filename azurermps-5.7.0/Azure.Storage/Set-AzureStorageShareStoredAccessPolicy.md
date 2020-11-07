---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C21CC2FA-017E-492E-96E7-B37829917FAF
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 0c77d2dedadd205a659bf296e02c09b98342dcc6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626456"
---
# <span data-ttu-id="6ba55-101">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6ba55-101">Set-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="6ba55-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6ba55-102">SYNOPSIS</span></span>
<span data-ttu-id="6ba55-103">更新儲存空間共用上的儲存存取原則。</span><span class="sxs-lookup"><span data-stu-id="6ba55-103">Updates a stored access policy on a Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ba55-104">句法</span><span class="sxs-lookup"><span data-stu-id="6ba55-104">SYNTAX</span></span>

```
Set-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ba55-105">說明</span><span class="sxs-lookup"><span data-stu-id="6ba55-105">DESCRIPTION</span></span>
<span data-ttu-id="6ba55-106">**AzureStorageShareStoredAccessPolicy** Cmdlet 會更新 Azure 儲存空間共用上儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="6ba55-106">The **Set-AzureStorageShareStoredAccessPolicy** cmdlet updates stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="6ba55-107">示例</span><span class="sxs-lookup"><span data-stu-id="6ba55-107">EXAMPLES</span></span>

### <span data-ttu-id="6ba55-108">範例1：在儲存空間共用中更新已儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="6ba55-108">Example 1: Update a stored access policy in Storage share</span></span>
```
PS C:\>Set-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="6ba55-109">這個命令會更新在共用中擁有完整許可權的儲存存取原則。</span><span class="sxs-lookup"><span data-stu-id="6ba55-109">This command updates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="6ba55-110">參數</span><span class="sxs-lookup"><span data-stu-id="6ba55-110">PARAMETERS</span></span>

### <span data-ttu-id="6ba55-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6ba55-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="6ba55-112">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="6ba55-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="6ba55-113">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="6ba55-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="6ba55-114">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="6ba55-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="6ba55-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="6ba55-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="6ba55-116">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="6ba55-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="6ba55-117">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="6ba55-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="6ba55-118">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="6ba55-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="6ba55-119">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="6ba55-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="6ba55-120">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="6ba55-120">The default value is 10.</span></span>

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

### <span data-ttu-id="6ba55-121">-內容</span><span class="sxs-lookup"><span data-stu-id="6ba55-121">-Context</span></span>
<span data-ttu-id="6ba55-122">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="6ba55-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="6ba55-123">若要取得儲存內容，請使用 [AzureStorageCoNtext](./New-AzureStorageContext.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6ba55-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="6ba55-124">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="6ba55-124">-ExpiryTime</span></span>
<span data-ttu-id="6ba55-125">指定儲存的存取原則失效的時間。</span><span class="sxs-lookup"><span data-stu-id="6ba55-125">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="6ba55-126">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="6ba55-126">-NoExpiryTime</span></span>
<span data-ttu-id="6ba55-127">表示此 Cmdlet 清除已儲存的存取原則中的 **ExpiryTime** 屬性。</span><span class="sxs-lookup"><span data-stu-id="6ba55-127">Indicates that this cmdlet clears the **ExpiryTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="6ba55-128">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="6ba55-128">-NoStartTime</span></span>
<span data-ttu-id="6ba55-129">表示此 Cmdlet 清除已儲存的 access 原則中的 **StartTime** 屬性。</span><span class="sxs-lookup"><span data-stu-id="6ba55-129">Indicates that this cmdlet clears the **StartTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="6ba55-130">-許可權</span><span class="sxs-lookup"><span data-stu-id="6ba55-130">-Permission</span></span>
<span data-ttu-id="6ba55-131">在儲存的存取原則中指定許可權，以存取共用或其底下的檔案。</span><span class="sxs-lookup"><span data-stu-id="6ba55-131">Specifies permissions in the stored access policy to access the share or files under it.</span></span>

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

### <span data-ttu-id="6ba55-132">-原則</span><span class="sxs-lookup"><span data-stu-id="6ba55-132">-Policy</span></span>
<span data-ttu-id="6ba55-133">指定儲存的存取原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="6ba55-133">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="6ba55-134">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6ba55-134">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="6ba55-135">指定要求中伺服器部分的超時時間長度。</span><span class="sxs-lookup"><span data-stu-id="6ba55-135">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="6ba55-136">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="6ba55-136">-ShareName</span></span>
<span data-ttu-id="6ba55-137">指定儲存空間共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="6ba55-137">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="6ba55-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="6ba55-138">-StartTime</span></span>
<span data-ttu-id="6ba55-139">指定儲存的存取原則生效的時間。</span><span class="sxs-lookup"><span data-stu-id="6ba55-139">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="6ba55-140">-確認</span><span class="sxs-lookup"><span data-stu-id="6ba55-140">-Confirm</span></span>
<span data-ttu-id="6ba55-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6ba55-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ba55-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ba55-142">-WhatIf</span></span>
<span data-ttu-id="6ba55-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6ba55-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6ba55-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6ba55-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ba55-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ba55-145">CommonParameters</span></span>
<span data-ttu-id="6ba55-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6ba55-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ba55-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6ba55-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ba55-148">輸入</span><span class="sxs-lookup"><span data-stu-id="6ba55-148">INPUTS</span></span>

### <span data-ttu-id="6ba55-149">IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="6ba55-149">IStorageContext</span></span>

<span data-ttu-id="6ba55-150">參數「CoNtext」接受來自管線的 "IStorageCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="6ba55-150">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="6ba55-151">字串</span><span class="sxs-lookup"><span data-stu-id="6ba55-151">String</span></span>

<span data-ttu-id="6ba55-152">參數「共用名稱」接受來自管線的 "String" 類型的值</span><span class="sxs-lookup"><span data-stu-id="6ba55-152">Parameter 'ShareName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="6ba55-153">輸出</span><span class="sxs-lookup"><span data-stu-id="6ba55-153">OUTPUTS</span></span>

### <span data-ttu-id="6ba55-154">System.object</span><span class="sxs-lookup"><span data-stu-id="6ba55-154">System.String</span></span>

## <span data-ttu-id="6ba55-155">筆記</span><span class="sxs-lookup"><span data-stu-id="6ba55-155">NOTES</span></span>

## <span data-ttu-id="6ba55-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="6ba55-156">RELATED LINKS</span></span>

[<span data-ttu-id="6ba55-157">AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6ba55-157">Get-AzureStorageShareStoredAccessPolicy</span></span>](./Get-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="6ba55-158">新-AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="6ba55-158">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="6ba55-159">新-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6ba55-159">New-AzureStorageShareStoredAccessPolicy</span></span>](./New-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="6ba55-160">移除-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6ba55-160">Remove-AzureStorageShareStoredAccessPolicy</span></span>](./Remove-AzureStorageShareStoredAccessPolicy.md)
