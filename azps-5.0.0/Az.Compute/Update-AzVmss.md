---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: 4b262b219c479cc2c56311c54d41eb05e2eb866d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284496"
---
# <span data-ttu-id="21711-101">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="21711-101">Update-AzVmss</span></span>

## <span data-ttu-id="21711-102">摘要</span><span class="sxs-lookup"><span data-stu-id="21711-102">SYNOPSIS</span></span>
<span data-ttu-id="21711-103">更新 VMSS 的狀態。</span><span class="sxs-lookup"><span data-stu-id="21711-103">Updates the state of a VMSS.</span></span>

## <span data-ttu-id="21711-104">句法</span><span class="sxs-lookup"><span data-stu-id="21711-104">SYNTAX</span></span>

### <span data-ttu-id="21711-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="21711-105">DefaultParameter (Default)</span></span>
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

### <span data-ttu-id="21711-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="21711-106">ExplicitIdentityParameterSet</span></span>
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

## <span data-ttu-id="21711-107">說明</span><span class="sxs-lookup"><span data-stu-id="21711-107">DESCRIPTION</span></span>
<span data-ttu-id="21711-108">**更新-AzVmss** Cmdlet 會更新虛擬機器縮放集 (VMSS) 的狀態設定為局部 VMSS 物件的狀態。</span><span class="sxs-lookup"><span data-stu-id="21711-108">The **Update-AzVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="21711-109">示例</span><span class="sxs-lookup"><span data-stu-id="21711-109">EXAMPLES</span></span>

### <span data-ttu-id="21711-110">範例1：更新 VMSS 的狀態至本機 VMSS 物件的狀態。</span><span class="sxs-lookup"><span data-stu-id="21711-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="21711-111">這個命令會將屬於名為 Group001 之資源群組之 VMSS001 的 VMSS 狀態更新為本機 VMSS 物件的狀態，$LocalVMSS。</span><span class="sxs-lookup"><span data-stu-id="21711-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="21711-112">參數</span><span class="sxs-lookup"><span data-stu-id="21711-112">PARAMETERS</span></span>

### <span data-ttu-id="21711-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="21711-113">-AsJob</span></span>
<span data-ttu-id="21711-114">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="21711-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="21711-115">-AutomaticOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="21711-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="21711-116">設定更新版本的影像時，是否應該將作業系統升級自動套用到縮放集實例，以滾動的方式進行。</span><span class="sxs-lookup"><span data-stu-id="21711-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="21711-117">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="21711-117">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="21711-118">因 VM 上狀態變更而暫停自動修復的時間長度。</span><span class="sxs-lookup"><span data-stu-id="21711-118">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="21711-119">當狀態變更完成後，寬限期即會開始。</span><span class="sxs-lookup"><span data-stu-id="21711-119">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="21711-120">這有助於避免過早或意外的修復。</span><span class="sxs-lookup"><span data-stu-id="21711-120">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="21711-121">應以 ISO 8601 格式指定持續時間。</span><span class="sxs-lookup"><span data-stu-id="21711-121">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="21711-122">[允許的最小寬限期] 是30分鐘 (PT30M) ，也是預設值。</span><span class="sxs-lookup"><span data-stu-id="21711-122">The minimum allowed grace period is 30 minutes (PT30M), which is also the default value.</span></span> <span data-ttu-id="21711-123">所允許的最大寬限期是90分鐘 (PT90M) 。</span><span class="sxs-lookup"><span data-stu-id="21711-123">The maximum allowed grace period is 90 minutes (PT90M).</span></span>

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

### <span data-ttu-id="21711-124">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="21711-124">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="21711-125">是否應該在虛擬機器規模集上啟用引導診斷程式。</span><span class="sxs-lookup"><span data-stu-id="21711-125">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="21711-126">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="21711-126">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="21711-127">要用來放置主控台輸出和螢幕擷取畫面的儲存空間帳戶 URI。</span><span class="sxs-lookup"><span data-stu-id="21711-127">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="21711-128">-CustomData</span><span class="sxs-lookup"><span data-stu-id="21711-128">-CustomData</span></span>
<span data-ttu-id="21711-129">指定自訂資料的基本64編碼字串。</span><span class="sxs-lookup"><span data-stu-id="21711-129">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="21711-130">這會解碼為二進位陣列，並儲存為虛擬機器上的檔案。</span><span class="sxs-lookup"><span data-stu-id="21711-130">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="21711-131">二進位陣列的最大長度為65535個位元組。</span><span class="sxs-lookup"><span data-stu-id="21711-131">The maximum length of the binary array is 65535 bytes.</span></span> <br>
<span data-ttu-id="21711-132">若要針對您的 VM 使用雲端初始化，請參閱 [在建立期間使用雲端初始化自訂 LINUX VM](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)。</span><span class="sxs-lookup"><span data-stu-id="21711-132">For using cloud-init for your VM, see [Using cloud-init to customize a Linux VM during creation](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span>

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

### <span data-ttu-id="21711-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21711-133">-DefaultProfile</span></span>
<span data-ttu-id="21711-134">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="21711-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21711-135">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="21711-135">-DisableAutoRollback</span></span>
<span data-ttu-id="21711-136">針對自動 OS 升級原則停用自動復原</span><span class="sxs-lookup"><span data-stu-id="21711-136">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="21711-137">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="21711-137">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="21711-138">表示此 Cmdlet 停用 Linux 作業系統的密碼驗證。</span><span class="sxs-lookup"><span data-stu-id="21711-138">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

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

### <span data-ttu-id="21711-139">-EnableAutomaticRepair</span><span class="sxs-lookup"><span data-stu-id="21711-139">-EnableAutomaticRepair</span></span>
<span data-ttu-id="21711-140">啟用或停用虛擬機器縮放設定上的自動修復。</span><span class="sxs-lookup"><span data-stu-id="21711-140">Enable or disable automatic repairs on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="21711-141">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="21711-141">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="21711-142">指出是否已針對自動更新啟用 VMSS 中的 Windows 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="21711-142">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="21711-143">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="21711-143">-EncryptionAtHost</span></span>
<span data-ttu-id="21711-144">使用者可以在要求中使用此參數來啟用或停用虛擬機器縮放集的主機加密。</span><span class="sxs-lookup"><span data-stu-id="21711-144">This parameter can be used by user in the request to enable or disable the Host Encryption for the virtual machine scale set.</span></span> 

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

### <span data-ttu-id="21711-145">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="21711-145">-IdentityId</span></span>
<span data-ttu-id="21711-146">指定與虛擬機器小性集相關聯的使用者識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="21711-146">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="21711-147">使用者身分識別參照將是下列形式的 ARM 資源識別碼： '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="21711-147">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="21711-148">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="21711-148">-IdentityType</span></span>
<span data-ttu-id="21711-149">指定用於虛擬機器規模集的身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="21711-149">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="21711-150">"SystemAssignedUserAssigned" 類型包含隱含建立的身分識別，以及一組使用者指派的身分識別。</span><span class="sxs-lookup"><span data-stu-id="21711-150">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="21711-151">"None" 類型將會移除虛擬機器小單位集中的任何身分識別。</span><span class="sxs-lookup"><span data-stu-id="21711-151">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="21711-152">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="21711-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="21711-153">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="21711-153">SystemAssigned</span></span>
- <span data-ttu-id="21711-154">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="21711-154">UserAssigned</span></span>
- <span data-ttu-id="21711-155">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="21711-155">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="21711-156">所有</span><span class="sxs-lookup"><span data-stu-id="21711-156">None</span></span>

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

### <span data-ttu-id="21711-157">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="21711-157">-ImageReferenceId</span></span>
<span data-ttu-id="21711-158">指定影像參照 ID。</span><span class="sxs-lookup"><span data-stu-id="21711-158">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="21711-159">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="21711-159">-ImageReferenceOffer</span></span>
<span data-ttu-id="21711-160">指定 (VMImage) 優惠的虛擬機器影像類型。</span><span class="sxs-lookup"><span data-stu-id="21711-160">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="21711-161">若要取得影像優惠，請使用 Get-AzVMImageOffer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="21711-161">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="21711-162">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="21711-162">-ImageReferencePublisher</span></span>
<span data-ttu-id="21711-163">指定 VMImage 發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="21711-163">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="21711-164">若要取得發行者，請使用 Get-AzVMImagePublisher Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="21711-164">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="21711-165">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="21711-165">-ImageReferenceSku</span></span>
<span data-ttu-id="21711-166">指定 VMImage SKU。</span><span class="sxs-lookup"><span data-stu-id="21711-166">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="21711-167">若要取得 Sku，請使用 Get-AzVMImageSku Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="21711-167">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="21711-168">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="21711-168">-ImageReferenceVersion</span></span>
<span data-ttu-id="21711-169">指定 VMImage 的版本。</span><span class="sxs-lookup"><span data-stu-id="21711-169">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="21711-170">若要使用最新版本，請指定最新的值，而不是特定的版本。</span><span class="sxs-lookup"><span data-stu-id="21711-170">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="21711-171">-ImageUri</span><span class="sxs-lookup"><span data-stu-id="21711-171">-ImageUri</span></span>
<span data-ttu-id="21711-172">指定使用者影像的 blob URI。</span><span class="sxs-lookup"><span data-stu-id="21711-172">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="21711-173">VMSS 會在使用者影像的同一個容器中建立作業系統磁片。</span><span class="sxs-lookup"><span data-stu-id="21711-173">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="21711-174">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="21711-174">-LicenseType</span></span>
<span data-ttu-id="21711-175">指定授權類型，這是用來提供您自己的授權案例。</span><span class="sxs-lookup"><span data-stu-id="21711-175">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="21711-176">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="21711-176">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="21711-177">指定受管理磁片的儲存帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="21711-177">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="21711-178">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="21711-178">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="21711-179">StandardLRS</span><span class="sxs-lookup"><span data-stu-id="21711-179">StandardLRS</span></span>
- <span data-ttu-id="21711-180">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="21711-180">PremiumLRS</span></span>

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

### <span data-ttu-id="21711-181">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="21711-181">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="21711-182">輪流升級在一批中同時升級之總虛擬機器實例的最大百分比。</span><span class="sxs-lookup"><span data-stu-id="21711-182">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="21711-183">如此一來，在前一個或將來的批次中，可能會導致批次中的實例百分比下降，以確保較高的可靠性。</span><span class="sxs-lookup"><span data-stu-id="21711-183">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="21711-184">如果未指定值，則會將該值設定為20。</span><span class="sxs-lookup"><span data-stu-id="21711-184">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="21711-185">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="21711-185">-MaxPrice</span></span>
<span data-ttu-id="21711-186">指定低優先順序 VM/VMSS 要支付的最大價格。</span><span class="sxs-lookup"><span data-stu-id="21711-186">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="21711-187">這個價格是美元。</span><span class="sxs-lookup"><span data-stu-id="21711-187">This price is in US Dollars.</span></span> <span data-ttu-id="21711-188">此價格將與 VM 大小的目前低優先順序價格進行比較。</span><span class="sxs-lookup"><span data-stu-id="21711-188">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="21711-189">此外，價格會在建立/更新低優先順序 VM/VMSS 的時間進行比較，而且只有在 maxPrice 大於目前的低優先順序價格時，作業才會成功。</span><span class="sxs-lookup"><span data-stu-id="21711-189">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="21711-190">如果在建立 VM/VMSS 之後，目前的低優先順序價格超過 maxPrice，則 maxPrice 也會用於逐出低優先順序 VM/VMSS。</span><span class="sxs-lookup"><span data-stu-id="21711-190">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="21711-191">可能的值為：任何大於零的十進位值。</span><span class="sxs-lookup"><span data-stu-id="21711-191">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="21711-192">範例：0.01538。</span><span class="sxs-lookup"><span data-stu-id="21711-192">Example: 0.01538.</span></span>  <span data-ttu-id="21711-193">-1 表示由於價格原因，不應逐出低優先順序 VM/VMSS。</span><span class="sxs-lookup"><span data-stu-id="21711-193">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="21711-194">此外，如果您沒有提供預設的最大價格，就是-1。</span><span class="sxs-lookup"><span data-stu-id="21711-194">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="21711-195">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="21711-195">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="21711-196">在輪流升級中止前，規模集中可同時進行升級的虛擬機器實例總數，或由虛擬機器健康情況檢查所顯示的總虛擬機器實例的最大百分比。</span><span class="sxs-lookup"><span data-stu-id="21711-196">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="21711-197">在開始任何批次之前，將會檢查此限制。</span><span class="sxs-lookup"><span data-stu-id="21711-197">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="21711-198">如果未指定值，則會將該值設定為20。</span><span class="sxs-lookup"><span data-stu-id="21711-198">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="21711-199">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="21711-199">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="21711-200">可發現處於不正常狀態之已升級虛擬機器實例的最大百分比。</span><span class="sxs-lookup"><span data-stu-id="21711-200">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="21711-201">這項檢查會在每個批次升級後發生。</span><span class="sxs-lookup"><span data-stu-id="21711-201">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="21711-202">如果曾經超過此百分比，則滾動更新會中止。</span><span class="sxs-lookup"><span data-stu-id="21711-202">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="21711-203">如果未指定值，則會將該值設定為20。</span><span class="sxs-lookup"><span data-stu-id="21711-203">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="21711-204">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="21711-204">-OsDiskCaching</span></span>
<span data-ttu-id="21711-205">指定作業系統磁片的快取模式。</span><span class="sxs-lookup"><span data-stu-id="21711-205">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="21711-206">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="21711-206">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="21711-207">所有</span><span class="sxs-lookup"><span data-stu-id="21711-207">None</span></span>
- <span data-ttu-id="21711-208">唯讀</span><span class="sxs-lookup"><span data-stu-id="21711-208">ReadOnly</span></span>
- <span data-ttu-id="21711-209">ReadWrite 的預設值是 ReadWrite。</span><span class="sxs-lookup"><span data-stu-id="21711-209">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="21711-210">如果您變更快取值，Cmdlet 會重新開機虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="21711-210">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="21711-211">此設定會影響磁片的一致性和效能。</span><span class="sxs-lookup"><span data-stu-id="21711-211">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="21711-212">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="21711-212">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="21711-213">指定是否應該在 OS 磁片上啟用或停用 WriteAccelerator。</span><span class="sxs-lookup"><span data-stu-id="21711-213">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="21711-214">-Overprovision</span><span class="sxs-lookup"><span data-stu-id="21711-214">-Overprovision</span></span>
<span data-ttu-id="21711-215">指示 Cmdlet 是否 overprovisions VMSS。</span><span class="sxs-lookup"><span data-stu-id="21711-215">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="21711-216">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="21711-216">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="21711-217">在一批中完成所有虛擬機器的更新與開始下一個批次之間的等待時間。</span><span class="sxs-lookup"><span data-stu-id="21711-217">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="21711-218">應以 ISO 8601 格式指定持續時間。</span><span class="sxs-lookup"><span data-stu-id="21711-218">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="21711-219">預設值為0秒 (PT0S) 。</span><span class="sxs-lookup"><span data-stu-id="21711-219">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="21711-220">-PlanName</span><span class="sxs-lookup"><span data-stu-id="21711-220">-PlanName</span></span>
<span data-ttu-id="21711-221">指定方案名稱。</span><span class="sxs-lookup"><span data-stu-id="21711-221">Specifies the plan name.</span></span>

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

### <span data-ttu-id="21711-222">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="21711-222">-PlanProduct</span></span>
<span data-ttu-id="21711-223">指定方案產品。</span><span class="sxs-lookup"><span data-stu-id="21711-223">Specifies the plan product.</span></span>

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

### <span data-ttu-id="21711-224">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="21711-224">-PlanPromotionCode</span></span>
<span data-ttu-id="21711-225">指定方案促銷代碼。</span><span class="sxs-lookup"><span data-stu-id="21711-225">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="21711-226">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="21711-226">-PlanPublisher</span></span>
<span data-ttu-id="21711-227">指定方案發行者。</span><span class="sxs-lookup"><span data-stu-id="21711-227">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="21711-228">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="21711-228">-ProvisionVMAgent</span></span>
<span data-ttu-id="21711-229">指出是否應該在 VMSS 中的 Windows 虛擬機器上預配虛擬機器代理程式。</span><span class="sxs-lookup"><span data-stu-id="21711-229">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="21711-230">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="21711-230">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="21711-231">要與此比例集搭配使用之鄰近性位置群組的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="21711-231">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="21711-232">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21711-232">-ResourceGroupName</span></span>
<span data-ttu-id="21711-233">指定 VMSS 所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="21711-233">Specifies the name of the resource group the VMSS belongs to.</span></span>

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

### <span data-ttu-id="21711-234">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="21711-234">-ScaleInPolicy</span></span>
<span data-ttu-id="21711-235">在虛擬電腦規模集中進行伸縮時遵循的規則。</span><span class="sxs-lookup"><span data-stu-id="21711-235">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="21711-236">可能的值為： "Default"、"OldestVM" 和 "NewestVM"。</span><span class="sxs-lookup"><span data-stu-id="21711-236">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="21711-237">[預設值] 當虛擬電腦縮放比例設定為放大時，如果區域為區域性比例集，則比例集會先平衡在各個區域。</span><span class="sxs-lookup"><span data-stu-id="21711-237">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="21711-238">接著，它會盡可能在故障網域之間平衡。</span><span class="sxs-lookup"><span data-stu-id="21711-238">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="21711-239">在每個容錯網域中，選取要移除的虛擬機器將是無法從擴展保護的最新虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="21711-239">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="21711-240">"OldestVM" 當虛擬電腦縮放比例設定為放大時，系統將不會選擇要移除的最舊虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="21711-240">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="21711-241">針對 [區塊虛擬電腦] 規模集，比例集將在各個區域之間進行平衡。</span><span class="sxs-lookup"><span data-stu-id="21711-241">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="21711-242">在每個區域中，將會選取未受保護的舊虛擬機器，以供移除。</span><span class="sxs-lookup"><span data-stu-id="21711-242">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="21711-243">"NewestVM" 當虛擬電腦縮放比例設定為放大時，系統將不會選取任何不受放大的虛擬機器來進行移除。</span><span class="sxs-lookup"><span data-stu-id="21711-243">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="21711-244">針對 [區塊虛擬電腦] 規模集，比例集將在各個區域之間進行平衡。</span><span class="sxs-lookup"><span data-stu-id="21711-244">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="21711-245">在每個區域中，將會選取未受到保護的新虛擬機器電腦來移除。</span><span class="sxs-lookup"><span data-stu-id="21711-245">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

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

### <span data-ttu-id="21711-246">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="21711-246">-SinglePlacementGroup</span></span>
<span data-ttu-id="21711-247">指定單一位置群組。</span><span class="sxs-lookup"><span data-stu-id="21711-247">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="21711-248">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="21711-248">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="21711-249">指定延伸不會在額外的 overprovisioned Vm 上執行。</span><span class="sxs-lookup"><span data-stu-id="21711-249">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="21711-250">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="21711-250">-SkuCapacity</span></span>
<span data-ttu-id="21711-251">指定 VMSS 中的實例數。</span><span class="sxs-lookup"><span data-stu-id="21711-251">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="21711-252">-SkuName</span><span class="sxs-lookup"><span data-stu-id="21711-252">-SkuName</span></span>
<span data-ttu-id="21711-253">指定 VMSS 的所有實例大小。</span><span class="sxs-lookup"><span data-stu-id="21711-253">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="21711-254">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="21711-254">-SkuTier</span></span>
<span data-ttu-id="21711-255">指定 VMSS 的層級。</span><span class="sxs-lookup"><span data-stu-id="21711-255">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="21711-256">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="21711-256">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="21711-257">標準</span><span class="sxs-lookup"><span data-stu-id="21711-257">Standard</span></span>
- <span data-ttu-id="21711-258">空白</span><span class="sxs-lookup"><span data-stu-id="21711-258">Basic</span></span>

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

### <span data-ttu-id="21711-259">-Tag</span><span class="sxs-lookup"><span data-stu-id="21711-259">-Tag</span></span>
<span data-ttu-id="21711-260">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="21711-260">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="21711-261">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="21711-261">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="21711-262">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="21711-262">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="21711-263">已刪除的虛擬機器 (數分鐘內可設定的時間長度) ，必須先核准終止排程事件，然後才能自動核准 (超時) 。</span><span class="sxs-lookup"><span data-stu-id="21711-263">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="21711-264">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="21711-264">-TerminateScheduledEvents</span></span>
<span data-ttu-id="21711-265">指定 [終止排程] 事件為 [已啟用] 還是 [停用]。</span><span class="sxs-lookup"><span data-stu-id="21711-265">Specifies whether the Terminate Scheduled event is enabled or disabled.</span></span>

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

### <span data-ttu-id="21711-266">-時區</span><span class="sxs-lookup"><span data-stu-id="21711-266">-TimeZone</span></span>
<span data-ttu-id="21711-267">指定 Windows 作業系統的時區。</span><span class="sxs-lookup"><span data-stu-id="21711-267">Specifies the time zone for Windows OS.</span></span> <span data-ttu-id="21711-268">例如， \" 太平洋標準時間 \" 。</span><span class="sxs-lookup"><span data-stu-id="21711-268">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="21711-269">可能的值可以是 [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) 從 [TimeZoneInfo](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones)傳回的時區值。</span><span class="sxs-lookup"><span data-stu-id="21711-269">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

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

### <span data-ttu-id="21711-270">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="21711-270">-UltraSSDEnabled</span></span>
<span data-ttu-id="21711-271">啟用或停用在虛擬機器縮放設定上有一個或多個受管理資料磁片的功能，以及 UltraSSD_LRS 儲存帳戶類型的標誌。</span><span class="sxs-lookup"><span data-stu-id="21711-271">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="21711-272">只有在啟用此屬性時，才能將儲存帳戶類型 UltraSSD_LRS 的受管理磁片新增至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="21711-272">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="21711-273">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="21711-273">-UpgradePolicyMode</span></span>
<span data-ttu-id="21711-274">已指定升級模式至規模集中的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="21711-274">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="21711-275">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="21711-275">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="21711-276">自動</span><span class="sxs-lookup"><span data-stu-id="21711-276">Automatic</span></span>
- <span data-ttu-id="21711-277">手動</span><span class="sxs-lookup"><span data-stu-id="21711-277">Manual</span></span>
- <span data-ttu-id="21711-278">擲</span><span class="sxs-lookup"><span data-stu-id="21711-278">Rolling</span></span>

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

### <span data-ttu-id="21711-279">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="21711-279">-VhdContainer</span></span>
<span data-ttu-id="21711-280">指定用來儲存 VMSS 作業系統磁片的容器 Url。</span><span class="sxs-lookup"><span data-stu-id="21711-280">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="21711-281">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="21711-281">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="21711-282">指定本機 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="21711-282">Specifies a local VMSS object.</span></span>
<span data-ttu-id="21711-283">若要取得 VMSS 物件，請使用 Get-AzVmss Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="21711-283">To obtain a VMSS object, use the Get-AzVmss cmdlet.</span></span>
<span data-ttu-id="21711-284">此虛擬機器物件包含 VMSS 的更新狀態。</span><span class="sxs-lookup"><span data-stu-id="21711-284">This virtual machine object contains the updated state for the VMSS.</span></span>

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

### <span data-ttu-id="21711-285">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="21711-285">-VMScaleSetName</span></span>
<span data-ttu-id="21711-286">指定此 Cmdlet 所建立之 VMSS 的名稱。</span><span class="sxs-lookup"><span data-stu-id="21711-286">Specifies the name of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="21711-287">-確認</span><span class="sxs-lookup"><span data-stu-id="21711-287">-Confirm</span></span>
<span data-ttu-id="21711-288">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="21711-288">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21711-289">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21711-289">-WhatIf</span></span>
<span data-ttu-id="21711-290">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="21711-290">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21711-291">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="21711-291">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21711-292">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21711-292">CommonParameters</span></span>
<span data-ttu-id="21711-293">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="21711-293">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21711-294">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="21711-294">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21711-295">輸入</span><span class="sxs-lookup"><span data-stu-id="21711-295">INPUTS</span></span>

### <span data-ttu-id="21711-296">System.object</span><span class="sxs-lookup"><span data-stu-id="21711-296">System.String</span></span>

### <span data-ttu-id="21711-297">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="21711-297">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="21711-298">System.object</span><span class="sxs-lookup"><span data-stu-id="21711-298">System.Boolean</span></span>

## <span data-ttu-id="21711-299">輸出</span><span class="sxs-lookup"><span data-stu-id="21711-299">OUTPUTS</span></span>

### <span data-ttu-id="21711-300">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="21711-300">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="21711-301">筆記</span><span class="sxs-lookup"><span data-stu-id="21711-301">NOTES</span></span>

## <span data-ttu-id="21711-302">相關連結</span><span class="sxs-lookup"><span data-stu-id="21711-302">RELATED LINKS</span></span>

[<span data-ttu-id="21711-303">AzVmss</span><span class="sxs-lookup"><span data-stu-id="21711-303">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="21711-304">新-AzVmss</span><span class="sxs-lookup"><span data-stu-id="21711-304">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="21711-305">移除-AzVmss</span><span class="sxs-lookup"><span data-stu-id="21711-305">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="21711-306">重新開機-AzVmss</span><span class="sxs-lookup"><span data-stu-id="21711-306">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="21711-307">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="21711-307">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="21711-308">開始-AzVmss</span><span class="sxs-lookup"><span data-stu-id="21711-308">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="21711-309">停止 AzVmss</span><span class="sxs-lookup"><span data-stu-id="21711-309">Stop-AzVmss</span></span>](./Stop-AzVmss.md)


