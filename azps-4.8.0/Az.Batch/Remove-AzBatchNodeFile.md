---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DBA02017-8372-4A91-A4F1-985777DEDAB9
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchnodefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchNodeFile.md
ms.openlocfilehash: 7e9aeebebfc5720ab006d43071eadeabe6bcf655
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970630"
---
# <span data-ttu-id="e096d-101">Remove-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="e096d-101">Remove-AzBatchNodeFile</span></span>

## <span data-ttu-id="e096d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e096d-102">SYNOPSIS</span></span>
<span data-ttu-id="e096d-103">刪除任務或計算節點的節點檔案。</span><span class="sxs-lookup"><span data-stu-id="e096d-103">Deletes a node file for a task or compute node.</span></span>

## <span data-ttu-id="e096d-104">句法</span><span class="sxs-lookup"><span data-stu-id="e096d-104">SYNTAX</span></span>

### <span data-ttu-id="e096d-105">工作</span><span class="sxs-lookup"><span data-stu-id="e096d-105">Task</span></span>
```
Remove-AzBatchNodeFile -JobId <String> -TaskId <String> -Path <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e096d-106">ComputeNode</span><span class="sxs-lookup"><span data-stu-id="e096d-106">ComputeNode</span></span>
```
Remove-AzBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> -Path <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e096d-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="e096d-107">InputObject</span></span>
```
Remove-AzBatchNodeFile [[-InputObject] <PSNodeFile>] [-Force] [-Recursive] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e096d-108">說明</span><span class="sxs-lookup"><span data-stu-id="e096d-108">DESCRIPTION</span></span>
<span data-ttu-id="e096d-109">**AzBatchNodeFile** Cmdlet 會刪除任務或計算節點的 Azure Batch-節點檔案。</span><span class="sxs-lookup"><span data-stu-id="e096d-109">The **Remove-AzBatchNodeFile** cmdlet deletes an Azure Batch node file for a task or compute node.</span></span>

## <span data-ttu-id="e096d-110">示例</span><span class="sxs-lookup"><span data-stu-id="e096d-110">EXAMPLES</span></span>

### <span data-ttu-id="e096d-111">範例1：刪除與任務相關聯的檔案</span><span class="sxs-lookup"><span data-stu-id="e096d-111">Example 1: Delete a file associated with a task</span></span>
```
PS C:\>Remove-AzBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "wd\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="e096d-112">這個命令會刪除名為 wd\testFile.txt 的節點檔案。</span><span class="sxs-lookup"><span data-stu-id="e096d-112">This command deletes the node file that is named wd\testFile.txt.</span></span>
<span data-ttu-id="e096d-113">該檔案與作業作業（000001）下具有識別碼 Task26 的任務相關聯。</span><span class="sxs-lookup"><span data-stu-id="e096d-113">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>

### <span data-ttu-id="e096d-114">範例2：從計算節點刪除檔案</span><span class="sxs-lookup"><span data-stu-id="e096d-114">Example 2: Delete a file from a compute node</span></span>
```
PS C:\>Remove-AzBatchNodeFile -PoolId "Pool07" -ComputeNodeId "tvm-2316545714_1-20150725t213220z" -Path "startup\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="e096d-115">這個命令會從擁有識別碼 Pool07 的池中的指定計算節點刪除名為 startup\testFile.txt 的節點檔案。</span><span class="sxs-lookup"><span data-stu-id="e096d-115">This command deletes the node file that is named startup\testFile.txt from the specified compute node in the pool that has the ID Pool07.</span></span>

### <span data-ttu-id="e096d-116">範例3：使用管線移除檔案</span><span class="sxs-lookup"><span data-stu-id="e096d-116">Example 3: Remove a file by using the pipeline</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "wd\testFile2.txt" -BatchContext $Context | Remove-AzBatchNodeFile -Force -BatchContext $Context
```

<span data-ttu-id="e096d-117">這個命令會使用 **AzBatchNodeFile** 來取得節點檔案。</span><span class="sxs-lookup"><span data-stu-id="e096d-117">This command gets the node file by using **Get-AzBatchNodeFile**.</span></span>
<span data-ttu-id="e096d-118">該檔案與作業作業（000001）下具有識別碼 Task26 的任務相關聯。</span><span class="sxs-lookup"><span data-stu-id="e096d-118">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>
<span data-ttu-id="e096d-119">命令會使用管線將該檔案傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e096d-119">The command passes that file to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="e096d-120">目前的 Cmdlet 會移除節點檔案。</span><span class="sxs-lookup"><span data-stu-id="e096d-120">The current cmdlet removes the node file.</span></span>
<span data-ttu-id="e096d-121">命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="e096d-121">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="e096d-122">因此，命令不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e096d-122">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="e096d-123">參數</span><span class="sxs-lookup"><span data-stu-id="e096d-123">PARAMETERS</span></span>

### <span data-ttu-id="e096d-124">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="e096d-124">-BatchContext</span></span>
<span data-ttu-id="e096d-125">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="e096d-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e096d-126">如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="e096d-126">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e096d-127">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="e096d-127">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e096d-128">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="e096d-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e096d-129">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="e096d-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e096d-130">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="e096d-130">-ComputeNodeId</span></span>
<span data-ttu-id="e096d-131">指定包含此 Cmdlet 刪除之批節點檔案之計算節點的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e096d-131">Specifies the ID of the compute node that contains the Batch node file that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e096d-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e096d-132">-DefaultProfile</span></span>
<span data-ttu-id="e096d-133">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e096d-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e096d-134">-Force</span><span class="sxs-lookup"><span data-stu-id="e096d-134">-Force</span></span>
<span data-ttu-id="e096d-135">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="e096d-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e096d-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e096d-136">-InputObject</span></span>
<span data-ttu-id="e096d-137">指定代表此 Cmdlet 刪除之節點檔案的 **PSNodeFile** 物件。</span><span class="sxs-lookup"><span data-stu-id="e096d-137">Specifies **PSNodeFile** object that represent the node file that this cmdlet deletes.</span></span>
<span data-ttu-id="e096d-138">若要取得 **PSNodeFile** ，請使用 Get-AzBatchNodeFile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e096d-138">To obtain a **PSNodeFile** , use the Get-AzBatchNodeFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSNodeFile
Parameter Sets: InputObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e096d-139">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="e096d-139">-JobId</span></span>
<span data-ttu-id="e096d-140">指定包含該任務的作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="e096d-140">Specifies the ID of the job that contains the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e096d-141">-Path</span><span class="sxs-lookup"><span data-stu-id="e096d-141">-Path</span></span>
<span data-ttu-id="e096d-142">要刪除之節點檔案的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="e096d-142">The file path of the node file to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: Task, ComputeNode
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e096d-143">-PoolId</span><span class="sxs-lookup"><span data-stu-id="e096d-143">-PoolId</span></span>
<span data-ttu-id="e096d-144">指定包含此 Cmdlet 移除檔案之計算節點的池 ID。</span><span class="sxs-lookup"><span data-stu-id="e096d-144">Specifies the ID of the pool that contains the compute nodes for which this cmdlet removes a file.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e096d-145">-Recursive</span><span class="sxs-lookup"><span data-stu-id="e096d-145">-Recursive</span></span>
<span data-ttu-id="e096d-146">表示此 Cmdlet 會刪除指定路徑下的資料夾及所有子資料夾及檔案。</span><span class="sxs-lookup"><span data-stu-id="e096d-146">Indicates that this cmdlet deletes the folder and all subfolders and files under the specified path.</span></span>
<span data-ttu-id="e096d-147">只有當路徑是資料夾時，才會涉及這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e096d-147">This cmdlet is relevant only if the path is a folder.</span></span>

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

### <span data-ttu-id="e096d-148">-TaskId</span><span class="sxs-lookup"><span data-stu-id="e096d-148">-TaskId</span></span>
<span data-ttu-id="e096d-149">指定任務的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e096d-149">Specifies the ID of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e096d-150">-確認</span><span class="sxs-lookup"><span data-stu-id="e096d-150">-Confirm</span></span>
<span data-ttu-id="e096d-151">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e096d-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e096d-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e096d-152">-WhatIf</span></span>
<span data-ttu-id="e096d-153">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e096d-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e096d-154">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e096d-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e096d-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e096d-155">CommonParameters</span></span>
<span data-ttu-id="e096d-156">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e096d-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e096d-157">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e096d-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e096d-158">輸入</span><span class="sxs-lookup"><span data-stu-id="e096d-158">INPUTS</span></span>

### <span data-ttu-id="e096d-159">System.object</span><span class="sxs-lookup"><span data-stu-id="e096d-159">System.String</span></span>

### <span data-ttu-id="e096d-160">Microsoft.Azure.Commands.Batch。PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="e096d-160">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>

### <span data-ttu-id="e096d-161">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="e096d-161">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e096d-162">輸出</span><span class="sxs-lookup"><span data-stu-id="e096d-162">OUTPUTS</span></span>

### <span data-ttu-id="e096d-163">System.void</span><span class="sxs-lookup"><span data-stu-id="e096d-163">System.Void</span></span>

## <span data-ttu-id="e096d-164">筆記</span><span class="sxs-lookup"><span data-stu-id="e096d-164">NOTES</span></span>

## <span data-ttu-id="e096d-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="e096d-165">RELATED LINKS</span></span>

[<span data-ttu-id="e096d-166">AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="e096d-166">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="e096d-167">AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="e096d-167">Get-AzBatchNodeFile</span></span>](./Get-AzBatchNodeFile.md)

[<span data-ttu-id="e096d-168">AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="e096d-168">Get-AzBatchNodeFileContent</span></span>](./Get-AzBatchNodeFileContent.md)


