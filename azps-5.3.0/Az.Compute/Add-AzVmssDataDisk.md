---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
ms.openlocfilehash: 41728fe644148a575e92136838aaf7f120f89ab7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449892"
---
# <span data-ttu-id="736c2-101">Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="736c2-101">Add-AzVmssDataDisk</span></span>

## <span data-ttu-id="736c2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="736c2-102">SYNOPSIS</span></span>
<span data-ttu-id="736c2-103">新增資料磁片至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="736c2-103">Adds a data disk to the VMSS.</span></span>

## <span data-ttu-id="736c2-104">句法</span><span class="sxs-lookup"><span data-stu-id="736c2-104">SYNTAX</span></span>

```
Add-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>] [[-Lun] <Int32>]
 [[-Caching] <CachingTypes>] [-WriteAccelerator] [-CreateOption <String>] [-DiskSizeGB <Int32>]
 [-DiskIOPSReadWrite <Int64>] [-DiskMBpsReadWrite <Int64>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="736c2-105">說明</span><span class="sxs-lookup"><span data-stu-id="736c2-105">DESCRIPTION</span></span>
<span data-ttu-id="736c2-106">**AzVmssDataDisk** Cmdlet 會將資料磁片新增到虛擬電腦規模集 (VMSS) 實例。</span><span class="sxs-lookup"><span data-stu-id="736c2-106">The **Add-AzVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="736c2-107">示例</span><span class="sxs-lookup"><span data-stu-id="736c2-107">EXAMPLES</span></span>

### <span data-ttu-id="736c2-108">範例1：新增資料磁片</span><span class="sxs-lookup"><span data-stu-id="736c2-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="736c2-109">這個命令會將空白的資料磁片新增至 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="736c2-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="736c2-110">參數</span><span class="sxs-lookup"><span data-stu-id="736c2-110">PARAMETERS</span></span>

### <span data-ttu-id="736c2-111">-快取</span><span class="sxs-lookup"><span data-stu-id="736c2-111">-Caching</span></span>
<span data-ttu-id="736c2-112">指定磁片的快取類型。</span><span class="sxs-lookup"><span data-stu-id="736c2-112">Specifies the caching type of the disk.</span></span>

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

### <span data-ttu-id="736c2-113">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="736c2-113">-CreateOption</span></span>
<span data-ttu-id="736c2-114">指定磁片的 [建立] 選項。</span><span class="sxs-lookup"><span data-stu-id="736c2-114">Specifies the create option of the disk.</span></span>

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

### <span data-ttu-id="736c2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="736c2-115">-DefaultProfile</span></span>
<span data-ttu-id="736c2-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="736c2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="736c2-117">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="736c2-117">-DiskEncryptionSetId</span></span>
<span data-ttu-id="736c2-118">指定客戶管理磁片加密集的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="736c2-118">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="736c2-119">只能為受管理的磁片指定這種情況。</span><span class="sxs-lookup"><span data-stu-id="736c2-119">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="736c2-120">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="736c2-120">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="736c2-121">指定受管理磁片的 Read-Write IOPS。</span><span class="sxs-lookup"><span data-stu-id="736c2-121">Specifies the Read-Write IOPS for the managed disk.</span></span> <span data-ttu-id="736c2-122">只能在 StorageAccountType UltraSSD_LRS 時使用。</span><span class="sxs-lookup"><span data-stu-id="736c2-122">Should be used only when StorageAccountType is UltraSSD_LRS.</span></span> <span data-ttu-id="736c2-123">如果未指定，將根據 diskSizeGB 指派預設值。</span><span class="sxs-lookup"><span data-stu-id="736c2-123">If not specified, a default value would be assigned based on diskSizeGB.</span></span>

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

### <span data-ttu-id="736c2-124">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="736c2-124">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="736c2-125">指定受管理磁片的頻寬（以每秒 MB 為單位）。</span><span class="sxs-lookup"><span data-stu-id="736c2-125">Specifies the bandwidth in MB per second for the managed disk.</span></span> <span data-ttu-id="736c2-126">只能在 StorageAccountType UltraSSD_LRS 時使用。</span><span class="sxs-lookup"><span data-stu-id="736c2-126">Should be used only when StorageAccountType is UltraSSD_LRS.</span></span> <span data-ttu-id="736c2-127">如果未指定，將根據 diskSizeGB 指派預設值。</span><span class="sxs-lookup"><span data-stu-id="736c2-127">If not specified, a default value would be assigned based on diskSizeGB.</span></span>

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

### <span data-ttu-id="736c2-128">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="736c2-128">-DiskSizeGB</span></span>
<span data-ttu-id="736c2-129">指定磁片大小（GB）。</span><span class="sxs-lookup"><span data-stu-id="736c2-129">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="736c2-130">-Lun</span><span class="sxs-lookup"><span data-stu-id="736c2-130">-Lun</span></span>
<span data-ttu-id="736c2-131">指定磁片的邏輯單元號碼。</span><span class="sxs-lookup"><span data-stu-id="736c2-131">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="736c2-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="736c2-132">-Name</span></span>
<span data-ttu-id="736c2-133">指定磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="736c2-133">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="736c2-134">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="736c2-134">-StorageAccountType</span></span>
<span data-ttu-id="736c2-135">指定磁片的儲存帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="736c2-135">Specifies the storage account type of the disk.</span></span>

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

### <span data-ttu-id="736c2-136">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="736c2-136">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="736c2-137">指定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="736c2-137">Specify the VMSS object.</span></span>
<span data-ttu-id="736c2-138">您可以使用 [新的-AzVmssConfig](./New-AzVmssConfig.md) Cmdlet 來建立物件。</span><span class="sxs-lookup"><span data-stu-id="736c2-138">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="736c2-139">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="736c2-139">-WriteAccelerator</span></span>
<span data-ttu-id="736c2-140">指定是否應該在資料磁片上啟用或停用 WriteAccelerator。</span><span class="sxs-lookup"><span data-stu-id="736c2-140">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="736c2-141">-確認</span><span class="sxs-lookup"><span data-stu-id="736c2-141">-Confirm</span></span>
<span data-ttu-id="736c2-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="736c2-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="736c2-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="736c2-143">-WhatIf</span></span>
<span data-ttu-id="736c2-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="736c2-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="736c2-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="736c2-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="736c2-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="736c2-146">CommonParameters</span></span>
<span data-ttu-id="736c2-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="736c2-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="736c2-148">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="736c2-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="736c2-149">輸入</span><span class="sxs-lookup"><span data-stu-id="736c2-149">INPUTS</span></span>

### <span data-ttu-id="736c2-150">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="736c2-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="736c2-151">System.object</span><span class="sxs-lookup"><span data-stu-id="736c2-151">System.String</span></span>

### <span data-ttu-id="736c2-152">System.object</span><span class="sxs-lookup"><span data-stu-id="736c2-152">System.Int32</span></span>

### <span data-ttu-id="736c2-153">"CachingTypes" 1 [[23.0.0.0]。計算，版本 =，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]]）。）</span><span class="sxs-lookup"><span data-stu-id="736c2-153">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="736c2-154">輸出</span><span class="sxs-lookup"><span data-stu-id="736c2-154">OUTPUTS</span></span>

### <span data-ttu-id="736c2-155">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="736c2-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="736c2-156">筆記</span><span class="sxs-lookup"><span data-stu-id="736c2-156">NOTES</span></span>

## <span data-ttu-id="736c2-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="736c2-157">RELATED LINKS</span></span>
