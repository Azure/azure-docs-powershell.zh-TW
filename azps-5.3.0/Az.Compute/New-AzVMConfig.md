---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: 62349410e3858978166fd9c5356a8c6b568b9600
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98446343"
---
# <span data-ttu-id="dc527-101">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="dc527-101">New-AzVMConfig</span></span>

## <span data-ttu-id="dc527-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dc527-102">SYNOPSIS</span></span>
<span data-ttu-id="dc527-103">建立可設定的虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="dc527-103">Creates a configurable virtual machine object.</span></span>

## <span data-ttu-id="dc527-104">句法</span><span class="sxs-lookup"><span data-stu-id="dc527-104">SYNTAX</span></span>

### <span data-ttu-id="dc527-105">DefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="dc527-105">DefaultParameterSet (Default)</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>]
 [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD] 
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc527-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc527-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>] [-MaxPrice <Double>]
 [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc527-107">說明</span><span class="sxs-lookup"><span data-stu-id="dc527-107">DESCRIPTION</span></span>
<span data-ttu-id="dc527-108">**新的-AzVMConfig** Cmdlet 會為 Azure 建立可設定的本機虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="dc527-108">The **New-AzVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="dc527-109">您可以使用其他 Cmdlet 來設定虛擬機器物件，例如設定 AzVMOperatingSystem、AzVMSourceImage、Add-AzVMNetworkInterface，以及 Set-AzVMOSDisk。</span><span class="sxs-lookup"><span data-stu-id="dc527-109">Other cmdlets can be used to configure a virtual machine object, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

## <span data-ttu-id="dc527-110">示例</span><span class="sxs-lookup"><span data-stu-id="dc527-110">EXAMPLES</span></span>

### <span data-ttu-id="dc527-111">範例1：建立虛擬電腦物件</span><span class="sxs-lookup"><span data-stu-id="dc527-111">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="dc527-112">第一個命令會在名為 [ResourceGroup11] 的資源群組中取得名為 AvailabilitySet03 的可用性集，然後將該物件儲存在 $AvailabilitySet 變數中。</span><span class="sxs-lookup"><span data-stu-id="dc527-112">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="dc527-113">第二個命令會建立一個虛擬電腦物件，然後將它儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="dc527-113">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="dc527-114">該命令會將名稱和大小指派給虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="dc527-114">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="dc527-115">虛擬機器屬於儲存在 $AvailabilitySet 的可用性集。</span><span class="sxs-lookup"><span data-stu-id="dc527-115">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="dc527-116">參數</span><span class="sxs-lookup"><span data-stu-id="dc527-116">PARAMETERS</span></span>

### <span data-ttu-id="dc527-117">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="dc527-117">-AvailabilitySetId</span></span>
<span data-ttu-id="dc527-118">指定可用性集的 ID。</span><span class="sxs-lookup"><span data-stu-id="dc527-118">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="dc527-119">若要取得可用性集物件，請使用 Get-AzAvailabilitySet Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dc527-119">To obtain an availability set object, use the Get-AzAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="dc527-120">可用性集物件包含識別碼屬性。</span><span class="sxs-lookup"><span data-stu-id="dc527-120">The availability set object contains an ID property.</span></span> <br>
<span data-ttu-id="dc527-121">相同可用性集中指定的虛擬機器會指派給不同的節點，以最大化可用性。</span><span class="sxs-lookup"><span data-stu-id="dc527-121">Virtual machines specified in the same availability set are allocated to different nodes to maximize availability.</span></span> <br>
<span data-ttu-id="dc527-122">如需可用性集的詳細資訊，請參閱 [管理虛擬機器的可用性](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-manage-availability?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)。</span><span class="sxs-lookup"><span data-stu-id="dc527-122">For more information about availability sets, see [Manage the availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-manage-availability?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json).</span></span> <br>
<span data-ttu-id="dc527-123">如需有關 Azure 規劃維護的詳細資訊，請參閱 [在 azure 中針對虛擬機器進行的規劃維護](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-planned-maintenance?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="dc527-123">For more information on Azure planned maintenance, see [Planned maintenance for virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-planned-maintenance?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)</span></span> <br>
<span data-ttu-id="dc527-124">目前，VM 只能在建立時新增至可用性集。</span><span class="sxs-lookup"><span data-stu-id="dc527-124">Currently, a VM can only be added to availability set at creation time.</span></span> <span data-ttu-id="dc527-125">要新增 VM 的可用性集，必須位於與可用性集資源相同的資源群組底下。</span><span class="sxs-lookup"><span data-stu-id="dc527-125">The availability set to which the VM is being added should be under the same resource group as the availability set resource.</span></span> <span data-ttu-id="dc527-126">無法將現有的 VM 新增至可用性集。</span><span class="sxs-lookup"><span data-stu-id="dc527-126">An existing VM cannot be added to an availability set.</span></span> <br>
<span data-ttu-id="dc527-127">這個屬性不能與非 null 屬性一起存在。 virtualMachineScaleSet 參考。</span><span class="sxs-lookup"><span data-stu-id="dc527-127">This property cannot exist along with a non-null properties.virtualMachineScaleSet reference.</span></span>

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

### <span data-ttu-id="dc527-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc527-128">-DefaultProfile</span></span>
<span data-ttu-id="dc527-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dc527-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc527-130">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="dc527-130">-EnableUltraSSD</span></span>
<span data-ttu-id="dc527-131">可讓一或多個受管理的資料磁片使用 VM 上的 UltraSSD_LRS 儲存帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="dc527-131">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="dc527-132">只有在啟用此屬性時，才能將儲存帳戶類型 UltraSSD_LRS 的受管理磁片新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="dc527-132">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>


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

### <span data-ttu-id="dc527-133">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="dc527-133">-EvictionPolicy</span></span>
<span data-ttu-id="dc527-134">Azure 點虛擬機器的逐出原則。</span><span class="sxs-lookup"><span data-stu-id="dc527-134">The eviction policy for the Azure Spot virtual machine.</span></span>  <span data-ttu-id="dc527-135">支援的值為 "解除配置" 和 "Delete"。</span><span class="sxs-lookup"><span data-stu-id="dc527-135">Supported values are 'Deallocate' and 'Delete'.</span></span>

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

### <span data-ttu-id="dc527-136">-HostId</span><span class="sxs-lookup"><span data-stu-id="dc527-136">-HostId</span></span>
<span data-ttu-id="dc527-137">主機的識別碼</span><span class="sxs-lookup"><span data-stu-id="dc527-137">The Id of Host</span></span>

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

### <span data-ttu-id="dc527-138">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="dc527-138">-IdentityId</span></span>
<span data-ttu-id="dc527-139">指定與虛擬機器小性集相關聯的使用者識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="dc527-139">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="dc527-140">使用者身分識別參照將是下列形式的 ARM 資源識別碼： '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="dc527-140">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="dc527-141">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="dc527-141">-IdentityType</span></span>
<span data-ttu-id="dc527-142">虛擬機器的身分識別（如果已設定）。</span><span class="sxs-lookup"><span data-stu-id="dc527-142">The identity of the virtual machine, if configured.</span></span>

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

### <span data-ttu-id="dc527-143">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="dc527-143">-LicenseType</span></span>
<span data-ttu-id="dc527-144">指定授權類型，這表示虛擬機器的影像或磁片已授權內部部署。</span><span class="sxs-lookup"><span data-stu-id="dc527-144">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="dc527-145">Windows Server 可能的值包括：</span><span class="sxs-lookup"><span data-stu-id="dc527-145">Possible values for Windows Server are:</span></span>
- <span data-ttu-id="dc527-146">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="dc527-146">Windows_Client</span></span>
- <span data-ttu-id="dc527-147">Windows_Server 的 Linux Server 作業系統可能值為：</span><span class="sxs-lookup"><span data-stu-id="dc527-147">Windows_Server Possible values for Linux Server operating system are:</span></span> 
- <span data-ttu-id="dc527-148">RHEL) 的 RHEL_BYOS (</span><span class="sxs-lookup"><span data-stu-id="dc527-148">RHEL_BYOS (for RHEL)</span></span> 
- <span data-ttu-id="dc527-149">SUSE) 的 SLES_BYOS (</span><span class="sxs-lookup"><span data-stu-id="dc527-149">SLES_BYOS (for SUSE)</span></span> 

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

### <span data-ttu-id="dc527-150">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="dc527-150">-MaxPrice</span></span>
<span data-ttu-id="dc527-151">指定低優先順序 VM/VMSS 要支付的最大價格。</span><span class="sxs-lookup"><span data-stu-id="dc527-151">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="dc527-152">這個價格是美元。</span><span class="sxs-lookup"><span data-stu-id="dc527-152">This price is in US Dollars.</span></span> <span data-ttu-id="dc527-153">此價格將與 VM 大小的目前低優先順序價格進行比較。</span><span class="sxs-lookup"><span data-stu-id="dc527-153">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="dc527-154">此外，價格會在建立/更新低優先順序 VM/VMSS 的時間進行比較，而且只有在 maxPrice 大於目前的低優先順序價格時，作業才會成功。</span><span class="sxs-lookup"><span data-stu-id="dc527-154">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="dc527-155">如果在建立 VM/VMSS 之後，目前的低優先順序價格超過 maxPrice，則 maxPrice 也會用於逐出低優先順序 VM/VMSS。</span><span class="sxs-lookup"><span data-stu-id="dc527-155">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="dc527-156">可能的值為：任何大於零的十進位值。</span><span class="sxs-lookup"><span data-stu-id="dc527-156">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="dc527-157">範例：0.01538。</span><span class="sxs-lookup"><span data-stu-id="dc527-157">Example: 0.01538.</span></span>  <span data-ttu-id="dc527-158">-1 表示由於價格原因，不應逐出低優先順序 VM/VMSS。</span><span class="sxs-lookup"><span data-stu-id="dc527-158">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="dc527-159">此外，如果您沒有提供預設的最大價格，就是-1。</span><span class="sxs-lookup"><span data-stu-id="dc527-159">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="dc527-160">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="dc527-160">-EncryptionAtHost</span></span>
<span data-ttu-id="dc527-161">使用者可以在要求中使用 EncryptionAtHost 屬性，以啟用或停用虛擬機器或虛擬機器規模設定的主機加密。</span><span class="sxs-lookup"><span data-stu-id="dc527-161">EncryptionAtHost property can be used by user in the request to enable or disable the Host Encryption for the virtual machine or virtual machine scale set.</span></span> <span data-ttu-id="dc527-162">這會啟用所有磁片的加密，包括主機本身的資源/Temp 磁片。</span><span class="sxs-lookup"><span data-stu-id="dc527-162">This will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="dc527-163">預設：除非針對資源將此屬性設為 true，否則將停用主機上的加密。</span><span class="sxs-lookup"><span data-stu-id="dc527-163">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

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

### <span data-ttu-id="dc527-164">-優先順序</span><span class="sxs-lookup"><span data-stu-id="dc527-164">-Priority</span></span>
<span data-ttu-id="dc527-165">虛擬機器的優先順序。</span><span class="sxs-lookup"><span data-stu-id="dc527-165">The priority for the virtual machine.</span></span>  <span data-ttu-id="dc527-166">僅支援的值為 "Regular"、"點" 和 "低"。</span><span class="sxs-lookup"><span data-stu-id="dc527-166">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="dc527-167">"Regular" 是適用于一般虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="dc527-167">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="dc527-168">「點」是用於找出虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="dc527-168">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="dc527-169">「低」也適用于 [專色虛擬機器]，但會以「點」取代。</span><span class="sxs-lookup"><span data-stu-id="dc527-169">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="dc527-170">請使用「污點」，而不是「低」。</span><span class="sxs-lookup"><span data-stu-id="dc527-170">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="dc527-171">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="dc527-171">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="dc527-172">要搭配此虛擬機器使用之鄰近性位置群組的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="dc527-172">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

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

### <span data-ttu-id="dc527-173">-標記</span><span class="sxs-lookup"><span data-stu-id="dc527-173">-Tags</span></span>
<span data-ttu-id="dc527-174">附加在資源上的標記。</span><span class="sxs-lookup"><span data-stu-id="dc527-174">The tags attached to the resource.</span></span>

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

### <span data-ttu-id="dc527-175">-VMName</span><span class="sxs-lookup"><span data-stu-id="dc527-175">-VMName</span></span>
<span data-ttu-id="dc527-176">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="dc527-176">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="dc527-177">-VMSize</span><span class="sxs-lookup"><span data-stu-id="dc527-177">-VMSize</span></span>
<span data-ttu-id="dc527-178">指定虛擬機器的大小。</span><span class="sxs-lookup"><span data-stu-id="dc527-178">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="dc527-179">-VmssId</span><span class="sxs-lookup"><span data-stu-id="dc527-179">-VmssId</span></span>
<span data-ttu-id="dc527-180">虛擬機器規模集的識別碼</span><span class="sxs-lookup"><span data-stu-id="dc527-180">The Id of virtual machine scale set</span></span>

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

### <span data-ttu-id="dc527-181">-Zone</span><span class="sxs-lookup"><span data-stu-id="dc527-181">-Zone</span></span>
<span data-ttu-id="dc527-182">指定虛擬機器的可用性區域清單。</span><span class="sxs-lookup"><span data-stu-id="dc527-182">Specifies the availability zone list for the virtual machine.</span></span> <span data-ttu-id="dc527-183">允許的值視區域的功能而定。</span><span class="sxs-lookup"><span data-stu-id="dc527-183">The allowed values depend on the capabilities of the region.</span></span> <span data-ttu-id="dc527-184">允許的值通常是1、2、3。</span><span class="sxs-lookup"><span data-stu-id="dc527-184">Allowed values will normally be 1,2,3.</span></span>

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

### <span data-ttu-id="dc527-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc527-185">CommonParameters</span></span>
<span data-ttu-id="dc527-186">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dc527-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc527-187">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="dc527-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc527-188">輸入</span><span class="sxs-lookup"><span data-stu-id="dc527-188">INPUTS</span></span>

### <span data-ttu-id="dc527-189">System.object</span><span class="sxs-lookup"><span data-stu-id="dc527-189">System.String</span></span>

### <span data-ttu-id="dc527-190">System.object []</span><span class="sxs-lookup"><span data-stu-id="dc527-190">System.String[]</span></span>

### <span data-ttu-id="dc527-191">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="dc527-191">System.Collections.Hashtable</span></span>

### <span data-ttu-id="dc527-192">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="dc527-192">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="dc527-193">輸出</span><span class="sxs-lookup"><span data-stu-id="dc527-193">OUTPUTS</span></span>

### <span data-ttu-id="dc527-194">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="dc527-194">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="dc527-195">筆記</span><span class="sxs-lookup"><span data-stu-id="dc527-195">NOTES</span></span>

## <span data-ttu-id="dc527-196">相關連結</span><span class="sxs-lookup"><span data-stu-id="dc527-196">RELATED LINKS</span></span>

[<span data-ttu-id="dc527-197">更新-AzVM</span><span class="sxs-lookup"><span data-stu-id="dc527-197">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="dc527-198">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="dc527-198">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="dc527-199">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="dc527-199">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="dc527-200">AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="dc527-200">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)


