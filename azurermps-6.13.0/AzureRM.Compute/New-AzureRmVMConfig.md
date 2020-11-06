---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMConfig.md
ms.openlocfilehash: 6809088110944648781fc2264bd2c56f98cbee1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451336"
---
# <span data-ttu-id="72cb8-101">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="72cb8-101">New-AzureRmVMConfig</span></span>

## <span data-ttu-id="72cb8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="72cb8-102">SYNOPSIS</span></span>
<span data-ttu-id="72cb8-103">建立可設定的虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="72cb8-103">Creates a configurable virtual machine object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72cb8-104">句法</span><span class="sxs-lookup"><span data-stu-id="72cb8-104">SYNTAX</span></span>

### <span data-ttu-id="72cb8-105">DefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="72cb8-105">DefaultParameterSet (Default)</span></span>
```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-Zone <String[]>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72cb8-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="72cb8-106">ExplicitIdentityParameterSet</span></span>
```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-Tags <Hashtable>] [-EnableUltraSSD] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72cb8-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="72cb8-107">AssignIdentityParameterSet</span></span>
```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-AssignIdentity] [-Zone <String[]>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72cb8-108">說明</span><span class="sxs-lookup"><span data-stu-id="72cb8-108">DESCRIPTION</span></span>
<span data-ttu-id="72cb8-109">**新的-AzureRmVMConfig** Cmdlet 會為 Azure 建立可設定的本機虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="72cb8-109">The **New-AzureRmVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="72cb8-110">您可以使用其他 Cmdlet 來設定虛擬機器物件，例如設定 AzureRmVMOperatingSystem、AzureRmVMSourceImage、Add-AzureRmVMNetworkInterface，以及 Set-AzureRmVMOSDisk。</span><span class="sxs-lookup"><span data-stu-id="72cb8-110">Other cmdlets can be used to configure a virtual machine object, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>

## <span data-ttu-id="72cb8-111">示例</span><span class="sxs-lookup"><span data-stu-id="72cb8-111">EXAMPLES</span></span>

### <span data-ttu-id="72cb8-112">範例1：建立虛擬電腦物件</span><span class="sxs-lookup"><span data-stu-id="72cb8-112">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="72cb8-113">第一個命令會在名為 [ResourceGroup11] 的資源群組中取得名為 AvailablitySet03 的可用性集，然後將該物件儲存在 $AvailabilitySet 變數中。</span><span class="sxs-lookup"><span data-stu-id="72cb8-113">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="72cb8-114">第二個命令會建立一個虛擬電腦物件，然後將它儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="72cb8-114">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="72cb8-115">該命令會將名稱和大小指派給虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="72cb8-115">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="72cb8-116">虛擬機器屬於儲存在 $AvailabilitySet 的可用性集。</span><span class="sxs-lookup"><span data-stu-id="72cb8-116">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="72cb8-117">參數</span><span class="sxs-lookup"><span data-stu-id="72cb8-117">PARAMETERS</span></span>

### <span data-ttu-id="72cb8-118">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="72cb8-118">-AssignIdentity</span></span>
<span data-ttu-id="72cb8-119">指定系統指派給虛擬機器的身分識別。</span><span class="sxs-lookup"><span data-stu-id="72cb8-119">Specify the system assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="72cb8-120">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="72cb8-120">-AvailabilitySetId</span></span>
<span data-ttu-id="72cb8-121">指定可用性集的 ID。</span><span class="sxs-lookup"><span data-stu-id="72cb8-121">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="72cb8-122">若要取得可用性集物件，請使用 Get-AzureRmAvailabilitySet Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="72cb8-122">To obtain an availability set object, use the Get-AzureRmAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="72cb8-123">可用性集物件包含識別碼屬性。</span><span class="sxs-lookup"><span data-stu-id="72cb8-123">The availability set object contains an ID property.</span></span>

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

### <span data-ttu-id="72cb8-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72cb8-124">-DefaultProfile</span></span>
<span data-ttu-id="72cb8-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="72cb8-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72cb8-126">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="72cb8-126">-EnableUltraSSD</span></span>
<span data-ttu-id="72cb8-127">可讓一或多個受管理的資料磁片使用 VM 上的 UltraSSD_LRS 儲存帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="72cb8-127">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="72cb8-128">只有在啟用此屬性時，才能將儲存帳戶類型 UltraSSD_LRS 的受管理磁片新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="72cb8-128">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>


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

### <span data-ttu-id="72cb8-129">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="72cb8-129">-IdentityId</span></span>
<span data-ttu-id="72cb8-130">指定與虛擬機器小性集相關聯的使用者識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="72cb8-130">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="72cb8-131">使用者身分識別參照將是下列形式的 ARM 資源識別碼： '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="72cb8-131">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="72cb8-132">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="72cb8-132">-IdentityType</span></span>
<span data-ttu-id="72cb8-133">虛擬機器的身分識別（如果已設定）。</span><span class="sxs-lookup"><span data-stu-id="72cb8-133">The identity of the virtual machine, if configured.</span></span>

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

### <span data-ttu-id="72cb8-134">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="72cb8-134">-LicenseType</span></span>
<span data-ttu-id="72cb8-135">授權類型，可用於提供您自己的授權案例。</span><span class="sxs-lookup"><span data-stu-id="72cb8-135">The license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="72cb8-136">-標記</span><span class="sxs-lookup"><span data-stu-id="72cb8-136">-Tags</span></span>
<span data-ttu-id="72cb8-137">附加在資源上的標記。</span><span class="sxs-lookup"><span data-stu-id="72cb8-137">The tags attached to the resource.</span></span>

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

### <span data-ttu-id="72cb8-138">-VMName</span><span class="sxs-lookup"><span data-stu-id="72cb8-138">-VMName</span></span>
<span data-ttu-id="72cb8-139">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="72cb8-139">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="72cb8-140">-VMSize</span><span class="sxs-lookup"><span data-stu-id="72cb8-140">-VMSize</span></span>
<span data-ttu-id="72cb8-141">指定虛擬機器的大小。</span><span class="sxs-lookup"><span data-stu-id="72cb8-141">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="72cb8-142">-Zone</span><span class="sxs-lookup"><span data-stu-id="72cb8-142">-Zone</span></span>
<span data-ttu-id="72cb8-143">指定虛擬機器的區域清單。</span><span class="sxs-lookup"><span data-stu-id="72cb8-143">Specifies the zone list for the virtual machine.</span></span>

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

### <span data-ttu-id="72cb8-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72cb8-144">CommonParameters</span></span>
<span data-ttu-id="72cb8-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="72cb8-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72cb8-146">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="72cb8-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72cb8-147">輸入</span><span class="sxs-lookup"><span data-stu-id="72cb8-147">INPUTS</span></span>

### <span data-ttu-id="72cb8-148">System.object</span><span class="sxs-lookup"><span data-stu-id="72cb8-148">System.String</span></span>

### <span data-ttu-id="72cb8-149">System.object []</span><span class="sxs-lookup"><span data-stu-id="72cb8-149">System.String[]</span></span>

### <span data-ttu-id="72cb8-150">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="72cb8-150">System.Collections.Hashtable</span></span>

## <span data-ttu-id="72cb8-151">輸出</span><span class="sxs-lookup"><span data-stu-id="72cb8-151">OUTPUTS</span></span>

### <span data-ttu-id="72cb8-152">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="72cb8-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="72cb8-153">筆記</span><span class="sxs-lookup"><span data-stu-id="72cb8-153">NOTES</span></span>

## <span data-ttu-id="72cb8-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="72cb8-154">RELATED LINKS</span></span>

[<span data-ttu-id="72cb8-155">更新-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="72cb8-155">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="72cb8-156">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="72cb8-156">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="72cb8-157">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="72cb8-157">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="72cb8-158">AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="72cb8-158">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)


