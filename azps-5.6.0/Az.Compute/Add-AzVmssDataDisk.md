---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
ms.openlocfilehash: ec16e946907e7d2815997cbcfb9cbf1563805039
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907793"
---
# <span data-ttu-id="e8c86-101">Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="e8c86-101">Add-AzVmssDataDisk</span></span>

## <span data-ttu-id="e8c86-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e8c86-102">SYNOPSIS</span></span>
<span data-ttu-id="e8c86-103">新增資料磁片至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="e8c86-103">Adds a data disk to the VMSS.</span></span>

## <span data-ttu-id="e8c86-104">語法</span><span class="sxs-lookup"><span data-stu-id="e8c86-104">SYNTAX</span></span>

```
Add-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>] [[-Lun] <Int32>]
 [[-Caching] <CachingTypes>] [-WriteAccelerator] [-CreateOption <String>] [-DiskSizeGB <Int32>]
 [-DiskIOPSReadWrite <Int64>] [-DiskMBpsReadWrite <Int64>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e8c86-105">描述</span><span class="sxs-lookup"><span data-stu-id="e8c86-105">DESCRIPTION</span></span>
<span data-ttu-id="e8c86-106">**Add-Az VmssDataDataData Cmdlet** 會將資料磁片新增到 VMSS 實例 (虛擬機器縮放) 集。</span><span class="sxs-lookup"><span data-stu-id="e8c86-106">The **Add-AzVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="e8c86-107">例子</span><span class="sxs-lookup"><span data-stu-id="e8c86-107">EXAMPLES</span></span>

### <span data-ttu-id="e8c86-108">範例 1：新增資料磁片</span><span class="sxs-lookup"><span data-stu-id="e8c86-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="e8c86-109">此命令會將空白資料磁片新增到 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="e8c86-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="e8c86-110">參數</span><span class="sxs-lookup"><span data-stu-id="e8c86-110">PARAMETERS</span></span>

### <span data-ttu-id="e8c86-111">-緩存</span><span class="sxs-lookup"><span data-stu-id="e8c86-111">-Caching</span></span>
<span data-ttu-id="e8c86-112">指定磁片的緩存類型。</span><span class="sxs-lookup"><span data-stu-id="e8c86-112">Specifies the caching type of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8c86-113">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="e8c86-113">-CreateOption</span></span>
<span data-ttu-id="e8c86-114">指定磁片的建立選項。</span><span class="sxs-lookup"><span data-stu-id="e8c86-114">Specifies the create option of the disk.</span></span>

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

### <span data-ttu-id="e8c86-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8c86-115">-DefaultProfile</span></span>
<span data-ttu-id="e8c86-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8c86-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8c86-117">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="e8c86-117">-DiskEncryptionSetId</span></span>
<span data-ttu-id="e8c86-118">指定客戶管理的磁片加密集的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e8c86-118">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="e8c86-119">這僅適用于受管理的磁片。</span><span class="sxs-lookup"><span data-stu-id="e8c86-119">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="e8c86-120">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="e8c86-120">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="e8c86-121">指定受Read-Write磁片的 IOPS 值。</span><span class="sxs-lookup"><span data-stu-id="e8c86-121">Specifies the Read-Write IOPS for the managed disk.</span></span> <span data-ttu-id="e8c86-122">只有在儲存AccountType 已儲存時UltraSSD_LRS。</span><span class="sxs-lookup"><span data-stu-id="e8c86-122">Should be used only when StorageAccountType is UltraSSD_LRS.</span></span> <span data-ttu-id="e8c86-123">如果未指定，將會根據 diskSizeGB 指派預設值。</span><span class="sxs-lookup"><span data-stu-id="e8c86-123">If not specified, a default value would be assigned based on diskSizeGB.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8c86-124">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="e8c86-124">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="e8c86-125">指定受管理磁片每秒 MB 的頻寬。</span><span class="sxs-lookup"><span data-stu-id="e8c86-125">Specifies the bandwidth in MB per second for the managed disk.</span></span> <span data-ttu-id="e8c86-126">只有在儲存AccountType 已儲存時UltraSSD_LRS。</span><span class="sxs-lookup"><span data-stu-id="e8c86-126">Should be used only when StorageAccountType is UltraSSD_LRS.</span></span> <span data-ttu-id="e8c86-127">如果未指定，將會根據 diskSizeGB 指派預設值。</span><span class="sxs-lookup"><span data-stu-id="e8c86-127">If not specified, a default value would be assigned based on diskSizeGB.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8c86-128">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="e8c86-128">-DiskSizeGB</span></span>
<span data-ttu-id="e8c86-129">指定磁片大小 ，以 GB 為單位。</span><span class="sxs-lookup"><span data-stu-id="e8c86-129">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="e8c86-130">-四分位</span><span class="sxs-lookup"><span data-stu-id="e8c86-130">-Lun</span></span>
<span data-ttu-id="e8c86-131">指定磁片的邏輯單位編號。</span><span class="sxs-lookup"><span data-stu-id="e8c86-131">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8c86-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="e8c86-132">-Name</span></span>
<span data-ttu-id="e8c86-133">指定磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8c86-133">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="e8c86-134">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="e8c86-134">-StorageAccountType</span></span>
<span data-ttu-id="e8c86-135">指定磁片的儲存空間帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="e8c86-135">Specifies the storage account type of the disk.</span></span>

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

### <span data-ttu-id="e8c86-136">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e8c86-136">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="e8c86-137">指定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="e8c86-137">Specify the VMSS object.</span></span>
<span data-ttu-id="e8c86-138">您可以使用 [New-AzEvssConfig](./New-AzVmssConfig.md) Cmdlet 來建立物件。</span><span class="sxs-lookup"><span data-stu-id="e8c86-138">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8c86-139">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="e8c86-139">-WriteAccelerator</span></span>
<span data-ttu-id="e8c86-140">指定資料磁片上是否應該啟用或停用 WriteAccelerator。</span><span class="sxs-lookup"><span data-stu-id="e8c86-140">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="e8c86-141">-確認</span><span class="sxs-lookup"><span data-stu-id="e8c86-141">-Confirm</span></span>
<span data-ttu-id="e8c86-142">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e8c86-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8c86-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8c86-143">-WhatIf</span></span>
<span data-ttu-id="e8c86-144">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e8c86-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8c86-145">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e8c86-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8c86-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8c86-146">CommonParameters</span></span>
<span data-ttu-id="e8c86-147">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e8c86-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8c86-148">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e8c86-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8c86-149">輸入</span><span class="sxs-lookup"><span data-stu-id="e8c86-149">INPUTS</span></span>

### <span data-ttu-id="e8c86-150">Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e8c86-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="e8c86-151">System.String</span><span class="sxs-lookup"><span data-stu-id="e8c86-151">System.String</span></span>

### <span data-ttu-id="e8c86-152">System.Int32</span><span class="sxs-lookup"><span data-stu-id="e8c86-152">System.Int32</span></span>

### <span data-ttu-id="e8c86-153">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="e8c86-153">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="e8c86-154">輸出</span><span class="sxs-lookup"><span data-stu-id="e8c86-154">OUTPUTS</span></span>

### <span data-ttu-id="e8c86-155">Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e8c86-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="e8c86-156">筆記</span><span class="sxs-lookup"><span data-stu-id="e8c86-156">NOTES</span></span>

## <span data-ttu-id="e8c86-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8c86-157">RELATED LINKS</span></span>
