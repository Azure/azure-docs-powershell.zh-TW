---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
ms.openlocfilehash: 2f2a6fc8c7e04798e0f2fd3095c2111f12bec65b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906298"
---
# <span data-ttu-id="76c64-101">Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="76c64-101">Add-AzVmssVMDataDisk</span></span>

## <span data-ttu-id="76c64-102">簡介</span><span class="sxs-lookup"><span data-stu-id="76c64-102">SYNOPSIS</span></span>
<span data-ttu-id="76c64-103">新增資料磁片至 Vmss VM。</span><span class="sxs-lookup"><span data-stu-id="76c64-103">Adds a data disk to a Vmss VM.</span></span>

## <span data-ttu-id="76c64-104">語法</span><span class="sxs-lookup"><span data-stu-id="76c64-104">SYNTAX</span></span>

```
Add-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-CreateOption] <String> [-ManagedDiskId] <String> [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-Caching <CachingTypes>] [-DiskSizeInGB <Int32>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76c64-105">描述</span><span class="sxs-lookup"><span data-stu-id="76c64-105">DESCRIPTION</span></span>
<span data-ttu-id="76c64-106">**Add-AzDatas VMDataData Cmdlet** 會將資料磁片新增到 Vmss VM。</span><span class="sxs-lookup"><span data-stu-id="76c64-106">The **Add-AzVmssVMDataDisk** cmdlet adds a data disk to a Vmss VM.</span></span>

## <span data-ttu-id="76c64-107">例子</span><span class="sxs-lookup"><span data-stu-id="76c64-107">EXAMPLES</span></span>

### <span data-ttu-id="76c64-108">範例 1：新增受管理的資料磁片至 Vmss VM。</span><span class="sxs-lookup"><span data-stu-id="76c64-108">Example 1: Add a managed data disk to a Vmss VM.</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVmssVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="76c64-109">第一個命令會獲得現有的受管理磁片。</span><span class="sxs-lookup"><span data-stu-id="76c64-109">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="76c64-110">下一個命令會獲得資源組名、vms 名稱和實例識別碼提供的現有 Vmss VM。</span><span class="sxs-lookup"><span data-stu-id="76c64-110">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="76c64-111">下一個命令會將受管理的磁片新增到儲存在 $VmssVM 中的 Vmss VM。</span><span class="sxs-lookup"><span data-stu-id="76c64-111">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="76c64-112">最後一個命令會以新增的資料磁片更新 Vmss VM。</span><span class="sxs-lookup"><span data-stu-id="76c64-112">The final command updates the Vmss VM with added data disk.</span></span>

## <span data-ttu-id="76c64-113">參數</span><span class="sxs-lookup"><span data-stu-id="76c64-113">PARAMETERS</span></span>

### <span data-ttu-id="76c64-114">-緩存</span><span class="sxs-lookup"><span data-stu-id="76c64-114">-Caching</span></span>
<span data-ttu-id="76c64-115">指定磁片的緩存模式。</span><span class="sxs-lookup"><span data-stu-id="76c64-115">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="76c64-116">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="76c64-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="76c64-117">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="76c64-117">ReadOnly</span></span>
- <span data-ttu-id="76c64-118">朗讀</span><span class="sxs-lookup"><span data-stu-id="76c64-118">ReadWrite</span></span>
- <span data-ttu-id="76c64-119">None 預設值為 ReadWrite。</span><span class="sxs-lookup"><span data-stu-id="76c64-119">None The default value is ReadWrite.</span></span>
<span data-ttu-id="76c64-120">變更此值會導致虛擬機器重新開機。</span><span class="sxs-lookup"><span data-stu-id="76c64-120">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="76c64-121">此設定會影響磁片的一致性與績效。</span><span class="sxs-lookup"><span data-stu-id="76c64-121">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76c64-122">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="76c64-122">-CreateOption</span></span>
<span data-ttu-id="76c64-123">指定此 Cmdlet 是否要從平臺或使用者映射在虛擬機器中建立磁片、建立空白磁片，或附加到現有的磁片。</span><span class="sxs-lookup"><span data-stu-id="76c64-123">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="76c64-124">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="76c64-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="76c64-125">附加。</span><span class="sxs-lookup"><span data-stu-id="76c64-125">Attach.</span></span>
<span data-ttu-id="76c64-126">指定此選項以從特殊磁片建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="76c64-126">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="76c64-127">當您指定此選項時，請勿指定 *SourceImageUri* 參數。</span><span class="sxs-lookup"><span data-stu-id="76c64-127">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="76c64-128">*VhdUri* 是告知 Azure 平臺虛擬硬碟 (VHD) 以資料磁片附加至虛擬機器所需的一切。</span><span class="sxs-lookup"><span data-stu-id="76c64-128">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="76c64-129">空。</span><span class="sxs-lookup"><span data-stu-id="76c64-129">Empty.</span></span>
<span data-ttu-id="76c64-130">指定此選項以建立空白的資料磁片。</span><span class="sxs-lookup"><span data-stu-id="76c64-130">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="76c64-131">FromImage.</span><span class="sxs-lookup"><span data-stu-id="76c64-131">FromImage.</span></span>
<span data-ttu-id="76c64-132">指定此選項以從一般圖像或磁片建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="76c64-132">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="76c64-133">當您指定此選項時，您必須指定 *SourceImageUri* 參數，才能告訴 Azure 平臺要附加為數據磁片的 VHD 位置。</span><span class="sxs-lookup"><span data-stu-id="76c64-133">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="76c64-134">*VhdUri* 參數會用來當虛擬機器使用資料磁片 VHD 時，用來識別資料磁片 VHD 儲存的位置。</span><span class="sxs-lookup"><span data-stu-id="76c64-134">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76c64-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76c64-135">-DefaultProfile</span></span>
<span data-ttu-id="76c64-136">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="76c64-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76c64-137">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="76c64-137">-DiskEncryptionSetId</span></span>
<span data-ttu-id="76c64-138">指定客戶管理的磁片加密集的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="76c64-138">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="76c64-139">這僅適用于受管理的磁片。</span><span class="sxs-lookup"><span data-stu-id="76c64-139">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="76c64-140">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="76c64-140">-DiskSizeInGB</span></span>
<span data-ttu-id="76c64-141">指定要附加到虛擬機器的空白磁片大小 ，以 GB 為單位。</span><span class="sxs-lookup"><span data-stu-id="76c64-141">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76c64-142">-四分位</span><span class="sxs-lookup"><span data-stu-id="76c64-142">-Lun</span></span>
<span data-ttu-id="76c64-143">指定資料磁片的 (或) 邏輯單位編號。</span><span class="sxs-lookup"><span data-stu-id="76c64-143">Specifies the logical unit number (LUN) for a data disk.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76c64-144">-Managed也Id</span><span class="sxs-lookup"><span data-stu-id="76c64-144">-ManagedDiskId</span></span>
<span data-ttu-id="76c64-145">指定受管理磁片的識別碼。</span><span class="sxs-lookup"><span data-stu-id="76c64-145">Specifies the ID of a managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76c64-146">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="76c64-146">-StorageAccountType</span></span>
<span data-ttu-id="76c64-147">指定受管理磁片的儲存帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="76c64-147">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="76c64-148">-VirtualMachineScaleSetMS</span><span class="sxs-lookup"><span data-stu-id="76c64-148">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="76c64-149">指定要新增資料磁片的本機虛擬機器縮放比例集 VM 物件。</span><span class="sxs-lookup"><span data-stu-id="76c64-149">Specifies the local virtual machine scale set VM object to which to add a data disk.</span></span>
<span data-ttu-id="76c64-150">您可以使用 **Get-Az VmsS VM** Cmdlet 來取得虛擬機器縮放集 VM 物件。</span><span class="sxs-lookup"><span data-stu-id="76c64-150">You can use the **Get-AzVmssVM** cmdlet to obtain a virtual machine scale set VM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76c64-151">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="76c64-151">-WriteAccelerator</span></span>
<span data-ttu-id="76c64-152">指定是否應該在受管理的資料磁片上啟用或停用 WriteAccelerator。</span><span class="sxs-lookup"><span data-stu-id="76c64-152">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

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

### <span data-ttu-id="76c64-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76c64-153">CommonParameters</span></span>
<span data-ttu-id="76c64-154">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="76c64-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76c64-155">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76c64-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76c64-156">輸入</span><span class="sxs-lookup"><span data-stu-id="76c64-156">INPUTS</span></span>

### <span data-ttu-id="76c64-157">Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSetVT</span><span class="sxs-lookup"><span data-stu-id="76c64-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

### <span data-ttu-id="76c64-158">System.Int32</span><span class="sxs-lookup"><span data-stu-id="76c64-158">System.Int32</span></span>

### <span data-ttu-id="76c64-159">System.String</span><span class="sxs-lookup"><span data-stu-id="76c64-159">System.String</span></span>

### <span data-ttu-id="76c64-160">Microsoft.Azure.management.Compute.models.CachingTypes</span><span class="sxs-lookup"><span data-stu-id="76c64-160">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

## <span data-ttu-id="76c64-161">輸出</span><span class="sxs-lookup"><span data-stu-id="76c64-161">OUTPUTS</span></span>

### <span data-ttu-id="76c64-162">Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSetVT</span><span class="sxs-lookup"><span data-stu-id="76c64-162">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="76c64-163">筆記</span><span class="sxs-lookup"><span data-stu-id="76c64-163">NOTES</span></span>

## <span data-ttu-id="76c64-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="76c64-164">RELATED LINKS</span></span>
