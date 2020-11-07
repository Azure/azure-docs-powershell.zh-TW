---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: 5e3bafbc667cc0e26eb6469e681ca9355b4f307f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795817"
---
# <span data-ttu-id="c9f17-101">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c9f17-101">Update-AzVmss</span></span>

## <span data-ttu-id="c9f17-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c9f17-102">SYNOPSIS</span></span>
<span data-ttu-id="c9f17-103">更新 VMSS 的狀態。</span><span class="sxs-lookup"><span data-stu-id="c9f17-103">Updates the state of a VMSS.</span></span>

## <span data-ttu-id="c9f17-104">句法</span><span class="sxs-lookup"><span data-stu-id="c9f17-104">SYNTAX</span></span>

### <span data-ttu-id="c9f17-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="c9f17-105">DefaultParameter (Default)</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
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

### <span data-ttu-id="c9f17-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9f17-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
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

## <span data-ttu-id="c9f17-107">說明</span><span class="sxs-lookup"><span data-stu-id="c9f17-107">DESCRIPTION</span></span>
<span data-ttu-id="c9f17-108">**更新-AzVmss** Cmdlet 會更新虛擬機器縮放集 (VMSS) 的狀態設定為局部 VMSS 物件的狀態。</span><span class="sxs-lookup"><span data-stu-id="c9f17-108">The **Update-AzVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="c9f17-109">示例</span><span class="sxs-lookup"><span data-stu-id="c9f17-109">EXAMPLES</span></span>

### <span data-ttu-id="c9f17-110">範例1：更新 VMSS 的狀態至本機 VMSS 物件的狀態。</span><span class="sxs-lookup"><span data-stu-id="c9f17-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="c9f17-111">這個命令會將屬於名為 Group001 之資源群組之 VMSS001 的 VMSS 狀態更新為本機 VMSS 物件的狀態，$LocalVMSS。</span><span class="sxs-lookup"><span data-stu-id="c9f17-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="c9f17-112">參數</span><span class="sxs-lookup"><span data-stu-id="c9f17-112">PARAMETERS</span></span>

### <span data-ttu-id="c9f17-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c9f17-113">-AsJob</span></span>
<span data-ttu-id="c9f17-114">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="c9f17-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="c9f17-115">-AutomaticOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="c9f17-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="c9f17-116">設定更新版本的影像時，是否應該將作業系統升級自動套用到縮放集實例，以滾動的方式進行。</span><span class="sxs-lookup"><span data-stu-id="c9f17-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="c9f17-117">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="c9f17-117">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="c9f17-118">是否應該在虛擬機器規模集上啟用引導診斷程式。</span><span class="sxs-lookup"><span data-stu-id="c9f17-118">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="c9f17-119">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="c9f17-119">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="c9f17-120">要用來放置主控台輸出和螢幕擷取畫面的儲存空間帳戶 URI。</span><span class="sxs-lookup"><span data-stu-id="c9f17-120">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="c9f17-121">-CustomData</span><span class="sxs-lookup"><span data-stu-id="c9f17-121">-CustomData</span></span>
<span data-ttu-id="c9f17-122">指定自訂資料的基本64編碼字串。</span><span class="sxs-lookup"><span data-stu-id="c9f17-122">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="c9f17-123">這會解碼為二進位陣列，並儲存為虛擬機器上的檔案。</span><span class="sxs-lookup"><span data-stu-id="c9f17-123">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="c9f17-124">二進位陣列的最大長度為65535個位元組。</span><span class="sxs-lookup"><span data-stu-id="c9f17-124">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="c9f17-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9f17-125">-DefaultProfile</span></span>
<span data-ttu-id="c9f17-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c9f17-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9f17-127">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="c9f17-127">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="c9f17-128">表示此 Cmdlet 停用 Linux 作業系統的密碼驗證。</span><span class="sxs-lookup"><span data-stu-id="c9f17-128">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

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

### <span data-ttu-id="c9f17-129">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="c9f17-129">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="c9f17-130">指出是否已針對自動更新啟用 VMSS 中的 Windows 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="c9f17-130">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="c9f17-131">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="c9f17-131">-IdentityId</span></span>
<span data-ttu-id="c9f17-132">指定與虛擬機器小性集相關聯的使用者識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="c9f17-132">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="c9f17-133">使用者身分識別參照將是下列形式的 ARM 資源識別碼： '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="c9f17-133">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="c9f17-134">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="c9f17-134">-IdentityType</span></span>
<span data-ttu-id="c9f17-135">指定用於虛擬機器規模集的身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="c9f17-135">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="c9f17-136">"SystemAssignedUserAssigned" 類型包含隱含建立的身分識別，以及一組使用者指派的身分識別。</span><span class="sxs-lookup"><span data-stu-id="c9f17-136">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="c9f17-137">"None" 類型將會移除虛擬機器小單位集中的任何身分識別。</span><span class="sxs-lookup"><span data-stu-id="c9f17-137">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="c9f17-138">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="c9f17-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c9f17-139">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="c9f17-139">SystemAssigned</span></span>
- <span data-ttu-id="c9f17-140">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="c9f17-140">UserAssigned</span></span>
- <span data-ttu-id="c9f17-141">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="c9f17-141">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="c9f17-142">所有</span><span class="sxs-lookup"><span data-stu-id="c9f17-142">None</span></span>

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

### <span data-ttu-id="c9f17-143">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="c9f17-143">-ImageReferenceId</span></span>
<span data-ttu-id="c9f17-144">指定影像參照 ID。</span><span class="sxs-lookup"><span data-stu-id="c9f17-144">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="c9f17-145">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="c9f17-145">-ImageReferenceOffer</span></span>
<span data-ttu-id="c9f17-146">指定 (VMImage) 優惠的虛擬機器影像類型。</span><span class="sxs-lookup"><span data-stu-id="c9f17-146">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="c9f17-147">若要取得影像優惠，請使用 Get-AzVMImageOffer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c9f17-147">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="c9f17-148">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="c9f17-148">-ImageReferencePublisher</span></span>
<span data-ttu-id="c9f17-149">指定 VMImage 發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="c9f17-149">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="c9f17-150">若要取得發行者，請使用 Get-AzVMImagePublisher Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c9f17-150">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="c9f17-151">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="c9f17-151">-ImageReferenceSku</span></span>
<span data-ttu-id="c9f17-152">指定 VMImage SKU。</span><span class="sxs-lookup"><span data-stu-id="c9f17-152">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="c9f17-153">若要取得 Sku，請使用 Get-AzVMImageSku Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c9f17-153">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="c9f17-154">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="c9f17-154">-ImageReferenceVersion</span></span>
<span data-ttu-id="c9f17-155">指定 VMImage 的版本。</span><span class="sxs-lookup"><span data-stu-id="c9f17-155">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="c9f17-156">若要使用最新版本，請指定最新的值，而不是特定的版本。</span><span class="sxs-lookup"><span data-stu-id="c9f17-156">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="c9f17-157">-ImageUri</span><span class="sxs-lookup"><span data-stu-id="c9f17-157">-ImageUri</span></span>
<span data-ttu-id="c9f17-158">指定使用者影像的 blob URI。</span><span class="sxs-lookup"><span data-stu-id="c9f17-158">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="c9f17-159">VMSS 會在使用者影像的同一個容器中建立作業系統磁片。</span><span class="sxs-lookup"><span data-stu-id="c9f17-159">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="c9f17-160">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="c9f17-160">-LicenseType</span></span>
<span data-ttu-id="c9f17-161">指定授權類型，這是用來提供您自己的授權案例。</span><span class="sxs-lookup"><span data-stu-id="c9f17-161">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="c9f17-162">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="c9f17-162">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="c9f17-163">指定受管理磁片的儲存帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="c9f17-163">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="c9f17-164">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="c9f17-164">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c9f17-165">StandardLRS</span><span class="sxs-lookup"><span data-stu-id="c9f17-165">StandardLRS</span></span>
- <span data-ttu-id="c9f17-166">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="c9f17-166">PremiumLRS</span></span>

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

### <span data-ttu-id="c9f17-167">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="c9f17-167">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="c9f17-168">輪流升級在一批中同時升級之總虛擬機器實例的最大百分比。</span><span class="sxs-lookup"><span data-stu-id="c9f17-168">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="c9f17-169">如此一來，在前一個或將來的批次中，可能會導致批次中的實例百分比下降，以確保較高的可靠性。</span><span class="sxs-lookup"><span data-stu-id="c9f17-169">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="c9f17-170">如果未指定值，則會將該值設定為20。</span><span class="sxs-lookup"><span data-stu-id="c9f17-170">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="c9f17-171">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="c9f17-171">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="c9f17-172">在輪流升級中止前，規模集中可同時進行升級的虛擬機器實例總數，或由虛擬機器健康情況檢查所顯示的總虛擬機器實例的最大百分比。</span><span class="sxs-lookup"><span data-stu-id="c9f17-172">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="c9f17-173">在開始任何批次之前，將會檢查此限制。</span><span class="sxs-lookup"><span data-stu-id="c9f17-173">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="c9f17-174">如果未指定值，則會將該值設定為20。</span><span class="sxs-lookup"><span data-stu-id="c9f17-174">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="c9f17-175">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="c9f17-175">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="c9f17-176">可發現處於不正常狀態之已升級虛擬機器實例的最大百分比。</span><span class="sxs-lookup"><span data-stu-id="c9f17-176">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="c9f17-177">這項檢查會在每個批次升級後發生。</span><span class="sxs-lookup"><span data-stu-id="c9f17-177">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="c9f17-178">如果曾經超過此百分比，則滾動更新會中止。</span><span class="sxs-lookup"><span data-stu-id="c9f17-178">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="c9f17-179">如果未指定值，則會將該值設定為20。</span><span class="sxs-lookup"><span data-stu-id="c9f17-179">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="c9f17-180">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="c9f17-180">-OsDiskCaching</span></span>
<span data-ttu-id="c9f17-181">指定作業系統磁片的快取模式。</span><span class="sxs-lookup"><span data-stu-id="c9f17-181">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="c9f17-182">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="c9f17-182">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c9f17-183">所有</span><span class="sxs-lookup"><span data-stu-id="c9f17-183">None</span></span>
- <span data-ttu-id="c9f17-184">唯讀</span><span class="sxs-lookup"><span data-stu-id="c9f17-184">ReadOnly</span></span>
- <span data-ttu-id="c9f17-185">讀</span><span class="sxs-lookup"><span data-stu-id="c9f17-185">ReadWrite</span></span>

<span data-ttu-id="c9f17-186">預設值為 ReadWrite。</span><span class="sxs-lookup"><span data-stu-id="c9f17-186">The default value is ReadWrite.</span></span>
<span data-ttu-id="c9f17-187">如果您變更快取值，Cmdlet 會重新開機虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="c9f17-187">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>

<span data-ttu-id="c9f17-188">此設定會影響磁片的一致性和效能。</span><span class="sxs-lookup"><span data-stu-id="c9f17-188">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="c9f17-189">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="c9f17-189">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="c9f17-190">指定是否應該在 OS 磁片上啟用或停用 WriteAccelerator。</span><span class="sxs-lookup"><span data-stu-id="c9f17-190">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="c9f17-191">-Overprovision</span><span class="sxs-lookup"><span data-stu-id="c9f17-191">-Overprovision</span></span>
<span data-ttu-id="c9f17-192">指示 Cmdlet 是否 overprovisions VMSS。</span><span class="sxs-lookup"><span data-stu-id="c9f17-192">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="c9f17-193">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="c9f17-193">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="c9f17-194">在一批中完成所有虛擬機器的更新與開始下一個批次之間的等待時間。</span><span class="sxs-lookup"><span data-stu-id="c9f17-194">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="c9f17-195">應以 ISO 8601 格式指定持續時間。</span><span class="sxs-lookup"><span data-stu-id="c9f17-195">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="c9f17-196">預設值為0秒 (PT0S) 。</span><span class="sxs-lookup"><span data-stu-id="c9f17-196">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="c9f17-197">-PlanName</span><span class="sxs-lookup"><span data-stu-id="c9f17-197">-PlanName</span></span>
<span data-ttu-id="c9f17-198">指定方案名稱。</span><span class="sxs-lookup"><span data-stu-id="c9f17-198">Specifies the plan name.</span></span>

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

### <span data-ttu-id="c9f17-199">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="c9f17-199">-PlanProduct</span></span>
<span data-ttu-id="c9f17-200">指定方案產品。</span><span class="sxs-lookup"><span data-stu-id="c9f17-200">Specifies the plan product.</span></span>

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

### <span data-ttu-id="c9f17-201">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="c9f17-201">-PlanPromotionCode</span></span>
<span data-ttu-id="c9f17-202">指定方案促銷代碼。</span><span class="sxs-lookup"><span data-stu-id="c9f17-202">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="c9f17-203">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="c9f17-203">-PlanPublisher</span></span>
<span data-ttu-id="c9f17-204">指定方案發行者。</span><span class="sxs-lookup"><span data-stu-id="c9f17-204">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="c9f17-205">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="c9f17-205">-ProvisionVMAgent</span></span>
<span data-ttu-id="c9f17-206">指出是否應該在 VMSS 中的 Windows 虛擬機器上預配虛擬機器代理程式。</span><span class="sxs-lookup"><span data-stu-id="c9f17-206">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="c9f17-207">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9f17-207">-ResourceGroupName</span></span>
<span data-ttu-id="c9f17-208">指定 VMSS 所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c9f17-208">Specifies the name of the resource group the VMSS belongs to.</span></span>

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

### <span data-ttu-id="c9f17-209">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="c9f17-209">-SinglePlacementGroup</span></span>
<span data-ttu-id="c9f17-210">指定單一位置群組。</span><span class="sxs-lookup"><span data-stu-id="c9f17-210">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="c9f17-211">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="c9f17-211">-SkuCapacity</span></span>
<span data-ttu-id="c9f17-212">指定 VMSS 中的實例數。</span><span class="sxs-lookup"><span data-stu-id="c9f17-212">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="c9f17-213">-SkuName</span><span class="sxs-lookup"><span data-stu-id="c9f17-213">-SkuName</span></span>
<span data-ttu-id="c9f17-214">指定 VMSS 的所有實例大小。</span><span class="sxs-lookup"><span data-stu-id="c9f17-214">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="c9f17-215">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="c9f17-215">-SkuTier</span></span>
<span data-ttu-id="c9f17-216">指定 VMSS 的層級。</span><span class="sxs-lookup"><span data-stu-id="c9f17-216">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="c9f17-217">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="c9f17-217">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c9f17-218">標準</span><span class="sxs-lookup"><span data-stu-id="c9f17-218">Standard</span></span>
- <span data-ttu-id="c9f17-219">空白</span><span class="sxs-lookup"><span data-stu-id="c9f17-219">Basic</span></span>

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

### <span data-ttu-id="c9f17-220">-Tag</span><span class="sxs-lookup"><span data-stu-id="c9f17-220">-Tag</span></span>
<span data-ttu-id="c9f17-221">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="c9f17-221">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c9f17-222">例如：</span><span class="sxs-lookup"><span data-stu-id="c9f17-222">For example:</span></span>

<span data-ttu-id="c9f17-223">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="c9f17-223">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c9f17-224">-時區</span><span class="sxs-lookup"><span data-stu-id="c9f17-224">-TimeZone</span></span>
<span data-ttu-id="c9f17-225">指定 Windows 作業系統的時區。</span><span class="sxs-lookup"><span data-stu-id="c9f17-225">Specifies the time zone for Windows OS.</span></span>

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

### <span data-ttu-id="c9f17-226">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="c9f17-226">-UpgradePolicyMode</span></span>
<span data-ttu-id="c9f17-227">已指定升級模式至規模集中的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="c9f17-227">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="c9f17-228">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="c9f17-228">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c9f17-229">自動</span><span class="sxs-lookup"><span data-stu-id="c9f17-229">Automatic</span></span>
- <span data-ttu-id="c9f17-230">手動</span><span class="sxs-lookup"><span data-stu-id="c9f17-230">Manual</span></span>
- <span data-ttu-id="c9f17-231">擲</span><span class="sxs-lookup"><span data-stu-id="c9f17-231">Rolling</span></span>

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

### <span data-ttu-id="c9f17-232">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="c9f17-232">-VhdContainer</span></span>
<span data-ttu-id="c9f17-233">指定用來儲存 VMSS 作業系統磁片的容器 Url。</span><span class="sxs-lookup"><span data-stu-id="c9f17-233">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="c9f17-234">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c9f17-234">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="c9f17-235">指定本機 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="c9f17-235">Specifies a local VMSS object.</span></span>
<span data-ttu-id="c9f17-236">若要取得 VMSS 物件，請使用 Get-AzVmss Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c9f17-236">To obtain a VMSS object, use the Get-AzVmss cmdlet.</span></span>
<span data-ttu-id="c9f17-237">此虛擬機器物件包含 VMSS 的更新狀態。</span><span class="sxs-lookup"><span data-stu-id="c9f17-237">This virtual machine object contains the updated state for the VMSS.</span></span>

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

### <span data-ttu-id="c9f17-238">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="c9f17-238">-VMScaleSetName</span></span>
<span data-ttu-id="c9f17-239">指定此 Cmdlet 所建立之 VMSS 的名稱。</span><span class="sxs-lookup"><span data-stu-id="c9f17-239">Specifies the name of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="c9f17-240">-確認</span><span class="sxs-lookup"><span data-stu-id="c9f17-240">-Confirm</span></span>
<span data-ttu-id="c9f17-241">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c9f17-241">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9f17-242">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9f17-242">-WhatIf</span></span>
<span data-ttu-id="c9f17-243">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c9f17-243">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="c9f17-244">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c9f17-244">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9f17-245">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9f17-245">CommonParameters</span></span>
<span data-ttu-id="c9f17-246">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c9f17-246">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9f17-247">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c9f17-247">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9f17-248">輸入</span><span class="sxs-lookup"><span data-stu-id="c9f17-248">INPUTS</span></span>

### <span data-ttu-id="c9f17-249">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c9f17-249">VirtualMachineScaleSet</span></span>
<span data-ttu-id="c9f17-250">形參 "VirtualMachineScaleSet" 接受管線中 "VirtualMachineScaleSet" 類型的值</span><span class="sxs-lookup"><span data-stu-id="c9f17-250">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="c9f17-251">輸出</span><span class="sxs-lookup"><span data-stu-id="c9f17-251">OUTPUTS</span></span>

### <span data-ttu-id="c9f17-252">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="c9f17-252">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="c9f17-253">筆記</span><span class="sxs-lookup"><span data-stu-id="c9f17-253">NOTES</span></span>

## <span data-ttu-id="c9f17-254">相關連結</span><span class="sxs-lookup"><span data-stu-id="c9f17-254">RELATED LINKS</span></span>

[<span data-ttu-id="c9f17-255">AzVmss</span><span class="sxs-lookup"><span data-stu-id="c9f17-255">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="c9f17-256">新-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c9f17-256">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="c9f17-257">移除-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c9f17-257">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="c9f17-258">重新開機-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c9f17-258">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="c9f17-259">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c9f17-259">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="c9f17-260">開始-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c9f17-260">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="c9f17-261">停止 AzVmss</span><span class="sxs-lookup"><span data-stu-id="c9f17-261">Stop-AzVmss</span></span>](./Stop-AzVmss.md)


