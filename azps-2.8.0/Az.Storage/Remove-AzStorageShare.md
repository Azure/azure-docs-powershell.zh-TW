---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FF3AD436-CA33-4A52-8580-D2345D80A231
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShare.md
ms.openlocfilehash: 05cb1fcbad453704a5295b38c8f0be3b1614f237
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793138"
---
# <span data-ttu-id="40534-101">Remove-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="40534-101">Remove-AzStorageShare</span></span>

## <span data-ttu-id="40534-102">摘要</span><span class="sxs-lookup"><span data-stu-id="40534-102">SYNOPSIS</span></span>
<span data-ttu-id="40534-103">刪除檔案共用。</span><span class="sxs-lookup"><span data-stu-id="40534-103">Deletes a file share.</span></span>

## <span data-ttu-id="40534-104">句法</span><span class="sxs-lookup"><span data-stu-id="40534-104">SYNTAX</span></span>

### <span data-ttu-id="40534-105">共用名稱 (預設) </span><span class="sxs-lookup"><span data-stu-id="40534-105">ShareName (Default)</span></span>
```
Remove-AzStorageShare [-Name] <String> [-IncludeAllSnapshot] [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="40534-106">共用</span><span class="sxs-lookup"><span data-stu-id="40534-106">Share</span></span>
```
Remove-AzStorageShare [-Share] <CloudFileShare> [-IncludeAllSnapshot] [-Force] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="40534-107">說明</span><span class="sxs-lookup"><span data-stu-id="40534-107">DESCRIPTION</span></span>
<span data-ttu-id="40534-108">**AzStorageShare** Cmdlet 會刪除檔案共用。</span><span class="sxs-lookup"><span data-stu-id="40534-108">The **Remove-AzStorageShare** cmdlet deletes a file share.</span></span>

## <span data-ttu-id="40534-109">示例</span><span class="sxs-lookup"><span data-stu-id="40534-109">EXAMPLES</span></span>

### <span data-ttu-id="40534-110">範例1：移除檔案共用</span><span class="sxs-lookup"><span data-stu-id="40534-110">Example 1: Remove a file share</span></span>
```
PS C:\>Remove-AzStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="40534-111">這個命令會移除名為 ContosoShare06 的檔案共用。</span><span class="sxs-lookup"><span data-stu-id="40534-111">This command removes the file share named ContosoShare06.</span></span>

### <span data-ttu-id="40534-112">範例2：移除檔案共用及其所有快照</span><span class="sxs-lookup"><span data-stu-id="40534-112">Example 2: Remove a file share and all its snapshots</span></span>
```
PS C:\>Remove-AzStorageShare -Name "ContosoShare06" -IncludeAllSnapshot
```

<span data-ttu-id="40534-113">這個命令會移除名為 ContosoShare06 的檔案共用及其所有快照。</span><span class="sxs-lookup"><span data-stu-id="40534-113">This command removes the file share named ContosoShare06 and all its snapshots.</span></span>

## <span data-ttu-id="40534-114">參數</span><span class="sxs-lookup"><span data-stu-id="40534-114">PARAMETERS</span></span>

### <span data-ttu-id="40534-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="40534-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="40534-116">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="40534-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="40534-117">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="40534-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="40534-118">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="40534-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="40534-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="40534-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="40534-120">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="40534-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="40534-121">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="40534-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="40534-122">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="40534-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="40534-123">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="40534-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="40534-124">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="40534-124">The default value is 10.</span></span>

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

### <span data-ttu-id="40534-125">-內容</span><span class="sxs-lookup"><span data-stu-id="40534-125">-Context</span></span>
<span data-ttu-id="40534-126">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="40534-126">Specifies an Azure storage context.</span></span>
<span data-ttu-id="40534-127">若要取得儲存內容，請使用 [AzStorageCoNtext](./New-AzStorageContext.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="40534-127">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40534-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40534-128">-DefaultProfile</span></span>
<span data-ttu-id="40534-129">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="40534-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40534-130">-Force</span><span class="sxs-lookup"><span data-stu-id="40534-130">-Force</span></span>
<span data-ttu-id="40534-131">強制移除所有快照的共用，以及所有內容。</span><span class="sxs-lookup"><span data-stu-id="40534-131">Force to remove the share with all of its snapshots, and all content.</span></span>

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

### <span data-ttu-id="40534-132">-IncludeAllSnapshot</span><span class="sxs-lookup"><span data-stu-id="40534-132">-IncludeAllSnapshot</span></span>
<span data-ttu-id="40534-133">移除檔案共用及其所有快照</span><span class="sxs-lookup"><span data-stu-id="40534-133">Remove File Share with all of its snapshots</span></span>

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

### <span data-ttu-id="40534-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="40534-134">-Name</span></span>
<span data-ttu-id="40534-135">指定檔案共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="40534-135">Specifies the name of the file share.</span></span>
<span data-ttu-id="40534-136">這個 Cmdlet 會刪除此參數指定的檔案共用。</span><span class="sxs-lookup"><span data-stu-id="40534-136">This cmdlet deletes the file share that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40534-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="40534-137">-PassThru</span></span>
<span data-ttu-id="40534-138">表示此 Cmdlet 會傳回反映操作成功的 **布林值** 。</span><span class="sxs-lookup"><span data-stu-id="40534-138">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="40534-139">根據預設，這個 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="40534-139">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="40534-140">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="40534-140">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="40534-141">指定要求中伺服器部分的超時時間長度。</span><span class="sxs-lookup"><span data-stu-id="40534-141">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="40534-142">-共用</span><span class="sxs-lookup"><span data-stu-id="40534-142">-Share</span></span>
<span data-ttu-id="40534-143">指定 **CloudFileShare** 物件。</span><span class="sxs-lookup"><span data-stu-id="40534-143">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="40534-144">這個 Cmdlet 會移除此參數指定的物件。</span><span class="sxs-lookup"><span data-stu-id="40534-144">This cmdlet removes the object that this parameter specifies.</span></span>
<span data-ttu-id="40534-145">若要取得 **CloudFileShare** 物件，請使用 Get-AzStorageShare Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="40534-145">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="40534-146">此物件包含儲存內容。</span><span class="sxs-lookup"><span data-stu-id="40534-146">This object contains the storage context.</span></span>
<span data-ttu-id="40534-147">如果您指定此參數，請勿指定 *CoNtext* 參數。</span><span class="sxs-lookup"><span data-stu-id="40534-147">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40534-148">-確認</span><span class="sxs-lookup"><span data-stu-id="40534-148">-Confirm</span></span>
<span data-ttu-id="40534-149">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="40534-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40534-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40534-150">-WhatIf</span></span>
<span data-ttu-id="40534-151">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="40534-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40534-152">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="40534-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40534-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40534-153">CommonParameters</span></span>
<span data-ttu-id="40534-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="40534-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40534-155">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="40534-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40534-156">輸入</span><span class="sxs-lookup"><span data-stu-id="40534-156">INPUTS</span></span>

### <span data-ttu-id="40534-157">System.object</span><span class="sxs-lookup"><span data-stu-id="40534-157">System.String</span></span>

### <span data-ttu-id="40534-158">CloudFileShare （即 Azure）</span><span class="sxs-lookup"><span data-stu-id="40534-158">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="40534-159">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="40534-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="40534-160">輸出</span><span class="sxs-lookup"><span data-stu-id="40534-160">OUTPUTS</span></span>

### <span data-ttu-id="40534-161">CloudFileShare （即 Azure）</span><span class="sxs-lookup"><span data-stu-id="40534-161">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

## <span data-ttu-id="40534-162">筆記</span><span class="sxs-lookup"><span data-stu-id="40534-162">NOTES</span></span>

## <span data-ttu-id="40534-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="40534-163">RELATED LINKS</span></span>

[<span data-ttu-id="40534-164">AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="40534-164">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="40534-165">新-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="40534-165">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="40534-166">新-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="40534-166">New-AzStorageShare</span></span>](./New-AzStorageShare.md)