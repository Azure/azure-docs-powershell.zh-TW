---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
ms.openlocfilehash: 032c38c3fcc3b09286b795fd3e0efba85e076807
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613455"
---
# <span data-ttu-id="4c713-101">Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="4c713-101">Add-AzVmssDataDisk</span></span>

## <span data-ttu-id="4c713-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4c713-102">SYNOPSIS</span></span>
<span data-ttu-id="4c713-103">新增資料磁片至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="4c713-103">Adds a data disk to the VMSS.</span></span>

## <span data-ttu-id="4c713-104">句法</span><span class="sxs-lookup"><span data-stu-id="4c713-104">SYNTAX</span></span>

```
Add-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>] [[-Lun] <Int32>]
 [[-Caching] <CachingTypes>] [-WriteAccelerator] [-CreateOption <String>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4c713-105">說明</span><span class="sxs-lookup"><span data-stu-id="4c713-105">DESCRIPTION</span></span>
<span data-ttu-id="4c713-106">**AzVmssDataDisk** Cmdlet 會將資料磁片新增到虛擬電腦規模集 (VMSS) 實例。</span><span class="sxs-lookup"><span data-stu-id="4c713-106">The **Add-AzVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="4c713-107">示例</span><span class="sxs-lookup"><span data-stu-id="4c713-107">EXAMPLES</span></span>

### <span data-ttu-id="4c713-108">範例1：新增資料磁片</span><span class="sxs-lookup"><span data-stu-id="4c713-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="4c713-109">這個命令會將空白的資料磁片新增至 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="4c713-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="4c713-110">參數</span><span class="sxs-lookup"><span data-stu-id="4c713-110">PARAMETERS</span></span>

### <span data-ttu-id="4c713-111">-快取</span><span class="sxs-lookup"><span data-stu-id="4c713-111">-Caching</span></span>
<span data-ttu-id="4c713-112">指定磁片的快取類型。</span><span class="sxs-lookup"><span data-stu-id="4c713-112">Specifies the caching type of the disk.</span></span>

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

### <span data-ttu-id="4c713-113">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="4c713-113">-CreateOption</span></span>
<span data-ttu-id="4c713-114">指定磁片的 [建立] 選項。</span><span class="sxs-lookup"><span data-stu-id="4c713-114">Specifies the create option of the disk.</span></span>

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

### <span data-ttu-id="4c713-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c713-115">-DefaultProfile</span></span>
<span data-ttu-id="4c713-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4c713-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c713-117">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="4c713-117">-DiskSizeGB</span></span>
<span data-ttu-id="4c713-118">指定磁片大小（GB）。</span><span class="sxs-lookup"><span data-stu-id="4c713-118">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="4c713-119">-Lun</span><span class="sxs-lookup"><span data-stu-id="4c713-119">-Lun</span></span>
<span data-ttu-id="4c713-120">指定磁片的邏輯單元號碼。</span><span class="sxs-lookup"><span data-stu-id="4c713-120">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="4c713-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="4c713-121">-Name</span></span>
<span data-ttu-id="4c713-122">指定磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="4c713-122">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="4c713-123">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="4c713-123">-StorageAccountType</span></span>
<span data-ttu-id="4c713-124">指定磁片的儲存帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="4c713-124">Specifies the storage account type of the disk.</span></span>

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

### <span data-ttu-id="4c713-125">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4c713-125">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="4c713-126">指定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="4c713-126">Specify the VMSS object.</span></span>
<span data-ttu-id="4c713-127">您可以使用 [新的-AzVmssConfig](./New-AzVmssConfig.md) Cmdlet 來建立物件。</span><span class="sxs-lookup"><span data-stu-id="4c713-127">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="4c713-128">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="4c713-128">-WriteAccelerator</span></span>
<span data-ttu-id="4c713-129">指定是否應該在資料磁片上啟用或停用 WriteAccelerator。</span><span class="sxs-lookup"><span data-stu-id="4c713-129">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="4c713-130">-確認</span><span class="sxs-lookup"><span data-stu-id="4c713-130">-Confirm</span></span>
<span data-ttu-id="4c713-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4c713-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c713-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c713-132">-WhatIf</span></span>
<span data-ttu-id="4c713-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4c713-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c713-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4c713-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c713-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c713-135">CommonParameters</span></span>
<span data-ttu-id="4c713-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4c713-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c713-137">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4c713-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c713-138">輸入</span><span class="sxs-lookup"><span data-stu-id="4c713-138">INPUTS</span></span>

### <span data-ttu-id="4c713-139">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="4c713-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="4c713-140">System.object</span><span class="sxs-lookup"><span data-stu-id="4c713-140">System.String</span></span>

### <span data-ttu-id="4c713-141">System.object</span><span class="sxs-lookup"><span data-stu-id="4c713-141">System.Int32</span></span>

### <span data-ttu-id="4c713-142">"CachingTypes" 1 [[23.0.0.0]。計算，版本 =，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]]）。）</span><span class="sxs-lookup"><span data-stu-id="4c713-142">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="4c713-143">輸出</span><span class="sxs-lookup"><span data-stu-id="4c713-143">OUTPUTS</span></span>

### <span data-ttu-id="4c713-144">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="4c713-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="4c713-145">筆記</span><span class="sxs-lookup"><span data-stu-id="4c713-145">NOTES</span></span>

## <span data-ttu-id="4c713-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="4c713-146">RELATED LINKS</span></span>
