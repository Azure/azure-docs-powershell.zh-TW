---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 65962F9A-CC79-4B8B-9208-A993708FD36F
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageDirectory.md
ms.openlocfilehash: 6f44f1545eea4e515064873cdc77f8b34819fabc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915073"
---
# <span data-ttu-id="952bf-101">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="952bf-101">New-AzStorageDirectory</span></span>

## <span data-ttu-id="952bf-102">簡介</span><span class="sxs-lookup"><span data-stu-id="952bf-102">SYNOPSIS</span></span>
<span data-ttu-id="952bf-103">建立目錄。</span><span class="sxs-lookup"><span data-stu-id="952bf-103">Creates a directory.</span></span>

## <span data-ttu-id="952bf-104">語法</span><span class="sxs-lookup"><span data-stu-id="952bf-104">SYNTAX</span></span>

### <span data-ttu-id="952bf-105">ShareName (預設) </span><span class="sxs-lookup"><span data-stu-id="952bf-105">ShareName (Default)</span></span>
```
New-AzStorageDirectory [-ShareName] <String> [-Path] <String> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="952bf-106">共用</span><span class="sxs-lookup"><span data-stu-id="952bf-106">Share</span></span>
```
New-AzStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="952bf-107">目錄</span><span class="sxs-lookup"><span data-stu-id="952bf-107">Directory</span></span>
```
New-AzStorageDirectory [-Directory] <CloudFileDirectory> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="952bf-108">描述</span><span class="sxs-lookup"><span data-stu-id="952bf-108">DESCRIPTION</span></span>
<span data-ttu-id="952bf-109">**New-AzStorageDirectory** Cmdlet 會建立目錄。</span><span class="sxs-lookup"><span data-stu-id="952bf-109">The **New-AzStorageDirectory** cmdlet creates a directory.</span></span>
<span data-ttu-id="952bf-110">此 Cmdlet 會返回 **CloudFileDirectory** 物件。</span><span class="sxs-lookup"><span data-stu-id="952bf-110">This cmdlet returns a **CloudFileDirectory** object.</span></span>

## <span data-ttu-id="952bf-111">例子</span><span class="sxs-lookup"><span data-stu-id="952bf-111">EXAMPLES</span></span>

### <span data-ttu-id="952bf-112">範例 1：在檔案共用中建立資料夾</span><span class="sxs-lookup"><span data-stu-id="952bf-112">Example 1: Create a folder in a file share</span></span>
```
PS C:\>New-AzStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="952bf-113">此命令在名為 ContosoShare06 的檔案共用中，建立一個名為 ContosoWorkingFolder 的資料夾。</span><span class="sxs-lookup"><span data-stu-id="952bf-113">This command creates a folder named ContosoWorkingFolder in the file share named ContosoShare06.</span></span>

### <span data-ttu-id="952bf-114">範例 2：在檔案共用物件中指定的檔案共用中建立資料夾</span><span class="sxs-lookup"><span data-stu-id="952bf-114">Example 2: Create a folder in a file share specified in a file share object</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" | New-AzStorageDirectory -Path "ContosoWorkingFolder"
```

<span data-ttu-id="952bf-115">此命令使用 **Get-AzStorageShare** Cmdlet 取得名為 ContosoShare06 的檔案共用，然後使用管線運算子將檔案共用傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="952bf-115">This command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="952bf-116">目前的 Cmdlet 在 ContosoShare06 中建立名為 ContosoWorkingFolder 的資料夾。</span><span class="sxs-lookup"><span data-stu-id="952bf-116">The current cmdlet creates the folder named ContosoWorkingFolder in ContosoShare06.</span></span>

## <span data-ttu-id="952bf-117">參數</span><span class="sxs-lookup"><span data-stu-id="952bf-117">PARAMETERS</span></span>

### <span data-ttu-id="952bf-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="952bf-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="952bf-119">指定一個服務要求用戶端的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="952bf-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="952bf-120">如果前一個通話在指定的時間間隔內失敗，此 Cmdlet 會重新重試要求。</span><span class="sxs-lookup"><span data-stu-id="952bf-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="952bf-121">如果此 Cmdlet 在間隔經過之前未收到成功回應，此 Cmdlet 會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="952bf-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="952bf-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="952bf-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="952bf-123">指定同時進行的最大網路通話數。</span><span class="sxs-lookup"><span data-stu-id="952bf-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="952bf-124">您可以使用此參數來限制並行，以節流本地 CPU 和頻寬使用量，方法為指定並行網路通話的數量上限。</span><span class="sxs-lookup"><span data-stu-id="952bf-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="952bf-125">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="952bf-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="952bf-126">此參數有助於減少低頻寬環境的網路連接問題，例如每秒 100 KB。</span><span class="sxs-lookup"><span data-stu-id="952bf-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="952bf-127">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="952bf-127">The default value is 10.</span></span>

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

### <span data-ttu-id="952bf-128">-內容</span><span class="sxs-lookup"><span data-stu-id="952bf-128">-Context</span></span>
<span data-ttu-id="952bf-129">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="952bf-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="952bf-130">若要取得儲存內容，請使用 [New-AzStorageCoNtext](./New-AzStorageContext.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="952bf-130">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="952bf-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="952bf-131">-DefaultProfile</span></span>
<span data-ttu-id="952bf-132">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="952bf-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="952bf-133">-目錄</span><span class="sxs-lookup"><span data-stu-id="952bf-133">-Directory</span></span>
<span data-ttu-id="952bf-134">將資料夾指定為 **CloudFileDirectory** 物件。</span><span class="sxs-lookup"><span data-stu-id="952bf-134">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="952bf-135">此 Cmdlet 會在此參數指定的位置建立資料夾。</span><span class="sxs-lookup"><span data-stu-id="952bf-135">This cmdlet creates the folder in the location that this parameter specifies.</span></span>
<span data-ttu-id="952bf-136">若要取得目錄，請使用 New-AzStorageDirectory Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="952bf-136">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="952bf-137">您也可以使用 Get-AzStorageFile取得目錄。</span><span class="sxs-lookup"><span data-stu-id="952bf-137">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="952bf-138">-路徑</span><span class="sxs-lookup"><span data-stu-id="952bf-138">-Path</span></span>
<span data-ttu-id="952bf-139">指定資料夾的路徑。</span><span class="sxs-lookup"><span data-stu-id="952bf-139">Specifies the path of a folder.</span></span>
<span data-ttu-id="952bf-140">此 Cmdlet 會為此 Cmdlet 指定的路徑建立資料夾。</span><span class="sxs-lookup"><span data-stu-id="952bf-140">This cmdlet creates a folder for the path that this cmdlet specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="952bf-141">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="952bf-141">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="952bf-142">指定要求的伺服器部分之時間長度。</span><span class="sxs-lookup"><span data-stu-id="952bf-142">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="952bf-143">-共用</span><span class="sxs-lookup"><span data-stu-id="952bf-143">-Share</span></span>
<span data-ttu-id="952bf-144">指定 **CloudFileShare** 物件。</span><span class="sxs-lookup"><span data-stu-id="952bf-144">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="952bf-145">此 Cmdlet 會在此參數指定的檔案共用中建立資料夾。</span><span class="sxs-lookup"><span data-stu-id="952bf-145">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>
<span data-ttu-id="952bf-146">若要取得 **CloudFileShare** 物件，請使用 Get-AzStorageShare Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="952bf-146">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="952bf-147">此物件包含儲存內容。</span><span class="sxs-lookup"><span data-stu-id="952bf-147">This object contains the storage context.</span></span>
<span data-ttu-id="952bf-148">如果您指定此參數，請勿指定 *CoNtext* 參數。</span><span class="sxs-lookup"><span data-stu-id="952bf-148">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="952bf-149">-ShareName</span><span class="sxs-lookup"><span data-stu-id="952bf-149">-ShareName</span></span>
<span data-ttu-id="952bf-150">指定檔案共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="952bf-150">Specifies the name of the file share.</span></span>
<span data-ttu-id="952bf-151">此 Cmdlet 會在此參數指定的檔案共用中建立資料夾。</span><span class="sxs-lookup"><span data-stu-id="952bf-151">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="952bf-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="952bf-152">CommonParameters</span></span>
<span data-ttu-id="952bf-153">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="952bf-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="952bf-154">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="952bf-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="952bf-155">輸入</span><span class="sxs-lookup"><span data-stu-id="952bf-155">INPUTS</span></span>

### <span data-ttu-id="952bf-156">Microsoft.Azure.storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="952bf-156">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="952bf-157">Microsoft.Azure.storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="952bf-157">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="952bf-158">System.String</span><span class="sxs-lookup"><span data-stu-id="952bf-158">System.String</span></span>

### <span data-ttu-id="952bf-159">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="952bf-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="952bf-160">輸出</span><span class="sxs-lookup"><span data-stu-id="952bf-160">OUTPUTS</span></span>

### <span data-ttu-id="952bf-161">Microsoft.WindowsAzure.Commands.Common.storage.ResourceModel.AzureStorageFileDirectory</span><span class="sxs-lookup"><span data-stu-id="952bf-161">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileDirectory</span></span>

## <span data-ttu-id="952bf-162">筆記</span><span class="sxs-lookup"><span data-stu-id="952bf-162">NOTES</span></span>

## <span data-ttu-id="952bf-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="952bf-163">RELATED LINKS</span></span>

[<span data-ttu-id="952bf-164">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="952bf-164">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="952bf-165">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="952bf-165">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="952bf-166">New-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="952bf-166">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="952bf-167">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="952bf-167">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="952bf-168">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="952bf-168">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)
