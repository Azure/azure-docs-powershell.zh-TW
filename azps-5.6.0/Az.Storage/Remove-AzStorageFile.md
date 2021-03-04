---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 811671E9-592E-4E58-8174-34D665206A65
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageFile.md
ms.openlocfilehash: f0a6352c8a9bbe20130924ce62b20c46fc005290
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908709"
---
# <span data-ttu-id="cf3c8-101">Remove-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="cf3c8-101">Remove-AzStorageFile</span></span>

## <span data-ttu-id="cf3c8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cf3c8-102">SYNOPSIS</span></span>
<span data-ttu-id="cf3c8-103">刪除檔案。</span><span class="sxs-lookup"><span data-stu-id="cf3c8-103">Deletes a file.</span></span>

## <span data-ttu-id="cf3c8-104">語法</span><span class="sxs-lookup"><span data-stu-id="cf3c8-104">SYNTAX</span></span>

### <span data-ttu-id="cf3c8-105">ShareName (預設) </span><span class="sxs-lookup"><span data-stu-id="cf3c8-105">ShareName (Default)</span></span>
```
Remove-AzStorageFile [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cf3c8-106">共用</span><span class="sxs-lookup"><span data-stu-id="cf3c8-106">Share</span></span>
```
Remove-AzStorageFile [-Share] <CloudFileShare> [-Path] <String> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf3c8-107">目錄</span><span class="sxs-lookup"><span data-stu-id="cf3c8-107">Directory</span></span>
```
Remove-AzStorageFile [-Directory] <CloudFileDirectory> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cf3c8-108">檔</span><span class="sxs-lookup"><span data-stu-id="cf3c8-108">File</span></span>
```
Remove-AzStorageFile [-File] <CloudFile> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf3c8-109">描述</span><span class="sxs-lookup"><span data-stu-id="cf3c8-109">DESCRIPTION</span></span>
<span data-ttu-id="cf3c8-110">**Remove-AzStorageFile** Cmdlet 會刪除檔案。</span><span class="sxs-lookup"><span data-stu-id="cf3c8-110">The **Remove-AzStorageFile** cmdlet deletes a file.</span></span>

## <span data-ttu-id="cf3c8-111">例子</span><span class="sxs-lookup"><span data-stu-id="cf3c8-111">EXAMPLES</span></span>

### <span data-ttu-id="cf3c8-112">範例 1：從檔案共用中刪除檔案</span><span class="sxs-lookup"><span data-stu-id="cf3c8-112">Example 1: Delete a file from a file share</span></span>
```
PS C:\>Remove-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoFile22"
```

<span data-ttu-id="cf3c8-113">此命令會從名為 ContosoShare06 的檔案共用中刪除名為 ContosoFile22 的檔案。</span><span class="sxs-lookup"><span data-stu-id="cf3c8-113">This command deletes the file that is named ContosoFile22 from the file share named ContosoShare06.</span></span>

### <span data-ttu-id="cf3c8-114">範例 2：使用檔案共用物件從檔案共用取得檔案</span><span class="sxs-lookup"><span data-stu-id="cf3c8-114">Example 2: Get a file from a file share by using a file share object</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" | Remove-AzStorageFile -Path "ContosoFile22"
```

<span data-ttu-id="cf3c8-115">此命令使用 **Get-AzStorageShare** Cmdlet 取得名為 ContosoShare06 的檔案共用，然後使用管線運算子將該物件傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cf3c8-115">This command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="cf3c8-116">目前的命令會從 ContosoShare06 刪除名為 ContosoFile22 的檔案。</span><span class="sxs-lookup"><span data-stu-id="cf3c8-116">The current command deletes the file that is named ContosoFile22 from ContosoShare06.</span></span>

## <span data-ttu-id="cf3c8-117">參數</span><span class="sxs-lookup"><span data-stu-id="cf3c8-117">PARAMETERS</span></span>

### <span data-ttu-id="cf3c8-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cf3c8-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="cf3c8-119">指定一個服務要求用戶端的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="cf3c8-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="cf3c8-120">如果前一個通話在指定的時間間隔內失敗，此 Cmdlet 會重新重試要求。</span><span class="sxs-lookup"><span data-stu-id="cf3c8-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="cf3c8-121">如果此 Cmdlet 在間隔經過之前未收到成功回應，此 Cmdlet 會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="cf3c8-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="cf3c8-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="cf3c8-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="cf3c8-123">指定同時進行的最大網路通話數。</span><span class="sxs-lookup"><span data-stu-id="cf3c8-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="cf3c8-124">您可以使用此參數來限制並行，以節流本地 CPU 和頻寬使用量，方法為指定並行網路通話的數量上限。</span><span class="sxs-lookup"><span data-stu-id="cf3c8-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="cf3c8-125">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="cf3c8-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="cf3c8-126">此參數有助於減少低頻寬環境的網路連接問題，例如每秒 100 KB。</span><span class="sxs-lookup"><span data-stu-id="cf3c8-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="cf3c8-127">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="cf3c8-127">The default value is 10.</span></span>

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

### <span data-ttu-id="cf3c8-128">-內容</span><span class="sxs-lookup"><span data-stu-id="cf3c8-128">-Context</span></span>
<span data-ttu-id="cf3c8-129">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="cf3c8-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="cf3c8-130">若要取得儲存內容，請使用 [New-AzStorageCoNtext](./New-AzStorageContext.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cf3c8-130">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="cf3c8-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf3c8-131">-DefaultProfile</span></span>
<span data-ttu-id="cf3c8-132">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="cf3c8-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf3c8-133">-目錄</span><span class="sxs-lookup"><span data-stu-id="cf3c8-133">-Directory</span></span>
<span data-ttu-id="cf3c8-134">將資料夾指定為 **CloudFileDirectory** 物件。</span><span class="sxs-lookup"><span data-stu-id="cf3c8-134">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="cf3c8-135">此 Cmdlet 會移除此參數指定之資料夾中的檔案。</span><span class="sxs-lookup"><span data-stu-id="cf3c8-135">This cmdlet removes a file in the folder that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases: CloudFileDirectory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf3c8-136">-檔案</span><span class="sxs-lookup"><span data-stu-id="cf3c8-136">-File</span></span>
<span data-ttu-id="cf3c8-137">將檔案指定為 **CloudFile** 物件。</span><span class="sxs-lookup"><span data-stu-id="cf3c8-137">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="cf3c8-138">此 Cmdlet 會移除此參數指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="cf3c8-138">This cmdlet removes the file that this parameter specifies.</span></span>
<span data-ttu-id="cf3c8-139">若要取得 **CloudFile** 物件，請使用 Get-AzStorageFile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cf3c8-139">To obtain a **CloudFile** object, use the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases: CloudFile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf3c8-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cf3c8-140">-PassThru</span></span>
<span data-ttu-id="cf3c8-141">表示此 Cmdlet 會返回 **反映** 作業成功的布林值。</span><span class="sxs-lookup"><span data-stu-id="cf3c8-141">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="cf3c8-142">根據預設，此 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="cf3c8-142">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="cf3c8-143">-路徑</span><span class="sxs-lookup"><span data-stu-id="cf3c8-143">-Path</span></span>
<span data-ttu-id="cf3c8-144">指定檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="cf3c8-144">Specifies the path of a file.</span></span>
<span data-ttu-id="cf3c8-145">此 Cmdlet 會刪除此參數指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="cf3c8-145">This cmdlet deletes the file that this parameter specifies.</span></span>

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

### <span data-ttu-id="cf3c8-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cf3c8-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="cf3c8-147">指定要求的伺服器部分之時間長度。</span><span class="sxs-lookup"><span data-stu-id="cf3c8-147">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="cf3c8-148">-共用</span><span class="sxs-lookup"><span data-stu-id="cf3c8-148">-Share</span></span>
<span data-ttu-id="cf3c8-149">指定 **CloudFileShare** 物件。</span><span class="sxs-lookup"><span data-stu-id="cf3c8-149">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="cf3c8-150">此 Cmdlet 會移除此參數指定之共用中的檔案。</span><span class="sxs-lookup"><span data-stu-id="cf3c8-150">This cmdlet removes the file in the share this parameter specifies.</span></span>
<span data-ttu-id="cf3c8-151">若要取得 **CloudFileShare** 物件，請使用 Get-AzStorageShare Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cf3c8-151">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="cf3c8-152">此物件包含儲存內容。</span><span class="sxs-lookup"><span data-stu-id="cf3c8-152">This object contains the storage context.</span></span>
<span data-ttu-id="cf3c8-153">如果您指定此參數，請勿指定 *CoNtext* 參數。</span><span class="sxs-lookup"><span data-stu-id="cf3c8-153">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="cf3c8-154">-ShareName</span><span class="sxs-lookup"><span data-stu-id="cf3c8-154">-ShareName</span></span>
<span data-ttu-id="cf3c8-155">指定檔案共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="cf3c8-155">Specifies the name of the file share.</span></span>
<span data-ttu-id="cf3c8-156">此 Cmdlet 會移除此參數指定之共用中的檔案。</span><span class="sxs-lookup"><span data-stu-id="cf3c8-156">This cmdlet removes the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="cf3c8-157">-確認</span><span class="sxs-lookup"><span data-stu-id="cf3c8-157">-Confirm</span></span>
<span data-ttu-id="cf3c8-158">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="cf3c8-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf3c8-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf3c8-159">-WhatIf</span></span>
<span data-ttu-id="cf3c8-160">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cf3c8-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf3c8-161">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cf3c8-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf3c8-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf3c8-162">CommonParameters</span></span>
<span data-ttu-id="cf3c8-163">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cf3c8-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf3c8-164">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="cf3c8-164">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf3c8-165">輸入</span><span class="sxs-lookup"><span data-stu-id="cf3c8-165">INPUTS</span></span>

### <span data-ttu-id="cf3c8-166">Microsoft.Azure.storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="cf3c8-166">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="cf3c8-167">Microsoft.Azure.storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="cf3c8-167">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="cf3c8-168">Microsoft.Azure.storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="cf3c8-168">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="cf3c8-169">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="cf3c8-169">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="cf3c8-170">輸出</span><span class="sxs-lookup"><span data-stu-id="cf3c8-170">OUTPUTS</span></span>

### <span data-ttu-id="cf3c8-171">Microsoft.WindowsAzure.Commands.Common.storage.ResourceModel.AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="cf3c8-171">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="cf3c8-172">筆記</span><span class="sxs-lookup"><span data-stu-id="cf3c8-172">NOTES</span></span>

## <span data-ttu-id="cf3c8-173">相關連結</span><span class="sxs-lookup"><span data-stu-id="cf3c8-173">RELATED LINKS</span></span>

[<span data-ttu-id="cf3c8-174">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="cf3c8-174">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="cf3c8-175">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="cf3c8-175">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="cf3c8-176">New-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="cf3c8-176">New-AzStorageContext</span></span>](./New-AzStorageContext.md)
