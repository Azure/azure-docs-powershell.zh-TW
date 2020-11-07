---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: 3c22f34b1dc4e01cf4e3ea2f2b3f9c6045197734
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956236"
---
# <span data-ttu-id="5e940-101">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="5e940-101">New-AzVmssConfig</span></span>

## <span data-ttu-id="5e940-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5e940-102">SYNOPSIS</span></span>
<span data-ttu-id="5e940-103">建立 VMSS 設定物件。</span><span class="sxs-lookup"><span data-stu-id="5e940-103">Creates a VMSS configuration object.</span></span>

## <span data-ttu-id="5e940-104">句法</span><span class="sxs-lookup"><span data-stu-id="5e940-104">SYNTAX</span></span>

### <span data-ttu-id="5e940-105">DefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5e940-105">DefaultParameterSet (Default)</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutomaticRepairMaxInstanceRepairsPercent <Int32>] [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>]
 [-EnableUltraSSD] [-HealthProbeId <String>] [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>]
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-TerminateScheduledEvents]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-ProximityPlacementGroupId <String>]
 [-ScaleInPolicy <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5e940-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e940-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutomaticRepairMaxInstanceRepairsPercent <Int32>] [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>]
 [-EnableUltraSSD] [-HealthProbeId <String>] [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>]
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-TerminateScheduledEvents]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-ProximityPlacementGroupId <String>]
 [-ScaleInPolicy <String[]>] -IdentityType <ResourceIdentityType> [-IdentityId <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e940-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e940-107">AssignIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutomaticRepairMaxInstanceRepairsPercent <Int32>] [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>]
 [-EnableUltraSSD] [-HealthProbeId <String>] [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>]
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-TerminateScheduledEvents]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-ProximityPlacementGroupId <String>]
 [-ScaleInPolicy <String[]>] [-AssignIdentity] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5e940-108">說明</span><span class="sxs-lookup"><span data-stu-id="5e940-108">DESCRIPTION</span></span>
<span data-ttu-id="5e940-109">**新的-AzVmssConfig** Cmdlet 會建立可設定的本機視覺管理員縮放比例集， (VMSS) 物件。</span><span class="sxs-lookup"><span data-stu-id="5e940-109">The **New-AzVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="5e940-110">需要其他 Cmdlet 來設定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="5e940-110">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="5e940-111">這些 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="5e940-111">These cmdlets are:</span></span>
- <span data-ttu-id="5e940-112">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="5e940-112">Set-AzVmssOsProfile</span></span>
- <span data-ttu-id="5e940-113">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="5e940-113">Set-AzVmssStorageProfile</span></span>
- <span data-ttu-id="5e940-114">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="5e940-114">Add-AzVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="5e940-115">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="5e940-115">Add-AzVmssExtension</span></span>

## <span data-ttu-id="5e940-116">示例</span><span class="sxs-lookup"><span data-stu-id="5e940-116">EXAMPLES</span></span>

### <span data-ttu-id="5e940-117">範例1：建立 VMSS 設定物件</span><span class="sxs-lookup"><span data-stu-id="5e940-117">Example 1: Create a VMSS configuration object</span></span>
```
PS C:\> $VMSS = New-AzVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic" -NetworkInterfaceConfiguration $NetCfg `
            | Add-AzVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
            | Set-AzVmssOSProfile -ComputerNamePrefix "Test" -AdminUsername $adminUsername -AdminPassword $AdminPassword `
            | Set-AzVmssStorageProfile -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VHDContainer `
            | Add-AzVmssAdditionalUnattendContent -ComponentName  $AUCComponentName -Content  $AUCContent -PassName  $AUCPassName -SettingName  $AUCSetting `
            | Remove-AzVmssAdditionalUnattendContent -ComponentName  $AUCComponentName;

New-AzVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

<span data-ttu-id="5e940-118">這個範例會建立 VMSS 設定物件。</span><span class="sxs-lookup"><span data-stu-id="5e940-118">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="5e940-119">第一個命令使用 **新的 AzVmssConfig** Cmdlet 來建立 VMSS 設定物件，並將結果儲存在名為 $VMSS 的變數中。</span><span class="sxs-lookup"><span data-stu-id="5e940-119">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="5e940-120">第二個命令使用 **AzVmss** Cmdlet 來建立使用在第一個命令中建立之 VMSS 設定物件的 VMSS。</span><span class="sxs-lookup"><span data-stu-id="5e940-120">The second command uses the **New-AzVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="5e940-121">參數</span><span class="sxs-lookup"><span data-stu-id="5e940-121">PARAMETERS</span></span>

### <span data-ttu-id="5e940-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="5e940-122">-AssignIdentity</span></span>
<span data-ttu-id="5e940-123">指定系統指派的虛擬機器縮放集身分識別。</span><span class="sxs-lookup"><span data-stu-id="5e940-123">Specify the system assigned identity for the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e940-124">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="5e940-124">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="5e940-125">因 VM 上狀態變更而暫停自動修復的時間長度。</span><span class="sxs-lookup"><span data-stu-id="5e940-125">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="5e940-126">當狀態變更完成後，寬限期即會開始。</span><span class="sxs-lookup"><span data-stu-id="5e940-126">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="5e940-127">這有助於避免過早或意外的修復。</span><span class="sxs-lookup"><span data-stu-id="5e940-127">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="5e940-128">應以 ISO 8601 格式指定持續時間。</span><span class="sxs-lookup"><span data-stu-id="5e940-128">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="5e940-129">預設值為5分鐘 (PT5M) 。</span><span class="sxs-lookup"><span data-stu-id="5e940-129">The default value is 5 minutes (PT5M).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e940-130">-AutomaticRepairMaxInstanceRepairsPercent</span><span class="sxs-lookup"><span data-stu-id="5e940-130">-AutomaticRepairMaxInstanceRepairsPercent</span></span>
<span data-ttu-id="5e940-131">將同時修復之 scaleset) 的虛擬機器容量 (產能的百分比。</span><span class="sxs-lookup"><span data-stu-id="5e940-131">The percentage (capacity of scaleset) of virtual machines that will be simultaneously repaired.</span></span> <span data-ttu-id="5e940-132">預設值為20%。</span><span class="sxs-lookup"><span data-stu-id="5e940-132">The default value is 20%.</span></span>

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

### <span data-ttu-id="5e940-133">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="5e940-133">-AutoOSUpgrade</span></span>
<span data-ttu-id="5e940-134">設定更新版本的影像時，是否應該將作業系統升級自動套用到縮放集實例，以滾動的方式進行。</span><span class="sxs-lookup"><span data-stu-id="5e940-134">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="5e940-135">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="5e940-135">-BootDiagnostic</span></span>
<span data-ttu-id="5e940-136">指定虛擬機器縮放設定啟動診斷設定檔。</span><span class="sxs-lookup"><span data-stu-id="5e940-136">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.BootDiagnostics
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e940-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e940-137">-DefaultProfile</span></span>
<span data-ttu-id="5e940-138">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5e940-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e940-139">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="5e940-139">-DisableAutoRollback</span></span>
<span data-ttu-id="5e940-140">針對自動 OS 升級原則停用自動復原</span><span class="sxs-lookup"><span data-stu-id="5e940-140">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="5e940-141">-EnableAutomaticRepair</span><span class="sxs-lookup"><span data-stu-id="5e940-141">-EnableAutomaticRepair</span></span>
<span data-ttu-id="5e940-142">在虛擬機器規模集上啟用自動修復。</span><span class="sxs-lookup"><span data-stu-id="5e940-142">Enables automatic repairs on the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e940-143">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="5e940-143">-EnableUltraSSD</span></span>
<span data-ttu-id="5e940-144">可讓一或多個受管理的資料磁片使用一或多個在虛擬機器縮放設定上擁有 UltraSSD_LRS 儲存帳戶類型的功能。</span><span class="sxs-lookup"><span data-stu-id="5e940-144">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="5e940-145">只有在啟用此屬性時，才能將儲存帳戶類型 UltraSSD_LRS 的受管理磁片新增至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="5e940-145">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e940-146">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="5e940-146">-EvictionPolicy</span></span>
<span data-ttu-id="5e940-147">針對規模集中的虛擬機器指定逐出原則。</span><span class="sxs-lookup"><span data-stu-id="5e940-147">Specifies the eviction policy for the virtual machines in the scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e940-148">-延伸</span><span class="sxs-lookup"><span data-stu-id="5e940-148">-Extension</span></span>
<span data-ttu-id="5e940-149">指定 VMSS 的延伸資訊物件。</span><span class="sxs-lookup"><span data-stu-id="5e940-149">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="5e940-150">您可以使用 **AzVmssExtension** Cmdlet 來新增此物件。</span><span class="sxs-lookup"><span data-stu-id="5e940-150">You can use the **Add-AzVmssExtension** cmdlet to add this object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e940-151">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="5e940-151">-HealthProbeId</span></span>
<span data-ttu-id="5e940-152">指定負載平衡器探測的識別碼，這些探測器用來判斷虛擬機器規模集中的實例健康情況。</span><span class="sxs-lookup"><span data-stu-id="5e940-152">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="5e940-153">HealthProbeId 的形式為「/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}」。</span><span class="sxs-lookup"><span data-stu-id="5e940-153">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e940-154">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="5e940-154">-IdentityId</span></span>
<span data-ttu-id="5e940-155">指定與虛擬機器小性集相關聯的使用者識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="5e940-155">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="5e940-156">使用者身分識別參照將是下列形式的 ARM 資源識別碼： '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="5e940-156">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e940-157">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="5e940-157">-IdentityType</span></span>
<span data-ttu-id="5e940-158">指定用於虛擬機器規模集的身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="5e940-158">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="5e940-159">"SystemAssignedUserAssigned" 類型包含隱含建立的身分識別，以及一組使用者指派的身分識別。</span><span class="sxs-lookup"><span data-stu-id="5e940-159">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="5e940-160">"None" 類型將會移除虛擬機器小單位集中的任何身分識別。</span><span class="sxs-lookup"><span data-stu-id="5e940-160">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="5e940-161">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="5e940-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5e940-162">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="5e940-162">SystemAssigned</span></span>
- <span data-ttu-id="5e940-163">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="5e940-163">UserAssigned</span></span>
- <span data-ttu-id="5e940-164">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="5e940-164">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="5e940-165">所有</span><span class="sxs-lookup"><span data-stu-id="5e940-165">None</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e940-166">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="5e940-166">-LicenseType</span></span>
<span data-ttu-id="5e940-167">指定授權類型，這是用來提供您自己的授權案例。</span><span class="sxs-lookup"><span data-stu-id="5e940-167">Specify the license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e940-168">-位置</span><span class="sxs-lookup"><span data-stu-id="5e940-168">-Location</span></span>
<span data-ttu-id="5e940-169">指定建立 VMSS 的 Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="5e940-169">Specifies the Azure location where the VMSS is created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e940-170">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="5e940-170">-MaxPrice</span></span>
<span data-ttu-id="5e940-171">指定低優先順序 VM/VMSS 要支付的最大價格。</span><span class="sxs-lookup"><span data-stu-id="5e940-171">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="5e940-172">這個價格是美元。</span><span class="sxs-lookup"><span data-stu-id="5e940-172">This price is in US Dollars.</span></span> <span data-ttu-id="5e940-173">此價格將與 VM 大小的目前低優先順序價格進行比較。</span><span class="sxs-lookup"><span data-stu-id="5e940-173">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="5e940-174">此外，價格會在建立/更新低優先順序 VM/VMSS 的時間進行比較，而且只有在 maxPrice 大於目前的低優先順序價格時，作業才會成功。</span><span class="sxs-lookup"><span data-stu-id="5e940-174">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="5e940-175">如果在建立 VM/VMSS 之後，目前的低優先順序價格超過 maxPrice，則 maxPrice 也會用於逐出低優先順序 VM/VMSS。</span><span class="sxs-lookup"><span data-stu-id="5e940-175">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="5e940-176">可能的值為：任何大於零的十進位值。</span><span class="sxs-lookup"><span data-stu-id="5e940-176">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="5e940-177">範例：0.01538。</span><span class="sxs-lookup"><span data-stu-id="5e940-177">Example: 0.01538.</span></span>  <span data-ttu-id="5e940-178">-1 表示由於價格原因，不應逐出低優先順序 VM/VMSS。</span><span class="sxs-lookup"><span data-stu-id="5e940-178">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="5e940-179">此外，如果您沒有提供預設的最大價格，就是-1。</span><span class="sxs-lookup"><span data-stu-id="5e940-179">Also, the default max price is -1 if it is not provided by you.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e940-180">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="5e940-180">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="5e940-181">指定包含 VMSS 設定之網路屬性的網路設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="5e940-181">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="5e940-182">您可以使用 **AzVmssNetworkInterfaceConfiguration** Cmdlet 來新增此物件。</span><span class="sxs-lookup"><span data-stu-id="5e940-182">You can use the **Add-AzVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e940-183">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="5e940-183">-OsProfile</span></span>
<span data-ttu-id="5e940-184">指定作業系統設定檔物件，其中包含 VMSS 設定的作業系統屬性。</span><span class="sxs-lookup"><span data-stu-id="5e940-184">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="5e940-185">您可以使用 **AzVmssOsProfile** Cmdlet 來設定此物件。</span><span class="sxs-lookup"><span data-stu-id="5e940-185">You can use the **Set-AzVmssOsProfile** cmdlet to set this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e940-186">-Overprovision</span><span class="sxs-lookup"><span data-stu-id="5e940-186">-Overprovision</span></span>
<span data-ttu-id="5e940-187">指示 Cmdlet 是否 overprovisions VMSS。</span><span class="sxs-lookup"><span data-stu-id="5e940-187">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e940-188">-PlanName</span><span class="sxs-lookup"><span data-stu-id="5e940-188">-PlanName</span></span>
<span data-ttu-id="5e940-189">指定方案名稱。</span><span class="sxs-lookup"><span data-stu-id="5e940-189">Specifies the plan name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e940-190">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="5e940-190">-PlanProduct</span></span>
<span data-ttu-id="5e940-191">指定方案產品。</span><span class="sxs-lookup"><span data-stu-id="5e940-191">Specifies the plan product.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e940-192">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="5e940-192">-PlanPromotionCode</span></span>
<span data-ttu-id="5e940-193">指定方案促銷代碼。</span><span class="sxs-lookup"><span data-stu-id="5e940-193">Specifies the plan promotion code.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e940-194">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="5e940-194">-PlanPublisher</span></span>
<span data-ttu-id="5e940-195">指定方案發行者。</span><span class="sxs-lookup"><span data-stu-id="5e940-195">Specifies the plan publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e940-196">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="5e940-196">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="5e940-197">每個位置群組的錯誤網域計數。</span><span class="sxs-lookup"><span data-stu-id="5e940-197">Fault Domain count for each placement group.</span></span>

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

### <span data-ttu-id="5e940-198">-優先順序</span><span class="sxs-lookup"><span data-stu-id="5e940-198">-Priority</span></span>
<span data-ttu-id="5e940-199">規模集中虛擬 machien 的優先順序。</span><span class="sxs-lookup"><span data-stu-id="5e940-199">The priority for the virtual machien in the scale set.</span></span>  <span data-ttu-id="5e940-200">僅支援的值為 "Regular"、"點" 和 "低"。</span><span class="sxs-lookup"><span data-stu-id="5e940-200">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="5e940-201">"Regular" 是適用于一般虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="5e940-201">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="5e940-202">「點」是用於找出虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="5e940-202">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="5e940-203">「低」也適用于 [專色虛擬機器]，但會以「點」取代。</span><span class="sxs-lookup"><span data-stu-id="5e940-203">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="5e940-204">請使用「污點」，而不是「低」。</span><span class="sxs-lookup"><span data-stu-id="5e940-204">Please use 'Spot' instead of 'Low'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e940-205">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="5e940-205">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="5e940-206">要與此比例集搭配使用之鄰近性位置群組的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="5e940-206">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e940-207">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="5e940-207">-RollingUpgradePolicy</span></span>
<span data-ttu-id="5e940-208">指定輪流升級原則。</span><span class="sxs-lookup"><span data-stu-id="5e940-208">Specifies the rolling upgrade policy.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e940-209">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="5e940-209">-ScaleInPolicy</span></span>
<span data-ttu-id="5e940-210">在虛擬電腦規模集中進行伸縮時遵循的規則。</span><span class="sxs-lookup"><span data-stu-id="5e940-210">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="5e940-211">可能的值為： "Default"、"OldestVM" 和 "NewestVM"。</span><span class="sxs-lookup"><span data-stu-id="5e940-211">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="5e940-212">[預設值] 當虛擬電腦縮放比例設定為放大時，如果區域為區域性比例集，則比例集會先平衡在各個區域。</span><span class="sxs-lookup"><span data-stu-id="5e940-212">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="5e940-213">接著，它會盡可能在故障網域之間平衡。</span><span class="sxs-lookup"><span data-stu-id="5e940-213">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="5e940-214">在每個容錯網域中，選取要移除的虛擬機器將是無法從擴展保護的最新虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="5e940-214">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="5e940-215">"OldestVM" 當虛擬電腦縮放比例設定為放大時，系統將不會選擇要移除的最舊虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="5e940-215">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="5e940-216">針對 [區塊虛擬電腦] 規模集，比例集將在各個區域之間進行平衡。</span><span class="sxs-lookup"><span data-stu-id="5e940-216">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="5e940-217">在每個區域中，將會選取未受保護的舊虛擬機器，以供移除。</span><span class="sxs-lookup"><span data-stu-id="5e940-217">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="5e940-218">"NewestVM" 當虛擬電腦縮放比例設定為放大時，系統將不會選取任何不受放大的虛擬機器來進行移除。</span><span class="sxs-lookup"><span data-stu-id="5e940-218">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="5e940-219">針對 [區塊虛擬電腦] 規模集，比例集將在各個區域之間進行平衡。</span><span class="sxs-lookup"><span data-stu-id="5e940-219">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="5e940-220">在每個區域中，將會選取未受到保護的新虛擬機器電腦來移除。</span><span class="sxs-lookup"><span data-stu-id="5e940-220">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e940-221">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="5e940-221">-SinglePlacementGroup</span></span>
<span data-ttu-id="5e940-222">指定單一位置群組。</span><span class="sxs-lookup"><span data-stu-id="5e940-222">Specifies the single placement group.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e940-223">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="5e940-223">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="5e940-224">指定延伸不會在額外的 overprovisioned Vm 上執行。</span><span class="sxs-lookup"><span data-stu-id="5e940-224">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="5e940-225">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="5e940-225">-SkuCapacity</span></span>
<span data-ttu-id="5e940-226">指定 VMSS 中的實例數。</span><span class="sxs-lookup"><span data-stu-id="5e940-226">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e940-227">-SkuName</span><span class="sxs-lookup"><span data-stu-id="5e940-227">-SkuName</span></span>
<span data-ttu-id="5e940-228">指定 VMSS 的所有實例大小。</span><span class="sxs-lookup"><span data-stu-id="5e940-228">Specifies the size of all the instances of VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e940-229">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="5e940-229">-SkuTier</span></span>
<span data-ttu-id="5e940-230">指定 VMSS 的層級。</span><span class="sxs-lookup"><span data-stu-id="5e940-230">Specifies the tier of VMSS.</span></span> <span data-ttu-id="5e940-231">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="5e940-231">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5e940-232">標準</span><span class="sxs-lookup"><span data-stu-id="5e940-232">Standard</span></span>
- <span data-ttu-id="5e940-233">空白</span><span class="sxs-lookup"><span data-stu-id="5e940-233">Basic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e940-234">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="5e940-234">-StorageProfile</span></span>
<span data-ttu-id="5e940-235">指定包含 VMSS 設定之磁片摘要資訊的儲存空間物件。</span><span class="sxs-lookup"><span data-stu-id="5e940-235">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="5e940-236">您可以使用 **AzVmssStorageProfile** Cmdlet 來設定此物件。</span><span class="sxs-lookup"><span data-stu-id="5e940-236">You can use the **Set-AzVmssStorageProfile** cmdlet to set this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e940-237">-Tag</span><span class="sxs-lookup"><span data-stu-id="5e940-237">-Tag</span></span>
<span data-ttu-id="5e940-238">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="5e940-238">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5e940-239">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="5e940-239">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e940-240">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="5e940-240">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="5e940-241">已刪除的虛擬機器 (數分鐘內可設定的時間長度) ，必須先核准終止排程事件，然後才能自動核准 (超時) 。</span><span class="sxs-lookup"><span data-stu-id="5e940-241">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="5e940-242">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="5e940-242">-TerminateScheduledEvents</span></span>
<span data-ttu-id="5e940-243">啟用終止排程事件</span><span class="sxs-lookup"><span data-stu-id="5e940-243">Enable the Terminate Scheduled events</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e940-244">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="5e940-244">-UpgradePolicyMode</span></span>
<span data-ttu-id="5e940-245">已指定升級模式至規模集中的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="5e940-245">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="5e940-246">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="5e940-246">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5e940-247">自動</span><span class="sxs-lookup"><span data-stu-id="5e940-247">Automatic</span></span>
- <span data-ttu-id="5e940-248">手動</span><span class="sxs-lookup"><span data-stu-id="5e940-248">Manual</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.UpgradeMode]
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e940-249">-Zone</span><span class="sxs-lookup"><span data-stu-id="5e940-249">-Zone</span></span>
<span data-ttu-id="5e940-250">指定虛擬機器縮放集的區域清單。</span><span class="sxs-lookup"><span data-stu-id="5e940-250">Specifies the zone list for the virtual machine scale set.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e940-251">-ZoneBalance</span><span class="sxs-lookup"><span data-stu-id="5e940-251">-ZoneBalance</span></span>
<span data-ttu-id="5e940-252">在發生區域中斷時，是否要強制嚴格地根據 x 個區域進行虛擬電腦發佈。</span><span class="sxs-lookup"><span data-stu-id="5e940-252">Whether to force strictly even Virtual Machine distribution cross x-zones in case there is zone outage.</span></span>

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

### <span data-ttu-id="5e940-253">-確認</span><span class="sxs-lookup"><span data-stu-id="5e940-253">-Confirm</span></span>
<span data-ttu-id="5e940-254">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5e940-254">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e940-255">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e940-255">-WhatIf</span></span>
<span data-ttu-id="5e940-256">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5e940-256">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5e940-257">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5e940-257">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e940-258">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e940-258">CommonParameters</span></span>
<span data-ttu-id="5e940-259">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5e940-259">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e940-260">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5e940-260">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e940-261">輸入</span><span class="sxs-lookup"><span data-stu-id="5e940-261">INPUTS</span></span>

### <span data-ttu-id="5e940-262">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5e940-262">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="5e940-263">System.object</span><span class="sxs-lookup"><span data-stu-id="5e940-263">System.String</span></span>

### <span data-ttu-id="5e940-264">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="5e940-264">System.Collections.Hashtable</span></span>

### <span data-ttu-id="5e940-265">System.object</span><span class="sxs-lookup"><span data-stu-id="5e940-265">System.Int32</span></span>

### <span data-ttu-id="5e940-266">"UpgradeMode" 1 [[23.0.0.0]。計算，版本 =，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]]）。）</span><span class="sxs-lookup"><span data-stu-id="5e940-266">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="5e940-267">VirtualMachineScaleSetOSProfile 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="5e940-267">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span></span>

### <span data-ttu-id="5e940-268">VirtualMachineScaleSetStorageProfile 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="5e940-268">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span></span>

### <span data-ttu-id="5e940-269">VirtualMachineScaleSetNetworkConfiguration [] 的計算模型。</span><span class="sxs-lookup"><span data-stu-id="5e940-269">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span></span>

### <span data-ttu-id="5e940-270">VirtualMachineScaleSetExtension [] 的計算模型。</span><span class="sxs-lookup"><span data-stu-id="5e940-270">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span></span>

### <span data-ttu-id="5e940-271">System.object []</span><span class="sxs-lookup"><span data-stu-id="5e940-271">System.String[]</span></span>

### <span data-ttu-id="5e940-272">RollingUpgradePolicy 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="5e940-272">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span></span>

### <span data-ttu-id="5e940-273">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="5e940-273">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="5e940-274">BootDiagnostics 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="5e940-274">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span></span>

### <span data-ttu-id="5e940-275">"ResourceIdentityType" 1 [[23.0.0.0]。計算，版本 =，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]]）。）</span><span class="sxs-lookup"><span data-stu-id="5e940-275">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="5e940-276">輸出</span><span class="sxs-lookup"><span data-stu-id="5e940-276">OUTPUTS</span></span>

### <span data-ttu-id="5e940-277">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="5e940-277">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="5e940-278">筆記</span><span class="sxs-lookup"><span data-stu-id="5e940-278">NOTES</span></span>

## <span data-ttu-id="5e940-279">相關連結</span><span class="sxs-lookup"><span data-stu-id="5e940-279">RELATED LINKS</span></span>

[<span data-ttu-id="5e940-280">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="5e940-280">Set-AzVmssOsProfile</span></span>](./Set-AzVmssOsProfile.md)

[<span data-ttu-id="5e940-281">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="5e940-281">Set-AzVmssStorageProfile</span></span>](./Set-AzVmssStorageProfile.md)

[<span data-ttu-id="5e940-282">附加 AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="5e940-282">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="5e940-283">附加 AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="5e940-283">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="5e940-284">新-AzVmss</span><span class="sxs-lookup"><span data-stu-id="5e940-284">New-AzVmss</span></span>](./New-AzVmss.md)
