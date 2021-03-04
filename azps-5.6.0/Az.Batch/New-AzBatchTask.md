---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2B4BFDDA-9721-42E6-84E1-A209CB782954
online version: https://docs.microsoft.com/powershell/module/az.batch/new-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchTask.md
ms.openlocfilehash: 254c9290b2cc838dc7ec53c2590d8505c24c1b69
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912469"
---
# <span data-ttu-id="972d4-101">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="972d4-101">New-AzBatchTask</span></span>

## <span data-ttu-id="972d4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="972d4-102">SYNOPSIS</span></span>
<span data-ttu-id="972d4-103">在工作下建立批次工作。</span><span class="sxs-lookup"><span data-stu-id="972d4-103">Creates a Batch task under a job.</span></span>

## <span data-ttu-id="972d4-104">語法</span><span class="sxs-lookup"><span data-stu-id="972d4-104">SYNTAX</span></span>

### <span data-ttu-id="972d4-105">JobId_Single (預設) </span><span class="sxs-lookup"><span data-stu-id="972d4-105">JobId_Single (Default)</span></span>
```
New-AzBatchTask -JobId <String> -Id <String> [-DisplayName <String>] -CommandLine <String>
 [-ResourceFiles <PSResourceFile[]>] [-EnvironmentSettings <IDictionary>]
 [-AuthenticationTokenSettings <PSAuthenticationTokenSettings>] [-UserIdentity <PSUserIdentity>]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-OutputFile <PSOutputFile[]>]
 [-ExitConditions <PSExitConditions>] [-ContainerSettings <PSTaskContainerSettings>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="972d4-106">JobId_Bulk</span><span class="sxs-lookup"><span data-stu-id="972d4-106">JobId_Bulk</span></span>
```
New-AzBatchTask -JobId <String> [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="972d4-107">JobObject_Bulk</span><span class="sxs-lookup"><span data-stu-id="972d4-107">JobObject_Bulk</span></span>
```
New-AzBatchTask [-Job <PSCloudJob>] [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="972d4-108">JobObject_Single</span><span class="sxs-lookup"><span data-stu-id="972d4-108">JobObject_Single</span></span>
```
New-AzBatchTask [-Job <PSCloudJob>] -Id <String> [-DisplayName <String>] -CommandLine <String>
 [-ResourceFiles <PSResourceFile[]>] [-EnvironmentSettings <IDictionary>]
 [-AuthenticationTokenSettings <PSAuthenticationTokenSettings>] [-UserIdentity <PSUserIdentity>]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-OutputFile <PSOutputFile[]>]
 [-ExitConditions <PSExitConditions>] [-ContainerSettings <PSTaskContainerSettings>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="972d4-109">描述</span><span class="sxs-lookup"><span data-stu-id="972d4-109">DESCRIPTION</span></span>
<span data-ttu-id="972d4-110">**New-AzBatchTask** Cmdlet 會依據 *JobId* 參數或 Job 參數指定的工作建立 *Azure 批次* 工作。</span><span class="sxs-lookup"><span data-stu-id="972d4-110">The **New-AzBatchTask** cmdlet creates an Azure Batch task under the job specified by the *JobId* parameter or the *Job* parameter.</span></span>

## <span data-ttu-id="972d4-111">例子</span><span class="sxs-lookup"><span data-stu-id="972d4-111">EXAMPLES</span></span>

### <span data-ttu-id="972d4-112">範例 1：建立批次工作</span><span class="sxs-lookup"><span data-stu-id="972d4-112">Example 1: Create a Batch task</span></span>
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
```

<span data-ttu-id="972d4-113">此命令會建立在具有識別碼 Job-000001 的工作下具有識別碼工作 23 的工作。</span><span class="sxs-lookup"><span data-stu-id="972d4-113">This command creates a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="972d4-114">任務會執行指定的命令。</span><span class="sxs-lookup"><span data-stu-id="972d4-114">The task runs the specified command.</span></span>
<span data-ttu-id="972d4-115">使用 **Get-AzBatchAccountKey** Cmdlet 將上下文指派給$CoNtext變數。</span><span class="sxs-lookup"><span data-stu-id="972d4-115">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="972d4-116">範例 2：建立批次工作</span><span class="sxs-lookup"><span data-stu-id="972d4-116">Example 2: Create a Batch task</span></span>
```
PS C:\> $autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
PS C:\> $userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
PS C:\>Get-AzBatchJob -Id "Job-000001" -BatchContext $Context | New-AzBatchTask -Id "Task26" -CommandLine "cmd /c echo hello > newFile.txt" -UserIdentity $userIdentity -BatchContext $Context
```

<span data-ttu-id="972d4-117">此命令會使用 **Get-AzBatchJob** Cmdlet 取得具有識別碼 Job-000001 的批次處理工作。</span><span class="sxs-lookup"><span data-stu-id="972d4-117">This command gets the Batch job that has the ID Job-000001 by using the **Get-AzBatchJob** cmdlet.</span></span>
<span data-ttu-id="972d4-118">該命令會使用管線運算子，將工作傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="972d4-118">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="972d4-119">命令會建立一個工作，該工作下有識別碼工作 26。</span><span class="sxs-lookup"><span data-stu-id="972d4-119">The command creates a task that has the ID Task26 under that job.</span></span>
<span data-ttu-id="972d4-120">工作會使用較高的權限執行指定的命令。</span><span class="sxs-lookup"><span data-stu-id="972d4-120">The task runs the specified command by using elevated permissions.</span></span>

### <span data-ttu-id="972d4-121">範例 3：使用管線將工作集合新增到指定的工作</span><span class="sxs-lookup"><span data-stu-id="972d4-121">Example 3: Add a collection of tasks to the specified job by using the pipeline</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> Get-AzBatchJob -Id "Job-000001" -BatchContext $Context | New-AzBatchTask -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="972d4-122">第一個命令會使用 **Get-AzBatchAccountKey，為名為 ContosoBatchAccount** 的批次帳戶建立帳戶金鑰的物件參照。</span><span class="sxs-lookup"><span data-stu-id="972d4-122">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="972d4-123">命令會在此變數中儲存$CoNtext參照。</span><span class="sxs-lookup"><span data-stu-id="972d4-123">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="972d4-124">接下來兩個命令會使用 **Cmdlet 建立 PSCloudTask** 物件New-Object物件。</span><span class="sxs-lookup"><span data-stu-id="972d4-124">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="972d4-125">命令會儲存在 $Task 01 和 $Task 02 變數中。</span><span class="sxs-lookup"><span data-stu-id="972d4-125">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>
<span data-ttu-id="972d4-126">最後一個命令會使用 **Get-AzBatchJob** 取得具有識別碼 Job-000001 的批次處理工作。</span><span class="sxs-lookup"><span data-stu-id="972d4-126">The final command gets the Batch job that has the ID Job-000001 by using **Get-AzBatchJob**.</span></span>
<span data-ttu-id="972d4-127">然後命令會使用管線運算子，將工作傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="972d4-127">Then the command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="972d4-128">該命令會新增該工作下的工作集合。</span><span class="sxs-lookup"><span data-stu-id="972d4-128">The command adds a collection of tasks under that job.</span></span>
<span data-ttu-id="972d4-129">命令會使用儲存在 $CoNtext。</span><span class="sxs-lookup"><span data-stu-id="972d4-129">The command uses the context stored in $Context.</span></span>

### <span data-ttu-id="972d4-130">範例 4：新增工作集合至指定的工作</span><span class="sxs-lookup"><span data-stu-id="972d4-130">Example 4: Add a collection of tasks to the specified job</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> New-AzBatchTask -JobId "Job-000001" -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="972d4-131">第一個命令會使用 **Get-AzBatchAccountKey，為名為 ContosoBatchAccount** 的批次帳戶建立帳戶金鑰的物件參照。</span><span class="sxs-lookup"><span data-stu-id="972d4-131">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="972d4-132">命令會在此變數中儲存$CoNtext參照。</span><span class="sxs-lookup"><span data-stu-id="972d4-132">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="972d4-133">接下來兩個命令會使用 **Cmdlet 建立 PSCloudTask** 物件New-Object物件。</span><span class="sxs-lookup"><span data-stu-id="972d4-133">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="972d4-134">命令會儲存在 $Task 01 和 $Task 02 變數中。</span><span class="sxs-lookup"><span data-stu-id="972d4-134">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>
<span data-ttu-id="972d4-135">最後一個命令會將儲存在 $Task 001 和 $Task 02 的工作中具有 ID Job-000001 的工作中的工作加入。</span><span class="sxs-lookup"><span data-stu-id="972d4-135">The final command adds the tasks stored in $Task01 and $Task02 under the job that has the ID Job-000001.</span></span>

### <span data-ttu-id="972d4-136">範例 5：使用輸出檔案新增工作</span><span class="sxs-lookup"><span data-stu-id="972d4-136">Example 5: Add a task with output files</span></span>
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
PS C:\>$blobContainerDestination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileBlobContainerDestination "https://myaccount.blob.core.windows.net/sascontainer?sv=2015-04-05&st=2015-04-29T22%3A18%3A26Z&se=2015-04-30T02%3A23%3A26Z&sr=b&sp=rw&spr=https&sig=Z%2FRHIX5Xcg0Mq2rqI3OlWTjEg2tYkboXr1P9ZUXDtkk%3D"
PS C:\>$destination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileDestination $blobContainerDestination
PS C:\>$uploadOptions = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileUploadOptions "TaskSuccess"
PS C:\>$outputFile = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFile "*.txt", $blobContainerDestination, $uploadOptions

PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -OutputFile $outputFile -BatchContext $Context
```

### <span data-ttu-id="972d4-137">範例 6：使用驗證權杖設定新增工作</span><span class="sxs-lookup"><span data-stu-id="972d4-137">Example 6: Add a task with authentication token settings</span></span>
```
PS C:\>$authSettings = New-Object Microsoft.Azure.Commands.Batch.Models.PSAuthenticationTokenSettings
PS C:\>$authSettings.Access = "Job"
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -AuthenticationTokenSettings $authSettings -BatchContext $Context
```

### <span data-ttu-id="972d4-138">範例 7：新增在容器中執行的工作</span><span class="sxs-lookup"><span data-stu-id="972d4-138">Example 7: Add a task which runs in a container</span></span>
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ContainerSettings New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskContainerSettings "containerImageName"
```

## <span data-ttu-id="972d4-139">參數</span><span class="sxs-lookup"><span data-stu-id="972d4-139">PARAMETERS</span></span>

### <span data-ttu-id="972d4-140">-AffinityInformation</span><span class="sxs-lookup"><span data-stu-id="972d4-140">-AffinityInformation</span></span>
<span data-ttu-id="972d4-141">指定 Batch 服務用來選取執行任務的節點之地區提示。</span><span class="sxs-lookup"><span data-stu-id="972d4-141">Specifies a locality hint that the Batch service uses to select a node on which to run the task.</span></span>

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

### <span data-ttu-id="972d4-142">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="972d4-142">-ApplicationPackageReferences</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSApplicationPackageReference[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases: ApplicationPackageReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="972d4-143">-AuthenticationTokenSettings</span><span class="sxs-lookup"><span data-stu-id="972d4-143">-AuthenticationTokenSettings</span></span>
<span data-ttu-id="972d4-144">工作可用於執行批次處理服務作業之驗證權杖的設定。</span><span class="sxs-lookup"><span data-stu-id="972d4-144">The settings for an authentication token that the task can use to perform Batch service operations.</span></span>
<span data-ttu-id="972d4-145">如果已設定此設定，批次服務會提供工作驗證權杖，可用來驗證批次處理服務作業，而不需要帳戶訪問金鑰。</span><span class="sxs-lookup"><span data-stu-id="972d4-145">If this is set, the Batch service provides the task with an authentication token which can be used to authenticate Batch service operations without requiring an account access key.</span></span> <span data-ttu-id="972d4-146">權杖是透過AZ_BATCH_AUTHENTICATION_TOKEN變數提供。</span><span class="sxs-lookup"><span data-stu-id="972d4-146">The token is provided via the AZ_BATCH_AUTHENTICATION_TOKEN environment variable.</span></span> <span data-ttu-id="972d4-147">任務可以使用權杖執行的操作取決於設定。</span><span class="sxs-lookup"><span data-stu-id="972d4-147">The operations that the task can carry out using the token depend on the settings.</span></span> <span data-ttu-id="972d4-148">例如，工作可以要求工作許可權，以將其他工作新增到該工作，或檢查工作或其他工作的狀態。</span><span class="sxs-lookup"><span data-stu-id="972d4-148">For example, a task can request job permissions in order to add other tasks to the job, or check the status of the job or of other tasks.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSAuthenticationTokenSettings
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="972d4-149">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="972d4-149">-BatchContext</span></span>
<span data-ttu-id="972d4-150">指定此 Cmdlet 用來與批次處理服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="972d4-150">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="972d4-151">如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="972d4-151">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="972d4-152">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="972d4-152">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="972d4-153">使用共用金鑰驗證時，預設會使用主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="972d4-153">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="972d4-154">若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。</span><span class="sxs-lookup"><span data-stu-id="972d4-154">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="972d4-155">-CommandLine</span><span class="sxs-lookup"><span data-stu-id="972d4-155">-CommandLine</span></span>
<span data-ttu-id="972d4-156">指定任務的命令列。</span><span class="sxs-lookup"><span data-stu-id="972d4-156">Specifies the command line for the task.</span></span>

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

### <span data-ttu-id="972d4-157">-限制式</span><span class="sxs-lookup"><span data-stu-id="972d4-157">-Constraints</span></span>
<span data-ttu-id="972d4-158">指定適用于此任務的執行限制條件。</span><span class="sxs-lookup"><span data-stu-id="972d4-158">Specifies the execution constraints that apply to this task.</span></span>

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

### <span data-ttu-id="972d4-159">-ContainerSettings</span><span class="sxs-lookup"><span data-stu-id="972d4-159">-ContainerSettings</span></span>
<span data-ttu-id="972d4-160">執行工作之容器的設定。</span><span class="sxs-lookup"><span data-stu-id="972d4-160">The settings for the container under which the task runs.</span></span>
<span data-ttu-id="972d4-161">如果執行這項工作的集區已設定 containerConfiguration，也必須設定此設定。</span><span class="sxs-lookup"><span data-stu-id="972d4-161">If the pool that will run this task has containerConfiguration set, this must be set as well.</span></span> <span data-ttu-id="972d4-162">如果執行這項工作的集區未設定 containerConfiguration，則不得設定此設定。</span><span class="sxs-lookup"><span data-stu-id="972d4-162">If the pool that will run this task doesn't have containerConfiguration set, this must not be set.</span></span> <span data-ttu-id="972d4-163">指定時，節點) 上 Azure Batch 目錄根目錄的 AZ_BATCH_NODE_ROOT_DIR (下方所有目錄會以遞迴方式對應到容器，所有工作環境變數會對應到容器，而任務命令列會于容器中執行。</span><span class="sxs-lookup"><span data-stu-id="972d4-163">When this is specified, all directories recursively below the AZ_BATCH_NODE_ROOT_DIR (the root of Azure Batch directories on the node) are mapped into the container, all task environment variables are mapped into the container, and the task command line is executed in the container.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSTaskContainerSettings
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="972d4-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="972d4-164">-DefaultProfile</span></span>
<span data-ttu-id="972d4-165">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="972d4-165">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="972d4-166">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="972d4-166">-DependsOn</span></span>
<span data-ttu-id="972d4-167">指定任務取決於其他工作。</span><span class="sxs-lookup"><span data-stu-id="972d4-167">Specifies that the task depends on other tasks.</span></span>
<span data-ttu-id="972d4-168">在所有依依的任務都順利完成之前，任務不會排程。</span><span class="sxs-lookup"><span data-stu-id="972d4-168">The task will not be scheduled until all depended-on tasks have completed successfully.</span></span>

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

### <span data-ttu-id="972d4-169">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="972d4-169">-DisplayName</span></span>
<span data-ttu-id="972d4-170">指定任務的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="972d4-170">Specifies the display name of the task.</span></span>

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

### <span data-ttu-id="972d4-171">-EnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="972d4-171">-EnvironmentSettings</span></span>
<span data-ttu-id="972d4-172">指定此 Cmdlet 新增到工作的環境設定，做為金鑰/值組。</span><span class="sxs-lookup"><span data-stu-id="972d4-172">Specifies the environment settings, as key/value pairs, that this cmdlet adds to the task.</span></span>
<span data-ttu-id="972d4-173">關鍵在於環境設定名稱。</span><span class="sxs-lookup"><span data-stu-id="972d4-173">The key is the environment setting name.</span></span>
<span data-ttu-id="972d4-174">值為環境設定。</span><span class="sxs-lookup"><span data-stu-id="972d4-174">The value is the environment setting.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: JobId_Single, JobObject_Single
Aliases: EnvironmentSetting

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="972d4-175">-ExitConditions</span><span class="sxs-lookup"><span data-stu-id="972d4-175">-ExitConditions</span></span>
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

### <span data-ttu-id="972d4-176">-Id</span><span class="sxs-lookup"><span data-stu-id="972d4-176">-Id</span></span>
<span data-ttu-id="972d4-177">指定任務的識別碼。</span><span class="sxs-lookup"><span data-stu-id="972d4-177">Specifies the ID of the task.</span></span>

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

### <span data-ttu-id="972d4-178">-Job</span><span class="sxs-lookup"><span data-stu-id="972d4-178">-Job</span></span>
<span data-ttu-id="972d4-179">指定此 Cmdlet 建立工作的工作。</span><span class="sxs-lookup"><span data-stu-id="972d4-179">Specifies the job under which this cmdlet creates the task.</span></span>
<span data-ttu-id="972d4-180">若要取得 **PSCloudJob 物件** ，請使用 Get-AzBatchJob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="972d4-180">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="972d4-181">-JobId</span><span class="sxs-lookup"><span data-stu-id="972d4-181">-JobId</span></span>
<span data-ttu-id="972d4-182">指定此 Cmdlet 建立工作的工作識別碼。</span><span class="sxs-lookup"><span data-stu-id="972d4-182">Specifies the ID of the job under which this cmdlet creates the task.</span></span>

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

### <span data-ttu-id="972d4-183">-MultiInstanceSettings</span><span class="sxs-lookup"><span data-stu-id="972d4-183">-MultiInstanceSettings</span></span>
<span data-ttu-id="972d4-184">指定如何執行多重實例工作的資訊。</span><span class="sxs-lookup"><span data-stu-id="972d4-184">Specifies information about how to run a multi-instance task.</span></span>

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

### <span data-ttu-id="972d4-185">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="972d4-185">-OutputFile</span></span>
<span data-ttu-id="972d4-186">執行命令列後，可獲取或設定批次處理服務會從計算節點上傳的檔案清單。</span><span class="sxs-lookup"><span data-stu-id="972d4-186">Gets or sets a list of files that the Batch service will upload from the compute node after running the command line.</span></span>
<span data-ttu-id="972d4-187">對於多實例任務，檔案只會從執行主要工作的計算節點上傳。</span><span class="sxs-lookup"><span data-stu-id="972d4-187">For multi-instance tasks, the files will only be uploaded from the compute node on which the primary task is executed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSOutputFile[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="972d4-188">-ResourceFiles</span><span class="sxs-lookup"><span data-stu-id="972d4-188">-ResourceFiles</span></span>
<span data-ttu-id="972d4-189">指定任務所需的資源檔案，做為金鑰/值組。</span><span class="sxs-lookup"><span data-stu-id="972d4-189">Specifies resource files, as key/value pairs, that the task requires.</span></span>
<span data-ttu-id="972d4-190">關鍵在於資源檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="972d4-190">The key is the resource file path.</span></span>
<span data-ttu-id="972d4-191">該值是資源檔案 Blob 來源。</span><span class="sxs-lookup"><span data-stu-id="972d4-191">The value is the resource file blob source.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSResourceFile[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases: ResourceFile

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="972d4-192">-工作</span><span class="sxs-lookup"><span data-stu-id="972d4-192">-Tasks</span></span>
<span data-ttu-id="972d4-193">指定要新增的工作集合。</span><span class="sxs-lookup"><span data-stu-id="972d4-193">Specifies the collection of tasks to be added.</span></span>
<span data-ttu-id="972d4-194">每個任務都必須有唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="972d4-194">Each task must have a unique ID.</span></span>

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

### <span data-ttu-id="972d4-195">-UserIdentity</span><span class="sxs-lookup"><span data-stu-id="972d4-195">-UserIdentity</span></span>
<span data-ttu-id="972d4-196">執行工作的使用者身分識別。</span><span class="sxs-lookup"><span data-stu-id="972d4-196">The user identity under which the task runs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSUserIdentity
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="972d4-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="972d4-197">CommonParameters</span></span>
<span data-ttu-id="972d4-198">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="972d4-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="972d4-199">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="972d4-199">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="972d4-200">輸入</span><span class="sxs-lookup"><span data-stu-id="972d4-200">INPUTS</span></span>

### <span data-ttu-id="972d4-201">Microsoft.Azure.Commands.Batch。Models.PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="972d4-201">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="972d4-202">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="972d4-202">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="972d4-203">輸出</span><span class="sxs-lookup"><span data-stu-id="972d4-203">OUTPUTS</span></span>

### <span data-ttu-id="972d4-204">System.Void</span><span class="sxs-lookup"><span data-stu-id="972d4-204">System.Void</span></span>

## <span data-ttu-id="972d4-205">筆記</span><span class="sxs-lookup"><span data-stu-id="972d4-205">NOTES</span></span>

## <span data-ttu-id="972d4-206">相關連結</span><span class="sxs-lookup"><span data-stu-id="972d4-206">RELATED LINKS</span></span>

[<span data-ttu-id="972d4-207">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="972d4-207">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="972d4-208">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="972d4-208">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="972d4-209">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="972d4-209">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="972d4-210">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="972d4-210">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="972d4-211">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="972d4-211">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="972d4-212">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="972d4-212">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="972d4-213">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="972d4-213">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
