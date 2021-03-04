---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: 71aa555528ff1cdb5748c1a4ac62481ddd17c17c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912050"
---
# <span data-ttu-id="14b38-101">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="14b38-101">New-AzVMConfig</span></span>

## <span data-ttu-id="14b38-102">簡介</span><span class="sxs-lookup"><span data-stu-id="14b38-102">SYNOPSIS</span></span>
<span data-ttu-id="14b38-103">建立可配置的虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="14b38-103">Creates a configurable virtual machine object.</span></span>

## <span data-ttu-id="14b38-104">語法</span><span class="sxs-lookup"><span data-stu-id="14b38-104">SYNTAX</span></span>

### <span data-ttu-id="14b38-105">DefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="14b38-105">DefaultParameterSet (Default)</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>]
 [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD] 
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14b38-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="14b38-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>] [-MaxPrice <Double>]
 [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14b38-107">描述</span><span class="sxs-lookup"><span data-stu-id="14b38-107">DESCRIPTION</span></span>
<span data-ttu-id="14b38-108">**New-AzMSConfig** Cmdlet 會為 Azure 建立可配置的本機虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="14b38-108">The **New-AzVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="14b38-109">其他 Cmdlet 可以用來設定虛擬機器物件，例如 Set-Az VIRTUALOperatingSystem、Set-Az VIRTUALSourceImage、Add-Az VIRTUALNetworkInterface 和 Set-Az VIRTUALOSSource。</span><span class="sxs-lookup"><span data-stu-id="14b38-109">Other cmdlets can be used to configure a virtual machine object, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

## <span data-ttu-id="14b38-110">例子</span><span class="sxs-lookup"><span data-stu-id="14b38-110">EXAMPLES</span></span>

### <span data-ttu-id="14b38-111">範例 1：建立虛擬機器物件</span><span class="sxs-lookup"><span data-stu-id="14b38-111">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="14b38-112">第一個命令會獲得名為 ResourceGroup11 的資源群組中名為 AvailabilitySet03 的可用性集，然後將該物件儲存在 $AvailabilitySet 變數中。</span><span class="sxs-lookup"><span data-stu-id="14b38-112">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="14b38-113">第二個命令會建立虛擬機器物件，然後將它儲存在$VirtualMachine變數中。</span><span class="sxs-lookup"><span data-stu-id="14b38-113">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="14b38-114">該命令會為虛擬機器指定名稱和大小。</span><span class="sxs-lookup"><span data-stu-id="14b38-114">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="14b38-115">虛擬機器屬於儲存在 $AvailabilitySet 的可用性集。</span><span class="sxs-lookup"><span data-stu-id="14b38-115">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="14b38-116">參數</span><span class="sxs-lookup"><span data-stu-id="14b38-116">PARAMETERS</span></span>

### <span data-ttu-id="14b38-117">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="14b38-117">-AvailabilitySetId</span></span>
<span data-ttu-id="14b38-118">指定可用性集的識別碼。</span><span class="sxs-lookup"><span data-stu-id="14b38-118">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="14b38-119">若要取得可用性集物件，請使用 Get-AzAvailabilitySet Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="14b38-119">To obtain an availability set object, use the Get-AzAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="14b38-120">可用性集物件包含識別碼屬性。</span><span class="sxs-lookup"><span data-stu-id="14b38-120">The availability set object contains an ID property.</span></span> <br>
<span data-ttu-id="14b38-121">相同可用性集指定的虛擬機器會配置給不同的節點，以最大化可用性。</span><span class="sxs-lookup"><span data-stu-id="14b38-121">Virtual machines specified in the same availability set are allocated to different nodes to maximize availability.</span></span> <br>
<span data-ttu-id="14b38-122">有關可用性集的資訊，請參閱管理 [虛擬機器的可用性](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-manage-availability?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)。</span><span class="sxs-lookup"><span data-stu-id="14b38-122">For more information about availability sets, see [Manage the availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-manage-availability?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json).</span></span> <br>
<span data-ttu-id="14b38-123">有關 Azure 規劃維護的資訊，請參閱[Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-planned-maintenance?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)虛擬機器的規劃維護</span><span class="sxs-lookup"><span data-stu-id="14b38-123">For more information on Azure planned maintenance, see [Planned maintenance for virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-planned-maintenance?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)</span></span> <br>
<span data-ttu-id="14b38-124">目前，VM 只能在建立時新增到可用性集。</span><span class="sxs-lookup"><span data-stu-id="14b38-124">Currently, a VM can only be added to availability set at creation time.</span></span> <span data-ttu-id="14b38-125">要新增 VM 的可用性集應位於與可用性集資源相同的資源群組下。</span><span class="sxs-lookup"><span data-stu-id="14b38-125">The availability set to which the VM is being added should be under the same resource group as the availability set resource.</span></span> <span data-ttu-id="14b38-126">現有的 VM 無法新增到可用性集。</span><span class="sxs-lookup"><span data-stu-id="14b38-126">An existing VM cannot be added to an availability set.</span></span> <br>
<span data-ttu-id="14b38-127">此屬性無法與非 Null properties.virtualMachineScaleSet 參照一起存在。</span><span class="sxs-lookup"><span data-stu-id="14b38-127">This property cannot exist along with a non-null properties.virtualMachineScaleSet reference.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14b38-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14b38-128">-DefaultProfile</span></span>
<span data-ttu-id="14b38-129">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="14b38-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14b38-130">-EnableUltrasSD</span><span class="sxs-lookup"><span data-stu-id="14b38-130">-EnableUltraSSD</span></span>
<span data-ttu-id="14b38-131">啟用在 VM 上具有一或多個受管理的資料UltraSSD_LRS儲存空間帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="14b38-131">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="14b38-132">只有啟用此屬性UltraSSD_LRS才能將具有儲存帳戶類型的受管理磁片新增到虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="14b38-132">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>


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

### <span data-ttu-id="14b38-133">-Policy</span><span class="sxs-lookup"><span data-stu-id="14b38-133">-EvictionPolicy</span></span>
<span data-ttu-id="14b38-134">Azure Spot 虛擬機器的回收政策。</span><span class="sxs-lookup"><span data-stu-id="14b38-134">The eviction policy for the Azure Spot virtual machine.</span></span>  <span data-ttu-id="14b38-135">支援的值為 'Deallocate' 和 'Delete'。</span><span class="sxs-lookup"><span data-stu-id="14b38-135">Supported values are 'Deallocate' and 'Delete'.</span></span>

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

### <span data-ttu-id="14b38-136">-HostId</span><span class="sxs-lookup"><span data-stu-id="14b38-136">-HostId</span></span>
<span data-ttu-id="14b38-137">主機名稱</span><span class="sxs-lookup"><span data-stu-id="14b38-137">The Id of Host</span></span>

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

### <span data-ttu-id="14b38-138">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="14b38-138">-IdentityId</span></span>
<span data-ttu-id="14b38-139">指定與虛擬機器縮放比例集相關聯的使用者身分設定清單。</span><span class="sxs-lookup"><span data-stu-id="14b38-139">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="14b38-140">使用者身分識別參照為表單中的 ARM 資源識別碼：'/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identityies/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="14b38-140">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="14b38-141">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="14b38-141">-IdentityType</span></span>
<span data-ttu-id="14b38-142">虛擬機器的身分識別 ，如果已配置。</span><span class="sxs-lookup"><span data-stu-id="14b38-142">The identity of the virtual machine, if configured.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14b38-143">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="14b38-143">-LicenseType</span></span>
<span data-ttu-id="14b38-144">指定授權類型，表示虛擬機器的映射或磁片已授權于內部部署。</span><span class="sxs-lookup"><span data-stu-id="14b38-144">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="14b38-145">Windows Server 的可能值為：</span><span class="sxs-lookup"><span data-stu-id="14b38-145">Possible values for Windows Server are:</span></span>
- <span data-ttu-id="14b38-146">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="14b38-146">Windows_Client</span></span>
- <span data-ttu-id="14b38-147">Windows_Server Linux Server 作業系統的可能值有：</span><span class="sxs-lookup"><span data-stu-id="14b38-147">Windows_Server Possible values for Linux Server operating system are:</span></span> 
- <span data-ttu-id="14b38-148">RHEL_BYOS (RHEL) </span><span class="sxs-lookup"><span data-stu-id="14b38-148">RHEL_BYOS (for RHEL)</span></span> 
- <span data-ttu-id="14b38-149">SLES_BYOS (SUSE) </span><span class="sxs-lookup"><span data-stu-id="14b38-149">SLES_BYOS (for SUSE)</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14b38-150">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="14b38-150">-MaxPrice</span></span>
<span data-ttu-id="14b38-151">指定您願意為低優先順序 VM/VMSS 支付的最高價格。</span><span class="sxs-lookup"><span data-stu-id="14b38-151">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="14b38-152">此價格為美元。</span><span class="sxs-lookup"><span data-stu-id="14b38-152">This price is in US Dollars.</span></span> <span data-ttu-id="14b38-153">此價格會與 VM 大小目前低優先順序價格進行比較。</span><span class="sxs-lookup"><span data-stu-id="14b38-153">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="14b38-154">此外，在建立/更新低優先順序 VM/VMSS 時，會比較價格，且只有在 maxPrice 大於目前低優先順序價格時，作業才能成功。</span><span class="sxs-lookup"><span data-stu-id="14b38-154">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="14b38-155">如果建立 VM/VMSS 之後，目前的低優先順序價格超出 maxPrice，maxPrice 也會用於評估低優先順序的 VM/VMSS。</span><span class="sxs-lookup"><span data-stu-id="14b38-155">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="14b38-156">可能的值為：任何大於零的十進位值。</span><span class="sxs-lookup"><span data-stu-id="14b38-156">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="14b38-157">範例：0.01538。</span><span class="sxs-lookup"><span data-stu-id="14b38-157">Example: 0.01538.</span></span>  <span data-ttu-id="14b38-158">-1 表示基於價格考慮，不應將低優先順序的 VM/VMSS 從上而退出。</span><span class="sxs-lookup"><span data-stu-id="14b38-158">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="14b38-159">此外，如果您未提供，預設最高價格為 -1。</span><span class="sxs-lookup"><span data-stu-id="14b38-159">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="14b38-160">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="14b38-160">-EncryptionAtHost</span></span>
<span data-ttu-id="14b38-161">使用者可在要求中使用 EncryptionAtHost 屬性，以啟用或停用虛擬機器或虛擬機器縮放集的主機加密。</span><span class="sxs-lookup"><span data-stu-id="14b38-161">EncryptionAtHost property can be used by user in the request to enable or disable the Host Encryption for the virtual machine or virtual machine scale set.</span></span> <span data-ttu-id="14b38-162">這會啟用所有磁片的加密，包括主機本身的資源/Temp 磁片。</span><span class="sxs-lookup"><span data-stu-id="14b38-162">This will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="14b38-163">預設：除非資源的此屬性設為 True，否則會停用主機的加密。</span><span class="sxs-lookup"><span data-stu-id="14b38-163">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

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

### <span data-ttu-id="14b38-164">-優先順序</span><span class="sxs-lookup"><span data-stu-id="14b38-164">-Priority</span></span>
<span data-ttu-id="14b38-165">虛擬機器的優先順序。</span><span class="sxs-lookup"><span data-stu-id="14b38-165">The priority for the virtual machine.</span></span>  <span data-ttu-id="14b38-166">只有支援的值是 "Regular"、'Spot' 和 'Low'。</span><span class="sxs-lookup"><span data-stu-id="14b38-166">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="14b38-167">"Regular" 適用于一般虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="14b38-167">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="14b38-168">"Spot" 適用于 Spot 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="14b38-168">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="14b38-169">"Low" 也適用于 Spot 虛擬機器，但會由 "Spot" 取代。</span><span class="sxs-lookup"><span data-stu-id="14b38-169">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="14b38-170">請使用 "Spot" 而不是 "Low"。</span><span class="sxs-lookup"><span data-stu-id="14b38-170">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="14b38-171">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="14b38-171">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="14b38-172">要用於此虛擬機器的鄰近位置群組資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="14b38-172">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

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

### <span data-ttu-id="14b38-173">-標記</span><span class="sxs-lookup"><span data-stu-id="14b38-173">-Tags</span></span>
<span data-ttu-id="14b38-174">附加至資源的標記。</span><span class="sxs-lookup"><span data-stu-id="14b38-174">The tags attached to the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14b38-175">-VMName</span><span class="sxs-lookup"><span data-stu-id="14b38-175">-VMName</span></span>
<span data-ttu-id="14b38-176">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="14b38-176">Specifies a name for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14b38-177">-VMSize</span><span class="sxs-lookup"><span data-stu-id="14b38-177">-VMSize</span></span>
<span data-ttu-id="14b38-178">指定虛擬機器的大小。</span><span class="sxs-lookup"><span data-stu-id="14b38-178">Specifies the size for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14b38-179">-VmssId</span><span class="sxs-lookup"><span data-stu-id="14b38-179">-VmssId</span></span>
<span data-ttu-id="14b38-180">虛擬機器縮放集的識別碼</span><span class="sxs-lookup"><span data-stu-id="14b38-180">The Id of virtual machine scale set</span></span>

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

### <span data-ttu-id="14b38-181">-區域</span><span class="sxs-lookup"><span data-stu-id="14b38-181">-Zone</span></span>
<span data-ttu-id="14b38-182">指定虛擬機器的可用性區域清單。</span><span class="sxs-lookup"><span data-stu-id="14b38-182">Specifies the availability zone list for the virtual machine.</span></span> <span data-ttu-id="14b38-183">允許的值取決於區域的功能。</span><span class="sxs-lookup"><span data-stu-id="14b38-183">The allowed values depend on the capabilities of the region.</span></span> <span data-ttu-id="14b38-184">允許的值通常會是 1，2，3。</span><span class="sxs-lookup"><span data-stu-id="14b38-184">Allowed values will normally be 1,2,3.</span></span>

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

### <span data-ttu-id="14b38-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14b38-185">CommonParameters</span></span>
<span data-ttu-id="14b38-186">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="14b38-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14b38-187">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="14b38-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14b38-188">輸入</span><span class="sxs-lookup"><span data-stu-id="14b38-188">INPUTS</span></span>

### <span data-ttu-id="14b38-189">System.String</span><span class="sxs-lookup"><span data-stu-id="14b38-189">System.String</span></span>

### <span data-ttu-id="14b38-190">System.String[]</span><span class="sxs-lookup"><span data-stu-id="14b38-190">System.String[]</span></span>

### <span data-ttu-id="14b38-191">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="14b38-191">System.Collections.Hashtable</span></span>

### <span data-ttu-id="14b38-192">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="14b38-192">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="14b38-193">輸出</span><span class="sxs-lookup"><span data-stu-id="14b38-193">OUTPUTS</span></span>

### <span data-ttu-id="14b38-194">Microsoft.Azure.Commands.Compute.models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="14b38-194">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="14b38-195">筆記</span><span class="sxs-lookup"><span data-stu-id="14b38-195">NOTES</span></span>

## <span data-ttu-id="14b38-196">相關連結</span><span class="sxs-lookup"><span data-stu-id="14b38-196">RELATED LINKS</span></span>

[<span data-ttu-id="14b38-197">Update-AzMS</span><span class="sxs-lookup"><span data-stu-id="14b38-197">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="14b38-198">Set-AzEVOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="14b38-198">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="14b38-199">Set-AzEVSourceImage</span><span class="sxs-lookup"><span data-stu-id="14b38-199">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="14b38-200">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="14b38-200">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)


