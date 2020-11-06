---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: e65bfa607f9689a85f7734b1913bbabadd4dd115
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613289"
---
# <span data-ttu-id="34a09-101">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="34a09-101">New-AzVmssConfig</span></span>

## <span data-ttu-id="34a09-102">摘要</span><span class="sxs-lookup"><span data-stu-id="34a09-102">SYNOPSIS</span></span>
<span data-ttu-id="34a09-103">建立 VMSS 設定物件。</span><span class="sxs-lookup"><span data-stu-id="34a09-103">Creates a VMSS configuration object.</span></span>

## <span data-ttu-id="34a09-104">句法</span><span class="sxs-lookup"><span data-stu-id="34a09-104">SYNTAX</span></span>

### <span data-ttu-id="34a09-105">DefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="34a09-105">DefaultParameterSet (Default)</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-ZoneBalance]
 [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>] [-PlanName <String>] [-PlanPublisher <String>]
 [-PlanProduct <String>] [-PlanPromotionCode <String>] [-RollingUpgradePolicy <RollingUpgradePolicy>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-MaxPrice <Double>] [-TerminateScheduledEvents] [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>]
 [-ProximityPlacementGroupId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="34a09-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="34a09-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-ZoneBalance]
 [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>] [-PlanName <String>] [-PlanPublisher <String>]
 [-PlanProduct <String>] [-PlanPromotionCode <String>] [-RollingUpgradePolicy <RollingUpgradePolicy>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-MaxPrice <Double>] [-TerminateScheduledEvents] [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>]
 [-ProximityPlacementGroupId <String>] -IdentityType <ResourceIdentityType> [-IdentityId <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34a09-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="34a09-107">AssignIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-ZoneBalance]
 [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>] [-PlanName <String>] [-PlanPublisher <String>]
 [-PlanProduct <String>] [-PlanPromotionCode <String>] [-RollingUpgradePolicy <RollingUpgradePolicy>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-MaxPrice <Double>] [-TerminateScheduledEvents] [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>]
 [-ProximityPlacementGroupId <String>] [-AssignIdentity] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34a09-108">說明</span><span class="sxs-lookup"><span data-stu-id="34a09-108">DESCRIPTION</span></span>
<span data-ttu-id="34a09-109">**新的-AzVmssConfig** Cmdlet 會建立可設定的本機視覺管理員縮放比例集， (VMSS) 物件。</span><span class="sxs-lookup"><span data-stu-id="34a09-109">The **New-AzVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="34a09-110">需要其他 Cmdlet 來設定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="34a09-110">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="34a09-111">這些 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="34a09-111">These cmdlets are:</span></span>
- <span data-ttu-id="34a09-112">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="34a09-112">Set-AzVmssOsProfile</span></span>
- <span data-ttu-id="34a09-113">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="34a09-113">Set-AzVmssStorageProfile</span></span>
- <span data-ttu-id="34a09-114">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="34a09-114">Add-AzVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="34a09-115">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="34a09-115">Add-AzVmssExtension</span></span>

## <span data-ttu-id="34a09-116">示例</span><span class="sxs-lookup"><span data-stu-id="34a09-116">EXAMPLES</span></span>

### <span data-ttu-id="34a09-117">範例1：建立 VMSS 設定物件</span><span class="sxs-lookup"><span data-stu-id="34a09-117">Example 1: Create a VMSS configuration object</span></span>
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

<span data-ttu-id="34a09-118">這個範例會建立 VMSS 設定物件。</span><span class="sxs-lookup"><span data-stu-id="34a09-118">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="34a09-119">第一個命令使用 **新的 AzVmssConfig** Cmdlet 來建立 VMSS 設定物件，並將結果儲存在名為 $VMSS 的變數中。</span><span class="sxs-lookup"><span data-stu-id="34a09-119">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="34a09-120">第二個命令使用 **AzVmss** Cmdlet 來建立使用在第一個命令中建立之 VMSS 設定物件的 VMSS。</span><span class="sxs-lookup"><span data-stu-id="34a09-120">The second command uses the **New-AzVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="34a09-121">參數</span><span class="sxs-lookup"><span data-stu-id="34a09-121">PARAMETERS</span></span>

### <span data-ttu-id="34a09-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="34a09-122">-AssignIdentity</span></span>
<span data-ttu-id="34a09-123">指定系統指派的虛擬機器縮放集身分識別。</span><span class="sxs-lookup"><span data-stu-id="34a09-123">Specify the system assigned identity for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="34a09-124">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="34a09-124">-AutoOSUpgrade</span></span>
<span data-ttu-id="34a09-125">設定更新版本的影像時，是否應該將作業系統升級自動套用到縮放集實例，以滾動的方式進行。</span><span class="sxs-lookup"><span data-stu-id="34a09-125">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="34a09-126">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="34a09-126">-BootDiagnostic</span></span>
<span data-ttu-id="34a09-127">指定虛擬機器縮放設定啟動診斷設定檔。</span><span class="sxs-lookup"><span data-stu-id="34a09-127">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="34a09-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34a09-128">-DefaultProfile</span></span>
<span data-ttu-id="34a09-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="34a09-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34a09-130">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="34a09-130">-DisableAutoRollback</span></span>
<span data-ttu-id="34a09-131">針對自動 OS 升級原則停用自動復原</span><span class="sxs-lookup"><span data-stu-id="34a09-131">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="34a09-132">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="34a09-132">-EnableUltraSSD</span></span>
<span data-ttu-id="34a09-133">可讓一或多個受管理的資料磁片使用一或多個在虛擬機器縮放設定上擁有 UltraSSD_LRS 儲存帳戶類型的功能。</span><span class="sxs-lookup"><span data-stu-id="34a09-133">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="34a09-134">只有在啟用此屬性時，才能將儲存帳戶類型 UltraSSD_LRS 的受管理磁片新增至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="34a09-134">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="34a09-135">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="34a09-135">-EvictionPolicy</span></span>
<span data-ttu-id="34a09-136">針對規模集中的虛擬機器指定逐出原則。</span><span class="sxs-lookup"><span data-stu-id="34a09-136">Specifies the eviction policy for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="34a09-137">-延伸</span><span class="sxs-lookup"><span data-stu-id="34a09-137">-Extension</span></span>
<span data-ttu-id="34a09-138">指定 VMSS 的延伸資訊物件。</span><span class="sxs-lookup"><span data-stu-id="34a09-138">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="34a09-139">您可以使用 **AzVmssExtension** Cmdlet 來新增此物件。</span><span class="sxs-lookup"><span data-stu-id="34a09-139">You can use the **Add-AzVmssExtension** cmdlet to add this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34a09-140">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="34a09-140">-HealthProbeId</span></span>
<span data-ttu-id="34a09-141">指定負載平衡器探測的識別碼，這些探測器用來判斷虛擬機器規模集中的實例健康情況。</span><span class="sxs-lookup"><span data-stu-id="34a09-141">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="34a09-142">HealthProbeId 的形式為「/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}」。</span><span class="sxs-lookup"><span data-stu-id="34a09-142">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="34a09-143">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="34a09-143">-IdentityId</span></span>
<span data-ttu-id="34a09-144">指定與虛擬機器小性集相關聯的使用者識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="34a09-144">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="34a09-145">使用者身分識別參照將是下列形式的 ARM 資源識別碼： '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="34a09-145">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="34a09-146">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="34a09-146">-IdentityType</span></span>
<span data-ttu-id="34a09-147">指定用於虛擬機器規模集的身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="34a09-147">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="34a09-148">"SystemAssignedUserAssigned" 類型包含隱含建立的身分識別，以及一組使用者指派的身分識別。</span><span class="sxs-lookup"><span data-stu-id="34a09-148">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="34a09-149">"None" 類型將會移除虛擬機器小單位集中的任何身分識別。</span><span class="sxs-lookup"><span data-stu-id="34a09-149">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="34a09-150">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="34a09-150">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="34a09-151">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="34a09-151">SystemAssigned</span></span>
- <span data-ttu-id="34a09-152">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="34a09-152">UserAssigned</span></span>
- <span data-ttu-id="34a09-153">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="34a09-153">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="34a09-154">所有</span><span class="sxs-lookup"><span data-stu-id="34a09-154">None</span></span>

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

### <span data-ttu-id="34a09-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="34a09-155">-LicenseType</span></span>
<span data-ttu-id="34a09-156">指定授權類型，這是用來提供您自己的授權案例。</span><span class="sxs-lookup"><span data-stu-id="34a09-156">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="34a09-157">-位置</span><span class="sxs-lookup"><span data-stu-id="34a09-157">-Location</span></span>
<span data-ttu-id="34a09-158">指定建立 VMSS 的 Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="34a09-158">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="34a09-159">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="34a09-159">-MaxPrice</span></span>
<span data-ttu-id="34a09-160">指定低優先順序 VM/VMSS 要支付的最大價格。</span><span class="sxs-lookup"><span data-stu-id="34a09-160">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="34a09-161">這個價格是美元。</span><span class="sxs-lookup"><span data-stu-id="34a09-161">This price is in US Dollars.</span></span> <span data-ttu-id="34a09-162">此價格將與 VM 大小的目前低優先順序價格進行比較。</span><span class="sxs-lookup"><span data-stu-id="34a09-162">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="34a09-163">此外，價格會在建立/更新低優先順序 VM/VMSS 的時間進行比較，而且只有在 maxPrice 大於目前的低優先順序價格時，作業才會成功。</span><span class="sxs-lookup"><span data-stu-id="34a09-163">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="34a09-164">如果在建立 VM/VMSS 之後，目前的低優先順序價格超過 maxPrice，則 maxPrice 也會用於逐出低優先順序 VM/VMSS。</span><span class="sxs-lookup"><span data-stu-id="34a09-164">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="34a09-165">可能的值為：任何大於零的十進位值。</span><span class="sxs-lookup"><span data-stu-id="34a09-165">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="34a09-166">範例：0.01538。</span><span class="sxs-lookup"><span data-stu-id="34a09-166">Example: 0.01538.</span></span>  <span data-ttu-id="34a09-167">-1 表示由於價格原因，不應逐出低優先順序 VM/VMSS。</span><span class="sxs-lookup"><span data-stu-id="34a09-167">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="34a09-168">此外，如果您沒有提供預設的最大價格，就是-1。</span><span class="sxs-lookup"><span data-stu-id="34a09-168">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="34a09-169">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="34a09-169">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="34a09-170">指定包含 VMSS 設定之網路屬性的網路設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="34a09-170">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="34a09-171">您可以使用 **AzVmssNetworkInterfaceConfiguration** Cmdlet 來新增此物件。</span><span class="sxs-lookup"><span data-stu-id="34a09-171">You can use the **Add-AzVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="34a09-172">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="34a09-172">-OsProfile</span></span>
<span data-ttu-id="34a09-173">指定作業系統設定檔物件，其中包含 VMSS 設定的作業系統屬性。</span><span class="sxs-lookup"><span data-stu-id="34a09-173">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="34a09-174">您可以使用 **AzVmssOsProfile** Cmdlet 來設定此物件。</span><span class="sxs-lookup"><span data-stu-id="34a09-174">You can use the **Set-AzVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="34a09-175">-Overprovision</span><span class="sxs-lookup"><span data-stu-id="34a09-175">-Overprovision</span></span>
<span data-ttu-id="34a09-176">指示 Cmdlet 是否 overprovisions VMSS。</span><span class="sxs-lookup"><span data-stu-id="34a09-176">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="34a09-177">-PlanName</span><span class="sxs-lookup"><span data-stu-id="34a09-177">-PlanName</span></span>
<span data-ttu-id="34a09-178">指定方案名稱。</span><span class="sxs-lookup"><span data-stu-id="34a09-178">Specifies the plan name.</span></span>

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

### <span data-ttu-id="34a09-179">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="34a09-179">-PlanProduct</span></span>
<span data-ttu-id="34a09-180">指定方案產品。</span><span class="sxs-lookup"><span data-stu-id="34a09-180">Specifies the plan product.</span></span>

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

### <span data-ttu-id="34a09-181">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="34a09-181">-PlanPromotionCode</span></span>
<span data-ttu-id="34a09-182">指定方案促銷代碼。</span><span class="sxs-lookup"><span data-stu-id="34a09-182">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="34a09-183">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="34a09-183">-PlanPublisher</span></span>
<span data-ttu-id="34a09-184">指定方案發行者。</span><span class="sxs-lookup"><span data-stu-id="34a09-184">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="34a09-185">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="34a09-185">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="34a09-186">每個位置群組的錯誤網域計數。</span><span class="sxs-lookup"><span data-stu-id="34a09-186">Fault Domain count for each placement group.</span></span>

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

### <span data-ttu-id="34a09-187">-優先順序</span><span class="sxs-lookup"><span data-stu-id="34a09-187">-Priority</span></span>
<span data-ttu-id="34a09-188">指定規模集中虛擬機器的優先順序。</span><span class="sxs-lookup"><span data-stu-id="34a09-188">Specifies the priority for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="34a09-189">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="34a09-189">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="34a09-190">ProximityPlacementGroup 的識別碼</span><span class="sxs-lookup"><span data-stu-id="34a09-190">The Id of ProximityPlacementGroup</span></span>

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

### <span data-ttu-id="34a09-191">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="34a09-191">-RollingUpgradePolicy</span></span>
<span data-ttu-id="34a09-192">指定輪流升級原則。</span><span class="sxs-lookup"><span data-stu-id="34a09-192">Specifies the rolling upgrade policy.</span></span>

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

### <span data-ttu-id="34a09-193">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="34a09-193">-SinglePlacementGroup</span></span>
<span data-ttu-id="34a09-194">指定單一位置群組。</span><span class="sxs-lookup"><span data-stu-id="34a09-194">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="34a09-195">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="34a09-195">-SkuCapacity</span></span>
<span data-ttu-id="34a09-196">指定 VMSS 中的實例數。</span><span class="sxs-lookup"><span data-stu-id="34a09-196">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="34a09-197">-SkuName</span><span class="sxs-lookup"><span data-stu-id="34a09-197">-SkuName</span></span>
<span data-ttu-id="34a09-198">指定 VMSS 的所有實例大小。</span><span class="sxs-lookup"><span data-stu-id="34a09-198">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="34a09-199">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="34a09-199">-SkuTier</span></span>
<span data-ttu-id="34a09-200">指定 VMSS 的層級。</span><span class="sxs-lookup"><span data-stu-id="34a09-200">Specifies the tier of VMSS.</span></span> <span data-ttu-id="34a09-201">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="34a09-201">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="34a09-202">標準</span><span class="sxs-lookup"><span data-stu-id="34a09-202">Standard</span></span>
- <span data-ttu-id="34a09-203">空白</span><span class="sxs-lookup"><span data-stu-id="34a09-203">Basic</span></span>

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

### <span data-ttu-id="34a09-204">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="34a09-204">-StorageProfile</span></span>
<span data-ttu-id="34a09-205">指定包含 VMSS 設定之磁片摘要資訊的儲存空間物件。</span><span class="sxs-lookup"><span data-stu-id="34a09-205">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="34a09-206">您可以使用 **AzVmssStorageProfile** Cmdlet 來設定此物件。</span><span class="sxs-lookup"><span data-stu-id="34a09-206">You can use the **Set-AzVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="34a09-207">-Tag</span><span class="sxs-lookup"><span data-stu-id="34a09-207">-Tag</span></span>
<span data-ttu-id="34a09-208">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="34a09-208">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="34a09-209">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="34a09-209">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="34a09-210">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="34a09-210">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="34a09-211">已刪除的虛擬機器 (數分鐘內可設定的時間長度) ，必須先核准終止排程事件，然後才能自動核准 (超時) 。</span><span class="sxs-lookup"><span data-stu-id="34a09-211">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="34a09-212">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="34a09-212">-TerminateScheduledEvents</span></span>
<span data-ttu-id="34a09-213">啟用終止排程事件</span><span class="sxs-lookup"><span data-stu-id="34a09-213">Enable the Terminate Scheduled events</span></span>

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

### <span data-ttu-id="34a09-214">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="34a09-214">-UpgradePolicyMode</span></span>
<span data-ttu-id="34a09-215">已指定升級模式至規模集中的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="34a09-215">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="34a09-216">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="34a09-216">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="34a09-217">自動</span><span class="sxs-lookup"><span data-stu-id="34a09-217">Automatic</span></span>
- <span data-ttu-id="34a09-218">手動</span><span class="sxs-lookup"><span data-stu-id="34a09-218">Manual</span></span>

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

### <span data-ttu-id="34a09-219">-Zone</span><span class="sxs-lookup"><span data-stu-id="34a09-219">-Zone</span></span>
<span data-ttu-id="34a09-220">指定虛擬機器縮放集的區域清單。</span><span class="sxs-lookup"><span data-stu-id="34a09-220">Specifies the zone list for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="34a09-221">-ZoneBalance</span><span class="sxs-lookup"><span data-stu-id="34a09-221">-ZoneBalance</span></span>
<span data-ttu-id="34a09-222">在發生區域中斷時，是否要強制嚴格地根據 x 個區域進行虛擬電腦發佈。</span><span class="sxs-lookup"><span data-stu-id="34a09-222">Whether to force strictly even Virtual Machine distribution cross x-zones in case there is zone outage.</span></span>

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

### <span data-ttu-id="34a09-223">-確認</span><span class="sxs-lookup"><span data-stu-id="34a09-223">-Confirm</span></span>
<span data-ttu-id="34a09-224">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="34a09-224">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34a09-225">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34a09-225">-WhatIf</span></span>
<span data-ttu-id="34a09-226">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="34a09-226">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="34a09-227">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="34a09-227">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34a09-228">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34a09-228">CommonParameters</span></span>
<span data-ttu-id="34a09-229">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="34a09-229">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34a09-230">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="34a09-230">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34a09-231">輸入</span><span class="sxs-lookup"><span data-stu-id="34a09-231">INPUTS</span></span>

### <span data-ttu-id="34a09-232">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="34a09-232">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="34a09-233">System.object</span><span class="sxs-lookup"><span data-stu-id="34a09-233">System.String</span></span>

### <span data-ttu-id="34a09-234">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="34a09-234">System.Collections.Hashtable</span></span>

### <span data-ttu-id="34a09-235">System.object</span><span class="sxs-lookup"><span data-stu-id="34a09-235">System.Int32</span></span>

### <span data-ttu-id="34a09-236">"UpgradeMode" 1 [[23.0.0.0]。計算，版本 =，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]]）。）</span><span class="sxs-lookup"><span data-stu-id="34a09-236">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="34a09-237">VirtualMachineScaleSetOSProfile 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="34a09-237">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span></span>

### <span data-ttu-id="34a09-238">VirtualMachineScaleSetStorageProfile 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="34a09-238">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span></span>

### <span data-ttu-id="34a09-239">VirtualMachineScaleSetNetworkConfiguration [] 的計算模型。</span><span class="sxs-lookup"><span data-stu-id="34a09-239">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span></span>

### <span data-ttu-id="34a09-240">VirtualMachineScaleSetExtension [] 的計算模型。</span><span class="sxs-lookup"><span data-stu-id="34a09-240">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span></span>

### <span data-ttu-id="34a09-241">System.object []</span><span class="sxs-lookup"><span data-stu-id="34a09-241">System.String[]</span></span>

### <span data-ttu-id="34a09-242">RollingUpgradePolicy 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="34a09-242">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span></span>

### <span data-ttu-id="34a09-243">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="34a09-243">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="34a09-244">BootDiagnostics 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="34a09-244">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span></span>

### <span data-ttu-id="34a09-245">"ResourceIdentityType" 1 [[23.0.0.0]。計算，版本 =，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]]）。）</span><span class="sxs-lookup"><span data-stu-id="34a09-245">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="34a09-246">輸出</span><span class="sxs-lookup"><span data-stu-id="34a09-246">OUTPUTS</span></span>

### <span data-ttu-id="34a09-247">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="34a09-247">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="34a09-248">筆記</span><span class="sxs-lookup"><span data-stu-id="34a09-248">NOTES</span></span>

## <span data-ttu-id="34a09-249">相關連結</span><span class="sxs-lookup"><span data-stu-id="34a09-249">RELATED LINKS</span></span>

[<span data-ttu-id="34a09-250">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="34a09-250">Set-AzVmssOsProfile</span></span>](./Set-AzVmssOsProfile.md)

[<span data-ttu-id="34a09-251">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="34a09-251">Set-AzVmssStorageProfile</span></span>](./Set-AzVmssStorageProfile.md)

[<span data-ttu-id="34a09-252">附加 AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="34a09-252">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="34a09-253">附加 AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="34a09-253">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="34a09-254">新-AzVmss</span><span class="sxs-lookup"><span data-stu-id="34a09-254">New-AzVmss</span></span>](./New-AzVmss.md)
