---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 2B4BFDDA-9721-42E6-84E1-A209CB782954
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchTask.md
ms.openlocfilehash: dd8825be6491b0a0c8c8589f77180b38f9f230d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450029"
---
# <span data-ttu-id="7be91-101">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="7be91-101">New-AzureBatchTask</span></span>

## <span data-ttu-id="7be91-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7be91-102">SYNOPSIS</span></span>
<span data-ttu-id="7be91-103">在工作中建立批次任務。</span><span class="sxs-lookup"><span data-stu-id="7be91-103">Creates a Batch task under a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7be91-104">句法</span><span class="sxs-lookup"><span data-stu-id="7be91-104">SYNTAX</span></span>

### <span data-ttu-id="7be91-105">JobId_Single (預設) </span><span class="sxs-lookup"><span data-stu-id="7be91-105">JobId_Single (Default)</span></span>
```
New-AzureBatchTask -JobId <String> -Id <String> [-DisplayName <String>] [-CommandLine <String>]
 [-ResourceFiles <IDictionary>] [-EnvironmentSettings <IDictionary>] [-RunElevated]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-ExitConditions <PSExitConditions>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7be91-106">JobId_Bulk</span><span class="sxs-lookup"><span data-stu-id="7be91-106">JobId_Bulk</span></span>
```
New-AzureBatchTask -JobId <String> [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7be91-107">JobObject_Bulk</span><span class="sxs-lookup"><span data-stu-id="7be91-107">JobObject_Bulk</span></span>
```
New-AzureBatchTask [-Job <PSCloudJob>] [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7be91-108">JobObject_Single</span><span class="sxs-lookup"><span data-stu-id="7be91-108">JobObject_Single</span></span>
```
New-AzureBatchTask [-Job <PSCloudJob>] -Id <String> [-DisplayName <String>] [-CommandLine <String>]
 [-ResourceFiles <IDictionary>] [-EnvironmentSettings <IDictionary>] [-RunElevated]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-ExitConditions <PSExitConditions>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7be91-109">說明</span><span class="sxs-lookup"><span data-stu-id="7be91-109">DESCRIPTION</span></span>
<span data-ttu-id="7be91-110">**新的-AzureBatchTask** Cmdlet 會在 *JobId* 參數指定的作業或 *作業* 參數所指定的工作下，建立 Azure Batch 任務。</span><span class="sxs-lookup"><span data-stu-id="7be91-110">The **New-AzureBatchTask** cmdlet creates an Azure Batch task under the job specified by the *JobId* parameter or the *Job* parameter.</span></span>

## <span data-ttu-id="7be91-111">示例</span><span class="sxs-lookup"><span data-stu-id="7be91-111">EXAMPLES</span></span>

### <span data-ttu-id="7be91-112">範例1：建立批次任務</span><span class="sxs-lookup"><span data-stu-id="7be91-112">Example 1: Create a Batch task</span></span>
```
PS C:\>New-AzureBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
```

<span data-ttu-id="7be91-113">這個命令會在具有 ID 作業的作業（000001）下建立具有識別碼 Task23 的工作。</span><span class="sxs-lookup"><span data-stu-id="7be91-113">This command creates a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="7be91-114">任務會執行指定的命令。</span><span class="sxs-lookup"><span data-stu-id="7be91-114">The task runs the specified command.</span></span>
<span data-ttu-id="7be91-115">使用 **AzureRmBatchAccountKeys** Cmdlet，將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="7be91-115">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="7be91-116">範例2：建立批次任務</span><span class="sxs-lookup"><span data-stu-id="7be91-116">Example 2: Create a Batch task</span></span>
```
PS C:\>Get-AzureBatchJob -Id "Job-000001" -BatchContext $Context | New-AzureBatchTask -Id "Task26" -CommandLine "cmd /c echo hello > newFile.txt" -RunElevated -BatchContext $Context
```

<span data-ttu-id="7be91-117">這個命令會使用 **AzureBatchJob** Cmdlet 來取得具有識別碼 job 000001 的批次作業。</span><span class="sxs-lookup"><span data-stu-id="7be91-117">This command gets the Batch job that has the ID Job-000001 by using the **Get-AzureBatchJob** cmdlet.</span></span>
<span data-ttu-id="7be91-118">命令會使用管線運算子，將該作業傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7be91-118">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7be91-119">該命令會建立一個工作，並在該作業下包含識別碼 Task26。</span><span class="sxs-lookup"><span data-stu-id="7be91-119">The command creates a task that has the ID Task26 under that job.</span></span>
<span data-ttu-id="7be91-120">工作會使用提升許可權來執行指定的命令。</span><span class="sxs-lookup"><span data-stu-id="7be91-120">The task runs the specified command by using elevated permissions.</span></span>

### <span data-ttu-id="7be91-121">範例3：使用管線將任務集合新增至指定的工作</span><span class="sxs-lookup"><span data-stu-id="7be91-121">Example 3: Add a collection of tasks to the specified job by using the pipeline</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> Get-AzureBatchJob -Id "Job-000001" -BatchContext $Context | New-AzureBatchTask -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="7be91-122">第一個命令會使用 **AzureRmBatchAccountKeys** 建立名為 ContosoBatchAccount 的 batch 帳戶的帳戶金鑰的物件參考。</span><span class="sxs-lookup"><span data-stu-id="7be91-122">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="7be91-123">該命令會將這個物件參照儲存在 $CoNtext 變數中。</span><span class="sxs-lookup"><span data-stu-id="7be91-123">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="7be91-124">接下來的兩個命令會使用 New-Object Cmdlet 來建立 **PSCloudTask** 物件。</span><span class="sxs-lookup"><span data-stu-id="7be91-124">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="7be91-125">這些命令會將工作儲存在 $Task 01 和 $Task 02 變數中。</span><span class="sxs-lookup"><span data-stu-id="7be91-125">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>

<span data-ttu-id="7be91-126">最後一個命令會使用 **AzureBatchJob** 來取得具有 ID 作業000001的批次作業。</span><span class="sxs-lookup"><span data-stu-id="7be91-126">The final command gets the Batch job that has the ID Job-000001 by using **Get-AzureBatchJob**.</span></span>
<span data-ttu-id="7be91-127">然後，命令會使用管線運算子，將該作業傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7be91-127">Then the command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7be91-128">該命令會將工作集合新增至該作業底下。</span><span class="sxs-lookup"><span data-stu-id="7be91-128">The command adds a collection of tasks under that job.</span></span>
<span data-ttu-id="7be91-129">命令會使用儲存在 $CoNtext 中的內容。</span><span class="sxs-lookup"><span data-stu-id="7be91-129">The command uses the context stored in $Context.</span></span>

### <span data-ttu-id="7be91-130">範例4：新增任務的集合至指定的工作</span><span class="sxs-lookup"><span data-stu-id="7be91-130">Example 4: Add a collection of tasks to the specified job</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> New-AzureBatchTask -JobId "Job-000001" -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="7be91-131">第一個命令會使用 **AzureRmBatchAccountKeys** 建立名為 ContosoBatchAccount 的 batch 帳戶的帳戶金鑰的物件參考。</span><span class="sxs-lookup"><span data-stu-id="7be91-131">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="7be91-132">該命令會將這個物件參照儲存在 $CoNtext 變數中。</span><span class="sxs-lookup"><span data-stu-id="7be91-132">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="7be91-133">接下來的兩個命令會使用 New-Object Cmdlet 來建立 **PSCloudTask** 物件。</span><span class="sxs-lookup"><span data-stu-id="7be91-133">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="7be91-134">這些命令會將工作儲存在 $Task 01 和 $Task 02 變數中。</span><span class="sxs-lookup"><span data-stu-id="7be91-134">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>

<span data-ttu-id="7be91-135">最後一個命令會將儲存在 $Task 01 和 $Task 02 中的任務新增至具有識別碼作業的作業-000001。</span><span class="sxs-lookup"><span data-stu-id="7be91-135">The final command adds the tasks stored in $Task01 and $Task02 under the job that has the ID Job-000001.</span></span>

## <span data-ttu-id="7be91-136">參數</span><span class="sxs-lookup"><span data-stu-id="7be91-136">PARAMETERS</span></span>

### <span data-ttu-id="7be91-137">-AffinityInformation</span><span class="sxs-lookup"><span data-stu-id="7be91-137">-AffinityInformation</span></span>
<span data-ttu-id="7be91-138">指定批次服務用來選取要在其上執行工作之節點的位置提示。</span><span class="sxs-lookup"><span data-stu-id="7be91-138">Specifies a locality hint that the Batch service uses to select a node on which to run the task.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSAffinityInformation
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7be91-139">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="7be91-139">-ApplicationPackageReferences</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSApplicationPackageReference[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7be91-140">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="7be91-140">-BatchContext</span></span>
<span data-ttu-id="7be91-141">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="7be91-141">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="7be91-142">若要取得包含您訂閱之便捷鍵的 **BatchAccountCoNtext** 物件，請使用 Get-AzureRmBatchAccountKeys Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7be91-142">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="7be91-143">-命令列</span><span class="sxs-lookup"><span data-stu-id="7be91-143">-CommandLine</span></span>
<span data-ttu-id="7be91-144">指定任務的命令列。</span><span class="sxs-lookup"><span data-stu-id="7be91-144">Specifies the command line for the task.</span></span>

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7be91-145">-限制式</span><span class="sxs-lookup"><span data-stu-id="7be91-145">-Constraints</span></span>
<span data-ttu-id="7be91-146">指定適用于此任務的執行限制。</span><span class="sxs-lookup"><span data-stu-id="7be91-146">Specifies the execution constraints that apply to this task.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7be91-147">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="7be91-147">-DependsOn</span></span>
<span data-ttu-id="7be91-148">指定任務依賴于其他任務。</span><span class="sxs-lookup"><span data-stu-id="7be91-148">Specifies that the task depends on other tasks.</span></span>
<span data-ttu-id="7be91-149">除非所有依存的任務都已順利完成，否則不會排程任務。</span><span class="sxs-lookup"><span data-stu-id="7be91-149">The task will not be scheduled until all depended-on tasks have completed successfully.</span></span>

```yaml
Type: Microsoft.Azure.Batch.TaskDependencies
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7be91-150">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7be91-150">-DisplayName</span></span>
<span data-ttu-id="7be91-151">指定任務的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="7be91-151">Specifies the display name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7be91-152">-EnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="7be91-152">-EnvironmentSettings</span></span>
<span data-ttu-id="7be91-153">指定此 Cmdlet 在工作中新增的環境設定，做為索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="7be91-153">Specifies the environment settings, as key/value pairs, that this cmdlet adds to the task.</span></span>
<span data-ttu-id="7be91-154">金鑰就是環境設定名稱。</span><span class="sxs-lookup"><span data-stu-id="7be91-154">The key is the environment setting name.</span></span>
<span data-ttu-id="7be91-155">此值為 [環境] 設定。</span><span class="sxs-lookup"><span data-stu-id="7be91-155">The value is the environment setting.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7be91-156">-ExitConditions</span><span class="sxs-lookup"><span data-stu-id="7be91-156">-ExitConditions</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSExitConditions
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7be91-157">-識別碼</span><span class="sxs-lookup"><span data-stu-id="7be91-157">-Id</span></span>
<span data-ttu-id="7be91-158">指定任務的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7be91-158">Specifies the ID of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7be91-159">-工作</span><span class="sxs-lookup"><span data-stu-id="7be91-159">-Job</span></span>
<span data-ttu-id="7be91-160">指定此 Cmdlet 建立任務所依據的作業。</span><span class="sxs-lookup"><span data-stu-id="7be91-160">Specifies the job under which this cmdlet creates the task.</span></span>
<span data-ttu-id="7be91-161">若要取得 **PSCloudJob** 物件，請使用 Get-AzureBatchJob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7be91-161">To obtain a **PSCloudJob** object, use the Get-AzureBatchJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: JobObject_Bulk, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7be91-162">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="7be91-162">-JobId</span></span>
<span data-ttu-id="7be91-163">指定此 Cmdlet 建立任務時所用作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7be91-163">Specifies the ID of the job under which this cmdlet creates the task.</span></span>

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobId_Bulk
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7be91-164">-MultiInstanceSettings</span><span class="sxs-lookup"><span data-stu-id="7be91-164">-MultiInstanceSettings</span></span>
<span data-ttu-id="7be91-165">指定如何執行多重實例任務的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7be91-165">Specifies information about how to run a multi-instance task.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7be91-166">-ResourceFiles</span><span class="sxs-lookup"><span data-stu-id="7be91-166">-ResourceFiles</span></span>
<span data-ttu-id="7be91-167">指定任務所需的資源檔（作為索引鍵/值組）。</span><span class="sxs-lookup"><span data-stu-id="7be91-167">Specifies resource files, as key/value pairs, that the task requires.</span></span>
<span data-ttu-id="7be91-168">金鑰就是資源檔路徑。</span><span class="sxs-lookup"><span data-stu-id="7be91-168">The key is the resource file path.</span></span>
<span data-ttu-id="7be91-169">此值是資源檔 blob 來源。</span><span class="sxs-lookup"><span data-stu-id="7be91-169">The value is the resource file blob source.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7be91-170">-RunElevated</span><span class="sxs-lookup"><span data-stu-id="7be91-170">-RunElevated</span></span>
<span data-ttu-id="7be91-171">表示工作流程以系統管理員許可權執行。</span><span class="sxs-lookup"><span data-stu-id="7be91-171">Indicates that the task process runs with administrator privileges.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7be91-172">-任務</span><span class="sxs-lookup"><span data-stu-id="7be91-172">-Tasks</span></span>
<span data-ttu-id="7be91-173">指定要新增的任務集合。</span><span class="sxs-lookup"><span data-stu-id="7be91-173">Specifies the collection of tasks to be added.</span></span>
<span data-ttu-id="7be91-174">每個工作必須具有唯一的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7be91-174">Each task must have a unique ID.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask[]
Parameter Sets: JobId_Bulk, JobObject_Bulk
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7be91-175">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7be91-175">-DefaultProfile</span></span>
<span data-ttu-id="7be91-176">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7be91-176">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7be91-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7be91-177">CommonParameters</span></span>
<span data-ttu-id="7be91-178">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7be91-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7be91-179">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7be91-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7be91-180">輸入</span><span class="sxs-lookup"><span data-stu-id="7be91-180">INPUTS</span></span>

### <span data-ttu-id="7be91-181">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="7be91-181">BatchAccountContext</span></span>
<span data-ttu-id="7be91-182">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="7be91-182">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="7be91-183">PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="7be91-183">PSCloudJob</span></span>
<span data-ttu-id="7be91-184">參數「作業」接受管道中類型 ' PSCloudJob」的值</span><span class="sxs-lookup"><span data-stu-id="7be91-184">Parameter 'Job' accepts value of type 'PSCloudJob' from the pipeline</span></span>

## <span data-ttu-id="7be91-185">輸出</span><span class="sxs-lookup"><span data-stu-id="7be91-185">OUTPUTS</span></span>

## <span data-ttu-id="7be91-186">筆記</span><span class="sxs-lookup"><span data-stu-id="7be91-186">NOTES</span></span>

## <span data-ttu-id="7be91-187">相關連結</span><span class="sxs-lookup"><span data-stu-id="7be91-187">RELATED LINKS</span></span>

[<span data-ttu-id="7be91-188">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="7be91-188">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="7be91-189">AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="7be91-189">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="7be91-190">AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="7be91-190">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="7be91-191">新-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="7be91-191">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="7be91-192">移除-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="7be91-192">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="7be91-193">停止 AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="7be91-193">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="7be91-194">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7be91-194">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


