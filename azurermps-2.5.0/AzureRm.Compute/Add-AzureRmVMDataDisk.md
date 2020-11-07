---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmdatadisk
schema: 2.0.0
ms.openlocfilehash: d644f0bdb770ec1c6b26656cb7bf8709ee369a05
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801437"
---
# <span data-ttu-id="6a496-101">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="6a496-101">Add-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="6a496-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6a496-102">SYNOPSIS</span></span>
<span data-ttu-id="6a496-103">將資料磁片新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="6a496-103">Adds a data disk to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a496-104">句法</span><span class="sxs-lookup"><span data-stu-id="6a496-104">SYNTAX</span></span>

```
Add-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <DiskCreateOptionTypes>
 [[-SourceImageUri] <String>] [[-ManagedDiskId] <String>] [[-StorageAccountType] <StorageAccountTypes>]
 [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a496-105">說明</span><span class="sxs-lookup"><span data-stu-id="6a496-105">DESCRIPTION</span></span>
<span data-ttu-id="6a496-106">**載入 AzureRmVMDataDisk** Cmdlet 會將資料磁片新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="6a496-106">The **Add-AzureRmVMDataDisk** cmdlet adds a data disk to a virtual machine.</span></span>
<span data-ttu-id="6a496-107">您可以在建立虛擬機器時新增資料磁片，也可以將資料磁片新增至現有的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="6a496-107">You can add a data disk when you create a virtual machine, or you can add a data disk to an existing virtual machine.</span></span>

## <span data-ttu-id="6a496-108">示例</span><span class="sxs-lookup"><span data-stu-id="6a496-108">EXAMPLES</span></span>

### <span data-ttu-id="6a496-109">範例1：將資料磁片新增至新的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="6a496-109">Example 1: Add data disks to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

<span data-ttu-id="6a496-110">第一個命令會建立一個虛擬電腦物件，然後將它儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="6a496-110">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="6a496-111">該命令會將名稱和大小指派給虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="6a496-111">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="6a496-112">接下來的三個命令會將三個數據磁片的路徑指派給 $DataDiskVhdUri 01、$DataDiskVhdUri 02 及 $DataDiskVhdUri 3 個變數。</span><span class="sxs-lookup"><span data-stu-id="6a496-112">The next three commands assign paths of three data disks to the $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03 variables.</span></span>
<span data-ttu-id="6a496-113">這個方法只是為了讓您瞭解下列命令的可讀性。</span><span class="sxs-lookup"><span data-stu-id="6a496-113">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="6a496-114">最後三個命令會將資料磁片新增至儲存在 $VirtualMachine 的虛擬機器中。</span><span class="sxs-lookup"><span data-stu-id="6a496-114">The final three commands each adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="6a496-115">此命令會指定磁片的名稱和位置，以及磁片的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="6a496-115">The command specifies the name and location for the disk, and other properties of the disk.</span></span>
<span data-ttu-id="6a496-116">每個磁片的 URI 都儲存在 $DataDiskVhdUri 01、$DataDiskVhdUri 02 和 $DataDiskVhdUri 03 中。</span><span class="sxs-lookup"><span data-stu-id="6a496-116">The URI of each disk is stored in $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03.</span></span>

### <span data-ttu-id="6a496-117">範例2：新增資料磁片至現有的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="6a496-117">Example 2: Add a data disk to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="6a496-118">第一個命令會使用 [AzureRmVM](./Get-AzureRmVM.md) Cmdlet 取得名為 VirtualMachine07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="6a496-118">The first command gets the virtual machine named VirtualMachine07 by using the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="6a496-119">該命令會將虛擬機器儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="6a496-119">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="6a496-120">第二個命令會將資料磁片新增至儲存在 $VirtualMachine 的虛擬機器中。</span><span class="sxs-lookup"><span data-stu-id="6a496-120">The second command adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="6a496-121">Final 命令會更新儲存在 ResourceGroup11 中 $VirtualMachine 的虛擬機器狀態。</span><span class="sxs-lookup"><span data-stu-id="6a496-121">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

### <span data-ttu-id="6a496-122">範例3：從通用使用者影像將資料磁片新增至新的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="6a496-122">Example 3: Add a data disk to a new virtual machine from a generalized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

<span data-ttu-id="6a496-123">第一個命令會建立一個虛擬電腦物件，並將它儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="6a496-123">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="6a496-124">該命令會將名稱和大小指派給虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="6a496-124">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="6a496-125">接下來的兩個命令會將資料影像和資料磁片的路徑指派給 $DataImageUri，並分別 $DataDiskUri 變數。</span><span class="sxs-lookup"><span data-stu-id="6a496-125">The next two commands assign paths for the data image and data disks to the $DataImageUri and $DataDiskUri variables respectively.</span></span>
<span data-ttu-id="6a496-126">這個方法是用來改善下列命令的可讀性。</span><span class="sxs-lookup"><span data-stu-id="6a496-126">This approach is used to improve the readability of the following commands.</span></span>

<span data-ttu-id="6a496-127">最終命令會將資料磁片新增至儲存在 $VirtualMachine 的虛擬機器中。</span><span class="sxs-lookup"><span data-stu-id="6a496-127">The final commands adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="6a496-128">此命令會指定磁片的名稱和位置，以及磁片的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="6a496-128">The command specifies the name and location for the disk and other properties of the disk.</span></span>

### <span data-ttu-id="6a496-129">範例4：從特殊的使用者影像將資料磁片新增至新的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="6a496-129">Example 4: Add data disks to a new virtual machine from a specialized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

<span data-ttu-id="6a496-130">第一個命令會建立一個虛擬電腦物件，並將它儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="6a496-130">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="6a496-131">該命令會將名稱和大小指派給虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="6a496-131">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="6a496-132">Next 命令會將資料磁片的路徑指派給 $DataDiskUri 變數。</span><span class="sxs-lookup"><span data-stu-id="6a496-132">The next commands assigns paths of the data disk to the $DataDiskUri variable.</span></span>
<span data-ttu-id="6a496-133">這個方法是用來改善下列命令的可讀性。</span><span class="sxs-lookup"><span data-stu-id="6a496-133">This approach is used to improve the readability of the following commands.</span></span>

<span data-ttu-id="6a496-134">最終命令會將資料磁片新增至儲存在 $VirtualMachine 的虛擬機器中。</span><span class="sxs-lookup"><span data-stu-id="6a496-134">The final command add a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="6a496-135">此命令會指定磁片的名稱和位置，以及磁片的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="6a496-135">The command specifies the name and location for the disk, and other properties of the disk.</span></span>

## <span data-ttu-id="6a496-136">參數</span><span class="sxs-lookup"><span data-stu-id="6a496-136">PARAMETERS</span></span>

### <span data-ttu-id="6a496-137">-快取</span><span class="sxs-lookup"><span data-stu-id="6a496-137">-Caching</span></span>
<span data-ttu-id="6a496-138">指定磁片的快取模式。</span><span class="sxs-lookup"><span data-stu-id="6a496-138">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="6a496-139">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="6a496-139">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6a496-140">唯讀</span><span class="sxs-lookup"><span data-stu-id="6a496-140">ReadOnly</span></span>
- <span data-ttu-id="6a496-141">讀</span><span class="sxs-lookup"><span data-stu-id="6a496-141">ReadWrite</span></span>
- <span data-ttu-id="6a496-142">所有</span><span class="sxs-lookup"><span data-stu-id="6a496-142">None</span></span>

<span data-ttu-id="6a496-143">預設值為 ReadWrite。</span><span class="sxs-lookup"><span data-stu-id="6a496-143">The default value is ReadWrite.</span></span>
<span data-ttu-id="6a496-144">變更此值會導致虛擬機器重新開機。</span><span class="sxs-lookup"><span data-stu-id="6a496-144">Changing this value causes the virtual machine to restart.</span></span>

<span data-ttu-id="6a496-145">此設定會影響磁片的一致性和效能。</span><span class="sxs-lookup"><span data-stu-id="6a496-145">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a496-146">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="6a496-146">-CreateOption</span></span>
<span data-ttu-id="6a496-147">指定此 Cmdlet 是否在虛擬機器中從平臺或使用者影像建立磁片、建立空白磁片，或附加現有磁片。</span><span class="sxs-lookup"><span data-stu-id="6a496-147">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="6a496-148">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="6a496-148">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6a496-149">選用.</span><span class="sxs-lookup"><span data-stu-id="6a496-149">Attach.</span></span>
<span data-ttu-id="6a496-150">指定此選項以從專用磁片建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="6a496-150">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="6a496-151">當您指定此選項時，請勿指定 *SourceImageUri* 參數。</span><span class="sxs-lookup"><span data-stu-id="6a496-151">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="6a496-152">您需要 *VhdUri* ，才能告知 Azure 平臺將虛擬硬碟的位置 (VHD) 附加成資料磁片至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="6a496-152">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="6a496-153">有空.</span><span class="sxs-lookup"><span data-stu-id="6a496-153">Empty.</span></span>
<span data-ttu-id="6a496-154">指定此程式以建立空白的資料磁片。</span><span class="sxs-lookup"><span data-stu-id="6a496-154">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="6a496-155">FromImage.</span><span class="sxs-lookup"><span data-stu-id="6a496-155">FromImage.</span></span>
<span data-ttu-id="6a496-156">指定此選項以從通用影像或磁片建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="6a496-156">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="6a496-157">當您指定此選項時，您必須指定 *SourceImageUri* 參數，以告知 Azure 平臺要作為資料磁片附加的 VHD 位置。</span><span class="sxs-lookup"><span data-stu-id="6a496-157">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="6a496-158">*VhdUri* 參數是用來識別虛擬機器所使用的資料磁片 VHD 儲存位置。</span><span class="sxs-lookup"><span data-stu-id="6a496-158">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

```yaml
Type: DiskCreateOptionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a496-159">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a496-159">-DefaultProfile</span></span>
<span data-ttu-id="6a496-160">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6a496-160">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a496-161">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="6a496-161">-DiskSizeInGB</span></span>
<span data-ttu-id="6a496-162">指定要附加至虛擬機器的空白磁片大小（以 gb 為位元組）。</span><span class="sxs-lookup"><span data-stu-id="6a496-162">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a496-163">-Lun</span><span class="sxs-lookup"><span data-stu-id="6a496-163">-Lun</span></span>
<span data-ttu-id="6a496-164">指定資料磁片的邏輯單元號碼 (LUN) 。</span><span class="sxs-lookup"><span data-stu-id="6a496-164">Specifies the logical unit number (LUN) for a data disk.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a496-165">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="6a496-165">-ManagedDiskId</span></span>
<span data-ttu-id="6a496-166">指定受管理磁片的 ID。</span><span class="sxs-lookup"><span data-stu-id="6a496-166">Specifies the ID of a managed disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a496-167">-名稱</span><span class="sxs-lookup"><span data-stu-id="6a496-167">-Name</span></span>
<span data-ttu-id="6a496-168">指定要新增的資料磁片名稱。</span><span class="sxs-lookup"><span data-stu-id="6a496-168">Specifies the name of the data disk to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a496-169">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="6a496-169">-SourceImageUri</span></span>
<span data-ttu-id="6a496-170">指定此 Cmdlet 附加磁片的來源 URI。</span><span class="sxs-lookup"><span data-stu-id="6a496-170">Specifies the source URI of the disk that this cmdlet attaches.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SourceImage

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a496-171">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="6a496-171">-StorageAccountType</span></span>
<span data-ttu-id="6a496-172">指定受管理磁片的儲存帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="6a496-172">Specifies the storage account type of managed disk.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a496-173">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="6a496-173">-VhdUri</span></span>
<span data-ttu-id="6a496-174">指定要在使用平臺影像或使用者影像時建立的虛擬硬碟 (VHD) 檔案 (URI) 的統一資源識別項。</span><span class="sxs-lookup"><span data-stu-id="6a496-174">Specifies the Uniform Resource Identifier (URI) for the virtual hard disk (VHD) file to create when a platform image or user image is used.</span></span>
<span data-ttu-id="6a496-175">這個 Cmdlet 會將影像二進位大型物件 (blob) 複製到此位置。</span><span class="sxs-lookup"><span data-stu-id="6a496-175">This cmdlet copies the image binary large object (blob) to this location.</span></span>
<span data-ttu-id="6a496-176">這是啟動虛擬機器的位置。</span><span class="sxs-lookup"><span data-stu-id="6a496-176">This is the location from which to start the virtual machine.</span></span>

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

### <span data-ttu-id="6a496-177">-VM</span><span class="sxs-lookup"><span data-stu-id="6a496-177">-VM</span></span>
<span data-ttu-id="6a496-178">指定要新增資料磁片的本機虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="6a496-178">Specifies the local virtual machine object to which to add a data disk.</span></span>
<span data-ttu-id="6a496-179">您可以使用 **AzureRmVM** Cmdlet 來取得虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="6a496-179">You can use the **Get-AzureRmVM** cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="6a496-180">您可以使用 **新的 AzureRmVMConfig** Cmdlet 來建立虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="6a496-180">You can use the **New-AzureRmVMConfig** cmdlet to create a virtual machine object.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a496-181">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="6a496-181">-WriteAccelerator</span></span>
<span data-ttu-id="6a496-182">指定是否應該在資料磁片上啟用或停用 WriteAccelerator。</span><span class="sxs-lookup"><span data-stu-id="6a496-182">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="6a496-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a496-183">CommonParameters</span></span>
<span data-ttu-id="6a496-184">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6a496-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a496-185">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6a496-185">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a496-186">輸入</span><span class="sxs-lookup"><span data-stu-id="6a496-186">INPUTS</span></span>

### <span data-ttu-id="6a496-187">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6a496-187">PSVirtualMachine</span></span>
<span data-ttu-id="6a496-188">[VM "參數從管線接受類型 ' PSVirtualMachine」的值</span><span class="sxs-lookup"><span data-stu-id="6a496-188">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="6a496-189">輸出</span><span class="sxs-lookup"><span data-stu-id="6a496-189">OUTPUTS</span></span>

### <span data-ttu-id="6a496-190">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="6a496-190">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="6a496-191">筆記</span><span class="sxs-lookup"><span data-stu-id="6a496-191">NOTES</span></span>

## <span data-ttu-id="6a496-192">相關連結</span><span class="sxs-lookup"><span data-stu-id="6a496-192">RELATED LINKS</span></span>

[<span data-ttu-id="6a496-193">移除-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="6a496-193">Remove-AzureRmVMDataDisk</span></span>](./Remove-AzureRmVMDataDisk.md)

[<span data-ttu-id="6a496-194">AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6a496-194">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="6a496-195">新-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="6a496-195">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
