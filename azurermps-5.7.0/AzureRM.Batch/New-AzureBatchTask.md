---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 2B4BFDDA-9721-42E6-84E1-A209CB782954
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchTask.md
ms.openlocfilehash: 904c3a40f8f153a97bf8016f3708a310adfea3bd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625632"
---
# <span data-ttu-id="78f66-101">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="78f66-101">New-AzureBatchTask</span></span>

## <span data-ttu-id="78f66-102">摘要</span><span class="sxs-lookup"><span data-stu-id="78f66-102">SYNOPSIS</span></span>
<span data-ttu-id="78f66-103">在工作中建立批次任務。</span><span class="sxs-lookup"><span data-stu-id="78f66-103">Creates a Batch task under a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78f66-104">句法</span><span class="sxs-lookup"><span data-stu-id="78f66-104">SYNTAX</span></span>

### <span data-ttu-id="78f66-105">JobId_Single (預設) </span><span class="sxs-lookup"><span data-stu-id="78f66-105">JobId_Single (Default)</span></span>
```
New-AzureBatchTask -JobId <String> -Id <String> [-DisplayName <String>] [-CommandLine <String>]
 [-ResourceFiles <IDictionary>] [-EnvironmentSettings <IDictionary>]
 [-AuthenticationTokenSettings <PSAuthenticationTokenSettings>] [-UserIdentity <PSUserIdentity>]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-OutputFile <PSOutputFile[]>]
 [-ExitConditions <PSExitConditions>] [-ContainerSettings <PSTaskContainerSettings>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78f66-106">JobId_Bulk</span><span class="sxs-lookup"><span data-stu-id="78f66-106">JobId_Bulk</span></span>
```
New-AzureBatchTask -JobId <String> [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78f66-107">JobObject_Bulk</span><span class="sxs-lookup"><span data-stu-id="78f66-107">JobObject_Bulk</span></span>
```
New-AzureBatchTask [-Job <PSCloudJob>] [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78f66-108">JobObject_Single</span><span class="sxs-lookup"><span data-stu-id="78f66-108">JobObject_Single</span></span>
```
New-AzureBatchTask [-Job <PSCloudJob>] -Id <String> [-DisplayName <String>] [-CommandLine <String>]
 [-ResourceFiles <IDictionary>] [-EnvironmentSettings <IDictionary>]
 [-AuthenticationTokenSettings <PSAuthenticationTokenSettings>] [-UserIdentity <PSUserIdentity>]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-OutputFile <PSOutputFile[]>]
 [-ExitConditions <PSExitConditions>] [-ContainerSettings <PSTaskContainerSettings>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78f66-109">說明</span><span class="sxs-lookup"><span data-stu-id="78f66-109">DESCRIPTION</span></span>
<span data-ttu-id="78f66-110">**新的-AzureBatchTask** Cmdlet 會在 *JobId* 參數指定的作業或 *作業* 參數所指定的工作下，建立 Azure Batch 任務。</span><span class="sxs-lookup"><span data-stu-id="78f66-110">The **New-AzureBatchTask** cmdlet creates an Azure Batch task under the job specified by the *JobId* parameter or the *Job* parameter.</span></span>

## <span data-ttu-id="78f66-111">示例</span><span class="sxs-lookup"><span data-stu-id="78f66-111">EXAMPLES</span></span>

### <span data-ttu-id="78f66-112">範例1：建立批次任務</span><span class="sxs-lookup"><span data-stu-id="78f66-112">Example 1: Create a Batch task</span></span>
```
PS C:\>New-AzureBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
```

<span data-ttu-id="78f66-113">這個命令會在具有 ID 作業的作業（000001）下建立具有識別碼 Task23 的工作。</span><span class="sxs-lookup"><span data-stu-id="78f66-113">This command creates a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="78f66-114">任務會執行指定的命令。</span><span class="sxs-lookup"><span data-stu-id="78f66-114">The task runs the specified command.</span></span>
<span data-ttu-id="78f66-115">使用 **AzureRmBatchAccountKeys** Cmdlet，將內容指派給 $CoNtext 變數。</span><span class="sxs-lookup"><span data-stu-id="78f66-115">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="78f66-116">範例2：建立批次任務</span><span class="sxs-lookup"><span data-stu-id="78f66-116">Example 2: Create a Batch task</span></span>
```
PS C:\> $autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
PS C:\> $userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
PS C:\>Get-AzureBatchJob -Id "Job-000001" -BatchContext $Context | New-AzureBatchTask -Id "Task26" -CommandLine "cmd /c echo hello > newFile.txt" -UserIdentity $userIdentity -BatchContext $Context
```

<span data-ttu-id="78f66-117">這個命令會使用 **AzureBatchJob** Cmdlet 來取得具有識別碼 job 000001 的批次作業。</span><span class="sxs-lookup"><span data-stu-id="78f66-117">This command gets the Batch job that has the ID Job-000001 by using the **Get-AzureBatchJob** cmdlet.</span></span>
<span data-ttu-id="78f66-118">命令會使用管線運算子，將該作業傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="78f66-118">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="78f66-119">該命令會建立一個工作，並在該作業下包含識別碼 Task26。</span><span class="sxs-lookup"><span data-stu-id="78f66-119">The command creates a task that has the ID Task26 under that job.</span></span>
<span data-ttu-id="78f66-120">工作會使用提升許可權來執行指定的命令。</span><span class="sxs-lookup"><span data-stu-id="78f66-120">The task runs the specified command by using elevated permissions.</span></span>

### <span data-ttu-id="78f66-121">範例3：使用管線將任務集合新增至指定的工作</span><span class="sxs-lookup"><span data-stu-id="78f66-121">Example 3: Add a collection of tasks to the specified job by using the pipeline</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> Get-AzureBatchJob -Id "Job-000001" -BatchContext $Context | New-AzureBatchTask -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="78f66-122">第一個命令會使用 **AzureRmBatchAccountKeys** 建立名為 ContosoBatchAccount 的 batch 帳戶的帳戶金鑰的物件參考。</span><span class="sxs-lookup"><span data-stu-id="78f66-122">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="78f66-123">該命令會將這個物件參照儲存在 $CoNtext 變數中。</span><span class="sxs-lookup"><span data-stu-id="78f66-123">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="78f66-124">接下來的兩個命令會使用 New-Object Cmdlet 來建立 **PSCloudTask** 物件。</span><span class="sxs-lookup"><span data-stu-id="78f66-124">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="78f66-125">這些命令會將工作儲存在 $Task 01 和 $Task 02 變數中。</span><span class="sxs-lookup"><span data-stu-id="78f66-125">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>

<span data-ttu-id="78f66-126">最後一個命令會使用 **AzureBatchJob** 來取得具有 ID 作業000001的批次作業。</span><span class="sxs-lookup"><span data-stu-id="78f66-126">The final command gets the Batch job that has the ID Job-000001 by using **Get-AzureBatchJob**.</span></span>
<span data-ttu-id="78f66-127">然後，命令會使用管線運算子，將該作業傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="78f66-127">Then the command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="78f66-128">該命令會將工作集合新增至該作業底下。</span><span class="sxs-lookup"><span data-stu-id="78f66-128">The command adds a collection of tasks under that job.</span></span>
<span data-ttu-id="78f66-129">命令會使用儲存在 $CoNtext 中的內容。</span><span class="sxs-lookup"><span data-stu-id="78f66-129">The command uses the context stored in $Context.</span></span>

### <span data-ttu-id="78f66-130">範例4：新增任務的集合至指定的工作</span><span class="sxs-lookup"><span data-stu-id="78f66-130">Example 4: Add a collection of tasks to the specified job</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> New-AzureBatchTask -JobId "Job-000001" -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="78f66-131">第一個命令會使用 **AzureRmBatchAccountKeys** 建立名為 ContosoBatchAccount 的 batch 帳戶的帳戶金鑰的物件參考。</span><span class="sxs-lookup"><span data-stu-id="78f66-131">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="78f66-132">該命令會將這個物件參照儲存在 $CoNtext 變數中。</span><span class="sxs-lookup"><span data-stu-id="78f66-132">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="78f66-133">接下來的兩個命令會使用 New-Object Cmdlet 來建立 **PSCloudTask** 物件。</span><span class="sxs-lookup"><span data-stu-id="78f66-133">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="78f66-134">這些命令會將工作儲存在 $Task 01 和 $Task 02 變數中。</span><span class="sxs-lookup"><span data-stu-id="78f66-134">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>

<span data-ttu-id="78f66-135">最後一個命令會將儲存在 $Task 01 和 $Task 02 中的任務新增至具有識別碼作業的作業-000001。</span><span class="sxs-lookup"><span data-stu-id="78f66-135">The final command adds the tasks stored in $Task01 and $Task02 under the job that has the ID Job-000001.</span></span>

### <span data-ttu-id="78f66-136">範例5：使用輸出檔案新增任務</span><span class="sxs-lookup"><span data-stu-id="78f66-136">Example 5: Add a task with output files</span></span>
```
PS C:\>New-AzureBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
PS C:\>$blobContainerDestination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileBlobContainerDestination "https://myaccount.blob.core.windows.net/sascontainer?sv=2015-04-05&st=2015-04-29T22%3A18%3A26Z&se=2015-04-30T02%3A23%3A26Z&sr=b&sp=rw&spr=https&sig=Z%2FRHIX5Xcg0Mq2rqI3OlWTjEg2tYkboXr1P9ZUXDtkk%3D"
PS C:\>$destination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileDestination $blobContainerDestination
PS C:\>$uploadOptions = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileUploadOptions "TaskSuccess"
PS C:\>$outputFile = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFile "*.txt", $blobContainerDestination, $uploadOptions

PS C:\>New-AzureBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -OutputFile $outputFile -BatchContext $Context
```

### <span data-ttu-id="78f66-137">範例6：新增具有驗證權杖設定的任務</span><span class="sxs-lookup"><span data-stu-id="78f66-137">Example 6: Add a task with authentication token settings</span></span>
```
PS C:\>$authSettings = New-Object Microsoft.Azure.Commands.Batch.Models.PSAuthenticationTokenSettings
PS C:\>$authSettings.Access = "Job"
PS C:\>New-AzureBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -AuthenticationTokenSettings $authSettings -BatchContext $Context
```

### <span data-ttu-id="78f66-138">範例7：新增在容器中執行的工作</span><span class="sxs-lookup"><span data-stu-id="78f66-138">Example 7: Add a task which runs in a container</span></span>
```
PS C:\>New-AzureBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ContainerSettings New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskContainerSettings "containerImageName"
```

## <span data-ttu-id="78f66-139">參數</span><span class="sxs-lookup"><span data-stu-id="78f66-139">PARAMETERS</span></span>

### <span data-ttu-id="78f66-140">-AffinityInformation</span><span class="sxs-lookup"><span data-stu-id="78f66-140">-AffinityInformation</span></span>
<span data-ttu-id="78f66-141">指定批次服務用來選取要在其上執行工作之節點的位置提示。</span><span class="sxs-lookup"><span data-stu-id="78f66-141">Specifies a locality hint that the Batch service uses to select a node on which to run the task.</span></span>

```yaml
Type: PSAffinityInformation
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f66-142">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="78f66-142">-ApplicationPackageReferences</span></span>
```yaml
Type: PSApplicationPackageReference[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases: ApplicationPackageReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f66-143">-AuthenticationTokenSettings</span><span class="sxs-lookup"><span data-stu-id="78f66-143">-AuthenticationTokenSettings</span></span>
<span data-ttu-id="78f66-144">可用於執行批服務作業之驗證權杖的設定。</span><span class="sxs-lookup"><span data-stu-id="78f66-144">The settings for an authentication token that the task can use to perform Batch service operations.</span></span>

<span data-ttu-id="78f66-145">如果已設定此選項，則批次服務會提供具有驗證權杖的工作，可用於在不需要帳戶存取金鑰的情況下驗證批服務作業。</span><span class="sxs-lookup"><span data-stu-id="78f66-145">If this is set, the Batch service provides the task with an authentication token which can be used to authenticate Batch service operations without requiring an account access key.</span></span> <span data-ttu-id="78f66-146">權杖是透過 AZ_BATCH_AUTHENTICATION_TOKEN 環境變數提供。</span><span class="sxs-lookup"><span data-stu-id="78f66-146">The token is provided via the AZ_BATCH_AUTHENTICATION_TOKEN environment variable.</span></span> <span data-ttu-id="78f66-147">任務可以使用權杖執行的作業取決於設定。</span><span class="sxs-lookup"><span data-stu-id="78f66-147">The operations that the task can carry out using the token depend on the settings.</span></span> <span data-ttu-id="78f66-148">例如，任務可以要求作業許可權，以便將其他工作新增至作業，或檢查作業或其他任務的狀態。</span><span class="sxs-lookup"><span data-stu-id="78f66-148">For example, a task can request job permissions in order to add other tasks to the job, or check the status of the job or of other tasks.</span></span>

```yaml
Type: PSAuthenticationTokenSettings
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f66-149">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="78f66-149">-BatchContext</span></span>
<span data-ttu-id="78f66-150">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="78f66-150">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="78f66-151">如果您使用 Get-AzureRmBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="78f66-151">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="78f66-152">若要改為使用共用金鑰驗證，請使用 Get-AzureRmBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="78f66-152">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="78f66-153">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="78f66-153">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="78f66-154">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="78f66-154">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="78f66-155">-命令列</span><span class="sxs-lookup"><span data-stu-id="78f66-155">-CommandLine</span></span>
<span data-ttu-id="78f66-156">指定任務的命令列。</span><span class="sxs-lookup"><span data-stu-id="78f66-156">Specifies the command line for the task.</span></span>

```yaml
Type: String
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f66-157">-限制式</span><span class="sxs-lookup"><span data-stu-id="78f66-157">-Constraints</span></span>
<span data-ttu-id="78f66-158">指定適用于此任務的執行限制。</span><span class="sxs-lookup"><span data-stu-id="78f66-158">Specifies the execution constraints that apply to this task.</span></span>

```yaml
Type: PSTaskConstraints
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f66-159">-ContainerSettings</span><span class="sxs-lookup"><span data-stu-id="78f66-159">-ContainerSettings</span></span>
<span data-ttu-id="78f66-160">在其下執行任務的容器的設定。</span><span class="sxs-lookup"><span data-stu-id="78f66-160">The settings for the container under which the task runs.</span></span>

<span data-ttu-id="78f66-161">如果執行此工作的池已設定 containerConfiguration，也必須加以設定。</span><span class="sxs-lookup"><span data-stu-id="78f66-161">If the pool that will run this task has containerConfiguration set, this must be set as well.</span></span> <span data-ttu-id="78f66-162">如果執行此工作的池子沒有設定 containerConfiguration，就不一定要設定此選項。</span><span class="sxs-lookup"><span data-stu-id="78f66-162">If the pool that will run this task doesn't have containerConfiguration set, this must not be set.</span></span> <span data-ttu-id="78f66-163">如果已指定此專案，則會將節點) 上的 Azure 批次目錄根目錄 AZ_BATCH_NODE_ROOT_DIR 下的所有目錄都以遞迴方式 (對應到容器，所有工作環境變數都會對應到該容器，而且會在容器中執行任務命令列。</span><span class="sxs-lookup"><span data-stu-id="78f66-163">When this is specified, all directories recursively below the AZ_BATCH_NODE_ROOT_DIR (the root of Azure Batch directories on the node) are mapped into the container, all task environment variables are mapped into the container, and the task command line is executed in the container.</span></span>

```yaml
Type: PSTaskContainerSettings
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f66-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78f66-164">-DefaultProfile</span></span>
<span data-ttu-id="78f66-165">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="78f66-165">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78f66-166">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="78f66-166">-DependsOn</span></span>
<span data-ttu-id="78f66-167">指定任務依賴于其他任務。</span><span class="sxs-lookup"><span data-stu-id="78f66-167">Specifies that the task depends on other tasks.</span></span>
<span data-ttu-id="78f66-168">除非所有依存的任務都已順利完成，否則不會排程任務。</span><span class="sxs-lookup"><span data-stu-id="78f66-168">The task will not be scheduled until all depended-on tasks have completed successfully.</span></span>

```yaml
Type: TaskDependencies
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f66-169">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="78f66-169">-DisplayName</span></span>
<span data-ttu-id="78f66-170">指定任務的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="78f66-170">Specifies the display name of the task.</span></span>

```yaml
Type: String
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f66-171">-EnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="78f66-171">-EnvironmentSettings</span></span>
<span data-ttu-id="78f66-172">指定此 Cmdlet 在工作中新增的環境設定，做為索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="78f66-172">Specifies the environment settings, as key/value pairs, that this cmdlet adds to the task.</span></span>
<span data-ttu-id="78f66-173">金鑰就是環境設定名稱。</span><span class="sxs-lookup"><span data-stu-id="78f66-173">The key is the environment setting name.</span></span>
<span data-ttu-id="78f66-174">此值為 [環境] 設定。</span><span class="sxs-lookup"><span data-stu-id="78f66-174">The value is the environment setting.</span></span>

```yaml
Type: IDictionary
Parameter Sets: JobId_Single, JobObject_Single
Aliases: EnvironmentSetting

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f66-175">-ExitConditions</span><span class="sxs-lookup"><span data-stu-id="78f66-175">-ExitConditions</span></span>
```yaml
Type: PSExitConditions
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f66-176">-識別碼</span><span class="sxs-lookup"><span data-stu-id="78f66-176">-Id</span></span>
<span data-ttu-id="78f66-177">指定任務的識別碼。</span><span class="sxs-lookup"><span data-stu-id="78f66-177">Specifies the ID of the task.</span></span>

```yaml
Type: String
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f66-178">-工作</span><span class="sxs-lookup"><span data-stu-id="78f66-178">-Job</span></span>
<span data-ttu-id="78f66-179">指定此 Cmdlet 建立任務所依據的作業。</span><span class="sxs-lookup"><span data-stu-id="78f66-179">Specifies the job under which this cmdlet creates the task.</span></span>
<span data-ttu-id="78f66-180">若要取得 **PSCloudJob** 物件，請使用 Get-AzureBatchJob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="78f66-180">To obtain a **PSCloudJob** object, use the Get-AzureBatchJob cmdlet.</span></span>

```yaml
Type: PSCloudJob
Parameter Sets: JobObject_Bulk, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78f66-181">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="78f66-181">-JobId</span></span>
<span data-ttu-id="78f66-182">指定此 Cmdlet 建立任務時所用作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="78f66-182">Specifies the ID of the job under which this cmdlet creates the task.</span></span>

```yaml
Type: String
Parameter Sets: JobId_Single, JobId_Bulk
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f66-183">-MultiInstanceSettings</span><span class="sxs-lookup"><span data-stu-id="78f66-183">-MultiInstanceSettings</span></span>
<span data-ttu-id="78f66-184">指定如何執行多重實例任務的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="78f66-184">Specifies information about how to run a multi-instance task.</span></span>

```yaml
Type: PSMultiInstanceSettings
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f66-185">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="78f66-185">-OutputFile</span></span>
<span data-ttu-id="78f66-186">取得或設定在執行命令列之後，批服務將從計算節點上傳的檔案清單。</span><span class="sxs-lookup"><span data-stu-id="78f66-186">Gets or sets a list of files that the Batch service will upload from the compute node after running the command line.</span></span>

<span data-ttu-id="78f66-187">針對多重實例工作，這些檔案只會從執行主要任務的計算節點上傳。</span><span class="sxs-lookup"><span data-stu-id="78f66-187">For multi-instance tasks, the files will only be uploaded from the compute node on which the primary task is executed.</span></span>

```yaml
Type: PSOutputFile[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f66-188">-ResourceFiles</span><span class="sxs-lookup"><span data-stu-id="78f66-188">-ResourceFiles</span></span>
<span data-ttu-id="78f66-189">指定任務所需的資源檔（作為索引鍵/值組）。</span><span class="sxs-lookup"><span data-stu-id="78f66-189">Specifies resource files, as key/value pairs, that the task requires.</span></span>
<span data-ttu-id="78f66-190">金鑰就是資源檔路徑。</span><span class="sxs-lookup"><span data-stu-id="78f66-190">The key is the resource file path.</span></span>
<span data-ttu-id="78f66-191">此值是資源檔 blob 來源。</span><span class="sxs-lookup"><span data-stu-id="78f66-191">The value is the resource file blob source.</span></span>

```yaml
Type: IDictionary
Parameter Sets: JobId_Single, JobObject_Single
Aliases: ResourceFile

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f66-192">-任務</span><span class="sxs-lookup"><span data-stu-id="78f66-192">-Tasks</span></span>
<span data-ttu-id="78f66-193">指定要新增的任務集合。</span><span class="sxs-lookup"><span data-stu-id="78f66-193">Specifies the collection of tasks to be added.</span></span>
<span data-ttu-id="78f66-194">每個工作必須具有唯一的識別碼。</span><span class="sxs-lookup"><span data-stu-id="78f66-194">Each task must have a unique ID.</span></span>

```yaml
Type: PSCloudTask[]
Parameter Sets: JobId_Bulk, JobObject_Bulk
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f66-195">-UserIdentity</span><span class="sxs-lookup"><span data-stu-id="78f66-195">-UserIdentity</span></span>
<span data-ttu-id="78f66-196">執行任務所依據的使用者身分識別。</span><span class="sxs-lookup"><span data-stu-id="78f66-196">The user identity under which the task runs.</span></span>

```yaml
Type: PSUserIdentity
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f66-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78f66-197">CommonParameters</span></span>
<span data-ttu-id="78f66-198">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="78f66-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78f66-199">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="78f66-199">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78f66-200">輸入</span><span class="sxs-lookup"><span data-stu-id="78f66-200">INPUTS</span></span>

### <span data-ttu-id="78f66-201">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="78f66-201">BatchAccountContext</span></span>
<span data-ttu-id="78f66-202">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="78f66-202">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="78f66-203">PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="78f66-203">PSCloudJob</span></span>
<span data-ttu-id="78f66-204">參數「作業」接受管道中類型 ' PSCloudJob」的值</span><span class="sxs-lookup"><span data-stu-id="78f66-204">Parameter 'Job' accepts value of type 'PSCloudJob' from the pipeline</span></span>

## <span data-ttu-id="78f66-205">輸出</span><span class="sxs-lookup"><span data-stu-id="78f66-205">OUTPUTS</span></span>

## <span data-ttu-id="78f66-206">筆記</span><span class="sxs-lookup"><span data-stu-id="78f66-206">NOTES</span></span>

## <span data-ttu-id="78f66-207">相關連結</span><span class="sxs-lookup"><span data-stu-id="78f66-207">RELATED LINKS</span></span>

[<span data-ttu-id="78f66-208">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="78f66-208">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="78f66-209">AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="78f66-209">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="78f66-210">AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="78f66-210">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="78f66-211">新-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="78f66-211">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="78f66-212">移除-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="78f66-212">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="78f66-213">停止 AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="78f66-213">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="78f66-214">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="78f66-214">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


