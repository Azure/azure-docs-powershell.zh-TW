---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C71C486E-34EB-42B5-B38A-D85B7DAA2F74
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchPool.md
ms.openlocfilehash: 54a5d6dc737bc0bd6a7f1d236ce855b2a08dca6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457180"
---
# <span data-ttu-id="365ec-101">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="365ec-101">New-AzureBatchPool</span></span>

## <span data-ttu-id="365ec-102">摘要</span><span class="sxs-lookup"><span data-stu-id="365ec-102">SYNOPSIS</span></span>
<span data-ttu-id="365ec-103">在批次服務中建立一個池。</span><span class="sxs-lookup"><span data-stu-id="365ec-103">Creates a pool in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="365ec-104">句法</span><span class="sxs-lookup"><span data-stu-id="365ec-104">SYNTAX</span></span>

### <span data-ttu-id="365ec-105">CloudServiceAndTargetDedicated (預設) </span><span class="sxs-lookup"><span data-stu-id="365ec-105">CloudServiceAndTargetDedicated (Default)</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-ResizeTimeout <TimeSpan>] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
 [-MaxTasksPerComputeNode <Int32>] [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 [-UserAccount <PSUserAccount[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="365ec-106">VirtualMachineAndTargetDedicated</span><span class="sxs-lookup"><span data-stu-id="365ec-106">VirtualMachineAndTargetDedicated</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-ResizeTimeout <TimeSpan>] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
 [-MaxTasksPerComputeNode <Int32>] [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] [-UserAccount <PSUserAccount[]>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="365ec-107">CloudServiceAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="365ec-107">CloudServiceAndAutoScale</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 [-UserAccount <PSUserAccount[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="365ec-108">VirtualMachineAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="365ec-108">VirtualMachineAndAutoScale</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] [-UserAccount <PSUserAccount[]>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="365ec-109">說明</span><span class="sxs-lookup"><span data-stu-id="365ec-109">DESCRIPTION</span></span>
<span data-ttu-id="365ec-110">**新的-AzureBatchPool** Cmdlet 會在 Azure Batch service 中，在由 *BatchCoNtext* 參數指定的帳號下建立一個池。</span><span class="sxs-lookup"><span data-stu-id="365ec-110">The **New-AzureBatchPool** cmdlet creates a pool in the Azure Batch service under the account specified by the *BatchContext* parameter.</span></span>

## <span data-ttu-id="365ec-111">示例</span><span class="sxs-lookup"><span data-stu-id="365ec-111">EXAMPLES</span></span>

### <span data-ttu-id="365ec-112">範例1：使用 TargetDedicated 參數集建立新的 pool</span><span class="sxs-lookup"><span data-stu-id="365ec-112">Example 1: Create a new pool using the TargetDedicated parameter set</span></span>
```
PS C:\>New-AzureBatchPool -Id "MyPool" -VirtualMachineSize "Small" -OSFamily "4" -TargetOSVersion "*" -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

<span data-ttu-id="365ec-113">這個命令會使用 TargetDedicated 參數集來建立 ID 為 MyPool 的新池。</span><span class="sxs-lookup"><span data-stu-id="365ec-113">This command creates a new pool with ID MyPool using the TargetDedicated parameter set.</span></span>
<span data-ttu-id="365ec-114">目標配置為三個計算節點。</span><span class="sxs-lookup"><span data-stu-id="365ec-114">The target allocation is three compute nodes.</span></span>
<span data-ttu-id="365ec-115">該池已設定為使用小型虛擬機器，並以最新的作業系統版本族4進行映射。</span><span class="sxs-lookup"><span data-stu-id="365ec-115">The pool is configured to use small virtual machines imaged with the latest operating system version of family four.</span></span>

### <span data-ttu-id="365ec-116">範例2：使用自動縮放參數集建立新的池</span><span class="sxs-lookup"><span data-stu-id="365ec-116">Example 2: Create a new pool using the AutoScale parameter set</span></span>
```
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -OSFamily "4" -TargetOSVersion "*" -AutoScaleFormula '$TargetDedicated=2;' -BatchContext $Context
```

<span data-ttu-id="365ec-117">這個命令會使用自動縮放參數集來建立 ID 為 AutoScalePool 的新的 pool。</span><span class="sxs-lookup"><span data-stu-id="365ec-117">This command creates a new pool with ID AutoScalePool using the AutoScale parameter set.</span></span>
<span data-ttu-id="365ec-118">該池已設定為使用使用最新作業系統版本的小型虛擬電腦（第四版），而計算節點的目標數是由自動縮放公式決定。</span><span class="sxs-lookup"><span data-stu-id="365ec-118">The pool is configured to use small virtual machines imaged with the latest operating system version of family four, and the target number of compute nodes are determined by the Autoscale formula.</span></span>

### <span data-ttu-id="365ec-119">範例3：建立包含子網上節點的文件庫</span><span class="sxs-lookup"><span data-stu-id="365ec-119">Example 3: Create a pool with nodes in a subnet</span></span>
```
PS C:\>$networkConfig = New-Object Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration
PS C:\>$networkConfig.SubnetId = "/subscriptions/{subscription}/resourceGroups/{group}/providers/{provider}/virtualNetworks/{network}/subnets/{subnet}"
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -OSFamily "4" -TargetDedicatedComputeNodes 3 -NetworkConfiguration $networkConfig -BatchContext $Context
```

### <span data-ttu-id="365ec-120">範例4：使用自訂使用者帳戶建立池</span><span class="sxs-lookup"><span data-stu-id="365ec-120">Example 4: Create a pool with custom user accounts</span></span>
```
PS C:\>$userAccount = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserAccount -ArgumentList @("myaccount", "mypassword")
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -OSFamily "4" -TargetDedicatedComputeNodes 3 -UserAccount $userAccount
```

## <span data-ttu-id="365ec-121">參數</span><span class="sxs-lookup"><span data-stu-id="365ec-121">PARAMETERS</span></span>

### <span data-ttu-id="365ec-122">-ApplicationLicenses</span><span class="sxs-lookup"><span data-stu-id="365ec-122">-ApplicationLicenses</span></span>
<span data-ttu-id="365ec-123">批次服務將可在池中的每個計算節點上使用的應用程式授權清單。</span><span class="sxs-lookup"><span data-stu-id="365ec-123">The list of application licenses the Batch service will make available on each compute node in the pool.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: ApplicationLicense

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365ec-124">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="365ec-124">-ApplicationPackageReferences</span></span>
```yaml
Type: PSApplicationPackageReference[]
Parameter Sets: (All)
Aliases: ApplicationPackageReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365ec-125">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="365ec-125">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="365ec-126">指定根據自動縮放公式自動調整池子大小之前所經過的時間（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="365ec-126">Specifies the amount of time, in minutes, that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="365ec-127">預設值為15分鐘，最小值為5分鐘。</span><span class="sxs-lookup"><span data-stu-id="365ec-127">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: CloudServiceAndAutoScale, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365ec-128">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="365ec-128">-AutoScaleFormula</span></span>
<span data-ttu-id="365ec-129">指定自動縮放池子的公式。</span><span class="sxs-lookup"><span data-stu-id="365ec-129">Specifies the formula for automatically scaling the pool.</span></span>

```yaml
Type: String
Parameter Sets: CloudServiceAndAutoScale, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365ec-130">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="365ec-130">-BatchContext</span></span>
<span data-ttu-id="365ec-131">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="365ec-131">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="365ec-132">如果您使用 Get-AzureRmBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="365ec-132">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="365ec-133">若要改為使用共用金鑰驗證，請使用 Get-AzureRmBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="365ec-133">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="365ec-134">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="365ec-134">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="365ec-135">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="365ec-135">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="365ec-136">-CertificateReferences</span><span class="sxs-lookup"><span data-stu-id="365ec-136">-CertificateReferences</span></span>
<span data-ttu-id="365ec-137">指定與該池相關聯的憑證。</span><span class="sxs-lookup"><span data-stu-id="365ec-137">Specifies certificates associated with the pool.</span></span>
<span data-ttu-id="365ec-138">批次服務會在池的每個計算節點上安裝參照的憑證。</span><span class="sxs-lookup"><span data-stu-id="365ec-138">The Batch service installs the referenced certificates on each compute node of the pool.</span></span>

```yaml
Type: PSCertificateReference[]
Parameter Sets: (All)
Aliases: CertificateReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365ec-139">-CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="365ec-139">-CloudServiceConfiguration</span></span>
<span data-ttu-id="365ec-140">根據 Azure 雲端服務平臺指定池的配置設定。</span><span class="sxs-lookup"><span data-stu-id="365ec-140">Specifies configuration settings for a pool based on the Azure cloud service platform.</span></span>

```yaml
Type: PSCloudServiceConfiguration
Parameter Sets: CloudServiceAndTargetDedicated, CloudServiceAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365ec-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="365ec-141">-DefaultProfile</span></span>
<span data-ttu-id="365ec-142">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="365ec-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="365ec-143">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="365ec-143">-DisplayName</span></span>
<span data-ttu-id="365ec-144">指定該池子的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="365ec-144">Specifies the display name of the pool.</span></span>

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

### <span data-ttu-id="365ec-145">-識別碼</span><span class="sxs-lookup"><span data-stu-id="365ec-145">-Id</span></span>
<span data-ttu-id="365ec-146">指定要建立之池的 ID。</span><span class="sxs-lookup"><span data-stu-id="365ec-146">Specifies the ID of the pool to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365ec-147">-InterComputeNodeCommunicationEnabled</span><span class="sxs-lookup"><span data-stu-id="365ec-147">-InterComputeNodeCommunicationEnabled</span></span>
<span data-ttu-id="365ec-148">表示此 Cmdlet 會為專用計算節點之間的直接通訊設定池。</span><span class="sxs-lookup"><span data-stu-id="365ec-148">Indicates that this cmdlet sets up the pool for direct communication between dedicated compute nodes.</span></span>

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

### <span data-ttu-id="365ec-149">-MaxTasksPerComputeNode</span><span class="sxs-lookup"><span data-stu-id="365ec-149">-MaxTasksPerComputeNode</span></span>
<span data-ttu-id="365ec-150">指定可在單一計算節點上執行的任務數目上限。</span><span class="sxs-lookup"><span data-stu-id="365ec-150">Specifies the maximum number of tasks that can run on a single compute node.</span></span>

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

### <span data-ttu-id="365ec-151">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="365ec-151">-Metadata</span></span>
<span data-ttu-id="365ec-152">指定中繼資料（做為索引鍵/值組），以新增到新的池中。</span><span class="sxs-lookup"><span data-stu-id="365ec-152">Specifies the metadata, as key/value pairs, to add to the new pool.</span></span>
<span data-ttu-id="365ec-153">金鑰就是中繼資料名稱。</span><span class="sxs-lookup"><span data-stu-id="365ec-153">The key is the metadata name.</span></span>
<span data-ttu-id="365ec-154">此值為中繼資料值。</span><span class="sxs-lookup"><span data-stu-id="365ec-154">The value is the metadata value.</span></span>

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

### <span data-ttu-id="365ec-155">-NetworkConfiguration</span><span class="sxs-lookup"><span data-stu-id="365ec-155">-NetworkConfiguration</span></span>
<span data-ttu-id="365ec-156">池的網路設定。</span><span class="sxs-lookup"><span data-stu-id="365ec-156">The network configuration for the pool.</span></span>

```yaml
Type: PSNetworkConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365ec-157">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="365ec-157">-ResizeTimeout</span></span>
<span data-ttu-id="365ec-158">指定將計算節點分配給池中的超時時間。</span><span class="sxs-lookup"><span data-stu-id="365ec-158">Specifies the time-out for allocating compute nodes to the pool.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365ec-159">-StartTask</span><span class="sxs-lookup"><span data-stu-id="365ec-159">-StartTask</span></span>
<span data-ttu-id="365ec-160">指定該池子的開始工作規格。</span><span class="sxs-lookup"><span data-stu-id="365ec-160">Specifies the start task specification for the pool.</span></span>
<span data-ttu-id="365ec-161">當計算節點加入該池，或當您重新開機或 reimaged 時，就會執行 [開始] 任務。</span><span class="sxs-lookup"><span data-stu-id="365ec-161">The start task is run when a compute node joins the pool, or when the compute node is rebooted or reimaged.</span></span>

```yaml
Type: PSStartTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365ec-162">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="365ec-162">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="365ec-163">指定要指派給池中的專用計算節點的目標數目。</span><span class="sxs-lookup"><span data-stu-id="365ec-163">Specifies the target number of dedicated compute nodes to allocate to the pool.</span></span>

```yaml
Type: Int32
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: TargetDedicated

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365ec-164">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="365ec-164">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="365ec-165">指定要分配至池中的低優先順序計算節點的目標數目。</span><span class="sxs-lookup"><span data-stu-id="365ec-165">Specifies the target number of low-priority compute nodes to allocate to the pool.</span></span>

```yaml
Type: Int32
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365ec-166">-TaskSchedulingPolicy</span><span class="sxs-lookup"><span data-stu-id="365ec-166">-TaskSchedulingPolicy</span></span>
<span data-ttu-id="365ec-167">指定任務排程原則，例如 ComputeNodeFillType。</span><span class="sxs-lookup"><span data-stu-id="365ec-167">Specifies the task scheduling policy, such as the ComputeNodeFillType.</span></span>

```yaml
Type: PSTaskSchedulingPolicy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365ec-168">-UserAccount</span><span class="sxs-lookup"><span data-stu-id="365ec-168">-UserAccount</span></span>
<span data-ttu-id="365ec-169">要在池中每個節點上建立的使用者帳戶清單。</span><span class="sxs-lookup"><span data-stu-id="365ec-169">The list of user accounts to be created on each node in the pool.</span></span>

```yaml
Type: PSUserAccount[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365ec-170">-VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="365ec-170">-VirtualMachineConfiguration</span></span>
<span data-ttu-id="365ec-171">指定虛擬機器基礎結構中某個池的設定設定。</span><span class="sxs-lookup"><span data-stu-id="365ec-171">Specifies configuration settings for a pool on the virtual machines infrastructure.</span></span>

```yaml
Type: PSVirtualMachineConfiguration
Parameter Sets: VirtualMachineAndTargetDedicated, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365ec-172">-VirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="365ec-172">-VirtualMachineSize</span></span>
<span data-ttu-id="365ec-173">指定池中虛擬機器的大小。</span><span class="sxs-lookup"><span data-stu-id="365ec-173">Specifies the size of the virtual machines in the pool.</span></span>
<span data-ttu-id="365ec-174">如需虛擬電腦大小的詳細資訊，請參閱 https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) Microsoft Azure 網站中 (的虛擬電腦大小。</span><span class="sxs-lookup"><span data-stu-id="365ec-174">For more information about virtual machine sizes, see Sizes for virtual machineshttps://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ (https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) in the Microsoft Azure site.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365ec-175">-確認</span><span class="sxs-lookup"><span data-stu-id="365ec-175">-Confirm</span></span>
<span data-ttu-id="365ec-176">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="365ec-176">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365ec-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="365ec-177">-WhatIf</span></span>
<span data-ttu-id="365ec-178">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="365ec-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="365ec-179">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="365ec-179">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365ec-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="365ec-180">CommonParameters</span></span>
<span data-ttu-id="365ec-181">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="365ec-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="365ec-182">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="365ec-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="365ec-183">輸入</span><span class="sxs-lookup"><span data-stu-id="365ec-183">INPUTS</span></span>

### <span data-ttu-id="365ec-184">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="365ec-184">BatchAccountContext</span></span>
<span data-ttu-id="365ec-185">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="365ec-185">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="365ec-186">輸出</span><span class="sxs-lookup"><span data-stu-id="365ec-186">OUTPUTS</span></span>

## <span data-ttu-id="365ec-187">筆記</span><span class="sxs-lookup"><span data-stu-id="365ec-187">NOTES</span></span>

## <span data-ttu-id="365ec-188">相關連結</span><span class="sxs-lookup"><span data-stu-id="365ec-188">RELATED LINKS</span></span>

[<span data-ttu-id="365ec-189">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="365ec-189">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="365ec-190">AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="365ec-190">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="365ec-191">移除-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="365ec-191">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="365ec-192">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="365ec-192">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


