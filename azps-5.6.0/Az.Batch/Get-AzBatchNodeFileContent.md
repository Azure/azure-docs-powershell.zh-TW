---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C9E2D9EC-3B6A-492D-B183-9856185548CD
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchnodefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFileContent.md
ms.openlocfilehash: 5790d217a63b7c2ef3aa7011d5f8a708df1dfbac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909786"
---
# <span data-ttu-id="eb8b9-101">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="eb8b9-101">Get-AzBatchNodeFileContent</span></span>

## <span data-ttu-id="eb8b9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="eb8b9-102">SYNOPSIS</span></span>
<span data-ttu-id="eb8b9-103">獲得批次處理節點檔案。</span><span class="sxs-lookup"><span data-stu-id="eb8b9-103">Gets a Batch node file.</span></span>

## <span data-ttu-id="eb8b9-104">語法</span><span class="sxs-lookup"><span data-stu-id="eb8b9-104">SYNTAX</span></span>

### <span data-ttu-id="eb8b9-105">Task_Id_Path</span><span class="sxs-lookup"><span data-stu-id="eb8b9-105">Task_Id_Path</span></span>
```
Get-AzBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationPath <String>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb8b9-106">Task_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="eb8b9-106">Task_Id_Stream</span></span>
```
Get-AzBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb8b9-107">ComputeNode_Id_Path</span><span class="sxs-lookup"><span data-stu-id="eb8b9-107">ComputeNode_Id_Path</span></span>
```
Get-AzBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationPath <String> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb8b9-108">ComputeNode_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="eb8b9-108">ComputeNode_Id_Stream</span></span>
```
Get-AzBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationStream <Stream> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb8b9-109">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="eb8b9-109">InputObject_Path</span></span>
```
Get-AzBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationPath <String> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eb8b9-110">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="eb8b9-110">InputObject_Stream</span></span>
```
Get-AzBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationStream <Stream> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eb8b9-111">描述</span><span class="sxs-lookup"><span data-stu-id="eb8b9-111">DESCRIPTION</span></span>
<span data-ttu-id="eb8b9-112">**Get-AzBatchNodeFileContent** Cmdlet 會取得 Azure Batch-節點檔案，並另存為檔案或串流。</span><span class="sxs-lookup"><span data-stu-id="eb8b9-112">The **Get-AzBatchNodeFileContent** cmdlet gets an Azure Batch node file and saves it as a file or to a stream.</span></span>

## <span data-ttu-id="eb8b9-113">例子</span><span class="sxs-lookup"><span data-stu-id="eb8b9-113">EXAMPLES</span></span>

### <span data-ttu-id="eb8b9-114">範例 1：取得與工作相關聯的批次處理節點檔案並儲存該檔案</span><span class="sxs-lookup"><span data-stu-id="eb8b9-114">Example 1: Get a Batch node file associated with a task and save the file</span></span>
```
PS C:\>Get-AzBatchNodeFileContent -JobId "Job01" -TaskId "Task01" -Path "StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="eb8b9-115">此命令會獲得名為 StdOut.txt 的節點檔案，並E:\PowerShell\StdOut.txt到本地電腦的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="eb8b9-115">This command gets the node file that is named StdOut.txt, and saves it to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="eb8b9-116">StdOut.txt節點檔案與具有識別碼 Job01 的工作具有識別碼工作01 的工作相關聯。</span><span class="sxs-lookup"><span data-stu-id="eb8b9-116">The StdOut.txt node file is associated with task that has the ID Task01 for the job that has the ID Job01.</span></span>
<span data-ttu-id="eb8b9-117">使用 Get-AzBatchAccountKey Cmdlet 將上下文指派給$CoNtext變數。</span><span class="sxs-lookup"><span data-stu-id="eb8b9-117">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="eb8b9-118">範例 2：取得批次節點檔案，然後使用管線將其儲存到指定的檔案路徑</span><span class="sxs-lookup"><span data-stu-id="eb8b9-118">Example 2: Get a Batch node file and save it to a specified file path using the pipeline</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job02" -TaskId "Task02" -Path "StdErr.txt" -BatchContext $Context | Get-AzBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="eb8b9-119">此命令會使用 Cmdlet StdErr.txt名為 Get-AzBatchNodeFile檔案。</span><span class="sxs-lookup"><span data-stu-id="eb8b9-119">This command gets the node file that is named StdErr.txt by using the Get-AzBatchNodeFile cmdlet.</span></span>
<span data-ttu-id="eb8b9-120">該命令會使用管線運算子，將檔案傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eb8b9-120">The command passes that file to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="eb8b9-121">目前的 Cmdlet 會將該檔案E:\PowerShell\StdOut.txt本地電腦的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="eb8b9-121">The current cmdlet saves that file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="eb8b9-122">StdOut.txt節點檔案與具有識別碼 Job02 的工作具有識別碼工作02 的工作相關聯。</span><span class="sxs-lookup"><span data-stu-id="eb8b9-122">The StdOut.txt node file is associated with the task that has the ID Task02 for the job that has the ID Job02.</span></span>

### <span data-ttu-id="eb8b9-123">範例 3：取得與工作相關聯的批次處理節點檔案，並引導它至串流</span><span class="sxs-lookup"><span data-stu-id="eb8b9-123">Example 3: Get a Batch node file associated with a task and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchNodeFileContent -JobId "Job03" -TaskId "Task11" -Path "StdOut.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="eb8b9-124">第一個命令會使用 New-Object Cmdlet 建立串流，然後將它儲存在 $Stream 變數中。</span><span class="sxs-lookup"><span data-stu-id="eb8b9-124">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="eb8b9-125">第二個命令會從具有識別碼 Job03 的工作StdOut.txt識別碼工作 11 的工作中，獲得名稱為 StdOut.txt 的節點檔案。</span><span class="sxs-lookup"><span data-stu-id="eb8b9-125">The second command gets the node file that is named StdOut.txt from the task that has the ID Task11 for the job that has the ID Job03.</span></span>
<span data-ttu-id="eb8b9-126">命令會以命令將檔案內容引導至 $Stream。</span><span class="sxs-lookup"><span data-stu-id="eb8b9-126">The command directs file contents to the stream in $Stream.</span></span>

### <span data-ttu-id="eb8b9-127">範例 4：從計算節點取得節點檔案並儲存</span><span class="sxs-lookup"><span data-stu-id="eb8b9-127">Example 4: Get a node file from a compute node and save it</span></span>
```
PS C:\>Get-AzBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="eb8b9-128">此命令會從具有識別碼Startup\StdOut.txt 01 之資料集中具有 ID ComputeNode01 的計算節點中，獲得節點檔案。</span><span class="sxs-lookup"><span data-stu-id="eb8b9-128">This command gets the node file Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="eb8b9-129">該命令會將檔案E:\PowerShell\StdOut.txt本地電腦的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="eb8b9-129">The command saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="eb8b9-130">範例 5：從計算節點取得節點檔案，然後使用管線儲存</span><span class="sxs-lookup"><span data-stu-id="eb8b9-130">Example 5: Get a node file from a compute node and save it by using the pipeline</span></span>
```
PS C:\>Get-AzBatchNodeFile -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context | Get-AzBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="eb8b9-131">此命令會使用具有 ID ComputeNode01 之Startup\StdOut.txt計算節點Get-AzBatchNodeFile的節點檔案。</span><span class="sxs-lookup"><span data-stu-id="eb8b9-131">This command gets the node file Startup\StdOut.txt by using Get-AzBatchNodeFile from the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="eb8b9-132">計算節點位於具有 ID Pool01 的集中。</span><span class="sxs-lookup"><span data-stu-id="eb8b9-132">The compute node is in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="eb8b9-133">該命令會將該節點檔案傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eb8b9-133">The command passes that node file to the current cmdlet.</span></span>
<span data-ttu-id="eb8b9-134">該 Cmdlet 會將檔案E:\PowerShell\StdOut.txt本地電腦的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="eb8b9-134">That cmdlet saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="eb8b9-135">範例 6：從計算節點取得節點檔案，並引導它至串流</span><span class="sxs-lookup"><span data-stu-id="eb8b9-135">Example 6: Get a node file from a compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "startup\stdout.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="eb8b9-136">第一個命令會使用 New-Object Cmdlet 建立串流，然後將它儲存在 $Stream 變數中。</span><span class="sxs-lookup"><span data-stu-id="eb8b9-136">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="eb8b9-137">第二個命令會從具有 ID pool01 之StdOut.txt識別碼 ComputeNode01 的計算節點中，獲得名為 StdOut.txt 的節點檔案。</span><span class="sxs-lookup"><span data-stu-id="eb8b9-137">The second command gets the node file that is named StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="eb8b9-138">命令會以命令將檔案內容引導至 $Stream。</span><span class="sxs-lookup"><span data-stu-id="eb8b9-138">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="eb8b9-139">參數</span><span class="sxs-lookup"><span data-stu-id="eb8b9-139">PARAMETERS</span></span>

### <span data-ttu-id="eb8b9-140">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="eb8b9-140">-BatchContext</span></span>
<span data-ttu-id="eb8b9-141">指定此 Cmdlet 用來與批次處理服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="eb8b9-141">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="eb8b9-142">如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="eb8b9-142">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="eb8b9-143">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="eb8b9-143">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="eb8b9-144">使用共用金鑰驗證時，預設會使用主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="eb8b9-144">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="eb8b9-145">若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。</span><span class="sxs-lookup"><span data-stu-id="eb8b9-145">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb8b9-146">-ByteRangeEnd</span><span class="sxs-lookup"><span data-stu-id="eb8b9-146">-ByteRangeEnd</span></span>
<span data-ttu-id="eb8b9-147">要下載的位元組範圍結尾。</span><span class="sxs-lookup"><span data-stu-id="eb8b9-147">The end of the byte range to be downloaded.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb8b9-148">-ByteRangeStart</span><span class="sxs-lookup"><span data-stu-id="eb8b9-148">-ByteRangeStart</span></span>
<span data-ttu-id="eb8b9-149">要下載的位元組範圍的開始。</span><span class="sxs-lookup"><span data-stu-id="eb8b9-149">The start of the byte range to be downloaded.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb8b9-150">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="eb8b9-150">-ComputeNodeId</span></span>
<span data-ttu-id="eb8b9-151">指定包含此 Cmdlet 所返回之節點檔案的計算節點識別碼。</span><span class="sxs-lookup"><span data-stu-id="eb8b9-151">Specifies the ID of the compute node that contains the node file that this cmdlet returns.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb8b9-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb8b9-152">-DefaultProfile</span></span>
<span data-ttu-id="eb8b9-153">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="eb8b9-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb8b9-154">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="eb8b9-154">-DestinationPath</span></span>
<span data-ttu-id="eb8b9-155">指定此 Cmdlet 將節點檔案另存的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="eb8b9-155">Specifies the file path where this cmdlet saves the node file.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, ComputeNode_Id_Path, InputObject_Path
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb8b9-156">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="eb8b9-156">-DestinationStream</span></span>
<span data-ttu-id="eb8b9-157">指定此 Cmdlet 寫入節點檔案內容的資料流程。</span><span class="sxs-lookup"><span data-stu-id="eb8b9-157">Specifies the stream into which this cmdlet writes the node file contents.</span></span>
<span data-ttu-id="eb8b9-158">此 Cmdlet 不會關閉或倒帶此串流。</span><span class="sxs-lookup"><span data-stu-id="eb8b9-158">This cmdlet does not close or rewind this stream.</span></span>

```yaml
Type: System.IO.Stream
Parameter Sets: Task_Id_Stream, ComputeNode_Id_Stream, InputObject_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb8b9-159">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eb8b9-159">-InputObject</span></span>
<span data-ttu-id="eb8b9-160">指定此 Cmdlet 以 **PSNodeFile** 物件獲得之檔案。</span><span class="sxs-lookup"><span data-stu-id="eb8b9-160">Specifies the file that this cmdlet gets, as a **PSNodeFile** object.</span></span>
<span data-ttu-id="eb8b9-161">若要取得節點檔案物件，請使用 Get-AzBatchNodeFile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eb8b9-161">To obtain a node file object, use the Get-AzBatchNodeFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSNodeFile
Parameter Sets: InputObject_Path, InputObject_Stream
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb8b9-162">-JobId</span><span class="sxs-lookup"><span data-stu-id="eb8b9-162">-JobId</span></span>
<span data-ttu-id="eb8b9-163">指定包含目標工作的工作的識別碼。</span><span class="sxs-lookup"><span data-stu-id="eb8b9-163">Specifies the ID of the job that contains the target task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb8b9-164">-路徑</span><span class="sxs-lookup"><span data-stu-id="eb8b9-164">-Path</span></span>
<span data-ttu-id="eb8b9-165">要下載的節點檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="eb8b9-165">The path of the node file to download.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream, ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb8b9-166">-PoolId</span><span class="sxs-lookup"><span data-stu-id="eb8b9-166">-PoolId</span></span>
<span data-ttu-id="eb8b9-167">指定包含包含此 Cmdlet 所獲取之節點檔案之計算節點的集區識別碼。</span><span class="sxs-lookup"><span data-stu-id="eb8b9-167">Specifies the ID of the pool that contains the compute node that contains the node file that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb8b9-168">-TaskId</span><span class="sxs-lookup"><span data-stu-id="eb8b9-168">-TaskId</span></span>
<span data-ttu-id="eb8b9-169">指定任務的識別碼。</span><span class="sxs-lookup"><span data-stu-id="eb8b9-169">Specifies the ID of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb8b9-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb8b9-170">CommonParameters</span></span>
<span data-ttu-id="eb8b9-171">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="eb8b9-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb8b9-172">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eb8b9-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb8b9-173">輸入</span><span class="sxs-lookup"><span data-stu-id="eb8b9-173">INPUTS</span></span>

### <span data-ttu-id="eb8b9-174">System.String</span><span class="sxs-lookup"><span data-stu-id="eb8b9-174">System.String</span></span>

### <span data-ttu-id="eb8b9-175">Microsoft.Azure.Commands.Batch。Models.PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="eb8b9-175">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>

### <span data-ttu-id="eb8b9-176">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="eb8b9-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="eb8b9-177">輸出</span><span class="sxs-lookup"><span data-stu-id="eb8b9-177">OUTPUTS</span></span>

### <span data-ttu-id="eb8b9-178">System.Void</span><span class="sxs-lookup"><span data-stu-id="eb8b9-178">System.Void</span></span>

## <span data-ttu-id="eb8b9-179">筆記</span><span class="sxs-lookup"><span data-stu-id="eb8b9-179">NOTES</span></span>

## <span data-ttu-id="eb8b9-180">相關連結</span><span class="sxs-lookup"><span data-stu-id="eb8b9-180">RELATED LINKS</span></span>

[<span data-ttu-id="eb8b9-181">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="eb8b9-181">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="eb8b9-182">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="eb8b9-182">Get-AzBatchNodeFile</span></span>](./Get-AzBatchNodeFile.md)

[<span data-ttu-id="eb8b9-183">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="eb8b9-183">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
