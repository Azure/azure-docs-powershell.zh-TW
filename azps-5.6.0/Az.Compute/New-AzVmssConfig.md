---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: ba44e397aa09834b1371fa9188527a056153017c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911169"
---
# <span data-ttu-id="26f56-101">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="26f56-101">New-AzVmssConfig</span></span>

## <span data-ttu-id="26f56-102">簡介</span><span class="sxs-lookup"><span data-stu-id="26f56-102">SYNOPSIS</span></span>
<span data-ttu-id="26f56-103">建立 VMSS 組組物件。</span><span class="sxs-lookup"><span data-stu-id="26f56-103">Creates a VMSS configuration object.</span></span>

## <span data-ttu-id="26f56-104">語法</span><span class="sxs-lookup"><span data-stu-id="26f56-104">SYNTAX</span></span>

### <span data-ttu-id="26f56-105">DefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="26f56-105">DefaultParameterSet (Default)</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-MaxPrice <Double>] [-TerminateScheduledEvents] [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>]
 [-ProximityPlacementGroupId <String>] [-ScaleInPolicy <String[]>] [-EncryptionAtHost]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26f56-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="26f56-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-MaxPrice <Double>] [-TerminateScheduledEvents] [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>]
 [-ProximityPlacementGroupId <String>] [-ScaleInPolicy <String[]>] -IdentityType <ResourceIdentityType>
 [-IdentityId <String[]>] [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="26f56-107">描述</span><span class="sxs-lookup"><span data-stu-id="26f56-107">DESCRIPTION</span></span>
<span data-ttu-id="26f56-108">**New-Az VmssConfig** Cmdlet 會建立可設定的本地虛擬管理員縮放集 (VMSS) 物件。</span><span class="sxs-lookup"><span data-stu-id="26f56-108">The **New-AzVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="26f56-109">設定 VMSS 物件需要其他 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="26f56-109">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="26f56-110">這些 Cmdlet 為：</span><span class="sxs-lookup"><span data-stu-id="26f56-110">These cmdlets are:</span></span>
- <span data-ttu-id="26f56-111">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="26f56-111">Set-AzVmssOsProfile</span></span>
- <span data-ttu-id="26f56-112">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="26f56-112">Set-AzVmssStorageProfile</span></span>
- <span data-ttu-id="26f56-113">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="26f56-113">Add-AzVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="26f56-114">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="26f56-114">Add-AzVmssExtension</span></span>

## <span data-ttu-id="26f56-115">例子</span><span class="sxs-lookup"><span data-stu-id="26f56-115">EXAMPLES</span></span>

### <span data-ttu-id="26f56-116">範例 1：建立 VMSS 組組物件</span><span class="sxs-lookup"><span data-stu-id="26f56-116">Example 1: Create a VMSS configuration object</span></span>
```powershell
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

<span data-ttu-id="26f56-117">此範例會建立 VMSS 組組物件。</span><span class="sxs-lookup"><span data-stu-id="26f56-117">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="26f56-118">第一個命令使用 **New-Az VmssConfig** Cmdlet 來建立 VMSS 組式物件，並儲存在名為 $VMSS 的變數中。</span><span class="sxs-lookup"><span data-stu-id="26f56-118">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="26f56-119">第二個命令使用 **New-Az Vmss** Cmdlet 來建立使用第一個命令中建立之 VMSS 組式物件的 VMSS。</span><span class="sxs-lookup"><span data-stu-id="26f56-119">The second command uses the **New-AzVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

### <span data-ttu-id="26f56-120">範例 2</span><span class="sxs-lookup"><span data-stu-id="26f56-120">Example 2</span></span>

<span data-ttu-id="26f56-121">建立 VMSS 組組物件。</span><span class="sxs-lookup"><span data-stu-id="26f56-121">Creates a VMSS configuration object.</span></span> <span data-ttu-id="26f56-122"> (自動) </span><span class="sxs-lookup"><span data-stu-id="26f56-122">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzVmssConfig -Location <String> -Overprovision $false -SkuCapacity 2 -SkuName 'Standard_A0' -Tag 'Sql' -UpgradePolicyMode Automatic
```

## <span data-ttu-id="26f56-123">參數</span><span class="sxs-lookup"><span data-stu-id="26f56-123">PARAMETERS</span></span>

### <span data-ttu-id="26f56-124">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="26f56-124">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="26f56-125">由於 VM 上的狀態變更，自動修復暫停的時間量。</span><span class="sxs-lookup"><span data-stu-id="26f56-125">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="26f56-126">狀態變更完成之後，寬限期即開始。</span><span class="sxs-lookup"><span data-stu-id="26f56-126">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="26f56-127">這有助於避免意外或意外維修。</span><span class="sxs-lookup"><span data-stu-id="26f56-127">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="26f56-128">時間長度應該以 ISO 8601 格式指定。</span><span class="sxs-lookup"><span data-stu-id="26f56-128">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="26f56-129">PT30M (允許的寬限期) 30 分鐘，這也是預設值。</span><span class="sxs-lookup"><span data-stu-id="26f56-129">The minimum allowed grace period is 30 minutes (PT30M), which is also the default value.</span></span> <span data-ttu-id="26f56-130">PT90M 的允許寬限期上限為 90 分鐘 (PT90M) 。</span><span class="sxs-lookup"><span data-stu-id="26f56-130">The maximum allowed grace period is 90 minutes (PT90M).</span></span>

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

### <span data-ttu-id="26f56-131">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="26f56-131">-AutoOSUpgrade</span></span>
<span data-ttu-id="26f56-132">設定當有較新版本的影像可用時，是否應該自動將作業系統升級套用至縮放集實例。</span><span class="sxs-lookup"><span data-stu-id="26f56-132">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="26f56-133">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="26f56-133">-BootDiagnostic</span></span>
<span data-ttu-id="26f56-134">指定虛擬機器縮放比例集開機診斷設定檔。</span><span class="sxs-lookup"><span data-stu-id="26f56-134">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="26f56-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26f56-135">-DefaultProfile</span></span>
<span data-ttu-id="26f56-136">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="26f56-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26f56-137">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="26f56-137">-DisableAutoRollback</span></span>
<span data-ttu-id="26f56-138">停用自動作業系統升級策略的自動重回</span><span class="sxs-lookup"><span data-stu-id="26f56-138">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="26f56-139">-EnableAutomaticRepair</span><span class="sxs-lookup"><span data-stu-id="26f56-139">-EnableAutomaticRepair</span></span>
<span data-ttu-id="26f56-140">啟用虛擬機器縮放集上的自動修復。</span><span class="sxs-lookup"><span data-stu-id="26f56-140">Enables automatic repairs on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="26f56-141">-EnableUltrasSD</span><span class="sxs-lookup"><span data-stu-id="26f56-141">-EnableUltraSSD</span></span>
<span data-ttu-id="26f56-142">啟用一或多個受管理的資料存放區，UltraSSD_LRS設定儲存空間帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="26f56-142">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="26f56-143">只有啟用此屬性時，UltraSSD_LRS儲存帳戶類型的受管理磁片才能新增到 VMSS。</span><span class="sxs-lookup"><span data-stu-id="26f56-143">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="26f56-144">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="26f56-144">-EncryptionAtHost</span></span>
<span data-ttu-id="26f56-145">此參數會針對主機本身的所有磁片啟用加密，包括 Resource/Temp 磁片。</span><span class="sxs-lookup"><span data-stu-id="26f56-145">This parameter will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="26f56-146">預設：除非資源的此屬性設為 True，否則會停用主機加密。</span><span class="sxs-lookup"><span data-stu-id="26f56-146">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

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

### <span data-ttu-id="26f56-147">-Policy</span><span class="sxs-lookup"><span data-stu-id="26f56-147">-EvictionPolicy</span></span>
<span data-ttu-id="26f56-148">指定縮放集內虛擬機器的回收政策。</span><span class="sxs-lookup"><span data-stu-id="26f56-148">Specifies the eviction policy for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="26f56-149">-擴充功能</span><span class="sxs-lookup"><span data-stu-id="26f56-149">-Extension</span></span>
<span data-ttu-id="26f56-150">指定 VMSS 的擴充功能資訊物件。</span><span class="sxs-lookup"><span data-stu-id="26f56-150">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="26f56-151">您可以使用 **Add-AzEvssExtension** Cmdlet 來新增此物件。</span><span class="sxs-lookup"><span data-stu-id="26f56-151">You can use the **Add-AzVmssExtension** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="26f56-152">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="26f56-152">-HealthProbeId</span></span>
<span data-ttu-id="26f56-153">指定用來判斷虛擬機器縮放集實例狀況的負載平衡器量值識別碼。</span><span class="sxs-lookup"><span data-stu-id="26f56-153">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="26f56-154">HealthProbeId 的形式為 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/或name}'。</span><span class="sxs-lookup"><span data-stu-id="26f56-154">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="26f56-155">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="26f56-155">-IdentityId</span></span>
<span data-ttu-id="26f56-156">指定與虛擬機器縮放比例集相關聯的使用者身分設定清單。</span><span class="sxs-lookup"><span data-stu-id="26f56-156">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="26f56-157">使用者身分識別參照為表單中的 ARM 資源識別碼：'/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identityies/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="26f56-157">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="26f56-158">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="26f56-158">-IdentityType</span></span>
<span data-ttu-id="26f56-159">指定虛擬機器縮放集所使用的身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="26f56-159">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="26f56-160">"SystemAssignedUserAssigned" 類型包括隱含建立身分識別，以及一組使用者指派的身分識別。</span><span class="sxs-lookup"><span data-stu-id="26f56-160">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="26f56-161">類型為 "None" 會從虛擬機器縮放集移除任何身分。</span><span class="sxs-lookup"><span data-stu-id="26f56-161">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="26f56-162">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="26f56-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="26f56-163">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="26f56-163">SystemAssigned</span></span>
- <span data-ttu-id="26f56-164">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="26f56-164">UserAssigned</span></span>
- <span data-ttu-id="26f56-165">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="26f56-165">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="26f56-166">沒有</span><span class="sxs-lookup"><span data-stu-id="26f56-166">None</span></span>

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

### <span data-ttu-id="26f56-167">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="26f56-167">-LicenseType</span></span>
<span data-ttu-id="26f56-168">指定授權類型，用於顯示您自己的授權案例。</span><span class="sxs-lookup"><span data-stu-id="26f56-168">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="26f56-169">-位置</span><span class="sxs-lookup"><span data-stu-id="26f56-169">-Location</span></span>
<span data-ttu-id="26f56-170">指定建立 VMSS 的 Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="26f56-170">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="26f56-171">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="26f56-171">-MaxPrice</span></span>
<span data-ttu-id="26f56-172">指定您願意支付 Spot VM/VMSS 的最大價格。</span><span class="sxs-lookup"><span data-stu-id="26f56-172">Specifies the maximum price you are willing to pay for a Spot VM/VMSS.</span></span> <span data-ttu-id="26f56-173">此價格為美元。</span><span class="sxs-lookup"><span data-stu-id="26f56-173">This price is in US Dollars.</span></span> <span data-ttu-id="26f56-174">此價格會與 VM 大小的目前 Spot 價格進行比較。</span><span class="sxs-lookup"><span data-stu-id="26f56-174">This price will be compared with the current Spot price for the VM size.</span></span> <span data-ttu-id="26f56-175">此外，在建立/更新 Spot VM/VMSS 時會比較價格，且只有在 maxPrice 大於目前 Spot price 時，作業才能成功。</span><span class="sxs-lookup"><span data-stu-id="26f56-175">Also, the prices are compared at the time of create/update of Spot VM/VMSS and the operation will only succeed if the maxPrice is greater than the current Spot price.</span></span> <span data-ttu-id="26f56-176">如果建立 VM/VMSS 後，目前的 Spot 價格超出 maxPrice，maxPrice 也會用於評估 Spot VM/VMSS。</span><span class="sxs-lookup"><span data-stu-id="26f56-176">The maxPrice will also be used for evicting a Spot VM/VMSS if the current Spot price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="26f56-177">可能的值為：任何大於零的十進位值。</span><span class="sxs-lookup"><span data-stu-id="26f56-177">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="26f56-178">範例：0.01538。</span><span class="sxs-lookup"><span data-stu-id="26f56-178">Example: 0.01538.</span></span>  <span data-ttu-id="26f56-179">-1 表示基於價格考慮，請勿將 Spot VM/VMSS 從系統退出。</span><span class="sxs-lookup"><span data-stu-id="26f56-179">-1 indicates that the Spot VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="26f56-180">此外，如果您未提供，預設最高價格為 -1。</span><span class="sxs-lookup"><span data-stu-id="26f56-180">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="26f56-181">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="26f56-181">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="26f56-182">指定包含 VMSS 組式網路屬性的網路設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="26f56-182">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="26f56-183">您可以使用 **Add-AzEvssNetworkInterfaceConfiguration** Cmdlet 來新增此物件。</span><span class="sxs-lookup"><span data-stu-id="26f56-183">You can use the **Add-AzVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="26f56-184">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="26f56-184">-OsProfile</span></span>
<span data-ttu-id="26f56-185">指定包含 VMSS 組配置之作業系統屬性的作業系統設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="26f56-185">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="26f56-186">您可以使用 **Set-AzEvssOsProfile** Cmdlet 來設定此物件。</span><span class="sxs-lookup"><span data-stu-id="26f56-186">You can use the **Set-AzVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="26f56-187">-過度配置</span><span class="sxs-lookup"><span data-stu-id="26f56-187">-Overprovision</span></span>
<span data-ttu-id="26f56-188">指出 Cmdlet 是否過度配置 VMSS。</span><span class="sxs-lookup"><span data-stu-id="26f56-188">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="26f56-189">-PlanName</span><span class="sxs-lookup"><span data-stu-id="26f56-189">-PlanName</span></span>
<span data-ttu-id="26f56-190">指定計劃名稱。</span><span class="sxs-lookup"><span data-stu-id="26f56-190">Specifies the plan name.</span></span>

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

### <span data-ttu-id="26f56-191">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="26f56-191">-PlanProduct</span></span>
<span data-ttu-id="26f56-192">指定計劃產品。</span><span class="sxs-lookup"><span data-stu-id="26f56-192">Specifies the plan product.</span></span>

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

### <span data-ttu-id="26f56-193">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="26f56-193">-PlanPromotionCode</span></span>
<span data-ttu-id="26f56-194">指定方案促銷代碼。</span><span class="sxs-lookup"><span data-stu-id="26f56-194">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="26f56-195">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="26f56-195">-PlanPublisher</span></span>
<span data-ttu-id="26f56-196">指定計劃發行者。</span><span class="sxs-lookup"><span data-stu-id="26f56-196">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="26f56-197">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="26f56-197">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="26f56-198">每個位置群組的故障網域計數。</span><span class="sxs-lookup"><span data-stu-id="26f56-198">Fault Domain count for each placement group.</span></span>

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

### <span data-ttu-id="26f56-199">-優先順序</span><span class="sxs-lookup"><span data-stu-id="26f56-199">-Priority</span></span>
<span data-ttu-id="26f56-200">縮放集虛擬 machien 的優先順序。</span><span class="sxs-lookup"><span data-stu-id="26f56-200">The priority for the virtual machien in the scale set.</span></span>  <span data-ttu-id="26f56-201">只有支援的值是 "Regular"、'Spot' 和 'Low'。</span><span class="sxs-lookup"><span data-stu-id="26f56-201">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="26f56-202">"Regular" 適用于一般虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="26f56-202">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="26f56-203">"Spot" 適用于 Spot 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="26f56-203">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="26f56-204">"Low" 也適用于 Spot 虛擬機器，但會由 "Spot" 取代。</span><span class="sxs-lookup"><span data-stu-id="26f56-204">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="26f56-205">請使用 "Spot" 而不是 "Low"。</span><span class="sxs-lookup"><span data-stu-id="26f56-205">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="26f56-206">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="26f56-206">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="26f56-207">要用於此縮放集的鄰近位置群組資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="26f56-207">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="26f56-208">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="26f56-208">-RollingUpgradePolicy</span></span>
<span data-ttu-id="26f56-209">指定輪流升級政策。</span><span class="sxs-lookup"><span data-stu-id="26f56-209">Specifies the rolling upgrade policy.</span></span>

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

### <span data-ttu-id="26f56-210">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="26f56-210">-ScaleInPolicy</span></span>
<span data-ttu-id="26f56-211">縮放虛擬機器縮放比例集時要遵循的規則。</span><span class="sxs-lookup"><span data-stu-id="26f56-211">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="26f56-212">可能的值為：「Default」、'Oldest%。以及'Newest%。。」</span><span class="sxs-lookup"><span data-stu-id="26f56-212">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="26f56-213">當虛擬機器縮放集已調整為比例時，如果這是一個分區比例集，則縮放集會先跨區域進行平衡的預設值。</span><span class="sxs-lookup"><span data-stu-id="26f56-213">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="26f56-214">然後，它會盡可能跨錯誤網域進行平衡。</span><span class="sxs-lookup"><span data-stu-id="26f56-214">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="26f56-215">在每個錯誤網域中，選擇移除的虛擬機器都是不受縮放保護的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="26f56-215">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="26f56-216">當虛擬機器縮放集進行縮放時，會選擇最舊、不受縮放保護的虛擬機器進行移除。</span><span class="sxs-lookup"><span data-stu-id="26f56-216">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="26f56-217">對於分區虛擬機器縮放集，縮放集會先跨區域平衡。</span><span class="sxs-lookup"><span data-stu-id="26f56-217">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="26f56-218">在每個區域中，會選擇最舊的未受到保護的虛擬機器進行移除。</span><span class="sxs-lookup"><span data-stu-id="26f56-218">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="26f56-219">當虛擬機器縮放集進行縮放時，將會選擇不受縮放保護的最新的虛擬機器，以移除最新的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="26f56-219">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="26f56-220">對於分區虛擬機器縮放集，縮放集會先跨區域平衡。</span><span class="sxs-lookup"><span data-stu-id="26f56-220">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="26f56-221">在每個區域中，系統將會選擇最新的未受到保護的虛擬機器進行移除。</span><span class="sxs-lookup"><span data-stu-id="26f56-221">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

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

### <span data-ttu-id="26f56-222">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="26f56-222">-SinglePlacementGroup</span></span>
<span data-ttu-id="26f56-223">指定單一位置群組。</span><span class="sxs-lookup"><span data-stu-id="26f56-223">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="26f56-224">-SkipExtensionsOnOverprovisionedVMS</span><span class="sxs-lookup"><span data-stu-id="26f56-224">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="26f56-225">指定擴充功能不會在額外過度配置之虛擬機器上執行。</span><span class="sxs-lookup"><span data-stu-id="26f56-225">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="26f56-226">-Sku以</span><span class="sxs-lookup"><span data-stu-id="26f56-226">-SkuCapacity</span></span>
<span data-ttu-id="26f56-227">指定 VMSS 中的實例數目。</span><span class="sxs-lookup"><span data-stu-id="26f56-227">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="26f56-228">-SKUName</span><span class="sxs-lookup"><span data-stu-id="26f56-228">-SkuName</span></span>
<span data-ttu-id="26f56-229">指定 VMSS 所有實例的大小。</span><span class="sxs-lookup"><span data-stu-id="26f56-229">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="26f56-230">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="26f56-230">-SkuTier</span></span>
<span data-ttu-id="26f56-231">指定 VMSS 的層級。</span><span class="sxs-lookup"><span data-stu-id="26f56-231">Specifies the tier of VMSS.</span></span> <span data-ttu-id="26f56-232">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="26f56-232">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="26f56-233">標準</span><span class="sxs-lookup"><span data-stu-id="26f56-233">Standard</span></span>
- <span data-ttu-id="26f56-234">基本</span><span class="sxs-lookup"><span data-stu-id="26f56-234">Basic</span></span>

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

### <span data-ttu-id="26f56-235">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="26f56-235">-StorageProfile</span></span>
<span data-ttu-id="26f56-236">指定包含 VMSS 組調之磁片屬性的儲存設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="26f56-236">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="26f56-237">您可以使用 **Set-AzEvssstorageProfile** Cmdlet 來設定此物件。</span><span class="sxs-lookup"><span data-stu-id="26f56-237">You can use the **Set-AzVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="26f56-238">-標記</span><span class="sxs-lookup"><span data-stu-id="26f56-238">-Tag</span></span>
<span data-ttu-id="26f56-239">以雜湊表格形式建立索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="26f56-239">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="26f56-240">例如：@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="26f56-240">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="26f56-241">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="26f56-241">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="26f56-242">刪除的虛擬機器 (分鐘數) 在事件自動核准之前 (終止已排程事件) 。</span><span class="sxs-lookup"><span data-stu-id="26f56-242">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="26f56-243">-終止ScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="26f56-243">-TerminateScheduledEvents</span></span>
<span data-ttu-id="26f56-244">啟用終止已排程事件</span><span class="sxs-lookup"><span data-stu-id="26f56-244">Enable the Terminate Scheduled events</span></span>

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

### <span data-ttu-id="26f56-245">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="26f56-245">-UpgradePolicyMode</span></span>
<span data-ttu-id="26f56-246">指定縮放集的虛擬機器升級模式。</span><span class="sxs-lookup"><span data-stu-id="26f56-246">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="26f56-247">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="26f56-247">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="26f56-248">自動</span><span class="sxs-lookup"><span data-stu-id="26f56-248">Automatic</span></span>
- <span data-ttu-id="26f56-249">手動</span><span class="sxs-lookup"><span data-stu-id="26f56-249">Manual</span></span>

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

### <span data-ttu-id="26f56-250">-區域</span><span class="sxs-lookup"><span data-stu-id="26f56-250">-Zone</span></span>
<span data-ttu-id="26f56-251">指定虛擬機器縮放集的區域清單。</span><span class="sxs-lookup"><span data-stu-id="26f56-251">Specifies the zone list for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="26f56-252">-ZoneBalance</span><span class="sxs-lookup"><span data-stu-id="26f56-252">-ZoneBalance</span></span>
<span data-ttu-id="26f56-253">是否強制強制甚至虛擬機器發佈跨 x 區域，以防發生區域中斷。</span><span class="sxs-lookup"><span data-stu-id="26f56-253">Whether to force strictly even Virtual Machine distribution cross x-zones in case there is zone outage.</span></span>

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

### <span data-ttu-id="26f56-254">-確認</span><span class="sxs-lookup"><span data-stu-id="26f56-254">-Confirm</span></span>
<span data-ttu-id="26f56-255">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="26f56-255">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26f56-256">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26f56-256">-WhatIf</span></span>
<span data-ttu-id="26f56-257">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="26f56-257">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="26f56-258">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="26f56-258">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26f56-259">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26f56-259">CommonParameters</span></span>
<span data-ttu-id="26f56-260">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="26f56-260">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26f56-261">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="26f56-261">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26f56-262">輸入</span><span class="sxs-lookup"><span data-stu-id="26f56-262">INPUTS</span></span>

### <span data-ttu-id="26f56-263">System.Nullable'1[[System.Boolean， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="26f56-263">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="26f56-264">System.String</span><span class="sxs-lookup"><span data-stu-id="26f56-264">System.String</span></span>

### <span data-ttu-id="26f56-265">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="26f56-265">System.Collections.Hashtable</span></span>

### <span data-ttu-id="26f56-266">System.Int32</span><span class="sxs-lookup"><span data-stu-id="26f56-266">System.Int32</span></span>

### <span data-ttu-id="26f56-267">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="26f56-267">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="26f56-268">Microsoft.Azure.management.Compute.models.VirtualMachineScaleSetOSProfile</span><span class="sxs-lookup"><span data-stu-id="26f56-268">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span></span>

### <span data-ttu-id="26f56-269">Microsoft.Azure.management.Compute.models.VirtualMachineScaleSetStorageProfile</span><span class="sxs-lookup"><span data-stu-id="26f56-269">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span></span>

### <span data-ttu-id="26f56-270">Microsoft.Azure.management.Compute.models.VirtualMachineScaleSetworkConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="26f56-270">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span></span>

### <span data-ttu-id="26f56-271">Microsoft.Azure.management.Compute.models.VirtualMachineScaleSetExtension[]</span><span class="sxs-lookup"><span data-stu-id="26f56-271">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span></span>

### <span data-ttu-id="26f56-272">System.String[]</span><span class="sxs-lookup"><span data-stu-id="26f56-272">System.String[]</span></span>

### <span data-ttu-id="26f56-273">Microsoft.Azure.management.Compute.models.RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="26f56-273">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span></span>

### <span data-ttu-id="26f56-274">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="26f56-274">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="26f56-275">Microsoft.Azure.management.Compute.models.BootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="26f56-275">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span></span>

### <span data-ttu-id="26f56-276">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="26f56-276">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="26f56-277">輸出</span><span class="sxs-lookup"><span data-stu-id="26f56-277">OUTPUTS</span></span>

### <span data-ttu-id="26f56-278">Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="26f56-278">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="26f56-279">筆記</span><span class="sxs-lookup"><span data-stu-id="26f56-279">NOTES</span></span>

## <span data-ttu-id="26f56-280">相關連結</span><span class="sxs-lookup"><span data-stu-id="26f56-280">RELATED LINKS</span></span>

[<span data-ttu-id="26f56-281">Set-AzEvssOsProfile</span><span class="sxs-lookup"><span data-stu-id="26f56-281">Set-AzVmssOsProfile</span></span>](./Set-AzVmssOsProfile.md)

[<span data-ttu-id="26f56-282">Set-AzEvssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="26f56-282">Set-AzVmssStorageProfile</span></span>](./Set-AzVmssStorageProfile.md)

[<span data-ttu-id="26f56-283">Add-AzEvssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="26f56-283">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="26f56-284">Add-AzEvssExtension</span><span class="sxs-lookup"><span data-stu-id="26f56-284">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="26f56-285">New-AzEvss</span><span class="sxs-lookup"><span data-stu-id="26f56-285">New-AzVmss</span></span>](./New-AzVmss.md)
