---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3AC3F8DE-E25D-41AE-9083-5C459A4C8CD0
online version: ''
schema: 2.0.0
ms.openlocfilehash: f92144b5cf5ffba1c470acf15c1c0145ebcc753f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93442740"
---
# <span data-ttu-id="5de02-101">Stop-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="5de02-101">Stop-AzureStorageFileCopy</span></span>

## <span data-ttu-id="5de02-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5de02-102">SYNOPSIS</span></span>
<span data-ttu-id="5de02-103">停止複製操作至指定的目的地檔案。</span><span class="sxs-lookup"><span data-stu-id="5de02-103">Stops a copy operation to the specified destination file.</span></span>

## <span data-ttu-id="5de02-104">句法</span><span class="sxs-lookup"><span data-stu-id="5de02-104">SYNTAX</span></span>

### <span data-ttu-id="5de02-105">名</span><span class="sxs-lookup"><span data-stu-id="5de02-105">ShareName</span></span>
```
Stop-AzureStorageFileCopy [-ShareName] <String> [-FilePath] <String> [-CopyId <String>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5de02-106">檔案</span><span class="sxs-lookup"><span data-stu-id="5de02-106">File</span></span>
```
Stop-AzureStorageFileCopy [-File] <CloudFile> [-CopyId <String>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5de02-107">說明</span><span class="sxs-lookup"><span data-stu-id="5de02-107">DESCRIPTION</span></span>
<span data-ttu-id="5de02-108">**AzureStorageFileCopy** Cmdlet 會停止將檔案複製到目的地檔案。</span><span class="sxs-lookup"><span data-stu-id="5de02-108">The **Stop-AzureStorageFileCopy** cmdlet stops copying a file to a destination file.</span></span>

## <span data-ttu-id="5de02-109">示例</span><span class="sxs-lookup"><span data-stu-id="5de02-109">EXAMPLES</span></span>

### <span data-ttu-id="5de02-110">範例1：停止複製操作</span><span class="sxs-lookup"><span data-stu-id="5de02-110">Example 1: Stop a copy operation</span></span>
```
PS C:\>Stop-AzureStorageFileCopy -ShareName "ContosoShare" -FilePath "FilePath" -CopyId "CopyId"
```

<span data-ttu-id="5de02-111">這個命令會停止複製具有指定名稱的檔案。</span><span class="sxs-lookup"><span data-stu-id="5de02-111">This command stops copying a file that has the specified name.</span></span>

## <span data-ttu-id="5de02-112">參數</span><span class="sxs-lookup"><span data-stu-id="5de02-112">PARAMETERS</span></span>

### <span data-ttu-id="5de02-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5de02-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="5de02-114">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="5de02-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="5de02-115">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="5de02-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="5de02-116">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="5de02-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="5de02-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="5de02-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="5de02-118">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="5de02-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="5de02-119">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="5de02-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="5de02-120">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="5de02-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="5de02-121">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="5de02-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="5de02-122">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="5de02-122">The default value is 10.</span></span>

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

### <span data-ttu-id="5de02-123">-內容</span><span class="sxs-lookup"><span data-stu-id="5de02-123">-Context</span></span>
<span data-ttu-id="5de02-124">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="5de02-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="5de02-125">若要取得儲存內容，請使用 [AzureStorageCoNtext](./New-AzureStorageContext.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5de02-125">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ShareName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5de02-126">-CopyId</span><span class="sxs-lookup"><span data-stu-id="5de02-126">-CopyId</span></span>
<span data-ttu-id="5de02-127">指定複製操作的 ID。</span><span class="sxs-lookup"><span data-stu-id="5de02-127">Specifies the ID of the copy operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5de02-128">檔案</span><span class="sxs-lookup"><span data-stu-id="5de02-128">-File</span></span>
<span data-ttu-id="5de02-129">指定 **CloudFile** 物件。</span><span class="sxs-lookup"><span data-stu-id="5de02-129">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="5de02-130">您可以使用 Get-AzureStorageFile Cmdlet 來建立雲端檔案或取得一個雲端檔案。</span><span class="sxs-lookup"><span data-stu-id="5de02-130">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: CloudFile
Parameter Sets: File
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5de02-131">-FilePath</span><span class="sxs-lookup"><span data-stu-id="5de02-131">-FilePath</span></span>
<span data-ttu-id="5de02-132">指定檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="5de02-132">Specifies the path of a file.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5de02-133">-Force</span><span class="sxs-lookup"><span data-stu-id="5de02-133">-Force</span></span>
<span data-ttu-id="5de02-134">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="5de02-134">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5de02-135">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5de02-135">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="5de02-136">指定要求中伺服器部分的超時時間長度。</span><span class="sxs-lookup"><span data-stu-id="5de02-136">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="5de02-137">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="5de02-137">-ShareName</span></span>
<span data-ttu-id="5de02-138">指定共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="5de02-138">Specifies the name of a share.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5de02-139">-確認</span><span class="sxs-lookup"><span data-stu-id="5de02-139">-Confirm</span></span>
<span data-ttu-id="5de02-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5de02-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5de02-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5de02-141">-WhatIf</span></span>
<span data-ttu-id="5de02-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5de02-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5de02-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5de02-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5de02-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5de02-144">CommonParameters</span></span>
<span data-ttu-id="5de02-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5de02-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5de02-146">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5de02-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5de02-147">輸入</span><span class="sxs-lookup"><span data-stu-id="5de02-147">INPUTS</span></span>

## <span data-ttu-id="5de02-148">輸出</span><span class="sxs-lookup"><span data-stu-id="5de02-148">OUTPUTS</span></span>

## <span data-ttu-id="5de02-149">筆記</span><span class="sxs-lookup"><span data-stu-id="5de02-149">NOTES</span></span>

## <span data-ttu-id="5de02-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="5de02-150">RELATED LINKS</span></span>

[<span data-ttu-id="5de02-151">AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="5de02-151">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="5de02-152">AzureStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="5de02-152">Get-AzureStorageFileCopyState</span></span>](./Get-AzureStorageFileCopyState.md)

[<span data-ttu-id="5de02-153">新-AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="5de02-153">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="5de02-154">開始-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="5de02-154">Start-AzureStorageFileCopy</span></span>](./Start-AzureStorageFileCopy.md)
