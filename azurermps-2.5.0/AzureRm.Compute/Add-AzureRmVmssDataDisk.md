---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssdatadisk
schema: 2.0.0
ms.openlocfilehash: c91b9dc68bcc0cdecda9ced83a9b3c64452d6413
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800593"
---
# <span data-ttu-id="313fe-101">Add-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="313fe-101">Add-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="313fe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="313fe-102">SYNOPSIS</span></span>
<span data-ttu-id="313fe-103">新增資料磁片至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="313fe-103">Adds a data disk to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="313fe-104">句法</span><span class="sxs-lookup"><span data-stu-id="313fe-104">SYNTAX</span></span>

```
Add-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Lun] <Int32>] [[-Caching] <CachingTypes>] [-WriteAccelerator] [-CreateOption <DiskCreateOptionTypes>]
 [-DiskSizeGB <Int32>] [-StorageAccountType <StorageAccountTypes>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="313fe-105">說明</span><span class="sxs-lookup"><span data-stu-id="313fe-105">DESCRIPTION</span></span>
<span data-ttu-id="313fe-106">**AzureRmVmssDataDisk** Cmdlet 會將資料磁片新增到虛擬電腦規模集 (VMSS) 實例。</span><span class="sxs-lookup"><span data-stu-id="313fe-106">The **Add-AzureRmVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="313fe-107">示例</span><span class="sxs-lookup"><span data-stu-id="313fe-107">EXAMPLES</span></span>

### <span data-ttu-id="313fe-108">範例1：新增資料磁片</span><span class="sxs-lookup"><span data-stu-id="313fe-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzureRmVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="313fe-109">這個命令會將空白的資料磁片新增至 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="313fe-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="313fe-110">參數</span><span class="sxs-lookup"><span data-stu-id="313fe-110">PARAMETERS</span></span>

### <span data-ttu-id="313fe-111">-快取</span><span class="sxs-lookup"><span data-stu-id="313fe-111">-Caching</span></span>
<span data-ttu-id="313fe-112">指定磁片的快取類型。</span><span class="sxs-lookup"><span data-stu-id="313fe-112">Specifies the caching type of the disk.</span></span>

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

### <span data-ttu-id="313fe-113">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="313fe-113">-CreateOption</span></span>
<span data-ttu-id="313fe-114">指定磁片的 [建立] 選項。</span><span class="sxs-lookup"><span data-stu-id="313fe-114">Specifies the create option of the disk.</span></span>

```yaml
Type: DiskCreateOptionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="313fe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="313fe-115">-DefaultProfile</span></span>
<span data-ttu-id="313fe-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="313fe-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="313fe-117">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="313fe-117">-DiskSizeGB</span></span>
<span data-ttu-id="313fe-118">指定磁片大小（GB）。</span><span class="sxs-lookup"><span data-stu-id="313fe-118">Specifies the size of the disk in GB.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="313fe-119">-Lun</span><span class="sxs-lookup"><span data-stu-id="313fe-119">-Lun</span></span>
<span data-ttu-id="313fe-120">指定磁片的邏輯單元號碼。</span><span class="sxs-lookup"><span data-stu-id="313fe-120">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="313fe-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="313fe-121">-Name</span></span>
<span data-ttu-id="313fe-122">指定磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="313fe-122">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="313fe-123">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="313fe-123">-StorageAccountType</span></span>
<span data-ttu-id="313fe-124">指定磁片的儲存帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="313fe-124">Specifies the storage account type of the disk.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="313fe-125">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="313fe-125">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="313fe-126">指定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="313fe-126">Specify the VMSS object.</span></span>
<span data-ttu-id="313fe-127">您可以使用 [新的-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) Cmdlet 來建立物件。</span><span class="sxs-lookup"><span data-stu-id="313fe-127">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="313fe-128">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="313fe-128">-WriteAccelerator</span></span>
<span data-ttu-id="313fe-129">指定是否應該在資料磁片上啟用或停用 WriteAccelerator。</span><span class="sxs-lookup"><span data-stu-id="313fe-129">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="313fe-130">-確認</span><span class="sxs-lookup"><span data-stu-id="313fe-130">-Confirm</span></span>
<span data-ttu-id="313fe-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="313fe-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="313fe-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="313fe-132">-WhatIf</span></span>
<span data-ttu-id="313fe-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="313fe-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="313fe-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="313fe-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="313fe-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="313fe-135">CommonParameters</span></span>
<span data-ttu-id="313fe-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="313fe-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="313fe-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="313fe-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="313fe-138">輸入</span><span class="sxs-lookup"><span data-stu-id="313fe-138">INPUTS</span></span>

### <span data-ttu-id="313fe-139">VirtualMachineScaleSet 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="313fe-139">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="313fe-140">字串 System. Int32 系統。可為 Null 的 `1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[31bf3856ad364e35]. 計算，版本 = 14.0.0.0，Culture = 中性，PublicKeyToken =]] System. null `1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable` 1 [，culture = 中性，publickeytoken = 14.0.0.0，Culture = 無特定，PublicKeyToken = 31bf3856ad364e35]] （"區域性 =]]）</span><span class="sxs-lookup"><span data-stu-id="313fe-140">System.String System.Int32 System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOptionTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="313fe-141">輸出</span><span class="sxs-lookup"><span data-stu-id="313fe-141">OUTPUTS</span></span>

### <span data-ttu-id="313fe-142">VirtualMachineScaleSet 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="313fe-142">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="313fe-143">筆記</span><span class="sxs-lookup"><span data-stu-id="313fe-143">NOTES</span></span>

## <span data-ttu-id="313fe-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="313fe-144">RELATED LINKS</span></span>
