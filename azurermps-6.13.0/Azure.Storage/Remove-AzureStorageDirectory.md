---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 53988D79-1F8B-4138-9F92-2912D418C121
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageDirectory.md
ms.openlocfilehash: 6df60027ff2c25a8f2c1c948d04213cfc6d6158e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445855"
---
# <span data-ttu-id="a994a-101">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="a994a-101">Remove-AzureStorageDirectory</span></span>

## <span data-ttu-id="a994a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a994a-102">SYNOPSIS</span></span>
<span data-ttu-id="a994a-103">刪除目錄。</span><span class="sxs-lookup"><span data-stu-id="a994a-103">Deletes a directory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a994a-104">句法</span><span class="sxs-lookup"><span data-stu-id="a994a-104">SYNTAX</span></span>

### <span data-ttu-id="a994a-105">共用名稱 (預設) </span><span class="sxs-lookup"><span data-stu-id="a994a-105">ShareName (Default)</span></span>
```
Remove-AzureStorageDirectory [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a994a-106">共用</span><span class="sxs-lookup"><span data-stu-id="a994a-106">Share</span></span>
```
Remove-AzureStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a994a-107">空目錄</span><span class="sxs-lookup"><span data-stu-id="a994a-107">Directory</span></span>
```
Remove-AzureStorageDirectory [-Directory] <CloudFileDirectory> [[-Path] <String>] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a994a-108">說明</span><span class="sxs-lookup"><span data-stu-id="a994a-108">DESCRIPTION</span></span>
<span data-ttu-id="a994a-109">**AzureStorageDirectory** Cmdlet 會刪除目錄。</span><span class="sxs-lookup"><span data-stu-id="a994a-109">The **Remove-AzureStorageDirectory** cmdlet deletes a directory.</span></span>

## <span data-ttu-id="a994a-110">示例</span><span class="sxs-lookup"><span data-stu-id="a994a-110">EXAMPLES</span></span>

### <span data-ttu-id="a994a-111">範例1：刪除資料夾</span><span class="sxs-lookup"><span data-stu-id="a994a-111">Example 1: Delete a folder</span></span>
```
PS C:\>Remove-AzureStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="a994a-112">這個命令會從名為 ContosoShare06 的檔案共用中刪除名為 ContosoWorkingFolder 的資料夾。</span><span class="sxs-lookup"><span data-stu-id="a994a-112">This command deletes the folder named ContosoWorkingFolder from the file share named ContosoShare06.</span></span>

## <span data-ttu-id="a994a-113">參數</span><span class="sxs-lookup"><span data-stu-id="a994a-113">PARAMETERS</span></span>

### <span data-ttu-id="a994a-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a994a-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a994a-115">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="a994a-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="a994a-116">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="a994a-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="a994a-117">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="a994a-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="a994a-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a994a-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a994a-119">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="a994a-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="a994a-120">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="a994a-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="a994a-121">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="a994a-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="a994a-122">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="a994a-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="a994a-123">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="a994a-123">The default value is 10.</span></span>

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

### <span data-ttu-id="a994a-124">-內容</span><span class="sxs-lookup"><span data-stu-id="a994a-124">-Context</span></span>
<span data-ttu-id="a994a-125">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="a994a-125">Specifies an Azure storage context.</span></span>
<span data-ttu-id="a994a-126">若要取得儲存內容，請使用 [AzureStorageCoNtext](./New-AzureStorageContext.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a994a-126">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="a994a-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a994a-127">-DefaultProfile</span></span>
<span data-ttu-id="a994a-128">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a994a-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a994a-129">-Directory</span><span class="sxs-lookup"><span data-stu-id="a994a-129">-Directory</span></span>
<span data-ttu-id="a994a-130">將資料夾指定為 **CloudFileDirectory** 物件。</span><span class="sxs-lookup"><span data-stu-id="a994a-130">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="a994a-131">這個 Cmdlet 會移除此參數指定的資料夾。</span><span class="sxs-lookup"><span data-stu-id="a994a-131">This cmdlet removes the folder that this parameter specifies.</span></span>
<span data-ttu-id="a994a-132">若要取得目錄，請使用 New-AzureStorageDirectory Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a994a-132">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="a994a-133">您也可以使用 **AzureStorageFile** Cmdlet 來取得目錄。</span><span class="sxs-lookup"><span data-stu-id="a994a-133">You can also use the **Get-AzureStorageFile** cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a994a-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a994a-134">-PassThru</span></span>
<span data-ttu-id="a994a-135">表示如果此 Cmdlet 成功，則會傳回 $True 的值。</span><span class="sxs-lookup"><span data-stu-id="a994a-135">Indicates that, if this cmdlet succeeds, it returns a value of $True.</span></span>
<span data-ttu-id="a994a-136">如果您指定此參數，且由於 _Path_ 參數不適當的值而使 Cmdlet 不成功，則 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="a994a-136">If you specify this parameter, and if the cmdlet is unsuccessful because of an inappropriate value for the _Path_ parameter, the cmdlet returns an error.</span></span>
<span data-ttu-id="a994a-137">如果您沒有指定此參數，這個 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="a994a-137">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="a994a-138">-Path</span><span class="sxs-lookup"><span data-stu-id="a994a-138">-Path</span></span>
<span data-ttu-id="a994a-139">指定資料夾的路徑。</span><span class="sxs-lookup"><span data-stu-id="a994a-139">Specifies the path of a folder.</span></span>
<span data-ttu-id="a994a-140">如果此參數指定的資料夾為空白，這個 Cmdlet 會刪除該資料夾。</span><span class="sxs-lookup"><span data-stu-id="a994a-140">If the folder that this parameter specifies is empty, this cmdlet deletes that folder.</span></span>
<span data-ttu-id="a994a-141">如果資料夾不是空白，這個 Cmdlet 不會變更，而會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="a994a-141">If the folder is not empty, this cmdlet makes no change, and returns an error.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, Share
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Directory
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a994a-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a994a-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a994a-143">指定要求中伺服器部分的超時時間長度。</span><span class="sxs-lookup"><span data-stu-id="a994a-143">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="a994a-144">-共用</span><span class="sxs-lookup"><span data-stu-id="a994a-144">-Share</span></span>
<span data-ttu-id="a994a-145">指定 **CloudFileShare** 物件。</span><span class="sxs-lookup"><span data-stu-id="a994a-145">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="a994a-146">這個 Cmdlet 會移除此參數指定之檔案共用底下的資料夾。</span><span class="sxs-lookup"><span data-stu-id="a994a-146">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>
<span data-ttu-id="a994a-147">若要取得 **CloudFileShare** 物件，請使用 Get-AzureStorageShare Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a994a-147">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="a994a-148">此物件包含儲存內容。</span><span class="sxs-lookup"><span data-stu-id="a994a-148">This object contains the storage context.</span></span>
<span data-ttu-id="a994a-149">如果您指定此參數，請勿指定 *CoNtext* 參數。</span><span class="sxs-lookup"><span data-stu-id="a994a-149">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a994a-150">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="a994a-150">-ShareName</span></span>
<span data-ttu-id="a994a-151">指定檔案共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="a994a-151">Specifies the name of the file share.</span></span>
<span data-ttu-id="a994a-152">這個 Cmdlet 會移除此參數指定之檔案共用底下的資料夾。</span><span class="sxs-lookup"><span data-stu-id="a994a-152">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a994a-153">-確認</span><span class="sxs-lookup"><span data-stu-id="a994a-153">-Confirm</span></span>
<span data-ttu-id="a994a-154">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a994a-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a994a-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a994a-155">-WhatIf</span></span>
<span data-ttu-id="a994a-156">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a994a-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a994a-157">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a994a-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a994a-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a994a-158">CommonParameters</span></span>
<span data-ttu-id="a994a-159">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a994a-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a994a-160">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a994a-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a994a-161">輸入</span><span class="sxs-lookup"><span data-stu-id="a994a-161">INPUTS</span></span>

### <span data-ttu-id="a994a-162">[WindowsAzure] CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="a994a-162">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="a994a-163">參數：共用 (ByValue) </span><span class="sxs-lookup"><span data-stu-id="a994a-163">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="a994a-164">[WindowsAzure] CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="a994a-164">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>
<span data-ttu-id="a994a-165">參數：目錄 (ByValue) </span><span class="sxs-lookup"><span data-stu-id="a994a-165">Parameters: Directory (ByValue)</span></span>

### <span data-ttu-id="a994a-166">System.object</span><span class="sxs-lookup"><span data-stu-id="a994a-166">System.String</span></span>

### <span data-ttu-id="a994a-167">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="a994a-167">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a994a-168">輸出</span><span class="sxs-lookup"><span data-stu-id="a994a-168">OUTPUTS</span></span>

### <span data-ttu-id="a994a-169">[WindowsAzure] CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="a994a-169">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>

## <span data-ttu-id="a994a-170">筆記</span><span class="sxs-lookup"><span data-stu-id="a994a-170">NOTES</span></span>

## <span data-ttu-id="a994a-171">相關連結</span><span class="sxs-lookup"><span data-stu-id="a994a-171">RELATED LINKS</span></span>

[<span data-ttu-id="a994a-172">AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="a994a-172">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="a994a-173">新-AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="a994a-173">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="a994a-174">新-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="a994a-174">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)
