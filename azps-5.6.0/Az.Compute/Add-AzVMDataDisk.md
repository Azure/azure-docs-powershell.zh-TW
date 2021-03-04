---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
ms.openlocfilehash: 685a1768dac652b3981bd081a2f8b29997c08639
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909213"
---
# <span data-ttu-id="59445-101">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="59445-101">Add-AzVMDataDisk</span></span>

## <span data-ttu-id="59445-102">簡介</span><span class="sxs-lookup"><span data-stu-id="59445-102">SYNOPSIS</span></span>
<span data-ttu-id="59445-103">新增資料磁片至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="59445-103">Adds a data disk to a virtual machine.</span></span>

## <span data-ttu-id="59445-104">語法</span><span class="sxs-lookup"><span data-stu-id="59445-104">SYNTAX</span></span>

### <span data-ttu-id="59445-105">VmNormalParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="59445-105">VmNormalDiskParameterSetName (Default)</span></span>
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-SourceImageUri] <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59445-106">VmManagedParameterSetName</span><span class="sxs-lookup"><span data-stu-id="59445-106">VmManagedDiskParameterSetName</span></span>
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-ManagedDiskId] <String>]
 [[-StorageAccountType] <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59445-107">描述</span><span class="sxs-lookup"><span data-stu-id="59445-107">DESCRIPTION</span></span>
<span data-ttu-id="59445-108">**Add-AzCMDataDataData Cmdlet** 會將資料磁片新增到虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="59445-108">The **Add-AzVMDataDisk** cmdlet adds a data disk to a virtual machine.</span></span>
<span data-ttu-id="59445-109">您可以在建立虛擬機器時新增資料磁片，也可以新增資料磁片至現有的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="59445-109">You can add a data disk when you create a virtual machine, or you can add a data disk to an existing virtual machine.</span></span>

## <span data-ttu-id="59445-110">例子</span><span class="sxs-lookup"><span data-stu-id="59445-110">EXAMPLES</span></span>

### <span data-ttu-id="59445-111">範例 1：新增資料磁片至新的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="59445-111">Example 1: Add data disks to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

<span data-ttu-id="59445-112">第一個命令會建立虛擬機器物件，然後將它儲存在$VirtualMachine變數中。</span><span class="sxs-lookup"><span data-stu-id="59445-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="59445-113">該命令會為虛擬機器指定名稱和大小。</span><span class="sxs-lookup"><span data-stu-id="59445-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="59445-114">接下來三個命令會指派三個數據磁片的路徑給$DataDiskVhdUri 01、$DataDiskVhdUri 02 和 $DataDiskVhdUri 03 變數。</span><span class="sxs-lookup"><span data-stu-id="59445-114">The next three commands assign paths of three data disks to the $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03 variables.</span></span>
<span data-ttu-id="59445-115">此方法僅適用于下列命令的可讀性。</span><span class="sxs-lookup"><span data-stu-id="59445-115">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="59445-116">最後三個命令各自會將資料磁片新增到儲存在 $VirtualMachine 中的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="59445-116">The final three commands each adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="59445-117">命令會指定磁片的名稱和位置，以及磁片的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="59445-117">The command specifies the name and location for the disk, and other properties of the disk.</span></span>
<span data-ttu-id="59445-118">每個磁片的 URI 會儲存在 $DataDiskVhdUri 01、$DataDiskVhdUri 02 和 $DataDiskVhdUri 03。</span><span class="sxs-lookup"><span data-stu-id="59445-118">The URI of each disk is stored in $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03.</span></span>

### <span data-ttu-id="59445-119">範例 2：新增資料磁片至現有的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="59445-119">Example 2: Add a data disk to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="59445-120">第一個命令會使用 [Get-Az VIRTUAL](./Get-AzVM.md) Cmdlet 取得名為 VirtualMachine07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="59445-120">The first command gets the virtual machine named VirtualMachine07 by using the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="59445-121">該命令將虛擬機器儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="59445-121">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="59445-122">第二個命令會將資料磁片新增到儲存在 $VirtualMachine 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="59445-122">The second command adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="59445-123">最後一個命令會更新儲存在 ResourceGroup11 $VirtualMachine的狀態。</span><span class="sxs-lookup"><span data-stu-id="59445-123">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

### <span data-ttu-id="59445-124">範例 3：從一般使用者映射新增資料磁片至新虛擬機器</span><span class="sxs-lookup"><span data-stu-id="59445-124">Example 3: Add a data disk to a new virtual machine from a generalized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

<span data-ttu-id="59445-125">第一個命令會建立虛擬機器物件，並儲存在$VirtualMachine變數中。</span><span class="sxs-lookup"><span data-stu-id="59445-125">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="59445-126">該命令會為虛擬機器指定名稱和大小。</span><span class="sxs-lookup"><span data-stu-id="59445-126">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="59445-127">接下來兩個命令會分別將資料影像和資料磁片路徑指派給$DataImageUri$DataDiskUri變數。</span><span class="sxs-lookup"><span data-stu-id="59445-127">The next two commands assign paths for the data image and data disks to the $DataImageUri and $DataDiskUri variables respectively.</span></span>
<span data-ttu-id="59445-128">此方法用來改善下列命令的可讀性。</span><span class="sxs-lookup"><span data-stu-id="59445-128">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="59445-129">最後的命令會將資料磁片新增到儲存在 $VirtualMachine 中的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="59445-129">The final commands adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="59445-130">命令會指定磁片的名稱與位置，以及磁片的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="59445-130">The command specifies the name and location for the disk and other properties of the disk.</span></span>

### <span data-ttu-id="59445-131">範例 4：從特殊使用者映射新增資料磁片至新虛擬機器</span><span class="sxs-lookup"><span data-stu-id="59445-131">Example 4: Add data disks to a new virtual machine from a specialized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

<span data-ttu-id="59445-132">第一個命令會建立虛擬機器物件，並儲存在$VirtualMachine變數中。</span><span class="sxs-lookup"><span data-stu-id="59445-132">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="59445-133">該命令會為虛擬機器指定名稱和大小。</span><span class="sxs-lookup"><span data-stu-id="59445-133">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="59445-134">下一個命令會指定資料磁片的路徑至$DataDiskUri變數。</span><span class="sxs-lookup"><span data-stu-id="59445-134">The next commands assigns paths of the data disk to the $DataDiskUri variable.</span></span>
<span data-ttu-id="59445-135">此方法用來改善下列命令的可讀性。</span><span class="sxs-lookup"><span data-stu-id="59445-135">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="59445-136">最後一個命令是新增資料磁片至儲存在 $VirtualMachine。</span><span class="sxs-lookup"><span data-stu-id="59445-136">The final command add a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="59445-137">命令會指定磁片的名稱和位置，以及磁片的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="59445-137">The command specifies the name and location for the disk, and other properties of the disk.</span></span>

## <span data-ttu-id="59445-138">參數</span><span class="sxs-lookup"><span data-stu-id="59445-138">PARAMETERS</span></span>

### <span data-ttu-id="59445-139">-緩存</span><span class="sxs-lookup"><span data-stu-id="59445-139">-Caching</span></span>
<span data-ttu-id="59445-140">指定磁片的緩存模式。</span><span class="sxs-lookup"><span data-stu-id="59445-140">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="59445-141">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="59445-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="59445-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="59445-142">ReadOnly</span></span>
- <span data-ttu-id="59445-143">朗讀</span><span class="sxs-lookup"><span data-stu-id="59445-143">ReadWrite</span></span>
- <span data-ttu-id="59445-144">None 預設值為 ReadWrite。</span><span class="sxs-lookup"><span data-stu-id="59445-144">None The default value is ReadWrite.</span></span>
<span data-ttu-id="59445-145">變更此值會導致虛擬機器重新開機。</span><span class="sxs-lookup"><span data-stu-id="59445-145">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="59445-146">此設定會影響磁片的一致性與績效。</span><span class="sxs-lookup"><span data-stu-id="59445-146">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="59445-147">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="59445-147">-CreateOption</span></span>
<span data-ttu-id="59445-148">指定此 Cmdlet 是否要從平臺或使用者映射在虛擬機器中建立磁片、建立空白磁片，或附加到現有的磁片。</span><span class="sxs-lookup"><span data-stu-id="59445-148">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="59445-149">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="59445-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="59445-150">附加。</span><span class="sxs-lookup"><span data-stu-id="59445-150">Attach.</span></span>
<span data-ttu-id="59445-151">指定此選項以從特殊磁片建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="59445-151">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="59445-152">當您指定此選項時，請勿指定 *SourceImageUri* 參數。</span><span class="sxs-lookup"><span data-stu-id="59445-152">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="59445-153">*VhdUri* 是告知 Azure 平臺虛擬硬碟 (VHD) 以資料磁片附加至虛擬機器所需的一切。</span><span class="sxs-lookup"><span data-stu-id="59445-153">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="59445-154">空。</span><span class="sxs-lookup"><span data-stu-id="59445-154">Empty.</span></span>
<span data-ttu-id="59445-155">指定此選項以建立空白的資料磁片。</span><span class="sxs-lookup"><span data-stu-id="59445-155">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="59445-156">FromImage.</span><span class="sxs-lookup"><span data-stu-id="59445-156">FromImage.</span></span>
<span data-ttu-id="59445-157">指定此選項以從一般圖像或磁片建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="59445-157">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="59445-158">當您指定此選項時，您必須指定 *SourceImageUri* 參數，才能告訴 Azure 平臺要附加為數據磁片的 VHD 位置。</span><span class="sxs-lookup"><span data-stu-id="59445-158">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="59445-159">*VhdUri* 參數會用來當虛擬機器使用資料磁片 VHD 時，用來識別資料磁片 VHD 儲存的位置。</span><span class="sxs-lookup"><span data-stu-id="59445-159">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

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

### <span data-ttu-id="59445-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59445-160">-DefaultProfile</span></span>
<span data-ttu-id="59445-161">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="59445-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59445-162">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="59445-162">-DiskEncryptionSetId</span></span>
<span data-ttu-id="59445-163">指定客戶管理的磁片加密集的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="59445-163">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="59445-164">這僅適用于受管理的磁片。</span><span class="sxs-lookup"><span data-stu-id="59445-164">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="59445-165">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="59445-165">-DiskSizeInGB</span></span>
<span data-ttu-id="59445-166">指定要附加到虛擬機器的空白磁片大小 ，以 GB 為單位。</span><span class="sxs-lookup"><span data-stu-id="59445-166">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

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

### <span data-ttu-id="59445-167">-四分位</span><span class="sxs-lookup"><span data-stu-id="59445-167">-Lun</span></span>
<span data-ttu-id="59445-168">指定資料磁片的 (或) 邏輯單位編號。</span><span class="sxs-lookup"><span data-stu-id="59445-168">Specifies the logical unit number (LUN) for a data disk.</span></span>

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

### <span data-ttu-id="59445-169">-Managed也Id</span><span class="sxs-lookup"><span data-stu-id="59445-169">-ManagedDiskId</span></span>
<span data-ttu-id="59445-170">指定受管理磁片的識別碼。</span><span class="sxs-lookup"><span data-stu-id="59445-170">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="59445-171">-名稱</span><span class="sxs-lookup"><span data-stu-id="59445-171">-Name</span></span>
<span data-ttu-id="59445-172">指定要新增的資料磁片名稱。</span><span class="sxs-lookup"><span data-stu-id="59445-172">Specifies the name of the data disk to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59445-173">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="59445-173">-SourceImageUri</span></span>
<span data-ttu-id="59445-174">指定此 Cmdlet 所附加到磁片的來源 URI。</span><span class="sxs-lookup"><span data-stu-id="59445-174">Specifies the source URI of the disk that this cmdlet attaches.</span></span>

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

### <span data-ttu-id="59445-175">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="59445-175">-StorageAccountType</span></span>
<span data-ttu-id="59445-176">指定受管理磁片的儲存帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="59445-176">Specifies the storage account type of managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59445-177">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="59445-177">-VhdUri</span></span>
<span data-ttu-id="59445-178">指定虛擬硬碟 (VHD) 檔案的統一資源識別項 (URI) ，以在使用平臺映射或使用者映射時建立。</span><span class="sxs-lookup"><span data-stu-id="59445-178">Specifies the Uniform Resource Identifier (URI) for the virtual hard disk (VHD) file to create when a platform image or user image is used.</span></span>
<span data-ttu-id="59445-179">此 Cmdlet 會複製圖像二進位大型物件 (blob) 到此位置。</span><span class="sxs-lookup"><span data-stu-id="59445-179">This cmdlet copies the image binary large object (blob) to this location.</span></span>
<span data-ttu-id="59445-180">這是啟動虛擬機器的位置。</span><span class="sxs-lookup"><span data-stu-id="59445-180">This is the location from which to start the virtual machine.</span></span>

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

### <span data-ttu-id="59445-181">-VM</span><span class="sxs-lookup"><span data-stu-id="59445-181">-VM</span></span>
<span data-ttu-id="59445-182">指定要新增資料磁片的本機虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="59445-182">Specifies the local virtual machine object to which to add a data disk.</span></span>
<span data-ttu-id="59445-183">您可以使用 **Get-AzMS** Cmdlet 來取得虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="59445-183">You can use the **Get-AzVM** cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="59445-184">您可以使用 **New-AzMSConfig** Cmdlet 來建立虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="59445-184">You can use the **New-AzVMConfig** cmdlet to create a virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59445-185">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="59445-185">-WriteAccelerator</span></span>
<span data-ttu-id="59445-186">指定是否應該在受管理的資料磁片上啟用或停用 WriteAccelerator。</span><span class="sxs-lookup"><span data-stu-id="59445-186">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59445-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59445-187">CommonParameters</span></span>
<span data-ttu-id="59445-188">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="59445-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59445-189">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="59445-189">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59445-190">輸入</span><span class="sxs-lookup"><span data-stu-id="59445-190">INPUTS</span></span>

### <span data-ttu-id="59445-191">Microsoft.Azure.Commands.Compute.models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="59445-191">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="59445-192">System.String</span><span class="sxs-lookup"><span data-stu-id="59445-192">System.String</span></span>

### <span data-ttu-id="59445-193">Microsoft.Azure.management.Compute.models.CachingTypes</span><span class="sxs-lookup"><span data-stu-id="59445-193">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="59445-194">System.Nullable'1[[System.Int32， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="59445-194">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="59445-195">輸出</span><span class="sxs-lookup"><span data-stu-id="59445-195">OUTPUTS</span></span>

### <span data-ttu-id="59445-196">Microsoft.Azure.Commands.Compute.models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="59445-196">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="59445-197">Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSetVT</span><span class="sxs-lookup"><span data-stu-id="59445-197">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="59445-198">筆記</span><span class="sxs-lookup"><span data-stu-id="59445-198">NOTES</span></span>

## <span data-ttu-id="59445-199">相關連結</span><span class="sxs-lookup"><span data-stu-id="59445-199">RELATED LINKS</span></span>

[<span data-ttu-id="59445-200">Remove-AzDATAData一體式應用程式</span><span class="sxs-lookup"><span data-stu-id="59445-200">Remove-AzVMDataDisk</span></span>](./Remove-AzVMDataDisk.md)

[<span data-ttu-id="59445-201">Get-AzMS</span><span class="sxs-lookup"><span data-stu-id="59445-201">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="59445-202">New-AzMSCONFIG</span><span class="sxs-lookup"><span data-stu-id="59445-202">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
