---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDataDisk.md
ms.openlocfilehash: 293bb0f314b82ed2318684996f9b18c79a3b81d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623479"
---
# <span data-ttu-id="28f68-101">Remove-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="28f68-101">Remove-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="28f68-102">摘要</span><span class="sxs-lookup"><span data-stu-id="28f68-102">SYNOPSIS</span></span>
<span data-ttu-id="28f68-103">從 VMSS 中移除資料磁片。</span><span class="sxs-lookup"><span data-stu-id="28f68-103">Removes a data disk from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28f68-104">句法</span><span class="sxs-lookup"><span data-stu-id="28f68-104">SYNTAX</span></span>

### <span data-ttu-id="28f68-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="28f68-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-Name] <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28f68-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="28f68-106">LunParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-Lun] <Int32> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28f68-107">說明</span><span class="sxs-lookup"><span data-stu-id="28f68-107">DESCRIPTION</span></span>
<span data-ttu-id="28f68-108">**AzureRmVmssDataDisk** Cmdlet 會從虛擬電腦規模集 (VMSS) 實例中移除資料磁片。</span><span class="sxs-lookup"><span data-stu-id="28f68-108">The **Remove-AzureRmVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="28f68-109">示例</span><span class="sxs-lookup"><span data-stu-id="28f68-109">EXAMPLES</span></span>

### <span data-ttu-id="28f68-110">範例1</span><span class="sxs-lookup"><span data-stu-id="28f68-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="28f68-111">這個命令會從 VMSS 物件中移除名為「DataDisk1」的資料磁片。</span><span class="sxs-lookup"><span data-stu-id="28f68-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="28f68-112">範例2</span><span class="sxs-lookup"><span data-stu-id="28f68-112">Example 2</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="28f68-113">這個命令會從 VMSS 物件中移除 LUN 0 的資料磁片。</span><span class="sxs-lookup"><span data-stu-id="28f68-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="28f68-114">參數</span><span class="sxs-lookup"><span data-stu-id="28f68-114">PARAMETERS</span></span>

### <span data-ttu-id="28f68-115">-Lun</span><span class="sxs-lookup"><span data-stu-id="28f68-115">-Lun</span></span>
<span data-ttu-id="28f68-116">指定磁片的邏輯單元號碼。</span><span class="sxs-lookup"><span data-stu-id="28f68-116">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: Int32
Parameter Sets: LunParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28f68-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="28f68-117">-Name</span></span>
<span data-ttu-id="28f68-118">指定磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="28f68-118">Specifies the name of the disk.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28f68-119">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="28f68-119">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="28f68-120">指定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="28f68-120">Specify the VMSS object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28f68-121">-確認</span><span class="sxs-lookup"><span data-stu-id="28f68-121">-Confirm</span></span>
<span data-ttu-id="28f68-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="28f68-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28f68-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28f68-123">-WhatIf</span></span>
<span data-ttu-id="28f68-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="28f68-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28f68-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="28f68-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28f68-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28f68-126">CommonParameters</span></span>
<span data-ttu-id="28f68-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="28f68-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28f68-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="28f68-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28f68-129">輸入</span><span class="sxs-lookup"><span data-stu-id="28f68-129">INPUTS</span></span>

### <span data-ttu-id="28f68-130">VirtualMachineScaleSet 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="28f68-130">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="28f68-131">System.object 系統為 Nullable "1 [（System.object，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]）</span><span class="sxs-lookup"><span data-stu-id="28f68-131">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="28f68-132">輸出</span><span class="sxs-lookup"><span data-stu-id="28f68-132">OUTPUTS</span></span>

### <span data-ttu-id="28f68-133">VirtualMachineScaleSet 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="28f68-133">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="28f68-134">筆記</span><span class="sxs-lookup"><span data-stu-id="28f68-134">NOTES</span></span>

## <span data-ttu-id="28f68-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="28f68-135">RELATED LINKS</span></span>

