---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 38ED2854-23D0-400E-A5C8-239346B2AF99
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchnodefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFile.md
ms.openlocfilehash: 0169748ffc6fa2004fe8b0ade542d288677776b5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916297"
---
# <span data-ttu-id="9b99c-101">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="9b99c-101">Get-AzBatchNodeFile</span></span>

## <span data-ttu-id="9b99c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9b99c-102">SYNOPSIS</span></span>
<span data-ttu-id="9b99c-103">獲得 Batch-節點檔案的屬性。</span><span class="sxs-lookup"><span data-stu-id="9b99c-103">Gets the properties of Batch node files.</span></span>

## <span data-ttu-id="9b99c-104">語法</span><span class="sxs-lookup"><span data-stu-id="9b99c-104">SYNTAX</span></span>

### <span data-ttu-id="9b99c-105">ComputeNode_Id (預設) </span><span class="sxs-lookup"><span data-stu-id="9b99c-105">ComputeNode_Id (Default)</span></span>
```
Get-AzBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> [[-Path] <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b99c-106">Task_Id</span><span class="sxs-lookup"><span data-stu-id="9b99c-106">Task_Id</span></span>
```
Get-AzBatchNodeFile -JobId <String> -TaskId <String> [[-Path] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b99c-107">Task_ODataFilter</span><span class="sxs-lookup"><span data-stu-id="9b99c-107">Task_ODataFilter</span></span>
```
Get-AzBatchNodeFile -JobId <String> -TaskId <String> [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b99c-108">ParentTask</span><span class="sxs-lookup"><span data-stu-id="9b99c-108">ParentTask</span></span>
```
Get-AzBatchNodeFile [[-Task] <PSCloudTask>] [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b99c-109">ComputeNode_ODataFilter</span><span class="sxs-lookup"><span data-stu-id="9b99c-109">ComputeNode_ODataFilter</span></span>
```
Get-AzBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Recursive] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9b99c-110">ParentComputeNode</span><span class="sxs-lookup"><span data-stu-id="9b99c-110">ParentComputeNode</span></span>
```
Get-AzBatchNodeFile [[-ComputeNode] <PSComputeNode>] [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b99c-111">描述</span><span class="sxs-lookup"><span data-stu-id="9b99c-111">DESCRIPTION</span></span>
<span data-ttu-id="9b99c-112">**Get-AzBatchNodeFile** Cmdlet 會取得任務或計算節點之 Azure Batch-節點檔案的屬性。</span><span class="sxs-lookup"><span data-stu-id="9b99c-112">The **Get-AzBatchNodeFile** cmdlet gets the properties of the Azure Batch node files of a task or compute node.</span></span>
<span data-ttu-id="9b99c-113">若要縮小結果範圍，您可以指定 OData (開啟) 篩選器。</span><span class="sxs-lookup"><span data-stu-id="9b99c-113">To narrow your results, you can specify an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="9b99c-114">如果您指定任務，但未指定篩選，此 Cmdlet 會針對該工作的所有節點檔案，會返回屬性。</span><span class="sxs-lookup"><span data-stu-id="9b99c-114">If you specify a task, but not a filter, this cmdlet returns properties for all node files for that task.</span></span>
<span data-ttu-id="9b99c-115">如果您指定計算節點，但未指定篩選，此 Cmdlet 會針對該計算節點的所有節點檔案，會返回屬性。</span><span class="sxs-lookup"><span data-stu-id="9b99c-115">If you specify a compute node, but not a filter, this cmdlet returns properties for all node files for that compute node.</span></span>

## <span data-ttu-id="9b99c-116">例子</span><span class="sxs-lookup"><span data-stu-id="9b99c-116">EXAMPLES</span></span>

### <span data-ttu-id="9b99c-117">範例 1：取得與工作相關聯的節點檔案屬性</span><span class="sxs-lookup"><span data-stu-id="9b99c-117">Example 1: Get the properties of a node file associated with a task</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "Stdout.txt" -BatchContext $Context
IsDirectory Name          Properties                                      Url

----------- ----          ----------                                      ---

False       StdOut.txt    Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="9b99c-118">此命令會獲得與具有識別碼 Job-StdOut.txt 000001 的工作中具有 ID Task26 之工作關聯的 StdOut.txt 節點檔案的屬性。</span><span class="sxs-lookup"><span data-stu-id="9b99c-118">This command gets the properties of the StdOut.txt node file associated with the task that has the ID Task26 in the job that has the ID Job-000001.</span></span>
<span data-ttu-id="9b99c-119">使用 Get-AzBatchAccountKey Cmdlet 將上下文指派給$CoNtext變數。</span><span class="sxs-lookup"><span data-stu-id="9b99c-119">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="9b99c-120">範例 2：使用篩選取得與工作相關聯的節點檔案屬性</span><span class="sxs-lookup"><span data-stu-id="9b99c-120">Example 2: Get the properties of node files associated with a task by using a filter</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job-00002" -TaskId "Task26" -Filter "startswith(name,'St')" -BatchContext $Context
IsDirectory Name        Properties                                      Url

----------- ----        ----------                                      ---

False       StdErr.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
False       StdOut.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="9b99c-121">此命令會獲得名稱以 st 為開始，且與識別碼為 Job-00002 的工作中具有 ID Task26 的工作相關聯的節點檔案屬性。</span><span class="sxs-lookup"><span data-stu-id="9b99c-121">This command gets the properties of the node files whose names start with st and are associated with task that has the ID Task26 under job that has the ID Job-00002.</span></span>

### <span data-ttu-id="9b99c-122">範例 3：以遞迴法取得與工作相關聯的節點檔案屬性</span><span class="sxs-lookup"><span data-stu-id="9b99c-122">Example 3: Recursively get the properties of node files associated with a task</span></span>
```
PS C:\>Get-AzBatchTask "Job-00003" "Task31" -BatchContext $Context | Get-AzBatchNodeFile -Recursive -BatchContext $Context
IsDirectory Name             Properties                                      Url

----------- ----             ----------                                      ---

False       ProcessEnv.cmd   Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
False       StdErr.txt       Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
False       StdOut.txt       Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
True        wd                                                               https://cmdletexample.westus.Batch.contoso...
False       wd\newFile.txt   Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="9b99c-123">此命令會獲得與 job Job-00003 中具有 ID Task31 之工作關聯的所有檔案的屬性。</span><span class="sxs-lookup"><span data-stu-id="9b99c-123">This command gets the properties of all files associated with the task that has the ID Task31 in job Job-00003.</span></span>
<span data-ttu-id="9b99c-124">此命令會指定 *遞迴參數* 。</span><span class="sxs-lookup"><span data-stu-id="9b99c-124">This command specifies the *Recursive* parameter.</span></span>
<span data-ttu-id="9b99c-125">因此，Cmdlet 會執行遞迴檔案搜尋，並wd\newFile.txt節點檔案。</span><span class="sxs-lookup"><span data-stu-id="9b99c-125">Therefore, the cmdlet performs a recursive file search is performed, and returns the wd\newFile.txt node file.</span></span>

### <span data-ttu-id="9b99c-126">範例 4：從計算節點取得單一檔案</span><span class="sxs-lookup"><span data-stu-id="9b99c-126">Example 4: Get a single file from a compute node</span></span>
```
PS C:\>Get-AzBatchNodeFile -PoolId "Pool22" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context
IsDirectory Name                    Properties                                      Url
----------- ----                    ----------                                      ---
False       startup\stdout.txt      Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="9b99c-127">此命令會從具有 ID pool22 之Startup\StdOut.txt ID ComputeNode01 的計算節點中，從名稱為 Startup\StdOut.txt 的檔案。</span><span class="sxs-lookup"><span data-stu-id="9b99c-127">This command gets the file that is named Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>

### <span data-ttu-id="9b99c-128">範例 5：從計算節點取得資料夾下的所有檔案</span><span class="sxs-lookup"><span data-stu-id="9b99c-128">Example 5: Get all files under a folder from a compute node</span></span>
```
PS C:\>Get-AzBatchNodeFile -PoolId "Pool22" -ComputeNodeId "ComputeNode01" -Filter "startswith(name,'startup')" -Recursive -BatchContext $Context
IsDirectory Name                      Properties                                      Url
----------- ----                      ----------                                      ---
True        startup                                                                   https://cmdletexample.westus.Batch.contoso...
False       startup\ProcessEnv.cmd    Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
False       startup\stderr.txt        Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
False       startup\stdout.txt        Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
True        startup\wd                                                                https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="9b99c-129">此命令會從具有識別碼 Pool22 之計算節點的開機檔案夾下，從具有 ID Pool22 之識別碼 ComputeNode01 的計算節點中，獲得所有檔案。</span><span class="sxs-lookup"><span data-stu-id="9b99c-129">This command gets all the files under the startup folder from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>
<span data-ttu-id="9b99c-130">此 Cmdlet 會指定 *遞迴* 參數。</span><span class="sxs-lookup"><span data-stu-id="9b99c-130">This cmdlet specifies the *Recursive* parameter.</span></span>

### <span data-ttu-id="9b99c-131">範例 6：從計算節點的根資料夾取得檔案</span><span class="sxs-lookup"><span data-stu-id="9b99c-131">Example 6: Get files from the root folder of a compute node</span></span>
```
PS C:\>Get-AzBatchComputeNode "Pool22" -Id "ComputeNode01" -BatchContext $Context | Get-AzBatchNodeFile -BatchContext $Context
IsDirectory Name           Properties       Url
----------- ----           ----------       ---
True        shared                          https://cmdletexample.westus.Batch.contoso...
True        startup                         https://cmdletexample.westus.Batch.contoso...
True        workitems                       https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="9b99c-132">此命令會獲得具有識別碼 Pool22 之計算節點根資料夾的所有檔案，該計算節點的集中具有 ID ComputeNode01。</span><span class="sxs-lookup"><span data-stu-id="9b99c-132">This command gets all the files at the root folder of the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>

## <span data-ttu-id="9b99c-133">參數</span><span class="sxs-lookup"><span data-stu-id="9b99c-133">PARAMETERS</span></span>

### <span data-ttu-id="9b99c-134">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="9b99c-134">-BatchContext</span></span>
<span data-ttu-id="9b99c-135">指定此 Cmdlet 用來與批次處理服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="9b99c-135">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="9b99c-136">如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="9b99c-136">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="9b99c-137">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="9b99c-137">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="9b99c-138">使用共用金鑰驗證時，預設會使用主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="9b99c-138">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="9b99c-139">若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。</span><span class="sxs-lookup"><span data-stu-id="9b99c-139">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="9b99c-140">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="9b99c-140">-ComputeNode</span></span>
<span data-ttu-id="9b99c-141">指定包含批次處理節點檔案的計算節點做為 **PSComputeNode** 物件。</span><span class="sxs-lookup"><span data-stu-id="9b99c-141">Specifies the compute node, as a **PSComputeNode** object, that contains the Batch node files.</span></span>
<span data-ttu-id="9b99c-142">若要取得計算節點物件，請使用 Get-AzBatchComputeNode Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9b99c-142">To obtain a compute node object, use the Get-AzBatchComputeNode cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: ParentComputeNode
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b99c-143">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="9b99c-143">-ComputeNodeId</span></span>
<span data-ttu-id="9b99c-144">指定包含 Batch-節點檔案的計算節點識別碼。</span><span class="sxs-lookup"><span data-stu-id="9b99c-144">Specifies the ID of the compute node that contains the Batch node files.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id, ComputeNode_ODataFilter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b99c-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b99c-145">-DefaultProfile</span></span>
<span data-ttu-id="9b99c-146">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9b99c-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b99c-147">-篩選</span><span class="sxs-lookup"><span data-stu-id="9b99c-147">-Filter</span></span>
<span data-ttu-id="9b99c-148">指定 OData 篩選子句。</span><span class="sxs-lookup"><span data-stu-id="9b99c-148">Specifies an OData filter clause.</span></span>
<span data-ttu-id="9b99c-149">此 Cmdlet 會針對符合此參數指定之篩選的節點檔案，返回屬性。</span><span class="sxs-lookup"><span data-stu-id="9b99c-149">This cmdlet returns properties for node files that match the filter that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_ODataFilter, ParentTask, ComputeNode_ODataFilter, ParentComputeNode
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b99c-150">-JobId</span><span class="sxs-lookup"><span data-stu-id="9b99c-150">-JobId</span></span>
<span data-ttu-id="9b99c-151">指定包含目標工作的工作的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9b99c-151">Specifies the ID of the job that contains the target task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id, Task_ODataFilter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b99c-152">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="9b99c-152">-MaxCount</span></span>
<span data-ttu-id="9b99c-153">指定此 Cmdlet 會針對哪些節點檔案最多會返回屬性。</span><span class="sxs-lookup"><span data-stu-id="9b99c-153">Specifies the maximum number of node files for which this cmdlet returns properties.</span></span>
<span data-ttu-id="9b99c-154">如果您將值指定為 0 (0) ，Cmdlet 不會使用上限。</span><span class="sxs-lookup"><span data-stu-id="9b99c-154">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="9b99c-155">預設值為 1000。</span><span class="sxs-lookup"><span data-stu-id="9b99c-155">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Task_ODataFilter, ParentTask, ComputeNode_ODataFilter, ParentComputeNode
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b99c-156">-路徑</span><span class="sxs-lookup"><span data-stu-id="9b99c-156">-Path</span></span>
<span data-ttu-id="9b99c-157">指定此 Cmdlet 會為它所取取屬性的節點檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="9b99c-157">Specifies the path of the node file for which this cmdlet retrieves properties.</span></span>
<span data-ttu-id="9b99c-158">您無法指定萬用字元。</span><span class="sxs-lookup"><span data-stu-id="9b99c-158">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id, Task_Id
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b99c-159">-PoolId</span><span class="sxs-lookup"><span data-stu-id="9b99c-159">-PoolId</span></span>
<span data-ttu-id="9b99c-160">指定包含計算節點之資料庫的識別碼，以取得節點檔案的屬性。</span><span class="sxs-lookup"><span data-stu-id="9b99c-160">Specifies the ID of the pool that contains the compute node from which to get properties of node files.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id, ComputeNode_ODataFilter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b99c-161">-遞迴</span><span class="sxs-lookup"><span data-stu-id="9b99c-161">-Recursive</span></span>
<span data-ttu-id="9b99c-162">表示此 Cmdlet 會返回檔案的遞迴清單。</span><span class="sxs-lookup"><span data-stu-id="9b99c-162">Indicates that this cmdlet returns a recursive list of files.</span></span>
<span data-ttu-id="9b99c-163">否則，它只會回到根資料夾中的檔案。</span><span class="sxs-lookup"><span data-stu-id="9b99c-163">Otherwise, it returns only the files in the root folder.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Task_ODataFilter, ParentTask, ComputeNode_ODataFilter, ParentComputeNode
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b99c-164">-工作</span><span class="sxs-lookup"><span data-stu-id="9b99c-164">-Task</span></span>
<span data-ttu-id="9b99c-165">指定工作 ，做為與節點檔案相關聯的 **PSCloudTask** 物件。</span><span class="sxs-lookup"><span data-stu-id="9b99c-165">Specifies the task, as a **PSCloudTask** object, with which the node files are associated.</span></span>
<span data-ttu-id="9b99c-166">若要取得工作物件，請使用 Get-AzBatchTask Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9b99c-166">To obtain a task object, use the Get-AzBatchTask cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: ParentTask
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b99c-167">-TaskId</span><span class="sxs-lookup"><span data-stu-id="9b99c-167">-TaskId</span></span>
<span data-ttu-id="9b99c-168">指定此 Cmdlet 會獲得節點檔案屬性的工作識別碼。</span><span class="sxs-lookup"><span data-stu-id="9b99c-168">Specifies the ID of the task for which this cmdlet gets properties of node files.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id, Task_ODataFilter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b99c-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b99c-169">CommonParameters</span></span>
<span data-ttu-id="9b99c-170">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9b99c-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b99c-171">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9b99c-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b99c-172">輸入</span><span class="sxs-lookup"><span data-stu-id="9b99c-172">INPUTS</span></span>

### <span data-ttu-id="9b99c-173">System.String</span><span class="sxs-lookup"><span data-stu-id="9b99c-173">System.String</span></span>

### <span data-ttu-id="9b99c-174">Microsoft.Azure.Commands.Batch。Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="9b99c-174">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="9b99c-175">Microsoft.Azure.Commands.Batch。Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="9b99c-175">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="9b99c-176">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="9b99c-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="9b99c-177">輸出</span><span class="sxs-lookup"><span data-stu-id="9b99c-177">OUTPUTS</span></span>

### <span data-ttu-id="9b99c-178">Microsoft.Azure.Commands.Batch。Models.PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="9b99c-178">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>

## <span data-ttu-id="9b99c-179">筆記</span><span class="sxs-lookup"><span data-stu-id="9b99c-179">NOTES</span></span>

## <span data-ttu-id="9b99c-180">相關連結</span><span class="sxs-lookup"><span data-stu-id="9b99c-180">RELATED LINKS</span></span>

[<span data-ttu-id="9b99c-181">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="9b99c-181">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="9b99c-182">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="9b99c-182">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="9b99c-183">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="9b99c-183">Get-AzBatchNodeFileContent</span></span>](./Get-AzBatchNodeFileContent.md)

[<span data-ttu-id="9b99c-184">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="9b99c-184">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="9b99c-185">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9b99c-185">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
