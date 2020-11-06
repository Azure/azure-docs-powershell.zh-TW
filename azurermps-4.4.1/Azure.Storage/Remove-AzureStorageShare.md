---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FF3AD436-CA33-4A52-8580-D2345D80A231
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageShare.md
gitcommit: https://github.com/Azure/azure-powershell/blob/173e94aec59d7f539b72e43e90e5e7f8ba5f62bc
ms.openlocfilehash: 66662899694f7b1fb93dd109e1dccefee5e00182
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455012"
---
# <span data-ttu-id="ac84b-101">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="ac84b-101">Remove-AzureStorageShare</span></span>

## <span data-ttu-id="ac84b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ac84b-102">SYNOPSIS</span></span>
<span data-ttu-id="ac84b-103">刪除檔案共用。</span><span class="sxs-lookup"><span data-stu-id="ac84b-103">Deletes a file share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac84b-104">句法</span><span class="sxs-lookup"><span data-stu-id="ac84b-104">SYNTAX</span></span>

### <span data-ttu-id="ac84b-105">共用名稱 (預設) </span><span class="sxs-lookup"><span data-stu-id="ac84b-105">ShareName (Default)</span></span>
```
Remove-AzureStorageShare [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac84b-106">共用</span><span class="sxs-lookup"><span data-stu-id="ac84b-106">Share</span></span>
```
Remove-AzureStorageShare [-Share] <CloudFileShare> [-Force] [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac84b-107">說明</span><span class="sxs-lookup"><span data-stu-id="ac84b-107">DESCRIPTION</span></span>
<span data-ttu-id="ac84b-108">**AzureStorageShare** Cmdlet 會刪除檔案共用。</span><span class="sxs-lookup"><span data-stu-id="ac84b-108">The **Remove-AzureStorageShare** cmdlet deletes a file share.</span></span>

## <span data-ttu-id="ac84b-109">示例</span><span class="sxs-lookup"><span data-stu-id="ac84b-109">EXAMPLES</span></span>

### <span data-ttu-id="ac84b-110">範例1：移除檔案共用</span><span class="sxs-lookup"><span data-stu-id="ac84b-110">Example 1: Remove a file share</span></span>
```
PS C:\>Remove-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="ac84b-111">這個命令會移除名為 ContosoShare06 的檔案共用。</span><span class="sxs-lookup"><span data-stu-id="ac84b-111">This command removes the file share named ContosoShare06.</span></span>

## <span data-ttu-id="ac84b-112">參數</span><span class="sxs-lookup"><span data-stu-id="ac84b-112">PARAMETERS</span></span>

### <span data-ttu-id="ac84b-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ac84b-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ac84b-114">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="ac84b-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ac84b-115">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="ac84b-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ac84b-116">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="ac84b-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ac84b-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ac84b-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ac84b-118">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="ac84b-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ac84b-119">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="ac84b-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ac84b-120">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="ac84b-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ac84b-121">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="ac84b-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ac84b-122">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="ac84b-122">The default value is 10.</span></span>

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

### <span data-ttu-id="ac84b-123">-內容</span><span class="sxs-lookup"><span data-stu-id="ac84b-123">-Context</span></span>
<span data-ttu-id="ac84b-124">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="ac84b-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ac84b-125">若要取得儲存內容，請使用 [AzureStorageCoNtext](./New-AzureStorageContext.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ac84b-125">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="ac84b-126">-Force</span><span class="sxs-lookup"><span data-stu-id="ac84b-126">-Force</span></span>
<span data-ttu-id="ac84b-127">強制移除共用及其中的所有內容</span><span class="sxs-lookup"><span data-stu-id="ac84b-127">Force to remove the share and all content in it</span></span>

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

### <span data-ttu-id="ac84b-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="ac84b-128">-Name</span></span>
<span data-ttu-id="ac84b-129">指定檔案共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="ac84b-129">Specifies the name of the file share.</span></span>
<span data-ttu-id="ac84b-130">這個 Cmdlet 會刪除此參數指定的檔案共用。</span><span class="sxs-lookup"><span data-stu-id="ac84b-130">This cmdlet deletes the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="ac84b-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ac84b-131">-PassThru</span></span>
<span data-ttu-id="ac84b-132">表示此 Cmdlet 會傳回反映操作成功的 **布林值** 。</span><span class="sxs-lookup"><span data-stu-id="ac84b-132">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="ac84b-133">根據預設，這個 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="ac84b-133">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="ac84b-134">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ac84b-134">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ac84b-135">指定要求中伺服器部分的超時時間長度。</span><span class="sxs-lookup"><span data-stu-id="ac84b-135">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="ac84b-136">-共用</span><span class="sxs-lookup"><span data-stu-id="ac84b-136">-Share</span></span>
<span data-ttu-id="ac84b-137">指定 **CloudFileShare** 物件。</span><span class="sxs-lookup"><span data-stu-id="ac84b-137">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="ac84b-138">這個 Cmdlet 會移除此參數指定的物件。</span><span class="sxs-lookup"><span data-stu-id="ac84b-138">This cmdlet removes the object that this parameter specifies.</span></span>
<span data-ttu-id="ac84b-139">若要取得 **CloudFileShare** 物件，請使用 Get-AzureStorageShare Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ac84b-139">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="ac84b-140">此物件包含儲存內容。</span><span class="sxs-lookup"><span data-stu-id="ac84b-140">This object contains the storage context.</span></span>
<span data-ttu-id="ac84b-141">如果您指定此參數，請勿指定 *CoNtext* 參數。</span><span class="sxs-lookup"><span data-stu-id="ac84b-141">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="ac84b-142">-確認</span><span class="sxs-lookup"><span data-stu-id="ac84b-142">-Confirm</span></span>
<span data-ttu-id="ac84b-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ac84b-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac84b-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac84b-144">-WhatIf</span></span>
<span data-ttu-id="ac84b-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ac84b-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac84b-146">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ac84b-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac84b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac84b-147">CommonParameters</span></span>
<span data-ttu-id="ac84b-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ac84b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac84b-149">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ac84b-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac84b-150">輸入</span><span class="sxs-lookup"><span data-stu-id="ac84b-150">INPUTS</span></span>

### <span data-ttu-id="ac84b-151">IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="ac84b-151">IStorageContext</span></span>

<span data-ttu-id="ac84b-152">參數「CoNtext」接受來自管線的 "IStorageCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="ac84b-152">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="ac84b-153">字串</span><span class="sxs-lookup"><span data-stu-id="ac84b-153">String</span></span>

<span data-ttu-id="ac84b-154">形參 "Name" 接受管線中類型 "String" 的值</span><span class="sxs-lookup"><span data-stu-id="ac84b-154">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="ac84b-155">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="ac84b-155">CloudFileShare</span></span>

<span data-ttu-id="ac84b-156">形參 "Share" 接受管線中 "CloudFileShare" 類型的值</span><span class="sxs-lookup"><span data-stu-id="ac84b-156">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

## <span data-ttu-id="ac84b-157">輸出</span><span class="sxs-lookup"><span data-stu-id="ac84b-157">OUTPUTS</span></span>

## <span data-ttu-id="ac84b-158">筆記</span><span class="sxs-lookup"><span data-stu-id="ac84b-158">NOTES</span></span>

## <span data-ttu-id="ac84b-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="ac84b-159">RELATED LINKS</span></span>

[<span data-ttu-id="ac84b-160">AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="ac84b-160">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="ac84b-161">新-AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="ac84b-161">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="ac84b-162">新-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="ac84b-162">New-AzureStorageShare</span></span>](./New-AzureStorageShare.md)
