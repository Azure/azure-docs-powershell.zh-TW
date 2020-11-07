---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 8F7AF1B8-D769-452C-92CF-4486C3EB894D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmosdisk
schema: 2.0.0
ms.openlocfilehash: 8185b1072a6964941a4c6c837806d2df13f1cf7c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800525"
---
# <span data-ttu-id="8f4cf-101">Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="8f4cf-101">Set-AzureRmVMOSDisk</span></span>

## <span data-ttu-id="8f4cf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8f4cf-102">SYNOPSIS</span></span>
<span data-ttu-id="8f4cf-103">在虛擬機器上設定作業系統磁片屬性。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-103">Sets the operating system disk properties on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f4cf-104">句法</span><span class="sxs-lookup"><span data-stu-id="8f4cf-104">SYNTAX</span></span>

### <span data-ttu-id="8f4cf-105">DefaultParamSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8f4cf-105">DefaultParamSet (Default)</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <DiskCreateOptionTypes>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <StorageAccountTypes>]
 [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f4cf-106">WindowsParamSet</span><span class="sxs-lookup"><span data-stu-id="8f4cf-106">WindowsParamSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <DiskCreateOptionTypes>] [-Windows]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <StorageAccountTypes>]
 [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f4cf-107">WindowsDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f4cf-107">WindowsDiskEncryptionParameterSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <DiskCreateOptionTypes>] [-Windows]
 [-DiskEncryptionKeyUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <StorageAccountTypes>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8f4cf-108">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="8f4cf-108">LinuxParamSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <DiskCreateOptionTypes>] [-Linux]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <StorageAccountTypes>]
 [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f4cf-109">LinuxDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f4cf-109">LinuxDiskEncryptionParameterSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <DiskCreateOptionTypes>] [-Linux]
 [-DiskEncryptionKeyUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <StorageAccountTypes>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8f4cf-110">說明</span><span class="sxs-lookup"><span data-stu-id="8f4cf-110">DESCRIPTION</span></span>
<span data-ttu-id="8f4cf-111">**AzureRmVMOSDisk** Cmdlet 會在虛擬機器上設定作業系統磁片屬性。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-111">The **Set-AzureRmVMOSDisk** cmdlet sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="8f4cf-112">示例</span><span class="sxs-lookup"><span data-stu-id="8f4cf-112">EXAMPLES</span></span>

### <span data-ttu-id="8f4cf-113">範例1：從平臺影像設定虛擬機器上的屬性</span><span class="sxs-lookup"><span data-stu-id="8f4cf-113">Example 1: Set properties on a virtual machine from platform image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential) 
PS C:\> $VirtualMachine = Set-AzureRmVMSourceImage -VM $VirtualMachine -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.10" -Version "latest" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption FromImage
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="8f4cf-114">第一個命令會在名為 [ResourceGroup11] 的資源群組中取得名為 AvailablitySet13 的可用性集，然後將該物件儲存在 $AvailabilitySet 變數中。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-114">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="8f4cf-115">第二個命令會建立一個虛擬電腦物件，然後將它儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-115">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="8f4cf-116">該命令會將名稱和大小指派給虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-116">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="8f4cf-117">虛擬機器屬於儲存在 $AvailabilitySet 的可用性集。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-117">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="8f4cf-118">最終命令會在 $VirtualMachine 的虛擬機器上設定屬性。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-118">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="8f4cf-119">範例2：從通用使用者影像設定虛擬機器上的屬性</span><span class="sxs-lookup"><span data-stu-id="8f4cf-119">Example 2: Sets properties on a virtual machine from generalized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential)
PS C:\> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -SourceImageUri "https://mystorageaccount.blob.core.windows.net/vhds/myOSImage.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption fromImage -Linux
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="8f4cf-120">第一個命令會在名為 ResourceGroup11 的資源群組中取得名為 AvailablitySet13 的可用性集，並將該物件儲存在 $AvailabilitySet 變數中。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-120">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="8f4cf-121">第二個命令會建立一個虛擬電腦物件，並將它儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-121">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="8f4cf-122">該命令會將名稱和大小指派給虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-122">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="8f4cf-123">虛擬機器屬於儲存在 $AvailabilitySet 的可用性集。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-123">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="8f4cf-124">最終命令會在 $VirtualMachine 的虛擬機器上設定屬性。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-124">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="8f4cf-125">範例3：從特殊的使用者影像設定虛擬機器上的屬性</span><span class="sxs-lookup"><span data-stu-id="8f4cf-125">Example 3: Sets properties on a virtual machine from specialized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption Attach -Linux
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="8f4cf-126">第一個命令會在名為 ResourceGroup11 的資源群組中取得名為 AvailablitySet13 的可用性集，並將該物件儲存在 $AvailabilitySet 變數中。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-126">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="8f4cf-127">第二個命令會建立一個虛擬電腦物件，並將它儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-127">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="8f4cf-128">該命令會將名稱和大小指派給虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-128">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="8f4cf-129">虛擬機器屬於儲存在 $AvailabilitySet 的可用性集。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-129">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="8f4cf-130">最終命令會在 $VirtualMachine 的虛擬機器上設定屬性。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-130">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="8f4cf-131">範例4：在虛擬機器作業系統磁片上設定磁片加密設定</span><span class="sxs-lookup"><span data-stu-id="8f4cf-131">Example 4: Set the disk encryption settings on a virtual machine operating system disk</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite -Windows -CreateOption "Attach" -DiskEncryptionKeyUrl "https://mytestvault.vault.azure.net/secrets/Test1/514ceb769c984379a7e0230bddaaaaaa" -DiskEncryptionKeyVaultId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myresourcegroup/providers/Microsoft.KeyVault/vaults/mytestvault"
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName " ResourceGroup11"
```

<span data-ttu-id="8f4cf-132">這個範例會設定虛擬機器作業系統磁片上的磁片加密設定。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-132">This example sets the disk encryption settings on a virtual machine operating system disk.</span></span>

## <span data-ttu-id="8f4cf-133">參數</span><span class="sxs-lookup"><span data-stu-id="8f4cf-133">PARAMETERS</span></span>

### <span data-ttu-id="8f4cf-134">-快取</span><span class="sxs-lookup"><span data-stu-id="8f4cf-134">-Caching</span></span>
<span data-ttu-id="8f4cf-135">指定作業系統磁片的快取模式。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-135">Specifies the caching mode of the operating system disk.</span></span>
<span data-ttu-id="8f4cf-136">有效值為：</span><span class="sxs-lookup"><span data-stu-id="8f4cf-136">Valid values are:</span></span> 

- <span data-ttu-id="8f4cf-137">唯讀</span><span class="sxs-lookup"><span data-stu-id="8f4cf-137">ReadOnly</span></span>
- <span data-ttu-id="8f4cf-138">讀</span><span class="sxs-lookup"><span data-stu-id="8f4cf-138">ReadWrite</span></span>

<span data-ttu-id="8f4cf-139">預設值為 ReadWrite。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-139">The default value is ReadWrite.</span></span>
<span data-ttu-id="8f4cf-140">變更快取值會導致虛擬機器重新開機。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-140">Changing the caching value causes the virtual machine to restart.</span></span>

<span data-ttu-id="8f4cf-141">此設定會影響磁片的效能。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-141">This setting affects the performance of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f4cf-142">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="8f4cf-142">-CreateOption</span></span>
<span data-ttu-id="8f4cf-143">指定此 Cmdlet 是否在虛擬機器中從平臺或使用者影像建立磁片，或附加現有的磁片。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-143">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, or attaches an existing disk.</span></span>
<span data-ttu-id="8f4cf-144">有效值為：</span><span class="sxs-lookup"><span data-stu-id="8f4cf-144">Valid values are:</span></span> 

- <span data-ttu-id="8f4cf-145">選用.</span><span class="sxs-lookup"><span data-stu-id="8f4cf-145">Attach.</span></span>
<span data-ttu-id="8f4cf-146">指定此選項以從專用磁片建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-146">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="8f4cf-147">當您指定此選項時，請勿指定 *SourceImageUri* 參數。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-147">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="8f4cf-148">請改為使用 Set-AzureRmVMSourceImage Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-148">Instead, use the Set-AzureRmVMSourceImage cmdlet.</span></span>
<span data-ttu-id="8f4cf-149">您也必須使用 [ *Windows* ] 或 [ *Linux* ] 參數來告訴 azure2 平臺在 VHD 上的作業系統類型。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-149">You must also use the use the *Windows* or *Linux* parameters to tell the azure2 platform the type of the operating system on the VHD.</span></span>
<span data-ttu-id="8f4cf-150">*VhdUri* 參數足以告知 azure2 平臺要附加的磁片位置。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-150">The *VhdUri* parameter is enough to tell the azure2 platform the location of the disk to attach.</span></span> 
- <span data-ttu-id="8f4cf-151">FromImage.</span><span class="sxs-lookup"><span data-stu-id="8f4cf-151">FromImage.</span></span>
<span data-ttu-id="8f4cf-152">指定此選項以從平臺影像或一般化使用者影像建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-152">Specify this option to create a virtual machine from a platform image or a generalized user image.</span></span>
<span data-ttu-id="8f4cf-153">在通用使用者影像的情況下，您也需要指定 *SourceImageUri* 參數，以及 *Windows* 或 *Linux* 參數，以告知 Azure 平臺是作業系統磁片 VHD 的位置和類型，而不是使用 **AzureRmVMSourceImage** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-153">In the case of a generalized user image, you also need to specify the *SourceImageUri* parameter and either the *Windows* or *Linux* parameters to tell the Azure platform the location and type of the operating system disk VHD instead of using the **Set-AzureRmVMSourceImage** cmdlet.</span></span>
<span data-ttu-id="8f4cf-154">如果是平臺影像，則 *VhdUri* 參數就足夠了。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-154">In the case of a platform image, the *VhdUri* parameter is sufficient.</span></span> 
- <span data-ttu-id="8f4cf-155">有空.</span><span class="sxs-lookup"><span data-stu-id="8f4cf-155">Empty.</span></span>

```yaml
Type: DiskCreateOptionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f4cf-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f4cf-156">-DefaultProfile</span></span>
<span data-ttu-id="8f4cf-157">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f4cf-158">-DiskEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="8f4cf-158">-DiskEncryptionKeyUrl</span></span>
<span data-ttu-id="8f4cf-159">指定磁片加密金鑰的位置。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-159">Specifies the location of the disk encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f4cf-160">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="8f4cf-160">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="8f4cf-161">指定包含磁片加密金鑰之主要電子倉庫的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-161">Specifies the resource ID of the Key Vault containing the disk encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: True
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f4cf-162">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="8f4cf-162">-DiskSizeInGB</span></span>
<span data-ttu-id="8f4cf-163">指定作業系統磁片的大小（以 GB 為來）。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-163">Specifies the size, in GB, of the operating system disk.</span></span>

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

### <span data-ttu-id="8f4cf-164">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="8f4cf-164">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="8f4cf-165">指定金鑰加密金鑰的位置。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-165">Specifies the location of the key encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f4cf-166">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="8f4cf-166">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="8f4cf-167">指定包含金鑰加密金鑰的主要保存庫的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-167">Specifies the resource ID of the Key Vault containing the key encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f4cf-168">-Linux</span><span class="sxs-lookup"><span data-stu-id="8f4cf-168">-Linux</span></span>
<span data-ttu-id="8f4cf-169">表示使用者影像上的作業系統是 Linux。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-169">Indicates that the operating system on the user image is Linux.</span></span>
<span data-ttu-id="8f4cf-170">針對以使用者映射為基礎的虛擬機器部署指定此參數。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-170">Specify this parameter for user image based virtual machine deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LinuxParamSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f4cf-171">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="8f4cf-171">-ManagedDiskId</span></span>
<span data-ttu-id="8f4cf-172">指定受管理磁片的 ID。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-172">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="8f4cf-173">-名稱</span><span class="sxs-lookup"><span data-stu-id="8f4cf-173">-Name</span></span>
<span data-ttu-id="8f4cf-174">指定作業系統磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-174">Specifies the name of the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: OSDiskName, DiskName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f4cf-175">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="8f4cf-175">-SourceImageUri</span></span>
<span data-ttu-id="8f4cf-176">指定使用者影像案例的 VHD URI。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-176">Specifies the URI of the VHD for user image scenarios.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SourceImage

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f4cf-177">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="8f4cf-177">-StorageAccountType</span></span>
<span data-ttu-id="8f4cf-178">指定受管理磁片的儲存帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-178">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="8f4cf-179">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="8f4cf-179">-VhdUri</span></span>
<span data-ttu-id="8f4cf-180">指定虛擬硬碟 (VHD)  (URI) 的統一資源識別項。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-180">Specifies the Uniform Resource Identifier (URI) of a virtual hard disk (VHD).</span></span>

<span data-ttu-id="8f4cf-181">針對以影像為基礎的虛擬機器，此參數會指定要在指定平臺影像或使用者影像時建立的 VHD 檔案。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-181">For an image based virtual machine, this parameter specifies the VHD file to create when a platform image or user image is specified.</span></span>
<span data-ttu-id="8f4cf-182">此位置是複製影像二進位大型物件 (BLOB) 的位置，以啟動虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-182">This is the location from which the image binary large object (BLOB) is copied to start the virtual machine.</span></span>

<span data-ttu-id="8f4cf-183">針對以磁片為基礎的虛擬電腦啟動案例，此參數會指定虛擬機器直接用來啟動的 VHD 檔案。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-183">For a disk based virtual machine boot scenario, this parameter specifies the VHD file that the virtual machine uses directly for starting up.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: OSDiskVhdUri, DiskVhdUri

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f4cf-184">-VM</span><span class="sxs-lookup"><span data-stu-id="8f4cf-184">-VM</span></span>
<span data-ttu-id="8f4cf-185">指定要設定作業系統磁片屬性的本機虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-185">Specifies the local virtual machine object on which to set operating system disk properties.</span></span>
<span data-ttu-id="8f4cf-186">若要取得虛擬機器物件，請使用 Get-AzureRmVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-186">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f4cf-187">-Windows</span><span class="sxs-lookup"><span data-stu-id="8f4cf-187">-Windows</span></span>
<span data-ttu-id="8f4cf-188">表示使用者影像上的作業系統是 Windows。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-188">Indicates that the operating system on the user image is Windows.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WindowsParamSet, WindowsDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f4cf-189">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="8f4cf-189">-WriteAccelerator</span></span>
<span data-ttu-id="8f4cf-190">指定是否應該在 OS 磁片上啟用或停用 WriteAccelerator。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-190">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="8f4cf-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f4cf-191">CommonParameters</span></span>
<span data-ttu-id="8f4cf-192">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f4cf-193">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8f4cf-193">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f4cf-194">輸入</span><span class="sxs-lookup"><span data-stu-id="8f4cf-194">INPUTS</span></span>

### <span data-ttu-id="8f4cf-195">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="8f4cf-195">PSVirtualMachine</span></span>
<span data-ttu-id="8f4cf-196">[VM "參數從管線接受類型 ' PSVirtualMachine」的值</span><span class="sxs-lookup"><span data-stu-id="8f4cf-196">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="8f4cf-197">輸出</span><span class="sxs-lookup"><span data-stu-id="8f4cf-197">OUTPUTS</span></span>

### <span data-ttu-id="8f4cf-198">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="8f4cf-198">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="8f4cf-199">筆記</span><span class="sxs-lookup"><span data-stu-id="8f4cf-199">NOTES</span></span>

## <span data-ttu-id="8f4cf-200">相關連結</span><span class="sxs-lookup"><span data-stu-id="8f4cf-200">RELATED LINKS</span></span>

[<span data-ttu-id="8f4cf-201">AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8f4cf-201">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="8f4cf-202">AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="8f4cf-202">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="8f4cf-203">新-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="8f4cf-203">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


