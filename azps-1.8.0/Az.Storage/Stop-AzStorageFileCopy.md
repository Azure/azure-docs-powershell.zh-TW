---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3AC3F8DE-E25D-41AE-9083-5C459A4C8CD0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/stop-azstoragefilecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageFileCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageFileCopy.md
ms.openlocfilehash: 9a2449299c6c4a6d87ee7c4b0403a35a0b7c3683
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614459"
---
# <span data-ttu-id="2e7ab-101">Stop-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="2e7ab-101">Stop-AzStorageFileCopy</span></span>

## <span data-ttu-id="2e7ab-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2e7ab-102">SYNOPSIS</span></span>
<span data-ttu-id="2e7ab-103">停止複製操作至指定的目的地檔案。</span><span class="sxs-lookup"><span data-stu-id="2e7ab-103">Stops a copy operation to the specified destination file.</span></span>

## <span data-ttu-id="2e7ab-104">句法</span><span class="sxs-lookup"><span data-stu-id="2e7ab-104">SYNTAX</span></span>

### <span data-ttu-id="2e7ab-105">名</span><span class="sxs-lookup"><span data-stu-id="2e7ab-105">ShareName</span></span>
```
Stop-AzStorageFileCopy [-ShareName] <String> [-FilePath] <String> [-CopyId <String>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2e7ab-106">檔案</span><span class="sxs-lookup"><span data-stu-id="2e7ab-106">File</span></span>
```
Stop-AzStorageFileCopy [-File] <CloudFile> [-CopyId <String>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e7ab-107">說明</span><span class="sxs-lookup"><span data-stu-id="2e7ab-107">DESCRIPTION</span></span>
<span data-ttu-id="2e7ab-108">**AzStorageFileCopy** Cmdlet 會停止將檔案複製到目的地檔案。</span><span class="sxs-lookup"><span data-stu-id="2e7ab-108">The **Stop-AzStorageFileCopy** cmdlet stops copying a file to a destination file.</span></span>

## <span data-ttu-id="2e7ab-109">示例</span><span class="sxs-lookup"><span data-stu-id="2e7ab-109">EXAMPLES</span></span>

### <span data-ttu-id="2e7ab-110">範例1：停止複製操作</span><span class="sxs-lookup"><span data-stu-id="2e7ab-110">Example 1: Stop a copy operation</span></span>
```
PS C:\>Stop-AzStorageFileCopy -ShareName "ContosoShare" -FilePath "FilePath" -CopyId "CopyId"
```

<span data-ttu-id="2e7ab-111">這個命令會停止複製具有指定名稱的檔案。</span><span class="sxs-lookup"><span data-stu-id="2e7ab-111">This command stops copying a file that has the specified name.</span></span>

## <span data-ttu-id="2e7ab-112">參數</span><span class="sxs-lookup"><span data-stu-id="2e7ab-112">PARAMETERS</span></span>

### <span data-ttu-id="2e7ab-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2e7ab-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="2e7ab-114">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="2e7ab-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="2e7ab-115">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="2e7ab-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="2e7ab-116">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="2e7ab-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="2e7ab-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="2e7ab-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="2e7ab-118">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="2e7ab-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="2e7ab-119">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="2e7ab-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="2e7ab-120">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="2e7ab-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="2e7ab-121">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="2e7ab-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="2e7ab-122">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="2e7ab-122">The default value is 10.</span></span>

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

### <span data-ttu-id="2e7ab-123">-內容</span><span class="sxs-lookup"><span data-stu-id="2e7ab-123">-Context</span></span>
<span data-ttu-id="2e7ab-124">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="2e7ab-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="2e7ab-125">若要取得儲存內容，請使用 [AzStorageCoNtext](./New-AzStorageContext.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2e7ab-125">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="2e7ab-126">-CopyId</span><span class="sxs-lookup"><span data-stu-id="2e7ab-126">-CopyId</span></span>
<span data-ttu-id="2e7ab-127">指定複製操作的 ID。</span><span class="sxs-lookup"><span data-stu-id="2e7ab-127">Specifies the ID of the copy operation.</span></span>

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

### <span data-ttu-id="2e7ab-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e7ab-128">-DefaultProfile</span></span>
<span data-ttu-id="2e7ab-129">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2e7ab-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e7ab-130">檔案</span><span class="sxs-lookup"><span data-stu-id="2e7ab-130">-File</span></span>
<span data-ttu-id="2e7ab-131">指定 **CloudFile** 物件。</span><span class="sxs-lookup"><span data-stu-id="2e7ab-131">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="2e7ab-132">您可以使用 Get-AzStorageFile Cmdlet 來建立雲端檔案或取得一個雲端檔案。</span><span class="sxs-lookup"><span data-stu-id="2e7ab-132">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="2e7ab-133">-FilePath</span><span class="sxs-lookup"><span data-stu-id="2e7ab-133">-FilePath</span></span>
<span data-ttu-id="2e7ab-134">指定檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="2e7ab-134">Specifies the path of a file.</span></span>

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

### <span data-ttu-id="2e7ab-135">-Force</span><span class="sxs-lookup"><span data-stu-id="2e7ab-135">-Force</span></span>
<span data-ttu-id="2e7ab-136">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="2e7ab-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2e7ab-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2e7ab-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="2e7ab-138">指定要求中伺服器部分的超時時間長度。</span><span class="sxs-lookup"><span data-stu-id="2e7ab-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="2e7ab-139">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="2e7ab-139">-ShareName</span></span>
<span data-ttu-id="2e7ab-140">指定共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="2e7ab-140">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="2e7ab-141">-確認</span><span class="sxs-lookup"><span data-stu-id="2e7ab-141">-Confirm</span></span>
<span data-ttu-id="2e7ab-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2e7ab-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e7ab-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e7ab-143">-WhatIf</span></span>
<span data-ttu-id="2e7ab-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2e7ab-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e7ab-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2e7ab-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e7ab-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e7ab-146">CommonParameters</span></span>
<span data-ttu-id="2e7ab-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2e7ab-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e7ab-148">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2e7ab-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e7ab-149">輸入</span><span class="sxs-lookup"><span data-stu-id="2e7ab-149">INPUTS</span></span>

### <span data-ttu-id="2e7ab-150">[WindowsAzure] CloudFile</span><span class="sxs-lookup"><span data-stu-id="2e7ab-150">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="2e7ab-151">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="2e7ab-151">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2e7ab-152">輸出</span><span class="sxs-lookup"><span data-stu-id="2e7ab-152">OUTPUTS</span></span>

### <span data-ttu-id="2e7ab-153">System.void</span><span class="sxs-lookup"><span data-stu-id="2e7ab-153">System.Void</span></span>

## <span data-ttu-id="2e7ab-154">筆記</span><span class="sxs-lookup"><span data-stu-id="2e7ab-154">NOTES</span></span>

## <span data-ttu-id="2e7ab-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="2e7ab-155">RELATED LINKS</span></span>

[<span data-ttu-id="2e7ab-156">AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="2e7ab-156">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="2e7ab-157">AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="2e7ab-157">Get-AzStorageFileCopyState</span></span>](./Get-AzStorageFileCopyState.md)

[<span data-ttu-id="2e7ab-158">新-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="2e7ab-158">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="2e7ab-159">開始-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="2e7ab-159">Start-AzStorageFileCopy</span></span>](./Start-AzStorageFileCopy.md)