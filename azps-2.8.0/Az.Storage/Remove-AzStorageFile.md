---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 811671E9-592E-4E58-8174-34D665206A65
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageFile.md
ms.openlocfilehash: 0b8adb43c8ae83afe0d8053d8367c8bf8152b233
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792897"
---
# <span data-ttu-id="47941-101">Remove-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="47941-101">Remove-AzStorageFile</span></span>

## <span data-ttu-id="47941-102">摘要</span><span class="sxs-lookup"><span data-stu-id="47941-102">SYNOPSIS</span></span>
<span data-ttu-id="47941-103">刪除檔案。</span><span class="sxs-lookup"><span data-stu-id="47941-103">Deletes a file.</span></span>

## <span data-ttu-id="47941-104">句法</span><span class="sxs-lookup"><span data-stu-id="47941-104">SYNTAX</span></span>

### <span data-ttu-id="47941-105">共用名稱 (預設) </span><span class="sxs-lookup"><span data-stu-id="47941-105">ShareName (Default)</span></span>
```
Remove-AzStorageFile [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="47941-106">共用</span><span class="sxs-lookup"><span data-stu-id="47941-106">Share</span></span>
```
Remove-AzStorageFile [-Share] <CloudFileShare> [-Path] <String> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47941-107">空目錄</span><span class="sxs-lookup"><span data-stu-id="47941-107">Directory</span></span>
```
Remove-AzStorageFile [-Directory] <CloudFileDirectory> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="47941-108">檔案</span><span class="sxs-lookup"><span data-stu-id="47941-108">File</span></span>
```
Remove-AzStorageFile [-File] <CloudFile> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47941-109">說明</span><span class="sxs-lookup"><span data-stu-id="47941-109">DESCRIPTION</span></span>
<span data-ttu-id="47941-110">**AzStorageFile** Cmdlet 會刪除檔案。</span><span class="sxs-lookup"><span data-stu-id="47941-110">The **Remove-AzStorageFile** cmdlet deletes a file.</span></span>

## <span data-ttu-id="47941-111">示例</span><span class="sxs-lookup"><span data-stu-id="47941-111">EXAMPLES</span></span>

### <span data-ttu-id="47941-112">範例1：從檔案共用中刪除檔案</span><span class="sxs-lookup"><span data-stu-id="47941-112">Example 1: Delete a file from a file share</span></span>
```
PS C:\>Remove-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoFile22"
```

<span data-ttu-id="47941-113">這個命令會從名為 ContosoShare06 的檔案共用中刪除名為 ContosoFile22 的檔案。</span><span class="sxs-lookup"><span data-stu-id="47941-113">This command deletes the file that is named ContosoFile22 from the file share named ContosoShare06.</span></span>

### <span data-ttu-id="47941-114">範例2：使用檔案共用物件從檔案共用取得檔案</span><span class="sxs-lookup"><span data-stu-id="47941-114">Example 2: Get a file from a file share by using a file share object</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" | Remove-AzStorageFile -Path "ContosoFile22"
```

<span data-ttu-id="47941-115">這個命令會使用 **AzStorageShare** Cmdlet 來取得名為 ContosoShare06 的檔案共用，然後使用管線運算子將該物件傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="47941-115">This command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="47941-116">目前的命令會從 ContosoShare06 中刪除名為 ContosoFile22 的檔案。</span><span class="sxs-lookup"><span data-stu-id="47941-116">The current command deletes the file that is named ContosoFile22 from ContosoShare06.</span></span>

## <span data-ttu-id="47941-117">參數</span><span class="sxs-lookup"><span data-stu-id="47941-117">PARAMETERS</span></span>

### <span data-ttu-id="47941-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="47941-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="47941-119">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="47941-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="47941-120">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="47941-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="47941-121">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="47941-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="47941-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="47941-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="47941-123">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="47941-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="47941-124">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="47941-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="47941-125">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="47941-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="47941-126">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="47941-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="47941-127">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="47941-127">The default value is 10.</span></span>

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

### <span data-ttu-id="47941-128">-內容</span><span class="sxs-lookup"><span data-stu-id="47941-128">-Context</span></span>
<span data-ttu-id="47941-129">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="47941-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="47941-130">若要取得儲存內容，請使用 [AzStorageCoNtext](./New-AzStorageContext.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="47941-130">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="47941-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47941-131">-DefaultProfile</span></span>
<span data-ttu-id="47941-132">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="47941-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47941-133">-Directory</span><span class="sxs-lookup"><span data-stu-id="47941-133">-Directory</span></span>
<span data-ttu-id="47941-134">將資料夾指定為 **CloudFileDirectory** 物件。</span><span class="sxs-lookup"><span data-stu-id="47941-134">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="47941-135">這個 Cmdlet 會移除此參數指定資料夾中的檔案。</span><span class="sxs-lookup"><span data-stu-id="47941-135">This cmdlet removes a file in the folder that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47941-136">檔案</span><span class="sxs-lookup"><span data-stu-id="47941-136">-File</span></span>
<span data-ttu-id="47941-137">將檔案指定為 **CloudFile** 物件。</span><span class="sxs-lookup"><span data-stu-id="47941-137">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="47941-138">這個 Cmdlet 會移除此參數指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="47941-138">This cmdlet removes the file that this parameter specifies.</span></span>
<span data-ttu-id="47941-139">若要取得 **CloudFile** 物件，請使用 Get-AzStorageFile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="47941-139">To obtain a **CloudFile** object, use the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47941-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="47941-140">-PassThru</span></span>
<span data-ttu-id="47941-141">表示此 Cmdlet 會傳回反映操作成功的 **布林值** 。</span><span class="sxs-lookup"><span data-stu-id="47941-141">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="47941-142">根據預設，這個 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="47941-142">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="47941-143">-Path</span><span class="sxs-lookup"><span data-stu-id="47941-143">-Path</span></span>
<span data-ttu-id="47941-144">指定檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="47941-144">Specifies the path of a file.</span></span>
<span data-ttu-id="47941-145">這個 Cmdlet 會刪除此參數指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="47941-145">This cmdlet deletes the file that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, Share, Directory
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47941-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="47941-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="47941-147">指定要求中伺服器部分的超時時間長度。</span><span class="sxs-lookup"><span data-stu-id="47941-147">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="47941-148">-共用</span><span class="sxs-lookup"><span data-stu-id="47941-148">-Share</span></span>
<span data-ttu-id="47941-149">指定 **CloudFileShare** 物件。</span><span class="sxs-lookup"><span data-stu-id="47941-149">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="47941-150">這個 Cmdlet 會移除此參數指定的共用中的檔案。</span><span class="sxs-lookup"><span data-stu-id="47941-150">This cmdlet removes the file in the share this parameter specifies.</span></span>
<span data-ttu-id="47941-151">若要取得 **CloudFileShare** 物件，請使用 Get-AzStorageShare Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="47941-151">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="47941-152">此物件包含儲存內容。</span><span class="sxs-lookup"><span data-stu-id="47941-152">This object contains the storage context.</span></span>
<span data-ttu-id="47941-153">如果您指定此參數，請勿指定 *CoNtext* 參數。</span><span class="sxs-lookup"><span data-stu-id="47941-153">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="47941-154">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="47941-154">-ShareName</span></span>
<span data-ttu-id="47941-155">指定檔案共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="47941-155">Specifies the name of the file share.</span></span>
<span data-ttu-id="47941-156">這個 Cmdlet 會移除此參數指定的共用中的檔案。</span><span class="sxs-lookup"><span data-stu-id="47941-156">This cmdlet removes the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="47941-157">-確認</span><span class="sxs-lookup"><span data-stu-id="47941-157">-Confirm</span></span>
<span data-ttu-id="47941-158">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="47941-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47941-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47941-159">-WhatIf</span></span>
<span data-ttu-id="47941-160">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="47941-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47941-161">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="47941-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47941-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47941-162">CommonParameters</span></span>
<span data-ttu-id="47941-163">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="47941-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47941-164">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="47941-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47941-165">輸入</span><span class="sxs-lookup"><span data-stu-id="47941-165">INPUTS</span></span>

### <span data-ttu-id="47941-166">CloudFileShare （即 Azure）</span><span class="sxs-lookup"><span data-stu-id="47941-166">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="47941-167">CloudFileDirectory （即 Azure）</span><span class="sxs-lookup"><span data-stu-id="47941-167">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="47941-168">CloudFile （即 Azure）</span><span class="sxs-lookup"><span data-stu-id="47941-168">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="47941-169">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="47941-169">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="47941-170">輸出</span><span class="sxs-lookup"><span data-stu-id="47941-170">OUTPUTS</span></span>

### <span data-ttu-id="47941-171">CloudFile （即 Azure）</span><span class="sxs-lookup"><span data-stu-id="47941-171">Microsoft.Azure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="47941-172">筆記</span><span class="sxs-lookup"><span data-stu-id="47941-172">NOTES</span></span>

## <span data-ttu-id="47941-173">相關連結</span><span class="sxs-lookup"><span data-stu-id="47941-173">RELATED LINKS</span></span>

[<span data-ttu-id="47941-174">AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="47941-174">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="47941-175">AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="47941-175">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="47941-176">新-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="47941-176">New-AzStorageContext</span></span>](./New-AzStorageContext.md)
