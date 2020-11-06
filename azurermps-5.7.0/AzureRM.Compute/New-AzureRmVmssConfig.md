---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssConfig.md
ms.openlocfilehash: 4b87c121368232769672c24bc5005f3a50bfd39a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447855"
---
# <span data-ttu-id="cb463-101">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="cb463-101">New-AzureRmVmssConfig</span></span>

## <span data-ttu-id="cb463-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cb463-102">SYNOPSIS</span></span>
<span data-ttu-id="cb463-103">建立 VMSS 設定物件。</span><span class="sxs-lookup"><span data-stu-id="cb463-103">Creates a VMSS configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb463-104">句法</span><span class="sxs-lookup"><span data-stu-id="cb463-104">SYNTAX</span></span>

```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int64>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-PlanName <String>]
 [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RecoveryPolicyMode <RecoveryMode>] [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>]
 [-IdentityType <ResourceIdentityType>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb463-105">說明</span><span class="sxs-lookup"><span data-stu-id="cb463-105">DESCRIPTION</span></span>
<span data-ttu-id="cb463-106">**新的-AzureRmVmssConfig** Cmdlet 會建立可設定的本機視覺管理員縮放比例集， (VMSS) 物件。</span><span class="sxs-lookup"><span data-stu-id="cb463-106">The **New-AzureRmVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span>
<span data-ttu-id="cb463-107">需要其他 Cmdlet 來設定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="cb463-107">Other cmdlets are needed to configure the VMSS object.</span></span>
<span data-ttu-id="cb463-108">這些 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="cb463-108">These cmdlets are:</span></span>

- <span data-ttu-id="cb463-109">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="cb463-109">Set-AzureRmVmssOsProfile</span></span>
- <span data-ttu-id="cb463-110">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="cb463-110">Set-AzureRmVmssStorageProfile</span></span>
- <span data-ttu-id="cb463-111">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb463-111">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="cb463-112">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="cb463-112">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="cb463-113">示例</span><span class="sxs-lookup"><span data-stu-id="cb463-113">EXAMPLES</span></span>

### <span data-ttu-id="cb463-114">範例1：建立 VMSS 設定物件</span><span class="sxs-lookup"><span data-stu-id="cb463-114">Example 1: Create a VMSS configuration object</span></span>
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

<span data-ttu-id="cb463-115">這個範例會建立 VMSS 設定物件。</span><span class="sxs-lookup"><span data-stu-id="cb463-115">This example creates a VMSS configuration object.</span></span>
<span data-ttu-id="cb463-116">第一個命令使用 **新的 AzureRmVmssConfig** Cmdlet 來建立 VMSS 設定物件，並將結果儲存在名為 $VMSS 的變數中。</span><span class="sxs-lookup"><span data-stu-id="cb463-116">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="cb463-117">第二個命令使用 **AzureRmVmss** Cmdlet 來建立使用在第一個命令中建立之 VMSS 設定物件的 VMSS。</span><span class="sxs-lookup"><span data-stu-id="cb463-117">The second command uses the **New-AzureRmVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="cb463-118">參數</span><span class="sxs-lookup"><span data-stu-id="cb463-118">PARAMETERS</span></span>

### <span data-ttu-id="cb463-119">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="cb463-119">-BootDiagnostic</span></span>
<span data-ttu-id="cb463-120">指定虛擬機器縮放設定啟動診斷設定檔。</span><span class="sxs-lookup"><span data-stu-id="cb463-120">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="cb463-121">-延伸</span><span class="sxs-lookup"><span data-stu-id="cb463-121">-Extension</span></span>
<span data-ttu-id="cb463-122">指定 VMSS 的延伸資訊物件。</span><span class="sxs-lookup"><span data-stu-id="cb463-122">Specifies the extension information object for the VMSS.</span></span>
<span data-ttu-id="cb463-123">您可以使用 **AzureRmVmssExtension** Cmdlet 來新增此物件。</span><span class="sxs-lookup"><span data-stu-id="cb463-123">You can use the **Add-AzureRmVmssExtension** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="cb463-124">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="cb463-124">-IdentityType</span></span>
<span data-ttu-id="cb463-125">指定虛擬機器規模集的身分識別（如果已設定）。</span><span class="sxs-lookup"><span data-stu-id="cb463-125">Specify the identity of the virtual machine scale set, if configured.</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb463-126">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="cb463-126">-LicenseType</span></span>
<span data-ttu-id="cb463-127">指定授權類型，這是用來提供您自己的授權案例。</span><span class="sxs-lookup"><span data-stu-id="cb463-127">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="cb463-128">-位置</span><span class="sxs-lookup"><span data-stu-id="cb463-128">-Location</span></span>
<span data-ttu-id="cb463-129">指定建立 VMSS 的 Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="cb463-129">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="cb463-130">-NetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb463-130">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="cb463-131">指定包含 VMSS 設定之網路屬性的網路設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="cb463-131">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="cb463-132">您可以使用 **AzureRmVmssNetworkInterfaceConfiguration** Cmdlet 來新增此物件。</span><span class="sxs-lookup"><span data-stu-id="cb463-132">You can use the **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="cb463-133">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="cb463-133">-OsProfile</span></span>
<span data-ttu-id="cb463-134">指定作業系統設定檔物件，其中包含 VMSS 設定的作業系統屬性。</span><span class="sxs-lookup"><span data-stu-id="cb463-134">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="cb463-135">您可以使用 **AzureRmVmssOsProfile** Cmdlet 來設定此物件。</span><span class="sxs-lookup"><span data-stu-id="cb463-135">You can use the **Set-AzureRmVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="cb463-136">-Overprovision</span><span class="sxs-lookup"><span data-stu-id="cb463-136">-Overprovision</span></span>
<span data-ttu-id="cb463-137">指示 Cmdlet 是否 overprovisions VMSS。</span><span class="sxs-lookup"><span data-stu-id="cb463-137">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="cb463-138">-PlanName</span><span class="sxs-lookup"><span data-stu-id="cb463-138">-PlanName</span></span>
<span data-ttu-id="cb463-139">指定方案名稱。</span><span class="sxs-lookup"><span data-stu-id="cb463-139">Specifies the plan name.</span></span>

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

### <span data-ttu-id="cb463-140">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="cb463-140">-PlanProduct</span></span>
<span data-ttu-id="cb463-141">指定方案產品。</span><span class="sxs-lookup"><span data-stu-id="cb463-141">Specifies the plan product.</span></span>

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

### <span data-ttu-id="cb463-142">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="cb463-142">-PlanPromotionCode</span></span>
<span data-ttu-id="cb463-143">指定方案促銷代碼。</span><span class="sxs-lookup"><span data-stu-id="cb463-143">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="cb463-144">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="cb463-144">-PlanPublisher</span></span>
<span data-ttu-id="cb463-145">指定方案發行者。</span><span class="sxs-lookup"><span data-stu-id="cb463-145">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="cb463-146">-RecoveryPolicyMode</span><span class="sxs-lookup"><span data-stu-id="cb463-146">-RecoveryPolicyMode</span></span>
<span data-ttu-id="cb463-147">指定損毀修復原則。</span><span class="sxs-lookup"><span data-stu-id="cb463-147">Specify the recovery policy.</span></span>

```yaml
Type: RecoveryMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb463-148">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="cb463-148">-SinglePlacementGroup</span></span>
<span data-ttu-id="cb463-149">指定單一位置群組。</span><span class="sxs-lookup"><span data-stu-id="cb463-149">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="cb463-150">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="cb463-150">-SkuCapacity</span></span>
<span data-ttu-id="cb463-151">指定 VMSS 中的實例數。</span><span class="sxs-lookup"><span data-stu-id="cb463-151">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb463-152">-SkuName</span><span class="sxs-lookup"><span data-stu-id="cb463-152">-SkuName</span></span>
<span data-ttu-id="cb463-153">指定 VMSS 的所有實例大小。</span><span class="sxs-lookup"><span data-stu-id="cb463-153">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="cb463-154">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="cb463-154">-SkuTier</span></span>
<span data-ttu-id="cb463-155">指定 VMSS 的層級。</span><span class="sxs-lookup"><span data-stu-id="cb463-155">Specifies the tier of VMSS.</span></span>

<span data-ttu-id="cb463-156">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="cb463-156">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cb463-157">標準</span><span class="sxs-lookup"><span data-stu-id="cb463-157">Standard</span></span>
- <span data-ttu-id="cb463-158">空白</span><span class="sxs-lookup"><span data-stu-id="cb463-158">Basic</span></span>

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

### <span data-ttu-id="cb463-159">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="cb463-159">-StorageProfile</span></span>
<span data-ttu-id="cb463-160">指定包含 VMSS 設定之磁片摘要資訊的儲存空間物件。</span><span class="sxs-lookup"><span data-stu-id="cb463-160">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="cb463-161">您可以使用 **AzureRmVmssStorageProfile** Cmdlet 來設定此物件。</span><span class="sxs-lookup"><span data-stu-id="cb463-161">You can use the **Set-AzureRmVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="cb463-162">-Tag</span><span class="sxs-lookup"><span data-stu-id="cb463-162">-Tag</span></span>
<span data-ttu-id="cb463-163">指定將指派給 VMSS 的標記。</span><span class="sxs-lookup"><span data-stu-id="cb463-163">Specifies the tags that will be assigned to the VMSS.</span></span>

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

### <span data-ttu-id="cb463-164">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="cb463-164">-UpgradePolicyMode</span></span>
<span data-ttu-id="cb463-165">已指定升級模式至規模集中的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="cb463-165">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>

<span data-ttu-id="cb463-166">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="cb463-166">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cb463-167">自動</span><span class="sxs-lookup"><span data-stu-id="cb463-167">Automatic</span></span>
- <span data-ttu-id="cb463-168">手動</span><span class="sxs-lookup"><span data-stu-id="cb463-168">Manual</span></span>

```yaml
Type: UpgradeMode
Parameter Sets: (All)
Aliases: 
Accepted values: Automatic, Manual

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb463-169">-確認</span><span class="sxs-lookup"><span data-stu-id="cb463-169">-Confirm</span></span>
<span data-ttu-id="cb463-170">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cb463-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb463-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb463-171">-WhatIf</span></span>
<span data-ttu-id="cb463-172">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cb463-172">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cb463-173">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cb463-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb463-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb463-174">CommonParameters</span></span>
<span data-ttu-id="cb463-175">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cb463-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb463-176">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cb463-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb463-177">輸入</span><span class="sxs-lookup"><span data-stu-id="cb463-177">INPUTS</span></span>

### <span data-ttu-id="cb463-178">所有</span><span class="sxs-lookup"><span data-stu-id="cb463-178">None</span></span>
<span data-ttu-id="cb463-179">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="cb463-179">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cb463-180">輸出</span><span class="sxs-lookup"><span data-stu-id="cb463-180">OUTPUTS</span></span>

### <span data-ttu-id="cb463-181">這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="cb463-181">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="cb463-182">筆記</span><span class="sxs-lookup"><span data-stu-id="cb463-182">NOTES</span></span>

## <span data-ttu-id="cb463-183">相關連結</span><span class="sxs-lookup"><span data-stu-id="cb463-183">RELATED LINKS</span></span>

[<span data-ttu-id="cb463-184">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="cb463-184">Set-AzureRmVmssOsProfile</span></span>](./Set-AzureRmVmssOsProfile.md)

[<span data-ttu-id="cb463-185">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="cb463-185">Set-AzureRmVmssStorageProfile</span></span>](./Set-AzureRmVmssStorageProfile.md)

[<span data-ttu-id="cb463-186">附加 AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb463-186">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="cb463-187">附加 AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="cb463-187">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)

[<span data-ttu-id="cb463-188">新-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="cb463-188">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)


