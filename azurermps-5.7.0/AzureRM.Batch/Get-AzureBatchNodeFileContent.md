---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C9E2D9EC-3B6A-492D-B183-9856185548CD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchnodefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFileContent.md
ms.openlocfilehash: 7795182ff1594c098a2afd778c137c48dc74c955
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450708"
---
# <span data-ttu-id="ed3f0-101">Get-AzureBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="ed3f0-101">Get-AzureBatchNodeFileContent</span></span>

## <span data-ttu-id="ed3f0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ed3f0-102">SYNOPSIS</span></span>
<span data-ttu-id="ed3f0-103">取得批節點檔案。</span><span class="sxs-lookup"><span data-stu-id="ed3f0-103">Gets a Batch node file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed3f0-104">句法</span><span class="sxs-lookup"><span data-stu-id="ed3f0-104">SYNTAX</span></span>

### <span data-ttu-id="ed3f0-105">Task_Id_Path</span><span class="sxs-lookup"><span data-stu-id="ed3f0-105">Task_Id_Path</span></span>
```
Get-AzureBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationPath <String>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed3f0-106">Task_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="ed3f0-106">Task_Id_Stream</span></span>
```
Get-AzureBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed3f0-107">ComputeNode_Id_Path</span><span class="sxs-lookup"><span data-stu-id="ed3f0-107">ComputeNode_Id_Path</span></span>
```
Get-AzureBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationPath <String> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed3f0-108">ComputeNode_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="ed3f0-108">ComputeNode_Id_Stream</span></span>
```
Get-AzureBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationStream <Stream> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed3f0-109">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="ed3f0-109">InputObject_Path</span></span>
```
Get-AzureBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationPath <String> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ed3f0-110">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="ed3f0-110">InputObject_Stream</span></span>
```
Get-AzureBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed3f0-111">說明</span><span class="sxs-lookup"><span data-stu-id="ed3f0-111">DESCRIPTION</span></span>
<span data-ttu-id="ed3f0-112">**AzureBatchNodeFileContent** Cmdlet 會取得 Azure Batch-節點檔案，並將它儲存為檔案或資料流程。</span><span class="sxs-lookup"><span data-stu-id="ed3f0-112">The **Get-AzureBatchNodeFileContent** cmdlet gets an Azure Batch node file and saves it as a file or to a stream.</span></span>

## <span data-ttu-id="ed3f0-113">示例</span><span class="sxs-lookup"><span data-stu-id="ed3f0-113">EXAMPLES</span></span>

### <span data-ttu-id="ed3f0-114">範例1：取得與任務相關聯的批節點檔案，並儲存檔案</span><span class="sxs-lookup"><span data-stu-id="ed3f0-114">Example 1: Get a Batch node file associated with a task and save the file</span></span>
```
PS C:\>Get-AzureBatchNodeFileContent -JobId "Job01" -TaskId "Task01" -Path "StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="ed3f0-115">這個命令會取得名為 StdOut.txt 的節點檔案，並將它儲存到本機電腦上的 E:\PowerShell\StdOut.txt 檔路徑。</span><span class="sxs-lookup"><span data-stu-id="ed3f0-115">This command gets the node file that is named StdOut.txt, and saves it to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="ed3f0-116">StdOut.txt 節點檔案與具有 ID Job01 之作業的識別碼 Task01 相關聯。</span><span class="sxs-lookup"><span data-stu-id="ed3f0-116">The StdOut.txt node file is associated with task that has the ID Task01 for the job that has the ID Job01.</span></span>
<span data-ttu-id="ed3f0-117">使用 Get-AzureRmBatchAccountKeys Cmdlet 將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="ed3f0-117">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="ed3f0-118">範例2：取得批節點檔案，並使用管線將它儲存到指定的檔案路徑</span><span class="sxs-lookup"><span data-stu-id="ed3f0-118">Example 2: Get a Batch node file and save it to a specified file path using the pipeline</span></span>
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job02" -TaskId "Task02" -Path "StdErr.txt" -BatchContext $Context | Get-AzureBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="ed3f0-119">這個命令會透過使用 Get-AzureBatchNodeFile Cmdlet 來取得名為 StdErr.txt 的節點檔案。</span><span class="sxs-lookup"><span data-stu-id="ed3f0-119">This command gets the node file that is named StdErr.txt by using the Get-AzureBatchNodeFile cmdlet.</span></span>
<span data-ttu-id="ed3f0-120">命令會使用管線運算子，將該檔案傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ed3f0-120">The command passes that file to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ed3f0-121">目前的 Cmdlet 會將該檔案儲存到本機電腦上的 E:\PowerShell\StdOut.txt 檔路徑。</span><span class="sxs-lookup"><span data-stu-id="ed3f0-121">The current cmdlet saves that file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="ed3f0-122">StdOut.txt 節點檔案與具有 ID Job02 之作業的識別碼 Task02 相關聯。</span><span class="sxs-lookup"><span data-stu-id="ed3f0-122">The StdOut.txt node file is associated with the task that has the ID Task02 for the job that has the ID Job02.</span></span>

### <span data-ttu-id="ed3f0-123">範例3：取得與任務相關聯的批節點檔案，並將它引導至資料流程</span><span class="sxs-lookup"><span data-stu-id="ed3f0-123">Example 3: Get a Batch node file associated with a task and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzureBatchNodeFileContent -JobId "Job03" -TaskId "Task11" -Path "StdOut.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="ed3f0-124">第一個命令會使用 New-Object Cmdlet 建立串流，然後將它儲存在 $Stream 變數中。</span><span class="sxs-lookup"><span data-stu-id="ed3f0-124">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>

<span data-ttu-id="ed3f0-125">第二個命令會從具有 ID Job03 之作業的識別碼 Task11 的任務中，取得名為 StdOut.txt 的節點檔案。</span><span class="sxs-lookup"><span data-stu-id="ed3f0-125">The second command gets the node file that is named StdOut.txt from the task that has the ID Task11 for the job that has the ID Job03.</span></span>
<span data-ttu-id="ed3f0-126">命令會將檔案內容定向至 $Stream 中的資料流程。</span><span class="sxs-lookup"><span data-stu-id="ed3f0-126">The command directs file contents to the stream in $Stream.</span></span>

### <span data-ttu-id="ed3f0-127">範例4：從計算節點取得節點檔案並儲存</span><span class="sxs-lookup"><span data-stu-id="ed3f0-127">Example 4: Get a node file from a compute node and save it</span></span>
```
PS C:\>Get-AzureBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="ed3f0-128">這個命令會在擁有 ID Pool01 的池中，從 ComputeNode01 ID 為的 compute 節點中取得 Startup\StdOut.txt 節點檔案。</span><span class="sxs-lookup"><span data-stu-id="ed3f0-128">This command gets the node file Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="ed3f0-129">該命令會將檔案儲存到本機電腦上的 E:\PowerShell\StdOut.txt 檔路徑。</span><span class="sxs-lookup"><span data-stu-id="ed3f0-129">The command saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="ed3f0-130">範例5：從計算節點取得節點檔案，然後使用管線儲存該檔</span><span class="sxs-lookup"><span data-stu-id="ed3f0-130">Example 5: Get a node file from a compute node and save it by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchNodeFile -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context | Get-AzureBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="ed3f0-131">此命令會從 ComputeNode01 ID 為的計算節點中，使用 Get-AzureBatchNodeFile 來取得節點檔案 Startup\StdOut.txt。</span><span class="sxs-lookup"><span data-stu-id="ed3f0-131">This command gets the node file Startup\StdOut.txt by using Get-AzureBatchNodeFile from the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="ed3f0-132">Compute 節點位於 ID 為 Pool01 的池中。</span><span class="sxs-lookup"><span data-stu-id="ed3f0-132">The compute node is in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="ed3f0-133">命令會將該節點檔案傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ed3f0-133">The command passes that node file to the current cmdlet.</span></span>
<span data-ttu-id="ed3f0-134">該 Cmdlet 會將檔案儲存到本機電腦上的 E:\PowerShell\StdOut.txt 檔路徑。</span><span class="sxs-lookup"><span data-stu-id="ed3f0-134">That cmdlet saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="ed3f0-135">範例6：從計算節點取得節點檔案，並將它引導至資料流程</span><span class="sxs-lookup"><span data-stu-id="ed3f0-135">Example 6: Get a node file from a compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzureBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "startup\stdout.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="ed3f0-136">第一個命令會使用 New-Object Cmdlet 建立串流，然後將它儲存在 $Stream 變數中。</span><span class="sxs-lookup"><span data-stu-id="ed3f0-136">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>

<span data-ttu-id="ed3f0-137">第二個命令會從具有 ID Pool01 的 ComputeNode01 中的計算節點，取得名為 StdOut.txt 的節點檔案。</span><span class="sxs-lookup"><span data-stu-id="ed3f0-137">The second command gets the node file that is named StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="ed3f0-138">命令會將檔案內容定向至 $Stream 中的資料流程。</span><span class="sxs-lookup"><span data-stu-id="ed3f0-138">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="ed3f0-139">參數</span><span class="sxs-lookup"><span data-stu-id="ed3f0-139">PARAMETERS</span></span>

### <span data-ttu-id="ed3f0-140">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="ed3f0-140">-BatchContext</span></span>
<span data-ttu-id="ed3f0-141">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="ed3f0-141">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ed3f0-142">如果您使用 Get-AzureRmBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="ed3f0-142">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ed3f0-143">若要改為使用共用金鑰驗證，請使用 Get-AzureRmBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="ed3f0-143">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ed3f0-144">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="ed3f0-144">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ed3f0-145">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="ed3f0-145">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed3f0-146">-ByteRangeEnd</span><span class="sxs-lookup"><span data-stu-id="ed3f0-146">-ByteRangeEnd</span></span>
<span data-ttu-id="ed3f0-147">要下載之位元組範圍的結尾。</span><span class="sxs-lookup"><span data-stu-id="ed3f0-147">The end of the byte range to be downloaded.</span></span>
```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed3f0-148">-ByteRangeStart</span><span class="sxs-lookup"><span data-stu-id="ed3f0-148">-ByteRangeStart</span></span>
<span data-ttu-id="ed3f0-149">要下載的位元組範圍起始。</span><span class="sxs-lookup"><span data-stu-id="ed3f0-149">The start of the byte range to be downloaded.</span></span>
```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed3f0-150">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="ed3f0-150">-ComputeNodeId</span></span>
<span data-ttu-id="ed3f0-151">指定包含此 Cmdlet 傳回之節點檔案之計算節點的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ed3f0-151">Specifies the ID of the compute node that contains the node file that this cmdlet returns.</span></span>

```yaml
Type: String
Parameter Sets: ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed3f0-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed3f0-152">-DefaultProfile</span></span>
<span data-ttu-id="ed3f0-153">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ed3f0-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed3f0-154">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="ed3f0-154">-DestinationPath</span></span>
<span data-ttu-id="ed3f0-155">指定此 Cmdlet 儲存節點檔案的檔路徑。</span><span class="sxs-lookup"><span data-stu-id="ed3f0-155">Specifies the file path where this cmdlet saves the node file.</span></span>

```yaml
Type: String
Parameter Sets: Task_Id_Path, ComputeNode_Id_Path, InputObject_Path
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed3f0-156">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="ed3f0-156">-DestinationStream</span></span>
<span data-ttu-id="ed3f0-157">指定此 Cmdlet 寫入節點檔內容的資料流程。</span><span class="sxs-lookup"><span data-stu-id="ed3f0-157">Specifies the stream into which this cmdlet writes the node file contents.</span></span>
<span data-ttu-id="ed3f0-158">這個 Cmdlet 不會關閉或倒帶此資料流程。</span><span class="sxs-lookup"><span data-stu-id="ed3f0-158">This cmdlet does not close or rewind this stream.</span></span>

```yaml
Type: Stream
Parameter Sets: Task_Id_Stream, ComputeNode_Id_Stream, InputObject_Stream
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed3f0-159">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed3f0-159">-InputObject</span></span>
<span data-ttu-id="ed3f0-160">指定此 Cmdlet 取得的檔案，做為 **PSNodeFile** 物件。</span><span class="sxs-lookup"><span data-stu-id="ed3f0-160">Specifies the file that this cmdlet gets, as a **PSNodeFile** object.</span></span>
<span data-ttu-id="ed3f0-161">若要取得節點檔物件，請使用 Get-AzureBatchNodeFile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ed3f0-161">To obtain a node file object, use the Get-AzureBatchNodeFile cmdlet.</span></span>

```yaml
Type: PSNodeFile
Parameter Sets: InputObject_Path, InputObject_Stream
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed3f0-162">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="ed3f0-162">-JobId</span></span>
<span data-ttu-id="ed3f0-163">指定包含目標任務之作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ed3f0-163">Specifies the ID of the job that contains the target task.</span></span>

```yaml
Type: String
Parameter Sets: Task_Id_Path, Task_Id_Stream
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed3f0-164">-Path</span><span class="sxs-lookup"><span data-stu-id="ed3f0-164">-Path</span></span>
<span data-ttu-id="ed3f0-165">要下載之節點檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="ed3f0-165">The path of the node file to download.</span></span>

```yaml
Type: String
Parameter Sets: Task_Id_Path, Task_Id_Stream, ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed3f0-166">-PoolId</span><span class="sxs-lookup"><span data-stu-id="ed3f0-166">-PoolId</span></span>
<span data-ttu-id="ed3f0-167">指定包含此 Cmdlet 所取得之節點檔案之 [計算] 節點的池 ID。</span><span class="sxs-lookup"><span data-stu-id="ed3f0-167">Specifies the ID of the pool that contains the compute node that contains the node file that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed3f0-168">-TaskId</span><span class="sxs-lookup"><span data-stu-id="ed3f0-168">-TaskId</span></span>
<span data-ttu-id="ed3f0-169">指定任務的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ed3f0-169">Specifies the ID of the task.</span></span>

```yaml
Type: String
Parameter Sets: Task_Id_Path, Task_Id_Stream
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed3f0-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed3f0-170">CommonParameters</span></span>
<span data-ttu-id="ed3f0-171">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ed3f0-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed3f0-172">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ed3f0-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed3f0-173">輸入</span><span class="sxs-lookup"><span data-stu-id="ed3f0-173">INPUTS</span></span>

### <span data-ttu-id="ed3f0-174">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="ed3f0-174">BatchAccountContext</span></span>
<span data-ttu-id="ed3f0-175">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="ed3f0-175">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="ed3f0-176">PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="ed3f0-176">PSNodeFile</span></span>
<span data-ttu-id="ed3f0-177">形參 "InputObject" 接受管線中 "PSNodeFile" 類型的值</span><span class="sxs-lookup"><span data-stu-id="ed3f0-177">Parameter 'InputObject' accepts value of type 'PSNodeFile' from the pipeline</span></span>

## <span data-ttu-id="ed3f0-178">輸出</span><span class="sxs-lookup"><span data-stu-id="ed3f0-178">OUTPUTS</span></span>

## <span data-ttu-id="ed3f0-179">筆記</span><span class="sxs-lookup"><span data-stu-id="ed3f0-179">NOTES</span></span>

## <span data-ttu-id="ed3f0-180">相關連結</span><span class="sxs-lookup"><span data-stu-id="ed3f0-180">RELATED LINKS</span></span>

[<span data-ttu-id="ed3f0-181">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="ed3f0-181">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="ed3f0-182">AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="ed3f0-182">Get-AzureBatchNodeFile</span></span>](./Get-AzureBatchNodeFile.md)

[<span data-ttu-id="ed3f0-183">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ed3f0-183">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


