---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmssConfig.md
ms.openlocfilehash: ee18925960b7f2afd9e35250a3cc33a5bd16e073
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447426"
---
# <span data-ttu-id="11267-101">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="11267-101">New-AzureRmVmssConfig</span></span>

## <span data-ttu-id="11267-102">摘要</span><span class="sxs-lookup"><span data-stu-id="11267-102">SYNOPSIS</span></span>
<span data-ttu-id="11267-103">建立 VMSS 設定物件。</span><span class="sxs-lookup"><span data-stu-id="11267-103">Creates a VMSS configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11267-104">句法</span><span class="sxs-lookup"><span data-stu-id="11267-104">SYNTAX</span></span>

### <span data-ttu-id="11267-105">DefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="11267-105">DefaultParameterSet (Default)</span></span>
```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-ZoneBalance]
 [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>] [-PlanName <String>] [-PlanPublisher <String>]
 [-PlanProduct <String>] [-PlanPromotionCode <String>] [-RollingUpgradePolicy <RollingUpgradePolicy>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11267-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="11267-106">ExplicitIdentityParameterSet</span></span>
```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
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

### <span data-ttu-id="11267-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="11267-107">AssignIdentityParameterSet</span></span>
```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-ZoneBalance]
 [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>] [-PlanName <String>] [-PlanPublisher <String>]
 [-PlanProduct <String>] [-PlanPromotionCode <String>] [-RollingUpgradePolicy <RollingUpgradePolicy>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-AssignIdentity] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11267-108">說明</span><span class="sxs-lookup"><span data-stu-id="11267-108">DESCRIPTION</span></span>
<span data-ttu-id="11267-109">**新的-AzureRmVmssConfig** Cmdlet 會建立可設定的本機視覺管理員縮放比例集， (VMSS) 物件。</span><span class="sxs-lookup"><span data-stu-id="11267-109">The **New-AzureRmVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="11267-110">需要其他 Cmdlet 來設定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="11267-110">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="11267-111">這些 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="11267-111">These cmdlets are:</span></span>
- <span data-ttu-id="11267-112">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="11267-112">Set-AzureRmVmssOsProfile</span></span>
- <span data-ttu-id="11267-113">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="11267-113">Set-AzureRmVmssStorageProfile</span></span>
- <span data-ttu-id="11267-114">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="11267-114">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="11267-115">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="11267-115">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="11267-116">示例</span><span class="sxs-lookup"><span data-stu-id="11267-116">EXAMPLES</span></span>

### <span data-ttu-id="11267-117">範例1：建立 VMSS 設定物件</span><span class="sxs-lookup"><span data-stu-id="11267-117">Example 1: Create a VMSS configuration object</span></span>
```
PS C:\> $VMSS = New-AzureRmVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic" -NetworkInterfaceConfiguration $NetCfg `
            | Add-AzureRmVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
            | Set-AzureRmVmssOSProfile -ComputerNamePrefix "Test" -AdminUsername $adminUsername -AdminPassword $AdminPassword `
            | Set-AzureRmVmssStorageProfile -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VHDContainer `
            | Add-AzureRmVmssAdditionalUnattendContent -ComponentName  $AUCComponentName -Content  $AUCContent -PassName  $AUCPassName -SettingName  $AUCSetting `
            | Remove-AzureRmVmssAdditionalUnattendContent -ComponentName  $AUCComponentName;

New-AzureRmVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

<span data-ttu-id="11267-118">這個範例會建立 VMSS 設定物件。</span><span class="sxs-lookup"><span data-stu-id="11267-118">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="11267-119">第一個命令使用 **新的 AzureRmVmssConfig** Cmdlet 來建立 VMSS 設定物件，並將結果儲存在名為 $VMSS 的變數中。</span><span class="sxs-lookup"><span data-stu-id="11267-119">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="11267-120">第二個命令使用 **AzureRmVmss** Cmdlet 來建立使用在第一個命令中建立之 VMSS 設定物件的 VMSS。</span><span class="sxs-lookup"><span data-stu-id="11267-120">The second command uses the **New-AzureRmVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="11267-121">參數</span><span class="sxs-lookup"><span data-stu-id="11267-121">PARAMETERS</span></span>

### <span data-ttu-id="11267-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="11267-122">-AssignIdentity</span></span>
<span data-ttu-id="11267-123">指定系統指派的虛擬機器縮放集身分識別。</span><span class="sxs-lookup"><span data-stu-id="11267-123">Specify the system assigned identity for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="11267-124">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="11267-124">-AutoOSUpgrade</span></span>
<span data-ttu-id="11267-125">設定更新版本的影像時，是否應該將作業系統升級自動套用到縮放集實例，以滾動的方式進行。</span><span class="sxs-lookup"><span data-stu-id="11267-125">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="11267-126">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="11267-126">-BootDiagnostic</span></span>
<span data-ttu-id="11267-127">指定虛擬機器縮放設定啟動診斷設定檔。</span><span class="sxs-lookup"><span data-stu-id="11267-127">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="11267-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11267-128">-DefaultProfile</span></span>
<span data-ttu-id="11267-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="11267-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11267-130">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="11267-130">-DisableAutoRollback</span></span>
<span data-ttu-id="11267-131">針對自動 OS 升級原則停用自動復原</span><span class="sxs-lookup"><span data-stu-id="11267-131">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="11267-132">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="11267-132">-EnableUltraSSD</span></span>
<span data-ttu-id="11267-133">可讓一或多個受管理的資料磁片使用一或多個在虛擬機器縮放設定上擁有 UltraSSD_LRS 儲存帳戶類型的功能。</span><span class="sxs-lookup"><span data-stu-id="11267-133">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="11267-134">只有在啟用此屬性時，才能將儲存帳戶類型 UltraSSD_LRS 的受管理磁片新增至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="11267-134">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="11267-135">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="11267-135">-EvictionPolicy</span></span>
<span data-ttu-id="11267-136">針對規模集中的虛擬機器指定逐出原則。</span><span class="sxs-lookup"><span data-stu-id="11267-136">Specifies the eviction policy for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="11267-137">-延伸</span><span class="sxs-lookup"><span data-stu-id="11267-137">-Extension</span></span>
<span data-ttu-id="11267-138">指定 VMSS 的延伸資訊物件。</span><span class="sxs-lookup"><span data-stu-id="11267-138">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="11267-139">您可以使用 **AzureRmVmssExtension** Cmdlet 來新增此物件。</span><span class="sxs-lookup"><span data-stu-id="11267-139">You can use the **Add-AzureRmVmssExtension** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="11267-140">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="11267-140">-HealthProbeId</span></span>
<span data-ttu-id="11267-141">指定負載平衡器探測的識別碼，這些探測器用來判斷虛擬機器規模集中的實例健康情況。</span><span class="sxs-lookup"><span data-stu-id="11267-141">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="11267-142">HealthProbeId 的形式為「/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}」。</span><span class="sxs-lookup"><span data-stu-id="11267-142">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="11267-143">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="11267-143">-IdentityId</span></span>
<span data-ttu-id="11267-144">指定與虛擬機器小性集相關聯的使用者識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="11267-144">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="11267-145">使用者身分識別參照將是下列形式的 ARM 資源識別碼： '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="11267-145">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="11267-146">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="11267-146">-IdentityType</span></span>
<span data-ttu-id="11267-147">指定用於虛擬機器規模集的身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="11267-147">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="11267-148">"SystemAssignedUserAssigned" 類型包含隱含建立的身分識別，以及一組使用者指派的身分識別。</span><span class="sxs-lookup"><span data-stu-id="11267-148">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="11267-149">"None" 類型將會移除虛擬機器小單位集中的任何身分識別。</span><span class="sxs-lookup"><span data-stu-id="11267-149">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="11267-150">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="11267-150">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="11267-151">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="11267-151">SystemAssigned</span></span>
- <span data-ttu-id="11267-152">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="11267-152">UserAssigned</span></span>
- <span data-ttu-id="11267-153">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="11267-153">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="11267-154">所有</span><span class="sxs-lookup"><span data-stu-id="11267-154">None</span></span>

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

### <span data-ttu-id="11267-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="11267-155">-LicenseType</span></span>
<span data-ttu-id="11267-156">指定授權類型，這是用來提供您自己的授權案例。</span><span class="sxs-lookup"><span data-stu-id="11267-156">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="11267-157">-位置</span><span class="sxs-lookup"><span data-stu-id="11267-157">-Location</span></span>
<span data-ttu-id="11267-158">指定建立 VMSS 的 Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="11267-158">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="11267-159">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="11267-159">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="11267-160">指定包含 VMSS 設定之網路屬性的網路設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="11267-160">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="11267-161">您可以使用 **AzureRmVmssNetworkInterfaceConfiguration** Cmdlet 來新增此物件。</span><span class="sxs-lookup"><span data-stu-id="11267-161">You can use the **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="11267-162">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="11267-162">-OsProfile</span></span>
<span data-ttu-id="11267-163">指定作業系統設定檔物件，其中包含 VMSS 設定的作業系統屬性。</span><span class="sxs-lookup"><span data-stu-id="11267-163">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="11267-164">您可以使用 **AzureRmVmssOsProfile** Cmdlet 來設定此物件。</span><span class="sxs-lookup"><span data-stu-id="11267-164">You can use the **Set-AzureRmVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="11267-165">-Overprovision</span><span class="sxs-lookup"><span data-stu-id="11267-165">-Overprovision</span></span>
<span data-ttu-id="11267-166">指示 Cmdlet 是否 overprovisions VMSS。</span><span class="sxs-lookup"><span data-stu-id="11267-166">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="11267-167">-PlanName</span><span class="sxs-lookup"><span data-stu-id="11267-167">-PlanName</span></span>
<span data-ttu-id="11267-168">指定方案名稱。</span><span class="sxs-lookup"><span data-stu-id="11267-168">Specifies the plan name.</span></span>

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

### <span data-ttu-id="11267-169">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="11267-169">-PlanProduct</span></span>
<span data-ttu-id="11267-170">指定方案產品。</span><span class="sxs-lookup"><span data-stu-id="11267-170">Specifies the plan product.</span></span>

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

### <span data-ttu-id="11267-171">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="11267-171">-PlanPromotionCode</span></span>
<span data-ttu-id="11267-172">指定方案促銷代碼。</span><span class="sxs-lookup"><span data-stu-id="11267-172">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="11267-173">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="11267-173">-PlanPublisher</span></span>
<span data-ttu-id="11267-174">指定方案發行者。</span><span class="sxs-lookup"><span data-stu-id="11267-174">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="11267-175">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="11267-175">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="11267-176">每個位置群組的錯誤網域計數。</span><span class="sxs-lookup"><span data-stu-id="11267-176">Fault Domain count for each placement group.</span></span>

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

### <span data-ttu-id="11267-177">-優先順序</span><span class="sxs-lookup"><span data-stu-id="11267-177">-Priority</span></span>
<span data-ttu-id="11267-178">指定規模集中虛擬機器的優先順序。</span><span class="sxs-lookup"><span data-stu-id="11267-178">Specifies the priority for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="11267-179">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="11267-179">-RollingUpgradePolicy</span></span>
<span data-ttu-id="11267-180">指定輪流升級原則。</span><span class="sxs-lookup"><span data-stu-id="11267-180">Specifies the rolling upgrade policy.</span></span>

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

### <span data-ttu-id="11267-181">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="11267-181">-SinglePlacementGroup</span></span>
<span data-ttu-id="11267-182">指定單一位置群組。</span><span class="sxs-lookup"><span data-stu-id="11267-182">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="11267-183">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="11267-183">-SkuCapacity</span></span>
<span data-ttu-id="11267-184">指定 VMSS 中的實例數。</span><span class="sxs-lookup"><span data-stu-id="11267-184">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="11267-185">-SkuName</span><span class="sxs-lookup"><span data-stu-id="11267-185">-SkuName</span></span>
<span data-ttu-id="11267-186">指定 VMSS 的所有實例大小。</span><span class="sxs-lookup"><span data-stu-id="11267-186">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="11267-187">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="11267-187">-SkuTier</span></span>
<span data-ttu-id="11267-188">指定 VMSS 的層級。</span><span class="sxs-lookup"><span data-stu-id="11267-188">Specifies the tier of VMSS.</span></span> <span data-ttu-id="11267-189">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="11267-189">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="11267-190">標準</span><span class="sxs-lookup"><span data-stu-id="11267-190">Standard</span></span>
- <span data-ttu-id="11267-191">空白</span><span class="sxs-lookup"><span data-stu-id="11267-191">Basic</span></span>

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

### <span data-ttu-id="11267-192">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="11267-192">-StorageProfile</span></span>
<span data-ttu-id="11267-193">指定包含 VMSS 設定之磁片摘要資訊的儲存空間物件。</span><span class="sxs-lookup"><span data-stu-id="11267-193">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="11267-194">您可以使用 **AzureRmVmssStorageProfile** Cmdlet 來設定此物件。</span><span class="sxs-lookup"><span data-stu-id="11267-194">You can use the **Set-AzureRmVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="11267-195">-Tag</span><span class="sxs-lookup"><span data-stu-id="11267-195">-Tag</span></span>
<span data-ttu-id="11267-196">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="11267-196">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="11267-197">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="11267-197">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="11267-198">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="11267-198">-UpgradePolicyMode</span></span>
<span data-ttu-id="11267-199">已指定升級模式至規模集中的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="11267-199">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="11267-200">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="11267-200">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="11267-201">自動</span><span class="sxs-lookup"><span data-stu-id="11267-201">Automatic</span></span>
- <span data-ttu-id="11267-202">手動</span><span class="sxs-lookup"><span data-stu-id="11267-202">Manual</span></span>

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

### <span data-ttu-id="11267-203">-Zone</span><span class="sxs-lookup"><span data-stu-id="11267-203">-Zone</span></span>
<span data-ttu-id="11267-204">指定虛擬機器縮放集的區域清單。</span><span class="sxs-lookup"><span data-stu-id="11267-204">Specifies the zone list for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="11267-205">-ZoneBalance</span><span class="sxs-lookup"><span data-stu-id="11267-205">-ZoneBalance</span></span>
<span data-ttu-id="11267-206">在發生區域中斷時，是否要強制嚴格地根據 x 個區域進行虛擬電腦發佈。</span><span class="sxs-lookup"><span data-stu-id="11267-206">Whether to force strictly even Virtual Machine distribution cross x-zones in case there is zone outage.</span></span>

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

### <span data-ttu-id="11267-207">-確認</span><span class="sxs-lookup"><span data-stu-id="11267-207">-Confirm</span></span>
<span data-ttu-id="11267-208">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="11267-208">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11267-209">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11267-209">-WhatIf</span></span>
<span data-ttu-id="11267-210">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="11267-210">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="11267-211">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="11267-211">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11267-212">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11267-212">CommonParameters</span></span>
<span data-ttu-id="11267-213">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="11267-213">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11267-214">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="11267-214">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11267-215">輸入</span><span class="sxs-lookup"><span data-stu-id="11267-215">INPUTS</span></span>

### <span data-ttu-id="11267-216">系統為 Nullable "1 [[System.object，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="11267-216">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="11267-217">System.object</span><span class="sxs-lookup"><span data-stu-id="11267-217">System.String</span></span>

### <span data-ttu-id="11267-218">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="11267-218">System.Collections.Hashtable</span></span>

### <span data-ttu-id="11267-219">System.object</span><span class="sxs-lookup"><span data-stu-id="11267-219">System.Int32</span></span>

### <span data-ttu-id="11267-220">"UpgradeMode" 1 [[21.0.0.0]。計算，版本 =，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]]）。）</span><span class="sxs-lookup"><span data-stu-id="11267-220">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="11267-221">VirtualMachineScaleSetOSProfile 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="11267-221">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span></span>

### <span data-ttu-id="11267-222">VirtualMachineScaleSetStorageProfile 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="11267-222">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span></span>

### <span data-ttu-id="11267-223">VirtualMachineScaleSetNetworkConfiguration [] 的計算模型。</span><span class="sxs-lookup"><span data-stu-id="11267-223">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span></span>

### <span data-ttu-id="11267-224">VirtualMachineScaleSetExtension [] 的計算模型。</span><span class="sxs-lookup"><span data-stu-id="11267-224">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span></span>

### <span data-ttu-id="11267-225">System.object []</span><span class="sxs-lookup"><span data-stu-id="11267-225">System.String[]</span></span>

### <span data-ttu-id="11267-226">RollingUpgradePolicy 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="11267-226">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span></span>

### <span data-ttu-id="11267-227">BootDiagnostics 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="11267-227">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span></span>

### <span data-ttu-id="11267-228">"ResourceIdentityType" 1 [[21.0.0.0]。計算，版本 =，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]]）。）</span><span class="sxs-lookup"><span data-stu-id="11267-228">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="11267-229">輸出</span><span class="sxs-lookup"><span data-stu-id="11267-229">OUTPUTS</span></span>

### <span data-ttu-id="11267-230">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="11267-230">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="11267-231">筆記</span><span class="sxs-lookup"><span data-stu-id="11267-231">NOTES</span></span>

## <span data-ttu-id="11267-232">相關連結</span><span class="sxs-lookup"><span data-stu-id="11267-232">RELATED LINKS</span></span>

[<span data-ttu-id="11267-233">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="11267-233">Set-AzureRmVmssOsProfile</span></span>](./Set-AzureRmVmssOsProfile.md)

[<span data-ttu-id="11267-234">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="11267-234">Set-AzureRmVmssStorageProfile</span></span>](./Set-AzureRmVmssStorageProfile.md)

[<span data-ttu-id="11267-235">附加 AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="11267-235">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="11267-236">附加 AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="11267-236">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)

[<span data-ttu-id="11267-237">新-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="11267-237">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)
