---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 38ED2854-23D0-400E-A5C8-239346B2AF99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchnodefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFile.md
ms.openlocfilehash: ac9a49b52dd2fecea12e3084e4d86077ddb06cb5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450711"
---
# <span data-ttu-id="605d2-101">Get-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="605d2-101">Get-AzureBatchNodeFile</span></span>

## <span data-ttu-id="605d2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="605d2-102">SYNOPSIS</span></span>
<span data-ttu-id="605d2-103">取得批節點檔案的屬性。</span><span class="sxs-lookup"><span data-stu-id="605d2-103">Gets the properties of Batch node files.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="605d2-104">句法</span><span class="sxs-lookup"><span data-stu-id="605d2-104">SYNTAX</span></span>

### <span data-ttu-id="605d2-105">ComputeNode_Id (預設) </span><span class="sxs-lookup"><span data-stu-id="605d2-105">ComputeNode_Id (Default)</span></span>
```
Get-AzureBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> [[-Path] <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="605d2-106">Task_Id</span><span class="sxs-lookup"><span data-stu-id="605d2-106">Task_Id</span></span>
```
Get-AzureBatchNodeFile -JobId <String> -TaskId <String> [[-Path] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="605d2-107">Task_ODataFilter</span><span class="sxs-lookup"><span data-stu-id="605d2-107">Task_ODataFilter</span></span>
```
Get-AzureBatchNodeFile -JobId <String> -TaskId <String> [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="605d2-108">ParentTask</span><span class="sxs-lookup"><span data-stu-id="605d2-108">ParentTask</span></span>
```
Get-AzureBatchNodeFile [[-Task] <PSCloudTask>] [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="605d2-109">ComputeNode_ODataFilter</span><span class="sxs-lookup"><span data-stu-id="605d2-109">ComputeNode_ODataFilter</span></span>
```
Get-AzureBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Recursive] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="605d2-110">ParentComputeNode</span><span class="sxs-lookup"><span data-stu-id="605d2-110">ParentComputeNode</span></span>
```
Get-AzureBatchNodeFile [[-ComputeNode] <PSComputeNode>] [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="605d2-111">說明</span><span class="sxs-lookup"><span data-stu-id="605d2-111">DESCRIPTION</span></span>
<span data-ttu-id="605d2-112">**AzureBatchNodeFile** Cmdlet 會取得任務或計算節點之 Azure Batch-節點檔案的屬性。</span><span class="sxs-lookup"><span data-stu-id="605d2-112">The **Get-AzureBatchNodeFile** cmdlet gets the properties of the Azure Batch node files of a task or compute node.</span></span>
<span data-ttu-id="605d2-113">若要縮小結果範圍，您可以指定開放資料通訊協定 (OData) 篩選。</span><span class="sxs-lookup"><span data-stu-id="605d2-113">To narrow your results, you can specify an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="605d2-114">如果您指定工作，但不是篩選，此 Cmdlet 會傳回該工作所有節點檔案的屬性。</span><span class="sxs-lookup"><span data-stu-id="605d2-114">If you specify a task, but not a filter, this cmdlet returns properties for all node files for that task.</span></span>
<span data-ttu-id="605d2-115">如果您指定的是計算節點，但不是篩選，這個 Cmdlet 會傳回該計算節點之所有節點檔案的屬性。</span><span class="sxs-lookup"><span data-stu-id="605d2-115">If you specify a compute node, but not a filter, this cmdlet returns properties for all node files for that compute node.</span></span>

## <span data-ttu-id="605d2-116">示例</span><span class="sxs-lookup"><span data-stu-id="605d2-116">EXAMPLES</span></span>

### <span data-ttu-id="605d2-117">範例1：取得與任務相關聯之節點檔的屬性</span><span class="sxs-lookup"><span data-stu-id="605d2-117">Example 1: Get the properties of a node file associated with a task</span></span>
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "Stdout.txt" -BatchContext $Context
IsDirectory Name          Properties                                      Url

----------- ----          ----------                                      ---

False       StdOut.txt    Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="605d2-118">這個命令會取得 StdOut.txt 節點檔案的屬性，該檔與具有 ID 作業的作業中具有識別碼 Task26 的任務000001。</span><span class="sxs-lookup"><span data-stu-id="605d2-118">This command gets the properties of the StdOut.txt node file associated with the task that has the ID Task26 in the job that has the ID Job-000001.</span></span>
<span data-ttu-id="605d2-119">使用 Get-AzureRmBatchAccountKeys Cmdlet 將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="605d2-119">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="605d2-120">範例2：使用篩選來取得與任務相關聯之節點檔案的屬性</span><span class="sxs-lookup"><span data-stu-id="605d2-120">Example 2: Get the properties of node files associated with a task by using a filter</span></span>
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job-00002" -TaskId "Task26" -Filter "startswith(name,'St')" -BatchContext $Context
IsDirectory Name        Properties                                      Url

----------- ----        ----------                                      ---

False       StdErr.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       StdOut.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="605d2-121">這個命令會取得名稱以 st 開頭，且與 ID 為 Task26 的工作（在作業中具有 ID 作業-00002）相關聯之節點檔案的屬性。</span><span class="sxs-lookup"><span data-stu-id="605d2-121">This command gets the properties of the node files whose names start with st and are associated with task that has the ID Task26 under job that has the ID Job-00002.</span></span>

### <span data-ttu-id="605d2-122">範例3：遞迴取得與任務相關聯之節點檔案的屬性</span><span class="sxs-lookup"><span data-stu-id="605d2-122">Example 3: Recursively get the properties of node files associated with a task</span></span>
```
PS C:\>Get-AzureBatchTask "Job-00003" "Task31" -BatchContext $Context | Get-AzureBatchNodeFile -Recursive -BatchContext $Context
IsDirectory Name             Properties                                      Url

----------- ----             ----------                                      ---

False       ProcessEnv.cmd   Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       StdErr.txt       Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       StdOut.txt       Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
True        wd                                                               https://cmdletexample.westus.Batch.contoso... 
False       wd\newFile.txt   Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="605d2-123">這個命令會取得與作業作業-00003 中具有識別碼 Task31 之任務相關聯之所有檔案的屬性。</span><span class="sxs-lookup"><span data-stu-id="605d2-123">This command gets the properties of all files associated with the task that has the ID Task31 in job Job-00003.</span></span>
<span data-ttu-id="605d2-124">這個命令會指定 *Recursive* 參數。</span><span class="sxs-lookup"><span data-stu-id="605d2-124">This command specifies the *Recursive* parameter.</span></span>
<span data-ttu-id="605d2-125">因此，此 Cmdlet 會執行遞迴檔案搜尋，並傳回 wd\newFile.txt 節點檔案。</span><span class="sxs-lookup"><span data-stu-id="605d2-125">Therefore, the cmdlet performs a recursive file search is performed, and returns the wd\newFile.txt node file.</span></span>

### <span data-ttu-id="605d2-126">範例4：從計算節點取得單一檔案</span><span class="sxs-lookup"><span data-stu-id="605d2-126">Example 4: Get a single file from a compute node</span></span>
```
PS C:\>Get-AzureBatchNodeFile -PoolId "Pool22" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context
IsDirectory Name                    Properties                                      Url
----------- ----                    ----------                                      ---
False       startup\stdout.txt      Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="605d2-127">這個命令會從具有 ID Pool22 的 ComputeNode01 中的計算節點，取得名 Startup\StdOut.txt 為的檔案。</span><span class="sxs-lookup"><span data-stu-id="605d2-127">This command gets the file that is named Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>

### <span data-ttu-id="605d2-128">範例5：從計算節點取得資料夾下的所有檔案</span><span class="sxs-lookup"><span data-stu-id="605d2-128">Example 5: Get all files under a folder from a compute node</span></span>
```
PS C:\>Get-AzureBatchNodeFile -PoolId "Pool22" -ComputeNodeId "ComputeNode01" -Filter "startswith(name,'startup')" -Recursive -BatchContext $Context
IsDirectory Name                      Properties                                      Url
----------- ----                      ----------                                      ---
True        startup                                                                   https://cmdletexample.westus.Batch.contoso... 
False       startup\ProcessEnv.cmd    Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       startup\stderr.txt        Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       startup\stdout.txt        Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
True        startup\wd                                                                https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="605d2-129">這個命令會從擁有 ID Pool22 的 ComputeNode01 中的 [計算] 節點，取得 [啟動] 資料夾底下的所有檔案。</span><span class="sxs-lookup"><span data-stu-id="605d2-129">This command gets all the files under the startup folder from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>
<span data-ttu-id="605d2-130">這個 Cmdlet 會指定 *Recursive* 參數。</span><span class="sxs-lookup"><span data-stu-id="605d2-130">This cmdlet specifies the *Recursive* parameter.</span></span>

### <span data-ttu-id="605d2-131">範例6：從計算節點的根資料夾取得檔案</span><span class="sxs-lookup"><span data-stu-id="605d2-131">Example 6: Get files from the root folder of a compute node</span></span>
```
PS C:\>Get-AzureBatchComputeNode "Pool22" -Id "ComputeNode01" -BatchContext $Context | Get-AzureBatchNodeFile -BatchContext $Context
IsDirectory Name           Properties       Url
----------- ----           ----------       ---
True        shared                          https://cmdletexample.westus.Batch.contoso... 
True        startup                         https://cmdletexample.westus.Batch.contoso... 
True        workitems                       https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="605d2-132">這個命令會在擁有 ID Pool22 的池中，取得具有識別碼 ComputeNode01 之 [計算] 節點根資料夾的所有檔案。</span><span class="sxs-lookup"><span data-stu-id="605d2-132">This command gets all the files at the root folder of the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>

## <span data-ttu-id="605d2-133">參數</span><span class="sxs-lookup"><span data-stu-id="605d2-133">PARAMETERS</span></span>

### <span data-ttu-id="605d2-134">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="605d2-134">-BatchContext</span></span>
<span data-ttu-id="605d2-135">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="605d2-135">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="605d2-136">如果您使用 Get-AzureRmBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="605d2-136">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="605d2-137">若要改為使用共用金鑰驗證，請使用 Get-AzureRmBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="605d2-137">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="605d2-138">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="605d2-138">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="605d2-139">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="605d2-139">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="605d2-140">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="605d2-140">-ComputeNode</span></span>
<span data-ttu-id="605d2-141">指定包含批節點檔案的計算節點（作為 **PSComputeNode** 物件）。</span><span class="sxs-lookup"><span data-stu-id="605d2-141">Specifies the compute node, as a **PSComputeNode** object, that contains the Batch node files.</span></span>
<span data-ttu-id="605d2-142">若要取得計算節點物件，請使用 Get-AzureBatchComputeNode Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="605d2-142">To obtain a compute node object, use the Get-AzureBatchComputeNode cmdlet.</span></span>

```yaml
Type: PSComputeNode
Parameter Sets: ParentComputeNode
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="605d2-143">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="605d2-143">-ComputeNodeId</span></span>
<span data-ttu-id="605d2-144">指定包含批節點檔案之計算節點的識別碼。</span><span class="sxs-lookup"><span data-stu-id="605d2-144">Specifies the ID of the compute node that contains the Batch node files.</span></span>

```yaml
Type: String
Parameter Sets: ComputeNode_Id, ComputeNode_ODataFilter
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="605d2-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="605d2-145">-DefaultProfile</span></span>
<span data-ttu-id="605d2-146">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="605d2-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="605d2-147">-篩選</span><span class="sxs-lookup"><span data-stu-id="605d2-147">-Filter</span></span>
<span data-ttu-id="605d2-148">指定 OData 篩選子句。</span><span class="sxs-lookup"><span data-stu-id="605d2-148">Specifies an OData filter clause.</span></span>
<span data-ttu-id="605d2-149">這個 Cmdlet 會傳回與此參數指定之篩選相符的節點檔案屬性。</span><span class="sxs-lookup"><span data-stu-id="605d2-149">This cmdlet returns properties for node files that match the filter that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Task_ODataFilter, ParentTask, ComputeNode_ODataFilter, ParentComputeNode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="605d2-150">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="605d2-150">-JobId</span></span>
<span data-ttu-id="605d2-151">指定包含目標任務之作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="605d2-151">Specifies the ID of the job that contains the target task.</span></span>

```yaml
Type: String
Parameter Sets: Task_Id, Task_ODataFilter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="605d2-152">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="605d2-152">-MaxCount</span></span>
<span data-ttu-id="605d2-153">指定此 Cmdlet 傳回屬性的節點檔案數目上限。</span><span class="sxs-lookup"><span data-stu-id="605d2-153">Specifies the maximum number of node files for which this cmdlet returns properties.</span></span>
<span data-ttu-id="605d2-154">如果您指定的值為零 (0) 或更小，則 Cmdlet 不會使用上限。</span><span class="sxs-lookup"><span data-stu-id="605d2-154">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="605d2-155">預設值為1000。</span><span class="sxs-lookup"><span data-stu-id="605d2-155">The default value is 1000.</span></span>

```yaml
Type: Int32
Parameter Sets: Task_ODataFilter, ParentTask, ComputeNode_ODataFilter, ParentComputeNode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="605d2-156">-Path</span><span class="sxs-lookup"><span data-stu-id="605d2-156">-Path</span></span>
<span data-ttu-id="605d2-157">指定此 Cmdlet 為其檢索屬性之節點檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="605d2-157">Specifies the path of the node file for which this cmdlet retrieves properties.</span></span>
<span data-ttu-id="605d2-158">您無法指定通配字元。</span><span class="sxs-lookup"><span data-stu-id="605d2-158">You cannot specify wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: ComputeNode_Id, Task_Id
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="605d2-159">-PoolId</span><span class="sxs-lookup"><span data-stu-id="605d2-159">-PoolId</span></span>
<span data-ttu-id="605d2-160">指定包含要取得節點檔案屬性之計算節點的池 ID。</span><span class="sxs-lookup"><span data-stu-id="605d2-160">Specifies the ID of the pool that contains the compute node from which to get properties of node files.</span></span>

```yaml
Type: String
Parameter Sets: ComputeNode_Id, ComputeNode_ODataFilter
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="605d2-161">-Recursive</span><span class="sxs-lookup"><span data-stu-id="605d2-161">-Recursive</span></span>
<span data-ttu-id="605d2-162">表示這個 Cmdlet 會傳回一份遞迴的檔案清單。</span><span class="sxs-lookup"><span data-stu-id="605d2-162">Indicates that this cmdlet returns a recursive list of files.</span></span>
<span data-ttu-id="605d2-163">否則，它只會傳回根資料夾中的檔案。</span><span class="sxs-lookup"><span data-stu-id="605d2-163">Otherwise, it returns only the files in the root folder.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Task_ODataFilter, ParentTask, ComputeNode_ODataFilter, ParentComputeNode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="605d2-164">-任務</span><span class="sxs-lookup"><span data-stu-id="605d2-164">-Task</span></span>
<span data-ttu-id="605d2-165">指定要與節點檔案相關聯的工作（ **PSCloudTask** 物件）。</span><span class="sxs-lookup"><span data-stu-id="605d2-165">Specifies the task, as a **PSCloudTask** object, with which the node files are associated.</span></span>
<span data-ttu-id="605d2-166">若要取得 task 物件，請使用 Get-AzureBatchTask Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="605d2-166">To obtain a task object, use the Get-AzureBatchTask cmdlet.</span></span>

```yaml
Type: PSCloudTask
Parameter Sets: ParentTask
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="605d2-167">-TaskId</span><span class="sxs-lookup"><span data-stu-id="605d2-167">-TaskId</span></span>
<span data-ttu-id="605d2-168">指定此 Cmdlet 取得節點檔案屬性的任務識別碼。</span><span class="sxs-lookup"><span data-stu-id="605d2-168">Specifies the ID of the task for which this cmdlet gets properties of node files.</span></span>

```yaml
Type: String
Parameter Sets: Task_Id, Task_ODataFilter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="605d2-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="605d2-169">CommonParameters</span></span>
<span data-ttu-id="605d2-170">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="605d2-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="605d2-171">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="605d2-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="605d2-172">輸入</span><span class="sxs-lookup"><span data-stu-id="605d2-172">INPUTS</span></span>

### <span data-ttu-id="605d2-173">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="605d2-173">BatchAccountContext</span></span>
<span data-ttu-id="605d2-174">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="605d2-174">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="605d2-175">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="605d2-175">PSComputeNode</span></span>
<span data-ttu-id="605d2-176">形參 "ComputeNode" 接受管線中 "PSComputeNode" 類型的值</span><span class="sxs-lookup"><span data-stu-id="605d2-176">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

### <span data-ttu-id="605d2-177">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="605d2-177">PSCloudTask</span></span>
<span data-ttu-id="605d2-178">形參 "Task" 接受管線中 "PSCloudTask" 類型的值</span><span class="sxs-lookup"><span data-stu-id="605d2-178">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="605d2-179">輸出</span><span class="sxs-lookup"><span data-stu-id="605d2-179">OUTPUTS</span></span>

### <span data-ttu-id="605d2-180">PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="605d2-180">PSNodeFile</span></span>

## <span data-ttu-id="605d2-181">筆記</span><span class="sxs-lookup"><span data-stu-id="605d2-181">NOTES</span></span>

## <span data-ttu-id="605d2-182">相關連結</span><span class="sxs-lookup"><span data-stu-id="605d2-182">RELATED LINKS</span></span>

[<span data-ttu-id="605d2-183">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="605d2-183">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="605d2-184">AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="605d2-184">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="605d2-185">AzureBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="605d2-185">Get-AzureBatchNodeFileContent</span></span>](./Get-AzureBatchNodeFileContent.md)

[<span data-ttu-id="605d2-186">AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="605d2-186">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="605d2-187">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="605d2-187">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


