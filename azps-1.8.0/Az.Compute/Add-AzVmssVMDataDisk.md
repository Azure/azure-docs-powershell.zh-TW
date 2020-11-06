---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
ms.openlocfilehash: 81f9e57bd2d815616cfc856246ff6950230f7112
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622814"
---
# <span data-ttu-id="7d009-101">Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="7d009-101">Add-AzVmssVMDataDisk</span></span>

## <span data-ttu-id="7d009-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7d009-102">SYNOPSIS</span></span>
<span data-ttu-id="7d009-103">在 Vmss VM 中新增資料磁片。</span><span class="sxs-lookup"><span data-stu-id="7d009-103">Adds a data disk to a Vmss VM.</span></span>

## <span data-ttu-id="7d009-104">句法</span><span class="sxs-lookup"><span data-stu-id="7d009-104">SYNTAX</span></span>

```
Add-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-CreateOption] <String> [-ManagedDiskId] <String> [-StorageAccountType <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d009-105">說明</span><span class="sxs-lookup"><span data-stu-id="7d009-105">DESCRIPTION</span></span>
<span data-ttu-id="7d009-106">**載入 AzVmssVMDataDisk** Cmdlet 會將資料磁片新增到 Vmss VM。</span><span class="sxs-lookup"><span data-stu-id="7d009-106">The **Add-AzVmssVMDataDisk** cmdlet adds a data disk to a Vmss VM.</span></span>

## <span data-ttu-id="7d009-107">示例</span><span class="sxs-lookup"><span data-stu-id="7d009-107">EXAMPLES</span></span>

### <span data-ttu-id="7d009-108">範例1：將受管理的資料磁片新增至 Vmss VM。</span><span class="sxs-lookup"><span data-stu-id="7d009-108">Example 1: Add a managed data disk to a Vmss VM.</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVmssVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="7d009-109">第一個命令會取得現有的受管理磁片。</span><span class="sxs-lookup"><span data-stu-id="7d009-109">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="7d009-110">Next 命令會取得資源群組名稱所提供的現有 Vmss VM、Vmss 名稱和實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="7d009-110">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="7d009-111">下一個命令會將受管理的磁片新增至儲存在本機 $VmssVM 的 Vmss VM 中。</span><span class="sxs-lookup"><span data-stu-id="7d009-111">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="7d009-112">Final 命令會使用已新增的資料磁片來更新 Vmss VM。</span><span class="sxs-lookup"><span data-stu-id="7d009-112">The final command updates the Vmss VM with added data disk.</span></span>

## <span data-ttu-id="7d009-113">參數</span><span class="sxs-lookup"><span data-stu-id="7d009-113">PARAMETERS</span></span>

### <span data-ttu-id="7d009-114">-快取</span><span class="sxs-lookup"><span data-stu-id="7d009-114">-Caching</span></span>
<span data-ttu-id="7d009-115">指定磁片的快取模式。</span><span class="sxs-lookup"><span data-stu-id="7d009-115">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="7d009-116">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="7d009-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7d009-117">唯讀</span><span class="sxs-lookup"><span data-stu-id="7d009-117">ReadOnly</span></span>
- <span data-ttu-id="7d009-118">讀</span><span class="sxs-lookup"><span data-stu-id="7d009-118">ReadWrite</span></span>
- <span data-ttu-id="7d009-119">None 預設值為 ReadWrite。</span><span class="sxs-lookup"><span data-stu-id="7d009-119">None The default value is ReadWrite.</span></span>
<span data-ttu-id="7d009-120">變更此值會導致虛擬機器重新開機。</span><span class="sxs-lookup"><span data-stu-id="7d009-120">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="7d009-121">此設定會影響磁片的一致性和效能。</span><span class="sxs-lookup"><span data-stu-id="7d009-121">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="7d009-122">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="7d009-122">-CreateOption</span></span>
<span data-ttu-id="7d009-123">指定此 Cmdlet 是否在虛擬機器中從平臺或使用者影像建立磁片、建立空白磁片，或附加現有磁片。</span><span class="sxs-lookup"><span data-stu-id="7d009-123">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="7d009-124">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="7d009-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7d009-125">選用.</span><span class="sxs-lookup"><span data-stu-id="7d009-125">Attach.</span></span>
<span data-ttu-id="7d009-126">指定此選項以從專用磁片建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="7d009-126">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="7d009-127">當您指定此選項時，請勿指定 *SourceImageUri* 參數。</span><span class="sxs-lookup"><span data-stu-id="7d009-127">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="7d009-128">您需要 *VhdUri* ，才能告知 Azure 平臺將虛擬硬碟的位置 (VHD) 附加成資料磁片至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="7d009-128">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="7d009-129">有空.</span><span class="sxs-lookup"><span data-stu-id="7d009-129">Empty.</span></span>
<span data-ttu-id="7d009-130">指定此程式以建立空白的資料磁片。</span><span class="sxs-lookup"><span data-stu-id="7d009-130">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="7d009-131">FromImage.</span><span class="sxs-lookup"><span data-stu-id="7d009-131">FromImage.</span></span>
<span data-ttu-id="7d009-132">指定此選項以從通用影像或磁片建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="7d009-132">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="7d009-133">當您指定此選項時，您必須指定 *SourceImageUri* 參數，以告知 Azure 平臺要作為資料磁片附加的 VHD 位置。</span><span class="sxs-lookup"><span data-stu-id="7d009-133">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="7d009-134">*VhdUri* 參數是用來識別虛擬機器所使用的資料磁片 VHD 儲存位置。</span><span class="sxs-lookup"><span data-stu-id="7d009-134">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

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

### <span data-ttu-id="7d009-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d009-135">-DefaultProfile</span></span>
<span data-ttu-id="7d009-136">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7d009-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d009-137">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="7d009-137">-DiskSizeInGB</span></span>
<span data-ttu-id="7d009-138">指定要附加至虛擬機器的空白磁片大小（以 gb 為位元組）。</span><span class="sxs-lookup"><span data-stu-id="7d009-138">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

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

### <span data-ttu-id="7d009-139">-Lun</span><span class="sxs-lookup"><span data-stu-id="7d009-139">-Lun</span></span>
<span data-ttu-id="7d009-140">指定資料磁片的邏輯單元號碼 (LUN) 。</span><span class="sxs-lookup"><span data-stu-id="7d009-140">Specifies the logical unit number (LUN) for a data disk.</span></span>

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

### <span data-ttu-id="7d009-141">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="7d009-141">-ManagedDiskId</span></span>
<span data-ttu-id="7d009-142">指定受管理磁片的 ID。</span><span class="sxs-lookup"><span data-stu-id="7d009-142">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="7d009-143">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="7d009-143">-StorageAccountType</span></span>
<span data-ttu-id="7d009-144">指定受管理磁片的儲存帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="7d009-144">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="7d009-145">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="7d009-145">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="7d009-146">指定要新增資料磁片的本機虛擬機器縮放設定 VM 物件。</span><span class="sxs-lookup"><span data-stu-id="7d009-146">Specifies the local virtual machine scale set VM object to which to add a data disk.</span></span>
<span data-ttu-id="7d009-147">您可以使用 **AzVmssVM** Cmdlet 來取得虛擬機器縮放設定 VM 物件。</span><span class="sxs-lookup"><span data-stu-id="7d009-147">You can use the **Get-AzVmssVM** cmdlet to obtain a virtual machine scale set VM object.</span></span>

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

### <span data-ttu-id="7d009-148">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="7d009-148">-WriteAccelerator</span></span>
<span data-ttu-id="7d009-149">指定是否應該在受管理的資料磁片上啟用或停用 WriteAccelerator。</span><span class="sxs-lookup"><span data-stu-id="7d009-149">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

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

### <span data-ttu-id="7d009-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d009-150">CommonParameters</span></span>
<span data-ttu-id="7d009-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7d009-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d009-152">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7d009-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d009-153">輸入</span><span class="sxs-lookup"><span data-stu-id="7d009-153">INPUTS</span></span>

### <span data-ttu-id="7d009-154">PSVirtualMachineScaleSetVM 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="7d009-154">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

### <span data-ttu-id="7d009-155">System.object</span><span class="sxs-lookup"><span data-stu-id="7d009-155">System.Int32</span></span>

### <span data-ttu-id="7d009-156">System.object</span><span class="sxs-lookup"><span data-stu-id="7d009-156">System.String</span></span>

### <span data-ttu-id="7d009-157">CachingTypes 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="7d009-157">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

## <span data-ttu-id="7d009-158">輸出</span><span class="sxs-lookup"><span data-stu-id="7d009-158">OUTPUTS</span></span>

### <span data-ttu-id="7d009-159">PSVirtualMachineScaleSetVM 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="7d009-159">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="7d009-160">筆記</span><span class="sxs-lookup"><span data-stu-id="7d009-160">NOTES</span></span>

## <span data-ttu-id="7d009-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="7d009-161">RELATED LINKS</span></span>
