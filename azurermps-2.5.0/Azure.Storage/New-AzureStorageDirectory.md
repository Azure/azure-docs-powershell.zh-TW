---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 65962F9A-CC79-4B8B-9208-A993708FD36F
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragedirectory
schema: 2.0.0
ms.openlocfilehash: 0a474171b7659346a1d921f98920a9befc85eea8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801474"
---
# <span data-ttu-id="4e763-101">New-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="4e763-101">New-AzureStorageDirectory</span></span>

## <span data-ttu-id="4e763-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4e763-102">SYNOPSIS</span></span>
<span data-ttu-id="4e763-103">建立目錄。</span><span class="sxs-lookup"><span data-stu-id="4e763-103">Creates a directory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e763-104">句法</span><span class="sxs-lookup"><span data-stu-id="4e763-104">SYNTAX</span></span>

### <span data-ttu-id="4e763-105">共用名稱 (預設) </span><span class="sxs-lookup"><span data-stu-id="4e763-105">ShareName (Default)</span></span>
```
New-AzureStorageDirectory [-ShareName] <String> [-Path] <String> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="4e763-106">共用</span><span class="sxs-lookup"><span data-stu-id="4e763-106">Share</span></span>
```
New-AzureStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="4e763-107">空目錄</span><span class="sxs-lookup"><span data-stu-id="4e763-107">Directory</span></span>
```
New-AzureStorageDirectory [-Directory] <CloudFileDirectory> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="4e763-108">說明</span><span class="sxs-lookup"><span data-stu-id="4e763-108">DESCRIPTION</span></span>
<span data-ttu-id="4e763-109">**新的-AzureStorageDirectory** Cmdlet 會建立目錄。</span><span class="sxs-lookup"><span data-stu-id="4e763-109">The **New-AzureStorageDirectory** cmdlet creates a directory.</span></span>
<span data-ttu-id="4e763-110">這個 Cmdlet 會傳回 **CloudFileDirectory** 物件。</span><span class="sxs-lookup"><span data-stu-id="4e763-110">This cmdlet returns a **CloudFileDirectory** object.</span></span>

## <span data-ttu-id="4e763-111">示例</span><span class="sxs-lookup"><span data-stu-id="4e763-111">EXAMPLES</span></span>

### <span data-ttu-id="4e763-112">範例1：在檔案共用中建立資料夾</span><span class="sxs-lookup"><span data-stu-id="4e763-112">Example 1: Create a folder in a file share</span></span>
```
PS C:\>New-AzureStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="4e763-113">這個命令會在檔案共用中建立名為 ContosoWorkingFolder 的資料夾（名為 ContosoShare06）。</span><span class="sxs-lookup"><span data-stu-id="4e763-113">This command creates a folder named ContosoWorkingFolder in the file share named ContosoShare06.</span></span>

### <span data-ttu-id="4e763-114">範例2：在檔案共用物件中指定的檔案共用中建立資料夾</span><span class="sxs-lookup"><span data-stu-id="4e763-114">Example 2: Create a folder in a file share specified in a file share object</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06" | New-AzureStorageDirectory -Path "ContosoWorkingFolder"
```

<span data-ttu-id="4e763-115">這個命令會使用 **AzureStorageShare** Cmdlet 來取得名為 ContosoShare06 的檔案共用，然後使用管線運算子將它傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4e763-115">This command uses the **Get-AzureStorageShare** cmdlet to get the file share named ContosoShare06, and then passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4e763-116">目前的 Cmdlet 會在 ContosoShare06 中建立名為 ContosoWorkingFolder 的資料夾。</span><span class="sxs-lookup"><span data-stu-id="4e763-116">The current cmdlet creates the folder named ContosoWorkingFolder in ContosoShare06.</span></span>

## <span data-ttu-id="4e763-117">參數</span><span class="sxs-lookup"><span data-stu-id="4e763-117">PARAMETERS</span></span>

### <span data-ttu-id="4e763-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4e763-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="4e763-119">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="4e763-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="4e763-120">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="4e763-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="4e763-121">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="4e763-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="4e763-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="4e763-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="4e763-123">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="4e763-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="4e763-124">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="4e763-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="4e763-125">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="4e763-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="4e763-126">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="4e763-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="4e763-127">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="4e763-127">The default value is 10.</span></span>

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

### <span data-ttu-id="4e763-128">-內容</span><span class="sxs-lookup"><span data-stu-id="4e763-128">-Context</span></span>
<span data-ttu-id="4e763-129">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="4e763-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="4e763-130">若要取得儲存內容，請使用 [AzureStorageCoNtext](./New-AzureStorageContext.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4e763-130">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="4e763-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e763-131">-DefaultProfile</span></span>
<span data-ttu-id="4e763-132">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4e763-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e763-133">-Directory</span><span class="sxs-lookup"><span data-stu-id="4e763-133">-Directory</span></span>
<span data-ttu-id="4e763-134">將資料夾指定為 **CloudFileDirectory** 物件。</span><span class="sxs-lookup"><span data-stu-id="4e763-134">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="4e763-135">這個 Cmdlet 會在此參數指定的位置中建立資料夾。</span><span class="sxs-lookup"><span data-stu-id="4e763-135">This cmdlet creates the folder in the location that this parameter specifies.</span></span>
<span data-ttu-id="4e763-136">若要取得目錄，請使用 New-AzureStorageDirectory Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4e763-136">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="4e763-137">您也可以使用 Get-AzureStorageFile Cmdlet 來取得目錄。</span><span class="sxs-lookup"><span data-stu-id="4e763-137">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="4e763-138">-Path</span><span class="sxs-lookup"><span data-stu-id="4e763-138">-Path</span></span>
<span data-ttu-id="4e763-139">指定資料夾的路徑。</span><span class="sxs-lookup"><span data-stu-id="4e763-139">Specifies the path of a folder.</span></span>
<span data-ttu-id="4e763-140">這個 Cmdlet 會為這個 Cmdlet 所指定的路徑建立一個資料夾。</span><span class="sxs-lookup"><span data-stu-id="4e763-140">This cmdlet creates a folder for the path that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="4e763-141">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4e763-141">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="4e763-142">指定要求中伺服器部分的超時時間長度。</span><span class="sxs-lookup"><span data-stu-id="4e763-142">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="4e763-143">-共用</span><span class="sxs-lookup"><span data-stu-id="4e763-143">-Share</span></span>
<span data-ttu-id="4e763-144">指定 **CloudFileShare** 物件。</span><span class="sxs-lookup"><span data-stu-id="4e763-144">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="4e763-145">這個 Cmdlet 會在檔案共用中建立此參數指定的資料夾。</span><span class="sxs-lookup"><span data-stu-id="4e763-145">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>
<span data-ttu-id="4e763-146">若要取得 **CloudFileShare** 物件，請使用 Get-AzureStorageShare Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4e763-146">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="4e763-147">此物件包含儲存內容。</span><span class="sxs-lookup"><span data-stu-id="4e763-147">This object contains the storage context.</span></span>
<span data-ttu-id="4e763-148">如果您指定此參數，請勿指定 *CoNtext* 參數。</span><span class="sxs-lookup"><span data-stu-id="4e763-148">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="4e763-149">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="4e763-149">-ShareName</span></span>
<span data-ttu-id="4e763-150">指定檔案共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="4e763-150">Specifies the name of the file share.</span></span>
<span data-ttu-id="4e763-151">這個 Cmdlet 會在檔案共用中建立此參數指定的資料夾。</span><span class="sxs-lookup"><span data-stu-id="4e763-151">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="4e763-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e763-152">CommonParameters</span></span>
<span data-ttu-id="4e763-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4e763-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e763-154">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4e763-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e763-155">輸入</span><span class="sxs-lookup"><span data-stu-id="4e763-155">INPUTS</span></span>

### <span data-ttu-id="4e763-156">[WindowsAzure] CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="4e763-156">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="4e763-157">參數：共用 (ByValue) </span><span class="sxs-lookup"><span data-stu-id="4e763-157">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="4e763-158">[WindowsAzure] CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="4e763-158">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>
<span data-ttu-id="4e763-159">參數：目錄 (ByValue) </span><span class="sxs-lookup"><span data-stu-id="4e763-159">Parameters: Directory (ByValue)</span></span>

### <span data-ttu-id="4e763-160">System.object</span><span class="sxs-lookup"><span data-stu-id="4e763-160">System.String</span></span>

### <span data-ttu-id="4e763-161">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="4e763-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4e763-162">輸出</span><span class="sxs-lookup"><span data-stu-id="4e763-162">OUTPUTS</span></span>

### <span data-ttu-id="4e763-163">[WindowsAzure] CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="4e763-163">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>

## <span data-ttu-id="4e763-164">筆記</span><span class="sxs-lookup"><span data-stu-id="4e763-164">NOTES</span></span>

## <span data-ttu-id="4e763-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="4e763-165">RELATED LINKS</span></span>

[<span data-ttu-id="4e763-166">AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="4e763-166">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="4e763-167">AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="4e763-167">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="4e763-168">新-AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="4e763-168">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="4e763-169">新-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="4e763-169">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)

[<span data-ttu-id="4e763-170">移除-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="4e763-170">Remove-AzureStorageDirectory</span></span>](./Remove-AzureStorageDirectory.md)
