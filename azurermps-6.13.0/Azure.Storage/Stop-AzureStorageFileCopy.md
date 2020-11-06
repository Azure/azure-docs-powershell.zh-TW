---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 3AC3F8DE-E25D-41AE-9083-5C459A4C8CD0
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/stop-azurestoragefilecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Stop-AzureStorageFileCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Stop-AzureStorageFileCopy.md
ms.openlocfilehash: 7aea0516080ccceb6b453de86f5b731f64a1a8f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447540"
---
# <span data-ttu-id="c1cb5-101">Stop-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="c1cb5-101">Stop-AzureStorageFileCopy</span></span>

## <span data-ttu-id="c1cb5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c1cb5-102">SYNOPSIS</span></span>
<span data-ttu-id="c1cb5-103">停止複製操作至指定的目的地檔案。</span><span class="sxs-lookup"><span data-stu-id="c1cb5-103">Stops a copy operation to the specified destination file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1cb5-104">句法</span><span class="sxs-lookup"><span data-stu-id="c1cb5-104">SYNTAX</span></span>

### <span data-ttu-id="c1cb5-105">名</span><span class="sxs-lookup"><span data-stu-id="c1cb5-105">ShareName</span></span>
```
Stop-AzureStorageFileCopy [-ShareName] <String> [-FilePath] <String> [-CopyId <String>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c1cb5-106">檔案</span><span class="sxs-lookup"><span data-stu-id="c1cb5-106">File</span></span>
```
Stop-AzureStorageFileCopy [-File] <CloudFile> [-CopyId <String>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1cb5-107">說明</span><span class="sxs-lookup"><span data-stu-id="c1cb5-107">DESCRIPTION</span></span>
<span data-ttu-id="c1cb5-108">**AzureStorageFileCopy** Cmdlet 會停止將檔案複製到目的地檔案。</span><span class="sxs-lookup"><span data-stu-id="c1cb5-108">The **Stop-AzureStorageFileCopy** cmdlet stops copying a file to a destination file.</span></span>

## <span data-ttu-id="c1cb5-109">示例</span><span class="sxs-lookup"><span data-stu-id="c1cb5-109">EXAMPLES</span></span>

### <span data-ttu-id="c1cb5-110">範例1：停止複製操作</span><span class="sxs-lookup"><span data-stu-id="c1cb5-110">Example 1: Stop a copy operation</span></span>
```
PS C:\>Stop-AzureStorageFileCopy -ShareName "ContosoShare" -FilePath "FilePath" -CopyId "CopyId"
```

<span data-ttu-id="c1cb5-111">這個命令會停止複製具有指定名稱的檔案。</span><span class="sxs-lookup"><span data-stu-id="c1cb5-111">This command stops copying a file that has the specified name.</span></span>

## <span data-ttu-id="c1cb5-112">參數</span><span class="sxs-lookup"><span data-stu-id="c1cb5-112">PARAMETERS</span></span>

### <span data-ttu-id="c1cb5-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c1cb5-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c1cb5-114">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="c1cb5-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c1cb5-115">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="c1cb5-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c1cb5-116">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="c1cb5-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c1cb5-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c1cb5-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c1cb5-118">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="c1cb5-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="c1cb5-119">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="c1cb5-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="c1cb5-120">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="c1cb5-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="c1cb5-121">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="c1cb5-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="c1cb5-122">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="c1cb5-122">The default value is 10.</span></span>

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

### <span data-ttu-id="c1cb5-123">-內容</span><span class="sxs-lookup"><span data-stu-id="c1cb5-123">-Context</span></span>
<span data-ttu-id="c1cb5-124">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="c1cb5-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="c1cb5-125">若要取得儲存內容，請使用 [AzureStorageCoNtext](./New-AzureStorageContext.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c1cb5-125">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="c1cb5-126">-CopyId</span><span class="sxs-lookup"><span data-stu-id="c1cb5-126">-CopyId</span></span>
<span data-ttu-id="c1cb5-127">指定複製操作的 ID。</span><span class="sxs-lookup"><span data-stu-id="c1cb5-127">Specifies the ID of the copy operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1cb5-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1cb5-128">-DefaultProfile</span></span>
<span data-ttu-id="c1cb5-129">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c1cb5-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1cb5-130">檔案</span><span class="sxs-lookup"><span data-stu-id="c1cb5-130">-File</span></span>
<span data-ttu-id="c1cb5-131">指定 **CloudFile** 物件。</span><span class="sxs-lookup"><span data-stu-id="c1cb5-131">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="c1cb5-132">您可以使用 Get-AzureStorageFile Cmdlet 來建立雲端檔案或取得一個雲端檔案。</span><span class="sxs-lookup"><span data-stu-id="c1cb5-132">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: File
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1cb5-133">-FilePath</span><span class="sxs-lookup"><span data-stu-id="c1cb5-133">-FilePath</span></span>
<span data-ttu-id="c1cb5-134">指定檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="c1cb5-134">Specifies the path of a file.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1cb5-135">-Force</span><span class="sxs-lookup"><span data-stu-id="c1cb5-135">-Force</span></span>
<span data-ttu-id="c1cb5-136">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="c1cb5-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c1cb5-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c1cb5-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c1cb5-138">指定要求中伺服器部分的超時時間長度。</span><span class="sxs-lookup"><span data-stu-id="c1cb5-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="c1cb5-139">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="c1cb5-139">-ShareName</span></span>
<span data-ttu-id="c1cb5-140">指定共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="c1cb5-140">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="c1cb5-141">-確認</span><span class="sxs-lookup"><span data-stu-id="c1cb5-141">-Confirm</span></span>
<span data-ttu-id="c1cb5-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c1cb5-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1cb5-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1cb5-143">-WhatIf</span></span>
<span data-ttu-id="c1cb5-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c1cb5-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1cb5-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c1cb5-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1cb5-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1cb5-146">CommonParameters</span></span>
<span data-ttu-id="c1cb5-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c1cb5-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1cb5-148">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c1cb5-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1cb5-149">輸入</span><span class="sxs-lookup"><span data-stu-id="c1cb5-149">INPUTS</span></span>

### <span data-ttu-id="c1cb5-150">[WindowsAzure] CloudFile</span><span class="sxs-lookup"><span data-stu-id="c1cb5-150">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>
<span data-ttu-id="c1cb5-151">參數：檔案 (ByValue) </span><span class="sxs-lookup"><span data-stu-id="c1cb5-151">Parameters: File (ByValue)</span></span>

### <span data-ttu-id="c1cb5-152">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="c1cb5-152">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c1cb5-153">輸出</span><span class="sxs-lookup"><span data-stu-id="c1cb5-153">OUTPUTS</span></span>

### <span data-ttu-id="c1cb5-154">System.void</span><span class="sxs-lookup"><span data-stu-id="c1cb5-154">System.Void</span></span>

## <span data-ttu-id="c1cb5-155">筆記</span><span class="sxs-lookup"><span data-stu-id="c1cb5-155">NOTES</span></span>

## <span data-ttu-id="c1cb5-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="c1cb5-156">RELATED LINKS</span></span>

[<span data-ttu-id="c1cb5-157">AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="c1cb5-157">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="c1cb5-158">AzureStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="c1cb5-158">Get-AzureStorageFileCopyState</span></span>](./Get-AzureStorageFileCopyState.md)

[<span data-ttu-id="c1cb5-159">新-AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="c1cb5-159">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="c1cb5-160">開始-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="c1cb5-160">Start-AzureStorageFileCopy</span></span>](./Start-AzureStorageFileCopy.md)
