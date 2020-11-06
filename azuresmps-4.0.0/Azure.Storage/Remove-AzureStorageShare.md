---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FF3AD436-CA33-4A52-8580-D2345D80A231
online version: ''
schema: 2.0.0
ms.openlocfilehash: 07ca74b29dad61c1cf909f13aefbf35b2048d4aa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93442968"
---
# <span data-ttu-id="5f115-101">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="5f115-101">Remove-AzureStorageShare</span></span>

## <span data-ttu-id="5f115-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5f115-102">SYNOPSIS</span></span>
<span data-ttu-id="5f115-103">刪除檔案共用。</span><span class="sxs-lookup"><span data-stu-id="5f115-103">Deletes a file share.</span></span>

## <span data-ttu-id="5f115-104">句法</span><span class="sxs-lookup"><span data-stu-id="5f115-104">SYNTAX</span></span>

### <span data-ttu-id="5f115-105">共用名稱 (預設) </span><span class="sxs-lookup"><span data-stu-id="5f115-105">ShareName (Default)</span></span>
```
Remove-AzureStorageShare [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f115-106">共用</span><span class="sxs-lookup"><span data-stu-id="5f115-106">Share</span></span>
```
Remove-AzureStorageShare [-Share] <CloudFileShare> [-Force] [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f115-107">說明</span><span class="sxs-lookup"><span data-stu-id="5f115-107">DESCRIPTION</span></span>
<span data-ttu-id="5f115-108">**AzureStorageShare** Cmdlet 會刪除檔案共用。</span><span class="sxs-lookup"><span data-stu-id="5f115-108">The **Remove-AzureStorageShare** cmdlet deletes a file share.</span></span>

## <span data-ttu-id="5f115-109">示例</span><span class="sxs-lookup"><span data-stu-id="5f115-109">EXAMPLES</span></span>

### <span data-ttu-id="5f115-110">範例1：移除檔案共用</span><span class="sxs-lookup"><span data-stu-id="5f115-110">Example 1: Remove a file share</span></span>
```
PS C:\>Remove-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="5f115-111">這個命令會移除名為 ContosoShare06 的檔案共用。</span><span class="sxs-lookup"><span data-stu-id="5f115-111">This command removes the file share named ContosoShare06.</span></span>

## <span data-ttu-id="5f115-112">參數</span><span class="sxs-lookup"><span data-stu-id="5f115-112">PARAMETERS</span></span>

### <span data-ttu-id="5f115-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5f115-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="5f115-114">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="5f115-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="5f115-115">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="5f115-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="5f115-116">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="5f115-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="5f115-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="5f115-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="5f115-118">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="5f115-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="5f115-119">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="5f115-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="5f115-120">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="5f115-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="5f115-121">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="5f115-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="5f115-122">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="5f115-122">The default value is 10.</span></span>

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

### <span data-ttu-id="5f115-123">-內容</span><span class="sxs-lookup"><span data-stu-id="5f115-123">-Context</span></span>
<span data-ttu-id="5f115-124">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="5f115-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="5f115-125">若要取得儲存內容，請使用 [AzureStorageCoNtext](./New-AzureStorageContext.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5f115-125">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ShareName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f115-126">-Force</span><span class="sxs-lookup"><span data-stu-id="5f115-126">-Force</span></span>
<span data-ttu-id="5f115-127">強制移除共用及其中的所有內容</span><span class="sxs-lookup"><span data-stu-id="5f115-127">Force to remove the share and all content in it</span></span>

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

### <span data-ttu-id="5f115-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="5f115-128">-Name</span></span>
<span data-ttu-id="5f115-129">指定檔案共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="5f115-129">Specifies the name of the file share.</span></span>
<span data-ttu-id="5f115-130">這個 Cmdlet 會刪除此參數指定的檔案共用。</span><span class="sxs-lookup"><span data-stu-id="5f115-130">This cmdlet deletes the file share that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f115-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5f115-131">-PassThru</span></span>
<span data-ttu-id="5f115-132">表示此 Cmdlet 會傳回反映操作成功的 **布林值** 。</span><span class="sxs-lookup"><span data-stu-id="5f115-132">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="5f115-133">根據預設，這個 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="5f115-133">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="5f115-134">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5f115-134">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="5f115-135">指定要求中伺服器部分的超時時間長度。</span><span class="sxs-lookup"><span data-stu-id="5f115-135">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="5f115-136">-共用</span><span class="sxs-lookup"><span data-stu-id="5f115-136">-Share</span></span>
<span data-ttu-id="5f115-137">指定 **CloudFileShare** 物件。</span><span class="sxs-lookup"><span data-stu-id="5f115-137">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="5f115-138">這個 Cmdlet 會移除此參數指定的物件。</span><span class="sxs-lookup"><span data-stu-id="5f115-138">This cmdlet removes the object that this parameter specifies.</span></span>
<span data-ttu-id="5f115-139">若要取得 **CloudFileShare** 物件，請使用 Get-AzureStorageShare Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5f115-139">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="5f115-140">此物件包含儲存內容。</span><span class="sxs-lookup"><span data-stu-id="5f115-140">This object contains the storage context.</span></span>
<span data-ttu-id="5f115-141">如果您指定此參數，請勿指定 *CoNtext* 參數。</span><span class="sxs-lookup"><span data-stu-id="5f115-141">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: CloudFileShare
Parameter Sets: Share
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f115-142">-確認</span><span class="sxs-lookup"><span data-stu-id="5f115-142">-Confirm</span></span>
<span data-ttu-id="5f115-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5f115-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f115-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f115-144">-WhatIf</span></span>
<span data-ttu-id="5f115-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5f115-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f115-146">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5f115-146">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f115-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f115-147">CommonParameters</span></span>
<span data-ttu-id="5f115-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5f115-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f115-149">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5f115-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f115-150">輸入</span><span class="sxs-lookup"><span data-stu-id="5f115-150">INPUTS</span></span>

## <span data-ttu-id="5f115-151">輸出</span><span class="sxs-lookup"><span data-stu-id="5f115-151">OUTPUTS</span></span>

## <span data-ttu-id="5f115-152">筆記</span><span class="sxs-lookup"><span data-stu-id="5f115-152">NOTES</span></span>

## <span data-ttu-id="5f115-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="5f115-153">RELATED LINKS</span></span>

[<span data-ttu-id="5f115-154">AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="5f115-154">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="5f115-155">新-AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="5f115-155">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="5f115-156">新-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="5f115-156">New-AzureStorageShare</span></span>](./New-AzureStorageShare.md)
