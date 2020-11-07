---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 65962F9A-CC79-4B8B-9208-A993708FD36F
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageDirectory.md
ms.openlocfilehash: 5965ef718a24a428dab84ddab8dc07495e2d8662
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791673"
---
# <span data-ttu-id="5b17c-101">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="5b17c-101">New-AzStorageDirectory</span></span>

## <span data-ttu-id="5b17c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5b17c-102">SYNOPSIS</span></span>
<span data-ttu-id="5b17c-103">建立目錄。</span><span class="sxs-lookup"><span data-stu-id="5b17c-103">Creates a directory.</span></span>

## <span data-ttu-id="5b17c-104">句法</span><span class="sxs-lookup"><span data-stu-id="5b17c-104">SYNTAX</span></span>

### <span data-ttu-id="5b17c-105">共用名稱 (預設) </span><span class="sxs-lookup"><span data-stu-id="5b17c-105">ShareName (Default)</span></span>
```
New-AzStorageDirectory [-ShareName] <String> [-Path] <String> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="5b17c-106">共用</span><span class="sxs-lookup"><span data-stu-id="5b17c-106">Share</span></span>
```
New-AzStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="5b17c-107">空目錄</span><span class="sxs-lookup"><span data-stu-id="5b17c-107">Directory</span></span>
```
New-AzStorageDirectory [-Directory] <CloudFileDirectory> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="5b17c-108">說明</span><span class="sxs-lookup"><span data-stu-id="5b17c-108">DESCRIPTION</span></span>
<span data-ttu-id="5b17c-109">**新的-AzStorageDirectory** Cmdlet 會建立目錄。</span><span class="sxs-lookup"><span data-stu-id="5b17c-109">The **New-AzStorageDirectory** cmdlet creates a directory.</span></span>
<span data-ttu-id="5b17c-110">這個 Cmdlet 會傳回 **CloudFileDirectory** 物件。</span><span class="sxs-lookup"><span data-stu-id="5b17c-110">This cmdlet returns a **CloudFileDirectory** object.</span></span>

## <span data-ttu-id="5b17c-111">示例</span><span class="sxs-lookup"><span data-stu-id="5b17c-111">EXAMPLES</span></span>

### <span data-ttu-id="5b17c-112">範例1：在檔案共用中建立資料夾</span><span class="sxs-lookup"><span data-stu-id="5b17c-112">Example 1: Create a folder in a file share</span></span>
```
PS C:\>New-AzStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="5b17c-113">這個命令會在檔案共用中建立名為 ContosoWorkingFolder 的資料夾（名為 ContosoShare06）。</span><span class="sxs-lookup"><span data-stu-id="5b17c-113">This command creates a folder named ContosoWorkingFolder in the file share named ContosoShare06.</span></span>

### <span data-ttu-id="5b17c-114">範例2：在檔案共用物件中指定的檔案共用中建立資料夾</span><span class="sxs-lookup"><span data-stu-id="5b17c-114">Example 2: Create a folder in a file share specified in a file share object</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" | New-AzStorageDirectory -Path "ContosoWorkingFolder"
```

<span data-ttu-id="5b17c-115">這個命令會使用 **AzStorageShare** Cmdlet 來取得名為 ContosoShare06 的檔案共用，然後使用管線運算子將它傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5b17c-115">This command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5b17c-116">目前的 Cmdlet 會在 ContosoShare06 中建立名為 ContosoWorkingFolder 的資料夾。</span><span class="sxs-lookup"><span data-stu-id="5b17c-116">The current cmdlet creates the folder named ContosoWorkingFolder in ContosoShare06.</span></span>

## <span data-ttu-id="5b17c-117">參數</span><span class="sxs-lookup"><span data-stu-id="5b17c-117">PARAMETERS</span></span>

### <span data-ttu-id="5b17c-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5b17c-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="5b17c-119">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="5b17c-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="5b17c-120">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="5b17c-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="5b17c-121">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="5b17c-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="5b17c-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="5b17c-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="5b17c-123">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="5b17c-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="5b17c-124">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="5b17c-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="5b17c-125">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="5b17c-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="5b17c-126">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="5b17c-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="5b17c-127">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="5b17c-127">The default value is 10.</span></span>

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

### <span data-ttu-id="5b17c-128">-內容</span><span class="sxs-lookup"><span data-stu-id="5b17c-128">-Context</span></span>
<span data-ttu-id="5b17c-129">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="5b17c-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="5b17c-130">若要取得儲存內容，請使用 [AzStorageCoNtext](./New-AzStorageContext.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5b17c-130">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="5b17c-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b17c-131">-DefaultProfile</span></span>
<span data-ttu-id="5b17c-132">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5b17c-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b17c-133">-Directory</span><span class="sxs-lookup"><span data-stu-id="5b17c-133">-Directory</span></span>
<span data-ttu-id="5b17c-134">將資料夾指定為 **CloudFileDirectory** 物件。</span><span class="sxs-lookup"><span data-stu-id="5b17c-134">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="5b17c-135">這個 Cmdlet 會在此參數指定的位置中建立資料夾。</span><span class="sxs-lookup"><span data-stu-id="5b17c-135">This cmdlet creates the folder in the location that this parameter specifies.</span></span>
<span data-ttu-id="5b17c-136">若要取得目錄，請使用 New-AzStorageDirectory Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5b17c-136">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="5b17c-137">您也可以使用 Get-AzStorageFile Cmdlet 來取得目錄。</span><span class="sxs-lookup"><span data-stu-id="5b17c-137">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="5b17c-138">-Path</span><span class="sxs-lookup"><span data-stu-id="5b17c-138">-Path</span></span>
<span data-ttu-id="5b17c-139">指定資料夾的路徑。</span><span class="sxs-lookup"><span data-stu-id="5b17c-139">Specifies the path of a folder.</span></span>
<span data-ttu-id="5b17c-140">這個 Cmdlet 會為這個 Cmdlet 所指定的路徑建立一個資料夾。</span><span class="sxs-lookup"><span data-stu-id="5b17c-140">This cmdlet creates a folder for the path that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="5b17c-141">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5b17c-141">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="5b17c-142">指定要求中伺服器部分的超時時間長度。</span><span class="sxs-lookup"><span data-stu-id="5b17c-142">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="5b17c-143">-共用</span><span class="sxs-lookup"><span data-stu-id="5b17c-143">-Share</span></span>
<span data-ttu-id="5b17c-144">指定 **CloudFileShare** 物件。</span><span class="sxs-lookup"><span data-stu-id="5b17c-144">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="5b17c-145">這個 Cmdlet 會在檔案共用中建立此參數指定的資料夾。</span><span class="sxs-lookup"><span data-stu-id="5b17c-145">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>
<span data-ttu-id="5b17c-146">若要取得 **CloudFileShare** 物件，請使用 Get-AzStorageShare Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5b17c-146">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="5b17c-147">此物件包含儲存內容。</span><span class="sxs-lookup"><span data-stu-id="5b17c-147">This object contains the storage context.</span></span>
<span data-ttu-id="5b17c-148">如果您指定此參數，請勿指定 *CoNtext* 參數。</span><span class="sxs-lookup"><span data-stu-id="5b17c-148">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="5b17c-149">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="5b17c-149">-ShareName</span></span>
<span data-ttu-id="5b17c-150">指定檔案共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="5b17c-150">Specifies the name of the file share.</span></span>
<span data-ttu-id="5b17c-151">這個 Cmdlet 會在檔案共用中建立此參數指定的資料夾。</span><span class="sxs-lookup"><span data-stu-id="5b17c-151">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="5b17c-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b17c-152">CommonParameters</span></span>
<span data-ttu-id="5b17c-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5b17c-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b17c-154">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5b17c-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b17c-155">輸入</span><span class="sxs-lookup"><span data-stu-id="5b17c-155">INPUTS</span></span>

### <span data-ttu-id="5b17c-156">CloudFileShare （即 Azure）</span><span class="sxs-lookup"><span data-stu-id="5b17c-156">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="5b17c-157">CloudFileDirectory （即 Azure）</span><span class="sxs-lookup"><span data-stu-id="5b17c-157">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="5b17c-158">System.object</span><span class="sxs-lookup"><span data-stu-id="5b17c-158">System.String</span></span>

### <span data-ttu-id="5b17c-159">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="5b17c-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="5b17c-160">輸出</span><span class="sxs-lookup"><span data-stu-id="5b17c-160">OUTPUTS</span></span>

### <span data-ttu-id="5b17c-161">CloudFileDirectory （即 Azure）</span><span class="sxs-lookup"><span data-stu-id="5b17c-161">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

## <span data-ttu-id="5b17c-162">筆記</span><span class="sxs-lookup"><span data-stu-id="5b17c-162">NOTES</span></span>

## <span data-ttu-id="5b17c-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="5b17c-163">RELATED LINKS</span></span>

[<span data-ttu-id="5b17c-164">AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="5b17c-164">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="5b17c-165">AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="5b17c-165">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="5b17c-166">新-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="5b17c-166">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="5b17c-167">新-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="5b17c-167">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="5b17c-168">移除-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="5b17c-168">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)
