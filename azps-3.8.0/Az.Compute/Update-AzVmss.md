---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: bf8fa8c4b7d1d08cdb6d0c2c348f5c97a2788a4e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93966033"
---
# <span data-ttu-id="6e99e-101">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6e99e-101">Update-AzVmss</span></span>

## <span data-ttu-id="6e99e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6e99e-102">SYNOPSIS</span></span>
<span data-ttu-id="6e99e-103">更新 VMSS 的狀態。</span><span class="sxs-lookup"><span data-stu-id="6e99e-103">Updates the state of a VMSS.</span></span>

## <span data-ttu-id="6e99e-104">句法</span><span class="sxs-lookup"><span data-stu-id="6e99e-104">SYNTAX</span></span>

### <span data-ttu-id="6e99e-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="6e99e-105">DefaultParameter (Default)</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-AutomaticRepairGracePeriod <String>] [-AutomaticRepairMaxInstanceRepairsPercent <Int32>]
 [-BootDiagnosticsEnabled <Boolean>] [-BootDiagnosticsStorageUri <String>] [-CustomData <String>]
 [-DisableAutoRollback <Boolean>] [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticRepair <Boolean>]
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
 [-VhdContainer <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6e99e-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e99e-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-AutomaticRepairGracePeriod <String>] [-AutomaticRepairMaxInstanceRepairsPercent <Int32>]
 [-BootDiagnosticsEnabled <Boolean>] [-BootDiagnosticsStorageUri <String>] [-CustomData <String>]
 [-DisableAutoRollback <Boolean>] [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticRepair <Boolean>]
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
 [-VhdContainer <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6e99e-107">說明</span><span class="sxs-lookup"><span data-stu-id="6e99e-107">DESCRIPTION</span></span>
<span data-ttu-id="6e99e-108">**更新-AzVmss** Cmdlet 會更新虛擬機器縮放集 (VMSS) 的狀態設定為局部 VMSS 物件的狀態。</span><span class="sxs-lookup"><span data-stu-id="6e99e-108">The **Update-AzVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="6e99e-109">示例</span><span class="sxs-lookup"><span data-stu-id="6e99e-109">EXAMPLES</span></span>

### <span data-ttu-id="6e99e-110">範例1：更新 VMSS 的狀態至本機 VMSS 物件的狀態。</span><span class="sxs-lookup"><span data-stu-id="6e99e-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="6e99e-111">這個命令會將屬於名為 Group001 之資源群組之 VMSS001 的 VMSS 狀態更新為本機 VMSS 物件的狀態，$LocalVMSS。</span><span class="sxs-lookup"><span data-stu-id="6e99e-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="6e99e-112">參數</span><span class="sxs-lookup"><span data-stu-id="6e99e-112">PARAMETERS</span></span>

### <span data-ttu-id="6e99e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6e99e-113">-AsJob</span></span>
<span data-ttu-id="6e99e-114">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="6e99e-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="6e99e-115">-AutomaticOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="6e99e-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="6e99e-116">設定更新版本的影像時，是否應該將作業系統升級自動套用到縮放集實例，以滾動的方式進行。</span><span class="sxs-lookup"><span data-stu-id="6e99e-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="6e99e-117">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="6e99e-117">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="6e99e-118">因 VM 上狀態變更而暫停自動修復的時間長度。</span><span class="sxs-lookup"><span data-stu-id="6e99e-118">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="6e99e-119">當狀態變更完成後，寬限期即會開始。</span><span class="sxs-lookup"><span data-stu-id="6e99e-119">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="6e99e-120">這有助於避免過早或意外的修復。</span><span class="sxs-lookup"><span data-stu-id="6e99e-120">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="6e99e-121">應以 ISO 8601 格式指定持續時間。</span><span class="sxs-lookup"><span data-stu-id="6e99e-121">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="6e99e-122">預設值為5分鐘 (PT5M) 。</span><span class="sxs-lookup"><span data-stu-id="6e99e-122">The default value is 5 minutes (PT5M).</span></span>

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

### <span data-ttu-id="6e99e-123">-AutomaticRepairMaxInstanceRepairsPercent</span><span class="sxs-lookup"><span data-stu-id="6e99e-123">-AutomaticRepairMaxInstanceRepairsPercent</span></span>
<span data-ttu-id="6e99e-124">將同時修復之 scaleset) 的虛擬機器容量 (產能的百分比。</span><span class="sxs-lookup"><span data-stu-id="6e99e-124">The percentage (capacity of scaleset) of virtual machines that will be simultaneously repaired.</span></span> <span data-ttu-id="6e99e-125">預設值為20%。</span><span class="sxs-lookup"><span data-stu-id="6e99e-125">The default value is 20%.</span></span>

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

### <span data-ttu-id="6e99e-126">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="6e99e-126">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="6e99e-127">是否應該在虛擬機器規模集上啟用引導診斷程式。</span><span class="sxs-lookup"><span data-stu-id="6e99e-127">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="6e99e-128">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="6e99e-128">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="6e99e-129">要用來放置主控台輸出和螢幕擷取畫面的儲存空間帳戶 URI。</span><span class="sxs-lookup"><span data-stu-id="6e99e-129">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="6e99e-130">-CustomData</span><span class="sxs-lookup"><span data-stu-id="6e99e-130">-CustomData</span></span>
<span data-ttu-id="6e99e-131">指定自訂資料的基本64編碼字串。</span><span class="sxs-lookup"><span data-stu-id="6e99e-131">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="6e99e-132">這會解碼為二進位陣列，並儲存為虛擬機器上的檔案。</span><span class="sxs-lookup"><span data-stu-id="6e99e-132">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="6e99e-133">二進位陣列的最大長度為65535個位元組。</span><span class="sxs-lookup"><span data-stu-id="6e99e-133">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="6e99e-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e99e-134">-DefaultProfile</span></span>
<span data-ttu-id="6e99e-135">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6e99e-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e99e-136">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="6e99e-136">-DisableAutoRollback</span></span>
<span data-ttu-id="6e99e-137">針對自動 OS 升級原則停用自動復原</span><span class="sxs-lookup"><span data-stu-id="6e99e-137">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="6e99e-138">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="6e99e-138">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="6e99e-139">表示此 Cmdlet 停用 Linux 作業系統的密碼驗證。</span><span class="sxs-lookup"><span data-stu-id="6e99e-139">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

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

### <span data-ttu-id="6e99e-140">-EnableAutomaticRepair</span><span class="sxs-lookup"><span data-stu-id="6e99e-140">-EnableAutomaticRepair</span></span>
<span data-ttu-id="6e99e-141">啟用或停用虛擬機器縮放設定上的自動修復。</span><span class="sxs-lookup"><span data-stu-id="6e99e-141">Enable or disable automatic repairs on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="6e99e-142">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="6e99e-142">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="6e99e-143">指出是否已針對自動更新啟用 VMSS 中的 Windows 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="6e99e-143">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="6e99e-144">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="6e99e-144">-IdentityId</span></span>
<span data-ttu-id="6e99e-145">指定與虛擬機器小性集相關聯的使用者識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="6e99e-145">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="6e99e-146">使用者身分識別參照將是下列形式的 ARM 資源識別碼： '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="6e99e-146">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="6e99e-147">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="6e99e-147">-IdentityType</span></span>
<span data-ttu-id="6e99e-148">指定用於虛擬機器規模集的身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="6e99e-148">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="6e99e-149">"SystemAssignedUserAssigned" 類型包含隱含建立的身分識別，以及一組使用者指派的身分識別。</span><span class="sxs-lookup"><span data-stu-id="6e99e-149">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="6e99e-150">"None" 類型將會移除虛擬機器小單位集中的任何身分識別。</span><span class="sxs-lookup"><span data-stu-id="6e99e-150">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="6e99e-151">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="6e99e-151">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6e99e-152">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="6e99e-152">SystemAssigned</span></span>
- <span data-ttu-id="6e99e-153">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="6e99e-153">UserAssigned</span></span>
- <span data-ttu-id="6e99e-154">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="6e99e-154">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="6e99e-155">所有</span><span class="sxs-lookup"><span data-stu-id="6e99e-155">None</span></span>

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

### <span data-ttu-id="6e99e-156">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="6e99e-156">-ImageReferenceId</span></span>
<span data-ttu-id="6e99e-157">指定影像參照 ID。</span><span class="sxs-lookup"><span data-stu-id="6e99e-157">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="6e99e-158">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="6e99e-158">-ImageReferenceOffer</span></span>
<span data-ttu-id="6e99e-159">指定 (VMImage) 優惠的虛擬機器影像類型。</span><span class="sxs-lookup"><span data-stu-id="6e99e-159">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="6e99e-160">若要取得影像優惠，請使用 Get-AzVMImageOffer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6e99e-160">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="6e99e-161">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="6e99e-161">-ImageReferencePublisher</span></span>
<span data-ttu-id="6e99e-162">指定 VMImage 發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="6e99e-162">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="6e99e-163">若要取得發行者，請使用 Get-AzVMImagePublisher Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6e99e-163">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="6e99e-164">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="6e99e-164">-ImageReferenceSku</span></span>
<span data-ttu-id="6e99e-165">指定 VMImage SKU。</span><span class="sxs-lookup"><span data-stu-id="6e99e-165">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="6e99e-166">若要取得 Sku，請使用 Get-AzVMImageSku Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6e99e-166">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="6e99e-167">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="6e99e-167">-ImageReferenceVersion</span></span>
<span data-ttu-id="6e99e-168">指定 VMImage 的版本。</span><span class="sxs-lookup"><span data-stu-id="6e99e-168">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="6e99e-169">若要使用最新版本，請指定最新的值，而不是特定的版本。</span><span class="sxs-lookup"><span data-stu-id="6e99e-169">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="6e99e-170">-ImageUri</span><span class="sxs-lookup"><span data-stu-id="6e99e-170">-ImageUri</span></span>
<span data-ttu-id="6e99e-171">指定使用者影像的 blob URI。</span><span class="sxs-lookup"><span data-stu-id="6e99e-171">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="6e99e-172">VMSS 會在使用者影像的同一個容器中建立作業系統磁片。</span><span class="sxs-lookup"><span data-stu-id="6e99e-172">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="6e99e-173">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="6e99e-173">-LicenseType</span></span>
<span data-ttu-id="6e99e-174">指定授權類型，這是用來提供您自己的授權案例。</span><span class="sxs-lookup"><span data-stu-id="6e99e-174">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="6e99e-175">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="6e99e-175">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="6e99e-176">指定受管理磁片的儲存帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="6e99e-176">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="6e99e-177">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="6e99e-177">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6e99e-178">StandardLRS</span><span class="sxs-lookup"><span data-stu-id="6e99e-178">StandardLRS</span></span>
- <span data-ttu-id="6e99e-179">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="6e99e-179">PremiumLRS</span></span>

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

### <span data-ttu-id="6e99e-180">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="6e99e-180">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="6e99e-181">輪流升級在一批中同時升級之總虛擬機器實例的最大百分比。</span><span class="sxs-lookup"><span data-stu-id="6e99e-181">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="6e99e-182">如此一來，在前一個或將來的批次中，可能會導致批次中的實例百分比下降，以確保較高的可靠性。</span><span class="sxs-lookup"><span data-stu-id="6e99e-182">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="6e99e-183">如果未指定值，則會將該值設定為20。</span><span class="sxs-lookup"><span data-stu-id="6e99e-183">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="6e99e-184">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="6e99e-184">-MaxPrice</span></span>
<span data-ttu-id="6e99e-185">指定低優先順序 VM/VMSS 要支付的最大價格。</span><span class="sxs-lookup"><span data-stu-id="6e99e-185">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="6e99e-186">這個價格是美元。</span><span class="sxs-lookup"><span data-stu-id="6e99e-186">This price is in US Dollars.</span></span> <span data-ttu-id="6e99e-187">此價格將與 VM 大小的目前低優先順序價格進行比較。</span><span class="sxs-lookup"><span data-stu-id="6e99e-187">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="6e99e-188">此外，價格會在建立/更新低優先順序 VM/VMSS 的時間進行比較，而且只有在 maxPrice 大於目前的低優先順序價格時，作業才會成功。</span><span class="sxs-lookup"><span data-stu-id="6e99e-188">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="6e99e-189">如果在建立 VM/VMSS 之後，目前的低優先順序價格超過 maxPrice，則 maxPrice 也會用於逐出低優先順序 VM/VMSS。</span><span class="sxs-lookup"><span data-stu-id="6e99e-189">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="6e99e-190">可能的值為：任何大於零的十進位值。</span><span class="sxs-lookup"><span data-stu-id="6e99e-190">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="6e99e-191">範例：0.01538。</span><span class="sxs-lookup"><span data-stu-id="6e99e-191">Example: 0.01538.</span></span>  <span data-ttu-id="6e99e-192">-1 表示由於價格原因，不應逐出低優先順序 VM/VMSS。</span><span class="sxs-lookup"><span data-stu-id="6e99e-192">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="6e99e-193">此外，如果您沒有提供預設的最大價格，就是-1。</span><span class="sxs-lookup"><span data-stu-id="6e99e-193">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="6e99e-194">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="6e99e-194">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="6e99e-195">在輪流升級中止前，規模集中可同時進行升級的虛擬機器實例總數，或由虛擬機器健康情況檢查所顯示的總虛擬機器實例的最大百分比。</span><span class="sxs-lookup"><span data-stu-id="6e99e-195">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="6e99e-196">在開始任何批次之前，將會檢查此限制。</span><span class="sxs-lookup"><span data-stu-id="6e99e-196">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="6e99e-197">如果未指定值，則會將該值設定為20。</span><span class="sxs-lookup"><span data-stu-id="6e99e-197">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="6e99e-198">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="6e99e-198">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="6e99e-199">可發現處於不正常狀態之已升級虛擬機器實例的最大百分比。</span><span class="sxs-lookup"><span data-stu-id="6e99e-199">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="6e99e-200">這項檢查會在每個批次升級後發生。</span><span class="sxs-lookup"><span data-stu-id="6e99e-200">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="6e99e-201">如果曾經超過此百分比，則滾動更新會中止。</span><span class="sxs-lookup"><span data-stu-id="6e99e-201">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="6e99e-202">如果未指定值，則會將該值設定為20。</span><span class="sxs-lookup"><span data-stu-id="6e99e-202">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="6e99e-203">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="6e99e-203">-OsDiskCaching</span></span>
<span data-ttu-id="6e99e-204">指定作業系統磁片的快取模式。</span><span class="sxs-lookup"><span data-stu-id="6e99e-204">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="6e99e-205">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="6e99e-205">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6e99e-206">所有</span><span class="sxs-lookup"><span data-stu-id="6e99e-206">None</span></span>
- <span data-ttu-id="6e99e-207">唯讀</span><span class="sxs-lookup"><span data-stu-id="6e99e-207">ReadOnly</span></span>
- <span data-ttu-id="6e99e-208">ReadWrite 的預設值是 ReadWrite。</span><span class="sxs-lookup"><span data-stu-id="6e99e-208">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="6e99e-209">如果您變更快取值，Cmdlet 會重新開機虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="6e99e-209">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="6e99e-210">此設定會影響磁片的一致性和效能。</span><span class="sxs-lookup"><span data-stu-id="6e99e-210">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="6e99e-211">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="6e99e-211">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="6e99e-212">指定是否應該在 OS 磁片上啟用或停用 WriteAccelerator。</span><span class="sxs-lookup"><span data-stu-id="6e99e-212">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="6e99e-213">-Overprovision</span><span class="sxs-lookup"><span data-stu-id="6e99e-213">-Overprovision</span></span>
<span data-ttu-id="6e99e-214">指示 Cmdlet 是否 overprovisions VMSS。</span><span class="sxs-lookup"><span data-stu-id="6e99e-214">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="6e99e-215">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="6e99e-215">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="6e99e-216">在一批中完成所有虛擬機器的更新與開始下一個批次之間的等待時間。</span><span class="sxs-lookup"><span data-stu-id="6e99e-216">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="6e99e-217">應以 ISO 8601 格式指定持續時間。</span><span class="sxs-lookup"><span data-stu-id="6e99e-217">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="6e99e-218">預設值為0秒 (PT0S) 。</span><span class="sxs-lookup"><span data-stu-id="6e99e-218">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="6e99e-219">-PlanName</span><span class="sxs-lookup"><span data-stu-id="6e99e-219">-PlanName</span></span>
<span data-ttu-id="6e99e-220">指定方案名稱。</span><span class="sxs-lookup"><span data-stu-id="6e99e-220">Specifies the plan name.</span></span>

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

### <span data-ttu-id="6e99e-221">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="6e99e-221">-PlanProduct</span></span>
<span data-ttu-id="6e99e-222">指定方案產品。</span><span class="sxs-lookup"><span data-stu-id="6e99e-222">Specifies the plan product.</span></span>

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

### <span data-ttu-id="6e99e-223">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="6e99e-223">-PlanPromotionCode</span></span>
<span data-ttu-id="6e99e-224">指定方案促銷代碼。</span><span class="sxs-lookup"><span data-stu-id="6e99e-224">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="6e99e-225">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="6e99e-225">-PlanPublisher</span></span>
<span data-ttu-id="6e99e-226">指定方案發行者。</span><span class="sxs-lookup"><span data-stu-id="6e99e-226">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="6e99e-227">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="6e99e-227">-ProvisionVMAgent</span></span>
<span data-ttu-id="6e99e-228">指出是否應該在 VMSS 中的 Windows 虛擬機器上預配虛擬機器代理程式。</span><span class="sxs-lookup"><span data-stu-id="6e99e-228">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="6e99e-229">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="6e99e-229">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="6e99e-230">要與此比例集搭配使用之鄰近性位置群組的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="6e99e-230">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="6e99e-231">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e99e-231">-ResourceGroupName</span></span>
<span data-ttu-id="6e99e-232">指定 VMSS 所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6e99e-232">Specifies the name of the resource group the VMSS belongs to.</span></span>

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

### <span data-ttu-id="6e99e-233">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="6e99e-233">-ScaleInPolicy</span></span>
<span data-ttu-id="6e99e-234">在虛擬電腦規模集中進行伸縮時遵循的規則。</span><span class="sxs-lookup"><span data-stu-id="6e99e-234">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="6e99e-235">可能的值為： "Default"、"OldestVM" 和 "NewestVM"。</span><span class="sxs-lookup"><span data-stu-id="6e99e-235">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="6e99e-236">[預設值] 當虛擬電腦縮放比例設定為放大時，如果區域為區域性比例集，則比例集會先平衡在各個區域。</span><span class="sxs-lookup"><span data-stu-id="6e99e-236">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="6e99e-237">接著，它會盡可能在故障網域之間平衡。</span><span class="sxs-lookup"><span data-stu-id="6e99e-237">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="6e99e-238">在每個容錯網域中，選取要移除的虛擬機器將是無法從擴展保護的最新虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="6e99e-238">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="6e99e-239">"OldestVM" 當虛擬電腦縮放比例設定為放大時，系統將不會選擇要移除的最舊虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="6e99e-239">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="6e99e-240">針對 [區塊虛擬電腦] 規模集，比例集將在各個區域之間進行平衡。</span><span class="sxs-lookup"><span data-stu-id="6e99e-240">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="6e99e-241">在每個區域中，將會選取未受保護的舊虛擬機器，以供移除。</span><span class="sxs-lookup"><span data-stu-id="6e99e-241">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="6e99e-242">"NewestVM" 當虛擬電腦縮放比例設定為放大時，系統將不會選取任何不受放大的虛擬機器來進行移除。</span><span class="sxs-lookup"><span data-stu-id="6e99e-242">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="6e99e-243">針對 [區塊虛擬電腦] 規模集，比例集將在各個區域之間進行平衡。</span><span class="sxs-lookup"><span data-stu-id="6e99e-243">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="6e99e-244">在每個區域中，將會選取未受到保護的新虛擬機器電腦來移除。</span><span class="sxs-lookup"><span data-stu-id="6e99e-244">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

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

### <span data-ttu-id="6e99e-245">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="6e99e-245">-SinglePlacementGroup</span></span>
<span data-ttu-id="6e99e-246">指定單一位置群組。</span><span class="sxs-lookup"><span data-stu-id="6e99e-246">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="6e99e-247">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="6e99e-247">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="6e99e-248">指定延伸不會在額外的 overprovisioned Vm 上執行。</span><span class="sxs-lookup"><span data-stu-id="6e99e-248">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="6e99e-249">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="6e99e-249">-SkuCapacity</span></span>
<span data-ttu-id="6e99e-250">指定 VMSS 中的實例數。</span><span class="sxs-lookup"><span data-stu-id="6e99e-250">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="6e99e-251">-SkuName</span><span class="sxs-lookup"><span data-stu-id="6e99e-251">-SkuName</span></span>
<span data-ttu-id="6e99e-252">指定 VMSS 的所有實例大小。</span><span class="sxs-lookup"><span data-stu-id="6e99e-252">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="6e99e-253">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="6e99e-253">-SkuTier</span></span>
<span data-ttu-id="6e99e-254">指定 VMSS 的層級。</span><span class="sxs-lookup"><span data-stu-id="6e99e-254">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="6e99e-255">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="6e99e-255">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6e99e-256">標準</span><span class="sxs-lookup"><span data-stu-id="6e99e-256">Standard</span></span>
- <span data-ttu-id="6e99e-257">空白</span><span class="sxs-lookup"><span data-stu-id="6e99e-257">Basic</span></span>

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

### <span data-ttu-id="6e99e-258">-Tag</span><span class="sxs-lookup"><span data-stu-id="6e99e-258">-Tag</span></span>
<span data-ttu-id="6e99e-259">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="6e99e-259">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6e99e-260">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="6e99e-260">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6e99e-261">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="6e99e-261">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="6e99e-262">已刪除的虛擬機器 (數分鐘內可設定的時間長度) ，必須先核准終止排程事件，然後才能自動核准 (超時) 。</span><span class="sxs-lookup"><span data-stu-id="6e99e-262">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="6e99e-263">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="6e99e-263">-TerminateScheduledEvents</span></span>
<span data-ttu-id="6e99e-264">指定 [終止排程] 事件為 [已啟用] 還是 [停用]。</span><span class="sxs-lookup"><span data-stu-id="6e99e-264">Specifies whether the Terminate Scheduled event is enabled or disabled.</span></span>

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

### <span data-ttu-id="6e99e-265">-時區</span><span class="sxs-lookup"><span data-stu-id="6e99e-265">-TimeZone</span></span>
<span data-ttu-id="6e99e-266">指定 Windows 作業系統的時區。</span><span class="sxs-lookup"><span data-stu-id="6e99e-266">Specifies the time zone for Windows OS.</span></span>

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

### <span data-ttu-id="6e99e-267">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="6e99e-267">-UltraSSDEnabled</span></span>
<span data-ttu-id="6e99e-268">啟用或停用在虛擬機器縮放設定上有一個或多個受管理資料磁片的功能，以及 UltraSSD_LRS 儲存帳戶類型的標誌。</span><span class="sxs-lookup"><span data-stu-id="6e99e-268">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="6e99e-269">只有在啟用此屬性時，才能將儲存帳戶類型 UltraSSD_LRS 的受管理磁片新增至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="6e99e-269">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="6e99e-270">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="6e99e-270">-UpgradePolicyMode</span></span>
<span data-ttu-id="6e99e-271">已指定升級模式至規模集中的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="6e99e-271">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="6e99e-272">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="6e99e-272">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6e99e-273">自動</span><span class="sxs-lookup"><span data-stu-id="6e99e-273">Automatic</span></span>
- <span data-ttu-id="6e99e-274">手動</span><span class="sxs-lookup"><span data-stu-id="6e99e-274">Manual</span></span>
- <span data-ttu-id="6e99e-275">擲</span><span class="sxs-lookup"><span data-stu-id="6e99e-275">Rolling</span></span>

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

### <span data-ttu-id="6e99e-276">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="6e99e-276">-VhdContainer</span></span>
<span data-ttu-id="6e99e-277">指定用來儲存 VMSS 作業系統磁片的容器 Url。</span><span class="sxs-lookup"><span data-stu-id="6e99e-277">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="6e99e-278">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6e99e-278">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="6e99e-279">指定本機 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="6e99e-279">Specifies a local VMSS object.</span></span>
<span data-ttu-id="6e99e-280">若要取得 VMSS 物件，請使用 Get-AzVmss Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6e99e-280">To obtain a VMSS object, use the Get-AzVmss cmdlet.</span></span>
<span data-ttu-id="6e99e-281">此虛擬機器物件包含 VMSS 的更新狀態。</span><span class="sxs-lookup"><span data-stu-id="6e99e-281">This virtual machine object contains the updated state for the VMSS.</span></span>

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

### <span data-ttu-id="6e99e-282">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="6e99e-282">-VMScaleSetName</span></span>
<span data-ttu-id="6e99e-283">指定此 Cmdlet 所建立之 VMSS 的名稱。</span><span class="sxs-lookup"><span data-stu-id="6e99e-283">Specifies the name of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="6e99e-284">-確認</span><span class="sxs-lookup"><span data-stu-id="6e99e-284">-Confirm</span></span>
<span data-ttu-id="6e99e-285">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6e99e-285">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e99e-286">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e99e-286">-WhatIf</span></span>
<span data-ttu-id="6e99e-287">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6e99e-287">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e99e-288">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6e99e-288">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e99e-289">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e99e-289">CommonParameters</span></span>
<span data-ttu-id="6e99e-290">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6e99e-290">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e99e-291">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6e99e-291">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e99e-292">輸入</span><span class="sxs-lookup"><span data-stu-id="6e99e-292">INPUTS</span></span>

### <span data-ttu-id="6e99e-293">System.object</span><span class="sxs-lookup"><span data-stu-id="6e99e-293">System.String</span></span>

### <span data-ttu-id="6e99e-294">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="6e99e-294">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="6e99e-295">System.object</span><span class="sxs-lookup"><span data-stu-id="6e99e-295">System.Boolean</span></span>

## <span data-ttu-id="6e99e-296">輸出</span><span class="sxs-lookup"><span data-stu-id="6e99e-296">OUTPUTS</span></span>

### <span data-ttu-id="6e99e-297">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="6e99e-297">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="6e99e-298">筆記</span><span class="sxs-lookup"><span data-stu-id="6e99e-298">NOTES</span></span>

## <span data-ttu-id="6e99e-299">相關連結</span><span class="sxs-lookup"><span data-stu-id="6e99e-299">RELATED LINKS</span></span>

[<span data-ttu-id="6e99e-300">AzVmss</span><span class="sxs-lookup"><span data-stu-id="6e99e-300">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="6e99e-301">新-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6e99e-301">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="6e99e-302">移除-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6e99e-302">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="6e99e-303">重新開機-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6e99e-303">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="6e99e-304">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6e99e-304">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="6e99e-305">開始-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6e99e-305">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="6e99e-306">停止 AzVmss</span><span class="sxs-lookup"><span data-stu-id="6e99e-306">Stop-AzVmss</span></span>](./Stop-AzVmss.md)


