---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: 8c20a6be76f77a74082090d1386054a23b9b9ea0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139852"
---
# <span data-ttu-id="55613-101">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="55613-101">New-AzVMConfig</span></span>

## <span data-ttu-id="55613-102">摘要</span><span class="sxs-lookup"><span data-stu-id="55613-102">SYNOPSIS</span></span>
<span data-ttu-id="55613-103">建立可設定的虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="55613-103">Creates a configurable virtual machine object.</span></span>

## <span data-ttu-id="55613-104">句法</span><span class="sxs-lookup"><span data-stu-id="55613-104">SYNTAX</span></span>

### <span data-ttu-id="55613-105">DefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="55613-105">DefaultParameterSet (Default)</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>]
 [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD] 
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55613-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="55613-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>] [-MaxPrice <Double>]
 [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55613-107">說明</span><span class="sxs-lookup"><span data-stu-id="55613-107">DESCRIPTION</span></span>
<span data-ttu-id="55613-108">**新的-AzVMConfig** Cmdlet 會為 Azure 建立可設定的本機虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="55613-108">The **New-AzVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="55613-109">您可以使用其他 Cmdlet 來設定虛擬機器物件，例如設定 AzVMOperatingSystem、AzVMSourceImage、Add-AzVMNetworkInterface，以及 Set-AzVMOSDisk。</span><span class="sxs-lookup"><span data-stu-id="55613-109">Other cmdlets can be used to configure a virtual machine object, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

## <span data-ttu-id="55613-110">示例</span><span class="sxs-lookup"><span data-stu-id="55613-110">EXAMPLES</span></span>

### <span data-ttu-id="55613-111">範例1：建立虛擬電腦物件</span><span class="sxs-lookup"><span data-stu-id="55613-111">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="55613-112">第一個命令會在名為 [ResourceGroup11] 的資源群組中取得名為 AvailabilitySet03 的可用性集，然後將該物件儲存在 $AvailabilitySet 變數中。</span><span class="sxs-lookup"><span data-stu-id="55613-112">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="55613-113">第二個命令會建立一個虛擬電腦物件，然後將它儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="55613-113">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="55613-114">該命令會將名稱和大小指派給虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="55613-114">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="55613-115">虛擬機器屬於儲存在 $AvailabilitySet 的可用性集。</span><span class="sxs-lookup"><span data-stu-id="55613-115">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="55613-116">參數</span><span class="sxs-lookup"><span data-stu-id="55613-116">PARAMETERS</span></span>

### <span data-ttu-id="55613-117">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="55613-117">-AvailabilitySetId</span></span>
<span data-ttu-id="55613-118">指定可用性集的 ID。</span><span class="sxs-lookup"><span data-stu-id="55613-118">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="55613-119">若要取得可用性集物件，請使用 Get-AzAvailabilitySet Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="55613-119">To obtain an availability set object, use the Get-AzAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="55613-120">可用性集物件包含識別碼屬性。</span><span class="sxs-lookup"><span data-stu-id="55613-120">The availability set object contains an ID property.</span></span> <br>
<span data-ttu-id="55613-121">相同可用性集中指定的虛擬機器會指派給不同的節點，以最大化可用性。</span><span class="sxs-lookup"><span data-stu-id="55613-121">Virtual machines specified in the same availability set are allocated to different nodes to maximize availability.</span></span> <br>
<span data-ttu-id="55613-122">如需可用性集的詳細資訊，請參閱 [管理虛擬機器的可用性](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-manage-availability?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)。</span><span class="sxs-lookup"><span data-stu-id="55613-122">For more information about availability sets, see [Manage the availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-manage-availability?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json).</span></span> <br>
<span data-ttu-id="55613-123">如需有關 Azure 規劃維護的詳細資訊，請參閱 [在 azure 中針對虛擬機器進行的規劃維護](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-planned-maintenance?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="55613-123">For more information on Azure planned maintenance, see [Planned maintenance for virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-planned-maintenance?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)</span></span> <br>
<span data-ttu-id="55613-124">目前，VM 只能在建立時新增至可用性集。</span><span class="sxs-lookup"><span data-stu-id="55613-124">Currently, a VM can only be added to availability set at creation time.</span></span> <span data-ttu-id="55613-125">要新增 VM 的可用性集，必須位於與可用性集資源相同的資源群組底下。</span><span class="sxs-lookup"><span data-stu-id="55613-125">The availability set to which the VM is being added should be under the same resource group as the availability set resource.</span></span> <span data-ttu-id="55613-126">無法將現有的 VM 新增至可用性集。</span><span class="sxs-lookup"><span data-stu-id="55613-126">An existing VM cannot be added to an availability set.</span></span> <br>
<span data-ttu-id="55613-127">這個屬性不能與非 null 屬性一起存在。 virtualMachineScaleSet 參考。</span><span class="sxs-lookup"><span data-stu-id="55613-127">This property cannot exist along with a non-null properties.virtualMachineScaleSet reference.</span></span>

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

### <span data-ttu-id="55613-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55613-128">-DefaultProfile</span></span>
<span data-ttu-id="55613-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="55613-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55613-130">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="55613-130">-EnableUltraSSD</span></span>
<span data-ttu-id="55613-131">可讓一或多個受管理的資料磁片使用 VM 上的 UltraSSD_LRS 儲存帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="55613-131">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="55613-132">只有在啟用此屬性時，才能將儲存帳戶類型 UltraSSD_LRS 的受管理磁片新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="55613-132">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>


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

### <span data-ttu-id="55613-133">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="55613-133">-EvictionPolicy</span></span>
<span data-ttu-id="55613-134">Azure 點虛擬機器的逐出原則。</span><span class="sxs-lookup"><span data-stu-id="55613-134">The eviction policy for the Azure Spot virtual machine.</span></span>  <span data-ttu-id="55613-135">支援的值為 "解除配置" 和 "Delete"。</span><span class="sxs-lookup"><span data-stu-id="55613-135">Supported values are 'Deallocate' and 'Delete'.</span></span>

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

### <span data-ttu-id="55613-136">-HostId</span><span class="sxs-lookup"><span data-stu-id="55613-136">-HostId</span></span>
<span data-ttu-id="55613-137">主機的識別碼</span><span class="sxs-lookup"><span data-stu-id="55613-137">The Id of Host</span></span>

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

### <span data-ttu-id="55613-138">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="55613-138">-IdentityId</span></span>
<span data-ttu-id="55613-139">指定與虛擬機器小性集相關聯的使用者識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="55613-139">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="55613-140">使用者身分識別參照將是下列形式的 ARM 資源識別碼： '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="55613-140">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="55613-141">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="55613-141">-IdentityType</span></span>
<span data-ttu-id="55613-142">虛擬機器的身分識別（如果已設定）。</span><span class="sxs-lookup"><span data-stu-id="55613-142">The identity of the virtual machine, if configured.</span></span>

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

### <span data-ttu-id="55613-143">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="55613-143">-LicenseType</span></span>
<span data-ttu-id="55613-144">授權類型，可用於提供您自己的授權案例。</span><span class="sxs-lookup"><span data-stu-id="55613-144">The license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="55613-145">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="55613-145">-MaxPrice</span></span>
<span data-ttu-id="55613-146">指定低優先順序 VM/VMSS 要支付的最大價格。</span><span class="sxs-lookup"><span data-stu-id="55613-146">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="55613-147">這個價格是美元。</span><span class="sxs-lookup"><span data-stu-id="55613-147">This price is in US Dollars.</span></span> <span data-ttu-id="55613-148">此價格將與 VM 大小的目前低優先順序價格進行比較。</span><span class="sxs-lookup"><span data-stu-id="55613-148">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="55613-149">此外，價格會在建立/更新低優先順序 VM/VMSS 的時間進行比較，而且只有在 maxPrice 大於目前的低優先順序價格時，作業才會成功。</span><span class="sxs-lookup"><span data-stu-id="55613-149">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="55613-150">如果在建立 VM/VMSS 之後，目前的低優先順序價格超過 maxPrice，則 maxPrice 也會用於逐出低優先順序 VM/VMSS。</span><span class="sxs-lookup"><span data-stu-id="55613-150">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="55613-151">可能的值為：任何大於零的十進位值。</span><span class="sxs-lookup"><span data-stu-id="55613-151">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="55613-152">範例：0.01538。</span><span class="sxs-lookup"><span data-stu-id="55613-152">Example: 0.01538.</span></span>  <span data-ttu-id="55613-153">-1 表示由於價格原因，不應逐出低優先順序 VM/VMSS。</span><span class="sxs-lookup"><span data-stu-id="55613-153">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="55613-154">此外，如果您沒有提供預設的最大價格，就是-1。</span><span class="sxs-lookup"><span data-stu-id="55613-154">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="55613-155">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="55613-155">-EncryptionAtHost</span></span>
<span data-ttu-id="55613-156">使用者可以在要求中使用 EncryptionAtHost 屬性，以啟用或停用虛擬機器或虛擬機器規模設定的主機加密。</span><span class="sxs-lookup"><span data-stu-id="55613-156">EncryptionAtHost property can be used by user in the request to enable or disable the Host Encryption for the virtual machine or virtual machine scale set.</span></span> <span data-ttu-id="55613-157">這會啟用所有磁片的加密，包括主機本身的資源/Temp 磁片。</span><span class="sxs-lookup"><span data-stu-id="55613-157">This will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="55613-158">預設：除非針對資源將此屬性設為 true，否則將停用主機上的加密。</span><span class="sxs-lookup"><span data-stu-id="55613-158">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

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

### <span data-ttu-id="55613-159">-優先順序</span><span class="sxs-lookup"><span data-stu-id="55613-159">-Priority</span></span>
<span data-ttu-id="55613-160">虛擬機器的優先順序。</span><span class="sxs-lookup"><span data-stu-id="55613-160">The priority for the virtual machine.</span></span>  <span data-ttu-id="55613-161">僅支援的值為 "Regular"、"點" 和 "低"。</span><span class="sxs-lookup"><span data-stu-id="55613-161">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="55613-162">"Regular" 是適用于一般虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="55613-162">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="55613-163">「點」是用於找出虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="55613-163">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="55613-164">「低」也適用于 [專色虛擬機器]，但會以「點」取代。</span><span class="sxs-lookup"><span data-stu-id="55613-164">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="55613-165">請使用「污點」，而不是「低」。</span><span class="sxs-lookup"><span data-stu-id="55613-165">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="55613-166">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="55613-166">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="55613-167">要搭配此虛擬機器使用之鄰近性位置群組的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="55613-167">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

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

### <span data-ttu-id="55613-168">-標記</span><span class="sxs-lookup"><span data-stu-id="55613-168">-Tags</span></span>
<span data-ttu-id="55613-169">附加在資源上的標記。</span><span class="sxs-lookup"><span data-stu-id="55613-169">The tags attached to the resource.</span></span>

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

### <span data-ttu-id="55613-170">-VMName</span><span class="sxs-lookup"><span data-stu-id="55613-170">-VMName</span></span>
<span data-ttu-id="55613-171">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="55613-171">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="55613-172">-VMSize</span><span class="sxs-lookup"><span data-stu-id="55613-172">-VMSize</span></span>
<span data-ttu-id="55613-173">指定虛擬機器的大小。</span><span class="sxs-lookup"><span data-stu-id="55613-173">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="55613-174">-VmssId</span><span class="sxs-lookup"><span data-stu-id="55613-174">-VmssId</span></span>
<span data-ttu-id="55613-175">虛擬機器規模集的識別碼</span><span class="sxs-lookup"><span data-stu-id="55613-175">The Id of virtual machine scale set</span></span>

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

### <span data-ttu-id="55613-176">-Zone</span><span class="sxs-lookup"><span data-stu-id="55613-176">-Zone</span></span>
<span data-ttu-id="55613-177">指定虛擬機器的可用性區域清單。</span><span class="sxs-lookup"><span data-stu-id="55613-177">Specifies the availability zone list for the virtual machine.</span></span> <span data-ttu-id="55613-178">允許的值視區域的功能而定。</span><span class="sxs-lookup"><span data-stu-id="55613-178">The allowed values depend on the capabilities of the region.</span></span> <span data-ttu-id="55613-179">允許的值通常是1、2、3。</span><span class="sxs-lookup"><span data-stu-id="55613-179">Allowed values will normally be 1,2,3.</span></span>

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

### <span data-ttu-id="55613-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55613-180">CommonParameters</span></span>
<span data-ttu-id="55613-181">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="55613-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55613-182">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="55613-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55613-183">輸入</span><span class="sxs-lookup"><span data-stu-id="55613-183">INPUTS</span></span>

### <span data-ttu-id="55613-184">System.object</span><span class="sxs-lookup"><span data-stu-id="55613-184">System.String</span></span>

### <span data-ttu-id="55613-185">System.object []</span><span class="sxs-lookup"><span data-stu-id="55613-185">System.String[]</span></span>

### <span data-ttu-id="55613-186">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="55613-186">System.Collections.Hashtable</span></span>

### <span data-ttu-id="55613-187">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="55613-187">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="55613-188">輸出</span><span class="sxs-lookup"><span data-stu-id="55613-188">OUTPUTS</span></span>

### <span data-ttu-id="55613-189">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="55613-189">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="55613-190">筆記</span><span class="sxs-lookup"><span data-stu-id="55613-190">NOTES</span></span>

## <span data-ttu-id="55613-191">相關連結</span><span class="sxs-lookup"><span data-stu-id="55613-191">RELATED LINKS</span></span>

[<span data-ttu-id="55613-192">更新-AzVM</span><span class="sxs-lookup"><span data-stu-id="55613-192">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="55613-193">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="55613-193">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="55613-194">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="55613-194">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="55613-195">AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="55613-195">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

