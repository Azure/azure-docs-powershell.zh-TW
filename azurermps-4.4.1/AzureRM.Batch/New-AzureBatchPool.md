---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C71C486E-34EB-42B5-B38A-D85B7DAA2F74
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchPool.md
ms.openlocfilehash: 3a9534ea2fd0f1bcfc17f9eb5df63b25f7760f2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450028"
---
# <span data-ttu-id="bd80a-101">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="bd80a-101">New-AzureBatchPool</span></span>

## <span data-ttu-id="bd80a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bd80a-102">SYNOPSIS</span></span>
<span data-ttu-id="bd80a-103">在批次服務中建立一個池。</span><span class="sxs-lookup"><span data-stu-id="bd80a-103">Creates a pool in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd80a-104">句法</span><span class="sxs-lookup"><span data-stu-id="bd80a-104">SYNTAX</span></span>

### <span data-ttu-id="bd80a-105">CloudServiceAndTargetDedicated (預設) </span><span class="sxs-lookup"><span data-stu-id="bd80a-105">CloudServiceAndTargetDedicated (Default)</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-ResizeTimeout <TimeSpan>] [-TargetDedicated <Int32>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bd80a-106">VirtualMachineAndTargetDedicated</span><span class="sxs-lookup"><span data-stu-id="bd80a-106">VirtualMachineAndTargetDedicated</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-ResizeTimeout <TimeSpan>] [-TargetDedicated <Int32>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd80a-107">CloudServiceAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="bd80a-107">CloudServiceAndAutoScale</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bd80a-108">VirtualMachineAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="bd80a-108">VirtualMachineAndAutoScale</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd80a-109">說明</span><span class="sxs-lookup"><span data-stu-id="bd80a-109">DESCRIPTION</span></span>
<span data-ttu-id="bd80a-110">**新的-AzureBatchPool** Cmdlet 會在 Azure Batch service 中，在由 *BatchCoNtext* 參數指定的帳號下建立一個池。</span><span class="sxs-lookup"><span data-stu-id="bd80a-110">The **New-AzureBatchPool** cmdlet creates a pool in the Azure Batch service under the account specified by the *BatchContext* parameter.</span></span>

## <span data-ttu-id="bd80a-111">示例</span><span class="sxs-lookup"><span data-stu-id="bd80a-111">EXAMPLES</span></span>

### <span data-ttu-id="bd80a-112">範例1：使用 TargetDedicated 參數集建立新的 pool</span><span class="sxs-lookup"><span data-stu-id="bd80a-112">Example 1: Create a new pool using the TargetDedicated parameter set</span></span>
```
PS C:\>New-AzureBatchPool -Id "MyPool" -VirtualMachineSize "Small" -OSFamily "4" -TargetOSVersion "*" -TargetDedicated 3 -BatchContext $Context
```

<span data-ttu-id="bd80a-113">這個命令會使用 TargetDedicated 參數集來建立 ID 為 MyPool 的新池。</span><span class="sxs-lookup"><span data-stu-id="bd80a-113">This command creates a new pool with ID MyPool using the TargetDedicated parameter set.</span></span>
<span data-ttu-id="bd80a-114">目標配置為三個計算節點。</span><span class="sxs-lookup"><span data-stu-id="bd80a-114">The target allocation is three compute nodes.</span></span>
<span data-ttu-id="bd80a-115">該池已設定為使用小型虛擬機器，並以最新的作業系統版本族4進行映射。</span><span class="sxs-lookup"><span data-stu-id="bd80a-115">The pool is configured to use small virtual machines imaged with the latest operating system version of family four.</span></span>

### <span data-ttu-id="bd80a-116">範例2：使用自動縮放參數集建立新的池</span><span class="sxs-lookup"><span data-stu-id="bd80a-116">Example 2: Create a new pool using the AutoScale parameter set</span></span>
```
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -OSFamily "4" -TargetOSVersion "*" -AutoScaleFormula '$TargetDedicated=2;' -BatchContext $Context
```

<span data-ttu-id="bd80a-117">這個命令會使用自動縮放參數集來建立 ID 為 AutoScalePool 的新的 pool。</span><span class="sxs-lookup"><span data-stu-id="bd80a-117">This command creates a new pool with ID AutoScalePool using the AutoScale parameter set.</span></span>
<span data-ttu-id="bd80a-118">該池已設定為使用使用最新作業系統版本的小型虛擬電腦（第四版），而計算節點的目標數是由自動縮放公式決定。</span><span class="sxs-lookup"><span data-stu-id="bd80a-118">The pool is configured to use small virtual machines imaged with the latest operating system version of family four, and the target number of compute nodes are determined by the Autoscale formula.</span></span>

## <span data-ttu-id="bd80a-119">參數</span><span class="sxs-lookup"><span data-stu-id="bd80a-119">PARAMETERS</span></span>

### <span data-ttu-id="bd80a-120">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="bd80a-120">-ApplicationPackageReferences</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSApplicationPackageReference[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd80a-121">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="bd80a-121">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="bd80a-122">指定根據自動縮放公式自動調整池子大小之前所經過的時間（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="bd80a-122">Specifies the amount of time, in minutes, that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="bd80a-123">預設值為15分鐘，最小值為5分鐘。</span><span class="sxs-lookup"><span data-stu-id="bd80a-123">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="bd80a-124">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="bd80a-124">-AutoScaleFormula</span></span>
<span data-ttu-id="bd80a-125">指定自動縮放池子的公式。</span><span class="sxs-lookup"><span data-stu-id="bd80a-125">Specifies the formula for automatically scaling the pool.</span></span>

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

### <span data-ttu-id="bd80a-126">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="bd80a-126">-BatchContext</span></span>
<span data-ttu-id="bd80a-127">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="bd80a-127">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="bd80a-128">若要取得包含您訂閱之便捷鍵的 **BatchAccountCoNtext** 物件，請使用 Get-AzureRmBatchAccountKeys Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bd80a-128">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="bd80a-129">-CertificateReferences</span><span class="sxs-lookup"><span data-stu-id="bd80a-129">-CertificateReferences</span></span>
<span data-ttu-id="bd80a-130">指定與該池相關聯的憑證。</span><span class="sxs-lookup"><span data-stu-id="bd80a-130">Specifies certificates associated with the pool.</span></span>
<span data-ttu-id="bd80a-131">批次服務會在池的每個計算節點上安裝參照的憑證。</span><span class="sxs-lookup"><span data-stu-id="bd80a-131">The Batch service installs the referenced certificates on each compute node of the pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCertificateReference[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd80a-132">-CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="bd80a-132">-CloudServiceConfiguration</span></span>
<span data-ttu-id="bd80a-133">根據 Azure 雲端服務平臺指定池的配置設定。</span><span class="sxs-lookup"><span data-stu-id="bd80a-133">Specifies configuration settings for a pool based on the Azure cloud service platform.</span></span>

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

### <span data-ttu-id="bd80a-134">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="bd80a-134">-DisplayName</span></span>
<span data-ttu-id="bd80a-135">指定該池子的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="bd80a-135">Specifies the display name of the pool.</span></span>

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

### <span data-ttu-id="bd80a-136">-識別碼</span><span class="sxs-lookup"><span data-stu-id="bd80a-136">-Id</span></span>
<span data-ttu-id="bd80a-137">指定要建立之池的 ID。</span><span class="sxs-lookup"><span data-stu-id="bd80a-137">Specifies the ID of the pool to create.</span></span>

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

### <span data-ttu-id="bd80a-138">-InterComputeNodeCommunicationEnabled</span><span class="sxs-lookup"><span data-stu-id="bd80a-138">-InterComputeNodeCommunicationEnabled</span></span>
<span data-ttu-id="bd80a-139">表示此 Cmdlet 會為專用計算節點之間的直接通訊設定池。</span><span class="sxs-lookup"><span data-stu-id="bd80a-139">Indicates that this cmdlet sets up the pool for direct communication between dedicated compute nodes.</span></span>

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

### <span data-ttu-id="bd80a-140">-MaxTasksPerComputeNode</span><span class="sxs-lookup"><span data-stu-id="bd80a-140">-MaxTasksPerComputeNode</span></span>
<span data-ttu-id="bd80a-141">指定可在單一計算節點上執行的任務數目上限。</span><span class="sxs-lookup"><span data-stu-id="bd80a-141">Specifies the maximum number of tasks that can run on a single compute node.</span></span>

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

### <span data-ttu-id="bd80a-142">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="bd80a-142">-Metadata</span></span>
<span data-ttu-id="bd80a-143">指定中繼資料（做為索引鍵/值組），以新增到新的池中。</span><span class="sxs-lookup"><span data-stu-id="bd80a-143">Specifies the metadata, as key/value pairs, to add to the new pool.</span></span>
<span data-ttu-id="bd80a-144">金鑰就是中繼資料名稱。</span><span class="sxs-lookup"><span data-stu-id="bd80a-144">The key is the metadata name.</span></span>
<span data-ttu-id="bd80a-145">此值為中繼資料值。</span><span class="sxs-lookup"><span data-stu-id="bd80a-145">The value is the metadata value.</span></span>

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

### <span data-ttu-id="bd80a-146">-NetworkConfiguration</span><span class="sxs-lookup"><span data-stu-id="bd80a-146">-NetworkConfiguration</span></span>
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

### <span data-ttu-id="bd80a-147">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="bd80a-147">-ResizeTimeout</span></span>
<span data-ttu-id="bd80a-148">指定將計算節點分配給池中的超時時間。</span><span class="sxs-lookup"><span data-stu-id="bd80a-148">Specifies the time-out for allocating compute nodes to the pool.</span></span>

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

### <span data-ttu-id="bd80a-149">-StartTask</span><span class="sxs-lookup"><span data-stu-id="bd80a-149">-StartTask</span></span>
<span data-ttu-id="bd80a-150">指定該池子的開始工作規格。</span><span class="sxs-lookup"><span data-stu-id="bd80a-150">Specifies the start task specification for the pool.</span></span>
<span data-ttu-id="bd80a-151">當計算節點加入該池，或當您重新開機或 reimaged 時，就會執行 [開始] 任務。</span><span class="sxs-lookup"><span data-stu-id="bd80a-151">The start task is run when a compute node joins the pool, or when the compute node is rebooted or reimaged.</span></span>

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

### <span data-ttu-id="bd80a-152">-TargetDedicated</span><span class="sxs-lookup"><span data-stu-id="bd80a-152">-TargetDedicated</span></span>
<span data-ttu-id="bd80a-153">指定要分配給池中的計算節點目標數目。</span><span class="sxs-lookup"><span data-stu-id="bd80a-153">Specifies the target number of compute nodes to allocate to the pool.</span></span>

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

### <span data-ttu-id="bd80a-154">-TaskSchedulingPolicy</span><span class="sxs-lookup"><span data-stu-id="bd80a-154">-TaskSchedulingPolicy</span></span>
<span data-ttu-id="bd80a-155">指定任務排程原則，例如 ComputeNodeFillType。</span><span class="sxs-lookup"><span data-stu-id="bd80a-155">Specifies the task scheduling policy, such as the ComputeNodeFillType.</span></span>

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

### <span data-ttu-id="bd80a-156">-VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="bd80a-156">-VirtualMachineConfiguration</span></span>
<span data-ttu-id="bd80a-157">指定虛擬機器基礎結構中某個池的設定設定。</span><span class="sxs-lookup"><span data-stu-id="bd80a-157">Specifies configuration settings for a pool on the virtual machines infrastructure.</span></span>

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

### <span data-ttu-id="bd80a-158">-VirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="bd80a-158">-VirtualMachineSize</span></span>
<span data-ttu-id="bd80a-159">指定池中虛擬機器的大小。</span><span class="sxs-lookup"><span data-stu-id="bd80a-159">Specifies the size of the virtual machines in the pool.</span></span>
<span data-ttu-id="bd80a-160">如需虛擬電腦大小的詳細資訊，請參閱 https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) Microsoft Azure 網站中 (的虛擬電腦大小。</span><span class="sxs-lookup"><span data-stu-id="bd80a-160">For more information about virtual machine sizes, see Sizes for virtual machineshttps://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ (https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) in the Microsoft Azure site.</span></span>

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

### <span data-ttu-id="bd80a-161">-確認</span><span class="sxs-lookup"><span data-stu-id="bd80a-161">-Confirm</span></span>
<span data-ttu-id="bd80a-162">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bd80a-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd80a-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd80a-163">-WhatIf</span></span>
<span data-ttu-id="bd80a-164">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bd80a-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd80a-165">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bd80a-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd80a-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd80a-166">-DefaultProfile</span></span>
<span data-ttu-id="bd80a-167">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bd80a-167">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd80a-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd80a-168">CommonParameters</span></span>
<span data-ttu-id="bd80a-169">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bd80a-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd80a-170">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bd80a-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd80a-171">輸入</span><span class="sxs-lookup"><span data-stu-id="bd80a-171">INPUTS</span></span>

### <span data-ttu-id="bd80a-172">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="bd80a-172">BatchAccountContext</span></span>
<span data-ttu-id="bd80a-173">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="bd80a-173">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="bd80a-174">輸出</span><span class="sxs-lookup"><span data-stu-id="bd80a-174">OUTPUTS</span></span>

## <span data-ttu-id="bd80a-175">筆記</span><span class="sxs-lookup"><span data-stu-id="bd80a-175">NOTES</span></span>

## <span data-ttu-id="bd80a-176">相關連結</span><span class="sxs-lookup"><span data-stu-id="bd80a-176">RELATED LINKS</span></span>

[<span data-ttu-id="bd80a-177">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="bd80a-177">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="bd80a-178">AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="bd80a-178">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="bd80a-179">移除-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="bd80a-179">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="bd80a-180">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="bd80a-180">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


