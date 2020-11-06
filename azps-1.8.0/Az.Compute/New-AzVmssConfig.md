---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: beb9c067fb2ca625fcf756747a52eef0bf1ca9b5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622745"
---
# <span data-ttu-id="49a92-101">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="49a92-101">New-AzVmssConfig</span></span>

## <span data-ttu-id="49a92-102">摘要</span><span class="sxs-lookup"><span data-stu-id="49a92-102">SYNOPSIS</span></span>
<span data-ttu-id="49a92-103">建立 VMSS 設定物件。</span><span class="sxs-lookup"><span data-stu-id="49a92-103">Creates a VMSS configuration object.</span></span>

## <span data-ttu-id="49a92-104">句法</span><span class="sxs-lookup"><span data-stu-id="49a92-104">SYNTAX</span></span>

### <span data-ttu-id="49a92-105">DefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="49a92-105">DefaultParameterSet (Default)</span></span>
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
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49a92-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="49a92-106">ExplicitIdentityParameterSet</span></span>
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
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49a92-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="49a92-107">AssignIdentityParameterSet</span></span>
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
 [-AssignIdentity] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49a92-108">說明</span><span class="sxs-lookup"><span data-stu-id="49a92-108">DESCRIPTION</span></span>
<span data-ttu-id="49a92-109">**新的-AzVmssConfig** Cmdlet 會建立可設定的本機視覺管理員縮放比例集， (VMSS) 物件。</span><span class="sxs-lookup"><span data-stu-id="49a92-109">The **New-AzVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="49a92-110">需要其他 Cmdlet 來設定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="49a92-110">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="49a92-111">這些 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="49a92-111">These cmdlets are:</span></span>
- <span data-ttu-id="49a92-112">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="49a92-112">Set-AzVmssOsProfile</span></span>
- <span data-ttu-id="49a92-113">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="49a92-113">Set-AzVmssStorageProfile</span></span>
- <span data-ttu-id="49a92-114">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="49a92-114">Add-AzVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="49a92-115">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="49a92-115">Add-AzVmssExtension</span></span>

## <span data-ttu-id="49a92-116">示例</span><span class="sxs-lookup"><span data-stu-id="49a92-116">EXAMPLES</span></span>

### <span data-ttu-id="49a92-117">範例1：建立 VMSS 設定物件</span><span class="sxs-lookup"><span data-stu-id="49a92-117">Example 1: Create a VMSS configuration object</span></span>
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

<span data-ttu-id="49a92-118">這個範例會建立 VMSS 設定物件。</span><span class="sxs-lookup"><span data-stu-id="49a92-118">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="49a92-119">第一個命令使用 **新的 AzVmssConfig** Cmdlet 來建立 VMSS 設定物件，並將結果儲存在名為 $VMSS 的變數中。</span><span class="sxs-lookup"><span data-stu-id="49a92-119">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="49a92-120">第二個命令使用 **AzVmss** Cmdlet 來建立使用在第一個命令中建立之 VMSS 設定物件的 VMSS。</span><span class="sxs-lookup"><span data-stu-id="49a92-120">The second command uses the **New-AzVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="49a92-121">參數</span><span class="sxs-lookup"><span data-stu-id="49a92-121">PARAMETERS</span></span>

### <span data-ttu-id="49a92-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="49a92-122">-AssignIdentity</span></span>
<span data-ttu-id="49a92-123">指定系統指派的虛擬機器縮放集身分識別。</span><span class="sxs-lookup"><span data-stu-id="49a92-123">Specify the system assigned identity for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="49a92-124">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="49a92-124">-AutoOSUpgrade</span></span>
<span data-ttu-id="49a92-125">設定更新版本的影像時，是否應該將作業系統升級自動套用到縮放集實例，以滾動的方式進行。</span><span class="sxs-lookup"><span data-stu-id="49a92-125">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="49a92-126">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="49a92-126">-BootDiagnostic</span></span>
<span data-ttu-id="49a92-127">指定虛擬機器縮放設定啟動診斷設定檔。</span><span class="sxs-lookup"><span data-stu-id="49a92-127">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="49a92-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49a92-128">-DefaultProfile</span></span>
<span data-ttu-id="49a92-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="49a92-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49a92-130">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="49a92-130">-DisableAutoRollback</span></span>
<span data-ttu-id="49a92-131">針對自動 OS 升級原則停用自動復原</span><span class="sxs-lookup"><span data-stu-id="49a92-131">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="49a92-132">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="49a92-132">-EnableUltraSSD</span></span>
<span data-ttu-id="49a92-133">可讓一或多個受管理的資料磁片使用一或多個在虛擬機器縮放設定上擁有 UltraSSD_LRS 儲存帳戶類型的功能。</span><span class="sxs-lookup"><span data-stu-id="49a92-133">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="49a92-134">只有在啟用此屬性時，才能將儲存帳戶類型 UltraSSD_LRS 的受管理磁片新增至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="49a92-134">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="49a92-135">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="49a92-135">-EvictionPolicy</span></span>
<span data-ttu-id="49a92-136">針對規模集中的虛擬機器指定逐出原則。</span><span class="sxs-lookup"><span data-stu-id="49a92-136">Specifies the eviction policy for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="49a92-137">-延伸</span><span class="sxs-lookup"><span data-stu-id="49a92-137">-Extension</span></span>
<span data-ttu-id="49a92-138">指定 VMSS 的延伸資訊物件。</span><span class="sxs-lookup"><span data-stu-id="49a92-138">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="49a92-139">您可以使用 **AzVmssExtension** Cmdlet 來新增此物件。</span><span class="sxs-lookup"><span data-stu-id="49a92-139">You can use the **Add-AzVmssExtension** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="49a92-140">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="49a92-140">-HealthProbeId</span></span>
<span data-ttu-id="49a92-141">指定負載平衡器探測的識別碼，這些探測器用來判斷虛擬機器規模集中的實例健康情況。</span><span class="sxs-lookup"><span data-stu-id="49a92-141">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="49a92-142">HealthProbeId 的形式為「/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}」。</span><span class="sxs-lookup"><span data-stu-id="49a92-142">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="49a92-143">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="49a92-143">-IdentityId</span></span>
<span data-ttu-id="49a92-144">指定與虛擬機器小性集相關聯的使用者識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="49a92-144">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="49a92-145">使用者身分識別參照將是下列形式的 ARM 資源識別碼： '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="49a92-145">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="49a92-146">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="49a92-146">-IdentityType</span></span>
<span data-ttu-id="49a92-147">指定用於虛擬機器規模集的身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="49a92-147">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="49a92-148">"SystemAssignedUserAssigned" 類型包含隱含建立的身分識別，以及一組使用者指派的身分識別。</span><span class="sxs-lookup"><span data-stu-id="49a92-148">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="49a92-149">"None" 類型將會移除虛擬機器小單位集中的任何身分識別。</span><span class="sxs-lookup"><span data-stu-id="49a92-149">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="49a92-150">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="49a92-150">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="49a92-151">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="49a92-151">SystemAssigned</span></span>
- <span data-ttu-id="49a92-152">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="49a92-152">UserAssigned</span></span>
- <span data-ttu-id="49a92-153">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="49a92-153">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="49a92-154">所有</span><span class="sxs-lookup"><span data-stu-id="49a92-154">None</span></span>

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

### <span data-ttu-id="49a92-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="49a92-155">-LicenseType</span></span>
<span data-ttu-id="49a92-156">指定授權類型，這是用來提供您自己的授權案例。</span><span class="sxs-lookup"><span data-stu-id="49a92-156">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="49a92-157">-位置</span><span class="sxs-lookup"><span data-stu-id="49a92-157">-Location</span></span>
<span data-ttu-id="49a92-158">指定建立 VMSS 的 Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="49a92-158">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="49a92-159">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="49a92-159">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="49a92-160">指定包含 VMSS 設定之網路屬性的網路設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="49a92-160">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="49a92-161">您可以使用 **AzVmssNetworkInterfaceConfiguration** Cmdlet 來新增此物件。</span><span class="sxs-lookup"><span data-stu-id="49a92-161">You can use the **Add-AzVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="49a92-162">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="49a92-162">-OsProfile</span></span>
<span data-ttu-id="49a92-163">指定作業系統設定檔物件，其中包含 VMSS 設定的作業系統屬性。</span><span class="sxs-lookup"><span data-stu-id="49a92-163">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="49a92-164">您可以使用 **AzVmssOsProfile** Cmdlet 來設定此物件。</span><span class="sxs-lookup"><span data-stu-id="49a92-164">You can use the **Set-AzVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="49a92-165">-Overprovision</span><span class="sxs-lookup"><span data-stu-id="49a92-165">-Overprovision</span></span>
<span data-ttu-id="49a92-166">指示 Cmdlet 是否 overprovisions VMSS。</span><span class="sxs-lookup"><span data-stu-id="49a92-166">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="49a92-167">-PlanName</span><span class="sxs-lookup"><span data-stu-id="49a92-167">-PlanName</span></span>
<span data-ttu-id="49a92-168">指定方案名稱。</span><span class="sxs-lookup"><span data-stu-id="49a92-168">Specifies the plan name.</span></span>

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

### <span data-ttu-id="49a92-169">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="49a92-169">-PlanProduct</span></span>
<span data-ttu-id="49a92-170">指定方案產品。</span><span class="sxs-lookup"><span data-stu-id="49a92-170">Specifies the plan product.</span></span>

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

### <span data-ttu-id="49a92-171">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="49a92-171">-PlanPromotionCode</span></span>
<span data-ttu-id="49a92-172">指定方案促銷代碼。</span><span class="sxs-lookup"><span data-stu-id="49a92-172">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="49a92-173">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="49a92-173">-PlanPublisher</span></span>
<span data-ttu-id="49a92-174">指定方案發行者。</span><span class="sxs-lookup"><span data-stu-id="49a92-174">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="49a92-175">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="49a92-175">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="49a92-176">每個位置群組的錯誤網域計數。</span><span class="sxs-lookup"><span data-stu-id="49a92-176">Fault Domain count for each placement group.</span></span>

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

### <span data-ttu-id="49a92-177">-優先順序</span><span class="sxs-lookup"><span data-stu-id="49a92-177">-Priority</span></span>
<span data-ttu-id="49a92-178">指定規模集中虛擬機器的優先順序。</span><span class="sxs-lookup"><span data-stu-id="49a92-178">Specifies the priority for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="49a92-179">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="49a92-179">-RollingUpgradePolicy</span></span>
<span data-ttu-id="49a92-180">指定輪流升級原則。</span><span class="sxs-lookup"><span data-stu-id="49a92-180">Specifies the rolling upgrade policy.</span></span>

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

### <span data-ttu-id="49a92-181">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="49a92-181">-SinglePlacementGroup</span></span>
<span data-ttu-id="49a92-182">指定單一位置群組。</span><span class="sxs-lookup"><span data-stu-id="49a92-182">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="49a92-183">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="49a92-183">-SkuCapacity</span></span>
<span data-ttu-id="49a92-184">指定 VMSS 中的實例數。</span><span class="sxs-lookup"><span data-stu-id="49a92-184">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="49a92-185">-SkuName</span><span class="sxs-lookup"><span data-stu-id="49a92-185">-SkuName</span></span>
<span data-ttu-id="49a92-186">指定 VMSS 的所有實例大小。</span><span class="sxs-lookup"><span data-stu-id="49a92-186">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="49a92-187">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="49a92-187">-SkuTier</span></span>
<span data-ttu-id="49a92-188">指定 VMSS 的層級。</span><span class="sxs-lookup"><span data-stu-id="49a92-188">Specifies the tier of VMSS.</span></span> <span data-ttu-id="49a92-189">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="49a92-189">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="49a92-190">標準</span><span class="sxs-lookup"><span data-stu-id="49a92-190">Standard</span></span>
- <span data-ttu-id="49a92-191">空白</span><span class="sxs-lookup"><span data-stu-id="49a92-191">Basic</span></span>

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

### <span data-ttu-id="49a92-192">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="49a92-192">-StorageProfile</span></span>
<span data-ttu-id="49a92-193">指定包含 VMSS 設定之磁片摘要資訊的儲存空間物件。</span><span class="sxs-lookup"><span data-stu-id="49a92-193">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="49a92-194">您可以使用 **AzVmssStorageProfile** Cmdlet 來設定此物件。</span><span class="sxs-lookup"><span data-stu-id="49a92-194">You can use the **Set-AzVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="49a92-195">-Tag</span><span class="sxs-lookup"><span data-stu-id="49a92-195">-Tag</span></span>
<span data-ttu-id="49a92-196">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="49a92-196">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="49a92-197">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="49a92-197">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="49a92-198">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="49a92-198">-UpgradePolicyMode</span></span>
<span data-ttu-id="49a92-199">已指定升級模式至規模集中的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="49a92-199">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="49a92-200">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="49a92-200">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="49a92-201">自動</span><span class="sxs-lookup"><span data-stu-id="49a92-201">Automatic</span></span>
- <span data-ttu-id="49a92-202">手動</span><span class="sxs-lookup"><span data-stu-id="49a92-202">Manual</span></span>

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

### <span data-ttu-id="49a92-203">-Zone</span><span class="sxs-lookup"><span data-stu-id="49a92-203">-Zone</span></span>
<span data-ttu-id="49a92-204">指定虛擬機器縮放集的區域清單。</span><span class="sxs-lookup"><span data-stu-id="49a92-204">Specifies the zone list for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="49a92-205">-ZoneBalance</span><span class="sxs-lookup"><span data-stu-id="49a92-205">-ZoneBalance</span></span>
<span data-ttu-id="49a92-206">在發生區域中斷時，是否要強制嚴格地根據 x 個區域進行虛擬電腦發佈。</span><span class="sxs-lookup"><span data-stu-id="49a92-206">Whether to force strictly even Virtual Machine distribution cross x-zones in case there is zone outage.</span></span>

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

### <span data-ttu-id="49a92-207">-確認</span><span class="sxs-lookup"><span data-stu-id="49a92-207">-Confirm</span></span>
<span data-ttu-id="49a92-208">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="49a92-208">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49a92-209">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49a92-209">-WhatIf</span></span>
<span data-ttu-id="49a92-210">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="49a92-210">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="49a92-211">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="49a92-211">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49a92-212">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49a92-212">CommonParameters</span></span>
<span data-ttu-id="49a92-213">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="49a92-213">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49a92-214">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="49a92-214">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49a92-215">輸入</span><span class="sxs-lookup"><span data-stu-id="49a92-215">INPUTS</span></span>

### <span data-ttu-id="49a92-216">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="49a92-216">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="49a92-217">System.object</span><span class="sxs-lookup"><span data-stu-id="49a92-217">System.String</span></span>

### <span data-ttu-id="49a92-218">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="49a92-218">System.Collections.Hashtable</span></span>

### <span data-ttu-id="49a92-219">System.object</span><span class="sxs-lookup"><span data-stu-id="49a92-219">System.Int32</span></span>

### <span data-ttu-id="49a92-220">"UpgradeMode" 1 [[23.0.0.0]。計算，版本 =，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]]）。）</span><span class="sxs-lookup"><span data-stu-id="49a92-220">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="49a92-221">VirtualMachineScaleSetOSProfile 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="49a92-221">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span></span>

### <span data-ttu-id="49a92-222">VirtualMachineScaleSetStorageProfile 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="49a92-222">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span></span>

### <span data-ttu-id="49a92-223">VirtualMachineScaleSetNetworkConfiguration [] 的計算模型。</span><span class="sxs-lookup"><span data-stu-id="49a92-223">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span></span>

### <span data-ttu-id="49a92-224">VirtualMachineScaleSetExtension [] 的計算模型。</span><span class="sxs-lookup"><span data-stu-id="49a92-224">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span></span>

### <span data-ttu-id="49a92-225">System.object []</span><span class="sxs-lookup"><span data-stu-id="49a92-225">System.String[]</span></span>

### <span data-ttu-id="49a92-226">RollingUpgradePolicy 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="49a92-226">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span></span>

### <span data-ttu-id="49a92-227">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="49a92-227">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="49a92-228">BootDiagnostics 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="49a92-228">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span></span>

### <span data-ttu-id="49a92-229">"ResourceIdentityType" 1 [[23.0.0.0]。計算，版本 =，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]]）。）</span><span class="sxs-lookup"><span data-stu-id="49a92-229">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="49a92-230">輸出</span><span class="sxs-lookup"><span data-stu-id="49a92-230">OUTPUTS</span></span>

### <span data-ttu-id="49a92-231">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="49a92-231">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="49a92-232">筆記</span><span class="sxs-lookup"><span data-stu-id="49a92-232">NOTES</span></span>

## <span data-ttu-id="49a92-233">相關連結</span><span class="sxs-lookup"><span data-stu-id="49a92-233">RELATED LINKS</span></span>

[<span data-ttu-id="49a92-234">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="49a92-234">Set-AzVmssOsProfile</span></span>](./Set-AzVmssOsProfile.md)

[<span data-ttu-id="49a92-235">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="49a92-235">Set-AzVmssStorageProfile</span></span>](./Set-AzVmssStorageProfile.md)

[<span data-ttu-id="49a92-236">附加 AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="49a92-236">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="49a92-237">附加 AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="49a92-237">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="49a92-238">新-AzVmss</span><span class="sxs-lookup"><span data-stu-id="49a92-238">New-AzVmss</span></span>](./New-AzVmss.md)
