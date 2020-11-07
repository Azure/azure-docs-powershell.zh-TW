---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: a53d8cc94ffcc34ddf32d9cfec3b543b0bd006e1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957386"
---
# <span data-ttu-id="a279b-101">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="a279b-101">New-AzVMConfig</span></span>

## <span data-ttu-id="a279b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a279b-102">SYNOPSIS</span></span>
<span data-ttu-id="a279b-103">建立可設定的虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="a279b-103">Creates a configurable virtual machine object.</span></span>

## <span data-ttu-id="a279b-104">句法</span><span class="sxs-lookup"><span data-stu-id="a279b-104">SYNTAX</span></span>

### <span data-ttu-id="a279b-105">DefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a279b-105">DefaultParameterSet (Default)</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>]
 [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a279b-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="a279b-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>] [-MaxPrice <Double>]
 [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a279b-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="a279b-107">AssignIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-AssignIdentity] [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-VmssId <String>] [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>]
 [-EnableUltraSSD] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a279b-108">說明</span><span class="sxs-lookup"><span data-stu-id="a279b-108">DESCRIPTION</span></span>
<span data-ttu-id="a279b-109">**新的-AzVMConfig** Cmdlet 會為 Azure 建立可設定的本機虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="a279b-109">The **New-AzVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="a279b-110">您可以使用其他 Cmdlet 來設定虛擬機器物件，例如設定 AzVMOperatingSystem、AzVMSourceImage、Add-AzVMNetworkInterface，以及 Set-AzVMOSDisk。</span><span class="sxs-lookup"><span data-stu-id="a279b-110">Other cmdlets can be used to configure a virtual machine object, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

## <span data-ttu-id="a279b-111">示例</span><span class="sxs-lookup"><span data-stu-id="a279b-111">EXAMPLES</span></span>

### <span data-ttu-id="a279b-112">範例1：建立虛擬電腦物件</span><span class="sxs-lookup"><span data-stu-id="a279b-112">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="a279b-113">第一個命令會在名為 [ResourceGroup11] 的資源群組中取得名為 AvailabilitySet03 的可用性集，然後將該物件儲存在 $AvailabilitySet 變數中。</span><span class="sxs-lookup"><span data-stu-id="a279b-113">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="a279b-114">第二個命令會建立一個虛擬電腦物件，然後將它儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="a279b-114">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="a279b-115">該命令會將名稱和大小指派給虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a279b-115">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="a279b-116">虛擬機器屬於儲存在 $AvailabilitySet 的可用性集。</span><span class="sxs-lookup"><span data-stu-id="a279b-116">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="a279b-117">參數</span><span class="sxs-lookup"><span data-stu-id="a279b-117">PARAMETERS</span></span>

### <span data-ttu-id="a279b-118">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="a279b-118">-AssignIdentity</span></span>
<span data-ttu-id="a279b-119">指定系統指派給虛擬機器的身分識別。</span><span class="sxs-lookup"><span data-stu-id="a279b-119">Specify the system assigned identity for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a279b-120">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="a279b-120">-AvailabilitySetId</span></span>
<span data-ttu-id="a279b-121">指定可用性集的 ID。</span><span class="sxs-lookup"><span data-stu-id="a279b-121">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="a279b-122">若要取得可用性集物件，請使用 Get-AzAvailabilitySet Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a279b-122">To obtain an availability set object, use the Get-AzAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="a279b-123">可用性集物件包含識別碼屬性。</span><span class="sxs-lookup"><span data-stu-id="a279b-123">The availability set object contains an ID property.</span></span>

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

### <span data-ttu-id="a279b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a279b-124">-DefaultProfile</span></span>
<span data-ttu-id="a279b-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a279b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a279b-126">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="a279b-126">-EnableUltraSSD</span></span>
<span data-ttu-id="a279b-127">可讓一或多個受管理的資料磁片使用 VM 上的 UltraSSD_LRS 儲存帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="a279b-127">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="a279b-128">只有在啟用此屬性時，才能將儲存帳戶類型 UltraSSD_LRS 的受管理磁片新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a279b-128">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>


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

### <span data-ttu-id="a279b-129">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="a279b-129">-EvictionPolicy</span></span>
<span data-ttu-id="a279b-130">低優先順序虛擬機器的逐出原則。</span><span class="sxs-lookup"><span data-stu-id="a279b-130">The eviction policy for the low priority virtual machine.</span></span>  <span data-ttu-id="a279b-131">僅支援的值為 "解除配置"。</span><span class="sxs-lookup"><span data-stu-id="a279b-131">Only supported value is 'Deallocate'.</span></span>

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

### <span data-ttu-id="a279b-132">-HostId</span><span class="sxs-lookup"><span data-stu-id="a279b-132">-HostId</span></span>
<span data-ttu-id="a279b-133">主機的識別碼</span><span class="sxs-lookup"><span data-stu-id="a279b-133">The Id of Host</span></span>

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

### <span data-ttu-id="a279b-134">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="a279b-134">-IdentityId</span></span>
<span data-ttu-id="a279b-135">指定與虛擬機器小性集相關聯的使用者識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="a279b-135">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="a279b-136">使用者身分識別參照將是下列形式的 ARM 資源識別碼： '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="a279b-136">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="a279b-137">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="a279b-137">-IdentityType</span></span>
<span data-ttu-id="a279b-138">虛擬機器的身分識別（如果已設定）。</span><span class="sxs-lookup"><span data-stu-id="a279b-138">The identity of the virtual machine, if configured.</span></span>

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

### <span data-ttu-id="a279b-139">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="a279b-139">-LicenseType</span></span>
<span data-ttu-id="a279b-140">授權類型，可用於提供您自己的授權案例。</span><span class="sxs-lookup"><span data-stu-id="a279b-140">The license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="a279b-141">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="a279b-141">-MaxPrice</span></span>
<span data-ttu-id="a279b-142">指定低優先順序 VM/VMSS 要支付的最大價格。</span><span class="sxs-lookup"><span data-stu-id="a279b-142">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="a279b-143">這個價格是美元。</span><span class="sxs-lookup"><span data-stu-id="a279b-143">This price is in US Dollars.</span></span> <span data-ttu-id="a279b-144">此價格將與 VM 大小的目前低優先順序價格進行比較。</span><span class="sxs-lookup"><span data-stu-id="a279b-144">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="a279b-145">此外，價格會在建立/更新低優先順序 VM/VMSS 的時間進行比較，而且只有在 maxPrice 大於目前的低優先順序價格時，作業才會成功。</span><span class="sxs-lookup"><span data-stu-id="a279b-145">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="a279b-146">如果在建立 VM/VMSS 之後，目前的低優先順序價格超過 maxPrice，則 maxPrice 也會用於逐出低優先順序 VM/VMSS。</span><span class="sxs-lookup"><span data-stu-id="a279b-146">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="a279b-147">可能的值為：任何大於零的十進位值。</span><span class="sxs-lookup"><span data-stu-id="a279b-147">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="a279b-148">範例：0.01538。</span><span class="sxs-lookup"><span data-stu-id="a279b-148">Example: 0.01538.</span></span>  <span data-ttu-id="a279b-149">-1 表示由於價格原因，不應逐出低優先順序 VM/VMSS。</span><span class="sxs-lookup"><span data-stu-id="a279b-149">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="a279b-150">此外，如果您沒有提供預設的最大價格，就是-1。</span><span class="sxs-lookup"><span data-stu-id="a279b-150">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="a279b-151">-優先順序</span><span class="sxs-lookup"><span data-stu-id="a279b-151">-Priority</span></span>
<span data-ttu-id="a279b-152">虛擬機器的優先順序。</span><span class="sxs-lookup"><span data-stu-id="a279b-152">The priority for the virtual machine.</span></span>  <span data-ttu-id="a279b-153">僅支援的值為 "Regular"、"點" 和 "低"。</span><span class="sxs-lookup"><span data-stu-id="a279b-153">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="a279b-154">"Regular" 是適用于一般虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a279b-154">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="a279b-155">「點」是用於找出虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a279b-155">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="a279b-156">「低」也適用于 [專色虛擬機器]，但會以「點」取代。</span><span class="sxs-lookup"><span data-stu-id="a279b-156">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="a279b-157">請使用「污點」，而不是「低」。</span><span class="sxs-lookup"><span data-stu-id="a279b-157">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="a279b-158">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="a279b-158">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="a279b-159">要搭配此虛擬機器使用之鄰近性位置群組的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a279b-159">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

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

### <span data-ttu-id="a279b-160">-標記</span><span class="sxs-lookup"><span data-stu-id="a279b-160">-Tags</span></span>
<span data-ttu-id="a279b-161">附加在資源上的標記。</span><span class="sxs-lookup"><span data-stu-id="a279b-161">The tags attached to the resource.</span></span>

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

### <span data-ttu-id="a279b-162">-VMName</span><span class="sxs-lookup"><span data-stu-id="a279b-162">-VMName</span></span>
<span data-ttu-id="a279b-163">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="a279b-163">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="a279b-164">-VMSize</span><span class="sxs-lookup"><span data-stu-id="a279b-164">-VMSize</span></span>
<span data-ttu-id="a279b-165">指定虛擬機器的大小。</span><span class="sxs-lookup"><span data-stu-id="a279b-165">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="a279b-166">-VmssId</span><span class="sxs-lookup"><span data-stu-id="a279b-166">-VmssId</span></span>
<span data-ttu-id="a279b-167">虛擬機器規模集的識別碼</span><span class="sxs-lookup"><span data-stu-id="a279b-167">The Id of virtual machine scale set</span></span>

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

### <span data-ttu-id="a279b-168">-Zone</span><span class="sxs-lookup"><span data-stu-id="a279b-168">-Zone</span></span>
<span data-ttu-id="a279b-169">指定虛擬機器的可用性區域清單。</span><span class="sxs-lookup"><span data-stu-id="a279b-169">Specifies the availability zone list for the virtual machine.</span></span> <span data-ttu-id="a279b-170">允許的值視區域的功能而定。</span><span class="sxs-lookup"><span data-stu-id="a279b-170">The allowed values depend on the capabilities of the region.</span></span> <span data-ttu-id="a279b-171">允許的值通常是1、2、3。</span><span class="sxs-lookup"><span data-stu-id="a279b-171">Allowed values will normally be 1,2,3.</span></span>

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

### <span data-ttu-id="a279b-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a279b-172">CommonParameters</span></span>
<span data-ttu-id="a279b-173">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a279b-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a279b-174">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a279b-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a279b-175">輸入</span><span class="sxs-lookup"><span data-stu-id="a279b-175">INPUTS</span></span>

### <span data-ttu-id="a279b-176">System.object</span><span class="sxs-lookup"><span data-stu-id="a279b-176">System.String</span></span>

### <span data-ttu-id="a279b-177">System.object []</span><span class="sxs-lookup"><span data-stu-id="a279b-177">System.String[]</span></span>

### <span data-ttu-id="a279b-178">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a279b-178">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a279b-179">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="a279b-179">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a279b-180">輸出</span><span class="sxs-lookup"><span data-stu-id="a279b-180">OUTPUTS</span></span>

### <span data-ttu-id="a279b-181">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="a279b-181">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="a279b-182">筆記</span><span class="sxs-lookup"><span data-stu-id="a279b-182">NOTES</span></span>

## <span data-ttu-id="a279b-183">相關連結</span><span class="sxs-lookup"><span data-stu-id="a279b-183">RELATED LINKS</span></span>

[<span data-ttu-id="a279b-184">更新-AzVM</span><span class="sxs-lookup"><span data-stu-id="a279b-184">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="a279b-185">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="a279b-185">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="a279b-186">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="a279b-186">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="a279b-187">AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a279b-187">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)


