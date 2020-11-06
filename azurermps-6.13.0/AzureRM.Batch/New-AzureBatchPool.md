---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C71C486E-34EB-42B5-B38A-D85B7DAA2F74
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchPool.md
ms.openlocfilehash: c401e5b4a85d8c994e96d77f39d646dabb74e02d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447470"
---
# <span data-ttu-id="5bfdc-101">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="5bfdc-101">New-AzureBatchPool</span></span>

## <span data-ttu-id="5bfdc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5bfdc-102">SYNOPSIS</span></span>
<span data-ttu-id="5bfdc-103">在批次服務中建立一個池。</span><span class="sxs-lookup"><span data-stu-id="5bfdc-103">Creates a pool in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5bfdc-104">句法</span><span class="sxs-lookup"><span data-stu-id="5bfdc-104">SYNTAX</span></span>

### <span data-ttu-id="5bfdc-105">CloudServiceAndTargetDedicated (預設) </span><span class="sxs-lookup"><span data-stu-id="5bfdc-105">CloudServiceAndTargetDedicated (Default)</span></span>
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

### <span data-ttu-id="5bfdc-106">VirtualMachineAndTargetDedicated</span><span class="sxs-lookup"><span data-stu-id="5bfdc-106">VirtualMachineAndTargetDedicated</span></span>
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

### <span data-ttu-id="5bfdc-107">CloudServiceAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="5bfdc-107">CloudServiceAndAutoScale</span></span>
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

### <span data-ttu-id="5bfdc-108">VirtualMachineAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="5bfdc-108">VirtualMachineAndAutoScale</span></span>
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

## <span data-ttu-id="5bfdc-109">說明</span><span class="sxs-lookup"><span data-stu-id="5bfdc-109">DESCRIPTION</span></span>
<span data-ttu-id="5bfdc-110">**新的-AzureBatchPool** Cmdlet 會在 Azure Batch service 中，在由 *BatchCoNtext* 參數指定的帳號下建立一個池。</span><span class="sxs-lookup"><span data-stu-id="5bfdc-110">The **New-AzureBatchPool** cmdlet creates a pool in the Azure Batch service under the account specified by the *BatchContext* parameter.</span></span>

## <span data-ttu-id="5bfdc-111">示例</span><span class="sxs-lookup"><span data-stu-id="5bfdc-111">EXAMPLES</span></span>

### <span data-ttu-id="5bfdc-112">範例1：使用 CloudServiceConfiguration 的 TargetDedicated 參數集建立新的池</span><span class="sxs-lookup"><span data-stu-id="5bfdc-112">Example 1: Create a new pool using the TargetDedicated parameter set using CloudServiceConfiguration</span></span>
```
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSCloudServiceConfiguration" -ArgumentList @(4,"*")
PS C:\>New-AzureBatchPool -Id "MyPool" -VirtualMachineSize "Small" -CloudServiceConfiguration $configuration  -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

### <span data-ttu-id="5bfdc-113">範例2：使用 VirtualMachineConfiguration 的 TargetDedicated 參數集建立新的池</span><span class="sxs-lookup"><span data-stu-id="5bfdc-113">Example 2: Create a new pool using the TargetDedicated parameter set using VirtualMachineConfiguration</span></span>
```
PS C:\$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.VirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>New-AzureBatchPool -Id "MyPool" -VirtualMachineSize "Small" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

<span data-ttu-id="5bfdc-114">這個命令會使用 TargetDedicated 參數集來建立 ID 為 MyPool 的新池。</span><span class="sxs-lookup"><span data-stu-id="5bfdc-114">This command creates a new pool with ID MyPool using the TargetDedicated parameter set.</span></span>
<span data-ttu-id="5bfdc-115">目標配置為三個計算節點。</span><span class="sxs-lookup"><span data-stu-id="5bfdc-115">The target allocation is three compute nodes.</span></span>
<span data-ttu-id="5bfdc-116">該池已設定為使用小型虛擬機器，並以最新的作業系統版本族4進行映射。</span><span class="sxs-lookup"><span data-stu-id="5bfdc-116">The pool is configured to use small virtual machines imaged with the latest operating system version of family four.</span></span>

### <span data-ttu-id="5bfdc-117">範例3：使用自動縮放參數集建立新的池</span><span class="sxs-lookup"><span data-stu-id="5bfdc-117">Example 3: Create a new pool using the AutoScale parameter set</span></span>
```
PS C:\$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.VirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -VirtualMachineConfiguration $configuration -AutoScaleFormula '$TargetDedicated=2;' -BatchContext $Context
```

<span data-ttu-id="5bfdc-118">這個命令會使用自動縮放參數集來建立 ID 為 AutoScalePool 的新的 pool。</span><span class="sxs-lookup"><span data-stu-id="5bfdc-118">This command creates a new pool with ID AutoScalePool using the AutoScale parameter set.</span></span>
<span data-ttu-id="5bfdc-119">該池已設定為使用使用最新作業系統版本的小型虛擬電腦（第四版），而計算節點的目標數是由自動縮放公式決定。</span><span class="sxs-lookup"><span data-stu-id="5bfdc-119">The pool is configured to use small virtual machines imaged with the latest operating system version of family four, and the target number of compute nodes are determined by the Autoscale formula.</span></span>

### <span data-ttu-id="5bfdc-120">範例4：建立包含子網上節點的文件庫</span><span class="sxs-lookup"><span data-stu-id="5bfdc-120">Example 4: Create a pool with nodes in a subnet</span></span>
```
PS C:\$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.VirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>$networkConfig = New-Object Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration
PS C:\>$networkConfig.SubnetId = "/subscriptions/{subscription}/resourceGroups/{group}/providers/{provider}/virtualNetworks/{network}/subnets/{subnet}"
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -NetworkConfiguration $networkConfig -BatchContext $Context
```

### <span data-ttu-id="5bfdc-121">範例5：使用自訂使用者帳戶建立池</span><span class="sxs-lookup"><span data-stu-id="5bfdc-121">Example 5: Create a pool with custom user accounts</span></span>
```
PS C:\$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.VirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>$userAccount = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserAccount -ArgumentList @("myaccount", "mypassword")
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -UserAccount $userAccount
```

## <span data-ttu-id="5bfdc-122">參數</span><span class="sxs-lookup"><span data-stu-id="5bfdc-122">PARAMETERS</span></span>

### <span data-ttu-id="5bfdc-123">-ApplicationLicenses</span><span class="sxs-lookup"><span data-stu-id="5bfdc-123">-ApplicationLicenses</span></span>
<span data-ttu-id="5bfdc-124">批次服務將可在池中的每個計算節點上使用的應用程式授權清單。</span><span class="sxs-lookup"><span data-stu-id="5bfdc-124">The list of application licenses the Batch service will make available on each compute node in the pool.</span></span>

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

### <span data-ttu-id="5bfdc-125">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="5bfdc-125">-ApplicationPackageReferences</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSApplicationPackageReference[]
Parameter Sets: (All)
Aliases: ApplicationPackageReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bfdc-126">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="5bfdc-126">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="5bfdc-127">指定根據自動縮放公式自動調整池子大小之前所經過的時間（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="5bfdc-127">Specifies the amount of time, in minutes, that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="5bfdc-128">預設值為15分鐘，最小值為5分鐘。</span><span class="sxs-lookup"><span data-stu-id="5bfdc-128">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: CloudServiceAndAutoScale, VirtualMachineAndAutoScale
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bfdc-129">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="5bfdc-129">-AutoScaleFormula</span></span>
<span data-ttu-id="5bfdc-130">指定自動縮放池子的公式。</span><span class="sxs-lookup"><span data-stu-id="5bfdc-130">Specifies the formula for automatically scaling the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: CloudServiceAndAutoScale, VirtualMachineAndAutoScale
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bfdc-131">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="5bfdc-131">-BatchContext</span></span>
<span data-ttu-id="5bfdc-132">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="5bfdc-132">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5bfdc-133">如果您使用 Get-AzureRmBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="5bfdc-133">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="5bfdc-134">若要改為使用共用金鑰驗證，請使用 Get-AzureRmBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="5bfdc-134">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="5bfdc-135">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="5bfdc-135">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="5bfdc-136">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="5bfdc-136">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="5bfdc-137">-CertificateReferences</span><span class="sxs-lookup"><span data-stu-id="5bfdc-137">-CertificateReferences</span></span>
<span data-ttu-id="5bfdc-138">指定與該池相關聯的憑證。</span><span class="sxs-lookup"><span data-stu-id="5bfdc-138">Specifies certificates associated with the pool.</span></span>
<span data-ttu-id="5bfdc-139">批次服務會在池的每個計算節點上安裝參照的憑證。</span><span class="sxs-lookup"><span data-stu-id="5bfdc-139">The Batch service installs the referenced certificates on each compute node of the pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCertificateReference[]
Parameter Sets: (All)
Aliases: CertificateReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bfdc-140">-CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="5bfdc-140">-CloudServiceConfiguration</span></span>
<span data-ttu-id="5bfdc-141">根據 Azure 雲端服務平臺指定池的配置設定。</span><span class="sxs-lookup"><span data-stu-id="5bfdc-141">Specifies configuration settings for a pool based on the Azure cloud service platform.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudServiceConfiguration
Parameter Sets: CloudServiceAndTargetDedicated, CloudServiceAndAutoScale
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bfdc-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bfdc-142">-DefaultProfile</span></span>
<span data-ttu-id="5bfdc-143">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5bfdc-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5bfdc-144">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5bfdc-144">-DisplayName</span></span>
<span data-ttu-id="5bfdc-145">指定該池子的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="5bfdc-145">Specifies the display name of the pool.</span></span>

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

### <span data-ttu-id="5bfdc-146">-識別碼</span><span class="sxs-lookup"><span data-stu-id="5bfdc-146">-Id</span></span>
<span data-ttu-id="5bfdc-147">指定要建立之池的 ID。</span><span class="sxs-lookup"><span data-stu-id="5bfdc-147">Specifies the ID of the pool to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bfdc-148">-InterComputeNodeCommunicationEnabled</span><span class="sxs-lookup"><span data-stu-id="5bfdc-148">-InterComputeNodeCommunicationEnabled</span></span>
<span data-ttu-id="5bfdc-149">表示此 Cmdlet 會為專用計算節點之間的直接通訊設定池。</span><span class="sxs-lookup"><span data-stu-id="5bfdc-149">Indicates that this cmdlet sets up the pool for direct communication between dedicated compute nodes.</span></span>

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

### <span data-ttu-id="5bfdc-150">-MaxTasksPerComputeNode</span><span class="sxs-lookup"><span data-stu-id="5bfdc-150">-MaxTasksPerComputeNode</span></span>
<span data-ttu-id="5bfdc-151">指定可在單一計算節點上執行的任務數目上限。</span><span class="sxs-lookup"><span data-stu-id="5bfdc-151">Specifies the maximum number of tasks that can run on a single compute node.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bfdc-152">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="5bfdc-152">-Metadata</span></span>
<span data-ttu-id="5bfdc-153">指定中繼資料（做為索引鍵/值組），以新增到新的池中。</span><span class="sxs-lookup"><span data-stu-id="5bfdc-153">Specifies the metadata, as key/value pairs, to add to the new pool.</span></span>
<span data-ttu-id="5bfdc-154">金鑰就是中繼資料名稱。</span><span class="sxs-lookup"><span data-stu-id="5bfdc-154">The key is the metadata name.</span></span>
<span data-ttu-id="5bfdc-155">此值為中繼資料值。</span><span class="sxs-lookup"><span data-stu-id="5bfdc-155">The value is the metadata value.</span></span>

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

### <span data-ttu-id="5bfdc-156">-NetworkConfiguration</span><span class="sxs-lookup"><span data-stu-id="5bfdc-156">-NetworkConfiguration</span></span>
<span data-ttu-id="5bfdc-157">池的網路設定。</span><span class="sxs-lookup"><span data-stu-id="5bfdc-157">The network configuration for the pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bfdc-158">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="5bfdc-158">-ResizeTimeout</span></span>
<span data-ttu-id="5bfdc-159">指定將計算節點分配給池中的超時時間。</span><span class="sxs-lookup"><span data-stu-id="5bfdc-159">Specifies the time-out for allocating compute nodes to the pool.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bfdc-160">-StartTask</span><span class="sxs-lookup"><span data-stu-id="5bfdc-160">-StartTask</span></span>
<span data-ttu-id="5bfdc-161">指定該池子的開始工作規格。</span><span class="sxs-lookup"><span data-stu-id="5bfdc-161">Specifies the start task specification for the pool.</span></span>
<span data-ttu-id="5bfdc-162">當計算節點加入該池，或當您重新開機或 reimaged 時，就會執行 [開始] 任務。</span><span class="sxs-lookup"><span data-stu-id="5bfdc-162">The start task is run when a compute node joins the pool, or when the compute node is rebooted or reimaged.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSStartTask
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bfdc-163">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="5bfdc-163">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="5bfdc-164">指定要指派給池中的專用計算節點的目標數目。</span><span class="sxs-lookup"><span data-stu-id="5bfdc-164">Specifies the target number of dedicated compute nodes to allocate to the pool.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: TargetDedicated

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bfdc-165">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="5bfdc-165">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="5bfdc-166">指定要分配至池中的低優先順序計算節點的目標數目。</span><span class="sxs-lookup"><span data-stu-id="5bfdc-166">Specifies the target number of low-priority compute nodes to allocate to the pool.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bfdc-167">-TaskSchedulingPolicy</span><span class="sxs-lookup"><span data-stu-id="5bfdc-167">-TaskSchedulingPolicy</span></span>
<span data-ttu-id="5bfdc-168">指定任務排程原則，例如 ComputeNodeFillType。</span><span class="sxs-lookup"><span data-stu-id="5bfdc-168">Specifies the task scheduling policy, such as the ComputeNodeFillType.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSTaskSchedulingPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bfdc-169">-UserAccount</span><span class="sxs-lookup"><span data-stu-id="5bfdc-169">-UserAccount</span></span>
<span data-ttu-id="5bfdc-170">要在池中每個節點上建立的使用者帳戶清單。</span><span class="sxs-lookup"><span data-stu-id="5bfdc-170">The list of user accounts to be created on each node in the pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSUserAccount[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bfdc-171">-VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="5bfdc-171">-VirtualMachineConfiguration</span></span>
<span data-ttu-id="5bfdc-172">指定虛擬機器基礎結構中某個池的設定設定。</span><span class="sxs-lookup"><span data-stu-id="5bfdc-172">Specifies configuration settings for a pool on the virtual machines infrastructure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration
Parameter Sets: VirtualMachineAndTargetDedicated, VirtualMachineAndAutoScale
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bfdc-173">-VirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="5bfdc-173">-VirtualMachineSize</span></span>
<span data-ttu-id="5bfdc-174">指定池中虛擬機器的大小。</span><span class="sxs-lookup"><span data-stu-id="5bfdc-174">Specifies the size of the virtual machines in the pool.</span></span>
<span data-ttu-id="5bfdc-175">如需虛擬電腦大小的詳細資訊，請參閱 https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) Microsoft Azure 網站中 (的虛擬電腦大小。</span><span class="sxs-lookup"><span data-stu-id="5bfdc-175">For more information about virtual machine sizes, see Sizes for virtual machineshttps://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ (https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) in the Microsoft Azure site.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bfdc-176">-確認</span><span class="sxs-lookup"><span data-stu-id="5bfdc-176">-Confirm</span></span>
<span data-ttu-id="5bfdc-177">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5bfdc-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bfdc-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bfdc-178">-WhatIf</span></span>
<span data-ttu-id="5bfdc-179">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5bfdc-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bfdc-180">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5bfdc-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bfdc-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bfdc-181">CommonParameters</span></span>
<span data-ttu-id="5bfdc-182">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5bfdc-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bfdc-183">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5bfdc-183">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bfdc-184">輸入</span><span class="sxs-lookup"><span data-stu-id="5bfdc-184">INPUTS</span></span>

### <span data-ttu-id="5bfdc-185">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="5bfdc-185">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="5bfdc-186">參數： BatchCoNtext (ByValue) </span><span class="sxs-lookup"><span data-stu-id="5bfdc-186">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="5bfdc-187">輸出</span><span class="sxs-lookup"><span data-stu-id="5bfdc-187">OUTPUTS</span></span>

### <span data-ttu-id="5bfdc-188">System.void</span><span class="sxs-lookup"><span data-stu-id="5bfdc-188">System.Void</span></span>

## <span data-ttu-id="5bfdc-189">筆記</span><span class="sxs-lookup"><span data-stu-id="5bfdc-189">NOTES</span></span>

## <span data-ttu-id="5bfdc-190">相關連結</span><span class="sxs-lookup"><span data-stu-id="5bfdc-190">RELATED LINKS</span></span>

[<span data-ttu-id="5bfdc-191">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="5bfdc-191">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="5bfdc-192">AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="5bfdc-192">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="5bfdc-193">移除-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="5bfdc-193">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="5bfdc-194">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5bfdc-194">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


