---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: c407ce7147d3eb175fc181b76b140605e463d9a0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796102"
---
# <span data-ttu-id="c7ad6-101">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="c7ad6-101">New-AzVmssConfig</span></span>

## <span data-ttu-id="c7ad6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c7ad6-102">SYNOPSIS</span></span>
<span data-ttu-id="c7ad6-103">建立 VMSS 設定物件。</span><span class="sxs-lookup"><span data-stu-id="c7ad6-103">Creates a VMSS configuration object.</span></span>

## <span data-ttu-id="c7ad6-104">句法</span><span class="sxs-lookup"><span data-stu-id="c7ad6-104">SYNTAX</span></span>

### <span data-ttu-id="c7ad6-105">DefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c7ad6-105">DefaultParameterSet (Default)</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-AutoOSUpgrade] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7ad6-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7ad6-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-AutoOSUpgrade] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7ad6-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7ad6-107">AssignIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-AutoOSUpgrade] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-AssignIdentity]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7ad6-108">說明</span><span class="sxs-lookup"><span data-stu-id="c7ad6-108">DESCRIPTION</span></span>
<span data-ttu-id="c7ad6-109">**新的-AzVmssConfig** Cmdlet 會建立可設定的本機視覺管理員縮放比例集， (VMSS) 物件。</span><span class="sxs-lookup"><span data-stu-id="c7ad6-109">The **New-AzVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="c7ad6-110">需要其他 Cmdlet 來設定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="c7ad6-110">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="c7ad6-111">這些 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="c7ad6-111">These cmdlets are:</span></span>

- <span data-ttu-id="c7ad6-112">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="c7ad6-112">Set-AzVmssOsProfile</span></span>
- <span data-ttu-id="c7ad6-113">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="c7ad6-113">Set-AzVmssStorageProfile</span></span>
- <span data-ttu-id="c7ad6-114">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7ad6-114">Add-AzVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="c7ad6-115">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="c7ad6-115">Add-AzVmssExtension</span></span>

## <span data-ttu-id="c7ad6-116">示例</span><span class="sxs-lookup"><span data-stu-id="c7ad6-116">EXAMPLES</span></span>

### <span data-ttu-id="c7ad6-117">範例1：建立 VMSS 設定物件</span><span class="sxs-lookup"><span data-stu-id="c7ad6-117">Example 1: Create a VMSS configuration object</span></span>
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

<span data-ttu-id="c7ad6-118">這個範例會建立 VMSS 設定物件。</span><span class="sxs-lookup"><span data-stu-id="c7ad6-118">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="c7ad6-119">第一個命令使用 **新的 AzVmssConfig** Cmdlet 來建立 VMSS 設定物件，並將結果儲存在名為 $VMSS 的變數中。</span><span class="sxs-lookup"><span data-stu-id="c7ad6-119">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="c7ad6-120">第二個命令使用 **AzVmss** Cmdlet 來建立使用在第一個命令中建立之 VMSS 設定物件的 VMSS。</span><span class="sxs-lookup"><span data-stu-id="c7ad6-120">The second command uses the **New-AzVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="c7ad6-121">參數</span><span class="sxs-lookup"><span data-stu-id="c7ad6-121">PARAMETERS</span></span>

### <span data-ttu-id="c7ad6-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="c7ad6-122">-AssignIdentity</span></span>
<span data-ttu-id="c7ad6-123">指定系統指派的虛擬機器縮放集身分識別。</span><span class="sxs-lookup"><span data-stu-id="c7ad6-123">Specify the system assigned identity for the virtual machine scale set.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7ad6-124">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="c7ad6-124">-AutoOSUpgrade</span></span>
<span data-ttu-id="c7ad6-125">設定更新版本的影像時，是否應該將作業系統升級自動套用到縮放集實例，以滾動的方式進行。</span><span class="sxs-lookup"><span data-stu-id="c7ad6-125">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="c7ad6-126">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="c7ad6-126">-BootDiagnostic</span></span>
<span data-ttu-id="c7ad6-127">指定虛擬機器縮放設定啟動診斷設定檔。</span><span class="sxs-lookup"><span data-stu-id="c7ad6-127">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

```yaml
Type: BootDiagnostics
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7ad6-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7ad6-128">-DefaultProfile</span></span>
<span data-ttu-id="c7ad6-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c7ad6-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7ad6-130">-延伸</span><span class="sxs-lookup"><span data-stu-id="c7ad6-130">-Extension</span></span>
<span data-ttu-id="c7ad6-131">指定 VMSS 的延伸資訊物件。</span><span class="sxs-lookup"><span data-stu-id="c7ad6-131">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="c7ad6-132">您可以使用 **AzVmssExtension** Cmdlet 來新增此物件。</span><span class="sxs-lookup"><span data-stu-id="c7ad6-132">You can use the **Add-AzVmssExtension** cmdlet to add this object.</span></span>

```yaml
Type: VirtualMachineScaleSetExtension[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7ad6-133">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="c7ad6-133">-HealthProbeId</span></span>
<span data-ttu-id="c7ad6-134">指定負載平衡器探測的識別碼，這些探測器用來判斷虛擬機器規模集中的實例健康情況。</span><span class="sxs-lookup"><span data-stu-id="c7ad6-134">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="c7ad6-135">HealthProbeId 的形式為「/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}」。</span><span class="sxs-lookup"><span data-stu-id="c7ad6-135">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7ad6-136">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="c7ad6-136">-IdentityId</span></span>
<span data-ttu-id="c7ad6-137">指定與虛擬機器小性集相關聯的使用者識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="c7ad6-137">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="c7ad6-138">使用者身分識別參照將是下列形式的 ARM 資源識別碼： '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="c7ad6-138">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7ad6-139">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="c7ad6-139">-IdentityType</span></span>
<span data-ttu-id="c7ad6-140">指定用於虛擬機器規模集的身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="c7ad6-140">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="c7ad6-141">"SystemAssignedUserAssigned" 類型包含隱含建立的身分識別，以及一組使用者指派的身分識別。</span><span class="sxs-lookup"><span data-stu-id="c7ad6-141">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="c7ad6-142">"None" 類型將會移除虛擬機器小單位集中的任何身分識別。</span><span class="sxs-lookup"><span data-stu-id="c7ad6-142">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="c7ad6-143">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="c7ad6-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c7ad6-144">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="c7ad6-144">SystemAssigned</span></span>
- <span data-ttu-id="c7ad6-145">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="c7ad6-145">UserAssigned</span></span>
- <span data-ttu-id="c7ad6-146">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="c7ad6-146">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="c7ad6-147">所有</span><span class="sxs-lookup"><span data-stu-id="c7ad6-147">None</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7ad6-148">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="c7ad6-148">-LicenseType</span></span>
<span data-ttu-id="c7ad6-149">指定授權類型，這是用來提供您自己的授權案例。</span><span class="sxs-lookup"><span data-stu-id="c7ad6-149">Specify the license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7ad6-150">-位置</span><span class="sxs-lookup"><span data-stu-id="c7ad6-150">-Location</span></span>
<span data-ttu-id="c7ad6-151">指定建立 VMSS 的 Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="c7ad6-151">Specifies the Azure location where the VMSS is created.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7ad6-152">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7ad6-152">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="c7ad6-153">指定包含 VMSS 設定之網路屬性的網路設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="c7ad6-153">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="c7ad6-154">您可以使用 **AzVmssNetworkInterfaceConfiguration** Cmdlet 來新增此物件。</span><span class="sxs-lookup"><span data-stu-id="c7ad6-154">You can use the **Add-AzVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

```yaml
Type: VirtualMachineScaleSetNetworkConfiguration[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7ad6-155">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="c7ad6-155">-OsProfile</span></span>
<span data-ttu-id="c7ad6-156">指定作業系統設定檔物件，其中包含 VMSS 設定的作業系統屬性。</span><span class="sxs-lookup"><span data-stu-id="c7ad6-156">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="c7ad6-157">您可以使用 **AzVmssOsProfile** Cmdlet 來設定此物件。</span><span class="sxs-lookup"><span data-stu-id="c7ad6-157">You can use the **Set-AzVmssOsProfile** cmdlet to set this object.</span></span>

```yaml
Type: VirtualMachineScaleSetOSProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7ad6-158">-Overprovision</span><span class="sxs-lookup"><span data-stu-id="c7ad6-158">-Overprovision</span></span>
<span data-ttu-id="c7ad6-159">指示 Cmdlet 是否 overprovisions VMSS。</span><span class="sxs-lookup"><span data-stu-id="c7ad6-159">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7ad6-160">-PlanName</span><span class="sxs-lookup"><span data-stu-id="c7ad6-160">-PlanName</span></span>
<span data-ttu-id="c7ad6-161">指定方案名稱。</span><span class="sxs-lookup"><span data-stu-id="c7ad6-161">Specifies the plan name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7ad6-162">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="c7ad6-162">-PlanProduct</span></span>
<span data-ttu-id="c7ad6-163">指定方案產品。</span><span class="sxs-lookup"><span data-stu-id="c7ad6-163">Specifies the plan product.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7ad6-164">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="c7ad6-164">-PlanPromotionCode</span></span>
<span data-ttu-id="c7ad6-165">指定方案促銷代碼。</span><span class="sxs-lookup"><span data-stu-id="c7ad6-165">Specifies the plan promotion code.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7ad6-166">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="c7ad6-166">-PlanPublisher</span></span>
<span data-ttu-id="c7ad6-167">指定方案發行者。</span><span class="sxs-lookup"><span data-stu-id="c7ad6-167">Specifies the plan publisher.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7ad6-168">-優先順序</span><span class="sxs-lookup"><span data-stu-id="c7ad6-168">-Priority</span></span>
<span data-ttu-id="c7ad6-169">指定規模集中虛擬機器的優先順序。</span><span class="sxs-lookup"><span data-stu-id="c7ad6-169">Specifies the priority for the virtual machines in the scale set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7ad6-170">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="c7ad6-170">-RollingUpgradePolicy</span></span>
<span data-ttu-id="c7ad6-171">指定輪流升級原則。</span><span class="sxs-lookup"><span data-stu-id="c7ad6-171">Specifies the rolling upgrade policy.</span></span>

```yaml
Type: RollingUpgradePolicy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7ad6-172">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="c7ad6-172">-SinglePlacementGroup</span></span>
<span data-ttu-id="c7ad6-173">指定單一位置群組。</span><span class="sxs-lookup"><span data-stu-id="c7ad6-173">Specifies the single placement group.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7ad6-174">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="c7ad6-174">-SkuCapacity</span></span>
<span data-ttu-id="c7ad6-175">指定 VMSS 中的實例數。</span><span class="sxs-lookup"><span data-stu-id="c7ad6-175">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7ad6-176">-SkuName</span><span class="sxs-lookup"><span data-stu-id="c7ad6-176">-SkuName</span></span>
<span data-ttu-id="c7ad6-177">指定 VMSS 的所有實例大小。</span><span class="sxs-lookup"><span data-stu-id="c7ad6-177">Specifies the size of all the instances of VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7ad6-178">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="c7ad6-178">-SkuTier</span></span>
<span data-ttu-id="c7ad6-179">指定 VMSS 的層級。</span><span class="sxs-lookup"><span data-stu-id="c7ad6-179">Specifies the tier of VMSS.</span></span> <span data-ttu-id="c7ad6-180">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="c7ad6-180">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c7ad6-181">標準</span><span class="sxs-lookup"><span data-stu-id="c7ad6-181">Standard</span></span>
- <span data-ttu-id="c7ad6-182">空白</span><span class="sxs-lookup"><span data-stu-id="c7ad6-182">Basic</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7ad6-183">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="c7ad6-183">-StorageProfile</span></span>
<span data-ttu-id="c7ad6-184">指定包含 VMSS 設定之磁片摘要資訊的儲存空間物件。</span><span class="sxs-lookup"><span data-stu-id="c7ad6-184">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="c7ad6-185">您可以使用 **AzVmssStorageProfile** Cmdlet 來設定此物件。</span><span class="sxs-lookup"><span data-stu-id="c7ad6-185">You can use the **Set-AzVmssStorageProfile** cmdlet to set this object.</span></span>

```yaml
Type: VirtualMachineScaleSetStorageProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7ad6-186">-Tag</span><span class="sxs-lookup"><span data-stu-id="c7ad6-186">-Tag</span></span>
<span data-ttu-id="c7ad6-187">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="c7ad6-187">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c7ad6-188">例如：</span><span class="sxs-lookup"><span data-stu-id="c7ad6-188">For example:</span></span>

<span data-ttu-id="c7ad6-189">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="c7ad6-189">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7ad6-190">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="c7ad6-190">-UpgradePolicyMode</span></span>
<span data-ttu-id="c7ad6-191">已指定升級模式至規模集中的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="c7ad6-191">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>

<span data-ttu-id="c7ad6-192">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="c7ad6-192">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c7ad6-193">自動</span><span class="sxs-lookup"><span data-stu-id="c7ad6-193">Automatic</span></span>
- <span data-ttu-id="c7ad6-194">手動</span><span class="sxs-lookup"><span data-stu-id="c7ad6-194">Manual</span></span>

```yaml
Type: UpgradeMode
Parameter Sets: (All)
Aliases: 
Accepted values: Automatic, Manual, Rolling

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7ad6-195">-Zone</span><span class="sxs-lookup"><span data-stu-id="c7ad6-195">-Zone</span></span>
<span data-ttu-id="c7ad6-196">指定虛擬機器縮放集的區域清單。</span><span class="sxs-lookup"><span data-stu-id="c7ad6-196">Specifies the zone list for the virtual machine scale set.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7ad6-197">-確認</span><span class="sxs-lookup"><span data-stu-id="c7ad6-197">-Confirm</span></span>
<span data-ttu-id="c7ad6-198">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c7ad6-198">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7ad6-199">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7ad6-199">-WhatIf</span></span>
<span data-ttu-id="c7ad6-200">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c7ad6-200">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c7ad6-201">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c7ad6-201">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7ad6-202">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7ad6-202">CommonParameters</span></span>
<span data-ttu-id="c7ad6-203">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c7ad6-203">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7ad6-204">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c7ad6-204">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7ad6-205">輸入</span><span class="sxs-lookup"><span data-stu-id="c7ad6-205">INPUTS</span></span>

### <span data-ttu-id="c7ad6-206">所有</span><span class="sxs-lookup"><span data-stu-id="c7ad6-206">None</span></span>
<span data-ttu-id="c7ad6-207">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="c7ad6-207">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c7ad6-208">輸出</span><span class="sxs-lookup"><span data-stu-id="c7ad6-208">OUTPUTS</span></span>

### <span data-ttu-id="c7ad6-209">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="c7ad6-209">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="c7ad6-210">筆記</span><span class="sxs-lookup"><span data-stu-id="c7ad6-210">NOTES</span></span>

## <span data-ttu-id="c7ad6-211">相關連結</span><span class="sxs-lookup"><span data-stu-id="c7ad6-211">RELATED LINKS</span></span>

[<span data-ttu-id="c7ad6-212">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="c7ad6-212">Set-AzVmssOsProfile</span></span>](./Set-AzVmssOsProfile.md)

[<span data-ttu-id="c7ad6-213">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="c7ad6-213">Set-AzVmssStorageProfile</span></span>](./Set-AzVmssStorageProfile.md)

[<span data-ttu-id="c7ad6-214">附加 AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7ad6-214">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="c7ad6-215">附加 AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="c7ad6-215">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="c7ad6-216">新-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c7ad6-216">New-AzVmss</span></span>](./New-AzVmss.md)
