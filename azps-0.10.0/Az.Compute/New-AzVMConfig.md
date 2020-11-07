---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: 4b128346d77e090e5b0699ace8f03eaa9a4786a1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796122"
---
# <span data-ttu-id="aded9-101">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="aded9-101">New-AzVMConfig</span></span>

## <span data-ttu-id="aded9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="aded9-102">SYNOPSIS</span></span>
<span data-ttu-id="aded9-103">建立可設定的虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="aded9-103">Creates a configurable virtual machine object.</span></span>

## <span data-ttu-id="aded9-104">句法</span><span class="sxs-lookup"><span data-stu-id="aded9-104">SYNTAX</span></span>

### <span data-ttu-id="aded9-105">DefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="aded9-105">DefaultParameterSet (Default)</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-Zone <String[]>] [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="aded9-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="aded9-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aded9-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="aded9-107">AssignIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-AssignIdentity] [-Zone <String[]>] [-Tags <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aded9-108">說明</span><span class="sxs-lookup"><span data-stu-id="aded9-108">DESCRIPTION</span></span>
<span data-ttu-id="aded9-109">**新的-AzVMConfig** Cmdlet 會為 Azure 建立可設定的本機虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="aded9-109">The **New-AzVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="aded9-110">您可以使用其他 Cmdlet 來設定虛擬機器物件，例如設定 AzVMOperatingSystem、AzVMSourceImage、Add-AzVMNetworkInterface，以及 Set-AzVMOSDisk。</span><span class="sxs-lookup"><span data-stu-id="aded9-110">Other cmdlets can be used to configure a virtual machine object, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

## <span data-ttu-id="aded9-111">示例</span><span class="sxs-lookup"><span data-stu-id="aded9-111">EXAMPLES</span></span>

### <span data-ttu-id="aded9-112">範例1：建立虛擬電腦物件</span><span class="sxs-lookup"><span data-stu-id="aded9-112">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="aded9-113">第一個命令會在名為 [ResourceGroup11] 的資源群組中取得名為 AvailablitySet03 的可用性集，然後將該物件儲存在 $AvailabilitySet 變數中。</span><span class="sxs-lookup"><span data-stu-id="aded9-113">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="aded9-114">第二個命令會建立一個虛擬電腦物件，然後將它儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="aded9-114">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="aded9-115">該命令會將名稱和大小指派給虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="aded9-115">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="aded9-116">虛擬機器屬於儲存在 $AvailabilitySet 的可用性集。</span><span class="sxs-lookup"><span data-stu-id="aded9-116">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="aded9-117">參數</span><span class="sxs-lookup"><span data-stu-id="aded9-117">PARAMETERS</span></span>

### <span data-ttu-id="aded9-118">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="aded9-118">-AssignIdentity</span></span>
<span data-ttu-id="aded9-119">指定系統指派給虛擬機器的身分識別。</span><span class="sxs-lookup"><span data-stu-id="aded9-119">Specify the system assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="aded9-120">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="aded9-120">-AvailabilitySetId</span></span>
<span data-ttu-id="aded9-121">指定可用性集的 ID。</span><span class="sxs-lookup"><span data-stu-id="aded9-121">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="aded9-122">若要取得可用性集物件，請使用 Get-AzAvailabilitySet Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="aded9-122">To obtain an availability set object, use the Get-AzAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="aded9-123">可用性集物件包含識別碼屬性。</span><span class="sxs-lookup"><span data-stu-id="aded9-123">The availability set object contains an ID property.</span></span>

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

### <span data-ttu-id="aded9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aded9-124">-DefaultProfile</span></span>
<span data-ttu-id="aded9-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="aded9-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aded9-126">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="aded9-126">-IdentityId</span></span>
<span data-ttu-id="aded9-127">指定與虛擬機器小性集相關聯的使用者識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="aded9-127">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="aded9-128">使用者身分識別參照將是下列形式的 ARM 資源識別碼： '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="aded9-128">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="aded9-129">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="aded9-129">-IdentityType</span></span>
<span data-ttu-id="aded9-130">虛擬機器的身分識別（如果已設定）。</span><span class="sxs-lookup"><span data-stu-id="aded9-130">The identity of the virtual machine, if configured.</span></span>

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

### <span data-ttu-id="aded9-131">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="aded9-131">-LicenseType</span></span>
<span data-ttu-id="aded9-132">授權類型，可用於提供您自己的授權案例。</span><span class="sxs-lookup"><span data-stu-id="aded9-132">The license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="aded9-133">-標記</span><span class="sxs-lookup"><span data-stu-id="aded9-133">-Tags</span></span>
<span data-ttu-id="aded9-134">附加在資源上的標記。</span><span class="sxs-lookup"><span data-stu-id="aded9-134">The tags attached to the resource.</span></span>

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

### <span data-ttu-id="aded9-135">-VMName</span><span class="sxs-lookup"><span data-stu-id="aded9-135">-VMName</span></span>
<span data-ttu-id="aded9-136">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="aded9-136">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="aded9-137">-VMSize</span><span class="sxs-lookup"><span data-stu-id="aded9-137">-VMSize</span></span>
<span data-ttu-id="aded9-138">指定虛擬機器的大小。</span><span class="sxs-lookup"><span data-stu-id="aded9-138">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="aded9-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="aded9-139">-Zone</span></span>
<span data-ttu-id="aded9-140">指定虛擬機器的區域清單。</span><span class="sxs-lookup"><span data-stu-id="aded9-140">Specifies the zone list for the virtual machine.</span></span>

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

### <span data-ttu-id="aded9-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aded9-141">CommonParameters</span></span>
<span data-ttu-id="aded9-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="aded9-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aded9-143">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="aded9-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aded9-144">輸入</span><span class="sxs-lookup"><span data-stu-id="aded9-144">INPUTS</span></span>

### <span data-ttu-id="aded9-145">所有</span><span class="sxs-lookup"><span data-stu-id="aded9-145">None</span></span>
<span data-ttu-id="aded9-146">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="aded9-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="aded9-147">輸出</span><span class="sxs-lookup"><span data-stu-id="aded9-147">OUTPUTS</span></span>

### <span data-ttu-id="aded9-148">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="aded9-148">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="aded9-149">筆記</span><span class="sxs-lookup"><span data-stu-id="aded9-149">NOTES</span></span>

## <span data-ttu-id="aded9-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="aded9-150">RELATED LINKS</span></span>

[<span data-ttu-id="aded9-151">更新-AzVM</span><span class="sxs-lookup"><span data-stu-id="aded9-151">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="aded9-152">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="aded9-152">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="aded9-153">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="aded9-153">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="aded9-154">AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="aded9-154">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)


