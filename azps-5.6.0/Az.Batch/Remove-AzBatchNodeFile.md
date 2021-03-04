---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DBA02017-8372-4A91-A4F1-985777DEDAB9
online version: https://docs.microsoft.com/powershell/module/az.batch/remove-azbatchnodefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchNodeFile.md
ms.openlocfilehash: a56b8d0613946b33629fda46cc710cdbeef0814e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916787"
---
# <span data-ttu-id="99cb8-101">Remove-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="99cb8-101">Remove-AzBatchNodeFile</span></span>

## <span data-ttu-id="99cb8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="99cb8-102">SYNOPSIS</span></span>
<span data-ttu-id="99cb8-103">刪除任務或計算節點的節點檔案。</span><span class="sxs-lookup"><span data-stu-id="99cb8-103">Deletes a node file for a task or compute node.</span></span>

## <span data-ttu-id="99cb8-104">語法</span><span class="sxs-lookup"><span data-stu-id="99cb8-104">SYNTAX</span></span>

### <span data-ttu-id="99cb8-105">任務</span><span class="sxs-lookup"><span data-stu-id="99cb8-105">Task</span></span>
```
Remove-AzBatchNodeFile -JobId <String> -TaskId <String> -Path <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="99cb8-106">ComputeNode</span><span class="sxs-lookup"><span data-stu-id="99cb8-106">ComputeNode</span></span>
```
Remove-AzBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> -Path <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="99cb8-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="99cb8-107">InputObject</span></span>
```
Remove-AzBatchNodeFile [[-InputObject] <PSNodeFile>] [-Force] [-Recursive] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99cb8-108">描述</span><span class="sxs-lookup"><span data-stu-id="99cb8-108">DESCRIPTION</span></span>
<span data-ttu-id="99cb8-109">**Remove-AzBatchNodeFile** Cmdlet 會刪除工作或計算節點的 Azure 批次處理節點檔案。</span><span class="sxs-lookup"><span data-stu-id="99cb8-109">The **Remove-AzBatchNodeFile** cmdlet deletes an Azure Batch node file for a task or compute node.</span></span>

## <span data-ttu-id="99cb8-110">例子</span><span class="sxs-lookup"><span data-stu-id="99cb8-110">EXAMPLES</span></span>

### <span data-ttu-id="99cb8-111">範例 1：刪除與工作相關聯的檔案</span><span class="sxs-lookup"><span data-stu-id="99cb8-111">Example 1: Delete a file associated with a task</span></span>
```
PS C:\>Remove-AzBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "wd\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="99cb8-112">此命令會刪除名為 wd\testFile.txt。</span><span class="sxs-lookup"><span data-stu-id="99cb8-112">This command deletes the node file that is named wd\testFile.txt.</span></span>
<span data-ttu-id="99cb8-113">該檔案與工作 Job-000001 下具有識別碼工作 26 的工作相關聯。</span><span class="sxs-lookup"><span data-stu-id="99cb8-113">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>

### <span data-ttu-id="99cb8-114">範例 2：從計算節點刪除檔案</span><span class="sxs-lookup"><span data-stu-id="99cb8-114">Example 2: Delete a file from a compute node</span></span>
```
PS C:\>Remove-AzBatchNodeFile -PoolId "Pool07" -ComputeNodeId "tvm-2316545714_1-20150725t213220z" -Path "startup\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="99cb8-115">此命令會從具有 ID Pool07 的startup\testFile.txt計算節點中刪除名為 startup\testFile.txt 的節點檔案。</span><span class="sxs-lookup"><span data-stu-id="99cb8-115">This command deletes the node file that is named startup\testFile.txt from the specified compute node in the pool that has the ID Pool07.</span></span>

### <span data-ttu-id="99cb8-116">範例 3：使用管線移除檔案</span><span class="sxs-lookup"><span data-stu-id="99cb8-116">Example 3: Remove a file by using the pipeline</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "wd\testFile2.txt" -BatchContext $Context | Remove-AzBatchNodeFile -Force -BatchContext $Context
```

<span data-ttu-id="99cb8-117">此命令會使用 **Get-AzBatchNodeFile 取得節點檔案**。</span><span class="sxs-lookup"><span data-stu-id="99cb8-117">This command gets the node file by using **Get-AzBatchNodeFile**.</span></span>
<span data-ttu-id="99cb8-118">該檔案與工作 Job-000001 下具有識別碼工作 26 的工作相關聯。</span><span class="sxs-lookup"><span data-stu-id="99cb8-118">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>
<span data-ttu-id="99cb8-119">該命令會使用管線，將檔案傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="99cb8-119">The command passes that file to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="99cb8-120">目前的 Cmdlet 會移除節點檔案。</span><span class="sxs-lookup"><span data-stu-id="99cb8-120">The current cmdlet removes the node file.</span></span>
<span data-ttu-id="99cb8-121">命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="99cb8-121">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="99cb8-122">因此，命令不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="99cb8-122">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="99cb8-123">參數</span><span class="sxs-lookup"><span data-stu-id="99cb8-123">PARAMETERS</span></span>

### <span data-ttu-id="99cb8-124">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="99cb8-124">-BatchContext</span></span>
<span data-ttu-id="99cb8-125">指定此 Cmdlet 用來與批次處理服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="99cb8-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="99cb8-126">如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="99cb8-126">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="99cb8-127">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="99cb8-127">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="99cb8-128">使用共用金鑰驗證時，預設會使用主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="99cb8-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="99cb8-129">若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。</span><span class="sxs-lookup"><span data-stu-id="99cb8-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="99cb8-130">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="99cb8-130">-ComputeNodeId</span></span>
<span data-ttu-id="99cb8-131">指定包含此 Cmdlet 刪除之 Batch-節點檔案的計算節點識別碼。</span><span class="sxs-lookup"><span data-stu-id="99cb8-131">Specifies the ID of the compute node that contains the Batch node file that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="99cb8-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99cb8-132">-DefaultProfile</span></span>
<span data-ttu-id="99cb8-133">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="99cb8-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99cb8-134">-強制</span><span class="sxs-lookup"><span data-stu-id="99cb8-134">-Force</span></span>
<span data-ttu-id="99cb8-135">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="99cb8-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="99cb8-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99cb8-136">-InputObject</span></span>
<span data-ttu-id="99cb8-137">指定 **PSNodeFile** 物件，代表此 Cmdlet 刪除的節點檔案。</span><span class="sxs-lookup"><span data-stu-id="99cb8-137">Specifies **PSNodeFile** object that represent the node file that this cmdlet deletes.</span></span>
<span data-ttu-id="99cb8-138">若要取得 **PSNodeFile，** 請使用 Get-AzBatchNodeFile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="99cb8-138">To obtain a **PSNodeFile**, use the Get-AzBatchNodeFile cmdlet.</span></span>

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

### <span data-ttu-id="99cb8-139">-JobId</span><span class="sxs-lookup"><span data-stu-id="99cb8-139">-JobId</span></span>
<span data-ttu-id="99cb8-140">指定包含該工作的工作的識別碼。</span><span class="sxs-lookup"><span data-stu-id="99cb8-140">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="99cb8-141">-路徑</span><span class="sxs-lookup"><span data-stu-id="99cb8-141">-Path</span></span>
<span data-ttu-id="99cb8-142">要刪除的節點檔案的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="99cb8-142">The file path of the node file to delete.</span></span>

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

### <span data-ttu-id="99cb8-143">-PoolId</span><span class="sxs-lookup"><span data-stu-id="99cb8-143">-PoolId</span></span>
<span data-ttu-id="99cb8-144">指定包含此 Cmdlet 移除檔案之計算節點之資料庫的識別碼。</span><span class="sxs-lookup"><span data-stu-id="99cb8-144">Specifies the ID of the pool that contains the compute nodes for which this cmdlet removes a file.</span></span>

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

### <span data-ttu-id="99cb8-145">-遞迴</span><span class="sxs-lookup"><span data-stu-id="99cb8-145">-Recursive</span></span>
<span data-ttu-id="99cb8-146">表示此 Cmdlet 會刪除資料夾，以及指定路徑下的所有子資料夾和檔案。</span><span class="sxs-lookup"><span data-stu-id="99cb8-146">Indicates that this cmdlet deletes the folder and all subfolders and files under the specified path.</span></span>
<span data-ttu-id="99cb8-147">只有在路徑是資料夾時，此 Cmdlet 才具有相關性。</span><span class="sxs-lookup"><span data-stu-id="99cb8-147">This cmdlet is relevant only if the path is a folder.</span></span>

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

### <span data-ttu-id="99cb8-148">-TaskId</span><span class="sxs-lookup"><span data-stu-id="99cb8-148">-TaskId</span></span>
<span data-ttu-id="99cb8-149">指定任務的識別碼。</span><span class="sxs-lookup"><span data-stu-id="99cb8-149">Specifies the ID of the task.</span></span>

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

### <span data-ttu-id="99cb8-150">-確認</span><span class="sxs-lookup"><span data-stu-id="99cb8-150">-Confirm</span></span>
<span data-ttu-id="99cb8-151">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="99cb8-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99cb8-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99cb8-152">-WhatIf</span></span>
<span data-ttu-id="99cb8-153">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="99cb8-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99cb8-154">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="99cb8-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99cb8-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99cb8-155">CommonParameters</span></span>
<span data-ttu-id="99cb8-156">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="99cb8-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99cb8-157">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="99cb8-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99cb8-158">輸入</span><span class="sxs-lookup"><span data-stu-id="99cb8-158">INPUTS</span></span>

### <span data-ttu-id="99cb8-159">System.String</span><span class="sxs-lookup"><span data-stu-id="99cb8-159">System.String</span></span>

### <span data-ttu-id="99cb8-160">Microsoft.Azure.Commands.Batch。Models.PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="99cb8-160">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>

### <span data-ttu-id="99cb8-161">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="99cb8-161">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="99cb8-162">輸出</span><span class="sxs-lookup"><span data-stu-id="99cb8-162">OUTPUTS</span></span>

### <span data-ttu-id="99cb8-163">System.Void</span><span class="sxs-lookup"><span data-stu-id="99cb8-163">System.Void</span></span>

## <span data-ttu-id="99cb8-164">筆記</span><span class="sxs-lookup"><span data-stu-id="99cb8-164">NOTES</span></span>

## <span data-ttu-id="99cb8-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="99cb8-165">RELATED LINKS</span></span>

[<span data-ttu-id="99cb8-166">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="99cb8-166">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="99cb8-167">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="99cb8-167">Get-AzBatchNodeFile</span></span>](./Get-AzBatchNodeFile.md)

[<span data-ttu-id="99cb8-168">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="99cb8-168">Get-AzBatchNodeFileContent</span></span>](./Get-AzBatchNodeFileContent.md)


