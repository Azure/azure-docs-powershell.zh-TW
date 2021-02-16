---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
ms.openlocfilehash: 5e7901f3e2d18b0707ccf9c5f62f9ab55789a45e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100136562"
---
# <span data-ttu-id="ec348-101">Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="ec348-101">Add-AzVmssVMDataDisk</span></span>

## <span data-ttu-id="ec348-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ec348-102">SYNOPSIS</span></span>
<span data-ttu-id="ec348-103">在 Vmss VM 中新增資料磁片。</span><span class="sxs-lookup"><span data-stu-id="ec348-103">Adds a data disk to a Vmss VM.</span></span>

## <span data-ttu-id="ec348-104">句法</span><span class="sxs-lookup"><span data-stu-id="ec348-104">SYNTAX</span></span>

```
Add-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-CreateOption] <String> [-ManagedDiskId] <String> [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-Caching <CachingTypes>] [-DiskSizeInGB <Int32>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec348-105">說明</span><span class="sxs-lookup"><span data-stu-id="ec348-105">DESCRIPTION</span></span>
<span data-ttu-id="ec348-106">**載入 AzVmssVMDataDisk** Cmdlet 會將資料磁片新增到 Vmss VM。</span><span class="sxs-lookup"><span data-stu-id="ec348-106">The **Add-AzVmssVMDataDisk** cmdlet adds a data disk to a Vmss VM.</span></span>

## <span data-ttu-id="ec348-107">示例</span><span class="sxs-lookup"><span data-stu-id="ec348-107">EXAMPLES</span></span>

### <span data-ttu-id="ec348-108">範例1：將受管理的資料磁片新增至 Vmss VM。</span><span class="sxs-lookup"><span data-stu-id="ec348-108">Example 1: Add a managed data disk to a Vmss VM.</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVmssVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="ec348-109">第一個命令會取得現有的受管理磁片。</span><span class="sxs-lookup"><span data-stu-id="ec348-109">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="ec348-110">Next 命令會取得資源群組名稱所提供的現有 Vmss VM、Vmss 名稱和實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="ec348-110">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="ec348-111">下一個命令會將受管理的磁片新增至儲存在本機 $VmssVM 的 Vmss VM 中。</span><span class="sxs-lookup"><span data-stu-id="ec348-111">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="ec348-112">Final 命令會使用已新增的資料磁片來更新 Vmss VM。</span><span class="sxs-lookup"><span data-stu-id="ec348-112">The final command updates the Vmss VM with added data disk.</span></span>

## <span data-ttu-id="ec348-113">參數</span><span class="sxs-lookup"><span data-stu-id="ec348-113">PARAMETERS</span></span>

### <span data-ttu-id="ec348-114">-快取</span><span class="sxs-lookup"><span data-stu-id="ec348-114">-Caching</span></span>
<span data-ttu-id="ec348-115">指定磁片的快取模式。</span><span class="sxs-lookup"><span data-stu-id="ec348-115">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="ec348-116">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ec348-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ec348-117">唯讀</span><span class="sxs-lookup"><span data-stu-id="ec348-117">ReadOnly</span></span>
- <span data-ttu-id="ec348-118">讀</span><span class="sxs-lookup"><span data-stu-id="ec348-118">ReadWrite</span></span>
- <span data-ttu-id="ec348-119">None 預設值為 ReadWrite。</span><span class="sxs-lookup"><span data-stu-id="ec348-119">None The default value is ReadWrite.</span></span>
<span data-ttu-id="ec348-120">變更此值會導致虛擬機器重新開機。</span><span class="sxs-lookup"><span data-stu-id="ec348-120">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="ec348-121">此設定會影響磁片的一致性和效能。</span><span class="sxs-lookup"><span data-stu-id="ec348-121">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="ec348-122">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="ec348-122">-CreateOption</span></span>
<span data-ttu-id="ec348-123">指定此 Cmdlet 是否在虛擬機器中從平臺或使用者影像建立磁片、建立空白磁片，或附加現有磁片。</span><span class="sxs-lookup"><span data-stu-id="ec348-123">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="ec348-124">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ec348-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ec348-125">選用.</span><span class="sxs-lookup"><span data-stu-id="ec348-125">Attach.</span></span>
<span data-ttu-id="ec348-126">指定此選項以從專用磁片建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="ec348-126">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="ec348-127">當您指定此選項時，請勿指定 *SourceImageUri* 參數。</span><span class="sxs-lookup"><span data-stu-id="ec348-127">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="ec348-128">您需要 *VhdUri* ，才能告知 Azure 平臺將虛擬硬碟的位置 (VHD) 附加成資料磁片至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="ec348-128">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="ec348-129">有空.</span><span class="sxs-lookup"><span data-stu-id="ec348-129">Empty.</span></span>
<span data-ttu-id="ec348-130">指定此程式以建立空白的資料磁片。</span><span class="sxs-lookup"><span data-stu-id="ec348-130">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="ec348-131">FromImage.</span><span class="sxs-lookup"><span data-stu-id="ec348-131">FromImage.</span></span>
<span data-ttu-id="ec348-132">指定此選項以從通用影像或磁片建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="ec348-132">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="ec348-133">當您指定此選項時，您必須指定 *SourceImageUri* 參數，以告知 Azure 平臺要作為資料磁片附加的 VHD 位置。</span><span class="sxs-lookup"><span data-stu-id="ec348-133">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="ec348-134">*VhdUri* 參數是用來識別虛擬機器所使用的資料磁片 VHD 儲存位置。</span><span class="sxs-lookup"><span data-stu-id="ec348-134">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

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

### <span data-ttu-id="ec348-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec348-135">-DefaultProfile</span></span>
<span data-ttu-id="ec348-136">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ec348-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec348-137">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="ec348-137">-DiskEncryptionSetId</span></span>
<span data-ttu-id="ec348-138">指定客戶管理磁片加密集的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ec348-138">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="ec348-139">只能為受管理的磁片指定這種情況。</span><span class="sxs-lookup"><span data-stu-id="ec348-139">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="ec348-140">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="ec348-140">-DiskSizeInGB</span></span>
<span data-ttu-id="ec348-141">指定要附加至虛擬機器的空白磁片大小（以 gb 為位元組）。</span><span class="sxs-lookup"><span data-stu-id="ec348-141">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

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

### <span data-ttu-id="ec348-142">-Lun</span><span class="sxs-lookup"><span data-stu-id="ec348-142">-Lun</span></span>
<span data-ttu-id="ec348-143">指定資料磁片的邏輯單元號碼 (LUN) 。</span><span class="sxs-lookup"><span data-stu-id="ec348-143">Specifies the logical unit number (LUN) for a data disk.</span></span>

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

### <span data-ttu-id="ec348-144">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="ec348-144">-ManagedDiskId</span></span>
<span data-ttu-id="ec348-145">指定受管理磁片的 ID。</span><span class="sxs-lookup"><span data-stu-id="ec348-145">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="ec348-146">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="ec348-146">-StorageAccountType</span></span>
<span data-ttu-id="ec348-147">指定受管理磁片的儲存帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="ec348-147">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="ec348-148">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="ec348-148">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="ec348-149">指定要新增資料磁片的本機虛擬機器縮放設定 VM 物件。</span><span class="sxs-lookup"><span data-stu-id="ec348-149">Specifies the local virtual machine scale set VM object to which to add a data disk.</span></span>
<span data-ttu-id="ec348-150">您可以使用 **AzVmssVM** Cmdlet 來取得虛擬機器縮放設定 VM 物件。</span><span class="sxs-lookup"><span data-stu-id="ec348-150">You can use the **Get-AzVmssVM** cmdlet to obtain a virtual machine scale set VM object.</span></span>

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

### <span data-ttu-id="ec348-151">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="ec348-151">-WriteAccelerator</span></span>
<span data-ttu-id="ec348-152">指定是否應該在受管理的資料磁片上啟用或停用 WriteAccelerator。</span><span class="sxs-lookup"><span data-stu-id="ec348-152">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

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

### <span data-ttu-id="ec348-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec348-153">CommonParameters</span></span>
<span data-ttu-id="ec348-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ec348-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec348-155">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ec348-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec348-156">輸入</span><span class="sxs-lookup"><span data-stu-id="ec348-156">INPUTS</span></span>

### <span data-ttu-id="ec348-157">PSVirtualMachineScaleSetVM 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="ec348-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

### <span data-ttu-id="ec348-158">System.object</span><span class="sxs-lookup"><span data-stu-id="ec348-158">System.Int32</span></span>

### <span data-ttu-id="ec348-159">System.object</span><span class="sxs-lookup"><span data-stu-id="ec348-159">System.String</span></span>

### <span data-ttu-id="ec348-160">CachingTypes 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="ec348-160">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

## <span data-ttu-id="ec348-161">輸出</span><span class="sxs-lookup"><span data-stu-id="ec348-161">OUTPUTS</span></span>

### <span data-ttu-id="ec348-162">PSVirtualMachineScaleSetVM 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="ec348-162">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="ec348-163">筆記</span><span class="sxs-lookup"><span data-stu-id="ec348-163">NOTES</span></span>

## <span data-ttu-id="ec348-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="ec348-164">RELATED LINKS</span></span>
