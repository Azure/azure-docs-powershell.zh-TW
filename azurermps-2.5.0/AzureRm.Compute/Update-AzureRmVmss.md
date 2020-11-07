---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermvmss
schema: 2.0.0
ms.openlocfilehash: 544af56c5e1ff72a3b23c3dcf89af36f7d74eff2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800509"
---
# <span data-ttu-id="d730f-101">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d730f-101">Update-AzureRmVmss</span></span>

## <span data-ttu-id="d730f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d730f-102">SYNOPSIS</span></span>
<span data-ttu-id="d730f-103">更新 VMSS 的狀態。</span><span class="sxs-lookup"><span data-stu-id="d730f-103">Updates the state of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d730f-104">句法</span><span class="sxs-lookup"><span data-stu-id="d730f-104">SYNTAX</span></span>

### <span data-ttu-id="d730f-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="d730f-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-ImageReferenceSku <String>]
 [-ManagedDiskStorageAccountType <StorageAccountTypes>] [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-Overprovision <Boolean>] [-MaxBatchInstancePercent <Int32>]
 [-TimeZone <String>] [-BootDiagnosticsStorageUri <String>] [-AutomaticOSUpgrade <Boolean>]
 [-SinglePlacementGroup <Boolean>] [-CustomData <String>] [-UpgradePolicyMode <UpgradeMode>]
 [-ImageReferenceId <String>] [-DisablePasswordAuthentication <Boolean>] [-Tag <Hashtable>]
 [-PlanName <String>] [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-ImageReferencePublisher <String>]
 [-PlanProduct <String>] [-VhdContainer <String[]>] [-ImageUri <String>] [-SkuTier <String>]
 [-EnableAutomaticUpdate <Boolean>] [-LicenseType <String>] [-SkuName <String>] [-PlanPromotionCode <String>]
 [-MaxUnhealthyInstancePercent <Int32>] [-SkuCapacity <Int32>] [-OsDiskWriteAccelerator <Boolean>]
 [-ImageReferenceOffer <String>] [-PauseTimeBetweenBatches <String>] [-OsDiskCaching <CachingTypes>]
 [-ImageReferenceVersion <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d730f-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="d730f-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-ImageReferenceSku <String>] [-IdentityId <String[]>]
 [-ManagedDiskStorageAccountType <StorageAccountTypes>] [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-Overprovision <Boolean>] [-MaxBatchInstancePercent <Int32>]
 [-TimeZone <String>] [-BootDiagnosticsStorageUri <String>] [-AutomaticOSUpgrade <Boolean>]
 [-SinglePlacementGroup <Boolean>] [-CustomData <String>] [-UpgradePolicyMode <UpgradeMode>]
 [-ImageReferenceId <String>] [-DisablePasswordAuthentication <Boolean>] [-Tag <Hashtable>]
 [-PlanName <String>] [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-ImageReferencePublisher <String>]
 [-PlanProduct <String>] [-VhdContainer <String[]>] [-ImageUri <String>] [-SkuTier <String>]
 [-EnableAutomaticUpdate <Boolean>] [-LicenseType <String>] -IdentityType <ResourceIdentityType>
 [-SkuName <String>] [-PlanPromotionCode <String>] [-MaxUnhealthyInstancePercent <Int32>]
 [-SkuCapacity <Int32>] [-OsDiskWriteAccelerator <Boolean>] [-ImageReferenceOffer <String>]
 [-PauseTimeBetweenBatches <String>] [-OsDiskCaching <CachingTypes>] [-ImageReferenceVersion <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d730f-107">說明</span><span class="sxs-lookup"><span data-stu-id="d730f-107">DESCRIPTION</span></span>
<span data-ttu-id="d730f-108">**更新-AzureRmVmss** Cmdlet 會更新虛擬機器縮放集 (VMSS) 的狀態設定為局部 VMSS 物件的狀態。</span><span class="sxs-lookup"><span data-stu-id="d730f-108">The **Update-AzureRmVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="d730f-109">示例</span><span class="sxs-lookup"><span data-stu-id="d730f-109">EXAMPLES</span></span>

### <span data-ttu-id="d730f-110">範例1：更新 VMSS 的狀態至本機 VMSS 物件的狀態。</span><span class="sxs-lookup"><span data-stu-id="d730f-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzureRmVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="d730f-111">這個命令會將屬於名為 Group001 之資源群組之 VMSS001 的 VMSS 狀態更新為本機 VMSS 物件的狀態，$LocalVMSS。</span><span class="sxs-lookup"><span data-stu-id="d730f-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="d730f-112">參數</span><span class="sxs-lookup"><span data-stu-id="d730f-112">PARAMETERS</span></span>

### <span data-ttu-id="d730f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d730f-113">-AsJob</span></span>
<span data-ttu-id="d730f-114">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="d730f-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d730f-115">-AutomaticOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="d730f-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="d730f-116">設定更新版本的影像時，是否應該將作業系統升級自動套用到縮放集實例，以滾動的方式進行。</span><span class="sxs-lookup"><span data-stu-id="d730f-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d730f-117">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="d730f-117">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="d730f-118">是否應該在虛擬機器規模集上啟用引導診斷程式。</span><span class="sxs-lookup"><span data-stu-id="d730f-118">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d730f-119">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="d730f-119">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="d730f-120">要用來放置主控台輸出和螢幕擷取畫面的儲存空間帳戶 URI。</span><span class="sxs-lookup"><span data-stu-id="d730f-120">URI of the storage account to use for placing the console output and screenshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d730f-121">-CustomData</span><span class="sxs-lookup"><span data-stu-id="d730f-121">-CustomData</span></span>
<span data-ttu-id="d730f-122">指定自訂資料的基本64編碼字串。</span><span class="sxs-lookup"><span data-stu-id="d730f-122">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="d730f-123">這會解碼為二進位陣列，並儲存為虛擬機器上的檔案。</span><span class="sxs-lookup"><span data-stu-id="d730f-123">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="d730f-124">二進位陣列的最大長度為65535個位元組。</span><span class="sxs-lookup"><span data-stu-id="d730f-124">The maximum length of the binary array is 65535 bytes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d730f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d730f-125">-DefaultProfile</span></span>
<span data-ttu-id="d730f-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d730f-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d730f-127">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="d730f-127">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="d730f-128">表示此 Cmdlet 停用 Linux 作業系統的密碼驗證。</span><span class="sxs-lookup"><span data-stu-id="d730f-128">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d730f-129">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="d730f-129">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="d730f-130">指出是否已針對自動更新啟用 VMSS 中的 Windows 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="d730f-130">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d730f-131">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="d730f-131">-IdentityId</span></span>
<span data-ttu-id="d730f-132">指定與虛擬機器小性集相關聯的使用者識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="d730f-132">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="d730f-133">使用者身分識別參照將是下列形式的 ARM 資源識別碼： '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="d730f-133">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d730f-134">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="d730f-134">-IdentityType</span></span>
<span data-ttu-id="d730f-135">指定用於虛擬機器規模集的身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="d730f-135">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="d730f-136">"SystemAssignedUserAssigned" 類型包含隱含建立的身分識別，以及一組使用者指派的身分識別。</span><span class="sxs-lookup"><span data-stu-id="d730f-136">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="d730f-137">"None" 類型將會移除虛擬機器小單位集中的任何身分識別。</span><span class="sxs-lookup"><span data-stu-id="d730f-137">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="d730f-138">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="d730f-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d730f-139">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="d730f-139">SystemAssigned</span></span>
- <span data-ttu-id="d730f-140">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="d730f-140">UserAssigned</span></span>
- <span data-ttu-id="d730f-141">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="d730f-141">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="d730f-142">所有</span><span class="sxs-lookup"><span data-stu-id="d730f-142">None</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d730f-143">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="d730f-143">-ImageReferenceId</span></span>
<span data-ttu-id="d730f-144">指定影像參照 ID。</span><span class="sxs-lookup"><span data-stu-id="d730f-144">Specifies the image reference ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d730f-145">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="d730f-145">-ImageReferenceOffer</span></span>
<span data-ttu-id="d730f-146">指定 (VMImage) 優惠的虛擬機器影像類型。</span><span class="sxs-lookup"><span data-stu-id="d730f-146">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="d730f-147">若要取得影像優惠，請使用 Get-AzureRmVMImageOffer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d730f-147">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d730f-148">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="d730f-148">-ImageReferencePublisher</span></span>
<span data-ttu-id="d730f-149">指定 VMImage 發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="d730f-149">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="d730f-150">若要取得發行者，請使用 Get-AzureRmVMImagePublisher Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d730f-150">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d730f-151">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="d730f-151">-ImageReferenceSku</span></span>
<span data-ttu-id="d730f-152">指定 VMImage SKU。</span><span class="sxs-lookup"><span data-stu-id="d730f-152">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="d730f-153">若要取得 Sku，請使用 Get-AzureRmVMImageSku Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d730f-153">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d730f-154">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="d730f-154">-ImageReferenceVersion</span></span>
<span data-ttu-id="d730f-155">指定 VMImage 的版本。</span><span class="sxs-lookup"><span data-stu-id="d730f-155">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="d730f-156">若要使用最新版本，請指定最新的值，而不是特定的版本。</span><span class="sxs-lookup"><span data-stu-id="d730f-156">To use the latest version, specify a value of latest instead of a particular version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d730f-157">-ImageUri</span><span class="sxs-lookup"><span data-stu-id="d730f-157">-ImageUri</span></span>
<span data-ttu-id="d730f-158">指定使用者影像的 blob URI。</span><span class="sxs-lookup"><span data-stu-id="d730f-158">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="d730f-159">VMSS 會在使用者影像的同一個容器中建立作業系統磁片。</span><span class="sxs-lookup"><span data-stu-id="d730f-159">VMSS creates an operating system disk in the same container of the user image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d730f-160">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="d730f-160">-LicenseType</span></span>
<span data-ttu-id="d730f-161">指定授權類型，這是用來提供您自己的授權案例。</span><span class="sxs-lookup"><span data-stu-id="d730f-161">Specify the license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d730f-162">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="d730f-162">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="d730f-163">指定受管理磁片的儲存帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="d730f-163">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="d730f-164">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="d730f-164">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d730f-165">StandardLRS</span><span class="sxs-lookup"><span data-stu-id="d730f-165">StandardLRS</span></span>
- <span data-ttu-id="d730f-166">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="d730f-166">PremiumLRS</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d730f-167">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="d730f-167">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="d730f-168">輪流升級在一批中同時升級之總虛擬機器實例的最大百分比。</span><span class="sxs-lookup"><span data-stu-id="d730f-168">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="d730f-169">如此一來，在前一個或將來的批次中，可能會導致批次中的實例百分比下降，以確保較高的可靠性。</span><span class="sxs-lookup"><span data-stu-id="d730f-169">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="d730f-170">如果未指定值，則會將該值設定為20。</span><span class="sxs-lookup"><span data-stu-id="d730f-170">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d730f-171">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="d730f-171">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="d730f-172">在輪流升級中止前，規模集中可同時進行升級的虛擬機器實例總數，或由虛擬機器健康情況檢查所顯示的總虛擬機器實例的最大百分比。</span><span class="sxs-lookup"><span data-stu-id="d730f-172">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="d730f-173">在開始任何批次之前，將會檢查此限制。</span><span class="sxs-lookup"><span data-stu-id="d730f-173">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="d730f-174">如果未指定值，則會將該值設定為20。</span><span class="sxs-lookup"><span data-stu-id="d730f-174">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d730f-175">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="d730f-175">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="d730f-176">可發現處於不正常狀態之已升級虛擬機器實例的最大百分比。</span><span class="sxs-lookup"><span data-stu-id="d730f-176">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="d730f-177">這項檢查會在每個批次升級後發生。</span><span class="sxs-lookup"><span data-stu-id="d730f-177">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="d730f-178">如果曾經超過此百分比，則滾動更新會中止。</span><span class="sxs-lookup"><span data-stu-id="d730f-178">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="d730f-179">如果未指定值，則會將該值設定為20。</span><span class="sxs-lookup"><span data-stu-id="d730f-179">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d730f-180">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="d730f-180">-OsDiskCaching</span></span>
<span data-ttu-id="d730f-181">指定作業系統磁片的快取模式。</span><span class="sxs-lookup"><span data-stu-id="d730f-181">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="d730f-182">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="d730f-182">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d730f-183">所有</span><span class="sxs-lookup"><span data-stu-id="d730f-183">None</span></span>
- <span data-ttu-id="d730f-184">唯讀</span><span class="sxs-lookup"><span data-stu-id="d730f-184">ReadOnly</span></span>
- <span data-ttu-id="d730f-185">讀</span><span class="sxs-lookup"><span data-stu-id="d730f-185">ReadWrite</span></span>

<span data-ttu-id="d730f-186">預設值為 ReadWrite。</span><span class="sxs-lookup"><span data-stu-id="d730f-186">The default value is ReadWrite.</span></span>
<span data-ttu-id="d730f-187">如果您變更快取值，Cmdlet 會重新開機虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="d730f-187">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>

<span data-ttu-id="d730f-188">此設定會影響磁片的一致性和效能。</span><span class="sxs-lookup"><span data-stu-id="d730f-188">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d730f-189">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="d730f-189">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="d730f-190">指定是否應該在 OS 磁片上啟用或停用 WriteAccelerator。</span><span class="sxs-lookup"><span data-stu-id="d730f-190">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d730f-191">-Overprovision</span><span class="sxs-lookup"><span data-stu-id="d730f-191">-Overprovision</span></span>
<span data-ttu-id="d730f-192">指示 Cmdlet 是否 overprovisions VMSS。</span><span class="sxs-lookup"><span data-stu-id="d730f-192">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d730f-193">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="d730f-193">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="d730f-194">在一批中完成所有虛擬機器的更新與開始下一個批次之間的等待時間。</span><span class="sxs-lookup"><span data-stu-id="d730f-194">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="d730f-195">應以 ISO 8601 格式指定持續時間。</span><span class="sxs-lookup"><span data-stu-id="d730f-195">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="d730f-196">預設值為0秒 (PT0S) 。</span><span class="sxs-lookup"><span data-stu-id="d730f-196">The default value is 0 seconds (PT0S).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d730f-197">-PlanName</span><span class="sxs-lookup"><span data-stu-id="d730f-197">-PlanName</span></span>
<span data-ttu-id="d730f-198">指定方案名稱。</span><span class="sxs-lookup"><span data-stu-id="d730f-198">Specifies the plan name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d730f-199">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="d730f-199">-PlanProduct</span></span>
<span data-ttu-id="d730f-200">指定方案產品。</span><span class="sxs-lookup"><span data-stu-id="d730f-200">Specifies the plan product.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d730f-201">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="d730f-201">-PlanPromotionCode</span></span>
<span data-ttu-id="d730f-202">指定方案促銷代碼。</span><span class="sxs-lookup"><span data-stu-id="d730f-202">Specifies the plan promotion code.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d730f-203">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="d730f-203">-PlanPublisher</span></span>
<span data-ttu-id="d730f-204">指定方案發行者。</span><span class="sxs-lookup"><span data-stu-id="d730f-204">Specifies the plan publisher.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d730f-205">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="d730f-205">-ProvisionVMAgent</span></span>
<span data-ttu-id="d730f-206">指出是否應該在 VMSS 中的 Windows 虛擬機器上預配虛擬機器代理程式。</span><span class="sxs-lookup"><span data-stu-id="d730f-206">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d730f-207">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d730f-207">-ResourceGroupName</span></span>
<span data-ttu-id="d730f-208">指定 VMSS 所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d730f-208">Specifies the name of the resource group the VMSS belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d730f-209">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="d730f-209">-SinglePlacementGroup</span></span>
<span data-ttu-id="d730f-210">指定單一位置群組。</span><span class="sxs-lookup"><span data-stu-id="d730f-210">Specifies the single placement group.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d730f-211">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="d730f-211">-SkuCapacity</span></span>
<span data-ttu-id="d730f-212">指定 VMSS 中的實例數。</span><span class="sxs-lookup"><span data-stu-id="d730f-212">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d730f-213">-SkuName</span><span class="sxs-lookup"><span data-stu-id="d730f-213">-SkuName</span></span>
<span data-ttu-id="d730f-214">指定 VMSS 的所有實例大小。</span><span class="sxs-lookup"><span data-stu-id="d730f-214">Specifies the size of all the instances of VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d730f-215">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="d730f-215">-SkuTier</span></span>
<span data-ttu-id="d730f-216">指定 VMSS 的層級。</span><span class="sxs-lookup"><span data-stu-id="d730f-216">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="d730f-217">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="d730f-217">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d730f-218">標準</span><span class="sxs-lookup"><span data-stu-id="d730f-218">Standard</span></span>
- <span data-ttu-id="d730f-219">空白</span><span class="sxs-lookup"><span data-stu-id="d730f-219">Basic</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d730f-220">-Tag</span><span class="sxs-lookup"><span data-stu-id="d730f-220">-Tag</span></span>
<span data-ttu-id="d730f-221">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="d730f-221">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d730f-222">例如：</span><span class="sxs-lookup"><span data-stu-id="d730f-222">For example:</span></span>

<span data-ttu-id="d730f-223">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="d730f-223">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d730f-224">-時區</span><span class="sxs-lookup"><span data-stu-id="d730f-224">-TimeZone</span></span>
<span data-ttu-id="d730f-225">指定 Windows 作業系統的時區。</span><span class="sxs-lookup"><span data-stu-id="d730f-225">Specifies the time zone for Windows OS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d730f-226">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="d730f-226">-UpgradePolicyMode</span></span>
<span data-ttu-id="d730f-227">已指定升級模式至規模集中的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="d730f-227">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="d730f-228">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="d730f-228">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d730f-229">自動</span><span class="sxs-lookup"><span data-stu-id="d730f-229">Automatic</span></span>
- <span data-ttu-id="d730f-230">手動</span><span class="sxs-lookup"><span data-stu-id="d730f-230">Manual</span></span>
- <span data-ttu-id="d730f-231">擲</span><span class="sxs-lookup"><span data-stu-id="d730f-231">Rolling</span></span>

```yaml
Type: UpgradeMode
Parameter Sets: (All)
Aliases: 
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d730f-232">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="d730f-232">-VhdContainer</span></span>
<span data-ttu-id="d730f-233">指定用來儲存 VMSS 作業系統磁片的容器 Url。</span><span class="sxs-lookup"><span data-stu-id="d730f-233">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d730f-234">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d730f-234">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="d730f-235">指定本機 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="d730f-235">Specifies a local VMSS object.</span></span>
<span data-ttu-id="d730f-236">若要取得 VMSS 物件，請使用 Get-AzureRmVmss Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d730f-236">To obtain a VMSS object, use the Get-AzureRmVmss cmdlet.</span></span>
<span data-ttu-id="d730f-237">此虛擬機器物件包含 VMSS 的更新狀態。</span><span class="sxs-lookup"><span data-stu-id="d730f-237">This virtual machine object contains the updated state for the VMSS.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d730f-238">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="d730f-238">-VMScaleSetName</span></span>
<span data-ttu-id="d730f-239">指定此 Cmdlet 所建立之 VMSS 的名稱。</span><span class="sxs-lookup"><span data-stu-id="d730f-239">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d730f-240">-確認</span><span class="sxs-lookup"><span data-stu-id="d730f-240">-Confirm</span></span>
<span data-ttu-id="d730f-241">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d730f-241">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d730f-242">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d730f-242">-WhatIf</span></span>
<span data-ttu-id="d730f-243">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d730f-243">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="d730f-244">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d730f-244">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d730f-245">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d730f-245">CommonParameters</span></span>
<span data-ttu-id="d730f-246">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d730f-246">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d730f-247">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d730f-247">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d730f-248">輸入</span><span class="sxs-lookup"><span data-stu-id="d730f-248">INPUTS</span></span>

### <span data-ttu-id="d730f-249">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d730f-249">VirtualMachineScaleSet</span></span>
<span data-ttu-id="d730f-250">形參 "VirtualMachineScaleSet" 接受管線中 "VirtualMachineScaleSet" 類型的值</span><span class="sxs-lookup"><span data-stu-id="d730f-250">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="d730f-251">輸出</span><span class="sxs-lookup"><span data-stu-id="d730f-251">OUTPUTS</span></span>

### <span data-ttu-id="d730f-252">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="d730f-252">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="d730f-253">筆記</span><span class="sxs-lookup"><span data-stu-id="d730f-253">NOTES</span></span>

## <span data-ttu-id="d730f-254">相關連結</span><span class="sxs-lookup"><span data-stu-id="d730f-254">RELATED LINKS</span></span>

[<span data-ttu-id="d730f-255">AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d730f-255">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="d730f-256">新-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d730f-256">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="d730f-257">移除-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d730f-257">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="d730f-258">重新開機-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d730f-258">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="d730f-259">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d730f-259">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="d730f-260">開始-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d730f-260">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="d730f-261">停止 AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d730f-261">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)


