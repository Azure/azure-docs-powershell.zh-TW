---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 6A46DA60-2ACF-4842-B5B3-58944264854A
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageContainer.md
ms.openlocfilehash: 23ea79879b7b194b9f761c585087a931f9373886
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447882"
---
# <span data-ttu-id="15af5-101">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="15af5-101">Remove-AzureStorageContainer</span></span>

## <span data-ttu-id="15af5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="15af5-102">SYNOPSIS</span></span>
<span data-ttu-id="15af5-103">移除指定的儲存空間容器。</span><span class="sxs-lookup"><span data-stu-id="15af5-103">Removes the specified storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15af5-104">句法</span><span class="sxs-lookup"><span data-stu-id="15af5-104">SYNTAX</span></span>

```
Remove-AzureStorageContainer [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15af5-105">說明</span><span class="sxs-lookup"><span data-stu-id="15af5-105">DESCRIPTION</span></span>
<span data-ttu-id="15af5-106">**AzureStorageContainer** Cmdlet 會在 Azure 中移除指定的儲存空間容器。</span><span class="sxs-lookup"><span data-stu-id="15af5-106">The **Remove-AzureStorageContainer** cmdlet removes the specified storage container in Azure.</span></span>

## <span data-ttu-id="15af5-107">示例</span><span class="sxs-lookup"><span data-stu-id="15af5-107">EXAMPLES</span></span>

### <span data-ttu-id="15af5-108">範例1：移除容器</span><span class="sxs-lookup"><span data-stu-id="15af5-108">Example 1: Remove a container</span></span>
```
PS C:\>Remove-AzureStorageContainer -Name "MyTestContainer"
```

<span data-ttu-id="15af5-109">這個範例會移除名為 MyTestContainer 的容器。</span><span class="sxs-lookup"><span data-stu-id="15af5-109">This example removes a container named MyTestContainer.</span></span>

## <span data-ttu-id="15af5-110">參數</span><span class="sxs-lookup"><span data-stu-id="15af5-110">PARAMETERS</span></span>

### <span data-ttu-id="15af5-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="15af5-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="15af5-112">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="15af5-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="15af5-113">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="15af5-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="15af5-114">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="15af5-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="15af5-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="15af5-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="15af5-116">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="15af5-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="15af5-117">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="15af5-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="15af5-118">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="15af5-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="15af5-119">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="15af5-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="15af5-120">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="15af5-120">The default value is 10.</span></span>

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

### <span data-ttu-id="15af5-121">-內容</span><span class="sxs-lookup"><span data-stu-id="15af5-121">-Context</span></span>
<span data-ttu-id="15af5-122">指定您要移除之容器的內容。</span><span class="sxs-lookup"><span data-stu-id="15af5-122">Specifies a context for the container you want to remove.</span></span>
<span data-ttu-id="15af5-123">您可以使用 New-AzureStorageContext Cmdlet 來建立它。</span><span class="sxs-lookup"><span data-stu-id="15af5-123">You can use the New-AzureStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="15af5-124">-Force</span><span class="sxs-lookup"><span data-stu-id="15af5-124">-Force</span></span>
<span data-ttu-id="15af5-125">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="15af5-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="15af5-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="15af5-126">-Name</span></span>
<span data-ttu-id="15af5-127">指定要移除之容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="15af5-127">Specifies the name of the container to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15af5-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="15af5-128">-PassThru</span></span>
<span data-ttu-id="15af5-129">表示此 Cmdlet 會傳回反映操作成功的 **布林值** 。</span><span class="sxs-lookup"><span data-stu-id="15af5-129">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="15af5-130">根據預設，這個 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="15af5-130">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="15af5-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="15af5-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="15af5-132">指定要求的服務端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="15af5-132">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="15af5-133">如果所指定的間隔在服務處理要求之前就已到期，儲存服務就會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="15af5-133">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="15af5-134">-確認</span><span class="sxs-lookup"><span data-stu-id="15af5-134">-Confirm</span></span>
<span data-ttu-id="15af5-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="15af5-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15af5-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15af5-136">-WhatIf</span></span>
<span data-ttu-id="15af5-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="15af5-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15af5-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="15af5-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15af5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15af5-139">CommonParameters</span></span>
<span data-ttu-id="15af5-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="15af5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15af5-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="15af5-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15af5-142">輸入</span><span class="sxs-lookup"><span data-stu-id="15af5-142">INPUTS</span></span>

### <span data-ttu-id="15af5-143">IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="15af5-143">IStorageContext</span></span>

<span data-ttu-id="15af5-144">參數「CoNtext」接受來自管線的 "IStorageCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="15af5-144">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="15af5-145">字串</span><span class="sxs-lookup"><span data-stu-id="15af5-145">String</span></span>

<span data-ttu-id="15af5-146">形參 "Name" 接受管線中類型 "String" 的值</span><span class="sxs-lookup"><span data-stu-id="15af5-146">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="15af5-147">輸出</span><span class="sxs-lookup"><span data-stu-id="15af5-147">OUTPUTS</span></span>

### <span data-ttu-id="15af5-148">System.object</span><span class="sxs-lookup"><span data-stu-id="15af5-148">System.Boolean</span></span>

## <span data-ttu-id="15af5-149">筆記</span><span class="sxs-lookup"><span data-stu-id="15af5-149">NOTES</span></span>

## <span data-ttu-id="15af5-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="15af5-150">RELATED LINKS</span></span>

[<span data-ttu-id="15af5-151">AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="15af5-151">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="15af5-152">新-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="15af5-152">New-AzureStorageContainer</span></span>](./New-AzureStorageContainer.md)
