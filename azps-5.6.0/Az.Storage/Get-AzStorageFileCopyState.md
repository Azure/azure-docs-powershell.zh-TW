---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C1648DC3-8CFD-4487-A080-D9BE25DAD258
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragefilecopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
ms.openlocfilehash: c86a2d616334729df6b7fa57a25cc51750bbff1a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909297"
---
# <span data-ttu-id="b8bc9-101">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="b8bc9-101">Get-AzStorageFileCopyState</span></span>

## <span data-ttu-id="b8bc9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b8bc9-102">SYNOPSIS</span></span>
<span data-ttu-id="b8bc9-103">獲得複製作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="b8bc9-103">Gets the state of a copy operation.</span></span>

## <span data-ttu-id="b8bc9-104">語法</span><span class="sxs-lookup"><span data-stu-id="b8bc9-104">SYNTAX</span></span>

### <span data-ttu-id="b8bc9-105">ShareName</span><span class="sxs-lookup"><span data-stu-id="b8bc9-105">ShareName</span></span>
```
Get-AzStorageFileCopyState [-ShareName] <String> [-FilePath] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="b8bc9-106">檔</span><span class="sxs-lookup"><span data-stu-id="b8bc9-106">File</span></span>
```
Get-AzStorageFileCopyState [-File] <CloudFile> [-WaitForComplete] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="b8bc9-107">描述</span><span class="sxs-lookup"><span data-stu-id="b8bc9-107">DESCRIPTION</span></span>
<span data-ttu-id="b8bc9-108">**Get-AzStorageFileCopyState** Cmdlet 會取得 Azure 儲存體檔案複製作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="b8bc9-108">The **Get-AzStorageFileCopyState** cmdlet gets the state of an Azure Storage file copy operation.</span></span>
<span data-ttu-id="b8bc9-109">它應在複製目標檔案上執行。</span><span class="sxs-lookup"><span data-stu-id="b8bc9-109">It should run on the copy destination file.</span></span>

## <span data-ttu-id="b8bc9-110">例子</span><span class="sxs-lookup"><span data-stu-id="b8bc9-110">EXAMPLES</span></span>

### <span data-ttu-id="b8bc9-111">範例 1：根據檔案名取得複製狀態</span><span class="sxs-lookup"><span data-stu-id="b8bc9-111">Example 1: Get the copy state by file name</span></span>
```
PS C:\>Get-AzStorageFileCopyState -ShareName "ContosoShare" -FilePath "ContosoFile"
```

<span data-ttu-id="b8bc9-112">此命令會針對具有指定名稱的檔案，獲得複製作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="b8bc9-112">This command gets the state of the copy operation for a file that has the specified name.</span></span>

### <span data-ttu-id="b8bc9-113">範例 2：啟動複製和管線以取得複製狀態</span><span class="sxs-lookup"><span data-stu-id="b8bc9-113">Example 2: Start Copy and pipeline to get the copy status</span></span>
```
C:\PS> $destfile = Start-AzStorageFileCopy -SrcShareName "contososhare" -SrcFilePath "contosofile" -DestShareName "contososhare2" -destfilepath "contosofile_copy"  

C:\PS> $destfile | Get-AzStorageFileCopyState
```

<span data-ttu-id="b8bc9-114">第一個命令會開始將檔案 "contosofile" 複製到 "contosofile_copy"，然後輸出 destiantion 檔案物件。</span><span class="sxs-lookup"><span data-stu-id="b8bc9-114">The first command starts copy file "contosofile" to "contosofile_copy", and output the destiantion file object.</span></span> <span data-ttu-id="b8bc9-115">第二個命令管線將 destiantion 檔案物件用於 Get-AzStorageFileCopyState，以取得檔案複製狀態。</span><span class="sxs-lookup"><span data-stu-id="b8bc9-115">The second command pipeline the destiantion file object to Get-AzStorageFileCopyState, to get file copy state.</span></span>

## <span data-ttu-id="b8bc9-116">參數</span><span class="sxs-lookup"><span data-stu-id="b8bc9-116">PARAMETERS</span></span>

### <span data-ttu-id="b8bc9-117">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b8bc9-117">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b8bc9-118">指定一個服務要求用戶端的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="b8bc9-118">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b8bc9-119">如果前一個通話在指定的時間間隔內失敗，此 Cmdlet 會重新重試要求。</span><span class="sxs-lookup"><span data-stu-id="b8bc9-119">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b8bc9-120">如果此 Cmdlet 在間隔經過之前未收到成功回應，此 Cmdlet 會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="b8bc9-120">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="b8bc9-121">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b8bc9-121">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b8bc9-122">指定同時進行的最大網路通話數。</span><span class="sxs-lookup"><span data-stu-id="b8bc9-122">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="b8bc9-123">您可以使用此參數來限制並行，以節流本地 CPU 和頻寬使用量，方法為指定並行網路通話的數量上限。</span><span class="sxs-lookup"><span data-stu-id="b8bc9-123">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="b8bc9-124">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="b8bc9-124">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="b8bc9-125">此參數有助於減少低頻寬環境的網路連接問題，例如每秒 100 KB。</span><span class="sxs-lookup"><span data-stu-id="b8bc9-125">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="b8bc9-126">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="b8bc9-126">The default value is 10.</span></span>

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

### <span data-ttu-id="b8bc9-127">-內容</span><span class="sxs-lookup"><span data-stu-id="b8bc9-127">-Context</span></span>
<span data-ttu-id="b8bc9-128">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="b8bc9-128">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="b8bc9-129">若要取得內容，請使用 [New-AzStorageCoNtext](./New-AzStorageContext.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b8bc9-129">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="b8bc9-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8bc9-130">-DefaultProfile</span></span>
<span data-ttu-id="b8bc9-131">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b8bc9-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8bc9-132">-檔案</span><span class="sxs-lookup"><span data-stu-id="b8bc9-132">-File</span></span>
<span data-ttu-id="b8bc9-133">指定 **CloudFile** 物件。</span><span class="sxs-lookup"><span data-stu-id="b8bc9-133">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="b8bc9-134">您可以使用 Cmdlet 建立雲端檔案，或取得Get-AzStorageFile檔案。</span><span class="sxs-lookup"><span data-stu-id="b8bc9-134">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="b8bc9-135">-FilePath</span><span class="sxs-lookup"><span data-stu-id="b8bc9-135">-FilePath</span></span>
<span data-ttu-id="b8bc9-136">指定檔案相對於 Azure 儲存空間共用的路徑。</span><span class="sxs-lookup"><span data-stu-id="b8bc9-136">Specifies the path of the file relative to an Azure Storage share.</span></span>

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

### <span data-ttu-id="b8bc9-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b8bc9-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b8bc9-138">指定要求的伺服器部分之時間長度。</span><span class="sxs-lookup"><span data-stu-id="b8bc9-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="b8bc9-139">-ShareName</span><span class="sxs-lookup"><span data-stu-id="b8bc9-139">-ShareName</span></span>
<span data-ttu-id="b8bc9-140">指定共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="b8bc9-140">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="b8bc9-141">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="b8bc9-141">-WaitForComplete</span></span>
<span data-ttu-id="b8bc9-142">表示此 Cmdlet 會等待複製完成。</span><span class="sxs-lookup"><span data-stu-id="b8bc9-142">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="b8bc9-143">如果您未指定此參數，此 Cmdlet 會立即返回結果。</span><span class="sxs-lookup"><span data-stu-id="b8bc9-143">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="b8bc9-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8bc9-144">CommonParameters</span></span>
<span data-ttu-id="b8bc9-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b8bc9-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8bc9-146">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="b8bc9-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8bc9-147">輸入</span><span class="sxs-lookup"><span data-stu-id="b8bc9-147">INPUTS</span></span>

### <span data-ttu-id="b8bc9-148">Microsoft.Azure.storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="b8bc9-148">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="b8bc9-149">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="b8bc9-149">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b8bc9-150">輸出</span><span class="sxs-lookup"><span data-stu-id="b8bc9-150">OUTPUTS</span></span>

### <span data-ttu-id="b8bc9-151">Microsoft.Azure.storage.File.CopyState</span><span class="sxs-lookup"><span data-stu-id="b8bc9-151">Microsoft.Azure.Storage.File.CopyState</span></span>

## <span data-ttu-id="b8bc9-152">筆記</span><span class="sxs-lookup"><span data-stu-id="b8bc9-152">NOTES</span></span>

## <span data-ttu-id="b8bc9-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="b8bc9-153">RELATED LINKS</span></span>

[<span data-ttu-id="b8bc9-154">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="b8bc9-154">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="b8bc9-155">New-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="b8bc9-155">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="b8bc9-156">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="b8bc9-156">Start-AzStorageFileCopy</span></span>](./Start-AzStorageFileCopy.md)

[<span data-ttu-id="b8bc9-157">Stop-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="b8bc9-157">Stop-AzStorageFileCopy</span></span>](./Stop-AzStorageFileCopy.md)
