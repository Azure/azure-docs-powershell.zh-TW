---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 53988D79-1F8B-4138-9F92-2912D418C121
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageDirectory.md
ms.openlocfilehash: 87e8792697093182d3ccd36d75ac072239f76e89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908414"
---
# <span data-ttu-id="a3192-101">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="a3192-101">Remove-AzStorageDirectory</span></span>

## <span data-ttu-id="a3192-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a3192-102">SYNOPSIS</span></span>
<span data-ttu-id="a3192-103">刪除目錄。</span><span class="sxs-lookup"><span data-stu-id="a3192-103">Deletes a directory.</span></span>

## <span data-ttu-id="a3192-104">語法</span><span class="sxs-lookup"><span data-stu-id="a3192-104">SYNTAX</span></span>

### <span data-ttu-id="a3192-105">ShareName (預設) </span><span class="sxs-lookup"><span data-stu-id="a3192-105">ShareName (Default)</span></span>
```
Remove-AzStorageDirectory [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a3192-106">共用</span><span class="sxs-lookup"><span data-stu-id="a3192-106">Share</span></span>
```
Remove-AzStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a3192-107">目錄</span><span class="sxs-lookup"><span data-stu-id="a3192-107">Directory</span></span>
```
Remove-AzStorageDirectory [-Directory] <CloudFileDirectory> [[-Path] <String>] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a3192-108">描述</span><span class="sxs-lookup"><span data-stu-id="a3192-108">DESCRIPTION</span></span>
<span data-ttu-id="a3192-109">**Remove-AzStorageDirectory Cmdlet** 會刪除目錄。</span><span class="sxs-lookup"><span data-stu-id="a3192-109">The **Remove-AzStorageDirectory** cmdlet deletes a directory.</span></span>

## <span data-ttu-id="a3192-110">例子</span><span class="sxs-lookup"><span data-stu-id="a3192-110">EXAMPLES</span></span>

### <span data-ttu-id="a3192-111">範例 1：刪除資料夾</span><span class="sxs-lookup"><span data-stu-id="a3192-111">Example 1: Delete a folder</span></span>
```
PS C:\>Remove-AzStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="a3192-112">此命令會從名為 ContosoShare06 的檔案共用中刪除名為 ContosoWorkingFolder 的資料夾。</span><span class="sxs-lookup"><span data-stu-id="a3192-112">This command deletes the folder named ContosoWorkingFolder from the file share named ContosoShare06.</span></span>

## <span data-ttu-id="a3192-113">參數</span><span class="sxs-lookup"><span data-stu-id="a3192-113">PARAMETERS</span></span>

### <span data-ttu-id="a3192-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a3192-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a3192-115">指定一個服務要求用戶端的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="a3192-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="a3192-116">如果前一個通話在指定的時間間隔內失敗，此 Cmdlet 會重新重試要求。</span><span class="sxs-lookup"><span data-stu-id="a3192-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="a3192-117">如果此 Cmdlet 在間隔經過之前未收到成功回應，此 Cmdlet 會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="a3192-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="a3192-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a3192-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a3192-119">指定同時進行的最大網路通話數。</span><span class="sxs-lookup"><span data-stu-id="a3192-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="a3192-120">您可以使用此參數來限制並行，以節流本地 CPU 和頻寬使用量，方法為指定並行網路通話的數量上限。</span><span class="sxs-lookup"><span data-stu-id="a3192-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="a3192-121">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="a3192-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="a3192-122">此參數有助於減少低頻寬環境的網路連接問題，例如每秒 100 KB。</span><span class="sxs-lookup"><span data-stu-id="a3192-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="a3192-123">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="a3192-123">The default value is 10.</span></span>

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

### <span data-ttu-id="a3192-124">-內容</span><span class="sxs-lookup"><span data-stu-id="a3192-124">-Context</span></span>
<span data-ttu-id="a3192-125">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="a3192-125">Specifies an Azure storage context.</span></span>
<span data-ttu-id="a3192-126">若要取得儲存內容，請使用 [New-AzStorageCoNtext](./New-AzStorageContext.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a3192-126">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="a3192-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3192-127">-DefaultProfile</span></span>
<span data-ttu-id="a3192-128">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a3192-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3192-129">-目錄</span><span class="sxs-lookup"><span data-stu-id="a3192-129">-Directory</span></span>
<span data-ttu-id="a3192-130">將資料夾指定為 **CloudFileDirectory** 物件。</span><span class="sxs-lookup"><span data-stu-id="a3192-130">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="a3192-131">此 Cmdlet 會移除此參數指定的資料夾。</span><span class="sxs-lookup"><span data-stu-id="a3192-131">This cmdlet removes the folder that this parameter specifies.</span></span>
<span data-ttu-id="a3192-132">若要取得目錄，請使用 New-AzStorageDirectory Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a3192-132">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="a3192-133">您也可以使用 **Get-AzStorageFile** Cmdlet 取得目錄。</span><span class="sxs-lookup"><span data-stu-id="a3192-133">You can also use the **Get-AzStorageFile** cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="a3192-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a3192-134">-PassThru</span></span>
<span data-ttu-id="a3192-135">表示如果此 Cmdlet 成功，它會將值$True。</span><span class="sxs-lookup"><span data-stu-id="a3192-135">Indicates that, if this cmdlet succeeds, it returns a value of $True.</span></span>
<span data-ttu-id="a3192-136">如果您指定此參數，而且如果 Cmdlet 因為 _Path_ 參數的值不當而失敗，Cmdlet 會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="a3192-136">If you specify this parameter, and if the cmdlet is unsuccessful because of an inappropriate value for the _Path_ parameter, the cmdlet returns an error.</span></span>
<span data-ttu-id="a3192-137">如果您未指定此參數，此 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="a3192-137">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="a3192-138">-路徑</span><span class="sxs-lookup"><span data-stu-id="a3192-138">-Path</span></span>
<span data-ttu-id="a3192-139">指定資料夾的路徑。</span><span class="sxs-lookup"><span data-stu-id="a3192-139">Specifies the path of a folder.</span></span>
<span data-ttu-id="a3192-140">如果此參數指定的資料夾是空白的，此 Cmdlet 會刪除該資料夾。</span><span class="sxs-lookup"><span data-stu-id="a3192-140">If the folder that this parameter specifies is empty, this cmdlet deletes that folder.</span></span>
<span data-ttu-id="a3192-141">如果資料夾不是空白的，此 Cmdlet 不會變更，並會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="a3192-141">If the folder is not empty, this cmdlet makes no change, and returns an error.</span></span>

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

### <span data-ttu-id="a3192-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a3192-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a3192-143">指定要求的伺服器部分之時間長度。</span><span class="sxs-lookup"><span data-stu-id="a3192-143">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="a3192-144">-共用</span><span class="sxs-lookup"><span data-stu-id="a3192-144">-Share</span></span>
<span data-ttu-id="a3192-145">指定 **CloudFileShare** 物件。</span><span class="sxs-lookup"><span data-stu-id="a3192-145">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="a3192-146">此 Cmdlet 會移除此參數指定的檔案共用下的資料夾。</span><span class="sxs-lookup"><span data-stu-id="a3192-146">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>
<span data-ttu-id="a3192-147">若要取得 **CloudFileShare** 物件，請使用 Get-AzStorageShare Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a3192-147">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="a3192-148">此物件包含儲存內容。</span><span class="sxs-lookup"><span data-stu-id="a3192-148">This object contains the storage context.</span></span>
<span data-ttu-id="a3192-149">如果您指定此參數，請勿指定 *CoNtext* 參數。</span><span class="sxs-lookup"><span data-stu-id="a3192-149">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="a3192-150">-ShareName</span><span class="sxs-lookup"><span data-stu-id="a3192-150">-ShareName</span></span>
<span data-ttu-id="a3192-151">指定檔案共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="a3192-151">Specifies the name of the file share.</span></span>
<span data-ttu-id="a3192-152">此 Cmdlet 會移除此參數指定的檔案共用下的資料夾。</span><span class="sxs-lookup"><span data-stu-id="a3192-152">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="a3192-153">-確認</span><span class="sxs-lookup"><span data-stu-id="a3192-153">-Confirm</span></span>
<span data-ttu-id="a3192-154">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a3192-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3192-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3192-155">-WhatIf</span></span>
<span data-ttu-id="a3192-156">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a3192-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3192-157">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a3192-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3192-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3192-158">CommonParameters</span></span>
<span data-ttu-id="a3192-159">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a3192-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3192-160">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a3192-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3192-161">輸入</span><span class="sxs-lookup"><span data-stu-id="a3192-161">INPUTS</span></span>

### <span data-ttu-id="a3192-162">Microsoft.Azure.storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="a3192-162">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="a3192-163">Microsoft.Azure.storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="a3192-163">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="a3192-164">System.String</span><span class="sxs-lookup"><span data-stu-id="a3192-164">System.String</span></span>

### <span data-ttu-id="a3192-165">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="a3192-165">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a3192-166">輸出</span><span class="sxs-lookup"><span data-stu-id="a3192-166">OUTPUTS</span></span>

### <span data-ttu-id="a3192-167">Microsoft.WindowsAzure.Commands.Common.storage.ResourceModel.AzureStorageFileDirectory</span><span class="sxs-lookup"><span data-stu-id="a3192-167">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileDirectory</span></span>

## <span data-ttu-id="a3192-168">筆記</span><span class="sxs-lookup"><span data-stu-id="a3192-168">NOTES</span></span>

## <span data-ttu-id="a3192-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="a3192-169">RELATED LINKS</span></span>

[<span data-ttu-id="a3192-170">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="a3192-170">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="a3192-171">New-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="a3192-171">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="a3192-172">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="a3192-172">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)
