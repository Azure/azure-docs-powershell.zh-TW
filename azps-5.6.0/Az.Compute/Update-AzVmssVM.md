---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/update-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
ms.openlocfilehash: 6c483e4146f4bb3ed7207fa5dc0805db239a63d7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902913"
---
# <span data-ttu-id="998ef-101">Update-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="998ef-101">Update-AzVmssVM</span></span>

## <span data-ttu-id="998ef-102">簡介</span><span class="sxs-lookup"><span data-stu-id="998ef-102">SYNOPSIS</span></span>
<span data-ttu-id="998ef-103">更新 Vmss VM 的狀態。</span><span class="sxs-lookup"><span data-stu-id="998ef-103">Updates the state of a Vmss VM.</span></span>

## <span data-ttu-id="998ef-104">語法</span><span class="sxs-lookup"><span data-stu-id="998ef-104">SYNTAX</span></span>

### <span data-ttu-id="998ef-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="998ef-105">DefaultParameter (Default)</span></span>
```
Update-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="998ef-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="998ef-106">ResourceIdParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="998ef-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="998ef-107">ObjectParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="998ef-108">描述</span><span class="sxs-lookup"><span data-stu-id="998ef-108">DESCRIPTION</span></span>
<span data-ttu-id="998ef-109">更新 Vmss VM 的狀態。</span><span class="sxs-lookup"><span data-stu-id="998ef-109">Updates the state of a Vmss VM.</span></span>  <span data-ttu-id="998ef-110">目前，唯一允許的更新是新增受管理的資料磁片。</span><span class="sxs-lookup"><span data-stu-id="998ef-110">For now, the only allowed update is adding a managed data disk.</span></span>

## <span data-ttu-id="998ef-111">例子</span><span class="sxs-lookup"><span data-stu-id="998ef-111">EXAMPLES</span></span>

### <span data-ttu-id="998ef-112">範例 1：使用 New-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="998ef-112">Example 1: Add a managed data disk to a Vmss VM using New-AzVMDataDisk</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="998ef-113">第一個命令會獲得現有的受管理磁片。</span><span class="sxs-lookup"><span data-stu-id="998ef-113">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="998ef-114">下一個命令會使用受管理的磁片建立資料磁片物件。</span><span class="sxs-lookup"><span data-stu-id="998ef-114">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="998ef-115">下一個命令會獲得資源組名、vms 名稱和實例識別碼提供的現有 Vmss VM。</span><span class="sxs-lookup"><span data-stu-id="998ef-115">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="998ef-116">最後一個命令會新增資料磁片來更新 Vmss VM。</span><span class="sxs-lookup"><span data-stu-id="998ef-116">The final command updates the Vmss VM by adding a new data disk.</span></span>

### <span data-ttu-id="998ef-117">範例 2：使用 Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="998ef-117">Example 2: Add a managed data disk to a Vmss VM using Add-AzVMDataDisk</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="998ef-118">第一個命令會獲得現有的受管理磁片。</span><span class="sxs-lookup"><span data-stu-id="998ef-118">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="998ef-119">下一個命令會獲得資源組名、vms 名稱和實例識別碼提供的現有 Vmss VM。</span><span class="sxs-lookup"><span data-stu-id="998ef-119">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="998ef-120">下一個命令會將受管理的磁片新增到儲存在 $VmssVM 中的 Vmss VM。</span><span class="sxs-lookup"><span data-stu-id="998ef-120">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="998ef-121">最後一個命令會以新增的資料磁片更新 Vmss VM。</span><span class="sxs-lookup"><span data-stu-id="998ef-121">The final command updates the Vmss VM with added data disk.</span></span>

### <span data-ttu-id="998ef-122">範例 3</span><span class="sxs-lookup"><span data-stu-id="998ef-122">Example 3</span></span>

<span data-ttu-id="998ef-123">更新 Vmss VM 的狀態。</span><span class="sxs-lookup"><span data-stu-id="998ef-123">Updates the state of a Vmss VM.</span></span> <span data-ttu-id="998ef-124"> (自動) </span><span class="sxs-lookup"><span data-stu-id="998ef-124">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Update-AzVmssVM -InstanceId 0 -ProtectFromScaleIn $false -ProtectFromScaleSetAction $false -ResourceGroupName 'myrg' -VMScaleSetName 'myvmss'
```

## <span data-ttu-id="998ef-125">參數</span><span class="sxs-lookup"><span data-stu-id="998ef-125">PARAMETERS</span></span>

### <span data-ttu-id="998ef-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="998ef-126">-AsJob</span></span>
<span data-ttu-id="998ef-127">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="998ef-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="998ef-128">-Data至上</span><span class="sxs-lookup"><span data-stu-id="998ef-128">-DataDisk</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="998ef-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="998ef-129">-DefaultProfile</span></span>
<span data-ttu-id="998ef-130">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="998ef-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="998ef-131">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="998ef-131">-InstanceId</span></span>
<span data-ttu-id="998ef-132">指定 VMSS VM 的實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="998ef-132">Specifies the instance ID of a VMSS VM.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="998ef-133">-ProtectFromScaleIn</span><span class="sxs-lookup"><span data-stu-id="998ef-133">-ProtectFromScaleIn</span></span>
<span data-ttu-id="998ef-134">表示在縮放作業期間，不應該考慮刪除虛擬機器縮放集 VM。</span><span class="sxs-lookup"><span data-stu-id="998ef-134">Indicates that the virtual machine scale set VM shouldn't be considered for deletion during a scale-in operation.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="998ef-135">-ProtectFromScaleSetAction</span><span class="sxs-lookup"><span data-stu-id="998ef-135">-ProtectFromScaleSetAction</span></span>
<span data-ttu-id="998ef-136">表示模型更新或動作 (，包括) 在 VMSS 上啟動的縮放功能，不應適用于 VMSS VM。</span><span class="sxs-lookup"><span data-stu-id="998ef-136">Indicates that model updates or actions (including scale-in) initiated on the VMSS should not be applied to the VMSS VM.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="998ef-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="998ef-137">-ResourceGroupName</span></span>
<span data-ttu-id="998ef-138">指定 VMSS 的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="998ef-138">Specifies the name of the Resource Group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="998ef-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="998ef-139">-ResourceId</span></span>
<span data-ttu-id="998ef-140">虛擬機器縮放集 VM 的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="998ef-140">The resource id for the virtual machine scale set VM</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="998ef-141">-VirtualMachineScaleSetMS</span><span class="sxs-lookup"><span data-stu-id="998ef-141">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="998ef-142">本機虛擬機器縮放比例集 VM 物件</span><span class="sxs-lookup"><span data-stu-id="998ef-142">Local virtual machine scale set VM object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="998ef-143">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="998ef-143">-VMScaleSetName</span></span>
<span data-ttu-id="998ef-144">虛擬機器縮放集的名稱</span><span class="sxs-lookup"><span data-stu-id="998ef-144">The name of the virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="998ef-145">-確認</span><span class="sxs-lookup"><span data-stu-id="998ef-145">-Confirm</span></span>
<span data-ttu-id="998ef-146">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="998ef-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="998ef-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="998ef-147">-WhatIf</span></span>
<span data-ttu-id="998ef-148">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="998ef-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="998ef-149">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="998ef-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="998ef-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="998ef-150">CommonParameters</span></span>
<span data-ttu-id="998ef-151">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="998ef-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="998ef-152">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="998ef-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="998ef-153">輸入</span><span class="sxs-lookup"><span data-stu-id="998ef-153">INPUTS</span></span>

### <span data-ttu-id="998ef-154">System.String</span><span class="sxs-lookup"><span data-stu-id="998ef-154">System.String</span></span>

### <span data-ttu-id="998ef-155">Microsoft.Azure.Commands.Compute.models.PSVirtualMachineDataAz[]</span><span class="sxs-lookup"><span data-stu-id="998ef-155">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk[]</span></span>

### <span data-ttu-id="998ef-156">Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSetVT</span><span class="sxs-lookup"><span data-stu-id="998ef-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="998ef-157">輸出</span><span class="sxs-lookup"><span data-stu-id="998ef-157">OUTPUTS</span></span>

### <span data-ttu-id="998ef-158">Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSetVT</span><span class="sxs-lookup"><span data-stu-id="998ef-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="998ef-159">筆記</span><span class="sxs-lookup"><span data-stu-id="998ef-159">NOTES</span></span>

## <span data-ttu-id="998ef-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="998ef-160">RELATED LINKS</span></span>
