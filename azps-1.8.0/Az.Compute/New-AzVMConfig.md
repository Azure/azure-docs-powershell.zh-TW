---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: 4fd4c3a903910068933a46d3343e8dc990565b8b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622752"
---
# <span data-ttu-id="48062-101">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="48062-101">New-AzVMConfig</span></span>

## <span data-ttu-id="48062-102">摘要</span><span class="sxs-lookup"><span data-stu-id="48062-102">SYNOPSIS</span></span>
<span data-ttu-id="48062-103">建立可設定的虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="48062-103">Creates a configurable virtual machine object.</span></span>

## <span data-ttu-id="48062-104">句法</span><span class="sxs-lookup"><span data-stu-id="48062-104">SYNTAX</span></span>

### <span data-ttu-id="48062-105">DefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="48062-105">DefaultParameterSet (Default)</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-Zone <String[]>] [-Tags <Hashtable>] [-EnableUltraSSD] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="48062-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="48062-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>] [-Tags <Hashtable>]
 [-EnableUltraSSD] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48062-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="48062-107">AssignIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-AssignIdentity] [-Zone <String[]>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48062-108">說明</span><span class="sxs-lookup"><span data-stu-id="48062-108">DESCRIPTION</span></span>
<span data-ttu-id="48062-109">**新的-AzVMConfig** Cmdlet 會為 Azure 建立可設定的本機虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="48062-109">The **New-AzVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="48062-110">您可以使用其他 Cmdlet 來設定虛擬機器物件，例如設定 AzVMOperatingSystem、AzVMSourceImage、Add-AzVMNetworkInterface，以及 Set-AzVMOSDisk。</span><span class="sxs-lookup"><span data-stu-id="48062-110">Other cmdlets can be used to configure a virtual machine object, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

## <span data-ttu-id="48062-111">示例</span><span class="sxs-lookup"><span data-stu-id="48062-111">EXAMPLES</span></span>

### <span data-ttu-id="48062-112">範例1：建立虛擬電腦物件</span><span class="sxs-lookup"><span data-stu-id="48062-112">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="48062-113">第一個命令會在名為 [ResourceGroup11] 的資源群組中取得名為 AvailablitySet03 的可用性集，然後將該物件儲存在 $AvailabilitySet 變數中。</span><span class="sxs-lookup"><span data-stu-id="48062-113">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="48062-114">第二個命令會建立一個虛擬電腦物件，然後將它儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="48062-114">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="48062-115">該命令會將名稱和大小指派給虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="48062-115">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="48062-116">虛擬機器屬於儲存在 $AvailabilitySet 的可用性集。</span><span class="sxs-lookup"><span data-stu-id="48062-116">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="48062-117">參數</span><span class="sxs-lookup"><span data-stu-id="48062-117">PARAMETERS</span></span>

### <span data-ttu-id="48062-118">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="48062-118">-AssignIdentity</span></span>
<span data-ttu-id="48062-119">指定系統指派給虛擬機器的身分識別。</span><span class="sxs-lookup"><span data-stu-id="48062-119">Specify the system assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="48062-120">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="48062-120">-AvailabilitySetId</span></span>
<span data-ttu-id="48062-121">指定可用性集的 ID。</span><span class="sxs-lookup"><span data-stu-id="48062-121">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="48062-122">若要取得可用性集物件，請使用 Get-AzAvailabilitySet Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="48062-122">To obtain an availability set object, use the Get-AzAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="48062-123">可用性集物件包含識別碼屬性。</span><span class="sxs-lookup"><span data-stu-id="48062-123">The availability set object contains an ID property.</span></span>

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

### <span data-ttu-id="48062-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48062-124">-DefaultProfile</span></span>
<span data-ttu-id="48062-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="48062-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48062-126">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="48062-126">-EnableUltraSSD</span></span>
<span data-ttu-id="48062-127">可讓一或多個受管理的資料磁片使用 VM 上的 UltraSSD_LRS 儲存帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="48062-127">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="48062-128">只有在啟用此屬性時，才能將儲存帳戶類型 UltraSSD_LRS 的受管理磁片新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="48062-128">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>


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

### <span data-ttu-id="48062-129">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="48062-129">-IdentityId</span></span>
<span data-ttu-id="48062-130">指定與虛擬機器小性集相關聯的使用者識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="48062-130">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="48062-131">使用者身分識別參照將是下列形式的 ARM 資源識別碼： '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="48062-131">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="48062-132">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="48062-132">-IdentityType</span></span>
<span data-ttu-id="48062-133">虛擬機器的身分識別（如果已設定）。</span><span class="sxs-lookup"><span data-stu-id="48062-133">The identity of the virtual machine, if configured.</span></span>

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

### <span data-ttu-id="48062-134">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="48062-134">-LicenseType</span></span>
<span data-ttu-id="48062-135">授權類型，可用於提供您自己的授權案例。</span><span class="sxs-lookup"><span data-stu-id="48062-135">The license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="48062-136">-標記</span><span class="sxs-lookup"><span data-stu-id="48062-136">-Tags</span></span>
<span data-ttu-id="48062-137">附加在資源上的標記。</span><span class="sxs-lookup"><span data-stu-id="48062-137">The tags attached to the resource.</span></span>

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

### <span data-ttu-id="48062-138">-VMName</span><span class="sxs-lookup"><span data-stu-id="48062-138">-VMName</span></span>
<span data-ttu-id="48062-139">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="48062-139">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="48062-140">-VMSize</span><span class="sxs-lookup"><span data-stu-id="48062-140">-VMSize</span></span>
<span data-ttu-id="48062-141">指定虛擬機器的大小。</span><span class="sxs-lookup"><span data-stu-id="48062-141">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="48062-142">-Zone</span><span class="sxs-lookup"><span data-stu-id="48062-142">-Zone</span></span>
<span data-ttu-id="48062-143">指定虛擬機器的可用性區域清單。</span><span class="sxs-lookup"><span data-stu-id="48062-143">Specifies the availability zone list for the virtual machine.</span></span> <span data-ttu-id="48062-144">允許的值視區域的功能而定。</span><span class="sxs-lookup"><span data-stu-id="48062-144">The allowed values depend on the capabilities of the region.</span></span> <span data-ttu-id="48062-145">允許的值通常是1、2、3。</span><span class="sxs-lookup"><span data-stu-id="48062-145">Allowed values will normally be 1,2,3.</span></span>

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

### <span data-ttu-id="48062-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48062-146">CommonParameters</span></span>
<span data-ttu-id="48062-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="48062-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48062-148">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="48062-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48062-149">輸入</span><span class="sxs-lookup"><span data-stu-id="48062-149">INPUTS</span></span>

### <span data-ttu-id="48062-150">System.object</span><span class="sxs-lookup"><span data-stu-id="48062-150">System.String</span></span>

### <span data-ttu-id="48062-151">System.object []</span><span class="sxs-lookup"><span data-stu-id="48062-151">System.String[]</span></span>

### <span data-ttu-id="48062-152">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="48062-152">System.Collections.Hashtable</span></span>

### <span data-ttu-id="48062-153">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="48062-153">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="48062-154">輸出</span><span class="sxs-lookup"><span data-stu-id="48062-154">OUTPUTS</span></span>

### <span data-ttu-id="48062-155">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="48062-155">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="48062-156">筆記</span><span class="sxs-lookup"><span data-stu-id="48062-156">NOTES</span></span>

## <span data-ttu-id="48062-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="48062-157">RELATED LINKS</span></span>

[<span data-ttu-id="48062-158">更新-AzVM</span><span class="sxs-lookup"><span data-stu-id="48062-158">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="48062-159">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="48062-159">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="48062-160">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="48062-160">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="48062-161">AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="48062-161">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)


