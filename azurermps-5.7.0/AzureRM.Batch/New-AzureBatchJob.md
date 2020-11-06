---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B6229D26-D38C-44CD-B9CA-7F39365C8B9D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJob.md
ms.openlocfilehash: bf96b5930895332de2e78ffdee71f9f6a2654b83
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457188"
---
# <span data-ttu-id="246b8-101">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="246b8-101">New-AzureBatchJob</span></span>

## <span data-ttu-id="246b8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="246b8-102">SYNOPSIS</span></span>
<span data-ttu-id="246b8-103">在批次服務中建立作業。</span><span class="sxs-lookup"><span data-stu-id="246b8-103">Creates a job in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="246b8-104">句法</span><span class="sxs-lookup"><span data-stu-id="246b8-104">SYNTAX</span></span>

```
New-AzureBatchJob [-Id] <String> [-CommonEnvironmentSettings <IDictionary>] [-DisplayName <String>]
 [-Constraints <PSJobConstraints>] [-JobManagerTask <PSJobManagerTask>]
 [-JobPreparationTask <PSJobPreparationTask>] [-JobReleaseTask <PSJobReleaseTask>] [-Metadata <IDictionary>]
 -PoolInformation <PSPoolInformation> [-Priority <Int32>] [-UsesTaskDependencies]
 [-OnTaskFailure <OnTaskFailure>] [-OnAllTasksComplete <OnAllTasksComplete>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="246b8-105">說明</span><span class="sxs-lookup"><span data-stu-id="246b8-105">DESCRIPTION</span></span>
<span data-ttu-id="246b8-106">**AzureBatchJob** Cmdlet 會在由 *BatchAccountCoNtext* 參數指定的帳號中，在 Azure Batch services 中建立作業。</span><span class="sxs-lookup"><span data-stu-id="246b8-106">The **New-AzureBatchJob** cmdlet creates a job in the Azure Batch service in the account specified by the *BatchAccountContext* parameter.</span></span>

## <span data-ttu-id="246b8-107">示例</span><span class="sxs-lookup"><span data-stu-id="246b8-107">EXAMPLES</span></span>

### <span data-ttu-id="246b8-108">範例1：建立工作</span><span class="sxs-lookup"><span data-stu-id="246b8-108">Example 1: Create a job</span></span>
```
PS C:\>$PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation" 
PS C:\> $PoolInformation.PoolId = "Pool22" 
PS C:\> New-AzureBatchJob -Id "ContosoJob35" -PoolInformation $PoolInformation -BatchContext $Context
```

<span data-ttu-id="246b8-109">第一個命令會使用 New-Object Cmdlet 來建立 **PSPoolInformation** 物件。</span><span class="sxs-lookup"><span data-stu-id="246b8-109">The first command creates a **PSPoolInformation** object by using the New-Object cmdlet.</span></span>
<span data-ttu-id="246b8-110">該命令會將該物件儲存在 $PoolInformation 變數中。</span><span class="sxs-lookup"><span data-stu-id="246b8-110">The command stores that object in the $PoolInformation variable.</span></span>

<span data-ttu-id="246b8-111">第二個命令會將識別碼 Pool22 指派給 $PoolInformation 中物件的 **PoolId** 屬性。</span><span class="sxs-lookup"><span data-stu-id="246b8-111">The second command assigns the ID Pool22 to the **PoolId** property of the object in $PoolInformation.</span></span>

<span data-ttu-id="246b8-112">最後一個命令會建立一個具有識別碼 ContosoJob35 的作業。</span><span class="sxs-lookup"><span data-stu-id="246b8-112">The final command creates a job that has the ID ContosoJob35.</span></span>
<span data-ttu-id="246b8-113">新增至作業的工作會在擁有識別碼 Pool22 的池中執行。</span><span class="sxs-lookup"><span data-stu-id="246b8-113">Tasks added to the job run on the pool that has the ID Pool22.</span></span>
<span data-ttu-id="246b8-114">使用 Get-AzureRmBatchAccountKeys Cmdlet 將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="246b8-114">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="246b8-115">參數</span><span class="sxs-lookup"><span data-stu-id="246b8-115">PARAMETERS</span></span>

### <span data-ttu-id="246b8-116">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="246b8-116">-BatchContext</span></span>
<span data-ttu-id="246b8-117">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="246b8-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="246b8-118">如果您使用 Get-AzureRmBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="246b8-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="246b8-119">若要改為使用共用金鑰驗證，請使用 Get-AzureRmBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="246b8-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="246b8-120">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="246b8-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="246b8-121">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="246b8-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="246b8-122">-CommonEnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="246b8-122">-CommonEnvironmentSettings</span></span>
<span data-ttu-id="246b8-123">指定此 Cmdlet 針對作業中所有工作所設定的一般環境變數（做為索引鍵/值組）。</span><span class="sxs-lookup"><span data-stu-id="246b8-123">Specifies the common environment variables, as key/value pairs, that this cmdlet sets for all tasks in the job.</span></span>
<span data-ttu-id="246b8-124">索引鍵是環境變數名稱。</span><span class="sxs-lookup"><span data-stu-id="246b8-124">The key is the environment variable name.</span></span>
<span data-ttu-id="246b8-125">此值是環境變數的值。</span><span class="sxs-lookup"><span data-stu-id="246b8-125">The value is the environment variable value.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: CommonEnvironmentSetting

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="246b8-126">-限制式</span><span class="sxs-lookup"><span data-stu-id="246b8-126">-Constraints</span></span>
<span data-ttu-id="246b8-127">指定作業的執行限制。</span><span class="sxs-lookup"><span data-stu-id="246b8-127">Specifies the execution constraints for the job.</span></span>

```yaml
Type: PSJobConstraints
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="246b8-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="246b8-128">-DefaultProfile</span></span>
<span data-ttu-id="246b8-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="246b8-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="246b8-130">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="246b8-130">-DisplayName</span></span>
<span data-ttu-id="246b8-131">指定作業的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="246b8-131">Specifies the display name for the job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="246b8-132">-識別碼</span><span class="sxs-lookup"><span data-stu-id="246b8-132">-Id</span></span>
<span data-ttu-id="246b8-133">指定作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="246b8-133">Specifies an ID for the job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="246b8-134">-JobManagerTask</span><span class="sxs-lookup"><span data-stu-id="246b8-134">-JobManagerTask</span></span>
<span data-ttu-id="246b8-135">指定作業管理員任務。</span><span class="sxs-lookup"><span data-stu-id="246b8-135">Specifies the Job Manager task.</span></span>
<span data-ttu-id="246b8-136">[批次服務] 會在作業啟動時執行作業管理員的工作。</span><span class="sxs-lookup"><span data-stu-id="246b8-136">The Batch service runs the Job Manager task when the job is started.</span></span>

```yaml
Type: PSJobManagerTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="246b8-137">-JobPreparationTask</span><span class="sxs-lookup"><span data-stu-id="246b8-137">-JobPreparationTask</span></span>
<span data-ttu-id="246b8-138">指定作業準備工作。</span><span class="sxs-lookup"><span data-stu-id="246b8-138">Specifies the Job Preparation task.</span></span>
<span data-ttu-id="246b8-139">Batch 服務會在計算節點上執行工作準備工作，然後才會在該計算節點上啟動該作業的任何任務。</span><span class="sxs-lookup"><span data-stu-id="246b8-139">The Batch service runs the Job Preparation task on a compute node before it starts any tasks of that job on that compute node.</span></span>

```yaml
Type: PSJobPreparationTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="246b8-140">-JobReleaseTask</span><span class="sxs-lookup"><span data-stu-id="246b8-140">-JobReleaseTask</span></span>
<span data-ttu-id="246b8-141">指定作業發行任務。</span><span class="sxs-lookup"><span data-stu-id="246b8-141">Specifies the Job Release task.</span></span>
<span data-ttu-id="246b8-142">當作業結束時，批次服務會執行作業發行工作。</span><span class="sxs-lookup"><span data-stu-id="246b8-142">The Batch service runs the Job Release task when the job ends.</span></span>
<span data-ttu-id="246b8-143">批次服務會在執行工作的每個計算節點上執行作業發行任務。</span><span class="sxs-lookup"><span data-stu-id="246b8-143">The Batch service runs the Job Release task on each compute node where it ran any task of the job.</span></span>

```yaml
Type: PSJobReleaseTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="246b8-144">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="246b8-144">-Metadata</span></span>
<span data-ttu-id="246b8-145">指定中繼資料（做為索引鍵/值組）以新增至作業。</span><span class="sxs-lookup"><span data-stu-id="246b8-145">Specifies metadata, as key/value pairs, to add to the job.</span></span>
<span data-ttu-id="246b8-146">金鑰就是中繼資料名稱。</span><span class="sxs-lookup"><span data-stu-id="246b8-146">The key is the metadata name.</span></span>
<span data-ttu-id="246b8-147">此值為中繼資料值。</span><span class="sxs-lookup"><span data-stu-id="246b8-147">The value is the metadata value.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="246b8-148">-OnAllTasksComplete</span><span class="sxs-lookup"><span data-stu-id="246b8-148">-OnAllTasksComplete</span></span>
<span data-ttu-id="246b8-149">指定當作業中的所有任務都處於 [已完成] 狀態時，批次服務所採取的動作。</span><span class="sxs-lookup"><span data-stu-id="246b8-149">Specifies an action the Batch service takes if all tasks in the job are in the completed state.</span></span>

```yaml
Type: OnAllTasksComplete
Parameter Sets: (All)
Aliases: 
Accepted values: NoAction, TerminateJob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="246b8-150">-OnTaskFailure</span><span class="sxs-lookup"><span data-stu-id="246b8-150">-OnTaskFailure</span></span>
<span data-ttu-id="246b8-151">指定當作業中的任何任務失敗時，批服務會採取的動作。</span><span class="sxs-lookup"><span data-stu-id="246b8-151">Specifies an action the Batch service takes if any task in the job fails.</span></span>

```yaml
Type: OnTaskFailure
Parameter Sets: (All)
Aliases: 
Accepted values: NoAction, PerformExitOptionsJobAction

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="246b8-152">-PoolInformation</span><span class="sxs-lookup"><span data-stu-id="246b8-152">-PoolInformation</span></span>
<span data-ttu-id="246b8-153">指定批服務在其上執行作業工作之池的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="246b8-153">Specifies the details of the pool on which the Batch service runs the tasks of the job.</span></span>

```yaml
Type: PSPoolInformation
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="246b8-154">-優先順序</span><span class="sxs-lookup"><span data-stu-id="246b8-154">-Priority</span></span>
<span data-ttu-id="246b8-155">指定作業的優先順序。</span><span class="sxs-lookup"><span data-stu-id="246b8-155">Specifies the priority of the job.</span></span>
<span data-ttu-id="246b8-156">有效值為：從-1000 到1000的整數。</span><span class="sxs-lookup"><span data-stu-id="246b8-156">Valid values are: integers from -1000 to 1000.</span></span>
<span data-ttu-id="246b8-157">值為-1000 是最低優先順序。</span><span class="sxs-lookup"><span data-stu-id="246b8-157">A value of -1000 is the lowest priority.</span></span>
<span data-ttu-id="246b8-158">1000的值是最高優先順序。</span><span class="sxs-lookup"><span data-stu-id="246b8-158">A value of 1000 is the highest priority.</span></span>
<span data-ttu-id="246b8-159">預設值為0。</span><span class="sxs-lookup"><span data-stu-id="246b8-159">The default value is 0.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="246b8-160">-UsesTaskDependencies</span><span class="sxs-lookup"><span data-stu-id="246b8-160">-UsesTaskDependencies</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="246b8-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="246b8-161">CommonParameters</span></span>
<span data-ttu-id="246b8-162">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="246b8-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="246b8-163">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="246b8-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="246b8-164">輸入</span><span class="sxs-lookup"><span data-stu-id="246b8-164">INPUTS</span></span>

### <span data-ttu-id="246b8-165">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="246b8-165">BatchAccountContext</span></span>
<span data-ttu-id="246b8-166">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="246b8-166">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="246b8-167">輸出</span><span class="sxs-lookup"><span data-stu-id="246b8-167">OUTPUTS</span></span>

## <span data-ttu-id="246b8-168">筆記</span><span class="sxs-lookup"><span data-stu-id="246b8-168">NOTES</span></span>

## <span data-ttu-id="246b8-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="246b8-169">RELATED LINKS</span></span>

[<span data-ttu-id="246b8-170">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="246b8-170">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="246b8-171">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="246b8-171">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="246b8-172">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="246b8-172">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="246b8-173">AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="246b8-173">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="246b8-174">AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="246b8-174">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="246b8-175">移除-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="246b8-175">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="246b8-176">停止 AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="246b8-176">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="246b8-177">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="246b8-177">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


