---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: DBA02017-8372-4A91-A4F1-985777DEDAB9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchNodeFile.md
ms.openlocfilehash: 5b8797cf2f6068098d1ca407f0f97283dd171af5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450025"
---
# <span data-ttu-id="e3bad-101">Remove-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="e3bad-101">Remove-AzureBatchNodeFile</span></span>

## <span data-ttu-id="e3bad-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e3bad-102">SYNOPSIS</span></span>
<span data-ttu-id="e3bad-103">刪除任務或計算節點的節點檔案。</span><span class="sxs-lookup"><span data-stu-id="e3bad-103">Deletes a node file for a task or compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3bad-104">句法</span><span class="sxs-lookup"><span data-stu-id="e3bad-104">SYNTAX</span></span>

### <span data-ttu-id="e3bad-105">工作</span><span class="sxs-lookup"><span data-stu-id="e3bad-105">Task</span></span>
```
Remove-AzureBatchNodeFile -JobId <String> -TaskId <String> -Name <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e3bad-106">ComputeNode</span><span class="sxs-lookup"><span data-stu-id="e3bad-106">ComputeNode</span></span>
```
Remove-AzureBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> -Name <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e3bad-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="e3bad-107">InputObject</span></span>
```
Remove-AzureBatchNodeFile [[-InputObject] <PSNodeFile>] [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e3bad-108">說明</span><span class="sxs-lookup"><span data-stu-id="e3bad-108">DESCRIPTION</span></span>
<span data-ttu-id="e3bad-109">**AzureBatchNodeFile** Cmdlet 會刪除任務或計算節點的 Azure Batch-節點檔案。</span><span class="sxs-lookup"><span data-stu-id="e3bad-109">The **Remove-AzureBatchNodeFile** cmdlet deletes an Azure Batch node file for a task or compute node.</span></span>

## <span data-ttu-id="e3bad-110">示例</span><span class="sxs-lookup"><span data-stu-id="e3bad-110">EXAMPLES</span></span>

### <span data-ttu-id="e3bad-111">範例1：使用任務刪除檔案 assocated</span><span class="sxs-lookup"><span data-stu-id="e3bad-111">Example 1: Delete a file assocated with a task</span></span>
```
PS C:\>Remove-AzureBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Name "wd\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="e3bad-112">這個命令會刪除名為 wd\testFile.txt 的節點檔案。</span><span class="sxs-lookup"><span data-stu-id="e3bad-112">This command deletes the node file that is named wd\testFile.txt.</span></span>
<span data-ttu-id="e3bad-113">該檔案與作業作業（000001）下具有識別碼 Task26 的任務相關聯。</span><span class="sxs-lookup"><span data-stu-id="e3bad-113">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>

### <span data-ttu-id="e3bad-114">範例2：從計算節點刪除檔案</span><span class="sxs-lookup"><span data-stu-id="e3bad-114">Example 2: Delete a file from a compute node</span></span>
```
PS C:\>Remove-AzureBatchNodeFile -PoolId "Pool07" -ComputeNodeId "tvm-2316545714_1-20150725t213220z" -Name "startup\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="e3bad-115">這個命令會從擁有識別碼 Pool07 的池中的指定計算節點刪除名為 startup\testFile.txt 的節點檔案。</span><span class="sxs-lookup"><span data-stu-id="e3bad-115">This command deletes the node file that is named startup\testFile.txt from the specified compute node in the pool that has the ID Pool07.</span></span>

### <span data-ttu-id="e3bad-116">範例3：使用管線移除檔案</span><span class="sxs-lookup"><span data-stu-id="e3bad-116">Example 3: Remove a file by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Name "wd\testFile2.txt" -BatchContext $Context | Remove-AzureBatchNodeFile -Force -BatchContext $Context
```

<span data-ttu-id="e3bad-117">這個命令會使用 **AzureBatchNodeFile** 來取得節點檔案。</span><span class="sxs-lookup"><span data-stu-id="e3bad-117">This command gets the node file by using **Get-AzureBatchNodeFile**.</span></span>
<span data-ttu-id="e3bad-118">該檔案與作業作業（000001）下具有識別碼 Task26 的任務相關聯。</span><span class="sxs-lookup"><span data-stu-id="e3bad-118">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>
<span data-ttu-id="e3bad-119">命令會使用管線將該檔案傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e3bad-119">The command passes that file to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="e3bad-120">目前的 Cmdlet 會移除節點檔案。</span><span class="sxs-lookup"><span data-stu-id="e3bad-120">The current cmdlet removes the node file.</span></span>
<span data-ttu-id="e3bad-121">命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="e3bad-121">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="e3bad-122">因此，命令不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e3bad-122">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="e3bad-123">參數</span><span class="sxs-lookup"><span data-stu-id="e3bad-123">PARAMETERS</span></span>

### <span data-ttu-id="e3bad-124">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="e3bad-124">-BatchContext</span></span>
<span data-ttu-id="e3bad-125">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="e3bad-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e3bad-126">若要取得包含您訂閱之便捷鍵的 **BatchAccountCoNtext** 物件，請使用 Get-AzureRmBatchAccountKeys Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e3bad-126">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="e3bad-127">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="e3bad-127">-ComputeNodeId</span></span>
<span data-ttu-id="e3bad-128">指定包含此 Cmdlet 刪除之批節點檔案之計算節點的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e3bad-128">Specifies the ID of the compute node that contains the Batch node file that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="e3bad-129">-Force</span><span class="sxs-lookup"><span data-stu-id="e3bad-129">-Force</span></span>
<span data-ttu-id="e3bad-130">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="e3bad-130">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e3bad-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3bad-131">-InputObject</span></span>
<span data-ttu-id="e3bad-132">指定代表此 Cmdlet 刪除之節點檔案的 **PSNodeFile** 物件。</span><span class="sxs-lookup"><span data-stu-id="e3bad-132">Specifies **PSNodeFile** object that represent the node file that this cmdlet deletes.</span></span>
<span data-ttu-id="e3bad-133">若要取得 **PSNodeFile** ，請使用 Get-AzureBatchNodeFile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e3bad-133">To obtain a **PSNodeFile** , use the Get-AzureBatchNodeFile cmdlet.</span></span>

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

### <span data-ttu-id="e3bad-134">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="e3bad-134">-JobId</span></span>
<span data-ttu-id="e3bad-135">指定包含該任務的作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="e3bad-135">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="e3bad-136">-名稱</span><span class="sxs-lookup"><span data-stu-id="e3bad-136">-Name</span></span>
<span data-ttu-id="e3bad-137">指定此 Cmdlet 刪除之節點檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="e3bad-137">Specifies the name of the node file that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: Task, ComputeNode
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3bad-138">-PoolId</span><span class="sxs-lookup"><span data-stu-id="e3bad-138">-PoolId</span></span>
<span data-ttu-id="e3bad-139">指定包含此 Cmdlet 移除檔案之計算節點的池 ID。</span><span class="sxs-lookup"><span data-stu-id="e3bad-139">Specifies the ID of the pool that contains the compute nodes for which this cmdlet removes a file.</span></span>

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

### <span data-ttu-id="e3bad-140">-Recursive</span><span class="sxs-lookup"><span data-stu-id="e3bad-140">-Recursive</span></span>
<span data-ttu-id="e3bad-141">表示此 Cmdlet 會刪除指定路徑下的資料夾及所有子資料夾及檔案。</span><span class="sxs-lookup"><span data-stu-id="e3bad-141">Indicates that this cmdlet deletes the folder and all subfolders and files under the specified path.</span></span>
<span data-ttu-id="e3bad-142">只有當路徑是資料夾時，才會涉及這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e3bad-142">This cmdlet is relevant only if the path is a folder.</span></span>

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

### <span data-ttu-id="e3bad-143">-TaskId</span><span class="sxs-lookup"><span data-stu-id="e3bad-143">-TaskId</span></span>
<span data-ttu-id="e3bad-144">指定任務的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e3bad-144">Specifies the ID of the task.</span></span>

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

### <span data-ttu-id="e3bad-145">-確認</span><span class="sxs-lookup"><span data-stu-id="e3bad-145">-Confirm</span></span>
<span data-ttu-id="e3bad-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e3bad-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3bad-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3bad-147">-WhatIf</span></span>
<span data-ttu-id="e3bad-148">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e3bad-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3bad-149">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e3bad-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3bad-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3bad-150">-DefaultProfile</span></span>
<span data-ttu-id="e3bad-151">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e3bad-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3bad-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3bad-152">CommonParameters</span></span>
<span data-ttu-id="e3bad-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e3bad-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3bad-154">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e3bad-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3bad-155">輸入</span><span class="sxs-lookup"><span data-stu-id="e3bad-155">INPUTS</span></span>

### <span data-ttu-id="e3bad-156">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="e3bad-156">BatchAccountContext</span></span>
<span data-ttu-id="e3bad-157">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="e3bad-157">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="e3bad-158">PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="e3bad-158">PSNodeFile</span></span>
<span data-ttu-id="e3bad-159">形參 "InputObject" 接受管線中 "PSNodeFile" 類型的值</span><span class="sxs-lookup"><span data-stu-id="e3bad-159">Parameter 'InputObject' accepts value of type 'PSNodeFile' from the pipeline</span></span>

## <span data-ttu-id="e3bad-160">輸出</span><span class="sxs-lookup"><span data-stu-id="e3bad-160">OUTPUTS</span></span>

## <span data-ttu-id="e3bad-161">筆記</span><span class="sxs-lookup"><span data-stu-id="e3bad-161">NOTES</span></span>

## <span data-ttu-id="e3bad-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="e3bad-162">RELATED LINKS</span></span>

[<span data-ttu-id="e3bad-163">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="e3bad-163">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="e3bad-164">AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="e3bad-164">Get-AzureBatchNodeFile</span></span>](./Get-AzureBatchNodeFile.md)

[<span data-ttu-id="e3bad-165">AzureBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="e3bad-165">Get-AzureBatchNodeFileContent</span></span>](./Get-AzureBatchNodeFileContent.md)


