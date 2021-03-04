---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: fbdefd7e80e0054bbef8e12614316f7b23ff134a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917770"
---
# <span data-ttu-id="cc32f-101">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cc32f-101">Update-AzVmss</span></span>

## <span data-ttu-id="cc32f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cc32f-102">SYNOPSIS</span></span>
<span data-ttu-id="cc32f-103">更新 VMSS 的狀態。</span><span class="sxs-lookup"><span data-stu-id="cc32f-103">Updates the state of a VMSS.</span></span>

## <span data-ttu-id="cc32f-104">語法</span><span class="sxs-lookup"><span data-stu-id="cc32f-104">SYNTAX</span></span>

### <span data-ttu-id="cc32f-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="cc32f-105">DefaultParameter (Default)</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-AutomaticRepairGracePeriod <String>] [-BootDiagnosticsEnabled <Boolean>]
 [-BootDiagnosticsStorageUri <String>] [-CustomData <String>] [-DisableAutoRollback <Boolean>]
 [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticRepair <Boolean>]
 [-EnableAutomaticUpdate <Boolean>] [-ImageReferenceId <String>] [-ImageReferenceOffer <String>]
 [-ImageReferencePublisher <String>] [-ImageReferenceSku <String>] [-ImageReferenceVersion <String>]
 [-ImageUri <String>] [-LicenseType <String>] [-ManagedDiskStorageAccountType <String>]
 [-MaxBatchInstancePercent <Int32>] [-MaxPrice <Double>] [-MaxUnhealthyInstancePercent <Int32>]
 [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-OsDiskCaching <CachingTypes>]
 [-OsDiskWriteAccelerator <Boolean>] [-Overprovision <Boolean>] [-PauseTimeBetweenBatches <String>]
 [-PlanName <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>] [-PlanPublisher <String>]
 [-ProvisionVMAgent <Boolean>] [-ProximityPlacementGroupId <String>] [-ScaleInPolicy <String[]>]
 [-SinglePlacementGroup <Boolean>] [-SkipExtensionsOnOverprovisionedVMs <Boolean>] [-SkuCapacity <Int32>]
 [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-TerminateScheduledEvents <Boolean>]
 [-TimeZone <String>] [-UltraSSDEnabled <Boolean>] [-UpgradePolicyMode <UpgradeMode>]
 [-VhdContainer <String[]>] [-AsJob] [-EncryptionAtHost <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc32f-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc32f-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-AutomaticRepairGracePeriod <String>] [-BootDiagnosticsEnabled <Boolean>]
 [-BootDiagnosticsStorageUri <String>] [-CustomData <String>] [-DisableAutoRollback <Boolean>]
 [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticRepair <Boolean>]
 [-EnableAutomaticUpdate <Boolean>] [-IdentityId <String[]>] -IdentityType <ResourceIdentityType>
 [-ImageReferenceId <String>] [-ImageReferenceOffer <String>] [-ImageReferencePublisher <String>]
 [-ImageReferenceSku <String>] [-ImageReferenceVersion <String>] [-ImageUri <String>] [-LicenseType <String>]
 [-ManagedDiskStorageAccountType <String>] [-MaxBatchInstancePercent <Int32>] [-MaxPrice <Double>]
 [-MaxUnhealthyInstancePercent <Int32>] [-MaxUnhealthyUpgradedInstancePercent <Int32>]
 [-OsDiskCaching <CachingTypes>] [-OsDiskWriteAccelerator <Boolean>] [-Overprovision <Boolean>]
 [-PauseTimeBetweenBatches <String>] [-PlanName <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>] [-ProximityPlacementGroupId <String>]
 [-ScaleInPolicy <String[]>] [-SinglePlacementGroup <Boolean>] [-SkipExtensionsOnOverprovisionedVMs <Boolean>]
 [-SkuCapacity <Int32>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-TerminateScheduledEvents <Boolean>]
 [-TimeZone <String>] [-UltraSSDEnabled <Boolean>] [-UpgradePolicyMode <UpgradeMode>]
 [-VhdContainer <String[]>] [-AsJob] [-EncryptionAtHost <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc32f-107">描述</span><span class="sxs-lookup"><span data-stu-id="cc32f-107">DESCRIPTION</span></span>
<span data-ttu-id="cc32f-108">**Update-Az Vms Cmdlet** 會更新虛擬機器縮放集 (VMSS) 本機 VMSS 物件的狀態。</span><span class="sxs-lookup"><span data-stu-id="cc32f-108">The **Update-AzVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="cc32f-109">例子</span><span class="sxs-lookup"><span data-stu-id="cc32f-109">EXAMPLES</span></span>

### <span data-ttu-id="cc32f-110">範例 1：將 VMSS 的狀態更新為本地 VMSS 物件的狀態。</span><span class="sxs-lookup"><span data-stu-id="cc32f-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="cc32f-111">此命令會更新名為 VMSS001 的 VMSS 狀態，該狀態屬於名為 Group001 的資源群組，並更新為本地 VMSS 物件的狀態 ，$LocalVMSS。</span><span class="sxs-lookup"><span data-stu-id="cc32f-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="cc32f-112">參數</span><span class="sxs-lookup"><span data-stu-id="cc32f-112">PARAMETERS</span></span>

### <span data-ttu-id="cc32f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cc32f-113">-AsJob</span></span>
<span data-ttu-id="cc32f-114">在背景中執行 Cmdlet 並返回工作以追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="cc32f-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="cc32f-115">-AutomaticOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="cc32f-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="cc32f-116">設定作業系統升級是否應該在較新版本的影像推出時自動套用至縮放集實例。</span><span class="sxs-lookup"><span data-stu-id="cc32f-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc32f-117">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="cc32f-117">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="cc32f-118">由於 VM 上的狀態變更，自動修復暫停的時間量。</span><span class="sxs-lookup"><span data-stu-id="cc32f-118">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="cc32f-119">狀態變更完成之後，寬限期即開始。</span><span class="sxs-lookup"><span data-stu-id="cc32f-119">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="cc32f-120">這有助於避免意外或意外維修。</span><span class="sxs-lookup"><span data-stu-id="cc32f-120">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="cc32f-121">時間長度應該以 ISO 8601 格式指定。</span><span class="sxs-lookup"><span data-stu-id="cc32f-121">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="cc32f-122">PT30M (允許的寬限期) 30 分鐘，這也是預設值。</span><span class="sxs-lookup"><span data-stu-id="cc32f-122">The minimum allowed grace period is 30 minutes (PT30M), which is also the default value.</span></span> <span data-ttu-id="cc32f-123">PT90M 中允許的最大寬限期為 90 (分鐘) 。</span><span class="sxs-lookup"><span data-stu-id="cc32f-123">The maximum allowed grace period is 90 minutes (PT90M).</span></span>

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

### <span data-ttu-id="cc32f-124">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="cc32f-124">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="cc32f-125">是否應該在虛擬機器縮放比例集上啟用開機診斷。</span><span class="sxs-lookup"><span data-stu-id="cc32f-125">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc32f-126">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="cc32f-126">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="cc32f-127">儲存空間帳戶的 URI，用於放置主機輸出和螢幕擷取畫面。</span><span class="sxs-lookup"><span data-stu-id="cc32f-127">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="cc32f-128">-CustomData</span><span class="sxs-lookup"><span data-stu-id="cc32f-128">-CustomData</span></span>
<span data-ttu-id="cc32f-129">指定自訂資料的底數為 64 的編碼字串。</span><span class="sxs-lookup"><span data-stu-id="cc32f-129">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="cc32f-130">這會解碼為二進位陣列，該陣列會儲存為虛擬機器上的檔案。</span><span class="sxs-lookup"><span data-stu-id="cc32f-130">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="cc32f-131">二進位陣列的長度上限為 65535 位元組。</span><span class="sxs-lookup"><span data-stu-id="cc32f-131">The maximum length of the binary array is 65535 bytes.</span></span> <br>
<span data-ttu-id="cc32f-132">若要針對您的 VM 使用雲端 init，請參閱在建立期間使用[雲端 init 自訂 Linux VM。](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="cc32f-132">For using cloud-init for your VM, see [Using cloud-init to customize a Linux VM during creation](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span>

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

### <span data-ttu-id="cc32f-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc32f-133">-DefaultProfile</span></span>
<span data-ttu-id="cc32f-134">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="cc32f-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc32f-135">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="cc32f-135">-DisableAutoRollback</span></span>
<span data-ttu-id="cc32f-136">停用自動作業系統升級策略的自動重回</span><span class="sxs-lookup"><span data-stu-id="cc32f-136">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc32f-137">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="cc32f-137">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="cc32f-138">表示此 Cmdlet 會停用 Linux OS 的密碼驗證。</span><span class="sxs-lookup"><span data-stu-id="cc32f-138">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc32f-139">-EnableAutomaticRepair</span><span class="sxs-lookup"><span data-stu-id="cc32f-139">-EnableAutomaticRepair</span></span>
<span data-ttu-id="cc32f-140">啟用或停用虛擬機器縮放比例集上的自動修復。</span><span class="sxs-lookup"><span data-stu-id="cc32f-140">Enable or disable automatic repairs on the virtual machine scale set.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc32f-141">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="cc32f-141">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="cc32f-142">指出 VMSS 中的 Windows 虛擬機器是否已啟用自動更新。</span><span class="sxs-lookup"><span data-stu-id="cc32f-142">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc32f-143">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="cc32f-143">-EncryptionAtHost</span></span>
<span data-ttu-id="cc32f-144">使用者可以在要求中使用此參數，以啟用或停用虛擬機器縮放集的主機加密。</span><span class="sxs-lookup"><span data-stu-id="cc32f-144">This parameter can be used by user in the request to enable or disable the Host Encryption for the virtual machine scale set.</span></span> 

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc32f-145">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="cc32f-145">-IdentityId</span></span>
<span data-ttu-id="cc32f-146">指定與虛擬機器縮放比例集相關聯的使用者身分設定清單。</span><span class="sxs-lookup"><span data-stu-id="cc32f-146">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="cc32f-147">使用者身分識別參照為表單中的 ARM 資源識別碼：'/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identityies/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="cc32f-147">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc32f-148">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="cc32f-148">-IdentityType</span></span>
<span data-ttu-id="cc32f-149">指定用於虛擬機器縮放集的身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="cc32f-149">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="cc32f-150">"SystemAssignedUserAssigned" 類型包括隱含建立身分識別，以及一組使用者指派的身分識別。</span><span class="sxs-lookup"><span data-stu-id="cc32f-150">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="cc32f-151">類型為 "None" 會從虛擬機器縮放集移除任何身分。</span><span class="sxs-lookup"><span data-stu-id="cc32f-151">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="cc32f-152">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="cc32f-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cc32f-153">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="cc32f-153">SystemAssigned</span></span>
- <span data-ttu-id="cc32f-154">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="cc32f-154">UserAssigned</span></span>
- <span data-ttu-id="cc32f-155">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="cc32f-155">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="cc32f-156">沒有</span><span class="sxs-lookup"><span data-stu-id="cc32f-156">None</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc32f-157">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="cc32f-157">-ImageReferenceId</span></span>
<span data-ttu-id="cc32f-158">指定影像參照識別碼。</span><span class="sxs-lookup"><span data-stu-id="cc32f-158">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="cc32f-159">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="cc32f-159">-ImageReferenceOffer</span></span>
<span data-ttu-id="cc32f-160">指定 VMImage 提供的虛擬機器 (類型) 類型。</span><span class="sxs-lookup"><span data-stu-id="cc32f-160">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="cc32f-161">若要取得影像優惠，請使用 Get-AzVMImageOffer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cc32f-161">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="cc32f-162">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="cc32f-162">-ImageReferencePublisher</span></span>
<span data-ttu-id="cc32f-163">指定 VMImage 的發行者名稱。</span><span class="sxs-lookup"><span data-stu-id="cc32f-163">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="cc32f-164">若要取得發行者，請使用 Get-AzVMImagePublisher Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cc32f-164">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="cc32f-165">-ImageReferenceSKU</span><span class="sxs-lookup"><span data-stu-id="cc32f-165">-ImageReferenceSku</span></span>
<span data-ttu-id="cc32f-166">指定 VMImage SKU。</span><span class="sxs-lookup"><span data-stu-id="cc32f-166">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="cc32f-167">若要取得 SKUS，請使用 Get-AzVMImageSku Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cc32f-167">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="cc32f-168">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="cc32f-168">-ImageReferenceVersion</span></span>
<span data-ttu-id="cc32f-169">指定 VMImage 的版本。</span><span class="sxs-lookup"><span data-stu-id="cc32f-169">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="cc32f-170">若要使用最新版本，請指定最新版本的值，而非特定版本。</span><span class="sxs-lookup"><span data-stu-id="cc32f-170">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="cc32f-171">-ImageUri</span><span class="sxs-lookup"><span data-stu-id="cc32f-171">-ImageUri</span></span>
<span data-ttu-id="cc32f-172">指定使用者圖像的 Blob URI。</span><span class="sxs-lookup"><span data-stu-id="cc32f-172">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="cc32f-173">VMSS 會在同一個使用者映射容器內建立作業系統磁片。</span><span class="sxs-lookup"><span data-stu-id="cc32f-173">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="cc32f-174">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="cc32f-174">-LicenseType</span></span>
<span data-ttu-id="cc32f-175">指定授權類型，用於顯示您自己的授權案例。</span><span class="sxs-lookup"><span data-stu-id="cc32f-175">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="cc32f-176">-Managed在 Managed的StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="cc32f-176">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="cc32f-177">指定受管理磁片的儲存帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="cc32f-177">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="cc32f-178">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="cc32f-178">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cc32f-179">StandardLRS</span><span class="sxs-lookup"><span data-stu-id="cc32f-179">StandardLRS</span></span>
- <span data-ttu-id="cc32f-180">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="cc32f-180">PremiumLRS</span></span>

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

### <span data-ttu-id="cc32f-181">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="cc32f-181">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="cc32f-182">在一個批次中以輪流升級同時升級的虛擬機器實例總數百分比上限。</span><span class="sxs-lookup"><span data-stu-id="cc32f-182">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="cc32f-183">由於這是上限，先前或未來批次中的不健康實例可能會導致批次中實例的百分比降低，以確保較高的可靠性。</span><span class="sxs-lookup"><span data-stu-id="cc32f-183">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="cc32f-184">如果未指定值，則值會設為 20。</span><span class="sxs-lookup"><span data-stu-id="cc32f-184">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="cc32f-185">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="cc32f-185">-MaxPrice</span></span>
<span data-ttu-id="cc32f-186">指定您願意為低優先順序 VM/VMSS 支付的最高價格。</span><span class="sxs-lookup"><span data-stu-id="cc32f-186">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="cc32f-187">此價格為美元。</span><span class="sxs-lookup"><span data-stu-id="cc32f-187">This price is in US Dollars.</span></span> <span data-ttu-id="cc32f-188">此價格會與 VM 大小目前低優先順序價格進行比較。</span><span class="sxs-lookup"><span data-stu-id="cc32f-188">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="cc32f-189">此外，在建立/更新低優先順序 VM/VMSS 時，會比較價格，且只有在 maxPrice 大於目前低優先順序價格時，作業才能成功。</span><span class="sxs-lookup"><span data-stu-id="cc32f-189">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="cc32f-190">如果建立 VM/VMSS 之後，目前的低優先順序價格超出 maxPrice，maxPrice 也會用於評估低優先順序的 VM/VMSS。</span><span class="sxs-lookup"><span data-stu-id="cc32f-190">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="cc32f-191">可能的值為：任何大於零的十進位值。</span><span class="sxs-lookup"><span data-stu-id="cc32f-191">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="cc32f-192">範例：0.01538。</span><span class="sxs-lookup"><span data-stu-id="cc32f-192">Example: 0.01538.</span></span>  <span data-ttu-id="cc32f-193">-1 表示基於價格考慮，不應將低優先順序的 VM/VMSS 從上而退出。</span><span class="sxs-lookup"><span data-stu-id="cc32f-193">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="cc32f-194">此外，如果您未提供，預設最高價格為 -1。</span><span class="sxs-lookup"><span data-stu-id="cc32f-194">Also, the default max price is -1 if it is not provided by you.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc32f-195">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="cc32f-195">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="cc32f-196">縮放集內同時不健康之虛擬機器實例總數的最大百分比，可能是升級的結果，或是由虛擬機器健康情況檢查在輪流升級中止之前發現處於不健康狀態。</span><span class="sxs-lookup"><span data-stu-id="cc32f-196">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="cc32f-197">在開始任何批次之前，將會檢查此限制。</span><span class="sxs-lookup"><span data-stu-id="cc32f-197">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="cc32f-198">如果未指定值，則值會設為 20。</span><span class="sxs-lookup"><span data-stu-id="cc32f-198">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="cc32f-199">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="cc32f-199">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="cc32f-200">可發現處於不健康狀態之升級虛擬機器實例的最大百分比。</span><span class="sxs-lookup"><span data-stu-id="cc32f-200">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="cc32f-201">此檢查將在每個批次升級之後執行。</span><span class="sxs-lookup"><span data-stu-id="cc32f-201">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="cc32f-202">如果超過此百分比，滾動更新會中止。</span><span class="sxs-lookup"><span data-stu-id="cc32f-202">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="cc32f-203">如果未指定值，則值會設為 20。</span><span class="sxs-lookup"><span data-stu-id="cc32f-203">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="cc32f-204">-Os在Caching</span><span class="sxs-lookup"><span data-stu-id="cc32f-204">-OsDiskCaching</span></span>
<span data-ttu-id="cc32f-205">指定作業系統磁片的緩存模式。</span><span class="sxs-lookup"><span data-stu-id="cc32f-205">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="cc32f-206">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="cc32f-206">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cc32f-207">沒有</span><span class="sxs-lookup"><span data-stu-id="cc32f-207">None</span></span>
- <span data-ttu-id="cc32f-208">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="cc32f-208">ReadOnly</span></span>
- <span data-ttu-id="cc32f-209">朗讀預設值為 ReadWrite。</span><span class="sxs-lookup"><span data-stu-id="cc32f-209">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="cc32f-210">如果您變更緩存值，Cmdlet 會重新開機虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="cc32f-210">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="cc32f-211">此設定會影響磁片的一致性與績效。</span><span class="sxs-lookup"><span data-stu-id="cc32f-211">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc32f-212">-OsRiteWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="cc32f-212">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="cc32f-213">指定作業系統磁片上是否應該啟用或停用 WriteAccelerator。</span><span class="sxs-lookup"><span data-stu-id="cc32f-213">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc32f-214">-過度配置</span><span class="sxs-lookup"><span data-stu-id="cc32f-214">-Overprovision</span></span>
<span data-ttu-id="cc32f-215">指出 Cmdlet 是否過度配置 VMSS。</span><span class="sxs-lookup"><span data-stu-id="cc32f-215">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc32f-216">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="cc32f-216">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="cc32f-217">在一個批次中完成所有虛擬機器的更新，到下一個批次開始之間的等待時間。</span><span class="sxs-lookup"><span data-stu-id="cc32f-217">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="cc32f-218">時間長度應該以 ISO 8601 格式指定。</span><span class="sxs-lookup"><span data-stu-id="cc32f-218">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="cc32f-219">預設值為 0 秒 (PT0S) 。</span><span class="sxs-lookup"><span data-stu-id="cc32f-219">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="cc32f-220">-PlanName</span><span class="sxs-lookup"><span data-stu-id="cc32f-220">-PlanName</span></span>
<span data-ttu-id="cc32f-221">指定計劃名稱。</span><span class="sxs-lookup"><span data-stu-id="cc32f-221">Specifies the plan name.</span></span>

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

### <span data-ttu-id="cc32f-222">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="cc32f-222">-PlanProduct</span></span>
<span data-ttu-id="cc32f-223">指定計劃產品。</span><span class="sxs-lookup"><span data-stu-id="cc32f-223">Specifies the plan product.</span></span>

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

### <span data-ttu-id="cc32f-224">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="cc32f-224">-PlanPromotionCode</span></span>
<span data-ttu-id="cc32f-225">指定方案促銷代碼。</span><span class="sxs-lookup"><span data-stu-id="cc32f-225">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="cc32f-226">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="cc32f-226">-PlanPublisher</span></span>
<span data-ttu-id="cc32f-227">指定計劃發行者。</span><span class="sxs-lookup"><span data-stu-id="cc32f-227">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="cc32f-228">-ProvisionMSEVAgent</span><span class="sxs-lookup"><span data-stu-id="cc32f-228">-ProvisionVMAgent</span></span>
<span data-ttu-id="cc32f-229">指出是否應該在 VMSS 的 Windows 虛擬機器上部署虛擬機器代理程式。</span><span class="sxs-lookup"><span data-stu-id="cc32f-229">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc32f-230">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="cc32f-230">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="cc32f-231">要用於此縮放集的鄰近位置群組資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="cc32f-231">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="cc32f-232">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc32f-232">-ResourceGroupName</span></span>
<span data-ttu-id="cc32f-233">指定 VMSS 所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="cc32f-233">Specifies the name of the resource group the VMSS belongs to.</span></span>

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

### <span data-ttu-id="cc32f-234">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="cc32f-234">-ScaleInPolicy</span></span>
<span data-ttu-id="cc32f-235">縮放虛擬機器縮放比例集時要遵循的規則。</span><span class="sxs-lookup"><span data-stu-id="cc32f-235">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="cc32f-236">可能的值為：「Default」、'Oldest%。以及'Newest%。。」</span><span class="sxs-lookup"><span data-stu-id="cc32f-236">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="cc32f-237">當虛擬機器縮放集已調整為比例時，如果這是一個分區比例集，則縮放集會先跨區域進行平衡的預設值。</span><span class="sxs-lookup"><span data-stu-id="cc32f-237">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="cc32f-238">然後，它會盡可能跨錯誤網域進行平衡。</span><span class="sxs-lookup"><span data-stu-id="cc32f-238">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="cc32f-239">在每個錯誤網域中，選擇移除的虛擬機器都是不受縮放保護的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="cc32f-239">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="cc32f-240">當虛擬機器縮放集進行縮放時，會選擇最舊、不受縮放保護的虛擬機器進行移除。</span><span class="sxs-lookup"><span data-stu-id="cc32f-240">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="cc32f-241">對於分區虛擬機器縮放集，縮放集會先跨區域平衡。</span><span class="sxs-lookup"><span data-stu-id="cc32f-241">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="cc32f-242">在每個區域中，會選擇最舊的未受到保護的虛擬機器進行移除。</span><span class="sxs-lookup"><span data-stu-id="cc32f-242">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="cc32f-243">當虛擬機器縮放集進行縮放時，將會選擇不受縮放保護的最新的虛擬機器，以移除最新的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="cc32f-243">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="cc32f-244">對於分區虛擬機器縮放集，縮放集會先跨區域平衡。</span><span class="sxs-lookup"><span data-stu-id="cc32f-244">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="cc32f-245">在每個區域中，系統將會選擇最新的未受到保護的虛擬機器進行移除。</span><span class="sxs-lookup"><span data-stu-id="cc32f-245">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc32f-246">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="cc32f-246">-SinglePlacementGroup</span></span>
<span data-ttu-id="cc32f-247">指定單一位置群組。</span><span class="sxs-lookup"><span data-stu-id="cc32f-247">Specifies the single placement group.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc32f-248">-SkipExtensionsOnOverprovisionedVMS</span><span class="sxs-lookup"><span data-stu-id="cc32f-248">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="cc32f-249">指定擴充功能不會在額外過度配置之虛擬機器上執行。</span><span class="sxs-lookup"><span data-stu-id="cc32f-249">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc32f-250">-Sku以</span><span class="sxs-lookup"><span data-stu-id="cc32f-250">-SkuCapacity</span></span>
<span data-ttu-id="cc32f-251">指定 VMSS 中的實例數目。</span><span class="sxs-lookup"><span data-stu-id="cc32f-251">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="cc32f-252">-SKUName</span><span class="sxs-lookup"><span data-stu-id="cc32f-252">-SkuName</span></span>
<span data-ttu-id="cc32f-253">指定 VMSS 所有實例的大小。</span><span class="sxs-lookup"><span data-stu-id="cc32f-253">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="cc32f-254">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="cc32f-254">-SkuTier</span></span>
<span data-ttu-id="cc32f-255">指定 VMSS 的層級。</span><span class="sxs-lookup"><span data-stu-id="cc32f-255">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="cc32f-256">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="cc32f-256">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cc32f-257">標準</span><span class="sxs-lookup"><span data-stu-id="cc32f-257">Standard</span></span>
- <span data-ttu-id="cc32f-258">基本</span><span class="sxs-lookup"><span data-stu-id="cc32f-258">Basic</span></span>

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

### <span data-ttu-id="cc32f-259">-標記</span><span class="sxs-lookup"><span data-stu-id="cc32f-259">-Tag</span></span>
<span data-ttu-id="cc32f-260">以雜湊表格形式建立索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="cc32f-260">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="cc32f-261">例如：@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="cc32f-261">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc32f-262">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="cc32f-262">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="cc32f-263">刪除的虛擬機器 (分鐘數) 在事件自動核准之前 (終止已排程事件) 。</span><span class="sxs-lookup"><span data-stu-id="cc32f-263">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc32f-264">-終止ScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="cc32f-264">-TerminateScheduledEvents</span></span>
<span data-ttu-id="cc32f-265">指定是否要啟用或停用終止已排程事件。</span><span class="sxs-lookup"><span data-stu-id="cc32f-265">Specifies whether the Terminate Scheduled event is enabled or disabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc32f-266">-時區</span><span class="sxs-lookup"><span data-stu-id="cc32f-266">-TimeZone</span></span>
<span data-ttu-id="cc32f-267">指定 Windows OS 的時區。</span><span class="sxs-lookup"><span data-stu-id="cc32f-267">Specifies the time zone for Windows OS.</span></span> <span data-ttu-id="cc32f-268">例如， \" 太平洋標準時間 \" 。</span><span class="sxs-lookup"><span data-stu-id="cc32f-268">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="cc32f-269">可以從[TimeZoneInfo.GetSystemTimeZones TimeZoneInfo.Id時區取得可能的值](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.getsystemtimezones)。 [](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id)</span><span class="sxs-lookup"><span data-stu-id="cc32f-269">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

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

### <span data-ttu-id="cc32f-270">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="cc32f-270">-UltraSSDEnabled</span></span>
<span data-ttu-id="cc32f-271">可啟用或停用一或多個受管理資料存放區的功能之標UltraSSD_LRS虛擬機器縮放比例集上的儲存空間帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="cc32f-271">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="cc32f-272">只有啟用此屬性時，UltraSSD_LRS儲存帳戶類型的受管理磁片才能新增到 VMSS。</span><span class="sxs-lookup"><span data-stu-id="cc32f-272">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc32f-273">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="cc32f-273">-UpgradePolicyMode</span></span>
<span data-ttu-id="cc32f-274">指定縮放集的虛擬機器升級模式。</span><span class="sxs-lookup"><span data-stu-id="cc32f-274">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="cc32f-275">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="cc32f-275">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cc32f-276">自動</span><span class="sxs-lookup"><span data-stu-id="cc32f-276">Automatic</span></span>
- <span data-ttu-id="cc32f-277">手動</span><span class="sxs-lookup"><span data-stu-id="cc32f-277">Manual</span></span>
- <span data-ttu-id="cc32f-278">滾動</span><span class="sxs-lookup"><span data-stu-id="cc32f-278">Rolling</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.UpgradeMode
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc32f-279">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="cc32f-279">-VhdContainer</span></span>
<span data-ttu-id="cc32f-280">指定用來儲存 VMSS 作業系統磁片的容器 URL。</span><span class="sxs-lookup"><span data-stu-id="cc32f-280">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc32f-281">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="cc32f-281">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="cc32f-282">指定一個本地 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="cc32f-282">Specifies a local VMSS object.</span></span>
<span data-ttu-id="cc32f-283">若要取得 VMSS 物件，請使用 Get-AzVmss Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cc32f-283">To obtain a VMSS object, use the Get-AzVmss cmdlet.</span></span>
<span data-ttu-id="cc32f-284">此虛擬機器物件包含 VMSS 的更新狀態。</span><span class="sxs-lookup"><span data-stu-id="cc32f-284">This virtual machine object contains the updated state for the VMSS.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc32f-285">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="cc32f-285">-VMScaleSetName</span></span>
<span data-ttu-id="cc32f-286">指定此 Cmdlet 所建立之 VMSS 的名稱。</span><span class="sxs-lookup"><span data-stu-id="cc32f-286">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc32f-287">-確認</span><span class="sxs-lookup"><span data-stu-id="cc32f-287">-Confirm</span></span>
<span data-ttu-id="cc32f-288">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="cc32f-288">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc32f-289">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc32f-289">-WhatIf</span></span>
<span data-ttu-id="cc32f-290">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cc32f-290">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc32f-291">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cc32f-291">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc32f-292">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc32f-292">CommonParameters</span></span>
<span data-ttu-id="cc32f-293">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cc32f-293">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc32f-294">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cc32f-294">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc32f-295">輸入</span><span class="sxs-lookup"><span data-stu-id="cc32f-295">INPUTS</span></span>

### <span data-ttu-id="cc32f-296">System.String</span><span class="sxs-lookup"><span data-stu-id="cc32f-296">System.String</span></span>

### <span data-ttu-id="cc32f-297">Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="cc32f-297">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="cc32f-298">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cc32f-298">System.Boolean</span></span>

## <span data-ttu-id="cc32f-299">輸出</span><span class="sxs-lookup"><span data-stu-id="cc32f-299">OUTPUTS</span></span>

### <span data-ttu-id="cc32f-300">Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="cc32f-300">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="cc32f-301">筆記</span><span class="sxs-lookup"><span data-stu-id="cc32f-301">NOTES</span></span>

## <span data-ttu-id="cc32f-302">相關連結</span><span class="sxs-lookup"><span data-stu-id="cc32f-302">RELATED LINKS</span></span>

[<span data-ttu-id="cc32f-303">Get-AzEvss</span><span class="sxs-lookup"><span data-stu-id="cc32f-303">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="cc32f-304">New-AzEvss</span><span class="sxs-lookup"><span data-stu-id="cc32f-304">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="cc32f-305">Remove-AzEvss</span><span class="sxs-lookup"><span data-stu-id="cc32f-305">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="cc32f-306">Restart-AzEvss</span><span class="sxs-lookup"><span data-stu-id="cc32f-306">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="cc32f-307">Set-AzEvss</span><span class="sxs-lookup"><span data-stu-id="cc32f-307">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="cc32f-308">Start-AzEvss</span><span class="sxs-lookup"><span data-stu-id="cc32f-308">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="cc32f-309">Stop-AzEvss</span><span class="sxs-lookup"><span data-stu-id="cc32f-309">Stop-AzVmss</span></span>](./Stop-AzVmss.md)


