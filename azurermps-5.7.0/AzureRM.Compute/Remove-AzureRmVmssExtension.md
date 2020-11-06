---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssExtension.md
ms.openlocfilehash: 09b90d5ef1f3852f7da39efac9167a8329fba85f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448727"
---
# <span data-ttu-id="0dcae-101">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="0dcae-101">Remove-AzureRmVmssExtension</span></span>

## <span data-ttu-id="0dcae-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0dcae-102">SYNOPSIS</span></span>
<span data-ttu-id="0dcae-103">從 VMSS 中移除延伸。</span><span class="sxs-lookup"><span data-stu-id="0dcae-103">Removes an extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0dcae-104">句法</span><span class="sxs-lookup"><span data-stu-id="0dcae-104">SYNTAX</span></span>

### <span data-ttu-id="0dcae-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0dcae-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-Name] <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0dcae-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0dcae-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-Id] <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0dcae-107">說明</span><span class="sxs-lookup"><span data-stu-id="0dcae-107">DESCRIPTION</span></span>
<span data-ttu-id="0dcae-108">**AzureRmVmssExtension** Cmdlet 會從虛擬電腦縮放集 (VMSS) 中移除延伸。</span><span class="sxs-lookup"><span data-stu-id="0dcae-108">The **Remove-AzureRmVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="0dcae-109">示例</span><span class="sxs-lookup"><span data-stu-id="0dcae-109">EXAMPLES</span></span>

## <span data-ttu-id="0dcae-110">參數</span><span class="sxs-lookup"><span data-stu-id="0dcae-110">PARAMETERS</span></span>

### <span data-ttu-id="0dcae-111">-識別碼</span><span class="sxs-lookup"><span data-stu-id="0dcae-111">-Id</span></span>
<span data-ttu-id="0dcae-112">指定此 Cmdlet 從 VMSS 移除的延伸 ID。</span><span class="sxs-lookup"><span data-stu-id="0dcae-112">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0dcae-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="0dcae-113">-Name</span></span>
<span data-ttu-id="0dcae-114">指定此 Cmdlet 從 VMSS 中移除之延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="0dcae-114">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="0dcae-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0dcae-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="0dcae-116">指定要從中移除延伸的 VMSS。</span><span class="sxs-lookup"><span data-stu-id="0dcae-116">Specifies the VMSS from which to remove the extension from.</span></span>

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

### <span data-ttu-id="0dcae-117">-確認</span><span class="sxs-lookup"><span data-stu-id="0dcae-117">-Confirm</span></span>
<span data-ttu-id="0dcae-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0dcae-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0dcae-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0dcae-119">-WhatIf</span></span>
<span data-ttu-id="0dcae-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0dcae-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0dcae-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0dcae-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0dcae-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dcae-122">CommonParameters</span></span>
<span data-ttu-id="0dcae-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0dcae-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dcae-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0dcae-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dcae-125">輸入</span><span class="sxs-lookup"><span data-stu-id="0dcae-125">INPUTS</span></span>

### <span data-ttu-id="0dcae-126">所有</span><span class="sxs-lookup"><span data-stu-id="0dcae-126">None</span></span>
<span data-ttu-id="0dcae-127">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="0dcae-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0dcae-128">輸出</span><span class="sxs-lookup"><span data-stu-id="0dcae-128">OUTPUTS</span></span>

### <span data-ttu-id="0dcae-129">這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="0dcae-129">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="0dcae-130">筆記</span><span class="sxs-lookup"><span data-stu-id="0dcae-130">NOTES</span></span>

## <span data-ttu-id="0dcae-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="0dcae-131">RELATED LINKS</span></span>

[<span data-ttu-id="0dcae-132">附加 AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="0dcae-132">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)
