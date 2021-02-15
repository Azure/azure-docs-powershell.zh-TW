---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FF3AD436-CA33-4A52-8580-D2345D80A231
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShare.md
ms.openlocfilehash: d51980303d4cb0bcd3ba7ec9e4f976634d37c689
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142420"
---
# <span data-ttu-id="dbedf-101">Remove-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="dbedf-101">Remove-AzStorageShare</span></span>

## <span data-ttu-id="dbedf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dbedf-102">SYNOPSIS</span></span>
<span data-ttu-id="dbedf-103">刪除檔案共用。</span><span class="sxs-lookup"><span data-stu-id="dbedf-103">Deletes a file share.</span></span>

## <span data-ttu-id="dbedf-104">句法</span><span class="sxs-lookup"><span data-stu-id="dbedf-104">SYNTAX</span></span>

### <span data-ttu-id="dbedf-105">共用名稱 (預設) </span><span class="sxs-lookup"><span data-stu-id="dbedf-105">ShareName (Default)</span></span>
```
Remove-AzStorageShare [-Name] <String> [-IncludeAllSnapshot] [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dbedf-106">共用</span><span class="sxs-lookup"><span data-stu-id="dbedf-106">Share</span></span>
```
Remove-AzStorageShare [-Share] <CloudFileShare> [-IncludeAllSnapshot] [-Force] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dbedf-107">說明</span><span class="sxs-lookup"><span data-stu-id="dbedf-107">DESCRIPTION</span></span>
<span data-ttu-id="dbedf-108">**AzStorageShare** Cmdlet 會刪除檔案共用。</span><span class="sxs-lookup"><span data-stu-id="dbedf-108">The **Remove-AzStorageShare** cmdlet deletes a file share.</span></span>

## <span data-ttu-id="dbedf-109">示例</span><span class="sxs-lookup"><span data-stu-id="dbedf-109">EXAMPLES</span></span>

### <span data-ttu-id="dbedf-110">範例1：移除檔案共用</span><span class="sxs-lookup"><span data-stu-id="dbedf-110">Example 1: Remove a file share</span></span>
```
PS C:\>Remove-AzStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="dbedf-111">這個命令會移除名為 ContosoShare06 的檔案共用。</span><span class="sxs-lookup"><span data-stu-id="dbedf-111">This command removes the file share named ContosoShare06.</span></span>

### <span data-ttu-id="dbedf-112">範例2：移除檔案共用及其所有快照</span><span class="sxs-lookup"><span data-stu-id="dbedf-112">Example 2: Remove a file share and all its snapshots</span></span>
```
PS C:\>Remove-AzStorageShare -Name "ContosoShare06" -IncludeAllSnapshot
```

<span data-ttu-id="dbedf-113">這個命令會移除名為 ContosoShare06 的檔案共用及其所有快照。</span><span class="sxs-lookup"><span data-stu-id="dbedf-113">This command removes the file share named ContosoShare06 and all its snapshots.</span></span>

## <span data-ttu-id="dbedf-114">參數</span><span class="sxs-lookup"><span data-stu-id="dbedf-114">PARAMETERS</span></span>

### <span data-ttu-id="dbedf-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="dbedf-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="dbedf-116">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="dbedf-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="dbedf-117">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="dbedf-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="dbedf-118">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="dbedf-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="dbedf-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="dbedf-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="dbedf-120">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="dbedf-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="dbedf-121">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="dbedf-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="dbedf-122">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="dbedf-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="dbedf-123">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="dbedf-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="dbedf-124">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="dbedf-124">The default value is 10.</span></span>

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

### <span data-ttu-id="dbedf-125">-內容</span><span class="sxs-lookup"><span data-stu-id="dbedf-125">-Context</span></span>
<span data-ttu-id="dbedf-126">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="dbedf-126">Specifies an Azure storage context.</span></span>
<span data-ttu-id="dbedf-127">若要取得儲存內容，請使用 [AzStorageCoNtext](./New-AzStorageContext.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dbedf-127">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="dbedf-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbedf-128">-DefaultProfile</span></span>
<span data-ttu-id="dbedf-129">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dbedf-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbedf-130">-Force</span><span class="sxs-lookup"><span data-stu-id="dbedf-130">-Force</span></span>
<span data-ttu-id="dbedf-131">強制移除所有快照的共用，以及所有內容。</span><span class="sxs-lookup"><span data-stu-id="dbedf-131">Force to remove the share with all of its snapshots, and all content.</span></span>

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

### <span data-ttu-id="dbedf-132">-IncludeAllSnapshot</span><span class="sxs-lookup"><span data-stu-id="dbedf-132">-IncludeAllSnapshot</span></span>
<span data-ttu-id="dbedf-133">移除檔案共用及其所有快照</span><span class="sxs-lookup"><span data-stu-id="dbedf-133">Remove File Share with all of its snapshots</span></span>

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

### <span data-ttu-id="dbedf-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="dbedf-134">-Name</span></span>
<span data-ttu-id="dbedf-135">指定檔案共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="dbedf-135">Specifies the name of the file share.</span></span>
<span data-ttu-id="dbedf-136">這個 Cmdlet 會刪除此參數指定的檔案共用。</span><span class="sxs-lookup"><span data-stu-id="dbedf-136">This cmdlet deletes the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="dbedf-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dbedf-137">-PassThru</span></span>
<span data-ttu-id="dbedf-138">表示此 Cmdlet 會傳回反映操作成功的 **布林值** 。</span><span class="sxs-lookup"><span data-stu-id="dbedf-138">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="dbedf-139">根據預設，這個 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="dbedf-139">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="dbedf-140">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="dbedf-140">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="dbedf-141">指定要求中伺服器部分的超時時間長度。</span><span class="sxs-lookup"><span data-stu-id="dbedf-141">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="dbedf-142">-共用</span><span class="sxs-lookup"><span data-stu-id="dbedf-142">-Share</span></span>
<span data-ttu-id="dbedf-143">指定 **CloudFileShare** 物件。</span><span class="sxs-lookup"><span data-stu-id="dbedf-143">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="dbedf-144">這個 Cmdlet 會移除此參數指定的物件。</span><span class="sxs-lookup"><span data-stu-id="dbedf-144">This cmdlet removes the object that this parameter specifies.</span></span>
<span data-ttu-id="dbedf-145">若要取得 **CloudFileShare** 物件，請使用 Get-AzStorageShare Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dbedf-145">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="dbedf-146">此物件包含儲存內容。</span><span class="sxs-lookup"><span data-stu-id="dbedf-146">This object contains the storage context.</span></span>
<span data-ttu-id="dbedf-147">如果您指定此參數，請勿指定 *CoNtext* 參數。</span><span class="sxs-lookup"><span data-stu-id="dbedf-147">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dbedf-148">-確認</span><span class="sxs-lookup"><span data-stu-id="dbedf-148">-Confirm</span></span>
<span data-ttu-id="dbedf-149">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dbedf-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbedf-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbedf-150">-WhatIf</span></span>
<span data-ttu-id="dbedf-151">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dbedf-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbedf-152">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dbedf-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbedf-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbedf-153">CommonParameters</span></span>
<span data-ttu-id="dbedf-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dbedf-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbedf-155">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dbedf-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbedf-156">輸入</span><span class="sxs-lookup"><span data-stu-id="dbedf-156">INPUTS</span></span>

### <span data-ttu-id="dbedf-157">System.object</span><span class="sxs-lookup"><span data-stu-id="dbedf-157">System.String</span></span>

### <span data-ttu-id="dbedf-158">CloudFileShare （即 Azure）</span><span class="sxs-lookup"><span data-stu-id="dbedf-158">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="dbedf-159">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="dbedf-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="dbedf-160">輸出</span><span class="sxs-lookup"><span data-stu-id="dbedf-160">OUTPUTS</span></span>

### <span data-ttu-id="dbedf-161">AzureStorageFileShare WindowsAzure. ResourceModel。</span><span class="sxs-lookup"><span data-stu-id="dbedf-161">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span></span>

## <span data-ttu-id="dbedf-162">筆記</span><span class="sxs-lookup"><span data-stu-id="dbedf-162">NOTES</span></span>

## <span data-ttu-id="dbedf-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="dbedf-163">RELATED LINKS</span></span>

[<span data-ttu-id="dbedf-164">AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="dbedf-164">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="dbedf-165">新-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="dbedf-165">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="dbedf-166">新-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="dbedf-166">New-AzStorageShare</span></span>](./New-AzStorageShare.md)
