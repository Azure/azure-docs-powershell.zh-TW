---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssConfig.md
ms.openlocfilehash: 3229f1e09cca1b32b62e5b7233806b20ed8ed78e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626018"
---
# <span data-ttu-id="ea074-101">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="ea074-101">New-AzureRmVmssConfig</span></span>

## <span data-ttu-id="ea074-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ea074-102">SYNOPSIS</span></span>
<span data-ttu-id="ea074-103">建立 VMSS 設定物件。</span><span class="sxs-lookup"><span data-stu-id="ea074-103">Creates a VMSS configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea074-104">句法</span><span class="sxs-lookup"><span data-stu-id="ea074-104">SYNTAX</span></span>

```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int64>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-AutoOSUpgrade] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-AssignIdentity]
 [-IdentityType <ResourceIdentityType>] [-RecoveryPolicyMode <RecoveryMode>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea074-105">說明</span><span class="sxs-lookup"><span data-stu-id="ea074-105">DESCRIPTION</span></span>
<span data-ttu-id="ea074-106">**新的-AzureRmVmssConfig** Cmdlet 會建立可設定的本機視覺管理員縮放比例集， (VMSS) 物件。</span><span class="sxs-lookup"><span data-stu-id="ea074-106">The **New-AzureRmVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span>
<span data-ttu-id="ea074-107">需要其他 Cmdlet 來設定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="ea074-107">Other cmdlets are needed to configure the VMSS object.</span></span>
<span data-ttu-id="ea074-108">這些 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="ea074-108">These cmdlets are:</span></span>

- <span data-ttu-id="ea074-109">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="ea074-109">Set-AzureRmVmssOsProfile</span></span>
- <span data-ttu-id="ea074-110">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="ea074-110">Set-AzureRmVmssStorageProfile</span></span>
- <span data-ttu-id="ea074-111">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="ea074-111">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="ea074-112">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="ea074-112">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="ea074-113">示例</span><span class="sxs-lookup"><span data-stu-id="ea074-113">EXAMPLES</span></span>

### <span data-ttu-id="ea074-114">範例1：建立 VMSS 設定物件</span><span class="sxs-lookup"><span data-stu-id="ea074-114">Example 1: Create a VMSS configuration object</span></span>
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

<span data-ttu-id="ea074-115">這個範例會建立 VMSS 設定物件。</span><span class="sxs-lookup"><span data-stu-id="ea074-115">This example creates a VMSS configuration object.</span></span>
<span data-ttu-id="ea074-116">第一個命令使用 **新的 AzureRmVmssConfig** Cmdlet 來建立 VMSS 設定物件，並將結果儲存在名為 $VMSS 的變數中。</span><span class="sxs-lookup"><span data-stu-id="ea074-116">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="ea074-117">第二個命令使用 **AzureRmVmss** Cmdlet 來建立使用在第一個命令中建立之 VMSS 設定物件的 VMSS。</span><span class="sxs-lookup"><span data-stu-id="ea074-117">The second command uses the **New-AzureRmVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="ea074-118">參數</span><span class="sxs-lookup"><span data-stu-id="ea074-118">PARAMETERS</span></span>

### <span data-ttu-id="ea074-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="ea074-119">-AssignIdentity</span></span>
<span data-ttu-id="ea074-120">指定系統指派的虛擬機器縮放集身分識別。</span><span class="sxs-lookup"><span data-stu-id="ea074-120">Specify the system assigned identity for the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea074-121">-AutoOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="ea074-121">-AutoOSUpgrade</span></span>
<span data-ttu-id="ea074-122">設定更新版本的影像時，是否應該將作業系統升級自動套用到縮放集實例，以滾動的方式進行。</span><span class="sxs-lookup"><span data-stu-id="ea074-122">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea074-123">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="ea074-123">-BootDiagnostic</span></span>
<span data-ttu-id="ea074-124">指定虛擬機器縮放設定啟動診斷設定檔。</span><span class="sxs-lookup"><span data-stu-id="ea074-124">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="ea074-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea074-125">-DefaultProfile</span></span>
<span data-ttu-id="ea074-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ea074-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea074-127">-延伸</span><span class="sxs-lookup"><span data-stu-id="ea074-127">-Extension</span></span>
<span data-ttu-id="ea074-128">指定 VMSS 的延伸資訊物件。</span><span class="sxs-lookup"><span data-stu-id="ea074-128">Specifies the extension information object for the VMSS.</span></span>
<span data-ttu-id="ea074-129">您可以使用 **AzureRmVmssExtension** Cmdlet 來新增此物件。</span><span class="sxs-lookup"><span data-stu-id="ea074-129">You can use the **Add-AzureRmVmssExtension** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="ea074-130">-HealthProbeId</span><span class="sxs-lookup"><span data-stu-id="ea074-130">-HealthProbeId</span></span>
<span data-ttu-id="ea074-131">指定負載平衡器探測的識別碼，這些探測器用來判斷虛擬機器規模集中的實例健康情況。</span><span class="sxs-lookup"><span data-stu-id="ea074-131">Specify the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span> <span data-ttu-id="ea074-132">HealthProbeId 的形式為「/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}」。</span><span class="sxs-lookup"><span data-stu-id="ea074-132">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="ea074-133">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="ea074-133">-IdentityType</span></span>
<span data-ttu-id="ea074-134">指定虛擬機器規模集的身分識別（如果已設定）。</span><span class="sxs-lookup"><span data-stu-id="ea074-134">Specify the identity of the virtual machine scale set, if configured.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: (All)
Aliases: 
Accepted values: SystemAssigned

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea074-135">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="ea074-135">-LicenseType</span></span>
<span data-ttu-id="ea074-136">指定授權類型，這是用來提供您自己的授權案例。</span><span class="sxs-lookup"><span data-stu-id="ea074-136">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="ea074-137">-位置</span><span class="sxs-lookup"><span data-stu-id="ea074-137">-Location</span></span>
<span data-ttu-id="ea074-138">指定建立 VMSS 的 Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="ea074-138">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="ea074-139">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="ea074-139">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="ea074-140">指定包含 VMSS 設定之網路屬性的網路設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="ea074-140">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="ea074-141">您可以使用 **AzureRmVmssNetworkInterfaceConfiguration** Cmdlet 來新增此物件。</span><span class="sxs-lookup"><span data-stu-id="ea074-141">You can use the **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="ea074-142">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="ea074-142">-OsProfile</span></span>
<span data-ttu-id="ea074-143">指定作業系統設定檔物件，其中包含 VMSS 設定的作業系統屬性。</span><span class="sxs-lookup"><span data-stu-id="ea074-143">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="ea074-144">您可以使用 **AzureRmVmssOsProfile** Cmdlet 來設定此物件。</span><span class="sxs-lookup"><span data-stu-id="ea074-144">You can use the **Set-AzureRmVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="ea074-145">-Overprovision</span><span class="sxs-lookup"><span data-stu-id="ea074-145">-Overprovision</span></span>
<span data-ttu-id="ea074-146">指示 Cmdlet 是否 overprovisions VMSS。</span><span class="sxs-lookup"><span data-stu-id="ea074-146">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="ea074-147">-PlanName</span><span class="sxs-lookup"><span data-stu-id="ea074-147">-PlanName</span></span>
<span data-ttu-id="ea074-148">指定方案名稱。</span><span class="sxs-lookup"><span data-stu-id="ea074-148">Specifies the plan name.</span></span>

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

### <span data-ttu-id="ea074-149">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="ea074-149">-PlanProduct</span></span>
<span data-ttu-id="ea074-150">指定方案產品。</span><span class="sxs-lookup"><span data-stu-id="ea074-150">Specifies the plan product.</span></span>

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

### <span data-ttu-id="ea074-151">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="ea074-151">-PlanPromotionCode</span></span>
<span data-ttu-id="ea074-152">指定方案促銷代碼。</span><span class="sxs-lookup"><span data-stu-id="ea074-152">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="ea074-153">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="ea074-153">-PlanPublisher</span></span>
<span data-ttu-id="ea074-154">指定方案發行者。</span><span class="sxs-lookup"><span data-stu-id="ea074-154">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="ea074-155">-RecoveryPolicyMode</span><span class="sxs-lookup"><span data-stu-id="ea074-155">-RecoveryPolicyMode</span></span>
<span data-ttu-id="ea074-156">指定損毀修復原則。</span><span class="sxs-lookup"><span data-stu-id="ea074-156">Specify the recovery policy.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Compute.Automation.RecoveryMode]
Parameter Sets: (All)
Aliases: 
Accepted values: None, OverProvision, Reprovision

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea074-157">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="ea074-157">-RollingUpgradePolicy</span></span>
<span data-ttu-id="ea074-158">指定輪流升級原則。</span><span class="sxs-lookup"><span data-stu-id="ea074-158">Specifies the rolling upgrade policy.</span></span>

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

### <span data-ttu-id="ea074-159">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="ea074-159">-SinglePlacementGroup</span></span>
<span data-ttu-id="ea074-160">指定單一位置群組。</span><span class="sxs-lookup"><span data-stu-id="ea074-160">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="ea074-161">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="ea074-161">-SkuCapacity</span></span>
<span data-ttu-id="ea074-162">指定 VMSS 中的實例數。</span><span class="sxs-lookup"><span data-stu-id="ea074-162">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea074-163">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ea074-163">-SkuName</span></span>
<span data-ttu-id="ea074-164">指定 VMSS 的所有實例大小。</span><span class="sxs-lookup"><span data-stu-id="ea074-164">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="ea074-165">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="ea074-165">-SkuTier</span></span>
<span data-ttu-id="ea074-166">指定 VMSS 的層級。</span><span class="sxs-lookup"><span data-stu-id="ea074-166">Specifies the tier of VMSS.</span></span>

<span data-ttu-id="ea074-167">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ea074-167">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ea074-168">標準</span><span class="sxs-lookup"><span data-stu-id="ea074-168">Standard</span></span>
- <span data-ttu-id="ea074-169">空白</span><span class="sxs-lookup"><span data-stu-id="ea074-169">Basic</span></span>

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

### <span data-ttu-id="ea074-170">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="ea074-170">-StorageProfile</span></span>
<span data-ttu-id="ea074-171">指定包含 VMSS 設定之磁片摘要資訊的儲存空間物件。</span><span class="sxs-lookup"><span data-stu-id="ea074-171">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="ea074-172">您可以使用 **AzureRmVmssStorageProfile** Cmdlet 來設定此物件。</span><span class="sxs-lookup"><span data-stu-id="ea074-172">You can use the **Set-AzureRmVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="ea074-173">-Tag</span><span class="sxs-lookup"><span data-stu-id="ea074-173">-Tag</span></span>
<span data-ttu-id="ea074-174">指定將指派給 VMSS 的標記。</span><span class="sxs-lookup"><span data-stu-id="ea074-174">Specifies the tags that will be assigned to the VMSS.</span></span>

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

### <span data-ttu-id="ea074-175">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="ea074-175">-UpgradePolicyMode</span></span>
<span data-ttu-id="ea074-176">已指定升級模式至規模集中的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="ea074-176">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>

<span data-ttu-id="ea074-177">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ea074-177">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ea074-178">自動</span><span class="sxs-lookup"><span data-stu-id="ea074-178">Automatic</span></span>
- <span data-ttu-id="ea074-179">手動</span><span class="sxs-lookup"><span data-stu-id="ea074-179">Manual</span></span>

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

### <span data-ttu-id="ea074-180">-Zone</span><span class="sxs-lookup"><span data-stu-id="ea074-180">-Zone</span></span>
<span data-ttu-id="ea074-181">指定虛擬機器縮放集的區域清單。</span><span class="sxs-lookup"><span data-stu-id="ea074-181">Specifies the zone list for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="ea074-182">-確認</span><span class="sxs-lookup"><span data-stu-id="ea074-182">-Confirm</span></span>
<span data-ttu-id="ea074-183">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ea074-183">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea074-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea074-184">-WhatIf</span></span>
<span data-ttu-id="ea074-185">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ea074-185">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ea074-186">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ea074-186">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea074-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea074-187">CommonParameters</span></span>
<span data-ttu-id="ea074-188">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ea074-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea074-189">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ea074-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea074-190">輸入</span><span class="sxs-lookup"><span data-stu-id="ea074-190">INPUTS</span></span>

## <span data-ttu-id="ea074-191">輸出</span><span class="sxs-lookup"><span data-stu-id="ea074-191">OUTPUTS</span></span>

### <span data-ttu-id="ea074-192">這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="ea074-192">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="ea074-193">筆記</span><span class="sxs-lookup"><span data-stu-id="ea074-193">NOTES</span></span>

## <span data-ttu-id="ea074-194">相關連結</span><span class="sxs-lookup"><span data-stu-id="ea074-194">RELATED LINKS</span></span>

[<span data-ttu-id="ea074-195">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="ea074-195">Set-AzureRmVmssOsProfile</span></span>](./Set-AzureRmVmssOsProfile.md)

[<span data-ttu-id="ea074-196">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="ea074-196">Set-AzureRmVmssStorageProfile</span></span>](./Set-AzureRmVmssStorageProfile.md)

[<span data-ttu-id="ea074-197">附加 AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="ea074-197">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="ea074-198">附加 AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="ea074-198">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)

[<span data-ttu-id="ea074-199">新-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ea074-199">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)


