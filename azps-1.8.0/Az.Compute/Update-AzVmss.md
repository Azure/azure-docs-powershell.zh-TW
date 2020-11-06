---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: 6fe6f6345f9208a524e1162fb317b88c450f3909
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622640"
---
# <span data-ttu-id="821b2-101">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="821b2-101">Update-AzVmss</span></span>

## <span data-ttu-id="821b2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="821b2-102">SYNOPSIS</span></span>
<span data-ttu-id="821b2-103">更新 VMSS 的狀態。</span><span class="sxs-lookup"><span data-stu-id="821b2-103">Updates the state of a VMSS.</span></span>

## <span data-ttu-id="821b2-104">句法</span><span class="sxs-lookup"><span data-stu-id="821b2-104">SYNTAX</span></span>

### <span data-ttu-id="821b2-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="821b2-105">DefaultParameter (Default)</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-BootDiagnosticsEnabled <Boolean>] [-Tag <Hashtable>]
 [-UpgradePolicyMode <UpgradeMode>] [-DisablePasswordAuthentication <Boolean>]
 [-ManagedDiskStorageAccountType <String>] [-AutomaticOSUpgrade <Boolean>] [-SkuTier <String>]
 [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-SinglePlacementGroup <Boolean>] [-PlanPublisher <String>]
 [-BootDiagnosticsStorageUri <String>] [-Overprovision <Boolean>] [-DisableAutoRollback <Boolean>]
 [-TimeZone <String>] [-PlanPromotionCode <String>] [-MaxBatchInstancePercent <Int32>] [-SkuCapacity <Int32>]
 [-OsDiskWriteAccelerator <Boolean>] [-ImageReferenceOffer <String>] [-ImageReferenceSku <String>]
 [-VhdContainer <String[]>] [-MaxUnhealthyInstancePercent <Int32>] [-ImageReferencePublisher <String>]
 [-ProvisionVMAgent <Boolean>] [-SkuName <String>] [-ImageReferenceVersion <String>]
 [-PauseTimeBetweenBatches <String>] [-ImageUri <String>] [-PlanName <String>] [-PlanProduct <String>]
 [-ImageReferenceId <String>] [-EnableAutomaticUpdate <Boolean>] [-CustomData <String>] [-LicenseType <String>]
 [-OsDiskCaching <CachingTypes>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="821b2-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="821b2-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-BootDiagnosticsEnabled <Boolean>] [-Tag <Hashtable>]
 [-UpgradePolicyMode <UpgradeMode>] [-DisablePasswordAuthentication <Boolean>]
 -IdentityType <ResourceIdentityType> [-ManagedDiskStorageAccountType <String>] [-AutomaticOSUpgrade <Boolean>]
 [-SkuTier <String>] [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-SinglePlacementGroup <Boolean>]
 [-PlanPublisher <String>] [-BootDiagnosticsStorageUri <String>] [-Overprovision <Boolean>]
 [-DisableAutoRollback <Boolean>] [-TimeZone <String>] [-PlanPromotionCode <String>]
 [-MaxBatchInstancePercent <Int32>] [-SkuCapacity <Int32>] [-OsDiskWriteAccelerator <Boolean>]
 [-ImageReferenceOffer <String>] [-ImageReferenceSku <String>] [-VhdContainer <String[]>]
 [-MaxUnhealthyInstancePercent <Int32>] [-ImageReferencePublisher <String>] [-ProvisionVMAgent <Boolean>]
 [-SkuName <String>] [-ImageReferenceVersion <String>] [-PauseTimeBetweenBatches <String>] [-ImageUri <String>]
 [-PlanName <String>] [-PlanProduct <String>] [-ImageReferenceId <String>] [-EnableAutomaticUpdate <Boolean>]
 [-CustomData <String>] [-LicenseType <String>] [-OsDiskCaching <CachingTypes>] [-IdentityId <String[]>]
 [-UltraSSDEnabled <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="821b2-107">說明</span><span class="sxs-lookup"><span data-stu-id="821b2-107">DESCRIPTION</span></span>
<span data-ttu-id="821b2-108">**更新-AzVmss** Cmdlet 會更新虛擬機器縮放集 (VMSS) 的狀態設定為局部 VMSS 物件的狀態。</span><span class="sxs-lookup"><span data-stu-id="821b2-108">The **Update-AzVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="821b2-109">示例</span><span class="sxs-lookup"><span data-stu-id="821b2-109">EXAMPLES</span></span>

### <span data-ttu-id="821b2-110">範例1：更新 VMSS 的狀態至本機 VMSS 物件的狀態。</span><span class="sxs-lookup"><span data-stu-id="821b2-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="821b2-111">這個命令會將屬於名為 Group001 之資源群組之 VMSS001 的 VMSS 狀態更新為本機 VMSS 物件的狀態，$LocalVMSS。</span><span class="sxs-lookup"><span data-stu-id="821b2-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="821b2-112">參數</span><span class="sxs-lookup"><span data-stu-id="821b2-112">PARAMETERS</span></span>

### <span data-ttu-id="821b2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="821b2-113">-AsJob</span></span>
<span data-ttu-id="821b2-114">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="821b2-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="821b2-115">-AutomaticOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="821b2-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="821b2-116">設定更新版本的影像時，是否應該將作業系統升級自動套用到縮放集實例，以滾動的方式進行。</span><span class="sxs-lookup"><span data-stu-id="821b2-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="821b2-117">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="821b2-117">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="821b2-118">是否應該在虛擬機器規模集上啟用引導診斷程式。</span><span class="sxs-lookup"><span data-stu-id="821b2-118">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="821b2-119">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="821b2-119">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="821b2-120">要用來放置主控台輸出和螢幕擷取畫面的儲存空間帳戶 URI。</span><span class="sxs-lookup"><span data-stu-id="821b2-120">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="821b2-121">-CustomData</span><span class="sxs-lookup"><span data-stu-id="821b2-121">-CustomData</span></span>
<span data-ttu-id="821b2-122">指定自訂資料的基本64編碼字串。</span><span class="sxs-lookup"><span data-stu-id="821b2-122">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="821b2-123">這會解碼為二進位陣列，並儲存為虛擬機器上的檔案。</span><span class="sxs-lookup"><span data-stu-id="821b2-123">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="821b2-124">二進位陣列的最大長度為65535個位元組。</span><span class="sxs-lookup"><span data-stu-id="821b2-124">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="821b2-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="821b2-125">-DefaultProfile</span></span>
<span data-ttu-id="821b2-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="821b2-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="821b2-127">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="821b2-127">-DisableAutoRollback</span></span>
<span data-ttu-id="821b2-128">針對自動 OS 升級原則停用自動復原</span><span class="sxs-lookup"><span data-stu-id="821b2-128">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="821b2-129">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="821b2-129">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="821b2-130">表示此 Cmdlet 停用 Linux 作業系統的密碼驗證。</span><span class="sxs-lookup"><span data-stu-id="821b2-130">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

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

### <span data-ttu-id="821b2-131">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="821b2-131">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="821b2-132">指出是否已針對自動更新啟用 VMSS 中的 Windows 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="821b2-132">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="821b2-133">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="821b2-133">-IdentityId</span></span>
<span data-ttu-id="821b2-134">指定與虛擬機器小性集相關聯的使用者識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="821b2-134">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="821b2-135">使用者身分識別參照將是下列形式的 ARM 資源識別碼： '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="821b2-135">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="821b2-136">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="821b2-136">-IdentityType</span></span>
<span data-ttu-id="821b2-137">指定用於虛擬機器規模集的身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="821b2-137">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="821b2-138">"SystemAssignedUserAssigned" 類型包含隱含建立的身分識別，以及一組使用者指派的身分識別。</span><span class="sxs-lookup"><span data-stu-id="821b2-138">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="821b2-139">"None" 類型將會移除虛擬機器小單位集中的任何身分識別。</span><span class="sxs-lookup"><span data-stu-id="821b2-139">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="821b2-140">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="821b2-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="821b2-141">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="821b2-141">SystemAssigned</span></span>
- <span data-ttu-id="821b2-142">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="821b2-142">UserAssigned</span></span>
- <span data-ttu-id="821b2-143">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="821b2-143">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="821b2-144">所有</span><span class="sxs-lookup"><span data-stu-id="821b2-144">None</span></span>

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

### <span data-ttu-id="821b2-145">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="821b2-145">-ImageReferenceId</span></span>
<span data-ttu-id="821b2-146">指定影像參照 ID。</span><span class="sxs-lookup"><span data-stu-id="821b2-146">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="821b2-147">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="821b2-147">-ImageReferenceOffer</span></span>
<span data-ttu-id="821b2-148">指定 (VMImage) 優惠的虛擬機器影像類型。</span><span class="sxs-lookup"><span data-stu-id="821b2-148">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="821b2-149">若要取得影像優惠，請使用 Get-AzVMImageOffer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="821b2-149">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="821b2-150">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="821b2-150">-ImageReferencePublisher</span></span>
<span data-ttu-id="821b2-151">指定 VMImage 發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="821b2-151">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="821b2-152">若要取得發行者，請使用 Get-AzVMImagePublisher Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="821b2-152">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="821b2-153">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="821b2-153">-ImageReferenceSku</span></span>
<span data-ttu-id="821b2-154">指定 VMImage SKU。</span><span class="sxs-lookup"><span data-stu-id="821b2-154">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="821b2-155">若要取得 Sku，請使用 Get-AzVMImageSku Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="821b2-155">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="821b2-156">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="821b2-156">-ImageReferenceVersion</span></span>
<span data-ttu-id="821b2-157">指定 VMImage 的版本。</span><span class="sxs-lookup"><span data-stu-id="821b2-157">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="821b2-158">若要使用最新版本，請指定最新的值，而不是特定的版本。</span><span class="sxs-lookup"><span data-stu-id="821b2-158">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="821b2-159">-ImageUri</span><span class="sxs-lookup"><span data-stu-id="821b2-159">-ImageUri</span></span>
<span data-ttu-id="821b2-160">指定使用者影像的 blob URI。</span><span class="sxs-lookup"><span data-stu-id="821b2-160">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="821b2-161">VMSS 會在使用者影像的同一個容器中建立作業系統磁片。</span><span class="sxs-lookup"><span data-stu-id="821b2-161">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="821b2-162">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="821b2-162">-LicenseType</span></span>
<span data-ttu-id="821b2-163">指定授權類型，這是用來提供您自己的授權案例。</span><span class="sxs-lookup"><span data-stu-id="821b2-163">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="821b2-164">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="821b2-164">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="821b2-165">指定受管理磁片的儲存帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="821b2-165">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="821b2-166">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="821b2-166">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="821b2-167">StandardLRS</span><span class="sxs-lookup"><span data-stu-id="821b2-167">StandardLRS</span></span>
- <span data-ttu-id="821b2-168">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="821b2-168">PremiumLRS</span></span>

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

### <span data-ttu-id="821b2-169">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="821b2-169">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="821b2-170">輪流升級在一批中同時升級之總虛擬機器實例的最大百分比。</span><span class="sxs-lookup"><span data-stu-id="821b2-170">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="821b2-171">如此一來，在前一個或將來的批次中，可能會導致批次中的實例百分比下降，以確保較高的可靠性。</span><span class="sxs-lookup"><span data-stu-id="821b2-171">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="821b2-172">如果未指定值，則會將該值設定為20。</span><span class="sxs-lookup"><span data-stu-id="821b2-172">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="821b2-173">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="821b2-173">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="821b2-174">在輪流升級中止前，規模集中可同時進行升級的虛擬機器實例總數，或由虛擬機器健康情況檢查所顯示的總虛擬機器實例的最大百分比。</span><span class="sxs-lookup"><span data-stu-id="821b2-174">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="821b2-175">在開始任何批次之前，將會檢查此限制。</span><span class="sxs-lookup"><span data-stu-id="821b2-175">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="821b2-176">如果未指定值，則會將該值設定為20。</span><span class="sxs-lookup"><span data-stu-id="821b2-176">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="821b2-177">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="821b2-177">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="821b2-178">可發現處於不正常狀態之已升級虛擬機器實例的最大百分比。</span><span class="sxs-lookup"><span data-stu-id="821b2-178">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="821b2-179">這項檢查會在每個批次升級後發生。</span><span class="sxs-lookup"><span data-stu-id="821b2-179">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="821b2-180">如果曾經超過此百分比，則滾動更新會中止。</span><span class="sxs-lookup"><span data-stu-id="821b2-180">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="821b2-181">如果未指定值，則會將該值設定為20。</span><span class="sxs-lookup"><span data-stu-id="821b2-181">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="821b2-182">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="821b2-182">-OsDiskCaching</span></span>
<span data-ttu-id="821b2-183">指定作業系統磁片的快取模式。</span><span class="sxs-lookup"><span data-stu-id="821b2-183">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="821b2-184">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="821b2-184">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="821b2-185">所有</span><span class="sxs-lookup"><span data-stu-id="821b2-185">None</span></span>
- <span data-ttu-id="821b2-186">唯讀</span><span class="sxs-lookup"><span data-stu-id="821b2-186">ReadOnly</span></span>
- <span data-ttu-id="821b2-187">ReadWrite 的預設值是 ReadWrite。</span><span class="sxs-lookup"><span data-stu-id="821b2-187">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="821b2-188">如果您變更快取值，Cmdlet 會重新開機虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="821b2-188">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="821b2-189">此設定會影響磁片的一致性和效能。</span><span class="sxs-lookup"><span data-stu-id="821b2-189">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="821b2-190">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="821b2-190">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="821b2-191">指定是否應該在 OS 磁片上啟用或停用 WriteAccelerator。</span><span class="sxs-lookup"><span data-stu-id="821b2-191">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="821b2-192">-Overprovision</span><span class="sxs-lookup"><span data-stu-id="821b2-192">-Overprovision</span></span>
<span data-ttu-id="821b2-193">指示 Cmdlet 是否 overprovisions VMSS。</span><span class="sxs-lookup"><span data-stu-id="821b2-193">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="821b2-194">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="821b2-194">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="821b2-195">在一批中完成所有虛擬機器的更新與開始下一個批次之間的等待時間。</span><span class="sxs-lookup"><span data-stu-id="821b2-195">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="821b2-196">應以 ISO 8601 格式指定持續時間。</span><span class="sxs-lookup"><span data-stu-id="821b2-196">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="821b2-197">預設值為0秒 (PT0S) 。</span><span class="sxs-lookup"><span data-stu-id="821b2-197">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="821b2-198">-PlanName</span><span class="sxs-lookup"><span data-stu-id="821b2-198">-PlanName</span></span>
<span data-ttu-id="821b2-199">指定方案名稱。</span><span class="sxs-lookup"><span data-stu-id="821b2-199">Specifies the plan name.</span></span>

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

### <span data-ttu-id="821b2-200">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="821b2-200">-PlanProduct</span></span>
<span data-ttu-id="821b2-201">指定方案產品。</span><span class="sxs-lookup"><span data-stu-id="821b2-201">Specifies the plan product.</span></span>

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

### <span data-ttu-id="821b2-202">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="821b2-202">-PlanPromotionCode</span></span>
<span data-ttu-id="821b2-203">指定方案促銷代碼。</span><span class="sxs-lookup"><span data-stu-id="821b2-203">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="821b2-204">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="821b2-204">-PlanPublisher</span></span>
<span data-ttu-id="821b2-205">指定方案發行者。</span><span class="sxs-lookup"><span data-stu-id="821b2-205">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="821b2-206">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="821b2-206">-ProvisionVMAgent</span></span>
<span data-ttu-id="821b2-207">指出是否應該在 VMSS 中的 Windows 虛擬機器上預配虛擬機器代理程式。</span><span class="sxs-lookup"><span data-stu-id="821b2-207">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="821b2-208">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="821b2-208">-ResourceGroupName</span></span>
<span data-ttu-id="821b2-209">指定 VMSS 所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="821b2-209">Specifies the name of the resource group the VMSS belongs to.</span></span>

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

### <span data-ttu-id="821b2-210">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="821b2-210">-SinglePlacementGroup</span></span>
<span data-ttu-id="821b2-211">指定單一位置群組。</span><span class="sxs-lookup"><span data-stu-id="821b2-211">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="821b2-212">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="821b2-212">-SkuCapacity</span></span>
<span data-ttu-id="821b2-213">指定 VMSS 中的實例數。</span><span class="sxs-lookup"><span data-stu-id="821b2-213">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="821b2-214">-SkuName</span><span class="sxs-lookup"><span data-stu-id="821b2-214">-SkuName</span></span>
<span data-ttu-id="821b2-215">指定 VMSS 的所有實例大小。</span><span class="sxs-lookup"><span data-stu-id="821b2-215">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="821b2-216">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="821b2-216">-SkuTier</span></span>
<span data-ttu-id="821b2-217">指定 VMSS 的層級。</span><span class="sxs-lookup"><span data-stu-id="821b2-217">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="821b2-218">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="821b2-218">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="821b2-219">標準</span><span class="sxs-lookup"><span data-stu-id="821b2-219">Standard</span></span>
- <span data-ttu-id="821b2-220">空白</span><span class="sxs-lookup"><span data-stu-id="821b2-220">Basic</span></span>

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

### <span data-ttu-id="821b2-221">-Tag</span><span class="sxs-lookup"><span data-stu-id="821b2-221">-Tag</span></span>
<span data-ttu-id="821b2-222">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="821b2-222">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="821b2-223">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="821b2-223">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="821b2-224">-時區</span><span class="sxs-lookup"><span data-stu-id="821b2-224">-TimeZone</span></span>
<span data-ttu-id="821b2-225">指定 Windows 作業系統的時區。</span><span class="sxs-lookup"><span data-stu-id="821b2-225">Specifies the time zone for Windows OS.</span></span>

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

### <span data-ttu-id="821b2-226">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="821b2-226">-UltraSSDEnabled</span></span>
<span data-ttu-id="821b2-227">啟用或停用在虛擬機器縮放設定上有一個或多個受管理資料磁片的功能，以及 UltraSSD_LRS 儲存帳戶類型的標誌。</span><span class="sxs-lookup"><span data-stu-id="821b2-227">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="821b2-228">只有在啟用此屬性時，才能將儲存帳戶類型 UltraSSD_LRS 的受管理磁片新增至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="821b2-228">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="821b2-229">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="821b2-229">-UpgradePolicyMode</span></span>
<span data-ttu-id="821b2-230">已指定升級模式至規模集中的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="821b2-230">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="821b2-231">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="821b2-231">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="821b2-232">自動</span><span class="sxs-lookup"><span data-stu-id="821b2-232">Automatic</span></span>
- <span data-ttu-id="821b2-233">手動</span><span class="sxs-lookup"><span data-stu-id="821b2-233">Manual</span></span>
- <span data-ttu-id="821b2-234">擲</span><span class="sxs-lookup"><span data-stu-id="821b2-234">Rolling</span></span>

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

### <span data-ttu-id="821b2-235">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="821b2-235">-VhdContainer</span></span>
<span data-ttu-id="821b2-236">指定用來儲存 VMSS 作業系統磁片的容器 Url。</span><span class="sxs-lookup"><span data-stu-id="821b2-236">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="821b2-237">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="821b2-237">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="821b2-238">指定本機 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="821b2-238">Specifies a local VMSS object.</span></span>
<span data-ttu-id="821b2-239">若要取得 VMSS 物件，請使用 Get-AzVmss Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="821b2-239">To obtain a VMSS object, use the Get-AzVmss cmdlet.</span></span>
<span data-ttu-id="821b2-240">此虛擬機器物件包含 VMSS 的更新狀態。</span><span class="sxs-lookup"><span data-stu-id="821b2-240">This virtual machine object contains the updated state for the VMSS.</span></span>

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

### <span data-ttu-id="821b2-241">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="821b2-241">-VMScaleSetName</span></span>
<span data-ttu-id="821b2-242">指定此 Cmdlet 所建立之 VMSS 的名稱。</span><span class="sxs-lookup"><span data-stu-id="821b2-242">Specifies the name of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="821b2-243">-確認</span><span class="sxs-lookup"><span data-stu-id="821b2-243">-Confirm</span></span>
<span data-ttu-id="821b2-244">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="821b2-244">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="821b2-245">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="821b2-245">-WhatIf</span></span>
<span data-ttu-id="821b2-246">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="821b2-246">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="821b2-247">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="821b2-247">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="821b2-248">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="821b2-248">CommonParameters</span></span>
<span data-ttu-id="821b2-249">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="821b2-249">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="821b2-250">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="821b2-250">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="821b2-251">輸入</span><span class="sxs-lookup"><span data-stu-id="821b2-251">INPUTS</span></span>

### <span data-ttu-id="821b2-252">System.object</span><span class="sxs-lookup"><span data-stu-id="821b2-252">System.String</span></span>

### <span data-ttu-id="821b2-253">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="821b2-253">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="821b2-254">System.object</span><span class="sxs-lookup"><span data-stu-id="821b2-254">System.Boolean</span></span>

## <span data-ttu-id="821b2-255">輸出</span><span class="sxs-lookup"><span data-stu-id="821b2-255">OUTPUTS</span></span>

### <span data-ttu-id="821b2-256">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="821b2-256">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="821b2-257">筆記</span><span class="sxs-lookup"><span data-stu-id="821b2-257">NOTES</span></span>

## <span data-ttu-id="821b2-258">相關連結</span><span class="sxs-lookup"><span data-stu-id="821b2-258">RELATED LINKS</span></span>

[<span data-ttu-id="821b2-259">AzVmss</span><span class="sxs-lookup"><span data-stu-id="821b2-259">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="821b2-260">新-AzVmss</span><span class="sxs-lookup"><span data-stu-id="821b2-260">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="821b2-261">移除-AzVmss</span><span class="sxs-lookup"><span data-stu-id="821b2-261">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="821b2-262">重新開機-AzVmss</span><span class="sxs-lookup"><span data-stu-id="821b2-262">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="821b2-263">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="821b2-263">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="821b2-264">開始-AzVmss</span><span class="sxs-lookup"><span data-stu-id="821b2-264">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="821b2-265">停止 AzVmss</span><span class="sxs-lookup"><span data-stu-id="821b2-265">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

