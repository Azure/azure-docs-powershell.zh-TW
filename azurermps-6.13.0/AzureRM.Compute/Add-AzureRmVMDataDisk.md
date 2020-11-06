---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVMDataDisk.md
ms.openlocfilehash: de0f5fd2583f1622e750e71299a5753444feed1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451903"
---
# <span data-ttu-id="6eec5-101">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="6eec5-101">Add-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="6eec5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6eec5-102">SYNOPSIS</span></span>
<span data-ttu-id="6eec5-103">在虛擬機器或 Vmss VM 中新增資料磁片。</span><span class="sxs-lookup"><span data-stu-id="6eec5-103">Adds a data disk to a virtual machine or a Vmss VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6eec5-104">句法</span><span class="sxs-lookup"><span data-stu-id="6eec5-104">SYNTAX</span></span>

### <span data-ttu-id="6eec5-105">VmNormalDiskParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="6eec5-105">VmNormalDiskParameterSetName (Default)</span></span>
```
Add-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String>
 [[-SourceImageUri] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6eec5-106">VmManagedDiskParameterSetName</span><span class="sxs-lookup"><span data-stu-id="6eec5-106">VmManagedDiskParameterSetName</span></span>
```
Add-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-ManagedDiskId] <String>]
 [[-StorageAccountType] <String>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6eec5-107">VmScaleSetVMParameterSetName</span><span class="sxs-lookup"><span data-stu-id="6eec5-107">VmScaleSetVMParameterSetName</span></span>
```
Add-AzureRmVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [-ManagedDiskId] <String>
 [[-StorageAccountType] <String>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6eec5-108">說明</span><span class="sxs-lookup"><span data-stu-id="6eec5-108">DESCRIPTION</span></span>
<span data-ttu-id="6eec5-109">**載入 AzureRmVMDataDisk** Cmdlet 會將資料磁片新增至虛擬機器或 Vmss VM。</span><span class="sxs-lookup"><span data-stu-id="6eec5-109">The **Add-AzureRmVMDataDisk** cmdlet adds a data disk to a virtual machine or a Vmss VM.</span></span>
<span data-ttu-id="6eec5-110">您可以在建立虛擬機器時新增資料磁片，也可以將資料磁片新增至現有的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="6eec5-110">You can add a data disk when you create a virtual machine, or you can add a data disk to an existing virtual machine.</span></span>

## <span data-ttu-id="6eec5-111">示例</span><span class="sxs-lookup"><span data-stu-id="6eec5-111">EXAMPLES</span></span>

### <span data-ttu-id="6eec5-112">範例1：將資料磁片新增至新的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="6eec5-112">Example 1: Add data disks to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

<span data-ttu-id="6eec5-113">第一個命令會建立一個虛擬電腦物件，然後將它儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="6eec5-113">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="6eec5-114">該命令會將名稱和大小指派給虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="6eec5-114">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="6eec5-115">接下來的三個命令會將三個數據磁片的路徑指派給 $DataDiskVhdUri 01、$DataDiskVhdUri 02 及 $DataDiskVhdUri 3 個變數。</span><span class="sxs-lookup"><span data-stu-id="6eec5-115">The next three commands assign paths of three data disks to the $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03 variables.</span></span>
<span data-ttu-id="6eec5-116">這個方法只是為了讓您瞭解下列命令的可讀性。</span><span class="sxs-lookup"><span data-stu-id="6eec5-116">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="6eec5-117">最後三個命令會將資料磁片新增至儲存在 $VirtualMachine 的虛擬機器中。</span><span class="sxs-lookup"><span data-stu-id="6eec5-117">The final three commands each adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="6eec5-118">此命令會指定磁片的名稱和位置，以及磁片的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="6eec5-118">The command specifies the name and location for the disk, and other properties of the disk.</span></span>
<span data-ttu-id="6eec5-119">每個磁片的 URI 都儲存在 $DataDiskVhdUri 01、$DataDiskVhdUri 02 和 $DataDiskVhdUri 03 中。</span><span class="sxs-lookup"><span data-stu-id="6eec5-119">The URI of each disk is stored in $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03.</span></span>

### <span data-ttu-id="6eec5-120">範例2：新增資料磁片至現有的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="6eec5-120">Example 2: Add a data disk to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="6eec5-121">第一個命令會使用 [AzureRmVM](./Get-AzureRmVM.md) Cmdlet 取得名為 VirtualMachine07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="6eec5-121">The first command gets the virtual machine named VirtualMachine07 by using the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="6eec5-122">該命令會將虛擬機器儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="6eec5-122">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="6eec5-123">第二個命令會將資料磁片新增至儲存在 $VirtualMachine 的虛擬機器中。</span><span class="sxs-lookup"><span data-stu-id="6eec5-123">The second command adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="6eec5-124">Final 命令會更新儲存在 ResourceGroup11 中 $VirtualMachine 的虛擬機器狀態。</span><span class="sxs-lookup"><span data-stu-id="6eec5-124">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

### <span data-ttu-id="6eec5-125">範例3：從通用使用者影像將資料磁片新增至新的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="6eec5-125">Example 3: Add a data disk to a new virtual machine from a generalized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

<span data-ttu-id="6eec5-126">第一個命令會建立一個虛擬電腦物件，並將它儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="6eec5-126">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="6eec5-127">該命令會將名稱和大小指派給虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="6eec5-127">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="6eec5-128">接下來的兩個命令會將資料影像和資料磁片的路徑指派給 $DataImageUri，並分別 $DataDiskUri 變數。</span><span class="sxs-lookup"><span data-stu-id="6eec5-128">The next two commands assign paths for the data image and data disks to the $DataImageUri and $DataDiskUri variables respectively.</span></span>
<span data-ttu-id="6eec5-129">這個方法是用來改善下列命令的可讀性。</span><span class="sxs-lookup"><span data-stu-id="6eec5-129">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="6eec5-130">最終命令會將資料磁片新增至儲存在 $VirtualMachine 的虛擬機器中。</span><span class="sxs-lookup"><span data-stu-id="6eec5-130">The final commands adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="6eec5-131">此命令會指定磁片的名稱和位置，以及磁片的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="6eec5-131">The command specifies the name and location for the disk and other properties of the disk.</span></span>

### <span data-ttu-id="6eec5-132">範例4：從特殊的使用者影像將資料磁片新增至新的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="6eec5-132">Example 4: Add data disks to a new virtual machine from a specialized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

<span data-ttu-id="6eec5-133">第一個命令會建立一個虛擬電腦物件，並將它儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="6eec5-133">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="6eec5-134">該命令會將名稱和大小指派給虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="6eec5-134">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="6eec5-135">Next 命令會將資料磁片的路徑指派給 $DataDiskUri 變數。</span><span class="sxs-lookup"><span data-stu-id="6eec5-135">The next commands assigns paths of the data disk to the $DataDiskUri variable.</span></span>
<span data-ttu-id="6eec5-136">這個方法是用來改善下列命令的可讀性。</span><span class="sxs-lookup"><span data-stu-id="6eec5-136">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="6eec5-137">最終命令會將資料磁片新增至儲存在 $VirtualMachine 的虛擬機器中。</span><span class="sxs-lookup"><span data-stu-id="6eec5-137">The final command add a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="6eec5-138">此命令會指定磁片的名稱和位置，以及磁片的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="6eec5-138">The command specifies the name and location for the disk, and other properties of the disk.</span></span>

### <span data-ttu-id="6eec5-139">範例5：將受管理的資料磁片新增至 Vmss VM。</span><span class="sxs-lookup"><span data-stu-id="6eec5-139">Example 5: Add a managed data disk to a Vmss VM.</span></span>
```
PS C:\> $disk = Get-AzureRmDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzureRmVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzureRmVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzureRmVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="6eec5-140">第一個命令會取得現有的受管理磁片。</span><span class="sxs-lookup"><span data-stu-id="6eec5-140">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="6eec5-141">Next 命令會取得資源群組名稱所提供的現有 Vmss VM、Vmss 名稱和實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="6eec5-141">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="6eec5-142">下一個命令會將受管理的磁片新增至儲存在本機 $VmssVM 的 Vmss VM 中。</span><span class="sxs-lookup"><span data-stu-id="6eec5-142">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="6eec5-143">Final 命令會使用已新增的資料磁片來更新 Vmss VM。</span><span class="sxs-lookup"><span data-stu-id="6eec5-143">The final command updates the Vmss VM with added data disk.</span></span>

## <span data-ttu-id="6eec5-144">參數</span><span class="sxs-lookup"><span data-stu-id="6eec5-144">PARAMETERS</span></span>

### <span data-ttu-id="6eec5-145">-快取</span><span class="sxs-lookup"><span data-stu-id="6eec5-145">-Caching</span></span>
<span data-ttu-id="6eec5-146">指定磁片的快取模式。</span><span class="sxs-lookup"><span data-stu-id="6eec5-146">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="6eec5-147">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="6eec5-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6eec5-148">唯讀</span><span class="sxs-lookup"><span data-stu-id="6eec5-148">ReadOnly</span></span>
- <span data-ttu-id="6eec5-149">讀</span><span class="sxs-lookup"><span data-stu-id="6eec5-149">ReadWrite</span></span>
- <span data-ttu-id="6eec5-150">None 預設值為 ReadWrite。</span><span class="sxs-lookup"><span data-stu-id="6eec5-150">None The default value is ReadWrite.</span></span>
<span data-ttu-id="6eec5-151">變更此值會導致虛擬機器重新開機。</span><span class="sxs-lookup"><span data-stu-id="6eec5-151">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="6eec5-152">此設定會影響磁片的一致性和效能。</span><span class="sxs-lookup"><span data-stu-id="6eec5-152">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6eec5-153">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="6eec5-153">-CreateOption</span></span>
<span data-ttu-id="6eec5-154">指定此 Cmdlet 是否在虛擬機器中從平臺或使用者影像建立磁片、建立空白磁片，或附加現有磁片。</span><span class="sxs-lookup"><span data-stu-id="6eec5-154">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="6eec5-155">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="6eec5-155">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6eec5-156">選用.</span><span class="sxs-lookup"><span data-stu-id="6eec5-156">Attach.</span></span>
<span data-ttu-id="6eec5-157">指定此選項以從專用磁片建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="6eec5-157">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="6eec5-158">當您指定此選項時，請勿指定 *SourceImageUri* 參數。</span><span class="sxs-lookup"><span data-stu-id="6eec5-158">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="6eec5-159">您需要 *VhdUri* ，才能告知 Azure 平臺將虛擬硬碟的位置 (VHD) 附加成資料磁片至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="6eec5-159">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="6eec5-160">有空.</span><span class="sxs-lookup"><span data-stu-id="6eec5-160">Empty.</span></span>
<span data-ttu-id="6eec5-161">指定此程式以建立空白的資料磁片。</span><span class="sxs-lookup"><span data-stu-id="6eec5-161">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="6eec5-162">FromImage.</span><span class="sxs-lookup"><span data-stu-id="6eec5-162">FromImage.</span></span>
<span data-ttu-id="6eec5-163">指定此選項以從通用影像或磁片建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="6eec5-163">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="6eec5-164">當您指定此選項時，您必須指定 *SourceImageUri* 參數，以告知 Azure 平臺要作為資料磁片附加的 VHD 位置。</span><span class="sxs-lookup"><span data-stu-id="6eec5-164">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="6eec5-165">*VhdUri* 參數是用來識別虛擬機器所使用的資料磁片 VHD 儲存位置。</span><span class="sxs-lookup"><span data-stu-id="6eec5-165">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6eec5-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eec5-166">-DefaultProfile</span></span>
<span data-ttu-id="6eec5-167">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6eec5-167">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6eec5-168">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="6eec5-168">-DiskSizeInGB</span></span>
<span data-ttu-id="6eec5-169">指定要附加至虛擬機器的空白磁片大小（以 gb 為位元組）。</span><span class="sxs-lookup"><span data-stu-id="6eec5-169">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6eec5-170">-Lun</span><span class="sxs-lookup"><span data-stu-id="6eec5-170">-Lun</span></span>
<span data-ttu-id="6eec5-171">指定資料磁片的邏輯單元號碼 (LUN) 。</span><span class="sxs-lookup"><span data-stu-id="6eec5-171">Specifies the logical unit number (LUN) for a data disk.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6eec5-172">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="6eec5-172">-ManagedDiskId</span></span>
<span data-ttu-id="6eec5-173">指定受管理磁片的 ID。</span><span class="sxs-lookup"><span data-stu-id="6eec5-173">Specifies the ID of a managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: VmScaleSetVMParameterSetName
Aliases:

Required: True
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6eec5-174">-名稱</span><span class="sxs-lookup"><span data-stu-id="6eec5-174">-Name</span></span>
<span data-ttu-id="6eec5-175">指定要新增的資料磁片名稱。</span><span class="sxs-lookup"><span data-stu-id="6eec5-175">Specifies the name of the data disk to add.</span></span>

```yaml
Type: System.String
Parameter Sets: VmNormalDiskParameterSetName, VmManagedDiskParameterSetName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6eec5-176">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="6eec5-176">-SourceImageUri</span></span>
<span data-ttu-id="6eec5-177">指定此 Cmdlet 附加磁片的來源 URI。</span><span class="sxs-lookup"><span data-stu-id="6eec5-177">Specifies the source URI of the disk that this cmdlet attaches.</span></span>

```yaml
Type: System.String
Parameter Sets: VmNormalDiskParameterSetName
Aliases: SourceImage

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6eec5-178">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="6eec5-178">-StorageAccountType</span></span>
<span data-ttu-id="6eec5-179">指定受管理磁片的儲存帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="6eec5-179">Specifies the storage account type of managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: VmManagedDiskParameterSetName, VmScaleSetVMParameterSetName
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6eec5-180">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="6eec5-180">-VhdUri</span></span>
<span data-ttu-id="6eec5-181">指定要在使用平臺影像或使用者影像時建立的虛擬硬碟 (VHD) 檔案 (URI) 的統一資源識別項。</span><span class="sxs-lookup"><span data-stu-id="6eec5-181">Specifies the Uniform Resource Identifier (URI) for the virtual hard disk (VHD) file to create when a platform image or user image is used.</span></span>
<span data-ttu-id="6eec5-182">這個 Cmdlet 會將影像二進位大型物件 (blob) 複製到此位置。</span><span class="sxs-lookup"><span data-stu-id="6eec5-182">This cmdlet copies the image binary large object (blob) to this location.</span></span>
<span data-ttu-id="6eec5-183">這是啟動虛擬機器的位置。</span><span class="sxs-lookup"><span data-stu-id="6eec5-183">This is the location from which to start the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: VmNormalDiskParameterSetName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6eec5-184">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="6eec5-184">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="6eec5-185">指定要新增資料磁片的本機虛擬機器縮放設定 VM 物件。</span><span class="sxs-lookup"><span data-stu-id="6eec5-185">Specifies the local virtual machine scale set VM object to which to add a data disk.</span></span>
<span data-ttu-id="6eec5-186">您可以使用 **AzureRmVmssVM** Cmdlet 來取得虛擬機器縮放設定 VM 物件。</span><span class="sxs-lookup"><span data-stu-id="6eec5-186">You can use the **Get-AzureRmVmssVM** cmdlet to obtain a virtual machine scale set VM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: VmScaleSetVMParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6eec5-187">-VM</span><span class="sxs-lookup"><span data-stu-id="6eec5-187">-VM</span></span>
<span data-ttu-id="6eec5-188">指定要新增資料磁片的本機虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="6eec5-188">Specifies the local virtual machine object to which to add a data disk.</span></span>
<span data-ttu-id="6eec5-189">您可以使用 **AzureRmVM** Cmdlet 來取得虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="6eec5-189">You can use the **Get-AzureRmVM** cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="6eec5-190">您可以使用 **新的 AzureRmVMConfig** Cmdlet 來建立虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="6eec5-190">You can use the **New-AzureRmVMConfig** cmdlet to create a virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: VmNormalDiskParameterSetName, VmManagedDiskParameterSetName
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6eec5-191">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="6eec5-191">-WriteAccelerator</span></span>
<span data-ttu-id="6eec5-192">指定是否應該在受管理的資料磁片上啟用或停用 WriteAccelerator。</span><span class="sxs-lookup"><span data-stu-id="6eec5-192">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VmManagedDiskParameterSetName, VmScaleSetVMParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6eec5-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eec5-193">CommonParameters</span></span>
<span data-ttu-id="6eec5-194">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6eec5-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eec5-195">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6eec5-195">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eec5-196">輸入</span><span class="sxs-lookup"><span data-stu-id="6eec5-196">INPUTS</span></span>

### <span data-ttu-id="6eec5-197">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="6eec5-197">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="6eec5-198">PSVirtualMachineScaleSetVM 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="6eec5-198">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

### <span data-ttu-id="6eec5-199">System.object</span><span class="sxs-lookup"><span data-stu-id="6eec5-199">System.String</span></span>

### <span data-ttu-id="6eec5-200">CachingTypes 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="6eec5-200">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="6eec5-201">System.object "1 [[System. Int32，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="6eec5-201">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="6eec5-202">輸出</span><span class="sxs-lookup"><span data-stu-id="6eec5-202">OUTPUTS</span></span>

### <span data-ttu-id="6eec5-203">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="6eec5-203">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="6eec5-204">PSVirtualMachineScaleSetVM 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="6eec5-204">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="6eec5-205">筆記</span><span class="sxs-lookup"><span data-stu-id="6eec5-205">NOTES</span></span>

## <span data-ttu-id="6eec5-206">相關連結</span><span class="sxs-lookup"><span data-stu-id="6eec5-206">RELATED LINKS</span></span>

[<span data-ttu-id="6eec5-207">移除-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="6eec5-207">Remove-AzureRmVMDataDisk</span></span>](./Remove-AzureRmVMDataDisk.md)

[<span data-ttu-id="6eec5-208">AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6eec5-208">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="6eec5-209">新-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="6eec5-209">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
