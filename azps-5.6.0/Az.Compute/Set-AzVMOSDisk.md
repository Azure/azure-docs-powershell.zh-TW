---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8F7AF1B8-D769-452C-92CF-4486C3EB894D
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOSDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOSDisk.md
ms.openlocfilehash: 07d71e8fa7cd5c19cfc6f4aab8d27e5c5758b41c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913962"
---
# <span data-ttu-id="24c6d-101">Set-AzVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="24c6d-101">Set-AzVMOSDisk</span></span>

## <span data-ttu-id="24c6d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="24c6d-102">SYNOPSIS</span></span>
<span data-ttu-id="24c6d-103">設定虛擬機器上的作業系統磁片屬性。</span><span class="sxs-lookup"><span data-stu-id="24c6d-103">Sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="24c6d-104">語法</span><span class="sxs-lookup"><span data-stu-id="24c6d-104">SYNTAX</span></span>

### <span data-ttu-id="24c6d-105">DefaultParamSet (預設) </span><span class="sxs-lookup"><span data-stu-id="24c6d-105">DefaultParamSet (Default)</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24c6d-106">WindowsParamSet</span><span class="sxs-lookup"><span data-stu-id="24c6d-106">WindowsParamSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Windows] [-DiskSizeInGB <Int32>]
 [-ManagedDiskId <String>] [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DiffDiskSetting <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24c6d-107">WindowsCryptEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="24c6d-107">WindowsDiskEncryptionParameterSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Windows] [-DiskEncryptionKeyUrl] <String>
 [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24c6d-108">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="24c6d-108">LinuxParamSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Linux] [-DiskSizeInGB <Int32>]
 [-ManagedDiskId <String>] [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DiffDiskSetting <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24c6d-109">LinuxCryptEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="24c6d-109">LinuxDiskEncryptionParameterSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Linux] [-DiskEncryptionKeyUrl] <String>
 [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24c6d-110">描述</span><span class="sxs-lookup"><span data-stu-id="24c6d-110">DESCRIPTION</span></span>
<span data-ttu-id="24c6d-111">**Set-AzCMOSCio** Cmdlet 會設定虛擬機器上的作業系統磁片屬性。</span><span class="sxs-lookup"><span data-stu-id="24c6d-111">The **Set-AzVMOSDisk** cmdlet sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="24c6d-112">例子</span><span class="sxs-lookup"><span data-stu-id="24c6d-112">EXAMPLES</span></span>

### <span data-ttu-id="24c6d-113">範例 1：從平臺圖像設定虛擬機器的屬性</span><span class="sxs-lookup"><span data-stu-id="24c6d-113">Example 1: Set properties on a virtual machine from platform image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential) 
PS C:\> $VirtualMachine = Set-AzVMSourceImage -VM $VirtualMachine -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.10" -Version "latest" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption FromImage
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="24c6d-114">第一個命令會獲得名稱為 ResourceGroup11 的資源群組中名為 AvailabilitySet13 的可用性集，然後將該物件儲存在 $AvailabilitySet 變數中。</span><span class="sxs-lookup"><span data-stu-id="24c6d-114">The first command gets the availability set named AvailabilitySet13 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="24c6d-115">第二個命令會建立虛擬機器物件，然後將它儲存在$VirtualMachine變數中。</span><span class="sxs-lookup"><span data-stu-id="24c6d-115">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="24c6d-116">該命令會為虛擬機器指定名稱和大小。</span><span class="sxs-lookup"><span data-stu-id="24c6d-116">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="24c6d-117">虛擬機器屬於儲存在 $AvailabilitySet 的可用性集。</span><span class="sxs-lookup"><span data-stu-id="24c6d-117">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="24c6d-118">最後一個命令會設定 $VirtualMachine 中的虛擬機器$VirtualMachine。</span><span class="sxs-lookup"><span data-stu-id="24c6d-118">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="24c6d-119">範例 2：從一般使用者映射設定虛擬機器的屬性</span><span class="sxs-lookup"><span data-stu-id="24c6d-119">Example 2: Sets properties on a virtual machine from generalized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential)
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -SourceImageUri "https://mystorageaccount.blob.core.windows.net/vhds/myOSImage.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption fromImage -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="24c6d-120">第一個命令會獲得名為 ResourceGroup11 的資源群組中名為 AvailabilitySet13 的可用性集，並且將該物件$AvailabilitySet變數。</span><span class="sxs-lookup"><span data-stu-id="24c6d-120">The first command gets the availability set named AvailabilitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="24c6d-121">第二個命令會建立虛擬機器物件，並儲存在$VirtualMachine變數中。</span><span class="sxs-lookup"><span data-stu-id="24c6d-121">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="24c6d-122">該命令會為虛擬機器指定名稱和大小。</span><span class="sxs-lookup"><span data-stu-id="24c6d-122">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="24c6d-123">虛擬機器屬於儲存在 $AvailabilitySet 的可用性集。</span><span class="sxs-lookup"><span data-stu-id="24c6d-123">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="24c6d-124">最後一個命令會設定 $VirtualMachine 中的虛擬機器$VirtualMachine。</span><span class="sxs-lookup"><span data-stu-id="24c6d-124">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="24c6d-125">範例 3：從特殊使用者映射設定虛擬機器的屬性</span><span class="sxs-lookup"><span data-stu-id="24c6d-125">Example 3: Sets properties on a virtual machine from specialized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption Attach -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="24c6d-126">第一個命令會獲得名為 ResourceGroup11 的資源群組中名為 AvailabilitySet13 的可用性集，並且將該物件$AvailabilitySet變數。</span><span class="sxs-lookup"><span data-stu-id="24c6d-126">The first command gets the availability set named AvailabilitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="24c6d-127">第二個命令會建立虛擬機器物件，並儲存在$VirtualMachine變數中。</span><span class="sxs-lookup"><span data-stu-id="24c6d-127">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="24c6d-128">該命令會為虛擬機器指定名稱和大小。</span><span class="sxs-lookup"><span data-stu-id="24c6d-128">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="24c6d-129">虛擬機器屬於儲存在 $AvailabilitySet 的可用性集。</span><span class="sxs-lookup"><span data-stu-id="24c6d-129">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="24c6d-130">最後一個命令會設定 $VirtualMachine 中的虛擬機器$VirtualMachine。</span><span class="sxs-lookup"><span data-stu-id="24c6d-130">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="24c6d-131">範例 4：設定虛擬機器作業系統磁片上的磁片加密設定</span><span class="sxs-lookup"><span data-stu-id="24c6d-131">Example 4: Set the disk encryption settings on a virtual machine operating system disk</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite -Windows -CreateOption "Attach" -DiskEncryptionKeyUrl "https://mytestvault.vault.azure.net/secrets/Test1/514ceb769c984379a7e0230bddaaaaaa" -DiskEncryptionKeyVaultId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myresourcegroup/providers/Microsoft.KeyVault/vaults/mytestvault"
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName " ResourceGroup11"
```

<span data-ttu-id="24c6d-132">此範例會設定虛擬機器作業系統磁片上的磁片加密設定。</span><span class="sxs-lookup"><span data-stu-id="24c6d-132">This example sets the disk encryption settings on a virtual machine operating system disk.</span></span>

## <span data-ttu-id="24c6d-133">參數</span><span class="sxs-lookup"><span data-stu-id="24c6d-133">PARAMETERS</span></span>

### <span data-ttu-id="24c6d-134">-緩存</span><span class="sxs-lookup"><span data-stu-id="24c6d-134">-Caching</span></span>
<span data-ttu-id="24c6d-135">指定作業系統磁片的緩存模式。</span><span class="sxs-lookup"><span data-stu-id="24c6d-135">Specifies the caching mode of the operating system disk.</span></span>
<span data-ttu-id="24c6d-136">有效的值為：</span><span class="sxs-lookup"><span data-stu-id="24c6d-136">Valid values are:</span></span> 
- <span data-ttu-id="24c6d-137">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="24c6d-137">ReadOnly</span></span>
- <span data-ttu-id="24c6d-138">朗讀預設值為 ReadWrite。</span><span class="sxs-lookup"><span data-stu-id="24c6d-138">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="24c6d-139">變更緩存值會導致虛擬機器重新開機。</span><span class="sxs-lookup"><span data-stu-id="24c6d-139">Changing the caching value causes the virtual machine to restart.</span></span>
<span data-ttu-id="24c6d-140">此設定會影響磁片的績效。</span><span class="sxs-lookup"><span data-stu-id="24c6d-140">This setting affects the performance of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24c6d-141">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="24c6d-141">-CreateOption</span></span>
<span data-ttu-id="24c6d-142">指定此 Cmdlet 是否要從平臺或使用者映射在虛擬機器中建立磁片，或附加到現有的磁片。</span><span class="sxs-lookup"><span data-stu-id="24c6d-142">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, or attaches an existing disk.</span></span>
<span data-ttu-id="24c6d-143">有效的值為：</span><span class="sxs-lookup"><span data-stu-id="24c6d-143">Valid values are:</span></span> 
- <span data-ttu-id="24c6d-144">附加。</span><span class="sxs-lookup"><span data-stu-id="24c6d-144">Attach.</span></span>
<span data-ttu-id="24c6d-145">指定此選項以從特殊磁片建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="24c6d-145">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="24c6d-146">當您指定此選項時，請勿指定 *SourceImageUri* 參數。</span><span class="sxs-lookup"><span data-stu-id="24c6d-146">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="24c6d-147">請改為使用 Set-AzVMSourceImage Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24c6d-147">Instead, use the Set-AzVMSourceImage cmdlet.</span></span>
<span data-ttu-id="24c6d-148">您也必須使用 *Windows* 或 *Linux* 參數，告訴 Azure 平臺 VHD 上的作業系統類型。</span><span class="sxs-lookup"><span data-stu-id="24c6d-148">You must also use the use the *Windows* or *Linux* parameters to tell the azure platform the type of the operating system on the VHD.</span></span>
<span data-ttu-id="24c6d-149">*VhdUri* 參數足以告知 Azure 平臺要附加的磁片位置。</span><span class="sxs-lookup"><span data-stu-id="24c6d-149">The *VhdUri* parameter is enough to tell the azure platform the location of the disk to attach.</span></span> 
- <span data-ttu-id="24c6d-150">FromImage.</span><span class="sxs-lookup"><span data-stu-id="24c6d-150">FromImage.</span></span>
<span data-ttu-id="24c6d-151">指定此選項以從平臺映射或一般使用者映射建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="24c6d-151">Specify this option to create a virtual machine from a platform image or a generalized user image.</span></span>
<span data-ttu-id="24c6d-152">在一般使用者影像的情況下，您也需要指定 *SourceImageUri* 參數，以及 *Windows* 或 *Linux* 參數，以告訴 Azure 平臺作業系統磁片 VHD 的位置和類型，而不是使用 **Set-Az VMSourceImage** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24c6d-152">In the case of a generalized user image, you also need to specify the *SourceImageUri* parameter and either the *Windows* or *Linux* parameters to tell the Azure platform the location and type of the operating system disk VHD instead of using the **Set-AzVMSourceImage** cmdlet.</span></span>
<span data-ttu-id="24c6d-153">在平臺圖像的情況下 *，VhdUri* 參數就足以滿足需要。</span><span class="sxs-lookup"><span data-stu-id="24c6d-153">In the case of a platform image, the *VhdUri* parameter is sufficient.</span></span> 
- <span data-ttu-id="24c6d-154">空。</span><span class="sxs-lookup"><span data-stu-id="24c6d-154">Empty.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24c6d-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24c6d-155">-DefaultProfile</span></span>
<span data-ttu-id="24c6d-156">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="24c6d-156">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24c6d-157">-DiffSettingSetting</span><span class="sxs-lookup"><span data-stu-id="24c6d-157">-DiffDiskSetting</span></span>
<span data-ttu-id="24c6d-158">指定作業系統磁片的不同磁片設定。</span><span class="sxs-lookup"><span data-stu-id="24c6d-158">Specifies the differencing disk settings for operating system disk.</span></span>

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

### <span data-ttu-id="24c6d-159">-DiskEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="24c6d-159">-DiskEncryptionKeyUrl</span></span>
<span data-ttu-id="24c6d-160">指定磁片加密金鑰的位置。</span><span class="sxs-lookup"><span data-stu-id="24c6d-160">Specifies the location of the disk encryption key.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: True
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24c6d-161">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="24c6d-161">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="24c6d-162">指定包含磁片加密金鑰之金鑰庫的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="24c6d-162">Specifies the resource ID of the Key Vault containing the disk encryption key.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: True
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24c6d-163">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="24c6d-163">-DiskEncryptionSetId</span></span>
<span data-ttu-id="24c6d-164">指定客戶管理的磁片加密集的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="24c6d-164">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="24c6d-165">這僅適用于受管理的磁片。</span><span class="sxs-lookup"><span data-stu-id="24c6d-165">This can only be specified for managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24c6d-166">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="24c6d-166">-DiskSizeInGB</span></span>
<span data-ttu-id="24c6d-167">指定作業系統磁片的大小 ，以 GB 為單位。</span><span class="sxs-lookup"><span data-stu-id="24c6d-167">Specifies the size, in GB, of the operating system disk.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24c6d-168">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="24c6d-168">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="24c6d-169">指定金鑰加密金鑰的位置。</span><span class="sxs-lookup"><span data-stu-id="24c6d-169">Specifies the location of the key encryption key.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24c6d-170">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="24c6d-170">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="24c6d-171">指定包含金鑰加密金鑰之金鑰庫的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="24c6d-171">Specifies the resource ID of the Key Vault containing the key encryption key.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24c6d-172">-Linux</span><span class="sxs-lookup"><span data-stu-id="24c6d-172">-Linux</span></span>
<span data-ttu-id="24c6d-173">表示使用者映射上的作業系統是 Linux。</span><span class="sxs-lookup"><span data-stu-id="24c6d-173">Indicates that the operating system on the user image is Linux.</span></span>
<span data-ttu-id="24c6d-174">為使用者映射型虛擬機器部署指定此參數。</span><span class="sxs-lookup"><span data-stu-id="24c6d-174">Specify this parameter for user image based virtual machine deployment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LinuxParamSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24c6d-175">-Managed也Id</span><span class="sxs-lookup"><span data-stu-id="24c6d-175">-ManagedDiskId</span></span>
<span data-ttu-id="24c6d-176">指定受管理磁片的識別碼。</span><span class="sxs-lookup"><span data-stu-id="24c6d-176">Specifies the ID of a managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24c6d-177">-名稱</span><span class="sxs-lookup"><span data-stu-id="24c6d-177">-Name</span></span>
<span data-ttu-id="24c6d-178">指定作業系統磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="24c6d-178">Specifies the name of the operating system disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: OSDiskName, DiskName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24c6d-179">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="24c6d-179">-SourceImageUri</span></span>
<span data-ttu-id="24c6d-180">指定使用者影像案例的 VHD URI。</span><span class="sxs-lookup"><span data-stu-id="24c6d-180">Specifies the URI of the VHD for user image scenarios.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourceImage

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24c6d-181">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="24c6d-181">-StorageAccountType</span></span>
<span data-ttu-id="24c6d-182">指定受管理磁片的儲存帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="24c6d-182">Specifies the storage account type of managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24c6d-183">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="24c6d-183">-VhdUri</span></span>
<span data-ttu-id="24c6d-184">指定虛擬硬碟的 URI (URI) VHD (URI) 。</span><span class="sxs-lookup"><span data-stu-id="24c6d-184">Specifies the Uniform Resource Identifier (URI) of a virtual hard disk (VHD).</span></span>
<span data-ttu-id="24c6d-185">對於以圖像為基礎的虛擬機器，此參數會指定指定平臺映射或使用者映射時要建立 VHD 檔案。</span><span class="sxs-lookup"><span data-stu-id="24c6d-185">For an image based virtual machine, this parameter specifies the VHD file to create when a platform image or user image is specified.</span></span>
<span data-ttu-id="24c6d-186">這是複製圖像二進位大型物件 (BLOB) 啟動虛擬機器的位置。</span><span class="sxs-lookup"><span data-stu-id="24c6d-186">This is the location from which the image binary large object (BLOB) is copied to start the virtual machine.</span></span>
<span data-ttu-id="24c6d-187">針對磁片型虛擬機器開機案例，此參數會指定虛擬機器直接用來啟動的 VHD 檔案。</span><span class="sxs-lookup"><span data-stu-id="24c6d-187">For a disk based virtual machine boot scenario, this parameter specifies the VHD file that the virtual machine uses directly for starting up.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: OSDiskVhdUri, DiskVhdUri

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24c6d-188">-VM</span><span class="sxs-lookup"><span data-stu-id="24c6d-188">-VM</span></span>
<span data-ttu-id="24c6d-189">指定要設定作業系統磁片屬性的本機虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="24c6d-189">Specifies the local virtual machine object on which to set operating system disk properties.</span></span>
<span data-ttu-id="24c6d-190">若要取得虛擬機器物件，請使用 Get-AzVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24c6d-190">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24c6d-191">-Windows</span><span class="sxs-lookup"><span data-stu-id="24c6d-191">-Windows</span></span>
<span data-ttu-id="24c6d-192">表示使用者映射上的作業系統是 Windows。</span><span class="sxs-lookup"><span data-stu-id="24c6d-192">Indicates that the operating system on the user image is Windows.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsParamSet, WindowsDiskEncryptionParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24c6d-193">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="24c6d-193">-WriteAccelerator</span></span>
<span data-ttu-id="24c6d-194">指定作業系統磁片上是否應該啟用或停用 WriteAccelerator。</span><span class="sxs-lookup"><span data-stu-id="24c6d-194">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24c6d-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24c6d-195">CommonParameters</span></span>
<span data-ttu-id="24c6d-196">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="24c6d-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24c6d-197">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="24c6d-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24c6d-198">輸入</span><span class="sxs-lookup"><span data-stu-id="24c6d-198">INPUTS</span></span>

### <span data-ttu-id="24c6d-199">Microsoft.Azure.Commands.Compute.models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="24c6d-199">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="24c6d-200">System.String</span><span class="sxs-lookup"><span data-stu-id="24c6d-200">System.String</span></span>

## <span data-ttu-id="24c6d-201">輸出</span><span class="sxs-lookup"><span data-stu-id="24c6d-201">OUTPUTS</span></span>

### <span data-ttu-id="24c6d-202">Microsoft.Azure.Commands.Compute.models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="24c6d-202">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="24c6d-203">筆記</span><span class="sxs-lookup"><span data-stu-id="24c6d-203">NOTES</span></span>

## <span data-ttu-id="24c6d-204">相關連結</span><span class="sxs-lookup"><span data-stu-id="24c6d-204">RELATED LINKS</span></span>

[<span data-ttu-id="24c6d-205">Get-AzMS</span><span class="sxs-lookup"><span data-stu-id="24c6d-205">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="24c6d-206">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="24c6d-206">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="24c6d-207">New-AzMSCONFIG</span><span class="sxs-lookup"><span data-stu-id="24c6d-207">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


