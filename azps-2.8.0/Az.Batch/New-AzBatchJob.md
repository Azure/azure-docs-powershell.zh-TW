---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B6229D26-D38C-44CD-B9CA-7F39365C8B9D
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJob.md
ms.openlocfilehash: 09e2d3effbe99c6f0f126b0665330b077f27af80
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2020
ms.locfileid: "93799638"
---
# <span data-ttu-id="69038-101">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="69038-101">New-AzBatchJob</span></span>

## <span data-ttu-id="69038-102">摘要</span><span class="sxs-lookup"><span data-stu-id="69038-102">SYNOPSIS</span></span>
<span data-ttu-id="69038-103">在批次服務中建立作業。</span><span class="sxs-lookup"><span data-stu-id="69038-103">Creates a job in the Batch service.</span></span>

## <span data-ttu-id="69038-104">句法</span><span class="sxs-lookup"><span data-stu-id="69038-104">SYNTAX</span></span>

```
New-AzBatchJob [-Id] <String> [-CommonEnvironmentSettings <IDictionary>] [-DisplayName <String>]
 [-Constraints <PSJobConstraints>] [-JobManagerTask <PSJobManagerTask>]
 [-JobPreparationTask <PSJobPreparationTask>] [-JobReleaseTask <PSJobReleaseTask>] [-Metadata <IDictionary>]
 -PoolInformation <PSPoolInformation> [-Priority <Int32>] [-UsesTaskDependencies]
 [-OnTaskFailure <OnTaskFailure>] [-OnAllTasksComplete <OnAllTasksComplete>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69038-105">說明</span><span class="sxs-lookup"><span data-stu-id="69038-105">DESCRIPTION</span></span>
<span data-ttu-id="69038-106">**AzBatchJob** Cmdlet 會在由 *BatchAccountCoNtext* 參數指定的帳號中，在 Azure Batch services 中建立作業。</span><span class="sxs-lookup"><span data-stu-id="69038-106">The **New-AzBatchJob** cmdlet creates a job in the Azure Batch service in the account specified by the *BatchAccountContext* parameter.</span></span>

## <span data-ttu-id="69038-107">示例</span><span class="sxs-lookup"><span data-stu-id="69038-107">EXAMPLES</span></span>

### <span data-ttu-id="69038-108">範例1：建立工作</span><span class="sxs-lookup"><span data-stu-id="69038-108">Example 1: Create a job</span></span>
```
PS C:\>$PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation" 
PS C:\> $PoolInformation.PoolId = "Pool22" 
PS C:\> New-AzBatchJob -Id "ContosoJob35" -PoolInformation $PoolInformation -BatchContext $Context
```

<span data-ttu-id="69038-109">第一個命令會使用 New-Object Cmdlet 來建立 **PSPoolInformation** 物件。</span><span class="sxs-lookup"><span data-stu-id="69038-109">The first command creates a **PSPoolInformation** object by using the New-Object cmdlet.</span></span>
<span data-ttu-id="69038-110">該命令會將該物件儲存在 $PoolInformation 變數中。</span><span class="sxs-lookup"><span data-stu-id="69038-110">The command stores that object in the $PoolInformation variable.</span></span>
<span data-ttu-id="69038-111">第二個命令會將識別碼 Pool22 指派給 $PoolInformation 中物件的 **PoolId** 屬性。</span><span class="sxs-lookup"><span data-stu-id="69038-111">The second command assigns the ID Pool22 to the **PoolId** property of the object in $PoolInformation.</span></span>
<span data-ttu-id="69038-112">最後一個命令會建立一個具有識別碼 ContosoJob35 的作業。</span><span class="sxs-lookup"><span data-stu-id="69038-112">The final command creates a job that has the ID ContosoJob35.</span></span>
<span data-ttu-id="69038-113">新增至作業的工作會在擁有識別碼 Pool22 的池中執行。</span><span class="sxs-lookup"><span data-stu-id="69038-113">Tasks added to the job run on the pool that has the ID Pool22.</span></span>
<span data-ttu-id="69038-114">使用 Get-AzBatchAccountKeys Cmdlet 將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="69038-114">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="69038-115">參數</span><span class="sxs-lookup"><span data-stu-id="69038-115">PARAMETERS</span></span>

### <span data-ttu-id="69038-116">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="69038-116">-BatchContext</span></span>
<span data-ttu-id="69038-117">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="69038-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="69038-118">如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="69038-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="69038-119">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="69038-119">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="69038-120">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="69038-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="69038-121">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="69038-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="69038-122">-CommonEnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="69038-122">-CommonEnvironmentSettings</span></span>
<span data-ttu-id="69038-123">指定此 Cmdlet 針對作業中所有工作所設定的一般環境變數（做為索引鍵/值組）。</span><span class="sxs-lookup"><span data-stu-id="69038-123">Specifies the common environment variables, as key/value pairs, that this cmdlet sets for all tasks in the job.</span></span>
<span data-ttu-id="69038-124">索引鍵是環境變數名稱。</span><span class="sxs-lookup"><span data-stu-id="69038-124">The key is the environment variable name.</span></span>
<span data-ttu-id="69038-125">此值是環境變數的值。</span><span class="sxs-lookup"><span data-stu-id="69038-125">The value is the environment variable value.</span></span>

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

### <span data-ttu-id="69038-126">-限制式</span><span class="sxs-lookup"><span data-stu-id="69038-126">-Constraints</span></span>
<span data-ttu-id="69038-127">指定作業的執行限制。</span><span class="sxs-lookup"><span data-stu-id="69038-127">Specifies the execution constraints for the job.</span></span>

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

### <span data-ttu-id="69038-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69038-128">-DefaultProfile</span></span>
<span data-ttu-id="69038-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="69038-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69038-130">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="69038-130">-DisplayName</span></span>
<span data-ttu-id="69038-131">指定作業的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="69038-131">Specifies the display name for the job.</span></span>

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

### <span data-ttu-id="69038-132">-識別碼</span><span class="sxs-lookup"><span data-stu-id="69038-132">-Id</span></span>
<span data-ttu-id="69038-133">指定作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="69038-133">Specifies an ID for the job.</span></span>

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

### <span data-ttu-id="69038-134">-JobManagerTask</span><span class="sxs-lookup"><span data-stu-id="69038-134">-JobManagerTask</span></span>
<span data-ttu-id="69038-135">指定作業管理員任務。</span><span class="sxs-lookup"><span data-stu-id="69038-135">Specifies the Job Manager task.</span></span>
<span data-ttu-id="69038-136">[批次服務] 會在作業啟動時執行作業管理員的工作。</span><span class="sxs-lookup"><span data-stu-id="69038-136">The Batch service runs the Job Manager task when the job is started.</span></span>

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

### <span data-ttu-id="69038-137">-JobPreparationTask</span><span class="sxs-lookup"><span data-stu-id="69038-137">-JobPreparationTask</span></span>
<span data-ttu-id="69038-138">指定作業準備工作。</span><span class="sxs-lookup"><span data-stu-id="69038-138">Specifies the Job Preparation task.</span></span>
<span data-ttu-id="69038-139">Batch 服務會在計算節點上執行工作準備工作，然後才會在該計算節點上啟動該作業的任何任務。</span><span class="sxs-lookup"><span data-stu-id="69038-139">The Batch service runs the Job Preparation task on a compute node before it starts any tasks of that job on that compute node.</span></span>

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

### <span data-ttu-id="69038-140">-JobReleaseTask</span><span class="sxs-lookup"><span data-stu-id="69038-140">-JobReleaseTask</span></span>
<span data-ttu-id="69038-141">指定作業發行任務。</span><span class="sxs-lookup"><span data-stu-id="69038-141">Specifies the Job Release task.</span></span>
<span data-ttu-id="69038-142">當作業結束時，批次服務會執行作業發行工作。</span><span class="sxs-lookup"><span data-stu-id="69038-142">The Batch service runs the Job Release task when the job ends.</span></span>
<span data-ttu-id="69038-143">批次服務會在執行工作的每個計算節點上執行作業發行任務。</span><span class="sxs-lookup"><span data-stu-id="69038-143">The Batch service runs the Job Release task on each compute node where it ran any task of the job.</span></span>

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

### <span data-ttu-id="69038-144">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="69038-144">-Metadata</span></span>
<span data-ttu-id="69038-145">指定中繼資料（做為索引鍵/值組）以新增至作業。</span><span class="sxs-lookup"><span data-stu-id="69038-145">Specifies metadata, as key/value pairs, to add to the job.</span></span>
<span data-ttu-id="69038-146">金鑰就是中繼資料名稱。</span><span class="sxs-lookup"><span data-stu-id="69038-146">The key is the metadata name.</span></span>
<span data-ttu-id="69038-147">此值為中繼資料值。</span><span class="sxs-lookup"><span data-stu-id="69038-147">The value is the metadata value.</span></span>

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

### <span data-ttu-id="69038-148">-OnAllTasksComplete</span><span class="sxs-lookup"><span data-stu-id="69038-148">-OnAllTasksComplete</span></span>
<span data-ttu-id="69038-149">指定當作業中的所有任務都處於 [已完成] 狀態時，批次服務所採取的動作。</span><span class="sxs-lookup"><span data-stu-id="69038-149">Specifies an action the Batch service takes if all tasks in the job are in the completed state.</span></span>

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

### <span data-ttu-id="69038-150">-OnTaskFailure</span><span class="sxs-lookup"><span data-stu-id="69038-150">-OnTaskFailure</span></span>
<span data-ttu-id="69038-151">指定當作業中的任何任務失敗時，批服務會採取的動作。</span><span class="sxs-lookup"><span data-stu-id="69038-151">Specifies an action the Batch service takes if any task in the job fails.</span></span>

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

### <span data-ttu-id="69038-152">-PoolInformation</span><span class="sxs-lookup"><span data-stu-id="69038-152">-PoolInformation</span></span>
<span data-ttu-id="69038-153">指定批服務在其上執行作業工作之池的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="69038-153">Specifies the details of the pool on which the Batch service runs the tasks of the job.</span></span>

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

### <span data-ttu-id="69038-154">-優先順序</span><span class="sxs-lookup"><span data-stu-id="69038-154">-Priority</span></span>
<span data-ttu-id="69038-155">指定作業的優先順序。</span><span class="sxs-lookup"><span data-stu-id="69038-155">Specifies the priority of the job.</span></span>
<span data-ttu-id="69038-156">有效值為：從-1000 到1000的整數。</span><span class="sxs-lookup"><span data-stu-id="69038-156">Valid values are: integers from -1000 to 1000.</span></span>
<span data-ttu-id="69038-157">值為-1000 是最低優先順序。</span><span class="sxs-lookup"><span data-stu-id="69038-157">A value of -1000 is the lowest priority.</span></span>
<span data-ttu-id="69038-158">1000的值是最高優先順序。</span><span class="sxs-lookup"><span data-stu-id="69038-158">A value of 1000 is the highest priority.</span></span>
<span data-ttu-id="69038-159">預設值為0。</span><span class="sxs-lookup"><span data-stu-id="69038-159">The default value is 0.</span></span>

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

### <span data-ttu-id="69038-160">-UsesTaskDependencies</span><span class="sxs-lookup"><span data-stu-id="69038-160">-UsesTaskDependencies</span></span>
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

### <span data-ttu-id="69038-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69038-161">CommonParameters</span></span>
<span data-ttu-id="69038-162">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="69038-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69038-163">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="69038-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69038-164">輸入</span><span class="sxs-lookup"><span data-stu-id="69038-164">INPUTS</span></span>

### <span data-ttu-id="69038-165">System.object</span><span class="sxs-lookup"><span data-stu-id="69038-165">System.String</span></span>

### <span data-ttu-id="69038-166">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="69038-166">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="69038-167">輸出</span><span class="sxs-lookup"><span data-stu-id="69038-167">OUTPUTS</span></span>

### <span data-ttu-id="69038-168">System.void</span><span class="sxs-lookup"><span data-stu-id="69038-168">System.Void</span></span>

## <span data-ttu-id="69038-169">筆記</span><span class="sxs-lookup"><span data-stu-id="69038-169">NOTES</span></span>

## <span data-ttu-id="69038-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="69038-170">RELATED LINKS</span></span>

[<span data-ttu-id="69038-171">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="69038-171">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="69038-172">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="69038-172">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="69038-173">AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="69038-173">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="69038-174">AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="69038-174">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="69038-175">AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="69038-175">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="69038-176">移除-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="69038-176">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="69038-177">停止 AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="69038-177">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="69038-178">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="69038-178">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


