---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C1648DC3-8CFD-4487-A080-D9BE25DAD258
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
ms.openlocfilehash: 870843a2cf8edc20a4de6474f35934a5d12df458
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958239"
---
# <span data-ttu-id="02c07-101">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="02c07-101">Get-AzStorageFileCopyState</span></span>

## <span data-ttu-id="02c07-102">摘要</span><span class="sxs-lookup"><span data-stu-id="02c07-102">SYNOPSIS</span></span>
<span data-ttu-id="02c07-103">取得複製操作的狀態。</span><span class="sxs-lookup"><span data-stu-id="02c07-103">Gets the state of a copy operation.</span></span>

## <span data-ttu-id="02c07-104">句法</span><span class="sxs-lookup"><span data-stu-id="02c07-104">SYNTAX</span></span>

### <span data-ttu-id="02c07-105">名</span><span class="sxs-lookup"><span data-stu-id="02c07-105">ShareName</span></span>
```
Get-AzStorageFileCopyState [-ShareName] <String> [-FilePath] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="02c07-106">檔案</span><span class="sxs-lookup"><span data-stu-id="02c07-106">File</span></span>
```
Get-AzStorageFileCopyState [-File] <CloudFile> [-WaitForComplete] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="02c07-107">說明</span><span class="sxs-lookup"><span data-stu-id="02c07-107">DESCRIPTION</span></span>
<span data-ttu-id="02c07-108">**AzStorageFileCopyState** Cmdlet 會取得 Azure 儲存空間複製作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="02c07-108">The **Get-AzStorageFileCopyState** cmdlet gets the state of an Azure Storage file copy operation.</span></span>

## <span data-ttu-id="02c07-109">示例</span><span class="sxs-lookup"><span data-stu-id="02c07-109">EXAMPLES</span></span>

### <span data-ttu-id="02c07-110">範例1：透過檔案名取得複製狀態</span><span class="sxs-lookup"><span data-stu-id="02c07-110">Example 1: Get the copy state by file name</span></span>
```
PS C:\>Get-AzStorageFileCopyState -ShareName "ContosoShare" -FilePath "ContosoFile"
```

<span data-ttu-id="02c07-111">這個命令會針對具有指定名稱的檔案，取得複製作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="02c07-111">This command gets the state of the copy operation for a file that has the specified name.</span></span>

## <span data-ttu-id="02c07-112">參數</span><span class="sxs-lookup"><span data-stu-id="02c07-112">PARAMETERS</span></span>

### <span data-ttu-id="02c07-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="02c07-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="02c07-114">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="02c07-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="02c07-115">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="02c07-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="02c07-116">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="02c07-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="02c07-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="02c07-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="02c07-118">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="02c07-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="02c07-119">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="02c07-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="02c07-120">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="02c07-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="02c07-121">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="02c07-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="02c07-122">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="02c07-122">The default value is 10.</span></span>

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

### <span data-ttu-id="02c07-123">-內容</span><span class="sxs-lookup"><span data-stu-id="02c07-123">-Context</span></span>
<span data-ttu-id="02c07-124">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="02c07-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="02c07-125">若要取得內容，請使用 [AzStorageCoNtext](./New-AzStorageContext.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="02c07-125">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="02c07-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02c07-126">-DefaultProfile</span></span>
<span data-ttu-id="02c07-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="02c07-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02c07-128">檔案</span><span class="sxs-lookup"><span data-stu-id="02c07-128">-File</span></span>
<span data-ttu-id="02c07-129">指定 **CloudFile** 物件。</span><span class="sxs-lookup"><span data-stu-id="02c07-129">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="02c07-130">您可以使用 Get-AzStorageFile Cmdlet 來建立雲端檔案或取得一個雲端檔案。</span><span class="sxs-lookup"><span data-stu-id="02c07-130">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="02c07-131">-FilePath</span><span class="sxs-lookup"><span data-stu-id="02c07-131">-FilePath</span></span>
<span data-ttu-id="02c07-132">指定檔案相對於 Azure 儲存空間共用的路徑。</span><span class="sxs-lookup"><span data-stu-id="02c07-132">Specifies the path of the file relative to an Azure Storage share.</span></span>

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

### <span data-ttu-id="02c07-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="02c07-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="02c07-134">指定要求中伺服器部分的超時時間長度。</span><span class="sxs-lookup"><span data-stu-id="02c07-134">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="02c07-135">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="02c07-135">-ShareName</span></span>
<span data-ttu-id="02c07-136">指定共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="02c07-136">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="02c07-137">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="02c07-137">-WaitForComplete</span></span>
<span data-ttu-id="02c07-138">表示此 Cmdlet 會等待複本完成。</span><span class="sxs-lookup"><span data-stu-id="02c07-138">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="02c07-139">如果您沒有指定此參數，這個 Cmdlet 會立即傳回結果。</span><span class="sxs-lookup"><span data-stu-id="02c07-139">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="02c07-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02c07-140">CommonParameters</span></span>
<span data-ttu-id="02c07-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="02c07-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02c07-142">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="02c07-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02c07-143">輸入</span><span class="sxs-lookup"><span data-stu-id="02c07-143">INPUTS</span></span>

### <span data-ttu-id="02c07-144">CloudFile （即 Azure）</span><span class="sxs-lookup"><span data-stu-id="02c07-144">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="02c07-145">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="02c07-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="02c07-146">輸出</span><span class="sxs-lookup"><span data-stu-id="02c07-146">OUTPUTS</span></span>

### <span data-ttu-id="02c07-147">CloudFile （即 Azure）</span><span class="sxs-lookup"><span data-stu-id="02c07-147">Microsoft.Azure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="02c07-148">筆記</span><span class="sxs-lookup"><span data-stu-id="02c07-148">NOTES</span></span>

## <span data-ttu-id="02c07-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="02c07-149">RELATED LINKS</span></span>

[<span data-ttu-id="02c07-150">AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="02c07-150">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="02c07-151">新-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="02c07-151">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="02c07-152">開始-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="02c07-152">Start-AzStorageFileCopy</span></span>](./Start-AzStorageFileCopy.md)

[<span data-ttu-id="02c07-153">停止 AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="02c07-153">Stop-AzStorageFileCopy</span></span>](./Stop-AzStorageFileCopy.md)
