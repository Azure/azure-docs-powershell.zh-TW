---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmconfig
schema: 2.0.0
ms.openlocfilehash: 3e42cf7c2be8433d9e1b7e85987e53b9f0050038
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801781"
---
# <span data-ttu-id="a535e-101">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="a535e-101">New-AzureRmVMConfig</span></span>

## <span data-ttu-id="a535e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a535e-102">SYNOPSIS</span></span>
<span data-ttu-id="a535e-103">建立可設定的虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="a535e-103">Creates a configurable virtual machine object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a535e-104">句法</span><span class="sxs-lookup"><span data-stu-id="a535e-104">SYNTAX</span></span>

### <span data-ttu-id="a535e-105">DefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a535e-105">DefaultParameterSet (Default)</span></span>
```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-Zone <String[]>] [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a535e-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="a535e-106">ExplicitIdentityParameterSet</span></span>
```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a535e-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="a535e-107">AssignIdentityParameterSet</span></span>
```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-AssignIdentity] [-Zone <String[]>] [-Tags <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a535e-108">說明</span><span class="sxs-lookup"><span data-stu-id="a535e-108">DESCRIPTION</span></span>
<span data-ttu-id="a535e-109">**新的-AzureRmVMConfig** Cmdlet 會為 Azure 建立可設定的本機虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="a535e-109">The **New-AzureRmVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="a535e-110">您可以使用其他 Cmdlet 來設定虛擬機器物件，例如設定 AzureRmVMOperatingSystem、AzureRmVMSourceImage、Add-AzureRmVMNetworkInterface，以及 Set-AzureRmVMOSDisk。</span><span class="sxs-lookup"><span data-stu-id="a535e-110">Other cmdlets can be used to configure a virtual machine object, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>

## <span data-ttu-id="a535e-111">示例</span><span class="sxs-lookup"><span data-stu-id="a535e-111">EXAMPLES</span></span>

### <span data-ttu-id="a535e-112">範例1：建立虛擬電腦物件</span><span class="sxs-lookup"><span data-stu-id="a535e-112">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="a535e-113">第一個命令會在名為 [ResourceGroup11] 的資源群組中取得名為 AvailablitySet03 的可用性集，然後將該物件儲存在 $AvailabilitySet 變數中。</span><span class="sxs-lookup"><span data-stu-id="a535e-113">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="a535e-114">第二個命令會建立一個虛擬電腦物件，然後將它儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="a535e-114">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="a535e-115">該命令會將名稱和大小指派給虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a535e-115">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="a535e-116">虛擬機器屬於儲存在 $AvailabilitySet 的可用性集。</span><span class="sxs-lookup"><span data-stu-id="a535e-116">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="a535e-117">參數</span><span class="sxs-lookup"><span data-stu-id="a535e-117">PARAMETERS</span></span>

### <span data-ttu-id="a535e-118">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="a535e-118">-AssignIdentity</span></span>
<span data-ttu-id="a535e-119">指定系統指派給虛擬機器的身分識別。</span><span class="sxs-lookup"><span data-stu-id="a535e-119">Specify the system assigned identity for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a535e-120">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="a535e-120">-AvailabilitySetId</span></span>
<span data-ttu-id="a535e-121">指定可用性集的 ID。</span><span class="sxs-lookup"><span data-stu-id="a535e-121">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="a535e-122">若要取得可用性集物件，請使用 Get-AzureRmAvailabilitySet Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a535e-122">To obtain an availability set object, use the Get-AzureRmAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="a535e-123">可用性集物件包含識別碼屬性。</span><span class="sxs-lookup"><span data-stu-id="a535e-123">The availability set object contains an ID property.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a535e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a535e-124">-DefaultProfile</span></span>
<span data-ttu-id="a535e-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a535e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a535e-126">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="a535e-126">-IdentityId</span></span>
<span data-ttu-id="a535e-127">指定與虛擬機器小性集相關聯的使用者識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="a535e-127">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="a535e-128">使用者身分識別參照將是下列形式的 ARM 資源識別碼： '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="a535e-128">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a535e-129">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="a535e-129">-IdentityType</span></span>
<span data-ttu-id="a535e-130">虛擬機器的身分識別（如果已設定）。</span><span class="sxs-lookup"><span data-stu-id="a535e-130">The identity of the virtual machine, if configured.</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a535e-131">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="a535e-131">-LicenseType</span></span>
<span data-ttu-id="a535e-132">授權類型，可用於提供您自己的授權案例。</span><span class="sxs-lookup"><span data-stu-id="a535e-132">The license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a535e-133">-標記</span><span class="sxs-lookup"><span data-stu-id="a535e-133">-Tags</span></span>
<span data-ttu-id="a535e-134">附加在資源上的標記。</span><span class="sxs-lookup"><span data-stu-id="a535e-134">The tags attached to the resource.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a535e-135">-VMName</span><span class="sxs-lookup"><span data-stu-id="a535e-135">-VMName</span></span>
<span data-ttu-id="a535e-136">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="a535e-136">Specifies a name for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a535e-137">-VMSize</span><span class="sxs-lookup"><span data-stu-id="a535e-137">-VMSize</span></span>
<span data-ttu-id="a535e-138">指定虛擬機器的大小。</span><span class="sxs-lookup"><span data-stu-id="a535e-138">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="a535e-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="a535e-139">-Zone</span></span>
<span data-ttu-id="a535e-140">指定虛擬機器的區域清單。</span><span class="sxs-lookup"><span data-stu-id="a535e-140">Specifies the zone list for the virtual machine.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a535e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a535e-141">CommonParameters</span></span>
<span data-ttu-id="a535e-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a535e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a535e-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a535e-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a535e-144">輸入</span><span class="sxs-lookup"><span data-stu-id="a535e-144">INPUTS</span></span>

### <span data-ttu-id="a535e-145">所有</span><span class="sxs-lookup"><span data-stu-id="a535e-145">None</span></span>
<span data-ttu-id="a535e-146">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="a535e-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a535e-147">輸出</span><span class="sxs-lookup"><span data-stu-id="a535e-147">OUTPUTS</span></span>

### <span data-ttu-id="a535e-148">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="a535e-148">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="a535e-149">筆記</span><span class="sxs-lookup"><span data-stu-id="a535e-149">NOTES</span></span>

## <span data-ttu-id="a535e-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="a535e-150">RELATED LINKS</span></span>

[<span data-ttu-id="a535e-151">更新-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a535e-151">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="a535e-152">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="a535e-152">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="a535e-153">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="a535e-153">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="a535e-154">AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a535e-154">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)


