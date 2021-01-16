---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
ms.openlocfilehash: 29233b0bdce273205acffcb87dbf3a8adb1d4a52
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280544"
---
# <span data-ttu-id="aaf23-101">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="aaf23-101">Add-AzVMDataDisk</span></span>

## <span data-ttu-id="aaf23-102">摘要</span><span class="sxs-lookup"><span data-stu-id="aaf23-102">SYNOPSIS</span></span>
<span data-ttu-id="aaf23-103">將資料磁片新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="aaf23-103">Adds a data disk to a virtual machine.</span></span>

## <span data-ttu-id="aaf23-104">句法</span><span class="sxs-lookup"><span data-stu-id="aaf23-104">SYNTAX</span></span>

### <span data-ttu-id="aaf23-105">VmNormalDiskParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="aaf23-105">VmNormalDiskParameterSetName (Default)</span></span>
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-SourceImageUri] <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aaf23-106">VmManagedDiskParameterSetName</span><span class="sxs-lookup"><span data-stu-id="aaf23-106">VmManagedDiskParameterSetName</span></span>
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-ManagedDiskId] <String>]
 [[-StorageAccountType] <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aaf23-107">說明</span><span class="sxs-lookup"><span data-stu-id="aaf23-107">DESCRIPTION</span></span>
<span data-ttu-id="aaf23-108">**載入 AzVMDataDisk** Cmdlet 會將資料磁片新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="aaf23-108">The **Add-AzVMDataDisk** cmdlet adds a data disk to a virtual machine.</span></span>
<span data-ttu-id="aaf23-109">您可以在建立虛擬機器時新增資料磁片，也可以將資料磁片新增至現有的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="aaf23-109">You can add a data disk when you create a virtual machine, or you can add a data disk to an existing virtual machine.</span></span>

## <span data-ttu-id="aaf23-110">示例</span><span class="sxs-lookup"><span data-stu-id="aaf23-110">EXAMPLES</span></span>

### <span data-ttu-id="aaf23-111">範例1：將資料磁片新增至新的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="aaf23-111">Example 1: Add data disks to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

<span data-ttu-id="aaf23-112">第一個命令會建立一個虛擬電腦物件，然後將它儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="aaf23-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="aaf23-113">該命令會將名稱和大小指派給虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="aaf23-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="aaf23-114">接下來的三個命令會將三個數據磁片的路徑指派給 $DataDiskVhdUri 01、$DataDiskVhdUri 02 及 $DataDiskVhdUri 3 個變數。</span><span class="sxs-lookup"><span data-stu-id="aaf23-114">The next three commands assign paths of three data disks to the $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03 variables.</span></span>
<span data-ttu-id="aaf23-115">這個方法只是為了讓您瞭解下列命令的可讀性。</span><span class="sxs-lookup"><span data-stu-id="aaf23-115">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="aaf23-116">最後三個命令會將資料磁片新增至儲存在 $VirtualMachine 的虛擬機器中。</span><span class="sxs-lookup"><span data-stu-id="aaf23-116">The final three commands each adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="aaf23-117">此命令會指定磁片的名稱和位置，以及磁片的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="aaf23-117">The command specifies the name and location for the disk, and other properties of the disk.</span></span>
<span data-ttu-id="aaf23-118">每個磁片的 URI 都儲存在 $DataDiskVhdUri 01、$DataDiskVhdUri 02 和 $DataDiskVhdUri 03 中。</span><span class="sxs-lookup"><span data-stu-id="aaf23-118">The URI of each disk is stored in $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03.</span></span>

### <span data-ttu-id="aaf23-119">範例2：新增資料磁片至現有的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="aaf23-119">Example 2: Add a data disk to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="aaf23-120">第一個命令會使用 [AzVM](./Get-AzVM.md) Cmdlet 取得名為 VirtualMachine07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="aaf23-120">The first command gets the virtual machine named VirtualMachine07 by using the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="aaf23-121">該命令會將虛擬機器儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="aaf23-121">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="aaf23-122">第二個命令會將資料磁片新增至儲存在 $VirtualMachine 的虛擬機器中。</span><span class="sxs-lookup"><span data-stu-id="aaf23-122">The second command adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="aaf23-123">Final 命令會更新儲存在 ResourceGroup11 中 $VirtualMachine 的虛擬機器狀態。</span><span class="sxs-lookup"><span data-stu-id="aaf23-123">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

### <span data-ttu-id="aaf23-124">範例3：從通用使用者影像將資料磁片新增至新的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="aaf23-124">Example 3: Add a data disk to a new virtual machine from a generalized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

<span data-ttu-id="aaf23-125">第一個命令會建立一個虛擬電腦物件，並將它儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="aaf23-125">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="aaf23-126">該命令會將名稱和大小指派給虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="aaf23-126">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="aaf23-127">接下來的兩個命令會將資料影像和資料磁片的路徑指派給 $DataImageUri，並分別 $DataDiskUri 變數。</span><span class="sxs-lookup"><span data-stu-id="aaf23-127">The next two commands assign paths for the data image and data disks to the $DataImageUri and $DataDiskUri variables respectively.</span></span>
<span data-ttu-id="aaf23-128">這個方法是用來改善下列命令的可讀性。</span><span class="sxs-lookup"><span data-stu-id="aaf23-128">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="aaf23-129">最終命令會將資料磁片新增至儲存在 $VirtualMachine 的虛擬機器中。</span><span class="sxs-lookup"><span data-stu-id="aaf23-129">The final commands adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="aaf23-130">此命令會指定磁片的名稱和位置，以及磁片的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="aaf23-130">The command specifies the name and location for the disk and other properties of the disk.</span></span>

### <span data-ttu-id="aaf23-131">範例4：從特殊的使用者影像將資料磁片新增至新的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="aaf23-131">Example 4: Add data disks to a new virtual machine from a specialized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

<span data-ttu-id="aaf23-132">第一個命令會建立一個虛擬電腦物件，並將它儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="aaf23-132">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="aaf23-133">該命令會將名稱和大小指派給虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="aaf23-133">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="aaf23-134">Next 命令會將資料磁片的路徑指派給 $DataDiskUri 變數。</span><span class="sxs-lookup"><span data-stu-id="aaf23-134">The next commands assigns paths of the data disk to the $DataDiskUri variable.</span></span>
<span data-ttu-id="aaf23-135">這個方法是用來改善下列命令的可讀性。</span><span class="sxs-lookup"><span data-stu-id="aaf23-135">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="aaf23-136">最終命令會將資料磁片新增至儲存在 $VirtualMachine 的虛擬機器中。</span><span class="sxs-lookup"><span data-stu-id="aaf23-136">The final command add a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="aaf23-137">此命令會指定磁片的名稱和位置，以及磁片的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="aaf23-137">The command specifies the name and location for the disk, and other properties of the disk.</span></span>

## <span data-ttu-id="aaf23-138">參數</span><span class="sxs-lookup"><span data-stu-id="aaf23-138">PARAMETERS</span></span>

### <span data-ttu-id="aaf23-139">-快取</span><span class="sxs-lookup"><span data-stu-id="aaf23-139">-Caching</span></span>
<span data-ttu-id="aaf23-140">指定磁片的快取模式。</span><span class="sxs-lookup"><span data-stu-id="aaf23-140">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="aaf23-141">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="aaf23-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="aaf23-142">唯讀</span><span class="sxs-lookup"><span data-stu-id="aaf23-142">ReadOnly</span></span>
- <span data-ttu-id="aaf23-143">讀</span><span class="sxs-lookup"><span data-stu-id="aaf23-143">ReadWrite</span></span>
- <span data-ttu-id="aaf23-144">None 預設值為 ReadWrite。</span><span class="sxs-lookup"><span data-stu-id="aaf23-144">None The default value is ReadWrite.</span></span>
<span data-ttu-id="aaf23-145">變更此值會導致虛擬機器重新開機。</span><span class="sxs-lookup"><span data-stu-id="aaf23-145">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="aaf23-146">此設定會影響磁片的一致性和效能。</span><span class="sxs-lookup"><span data-stu-id="aaf23-146">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="aaf23-147">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="aaf23-147">-CreateOption</span></span>
<span data-ttu-id="aaf23-148">指定此 Cmdlet 是否在虛擬機器中從平臺或使用者影像建立磁片、建立空白磁片，或附加現有磁片。</span><span class="sxs-lookup"><span data-stu-id="aaf23-148">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="aaf23-149">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="aaf23-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="aaf23-150">選用.</span><span class="sxs-lookup"><span data-stu-id="aaf23-150">Attach.</span></span>
<span data-ttu-id="aaf23-151">指定此選項以從專用磁片建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="aaf23-151">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="aaf23-152">當您指定此選項時，請勿指定 *SourceImageUri* 參數。</span><span class="sxs-lookup"><span data-stu-id="aaf23-152">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="aaf23-153">您需要 *VhdUri* ，才能告知 Azure 平臺將虛擬硬碟的位置 (VHD) 附加成資料磁片至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="aaf23-153">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="aaf23-154">有空.</span><span class="sxs-lookup"><span data-stu-id="aaf23-154">Empty.</span></span>
<span data-ttu-id="aaf23-155">指定此程式以建立空白的資料磁片。</span><span class="sxs-lookup"><span data-stu-id="aaf23-155">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="aaf23-156">FromImage.</span><span class="sxs-lookup"><span data-stu-id="aaf23-156">FromImage.</span></span>
<span data-ttu-id="aaf23-157">指定此選項以從通用影像或磁片建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="aaf23-157">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="aaf23-158">當您指定此選項時，您必須指定 *SourceImageUri* 參數，以告知 Azure 平臺要作為資料磁片附加的 VHD 位置。</span><span class="sxs-lookup"><span data-stu-id="aaf23-158">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="aaf23-159">*VhdUri* 參數是用來識別虛擬機器所使用的資料磁片 VHD 儲存位置。</span><span class="sxs-lookup"><span data-stu-id="aaf23-159">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

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

### <span data-ttu-id="aaf23-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaf23-160">-DefaultProfile</span></span>
<span data-ttu-id="aaf23-161">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="aaf23-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aaf23-162">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="aaf23-162">-DiskEncryptionSetId</span></span>
<span data-ttu-id="aaf23-163">指定客戶管理磁片加密集的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="aaf23-163">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="aaf23-164">只能為受管理的磁片指定這種情況。</span><span class="sxs-lookup"><span data-stu-id="aaf23-164">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="aaf23-165">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="aaf23-165">-DiskSizeInGB</span></span>
<span data-ttu-id="aaf23-166">指定要附加至虛擬機器的空白磁片大小（以 gb 為位元組）。</span><span class="sxs-lookup"><span data-stu-id="aaf23-166">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

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

### <span data-ttu-id="aaf23-167">-Lun</span><span class="sxs-lookup"><span data-stu-id="aaf23-167">-Lun</span></span>
<span data-ttu-id="aaf23-168">指定資料磁片的邏輯單元號碼 (LUN) 。</span><span class="sxs-lookup"><span data-stu-id="aaf23-168">Specifies the logical unit number (LUN) for a data disk.</span></span>

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

### <span data-ttu-id="aaf23-169">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="aaf23-169">-ManagedDiskId</span></span>
<span data-ttu-id="aaf23-170">指定受管理磁片的 ID。</span><span class="sxs-lookup"><span data-stu-id="aaf23-170">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="aaf23-171">-名稱</span><span class="sxs-lookup"><span data-stu-id="aaf23-171">-Name</span></span>
<span data-ttu-id="aaf23-172">指定要新增的資料磁片名稱。</span><span class="sxs-lookup"><span data-stu-id="aaf23-172">Specifies the name of the data disk to add.</span></span>

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

### <span data-ttu-id="aaf23-173">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="aaf23-173">-SourceImageUri</span></span>
<span data-ttu-id="aaf23-174">指定此 Cmdlet 附加磁片的來源 URI。</span><span class="sxs-lookup"><span data-stu-id="aaf23-174">Specifies the source URI of the disk that this cmdlet attaches.</span></span>

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

### <span data-ttu-id="aaf23-175">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="aaf23-175">-StorageAccountType</span></span>
<span data-ttu-id="aaf23-176">指定受管理磁片的儲存帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="aaf23-176">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="aaf23-177">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="aaf23-177">-VhdUri</span></span>
<span data-ttu-id="aaf23-178">指定要在使用平臺影像或使用者影像時建立的虛擬硬碟 (VHD) 檔案 (URI) 的統一資源識別項。</span><span class="sxs-lookup"><span data-stu-id="aaf23-178">Specifies the Uniform Resource Identifier (URI) for the virtual hard disk (VHD) file to create when a platform image or user image is used.</span></span>
<span data-ttu-id="aaf23-179">這個 Cmdlet 會將影像二進位大型物件 (blob) 複製到此位置。</span><span class="sxs-lookup"><span data-stu-id="aaf23-179">This cmdlet copies the image binary large object (blob) to this location.</span></span>
<span data-ttu-id="aaf23-180">這是啟動虛擬機器的位置。</span><span class="sxs-lookup"><span data-stu-id="aaf23-180">This is the location from which to start the virtual machine.</span></span>

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

### <span data-ttu-id="aaf23-181">-VM</span><span class="sxs-lookup"><span data-stu-id="aaf23-181">-VM</span></span>
<span data-ttu-id="aaf23-182">指定要新增資料磁片的本機虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="aaf23-182">Specifies the local virtual machine object to which to add a data disk.</span></span>
<span data-ttu-id="aaf23-183">您可以使用 **AzVM** Cmdlet 來取得虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="aaf23-183">You can use the **Get-AzVM** cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="aaf23-184">您可以使用 **新的 AzVMConfig** Cmdlet 來建立虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="aaf23-184">You can use the **New-AzVMConfig** cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="aaf23-185">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="aaf23-185">-WriteAccelerator</span></span>
<span data-ttu-id="aaf23-186">指定是否應該在受管理的資料磁片上啟用或停用 WriteAccelerator。</span><span class="sxs-lookup"><span data-stu-id="aaf23-186">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

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

### <span data-ttu-id="aaf23-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaf23-187">CommonParameters</span></span>
<span data-ttu-id="aaf23-188">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="aaf23-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaf23-189">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="aaf23-189">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaf23-190">輸入</span><span class="sxs-lookup"><span data-stu-id="aaf23-190">INPUTS</span></span>

### <span data-ttu-id="aaf23-191">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="aaf23-191">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="aaf23-192">System.object</span><span class="sxs-lookup"><span data-stu-id="aaf23-192">System.String</span></span>

### <span data-ttu-id="aaf23-193">CachingTypes 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="aaf23-193">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="aaf23-194">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="aaf23-194">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="aaf23-195">輸出</span><span class="sxs-lookup"><span data-stu-id="aaf23-195">OUTPUTS</span></span>

### <span data-ttu-id="aaf23-196">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="aaf23-196">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="aaf23-197">PSVirtualMachineScaleSetVM 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="aaf23-197">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="aaf23-198">筆記</span><span class="sxs-lookup"><span data-stu-id="aaf23-198">NOTES</span></span>

## <span data-ttu-id="aaf23-199">相關連結</span><span class="sxs-lookup"><span data-stu-id="aaf23-199">RELATED LINKS</span></span>

[<span data-ttu-id="aaf23-200">移除-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="aaf23-200">Remove-AzVMDataDisk</span></span>](./Remove-AzVMDataDisk.md)

[<span data-ttu-id="aaf23-201">AzVM</span><span class="sxs-lookup"><span data-stu-id="aaf23-201">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="aaf23-202">新-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="aaf23-202">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
