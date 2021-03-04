---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B6229D26-D38C-44CD-B9CA-7F39365C8B9D
online version: https://docs.microsoft.com/powershell/module/az.batch/new-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJob.md
ms.openlocfilehash: 97b6d2c332b4bc59df165599fe49d38fe496008c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910766"
---
# <span data-ttu-id="2282b-101">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2282b-101">New-AzBatchJob</span></span>

## <span data-ttu-id="2282b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2282b-102">SYNOPSIS</span></span>
<span data-ttu-id="2282b-103">在批次處理服務中建立工作。</span><span class="sxs-lookup"><span data-stu-id="2282b-103">Creates a job in the Batch service.</span></span>

## <span data-ttu-id="2282b-104">語法</span><span class="sxs-lookup"><span data-stu-id="2282b-104">SYNTAX</span></span>

```
New-AzBatchJob [-Id] <String> [-CommonEnvironmentSettings <IDictionary>] [-DisplayName <String>]
 [-Constraints <PSJobConstraints>] [-JobManagerTask <PSJobManagerTask>]
 [-JobPreparationTask <PSJobPreparationTask>] [-JobReleaseTask <PSJobReleaseTask>] [-Metadata <IDictionary>]
 -PoolInformation <PSPoolInformation> [-Priority <Int32>] [-UsesTaskDependencies]
 [-OnTaskFailure <OnTaskFailure>] [-OnAllTasksComplete <OnAllTasksComplete>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2282b-105">描述</span><span class="sxs-lookup"><span data-stu-id="2282b-105">DESCRIPTION</span></span>
<span data-ttu-id="2282b-106">**New-AzBatchJob** Cmdlet 會以 *BatchAccountCoNtext* 參數指定的帳號，在 Azure Batch 服務中建立工作。</span><span class="sxs-lookup"><span data-stu-id="2282b-106">The **New-AzBatchJob** cmdlet creates a job in the Azure Batch service in the account specified by the *BatchAccountContext* parameter.</span></span>

## <span data-ttu-id="2282b-107">例子</span><span class="sxs-lookup"><span data-stu-id="2282b-107">EXAMPLES</span></span>

### <span data-ttu-id="2282b-108">範例 1：建立工作</span><span class="sxs-lookup"><span data-stu-id="2282b-108">Example 1: Create a job</span></span>
```
PS C:\>$PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation"
PS C:\> $PoolInformation.PoolId = "Pool22"
PS C:\> New-AzBatchJob -Id "ContosoJob35" -PoolInformation $PoolInformation -BatchContext $Context
```

<span data-ttu-id="2282b-109">第一個命令會使用 **Cmdlet 建立 PSPoolInformation** New-Object物件。</span><span class="sxs-lookup"><span data-stu-id="2282b-109">The first command creates a **PSPoolInformation** object by using the New-Object cmdlet.</span></span>
<span data-ttu-id="2282b-110">該命令會儲存該物件于$PoolInformation變數。</span><span class="sxs-lookup"><span data-stu-id="2282b-110">The command stores that object in the $PoolInformation variable.</span></span>
<span data-ttu-id="2282b-111">第二個命令會指派識別碼 Pool22 給目標物件 **中的 PoolId** 屬性$PoolInformation。</span><span class="sxs-lookup"><span data-stu-id="2282b-111">The second command assigns the ID Pool22 to the **PoolId** property of the object in $PoolInformation.</span></span>
<span data-ttu-id="2282b-112">最後一個命令會建立具有識別碼 ContosoJob35 的工作。</span><span class="sxs-lookup"><span data-stu-id="2282b-112">The final command creates a job that has the ID ContosoJob35.</span></span>
<span data-ttu-id="2282b-113">新增到工作的工作會執行在具有 ID Pool22 的集中。</span><span class="sxs-lookup"><span data-stu-id="2282b-113">Tasks added to the job run on the pool that has the ID Pool22.</span></span>
<span data-ttu-id="2282b-114">使用 Get-AzBatchAccountKey Cmdlet 將上下文指派給$CoNtext變數。</span><span class="sxs-lookup"><span data-stu-id="2282b-114">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="2282b-115">參數</span><span class="sxs-lookup"><span data-stu-id="2282b-115">PARAMETERS</span></span>

### <span data-ttu-id="2282b-116">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="2282b-116">-BatchContext</span></span>
<span data-ttu-id="2282b-117">指定此 Cmdlet 用來與批次處理服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="2282b-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="2282b-118">如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="2282b-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="2282b-119">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="2282b-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="2282b-120">使用共用金鑰驗證時，預設會使用主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="2282b-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="2282b-121">若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。</span><span class="sxs-lookup"><span data-stu-id="2282b-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="2282b-122">-CommonEnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="2282b-122">-CommonEnvironmentSettings</span></span>
<span data-ttu-id="2282b-123">指定此 Cmdlet 針對工作中所有工作所設定的共同環境變數，做為金鑰/值組。</span><span class="sxs-lookup"><span data-stu-id="2282b-123">Specifies the common environment variables, as key/value pairs, that this cmdlet sets for all tasks in the job.</span></span>
<span data-ttu-id="2282b-124">關鍵在於環境變數名稱。</span><span class="sxs-lookup"><span data-stu-id="2282b-124">The key is the environment variable name.</span></span>
<span data-ttu-id="2282b-125">該值是環境變數值。</span><span class="sxs-lookup"><span data-stu-id="2282b-125">The value is the environment variable value.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: CommonEnvironmentSetting

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2282b-126">-限制式</span><span class="sxs-lookup"><span data-stu-id="2282b-126">-Constraints</span></span>
<span data-ttu-id="2282b-127">指定工作的執行限制條件。</span><span class="sxs-lookup"><span data-stu-id="2282b-127">Specifies the execution constraints for the job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2282b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2282b-128">-DefaultProfile</span></span>
<span data-ttu-id="2282b-129">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2282b-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2282b-130">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2282b-130">-DisplayName</span></span>
<span data-ttu-id="2282b-131">指定工作的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="2282b-131">Specifies the display name for the job.</span></span>

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

### <span data-ttu-id="2282b-132">-Id</span><span class="sxs-lookup"><span data-stu-id="2282b-132">-Id</span></span>
<span data-ttu-id="2282b-133">指定工作的識別碼。</span><span class="sxs-lookup"><span data-stu-id="2282b-133">Specifies an ID for the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2282b-134">-JobManagerTask</span><span class="sxs-lookup"><span data-stu-id="2282b-134">-JobManagerTask</span></span>
<span data-ttu-id="2282b-135">指定 Job Manager 工作。</span><span class="sxs-lookup"><span data-stu-id="2282b-135">Specifies the Job Manager task.</span></span>
<span data-ttu-id="2282b-136">工作開始時，批次處理服務會執行 Job Manager 工作。</span><span class="sxs-lookup"><span data-stu-id="2282b-136">The Batch service runs the Job Manager task when the job is started.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobManagerTask
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2282b-137">-JobPreparationTask</span><span class="sxs-lookup"><span data-stu-id="2282b-137">-JobPreparationTask</span></span>
<span data-ttu-id="2282b-138">指定工作準備工作。</span><span class="sxs-lookup"><span data-stu-id="2282b-138">Specifies the Job Preparation task.</span></span>
<span data-ttu-id="2282b-139">批次處理服務會先在計算節點上執行工作準備工作，再于該計算節點上啟動該工作的任何工作。</span><span class="sxs-lookup"><span data-stu-id="2282b-139">The Batch service runs the Job Preparation task on a compute node before it starts any tasks of that job on that compute node.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTask
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2282b-140">-JobReleaseTask</span><span class="sxs-lookup"><span data-stu-id="2282b-140">-JobReleaseTask</span></span>
<span data-ttu-id="2282b-141">指定工作釋放工作。</span><span class="sxs-lookup"><span data-stu-id="2282b-141">Specifies the Job Release task.</span></span>
<span data-ttu-id="2282b-142">當工作結束時，批次處理服務會執行 Job Release 工作。</span><span class="sxs-lookup"><span data-stu-id="2282b-142">The Batch service runs the Job Release task when the job ends.</span></span>
<span data-ttu-id="2282b-143">批次處理服務會在每個執行任何工作之計算節點上執行 Job Release 工作。</span><span class="sxs-lookup"><span data-stu-id="2282b-143">The Batch service runs the Job Release task on each compute node where it ran any task of the job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobReleaseTask
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2282b-144">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="2282b-144">-Metadata</span></span>
<span data-ttu-id="2282b-145">指定要新加入工作的中繼資料，做為金鑰/值組。</span><span class="sxs-lookup"><span data-stu-id="2282b-145">Specifies metadata, as key/value pairs, to add to the job.</span></span>
<span data-ttu-id="2282b-146">鍵是中繼資料名稱。</span><span class="sxs-lookup"><span data-stu-id="2282b-146">The key is the metadata name.</span></span>
<span data-ttu-id="2282b-147">該值是中繼資料值。</span><span class="sxs-lookup"><span data-stu-id="2282b-147">The value is the metadata value.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2282b-148">-OnAllTasksComplete</span><span class="sxs-lookup"><span data-stu-id="2282b-148">-OnAllTasksComplete</span></span>
<span data-ttu-id="2282b-149">指定如果工作的所有工作都已完成，批次服務會採取的動作。</span><span class="sxs-lookup"><span data-stu-id="2282b-149">Specifies an action the Batch service takes if all tasks in the job are in the completed state.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.OnAllTasksComplete]
Parameter Sets: (All)
Aliases:
Accepted values: NoAction, TerminateJob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2282b-150">-OnTaskFailure</span><span class="sxs-lookup"><span data-stu-id="2282b-150">-OnTaskFailure</span></span>
<span data-ttu-id="2282b-151">指定當工作有任何任務失敗時，批次處理服務會採取的動作。</span><span class="sxs-lookup"><span data-stu-id="2282b-151">Specifies an action the Batch service takes if any task in the job fails.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.OnTaskFailure]
Parameter Sets: (All)
Aliases:
Accepted values: NoAction, PerformExitOptionsJobAction

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2282b-152">-PoolInformation</span><span class="sxs-lookup"><span data-stu-id="2282b-152">-PoolInformation</span></span>
<span data-ttu-id="2282b-153">指定批次處理服務執行工作之資料庫的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="2282b-153">Specifies the details of the pool on which the Batch service runs the tasks of the job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2282b-154">-優先順序</span><span class="sxs-lookup"><span data-stu-id="2282b-154">-Priority</span></span>
<span data-ttu-id="2282b-155">指定工作的優先順序。</span><span class="sxs-lookup"><span data-stu-id="2282b-155">Specifies the priority of the job.</span></span>
<span data-ttu-id="2282b-156">有效的值為：從 -1000 到 1000 的整數。</span><span class="sxs-lookup"><span data-stu-id="2282b-156">Valid values are: integers from -1000 to 1000.</span></span>
<span data-ttu-id="2282b-157">-1000 的值是最低的優先順序。</span><span class="sxs-lookup"><span data-stu-id="2282b-157">A value of -1000 is the lowest priority.</span></span>
<span data-ttu-id="2282b-158">1000 的值是最高優先順序。</span><span class="sxs-lookup"><span data-stu-id="2282b-158">A value of 1000 is the highest priority.</span></span>
<span data-ttu-id="2282b-159">預設值為 0。</span><span class="sxs-lookup"><span data-stu-id="2282b-159">The default value is 0.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2282b-160">-UsesTaskDependencies</span><span class="sxs-lookup"><span data-stu-id="2282b-160">-UsesTaskDependencies</span></span>
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

### <span data-ttu-id="2282b-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2282b-161">CommonParameters</span></span>
<span data-ttu-id="2282b-162">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2282b-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2282b-163">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2282b-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2282b-164">輸入</span><span class="sxs-lookup"><span data-stu-id="2282b-164">INPUTS</span></span>

### <span data-ttu-id="2282b-165">System.String</span><span class="sxs-lookup"><span data-stu-id="2282b-165">System.String</span></span>

### <span data-ttu-id="2282b-166">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="2282b-166">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="2282b-167">輸出</span><span class="sxs-lookup"><span data-stu-id="2282b-167">OUTPUTS</span></span>

### <span data-ttu-id="2282b-168">System.Void</span><span class="sxs-lookup"><span data-stu-id="2282b-168">System.Void</span></span>

## <span data-ttu-id="2282b-169">筆記</span><span class="sxs-lookup"><span data-stu-id="2282b-169">NOTES</span></span>

## <span data-ttu-id="2282b-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="2282b-170">RELATED LINKS</span></span>

[<span data-ttu-id="2282b-171">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2282b-171">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="2282b-172">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2282b-172">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="2282b-173">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="2282b-173">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="2282b-174">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2282b-174">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="2282b-175">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="2282b-175">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="2282b-176">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2282b-176">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="2282b-177">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2282b-177">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="2282b-178">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2282b-178">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
