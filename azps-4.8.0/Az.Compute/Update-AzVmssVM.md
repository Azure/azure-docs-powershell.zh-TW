---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
ms.openlocfilehash: e97c52e8bc22f1eff42a4ffade598fb28c2aff36
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129008"
---
# <span data-ttu-id="b96e4-101">Update-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="b96e4-101">Update-AzVmssVM</span></span>

## <span data-ttu-id="b96e4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b96e4-102">SYNOPSIS</span></span>
<span data-ttu-id="b96e4-103">更新 Vmss VM 的狀態。</span><span class="sxs-lookup"><span data-stu-id="b96e4-103">Updates the state of a Vmss VM.</span></span>

## <span data-ttu-id="b96e4-104">句法</span><span class="sxs-lookup"><span data-stu-id="b96e4-104">SYNTAX</span></span>

### <span data-ttu-id="b96e4-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="b96e4-105">DefaultParameter (Default)</span></span>
```
Update-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b96e4-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="b96e4-106">ResourceIdParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b96e4-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="b96e4-107">ObjectParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b96e4-108">說明</span><span class="sxs-lookup"><span data-stu-id="b96e4-108">DESCRIPTION</span></span>
<span data-ttu-id="b96e4-109">更新 Vmss VM 的狀態。</span><span class="sxs-lookup"><span data-stu-id="b96e4-109">Updates the state of a Vmss VM.</span></span>  <span data-ttu-id="b96e4-110">目前，唯一允許的更新是新增受管理的資料磁片。</span><span class="sxs-lookup"><span data-stu-id="b96e4-110">For now, the only allowed update is adding a managed data disk.</span></span>

## <span data-ttu-id="b96e4-111">示例</span><span class="sxs-lookup"><span data-stu-id="b96e4-111">EXAMPLES</span></span>

### <span data-ttu-id="b96e4-112">範例1：使用 New-AzVMDataDisk 將受管理的資料磁片新增至 Vmss VM</span><span class="sxs-lookup"><span data-stu-id="b96e4-112">Example 1: Add a managed data disk to a Vmss VM using New-AzVMDataDisk</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="b96e4-113">第一個命令會取得現有的受管理磁片。</span><span class="sxs-lookup"><span data-stu-id="b96e4-113">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="b96e4-114">下一個命令會使用受管理的磁片建立資料磁片物件。</span><span class="sxs-lookup"><span data-stu-id="b96e4-114">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="b96e4-115">Next 命令會取得資源群組名稱所提供的現有 Vmss VM、Vmss 名稱和實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="b96e4-115">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="b96e4-116">最後一個命令會透過新增資料磁片來更新 Vmss VM。</span><span class="sxs-lookup"><span data-stu-id="b96e4-116">The final command updates the Vmss VM by adding a new data disk.</span></span>

### <span data-ttu-id="b96e4-117">範例2：使用 Add-AzVMDataDisk 將受管理的資料磁片新增至 Vmss VM</span><span class="sxs-lookup"><span data-stu-id="b96e4-117">Example 2: Add a managed data disk to a Vmss VM using Add-AzVMDataDisk</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="b96e4-118">第一個命令會取得現有的受管理磁片。</span><span class="sxs-lookup"><span data-stu-id="b96e4-118">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="b96e4-119">Next 命令會取得資源群組名稱所提供的現有 Vmss VM、Vmss 名稱和實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="b96e4-119">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="b96e4-120">下一個命令會將受管理的磁片新增至儲存在本機 $VmssVM 的 Vmss VM 中。</span><span class="sxs-lookup"><span data-stu-id="b96e4-120">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="b96e4-121">Final 命令會使用已新增的資料磁片來更新 Vmss VM。</span><span class="sxs-lookup"><span data-stu-id="b96e4-121">The final command updates the Vmss VM with added data disk.</span></span>

### <span data-ttu-id="b96e4-122">範例3</span><span class="sxs-lookup"><span data-stu-id="b96e4-122">Example 3</span></span>

<span data-ttu-id="b96e4-123">更新 Vmss VM 的狀態。</span><span class="sxs-lookup"><span data-stu-id="b96e4-123">Updates the state of a Vmss VM.</span></span> <span data-ttu-id="b96e4-124"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="b96e4-124">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Update-AzVmssVM -InstanceId 0 -ProtectFromScaleIn $false -ProtectFromScaleSetAction $false -ResourceGroupName 'myrg' -VMScaleSetName 'myvmss'
```

## <span data-ttu-id="b96e4-125">參數</span><span class="sxs-lookup"><span data-stu-id="b96e4-125">PARAMETERS</span></span>

### <span data-ttu-id="b96e4-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b96e4-126">-AsJob</span></span>
<span data-ttu-id="b96e4-127">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b96e4-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b96e4-128">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="b96e4-128">-DataDisk</span></span>

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

### <span data-ttu-id="b96e4-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b96e4-129">-DefaultProfile</span></span>
<span data-ttu-id="b96e4-130">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b96e4-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b96e4-131">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="b96e4-131">-InstanceId</span></span>
<span data-ttu-id="b96e4-132">指定 VMSS VM 的實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="b96e4-132">Specifies the instance ID of a VMSS VM.</span></span>

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

### <span data-ttu-id="b96e4-133">-ProtectFromScaleIn</span><span class="sxs-lookup"><span data-stu-id="b96e4-133">-ProtectFromScaleIn</span></span>
<span data-ttu-id="b96e4-134">指示在進行放大作業期間，不應考慮刪除虛擬機器縮放設定 VM。</span><span class="sxs-lookup"><span data-stu-id="b96e4-134">Indicates that the virtual machine scale set VM shouldn't be considered for deletion during a scale-in operation.</span></span>

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

### <span data-ttu-id="b96e4-135">-ProtectFromScaleSetAction</span><span class="sxs-lookup"><span data-stu-id="b96e4-135">-ProtectFromScaleSetAction</span></span>
<span data-ttu-id="b96e4-136">指出模型更新或動作 (包括在 VMSS 上啟動的 [擴展]) ，不應該套用到 VMSS VM。</span><span class="sxs-lookup"><span data-stu-id="b96e4-136">Indicates that model updates or actions (including scale-in) initiated on the VMSS should not be applied to the VMSS VM.</span></span>

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

### <span data-ttu-id="b96e4-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b96e4-137">-ResourceGroupName</span></span>
<span data-ttu-id="b96e4-138">指定 VMSS 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b96e4-138">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="b96e4-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b96e4-139">-ResourceId</span></span>
<span data-ttu-id="b96e4-140">虛擬機器縮放設定 VM 的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="b96e4-140">The resource id for the virtual machine scale set VM</span></span>

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

### <span data-ttu-id="b96e4-141">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="b96e4-141">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="b96e4-142">本機虛擬機器縮放設定 VM 物件</span><span class="sxs-lookup"><span data-stu-id="b96e4-142">Local virtual machine scale set VM object</span></span>

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

### <span data-ttu-id="b96e4-143">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="b96e4-143">-VMScaleSetName</span></span>
<span data-ttu-id="b96e4-144">虛擬機器規模集的名稱</span><span class="sxs-lookup"><span data-stu-id="b96e4-144">The name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="b96e4-145">-確認</span><span class="sxs-lookup"><span data-stu-id="b96e4-145">-Confirm</span></span>
<span data-ttu-id="b96e4-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b96e4-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b96e4-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b96e4-147">-WhatIf</span></span>
<span data-ttu-id="b96e4-148">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b96e4-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b96e4-149">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b96e4-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b96e4-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b96e4-150">CommonParameters</span></span>
<span data-ttu-id="b96e4-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b96e4-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b96e4-152">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b96e4-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b96e4-153">輸入</span><span class="sxs-lookup"><span data-stu-id="b96e4-153">INPUTS</span></span>

### <span data-ttu-id="b96e4-154">System.object</span><span class="sxs-lookup"><span data-stu-id="b96e4-154">System.String</span></span>

### <span data-ttu-id="b96e4-155">PSVirtualMachineDataDisk [] 的計算模型。</span><span class="sxs-lookup"><span data-stu-id="b96e4-155">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk[]</span></span>

### <span data-ttu-id="b96e4-156">PSVirtualMachineScaleSetVM 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="b96e4-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="b96e4-157">輸出</span><span class="sxs-lookup"><span data-stu-id="b96e4-157">OUTPUTS</span></span>

### <span data-ttu-id="b96e4-158">PSVirtualMachineScaleSetVM 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="b96e4-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="b96e4-159">筆記</span><span class="sxs-lookup"><span data-stu-id="b96e4-159">NOTES</span></span>

## <span data-ttu-id="b96e4-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="b96e4-160">RELATED LINKS</span></span>
