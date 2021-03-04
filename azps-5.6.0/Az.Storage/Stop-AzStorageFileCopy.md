---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3AC3F8DE-E25D-41AE-9083-5C459A4C8CD0
online version: https://docs.microsoft.com/powershell/module/az.storage/stop-azstoragefilecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageFileCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageFileCopy.md
ms.openlocfilehash: b306b5820e55687c1116adc56b92e1ee5ebd4115
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903922"
---
# <span data-ttu-id="fcfe1-101">Stop-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="fcfe1-101">Stop-AzStorageFileCopy</span></span>

## <span data-ttu-id="fcfe1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fcfe1-102">SYNOPSIS</span></span>
<span data-ttu-id="fcfe1-103">停止對指定目的地檔案的複製作業。</span><span class="sxs-lookup"><span data-stu-id="fcfe1-103">Stops a copy operation to the specified destination file.</span></span>

## <span data-ttu-id="fcfe1-104">語法</span><span class="sxs-lookup"><span data-stu-id="fcfe1-104">SYNTAX</span></span>

### <span data-ttu-id="fcfe1-105">ShareName</span><span class="sxs-lookup"><span data-stu-id="fcfe1-105">ShareName</span></span>
```
Stop-AzStorageFileCopy [-ShareName] <String> [-FilePath] <String> [-CopyId <String>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fcfe1-106">檔</span><span class="sxs-lookup"><span data-stu-id="fcfe1-106">File</span></span>
```
Stop-AzStorageFileCopy [-File] <CloudFile> [-CopyId <String>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcfe1-107">描述</span><span class="sxs-lookup"><span data-stu-id="fcfe1-107">DESCRIPTION</span></span>
<span data-ttu-id="fcfe1-108">**Stop-AzStorageFileCopy** Cmdlet 停止將檔案複製到目的地檔案。</span><span class="sxs-lookup"><span data-stu-id="fcfe1-108">The **Stop-AzStorageFileCopy** cmdlet stops copying a file to a destination file.</span></span>

## <span data-ttu-id="fcfe1-109">例子</span><span class="sxs-lookup"><span data-stu-id="fcfe1-109">EXAMPLES</span></span>

### <span data-ttu-id="fcfe1-110">範例 1：停止複製作業</span><span class="sxs-lookup"><span data-stu-id="fcfe1-110">Example 1: Stop a copy operation</span></span>
```
PS C:\>Stop-AzStorageFileCopy -ShareName "ContosoShare" -FilePath "FilePath" -CopyId "CopyId"
```

<span data-ttu-id="fcfe1-111">此命令會停止複製具有指定名稱的檔案。</span><span class="sxs-lookup"><span data-stu-id="fcfe1-111">This command stops copying a file that has the specified name.</span></span>

## <span data-ttu-id="fcfe1-112">參數</span><span class="sxs-lookup"><span data-stu-id="fcfe1-112">PARAMETERS</span></span>

### <span data-ttu-id="fcfe1-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fcfe1-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="fcfe1-114">指定一個服務要求用戶端的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="fcfe1-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="fcfe1-115">如果前一個通話在指定的時間間隔內失敗，此 Cmdlet 會重新重試要求。</span><span class="sxs-lookup"><span data-stu-id="fcfe1-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="fcfe1-116">如果此 Cmdlet 在間隔經過之前未收到成功回應，此 Cmdlet 會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="fcfe1-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="fcfe1-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="fcfe1-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="fcfe1-118">指定同時進行的最大網路通話數。</span><span class="sxs-lookup"><span data-stu-id="fcfe1-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="fcfe1-119">您可以使用此參數來限制並行，以節流本地 CPU 和頻寬使用量，方法為指定並行網路通話的數量上限。</span><span class="sxs-lookup"><span data-stu-id="fcfe1-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="fcfe1-120">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="fcfe1-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="fcfe1-121">此參數有助於減少低頻寬環境的網路連接問題，例如每秒 100 KB。</span><span class="sxs-lookup"><span data-stu-id="fcfe1-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="fcfe1-122">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="fcfe1-122">The default value is 10.</span></span>

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

### <span data-ttu-id="fcfe1-123">-內容</span><span class="sxs-lookup"><span data-stu-id="fcfe1-123">-Context</span></span>
<span data-ttu-id="fcfe1-124">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="fcfe1-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="fcfe1-125">若要取得儲存內容，請使用 [New-AzStorageCoNtext](./New-AzStorageContext.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fcfe1-125">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="fcfe1-126">-CopyId</span><span class="sxs-lookup"><span data-stu-id="fcfe1-126">-CopyId</span></span>
<span data-ttu-id="fcfe1-127">指定複製作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="fcfe1-127">Specifies the ID of the copy operation.</span></span>

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

### <span data-ttu-id="fcfe1-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcfe1-128">-DefaultProfile</span></span>
<span data-ttu-id="fcfe1-129">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="fcfe1-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcfe1-130">-檔案</span><span class="sxs-lookup"><span data-stu-id="fcfe1-130">-File</span></span>
<span data-ttu-id="fcfe1-131">指定 **CloudFile** 物件。</span><span class="sxs-lookup"><span data-stu-id="fcfe1-131">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="fcfe1-132">您可以使用 Cmdlet 建立雲端檔案，或取得Get-AzStorageFile檔案。</span><span class="sxs-lookup"><span data-stu-id="fcfe1-132">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="fcfe1-133">-FilePath</span><span class="sxs-lookup"><span data-stu-id="fcfe1-133">-FilePath</span></span>
<span data-ttu-id="fcfe1-134">指定檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="fcfe1-134">Specifies the path of a file.</span></span>

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

### <span data-ttu-id="fcfe1-135">-強制</span><span class="sxs-lookup"><span data-stu-id="fcfe1-135">-Force</span></span>
<span data-ttu-id="fcfe1-136">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="fcfe1-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fcfe1-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fcfe1-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="fcfe1-138">指定要求的伺服器部分之時間長度。</span><span class="sxs-lookup"><span data-stu-id="fcfe1-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="fcfe1-139">-ShareName</span><span class="sxs-lookup"><span data-stu-id="fcfe1-139">-ShareName</span></span>
<span data-ttu-id="fcfe1-140">指定共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="fcfe1-140">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="fcfe1-141">-確認</span><span class="sxs-lookup"><span data-stu-id="fcfe1-141">-Confirm</span></span>
<span data-ttu-id="fcfe1-142">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="fcfe1-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcfe1-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcfe1-143">-WhatIf</span></span>
<span data-ttu-id="fcfe1-144">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fcfe1-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcfe1-145">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fcfe1-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcfe1-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcfe1-146">CommonParameters</span></span>
<span data-ttu-id="fcfe1-147">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fcfe1-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcfe1-148">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="fcfe1-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcfe1-149">輸入</span><span class="sxs-lookup"><span data-stu-id="fcfe1-149">INPUTS</span></span>

### <span data-ttu-id="fcfe1-150">Microsoft.Azure.storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="fcfe1-150">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="fcfe1-151">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="fcfe1-151">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="fcfe1-152">輸出</span><span class="sxs-lookup"><span data-stu-id="fcfe1-152">OUTPUTS</span></span>

### <span data-ttu-id="fcfe1-153">System.Void</span><span class="sxs-lookup"><span data-stu-id="fcfe1-153">System.Void</span></span>

## <span data-ttu-id="fcfe1-154">筆記</span><span class="sxs-lookup"><span data-stu-id="fcfe1-154">NOTES</span></span>

## <span data-ttu-id="fcfe1-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="fcfe1-155">RELATED LINKS</span></span>

[<span data-ttu-id="fcfe1-156">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="fcfe1-156">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="fcfe1-157">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="fcfe1-157">Get-AzStorageFileCopyState</span></span>](./Get-AzStorageFileCopyState.md)

[<span data-ttu-id="fcfe1-158">New-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="fcfe1-158">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="fcfe1-159">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="fcfe1-159">Start-AzStorageFileCopy</span></span>](./Start-AzStorageFileCopy.md)
