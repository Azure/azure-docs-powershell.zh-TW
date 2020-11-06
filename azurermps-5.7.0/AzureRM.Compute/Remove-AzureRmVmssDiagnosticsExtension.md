---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 5F135E64-9432-4D08-961F-4604410378A3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDiagnosticsExtension.md
ms.openlocfilehash: 07f679c714c7c8f6f65f89681e3c8df0fff133df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448775"
---
# <span data-ttu-id="55708-101">Remove-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="55708-101">Remove-AzureRmVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="55708-102">摘要</span><span class="sxs-lookup"><span data-stu-id="55708-102">SYNOPSIS</span></span>
<span data-ttu-id="55708-103">從 VMSS 移除診斷延伸。</span><span class="sxs-lookup"><span data-stu-id="55708-103">Removes a diagnostics extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55708-104">句法</span><span class="sxs-lookup"><span data-stu-id="55708-104">SYNTAX</span></span>

```
Remove-AzureRmVmssDiagnosticsExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Name] <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55708-105">說明</span><span class="sxs-lookup"><span data-stu-id="55708-105">DESCRIPTION</span></span>
<span data-ttu-id="55708-106">**AzureRmVmssDiagnosticsExtension** Cmdlet 會從虛擬機器縮放集 (VMSS) 中移除診斷延伸。</span><span class="sxs-lookup"><span data-stu-id="55708-106">The **Remove-AzureRmVmssDiagnosticsExtension** cmdlet removes a diagnostics extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="55708-107">示例</span><span class="sxs-lookup"><span data-stu-id="55708-107">EXAMPLES</span></span>

### <span data-ttu-id="55708-108">範例1：從 VMSS 移除診斷延伸</span><span class="sxs-lookup"><span data-stu-id="55708-108">Example 1: Remove a diagnostics extension from the VMSS</span></span>
```
PS C:\> Remove-AzureRmVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

<span data-ttu-id="55708-109">這個命令會從 VMSS 中移除診斷延伸。</span><span class="sxs-lookup"><span data-stu-id="55708-109">This command removes diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="55708-110">參數</span><span class="sxs-lookup"><span data-stu-id="55708-110">PARAMETERS</span></span>

### <span data-ttu-id="55708-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="55708-111">-Name</span></span>
<span data-ttu-id="55708-112">指定此 Cmdlet 從 VMSS 中移除之延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="55708-112">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55708-113">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="55708-113">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="55708-114">指定要移除延伸的 VMSS。</span><span class="sxs-lookup"><span data-stu-id="55708-114">Specifies the VMSS from which to remove the extension.</span></span>

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

### <span data-ttu-id="55708-115">-確認</span><span class="sxs-lookup"><span data-stu-id="55708-115">-Confirm</span></span>
<span data-ttu-id="55708-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="55708-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55708-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55708-117">-WhatIf</span></span>
<span data-ttu-id="55708-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="55708-118">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="55708-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="55708-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55708-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55708-120">CommonParameters</span></span>
<span data-ttu-id="55708-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="55708-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55708-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="55708-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55708-123">輸入</span><span class="sxs-lookup"><span data-stu-id="55708-123">INPUTS</span></span>

### <span data-ttu-id="55708-124">所有</span><span class="sxs-lookup"><span data-stu-id="55708-124">None</span></span>
<span data-ttu-id="55708-125">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="55708-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="55708-126">輸出</span><span class="sxs-lookup"><span data-stu-id="55708-126">OUTPUTS</span></span>

###  
<span data-ttu-id="55708-127">這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="55708-127">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="55708-128">筆記</span><span class="sxs-lookup"><span data-stu-id="55708-128">NOTES</span></span>

## <span data-ttu-id="55708-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="55708-129">RELATED LINKS</span></span>

[<span data-ttu-id="55708-130">附加 AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="55708-130">Add-AzureRmVmssDiagnosticsExtension</span></span>](./Add-AzureRmVmssDiagnosticsExtension.md)

[<span data-ttu-id="55708-131">移除-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="55708-131">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)

[<span data-ttu-id="55708-132">移除-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="55708-132">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)


